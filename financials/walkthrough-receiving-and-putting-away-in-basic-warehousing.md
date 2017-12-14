---
title: "Gennemgang - Modtagelse og placering på lager i grundlæggende lageropsætninger | Microsoft Docs"
description: "I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan de indgående processer for modtagelse og placering på lager udføres på fire måder ved hjælp af forskellige funktioner afhængigt af kompleksitetsniveauet på lageret."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: d985a6c1a28ee20dab73a8627e18eb4805f78b6e
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---
# <a name="walkthrough-receiving-and-putting-away-in-basic-warehouse-configurations"></a>Gennemgang: Modtagelse og placering på lager i grundlæggende lageropsætninger
I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan de indgående processer for modtagelse og placering på lager udføres på fire måder ved hjælp af forskellige funktioner afhængigt af kompleksitetsniveauet på lageret.  

|Metode|Indgående proces|Placering|Modtagelser|Læg-på-lager-aktiviteter|Kompleksitetsniveau (Se [Designoplysninger: Opsætning af lager](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|T|Bogfør lagermodtagelse og læg-på-lager fra ordrelinjen|X|||2|  
|B|Bogfør lagermodtagelse og læg-på-lager fra et læg-på-lager-dokument|||X|3|  
|L|Bogfør lagermodtagelse og læg-på-lager fra et lagermodtagelsesdokument||X||5-4-6|  
|D|Bogfør modtagelse fra et lagermodtagelsesdokument, og bogfør læg-på-lager fra lagerets læg-på-lager-dokument||X|X|5-4-6|  

Du kan finde flere oplysninger i [Designoplysninger: Indgående lagerflow](design-details-inbound-warehouse-flow.md)  

Den følgende gennemgang viser metode B i forrige tabel.  

## <a name="about-this-walkthrough"></a>Om denne gennemgang  
I grundlæggende lageropsætninger, hvor lokationen, du vil plukke fra, er sat op til at kræve læg-på-lager men ikke modtagelse, bruges vinduet **Læg-på-lager** til at registrere og bogføre læg-på-lager- og modtagelsesoplysninger for de indgående kildedokumenterne. Det indgående kildedokument kan være en købsordre, en salgsreturvareordre, en indgående overflytningsordre eller en produktionsordre med afgang, der er klar til at blive lagt på lager.

> [!NOTE]
> Selv om indstillingerne kaldes **Kræv pluk** og **Kræv læg-på-lager**, kan du bogføre modtagelser og leverancer direkte fra kildeforretningsdokumenterne på lokationer, hvor du kan markerer disse afkrydsningsfelter.  

Denne gennemgang viser følgende opgaver.  

-   Indstilling af SØLV-lokation til læg-på-lager-aktiviteter.  
-   Indstilling af SØLV-lokation til placeringshåndtering.  
-   Definition af en standardplacering for varen LS-81. (LS-75 er allerede oprettet i CRONUS).  
-   Oprettelse af en købsordre for kreditor 10000 til 40 højttalere.  
-   Kontrol af, at lagerplaceringerne er forudindstillet af opsætningen.  
-   Frigivelse af købsordren til lagerekspedition.  
-   Oprettelse af en læg-på-lager-aktivitet baseret på et frigivet kildedokumentet.  
-   Kontrol af, at lagerplaceringerne er overført fra købsordren.  
-   Registrering af lagerbevægelsen til lageret og på samme tid bogføring af købsmodtagelsen til kildekøbsordren.  

## <a name="roles"></a>Roller  
Denne gennemgang viser de opgaver, der udføres af følgende brugerroller:  

-   Lagerchef  
-   Indkøbsagent  
-   Lagermedarbejder  

## <a name="prerequisites"></a>Forudsætninger  
For at gennemføre denne gennemgang skal:  

-   CRONUS Danmark A/S være installeret.  
-   Du kan oprette dig selv som en lagermedarbejder på lokationen SØLV ved at følge disse trin:  

    1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lagermedarbejdere**, og vælg derefter det relaterede link.  
    2.  Vælg feltet **Bruger-id**, og vælg din egen brugerkonto i vinduet **Brugere**.  
    3.  Angiv SØLV i feltet **Lokationskode**.  
    4.  Markér feltet **Standard**.  

## <a name="story"></a>Historie  
Ellen, som er indkøbschef hos CRONUS Danmark A/S, opretter en købsordre til 10 enheder af varen LS-75 og 30 enheder af varen LS-81 fra kreditoren 10000 til afsendelse til lagerstedet SØLV. Når leveringen ankommer på lagerstedet, sætter John, som er lagerarbejder, varerne på lager på standardplaceringer, der er defineret for varerne. Når John bogfører placeringen på lager, bogføres varerne som modtaget på lageret og tilgængelige til salg eller andre behov.  

## <a name="setting-up-the-location"></a>Indstilling af lokation  
 Opsætningen af vinduet **Lokationskort** definerer arbejdsgangene i virksomheden.  

### <a name="to-set-up-the-location"></a>Sådan oprettes lokationen  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lokationer**, og vælg derefter det relaterede link.  
2.  Åbn lokationskortet SØLV.  
3.  Markér afkrydsningsfeltet **Kræv læg-på-lager**.  

    Fortsæt ved at oprette en standardplacering for de to varenumre for at kontrollere, hvor de lægges på lager.  

4.  Vælg handlingen **Placeringer**.  
5.  Vælg den første række, til placering S-01-0001, og vælg derefter handlingen **Indhold**.  

    Bemærk i vinduet **Placeringsindhold**, at vare LS-75 allerede er oprettet som indhold på placering S-01-0001.  

6.  Vælg handlingen **Ny**.  
7.  Vælg felterne **Fast** og **Standard**.  
8.  Skriv LS-81 i feltet **Bilagsnr.**.  

## <a name="creating-the-purchase-order"></a>Oprettelse af købsordren  
Købsordrer er den mest almindelige type indgående kildedokument.  

### <a name="to-create-the-purchase-order"></a>Hvis du vil oprette købsordren  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Købsordrer**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**.  
3.  Opret en købsordre for kreditor 10000 på arbejdsdatoen (23. januar) med følgende købsordrelinjer.  

    |Vare|Lokationskode|Placeringskode|Antal|  
    |----------|-------------------|--------------|--------------|  
    |LS_75|SØLV|S-01-0001|10|  
    |LS-81|SØLV|S-01-0001|30|  

    > [!NOTE]  
    >  Placeringskoden angives automatisk i overensstemmelse med opsætningen, som du har foretaget i afsnittet "Indstilling af lokation".  

    Fortsæt ved at meddele lageret, at købsordren er klar til lagerekspedition, når leverancen ankommer.  

4.  Vælg handlingen **Frigivelse**.  

    Leverancen af højttalere fra kreditor 10000 er modtaget på SØLV-lageret, og John fortsætter med at lægge dem på plads.  

## <a name="receiving-and-putting-the-items-away"></a>Modtagelse og placering af varer på lager  
I vinduet **Læg-på-lager** kan du administrere alle indgående lageraktiviteter til et specifikt kildedokument, f.eks. en købsordre.  

### <a name="to-receive-and-put-the-items-away"></a>Sådan modtager du varerne og lægger dem på lager  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Læg-på-lager-akt. (lager)**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**.  
3.  Vælg feltet **Kildedokument**, og vælg derefter **Købsordre**.  
4.  Vælg feltet **Kildenr.**, vælg linjen til købet fra kreditor 10000, og vælg knappen **OK**.  

    Du kan også gå til fanen **Handlinger** i gruppen **Funktioner** og vælge **Hent kildedokument** og derefter vælge købsordren.  

5.  Vælg handlingen **Autofyld håndteringsantal**.  

    Du kan også indtaste henholdsvis 10 og 30 på de to læg-på-lager-linjer i feltet **Håndteringsantal**.  

6.  Vælg handlingen **Bogfør**, vælg handlingen **Modtag**, og vælg derefter knappen **OK**.  

    De 40 højttalere er nu registreret som lagt på lager på placering S-01-0001, og der oprettes en positiv varepost, der afspejler den bogførte købsmodtagelse.  

## <a name="see-also"></a>Se også  
 [Sådan lægges varer på lager med Læg-på-lager](warehouse-how-to-put-items-away-with-inventory-put-aways.md)   
 [Fremgangsmåde: Oprette grundlæggende lagersteder med handlingsområder](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)   
 [Sådan flyttes komponenter til et handlingsområde i grundlæggende lageropsætninger](warehouse-how-to-move-components-to-an-operation-area-in-basic-warehousing.md)   
 [Fremgangsmåde: Plukke til produktion eller montage](warehouse-how-to-pick-for-production.md)   
 [Sådan flyttes varer ad hoc i grundlæggende lageropsætninger](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)   
 [Designoplysninger: Indgående lagerflow](design-details-inbound-warehouse-flow.md)   
 [Gennemgang af forretningsprocesser](walkthrough-business-process-walkthroughs.md)  
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
