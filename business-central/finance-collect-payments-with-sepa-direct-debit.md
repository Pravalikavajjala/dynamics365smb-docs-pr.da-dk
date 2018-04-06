---
title: SEPA Direct Debit i Business Central | Microsoft Docs
description: "Du kan opkræve betalinger direkte fra kundens bankkonto i overensstemmelse med SEPA-formatet."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 557d6411540cc778a8f6810e747d4113fccd8f4c
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="collecting-payments-with-sepa-direct-debit"></a><span data-ttu-id="e1515-103">Indhente betalinger med SEPA Direct Debit</span><span class="sxs-lookup"><span data-stu-id="e1515-103">Collecting Payments with SEPA Direct Debit</span></span>
<span data-ttu-id="e1515-104">Du kan opkræve betalinger direkte fra kundens bankkonto i overensstemmelse med SEPA-formatet med kundens samtykke.</span><span class="sxs-lookup"><span data-stu-id="e1515-104">With your customer’s consent, you can collect payments directly from the customer’s bank account according to the SEPA format.</span></span>  

 <span data-ttu-id="e1515-105">Opret først eksportformatet for bankfilen, der instruerer din bank i at udføre en Direct Debit.</span><span class="sxs-lookup"><span data-stu-id="e1515-105">First, set up the export format of the bank file that instructs your bank to perform a direct debit.</span></span> <span data-ttu-id="e1515-106">Derefter konfigureres kundens betalingsform.</span><span class="sxs-lookup"><span data-stu-id="e1515-106">Then, set up the customer’s payment method.</span></span> <span data-ttu-id="e1515-107">Til sidst oprettes den Direct Debit-betalingsaftale, der afspejler din aftale med kunden om opkrævning af deres betalinger i en bestemt periode i aftalen.</span><span class="sxs-lookup"><span data-stu-id="e1515-107">Last, set up the direct-debit mandate that reflects your agreement with the customer to collect their payments in a certain agreement period.</span></span>  

 <span data-ttu-id="e1515-108">For at instruere banken i at overføre det indbetalte beløb fra kundens bankkonto til din virksomheds konto, opretter du en post i den Direct Debit-opkrævning, der indeholder oplysninger om bankkonti, de berørte salgsfakturaer og den Direct Debit-betalingsaftale.</span><span class="sxs-lookup"><span data-stu-id="e1515-108">To instruct the bank to transfer the payment amount from the customer’s bank account to your company’s account, you create a direct-debit collection entry, which holds information about bank accounts, the affected sales invoices, and the direct-debit mandate.</span></span> <span data-ttu-id="e1515-109">Derefter eksporterer du en XML-fil, der er baseret på opkrævningsposten, som du sender til din bank til behandling.</span><span class="sxs-lookup"><span data-stu-id="e1515-109">You then export an XML file that is based on the collection entry, which you send to your bank for processing.</span></span> <span data-ttu-id="e1515-110">Du får besked fra banken om alle betalinger, der ikke kunne behandles af banken, og derefter skal du manuelt afvise de pågældende poster i den Direct Debit-opkrævning.</span><span class="sxs-lookup"><span data-stu-id="e1515-110">Any payments that could not be processed will be communicated to you by your bank, and you must then manually reject the direct debit-collection entries in question.</span></span>  

 <span data-ttu-id="e1515-111">Du kan angive standarddebitorsalgskoder med oplysninger om Direct Debit-betalingsform og -bemyndigelse.</span><span class="sxs-lookup"><span data-stu-id="e1515-111">You can set up standard customer sales codes with the direct-debit payment method and mandate information.</span></span> <span data-ttu-id="e1515-112">Du kan derefter bruge kørslen **Opret standardkundefakturaer** til at generere flere salgsfakturaer med oplysninger om Direct Debit udfyldt på forhånd.</span><span class="sxs-lookup"><span data-stu-id="e1515-112">You can then use the **Create Standard Cust. Invoices** batch job to generate multiple sales invoices with the direct-debit information prefilled.</span></span> <span data-ttu-id="e1515-113">Dette kan udføres manuelt eller automatisk, alt efter betalingens forfaldsdato.</span><span class="sxs-lookup"><span data-stu-id="e1515-113">This is can be done manually or automatically, according to the payment due date.</span></span>  

 <span data-ttu-id="e1515-114">Når betalinger er behandlet, og banken har informeret om det, kan du bogføre betalingskvitteringer enten direkte fra vinduet **Poster i Direct Debit-opkrævning** eller ved at flytte betalingslinjerne til den kladde, hvor du bogfører betalingskvitteringer, f.eks. vinduet **Indbetalingskladde**.</span><span class="sxs-lookup"><span data-stu-id="e1515-114">When payments are successfully processed, as communicated by your bank, you can post the payment receipts either directly from the **Direct Debit Collect. Entries** window or by moving the payment lines to the journal where you post payment receipts, such as the **Cash Receipt Journal** window.</span></span> <span data-ttu-id="e1515-115">Alternativt kan du, afhængigt af hvordan din likviditetsstyring foregår, vente og kun anvende betalingerne som en del af bankafstemningen.</span><span class="sxs-lookup"><span data-stu-id="e1515-115">Alternatively, depending on your cash management process, you can wait and just apply the payments as a part of bank reconciliation.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="e1515-116">Hvis du vil samle betalinger ved hjælp af SEPA Direct Debit, skal valutaen på salgsfakturaen være i EURO.</span><span class="sxs-lookup"><span data-stu-id="e1515-116">To collect payments using SEPA Direct Debit, the currency on the sales invoice must be EURO.</span></span>  

 <span data-ttu-id="e1515-117">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="e1515-117">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="e1515-118">**Hvis du vil**</span><span class="sxs-lookup"><span data-stu-id="e1515-118">**To**</span></span>|<span data-ttu-id="e1515-119">**Se**</span><span class="sxs-lookup"><span data-stu-id="e1515-119">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="e1515-120">Udarbejd bankkontoformater, betalingsformer og kundeaftaler til SEPA Direct Debit.</span><span class="sxs-lookup"><span data-stu-id="e1515-120">Prepare bank account formats, payment methods, and customer agreements for SEPA direct debit.</span></span>|[<span data-ttu-id="e1515-121">Konfigurere SEPA Direct Debit</span><span class="sxs-lookup"><span data-stu-id="e1515-121">Set Up SEPA Direct Debit</span></span>](finance-how-to-set-up-sepa-direct-debit.md)|  
