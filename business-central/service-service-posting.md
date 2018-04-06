---
title: "Servicebogføring | Microsoft Docs"
description: "Servicebogføringsfunktionen gør det muligt at behandle dokumenter effektivt og hele tiden bevare en gennemført kundeservicepolitik. Du kan oprette og opdatere bogførte dokumenter og oprette poster både inden for serviceområdet og i andre moduler for at sikre korrekt opdatering."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b191b5e8fbe0a60a32d32bd2dc1ca0cca07c06e4
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="service-posting"></a><span data-ttu-id="d3707-104">Bogføring af tjenesten</span><span class="sxs-lookup"><span data-stu-id="d3707-104">Service Posting</span></span>
<span data-ttu-id="d3707-105">Servicebogføringsfunktionen gør det muligt at behandle dokumenter effektivt og hele tiden bevare en gennemført kundeservicepolitik.</span><span class="sxs-lookup"><span data-stu-id="d3707-105">Service posting functionality lets you process your documents efficiently and maintain successful customer service policy.</span></span> <span data-ttu-id="d3707-106">Du kan oprette og opdatere bogførte dokumenter og oprette poster både inden for serviceområdet og i andre moduler for at sikre korrekt opdatering.</span><span class="sxs-lookup"><span data-stu-id="d3707-106">You can create and update posted documents, and create ledger entries both in the service area and in other modules to ensure the correct update.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="d3707-107">Nedenfor beskrives servicepostering, uanset hvordan varerne fysisk håndteres på lageret.</span><span class="sxs-lookup"><span data-stu-id="d3707-107">The following describes service posting regardless of how items are physically handled in the warehouse.</span></span>  
>   
>  <span data-ttu-id="d3707-108">På en placering, der ikke er konfigureret til at kræve lagerekspedition, skal du udføre bogføringsprocesserne direkte fra vinduet **Servicelinjer**.</span><span class="sxs-lookup"><span data-stu-id="d3707-108">In a location that is not set up to require warehouse handling, you perform the posting actions directly from the **Service Lines** window.</span></span> <span data-ttu-id="d3707-109">På lokationer, der involverer lagerekspedition, udføres de beskrevne bogføringsprocesser, undtagen Send og forbrug, indirekte via forskellige lagerleverancefunktioner afhængigt af konfuguration.</span><span class="sxs-lookup"><span data-stu-id="d3707-109">In locations that involve warehouse handling, the described posting actions, except Ship and Consume, are performed indirectly through varying warehouse ship functions, depending on setup.</span></span> <span data-ttu-id="d3707-110">Du kan finde flere oplysninger i [Plukke varer med Pluk fra lager](warehouse-how-to-pick-items-with-inventory-picks.md).</span><span class="sxs-lookup"><span data-stu-id="d3707-110">For more information, see [Pick Items with Inventory Picks](warehouse-how-to-pick-items-with-inventory-picks.md).</span></span>  

## <a name="ship"></a><span data-ttu-id="d3707-111">Lever</span><span class="sxs-lookup"><span data-stu-id="d3707-111">Ship</span></span>  
<span data-ttu-id="d3707-112">Med leveringsindstillingen kan du registrere relevante varer og den tid, der er angivet på linjerne i en serviceordre, når du har afsluttet servicen.</span><span class="sxs-lookup"><span data-stu-id="d3707-112">The ship option lets you register the relevant items and time entered on the lines of a service order after you complete the service.</span></span> <span data-ttu-id="d3707-113">Der oprettes en bogført leverance, og modulet Lagerbeholdning og andre moduler i [!INCLUDE[d365fin](includes/d365fin_md.md)] opdateres, så det afspejles, at varerne er taget ud af lageret og sendt til kunden.</span><span class="sxs-lookup"><span data-stu-id="d3707-113">A posted shipment is created and updates occur in the Inventory module and other modules in [!INCLUDE[d365fin](includes/d365fin_md.md)] to reflect that the items have been taken out of the inventory and sent to the customer.</span></span> <span data-ttu-id="d3707-114">Der oprettes specielt vareposter, værdiposter, serviceposter og garantiposter.</span><span class="sxs-lookup"><span data-stu-id="d3707-114">In particular, the item ledger entries, value ledger entries, service ledger entries, and warranty ledger entries are produced.</span></span>  

<span data-ttu-id="d3707-115">Hvis lokationen er angivet til at kræve lagerekspedition, sker forsendelse og flytning af servicelinjevarefunktioner på samme måde som for andre kildedokumenter.</span><span class="sxs-lookup"><span data-stu-id="d3707-115">If the location is set up to require warehouse handling, then the shipping and moving of service line items functions in the same ways as for other source documents.</span></span> <span data-ttu-id="d3707-116">Den eneste forskel er, at servicelinjevarer kan forbruges eksternt eller internt, hvilket kræver de to forskellige frigivelsesfunktioner.</span><span class="sxs-lookup"><span data-stu-id="d3707-116">The only difference is that service line items can be consumed either externally or internally, which requires two different release functions.</span></span>

