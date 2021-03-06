---
title: Udligne poster i forskellige valutaer | Microsoft Docs
description: "Du kan udligne finansposter i flere valutaer, f.eks. hvis du sælger i én valuta og modtager betaling i en anden."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 6379aea58ab7943b117e5b19b22f71193290c2cb
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-enable-application-of-ledger-entries-in-different-currencies"></a>Fremgangsmåde: Muliggøre udligning af finansposter i forskellige valutaer
Hvis du køber varer fra en leverandør i én valuta, men foretager betaling i en anden valuta, kan du udligne betalingen med købet.

Ligeledes, hvis du sælger til en debitor i en valuta og modtager betaling i en anden, kan du knytte betalingen til salgsfakturaen.

Følgende procedure beskriver, hvordan du kan angive dette for kreditorposter i vinduet **Købsopsætning**. Der er tilsvarende opsætning for debitorposter i vinduet **Salgsopsætning**.

> [!NOTE]  
>   Denne funktion kræver, at oplevelsen er indstillet til **Suite**. Du kan finde flere oplysninger under [Tilpasse din [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplevelse](ui-experiences.md).

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a>Sådan aktiveres udligning af kreditorposter i forskellige valutaer
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Købsopsætning**, og vælg derefter det relaterede link.
2. Vælg en af følgende indstillinger i feltet **Valutaudligning**.

| Indstilling | Beskrivelse |
| --- | --- |
| Ingen |Udligning mellem valutaer er ikke tilladt. |
| ØMU |Udligning mellem ØMU-valutaer er tilladt. |
| Alle |Udligning mellem alle valutaer er tilladt. |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a>Sådan opsættes finanskonti til afrundingsdifferencer ved valutaudligning  
Hvis du anvender poster i forskellige valutaer, skal du oprette finanskonti, hvor du kan bogføre afrundingsdifferencer.  
  
> [!NOTE]  
>  Du skal oprette de pågældende finanskonti, før du kan udføre opgaven. Du kan finde flere oplysninger i [Om finans- og kontoplanen](finance-general-ledger.md). 
  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Debitorbogføringsgrupper**, og vælg derefter det relaterede link.  
2. I felterne **Valutaudlign.afrnd.kto (deb.)** og **Valutaudlign.afrnd.kto (kre.)** skal du indtaste de relevante finanskonti bogføring af afrundingsdifferencer.  
3. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kreditorbogføringsgrupper**, og vælg derefter det relaterede link.  
4. I felterne **Valutaudlign.afrnd.kto (deb.)** og **Valutaudlign.afrnd.kto (kre.)** skal du indtaste de relevante finanskonti bogføring af afrundingsdifferencer.  

## <a name="see-also"></a>Se også
[Administrere skyldige beløb](payables-manage-payables.md)  
[Administrere tilgodehavender](receivables-manage-receivables.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

