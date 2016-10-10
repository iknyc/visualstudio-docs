---
title: "CA1002: Do not expose generic lists"
ms.custom: na
ms.date: 10/03/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-devops-test
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5caac810-1a79-47df-a27b-c46c5040bf34
caps.latest.revision: 20
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
# CA1002: Do not expose generic lists
|||  
|-|-|  
|TypeName|DoNotExposeGenericLists|  
|CheckId|CA1002|  
|Category|Microsoft.Design|  
|Breaking Change|Breaking|  
  
## Cause  
 A type contains an externally visible member that is a <xref:System.Collections.Generic.List`1?qualifyHint=True> type, returns a <xref:System.Collections.Generic.List`1?qualifyHint=True> type, or whose signature includes a <xref:System.Collections.Generic.List`1?qualifyHint=True> parameter.  
  
## Rule Description  
 <xref:System.Collections.Generic.List`1?qualifyHint=True> is a generic collection that is designed for performance and not inheritance. <xref:System.Collections.Generic.List`1?qualifyHint=True> does not contain virtual members that make it easier to change the behavior of an inherited class. The following generic collections are designed for inheritance and should be exposed instead of <xref:System.Collections.Generic.List`1?qualifyHint=True>.  
  
-   <xref:System.Collections.ObjectModel.Collection`1?qualifyHint=True>  
  
-   <xref:System.Collections.ObjectModel.ReadOnlyCollection`1?qualifyHint=True>  
  
-   <xref:System.Collections.ObjectModel.KeyedCollection`2?qualifyHint=True>  
  
## How to Fix Violations  
 To fix a violation of this rule, change the <xref:System.Collections.Generic.List`1?qualifyHint=True> type to one of the generic collections that is designed for inheritance.  
  
## When to Suppress Warnings  
 Do not suppress a warning from this rule unless the assembly that raises this warning is not meant to be a reusable library. For example, it would be safe to suppress this warning in a performance tuned application where a performance benefit was gained from the use of generic lists.  
  
## Related Rules  
 [CA1005: Avoid excessive parameters on generic types](../VS_IDE/CA1005--Avoid-excessive-parameters-on-generic-types.md)  
  
 [CA1010: Collections should implement generic interface](../VS_IDE/CA1010--Collections-should-implement-generic-interface.md)  
  
 [CA1000: Do not declare static members on generic types](../VS_IDE/CA1000--Do-not-declare-static-members-on-generic-types.md)  
  
 [CA1006: Do not nest generic types in member signatures](../VS_IDE/CA1006--Do-not-nest-generic-types-in-member-signatures.md)  
  
 [CA1004: Generic methods should provide type parameter](../VS_IDE/CA1004--Generic-methods-should-provide-type-parameter.md)  
  
 [CA1003: Use generic event handler instances](../VS_IDE/CA1003--Use-generic-event-handler-instances.md)  
  
 [CA1007: Use generics where appropriate](../VS_IDE/CA1007--Use-generics-where-appropriate.md)  
  
## See Also  
 [Generics](../Topic/Generics%20\(C%23%20Programming%20Guide\).md)