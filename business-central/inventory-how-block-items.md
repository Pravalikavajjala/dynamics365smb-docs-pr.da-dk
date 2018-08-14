---
title: "Sådan spærres varer mod salg eller køb"
description: "I Business Central kan en vare være markeret som spærret for salg, spærret for køb eller spærret i alle sammenhænge."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/23/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: c6f10f8252c00bf0a599f9fa794ee36c41ce92be
ms.openlocfilehash: 2f8be478dda62fef2cb34397de488f45d4fcfc0c
ms.contentlocale: da-dk
ms.lasthandoff: 07/30/2018

---
# <a name="block-items-from-sales-or-purchasing"></a><span data-ttu-id="9c3dd-103">Spærre varer mod salg eller køb</span><span class="sxs-lookup"><span data-stu-id="9c3dd-103">Block Items from Sales or Purchasing</span></span>
<span data-ttu-id="9c3dd-104">Du kan spærre for, at en vare angives på salgs- eller købslinjer og for, at den bogføres i nogen posteringer.</span><span class="sxs-lookup"><span data-stu-id="9c3dd-104">You can block an item from being entered on sales or purchase lines, and you can block it from being posted in any transaction.</span></span>  

<span data-ttu-id="9c3dd-105">Tabellen nedenfor viser, hvad der sker, når varer spærres.</span><span class="sxs-lookup"><span data-stu-id="9c3dd-105">The following table illustrates what occurs when items are blocked.</span></span>  

|<span data-ttu-id="9c3dd-106">Indstilling</span><span class="sxs-lookup"><span data-stu-id="9c3dd-106">Option</span></span>|<span data-ttu-id="9c3dd-107">Description</span><span class="sxs-lookup"><span data-stu-id="9c3dd-107">Description</span></span>|  
|--------------------|------------|  
|<span data-ttu-id="9c3dd-108">**Spærret salg**</span><span class="sxs-lookup"><span data-stu-id="9c3dd-108">**Sales Blocked**</span></span>|<span data-ttu-id="9c3dd-109">Du kan ikke angive varen i et salgsdokument eller i en salgsvarekladde.</span><span class="sxs-lookup"><span data-stu-id="9c3dd-109">You cannot enter the item in a sales document or in a sales item journal.</span></span>|  
|<span data-ttu-id="9c3dd-110">**Spærret køb**</span><span class="sxs-lookup"><span data-stu-id="9c3dd-110">**Purchasing Blocked**</span></span>|<span data-ttu-id="9c3dd-111">Du kan ikke angive varen i et købsdokument, i en købsvarekladde eller i købsplanlægningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="9c3dd-111">You cannot enter the item in a purchase document, in a purchase item journal, or in purchase planning processes.</span></span>|  
|<span data-ttu-id="9c3dd-112">**Spærret**</span><span class="sxs-lookup"><span data-stu-id="9c3dd-112">**Blocked**</span></span>|<span data-ttu-id="9c3dd-113">Du kan ikke bruge varen til nogen varetransaktioner.</span><span class="sxs-lookup"><span data-stu-id="9c3dd-113">You cannot use the item for any item transaction.</span></span> <span data-ttu-id="9c3dd-114">Du kan finde flere oplysninger om spærring af en vare i alle sammenhænge på varekortet.</span><span class="sxs-lookup"><span data-stu-id="9c3dd-114">For more information about blocking an item for all purposes, see Item Card.</span></span>|  

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a><span data-ttu-id="9c3dd-115">Sådan spærrer du for, at en vare kan angives på salgslinjer</span><span class="sxs-lookup"><span data-stu-id="9c3dd-115">To block an item from being entered on sales lines</span></span>  

1.  <span data-ttu-id="9c3dd-116">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="9c3dd-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="9c3dd-117">Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret salg**.</span><span class="sxs-lookup"><span data-stu-id="9c3dd-117">Select the item that you want to block, and then select the **Sales Blocked** check box.</span></span>  

<span data-ttu-id="9c3dd-118">Hvis du forsøger at angive varen på et salgsdokument eller kladdelinje, får du nu en fejlmeddelelse om, at varen er spærret.</span><span class="sxs-lookup"><span data-stu-id="9c3dd-118">If you try to enter the item on a sales document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a><span data-ttu-id="9c3dd-119">Sådan spærrer du for, at en vare kan angives på købslinjer</span><span class="sxs-lookup"><span data-stu-id="9c3dd-119">To block an item from being entered on purchase lines</span></span>  

1.  <span data-ttu-id="9c3dd-120">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="9c3dd-120">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="9c3dd-121">Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret køb**.</span><span class="sxs-lookup"><span data-stu-id="9c3dd-121">Select the item that you want to block, and then select the **Purchasing Blocked** check box.</span></span>  

<span data-ttu-id="9c3dd-122">Hvis du forsøger at angive varen på et købsdokument eller kladdelinje, får du nu en fejlmeddelelse om, at varen er spærret.</span><span class="sxs-lookup"><span data-stu-id="9c3dd-122">If you try to enter the item on a purchase document or journal line, you will now get an error message that the item is blocked.</span></span>

## <a name="to-block-an-item-from-being-posted"></a><span data-ttu-id="9c3dd-123">Sådan spærrer du for, at en vare kan bogføres</span><span class="sxs-lookup"><span data-stu-id="9c3dd-123">To block an item from being posted</span></span>
1. <span data-ttu-id="9c3dd-124">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="9c3dd-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.</span></span>
2. <span data-ttu-id="9c3dd-125">Vælg den vare, du vil spærre, og marker derefter afkrydsningsfeltet **Spærret**.</span><span class="sxs-lookup"><span data-stu-id="9c3dd-125">Select the item that you want to block, and then select the **Blocked** check box.</span></span>

<span data-ttu-id="9c3dd-126">Hvis du forsøger at bogføre en transaktionstype for varen, får du nu en fejlmeddelelse om, at varen er spærret.</span><span class="sxs-lookup"><span data-stu-id="9c3dd-126">If you try to post any type of transaction for the item, you will now get an error message that the item is blocked.</span></span>

## <a name="see-also"></a><span data-ttu-id="9c3dd-127">Se også</span><span class="sxs-lookup"><span data-stu-id="9c3dd-127">See Also</span></span>  
[<span data-ttu-id="9c3dd-128">Registrere nye varer</span><span class="sxs-lookup"><span data-stu-id="9c3dd-128">Register New Items</span></span>](inventory-how-register-new-items.md)  
[<span data-ttu-id="9c3dd-129">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="9c3dd-129">Inventory</span></span>](inventory-manage-inventory.md)  
