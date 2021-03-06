---
title: "Oprette en salgsordre og sælge produkter | Microsoft Docs"
description: "Beskriver, hvordan du opretter en salgsnota for at registrere en aftale med en kunde om at sælge eller handle med produkter i henhold til bestemte betingelser."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7516e79a7cd5585629bb39ac7d97a4e6ba929712
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-sell-products"></a>Fremgangsmåde: Sælge produkter
Du opretter en salgsordre eller salgsfaktura for at registrere din aftale med en kunde om at sælge bestemte produkter på bestemte leverings- og betalingsbetingelser.

> [!NOTE]  
>   Du skal bruge salgsordrer, hvis din salgsproces kræver, at du kan levere dele af et ordreantal, f.eks. fordi hele antallet ikke er tilgængeligt på én gang. Hvis du sælger varer ved at levere direkte fra leverandøren til kunden som en direkte levering, skal du også bruge salgsordrer. Du kan finde flere oplysninger i [Fremgangsmåde: Foretage direkte leveringer](sales-how-drop-shipment.md). I alle andre henseender fungerer salgsordrer på samme måde som salgsfakturaer. Du kan finde flere oplysninger under [Fremgangsmåde: Fakturere salg](sales-how-invoice-sales.md).

Du kan forhandle med kunden ved først at oprette et salgstilbud, som du kan konvertere til en salgsordre, når I har aftalt salget. Du kan finde flere oplysninger under [Fremgangsmåde: Fremsætte tilbud](sales-how-make-offers.md).

Når debitoren har bekræftet aftalen, f.eks. efter en tilbudsproces, kan du sende en ordrebekræftelse for at registrere din forpligtelse til at levere produkterne som aftalt.

Når du leverer varerne, enten helt eller delvist, kan du bogføre salgsordren som leveret eller leveret og faktureret for at oprette de relaterede vare- og debitorposter i systemet. Når du bogfører salgsordren, kan du også sende dokumentet som en vedhæftet PDF-fil i en mail. Du kan få brødteksten i mailen udfyldt med en oversigt over ordre- og betalingsoplysninger, f.eks. et link til PayPal. Du kan finde flere oplysninger under [Fremgangsmåde: Sende dokumenter via mail](ui-how-send-documents-email.md).

I de situationer, hvor debitoren skal betale, før produkterne leveres, f.eks i detailbranchen, skal du vente på betalingsmodtagelse, før du leverer produkterne. I de fleste tilfælde kan du behandle indgående betalinger nogle uger efter levering ved at udligne betalingerne på de relaterede bogførte ubetalte salgsfakturaer. Du kan finde flere oplysninger i [Fremgangsmåde: Afstemme betalinger ved hjælp af automatisk udligning](receivables-how-reconcile-payments-auto-application.md).

Du kan nemt rette eller annullere en bogført salgsfaktura, der er oprettet i forbindelse med en salgsordre, inden den betales. Dette er nyttigt, hvis du vil rette en skrivefejl, eller hvis debitoren anmoder om en ændring i ordreprocessen. Du kan finde flere oplysninger under [Fremgangsmåde: Rette eller annullere ubetalte salgsfakturaer](sales-how-correct-cancel-sales-invoice.md). Hvis den bogførte faktura betales, skal du oprette en salgskreditnota for at tilbageføre salget. Du kan finde flere oplysninger i [Fremgangsmåde: Behandle salgsreturvarer eller annulleringer](sales-how-process-sales-returns-cancellations.md).

Varerne kan være både lagervarer og tjenester, angivet af typerne **Vare - lager** og **Vare - Service** på salgslinjerne. Salgsordreprocessen er den samme for begge varetyper. Du kan finde flere oplysninger under [Fremgangsmåde: Registrere nye varer](inventory-how-register-new-items.md).

Du kan udfylde debitorfelter i salgsordren på to måder, afhængigt af om debitoren allerede er registreret. Se trin 2 og 3 i følgende procedure.

