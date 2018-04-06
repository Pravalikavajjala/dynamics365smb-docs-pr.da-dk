---
title: "Sådan konfigureres lokationer til at bruge placeringer | Microsoft Docs"
description: "Placeringer udgør den grundlæggende lagerstruktur og bruges til at fremsætte forslag om placeringen af varer. Når du har oprettet placeringerne, kan du meget præcist definere det indhold, du vil placere på hver placering, eller placeringen kan fungere som en løs placering uden angivet indhold."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: c3e091843b6c2f4a5df0a93c5e70df2c20796a4c
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-locations-to-use-bins"></a><span data-ttu-id="b249f-104">Oprette lokationer til brug af placeringer</span><span class="sxs-lookup"><span data-stu-id="b249f-104">Set Up Locations to Use Bins</span></span>
<span data-ttu-id="b249f-105">Placeringer udgør den grundlæggende lagerstruktur og bruges til at fremsætte forslag om placeringen af varer.</span><span class="sxs-lookup"><span data-stu-id="b249f-105">Bins represent the basic warehouse structure and are used to make suggestions about the placement of items.</span></span> <span data-ttu-id="b249f-106">Når du har oprettet placeringerne, kan du meget præcist definere det indhold, du vil placere på hver placering, eller placeringen kan fungere som en løs placering uden angivet indhold.</span><span class="sxs-lookup"><span data-stu-id="b249f-106">When you have created your bins, you can define very specifically the contents that you want to place in each bin, or the bin can function as a floating bin without specified contents.</span></span>  

<span data-ttu-id="b249f-107">Hvis du vil benytte placeringer på en lokation, skal du først aktivere funktionaliteten på kortet **Lokation**.</span><span class="sxs-lookup"><span data-stu-id="b249f-107">To use the bin functionality at a location, you first activate the functionality on the **Location** card.</span></span> <span data-ttu-id="b249f-108">Derefter kan du designe varestrømmen på placeringen ved at angive placeringskoder i konfigurationsfelter, der repræsenterer forskellige strømme.</span><span class="sxs-lookup"><span data-stu-id="b249f-108">Then you design the item flow at the location by specifying bin codes in setup fields that represent the different flows.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="b249f-109">Placeringskoderne skal være oprettet, før du kan angive placeringskoder på lokationskortet.</span><span class="sxs-lookup"><span data-stu-id="b249f-109">Before you can specify bin codes on the location card, the bin codes must be created.</span></span> <span data-ttu-id="b249f-110">Du kan finde flere oplysninger under [Oprette placeringer](warehouse-how-to-create-individual-bins.md).</span><span class="sxs-lookup"><span data-stu-id="b249f-110">For more information, see [Create Bins](warehouse-how-to-create-individual-bins.md).</span></span>  

