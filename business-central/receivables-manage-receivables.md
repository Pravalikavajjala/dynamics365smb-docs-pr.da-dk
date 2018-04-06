---
title: Oversigt over opgaver til administration af tilgodehavender | Microsoft Docs
description: Beskrives opgaver til administration af tilgodehavender og udligning af betalinger til debitor- eller kreditorposter.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customer payment, debtor, balance due, AR
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 3ffd3b31dcef871ceb30eae6a041f68a4972b2cb
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="managing-receivables"></a><span data-ttu-id="a754a-103">Administrere tilgodehavender</span><span class="sxs-lookup"><span data-stu-id="a754a-103">Managing Receivables</span></span>
<span data-ttu-id="a754a-104">Almindelige trin i en økonomisk cyklus er at udligne bankkonti, hvilket indebærer, at du udligner betalinger til debitor- eller kreditorposter for at lukke salgsfakturaer og købskreditnotaer.</span><span class="sxs-lookup"><span data-stu-id="a754a-104">A regular step in any financial rhythm is to reconcile bank accounts, which requires that you apply payments to customer or vendor ledger entries to close sales invoices and purchase credit memos.</span></span>  

<span data-ttu-id="a754a-105">I [!INCLUDE[d365fin](includes/d365fin_md.md)] kan du hurtigt registrere betalinger i vinduet **Betalingsudligningskladde** ved at importere en bankkontoudtogsfil eller et -feed.</span><span class="sxs-lookup"><span data-stu-id="a754a-105">In [!INCLUDE[d365fin](includes/d365fin_md.md)], one of the fastest ways to register payments from the **Payment Reconciliation Journal** window by importing a bank statement file or feed.</span></span> <span data-ttu-id="a754a-106">Betalingerne udlignes til åbne debitor- eller kreditorposter baseret på sammenligninger af data i betalingstekst og oplysninger i poster.</span><span class="sxs-lookup"><span data-stu-id="a754a-106">The payments are applied to open customer or vendor ledger entries based on data matches between payment text and entry information.</span></span> <span data-ttu-id="a754a-107">Du kan gennemse og ændre de fundne data, før du bogfører kladden, og lukke bankposter for poster, når du bogfører kladden.</span><span class="sxs-lookup"><span data-stu-id="a754a-107">You can review and change the matches before you post the journal, and close bank account ledger entries for ledger entries when you post the journal.</span></span> <span data-ttu-id="a754a-108">Bankkontoen er udlignet, når alle betalinger er udlignet.</span><span class="sxs-lookup"><span data-stu-id="a754a-108">The bank account is reconciled when all payments are applied.</span></span>

<span data-ttu-id="a754a-109">Der findes imidlertid andre steder, hvor det er praktisk at udligne betalinger og afstemme bankkonti:</span><span class="sxs-lookup"><span data-stu-id="a754a-109">There are, however, other handy places to apply payments and reconcile bank accounts:</span></span>  

* <span data-ttu-id="a754a-110">Vinduet **Bankkontoafstemninger**, hvor du kan også kontrollere poster.</span><span class="sxs-lookup"><span data-stu-id="a754a-110">The **Bank Account Reconciliations** window, which also lets you check ledger entries.</span></span> <span data-ttu-id="a754a-111">Du kan finde flere oplysninger i [Afstemme bankkonti separat](bank-how-reconcile-bank-accounts-separately.md).</span><span class="sxs-lookup"><span data-stu-id="a754a-111">For more information, see [Reconcile Bank Accounts Separately](bank-how-reconcile-bank-accounts-separately.md).</span></span>  
* <span data-ttu-id="a754a-112">Vinduet **Betalingsregistrering**, hvor du kan udligne og manuelt kontrollere betalinger modtaget som kontant, check eller banktransaktion ud fra en genereret liste over ubetalte salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="a754a-112">The **Payment Registration** window, where you can apply and manually check payments received as cash, check, or bank transaction against a generated list of unpaid sales documents.</span></span> <span data-ttu-id="a754a-113">Bemærk, at denne funktion kun er tilgængelig for salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="a754a-113">Note that this functionality is available only for sales documents.</span></span>  
* <span data-ttu-id="a754a-114">Vinduet **Indbetalingskladde**, hvor du manuelt bogfører indbetalinger til den relevante finans- eller debitorkonto eller anden konto ved at indtaste en betalingslinje.</span><span class="sxs-lookup"><span data-stu-id="a754a-114">The **Cash Receipt Journal** window, where you manually post receipts to the relevant general ledger, customer, or other account by entering a payment line.</span></span> <span data-ttu-id="a754a-115">Du kan enten udligne indbetalingen eller refunderingen til en eller flere åbne poster, før du bogfører indbetalingskladden, eller fra debitorposterne.</span><span class="sxs-lookup"><span data-stu-id="a754a-115">You can either apply the receipt or refund to one or more open entries before you post the cash receipt journal, or from the customer ledger entries.</span></span>  

