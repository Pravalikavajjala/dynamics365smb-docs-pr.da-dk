---
title: "Sådan aktiveres pluk efter FEFO | Microsoft Docs"
description: "Første-udløbet-først ud (FEFO) er en sorteringsmetode, der sikrer, at de ældste elementer med den tidligste udløbsdato plukkes først."
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
ms.openlocfilehash: 34d6e46146f3072da49cd28e4b4bf1b0f00d1369
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-enable-picking-items-by-fefo"></a>Fremgangsmåde: Aktivere pluk af varer efter FEFO
Første-udløbet-først ud (FEFO) er en sorteringsmetode, der sikrer, at de ældste elementer med den tidligste udløbsdato plukkes først.  

 Denne funktionalitet fungerer kun, når følgende kriterier er opfyldt:  

-   Varen skal have et serie-/lotnummer.  
-   I opsætningen af varens varesporingskode skal feltet **SN-specifik logistiksporing** eller feltet **Lotspecifik lagersporing** være markeret.  
-   Varen skal bogføres til lageret med en udløbsdato.  
-   Afkrydsningsfeltet **Kræv pluk** skal være markeret på lokationskortet.  
-   Afkrydsningsfeltet **Vælg i overensstemmelse med FEFO** skal være markeret på lokationskortet.  
-   Afkrydsningsfeltet **Tvungen placering** skal være markeret på lokationskortet.  

 Når alle kriterierne er opfyldt, sorteres serie-/lotnummererede varer, som skal plukkes, med de ældste først i alle pluk og bevægelser, undtagen for varer, der bruger SN-specifik eller lotspecifik sporing.  

> [!NOTE]  
>  Hvis nogen varer med serie-/lotnumre bruger specifik sporing, overholdes de først, og under dem vises de resterende, ikke-specifikke serienumre/lotnumre i henhold til FEFO.  

 Hvis der er to varer med serie- eller lotnumre, der har samme udløbsdato, vælges varen med det laveste serie- eller lotnummer. Hvis serie- eller lotnumrene er ens, vælges den vare, der blev registreret først.  

> [!NOTE]  
>  -   Når du plukker varer med serie- eller lotnumre på lokationer, der er sat op til styret læg-på-lager, er det kun antal på placeringer af typen *Pluk*, der plukkes i overensstemmelse med FEFO.  
> -   Hvis du vil aktivere bevægelser i henhold til FEFO, skal du enten i vinduet **Flytning (lager)** eller vinduet **Bevægelseskladde** lade feltet **Fra placering** være tomt.  
> -   Hvis feltet **Nøje bogføring af udløbsdato** er markeret, er det kun varer, der ikke er udløbet, der inkluderes i plukket. Dette gælder, selvom du ikke bruger Vælg i overensstemmelse med FEFO.  

## <a name="see-also"></a>Se også  
[Plukke varer](warehouse-pick-items.md)   
[Fremgangsmåde: Plukke varer til lagerleverance](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
[Sådan plukkes varer med Pluk fra lager](warehouse-how-to-pick-items-with-inventory-picks.md)   
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

