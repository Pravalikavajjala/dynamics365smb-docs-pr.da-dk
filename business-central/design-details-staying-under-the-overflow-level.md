---
title: "Designoplysninger - Forblive under overløbsniveauet | Microsoft Docs"
description: "Når du bruger Maks. antal og Fast genbestil.antal, fokuserer planlægningssystemet kun på den planlagte lagerbeholdning i det angivne tidsinterval. Det betyder, at planlægningssystemet kan foreslå overflødig forsyning, når der forekommer negative behovs- eller positive forsyningsændringer uden for det angivne tidsinterval."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 2fc2ef2528a1edc85c0a7694c1afc5bec7a0065a
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-staying-under-the-overflow-level"></a><span data-ttu-id="506a8-104">Designoplysninger: Forblive under overløbsniveauet</span><span class="sxs-lookup"><span data-stu-id="506a8-104">Design Details: Staying under the Overflow Level</span></span>
<span data-ttu-id="506a8-105">Når du bruger metoderne Maks. antal og Fast genbestil.antal, fokuserer planlægningssystemet kun på den planlagte lagerbeholdning i det angivne tidsinterval.</span><span class="sxs-lookup"><span data-stu-id="506a8-105">When using the Maximum Qty. and Fixed Reorder Qty. policies, the planning system focuses on the projected inventory in the given time-bucket only.</span></span> <span data-ttu-id="506a8-106">Det betyder, at planlægningssystemet kan foreslå overflødig forsyning, når der forekommer negative behovs- eller positive forsyningsændringer uden for det angivne tidsinterval.</span><span class="sxs-lookup"><span data-stu-id="506a8-106">This means that the planning system may suggest superfluous supply when negative demand or positive supply changes occur outside of the given time bucket.</span></span> <span data-ttu-id="506a8-107">Hvis der derfor foreslås en overflødig forsyning, beregner planlægningssystemet, hvilket antal forsyningen skal reduceres til (eller slettes) for at undgå overflødig forsyning.</span><span class="sxs-lookup"><span data-stu-id="506a8-107">If, for this reason, a superfluous supply is suggested, the planning system calculates which quantity the supply should be decreased to (or deleted) to avoid the superfluous supply.</span></span> <span data-ttu-id="506a8-108">Dette antal kaldes "overløbsniveauet".</span><span class="sxs-lookup"><span data-stu-id="506a8-108">This quantity is called the “overflow level.”</span></span> <span data-ttu-id="506a8-109">Overløbet kommunikeres som en planlægningslinje med en handling i form af **Ret antal (reducering)** eller **Annuller** og følgende advarselsmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="506a8-109">The overflow is communicated as a planning line with a **Change Qty. (Decrease)** or **Cancel** action and the following warning message:</span></span>  

<span data-ttu-id="506a8-110">*Bemærk: Den forventede lagerbeholdning [xx] er højere end overløbsniveauet [xx] på forfaldsdatoen [xx].*</span><span class="sxs-lookup"><span data-stu-id="506a8-110">*Attention: The projected inventory [xx] is higher than the overflow level [xx] on the Due Date [xx].*</span></span>  

<span data-ttu-id="506a8-111">![Lageroverløbsniveau](media/supplyplanning_2_overflow1_new.png "supplyplanning_2_overflow1_new")</span><span class="sxs-lookup"><span data-stu-id="506a8-111">![Inventory overflow level](media/supplyplanning_2_overflow1_new.png "supplyplanning_2_overflow1_new")</span></span>  

##  <a name="calculating-the-overflow-level"></a><span data-ttu-id="506a8-112">Beregning af overløbsniveau</span><span class="sxs-lookup"><span data-stu-id="506a8-112">Calculating the Overflow Level</span></span>  
<span data-ttu-id="506a8-113">Overløbsniveauet beregnes på forskellige måder afhængig af planlægningsopsætningen.</span><span class="sxs-lookup"><span data-stu-id="506a8-113">The overflow level is calculated in different ways depending on planning setup.</span></span>  

### <a name="maximum-qty-reordering-policy"></a><span data-ttu-id="506a8-114">Maksimalt antal som genbestillingsmetode</span><span class="sxs-lookup"><span data-stu-id="506a8-114">Maximum Qty. reordering policy</span></span>  
<span data-ttu-id="506a8-115">Overløbsniveau = Maks. lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="506a8-115">Overflow level = Maximum Inventory</span></span>  

