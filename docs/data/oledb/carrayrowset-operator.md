---
title: "CArrayRowset::operator | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.technology: ["cpp-data"]
ms.topic: "reference"
f1_keywords: ["CArrayRowset::operator[]", "CArrayRowset.operator[]"]
dev_langs: ["C++"]
helpviewer_keywords: ["operator [], arrays", "[] operator", "operator[], arrays"]
ms.assetid: 3bb8c310-cc1e-46e8-9711-9b565488acaa
author: "mikeblome"
ms.author: "mblome"
ms.workload: ["cplusplus", "data-storage"]
---
# CArrayRowset::operator
Provides array-like syntax for accessing a row in the rowset.  
  
## Syntax  
  
```cpp
      TAccessor  
      & operator[](int nrow);  
```  
  
#### Parameters  
 `TAccessor`  
 A templated parameter that specifies the type of accessor stored in the rowset.  
  
 `nRow`  
 [in] Number of the row (array element) you want to access.  
  
## Return Value  
 The contents of the requested row.  
  
## Remarks  
 If `nRow` exceeds the number of rows in the rowset, an exception is thrown.  
  
## Requirements  
 **Header:** atldbcli.h  
  
## See Also  
 [CArrayRowset Class](../../data/oledb/carrayrowset-class.md)