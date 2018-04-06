---
title: "Sådan oprettes læg-på-lager-aktiviteter fra interne læg-på-lager-aktiviteter | Microsoft Docs"
description: "Når varer er blevet lagt på plads, og indtil de plukkes til en produktionsordre eller leverance, opbevares de på lagerstedet og indgår i den disponible lagerbeholdning."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/16/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 3faa88fada0969e118c33305b84824e0f0f9b422
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="pick-and-put-away-without-a-source-document"></a><span data-ttu-id="5ed8f-103">Plukke og lægge på lager uden et kildedokument</span><span class="sxs-lookup"><span data-stu-id="5ed8f-103">Pick and Put Away Without a Source Document</span></span>
<span data-ttu-id="5ed8f-104">Når varer er blevet lagt på plads, og indtil de plukkes til en produktionsordre eller leverance, opbevares de på lagerstedet og indgår i den disponible lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-104">After items have been put away and before they are picked to fulfill the needs of a production order or shipment, they are stored in the warehouse as part of available inventory.</span></span>  

<span data-ttu-id="5ed8f-105">Der kan være tilfælde, hvor varer midlertidigt fjernes fra lagerplaceringer, f.eks. fordi de skal fungere som demonstrationsvarer ved en salgspræsentation.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-105">Situations can arise where items must be taken out of the warehouse pick bins temporarily, perhaps to serve as demonstration models in a sales presentation.</span></span> <span data-ttu-id="5ed8f-106">Sådanne varer ejes stadig af virksomheden og er en del af lageret, men de er ikke tilgængelige til pluk.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-106">These items are still owned by the company and are part of inventory, but they are not available for picking.</span></span> <span data-ttu-id="5ed8f-107">De registreres på en specialplacering, som du opretter til formålet; og er teknisk set stadig på lager, selvom de rent fysisk befinder sig på en messe eller i et demonstrationsrum.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-107">They are registered in a special purpose bin that you create for this purpose; technically, the items are in the warehouse, but physically, they could be in a conference or demonstration room.</span></span>  

<span data-ttu-id="5ed8f-108">I andre situationer kan produktionsenheden mod forventning have brug for et par ekstra komponenter til en proces.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-108">In other situations, the production unit might unexpectedly need a few parts for a process.</span></span> <span data-ttu-id="5ed8f-109">Du kan plukke varer til produktionsplaceringer ved interne pluk.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-109">You can pick items for the production bins using the internal pick.</span></span> <span data-ttu-id="5ed8f-110">Når produktionen er færdig, og afgangen er oprettet, bogfører du forbruget af varerne og tømmer produktionsplaceringen, hvilket nedsætter antallet af varer på din lokation.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-110">When the process is over and output is created, you post the consumption of the items and empty the production bin, which in turn decreases the quantity of the item at your location.</span></span>  

<span data-ttu-id="5ed8f-111">På samme måde kan der returneres varer til lagerstedet for at blive lagt på plads.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-111">Likewise, items can be returned to the warehouse to be put away.</span></span> <span data-ttu-id="5ed8f-112">Varerne kan f.eks. være blevet taget fra den disponible beholdning til en produktionsordre, men alligevel ikke være brugt til formålet.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-112">The items may have been taken out of available inventory for a production order, and then not used at all.</span></span> <span data-ttu-id="5ed8f-113">De kan blive en del af den disponible beholdning igen, hvis du lægger dem på lager på placeringen.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-113">To make them part of available inventory again, they must be put away in the bin.</span></span>  

<span data-ttu-id="5ed8f-114">Ved hjælp af **Interne pluk**-aktiviteter kan du udføre læg-på-lager-aktiviteter uden at henvise til et bestemt kildedokument.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-114">The **Internal Put-aways** enables you to perform put-aways without having to refer to a particular source document.</span></span> <span data-ttu-id="5ed8f-115">Du kan nemt angive alle de nødvendige oplysninger til oprettelse af en lagerinstruktion.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-115">You can easily set up all the information you need to create a put-away warehouse instruction.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="5ed8f-116">Hvis du ikke benytter interne pluk og interne læg-på-lager-aktiviteter, kan du udføre disse reguleringer ved hjælp af metoden til flytning af varer fra placering til placering eller til bogføring af mængdereguleringer på en placering.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-116">If you are not using internal picks and internal put-aways, these adjustments can be performed using the methods to move items from bin to bin or to post quantity adjustments in a bin.</span></span>  
>   
>  <span data-ttu-id="5ed8f-117">Når lokationen bruger styret læg-på-lager og pluk og derfor placeringstyper, kan du ikke manuelt flytte varer ind eller ud af en placering af typen MODTAG, fordi varer, der findes på en placering af typen MODTAG, skal registreres som lagt på lager, før de bliver en del af den tilgængelige lagerbeholdning.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-117">When the location uses directed put-away and pick, and therefore uses bin types, you cannot manually move items in or out of a bin of bin type RECEIVE, because items that are in a RECEIVE-type bin must be registered as being put away before they are part of available inventory.</span></span>  