> [!NOTE]  
>  <span data-ttu-id="506a8-116">Hvis der findes en min. ordrestørrelse bliver den tilføjet som følger: overløbsniveau = maks. lagerbeholdning + min. ordrestørrelse.</span><span class="sxs-lookup"><span data-stu-id="506a8-116">If a minimum order quantity exists, then it will be added as follows: Overflow level = Maximum Inventory + Minimum Order Quantity.</span></span>  

### <a name="fixed-reorder-qty-reordering-policy"></a><span data-ttu-id="506a8-117">Fast genbestil.antal-genbestillingsmetode</span><span class="sxs-lookup"><span data-stu-id="506a8-117">Fixed Reorder Qty. reordering policy</span></span>  
<span data-ttu-id="506a8-118">Overløbsniveau = Ordrekvantum + Genbestillingspunkt</span><span class="sxs-lookup"><span data-stu-id="506a8-118">Overflow level = Reorder Quantity + Reorder Point</span></span>  

> [!NOTE]  
>  <span data-ttu-id="506a8-119">Hvis den mindste ordrestørrelse er højere end genbestillingspunktet, vil det erstatte på følgende måde: Overløbsniveau = genbestil.antal + min. ordrestørrelse</span><span class="sxs-lookup"><span data-stu-id="506a8-119">If the minimum order quantity is higher than the reorder point, then it will replace as follows: Overflow Level = Reorder Quantity + Minimum Order Quantity</span></span>  

### <a name="order-multiple"></a><span data-ttu-id="506a8-120">Oprundingsfaktor</span><span class="sxs-lookup"><span data-stu-id="506a8-120">Order Multiple</span></span>  
<span data-ttu-id="506a8-121">Hvis en ordre findes flere gange, vil den justere overløbsniveauet for både maks. og fast genbestillingsantal som genbestillingsmetoder.</span><span class="sxs-lookup"><span data-stu-id="506a8-121">If an order multiple exists, then it will adjust the overflow level for both Maximum Qty. and Fixed Reorder Qty. reordering policies.</span></span>  

##  <a name="creating-the-planning-line-with-overflow-warning"></a><span data-ttu-id="506a8-122">Oprettelse af planlægningslinjen med overløbsadvarsel</span><span class="sxs-lookup"><span data-stu-id="506a8-122">Creating the Planning Line with Overflow Warning</span></span>  
<span data-ttu-id="506a8-123">Når en eksisterende forsyning medfører, at den projekterede lagerbeholdning bliver større end overløbsniveauet ved slutningen af et interval, oprettes der en planlægningslinje.</span><span class="sxs-lookup"><span data-stu-id="506a8-123">When an existing supply causes the projected inventory to be higher than the overflow level at the end of a time bucket, a planning line is created.</span></span> <span data-ttu-id="506a8-124">For at advare om potentiel overflødig levering indeholder planlægningslinjen en advarselsmeddelelse, feltet **Accepter aktionsmeddelelse** er ikke markeret, og aktionsmeddelelsen er enten Annuller eller Ret antal.</span><span class="sxs-lookup"><span data-stu-id="506a8-124">To warn about the potential superfluous supply, the planning line has a warning message, the **Accept Action Message** field is not selected, and the action message is either Cancel or Change Qty.</span></span>  

### <a name="calculating-the-planning-line-quantity"></a><span data-ttu-id="506a8-125">Beregning af antallet af planlægningslinjer.</span><span class="sxs-lookup"><span data-stu-id="506a8-125">Calculating the Planning Line Quantity</span></span>  
<span data-ttu-id="506a8-126">Planlægning af linjeantallet = aktuel forsyningsmængde – (projekteret lagerbeholdning – overløbsniveau)</span><span class="sxs-lookup"><span data-stu-id="506a8-126">Planning Line Quantity = Current Supply Quantity – (Projected Inventory – Overflow Level)</span></span>  

> [!NOTE]  
>  <span data-ttu-id="506a8-127">Som med alle advarselslinjer vil alle maksimale/minimale ordremængder eller oprundingsfaktorer blive ignoreret.</span><span class="sxs-lookup"><span data-stu-id="506a8-127">As with all warning lines, any maximum/minimum order quantity or order multiple will be ignored.</span></span>  

