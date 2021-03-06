---
title: "Oprette og bruge standardlinjer til tilbagevendende salg og køb | Microsoft Docs"
description: "Du kan oprette salgslinjer og købslinjer, som du ofte bruger, og derefter indsætte dem i salgs- og købsdokumenter, som du kan hurtigt udfylde linjerne med standardoplysninger."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, replenishment
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 8b2e20e694279a8c06188e0e429ef3b4fb43aea2
ms.openlocfilehash: 6f7202da4290ae3f6093baed4185649c30d6a199
ms.contentlocale: da-dk
ms.lasthandoff: 09/27/2017

---
# <a name="how-to-create-recurring-sales-and-purchase-lines"></a>Fremgangsmåde: Oprette gentagne salgs- og købslinjer
Hvis du ofte har brug at oprette salgs- og købslinjer med næsten ens oplysninger, kan du oprette standardlinjer, som du derefter kan indsætte i tilbagevendende salgs- og købsdokumenter, f.eks. for tilbagevendende genbestillingsordrer.  

Følgende procedure viser, hvordan du arbejder med standardsalgslinjer. Det fungerer på samme måde for standardkøbslinjer.  

## <a name="to-set-up-standard-sales-lines"></a>Sådan opretter du standardsalgslinjer  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Standardsalgskoder**, og vælg derefter det relaterede link.  
2. Vælg handlingen **Ny** i vinduet **Standardsalgslinjer**.  
3. Udfyld felterne efter behov i oversigtspanelet **Generelt**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. I oversigtspanelet **Linjer** skal du angive oplysninger i felterne for at forberede salgslinjer, der afspejler de standardlinjer, du forventer at bruge som tilbagevendende linjerne på salgsdokumenter.  

## <a name="to-insert-standard-sales-lines-on-a-sales-invoice"></a>Sådan indsættes standardsalgslinjer i en salgsfaktura
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Fakturaer**, og vælg derefter det relaterede link.
2. Åbn den salgsfaktura, som du vil indsætte en eller flere standardsalgslinjer i.
3. Vælg handlingen **Hent tilbagevendende salgslinjer**.
4. I vinduet **Tilbagevendende salgslinjer** skal du vælge på opslagsknappen i feltet **Kode** og derefter vælge en række standardsalgslinjer.
5. Vælg knappen **OK** for at indsætte standardsalgslinjerne på fakturaen, hvor du kan genbruge eller redigere oplysningerne.

## <a name="to-create-multiple-sales-invoices-based-on-standard-sales-lines"></a>Sådan opretter du flere salgsfakturaer baseret på standardsalgslinjer
Du kan bruge kørslen **Opret tilbagevendende salgsfaktura** til at oprette salgsfakturaer i overensstemmelse med standardsalgslinjer, som er knyttet til kunderne og med bogføringsdatoer inden for de gyldige fra- og til-datoer, som du angiver i standardsalgskoden.

I vinduet **Tilbagevendende salgslinjer** kan du også angive en Direct Debit-betalingsform og Direct Debit-betalingsaftale. Salgsfakturaer, der er oprettet med kørslen **Opret tilbagevendende salgsfaktura**, vil derefter indeholde oplysninger, der skal bruges til at opkræve betaling for salgsfakturaer med SEPA-Direct Debit. Du kan finde flere oplysninger i [Indhente betalinger med SEPA Direct Debit](finance-collect-payments-with-sepa-direct-debit.md).

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opret tilbagevendende salgsfakturaer**, og vælg derefter det relaterede link.
2. Udfyld felterne efter behov i vinduet **Opret tilbagevendende salgsfaktura**.
3. I feltet **Kode** skal du angive den kode for standardsalgslinjer, der er knyttet til en debitor, som du vil oprette salgsfakturaer for.
4. Vælg knappen **OK**.

Salgsfakturaer oprettes for kunder med den angivne standarddebitorsalgskode og eventuelle angivne oplysninger om direkte debitering for bogføring på den angivne dato.

## <a name="see-also"></a>Se også  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

