---
title: "Få mere at vide om Finans og kontoplan | Microsoft Docs"
description: Beskriver finans, kontoplanen og kontokategorier.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 1c5fda0c8cd063e784ec44448b040a298bfeaf2f
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="understanding-the-general-ledger-and-the-coa"></a><span data-ttu-id="f5efc-103">Om Finans og kontoplanen</span><span class="sxs-lookup"><span data-stu-id="f5efc-103">Understanding the General Ledger and the COA</span></span>
<span data-ttu-id="f5efc-104">Finansregnskabet gemmer de finansielle data, og kontoplanen viser de konti, som alle finansposter bogføres til.</span><span class="sxs-lookup"><span data-stu-id="f5efc-104">The general ledger stores your financial data, and the chart of accounts shows the accounts that all general ledger entries are posted to.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="f5efc-105"> indeholder en standardkontoplan, der er klar til at understøtte din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="f5efc-105"> includes a standard chart of accounts that is ready to support your business.</span></span>

## <a name="general-ledger-setup-and-general-posting-setup"></a><span data-ttu-id="f5efc-106">Finansopsætning og bogføringsopsætning</span><span class="sxs-lookup"><span data-stu-id="f5efc-106">General Ledger Setup and General Posting Setup</span></span>
<span data-ttu-id="f5efc-107">Opsætningen af finansmodulet er kernen i økonomiprocesser, fordi den definerer, hvordan du bogfører data.</span><span class="sxs-lookup"><span data-stu-id="f5efc-107">The setup of the general ledger is at the core of financial processes because it defines how you post data.</span></span>  

<span data-ttu-id="f5efc-108">I vinduet **Opsætning af Finans** angiver du, hvordan du vil behandle bestemte regnskabsopgaver i virksomheden, f.eks.:</span><span class="sxs-lookup"><span data-stu-id="f5efc-108">In the **General Ledger Setup** window, you specify how to handle certain accounting issues in your company, such as:</span></span>  

* <span data-ttu-id="f5efc-109">Detaljer om fakturaafrunding</span><span class="sxs-lookup"><span data-stu-id="f5efc-109">Invoice rounding details</span></span>  
* <span data-ttu-id="f5efc-110">Adresseformater</span><span class="sxs-lookup"><span data-stu-id="f5efc-110">Address formats</span></span>  
* <span data-ttu-id="f5efc-111">Økonomirapportering</span><span class="sxs-lookup"><span data-stu-id="f5efc-111">Financial reporting</span></span>  

<span data-ttu-id="f5efc-112">Desuden kan du i vinduet **Bogføringsopsætning** angive, hvordan du vil oprette kombinationer af virksomheds- og produktbogføringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="f5efc-112">Similarly, in the **General Posting Setup** window, you specify how you want to set up combinations of general business and general product posting groups.</span></span> <span data-ttu-id="f5efc-113">Bogføringsgrupper knytter enheder som debitorer, kreditorer, varer, ressourcer og salgs- og købsdokumenter til finanskonti.</span><span class="sxs-lookup"><span data-stu-id="f5efc-113">Posting groups map entities like customers, vendors, items, resources, and sales and purchase documents to general ledger accounts.</span></span> <span data-ttu-id="f5efc-114">Udfyld en linje for hver kombination af virksomheds- og produktbogføringsgrupper.</span><span class="sxs-lookup"><span data-stu-id="f5efc-114">You fill in a line for each combination of business posting group and product posting group.</span></span> <span data-ttu-id="f5efc-115">Du kan finde flere oplysninger under [Opsætning af bogføringsgrupper](finance-posting-groups.md)</span><span class="sxs-lookup"><span data-stu-id="f5efc-115">For more information, see [Posting Group Setups](finance-posting-groups.md)</span></span>  

## <a name="the-chart-of-accounts"></a><span data-ttu-id="f5efc-116">Kontoplan</span><span class="sxs-lookup"><span data-stu-id="f5efc-116">The Chart of Accounts</span></span>
<span data-ttu-id="f5efc-117">Kontoplanen viser alle finanskonti.</span><span class="sxs-lookup"><span data-stu-id="f5efc-117">The chart of accounts shows all general ledger accounts.</span></span> <span data-ttu-id="f5efc-118">Fra kontoplanen kan du gøre ting som at:</span><span class="sxs-lookup"><span data-stu-id="f5efc-118">From the chart of accounts, you can do things like:</span></span>  

* <span data-ttu-id="f5efc-119">Vise rapporter med finansposter og saldi.</span><span class="sxs-lookup"><span data-stu-id="f5efc-119">View reports that show general ledger entries and balances.</span></span>  
* <span data-ttu-id="f5efc-120">Lukke din resultatopgørelse.</span><span class="sxs-lookup"><span data-stu-id="f5efc-120">Close your income statement.</span></span>  
* <span data-ttu-id="f5efc-121">Åbne finanskontokortet for at tilføje eller ændre indstillinger.</span><span class="sxs-lookup"><span data-stu-id="f5efc-121">Open the G/L account card to add or change settings.</span></span>  
* <span data-ttu-id="f5efc-122">Se en oversigt over bogføringsgrupper, som bogføres til kontoen.</span><span class="sxs-lookup"><span data-stu-id="f5efc-122">See a list of posting groups that post to that account.</span></span>
* <span data-ttu-id="f5efc-123">Vise separate debet- og kreditsaldi for en enkelt konto</span><span class="sxs-lookup"><span data-stu-id="f5efc-123">View separate debit and credit balances for a single account</span></span>  

