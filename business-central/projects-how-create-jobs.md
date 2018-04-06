---
title: Oprette et sagskort for en sag og angive opgaver | Microsoft Docs
description: "Du kan oprette et sagskort, der viser sagsopgaver og planlægningslinjer, så det er nemmere at administrere status og budgetter for et nyt projekt."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, task
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: af8102b8f8ea51cbe0831388fab6d6bfc3a45101
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="create-jobs"></a><span data-ttu-id="90e2e-103">Oprette sager</span><span class="sxs-lookup"><span data-stu-id="90e2e-103">Create Jobs</span></span>
<span data-ttu-id="90e2e-104">Når du starter et nyt projekt, skal du oprette et sagskort med integrerede sagsopgaver og sagsplanlægningslinjer, opdelt i to niveauer.</span><span class="sxs-lookup"><span data-stu-id="90e2e-104">When you start a new project, you must create a job card with integrated job tasks and job planning lines, structured in two layers.</span></span>  

<span data-ttu-id="90e2e-105">Det første niveau består af sagsopgaver.</span><span class="sxs-lookup"><span data-stu-id="90e2e-105">The first layer consists of job tasks.</span></span> <span data-ttu-id="90e2e-106">Da al bogføring henviser til en sagsopgave, skal du oprette mindst én sagsopgave pr. sag.</span><span class="sxs-lookup"><span data-stu-id="90e2e-106">You must create at least one job task per job because all posting refers to a job task.</span></span> <span data-ttu-id="90e2e-107">Når sagen indeholder mindst én sagsopgave, kan du oprette sagsplanlægningslinjer og bogføre forbruget i sagen.</span><span class="sxs-lookup"><span data-stu-id="90e2e-107">Having at least one job task in your job enables you to set up job planning lines and to post consumption to the job.</span></span>

<span data-ttu-id="90e2e-108">Det andet lag består af sagsplanlægningslinjer, der angiver den detaljerede brug af ressourcer, varer og diverse regnskabsmæssige udgifter.</span><span class="sxs-lookup"><span data-stu-id="90e2e-108">The second layer consists of job planning lines, which specify the detailed use of resources, items and various general ledger expenses.</span></span>

<span data-ttu-id="90e2e-109">Den lagdelte struktur giver dig mulighed for at opdele sagen i mindre opgaver og dermed angive mere detaljerede oplysninger i budgetter, rekvisitioner og registreringer.</span><span class="sxs-lookup"><span data-stu-id="90e2e-109">The layer structure enables you to divide the job into smaller tasks, and therefore use more specific details in budgeting, quotes, and registration.</span></span> <span data-ttu-id="90e2e-110">Desuden får du indsigt i, hvordan en sag skrider frem.</span><span class="sxs-lookup"><span data-stu-id="90e2e-110">In addition, it gives you insight into how a job is progressing.</span></span> <span data-ttu-id="90e2e-111">Du kan f.eks. spore, om du opfylder udpegede milepæl, eller om du overholder tidsplanen for opfyldelse af forventninger til budgettet.</span><span class="sxs-lookup"><span data-stu-id="90e2e-111">For example, you can track whether you are meeting designated milestones or if you are on target to meet budget expectations.</span></span>

> [!NOTE]  
>   <span data-ttu-id="90e2e-112">Handlingen **Ny sag** i **Projektleder**-rollecenteret starter en assisteret opsætning, som vejleder dig gennem trinnene til oprettelse af integrerede opgaver og planlægningslinjer.</span><span class="sxs-lookup"><span data-stu-id="90e2e-112">The **New Job** action on the **Project Manager** Role Center launches an assisted setup that guides you through the steps of creating a job with integrated tasks and planning lines.</span></span> <span data-ttu-id="90e2e-113">Følgende fremgangsmåde beskriver, hvordan trinnene udføres manuelt.</span><span class="sxs-lookup"><span data-stu-id="90e2e-113">The following procedure describes how to perform the steps manually.</span></span>

## <a name="to-create-a-job-card"></a><span data-ttu-id="90e2e-114">Sådan oprettes et sagskort</span><span class="sxs-lookup"><span data-stu-id="90e2e-114">To create a job card</span></span>
<span data-ttu-id="90e2e-115">Du kan oprette et sagskort og derefter oprette sagsopgavelinjer og sagsplanlægningslinjer for det.</span><span class="sxs-lookup"><span data-stu-id="90e2e-115">You create a job card and then create job task lines and job planning lines for it.</span></span>

1. <span data-ttu-id="90e2e-116">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Sager**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="90e2e-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>  
2. <span data-ttu-id="90e2e-117">Vælg handlingen **Ny**, og udfyld derefter felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="90e2e-117">Choose the **New** action, and then fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="90e2e-118">For at angive sagen med oplysninger om andre sager skal du vælge handlingen **Kopier sag**, udfylde felterne efter behov, og derefter vælge knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="90e2e-118">To specify the job with information on other jobs, choose the **Copy Job** action, fill in the fields as necessary, and then choose the **OK** button.</span></span>

