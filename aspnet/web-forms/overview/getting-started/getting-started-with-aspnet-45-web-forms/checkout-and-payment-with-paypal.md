---
uid: web-forms/overview/getting-started/getting-started-with-aspnet-45-web-forms/checkout-and-payment-with-paypal
title: "簽出和與 PayPal 付款 |Microsoft 文件"
author: Erikre
description: "此教學課程將告訴您建置使用 ASP.NET 4.5 和 Microsoft Visual Studio Express 2013 for 我們的 ASP.NET Web Form 應用程式的基本概念..."
ms.author: aspnetcontent
manager: wpickett
ms.date: 09/08/2014
ms.topic: article
ms.assetid: 664ec95e-b0c9-4f43-a39f-798d0f2a7e08
ms.technology: dotnet-webforms
ms.prod: .net-framework
msc.legacyurl: /web-forms/overview/getting-started/getting-started-with-aspnet-45-web-forms/checkout-and-payment-with-paypal
msc.type: authoredcontent
ms.openlocfilehash: dd975850a3ed3e7b1746d5123572065675a88656
ms.sourcegitcommit: 9a9483aceb34591c97451997036a9120c3fe2baf
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/10/2017
---
<a name="checkout-and-payment-with-paypal"></a><span data-ttu-id="58d32-103">簽出和與 PayPal 付款</span><span class="sxs-lookup"><span data-stu-id="58d32-103">Checkout and Payment with PayPal</span></span>
====================
<span data-ttu-id="58d32-104">由[Erik Reitan](https://github.com/Erikre)</span><span class="sxs-lookup"><span data-stu-id="58d32-104">by [Erik Reitan](https://github.com/Erikre)</span></span>

<span data-ttu-id="58d32-105">[下載 Wingtip Toys 範例專案 (C#)](http://go.microsoft.com/fwlink/?LinkID=389434&clcid=0x409)或[下載電子書 (PDF)](http://download.microsoft.com/download/0/F/B/0FBFAA46-2BFD-478F-8E56-7BF3C672DF9D/Getting%20Started%20with%20ASP.NET%204.5%20Web%20Forms%20and%20Visual%20Studio%202013.pdf)</span><span class="sxs-lookup"><span data-stu-id="58d32-105">[Download Wingtip Toys Sample Project (C#)](http://go.microsoft.com/fwlink/?LinkID=389434&clcid=0x409) or [Download E-book (PDF)](http://download.microsoft.com/download/0/F/B/0FBFAA46-2BFD-478F-8E56-7BF3C672DF9D/Getting%20Started%20with%20ASP.NET%204.5%20Web%20Forms%20and%20Visual%20Studio%202013.pdf)</span></span>

> <span data-ttu-id="58d32-106">此教學課程將告訴您建置一個使用 ASP.NET 4.5 和 Microsoft Visual Studio Express 2013 for Web 的 ASP.NET Web Form 應用程式的基本概念。</span><span class="sxs-lookup"><span data-stu-id="58d32-106">This tutorial series will teach you the basics of building an ASP.NET Web Forms application using ASP.NET 4.5 and Microsoft Visual Studio Express 2013 for Web.</span></span> <span data-ttu-id="58d32-107">Visual Studio 2013[與 C# 原始程式碼的專案](https://go.microsoft.com/fwlink/?LinkID=389434&clcid=0x409)隨附此教學課程了。</span><span class="sxs-lookup"><span data-stu-id="58d32-107">A Visual Studio 2013 [project with C# source code](https://go.microsoft.com/fwlink/?LinkID=389434&clcid=0x409) is available to accompany this tutorial series.</span></span>


<span data-ttu-id="58d32-108">本教學課程說明如何修改 Wingtip Toys 範例應用程式，包括使用者的授權、 註冊和使用 PayPal 付款。</span><span class="sxs-lookup"><span data-stu-id="58d32-108">This tutorial describes how to modify the Wingtip Toys sample application to include user authorization, registration, and payment using PayPal.</span></span> <span data-ttu-id="58d32-109">使用者已登入必須購買產品的授權。</span><span class="sxs-lookup"><span data-stu-id="58d32-109">Only users who are logged in will have authorization to purchase products.</span></span> <span data-ttu-id="58d32-110">ASP.NET 4.5 Web Form 專案範本的內建的使用者註冊功能已包含許多您的需要。</span><span class="sxs-lookup"><span data-stu-id="58d32-110">The ASP.NET 4.5 Web Forms project template's built-in user registration functionality already includes much of what you need.</span></span> <span data-ttu-id="58d32-111">您將加入 PayPal Express 簽出功能。</span><span class="sxs-lookup"><span data-stu-id="58d32-111">You will add PayPal Express Checkout functionality.</span></span> <span data-ttu-id="58d32-112">在本教學課程中，您會使用 PayPal 開發人員在測試環境中，因此會不傳輸任何實際的款項。</span><span class="sxs-lookup"><span data-stu-id="58d32-112">In this tutorial you be using the PayPal developer testing environment, so no actual funds will be transferred.</span></span> <span data-ttu-id="58d32-113">在本教學課程結束時，您將測試應用程式選取產品加入購物車，然後按一下 [簽出] 按鈕，再將資料傳輸到 PayPal 測試的網站。</span><span class="sxs-lookup"><span data-stu-id="58d32-113">At the end of the tutorial, you will test the application by selecting products to add to the shopping cart, clicking the checkout button, and transferring data to the PayPal testing web site.</span></span> <span data-ttu-id="58d32-114">PayPal 測試在網站上，您會確認您的傳送和付款資訊，然後再回頭本機 Wingtip Toys 範例應用程式，以確認並完成購買程序。</span><span class="sxs-lookup"><span data-stu-id="58d32-114">On the PayPal testing web site, you will confirm your shipping and payment information and then return to the local Wingtip Toys sample application to confirm and complete the purchase.</span></span>

<span data-ttu-id="58d32-115">有數個特製化的經驗豐富的協力廠商付款處理器中線上購物，該位址延展性和安全性。</span><span class="sxs-lookup"><span data-stu-id="58d32-115">There are several experienced third-party payment processors that specialize in online shopping that address scalability and security.</span></span> <span data-ttu-id="58d32-116">ASP.NET 開發人員應該考慮利用協力廠商付款解決方案之前實作購物和購買方案的優點。</span><span class="sxs-lookup"><span data-stu-id="58d32-116">ASP.NET developers should consider the advantages of utilizing a third party payment solution before implementing a shopping and purchasing solution.</span></span>

> [!NOTE] 
> 
> <span data-ttu-id="58d32-117">Wingtip Toys 範例應用程式被設計成以 ASP.NET web 開發人員顯示 ASP.NET 的特定概念與功能。</span><span class="sxs-lookup"><span data-stu-id="58d32-117">The Wingtip Toys sample application was designed to shown specific ASP.NET concepts and features available to ASP.NET web developers.</span></span> <span data-ttu-id="58d32-118">此範例應用程式不是為所有可能的情況下就延展性和安全性最佳化。</span><span class="sxs-lookup"><span data-stu-id="58d32-118">This sample application was not optimized for all possible circumstances in regard to scalability and security.</span></span>


## <a name="what-youll-learn"></a><span data-ttu-id="58d32-119">您將學習：</span><span class="sxs-lookup"><span data-stu-id="58d32-119">What you'll learn:</span></span>

- <span data-ttu-id="58d32-120">如何限制存取特定網頁的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="58d32-120">How to restrict access to specific pages in a folder.</span></span>
- <span data-ttu-id="58d32-121">如何建立從匿名的購物車的已知的購物車。</span><span class="sxs-lookup"><span data-stu-id="58d32-121">How to create a known shopping cart from an anonymous shopping cart.</span></span>
- <span data-ttu-id="58d32-122">如何為專案啟用 SSL。</span><span class="sxs-lookup"><span data-stu-id="58d32-122">How to enable SSL for the project.</span></span>
- <span data-ttu-id="58d32-123">如何將 OAuth 提供者加入至專案。</span><span class="sxs-lookup"><span data-stu-id="58d32-123">How to add an OAuth provider to the project.</span></span>
- <span data-ttu-id="58d32-124">如何使用 PayPal 購買產品使用 PayPal 測試環境。</span><span class="sxs-lookup"><span data-stu-id="58d32-124">How to use PayPal to purchase products using the PayPal testing environment.</span></span>
- <span data-ttu-id="58d32-125">如何顯示詳細資料中的 paypal **DetailsView**控制項。</span><span class="sxs-lookup"><span data-stu-id="58d32-125">How to display details from PayPal in a **DetailsView** control.</span></span>
- <span data-ttu-id="58d32-126">如何更新詳細資料取自 PayPal Wingtip Toys 應用程式的資料庫。</span><span class="sxs-lookup"><span data-stu-id="58d32-126">How to update the database of the Wingtip Toys application with details obtained from PayPal.</span></span>

## <a name="adding-order-tracking"></a><span data-ttu-id="58d32-127">加入訂單追蹤</span><span class="sxs-lookup"><span data-stu-id="58d32-127">Adding Order Tracking</span></span>

<span data-ttu-id="58d32-128">在本教學課程中，您將建立兩個新的類別來追蹤資料從使用者建立的順序。</span><span class="sxs-lookup"><span data-stu-id="58d32-128">In this tutorial, you'll create two new classes to track data from the order a user has created.</span></span> <span data-ttu-id="58d32-129">類別會追蹤出貨資訊、 訂單總計和付款確認的資料。</span><span class="sxs-lookup"><span data-stu-id="58d32-129">The classes will track data regarding shipping information, purchase total, and payment confirmation.</span></span>

### <a name="add-the-order-and-orderdetail-model-classes"></a><span data-ttu-id="58d32-130">新增的順序和 OrderDetail 模型類別</span><span class="sxs-lookup"><span data-stu-id="58d32-130">Add the Order and OrderDetail Model Classes</span></span>

<span data-ttu-id="58d32-131">稍早在本教學課程的系列中已定義類別目錄、 產品、 結構描述和購物車的項目藉由建立`Category`， `Product`，和`CartItem`中的類別*模型*資料夾。</span><span class="sxs-lookup"><span data-stu-id="58d32-131">Earlier in this tutorial series, you defined the schema for categories, products, and shopping cart items by creating the `Category`, `Product`, and `CartItem` classes in the *Models* folder.</span></span> <span data-ttu-id="58d32-132">現在您會加入兩個新的類別來定義產品訂單和訂單的詳細資料的結構描述。</span><span class="sxs-lookup"><span data-stu-id="58d32-132">Now you will add two new classes to define the schema for the product order and the details of the order.</span></span>

1. <span data-ttu-id="58d32-133">在**模型**資料夾中，加入新的類別，名為*Order.cs*。</span><span class="sxs-lookup"><span data-stu-id="58d32-133">In the **Models** folder, add a new class named *Order.cs*.</span></span>   
 <span data-ttu-id="58d32-134">在編輯器中，會顯示新的類別檔案。</span><span class="sxs-lookup"><span data-stu-id="58d32-134">The new class file is displayed in the editor.</span></span>
2. <span data-ttu-id="58d32-135">以下列內容取代預設程式碼：</span><span class="sxs-lookup"><span data-stu-id="58d32-135">Replace the default code with the following:</span></span>   

    [!code-csharp[Main](checkout-and-payment-with-paypal/samples/sample1.cs)]
3. <span data-ttu-id="58d32-136">新增*OrderDetail.cs*類別*模型*資料夾。</span><span class="sxs-lookup"><span data-stu-id="58d32-136">Add an *OrderDetail.cs* class to the *Models* folder.</span></span>
4. <span data-ttu-id="58d32-137">下列程式碼取代預設程式碼：</span><span class="sxs-lookup"><span data-stu-id="58d32-137">Replace the default code with the following code:</span></span>   

    [!code-csharp[Main](checkout-and-payment-with-paypal/samples/sample2.cs)]

<span data-ttu-id="58d32-138">`Order`和`OrderDetail`類別包含的結構描述來定義用於購買和出貨的訂單資訊。</span><span class="sxs-lookup"><span data-stu-id="58d32-138">The `Order` and `OrderDetail` classes contain the schema to define the order information used for purchasing and shipping.</span></span>

<span data-ttu-id="58d32-139">此外，您必須更新管理的實體類別，以及提供資料存取資料庫的資料庫內容類別。</span><span class="sxs-lookup"><span data-stu-id="58d32-139">In addition, you will need to update the database context class that manages the entity classes and that provides data access to the database.</span></span> <span data-ttu-id="58d32-140">若要這樣做，您將加入新建立的順序和`OrderDetail`模型類別`ProductContext`類別。</span><span class="sxs-lookup"><span data-stu-id="58d32-140">To do this, you will add the newly created Order and `OrderDetail` model classes to `ProductContext` class.</span></span>

1. <span data-ttu-id="58d32-141">在**方案總管 中**、 尋找和開啟*ProductContext.cs*檔案。</span><span class="sxs-lookup"><span data-stu-id="58d32-141">In **Solution Explorer**, find and open the *ProductContext.cs* file.</span></span>
2. <span data-ttu-id="58d32-142">將反白顯示的程式碼加入*ProductContext.cs*檔案如下所示：</span><span class="sxs-lookup"><span data-stu-id="58d32-142">Add the highlighted code to the *ProductContext.cs* file as shown below:</span></span>   

    [!code-csharp[Main](checkout-and-payment-with-paypal/samples/sample3.cs?highlight=14-15)]

<span data-ttu-id="58d32-143">如先前所述，本教學課程系列中的程式碼*ProductContext.cs*檔都會將`System.Data.Entity`命名空間，所以您需要存取的 Entity framework 的核心功能。</span><span class="sxs-lookup"><span data-stu-id="58d32-143">As mentioned previously in this tutorial series, the code in the *ProductContext.cs* file adds the `System.Data.Entity` namespace so that you have access to all the core functionality of the Entity Framework.</span></span> <span data-ttu-id="58d32-144">此功能包括查詢、 插入、 更新和刪除資料，藉由使用強型別物件的能力。</span><span class="sxs-lookup"><span data-stu-id="58d32-144">This functionality includes the capability to query, insert, update, and delete data by working with strongly typed objects.</span></span> <span data-ttu-id="58d32-145">在上述程式碼`ProductContext`類別加入至新加入的 Entity Framework 存取`Order`和`OrderDetail`類別。</span><span class="sxs-lookup"><span data-stu-id="58d32-145">The above code in the `ProductContext` class adds Entity Framework access to the newly added `Order` and `OrderDetail` classes.</span></span>

## <a name="adding-checkout-access"></a><span data-ttu-id="58d32-146">新增簽出的存取權</span><span class="sxs-lookup"><span data-stu-id="58d32-146">Adding Checkout Access</span></span>

<span data-ttu-id="58d32-147">Wingtip Toys 範例應用程式可讓匿名使用者檢閱，並將產品加入購物車。</span><span class="sxs-lookup"><span data-stu-id="58d32-147">The Wingtip Toys sample application allows anonymous users to review and add products to a shopping cart.</span></span> <span data-ttu-id="58d32-148">不過，當匿名使用者選擇購買它們加入至購物車的產品時，他們必須登入至站台。</span><span class="sxs-lookup"><span data-stu-id="58d32-148">However, when anonymous users choose to purchase the products they added to the shopping cart, they must log on to the site.</span></span> <span data-ttu-id="58d32-149">一旦登入，就可以存取受限制的網頁之 Web 應用程式的處理簽出和購買程序。</span><span class="sxs-lookup"><span data-stu-id="58d32-149">Once they have logged on, they can access the restricted pages of the Web application that handle the checkout and purchase process.</span></span> <span data-ttu-id="58d32-150">這些限制的頁面包含在*簽出*的應用程式資料夾。</span><span class="sxs-lookup"><span data-stu-id="58d32-150">These restricted pages are contained in the *Checkout* folder of the application.</span></span>

### <a name="add-a-checkout-folder-and-pages"></a><span data-ttu-id="58d32-151">簽出，將資料夾加入頁面</span><span class="sxs-lookup"><span data-stu-id="58d32-151">Add a Checkout Folder and Pages</span></span>

<span data-ttu-id="58d32-152">您即將建立*簽出*資料夾和它的客戶會看到在結帳程序中的頁面。</span><span class="sxs-lookup"><span data-stu-id="58d32-152">You will now create the *Checkout* folder and the pages in it that the customer will see during the checkout process.</span></span> <span data-ttu-id="58d32-153">稍後在本教學課程，您將會更新這些頁面。</span><span class="sxs-lookup"><span data-stu-id="58d32-153">You will update these pages later in this tutorial.</span></span>

1. <span data-ttu-id="58d32-154">以滑鼠右鍵按一下專案名稱 (**Wingtip Toys**) 中**方案總管 中**選取**加入新的資料夾**。</span><span class="sxs-lookup"><span data-stu-id="58d32-154">Right-click the project name (**Wingtip Toys**) in **Solution Explorer** and select **Add a New Folder**.</span></span> 

    ![簽出和 PayPal-新增資料夾與付款](checkout-and-payment-with-paypal/_static/image1.png)
2. <span data-ttu-id="58d32-156">將新的資料夾命名*簽出*。</span><span class="sxs-lookup"><span data-stu-id="58d32-156">Name the new folder *Checkout*.</span></span>
3. <span data-ttu-id="58d32-157">以滑鼠右鍵按一下*簽出*資料夾，然後選取**新增**-&gt;**新項目**。</span><span class="sxs-lookup"><span data-stu-id="58d32-157">Right-click the *Checkout* folder and then select **Add**-&gt;**New Item**.</span></span> 

    ![簽出和 PayPal-新項目與付款](checkout-and-payment-with-paypal/_static/image2.png)
4. <span data-ttu-id="58d32-159">隨即顯示 [ 新增項目] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="58d32-159">The **Add New Item** dialog box is displayed.</span></span>
5. <span data-ttu-id="58d32-160">選取**Visual C#**  - &gt; **Web**左側的 [範本] 群組。</span><span class="sxs-lookup"><span data-stu-id="58d32-160">Select the **Visual C#** -&gt; **Web** templates group on the left.</span></span> <span data-ttu-id="58d32-161">然後從中間窗格中，選取**使用主版頁面的 Web Form**並將其命名*CheckoutStart.aspx*。</span><span class="sxs-lookup"><span data-stu-id="58d32-161">Then, from the middle pane, select **Web Form with Master Page**and name it *CheckoutStart.aspx*.</span></span> 

    ![簽出 」 和 「 付款 PayPal-與加入新項目 對話方塊](checkout-and-payment-with-paypal/_static/image3.png)
6. <span data-ttu-id="58d32-163">如往常一般，選取*Site.Master*主版頁面檔案。</span><span class="sxs-lookup"><span data-stu-id="58d32-163">As before, select the *Site.Master* file as the master page.</span></span>
7. <span data-ttu-id="58d32-164">加入下列的其他頁面，以*簽出*資料夾使用上述相同的步驟：</span><span class="sxs-lookup"><span data-stu-id="58d32-164">Add the following additional pages to the *Checkout* folder using the same steps above:</span></span>   

    - <span data-ttu-id="58d32-165">CheckoutReview.aspx</span><span class="sxs-lookup"><span data-stu-id="58d32-165">CheckoutReview.aspx</span></span>
    - <span data-ttu-id="58d32-166">CheckoutComplete.aspx</span><span class="sxs-lookup"><span data-stu-id="58d32-166">CheckoutComplete.aspx</span></span>
    - <span data-ttu-id="58d32-167">CheckoutCancel.aspx</span><span class="sxs-lookup"><span data-stu-id="58d32-167">CheckoutCancel.aspx</span></span>
    - <span data-ttu-id="58d32-168">CheckoutError.aspx</span><span class="sxs-lookup"><span data-stu-id="58d32-168">CheckoutError.aspx</span></span>

### <a name="add-a-webconfig-file"></a><span data-ttu-id="58d32-169">加入 Web.config 檔案</span><span class="sxs-lookup"><span data-stu-id="58d32-169">Add a Web.config File</span></span>

<span data-ttu-id="58d32-170">透過新增*Web.config*檔案*簽出*資料夾中，您將能夠存取限於資料夾中包含的所有頁面。</span><span class="sxs-lookup"><span data-stu-id="58d32-170">By adding a new *Web.config* file to the *Checkout* folder, you will be able to restrict access to all the pages contained in the folder.</span></span>

1. <span data-ttu-id="58d32-171">以滑鼠右鍵按一下*簽出*資料夾，然後選取**新增** - &gt; **新項目**。</span><span class="sxs-lookup"><span data-stu-id="58d32-171">Right-click the *Checkout* folder and select **Add** -&gt; **New Item**.</span></span>  
 <span data-ttu-id="58d32-172">隨即顯示 [ 新增項目] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="58d32-172">The **Add New Item** dialog box is displayed.</span></span>
2. <span data-ttu-id="58d32-173">選取**Visual C#**  - &gt; **Web**左側的 [範本] 群組。</span><span class="sxs-lookup"><span data-stu-id="58d32-173">Select the **Visual C#** -&gt; **Web** templates group on the left.</span></span> <span data-ttu-id="58d32-174">然後從中間窗格中，選取**Web 組態檔**，接受預設名稱*Web.config*，然後選取**新增**。</span><span class="sxs-lookup"><span data-stu-id="58d32-174">Then, from the middle pane, select **Web Configuration File**, accept the default name of *Web.config*, and then select **Add**.</span></span>
3. <span data-ttu-id="58d32-175">取代現有的 XML 內容中*Web.config*以下列檔案：</span><span class="sxs-lookup"><span data-stu-id="58d32-175">Replace the existing XML content in the *Web.config* file with the following:</span></span>  

    [!code-xml[Main](checkout-and-payment-with-paypal/samples/sample4.xml)]
4. <span data-ttu-id="58d32-176">儲存*Web.config*檔案。</span><span class="sxs-lookup"><span data-stu-id="58d32-176">Save the *Web.config* file.</span></span>

<span data-ttu-id="58d32-177">*Web.config*檔案會指定所有未知的使用者的 Web 應用程式必須拒絕存取的頁面中包含*簽出*資料夾。</span><span class="sxs-lookup"><span data-stu-id="58d32-177">The *Web.config* file specifies that all unknown users of the Web application must be denied access to the pages contained in the *Checkout* folder.</span></span> <span data-ttu-id="58d32-178">不過，如果使用者已註冊的帳戶和登入，它們會是已知的使用者，都可存取的網頁*簽出*資料夾。</span><span class="sxs-lookup"><span data-stu-id="58d32-178">However, if the user has registered an account and is logged on, they will be a known user and will have access to the pages in the *Checkout* folder.</span></span>

<span data-ttu-id="58d32-179">請務必注意，ASP.NET 組態如下所示的階層，其中每個*Web.config*檔案適用於組態設定，在其所在的資料夾和所有其下的子目錄。</span><span class="sxs-lookup"><span data-stu-id="58d32-179">It's important to note that ASP.NET configuration follows a hierarchy, where each *Web.config* file applies configuration settings to the folder that it is in and to all of the child directories below it.</span></span>

<a id="SSLWebForms"></a>
## <a name="enable-ssl-for-the-project"></a><span data-ttu-id="58d32-180">專案中啟用 SSL</span><span class="sxs-lookup"><span data-stu-id="58d32-180">Enable SSL for the Project</span></span>

 <span data-ttu-id="58d32-181">安全通訊端層 (SSL) 是定義為允許 Web 伺服器和 Web 用戶端透過加密使用更安全地通訊的通訊協定。</span><span class="sxs-lookup"><span data-stu-id="58d32-181">Secure Sockets Layer (SSL) is a protocol defined to allow Web servers and Web clients to communicate more securely through the use of encryption.</span></span> <span data-ttu-id="58d32-182">不使用 SSL，用戶端與伺服器之間傳送資料時，封包探測實體存取網路的任何人開啟。</span><span class="sxs-lookup"><span data-stu-id="58d32-182">When SSL is not used, data sent between the client and server is open to packet sniffing by anyone with physical access to the network.</span></span> <span data-ttu-id="58d32-183">此外，許多常見的驗證配置並不安全透過一般 HTTP。</span><span class="sxs-lookup"><span data-stu-id="58d32-183">Additionally, several common authentication schemes are not secure over plain HTTP.</span></span> <span data-ttu-id="58d32-184">特別是，基本驗證和表單驗證來傳送未加密的認證。</span><span class="sxs-lookup"><span data-stu-id="58d32-184">In particular, Basic authentication and forms authentication send unencrypted credentials.</span></span> <span data-ttu-id="58d32-185">若要安全的這些驗證配置必須使用 SSL。</span><span class="sxs-lookup"><span data-stu-id="58d32-185">To be secure, these authentication schemes must use SSL.</span></span> 

1. <span data-ttu-id="58d32-186">在**方案總管] 中**，按一下 [ **WingtipToys**專案，然後按下**F4**顯示**屬性**視窗。</span><span class="sxs-lookup"><span data-stu-id="58d32-186">In **Solution Explorer**, click the **WingtipToys** project, then press **F4** to display the **Properties** window.</span></span>
2. <span data-ttu-id="58d32-187">變更**啟用 SSL**至`true`。</span><span class="sxs-lookup"><span data-stu-id="58d32-187">Change **SSL Enabled** to `true`.</span></span>
3. <span data-ttu-id="58d32-188">複製**SSL URL**因此您可以在稍後使用。</span><span class="sxs-lookup"><span data-stu-id="58d32-188">Copy the **SSL URL** so you can use it later.</span></span>   
 <span data-ttu-id="58d32-189">將 SSL URL`https://localhost:44300/`除非您先前建立 SSL 的網站 （如下所示）。</span><span class="sxs-lookup"><span data-stu-id="58d32-189">The SSL URL will be `https://localhost:44300/` unless you've previously created SSL Web Sites (as shown below).</span></span>   
    <span data-ttu-id="58d32-190">![專案屬性](checkout-and-payment-with-paypal/_static/image4.png)</span><span class="sxs-lookup"><span data-stu-id="58d32-190">![Project Properties](checkout-and-payment-with-paypal/_static/image4.png)</span></span>
4. <span data-ttu-id="58d32-191">在**方案總管 中**，以滑鼠右鍵按一下**WingtipToys**專案，然後按一下**屬性**。</span><span class="sxs-lookup"><span data-stu-id="58d32-191">In **Solution Explorer**, right click the **WingtipToys** project and click **Properties**.</span></span>
5. <span data-ttu-id="58d32-192">在左側的索引標籤上，按一下**Web**。</span><span class="sxs-lookup"><span data-stu-id="58d32-192">In the left tab, click **Web**.</span></span>
6. <span data-ttu-id="58d32-193">變更**專案 Url**使用**SSL URL**您稍早儲存。</span><span class="sxs-lookup"><span data-stu-id="58d32-193">Change the **Project Url** to use the **SSL URL** that you saved earlier.</span></span>   
    <span data-ttu-id="58d32-194">![專案 Web 屬性](checkout-and-payment-with-paypal/_static/image5.png)</span><span class="sxs-lookup"><span data-stu-id="58d32-194">![Project Web Properties](checkout-and-payment-with-paypal/_static/image5.png)</span></span>
7. <span data-ttu-id="58d32-195">按下儲存網頁**CTRL + S**。</span><span class="sxs-lookup"><span data-stu-id="58d32-195">Save the page by pressing **CTRL+S**.</span></span>
8. <span data-ttu-id="58d32-196">按**Ctrl + F5**執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="58d32-196">Press **Ctrl+F5** to run the application.</span></span> <span data-ttu-id="58d32-197">Visual Studio 會顯示可讓您避免 SSL 警告的選項。</span><span class="sxs-lookup"><span data-stu-id="58d32-197">Visual Studio will display an option to allow you to avoid SSL warnings.</span></span>
9. <span data-ttu-id="58d32-198">按一下**是**信任 IIS Express SSL 憑證，並繼續。</span><span class="sxs-lookup"><span data-stu-id="58d32-198">Click **Yes** to trust the IIS Express SSL certificate and continue.</span></span>   
    <span data-ttu-id="58d32-199">![IIS Express SSL 憑證的詳細資訊](checkout-and-payment-with-paypal/_static/image6.png)</span><span class="sxs-lookup"><span data-stu-id="58d32-199">![IIS Express SSL certificate details](checkout-and-payment-with-paypal/_static/image6.png)</span></span>  
 <span data-ttu-id="58d32-200">會顯示安全性警告。</span><span class="sxs-lookup"><span data-stu-id="58d32-200">A Security Warning is displayed.</span></span>
10. <span data-ttu-id="58d32-201">按一下**是**將憑證安裝到您的 localhost。</span><span class="sxs-lookup"><span data-stu-id="58d32-201">Click **Yes** to install the certificate to your localhost.</span></span>   
    <span data-ttu-id="58d32-202">![安全性警告對話方塊](checkout-and-payment-with-paypal/_static/image7.png)</span><span class="sxs-lookup"><span data-stu-id="58d32-202">![Security Warning dialog box](checkout-and-payment-with-paypal/_static/image7.png)</span></span>  
 <span data-ttu-id="58d32-203">瀏覽器視窗隨即出現。</span><span class="sxs-lookup"><span data-stu-id="58d32-203">The browser window will be displayed.</span></span>

<span data-ttu-id="58d32-204">您現在可以輕鬆地測試在本機上使用 SSL 的 Web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="58d32-204">You can now easily test your Web application locally using SSL.</span></span>

<a id="OAuthWebForms"></a>
## <a name="add-an-oauth-20-provider"></a><span data-ttu-id="58d32-205">新增的 OAuth 2.0 提供者</span><span class="sxs-lookup"><span data-stu-id="58d32-205">Add an OAuth 2.0 Provider</span></span>

<span data-ttu-id="58d32-206">ASP.NET Web Form 提供增強的成員資格和驗證的選項。</span><span class="sxs-lookup"><span data-stu-id="58d32-206">ASP.NET Web Forms provides enhanced options for membership and authentication.</span></span> <span data-ttu-id="58d32-207">這些增強功能包括 OAuth。</span><span class="sxs-lookup"><span data-stu-id="58d32-207">These enhancements include OAuth.</span></span> <span data-ttu-id="58d32-208">OAuth 是開放的通訊協定，允許使用簡單和標準的方法，從 web、 行動及桌面應用程式安全的授權。</span><span class="sxs-lookup"><span data-stu-id="58d32-208">OAuth is an open protocol that allows secure authorization in a simple and standard method from web, mobile, and desktop applications.</span></span> <span data-ttu-id="58d32-209">ASP.NET Web Form 範本使用 OAuth 來作為驗證提供者會公開 Facebook、 Twitter、 Google 和 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="58d32-209">The ASP.NET Web Forms template uses OAuth to expose Facebook, Twitter, Google and Microsoft as authentication providers.</span></span> <span data-ttu-id="58d32-210">雖然本教學課程會使用僅 Google 做為驗證提供者，您可以輕鬆地修改程式碼以使用任何提供者。</span><span class="sxs-lookup"><span data-stu-id="58d32-210">Although this tutorial uses only Google as the authentication provider, you can easily modify the code to use any of the providers.</span></span> <span data-ttu-id="58d32-211">實作其他提供者的步驟會在本教學課程，您會看到的步驟非常類似。</span><span class="sxs-lookup"><span data-stu-id="58d32-211">The steps to implement other providers are very similar to the steps you will see in this tutorial.</span></span>

<span data-ttu-id="58d32-212">除了驗證，本教學課程也會使用角色來實作授權。</span><span class="sxs-lookup"><span data-stu-id="58d32-212">In addition to authentication, the tutorial will also use roles to implement authorization.</span></span> <span data-ttu-id="58d32-213">只有在您將加入的使用者`canEdit`角色將無法變更資料 （建立、 編輯或刪除連絡人）。</span><span class="sxs-lookup"><span data-stu-id="58d32-213">Only those users you add to the `canEdit` role will be able to change data (create, edit, or delete contacts).</span></span>

> [!NOTE] 
> 
> <span data-ttu-id="58d32-214">Windows Live 應用程式只接受即時工作網站 URL，因此您無法使用本機網站 URL，測試登入。</span><span class="sxs-lookup"><span data-stu-id="58d32-214">Windows Live applications only accept a live URL for a working website, so you cannot use a local website URL for testing logins.</span></span>


<span data-ttu-id="58d32-215">下列步驟可讓您新增 Google 驗證提供者。</span><span class="sxs-lookup"><span data-stu-id="58d32-215">The following steps will allow you to add a Google authentication provider.</span></span>

1. <span data-ttu-id="58d32-216">開啟*應用程式\_Start\Startup.Auth.cs*檔案。</span><span class="sxs-lookup"><span data-stu-id="58d32-216">Open the *App\_Start\Startup.Auth.cs* file.</span></span>
2. <span data-ttu-id="58d32-217">移除註解字元從`app.UseGoogleAuthentication()`方法讓，方法會顯示為如下所示：</span><span class="sxs-lookup"><span data-stu-id="58d32-217">Remove the comment characters from the `app.UseGoogleAuthentication()` method so that the method appears as follows:</span></span> 

    [!code-csharp[Main](checkout-and-payment-with-paypal/samples/sample5.cs)]
3. <span data-ttu-id="58d32-218">瀏覽至[Google 開發人員主控台](https://console.developers.google.com/)。</span><span class="sxs-lookup"><span data-stu-id="58d32-218">Navigate to the [Google Developers Console](https://console.developers.google.com/).</span></span> <span data-ttu-id="58d32-219">您也必須使用您的 Google 開發人員的電子郵件帳戶 (gmail.com) 登入。</span><span class="sxs-lookup"><span data-stu-id="58d32-219">You will also need to sign-in with your Google developer email account (gmail.com).</span></span> <span data-ttu-id="58d32-220">如果您沒有 Google 帳戶，請選取**建立帳戶**連結。</span><span class="sxs-lookup"><span data-stu-id="58d32-220">If you do not have a Google account, select the **Create an account** link.</span></span>   
 <span data-ttu-id="58d32-221">接下來，您會看到**Google 開發人員主控台**。</span><span class="sxs-lookup"><span data-stu-id="58d32-221">Next, you'll see the **Google Developers Console**.</span></span>   
    <span data-ttu-id="58d32-222">![Google 開發人員主控台](checkout-and-payment-with-paypal/_static/image8.png)</span><span class="sxs-lookup"><span data-stu-id="58d32-222">![Google Developers Console](checkout-and-payment-with-paypal/_static/image8.png)</span></span>
4. <span data-ttu-id="58d32-223">按一下**建立專案**按鈕並輸入專案名稱和識別碼 （您可以使用預設值）。</span><span class="sxs-lookup"><span data-stu-id="58d32-223">Click the **Create Project** button and enter a project name and ID (you can use the default values).</span></span> <span data-ttu-id="58d32-224">然後，按一下 **協議 核取方塊**和**建立** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="58d32-224">Then, click the **agreement checkbox** and the **Create** button.</span></span>  

    ![Google-新的專案](checkout-and-payment-with-paypal/_static/image9.png)

 <span data-ttu-id="58d32-226">幾分鐘後將會建立新的專案，您的瀏覽器會顯示新的 [專案] 頁面。</span><span class="sxs-lookup"><span data-stu-id="58d32-226">In a few seconds the new project will be created and your browser will display the new projects page.</span></span>
5. <span data-ttu-id="58d32-227">在左側的索引標籤上，按一下**Api &amp; auth**，然後按一下 **認證**。</span><span class="sxs-lookup"><span data-stu-id="58d32-227">In the left tab, click **APIs &amp; auth**, and then click **Credentials**.</span></span>
6. <span data-ttu-id="58d32-228">按一下**建立新的用戶端識別碼**下**OAuth**。</span><span class="sxs-lookup"><span data-stu-id="58d32-228">Click the **Create New Client ID** under **OAuth**.</span></span>   
 <span data-ttu-id="58d32-229">**建立用戶端識別碼**對話方塊隨即出現。</span><span class="sxs-lookup"><span data-stu-id="58d32-229">The **Create Client ID** dialog will be displayed.</span></span>   
    <span data-ttu-id="58d32-230">![Google-建立用戶端識別碼](checkout-and-payment-with-paypal/_static/image10.png)</span><span class="sxs-lookup"><span data-stu-id="58d32-230">![Google - Create Client ID](checkout-and-payment-with-paypal/_static/image10.png)</span></span>
7. <span data-ttu-id="58d32-231">在**建立用戶端識別碼** 對話方塊中，保留預設值**Web 應用程式**應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="58d32-231">In the **Create Client ID** dialog, keep the default **Web application** for the application type.</span></span>
8. <span data-ttu-id="58d32-232">設定**授權 JavaScript Origins**您稍早在本教學課程中使用的 SSL url (`https://localhost:44300/`除非您已建立其他 SSL 專案)。</span><span class="sxs-lookup"><span data-stu-id="58d32-232">Set the **Authorized JavaScript Origins** to the SSL URL you used earlier in this tutorial (`https://localhost:44300/` unless you've created other SSL projects).</span></span>   
 <span data-ttu-id="58d32-233">此 URL 是您的應用程式的原點。</span><span class="sxs-lookup"><span data-stu-id="58d32-233">This URL is the origin for your application.</span></span> <span data-ttu-id="58d32-234">此範例中，您只能將輸入 localhost 測試 URL。</span><span class="sxs-lookup"><span data-stu-id="58d32-234">For this sample, you will only enter the localhost test URL.</span></span> <span data-ttu-id="58d32-235">不過，您可以輸入 localhost 和生產環境的多個 Url。</span><span class="sxs-lookup"><span data-stu-id="58d32-235">However, you can enter multiple URLs to account for localhost and production.</span></span>
9. <span data-ttu-id="58d32-236">設定**授權重新導向 URI**如下：</span><span class="sxs-lookup"><span data-stu-id="58d32-236">Set the **Authorized Redirect URI** to the following:</span></span> 

    [!code-html[Main](checkout-and-payment-with-paypal/samples/sample6.html)]

 <span data-ttu-id="58d32-237">此值為該 ASP.NET OAuth 的 URI 來與 google OAuth 伺服器通訊的使用者。</span><span class="sxs-lookup"><span data-stu-id="58d32-237">This value is the URI that ASP.NET OAuth users to communicate with the google OAuth server.</span></span> <span data-ttu-id="58d32-238">請記住您在上面使用的 SSL URL (`https://localhost:44300/`除非您已建立其他 SSL 專案)。</span><span class="sxs-lookup"><span data-stu-id="58d32-238">Remember the SSL URL you used above (    `https://localhost:44300/` unless you've created other SSL projects).</span></span>
10. <span data-ttu-id="58d32-239">按一下**建立用戶端識別碼** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="58d32-239">Click the **Create Client ID** button.</span></span>
11. <span data-ttu-id="58d32-240">Google 開發人員主控台的左窗格中，按一下 **同意畫面**功能表項目，然後設定您的電子郵件地址和產品名稱。</span><span class="sxs-lookup"><span data-stu-id="58d32-240">On the left menu of the Google Developers Console, click the **Consent screen** menu item, then set your email address and product name.</span></span> <span data-ttu-id="58d32-241">當您完成表單時，按一下 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="58d32-241">When you have completed the form, click **Save**.</span></span>
12. <span data-ttu-id="58d32-242">按一下**Api**功能表項目，向下的捲動並按一下**關閉**旁邊**Google + API**。</span><span class="sxs-lookup"><span data-stu-id="58d32-242">Click the **APIs** menu item, scroll down and click the **off** button next to **Google+ API**.</span></span>   
 <span data-ttu-id="58d32-243">接受此選項會啟用 Google + API。</span><span class="sxs-lookup"><span data-stu-id="58d32-243">Accepting this option will enable the Google+ API.</span></span>
13. <span data-ttu-id="58d32-244">您也必須更新**Microsoft.Owin** 3.0.0 版本的 NuGet 封裝。</span><span class="sxs-lookup"><span data-stu-id="58d32-244">You must also update the **Microsoft.Owin** NuGet package to version 3.0.0.</span></span>   
 <span data-ttu-id="58d32-245">從**工具**功能表上，選取**NuGet 套件管理員**，然後選取 **管理方案的 NuGet 套件**。</span><span class="sxs-lookup"><span data-stu-id="58d32-245">From the **Tools** menu, select **NuGet Package Manager** and then select **Manage NuGet Packages for Solution**.</span></span>  
 <span data-ttu-id="58d32-246">從**管理 NuGet 封裝** 視窗中，尋找及更新**Microsoft.Owin** 3.0.0 版本的封裝。</span><span class="sxs-lookup"><span data-stu-id="58d32-246">From the **Manage NuGet Packages** window, find and update the **Microsoft.Owin** package to version 3.0.0.</span></span>
14. <span data-ttu-id="58d32-247">在 Visual Studio 中，更新`UseGoogleAuthentication`方法*Startup.Auth.cs*複製及貼上頁面**用戶端識別碼**和**用戶端密碼**至方法。</span><span class="sxs-lookup"><span data-stu-id="58d32-247">In Visual Studio, update the `UseGoogleAuthentication` method of the *Startup.Auth.cs* page by copying and pasting the **Client ID** and **Client Secret** into the method.</span></span> <span data-ttu-id="58d32-248">**用戶端識別碼**和**用戶端密碼**值如下所示的範例，將無法運作。</span><span class="sxs-lookup"><span data-stu-id="58d32-248">The **Client ID** and **Client Secret** values shown below are samples and will not work.</span></span> 

    [!code-csharp[Main](checkout-and-payment-with-paypal/samples/sample7.cs?highlight=64-65)]
15. <span data-ttu-id="58d32-249">按**CTRL + F5**建置並執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="58d32-249">Press **CTRL+F5** to build and run the application.</span></span> <span data-ttu-id="58d32-250">按一下**登入**連結。</span><span class="sxs-lookup"><span data-stu-id="58d32-250">Click the **Log in** link.</span></span>
16. <span data-ttu-id="58d32-251">在下**使用另一個服務登入**，按一下  **Google**。</span><span class="sxs-lookup"><span data-stu-id="58d32-251">Under **Use another service to log in**, click **Google**.</span></span>  
    <span data-ttu-id="58d32-252">![登入](checkout-and-payment-with-paypal/_static/image11.png)</span><span class="sxs-lookup"><span data-stu-id="58d32-252">![Log in](checkout-and-payment-with-paypal/_static/image11.png)</span></span>
17. <span data-ttu-id="58d32-253">如果您需要輸入您的認證，您將會重新導向至 google 站台，您將在其中輸入您的認證。</span><span class="sxs-lookup"><span data-stu-id="58d32-253">If you need to enter your credentials, you will be redirected to the google site where you will enter your credentials.</span></span>  
    ![Google-登入](checkout-and-payment-with-paypal/_static/image12.png)
18. <span data-ttu-id="58d32-255">輸入您的認證之後，系統會提示您授與您剛才建立的 web 應用程式的權限。</span><span class="sxs-lookup"><span data-stu-id="58d32-255">After you enter your credentials, you will be prompted to give permissions to the web application you just created.</span></span>  
    ![專案預設服務帳戶](checkout-and-payment-with-paypal/_static/image13.png)
19. <span data-ttu-id="58d32-257">按一下**接受**。</span><span class="sxs-lookup"><span data-stu-id="58d32-257">Click **Accept**.</span></span> <span data-ttu-id="58d32-258">您將會被重新導向至**註冊**頁面**WingtipToys**應用程式，您可以在其中註冊您的 Google 帳戶。</span><span class="sxs-lookup"><span data-stu-id="58d32-258">You will now be redirected back to the **Register** page of the **WingtipToys** application where you can register your Google account.</span></span>  
    <span data-ttu-id="58d32-259">![向您的 Google 帳戶](checkout-and-payment-with-paypal/_static/image14.png)</span><span class="sxs-lookup"><span data-stu-id="58d32-259">![Register with your Google Account](checkout-and-payment-with-paypal/_static/image14.png)</span></span>
20. <span data-ttu-id="58d32-260">您可以選擇變更為您的 Gmail 帳戶所使用的本機電子郵件註冊名稱，但您通常想要保留的預設電子郵件別名 （也就是一個用來驗證）。</span><span class="sxs-lookup"><span data-stu-id="58d32-260">You have the option of changing the local email registration name used for your Gmail account, but you generally want to keep the default email alias (that is, the one you used for authentication).</span></span> <span data-ttu-id="58d32-261">按一下**登入**如上所示。</span><span class="sxs-lookup"><span data-stu-id="58d32-261">Click **Log in** as shown above.</span></span>

### <a name="modifying-login-functionality"></a><span data-ttu-id="58d32-262">修改登入功能</span><span class="sxs-lookup"><span data-stu-id="58d32-262">Modifying Login Functionality</span></span>

<span data-ttu-id="58d32-263">如先前所述在此教學課程中，大部分的使用者註冊功能已包含在 ASP.NET Web Form 範本預設。</span><span class="sxs-lookup"><span data-stu-id="58d32-263">As previously mentioned in this tutorial series, much of the user registration functionality has been included in the ASP.NET Web Forms template by default.</span></span> <span data-ttu-id="58d32-264">現在您將修改預設*Login.aspx*和*Register.aspx*頁面來呼叫`MigrateCart`方法。</span><span class="sxs-lookup"><span data-stu-id="58d32-264">Now you will modify the default *Login.aspx* and *Register.aspx* pages to call the `MigrateCart` method.</span></span> <span data-ttu-id="58d32-265">`MigrateCart`方法關聯匿名的購物車中的新登入的使用者。</span><span class="sxs-lookup"><span data-stu-id="58d32-265">The `MigrateCart` method associates a newly logged in user with an anonymous shopping cart.</span></span> <span data-ttu-id="58d32-266">藉由建立關聯的使用者和購物車，Wingtip Toys 範例應用程式將能夠維護購物車之間瀏覽的使用者。</span><span class="sxs-lookup"><span data-stu-id="58d32-266">By associating the user and shopping cart, the Wingtip Toys sample application will be able to maintain the shopping cart of the user between visits.</span></span>

1. <span data-ttu-id="58d32-267">在**方案總管 中**、 尋找和開啟*帳戶*資料夾。</span><span class="sxs-lookup"><span data-stu-id="58d32-267">In **Solution Explorer**, find and open the *Account* folder.</span></span>
2. <span data-ttu-id="58d32-268">修改程式碼後置頁面，名為*Login.aspx.cs*包含以黃色反白顯示的程式碼，使其顯示，如下所示：</span><span class="sxs-lookup"><span data-stu-id="58d32-268">Modify the code-behind page named *Login.aspx.cs* to include the code highlighted in yellow, so that it appears as follows:</span></span>   

    [!code-csharp[Main](checkout-and-payment-with-paypal/samples/sample8.cs?highlight=41-43)]
3. <span data-ttu-id="58d32-269">儲存*Login.aspx.cs*檔案。</span><span class="sxs-lookup"><span data-stu-id="58d32-269">Save the *Login.aspx.cs* file.</span></span>

<span data-ttu-id="58d32-270">現在，您可以忽略沒有定義的警告`MigrateCart`方法。</span><span class="sxs-lookup"><span data-stu-id="58d32-270">For now, you can ignore the warning that there is no definition for the `MigrateCart` method.</span></span> <span data-ttu-id="58d32-271">您將加入它稍後在本教學課程。</span><span class="sxs-lookup"><span data-stu-id="58d32-271">You will be adding it a bit later in this tutorial.</span></span>

<span data-ttu-id="58d32-272">*Login.aspx.cs*支援登入方法的程式碼後置檔案。</span><span class="sxs-lookup"><span data-stu-id="58d32-272">The *Login.aspx.cs* code-behind file supports a LogIn method.</span></span> <span data-ttu-id="58d32-273">藉由檢查 Login.aspx 頁面，您會看到此頁面包含的 「 登入 」 按鈕，當按一下 觸發程序`LogIn`上程式碼後置處理常式。</span><span class="sxs-lookup"><span data-stu-id="58d32-273">By inspecting the Login.aspx page, you'll see that this page includes a "Log in" button that when click triggers the `LogIn` handler on the code-behind.</span></span>

<span data-ttu-id="58d32-274">當`Login`方法*Login.aspx.cs*會呼叫名為購物籃中的新執行個體`usersShoppingCart`建立。</span><span class="sxs-lookup"><span data-stu-id="58d32-274">When the `Login` method on the *Login.aspx.cs* is called, a new instance of the shopping cart named `usersShoppingCart` is created.</span></span> <span data-ttu-id="58d32-275">擷取和設定為購物車 (GUID) 識別碼`cartId`變數。</span><span class="sxs-lookup"><span data-stu-id="58d32-275">The ID of the shopping cart (a GUID) is retrieved and set to the `cartId` variable.</span></span> <span data-ttu-id="58d32-276">然後，`MigrateCart`呼叫方法時，傳遞兩者`cartId`和登入的使用者對這個方法的名稱。</span><span class="sxs-lookup"><span data-stu-id="58d32-276">Then, the `MigrateCart` method is called, passing both the `cartId` and the name of the logged-in user to this method.</span></span> <span data-ttu-id="58d32-277">購物車移轉時，用來識別匿名的購物車的 GUID 會取代使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="58d32-277">When the shopping cart is migrated, the GUID used to identify the anonymous shopping cart is replaced with the user name.</span></span>

<span data-ttu-id="58d32-278">除了修改*Login.aspx.cs*程式碼後置檔案，以移轉購物車，當使用者登入，您也必須修改*Register.aspx.cs 程式碼後置檔案*移轉購物車當使用者建立新的帳戶，登入。</span><span class="sxs-lookup"><span data-stu-id="58d32-278">In addition to modifying the *Login.aspx.cs* code-behind file to migrate the shopping cart when the user logs in, you must also modify the *Register.aspx.cs code-behind file* to migrate the shopping cart when the user creates a new account and logs in.</span></span>

1. <span data-ttu-id="58d32-279">在*帳戶*資料夾中，開啟的程式碼後置檔案命名為*Register.aspx.cs*。</span><span class="sxs-lookup"><span data-stu-id="58d32-279">In the *Account* folder, open the code-behind file named *Register.aspx.cs*.</span></span>
2. <span data-ttu-id="58d32-280">修改包含的程式碼以黃色，程式碼後置檔案，使其顯示，如下所示：</span><span class="sxs-lookup"><span data-stu-id="58d32-280">Modify the code-behind file by including the code in yellow, so that it appears as follows:</span></span>   

    [!code-csharp[Main](checkout-and-payment-with-paypal/samples/sample9.cs?highlight=28-32)]
3. <span data-ttu-id="58d32-281">儲存*Register.aspx.cs*檔案。</span><span class="sxs-lookup"><span data-stu-id="58d32-281">Save the *Register.aspx.cs* file.</span></span> <span data-ttu-id="58d32-282">同樣地，忽略此警告關於`MigrateCart`方法。</span><span class="sxs-lookup"><span data-stu-id="58d32-282">Once again, ignore the warning about the `MigrateCart` method.</span></span>

<span data-ttu-id="58d32-283">請注意程式碼中所使用`CreateUser_Click`事件處理常式是非常類似的程式碼中使用`LogIn`方法。</span><span class="sxs-lookup"><span data-stu-id="58d32-283">Notice that the code you used in the `CreateUser_Click` event handler is very similar to the code you used in the `LogIn` method.</span></span> <span data-ttu-id="58d32-284">當使用者註冊或登入站台，呼叫`MigrateCart`方法不會進行。</span><span class="sxs-lookup"><span data-stu-id="58d32-284">When the user registers or logs in to the site, a call to the `MigrateCart` method will be made.</span></span>

## <a name="migrating-the-shopping-cart"></a><span data-ttu-id="58d32-285">移轉購物車</span><span class="sxs-lookup"><span data-stu-id="58d32-285">Migrating the Shopping Cart</span></span>

<span data-ttu-id="58d32-286">有更新的登入和註冊程序之後，您可以加入購物車使用移轉程式碼`MigrateCart`方法。</span><span class="sxs-lookup"><span data-stu-id="58d32-286">Now that you have the log-in and registration process updated, you can add the code to migrate the shopping cart using the `MigrateCart` method.</span></span>

1. <span data-ttu-id="58d32-287">在**方案總管 中**，尋找*邏輯*資料夾，然後開啟*ShoppingCartActions.cs*類別檔案。</span><span class="sxs-lookup"><span data-stu-id="58d32-287">In **Solution Explorer**, find the *Logic* folder and open the *ShoppingCartActions.cs* class file.</span></span>
2. <span data-ttu-id="58d32-288">加入程式碼中的現有程式碼以黃色反白顯示*ShoppingCartActions.cs*檔案，以便中的程式碼*ShoppingCartActions.cs*檔案會出現，如下所示：</span><span class="sxs-lookup"><span data-stu-id="58d32-288">Add the code highlighted in yellow to the existing code in the *ShoppingCartActions.cs* file, so that the code in the *ShoppingCartActions.cs* file appears as follows:</span></span>   

    [!code-csharp[Main](checkout-and-payment-with-paypal/samples/sample10.cs?highlight=215-224)]

<span data-ttu-id="58d32-289">`MigrateCart`方法用來尋找使用者的購物車的現有 cartId。</span><span class="sxs-lookup"><span data-stu-id="58d32-289">The `MigrateCart` method uses the existing cartId to find the shopping cart of the user.</span></span> <span data-ttu-id="58d32-290">接下來，此程式碼所有的購物車項目間執行迴圈，並取代`CartId`屬性 (依照`CartItem`結構描述) 的登入的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="58d32-290">Next, the code loops through all the shopping cart items and replaces the `CartId` property (as specified by the `CartItem` schema) with the logged-in user name.</span></span>

### <a name="updating-the-database-connection"></a><span data-ttu-id="58d32-291">更新資料庫連接</span><span class="sxs-lookup"><span data-stu-id="58d32-291">Updating the Database Connection</span></span>

<span data-ttu-id="58d32-292">如果您要遵照這個教學課程使用**預先建置**Wingtip Toys 範例應用程式，您必須重新建立的預設成員資格資料庫。</span><span class="sxs-lookup"><span data-stu-id="58d32-292">If you are following this tutorial using the **prebuilt** Wingtip Toys sample application, you must recreate the default membership database.</span></span> <span data-ttu-id="58d32-293">藉由修改預設的連接字串，成員資格資料庫將會建立的下次執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="58d32-293">By modifying the default connection string, the membership database will be created the next time the application runs.</span></span>

1. <span data-ttu-id="58d32-294">開啟*Web.config*專案根目錄的檔案。</span><span class="sxs-lookup"><span data-stu-id="58d32-294">Open the *Web.config* file at the root of the project.</span></span>
2. <span data-ttu-id="58d32-295">更新預設的連接字串，使其顯示，如下所示：</span><span class="sxs-lookup"><span data-stu-id="58d32-295">Update the default connection string so that it appears as follows:</span></span>   

    [!code-xml[Main](checkout-and-payment-with-paypal/samples/sample11.xml)]

<a id="PayPalWebForms"></a>
## <a name="integrating-paypal"></a><span data-ttu-id="58d32-296">將 PayPal 整合</span><span class="sxs-lookup"><span data-stu-id="58d32-296">Integrating PayPal</span></span>

<span data-ttu-id="58d32-297">PayPal 是網頁型計費平台可接受的線上商家付款。</span><span class="sxs-lookup"><span data-stu-id="58d32-297">PayPal is a web-based billing platform that accepts payments by online merchants.</span></span> <span data-ttu-id="58d32-298">本教學課程接下來會說明如何將 PayPal Express 簽出功能整合到您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="58d32-298">This tutorial next explains how to integrate PayPal's Express Checkout functionality into your application.</span></span> <span data-ttu-id="58d32-299">Express 簽出可讓您的客戶使用 PayPal 支付它們新增至購物車的項目。</span><span class="sxs-lookup"><span data-stu-id="58d32-299">Express Checkout allows your customers to use PayPal to pay for the items they have added to their shopping cart.</span></span>

### <a name="create-paylpal-test-accounts"></a><span data-ttu-id="58d32-300">建立 PaylPal 測試帳戶</span><span class="sxs-lookup"><span data-stu-id="58d32-300">Create PaylPal Test Accounts</span></span>

<span data-ttu-id="58d32-301">若要使用測試環境的 PayPal，您必須建立並確認測試開發人員帳戶。</span><span class="sxs-lookup"><span data-stu-id="58d32-301">To use the PayPal testing environment, you must create and verify a developer test account.</span></span> <span data-ttu-id="58d32-302">若要建立買方測試帳戶和賣方測試帳戶，您將使用開發人員測試帳戶。</span><span class="sxs-lookup"><span data-stu-id="58d32-302">You will use the developer test account to create a buyer test account and a seller test account.</span></span> <span data-ttu-id="58d32-303">開發人員測試帳戶認證也會讓 Wingtip Toys 範例應用程式存取 PayPal 測試環境。</span><span class="sxs-lookup"><span data-stu-id="58d32-303">The developer test account credentials also will allow the Wingtip Toys sample application to access the PayPal testing environment.</span></span>

1. <span data-ttu-id="58d32-304">在瀏覽器中，瀏覽至 PayPal 開發人員網站測試：</span><span class="sxs-lookup"><span data-stu-id="58d32-304">In a browser, navigate to the PayPal developer testing site:</span></span>   
    [<span data-ttu-id="58d32-305">https://developer.paypal.com</span><span class="sxs-lookup"><span data-stu-id="58d32-305">https://developer.paypal.com</span></span>](https://developer.paypal.com/)
2. <span data-ttu-id="58d32-306">如果您沒有 PayPal 開發人員帳戶，建立新帳戶，即可**註冊**並遵循的步驟登入。</span><span class="sxs-lookup"><span data-stu-id="58d32-306">If you don't have a PayPal developer account, create a new account by clicking **Sign Up**and following the sign up steps.</span></span> <span data-ttu-id="58d32-307">如果您有現有的 PayPal 開發人員帳戶，登入即可**登入**。</span><span class="sxs-lookup"><span data-stu-id="58d32-307">If you have an existing PayPal developer account, sign in by clicking **Log In**.</span></span> <span data-ttu-id="58d32-308">您必須測試 Wingtip Toys 範例應用程式，稍後在本教學課程 PayPal 開發人員帳戶。</span><span class="sxs-lookup"><span data-stu-id="58d32-308">You will need your PayPal developer account to test the Wingtip Toys sample application later in this tutorial.</span></span>
3. <span data-ttu-id="58d32-309">如果您只要已註冊 PayPal 開發人員帳戶，您可能需要驗證您的 PayPal PayPal 開發人員帳戶。</span><span class="sxs-lookup"><span data-stu-id="58d32-309">If you have just signed up for your PayPal developer account, you may need to verify your PayPal developer account with PayPal.</span></span> <span data-ttu-id="58d32-310">您可以依照 PayPal 傳送電子郵件帳戶的步驟來確認您的帳戶。</span><span class="sxs-lookup"><span data-stu-id="58d32-310">You can verify your account by following the steps that PayPal sent to your email account.</span></span> <span data-ttu-id="58d32-311">一旦確認 PayPal 開發人員帳戶，登入 PayPal 開發人員網站測試。</span><span class="sxs-lookup"><span data-stu-id="58d32-311">Once you have verified your PayPal developer account, log back into the PayPal developer testing site.</span></span>
4. <span data-ttu-id="58d32-312">您登入 PayPal 開發人員網站與您要建立 PayPal 買方測試帳戶，如果您已經沒有 PayPal 開發人員帳戶之後有一個。</span><span class="sxs-lookup"><span data-stu-id="58d32-312">After you are logged in to the PayPal developer site with your PayPal developer account you need to create a PayPal buyer test account if you don't already have one.</span></span> <span data-ttu-id="58d32-313">若要建立買方測試帳戶、 PayPal 網站按一下**應用程式**索引標籤，然後按一下 **沙箱帳戶**。</span><span class="sxs-lookup"><span data-stu-id="58d32-313">To create a buyer test account, on the PayPal site click the **Applications** tab and then click **Sandbox accounts**.</span></span>   
 <span data-ttu-id="58d32-314">**沙箱測試帳戶**頁面隨即顯示。</span><span class="sxs-lookup"><span data-stu-id="58d32-314">The **Sandbox test accounts** page is shown.</span></span>   

    > [!NOTE] 
    > 
    > <span data-ttu-id="58d32-315">PayPal 開發人員網站已提供商家測試帳戶。</span><span class="sxs-lookup"><span data-stu-id="58d32-315">The PayPal Developer site already provides a merchant test account.</span></span>

    ![簽出和 PayPal-沙箱測試帳戶與付款](checkout-and-payment-with-paypal/_static/image15.png)
5. <span data-ttu-id="58d32-317">在沙箱測試的 帳戶 頁面中，按一下 **建立帳戶**。</span><span class="sxs-lookup"><span data-stu-id="58d32-317">On the Sandbox test accounts page, click **Create Account**.</span></span>
6. <span data-ttu-id="58d32-318">在**建立測試帳戶**頁面上選擇買方測試帳戶電子郵件和您選擇的密碼。</span><span class="sxs-lookup"><span data-stu-id="58d32-318">On the **Create test account** page choose a buyer test account email and password of your choice.</span></span>   

    > [!NOTE] 
    > 
    > <span data-ttu-id="58d32-319">您必須購買者的電子郵件地址和密碼才能測試 Wingtip Toys 範例應用程式，在本教學課程結尾處。</span><span class="sxs-lookup"><span data-stu-id="58d32-319">You will need the buyer email addresses and password to test the Wingtip Toys sample application at the end of this tutorial.</span></span>

    ![簽出和 PayPal-沙箱測試帳戶與付款](checkout-and-payment-with-paypal/_static/image16.png)
7. <span data-ttu-id="58d32-321">按一下 [建立買方測試帳戶**建立帳戶**] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="58d32-321">Create the buyer test account by clicking the **Create Account** button.</span></span>  
 <span data-ttu-id="58d32-322">**沙箱測試帳戶**頁面隨即顯示。</span><span class="sxs-lookup"><span data-stu-id="58d32-322">The **Sandbox Test accounts** page is displayed.</span></span> 

    ![簽出和 PayPal-PaylPal 帳戶與付款](checkout-and-payment-with-paypal/_static/image17.png)
8. <span data-ttu-id="58d32-324">在**沙箱測試帳戶**頁面上，按一下**促進**電子郵件帳戶。</span><span class="sxs-lookup"><span data-stu-id="58d32-324">On the **Sandbox test accounts** page, click the **facilitator** email account.</span></span>  
    <span data-ttu-id="58d32-325">**設定檔**和**通知**選項會出現。</span><span class="sxs-lookup"><span data-stu-id="58d32-325">**Profile** and **Notification** options appear.</span></span>
9. <span data-ttu-id="58d32-326">選取**設定檔**選項，然後按一下  **API 認證**檢視 API 商家測試帳戶的認證。</span><span class="sxs-lookup"><span data-stu-id="58d32-326">Select the **Profile** option, then click **API credentials** to view your API credentials for the merchant test account.</span></span>
10. <span data-ttu-id="58d32-327">將測試 API 認證複製到 [記事本]。</span><span class="sxs-lookup"><span data-stu-id="58d32-327">Copy the TEST API credentials to notepad.</span></span>

<span data-ttu-id="58d32-328">您必須顯示傳統測試 API 認證 （使用者名稱、 密碼和簽章） 進行 API 呼叫，Wingtip Toys 範例應用程式從測試環境的 PayPal。</span><span class="sxs-lookup"><span data-stu-id="58d32-328">You will need your displayed Classic TEST API credentials (Username, Password, and Signature) to make API calls from the Wingtip Toys sample application to the PayPal testing environment.</span></span> <span data-ttu-id="58d32-329">您將在下一個步驟中加入認證。</span><span class="sxs-lookup"><span data-stu-id="58d32-329">You will add the credentials in the next step.</span></span>

### <a name="add-paypal-class-and-api-credentials"></a><span data-ttu-id="58d32-330">加入 PayPal 類別和應用程式開發介面的認證</span><span class="sxs-lookup"><span data-stu-id="58d32-330">Add PayPal Class and API Credentials</span></span>

<span data-ttu-id="58d32-331">您會將大部分的 PayPal 程式碼為單一類別。</span><span class="sxs-lookup"><span data-stu-id="58d32-331">You will place the majority of the PayPal code into a single class.</span></span> <span data-ttu-id="58d32-332">這個類別包含用來與 PayPal 通訊的方法。</span><span class="sxs-lookup"><span data-stu-id="58d32-332">This class contains the methods used to communicate with PayPal.</span></span> <span data-ttu-id="58d32-333">此外，您將這個類別加入您 PayPal 的認證。</span><span class="sxs-lookup"><span data-stu-id="58d32-333">Also, you will add your PayPal credentials to this class.</span></span>

1. <span data-ttu-id="58d32-334">在 Visual Studio 內 Wingtip Toys 範例應用程式，以滑鼠右鍵按一下**邏輯**資料夾，然後選取**新增** - &gt; **新項目**。</span><span class="sxs-lookup"><span data-stu-id="58d32-334">In the Wingtip Toys sample application within Visual Studio, right-click the **Logic** folder and then select **Add** -&gt; **New Item**.</span></span>   
 <span data-ttu-id="58d32-335">隨即顯示 [ 新增項目] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="58d32-335">The **Add New Item** dialog box is displayed.</span></span>
2. <span data-ttu-id="58d32-336">在下**Visual C#**從**已安裝**左邊的窗格，選取**程式碼**。</span><span class="sxs-lookup"><span data-stu-id="58d32-336">Under **Visual C#** from the **Installed** pane on the left, select **Code**.</span></span>
3. <span data-ttu-id="58d32-337">從中間窗格中，選取**類別**。</span><span class="sxs-lookup"><span data-stu-id="58d32-337">From the middle pane, select **Class**.</span></span> <span data-ttu-id="58d32-338">這個新類別命名**PayPalFunctions.cs**。</span><span class="sxs-lookup"><span data-stu-id="58d32-338">Name this new class **PayPalFunctions.cs**.</span></span>
4. <span data-ttu-id="58d32-339">按一下 [加入] 。</span><span class="sxs-lookup"><span data-stu-id="58d32-339">Click **Add**.</span></span>  
 <span data-ttu-id="58d32-340">在編輯器中，會顯示新的類別檔案。</span><span class="sxs-lookup"><span data-stu-id="58d32-340">The new class file is displayed in the editor.</span></span>
5. <span data-ttu-id="58d32-341">下列程式碼取代預設程式碼：</span><span class="sxs-lookup"><span data-stu-id="58d32-341">Replace the default code with the following code:</span></span>  

    [!code-csharp[Main](checkout-and-payment-with-paypal/samples/sample12.cs)]
6. <span data-ttu-id="58d32-342">新增您稍早在本教學課程中，讓您可以函式呼叫 PayPal 測試環境來顯示商店 API 認證 （使用者名稱、 密碼和簽章）。</span><span class="sxs-lookup"><span data-stu-id="58d32-342">Add the Merchant API credentials (Username, Password, and Signature) that you displayed earlier in this tutorial so that you can make function calls to the PayPal testing environment.</span></span>  

    [!code-csharp[Main](checkout-and-payment-with-paypal/samples/sample13.cs)]

> [!NOTE] 
> 
> <span data-ttu-id="58d32-343">在此範例應用程式只會將認證加入至 C# 檔案 (.cs)。</span><span class="sxs-lookup"><span data-stu-id="58d32-343">In this sample application you are simply adding credentials to a C# file (.cs).</span></span> <span data-ttu-id="58d32-344">不過，在實作解決方案中，您應該考慮加密您在組態檔中的認證。</span><span class="sxs-lookup"><span data-stu-id="58d32-344">However, in a implemented solution, you should consider encrypting your credentials in a configuration file.</span></span>


<span data-ttu-id="58d32-345">NVPAPICaller 類別包含大部分的 PayPal 功能。</span><span class="sxs-lookup"><span data-stu-id="58d32-345">The NVPAPICaller class contains the majority of the PayPal functionality.</span></span> <span data-ttu-id="58d32-346">類別中的程式碼可進行購買 PayPal 測試環境的測試所需的方法。</span><span class="sxs-lookup"><span data-stu-id="58d32-346">The code in the class provides the methods needed to make a test purchase from the PayPal testing environment.</span></span> <span data-ttu-id="58d32-347">下列三個 PayPal 函式用來進行購買：</span><span class="sxs-lookup"><span data-stu-id="58d32-347">The following three PayPal functions are used to make purchases:</span></span>

- <span data-ttu-id="58d32-348">`SetExpressCheckout`函式</span><span class="sxs-lookup"><span data-stu-id="58d32-348">`SetExpressCheckout` function</span></span>
- <span data-ttu-id="58d32-349">`GetExpressCheckoutDetails`函式</span><span class="sxs-lookup"><span data-stu-id="58d32-349">`GetExpressCheckoutDetails` function</span></span>
- <span data-ttu-id="58d32-350">`DoExpressCheckoutPayment`函式</span><span class="sxs-lookup"><span data-stu-id="58d32-350">`DoExpressCheckoutPayment` function</span></span>

<span data-ttu-id="58d32-351">`ShortcutExpressCheckout`方法會測試採購資訊與產品詳細資料收集從購物車和呼叫`SetExpressCheckout`PayPal 函式。</span><span class="sxs-lookup"><span data-stu-id="58d32-351">The `ShortcutExpressCheckout` method collects the test purchase information and product details from the shopping cart and calls the `SetExpressCheckout` PayPal function.</span></span> <span data-ttu-id="58d32-352">`GetCheckoutDetails`方法確認採購詳細資料，並呼叫`GetExpressCheckoutDetails`之前測試購買 PayPal 函式。</span><span class="sxs-lookup"><span data-stu-id="58d32-352">The `GetCheckoutDetails` method confirms purchase details and calls the `GetExpressCheckoutDetails` PayPal function before making the test purchase.</span></span> <span data-ttu-id="58d32-353">`DoCheckoutPayment`方法呼叫來完成從測試環境的測試購買`DoExpressCheckoutPayment`PayPal 函式。</span><span class="sxs-lookup"><span data-stu-id="58d32-353">The `DoCheckoutPayment` method completes the test purchase from the testing environment by calling the `DoExpressCheckoutPayment` PayPal function.</span></span> <span data-ttu-id="58d32-354">其餘的程式碼支援的 PayPal 方法和處理程序，例如字串的編碼方式、 解碼的字串、 處理陣列，以及決定認證。</span><span class="sxs-lookup"><span data-stu-id="58d32-354">The remaining code supports the PayPal methods and process, such as encoding strings, decoding strings, processing arrays, and determining credentials.</span></span>

> [!NOTE] 
> 
> <span data-ttu-id="58d32-355">PayPal 可讓您包含選擇性的採購單詳細資料，根據[PayPal 的 API 規格](https://cms.paypal.com/us/cgi-bin/?cmd=_render-content&amp;content_ID=developer/e_howto_api_nvp_r_SetExpressCheckout)。</span><span class="sxs-lookup"><span data-stu-id="58d32-355">PayPal allows you to include optional purchase details based on [PayPal's API specification](https://cms.paypal.com/us/cgi-bin/?cmd=_render-content&amp;content_ID=developer/e_howto_api_nvp_r_SetExpressCheckout).</span></span> <span data-ttu-id="58d32-356">您可以藉由擴充 Wingtip Toys 範例應用程式中的程式碼，包含當地語系化的詳細資料、 產品描述、 稅金、 客戶服務編號，以及許多其他選擇性欄位。</span><span class="sxs-lookup"><span data-stu-id="58d32-356">By extending the code in the Wingtip Toys sample application, you can include localization details, product descriptions, tax, a customer service number, as well as many other optional fields.</span></span>


<span data-ttu-id="58d32-357">請注意，傳回和 [取消] Url 中指定的**ShortcutExpressCheckout**方法使用的通訊埠編號。</span><span class="sxs-lookup"><span data-stu-id="58d32-357">Notice that the return and cancel URLs that are specified in the **ShortcutExpressCheckout** method use a port number.</span></span>

[!code-html[Main](checkout-and-payment-with-paypal/samples/sample14.html)]

<span data-ttu-id="58d32-358">Visual Web Developer 中執行時使用 SSL 的 web 專案，連接埠 44300 常用的 web 伺服器。</span><span class="sxs-lookup"><span data-stu-id="58d32-358">When Visual Web Developer runs a web project using SSL, commonly the port 44300 is used for the web server.</span></span> <span data-ttu-id="58d32-359">如上所示，連接埠號碼是 44300。</span><span class="sxs-lookup"><span data-stu-id="58d32-359">As shown above, the port number is 44300.</span></span> <span data-ttu-id="58d32-360">當您執行應用程式時，您可以查看其他通訊埠編號。</span><span class="sxs-lookup"><span data-stu-id="58d32-360">When you run the application, you could see a different port number.</span></span> <span data-ttu-id="58d32-361">連接埠號碼需要正確設定程式碼中，讓您可以成功執行 Wingtip Toys 範例應用程式在此教學課程結尾處。</span><span class="sxs-lookup"><span data-stu-id="58d32-361">Your port number needs to be correctly set in the code so that you can successful run the Wingtip Toys sample application at the end of this tutorial.</span></span> <span data-ttu-id="58d32-362">本教學課程的下一節說明如何擷取本機主機通訊埠編號和 PayPal 類別的更新。</span><span class="sxs-lookup"><span data-stu-id="58d32-362">The next section of this tutorial explains how to retrieve the local host port number and update the PayPal class.</span></span>

### <a name="update-the-localhost-port-number-in-the-paypal-class"></a><span data-ttu-id="58d32-363">更新 PayPal 類別中的 LocalHost 的連接埠號碼</span><span class="sxs-lookup"><span data-stu-id="58d32-363">Update the LocalHost Port Number in the PayPal Class</span></span>

<span data-ttu-id="58d32-364">Wingtip Toys 範例應用程式瀏覽 PayPal 測試網站，然後返回 Wingtip Toys 範例應用程式的本機執行個體所購買的產品。</span><span class="sxs-lookup"><span data-stu-id="58d32-364">The Wingtip Toys sample application purchases products by navigating to the PayPal testing site and returning to your local instance of the Wingtip Toys sample application.</span></span> <span data-ttu-id="58d32-365">若要有 PayPal 傳回至正確的 URL，您必須指定連接埠號碼，在本機執行的範例應用程式，在上面提到的 PayPal 程式碼。</span><span class="sxs-lookup"><span data-stu-id="58d32-365">In order to have PayPal return to the correct URL, you need to specify the port number of the locally running sample application in the PayPal code mentioned above.</span></span>

1. <span data-ttu-id="58d32-366">以滑鼠右鍵按一下專案名稱 (**WingtipToys**) 中**方案總管 中**選取**屬性**。</span><span class="sxs-lookup"><span data-stu-id="58d32-366">Right-click the project name (**WingtipToys**) in **Solution Explorer** and select **Properties**.</span></span>
2. <span data-ttu-id="58d32-367">在左側的資料行中，選取**Web**  索引標籤。</span><span class="sxs-lookup"><span data-stu-id="58d32-367">In the left column, select the **Web** tab.</span></span>
3. <span data-ttu-id="58d32-368">擷取連接埠號碼從**專案 Url**方塊。</span><span class="sxs-lookup"><span data-stu-id="58d32-368">Retrieve the port number from the **Project Url** box.</span></span>
4. <span data-ttu-id="58d32-369">視需要更新`returnURL`和`cancelURL`PayPal 類別中 (`NVPAPICaller`) 中*PayPalFunctions.cs*檔案，以使用 web 應用程式的通訊埠編號：</span><span class="sxs-lookup"><span data-stu-id="58d32-369">If needed, update the `returnURL` and `cancelURL` in the PayPal class (`NVPAPICaller`) in the *PayPalFunctions.cs* file to use the port number of your web application:</span></span>   

    [!code-html[Main](checkout-and-payment-with-paypal/samples/sample15.html?highlight=1-2)]

<span data-ttu-id="58d32-370">現在您加入的程式碼會比對本機 Web 應用程式預期的連接埠。</span><span class="sxs-lookup"><span data-stu-id="58d32-370">Now the code that you added will match the expected port for your local Web application.</span></span> <span data-ttu-id="58d32-371">PayPal 可以回到本機電腦上的正確的 URL。</span><span class="sxs-lookup"><span data-stu-id="58d32-371">PayPal will be able to return to the correct URL on your local machine.</span></span>

### <a name="add-the-paypal-checkout-button"></a><span data-ttu-id="58d32-372">新增 PayPal 簽出 按鈕</span><span class="sxs-lookup"><span data-stu-id="58d32-372">Add the PayPal Checkout Button</span></span>

<span data-ttu-id="58d32-373">現在，主要的 PayPal 函式已加入到範例應用程式，您可以開始加入標記和程式碼需要呼叫這些函式。</span><span class="sxs-lookup"><span data-stu-id="58d32-373">Now that the primary PayPal functions have been added to the sample application, you can begin adding the markup and code needed to call these functions.</span></span> <span data-ttu-id="58d32-374">首先，您必須加入使用者會看到在購物車網頁的 [簽出] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="58d32-374">First, you must add the checkout button that the user will see on the shopping cart page.</span></span>

1. <span data-ttu-id="58d32-375">開啟*ShoppingCart.aspx*檔案。</span><span class="sxs-lookup"><span data-stu-id="58d32-375">Open the *ShoppingCart.aspx* file.</span></span>
2. <span data-ttu-id="58d32-376">捲動到檔案底部，然後尋找`<!--Checkout Placeholder -->`註解。</span><span class="sxs-lookup"><span data-stu-id="58d32-376">Scroll to the bottom of the file and find the `<!--Checkout Placeholder -->` comment.</span></span>
3. <span data-ttu-id="58d32-377">取代註解與`ImageButton`控制，讓標記取代，如下所示：</span><span class="sxs-lookup"><span data-stu-id="58d32-377">Replace the comment with an `ImageButton` control so that the mark up is replaced as follows:</span></span>  

    [!code-aspx[Main](checkout-and-payment-with-paypal/samples/sample16.aspx)]
4. <span data-ttu-id="58d32-378">在*ShoppingCart.aspx.cs*檔案，之後`UpdateBtn_Click`檔案，結尾附近的事件處理常式加入`CheckOutBtn_Click`事件處理常式：</span><span class="sxs-lookup"><span data-stu-id="58d32-378">In the *ShoppingCart.aspx.cs* file, after the `UpdateBtn_Click` event handler near the end of the file, add the `CheckOutBtn_Click` event handler:</span></span>  

    [!code-csharp[Main](checkout-and-payment-with-paypal/samples/sample17.cs)]
5. <span data-ttu-id="58d32-379">此外，在*ShoppingCart.aspx.cs*檔案中，將參考加入`CheckoutBtn`，如此一來，新的映像按鈕參考，如下所示：</span><span class="sxs-lookup"><span data-stu-id="58d32-379">Also in the *ShoppingCart.aspx.cs* file, add a reference to the `CheckoutBtn`, so that the new image button is referenced as follows:</span></span>  

    [!code-csharp[Main](checkout-and-payment-with-paypal/samples/sample18.cs?highlight=18)]
6. <span data-ttu-id="58d32-380">儲存您的變更同時*ShoppingCart.aspx*檔案和*ShoppingCart.aspx.cs*檔案。</span><span class="sxs-lookup"><span data-stu-id="58d32-380">Save your changes to both the *ShoppingCart.aspx* file and the *ShoppingCart.aspx.cs* file.</span></span>
7. <span data-ttu-id="58d32-381">從功能表中，選取**偵錯**-&gt;**建置 WingtipToys**。</span><span class="sxs-lookup"><span data-stu-id="58d32-381">From the menu, select **Debug**-&gt;**Build WingtipToys**.</span></span>  
 <span data-ttu-id="58d32-382">專案將會重建與新加入**ImageButton**控制項。</span><span class="sxs-lookup"><span data-stu-id="58d32-382">The project will be rebuilt with the newly added **ImageButton** control.</span></span>

### <a name="send-purchase-details-to-paypal"></a><span data-ttu-id="58d32-383">PayPal 來傳送訂單詳細資料</span><span class="sxs-lookup"><span data-stu-id="58d32-383">Send Purchase Details to PayPal</span></span>

<span data-ttu-id="58d32-384">當使用者按一下**簽出**購物車網頁上的按鈕 (*ShoppingCart.aspx*)，它們將會開始採購程序。</span><span class="sxs-lookup"><span data-stu-id="58d32-384">When the user clicks the **Checkout** button on the shopping cart page (*ShoppingCart.aspx*), they'll begin the purchase process.</span></span> <span data-ttu-id="58d32-385">下列程式碼會呼叫購買產品的第一個 PayPal 函式。</span><span class="sxs-lookup"><span data-stu-id="58d32-385">The following code calls the first PayPal function needed to purchase products.</span></span>

1. <span data-ttu-id="58d32-386">從*簽出*資料夾中，開啟的程式碼後置檔案命名為*CheckoutStart.aspx.cs*。</span><span class="sxs-lookup"><span data-stu-id="58d32-386">From the *Checkout* folder, open the code-behind file named *CheckoutStart.aspx.cs*.</span></span>   
 <span data-ttu-id="58d32-387">請務必開啟程式碼後置檔案。</span><span class="sxs-lookup"><span data-stu-id="58d32-387">Be sure to open the code-behind file.</span></span>
2. <span data-ttu-id="58d32-388">將現有的程式碼取代為下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="58d32-388">Replace the existing code with the following:</span></span>   

    [!code-csharp[Main](checkout-and-payment-with-paypal/samples/sample19.cs)]

<span data-ttu-id="58d32-389">當應用程式的使用者按一下**簽出**購物車網頁瀏覽器 按鈕會瀏覽至*CheckoutStart.aspx*頁面。</span><span class="sxs-lookup"><span data-stu-id="58d32-389">When the user of the application clicks the **Checkout** button on the shopping cart page, the browser will navigate to the *CheckoutStart.aspx* page.</span></span> <span data-ttu-id="58d32-390">當*CheckoutStart.aspx*頁面載入，`ShortcutExpressCheckout`方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="58d32-390">When the *CheckoutStart.aspx* page loads, the `ShortcutExpressCheckout` method is called.</span></span> <span data-ttu-id="58d32-391">此時，使用者會轉移至 PayPal 測試的網站。</span><span class="sxs-lookup"><span data-stu-id="58d32-391">At this point, the user is transferred to the PayPal testing web site.</span></span> <span data-ttu-id="58d32-392">PayPal 在網站上，使用者輸入他們的 PayPal 認證，檢閱採購詳細資料、 接受 PayPal 合約並 Wingtip Toys 範例應用程式會傳回其中`ShortcutExpressCheckout`方法完成。</span><span class="sxs-lookup"><span data-stu-id="58d32-392">On the PayPal site, the user enters their PayPal credentials, reviews the purchase details, accepts the PayPal agreement and returns to the Wingtip Toys sample application where the `ShortcutExpressCheckout` method completes.</span></span> <span data-ttu-id="58d32-393">當`ShortcutExpressCheckout`方法完成時，它會將使用者重新導向*CheckoutReview.aspx*頁面中指定`ShortcutExpressCheckout`方法。</span><span class="sxs-lookup"><span data-stu-id="58d32-393">When the `ShortcutExpressCheckout` method is complete, it will redirect the user to the *CheckoutReview.aspx* page specified in the `ShortcutExpressCheckout` method.</span></span> <span data-ttu-id="58d32-394">這可讓使用者檢閱來自 Wingtip Toys 範例應用程式中的訂單詳細資料。</span><span class="sxs-lookup"><span data-stu-id="58d32-394">This allows the user to review the order details from within the Wingtip Toys sample application.</span></span>

### <a name="review-order-details"></a><span data-ttu-id="58d32-395">檢閱訂單詳細資料</span><span class="sxs-lookup"><span data-stu-id="58d32-395">Review Order Details</span></span>

<span data-ttu-id="58d32-396">傳回從 PayPal 之後, *CheckoutReview.aspx* Wingtip Toys 範例應用程式的頁面會顯示訂單詳細資料。</span><span class="sxs-lookup"><span data-stu-id="58d32-396">After returning from PayPal, the *CheckoutReview.aspx* page of the Wingtip Toys sample application displays the order details.</span></span> <span data-ttu-id="58d32-397">此頁面可讓使用者檢閱再購買產品的訂單詳細資料。</span><span class="sxs-lookup"><span data-stu-id="58d32-397">This page allows the user to review the order details before purchasing the products.</span></span> <span data-ttu-id="58d32-398">*CheckoutReview.aspx*必須建立頁面，如下所示：</span><span class="sxs-lookup"><span data-stu-id="58d32-398">The *CheckoutReview.aspx* page must be created as follows:</span></span>

1. <span data-ttu-id="58d32-399">在*簽出*資料夾中，開啟名為頁面*CheckoutReview.aspx*。</span><span class="sxs-lookup"><span data-stu-id="58d32-399">In the *Checkout* folder, open the page named *CheckoutReview.aspx*.</span></span>
2. <span data-ttu-id="58d32-400">以下列內容取代現有的標記：</span><span class="sxs-lookup"><span data-stu-id="58d32-400">Replace the existing markup with the following:</span></span>   

    [!code-aspx[Main](checkout-and-payment-with-paypal/samples/sample20.aspx)]
3. <span data-ttu-id="58d32-401">開啟程式碼後置頁面，名為*CheckoutReview.aspx.cs*和現有的程式碼替換成下列：</span><span class="sxs-lookup"><span data-stu-id="58d32-401">Open the code-behind page named *CheckoutReview.aspx.cs* and replace the existing code with the following:</span></span>   

    [!code-csharp[Main](checkout-and-payment-with-paypal/samples/sample21.cs)]

<span data-ttu-id="58d32-402">**DetailsView**控制項用來顯示已從 PayPal 傳回的訂單詳細資料。</span><span class="sxs-lookup"><span data-stu-id="58d32-402">The **DetailsView** control is used to display the order details that have been returned from PayPal.</span></span> <span data-ttu-id="58d32-403">此外，上述程式碼將訂單詳細資料儲存至 Wingtip Toys 資料庫做為`OrderDetail`物件。</span><span class="sxs-lookup"><span data-stu-id="58d32-403">Also, the above code saves the order details to the Wingtip Toys database as an `OrderDetail` object.</span></span> <span data-ttu-id="58d32-404">當使用者按一下**完成訂單**按鈕時，會被重新導向至*CheckoutComplete.aspx*頁面。</span><span class="sxs-lookup"><span data-stu-id="58d32-404">When the user clicks on the **Complete Order** button, they are redirected to the *CheckoutComplete.aspx* page.</span></span>

> [!NOTE] 
> 
> <span data-ttu-id="58d32-405">**秘訣**</span><span class="sxs-lookup"><span data-stu-id="58d32-405">**Tip**</span></span>
> 
> <span data-ttu-id="58d32-406">在標記中*CheckoutReview.aspx*頁面上，請注意，`<ItemStyle>`標記用來變更中的項目樣式**DetailsView**靠近頁面底部的控制項。</span><span class="sxs-lookup"><span data-stu-id="58d32-406">In the markup of the *CheckoutReview.aspx* page, notice that the `<ItemStyle>` tag is used to change the style of the items within the **DetailsView** control near the bottom of the page.</span></span> <span data-ttu-id="58d32-407">藉由檢視中的頁面**設計 檢視**(藉由選取**設計**在 Visual Studio 左下角)，然後選取**DetailsView**控制項，然後選取**智慧標籤**(在最上方的箭號圖示右邊的控制項)，您將能夠看到**DetailsView 工作**。</span><span class="sxs-lookup"><span data-stu-id="58d32-407">By viewing the page in **Design View** (by selecting **Design** at the lower left corner of Visual Studio), then selecting the **DetailsView** control, and selecting the **Smart Tag** (the arrow icon at the top right of the control), you will be able to see the **DetailsView Tasks**.</span></span>
> 
> ![簽出 」 和 「 付款 PayPal-與編輯欄位](checkout-and-payment-with-paypal/_static/image18.png)
> 
> <span data-ttu-id="58d32-409">藉由選取**編輯欄位**、**欄位**對話方塊隨即出現。</span><span class="sxs-lookup"><span data-stu-id="58d32-409">By selecting **Edit Fields**, the **Fields** dialog box will appear.</span></span> <span data-ttu-id="58d32-410">在此對話方塊中您可以輕鬆控制的視覺屬性，例如**ItemStyle**的**DetailsView**控制項。</span><span class="sxs-lookup"><span data-stu-id="58d32-410">In this dialog box you can easily control the visual properties, such as **ItemStyle**, of the **DetailsView** control.</span></span>
> 
> ![簽出 」 和 「 付款與 PayPal-欄位 對話方塊](checkout-and-payment-with-paypal/_static/image19.png)


### <a name="complete-purchase"></a><span data-ttu-id="58d32-412">完成購買程序</span><span class="sxs-lookup"><span data-stu-id="58d32-412">Complete Purchase</span></span>

<span data-ttu-id="58d32-413">*CheckoutComplete.aspx*網頁可從 PayPal 進行購買。</span><span class="sxs-lookup"><span data-stu-id="58d32-413">*CheckoutComplete.aspx* page makes the purchase from PayPal.</span></span> <span data-ttu-id="58d32-414">如上面所述，使用者必須按一下**完成訂單**按鈕會瀏覽應用程式之前*CheckoutComplete.aspx*頁面。</span><span class="sxs-lookup"><span data-stu-id="58d32-414">As mentioned above, the user must click on the **Complete Order** button before the application will navigate to the *CheckoutComplete.aspx* page.</span></span>

1. <span data-ttu-id="58d32-415">在*簽出*資料夾中，開啟名為頁面*CheckoutComplete.aspx*。</span><span class="sxs-lookup"><span data-stu-id="58d32-415">In the *Checkout* folder, open the page named *CheckoutComplete.aspx*.</span></span>
2. <span data-ttu-id="58d32-416">以下列內容取代現有的標記：</span><span class="sxs-lookup"><span data-stu-id="58d32-416">Replace the existing markup with the following:</span></span>   

    [!code-aspx[Main](checkout-and-payment-with-paypal/samples/sample22.aspx)]
3. <span data-ttu-id="58d32-417">開啟程式碼後置頁面，名為*CheckoutComplete.aspx.cs*和現有的程式碼替換成下列：</span><span class="sxs-lookup"><span data-stu-id="58d32-417">Open the code-behind page named *CheckoutComplete.aspx.cs* and replace the existing code with the following:</span></span>   

    [!code-csharp[Main](checkout-and-payment-with-paypal/samples/sample23.cs)]

<span data-ttu-id="58d32-418">當*CheckoutComplete.aspx*網頁載入時，`DoCheckoutPayment`方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="58d32-418">When the *CheckoutComplete.aspx* page is loaded, the `DoCheckoutPayment` method is called.</span></span> <span data-ttu-id="58d32-419">如先前所述，`DoCheckoutPayment`方法完成購買程序從 PayPal 測試環境。</span><span class="sxs-lookup"><span data-stu-id="58d32-419">As mentioned earlier, the `DoCheckoutPayment` method completes the purchase from the PayPal testing environment.</span></span> <span data-ttu-id="58d32-420">PayPal 完成訂單的訂單後*CheckoutComplete.aspx*頁面會顯示付款交易`ID`來購買。</span><span class="sxs-lookup"><span data-stu-id="58d32-420">Once PayPal has completed the purchase of the order, the *CheckoutComplete.aspx* page displays a payment transaction `ID` to the purchaser.</span></span>

### <a name="handle-cancel-purchase"></a><span data-ttu-id="58d32-421">處理取消訂單</span><span class="sxs-lookup"><span data-stu-id="58d32-421">Handle Cancel Purchase</span></span>

<span data-ttu-id="58d32-422">如果使用者決定取消購買時，它們會導向至*CheckoutCancel.aspx*頁面位置就會看到它們的順序已經取消。</span><span class="sxs-lookup"><span data-stu-id="58d32-422">If the user decides to cancel the purchase, they will be directed to the *CheckoutCancel.aspx* page where they will see that their order has been cancelled.</span></span>

1. <span data-ttu-id="58d32-423">開啟此頁面*CheckoutCancel.aspx*中*簽出*資料夾。</span><span class="sxs-lookup"><span data-stu-id="58d32-423">Open the page named *CheckoutCancel.aspx* in the *Checkout* folder.</span></span>
2. <span data-ttu-id="58d32-424">以下列內容取代現有的標記：</span><span class="sxs-lookup"><span data-stu-id="58d32-424">Replace the existing markup with the following:</span></span>   

    [!code-aspx[Main](checkout-and-payment-with-paypal/samples/sample24.aspx)]

### <a name="handle-purchase-errors"></a><span data-ttu-id="58d32-425">處理購買錯誤</span><span class="sxs-lookup"><span data-stu-id="58d32-425">Handle Purchase Errors</span></span>

<span data-ttu-id="58d32-426">採購程序期間發生的錯誤處理*CheckoutError.aspx*頁面。</span><span class="sxs-lookup"><span data-stu-id="58d32-426">Errors during the purchase process will be handled by the *CheckoutError.aspx* page.</span></span> <span data-ttu-id="58d32-427">程式碼後置的*CheckoutStart.aspx*  頁面上， *CheckoutReview.aspx*  頁面上，而*CheckoutComplete.aspx*頁面將每個重新導向至*CheckoutError.aspx*頁面上，如果發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="58d32-427">The code-behind of the *CheckoutStart.aspx* page, the *CheckoutReview.aspx* page, and the *CheckoutComplete.aspx* page will each redirect to the *CheckoutError.aspx* page if an error occurs.</span></span>

1. <span data-ttu-id="58d32-428">開啟此頁面*CheckoutError.aspx*中*簽出*資料夾。</span><span class="sxs-lookup"><span data-stu-id="58d32-428">Open the page named *CheckoutError.aspx* in the *Checkout* folder.</span></span>
2. <span data-ttu-id="58d32-429">以下列內容取代現有的標記：</span><span class="sxs-lookup"><span data-stu-id="58d32-429">Replace the existing markup with the following:</span></span>   

    [!code-aspx[Main](checkout-and-payment-with-paypal/samples/sample25.aspx)]

<span data-ttu-id="58d32-430">*CheckoutError.aspx*頁面會顯示錯誤詳細資料在結帳程序期間發生錯誤時。</span><span class="sxs-lookup"><span data-stu-id="58d32-430">The *CheckoutError.aspx* page is displayed with the error details when an error occurs during the checkout process.</span></span>

## <a name="running-the-application"></a><span data-ttu-id="58d32-431">執行應用程式</span><span class="sxs-lookup"><span data-stu-id="58d32-431">Running the Application</span></span>

<span data-ttu-id="58d32-432">執行應用程式以了解如何購買的產品。</span><span class="sxs-lookup"><span data-stu-id="58d32-432">Run the application to see how to purchase products.</span></span> <span data-ttu-id="58d32-433">請注意，您將執行中的 PayPal 測試環境。</span><span class="sxs-lookup"><span data-stu-id="58d32-433">Note that you will be running in the PayPal testing environment.</span></span> <span data-ttu-id="58d32-434">正在交換沒有實際的成本。</span><span class="sxs-lookup"><span data-stu-id="58d32-434">No actual money is being exchanged.</span></span>

1. <span data-ttu-id="58d32-435">請確定所有 Visual Studio 中儲存您的檔案。</span><span class="sxs-lookup"><span data-stu-id="58d32-435">Make sure all your files are saved in Visual Studio.</span></span>
2. <span data-ttu-id="58d32-436">開啟網頁瀏覽器並瀏覽至[https://developer.paypal.com](https://developer.paypal.com/)。</span><span class="sxs-lookup"><span data-stu-id="58d32-436">Open a Web browser and navigate to [https://developer.paypal.com](https://developer.paypal.com/).</span></span>
3. <span data-ttu-id="58d32-437">以您稍早在本教學課程中建立您 PayPal 開發人員帳戶登入。</span><span class="sxs-lookup"><span data-stu-id="58d32-437">Login with your PayPal developer account that you created earlier in this tutorial.</span></span>  
 <span data-ttu-id="58d32-438">PayPal 的開發人員沙箱，您需要在登入[https://developer.paypal.com](https://developer.paypal.com/)測試 express 簽出。</span><span class="sxs-lookup"><span data-stu-id="58d32-438">For PayPal's developer sandbox, you need to be logged in at [https://developer.paypal.com](https://developer.paypal.com/) to test express checkout.</span></span> <span data-ttu-id="58d32-439">這只適用於 PayPal 的沙箱測試，不 PayPal 的實際環境。</span><span class="sxs-lookup"><span data-stu-id="58d32-439">This only applies to PayPal's sandbox testing, not to PayPal's live environment.</span></span>
4. <span data-ttu-id="58d32-440">在 Visual Studio 中，按**F5**執行 Wingtip Toys 範例應用程式。</span><span class="sxs-lookup"><span data-stu-id="58d32-440">In Visual Studio, press **F5** to run the Wingtip Toys sample application.</span></span>  
 <span data-ttu-id="58d32-441">重建資料庫之後，瀏覽器會開啟並顯示*Default.aspx*頁面。</span><span class="sxs-lookup"><span data-stu-id="58d32-441">After the database rebuilds, the browser will open and show the *Default.aspx* page.</span></span>
5. <span data-ttu-id="58d32-442">將三個不同的產品加入購物車選取產品類別目錄，例如 「 汽車 」，然後按一下**加入購物車**旁邊每項產品。</span><span class="sxs-lookup"><span data-stu-id="58d32-442">Add three different products to the shopping cart by selecting the product category, such as "Cars" and then clicking **Add to Cart** next to each product.</span></span>  
 <span data-ttu-id="58d32-443">購物車就會顯示您所選取的產品。</span><span class="sxs-lookup"><span data-stu-id="58d32-443">The shopping cart will display the product you have selected.</span></span>
6. <span data-ttu-id="58d32-444">按一下**PayPal**簽出 按鈕。</span><span class="sxs-lookup"><span data-stu-id="58d32-444">Click the **PayPal** button to checkout.</span></span> 

    ![簽出 」 和 「 付款 PayPal-與購物車](checkout-and-payment-with-paypal/_static/image20.png)

 <span data-ttu-id="58d32-446">簽出，將會需要您具備 Wingtip Toys 範例應用程式的使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="58d32-446">Checking out will require that you have a user account for the Wingtip Toys sample application.</span></span>
7. <span data-ttu-id="58d32-447">按一下**Google**上頁面的右邊，以現有的 gmail.com 電子郵件帳戶登入連結。</span><span class="sxs-lookup"><span data-stu-id="58d32-447">Click the **Google** link on the right of the page to log in with an existing gmail.com email account.</span></span>  
 <span data-ttu-id="58d32-448">如果您沒有 gmail.com 帳戶，您可以建立另一個用於測試用途[www.gmail.com](https://www.gmail.com/)。您也可以使用標準的本機帳戶，依序按一下 「 註冊 」。</span><span class="sxs-lookup"><span data-stu-id="58d32-448">If you do not have a gmail.com account, you can create one for testing purposes at [www.gmail.com](https://www.gmail.com/). You can also use a standard local account by clicking "Register".</span></span> 

    ![簽出 」 和 「 付款 PayPal-與登入](checkout-and-payment-with-paypal/_static/image21.png)
8. <span data-ttu-id="58d32-450">使用您 gmail 帳戶和密碼登入。</span><span class="sxs-lookup"><span data-stu-id="58d32-450">Sign in with your gmail account and password.</span></span> 

    ![簽出和 PayPal-Gmail 登入與付款](checkout-and-payment-with-paypal/_static/image22.png)
9. <span data-ttu-id="58d32-452">按一下**登入**gmail 帳戶向您 Wingtip Toys 範例應用程式的使用者名稱 按鈕。</span><span class="sxs-lookup"><span data-stu-id="58d32-452">Click the **Log in** button to register your gmail account with your Wingtip Toys sample application user name.</span></span> 

    ![簽出 」 和 「 付款與 PayPal-註冊帳戶](checkout-and-payment-with-paypal/_static/image23.png)
10. <span data-ttu-id="58d32-454">PayPal 測試站台上新增您**買方**電子郵件地址和您稍早在本教學課程中建立的密碼，然後按一下 [**登入**] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="58d32-454">On the PayPal test site, add your **buyer** email address and password that you created earlier in this tutorial, then click the **Log In** button.</span></span> 

    ![簽出和 PayPal-PayPal 登入與付款](checkout-and-payment-with-paypal/_static/image24.png)
11. <span data-ttu-id="58d32-456">同意 PayPal 原則並按一下**同意後繼續** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="58d32-456">Agree to the PayPal policy and click the **Agree and Continue** button.</span></span>  
 <span data-ttu-id="58d32-457">請注意，此頁面才會顯示您使用此 PayPal 帳戶第一次。</span><span class="sxs-lookup"><span data-stu-id="58d32-457">Note that this page is only displayed the first time you use this PayPal account.</span></span> <span data-ttu-id="58d32-458">再次請注意，這是測試帳戶，沒有實際 money 交換。</span><span class="sxs-lookup"><span data-stu-id="58d32-458">Again note that this is a test account, no real money is exchanged.</span></span> 

    ![簽出和 PayPal-PayPal 原則與付款](checkout-and-payment-with-paypal/_static/image25.png)
12. <span data-ttu-id="58d32-460">檢閱在測試環境 [檢閱] 頁面，然後按一下 PayPal 的訂單資訊**繼續**。</span><span class="sxs-lookup"><span data-stu-id="58d32-460">Review the order information on the PayPal testing environment review page and click **Continue**.</span></span> 

    ![簽出和 PayPal-檢閱資訊與付款](checkout-and-payment-with-paypal/_static/image26.png)
13. <span data-ttu-id="58d32-462">在*CheckoutReview.aspx*頁面上，確認訂單金額，檢視產生的送貨地址。</span><span class="sxs-lookup"><span data-stu-id="58d32-462">On the *CheckoutReview.aspx* page, verify the order amount and view the generated shipping address.</span></span> <span data-ttu-id="58d32-463">然後，按一下 [**完成訂單**] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="58d32-463">Then, click the **Complete Order** button.</span></span> 

    ![簽出和 PayPal-順序檢閱與付款](checkout-and-payment-with-paypal/_static/image27.png)
14. <span data-ttu-id="58d32-465">**CheckoutComplete.aspx**頁面會顯示付款交易識別碼。</span><span class="sxs-lookup"><span data-stu-id="58d32-465">The **CheckoutComplete.aspx** page is displayed with a payment transaction ID.</span></span> 

    ![簽出和 PayPal-完成簽出與付款](checkout-and-payment-with-paypal/_static/image28.png)

<a id="ReviewDBWebForms"></a>
## <a name="reviewing-the-database"></a><span data-ttu-id="58d32-467">檢閱資料庫</span><span class="sxs-lookup"><span data-stu-id="58d32-467">Reviewing the Database</span></span>

<span data-ttu-id="58d32-468">藉由檢閱 Wingtip Toys 範例應用程式資料庫中更新的資料執行應用程式之後，您可以看到應用程式成功地錄製產品的訂單。</span><span class="sxs-lookup"><span data-stu-id="58d32-468">By reviewing the updated data in the Wingtip Toys sample application database after running the application, you can see that the application successfully recorded the purchase of the products.</span></span>

<span data-ttu-id="58d32-469">您可以檢查所包含的資料*Wingtiptoys.mdf*資料庫檔案使用**資料庫總管**視窗 (**伺服器總管**Visual Studio 中的視窗) 您可以如同稍早在本教學課程的系列。</span><span class="sxs-lookup"><span data-stu-id="58d32-469">You can inspect the data contained in the *Wingtiptoys.mdf* database file by using the **Database Explorer** window (**Server Explorer** window in Visual Studio) as you did earlier in this tutorial series.</span></span>

1. <span data-ttu-id="58d32-470">如果它仍為開啟，請關閉瀏覽器視窗。</span><span class="sxs-lookup"><span data-stu-id="58d32-470">Close the browser window if it is still open.</span></span>
2. <span data-ttu-id="58d32-471">在 Visual Studio 中，選取**顯示所有檔案**上方的圖示**方案總管 中**可讓您展開**應用程式\_資料**資料夾。</span><span class="sxs-lookup"><span data-stu-id="58d32-471">In Visual Studio, select the **Show All Files** icon at the top of **Solution Explorer** to allow you to expand the **App\_Data** folder.</span></span>
3. <span data-ttu-id="58d32-472">展開**應用程式\_資料**資料夾。</span><span class="sxs-lookup"><span data-stu-id="58d32-472">Expand the **App\_Data** folder.</span></span>  
 <span data-ttu-id="58d32-473">您可能需要選取**顯示所有檔案**資料夾圖示。</span><span class="sxs-lookup"><span data-stu-id="58d32-473">You may need to select the **Show All Files** icon for the folder.</span></span>
4. <span data-ttu-id="58d32-474">以滑鼠右鍵按一下*Wingtiptoys.mdf*資料庫檔案，然後選取**開啟**。</span><span class="sxs-lookup"><span data-stu-id="58d32-474">Right-click the *Wingtiptoys.mdf* database file and select **Open**.</span></span>  
    <span data-ttu-id="58d32-475">**伺服器總管**隨即出現。</span><span class="sxs-lookup"><span data-stu-id="58d32-475">**Server Explorer** is displayed.</span></span>
5. <span data-ttu-id="58d32-476">展開**資料表**資料夾。</span><span class="sxs-lookup"><span data-stu-id="58d32-476">Expand the **Tables** folder.</span></span>
6. <span data-ttu-id="58d32-477">以滑鼠右鍵按一下**訂單**資料表，然後選取**顯示資料表資料**。</span><span class="sxs-lookup"><span data-stu-id="58d32-477">Right-click the **Orders**table and select **Show Table Data**.</span></span>  
 <span data-ttu-id="58d32-478">**訂單**資料表就會顯示。</span><span class="sxs-lookup"><span data-stu-id="58d32-478">The **Orders** table is displayed.</span></span>
7. <span data-ttu-id="58d32-479">檢閱**PaymentTransactionID**資料行，以確認成功的交易。</span><span class="sxs-lookup"><span data-stu-id="58d32-479">Review the **PaymentTransactionID** column to confirm successful transactions.</span></span> 

    ![簽出和 PayPal-檢閱資料庫與付款](checkout-and-payment-with-paypal/_static/image29.png)
8. <span data-ttu-id="58d32-481">關閉**訂單**資料表視窗中。</span><span class="sxs-lookup"><span data-stu-id="58d32-481">Close the **Orders** table window.</span></span>
9. <span data-ttu-id="58d32-482">在 [伺服器總管] 中，以滑鼠右鍵按一下**OrderDetails**資料表，然後選取**顯示資料表資料**。</span><span class="sxs-lookup"><span data-stu-id="58d32-482">In the Server Explorer, right-click the **OrderDetails** table and select **Show Table Data**.</span></span>
10. <span data-ttu-id="58d32-483">檢閱`OrderId`和`Username`值**OrderDetails**資料表。</span><span class="sxs-lookup"><span data-stu-id="58d32-483">Review the `OrderId` and `Username` values in the **OrderDetails** table.</span></span> <span data-ttu-id="58d32-484">請注意，這些值相符`OrderId`和`Username`值包含在**訂單**資料表。</span><span class="sxs-lookup"><span data-stu-id="58d32-484">Note that these values match the `OrderId` and `Username` values included in the **Orders** table.</span></span>
11. <span data-ttu-id="58d32-485">關閉**OrderDetails**資料表視窗中。</span><span class="sxs-lookup"><span data-stu-id="58d32-485">Close the **OrderDetails** table window.</span></span>
12. <span data-ttu-id="58d32-486">以滑鼠右鍵按一下 Wingtip Toys 資料庫檔案 (*Wingtiptoys.mdf*) 並選取**關閉連接**。</span><span class="sxs-lookup"><span data-stu-id="58d32-486">Right-click the Wingtip Toys database file (*Wingtiptoys.mdf*) and select **Close Connection**.</span></span>
13. <span data-ttu-id="58d32-487">如果您看不**方案總管 中**視窗中，按一下**方案總管 中**底部**伺服器總管**視窗以顯示**方案總管**一次。</span><span class="sxs-lookup"><span data-stu-id="58d32-487">If you do not see the **Solution Explorer** window, click **Solution Explorer** at the bottom of the **Server Explorer** window to show the **Solution Explorer** again.</span></span>

## <a name="summary"></a><span data-ttu-id="58d32-488">總結</span><span class="sxs-lookup"><span data-stu-id="58d32-488">Summary</span></span>

<span data-ttu-id="58d32-489">在本教學課程中加入訂單及訂單詳細資料的結構描述追蹤購買的產品。</span><span class="sxs-lookup"><span data-stu-id="58d32-489">In this tutorial you added order and order detail schemas to track the purchase of products.</span></span> <span data-ttu-id="58d32-490">您也會整合至 Wingtip Toys 範例應用程式的 PayPal 功能。</span><span class="sxs-lookup"><span data-stu-id="58d32-490">You also integrated PayPal functionality into the Wingtip Toys sample application.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="58d32-491">其他資源</span><span class="sxs-lookup"><span data-stu-id="58d32-491">Additional Resources</span></span>

<span data-ttu-id="58d32-492">[ASP.NET 組態概觀](https://msdn.microsoft.com/library/ms178683(v=vs.100).aspx)</span><span class="sxs-lookup"><span data-stu-id="58d32-492">[ASP.NET Configuration Overview](https://msdn.microsoft.com/library/ms178683(v=vs.100).aspx)</span></span>  
[<span data-ttu-id="58d32-493">將具有成員資格、 OAuth、 和 SQL Database 的安全的 ASP.NET Web Form 應用程式部署至 Azure App Service</span><span class="sxs-lookup"><span data-stu-id="58d32-493">Deploy a Secure ASP.NET Web Forms App with Membership, OAuth, and SQL Database to Azure App Service</span></span>](https://azure.microsoft.com/documentation/articles/web-sites-dotnet-deploy-aspnet-webforms-app-membership-oauth-sql-database/)  
[<span data-ttu-id="58d32-494">Microsoft Azure-免費試用版</span><span class="sxs-lookup"><span data-stu-id="58d32-494">Microsoft Azure - Free Trial</span></span>](https://azure.microsoft.com/pricing/free-trial/)

## <a name="disclaimer"></a><span data-ttu-id="58d32-495">免責聲明</span><span class="sxs-lookup"><span data-stu-id="58d32-495">Disclaimer</span></span>

<span data-ttu-id="58d32-496">本教學課程包含範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="58d32-496">This tutorial contains sample code.</span></span> <span data-ttu-id="58d32-497">這類的範例程式碼係依 「 現況 」 不含任何種類的擔保。</span><span class="sxs-lookup"><span data-stu-id="58d32-497">Such sample code is provided "as is" without warranty of any kind.</span></span> <span data-ttu-id="58d32-498">因此，Microsoft 不保證精確度、 完整性或範例程式碼的品質。</span><span class="sxs-lookup"><span data-stu-id="58d32-498">Accordingly, Microsoft does not guarantee the accuracy, integrity, or quality of the sample code.</span></span> <span data-ttu-id="58d32-499">您同意自行承擔使用範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="58d32-499">You agree to use the sample code at your own risk.</span></span> <span data-ttu-id="58d32-500">在任何情況下 Microsoft 會負責您以任何方式的任何程式碼範例內容，包括但不是限於任何錯誤或不作為概不在任何程式碼範例、 內容或任何遺失或損毀所造成的結果的任何程式碼範例使用任何種類。</span><span class="sxs-lookup"><span data-stu-id="58d32-500">Under no circumstances will Microsoft be liable to you in any way for any sample code, content, including but not limited to, any errors or omissions in any sample code, content, or any loss or damage of any kind incurred as a result of the use of any sample code.</span></span> <span data-ttu-id="58d32-501">被授權人有收到通知，並被授權人有同意出面代為辯護，請儲存並保留 Microsoft 無害遭受任何和所有遺失、 遺失、 傷害或損任何的毀種類包括，但不限於由 occasioned 或資料，以在張貼時，所引起的宣告傳輸、 使用或依賴包括但不是限於表示其中的檢視。</span><span class="sxs-lookup"><span data-stu-id="58d32-501">You are hereby notified and do hereby agree to indemnify, save and hold Microsoft harmless from and against any and all loss, claims of loss, injury or damage of any kind including, without limitation, those occasioned by or arising from material that you post, transmit, use or rely on including, but not limited to, the views expressed therein.</span></span>

>[!div class="step-by-step"]
<span data-ttu-id="58d32-502">[上一頁](shopping-cart.md)
[下一頁](membership-and-administration.md)</span><span class="sxs-lookup"><span data-stu-id="58d32-502">[Previous](shopping-cart.md)
[Next](membership-and-administration.md)</span></span>