## <a name="invoice"></a><span data-ttu-id="d3707-117">Faktura</span><span class="sxs-lookup"><span data-stu-id="d3707-117">Invoice</span></span>  
<span data-ttu-id="d3707-118">Du skal bruge faktureringsindstillingen til at udstede en faktura til den kunde, der skal betale for servicen.</span><span class="sxs-lookup"><span data-stu-id="d3707-118">You have to use the invoice option to issue an invoice to the customer you want to charge for the service.</span></span> <span data-ttu-id="d3707-119">Det er som regel forskellen mellem det leverede antal, der er registreret vha. funktionen **Bogfør lev.**, og det forbrugte antal, der er registreret vha. funktionen til **bogføring af forbrug**, som er forbundet med faktureringen.</span><span class="sxs-lookup"><span data-stu-id="d3707-119">Usually, it is the difference between the shipped quantity registered by the **Post Shipment** function and the consumed quantity registered by the **Post Consumption** function that is subject to invoice.</span></span> <span data-ttu-id="d3707-120">Du kan ikke fakturere noget, der ikke er leveret.</span><span class="sxs-lookup"><span data-stu-id="d3707-120">You cannot invoice what has not been shipped.</span></span> <span data-ttu-id="d3707-121">Når du kører funktionen **Bogfør fakturaer**, opretter du en bogført servicefaktura og opdaterer de dokumenter, der er bogført før, så de er i overensstemmelse med det antal, der er angivet i den udstedte faktura.</span><span class="sxs-lookup"><span data-stu-id="d3707-121">When you run the **Post Invoice** function, you create a posted service invoice and update the documents posted before to make them consistent with the quantities that are contained in the issued invoice.</span></span> <span data-ttu-id="d3707-122">Som det er tilfældet med andre bogføringsprocedurer, oprettes de relevante poster, inklusive finansposter.</span><span class="sxs-lookup"><span data-stu-id="d3707-122">Like in other posting procedures, the relevant ledger entries that includes general ledger entries, are generated.</span></span>  

## <a name="ship-and-invoice"></a><span data-ttu-id="d3707-123">Lever og fakturer</span><span class="sxs-lookup"><span data-stu-id="d3707-123">Ship and Invoice</span></span>  
<span data-ttu-id="d3707-124">Med indstillingen Send og fakturer kan du udstede en serviceleverance og en faktura på samme tid.</span><span class="sxs-lookup"><span data-stu-id="d3707-124">The ship and invoice option lets you issue both a service shipment and an invoice at the same time.</span></span>  

## <a name="ship-and-consume"></a><span data-ttu-id="d3707-125">Send og forbrug</span><span class="sxs-lookup"><span data-stu-id="d3707-125">Ship and Consume</span></span>  
<span data-ttu-id="d3707-126">Med indstillingen Send og forbrug, kan du registrere og bogføre varer, omkostninger eller timer, der er anvendt til servicen, men som ikke kan medtages på fakturaen til kunden.</span><span class="sxs-lookup"><span data-stu-id="d3707-126">With the ship and consume option, you can register and post items, costs, or hours that have been used for servicing but that cannot be included in the invoice to the customer.</span></span> <span data-ttu-id="d3707-127">Der udstedes ikke en faktura i programmet, men du har mulighed for at udstede både serviceleverance og serviceforbrug samtidig for at afspejle den kendsgerning, at kunden får nogle varer eller timer gratis.</span><span class="sxs-lookup"><span data-stu-id="d3707-127">An invoice is not issued, but you can issue both a service shipment and service consumption at the same time to reflect the fact that some items or hours have been given to the customer free of charge.</span></span> <span data-ttu-id="d3707-128">De tilsvarende poster oprettes også, så forbruget registreres.</span><span class="sxs-lookup"><span data-stu-id="d3707-128">The corresponding ledger entries are also created to register consumption.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="d3707-129">Proceduren til servicepostering sætter dig i stand til at foretage delvis bogføring.</span><span class="sxs-lookup"><span data-stu-id="d3707-129">The service posting procedure enables you to perform partial posting.</span></span> <span data-ttu-id="d3707-130">Du kan oprette en delleverance eller en delfaktura ved at udfylde felterne **Lever (antal)** og **Fakturer (antal)** på de enkelte servicelinjer i serviceordrerne, før du bogfører.</span><span class="sxs-lookup"><span data-stu-id="d3707-130">You can create a partial shipment or a partial invoice by filling in the **Qty. to Ship** and **Qty. to Invoice** fields on the individual service lines of the service orders before you post.</span></span> <span data-ttu-id="d3707-131">Bemærk, at du ikke kan oprette en faktura for noget, der ikke er leveret.</span><span class="sxs-lookup"><span data-stu-id="d3707-131">Note that you cannot create an invoice for something that is not shipped.</span></span> <span data-ttu-id="d3707-132">Dvs., før du kan fakturere, skal der være registreret en leverance, eller du skal vælge at sende og fakturere på samme tid.</span><span class="sxs-lookup"><span data-stu-id="d3707-132">That is, before you can invoice, you must have registered a shipment, or you must choose to ship and invoice at the same time.</span></span>  

