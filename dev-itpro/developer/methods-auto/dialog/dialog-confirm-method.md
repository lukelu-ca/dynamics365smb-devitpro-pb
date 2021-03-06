---
title: "Confirm Method"
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
# Confirm Method
Creates a dialog box that prompts the user for a yes or no answer. The dialog box is centered on the screen.


## Syntax
```
Ok :=   Dialog.Confirm(String: String, [Default: Boolean], [Value1: Any,...])
```
> [!NOTE]  
> This method can be invoked without specifying the data type name.  
## Parameters
*String*  
&emsp;Type: [String](../string/string-data-type.md)  
Specifies the string that is displayed in the dialog box. Use a backslash (\) to indicate a new line. The string can be a text constant that is enabled for multilanguage functionality.
        
*Default*  
&emsp;Type: [Boolean](../boolean/boolean-data-type.md)  
Specifies the default button. If you do not specify a default button, then No is used as the default button.  
*Value1*  
&emsp;Type: [Any](../any/any-data-type.md)  
  


## Return Value
*Ok*  
&emsp;Type: [Boolean](../boolean/boolean-data-type.md)  
  


[//]: # (IMPORTANT: END>DO_NOT_EDIT)

## Remarks  
 The message window is automatically sized. The height of the window corresponds to the number of lines and the width corresponds to the length of the longest line.  

 We recommend that you always end CONFIRM messages with a question mark. For more information about best practices for end-user messages, see [Progress Windows, MESSAGE, ERROR, and CONFIRM Methods](../../devenv-progress-windows-message-error-and-confirm-methods.md).  

## Example  
 In the following example, the Dialog.CONFIRM method prompts the user for a **true** or **false** answer. This code example requires that you create the following variables.  

|Name|DataType|  
|----------|--------------|  
|Question|Text|  
|Answer|Boolean|  
|CustomerNo|Integer|  

 This code example requires that you create the following text constants.  

|Name|ConstValue|  
|----------|----------------|  
|Text000|Exit without saving changes to customer %1?|  
|Text001|You selected %1.|  

```  
CustomerNo := 01121212;  
Question := Text000;  
Answer := Dialog.CONFIRM(Question, TRUE, CustomerNo);  
MESSAGE(Text001, Answer);  
```  

 The first dialog box shows:  

 **Exit without saving changes to customer 1121212?**  

 If you select the default **true** value, then the second dialog box is shown:  

 **You selected true.**  


## See Also
[Dialog Data Type](dialog-data-type.md)  
[Getting Started with AL](../../devenv-get-started.md)  
[Developing Extensions](../../devenv-dev-overview.md)