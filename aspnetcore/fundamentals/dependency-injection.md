---
title: .NET Core 中的相依性插入
author: guardrex
description: 了解 ASP.NET Core 如何實作相依性插入以及如何使用它。
ms.author: riande
ms.custom: mvc
ms.date: 07/02/2018
uid: fundamentals/dependency-injection
ms.openlocfilehash: 861370dc689e2420838f639ea0b1fb8f73927e16
ms.sourcegitcommit: 927e510d68f269d8335b5a7c8592621219a90965
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/30/2018
ms.locfileid: "39342415"
---
# <a name="dependency-injection-in-aspnet-core"></a>.NET Core 中的相依性插入

作者：[Steve Smith](https://ardalis.com/)、[Scott Addie](https://scottaddie.com) 與 [Luke Latham](https://github.com/guardrex)

ASP.NET Core 支援相依性插入 (DI) 軟體設計模式，這是用來在類別與其相依性之間達成[控制權反轉 (IoC)](https://deviq.com/inversion-of-control/) \(英文\) 的技術。

如需有關 MVC 控制器內相依性插入的特定詳細資訊，請參閱 <xref:mvc/controllers/dependency-injection>。

[檢視或下載範例程式碼](https://github.com/aspnet/Docs/tree/master/aspnetcore/fundamentals/dependency-injection/samples) \(英文\) ([如何下載](xref:tutorials/index#how-to-download-a-sample))

## <a name="overview-of-dependency-injection"></a>相依性插入概觀

「相依性」是另一個物件所需的任何物件。 檢查具有 `WriteMessage` 方法的下列 `MyDependency` 物件，應用程式中的其他類別相依於此物件：

```csharp
public class MyDependency
{
    public MyDependency()
    {
    }

    public Task WriteMessage(string message)
    {
        Console.WriteLine(
            $"MyDependency.WriteMessage called. Message: {message}");

        return Task.FromResult(0);
    }
}
```

::: moniker range=">= aspnetcore-2.1"

您可以建立 `MyDependency` 類別的執行個體，讓 `WriteMessage` 方法可供類別使用。 `MyDependency` 類別是 `IndexModel` 類別的相依性：

```csharp
public class IndexModel : PageModel
{
    MyDependency _dependency = new MyDependency();

    public async Task OnGetAsync()
    {
        await _myDependency.WriteMessage(
            "IndexModel.OnGetAsync created this message.");
    }
}
```

::: moniker-end

::: moniker range="<= aspnetcore-2.0"

您可以建立 `MyDependency` 類別的執行個體，讓 `WriteMessage` 方法可供類別使用。 `MyDependency` 類別是 `HomeController` 類別的相依性：

```csharp
public class HomeController : Controller
{
    MyDependency _dependency = new MyDependency();

    public async Task<IActionResult> Index()
    {
        await _myDependency.WriteMessage(
            "HomeController.Index created this message.");

        return View();
    }
}
```

::: moniker-end

該類別會建立 `MyDependency` 執行個體並直接相依於該執行個體。 程式碼相依性 (例如前一個範例) 有問題，因此基於下列原因應該避免使用：

* 若要將 `MyDependency` 取代為不同的實作，必須修改該類別。
* 若 `MyDependency` 有相依性，那些相依性必須由該類別設定。 在具有多個相依於 `MyDependency` 之多個類別的大型專案中，設定程式碼在不同的應用程式之間會變得鬆散。
* 此實作難以進行單元測試。 應用程式應該使用模擬 (Mock) 或虛設常式 (Stub) `MyDependency` 類別，這在使用此方法時無法使用。

相依性插入可透過下列方式解決這些問題：

* 使用介面來將相依性資訊抽象化。
* 在服務容器中註冊相依性。 ASP.NET Core 提供內建服務容器 [IServiceProvider](/dotnet/api/system.iserviceprovider)。 服務會在應用程式的 `Startup.ConfigureServices` 方法中註冊。
* 將服務「插入」到服務使用位置之類別的建構函式。 架構會負責建立相依性的執行個體，並在不再需要時將它捨棄。

在[範例應用程式](https://github.com/aspnet/Docs/tree/master/aspnetcore/fundamentals/dependency-injection/samples)中，`IMyDependency` 介面定義了服務提供給應用程式的方法：

::: moniker range=">= aspnetcore-2.1"

[!code-csharp[](dependency-injection/samples/2.x/DependencyInjectionSample/Interfaces/IMyDependency.cs?name=snippet1)]

::: moniker-end

::: moniker range="<= aspnetcore-2.0"

[!code-csharp[](dependency-injection/samples/1.x/DependencyInjectionSample/Interfaces/IMyDependency.cs?name=snippet1)]

::: moniker-end

這個介面是由具象型別 `MyDependency` 所實作：

::: moniker range=">= aspnetcore-2.1"

[!code-csharp[](dependency-injection/samples/2.x/DependencyInjectionSample/Services/MyDependency.cs?name=snippet1)]

::: moniker-end

::: moniker range="<= aspnetcore-2.0"

[!code-csharp[](dependency-injection/samples/1.x/DependencyInjectionSample/Services/MyDependency.cs?name=snippet1)]

::: moniker-end

`MyDependency` 在其建構函式中要求 [ILogger&lt;TCategoryName&gt;](/dotnet/api/microsoft.extensions.logging.ilogger-1)。 以鏈結方式使用相依性插入並非不尋常。 每個要求的相依性接著會要求其自己的相依性。 容器會解決圖形中的相依性，並傳回完全解析的服務。 必須先解析的相依性集合組通常稱為「相依性樹狀結構」、「相依性圖形」或「物件圖形」。

`IMyDependency` 與 `ILogger<TCategoryName>` 必須在服務容器中註冊。 `IMyDependency` 是在 `Startup.ConfigureServices` 中註冊。 `ILogger<TCategoryName>` 是由記錄抽象基礎結構所註冊，所以它是預設由架構所註冊的[架構提供的服務](#framework-provided-services)。

在範例應用程式中，`IMyDependency` 服務是使用具象型別 `MyDependency` 所註冊。 註冊會將服務的存留期範圍限制為單一要求的存留期。 將在此主題稍後將說明[服務存留期](#service-lifetimes)。

::: moniker range=">= aspnetcore-2.1"

[!code-csharp[](dependency-injection/samples/2.x/DependencyInjectionSample/Startup.cs?name=snippet1&highlight=11)]

::: moniker-end

::: moniker range="<= aspnetcore-2.0"

[!code-csharp[](dependency-injection/samples/1.x/DependencyInjectionSample/Startup.cs?name=snippet1&highlight=5)]

::: moniker-end

> [!NOTE]
> 每個 `services.Add<ServiceName>` 擴充方法都會新增 (並且可能會設定) 服務。 例如，`services.AddMvc()` 會新增 Razor Pages 與 MVC 要求的服務。 建議應用程式遵循此慣例。 在 [Microsoft.Extensions.DependencyInjection](/dotnet/api/microsoft.extensions.dependencyinjection) 命名空間中放置擴充方法，以封裝服務註冊群組。

如果服務的建構函式需要基本類型 (例如 `string`)，基本類型可以藉由使用[設定](xref:fundamentals/configuration/index)或[選項模式](xref:fundamentals/configuration/options)來插入：

```csharp
public class MyDependency : IMyDependency
{
    public MyDependency(IConfiguration config)
    {
        var myStringValue = config["MyStringKey"];

        // Use myStringValue
    }

    ...
}
```

服務執行個體是透過服務使用所在之類別建構函式所要求，而且會指派給私人欄位。 該欄位會視需要用來存取整個類別中的服務。

在範例應用程式中，會要求 `IMyDependency` 執行個體並使用它來呼叫服務的 `WriteMessage` 方法：

::: moniker range=">= aspnetcore-2.1"

[!code-csharp[](dependency-injection/samples/2.x/DependencyInjectionSample/Pages/Index.cshtml.cs?name=snippet1&highlight=3,6,13,29-30)]

::: moniker-end

::: moniker range="<= aspnetcore-2.0"

[!code-csharp[](dependency-injection/samples/1.x/DependencyInjectionSample/Controllers/MyDependencyController.cs?name=snippet1&highlight=3,5-8,13-14)]

::: moniker-end

## <a name="framework-provided-services"></a>架構提供的服務

`Startup.ConfigureServices` 方法負責定義應用程式將使用的服務，包括像是 Entity Framework Core 與 ASP.NET Core MVC 等平台功能。 一開始，提供給 `ConfigureServices` 的 `IServiceCollection` 具有下列已定義的服務 (取決於[主機的設定方式](xref:fundamentals/host/index))：

| 服務類型 | 存留期 |
| ------------ | -------- |
| [Microsoft.AspNetCore.Hosting.Builder.IApplicationBuilderFactory](/dotnet/api/microsoft.aspnetcore.hosting.builder.iapplicationbuilderfactory) | 暫時性 |
| [Microsoft.AspNetCore.Hosting.IApplicationLifetime](/dotnet/api/microsoft.aspnetcore.hosting.iapplicationlifetime) | 單一 |
| [Microsoft.AspNetCore.Hosting.IHostingEnvironment](/dotnet/api/microsoft.aspnetcore.hosting.ihostingenvironment) | 單一 |
| [Microsoft.AspNetCore.Hosting.IStartup](/dotnet/api/microsoft.aspnetcore.hosting.istartup) | 單一 |
| [Microsoft.AspNetCore.Hosting.IStartupFilter](/dotnet/api/microsoft.aspnetcore.hosting.istartupfilter) | 暫時性 |
| [Microsoft.AspNetCore.Hosting.Server.IServer](/dotnet/api/microsoft.aspnetcore.hosting.server.iserver) | 單一 |
| [Microsoft.AspNetCore.Http.IHttpContextFactory](/dotnet/api/microsoft.aspnetcore.http.ihttpcontextfactory) | 暫時性 |
| [Microsoft.Extensions.Logging.ILogger&lt;T&gt;](/dotnet/api/microsoft.extensions.logging.ilogger) | 單一 |
| [Microsoft.Extensions.Logging.ILoggerFactory](/dotnet/api/microsoft.extensions.logging.iloggerfactory) | 單一 |
| [Microsoft.Extensions.ObjectPool.ObjectPoolProvider](/dotnet/api/microsoft.extensions.objectpool.objectpoolprovider) | 單一 |
| [Microsoft.Extensions.Options.IConfigureOptions&lt;T&gt;](/dotnet/api/microsoft.extensions.options.iconfigureoptions-1) | 暫時性 |
| [Microsoft.Extensions.Options.IOptions&lt;T&gt;](/dotnet/api/microsoft.extensions.options.ioptions-1) | 單一 |
| [System.Diagnostics.DiagnosticSource](https://docs.microsoft.com/dotnet/core/api/system.diagnostics.diagnosticsource) | 單一 |
| [System.Diagnostics.DiagnosticListener](https://docs.microsoft.com/dotnet/core/api/system.diagnostics.diagnosticlistener) | 單一 |

當可以使用服務集合擴充方法來註冊服務 (如果需要，也可以註冊其相依服務) 時，慣例是使用單一 `Add<ServiceName>` 擴充方法來註冊該服務要求的所有服務。 下列程式碼範例示範如何使用擴充方法 [AddDbContext](/dotnet/api/microsoft.extensions.dependencyinjection.entityframeworkservicecollectionextensions.adddbcontext)、[AddIdentity](/dotnet/api/microsoft.extensions.dependencyinjection.identityservicecollectionextensions.addidentity) 與 [AddMvc](/dotnet/api/microsoft.extensions.dependencyinjection.mvcservicecollectionextensions.addmvc) 將額外服務新增到容器中：

```csharp
public void ConfigureServices(IServiceCollection services)
{
    services.AddDbContext<ApplicationDbContext>(options =>
        options.UseSqlServer(Configuration.GetConnectionString("DefaultConnection")));

    services.AddIdentity<ApplicationUser, IdentityRole>()
        .AddEntityFrameworkStores<ApplicationDbContext>()
        .AddDefaultTokenProviders();

    services.AddMvc();
}
```

如需詳細資訊，請參閱 API 文件中的 [ServiceCollection Class](/dotnet/api/microsoft.extensions.dependencyinjection.servicecollection)。

## <a name="service-lifetimes"></a>執行個體存留期

為每個已註冊的服務選擇適當的存留期。 ASP.NET Core 服務可以使用下列存留期進行設定：

**暫時性**

每次要求暫時性存留期服務時都會建立它們。 此存留期最適合用於輕量型的無狀態服務。

**具範圍**

具範圍存留期服務會針對每個要求建立一次。

> [!WARNING]
> 在中介軟體中使用具範圍服務時，請將該服務插入 `Invoke` 或 `InvokeAsync` 方法中。 因為其會強制服務執行單一服務的行為，所以請勿透過建構函式插入進行插入。 如需詳細資訊，請參閱<xref:fundamentals/middleware/index>。

**單一**

當第一次收到有關單一資料庫存留期服務的要求時 (或是當執行 `ConfigureServices` 而且隨著服務註冊指定執行個體時)，即會建立單一資料庫存留期服務。 每個後續要求都會使用相同的執行個體。 若應用程式要求單一資料庫行為，建議您允許服務容器管理服務的存留期。 不要實作單一資料庫設計模式並為使用者提供可用來管理類別中物件存留期的程式碼。

> [!WARNING]
> 從單一資料庫解析具範圍服務是非常危險的。 處理後續要求時，它可能會導致服務有不正確的狀態。

### <a name="constructor-injection-behavior"></a>建構函式插入行為

服務可以透過兩個機制來解析：

* `IServiceProvider`
* [ActivatorUtilities](/dotnet/api/microsoft.extensions.dependencyinjection.activatorutilities) &ndash; 允許建立物件，而不需要在相依性插入容器中註冊服務。 搭配使用者面向抽象 (標籤協助程式、MVC 控制器、SignalR 中樞與模型繫結器) 使用 `ActivatorUtilities`。

建構函式可以接受不是由相依性插入提供的引數，但引數必須指派預設值。

當服務由 `IServiceProvider` 或 `ActivatorUtilities` 解析時，建構函式插入會要求 *public*建構函式。

當服務由 `ActivatorUtilities` 解析時，建構函式插入只要求只能有一個適用的建構函式存在。 支援建構函式多載，但只能有一個多載存在，其引數可以藉由相依性插入而完成。

## <a name="entity-framework-contexts"></a>Entity Framework 內容

Entity Framework 內容應該使用具範圍存留期新增至服務容器。 這是在註冊資料庫內容時透過對 [AddDbContext](/dotnet/api/microsoft.extensions.dependencyinjection.entityframeworkservicecollectionextensions.adddbcontext) 方法的呼叫來自動處理的。 使用資料庫內容的服務也應該使用具範圍存留期。

## <a name="lifetime-and-registration-options"></a>留期和註冊選項

為了示範這些存留期和註冊選項之間的差異，請考慮下列介面，以具有唯一識別碼 `OperationId` 的「作業」代表工作。 視如何針對下列介面設定作業服務存留期而定，當類別要求時，容器會提供相同或不同的服務執行個體：

::: moniker range=">= aspnetcore-2.1"

[!code-csharp[](dependency-injection/samples/2.x/DependencyInjectionSample/Interfaces/IOperation.cs?name=snippet1)]

::: moniker-end

::: moniker range="<= aspnetcore-2.0"

[!code-csharp[](dependency-injection/samples/1.x/DependencyInjectionSample/Interfaces/IOperation.cs?name=snippet1)]

::: moniker-end

介面是在 `Operation` 類別中實作。 若未提供 GUID，`Operation` 建構函式會產生 GUID：

::: moniker range=">= aspnetcore-2.1"

[!code-csharp[](dependency-injection/samples/2.x/DependencyInjectionSample/Models/Operation.cs?name=snippet1)]

::: moniker-end

::: moniker range="<= aspnetcore-2.0"

[!code-csharp[](dependency-injection/samples/1.x/DependencyInjectionSample/Models/Operation.cs?name=snippet1)]

::: moniker-end

會註冊相依於每種其他 `Operation` 類型的 `OperationService`。 當透過相依性插入要求 `OperationService` 時，它會根據相依服務的存留期擷取每個服務的新執行個體或現有執行個體。

* 若在收到要求時建立暫時性服務，`IOperationTransient` 服務的 `OperationsId` 會與 `OperationService` 的 `OperationsId` 不同。 `OperationService` 會收到 `IOperationTransient` 類別的新執行個體。 新執行個體會產生不同的 `OperationsId`。
* 若在收到要求時建立具範圍服務，`IOperationScoped` 服務的 `OperationsId` `OperationService` 的項目相同。 在不同的要求中，兩個服務會共用不同的 `OperationsId` 值。
* 若建立一資料庫與單一資料庫執行個體服務並在所有要求與所有服務中使用，`OperationsId` 在所有服務要求中會固定不變。

::: moniker range=">= aspnetcore-2.1"

[!code-csharp[](dependency-injection/samples/2.x/DependencyInjectionSample/Services/OperationService.cs?name=snippet1)]

::: moniker-end

::: moniker range="<= aspnetcore-2.0"

[!code-csharp[](dependency-injection/samples/1.x/DependencyInjectionSample/Services/OperationService.cs?name=snippet1)]

::: moniker-end

在 `Startup.ConfigureServices` 中，每個類型都會根據其具名存留期新增至容器：

::: moniker range=">= aspnetcore-2.1"

[!code-csharp[](dependency-injection/samples/2.x/DependencyInjectionSample/Startup.cs?name=snippet1&highlight=12-15,18)]

::: moniker-end

::: moniker range="<= aspnetcore-2.0"

[!code-csharp[](dependency-injection/samples/1.x/DependencyInjectionSample/Startup.cs?name=snippet1&highlight=6-9,12)]

::: moniker-end

`IOperationSingletonInstance` 服務使用具有 `Guid.Empty` 已知識別碼的特定執行個體。 很明顯此型別是使用中 (其 GUID 是所有區域)。

::: moniker range=">= aspnetcore-2.1"

範例應用程式示範個別要求內與個別要求之間的物件存留期。 範例應用程式的 `IndexModel` 會要求每種 `IOperation` 型別與 `OperationService`。 頁面接著會透過屬性指派來顯示所有頁面模型類別與服務的 `OperationId` 值：

[!code-csharp[](dependency-injection/samples/2.x/DependencyInjectionSample/Pages/Index.cshtml.cs?name=snippet1&highlight=7-11,14-18,21-25)]

::: moniker-end

::: moniker range="<= aspnetcore-2.0"

範例應用程式示範個別要求內與個別要求之間的物件存留期。 範例應用程式包括會要求每種 `IOperation` 類型與 `OperationService` 的 `OperationsController` 要求。 `Index` 動作會將服務設定為 `ViewBag` 以顯示服務的 `OperationId` 值：

[!code-csharp[](dependency-injection/samples/1.x/DependencyInjectionSample/Controllers/OperationsController.cs?name=snippet1)]

::: moniker-end

下面兩個輸出顯示兩個要求的結果：

**第一個要求：**

控制器作業：

暫時性： d233e165-f417-469b-a866-1cf1935d2518  
具範圍： 5d997e2d-55f5-4a64-8388-51c4e3a1ad19  
單一資料庫： 01271bc1-9e31-48e7-8f7c-7261b040ded9  
執行個體： 00000000-0000-0000-0000-000000000000

`OperationService` 作業：

暫時性： c6b049eb-1318-4e31-90f1-eb2dd849ff64  
具範圍： 5d997e2d-55f5-4a64-8388-51c4e3a1ad19  
單一資料庫： 01271bc1-9e31-48e7-8f7c-7261b040ded9  
執行個體： 00000000-0000-0000-0000-000000000000

**:第二個要求：**

控制器作業：

暫時性： b63bd538-0a37-4ff1-90ba-081c5138dda0  
具範圍： 31e820c5-4834-4d22-83fc-a60118acb9f4  
單一資料庫： 01271bc1-9e31-48e7-8f7c-7261b040ded9  
執行個體： 00000000-0000-0000-0000-000000000000

`OperationService` 作業：

暫時性： c4cbacb8-36a2-436d-81c8-8c1b78808aaf  
具範圍： 31e820c5-4834-4d22-83fc-a60118acb9f4  
單一資料庫： 01271bc1-9e31-48e7-8f7c-7261b040ded9  
執行個體： 00000000-0000-0000-0000-000000000000

觀察哪些 `OperationId` 值在要求內以及要求之間不同：

* 「暫時性」 物件一律不同。 請注意，第一個與第二個要求的暫時性 `OperationId` 值在兩個 `OperationService` 作業之間與各要求之間都不同。 新執行個體會提供給每個服務與要求。
* 「具範圍」物件在要求內相同，但在不同的要求之間會不同。
* 「單一資料庫」物件對於每個物件與每個要求都相同 (不論 `Operation` 執行個體是否提供於 `ConfigureServices`)。

## <a name="call-services-from-main"></a>從主要呼叫服務

使用 [IServiceScopeFactory.CreateScope](/dotnet/api/microsoft.extensions.dependencyinjection.iservicescopefactory.createscope) 建立 [IServiceScope](/dotnet/api/microsoft.extensions.dependencyinjection.iservicescope)，以解析應用程式範圍中的具範圍服務。 此法可用於在開機時存取具範圍服務，以執行初始化工作。 下列範例示範如何在 `Program.Main` 中取得 `MyScopedService`：

```csharp
public static void Main(string[] args)
{
    var host = CreateWebHostBuilder(args).Build();

    using (var serviceScope = host.Services.CreateScope())
    {
        var services = serviceScope.ServiceProvider;

        try
        {
            var serviceContext = services.GetRequiredService<MyScopedService>();
            // Use the context here
        }
        catch (Exception ex)
        {
            var logger = services.GetRequiredService<ILogger<Program>>();
            logger.LogError(ex, "An error occurred.");
        }
    }

    host.Run();
}
```

## <a name="scope-validation"></a>範圍驗證

::: moniker range=">= aspnetcore-2.0"

當應用程式在開發環境中執行時，預設服務提供者會執行檢查以確認：

* 具範圍服務不是直接或間接由根服務提供者解析。
* 具範圍服務不是直接或間接插入至單一服務。

::: moniker-end

根服務提供者會在呼叫 [BuildServiceProvider](/dotnet/api/microsoft.extensions.dependencyinjection.servicecollectioncontainerbuilderextensions.buildserviceprovider) 時建立。 當提供者啟動應用程式時，根服務提供者的存留期與應用程式/伺服器的存留期一致，並會在應用程式關閉時處置。

具範圍服務會由建立這些服務的容器處置。 若是在根容器中建立具範圍服務，因為當應用程式/伺服器關機時，服務只會由根容器處理，所以服務的存留期會提升為單一服務等級。 當呼叫 `BuildServiceProvider` 時，驗證服務範圍會攔截到這些情況。

如需詳細資訊，請參閱<xref:fundamentals/host/web-host#scope-validation>。

## <a name="request-services"></a>要求服務

來自 `HttpContext`，在 ASP.NET Core 要求內提供的服務是透過 [HttpContext.RequestServices](/dotnet/api/microsoft.aspnetcore.http.httpcontext.requestservices) 集合公開。

要求服務代表您在應用程式中設定和要求的服務。 當物件指定相依性時，這些會由在 `RequestServices` 中找到的類型來滿足，而非 `ApplicationServices`。

一般而言，應用程式不應該直接使用這些屬性。 相反地，透過類別建構函式要求類別所需的型別，以及允許架構插入相依性。 如此產生的類別將更較容易測試 (請參閱[測試與偵錯](xref:test/index)主題)。

> [!NOTE]
> 偏好要求相依性作為建構函式參數，而不要存取 `RequestServices` 集合。

## <a name="design-services-for-dependency-injection"></a>針對相依性插入設計服務

最佳做法是：

* 設計服務以使用相依性插入來取得其相依性。
* 避免具狀態的靜態方法呼叫 (一個稱為[靜電依附](https://deviq.com/static-cling/)的實踐)。
* 避免直接在服務內具現化相依類別。 直接具現化會將程式碼耦合到特定實作。

藉由遵循[物件導向設計的 SOLID 準則](https://deviq.com/solid/)，應用程式類別自然而然會傾向小型、構造良好且可輕鬆地測試。

若類別有太多插入的相依性，這通常表示類別有太多責任而且正違反[單一責任原則 (SRP)](https://deviq.com/single-responsibility-principle/) \(英文\)。 將類別負責的某些部分移到新的類別，以嘗試重構類別。 請記住，Razor Pages 頁面模型類別與 MVC 控制器類別應該專注於 UI 考量。 商務規則和資料存取實作詳細資料應該保存在適合這些[分開考量](https://deviq.com/separation-of-concerns/) (Separation of Concerns) 類別中。

### <a name="disposal-of-services"></a>處置服務

容器會為它建立的 `IDisposable` 類型呼叫 `Dispose`。 若執行個體由使用者程式碼新增到容器中，它將不會自動處置。

```csharp
// Services that implement IDisposable:
public class Service1 : IDisposable {}
public class Service2 : IDisposable {}
public class Service3 : IDisposable {}

public interface ISomeService {}
public class SomeServiceImplementation : ISomeService, IDisposable {}

public void ConfigureServices(IServiceCollection services)
{
    // The container creates the following instances and disposes them automatically:
    services.AddScoped<Service1>();
    services.AddSingleton<Service2>();
    services.AddSingleton<ISomeService>(sp => new SomeServiceImplementation());

    // The container doesn't create the following instances, so it doesn't dispose of
    // the instances automatically:
    services.AddSingleton<Service3>(new Service3());
    services.AddSingleton(new Service3());
}
```

::: moniker range="= aspnetcore-1.0"

> [!NOTE]
> 在 ASP.NET Core 1.0 中，容器會對「所有」`IDisposable` 物件呼叫 dispose，包括它未建立的物件。

::: moniker-end

## <a name="default-service-container-replacement"></a>預設服務容器取代

內建的服務容器是要服務架構和建置在其上的大部分取用者應用程式的基本需求。 不過，開發人員可以使用其偏好的容器取代內建的容器。 `Startup.ConfigureServices` 方法通常會傳回 `void`。 如果方法的簽章變更為傳回 [IServiceProvider](/dotnet/api/system.iserviceprovider)，則可以設定並傳回不同的容器。 .NET 有許多 IoC 容器可用。 在下列範例中，我們使用了 [Autofac](https://autofac.org/) 容器：

1. 安裝適當的容器套件：

    * [Autofac](https://www.nuget.org/packages/Autofac/)
    * [Autofac.Extensions.DependencyInjection](https://www.nuget.org/packages/Autofac.Extensions.DependencyInjection/)

2. 在 `Startup.ConfigureServices` 中設定容器並傳回 `IServiceProvider`：

    ```csharp
    public IServiceProvider ConfigureServices(IServiceCollection services)
    {
        services.AddMvc();
        // Add other framework services

        // Add Autofac
        var containerBuilder = new ContainerBuilder();
        containerBuilder.RegisterModule<DefaultModule>();
        containerBuilder.Populate(services);
        var container = containerBuilder.Build();
        return new AutofacServiceProvider(container);
    }
    ```

    若要使用第三方容器，`Startup.ConfigureServices` 必須傳回 `IServiceProvider`。

3. 在 `DefaultModule` 中設定 Autofac：

    ```csharp
    public class DefaultModule : Module
    {
        protected override void Load(ContainerBuilder builder)
        {
            builder.RegisterType<CharacterRepository>().As<ICharacterRepository>();
        }
    }
    ```

在執行階段，Autofac 會用來解析類型及插入相依性。 若要深入了解如何搭配 ASP.NET Core 使用 Autofac，請參閱 [Autofac 文件 ](https://docs.autofac.org/en/latest/integration/aspnetcore.html) \(英文\)。

### <a name="thread-safety"></a>執行緒安全

單一服務需要具備執行緒安全。 如果單一服務相依於暫時性服務，暫時性服務可能也需要具備執行緒安全，視它如何由單一項目使用。

單一服務的 Factory 方法 (例如 [AddSingleton&lt;TService&gt;(IServiceCollection, Func&lt;IServiceProvider,TService&gt;)](/dotnet/api/microsoft.extensions.dependencyinjection.servicecollectionserviceextensions.addsingleton#Microsoft_Extensions_DependencyInjection_ServiceCollectionServiceExtensions_AddSingleton__1_Microsoft_Extensions_DependencyInjection_IServiceCollection_System_Func_System_IServiceProvider___0__) 的第二個引數) 不需要是安全執行緒。 就像型別 (`static`) 建構函式一樣，它一定會被單一執行緒呼叫一次。

## <a name="recommendations"></a>建議

使用相依性插入時，請記住下列建議：

* 避免直接在服務容器中儲存資料與設定。 例如，使用者的購物車通常不應該新增至服務容器。 組態應該使用[選項模式](xref:fundamentals/configuration/options)。 同樣地，請避免只存在以允許存取某個其他物件的「資料持有者」物件。 最好是盡可能透過相依性插入來要求所需的實際項目。

* 避免以靜態方式存取服務 (例如，以靜態方式設定 [IApplicationBuilder.ApplicationServices](/dotnet/api/microsoft.aspnetcore.builder.iapplicationbuilder.applicationservices) 型別以四處使用)。

* 避免使用服務定位器模式 (例如 [IServiceProvider.GetService](/dotnet/api/system.iserviceprovider.getservice))。

* 避免以靜態方式存取 `HttpContext` (例如 [IHttpContextAccessor.HttpContext](/dotnet/api/microsoft.aspnetcore.http.ihttpcontextaccessor.httpcontext))。

就像所有的建議集，您可能會遇到需要忽略建議的情況。 例外狀況很少見&mdash;大部分是架構本身內的特殊案例。

相依性插入是靜態/全域物件存取模式的「替代」選項。 如果您將相依性插入與靜態物件存取混合，則可能無法實現相依性插入的優點。

## <a name="additional-resources"></a>其他資源

* <xref:mvc/views/dependency-injection>
* <xref:mvc/controllers/dependency-injection>
* <xref:security/authorization/dependencyinjection>
* <xref:fundamentals/repository-pattern>
* <xref:fundamentals/startup>
* <xref:test/index>
* <xref:fundamentals/middleware/extensibility>
* [在 ASP.NET Core 使用 Dependency Injection 撰寫簡潔的程式碼 (MSDN)](https://msdn.microsoft.com/magazine/mt703433.aspx)
* [Container-Managed Application Design, Prelude: Where does the Container Belong?](https://blogs.msdn.microsoft.com/nblumhardt/2008/12/26/container-managed-application-design-prelude-where-does-the-container-belong/) (容器管理的應用程式設計，序曲：容器屬於何處？)
* [明確相依性準則](https://deviq.com/explicit-dependencies-principle/)
* [逆轉控制容器和相依性插入模式 (Martin Fowler)](https://www.martinfowler.com/articles/injection.html) \(英文\)
* [New is Glue (「黏附」程式碼到特定實作)](https://ardalis.com/new-is-glue) \(英文\)
