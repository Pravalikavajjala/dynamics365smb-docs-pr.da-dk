---
title: "Oversigt over opgaver til allokering af omkostninger og indtægter | Microsoft Docs"
description: "Beskriver de opgaver, du skal udføre for at allokere en post i en finanskladde til flere forskellige konti, når du bogfører kladden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 31f8d40d5a8cf8d190f4a6cb655f09ca72f3e070
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="allocate-costs-and-income"></a><span data-ttu-id="5b46b-103">Fordele omkostninger og indtægter</span><span class="sxs-lookup"><span data-stu-id="5b46b-103">Allocate Costs and Income</span></span>
<span data-ttu-id="5b46b-104">Du kan allokere en post i en finanskladde til flere forskellige konti, når du bogfører kladden.</span><span class="sxs-lookup"><span data-stu-id="5b46b-104">You can allocate an entry in a general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="5b46b-105">Allokeringen kan foretages på tre forskellige måder:</span><span class="sxs-lookup"><span data-stu-id="5b46b-105">The allocation can be made by three different methods:</span></span>

* <span data-ttu-id="5b46b-106">Antal</span><span class="sxs-lookup"><span data-stu-id="5b46b-106">Quantity</span></span>
* <span data-ttu-id="5b46b-107">Procent (%)</span><span class="sxs-lookup"><span data-stu-id="5b46b-107">Percentage (%)</span></span>
* <span data-ttu-id="5b46b-108">Beløb</span><span class="sxs-lookup"><span data-stu-id="5b46b-108">Amount</span></span>

<span data-ttu-id="5b46b-109">Allokeringsfunktionen kan bruges sammen med finansgentagelseskladder og i anlægskladder.</span><span class="sxs-lookup"><span data-stu-id="5b46b-109">The allocation features can be used with recurring general journals and in fixed assets journals.</span></span>
<!--You can also distribute the cost or revenue of a line to an intercompany partner when you post a sales or purchase document. When you post the document, a line will be posted in your general journal, and a corresponding line will be created in the intercompany outbox.-->

<span data-ttu-id="5b46b-110">I følgende procedurer beskrives, hvordan du forbereder at allokere omkostninger i en finansgentagelseskladde ved at definere fordelingsnøgler.</span><span class="sxs-lookup"><span data-stu-id="5b46b-110">The following procedures describe how to prepare to allocate costs in a recurring general journal by defining allocation keys.</span></span> <span data-ttu-id="5b46b-111">Når der er defineret fordelingsnøgler, skal du udfylde og bogføre kladden ligesom alle andre finansgentagelseskladder.</span><span class="sxs-lookup"><span data-stu-id="5b46b-111">When allocation keys are defined, you complete and post the journal like any other recurring general journal.</span></span> <span data-ttu-id="5b46b-112">Du kan finde flere oplysninger under [Arbejde med finanskladder](ui-work-general-journals.md).</span><span class="sxs-lookup"><span data-stu-id="5b46b-112">For more information, see [Working with General Journals](ui-work-general-journals.md).</span></span>

## <a name="to-set-up-allocation-keys"></a><span data-ttu-id="5b46b-113">Sådan konfigureres fordelingsnøgler</span><span class="sxs-lookup"><span data-stu-id="5b46b-113">To set up allocation keys</span></span>
<span data-ttu-id="5b46b-114">Du kan allokere en post i en finansgentagelseskladde til flere forskellige konti, når du bogfører kladden.</span><span class="sxs-lookup"><span data-stu-id="5b46b-114">You can allocate an entry in a recurring general journal to several different accounts when you post the journal.</span></span> <span data-ttu-id="5b46b-115">Allokeringen kan foretages efter antal, procent eller beløb.</span><span class="sxs-lookup"><span data-stu-id="5b46b-115">The allocation can be made by quantity, percentage, or amount.</span></span>
1. <span data-ttu-id="5b46b-116">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Finansgentagelseskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="5b46b-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="5b46b-117">Vælg feltet **Kladdenavn** for at åbne vinduet **Finanskladdenavne**.</span><span class="sxs-lookup"><span data-stu-id="5b46b-117">Choose the **Batch Name** field to open the **General Journal Batches** window.</span></span>
3. <span data-ttu-id="5b46b-118">Du kan ændre fordelinger for et eksisterende navn på listen eller oprette et nyt navn med fordelinger.</span><span class="sxs-lookup"><span data-stu-id="5b46b-118">You can either modify allocations on an existing batch in the list or create a new batch with allocations.</span></span>
   * <span data-ttu-id="5b46b-119">Du kan oprette en ny kladde ved at vælge handlingen **Ny** og gå til næste trin.</span><span class="sxs-lookup"><span data-stu-id="5b46b-119">To create a new batch, choose the **New** action, and go to the next step.</span></span>
   * <span data-ttu-id="5b46b-120">Vælg kladden og gå til trin 7, hvis du vil ændre fordelingerne af en eksisterende kladde.</span><span class="sxs-lookup"><span data-stu-id="5b46b-120">To change the allocations of an existing journal, select the journal and go to step 7.</span></span>    
