---
title: "CAutoPtrList Class"
ms.custom: na
ms.date: 10/03/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 11de4aca-28b0-4ff2-a74a-cb602312ffbd
caps.latest.revision: 14
manager: ghogen
translation.priority.ht: 
  - cs-cz
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pl-pl
  - pt-br
  - ru-ru
  - tr-tr
  - zh-cn
  - zh-tw
---
# CAutoPtrList Class
This class provides methods useful when constructing a list of smart pointers.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```  
template<  
    typename E>  
    class CAutoPtrList : public CAtlList<  
    ATL::CAutoPtr< E  
   >,  
    CAutoPtrElementTraits< E>>  
```  
  
#### Parameters  
 `E`  
 The pointer type.  
  
## Members  
  
### Public Constructors  
  
|Name|Description|  
|----------|-----------------|  
|[CAutoPtrList::CAutoPtrList](../Topic/CAutoPtrList::CAutoPtrList.md)|The constructor.|  
  
## Remarks  
 This class provides a constructor and derives methods from [CAtlList](../VS_visualcpp/CAtlList-Class.md) and [CAutoPtrElementTraits](../VS_visualcpp/CAutoPtrElementTraits-Class.md) to aid the creation of a list object storing smart pointers. The class [CAutoPtrArray](../VS_visualcpp/CAutoPtrArray-Class.md) provides a similar function for an array object.  
  
 For more information, see [ATL Collection Classes](../VS_visualcpp/ATL-Collection-Classes.md).  
  
## Inheritance Hierarchy  
 [CAtlList](../VS_visualcpp/CAtlList-Class.md)  
  
 `CAutoPtrList`  
  
## Requirements  
 **Header:** atlcoll.h  
  
##  <a name="cautoptrlist__cautoptrlist"></a>  CAutoPtrList::CAutoPtrList  
 The constructor.  
  
```  
CAutoPtrList(    UINT nBlockSize = 10 ) throw();  
```  
  
### Parameters  
 `nBlockSize`  
 The block size, with a default of 10.  
  
### Remarks  
 The block size is a measure of the amount of memory allocated when a new element is required. Larger block sizes reduce calls to memory allocation routines, but use more resources.  
  
## See Also  
 [CAtlList Class](../VS_visualcpp/CAtlList-Class.md)   
 [CAutoPtrElementTraits Class](../VS_visualcpp/CAutoPtrElementTraits-Class.md)   
 [Class Overview](../VS_visualcpp/ATL-Class-Overview.md)