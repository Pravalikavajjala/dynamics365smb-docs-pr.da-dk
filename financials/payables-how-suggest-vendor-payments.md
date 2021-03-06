---
title: "Bruge kørslen Lav kreditorbetalingsforslag | Microsoft Docs"
description: "Du kan angive kreditorbetalingsindstillinger for at få vist forslag eller forslag til betalinger, der forfalder snart, eller hvor en rabat er tilgængelig."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: eea34afbee429d14ab150894729cb4ea3843bb2b
ms.openlocfilehash: 2085cc744c2ff3761937920cd893faab5a84dada
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-suggest-vendor-payments"></a>Fremgangsmåde: Lave kreditorbetalingsforslag
I vinduet **Udbetalingskladde** kan du bruge kørslen **Lav kreditorbetalingsforslag** til at foreslå betalingslinjer. Linjer til ting som betalinger, som snart forfalder, eller betalinger, hvor en kontantrabat er tilgængelig, foreslås baseret på dine indstillinger.

For at få det fulde udbytte af foreslåede linjer skal du først prioritere dine kreditorer. Du kan finde flere oplysninger i [Fremgangsmåde: Prioritere kreditorer](purchasing-how-prioritize-vendors.md).  

Kreditorposter, der ikke er indstillet til **Afvent**, medtages ikke.  

> [!IMPORTANT]  
>   Hvis du vil have fordel af kontantrabatter og har indtastet et disponibelt beløb, bliver beløbet brugt til:  

* Prioriterede forfaldne kreditorposter først i prioriteret rækkefølge.  
* Forfaldne kreditorposter, der ikke er prioriteret.  
* Åbne kreditorposter, hvor der ydes kontantrabat, arrangeret efter kreditornummer.  

## <a name="to-use-the-suggest-vendor-payments-function"></a>Sådan bruges funktionen Lav kreditorbetalingsforslag
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Udbetalingskladder**, og vælg derefter det relaterede link.  
2. Åbn den relevante kladde, og vælg derefter handlingen **Lav kreditorbetalingsforslag**.  
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Vælg knappen **OK**.  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a>Sådan indsættes forfaldsdatoen som bogføringsdato på betalingskladdelinjer
Når du udfører kørslen **Lav kreditorbetalingsforslag** til at oprette betalingslinjer for dine kreditorer, kan du udfylde to særlige felter for at sikre, at de genererede linjer bruger forfaldsdatoen til at beregne bogføringsdatoen. Disse felter er **Beregn bogføringsdato fra forfaldsdato for udligningsbilag** og **Forskydning af forfaldsdato for udligningsbilag**.  

> [!IMPORTANT]  
>   Du kan ikke bruge feltet **Beregn bogføringsdato fra forfaldsdato for udligningsbilag** sammen med **Find kontantrabatter** eller feltet **Sammenfat pr. kreditor**. Hvis bogføringsdatoen er baseret på forfaldsdatoen, beregnes nogle kontantrabatter måske ikke korrekt, da bogføringsdatoen ligger efter kontantrabatdatoen.  

Hvis den beregnede bogføringsdato er i fortiden, bliver bogføringsdatoen desuden flyttet til arbejdsdatoen, og der vises en advarsel.  

Du kan manuelt oprette betalingslinjer ved at bruge forfaldsdatoen til at beregne bogføringsdatoen. Når du udligner kreditorposter, kan du bruge handlingen **Beregn bogføringsdato** til at opdatere bogføringsdatoen på kladdelinjen med forfaldsdatoen for den relaterede købsfaktura. Du kan finde flere oplysninger i [Fremgangsmåde: Udligne købstransaktioner manuelt](payables-how-apply-purchase-transactions-manually.md).  

> [!NOTE]  
>   Hvis købsfakturaen er overskredet, bliver bogføringsdatoen indstillet til arbejdsdatoen, og skrifttypen på linjen bliver rød.  

## <a name="see-also"></a>Se også
[Administrere skyldige beløb](payables-manage-payables.md)  
[Foretage betaling](payables-make-payments.md)  
[Arbejde med finanskladder](ui-work-general-journals.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

