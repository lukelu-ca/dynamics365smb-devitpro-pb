---
title: "COPYSTREAM Method"
ms.custom: na
ms.date: 04/01/2019
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
ms.assetid: e4fcfe56-27f2-4d8e-9bfa-798fe6a70c5e
author: SusanneWindfeldPedersen
redirect_url: /dynamics365/business-central/dev-itpro/developer/methods-auto/library
---

 

# COPYSTREAM Method
Copies the information that is contained in an InStream to an OutStream.  

## Syntax  

```  

[Ok :=] COPYSTREAM(OutStream, InStream)  
```  

#### Parameters  
 *OutStream*  
 Type: OutStream  

 The OutStream object to which you will copy the information; the destination stream.  

 *InStream*  
 Type: InStream  

 The InStream object from which you want to copy; the source stream.  

## Property Value/Return Value  
 Type: Boolean  

 Specifies whether the data was copied.  

## Example  
 This example requires that you create the following variables.  

|Variable name|DataType|  
|-------------------|--------------|  
|F1|File|  
|F2|File|  
|InS|InStream|  
|OutS|OutStream|  

```  
F1.OPEN('c:\Test.txt');  
F1.CREATEINSTREAM(InS);  
F2.CREATE('c:\CopyTest.txt');  
F2.CREATEOUTSTREAM(OutS);  
COPYSTREAM(OutS,InS);  
F1.CLOSE();  
F2.CLOSE();  
```  

## See Also  
 [InStream and OutStream Data Types](../datatypes/devenv-InStream-and-OutStream-Data-Types.md)
