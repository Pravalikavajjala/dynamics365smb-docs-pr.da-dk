---
title: "Udligne betalinger til relaterede dokumenter og bogføre dem | Microsoft Docs"
description: "Beskriver, hvordan du registrerer betalinger, du foretager til leverandører, og refusioner, du foretager til kunder."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, customer refund, creditor, debt, balance due, AP
ms.date: 04/30/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 3cad699234d95a849bf48f04c8462afa968789f6
ms.contentlocale: da-dk
ms.lasthandoff: 05/15/2018

---
# <a name="record-payments-and-refunds"></a><span data-ttu-id="63c56-103">Registrere betalinger og refusioner</span><span class="sxs-lookup"><span data-stu-id="63c56-103">Record Payments and Refunds</span></span>
<span data-ttu-id="63c56-104">I vinduet **Udbetalingskladde** registrerer du betalinger, du foretager til leverandører, og refusioner, du foretager til kunder.</span><span class="sxs-lookup"><span data-stu-id="63c56-104">In the **Payment Journal** window, you record payments that you make to vendors and refunds that you make to customers.</span></span> <span data-ttu-id="63c56-105">Når du bogfører en udbetalingskladdelinje, registreres det betalte beløb i det angivne banksystem.</span><span class="sxs-lookup"><span data-stu-id="63c56-105">When you post a payment journal line, the paid amount is recorded on the specified system bank account.</span></span> <span data-ttu-id="63c56-106">Du skal derefter sørge for at udføre den faktiske pengeoverførsel fra den relaterede bankkonto.</span><span class="sxs-lookup"><span data-stu-id="63c56-106">You must then take steps to perform the actual money transfer from the related bank account.</span></span>

