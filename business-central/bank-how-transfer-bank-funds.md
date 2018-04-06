---
title: "Overføre bankbeløb | Microsoft Docs"
description: "Du kan overføre beløb fra én bankkonto til en anden, herunder forskellige valutaer, ved at bogføre transaktionen i finanskladden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account transfer, multiple currencies
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 54e8a7bf7ca8761d6317b57d45e64f9ee628f4b8
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="transfer-bank-funds"></a><span data-ttu-id="14bf3-103">Overføre bankbeløb</span><span class="sxs-lookup"><span data-stu-id="14bf3-103">Transfer Bank Funds</span></span>
<span data-ttu-id="14bf3-104">Undertiden kan du have brug for at overføre et beløb fra én bankkonto til en anden.</span><span class="sxs-lookup"><span data-stu-id="14bf3-104">You may sometimes need to transfer an amount from one bank account to another.</span></span> <span data-ttu-id="14bf3-105">Hvis du vil gøre dette, skal du bogføre på en transaktion i finanskladden.</span><span class="sxs-lookup"><span data-stu-id="14bf3-105">To do this, you must post the a transaction in the general journal.</span></span> <span data-ttu-id="14bf3-106">Opgaven afhænger af, om bankkontiene bruger samme valuta eller forskellige valutaer.</span><span class="sxs-lookup"><span data-stu-id="14bf3-106">The task varies depending on whether the bank accounts use the same currency or different currencies.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-the-same-currency-code"></a><span data-ttu-id="14bf3-107">Sådan bogføres overførsler mellem bankkonti med samme valutakode</span><span class="sxs-lookup"><span data-stu-id="14bf3-107">To post a transfer between bank accounts with the same currency code</span></span>
1. <span data-ttu-id="14bf3-108">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Finanskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="14bf3-108">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="14bf3-109">Udfyld **Bogføringsdato** og **Bilagsnr.** på en kladdelinje.</span><span class="sxs-lookup"><span data-stu-id="14bf3-109">On a journal line, fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="14bf3-110">Klik på feltet **Kontotype**, og vælg **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="14bf3-110">In the **Account Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="14bf3-111">I feltet **Kontonr.** skal du vælge den bank, hvorfra du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="14bf3-111">In the **Account No.** field, select the bank from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="14bf3-112">Angiv det beløb, der skal overføres, i feltet **Beløb**.</span><span class="sxs-lookup"><span data-stu-id="14bf3-112">In the **Amount** field, enter the amount to be transferred.</span></span>
6. <span data-ttu-id="14bf3-113">I feltet **Modkontotype** skal du vælge **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="14bf3-113">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="14bf3-114">I feltet **Modkontonr.** skal du vælge den bankkonto, hvortil du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="14bf3-114">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="14bf3-115">Bogfør journalen.</span><span class="sxs-lookup"><span data-stu-id="14bf3-115">Post the journal.</span></span>

## <a name="to-post-a-transfer-between-bank-accounts-with-different-currency-codes"></a><span data-ttu-id="14bf3-116">Sådan bogføres overførsler mellem bankkonti med forskellige valutakoder</span><span class="sxs-lookup"><span data-stu-id="14bf3-116">To post a transfer between bank accounts with different currency codes</span></span>
<span data-ttu-id="14bf3-117">Hvis du vil overføre beløb mellem bankkonti, der bruger forskellige valutaer, skal du bogføre to finanskladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="14bf3-117">To transfer funds between bank accounts that use different currencies, you must post two general journal lines.</span></span>

