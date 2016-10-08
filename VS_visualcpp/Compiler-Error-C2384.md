---
title: "Compiler Error C2384"
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
ms.topic: error-reference
ms.assetid: 8145f7ad-31b1-406d-ac43-0d557feab635
caps.latest.revision: 15
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
# Compiler Error C2384
'member' : cannot apply __declspec(thread) to a member of a managed or WinRT class  
  
 The [thread](../VS_visualcpp/thread.md) `__declspec` modifier cannot be used on a member of a managed or Windows Runtime class.  
  
 Static thread local storage in managed code can only be used for statically loaded DLLs—the DLL must be statically loaded when the process starts. Windows Runtime does not support thread local storage.  
  
 The following line generates C2384 and shows how to fix it in C++/CLI code:  
  
```  
// C2384.cpp  
// compile with: /clr /c  
public ref class B {  
public:  
   __declspec( thread ) static int tls_i = 1;   // C2384  
  
   // OK - declare with attribute instead  
   [System::ThreadStaticAttribute]  
   static int tls_j;  
};  
```