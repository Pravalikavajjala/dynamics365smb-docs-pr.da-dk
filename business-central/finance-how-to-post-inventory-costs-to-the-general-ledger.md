---
title: "Sådan bogfører du kostpriser i finansregnskabet | Microsoft Docs"
description: "Bruges til at styre de fysiske produkter, som du handler med, f.eks. håndtering af lagerbeholdning på lagerstedet."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 07/05/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8292864e7b25b0e5f0fb1f6668fb8622efb031e2
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="reconcile-inventory-costs-with-the-general-ledger"></a><span data-ttu-id="a2d80-103">Afstemme lagerværdier med finansregnskabet</span><span class="sxs-lookup"><span data-stu-id="a2d80-103">Reconcile Inventory Costs with the General Ledger</span></span>
<span data-ttu-id="a2d80-104">Når du bogfører lagertransaktioner, f.eks. salgsleverancer, købsfakturaer eller lagerreguleringer, registreres ændringen i varepriser i værdiposterne.</span><span class="sxs-lookup"><span data-stu-id="a2d80-104">When you post inventory transactions, such as sales shipments, purchase invoices, or inventory adjustments, the changed item costs are recorded in item value entries.</span></span> <span data-ttu-id="a2d80-105">For at afspejle ændringen af lagerværdien i dine finansielle regnskaber bogføres lagerværdien automatisk i de relaterede lagerkonti i finansbogholderiet.</span><span class="sxs-lookup"><span data-stu-id="a2d80-105">To reflect this change of inventory value in your financial books, the inventory costs are automatically posted to the related inventory accounts in the general ledger.</span></span> <span data-ttu-id="a2d80-106">For hver lagertransaktion du bogfører, bogføres den relevante værdi på lagerkontoen, reguleringskontoen og vareforbrugskontoen i finansregnskabet.</span><span class="sxs-lookup"><span data-stu-id="a2d80-106">For each inventory transaction that you post, the appropriate values are posted to the inventory account, adjustment account, and COGS account in the general ledger.</span></span>

<span data-ttu-id="a2d80-107">Automatisk lagerværdibogføring er defineret i feltet **Aut. lagerværdibogføring** i vinduet **Lageropsætning**.</span><span class="sxs-lookup"><span data-stu-id="a2d80-107">Automatic cost posting is defined by the **Automatic Cost Posting** field in the **Inventory Setup** window.</span></span>

<span data-ttu-id="a2d80-108">Selvom lagerværdien automatisk bogføres i Finans, er det stadig nødvendigt at sikre, at værdien af varerne overføres til de relaterede udgående transaktioner, f.eks salg eller overflytninger. Dette er især vigtigt i de situationer, hvor du sælger varer, inden du fakturerer købet af varerne.</span><span class="sxs-lookup"><span data-stu-id="a2d80-108">Even though inventory costs are automatically posted to the general ledger, it is still necessary to ensure that the costs of goods are forwarded to the related outbound sales transaction, especially in situations where you sell goods before you invoice the purchase of those goods.</span></span> <span data-ttu-id="a2d80-109">Dette omtales som omkostningsregulering.</span><span class="sxs-lookup"><span data-stu-id="a2d80-109">This is referred to as cost adjustment.</span></span> <span data-ttu-id="a2d80-110">Varepriser reguleres automatisk, når du bogfører transaktioner, men du kan også justere varepriser manuelt.</span><span class="sxs-lookup"><span data-stu-id="a2d80-110">Item costs are automatically adjusted when you post item transactions, but you can also adjust item costs manually.</span></span> <span data-ttu-id="a2d80-111">Du kan finde flere oplysninger i [Regulere varepriser](inventory-how-adjust-item-costs.md).</span><span class="sxs-lookup"><span data-stu-id="a2d80-111">For more information, see [Adjust Item Costs](inventory-how-adjust-item-costs.md).</span></span>

## <a name="to-post-inventory-costs-manually"></a><span data-ttu-id="a2d80-112">Sådan bogføres lagerværdier manuelt</span><span class="sxs-lookup"><span data-stu-id="a2d80-112">To post inventory costs manually</span></span>
1. <span data-ttu-id="a2d80-113">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bogfør lagerregulering**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="a2d80-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") ico, enter **Post Inventory Cost to G/L**, and then choose the related link.</span></span>
2. <span data-ttu-id="a2d80-114">Du kan bogføre lagerværdier i finansregnskabet ved at udføre kørslen.</span><span class="sxs-lookup"><span data-stu-id="a2d80-114">Post inventory costs to the general ledger manually by running the batch job.</span></span> <span data-ttu-id="a2d80-115">Når du udfører denne kørsel, oprettes finansposter ud fra værdiposterne.</span><span class="sxs-lookup"><span data-stu-id="a2d80-115">When you run this batch job, general ledger entries are created on the basis of value entries.</span></span> <span data-ttu-id="a2d80-116">Du kan bogføre posterne, så de opsummeres pr. bogføringsgruppe.</span><span class="sxs-lookup"><span data-stu-id="a2d80-116">You can post the entries so that they are summarized per posting group.</span></span>

