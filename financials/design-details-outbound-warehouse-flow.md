---
title: "Designoplysninger – Udgående lagerflow | Microsoft Docs"
description: "Det udgående flow fra lageret begynder med en anmodning fra frigivne kildedokumenter om at bringe varerne ud af lagerlokationen, enten for at blive leveret til en ekstern part eller et andet sted i virksomheden. Fra lagerområdet udføres lageraktiviteterne på forskellige kompleksitetsniveauer for at bringe varerne ud til afsendelsesområderne."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 54489c23a34e409ccb22faff77da41acdaf065b3
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-outbound-warehouse-flow"></a>Designoplysninger: Udgående lagerflow
Det udgående flow fra lageret begynder med en anmodning fra frigivne kildedokumenter om at bringe varerne ud af lagerlokationen, enten for at blive leveret til en ekstern part eller et andet sted i virksomheden. Fra lagerområdet udføres lageraktiviteterne på forskellige kompleksitetsniveauer for at bringe varerne ud til afsendelsesområderne.  

 Hvert element identificeres og afstemmes med et tilsvarende indgående kildedokument. Der findes følgende udgående kildedokumenter:  

- Salgsordre  
- Udgående overflytningsordre  
- Købsreturvareordre  
- Serviceordre  

Desuden findes følgende interne kildedokumenter, der fungerer ligesom udgående kilder:  

- Produktionsordre med komponentbehov  
- Montageordre med komponentbehov  

 De sidste to dokumenter udgør udgående strømme fra lageret til interne operationsområder. Du kan finde flere oplysninger om lagerekspedition for interne indgående og udgående processer i [Designoplysninger: Internt lagerflow](design-details-internal-warehouse-flows.md).  

 Processer og brugergrænsefladedokumenter i udgående lagerstrømme er forskellige for grundlæggende og avancerede lageropsætninger. Den væsentligste forskel er, at aktiviteter udføres ordre for ordre i grundlæggende lageropsætninger, og de er fælles for flere ordrer i avancerede lageropsætninger. Du kan finde flere oplysninger om forskellige lagerkompleksitetsniveauer i [Designoplysninger: Oversigt over logistik](design-details-warehouse-setup.md)  

 I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan de udgående processer for pluk og levering udføres på fire måder ved hjælp af forskellige funktioner, afhængigt af kompleksitetsniveauet på lageret.  

