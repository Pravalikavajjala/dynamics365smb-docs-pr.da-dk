---
title: Administrere lager | Microsoft Docs
description: "Bruges til at styre de fysiske produkter, som du handler med, f.eks. håndtering af lagerbeholdning på lagerstedet."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f5b69dce5426f828572fa57e73c03ac35332e101
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---

# <a name="inventory"></a><span data-ttu-id="fdb34-103">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="fdb34-103">Inventory</span></span>
<span data-ttu-id="fdb34-104">For hvert fysisk produkt, som du vil handle med, skal du oprette et varekort af typen **Lager**.</span><span class="sxs-lookup"><span data-stu-id="fdb34-104">For each physical product that you trade in, you must create an item card of type **Inventory**.</span></span> <span data-ttu-id="fdb34-105">De varer, du tilbyder kunderne, men ikke lagerfører, kan du registrere som katalogvarer, som du kan konvertere til lagervarer, når det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="fdb34-105">Items that you offer to customers but do not keep in inventory you can register as nonstock items, which you can convert to inventory items when necessary.</span></span> <span data-ttu-id="fdb34-106">Du kan øge eller mindske antallet af en vare på lager ved at bogføre direkte til vareposterne, f.eks. efter en fysisk optælling eller hvis du ikke registrerer indkøb.</span><span class="sxs-lookup"><span data-stu-id="fdb34-106">You can increase or decrease the quantity of an item in inventory by posting directly to the item ledger entries, for example, after a physical count or if you do not record purchases.</span></span>