<span data-ttu-id="d3707-133">Når bogføringen er færdig, kan du se de bogførte servicedokumenter i de tilsvarende vinduer **Bogført serviceleverance** og **Bogført servicefaktura**.</span><span class="sxs-lookup"><span data-stu-id="d3707-133">After the posting has been completed, you will be able to view the posted service documents from the corresponding **Posted Service Shipment** and **Posted Service Invoice** windows.</span></span> <span data-ttu-id="d3707-134">De bogførte poster, der er oprettet, kan ses i de forskellige vinduer med bogførte poster **Finansposter**, **Vareposter**, **Lagerposter**, **Serviceposter**, **Sagsposter** og **Garantiposter**.</span><span class="sxs-lookup"><span data-stu-id="d3707-134">The posted entries created can be seen in various windows that contain posted entries, such as **G/L Entries**, **Item Ledger Entries**, **Warehouse Entries**, **Service Ledger Entries**, **Job Ledger Entries**, and **Warranty Ledger Entries**.</span></span>  

## <a name="to-view-information-about-a-posted-service-document"></a><span data-ttu-id="d3707-135">Sådan får du vist oplysninger om et bogført servicedokument</span><span class="sxs-lookup"><span data-stu-id="d3707-135">To view information about a posted service document</span></span>  
<span data-ttu-id="d3707-136">Når du bogfører en servicefaktura, en serviceleverance eller en servicekreditnota, overføres oplysningerne i dokumentet til et af vinduerne **Bogført servicefaktura**, **Bogført serviceleverance** eller **Bogført servicekreditnota**.</span><span class="sxs-lookup"><span data-stu-id="d3707-136">When you post a service invoice, a service shipment, or a service credit memo, the information on the document is transferred to the **Posted Service Invoice**, **Posted Service Shipment**, or **Posted Service Credit Memo** windows respectively.</span></span> <span data-ttu-id="d3707-137">Du kan ikke skrive, ændre eller slette noget i disse vinduer.</span><span class="sxs-lookup"><span data-stu-id="d3707-137">You cannot enter, change, or delete anything in these windows.</span></span> <span data-ttu-id="d3707-138">Du kan udskrive en leverance, faktura eller kreditnota fra disse vinduer.</span><span class="sxs-lookup"><span data-stu-id="d3707-138">You can print a shipment, invoice, or credit memo from these windows.</span></span>  

<span data-ttu-id="d3707-139">I følgende procedure bruges en bogført servicefaktura som eksempel, men der kan anvendes samme fremgangsmåde på bogførte serviceleverancer og bogførte kreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="d3707-139">The following procedure uses a posted service invoice as an example, but the same procedure can apply to posted service shipments and posted credit memos.</span></span>  

1. <span data-ttu-id="d3707-140">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bogført servicefaktura**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d3707-140">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Posted Service Invoice**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d3707-141">Åbn den bogførte servicefaktura, som du vil se.</span><span class="sxs-lookup"><span data-stu-id="d3707-141">Open the posted service invoice you want to view.</span></span>  
3. <span data-ttu-id="d3707-142">For at få et overblik over den bogførte faktura skal du vælge handlingen **Statistik**.</span><span class="sxs-lookup"><span data-stu-id="d3707-142">To get an overview of the posted invoice, choose the **Statistics** action.</span></span>  

    <span data-ttu-id="d3707-143">Vinduet **Serviceordrestatistik** åbnes.</span><span class="sxs-lookup"><span data-stu-id="d3707-143">The **Service Order Statistics** window opens.</span></span> <span data-ttu-id="d3707-144">I vinduet vises der oplysninger som antal, beløb, moms, omkostninger, avance og kundekreditmaksimum for det bogførte dokument.</span><span class="sxs-lookup"><span data-stu-id="d3707-144">The window displays information such as quantity, amount, VAT, cost, profit, and customer credit limit for the posted document.</span></span>

## <a name="see-also"></a><span data-ttu-id="d3707-145">Se også</span><span class="sxs-lookup"><span data-stu-id="d3707-145">See Also</span></span>  
<span data-ttu-id="d3707-146">[Postere serviceordrer](service-how-to-post-service-orders.md) </span><span class="sxs-lookup"><span data-stu-id="d3707-146">[Post Service Orders](service-how-to-post-service-orders.md) </span></span>  
[<span data-ttu-id="d3707-147">Oprette serviceordrer</span><span class="sxs-lookup"><span data-stu-id="d3707-147">Create Service Orders</span></span>](service-how-to-create-service-orders.md)
