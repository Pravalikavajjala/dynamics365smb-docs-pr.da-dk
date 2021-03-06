---
title: "Sådan omplanlægges eller fornys produktionsordrer direkte | Microsoft Docs"
description: Produktionsordrelinjer indeholder de varer, der skal produceres i produktionsordren.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 147163d0b75853914e5b4bd3417c3525d29caefc
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-replan-or-refresh-production-orders-directly"></a>Fremgangsmåde: Omplanlægge eller forny produktionsordrer direkte
Funktionen **Docs** på produktionsordrer bruges normalt, når du har tilføjet eller ændret komponenter, der opretter underliggende produktionsordrer. Funktionen beregner ændringer, der er foretaget i komponenter og rutelinjer, og omfatter varer på lavere produktionsstyklisteniveauer, som der muligvis oprettes nye produktionsordrer for.  

Ud fra de ændringer, du foretager i komponenterne og rutelinjerne, udfører funktionen Omplanlæg beregninger og planlægning med henblik på alle nye behov for produktionsordren.  

Funktionen **Opdater** på produktionsordrer bruges typisk, når du har gjort ét af følgende:

- Oprettet et produktionsordrehoved manuelt til beregning og oprette af linjedata første gang.
- Foretaget ændringer i produktionsordrehovedet for at genberegne alle linjedata.

Funktionen Opdater beregner ændringer, der er foretaget i et produktionsordrehoved, og omfatter ikke produktionsstyklisteniveauer. Funktionen Forny beregner og initialiserer værdierne for komponentlinjer og rutelinjer baseret på de stamdata, som er defineret i den tilknyttede produktionsstykliste og rute og i overensstemmelse med ordreantallet og forfaldsdatoen i produktionsordrehovedet.

Du kan indsætte produktionsordrelinjerne manuelt eller bruge funktionen, der kalkulerer produktionsordrelinjer fra hovedet.  

> [!NOTE]
 Hvis du bruger funktionen Opdater til at genberegne produktionsordrelinjer, sletter programmet de gamle produktionsordrelinjer og beregner nye produktionsordrelinjer.  

## <a name="to-replan-a-production-order"></a>Sådan omplanlægges en produktionsordre  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ordreplanlægning**, og vælg derefter det relaterede link.  
2.  Åbn den produktionsordre, du vil omplanlægge.  
3.  På oversigtspanelet **Linjer** skal du vælge handlingen **Linjer** og derefter handlingen **Komponenter**.  
4.  Tilføj en komponent, som er en produktionsvare eller et halvfabrikata.  
5.  Vælg handlingen **Omplanlæg** i produktionsordren.  

    Fortsæt med at definere, hvad der skal omplanlægges og hvordan, i vinduet **Omplanlæg produktionsordre**.  
6.  Vælg én af følgende indstillinger i feltet **Systemindikator**.  

    |Indstilling|Description|  
    |----------------------------------|---------------------------------------|  
    |**Baglæns**|Beregner operationssekvensen baglæns fra den tidligst mulige slutdato, defineret ved forfaldsdatoen og/eller andre planlagte ordrer til den senest mulige startdato. **Bemærk!** Denne standardindstilling er relevant i de fleste situationer.|  
    |**Forlæns**|Beregner operationssekvensen forlæns fra den senest mulige startdato, defineret ved forfaldsdatoen og/eller andre planlagte ordrer til den tidligst mulige slutdato. **Bemærk!** Denne indstilling er kun relevant for fremskyndede ordrer.|  

7.  Vælg, om produktionskravene skal beregnes for produktionsvarer på produktionsstyklisten, i feltet **Planlæg** på følgende måde.  

    |Indstilling|Description|  
    |----------------------------------|---------------------------------------|  
    |**Ingen niveauer**|Medtag ikke produktion på lavere niveau. Denne indstilling opdaterer kun varens plan, på samme måde som Forny.|  
    |**Ét niveau**|Planlæg for produktionsbehov på 1. niveau. Der oprettes muligvis produktionsordrer på første niveau.|  
    |**Alle niveauer**|Planlæg for produktionsbehov på alle niveauer. Der oprettes muligvis produktionsordrer på alle niveauer.|  

8.  Vælg **Et niveau**, og klik på **OK**, hvis du vil omplanlægge produktionsordren og beregne og oprette en ny underliggende produktionsordre for det nye halvfabrikata, hvis det ikke er fuldt tilgængeligt.  

> [!NOTE]  
>  Ændringer, der implementeres med funktionen **Omplanlægning** vil sandsynligvis ændre produktionsordrens kapacitetsbehov, hvorfor du muligvis skal ændre planlægning for operationerne bagefter.  

## <a name="to-refresh-a-production-order"></a>Sådan fornys en produktionsordre  
Hvis du har ændret produktionsordrelinjer, komponenter eller rutelinjer, skal du også opdatere oplysningerne i produktionsordren. I det følgende beregnes komponenterne for en fastlagt produktionsordre. Trinnene er de samme for rutelinjer.

1.  Vælg ikonet ![Søg efter side eller en rapport](media/ui-search/search_small.png "Søg efter side eller en rapport ikonet"), angiv **Fastlagt produktionsordre**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**. Du kan finde flere oplysninger i [Fremgangsmåde: Oprette produktionsordrer](production-how-to-create-production-orders.md).  
3.  Vælg handlingen **Opdater**.
4. Vælg en af følgende muligheder i vinduet **Opdater produktionsordre**:

    |Indstilling|Description|  
    |----------------------------------|---------------|---------------------------------------|  
    |**Planlægningsretning**|**Forlæns**|Planlægning begynder ved startdatoen og beregnes fremad til slutdatoen. Du skal angive startdatoen, hvis du vil bruge denne indstilling.|  
    ||**Baglæns**|Planlægning slutter ved startdatoen og beregnes bagud til startdatoen.|  
    |**Beregn**|**Linjer**|Markér dette felt for at beregne produktionsordrelinjerne.|  
    ||**Rute**|Dette felt har ingen indflydelse på beregning af produktionsordrelinjerne.|  
    ||**Komponentbehov**|Dette felt har ingen indflydelse på beregning af produktionsordrelinjerne.|  
    |**Lageragersted**|**Opret indgående anmodning**|Dette felt har ingen indflydelse på beregning af produktionsordrelinjerne.|  

5. Vælg knappen **OK** for at bekræfte dit valg. Nu beregnes produktionsordrelinjerne.

> [!NOTE]  
>  Når du beregner produktionsordrekomponenter, slettes tidligere ændringer i komponenterne.

## <a name="see-also"></a>Se også  
[Skabelon](production-planning.md)  
[Konfigurere produktion](production-configure-production-processes.md)  
[Produktion](production-manage-manufacturing.md)    
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)   
[Konfigurere bedste fremgangsmåder: Forsyningsplanlægning](setup-best-practices-supply-planning.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

