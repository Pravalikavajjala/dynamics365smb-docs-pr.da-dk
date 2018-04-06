---
title: "Designoplysninger – Bogføring af produktionsordre | Microsoft Docs"
description: "I lighed med montageordrebogføring bliver de forbrugte komponenter og den anvendte computertid konverteret og udlæst som den producerede vare, når produktionsordren er afsluttet."
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
ms.openlocfilehash: 08e7aac45ecc90b9b4957a8722e1a9ae13d6c321
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-production-order-posting"></a><span data-ttu-id="79539-103">Designoplysninger: Bogføring af produktionsordre</span><span class="sxs-lookup"><span data-stu-id="79539-103">Design Details: Production Order Posting</span></span>
<span data-ttu-id="79539-104">I lighed med montageordrebogføring bliver de forbrugte komponenter og den anvendte computertid konverteret og udlæst som den producerede vare, når produktionsordren er afsluttet.</span><span class="sxs-lookup"><span data-stu-id="79539-104">Similar to assembly order posting, the consumed components and the used machine time are converted and output as the produced item when the production order is finished.</span></span> <span data-ttu-id="79539-105">Du kan finde flere oplysninger i [Designoplysninger: Bogføring af montageordre](design-details-assembly-order-posting.md).</span><span class="sxs-lookup"><span data-stu-id="79539-105">For more information, see [Design Details: Assembly Order Posting](design-details-assembly-order-posting.md).</span></span> <span data-ttu-id="79539-106">Men montageordrers kost-flow er mindre kompliceret, især fordi montageomkostninger kun bogføres én gang og derfor ikke opretter lageret for igangværende arbejde.</span><span class="sxs-lookup"><span data-stu-id="79539-106">However, the cost flow for assembly orders is less complex, especially because assembly cost posting only occurs once and therefore does not generate work-in-process inventory.</span></span>


<span data-ttu-id="79539-107">Transaktioner, der forekommer under produktionsprocessen, kan spores via følgende faser:</span><span class="sxs-lookup"><span data-stu-id="79539-107">Transactions that occur during the manufacturing process can be tracked through the following stages:</span></span>  

1.  <span data-ttu-id="79539-108">Indkøb af materialer og andre tilgange til produktion.</span><span class="sxs-lookup"><span data-stu-id="79539-108">Purchase of materials and other manufacturing inputs.</span></span>  
2.  <span data-ttu-id="79539-109">Konvertering til igangværende arbejde.</span><span class="sxs-lookup"><span data-stu-id="79539-109">Conversion into work in process.</span></span>  
3.  <span data-ttu-id="79539-110">Konvertering til færdigvarelager.</span><span class="sxs-lookup"><span data-stu-id="79539-110">Conversion into finished goods inventory.</span></span>  
4.  <span data-ttu-id="79539-111">Salg af færdigvarer</span><span class="sxs-lookup"><span data-stu-id="79539-111">Sale of finished goods.</span></span>  

<span data-ttu-id="79539-112">Udover almindelige lagerkonti skal en produktionsvirksomhed derfor oprette tre separate lagerkontoer for at registrere transaktioner på forskellige stadier af produktionen.</span><span class="sxs-lookup"><span data-stu-id="79539-112">Therefore, apart from regular inventory accounts, a manufacturing company must establish three separate inventory accounts to record transactions at various stages of production.</span></span>  

