---
title: Betalingstolerance og kontantrabattolerance | Microsoft Docs
description: "Du kan angive betalingstolerance for at afslutte en faktura, når betalingen ikke fuldt ud dækker beløbet på fakturaen."
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
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: c6365507992b75d5fa264491bbc85bb1b4a8ed7a
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-work-with-payment-tolerances-and-payment-discount-tolerances"></a>Fremgangsmåde: Arbejde med betalingstolerancer og kontantrabattolerancer
Du kan angive en betalingstolerance for at afslutte en faktura, når betalingen ikke fuldt ud dækker beløbet på fakturaen. Du kan angive en kontantrabattolerance til at give kontantrabat, efter at kontantrabatdatoen er overskredet.  

Du kan bruge betalingstolerancer, så alle udestående beløb har en angivet maksimal tilladt betalingstolerance. Hvis betalingstolerance er overholdt, analyseres det indbetalte beløb. Hvis det indbetalte beløb er utilstrækkeligt, vil det udestående beløb lukkes helt af den utilstrækkelige indbetaling. Der bogføres automatisk en detaljeret post på betalingsposten, så der ikke er noget restbeløb på den udlignede fakturapost. Hvis det indbetalte beløb er en overbetaling, bogføres automatisk en ny detaljeret post på betalingsposten, så der ikke er noget restbeløb på betalingsposten.

Du kan bruge kontantrabattolerancer, så hvis du accepterer en kontantrabat efter kontantrabatdatoen, bogføres den altid på enten kontantrabatkontoen eller en betalingstolerancekonto.

## <a name="applying-payment-tolerance-to-multiple-documents"></a>Anvendelse af betalingstolerance for flere dokumenter  
Et enkelt dokument har den samme betalingstolerance, hvad enten det bruges individuelt eller sammen med andre dokumenter. Accept af forsinket kontantrabat, når du anvender betalingstolerance på flere dokumenter, finder automatisk sted for hvert dokument, hvor følgende regel gælder:  

*kontantrabatdato < betalingsdato på den valgte post <= betalingstolerancedato*  

Denne regel gælder også, når det skal afgøres, om der skal vises advarsler, når du anvender betalingstolerance på flere dokumenter. Kontantrabattoleranceadvarslen vises for hver post, der opfylder datokriterierne. Yderligere oplysninger finder du i afsnittet "Eksempel 2 - Toleranceberegninger for flere bilag".

Du kan vælge at vise en advarsel, der er baseret på tolerance i forskellige situationer.  

- Den første advarsel er til kontantrabatdatoen. Du bliver informeret om, at du kan acceptere en forsinket kontantrabat. Du kan derefter vælge, om der skal accepteres tolerance på rabatdatoen.  
- Den anden advarsel er til betalingstolerancen. Du bliver informeret om, at alle poster kan lukkes, fordi differencen ligger inden for den samlede, maksimale betalingstolerance for de udlignede poster. Du kan derefter vælge, om der skal accepteres tolerance på betalingsdatoen.

Du kan finde flere oplysninger i "Sådan aktiveres eller deaktiveres betalingstoleranceadvarsel".     

## <a name="to-set-up-tolerances"></a>Sådan opsættes tolerancer  
Tolerancer på dato eller beløb giver dig mulighed for at afslutte en faktura, også selvom den ikke dækker fakturabeløbet fuldt ud, uanset om det skyldes, at forfaldsdatoen for betalingsrabatten er overskredet, om der er fratrukket varer, eller om der er tale om en mindre fejl. Det samme gælder for refusioner og kreditnotaer.  

