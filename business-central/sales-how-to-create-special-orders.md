---
title: "Sådan oprettes specialordrer | Microsoft Docs"
description: "Du kan oprette en specialordre på en bestemt katalogvare, der skal sendes til en bestemt kunde. Din leverandør sender varen til dit lagersted, og derfra kan du levere varen til debitoren, enten alene eller sammen med andre varer fra en anden ordre."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 84b7a66734b3da5bdbc474bc43e463481c7f6ba5
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="create-special-orders"></a><span data-ttu-id="7a520-104">Oprette specialordrer</span><span class="sxs-lookup"><span data-stu-id="7a520-104">Create Special Orders</span></span>
<span data-ttu-id="7a520-105">Du kan oprette en specialordre på en bestemt katalogvare, der skal sendes til en bestemt kunde.</span><span class="sxs-lookup"><span data-stu-id="7a520-105">You can create a special order for a specific nonstock item to be shipped to a specific customer.</span></span> <span data-ttu-id="7a520-106">Din leverandør sender varen til dit lagersted, og derfra kan du levere varen til debitoren, enten alene eller sammen med andre varer fra en anden ordre.</span><span class="sxs-lookup"><span data-stu-id="7a520-106">Your vendor ships the item to your warehouse and you can then ship the item on to your customer either independently or together with other items on another order.</span></span>  

<span data-ttu-id="7a520-107">Specialordrer medfører, at købs- og salgsordrer sammenkædes for at sikre, at en bestemt katalogvare plukkes og leveres til kunden.</span><span class="sxs-lookup"><span data-stu-id="7a520-107">Special orders imply that the purchase and sales order are linked to ensure that the specific nonstock item is picked and delivered to the customer.</span></span>  

<span data-ttu-id="7a520-108">Før du kan bruge denne funktion, skal du oprette den kunde, den leverandør, og det varekort, som skal bruges i ordren.</span><span class="sxs-lookup"><span data-stu-id="7a520-108">Before you can use this feature, you must first set up the customer, vendor, and item cards necessary for the order.</span></span>  

## <a name="to-create-a-special-order"></a><span data-ttu-id="7a520-109">Sådan oprettes en specialordre</span><span class="sxs-lookup"><span data-stu-id="7a520-109">To create a special order</span></span>  
1.  <span data-ttu-id="7a520-110">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Salgsordre**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="7a520-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Order**, and then choose the related link.</span></span>  
2. <span data-ttu-id="7a520-111">Vælg handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7a520-111">Choose the **New** action.</span></span> <span data-ttu-id="7a520-112">Opret og udfyld en  salgsordre for varen.</span><span class="sxs-lookup"><span data-stu-id="7a520-112">Create and fill in a  sales order for the item.</span></span> <span data-ttu-id="7a520-113">Du kan finde flere oplysninger i [Sælge produkter](sales-how-sell-products.md).</span><span class="sxs-lookup"><span data-stu-id="7a520-113">For more information, see [Sell Products](sales-how-sell-products.md).</span></span>
3.  <span data-ttu-id="7a520-114">Udfyld salgslinjen på oversigtspanelet **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="7a520-114">On the **Lines** FastTab, fill in the sales line.</span></span> <span data-ttu-id="7a520-115">I feltet **Indkøbskode** skal du vælge en indkøbskode, hvor der er en markering i feltet **Specialordre**.</span><span class="sxs-lookup"><span data-stu-id="7a520-115">In the **Purchasing Code** field, select a purchasing code that has the **Special Order** field selected.</span></span>

    <span data-ttu-id="7a520-116">Du skal nu oprette købsordren fra en indkøbskladde.</span><span class="sxs-lookup"><span data-stu-id="7a520-116">You must now create a purchase order from a requisition worksheet.</span></span>  
