---
title: Oprette et sagskort for en sag og angive opgaver | Microsoft Docs
description: "Du kan oprette et sagskort, der viser sagsopgaver og planlægningslinjer, så det er nemmere at administrere status og budgetter for et nyt projekt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, task
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 50ea98d45875fa418d12c5ba378f26208d739126
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-jobs"></a>Fremgangsmåde: Oprette sager
Når du starter et nyt projekt, skal du oprette et sagskort med integrerede sagsopgaver og sagsplanlægningslinjer, opdelt i to niveauer.  

Det første niveau består af sagsopgaver. Da al bogføring henviser til en sagsopgave, skal du oprette mindst én sagsopgave pr. sag. Når sagen indeholder mindst én sagsopgave, kan du oprette sagsplanlægningslinjer og bogføre forbruget i sagen.

Det andet lag består af sagsplanlægningslinjer, der angiver den detaljerede brug af ressourcer, varer og diverse regnskabsmæssige udgifter.

Den lagdelte struktur giver dig mulighed for at opdele sagen i mindre opgaver og dermed angive mere detaljerede oplysninger i budgetter, rekvisitioner og registreringer. Desuden får du indsigt i, hvordan en sag skrider frem. Du kan f.eks. spore, om du opfylder udpegede milepæl, eller om du overholder tidsplanen for opfyldelse af forventninger til budgettet.

> [!NOTE]  
>   Handlingen **Ny sag** i **Projektleder**-rollecenteret starter en assisteret opsætning, som vejleder dig gennem trinnene til oprettelse af integrerede opgaver og planlægningslinjer. Følgende fremgangsmåde beskriver, hvordan trinnene udføres manuelt.

> [!NOTE]  
>   Denne funktion kræver, at oplevelsen er indstillet til **Suite**. Du kan finde flere oplysninger under [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md).

## <a name="to-create-a-job-card"></a>Sådan oprettes et sagskort
Du kan oprette et sagskort og derefter oprette sagsopgavelinjer og sagsplanlægningslinjer for det.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Sager**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**, og udfyld derefter felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. For at angive sagen med oplysninger om andre sager skal du vælge handlingen **Kopier sag**, udfylde felterne efter behov, og derefter vælge knappen **OK**.

> [!NOTE]  
>   Hvis du bruger timesedler i din sag, skal du også tildele en ansvarlig person. Denne person kan godkende timesedler for medarbejderopgaver, der er knyttet til sagen. Du kan finde flere oplysninger i [Fremgangsmåde: Angive timesedler](projects-how-setup-time-sheets.md).

## <a name="to-create-tasks-for-a-job"></a>Sådan oprettes opgaver for en sag
Når du opretter en sag, skal du også angive de forskellige opgaver, som sagen indeholder. Det gør du ved at tilføje nye linjer i oversigtspanelet **Opgaver** i vinduet **Jobkort**, en opgave pr. linje. Hver sag skal have mindst én opgave.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Sager**, og vælg derefter det relaterede link.
2. Åbn sagskortet for den relevante sag.
3. På oversigtspanelet **Opgaver** skal du udfylde felterne efter behov på en ny linje.
4. For at indrykke opgaver og oprette et hierarki, skal du vælge handlingen **Opgaver** og derefter vælge handlingen **Indryk sagsopgaver**.
5. Gentag trin 3 og 4 for alle de opgaver, du skal bruge for sagen.
6. For at angive sagsopgaverne med oplysninger om andre sagsopgaver skal du vælge handlingen **Kopier sagsopgaver fra**, udfylde felterne efter behov, og derefter vælge knappen **OK**.

## <a name="to-create-planning-lines-for-a-job"></a>Sådan oprettes planlægningslinjer for en sag
Du kan begrænse dine nye sagsopgaver på sagsplanlægningslinjer. En planlægningslinje kan bruges til at hente alle oplysninger, du vil spore for en sag. Du kan bruge planlægningslinjer til at tilføje oplysninger, f.eks. hvilke ressourcer der kræves, eller til at hente de varer, der er brug for til at udføre sagen. Hvis du f.eks. har til opgave at få kundens godkendelse af en sag, kan du knytte den pågældende opgave til planlægningslinjer for varer, f.eks. et møde med kunden og tildelelse af en ressource.  

En sagsplanlægningslinje han være en af følgende typer.  

| Enhedstype | Beskrivelse |
| --- | --- |
| **Budget** |Viser forventet forbrug og omkostninger i forbindelse med sagen, typisk i et projekt af typen tidspunkt og materialer. Planlægningslinjer af denne type kan ikke faktureres. |
| **Fakturerbar** |Viser forventet fakturering til kunden, typisk i et fast pris-projekt. |
| **Både budget og fakturerbar** |Viser budgetteret forbrug, der er lig med, hvad du vil fakturere. |

**Bemærk**! Når du angiver oplysninger på sagsplanlægningslinjer, udfyldes omkostningsoplysninger automatisk. Omkostning, pris og rabat for ressourcer og varer er f.eks. først baseret på de oplysninger, der er defineret på ressource- og varekort.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Sager**, og vælg derefter det relaterede link.
2. Åbn et relevant sagskort.
3. Vælg en sagsopgave, hvor feltet **Sagsopgavetype** indeholder **Bogføring**, og vælg derefter handlingen **Sagsplanlægningslinjer**.  
4. I vinduet **Sagsplanlægningslinjer** skal du udfylde felterne på en ny linje efter behov.
5. Gentag trin 3 og 4 for alle planlægninglinjer, du skal bruge for sagsopgaven.

## <a name="see-also"></a>Se også
[Projektstyring](projects-manage-projects.md)  
[Finans](finance.md)  
[Køb](purchasing-manage-purchasing.md)         
[Salg](sales-manage-sales.md)      
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