> [!NOTE]  
> <span data-ttu-id="a2d80-117">Når du udfører kørslen, kan du finde fejl, der relaterer til manglende opsætning eller inkompatibel opsætning af dimensioner.</span><span class="sxs-lookup"><span data-stu-id="a2d80-117">When you run this batch job, you might encounter errors having to do with missing setup or incompatible dimension setup.</span></span> <span data-ttu-id="a2d80-118">Hvis kørslen finder fejl i opsætningen af dimensioner, bliver disse fejl tilsidesat, og kørslen bruger dimensionerne for værdiposten.</span><span class="sxs-lookup"><span data-stu-id="a2d80-118">If the batch job encounters errors in the dimension setup, it overrides these errors and uses the dimensions of the value entry.</span></span> <span data-ttu-id="a2d80-119">For alle andre typer fejl springer kørslen bogføring af værdiposter over, og anfører dem i slutningen af rapporten under overskriften “Poster, der er sprunget over”.</span><span class="sxs-lookup"><span data-stu-id="a2d80-119">For any other errors, the batch job skips posting the value entries and lists them at the end of the report in a section titled “Skipped Entries.”</span></span> <span data-ttu-id="a2d80-120">Du skal rette fejlene, inden du kan bogføre posterne.</span><span class="sxs-lookup"><span data-stu-id="a2d80-120">To post these entries, you must fix the errors.</span></span>

<span data-ttu-id="a2d80-121">Hvis du vil se en liste over fejl før kørslen af bogføringen, kan du køre rapporten **Bogfør lageromkostning - kontrol**.</span><span class="sxs-lookup"><span data-stu-id="a2d80-121">To see a list of errors before running the posting batch job, you can run the **Post Invt. Cost to G/L - Test** report.</span></span> <span data-ttu-id="a2d80-122">Denne kontrolrapport viser alle de fejl, som fanges under en bogføringstest.</span><span class="sxs-lookup"><span data-stu-id="a2d80-122">The test report lists all the errors encountered during a test posting.</span></span> <span data-ttu-id="a2d80-123">Du kan derefter rette fejlene og udføre kørslen til bogføring af lagerreguleringer uden at springe nogen poster over.</span><span class="sxs-lookup"><span data-stu-id="a2d80-123">You can then fix the errors, and run the inventory cost posting batch job without skipping any entries.</span></span>

<span data-ttu-id="a2d80-124">Hvis du ganske enkelt vil have en oversigt over, hvilke værdier der kan bogføres i finansregnskabet uden at gennemføre bogføringen, kan du udføre kørslen **Bogfør lagerregulering** uden at bogføre værdierne i finansregnskabet.</span><span class="sxs-lookup"><span data-stu-id="a2d80-124">If you would like to simply get an overview of what values could be posted to the general ledger without actually performing the posting, you can run the **Post Inventory Cost to G/L** batch job without actually posting the values to the general ledger.</span></span> <span data-ttu-id="a2d80-125">Dette kan du gøre ved at fjerne markeringen i feltet **Bogfør** på anmodningssiden.</span><span class="sxs-lookup"><span data-stu-id="a2d80-125">You do this by clearing the check mark from the **Post** field on the request page.</span></span> <span data-ttu-id="a2d80-126">Når du derefter udfører kørslen, oprettes der kun en rapport, der viser de værdier, der er klar til at blive bogført i finansregnskabet, men de er ikke bogført.</span><span class="sxs-lookup"><span data-stu-id="a2d80-126">This way, when you run the batch job, the report is produced showing the values that are ready to be posted to the general ledger, but they are not posted.</span></span>

## <a name="to-audit-the-reconciliation-between-the-inventory-ledger-and-the-general-ledger"></a><span data-ttu-id="a2d80-127">Sådan reviderer du afstemningen mellem lagerposterne og finansposterne</span><span class="sxs-lookup"><span data-stu-id="a2d80-127">To audit the reconciliation between the inventory ledger and the general ledger</span></span>
<span data-ttu-id="a2d80-128">Vinduet **Lagerbeholdning - afstemning** indeholder følgende:</span><span class="sxs-lookup"><span data-stu-id="a2d80-128">The **Inventory - G/L Reconciliation** window provides the following:</span></span>