|<span data-ttu-id="79539-113">Lagerkonto</span><span class="sxs-lookup"><span data-stu-id="79539-113">Inventory Account</span></span>|<span data-ttu-id="79539-114">Description</span><span class="sxs-lookup"><span data-stu-id="79539-114">Description</span></span>|  
|-----------------------|---------------------------------------|  
|<span data-ttu-id="79539-115">**Konto for råmaterialer**</span><span class="sxs-lookup"><span data-stu-id="79539-115">**Raw Materials account**</span></span>|<span data-ttu-id="79539-116">Omfatter køb af råvarer, der er købt, men som endnu ikke er overført til produktion.</span><span class="sxs-lookup"><span data-stu-id="79539-116">Includes the cost of raw materials that are purchased but not yet transferred to production.</span></span> <span data-ttu-id="79539-117">Saldoen på kontoen for råvarer angiver omkostningerne ved råvarer på lager.</span><span class="sxs-lookup"><span data-stu-id="79539-117">The balance in the Raw Materials account indicates the cost of raw materials on hand.</span></span><br /><br /> <span data-ttu-id="79539-118">Når råvarer flyttes til produktionsafdelingen, overføres kostprisen for materialerne fra kontoen Råvarer til IVA-kontoen.</span><span class="sxs-lookup"><span data-stu-id="79539-118">When raw materials move into the production department, the cost of the materials is transferred from the Raw Materials account to the WIP account.</span></span>|  
|<span data-ttu-id="79539-119">**VIA-konto (VIA)**</span><span class="sxs-lookup"><span data-stu-id="79539-119">**Work in Process (WIP) account**</span></span>|<span data-ttu-id="79539-120">Akkumulerer de omkostninger, der er påløbet i produktionsprocessen i regnskabsperioden.</span><span class="sxs-lookup"><span data-stu-id="79539-120">Accumulates the costs that are incurred during production in the accounting period.</span></span> <span data-ttu-id="79539-121">VIA-kontoen debiteres for omkostningerne i forbindelse med råmaterialer, der overføres fra lagerstedet for råvarer, omkostningerne ved direkte udført arbejde og de faste produktionsomkostninger, der er påløbet.</span><span class="sxs-lookup"><span data-stu-id="79539-121">The WIP account is debited for the cost of raw materials that are transferred from the raw materials warehouse, the cost of direct labor performed, and the manufacturing overhead costs that are incurred.</span></span><br /><br /> <span data-ttu-id="79539-122">VIA-kontoen krediteres de samlede produktionsomkostninger for enheder, der er udført på fabrikken og overført til lageret for færdigvarer.</span><span class="sxs-lookup"><span data-stu-id="79539-122">The WIP account is credited for the total manufacturing cost of units that are completed in the factory and transferred to the finished goods warehouse.</span></span>|  
|<span data-ttu-id="79539-123">**Konto for færdigvarer**</span><span class="sxs-lookup"><span data-stu-id="79539-123">**Finished Goods account**</span></span>|<span data-ttu-id="79539-124">Denne konto indeholder de samlede produktionsomkostninger for enheder, der er fuldført, men som endnu ikke er solgt.</span><span class="sxs-lookup"><span data-stu-id="79539-124">This account includes the total manufacturing cost of units that are completed but not yet sold.</span></span> <span data-ttu-id="79539-125">På salgstidspunktet overføres kostprisen for solgte enheder fra kontoen for færdigvarer til kontoen for solgte varer.</span><span class="sxs-lookup"><span data-stu-id="79539-125">At the time of sale, the cost of units sold is transferred from the Finished Goods account to the Cost of Goods Sold account.</span></span>|  

<span data-ttu-id="79539-126">Lagerværdien beregnes ved at spore omkostninger for alle forøgelser og reduceringer, som udtrykt i følgende ligning:</span><span class="sxs-lookup"><span data-stu-id="79539-126">The inventory value is calculated by tracking the costs of all increases and decreases, as expressed by the following equation:</span></span>  

* <span data-ttu-id="79539-127">lagerværdi = startsaldo for lager + værdi af alle forøgelser - værdi af alle reduceringer</span><span class="sxs-lookup"><span data-stu-id="79539-127">inventory value = beginning balance of inventory + value of all increases - value of all decreases</span></span>  

<span data-ttu-id="79539-128">Afhængigt af typen af lager repræsenteres forøgelser og reduceringer af forskellige posteringer.</span><span class="sxs-lookup"><span data-stu-id="79539-128">Depending on the type of inventory, increases and decreases are represented by different transactions.</span></span>  