<span data-ttu-id="f5efc-124">Du kan tilføje, ændre eller slette finanskonti.</span><span class="sxs-lookup"><span data-stu-id="f5efc-124">You can add, change, or delete general ledger accounts.</span></span> <span data-ttu-id="f5efc-125">Men for at forhindre afvigelser kan du ikke slette en finanskonto, hvis dens data bruges i kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="f5efc-125">However, to prevent discrepancies, you can't delete a general ledger account if it's data is used in the chart of accounts.</span></span>  

## <a name="account-categories"></a><span data-ttu-id="f5efc-126">Kontokategorier</span><span class="sxs-lookup"><span data-stu-id="f5efc-126">Account Categories</span></span>
<span data-ttu-id="f5efc-127">Du kan tilpasse strukturen i regnskabsopgørelser ved at knytte finanskonti til kontokategorier.</span><span class="sxs-lookup"><span data-stu-id="f5efc-127">You can personalize the structure of your financial statements by mapping general ledger accounts to account categories.</span></span>  

<span data-ttu-id="f5efc-128">Vinduet **Finanskontokategorier** viser dine kategorier og underkategorier, og de finanskonti, der er knyttet til dem.</span><span class="sxs-lookup"><span data-stu-id="f5efc-128">The **G/L Account Categories** window shows your categories and subcategories, and the G/L accounts that are assigned to them.</span></span> <span data-ttu-id="f5efc-129">Du kan oprette nye underkategorier og tildele disse kategorier til eksisterende konti.</span><span class="sxs-lookup"><span data-stu-id="f5efc-129">You can create new subcategories and assign those categories to existing accounts.</span></span>  

<span data-ttu-id="f5efc-130">Du kan oprette en kategorigruppe ved at indrykke andre underkategorier under en linje i vinduet **Finanskontokategorier**.</span><span class="sxs-lookup"><span data-stu-id="f5efc-130">You create a category group by indenting other subcategories under a line in the **G/L Account Categories** window.</span></span> <span data-ttu-id="f5efc-131">Dermed kan du nemt få vist en oversigt, da hver grupperingen viser den samlede saldo.</span><span class="sxs-lookup"><span data-stu-id="f5efc-131">This makes it easy for you to get an overview, because each grouping shows a total balance.</span></span> <span data-ttu-id="f5efc-132">Du kan f.eks. oprette underkategorier for forskellige typer anlægsaktiver og derefter oprette kategorigrupper for anlægsaktiver i forhold til omsætningsaktiver.</span><span class="sxs-lookup"><span data-stu-id="f5efc-132">For example, you can create subcategories for different types of assets, and then create category groups for fixed assets versus current assets.</span></span>  

<span data-ttu-id="f5efc-133">Du kan angive, om kontiene i hver underkategori skal medtages i bestemte typer rapporter.</span><span class="sxs-lookup"><span data-stu-id="f5efc-133">You can specify whether the accounts in each subcategory must be included in specific types of reports.</span></span> <span data-ttu-id="f5efc-134">Kontokategorier hjælper med at definere layoutet af regnskabet.</span><span class="sxs-lookup"><span data-stu-id="f5efc-134">The account categories help define the layout of your financial statements.</span></span>  

<span data-ttu-id="f5efc-135">F.eks. har standardsaldoopgørelsen en underkategori for Kassebeholdning under Omsætningsaktiver.</span><span class="sxs-lookup"><span data-stu-id="f5efc-135">For example, the default balance statement has a subcategory for Cash under Current Assets.</span></span> <span data-ttu-id="f5efc-136">Hvis du vil have, at kontantbeholdning og checks skal indgå i saldoopgørelsen, kan du:</span><span class="sxs-lookup"><span data-stu-id="f5efc-136">If you want the balance statement consider petty cash and checking, you can:</span></span>  

1. <span data-ttu-id="f5efc-137">Tilføje to nye underkategorier.</span><span class="sxs-lookup"><span data-stu-id="f5efc-137">Add two new subcategories.</span></span> <span data-ttu-id="f5efc-138">Én for kontantbeholdning og én for din checkkonto.</span><span class="sxs-lookup"><span data-stu-id="f5efc-138">One for petty cash, and one for your checking account.</span></span>  
2. <span data-ttu-id="f5efc-139">Angive den ekstra rapportdefinition **Saldo for kassekonti** for disse underkategorier.</span><span class="sxs-lookup"><span data-stu-id="f5efc-139">Specify the additional report definition **Cash Accounts** for these subcategories.</span></span>  
3. <span data-ttu-id="f5efc-140">Indrykke dem under underkategorien **Kassebeholdning**.</span><span class="sxs-lookup"><span data-stu-id="f5efc-140">Indent them under the **Cash** subcategory.</span></span>  

<span data-ttu-id="f5efc-141">Næste gang du genererer kontoskemaer viser din kontoopgørelse den samlede saldo for kontant og to linjer med saldi for kontantbeholdning og checkkontoen.</span><span class="sxs-lookup"><span data-stu-id="f5efc-141">The next time you generate account schedules your balance statement will show a total balance for cash and two lines with balances for petty cash and the checking account.</span></span>  

## <a name="see-also"></a><span data-ttu-id="f5efc-142">Se også</span><span class="sxs-lookup"><span data-stu-id="f5efc-142">See Also</span></span>
[<span data-ttu-id="f5efc-143">Finans</span><span class="sxs-lookup"><span data-stu-id="f5efc-143">Finance</span></span>](finance.md)  
[<span data-ttu-id="f5efc-144">Konfigurere eller ændre kontoplanen</span><span class="sxs-lookup"><span data-stu-id="f5efc-144">Setting Up or Changing the Chart of Accounts</span></span>](finance-setup-chart-accounts.md)  
[<span data-ttu-id="f5efc-145">Business Intelligence</span><span class="sxs-lookup"><span data-stu-id="f5efc-145">Business Intelligence</span></span>](bi.md)  