- <span data-ttu-id="a2d80-129">Vise afstemningsdifferencer ved at sammenligne det, der er registreret i finans, og det, der er registreret i lageropgørelsen (værdiposter).</span><span class="sxs-lookup"><span data-stu-id="a2d80-129">Exposes reconciliation differences by comparing what is recorded in G/L and what is recorded in the inventory ledger (value entries).</span></span>
- <span data-ttu-id="a2d80-130">Vise ikke-afstemte kostbeløb i værdiposter i lageropgørelsen, som om de var koblet til tilsvarende lagerrelaterede konti i finans og sammenligne disse med de totaler, der faktisk registreres i de samme konti i finans.</span><span class="sxs-lookup"><span data-stu-id="a2d80-130">Displays unreconciled cost amounts in the value entries in the inventory ledger as if they were mapped to corresponding inventory-related accounts in G/L and compares those to the totals actually recorded in the same accounts in G/L.</span></span>
- <span data-ttu-id="a2d80-131">Afspejle dobbeltindtastningsstrukturen i finans ved visuelt at præsentere data som sådan.</span><span class="sxs-lookup"><span data-stu-id="a2d80-131">Reflects the double entry structure of G/L by visually presenting data as such.</span></span> <span data-ttu-id="a2d80-132">En vareforbrugsindtastning har f.eks. en tilsvarende lagerpost.</span><span class="sxs-lookup"><span data-stu-id="a2d80-132">For example, a COGS entry has a corresponding inventory entry.</span></span>
- <span data-ttu-id="a2d80-133">Lade brugerne specificere og få vist de poster, der udgør kostbeløb.</span><span class="sxs-lookup"><span data-stu-id="a2d80-133">Lets users drill down and see the entries that make up the cost amounts.</span></span>
- <span data-ttu-id="a2d80-134">Inkludere filtre, der begrænser analysen efter dato, vare og lokation.</span><span class="sxs-lookup"><span data-stu-id="a2d80-134">Includes filters to narrow the analysis by date, item, and location.</span></span>
- <span data-ttu-id="a2d80-135">Forklare årsager til afstemningsdifferencer i informative meddelelser.</span><span class="sxs-lookup"><span data-stu-id="a2d80-135">Explains reasons for reconciliation differences in informative messages.</span></span>


<span data-ttu-id="a2d80-136">Kolonnen **Navn** yderst til venstre i gitteret viser de forskellige finanskontotyper, der er tilknyttet lager.</span><span class="sxs-lookup"><span data-stu-id="a2d80-136">The **Name** column on the far left in the grid lists the various G/L account types that are associated with inventory.</span></span>

<span data-ttu-id="a2d80-137">Kolonnerne **Lager**, **Lager (mellemkonto)** og **Igangværende lager** viser de fakturerede og ikke-fakturerede totaler og totaler for igangværende arbejde for hver finanskontotype.</span><span class="sxs-lookup"><span data-stu-id="a2d80-137">The **Inventory**, **Inventory (Interim)**, and **WIP Inventory** columns show the invoiced, non-invoiced, and WIP totals of each G/L account type.</span></span> <span data-ttu-id="a2d80-138">Disse beregnes ud fra værdiposter, dvs. de projiceres over på de finanskontotyper, hvor de skal være, når de til sidste bogføres til finans.</span><span class="sxs-lookup"><span data-stu-id="a2d80-138">These are calculated from value entries, that is, they are projected onto the G/L account types where they will end when they are eventually posted to G/L.</span></span>

<span data-ttu-id="a2d80-139">Kolonnen **Total** viser summen (med fed tekst) af værdipostbeløbene i de tre lagerkolonner.</span><span class="sxs-lookup"><span data-stu-id="a2d80-139">The **Total** column shows the sum (in bold font) of the value entry amounts in the three inventory columns.</span></span>

<span data-ttu-id="a2d80-140">Kolonnen **Finanstotal** viser beløbene (med fed skrift) for hver finanskontotype, der findes i finans.</span><span class="sxs-lookup"><span data-stu-id="a2d80-140">The **G/L Total** column shows the amounts (in bold font) for each G/L account type that exists in G/L.</span></span> <span data-ttu-id="a2d80-141">Disse beregnes ud fra finansposter, dvs. de repræsenterer lagerreguleringer, der allerede er bogført til finans.</span><span class="sxs-lookup"><span data-stu-id="a2d80-141">These are calculated from G/L entries, that is, they represent inventory costs already posted to G/L.</span></span>

<span data-ttu-id="a2d80-142">Kolonnen **Difference** repræsenterer forskellen mellem værdien i feltet **Finanstotal** og **Total**.</span><span class="sxs-lookup"><span data-stu-id="a2d80-142">The **Difference** column represents the difference between the value in the **G/L Total** and **Total** fields.</span></span>