Hvis du skal opsætte tolerancer, skal du oprette forskellige tolerancekonti. Du skal både angive en metode til bogføring af kontantrabattolerance og en metode til bogføring af betalingstolerance og derefter afvikle kørslen **Skift betalingstolerance**.  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bogføringsopsætning**, og vælg derefter det relaterede link.  
2. I vinduet **Bogføringsopsætning** skal du oprette en debet- og en kreditsalgstolerancekonto og en debet- og kreditkøbstolerancekonto.  
3. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Debitorbogføringsgrupper**, og vælg derefter det relaterede link.    
4. I vinduet **Debitorbogføringsgrupper** skal du oprette en debet- og en kreditbetalingstolerancekonto. Du kan finde flere oplysninger under [Konfigurere bogføringsgrupper](finance-posting-groups.md).  
5. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bogføringsopsætning**, og vælg derefter det relaterede link.  
6. I vinduet **Kreditorbogføringsgrupper** skal du oprette en debet- og en kreditbetalingstolerancekonto.  
7. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opsætning af Finans**, og vælg derefter det relaterede link.  
8. Åbn vinduet **Opsætning af finans**.  
9. På oversigtspanelet **Udligning** skal du udfylde felterne **Bogf. af kont.rabattolerance**, **Kontantrabat - respitperiode** and **Bogf. af betalingstolerance**.   
10. Vælg handlingen **Skift betalingstolerance**.
11. I vinduet **Skift betalingstolerance** skal du udfylde felterne **Betalingstolerancepct.** og **Maks. betalingstolerancebeløb** og derefter vælge knappen **OK**.

> [!IMPORTANT]  
>  Du har nu kun opsat tolerancer for lokal valuta. Hvis [!INCLUDE[d365fin](includes/d365fin_md.md)] skal håndtere betalingstolerancer, kreditnotaer og refusioner i fremmed valuta, skal du udføre kørslen **Skift betalingstolerance** med en værdi i feltet **Valutakode**.  

> [!NOTE]  
>  Hvis du vil have vist en advarsel om betalingstolerance, hver gang du bogfører en udligning inden for tolerancen, skal du aktivere betalingstoleranceadvarslen. Du kan finde flere oplysninger i "Sådan aktiveres eller deaktiveres betalingstoleranceadvarsel".  
>   
>  For at deaktivere tolerancer for en debitor eller kreditor skal du spærre tolerancer på de relevante debitor- eller kreditorkort. Du kan finde flere oplysninger i afsnittet "Sådan spærres betalingstolerancer for debitorer".  
>   
>  Når du opsætter tolerancer, kontrolleres det via [!INCLUDE[d365fin](includes/d365fin_md.md)], om der er åbne poster, og tolerancen beregnes også for disse poster.

## <a name="to-enable-or-disable-payment-tolerance-warnings"></a>Sådan aktiveres eller deaktiveres betalingstoleranceadvarsler
Advarslen om betalingstolerance vises, når du bogfører en udligning, der har en saldo i den tilladte tolerance. Du kan derefter vælge, hvordan du vil bogføre og dokumentere saldoen.    
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opsætning af Finans**, og vælg derefter det relaterede link.  
2. I vinduet **Opsætning af Finans** på oversigtspanelet **Udligning** skal du markere afkrydsningsfeltet **Betalingstolerance - advarsel** for at aktivere advarslen. Fjern markeringen i afkrydsningsfeltet, hvis du vil deaktivere advarslen.  

> [!NOTE]  
>  Standardindstillingen for vinduet **Betalingstolerance - advarsel** er **Lad saldoen stå som restbeløb**. Standardindstillingen for vinduet **Kont.rabattolerance - advarsel** er **Afvis den forsinkede kontantrabat**.

## <a name="to-block-payment-tolerance-for-customers"></a>Sådan spærres betalingstolerancer for debitorer  
Standardindstillingen for betalingstolerancer er tilladt. Hvis du vil afvise betalingstolerancer for en bestemt debitor eller kreditor, skal du spærre tolerancer på henholdsvis debitor- eller kreditorkortet. Følgende beskriver, hvordan du skal gøre det for en debitor. Trinene er de samme for en kreditor.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Debitor** eller **Kreditor**, og vælg derefter det relaterede link.  
2. På oversigtspanelet **Betalinger** skal du vælge afkrydsningsfeltet **Spær betalingstolerance**.  

> [!NOTE]  
>  Hvis debitoren eller kreditoren har åbne poster, skal du først fjerne betalingstolerancer fra poster, der aktuelt er åbne.

