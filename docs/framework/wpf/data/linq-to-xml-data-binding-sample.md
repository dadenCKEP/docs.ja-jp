---
title: LINQ to XML データバインディングの例
ms.date: 10/22/2019
ms.topic: sample
helpviewer_keywords:
- linq to xml data binding sample
ms.openlocfilehash: aac814e4768a863a93e69e34cd18c941a9b35c89
ms.sourcegitcommit: 82f94a44ad5c64a399df2a03fa842db308185a76
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/25/2019
ms.locfileid: "72921222"
---
# <a name="linq-to-xml-data-binding-sample"></a><span data-ttu-id="bc7e0-102">LINQ to XML データバインディングのサンプル</span><span class="sxs-lookup"><span data-stu-id="bc7e0-102">LINQ to XML data binding sample</span></span>

<span data-ttu-id="bc7e0-103">この記事では、ユーザーインターフェイスコンポーネントを埋め込み XML データソースにバインドする Windows Presentation Foundation (WPF) アプリである LinqToXmlDataBinding サンプルについて説明します。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-103">This article describes the LinqToXmlDataBinding sample, a Windows Presentation Foundation (WPF) app that binds user interface components to an embedded XML data source.</span></span>

## <a name="overview"></a><span data-ttu-id="bc7e0-104">概要</span><span class="sxs-lookup"><span data-stu-id="bc7e0-104">Overview</span></span>

<span data-ttu-id="bc7e0-105">LinqToXmlDataBinding サンプルは、および XAML ソースファイルを含むC# WINDOWS PRESENTATION FOUNDATION (WPF) アプリです。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-105">The LinqToXmlDataBinding sample is a Windows Presentation Foundation (WPF) app that contains C# and XAML source files.</span></span> <span data-ttu-id="bc7e0-106">埋め込み XML ドキュメントには、書籍の一覧が定義されています。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-106">An embedded XML document defines a list of books.</span></span> <span data-ttu-id="bc7e0-107">ユーザーは、アプリを使用して、ブックのエントリを表示、追加、削除、および編集できます。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-107">The app enables the user to view, add, delete, and edit the book entries.</span></span>

<span data-ttu-id="bc7e0-108">プライマリソースファイルは2つあります。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-108">There are two primary source files:</span></span>

- <span data-ttu-id="bc7e0-109">[L2DBForm.xaml](l2dbform-xaml-source-code.md) には、メイン ウィンドウのユーザー インターフェイス (UI) の XAML 宣言コードが含まれています。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-109">[L2DBForm.xaml](l2dbform-xaml-source-code.md) contains the XAML declaration code for the user interface (UI) of the main window.</span></span> <span data-ttu-id="bc7e0-110">また、データプロバイダーと、書籍の一覧の埋め込み XML ドキュメントを定義するウィンドウリソースセクションも含まれています。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-110">It also contains a window resource section that defines a data provider and an embedded XML document for the book listings.</span></span>

- <span data-ttu-id="bc7e0-111">[L2DBForm.xaml.cs](l2dbform-xaml-cs-source-code.md) には、UI に関連付けられている初期化メソッドとイベント処理メソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-111">[L2DBForm.xaml.cs](l2dbform-xaml-cs-source-code.md) contains the initialization and event-handling methods associated with the UI.</span></span>

<span data-ttu-id="bc7e0-112">メイン ウィンドウは縦に区切られ、次の 4 つの UI セクションに分かれています。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-112">The main window is divided into the following four vertical UI sections:</span></span>

- <span data-ttu-id="bc7e0-113">**[XML]** には、組み込まれている書籍一覧の生の XML ソースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-113">**XML** displays the raw XML source of the embedded book listing.</span></span>

- <span data-ttu-id="bc7e0-114">**[Book List]** には書籍エントリが標準テキストで表示され、ユーザーはエントリを個別に選択および削除できます。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-114">**Book List** displays the book entries as standard text and enables the user to select and delete individual entries.</span></span>

- <span data-ttu-id="bc7e0-115">**[Edit Selected Book]** では、ユーザーは現在選択している書籍エントリに関連付けられている値を編集できます。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-115">**Edit Selected Book** enables the user to edit the values associated with the currently selected book entry.</span></span>

- <span data-ttu-id="bc7e0-116">**[Add New Book]** では、ユーザーが入力した値に基づいて新しい書籍エントリを作成できます。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-116">**Add New Book** enables the creation of a new book entry based on values entered by the user.</span></span>

## <a name="run-the-sample"></a><span data-ttu-id="bc7e0-117">サンプルを実行する</span><span class="sxs-lookup"><span data-stu-id="bc7e0-117">Run the sample</span></span>