4. <span data-ttu-id="7a520-117">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Indkøbskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="7a520-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Requisition Worksheet**, and then choose the related link.</span></span>  
5. <span data-ttu-id="7a520-118">Vælg handlingen **Specialordre**, og vælg derefter handlingen **Hent salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="7a520-118">Choose the **Special Order** action, and then choose the **Get Sales Orders** action.</span></span>  
6.  <span data-ttu-id="7a520-119">I vinduet **Hent salgsordrer** skal du vise de resultater, hvor **Bilagsnr.** er nummeret på salgsordren.</span><span class="sxs-lookup"><span data-stu-id="7a520-119">In the **Get Sales Orders** window, show results where the **Document No.** is the sales order number.</span></span> <span data-ttu-id="7a520-120">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a520-120">Choose the **OK** button.</span></span> <span data-ttu-id="7a520-121">Der oprettes en indkøbskladdelinje for varen.</span><span class="sxs-lookup"><span data-stu-id="7a520-121">A requisition worksheet line is created for the item.</span></span>  
7.  <span data-ttu-id="7a520-122">Vælg **Ny** i feltet **Aktionsmeddelelse** på indkøbskladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="7a520-122">On the requisition worksheet line, in the **Action Message** field, select **New**.</span></span>  
8.  <span data-ttu-id="7a520-123">I vinduet **Indkøbskladde** skal du vælge handlingen **Udfør aktionsmeddelelse**.</span><span class="sxs-lookup"><span data-stu-id="7a520-123">In the **Req. Worksheet** window, choose the **Carry Out Action Message** action.</span></span> <span data-ttu-id="7a520-124">Vinduet **Udfør aktionsmeddl. - Indk.** åbnes.</span><span class="sxs-lookup"><span data-stu-id="7a520-124">The **Carry Out Action Msg. - Req.** window opens.</span></span> <span data-ttu-id="7a520-125">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a520-125">Choose the **OK** button.</span></span>  

    <span data-ttu-id="7a520-126">Du får vist en meddelelse om, at købsordrerne er oprettet.</span><span class="sxs-lookup"><span data-stu-id="7a520-126">A message appears telling you that the purchase orders have been created.</span></span> <span data-ttu-id="7a520-127">Vælg knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a520-127">Choost the **OK** button.</span></span>  

<span data-ttu-id="7a520-128">En indkøbsordre, der er oprettet som en specialordre for en salgsordre, respekteres i planlægningssystemet, når efterspørgsel og udbud afstemmes.</span><span class="sxs-lookup"><span data-stu-id="7a520-128">A purchase order created as a special order for a sales order is respected by the planning system as it balances demand and supply.</span></span> <span data-ttu-id="7a520-129">Dvs. at købsordren (forsyning) forbliver tilknyttet salgsordren (behov), også selvom den pågældende købsordre kunne forsyne et andet tidligere behov.</span><span class="sxs-lookup"><span data-stu-id="7a520-129">That is, the purchase order (supply) remains linked to the sales order (demand), even if that purchase order could supply another earlier demand.</span></span> <span data-ttu-id="7a520-130">Du kan finde flere oplysninger i [Designoplysninger: Genbestillingsmetoder](design-details-reservation-order-tracking-and-action-messaging.md).</span><span class="sxs-lookup"><span data-stu-id="7a520-130">For more information, see [Design Details: Reordering Policies](design-details-reservation-order-tracking-and-action-messaging.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="7a520-131">Du kan ikke bruge funktionen til specialordre, hvis varen allerede er reserveret.</span><span class="sxs-lookup"><span data-stu-id="7a520-131">You cannot use the special order functionality if the item is already reserved.</span></span> <span data-ttu-id="7a520-132">For varer, der sælges på specialordrer, skal du derfor sørge for, at feltet **Reserver** på varekortet ikke er angivet til **Altid**.</span><span class="sxs-lookup"><span data-stu-id="7a520-132">Therefore, for items that are sold on special orders, make sure the **Reserve** field on the item card is not set to **Always**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7a520-133">Se også</span><span class="sxs-lookup"><span data-stu-id="7a520-133">See Also</span></span>  
[<span data-ttu-id="7a520-134">Arbejde med katalogvarer</span><span class="sxs-lookup"><span data-stu-id="7a520-134">Work with Nonstock Items</span></span>](inventory-how-work-nonstock-items.md)  
[<span data-ttu-id="7a520-135">Salg</span><span class="sxs-lookup"><span data-stu-id="7a520-135">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="7a520-136">[Foretage direkte leveringer](sales-how-drop-shipment.md) </span><span class="sxs-lookup"><span data-stu-id="7a520-136">[Make Drop Shipments](sales-how-drop-shipment.md) </span></span>  
[<span data-ttu-id="7a520-137">Designoplysninger: Genbestillingsmetoder</span><span class="sxs-lookup"><span data-stu-id="7a520-137">Design Details: Reordering Policies</span></span>](design-details-reservation-order-tracking-and-action-messaging.md)  
<span data-ttu-id="7a520-138">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7a520-138">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