### <a name="defining-the-action-message-type"></a><span data-ttu-id="506a8-128">Definition af aktionsmeddelelsestypen</span><span class="sxs-lookup"><span data-stu-id="506a8-128">Defining the Action Message Type</span></span>  

-   <span data-ttu-id="506a8-129">Hvis antallet på planlægningslinjen er højere end 0, er aktionsmeddelelsen Ret antal</span><span class="sxs-lookup"><span data-stu-id="506a8-129">If the planning line quantity is higher than 0, then the action message is Change Qty.</span></span>  
-   <span data-ttu-id="506a8-130">Hvis antallet på planlægningslinjen er lig med eller mindre end 0, er aktionsmeddelelsen Annuller</span><span class="sxs-lookup"><span data-stu-id="506a8-130">If the planning line quantity is equal to or lower than 0, then the action message is Cancel</span></span>  

### <a name="composing-the-warning-message"></a><span data-ttu-id="506a8-131">Oprettelse af advarselsmeddelelsen</span><span class="sxs-lookup"><span data-stu-id="506a8-131">Composing the Warning Message</span></span>  
<span data-ttu-id="506a8-132">I forbindelse med overløb vises der i vinduet **Ikke-sporede planlægningselementer** en advarsel med følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="506a8-132">In case of overflow, the **Untracked Planning Elements** window displays a warning message with the following information:</span></span>  

-   <span data-ttu-id="506a8-133">Det planlagte lagerniveau, der udløste advarslen</span><span class="sxs-lookup"><span data-stu-id="506a8-133">The projected inventory level that triggered the warning</span></span>  
-   <span data-ttu-id="506a8-134">Det beregnede overløbsniveau</span><span class="sxs-lookup"><span data-stu-id="506a8-134">The calculated overflow level</span></span>  
-   <span data-ttu-id="506a8-135">Forfaldsdatoen for forsyningshændelsen.</span><span class="sxs-lookup"><span data-stu-id="506a8-135">The due date of the supply event.</span></span>  

<span data-ttu-id="506a8-136">Eksempel: "Den planlagte beholdning 120 er større end overløbsniveauet 60 på 28-01-11"</span><span class="sxs-lookup"><span data-stu-id="506a8-136">Example: “The projected inventory 120 is higher than the overflow level 60 on 28-01-11”</span></span>  

## <a name="scenario"></a><span data-ttu-id="506a8-137">Scenarie</span><span class="sxs-lookup"><span data-stu-id="506a8-137">Scenario</span></span>  
<span data-ttu-id="506a8-138">I dette scenario ændrer en kunde en salgsordre fra 70 til 40 stykker mellem to kørsler af planlægning.</span><span class="sxs-lookup"><span data-stu-id="506a8-138">In this scenario, a customer changes a sales order from 70 to 40 pieces between two planning runs.</span></span> <span data-ttu-id="506a8-139">Overløbsfunktionen begynder at reducere det køb, der blev foreslået for det oprindelige salgsantal.</span><span class="sxs-lookup"><span data-stu-id="506a8-139">The overflow feature sets in to reduce the purchase that was suggested for the initial sales quantity.</span></span>  

### <a name="item-setup"></a><span data-ttu-id="506a8-140">Vareopsætning</span><span class="sxs-lookup"><span data-stu-id="506a8-140">Item setup</span></span>  

|<span data-ttu-id="506a8-141">Genbestillingsmetode</span><span class="sxs-lookup"><span data-stu-id="506a8-141">Reordering Policy</span></span>|<span data-ttu-id="506a8-142">Maks. antal</span><span class="sxs-lookup"><span data-stu-id="506a8-142">Maximum Qty.</span></span>|  
|-----------------------|------------------|  
|<span data-ttu-id="506a8-143">Maks. ordrestørrelse</span><span class="sxs-lookup"><span data-stu-id="506a8-143">Maximum Order Quantity</span></span>|<span data-ttu-id="506a8-144">100</span><span class="sxs-lookup"><span data-stu-id="506a8-144">100</span></span>|  
|<span data-ttu-id="506a8-145">Genbestillingspunkt</span><span class="sxs-lookup"><span data-stu-id="506a8-145">Reorder Point</span></span>|<span data-ttu-id="506a8-146">50</span><span class="sxs-lookup"><span data-stu-id="506a8-146">50</span></span>|  
|<span data-ttu-id="506a8-147">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="506a8-147">Inventory</span></span>|<span data-ttu-id="506a8-148">80</span><span class="sxs-lookup"><span data-stu-id="506a8-148">80</span></span>|  

