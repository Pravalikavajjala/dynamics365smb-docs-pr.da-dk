---
title: "Konfigurere bedste fremgangsmåder: kostmetode | Microsoft Docs"
description: "**Kostmetode** på varekortet definerer, hvordan varens kostprisforløb registreres, og om en faktisk eller budgetteret værdi føres som aktiv og bruges i beregningen af kostprisen."
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
ms.openlocfilehash: d4f533d42cc813d3ebc0ccbb00228a6c8e188c14
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="setup-best-practices-costing-method"></a>Konfigurere bedste fremgangsmåder: kostmetode
**Kostmetode** på varekortet definerer, hvordan varens kostprisforløb registreres, og om en faktisk eller budgetteret værdi føres som aktiv og bruges i beregningen af kostprisen.  

 Det er vigtigt at indstille den korrekte kostmetode i overensstemmelse med varetype og forretningsmiljø for at sikre økonomiske lagerbeholdninger.  

 Den følgende tabel viser de bedste fremgangsmåder til konfiguration af feltet **Kostprisberegningsmetode**. Du kan finde flere oplysninger i [Designoplysninger: Kostmetoder](design-details-costing-methods.md).  

|Opsætningsindstilling|Bedste fremgangsmåde|Bemærkning|  
|------------------|-------------------|-------------|  
|FIFO|Bruges, hvor produktomkostninger er stabile.<br /><br /> Bruges for elementer med en begrænset hyldelevetid, fordi de ældste varer skal sælges, inden de overskrider deres sidste salgsdato.|En vares kostpris er den faktiske værdi af alle modtagelser af varen, som vælges af FIFO-reglen.<br /><br /> I lagerværdien forudsættes det, at de første varer, der lægges på lager, bliver solgt først. **Bemærk!** Når priserne stiger, viser balancen højere værdi. Dette betyder, at skatteforpligtelserne øges, men kreditvurderinger og muligheden for at låne penge forbedres.|  
|LIFO|Bruges, hvor lagerniveauer konsekvent vedligeholdes eller øges over tid.|En vares kostpris er den faktiske værdi af alle modtagelser af varen, som vælges af LIFO-reglen.<br /><br /> I lagerværdien forudsættes det, at de sidste varer, der lægges på lager, bliver solgt først. **Bemærk!** Når priserne stiger, falder værdien på resultatopgørelsen. Dette betyder, at skatteforpligtelserne reduceres, men muligheden for at låne penge forringes. **Vigtigt:** Forbudt i mange lande/områder, da det kan bruges til at holde avancen nede.|  
|Gennemsnit|Bruges, hvor produktomkostninger er ustabile.<br /><br /> Bruges, hvor lagrer stables eller blandes sammen og der ikke kan skelnes mellem dem, f.eks. kemikalier.|En vares kostpris er den præcise kostpris, som den aktuelle enhed er modtaget til.|  
|Bestemt|Bruges i produktionen eller handel med varer, der nemt kan identificeres, med forholdsvis høje kostpriser.<br /><br /> Bruges til varer, der er omfattet af regulering.<br /><br /> Bruges for varer med serienumre.|En vares kostpris beregnes som den gennemsnitlige kostpris på hvert enkelt tidspunkt efter et køb.<br /><br /> For værdiansættelse af lageret antages det, at alle lagerbeholdninger sælges samtidig.|  
|Standard|Bruges, hvor omkostningsstyring er afgørende.<br /><br /> Bruges i serieproduktion til at evaluere kostpriserne for direkte materialeomkostninger, arbejdsomkostninger og produktionsomkostninger.<br /><br /> Bruges, hvor der er disciplin og personale til at vedligeholde standarderne.|En vares kostpris forudindstilles baseret på forventninger.<br /><br /> Når det faktiske kostbeløb realiseres senere, skal standardkostprisen reguleres til de faktiske omkostninger gennem variansværdier.|  

## <a name="see-also"></a>Se også  
 [Designoplysninger: Kostmetoder](design-details-costing-methods.md)   
 [Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)   
 [Opret komplekse moduler ved hjælp af bedste praksis](set-up-complex-application-areas-using-best-practices.md)  
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

