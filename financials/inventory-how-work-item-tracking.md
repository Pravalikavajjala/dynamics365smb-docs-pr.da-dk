---
title: "Sådan tildeles serienumre og lotnumre numre til varer til sporing | Microsoft Docs"
description: "Du kan tilføje serienumre og lotnumre til ethvert udgående eller indgående dokument, og dets posterede varesporing vises i de tilknyttede vareposter."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 326c7931cc0217c72ede62d5516dba5f4ee6fa32
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-work-with-serial-and-lot-numbers"></a>Fremgangsmåde: Arbejde med serienumre og lotnumre
Du kan tildele serienumre og lotnumre til ethvert udgående eller indgående dokument, og dets posterede varesporing vises i de tilknyttede vareposter. Du kan udføre arbejdet i vinduet **Varesporingslinjer**.

Matrixen for mængdefelter øverst i vinduet **Varesporingslinjer** viser mængder og summer for de varesporingsnumre, der defineres på linjerne. Mængderne skal svare til mængderne på dokumentlinjen, der er angivet med 0 i felterne **Udefineret**.

Af hensyn til ydeevnen indsamler programmet kun disponeringsoplysninger i vinduet **Varesporingslinjer** én gang, når du åbner vinduet. Det betyder, at programmet ikke opdaterer disponeringsoplysningerne, mens du har vinduet åbent – heller ikke selvom der sker ændringer i lageret eller i andre dokumenter.

Varer med serie- eller lotnumre kan spores både frem og tilbage i deres forsyningskæde. Dette er nyttigt ved generel kvalitetssikring og tilbagekaldelser af produkter. Du kan finde flere oplysninger i [Sådan gør du: Spore varesporede varer](inventory-how-to-trace-item-tracked-items.md).

## <a name="about-picking-serial-or-lot-numbers-in-the-warehouse"></a>Om plukning af serie- eller lotnumre på lagerstedet
Udgående håndtering af serie eller lotnumre er en almindeligt forekommende opgave i mange forskellige lagerprocesser.  

I nogle processer har lagervarerne ikke serie- eller lotnumre, og lagermedarbejderen skal tildele nye under den udgående håndtering, typisk fra en foruddefineret nummerserie.

I enkle processer har lagervarerne allerede serie- eller lotnumre, som f.eks. blev tildelt, da de blev lagt på lager, og disse numre overføres automatisk via alle udgående lageraktiviteter uden interaktion ved lagermedarbejderne.

I visse situationer vedr. lagervare med serie - eller lotnumre defineres bestemte serie- eller lotnumre på kildedokumentet, f.eks. en salgsordre, som lagermedarbejderen skal respektere under den udgående lageradministration. Dette kan skyldes, at debitor har anmodet om et bestemt lot under ordreprocessen. Når lagerplukdokumentet er oprettet fra et udgående kildedokument, hvor der allerede er defineret serie- eller lotnumre, er alle felterne i vinduet **Varesporingslinjer** under lagerpluk skrivebeskyttede, undtagen feltet **Håndteringsantal**. I så fald angiver pluklinjerne for lageret varesporingsnumrene på de enkelte Hent- og Placer-linjer. Antallet er allerede opdelt i entydige serie- eller lotnummerkombinationer, fordi salgsordren angiver de varesporingsnumre, der skal leveres.  

## <a name="item-tracking-availability"></a>Tilgængelighed af varesporing
Når du arbejder med serie- og lotnumre, beregner [!INCLUDE[d365fin](includes/d365fin_md.md)] disponeringsoplysningerne for lot- og serienumre, og oplysningerne vises i de forskellige vinduer til varesporing. På denne måde kan du se, hvor meget af et lot- eller serienummer der i øjeblikket bruges i andre dokumenter. Dette reducerer fejl og usikkerhed, der skyldes dobbelte tildelinger.

I vinduet **Varesporingslinjer** vises et advarselsikon i feltet **Lotnr.disponering** eller feltet **Serienr.disponering**, hvis nogle eller alle af det valgte antal allerede bruges i andre dokumenter, eller hvis lot- eller serienummeret ikke er tilgængeligt.

