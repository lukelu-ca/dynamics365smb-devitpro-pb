---
title: "ISSESSIONACTIVE Method (Debugger)"
author: edupont04
manager: edupont04
ms.custom: na
ms.date: 04/01/2019
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
redirect_url: /dynamics365/business-central/dev-itpro/developer/methods-auto/library
---

 

# ISSESSIONACTIVE Method (Session)
Tests if the specified SessionID is active on the [!INCLUDE[d365fin_server_md](../includes/d365fin_server_md.md)] instance where it was started.  

## Syntax  

```  
Ok := ISSESSIONACTIVE(SessionID)   
```  

## Parameters
*SessionID*
    Type: Integer
    The ID of the session that you want to test if it is still active.
## Property Value/Return Value  
Type: Boolean  

**True** if a session with a specified ID is active on the [!INCLUDE[d365fin_server_md](../includes/d365fin_server_md.md)] instance; otherwise, **false**.  

## Remarks
Use this method to test if a session has completed or is still active, for example if you want to check that a session started with STARTSESSION is still running.  

>   [!NOTE]  
>    The method looks for sessions on the local machine.


## See Also  
[STARTSESSION](devenv-STARTSESSION-Method-Sessions.md)  