|<span data-ttu-id="e1515-122">Bed din bank om at overføre beløb fra din kundes bankkonti til dit firmas konto i overensstemmelse med konfigurationen af SEPA Direct Debit.</span><span class="sxs-lookup"><span data-stu-id="e1515-122">Instruct your bank to transfer payment amounts from your customers’ bank accounts to your company’s account according to your setup of SEPA direct debit.</span></span>|[<span data-ttu-id="e1515-123">Oprette poster i SEPA Direct Debit-opkrævning, og eksportere til en bankfil</span><span class="sxs-lookup"><span data-stu-id="e1515-123">Create SEPA Direct Debit Collection Entries and Export to a Bank File</span></span>](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)|  
|<span data-ttu-id="e1515-124">Konfigurer standarddebitorsalgskoder for fakturaer til direkte debitering, og opret salgsfakturaer med oplysninger om direkte debitering, når fakturaerne forfalder til betaling.</span><span class="sxs-lookup"><span data-stu-id="e1515-124">Set up standard customer sales codes for direct-debit invoices and generate sales invoices with direct-debit information when the invoices are due for payment.</span></span>|[<span data-ttu-id="e1515-125">Oprette gentagne salgs- og købslinjer</span><span class="sxs-lookup"><span data-stu-id="e1515-125">Create Recurring Sales and Purchase Lines</span></span>](sales-how-work-standard-lines.md)|  
|<span data-ttu-id="e1515-126">Bogfør betalinger foretaget som SEPA Direct Debit.</span><span class="sxs-lookup"><span data-stu-id="e1515-126">Post payments made as SEPA direct debits.</span></span>|[<span data-ttu-id="e1515-127">Bogføre SEPA Direct Debit-betalingskvitteringer</span><span class="sxs-lookup"><span data-stu-id="e1515-127">Post SEPA Direct Debit Payment Receipts</span></span>](finance-how-to-post-sepa-direct-debit-payment-receipts.md)|  

## <a name="see-also"></a><span data-ttu-id="e1515-128">Se også</span><span class="sxs-lookup"><span data-stu-id="e1515-128">See Also</span></span>  
[<span data-ttu-id="e1515-129">Administrere tilgodehavender</span><span class="sxs-lookup"><span data-stu-id="e1515-129">Managing Receivables</span></span>](receivables-manage-receivables.md)