<span data-ttu-id="63c56-107">Hvis du udfylder feltet **Udligningsbilagsnr.** med den faktura eller kreditnota, der skal betales eller refunderes, indstillet det pågældende dokument til betalt, når du bogfører kladden.</span><span class="sxs-lookup"><span data-stu-id="63c56-107">If you fill in the **Applies-to Doc. No.** field with the invoice or credit memo that must be paid or refunded, then the document in question is set to paid when you post the journal.</span></span> <span data-ttu-id="63c56-108">Det betegnes "udlignet".</span><span class="sxs-lookup"><span data-stu-id="63c56-108">This is referred to as "applied".</span></span> <span data-ttu-id="63c56-109">Som et alternativ til udligning under bogføring af betalingen, kan du bruge vinduerne **Udlign kred.poster** og **Udlign debitorposter**, når du har foretaget bogføringen af betalingen.</span><span class="sxs-lookup"><span data-stu-id="63c56-109">As an alternative to applying during payment posting, you can use the **Apply Vendor Entries** and **Apply Customer Entries** window after you have made the payment posting.</span></span> <span data-ttu-id="63c56-110">Du kan finde flere oplysninger i f.eks. [Udligne kreditorbetalinger manuelt](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="63c56-110">For more information, see, for example, [Reconcile Vendor Payments Manually](payables-how-apply-purchase-transactions-manually.md).</span></span>

<span data-ttu-id="63c56-111">Funktionen **Lav forslag** kan hjælpe dig med at udfylde betalingskladdelinjer automatisk i overensstemmelse med kreditorprioriteringen og forfaldsdatoer.</span><span class="sxs-lookup"><span data-stu-id="63c56-111">The **Suggest Vendor Payments** function can help you fill payment journal lines automatically according to vendor prioritization and due dates.</span></span> <span data-ttu-id="63c56-112">Du kan finde flere oplysninger i [Lave kreditorbetalingsforslag](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="63c56-112">For more information, see [Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span> <span data-ttu-id="63c56-113">Med denne funktion er feltet **Udligningsbilagsnr.** altid udfyldt.</span><span class="sxs-lookup"><span data-stu-id="63c56-113">With this function, the **Applies-to Doc. No.** field is always filled in.</span></span>

<span data-ttu-id="63c56-114">Ud over at registrere, at betalingen er foretaget, kan du også bruge vinduet **Udbetalingskladde** til at sende betalingen til yderligere behandling i banken.</span><span class="sxs-lookup"><span data-stu-id="63c56-114">In addition to recording that the payment is made, you can also use the **Payment Journal** window to output the payment for further processing by your bank.</span></span> <span data-ttu-id="63c56-115">Du kan finde flere oplysninger i [Foretage betalinger med check](payables-how-work-checks.md) og [Foretage elektroniske betalinger](payables-how-export-payments-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="63c56-115">For more information, see [Make Check Payments](payables-how-work-checks.md) and [Make Electronic Payments](payables-how-export-payments-bank-file.md).</span></span>  

1. <span data-ttu-id="63c56-116">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Udbetalingskladder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="63c56-116">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="63c56-117">Åbn det kladdenavn, der er dedikeret til betalinger.</span><span class="sxs-lookup"><span data-stu-id="63c56-117">Open the journal batch that is dedicated to payments.</span></span>
3. <span data-ttu-id="63c56-118">Hvis du ved, hvem der skal betales eller refunderes, skal du udfylde felterne manuelt.</span><span class="sxs-lookup"><span data-stu-id="63c56-118">If you know who to pay or refund, fill in the fields manually.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. <span data-ttu-id="63c56-119">Du kan også udligne betalingen til den relaterede faktura eller kreditnota, vælge feltet **Udligningsbilagsnr.**</span><span class="sxs-lookup"><span data-stu-id="63c56-119">To also apply the payment to the related invoice or credit memo, choose the **Applies-to Doc No.**</span></span> <span data-ttu-id="63c56-120">i vinduet **Udlign kred.poster**, vælge den relevante faktura eller kreditnota og derefter vælge knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="63c56-120">field, in the **Apply Vendor Entries** window, select the relevant invoice or credit memo, and then choose the **OK** button.</span></span>

    <span data-ttu-id="63c56-121">Mange felter som f.eks. feltet **Beløb** og **Forfaldsdato** udfyldes nu med oplysninger fra det valgte dokument.</span><span class="sxs-lookup"><span data-stu-id="63c56-121">Many fields, such as the **Amount** and **Due Date** fields, are now filled in with information from the selected document.</span></span>
5. <span data-ttu-id="63c56-122">Du kan også bruge funktionen **Lav kreditorbetalingsforslag**.</span><span class="sxs-lookup"><span data-stu-id="63c56-122">Alternatively, use the **Suggest Vendor Payments** function.</span></span> <span data-ttu-id="63c56-123">Alle udligningsoplysninger og -beløb angives derefter også på kladdelinjerne.</span><span class="sxs-lookup"><span data-stu-id="63c56-123">All the applies-to information and amounts are then also entered on the journal lines.</span></span> <span data-ttu-id="63c56-124">Du kan finde flere oplysninger i [Lave kreditorbetalingsforslag](payables-how-suggest-vendor-payments.md).</span><span class="sxs-lookup"><span data-stu-id="63c56-124">For more information, see [Suggest Vendor Payments](payables-how-suggest-vendor-payments.md).</span></span>

    <span data-ttu-id="63c56-125">Meddelelser hjælper dig til at udfylde de obligatoriske felter korrekt.</span><span class="sxs-lookup"><span data-stu-id="63c56-125">Messages will guide you to fill in the required fields correctly.</span></span>
6.  <span data-ttu-id="63c56-126">Når alle betalingskladdelinjer er fuldført, skal du vælge handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="63c56-126">When all payment journal lines are completed, choose the **Post** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="63c56-127">Se også</span><span class="sxs-lookup"><span data-stu-id="63c56-127">See Also</span></span>
[<span data-ttu-id="63c56-128">Foretage betalinger med check</span><span class="sxs-lookup"><span data-stu-id="63c56-128">Make Check Payments</span></span>](payables-how-work-checks.md)  
[<span data-ttu-id="63c56-129">Foretage elektroniske betalinger</span><span class="sxs-lookup"><span data-stu-id="63c56-129">Make Electronic Payments</span></span>](payables-how-export-payments-bank-file.md)  
[<span data-ttu-id="63c56-130">Administrere skyldige beløb</span><span class="sxs-lookup"><span data-stu-id="63c56-130">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="63c56-131">Konfigurere banktransaktioner</span><span class="sxs-lookup"><span data-stu-id="63c56-131">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="63c56-132">Eksportere en Positive Pay-fil</span><span class="sxs-lookup"><span data-stu-id="63c56-132">Export a Positive Pay file</span></span>](finance-how-positive-pay.md)  
<span data-ttu-id="63c56-133">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="63c56-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