> [!NOTE]  
>   <span data-ttu-id="90e2e-119">Hvis du bruger timesedler i din sag, skal du også tildele en ansvarlig person.</span><span class="sxs-lookup"><span data-stu-id="90e2e-119">If you are using time sheets with your job, you must also designate a person responsible.</span></span> <span data-ttu-id="90e2e-120">Denne person kan godkende timesedler for medarbejderopgaver, der er knyttet til sagen.</span><span class="sxs-lookup"><span data-stu-id="90e2e-120">This person can approve time sheets for the employee tasks associated with the job.</span></span> <span data-ttu-id="90e2e-121">Der er flere oplysninger i [Konfigurere timesedler](projects-how-setup-time-sheets.md).</span><span class="sxs-lookup"><span data-stu-id="90e2e-121">For more information, see [Set Up Timesheets](projects-how-setup-time-sheets.md).</span></span>

## <a name="to-create-tasks-for-a-job"></a><span data-ttu-id="90e2e-122">Sådan oprettes opgaver for en sag</span><span class="sxs-lookup"><span data-stu-id="90e2e-122">To create tasks for a job</span></span>
<span data-ttu-id="90e2e-123">Når du opretter en sag, skal du også angive de forskellige opgaver, som sagen indeholder.</span><span class="sxs-lookup"><span data-stu-id="90e2e-123">A key part of creating a job is to specify the various tasks involved in the job.</span></span> <span data-ttu-id="90e2e-124">Det gør du ved at tilføje nye linjer i oversigtspanelet **Opgaver** i vinduet **Jobkort**, en opgave pr. linje.</span><span class="sxs-lookup"><span data-stu-id="90e2e-124">You do this by adding new lines on the **Tasks** FastTab in the **Job Card** window, one task per line.</span></span> <span data-ttu-id="90e2e-125">Hver sag skal have mindst én opgave.</span><span class="sxs-lookup"><span data-stu-id="90e2e-125">Every job must have at least one task.</span></span>

1. <span data-ttu-id="90e2e-126">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Sager**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="90e2e-126">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="90e2e-127">Åbn sagskortet for den relevante sag.</span><span class="sxs-lookup"><span data-stu-id="90e2e-127">Open the job card for a relevant job.</span></span>
3. <span data-ttu-id="90e2e-128">På oversigtspanelet **Opgaver** skal du udfylde felterne efter behov på en ny linje.</span><span class="sxs-lookup"><span data-stu-id="90e2e-128">On the **Tasks** FastTab, fill in the fields as necessary on a new line.</span></span>
4. <span data-ttu-id="90e2e-129">For at indrykke opgaver og oprette et hierarki, skal du vælge handlingen **Opgaver** og derefter vælge handlingen **Indryk sagsopgaver**.</span><span class="sxs-lookup"><span data-stu-id="90e2e-129">To indent tasks and create a hierarchy, Choose the **Tasks** action, the then choose **Indent Job Tasks** action.</span></span>
5. <span data-ttu-id="90e2e-130">Gentag trin 3 og 4 for alle de opgaver, du skal bruge for sagen.</span><span class="sxs-lookup"><span data-stu-id="90e2e-130">Repeat steps 3 and 4 for all the tasks that you need for the job.</span></span>
6. <span data-ttu-id="90e2e-131">For at angive sagsopgaverne med oplysninger om andre sagsopgaver skal du vælge handlingen **Kopier sagsopgaver fra**, udfylde felterne efter behov, og derefter vælge knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="90e2e-131">To specify the job tasks with information on other job tasks, choose the **Copy Job Tasks from** action, fill in the fields as necessary, and then choose the **OK** button.</span></span>

## <a name="to-create-planning-lines-for-a-job"></a><span data-ttu-id="90e2e-132">Sådan oprettes planlægningslinjer for en sag</span><span class="sxs-lookup"><span data-stu-id="90e2e-132">To create planning lines for a job</span></span>
<span data-ttu-id="90e2e-133">Du kan begrænse dine nye sagsopgaver på sagsplanlægningslinjer.</span><span class="sxs-lookup"><span data-stu-id="90e2e-133">You can refine your new job tasks on job planning lines.</span></span> <span data-ttu-id="90e2e-134">En planlægningslinje kan bruges til at hente alle oplysninger, du vil spore for en sag.</span><span class="sxs-lookup"><span data-stu-id="90e2e-134">A planning line can be used to capture any information that you want to track for a job.</span></span> <span data-ttu-id="90e2e-135">Du kan bruge planlægningslinjer til at tilføje oplysninger, f.eks. hvilke ressourcer der kræves, eller til at hente de varer, der er brug for til at udføre sagen.</span><span class="sxs-lookup"><span data-stu-id="90e2e-135">You can use planning lines to add information such as what resources are required or to capture what items are needed to perform the job.</span></span> <span data-ttu-id="90e2e-136">Hvis du f.eks. har til opgave at få kundens godkendelse af en sag, kan du knytte den pågældende opgave til planlægningslinjer for varer, f.eks. et møde med kunden og tildelelse af en ressource.</span><span class="sxs-lookup"><span data-stu-id="90e2e-136">For example, if you have a task to obtain customer approval of a job, you can associate that task with planning lines for items such as meeting with the customer and assigning a resource.</span></span>  