I vinduerne **Serienr./lotnr. - liste**, **Serienr./lotnr. - disponering** og **Varesporing - vælg poster** vises oplysninger om, hvor mange af en vare der bruges. Dette omfatter følgende oplysninger.

|Felt|Description|
|-----|-----------|  
|**I alt**|Det samlede antal varer på lager|
|**Ønsket antal i alt**|Det samlede antal varer, der ønskes til brug i dette og andre dokumenter|
|**Aktuelt ventende antal**|Det antal varer, der ønskes brugt i det aktuelle dokument, men som endnu ikke er sendt til databasen|
|**Aktuelt bestilt antal**|Det antal varer, der vil blive brugt i det aktuelle dokument|
|**Beholdning i alt**|Det samlede antal varer på lager minus det antal af varen, der ønskes brugt i dette og andre dokumenter (ønsket antal i alt) minus det antal, der ønskes, men som endnu ikke er sendt i dette dokument (aktuelt ventende antal)|

Hvis du arbejder i vinduet **Varesporingslinjer** i lang tid, eller hvis der er stor aktivitet omkring den vare, du arbejder med, kan du vælge handlingen **Opdater disponering**. Varedisponeringen kontrolleres også automatisk, når du lukker vinduet, så det kontrolleres, at der ikke er nogen disponeringsproblemer.

## <a name="to-set-up-item-tracking-codes"></a>Sådan oprettes varesporingskoder
En varesporingskode afspejler de forskellige overvejelser, som en virksomhed skal gøre sig i forbindelse med brugen af serie- og lotnumre på varer, der bevæger sig igennem lageret.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varesporingskoder**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny**.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Klik på oversigtspanelet **Serienr.** og **Lotnr.** for at definere varesporingsmetoder efter henholdsvis serienummer og lotnummer.  

### <a name="to-set-up-expiration-rules-for-serial-or-lot-numbers"></a>Sådan oprettes udløbsregler for serienumre eller lotnumre  
Det kan være praktisk at angive særlige udløbsdatoer og regler i varesporingskoden. Dette gør det muligt at holde styr på, hvornår bestemte serie- og lotnumre udløber.

1. Vælg en eksisterende varesporingskode, og vælg derefter handlingen **Rediger**.  
2.  Markér følgende afkrydsningsfelter i oversigtspanelet **Diverse**.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**Nøje bogføring af udløbsdato**|Angiver, at den udløbsdato, der blev knyttet til varesporingsnummeret ved modtagelse på lageret, skal overholdes, når varen forlader lageret.|  
    |**Man. angivelse af udløbsdato**|Angiver, at du skal angive en udløbsdato manuelt på varesporingslinjen.|  

### <a name="to-set-up-warranties-for-serial-or-lot-numbers"></a>Sådan oprettes garantier for serie- eller lotnumre  
Det kan være praktisk at angive særlige garantier for bestemte varer i varesporingskoden. Det betyder, at du kan holde styr på, hvornår garantierne for bestemte serie- eller lotnumre udløber for varerne på dit lager.        
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varesporingskoder**, og vælg derefter det relaterede link.  

1. Vælg en eksisterende varesporingskode, og vælg derefter handlingen **Rediger**.  
2.  Udfyld feltet **Garantiophørsformel** i oversigtspanelet **Diverse**, og marker derefter afkrydsningsfeltet på følgende måde.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**Garantiophørsformel**|Angiver den sidste dag for garantien på varen.|  
    |**Man. angivelse af garantiophør**|Angiver, at du manuelt skal angive en garantidato på varesporingslinjen.|  

## <a name="to-record-serial-or-lot-number-information"></a>Sådan registreres oplysninger om serie- eller lotnumre  
Hvis du vil knytte specielle oplysninger til et bestemt varesporingsnummer, f.eks. for kvalitetssikring, kan du gøre dette på serie- eller lotnr.oplysningskortet.

1. Åbn et dokument, der har tildelte serie- eller lotnumre.
2. Åbn vinduet **Varesporingslinjer** for dokumentet.
3. Vælg f.eks. handlingen **Serienr.oplysningskort**.  

    Felterne **Serienr.** og **Lotnr.** er udfyldt på forhånd fra varesporingslinjen.  