4. <span data-ttu-id="5b46b-121">Angiv navnet på en ny kladde i feltet **Navn**, f.eks. Rengøring.</span><span class="sxs-lookup"><span data-stu-id="5b46b-121">In the **Name** field, enter a name for the batch, such as CLEANING.</span></span> <span data-ttu-id="5b46b-122">Angiv en beskrivelse i feltet **Beskrivelse**, f.eks. Kladde til rengøringsudgifter.</span><span class="sxs-lookup"><span data-stu-id="5b46b-122">In the **Description** field, enter a description, such as Cleaning Expenses Journal.</span></span>
5. <span data-ttu-id="5b46b-123">Når du er færdig, skal du lukke vinduet.</span><span class="sxs-lookup"><span data-stu-id="5b46b-123">When you are done, close the window.</span></span> <span data-ttu-id="5b46b-124">Der åbnes en ny tom gentagelseskladde.</span><span class="sxs-lookup"><span data-stu-id="5b46b-124">A new, empty recurring journal opens.</span></span>
6. <span data-ttu-id="5b46b-125">Udfyld felterne på linjen.</span><span class="sxs-lookup"><span data-stu-id="5b46b-125">Fill in the fields on the line.</span></span>
7. <span data-ttu-id="5b46b-126">Vælg handlingen **Fordelinger**.</span><span class="sxs-lookup"><span data-stu-id="5b46b-126">Choose the **Allocations** action.</span></span>
8. <span data-ttu-id="5b46b-127">Tilføj en linje for hver fordeling.</span><span class="sxs-lookup"><span data-stu-id="5b46b-127">Add a line for each allocation.</span></span> <span data-ttu-id="5b46b-128">Du skal udfylde et af følgende felter: **Allokeringspct.**, **Andel i antal** eller **Beløb**.</span><span class="sxs-lookup"><span data-stu-id="5b46b-128">You must fill in either the **Allocation %**, **Allocation Quantity**, or **Amount** field.</span></span> <span data-ttu-id="5b46b-129">Du skal udfylde feltet **Kontonr.** og desuden felterne for globale dimensioner, hvis du allokerer transaktionen mellem globale dimensioner.</span><span class="sxs-lookup"><span data-stu-id="5b46b-129">You must also fill in the **Account No.** field and, if you are allocating the transaction among global dimensions, the global dimension fields.</span></span>
9. <span data-ttu-id="5b46b-130">Hvis du angiver en procent på en linje, beregnes beløbet i feltet **Beløb** automatisk.</span><span class="sxs-lookup"><span data-stu-id="5b46b-130">If you enter a percentage on a line, the amount in the **Amount** field is calculated automatically.</span></span> <span data-ttu-id="5b46b-131">Disse beløb har det modsatte tegn af tegnet fra det totale beløb i feltet **Beløb** i gentagelseskladden.</span><span class="sxs-lookup"><span data-stu-id="5b46b-131">These amounts have the opposite sign from the total amount in the **Amount** field in the recurring journal.</span></span>
10. <span data-ttu-id="5b46b-132">Når du har angivet linjerne med fordelinger, skal du vælge **OK** for at gå tilbage til vinduet **Finansgentagelseskladde**.</span><span class="sxs-lookup"><span data-stu-id="5b46b-132">After entering the allocations lines, choose **OK** to return to the **Recurring General Journal** window.</span></span> <span data-ttu-id="5b46b-133">Feltet **Fordelt beløb (RV)** udfyldes og svarer til feltet **Beløb**.</span><span class="sxs-lookup"><span data-stu-id="5b46b-133">The **Allocated Amt. (USD)** field is filled in and matches the **Amount** field.</span></span>
11. <span data-ttu-id="5b46b-134">Bogfør journalen.</span><span class="sxs-lookup"><span data-stu-id="5b46b-134">Post the journal.</span></span>

## <a name="to-change-an-allocation-key-that-has-already-been-set-up"></a><span data-ttu-id="5b46b-135">Sådan ændres en fordelingsnøgle, der allerede er oprettet</span><span class="sxs-lookup"><span data-stu-id="5b46b-135">To change an allocation key that has already been set up</span></span>
1. <span data-ttu-id="5b46b-136">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Finansgentagelseskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="5b46b-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Recurring General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="5b46b-137">Vælg kladden med allokeringen i vinduet **Finansgentagelseskladde**.</span><span class="sxs-lookup"><span data-stu-id="5b46b-137">In the **Recurring General Journal** window, select the journal with the allocation.</span></span>
3. <span data-ttu-id="5b46b-138">Vælg linjen med fordelingen og vælg derefter handlingen **Fordelinger**.</span><span class="sxs-lookup"><span data-stu-id="5b46b-138">Choose the line with the allocation, and then choose **Allocations** action.</span></span>
4. <span data-ttu-id="5b46b-139">Rediger de relevante felter, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b46b-139">Change the relevant fields, and then choose the **OK** button.</span></span>

## <a name="see-also"></a><span data-ttu-id="5b46b-140">Se også</span><span class="sxs-lookup"><span data-stu-id="5b46b-140">See Also</span></span>
[<span data-ttu-id="5b46b-141">Afslutning af år og perioder</span><span class="sxs-lookup"><span data-stu-id="5b46b-141">Closing Years and Periods</span></span>](year-close-years-periods.md)  
<span data-ttu-id="5b46b-142">[Arbejde med finanskladder](ui-work-general-journals.md)  </span><span class="sxs-lookup"><span data-stu-id="5b46b-142">[Working with General Journals](ui-work-general-journals.md)  </span></span>  
<span data-ttu-id="5b46b-143">[Bogføring af dokumenter og kladder](ui-post-documents-journals.md)  </span><span class="sxs-lookup"><span data-stu-id="5b46b-143">[Posting Documents and Journals](ui-post-documents-journals.md)  </span></span>  
<span data-ttu-id="5b46b-144">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5b46b-144">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
