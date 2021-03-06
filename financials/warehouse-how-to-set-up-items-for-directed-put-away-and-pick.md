---
title: "Sådan konfigureres varer og lokationer til styret læg-på-lager og pluk | Microsoft Docs"
description: "Når lagerlokationen kræver styret læg-på-lager og pluk, kan du bruge en ny funktion, der hjælper dig med at styre lagerstedet på den mest effektive måde."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9b41bb902d8a2298f438233ca24c5a7bcf7f69d9
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-items-and-locations-for-directed-put-away-and-pick"></a>Sådan konfigureres varer og lokationer til styret læg-på-lager og pluk
Når lagerlokationen kræver styret læg-på-lager og pluk, kan du bruge en ny funktion, der hjælper dig med at styre lagerstedet på den mest effektive måde. Hvis du vil have fuldt udbytte af denne funktion, skal du give yderligere oplysninger om varerne, som til gengæld hjælper med at foretage de nødvendige beregninger for at kunne give forslag til de mest effektive måder at styre lageraktiviteter på. Du kan finde flere oplysninger i [Designoplysninger: Opsætning af lager](design-details-warehouse-setup.md)

## <a name="to-set-up-an-item-for-directed-put-away-and-pick"></a>Sådan opsættes varer til styret læg-på-lager og pluk  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varer**, og vælg derefter det relaterede link.  
2.  Åbn kortet for den vare, som du vil konfigurere til styret læg-på-lager og pluk.
3. Udfyld felterne i oversigtspanelet **Lagersted** på varekortet for at definere, hvordan varen skal håndteres på lagerstedet.  
4.  Vælg handlingen **Enheder**.
5. I vinduet **Enheder** skal du udfylde felterne for at definere de forskellige enheder, som varen kan håndteres i, herunder højde, bredde, længde, rummål og vægt for enheden.
6. Vælg handlingen **Placeringsindhold**.
7. I vinduet **Placeringsindhold** kan du definere de lokationer og placeringer, som varen skal tilknyttes. Feltet **Standard** bruges ikke, når lokationen kræver styret læg-på-lager og pluk.  

## <a name="to-activate-directed-put-away-and-pick-functionality"></a>Sådan aktiveres funktionaliteten styret læg-på-lager og pluk  
Styret læg-på-lager og pluk giver dig adgang til funktioner for avanceret lageropsætning, der kan medføre en væsentlig forbedring af effektiviteten og dataenes pålidelighed. Hvis du vil bruge disse funktioner, skal du først opsætte en række parametre i lagerlokationen.  

Hvis du vil benytte styret læg-på-lager og pluk, skal du aktivere den tilknyttede funktionalitet på lokationskortet.    
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lokationer**, og vælg derefter det relaterede link.  
2.  Vælg den lokation, hvor du vil bruge styret læg-på-lager og pluk, og vælg derefter handlingen **Rediger**.  
3.  I oversigtspanelet **Lagersted** skal du markere afkrydsningsfeltet **Styret læg-på-lager og pluk**.  

Det er ikke nødvendigt at udfylde andre felter på lokationskortet før senere i opsætningen.  

> [!NOTE]  
>  Du kan ikke sætte lageret op til at bruge placeringer, når lokationen har åbne vareposter.  

Det næste trin er at definere de placeringer, du vil styre. Du kan finde flere oplysninger i [Sådan oprettes placeringstyper](warehouse-how-to-set-up-bin-types.md). Placeringstypen definerer, hvordan en angivet placering skal bruges, når varestrømmen behandles på lagerstedet. Du kan tildele en placeringstype til både en zone og en placering.  

Du kan også definere lagerklassekoder, hvis der håndteres varer med forskellige krav til oplagringsforhold. Lagerklassekoder bruges, når der foreslås vareplaceringer. Du tildeler lagerklassekoder til produktgrupper, der derefter tildeles til varer og lagervarer eller til zoner og placeringer, der kan tilpasses de opbevaringsforhold, som er påkrævet i henhold til lagerklassekoderne.  

Du er nu klar til at opsætte zoner, hvis du vil arbejde med zoner på lagerstedet. Brugen af zoner nedsætter det antal felter, det er nødvendigt at udfylde, når du skal oprette placeringer, fordi de placeringer, der oprettes inden for en zone, automatisk overtager en række egenskaber fra denne. Zoner kan også gøre det nemmere for nye eller midlertidige medarbejdere at finde rundt på lagerstedet. Bemærk, at strømmen styres af placeringer. Det er derfor muligt at styre med placeringer og kun have én zone.  

## <a name="to-set-up-a-zone-in-your-warehouse"></a>Sådan oprettes en zone på lagerstedet  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lokationer**, og vælg derefter det relaterede link.  
2.  Vælg den lokation, hvor du vil oprette zone, åbn lokationskortet, og vælg derefter handlingen **Zoner**.  
3.  I vinduet **Zoner** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

Når du ændrer en zoneparameter, vil alle placeringer i zonen, der oprettes efter dette tidspunkt, få de nye egenskaber, men de oprindelige placeringer ændres ikke.  

> [!NOTE]  
>  Hvis du vil arbejde uden zoner, skal du stadigvæk oprette en zonekode uden definition bortset fra koden.  

Det næste trin i opsætning af lagerstedet omfatter definition af placeringer. Du kan finde flere oplysninger under [Fremgangsmåde: Oprette lokationer til brug af placeringer](warehouse-how-to-set-up-locations-to-use-bins.md).  

Derudover skal du oprette læg-på-lager-skabeloner og optællingsperioder. Du kan finde flere oplysninger i [Sådan oprettes læg-på-lager-skabeloner](warehouse-how-to-set-up-put-away-templates.md).  

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

