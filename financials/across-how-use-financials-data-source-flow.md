---
title: Forbinde dataene med Flow | Microsoft Docs
description: "Du kan gøre dine Financials-data tilgængelige som datakilde og angive en OData URL-adresse til dine webtjenester for at oprette et automatiseret workflow."
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 277dda7c954380138af1ecabc02d77121f35aac7
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="using-included365finincludesd365finmdmd-in-an-automated-workflow"></a>Bruge [!INCLUDE[d365fin](includes/d365fin_md.md)] i et automatisk workflow
Du kan bruge dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data som en del af en arbejdsproces i Microsoft Flow.  

> [!NOTE]  
>   Du skal have en gyldig konto til [!INCLUDE[d365fin](includes/d365fin_md.md)] og til Flow.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>Sådan tilføjes [!INCLUDE[d365fin](includes/d365fin_md.md)] som en datakilde i Flow
1. Gå til [flow.microsoft.com](https://flow.microsoft.com/en-us/) i din webbrowser, og log på.
2. Vælg **Mine Flows** på båndet øverst på siden.
3. I vinduet **Mine Flows** skal du vælge indstillingen **Opret fra tom**.
4. På listen over tilgængelige udløsere skal du vælge en af to [!INCLUDE[d365fin](includes/d365fin_md.md)] tilgængelige udløsere: *Når der oprettes en post* eller *Når en post er blevet ændret*.
5. Flow viser en forbindelsesside, hvor du bliver bedt om de oplysninger, der kræves for at oprette forbindelse til dine [!INCLUDE[d365fin](includes/d365fin_md.md)]-data. Hvis du vil oprette forbindelse, skal du angive et navn til forbindelsen, en OData URL-adresse, brugernavn, adgangskode og firmanavn.

   For *OData URL-adressen* kan du kopiere OData V4 URL-adressen på en af de webtjenester, der er angivet på siden **Webtjeneste** i [!INCLUDE[d365fin](includes/d365fin_md.md)], f.eks. `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   Som *Virksomhedsnavn* skal du bruge det navn, der vises i feltet **Navn** i vinduet **Virksomhedsoplysninger** vindue i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Hvis din [!INCLUDE[d365fin](includes/d365fin_md.md)]-version indeholder flere virksomheder, skal du vælge det relevante virksomhedsnavn på listen i vinduet **Virksomheder**. I begge tilfælde skal du sørge for, at det navn, du angiver i guiden PowerApps, er nøjagtigt det samme som den tekst, der vises i [!INCLUDE[d365fin](includes/d365fin_md.md)], f.eks. `My Company`.

   Som brugernavn og adgangskode skal du bruge navnet og webserviceadgangsnøglen, der er angivet for din konto i vinduet **Brugere** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dit brugernavn er f.eks. *Administrator*, og den webtjenesteadgangsnøgle, der fungerer som din adgangskode, er *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU =*. Du kan finde flere oplysninger i [Fremgangsmåde: Administrere brugere og rettigheder](ui-how-users-permissions.md).
6. Vælg knappen **Opret** nederst på siden for at fortsætte.

   Flow viser en liste over tabeller, der er tilgængelige fra [!INCLUDE[d365fin](includes/d365fin_md.md)]. Disse tabeller, eller slutpunkter, repræsenterer de webtjenester, som du har publiceret fra [!INCLUDE[d365fin](includes/d365fin_md.md)].

   Du kan også vælge at oprette en ny URL-adresse for webtjenesten i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved at bruge handlingen **Opret datasæt** på siden **Webtjenester** ved hjælp af guiden Assisteret opsætning for **Konfigurer rapporteringsdata** eller ved at vælge handlingen **Rediger i Excel** på en af listerne.
7. Vælg de data, du vil bruge i Flow.

Nu har du oprettet forbindelse til dine Dynamics 365-data og er klar til at opbygge din arbejdsgang. Du kan finde flere oplysninger i [Flow-dokumentationen](https://flow.microsoft.com/documentation/getting-started/).

## <a name="see-also"></a>Se også
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importere virksomhedsdata fra andre økonomisystemer](upload-data.md)  
[Fremgangsmåde: Administrere brugere og rettigheder](ui-how-users-permissions.md)    
[Opsætning af [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Finans](finance.md)  