4. Angiv korte oplysninger i feltet **Beskrivelse**, for eksempel om varens tilstand.  
5. Vælg handlingen **Kommentar** for at oprette en separat kommentar.  
6. Markér afkrydsningsfeltet **Spærret** for at udelade serienummeret eller lotnummeret i alle transaktioner.  

## <a name="to-modify-existing-serial-or-lot-number-information"></a>Sådan ændres eksisterende serie-/lotnummeroplysninger  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varer**, og vælg derefter det relaterede link.  
2. Vælg en vare, der har en varesporingskode og har serie- eller lotnummeroplysninger.
3. I vinduet **Varekort** skal du vælge handlingen **Poster** og derefter klikke på **Poster**.
4. Vælg feltet **Lotnr.** eller **Serienr.**. Hvis der findes oplysninger for varesporingsnummeret, åbnes vinduet **Oversigt over lotnr.oplysninger** eller **Oversigt over serienr.oplysninger**.  
5. Vælg et kort, og vælg derefter handlingen **Lotnr.oplysningskort/Serienr.oplysningskort**.  
6. Rediger den korte beskrivelsestekst, kommentarposten eller feltet **Spærret**.  

Du kan ikke redigere serienumre, lotnumre eller mængder. For at gøre det skal du ompostere den pågældende varepost. Du kan finde flere oplysninger i afsnittet "Sådan omposteres lot- eller serienumre".

## <a name="to-assign-serial-or-lot-numbers-during-an-inbound-transaction"></a>Sådan tildeles serie- eller lotnumre under indgående transaktioner  
Mange virksomheder ønsker at holde styr på varer, lige så snart de modtager dem. I denne situation er købsordren ofte det centrale dokument, selvom varesporing kan håndteres fra alle indgående dokumenter, og de tilhørende poster kan ses i de tilknyttede vareposter.  

De nøjagtige regler for håndtering af varesporingsnumre i din virksomhed bestemmes af opsætningen i vinduet **Varesporingskodekort**.  

> [!NOTE]  
>  For at bruge varesporingsnumre i lageraktiviteter skal opsætningsfelterne **Lotlagersporing** og **Serienr.- lagersporing** vælges, da de definerer de bestemte regler for håndtering af serie- og lotnumre i lageraktiviteter.  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Købsordrer**, og vælg derefter det relaterede link.  
2.  Markér den relevante dokumentlinje, og vælg handlingen **Linje** i oversigtspanelet **Linjer**, og vælg derefter handlingen **Varesporingslinjer**.  

    Du kan tildele serie- eller lotnumre på følgende måder:  

    -   Automatisk ved at vælge **Tildel serienr.** eller **Tildel lotnr.** for at tildele serienumre/lotnumre fra foruddefinerede nummerserier.  
    -   Automatisk ved at vælge **Opret brugerdef. serienr.** for at tildele serienumre/lotnumre baseret på de parametre, du definerer for de ankomne varer.  
    -   Manuelt ved at angive serie- eller lotnumre direkte, f.eks. kreditornumrene.  
    -   Manuelt ved at tildele et specifikt nummer til hver vareenhed.  

3. Hvis du vil tildele automatisk, skal du vælge handlingen **Opret brugerdef. serienr.**.  
4. Angiv startnummeret i en beskrivende serienummerserie, f.eks. **S/N-Vend0001**, i feltet **Brugerdef. serienr.**.  
5. Indtast 1 i feltet **Forøgelse** for at angive, at hvert fortløbende nummer stiger med 1.  

    Feltet **Antal, der skal oprettes** indeholder standardlinjeantallet, men dette kan ændres.  

6. Marker afkrydsningsfeltet **Opret nyt lotnr.** for at organisere de nye serienumre i en bestemt lot.  
7. Vælg knappen **OK**.  

Der oprettes nu et lotnummer med individuelle serienumre i overensstemmelse med vareantallet på dokumentlinjen, startende med **S/N-Vend0001**.  

Matrixen for mængdefelter på formularhovedet viser dynamisk mængder og summer for de varesporingsnumre, du angiver i vinduet. Mængderne skal svare til mængderne på dokumentlinjen, der er angivet med 0 i felterne **Udefineret**.  