||<span data-ttu-id="79539-129">Forøgelse</span><span class="sxs-lookup"><span data-stu-id="79539-129">Increases</span></span>|<span data-ttu-id="79539-130">Reducering</span><span class="sxs-lookup"><span data-stu-id="79539-130">Decreases</span></span>|  
|-|---------------|---------------|  
|<span data-ttu-id="79539-131">**Lager af råmaterialer**</span><span class="sxs-lookup"><span data-stu-id="79539-131">**Raw material inventory**</span></span>|<span data-ttu-id="79539-132">-   Nettokøb af materiale</span><span class="sxs-lookup"><span data-stu-id="79539-132">-   Net purchases of material</span></span><br /><span data-ttu-id="79539-133">-   Afgang af halvfabrikata</span><span class="sxs-lookup"><span data-stu-id="79539-133">-   Output of subassemblies</span></span><br /><span data-ttu-id="79539-134">-   Negativt forbrug</span><span class="sxs-lookup"><span data-stu-id="79539-134">-   Negative consumption</span></span>|<span data-ttu-id="79539-135">Materialeforbrug</span><span class="sxs-lookup"><span data-stu-id="79539-135">Material consumption</span></span>|  
|<span data-ttu-id="79539-136">**VIA-lagerbeholdning**</span><span class="sxs-lookup"><span data-stu-id="79539-136">**WIP inventory**</span></span>|<span data-ttu-id="79539-137">-   Materialeforbrug</span><span class="sxs-lookup"><span data-stu-id="79539-137">-   Material consumption</span></span><br /><span data-ttu-id="79539-138">-   (Forbrug, kapacitet)</span><span class="sxs-lookup"><span data-stu-id="79539-138">-   Capacity consumption</span></span><br /><span data-ttu-id="79539-139">-   Indirekte prod.kostpris</span><span class="sxs-lookup"><span data-stu-id="79539-139">-   Manufacturing overhead</span></span>|<span data-ttu-id="79539-140">Afgang af færdigvarer (omkostninger af fremstillede varer)</span><span class="sxs-lookup"><span data-stu-id="79539-140">Output of end items (cost of goods manufactured)</span></span>|  
|<span data-ttu-id="79539-141">**Færdigvarelager**</span><span class="sxs-lookup"><span data-stu-id="79539-141">**Finished goods inventory**</span></span>|<span data-ttu-id="79539-142">Afgang af færdigvarer (omkostninger af fremstillede varer)</span><span class="sxs-lookup"><span data-stu-id="79539-142">Output of end items (cost of goods manufactured)</span></span>|<span data-ttu-id="79539-143">-   Salg (vareforbrug)</span><span class="sxs-lookup"><span data-stu-id="79539-143">-   Sales (cost of goods sold)</span></span><br /><span data-ttu-id="79539-144">-   Negativ afgang</span><span class="sxs-lookup"><span data-stu-id="79539-144">-   Negative output</span></span>|  
|<span data-ttu-id="79539-145">**Lager af råmaterialer**</span><span class="sxs-lookup"><span data-stu-id="79539-145">**Raw material inventory**</span></span>|<span data-ttu-id="79539-146">-   Nettokøb af materiale</span><span class="sxs-lookup"><span data-stu-id="79539-146">-   Net purchases of material</span></span><br /><span data-ttu-id="79539-147">-   Afgang af halvfabrikata</span><span class="sxs-lookup"><span data-stu-id="79539-147">-   Output of subassemblies</span></span><br /><span data-ttu-id="79539-148">-   Negativt forbrug</span><span class="sxs-lookup"><span data-stu-id="79539-148">-   Negative consumption</span></span>|<span data-ttu-id="79539-149">Materialeforbrug</span><span class="sxs-lookup"><span data-stu-id="79539-149">Material consumption</span></span>|  

<span data-ttu-id="79539-150">Værdierne for forøgelser og reduceringer registreres i de forskellige typer af produceret lager på samme måde som for købt lager.</span><span class="sxs-lookup"><span data-stu-id="79539-150">The values of increases and decreases are recorded in the different types of manufactured inventory in the same way as for purchased inventory.</span></span> <span data-ttu-id="79539-151">Hver gang en lagerforøgelses- eller lagerreduceringstransaktion finder sted, oprettes der en varepost og en tilsvarende finanspost for beløbet.</span><span class="sxs-lookup"><span data-stu-id="79539-151">Every time a transaction of inventory increase or decrease takes place, an item ledger entry and a corresponding general ledger entry are created for the amount.</span></span> <span data-ttu-id="79539-152">Du kan finde flere oplysninger i [Designoplysninger: Varekladde](design-details-inventory-posting.md).</span><span class="sxs-lookup"><span data-stu-id="79539-152">For more information, see [Design Details: Inventory Posting](design-details-inventory-posting.md).</span></span>  

<span data-ttu-id="79539-153">Selvom værdier af transaktioner, der vedrører købte varer, kun bogføres som vareposter med relaterede værdiposter, bogføres transaktioner, der er knyttet til producerede varer, som kapacitetsposter med relaterede værdiposter, udover vareposterne.</span><span class="sxs-lookup"><span data-stu-id="79539-153">Although values of transactions that are related to purchased goods are posted only as item ledger entries with related value entries, transactions that are related to produced items are posted as capacity ledger entries with related value entries, in addition to the item ledger entries.</span></span>  

