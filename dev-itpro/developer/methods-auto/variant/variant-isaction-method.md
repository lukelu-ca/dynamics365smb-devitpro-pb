---
title: "IsAction Method"
ms.author: solsen
ms.custom: na
ms.date: 04/01/2019
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: "dynamics365-business-central"
author: solsen
---
[//]: # (START>DO_NOT_EDIT)
[//]: # (IMPORTANT:Do not edit any of the content between here and the END>DO_NOT_EDIT.)
[//]: # (Any modifications should be made in the .xml files in the ModernDev repo.)
# IsAction Method
Indicates whether an AL variant contains an Action variable.


## Syntax
```
Ok :=   Variant.IsAction()
```
> [!NOTE]  
> This method can be invoked using property access syntax.  

## Parameters
*Variant*  
&emsp;Type: [Variant](variant-data-type.md)  
An instance of the [Variant](variant-data-type.md) data type.  

## Return Value
*Ok*  
&emsp;Type: [Boolean](../boolean/boolean-data-type.md)  
**true** if the AL variant contains an Action variable, otherwise **false**.  


[//]: # (IMPORTANT: END>DO_NOT_EDIT)

## Example  
 The following example determines whether an AL variant contains an Automation variable. The MyAutomation variable is assigned to the variant variable that is named MyVariant. The **ISAUTOMATION** method determines whether the variant contains an Automation variable and stores the return value in the varResult variable. In this case, the variant contains an Automation variable so **Yes** is returned and displayed in a message box. The [ISCODE Method (Variant)](../../methods/devenv-iscode-method-variant.md) determines whether the variant contains a code variable. The return value is **No** because the variant does not contain a code. This example requires that you create the following global variables and text constants.  
  
|Variable name|DataType|Subtype|  
|-------------------|--------------|-------------|  
|MyAutomation|Automation|AFormAut 1.0 Type Library|  
|MyVariant|Variant|Not applicable|  
|varResult|Boolean|Not applicable|  
  
|Text constant name|ConstValue|  
|------------------------|----------------|  
|Text000|Does the variant contain an Automation variable? %1|  
|Text001|Does the variant contain a code variable? %1|  
  
```  
MyVariant := MyAutomation;  
varResult := MyVariant.ISAUTOMATION;  
MESSAGE(Text000,varResult);  
varResult := MyVariant.ISCODE;  
MESSAGE(Text001, varResult);  
```  
  

## See Also
[Variant Data Type](variant-data-type.md)  
[Getting Started with AL](../../devenv-get-started.md)  
[Developing Extensions](../../devenv-dev-overview.md)