---
title: "Sådan beregnes ordrebekræftelsesdatoer | Microsoft Docs"
description: "Beregning af leveringstid er et værktøj, du kan bruge til at beregne den tidligst mulige dato, en vare er disponibel til afsendelse eller levering. Funktionen opretter også indkøbskladdelinjer for de datoer, du godkender."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: ff83b7e5b61cd265bb3cb1af0bd5db3513c26072
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-calculate-order-promising-dates"></a>Sådan beregnes ordrebekræftelsesdatoer
En virksomhed skal være i stand til at informere deres kunder om leveringsdatoer for ordren. Med vinduet **Beregning af lev.tid - linjer** kan du gøre dette fra en salgsordrelinje.  

Baseret på en vares kendte og forventede rådighedsdatoer vil [!INCLUDE[d365fin](includes/d365fin_md.md)] øjeblikkeligt beregne leverance- og leveringsdatoer, som derefter kan stilles i udsigt for debitor.  

Hvis der står en ønsket leveringsdato på en salgsordrelinje, bruges denne dato som udgangspunkt for følgende beregninger:  

- ønsket leveringsdato– transporttid = planlagt afsendelsesdato  
- planlagt afsendelsesdato – udgående lagerekspeditionstid = planlagt afsendelsesdato  

Hvis varen er disponibel til pluk på afsendelsesdatoen, kan salgsprocessen fortsættes. Hvis varen ikke er disponibel til pluk på afsendelsesdatoen, vises en advarsel om, at varen ikke er på lager.  

Hvis du ikke angiver en ønsket leveringsdato på en salgsordrelinje, eller hvis ikke den ønskede leveringsdato kan imødekommes, vil den tidligste dato for varernes tilgængelighed blive beregnet. Datoen kan derefter indtastes i feltet **Afsendelsesdato** på linjen, og den dato, som du planlægger at levere varer samt den dato, hvor de leveres til debitor beregnes ved hjælp af følgende beregninger:  

- afsendelsesdato + udgående lagerekspeditionstid = planlagt afsendelses dato  
- planlagt afsendelsesdato + transporttid = planlagt leveringsdato  

## <a name="about-order-promising"></a>Om beregning af leveringstid
Vha. funktionen Beregning af leveringstid kan du oprette en ordrebekræftelse med en bestemt afsendelses- eller leveringsdato. Den dato, hvor en vare er disponibel til levering eller den første mulige afsendelsesdato for en vare og opretter ordrelinjer for de datoer, som du godkender. Funktionen beregner den tidligst mulige dato, en vare er disponibel til afsendelse eller levering. Funktionen opretter også rekvisitionslinjer, hvis varerne først skal købes, for de datoer, du godkender.

[!INCLUDE[d365fin](includes/d365fin_md.md)] bruger to grundlæggende begreber:  

- Disp.-til-levering  
- Første m. afs.dato  

### <a name="available-to-promise"></a>Disp.-til-levering  
Disp.-til-levering (ATP) beregner datoer baseret på reservationssystemet. Der udføres en tilgængelighedskontrol af de ikke-reserverede mængder på lageret med henblik på planlagt produktion, indkøb, overførsler og salgsreturvarer. Baseret på disse oplysninger beregner [!INCLUDE[d365fin](includes/d365fin_md.md)] automatisk leveringsdato for kundens ordre, da varerne er tilgængelige på lageret eller på fastlagte tilgange.  

### <a name="capable-to-promise"></a>Første m. afs.dato  
Første m. afs.dato (CTP) forudsætter et "hvad hvis"-scenarie, hvor varen ikke er på lager, og der ikke planlagt nogen ordrer. Baseret på dette scenarie vil [!INCLUDE[d365fin](includes/d365fin_md.md)] beregne den tidligste dato, varen kan være tilgængelig, hvis den skal produceres, købes eller overføres.  


### <a name="calculations"></a>Beregninger  
Når [!INCLUDE[d365fin](includes/d365fin_md.md)] beregner kundens leveringsdato, udfører den to opgaver:  

- Den beregner den tidligste leveringsdato, når kunden ikke har anmodet om en bestemt leveringsdato.  
- Kontrollerer, om den leveringsdato, som kunden havde ønsket, eller som var blevet lovet kunden, er realistisk.  

