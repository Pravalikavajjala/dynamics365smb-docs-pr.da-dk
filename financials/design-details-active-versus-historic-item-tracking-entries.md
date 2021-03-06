---
title: "Designoplysninger – Aktive kontra historiske varesporingsposter | Microsoft Docs"
description: "Når dele af et dokumentlinjeantal er bogført, overføres kun det bestemte antal til vareposter og dets varesporingsnumre. Dog skal du kunne få adgang til alle relevante oplysninger om varesporing direkte fra den aktive bilagslinje. Det vil sige, at du ikke kun vil se de poster, der er relateret til det resterende antal, men du vil også have oplysninger om de enheder, der er bogført. Når du får vist eller redigerer vinduet **Varesporingslinjer**, vises det samlede indhold af tabellen **Sporingsspecifikation** (T336) og tabellen **Reservationspost** (T337) i en midlertidig version af T336. Dette sikrer, at historiske og aktive varesporingsdata kan åbnes som en."
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
ms.openlocfilehash: 0b0d49b4f9b9e77b311628c2d88b4891b32f8276
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-active-versus-historic-item-tracking-entries"></a>Designoplysninger: Aktive kontra historiske varesporingsposter
Når dele af et dokumentlinjeantal er bogført, overføres kun det bestemte antal til vareposter og dets varesporingsnumre. Dog skal du kunne få adgang til alle relevante oplysninger om varesporing direkte fra den aktive bilagslinje. Det vil sige, at du ikke kun vil se de poster, der er relateret til det resterende antal, men du vil også have oplysninger om de enheder, der er bogført. Når du får vist eller redigerer vinduet **Varesporingslinjer**, vises det samlede indhold af tabellen **Sporingsspecifikation** (T336) og tabellen **Reservationspost** (T337) i en midlertidig version af T336. Dette sikrer, at historiske og aktive varesporingsdata kan åbnes som en.  

 Følgende tabel viser, hvordan T336 og T337 bruges i forbindelse med køb. Fede tal repræsenterer værdier, som brugeren indtaster manuelt i vinduet **Varesporingslinjer**.  

 Trin 1: Opret en indkøbsordrelinje for syv stykker med varesporingsnumre.  

||**Antal (basis)**|**Mgd. at håndtere**|**Fakturer antal (basis)**|**Håndteret antal (basis)**|**Faktureret antal (basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|**T337**|7|0|0|0|0|  
|**T336**|0|0|0|0|0|  

 Trin 2: Modtag fire stykker.  

||**Antal (basis)**|**Mgd. at håndtere**|**Fakturer antal (basis)**|**Håndteret antal (basis)**|**Faktureret antal (basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Vinduet **Varesporingslinjer**|7|**4**|**0**|0|0|  
|**T337**|3|0|0|0|0|  
|**T336**|4|0|0|4|0|  

 Trin 3: Modtag to stykker, og fakturer to stykker.  

||**Antal (basis)**|**Mgd. at håndtere**|**Fakturer antal (basis)**|**Håndteret antal (basis)**|**Faktureret antal (basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Vinduet **Varesporingslinjer**|7|**2**|**2**|4|0|  
|**T337**|0|0|0|0|0|  
|**T336**|6|0|0|6|2|  

 Trin 4: Modtag ét stykke.  

||**Antal (basis)**|**Mgd. at håndtere**|**Fakturer antal (basis)**|**Håndteret antal (basis)**|**Faktureret antal (basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Vinduet **Varesporingslinjer**|7|**1**|**0**|6|2|  
|**T336**|7|0|0|7|2|  

 Fakturere 5 styk.  

||**Antal (basis)**|**Mgd. at håndtere**|**Fakturer antal (basis)**|**Håndteret antal (basis)**|**Faktureret antal (basis)**|  
|-|----------------------------------------------|--------------------------------------------|------------------------------------------------------|-------------------------------------------------------|--------------------------------------------------------|  
|Vinduet **Varesporingslinjer**|7|0|**5**|7|2|  
|**T336**|7|0|0|7|7|  

## <a name="see-also"></a>Se også  
 [Designoplysninger: Varesporing](design-details-item-tracking.md)   
 [Designoplysninger: Vinduet Varesporingslinjer](design-details-item-tracking-lines-window.md)

