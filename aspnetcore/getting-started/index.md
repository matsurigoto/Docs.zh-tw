---
title: ASP.NET Core 使用者入門
author: rick-anderson
description: 使用 ASP.NET Core 建立並執行簡單 Hello World 應用程式的快速教學課程。
ms.author: riande
ms.custom: mvc
ms.date: 05/31/2018
uid: getting-started
ms.openlocfilehash: 7ab9f303d74786c4ac76f002d0f2c66371e78cb8
ms.sourcegitcommit: b4c7b1a4c48dec0865f27874275c73da1f75e918
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/24/2018
ms.locfileid: "39228578"
---
# <a name="get-started-with-aspnet-core"></a>ASP.NET Core 使用者入門

::: moniker range=">= aspnetcore-2.1"

1. 安裝 [!INCLUDE [](~/includes/2.1-SDK.md)]。

2. 建立 ASP.NET Core 專案。 開啟命令殼層，並輸入下列命令：

    ```console
    dotnet new webapp -o aspnetcoreapp
    ```

    [!INCLUDE [](~/includes/webapp-alias-notice.md)]

3. 信任 HTTPS 開發憑證：

# <a name="windowstabwindows"></a>[Windows](#tab/windows)

    ```console
    dotnet dev-certs https --trust
    ```

   上述命令會顯示以下對話方塊：

   ![安全性警告對話方塊](_static/cert.png)

   若您同意信任開發憑證，請選取 [是]。

# <a name="macostabmacos"></a>[macOS](#tab/macos)

    ```console
    dotnet dev-certs https --trust
    ```

   上述命令會顯示以下訊息：

   已要求信任 HTTPS 開發憑證。若憑證尚未受到信任，我們會執行以下命令：`'sudo security add-trusted-cert -d -r trustRoot -k /Library/Keychains/System.keychain <<certificate>>'`。此命令可能會提示您提供密碼，以在系統金鑰鏈上安裝憑證。  密碼：

   若您同意信任開發憑證，請輸入您的密碼。

# <a name="linuxtablinux"></a>[Linux](#tab/linux)

   <a name="see-the-documentation-for-your-linux-distribution-on-how-to-trust-the-https-development-certificate"></a>請參閱您 Linux 發行版的文件，來了解如何信任 HTTPS 開發憑證
---

4. 執行應用程式：

    ```console
    cd aspnetcoreapp
    dotnet run
    ```

5. 瀏覽至 [http://localhost:5001](http://localhost:5001)。  按一下 [接受] 以接受隱私權與 Cookie 原則。 此應用程式不會保留個人資訊。

6. 開啟 *Pages/About.cshtml*，然後以下列醒目提示的標記修改頁面：

    [!code-cshtml[](sample/getting-started/about.cshtml?highlight=9)]

7. 瀏覽到 [http://localhost:5001/About](http://localhost:5001/About) 並驗證已顯示變更。

[!INCLUDE [next steps](~/includes/getting-started/next-steps.md)]

::: moniker-end

::: moniker range="= aspnetcore-2.0"

1. 安裝 [!INCLUDE [](~/includes/net-core-sdk-download-link.md)]。

2. 建立新的 ASP.NET Core 專案。

   開啟命令殼層。 輸入下列命令：

    ```console
    dotnet new razor -o aspnetcoreapp
    ```

3. 使用下列命令來執行應用程式：

    ```console
    cd aspnetcoreapp
    dotnet run
    ```

4. 瀏覽至 [http://localhost:5000](http://localhost:5000)。

5. 開啟 *Pages/About.cshtml* 並將頁面顯示訊息修改為 "Hello, world! 伺服器的時間為 @DateTime.Now“ ：

    [!code-cshtml[](sample/getting-started/about.cshtml?highlight=9&range=1-9)]

6. 瀏覽至 [http://localhost:5000/About](http://localhost:5000/About) 並確認所做的變更。

[!INCLUDE [next steps](~/includes/getting-started/next-steps.md)]

::: moniker-end

::: moniker range="<= aspnetcore-1.1"

1. 從 [.NET Core All Downloads](https://www.microsoft.com/net/download/all) (.NET Core 所有下載) 頁面安裝適用於 SDK 1.0.4 的 .NET Core **SDK 安裝程式**。

2. 為新的 ASP.NET Core 專案建立資料夾。

   開啟命令殼層。 輸入下列命令：

   ```console
   mkdir aspnetcoreapp
   cd aspnetcoreapp
   ```

3. 如果您已在電腦上安裝較新版的 SDK，請建立 *global.json* 檔案來選取 1.0.4 SDK。

   ```json
   {
     "sdk": { "version": "1.0.4" }
   }
   ```

4. 建立新的 ASP.NET Core 專案。

   ```console
   dotnet new web
   ```

5. 還原套件。

    ```console
    dotnet restore
    ```

6. 執行應用程式。

   ```console
   dotnet run
   ```

   [dotnet run](/dotnet/core/tools/dotnet-run) 命令會在必要時先建置應用程式。

7. 瀏覽至 `http://localhost:5000`。

[!INCLUDE [next steps](~/includes/getting-started/next-steps.md)]
::: moniker-end
