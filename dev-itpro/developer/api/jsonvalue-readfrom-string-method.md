---
title: "ReadFrom_String Method"
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

 

# ReadFrom_String Method

Reads the JSON data from the string into a JsonValue variable.

```
[Ok := ] JsonValue.ReadFrom(String)
```

## Parameters
*JsonValue*  
&emsp;Type: [JsonValue](jsonvalue-class.md)

*String*  
&emsp;Type: [String](../datatypes/devenv-text-data-type.md)

The String object from which the JSON data will be read.

## Property Value/Return Value
&emsp;Type: [Boolean](../datatypes/devenv-boolean-data-type.md)

**True** if the read was successful; otherwise, **false**.

If you omit this optional return value and if the read does not execute successfully, then a run-time error occurs.

## Remarks
1. This method can fail if the JSON data is malformed..
2. If the operation succeeds, the JsonValue will be disconnected from its current JSON tree and the data contained by the JsonValue will be replaced with the new value.
3. To delete the contents in a JsonValue variable use the Clear function.

To delete the contents in a JsonValue variable use the **Clear** function.

```
Clear(JsonValue)
```

## Example
This example shows how to read JSON data from a string into a **JsonValue** variable.

```
local procedure ReadJson(data : Text) result : JsonValue;
begin
    result.ReadFrom(data);    
end;

```

## See Also
[Getting Started with AL](../devenv-get-started.md)  
[Developing Extensions](../devenv-dev-overview.md)