1. <span data-ttu-id="14bf3-118">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Finanskladde**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="14bf3-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journal**, and then choose the related link.</span></span>
2. <span data-ttu-id="14bf3-119">Opret to kladdelinjer, og udfyld felterne **Bogføringsdato** og **Bilagsnr.**</span><span class="sxs-lookup"><span data-stu-id="14bf3-119">Create two journal lines, and fill in the **Posting Date** and **Document No.** fields.</span></span>
3. <span data-ttu-id="14bf3-120">På den første kladdelinje skal du vælge **Bankkonto** i feltet **Type**.</span><span class="sxs-lookup"><span data-stu-id="14bf3-120">On the first journal line, in the **Type** field, select **Bank Account**.</span></span>
4. <span data-ttu-id="14bf3-121">I feltet **Kontonr.** skal du vælge den bankkonto, hvorfra du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="14bf3-121">In the **Account No.** field, select the bank account from which you want to transfer the funds.</span></span>
5. <span data-ttu-id="14bf3-122">I feltet **Beløb** skal du indtaste beløbet i valutaen for bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="14bf3-122">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="14bf3-123">Angiv kreditbeløb med et minus-tegn.</span><span class="sxs-lookup"><span data-stu-id="14bf3-123">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="14bf3-124">Angiv debetbeløb uden et minus-tegn.</span><span class="sxs-lookup"><span data-stu-id="14bf3-124">Enter debit amounts without a minus sign.</span></span>
6. <span data-ttu-id="14bf3-125">I feltet **Modkontotype** skal du vælge **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="14bf3-125">In the **Bal. Account Type** field, select **Bank Account**.</span></span>
7. <span data-ttu-id="14bf3-126">I feltet **Modkontonr.** skal du vælge den bankkonto, hvortil du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="14bf3-126">In the **Bal. Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
8. <span data-ttu-id="14bf3-127">På den anden kladdelinje skal du vælge **Bankkonto** i feltet **Type**.</span><span class="sxs-lookup"><span data-stu-id="14bf3-127">On the second journal line, in the **Type** field, select **Bank Account**.</span></span>
9. <span data-ttu-id="14bf3-128">I feltet **Kontonr.** skal du vælge den bankkonto, hvortil du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="14bf3-128">In the **Account No.** field, select the bank account to which you want to transfer the funds.</span></span>
10. <span data-ttu-id="14bf3-129">I feltet **Beløb** skal du indtaste beløbet i valutaen for bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="14bf3-129">In the **Amount** field, enter the amount in the currency of the bank account.</span></span> <span data-ttu-id="14bf3-130">Angiv kreditbeløb med et minus-tegn.</span><span class="sxs-lookup"><span data-stu-id="14bf3-130">Enter credit amounts with a minus sign.</span></span> <span data-ttu-id="14bf3-131">Angiv debetbeløb uden et minus-tegn.</span><span class="sxs-lookup"><span data-stu-id="14bf3-131">Enter debit amounts without a minus sign.</span></span>
11. <span data-ttu-id="14bf3-132">I feltet **Modkontotype** skal du vælge **Bankkonto**.</span><span class="sxs-lookup"><span data-stu-id="14bf3-132">In the **Bal. Account Type** field, select **Bank Account**.</span></span>  
12. <span data-ttu-id="14bf3-133">I feltet **Modkontonr.** skal du vælge den bankkonto, hvorfra du vil overføre beløbet.</span><span class="sxs-lookup"><span data-stu-id="14bf3-133">In the **Bal. Account No.** field, select the bank account from which you want to transfer the funds.</span></span>

    > [!NOTE]  
>   <span data-ttu-id="14bf3-134">Hvis den anvendte valutakurs i kladden er en anden en kursen i vinduet **Valutakurser**, skal du oprette en tredje linje til kurstab og -gevinster.</span><span class="sxs-lookup"><span data-stu-id="14bf3-134">If the exchange rates used in the journal are different than the exchange rates in the **Currency Exchange Rates** window, enter a third line for the exchange rate gain or loss.</span></span> <span data-ttu-id="14bf3-135">Indtast **Finanskonto** i feltet **Kontotype**.</span><span class="sxs-lookup"><span data-stu-id="14bf3-135">Enter **G/L Account** in the **Account Type** field.</span></span> <span data-ttu-id="14bf3-136">Angiv finanskontonummeret for kurstab og -gevinster i feltet **Kontonummer**.</span><span class="sxs-lookup"><span data-stu-id="14bf3-136">Enter the G/L account number for exchange rate gain or loss in the **Account No.** field.</span></span> <span data-ttu-id="14bf3-137">Angiv kurstab eller -tab i feltet **Beløb** henholdsvis med og uden et minustegn foran kredit og debet.</span><span class="sxs-lookup"><span data-stu-id="14bf3-137">Enter the exchange rate gain or loss in the **Amount** field with or without a minus sign for credits and debits respectively.</span></span>
13. <span data-ttu-id="14bf3-138">Bogfør journalen.</span><span class="sxs-lookup"><span data-stu-id="14bf3-138">Post the journal.</span></span>

## <a name="see-also"></a><span data-ttu-id="14bf3-139">Se også</span><span class="sxs-lookup"><span data-stu-id="14bf3-139">See Also</span></span>
[<span data-ttu-id="14bf3-140">Håndtere bankkonti</span><span class="sxs-lookup"><span data-stu-id="14bf3-140">Managing Bank Accounts</span></span>](bank-manage-bank-accounts.md)  
[<span data-ttu-id="14bf3-141">Konfigurere banktransaktioner</span><span class="sxs-lookup"><span data-stu-id="14bf3-141">Setting Up Banking</span></span>](bank-setup-banking.md)  
[<span data-ttu-id="14bf3-142">Arbejde med finanskladder</span><span class="sxs-lookup"><span data-stu-id="14bf3-142">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="14bf3-143">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="14bf3-143">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
