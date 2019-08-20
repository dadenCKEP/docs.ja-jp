---
title: ICorProfilerInfo9 インターフェイス
ms.date: 08/06/2019
author: davmason
ms.author: davmason
ms.openlocfilehash: 0ba4f2b4a515143d50bc812f04ea75d821b69471
ms.sourcegitcommit: a97ecb94437362b21fffc5eb3c38b6c0b4368999
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/13/2019
ms.locfileid: "68973802"
---
# <a name="icorprofilerinfo9-interface"></a>ICorProfilerInfo9 インターフェイス

複数のネイティブコードバージョンを持つ関数に関する情報を照会するメソッドを提供する[ICorProfilerInfo8](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo8-interface.md)のサブクラス。  

## <a name="methods"></a>メソッド  

| メソッド|説明|  
| ------------|-----------------|  
|[GetNativeCodeStartAddresses メソッド](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo9-getnativecodestartaddresses-method.md)| 指定された functionId と rejitId は、現在存在する、このコードのすべての just-in-time バージョンのネイティブコードの開始アドレスを列挙します。 |
|[GetILToNativeMapping3 メソッド](../../../../docs/framework/unmanaged-api/profiling/icorprofilerinfo9-getiltonativemapping3-method.md)| ネイティブコードの開始アドレスが指定されている場合、この just-in-time バージョンのコードのネイティブから IL へのマッピング情報を返します。 |
|[GetCodeInfo4 メソッド](icorprofilerinfo9-getcodeinfo4-method.md)| ネイティブコードの開始アドレスを指定すると、このコードを格納する仮想メモリのブロックが返されます。 |

## <a name="requirements"></a>必要条件  
**・** 「 [.Net Core でサポートされるオペレーティングシステム](../../../core/windows-prerequisites.md#net-core-supported-operating-systems)」を参照してください。  
**ヘッダー:** Corprof.idl、Corprof.idl  
**.Net のバージョン:** [!INCLUDE[net_core](../../../../includes/net-core-22-md.md)]  
## <a name="see-also"></a>関連項目
- [プロファイリングのインターフェイス](../../../../docs/framework/unmanaged-api/profiling/profiling-interfaces.md)