Når dokumentet er bogført, overføres varesporingsposterne til de tilknyttede vareposter.

## <a name="to-assign-a-serial-or-lot-number-during-an-outbound-transaction"></a>Sådan tildeles serie- eller lotnumre under en udgående transaktion  
Serie- og lotnumre kan føjes til udgående transaktioner på to måder:  

-   Vælg fra eksisterende serie- eller lotnumre. Bruges, når der allerede er blevet tildelt varesporingsnumre i forbindelse med en indgående transaktion. Du kan finde flere oplysninger i afsnittet "Sådan vælge fra eksisterende serie- eller lotnumre"
-   Tildeling af nye serie- eller lotnumre under udgående transaktioner. Dette gælder, når varesporingsnumre ikke skal tildeles til varer, før de er solgt og klar til at blive afsendt.  

Forskellige regler for varesporingsnumre er angivet i vinduet **Varesporingskodekort**.  

> [!NOTE]  
>  Når du vil tildele varesporingsnumre i lageraktiviteter, skal afkrydsningsfelterne **Serienr.- lagersporing** og **Lotlagersporing** være markeret på varens varesporingskodekort.    

1. Markér den relevante dokumentlinje, og vælg handlingen **Ordre** i oversigtspanelet **Linjer**, og vælg derefter handlingen **Varesporingslinjer**.  

    Du kan tildele varesporingsnumre på følgende måder:  
    -   Automatisk fra foruddefineret nummerserie: Vælg handlingen **Tildel serienr.** eller **Tildel lotnr.**.  
    -   Automatisk, på basis af de parametre, du definerer for den udgående vare: Vælg handlingen **Opret brugerdef. serienr.**.  
    -   Manuelt ved at angive serie- eller lotnumre uafhængigt af nummerserier.  

2.  For denne fremgangsmåde skal du tildele et serienummer automatisk ved at vælge **Tildel serienr.**  

    Feltet **Antal, der skal oprettes** indeholder standardlinjeantallet, men dette kan ændres.  
3.  Vælg feltet **Opret nyt lotnr.** for at organisere de nye serienumre i en bestemt lot.  
4.  Klik på **OK** for at oprette et lotnummer og nye individuelle serienumre i overensstemmelse med det antal, der skal håndteres på den tilsvarende dokumentlinje.  

Matrixen for mængdefelter i den øverste visning viser, dynamisk, mængder og summer for de varesporingsnumre, du angiver på formularen. Mængderne skal svare til mængderne på dokumentlinjen, der er angivet med **0** i felterne **Udefineret**.  

Når dokumentet er bogført, overføres varesporingsposterne til de tilknyttede vareposter.  

## <a name="to-select-from-existing-serial-or-lot-numbers"></a>Sådan vælges der fra eksisterende serienumre eller lotnumre  
Når du arbejder med varer, der kræver varesporing, og du opretter udgående transaktioner, hvor varerne forlader lageret, skal du som regel vælge lot- eller serienumrene ud fra dem, der allerede findes på lageret.  

 De nøjagtige regler for håndtering af varesporingsnumre i din virksomhed bestemmes af opsætningen af tabellen **Varesporingskode**.  

> [!NOTE]  
>  For at håndtere varesporingsnumre i lageraktiviteterne skal varen oprettes med Serienr. - lagersporing / Lotlagersporing, da dette angiver de særlige regler, der gælder for serie og lotnumre på lageret.

1.  Marker den linje, du vil vælge et lot- eller serienummer til, i et hvilket som helst udgående dokument.  
2.  I oversigtspanelet **Linjer**, skal du vælge **Handlinger**, vælge handlingen **Linje** eller **Vare**, og derefter vælge handlingen **Varesporingslinjer**.  
3.  I formularen **Varesporingslinjer** har du tre muligheder for at vælge lot- eller serienumre:  

    -   Klik på feltet **Lotnr.** eller **Serienr.**, og vælg derefter et nummer fra vinduet **Varesporingsoversigt**.  
    -   Vælg handlingen **Vælg poster**. Vinduet **Marker poster** viser alle lot- eller serienumre sammen med disponeringsoplysninger.