<span data-ttu-id="fdb34-107">Lagerforøgelser og -reduktioner registreres naturligt også, når du bogfører købs- og salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="fdb34-107">Inventory increases and decreases are naturally also recorded when you post purchase and sales documents respectively.</span></span> <span data-ttu-id="fdb34-108">Du kan finde flere oplysninger i [Registrere køb](purchasing-how-record-purchases.md) og [Sælge produkter](sales-how-sell-products.md) og [Fakturere salg](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="fdb34-108">For more information, see [Record Purchases](purchasing-how-record-purchases.md), [Sell Products](sales-how-sell-products.md), and [Invoice Sales](sales-how-invoice-sales.md).</span></span> <span data-ttu-id="fdb34-109">Overførsler mellem lokationer ændrer lagerbeholdningen på tværs af virksomhedens lagersteder.</span><span class="sxs-lookup"><span data-stu-id="fdb34-109">Transfers between locations changes inventory quantities across your company's warehouses.</span></span>   

<span data-ttu-id="fdb34-110">Hvis du vil øge dit overblik over varerne og lettere kunne finde dem, kan du kategorisere varer og give dem attributter, du kan søge og sortere efter.</span><span class="sxs-lookup"><span data-stu-id="fdb34-110">To increase your overview of items and to help you find them, you can categorize items and give them attributes to search and sort by.</span></span>

> [!NOTE]
> <span data-ttu-id="fdb34-111">Den fysiske håndtering af varer kaldes lageraktiviteter.</span><span class="sxs-lookup"><span data-stu-id="fdb34-111">The physical handling of items is referred to as warehouse activities.</span></span> <span data-ttu-id="fdb34-112">Du kan finde flere oplysninger i [Logistik](warehouse-manage-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="fdb34-112">For more information, see [Warehouse Management](warehouse-manage-warehouse.md).</span></span>

## <a name="inventory-reconciliation"></a><span data-ttu-id="fdb34-113">Lagerafstemning</span><span class="sxs-lookup"><span data-stu-id="fdb34-113">Inventory Reconciliation</span></span>
<span data-ttu-id="fdb34-114">Når du bogfører lagertransaktioner, f.eks. salgsleverancer, købsfakturaer eller lagerreguleringer, registreres ændringen i varepriser i værdiposterne.</span><span class="sxs-lookup"><span data-stu-id="fdb34-114">When you post inventory transactions, such as sales shipments, purchase invoices, or inventory adjustments, the changed item costs are recorded in item value entries.</span></span> <span data-ttu-id="fdb34-115">For at afspejle ændringen af lagerværdien i dine finansielle regnskaber bogføres lagerværdien automatisk i de relaterede lagerkonti i finansbogholderiet.</span><span class="sxs-lookup"><span data-stu-id="fdb34-115">To reflect this change of inventory value in your financial books, the inventory costs are automatically posted to the related inventory accounts in the general ledger.</span></span> <span data-ttu-id="fdb34-116">For hver lagertransaktion du bogfører, bogføres den relevante værdi på lagerkontoen, reguleringskontoen og vareforbrugskontoen i finansregnskabet.</span><span class="sxs-lookup"><span data-stu-id="fdb34-116">For each inventory transaction that you post, the appropriate values are posted to the inventory account, adjustment account, and COGS account in the general ledger.</span></span> <span data-ttu-id="fdb34-117">Du kan finde flere oplysninger i [Afstemme kostpriser med finansregnskabet](finance-how-to-post-inventory-costs-to-the-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="fdb34-117">For more information, see [Reconcile Inventory Costs with the General Ledger](finance-how-to-post-inventory-costs-to-the-general-ledger.md).</span></span>

<span data-ttu-id="fdb34-118">Selvom lagerværdien automatisk bogføres i Finans, er det stadig nødvendigt at sikre, at værdien af varerne overføres til de relaterede udgående transaktioner, f.eks salg eller overflytninger. Dette er især vigtigt i de situationer, hvor du sælger varer, inden du fakturerer købet af varerne.</span><span class="sxs-lookup"><span data-stu-id="fdb34-118">Even though inventory costs are automatically posted to the general ledger, it is still necessary to ensure that the costs of goods are forwarded to the related outbound sales transaction, especially in situations where you sell goods before you invoice the purchase of those goods.</span></span> <span data-ttu-id="fdb34-119">Dette omtales som omkostningsregulering.</span><span class="sxs-lookup"><span data-stu-id="fdb34-119">This is referred to as cost adjustment.</span></span> <span data-ttu-id="fdb34-120">Varepriser reguleres automatisk, når du bogfører transaktioner, men du kan også justere varepriser manuelt.</span><span class="sxs-lookup"><span data-stu-id="fdb34-120">Item costs are automatically adjusted when you post item transactions, but you can also adjust item costs manually.</span></span> <span data-ttu-id="fdb34-121">Du kan finde flere oplysninger i [Regulere varepriser](inventory-how-adjust-item-costs.md).</span><span class="sxs-lookup"><span data-stu-id="fdb34-121">For more information, see [Adjust Item Costs](inventory-how-adjust-item-costs.md).</span></span>

|<span data-ttu-id="fdb34-122">Til</span><span class="sxs-lookup"><span data-stu-id="fdb34-122">To</span></span> |<span data-ttu-id="fdb34-123">Se</span><span class="sxs-lookup"><span data-stu-id="fdb34-123">See</span></span> |
|---|----|
|<span data-ttu-id="fdb34-124">Oprette varekort for lagervarer, som du handler med.</span><span class="sxs-lookup"><span data-stu-id="fdb34-124">Create item cards for inventory items that you trade in.</span></span>|[<span data-ttu-id="fdb34-125">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="fdb34-125">Register New Items</span></span>](inventory-how-register-new-items.md)|
|<span data-ttu-id="fdb34-126">Strukturer overordnede varer, du sælger som pakker, der består af den overordnede vares komponenter eller af montage til ordre- eller montage til lager-pakker.</span><span class="sxs-lookup"><span data-stu-id="fdb34-126">Structure parent items that you sell as kits consisting of the parent's components or that you assemble to order or to stock.</span></span>|[<span data-ttu-id="fdb34-127">Arbejde med styklister</span><span class="sxs-lookup"><span data-stu-id="fdb34-127">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)|
|<span data-ttu-id="fdb34-128">Hav altid overblik over varer, og få hjælp til at finde og sortere varer ved at arrangere dem i kategorier.</span><span class="sxs-lookup"><span data-stu-id="fdb34-128">Maintain an overview of items and help you find and sort items by organizing them in categories.</span></span>|[<span data-ttu-id="fdb34-129">Kategorisere varer</span><span class="sxs-lookup"><span data-stu-id="fdb34-129">Categorize Items</span></span>](inventory-how-categorize-items.md)|
|<span data-ttu-id="fdb34-130">Tildel vareattributter af forskellige værdityper til dine varer for lettere at kunne sortere og finde varer.</span><span class="sxs-lookup"><span data-stu-id="fdb34-130">Assign item attributes of different value types to your items to help you sort and find items.</span></span>|[<span data-ttu-id="fdb34-131">Arbejde med vareattributter</span><span class="sxs-lookup"><span data-stu-id="fdb34-131">Work with Item Attributes</span></span>](inventory-how-work-item-attributes.md)|
|<span data-ttu-id="fdb34-132">Opret særlige varekort for de varer, du tilbyder kunderne, men ikke lagerfører.</span><span class="sxs-lookup"><span data-stu-id="fdb34-132">Create special item cards for items that you offer to customers but do not maintain inventory for.</span></span>|[<span data-ttu-id="fdb34-133">Arbejde med katalogvarer</span><span class="sxs-lookup"><span data-stu-id="fdb34-133">Work with Nonstock Items</span></span>](inventory-how-work-nonstock-items.md)|
|<span data-ttu-id="fdb34-134">Foretag fysisk optælling, foretag negative eller positive reguleringer, og rediger oplysninger, f.eks. placering eller lotnummer, på vareposter.</span><span class="sxs-lookup"><span data-stu-id="fdb34-134">Perform physical counting, make negative or positive adjustments, and change information, such as location or lot number, on item ledger entries.</span></span>|[<span data-ttu-id="fdb34-135">Tælle, justere og ompostere lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="fdb34-135">Count, Adjust, and Reclassify Inventory Inventory</span></span>](inventory-how-count-adjust-reclassify.md)|
|<span data-ttu-id="fdb34-136">Få vist tilgængeligheden af varer pr. lokation og pr. periode efter salgs- eller købshændelse eller efter deres brug i montage- eller produktionsstyklister.</span><span class="sxs-lookup"><span data-stu-id="fdb34-136">View the availability of items per location, by period, by sales or purchase event, or by their use on assembly or production BOMs.</span></span>|[<span data-ttu-id="fdb34-137">Vise varedisponering</span><span class="sxs-lookup"><span data-stu-id="fdb34-137">View the Availability of Items</span></span>](inventory-how-availability-overview.md)|
|<span data-ttu-id="fdb34-138">Overflyt lagervarer mellem lokationer med overflytningsordrer for at styre lageraktiviteter eller med vareomposteringskladden.</span><span class="sxs-lookup"><span data-stu-id="fdb34-138">Transfer inventory items between locations with transfer orders, to manage warehouse activities, or with the item reclassification journal.</span></span>|[<span data-ttu-id="fdb34-139">Overflytte lagerbeholdning mellem lokationer</span><span class="sxs-lookup"><span data-stu-id="fdb34-139">Transfer Inventory Between Locations</span></span>](inventory-how-transfer-between-locations.md)|
|<span data-ttu-id="fdb34-140">Reservere lagervarer eller indgående varer til salgsordrer, købsordrer, serviceordrer, montageordrer eller produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="fdb34-140">Reserve inventory or inbound items for sales orders, purchase orders, service orders, assembly orders, or production orders.</span></span>|[<span data-ttu-id="fdb34-141">Reservere varer</span><span class="sxs-lookup"><span data-stu-id="fdb34-141">Reserve Items</span></span>](inventory-how-to-reserve-items.md)|
|<span data-ttu-id="fdb34-142">Tildel serienumre eller lotnumre til en udgående eller indgående dokument- eller kladdelinje, for eksempel for at spore varer i tilfælde af tilbagekaldelser.</span><span class="sxs-lookup"><span data-stu-id="fdb34-142">Assign serial numbers or lot numbers to any outbound or inbound document or journal line, for example to track items in case of recalls.</span></span>|[<span data-ttu-id="fdb34-143">Arbejde med serienumre og lotnumre</span><span class="sxs-lookup"><span data-stu-id="fdb34-143">Work with Serial and Lot Numbers</span></span>](inventory-how-work-item-tracking.md)|
|<span data-ttu-id="fdb34-144">Find, hvor et serie- eller lotnummer blev brugt i forsyningskæden, f.eks. i tilfælde af tilbagekaldelse.</span><span class="sxs-lookup"><span data-stu-id="fdb34-144">Find where any serial or lot number was used in its supply chain, for example in recall situations.</span></span>|[<span data-ttu-id="fdb34-145">Spore vare via varesporing</span><span class="sxs-lookup"><span data-stu-id="fdb34-145">Trace Item-Tracked Items</span></span>](inventory-how-to-trace-item-tracked-items.md)|
|<span data-ttu-id="fdb34-146">Administrer forretningsaktiviteter på salgskontorer, indkøbsafdelinger eller fabriksplanlægningskontor på tværs af flere lokationer.</span><span class="sxs-lookup"><span data-stu-id="fdb34-146">Manage business operations in sales offices, a purchasing departments, or plant planning offices across multiple locations.</span></span>|[<span data-ttu-id="fdb34-147">Arbejde med ansvarscentre</span><span class="sxs-lookup"><span data-stu-id="fdb34-147">Work with Responsibility Centers</span></span>](inventory-responsibility-centers.md)|

## <a name="see-also"></a><span data-ttu-id="fdb34-148">Se også</span><span class="sxs-lookup"><span data-stu-id="fdb34-148">See Also</span></span>  
[<span data-ttu-id="fdb34-149">Logistik</span><span class="sxs-lookup"><span data-stu-id="fdb34-149">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="fdb34-150">Køb</span><span class="sxs-lookup"><span data-stu-id="fdb34-150">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="fdb34-151">[Salg](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="fdb34-151">[Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="fdb34-152">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="fdb34-152">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="fdb34-153">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="fdb34-153">General Business Functionality</span></span>](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]
