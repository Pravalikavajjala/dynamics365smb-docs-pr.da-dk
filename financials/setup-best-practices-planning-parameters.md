---
title: "Konfigurere bedste fremgangsmåder: Planlægningsparametre | Microsoft Docs"
description: "Oversigtspanelet **Planlægning** på varekortet er midtpunktet i en virksomheds forsyningskæde. Det er meget vigtigt at angive de korrekte planlægningsparametre til omkostningseffektiv lagerstyring og høj kundeservice."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: a9dfb17b0cbddb3d6b65e8d807dd92990c2ccdc1
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="setup-best-practices-planning-parameters"></a>Oprette bedste fremgangsmåder: Planlægningsparametre
Oversigtspanelet **Planlægning** på varekortet er midtpunktet i en virksomheds forsyningskæde. Det er meget vigtigt at angive de korrekte planlægningsparametre til omkostningseffektiv lagerstyring og høj kundeservice.  

 Følgende tabel viser de bedste fremgangsmåder til konfiguration af udvalgte globale felter med planlægningsparametre. Du kan få yderligere oplysninger om et felt ved at vælge linket i kolonnen **Opsætningsfelt**.  

|Angive indstillinger for felt|Bedste fremgangsmåde|Bemærkning|  
|-----------------|-------------------|-------------|  
|Genbestillingsmetode||Du kan finde flere oplysninger i [Oprette bedste fremgangsmåder: Genbestillingspolitikker](setup-best-practices-reordering-policies.md).|  
|Reserver|Vælg **Aldrig**, når varen er planlagt ved hjælp af et genbestillingspunkt.<br /><br /> I produktion skal du vælge **Aldrig** for at tillade planlægningssystemet at dække alle behov.<br /><br /> Vælg **Eventuelt** for varer, du vil reservere til kunder med topprioritet.<br /><br /> Vælg **Altid** for ikke-entydige elementer som elementer af typen Diverse, der er indgået til specifikke krav.|Reservationer modvirker generelt formålet med planlægning, der er at skabe balance mellem efterspørgsel og udbud. Derfor skal varer, der er angivet til planlægning normalt ikke reserveres.<br /><br /> Hvis brugeren reserverer en lagerantal til fremtidige behov, forstyrres planlægningsgrundlaget, og genbestillingspunktet fungerer muligvis ikke korrekt. Selvom det planlagte beholdningsniveau er acceptabelt med hensyn til genbestillingspunkt, er mængderne muligvis ikke tilgængelige på grund af reservationen.|  
|Bufferperiode|Indstil med hensyn til leverandørens fleksibilitet.|Hvis leverandøren accepterer ordreændringer i sidste øjeblik, skal du bruge en længere periode. Hvis leverandøren kræver fast planlægning, skal du afkorte dit tidsrum så meget som muligt.<br /><br /> Du kan finde oplysninger om den globale opsætning i [Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md).|  
|Buffermængde||Du kan finde oplysninger om den globale opsætning i [Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md).|  
|Medtag lager|Vælg altid, når du bruger en Lot-for-Lot genbestillingsmetode.|Vælg ikke kun i særlige situationer, f.eks når lagervarer ikke er salgbare.|  
|Sikkerhedstid|Indstillingen skal ligge mellem 1D og 6D.<br /><br /> Angiv en sikkerhedstid på mindst én dag for at sikre, at leverancer er tilgængelige på dagen, før der er behov for dem.<br /><br /> Hvis du bruger en ny leverandør, skal du definere en længere tid, indtil deres leveringsevne er kendt.<br /><br /> Definer længere sikkerhedstider for kritiske komponenter i produktion.|Levering, som er planlagt af systemet for at undgå, at varen ikke er på lager, vil ankomme på samme dag, som varen ikke længere er på lager. Dette kan være flere timer for sent, hvis der f.eks. er efterspørgsel om morgenen, og leveringen ankommer om eftermiddagen. **Bemærk:** Feltet **Sikkerhedstid** bruger basiskalenderen. Derfor er 14 D ikke nødvendigvis to uger.|  
|Sikkerhedslager|Bruges til varer med store efterspørgselsudsving.<br /><br /> I produktion, bruges til kritiske komponenter.<br /><br /> Bruges til varer, der er omfattet af serviceaftaler.|Hvis feltet **Genbestillingspunkt** ikke er udfyldt, så fungerer sikkerhedslageret også som et genbestillingspunkt.|  
|Akkumuleringsperiode for lot|Hvis du ønsker kun nogle få store ordrer, og du accepterer at have lager, så skal du angive en lang akkumuleringsperiode for lot.<br /><br /> Hvis du ønsker flere små ordrer og minimalt lager, så skal du angive en kort akkumuleringsperiode for lot.|Akkumuleringsperioden for lot er normalt den længste periode, hvor du vil have lager.|  
|Genbestillingspunkt|Du kan basere genbestillingspunktet på varens behovsprofil.|Hvis historiske data viser, at det gennemsnitlige varebehov er 100 enheder i en leveringstid på syv dage, kan genbestillingspunktet indstilles til 100 som et minimum.<br /><br /> Det betyder, at når lagerniveauet falder i under 100 enheder, vil planlægningssystemet foreslå at genbestille, fordi det tager syv dage at levere varen, og der skal være tilstrækkeligt til at dække efterspørgslen i disse syv dage.|  
|Interval|Skal være tomt, det betyder, at lagerniveauet kontrolleres hver dag.|Kontrol af lagerniveauet hver dag sikrer optimal genbestillingspunktsplanlægning. **Bemærk:** Et interval på 1U betyder, at lagerniveauet må være under genbestillingspunktet i en uge, før der foreslås en forsyningsordre.|  
|Afrundingspræcision|I dyr produktion, skal du angive 0,00001.|Store afrundingsmængder af spild eller materialeforbrug kan føre til meget store lageromkostninger. Det kan derfor være relevant at angive den mindste afrundingspræcision for at minimere denne potentielle omkostning.|  

> [!NOTE]  
>  De bedste fremgangsmåder til planlægningsparametrene på varekortet gælder også for de samme felter på varekortene.  
>   
>  Hvis virksomheder planlægger med behov på forskellige lokationer, anbefales det kraftigt at definere lagervarer for hver lokation, og at alle behov oprettes ved hjælp af en værdi i feltet **Lokationskode**. Du kan finde flere oplysninger i [Designoplysninger: Behov på lokationen TOM](design-details-demand-at-blank-location.md).  

## <a name="see-also"></a>Se også  
 [Konfigurere bedste fremgangsmåder: Forsyningsplanlægning](setup-best-practices-supply-planning.md)   
 [Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)   
 [Opret komplekse moduler ved hjælp af bedste praksis](set-up-complex-application-areas-using-best-practices.md)  
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