### <a name="situation-before-sales-decrease"></a><span data-ttu-id="506a8-149">Situationen før salgsreducering</span><span class="sxs-lookup"><span data-stu-id="506a8-149">Situation before sales decrease</span></span>  

|<span data-ttu-id="506a8-150">Begivenhed</span><span class="sxs-lookup"><span data-stu-id="506a8-150">Event</span></span>|<span data-ttu-id="506a8-151">Ret antal</span><span class="sxs-lookup"><span data-stu-id="506a8-151">Change Qty.</span></span>|<span data-ttu-id="506a8-152">Planlagt beholdning</span><span class="sxs-lookup"><span data-stu-id="506a8-152">Projected Inventory</span></span>|  
|-----------|-----------------|-------------------------|  
|<span data-ttu-id="506a8-153">Dag et</span><span class="sxs-lookup"><span data-stu-id="506a8-153">Day one</span></span>|<span data-ttu-id="506a8-154">Ingen</span><span class="sxs-lookup"><span data-stu-id="506a8-154">None</span></span>|<span data-ttu-id="506a8-155">80</span><span class="sxs-lookup"><span data-stu-id="506a8-155">80</span></span>|  
|<span data-ttu-id="506a8-156">Salg</span><span class="sxs-lookup"><span data-stu-id="506a8-156">Sale</span></span>|<span data-ttu-id="506a8-157">-70</span><span class="sxs-lookup"><span data-stu-id="506a8-157">-70</span></span>|<span data-ttu-id="506a8-158">10</span><span class="sxs-lookup"><span data-stu-id="506a8-158">10</span></span>|  
|<span data-ttu-id="506a8-159">Slutning på interval</span><span class="sxs-lookup"><span data-stu-id="506a8-159">End of time bucket</span></span>|<span data-ttu-id="506a8-160">Ingen</span><span class="sxs-lookup"><span data-stu-id="506a8-160">None</span></span>|<span data-ttu-id="506a8-161">10</span><span class="sxs-lookup"><span data-stu-id="506a8-161">10</span></span>|  
|<span data-ttu-id="506a8-162">Foreslå ny købsordre</span><span class="sxs-lookup"><span data-stu-id="506a8-162">Suggest new purchase order</span></span>|<span data-ttu-id="506a8-163">+90</span><span class="sxs-lookup"><span data-stu-id="506a8-163">+90</span></span>|<span data-ttu-id="506a8-164">100</span><span class="sxs-lookup"><span data-stu-id="506a8-164">100</span></span>|  

### <a name="situation-after-sales-decrease"></a><span data-ttu-id="506a8-165">Situationen efter salgsreducering</span><span class="sxs-lookup"><span data-stu-id="506a8-165">Situation after sales decrease</span></span>  

