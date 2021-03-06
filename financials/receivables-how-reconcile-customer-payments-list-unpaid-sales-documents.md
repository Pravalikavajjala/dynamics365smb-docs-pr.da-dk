---
title: Udligne betalinger til ubetalte salgsdokumenter | Microsoft Docs
description: "Du kan udligne beløb, der er betalt af debitorer, til relaterede salgsdokumenter og bogføre betalingen for at opdatere debitor-, finans- og bankposter."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipts, customer payment
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 94055c34b67f05faa8955fdff28f854e77d9664f
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-reconcile-customer-payments-manually-from-a-list-of-unpaid-sales-documents"></a>Fremgangsmåde: Afstemme debitorbetalinger manuelt på en liste over ubetalte salgsdokumenter
Når debitorerne har foretaget betalinger til din elektroniske bankkonto, skal du udligne hvert indbetalte beløb med det relaterede salgsbilag og derefter bogføre betalingen for at opdatere posterne for debitor, finans og bankkonto.

> [!NOTE]  
>   Du kan udføre de samme opgaver, herunder kreditorbetalinger, i vinduet **Betalingsudligningskladde** ved hjælp af funktioner til import af bankkontoudtog, automatisk udligning og bankkontoudligning. Du kan finde flere oplysninger i [Afstemme betalinger ved hjælp af automatisk udligning](receivables-how-reconcile-payments-auto-application.md).

Vinduet **Betalingsregistrering** er beregnet til at understøtte dig i opgaver, der involverer afstemning af interne konti ved at bruge faktiske tal til at sikre, at betalinger opkræves effektivt fra debitorer. Dette værktøj til betalingsbehandling gør det muligt hurtigt at kontrollere og bogføre individuelle betalinger eller engangsbetalinger, behandle fratrukne betalinger og finde ubetalte bilag, hvortil der udføres betaling.

Betalinger til forskellige debitorer, som har forskellige betalingsdatoer, skal bogføres som individuelle betalinger. Betalinger til den samme debitor, som har den samme betalingsdato, kan bogføres som en engangsbetaling. Dette er nyttigt, når en debitor f.eks. har foretaget en enkelt betaling, der dækker flere salgsfakturaer.

## <a name="to-set-up-the-payment-registration-journal"></a>Sådan konfigurerer du betalingsregistreringskladden
Fordi du kan bogføre forskellige typer betaling til forskellige modkonti, skal du vælge en modkonto i vinduet **Opsætning af betalingsregistrering**, før du starte behandlingen af debitorbetalinger. Hvis du altid bogfører på den samme modkonto, kan du angive den pågældende konto som standard og undgå dette trin, hver gang du åbner vinduet **Betalingsregistrering**.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opsætning af betalingsregistrering**, vælg og derefter det relaterede link.

    Du kan også vælge handlingen **Godkendere** i vinduet **Betalingsregistrering**.    
2. Udfyld felterne i vinduet **Opsætning af betalingsregistrering**. Vælg et felt for at læse en kort beskrivelse af det eller et link til relaterede oplysninger.  

## <a name="to-reconcile-payments-individually"></a>Sådan afstemmes betalinger manuelt
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Betalingsregistrering**, vælg og derefter det relaterede link.  
2. Marker afkrydsningsfeltet **Betaling foretaget** på den linje, der repræsenterer det bogførte bilag, hvortil der er foretaget en betaling.

    Hvis afkrydsningsfeltet **Udfyld Dato for modtaget automatisk** er markeret i vinduet **Opsætning af betalingsregistrering**, er arbejdsdatoen angivet i feltet **Dato for modtaget**.  
3. I feltet **Dato for modtaget** kan du indtaste den dato, hvor betalingen blev foretaget. Denne dato kan adskille sig fra arbejdsdatoen.  
4. I feltet **Beløb modtaget** skal du indtaste det beløb, der er betalt.

    Ved fuld betaling er dette det samme som beløbet i feltet **Restbeløb** på linjen. Ved delvise betalinger er dette lavere end beløbet i feltet **Restbeløb** på linjen.    
5. Gentag trin 2-4 for andre linjer, der repræsenterer bogførte bilag, hvortil der er foretaget betalinger.  
6. Vælg handlingen **Bogfør betalinger**.  

De angivne betalingsoplysninger bogføres for bilag, der repræsenteres af linjer, hvor afkrydsningsfeltet **Betaling foretaget** er markeret.  

Betalingsposter bogføres til finans, bank og debitorkonti. Hver betaling anvendes på det relevante bogførte salgsdokument.  

