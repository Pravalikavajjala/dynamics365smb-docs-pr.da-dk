---
title: Definere koder for standardservices | Microsoft Docs
description: "Få at vide, hvordan du definerer koder for serviceaktiviteter, du udfører ofte."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, service item, service order, repairs, maintenance
ms.date: 08/22/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: bca816da5473ea3f5f8eab892125e32a045ffec3
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---

# <a name="set-up-standard-service-codes"></a><span data-ttu-id="05177-103">Konfigurere standardservicekoder</span><span class="sxs-lookup"><span data-stu-id="05177-103">Set Up Standard Service Codes</span></span>
<span data-ttu-id="05177-104">Når der foretages standardservice, skal der ofte oprettes servicedokumenter, der bruger servicelinjer, der indeholder ensartede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="05177-104">When you perform typical service, you often have to create service documents that use service lines that contain similar information.</span></span> <span data-ttu-id="05177-105">For at gøre det nemmere at oprette disse linjer kan du oprette standardservicekoder, der har et foruddefineret sæt af servicelinjer.</span><span class="sxs-lookup"><span data-stu-id="05177-105">To make it easy to create these lines, you can set up standard service codes that have a predefined set of service lines.</span></span> <span data-ttu-id="05177-106">Når du vælger koden i et servicedokument, indsættes linjerne automatisk.</span><span class="sxs-lookup"><span data-stu-id="05177-106">When you choose the code on a service document, the lines are entered automatically.</span></span> <span data-ttu-id="05177-107">Du kan oprette et hvilket som helst antal standardservicekoder, og hver kode kan have et ubegrænset antal servicelinjer af forskellige typer, herunder vare, ressource, pris eller tekst, tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="05177-107">You can set up any number of standard service codes, and each code can have an unlimited number of service lines of different types, including item, resource, cost, or standrd text linked to it.</span></span> <span data-ttu-id="05177-108">Du opretter servicelinjer for hver standardservicekode på kortet **Standardservicekode**.</span><span class="sxs-lookup"><span data-stu-id="05177-108">You create service lines of each standard serice code on the **Standard Service Code** card.</span></span> <span data-ttu-id="05177-109">Derefter tildeler du standardservicekoder til serviceartikelgrupper på siden **Koder til standardserv.varegrupper**.</span><span class="sxs-lookup"><span data-stu-id="05177-109">You then assign standard service codes to service item groups on the **Standard Serv. Item Gr. Codes** page.</span></span> <span data-ttu-id="05177-110">Senere, når du opretter et servicedokument, du kan bruge handlingen **Hent standardservicekoder** til at tilføje servicelinjer.</span><span class="sxs-lookup"><span data-stu-id="05177-110">Later, when you create a service document, you can use the **Get Standard Service Codes** action to add service lines.</span></span>  
  
> [!Tip]
>  <span data-ttu-id="05177-111">Du kan bruge den samme fremgangsmåde til at oprette linjer på salgs- og købsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="05177-111">You can use the same concept to create lines on sales and purchase documents.</span></span> <span data-ttu-id="05177-112">Du kan finde flere oplysninger i [Oprette gentagne salgs- og købslinjer](sales-how-work-standard-lines.md).</span><span class="sxs-lookup"><span data-stu-id="05177-112">For more information, see [Create Recurring Sales and Purchase Lines](sales-how-work-standard-lines.md).</span></span>    
  
## <a name="to-set-up-a-standard-service-code"></a><span data-ttu-id="05177-113">Sådan oprettes standardservicekoder</span><span class="sxs-lookup"><span data-stu-id="05177-113">To set up a standard service code</span></span>    
1. <span data-ttu-id="05177-114">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Standardservicekoder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="05177-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Standard Service Codes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="05177-115">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="05177-115">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="05177-116">Udfyld de servicelinjer, der er knyttet til denne servicekode.</span><span class="sxs-lookup"><span data-stu-id="05177-116">Fill in the service lines linked to this service code.</span></span>  

## <a name="to-assign-a-standard-service-code-to-a-service-item-group"></a><span data-ttu-id="05177-117">Tildele en standardservicekode til en serviceartikelgruppe</span><span class="sxs-lookup"><span data-stu-id="05177-117">To assign a standard service code to a service item group</span></span>
1. <span data-ttu-id="05177-118">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Serviceartikelgrupper**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="05177-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service item Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="05177-119">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="05177-119">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="05177-120">Udfyld de servicelinjer, der er knyttet til denne servicekode.</span><span class="sxs-lookup"><span data-stu-id="05177-120">Fill in the service lines linked to this service code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="05177-121">Se også</span><span class="sxs-lookup"><span data-stu-id="05177-121">See Also</span></span>
[<span data-ttu-id="05177-122">Service</span><span class="sxs-lookup"><span data-stu-id="05177-122">Service Management</span></span>](service-service.md)