## <a name="to-create-an-internal-pick"></a><span data-ttu-id="5ed8f-118">Sådan oprettes et internt pluk</span><span class="sxs-lookup"><span data-stu-id="5ed8f-118">To create an internal pick</span></span>  
1.  <span data-ttu-id="5ed8f-119">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Internt lagerpluk**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Whse. Internal Pick**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5ed8f-120">Udfyld feltet **Nummer**.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-120">Fill in the **No.**</span></span> <span data-ttu-id="5ed8f-121">og **Til placeringskode** i oversigtspanelet **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-121">field and the **To Bin Code** field on the **General** FastTab.</span></span> <span data-ttu-id="5ed8f-122">Feltet **Til placeringskode** angiver den placering, hvor varerne skal hentes.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-122">The **To Bin Code** field specifies the bin from which you want to get the items.</span></span> <span data-ttu-id="5ed8f-123">I forbindelse med produktion er denne placering placeringen for indgående produktion eller åben produktion.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-123">For production purposes, this bin would be the inbound production bin or the open shop bin.</span></span> <span data-ttu-id="5ed8f-124">I andre forbindelser skal du vælge en Til placeringskode med en placeringstype, som ikke bruges til pluk, sandsynligvis en leveranceplacering eller specialplacering.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-124">For other purposes, choose a To Bin Code of a bin type that is not used for picking, most likely a staging, shipping or special purpose bin.</span></span>  
3.  <span data-ttu-id="5ed8f-125">Vælg en vare i feltet **Varenr.** , og indtast de antal, der skal plukkes.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-125">Select an item in the **Item No.** field, and fill in the quantities you want to pick.</span></span>  
4. <span data-ttu-id="5ed8f-126">Vælg handlingen **Opret pluk**.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-126">Choose the **Create Pick** action.</span></span> <span data-ttu-id="5ed8f-127">Der er nu en lagerplukinstruktion klar til en lagermedarbejder.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-127">A warehouse pick instruction is now ready for a warehouse employee to perform.</span></span>  

## <a name="to-create-an-internal-put-away"></a><span data-ttu-id="5ed8f-128">Sådan oprettes en intern læg-på-lager-aktivitet</span><span class="sxs-lookup"><span data-stu-id="5ed8f-128">To create an internal put-away</span></span>  
1.  <span data-ttu-id="5ed8f-129">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Intern læg-på-lager (logistik)**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-129">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Whse. Internal Put-away**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="5ed8f-130">Udfyld feltet **Nummer**.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-130">Fill in the **No.**</span></span> <span data-ttu-id="5ed8f-131">og **Fra placeringskode** i oversigtspanelet **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-131">and **From Bin Code** fields on the **General** FastTab.</span></span> <span data-ttu-id="5ed8f-132">Feltet **Fra placeringskode** angiver stedet for den placering, som varerne returneres fra til lagerstedet, f.eks. fra produktionsenheden.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-132">The **From Bin Code** field specifies the bin where the items being returned to the warehouse, perhaps from production, are located.</span></span>  
3.  <span data-ttu-id="5ed8f-133">Angiv varenumre og antal på linjerne.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-133">Fill in the item numbers and quantities on the lines.</span></span>  
4.  <span data-ttu-id="5ed8f-134">Vælg handlingen **Opret læg-på-lager**.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-134">Choose the **Create Put-away** action.</span></span> <span data-ttu-id="5ed8f-135">Der er nu en læg-på-lager-instruktion klar til en lagermedarbejder.</span><span class="sxs-lookup"><span data-stu-id="5ed8f-135">A warehouse put-away instruction is now ready for a warehouse employee to perform.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5ed8f-136">Se også</span><span class="sxs-lookup"><span data-stu-id="5ed8f-136">See Also</span></span>  
[<span data-ttu-id="5ed8f-137">Logistik</span><span class="sxs-lookup"><span data-stu-id="5ed8f-137">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="5ed8f-138">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="5ed8f-138">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="5ed8f-139">[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="5ed8f-139">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="5ed8f-140">[Montagestyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="5ed8f-140">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="5ed8f-141">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="5ed8f-141">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="5ed8f-142">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5ed8f-142">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
