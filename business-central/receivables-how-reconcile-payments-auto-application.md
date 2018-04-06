---
title: Bruge automatisk udligning til at afstemme betalinger | Microsoft Docs
description: "Beskriver, hvordan du bruger den automatiske udligningsfunktion til at udligne betalinger eller indbetalinger til de relaterede åbne poster og afstemme betalinger."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 75b030e6fc1a2cc5cf3c1068337dfd8c1c905543
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="reconcile-payments-using-automatic-application"></a><span data-ttu-id="d282b-103">Afstemme betalinger ved hjælp af automatisk udligning</span><span class="sxs-lookup"><span data-stu-id="d282b-103">Reconcile Payments Using Automatic Application</span></span>
<span data-ttu-id="d282b-104">Vinduet **Betalingsudligningskladde** angiver betalinger, enten indgående eller udgående, der er registreret som transaktioner på din onlinebankkonto, og som du kan udligne på deres relaterede åbne debitor-, kreditor- og bankkontoposter.</span><span class="sxs-lookup"><span data-stu-id="d282b-104">The **Payment Reconciliation Journal** window specifies payments, either incoming or outgoing, that have been recorded as transactions on your online bank account and that you can apply to their related open customer, vendor, and bank account ledger entries.</span></span> <span data-ttu-id="d282b-105">Linjerne i kladden udfyldes ved at importere et bankkontoudtog som et bankfeed eller en fil.</span><span class="sxs-lookup"><span data-stu-id="d282b-105">The lines in the journal are filled by importing a bank statement as a bank feed or file.</span></span>

<span data-ttu-id="d282b-106">En betalingsudligningskladde er relateret til en bankkonto i [!INCLUDE[d365fin](includes/d365fin_md.md)], der afspejler den onlinebankkonto, hvor betalingstransaktionerne registreres.</span><span class="sxs-lookup"><span data-stu-id="d282b-106">A payment reconciliation journal is related to one bank account in [!INCLUDE[d365fin](includes/d365fin_md.md)] that reflects the online bank account where the payment transactions are recorded.</span></span> <span data-ttu-id="d282b-107">Eventuelle åbne bankposter vedrørende de udlignede debitor- eller kreditorposter bliver lukket, når du vælger handlingen **Bogfør betalinger og afstem bankkonti**.</span><span class="sxs-lookup"><span data-stu-id="d282b-107">Any open bank account ledger entries related to the applied customer or vendor ledger entries will be closed when you choose the **Post Payments and Reconcile Bank Account** action.</span></span> <span data-ttu-id="d282b-108">Det betyder, at bankkontoen automatisk afstemmes for de betalinger, du bogfører, med kladden.</span><span class="sxs-lookup"><span data-stu-id="d282b-108">This means that the bank account is automatically reconciled for payments that you post with the journal.</span></span>

