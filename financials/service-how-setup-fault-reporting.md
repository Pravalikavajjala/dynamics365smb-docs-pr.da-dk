---
title: Konfigurere fejlrapportering i Service | Microsoft Docs
description: "Få at vide, hvordan du konfigurerer fejlrapporteringsprocesser."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 19a377f9c4a41bee6aecc182774f884b1ead36ad
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---

# <a name="how-to-set-up-fault-reporting"></a>Fremgangsmåde: Definere fejlrapportering
Med Fejlrapportering kan du angive standarder for registrering af oplysninger om fejl på serviceartikler. F.eks. kan du angive, hvad problemet er, de symptomer, du ser, årsagen til problemet, og hvordan det løses.  

Fejlkoder angiver de typiske serviceartikelfejl eller de handlinger, der udføres på serviceartikler. Det afhænger af niveauet for fejlrapporteringen i din virksomhed, om du evt. blive nødt til at definere fejlområdekoder og symptomkoder, inden du definerer fejlkoder. Fejlområder beskriver områder med serviceartikelfejl. Fejlårsagskoder beskriver årsagen til serviceartikelfejl og om nødvendigt, om garanti- og kontraktrabatter skal udelukkes. Hvis kunden f.eks. er ansvarlig for fejlen på serviceartiklen, vil der evt. være behov for at udelukke garanti- og kontraktrabatter. Du tildeler fejlårsagskoder til serviceordrer. Du kan finde flere oplysninger i [Fremgangmåde: Arbejde med serviceopgaver](service-how-to-work-on-service-tasks.md).  

## <a name="to-specify-the-overall-level-of-fault-reporting-to-use"></a>Sådan angives det generelle fejlrapporteringsniveau, der skal bruges
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceopsætning**, og vælg derefter det relaterede link. 
2. I feltet **Fejlrapporteringsniveau** skal du vælge en af de indstillinger, der er beskrevet i følgende tabel.  
  
    |**Fejlniveau**|**Beskrivelse**|  
    |------------|-------------|  
    |Ingen | Der bruges ikke rapporteringskoder.|  
    |Fejl | Koderne vises i tabellen **Fejlkoder**. Disse koder identificerer fejl på serviceartikler eller handlinger, der skal udføres på serviceartikler. Du kan samle relaterede koder i grupper af **Fejlområdekode**.|  
    |Fejl + symptom | Du angiver en kombination af koder i tabellerne **Fejlkoder** og **Symptomkoder**. De typiske symptomkoder er bl.a. indikationer, som en kunde kan bruge til at beskrive et problem, f.eks. en mislyd eller en egenskab.|  
    |Fejl + symptom + type. | Du bruger koderne for fejl, symptom og fejlområde, som er en implementering af det internationale reparationskodesystem IRIS (International Repair Coding System).|  
  
Når du skal færdiggøre opsætningen af fejlrapportering, kan du også angive, hvilke reparationer eller løsninger der er knyttet til en fejl eller defekt. Du konfigurerer dette på siden **Fejl/løsn.koderelation**, hvor du opretter kombinationer af koder for serviceartikelgruppen i den serviceartikel, hvorfra du har åbnet vinduet, og antallet af forekomster for hver enkelt.

## <a name="to-create-fault-and-resolution-code-relationships"></a>Sådan indsættes fejl- og løsningskoderelationer
<!--this needs to go in a working with topic-->
Du skal samle oplysninger sammen vedr. fejl/løsningskoderelationer, så du kan se de mest almindelige reparationsmetoder for bestemte varefejl, når du reparerer varerne. Brug kørslen **Indsæt fejl/løsningsrelationer** til at finde alle kombinationerne af fejl- og løsningskoder i bogførte serviceordrer, og registrer dem på siden **Fejl/løsn.koderelationer**. 
  
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Indsæt fejl/løsningsrelationer**, og vælg derefter det relaterede link.  
2. Angiv datoer for at definere den periode, du vil have med i kørslen.  
3. Marker afkrydsningsfeltet **Relation baseret på serviceartikelgrp.**, hvis du vil gruppere relationerne efter serviceartikelgruppe.  
4. Markér afkrydsningsfeltet **Bevar manuelt indsat post**, hvis du vil bevare de poster, du allerede har indsat manuelt på siden **Fejl/løsn.koderelationer**.  

## <a name="see-also"></a>Se også
[Konfigurere Service](service-setup-service.md)  
[Service Management](service-service.md)  