## <a name="to-reconcile-lump-payments"></a>Sådan afstemmer du engangsbetalinger
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Betalingsregistrering**, vælg og derefter det relaterede link.
2. Marker afkrydsningsfeltet **Betaling foretaget** på de linjer, der repræsenterer de bogførte bilag til den samme debitor, som engangsbeløbet blev betalt til.  

    > [!NOTE]  
>   Debitoren i feltet **Navn** skal være den samme i alle linjer, der skal bogføres som engangsbetaling.  

    Hvis afkrydsningsfeltet **Udfyld Dato for modtaget automatisk** er markeret i vinduet **Opsætning af betalingsregistrering**, er arbejdsdatoen angivet i feltet **Dato for modtaget**.  
3. I feltet **Dato for modtaget** kan du indtaste den dato, hvor betalingen blev foretaget. Denne dato kan adskille sig fra arbejdsdatoen.  

    > [!NOTE]  
>   Denne dato skal være ens på alle linjer, der skal bogføres som engangsbetaling.  
4. I feltet **Beløb modtaget** kan du indtaste beløb på flere linjer, der i alt er lig med engangsbetalingsbeløbet.  

    > [!TIP]  
>   Prøv at bogføre så mange fulde betalinger som muligt med engangsbeløbet. Indtast beløb, der er det samme som beløbet i feltet **Restbeløb** på så mange linjer som muligt.  
5. Gentag trin 2-4 for andre linjer, der repræsenterer bogførte dokumenter for den samme debitor, hvortil der er foretaget en engangsbetaling.  
6. Vælg handlingen **Bogfør som engangsbetaling**. De angivne betalingsoplysninger bogføres for bilag, der repræsenteres af linjer, hvor afkrydsningsfeltet **Betaling foretaget** er markeret.  

Betalingsposter bogføres til finans, bank og debitorkonti. Hver betaling anvendes på det relevante bogførte salgsdokument.  

Hvis en betaling i banken ikke repræsenteres af nogen bilag i vinduet **Betalingsregistrering**, kan det skyldes, at det relaterede bilag endnu ikke er bogført. I dette tilfælde kan du bruge en søgefunktion til hurtigt at finde bilaget og bogføre det for at behandle betalingen. Du kan finde flere oplysninger i afsnittet "Sådan finder du et bestemt salgsdokument, der ikke er fuldt faktureret".  

Hvis en betaling i banken ikke repræsenteres af nogen bilag i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du åbne en finanskladdelinje, som er udfyldt på forhånd, i vinduet **Betalingsregistrering** for at bogføre betalingen direkte på modkontoen uden at knytte betalingen til et bilag. Du kan også registrere betalingen i kladden, indtil den betalingens oprindelse er løst. Du kan finde flere oplysninger i afsnittet "Sådan registrerer eller bogfører du en betaling uden et relateret dokument".  

## <a name="to-process-customer-payments-with-discounts-manually"></a>Sådan behandler du debitorbetalinger med rabatter manuelt
Hvis du har aftalt en kontantrabat med debitoren, kan de indbetalte beløb være mindre end fakturabeløbene, hvis betalingen finder sted inden den aftalte rabatdato.  

I følgende fremgangsmåder beskrives fire forskellige måder til at bogføre fratrukne betalinger i vinduet **Betalingsregistrering**.  

* Det indbetalte beløb er lig med det resterende beløb, og betalingsdatoen ligger før rabatdatoen. Du bogfører betalingen, som den er.  
* Det indbetalte beløb er lig med det resterende fratrukne beløb, men betalingsdatoen ligger efter rabatdatoen. Du bogfører betalingen delvis. Bilaget forbliver åbent, så restbeløbet kan opkræves/betales. Du kan også angive rabatdatoen til at tillade fuld betaling.  
* Betalingsbeløbet er lavere end det resterende fratrukne beløb. Du bogfører betalingen delvis. Bilaget forbliver åbent, så restbeløbet kan opkræves/betales.  
* Betalingsbeløbet er højere end det resterende fratrukne beløb. Du bogfører betalingerne, som de er. Kun det resterende beløb bogføres. Det ekstra beløb krediteres til debitoren.  

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-and-where-the-payment-date-is-before-the-discount-date"></a>Sådan behandler du et betalingsbeløb, der er lig med det fratrukne beløb, og hvor betalingsdatoen ligger før rabatdatoen
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Betalingsregistrering**, vælg og derefter det relaterede link.  
2. Angiv betalingsbeløbet i feltet **Beløb modtaget**. Beløbet er lig med beløbet i feltet **Rest. bel. efter rabat**.

    Afkrydsningsfeltet **Betaling foretaget** markeres automatisk, og feltet **Dato for modtaget** udfyldes med arbejdsdatoen.    
