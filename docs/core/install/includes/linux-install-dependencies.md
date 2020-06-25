---
ms.openlocfilehash: b371525c9f4e57c6a09e5bb9232884e5c5e707e0
ms.sourcegitcommit: cdb295dd1db589ce5169ac9ff096f01fd0c2da9d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/09/2020
ms.locfileid: "84602766"
---

<span data-ttu-id="3ac9f-101">パッケージ マネージャーを使用してインストールする場合、次のライブラリが自動的にインストールされます。</span><span class="sxs-lookup"><span data-stu-id="3ac9f-101">When you install with a package manager, these libraries are installed for you.</span></span> <span data-ttu-id="3ac9f-102">ただし、手動で .NET Core をインストールする場合、または自己完結型アプリを公開する場合は、次のライブラリがインストールされていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ac9f-102">But, if you manually install .NET Core or you publish a self-contained app, you'll need to make sure these libraries are installed:</span></span>

- <span data-ttu-id="3ac9f-103">lttng-ust</span><span class="sxs-lookup"><span data-stu-id="3ac9f-103">lttng-ust</span></span>
- <span data-ttu-id="3ac9f-104">libcurl</span><span class="sxs-lookup"><span data-stu-id="3ac9f-104">libcurl</span></span>
- <span data-ttu-id="3ac9f-105">openssl-libs</span><span class="sxs-lookup"><span data-stu-id="3ac9f-105">openssl-libs</span></span>
- <span data-ttu-id="3ac9f-106">krb5-libs</span><span class="sxs-lookup"><span data-stu-id="3ac9f-106">krb5-libs</span></span>
- <span data-ttu-id="3ac9f-107">libicu</span><span class="sxs-lookup"><span data-stu-id="3ac9f-107">libicu</span></span>
- <span data-ttu-id="3ac9f-108">zlib</span><span class="sxs-lookup"><span data-stu-id="3ac9f-108">zlib</span></span>
- <span data-ttu-id="3ac9f-109">libunwind</span><span class="sxs-lookup"><span data-stu-id="3ac9f-109">libunwind</span></span>
- <span data-ttu-id="3ac9f-110">libuuid</span><span class="sxs-lookup"><span data-stu-id="3ac9f-110">libuuid</span></span>

<span data-ttu-id="3ac9f-111">ターゲット ランタイム環境の OpenSSL バージョンが 1.1 以降である場合は、**compat-openssl10** をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ac9f-111">If the target runtime environment's OpenSSL version is 1.1 or newer, you'll need to install **compat-openssl10**.</span></span>

<span data-ttu-id="3ac9f-112">依存関係の詳細については、「[Self-contained Linux applications](https://github.com/dotnet/core/blob/master/Documentation/self-contained-linux-apps.md)」(自己完結型 Linux アプリケーション) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="3ac9f-112">For more information about the dependencies, see [Self-contained Linux apps](https://github.com/dotnet/core/blob/master/Documentation/self-contained-linux-apps.md).</span></span>

<span data-ttu-id="3ac9f-113">*System.Drawing.Common* アセンブリを使用する .NET Core アプリの場合は、次の依存関係も必要です。</span><span class="sxs-lookup"><span data-stu-id="3ac9f-113">For .NET Core apps that use the *System.Drawing.Common* assembly, you'll also need the following dependency:</span></span>

- [<span data-ttu-id="3ac9f-114">libgdiplus (バージョン 6.0.1 以降)</span><span class="sxs-lookup"><span data-stu-id="3ac9f-114">libgdiplus (version 6.0.1 or later)</span></span>](https://www.mono-project.com/docs/gui/libgdiplus/)

  > [!WARNING]
  > <span data-ttu-id="3ac9f-115">最新バージョンの *libgdiplus* をインストールするには、システムに Mono リポジトリを追加します。</span><span class="sxs-lookup"><span data-stu-id="3ac9f-115">You can install a recent version of *libgdiplus* by adding the Mono repository to your system.</span></span> <span data-ttu-id="3ac9f-116">詳細については、「<https://www.mono-project.com/download/stable/>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3ac9f-116">For more information, see <https://www.mono-project.com/download/stable/>.</span></span>