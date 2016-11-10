---
title: "Program Control"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "debugging [Debugging SDK], control of execution"
ms.assetid: 6be80904-e66c-4cae-8891-1113b799fb01
caps.latest.revision: 9
ms.author: "gregvanl"
manager: "ghogen"
translation.priority.mt: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# Program Control
In Visual Studio debugging, all of the following stepping and continuing routines occur at the program level:  
  
-   Setting the next statement, that is, setting your computer to the next instruction to be executed in a particular frame environment  
  
-   Executing, that is, continuing to exit out of stepping mode  
  
-   Stepping to the next instruction  
  
-   Continuing with the current stepping mode  
  
-   Suspending the threads contained by the program  
  
-   Resuming the threads contained by the program  
  
> [!NOTE]
>  Viewing the call stack is implemented on the thread level. To enumerate the frame information when viewing the call stack for a thread, you must implement all the methods of the [IEnumDebugFrameInfo2](../extensibility/ienumdebugframeinfo2.md) interface.  
  
## Methods of Program Control  
 The following table shows the methods of [IDebugProgram2](../extensibility/idebugprogram2.md) that must be implemented for a minimally functional debug engine (DE) and execution control.  
  
|Method|Description|  
|------------|-----------------|  
|[IDebugProgram2::Execute](../extensibility/idebugprogram2--execute.md)|Continues running all threads contained by a program from a stopped state. Required for execution control.|  
|[IDebugProgram2::Continue](../extensibility/idebugprogram2--continue.md)|Continues running all threads contained by a program from a stopped state. Required for execution control.|  
|[IDebugProgram2::Step](../extensibility/idebugprogram2--step.md)|Performs a step on the given thread. Continues running all other threads contained by the program. Required for execution control.|  
  
 For multithreaded programs, you must also implement the [IDebugProgram2::EnumThreads](../extensibility/idebugprogram2--enumthreads.md) method and all the methods of the [IEnumDebugThreads2](../extensibility/ienumdebugthreads2.md) interface.  
  
## See Also  
 [Execution Control and State Evaluation](../extensibility/execution-control-and-state-evaluation.md)