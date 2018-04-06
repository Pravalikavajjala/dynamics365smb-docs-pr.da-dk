---
title: "Bruge udvidelsen QuickBooks-overførsel | Microsoft Docs"
description: "Beskriver, hvordan du bruger udvidelsen til at overføre debitorer, kreditorer, varer og konti fra QuickBooks Online til Business Central."
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, QuickBooks, import
ms.date: 05/24/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f84d2bcccb8876588e7292708ba2cc98fcbe50fb
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---

# <a name="the-quickbooks-online-data-migration-extension-for-business-central"></a><span data-ttu-id="1890b-103">Udvidelsen Overførsel af QuickBooks Online-data til Business Central</span><span class="sxs-lookup"><span data-stu-id="1890b-103">The QuickBooks Online Data Migration Extension for Business Central</span></span>
<span data-ttu-id="1890b-104">Denne udvidelse er inkluderet i den assisterede opsætningsvejledning **Dataoverførsel** for at hjælpe dig med at overføre vigtige forretningsdata fra QuickBooks Online til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="1890b-104">This extension is included in the **Data Migration** assisted setup guide to help you migrate important business data from QuickBooks Online to [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="1890b-105">F.eks. er dette nyttigt, når virksomheden vokser, og du har besluttet at opgradere din virksomheds administrationsapp ved at starte med at bruge [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="1890b-105">For example, this is useful when your business is growing, and you've decided to upgrade your business management app by starting to use [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

## <a name="what-data-can-i-import-from-quickbooks-online"></a><span data-ttu-id="1890b-106">Hvilke data kan jeg importere fra QuickBooks Online?</span><span class="sxs-lookup"><span data-stu-id="1890b-106">What data can I import from QuickBooks Online?</span></span>
<span data-ttu-id="1890b-107">Du kan importere følgende data fra QuickBooks Online til [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span><span class="sxs-lookup"><span data-stu-id="1890b-107">You can import the following data from QuickBooks Online to [!INCLUDE[d365fin](includes/d365fin_md.md)]:</span></span>  

* <span data-ttu-id="1890b-108">Kunder (Debitorer)</span><span class="sxs-lookup"><span data-stu-id="1890b-108">Customers</span></span>
* <span data-ttu-id="1890b-109">Leverandører (Kreditorer)</span><span class="sxs-lookup"><span data-stu-id="1890b-109">Vendors</span></span>
* <span data-ttu-id="1890b-110">Varer</span><span class="sxs-lookup"><span data-stu-id="1890b-110">Items</span></span>
* <span data-ttu-id="1890b-111">Kontoplan</span><span class="sxs-lookup"><span data-stu-id="1890b-111">Chart of accounts</span></span>
* <span data-ttu-id="1890b-112">Primosaldopostering i regnskabet</span><span class="sxs-lookup"><span data-stu-id="1890b-112">Beginning balance transaction in the general ledger</span></span>
* <span data-ttu-id="1890b-113">Disponible antal for lagervarer</span><span class="sxs-lookup"><span data-stu-id="1890b-113">On-hand quantities for inventory items</span></span>
* <span data-ttu-id="1890b-114">Åbne dokumenter for debitorer og kreditorer, f.eks. fakturaer, kreditnotaer og betalinger</span><span class="sxs-lookup"><span data-stu-id="1890b-114">Open documents for customers and vendors, such as invoices, credit memos, and payments</span></span>

<span data-ttu-id="1890b-115">Vi overfører kun fulde beløb på salgs- og købsdokumenter.</span><span class="sxs-lookup"><span data-stu-id="1890b-115">We migrate only full amounts on sales and purchase documents.</span></span> <span data-ttu-id="1890b-116">Delvist betalte beløb opdateres ikke.</span><span class="sxs-lookup"><span data-stu-id="1890b-116">We do not update partially paid amounts.</span></span> <span data-ttu-id="1890b-117">F.eks. hvis en debitor har indbetalt 300 af i alt 500 dollar på en salgsfaktura, overfører vi hele 500.</span><span class="sxs-lookup"><span data-stu-id="1890b-117">For example, if a customer has paid 300 of a total of 500 dollars on a sales invoice, we migrate the full 500.</span></span> <span data-ttu-id="1890b-118">Hvis du har modtaget delbetalinger, skal du opdatere dem manuelt, før eller efter at du overfører data.</span><span class="sxs-lookup"><span data-stu-id="1890b-118">If you have received partial payments, you must update these manually, either before or after you migrate data.</span></span> <span data-ttu-id="1890b-119">Det anbefales, at du anvender udestående transaktioner, inden du overfører, for at gøre tingene nemmere bagefter.</span><span class="sxs-lookup"><span data-stu-id="1890b-119">We recommend that you apply outstanding transactions before you migrate, just to make things easier afterward.</span></span>

> [!NOTE]  
>   <span data-ttu-id="1890b-120">Vi overfører ikke indkøbsordrer eller salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="1890b-120">We do not migrate purchase orders or sales orders.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="1890b-121">Før du starter</span><span class="sxs-lookup"><span data-stu-id="1890b-121">Before you start</span></span>
<span data-ttu-id="1890b-122">Det er en vigtig del af overførslen at angive de konti, transaktioner skal overføres til.</span><span class="sxs-lookup"><span data-stu-id="1890b-122">An important part of the migration process is to specify the accounts to migrate transactions to.</span></span> <span data-ttu-id="1890b-123">Det er en god ide at planlægge denne tilknytning, før du overfører data.</span><span class="sxs-lookup"><span data-stu-id="1890b-123">It's a good idea to plan this mapping before you migrate data.</span></span> <span data-ttu-id="1890b-124">F.eks. de konti, hvor du bogfører poster for:</span><span class="sxs-lookup"><span data-stu-id="1890b-124">For example, the accounts where you post transactions for:</span></span>  

* <span data-ttu-id="1890b-125">Salget af varer eller servicer til debitorer.</span><span class="sxs-lookup"><span data-stu-id="1890b-125">The sale of items or services to customers.</span></span>
* <span data-ttu-id="1890b-126">Køb af varer eller servicer fra kreditorer.</span><span class="sxs-lookup"><span data-stu-id="1890b-126">The purchase of items or services from vendors.</span></span>  
* <span data-ttu-id="1890b-127">Ændringer i finansbogholderiet.</span><span class="sxs-lookup"><span data-stu-id="1890b-127">Adjustments in the general ledger.</span></span>  

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="1890b-128"> kræver, at finanskonti har kontonumre tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="1890b-128"> requires that general ledger accounts have account numbers assigned to them.</span></span> <span data-ttu-id="1890b-129">Sørg for, at kontonumre er tildelt til kontiene i QuickBooks Online.</span><span class="sxs-lookup"><span data-stu-id="1890b-129">Make sure that account numbers are assigned to your accounts in QuickBooks Online.</span></span>

<span data-ttu-id="1890b-130">Hvis der er transaktioner i QuickBooks Online, der har momsbeløb, du skal oprette en momskonto for dine skatteregioner i [!INCLUDE[d365fin](includes/d365fin_md.md)], før du kan bogføre transaktioner.</span><span class="sxs-lookup"><span data-stu-id="1890b-130">If transactions in QuickBooks Online have tax amounts, you must set up a tax account for your tax jurisdictions in [!INCLUDE[d365fin](includes/d365fin_md.md)] before you can post transactions.</span></span>

## <a name="how-do-i-start-using-the-extension"></a><span data-ttu-id="1890b-131">Hvordan begynder jeg at bruge udvidelsen?</span><span class="sxs-lookup"><span data-stu-id="1890b-131">How do I start using the extension?</span></span>
<span data-ttu-id="1890b-132">Det er nemt at komme i gang.</span><span class="sxs-lookup"><span data-stu-id="1890b-132">Getting started is easy.</span></span> <span data-ttu-id="1890b-133">Du skal blot køre den assisterede opsætningsvejledning **Dataoverførsel**.</span><span class="sxs-lookup"><span data-stu-id="1890b-133">All you need to do is run the **Data Migration** assisted setup guide.</span></span> <span data-ttu-id="1890b-134">Sådan gør du:</span><span class="sxs-lookup"><span data-stu-id="1890b-134">Here's how:</span></span>

1. <span data-ttu-id="1890b-135">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Assisteret opsætning**, og vælg derefter **Overflyt virksomhedsdata**.</span><span class="sxs-lookup"><span data-stu-id="1890b-135">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Assisted Setup**, and then choose **Migrate business data**.</span></span>
2. <span data-ttu-id="1890b-136">Følg vejledningen på de enkelte trin i den assisterede opsætningsvejledning.</span><span class="sxs-lookup"><span data-stu-id="1890b-136">Follow the instructions on each step in the assisted setup guide.</span></span>

## <a name="what-do-i-do-after-i-migrate-data"></a><span data-ttu-id="1890b-137">Hvad gør jeg gøre, når jeg har overført data?</span><span class="sxs-lookup"><span data-stu-id="1890b-137">What do I do after I migrate data?</span></span>
<span data-ttu-id="1890b-138">Når du har overført data, har transaktioner status **Ikke-bogførte**, så du kan gennemgå dem og foretage ændringer.</span><span class="sxs-lookup"><span data-stu-id="1890b-138">After you migrate data, transactions have the status **Unposted**, so you can review them and make adjustments.</span></span> <span data-ttu-id="1890b-139">For at få vist transaktionerne skal du gå til siden, hvor du vil finde dem normalt.</span><span class="sxs-lookup"><span data-stu-id="1890b-139">To review the transactions, go to the page where you would normally find them.</span></span> <span data-ttu-id="1890b-140">F.eks. for at få vist ikke-bogførte salgsfakturaer, skal du gå til siden **Salgsfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="1890b-140">For example, to review unposted sales invoices, go to the **Sales Invoices** page.</span></span> <span data-ttu-id="1890b-141">For at få vist udbetalingskladder skal du gå til siden **Udbetalingskladder**.</span><span class="sxs-lookup"><span data-stu-id="1890b-141">To review payment journals, go to the **Payment Journals** page.</span></span>   

<span data-ttu-id="1890b-142">Der er især et par ting, du skal gøre:</span><span class="sxs-lookup"><span data-stu-id="1890b-142">There are a few things in particular that you should do:</span></span>

* <span data-ttu-id="1890b-143">Hvis transaktioner i QuickBooks Online havde avance- eller rabatbeløb, skal du manuelt føje beløbene til de relaterede transaktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)], før du bogfører dem.</span><span class="sxs-lookup"><span data-stu-id="1890b-143">If the transactions in QuickBooks Online had markup or discount amounts, you must manually add the amounts to the related transactions in [!INCLUDE[d365fin](includes/d365fin_md.md)] before you post them.</span></span>
* <span data-ttu-id="1890b-144">Hvis du bruger moms, skal du evt. tilføje en virksomhedsbogføringsgruppe og en produktbogføringsgruppe i bogføringsopsætningen, så du kan bogføre momsbeløb.</span><span class="sxs-lookup"><span data-stu-id="1890b-144">If you are using value added tax (VAT), you may need to add a business posting group and a product posting group to the posting setup so that you can post VAT amounts.</span></span>
* <span data-ttu-id="1890b-145">Kontroller primosaldi for konti i finansbogholderiet.</span><span class="sxs-lookup"><span data-stu-id="1890b-145">Verify the beginning balances for accounts in the general ledger.</span></span> <span data-ttu-id="1890b-146">QuickBooks Online gemmer ikke den aktuelle saldo for alle konti, så det kan være nødvendigt at rette primosaldi.</span><span class="sxs-lookup"><span data-stu-id="1890b-146">QuickBooks Online does not store the current balance for all accounts, so you might need to correct beginning balances.</span></span>

## <a name="see-also"></a><span data-ttu-id="1890b-147">Se også</span><span class="sxs-lookup"><span data-stu-id="1890b-147">See Also</span></span>
[<span data-ttu-id="1890b-148">Importere virksomhedsdata fra andre økonomisystemer</span><span class="sxs-lookup"><span data-stu-id="1890b-148">Importing Business Data from Other Finance Systems</span></span>](upload-data.md)  
<span data-ttu-id="1890b-149">[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="1890b-149">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
