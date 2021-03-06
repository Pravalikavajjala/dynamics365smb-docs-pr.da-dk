---
title: "Sådan arbejder du med moms af salg og køb | Microsoft Docs"
description: "I dette emne beskrives, hvordan du udfører opgaver som at korrigere bogført moms i EU-lande/områder, hvor der beregnes moms af alle salgs- og købstransaktioner. I dette emne kan du læse, hvordan du gør."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: VAT, sales, purchases,
ms.date: 09/08/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 596b5d73e019375aa84b7cb227d305fc29762ae1
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-work-with-vat-on-sales-and-purchases"></a>Fremgangsmåde: Arbejde moms af salg og køb
Hvis dit land eller område kræver, at du beregner moms af salgs- og købstransaktioner, så du kan indberette beløbene til skattemyndighederne, kan du konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)] til automatisk at beregne moms på salgs- og købsdokumenter. Du kan finde flere oplysninger i [Konfigurere beregnings- og bogføringsmetoder for moms] (finance-setup-vat.md).

Der er dog nogle opgaver i forbindelse med moms, der kan udføres manuelt. Du kan f.eks. rette et bogførte beløb, hvis du opdager, at en leverandør anvender en anden afrundingsmetode.

## <a name="calculating-and-displaying-vat-amounts-in-sales-and-purchase-documents"></a>Beregne og vise momsbeløb i salg- og købsdokumenter  
Du kan beregne og vise momsbeløb i salgs- og købsdokumenter forskelligt, afhængigt af den type debitor eller kreditor, du handler med. Du kan også tilsidesætte det beregnede momsbeløb for at have det samme momsbeløb som det, der er beregnet af kreditoren i en given transaktion.  

### <a name="unit-price-and-line-amount-includingexcluding-vat-on-sales-documents"></a>Salgspris og linjebeløb inkl./ekskl. moms i salgsdokumenter  
Når du vælger et varenummer i feltet **Nummer** i et salgsdokument, udfylder [!INCLUDE[d365fin](includes/d365fin_md.md)] også feltet **Salgspris**. Salgsprisen stammer fra enten **Vare**-kortet eller fra de varesalgspriser, der er tilladt for varen og debitoren. [!INCLUDE[d365fin](includes/d365fin_md.md)] beregner kun **Linjebeløb**, når du angiver et antal for linjen.  

Hvis du sælger til detailhandelsvirksomheder, skal priserne på salgsdokumenterne evt. være inkl. moms. For at gøre dette skal du markere afkrydsningsfeltet **Priser inkl. moms** på dokumentet.  

### <a name="including-or-excluding-vat-on-prices"></a>Priser med eller uden moms
Hvis afkrydsningsfeltet **Priser inkl. moms** er markeret på et salgsdokument, vil felterne **Salgspris** og **Linjebeløb** være inkl. moms. Feltnavnene vil også afspejle dette. Som standard er moms ikke inkluderet i disse felter.  

Hvis afkrydsningsfeltet ikke er markeret, vil felterne **Salgspris** og **Linjebeløb** udfyldes ekskl. moms, og feltnavnene vil afspejle dette.  

Du kan oprette standardindstillinger for **Priser inkl. moms** for alle salgsdokumenterne for en kunde i feltet **Priser inkl. moms** på kortet **Debitor**. Du kan også oprette varesalgspriser, så de er inkl. eller ekskl. moms. Sædvanligvis vil varesalgsprisen på varekortet være prisen ekskl. moms. Det er oplysningerne i feltet **Salgspris inkl. moms** på **Vare**-kortet, der bruges til at bestemme salgsprisbeløbet for salgsdokumenter.  

Følgende tabel indeholder en oversigt over, hvordan salgsprisbeløbene for et salgsdokument beregnes, når du har oprettet priser i vinduet **Salgspriser**:  

