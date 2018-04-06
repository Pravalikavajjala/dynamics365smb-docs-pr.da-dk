---
title: Udligne poster i forskellige valutaer | Microsoft Docs
description: "Du kan udligne finansposter i flere valutaer, f.eks. hvis du sælger i én valuta og modtager betaling i en anden."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 01/25/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 960ae581a3f933c6e9c2ed5183944ddf62ca5965
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="enable-application-of-ledger-entries-in-different-currencies"></a><span data-ttu-id="44e46-103">Aktivere anvendelsen af finansposter i forskellige valutaer</span><span class="sxs-lookup"><span data-stu-id="44e46-103">Enable Application of Ledger Entries in Different Currencies</span></span>
<span data-ttu-id="44e46-104">Hvis du køber varer fra en leverandør i én valuta, men foretager betaling i en anden valuta, kan du udligne betalingen med købet.</span><span class="sxs-lookup"><span data-stu-id="44e46-104">If you purchase from a vendor in one currency and submit payment in another currency, you can apply the payment to the purchase.</span></span>

<span data-ttu-id="44e46-105">Ligeledes, hvis du sælger til en debitor i en valuta og modtager betaling i en anden, kan du knytte betalingen til salgsfakturaen.</span><span class="sxs-lookup"><span data-stu-id="44e46-105">Likewise, if you sell to a customer in one currency and receive payment in another currency, you can apply the payment to the sales invoice.</span></span>

<span data-ttu-id="44e46-106">Følgende procedure beskriver, hvordan du kan angive dette for kreditorposter i vinduet **Købsopsætning**.</span><span class="sxs-lookup"><span data-stu-id="44e46-106">The following procedure describes how to set this up for vendor ledger entries in the **Purchases & Payables Setup** window.</span></span> <span data-ttu-id="44e46-107">Der er tilsvarende opsætning for debitorposter i vinduet **Salgsopsætning**.</span><span class="sxs-lookup"><span data-stu-id="44e46-107">The setup is similar for customer ledger entries in the **Sales & Receivables Setup** window.</span></span>

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a><span data-ttu-id="44e46-108">Sådan aktiveres udligning af kreditorposter i forskellige valutaer</span><span class="sxs-lookup"><span data-stu-id="44e46-108">To enable application of vendor ledger entries in different currencies</span></span>
1. <span data-ttu-id="44e46-109">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Købsopsætning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="44e46-109">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Purchases & Payables Setup**, and then choose the related link.</span></span>
2. <span data-ttu-id="44e46-110">Vælg en af følgende indstillinger i feltet **Valutaudligning**.</span><span class="sxs-lookup"><span data-stu-id="44e46-110">In the **Appln. between Currencies** field, select one of the following options.</span></span>

| <span data-ttu-id="44e46-111">Indstilling</span><span class="sxs-lookup"><span data-stu-id="44e46-111">Option</span></span> | <span data-ttu-id="44e46-112">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="44e46-112">Description</span></span> |
| --- | --- |
| <span data-ttu-id="44e46-113">Ingen</span><span class="sxs-lookup"><span data-stu-id="44e46-113">None</span></span> |<span data-ttu-id="44e46-114">Udligning mellem valutaer er ikke tilladt.</span><span class="sxs-lookup"><span data-stu-id="44e46-114">Application between currencies is not allowed.</span></span> |
| <span data-ttu-id="44e46-115">ØMU</span><span class="sxs-lookup"><span data-stu-id="44e46-115">EMU</span></span> |<span data-ttu-id="44e46-116">Udligning mellem ØMU-valutaer er tilladt.</span><span class="sxs-lookup"><span data-stu-id="44e46-116">Application between EMU currencies is allowed.</span></span> |
| <span data-ttu-id="44e46-117">Alle</span><span class="sxs-lookup"><span data-stu-id="44e46-117">All</span></span> |<span data-ttu-id="44e46-118">Udligning mellem alle valutaer er tilladt.</span><span class="sxs-lookup"><span data-stu-id="44e46-118">Application between all currencies is allowed.</span></span> |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a><span data-ttu-id="44e46-119">Sådan opsættes finanskonti til afrundingsdifferencer ved valutaudligning</span><span class="sxs-lookup"><span data-stu-id="44e46-119">To set up G/L accounts for currency application rounding differences</span></span>  
<span data-ttu-id="44e46-120">Hvis du anvender poster i forskellige valutaer, skal du oprette finanskonti, hvor du kan bogføre afrundingsdifferencer.</span><span class="sxs-lookup"><span data-stu-id="44e46-120">If you apply entries in different currencies, you must set up the general ledger accounts to which you want to post rounding differences.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="44e46-121">Du skal oprette de pågældende finanskonti, før du kan udføre opgaven.</span><span class="sxs-lookup"><span data-stu-id="44e46-121">You must set up the general ledger accounts before you complete the task.</span></span> <span data-ttu-id="44e46-122">Du kan finde flere oplysninger i [Om finans- og kontoplanen](finance-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="44e46-122">For more information, see [Understanding the General Ledger and the Chart of Accounts](finance-general-ledger.md).</span></span>

1. <span data-ttu-id="44e46-123">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Debitorbogføringsgrupper**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="44e46-123">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customer Posting Groups**, and then choose the related link.</span></span>  
2. <span data-ttu-id="44e46-124">I felterne **Valutaudlign.afrnd.kto (deb.)** og **Valutaudlign.afrnd.kto (kre.)** skal du indtaste de relevante finanskonti bogføring af afrundingsdifferencer.</span><span class="sxs-lookup"><span data-stu-id="44e46-124">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  
3. <span data-ttu-id="44e46-125">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Kreditorbogføringsgrupper**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="44e46-125">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendor Posting Groups**, and then choose the related link.</span></span>  
4. <span data-ttu-id="44e46-126">I felterne **Valutaudlign.afrnd.kto (deb.)** og **Valutaudlign.afrnd.kto (kre.)** skal du indtaste de relevante finanskonti bogføring af afrundingsdifferencer.</span><span class="sxs-lookup"><span data-stu-id="44e46-126">In the **Debit Curr. Appln. Rndg. Acc.** and **Credit Curr. Appln. Rndg. Acc.** fields, enter the relevant general ledger accounts to post rounding differences.</span></span>  

## <a name="see-also"></a><span data-ttu-id="44e46-127">Se også</span><span class="sxs-lookup"><span data-stu-id="44e46-127">See Also</span></span>
[<span data-ttu-id="44e46-128">Administrere skyldige beløb</span><span class="sxs-lookup"><span data-stu-id="44e46-128">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="44e46-129">Administrere tilgodehavender</span><span class="sxs-lookup"><span data-stu-id="44e46-129">Managing Receivables</span></span>](receivables-manage-receivables.md)  
<span data-ttu-id="44e46-130">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="44e46-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
