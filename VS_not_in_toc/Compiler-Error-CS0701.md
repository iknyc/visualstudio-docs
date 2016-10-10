---
title: "Compiler Error CS0701"
ms.custom: na
ms.date: 10/02/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: eb844e31-00bd-468d-9f77-11d10a4ef120
caps.latest.revision: 13
manager: douge
translation.priority.ht: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - ru-ru
  - zh-cn
  - zh-tw
translation.priority.mt: 
  - cs-cz
  - pl-pl
  - pt-br
  - tr-tr
---
# Compiler Error CS0701
'identifier' is not a valid constraint. A type used as a constraint must be an interface, a non-sealed class or a type parameter.  
  
 This error occurs if a sealed type is used as a constraint. To resolve this error, use only non-sealed types as constraints.  
  
## Example  
 The following sample generates CS0701.  
  
```  
// CS0701.cs  
// compile with: /target:library  
class C<T> where T : System.String {}   // CS0701  
class D<T> where T : System.Attribute {}   // OK  
```