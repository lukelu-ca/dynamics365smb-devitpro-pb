---
title: "AsInteger Method"
ms.author: solsen
ms.custom: na
ms.date: 04/01/2019
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: "dynamics365-business-central"
ms.assetid: 620f0e32-eadc-43e9-8f6e-8fc0b12c3aaf
caps.latest.revision: 9
manager: edupont
author: SusanneWindfeldPedersen
redirect_url: /dynamics365/business-central/dev-itpro/developer/methods-auto/library
---
<!--This topic is deprected, see redirection URL-->

 

# AsInteger Method

Converts the value in a JsonValue to an **Integer** data type.

```
Integer := JsonValue.AsInteger
```

## Parameters
*JsonValue*  
&emsp;Type: [JsonValue](jsonvalue-class.md)

## Return Value
&emsp;Type: [Integer](../datatypes/devenv-integer-data-type.md)

## Remarks
If the JsonValue does not contain a number which can be converted without loss of precision to an Integer, the operation will fail with a run-time error.

## See Also
[Getting Started with AL](../devenv-get-started.md)  
[Developing Extensions](../devenv-dev-overview.md)
