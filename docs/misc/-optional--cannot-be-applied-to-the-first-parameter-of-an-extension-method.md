---
title: "&#39;Optional&#39; cannot be applied to the first parameter of an extension method"
ms.custom: na
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "bc36553"
  - "vbc36553"
helpviewer_keywords: 
  - "BC36553"
ms.assetid: 8ea0b90c-f155-47a9-988b-5b8009b510af
caps.latest.revision: 19
ms.author: "billchi"
manager: "douge"
translation.priority.ht: 
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "ru-ru"
  - "zh-cn"
  - "zh-tw"
translation.priority.mt: 
  - "cs-cz"
  - "pl-pl"
  - "pt-br"
  - "tr-tr"
---
# &#39;Optional&#39; cannot be applied to the first parameter of an extension method
'Optional' cannot be applied to the first parameter of an extension method. The first parameter specifies which type to extend.  
  
 The first parameter of an extension method specifies the data type that the method extends. When the method is executed, the first parameter is bound to the instance of the data type that invokes the method. Therefore, the first parameter is required and cannot be optional.  
  
 The restriction applies only to the first parameter. Other parameters can be optional or not, following the same rules as in any other method. For more information, see [Parameter List](../Topic/Parameter%20List%20\(Visual%20Basic\).md).  
  
 **Error ID:** BC36553  
  
### To correct this error  
  
-   If you want the current first parameter to specify the data type being extended, remove the `Optional` keyword.  
  
-   If the current first parameter is a standard parameter to the method and you do not want it to represent the data type being extended, add a new first parameter.  
  
## Example  
 The first parameter in the following example is the only indication that the `Print` method extends the `String` data type. Therefore, it cannot be optional.  
  
```  
<Extension()>  
Public Sub Print (ByVal str As String)  
    Console.WriteLine(str)  
End Sub  
```  
  
 When the extension method is called as follows, parameter `str` in the method is bound to `greeting`, the instance of `String` that calls `Print`. The compiler uses `greeting` as the argument to extension method `Print`.  
  
```  
Dim greeting As String = "Hello"  
greeting.Print()  
```  
  
## See Also  
 [Extension Methods](../Topic/Extension%20Methods%20\(Visual%20Basic\).md)   
 [How to: Define Optional Parameters for a Procedure (Visual Basic)](assetId:///0b32b312-0da0-489b-96ad-7dcb1f1f8f88)   
 [Optional Parameters](../Topic/Optional%20Parameters%20\(Visual%20Basic\).md)