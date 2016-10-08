---
title: "Compiler Error C2019"
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
ms.assetid: 4f37b1e1-9eca-418f-a4c3-141e8512d7b6
caps.latest.revision: 7
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
# Compiler Error C2019
expected preprocessor directive, found 'character'  
  
 The character followed a `#` sign but it is not the first letter of a preprocessor directive.  
  
 The following sample generates C2019:  
  
```  
// C2019.cpp  
#!define TRUE 1   // C2019  
```  
  
 Possible resolution:  
  
```  
// C2019b.cpp  
// compile with: /c  
#define TRUE 1  
```