<span data-ttu-id="bc7e0-118">このセクションでは、Visual Studio で LinqToXmlDataBinding プロジェクトを作成してビルドする方法と、結果の LinqToXmlDataBinding Windows Presentation Foundation (WPF) アプリを実行する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-118">This section shows how to create and build the LinqToXmlDataBinding project in Visual Studio, and how to run the resulting LinqToXmlDataBinding Windows Presentation Foundation (WPF) app.</span></span>

### <a name="create-the-project"></a><span data-ttu-id="bc7e0-119">プロジェクトの作成</span><span class="sxs-lookup"><span data-stu-id="bc7e0-119">Create the project</span></span>

1. <span data-ttu-id="bc7e0-120">Visual Studio を開き、**LinqToXmlDataBinding** という名前の C# **WPF アプリ**を作成します。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-120">Open Visual Studio and create a C# **WPF App** named **LinqToXmlDataBinding**.</span></span>

   <span data-ttu-id="bc7e0-121">プロジェクトの対象は、.NET Framework 3.5 (またはそれ以降) にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-121">The project should target the .NET Framework 3.5 (or later).</span></span>

1. <span data-ttu-id="bc7e0-122">次の .NET アセンブリ用のプロジェクト参照がない場合は追加します。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-122">If not already present, add project references for the following .NET assemblies:</span></span>

    - <span data-ttu-id="bc7e0-123">System.Data</span><span class="sxs-lookup"><span data-stu-id="bc7e0-123">System.Data</span></span>
    - <span data-ttu-id="bc7e0-124">System.Data.DataSetExtensions</span><span class="sxs-lookup"><span data-stu-id="bc7e0-124">System.Data.DataSetExtensions</span></span>
    - <span data-ttu-id="bc7e0-125">System.Xml</span><span class="sxs-lookup"><span data-stu-id="bc7e0-125">System.Xml</span></span>
    - <span data-ttu-id="bc7e0-126">System.Xml</span><span class="sxs-lookup"><span data-stu-id="bc7e0-126">System.Xml</span></span>

1. <span data-ttu-id="bc7e0-127">**Ctrl** キーと **Shift** キーを押しながら **B** キーを押してソリューションをビルドし、**F5** キーを押してそのソリューションを実行します。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-127">Build the solution by pressing **Ctrl**+**Shift**+**B**, then run it by pressing **F5**.</span></span>

   <span data-ttu-id="bc7e0-128">プロジェクトがエラーなくコンパイルされ、汎用 WPF アプリケーションとして実行されます。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-128">The project should compile without errors and run as a generic WPF application.</span></span>

### <a name="add-code"></a><span data-ttu-id="bc7e0-129">コードの追加</span><span class="sxs-lookup"><span data-stu-id="bc7e0-129">Add code</span></span>

1. <span data-ttu-id="bc7e0-130">**ソリューション エクスプローラー**でソース ファイルの名前を **Window1.xaml** から **L2XDBForm.xaml** に変更します。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-130">In **Solution Explorer**, rename the source file **Window1.xaml** to **L2XDBForm.xaml**.</span></span>

   <span data-ttu-id="bc7e0-131">依存ソースファイル Window1.xaml.cs の名前は自動的に L2XDBForm.xaml.cs に変更されます。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-131">The dependent source file Window1.xaml.cs is automatically renamed to L2XDBForm.xaml.cs.</span></span>

1. <span data-ttu-id="bc7e0-132">**L2xdbform.xaml**ファイルで見つかったソースコードを[l2dbform.xaml ソースコード](l2dbform-xaml-source-code.md)に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-132">Replace the source code found in the file **L2XDBForm.xaml** with the [L2DBForm.xaml source code](l2dbform-xaml-source-code.md).</span></span> <span data-ttu-id="bc7e0-133">このファイルは XAML ソース ビューで操作します。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-133">Use the XAML source view to work with this file.</span></span>

1. <span data-ttu-id="bc7e0-134">同様に、 **L2XDBForm.xaml.cs**内のソースを[L2DBForm.xaml.cs ソースコード](l2dbform-xaml-cs-source-code.md)に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-134">Similarly, replace the source in **L2XDBForm.xaml.cs** with the [L2DBForm.xaml.cs source code](l2dbform-xaml-cs-source-code.md).</span></span>

1. <span data-ttu-id="bc7e0-135">**ファイル app.xaml で、文字列** **window1.xaml**のすべての出現箇所を**l2xdbform.xaml**に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-135">In the file **App.xaml**, replace all occurrences of the string **Window1.xaml** with **L2XDBForm.xaml**.</span></span>

1. <span data-ttu-id="bc7e0-136">**Ctrl** キーと **Shift** キーを押しながら **B** キーを押して、ソリューションをビルドします。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-136">Build the solution by pressing **Ctrl**+**Shift**+**B**.</span></span>