## <a name="to-create-a-sales-order"></a>Sådan oprettes en salgsordre
1. På startsiden skal du vælge handlingen **Salgsordre**.  
2. I feltet **Debitor** skal du indtaste navnet på en eksisterende debitor.

    Andre felter i vinduet **Salgsordre** er nu udfyldt med standardoplysningerne for den valgte debitor. Hvis debitoren ikke er registreret, skal du følge disse trin:
3. I feltet **Debitor** skal du indtaste navnet på den nye debitor.
4. I dialogboksen, hvor du registrerer den nye debitor, skal du trykke på knappen **Ja**.
5. I vinduet **Vælg en skabelon til en ny debitor** skal du vælge en skabelon, som det nye debitorkort skal baseres på, og derefter vælge knappen **OK**.

    Et nyt debitorkort åbnes, udfyldt med oplysninger om den valgte debitorskabelon. Feltet **Navn** udfyldes på forhånd med den nye debitors navn, som du har angivet på salgsordren.
6. Fortsæt med at udfylde resten af felterne på debitorkortet. Du kan finde flere oplysninger i [Fremgangsmåde: Registrere nye debitorer](sales-how-register-new-customers.md).  
7. Når du er færdig med debitorkortet, skal du vælge **OK** for at vende tilbage til vinduet **Salgsordre**.

    En række af felterne i salgsordren er nu udfyldt med oplysninger, der er angivet på det nye debitorkort.
8. Udfyld de resterende felter efter behov i vinduet **Salgsordre**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    Du er nu klar til at udfylde salgsordrelinjerne med lagervarer eller services, som du ønsker at sælge til debitoren.

    Hvis du har konfigureret de tilbagevendende salgslinjer for debitoren, f.eks en månedlig genbestillingsordre, kan du indsætte disse linjer i ordren ved at vælge handlingen **Hent tilbagevendende salgslinjer**.
9. I oversigtspanelet **Linjer** skal du i feltet **Vare** indsætte nummeret på en vare eller en service.  
10. Angiv det antal varer, der skal sælges, i feltet **Antal**.

    > [!NOTE]  
>   For varer af typen Service er antallet en tidsenhed, f.eks. timer, der er angivet i feltet **Enhedskode** på linjen.

    Feltet **Linjebeløb** opdateres, så det viser værdien i feltet **Enhedspris** ganget med værdien i feltet **Antal**.

    Prisen og linjebeløbene vises med eller uden moms, afhængigt af hvad du har valgt i feltet **Priser inkl. moms** på debitorkortet.
11. I feltet **Linjerabatpct.** kan du indtaste en procentdel, hvis du vil give debitoren en rabat på produktet. Værdien i feltet **Linjebeløb** opdateres tilsvarende.

    Hvis du har konfigureret specialvarepriser i oversigtspanelet **Salgspriser og salgslinjerabatter** på debitor- eller varekortet, opdateres linjerabatprocenten, prisen og beløbet på tilbudslinjen automatisk, hvis de aftalte priskriterier opfyldes. Du kan finde flere oplysninger under [Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md).
12. Hvis du vil tilføje en kommentar om den tilbudslinje, som kunden kan se på det udskrevne salgstilbud, skal du skrive en tekst i feltet **Beskrivelse** på en tom linje.  
13. Gentag trin 10 til 13 for hver vare, du ønsker at tilbyde til debitoren.

    Totalerne under linjerne beregnes automatisk, mens du opretter eller redigerer linjer.
6. Et nyt debitorkort viser oplysninger om den valgte debitorskabelon. Udfyld de resterende felter. Du kan finde flere oplysninger i [Fremgangsmåde: Registrere nye debitorer](sales-how-register-new-customers.md).  
7. Når du er færdig med debitorkortet, skal du vælge **OK** for at vende tilbage til vinduet **Salgsordre**.

   En række af felterne i salgsordren er nu udfyldt med oplysninger, der er angivet på det nye debitorkort.  
8. Udfyld de resterende felter efter behov i vinduet **Salgsordre**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

   Du er nu klar til at udfylde salgsordrelinjerne for produkter, du sælger til debitoren, eller til andre transaktioner med debitoren, som du vil registrere i en finanskonto.   

   Hvis du har konfigureret de tilbagevendende salgslinjer for debitoren, f.eks en månedlig genbestillingsordre, kan du indsætte disse linjer i ordren ved at vælge handlingen **Hent tilbagevendende salgslinjer**.  
