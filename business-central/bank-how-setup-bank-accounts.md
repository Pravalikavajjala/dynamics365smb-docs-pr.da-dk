---
title: Oprette bankkonti | Microsoft Docs
description: Du kan afstemme bankkonti i Financials med kontoudtog fra banken.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Yodlee, feed, stream
ms.date: 09/26/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7c626c96e3dc4d445a463a050af5c6663cb4ade1
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-bank-accounts"></a><span data-ttu-id="ca328-103">Sådan oprettes bankkonti</span><span class="sxs-lookup"><span data-stu-id="ca328-103">Set Up Bank Accounts</span></span>
<span data-ttu-id="ca328-104">Brug bankkonti i [!INCLUDE[d365fin](includes/d365fin_md.md)] til at holde styr på dine banktransaktioner.</span><span class="sxs-lookup"><span data-stu-id="ca328-104">You use bank accounts in the [!INCLUDE[d365fin](includes/d365fin_md.md)] to keep track of your banking transactions.</span></span> <span data-ttu-id="ca328-105">Konti kan være i den lokale valuta eller i fremmed valuta.</span><span class="sxs-lookup"><span data-stu-id="ca328-105">Accounts can be denominated in your local currency or in a foreign currency.</span></span> <span data-ttu-id="ca328-106">Når du har oprettet bankkonti, kan du også bruge funktionen til kontrol af udskrevne check.</span><span class="sxs-lookup"><span data-stu-id="ca328-106">After you have set up bank accounts, you can also use the check printing option.</span></span>