|<span data-ttu-id="506a8-166">Ændring</span><span class="sxs-lookup"><span data-stu-id="506a8-166">Change</span></span>|<span data-ttu-id="506a8-167">Ret antal</span><span class="sxs-lookup"><span data-stu-id="506a8-167">Change Qty.</span></span>|<span data-ttu-id="506a8-168">Planlagt beholdning</span><span class="sxs-lookup"><span data-stu-id="506a8-168">Projected Inventory</span></span>|  
|------------|-----------------|-------------------------|  
|<span data-ttu-id="506a8-169">Dag et</span><span class="sxs-lookup"><span data-stu-id="506a8-169">Day one</span></span>|<span data-ttu-id="506a8-170">Ingen</span><span class="sxs-lookup"><span data-stu-id="506a8-170">None</span></span>|<span data-ttu-id="506a8-171">80</span><span class="sxs-lookup"><span data-stu-id="506a8-171">80</span></span>|  
|<span data-ttu-id="506a8-172">Salg</span><span class="sxs-lookup"><span data-stu-id="506a8-172">Sale</span></span>|<span data-ttu-id="506a8-173">-40</span><span class="sxs-lookup"><span data-stu-id="506a8-173">-40</span></span>|<span data-ttu-id="506a8-174">40</span><span class="sxs-lookup"><span data-stu-id="506a8-174">40</span></span>|  
|<span data-ttu-id="506a8-175">Køb</span><span class="sxs-lookup"><span data-stu-id="506a8-175">Purchase</span></span>|<span data-ttu-id="506a8-176">+90</span><span class="sxs-lookup"><span data-stu-id="506a8-176">+90</span></span>|<span data-ttu-id="506a8-177">130</span><span class="sxs-lookup"><span data-stu-id="506a8-177">130</span></span>|  
|<span data-ttu-id="506a8-178">Slutning på interval</span><span class="sxs-lookup"><span data-stu-id="506a8-178">End of time bucket</span></span>|<span data-ttu-id="506a8-179">Ingen</span><span class="sxs-lookup"><span data-stu-id="506a8-179">None</span></span>|<span data-ttu-id="506a8-180">130</span><span class="sxs-lookup"><span data-stu-id="506a8-180">130</span></span>|  
|<span data-ttu-id="506a8-181">Foreslå at reducere køb</span><span class="sxs-lookup"><span data-stu-id="506a8-181">Suggest to decrease purchase</span></span><br /><br /> <span data-ttu-id="506a8-182">ordre fra 90 til 60</span><span class="sxs-lookup"><span data-stu-id="506a8-182">order from 90 to 60</span></span>|<span data-ttu-id="506a8-183">-30</span><span class="sxs-lookup"><span data-stu-id="506a8-183">-30</span></span>|<span data-ttu-id="506a8-184">100</span><span class="sxs-lookup"><span data-stu-id="506a8-184">100</span></span>|  

### <a name="resulting-planning-lines"></a><span data-ttu-id="506a8-185">Resulterende planlægningslinjer</span><span class="sxs-lookup"><span data-stu-id="506a8-185">Resulting Planning Lines</span></span>  
 <span data-ttu-id="506a8-186">Der oprettes en planlægningslinje (advarsel) for at reducere køb med 30 fra 90 til 60 for at bevare den projekterede lagerbeholdning på 100 i henhold til overløbsniveauet.</span><span class="sxs-lookup"><span data-stu-id="506a8-186">One planning line (warning) is created to reduce the purchase with 30 from 90 to 60 to keep the projected inventory on 100 according to the overflow level.</span></span>  

<span data-ttu-id="506a8-187">![Planlægge efter overløbsniveauet](media/nav_app_supply_planning_2_overflow2.png "nav_app_supply_planning_2_overflow2")</span><span class="sxs-lookup"><span data-stu-id="506a8-187">![Plan according to overflow level](media/nav_app_supply_planning_2_overflow2.png "nav_app_supply_planning_2_overflow2")</span></span>  

> [!NOTE]  
>  <span data-ttu-id="506a8-188">Uden overløbsfunktionen vises der ingen advarsel, hvis den projekterede lagerbeholdning ligger over maks.</span><span class="sxs-lookup"><span data-stu-id="506a8-188">Without the Overflow feature, no warning is created if the projected inventory level is above maximum inventory.</span></span> <span data-ttu-id="506a8-189">Dette kan medføre en overflødig forsyning på 30.</span><span class="sxs-lookup"><span data-stu-id="506a8-189">This could cause a superfluous supply of 30.</span></span>  

## <a name="see-also"></a><span data-ttu-id="506a8-190">Se også</span><span class="sxs-lookup"><span data-stu-id="506a8-190">See Also</span></span>  
<span data-ttu-id="506a8-191">[Designoplysninger: Genbestillingsmetoder](design-details-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="506a8-191">[Design Details: Reordering Policies](design-details-reordering-policies.md) </span></span>  
<span data-ttu-id="506a8-192">[Designoplysninger: Planlægningsparametre](design-details-planning-parameters.md) </span><span class="sxs-lookup"><span data-stu-id="506a8-192">[Design Details: Planning Parameters](design-details-planning-parameters.md) </span></span>  
<span data-ttu-id="506a8-193">[Designoplysninger: Håndtering af genbestillingsmetoder](design-details-handling-reordering-policies.md) </span><span class="sxs-lookup"><span data-stu-id="506a8-193">[Design Details: Handling Reordering Policies](design-details-handling-reordering-policies.md) </span></span>  
[<span data-ttu-id="506a8-194">Designoplysninger: Forsyningsplanlægning</span><span class="sxs-lookup"><span data-stu-id="506a8-194">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)