## <a name="example-1---tolerance-calculations-for-a-single-document"></a>Eksempel 1 – Toleranceberegninger for et enkelt bilag
Nedenfor findes nogle eksempelscenarier, som viser de forventede toleranceberegninger og -bogføringer, der kan opstå i forskellige situationer.  

Vinduet **Regnskabsopsætning** indeholder følgende opsætning:
- Kontantrabat - respitperiode    5D  
- Maks. betalingstolerance: 5  

Scenarier med alternativ A eller B repræsenterer følgende:  

- **A** – I dette tilfælde er advarslen om kontantrabattolerance slået fra, ELLER brugeren har slået advarslen til og valgt at tillade den forsinkede kontantrabat (Bogfør saldoen som betalingstolerance).  
- **B** – I dette tilfælde har brugeren slået advarslen til og valgt ikke at tillade den forsinkede kontantrabat (Lad saldoen stå som restbeløb).  

[!div class="mx-tdBreakAll"]  
|–|Faktura|Kont.rabat|Maks. betal.tol.|Kont.rabatdato|Kont.rabattol. Dato|Betal.dato|Kont.|Tol.type|Alle poster lukket|Kont.rabattol. finans/debitor|Bet.Tol. finans|  
|-------|----------|----------------|-----------------------|---------------------|--------------------------|------------------|----------|--------------------|------------------------|------------------------------|----------------------------|  
|1|1.000|20|5|01/15/03|01/20/03|<=15-01-03|985|Pmt.Tol.|Ja|0|-5|  
|2|**1,000**|**20**|**5**|**01/15/03**|**01/20/03**|**<=01/15/03**|**980**|**Ingen**|**Ja**|**0**|**0**|  
|3|1.000|20|5|01/15/03|c|<=15-01-03|975|Pmt.Tol.|Ja|0|5|  
|4A|1.000|20|5|01/15/03|01/20/03|16.01.03 - 20-01-03|1005|Kont.rab.tolerance|Nr, 25 kont.|20/-20|0|  
|5A|1.000|20|5|01/15/03|01/20/03|16.01.03 - 20-01-03|1000|Kont.rab.tolerance|Nr, 20 kont.|20/-20|0|  
|8.0pt|1.000|20|5|01/15/03|01/20/03|16.01.03 - 20-01-03|995|Kont.rab.tolerance|Nr., 15 kont.|20/-20|0|  
|4B|1.000|20|5|01/15/03|01/20/03|16.01.03 - 20-01-03|1005|Pmt.Tol.|Ja|0|-5|  
|**5B**|**1,000**|**20**|**5**|**01/15/03**|**01/20/03**|**16.01.03 - 20-01-03**|**1000**|**Ingen**|**Ja**|**0**|**0**|  
|6B|1.000|20|5|01/15/03|01/20/03|16.01.03 - 20-01-03|995|Pmt.Tol.|Ja|0|5|  
|7|1.000|20|5|01/15/03|01/20/03|16.01.03 - 20-01-03|985|Kont.rab.tolerance & Bet.Tol.|Ja|20/-20|-5|  
|8|1.000|20|5|01/15/03|01/20/03|16.01.03 - 20-01-03|980|Kont.rab.tolerance|Ja|20/-20|0|  
|9|1.000|20|5|01/15/03|01/20/03|16.01.03 - 20-01-03|975|Kont.rab.tolerance & Bet.Tol.|Ja|20/-20|5|  
|10|1.000|20|5|01/15/03|01/20/03|>01/20/03|1005|Pmt.Tol.|Ja|0|-5|  
|**11**|**1,000**|**20**|**5**|**01/15/03**|**01/20/03**|**>01/20/03**|**1000**|**Ingen**|**Ja**|**0**|**0**|  
|12|1.000|20|5|01/15/03|01/20/03|>01/20/03|995|Pmt.Tol.|Ja|0|5|  
|13|1.000|20|5|01/15/03|01/20/03|>01/20/03|985|Ingen|Nr., 15 på fakturaen|0|0|  
|14|1.000|20|5|01/15/03|01/20/03|>01/20/03|980|Ingen|Nr., 20 på fakturaen|0|0|  
|15|1.000|20|5|01/15/03|01/20/03|>01/20/03|975|Ingen|Nr., 25 på fakturaen|0|0|  

