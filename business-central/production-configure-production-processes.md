---
title: Konfigurere produktionsprocesser | Microsoft Docs
description: "Hvis du vil konvertere materialer til fremstillede færdigvarer, skal produktionsressourcer, f.eks. styklister, ruter, maskinoperatører og maskiner, konfigureres i systemet."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/04/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 2419755f5788eb7cb8ed464ac97fccd7e63e795c
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-manufacturing"></a><span data-ttu-id="58885-103">Konfigurere produktion</span><span class="sxs-lookup"><span data-stu-id="58885-103">Setting Up Manufacturing</span></span>
<span data-ttu-id="58885-104">Hvis du vil konvertere materialer til fremstillede færdigvarer, skal produktionsressourcer, f.eks. styklister, ruter, maskinoperatører og maskiner, konfigureres i systemet.</span><span class="sxs-lookup"><span data-stu-id="58885-104">To convert material into produced end items, production resources, such as bills of material, routings, machine operators, and machinery must be set up in the system.</span></span>

<span data-ttu-id="58885-105">Operatører og maskiner repræsenteres i systemet af produktionsressourcer, der kan være organiseret i arbejdscentre og arbejdscentergrupper.</span><span class="sxs-lookup"><span data-stu-id="58885-105">Operators and machines are represented in the system as machine centers that may be organized in work centers and work center groups.</span></span> <span data-ttu-id="58885-106">Når disse ressourcer er etableret, kan der indlæses operationer i henhold til varens definerede materialestykliste og processtruktur (rute) og i henhold til produktionsressourcens eller arbejdscentrets kapacitet.</span><span class="sxs-lookup"><span data-stu-id="58885-106">When these resources are established, they can be loaded with operations according to the item's defined material (BOM) and process (routing) structure, and according to the capacity of the machine or work center.</span></span> <span data-ttu-id="58885-107">Du kan også angive produktionskapaciteten for hver ressource.</span><span class="sxs-lookup"><span data-stu-id="58885-107">You can also set the production capacity of each resource.</span></span> <span data-ttu-id="58885-108">Kapaciteten defineres af den tilgængelige arbejdstid i produktionsressourcerne og arbejdscentrene, som styres af kalendere for hvert niveau.</span><span class="sxs-lookup"><span data-stu-id="58885-108">Capacity is defined by the work time available in the machine and work centers, and is governed by calendars for each level.</span></span> <span data-ttu-id="58885-109">En arbejdscenterkalender angiver arbejdsdage eller -timer, skiftehold, fridage og fravær, som bestemmer arbejdscentrets disponible bruttokapacitet, som typisk måles i minutter.</span><span class="sxs-lookup"><span data-stu-id="58885-109">A work center calendar specifies the working days or hours, shifts, holidays, and absence that determine the work center’s gross available capacity (typically measured in minutes).</span></span> <span data-ttu-id="58885-110">Alt dette bestemmes af de effektivitets- og kapacitetsværdier, der er defineret.</span><span class="sxs-lookup"><span data-stu-id="58885-110">All of this is determined by defined efficiency and capacity values.</span></span>  

<span data-ttu-id="58885-111">Når du har defineret en produktion, kan du planlægge og udføre produktionsordrer.</span><span class="sxs-lookup"><span data-stu-id="58885-111">When you have set up manufacturing, you can plan and execute production orders.</span></span> <span data-ttu-id="58885-112">Du kan finde flere oplysninger i [Planlægning](production-planning.md) og [Produktion](production-manage-manufacturing.md).</span><span class="sxs-lookup"><span data-stu-id="58885-112">For more information, see [Planning](production-planning.md) and [Manufacturing](production-manage-manufacturing.md).</span></span>  

 <span data-ttu-id="58885-113">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="58885-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="58885-114">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="58885-114">**To**</span></span>|<span data-ttu-id="58885-115">**Se**</span><span class="sxs-lookup"><span data-stu-id="58885-115">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="58885-116">Konfigurere produktionsfunktioner som f.eks. angivelse af produktionsarbejdstimer og valg af planlægningsprincipper.</span><span class="sxs-lookup"><span data-stu-id="58885-116">Configure the manufacturing features, such as defining shop floor work hours and selecting planning principles.</span></span>|<span data-ttu-id="58885-117">Siden **Produktionsopsætning**.</span><span class="sxs-lookup"><span data-stu-id="58885-117">The **Manufacturing Setup** page.</span></span>|  
