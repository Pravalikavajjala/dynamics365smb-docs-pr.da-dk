---
title: Godkende eller afvise dokumenter i workflows | Microsoft Docs
description: "Du kan anmode om, afvise eller uddelegere en godkendelse af f.eks. et købs- eller salgsdokument som en del af et workflow."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 08/24/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 000a27efed9ff6c20cffd470e1d5dda0b9387bb6
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-use-approval-workflows"></a>Fremgangsmåde: Bruge godkendelsesworkflows
Når en post, f.eks et købsdokument eller et debitorkort, skal godkendes af en person i organisationen, sendes en godkendelsesanmodning som en del af en arbejdsgang. Afhængigt af hvordan arbejdsgangen er konfigureret, får den relevante godkender derefter besked om, at posten kræver godkendelse.

Du kan konfigurere godkendelsesworkflows i vinduet **Workflow**. Du kan finde flere oplysninger under [Opsætte workflows](across-set-up-workflows.md).

Ud over godkendelsesworkflows, der er beskrevet i dette emne, kan du udføre forskellige andre opgaver i workflowet. Der er flere oplysninger i [Anvende workflows](across-use-workflows.md).

Grundlæggende godkendelsesworkflows for købsdokumenter, salgsdokumenter, udbetalingskladder, debitorkort og varekort er klar til brug som assisteret opsætning. Du kan finde flere oplysninger under [Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md).

> [!NOTE]  
>   Denne funktion kræver, at oplevelsen er indstillet til **Suite**. Du kan finde flere oplysninger under [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md).

## <a name="to-request-approval-of-a-record"></a>Sådan anmodes om godkendelse af en post
Følgende opgave udføres af en godkendelsesbruger.

1. I det vindue, hvor posten vises, kan du vælge handlingen **Send godkendelsesanmodning**.
2. Hvis du vil se alle dine godkendelsesanmodninger, skal du vælge ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Godkendelsesanmodningsposter** og derefter vælge det relaterede link.  

Godkendelsespostens status opdateres fra **Oprettet** til **Åben**. Postens status, f.eks. en købsfaktura, opdateres fra **Åben** til **Afventer godkendelse** og forbliver låst mod behandling, indtil alle godkendere har godkendt posten.

Når godkenderen har godkendt posten, ændres status til **Frigivet**. Du kan derefter fortsætte dine opgaver med posten.

## <a name="to-cancel-requests-for-approval"></a>Sådan annulleres godkendelsesanmodninger
Følgende opgave udføres af en godkendelsesbruger med godkendelsesrettigheder.

En kunde vil måske ændre en ordre, efter at den er sendt til godkendelse. I så fald kan du annullere godkendelsesprocessen og foretage de nødvendige ændringer i ordren, inden du anmoder om godkendelse igen.

- I det vindue, hvor posten vises, kan du vælge handlingen **Annuller godkendelsesanmodning**.

Når godkendelsesanmodningen er annulleret, ændres statussen for den relaterede godkendelsespost til **Annulleret**. Postens status opdateres fra **Afventer godkendelse** til **Åben**. Godkendelsesprocessen kan derefter starte igen.

## <a name="to-approve-or-reject-requests-for-approval"></a>Sådan godkendes eller afvises anmodninger om godkendelse
Følgende opgave udføres af en godkendelsesbruger med godkendelsesrettigheder.

Du kan behandle godkendelsesanmodninger i vinduet **Anmodninger til godkendelse** for eksempel for at godkende flere anmodninger ad gangen. Alternativt kan du behandle hver anmodning i den relaterede post, f.eks vinduet **Købsfaktura**, ved at klikke på linket i meddelelsen, som du modtager.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Anmodninger til godkendelse**, og vælg derefter det relaterede link.
2. Vælg en eller flere linjer for den eller de poster, du vil godkende eller afvise.
3. Vælg handlingerne **Godkend**, **Afvis** eller **Uddeleger**.

Når en post er blevet godkendt eller afvist, ændres godkendelsesstatussen i feltet **Status** til **Godkendt** eller **Afvist**.

Hvis der er konfigureret et godkenderhierarki, er poststatussen **Afventer godkendelse**, indtil alle godkendere har godkendt posten. Derefter ændres postens status til **Frigivet**.

På samme tid ændres godkendelsespostens status fra **Oprettet** til **Åben**, så snart der oprettes en godkendelsesanmodning for posten. Hvis anmodningen afvises, ændres godkendelsesstatusen til **Afvist**. Statussen forbliver **Åben** eller **Afvist**, indtil alle godkendere har godkendt anmodningen.

## <a name="to-delegate-requests-for-approval"></a>Sådan uddelegeres godkendelsesanmodninger
Følgende opgave udføres af en godkendelsesbruger med godkendelsesrettigheder.

For at forhindre, at dokumenter hober sig op eller på anden måde blokerer arbejdsgangen, kan godkenderen og godkendelsesaministratoren uddelegere en godkendelsesanmodning til en stedfortrædende godkender. Stedfortræderen kan enten være en angivet stedfortræder, den direkte godkender eller godkendelsesadministratoren, i nævnte rækkefølge. Du bruger typisk denne funktion, hvis en godkender ikke til stede og ikke kan godkende anmodninger inden forfaldsdatoen.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Anmodninger til godkendelse**, og vælg derefter det relaterede link.
2. Vælg en eller flere linjer for de godkendelsesanmodninger, som du vil uddelegere til en stedfortrædende godkender, og vælg derefter handlingen **Uddeleger**.

En notifikation til at godkende anmodningen sendes til en anden foruddefineret stedfortrædende godkender.

## <a name="to-manage-overdue-approval-requests"></a>Sådan administreres forfaldne godkendelsesanmodninger
Følgende opgave udføres af en godkendelsesbruger med godkendelsesrettigheder.

Med jævne mellemrum skal du minde brugerne i en godkendelsesarbejdsgang om forfaldne godkendelsesanmodninger, de skal reagere på. Du bruger funktionen **Send notifikationer om forfaldne godkendelser** til dette.

Funktionen **Send notifikationer om forfaldne godkendelser** tjekker for alle åbne anmodninger, der aktuelt er forfaldne. Hver godkender, der har mindst én forfalden godkendelsespost, modtager en notifikation med listen over deres forfaldne godkendelsesanmodninger. Notifikationen sendes også til deres godkender og alle anmodere om de forfaldne godkendelser. Det kan være en hjælp, hvis den forfaldne godkendelsespost skal uddelegeres til en anden godkender.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Forfaldne godkendelsesanmodninger**, og vælg derefter det relaterede link.
2. I vinduet **Forfaldne godkendelsesanmodninger** skal du vælge handlingen **Send notifikationer om forfaldne godkendelser**.

## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)    
[Indgående bilag](across-income-documents.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

