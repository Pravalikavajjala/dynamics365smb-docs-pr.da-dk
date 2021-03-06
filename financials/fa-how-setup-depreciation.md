---
title: "Definere anlægsafskrivning | Microsoft Docs"
description: "Du bruger en afskrivningsprofil til at angive, hvordan anlægsaktiver skal afskrives eller nedskrives."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: fbdfc4431056c4851208aa063daf8761b4e70bf1
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-fixed-asset-depreciation"></a>Fremgangsmåde: Konfigurere afskrivning af anlægsaktiver
 Du kan bruge forskellige afskrivningsmetoder til forberedelse af årsregnskab og selvangivelse. Mange store virksomheder benytter lineær afskrivning i deres årsregnskab, fordi dette som regel tillader angivelse af højere indkomst. Af skattemæssige årsager bruger mange virksomheder dog en metode til hurtigere afskrivning. Du kan finde flere oplysninger i [Afskrivningsmetoder](fa-depreciation-methods.md).

 Når du har oprettet de relevante afskrivningsprofiler, skal du tildele en eller flere afskrivningsprofiler til hvert anlægsaktiv. En afskrivningsprofil, der er tildelt til et anlægsaktiv, kaldes en anlægsafskrivningsprofil. Derfor kaldes vinduet for tildelte afskrivningsprofiler **Anlægsafskrivningsprofiler**.

## <a name="to-create-a-depreciation-book"></a>Sådan oprettes en afskrivningsprofil
I en anlægsafskrivningsprofil angiver du, hvordan anlægsaktiver skal afskrives. Du kan definere flere afskrivningsprofiler for at tage højde for forskellig slags afskrivningsmetoder.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Afskrivningsprofiler**, og vælg derefter det relaterede link.
2. I vinduet **Afskrivningsprofiloversigt** skal du vælge handlingen **Ny**.
3. I vinduet **Afskrivningsprofilkort** skal du udfylde felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
>   Du kan registrere anlægstransaktioner i vinduet **Anlægskassekladde** eller i vinduet **Anlægskladde**, afhængigt af, om transaktionerne, der er til finansiel rapportering eller intern administration. Udfør næste trin for at angive, hvilken type kladden der som standard bruges til de forskellige anlægsaktiviteter.
4. På oversigtspanelet **Integration** skal du markere afkrydsningsfeltet for hvert anlægsaktivitet, hvis transaktioner skal bogføres ved hjælp af vinduet **Anlægskassekladde**.
5. Gentag trin 2 til 4 for hver afskrivningsmetode eller bogføringsmetode, du vil tildele til anlægsaktiver som en afskrivningsprofil.

## <a name="to-assign-a-depreciation-book-to-a-fixed-asset"></a>Sådan tildeles en afskrivningsprofil til et anlægsaktiv
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Anlægsaktiver**, og vælg derefter det relaterede link.
2. Vælg det anlægsaktiv, som du vil konfigurere en anlægsafskrivningsprofil for.
3. I oversigtspanelet **Afskrivningsprofil** skal du udfylde felterne efter behov.
4. Hvis du vil tildele mere end én afskrivningsprofil til anlægsaktivet, skal du vælge handlingen **Tilføj flere afskrivningsprofiler**.
5. Du kan også vælge handlingen **Afskrivningsprofiler** for at angive en eller flere anlægsafskrivningsprofiler.

    > [!NOTE]  
>   Når du bruger den manuelle afskrivningsmetode, skal du angive afskrivningen manuelt i anlægskassekladden. Funktionen **Beregn afskrivninger** udelader de anlægsaktiver, som benytter den manuelle afskrivningsmetode. Du kan bruge denne metode til aktiver, der ikke skal afskrives, f.eks. jord.

## <a name="to-assign-a-depreciation-book-to-multiple-fixed-assets-with-a-batch-job"></a>Sådan tildeles en afskrivningsprofil til flere anlægsaktiver med en kørsel
Hvis du vil tildele en afskrivningsprofil til flere anlægsaktiver, kan du bruge kørslen **Opret anlægsafskr.profiler** til at oprette anlægsafskrivningsprofiler.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Anlægsaktiver**, og vælg derefter det relaterede link.
2. Vælg det anlægsaktiv, som du vil tildele en afskrivningsprofil, og vælg derefter handlingen **Rediger**.
3. I vinduet **Afskrivningsprofilkort** skal du vælge handlingen **Opret anlægsafskr.profiler**.
4. I vinduet **Opret anlægsafskr.profiler** skal du udfylde feltet **Afskrivningsprofil**.
5. Vælg feltet **Kopier fra anlægsnr.**, og vælg derefter det anlægsnummer, du vil bruge som grundlag for oprettelsen af nye afskrivningsprofiler for anlægsaktiver.

    Hvis du udfylder feltet, får afskrivningsfelterne i de nye anlægsafskrivningsprofiler samme indhold som de tilsvarende felter i den anlægsafkrivningsprofil, du kopierer fra. Lad feltet stå tomt, hvis du vil oprette nye anlægsafskrivningsprofiler med tomme afskrivningsfelter.  
6. I oversigtspanelet **Anlæg** kan du definere et filter for at udvælge de aktiver, som du vil oprette anlægsafskrivningsprofiler for.
7. Vælg knappen **OK**.

## <a name="to-set-up-depreciation-posting-types"></a>Sådan defineres bogføringstyper for afskrivning
For hver afskrivningsprofil skal du angive, hvordan [!INCLUDE[d365fin](includes/d365fin_md.md)] skal håndtere forskellige bogføringstyper. For eksempel skal det angives, om bogføringen skal være debet eller kredit, og om bogføringstypen skal medtages i afskrivningsgrundlaget.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Afskrivningsprofiler**, og vælg derefter det relaterede link.  
2. Vælg den afskrivningsprofil, du vil konfigurere, og vælg derefter handlingen **Anlægsbogf.typeopsætning**.
3. Udfyld felterne efter behov i vinduet **Anlægsbogf.typeopsætning**.

    > [!NOTE]  
>   Du kan ikke indsætte eller slette linjer i vinduet **Anlægsbogf.typeopsætning**. Du kan kun rette eksisterende linjer.

    Det anbefales dog, at du ikke ændrer opsætningen af afskrivningsprofiler, hvori posteringer allerede er blevet bogført. Ændringer har ikke indflydelse på posteringer, som allerede er bogført, hvilket ville gøre afskrivningsprofilstatistikken misvisende.

## <a name="to-set-up-default-templates-and-batches-for-fixed-asset-depreciation"></a>Sådan defineres standardtyper og -kørsler for anlægsafskrivning
For hver afskrivningsprofil skal du definere en standardopsætning med typer og navne. Du bruger disse standarder til at duplikere linjer fra én kladde til en anden, oprette kladdelinjer ved hjælp af kørslen **Beregn afskrivning** eller **Indekser anlæg**, duplikere anskaffelsesomkostninger i forsikringskladden.  

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Afskrivningsprofiler**, og vælg derefter det relaterede link.  
2. Vælg den afskrivningsprofil, du vil definere standardkladder for, og vælg derefter handlingen **Anlægskladdeopsætning**.  
3. Hvis du vil have en standardopsætning for hver enkelt bruger, skal du vælge feltet **Bruger-id** for at vælge opsætninger i vinduet **Brugere**.  
4. Vælg den kladdetype eller kørsel i de andre felter, som skal bruges som standard.  

## <a name="see-also"></a>Se også
[Opsætning af anlægsaktiver](fa-setup.md)  
[Anlægsaktiver](fa-manage.md)  
[Finans](finance.md)  
[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