9. I oversigtspanelet **Linjer** i feltet **Type** skal du vælge, hvilken type produkt, gebyr eller transaktion, som du vil bogføre for debitoren med salgslinjen.
10. I feltet **Nummer** skal du vælge en post, der skal bogføres i overensstemmelse med værdien i feltet **Type**.

    Lad feltet **Nummer** stå tomt i følgende tilfælde: – Hvis linjen bruges til en bemærkning. Skriv bemærkningen i feltet **Beskrivelse**.
    – Hvis der er tale om en katalogvare. Vælg handlingen **Vælg katalogvarer**. Du kan finde flere oplysninger under [Fremgangsmåde: Arbejde med katalogvarer](inventory-how-work-nonstock-items.md).

11. I feltet **Antal** skal du angive, hvor mange enheder af produktet, gebyret eller transaktion, som linjen skal registrere for debitoren.  

    > [!NOTE]  
>   Hvis varen er af typen **Vare - Service** er **Ressource**, er antallet en tidsenhed, f.eks. timer, som angivet i feltet **Enhedskode** på linjen.  

    Værdien i feltet **Linjebeløb** beregnes som *Enhedspris* x *Antal*.  

    Prisen og linjebeløbene er med eller uden moms, afhængigt af hvad du har valgt i feltet **Priser inkl. moms** på debitorkortet.  
12. Hvis du vil give en rabat, skal du angive en procentdel i feltet **Linjerabatpct.**. Værdien i feltet **Linjebeløb** opdateres tilsvarende.  

    Hvis der er konfigureret specialvarepriser i oversigtspanelet **Salgspriser og salgslinjerabatter** på debitor- eller varekortet, opdateres linjerabatprocenten, prisen og beløbet på salgslinjen automatisk, hvis priskriterierne er opfyldt. Du kan finde flere oplysninger under [Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md).  
13. Gentag trin 9 til 12 for hvert produkt eller gebyr, du ønsker at sælge til debitoren.  

    Totalerne under linjerne beregnes automatisk, mens du opretter eller redigerer linjer.  
14. I feltet **Fakturarabatbeløb** skal du indtaste et beløb, der trækkes fra den værdi, der vises i feltet **I alt inkl. moms**.

    Hvis du har konfigureret fakturarabatter til debitoren, indsættes den angivne procentværdi automatisk i feltet **Fakturarabat i %**, hvis kriterierne er opfyldt, og det relaterede beløb indsættes i feltet **Fakturarabat ekskl. moms**. Du kan finde flere oplysninger under [Registrere salgspris, rabat og betalingsaftaler](sales-how-record-sales-price-discount-payment-agreements.md).
15. Hvis du kun vil sende en del af ordreantallet, skal du angive dette antal i feltet **Lever antal**. Værdien kopieres til feltet **Fakturer antal**.
16. Hvis du kun vil fakturere en del af det leverede antal, skal du angive dette antal i feltet **Fakturer antal**. Antallet skal være mindre end værdien i feltet **Lever antal**.   
17. Når salgsordrelinjerne er fuldført, skal du vælge handlingen **Bogfør og send**.

Dialogboksen **Bekræftelse af bogfør og send** viser debitorens foretrukne metode til modtagelse af dokumenter. Du kan ændre afsendelsesmetoden ved at vælge opslagsknappen for feltet **Send bilag til**. Du kan finde flere oplysninger under [Fremgangsmåde: Konfigurerer dokumentafsendelsesprofiler](sales-how-setup-document-send-profiles.md).

De relaterede vare- og debitorposter oprettes nu i systemet, og salgsordren udlæses som et PDF-dokument. Når salgsordren er bogført fuldstændigt, fjernes den fra listen over salgsordrer og erstattes med nye dokumenter på listen over bogførte salgsfakturaer og oversigten over bogførte salgsleverancer.

## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)  
[Konfigurere salg](sales-setup-sales.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Fremgangsmåde: Sende dokumenter via mail](ui-how-send-documents-email.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