3. Angiv betalingsdatoen i feltet **Dato for modtaget**. Datoen er inden datoen i feltet **Kont.rabatdato**.
4. Kontrollér, at feltet **Restbeløb** indeholder et nul (0).  
5. Vælg handlingen **Bogfør betalinger** for at bogføre hele betalingen til finans-, bank- og debitorkonti.

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-but-where-the-payment-date-is-after-the-discount-date"></a>Sådan behandler du et betalingsbeløb, der er lig med det fratrukne beløb, men hvor betalingsdatoen ligger efter rabatdatoen
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Betalingsregistrering**, vælg og derefter det relaterede link.  
2. Angiv betalingsbeløbet i feltet **Beløb modtaget**. Beløbet er lig med beløbet i feltet **Rest. bel. efter rabat**.

    Afkrydsningsfeltet **Betaling foretaget** markeres automatisk, og feltet **Dato for modtaget** udfyldes med arbejdsdatoen.
3. I feltet **Dato for modtaget** kan du indtaste en betalingsdato, som ligger efter datoen i feltet **Kont.rabatdato**. Datofelter ændres til rød skrift, og en fejlmeddelelse vises nederst i vinduet.

    > [!TIP]  
>   Hvis du vil gøre en undtagelse og tildele rabatten, selvom betalingen falder for sent, skal du følge disse trin:
4. Vælg handlingen **Detaljer**.  
5. I vinduet **Oplysninger om betalingsregistrering** i feltet **Kont.rabatdato** i oversigtspanelet **Kontantrabat** skal du indtaste en dato, der ligger efter datoen i feltet **Dato for modtaget** i vinduet **Betalingsregistrering**.  

    Fejlmeddelelsen og den røde skrift forsvinder, og du kan fortsætte med at behandle den fratrukne betaling.    
6. Kontrollér, at feltet **Restbeløb** indeholder det beløb, der resterer, før det fulde fakturabeløb er betalt.  
7. Vælg handlingen **Bogfør betalinger** for at bogføre delbetalingen til finans-, bank- og debitorkonti.  

Det relaterede bilag forbliver åbent.

### <a name="to-process-a-payment-that-is-lower-than-the-remaining-discounted-amount"></a>Sådan behandler du en betaling, der er lavere end det resterende fratrukne beløb
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Betalingsregistrering**, vælg og derefter det relaterede link.  
2. Angiv betalingsbeløbet i feltet **Beløb modtaget**. Beløbet er lavere end beløbet i feltet **Rest. bel. efter rabat**.

    Afkrydsningsfeltet **Betaling foretaget** markeres automatisk, og feltet **Dato for modtaget** udfyldes med arbejdsdatoen.  
3. Angiv betalingsdatoen i feltet **Dato for modtaget**. Datoen er inden datoen i feltet **Kont.rabatdato**.
4. Kontrollér, at feltet **Restbeløb** indeholder det beløb, der resterer, før rabatbeløbet er betalt.  
5. Vælg handlingen **Bogfør betalinger** for at bogføre delbetalingen til finans-, bank- og debitorkonti.  

Det relaterede bilag forbliver åbent.

### <a name="to-process-a-payment-that-is-more-than-the-remaining-discounted-amount"></a>Sådan behandler du en betaling, der er højere end det resterende fratrukne beløb
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Betalingsregistrering**, vælg og derefter det relaterede link.  
2. Angiv betalingsbeløbet i feltet **Beløb modtaget**. Beløbet er højere end beløbet i feltet **Rest. bel. efter rabat**.  

    Afkrydsningsfeltet **Betaling foretaget** markeres automatisk, og feltet **Dato for modtaget** udfyldes med arbejdsdatoen.    
3. Angiv betalingsdatoen i feltet **Dato for modtaget**. Datoen er inden datoen i feltet **Kont.rabatdato**.
4. Kontrollér, at feltet **Restbeløb** indeholder et nul (0).  
5. Vælg handlingen **Bogfør betalinger** for at bogføre hele betalingen til finans-, bank- og debitorkonti.  

Det relaterede bilag er lukket, og debitoren krediteres det overskydende betalingsbeløb.  

