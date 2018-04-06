---
title: "Kriterier for overførsel af finansposter til omkostningsposter | Microsoft Docs"
description: "Det er vigtigt at forstå kriterierne for overførsel af finansposter til prisposter. Under overførslen bruger kørslen **Overfør finansposter til CA** følgende kriterier til at fastslå, om og hvordan finansposterne overføres."
services: project-madeira
documentationcenter: 
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
ms.openlocfilehash: b1ac9d3d0ab7022d5a11ad1642cf496d07bc81ce
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="criteria-for-transferring-general-ledger-entries-to-cost-entries"></a><span data-ttu-id="7a050-104">Kriterier for overførsel af finansposter til omkostningsposter.</span><span class="sxs-lookup"><span data-stu-id="7a050-104">Criteria for Transferring General Ledger Entries to Cost Entries</span></span>
<span data-ttu-id="7a050-105">Det er vigtigt at forstå kriterierne for overførsel af finansposter til prisposter.</span><span class="sxs-lookup"><span data-stu-id="7a050-105">It is important to understand the criteria for transferring general ledger entries to cost entries.</span></span> <span data-ttu-id="7a050-106">Under overførslen bruger kørslen **Overfør finansposter til CA** følgende kriterier til at fastslå, om og hvordan finansposterne overføres.</span><span class="sxs-lookup"><span data-stu-id="7a050-106">During the transfer, the **Transfer GL Entries to CA** batch job uses the following criteria to determine if and how the general ledger entries are transferred.</span></span>  

<span data-ttu-id="7a050-107">Finansposter overføres i følgende tilfælde:</span><span class="sxs-lookup"><span data-stu-id="7a050-107">General ledger entries are transferred if:</span></span>  

-   <span data-ttu-id="7a050-108">Posterne har dimensionsværdier, der svarer til enten et omkostningssted eller et omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="7a050-108">The entries have dimension values corresponding to either a cost center or a cost object.</span></span>  
-   <span data-ttu-id="7a050-109">Posterne har dimensionsværdier, der svarer til et omkostningssted og et omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="7a050-109">The entries have dimension values that correspond to a cost center and a cost object.</span></span> <span data-ttu-id="7a050-110">For disse poster har omkostningsstedet forrang.</span><span class="sxs-lookup"><span data-stu-id="7a050-110">For these entries, the cost center takes precedence.</span></span> <span data-ttu-id="7a050-111">Dette hjælper med at undgå en situation, hvor en omkostningstype vises i både et omkostningsobjekt og et omkostningssted og derfor tælles to gange i statistikken.</span><span class="sxs-lookup"><span data-stu-id="7a050-111">This helps avoid a situation where a cost type appears in both a cost object and a cost center and is therefore counted twice in the statistics.</span></span>  
-   <span data-ttu-id="7a050-112">Dokumentnummeret i posterne er tomt, så det vises med dokumentnummeret 0000 i omkostningsposterne.</span><span class="sxs-lookup"><span data-stu-id="7a050-112">The document number in the entries is empty, so it will appear with a document number of 0000 in the cost entries.</span></span>  
-   <span data-ttu-id="7a050-113">Posterne overføres til en omkostningstype, der giver mulighed for samlede poster, og disse poster overføres som en samlet post enten hver måned eller hver dag.</span><span class="sxs-lookup"><span data-stu-id="7a050-113">The entries are transferred to a cost type that allows for combined entries and these entries are transferred as a combined entry either monthly or daily.</span></span>  

<span data-ttu-id="7a050-114">Finansposter overføres ikke i følgende tilfælde:</span><span class="sxs-lookup"><span data-stu-id="7a050-114">General ledger entries are not transferred if:</span></span>  

-   <span data-ttu-id="7a050-115">Posterne har dimensionsværdier, der ikke svarer til et omkostningssted eller et omkostningsobjekt.</span><span class="sxs-lookup"><span data-stu-id="7a050-115">The entries have dimension values that do not correspond to a cost center or a cost object.</span></span>  
-   <span data-ttu-id="7a050-116">Posterne har værdien nul.</span><span class="sxs-lookup"><span data-stu-id="7a050-116">The entries have an amount of zero.</span></span>  
-   <span data-ttu-id="7a050-117">Posterne har en finanskonto, der er blevet slettet.</span><span class="sxs-lookup"><span data-stu-id="7a050-117">The entries have a general ledger account that has been deleted.</span></span>  
-   <span data-ttu-id="7a050-118">Posterne har en finanskonto, der ikke er af typen **Resultatopgørelse**.</span><span class="sxs-lookup"><span data-stu-id="7a050-118">The entries have a general ledger account that is not of the type **Income Statement**.</span></span>  
-   <span data-ttu-id="7a050-119">Posterne har en finanskonto, der ikke er tildelt en omkostningstype.</span><span class="sxs-lookup"><span data-stu-id="7a050-119">The entries have a general ledger account that is not assigned a cost type.</span></span>  
-   <span data-ttu-id="7a050-120">Posterne har en bogføringsdato før **Startdato for finansoverførsel**.</span><span class="sxs-lookup"><span data-stu-id="7a050-120">The entries have a posting date before the **Starting Date for G/L Transfer**.</span></span>  
-   <span data-ttu-id="7a050-121">Posterne er blevet bogført med en ultimodato.</span><span class="sxs-lookup"><span data-stu-id="7a050-121">The entries have been posted with a closing date.</span></span> <span data-ttu-id="7a050-122">De er typisk poster, der fører resultatopgørelsens saldo tilbage i slutningen af året.</span><span class="sxs-lookup"><span data-stu-id="7a050-122">These are typically entries that set back the balance of the income statement at the end of the year.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7a050-123">Se også</span><span class="sxs-lookup"><span data-stu-id="7a050-123">See Also</span></span>  
[<span data-ttu-id="7a050-124">Regnskab for omkostninger</span><span class="sxs-lookup"><span data-stu-id="7a050-124">Accounting for Costs</span></span>](finance-manage-cost-accounting.md)  
 <span data-ttu-id="7a050-125">[Overføre finansposter til omkostningsposter](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="7a050-125">[Transfer General Ledger Entries to Cost Entries](finance-how-to-transfer-general-ledger-entries-to-cost-entries.md) </span></span>  
 <span data-ttu-id="7a050-126">[Overførsel og bogføring af omkostningsposter](finance-transfer-and-post-cost-entries.md) </span><span class="sxs-lookup"><span data-stu-id="7a050-126">[Transferring and Posting Cost Entries](finance-transfer-and-post-cost-entries.md) </span></span>  
 [<span data-ttu-id="7a050-127">Om omkostningsregnskab</span><span class="sxs-lookup"><span data-stu-id="7a050-127">About Cost Accounting</span></span>](finance-about-cost-accounting.md)  
 <span data-ttu-id="7a050-128">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7a050-128">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
