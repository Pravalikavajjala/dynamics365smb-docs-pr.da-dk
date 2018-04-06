---
title: "Metoder for igangværende arbejde til beregning og registrering af sagsstatus | Microsoft Docs"
description: "Beskriver de forskellige metoder for igangværende arbejde, du kan bruge til at bogføre, overvåge og beregne finansielle oplysninger for igangværende arbejdssager."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: work in process, work in progress, calculate project WIP
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 85724fd6f43c684007dd22b34665438bf22bf99a
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="understanding-wip-methods"></a><span data-ttu-id="5a79e-103">Forstå VIA -metoder</span><span class="sxs-lookup"><span data-stu-id="5a79e-103">Understanding WIP Methods</span></span>
[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="5a79e-104"> understøtter følgende metoder til beregning og registrering af værdien af igangværende arbejde.</span><span class="sxs-lookup"><span data-stu-id="5a79e-104"> supports the following methods of calculating and recording the value of work in process.</span></span>

| <span data-ttu-id="5a79e-105">VIA-metode</span><span class="sxs-lookup"><span data-stu-id="5a79e-105">WIP Method</span></span> | <span data-ttu-id="5a79e-106">Beregningsformel</span><span class="sxs-lookup"><span data-stu-id="5a79e-106">Calculation Formula</span></span> | <span data-ttu-id="5a79e-107">Beregningsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="5a79e-107">Calculation Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="5a79e-108">Kostværdi</span><span class="sxs-lookup"><span data-stu-id="5a79e-108">Cost Value</span></span> |<span data-ttu-id="5a79e-109">Realiserede indtægter = Fakturerbar faktureret pris</span><span class="sxs-lookup"><span data-stu-id="5a79e-109">Recognized Revenue = Billable Invoiced Price</span></span><br /><br /> <span data-ttu-id="5a79e-110">Anslået kostbeløb = Fakturerbart salgsbeløb x Budgetomkostninger</span><span class="sxs-lookup"><span data-stu-id="5a79e-110">Estimated Total Costs = Billable Total Price x Budget Cost Ratio</span></span><br /><br /> <span data-ttu-id="5a79e-111">VIA-omkostninger = (Færdiggørelsesgrad -faktureret % x Anslået kostbeløb</span><span class="sxs-lookup"><span data-stu-id="5a79e-111">WIP Costs = (Percentage of Completion - Invoiced %) x Estimated Total Costs</span></span><br /><br /> <span data-ttu-id="5a79e-112">Færdiggørelsesgrad = Forbrug-kostbeløb/Budget-kostbeløb</span><span class="sxs-lookup"><span data-stu-id="5a79e-112">Percentage of Completion = Usage Total Costs / Budget Total Costs</span></span><br /> <span data-ttu-id="5a79e-113">Faktureret % = Fakturerbar faktureret pris</span><span class="sxs-lookup"><span data-stu-id="5a79e-113">Invoiced % = Billable Invoiced Price</span></span><br /><br /> <span data-ttu-id="5a79e-114">Fakturerbart salgsbeløb realiserede omkostninger = Forbrug-kostbeløb - Igangværende arbejde</span><span class="sxs-lookup"><span data-stu-id="5a79e-114">Billable Total Price Recognized Costs = Usage Total Costs - WIP</span></span> |<span data-ttu-id="5a79e-115">I beregninger af kostværdi startes der med at beregne værdien af det, der er leveret, idet der tages en del af det anslåede kostbeløb baseret på færdiggørelsesgrad.</span><span class="sxs-lookup"><span data-stu-id="5a79e-115">Cost value calculations start by calculating the value of what has been provided by taking a proportion of the estimated total costs based on percentage of completion.</span></span> <span data-ttu-id="5a79e-116">Fakturerede kostbeløb fratrækkes, ved at der tages en del af det anslåede kostbeløb baseret på faktureringsprocenten.</span><span class="sxs-lookup"><span data-stu-id="5a79e-116">Invoiced costs are subtracted by taking a proportion of the estimated total costs based on the invoiced percentage.</span></span><br /><br /> <span data-ttu-id="5a79e-117">Denne beregning kræver, at fakturerbart salgsbeløb, budget-salgsbeløb og budget-kostbeløb angives korrekt for hele sagen.</span><span class="sxs-lookup"><span data-stu-id="5a79e-117">This calculation requires that the billable total price, budget total price, and budget total costs be correctly entered for the whole job.</span></span> |
| <span data-ttu-id="5a79e-118">Salgsomkostning</span><span class="sxs-lookup"><span data-stu-id="5a79e-118">Cost of Sales</span></span> |<span data-ttu-id="5a79e-119">Realiserede indtægter = Fakturerbar faktureret pris</span><span class="sxs-lookup"><span data-stu-id="5a79e-119">Recognized Revenue = Billable Invoiced Price</span></span><br /><br /> <span data-ttu-id="5a79e-120">Realiserede omkostninger = Budget-kostbeløb x faktureringsprocent</span><span class="sxs-lookup"><span data-stu-id="5a79e-120">Recognized Costs = Budget Total Cost x Invoiced Percentage</span></span><br /><br /> <span data-ttu-id="5a79e-121">Faktureret % = Fakturerbart faktureret salgsbeløb / Fakturerbart salgsbeløb</span><span class="sxs-lookup"><span data-stu-id="5a79e-121">Invoiced % = Billable Invoiced Price / Billable Total Price</span></span><br /><br /> <span data-ttu-id="5a79e-122">(Faktureret % findes som kolonne i sagsopgavelinjer)</span><span class="sxs-lookup"><span data-stu-id="5a79e-122">(Invoiced % exists as column on job task lines)</span></span><br /><br /> <span data-ttu-id="5a79e-123">Igangv. arbejder køb = Forbrug-kostbeløb – realiserede omkostninger</span><span class="sxs-lookup"><span data-stu-id="5a79e-123">WIP Costs = Usage Total Costs – Recognized Costs</span></span> |<span data-ttu-id="5a79e-124">Beregninger af salgsomkostninger starter med beregning af realiserede omkostninger.</span><span class="sxs-lookup"><span data-stu-id="5a79e-124">Cost of sales calculations begin by calculating the recognized costs.</span></span> <span data-ttu-id="5a79e-125">Omkostninger realiseres proportionalt baseret på budgetteret kostbeløb.</span><span class="sxs-lookup"><span data-stu-id="5a79e-125">Costs are recognized proportionally based on budget total costs.</span></span><br /><br /> <span data-ttu-id="5a79e-126">Denne beregning kræver, at det fakturerbare salgsbeløb og det budgetterede kostbeløb angives korrekt for hele sagen.</span><span class="sxs-lookup"><span data-stu-id="5a79e-126">This calculation requires that the billable total price and budget total costs be correctly entered for the whole job.</span></span> |
| <span data-ttu-id="5a79e-127">Salgsværdi</span><span class="sxs-lookup"><span data-stu-id="5a79e-127">Sales Value</span></span> |<span data-ttu-id="5a79e-128">Realiserede omkostninger = Forbrug-kostbeløb</span><span class="sxs-lookup"><span data-stu-id="5a79e-128">Recognized Costs = Usage Total Costs</span></span><br /><br /> <span data-ttu-id="5a79e-129">Realiseret indtægt = Forbrug-salgsbeløb x Forventet faktureringsforhold</span><span class="sxs-lookup"><span data-stu-id="5a79e-129">Recognized Revenue = Usage Total Price x Expected invoicing ratio</span></span><br /><br /> <span data-ttu-id="5a79e-130">Omkostningsdækningspct. % = Fakturerbart salgsbeløb/Budgetteret salgsbeløb</span><span class="sxs-lookup"><span data-stu-id="5a79e-130">Cost Recovery % = Billable Total Price / Budget Total Price</span></span><br /><br /> <span data-ttu-id="5a79e-131">Igangværende arbejde salg = Realiseret salg - Fakturerbart faktureret salgsbeløb</span><span class="sxs-lookup"><span data-stu-id="5a79e-131">WIP Sales = Recognized Sales - Billable Invoiced Price</span></span> |<span data-ttu-id="5a79e-132">I beregninger af salgsværdi realiseres indtægter proportionalt baseret på Forbrug-kostbeløb og det forventede omkostningsdækningsforhold.</span><span class="sxs-lookup"><span data-stu-id="5a79e-132">Sales value calculations recognize revenue proportionally based on usage total costs and the expected cost recovery ratio.</span></span><br /><br /> <span data-ttu-id="5a79e-133">Denne beregning kræver, at det fakturerbare salgsbeløb og det budgetterede salgsbeløb angives korrekt for hele sagen.</span><span class="sxs-lookup"><span data-stu-id="5a79e-133">This calculation requires that the billable total price and budget total price be correctly entered for the whole job.</span></span> |
| <span data-ttu-id="5a79e-134">Færdiggørelsesgrad</span><span class="sxs-lookup"><span data-stu-id="5a79e-134">Percentage of Completion</span></span> |<span data-ttu-id="5a79e-135">Realiserede omkostninger = Forbrug-kostbeløb</span><span class="sxs-lookup"><span data-stu-id="5a79e-135">Recognized Costs = Usage Total Costs</span></span><br /><br /> <span data-ttu-id="5a79e-136">Realiseret indtægt = Fakturerbar salgspris x Færdiggørelsesgrad</span><span class="sxs-lookup"><span data-stu-id="5a79e-136">Recognized Revenue = Billable Total Price x Percentage of Completion</span></span><br /><br /> <span data-ttu-id="5a79e-137">Færdiggørelsesgrad = Forbrug-kostbeløb/Budget-kostbeløb</span><span class="sxs-lookup"><span data-stu-id="5a79e-137">Percentage of Completion = Usage Total Costs / Budget Total Costs</span></span><br /> <span data-ttu-id="5a79e-138">(Kaldes “Fuldførelse af omkostning i % “ på sagsopgavelinjer)</span><span class="sxs-lookup"><span data-stu-id="5a79e-138">(Referred to as "Cost Completion %" on job task lines)</span></span><br /><br /> <span data-ttu-id="5a79e-139">Igangværende arbejde salg = Realiseret salg - Fakturerbart faktureret salgsbeløb</span><span class="sxs-lookup"><span data-stu-id="5a79e-139">WIP Sales = Recognized Sales - Billable Invoiced Price</span></span> |<span data-ttu-id="5a79e-140">I beregninger af færdiggørelsesgrad realiseres indtægt proportionalt baseret på færdiggørelsesgraden, dvs. Forbrug-kostbeløb over for Budgetomkostninger.</span><span class="sxs-lookup"><span data-stu-id="5a79e-140">Percentage of completion calculations recognize revenue proportionally based on the percentage of completion, that is, usage total costs vs. budget costs.</span></span><br /><br /> <span data-ttu-id="5a79e-141">Denne beregning kræver, at det fakturerbare salgsbeløb og det budgetterede kostbeløb angives korrekt for hele sagen.</span><span class="sxs-lookup"><span data-stu-id="5a79e-141">This calculation requires that the billable total price and budget total costs be correctly entered for the whole job.</span></span> |
| <span data-ttu-id="5a79e-142">Afsluttet kontrakt</span><span class="sxs-lookup"><span data-stu-id="5a79e-142">Completed Contract</span></span> |<span data-ttu-id="5a79e-143">VIA-beløb = VIA-kostbeløb = Forbrug (kostbeløb)</span><span class="sxs-lookup"><span data-stu-id="5a79e-143">WIP Amount = WIP Cost Amount = Usage (Total Cost)</span></span><br /><br /> <span data-ttu-id="5a79e-144">Igangværende arbejde - salgsbeløb = Fakturerbar (faktureret salg)</span><span class="sxs-lookup"><span data-stu-id="5a79e-144">WIP Sales Amount = Billable (Invoiced Price)</span></span> |<span data-ttu-id="5a79e-145">Afsluttet kontrakt realiserer ikke indtægter og omkostninger, før sagen er afsluttet.</span><span class="sxs-lookup"><span data-stu-id="5a79e-145">Completed contract does not recognize revenue and costs until the job is complete.</span></span> <span data-ttu-id="5a79e-146">Du kan vælge denne metode, hvis der er stor tvivl omkring de anslåede kostbeløb og sagens omsætning.</span><span class="sxs-lookup"><span data-stu-id="5a79e-146">You may want to do this when there is high uncertainty around the estimates of costs and revenue for the job.</span></span><br /><br /> <span data-ttu-id="5a79e-147">Alt forbrug bogføres til kontoen til VIA-omkostninger (aktiv), og alt faktureret salg bogføres til kontoen til faktureret VIA-salg (kreditorkonto), indtil sagen er afsluttet.</span><span class="sxs-lookup"><span data-stu-id="5a79e-147">All usage is posted to the WIP Costs account (asset) and all invoiced sales are posted to the WIP Invoiced Sales account (liability) until the job is complete.</span></span> |

## <a name="see-also"></a><span data-ttu-id="5a79e-148">Se også</span><span class="sxs-lookup"><span data-stu-id="5a79e-148">See Also</span></span>
[<span data-ttu-id="5a79e-149">Projektstyring</span><span class="sxs-lookup"><span data-stu-id="5a79e-149">Project Management</span></span>](projects-manage-projects.md)  
[<span data-ttu-id="5a79e-150">Finans</span><span class="sxs-lookup"><span data-stu-id="5a79e-150">Finance</span></span>](finance.md)  
<span data-ttu-id="5a79e-151">[Køb](purchasing-manage-purchasing.md)       </span><span class="sxs-lookup"><span data-stu-id="5a79e-151">[Purchasing](purchasing-manage-purchasing.md)       </span></span>  
<span data-ttu-id="5a79e-152">[Salg](sales-manage-sales.md)    </span><span class="sxs-lookup"><span data-stu-id="5a79e-152">[Sales](sales-manage-sales.md)    </span></span>  
<span data-ttu-id="5a79e-153">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5a79e-153">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