|**Feltet Salgspris inkl. moms på varekortet**|**Feltet Priser inkl. moms i salgshovedet**|**Handling**|  
|-----------------------------------------------|----------------------------------------------------|--------------------------|  
|Ingen markering|Ingen markering|**Salgsprisen** på varekortet kopieres til feltet **med salgsprisen ekskl. moms** i salgslinjerne.|  
|Ingen markering|Markering|Momsbeløbet pr. salgsenhed beregnes og lægges til **salgsprisen** på varekortet. Den samlede salgspris indsættes derefter i feltet **med salgsprisen inkl. moms** på salgslinjerne.|  
|Markering|Ingen markering|Programmer beregner momsbeløbet, der er medtaget i **Salgsprisen** på varekortet ved hjælp af momsprocenten relateret til feltet Momsvirksomhedsbogf.gruppe. Bogføring Gr. (Pris) og Modkontos momsprod.bogf.gr. Kombination af bogføringsgruppe. **Salgsprisen** på varekortet, reduceret med momsbeløbet, angives derefter i feltet **Enhed pris ekskl. MOMS** i salgslinjerne.|  
|Markering|Markering|**Salgsprisen** på varekortet kopieres til feltet **med salgsprisen inkl. moms** i salgslinjerne.|

## <a name="correcting-vat-amounts-manually-in-sales-and-purchase-documents"></a>Manuel korrektion af momsbeløb i salgs- og købsdokumenter  
Du kan korrigere bogførte momsposter. Det giver mulighed for at ændre de samlede salgs- eller købsmomsbeløb uden at ændre momsgrundlaget. Det kan være nødvendigt, hvis du f.eks. modtager en faktura fra en leverandør, der har beregnet momsen forkert.  

Selvom du måske har oprettet en eller flere kombinationer til håndtering af importmoms, skal du angive mindst én momsproduktbogføringsgruppe. For eksempel kan du navngive den **RETTELSER** med henblik på korrektion, medmindre du kan bruge den samme finanskonto i feltet **Købsmomskonto** på momsbogføringslinjen. Du kan finde flere oplysninger i [Konfigurere beregnings- og bogføringsmetoder for moms](finance-setup-vat.md).

Hvis en kontantrabat er beregnet på basis af et fakturabeløb, der er inkl. moms, tilbagefører du momsen af kontantrabatten, når rabatten er tildelt. Bemærk, at du skal aktivere feltet **Reguler moms ved kontantrabat** for både opsætning af finanskontiene generelt og momsbogføringsopsætning for en bestemt kombination af en momsvirksomhedsbogføringsgruppe og en momsproduktbogføringsgruppe.  

#### <a name="to-manually-enter-vat-in-sales-documents"></a>Sådan angives moms manuelt i salgsbilag  
1. På siden **Regnskabsopsætning** skal du angive **Maks. momsdifference tilladt** mellem det beløb, der beregnes af programmet, og det manuelle beløb.  
2. På siden **Salgsopsætning** skal du markere afkrydsningsfeltet **Tillad momsdifference**.  

#### <a name="to-adjust-vat-for-a-sales-document"></a>Sådan reguleres moms for et salgsdokument  
1. Åbn den relevante Salgsordre.  
2. Vælg handlingen **Statistik**.  
3. Vælg oversigtspanelet **Fakturering**.  
  
    > [!NOTE]  
    >  Det samlede momsbeløb på fakturaen, grupperet efter moms-id, vises på linjerne. Du kan justere beløbet manuelt i feltet **Momsbeløb** på linjerne for hvert moms-id. Når du retter i feltet **Momsbeløb**, kontrolleres det, at du ikke har ændret momsen med mere end det beløb, du har angivet som den maksimalt tilladte difference. Hvis beløbet er uden for **den maksimalt tilladte momsdifference**, vises der en advarsel, hvor den maksimalt tilladte difference vises. Du vil ikke kunne fortsætte, før beløbet ændres, så det ligger inden for de acceptable parametre. Klik på **OK** , og angiv et andet **momsbeløb**, som ligger inden for det tilladte. Hvis momsdifferencen er lig med eller lavere end den maksimalt tilladte, deles momsen proportionalt mellem de dokumentlinjer, der har det samme moms-id.  