4. I feltet **Valgt antal** skal du angive antallet for hvert af de lot- eller serienumre, du vil bruge.   
5. Klik på **OK**, hvorefter programmet overfører de valgte varesporingsoplysninger til vinduet **Varesporingslinjer**.  
6. Indtast eller scan varesporingsnummeret.

Matrixen for mængdefelter på formularhovedet viser dynamisk mængder og summer for de varesporingsnumre, du angiver i vinduet. Mængderne skal svare til mængderne på dokumentlinjen, der er angivet med **0** i felterne **Udefineret**.  

 Når du bogfører dokumentlinjen, overføres varesporingsoplysningerne til de tilknyttede vareposter.

## <a name="to-handle-serial-and-lot-numbers-on-transfer-orders"></a>Sådan håndteres serie- og lotnumre på overflytningsordrer  
Procedurerne for håndtering af serie- og lotnumre, der overføres mellem forskellige lokationer, ligner de procedurer, der bruges, når varer sælges eller købes.  

Overførselsordren er imidlertid entydig i den pågældende leverance, og begge modtagelser sker fra den samme overførselslinje og bruger derfor den samme forekomst i vinduet **Varesporingslinjer**. Det betyder, at varesporingslinjer, der sendes fra en lokation, skal modtages uændret på en anden.  

 De nøjagtige regler for håndtering af varesporingsnumre i din virksomhed bestemmes af opsætningen af tabellen  **Varesporingskode**.    
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Overflytningsordrer**, og vælg derefter det relaterede link.  
2.  Åbn den overflytningsordre, du vil behandle. I oversigtspanelet **Linjer**, skal du vælge handlingen **Linje**, vælge handlingen **Varesporingslinjer** og derefter vælge handlingen **Leverance**.  
3.  Tilknyt eller vælg serie- eller lotnumre i vinduet **Varesporingslinjer** som for enhver anden udgående varetransaktion.  

    Når du arbejder med serie- og lotnumre for overflytningsvarer, er der normalt allerede tildelt numre til varerne. Derfor består proceduren oftest af at vælge fra de eksisterende serie- eller lotnumre.  

4.  Bogfør overflytningsordren (leverance og modtagelse) for at registrere, at varerne er blevet overført med deres specifikke varesporingsposter.  

Under overførslen er vinduet **Varesporingslinjer** låst, så der ikke kan skrives i dem.  

## <a name="to-handle-serial-and-lot-numbers-when-getting-receipt-lines-from-a-purchase-invoice"></a>Sådan håndteres serie- og lotnumre, når der hentes modtagelseslinjer fra en købsfaktura  
Hvis du bruger funktioner til at få bogførte modtagelses- eller afsendelseslinjer fra relaterede fakturaer eller kreditnotaer, så overføres alle varesporingslinjer på lagerdokumenter automatisk, men de behandles de på en særlig måde.

Funktionen understøtter følgende indgående processer:  
-   **Hent købsleverancelinjer** – fra en købsfaktura.  
-   **Hent returvarelev.linjer** – fra en købskreditnota.  

Funktionen understøtter følgende udgående processer:  
-   **Hent salgsleverancelinjer** – fra en salgsfaktura eller kombinerede leverancer.  
-   **Hent returvaremodt.linjer** – fra en salgskreditnota.  

I disse situationer kopieres de eksisterende varesporingslinjer automatisk til fakturaen eller kreditnotaen, men vinduet **Varesporingslinjer** tillader ikke, at serie- eller lotnumre ændres. Det er kun mængderne, der kan ændres.  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Købsfakturaer**, og vælg derefter det relaterede link.  
2.  Åbn en købsfaktura for varer, der er køb med serienumre eller lotnumre.  
3.  Fra en købsfakturalinje skal du i oversigtspanelet **Linjer** vælge handlingen **Hent købsleverancelinjer**.  
4.  Vælg modtagelseslinjer, der har varesporingslinjer i vinduet **Hent købsleverancelinjer**, og vælg derefter knappen **OK**.  

    Kildedokumentet kopieres til købsfakturaen som en ny linje, og dets varesporingslinjer overføres uændret til det underliggende vindue **Varesporingslinjer**.  

