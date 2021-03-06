---
title: "Sådan oprettes læg-på-lager-skabeloner | Microsoft Docs"
description: "Hvis du benytter styret læg-på-lager og pluk, foreslås den til enhver tid mest velegnede placering til varer ifølge den læg-på-lager-skabelon, du har defineret til lagerstedet, de placeringsniveauer, du har tildelt placeringerne, og de minimum- og maksimumantal, du har angivet for faste placeringer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 5a81b904a9180d7370a00f94a129ec707398e89a
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-put-away-templates"></a>Sådan oprettes læg-på-lager-skabeloner
Hvis du benytter styret læg-på-lager og pluk, foreslås den til enhver tid mest velegnede placering til varer ifølge den læg-på-lager-skabelon, du har defineret til lagerstedet, de placeringsniveauer, du har tildelt placeringerne, og de minimum- og maksimumantal, du har angivet for faste placeringer.  

Du kan oprette en række læg-på-lager-skabeloner og vælge en af som standardskabelon for læg-på-lager-aktiviteter. Du kan også vælge en bestemt skabelon til en vare eller lagervare, som der er specielle krav til i forbindelse med læg-på-lager-aktiviteter.  

## <a name="to-set-up-put-away-templates"></a>Sådan oprettes læg-på-lager-skabeloner  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Læg-på-lager-skabeloner**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Ny**.  
3.  Indtast en kode som entydig id for skabelonen.  
4.  Indtast evt. en kort beskrivelse.  
5.  Brug den første linje til at angive de krav til placeringer, som du ønsker, først og fremmest skal være overholdt, når der foreslås en læg-på-lager-aktivitet.  
6.  Brug den anden linje til at angive de sekundære krav til placeringer, som skal overholdes, når der skal findes en placering for en læg-på-lager-aktivitet. Den anden linje bruges kun, hvis en placering, der overholder kravene på den første linje, ikke kan findes.  
7.  Fortsæt med at udfylde linjerne, indtil du har beskrevet alle de acceptable placeringer, som du vil bruge til læg-på-lager-aktiviteter.  
8.  Marker afkrydsningsfeltet **Find løs placering** på den nederste linje i skabelonen.  

Du kan oprette en række læg-på-lager-skabeloner og bruge dem efter behov. Den læg-på-lager-skabelon, som du har valgt til varen eller lagervaren, hvis en sådan er oprettet, benyttes først. Hvis felterne her ikke er udfyldt, anvendes den læg-på-lager-skabelon, du har valgt til lagerstedet i oversigtspanelet **Placeringsmetode** på lokationskortet.  

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

