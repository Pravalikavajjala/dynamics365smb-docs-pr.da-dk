---
title: Definere omkostningssteder og omkostningsemner for kontoplanen | Microsoft Docs
description: "Du kan automatisk overføre posterne udgifter og indtægter fra regnskabet til omkostningsregnskab, enten for hver bogføring til regnskab eller med et batchjob. Når du foretager overførslen, overfører systemet kun de poster, der allerede er knyttet til et omkostningssted eller et omkostningsobjekt. For at oprette en relevant overførsel skal du sikre omkostningssteder og omkostningsobjekter er korrekt defineret."
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
ms.openlocfilehash: 0a3b89e2d2a59aa3434e747976437f24860be408
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="defining-cost-centers-and-cost-objects-for-chart-of-accounts"></a>Definition af omkostningssteder og omkostningsobjekter for kontoplanen
Du kan automatisk overføre posterne udgifter og indtægter fra regnskabet til omkostningsregnskab, enten for hver bogføring til regnskab eller med et batchjob. Når du foretager overførslen, overfører [!INCLUDE[d365fin](includes/d365fin_md.md)] kun de poster, der allerede er knyttet til et omkostningssted eller et omkostningsobjekt. For at oprette en relevant overførsel skal du sikre omkostningssteder og omkostningsobjekter er korrekt defineret.  

## <a name="defining-default-dimension-values-for-general-ledger-accounts"></a>Definere standarddimensionsværdier for finanskonti  
For hver enkelt finanskonto kan du definere standarddimensionsværdier i tabellen **Standarddimension**. Følgende eksempel viser, hvordan du definerer, at der altid skal være et omkostningssted DEPARTMENT, men aldrig et omkostningsobjekt PROJECT, når du bogfører til en finanskonto.  

|**Dimensionskode**|**Værdibogføring**|  
|------------------------------------------|-----------------------------------------|  
|Afdeling|Tvungen kode|  
|Projekt|Ingen kode|  

## <a name="defining-dimension-values-for-overhead-costs-and-direct-costs"></a>Definition af dimensionsværdier for faste og direkte omkostninger  
 Du kan overføre faste omkostninger til et omkostningssted og direkte omkostninger til et omkostningsobjekt. Følgende tabel viser den optimale kombination af dimensionsopsætningsværdierne.  

|Kopiér til|Omkostningsstedbogføring|Omkostningsobjektbogføring|  
|-----------------|-------------------------|-------------------------|  
|Omkostningssted|Tvungen kode|Ingen kode|  
|Omkostningsobjekt|Ingen kode|Tvungen kode|  

> [!NOTE]  
>  For at sikre, at det foruddefinerede omkostningssted og omkostningsemne, du har oprettet i regnskabet, automatisk overføres til omkostningsregnskab, skal du markere afkrydsningsfeltet **Kontroller finansbogføringer** i vinduet Konfiguration af omkostningsregnskab.  

## <a name="see-also"></a>Se også  
[Regnskab for omkostninger](finance-manage-cost-accounting.md)  
[Sådan opsættes omkostningssteder](finance-how-to-set-up-cost-centers.md)   
[Fremgangsmåde: Konfigurere omkostningsobjekter](finance-how-to-set-up-cost-objects.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