5.  Vælg den overførte modtagelseslinje i købsfakturaen.  
6.  I oversigtspanelet **Linjer** skal du vælge handlingen **Linje** og derefter vælge handlingen **Varesporingslinjer** for at få vist de overførte varesporingslinjer.  

Du kan ikke ændre felterne **Serienr.** og **Lotnr.** Du kan imidlertid slette hele linjer eller ændre mængder, så de svarer til de ændringer, der er foretaget på kildelinjen.  

## <a name="to-reclassify-serial-or-lot-numbers"></a>Sådan omposteres serie- eller lotnumre  
Ompostering af varesporing for en vare betyder, at et lot- eller serienummer ændres til et nyt lot- eller serienummer, eller at udløbsdatoen ændres til en ny udløbsdato. Hvis du arbejder med lotter, kan du også samle flere lotter i en enkelt lot. Disse opgaver udføres ved hjælp af vareomposteringskladden.

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Vareomposteringskladde**, og vælg derefter det relaterede link.  
2.  Udfyld linjen med de relevante oplysninger. Du kan finde flere oplysninger i [Fremgangsmåde: Tælle, justere og ompostere inventar](inventory-how-count-adjust-reclassify.md).
3.  Vælg handlingen **Varesporingslinjer**.  
4.  Vælg det aktuelle serie- eller lotnummer i feltet **Serienr.** eller **Lotnr.**.  
5.  Hvis du vil angive et nyt varesporingsnummer, skal du angive det i feltet **Nyt serienummer** eller **Nyt lotnr.**. Du kan flette en eller flere lotter til en ny eller en eksisterende lot.  

    > [!NOTE]  
    >  Når du omposterer udløbsdatoer, skal du være opmærksom på, at varene med den tidligste udløbsdato for udgående transaktioner foreslås først. Du kan finde flere oplysninger i [Plukke efter FEFO](warehouse-picking-by-fefo.md).  

5.  Hvis du vil angive en ny udløbsdato for serie- eller lotnummeret, skal du angive det i feltet **Ny udløbsdato**.  

    > [!IMPORTANT]  
    >  Hvis du omposterer en lot til det samme lotnummer, men med en anden udløbsdato, skal du ompostere hele lotten ved hjælp af én vareomposteringskladdelinje. Hvis du omposterer mere end én lot til én ny lot, skal du angive den samme nye udløbsdato for alle lot'ene. Hvis du omposterer én eksisterende lot til en anden eksisterende lot, som har en anden udløbsdato, skal du bruge udløbsdatoen fra den anden lot. Hvis du lader feltet **Ny udløbsdato** være tomt, vil lot- eller serienummeret blive omposteret med en tom udløbsdato.  

6.  Hvis du har eksisterende oplysninger om det gamle serie- eller lotnummer, kan du kopiere dem til det nye serie- eller lotnummer.  

    1.  I vinduet **Varesporingslinjer** skal du vælge handlingen **Nye serienr.oplysninger** eller handlingen **Nye lotnr.oplysninger**.  
    2.  Hvis du vil kopiere oplysninger fra det gamle lot- eller serienummer, skal du vælge handlingen **Kopier oplysninger**.  
    3.  Vælg det lot- eller serienummer, du vil kopiere fra, i vinduet med oplysninger, og vælg knappen **OK**.  

7.  Hvis du vil ændre de eksisterende oplysninger for lot- eller serienummeret, kan du angive lot- eller serieoplysninger.  
8.  Bogfør kladden for at linke de ændrede varesporingsnumre eller udløbsdatoerne til den tilknyttede varepost

## <a name="see-also"></a>Se også
[Sådan gør du: Spore varesporede varer](inventory-how-to-trace-item-tracked-items.md)   
[Lagerbeholdning](inventory-manage-inventory.md)  
[Designoplysninger: Varesporing](design-details-item-tracking.md)
[Designoplysninger: Varesporing og reservationer](design-details-item-tracking-and-reservations.md)  
[Sådan reserverer du varer](inventory-how-to-reserve-items.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