<span data-ttu-id="a754a-116">En andet område af administration af tilgodehavender er at indhente udestående beløb, herunder gebyrer, og udstede rykkere.</span><span class="sxs-lookup"><span data-stu-id="a754a-116">Another part of managing receivables is to collect outstanding balances, including finance charges, and issue reminders.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="a754a-117"> indeholder også måder at gøre dette på.</span><span class="sxs-lookup"><span data-stu-id="a754a-117"> offers ways to do those things as well.</span></span> <span data-ttu-id="a754a-118">Du kan finde flere oplysninger under [Indhente udestående beløb](receivables-collect-outstanding-balances.md).</span><span class="sxs-lookup"><span data-stu-id="a754a-118">For more information, see [Collect Outstanding Balances](receivables-collect-outstanding-balances.md).</span></span>  

<span data-ttu-id="a754a-119">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="a754a-119">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

| <span data-ttu-id="a754a-120">Hvis du vil</span><span class="sxs-lookup"><span data-stu-id="a754a-120">To</span></span> | <span data-ttu-id="a754a-121">Se</span><span class="sxs-lookup"><span data-stu-id="a754a-121">See</span></span> |
| --- | --- |
| <span data-ttu-id="a754a-122">Udligne betalinger for at åbne debitor- eller kreditorposter baseret på et importeret bankkontoudtogsfil eller -feed og afstemme bankkontoen, når alle betalinger er udlignet.</span><span class="sxs-lookup"><span data-stu-id="a754a-122">Apply payments to open customer or vendor ledger entries based on an imported bank statement file or feed, and reconcile the bank account when all payments are applied.</span></span> |[<span data-ttu-id="a754a-123">Udligne betalinger automatisk og afstemme bankkonti</span><span class="sxs-lookup"><span data-stu-id="a754a-123">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md) |
| <span data-ttu-id="a754a-124">Udligne betalinger for at åbne debitorposter baseret på manuel indtastning på en liste over ubetalte salgsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="a754a-124">Apply payments to open customer ledger entries based on manual entry in a list of unpaid sales documents.</span></span> |[<span data-ttu-id="a754a-125">Afstemme debitorbetalinger manuelt på en liste over ubetalte salgsdokumenter</span><span class="sxs-lookup"><span data-stu-id="a754a-125">Reconcile Customer Payments Manually From a List of Unpaid Sales Documents</span></span>](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) |
| <span data-ttu-id="a754a-126">Bogføre indbetalinger eller refusioner for debitorer i indbetalingskladden og udligne debitorposter, fra kladden eller fra bogførte poster.</span><span class="sxs-lookup"><span data-stu-id="a754a-126">Post cash receipts or refunds for customers in the cash receipt journal and apply to customer ledger entries, either from the journal or from posted ledger entries.</span></span> |[<span data-ttu-id="a754a-127">Afstemme debitorbetalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="a754a-127">Reconcile Customer Payments Manually</span></span>](receivables-how-apply-sales-transactions-manually.md) |
| <span data-ttu-id="a754a-128">Minde debitorer om forfaldne beløb, beregne rente, oprette rentenotaer og håndtere tilgodehavender.</span><span class="sxs-lookup"><span data-stu-id="a754a-128">Remind customers of overdue amounts, calculate interest and finance charges, and manage accounts receivable.</span></span> |[<span data-ttu-id="a754a-129">Indhente udestående beløb</span><span class="sxs-lookup"><span data-stu-id="a754a-129">Collect Outstanding Balances</span></span>](receivables-collect-outstanding-balances.md) |
|<span data-ttu-id="a754a-130">Du kan sikre dig, at du kender omkostningerne for leverede varer ved at tildele ekstra vareomkostninger, f.eks. fragt, fysisk håndtering, forsikring og transport, som du har efter salg af varer.</span><span class="sxs-lookup"><span data-stu-id="a754a-130">Ensure that you know the cost of shipped items by assigning added item costs, such as freight, physical handling, insurance, and transportation that you incur after selling.</span></span>|[<span data-ttu-id="a754a-131">Bruge varegebyrer til at angive ekstra handelsomkostninger</span><span class="sxs-lookup"><span data-stu-id="a754a-131">Use Item Charges to Account for Additional Trade Costs</span></span>](payables-how-assign-item-charges.md)|
|<span data-ttu-id="a754a-132">Angive en tolerance, som systemet lukker en faktura efter, også selvom betalingen, inklusive eventuel rabat, ikke fuldt ud dækker beløbet på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="a754a-132">Set up a tolerance by which the system closes an invoice even though the payment, including any discount, does not fully cover the amount on the invoice.</span></span>|[<span data-ttu-id="a754a-133">Arbejde med betalingstolerancer og kontantrabattolerancer</span><span class="sxs-lookup"><span data-stu-id="a754a-133">Work with Payment Tolerances and Payment Discount Tolerances</span></span>](finance-payment-tolerance-and-payment-discount-tolerance.md)|
## <a name="see-also"></a><span data-ttu-id="a754a-134">Se også</span><span class="sxs-lookup"><span data-stu-id="a754a-134">See Also</span></span>
[<span data-ttu-id="a754a-135">Salg</span><span class="sxs-lookup"><span data-stu-id="a754a-135">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="a754a-136">Administrere skyldige beløb</span><span class="sxs-lookup"><span data-stu-id="a754a-136">Managing Payables</span></span>](payables-manage-payables.md)  
<span data-ttu-id="a754a-137">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a754a-137">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="a754a-138">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="a754a-138">General Business Functionality</span></span>](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]