<span data-ttu-id="d282b-109">Hvis du vil indlæse bankkontoudtog, som banken sender som feeds, skal du først aktivere tjenesten Envestnet Yodlee Bank Feeds og derefter knytter bankkontoen til den relaterede onlinebankkonto.</span><span class="sxs-lookup"><span data-stu-id="d282b-109">If you want to import bank statements as bank feeds, you must first enable the Envestnet Yodlee Bank Feeds service and then link the bank account to its related online bank account.</span></span> <span data-ttu-id="d282b-110">Betalingsudligningskladden registrerer derefter automatisk bankfeeds, når du klikker på handlingen **Importér banktransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="d282b-110">The payment reconciliation journal will then automatically detect bank feeds when you choose the **Import Bank Transactions** action.</span></span> <span data-ttu-id="d282b-111">Du kan desuden konfigurere en bankkonto til automatisk at indlæse nye feeds til bankkontoudtog hver time.</span><span class="sxs-lookup"><span data-stu-id="d282b-111">In addition, you can set a bank account up to automatically import new bank statement feeds every hour.</span></span> <span data-ttu-id="d282b-112">Transaktioner for betalinger, der allerede er bogført som udlignet og/eller afstemt indlæses ikke.</span><span class="sxs-lookup"><span data-stu-id="d282b-112">Transactions for payments that have already been posted as applied and/or reconciled will not be imported.</span></span> <span data-ttu-id="d282b-113">Du kan finde flere oplysninger under [Konfigurere tjenesten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="d282b-113">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

<span data-ttu-id="d282b-114">Med handlingen **Knyt tekst til konto** kan du oprette tilknytninger mellem tekst på betalinger og specifikke debet-, kredit- og modkonti, så disse betalinger bliver bogført på de angivne konti, når du bogfører kladden til betalingsafstemning.</span><span class="sxs-lookup"><span data-stu-id="d282b-114">With the **Map Text to Account** action, you can set up mappings between text on payments and specific debit, credit, and balancing accounts so that such payments are posted to the specified accounts when you post the payment reconciliation journal.</span></span> <span data-ttu-id="d282b-115">Se trin 8.</span><span class="sxs-lookup"><span data-stu-id="d282b-115">See step 8.</span></span> <span data-ttu-id="d282b-116">Du kan finde flere oplysninger under [Knytte tekst på tilbagevendende betalinger til automatisk afstemning af konti](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)</span><span class="sxs-lookup"><span data-stu-id="d282b-116">For more information, see [Map Text on Recurring Payments to Accounts for Automatic Reconciliation](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).</span></span>

<span data-ttu-id="d282b-117">Der findes lignende funktioner til afstemning af overskydende beløb på betalingsudligningskladdelinjer på ad hoc-basis.</span><span class="sxs-lookup"><span data-stu-id="d282b-117">Similar functionality exists to reconcile excess amounts on payment reconciliation journal lines on an ad-hoc basis.</span></span> <span data-ttu-id="d282b-118">Du kan finde flere oplysninger i [Afstemme betalinger, der ikke kan udlignes automatisk.](receivables-how-reconcile-payments-cannot-apply-auto.md)</span><span class="sxs-lookup"><span data-stu-id="d282b-118">For more information, see [Reconcile Payments That Cannot be Applied.](receivables-how-reconcile-payments-cannot-apply-auto.md)</span></span>

<span data-ttu-id="d282b-119">Du kan bruge funktionen **Udlign automatisk** enten automatisk, når du importerer en bankfil eller -feed med betalingstransaktioner, eller når du aktiverer den for at udligne betalinger til deres relaterede åbne poster, der er baseret på en afstemning af data på en kladdelinje med data på en eller flere åbne poster.</span><span class="sxs-lookup"><span data-stu-id="d282b-119">You use the **Apply Automatically** function, either automatically when you import a bank file or feed with payment transactions or when you activate it, to apply payments to their related open entries based on a matching of data on a journal line with data on one or more open entries.</span></span>

<span data-ttu-id="d282b-120">På kladdelinjer, hvor betaling er udlignet automatisk til en eller flere åbne poster, har feltet **Matchtillid** en værdi mellem Lav og Høj for at angive kvaliteten af den dataafstemning, som den foreslåede betalingsudligning er baseret på.</span><span class="sxs-lookup"><span data-stu-id="d282b-120">On journal lines where a payment has been applied automatically to one or more open entries, the **Match Confidence** field has a value between Low and High to indicate the quality of the data matching that the suggested payment application is based on.</span></span> <span data-ttu-id="d282b-121">Derudover bliver felterne **Kontotype** og **Kontonr.** udfyldt med oplysninger om debitoren eller kreditoren, som betalingen udlignes for.</span><span class="sxs-lookup"><span data-stu-id="d282b-121">In addition, the **Account Type** and **Account No.** fields are filled with information about the customer or vendor that the payment is applied to.</span></span> <span data-ttu-id="d282b-122">Hvis du har oprettet en tekst-til-kontotilknytning, kan automatisk udligning resultere i værdien **Høj – tekst-til-kontotilknytning** som udligningstillid.</span><span class="sxs-lookup"><span data-stu-id="d282b-122">If you have set up a text-to-account mapping, the automatic application can result in a match confidence value of **High - Text-to-Account Mapping**.</span></span>

<span data-ttu-id="d282b-123">For hver kladdelinje i vinduet **Betalingsudligningskladde** kan du åbne vinduet **Betalingsudligning** for at få vist alle åbne kandidatposter for betalingen og se detaljerede oplysninger for hver post om den dataafstemning, som en betalingsudligning er baseret på.</span><span class="sxs-lookup"><span data-stu-id="d282b-123">For each journal line in the **Payment Reconciliation Journal** window, you can open the **Payment Application** window to see all candidate open entries for the payment and view detailed information for each entry about the data matching that a payment application is based on.</span></span> <span data-ttu-id="d282b-124">Her kan du manuelt udligne betalinger eller udligne betalinger igen, der er udlignet automatisk til en forkert post.</span><span class="sxs-lookup"><span data-stu-id="d282b-124">Here, you can manually apply payments or reapply payments that were applied automatically to a wrong entry.</span></span> <span data-ttu-id="d282b-125">Du kan finde flere oplysninger i [Gennemse eller udligne betalinger efter automatisk udligning](receivables-how-review-apply-payments-auto-application.md).</span><span class="sxs-lookup"><span data-stu-id="d282b-125">For more information, see [Review or Apply Payments After Automatic Application](receivables-how-review-apply-payments-auto-application.md).</span></span>

> [!NOTE]  
>   <span data-ttu-id="d282b-126">Du kan starte importen af banktransaktioner på samme tid, som du åbner vinduet **Betalingsudligningskladde** for en eksisterende betalingsafstemningskladde i vinduet **Betalingsafstemningskladder**.</span><span class="sxs-lookup"><span data-stu-id="d282b-126">You can start the bank transactions import at the same time as you open the **Payment Reconciliation** Journal window for an existing payment reconciliation journal in the **Payment Reconciliation Journals** window.</span></span> <span data-ttu-id="d282b-127">Følgende procedure beskriver, hvordan du importerer banktransaktioner i vinduet **Betalingsudligningskladde**, når du har oprettet en ny kladde.</span><span class="sxs-lookup"><span data-stu-id="d282b-127">The following procedure describes how to import bank transactions into the **Payment Reconciliation Journal** window after you have created a new journal.</span></span>

## <a name="to-reconcile-payments-using-automatic-application"></a><span data-ttu-id="d282b-128">Sådan afstemmer du betalinger ved hjælp af automatisk udligning</span><span class="sxs-lookup"><span data-stu-id="d282b-128">To reconcile payments using automatic application</span></span>
1. <span data-ttu-id="d282b-129">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Betalingsudbetalingskladder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d282b-129">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Reconciliation Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="d282b-130">Hvis du vil arbejde i en ny betalingsafstemningskladde, skal du vælge handlingen **Ny kladde**.</span><span class="sxs-lookup"><span data-stu-id="d282b-130">To work in a new payment reconciliation journal, choose the **New Journal** action.</span></span>
3. <span data-ttu-id="d282b-131">Brug vinduet **Betalingsbankkontooversigt** til at vælge den bankkonto, som du vil afstemme betalinger for, og vælg derefter knappen **OK**.</span><span class="sxs-lookup"><span data-stu-id="d282b-131">In the **Payment Bank Account List** window, select the bank account that you want to reconcile payments for, and then choose the **OK** button.</span></span>
   <span data-ttu-id="d282b-132">Vinduet **Betalingsudligningskladde** åbnes forberedt til den valgte bankkonto.</span><span class="sxs-lookup"><span data-stu-id="d282b-132">The **Payment Reconciliation Journal** window opens prepared for the selected bank account.</span></span>
4. <span data-ttu-id="d282b-133">Vælg handlingen **Importer banktransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="d282b-133">Choose the **Import Bank Transactions** action.</span></span>
   <span data-ttu-id="d282b-134">Hvis bankkontoen for den valgte kladde ikke er angivet for import af banktransaktioner, åbnes en dialogboks for at hjælpe dig med at udfylde de relevante felter.</span><span class="sxs-lookup"><span data-stu-id="d282b-134">If the bank account for the selected journal is not set up for import of bank transactions, then a dialog box will open to help you fill in the relevant fields.</span></span>
5. <span data-ttu-id="d282b-135">Brug vinduet **Vælg den fil, der skal importeres** til at vælge den fil, der indeholder banktransaktioner for betalinger, der skal afstemmes, og vælg derefter knappen **Åbn**.</span><span class="sxs-lookup"><span data-stu-id="d282b-135">In the **Select a file to import** window, select the file that contains the bank transactions for payments that you want to reconcile, and then choose the **Open** button.</span></span>  
6. <span data-ttu-id="d282b-136">Hvis tjenesten Bankkontoudtog er aktiveret, skal du i vinduet **Bankkontoudtogsfilter**, der åbnes automatisk, angive datointervallet for bankkontoudtog, der skal importeres.</span><span class="sxs-lookup"><span data-stu-id="d282b-136">If the Bank Statement service is enabled, in the **Bank Statement Filter** window that opens automatically, specify the date interval for the bank statements to be imported.</span></span>

    <span data-ttu-id="d282b-137">Vinduet **Betalingsudligningskladde** er fyldt med linjer for betalinger, der repræsenterer banktransaktioner i det importerede bankkontoudtog.</span><span class="sxs-lookup"><span data-stu-id="d282b-137">The **Payment Reconciliation Journal** window is filled with lines for payments representing bank transactions in the imported bank statement.</span></span>

    <span data-ttu-id="d282b-138">På linjer, hvor betaling er udlignet automatisk til den relaterede åbne post, har feltet **Matchtillid** en værdi mellem **Lav** og **Høj** for at angive kvaliteten af den dataafstemning, som den foreslåede betalingsudligning er baseret på.</span><span class="sxs-lookup"><span data-stu-id="d282b-138">On lines for payments that have been automatically applied to their related open entries, the **Match Confidence** field has a value between **Low** and **High** to indicate the quality of the data matching that the suggested payment application is based on.</span></span> <span data-ttu-id="d282b-139">Derudover bliver felterne **Kontotype** og **Kontonr.** udfyldt med oplysninger om debitoren eller kreditoren, som betalingen udlignes for.</span><span class="sxs-lookup"><span data-stu-id="d282b-139">In addition, the **Account Type** and **Account No.** fields are filled with information about the customer or vendor that the payment is applied to.</span></span>
7. <span data-ttu-id="d282b-140">Vælg en kladdelinje, og vælg derefter den **Udlign manuelt**-handling, der skal gennemgås, eller udlign betalingen manuelt i vinduet **Betalingsudligning**.</span><span class="sxs-lookup"><span data-stu-id="d282b-140">Select a journal line, and then, choose the **Apply Manually** action to review, reapply, or apply the payment manually in the **Payment Application** window.</span></span> <span data-ttu-id="d282b-141">Du kan finde flere oplysninger i [Gennemse eller udligne betalinger efter automatisk udligning](receivables-how-review-apply-payments-auto-application.md).</span><span class="sxs-lookup"><span data-stu-id="d282b-141">For more information, see [Review or Apply Payments After Automatic Application](receivables-how-review-apply-payments-auto-application.md).</span></span>

    <span data-ttu-id="d282b-142">Når du er færdig med manuel udligning, indeholder feltet **Matchtillid** på den kladdelinje, du har behandlet manuelt, **Accepteret**.</span><span class="sxs-lookup"><span data-stu-id="d282b-142">When you have finished your manual application, the **Match Confidence** field on the journal line that you have processed manually contains **Accepted**.</span></span>
8. <span data-ttu-id="d282b-143">Vælg en ikke-udlignet kladdelinje for en tilbagevendende indbetaling eller en udgift, f.eks køb af benzin, og vælg derefter handlingen **Knyt tekst til konto**.</span><span class="sxs-lookup"><span data-stu-id="d282b-143">Select an unapplied journal line for a recurring cash receipt or expense, such as a car gasoline purchase, and then choose the **Map Text to Account** action.</span></span> <span data-ttu-id="d282b-144">Du kan finde flere oplysninger under [Knytte tekst på tilbagevendende betalinger til automatisk afstemning af konti](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)</span><span class="sxs-lookup"><span data-stu-id="d282b-144">For more information, see [Map Text on Recurring Payments to Accounts for Automatic Reconciliation](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md)</span></span>
9. <span data-ttu-id="d282b-145">Når du er færdig med at knytte betalingstekst til konti, skal du vælge handlingen **Udlign manuelt**.</span><span class="sxs-lookup"><span data-stu-id="d282b-145">When you have finished your mapping of payment text to accounts, choose the **Apply Manually** action.</span></span>
10. <span data-ttu-id="d282b-146">Når du er sikker på, at alle betalinger på kladdelinjerne er korrekt udlignet eller indstillet til direkte bogføring, skal du vælge handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="d282b-146">When you are content that all payments on the journal lines are correctly applied or set to direct posting, choose the **Post** action.</span></span>

<span data-ttu-id="d282b-147">Når du bogfører betalingsafstemningskladden, bliver de udlignede åbne poster lukket, og de relaterede debitor-, kreditor- eller finanskonti opdateres.</span><span class="sxs-lookup"><span data-stu-id="d282b-147">When you post the payment reconciliation journal, the applied open entries memos are closed, and the related customer, vendor, or general ledger accounts are updated.</span></span> <span data-ttu-id="d282b-148">De angivne debitor-, kreditor- og finanskonti opdateres for betalinger på kladdelinjer, der er baseret på tekst-til-kontotilknytning.</span><span class="sxs-lookup"><span data-stu-id="d282b-148">For payments on journal lines based on text-to-account mapping, the specified customer, vendor, and general ledger accounts are updated.</span></span> <span data-ttu-id="d282b-149">For alle kladdelinjer oprettes bankposter.</span><span class="sxs-lookup"><span data-stu-id="d282b-149">For all journal lines, bank account ledger entries are created.</span></span> <span data-ttu-id="d282b-150">Hvis du vælger handlingen **Bogfør betalinger og afstem bankkonti**, bliver eventuelle åbne bankposter vedrører de udlignede debitor- eller kreditorposter lukket.</span><span class="sxs-lookup"><span data-stu-id="d282b-150">If you choose the **Post Payments and Reconcile Bank Account** action, any open bank account ledger entries related to the applied customer or vendor ledger entries will be closed.</span></span> <span data-ttu-id="d282b-151">Det betyder, at bankkontoen automatisk afstemmes for de betalinger, du bogfører, med kladden.</span><span class="sxs-lookup"><span data-stu-id="d282b-151">This means that the bank account is automatically reconciled for payments that you post with the journal.</span></span>

<span data-ttu-id="d282b-152">Du kan sammenligne værdien i feltet **Saldo på bankkonto efter bogføring** med værdien i feltet **Kontoudtogs slutsaldo** for at spore, hvornår bankkontoen er afstemt baseret på betalinger, du bogfører.</span><span class="sxs-lookup"><span data-stu-id="d282b-152">You can compare the value in the **Balance on Bank Account After Posting** field together with the value in the **Statement Ending Balance** field to track when the bank account is reconciled based on payments that you post.</span></span>

> [!NOTE]  
>   <span data-ttu-id="d282b-153">Hvis du ikke vil afstemme bankkontoen fra vinduet **Betalingsudligningskladde**, skal du bruge vinduet **Bankkontoafstemning**.</span><span class="sxs-lookup"><span data-stu-id="d282b-153">If you do not want to reconcile the bank account from the **Payment Reconciliation Journal** window, then you must use the **Bank Acc. Reconciliation** window.</span></span> <span data-ttu-id="d282b-154">Du kan finde flere oplysninger i [Afstemme bankkonti separat](bank-how-reconcile-bank-accounts-separately.md).</span><span class="sxs-lookup"><span data-stu-id="d282b-154">For more information, see [Reconcile Bank Accounts Separately](bank-how-reconcile-bank-accounts-separately.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d282b-155">Se også</span><span class="sxs-lookup"><span data-stu-id="d282b-155">See Also</span></span>
[<span data-ttu-id="d282b-156">Administrere tilgodehavender</span><span class="sxs-lookup"><span data-stu-id="d282b-156">Managing Receivables</span></span>](receivables-manage-receivables.md)  
[<span data-ttu-id="d282b-157">Salg</span><span class="sxs-lookup"><span data-stu-id="d282b-157">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="d282b-158">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d282b-158">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
