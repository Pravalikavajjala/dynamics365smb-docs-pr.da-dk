---
title: "Designoplysninger – Tilgængelighed i lageret | Microsoft Docs"
description: "Systemet skal holde en konstant kontrol over varedisponering på lageret, så udgående ordrer kan flyde effektivt og levere optimale leverancer."
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
ms.openlocfilehash: 0b560d61d39ba22f0008e6cb5ef11d2f6c9aa9e0
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-availability-in-the-warehouse"></a>Designoplysninger: Tilgængelighed i lageret
Systemet skal holde en konstant kontrol over varedisponering på lageret, så udgående ordrer kan flyde effektivt og levere optimale leverancer.  

 Tilgængeligheden varierer afhængigt af allokeringer på placeringsniveauet, når lageraktiviteter som pluk og bevægelser forekommer, og når lagerreservationssystemet pålægger begrænsninger, der skal overholdes. En meget kompleks algoritme kontrollerer, at alle betingelser er opfyldt, før der tildeles antal til pluk for udgående forløb.  

## <a name="bin-content-and-reservations"></a>Placeringsindhold og reservationer  
 I en installation af logistik findes vareantal både som lagerposter, i logistikmodulet, og som vareposter i modulet Lagerbeholdning. Disse to typer indeholder forskellige oplysninger om, hvor varer findes, og om de er tilgængelige. Lagerposter definerer en vares tilgængelighed efter placering og placeringstype, samlet kaldet placeringsindhold. Vareposter definerer en varedisponering ved sin reservation til udgående dokumenter.  

 Der findes specielle funktioner i pluk-algoritme til beregning af den mængde, der er disponibel til pluk, når placeringsindholdet er kombineret med reservationer.  

## <a name="quantity-available-to-pick"></a>Mængde, der kan plukkes  
 Hvis for eksempel algoritmen for pluk ikke tager højde for vareantal, der er reserveret til en ventende salgsordreforsendelse, kan disse varer plukkes til en anden salgsordre, der er sendt tidligere, hvilket forhindrer, at det første salg er opfyldt. Hvis du vil undgå denne situation, fratrækker plukalgoritmen antal, der er reserveret til andre udgående dokumenter, antal på eksisterende plukdokumenter og antal, der er plukket, men endnu ikke leveret eller forbrugt.  

 Resultatet vises i feltet **Disp. antal til pluk** i vinduet **Plukkladde**, hvor feltet beregnes dynamisk. Værdien beregnes også, når brugere opretter lagerpluk direkte for udgående dokumenter. Disse udgående dokumenter kan være salgsordrer, produktionsforbrug eller udgående overflytninger, hvor resultatet er afspejlet i de relaterede antalsfelter, f.eks. **Mgd. at håndtere**.  

> [!NOTE]  
>  Med hensyn til prioriteten af reservationer fratrækkes antallet, der skal reserveres, fra antallet, der er disponibelt til pluk. Hvis det tilgængelige antal i plukplaceringer f.eks. er 5 enheder, men der er 100 enheder på læg-på-lager-placeringer, vises der en fejlmeddelelse, når du prøver at reservere mere end 5 enheder til en anden ordre, fordi det ekstra antal skal være tilgængeligt på plukplaceringer.  

### <a name="calculating-the-quantity-available-to-pick"></a>Beregning af det antal, der er disponibelt til pluk  
 Det antal, der kan plukkes, beregnes sådan:  

 mængde, der kan plukkes = antal i plukplaceringer - antal på pluk og bevægelser – (reserveret antal i plukplaceringer + reserveret antal på pluk og bevægelser)  

 Følgende diagram viser de forskellige elementer i beregningen.  

 ![Disponibel til pluk med reservationsoverlap](media/design_details_warehouse_management_availability_2.png "design_details_warehouse_management_availability_2")  

## <a name="quantity-available-to-reserve"></a>Antal disponible til reservation  
 Da begreberne om placeringsindhold og reservation eksisterer side om side, skal antallet af varer, der kan reserveres, justeres med fordelinger på udgående lagerdokumenter.  

 Det bør være muligt at reservere alle varer på lager, bortset fra dem, der har startet udgående behandling. Derfor defineres det antal, der kan reserveres, som antallet på alle dokumenter og alle placeringstyper, undtagen følgende udgående mængder:  

-   Antal på uregistrerede plukdokumenter  
-   Antal på forsendelsesplaceringer  
-   Antal til produktionsplaceringer  
-   Antal åbne produktionsplaceringer  
-   Antal til montageplaceringer  
-   Antal på reguleringsplaceringer  

 Resultatet vises i feltet **Beholdning i alt** i vinduet **Reservation**.  

 På en reservationslinje vises det antal, der ikke kan reserveres, fordi det er fordelt i lageret, i feltet **Allokeret antal på lager** i vinduet **Reservation**.  

### <a name="calculating-the-quantity-available-to-reserve"></a>Beregning af det antal, der er disponibelt til reservation  
 Det antal, der kan reserveres, beregnes sådan:  

 mængde, der kan reserveres = samlet antal på lager - antal på pluk og bevægelser for kildedokumenter - reserveret antal - antal i udgående placeringer  

 Følgende diagram viser de forskellige elementer i beregningen.  

 ![Disponibel til reservation pr. lagerstedsallokeringer](media/design_details_warehouse_management_availability_3.png "design_details_warehouse_management_availability_3")  

## <a name="see-also"></a>Se også  
 [Designoplysninger: Logistik](design-details-warehouse-management.md)

