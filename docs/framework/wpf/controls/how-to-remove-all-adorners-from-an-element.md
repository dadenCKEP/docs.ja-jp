---
title: '方法: 要素からすべての装飾を削除する'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- adorners [WPF], removing
ms.assetid: fe5303a3-b76e-4643-aafb-51419032b47b
ms.openlocfilehash: 8504bb1ec70de188033b2b092bbb66cf9da3dc11
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "61770774"
---
# <a name="how-to-remove-all-adorners-from-an-element"></a>方法: 要素からすべての装飾を削除する
この例では、指定された <xref:System.Windows.UIElement> からすべての装飾をプログラムで削除する方法を示します。  
  
## <a name="example"></a>例  
 この詳細なコード例では、<xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A> によって返される装飾の配列にあるすべての装飾を削除します。  この例では、*myTextBox* という名前の <xref:System.Windows.UIElement> の装飾を取得します。  <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A> の呼び出しで指定された要素に装飾がない場合、`null` が返されます。  このコードによって、Null 配列が明示的にチェックされます。これは、Null 配列が比較的一般的であると予想されるアプリケーションに最適です。  
  
 [!code-csharp[AdornersMiscCode#_RemoveAllAdornersLong](~/samples/snippets/csharp/VS_Snippets_Wpf/AdornersMiscCode/CSharp/Window1.xaml.cs#_removealladornerslong)]
 [!code-vb[AdornersMiscCode#_RemoveAllAdornersLong](~/samples/snippets/visualbasic/VS_Snippets_Wpf/AdornersMiscCode/visualbasic/window1.xaml.vb#_removealladornerslong)]  
  
## <a name="example"></a>例  
 この簡約されたコード例は、上記の詳細な例と機能的には同等です。 このコードでは、Null 配列が明示的にチェックされないため、<xref:System.NullReferenceException> の例外が発生する可能性があります。  このコードは、Null 配列がまれであると予想されるアプリケーションに最適です。  
  
 [!code-csharp[AdornersMiscCode#_RemoveAllAdornersShort](~/samples/snippets/csharp/VS_Snippets_Wpf/AdornersMiscCode/CSharp/Window1.xaml.cs#_removealladornersshort)]
 [!code-vb[AdornersMiscCode#_RemoveAllAdornersShort](~/samples/snippets/visualbasic/VS_Snippets_Wpf/AdornersMiscCode/visualbasic/window1.xaml.vb#_removealladornersshort)]  
  
## <a name="see-also"></a>関連項目

- [装飾の概要](adorners-overview.md)
