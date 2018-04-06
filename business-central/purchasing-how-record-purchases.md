---
title: "Oprette en købsfaktura og registrere indkøb | Microsoft Docs"
description: "Beskriver, hvordan du køber lager- eller serviceartikler ved at oprette og bogføre købsfakturaer eller ordrer."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 4823bcb9468630a19b274708d4309331242392f8
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="record-purchases"></a><span data-ttu-id="d3c8b-103">Registrere køb</span><span class="sxs-lookup"><span data-stu-id="d3c8b-103">Record Purchases</span></span>
<span data-ttu-id="d3c8b-104">Du kan oprette en købsfaktura eller købsordre for at registrere omkostningerne ved køb og spore gæld.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-104">You create a purchase invoice or purchase order to record the cost of purchases and to track accounts payable.</span></span> <span data-ttu-id="d3c8b-105">Hvis du vil styre en lagerbeholdning, benyttes købsfakturaer og købsordrer også til at opdatere lagerniveauer dynamisk, så du kan minimere lageromkostningerne og yde bedre kundeservice.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-105">If you need to control an inventory, purchase invoices and purchase orders are also used to dynamically update inventory levels so that you can minimize your inventory costs and provide better customer service.</span></span> <span data-ttu-id="d3c8b-106">Købsomkostningerne, herunder serviceudgifter og lagerværdier, der stammer fra bogføring af købsfakturaer eller ordrer, bidrager til avancebeløb og andre finansielle nøgletal i dit Rollecenter.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-106">The purchasing costs, including service expenses, and inventory values that result from posting purchase invoices or orders contribute to profit figures and other financial KPIs on your Role Center.</span></span>

> [!NOTE]  
>   <span data-ttu-id="d3c8b-107">Du skal bruge købsordrer, hvis din købsproces kræver, at du kan registrere delleveringer af et ordreantal, f.eks. fordi hele antallet ikke er tilgængeligt hos leverandøren.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-107">You must use purchase orders if your purchasing process requires that you record partial receipts of an order quantity, for example, because the full quantity was not available at the vendor.</span></span> <span data-ttu-id="d3c8b-108">Hvis du sælger varer ved at levere direkte fra leverandøren til kunden som en direkte levering, skal du også bruge købsordrer.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-108">If you sell items by delivering directly from your vendor to your customer, as a drop shipment, then you must also use purchase orders.</span></span> <span data-ttu-id="d3c8b-109">Du kan finde flere oplysninger i [Foretage direkte leveringer](sales-how-drop-shipment.md).</span><span class="sxs-lookup"><span data-stu-id="d3c8b-109">For more information, see [Make Drop Shipments](sales-how-drop-shipment.md).</span></span> <span data-ttu-id="d3c8b-110">I alle andre henseender fungerer købsordrer på samme måde som købsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-110">In all other aspects, purchase orders work the same way as purchase invoices.</span></span> <span data-ttu-id="d3c8b-111">Følgende procedure er baseret på en købsfaktura.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-111">The following procedure is based on a purchase invoice.</span></span> <span data-ttu-id="d3c8b-112">Fremgangsmåden er den samme for en købsordre.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-112">The steps are similar for a purchase order.</span></span>

<span data-ttu-id="d3c8b-113">Når du modtager lagervarerne, eller når den købte service er fuldført, skal du bogføre købsfakturaen eller -ordren for at opdatere lager- og finansrecords og aktivere betaling til kreditor i henhold til betalingsbetingelserne.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-113">When you receive the inventory items, or when the purchased service is completed, you post the purchase invoice or order to update inventory and financial records and to activate payment to the vendor according to the payment terms.</span></span> <span data-ttu-id="d3c8b-114">Du kan finde flere oplysninger under [Foretage betalinger](payables-make-payments.md).</span><span class="sxs-lookup"><span data-stu-id="d3c8b-114">For more information, see [Making Payments](payables-make-payments.md).</span></span>

