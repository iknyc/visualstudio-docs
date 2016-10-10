---
title: "Data (Debug Interface Access SDK)"
ms.custom: na
ms.date: 10/03/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-debug
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0f17e96a-2e06-42c9-a877-3e5e670ee0ef
caps.latest.revision: 17
manager: ghogen
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
# Data (Debug Interface Access SDK)
All variables, such as parameters, local variables, global variables, and class members, are identified by `SymTagData` symbols. Constant values (`LocIsConstant`) are also identified with this type.  
  
## Properties  
 The following table shows the properties that are valid for this symbol type.  
  
|Property|Data type|Description|  
|--------------|---------------|-----------------|  
|[IDiaSymbol::get_access](../VS_debugger/IDiaSymbol--get_access.md)|`DWORD`|If a field, then one of the values of the [CV_access_e Enumeration](../VS_debugger/CV_access_e.md).|  
|[IDiaSymbol::get_addressOffset](../VS_debugger/IDiaSymbol--get_addressOffset.md)|`DWORD`|Offset part of location; for details, see the [LocationType Enumeration](../VS_debugger/LocationType.md).|  
|[IDiaSymbol::get_addressSection](../VS_debugger/IDiaSymbol--get_addressSection.md)|`DWORD`|Section part of location; for details, see the [LocationType Enumeration](../VS_debugger/LocationType.md).|  
|[IDiaSymbol::get_addressTaken](../VS_debugger/IDiaSymbol--get_addressTaken.md)|`BOOL`|`TRUE` if this data's address is referenced by another symbol.|  
|[IDiaSymbol::get_bitPosition](../VS_debugger/IDiaSymbol--get_bitPosition.md)|`DWORD`|Bit position of location; for details, see the [LocationType Enumeration](../VS_debugger/LocationType.md) (not supported in DIA SDK v8.0).|  
|[IDiaSymbol::get_classParent](../VS_debugger/IDiaSymbol--get_classParent.md)|`IDiaSymbol*`|Symbol for the class, if this is a structure, union, or class field.|  
|[IDiaSymbol::get_classParentId](../VS_debugger/IDiaSymbol--get_classParentId.md)|`DWORD`|ID of the class parent symbol.|  
|[IDiaSymbol::get_compilerGenerated](../VS_debugger/IDiaSymbol--get_compilerGenerated.md)|`BOOL`|`TRUE` if the data was generated by the compiler.|  
|[IDiaSymbol::get_constType](../VS_debugger/IDiaSymbol--get_constType.md)|`BOOL`|`TRUE` if the data is marked as being constant.|  
|[IDiaSymbol::get_dataKind](../VS_debugger/IDiaSymbol--get_dataKind.md)|`DWORD`|One of the [DataKind Enumeration](../VS_debugger/DataKind.md) values.|  
|[IDiaSymbol::get_isAggregated](../VS_debugger/IDiaSymbol--get_isAggregated.md)|`BOOL`|`TRUE` if the data is part of an aggregated data type (only in DIA SDK v8.0 and later).|  
|[IDiaSymbol::get_isSplitted](../VS_debugger/IDiaSymbol--get_isSplitted.md)|`BOOL`|`TRUE` if data is has been split into an aggregate of multiple symbols (only in DIA SDK v8.0 and later).|  
|[IDiaSymbol::get_length](../VS_debugger/IDiaSymbol--get_length.md)|`ULONGLONG`|Length of bitfield; for details, see the [LocationType Enumeration](../VS_debugger/LocationType.md).|  
|[IDiaSymbol::get_lexicalParent](../VS_debugger/IDiaSymbol--get_lexicalParent.md)|`IDiaSymbol*`|Symbol for the enclosing compiland, function, or block.|  
|[IDiaSymbol::get_lexicalParentId](../VS_debugger/IDiaSymbol--get_lexicalParentId.md)|`DWORD`|ID of the lexical parent symbol.|  
|[IDiaSymbol::get_locationType](../VS_debugger/IDiaSymbol--get_locationType.md)|`DWORD`|Any of the allowable location types; for details, see [Symbol Locations](../VS_debugger/Symbol-Locations.md)|  
|[IDiaSymbol::get_name](../VS_debugger/IDiaSymbol--get_name.md)|`BSTR`|Name of the variable.|  
|[IDiaSymbol::get_offset](../VS_debugger/IDiaSymbol--get_offset.md)|`LONG`|Offset from register contents; for details, see the [LocationType Enumeration](../VS_debugger/LocationType.md).|  
|[IDiaSymbol::get_registerId](../VS_debugger/IDiaSymbol--get_registerId.md)|`DWORD`|Register designator of location; for details, see the [LocationType Enumeration](../VS_debugger/LocationType.md).|  
|[IDiaSymbol::get_relativeVirtualAddress](../VS_debugger/IDiaSymbol--get_relativeVirtualAddress.md)|`DWORD`|Relative position of the data within its block.|  
|[IDiaSymbol::get_slot](../VS_debugger/IDiaSymbol--get_slot.md)|`DWORD`|Gets slot number of the data.|  
|[IDiaSymbol::get_symIndexId](../VS_debugger/IDiaSymbol--get_symIndexId.md)|`DWORD`|Index ID of symbol.|  
|[IDiaSymbol::get_symTag](../VS_debugger/IDiaSymbol--get_symTag.md)|`DWORD`|Returns `SymTagData` (one of the [SymTagEnum Enumeration](../VS_debugger/SymTagEnum.md) values).|  
|[IDiaSymbol::get_token](../VS_debugger/IDiaSymbol--get_token.md)|`DWORD`|The metadata token representing the data.|  
|[IDiaSymbol::get_type](../VS_debugger/IDiaSymbol--get_type.md)|`IDiaSymbol*`|Symbol for the variable type.|  
|[IDiaSymbol::get_typeId](../VS_debugger/IDiaSymbol--get_typeId.md)|`DWORD`|ID of the variable type symbol.|  
|[IDiaSymbol::get_unalignedType](../VS_debugger/IDiaSymbol--get_unalignedType.md)|`BOOL`|`TRUE` if the data is unaligned.|  
|[IDiaSymbol::get_value](../VS_debugger/IDiaSymbol--get_value.md)|`VARIANT`|The value of constant data.|  
|[IDiaSymbol::get_virtualAddress](../VS_debugger/IDiaSymbol--get_virtualAddress.md)|`ULONGLONG`|Position of the data within the executable.|  
|[IDiaSymbol::get_volatileType](../VS_debugger/IDiaSymbol--get_volatileType.md)|`BOOL`|`TRUE` if the data is marked as volatile.|  
  
## See Also  
 [CV_access_e Enumeration](../VS_debugger/CV_access_e.md)   
 [DataKind Enumeration](../VS_debugger/DataKind.md)   
 [Lexical Hierarchy of Symbol Types](../VS_debugger/Lexical-Hierarchy-of-Symbol-Types.md)   
 [LocationType Enumeration](../VS_debugger/LocationType.md)   
 [Symbol Locations](../VS_debugger/Symbol-Locations.md)