|<span data-ttu-id="58885-118">Definer en standardarbejdsuge i produktionen med hensyn til start- og sluttidspunkter for hver enkelt arbejdsdag og relaterede arbejdsskift.</span><span class="sxs-lookup"><span data-stu-id="58885-118">Define a standard working week in the manufacturing department in terms of starting and ending times of each work day and related work shift.</span></span>|[<span data-ttu-id="58885-119">Opsætte produktionskalendere</span><span class="sxs-lookup"><span data-stu-id="58885-119">Create Shop Calendars</span></span>](production-how-to-create-work-center-calendars.md)|  
|<span data-ttu-id="58885-120">Organiser faste værdier og behov for produktionsressourcer som arbejdscentre eller produktionsressourcer for at styre outputtet af den udførte produktion.</span><span class="sxs-lookup"><span data-stu-id="58885-120">Organize fixed values and requirements of production resources as work centers or machine centers to govern their output of production performed.</span></span>|[<span data-ttu-id="58885-121">Konfigurere arbejdscentre og produktionsressourcer</span><span class="sxs-lookup"><span data-stu-id="58885-121">Set Up Work Centers and Machine Centers</span></span>](production-how-to-set-up-work-and-machine-centers.md)|
|<span data-ttu-id="58885-122">Organiser produktionsoperationer i den rækkefølge, der kræves, og tildel dem til arbejdscentre eller produktionsressourcer med de nødvendige arbejdstider.</span><span class="sxs-lookup"><span data-stu-id="58885-122">Organize production operations in the required order and assign them to work or machine centers with the required work times.</span></span>|[<span data-ttu-id="58885-123">Oprette ruter</span><span class="sxs-lookup"><span data-stu-id="58885-123">Create Routings</span></span>](production-how-to-create-routings.md)|
|<span data-ttu-id="58885-124">Organiser produktionskomponenter eller underordnede samlinger under en overordnet vare, og godkend styklisten til afvikling i arbejdscentre.</span><span class="sxs-lookup"><span data-stu-id="58885-124">Organize production components or subassemblies under a produced parent item and certify the BOM for execution at work centers.</span></span>|[<span data-ttu-id="58885-125">Oprette produktionsstyklister</span><span class="sxs-lookup"><span data-stu-id="58885-125">Create Production BOMs</span></span>](production-how-to-create-production-boms.md)|
|<span data-ttu-id="58885-126">Sørg for, at det rette komponentantal er tilgængeligt, når produktionsvarer lagerføres i én måleenhed, men produceres i en anden.</span><span class="sxs-lookup"><span data-stu-id="58885-126">Make sure that the right component quantity is available when produced items are stocked in one unit of measure but produced in another.</span></span>|[<span data-ttu-id="58885-127">Arbejde med produktionskladdeenheder</span><span class="sxs-lookup"><span data-stu-id="58885-127">Work With Manufacturing Batch Units of Measure</span></span>](production-how-to-use-the-manufacturing-batch-unit-of-measure.md)|  
|<span data-ttu-id="58885-128">Definer familier af produktionselementer med lignende produktionsprocesser for at spare på forbruget.</span><span class="sxs-lookup"><span data-stu-id="58885-128">Define families of production items with similar manufacturing processes to save consumption.</span></span> <span data-ttu-id="58885-129">F.eks. kan fire stk. af den samme vare produceres fra én plade samtidig med ti stk. af en anden vare.</span><span class="sxs-lookup"><span data-stu-id="58885-129">For example, four pieces of the same item can be produced from one sheet and 10 pieces of another, different, item at the same time.</span></span>|[<span data-ttu-id="58885-130">Arbejde med produktionsfamilier</span><span class="sxs-lookup"><span data-stu-id="58885-130">Work With Production Families</span></span>](production-how-work-family.md)|
|<span data-ttu-id="58885-131">Brug standardoperationer til at forenkle oprettelsen af ruter ved hurtigt at knytte ekstra oplysninger til gentagne operationer.</span><span class="sxs-lookup"><span data-stu-id="58885-131">Use standard tasks to simplify the creation of routings by quickly attaching extra information to recurring operations.</span></span>|[<span data-ttu-id="58885-132">Konfigurere standardrutelinjer</span><span class="sxs-lookup"><span data-stu-id="58885-132">Set Up Standard Routing Lines</span></span>](production-how-set-up-standard-routing-lines.md)|  
|<span data-ttu-id="58885-133">Forbered arbejdscentre og ruter til at repræsentere underleverandørens produktionsoperationer.</span><span class="sxs-lookup"><span data-stu-id="58885-133">Prepare work centers and routings to represent subcontracted production operations.</span></span>|[<span data-ttu-id="58885-134">Produktion hos underleverandør</span><span class="sxs-lookup"><span data-stu-id="58885-134">Subcontract Manufacturing</span></span>](production-how-to-subcontract-manufacturing.md)|  

## <a name="see-also"></a><span data-ttu-id="58885-135">Se også</span><span class="sxs-lookup"><span data-stu-id="58885-135">See Also</span></span>
<span data-ttu-id="58885-136">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="58885-136">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
<span data-ttu-id="58885-137">[Planlægning](production-planning.md) </span><span class="sxs-lookup"><span data-stu-id="58885-137">[Planning](production-planning.md) </span></span>  
[<span data-ttu-id="58885-138">Lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="58885-138">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="58885-139">Køb</span><span class="sxs-lookup"><span data-stu-id="58885-139">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="58885-140">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="58885-140">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