### <a name="run-the-app"></a><span data-ttu-id="bc7e0-137">アプリを実行する</span><span class="sxs-lookup"><span data-stu-id="bc7e0-137">Run the app</span></span>

<span data-ttu-id="bc7e0-138">LinqToXmlDataBinding アプリを使用すると、埋め込み XML 要素として格納されている書籍の一覧を表示および操作できます。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-138">The LinqToXmlDataBinding app enables the user to view and manipulate a list of books that's stored as an embedded XML element.</span></span> <span data-ttu-id="bc7e0-139">**F5**キー ([デバッグ開始]) または**Ctrl**+**F5** ([デバッグなしで開始]) を押して、アプリを実行します。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-139">Run the app by pressing **F5** (Start Debugging) or **Ctrl**+**F5** (Start Without Debugging).</span></span>

<span data-ttu-id="bc7e0-140">**[WPF Data Binding using LINQ to XML]** というタイトルのプログラム ウィンドウが表示されます。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-140">A program window with the title **WPF Data Binding using LINQ to XML** appears.</span></span>

<span data-ttu-id="bc7e0-141">UI の上部のセクションには、書籍リストを表す未加工の**XML**が表示されます。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-141">The top section of the UI displays the raw **XML** that represents the book list.</span></span> <span data-ttu-id="bc7e0-142">この部分は WPF の <xref:System.Windows.Controls.TextBlock> コントロールを使って表示されており、マウスやキーボードで操作できません。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-142">It is displayed using a WPF <xref:System.Windows.Controls.TextBlock> control, which does not enable interaction through the mouse or keyboard.</span></span>

<span data-ttu-id="bc7e0-143">**[Book List]** というラベルの付いた 2 番目のセクションには、プレーンテキストの順序付けられた一覧として書籍が表示されます。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-143">The second vertical section, labeled **Book List**, displays the books as a plain text ordered list.</span></span> <span data-ttu-id="bc7e0-144">この部分では <xref:System.Windows.Controls.ListBox> コントロールが使用されており、マウスまたはキーボードによる選択が可能です。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-144">It uses a <xref:System.Windows.Controls.ListBox> control that enables selection though the mouse or keyboard.</span></span>

### <a name="add-and-delete-books"></a><span data-ttu-id="bc7e0-145">ブックの追加と削除</span><span class="sxs-lookup"><span data-stu-id="bc7e0-145">Add and delete books</span></span>

<span data-ttu-id="bc7e0-146">一覧に新しい書籍を追加するには、 **[新しい書籍の追加]** の **[ID]** と **[値]** <xref:System.Windows.Controls.TextBox> コントロールに値を入力し、add **[book]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-146">To add a new book to the list, enter values into the **ID** and **Value** <xref:System.Windows.Controls.TextBox> controls in the last section, **Add New Book**, and then select **Add Book**.</span></span> <span data-ttu-id="bc7e0-147">書籍と XML の両方の一覧に書籍が追加されます。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-147">The book is appended to the list in both the book and XML listings.</span></span> <span data-ttu-id="bc7e0-148">このプログラムでは入力値が検証されません。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-148">This program does not validate input values.</span></span>

<span data-ttu-id="bc7e0-149">一覧から既存の書籍を削除するには、 **[Book list]** セクションでそのブックを選択し、 **[選択したブックの削除]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-149">To delete an existing book from the list, select it in the **Book List** section, and then select **Remove Selected Book**.</span></span> <span data-ttu-id="bc7e0-150">書籍のエントリは、書籍と未加工の XML ソースの一覧の両方から削除されます。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-150">The book entry is removed from both the book and the raw XML source listings.</span></span>

### <a name="edit-a-book-entry"></a><span data-ttu-id="bc7e0-151">書籍のエントリを編集する</span><span class="sxs-lookup"><span data-stu-id="bc7e0-151">Edit a book entry</span></span>

1. <span data-ttu-id="bc7e0-152">2 番目の **[Book List]** セクションで書籍エントリを選択します。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-152">Select the book entry in the second **Book List** section.</span></span>

   <span data-ttu-id="bc7e0-153">現在の値は、 **[選択したブックの編集]** セクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-153">Its current values are displayed in the **Edit Selected Book** section.</span></span>

1. <span data-ttu-id="bc7e0-154">キーボードを使用して値を編集します。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-154">Edit the values using the keyboard.</span></span> <span data-ttu-id="bc7e0-155"><xref:System.Windows.Controls.TextBox> 制御がフォーカスを失うとすぐに、変更は XML ソースと書籍の一覧に自動的に反映されます。</span><span class="sxs-lookup"><span data-stu-id="bc7e0-155">As soon as either <xref:System.Windows.Controls.TextBox> control loses focus, changes are automatically propagated to the XML source and book listings.</span></span>