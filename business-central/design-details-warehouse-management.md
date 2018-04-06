---
title: "Designoplysninger – Logistik | Microsoft Docs"
description: Dette emne giver et overblik over designet, begreberne og principperne bag logistikfunktionerne i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/23/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a55be802506d9d8cbaae1cea9801a85c61e7374f
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-warehouse-management"></a><span data-ttu-id="ecbc2-103">Designoplysninger: Logistik</span><span class="sxs-lookup"><span data-stu-id="ecbc2-103">Design Details: Warehouse Management</span></span>
<span data-ttu-id="ecbc2-104">Denne dokumentation giver et overblik over de begreber og principper, der bruges i logistikfunktionerne i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ecbc2-104">This documentation gives an overview of the concepts and principles that are used in the Warehouse Management features in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="ecbc2-105">Det forklarer designet bag centrallagerfunktioner, og hvordan logistik integreres med andre funktioner i forsyningskæden.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-105">It explains the design behind central warehouse features and how warehousing integrates with other supply chain features.</span></span>  

<span data-ttu-id="ecbc2-106">Med henblik på at skelne mellem forskellige kompleksitetsniveauer af logistik er dette dokument opdelt i to generelle grupper, grundlæggende og avancerede lageropsætninger, angivet ved titlerne på afsnittene.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-106">To differentiate the different complexity levels of the warehousing, this documentation is divided into two general groups, Basic and Advanced warehouse configurations, indicated by section titles.</span></span> <span data-ttu-id="ecbc2-107">Denne simple differentiering dækker forskellige kompleksitetsniveauer, som defineret af produktdetaljer og lokationsopsætning.</span><span class="sxs-lookup"><span data-stu-id="ecbc2-107">This simple differentiation covers different complexity levels as defined by product granules and location setup.</span></span> <span data-ttu-id="ecbc2-108">Du kan finde flere oplysninger i [Designoplysninger: Opsætning af lager](design-details-warehouse-setup.md)</span><span class="sxs-lookup"><span data-stu-id="ecbc2-108">For more information, see [Design Details: Warehouse Setup](design-details-warehouse-setup.md).</span></span>  

## <a name="in-this-section"></a><span data-ttu-id="ecbc2-109">Dette afsnit indeholder</span><span class="sxs-lookup"><span data-stu-id="ecbc2-109">In This Section</span></span>  
[<span data-ttu-id="ecbc2-110">Designoplysninger: Oversigt over logistik</span><span class="sxs-lookup"><span data-stu-id="ecbc2-110">Design Details: Warehouse Overview</span></span>](design-details-warehouse-overview.md)  
[<span data-ttu-id="ecbc2-111">Designoplysninger: Opsætning af lager</span><span class="sxs-lookup"><span data-stu-id="ecbc2-111">Design Details: Warehouse Setup</span></span>](design-details-warehouse-setup.md)  
[<span data-ttu-id="ecbc2-112">Designoplysninger: Indgående lagerflow</span><span class="sxs-lookup"><span data-stu-id="ecbc2-112">Design Details: Inbound Warehouse Flow</span></span>](design-details-inbound-warehouse-flow.md)  
[<span data-ttu-id="ecbc2-113">Designoplysninger: Internt lagerflow</span><span class="sxs-lookup"><span data-stu-id="ecbc2-113">Design Details: Internal Warehouse Flows</span></span>](design-details-internal-warehouse-flows.md)  
[<span data-ttu-id="ecbc2-114">Designoplysninger: Tilgængelighed i lageret</span><span class="sxs-lookup"><span data-stu-id="ecbc2-114">Design Details: Availability in the Warehouse</span></span>](design-details-availability-in-the-warehouse.md)  
[<span data-ttu-id="ecbc2-115">Designoplysninger: Udgående lagerflow</span><span class="sxs-lookup"><span data-stu-id="ecbc2-115">Design Details: Outbound Warehouse Flow</span></span>](design-details-outbound-warehouse-flow.md)  
[<span data-ttu-id="ecbc2-116">Designoplysninger: Integration med lager</span><span class="sxs-lookup"><span data-stu-id="ecbc2-116">Design Details: Integration with Inventory</span></span>](design-details-integration-with-inventory.md)
