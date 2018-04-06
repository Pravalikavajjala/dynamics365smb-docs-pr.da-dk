---
title: Montagestyring | Microsoft Docs
description: "Støt virksomheder, som leverer produkter til deres kunder, ved at kombinere komponenter i enkle processer uden brug af produktionsfunktioner, men med funktioner til montage af varer, der kan integreres med eksisterende funktioner som salg, planlægning, reservationer og opbevaring."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/26/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4ce03eb7a3685f53869795ded646ef6917a1730a
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="assembly-management"></a><span data-ttu-id="a1756-103">Montagestyring</span><span class="sxs-lookup"><span data-stu-id="a1756-103">Assembly Management</span></span>
<span data-ttu-id="a1756-104">For at støtte virksomheder, som leverer produkter til deres kunder ved at kombinere komponenter i enkle processer uden brug af produktionsfunktioner, indeholder [!INCLUDE[d365fin](includes/d365fin_md.md)] funktioner til montage af varer, der kan integreres med eksisterende funktioner som salg, planlægning, reservationer og opbevaring.</span><span class="sxs-lookup"><span data-stu-id="a1756-104">To support companies that supply products to their customers by combining components in simple processes without the need of manufacturing functionality, [!INCLUDE[d365fin](includes/d365fin_md.md)] includes features to assemble items that integrate with existing features, such as sales, planning, reservations, and warehousing.</span></span>  

 <span data-ttu-id="a1756-105">Et montageelement er defineret som et salgbart element, der indeholder en montagestykliste.</span><span class="sxs-lookup"><span data-stu-id="a1756-105">An assembly item is defined as a sellable item that contains an assembly BOM.</span></span> <span data-ttu-id="a1756-106">Du kan finde flere oplysninger under [Arbejde med styklister](inventory-how-work-BOMs.md).</span><span class="sxs-lookup"><span data-stu-id="a1756-106">For more information, see [Work with Bills of Material](inventory-how-work-BOMs.md).</span></span>

 <span data-ttu-id="a1756-107">Montageordrer er interne ordrer, ligesom produktionsordrer, der bruges til at administrere montageprocessen og til at forbinde salgskravene med de involverede lageraktiviteter.</span><span class="sxs-lookup"><span data-stu-id="a1756-107">Assembly orders are internal orders, just like production orders, that are used to manage the assembly process and to connect the sales requirements with the involved warehouse activities.</span></span> <span data-ttu-id="a1756-108">Montageordrer adskiller sig fra andre ordretyper, da de omfatter både afgang og forbrug, når de bogføres.</span><span class="sxs-lookup"><span data-stu-id="a1756-108">Assembly orders differ from other order types because they involve both output and consumption when posting.</span></span> <span data-ttu-id="a1756-109">Montageordrehovedet fungerer på samme måde en salgsordrelinje, og montageordrelinjerne fungerer på samme måde som forbrugskladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="a1756-109">The assembly order header behaves similarly to a sales order line, and the assembly order lines behave similarly to consumption journal lines.</span></span>  

 <span data-ttu-id="a1756-110">For at støtte en for JIT-lagerstrategi og muligheden for at tilpasse produkter til debitorkrav, kan montageordrer automatisk oprettes og kædes sammen, så snart salgsordrelinjen er oprettet.</span><span class="sxs-lookup"><span data-stu-id="a1756-110">To support a just-in-time inventory strategy and the ability to customize products to customer requests, assembly orders may be automatically created and linked as soon as the sales order line is created.</span></span> <span data-ttu-id="a1756-111">Sammenkædningen mellem salgsbehovet og montageleveringen gør det muligt for salgsordrebehandleren at tilpasse montageelementet løbende, love leveringsdatoer ifølge komponenttilgængeligheden og bogføre afgang og levering af montageelementet direkte fra deres salgsordregrænseflade.</span><span class="sxs-lookup"><span data-stu-id="a1756-111">The link between the sales demand and the assembly supply enables sales order processors to customize the assembly item on the fly, promise delivery dates according to component availability, and to post output and shipment of the assembled item directly from their sales order interface.</span></span> <span data-ttu-id="a1756-112">Du kan finde flere oplysninger i [Sælge varer, der er monteret til ordre](assembly-how-to-sell-items-assembled-to-order.md).</span><span class="sxs-lookup"><span data-stu-id="a1756-112">For more information, see [Sell Items Assembled to Order](assembly-how-to-sell-items-assembled-to-order.md).</span></span>  

 <span data-ttu-id="a1756-113">På en salgsordrelinje kan du sælge et antal, der er tilgængeligt, og som skal plukkes fra lageret sammen med et montage efter ordre-antal.</span><span class="sxs-lookup"><span data-stu-id="a1756-113">On one sales order line, you can sell a quantity that is available and must be picked from stock together with a quantity that must be assembled to the order.</span></span> <span data-ttu-id="a1756-114">Der findes visse regler for fordelingen af disse mængder for at sikre, at montage efter ordre-mængder har højere prioritet end lagerantal i delvis levering.</span><span class="sxs-lookup"><span data-stu-id="a1756-114">Certain rules exist to govern the distribution of such quantities to ensure that assemble-to-order quantities take priority over inventory quantities in partial shipping.</span></span> <span data-ttu-id="a1756-115">Du kan finde flere oplysninger i afsnittet "Kombinationsscenarier" i [Om Montage til ordre og Montage til lager](assembly-assemble-to-order-or-assemble-to-stock.md).</span><span class="sxs-lookup"><span data-stu-id="a1756-115">For more information, see the “Combination Scenarios” section in [Understanding Assemble to Order and Assemble to Stock](assembly-assemble-to-order-or-assemble-to-stock.md).</span></span>  

 <span data-ttu-id="a1756-116">Der findes specialfunktioner til styring af leveringen af montage efter ordre-mængder.</span><span class="sxs-lookup"><span data-stu-id="a1756-116">Special functionality exists to govern the shipping of assemble-to-order quantities.</span></span> <span data-ttu-id="a1756-117">Når en montage efter ordre-mængde er klar til at blive leveret, bogfører den ansvarlige lagermedarbejder et lagerpluk for de pågældende salgsordrelinjer.</span><span class="sxs-lookup"><span data-stu-id="a1756-117">When an assemble-to-order quantity is ready to be shipped, the warehouse worker in charge posts an inventory pick for the sales order line(s) in question.</span></span> <span data-ttu-id="a1756-118">Dette opretter derefter en flytning (lager) for komponenterne, bogfører montageoutputtet og salgsordreleverancen.</span><span class="sxs-lookup"><span data-stu-id="a1756-118">This, in turn, creates an inventory movement for the components, posts the assembly output, and the sales order shipment.</span></span> <span data-ttu-id="a1756-119">Du kan finde flere oplysninger i afsnittet "Håndtere montage til ordre-varer i Pluk (lager)" i [Plukke varer med Pluk fra lager](warehouse-how-to-pick-items-with-inventory-picks.md).</span><span class="sxs-lookup"><span data-stu-id="a1756-119">For more information, see the "Handling Assemble-to-Order Items in Inventory Picks” section in [Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md).</span></span>

