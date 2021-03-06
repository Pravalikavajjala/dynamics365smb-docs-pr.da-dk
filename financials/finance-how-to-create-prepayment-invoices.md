---
title: "Sådan opretter du forudbetalingsfakturaer | Microsoft Docs"
description: "Få at vide, hvordan du håndterer situationer, hvor du eller din leverandør kræver forudbetaling."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 04d7703df0c1b5e4da8996f00b5f1eed293cbf56
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-prepayment-invoices"></a>Sådan oprettes forudbetalingsfakturarer
Hvis det er et krav, at dine kunder skal betale, før du leverer en ordre til dem, eller hvis din leverandør kræver, at du skal betale, før de sender en ordre til dig, kan du bruge forudbetalinger.  

Når du har oprettet en salgs- eller købsordre, kan du oprette en forudbetalingsfaktura. Du kan bruge standardprocenterne til hver enkelt salgs- eller købslinje, eller du kan regulere beløbet efter behov. Du kan f.eks. angive et samlet beløb til hele ordren.  

Følgende procedure beskriver, hvordan du fakturerer en forudbetaling for en salgsordre. Fremgangsmåden er den samme for købsordrer.  

## <a name="to-create-a-prepayment-invoice"></a>Sådan oprettes en forudbetalingsfaktura  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsordrer**, og vælg derefter det relaterede link.  
2. Opret en ny salgsordre. Du kan finde flere oplysninger i [Fremgangsmåde: Sælge produkter](sales-how-sell-products.md).  

    I oversigtspanelet **Forudbetaling**, udfyldes feltet **Forudbetaling i %** automatisk, hvis der er angivet en standardforudbetalingsprocent på debitorkortet. Du kan ændre indholdet i feltet. Forudbetalingsprocenten kopieres kun fra hovedet til de linjer, hvor standardforudbetalingsprocenten ikke kopieres fra varen.  

    Hvis afkrydsningsfeltet **Komprimer forudbetaling** er markeret, samles linjerne på fakturaen, hvis:  
    - De har samme finanskonto til forudbetalinger, som angivet i bogføringsopsætning.  
    - De har samme dimensioner.  

    Lad feltet være tomt, hvis du vil angive en forudbetalingsfaktura med én linje for hver salgsordre, der har en forudbetalingsprocent.  

3. Udfyld salgslinjerne.  

    Hvis der er oprettet standardforudbetalingsprocenter til dine varer, kopieres de automatisk til feltet **Forudbetaling i %** på linjen. Ellers kopieres forudbetalingsprocenten fra hovedet. Du kan ændre indholdet i feltet **Forudbetaling i %** på linjen.  
4. Hvis du vil bruge én forudbetalingsprocent til hele ordren, skal du ændre feltet **Forudbetaling i %** i hovedet, efter at du har udfyldt linjerne.  
5. Du kan se det samlede forudbetalingsbeløb ved at vælge handlingen **Statistik**.

    Hvis du vil regulere det samlede forudbetalingsbeløb for ordren, kan du ændre indholdet i feltet **Forudbetalingsbeløb** i vinduet **Salgsordrestatistik**.  

    Hvis feltet **Priser inkl. moms** er markeret, kan feltet **Forudbetalingsbeløb Inkl. moms** redigeres.  

    Hvis du ændrer indholdet i feltet **Forudbetalingsbeløb**, fordeles beløbet proportionalt mellem alle linjerne bortset fra dem, hvor der står **0** i feltet **Forudbetaling i %**.  
6. For at udskrive en kontrolrapport, inden du bogfører forudbetalingsfakturaen, skal du vælge handlingen **Forudbetaling** og derefter vælge **Forudbetalingstestrapport**.  
7. For at bogføre forudbetalingsfakturaen skal du vælge handlingen **Forudbetaling** og derefter vælge handlingen **Bogfør forudbetalingsfaktura**.  

    Hvis du både vil bogføre og udskrive forudbetalingsfakturaen, skal du vælge handlingen **Bogfør og udskriv forudbetalingsfaktura**.  

Du kan udstede flere forudbetalingsfakturaer til ordren. I så fald skal du øge forudbetalingsbeløbet på en eller flere linjer, justere dokumentdatoen, hvis det er nødvendigt, og bogføre forudbetalingsfakturaen. Der oprettes en ny faktura, som dækker differencen mellem de forudbetalte beløb, der er faktureret indtil videre, og det nye forudbetalingsbeløb.  

> [!NOTE]  
>  Hvis du befinder dig i USA, kan du ikke ændre forudbetalingsprocenten, når forudbetalingsfakturaen er blevet bogført. Dette forhindres i den amerikanske version af [!INCLUDE[d365fin](includes/d365fin_md.md)], fordi beregningen af moms ellers ville være forkert.  

 Når du er klar til at bogføre resten af fakturaen, skal du benytte samme fremgangsmåde som med alle andre fakturaer, hvorefter det forudbetalte beløb automatisk trækkes fra det forfaldne beløb.  

## <a name="see-also"></a>Se også  
[Fakturere forudbetalinger](finance-invoice-prepayments.md)  
[Gennemgang: Opsætning og fakturering af salgsforudbetalinger](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Finans](finance.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

