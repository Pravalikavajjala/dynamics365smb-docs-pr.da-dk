---
title: "Sådan opretter du workflows ud fra workflowskabeloner | Microsoft Docs"
description: For at spare tid ved oprettelse af nye workflows kan du oprette workflows ud fra workflowskabeloner.
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
ms.openlocfilehash: dcf6f5f5b0364ebcaefdcbc43fdbd7471cb6079e
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-create-workflows-from-workflow-templates"></a>Fremgangsmåde: Oprette workflows ud fra workflowskabeloner
For at spare tid ved oprettelse af nye workflows kan du oprette workflows ud fra workflowskabeloner.  

 Workflowskabeloner er workflows, som ikke kan redigeres, og som findes i den generiske version af [!INCLUDE[d365fin](includes/d365fin_md.md)]. Koderne for workflowskabeloner, som er tilføjet af Microsoft, har "MS" foran som f.eks. i "MS-".  

 En anden måde til hurtigt at oprette et workflow på er at importere et eksisterende workflow, som du har på en fil uden for [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan finde flere oplysninger i [Fremgangsmåde: Importere og eksportere workflows](across-how-to-export-and-import-workflows.md).  

I vinduet **Workflow** opretter du et workflow ved at angive de involverede trin på linjerne. Hvert trin består af en hændelse i arbejdsgangen, begrænset af hændelsesbetingelser og et arbejdsgangssvar, begrænset af svarmuligheder. Du definerer arbejdsgangstrin ved at udfylde felter om arbejdsganglinjer fra faste lister over hændelses- og svarværdier, der repræsenterer scenarier, der understøttes af programkoden. Du kan finde flere oplysninger i [Fremgangsmåde: Oprette arbejdsgange](across-how-to-create-workflows.md).  

## <a name="to-create-a-workflow-from-workflow-template"></a>Sådan opretter du fra et workflow ud fra en workflowskabelon  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), og angiv **Workflows**, og vælg derefter det relaterede link.  
2.  Vælg handlingen **Opret workflow fra skabelon**. Vinduet **Workflowskabeloner** åbnes.  
3.  Vælg et workflow, og vælg derefter knappen **OK**.  

     Vinduet **Workflow** åbnes for et nyt workflow, der indeholder alle oplysninger fra den valgte skabelon. Værdien i feltet **Kode** er udvidet med f.eks. "-01" for at angive, at dette er det første workflow, som oprettes ud fra workflowskabelonen.  
4.  Fortsæt med at oprette workflowet ved at redigere workflowtrinene eller tilføje nye trin. Du kan finde flere oplysninger i [Fremgangsmåde: Oprette arbejdsgange](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Se også  
 [Fremgangsmåde: Oprette arbejdsgange](across-how-to-create-workflows.md)   
 [Fremgangsmåde: Importere og eksportere workflows](across-how-to-export-and-import-workflows.md)   
 [Fremgangsmåde: Se arkiverede forekomster af arbejdsgangstrin](across-how-to-view-archived-workflow-step-instances.md)   
 [Fremgangsmåde: Slette arbejdsgange](across-how-to-delete-workflows.md)   
 [Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Opsætte workflows](across-set-up-workflows.md)   
 [Anvende workflows](across-use-workflows.md)   
 [Workflow](across-workflow.md)   

