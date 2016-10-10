---
title: "Browse and Select a .NET Type Dialog Box"
ms.custom: na
ms.date: 10/02/2016
ms.prod: .net-framework-4.6
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: reference
ms.assetid: 864b60b6-a070-4e5c-aa5b-a25341b57ea6
caps.latest.revision: 13
manager: erikre
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
# Browse and Select a .NET Type Dialog Box
In the **Properties** window, dialog boxes, or designers such as the variable designer, when you select **Browse for Types…** from a list of data types, is the **Browse and Select a .NET Type** dialog box (referred to in an abbreviated form as the “type browser”). In this dialog box, you can choose a type from a tree view of assemblies and projects.  
  
 This dialog box is employed in a number of user scenarios, including the following:  
  
-   When setting the type of a variable or argument.  
  
-   When selecting a type for a generic activity.  
  
-   When adding a catch on the <xref:System.Activities.Statements.TryCatch?qualifyHint=False> activity.  
  
> [!NOTE]
>  The type browser can display Visual Basic jagged array types, but not multidimensional array types. See [Jagged Arrays](http://go.microsoft.com/fwlink/?LinkId=195226) and [Multidimensional Arrays](http://go.microsoft.com/fwlink/?LinkId=195227) for details.  
  
## Selecting a Value or Reference Type from the Type Browser  
  
#### To select a value or reference type from the type browser  
  
1.  In the **Type Name** box, enter the name of the type that you want to use.  
  
2.  Do one of the following:  
  
    -   Once the name of the type that you want to use appears in the tree in the **Type Name** box, double-click the type to select it.  
  
    -   Type enough characters in the **Type Name** box to uniquely identify the type that you want to use and then press enter to select the type  
  
#### To select a generic type from the type browser  
  
1.  In the **Type Name** box, type in the name of the type that you want to use.  
  
2.  Once the name of the type that you want to use appears in the tree in the **Type Name** box, click the type to select it to cause drop-down boxes appear.  
  
     Select the type that you want to use to close the generic from the drop-down boxes, and then click **OK**.  
  
## Types displayed in the type browser  
 The types displayed in the type browser can vary depending on how the type browser was launched. If the type browser was launched from a workflow project inside of **vs2010**, by default all of the types in the referenced assemblies and referenced projects are shown. If the type browser was launched from outside of a **vs2010** project system (such as in a rehosted workflow application or in a standalone workflow file), then by default the types from all of the assemblies loaded in the AppDomain are shown.  
  
 Types in the type browser can be filtered by activity designer developers. For any given activity, you may see just a subset of the types. For example, in the <xref:System.Activities.Statements.TryCatch?qualifyHint=False> activity, only types derived from <xref:System.Exception?qualifyHint=False> are shown in the type browser.  
  
## Filtering Search Results in the Type Browser  
 The list of types in the **Type Name** box gets shorter as you type more characters to find a match. Only types whose fully-qualified name begins with the string you have typed or types whose short name begins with the string that you have typed appear in the filtered list.  
  
 For example:  
  
1.  Typing **Operation** matches <xref:System.OperationCanceledException?qualifyHint=False> but not <xref:System.InvalidOperationException?qualifyHint=False>. To match <xref:System.InvalidOperationException?qualifyHint=False>, start typing System.I or Invalid.  
  
2.  Typing **Generic** matches <xref:System.GenericUriParser?qualifyHint=False> but not types in the <xref:System.Collections.Generic?qualifyHint=False> namespace. To search for types in the <xref:System.Collections.Generic?qualifyHint=False> namespace, type the fully-qualified name of the namespace.  
  
## Selecting a service contract using the type browser dialog  
 When selecting a service contract type, the type browser only shows types that have the <xref:System.ServiceModel.ServiceContractAttribute?qualifyHint=False> attribute.  
  
## See Also  
 [Using the Activity Designers](../WF_Design/Using-the-Activity-Designers.md)