<span data-ttu-id="a2d80-143">Øverst i vinduet **Lagerbeholdning - afstemning** kan du angive filtre for at begrænse, hvilke oplysninger der skal vises, f.eks. inden for en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="a2d80-143">In the top of the **Inventory - G/L Reconciliation** window, you can enter filters to limit, for example, the period of time for which you want information.</span></span>

<span data-ttu-id="a2d80-144">Hvis du vælger afkrydsningsfeltet **Vis advarsel**, og hvis der er uoverensstemmelser mellem lagertotaler og finanstotaler, vises meddelelser i feltet **Advarsel** for gitteret, som beskriver uoverensstemmelserne.</span><span class="sxs-lookup"><span data-stu-id="a2d80-144">If you select the **Show Warning** check box and if there are any discrepancies between the inventory totals and G/L totals, the program shows messages in the **Warning** field of the grid that explain the discrepancy.</span></span> <span data-ttu-id="a2d80-145">Hvis du klikker på feltet Advarsel, får du yderligere oplysninger om, hvad advarslen betyder.</span><span class="sxs-lookup"><span data-stu-id="a2d80-145">If you choose the Warning field, the program gives you more information on what the warning means.</span></span>

<span data-ttu-id="a2d80-146">Vælg handlingen **Vis matrix**, når du har angivet alle relevante filtre.</span><span class="sxs-lookup"><span data-stu-id="a2d80-146">When you have entered all relevant filters, choose the **Show Matrix** action.</span></span> <span data-ttu-id="a2d80-147">Dataene udregnes og matrix-vinduet vises.</span><span class="sxs-lookup"><span data-stu-id="a2d80-147">The data is calculated and the matrix window appears.</span></span>

<span data-ttu-id="a2d80-148">I den venstre kolonne i gitteret vises forskellige finanskontotyper, som er tilknyttet lageret.</span><span class="sxs-lookup"><span data-stu-id="a2d80-148">On the far left column in the grid, you see the various general ledger account types that are associated with inventory.</span></span> <span data-ttu-id="a2d80-149">Gitteret viser derefter totalerne for fakturerede, ufakturerede (foreløbige) og VIA-værdi for hver kontotype.</span><span class="sxs-lookup"><span data-stu-id="a2d80-149">The grid then shows the invoiced, non-invoiced (interim), and WIP inventory totals for each of these account types.</span></span> <span data-ttu-id="a2d80-150">Disse totaler beregnes ud fra værdiposterne.</span><span class="sxs-lookup"><span data-stu-id="a2d80-150">These totals are calculated from the value entries.</span></span>

<span data-ttu-id="a2d80-151">De næste kolonner viser totalerne for de samme kontotyper beregnet ud fra finansposterne.</span><span class="sxs-lookup"><span data-stu-id="a2d80-151">The next columns show the totals for the same account types calculated from the general ledger entries.</span></span>

<span data-ttu-id="a2d80-152">Vælg beløbet i en af totalerne for at se de poster i lagerrapporten, der blev brugt til at beregne totalerne.</span><span class="sxs-lookup"><span data-stu-id="a2d80-152">Choose the  amount in any of the total fields to see the inventory report entries that were used to calculate the totals.</span></span> <span data-ttu-id="a2d80-153">For lagertotalerne er posterne i lagerrapporten summen af værdiposterne for varerne.</span><span class="sxs-lookup"><span data-stu-id="a2d80-153">For inventory totals, the inventory report entries are the sums of the value entries for the items.</span></span> <span data-ttu-id="a2d80-154">For finanstotalerne er posterne i lagerrapporten summen fra finansposterne.</span><span class="sxs-lookup"><span data-stu-id="a2d80-154">For the G/L totals, the inventory report entries are the sums from the general ledger entries.</span></span>

## <a name="see-also"></a><span data-ttu-id="a2d80-155">Se også</span><span class="sxs-lookup"><span data-stu-id="a2d80-155">See Also</span></span>  
[<span data-ttu-id="a2d80-156">Administrere lageromkostninger</span><span class="sxs-lookup"><span data-stu-id="a2d80-156">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
[<span data-ttu-id="a2d80-157">Køb</span><span class="sxs-lookup"><span data-stu-id="a2d80-157">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="a2d80-158">[Salg](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="a2d80-158">[Sales](sales-manage-sales.md)  </span></span>  
<span data-ttu-id="a2d80-159">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a2d80-159">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="a2d80-160">Generelle forretningsfunktioner</span><span class="sxs-lookup"><span data-stu-id="a2d80-160">General Business Functionality</span></span>](ui-across-business-areas.md)