## <a name="to-set-up-a-location-to-use-bins"></a><span data-ttu-id="b249f-111">Sådan konfigureres en lokation til at bruge placeringer</span><span class="sxs-lookup"><span data-stu-id="b249f-111">To set up a location to use bins</span></span>  
1.  <span data-ttu-id="b249f-112">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Lokationer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="b249f-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Locations**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="b249f-113">Vælg den lokation, hvor du vil bruge placeringer.</span><span class="sxs-lookup"><span data-stu-id="b249f-113">Select the location where you want to use bins.</span></span>  
3.  <span data-ttu-id="b249f-114">Vælg handlingen **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="b249f-114">Choose the **Edit** action.</span></span>  
4.  <span data-ttu-id="b249f-115">Markér afkrydsningsfeltet **Tvungen placering** i oversigtspanelet **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="b249f-115">On the **Warehouse** FastTab, select the **Bin Mandatory** check box.</span></span>  
5.  <span data-ttu-id="b249f-116">Hvis du ikke bruger styret læg-på-lager og pluk for lokationen, skal du udfylde feltet **Standardplacering** med den metode, der skal bruges, når en vare tildeles en standardplacering.</span><span class="sxs-lookup"><span data-stu-id="b249f-116">If you are not using directed put-away and pick for the location, fill in the **Default Bin Selection** field with the method the system should use when assigning a default bin to an item.</span></span>  
6.  <span data-ttu-id="b249f-117">Åbn kortet for den lokation, du vil konfigurere placeringer for.</span><span class="sxs-lookup"><span data-stu-id="b249f-117">Open the card for the location that you want to set up bins for.</span></span>
7.  <span data-ttu-id="b249f-118">I oversigtspanelet **Placeringer** skal du vælge de placeringer, der skal bruges som standardplaceringer for modtagelser, leverancer samt for indgående, udgående og åbne produktionsplaceringer.</span><span class="sxs-lookup"><span data-stu-id="b249f-118">On the **Bins** FastTab, select the bins that you want to use as the default for receipts, shipments, inbound, outbound, and open shop floor bins.</span></span>  
8.  <span data-ttu-id="b249f-119">De placeringskoder, som du angiver her, vises automatisk i hovederne og på linjerne af de forskellige lagerdokumenter.</span><span class="sxs-lookup"><span data-stu-id="b249f-119">The bin codes you fill in here will appear automatically on the headers and on the lines of various warehouse documents.</span></span> <span data-ttu-id="b249f-120">Standardplaceringerne definerer alle start- og slutplaceringer for varer på lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="b249f-120">The default bins define all starting or ending placements of items in the warehouse.</span></span>  
9.  <span data-ttu-id="b249f-121">Hvis du bruger styret læg-på-lager og pluk, skal du vælge en placering til lagerreguleringerne.</span><span class="sxs-lookup"><span data-stu-id="b249f-121">If you are using directed put-away and pick, select a bin for your warehouse adjustments.</span></span> <span data-ttu-id="b249f-122">Placeringskoden i feltet **Reguleringsplaceringskode** angiver den virtuelle placering, hvor du skal registrere afvigelser i lagerbeholdningen, når du enten registrerer fundne afvigelser registreret i lagerkladden, eller afvigelser, der beregnes, når du registrerer en lagerplaceringsopgørelse.</span><span class="sxs-lookup"><span data-stu-id="b249f-122">The bin code in the **Adjustment Bin Code** field defines the virtual bin in which to record discrepancies in inventory when you register either observed differences registered in the warehouse item journal, or differences calculated when you register a warehouse physical inventory.</span></span>  
10. <span data-ttu-id="b249f-123">Udfyld felterne i oversigtspanelet **Plac.metode**, hvis de er relevante for lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="b249f-123">Fill in the fields on the **Bin Policies** FastTab if they are relevant to your warehouse.</span></span> <span data-ttu-id="b249f-124">De vigtigste felter er **Placeringskap.regel**, **Tillad nedbrydning** og **Læg-på-lager-skabelonkode**.</span><span class="sxs-lookup"><span data-stu-id="b249f-124">The most important fields are **Bin Capacity Policy**, **Allow Breakbulk**, and **Put-away Template Code** fields.</span></span>  
11. <span data-ttu-id="b249f-125">Vælg oversigtspanelet **Lagersted**, og udfyld felterne **Udgående lagerekspeditionstid**, **Indgående lagerekspeditionstid** og **Basiskalenderkode**.</span><span class="sxs-lookup"><span data-stu-id="b249f-125">On the **Warehouse** FastTab, fill in the **Outbound Whse. Handling Time**, **Inbound Whse. Handling Time**, and the **Base Calendar Code** fields.</span></span> <span data-ttu-id="b249f-126">Du kan finde flere oplysninger i [Opsætte basiskalendere](across-how-to-assign-base-calendars.md).</span><span class="sxs-lookup"><span data-stu-id="b249f-126">For more information, see [Set Up Base Calendars](across-how-to-assign-base-calendars.md).</span></span>

## <a name="filling-the-consumption-bin"></a><span data-ttu-id="b249f-127">Udfylde forbrugsplaceringen</span><span class="sxs-lookup"><span data-stu-id="b249f-127">Filling the Consumption Bin</span></span>
<span data-ttu-id="b249f-128">Dette flow-diagram viser, hvordan feltet **Placeringskode** i produktionsordrekomponenter udfyldes i henhold til din lokationsopsætning.</span><span class="sxs-lookup"><span data-stu-id="b249f-128">This flow chart shows how the **Bin Code** field on production order component lines is filled according to your location setup.</span></span>

<span data-ttu-id="b249f-129">![Placeringsrutediagram](media/binflow.png "BinFlow")</span><span class="sxs-lookup"><span data-stu-id="b249f-129">![Bin flow chart](media/binflow.png "BinFlow")</span></span>  

## <a name="see-also"></a><span data-ttu-id="b249f-130">Se også</span><span class="sxs-lookup"><span data-stu-id="b249f-130">See Also</span></span>
[<span data-ttu-id="b249f-131">Logistik</span><span class="sxs-lookup"><span data-stu-id="b249f-131">Warehouse Management</span></span>](warehouse-manage-warehouse.md)  
[<span data-ttu-id="b249f-132">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="b249f-132">Inventory</span></span>](inventory-manage-inventory.md)  
<span data-ttu-id="b249f-133">[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)   </span><span class="sxs-lookup"><span data-stu-id="b249f-133">[Setting Up Warehouse Management](warehouse-setup-warehouse.md)   </span></span>  
<span data-ttu-id="b249f-134">[Montagestyring](assembly-assemble-items.md)  </span><span class="sxs-lookup"><span data-stu-id="b249f-134">[Assembly Management](assembly-assemble-items.md)  </span></span>  
[<span data-ttu-id="b249f-135">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="b249f-135">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="b249f-136">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="b249f-136">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