## <a name="calculating-vat-manually-using-journals"></a>Manuel momsberegning ved hjælp af kladder  
Du kan også justere momsbeløb i finans-, salgs- og købskladder. Det kan f.eks. være nødvendigt, når du angiver en kreditorfaktura i kladden, og der er en forskel mellem det momsbeløb, som [!INCLUDE[d365fin](includes/d365fin_md.md)] har beregnet, og momsbeløbet på kreditorfakturaen.  

#### <a name="before-you-manually-enter-vat-on-a-general-journal"></a>Før du manuelt angiver moms i en finanskladde  
1. På siden **Regnskabsopsætning** skal du angive **Maks. momsdifference tilladt** mellem det beløb, der beregnes af programmet, og det manuelle beløb.  
2. På siden **Finanskladdetyper** skal du markere afkrydsningsfeltet **Tillad momsdifference** for den relevante kladde.  

#### <a name="before-you-manually-enter-vat-on-sales-and-purchase-journals"></a>Før du manuelt angiver moms i salgs- og købskladder  
1. På siden **Købsopsætning** skal du markere afkrydsningsfeltet **Tillad momsdifference**.  
2. Når du har fuldført konfigurationen som beskrevet ovenfor, kan du justere værdien i feltet **Momsbeløb** på finanskladdelinjen eller værdien i feltet **Modkontos momsbeløb** på salgs- eller købskladdelinjen. [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrollerer, at differencen ikke er større end det angivne maksimum.  
  
    > [!NOTE]  
    > Hvis differencen er større, bliver der vist en advarsel med den maksimalt tilladte difference. Hvis du vil fortsætte, skal du justere beløbet. Vælg **OK**, og angiv derefter et beløb, som ligger inden for det tilladte. Hvis momsforskellen er lig med eller lavere end det maksimalt tilladte, viser [!INCLUDE[d365fin](includes/d365fin_md.md)] differencen i feltet **Momsdifference**.  

## <a name="to-post-import-vat-with-purchase-invoices"></a>Sådan bogføres importmoms på købsfakturaer
I stedet for at bruge en finanskladde, når du bogfører en faktura med importmoms, kan du bruge en købsfaktura.  

### <a name="to-set-up-purchasing-for-posting-import-vat-invoices"></a>Konfigurere Indkøb til at bogføre fakturaer med importmoms  
1. Opret et kreditorkort for den importmyndighed, der sender dig fakturaen med importmoms. Du skal vælge de samme indstillinger til **Virksomhedsbogføringsgruppe** og **Momsvirksomhedsbogf.gruppe** som til den finanskonto, der bruges til importmoms.  
2. Opret en **Produktbogføringsgruppe** til importmomsen, og opret en **Momsproduktbogf.gruppe**, der skal bruges som standard til den tilhørende **Produktbogføringsgruppe**.  
3. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kontoplan**, og vælg derefter det relaterede link.  
4. Markér finanskontoen for importmoms og vælg derefter **Rediger** i gruppen **Administrer** under fanen **Startside**.  
5. På oversigtspanelet **Bogføring** skal du vælge opsætningen **Produktbogføringsgruppe** for at importere moms. [!INCLUDE[d365fin](includes/d365fin_md.md)] udfylder automatisk feltet **Momsproduktbogf.gruppe**.  
6. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bogføringsopsætning**, og vælg derefter det relaterede link.  
7. Opret en kombination af **Virksomhedsbogføringsgruppe** til momsmyndighederne og **Produktbogføringsgruppe** til importmoms. Til denne nye kombination skal du i feltet **Købskonto** vælge finanskontoen for importmoms.  

### <a name="to-create-a-new-invoice-for-the-import-authority-vendor-once-you-have-completed-the-setup"></a>Sådan oprettes en ny faktura til importmyndigheden (leverandører), når du har foretaget opsætningen  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Købsfakturaer**, og vælg derefter det relaterede link.  
2. Opret en ny købsfaktura.  
3. I feltet **Leverandørnr.** skal du vælge importmyndigheden (leverandøren), og derefter vælge knappen **OK**.  
4. På købslinjen i feltet **Type** skal du vælge **Finanskonto** og i feltet **Nummer** og vælge finanskontoen til importmoms.  
5. I feltet **Antal** skal du skrive **1**.  
6. Angiv momsbeløbet i feltet **Købspris Ekskl. moms**.  
7. Bogfør fakturaen.  

## <a name="to-process-certificates-of-supply"></a>Sådan behandles leveringscertifikater
Når du sælger varer til en kunde i et andet EU-land/-område, skal du tilsende kunden et leveringscertifikat, som kunden skal underskrive og returnere til dig. Der er følgende procedurer for behandling af leveringscertifikater for salgsleverancer, men de samme trin gælder for serviceleverancer af varer og returvareleverancer til kreditorer.  

### <a name="to-view-certificate-of-supply-details"></a>Sådan får du vist leveringscertifikatdetaljer  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bogf. salgsleverancer**, og vælg derefter det relaterede link.  
2. Vælg den relevante salgsleverance til en kunde i et andet EU-land/-område.  
3. Vælg **Leveringscertifikatdetaljer**.  
4. Som standard, hvis afkrydsningsfeltet **Leveringscertifikat påkrævet** er markeret for opsætningen af momsbogføringsgruppen for kunden, er feltet **Status** indstillet til **Påkrævet**. Du kan opdatere feltet for at angive, om kunden har returneret certifikatet.  

    > [!Note]  
    >  Hvis opsætningen af momsbogføringsgruppe ikke har afkrydsningsfeltet **Leveringscertifikat påkrævet** markeret, oprettes der en post, og feltet **Status** indstilles til **Ikke tilgængelig**. Du kan opdatere feltet for at afspejle de korrekte statusoplysninger. Du kan manuelt ændre status fra **Ikke tilgængelig** til **Påkrævet** og fra **Påkrævet** til **Ikke tilgængelig** efter behov.  

   Når du opdaterer feltet **Status** til **Påkrævet**, **Modtaget** eller **Ikke modtaget**, oprettes der et certifikat.  
  
    > [!TIP]  
    >  Du kan bruge vinduet **Leveringscertifikater** til at få et overblik over status for alle bogførte leverancer, der er blevet oprettet et leveringscertifikat for.  

5. Vælg **Udskriv leveringscertifikat**.  
  
    > [!Note]  
    >  Du kan se eller udskrive dokumentet. Når du vælger **Udskriv leveringscertifikat** og udskriver dokumentet, bliver afkrydsningsfeltet **Udskrevet** automatisk markeret. Desuden, hvis det ikke allerede er angivet, opdateres status for certifikatet til **Påkrævet**. Du kan evt. også medtage det udskrevne certifikat i leverancen.  

### <a name="to-print-a-certificate-of-supply"></a>Sådan udskriver du et leveringscertifikat  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bogf. salgsleverancer**, og vælg derefter det relaterede link.  
2. Vælg den relevante salgsleverance til en kunde i et andet EU-land/-område.  
3. Vælg handlingen **Udskriv leveringscertifikat**.  

    > [!NOTE]  
    >  Alternativt kan du udskrive et certifikat fra siden **Leveringscertifikat**.  

4. Markér afkrydsningsfeltet **Udskriv linjedetaljer** for at medtage oplysninger fra linjerne på leverancedokumentet i certifikatet.  
5. Markér afkrydsningsfeltet **Opret leveringscertifikater, hvis de ikke allerede er oprettet** for at få [!INCLUDE[d365fin](includes/d365fin_md.md)] til at oprette certifikater til bogførte leverancer, der ikke har ét på tidspunktet for udførelsen. Når du markerer afkrydsningsfeltet, oprettes nye certifikater for alle bogførte leverancer, der ikke har certifikater i det valgte område.  
6. Som standard er filterindstillingerne for det leverancedokument, du har valgt. Udfyld filtreringsoplysningerne for at vælge et bestemt certifikat for levering, som du vil udskrive.  
7. På siden **Leveringscertifikat** skal du vælge knappen **Udskriv** for at udskrive rapporten eller vælge handlingen **Vis udskrift** for at se den på skærmen.  

    > [!Note]  
    > Feltet **Status for leveringscertifikat** og feltet **Udskrevet** opdateres med leveringen på siden **Leveringscertifikater**.  

8. Send det trykte leveringscertifikat til underskrift hos kunden.  

### <a name="to-update-the-status-of-a-certificate-of-supply-for-a-shipment"></a>Sådan opdaterer du status for et leveringscertifikat til en leverance  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bogf. salgsleverancer**, og vælg derefter det relaterede link.  
2. Vælg den relevante salgsleverance til en kunde i et andet EU-land/-område.  
3. Vælg den relevante indstilling i feltet **Status**.  

   Hvis kunden ikke har returneret det signerede forsyningscertifikat, skal du vælge **Ikke modtaget**. Feltet **Modtagelsesdato** opdateres. Modtagelsesdatoen er som standard angivet til den aktuelle arbejdsdato.  

   Du kan ændre datoen for at afspejle den dato, hvor du modtog kundens signerede leveringscertifikat. Du kan også føje et link til det signerede certifikat ved hjælp af almindelig [!INCLUDE[d365fin](includes/d365fin_md.md)]-sammenkædning.  

   Hvis kunden ikke returnerer det signerede forsyningscertifikat, skal du vælge **Ikke modtaget**. Du skal derefter tilsende kunden en ny faktura, der inkluderer moms, fordi den oprindelige faktura ikke vil blive accepteret af skattemyndighederne.  

Hvis du vil se en gruppe af certifikater, skal du starte fra vinduet **Leveringscertifikater** og derefter opdatere oplysninger om status for udestående certifikater, når du får dem tilbage fra dine kunder. Dette kan være nyttigt, når du vil søge efter alle de certifikater, der har en bestemt status, for eksempel **Påkrævet**, hvis status du vil opdatere til **Ikke modtaget**.  

### <a name="to-update-the-status-of-a-group-of-certificates-of-supply"></a>Sådan opdaterer du status for en gruppe af leveringscertifikater  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Leveringscertifikater**, og vælg det relaterede link.  
2. Filtrer feltet **Status** til den værdi, du ønsker, for at oprette en liste over certifikater, som du vil administrere.  
3. For at opdatere statusoplysningerne skal du vælge **Rediger liste**.  
4. Vælg den relevante indstilling i feltet **Status**.  

   Hvis kunden ikke har returneret det signerede forsyningscertifikat, skal du vælge **Ikke modtaget**. Feltet **Modtagelsesdato** opdateres. Modtagelsesdatoen er som standard angivet til den aktuelle arbejdsdato.  

   Du kan ændre datoen for at afspejle den dato, hvor du modtog det signerede leveringscertifikat. Du kan også føje et link til det signerede certifikat ved hjælp af almindelig [!INCLUDE[d365fin](includes/d365fin_md.md)]-dokumentsammenkædning.  

    > [!NOTE]  
    >  Du kan ikke oprette et nyt leveringscertifikat i vinduet **Leveringscertifikat**, når du navigerer til det ved hjælp af denne procedure. Hvis du vil oprette et certifikat til en forsendelse, der ikke var sat op til at kræve ét, skal du åbne den bogførte salgsleverance og bruge den ene af de to fremgangsmåder, der er beskrevet ovenfor:  
    >   
    > * Sådan opretter du manuelt et leveringscertifikat  
    > * Sådan udskriver du et leveringscertifikat.

## <a name="see-also"></a>Se også  
[Konfigurere beregnings- og bogføringsmetoder for moms](finance-setup-vat.md)   
[Fremgangsmåde: Rapportere moms til en skattemyndighed](finance-how-report-vat.md)   