## <a name="posting-structure"></a><span data-ttu-id="79539-154">Bogføringsstruktur</span><span class="sxs-lookup"><span data-stu-id="79539-154">Posting Structure</span></span>  
<span data-ttu-id="79539-155">Bogføring af produktionsordrer til igangværende arbejdslager omfatter afgang, forbrug og kapacitet.</span><span class="sxs-lookup"><span data-stu-id="79539-155">Posting production orders to WIP inventory involves output, consumption, and capacity.</span></span>  

<span data-ttu-id="79539-156">Følgende diagram viser de involverede bogføringsrutiner i kodeenhed 22.</span><span class="sxs-lookup"><span data-stu-id="79539-156">The following diagram shows the involved posting routines in codeunit 22.</span></span>  

<span data-ttu-id="79539-157">![Posteringsrutiner for produktionsordre](media/design_details_inventory_costing_14_production_posting_1.png "design_details_inventory_costing_14_production_posting_1")</span><span class="sxs-lookup"><span data-stu-id="79539-157">![Production order posting routines](media/design_details_inventory_costing_14_production_posting_1.png "design_details_inventory_costing_14_production_posting_1")</span></span>  

<span data-ttu-id="79539-158">I følgende diagram vises tilknytninger mellem de oprettede poster og omkostningsemnerne.</span><span class="sxs-lookup"><span data-stu-id="79539-158">The following diagram shows the associations between the resulting entries and the cost objects.</span></span>  

<span data-ttu-id="79539-159">![Produktionspostflow](media/design_details_inventory_costing_14_production_posting_2.png "design_details_inventory_costing_14_production_posting_2")</span><span class="sxs-lookup"><span data-stu-id="79539-159">![Production entry flows](media/design_details_inventory_costing_14_production_posting_2.png "design_details_inventory_costing_14_production_posting_2")</span></span>  

<span data-ttu-id="79539-160">Kapacitetsposten beskriver kapacitetsforbrug i tidsenheder, hvorimod den tilknyttede værdipost beskriver værdien af det specifikke kapacitetsforbrug.</span><span class="sxs-lookup"><span data-stu-id="79539-160">The capacity ledger entry describes the capacity consumption in terms of time units, whereas the related value entry describes the value of the specific capacity consumption.</span></span>  

<span data-ttu-id="79539-161">Vareposten beskriver materialeforbrug eller afgang med hensyn til mængder, mens den tilknyttede værdipost beskriver værdien af dette specifikke materialeforbrug eller afgangen.</span><span class="sxs-lookup"><span data-stu-id="79539-161">The item ledger entry describes the material consumption or output in terms of quantities, whereas the related value entry describes the value of this specific material consumption or output.</span></span>  

<span data-ttu-id="79539-162">En værdipost, der beskriver det igangværendes arbejdes værdi, kan være knyttet til en af følgende kombinationer af omkostningsemner:</span><span class="sxs-lookup"><span data-stu-id="79539-162">A value entry that describes WIP inventory value can be associated with one of the following combinations of cost objects:</span></span>  

-   <span data-ttu-id="79539-163">En produktionsordrelinje, et arbejdscenter eller en produktionsressource og en kapacitetspost.</span><span class="sxs-lookup"><span data-stu-id="79539-163">A production order line, a work or machine center, and a capacity ledger entry.</span></span>  
-   <span data-ttu-id="79539-164">En produktionsordrelinje, en vare og en varepost.</span><span class="sxs-lookup"><span data-stu-id="79539-164">A production order line, an item, and an item ledger entry.</span></span>  
-   <span data-ttu-id="79539-165">Kun en produktionsordrelinje</span><span class="sxs-lookup"><span data-stu-id="79539-165">Only a production order line</span></span>  

<span data-ttu-id="79539-166">Du kan finde flere oplysninger om, hvordan omkostninger fra produktion og montage bogføres i finansregnskabet, i [Designoplysninger: Varekladde](design-details-inventory-posting.md).</span><span class="sxs-lookup"><span data-stu-id="79539-166">For more information about how costs from production and assembly are posted to the general ledger, see [Design Details: Inventory Posting](design-details-inventory-posting.md).</span></span>  

