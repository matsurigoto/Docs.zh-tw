---
uid: visual-studio/overview/2013/release-notes
title: "ASP.NET 及 Web Tools for Visual Studio 2013 版本資訊 |Microsoft 文件"
author: microsoft
description: "本文件說明 Visual Studio 2013 ASP.NET 及 Web 工具版本。"
ms.author: aspnetcontent
manager: wpickett
ms.date: 10/17/2013
ms.topic: article
ms.assetid: 08815768-2702-42ae-ae85-0a59934a11d1
ms.technology: 
ms.prod: .net-framework
msc.legacyurl: /visual-studio/overview/2013/release-notes
msc.type: authoredcontent
ms.openlocfilehash: 10835c39d3bca752ed3068a23fecaaab56449e41
ms.sourcegitcommit: 9a9483aceb34591c97451997036a9120c3fe2baf
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/10/2017
---
<a name="aspnet-and-web-tools-for-visual-studio-2013-release-notes"></a><span data-ttu-id="605aa-103">ASP.NET 及 Web Tools for Visual Studio 2013 版本資訊</span><span class="sxs-lookup"><span data-stu-id="605aa-103">ASP.NET and Web Tools for Visual Studio 2013 Release Notes</span></span>
====================
<span data-ttu-id="605aa-104">由[Microsoft](https://github.com/microsoft)</span><span class="sxs-lookup"><span data-stu-id="605aa-104">by [Microsoft](https://github.com/microsoft)</span></span>

> <span data-ttu-id="605aa-105">本文件說明 Visual Studio 2013 ASP.NET 及 Web 工具版本。</span><span class="sxs-lookup"><span data-stu-id="605aa-105">This document describes the release of ASP.NET and Web Tools for Visual Studio 2013.</span></span>


## <a name="contents"></a><span data-ttu-id="605aa-106">內容</span><span class="sxs-lookup"><span data-stu-id="605aa-106">Contents</span></span>

- [<span data-ttu-id="605aa-107">安裝注意事項</span><span class="sxs-lookup"><span data-stu-id="605aa-107">Installation Notes</span></span>](#TOC1)
- [<span data-ttu-id="605aa-108">文件 (英文)</span><span class="sxs-lookup"><span data-stu-id="605aa-108">Documentation</span></span>](#TOC2)
- [<span data-ttu-id="605aa-109">軟體需求</span><span class="sxs-lookup"><span data-stu-id="605aa-109">Software Requirements</span></span>](#TOC4)

### <a name="new-features-in-aspnet-and-web-tools-for-visual-studio-2013"></a><span data-ttu-id="605aa-110">在 ASP.NET 和 Web Tools for Visual Studio 2013 中的新功能</span><span class="sxs-lookup"><span data-stu-id="605aa-110">New Features in ASP.NET and Web Tools for Visual Studio 2013</span></span>

- [<span data-ttu-id="605aa-111">一個 ASP.NET</span><span class="sxs-lookup"><span data-stu-id="605aa-111">One ASP.NET</span></span>](#TOC6)
- [<span data-ttu-id="605aa-112">新的 Web 專案經驗</span><span class="sxs-lookup"><span data-stu-id="605aa-112">New Web Project Experience</span></span>](#newproj)
- [<span data-ttu-id="605aa-113">ASP.NET Scaffolding</span><span class="sxs-lookup"><span data-stu-id="605aa-113">ASP.NET Scaffolding</span></span>](#scaffold)
- [<span data-ttu-id="605aa-114">瀏覽器連結</span><span class="sxs-lookup"><span data-stu-id="605aa-114">Browser Link</span></span>](#browser-link)
- [<span data-ttu-id="605aa-115">Visual Studio Web 編輯器增強功能</span><span class="sxs-lookup"><span data-stu-id="605aa-115">Visual Studio Web Editor Enhancements</span></span>](#web-editor)
- [<span data-ttu-id="605aa-116">在 Visual Studio 中的 azure App Service Web 應用程式支援</span><span class="sxs-lookup"><span data-stu-id="605aa-116">Azure App Service Web Apps Support in Visual Studio</span></span>](#waws)
- [<span data-ttu-id="605aa-117">Web 發行的增強功能</span><span class="sxs-lookup"><span data-stu-id="605aa-117">Web Publish Enhancements</span></span>](#publish)
- [<span data-ttu-id="605aa-118">NuGet 2.7</span><span class="sxs-lookup"><span data-stu-id="605aa-118">NuGet 2.7</span></span>](#nuget)
- [<span data-ttu-id="605aa-119">ASP.NET Web Form</span><span class="sxs-lookup"><span data-stu-id="605aa-119">ASP.NET Web Forms</span></span>](#TOC9)
- [<span data-ttu-id="605aa-120">ASP.NET MVC 5</span><span class="sxs-lookup"><span data-stu-id="605aa-120">ASP.NET MVC 5</span></span>](#TOC10)
- [<span data-ttu-id="605aa-121">ASP.NET Web API 2</span><span class="sxs-lookup"><span data-stu-id="605aa-121">ASP.NET Web API 2</span></span>](#TOC11)
- [<span data-ttu-id="605aa-122">ASP.NET SignalR</span><span class="sxs-lookup"><span data-stu-id="605aa-122">ASP.NET SignalR</span></span>](#TOC13)
- [<span data-ttu-id="605aa-123">ASP.NET Identity</span><span class="sxs-lookup"><span data-stu-id="605aa-123">ASP.NET Identity</span></span>](#TOC8)
- [<span data-ttu-id="605aa-124">Microsoft OWIN 元件</span><span class="sxs-lookup"><span data-stu-id="605aa-124">Microsoft OWIN Components</span></span>](#TOC7)
- [<span data-ttu-id="605aa-125">Entity Framework 6</span><span class="sxs-lookup"><span data-stu-id="605aa-125">Entity Framework 6</span></span>](#ef6)
- [<span data-ttu-id="605aa-126">ASP.NET Razor 3</span><span class="sxs-lookup"><span data-stu-id="605aa-126">ASP.NET Razor 3</span></span>](#TOC14)
- [<span data-ttu-id="605aa-127">ASP.NET 應用程式暫停</span><span class="sxs-lookup"><span data-stu-id="605aa-127">ASP.NET App Suspend</span></span>](#TOC15)
- [<span data-ttu-id="605aa-128">已知的問題和重大變更</span><span class="sxs-lookup"><span data-stu-id="605aa-128">Known Issues and Breaking Changes</span></span>](#knownissues)

<a id="TOC1"></a>
## <a name="installation-notes"></a><span data-ttu-id="605aa-129">安裝注意事項</span><span class="sxs-lookup"><span data-stu-id="605aa-129">Installation Notes</span></span>

<span data-ttu-id="605aa-130">ASP.NET 及 Web Tools for Visual Studio 2013 會集結在主要安裝程式，而且可以下載[這裡](https://www.asp.net/downloads)。</span><span class="sxs-lookup"><span data-stu-id="605aa-130">ASP.NET and Web Tools for Visual Studio 2013 are bundled in the main installer and can be downloaded [here](https://www.asp.net/downloads).</span></span>

<a id="TOC2"></a>
## <a name="documentation"></a><span data-ttu-id="605aa-131">文件</span><span class="sxs-lookup"><span data-stu-id="605aa-131">Documentation</span></span>

<span data-ttu-id="605aa-132">教學課程和其他資訊 ASP.NET 及 Web Tools for Visual Studio 2013 都是從[ASP.NET 網站](https://www.asp.net/)。</span><span class="sxs-lookup"><span data-stu-id="605aa-132">Tutorials and other information about ASP.NET and Web Tools for Visual Studio 2013 are available from the [ASP.NET web site](https://www.asp.net/).</span></span>

<a id="TOC4"></a>
## <a name="software-requirements"></a><span data-ttu-id="605aa-133">軟體需求</span><span class="sxs-lookup"><span data-stu-id="605aa-133">Software Requirements</span></span>

<span data-ttu-id="605aa-134">ASP.NET 及 Web 工具需要 Visual Studio 2013。</span><span class="sxs-lookup"><span data-stu-id="605aa-134">ASP.NET and Web Tools requires Visual Studio 2013.</span></span>

<a id="TOC5"></a>
## <a name="new-features-in-aspnet-and-web-tools-for-visual-studio-2013"></a><span data-ttu-id="605aa-135">在 ASP.NET 和 Web Tools for Visual Studio 2013 中的新功能</span><span class="sxs-lookup"><span data-stu-id="605aa-135">New Features in ASP.NET and Web Tools for Visual Studio 2013</span></span>

<span data-ttu-id="605aa-136">下列章節說明在版本中已引進的功能。</span><span class="sxs-lookup"><span data-stu-id="605aa-136">The following sections describe the features that have been introduced in the release.</span></span>

<a id="TOC6"></a>
## <a name="one-aspnet"></a><span data-ttu-id="605aa-137">一個 ASP.NET</span><span class="sxs-lookup"><span data-stu-id="605aa-137">One ASP.NET</span></span>

<span data-ttu-id="605aa-138">使用 Visual Studio 2013 版本，我們已了進一步的整合，讓您輕鬆混合和比對您想的要使用 ASP.NET 技術的體驗。</span><span class="sxs-lookup"><span data-stu-id="605aa-138">With the release of Visual Studio 2013, we have taken a step towards unifying the experience of using ASP.NET technologies, so that you can easily mix and match the ones you want.</span></span> <span data-ttu-id="605aa-139">比方說，您可以開始使用 MVC 專案並輕鬆地更新版本中，加入至專案的 Web Form 網頁或 scaffold Web Form 專案中的 Web 應用程式開發介面。</span><span class="sxs-lookup"><span data-stu-id="605aa-139">For example, you can start a project using MVC and easily add Web Forms pages to the project later, or scaffold Web APIs in a Web Forms project.</span></span> <span data-ttu-id="605aa-140">一個 ASP.NET 就是要讓更容易為您身為開發人員要您喜歡在 ASP.NET 中的項目。</span><span class="sxs-lookup"><span data-stu-id="605aa-140">One ASP.NET is all about making it easier for you as a developer to do the things you love in ASP.NET.</span></span> <span data-ttu-id="605aa-141">無論您選擇何種技術，您可以讓您一個 ASP.NET 的信任基礎架構建置的信心。</span><span class="sxs-lookup"><span data-stu-id="605aa-141">No matter what technology you choose, you can have confidence that you are building on the trusted underlying framework of One ASP.NET.</span></span>

<a id="newproj"></a>
## <a name="new-web-project-experience"></a><span data-ttu-id="605aa-142">新的 Web 專案經驗</span><span class="sxs-lookup"><span data-stu-id="605aa-142">New Web Project Experience</span></span>

<span data-ttu-id="605aa-143">我們有增強 Visual Studio 2013 中建立新的 web 專案的經驗。</span><span class="sxs-lookup"><span data-stu-id="605aa-143">We have enhanced the experience of creating new web projects in Visual Studio 2013.</span></span> <span data-ttu-id="605aa-144">在**新的 ASP.NET Web 專案**對話方塊，您可以選取專案類型，設定技術 (Web Forms、 MVC、 Web API) 的任何組合，設定驗證選項，然後加入單元測試專案。</span><span class="sxs-lookup"><span data-stu-id="605aa-144">In the **New ASP.NET Web Project** dialog you can select the project type you want, configure any combination of technologies (Web Forms, MVC, Web API), configure authentication options, and add a unit test project.</span></span>

![新增 ASP.NET 專案](release-notes/_static/image1.png)

<span data-ttu-id="605aa-146">[新增] 對話方塊可讓您變更許多範本的預設驗證選項。</span><span class="sxs-lookup"><span data-stu-id="605aa-146">The new dialog enables you to change the default authentication options for many of the templates.</span></span> <span data-ttu-id="605aa-147">例如，當您建立的 ASP.NET Web Form 專案時您可以選取任何下列選項：</span><span class="sxs-lookup"><span data-stu-id="605aa-147">For example, when you create an ASP.NET Web Forms project you can select any of the following options:</span></span>

- <span data-ttu-id="605aa-148">無驗證</span><span class="sxs-lookup"><span data-stu-id="605aa-148">No Authentication</span></span>
- <span data-ttu-id="605aa-149">個別使用者帳戶 （ASP.NET 成員資格或社交提供者登入）</span><span class="sxs-lookup"><span data-stu-id="605aa-149">Individual User Accounts (ASP.NET membership or social provider log in)</span></span>
- <span data-ttu-id="605aa-150">組織帳戶 (網際網路應用程式中的 Active Directory)</span><span class="sxs-lookup"><span data-stu-id="605aa-150">Organizational Accounts (Active Directory in an internet application)</span></span>
- <span data-ttu-id="605aa-151">Windows 驗證 (內部網路應用程式中的 Active Directory)</span><span class="sxs-lookup"><span data-stu-id="605aa-151">Windows Authentication (Active Directory in an intranet application)</span></span>

![驗證選項](release-notes/_static/image2.png)

<span data-ttu-id="605aa-153">如需建立 web 專案的新程序的詳細資訊，請參閱[Visual Studio 2013 中建立 ASP.NET Web 專案](creating-web-projects-in-visual-studio.md)。</span><span class="sxs-lookup"><span data-stu-id="605aa-153">For more information about the new process for creating web projects, see [Creating ASP.NET Web Projects in Visual Studio 2013](creating-web-projects-in-visual-studio.md).</span></span> <span data-ttu-id="605aa-154">如需新的驗證選項的詳細資訊，請參閱[ASP.NET Identity](#TOC8)本文件後面。</span><span class="sxs-lookup"><span data-stu-id="605aa-154">For more information about the new authentication options, see [ASP.NET Identity](#TOC8) later in this document.</span></span>

<a id="scaffold"></a>
## <a name="aspnet-scaffolding"></a><span data-ttu-id="605aa-155">ASP.NET Scaffolding</span><span class="sxs-lookup"><span data-stu-id="605aa-155">ASP.NET Scaffolding</span></span>

<span data-ttu-id="605aa-156">ASP.NET Scaffolding 是 ASP.NET Web 應用程式的程式碼產生架構。</span><span class="sxs-lookup"><span data-stu-id="605aa-156">ASP.NET Scaffolding is a code generation framework for ASP.NET Web applications.</span></span> <span data-ttu-id="605aa-157">它可讓您輕鬆地將未定案程式碼加入至您的專案與資料模型互動。</span><span class="sxs-lookup"><span data-stu-id="605aa-157">It makes it easy to add boilerplate code to your project that interacts with a data model.</span></span>

<span data-ttu-id="605aa-158">在舊版的 Visual Studio 中，scaffolding 限於 ASP.NET MVC 專案。</span><span class="sxs-lookup"><span data-stu-id="605aa-158">In previous versions of Visual Studio, scaffolding was limited to ASP.NET MVC projects.</span></span> <span data-ttu-id="605aa-159">使用 Visual Studio 2013，您現在可以針對任何 ASP.NET 專案，包括 Web Form 使用 scaffolding。</span><span class="sxs-lookup"><span data-stu-id="605aa-159">With Visual Studio 2013, you can now use scaffolding for any ASP.NET project, including Web Forms.</span></span> <span data-ttu-id="605aa-160">Visual Studio 2013 目前不支援產生頁面的 Web Form 專案，但您仍然可以使用與 Web Form scaffolding，將 MVC 相依性加入至專案。</span><span class="sxs-lookup"><span data-stu-id="605aa-160">Visual Studio 2013 does not currently support generating pages for a Web Forms project, but you can still use scaffolding with Web Forms by adding MVC dependencies to the project.</span></span> <span data-ttu-id="605aa-161">在未來的更新中，將會加入產生的 Web Form 網頁的支援。</span><span class="sxs-lookup"><span data-stu-id="605aa-161">Support for generating pages for Web Forms will be added in a future update.</span></span>

<span data-ttu-id="605aa-162">當使用 scaffolding，我們可以確定所有必要的相依性安裝到專案。</span><span class="sxs-lookup"><span data-stu-id="605aa-162">When using scaffolding, we ensure that all required dependencies are installed in the project.</span></span> <span data-ttu-id="605aa-163">比方說，如果您從 ASP.NET Web Form 專案開始，然後使用 scaffolding 新增 Web API 控制器所需的 NuGet 封裝和參考會加入至您的專案會自動。</span><span class="sxs-lookup"><span data-stu-id="605aa-163">For example, if you start with an ASP.NET Web Forms project and then use scaffolding to add a Web API Controller, the required NuGet packages and references are added to your project automatically.</span></span>

<span data-ttu-id="605aa-164">MVC 樣板加入至 Web Form 專案，加入**新的 Scaffold 項目**選取**MVC 5 相依性**對話視窗中。</span><span class="sxs-lookup"><span data-stu-id="605aa-164">To add MVC scaffolding to a Web Forms project, add a **New Scaffolded Item** and select **MVC 5 Dependencies** in the dialog window.</span></span> <span data-ttu-id="605aa-165">有兩個選項的 scaffolding MVC;最少且完整。</span><span class="sxs-lookup"><span data-stu-id="605aa-165">There are two options for scaffolding MVC; Minimal and Full.</span></span> <span data-ttu-id="605aa-166">如果您選取最少，只有 NuGet 封裝和 ASP.NET MVC 的參考會加入至您的專案。</span><span class="sxs-lookup"><span data-stu-id="605aa-166">If you select Minimal, only the NuGet packages and references for ASP.NET MVC are added to your project.</span></span> <span data-ttu-id="605aa-167">如果您選取 [完整] 選項，加入最少的相依性，以及所需的內容檔案的 MVC 專案。</span><span class="sxs-lookup"><span data-stu-id="605aa-167">If you select the Full option, the Minimal dependencies are added, as well as the required content files for an MVC project.</span></span>

<span data-ttu-id="605aa-168">支援的 scaffolding 非同步控制器會使用新的非同步功能，從 Entity Framework 6。</span><span class="sxs-lookup"><span data-stu-id="605aa-168">Support for scaffolding async controllers uses the new async features from Entity Framework 6.</span></span>

<span data-ttu-id="605aa-169">如需詳細資訊和教學課程，請參閱[ASP.NET Scaffolding 概觀](aspnet-scaffolding-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="605aa-169">For more information and tutorials, see [ASP.NET Scaffolding Overview](aspnet-scaffolding-overview.md).</span></span>

<a id="browser-link"></a>
## <a name="browser-link--signalr-channel-between-browser-and-visual-studio"></a><span data-ttu-id="605aa-170">瀏覽器連結-瀏覽器和 Visual Studio 之間的 SignalR 通道</span><span class="sxs-lookup"><span data-stu-id="605aa-170">Browser Link – SignalR channel between browser and Visual Studio</span></span>

<span data-ttu-id="605aa-171">新[瀏覽器連結](using-browser-link.md)功能可讓您連接至 Visual Studio 的多個瀏覽器，並加以重新整理所有依序按一下工具列中的按鈕。</span><span class="sxs-lookup"><span data-stu-id="605aa-171">The new [Browser Link](using-browser-link.md) feature lets you connect multiple browsers to Visual Studio and refresh them all by clicking a button in the toolbar.</span></span> <span data-ttu-id="605aa-172">您可以連接到您的開發網站，包括行動模擬器的多個瀏覽器，並按一下 重新整理以重新整理所有瀏覽器，所有在相同的時間。</span><span class="sxs-lookup"><span data-stu-id="605aa-172">You can connect multiple browsers to your development site, including mobile emulators, and click refresh to refresh all the browsers all at the same time.</span></span> <span data-ttu-id="605aa-173">瀏覽器連結也會公開可讓開發人員來寫入瀏覽器連結延伸的 API。</span><span class="sxs-lookup"><span data-stu-id="605aa-173">Browser Link also exposes an API to enable developers to write Browser Link extensions.</span></span>

![](release-notes/_static/image3.png)

<span data-ttu-id="605aa-174">讓開發人員充分利用瀏覽器連結 API，它會變成可以建立 Visual Studio 和任何連接的瀏覽器之間跨越界限的非常進階的案例。</span><span class="sxs-lookup"><span data-stu-id="605aa-174">By enabling developers to take advantage of the Browser Link API, it becomes possible to create very advanced scenarios that crosses boundaries between Visual Studio and any browser that's connected.</span></span> <span data-ttu-id="605aa-175">Web Essentials 利用 API 來建立 Visual Studio 和瀏覽器的開發人員工具，遠端控制行動模擬器以及其他的之間的整合式的經驗。</span><span class="sxs-lookup"><span data-stu-id="605aa-175">Web Essentials takes advantage of the API to create an integrated experience between Visual Studio and the browser's developer tools, remote controlling mobile emulators and a lot more.</span></span>

<a id="web-editor"></a>
## <a name="visual-studio-web-editor-enhancements"></a><span data-ttu-id="605aa-176">Visual Studio Web 編輯器增強功能</span><span class="sxs-lookup"><span data-stu-id="605aa-176">Visual Studio Web Editor Enhancements</span></span>

<span data-ttu-id="605aa-177">Visual Studio 2013 web 應用程式中包含新的 HTML 編輯器，Razor 檔案和 HTML 檔。</span><span class="sxs-lookup"><span data-stu-id="605aa-177">Visual Studio 2013 includes a new HTML editor for Razor files and HTML files in web applications.</span></span> <span data-ttu-id="605aa-178">新的 HTML 編輯器提供 HTML5 為基礎的單一統一結構描述。</span><span class="sxs-lookup"><span data-stu-id="605aa-178">The new HTML editor provides a single unified schema based on HTML5.</span></span> <span data-ttu-id="605aa-179">它有自動大括號完成、 jQuery UI 和 AngularJS 屬性 IntelliSense，屬性 IntelliSense 群組、 ID 和類別名稱 Intellisense，以及其他改進還包括提升效能、 格式和智慧標籤。</span><span class="sxs-lookup"><span data-stu-id="605aa-179">It has automatic brace completion, jQuery UI and AngularJS attribute IntelliSense, attribute IntelliSense Grouping, ID and class name Intellisense, and other improvements including better performance, formatting and SmartTags.</span></span>

<span data-ttu-id="605aa-180">下列螢幕擷取畫面將示範如何使用啟動程序屬性 IntelliSense HTML 編輯器中。</span><span class="sxs-lookup"><span data-stu-id="605aa-180">The following screenshot demonstrates using Bootstrap attribute IntelliSense in the HTML editor.</span></span>

![HTML 編輯器中的 Intellisense](release-notes/_static/image4.png)

<span data-ttu-id="605aa-182">Visual Studio 2013 也提供使用這兩個 CoffeeScript 和較低的內建的編輯器。</span><span class="sxs-lookup"><span data-stu-id="605aa-182">Visual Studio 2013 also comes with both CoffeeScript and LESS editors built in.</span></span> <span data-ttu-id="605aa-183">LESS 編輯器所有酷炫的功能來自 CSS 編輯器，且所有較少文件中都有特定的 Intellisense 的變數和 mixins@import鏈結。</span><span class="sxs-lookup"><span data-stu-id="605aa-183">The LESS editor comes with all the cool features from the CSS editor and has specific Intellisense for variables and mixins across all the LESS documents in the @import chain.</span></span>

<a id="waws"></a>
## <a name="azure-app-service-web-apps-support-in-visual-studio"></a><span data-ttu-id="605aa-184">在 Visual Studio 中的 azure App Service Web 應用程式支援</span><span class="sxs-lookup"><span data-stu-id="605aa-184">Azure App Service Web Apps Support in Visual Studio</span></span>

<span data-ttu-id="605aa-185">在與 Azure SDK for.NET 2.2 的 Visual Studio 2013，您可以使用**伺服器總管**直接與遠端的 web 應用程式互動。</span><span class="sxs-lookup"><span data-stu-id="605aa-185">In Visual Studio 2013 with the Azure SDK for .NET 2.2, you can use **Server Explorer** to interact directly with your remote web apps.</span></span> <span data-ttu-id="605aa-186">您可以登入您的 Azure 帳戶、 建立新的 web 應用程式，設定應用程式、 檢視即時記錄，以及更多。</span><span class="sxs-lookup"><span data-stu-id="605aa-186">You can sign in to your Azure account, create new web apps, configure apps, view real-time logs, and more.</span></span> <span data-ttu-id="605aa-187">推出之後 SDK 2.2 即發行，您可以在 Azure 中的遠端偵錯模式執行。</span><span class="sxs-lookup"><span data-stu-id="605aa-187">Coming soon after SDK 2.2 is released, you'll be able to run in debug mode remotely in Azure.</span></span> <span data-ttu-id="605aa-188">當您安裝最新版的 Azure sdk for.NET 時，大部分的 Azure App Service Web 應用程式的新功能也在 Visual Studio 2012 中運作。</span><span class="sxs-lookup"><span data-stu-id="605aa-188">Most of the new features for Azure App Service Web Apps also work in Visual Studio 2012 when you install the current release of the Azure SDK for .NET.</span></span>

<span data-ttu-id="605aa-189">如需詳細資訊，請參閱下列資源：</span><span class="sxs-lookup"><span data-stu-id="605aa-189">For more information, see the following resources:</span></span>

- [<span data-ttu-id="605aa-190">在 Azure App Service 中建立 ASP.NET web 應用程式</span><span class="sxs-lookup"><span data-stu-id="605aa-190">Create an ASP.NET web app in Azure App Service</span></span>](https://azure.microsoft.com/en-us/documentation/articles/web-sites-dotnet-get-started/)
- [<span data-ttu-id="605aa-191">疑難排解 Azure App Service 使用 Visual Studio 中的 web 應用程式</span><span class="sxs-lookup"><span data-stu-id="605aa-191">Troubleshoot a web app in Azure App Service using Visual Studio</span></span>](https://azure.microsoft.com/en-us/documentation/articles/web-sites-dotnet-troubleshoot-visual-studio/)

<a id="publish"></a>
## <a name="web-publish-enhancements"></a><span data-ttu-id="605aa-192">Web 發行的增強功能</span><span class="sxs-lookup"><span data-stu-id="605aa-192">Web Publish Enhancements</span></span>

<span data-ttu-id="605aa-193">Visual Studio 2013 包含新功能和增強 Web Publish 功能。</span><span class="sxs-lookup"><span data-stu-id="605aa-193">Visual Studio 2013 includes new and enhanced Web Publish features.</span></span> <span data-ttu-id="605aa-194">以下是少數幾個：</span><span class="sxs-lookup"><span data-stu-id="605aa-194">Here are a few of them:</span></span>

- <span data-ttu-id="605aa-195">輕鬆地[自動化 Web.config 檔案加密](https://go.microsoft.com/fwlink/?LinkId=325529)。</span><span class="sxs-lookup"><span data-stu-id="605aa-195">Easily [automate Web.config file encryption](https://go.microsoft.com/fwlink/?LinkId=325529).</span></span> <span data-ttu-id="605aa-196">（此連結和下面兩個點上可能無法使用之前在 10/17 當天的 MSDN 文件。）</span><span class="sxs-lookup"><span data-stu-id="605aa-196">(This link and the following two point to documentation on MSDN that might not be available until late in the day on 10/17.)</span></span>
- <span data-ttu-id="605aa-197">輕鬆地[自動化取得應用程式離線以在部署期間](https://go.microsoft.com/fwlink/?LinkId=325530)。</span><span class="sxs-lookup"><span data-stu-id="605aa-197">Easily [automate taking an application offline during deployment](https://go.microsoft.com/fwlink/?LinkId=325530).</span></span>
- <span data-ttu-id="605aa-198">設定 Web Deploy 以[檔案總和檢查碼使用而不是上次變更日期](https://go.microsoft.com/fwlink/?LinkId=325531)來判斷哪些檔案應該複製到伺服器。</span><span class="sxs-lookup"><span data-stu-id="605aa-198">Configure Web Deploy to [use file checksum instead of last-changed date](https://go.microsoft.com/fwlink/?LinkId=325531) for determining which files should be copied to the server.</span></span>
- <span data-ttu-id="605aa-199">當您使用 FTP 或檔案系統發行方法時，以及使用 Web Deploy，快速地發佈個別選取的檔案 （包括 Web.config）。</span><span class="sxs-lookup"><span data-stu-id="605aa-199">Quickly publish individual selected files (including Web.config) when you're using the FTP or file system publish methods as well as with Web Deploy.</span></span>

<span data-ttu-id="605aa-200">如需 ASP.NET web 部署的詳細資訊，請參閱[ASP.NET 網站](https://go.microsoft.com/fwlink/?LinkId=322027)。</span><span class="sxs-lookup"><span data-stu-id="605aa-200">For more information about ASP.NET web deployment, see [the ASP.NET site](https://go.microsoft.com/fwlink/?LinkId=322027).</span></span>

<a id="nuget"></a>
## <a name="nuget-27"></a><span data-ttu-id="605aa-201">NuGet 2.7</span><span class="sxs-lookup"><span data-stu-id="605aa-201">NuGet 2.7</span></span>

<span data-ttu-id="605aa-202">NuGet 2.7 包含一組豐富的新功能所說明的詳細討論[NuGet 2.7 版本資訊](http://docs.nuget.org/docs/release-notes/nuget-2.7)。</span><span class="sxs-lookup"><span data-stu-id="605aa-202">NuGet 2.7 includes a rich set of new features which are described in detail at [NuGet 2.7 Release Notes](http://docs.nuget.org/docs/release-notes/nuget-2.7).</span></span>

<span data-ttu-id="605aa-203">這個版本的 NuGet 也不再需要明確同意下載的套件，NuGet 的封裝還原功能。</span><span class="sxs-lookup"><span data-stu-id="605aa-203">This version of NuGet also removes the need to provide explicit consent for NuGet's package restore feature to download packages.</span></span> <span data-ttu-id="605aa-204">藉由安裝 NuGet 現在授與同意 （與在 NuGet 的喜好設定對話方塊相關聯的核取方塊）。</span><span class="sxs-lookup"><span data-stu-id="605aa-204">Consent (and the associated checkbox in NuGet's preferences dialog) is now granted by installing NuGet.</span></span> <span data-ttu-id="605aa-205">現在套件還原只運作方式是預設值。</span><span class="sxs-lookup"><span data-stu-id="605aa-205">Now package restore simply works by default.</span></span>

<a id="TOC9"></a>
## <a name="aspnet-web-forms"></a><span data-ttu-id="605aa-206">ASP.NET Web Form</span><span class="sxs-lookup"><span data-stu-id="605aa-206">ASP.NET Web Forms</span></span>

### <a name="one-aspnet"></a><span data-ttu-id="605aa-207">一個 ASP.NET</span><span class="sxs-lookup"><span data-stu-id="605aa-207">One ASP.NET</span></span>

<span data-ttu-id="605aa-208">Web Form 專案範本緊密整合新的一個 ASP.NET 體驗中。</span><span class="sxs-lookup"><span data-stu-id="605aa-208">The Web Forms project templates integrate seamlessly with the new One ASP.NET experience.</span></span> <span data-ttu-id="605aa-209">您可以將 MVC 和 Web 應用程式開發介面支援至 Web Form 專案，而且您可以設定使用一個 ASP.NET 專案建立精靈的驗證。</span><span class="sxs-lookup"><span data-stu-id="605aa-209">You can add MVC and Web API support to your Web Forms project, and you can configure authentication using the One ASP.NET project creation wizard.</span></span> <span data-ttu-id="605aa-210">如需詳細資訊，請參閱[Visual Studio 2013 中建立 ASP.NET Web 專案](creating-web-projects-in-visual-studio.md)。</span><span class="sxs-lookup"><span data-stu-id="605aa-210">For more information, see [Creating ASP.NET Web Projects in Visual Studio 2013](creating-web-projects-in-visual-studio.md).</span></span>

### <a name="aspnet-identity"></a><span data-ttu-id="605aa-211">ASP.NET Identity</span><span class="sxs-lookup"><span data-stu-id="605aa-211">ASP.NET Identity</span></span>

<span data-ttu-id="605aa-212">Web Form 專案範本支援新的 ASP.NET Identity framework。</span><span class="sxs-lookup"><span data-stu-id="605aa-212">The Web Forms project templates support the new ASP.NET Identity framework.</span></span> <span data-ttu-id="605aa-213">此外，範本現在支援建立 Web Form 內部網路專案。</span><span class="sxs-lookup"><span data-stu-id="605aa-213">In addition, the templates now support creation of a Web Forms intranet project.</span></span> <span data-ttu-id="605aa-214">如需詳細資訊，請參閱[驗證方法](creating-web-projects-in-visual-studio.md#auth)中**Visual Studio 2013 中建立 ASP.NET Web 專案**。</span><span class="sxs-lookup"><span data-stu-id="605aa-214">For more information, see [Authentication Methods](creating-web-projects-in-visual-studio.md#auth) in **Creating ASP.NET Web Projects in Visual Studio 2013**.</span></span>

### <a name="bootstrap"></a><span data-ttu-id="605aa-215">啟動程序</span><span class="sxs-lookup"><span data-stu-id="605aa-215">Bootstrap</span></span>

<span data-ttu-id="605aa-216">Web Form 範本使用[Bootstrap](http://twitter.github.io/bootstrap/)提供精緻且回應迅速外觀及操作，您可以輕鬆地自訂。</span><span class="sxs-lookup"><span data-stu-id="605aa-216">The Web Forms templates use [Bootstrap](http://twitter.github.io/bootstrap/) to provide a sleek and responsive look and feel that you can easily customize.</span></span> <span data-ttu-id="605aa-217">如需詳細資訊，請參閱[啟動 Visual Studio 2013 的 web 專案範本中的程序](creating-web-projects-in-visual-studio.md#bootstrap)。</span><span class="sxs-lookup"><span data-stu-id="605aa-217">For more information, see [Bootstrap in the Visual Studio 2013 web project templates](creating-web-projects-in-visual-studio.md#bootstrap).</span></span>

<a id="TOC10"></a>
## <a name="aspnet-mvc-5"></a><span data-ttu-id="605aa-218">ASP.NET MVC 5</span><span class="sxs-lookup"><span data-stu-id="605aa-218">ASP.NET MVC 5</span></span>

### <a name="one-aspnet"></a><span data-ttu-id="605aa-219">一個 ASP.NET</span><span class="sxs-lookup"><span data-stu-id="605aa-219">One ASP.NET</span></span>

<span data-ttu-id="605aa-220">Web MVC 專案範本緊密整合新的一個 ASP.NET 體驗中。</span><span class="sxs-lookup"><span data-stu-id="605aa-220">The Web MVC project templates integrate seamlessly with the new One ASP.NET experience.</span></span> <span data-ttu-id="605aa-221">您可以自訂 MVC 專案，並使用一個 ASP.NET 專案建立精靈設定驗證。</span><span class="sxs-lookup"><span data-stu-id="605aa-221">You can customize your MVC project and configure authentication using the One ASP.NET project creation wizard.</span></span> <span data-ttu-id="605aa-222">ASP.NET MVC 5 需入門教學課程，請參閱[開始使用 ASP.NET MVC 5](../../../mvc/overview/getting-started/introduction/getting-started.md)。</span><span class="sxs-lookup"><span data-stu-id="605aa-222">An introductory tutorial to ASP.NET MVC 5 can be found at [Getting Started with ASP.NET MVC 5](../../../mvc/overview/getting-started/introduction/getting-started.md).</span></span>

<span data-ttu-id="605aa-223">將 MVC 4 專案升級至 MVC 5 的資訊，請參閱[如何將 ASP.NET MVC 4 和 Web API 專案升級至 ASP.NET MVC 5 和 Web API 2](../../../mvc/overview/releases/how-to-upgrade-an-aspnet-mvc-4-and-web-api-project-to-aspnet-mvc-5-and-web-api-2.md)。</span><span class="sxs-lookup"><span data-stu-id="605aa-223">For information on upgrading MVC 4 projects to MVC 5, see [How to Upgrade an ASP.NET MVC 4 and Web API Project to ASP.NET MVC 5 and Web API 2](../../../mvc/overview/releases/how-to-upgrade-an-aspnet-mvc-4-and-web-api-project-to-aspnet-mvc-5-and-web-api-2.md).</span></span>

### <a name="aspnet-identity"></a><span data-ttu-id="605aa-224">ASP.NET Identity</span><span class="sxs-lookup"><span data-stu-id="605aa-224">ASP.NET Identity</span></span>

<span data-ttu-id="605aa-225">要用於驗證和身分識別管理 ASP.NET 識別的 MVC 專案範本已更新。</span><span class="sxs-lookup"><span data-stu-id="605aa-225">The MVC project templates have been updated to use ASP.NET Identity for authentication and identity management.</span></span> <span data-ttu-id="605aa-226">將 Facebook 和 Google 驗證和新的成員資格應用程式開發介面設為特色的教學課程，請參閱[建立 ASP.NET MVC 5 應用程式與 Facebook、 Google OAuth2 和 OpenID 登入](../../../mvc/overview/security/create-an-aspnet-mvc-5-app-with-facebook-and-google-oauth2-and-openid-sign-on.md)和[建立 ASP.NET MVC 應用程式具有驗證和SQL 資料庫並部署至 Azure App Service](https://azure.microsoft.com/en-us/documentation/articles/web-sites-dotnet-deploy-aspnet-mvc-app-membership-oauth-sql-database/)。</span><span class="sxs-lookup"><span data-stu-id="605aa-226">A tutorial featuring Facebook and Google authentication and the new membership API can be found at [Create an ASP.NET MVC 5 App with Facebook and Google OAuth2 and OpenID Sign-on](../../../mvc/overview/security/create-an-aspnet-mvc-5-app-with-facebook-and-google-oauth2-and-openid-sign-on.md) and [Create an ASP.NET MVC app with auth and SQL DB and deploy to Azure App Service](https://azure.microsoft.com/en-us/documentation/articles/web-sites-dotnet-deploy-aspnet-mvc-app-membership-oauth-sql-database/).</span></span>

### <a name="bootstrap"></a><span data-ttu-id="605aa-227">啟動程序</span><span class="sxs-lookup"><span data-stu-id="605aa-227">Bootstrap</span></span>

<span data-ttu-id="605aa-228">MVC 專案範本已更新為使用[Bootstrap](http://getbootstrap.com/)提供精緻且回應迅速外觀及操作，您可以輕鬆地自訂。</span><span class="sxs-lookup"><span data-stu-id="605aa-228">The MVC project template has been updated to use [Bootstrap](http://getbootstrap.com/) to provide a sleek and responsive look and feel that you can easily customize.</span></span> <span data-ttu-id="605aa-229">如需詳細資訊，請參閱[啟動 Visual Studio 2013 的 web 專案範本中的程序](creating-web-projects-in-visual-studio.md#bootstrap)。</span><span class="sxs-lookup"><span data-stu-id="605aa-229">For more information, see [Bootstrap in the Visual Studio 2013 web project templates](creating-web-projects-in-visual-studio.md#bootstrap).</span></span>

### <a name="authentication-filters"></a><span data-ttu-id="605aa-230">驗證篩選條件</span><span class="sxs-lookup"><span data-stu-id="605aa-230">Authentication filters</span></span>

<span data-ttu-id="605aa-231">驗證篩選條件是一種新的 ASP.NET MVC 管線中的授權篩選條件之前執行，並允許您指定驗證邏輯每個動作，ASP.NET MVC 中篩選每個控制器，或全域的所有控制站。</span><span class="sxs-lookup"><span data-stu-id="605aa-231">Authentication filters are a new kind of filter in ASP.NET MVC that run prior to authorization filters in the ASP.NET MVC pipeline and allow you to specify authentication logic per-action, per-controller, or globally for all controllers.</span></span> <span data-ttu-id="605aa-232">驗證篩選條件處理要求中的認證，並提供對應的主體。</span><span class="sxs-lookup"><span data-stu-id="605aa-232">Authentication filters process credentials in the request and provide a corresponding principal.</span></span> <span data-ttu-id="605aa-233">驗證篩選條件也可以將驗證挑戰回應未經授權的要求。</span><span class="sxs-lookup"><span data-stu-id="605aa-233">Authentication filters can also add authentication challenges in response to unauthorized requests.</span></span>

### <a name="filter-overrides"></a><span data-ttu-id="605aa-234">篩選會覆寫</span><span class="sxs-lookup"><span data-stu-id="605aa-234">Filter overrides</span></span>

<span data-ttu-id="605aa-235">您現在可以覆寫的篩選會套用至指定的動作方法或控制器藉由指定覆寫篩選條件。</span><span class="sxs-lookup"><span data-stu-id="605aa-235">You can now override which filters apply to a given action method or controller by specifying an override filter.</span></span> <span data-ttu-id="605aa-236">覆寫篩選條件會指定一組篩選器型別，且不應該執行給定的範圍 （動作或控制器）。</span><span class="sxs-lookup"><span data-stu-id="605aa-236">Override filters specify a set of filter types that should not be run for a given scope (action or controller).</span></span> <span data-ttu-id="605aa-237">這可讓您設定篩選器，全域套用，但無法套用至特定動作或控制器中排除某些全域篩選器。</span><span class="sxs-lookup"><span data-stu-id="605aa-237">This allows you to configure filters that apply globally but then exclude certain global filters from applying to specific actions or controllers.</span></span>

### <a name="attribute-routing"></a><span data-ttu-id="605aa-238">路由屬性</span><span class="sxs-lookup"><span data-stu-id="605aa-238">Attribute routing</span></span>

<span data-ttu-id="605aa-239">ASP.NET MVC 現在支援路由屬性，這點受惠 Tim McCall，作者比重[http://attributerouting.net](http://attributerouting.net)。</span><span class="sxs-lookup"><span data-stu-id="605aa-239">ASP.NET MVC now supports attribute routing, thanks to a contribution by Tim McCall, the author of [http://attributerouting.net](http://attributerouting.net).</span></span> <span data-ttu-id="605aa-240">路由屬性中，您可以指定您的路由加上附註您的動作與控制器。</span><span class="sxs-lookup"><span data-stu-id="605aa-240">With attribute routing you can specify your routes by annotating your actions and controllers.</span></span>

<a id="TOC11"></a>
## <a name="aspnet-web-api-2"></a><span data-ttu-id="605aa-241">ASP.NET Web API 2</span><span class="sxs-lookup"><span data-stu-id="605aa-241">ASP.NET Web API 2</span></span>

### <a name="attribute-routing"></a><span data-ttu-id="605aa-242">路由屬性</span><span class="sxs-lookup"><span data-stu-id="605aa-242">Attribute routing</span></span>

<span data-ttu-id="605aa-243">ASP.NET Web API 現在支援路由屬性，這點受惠 Tim McCall，作者比重[http://attributerouting.net](http://attributerouting.net)。</span><span class="sxs-lookup"><span data-stu-id="605aa-243">ASP.NET Web API now supports attribute routing, thanks to a contribution by Tim McCall, the author of [http://attributerouting.net](http://attributerouting.net).</span></span> <span data-ttu-id="605aa-244">屬由路由中，您可以指定您的 Web API 路由加上附註您的動作和控制站，像這樣：</span><span class="sxs-lookup"><span data-stu-id="605aa-244">With attribute routing you can specify your Web API routes by annotating your actions and controllers like this:</span></span>

[!code-csharp[Main](release-notes/samples/sample1.cs)]

<span data-ttu-id="605aa-245">路由屬性讓您更充分掌控 Uri 在您的 web API。</span><span class="sxs-lookup"><span data-stu-id="605aa-245">Attribute routing gives you more control over the URIs in your web API.</span></span> <span data-ttu-id="605aa-246">例如，您可以輕鬆地定義資源階層，使用單一的 API 控制器：</span><span class="sxs-lookup"><span data-stu-id="605aa-246">For example, you can easily define a resource hierarchy using a single API controller:</span></span>

[!code-csharp[Main](release-notes/samples/sample2.cs)]

<span data-ttu-id="605aa-247">屬性路由也提供方便的語法指定選擇性參數、 預設值和路由條件約束：</span><span class="sxs-lookup"><span data-stu-id="605aa-247">Attribute routing also provides a convenient syntax for specifying optional parameters, default values, and route constraints:</span></span>

[!code-csharp[Main](release-notes/samples/sample3.cs)]

<span data-ttu-id="605aa-248">如需路由屬性的詳細資訊，請參閱[屬性路由中 Web API 2](../../../web-api/overview/web-api-routing-and-actions/attribute-routing-in-web-api-2.md)。</span><span class="sxs-lookup"><span data-stu-id="605aa-248">For more information about attribute routing, see [Attribute Routing in Web API 2](../../../web-api/overview/web-api-routing-and-actions/attribute-routing-in-web-api-2.md).</span></span>

### <a name="oauth-20"></a><span data-ttu-id="605aa-249">OAuth 2.0</span><span class="sxs-lookup"><span data-stu-id="605aa-249">OAuth 2.0</span></span>

<span data-ttu-id="605aa-250">Web API 和單一頁面應用程式專案範本現在支援使用 OAuth 2.0 授權。</span><span class="sxs-lookup"><span data-stu-id="605aa-250">The Web API and Single Page Application project templates now support authorization using OAuth 2.0.</span></span> <span data-ttu-id="605aa-251">OAuth 2.0 是一種架構用戶端存取受保護資源的授權。</span><span class="sxs-lookup"><span data-stu-id="605aa-251">OAuth 2.0 is a framework for authorizing client access to protected resources.</span></span> <span data-ttu-id="605aa-252">這也適用於各種不同的用戶端包括瀏覽器和行動裝置。</span><span class="sxs-lookup"><span data-stu-id="605aa-252">It works for a variety of clients including browsers and mobile devices.</span></span>

<span data-ttu-id="605aa-253">OAuth 2.0 的支援根據新安全性中介軟體提供由 Microsoft OWIN 元件承載驗證和執行授權伺服器角色。</span><span class="sxs-lookup"><span data-stu-id="605aa-253">Support for OAuth 2.0 is based on new security middleware provided by the Microsoft OWIN Components for bearer authentication and implementing the authorization server role.</span></span> <span data-ttu-id="605aa-254">或者，您可以使用組織的授權伺服器，例如 Azure Active Directory 或 Windows Server 2012 R2 中的 ADFS 進行授權用戶端。</span><span class="sxs-lookup"><span data-stu-id="605aa-254">Alternatively, clients can be authorized using an organizational authorization server, such as Azure Active Directory or ADFS in Windows Server 2012 R2.</span></span>

### <a name="odata-improvements"></a><span data-ttu-id="605aa-255">OData 增強功能</span><span class="sxs-lookup"><span data-stu-id="605aa-255">OData Improvements</span></span>

<span data-ttu-id="605aa-256">**展開 支援 $select，$，$batch 和 $value**</span><span class="sxs-lookup"><span data-stu-id="605aa-256">**Support for $select, $expand, $batch, and $value**</span></span>

<span data-ttu-id="605aa-257">ASP.NET Web API OData 現在會有完整支援 $select、 $expand、 和 $value。</span><span class="sxs-lookup"><span data-stu-id="605aa-257">ASP.NET Web API OData now has full support for $select, $expand, and $value.</span></span> <span data-ttu-id="605aa-258">您也可以使用 $batch 批次和變更集的處理要求。</span><span class="sxs-lookup"><span data-stu-id="605aa-258">You can also use $batch for request batching and processing of change sets.</span></span>

<span data-ttu-id="605aa-259">$Select 及 $expand 選項可讓您變更 從 OData 端點會傳回資料的外觀。</span><span class="sxs-lookup"><span data-stu-id="605aa-259">The $select and $expand options let you change the shape of the data that is returned from an OData endpoint.</span></span> <span data-ttu-id="605aa-260">如需詳細資訊，請參閱[簡介 $select 和 $expand Web API OData 中的支援](../../../web-api/overview/odata-support-in-aspnet-web-api/using-select-expand-and-value.md)。</span><span class="sxs-lookup"><span data-stu-id="605aa-260">For more information, see [Introducing $select and $expand support in Web API OData](../../../web-api/overview/odata-support-in-aspnet-web-api/using-select-expand-and-value.md).</span></span>

<span data-ttu-id="605aa-261">**改善擴充性**</span><span class="sxs-lookup"><span data-stu-id="605aa-261">**Improved extensibility**</span></span>

<span data-ttu-id="605aa-262">OData 格式器現在是可擴充的。</span><span class="sxs-lookup"><span data-stu-id="605aa-262">The OData formatters are now extensible.</span></span> <span data-ttu-id="605aa-263">您可以加入 Atom 項目中繼資料、 支援具名資料流與媒體連結項目、 加入執行個體註解，並自訂連結的產生方式。</span><span class="sxs-lookup"><span data-stu-id="605aa-263">You can add Atom entry metadata, support named stream and media link entries, add instance annotations, and customize how links are generated.</span></span>

<span data-ttu-id="605aa-264">**無類型的支援**</span><span class="sxs-lookup"><span data-stu-id="605aa-264">**Type-less support**</span></span>

<span data-ttu-id="605aa-265">您現在可以建置 OData 服務，而不需要定義實體類型的 CLR 型別。</span><span class="sxs-lookup"><span data-stu-id="605aa-265">You can now build OData services without needing to define CLR types for your entity types.</span></span> <span data-ttu-id="605aa-266">相反地，OData 控制器可以接受或傳回執行個體**IEdmObject**、 哪些是序列化/還原序列化的 OData 格式器。</span><span class="sxs-lookup"><span data-stu-id="605aa-266">Instead, your OData controllers can take or return instances of **IEdmObject**, which are the OData formatters serialize/deserialize.</span></span>

<span data-ttu-id="605aa-267">**重複使用現有的模型**</span><span class="sxs-lookup"><span data-stu-id="605aa-267">**Reuse an existing model**</span></span>

<span data-ttu-id="605aa-268">如果您已經有現有的實體資料模型 (EDM)，您可以立即重複使用它直接管理，而不必建立新的。</span><span class="sxs-lookup"><span data-stu-id="605aa-268">If you already have an existing entity data model (EDM), you can now reuse it directly, instead of having to build a new one.</span></span> <span data-ttu-id="605aa-269">例如，如果您使用 Entity Framework，您可以使用 EF 為您建立 EDM。</span><span class="sxs-lookup"><span data-stu-id="605aa-269">For example, if you are using Entity Framework, you can use the EDM that EF builds for you.</span></span>

### <a name="request-batching"></a><span data-ttu-id="605aa-270">要求批次處理</span><span class="sxs-lookup"><span data-stu-id="605aa-270">Request Batching</span></span>

<span data-ttu-id="605aa-271">批次處理要求結合成單一的 HTTP POST 要求，以減少網路流量並提供更順暢，較多對話的使用者介面的多個作業。</span><span class="sxs-lookup"><span data-stu-id="605aa-271">Request batching combines multiple operations into a single HTTP POST request, to reduce network traffic and provide a smoother, less chatty user interface.</span></span> <span data-ttu-id="605aa-272">ASP.NET Web API 現在支援數種策略的批次要求：</span><span class="sxs-lookup"><span data-stu-id="605aa-272">ASP.NET Web API now supports several strategies for request batching:</span></span>

- <span data-ttu-id="605aa-273">使用 OData 服務的 $batch 端點。</span><span class="sxs-lookup"><span data-stu-id="605aa-273">Use the $batch endpoint of an OData service.</span></span>
- <span data-ttu-id="605aa-274">封裝的多個要求結合為單一的 MIME 多組件的要求。</span><span class="sxs-lookup"><span data-stu-id="605aa-274">Package multiple requests into a single MIME multipart request.</span></span>
- <span data-ttu-id="605aa-275">使用自訂的批次處理格式。</span><span class="sxs-lookup"><span data-stu-id="605aa-275">Use a custom batching format.</span></span>

<span data-ttu-id="605aa-276">若要啟用批次處理的要求，只需新增與批次的處理常式路由到 Web API 組態：</span><span class="sxs-lookup"><span data-stu-id="605aa-276">To enable request batching, simply add a route with a batching handler to your Web API configuration:</span></span>

[!code-csharp[Main](release-notes/samples/sample4.cs)]

<span data-ttu-id="605aa-277">您也可以控制是否要求或循序或依任何順序執行。</span><span class="sxs-lookup"><span data-stu-id="605aa-277">You can also control whether requests or executed sequentially or in any order.</span></span>

### <a name="portable-aspnet-web-api-client"></a><span data-ttu-id="605aa-278">可攜式的 ASP.NET Web API 的用戶端</span><span class="sxs-lookup"><span data-stu-id="605aa-278">Portable ASP.NET Web API Client</span></span>

<span data-ttu-id="605aa-279">您現在可以使用 ASP.NET Web API 的用戶端建立可攜式類別庫可透過 Windows 市集和 Windows Phone 8 應用程式。</span><span class="sxs-lookup"><span data-stu-id="605aa-279">You can now use the ASP.NET Web API Client to create portable class libraries that work across your Windows Store and Windows Phone 8 applications.</span></span> <span data-ttu-id="605aa-280">您也可以建立可攜式格式器會在用戶端和伺服器之間共用。</span><span class="sxs-lookup"><span data-stu-id="605aa-280">You can also create portable formatters that can be shared across client and server.</span></span>

### <a name="improved-testability"></a><span data-ttu-id="605aa-281">改良的測試能力</span><span class="sxs-lookup"><span data-stu-id="605aa-281">Improved Testability</span></span>

<span data-ttu-id="605aa-282">Web API 2 可讓它更容易單元測試您的 API 控制器。</span><span class="sxs-lookup"><span data-stu-id="605aa-282">Web API 2 makes it much easier to unit test your API controllers.</span></span> <span data-ttu-id="605aa-283">只會初始化您的應用程式開發介面控制站與您的要求訊息的組態，並接著呼叫您要測試的動作方法。</span><span class="sxs-lookup"><span data-stu-id="605aa-283">Just instantiate your API controller with your request message and configuration, and then call the action method you wish to test.</span></span> <span data-ttu-id="605aa-284">所以也可以輕鬆地模擬**UrlHelper**類別，適用於執行連結產生的動作方法。</span><span class="sxs-lookup"><span data-stu-id="605aa-284">It is also easy to mock the **UrlHelper** class, for action methods that perform link generation.</span></span>

### <a name="ihttpactionresult"></a><span data-ttu-id="605aa-285">IHttpActionResult</span><span class="sxs-lookup"><span data-stu-id="605aa-285">IHttpActionResult</span></span>

<span data-ttu-id="605aa-286">您現在可以實作 IHttpActionResult 來封裝您的 Web API 的動作方法的結果。</span><span class="sxs-lookup"><span data-stu-id="605aa-286">You can now implement IHttpActionResult to encapsulate the result of your Web API action methods.</span></span> <span data-ttu-id="605aa-287">從 Web API 的動作方法傳回 IHttpActionResult 執行 ASP.NET Web API 執行階段，以產生結果的回應訊息。</span><span class="sxs-lookup"><span data-stu-id="605aa-287">An IHttpActionResult returned from a Web API action method is executed by the ASP.NET Web API runtime to produce the resultant response message.</span></span> <span data-ttu-id="605aa-288">可傳回 IHttpActionResult 從任何 Web 應用程式開發介面 動作，以簡化單元測試的 Web 應用程式開發介面實作。</span><span class="sxs-lookup"><span data-stu-id="605aa-288">An IHttpActionResult can be returned from any Web API action to simplify unit testing of your Web API implementation.</span></span> <span data-ttu-id="605aa-289">為了方便起見 IHttpActionResult 實作 (implementation) 的數字會提供現成的包括傳回特定的狀態碼的結果，格式化內容或內容交涉的回應。</span><span class="sxs-lookup"><span data-stu-id="605aa-289">For convenience a number of IHttpActionResult implementations are provided out of the box including results for returning specific status codes, formatted content or content-negotiated responses.</span></span>

### <a name="httprequestcontext"></a><span data-ttu-id="605aa-290">HttpRequestContext</span><span class="sxs-lookup"><span data-stu-id="605aa-290">HttpRequestContext</span></span>

<span data-ttu-id="605aa-291">新**HttpRequestContext**會追蹤任何繫結至要求，但沒有立即可用從要求的狀態。</span><span class="sxs-lookup"><span data-stu-id="605aa-291">The new **HttpRequestContext** tracks any state that is tied to the request but is not immediately available from the request.</span></span> <span data-ttu-id="605aa-292">例如，您可以使用**HttpRequestContext**取得路由資料的要求，用戶端憑證，與關聯的主體**UrlHelper**和虛擬路徑根。</span><span class="sxs-lookup"><span data-stu-id="605aa-292">For example, you can use the **HttpRequestContext** to get route data, the principal associated with the request, the client certificate, the **UrlHelper** and the virtual path root.</span></span> <span data-ttu-id="605aa-293">您可以輕鬆地建立**HttpRequestContext**進行單元測試。</span><span class="sxs-lookup"><span data-stu-id="605aa-293">You can easily create an **HttpRequestContext** for unit testing purposes.</span></span>

<span data-ttu-id="605aa-294">因為要求主體流動的要求，而不是依賴**Thread.CurrentPrincipal**，在 Web API 管線時，就可存留期中的要求主體。</span><span class="sxs-lookup"><span data-stu-id="605aa-294">Because the principal for the request is flowed with the request instead of relying on **Thread.CurrentPrincipal**, the principal is now available throughout the lifetime of the request while it is in the Web API pipeline.</span></span>

### <a name="cors"></a><span data-ttu-id="605aa-295">CORS</span><span class="sxs-lookup"><span data-stu-id="605aa-295">CORS</span></span>

<span data-ttu-id="605aa-296">這點受惠 Brock Allen 從另一個絕佳的比重，ASP.NET 現在完全支援跨原始要求共用 (CORS)。</span><span class="sxs-lookup"><span data-stu-id="605aa-296">Thanks to another great contribution from Brock Allen, ASP.NET now fully supports Cross Origin Request Sharing (CORS).</span></span>

<span data-ttu-id="605aa-297">瀏覽器安全性防止網頁 AJAX 要求到另一個網域。</span><span class="sxs-lookup"><span data-stu-id="605aa-297">Browser security prevents a web page from making AJAX requests to another domain.</span></span> <span data-ttu-id="605aa-298">[CORS](http://www.w3.org/TR/cors/)是 W3C 標準，可放寬的相同來源原則的伺服器。</span><span class="sxs-lookup"><span data-stu-id="605aa-298">[CORS](http://www.w3.org/TR/cors/) is a W3C standard that allows a server to relax the same-origin policy.</span></span> <span data-ttu-id="605aa-299">使用 CORS，伺服器可以明確地允許某些跨原始要求時拒絕其他人。</span><span class="sxs-lookup"><span data-stu-id="605aa-299">Using CORS, a server can explicitly allow some cross-origin requests while rejecting others.</span></span>

<span data-ttu-id="605aa-300">Web API 2 現在支援 CORS，包括自動處理的預檢要求。</span><span class="sxs-lookup"><span data-stu-id="605aa-300">Web API 2 now supports CORS, including automatic handling of preflight requests.</span></span> <span data-ttu-id="605aa-301">如需詳細資訊，請參閱[啟用 ASP.NET Web API 中的跨原始要求](../../../web-api/overview/security/enabling-cross-origin-requests-in-web-api.md)。</span><span class="sxs-lookup"><span data-stu-id="605aa-301">For more information, see [Enabling Cross-Origin Requests in ASP.NET Web API](../../../web-api/overview/security/enabling-cross-origin-requests-in-web-api.md).</span></span>

### <a name="authentication-filters"></a><span data-ttu-id="605aa-302">驗證篩選條件</span><span class="sxs-lookup"><span data-stu-id="605aa-302">Authentication Filters</span></span>

<span data-ttu-id="605aa-303">驗證篩選條件是一種新的 ASP.NET Web API 管線中的授權篩選條件之前執行，並允許您指定驗證邏輯每個動作，ASP.NET Web API 中的篩選每個控制器，或全域的所有控制站。</span><span class="sxs-lookup"><span data-stu-id="605aa-303">Authentication filters are a new kind of filter in ASP.NET Web API that run prior to authorization filters in the ASP.NET Web API pipeline and allow you to specify authentication logic per-action, per-controller, or globally for all controllers.</span></span> <span data-ttu-id="605aa-304">驗證篩選條件處理要求中的認證，並提供對應的主體。</span><span class="sxs-lookup"><span data-stu-id="605aa-304">Authentication filters process credentials in the request and provide a corresponding principal.</span></span> <span data-ttu-id="605aa-305">驗證篩選條件也可以將驗證挑戰回應未經授權的要求。</span><span class="sxs-lookup"><span data-stu-id="605aa-305">Authentication filters can also add authentication challenges in response to unauthorized requests.</span></span>

### <a name="filter-overrides"></a><span data-ttu-id="605aa-306">篩選條件覆寫</span><span class="sxs-lookup"><span data-stu-id="605aa-306">Filter Overrides</span></span>

<span data-ttu-id="605aa-307">您現在可以覆寫的篩選會套用至指定的動作方法或控制器，藉由指定覆寫篩選條件。</span><span class="sxs-lookup"><span data-stu-id="605aa-307">You can now override which filters apply to a given action method or controller, by specifying an override filter.</span></span> <span data-ttu-id="605aa-308">覆寫篩選條件會指定一組不應該執行給定的範圍 （動作或控制器） 的篩選器型別。</span><span class="sxs-lookup"><span data-stu-id="605aa-308">Override filters specify a set of filter types that should not run for a given scope (action or controller).</span></span> <span data-ttu-id="605aa-309">這可讓您將加入全域的篩選，但是再排除某些特定的動作或控制器。</span><span class="sxs-lookup"><span data-stu-id="605aa-309">This allows you to add global filters, but then exclude some from specific actions or controllers.</span></span>

### <a name="owin-integration"></a><span data-ttu-id="605aa-310">OWIN 整合</span><span class="sxs-lookup"><span data-stu-id="605aa-310">OWIN Integration</span></span>

<span data-ttu-id="605aa-311">ASP.NET Web API 現在完全支援 OWIN，並可以在任何 OWIN 功能的主機上執行。</span><span class="sxs-lookup"><span data-stu-id="605aa-311">ASP.NET Web API now fully supports OWIN and can be run on any OWIN capable host.</span></span> <span data-ttu-id="605aa-312">另外還包括**HostAuthenticationFilter**提供與 OWIN 驗證系統的整合。</span><span class="sxs-lookup"><span data-stu-id="605aa-312">Also included is a **HostAuthenticationFilter** that provides integration with the OWIN authentication system.</span></span>

<span data-ttu-id="605aa-313">與 OWIN 整合，您可以連同其他 OWIN 中介軟體，例如 SignalR 自己處理序中自我裝載 Web 應用程式開發介面。</span><span class="sxs-lookup"><span data-stu-id="605aa-313">With OWIN integration, you can self-host Web API in your own process alongside other OWIN middleware, such as SignalR.</span></span> <span data-ttu-id="605aa-314">如需詳細資訊，請參閱[Self-Host ASP.NET Web 應用程式開發介面使用 OWIN](../../../signalr/overview/deployment/tutorial-signalr-self-host.md)。</span><span class="sxs-lookup"><span data-stu-id="605aa-314">For more information, see [Use OWIN to Self-Host ASP.NET Web API](../../../signalr/overview/deployment/tutorial-signalr-self-host.md).</span></span>

<a id="TOC13"></a>
## <a name="aspnet-signalr-20"></a><span data-ttu-id="605aa-315">ASP.NET SignalR 2.0</span><span class="sxs-lookup"><span data-stu-id="605aa-315">ASP.NET SignalR 2.0</span></span>

<span data-ttu-id="605aa-316">下列章節說明 SignalR 2.0 的功能。</span><span class="sxs-lookup"><span data-stu-id="605aa-316">The following sections describe features of SignalR 2.0.</span></span>

- [<span data-ttu-id="605aa-317">在 OWIN 上建置</span><span class="sxs-lookup"><span data-stu-id="605aa-317">Built on OWIN</span></span>](#builtonowin)
- [<span data-ttu-id="605aa-318">MapHubs 和 MapConnection 現在是 MapSignalR</span><span class="sxs-lookup"><span data-stu-id="605aa-318">MapHubs and MapConnection are now MapSignalR</span></span>](#MapSignalR)
- [<span data-ttu-id="605aa-319">跨網域支援</span><span class="sxs-lookup"><span data-stu-id="605aa-319">Cross-Domain Support</span></span>](#crossdomain)
- [<span data-ttu-id="605aa-320">iOS 和 Android 支援透過 MonoTouch 和 MonoDroid</span><span class="sxs-lookup"><span data-stu-id="605aa-320">iOS and Android support via MonoTouch and MonoDroid</span></span>](#mobile)
- [<span data-ttu-id="605aa-321">可攜式.NET 用戶端</span><span class="sxs-lookup"><span data-stu-id="605aa-321">Portable .NET Client</span></span>](#portable)
- [<span data-ttu-id="605aa-322">新的自我裝載的封裝</span><span class="sxs-lookup"><span data-stu-id="605aa-322">New Self-Host Package</span></span>](#selfhost)
- [<span data-ttu-id="605aa-323">回溯相容的伺服器支援</span><span class="sxs-lookup"><span data-stu-id="605aa-323">Backward-compatible server support</span></span>](#backwardcompat)
- [<span data-ttu-id="605aa-324">移除.NET 4.0 的伺服器支援</span><span class="sxs-lookup"><span data-stu-id="605aa-324">Removed server support for .NET 4.0</span></span>](#remove40)
- [<span data-ttu-id="605aa-325">將訊息傳送到用戶端和群組的清單</span><span class="sxs-lookup"><span data-stu-id="605aa-325">Sending a message to a list of clients and groups</span></span>](#messagelist)
- [<span data-ttu-id="605aa-326">傳送訊息給特定使用者</span><span class="sxs-lookup"><span data-stu-id="605aa-326">Sending a message to a specific user</span></span>](#sendtouser)
- [<span data-ttu-id="605aa-327">更好的錯誤處理支援</span><span class="sxs-lookup"><span data-stu-id="605aa-327">Better error handling support</span></span>](#errorhandling)
- [<span data-ttu-id="605aa-328">更容易的單元測試中樞</span><span class="sxs-lookup"><span data-stu-id="605aa-328">Easier unit testing of hubs</span></span>](#unittesting)
- [<span data-ttu-id="605aa-329">JavaScript 錯誤處理</span><span class="sxs-lookup"><span data-stu-id="605aa-329">JavaScript error handling</span></span>](#javascripterror)

<span data-ttu-id="605aa-330">如需如何將現有的 1.x 專案升級至 SignalR 2.0 的範例，請參閱[升級 SignalR 1.x 專案](../../../signalr/overview/releases/upgrading-signalr-1x-projects-to-20.md)。</span><span class="sxs-lookup"><span data-stu-id="605aa-330">For an example of how to upgrade an existing 1.x project to SignalR 2.0, see [Upgrading a SignalR 1.x Project](../../../signalr/overview/releases/upgrading-signalr-1x-projects-to-20.md).</span></span>

<a id="builtonowin"></a>
### <a name="built-on-owin"></a><span data-ttu-id="605aa-331">在 OWIN 上建置</span><span class="sxs-lookup"><span data-stu-id="605aa-331">Built on OWIN</span></span>

<span data-ttu-id="605aa-332">完全在建置 SignalR 2.0 [OWIN （開啟 Web 介面 for.NET）](http://owin.org/)。</span><span class="sxs-lookup"><span data-stu-id="605aa-332">SignalR 2.0 is built completely on [OWIN (the Open Web Interface for .NET)](http://owin.org/).</span></span> <span data-ttu-id="605aa-333">這項變更讓 web 主控和自我裝載 SignalR 應用程式之間更為一致 SignalR 的安裝程序，但也有必要的應用程式開發介面變更數目。</span><span class="sxs-lookup"><span data-stu-id="605aa-333">This change makes the setup process for SignalR much more consistent between web-hosted and self-hosted SignalR applications, but has also required a number of API changes.</span></span>

<a id="MapSignalR"></a>

### <a name="maphubs-and-mapconnection-are-now-mapsignalr"></a><span data-ttu-id="605aa-334">MapHubs 和 MapConnection 現在是 MapSignalR</span><span class="sxs-lookup"><span data-stu-id="605aa-334">MapHubs and MapConnection are now MapSignalR</span></span>

<span data-ttu-id="605aa-335">為了與 OWIN 標準相容，這些方法已重新命名為`MapSignalR`。</span><span class="sxs-lookup"><span data-stu-id="605aa-335">For compatibility with OWIN standards, these methods have been renamed to `MapSignalR`.</span></span> <span data-ttu-id="605aa-336">`MapSignalR`呼叫沒有參數會對應所有中樞 (做為`MapHubs`中版本 1.x); 若要將都對應個別**PersistentConnection**物件，指定連接類型為型別參數，以及做為連線的 URL 擴充功能第一個引數。</span><span class="sxs-lookup"><span data-stu-id="605aa-336">`MapSignalR` called without parameters will map all hubs (as `MapHubs` does in version 1.x); to map individual **PersistentConnection** objects, specify the connection type as the type parameter, and the URL extension for the connection as the first argument.</span></span>

<span data-ttu-id="605aa-337">`MapSignalR` Owin 啟動類別中呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="605aa-337">The `MapSignalR` method is called in an Owin startup class.</span></span> <span data-ttu-id="605aa-338">Visual Studio 2013 包含 Owin 啟動類別; 事件類別的新範本若要使用此範本，執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="605aa-338">Visual Studio 2013 contains a new template for an Owin startup class; to use this template, do the following:</span></span>

1. <span data-ttu-id="605aa-339">以滑鼠右鍵按一下專案</span><span class="sxs-lookup"><span data-stu-id="605aa-339">Right-click on the project</span></span>
2. <span data-ttu-id="605aa-340">選取**新增**，**新項目...**</span><span class="sxs-lookup"><span data-stu-id="605aa-340">Select **Add**, **New Item...**</span></span>
3. <span data-ttu-id="605aa-341">選取**Owin 啟動 「 類別**。</span><span class="sxs-lookup"><span data-stu-id="605aa-341">Select **Owin Startup class**.</span></span> <span data-ttu-id="605aa-342">將新類別**Startup.cs**。</span><span class="sxs-lookup"><span data-stu-id="605aa-342">Name the new class **Startup.cs**.</span></span>

<span data-ttu-id="605aa-343">在**Web 應用程式，** Owin 啟動類別包含`MapSignalR`方法接著會新增至 Owin 的啟動程序使用的項目中的應用程式設定節點的 Web.Config 檔案中，如下所示。</span><span class="sxs-lookup"><span data-stu-id="605aa-343">In a **Web application,** the Owin startup class containing the `MapSignalR` method is then added to Owin's startup process using an entry in the application settings node of the Web.Config file, as shown below.</span></span>

<span data-ttu-id="605aa-344">在**自我裝載應用程式**，啟動類別會傳遞做為型別參數的`WebApp.Start`方法。</span><span class="sxs-lookup"><span data-stu-id="605aa-344">In a **Self-hosted application**, the Startup class is passed as the type parameter of the `WebApp.Start` method.</span></span>

<span data-ttu-id="605aa-345">**對應集線器與 SignalR 連線 1.x （從 web 應用程式中的全域應用程式檔案）：**</span><span class="sxs-lookup"><span data-stu-id="605aa-345">**Mapping hubs and connections in SignalR 1.x (from the global application file in a web application):**</span></span> 

[!code-csharp[Main](release-notes/samples/sample5.cs)]

<span data-ttu-id="605aa-346">**對應集線器與 SignalR 2.0 （從 Owin 啟動 「 類別檔案） 中的連線：**</span><span class="sxs-lookup"><span data-stu-id="605aa-346">**Mapping hubs and connections in SignalR 2.0 (from an Owin Startup class file):**</span></span> 

[!code-csharp[Main](release-notes/samples/sample6.cs)]

<span data-ttu-id="605aa-347">在**自我裝載應用程式**，啟動類別會當做型別參數傳遞`WebApp.Start`方法，如下所示。</span><span class="sxs-lookup"><span data-stu-id="605aa-347">In a **Self-hosted application**, the Startup class is passed as the type parameter for the `WebApp.Start` method, as shown below.</span></span>

[!code-csharp[Main](release-notes/samples/sample7.cs)]

<a id="crossdomain"></a>

### <a name="cross-domain-support"></a><span data-ttu-id="605aa-348">跨網域支援</span><span class="sxs-lookup"><span data-stu-id="605aa-348">Cross-Domain Support</span></span>

<span data-ttu-id="605aa-349">SignalR 1.x，跨網域要求由單一 EnableCrossDomain 中的旗標。</span><span class="sxs-lookup"><span data-stu-id="605aa-349">In SignalR 1.x, cross domain requests were controlled by a single EnableCrossDomain flag.</span></span> <span data-ttu-id="605aa-350">這個旗標控制 JSONP 及 CORS 要求。</span><span class="sxs-lookup"><span data-stu-id="605aa-350">This flag controlled both JSONP and CORS requests.</span></span> <span data-ttu-id="605aa-351">所有的 CORS 支援較大的彈性，已經移除了 SignalR 的伺服器元件 （JavaScript lients 仍然使用 CORS 通常如果它偵測到瀏覽器支援它），而且新的 OWIN 中介軟體進行可用來支援這些案例。</span><span class="sxs-lookup"><span data-stu-id="605aa-351">For greater flexibility, all CORS support has been removed from the server component of SignalR (JavaScript lients still use CORS normally if it is detected that the browser supports it), and new OWIN middleware has been made available to support these scenarios.</span></span>

<span data-ttu-id="605aa-352">在 SignalR 2.0 中，如果 JSONP 才能在用戶端 （支援跨網域要求中舊的瀏覽器），它必須明確啟用藉由設定`EnableJSONP`上`HubConfiguration`物件`true`，如下所示。</span><span class="sxs-lookup"><span data-stu-id="605aa-352">In SignalR 2.0, If JSONP is required on the client (to support cross-domain requests in older browsers), it will need to be enabled explicitly by setting `EnableJSONP` on the `HubConfiguration` object to `true`, as shown below.</span></span> <span data-ttu-id="605aa-353">JSONP 已停用根據預設，因為它比 CORS 較不安全。</span><span class="sxs-lookup"><span data-stu-id="605aa-353">JSONP is disabled by default, as it is less secure than CORS.</span></span>

<span data-ttu-id="605aa-354">若要加入新的 CORS 中介軟體 SignalR 2.0 中，加入`Microsoft.Owin.Cors`至您的專案，並呼叫的程式庫`UseCors`之前 SignalR 中介軟體下, 一節中所示。</span><span class="sxs-lookup"><span data-stu-id="605aa-354">To add the new CORS middleware in SignalR 2.0, add the `Microsoft.Owin.Cors` library to your project, and call `UseCors` before your SignalR middleware, as shown in the section below.</span></span>

<span data-ttu-id="605aa-355">**專案中加入 Microsoft.Owin.Cors**： 若要安裝此程式庫，請在 Package Manager Console 中執行下列命令：</span><span class="sxs-lookup"><span data-stu-id="605aa-355">**Adding Microsoft.Owin.Cors to your project**: To install this library, run the following command in the Package Manager Console:</span></span>

[!code-powershell[Main](release-notes/samples/sample8.ps1)]

<span data-ttu-id="605aa-356">此命令將新增 2.0.0 封裝至您的專案版本。</span><span class="sxs-lookup"><span data-stu-id="605aa-356">This command will add the 2.0.0 version of the package to your project.</span></span>

<span data-ttu-id="605aa-357">**呼叫 UseCors**</span><span class="sxs-lookup"><span data-stu-id="605aa-357">**Calling UseCors**</span></span>

<span data-ttu-id="605aa-358">下列程式碼片段示範如何實作 SignalR 中跨網域連線 1.x 和 2.0 版。</span><span class="sxs-lookup"><span data-stu-id="605aa-358">The following code snippets demonstrate how to implement cross-domain connections in SignalR 1.x and 2.0.</span></span>

<span data-ttu-id="605aa-359">**實作 SignalR 中跨網域要求 1.x （從全域應用程式檔案）**</span><span class="sxs-lookup"><span data-stu-id="605aa-359">**Implementing cross-domain requests in SignalR 1.x (from the global application file)**</span></span>

[!code-csharp[Main](release-notes/samples/sample9.cs)]

<span data-ttu-id="605aa-360">**實作 SignalR 2.0 （從 C# 程式碼檔案） 中的跨網域要求**</span><span class="sxs-lookup"><span data-stu-id="605aa-360">**Implementing cross-domain requests in SignalR 2.0 (from a C# code file)**</span></span>

<span data-ttu-id="605aa-361">下列程式碼會示範如何啟用 CORS 或 JSONP SignalR 2.0 專案中。</span><span class="sxs-lookup"><span data-stu-id="605aa-361">The following code demonstrates how to enable CORS or JSONP in a SignalR 2.0 project.</span></span> <span data-ttu-id="605aa-362">這個程式碼範例會使用`Map`和`RunSignalR`而不是`MapSignalR`，如此一來，CORS 中介軟體執行只會針對需要 CORS 支援 SignalR 要求 (而不會針對在指定的路徑上的所有流量`MapSignalR`。)`Map`也可以用於任何其他中介軟體，必須執行特定的 URL 前置詞，而不是整個應用程式。</span><span class="sxs-lookup"><span data-stu-id="605aa-362">This code sample uses `Map` and `RunSignalR` instead of `MapSignalR`, so that the CORS middleware runs only for the SignalR requests that require CORS support (rather than for all traffic at the path specified in `MapSignalR`.) `Map` can also be used for any other middleware that needs to run for a specific URL prefix, rather than for the entire application.</span></span>

[!code-csharp[Main](release-notes/samples/sample10.cs)]

<a id="mobile"></a>

### <a name="ios-and-android-support-via-monotouch-and-monodroid"></a><span data-ttu-id="605aa-363">iOS 和 Android 支援透過 MonoTouch 和 MonoDroid</span><span class="sxs-lookup"><span data-stu-id="605aa-363">iOS and Android support via MonoTouch and MonoDroid</span></span>

<span data-ttu-id="605aa-364">已新增支援適用於 iOS 和 Android 的用戶端使用 MonoTouch 和 MonoDroid 元件從[Xamarin 程式庫](https://xamarin.com/)。</span><span class="sxs-lookup"><span data-stu-id="605aa-364">Support has been added for iOS and Android clients using MonoTouch and MonoDroid components from the [Xamarin library](https://xamarin.com/).</span></span> <span data-ttu-id="605aa-365">如需使用方式的詳細資訊，請參閱[使用 Xamarin 元件](https://github.com/SignalR/SignalR/wiki/Building-Mono.Mobile.sln)。</span><span class="sxs-lookup"><span data-stu-id="605aa-365">For more information on how to use them, see [Using Xamarin Components](https://github.com/SignalR/SignalR/wiki/Building-Mono.Mobile.sln).</span></span> <span data-ttu-id="605aa-366">這些元件可在[Xamarin 市集](https://store.xamarin.com/)SignalR RTW 發行時使用。</span><span class="sxs-lookup"><span data-stu-id="605aa-366">These components will be available in the [Xamarin Store](https://store.xamarin.com/) when the SignalR RTW release is available.</span></span>

<a id="portable"></a><span data-ttu-id="605aa-367"># # # 可攜式.NET 用戶端</span><span class="sxs-lookup"><span data-stu-id="605aa-367">### Portable .NET client</span></span>

<span data-ttu-id="605aa-368">以更好地簡化跨平台開發、 Silverlight、 WinRT 和 Windows Phone 用戶端已取代為單一可攜式.NET 用戶端支援下列平台：</span><span class="sxs-lookup"><span data-stu-id="605aa-368">To better facilitate cross-platform development, the Silverlight, WinRT and Windows Phone clients have been replaced with a single portable .NET client that supports the following platforms:</span></span>

- <span data-ttu-id="605aa-369">NET 4.5</span><span class="sxs-lookup"><span data-stu-id="605aa-369">NET 4.5</span></span>
- <span data-ttu-id="605aa-370">Silverlight 5</span><span class="sxs-lookup"><span data-stu-id="605aa-370">Silverlight 5</span></span>
- <span data-ttu-id="605aa-371">WinRT (Windows 市集應用程式的.NET)</span><span class="sxs-lookup"><span data-stu-id="605aa-371">WinRT (.NET for Windows Store Apps)</span></span>
- <span data-ttu-id="605aa-372">Windows Phone 8</span><span class="sxs-lookup"><span data-stu-id="605aa-372">Windows Phone 8</span></span>

<a id="selfhost"></a>

### <a name="new-self-host-package"></a><span data-ttu-id="605aa-373">新的自我裝載的封裝</span><span class="sxs-lookup"><span data-stu-id="605aa-373">New Self-Host Package</span></span>

<span data-ttu-id="605aa-374">現在是 NuGet 封裝來更輕鬆地開始使用 SignalR 自我裝載 （所裝載處理序中的 SignalR 應用程式或其他應用程式，而非裝載在網頁伺服器）。</span><span class="sxs-lookup"><span data-stu-id="605aa-374">There is now a NuGet package to make it easier to get started with SignalR Self-Host (SignalR applications that are hosted in a process or other application, rather than being hosted in a web server).</span></span> <span data-ttu-id="605aa-375">若要升級自我裝載所建置的專案與 SignalR 1.x 移除 Microsoft.AspNet.SignalR.Owin 封裝，並新增 Microsoft.AspNet.SignalR.SelfHost 封裝。</span><span class="sxs-lookup"><span data-stu-id="605aa-375">To upgrade a self-host project built with SignalR 1.x, remove the Microsoft.AspNet.SignalR.Owin package, and add the Microsoft.AspNet.SignalR.SelfHost package.</span></span> <span data-ttu-id="605aa-376">如需有關如何開始使用的自我裝載套件的詳細資訊，請參閱[教學課程： 自我裝載的 SignalR](../../../signalr/overview/deployment/tutorial-signalr-self-host.md)。</span><span class="sxs-lookup"><span data-stu-id="605aa-376">For more information on getting started with the self-host package, see [Tutorial: SignalR Self-Host](../../../signalr/overview/deployment/tutorial-signalr-self-host.md).</span></span>

<a id="backwardcompat"></a>

### <a name="backward-compatible-server-support"></a><span data-ttu-id="605aa-377">回溯相容的伺服器支援</span><span class="sxs-lookup"><span data-stu-id="605aa-377">Backward-compatible server support</span></span>

<span data-ttu-id="605aa-378">在舊版的 SignalR、 SignalR 封裝用於用戶端和伺服器必須是相同的版本。</span><span class="sxs-lookup"><span data-stu-id="605aa-378">In previous versions of SignalR, the versions of the SignalR package used in the client and the server needed to be identical.</span></span> <span data-ttu-id="605aa-379">為了支援大型用戶端應用程式會很難更新，SignalR 2.0 現在支援使用舊版用戶端較新的伺服器版本。</span><span class="sxs-lookup"><span data-stu-id="605aa-379">In order to support thick-client applications that would be difficult to update, SignalR 2.0 now supports using a newer server version with an older client.</span></span> <span data-ttu-id="605aa-380">**注意： SignalR 2.0 不支援與較新的用戶端所建置與較舊版本的伺服器。**</span><span class="sxs-lookup"><span data-stu-id="605aa-380">**Note: SignalR 2.0 does not support servers built with older versions with newer clients.**</span></span>

<a id="remove40"></a>

### <a name="removed-server-support-for-net-40"></a><span data-ttu-id="605aa-381">移除.NET 4.0 的伺服器支援</span><span class="sxs-lookup"><span data-stu-id="605aa-381">Removed server support for .NET 4.0</span></span>

<span data-ttu-id="605aa-382">SignalR 2.0 已卸除伺服器互通性與.NET 4.0 的支援。</span><span class="sxs-lookup"><span data-stu-id="605aa-382">SignalR 2.0 has dropped support for server interoperability with .NET 4.0.</span></span> <span data-ttu-id="605aa-383">與 SignalR 2.0 伺服器，必須使用.NET 4.5。</span><span class="sxs-lookup"><span data-stu-id="605aa-383">.NET 4.5 must be used with SignalR 2.0 servers.</span></span> <span data-ttu-id="605aa-384">仍有 SignalR 2.0 針對.NET 4.0 用戶端。</span><span class="sxs-lookup"><span data-stu-id="605aa-384">There is still a .NET 4.0 client for SignalR 2.0.</span></span>

<a id="messagelist"></a>

### <a name="sending-a-message-to-a-list-of-clients-and-groups"></a><span data-ttu-id="605aa-385">將訊息傳送到用戶端和群組的清單</span><span class="sxs-lookup"><span data-stu-id="605aa-385">Sending a message to a list of clients and groups</span></span>

<span data-ttu-id="605aa-386">在 SignalR 2.0 中，很可能傳送訊息使用的用戶端與群組識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="605aa-386">In SignalR 2.0, it's possible to send a message using a list of client and group IDs.</span></span> <span data-ttu-id="605aa-387">下列程式碼片段會示範如何執行這項操作。</span><span class="sxs-lookup"><span data-stu-id="605aa-387">The following code snippets demonstrate how to do this.</span></span>

<span data-ttu-id="605aa-388">**將訊息傳送到用戶端與使用 PersistentConnection 群組的清單**</span><span class="sxs-lookup"><span data-stu-id="605aa-388">**Sending a message to a list of clients and groups using PersistentConnection**</span></span>

[!code-csharp[Main](release-notes/samples/sample11.cs)]

<span data-ttu-id="605aa-389">**將訊息傳送到用戶端與使用中樞群組的清單**</span><span class="sxs-lookup"><span data-stu-id="605aa-389">**Sending a message to a list of clients and groups using Hubs**</span></span>

[!code-csharp[Main](release-notes/samples/sample12.cs)]

<a id="sendtouser"></a>

### <a name="sending-a-message-to-a-specific-user"></a><span data-ttu-id="605aa-390">傳送訊息給特定使用者</span><span class="sxs-lookup"><span data-stu-id="605aa-390">Sending a message to a specific user</span></span>

<span data-ttu-id="605aa-391">這項功能可讓使用者指定的使用者識別碼的是根據透過新的介面 IUserIdProvider IRequest:</span><span class="sxs-lookup"><span data-stu-id="605aa-391">This feature allows users to specify what the userId is based on an IRequest via a new interface IUserIdProvider:</span></span>

<span data-ttu-id="605aa-392">**IUserIdProvider 介面**</span><span class="sxs-lookup"><span data-stu-id="605aa-392">**The IUserIdProvider interface**</span></span>

[!code-csharp[Main](release-notes/samples/sample13.cs)]

<span data-ttu-id="605aa-393">依預設會有的實作會透過使用者的 IPrincipal.Identity.Name 的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="605aa-393">By default there will be an implementation that uses the user's IPrincipal.Identity.Name as the user name.</span></span>

<span data-ttu-id="605aa-394">在中樞，您可以將訊息傳送給這些使用者，透過新的 API:</span><span class="sxs-lookup"><span data-stu-id="605aa-394">In hubs, you'll be able to send messages to these users via a new API:</span></span>

<span data-ttu-id="605aa-395">**使用 Clients.User 應用程式開發介面**</span><span class="sxs-lookup"><span data-stu-id="605aa-395">**Using the Clients.User API**</span></span>

[!code-csharp[Main](release-notes/samples/sample14.cs)]

<a id="errorhandling"></a>

### <a name="better-error-handling-support"></a><span data-ttu-id="605aa-396">更好的錯誤處理支援</span><span class="sxs-lookup"><span data-stu-id="605aa-396">Better Error Handling Support</span></span>

<span data-ttu-id="605aa-397">使用者現在可以擲回**HubException**從任何中樞叫用。</span><span class="sxs-lookup"><span data-stu-id="605aa-397">Users can now throw **HubException** from any hub invocation.</span></span> <span data-ttu-id="605aa-398">建構函式**HubException**字串訊息和物件可能需要額外的錯誤資料。</span><span class="sxs-lookup"><span data-stu-id="605aa-398">The constructor of the **HubException** can take a string message and an object extra error data.</span></span> <span data-ttu-id="605aa-399">SignalR 將自動序列化例外狀況，並將它傳送至用戶端它用來拒絕/失敗中樞方法叫用。</span><span class="sxs-lookup"><span data-stu-id="605aa-399">SignalR will auto-serialize the exception and send it to the client where it will be used to reject/fail the hub method invocation.</span></span>

<span data-ttu-id="605aa-400">**顯示詳細的中樞例外狀況**設定沒有任何關係**HubException**或; 傳送回用戶端一律傳送出去。</span><span class="sxs-lookup"><span data-stu-id="605aa-400">The **show detailed hub exceptions** setting has no bearing on **HubException** being sent back to the client or not; it is always sent.</span></span>

<span data-ttu-id="605aa-401">**伺服器端程式碼示範 HubException 傳送給用戶端**</span><span class="sxs-lookup"><span data-stu-id="605aa-401">**Server-side code demonstrating sending a HubException to the client**</span></span>

[!code-csharp[Main](release-notes/samples/sample15.cs)]

<span data-ttu-id="605aa-402">**JavaScript 用戶端程式碼示範 HubException，從伺服器傳送回應**</span><span class="sxs-lookup"><span data-stu-id="605aa-402">**JavaScript client code demonstrating responding to a HubException sent from the server**</span></span>

[!code-html[Main](release-notes/samples/sample16.html)]

<span data-ttu-id="605aa-403">**.NET 用戶端程式碼示範 HubException，從伺服器傳送回應**</span><span class="sxs-lookup"><span data-stu-id="605aa-403">**.NET client code demonstrating responding to a HubException sent from the server**</span></span>

[!code-csharp[Main](release-notes/samples/sample17.cs)]

<a id="unittesting"></a>

### <a name="easier-unit-testing-of-hubs"></a><span data-ttu-id="605aa-404">更容易的單元測試中樞</span><span class="sxs-lookup"><span data-stu-id="605aa-404">Easier unit testing of hubs</span></span>

<span data-ttu-id="605aa-405">SignalR 2.0 包含呼叫的介面`IHubCallerConnectionContext`輕鬆地建立模擬用戶端端引動過程的中樞上。</span><span class="sxs-lookup"><span data-stu-id="605aa-405">SignalR 2.0 includes an interface called `IHubCallerConnectionContext` on Hubs that makes it easier to create mock client side invocations.</span></span> <span data-ttu-id="605aa-406">下列程式碼片段將示範如何使用這個介面與熱門測試控管[xUnit.net](https://github.com/xunit/xunit)和[moq](https://code.google.com/p/moq/)。</span><span class="sxs-lookup"><span data-stu-id="605aa-406">The following code snippets demonstrate using this interface with popular test harnesses [xUnit.net](https://github.com/xunit/xunit) and [moq](https://code.google.com/p/moq/).</span></span>

<span data-ttu-id="605aa-407">**使用單元測試 SignalR xUnit.net**</span><span class="sxs-lookup"><span data-stu-id="605aa-407">**Unit testing SignalR with xUnit.net**</span></span>

[!code-csharp[Main](release-notes/samples/sample18.cs)]

<span data-ttu-id="605aa-408">**使用單元測試 SignalR moq**</span><span class="sxs-lookup"><span data-stu-id="605aa-408">**Unit testing SignalR with moq**</span></span>

[!code-csharp[Main](release-notes/samples/sample19.cs)]

<a id="javascripterror"></a>

### <a name="javascript-error-handling"></a><span data-ttu-id="605aa-409">JavaScript 錯誤處理</span><span class="sxs-lookup"><span data-stu-id="605aa-409">JavaScript error handling</span></span>

<span data-ttu-id="605aa-410">在 SignalR 2.0 中，所有的 JavaScript 錯誤處理回呼會傳回 JavaScript 錯誤物件，而不是原始字串。</span><span class="sxs-lookup"><span data-stu-id="605aa-410">In SignalR 2.0, all JavaScript error handling callbacks return JavaScript error objects instead of raw strings.</span></span> <span data-ttu-id="605aa-411">這可讓 SignalR 流動至您的錯誤處理常式更豐富的資訊。</span><span class="sxs-lookup"><span data-stu-id="605aa-411">This allows SignalR to flow richer information to your error handlers.</span></span> <span data-ttu-id="605aa-412">您可以取得內部例外狀況，從`source`錯誤的屬性。</span><span class="sxs-lookup"><span data-stu-id="605aa-412">You can get the inner exception from the `source` property of the error.</span></span>

<span data-ttu-id="605aa-413">**處理 Start.Fail 例外狀況的 JavaScript 用戶端程式碼**</span><span class="sxs-lookup"><span data-stu-id="605aa-413">**JavaScript client code that handles the Start.Fail exception**</span></span>

[!code-javascript[Main](release-notes/samples/sample20.js)]

<a id="TOC8"></a>
## <a name="aspnet-identity"></a><span data-ttu-id="605aa-414">ASP.NET Identity</span><span class="sxs-lookup"><span data-stu-id="605aa-414">ASP.NET Identity</span></span>

### <a name="new-aspnet-membership-system"></a><span data-ttu-id="605aa-415">新的 ASP.NET 成員資格系統</span><span class="sxs-lookup"><span data-stu-id="605aa-415">New ASP.NET Membership System</span></span>

<span data-ttu-id="605aa-416">ASP.NET Identity 是新的成員資格系統，ASP.NET 應用程式。</span><span class="sxs-lookup"><span data-stu-id="605aa-416">ASP.NET Identity is the new membership system for ASP.NET applications.</span></span> <span data-ttu-id="605aa-417">ASP.NET Identity 輕鬆地整合應用程式資料的使用者特定設定檔資料。</span><span class="sxs-lookup"><span data-stu-id="605aa-417">ASP.NET Identity makes it easy to integrate user-specific profile data with application data.</span></span> <span data-ttu-id="605aa-418">ASP.NET Identity 也可讓您選擇您的應用程式中的使用者設定檔的持續性模型。</span><span class="sxs-lookup"><span data-stu-id="605aa-418">ASP.NET Identity also allows you to choose the persistence model for user profiles in your application.</span></span> <span data-ttu-id="605aa-419">您可以將資料儲存在 SQL Server 資料庫或其他資料存放區，包括 NoSQL 資料存放區，例如 Azure 儲存體資料表。</span><span class="sxs-lookup"><span data-stu-id="605aa-419">You can store the data in a SQL Server database or another data store, including NoSQL data stores such as Azure Storage Tables.</span></span> <span data-ttu-id="605aa-420">如需詳細資訊，請參閱[個別使用者帳戶](creating-web-projects-in-visual-studio.md#indauth)中**Visual Studio 2013 中建立 ASP.NET Web 專案**。</span><span class="sxs-lookup"><span data-stu-id="605aa-420">For more information, see [Individual User Accounts](creating-web-projects-in-visual-studio.md#indauth) in **Creating ASP.NET Web Projects in Visual Studio 2013**.</span></span>

### <a name="claims-based-authentication"></a><span data-ttu-id="605aa-421">宣告架構驗證</span><span class="sxs-lookup"><span data-stu-id="605aa-421">Claims-based authentication</span></span>

<span data-ttu-id="605aa-422">ASP.NET 現在支援宣告式的驗證，而使用者的身分識別都代表一組從受信任的簽發者的宣告。</span><span class="sxs-lookup"><span data-stu-id="605aa-422">ASP.NET now supports claims-based authentication, where the user's identity is represented as a set of claims from a trusted issuer.</span></span> <span data-ttu-id="605aa-423">使用者可以是已驗證的使用者名稱和密碼保存在應用程式資料庫，或使用社交身分識別提供者 (例如： Microsoft 帳戶、 Facebook、 Google、 Twitter)，或使用透過 Azure Active Directory 組織帳戶或Active Directory Federation Services (ADFS)。</span><span class="sxs-lookup"><span data-stu-id="605aa-423">Users can be authenticated using a username and password maintained in an application database, or using social identity providers (for example: Microsoft Accounts, Facebook, Google, Twitter), or using organizational accounts through Azure Active Directory or Active Directory Federation Services (ADFS).</span></span>

### <a name="integration-with-azure-active-directory-and-windows-server-active-directory"></a><span data-ttu-id="605aa-424">與 Azure Active Directory 和 Windows Server Active Directory 整合</span><span class="sxs-lookup"><span data-stu-id="605aa-424">Integration with Azure Active Directory and Windows Server Active Directory</span></span>

<span data-ttu-id="605aa-425">您現在可以建立使用 Azure Active Directory 或 Windows Server Active Directory (AD) 進行驗證的 ASP.NET 專案。</span><span class="sxs-lookup"><span data-stu-id="605aa-425">You can now create ASP.NET projects that use Azure Active Directory or Windows Server Active Directory (AD) for authentication.</span></span> <span data-ttu-id="605aa-426">如需詳細資訊，請參閱[組織帳戶](creating-web-projects-in-visual-studio.md#orgauth)中**Visual Studio 2013 中建立 ASP.NET Web 專案**。</span><span class="sxs-lookup"><span data-stu-id="605aa-426">For more information, see [Organizational Accounts](creating-web-projects-in-visual-studio.md#orgauth) in **Creating ASP.NET Web Projects in Visual Studio 2013**.</span></span>

### <a name="owin-integration"></a><span data-ttu-id="605aa-427">OWIN 整合</span><span class="sxs-lookup"><span data-stu-id="605aa-427">OWIN Integration</span></span>

<span data-ttu-id="605aa-428">ASP.NET 驗證現在會根據可用在任何 OWIN 架構的主機的 OWIN 中介軟體。</span><span class="sxs-lookup"><span data-stu-id="605aa-428">ASP.NET authentication is now based on OWIN middleware that can be used on any OWIN-based host.</span></span> <span data-ttu-id="605aa-429">如需 OWIN 的詳細資訊，請參閱下列[Microsoft OWIN 元件](#TOC7)> 一節。</span><span class="sxs-lookup"><span data-stu-id="605aa-429">For more information about OWIN, see the following [Microsoft OWIN Components](#TOC7) section.</span></span>

<a id="TOC7"></a>
## <a name="microsoft-owin-components"></a><span data-ttu-id="605aa-430">Microsoft OWIN 元件</span><span class="sxs-lookup"><span data-stu-id="605aa-430">Microsoft OWIN Components</span></span>

<span data-ttu-id="605aa-431">[開啟適用於.NET 的 Web 介面](http://owin.org/)(OWIN) 定義.NET web 伺服器和 web 應用程式之間的抽象概念。</span><span class="sxs-lookup"><span data-stu-id="605aa-431">[Open Web Interface for .NET](http://owin.org/) (OWIN) defines an abstraction between .NET web servers and web applications.</span></span> <span data-ttu-id="605aa-432">OWIN 分隔與 web 應用程式，從伺服器進行 web 應用程式主機無從驗證的。</span><span class="sxs-lookup"><span data-stu-id="605aa-432">OWIN decouples the web application from the server, making web applications host-agnostic.</span></span> <span data-ttu-id="605aa-433">例如，您可以裝載在 IIS 中 OWIN web 應用程式，或自我裝載的自訂程序中。</span><span class="sxs-lookup"><span data-stu-id="605aa-433">For example, you can host an OWIN-based web application in IIS or self-host it in a custom process.</span></span>

<span data-ttu-id="605aa-434">Microsoft OWIN 元件 （也稱為 Katana 專案） 中導入的變更包括新的伺服器和主機的元件、 新的協助程式程式庫中介軟體，以及新的驗證中介軟體。</span><span class="sxs-lookup"><span data-stu-id="605aa-434">Changes introduced in the Microsoft OWIN components (also known as the Katana project) include new server and host components, new helper libraries and middleware, and new authentication middleware.</span></span>

<span data-ttu-id="605aa-435">OWIN 和 Katana 相關的詳細資訊，請參閱[OWIN 和 Katana 中最新消息](../../../aspnet/overview/owin-and-katana/index.md)。</span><span class="sxs-lookup"><span data-stu-id="605aa-435">For more information about OWIN and Katana, see [What's new in OWIN and Katana](../../../aspnet/overview/owin-and-katana/index.md).</span></span>

<span data-ttu-id="605aa-436">**注意： [OWIN](../../../aspnet/overview/owin-and-katana/an-overview-of-project-katana.md)應用程式無法在 IIS 傳統模式執行，則必須在整合式模式中執行。**</span><span class="sxs-lookup"><span data-stu-id="605aa-436">**Note: [OWIN](../../../aspnet/overview/owin-and-katana/an-overview-of-project-katana.md) applications cannot run in IIS classic mode; they must be run in integrated mode.**</span></span>

<span data-ttu-id="605aa-437">**注意： [OWIN](../../../aspnet/overview/owin-and-katana/an-overview-of-project-katana.md)必須完全信任中執行應用程式。**</span><span class="sxs-lookup"><span data-stu-id="605aa-437">**Note: [OWIN](../../../aspnet/overview/owin-and-katana/an-overview-of-project-katana.md) applications must be run in full trust.**</span></span>

### <a name="new-servers-and-hosts"></a><span data-ttu-id="605aa-438">新的伺服器與主控件</span><span class="sxs-lookup"><span data-stu-id="605aa-438">New Servers and Hosts</span></span>

<span data-ttu-id="605aa-439">與此版本中，加入了新元件，以啟用自我裝載案例。</span><span class="sxs-lookup"><span data-stu-id="605aa-439">With this release, new components were added to enable self-host scenarios.</span></span> <span data-ttu-id="605aa-440">這些元件包括下列 NuGet 套件：</span><span class="sxs-lookup"><span data-stu-id="605aa-440">These components include the following NuGet packages:</span></span>

- <span data-ttu-id="605aa-441">**Microsoft.Owin.Host.HttpListener**。</span><span class="sxs-lookup"><span data-stu-id="605aa-441">**Microsoft.Owin.Host.HttpListener**.</span></span> <span data-ttu-id="605aa-442">提供 OWIN 使用的伺服器， **HttpListener**接聽 HTTP 要求，並將他們導向至 OWIN 管線。</span><span class="sxs-lookup"><span data-stu-id="605aa-442">Provides an OWIN server that uses **HttpListener** to listen for HTTP requests and direct them into the OWIN pipeline.</span></span>
- <span data-ttu-id="605aa-443">**Microsoft.Owin.Hosting**提供文件庫的開發人員想要自助代管 OWIN 管線中的自訂處理序，例如主控台應用程式或 Windows 服務。</span><span class="sxs-lookup"><span data-stu-id="605aa-443">**Microsoft.Owin.Hosting** Provides a library for developers who wish to self-host an OWIN pipeline in a custom process, such as a console application or Windows service.</span></span>
- <span data-ttu-id="605aa-444">**OwinHost**。</span><span class="sxs-lookup"><span data-stu-id="605aa-444">**OwinHost**.</span></span> <span data-ttu-id="605aa-445">提供獨立的可執行檔包裝`Microsoft.Owin.Hosting`並可讓您在自我裝載 OWIN 管線，而不需要撰寫自訂主應用程式。</span><span class="sxs-lookup"><span data-stu-id="605aa-445">Provides a stand-alone executable that wraps `Microsoft.Owin.Hosting` and lets you self-host an OWIN pipeline without having to write a custom host application.</span></span>

<span data-ttu-id="605aa-446">此外，`Microsoft.Owin.Host.SystemWeb`封裝現在可讓中介軟體提供提示給**SystemWeb**伺服器，表示在特定的 ASP.NET 管線階段期間，應該呼叫中介軟體。</span><span class="sxs-lookup"><span data-stu-id="605aa-446">In addition, the `Microsoft.Owin.Host.SystemWeb` package now enables middleware to provide hints to the **SystemWeb** server, indicating that the middleware should be called during a specific ASP.NET pipeline stage.</span></span> <span data-ttu-id="605aa-447">這項功能就特別有用，驗證中介軟體，應該在早期的 ASP.NET 管線中執行的。</span><span class="sxs-lookup"><span data-stu-id="605aa-447">This feature is particularly useful for authentication middleware, which should run early in the ASP.NET pipeline.</span></span>

### <a name="helper-libraries-and-middleware"></a><span data-ttu-id="605aa-448">協助程式程式庫和中介軟體</span><span class="sxs-lookup"><span data-stu-id="605aa-448">Helper Libraries and Middleware</span></span>

<span data-ttu-id="605aa-449">雖然您可以撰寫 OWIN 元件使用的函式和類型定義 OWIN 規格中，從新`Microsoft.Owin`套件提供一組更加易懂易記的抽象概念。</span><span class="sxs-lookup"><span data-stu-id="605aa-449">Although you can write OWIN components using only the function and type definitions from the OWIN specification, the new `Microsoft.Owin` package provides a more user-friendly set of abstractions.</span></span> <span data-ttu-id="605aa-450">此套件會結合數個舊版的封裝 (例如`Owin.Extensions`， `Owin.Types`) 到單一結構完善的物件模型可以輕鬆地使用其他 OWIN 元件。</span><span class="sxs-lookup"><span data-stu-id="605aa-450">This package combines several earlier packages (e.g., `Owin.Extensions`, `Owin.Types`) into a single, well-structured object model that can then be easily used by other OWIN components.</span></span> <span data-ttu-id="605aa-451">事實上，大部分的 Microsoft OWIN 元件現在會使用此封裝。</span><span class="sxs-lookup"><span data-stu-id="605aa-451">In fact, the majority of Microsoft OWIN components now use this package.</span></span>

> [!NOTE]
> <span data-ttu-id="605aa-452">[OWIN](http://www.owin.org)應用程式無法在 IIS 傳統模式執行，則必須在整合式模式中執行。</span><span class="sxs-lookup"><span data-stu-id="605aa-452">[OWIN](http://www.owin.org) applications cannot run in IIS classic mode; they must be run in integrated mode.</span></span>

> [!NOTE]
> <span data-ttu-id="605aa-453">[OWIN](http://www.owin.org)必須完全信任中執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="605aa-453">[OWIN](http://www.owin.org) applications must be run in full trust.</span></span>

<span data-ttu-id="605aa-454">此版本也包含 Microsoft.Owin.Diagnostics 套件，其中包含中介軟體驗證執行的 OWIN 應用程式，再加上以協助調查失敗的錯誤頁面中介軟體。</span><span class="sxs-lookup"><span data-stu-id="605aa-454">This release also includes the Microsoft.Owin.Diagnostics package, which includes middleware to validate a running OWIN application, plus error-page middleware to help investigate failures.</span></span>

### <a name="authentication-components"></a><span data-ttu-id="605aa-455">驗證元件</span><span class="sxs-lookup"><span data-stu-id="605aa-455">Authentication Components</span></span>

<span data-ttu-id="605aa-456">使用下列的驗證元件。</span><span class="sxs-lookup"><span data-stu-id="605aa-456">The following authentication components are available.</span></span>

- <span data-ttu-id="605aa-457">**Microsoft.Owin.Security.ActiveDirectory**。</span><span class="sxs-lookup"><span data-stu-id="605aa-457">**Microsoft.Owin.Security.ActiveDirectory**.</span></span> <span data-ttu-id="605aa-458">啟用使用在內部部署或雲端式目錄服務的驗證。</span><span class="sxs-lookup"><span data-stu-id="605aa-458">Enables authentication using on-premise or cloud-based directory services.</span></span>
- <span data-ttu-id="605aa-459">**Microsoft.Owin.Security.Cookies**使用 cookie 會啟用驗證。</span><span class="sxs-lookup"><span data-stu-id="605aa-459">**Microsoft.Owin.Security.Cookies** Enables authentication using cookies.</span></span> <span data-ttu-id="605aa-460">此套件先前命名為`Microsoft.Owin.Security.Forms`。</span><span class="sxs-lookup"><span data-stu-id="605aa-460">This package was previously named `Microsoft.Owin.Security.Forms`.</span></span>
- <span data-ttu-id="605aa-461">**Microsoft.Owin.Security.Facebook**啟用驗證使用 Facebook 的 OAuth 基礎服務。</span><span class="sxs-lookup"><span data-stu-id="605aa-461">**Microsoft.Owin.Security.Facebook** Enables authentication using Facebook's OAuth-based service.</span></span>
- <span data-ttu-id="605aa-462">**Microsoft.Owin.Security.Google**使用 Google OpenID 型服務啟用驗證。</span><span class="sxs-lookup"><span data-stu-id="605aa-462">**Microsoft.Owin.Security.Google** Enables authentication using Google's OpenID-based service.</span></span>
- <span data-ttu-id="605aa-463">**Microsoft.Owin.Security.Jwt**啟用驗證使用 JWT 權杖。</span><span class="sxs-lookup"><span data-stu-id="605aa-463">**Microsoft.Owin.Security.Jwt** Enables authentication using JWT tokens.</span></span>
- <span data-ttu-id="605aa-464">**Microsoft.Owin.Security.MicrosoftAccount**啟用驗證使用 Microsoft 帳戶。</span><span class="sxs-lookup"><span data-stu-id="605aa-464">**Microsoft.Owin.Security.MicrosoftAccount** Enables authentication using Microsoft accounts.</span></span>
- <span data-ttu-id="605aa-465">**Microsoft.Owin.Security.OAuth**。</span><span class="sxs-lookup"><span data-stu-id="605aa-465">**Microsoft.Owin.Security.OAuth**.</span></span> <span data-ttu-id="605aa-466">提供 OAuth 授權伺服器與中介軟體驗證持有人權杖。</span><span class="sxs-lookup"><span data-stu-id="605aa-466">Provides an OAuth authorization server as well as middleware for authenticating bearer tokens.</span></span>
- <span data-ttu-id="605aa-467">**Microsoft.Owin.Security.Twitter**啟用驗證使用 Twitter 的 OAuth 基礎服務。</span><span class="sxs-lookup"><span data-stu-id="605aa-467">**Microsoft.Owin.Security.Twitter** Enables authentication using Twitter's OAuth-based service.</span></span>

<span data-ttu-id="605aa-468">此版本也包含`Microsoft.Owin.Cors`包含處理跨原始 HTTP 要求的中介軟體套件。</span><span class="sxs-lookup"><span data-stu-id="605aa-468">This release also includes the `Microsoft.Owin.Cors` package, which contains middleware for processing cross-origin HTTP requests.</span></span>

> [!NOTE]
> <span data-ttu-id="605aa-469">在 Visual Studio 2013 的最終版本中移除了來簽署 JWT 的支援。</span><span class="sxs-lookup"><span data-stu-id="605aa-469">Support for JWT signing has been removed in the final version of Visual Studio 2013.</span></span>

<a id="ef6"></a>
## <a name="entity-framework-6"></a><span data-ttu-id="605aa-470">Entity Framework 6</span><span class="sxs-lookup"><span data-stu-id="605aa-470">Entity Framework 6</span></span>

<span data-ttu-id="605aa-471">如需新功能和 Entity Framework 6 中的其他變更的清單，請參閱[Entity Framework 版本記錄](https://msdn.com/data/jj574253)。</span><span class="sxs-lookup"><span data-stu-id="605aa-471">For a list of new features and other changes in Entity Framework 6, see [Entity Framework Version History](https://msdn.com/data/jj574253).</span></span>

<a id="TOC14"></a>
## <a name="aspnet-razor-3"></a><span data-ttu-id="605aa-472">ASP.NET Razor 3</span><span class="sxs-lookup"><span data-stu-id="605aa-472">ASP.NET Razor 3</span></span>

<span data-ttu-id="605aa-473">ASP.NET Razor 3 包含下列新功能：</span><span class="sxs-lookup"><span data-stu-id="605aa-473">ASP.NET Razor 3 includes the following new features:</span></span>

- <span data-ttu-id="605aa-474">支援編輯索引標籤。</span><span class="sxs-lookup"><span data-stu-id="605aa-474">Support for Tab editing.</span></span> <span data-ttu-id="605aa-475">Preivously，**格式化文件**命令、 自動縮排，並自動在 Visual Studio 中格式化未正確運作時使用**保留定位點**選項。</span><span class="sxs-lookup"><span data-stu-id="605aa-475">Preivously, the **Format Document** command, auto indenting, and auto formatting in Visual Studio did not work correctly when using the **Keep Tabs** option.</span></span> <span data-ttu-id="605aa-476">這項變更就會更正格式的格式設定 索引標籤的 Razor 程式碼的 Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="605aa-476">This change corrects Visual Studio formatting for Razor code for tab formatting.</span></span>
- <span data-ttu-id="605aa-477">支援 URL 重寫規則時產生連結。</span><span class="sxs-lookup"><span data-stu-id="605aa-477">Support for URL Rewrite rules when generating links.</span></span>
- <span data-ttu-id="605aa-478">安全性透明屬性中移除。</span><span class="sxs-lookup"><span data-stu-id="605aa-478">Removal of security transparent attribute.</span></span>
 > [!NOTE]
 > <span data-ttu-id="605aa-479">這是一項重大變更，並使 Razor 3 相容 MVC4 和舊版中，Razor 2 時與 MVC5 或針對 MVC5 編譯的組件不相容。</span><span class="sxs-lookup"><span data-stu-id="605aa-479">This is a breaking change, and makes Razor 3 incompatible with MVC4 and earlier, while Razor 2 is incompatible with MVC5 or assemblies compiled against MVC5.</span></span>

<span data-ttu-id="605aa-480">修正 Visual Studio 2013 中，從發行前版本的 razor 3 問題可以找到[這裡](https://aspnetwebstack.codeplex.com/workitem/list/advanced?keyword=&status=Resolved%7cClosed&type=All&priority=All&release=All%7cv5.0%2bPreview%7cv5.0%2bRC%7cv5.0%2bRTM&assignedTo=All&component=Web%2bPages%252fRazor&reasonClosed=Fixed&sortField=LastUpdatedDate&sortDirection=Descending&page=0)。</span><span class="sxs-lookup"><span data-stu-id="605aa-480">Razor 3 issues fixed in Visual Studio 2013 from pre-release versions can be found [here](https://aspnetwebstack.codeplex.com/workitem/list/advanced?keyword=&status=Resolved%7cClosed&type=All&priority=All&release=All%7cv5.0%2bPreview%7cv5.0%2bRC%7cv5.0%2bRTM&assignedTo=All&component=Web%2bPages%252fRazor&reasonClosed=Fixed&sortField=LastUpdatedDate&sortDirection=Descending&page=0).</span></span>

<a id="TOC15"></a>
## <a name="aspnet-app-suspend"></a><span data-ttu-id="605aa-481">ASP.NET 應用程式暫停</span><span class="sxs-lookup"><span data-stu-id="605aa-481">ASP.NET App Suspend</span></span>

<span data-ttu-id="605aa-482">ASP.NET 應用程式暫停是.NET Framework 4.5.1 會徹底變更的使用者經驗與裝載在單一機器上的 ASP.NET 網站的數目很大的經濟模型遊戲變更功能。</span><span class="sxs-lookup"><span data-stu-id="605aa-482">ASP.NET App Suspend is a game-changing feature in the .NET Framework 4.5.1 that radically changes the user experience and economic model for hosting large numbers of ASP.NET sites on a single machine.</span></span> <span data-ttu-id="605aa-483">如需詳細資訊，請參閱[.NET web 裝載的 ASP.NET 應用程式暫止 – 回應共用](https://blogs.msdn.com/b/dotnet/archive/2013/10/09/asp-net-app-suspend-responsive-shared-net-web-hosting.aspx)。</span><span class="sxs-lookup"><span data-stu-id="605aa-483">For more information, see [ASP.NET App Suspend – responsive shared .NET web hosting](https://blogs.msdn.com/b/dotnet/archive/2013/10/09/asp-net-app-suspend-responsive-shared-net-web-hosting.aspx).</span></span>

<a id="knownissues"></a>
## <a name="known-issues-and-breaking-changes"></a><span data-ttu-id="605aa-484">已知的問題和重大變更</span><span class="sxs-lookup"><span data-stu-id="605aa-484">Known Issues and Breaking Changes</span></span>

<span data-ttu-id="605aa-485">本章節描述已知的問題和重大變更 ASP.NET 及 Web Tools for Visual Studio 2013。</span><span class="sxs-lookup"><span data-stu-id="605aa-485">This section describes known issues and breaking changes in the ASP.NET and Web Tools for Visual Studio 2013.</span></span>

### <a name="nuget"></a><span data-ttu-id="605aa-486">NuGet</span><span class="sxs-lookup"><span data-stu-id="605aa-486">NuGet</span></span>

- <span data-ttu-id="605aa-487">[新的封裝還原不適用於單聲道上使用 SLN 檔](https://nuget.codeplex.com/workitem/3596)– 即將 nuget.exe 下載將會修正和[NuGet.CommandLine 封裝](http://www.nuget.org/packages/NuGet.CommandLine/)更新。</span><span class="sxs-lookup"><span data-stu-id="605aa-487">[New package restore doesn't work on Mono when using SLN file](https://nuget.codeplex.com/workitem/3596) – will be fixed in an upcoming nuget.exe download and [NuGet.CommandLine package](http://www.nuget.org/packages/NuGet.CommandLine/) update.</span></span>
- <span data-ttu-id="605aa-488">[新的封裝還原不適合用於 Wix 專案](https://nuget.codeplex.com/workitem/3598)– 即將 nuget.exe 下載將會修正和[NuGet.CommandLine 封裝](http://www.nuget.org/packages/NuGet.CommandLine/)更新。</span><span class="sxs-lookup"><span data-stu-id="605aa-488">[New package restore doesn't work with Wix projects](https://nuget.codeplex.com/workitem/3598) – will be fixed in an upcoming nuget.exe download and [NuGet.CommandLine package](http://www.nuget.org/packages/NuGet.CommandLine/) update.</span></span>
- <span data-ttu-id="605aa-489">[自動封裝還原不適用於專案的方案資料夾下](https://nuget.codeplex.com/workitem/3625)– NuGet 2.8 會修正問題。</span><span class="sxs-lookup"><span data-stu-id="605aa-489">[Automatic Package restore doesn't work for projects under a solution folder](https://nuget.codeplex.com/workitem/3625) – will be fixed in NuGet 2.8.</span></span>

### <a name="aspnet-web-api"></a><span data-ttu-id="605aa-490">ASP.NET Web API</span><span class="sxs-lookup"><span data-stu-id="605aa-490">ASP.NET Web API</span></span>

1. <span data-ttu-id="605aa-491">`ODataQueryOptions<T>.ApplyTo(IQueryable)`不會傳回`IQueryable<T>`一律，我們加入了支援`$select`和`$expand`。</span><span class="sxs-lookup"><span data-stu-id="605aa-491">`ODataQueryOptions<T>.ApplyTo(IQueryable)` doesn't return `IQueryable<T>` always, as we added support for `$select` and `$expand`.</span></span>

    <span data-ttu-id="605aa-492">我們先前的範例如`ODataQueryOptions<T>`一律轉型的傳回值從`ApplyTo`至`IQueryable<T>`。</span><span class="sxs-lookup"><span data-stu-id="605aa-492">Our earlier samples for `ODataQueryOptions<T>` always casted the return value from `ApplyTo` to `IQueryable<T>`.</span></span> <span data-ttu-id="605aa-493">此查詢選項，因為先前使用過我們支援早 (`$filter`， `$orderby`， `$skip`， `$top`) 不會變更查詢的圖形。</span><span class="sxs-lookup"><span data-stu-id="605aa-493">This worked earlier because the query options that we supported earlier (`$filter`, `$orderby`, `$skip`, `$top`) do not change the shape of the query.</span></span> <span data-ttu-id="605aa-494">現在，我們支援`$select`和`$expand`的傳回值`ApplyTo`將不會`IQueryable<T>`一律。</span><span class="sxs-lookup"><span data-stu-id="605aa-494">Now that we support `$select` and `$expand` the return value from `ApplyTo` will not be `IQueryable<T>` always.</span></span>

    [!code-csharp[Main](release-notes/samples/sample21.cs)]

    <span data-ttu-id="605aa-495">如果您使用從先前的範例程式碼，它就會繼續工作，如果用戶端不會傳送`$select`和`$expand`。</span><span class="sxs-lookup"><span data-stu-id="605aa-495">If you are using the sample code from earlier, it will continue working if the client does not send `$select` and `$expand`.</span></span> <span data-ttu-id="605aa-496">不過，如果您想要支援`$select`和`$expand`您必須將該程式碼變更為。</span><span class="sxs-lookup"><span data-stu-id="605aa-496">However, if you wish to support `$select` and `$expand` you have to change that code to this.</span></span>

    [!code-csharp[Main](release-notes/samples/sample22.cs)]
2. <span data-ttu-id="605aa-497">**Request.Url RequestContext.Url 設為 null 或批次要求期間**</span><span class="sxs-lookup"><span data-stu-id="605aa-497">**Request.Url or RequestContext.Url is null during a batch request**</span></span>

    <span data-ttu-id="605aa-498">在批次處理的案例中， **UrlHelper**為 null 時從存取**Request.Url**或**RequestContext.Url**。</span><span class="sxs-lookup"><span data-stu-id="605aa-498">In a batching scenario, **UrlHelper** is null when accessed from **Request.Url** or **RequestContext.Url**.</span></span>

    <span data-ttu-id="605aa-499">此問題目前追蹤以下： [BatchRequestContext.Url 為 null 的批次要求](http://aspnetwebstack.codeplex.com/workitem/1301)。</span><span class="sxs-lookup"><span data-stu-id="605aa-499">This issue is currently tracked here: [BatchRequestContext.Url is null for batching request](http://aspnetwebstack.codeplex.com/workitem/1301).</span></span>

    <span data-ttu-id="605aa-500">此問題的因應措施是建立的新執行個體**UrlHelper**，如下列範例所示：</span><span class="sxs-lookup"><span data-stu-id="605aa-500">The workaround for this issue is to create a new instance of **UrlHelper**, as in the following example:</span></span>

    <span data-ttu-id="605aa-501">**建立 UrlHelper 的新執行個體**</span><span class="sxs-lookup"><span data-stu-id="605aa-501">**Creating a new instance of UrlHelper**</span></span>

    [!code-csharp[Main](release-notes/samples/sample23.cs)]

### <a name="aspnet-mvc"></a><span data-ttu-id="605aa-502">ASP.NET MVC</span><span class="sxs-lookup"><span data-stu-id="605aa-502">ASP.NET MVC</span></span>

1. <span data-ttu-id="605aa-503">使用 MVC5 和時 OrgAuth，如果您的檢視完成這件事 AntiForgerToken 驗證，您可能會遇到下列錯誤時張貼至檢視的資料：</span><span class="sxs-lookup"><span data-stu-id="605aa-503">When using MVC5 and OrgAuth, if you have views which do AntiForgerToken validation, you might come across the following error when you post data to the view:</span></span>

    <span data-ttu-id="605aa-504">**錯誤**:</span><span class="sxs-lookup"><span data-stu-id="605aa-504">**Error**:</span></span>

    <span data-ttu-id="605aa-505">*'/' 應用程式中的伺服器錯誤。*</span><span class="sxs-lookup"><span data-stu-id="605aa-505">*Server Error in '/' Application.*</span></span>

    <span data-ttu-id="605aa-506">*之宣告的型別 'http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier' 或 'http://schemas.microsoft.com/accesscontrolservice/2010/07/claims/identityprovider' 不存在於上提供的身分識別。若要啟用防偽語彙基元支援使用宣告式驗證，請確認已設定的宣告提供者會提供這兩個身分識別執行個體就會產生這些宣告。如果已設定的宣告提供者改為使用不同的宣告類型做為唯一的識別項，則它可以設定的靜態屬性 AntiForgeryConfig.UniqueClaimTypeIdentifier 設定。*</span><span class="sxs-lookup"><span data-stu-id="605aa-506">*A claim of type 'http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier' or 'http://schemas.microsoft.com/accesscontrolservice/2010/07/claims/identityprovider' was not present on the provided ClaimsIdentity. To enable anti-forgery token support with claims-based authentication, please verify that the configured claims provider is providing both of these claims on the ClaimsIdentity instances it generates. If the configured claims provider instead uses a different claim type as a unique identifier, it can be configured by setting the static property AntiForgeryConfig.UniqueClaimTypeIdentifier.*</span></span>

    <span data-ttu-id="605aa-507">**因應措施**：</span><span class="sxs-lookup"><span data-stu-id="605aa-507">**Workaround**:</span></span>

    <span data-ttu-id="605aa-508">若要修正此問題的 Global.asax 中加入下行：</span><span class="sxs-lookup"><span data-stu-id="605aa-508">Add the following line in Global.asax to fix it:</span></span>

    `AntiForgeryConfig.UniqueClaimTypeIdentifier = ClaimTypes.Name;`

    <span data-ttu-id="605aa-509">這將在下一版的修正。</span><span class="sxs-lookup"><span data-stu-id="605aa-509">This will be fixed for the next release.</span></span>
2. <span data-ttu-id="605aa-510">升級之後的 MVC4 應用程式至 MVC5，建置方案並啟動它。</span><span class="sxs-lookup"><span data-stu-id="605aa-510">After upgrading an MVC4 app to MVC5, build the solution and launch it.</span></span> <span data-ttu-id="605aa-511">您應該會看到下列錯誤：</span><span class="sxs-lookup"><span data-stu-id="605aa-511">You should see the following error:</span></span>

    <span data-ttu-id="605aa-512">[A]System.Web.WebPages.Razor.Configuration.HostSection 無法轉換成 [B]System.Web.WebPages.Razor.Configuration.HostSection。</span><span class="sxs-lookup"><span data-stu-id="605aa-512">[A]System.Web.WebPages.Razor.Configuration.HostSection cannot be cast to [B]System.Web.WebPages.Razor.Configuration.HostSection.</span></span> <span data-ttu-id="605aa-513">類型為 A 源自 'System.Web.WebPages.Razor，Version = 2.0.0.0，Culture = neutral，PublicKeyToken = 31bf3856ad364e35' 內容位置的' Default' 中 ' C:\windows\Microsoft.Net\assembly\GAC\_MSIL\System.Web.WebPages.Razor\v4.0\_2.0.0.0\_\_31bf3856ad364e35\System.Web.WebPages.Razor.dll'。</span><span class="sxs-lookup"><span data-stu-id="605aa-513">Type A originates from 'System.Web.WebPages.Razor, Version=2.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35' in the context 'Default' at location 'C:\windows\Microsoft.Net\assembly\GAC\_MSIL\System.Web.WebPages.Razor\v4.0\_2.0.0.0\_\_31bf3856ad364e35\System.Web.WebPages.Razor.dll'.</span></span> <span data-ttu-id="605aa-514">型別 B 源自 'System.Web.WebPages.Razor，Version = 3.0.0.0，Culture = neutral，PublicKeyToken = 31bf3856ad364e35' 中的內容位置的' Default' ' C:\Windows\Microsoft.NET\Framework\v4.0.30319\Temporary ASP.NET Files\root\6d05bbd0\e8b5908e\assembly\dl3\c9cbca63\f8910382\_6273ce01\System.Web.WebPages.Razor.dll'。</span><span class="sxs-lookup"><span data-stu-id="605aa-514">Type B originates from 'System.Web.WebPages.Razor, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35' in the context 'Default' at location 'C:\Windows\Microsoft.NET\Framework\v4.0.30319\Temporary ASP.NET Files\root\6d05bbd0\e8b5908e\assembly\dl3\c9cbca63\f8910382\_6273ce01\System.Web.WebPages.Razor.dll'.</span></span>

    <span data-ttu-id="605aa-515">若要修正上述錯誤，請開啟*所有*中的 Web.config 檔案 （包括 [檢視] 資料夾中） 您的專案並執行下列：</span><span class="sxs-lookup"><span data-stu-id="605aa-515">To fix the above error, open *all* the Web.config files (including the ones in the Views folder) in your project and do the following:</span></span>

    1. <span data-ttu-id="605aa-516">更新版本的"4.0.0.0 」"system.web.mvc 的參考 」 到 「 5.0.0.0 」 的所有項目。</span><span class="sxs-lookup"><span data-stu-id="605aa-516">Update all occurrences of version "4.0.0.0" of "System.Web.Mvc" to "5.0.0.0".</span></span>
    2. <span data-ttu-id="605aa-517">更新 「 System.Web.Helpers"，版本"2.0.0.0"的所有項目&quot;System.Web.WebPages&quot;和&quot;System.Web.WebPages.Razor&quot;至 「 3.0.0.0"</span><span class="sxs-lookup"><span data-stu-id="605aa-517">Update all occurrences of version "2.0.0.0" of "System.Web.Helpers", &quot;System.Web.WebPages&quot; and &quot;System.Web.WebPages.Razor&quot; to "3.0.0.0"</span></span>

    <span data-ttu-id="605aa-518">例如，您進行上述變更之後，組件繫結看起來應該像這樣：</span><span class="sxs-lookup"><span data-stu-id="605aa-518">For example, after you make the above changes, the assembly bindings should look like this:</span></span>

    [!code-xml[Main](release-notes/samples/sample24.xml)]

    <span data-ttu-id="605aa-519">將 MVC 4 專案升級至 MVC 5 的資訊，請參閱[如何將 ASP.NET MVC 4 和 Web API 專案升級至 ASP.NET MVC 5 和 Web API 2](../../../mvc/overview/releases/how-to-upgrade-an-aspnet-mvc-4-and-web-api-project-to-aspnet-mvc-5-and-web-api-2.md)。</span><span class="sxs-lookup"><span data-stu-id="605aa-519">For information on upgrading MVC 4 projects to MVC 5, see [How to Upgrade an ASP.NET MVC 4 and Web API Project to ASP.NET MVC 5 and Web API 2](../../../mvc/overview/releases/how-to-upgrade-an-aspnet-mvc-4-and-web-api-project-to-aspnet-mvc-5-and-web-api-2.md).</span></span>
3. <span data-ttu-id="605aa-520">當使用 jQuery 驗證不顯眼的用戶端驗證，驗證訊息有時不正確的 HTML input 元素，具有類型 = 'number'。</span><span class="sxs-lookup"><span data-stu-id="605aa-520">When using client-side validation with jQuery Unobtrusive Validation, the validation message is sometimes incorrect for an HTML input element with type='number'.</span></span> <span data-ttu-id="605aa-521">驗證錯誤必要值 （「 時間欄位必要 」) 會顯示無效的數字輸入而不是正確的有效數字是必要的訊息時。</span><span class="sxs-lookup"><span data-stu-id="605aa-521">The validation error for a required value ("The Age field is required") is shown when an invalid number is entered instead of the correct message that a valid number is required.</span></span>

    <span data-ttu-id="605aa-522">此問題通常找到具有 scaffold 的程式碼的整數屬性上建立與編輯檢視的模型。</span><span class="sxs-lookup"><span data-stu-id="605aa-522">This issue is commonly found with scaffolded code for a model with an integer property on the Create and Edit views.</span></span>

    <span data-ttu-id="605aa-523">若要解決此問題，請變更編輯器協助專家從：</span><span class="sxs-lookup"><span data-stu-id="605aa-523">To work around this issue, change the editor helper from:</span></span>

    `@Html.EditorFor(person => person.Age)`

    <span data-ttu-id="605aa-524">收件者:</span><span class="sxs-lookup"><span data-stu-id="605aa-524">To:</span></span>

    `@Html.TextBoxFor(person => person.Age)`
4. <span data-ttu-id="605aa-525">ASP.NET MVC 5 已不再支援部分信任。</span><span class="sxs-lookup"><span data-stu-id="605aa-525">ASP.NET MVC 5 no longer supports partial trust.</span></span> <span data-ttu-id="605aa-526">專案和 MVC 或 WebAPI 二進位檔連結應該移除[SecurityTransparent](https://msdn.microsoft.com/en-us/library/system.security.securitytransparentattribute.aspx)屬性和[AllowPartiallyTrustedCallers](https://msdn.microsoft.com/en-us/library/system.security.allowpartiallytrustedcallersattribute.aspx)屬性。</span><span class="sxs-lookup"><span data-stu-id="605aa-526">Projects linking to the MVC or WebAPI binaries should remove the [SecurityTransparent](https://msdn.microsoft.com/en-us/library/system.security.securitytransparentattribute.aspx) attribute and the [AllowPartiallyTrustedCallers](https://msdn.microsoft.com/en-us/library/system.security.allowpartiallytrustedcallersattribute.aspx) attribute.</span></span> <span data-ttu-id="605aa-527">移除這些屬性會消除編譯器錯誤，如下所示。</span><span class="sxs-lookup"><span data-stu-id="605aa-527">Removing these attributes will eliminate compiler errors such as the following.</span></span>

    `Attempt by security transparent method ‘MyComponent' to access security critical type 'System.Web.Mvc.MvcHtmlString' failed. Assembly 'PagedList.Mvc, Version=4.3.0.0, Culture=neutral, PublicKeyToken=abbb863e9397c5e1' is marked with the AllowPartiallyTrustedCallersAttribute, and uses the level 2 security transparency model. Level 2 transparency causes all methods in AllowPartiallyTrustedCallers assemblies to become security transparent by default, which may be the cause of this exception.`

    > <span data-ttu-id="605aa-528">請注意，當副作用： 您無法在相同的應用程式中使用 4.0 和 5.0 的組件。</span><span class="sxs-lookup"><span data-stu-id="605aa-528">Note, as a side effect of this you cannot use 4.0 and 5.0 assemblies in the same application.</span></span> <span data-ttu-id="605aa-529">您必須全部更新至 5.0。</span><span class="sxs-lookup"><span data-stu-id="605aa-529">You need to update all of them to 5.0.</span></span>

### <a name="spa-template-with-facebook-authorization-may-cause-instability-in-ie-while-the-web-site-is-hosted-in-intranet-zone"></a><span data-ttu-id="605aa-530">SPA Facebook 授權範本可能會造成不穩定在 IE 中時的網站裝載在內部網路區域</span><span class="sxs-lookup"><span data-stu-id="605aa-530">SPA Template with Facebook authorization may cause instability in IE while the web site is hosted in intranet zone</span></span>

<span data-ttu-id="605aa-531">SPA 範本提供使用 Facebook 的外部記錄檔。</span><span class="sxs-lookup"><span data-stu-id="605aa-531">The SPA template provides external log in with Facebook.</span></span> <span data-ttu-id="605aa-532">當執行使用範本建立專案時，請在本機登入可能會導致 IE 損毀。</span><span class="sxs-lookup"><span data-stu-id="605aa-532">When the project created with the template is running locally, signing in may cause IE to crash.</span></span>

<span data-ttu-id="605aa-533">解決方案:</span><span class="sxs-lookup"><span data-stu-id="605aa-533">Solution:</span></span>

1. <span data-ttu-id="605aa-534">裝載在網際網路區域; 中的網站或</span><span class="sxs-lookup"><span data-stu-id="605aa-534">Host the web site in internet zone; or</span></span>

2. <span data-ttu-id="605aa-535">在非 IE 的瀏覽器中測試案例。</span><span class="sxs-lookup"><span data-stu-id="605aa-535">Test the scenario in a browser other than IE.</span></span>

### <a name="web-forms-scaffolding"></a><span data-ttu-id="605aa-536">Web Form 的 Scaffolding</span><span class="sxs-lookup"><span data-stu-id="605aa-536">Web Forms Scaffolding</span></span>

<span data-ttu-id="605aa-537">Web Form Scaffolding 已經移除了 VS2013，並將可在 Visual Studio 的未來更新中。</span><span class="sxs-lookup"><span data-stu-id="605aa-537">Web Forms Scaffolding has been removed from VS2013 and will be available in a future update to Visual Studio.</span></span> <span data-ttu-id="605aa-538">不過，您仍然可以藉由新增 MVC 相依性產生 scaffolding mvc 中使用 scaffolding Web Form 專案中。</span><span class="sxs-lookup"><span data-stu-id="605aa-538">However, you can still use scaffolding within a Web Forms project by adding MVC dependencies and generating scaffolding for MVC.</span></span> <span data-ttu-id="605aa-539">您的專案會包含 Web Form 和 MVC 的組合。</span><span class="sxs-lookup"><span data-stu-id="605aa-539">Your project will contain a combination of Web Forms and MVC.</span></span>

<span data-ttu-id="605aa-540">若要新增 MVC Web Form 專案，加入新的 scaffold 項目，然後選取**MVC 5 相依性**。</span><span class="sxs-lookup"><span data-stu-id="605aa-540">To add MVC to your Web Forms project, add a new scaffolded item and select **MVC 5 Dependencies**.</span></span> <span data-ttu-id="605aa-541">選取最少或完全根據您是否需要的所有內容檔案，例如指令碼。</span><span class="sxs-lookup"><span data-stu-id="605aa-541">Select either Minimal or Full depending on whether you need all of the content files, such as scripts.</span></span> <span data-ttu-id="605aa-542">然後，將會在您的專案建立檢視和控制器的 mvc 加入 scaffold 項目。</span><span class="sxs-lookup"><span data-stu-id="605aa-542">Then, add a scaffolded item for MVC, which will create views and a controller in your project.</span></span>

### <a name="mvc-and-web-api-scaffolding---http-404-not-found-error"></a><span data-ttu-id="605aa-543">MVC 和 Web API Scaffolding-HTTP 404 找不到錯誤</span><span class="sxs-lookup"><span data-stu-id="605aa-543">MVC and Web API Scaffolding - HTTP 404, Not Found error</span></span>

<span data-ttu-id="605aa-544">如果專案中加入 scaffold 項目時，發生錯誤，，很可能您的專案將會處於不一致的狀態。</span><span class="sxs-lookup"><span data-stu-id="605aa-544">If an error is encountered when adding a scaffolded item to a project, it is possible your project will be left in an inconsistent state.</span></span> <span data-ttu-id="605aa-545">部分 scaffolding 所做的變更將會回復，但其他變更，例如安裝的 NuGet 套件，將不會回復。</span><span class="sxs-lookup"><span data-stu-id="605aa-545">Some of the changes made be scaffolding will be rolled back but other changes, such as the installed NuGet packages, will not be rolled back.</span></span> <span data-ttu-id="605aa-546">如果路由的組態變更會回復，使用者會收到 HTTP 404 錯誤，當巡覽至 scaffold 項目。</span><span class="sxs-lookup"><span data-stu-id="605aa-546">If the routing configuration changes are rolled back, users will receive an HTTP 404 error when navigating to scaffolded items.</span></span>

<span data-ttu-id="605aa-547">因應措施：</span><span class="sxs-lookup"><span data-stu-id="605aa-547">Workaround:</span></span>

- <span data-ttu-id="605aa-548">若要修正這個錯誤 mvc 中，加入新的 scaffold 項目，然後選取 MVC 5 相依性 （基本或完整）。</span><span class="sxs-lookup"><span data-stu-id="605aa-548">To fix this error for MVC, add a new scaffolded item and select MVC 5 Dependencies (either Minimal or Full).</span></span> <span data-ttu-id="605aa-549">此程序將會加入所有必要的變更您的專案。</span><span class="sxs-lookup"><span data-stu-id="605aa-549">This process will add all of the required changes to your project.</span></span>
- <span data-ttu-id="605aa-550">若要修正這個錯誤 Web api:</span><span class="sxs-lookup"><span data-stu-id="605aa-550">To fix this error for Web API:</span></span>

    1. <span data-ttu-id="605aa-551">視情況將類別加入至您的專案。</span><span class="sxs-lookup"><span data-stu-id="605aa-551">Add the WebApiConfig class to your project.</span></span>

        [!code-csharp[Main](release-notes/samples/sample25.cs)]

        [!code-vb[Main](release-notes/samples/sample26.vb)]
    2. <span data-ttu-id="605aa-552">在應用程式中設定 WebApiConfig.Register\_，如下所示在 Global.asax 中啟動方法：</span><span class="sxs-lookup"><span data-stu-id="605aa-552">Configure WebApiConfig.Register in the Application\_Start method in Global.asax as follows:</span></span>

        [!code-csharp[Main](release-notes/samples/sample27.cs)]

        [!code-vb[Main](release-notes/samples/sample28.vb)]