<span data-ttu-id="a1756-120">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="a1756-120">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="a1756-121">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="a1756-121">**To**</span></span>|<span data-ttu-id="a1756-122">**Se**</span><span class="sxs-lookup"><span data-stu-id="a1756-122">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="a1756-123">Få mere at vide om forskellen mellem at montere elementer korrekt, før levering af salgsordrer og montering af varer, der er bestemt til oplagring.</span><span class="sxs-lookup"><span data-stu-id="a1756-123">Learn about the difference between assembling items right before shipping sales orders and assembling items that are intended for storage.</span></span>|[<span data-ttu-id="a1756-124">Om montage til ordre og montage til lager</span><span class="sxs-lookup"><span data-stu-id="a1756-124">Understanding Assemble to Order and Assemble to Stock</span></span>](assembly-assemble-to-order-or-assemble-to-stock.md)|
|<span data-ttu-id="a1756-125">Udfyld felter på lokationskort og lageropsætning for at definere, hvordan varer strømmer til og fra montageafdelingen.</span><span class="sxs-lookup"><span data-stu-id="a1756-125">Fill in fields on location cards and in inventory setup to define how items flow to and from the assembly department.</span></span>|[<span data-ttu-id="a1756-126">Oprette grundlæggende lagersteder med handlingsområder</span><span class="sxs-lookup"><span data-stu-id="a1756-126">Set Up Basic Warehouses with Operations Areas</span></span>](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)|
|<span data-ttu-id="a1756-127">Tilpas et montageelement til en kundes anmodning under salgsprocessen, og konverter til et salg ved accept.</span><span class="sxs-lookup"><span data-stu-id="a1756-127">Customize an assembly item to a customer’s request during the sales process, and convert to a sale when accepted.</span></span>|[<span data-ttu-id="a1756-128">Oprette tilbud på montage til ordre-salg</span><span class="sxs-lookup"><span data-stu-id="a1756-128">Quote an Assemble-to-Order Sale</span></span>](assembly-how-to-quote-an-assemble-to-order-sale.md)|
|<span data-ttu-id="a1756-129">Kombiner komponenter for at oprette et element i en enkel proces, til bestilling eller til lager.</span><span class="sxs-lookup"><span data-stu-id="a1756-129">Combine components to create an item in a simple process, to order or to stock.</span></span>|[<span data-ttu-id="a1756-130">Montere varer</span><span class="sxs-lookup"><span data-stu-id="a1756-130">Assemble Items</span></span>](assembly-how-to-assemble-items.md)|  
|<span data-ttu-id="a1756-131">Sælg montageelementer, der ikke er tilgængelige i øjeblikket, ved at oprette en tilknyttet montageordre for at levere den fulde eller delvise salgsordremængde.</span><span class="sxs-lookup"><span data-stu-id="a1756-131">Sell assembly items that are not currently available by creating a linked assembly order to supply the full or partial sales order quantity.</span></span>|[<span data-ttu-id="a1756-132">Sælge varer, der er monteret til ordre</span><span class="sxs-lookup"><span data-stu-id="a1756-132">Sell Items Assembled to Order</span></span>](assembly-how-to-sell-items-assembled-to-order.md)|
|<span data-ttu-id="a1756-133">Når nogle montage til ordre-elementer allerede findes i lageret, kan du fratrække mængden fra montageordren og reservere den fra lageret.</span><span class="sxs-lookup"><span data-stu-id="a1756-133">When some assemble-to-order items are already in inventory, deduct that quantity from the assembly order and reserve it from inventory.</span></span>|[<span data-ttu-id="a1756-134">Sælge lagervarer i montage til ordre-forløb</span><span class="sxs-lookup"><span data-stu-id="a1756-134">Sell Inventory Items in Assemble-to-Order Flows</span></span>](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)|  
|<span data-ttu-id="a1756-135">Når du sælger montageelementer fra lageret, og alle elementer ikke er tilgængelige, kan du starte en montageordre til automatisk at levere en del af eller hele salgsordremængden.</span><span class="sxs-lookup"><span data-stu-id="a1756-135">When you are selling assembly items from inventory and all items are not available, initiate an assembly order to automatically supply a part or all of the sales order quantity.</span></span>|[<span data-ttu-id="a1756-136">Sælge montage til ordre-varer og lagervarer sammen</span><span class="sxs-lookup"><span data-stu-id="a1756-136">Sell Assemble-to-Order Items and Inventory Items Together</span></span>](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)|
|<span data-ttu-id="a1756-137">Annuller en bogført montageordre, for eksempel fordi ordren er bogført med fejl, der skal rettes.</span><span class="sxs-lookup"><span data-stu-id="a1756-137">Undo a posted assembly order, for example because the order was posted with mistakes that must be corrected.</span></span>|[<span data-ttu-id="a1756-138">Fortryde bogføring af montage</span><span class="sxs-lookup"><span data-stu-id="a1756-138">Undo Assembly Posting</span></span>](assembly-how-to-undo-assembly-posting.md)|
|<span data-ttu-id="a1756-139">Få mere at vide om forskellen mellem montagestyklister og produktionsstyklister og de involverede behandlingsforskelle.</span><span class="sxs-lookup"><span data-stu-id="a1756-139">Learn about the difference between assembly BOMs and production BOMs and the involved processing differences.</span></span>|[<span data-ttu-id="a1756-140">Arbejde med styklister</span><span class="sxs-lookup"><span data-stu-id="a1756-140">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)|
|<span data-ttu-id="a1756-141">Lær, hvordan montageforbrug og afgang håndteres, når du bogfører montageordrer, og hvordan de afledte omkostninger for varen og ressourcen behandles og fordeles i regnskabet.</span><span class="sxs-lookup"><span data-stu-id="a1756-141">Learn how assembly consumption and output are handled when you post assembly orders and how the derived item and resource costs are processed and distributed to the general ledger.</span></span>|[<span data-ttu-id="a1756-142">Designoplysninger: Bogføring af montageordre</span><span class="sxs-lookup"><span data-stu-id="a1756-142">Design Details: Assembly Order Posting</span></span>](design-details-assembly-order-posting.md)|  

## <a name="see-also"></a><span data-ttu-id="a1756-143">Se også</span><span class="sxs-lookup"><span data-stu-id="a1756-143">See Also</span></span>  
[<span data-ttu-id="a1756-144">Arbejde med styklister</span><span class="sxs-lookup"><span data-stu-id="a1756-144">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)  
[<span data-ttu-id="a1756-145">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="a1756-145">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="a1756-146">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="a1756-146">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="a1756-147">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a1756-147">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]
