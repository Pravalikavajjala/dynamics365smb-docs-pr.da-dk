---
title: "Sådan eksporterer og importerer du workflows | Microsoft Docs"
description: "Du kan overføre workflows til andre Business Central-databaser, f.eks. for at spare tid ved oprettelse af nye workflows, ved at eksportere og importere workflows."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 3491a8cf322c4a1ac5385c09e05ec6cd828b4c53
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="export-and-import-workflows"></a><span data-ttu-id="f253d-103">Eksportere og importere workflows</span><span class="sxs-lookup"><span data-stu-id="f253d-103">Export and Import Workflows</span></span>
<span data-ttu-id="f253d-104">Du kan overføre workflows til andre [!INCLUDE[d365fin](includes/d365fin_md.md)]-databaser, f.eks. for at spare tid ved oprettelse af nye workflows, ved at eksportere og importere workflows.</span><span class="sxs-lookup"><span data-stu-id="f253d-104">To transfer workflows to other [!INCLUDE[d365fin](includes/d365fin_md.md)] databases, for example to save time when creating new workflows, you can export and import workflows.</span></span>  

 <span data-ttu-id="f253d-105">En anden måde til hurtigt at oprette workflows er at oprette workflows fra workflowskabeloner.</span><span class="sxs-lookup"><span data-stu-id="f253d-105">Another way to quickly create workflows is to create workflows from workflow templates.</span></span> <span data-ttu-id="f253d-106">Du kan finde flere oplysninger i [Oprette workflows ud fra workflowskabeloner](across-how-to-create-workflows-from-workflow-templates.md).</span><span class="sxs-lookup"><span data-stu-id="f253d-106">For more information, see [Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md).</span></span>  

 <span data-ttu-id="f253d-107">I vinduet **Workflow** opretter du et workflow ved at angive de involverede trin på linjerne.</span><span class="sxs-lookup"><span data-stu-id="f253d-107">In the **Workflow** window, you create a workflow by listing the involved steps on the lines.</span></span> <span data-ttu-id="f253d-108">Hvert trin består af en hændelse i arbejdsgangen, begrænset af hændelsesbetingelser og et arbejdsgangssvar, begrænset af svarmuligheder.</span><span class="sxs-lookup"><span data-stu-id="f253d-108">Each step consists of a workflow event, moderated by event conditions, and a workflow response, moderated by response options.</span></span> <span data-ttu-id="f253d-109">Du definerer workflowtrin ved at udfylde felter om workflowlinjer fra faste lister over hændelses- og responsværdier, der repræsenterer scenarier, der understøttes af programkoden.</span><span class="sxs-lookup"><span data-stu-id="f253d-109">You define workflow steps by filling fields on workflow lines from fixed lists of event and response values representing scenarios that are supported by the application code.</span></span> <span data-ttu-id="f253d-110">Du kan finde flere oplysninger i [Oprette arbejdsgange](across-how-to-create-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="f253d-110">For more information, see [Create Workflows](across-how-to-create-workflows.md).</span></span>  

## <a name="to-export-a-workflow"></a><span data-ttu-id="f253d-111">Sådan eksporteres et workflow</span><span class="sxs-lookup"><span data-stu-id="f253d-111">To export a workflow</span></span>  
1.  <span data-ttu-id="f253d-112">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), og angiv **Workflows**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f253d-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f253d-113">Vælg et workflow, og vælg derefter handlingen **Eksportér til fil**.</span><span class="sxs-lookup"><span data-stu-id="f253d-113">Select a workflow, and then choose the **Export to File** action.</span></span>  
3.  <span data-ttu-id="f253d-114">Vælg knappen **Gem** i vinduet **Udlæs fil**.</span><span class="sxs-lookup"><span data-stu-id="f253d-114">In the **Export File** window, choose the **Save** button.</span></span>  
4.  <span data-ttu-id="f253d-115">I vinduet **Udlæs** skal du vælge en filplacering og derefter klikke på knappen **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f253d-115">In the **Export** window, select a file location, and then choose the **Save** button.</span></span>  

## <a name="to-import-a-workflow"></a><span data-ttu-id="f253d-116">Sådan indlæses et workflow</span><span class="sxs-lookup"><span data-stu-id="f253d-116">To import a workflow</span></span>  
1.  <span data-ttu-id="f253d-117">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), og angiv **Workflows**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="f253d-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Workflows**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="f253d-118">Vælg handlingen **Importér fra fil**.</span><span class="sxs-lookup"><span data-stu-id="f253d-118">Choose the **Import from File** action.</span></span>  
3.  <span data-ttu-id="f253d-119">Vælg den XML-fil, der indeholder workflowet, i vinduet **Indlæs**, og vælg derefter knappen **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="f253d-119">In the **Import** window, choose the XML file that contains the workflow, and then choose the **Open** button.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="f253d-120">Hvis workflowkoden allerede findes i databasen, overskrives workflowtrinene med trinene i det indlæste workflow.</span><span class="sxs-lookup"><span data-stu-id="f253d-120">If the workflow code already exists in the database, the workflow steps will be overwritten with the steps in the imported workflow.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f253d-121">Se også</span><span class="sxs-lookup"><span data-stu-id="f253d-121">See Also</span></span>  
 <span data-ttu-id="f253d-122">[Oprette arbejdsgange](across-how-to-create-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="f253d-122">[Create Workflows](across-how-to-create-workflows.md) </span></span>  
 <span data-ttu-id="f253d-123">[Oprette workflows ud fra workflowskabeloner](across-how-to-create-workflows-from-workflow-templates.md) </span><span class="sxs-lookup"><span data-stu-id="f253d-123">[Create Workflows from Workflow Templates](across-how-to-create-workflows-from-workflow-templates.md) </span></span>  
 <span data-ttu-id="f253d-124">[Vise arkiverede forekomster af arbejdsgangstrin](across-how-to-view-archived-workflow-step-instances.md) </span><span class="sxs-lookup"><span data-stu-id="f253d-124">[View Archived Workflow Step Instances](across-how-to-view-archived-workflow-step-instances.md) </span></span>  
 <span data-ttu-id="f253d-125">[Slette arbejdsgange](across-how-to-delete-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="f253d-125">[Delete Workflows](across-how-to-delete-workflows.md) </span></span>  
 <span data-ttu-id="f253d-126">[Gennemgang: Opsætning og brug af workflow for godkendelse af køb](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span><span class="sxs-lookup"><span data-stu-id="f253d-126">[Walkthrough: Setting Up and Using a Purchase Approval Workflow](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md) </span></span>  
 <span data-ttu-id="f253d-127">[Opsætte workflows](across-set-up-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="f253d-127">[Setting Up Workflows](across-set-up-workflows.md) </span></span>  
 <span data-ttu-id="f253d-128">[Anvende workflows](across-use-workflows.md) </span><span class="sxs-lookup"><span data-stu-id="f253d-128">[Using Workflows](across-use-workflows.md) </span></span>  
 [<span data-ttu-id="f253d-129">Workflow</span><span class="sxs-lookup"><span data-stu-id="f253d-129">Workflow</span></span>](across-workflow.md)   
