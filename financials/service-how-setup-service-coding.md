---
title: Definere koder for standardservices | Microsoft Docs
description: "Få at vide, hvordan du definerer koder for serviceaktiviteter, du udfører ofte."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 8a31e312fc12d75d4eb75a191b2b82bf9a6ff3c5
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---

# <a name="how-to-set-up-standard-service-codes"></a>Sådan gør du: Definere standardservicekoder
Når der foretages standardservice, skal der ofte oprettes servicedokumenter, der bruger servicelinjer, der indeholder ensartede oplysninger. For at gøre det nemmere at oprette disse linjer kan du oprette standardservicekoder, der har et foruddefineret sæt af servicelinjer. Når du vælger koden i et servicedokument, indsættes linjerne automatisk. Du kan oprette et hvilket som helst antal standardservicekoder, og hver kode kan have et ubegrænset antal servicelinjer af forskellige typer, herunder vare, ressource, pris eller tekst, tilknyttet. Du opretter servicelinjer for hver standardservicekode på kortet **Standardservicekode**. Derefter tildeler du standardservicekoder til serviceartikelgrupper på siden **Koder til standardserv.varegrupper**. Senere, når du opretter et servicedokument, du kan bruge handlingen **Hent standardservicekoder** til at tilføje servicelinjer.  
  
> [!Tip]
>  Du kan bruge den samme fremgangsmåde til at oprette linjer på salgs- og købsdokumenter. Du kan finde flere oplysninger i [Fremgangsmåde: Oprette gentagne salgs- og købslinjer](sales-how-work-standard-lines.md).    
  
## <a name="to-set-up-a-standard-service-code"></a>Sådan oprettes standardservicekoder    
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Standardservicekoder**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Udfyld de servicelinjer, der er knyttet til denne servicekode.  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a>Tildele en standardservicekode til en serviceartikelgruppe
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceartikelgrupper**, og vælg derefter det relaterede link.  
2. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Udfyld de servicelinjer, der er knyttet til denne servicekode.  

## <a name="see-also"></a>Se også
[Service](service-service.md)
