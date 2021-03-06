---
title: "Bedste fremgangsmåder for opsætning af global planlægning | Microsoft Docs"
description: "Oversigtpanelet **Planlægning** i vinduet **Produktionsopsætning** indeholder flere felter, der definerer globale regler for forsyningsplanlægning."
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
ms.openlocfilehash: f1a4e3a30d4d665a83ab599ad19dfd3760d744b2
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="setup-best-practices-global-planning-setup"></a>Konfigurere bedste fremgangsmåder: Global planlægningsopsætning
Oversigtpanelet **Planlægning** i vinduet **Produktionsopsætning** indeholder flere felter, der definerer globale regler for forsyningsplanlægning.  

 Følgende tabel viser de bedste fremgangsmåder til konfiguration af udvalgte globale felter med planlægningsparametre. Du kan få yderligere oplysninger om et felt ved at vælge linket i kolonnen **Opsætningsfelt**.  

|Angive indstillinger for felt|Bedste fremgangsmåde|Bemærkning|  
|-----------------|-------------------|-------------|  
|Forecast på lokationer|Vælg denne indstilling, hvis du har prognoser for bestemte lokationer.||  
|Komponenter på lokation|Hvis varerne ikke er defineret som lagervarer, skal du vælge lokationskoden til hovedlageret.|Dette gælder også, hvis du kun bruger indkøbskladden.|  
|Tomt overløbsniveau|Vælg **Tillad standardberegning** Hvis du overfører fra Microsoft Dynamics NAV 5.0 eller tidligere.|Skal kun bruges, hvis du vil tillade alle eller nogle af varerne at løbe over genbestillingspunktet.|  
|Standardbufferperiode|Indstillingen skal ligge mellem 1D og 5D.<br /><br /> Hvis du er nybegynder i planlægning i [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du angive en længere periode.|Når brugerne er mere fortrolige med de forskellige årsager til aktionsmeddelelser, kan du afkorte bufferperioden for at tillade flere ændringsforslag.|  
|Standardbufferantal|Indstilles til mellem 5 og 20 % af varens lotstørrelse.||  

## <a name="see-also"></a>Se også  
 [Konfigurere bedste fremgangsmåder: Forsyningsplanlægning](setup-best-practices-supply-planning.md)   
 [Designoplysninger: Forsyningsplanlægning](design-details-supply-planning.md)   
 [Opret komplekse moduler ved hjælp af bedste praksis](set-up-complex-application-areas-using-best-practices.md)  
 [Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

