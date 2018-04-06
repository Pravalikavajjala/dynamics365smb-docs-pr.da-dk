---
title: "Åbn vareposter"
description: "Få mere at vide om, hvorfor lagerniveauet er nul, selvom der findes åbne vareposter."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/23/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e25721b0c79a87f4201314a0f3556f969a110e18
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-known-item-application-issue"></a><span data-ttu-id="01801-103">Designoplysninger: Kendt problem med vareudligning</span><span class="sxs-lookup"><span data-stu-id="01801-103">Design Details: Known Item Application Issue</span></span>
<span data-ttu-id="01801-104">Denne artikel vedrører et problem, hvor lagerniveauet er nul, selvom der findes åbne vareposter [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="01801-104">This article addresses an issue where the inventory level is zero although open item ledger entries exist in  [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="01801-105">Artiklen starter ved at angive typiske symptomer på problemet, efterfulgt af de grundlæggende oplysninger om vareudligning til at understøtte de beskrevne årsager til problemet.</span><span class="sxs-lookup"><span data-stu-id="01801-105">The article starts by listing typical symptoms of the issue, followed by the basics of item application to support the described reasons for this issue.</span></span> <span data-ttu-id="01801-106">I slutningen af artiklen er en løsning til at løse sådanne åbne vareposter.</span><span class="sxs-lookup"><span data-stu-id="01801-106">At the end of the article is a workaround to address such open item ledger entries.</span></span>  

## <a name="symptoms-of-the-issue"></a><span data-ttu-id="01801-107">Symptomer på problemet</span><span class="sxs-lookup"><span data-stu-id="01801-107">Symptoms of the Issue</span></span>  
 <span data-ttu-id="01801-108">De typiske symptomer på problemet med nul lager, selvom der findes åbne vareposter, er følgende:</span><span class="sxs-lookup"><span data-stu-id="01801-108">Typical symptoms of the issue with zero inventory although open item ledger entries exist are the following:</span></span>  

-   <span data-ttu-id="01801-109">Du får vist følgende meddelelse, når du forsøger at lukke en lagerperiode: "Lageret kan ikke lukkes, fordi der er negativt lager for én eller flere varer".</span><span class="sxs-lookup"><span data-stu-id="01801-109">The following message when you try to close an inventory period: “The inventory cannot be closed because there is negative inventory for one or more items.”</span></span>  

-   <span data-ttu-id="01801-110">En situation med en varepost, hvor både en udgående varepost og dens relaterede indgående varepost er åben.</span><span class="sxs-lookup"><span data-stu-id="01801-110">An item ledger entry situation where both an outbound item ledger entry and its related inbound item ledger entry are open.</span></span>  

     <span data-ttu-id="01801-111">Se følgende eksempel på en situation med en varepost.</span><span class="sxs-lookup"><span data-stu-id="01801-111">See the following example of an item ledger entry situation.</span></span>  

     |<span data-ttu-id="01801-112">Løbenummer</span><span class="sxs-lookup"><span data-stu-id="01801-112">Entry No.</span></span>|<span data-ttu-id="01801-113">Bogføringsdato</span><span class="sxs-lookup"><span data-stu-id="01801-113">Posting Date</span></span>|<span data-ttu-id="01801-114">Postens type</span><span class="sxs-lookup"><span data-stu-id="01801-114">Entry Type</span></span>|<span data-ttu-id="01801-115">Dokumenttype</span><span class="sxs-lookup"><span data-stu-id="01801-115">Document Type</span></span>|<span data-ttu-id="01801-116">Bilagsnr.</span><span class="sxs-lookup"><span data-stu-id="01801-116">Document No.</span></span>|<span data-ttu-id="01801-117">Varenr.</span><span class="sxs-lookup"><span data-stu-id="01801-117">Item No.</span></span>|<span data-ttu-id="01801-118">Lokationskode</span><span class="sxs-lookup"><span data-stu-id="01801-118">Location Code</span></span>|<span data-ttu-id="01801-119">Antal</span><span class="sxs-lookup"><span data-stu-id="01801-119">Quantity</span></span>|<span data-ttu-id="01801-120">Kostbeløb (faktisk)</span><span class="sxs-lookup"><span data-stu-id="01801-120">Cost Amount (Actual)</span></span>|<span data-ttu-id="01801-121">Faktureret antal</span><span class="sxs-lookup"><span data-stu-id="01801-121">Invoiced Quantity</span></span>|<span data-ttu-id="01801-122">Restantal</span><span class="sxs-lookup"><span data-stu-id="01801-122">Remaining Quantity</span></span>|<span data-ttu-id="01801-123">Åbn</span><span class="sxs-lookup"><span data-stu-id="01801-123">Open</span></span>|  
     |---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|  
     |<span data-ttu-id="01801-124">333</span><span class="sxs-lookup"><span data-stu-id="01801-124">333</span></span>|<span data-ttu-id="01801-125">28-01-2018</span><span class="sxs-lookup"><span data-stu-id="01801-125">01/28/2018</span></span>|<span data-ttu-id="01801-126">Salg</span><span class="sxs-lookup"><span data-stu-id="01801-126">Sale</span></span>|<span data-ttu-id="01801-127">Salgsleverance</span><span class="sxs-lookup"><span data-stu-id="01801-127">Sales Shipment</span></span>|<span data-ttu-id="01801-128">102043</span><span class="sxs-lookup"><span data-stu-id="01801-128">102043</span></span>|<span data-ttu-id="01801-129">TEST</span><span class="sxs-lookup"><span data-stu-id="01801-129">TEST</span></span>|<span data-ttu-id="01801-130">BLÅ</span><span class="sxs-lookup"><span data-stu-id="01801-130">BLUE</span></span>|<span data-ttu-id="01801-131">-1</span><span class="sxs-lookup"><span data-stu-id="01801-131">-1</span></span>|<span data-ttu-id="01801-132">-10</span><span class="sxs-lookup"><span data-stu-id="01801-132">-10</span></span>|<span data-ttu-id="01801-133">-1</span><span class="sxs-lookup"><span data-stu-id="01801-133">-1</span></span>|<span data-ttu-id="01801-134">-1</span><span class="sxs-lookup"><span data-stu-id="01801-134">-1</span></span>|<span data-ttu-id="01801-135">Ja</span><span class="sxs-lookup"><span data-stu-id="01801-135">Yes</span></span>|  
     |<span data-ttu-id="01801-136">334</span><span class="sxs-lookup"><span data-stu-id="01801-136">334</span></span>|<span data-ttu-id="01801-137">28-01-2018</span><span class="sxs-lookup"><span data-stu-id="01801-137">01/28/2018</span></span>|<span data-ttu-id="01801-138">Salg</span><span class="sxs-lookup"><span data-stu-id="01801-138">Sale</span></span>|<span data-ttu-id="01801-139">Salgsleverance</span><span class="sxs-lookup"><span data-stu-id="01801-139">Sales Shipment</span></span>|<span data-ttu-id="01801-140">102043</span><span class="sxs-lookup"><span data-stu-id="01801-140">102043</span></span>|<span data-ttu-id="01801-141">TEST</span><span class="sxs-lookup"><span data-stu-id="01801-141">TEST</span></span>|<span data-ttu-id="01801-142">BLÅ</span><span class="sxs-lookup"><span data-stu-id="01801-142">BLUE</span></span>|<span data-ttu-id="01801-143">1</span><span class="sxs-lookup"><span data-stu-id="01801-143">1</span></span>|<span data-ttu-id="01801-144">10</span><span class="sxs-lookup"><span data-stu-id="01801-144">10</span></span>|<span data-ttu-id="01801-145">1</span><span class="sxs-lookup"><span data-stu-id="01801-145">1</span></span>|<span data-ttu-id="01801-146">1</span><span class="sxs-lookup"><span data-stu-id="01801-146">1</span></span>|<span data-ttu-id="01801-147">Ja</span><span class="sxs-lookup"><span data-stu-id="01801-147">Yes</span></span>|  

<!--![Why is inventory zero 1](media/helene/TechArticleInventoryZero1.png "Whyisinventoryzero\_1")-->

## <a name="basics-of-item-application"></a><span data-ttu-id="01801-148">Grundlæggende oplysninger om vareudligning</span><span class="sxs-lookup"><span data-stu-id="01801-148">Basics of Item Application</span></span>  
 <span data-ttu-id="01801-149">Der oprettes en vareudligningspost for hver lagertransaktion for at kæde omkostningsmodtageren sammen med omkostningskilden, så omkostningerne kan videresendes i henhold til kostmetoden.</span><span class="sxs-lookup"><span data-stu-id="01801-149">An item application entry is created for every inventory transaction to link the cost recipient to its cost source so that the cost can be forwarded according to the costing method.</span></span> <span data-ttu-id="01801-150">Du kan finde flere oplysninger i [Designoplysninger: Vareudligning](design-details-item-application.md).</span><span class="sxs-lookup"><span data-stu-id="01801-150">For more information, see [Design Details: Item Application](design-details-item-application.md).</span></span>  

-   <span data-ttu-id="01801-151">For en indgående varepost oprettes vareudligningsposten, når vareposten oprettes.</span><span class="sxs-lookup"><span data-stu-id="01801-151">For an inbound item ledger entry, the item application entry is created when the item ledger entry is created.</span></span>  

-   <span data-ttu-id="01801-152">For en udgående varepost oprettes vareudligningsposten, når finansposten bogføres, hvis der er en åben indgående varepost med et disponibelt antal, den kan anvendes på.</span><span class="sxs-lookup"><span data-stu-id="01801-152">For an outbound item ledger entry, the item application entry is created when the item ledger entry is posted, IF there is an open inbound item ledger entry with available quantity that it can apply to.</span></span> <span data-ttu-id="01801-153">Hvis der ikke er nogen åben indgående varepost, som den kan anvendes på, så forbliver den udgående varepost åben, indtil der posteres en indgående varepost, som den kan anvendes på.</span><span class="sxs-lookup"><span data-stu-id="01801-153">If there is no open inbound item ledger entry that it can apply to, then the outbound item ledger entry remains open until an inbound item ledger entry that it can apply to is posted.</span></span>  

 <span data-ttu-id="01801-154">Der er to typer af vareudligning:</span><span class="sxs-lookup"><span data-stu-id="01801-154">There are two types of item application:</span></span>  

-   <span data-ttu-id="01801-155">Mængdeudligning</span><span class="sxs-lookup"><span data-stu-id="01801-155">Quantity Application</span></span>  

-   <span data-ttu-id="01801-156">Kostprisudligning</span><span class="sxs-lookup"><span data-stu-id="01801-156">Cost Application</span></span>  

### <a name="quantity-application"></a><span data-ttu-id="01801-157">Mængdeudligning</span><span class="sxs-lookup"><span data-stu-id="01801-157">Quantity Application</span></span>  
 <span data-ttu-id="01801-158">Mængdeudligninger foretages for alle lagertransaktioner, og de oprettes automatisk eller manuelt i særlige processer.</span><span class="sxs-lookup"><span data-stu-id="01801-158">Quantity applications are made for all inventory transactions and are created automatically, or manually in special processes.</span></span> <span data-ttu-id="01801-159">Når de foretages manuelt, kaldes mængdeudligninger for fast udligning.</span><span class="sxs-lookup"><span data-stu-id="01801-159">When made manually, quantity applications are referred to as fixed application.</span></span>  

 <span data-ttu-id="01801-160">I følgende diagram vises, hvordan mængdeudligninger foretages.</span><span class="sxs-lookup"><span data-stu-id="01801-160">The following diagram shows how quantity applications are made.</span></span>  

<span data-ttu-id="01801-161">![Hvorfor er lageret nul 2](media/helene/TechArticleInventoryZero2.png "Whyisinventoryzero\_2")</span><span class="sxs-lookup"><span data-stu-id="01801-161">![Why is inventory zero 2](media/helene/TechArticleInventoryZero2.png "Whyisinventoryzero\_2")</span></span>

 <span data-ttu-id="01801-162">Bemærk ovenfor, at vareposten 1 (køb) både er leverandør af varen og omkostningskilden til den udlignende varepost, varepost 2 (salg).</span><span class="sxs-lookup"><span data-stu-id="01801-162">Notice above that item ledger entry 1 (Purchase) is both the supplier of the item and the cost source to the applied item ledger entry, item ledger entry 2 (Sale).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="01801-163">Hvis den udgående varepost værdiansættes fra gennemsnitlige kostpris, er den anvendte indgående varepost ikke den entydige omkostningskilde.</span><span class="sxs-lookup"><span data-stu-id="01801-163">If the outbound item ledger entry is valued by average cost, then the applied inbound item ledger entry is not the unique cost source.</span></span> <span data-ttu-id="01801-164">Den spiller blot en rolle i beregningen af den gennemsnitlige kostpris for perioden.</span><span class="sxs-lookup"><span data-stu-id="01801-164">It merely plays a part in the calculation of the average cost of the period.</span></span>  

### <a name="cost-application"></a><span data-ttu-id="01801-165">Kostprisudligning</span><span class="sxs-lookup"><span data-stu-id="01801-165">Cost Application</span></span>  
<span data-ttu-id="01801-166">Kostprisudligninger oprettes kun for indgående transaktioner, hvor feltet **Udlign fra-varepost** er udfyldt for at oprette en fast udligning.</span><span class="sxs-lookup"><span data-stu-id="01801-166">Cost applications are only created for inbound transactions where the **Appl.-from Item Entry** field is filled to provide a fixed application.</span></span> <span data-ttu-id="01801-167">Dette sker typisk i forbindelse med en salgskreditnota og et scenarie med annullering af leverance.</span><span class="sxs-lookup"><span data-stu-id="01801-167">This typically happens in connection with a sales credit memo or an undo shipment scenario.</span></span> <span data-ttu-id="01801-168">Kostprisudligningen sikre, at varen går ind på lageret igen med samme kostpris, som da den blev leveret.</span><span class="sxs-lookup"><span data-stu-id="01801-168">The cost application ensures that the item re-enters inventory with the same cost as when it was shipped.</span></span>  

<span data-ttu-id="01801-169">I følgende diagram vises, hvordan kostprisudligninger foretages.</span><span class="sxs-lookup"><span data-stu-id="01801-169">The following diagram shows how cost applications are made.</span></span>  

|<span data-ttu-id="01801-170">Løbenummer</span><span class="sxs-lookup"><span data-stu-id="01801-170">Entry No.</span></span>|<span data-ttu-id="01801-171">Bogføringsdato</span><span class="sxs-lookup"><span data-stu-id="01801-171">Posting Date</span></span>|<span data-ttu-id="01801-172">Postens type</span><span class="sxs-lookup"><span data-stu-id="01801-172">Entry Type</span></span>|<span data-ttu-id="01801-173">Dokumenttype</span><span class="sxs-lookup"><span data-stu-id="01801-173">Document Type</span></span>|<span data-ttu-id="01801-174">Bilagsnr.</span><span class="sxs-lookup"><span data-stu-id="01801-174">Document No.</span></span>|<span data-ttu-id="01801-175">Varenr.</span><span class="sxs-lookup"><span data-stu-id="01801-175">Item No.</span></span>|<span data-ttu-id="01801-176">Lokationskode</span><span class="sxs-lookup"><span data-stu-id="01801-176">Location Code</span></span>|<span data-ttu-id="01801-177">Antal</span><span class="sxs-lookup"><span data-stu-id="01801-177">Quantity</span></span>|<span data-ttu-id="01801-178">Kostbeløb (faktisk)</span><span class="sxs-lookup"><span data-stu-id="01801-178">Cost Amount (Actual)</span></span>|<span data-ttu-id="01801-179">Faktureret antal</span><span class="sxs-lookup"><span data-stu-id="01801-179">Invoiced Quantity</span></span>|<span data-ttu-id="01801-180">Restantal</span><span class="sxs-lookup"><span data-stu-id="01801-180">Remaining Quantity</span></span>|<span data-ttu-id="01801-181">Åbn</span><span class="sxs-lookup"><span data-stu-id="01801-181">Open</span></span>|  
|---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|  
|<span data-ttu-id="01801-182">333</span><span class="sxs-lookup"><span data-stu-id="01801-182">333</span></span>|<span data-ttu-id="01801-183">28-01-2018</span><span class="sxs-lookup"><span data-stu-id="01801-183">01/28/2018</span></span>|<span data-ttu-id="01801-184">Salg</span><span class="sxs-lookup"><span data-stu-id="01801-184">Sale</span></span>|<span data-ttu-id="01801-185">Salgsleverance</span><span class="sxs-lookup"><span data-stu-id="01801-185">Sales Shipment</span></span>|<span data-ttu-id="01801-186">102043</span><span class="sxs-lookup"><span data-stu-id="01801-186">102043</span></span>|<span data-ttu-id="01801-187">TEST</span><span class="sxs-lookup"><span data-stu-id="01801-187">TEST</span></span>|<span data-ttu-id="01801-188">BLÅ</span><span class="sxs-lookup"><span data-stu-id="01801-188">BLUE</span></span>|<span data-ttu-id="01801-189">-1</span><span class="sxs-lookup"><span data-stu-id="01801-189">-1</span></span>|<span data-ttu-id="01801-190">-10</span><span class="sxs-lookup"><span data-stu-id="01801-190">-10</span></span>|<span data-ttu-id="01801-191">-1</span><span class="sxs-lookup"><span data-stu-id="01801-191">-1</span></span>|<span data-ttu-id="01801-192">-1</span><span class="sxs-lookup"><span data-stu-id="01801-192">-1</span></span>|<span data-ttu-id="01801-193">Ja</span><span class="sxs-lookup"><span data-stu-id="01801-193">Yes</span></span>|  
|<span data-ttu-id="01801-194">334</span><span class="sxs-lookup"><span data-stu-id="01801-194">334</span></span>|<span data-ttu-id="01801-195">28-01-2018</span><span class="sxs-lookup"><span data-stu-id="01801-195">01/28/2018</span></span>|<span data-ttu-id="01801-196">Salg</span><span class="sxs-lookup"><span data-stu-id="01801-196">Sale</span></span>|<span data-ttu-id="01801-197">Salgsleverance</span><span class="sxs-lookup"><span data-stu-id="01801-197">Sales Shipment</span></span>|<span data-ttu-id="01801-198">102043</span><span class="sxs-lookup"><span data-stu-id="01801-198">102043</span></span>|<span data-ttu-id="01801-199">TEST</span><span class="sxs-lookup"><span data-stu-id="01801-199">TEST</span></span>|<span data-ttu-id="01801-200">BLÅ</span><span class="sxs-lookup"><span data-stu-id="01801-200">BLUE</span></span>|<span data-ttu-id="01801-201">1</span><span class="sxs-lookup"><span data-stu-id="01801-201">1</span></span>|<span data-ttu-id="01801-202">10</span><span class="sxs-lookup"><span data-stu-id="01801-202">10</span></span>|<span data-ttu-id="01801-203">1</span><span class="sxs-lookup"><span data-stu-id="01801-203">1</span></span>|<span data-ttu-id="01801-204">1</span><span class="sxs-lookup"><span data-stu-id="01801-204">1</span></span>|<span data-ttu-id="01801-205">Ja</span><span class="sxs-lookup"><span data-stu-id="01801-205">Yes</span></span>|  
<!--![Why is inventory zero 3](media/helene/TechArticleInventoryZero3.png "Whyisinventoryzero\_3")-->

 <span data-ttu-id="01801-206">Bemærk over den indgående varepost 3 (salgsreturvareordre) er en omkostningsmodtager for den oprindelige udgående varepost 2 (salg).</span><span class="sxs-lookup"><span data-stu-id="01801-206">Notice above that inbound item ledger 3 (Sales Return) is a cost recipient for the original outbound item ledger entry 2 (Sale).</span></span>  

## <a name="illustration-of-a-basic-cost-flow"></a><span data-ttu-id="01801-207">Illustration af et grundlæggende omkostningsflow</span><span class="sxs-lookup"><span data-stu-id="01801-207">Illustration of a Basic Cost Flow</span></span>  
 <span data-ttu-id="01801-208">Forudsæt et komplet omkostningsflow, hvor en vare modtages, leveres og faktureres og returneres med nøjagtig\-kostpristilbageførsel og derefter sendes igen.</span><span class="sxs-lookup"><span data-stu-id="01801-208">Assume a complete cost flow where an item is received, is shipped and invoiced, is returned with exact\-cost reversal, and is shipped again.</span></span>  

 <span data-ttu-id="01801-209">I følgende diagram illustreres omkostningsflowet.</span><span class="sxs-lookup"><span data-stu-id="01801-209">The following diagram illustrates the cost flow.</span></span>  

<span data-ttu-id="01801-210">![Hvorfor er lageret nul 4](media/helene/TechArticleInventoryZero4.png "Whyisinventoryzero\_4")</span><span class="sxs-lookup"><span data-stu-id="01801-210">![Why is inventory zero 4](media/helene/TechArticleInventoryZero4.png "Whyisinventoryzero\_4")</span></span>

 <span data-ttu-id="01801-211">Bemærk over kostprisen overføres til vareposten 2 (salg) og derefter til vareposten 3 (salgsreturvareordre), og til sidst til vareposten 4 (salg 2).</span><span class="sxs-lookup"><span data-stu-id="01801-211">Notice above that the cost is forwarded to item ledger entry 2 (Sale), then to item ledger entry 3 (Sales Return), and finally to item ledger entry 4 (Sale 2).</span></span>  

## <a name="reasons-for-the-issue"></a><span data-ttu-id="01801-212">Årsager til problemet</span><span class="sxs-lookup"><span data-stu-id="01801-212">Reasons for the Issue</span></span>  
 <span data-ttu-id="01801-213">Problemet med nul lager, selvom der findes åbne vareposter, kan være forårsaget af følgende scenarier:</span><span class="sxs-lookup"><span data-stu-id="01801-213">The issue with zero inventory although open item ledger entries exist can be caused by the following scenarios:</span></span>  

-   <span data-ttu-id="01801-214">Scenarie 1: En leverance og en faktura bogføres, selvom varen ikke er tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="01801-214">Scenario 1: A shipment and invoice is posted although the item is not available.</span></span> <span data-ttu-id="01801-215">Bogføringen tilbageføres derefter med præcis kostprisudligning med en salgskreditnota.</span><span class="sxs-lookup"><span data-stu-id="01801-215">The posting is then exact-cost reversed with a sales credit memo.</span></span>  

-   <span data-ttu-id="01801-216">Scenarie 2: En leverance bogføres, selvom varen ikke er tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="01801-216">Scenario 2: A shipment is posted although the item is not available.</span></span> <span data-ttu-id="01801-217">Bogføring annulleres derefter med funktionen Annuller leverance.</span><span class="sxs-lookup"><span data-stu-id="01801-217">The posting is then undone with the Undo Shipment function.</span></span>  

 <span data-ttu-id="01801-218">I følgende diagram illustreres, hvordan vareudligninger foretages i begge scenarier.</span><span class="sxs-lookup"><span data-stu-id="01801-218">The following diagram illustrates how item applications are made in both scenarios.</span></span>  

<span data-ttu-id="01801-219">![Hvorfor er lageret nul 6](media/helene/TechArticleInventoryZero6.png "Whyisinventoryzero\_6")</span><span class="sxs-lookup"><span data-stu-id="01801-219">![Why is inventory zero 6](media/helene/TechArticleInventoryZero6.png "Whyisinventoryzero\_6")</span></span>  

 <span data-ttu-id="01801-220">Bemærk, at der foretages en kostprisudligning (vises med blå pil) for at sikre, at post 2 (salgsreturvareordre) tildeles samme omkostninger som den varepost, den udligner, varepost 1 (salg 1).</span><span class="sxs-lookup"><span data-stu-id="01801-220">Notice above that a cost application is made (represented by the blue arrows) to ensure that item ledger entry 2 (Sales Return) is assigned the same costs as the item ledger entry that it reverses, item ledger entry 1 (Sale 1).</span></span> <span data-ttu-id="01801-221">Men, der foretages ikke en antalsudligning (repræsenteret af den røde pil).</span><span class="sxs-lookup"><span data-stu-id="01801-221">However, a quantity application (represented by the red arrows) is not made.</span></span>  

 <span data-ttu-id="01801-222">Varepost 2 (salgsreturvareordre) kan ikke være både omkostningsmodtager for den oprindelige varepost og samtidig være en leverandør af varer og deres omkostningskilde.</span><span class="sxs-lookup"><span data-stu-id="01801-222">Item ledger entry 2 (Sales Return) cannot be both a cost recipient of the original item ledger entry and at the same time be a supplier of items and their source of costs.</span></span> <span data-ttu-id="01801-223">Derfor kan den oprindelige varepost 1 (salg 1) forblive åben, indtil der vises en gyldig kilde.</span><span class="sxs-lookup"><span data-stu-id="01801-223">Therefore, the original item ledger entry 1 (Sale 1) remains open until a valid source appears.</span></span>  

## <a name="identifying-the-issue"></a><span data-ttu-id="01801-224">Identificere problemet</span><span class="sxs-lookup"><span data-stu-id="01801-224">Identifying the Issue</span></span>  
 <span data-ttu-id="01801-225">Gør følgende i det respektive scenarie for at finde ud af, om de åbne vareposter er oprettet:</span><span class="sxs-lookup"><span data-stu-id="01801-225">To find out if the open item ledger entries are created, do as follows for the respective scenario:</span></span>  

 <span data-ttu-id="01801-226">I scenarie 1 kan du identificere problemet på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="01801-226">For scenario 1, identify the issue as follows:</span></span>  

-   <span data-ttu-id="01801-227">I vinduet **Bogført salgskreditnota** eller **Bogført returvaremodt.** skal du foretage opslag fra feltet **Udlign\-fra-vareposten** for at se, om feltet er udfyldt, og så tilfælde til hvilken varepost returneringsmodtagelsen er omkostningsudlignet.</span><span class="sxs-lookup"><span data-stu-id="01801-227">In the **Posted Sales Credit Memo** or **Posted Return Receipt** window, look up from the **Appl.\-from Item Entry** field to see if the field is populated, and in that case to which item ledger entry the return receipt is cost applied.</span></span>  

 <span data-ttu-id="01801-228">I scenarie 2 kan du identificere problemet på en af følgende måder:</span><span class="sxs-lookup"><span data-stu-id="01801-228">For scenario 2, identify the issue in either of the following ways:</span></span>  

-   <span data-ttu-id="01801-229">Søg efter en åben udgående varepost og en indgående varepost med samme nummer i feltet **Bilagsnr.** og Ja i feltet **Rettelse**.</span><span class="sxs-lookup"><span data-stu-id="01801-229">Look for an open outbound item ledger entry and an inbound item ledger entry with same number in the **Document No.** field, and Yes in the **Correction** field.</span></span> <span data-ttu-id="01801-230">Se følgende eksempel på en sådan situation med en varepost.</span><span class="sxs-lookup"><span data-stu-id="01801-230">See the following example of such an item ledger entry situation.</span></span>  

|<span data-ttu-id="01801-231">Løbenummer</span><span class="sxs-lookup"><span data-stu-id="01801-231">Entry No.</span></span>|<span data-ttu-id="01801-232">Bogføringsdato</span><span class="sxs-lookup"><span data-stu-id="01801-232">Posting Date</span></span>|<span data-ttu-id="01801-233">Postens type</span><span class="sxs-lookup"><span data-stu-id="01801-233">Entry Type</span></span>|<span data-ttu-id="01801-234">Dokumenttype</span><span class="sxs-lookup"><span data-stu-id="01801-234">Document Type</span></span>|<span data-ttu-id="01801-235">Bilagsnr.</span><span class="sxs-lookup"><span data-stu-id="01801-235">Document No.</span></span>|<span data-ttu-id="01801-236">Varenr.</span><span class="sxs-lookup"><span data-stu-id="01801-236">Item No.</span></span>|<span data-ttu-id="01801-237">Lokationskode</span><span class="sxs-lookup"><span data-stu-id="01801-237">Location Code</span></span>|<span data-ttu-id="01801-238">Antal</span><span class="sxs-lookup"><span data-stu-id="01801-238">Quantity</span></span>|<span data-ttu-id="01801-239">Kostbeløb (faktisk)</span><span class="sxs-lookup"><span data-stu-id="01801-239">Cost Amount (Actual)</span></span>|<span data-ttu-id="01801-240">Faktureret antal</span><span class="sxs-lookup"><span data-stu-id="01801-240">Invoiced Quantity</span></span>|<span data-ttu-id="01801-241">Restantal</span><span class="sxs-lookup"><span data-stu-id="01801-241">Remaining Quantity</span></span>|<span data-ttu-id="01801-242">Åbn</span><span class="sxs-lookup"><span data-stu-id="01801-242">Open</span></span>|<span data-ttu-id="01801-243">Rettelse</span><span class="sxs-lookup"><span data-stu-id="01801-243">Correction</span></span>|  
|---------|------------|----------|-------------|------------|--------|-------------|--------|------------------------|-----------------|------------------|----|---------|
|<span data-ttu-id="01801-244">333</span><span class="sxs-lookup"><span data-stu-id="01801-244">333</span></span>|<span data-ttu-id="01801-245">28-01-2018</span><span class="sxs-lookup"><span data-stu-id="01801-245">01/28/2018</span></span>|<span data-ttu-id="01801-246">Salg</span><span class="sxs-lookup"><span data-stu-id="01801-246">Sale</span></span>|<span data-ttu-id="01801-247">Salgsleverance</span><span class="sxs-lookup"><span data-stu-id="01801-247">Sales Shipment</span></span>|<span data-ttu-id="01801-248">102043</span><span class="sxs-lookup"><span data-stu-id="01801-248">102043</span></span>|<span data-ttu-id="01801-249">TEST</span><span class="sxs-lookup"><span data-stu-id="01801-249">TEST</span></span>|<span data-ttu-id="01801-250">BLÅ</span><span class="sxs-lookup"><span data-stu-id="01801-250">BLUE</span></span>|<span data-ttu-id="01801-251">-1</span><span class="sxs-lookup"><span data-stu-id="01801-251">-1</span></span>|<span data-ttu-id="01801-252">-10</span><span class="sxs-lookup"><span data-stu-id="01801-252">-10</span></span>|<span data-ttu-id="01801-253">-1</span><span class="sxs-lookup"><span data-stu-id="01801-253">-1</span></span>|<span data-ttu-id="01801-254">-1</span><span class="sxs-lookup"><span data-stu-id="01801-254">-1</span></span>|<span data-ttu-id="01801-255">Ja</span><span class="sxs-lookup"><span data-stu-id="01801-255">Yes</span></span>|<span data-ttu-id="01801-256">Nej</span><span class="sxs-lookup"><span data-stu-id="01801-256">No</span></span>|  
|<span data-ttu-id="01801-257">334</span><span class="sxs-lookup"><span data-stu-id="01801-257">334</span></span>|<span data-ttu-id="01801-258">28-01-2018</span><span class="sxs-lookup"><span data-stu-id="01801-258">01/28/2018</span></span>|<span data-ttu-id="01801-259">Salg</span><span class="sxs-lookup"><span data-stu-id="01801-259">Sale</span></span>|<span data-ttu-id="01801-260">Salgsleverance</span><span class="sxs-lookup"><span data-stu-id="01801-260">Sales Shipment</span></span>|<span data-ttu-id="01801-261">102043</span><span class="sxs-lookup"><span data-stu-id="01801-261">102043</span></span>|<span data-ttu-id="01801-262">TEST</span><span class="sxs-lookup"><span data-stu-id="01801-262">TEST</span></span>|<span data-ttu-id="01801-263">BLÅ</span><span class="sxs-lookup"><span data-stu-id="01801-263">BLUE</span></span>|<span data-ttu-id="01801-264">1</span><span class="sxs-lookup"><span data-stu-id="01801-264">1</span></span>|<span data-ttu-id="01801-265">10</span><span class="sxs-lookup"><span data-stu-id="01801-265">10</span></span>|<span data-ttu-id="01801-266">1</span><span class="sxs-lookup"><span data-stu-id="01801-266">1</span></span>|<span data-ttu-id="01801-267">1</span><span class="sxs-lookup"><span data-stu-id="01801-267">1</span></span>|<span data-ttu-id="01801-268">Ja</span><span class="sxs-lookup"><span data-stu-id="01801-268">Yes</span></span>|<span data-ttu-id="01801-269">**Ja**</span><span class="sxs-lookup"><span data-stu-id="01801-269">**Yes**</span></span>|  
<!--![Why is inventory zero 7](media/helene/TechArticleInventoryZero7.png "Whyisinventoryzero\_7")-->

-   <span data-ttu-id="01801-270">I vinduet **Bogført salgsleverance** skal du foretage opslag fra feltet **Udlign fra-varepost** for at se, om feltet er udfyldt, og så tilfælde til hvilken varepost returneringsmodtagelsen er omkostningsudlignet.</span><span class="sxs-lookup"><span data-stu-id="01801-270">In the **Posted Sales Shipment** window, look up from the **Appl.-from Item Entry** field to see if the field is populated, and in that case to which item ledger entry the return receipt is cost applied.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="01801-271">Kostprisudligning kan ikke identificeres i vinduet **Udlignede vareposter**, da vinduet kun viser mængdeudligninger.</span><span class="sxs-lookup"><span data-stu-id="01801-271">Cost applications cannot be identified in the **Applied Item Entries** window because that window only shows quantity applications.</span></span>  

 <span data-ttu-id="01801-272">I begge scenarier kan du identificere den involverede kostprisudligning på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="01801-272">For both scenarios, identify the involved cost application as follows:</span></span>  

1.  <span data-ttu-id="01801-273">Åbn tabellen **Vareudligningspost**.</span><span class="sxs-lookup"><span data-stu-id="01801-273">Open the **Item Application Entry** table.</span></span>  

2.  <span data-ttu-id="01801-274">Filtrer efter **Varepostløbenr.** ved hjælp af nummeret på vareposten for salgsreturvareordren.</span><span class="sxs-lookup"><span data-stu-id="01801-274">Filter on the **Item Ledger Entry No.** field using the number of the Sales Return item ledger entry.</span></span>  

3.  <span data-ttu-id="01801-275">Analysér vareudligningsposten og vær opmærksom på følgende:</span><span class="sxs-lookup"><span data-stu-id="01801-275">Analyze the item application entry, taking note of the following:</span></span>  

     <span data-ttu-id="01801-276">Hvis feltet **Udgående varepostløbenr.** er udfyldt for en indgående varepost (positivt antal), betyder det, at den indgående varepost er omkostningsmodtager for den udgående varepost.</span><span class="sxs-lookup"><span data-stu-id="01801-276">If the **Outbound Item Entry No.** field is populated for an inbound item ledger entry (positive quantity), then it means that the inbound item ledger entry is the cost recipient of the outbound item ledger entry.</span></span>  

     <span data-ttu-id="01801-277">Se følgende eksempel på en vareudligningspost.</span><span class="sxs-lookup"><span data-stu-id="01801-277">See the following example of an item application entry.</span></span>  

     |<span data-ttu-id="01801-278">Løbenummer</span><span class="sxs-lookup"><span data-stu-id="01801-278">Entry No.</span></span>|<span data-ttu-id="01801-279">Varepostløbenr.</span><span class="sxs-lookup"><span data-stu-id="01801-279">Item Ledger Entry No.</span></span>|<span data-ttu-id="01801-280">Indgående varepostløbenr.</span><span class="sxs-lookup"><span data-stu-id="01801-280">Inbound Item Entry No.</span></span>|<span data-ttu-id="01801-281">Udgående varepostløbenr.</span><span class="sxs-lookup"><span data-stu-id="01801-281">Outbound Item Entry No.</span></span>|<span data-ttu-id="01801-282">Antal</span><span class="sxs-lookup"><span data-stu-id="01801-282">Quantity</span></span>|<span data-ttu-id="01801-283">Bogføringsdato</span><span class="sxs-lookup"><span data-stu-id="01801-283">Posting Date</span></span>|<span data-ttu-id="01801-284">Kostprisudligning</span><span class="sxs-lookup"><span data-stu-id="01801-284">Cost Application</span></span>|  
     |---------|---------------------|----------------------|-----------------------|--------|------------|----------------|  
     |<span data-ttu-id="01801-285">299</span><span class="sxs-lookup"><span data-stu-id="01801-285">299</span></span>|<span data-ttu-id="01801-286">334</span><span class="sxs-lookup"><span data-stu-id="01801-286">334</span></span>|<span data-ttu-id="01801-287">334</span><span class="sxs-lookup"><span data-stu-id="01801-287">334</span></span>|<span data-ttu-id="01801-288">333</span><span class="sxs-lookup"><span data-stu-id="01801-288">333</span></span>|<span data-ttu-id="01801-289">1</span><span class="sxs-lookup"><span data-stu-id="01801-289">1</span></span>|<span data-ttu-id="01801-290">28-01-2018</span><span class="sxs-lookup"><span data-stu-id="01801-290">01/28/2018</span></span>|<span data-ttu-id="01801-291">Ja</span><span class="sxs-lookup"><span data-stu-id="01801-291">Yes</span></span>|  
<!--![Why is inventory zero 8](media/helene/TechArticleInventoryZero8.png "Whyisinventoryzero\_8")  -->

 <span data-ttu-id="01801-292">Læg mærke til ovenfor, at den indgående varepost 334 er omkostningsudlignet til den udgående varepost 333.</span><span class="sxs-lookup"><span data-stu-id="01801-292">Notice above that inbound item ledger entry 334 is cost applied to outbound item ledger entry 333.</span></span>  

## <a name="workaround-for-the-issue"></a><span data-ttu-id="01801-293">Løsning til problemet</span><span class="sxs-lookup"><span data-stu-id="01801-293">Workaround for the Issue</span></span>  
 <span data-ttu-id="01801-294">I vinduet **Varekladde** skal du bogføre følgende linjer for den pågældende vare:</span><span class="sxs-lookup"><span data-stu-id="01801-294">In the **Item Journal** window, post the following lines for the item in question:</span></span>  

-   <span data-ttu-id="01801-295">En opregulering for at lukke den åbne udgående varepost.</span><span class="sxs-lookup"><span data-stu-id="01801-295">A positive adjustment to close the open outbound item ledger entry.</span></span>  

-   <span data-ttu-id="01801-296">En nedregulering med det samme antal.</span><span class="sxs-lookup"><span data-stu-id="01801-296">A negative adjustment with the same quantity.</span></span>  

     <span data-ttu-id="01801-297">Denne regulering balancerer den lagerforøgelse, der er forårsaget af opreguleringen og lukker den åbne indgående varepost.</span><span class="sxs-lookup"><span data-stu-id="01801-297">This adjustment balances the inventory increase caused by the positive adjustment and closes the open inbound item ledger entry.</span></span>  

 <span data-ttu-id="01801-298">Resultatet er, at lageret er nul, og alle vareposter er lukket.</span><span class="sxs-lookup"><span data-stu-id="01801-298">The result is that inventory is zero and all item ledger entries are closed.</span></span>  

## <a name="see-also"></a><span data-ttu-id="01801-299">Se også</span><span class="sxs-lookup"><span data-stu-id="01801-299">See Also</span></span>  
<span data-ttu-id="01801-300">[Designoplysninger: Vareudligning](design-details-item-application.md) </span><span class="sxs-lookup"><span data-stu-id="01801-300">[Design Details: Item Application](design-details-item-application.md) </span></span>  
[<span data-ttu-id="01801-301">Designoplysninger: Lagerkostmetode</span><span class="sxs-lookup"><span data-stu-id="01801-301">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)  
