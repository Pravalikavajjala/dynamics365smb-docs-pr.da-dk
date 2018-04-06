---
title: "Designoplysninger – Design af varesporing | Microsoft Docs"
description: I dette emne beskrives designet bag varesporing i Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: design, item, tracking, tracing
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4d2b4d9e55851564b003ed9c85178237f8689122
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-item-tracking-design"></a><span data-ttu-id="93800-103">Designoplysninger: Design af varesporing</span><span class="sxs-lookup"><span data-stu-id="93800-103">Design Details: Item Tracking Design</span></span>
<span data-ttu-id="93800-104">I den første version af Varesporing i [!INCLUDE[d365fin](includes/d365fin_md.md)] 2.60 er serie- eller lotnumre registreret direkte i vareposter.</span><span class="sxs-lookup"><span data-stu-id="93800-104">In the first version of Item Tracking in [!INCLUDE[d365fin](includes/d365fin_md.md)] 2.60, serial numbers or lot numbers were recorded directly on item ledger entries.</span></span> <span data-ttu-id="93800-105">Dette design leverede komplette tilgængelighedsoplysninger og simpel sporing af historiske poster, men det manglede fleksibilitet og funktionalitet.</span><span class="sxs-lookup"><span data-stu-id="93800-105">This design provided full availability information and simple tracking of historic entries, but it lacked flexibility and functionality.</span></span>  

<span data-ttu-id="93800-106">Fra [!INCLUDE[d365fin](includes/d365fin_md.md)] 3.00 fandtes varesporingsfunktionen i en separat objektstruktur med komplicerede links til bogførte dokumenter og vareposter.</span><span class="sxs-lookup"><span data-stu-id="93800-106">From [!INCLUDE[d365fin](includes/d365fin_md.md)] 3.00, item tracking functionality was in a separate object structure with intricate links to posted documents and item ledger entries.</span></span> <span data-ttu-id="93800-107">Dette design var fleksibelt og omfattende i funktionalitet, men varesporingsposter var ikke fuldt inddraget i disponeringsberegningerne.</span><span class="sxs-lookup"><span data-stu-id="93800-107">This design was flexible and rich in functionality, but item tracking entries were not fully involved in availability calculations.</span></span>  

<span data-ttu-id="93800-108">Siden [!INCLUDE[d365fin](includes/d365fin_md.md)] 3.60 er varesporingsfunktionen integreret med reservationssystemet, som håndterer reservation, ordresporing og aktionsmeddelelser.</span><span class="sxs-lookup"><span data-stu-id="93800-108">Since [!INCLUDE[d365fin](includes/d365fin_md.md)] 3.60, item tracking functionality is integrated with the reservation system, which handles reservation, order tracking, and action messaging.</span></span> <span data-ttu-id="93800-109">Hvis du ønsker yderligere oplysninger, kan du se "Designoplysninger: Reservation, ordresporing og aktionsmeddelelser" i "Designoplysninger: Forsyningsplanlægning".</span><span class="sxs-lookup"><span data-stu-id="93800-109">For more information, see “Design Details: Reservation, Order Tracking, and Action Messaging” in “Design Details: Supply Planning”.</span></span>  

<span data-ttu-id="93800-110">Dette seneste design omfatter varesporingsposter i samlede disponeringsberegninger i hele systemet, herunder planlægning, produktion og logistik.</span><span class="sxs-lookup"><span data-stu-id="93800-110">This latest design incorporates item tracking entries in total availability calculations throughout the system, including planning, manufacturing, and warehousing.</span></span> <span data-ttu-id="93800-111">Det gamle ide med at overføre serie- og lotnumre på vareposterne introduceres igen for at sikre nem adgang til historiske data af varesporingsformål.</span><span class="sxs-lookup"><span data-stu-id="93800-111">The old concept of carrying serial and lot numbers on the item ledger entries is reintroduced to ensure simple access to historical data for item tracking purposes.</span></span> <span data-ttu-id="93800-112">I forbindelse med varesporingsforbedringer i [!INCLUDE[d365fin](includes/d365fin_md.md)] 3.60 blev reservationssystemet udvidet til ikke-ordrenetværksenheder som kladder, fakturaer og kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="93800-112">In connection with item tracking improvements in [!INCLUDE[d365fin](includes/d365fin_md.md)] 3.60, the reservation system was expanded to non-order network entities, such as journals, invoices, and credit memos.</span></span>  

