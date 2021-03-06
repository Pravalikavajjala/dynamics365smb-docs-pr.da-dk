---
title: Lageraktiviteter | Microsoft Docs
description: "Når varer er modtaget, og før varerne afsendes, finder der en serie interne lageraktiviteter sted for at sikre et effektivt forløb gennem lagerstedet og for at organisere og vedligeholde virksomhedens lagerbeholdninger."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: c1ea1c4a5ea4b917243d60981ec35050895f82a7
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="warehouse-management"></a>Logistik
Når varer er modtaget, og før varerne afsendes, finder der en serie interne lageraktiviteter sted for at sikre et effektivt forløb gennem lagerstedet og for at organisere og vedligeholde virksomhedens lagerbeholdninger.

Blandt typiske lageraktiviteter er at lægge varer på lager, flytte varer til eller mellem lagersteder og plukke varer til montage, produktion eller afsendelse. Montageelementer til salg eller lager kan også betragtes som lageraktiviteter, men de beskrives andre steder. Du kan finde flere oplysninger i [Montagestyring](assembly-assemble-items.md).  

På store lagre kan de forskellige håndteringsopgaver opdeles efter afdelinger, og integrationen håndteres af en styret arbejdsgang. I simplere installationer er arbejdsgangen mindre formaliseret, og lageraktiviteterne udføres via de såkaldte læg-på-lager og lagerpluk. Du kan finde flere oplysninger om de grundlæggende kontra avancerede lageropsætninger i [Designoplysninger: Oversigt over logistik](design-details-warehouse-overview.md).

Før du kan udføre lageraktiviteter, skal du konfigurere systemet til den relevante lagerbehandlingskompleksitet. Der er flere oplysninger under [Konfigurere lokalitetsstyring](warehouse-setup-warehouse.md).

 Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Registrere modtagelsen af varer på lagerlokationer, enten med en købsordre, i enkle lokationsopsætninger eller med en lagermodtagelse, i tilfælde af halvt eller fuldt automatiseret lagerbehandling på lokationen.|[Sådan modtages varer](warehouse-how-receive-items.md)|
|Spring læg-på-lager- og plukprocesserne over for at fremskynde en vare direkte fra modtagelse eller produktion til levering.|[Fremgangsmåde: Afsendelse](warehouse-how-to-cross-dock-items.md)|    
|Lægge varer på lager, der er modtaget fra køb, salgsreturvarer, overflytninger eller produktionsafgange, i henhold til den konfigurerede lagerproces.|[Lægge varer på lager](warehouse-put-away-items.md)|
|Flytte varer mellem placeringer på lageret.|[Flytte varer](warehouse-move-items.md)|
|Plukke varer der skal afsendes, overflyttes eller forbruges i montage eller produktionen, i henhold til den konfigurerede lagerproces.|[Plukke varer](warehouse-pick-items.md)|
|Registrere leveringen af varer fra lagerlokationer, enten med en salgsordre, i enkle lokationsopsætninger eller med en lagerleverance, i tilfælde af halvt eller fuldt automatiserede lagerprocesser på lokationen.|[Fremgangsmåde: Sende varer](warehouse-how-ship-items.md)|  

## <a name="see-also"></a>Se også  
 [Lagerbeholdning](inventory-manage-inventory.md)  
 [Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
 [Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