## <a name="capacity-posting"></a><span data-ttu-id="79539-167">Bogføring af kapacitet</span><span class="sxs-lookup"><span data-stu-id="79539-167">Capacity Posting</span></span>  
<span data-ttu-id="79539-168">Bogføring af afgang fra den sidste produktionsordrerutelinje resulterer i en kapacitetsfinanspost for færdigvaren, i tillæg til dens lagerforøgelse.</span><span class="sxs-lookup"><span data-stu-id="79539-168">Posting output from the last production order routing line results in a capacity ledger entry for the end item, in addition to its inventory increase.</span></span>  

 <span data-ttu-id="79539-169">Kapacitetsposten er en post over den tid, der er brugt til at producere varen.</span><span class="sxs-lookup"><span data-stu-id="79539-169">The capacity ledger entry is a record of the time that was spent to produce the item.</span></span> <span data-ttu-id="79539-170">Den relaterede værdipost beskrives i VIA-lagerværdien, som er værdien af konverteringsomkostningerne.</span><span class="sxs-lookup"><span data-stu-id="79539-170">The related value entry describes the increase of the WIP inventory value, which is the value of the conversion cost.</span></span> <span data-ttu-id="79539-171">Du kan finde flere oplysninger i "Fra kapacitetsposten" i [Designoplysninger: Konti i Finans](design-details-accounts-in-the-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="79539-171">For more information, see “From the Capacity Ledger” in [Design Details: Accounts in the General Ledger](design-details-accounts-in-the-general-ledger.md).</span></span>  

## <a name="production-order-costing"></a><span data-ttu-id="79539-172">Produktionsordrekostmetode</span><span class="sxs-lookup"><span data-stu-id="79539-172">Production Order Costing</span></span>  
 <span data-ttu-id="79539-173">Med henblik på at kontrollere lager- og produktionsomkostninger skal en produktionsvirksomhed måle omkostningerne for produktionsordrer, da de standardomkostninger, der er fastsat på forhånd for hver produceret vare, kapitaliseres i balancen.</span><span class="sxs-lookup"><span data-stu-id="79539-173">To control inventory and production costs, a manufacturing company must measure the cost of production orders, because the predetermined standard cost of each produced item is capitalized in the balance sheet.</span></span> <span data-ttu-id="79539-174">Hvis du ønsker oplysninger om, hvorfor producerede varer bruger kostmetoden Standard, kan du se [Designoplysninger: Kostmetoder](design-details-costing-methods.md).</span><span class="sxs-lookup"><span data-stu-id="79539-174">For information about why produced items use the Standard costing method, see [Design Details: Costing Methods](design-details-costing-methods.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="79539-175">I miljøer, der ikke bruger kostmetoden Standard, aktiveres den faktiske værdi i stedet for standardkostprisen for fremstillede varer på balancen.</span><span class="sxs-lookup"><span data-stu-id="79539-175">In environments that do not use the Standard costing method, the actual rather than the standard cost of produced items is capitalized on the balance sheet.</span></span>  

<span data-ttu-id="79539-176">De faktiske omkostninger for en produktionsordre består af følgende omkostningskomponenter:</span><span class="sxs-lookup"><span data-stu-id="79539-176">The actual cost of a production order consists of the following cost components:</span></span>  

-   <span data-ttu-id="79539-177">Faktisk materialekostpris</span><span class="sxs-lookup"><span data-stu-id="79539-177">Actual material cost</span></span>  
-   <span data-ttu-id="79539-178">Faktiske kapacitetsomkostninger eller omkostninger til underleverandør</span><span class="sxs-lookup"><span data-stu-id="79539-178">Actual capacity cost or subcontractor cost</span></span>  
-   <span data-ttu-id="79539-179">Indirekte prod.kostpris</span><span class="sxs-lookup"><span data-stu-id="79539-179">Manufacturing overhead</span></span>  

<span data-ttu-id="79539-180">Disse faktiske omkostninger bogføres til produktionsordren og sammenlignes med standardkostprisen for at beregne afvigelser.</span><span class="sxs-lookup"><span data-stu-id="79539-180">These actual costs are posted to the production order and compared to the standard cost to calculate variances.</span></span> <span data-ttu-id="79539-181">Afvigelser beregnes for hver af varekomponentomkostningerne: råvarer, kapacitet, underleverandør-, kapacitets- og produktionsomkostninger.</span><span class="sxs-lookup"><span data-stu-id="79539-181">Variances are calculated for each of the item cost components: raw materials, capacity, subcontractor, capacity overhead, and manufacturing overhead.</span></span> <span data-ttu-id="79539-182">Afvigelserne kan analyseres for at afgøre, om der er problemer, som f.eks. overdrevent tab i behandlingen.</span><span class="sxs-lookup"><span data-stu-id="79539-182">The variances can be analyzed to determine problems, such as excessive waste in processing.</span></span>  

<span data-ttu-id="79539-183">I miljøer med standardkostpriser er omkostninger for en produktionsordre baseret på følgende metode:</span><span class="sxs-lookup"><span data-stu-id="79539-183">In standard-cost environments, the costing of a production order is based on the following mechanism:</span></span>  

1.  <span data-ttu-id="79539-184">Når den sidste ruteoperation bogføres, bogføres kostprisen for produktionsordren til vareposten og indstilles til de forventede omkostninger.</span><span class="sxs-lookup"><span data-stu-id="79539-184">When the last routing operation is posted, the production order cost is posted to the item ledger and set to the expected cost.</span></span>  

    <span data-ttu-id="79539-185">Disse omkostninger er lig med det afgangsantal, der er bogført i afgangskladden ganget med de standardomkostninger, der er kopieret fra varekortet.</span><span class="sxs-lookup"><span data-stu-id="79539-185">This cost equals the output quantity that is posted in the output journal multiplied by the standard cost that is copied from the item card.</span></span> <span data-ttu-id="79539-186">Omkostninger behandles som forventet kostpris, indtil produktionsordren er afsluttet.</span><span class="sxs-lookup"><span data-stu-id="79539-186">The cost is treated as expected cost until the production order is finished.</span></span> <span data-ttu-id="79539-187">Du kan finde flere oplysninger i [Designoplysninger: Bogføring af forventet kostpris](design-details-expected-cost-posting.md).</span><span class="sxs-lookup"><span data-stu-id="79539-187">For more information, see [Design Details: Expected Cost Posting](design-details-expected-cost-posting.md).</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="79539-188">Dette adskiller sig fra montageordrebogføring, hvor der altid bogføres faktiske omkostninger.</span><span class="sxs-lookup"><span data-stu-id="79539-188">This differs from assembly order posting, which always posts actual costs.</span></span> <span data-ttu-id="79539-189">Du kan finde flere oplysninger i [Designoplysninger: Bogføring af montageordre](design-details-assembly-order-posting.md).</span><span class="sxs-lookup"><span data-stu-id="79539-189">For more information, see [Design Details: Assembly Order Posting](design-details-assembly-order-posting.md).</span></span>  
2.  <span data-ttu-id="79539-190">Når produktionsordren er indstillet til **Færdig**, faktureres ordren ved at udføre kørslen **Juster kostpris - vareposter**.</span><span class="sxs-lookup"><span data-stu-id="79539-190">When the production order is set to **Finished**, the order is invoiced by running the **Adjust Cost-Item Entries** batch job.</span></span> <span data-ttu-id="79539-191">Som resultat beregnes de samlede omkostninger for ordren baseret på standardkostprisen for de anvendte materialer og kapacitet.</span><span class="sxs-lookup"><span data-stu-id="79539-191">As a result, the total cost of the order is calculated based on the standard cost of the consumed materials and capacity.</span></span> <span data-ttu-id="79539-192">Afvigelserne mellem de beregnede standardkostpriser og de faktiske produktionskostpriser beregnes og bogføres.</span><span class="sxs-lookup"><span data-stu-id="79539-192">The variances between the calculated standard costs and the actual production costs are calculated and posted.</span></span>  

## <a name="see-also"></a><span data-ttu-id="79539-193">Se også</span><span class="sxs-lookup"><span data-stu-id="79539-193">See Also</span></span>  
 <span data-ttu-id="79539-194">[Designoplysninger: Lagerkostmetode](design-details-inventory-costing.md) </span><span class="sxs-lookup"><span data-stu-id="79539-194">[Design Details: Inventory Costing](design-details-inventory-costing.md) </span></span>  
 [<span data-ttu-id="79539-195">Designoplysninger: Bogføring af montageordre</span><span class="sxs-lookup"><span data-stu-id="79539-195">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)  
 <span data-ttu-id="79539-196">[Administrere lageromkostninger](finance-manage-inventory-costs.md) [Finans](finance.md)</span><span class="sxs-lookup"><span data-stu-id="79539-196">[Managing Inventory Costs](finance-manage-inventory-costs.md) [Finance](finance.md)</span></span>  
 [<span data-ttu-id="79539-197">Arbejde med Financials</span><span class="sxs-lookup"><span data-stu-id="79539-197">Working with Financials</span></span>](ui-work-product.md)