|Metode|Indgående proces|Placering|Pluk|Leverancer|Kompleksitetsniveau (Se [Designoplysninger: Opsætning af lager](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|-----------|---------------|--------------------------------------------------------------------------------------------------------------------|  
|T|Bogfør pluk og leverance fra ordrelinjen|X|||2|  
|B|Bogfør pluk og leverance fra et lagerplukdokument||X||3|  
|L|Bogfør pluk og leverance fra et lagerleverancedokument|||X|5-4-6|  
|D|Bogfør pluk fra et lagerplukdokument, og bogfør leverance fra et lagerleverancedokument||X|X|5-4-6|  

 Du kan finde flere oplysninger i [Designoplysninger: Udgående lagerflow]()  

 Valg af metode afhænger af virksomhedens accepterede praksis og graden af organisationens kompleksitet. I et ordre for ordre-miljø med enkle processer og simpel placeringsstruktur, metode A, er pluk og levering fra ordrelinjen passende. I andre ordre for ordre-virksomheder, hvor varerne for én ordrelinje kan komme fra mere end én placering, eller hvor lagermedarbejderne ikke kan arbejde med ordredokumenterne, er brugen af separate plukdokumenter relevant, metode B. Hvor en virksomheds pluk- og leveringsprocesser omfatter håndtering af flere ordrer og derfor kræver mere styring og overblik, kan virksomheden vælge at bruge et lagerleverancedokument og lagerplukdokument til at adskille pluk- og leveringsopgaver, metode C og D.  

 Handlinger af pluk og levering kombineres i metoderne A, B og C i ét trin, hvor det tilsvarende dokumentet bogføres som leveret. Plukket er registreret første gang i metode D, og derefter bogføres leverancen på et senere tidspunkt fra et andet dokument.  

## <a name="basic-warehouse-configurations"></a>Grundlæggende lageropsætninger  
 I følgende diagram illustreres de udgående lagerstrømme af dokumenttype i grundlæggende lageropsætninger. Tallene i diagrammet svarer til trinnene i afsnittene efter diagrammet.  

 ![Udgående flow i grundlæggende lageropsætninger](media/design_details_warehouse_management_outbound_basic_flow.png "design_details_warehouse_management_outbound_basic_flow")  

### <a name="1-release-source-document--create-inventory-pick-or-movement"></a>1: Frigiv kildedokument / Opret pluk (lager) eller flytning (lager)  
 Når en bruger, der er ansvarlig for kildedokumenter, f.eks. en salgsordrebehandler eller produktionsplanlægger, er klar til den udgående lageraktivitet, frigiver han eller hun kildedokumentet for at signalere til lagermedarbejdere, at solgte varer eller komponenter kan plukkes og placeres på de angivne placeringer. Alternativt opretter brugeren lagerpluk- eller bevægelsesdokumenter for de enkelte ordrelinjer på en push-måde, baseret på angivne placeringer og mængder, der skal håndteres.  

> [!NOTE]  
>  Flytninger (lager) bruges til at flytte varer til interne operationsområder i grundlæggende lageropsætninger baseret på kildedokumenter eller en ad hoc-basis.  

### <a name="2-create-outbound-request"></a>2: Opret udgående anmodning  
 Når det udgående kildedokument frigives, oprettes der automatisk en udgående lageranmodning. Den indeholder referencer til kildebilagstype og -nummer og er ikke synlig for brugeren.  

### <a name="3-create-inventory-pick-or-movement"></a>3: Opret pluk (lager) eller flytning (lager)  
 I vinduet **Pluk (lager)** eller **Flytning (lager)** modtager lagermedarbejderen på en pull-måde ventende kildedokumentlinjer, der er baseret på udgående lageranmodninger. Alternativt er pluklinjerne for lageret allerede oprettet på en push-måde af den bruger, der er ansvarlig for kildedokumentet.  

### <a name="4-post-inventory-pick-or-register-inventory-movement"></a>4: Bogfør pluk (lager), eller registrer flytning (lager)  
 På hver linje for varer, der er plukket eller flyttet helt eller delvist, udfylder lagermedarbejderen feltet **Antal** og bogfører derefter lagerplukningen eller registrerer flytning (lager). Kildedokumenter, der er knyttet til lagerplukningen, bogføres som leveret eller forbrugt. Kildedokumenter, der er relateret til lagerflytning, bogføres ikke.  

 Ved lagerpluk oprettes der negative vareposter, lagerposter oprettes, og plukanmodningen slettes, hvis fuldt håndteret. Feltet **Leveret (antal)** opdateres f.eks. på den udgående kildedokumentlinje. Der oprettes f.eks. et bogført leverancedokument, der afspejler salgsordren og de leverede varer.  

## <a name="advanced-warehouse-configurations"></a>Avancerede lageropsætninger  
 I følgende diagram illustreres den udgående lagerstrøm af dokumenttype i avancerede lageropsætninger. Tallene i diagrammet svarer til trinnene i afsnittene efter diagrammet.  

 ![Udgående flow i avancerede lageropsætninger](media/design_details_warehouse_management_outbound_advanced_flow.png "design_details_warehouse_management_outbound_advanced_flow")  

### <a name="1-release-source-document"></a>1: Frigiv kildedokument  
 Når en bruger, der er ansvarlig for kildedokumenter, f.eks. en salgsordrebehandler eller produktionsplanlægger, er klar til den udgående lageraktivitet, frigiver han eller hun kildedokumentet for at signalere til lagermedarbejdere, at solgte varer eller komponenter kan plukkes og placeres på de angivne placeringer.  

### <a name="2-create-outbound-request"></a>2: Opret udgående anmodning  
 Når det indgående kildedokument frigives, oprettes der automatisk en udgående lageranmodning. Den indeholder referencer til kildebilagstype og -nummer og er ikke synlig for brugeren.  

### <a name="3-create-warehouse-shipment"></a>3: Opret lagerleverance  
 I vinduet **Lagerleverance** modtager den ansvarlige speditionsmedarbejder ventende kildedokumentlinjer, der er baseret på den udgående lageranmodning. Flere kildedokumentlinjer kan kombineres i et lagerleverancedokument.  

### <a name="4-release-shipment--create-warehouse-pick"></a>4: Frigiv leverance / Opret pluk (logistik)  
 Den speditionsmedarbejder, der er ansvarlig, frigiver lagerleverancen, så lagermedarbejderne kan oprette eller koordinere lagerpluk for den pågældende leverance.  

 Alternativt kan brugeren oprette lagerplukdokumenter for de enkelte leverancelinjer på en push-måde, baseret på angivne placeringer og antal der skal håndteres.  

### <a name="5-release-internal-operation--create-warehouse-pick"></a>5: Frigiv intern handling / Opret pluk (logistik)  
 Den bruger, der er ansvarlig for interne operationer, frigiver et internt kildedokument, f.eks. en produktions- og montageordre, så lagermedarbejdere kan oprette eller koordinere lagerpluk for den pågældende interne operation.  

 Alternativt kan brugeren oprette lagerplukdokumenter for den enkelte produktion eller montageordre på en push-måde, baseret på angivne placeringer og antal der skal håndteres.  

### <a name="6-create-pick-request"></a>6: Opret plukanmodning  
 Når det udgående kildedokument frigives, oprettes der automatisk en lagerplukanmodning. Den indeholder referencer til kildebilagstype og -nummer og er ikke synlig for brugeren. Afhængigt af opsætningen, opretter forbrug fra en produktions- og montageordre også en plukanmodning om at plukke de nødvendige komponenter fra lageret.  

### <a name="7-generate-pick-worksheet-lines"></a>7: Generér plukkladdelinjer  
 Den bruger, der er ansvarlig for at koordinere pluk, henter pluklinjer i **Plukkladden** baseret på plukanmodninger fra lagerleverancer eller interne aktiviteter med komponentforbrug. Brugeren vælger de linjer, der skal plukkes, og forbereder plukkene ved at angive, hvilke placeringer der skal tages fra, hvilke placeringer der skal placeres i, og hvor mange enheder der skal håndteres. Placeringerne kan være foruddefineret ved opsætning af lagerlokationen eller operationsressourcen.  

 Brugeren angiver plukmetoder for optimeret lagerekspedition og bruger derefter en funktion til at oprette de tilsvarende pluk-dokumenter, der er tildelt til forskellige lagermedarbejdere, der udfører lagerpluk. Når lagerpluk er fuldt tildelt, slettes linjerne i **Plukkladde**.  

### <a name="8-create-warehouse-pick-documents"></a>8: Opret lagerplukdokumenter  
 Den lagermedarbejder, der udfører pluk, opretter et lagerplukdokument på en pull-måde baseret på det frigivne kildedokument. Alternativt er lagerplukdokumentet oprettet og tildelt lagermedarbejderen på en push-måde.  

### <a name="9-register-warehouse-pick"></a>9: Registrer pluk (lager)  
 På hver linje for varer, der er plukket eller flyttet helt eller delvist, udfylder lagermedarbejderen feltet **Antal** i vinduet **Pluk (logistik)** og registrerer derefter lagerplukningen.  

 Lagerposter oprettes og lagerpluklinjerne slettes, hvis de er fuldt håndteret. Lagerplukdokumentet forbliver åbent, indtil det fulde antal af den relaterede lagerleverance er registreret. Feltet **Plukket antal** på lagerleverancelinjerne opdateres i overensstemmelse hermed.  

### <a name="10-post-warehouse-shipment"></a>10: Bogfør lagerleverance  
 Når alle varer på lagerleverancedokumentet er registreret som plukket til de angivne leveranceplaceringer, bogfører den speditionsmedarbejder, der er ansvarlig, lagerleverancen. Negative vareposter oprettes. Feltet **Leveret (antal)** opdateres f.eks. på den udgående kildedokumentlinje.  

## <a name="see-also"></a>Se også  
 [Designoplysninger: Logistik](design-details-warehouse-management.md)