## <a name="to-find-a-specific-sales-document-that-is-not-fully-invoiced"></a>Sådan finder du et bestemt salgsdokument, der ikke er fuldt faktureret
Vinduet **Betalingsregistrering** understøtter dig i opgaver, der er nødvendige for at afstemme interne konti med aktuelle tal for at sikre effektiv indsamling fra debitorer. Den viser udestående indgående betalinger som linjer, der repræsenterer salgsdokumenter, hvor et beløb er forfaldent til betaling.  

Typisk når en betaling er foretaget, registreret i bankbogføringsgrupperne eller lignende, repræsenteres det relaterede, salgs- eller købsdokument som en linje i vinduet **Betalingsregistrering**, fordi det pågældende dokument afventer, at betalingen bogføres i forhold til det udestående beløb. Ind imellem er der dog en udført betaling, som ikke repræsenteres af en linje i vinduet **Betalingsregistrering**, typisk fordi det pågældende bilag ikke er helt fakturabogført.

I vinduet **Dokumentsøgning** kan du søge efter bilag, der ikke er fuldstændig faktureret. Du kan søge baseret på et eller flere af følgende kriterier:  

* Bilagsnr.  
* Beløb eller beløbområde  

Den følgende procedure beskriver, hvordan du finder et bestemt dokument ved at bruge begge søgekriterier.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Betalingsregistrering**, vælg og derefter det relaterede link.
2. Placer markøren på en linje, og vælg handlingen **Søg i dokumenter**.
3. I vinduet **Dokumentsøgning** skal du indtaste en værdi i feltet **Dokumentnr.**.  

    > [!NOTE]  
>   Den værdi, du indtaster i dette felt, er omsluttet af skjulte jokertegn. Dette betyder, at funktionen søger efter alle dokumentnumre, der indeholder den angivne værdi.    
4. I feltet **Beløb** skal du indtaste det specifikke beløb på det bilag, du ønsker at finde.  
5. I feltet **Tolerancebeløb %** skal du angive en procentværdi for at angive det beløbsinterval, som du vil søge i, for at finde det åbne bilag.  

    Hvis du angiver 10, vil funktionen søge efter beløb i et interval mellem ti procent lavere og ti procent højere end værdien i feltet **Beløb**.    
6. Vælg handlingen **Søg**.  

Søgefunktionen søger mellem bilag, der ikke er faktureret fuldstændigt, baseret på angivne kriterier.  

Hvis et eller flere bilag matcher kriterierne, åbnes vinduet **Resultat af dokumentsøgning** for at vise linjer, der repræsenterer disse bilag. Hver linje indeholder et bilagsnummer, en beskrivelse og et beløb, så du nemt kan finde et bestemt bilag, f.eks. baseret på oplysninger om dine bankkontoudtog.  

Hvis en betaling i banken ikke repræsenteres af nogen bilag i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du åbne en finanskladdelinje, som er udfyldt på forhånd, i vinduet **Betalingsregistrering** for at bogføre betalingen direkte på modkontoen uden at knytte betalingen til et bilag. Du kan også registrere betalingen i kladden, indtil den betalingens oprindelse er løst.  

## <a name="to-record-or-post-a-payment-without-a-related-document"></a>Sådan registrerer eller bogfører du en betaling uden et relateret dokument
Hvis en betaling i banken ikke repræsenteres af nogen bilag i [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du åbne en finanskladdelinje, som er udfyldt på forhånd, i vinduet **Betalingsregistrering** for at bogføre betalingen direkte på modkontoen uden at knytte betalingen til et bilag. Du kan også registrere betalingen i kladden, indtil den betalingens oprindelse er afklaret.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Betalingsregistrering**, vælg og derefter det relaterede link.  

Fortsæt ved at registrere en udokumenteret betaling.  

1. Vælg handlingen **Finanskladde**.  

    Vinduet **Finanskladde** åbnes med en linje med, der er udfyldt på forhånd med modkontoen for den kladde, der er konfigureret i vinduet **Opsætning af betalingsregistrering**.  
2. Udfyld resten af felterne på finanskladdelinjen, f.eks. beløbet og debitornummeret eller andre oplysninger fra bankens kontoudtog. Du kan finde flere oplysninger i [Fremgangsmåde: Bogføre transaktioner direkte i finansregnskabet](finance-how-post-transactions-directly.md).  

Du kan bogføre kladdelinjen for at opdatere det samlede beløb på modkontoen. Du kan også lade kladdelinjen ikke-bogført og måske knytte den til en note, om at betalingen skal bruge flere analyser.  

Hvis du efterlader kladdelinjen uden at bogføre den, vil den tilføre værdi til feltet **Ikke-bogført saldo** nederst i vinduet **Betalingsregistrering**.  

## <a name="see-also"></a>Se også
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

