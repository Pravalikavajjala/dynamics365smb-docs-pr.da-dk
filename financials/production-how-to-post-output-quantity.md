---
title: "Sådan massebogføres produktionsafgang og operationstid | Microsoft Docs"
description: "Afgangsantallet angiver arbejdsforløbet i form af det færdige antal."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: ee5ee5d08804439a79f8029eaa25ab7547349a1b
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-batch-post-output-and-run-times"></a>Fremgangsmåde: Massebogføre afgang og operationstider
Afgangsantallet angiver arbejdsforløbet i form af det færdige antal.  

> [!NOTE]
> Lageret opdateres kun automatisk, når du bogfører afgangsantal i den sidste operation.  

## <a name="to-post-output-quantities-for-one-or-more-production-order-lines"></a>Sådan bogføres afgangsantal for en eller flere produktionsordrelinjer
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Afgangskladde**, og vælg derefter det relaterede link.  
2. Udfyld felterne med produktionsordredataene og afgangsdataene. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Hvis operationen er afsluttet, skal du markere feltet **Afsluttet**.  

    Hvis den lagerlokation, hvor varerne skal lægges på lager, bruger placeringer, men ikke kræver læg-på-lager, skal du  tildele en placeringskode til kladdelinjen for at angive, hvor varerne skal lægges på lageret. Du kan finde flere oplysninger i [Fremgangsmåde: Lægge produktions- eller montageafgange på lager](warehouse-how-to-put-away-production-output.md).  

4. Vælg handlingen **Bogfør** for at bogføre operationerne. Afgangsantallet bogføres. Varen er nu klar til afsendelse.  

## <a name="to-post-run-times-for-one-or-more-production-order-lines"></a>Sådan bogføres operationstider for en eller flere produktionsordrelinjer
Operationstiden angiver arbejdsforløbet i form af den nødvendige arbejdstid.    

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Afgangskladde**, og vælg derefter det relaterede link.  
2. Udfyld felterne med produktionsordredataene og afgangsdataene.  
3.  Hvis operationen er afsluttet, skal du vælge feltet **Afsluttet**.  
4. Vælg handlingen **Bogfør** for at bogføre den tid, der bruges pr. operation. Kapacitetsposter opdateres for de anvendte arbejdscentre eller produktionsressourcer.

## <a name="see-also"></a>Se også  
[Produktion](production-manage-manufacturing.md)    
[Konfigurere produktion](production-configure-production-processes.md)  
[Planlægning](production-planning.md)      
[Lagerbeholdning](inventory-manage-inventory.md)  
[Køb](purchasing-manage-purchasing.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

