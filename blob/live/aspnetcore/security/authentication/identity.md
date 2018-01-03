---
title: "在 ASP.NET Core 上的識別簡介"
author: rick-anderson
description: "使用身分識別與 ASP.NET Core 應用程式"
keywords: "ASP.NET Core，身分識別授權安全性"
ms.author: riande
manager: wpickett
ms.date: 12/15/2017
ms.topic: article
ms.assetid: cf119f21-1a2b-49a2-b052-547ccb66ee83
ms.technology: aspnet
ms.prod: asp.net-core
uid: security/authentication/identity
ms.openlocfilehash: 7daf0267a6dc659afbd188ce87e35ca40816a31d
ms.sourcegitcommit: 198fb0488e961048bfa376cf58cb853ef1d1cb91
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2017
---
# <a name="introduction-to-identity-on-aspnet-core"></a><span data-ttu-id="a9cd8-104">在 ASP.NET Core 上的識別簡介</span><span class="sxs-lookup"><span data-stu-id="a9cd8-104">Introduction to Identity on ASP.NET Core</span></span>

<span data-ttu-id="a9cd8-105">由[Pranav Rastogi](https://github.com/rustd)， [Rick Anderson](https://twitter.com/RickAndMSFT)， [Tom Dykstra](https://github.com/tdykstra)，Jon Galloway [Erik Reitan](https://github.com/Erikre)，和[Steve Smith](https://ardalis.com/)</span><span class="sxs-lookup"><span data-stu-id="a9cd8-105">By [Pranav Rastogi](https://github.com/rustd), [Rick Anderson](https://twitter.com/RickAndMSFT), [Tom Dykstra](https://github.com/tdykstra), Jon Galloway, [Erik Reitan](https://github.com/Erikre), and [Steve Smith](https://ardalis.com/)</span></span>

<span data-ttu-id="a9cd8-106">ASP.NET Core 身分識別是可讓您登入功能加入您的應用程式的成員資格系統。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-106">ASP.NET Core Identity is a membership system which allows you to add login functionality to your application.</span></span> <span data-ttu-id="a9cd8-107">使用者可以建立帳戶和登入的使用者名稱和密碼，或者也可以使用例如 Facebook、 Google、 Microsoft 帳戶、 Twitter 或其他外部登入提供者。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-107">Users can create an account and login with a user name and password or they can use an external login provider such as Facebook, Google, Microsoft Account, Twitter or others.</span></span>

<span data-ttu-id="a9cd8-108">您可以設定要用來儲存使用者名稱、 密碼及分析資料的 SQL Server 資料庫的 ASP.NET 核心身分識別。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-108">You can configure ASP.NET Core Identity to use a SQL Server database to store user names, passwords, and profile data.</span></span> <span data-ttu-id="a9cd8-109">或者，您可以使用您自己的持續性存放區，例如 Azure 資料表儲存體。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-109">Alternatively, you can use your own persistent store, for example, an Azure Table Storage.</span></span> <span data-ttu-id="a9cd8-110">本文件包含適用於 Visual Studio 以及使用 CLI 的指示。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-110">This document contains instructions for Visual Studio and for using the CLI.</span></span>

## <a name="overview-of-identity"></a><span data-ttu-id="a9cd8-111">身分識別的概觀</span><span class="sxs-lookup"><span data-stu-id="a9cd8-111">Overview of Identity</span></span>

<span data-ttu-id="a9cd8-112">本主題中，您將了解如何使用 ASP.NET Core 身分加入的功能，以註冊、 登入，並登出使用者。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-112">In this topic, you'll learn how to use ASP.NET Core Identity to add functionality to register, log in, and log out a user.</span></span> <span data-ttu-id="a9cd8-113">如需使用 ASP.NET Core 識別建立應用程式的詳細指示，請參閱本文結尾處的後續步驟 > 一節。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-113">For more detailed instructions about creating apps using ASP.NET Core Identity, see the Next Steps section at the end of this article.</span></span>

1.  <span data-ttu-id="a9cd8-114">建立 ASP.NET Core Web 應用程式專案與個別使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-114">Create an ASP.NET Core Web Application project with Individual User Accounts.</span></span>

    # <a name="visual-studiotabvisual-studio"></a>[<span data-ttu-id="a9cd8-115">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a9cd8-115">Visual Studio</span></span>](#tab/visual-studio)
    <span data-ttu-id="a9cd8-116">在 Visual Studio 中，選取**檔案** -> **新增** -> **專案**。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-116">In Visual Studio, select **File** -> **New** -> **Project**.</span></span> <span data-ttu-id="a9cd8-117">選取**ASP.NET Web 應用程式**從**新專案** 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-117">Select the **ASP.NET Web Application** from the **New Project** dialog box.</span></span> <span data-ttu-id="a9cd8-118">選取 ASP.NET Core **Web Application(Model-View-Controller)**適用於 ASP.NET Core 與 2.x**個別使用者帳戶**做為驗證方法。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-118">Selecting an ASP.NET Core **Web Application(Model-View-Controller)** for ASP.NET Core 2.x with **Individual User Accounts** as the authentication method.</span></span>

    <span data-ttu-id="a9cd8-119">注意： 您必須選取**個別使用者帳戶**。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-119">Note: You must select **Individual User Accounts**.</span></span>
 
    ![[新增專案] 對話](identity/_static/01-mvc_2.png)
    
    # <a name="net-core-clitabnetcore-cli"></a>[<span data-ttu-id="a9cd8-121">.NET Core CLI</span><span class="sxs-lookup"><span data-stu-id="a9cd8-121">.NET Core CLI</span></span>](#tab/netcore-cli)
    <span data-ttu-id="a9cd8-122">如果使用.NET 核心 CLI，請建立新的專案使用``dotnet new mvc --auth Individual``。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-122">If using the .NET Core CLI, create the new project using ``dotnet new mvc --auth Individual``.</span></span> <span data-ttu-id="a9cd8-123">此命令會建立新的專案與 Visual Studio 建立的相同身分識別範本程式碼。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-123">This command creates a new project with the same Identity template code Visual Studio creates.</span></span>
 
    <span data-ttu-id="a9cd8-124">建立的專案包含`Microsoft.AspNetCore.Identity.EntityFrameworkCore`封裝，它會保存身分資料和 SQL Server 使用的結構描述[Entity Framework Core](https://docs.microsoft.com/ef/)。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-124">The created project contains the `Microsoft.AspNetCore.Identity.EntityFrameworkCore` package, which persists the Identity data and schema to SQL Server using [Entity Framework Core](https://docs.microsoft.com/ef/).</span></span>
    
    ---
 
2.  <span data-ttu-id="a9cd8-125">設定身分識別服務，並將新增中的介軟體中`Startup`。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-125">Configure Identity services and add middleware in `Startup`.</span></span>

    <span data-ttu-id="a9cd8-126">識別服務會加入至應用程式中`ConfigureServices`方法中的`Startup`類別：</span><span class="sxs-lookup"><span data-stu-id="a9cd8-126">The Identity services are added to the application in the `ConfigureServices` method in the `Startup` class:</span></span>

    # <a name="aspnet-core-2xtabaspnetcore2x"></a>[<span data-ttu-id="a9cd8-127">ASP.NET Core 2.x</span><span class="sxs-lookup"><span data-stu-id="a9cd8-127">ASP.NET Core 2.x</span></span>](#tab/aspnetcore2x)
    
    [!code-csharp[Main](identity/sample/src/ASPNETv2-IdentityDemo/Startup.cs?name=snippet_configureservices&highlight=7-9,11-28,30-39)]
    
    <span data-ttu-id="a9cd8-128">這些服務會提供給應用程式透過[相依性插入](xref:fundamentals/dependency-injection)。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-128">These services are made available to the application through [dependency injection](xref:fundamentals/dependency-injection).</span></span>
    
    <span data-ttu-id="a9cd8-129">識別已啟用應用程式藉由呼叫`UseAuthentication`中`Configure`方法。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-129">Identity is enabled for the application by calling `UseAuthentication` in the `Configure` method.</span></span> <span data-ttu-id="a9cd8-130">`UseAuthentication`加入驗證[中介軟體](xref:fundamentals/middleware)要求管線。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-130">`UseAuthentication` adds authentication [middleware](xref:fundamentals/middleware) to the request pipeline.</span></span>
    
    [!code-csharp[Main](identity/sample/src/ASPNETv2-IdentityDemo/Startup.cs?name=snippet_configure&highlight=17)]
    
    # <a name="aspnet-core-1xtabaspnetcore1x"></a>[<span data-ttu-id="a9cd8-131">ASP.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="a9cd8-131">ASP.NET Core 1.x</span></span>](#tab/aspnetcore1x)
    
    [!code-csharp[Main](identity/sample/src/ASPNET-IdentityDemo/Startup.cs?name=snippet_configureservices&highlight=7-9,13-34)]
    
    <span data-ttu-id="a9cd8-132">這些服務會提供給應用程式透過[相依性插入](xref:fundamentals/dependency-injection)。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-132">These services are made available to the application through [dependency injection](xref:fundamentals/dependency-injection).</span></span>
    
    <span data-ttu-id="a9cd8-133">識別已啟用應用程式藉由呼叫`UseIdentity`中`Configure`方法。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-133">Identity is enabled for the application by calling `UseIdentity` in the `Configure` method.</span></span> <span data-ttu-id="a9cd8-134">`UseIdentity`新增 cookie 基本驗證[中介軟體](xref:fundamentals/middleware)要求管線。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-134">`UseIdentity` adds cookie-based authentication [middleware](xref:fundamentals/middleware) to the request pipeline.</span></span>
        
    [!code-csharp[Main](identity/sample/src/ASPNET-IdentityDemo/Startup.cs?name=snippet_configure&highlight=21)]
    
    ---
     
    <span data-ttu-id="a9cd8-135">如需處理程序的應用程式啟動的詳細資訊，請參閱[應用程式啟動](xref:fundamentals/startup)。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-135">For more information about the application start up process, see [Application Startup](xref:fundamentals/startup).</span></span>

3.  <span data-ttu-id="a9cd8-136">建立使用者。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-136">Create a user.</span></span>

    <span data-ttu-id="a9cd8-137">啟動應用程式，然後按一下**註冊**連結。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-137">Launch the application and then click on the **Register** link.</span></span>

    <span data-ttu-id="a9cd8-138">如果這是您要執行此動作的第一次，您可能需要執行移轉。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-138">If this is the first time you're performing this action, you may be required to run migrations.</span></span> <span data-ttu-id="a9cd8-139">應用程式會提示您**套用移轉**:</span><span class="sxs-lookup"><span data-stu-id="a9cd8-139">The application prompts you to **Apply Migrations**:</span></span>
    
    ![適用於移轉 Web 網頁](identity/_static/apply-migrations.png)
    
    <span data-ttu-id="a9cd8-141">或者，您可以測試沒有持續性資料庫的應用程式使用 ASP.NET Core 身分識別，使用記憶體中資料庫。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-141">Alternately, you can test using ASP.NET Core Identity with your app without a persistent database by using an in-memory database.</span></span> <span data-ttu-id="a9cd8-142">若要使用記憶體中資料庫時，將``Microsoft.EntityFrameworkCore.InMemory``封裝到您的應用程式，並修改您的應用程式呼叫``AddDbContext``中``ConfigureServices``，如下所示：</span><span class="sxs-lookup"><span data-stu-id="a9cd8-142">To use an in-memory database, add the ``Microsoft.EntityFrameworkCore.InMemory`` package to your app and modify your app's call to ``AddDbContext`` in ``ConfigureServices`` as follows:</span></span>

    ```csharp
    services.AddDbContext<ApplicationDbContext>(options =>
        options.UseInMemoryDatabase(Guid.NewGuid().ToString()));
    ```
    
    <span data-ttu-id="a9cd8-143">當使用者按一下**註冊**連結，``Register``上叫用動作``AccountController``。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-143">When the user clicks the **Register** link, the ``Register`` action is invoked on ``AccountController``.</span></span> <span data-ttu-id="a9cd8-144">``Register``動作會建立使用者藉由呼叫`CreateAsync`上`_userManager`物件 (提供給``AccountController``的相依性插入):</span><span class="sxs-lookup"><span data-stu-id="a9cd8-144">The ``Register`` action creates the user by calling `CreateAsync` on the  `_userManager` object (provided to ``AccountController`` by dependency injection):</span></span>
 
    [!code-csharp[Main](identity/sample/src/ASPNET-IdentityDemo/Controllers/AccountController.cs?name=snippet_register&highlight=11)]

    <span data-ttu-id="a9cd8-145">如果已成功建立使用者，使用者會登入的呼叫所``_signInManager.SignInAsync``。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-145">If the user was created successfully, the user is logged in by the call to ``_signInManager.SignInAsync``.</span></span>

    <span data-ttu-id="a9cd8-146">**注意：**看到[帳戶確認](xref:security/authentication/accconfirm#prevent-login-at-registration)的步驟，以避免立即註冊登入。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-146">**Note:** See [account confirmation](xref:security/authentication/accconfirm#prevent-login-at-registration) for steps to prevent immediate login at registration.</span></span>
 
4.  <span data-ttu-id="a9cd8-147">登入。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-147">Log in.</span></span>
 
    <span data-ttu-id="a9cd8-148">使用者可以登入，依序按一下**登入**頂端的站台連結或它們可能瀏覽至登入頁面當他們嘗試存取需要的授權站台的一部分。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-148">Users can sign in by clicking the **Log in** link at the top of the site, or they may be navigated to the Login page if they attempt to access a part of the site that requires authorization.</span></span> <span data-ttu-id="a9cd8-149">當使用者提交表單的登入頁面上， ``AccountController`` ``Login``動作呼叫。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-149">When the user submits the form on the Login page, the ``AccountController`` ``Login`` action is called.</span></span>

    [!code-csharp[Main](identity/sample/src/ASPNET-IdentityDemo/Controllers/AccountController.cs?name=snippet_login&highlight=13-14)]
 
    <span data-ttu-id="a9cd8-150">``Login``動作呼叫``PasswordSignInAsync``上``_signInManager``物件 (提供給``AccountController``的相依性插入)。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-150">The ``Login`` action calls ``PasswordSignInAsync`` on the ``_signInManager`` object (provided to ``AccountController`` by dependency injection).</span></span>
 
    <span data-ttu-id="a9cd8-151">基底``Controller``類別會公開``User``從控制器方法可以存取的屬性。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-151">The base ``Controller`` class exposes a ``User`` property that you can access from controller methods.</span></span> <span data-ttu-id="a9cd8-152">比方說，您可以列舉`User.Claims`和進行授權決策。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-152">For instance, you can enumerate `User.Claims` and make authorization decisions.</span></span> <span data-ttu-id="a9cd8-153">如需詳細資訊，請參閱[授權](xref:security/authorization/index)。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-153">For more information, see [Authorization](xref:security/authorization/index).</span></span>
 
5.  <span data-ttu-id="a9cd8-154">登出。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-154">Log out.</span></span>
 
    <span data-ttu-id="a9cd8-155">按一下**登出**連結呼叫`LogOut`動作。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-155">Clicking the **Log out** link calls the `LogOut` action.</span></span>
 
    [!code-csharp[Main](identity/sample/src/ASPNET-IdentityDemo/Controllers/AccountController.cs?name=snippet_logout&highlight=7)]
 
    <span data-ttu-id="a9cd8-156">上述程式碼中的呼叫上述`_signInManager.SignOutAsync`方法。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-156">The preceding code above calls the `_signInManager.SignOutAsync` method.</span></span> <span data-ttu-id="a9cd8-157">`SignOutAsync`方法會清除儲存在 cookie 中的使用者的宣告。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-157">The `SignOutAsync` method clears the user's claims stored in a cookie.</span></span>
 
6.  <span data-ttu-id="a9cd8-158">組態設定。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-158">Configuration.</span></span>

    <span data-ttu-id="a9cd8-159">識別有一些您可以在您的應用程式啟動類別中覆寫的預設行為。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-159">Identity has some default behaviors that you can override in your application's startup class.</span></span> <span data-ttu-id="a9cd8-160">您不需要設定``IdentityOptions``如果您使用的預設行為。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-160">You do not need to configure ``IdentityOptions`` if you are using the default behaviors.</span></span>

    # <a name="aspnet-core-2xtabaspnetcore2x"></a>[<span data-ttu-id="a9cd8-161">ASP.NET Core 2.x</span><span class="sxs-lookup"><span data-stu-id="a9cd8-161">ASP.NET Core 2.x</span></span>](#tab/aspnetcore2x)
    
    [!code-csharp[Main](identity/sample/src/ASPNETv2-IdentityDemo/Startup.cs?name=snippet_configureservices&highlight=7-9,11-28,30-39)]
    
    # <a name="aspnet-core-1xtabaspnetcore1x"></a>[<span data-ttu-id="a9cd8-162">ASP.NET Core 1.x</span><span class="sxs-lookup"><span data-stu-id="a9cd8-162">ASP.NET Core 1.x</span></span>](#tab/aspnetcore1x)
    
    [!code-csharp[Main](identity/sample/src/ASPNET-IdentityDemo/Startup.cs?name=snippet_configureservices&highlight=13-34)]

    ---
    
    <span data-ttu-id="a9cd8-163">如需如何設定身分識別的詳細資訊，請參閱[設定身分識別](xref:security/authentication/identity-configuration)。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-163">For more information about how to configure Identity, see [Configure Identity](xref:security/authentication/identity-configuration).</span></span>
    
    <span data-ttu-id="a9cd8-164">您也可以設定資料類型的主索引鍵，請參閱[設定識別主索引鍵資料類型](xref:security/authentication/identity-primary-key-configuration)。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-164">You also can configure the data type of the primary key, see [Configure Identity primary keys data type](xref:security/authentication/identity-primary-key-configuration).</span></span>
 
7.  <span data-ttu-id="a9cd8-165">檢視的資料庫。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-165">View the database.</span></span>

    <span data-ttu-id="a9cd8-166">如果您的應用程式使用 SQL Server 資料庫 （預設值在 Windows 上，以及適用於 Visual Studio 使用者），您可以檢視資料庫建立的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-166">If your app is using a SQL Server database (the default on Windows and for Visual Studio users), you can view the database the app created.</span></span> <span data-ttu-id="a9cd8-167">您可以使用**SQL Server Management Studio**。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-167">You can use **SQL Server Management Studio**.</span></span> <span data-ttu-id="a9cd8-168">或者，從 Visual Studio 中，選取**檢視** -> **SQL Server 物件總管**。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-168">Alternatively, from Visual Studio, select **View** -> **SQL Server Object Explorer**.</span></span> <span data-ttu-id="a9cd8-169">連接到**(localdb) \MSSQLLocalDB**。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-169">Connect to **(localdb)\MSSQLLocalDB**.</span></span> <span data-ttu-id="a9cd8-170">資料庫名稱符合 **aspnet-<*的專案名稱*>-<*日期字串*> * * 隨即出現。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-170">The database with a name matching **aspnet-<*name of your project*>-<*date string*>** is displayed.</span></span>

    ![AspNetUsers 資料庫資料表上的內容功能表](identity/_static/04-db.png)
    
    <span data-ttu-id="a9cd8-172">展開的資料庫及其**資料表**，然後以滑鼠右鍵按一下**dbo。AspNetUsers**資料表，然後選取**檢視資料**。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-172">Expand the database and its **Tables**, then right-click the **dbo.AspNetUsers** table and select **View Data**.</span></span>

## <a name="identity-components"></a><span data-ttu-id="a9cd8-173">身分識別的元件</span><span class="sxs-lookup"><span data-stu-id="a9cd8-173">Identity Components</span></span>

<span data-ttu-id="a9cd8-174">識別系統的主要參考組件是`Microsoft.AspNetCore.Identity`。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-174">The primary reference assembly for the Identity system is `Microsoft.AspNetCore.Identity`.</span></span> <span data-ttu-id="a9cd8-175">此套件包含一組核心介面 ASP.NET Core 身分識別，而且會包含`Microsoft.AspNetCore.Identity.EntityFrameworkCore`。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-175">This package contains the core set of interfaces for ASP.NET Core Identity, and is included by `Microsoft.AspNetCore.Identity.EntityFrameworkCore`.</span></span>

<span data-ttu-id="a9cd8-176">可用於 ASP.NET Core 應用程式的身分識別系統，會需要這些相依性：</span><span class="sxs-lookup"><span data-stu-id="a9cd8-176">These dependencies are needed to use the Identity system in ASP.NET Core applications:</span></span>

* <span data-ttu-id="a9cd8-177">`Microsoft.AspNetCore.Identity.EntityFrameworkCore`-包含必要的型別，以搭配 Entity Framework Core 的身分識別。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-177">`Microsoft.AspNetCore.Identity.EntityFrameworkCore` - Contains the required types to use Identity with Entity Framework Core.</span></span>

* <span data-ttu-id="a9cd8-178">`Microsoft.EntityFrameworkCore.SqlServer`實體架構的核心是 Microsoft 的建議的資料存取技術，例如 SQL Server 關聯式資料庫。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-178">`Microsoft.EntityFrameworkCore.SqlServer` - Entity Framework Core is Microsoft's recommended data access technology for relational databases like SQL Server.</span></span> <span data-ttu-id="a9cd8-179">為了測試，您可以使用`Microsoft.EntityFrameworkCore.InMemory`。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-179">For testing, you can use `Microsoft.EntityFrameworkCore.InMemory`.</span></span>

* <span data-ttu-id="a9cd8-180">`Microsoft.AspNetCore.Authentication.Cookies`中介軟體，可讓應用程式使用 cookie 型驗證。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-180">`Microsoft.AspNetCore.Authentication.Cookies` - Middleware that enables an app to use cookie-based authentication.</span></span>

## <a name="migrating-to-aspnet-core-identity"></a><span data-ttu-id="a9cd8-181">移轉至 ASP.NET Core 身分識別</span><span class="sxs-lookup"><span data-stu-id="a9cd8-181">Migrating to ASP.NET Core Identity</span></span>

<span data-ttu-id="a9cd8-182">針對其他資訊和指引移轉您現有的身分識別存放區，請參閱[移轉的驗證和身分識別](xref:migration/identity)。</span><span class="sxs-lookup"><span data-stu-id="a9cd8-182">For additional information and guidance on migrating your existing Identity store see [Migrating Authentication and Identity](xref:migration/identity).</span></span>

## <a name="next-steps"></a><span data-ttu-id="a9cd8-183">後續步驟</span><span class="sxs-lookup"><span data-stu-id="a9cd8-183">Next Steps</span></span>

* [<span data-ttu-id="a9cd8-184">移轉驗證和身分識別</span><span class="sxs-lookup"><span data-stu-id="a9cd8-184">Migrating Authentication and Identity</span></span>](xref:migration/identity)
* [<span data-ttu-id="a9cd8-185">帳戶確認和密碼復原</span><span class="sxs-lookup"><span data-stu-id="a9cd8-185">Account Confirmation and Password Recovery</span></span>](xref:security/authentication/accconfirm)
* [<span data-ttu-id="a9cd8-186">使用 SMS 的雙因素驗證</span><span class="sxs-lookup"><span data-stu-id="a9cd8-186">Two-factor authentication with SMS</span></span>](xref:security/authentication/2fa)
* [<span data-ttu-id="a9cd8-187">使用 Facebook、Google 和其他外部提供者啟用驗證</span><span class="sxs-lookup"><span data-stu-id="a9cd8-187">Enabling authentication using Facebook, Google and other external providers</span></span>](xref:security/authentication/social/index)