## <a name="to-set-up-bank-accounts"></a><span data-ttu-id="ca328-107">Sådan oprettes bankkonti</span><span class="sxs-lookup"><span data-stu-id="ca328-107">To set up bank accounts</span></span>
1. <span data-ttu-id="ca328-108">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bankkonti**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ca328-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="ca328-109">I vinduet **Bankkonti** skal du vælge handlingen **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ca328-109">In the **Bank Accounts** window, choose the **New** action.</span></span>
3. <span data-ttu-id="ca328-110">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="ca328-110">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> <span data-ttu-id="ca328-111">For at udfylde feltet **Saldo** med en startsaldo, skal du bogføre en bankkontopost med det pågældende beløb.</span><span class="sxs-lookup"><span data-stu-id="ca328-111">To fill in the **Balance** field with an opening balance, you must post a bank account ledger entry with the amount in question.</span></span> <span data-ttu-id="ca328-112">Du kan gøre dette ved at udføre en afstemning af bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="ca328-112">You can do this by performing a bank account reconciliation.</span></span> <span data-ttu-id="ca328-113">Du kan finde flere oplysninger i [Afstemme bankkonti separat](bank-how-reconcile-bank-accounts-separately.md).</span><span class="sxs-lookup"><span data-stu-id="ca328-113">For more information, see [Reconcile Bank Accounts Separately](bank-how-reconcile-bank-accounts-separately.md).</span></span> <span data-ttu-id="ca328-114">Du kan også implementere primosaldoen som en del af oprettelse af generelle oplysninger i nye virksomheder ved hjælp af den assisterede opsætning **Overflyt virksomhedsdata** .</span><span class="sxs-lookup"><span data-stu-id="ca328-114">Alternatively, you can implement the opening balance as a part of general data creation in new companies by using the **Migrate Business Data** assisted setup.</span></span> <span data-ttu-id="ca328-115">Du kan finde flere oplysninger under [Velkommen til [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md).</span><span class="sxs-lookup"><span data-stu-id="ca328-115">For more information, see [Welcome to [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md).</span></span>

## <a name="to-set-up-your-bank-account-for-import-or-export-of-bank-files"></a><span data-ttu-id="ca328-116">Sådan oprettes bankkontoen for import eller eksport af bankfiler</span><span class="sxs-lookup"><span data-stu-id="ca328-116">To set up your bank account for import or export of bank files</span></span>
<span data-ttu-id="ca328-117">Felter i oversigtspanelet **Overførsel** i vinduet **Bankkontokort** er relateret til indlæsning og udlæsning af bankfeeds og -filer.</span><span class="sxs-lookup"><span data-stu-id="ca328-117">Fields on the **Transfer** FastTab in the **Bank Account Card** window are related to import and export of bank feeds and files.</span></span> <span data-ttu-id="ca328-118">Du kan finde flere oplysninger i [Konfigurere tjenesten til konvertering af bankdata](bank-how-setup-bank-data-conversion-service.md) og [Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="ca328-118">For more information, see [Set Up the Bank Data Conversion Service](bank-how-setup-bank-data-conversion-service.md) and [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

1. <span data-ttu-id="ca328-119">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bankkonti**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ca328-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="ca328-120">Åbn kortet for en bankkonto, du vil eksportere eller importere bankfiler for.</span><span class="sxs-lookup"><span data-stu-id="ca328-120">Open the card for a bank account that you will export or import bank files for.</span></span>
3. <span data-ttu-id="ca328-121">Udfyld felterne efter behov i oversigtspanelet **Overførsel**.</span><span class="sxs-lookup"><span data-stu-id="ca328-121">On the **Transfer** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
>   <span data-ttu-id="ca328-122">Andre fileksporttjenester og deres formater kræver andre konfigurationsværdier i vinduet **Bankkontokort**.</span><span class="sxs-lookup"><span data-stu-id="ca328-122">Different file export services and their formats require different setup values in the **Bank Account Card** window.</span></span> <span data-ttu-id="ca328-123">Du får information om forkerte eller manglende konfigurationsværdier, når du prøver at eksportere filen.</span><span class="sxs-lookup"><span data-stu-id="ca328-123">You will be informed about wrong or missing setup values as you try to export the file.</span></span> <span data-ttu-id="ca328-124">Så læs omhyggeligt korte beskrivelser af felterne, eller se de relaterede emner med fremgangsmåder.</span><span class="sxs-lookup"><span data-stu-id="ca328-124">So read the short descriptions of the fields carefully or refer to the related procedure topics.</span></span> <span data-ttu-id="ca328-125">Eksport af en betalingsfil med f.eks. nordamerikansk elektronisk pengeoverførsel (EFT) kræver, at både **Sidste remitteringsadvisnr.** og **Transitnr.** er udfyldt.</span><span class="sxs-lookup"><span data-stu-id="ca328-125">For example, exporting a payment file for North American electronic funds transfer (EFT) requires that both the **Last Remittance Advice No.** field and the **Transit No.** field are filled in.</span></span> <span data-ttu-id="ca328-126">Du kan finde flere oplysninger i [Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="ca328-126">For more information, see [Export Payments to a Bank File](payables-how-export-payments-bank-file.md).</span></span>

## <a name="to-set-up-vendor-bank-accounts-for-export-of-bank-files"></a><span data-ttu-id="ca328-127">Sådan konfigureres kreditorbankkonti til eksport af bankfiler</span><span class="sxs-lookup"><span data-stu-id="ca328-127">To set up vendor bank accounts for export of bank files</span></span>
<span data-ttu-id="ca328-128">Felter i oversigtspanelet **Overførsel** i vinduet **Kreditors bankkontokort** er relateret til udlæsning af bankfeeds og -filer.</span><span class="sxs-lookup"><span data-stu-id="ca328-128">Fields on the **Transfer** FastTab in the **Vendor Bank Account Card** window are related to export of bank feeds and files.</span></span> <span data-ttu-id="ca328-129">Du kan finde flere oplysninger i [Konfigurere tjenesten til konvertering af bankdata](bank-how-setup-bank-data-conversion-service.md) og [Eksportere betalinger til en bankfil](payables-how-export-payments-bank-file.md).</span><span class="sxs-lookup"><span data-stu-id="ca328-129">For more information, see [Set Up the Bank Data Conversion Service](bank-how-setup-bank-data-conversion-service.md) and [Export Payments to a Bank File](payables-how-export-payments-bank-file.md).</span></span>

1. <span data-ttu-id="ca328-130">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bankkonti**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="ca328-130">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.</span></span>
2. <span data-ttu-id="ca328-131">Åbn kortet for en kreditor, hvis bankkonto du vil eksportere betalingsbankfiler til.</span><span class="sxs-lookup"><span data-stu-id="ca328-131">Open the card for a vendor whose bank account you will export payment bank files to.</span></span>
3. <span data-ttu-id="ca328-132">Vælg handlingen **Bankkonti**.</span><span class="sxs-lookup"><span data-stu-id="ca328-132">Choose the **Bank Accounts** action.</span></span>
3. <span data-ttu-id="ca328-133">Udfyld felterne efter behov i vinduet **Kreditors bankkontokort** i oversigtspanelet **Overførsel**.</span><span class="sxs-lookup"><span data-stu-id="ca328-133">In the **Vendor Bank Account Card** window, on the **Transfer** FastTab, fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="ca328-134">Se også</span><span class="sxs-lookup"><span data-stu-id="ca328-134">See Also</span></span>
[<span data-ttu-id="ca328-135">Konfigurere banktransaktioner</span><span class="sxs-lookup"><span data-stu-id="ca328-135">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="ca328-136">Håndtere bankkonti</span><span class="sxs-lookup"><span data-stu-id="ca328-136">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
<span data-ttu-id="ca328-137">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ca328-137">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
