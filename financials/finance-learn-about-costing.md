---
title: Om lagerkostmetode | Microsoft Docs
description: "Administration af lagerkostmetoder vedrører registrering og rapportering af virksomhedens driftsomkostninger. Den omfatter rapportering af produktionsomkostninger og lageromkostninger, dvs. værdien af varer."
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
ms.openlocfilehash: 5e6b691eae1663cdc93d851f531306c472291484
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="about-inventory-costing"></a>Om lagerkostmetode
Administration af lagerkostmetoder vedrører registrering og rapportering af virksomhedens driftsomkostninger. Den omfatter rapportering af produktionsomkostninger og lageromkostninger, dvs. værdien af varer.  

 De centrale principper, der er vigtige at forstå, er, at kostmetoder definerer den måde, varer værdiansættes på, når de forlader lageret, at kostregulering opdaterer omkostningerne ved solgte varer med relaterede købsomkostninger bogført efter salget, og at lagerværdier skal bogføres til dedikerede finanskonti med regelmæssige mellemrum.  

 Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.   

|**Hvis du vil**|**Se**|  
|------------|-------------|  
|Kunne skelne mellem de fem forskellige prisberegningsmetoder og deres virkning på omkostningsforløb.|[Designoplysninger: Kostmetoder](design-details-costing-methods.md)|  
|Lære, hvordan vareudligningsposter dynamisk sammenkæder lagerafgange med tilgange for at bevare kontrollen med omkostningsforløb.|[Designoplysninger: Vareudligning](design-details-item-application.md)|  
|Lære, hvordan en vares købspris fortsat opdateres med omkostningerne ved de seneste transaktioner i overensstemmelse med prisberegningsmetoden for varen.|[Designoplysninger: Omkostningsregulering](design-details-cost-adjustment.md)|  
|Lære, hvordan gennemsnitsomkostningerne for en vare beregnes dynamisk i overensstemmelse med den valgte gennemsnitlige omkostningsperiode.|[Designoplysninger: Gennemsnitlig kostpris](design-details-average-cost.md)|  
|Kunne skelne forventede omkostninger (endnu ikke faktureret) fra faktiske omkostninger og lære, hvordan de håndteres i finansposterne.|[Designoplysninger: Bogføring af forventet kostpris](design-details-expected-cost-posting.md)|  
|Forstå omkostningsreguleringsmekanismen, som sikrer, at omkostningerne sendes videre, selvom lagertransaktioner forekommer med uregelmæssige mellemrum.|[Designoplysninger: Omkostningsregulering](design-details-cost-adjustment.md)|  
|Læse om årsagen til, at standardomkostninger ofte bruges af produktionsvirksomheder som værdigrundlag for komponenter og varer.|[Om beregning af standardomkostning](finance-about-calculating-standard-cost.md)|  
|Forstå, hvordan værdien af lageret afspejles i finansposterne.|[Rapportere omkostninger og afstemme med regnskabet](finance-report-costs-and-reconcile-with-the-general-ledger.md)|  
|Lære, hvordan varegebyrer, f.eks. for fragt og forsikring, kan føje ekstra omkostningskomponenter til en vares enhedspris.|[Fremgangsmåde: Bruge varegebyrer til at angive ekstra handelsomkostninger](payables-how-assign-item-charges.md)|  
|Læse, hvordan lagerperioder hjælper en virksomhed med at styre lagerværdi over tid, hvis der defineres kortere perioder, hvor der kan være lukket for bogføringer, efterhånden som regnskabsåret skrider frem.|[Sådan gør du: Arbejde med lagerperioder](finance-how-to-work-with-inventory-periods.md)|  
|Forstå alle mekanismerne i prisberegningsprogrammet, herunder hvad der sker, når du bogfører montage og produktionstransaktioner.|[Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md)|

## <a name="see-also"></a>Se også
[Administrere lageromkostninger](finance-manage-inventory-costs.md)    
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

