---
title: "Sådan udskrives en rapport til afstemning af moms | Microsoft Docs"
description: "I [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kan du bruge rapporten **Momsafstemning** til at få vist en oversigt over finanskonti med deres grundlæggende beløb og momsbeløb. Disse beløb er grupperet efter moms-type for at hjælpe med afstemningen for afregning af moms."
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
ms.openlocfilehash: 97025baf2fedd739ecf671766aacdebb482ef000
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-print-vat-reconciliation-reports"></a>Fremgangsmåde: Udskrive en rapport til afstemning af moms
I [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kan du bruge rapporten **Momsafstemning** til at få vist en oversigt over finanskonti med deres grundlæggende beløb og momsbeløb. Disse beløb er grupperet efter moms-type for at hjælpe med afstemningen for afregning af moms.  

### <a name="to-print-a-vat-reconciliation-report"></a>Sådan udskrives en momsafstemningsrapport  

1.  Vælg ikonet ![Søg efter side eller rapport](../../media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Momsafstemning**, og vælg derefter det relaterede link.  
2.  I oversigtspanelet **Indstillinger** skal du udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**Vis detaljer**|Vælg for at udskrive alle transaktionsbeløb i rapporten.<br /><br /> Hvis du ikke markerer feltet, udskrives en enkelt akkumuleret linje for hver finanskonto.|  
    |**Vis transaktioner uden moms**|Vælg for at udskrive en linje for hver finanskonto, som transaktioner bogføres på. Du kan bruge denne indstilling for både enkelte konti og flere konti.<br /><br /> Standardværdien er **Nej**. Rapporten indeholder kun de transaktioner, der omfatter momsposter. Hvis du markerer dette felt, medtager rapporten alle posteringer.|  

3.  I oversigtspanelet **Finanspost** skal du vælge de relevante filtre.  
4.  Vælg **Udskriv** for at udskrive rapporten, eller vælg **Vis udskrift** for at se den på skærmen.  

## <a name="see-also"></a>Se også  
 [Lokal funktionalitet for Danmark](denmark-local-functionality.md)  