<span data-ttu-id="90e2e-137">En sagsplanlægningslinje han være en af følgende typer.</span><span class="sxs-lookup"><span data-stu-id="90e2e-137">A job planning line can have one of the following types.</span></span>  

| <span data-ttu-id="90e2e-138">Enhedstype</span><span class="sxs-lookup"><span data-stu-id="90e2e-138">Type</span></span> | <span data-ttu-id="90e2e-139">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="90e2e-139">Description</span></span> |
| --- | --- |
| <span data-ttu-id="90e2e-140">**Budget**</span><span class="sxs-lookup"><span data-stu-id="90e2e-140">**Budget**</span></span> |<span data-ttu-id="90e2e-141">Viser forventet forbrug og omkostninger i forbindelse med sagen, typisk i et projekt af typen tidspunkt og materialer.</span><span class="sxs-lookup"><span data-stu-id="90e2e-141">Provides estimated usage and costs for the job, typically in a time and materials type project.</span></span> <span data-ttu-id="90e2e-142">Planlægningslinjer af denne type kan ikke faktureres.</span><span class="sxs-lookup"><span data-stu-id="90e2e-142">Planning lines of this type cannot be invoiced.</span></span> |
| <span data-ttu-id="90e2e-143">**Fakturerbar**</span><span class="sxs-lookup"><span data-stu-id="90e2e-143">**Billable**</span></span> |<span data-ttu-id="90e2e-144">Viser forventet fakturering til kunden, typisk i et fast pris-projekt.</span><span class="sxs-lookup"><span data-stu-id="90e2e-144">Provides estimated invoicing to the customer, typically in a fixed price project.</span></span> |
| <span data-ttu-id="90e2e-145">**Både budget og fakturerbar**</span><span class="sxs-lookup"><span data-stu-id="90e2e-145">**Both Budget and Billable**</span></span> |<span data-ttu-id="90e2e-146">Viser budgetteret forbrug, der er lig med, hvad du vil fakturere.</span><span class="sxs-lookup"><span data-stu-id="90e2e-146">Provides budgeted usage equal to what you want to invoice.</span></span> |

<span data-ttu-id="90e2e-147">**Bemærk**!</span><span class="sxs-lookup"><span data-stu-id="90e2e-147">**Note**.</span></span> <span data-ttu-id="90e2e-148">Når du angiver oplysninger på sagsplanlægningslinjer, udfyldes omkostningsoplysninger automatisk.</span><span class="sxs-lookup"><span data-stu-id="90e2e-148">As you enter information on job planning lines, cost information is automatically filled in.</span></span> <span data-ttu-id="90e2e-149">Omkostning, pris og rabat for ressourcer og varer er f.eks. først baseret på de oplysninger, der er defineret på ressource- og varekort.</span><span class="sxs-lookup"><span data-stu-id="90e2e-149">For example, the cost, price, and discount for resources and items are initially based on the information that is defined on the resource and item cards.</span></span>

1. <span data-ttu-id="90e2e-150">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Sager**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="90e2e-150">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Jobs**, and then choose the related link.</span></span>
2. <span data-ttu-id="90e2e-151">Åbn et relevant sagskort.</span><span class="sxs-lookup"><span data-stu-id="90e2e-151">Open a relevant job card.</span></span>
3. <span data-ttu-id="90e2e-152">Vælg en sagsopgave, hvor feltet **Sagsopgavetype** indeholder **Bogføring**, og vælg derefter handlingen **Sagsplanlægningslinjer**.</span><span class="sxs-lookup"><span data-stu-id="90e2e-152">Select a job task for which the **Job Task Type** field contains **Posting**, and then choose the **Job Planning Lines** action.</span></span>  
4. <span data-ttu-id="90e2e-153">I vinduet **Sagsplanlægningslinjer** skal du udfylde felterne på en ny linje efter behov.</span><span class="sxs-lookup"><span data-stu-id="90e2e-153">In the **Job Planning Lines** window, on a new line, fill in the fields as necessary.</span></span>
5. <span data-ttu-id="90e2e-154">Gentag trin 3 og 4 for alle planlægninglinjer, du skal bruge for sagsopgaven.</span><span class="sxs-lookup"><span data-stu-id="90e2e-154">Repeat steps 3 and 4 for all planning lines that you need for the job task.</span></span>

## <a name="see-also"></a><span data-ttu-id="90e2e-155">Se også</span><span class="sxs-lookup"><span data-stu-id="90e2e-155">See Also</span></span>
[<span data-ttu-id="90e2e-156">Projektstyring</span><span class="sxs-lookup"><span data-stu-id="90e2e-156">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="90e2e-157">Finans</span><span class="sxs-lookup"><span data-stu-id="90e2e-157">Finance</span></span>](finance.md)  
<span data-ttu-id="90e2e-158">[Køb](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="90e2e-158">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="90e2e-159">[Salg](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="90e2e-159">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="90e2e-160">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="90e2e-160">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