<span data-ttu-id="93800-113">Med tilføjelsen af serie- eller lotnumre håndterer reservationssystemet permanente vareattributter, mens der også håndteres periodiske links mellem forsyning og behov i form af ordresporings- og reservationsposter.</span><span class="sxs-lookup"><span data-stu-id="93800-113">With the addition of serial or lot numbers, the reservation system handles permanent item attributes while also handling intermittent links between supply and demand in the form of order tracking entries and reservation entries.</span></span> <span data-ttu-id="93800-114">Et andet træk ved serienumre eller lotnumre sammenlignet med konventionelle reservationsdata er det faktum, at de kan bogføres enten helt eller delvist.</span><span class="sxs-lookup"><span data-stu-id="93800-114">Another different characteristic of serial or lot numbers compared to the conventional reservation data is the fact that they can be posted, either partially or fully.</span></span> <span data-ttu-id="93800-115">Derfor fungerer tabellen **Reservationspost** (T337) nu med en relateret tabel, tabellen **Sporingsspecifikation** (T336), som administrerer og viser en opsummering på tværs af aktive og bogførte varesporingsantal.</span><span class="sxs-lookup"><span data-stu-id="93800-115">Therefore, the **Reservation Entry** table (T337) now works with a related table, the **Tracking Specification** table (T336), which manages and displays summing across active and posted item tracking quantities.</span></span> <span data-ttu-id="93800-116">Du kan finde flere oplysninger i [Designoplysninger: Aktive kontra historiske varesporingsposter](design-details-active-versus-historic-item-tracking-entries.md).</span><span class="sxs-lookup"><span data-stu-id="93800-116">For more information, see [Design Details: Active versus Historic Item Tracking Entries](design-details-active-versus-historic-item-tracking-entries.md).</span></span>  

<span data-ttu-id="93800-117">I følgende diagram beskrives udformningen af varesporingsfunktionen i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="93800-117">The following diagram outlines the design of item tracking functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="93800-118">![Varesporingsdesign](media/design_details_item_tracking_design.png "design_details_item_tracking_design")</span><span class="sxs-lookup"><span data-stu-id="93800-118">![Item tracking design](media/design_details_item_tracking_design.png "design_details_item_tracking_design")</span></span>  

<span data-ttu-id="93800-119">Objektet til central bogføring er ændret for at håndtere entydig underklassifikation af en bilagslinje i form af serie- eller lotnumre, og særlige relationstabeller er tilføjet for at oprette en-til-mange-relationer mellem bogførte dokumenter og deres opdelte vareposter og værdiposter.</span><span class="sxs-lookup"><span data-stu-id="93800-119">The central posting object is redesigned to handle the unique subclassification of a document line in the form of serial or lot numbers, and special relation tables are added to create the one-to-many relations between posted documents and their split item ledger entries and value ledger entries.</span></span>  

<span data-ttu-id="93800-120">Kodeenhed 22 **Varekladde – Bogfør linje** opdeler nu bogføringen i overensstemmelse med de varesporingsnumre, der er angivet på dokumentlinjen.</span><span class="sxs-lookup"><span data-stu-id="93800-120">Codeunit 22, **Item Jnl. – Post Line**, now splits the posting according to the item tracking numbers that are specified on the document line.</span></span> <span data-ttu-id="93800-121">Hvert entydigt varesporingsnummer på linjen opretter dets egen varepost for varen.</span><span class="sxs-lookup"><span data-stu-id="93800-121">Each unique item tracking number on the line creates its own item ledger entry for the item.</span></span> <span data-ttu-id="93800-122">Det betyder, at tilknytningen fra den bogførte dokumentlinje til de tilknyttede vareposter nu er en en-til-mange-relation.</span><span class="sxs-lookup"><span data-stu-id="93800-122">This means that the link from the posted document line to the associated item ledger entries is now a one-to-many relation.</span></span> <span data-ttu-id="93800-123">Denne relation håndteres af de følgende ordresporingsrelationstabeller.</span><span class="sxs-lookup"><span data-stu-id="93800-123">This relation is handled by the following item tracking relation tables.</span></span>  

|<span data-ttu-id="93800-124">Felt</span><span class="sxs-lookup"><span data-stu-id="93800-124">Field</span></span>|<span data-ttu-id="93800-125">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="93800-125">Description</span></span>|  
|---------------|---------------------------------------|  
|<span data-ttu-id="93800-126">**Varepostrelation** (T6507)</span><span class="sxs-lookup"><span data-stu-id="93800-126">**Item Entry Relation** (T6507)</span></span>|<span data-ttu-id="93800-127">Relaterer afsendte eller modtagne linjer til vareposter</span><span class="sxs-lookup"><span data-stu-id="93800-127">Relates shipped or received lines to item ledger entries</span></span>|  
|<span data-ttu-id="93800-128">**Værdipostrelation** (T6508)</span><span class="sxs-lookup"><span data-stu-id="93800-128">**Value Entry Relation** (T6508)</span></span>|<span data-ttu-id="93800-129">Relaterer fakturerede linjer til værdiposter</span><span class="sxs-lookup"><span data-stu-id="93800-129">Relates invoiced lines to value entries</span></span>|  

<span data-ttu-id="93800-130">Du kan finde flere oplysninger i [Designoplysninger: Bogføringsstruktur for varesporing](design-details-item-tracking-posting-structure.md).</span><span class="sxs-lookup"><span data-stu-id="93800-130">For more information, see [Design Details: Item Tracking Posting Structure](design-details-item-tracking-posting-structure.md).</span></span>  

## <a name="see-also"></a><span data-ttu-id="93800-131">Se også</span><span class="sxs-lookup"><span data-stu-id="93800-131">See Also</span></span>  
[<span data-ttu-id="93800-132">Designoplysninger: Varesporing</span><span class="sxs-lookup"><span data-stu-id="93800-132">Design Details: Item Tracking</span></span>](design-details-item-tracking.md)
