---
title: "replace_if (STL/CLR) | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.technology: ["cpp-cli"]
ms.topic: "reference"
f1_keywords: ["cliext::replace_if"]
dev_langs: ["C++"]
helpviewer_keywords: ["replace_if function [STL/CLR]"]
ms.assetid: 485ed698-551f-4808-8562-9e32b151786d
author: "mikeblome"
ms.author: "mblome"
ms.workload: ["cplusplus", "dotnet"]
---
# replace_if (STL/CLR)
Examines each element in a range and replaces it if it satisfies a specified predicate.  
  
## Syntax  
  
```  
template<class _FwdIt, class _Pr, class _Ty> inline  
    void replace_if(_FwdIt _First, _FwdIt _Last, _Pr _Pred,  
        const _Ty% _Val);  
```  
  
## Remarks  
 This function behaves the same as the C++ Standard Library function `replace_if`. For more information, see [replace_if](../standard-library/algorithm-functions.md#replace_if).  
  
## Requirements  
 **Header:** \<cliext/algorithm>  
  
 **Namespace:** cliext  
  
## See Also  
 [algorithm (STL/CLR)](../dotnet/algorithm-stl-clr.md)