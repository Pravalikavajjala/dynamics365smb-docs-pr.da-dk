---
title: Angive ressourcekostpriser, priser og kapacitet | Microsoft Docs
description: For at bruge ressourcer og lette projektstyring skal du angive omkostninger og priser for individuelle ressourcer eller ressourcegrupper og angive ressourcekapacitet.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, capacity, staff
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 982c250becec74472b89ae705057d1b34f95e338
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-resources"></a><span data-ttu-id="c9d43-103">Konfigurere ressourcer</span><span class="sxs-lookup"><span data-stu-id="c9d43-103">Set Up Resources</span></span>
<span data-ttu-id="c9d43-104">For at kunne administrere ressourceaktiviteterne korrekt skal du oprette ressourcerne og de tilhørende omkostninger og priser.</span><span class="sxs-lookup"><span data-stu-id="c9d43-104">To correctly manage resource activities, you must set up your resources and the related costs and prices.</span></span> <span data-ttu-id="c9d43-105">De sagsrelaterede pris-, rabat- og kostfaktorregler oprettes på jobkortet.</span><span class="sxs-lookup"><span data-stu-id="c9d43-105">The job-related prices, discounts, and cost factor rules are set up on the job card.</span></span> <span data-ttu-id="c9d43-106">Du kan angive omkostninger og priser for individuelle ressourcer, ressourcegrupper eller alle tilgængelige ressourcer i virksomheden.</span><span class="sxs-lookup"><span data-stu-id="c9d43-106">You can specify the costs and prices for individual resources, resource groups, or all available resources of the company.</span></span>

<span data-ttu-id="c9d43-107">Når der bruges eller sælges ressourcer i en sag, hentes de tilhørende priser og omkostninger fra de oplysninger, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="c9d43-107">When resources are used or sold in a job, the prices and costs associated with them are retrieved from the information that you set up.</span></span>

<span data-ttu-id="c9d43-108">Du kan angive standardbeløbet pr. time, når ressourcen oprettes.</span><span class="sxs-lookup"><span data-stu-id="c9d43-108">You specify the default amount per hour when the resource is created.</span></span> <span data-ttu-id="c9d43-109">Hvis du f.eks. bruger en bestemt maskine i fem timer i en sag, udregnes sagen ud fra beløbet pr. time.</span><span class="sxs-lookup"><span data-stu-id="c9d43-109">For example, if you use a specific machine on a job for five hours, the job would be calculated based on the amount per hour.</span></span>

## <a name="to-set-up-a-resource"></a><span data-ttu-id="c9d43-110">Sådan defineres en ressource</span><span class="sxs-lookup"><span data-stu-id="c9d43-110">To set up a resource</span></span>
<span data-ttu-id="c9d43-111">Opret et kort for hver ressource, du vil bruge i projekter.</span><span class="sxs-lookup"><span data-stu-id="c9d43-111">Create a card for each resource that you want to use in projects.</span></span>

1. <span data-ttu-id="c9d43-112">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ressourcer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c9d43-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resources**, and then choose the related link.</span></span>
2. <span data-ttu-id="c9d43-113">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c9d43-113">Choose the **New** action.</span></span>
3. <span data-ttu-id="c9d43-114">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="c9d43-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-set-up-a-resource-group"></a><span data-ttu-id="c9d43-115">Sådan oprettes en ressourcegruppe</span><span class="sxs-lookup"><span data-stu-id="c9d43-115">To set up a resource group</span></span>
<span data-ttu-id="c9d43-116">Du kan samle flere forskellige ressourcer i en ressourcegruppe.</span><span class="sxs-lookup"><span data-stu-id="c9d43-116">You can combine several resources in one resource group.</span></span> <span data-ttu-id="c9d43-117">Ressourcegruppens kapaciteter og budgetter bliver akkumuleret fra de enkelte ressourcer i gruppen.</span><span class="sxs-lookup"><span data-stu-id="c9d43-117">All capacities and budgets of resource groups are accumulated from the individual resources.</span></span> <span data-ttu-id="c9d43-118">Du kan også indtaste kapaciteter for ressourcegrupper, enten uafhængigt af de akkumulerede værdier eller som supplement til dem.</span><span class="sxs-lookup"><span data-stu-id="c9d43-118">It is also possible to enter capacities for resource groups either independently of the accumulated values or in addition to them.</span></span>

1. <span data-ttu-id="c9d43-119">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ressourcer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c9d43-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resource groups**, and then choose the related link.</span></span>
2. <span data-ttu-id="c9d43-120">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c9d43-120">Choose the **New** action.</span></span>
3. <span data-ttu-id="c9d43-121">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="c9d43-121">Fill in the fields as necessary.</span></span>

