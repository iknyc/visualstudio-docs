---
title: "IDebugThread2"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "IDebugThread2"
helpviewer_keywords: 
  - "IDebugThread2 interface"
ms.assetid: 221b4b1b-4a26-466e-bc29-5eff800fab13
caps.latest.revision: 12
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
# IDebugThread2
This interface represents a thread running in a program.  
  
## Syntax  
  
```  
IDebugThread2 : IUnknown  
```  
  
## Notes for Implementers  
 The debug engine (DE) implements this interface to represent a thread of execution in a single program.  
  
## Notes for Callers  
 Call [GetThread](../extensibility/idebugstackframe2--getthread.md) to obtain this interface representing the currently active thread.  
  
 This interface is also used in creating a breakpoint request (see [BP_REQUEST_INFO](../extensibility/bp_request_info.md)).  
  
 This interface is also returned when resolving a bound or error breakpoint (see [BP_RESOLUTION_INFO](../extensibility/bp_resolution_info.md) and [BP_ERROR_RESOLUTION_INFO](../extensibility/bp_error_resolution_info.md)).  
  
## Methods in Vtable Order  
 The following table shows the methods of `IDebugThread2`.  
  
|Method|Description|  
|------------|-----------------|  
|[EnumFrameInfo](../extensibility/idebugthread2--enumframeinfo.md)|Retrieves a list of the stack frames for this thread.|  
|[GetName](../extensibility/idebugthread2--getname.md)|Gets the name of the thread.|  
|[SetThreadName](../extensibility/idebugthread2--setthreadname.md)|Sets the name of the thread.|  
|[GetProgram](../extensibility/idebugthread2--getprogram.md)|Gets the program in which a thread is running.|  
|[CanSetNextStatement](../extensibility/idebugthread2--cansetnextstatement.md)|Determines whether the next statement can be set to the given stack frame and code context.|  
|[SetNextStatement](../extensibility/idebugthread2--setnextstatement.md)|Sets the next statement to the given stack frame and code context.|  
|[GetThreadId](../extensibility/idebugthread2--getthreadid.md)|Gets the system thread identifier.|  
|[Suspend](../extensibility/idebugthread2--suspend.md)|Suspends a thread.|  
|[Resume](../extensibility/idebugthread2--resume.md)|Resumes a thread.|  
|[GetThreadProperties](../extensibility/idebugthread2--getthreadproperties.md)|Gets properties that describe a thread.|  
|[GetLogicalThread](../extensibility/idebugthread2--getlogicalthread.md)|Gets the logical thread associated with this physical thread.|  
  
## Remarks  
 Because a single physical thread can run in multiple programs, more than one `IDebugThread2` from more than one program can represent the same physical thread.  
  
 When a breakpoint or exception occurs, an event is sent by calling [Event](../extensibility/idebugeventcallback2--event.md). One of the arguments to this method is an `IDebugThread2` interface representing the current thread. [EnumFrameInfo](../extensibility/idebugthread2--enumframeinfo.md) is used to obtain the [IDebugStackFrame2](../extensibility/idebugstackframe2.md) interface for the current stack frame.  
  
## Requirements  
 Header: msdbg.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Core Interfaces](../extensibility/core-interfaces.md)   
 [Event](../extensibility/idebugeventcallback2--event.md)   
 [GetThread](../extensibility/idebugstackframe2--getthread.md)   
 [BP_REQUEST_INFO](../extensibility/bp_request_info.md)   
 [BP_RESOLUTION_INFO](../extensibility/bp_resolution_info.md)   
 [BP_ERROR_RESOLUTION_INFO](../extensibility/bp_error_resolution_info.md)