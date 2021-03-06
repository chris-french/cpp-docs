---
title: "IAccessorImpl Class | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.technology: ["cpp-data"]
ms.topic: "reference"
f1_keywords: ["IAccessorImpl"]
dev_langs: ["C++"]
helpviewer_keywords: ["IAccessorImpl class"]
ms.assetid: 768606da-8b71-417c-a62c-88069ce7730d
author: "mikeblome"
ms.author: "mblome"
ms.workload: ["cplusplus", "data-storage"]
---
# IAccessorImpl Class
Provides an implementation of the [IAccessor](https://msdn.microsoft.com/en-us/library/ms719672.aspx) interface.  
  
## Syntax

```cpp
template <class T, 
          class BindType = ATLBINDINGS,
          class BindingVector = CAtlMap <HACCESSOR hAccessor, BindType* pBindingsStructure>>  
class ATL_NO_VTABLE IAccessorImpl : public IAccessorImplBase<BindType>  
```  
  
#### Parameters  
 `T`  
 Your rowset or command object class.  
  
 `BindType`  
 Storage unit for binding information. The default is the **ATLBINDINGS** structure (see atldb.h).  
  
 `BindingVector`  
 Storage unit for column information. The default is [CAtlMap](../../atl/reference/catlmap-class.md) where the key element is an **HACCESSOR** value and the value element is a pointer to a `BindType` structure.  
  
## Members  
  
### Methods  
  
|||  
|-|-|  
|[IAccessorImpl](../../data/oledb/iaccessorimpl-class.md)|The constructor.|  
  
### Interface Methods  
  
|||  
|-|-|  
|[AddRefAccessor](../../data/oledb/iaccessorimpl-addrefaccessor.md)|Adds a reference count to an existing accessor.|  
|[CreateAccessor](../../data/oledb/iaccessorimpl-createaccessor.md)|Creates an accessor from a set of bindings.|  
|[GetBindings](../../data/oledb/iaccessorimpl-getbindings.md)|Returns the bindings in an accessor.|  
|[ReleaseAccessor](../../data/oledb/iaccessorimpl-releaseaccessor.md)|Releases an accessor.|  
  
## Remarks  
 This is mandatory on rowsets and commands. OLE DB requires providers to implement an **HACCESSOR**, which is a tag to an array of [DBBINDING](https://msdn.microsoft.com/en-us/library/ms716845.aspx) structures. **HACCESSOR**s provided by `IAccessorImpl` are addresses of the `BindType` structures. By default, `BindType` is defined as an **ATLBINDINGS** in `IAccessorImpl`'s template definition. `BindType` provides a mechanism used by `IAccessorImpl` to track the number of elements in its **DBBINDING** array as well as a reference count and accessor flags.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [OLE DB Provider Templates](../../data/oledb/ole-db-provider-templates-cpp.md)   
 [OLE DB Provider Template Architecture](../../data/oledb/ole-db-provider-template-architecture.md)