## <a name="to-set-capacity-for-a-resource"></a><span data-ttu-id="c9d43-122">Sådan angives kapaciteten for en ressource</span><span class="sxs-lookup"><span data-stu-id="c9d43-122">To set capacity for a resource</span></span>
<span data-ttu-id="c9d43-123">For at beregne, hvor lang tid en ressource kan bruge på sager, skal der først ressourcenes kapacitet først angives som disponible tid pr. periode i arbejdskalenderen.</span><span class="sxs-lookup"><span data-stu-id="c9d43-123">To calculate how much time a resource can spend on jobs, their capacity must first be set up as available time per period on the work calendar.</span></span> <span data-ttu-id="c9d43-124">Denne opsætning anvendes, når du udfylder sagsplanlægningslinjer, som indeholder ressourcen.</span><span class="sxs-lookup"><span data-stu-id="c9d43-124">This setup is used when you fill in job planning lines that contain the resource.</span></span> <span data-ttu-id="c9d43-125">Du kan finde flere oplysninger i [Oprette sager](projects-how-create-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="c9d43-125">For more information, see [Create Jobs](projects-how-create-jobs.md).</span></span>

1. <span data-ttu-id="c9d43-126">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ressourcer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c9d43-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resources**, and then choose the related link.</span></span>
2. <span data-ttu-id="c9d43-127">Åbn det relevante ressourcekort, og vælg derefter handlingen **Ressourcekapacitet**.</span><span class="sxs-lookup"><span data-stu-id="c9d43-127">Open the relevant resource card, and then choose the **Resource Capacity** action.</span></span>
3. <span data-ttu-id="c9d43-128">I vinduet **Ressourcekapacitet** feltet **Vis efter** skal du angive periodens længde, f.eks **Dag**, som vises i kolonnerne på oversigtspanelet **Matrix for ressourcekapacitet**.</span><span class="sxs-lookup"><span data-stu-id="c9d43-128">In the **Resource Capacity** window, in the **View By** field, specify the length of the period, such as **Day**, that is shown on columns on the **Resource Capacity Matrix** FastTab.</span></span>
4. <span data-ttu-id="c9d43-129">For hver ressource på en linje skal du for hver periode i kolonnerne angive det antal timer, hvor ressourcen er tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="c9d43-129">For each resource on a line, specify for each period on the columns the number of hours that the resource is available.</span></span>
5. <span data-ttu-id="c9d43-130">Du kan også angive ressourcens ugentlige kapacitet med en startdato og en slutdato ved at vælge handlingen **Angiv kapacitet**.</span><span class="sxs-lookup"><span data-stu-id="c9d43-130">Alternatively, to detail the resource's weekly capacity within a starting and ending date, choose the **Set Capacity** action.</span></span>
6. <span data-ttu-id="c9d43-131">I vinduet **Ressourcekap.indstillinger** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="c9d43-131">In the **Resource Capacity Settings** window, fill in the fields as necessary.</span></span>
7. <span data-ttu-id="c9d43-132">Vælg handlingen **Opdater kapacitet**.</span><span class="sxs-lookup"><span data-stu-id="c9d43-132">Choose the **Update Capacity** action.</span></span> <span data-ttu-id="c9d43-133">Vinduet **Ressourcekapacitet** opdateres med den angivne kapacitet.</span><span class="sxs-lookup"><span data-stu-id="c9d43-133">The **Resource Capacity** window is updated with the entered capacity.</span></span>
8. <span data-ttu-id="c9d43-134">Luk vinduet.</span><span class="sxs-lookup"><span data-stu-id="c9d43-134">Close the window.</span></span>

## <a name="to-set-up-alternate-resource-costs"></a><span data-ttu-id="c9d43-135">Sådan angives ressourcekostpriser</span><span class="sxs-lookup"><span data-stu-id="c9d43-135">To set up alternate resource costs</span></span>
<span data-ttu-id="c9d43-136">Udover de omkostninger, der er angivet på ressourcekortet, kan du oprette alternative omkostninger for hver ressource.</span><span class="sxs-lookup"><span data-stu-id="c9d43-136">In addition to the cost specified on the resource card, you can set up alternate costs for each resource.</span></span> <span data-ttu-id="c9d43-137">Hvis en medarbejder f.eks. har en højere timesats for overarbejde, kan du i denne tabel oprette en ressourcekostpris for overtidsbetalingen.</span><span class="sxs-lookup"><span data-stu-id="c9d43-137">For example, if you pay an employee a higher hourly rate for overtime, you can set up a resource cost for the overtime rate.</span></span> <span data-ttu-id="c9d43-138">Den alternative kostpris, du angiver for ressourcen, tilsidesætter kostprisen på ressourcekortet, når du bruger ressourcen i ressourcekladden.</span><span class="sxs-lookup"><span data-stu-id="c9d43-138">The alternate cost that you set up for the resource will override the cost on the resource card when you use the resource in the resource journal.</span></span>

1. <span data-ttu-id="c9d43-139">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ressourcer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c9d43-139">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resources**, and then choose the related link.</span></span>  
2. <span data-ttu-id="c9d43-140">Vælg ressource, som du vil angive en eller flere alternative omkostninger for, og vælg derefter handlingen **Kostpriser**.</span><span class="sxs-lookup"><span data-stu-id="c9d43-140">Select the resource for that you want to set up one or more alternate costs for, and then choose the **Costs** action.</span></span>  
3. <span data-ttu-id="c9d43-141">I vinduet **Ressourcekostpriser** skal du udfylde felterne på en linje efter behov.</span><span class="sxs-lookup"><span data-stu-id="c9d43-141">In the **Resource Costs** window, fill in the fields on a line as necessary.</span></span>  
4. <span data-ttu-id="c9d43-142">Gentag trin 3 for hver alternativ ressourcekostpris, du vil oprette.</span><span class="sxs-lookup"><span data-stu-id="c9d43-142">Repeat step 3 for each alternate resource cost that you want to set up.</span></span>

<span data-ttu-id="c9d43-143">**Bemærk**!</span><span class="sxs-lookup"><span data-stu-id="c9d43-143">**Note**.</span></span> <span data-ttu-id="c9d43-144">Åbn vinduet **Ressourcekostpriser** og udfyld felterne for at angive ressourcekostpriser, der kan anvendes til alle ressourcer og ressourcegrupper.</span><span class="sxs-lookup"><span data-stu-id="c9d43-144">To set up resource costs that will apply to all resources and resource groups, open the **Resource Costs** window and fill in the fields.</span></span>

## <a name="to-set-up-alternate-resource-prices"></a><span data-ttu-id="c9d43-145">Sådan angives ressourcepriser</span><span class="sxs-lookup"><span data-stu-id="c9d43-145">To set up alternate resource prices</span></span>
<span data-ttu-id="c9d43-146">Udover den pris, der er angivet på ressourcekortet, kan du oprette alternative priser for hver ressource.</span><span class="sxs-lookup"><span data-stu-id="c9d43-146">In addition to price specified on the resource card, you can set up alternate prices for each resource.</span></span> <span data-ttu-id="c9d43-147">Alternative priser kan være betingede.</span><span class="sxs-lookup"><span data-stu-id="c9d43-147">These alternate prices can be conditional.</span></span> <span data-ttu-id="c9d43-148">De kan være betinget af, om ressourcen anvendes med et bestemt job eller en bestemt arbejdstype.</span><span class="sxs-lookup"><span data-stu-id="c9d43-148">They can depend on whether the resource is used with a specific job or work type.</span></span>

1. <span data-ttu-id="c9d43-149">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Ressourcer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="c9d43-149">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resources**, and then choose the related link.</span></span>
2. <span data-ttu-id="c9d43-150">Vælg ressource, som du vil angive en eller flere alternative priser for, og vælg derefter handlingen **Priser**.</span><span class="sxs-lookup"><span data-stu-id="c9d43-150">Select the resource for that you want to set up one or more alternate prices for, and then choose the **Prices** action.</span></span>
3. <span data-ttu-id="c9d43-151">I vinduet **Ressourcepriser** skal du udfylde felterne på en linje efter behov.</span><span class="sxs-lookup"><span data-stu-id="c9d43-151">In the **Resource Prices** window, fill in the fields on a line as necessary.</span></span>
4. <span data-ttu-id="c9d43-152">Gentag trin 3 for hver alternativ ressourcepris, du vil oprette.</span><span class="sxs-lookup"><span data-stu-id="c9d43-152">Repeat step 3 for each alternate resource price that you want to set up.</span></span>

## <a name="see-also"></a><span data-ttu-id="c9d43-153">Se også</span><span class="sxs-lookup"><span data-stu-id="c9d43-153">See Also</span></span>
[<span data-ttu-id="c9d43-154">Konfigurere projektstyring</span><span class="sxs-lookup"><span data-stu-id="c9d43-154">Setting Up Project Management</span></span>](projects-setup-projects.md)  
[<span data-ttu-id="c9d43-155">Projektstyring</span><span class="sxs-lookup"><span data-stu-id="c9d43-155">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="c9d43-156">Finans</span><span class="sxs-lookup"><span data-stu-id="c9d43-156">Finance</span></span>](finance.md)  
<span data-ttu-id="c9d43-157">[Køb](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="c9d43-157">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="c9d43-158">[Salg](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="c9d43-158">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="c9d43-159">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c9d43-159">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