> [!CAUTION]  
>   <span data-ttu-id="d3c8b-115">Bogfør ikke en købsfaktura, før du modtager varerne og kender de endelige omkostninger for købet, herunder eventuelle yderligere udgifter.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-115">Do not post a purchase invoice until you receive the items and know the final cost of the purchase, including any additional charges.</span></span> <span data-ttu-id="d3c8b-116">Ellers kan din lagerværdi og avancetal blive skævt.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-116">Otherwise, your inventory value and profit figures may be skewed.</span></span>

<span data-ttu-id="d3c8b-117">Du kan nemt rette eller annullere en bogført købsfaktura, før du betaler kreditoren.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-117">You can easily correct or cancel a posted purchase invoice before you pay the vendor.</span></span> <span data-ttu-id="d3c8b-118">Dette er nyttigt, hvis du vil rette en skrivefejl, eller hvis du ønsker at ændre købet tidligt i ordreprocessen.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-118">This is useful if you want to correct a typing mistake or if you want to change the purchase early in the order process.</span></span> <span data-ttu-id="d3c8b-119">Du kan finde flere oplysninger under [Rette eller annullere ubetalte købsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="d3c8b-119">For more information, see [Correct or Cancel Unpaid Purchase Invoices](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).</span></span> <span data-ttu-id="d3c8b-120">Hvis du allerede har betalt for varer på den bogførte købsfaktura, skal du oprette en købskreditnota for at tilbageføre købet.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-120">If you have already paid for items on the posted purchase invoice, then you must create a purchase credit memo to reverse the purchase.</span></span> <span data-ttu-id="d3c8b-121">Du kan finde flere oplysninger i [Behandle købsreturvarer eller annulleringer](purchasing-how-process-purchase-returns-cancellations.md).</span><span class="sxs-lookup"><span data-stu-id="d3c8b-121">For more information, see [Process Purchase Returns or Cancellations](purchasing-how-process-purchase-returns-cancellations.md).</span></span>

<span data-ttu-id="d3c8b-122">Varer kan være af typen **Lager** eller **Service**.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-122">Items can be type **Inventory** or **Service**.</span></span> <span data-ttu-id="d3c8b-123">Du kan finde flere oplysninger i [Registrere nye varer](inventory-how-register-new-items.md).</span><span class="sxs-lookup"><span data-stu-id="d3c8b-123">For more information, see [Register New Items](inventory-how-register-new-items.md).</span></span> <span data-ttu-id="d3c8b-124">Købsfakturaproceduren er den samme for begge varetyper.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-124">The purchase invoice process is the same for both item types.</span></span>

<span data-ttu-id="d3c8b-125">Du kan udfylde kreditorfelter i købsfakturaen på to måder, afhængigt af om debitoren er registreret.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-125">You can fill vendor fields on the purchase invoice in two ways depending on whether the vendor is already registered.</span></span>

## <a name="to-create-a-purchase-invoice"></a><span data-ttu-id="d3c8b-126">Sådan oprettes en købsfaktura</span><span class="sxs-lookup"><span data-stu-id="d3c8b-126">To create a purchase invoice</span></span>
1. <span data-ttu-id="d3c8b-127">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Købsfakturaer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-127">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchase Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="d3c8b-128">I feltet **Kreditor** skal du indtaste navnet på en eksisterende kreditor.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-128">In the **Vendor** field, enter the name of an existing vendor.</span></span>

    <span data-ttu-id="d3c8b-129">Andre felter i vinduet **Købsfaktura** er nu udfyldt med standardoplysningerne for den valgte kreditor.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-129">Other fields in the **Purchase Invoice** window are now filled with the standard information of the selected vendor.</span></span> <span data-ttu-id="d3c8b-130">Hvis kreditoren ikke er registreret, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="d3c8b-130">If the vendor is not registered, then follow these steps:</span></span>
3. <span data-ttu-id="d3c8b-131">I feltet **Kreditor** skal du indtaste navnet på den nye kreditor.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-131">In the **Vendor** field, enter the name of the new vendor.</span></span>
4. <span data-ttu-id="d3c8b-132">I dialogboksen, hvor du registrerer den nye kreditor, skal du trykke på knappen **Ja**.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-132">In the dialog box about registering the new vendor, choose the **Yes** button.</span></span>
5. <span data-ttu-id="d3c8b-133">I vinduet **Vælg en skabelon til en ny kreditor** skal du vælge en skabelon, som det nye kreditorkort skal baseres på, og derefter vælge knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-133">In the **Select a template for a new vendor** window, choose a template to base the new vendor card on, and then choose the **OK** button.</span></span>
6. <span data-ttu-id="d3c8b-134">Et nyt kreditorkort åbnes, udfyldt med oplysninger om den valgte kreditorskabelon.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-134">A new vendor card opens, prefilled with the information on the selected vendor template.</span></span> <span data-ttu-id="d3c8b-135">Feltet **Navn** udfyldes på forhånd med den nye kreditors navn, som du har angivet på købsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-135">The **Name** field is prefilled with the new vendor’s name that you entered on the purchase invoice.</span></span>
7. <span data-ttu-id="d3c8b-136">Fortsæt med at udfylde resten af felterne på kreditorkortet.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-136">Proceed to fill in the remaining fields on the vendor card.</span></span> <span data-ttu-id="d3c8b-137">Du kan finde flere oplysninger i [Registrere nye kreditorer](purchasing-how-register-new-vendors.md).</span><span class="sxs-lookup"><span data-stu-id="d3c8b-137">For more information, see [Register New Vendors](purchasing-how-register-new-vendors.md).</span></span>  
8. <span data-ttu-id="d3c8b-138">Når du er færdig med kreditorkortet, skal du vælge **OK** for at vende tilbage til vinduet **Købsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-138">When you have completed the vendor card, choose the **OK** button to return to the **Purchase Invoice** window.</span></span>

    <span data-ttu-id="d3c8b-139">Flere felter i vinduet **Købsfaktura** udfyldes med de oplysninger, som du angav på det nye kreditorkort.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-139">Several fields in the **Purchase Invoice** window are filled with information that you specified on the new vendor card.</span></span>
9. <span data-ttu-id="d3c8b-140">Udfyld de resterende felter efter behov i vinduet **Købsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-140">Fill in the remaining fields in the **Purchase Invoice** window as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    <span data-ttu-id="d3c8b-141">Du er nu klar til at udfylde købsfakturalinjerne med lagervarer eller services, som du har købt af kreditoren.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-141">You are now ready to fill in the purchase invoice lines with inventory items or services that you have purchased from the vendor.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="d3c8b-142">Hvis du har konfigureret de tilbagevendende købslinjer for kreditoren, f.eks en månedlig genbestillingsordre, kan du indsætte disse linjer i fakturaen ved at vælge handlingen **Hent tilbagevendende købslinjer**.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-142">If you have set up recurring purchase lines for the vendor, such as a monthly replenishment order, then you can insert these lines on the invoice by choosing the **Get Recurring Purchase Lines** action.</span></span>
10. <span data-ttu-id="d3c8b-143">I oversigtspanelet **Linjer** skal du i feltet **Varenr.** indsætte nummeret på en vare eller en service.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-143">On the **Lines** FastTab, in the **Item No.** field, enter the number of an inventory item or service.</span></span>
11. <span data-ttu-id="d3c8b-144">Angiv antal varer, der skal købes, i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-144">In the **Quantity** field, enter the number of items to be purchased.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="d3c8b-145">For varer af typen **Service** er antallet en tidsenhed, f.eks. timer, der er angivet i feltet **Enhedskode** på linjen.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-145">For items of type **Service**, the quantity is a time unit, such as hours, as indicated in the **Unit of Measure Code** field on the line.</span></span>

    <span data-ttu-id="d3c8b-146">Feltet **Linjebeløb** opdateres, så det viser værdien i feltet **Købspris** ganget med værdien i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-146">The **Line Amount** field is updated to show the value in the **Direct Unit Cost** field multiplied by the value in the **Quantity** field.</span></span>

    <span data-ttu-id="d3c8b-147">Prisen og linjebeløbet vises med eller uden moms, afhængigt af hvad du har valgt i feltet **Priser inkl. moms** på kreditorkortet.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-147">The price and line amount are shown with or without sales tax depending on what you selected in the **Prices Including Tax** field on the vendor card.</span></span>
12. <span data-ttu-id="d3c8b-148">I feltet **Fakturarabatbeløb** skal du indtaste et beløb, der trækkes fra den værdi, der vises i feltet **I alt inkl. moms** nederst i fakturaen.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-148">In the **Invoice Discount Amount** field, enter an amount that should be deducted from the value shown in the **Total Incl. Tax** field at the bottom of the invoice.</span></span>

    > [!NOTE]  
    >   <span data-ttu-id="d3c8b-149">Hvis du har konfigureret fakturarabatter til kreditoren, indsættes den angivne procentværdi automatisk i feltet **Leverandørfakturarabat i %**, hvis kriterierne er opfyldt, og det relaterede beløb indsættes i feltet **Fakturarabatbeløb**.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-149">If you have set up invoice discounts for the vendor, then the specified percentage value is automatically inserted in the **Vendor Invoice Discount %** field if the criteria are met, and the related amount is inserted in the **Invoice Discount Amount** field.</span></span>
13. <span data-ttu-id="d3c8b-150">Når du modtager de købte varer eller servicer, skal du vælge **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-150">When you receive the purchased items or services, choose **Post**.</span></span>

<span data-ttu-id="d3c8b-151">Købet afspejles nu i lager- og finansrecords, og kreditorbetalingen aktiveres.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-151">The purchase is now reflected in inventory and financial records, and the vendor payment is activated.</span></span> <span data-ttu-id="d3c8b-152">Købsfakturaen fjernes fra listen over købsfakturaer og erstattes med et nyt bilag i oversigten over bogførte købsfakturaer.</span><span class="sxs-lookup"><span data-stu-id="d3c8b-152">The purchase invoice is removed from the list of purchase invoices and replaced with a new document in the list of posted purchase invoices.</span></span>

## <a name="see-also"></a><span data-ttu-id="d3c8b-153">Se også</span><span class="sxs-lookup"><span data-stu-id="d3c8b-153">See Also</span></span>
[<span data-ttu-id="d3c8b-154">Køb</span><span class="sxs-lookup"><span data-stu-id="d3c8b-154">Purchasing</span></span>](purchasing-manage-purchasing.md)  
[<span data-ttu-id="d3c8b-155">Opsætning af indkøb</span><span class="sxs-lookup"><span data-stu-id="d3c8b-155">Setting Up Purchasing</span></span>](purchasing-setup-purchasing.md)  
[<span data-ttu-id="d3c8b-156">Anmode om tilbud</span><span class="sxs-lookup"><span data-stu-id="d3c8b-156">Request Quotes</span></span>](purchasing-how-request-quotes.md)  
[<span data-ttu-id="d3c8b-157">Købe varer til et salg</span><span class="sxs-lookup"><span data-stu-id="d3c8b-157">Purchase Items for a Sale</span></span>](purchasing-how-purchase-products-sale.md)  
[<span data-ttu-id="d3c8b-158">Registrere nye kreditorer</span><span class="sxs-lookup"><span data-stu-id="d3c8b-158">Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
[<span data-ttu-id="d3c8b-159">Forberede direkte leveringer</span><span class="sxs-lookup"><span data-stu-id="d3c8b-159">Prepare Drop Shipments</span></span>](sales-how-drop-shipment.md)  
<span data-ttu-id="d3c8b-160">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d3c8b-160">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