Hvis kunden ikke anmoder om en bestemt leveringsdato, bliver afsendelsesdato sat til at være lig med arbejdsdato, og tilgængeligheden er derefter baseret på denne dato. Hvis varen er på lager, beregner [!INCLUDE[d365fin](includes/d365fin_md.md)] fremad i tiden for at bestemme, hvornår ordren kan leveres. Dette opnås ved hjælp af følgende formler:  

- Afsendelsesdato + Udgående lagerekspeditionstid + Planlagt afsendelsesdato + Ekspeditionstid = Dato  
- Planlagt afsendelsesdato + Transporttid = Planlagt leveringsdato  

[!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerer derefter, om den beregnede leveringsdato er realistisk ved at regne bagud i tid og afgøre, hvornår varen skal være tilgængelig for at kunne opfylde den lovede dato. Dette opnås ved hjælp af følgende formler:  

- Planlagt leveringsdato + Transporttid = Planlagt afsendelsesdato  
- Planlagt afsendelsesdato - Udgående lagerekspeditionstid = Afsendelsesdato  

Afsendelsesdatoen bruges til udførelse af tilgængelighedskontrollen. Hvis varen er tilgængelig på denne dato, vil [!INCLUDE[d365fin](includes/d365fin_md.md)] bekræfte, at den ønskede/bekræftede leveringsdato kan overholdes ved at angive den planlagte leveringsdato skal være lig med den ønskede/bekræftede leveringsdato. Hvis varen ikke er tilgængelig, returneres en tom dato og ordrebehandler kan derefter bruge funktionen LE.  

Baseret på nye datoer og klokkeslæt, beregnes alle relaterede datoer ifølge de formler, der er angivet tidligere i dette afsnit. LE-beregningen tager længere tid, men den giver en nøjagtig dato, når kunden kan forvente at have varen leveret. De datoer, som beregnes ud fra CTP, vises i felterne **Planlagt leveringsdato** og **Tidligste afsendelsesdato** i vinduet **Beregning af lev.tid - linjer**.  

Ordrebehandler afslutter LE-processen ved at acceptere datoerne. Det betyder, at en planlægningslinje og en reservationspost oprettes for varen, inden de datoer, der er beregnet til at sikre, at ordren opfyldes.  

Foruden den eksterne beregning af leveringstid, som du kan udføre i vinduet **Beregning af lev.tid - linjer**, kan du også love interne eller eksterne leveringsdatoer for stykliste-elementer. Du kan finde flere oplysninger i [Sådan får du vist tilgængeligheden af varer](inventory-how-availability-overview.md).

## <a name="to-set-up-order-promising"></a>Sådan defineres beregning af leveringstid  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opsætn. af beregn. af lev.tid**, og vælg derefter det relaterede link.  
2. Angiv et nummer og en tidsenhedskode i feltet **Responstid**. Marker én af følgende koder.  

    |Kode|Beskrivelse|  
    |----------|-----------------|  
    |**d**|Kalenderdag|  
    |**a**|Uge|  
    |**m**|Måned|  
    |**q**|Kvartal|  
    |**y**|År|  

    ”3u” angiver f.eks., at responstiden er 3 uger. Brug ”c” som præfiks til koderne for at angive den aktuelle tidsenhed. Hvis responstiden f.eks. skal være den aktuelle måned, skal du angive **cm**.  
3. Angiv en nummerserie i feltet **Nr. for beregn. af lev.tid** ved at vælge en linje fra oversigten i vinduet **Nummerserier**.  
4. Angiv en skabelon til beregning af leveringstid i feltet **Skabl. til beregn. af lev.tid** ved at vælge en linje fra oversigten i vinduet **Indkøbskld.typeover**.  
5. Angiv en indkøbskladdetype i feltet **Kld. til beregn. af lev.tid** ved at vælge en linje i oversigten i vinduet **Indkøbskladdenavne**.

### <a name="to-enter-inbound-warehouse-handling-time-in-the-inventory-setup-window"></a>Sådan indtastes indgående lagerekspeditionstid i vinduet Lageropsætning  
Hvis du vil inkludere lagerekspeditionstiden i beregningen af leveringstiden på købslinjen, kan du angive det som standardindstilling for lageret og for din lokation.    
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opsætning af Lager**, og vælg derefter det relaterede link.  
2. På oversigtspanelet **Generelt**, i feltet **Indgående lagerekspeditionstid**, og angiv det antal dage, du vil inkludere i beregningen af leveringstiden.  

> [!NOTE]  
>  Hvis du har udfyldt feltet **Indgående lagerekspeditionstid** på **Lokationskort** for din lokation, bruges dette felt som standardekspeditionstid for indgående lageraktiviteter.  

### <a name="to-enter-inbound-warehouse-handling-time-on-location-cards"></a>Sådan angives indgående lagerekspeditionstid på lokationskort  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lokation**, og vælg derefter det relaterede link.  
2.  Åbn det relevante lokationskort.  
3.  Gå til oversigtspanelet **Lagersted**, feltet **Indgående lagerekspeditionstid**, og angiv det antal dage, du vil inkludere i beregningen af leveringstiden.  

> [!NOTE]  
>  Hvis du lader feltet **Indgående lagerekspeditionstid** stå tomt, bruger beregningen værdien i vinduet **Lageropsætning**.

### <a name="to-enter-outbound-warehouse-handling-time-in-the-inventory-setup-window"></a>Sådan indtastes udgående lagerekspeditionstid under Lageropsætning  
Hvis du vil have, at beregningen af leveringstiden på salgslinjen skal indeholde en udgående lagerekspeditionstid, kan du angive dette som en standardindstilling for lageret.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opsætning af Lager**, og vælg derefter det relaterede link.  
2. Gå til oversigtspanelet **Generel**, feltet **Udgående lagerekspeditionstid**, og angiv det antal dage, du vil inkludere i beregningen af leveringstiden.  

> [!NOTE]  
>  Hvis du har udfyldt feltet **Udgående lagerekspeditionstid** på Lokationskortet for din lokation, indsættes automatisk indholdet af dette felt som standardekspeditionstid for udgående lageraktiviteter.  

### <a name="to-enter-outbound-warehouse-handling-time-on-location-cards"></a>Sådan angives udgående Lagerekspeditionstid på lokationskort  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lokationer**, og vælg derefter det relaterede link.  
2.  Åbn det relevante lokationskort.  
3.  Gå til oversigtspanelet **Lagersted**, feltet **Udgående lagerekspeditionstid**, og angiv det antal dage, du vil inkludere i beregningen af leveringstiden.  

> [!NOTE]  
>  Hvis du lader feltet **Udgående lagerekspeditionstid** stå tomt, så bruger beregningen værdien i vinduet **Lageropsætning**.

## <a name="to-make-an-item-critical"></a>Sådan gør du en vare kritisk  
Før en vare kan indgå i beregningen af ordrebekræftelsen, skal den markeres som kritisk. Denne opsætning sikrer, at ikke-kritiske varer ikke medfører irrelevante beregnede leveringstider.   
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varer**, og vælg derefter det relaterede link.  
2.  Åbn det relevante varekort.  
3.  Vælg feltet **Kritisk** i oversigtspanel **Planlægning**.  

## <a name="to-calculate-an-order-promising-date"></a>Sådan beregnes en ordrebekræftelsesdato  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsordre**, og vælg derefter det relaterede link.  
2.  Åbn den relevante salgsordre, og vælg de salgsordrelinjer, du vil have programmet til at beregne.  
3.  Vælg handlingen **Beregning af leveringstid**, og vælg derefter handlingen **Beregning af lev.tid - linjer**.  
4.  Vælg en linje, og vælg derefter en af følgende indstillinger:  

    - Marker **Disp.-til-bekræftelse**, hvis du vil beregne den tidligste dato, en vare er disponibel med hensyntagen til lager, fastlagt tilgang og bruttobehov.  
    - Marker **Første m. afs.dato**, hvis du ved, at varen er udgået af lageret og du vil beregne den tidligste dato, varen kan være disponibel ved at afsende en genbestillingsordre.  
5.  Vælg knappen **Accepter** for at godkende den tidligst tilgængelige afsendelsesdato.  

## <a name="see-also"></a>Se også  
[Salg](sales-manage-sales.md)  
[Beregning af forfaldsdato for køb](purchasing-date-calculation-for-purchases.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

