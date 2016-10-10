---
title: "&#39;System.Nullable&#39; does not satisfy the &#39;Structure&#39; constraint for type parameter &#39;&lt;typeparametername&gt;&#39;"
ms.custom: na
ms.date: 10/01/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 98053645-fa76-4826-a7c1-f1bdf3511863
caps.latest.revision: 9
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
# &#39;System.Nullable&#39; does not satisfy the &#39;Structure&#39; constraint for type parameter &#39;&lt;typeparametername&gt;&#39;
A generic type is invoked passing a type argument of <xref:System.Nullable`1?qualifyHint=False> to a type parameter with a `Structure` constraint.  
  
 The common language runtime (CLR) specifically disallows the <xref:System.Nullable`1?qualifyHint=False> structure as a type argument to itself. Even though it is a structure and would otherwise satisfy a `Structure` constraint, using it recursively could lead to awkward constructions such as `Nullable(Of Nullable(Of Nullable))`.  
  
 **Error ID:** BC32115  
  
### To correct this error  
  
-   Either remove the `Structure` constraint from the type parameter, or change the type argument to some value type other than <xref:System.Nullable`1?qualifyHint=False>.  
  
## See Also  
 <xref:System.Nullable`1?qualifyHint=False>   
 [Generic Types in Visual Basic](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Structure (Visual Basic)](assetId:///263ce115-ac36-4c05-8cb7-0e0eead5c6d0)