### <a name="payment-range-diagrams"></a>Betalingsområdediagrammer  
I forbindelse med ovenstående scenarie er diagrammerne over betalingsintervaller som følger:  

#### <a name="1-payment-date-011503-scenarios-1-3"></a>(1) Betalingsdato <=15-01-03 (scenarie 1-3)  
Restbeløb pr.  

Normale udligningsregler  

![Regler for en enkelt betalingstolerance &#40;før 03&#47;15&#41;](media/singlePmtTolRules(Pre1503).gif "singlePmtTolRules(Pre1503)")  

(1) Hvis betaling falder i disse intervaller, kan alle udligningsposter lukkes med eller uden tolerance.  

(2) Hvis betaling falder i disse intervaller, er det ikke alle udligningsposter, der kan lukkes, selvom der anvendes tolerance.  

#### <a name="2-payment-date-is-between-011603-and-012003-scenarios-4-9"></a>(2) Betalingsdato er mellem 16.01.03 og 20.01.03 (scenarie 4-9)  
Restbeløb pr.  

Normale udligningsregler  

![Regler for en enkelt betalingstolerance & #40; respitperiode& #41;](media/singlePmtTolRules(GracePeriod).gif "singlePmtTolRules(GracePeriod)")  

(1) Hvis betaling falder i disse intervaller, kan alle udligningsposter lukkes med eller uden tolerance.  

(2) Hvis betaling falder i disse intervaller, er det ikke alle udligningsposter, der kan lukkes, selvom der anvendes tolerance.  

#### <a name="3-payment-date-is-after-012003-scenarios-10-15"></a>(3) Betalingsdato er efter 20.01.03 (scenarie 10-15)  
Restbeløb pr.  

Normale udligningsregler  

![Regler for en enkelt betalingstolerance &#40;før 01&#47;20&#41;](media/singlePmtTolRules(Post0120).gif "singlePmtTolRules(Post0120)")  

(1) Hvis betaling falder i disse intervaller, kan alle udligningsposter lukkes med eller uden tolerance.  

(2) Hvis betaling falder i disse intervaller, er det ikke alle udligningsposter, der kan lukkes, selvom der anvendes tolerance.  

## <a name="example-2---tolerance-calculations-for-multiple-documents"></a>Eksempel 2 – Toleranceberegninger for flere bilag
Nedenfor findes nogle eksempelscenarier, som viser de forventede toleranceberegninger og -bogføringer, der kan opstå i forskellige situationer. Eksemplerne er begrænset til de scenarier, der resulterer i, at alle poster i systemet kan lukkes.  

Vinduet **Regnskabsopsætning** indeholder følgende opsætning:
- Kontantrabat - respitperiode    5D  
- Maks. betalingstolerance 5  

Scenarier med alternativ A, B, C eller D repræsenterer følgende:  

- **A** – I dette tilfælde er advarslen om kontantrabattolerancen slået fra, ELLER brugeren har slået advarslen til og valgt at tillade den forsinkede kontantrabat (Bogfør som tolerance) for enhver faktura.  
- **B** – I dette tilfælde har brugeren slået advarslen til og valgt ikke at tillade den forsinkede kontantrabat for nogen faktura.  
- **C** – I dette tilfælde har brugeren slået advarslen til og valgt at tillade den forsinkede kontantrabat for den første faktura, men ikke den anden faktura.  
- **D** – I dette tilfælde har brugeren slået advarslen til og valgt ikke at tillade den forsinkede kontantrabat for den første faktura, men at tillade den for den anden faktura.  

[!div class="mx-tdBreakAll"]  

|–|Faktura|Kont.rabat|Maks. betal.tol.|Kont.rabatdato|Kont.rabattol. Dato|Betal.dato|Kont.|Tol.type|Alle poster lukket|Kont.rabattol. finans/debitor|Bet.Tol. finans|  
|-------|----------|---------------|-------------------|---------------------|--------------------------|------------------|---------|--------------------|------------------------|------------------------------|------------------------|  
|1|1.000 <br />1.000|60 <br />30|5 <br />5|01/15/03 <br />17-01-03|01/20/03 <br />22-01-03|<=15-01-03|1920|Bet.tol.|Ja|0<br /><br /> 0|-5 <br />-5|  
|**2**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**01/15/03** <br />**01/17/03**|**01/20/03** <br />**01/22/03**|**<=01/15/03**|**1910**|**Ingen**|**Ja**|**0**<br /><br /> **0**|0 <br />0|  
|3|1.000 <br />1.000|60 <br />30|5 <br />5|01/15/03 <br />17-01-03|01/20/03 <br />22-01-03|<=15-01-03|1900|Pmt.Tol.|Ja|0<br /><br /> 0|5 <br />5|  
|4B|1.000 <br />1.000|60 <br />30|5 <br />5|01/15/03 <br />17-01-03|01/20/03 <br />22-01-03|16-01-03 - 17-01-03|1980|Bet.tol.|Ja|0<br /><br /> 0|-5<br /><br /> -5|  
|**5B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**01/15/03** <br />**01/17/03**|**01/20/03** <br />**01/22/03**|**16-01-03 - 17-01-03**|**1970**|**Ingen**|**Ja**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|6B|1.000 <br />1.000|60 <br />30|5 <br />5|01/15/03 <br />17-01-03|01/20/03 <br />22-01-03|16-01-03 - 17-01-03|1960|Bet.tol.|Ja|0<br /><br /> 0|5<br /><br /> 5|  
|7A|1.000 <br />1.000|60 <br />30|5 <br />5|01/15/03 <br />17-01-03|01/20/03 <br />22-01-03|16-01-03 - 17-01-03|1920|Kont.rab.tolerance & Bet.Tol.|Ja|60/60<br /><br /> 0/0|-5 <br />-5|  
|8A|1.000 <br />1.000|60 <br />30|5 <br />5|01/15/03 <br />17-01-03|01/20/03 <br />22-01-03|16-01-03 - 17-01-03|1910|Kont.rab.tolerance|Ja|60/60<br /><br /> 0/0|0 <br />0|  
|9A|1.000 <br />1.000|60 <br />30|5 <br />5|01/15/03 <br />17-01-03|01/20/03 <br />22-01-03|16-01-03 - 17-01-03|1900|Kont.rab.tolerance & Bet.Tol.|Ja|60/60|5 <br />5|  
|10B|1.000 <br />1.000|60 <br />30|5 <br />5|01/15/03 <br />17-01-03|01/20/03 <br />22-01-03|18-01-03 - 20-01-03|2010|Bet.tol.|Ja|0<br /><br /> 0|-5<br /><br /> -5|  
|**11B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**01/15/03** <br />**01/17/03**|**01/20/03** <br />**01/22/03**|**18-01-03 - 20-01-03**|**2000**|**Ingen**|**Ja**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|12B|1.000 <br />1.000|60 <br />30|5 <br />5|01/15/03 <br />17-01-03|01/20/03 <br />22-01-03|18-01-03 - 20-01-03|1990|Bet.tol.|Ja|0<br /><br /> 0|5<br /><br /> 5|  
|13D|1.000 <br />1.000|60 <br />30|5 <br />5|01/15/03 <br />17-01-03|01/20/03 <br />22-01-03|18-01-03 - 20-01-03|1980|Kont.rab.tolerance & Bet.Tol.|Ja|0/0<br /><br /> 30/-30|-5 <br />-5|  
|14D|1.000 <br />1.000|60 <br />30|5 <br />5|01/15/03 <br />17-01-03|01/20/03 <br />22-01-03|18-01-03 - 20-01-03|1970|Kont.rab.tolerance|Ja|0/0<br /><br /> 30/-30|0 <br />0|  
|15D|1.000 <br />1.000|60 <br />30|5 <br />5|01/15/03 <br />17-01-03|01/20/03 <br />22-01-03|18-01-03 - 20-01-03|1960|Kont.rab.tolerance & Bet.Tol.|Ja|0/0<br /><br /> 30/-30|5 <br />5|  
|16D|1.000 <br />1.000|60 <br />30|5 <br />5|01/15/03 <br />17-01-03|01/20/03 <br />22-01-03|18-01-03 - 20-01-03|1950|Kont.rab.tolerance & Bet.Tol.|Ja|60/-60<br /><br /> 0/0|-5 <br />-5|  
|17D|1.000 <br />1.000|60 <br />30|5 <br />5|01/15/03 <br />17-01-03|01/20/03 <br />22-01-03|18-01-03 - 20-01-03|1940|Kont.rab.tolerance|Ja|60/-60<br /><br /> 0/0|0 <br />0|  
|18D|1.000 <br />1.000|60 <br />30|5 <br />5|01/15/03 <br />17-01-03|01/20/03 <br />22-01-03|18-01-03 - 20-01-03|1930|Kont.rab.tolerance & Bet.Tol.|Ja|60/-60<br /><br /> 0/0|5 <br />5|  
|19A|1.000 <br />1.000|60 <br />30|5 <br />5|01/15/03 <br />17-01-03|01/20/03 <br />22-01-03|18-01-03 - 20-01-03|1920|Kont.rab.tolerance & Bet.Tol.|Ja|60/-60<br /><br /> 30/-30|-5 <br />-5|  
|20A|1.000 <br />1.000|60 <br />30|5 <br />5|01/15/03 <br />17-01-03|01/20/03 <br />22-01-03|18-01-03 - 20-01-03|1910|Kont.rab.tolerance|Ja|60/-60<br /><br /> 30/-30|0 <br />0|  
|21A|1.000 <br />1.000|60 <br />30|5 <br />5|01/15/03 <br />17-01-03|01/20/03 <br />22-01-03|18-01-03 - 20-01-03|1900|Kont.rab.tolerance & Bet.Tol.|Ja|60/-60<br /><br /> 30/-30|5 <br />5|  
|22B|1.000 <br />1.000|60 <br />30|5 <br />5|01/15/03 <br />17-01-03|01/20/03 <br />22-01-03|21-01-03 - 22-01-03|2010|Bet.tol.|Ja|0<br /><br /> 0|-5<br /><br /> -5|  
|**23B**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**01/15/03** <br />**01/17/03**|**01/20/03** <br />**01/22/03**|**21-01-03 - 22-01-03**|**2000**|**Ingen**|**Ja**|**0**<br /><br /> **0**|**0**<br /><br /> **0**|  
|24B|1.000 <br />1.000|60 <br />30|5 <br />5|01/15/03 <br />17-01-03|01/20/03 <br />22-01-03|21-01-03 - 22-01-03|1990|Bet.tol.|Ja|0<br /><br /> 0|5<br /><br /> 5|  
|25A|1.000 <br />1.000|60 <br />30|5 <br />5|01/15/03 <br />17-01-03|01/20/03 <br />22-01-03|21-01-03 - 22-01-03|1980|Kont.rab.tolerance & Bet.Tol.|Ja|0/0<br /><br /> 30/30|-5 <br />-5|  
|26A|1.000 <br />1.000|60 <br />30|5 <br />5|01/15/03 <br />17-01-03|01/20/03 <br />22-01-03|21-01-03 - 22-01-03|1970|Kont.rab.tolerance|Ja|0/0<br /><br /> 30/30|0 <br />0|  
|27A|1.000 <br />1.000|60 <br />30|5 <br />5|01/15/03 <br />17-01-03|01/20/03 <br />22-01-03|21-01-03 - 22-01-03|1960|Kont.rab.tolerance & Bet.Tol.|Ja|0/0<br /><br /> 30/30|5 <br />5|  
|28|1.000 <br />1.000|60 <br />30|5 <br />5|01/15/03 <br />17-01-03|01/20/03 <br />22-01-03|>22-01-03|2010|Bet.tol.|Ja|0|-5|  
|**29**|**1,000** <br />**1,000**|**60** <br />**30**|**5** <br />**5**|**01/15/03** <br />**01/17/03**|**01/20/03** <br />**01/22/03**|**>22-01-03**|**2000**|**Ingen**|**Ja**|**0**|**0**|  
|30|1.000 <br />1.000|60 <br />30|5 <br />5|01/15/03 <br />17-01-03|01/20/03 <br />22-01-03|>22-01-03|1990|Pmt.Tol.|Ja|0|5|  

### <a name="payment-range-diagrams"></a>Betalingsområdediagrammer  
I forbindelse med ovenstående scenarie er diagrammerne over betalingsintervaller som følger:  

#### <a name="1-payment-date-011503-scenarios-1-3"></a>(1) Betalingsdato <=15-01-03 (scenarie 1-3)  
Restbeløb pr.  

Normale udligningsregler  

![Regler for flere betalingstolerancer &#40;før 03&#47;15&#41;](media/multiplePmtTolRules(Pre1503).gif "multiplePmtTolRules(Pre1503)")  

(1) Hvis betaling falder i disse intervaller, kan alle udligningsposter lukkes med eller uden tolerance.  

(2) Hvis betaling falder i disse intervaller, er det ikke alle udligningsposter, der kan lukkes, selvom der anvendes tolerance.  

#### <a name="2-payment-date-is-between-011603-and-011703-scenarios-4-9"></a>(2) Betalingsdato er mellem 16.01.03 og 17.01.03 (scenarie 4-9)  
Restbeløb pr.  

Normale udligningsregler  

![Regler for flere betalingstolerancer & #40;respitperiode& #41;](media/multiplePmtTolRules(GracePeriodInv1).gif "multiplePmtTolRules(GracePeriodInv1)")  

(1) Hvis betaling falder i disse intervaller, kan alle udligningsposter lukkes med eller uden tolerance.  

(2) Hvis betaling falder i disse intervaller, er det ikke alle udligningsposter, der kan lukkes, selvom der anvendes tolerance.  

#### <a name="3-payment-date-is-between-011803-and-012003-scenarios-10-21"></a>(3) Betalingsdato er mellem 18.01.03 og 20.01.03 (scenarie 10-21)  
Restbeløb pr.  

Normale udligningsregler  

![Regler for flere betalingstolerancer & #40; respitperiode& #41;](media/multiplePmtTolRules(GracePeriodInv1-2).gif "multiplePmtTolRules(GracePeriodInv1-2)")  

(1) Hvis betaling falder i disse intervaller, kan alle udligningsposter lukkes med eller uden tolerance.  

(2) Hvis betaling falder i disse intervaller, er det ikke alle udligningsposter, der kan lukkes, selvom der anvendes tolerance.  

#### <a name="4-payment-date-is-between-012103-and-012203-scenarios-22-27"></a>(4) Betalingsdato er mellem 21-01-03 og 22-01-03 (scenarie 22-27)  
Restbeløb pr.  

Normale udligningsregler  

![Regler for flere betalingstolerancer & #40;respitperiode& #41;](media/multiplePmtTolRules(GracePeriodInv2).gif "multiplePmtTolRules(GracePeriodInv2)")  

(1) Hvis betaling falder i disse intervaller, kan alle udligningsposter lukkes med eller uden tolerance.  

(2) Hvis betaling falder i disse intervaller, er det ikke alle udligningsposter, der kan lukkes, selvom der anvendes tolerance.  

#### <a name="5-payment-date-is-after-012203-scenarios-28-30"></a>(5) Betalingsdato er efter 22-01-03 (scenarie 28-30)  
Restbeløb pr.  

Normale udligningsregler  

![Regler for flere betalingstolerancer &#40;efter 01&#47;22&#41;](media/multiplePmtTolRules(Post0122).gif "multiplePmtTolRules(Post0122)")  

(1) Hvis betaling falder i disse intervaller, kan alle udligningsposter lukkes med eller uden tolerance.  

(2) Hvis betaling falder i disse intervaller, er det ikke alle udligningsposter, der kan lukkes, selvom der anvendes tolerance.

## <a name="see-also"></a>Se også  
[Finans](finance.md)  
[Konfigurere Finans](finance-setup-finance.md)  
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

