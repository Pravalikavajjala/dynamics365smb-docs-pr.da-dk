---
title: "Anskaffe anlægsaktiver | Microsoft Docs"
description: "Du kan oprette et anlægsaktiv, tildele en afskrivningsprofil og registrere anlægsaktivets anskaffelsespris."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: purchase fixed asset
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: dc869b481ed84ab96a8b7cef0e15dd0cf8fef213
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="acquire-fixed-assets"></a><span data-ttu-id="86c3a-103">Anskaffede anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="86c3a-103">Acquire Fixed Assets</span></span>
<span data-ttu-id="86c3a-104">For hvert anlægsaktiv skal du definere et kort med oplysninger om aktivet.</span><span class="sxs-lookup"><span data-stu-id="86c3a-104">For each fixed asset, you must set up a card containing information about the asset.</span></span> <span data-ttu-id="86c3a-105">Du kan angive bygninger eller produktionsudstyr som et hovedanlæg med en komponentliste, og du kan gruppere dem på forskellige måder, f.eks efter art, afdeling eller lokation.</span><span class="sxs-lookup"><span data-stu-id="86c3a-105">You can set up buildings or production equipment as a main asset with a component list, and you can group them in various ways, such as by class, department, or location.</span></span> <span data-ttu-id="86c3a-106">Der skal oprettes en afskrivningsprofil, og den skal tildeles til hvert enkelt anlægsaktiv, før du kan hente det.</span><span class="sxs-lookup"><span data-stu-id="86c3a-106">A depreciation book must be set up and assigned to each fixed asset before you can acquire it.</span></span>

<span data-ttu-id="86c3a-107">Når der er oprettet et anlægsaktiv, og der er tildelt en afskrivningsprofil, skal du anskaffe anlægsaktivet.</span><span class="sxs-lookup"><span data-stu-id="86c3a-107">When a fixed asset is set up and a depreciation book assigned, you must acquire the fixed asset.</span></span> <span data-ttu-id="86c3a-108">For at få et anlægsaktiv skal du registrere dens anskaffelsespris i den relevante finanskonto, bankkonto eller leverandør ved at bogføre en anskaffelsestransaktion fra vinduet **Anlægskassekladde**.</span><span class="sxs-lookup"><span data-stu-id="86c3a-108">To acquire a fixed asset, you record its acquisition cost in the relevant G/L account, bank account, or vendor by posting an acquisition transaction from the **Fixed Asset G/L Journal** window.</span></span> <span data-ttu-id="86c3a-109">Du kan bruge den **Bistået anskaffelse af anlægsaktiv** til at oprette og bogføre de nødvendige finanskladdelinjer automatisk.</span><span class="sxs-lookup"><span data-stu-id="86c3a-109">You can use the **Assisted Fixed Asset Acquisition** window to create and post the required general journal lines automatically.</span></span>

<span data-ttu-id="86c3a-110">Skrapværdien er restværdien af et anlæg, der ikke længere kan bruges.</span><span class="sxs-lookup"><span data-stu-id="86c3a-110">The salvage value is the residual value of a fixed asset when it can no longer be used.</span></span> <span data-ttu-id="86c3a-111">Du kan bogføre skrapværdien samtidigt med, at du bogfører anskaffelsesprisen.</span><span class="sxs-lookup"><span data-stu-id="86c3a-111">You can post the salvage value at the same time as you post the acquisition cost.</span></span> <span data-ttu-id="86c3a-112">Du kan finde flere oplysninger i [Afskrive eller amortisere anlægsaktiver](fa-how-depreciate-amortize.md).</span><span class="sxs-lookup"><span data-stu-id="86c3a-112">For more information, see [Depreciate or Amortize Fixed Assets](fa-how-depreciate-amortize.md).</span></span>

<span data-ttu-id="86c3a-113">Indeksering anvendes til at justere for ændringer af det generelle prisniveau.</span><span class="sxs-lookup"><span data-stu-id="86c3a-113">Indexation is used to adjust values for general price-level changes.</span></span> <span data-ttu-id="86c3a-114">Kørslen **Indekser anlæg** kan bruges til at beregne anskaffelsespriser som genanskaffelsespriser.</span><span class="sxs-lookup"><span data-stu-id="86c3a-114">The **Index Fixed Assets** batch job can be used to calculate the acquisition costs at replacement costs.</span></span>

## <a name="to-create-a-fixed-asset-and-acquire-it-automatically"></a><span data-ttu-id="86c3a-115">Sådan oprettes og anskaffes et anlægsaktiv automatisk</span><span class="sxs-lookup"><span data-stu-id="86c3a-115">To create a fixed asset and acquire it automatically</span></span>
<span data-ttu-id="86c3a-116">Følgende procedure beskriver, hvordan du opretter et anlægsaktiv og derefter anskaffer det ved hjælp af vinduet **Bistået anskaffelse af anlægsaktiver** for at oprette og bogføre de nødvendige anlægskassekladdelinjer.</span><span class="sxs-lookup"><span data-stu-id="86c3a-116">The following procedure describes how to create a fixed asset and then acquire it by using the **Assisted Fixed Asset Acquisition** window to create and post the required fixed asset G/L journal lines.</span></span> <span data-ttu-id="86c3a-117">Du kan også oprette og bogføre linjerne manuelt.</span><span class="sxs-lookup"><span data-stu-id="86c3a-117">You can also create and post the journal lines manually.</span></span> <span data-ttu-id="86c3a-118">Du kan finde flere oplysninger i afsnittet "Sådan bogføres anskaffelse af et anlægsaktiv manuelt med anlægskassekladden".</span><span class="sxs-lookup"><span data-stu-id="86c3a-118">For more information, see the "To post a fixed asset acquisition manually with the fixed asset G/L journal" section.</span></span>

1. <span data-ttu-id="86c3a-119">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Anlægsaktiver**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="86c3a-119">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>  
2. <span data-ttu-id="86c3a-120">Vælg handlingen **Ny** handling, og udfyld felterne på oversigtspanelet **Generelt** efter behov.</span><span class="sxs-lookup"><span data-stu-id="86c3a-120">Choose the **New** action, and then fill in the fields on the **General** FastTab as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="86c3a-121">I oversigtspanelet **Afskrivningsprofil** skal du udfylde felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="86c3a-121">On the **Depreciation Book** FastTab, fill in the fields as necessary.</span></span> <span data-ttu-id="86c3a-122">I dette trin tildeles en afskrivningsprofil til anlægsaktivet.</span><span class="sxs-lookup"><span data-stu-id="86c3a-122">This step assigns a depreciation book to the fixed asset.</span></span>  
4. <span data-ttu-id="86c3a-123">Hvis du vil tildele mere end én afskrivningsprofil til anlægsaktivet, skal du vælge handlingen **Tilføj flere afskrivningsprofiler**.</span><span class="sxs-lookup"><span data-stu-id="86c3a-123">If you need to assign more than one depreciation book to the fixed asset, choose the **Add More Depreciation Books** action.</span></span> <span data-ttu-id="86c3a-124">Du kan finde flere oplysninger i afsnittet "Sådan tildeles en afskrivningsprofil til et anlægsaktiv" i [Konfigurere afskrivning af anlægsaktiver](fa-how-setup-depreciation.md).</span><span class="sxs-lookup"><span data-stu-id="86c3a-124">For more information, see the "To assign a depreciation book to a fixed asset" section in [Set Up Fixed Asset Depreciation](fa-how-setup-depreciation.md).</span></span>

    <span data-ttu-id="86c3a-125">Når alle felter, der kræves for at anskaffe et anlægsaktiv, er udfyldt, vises beskeden **Du er klar til at anskaffe anlægsaktivet. Anskaf** øverst på siden.</span><span class="sxs-lookup"><span data-stu-id="86c3a-125">When all fields required to acquire a fixed asset are filled in, the **You are ready to acquire the fixed asset. Acquire** notification appears at the top of the page.</span></span>
5. <span data-ttu-id="86c3a-126">Vælg handlingen **Anskaf** i beskeden.</span><span class="sxs-lookup"><span data-stu-id="86c3a-126">Choose the **Acquire** action in the notification.</span></span>
6. <span data-ttu-id="86c3a-127">Følg trinnene i vinduet **Bistået anskaffelse af anlægsaktiver** for at fuldføre automatisk anskaffelse af anlægsaktivet.</span><span class="sxs-lookup"><span data-stu-id="86c3a-127">Follow the steps in the **Assisted Fixed Asset Acquisition** window to complete the automatic acquisition of the fixed asset.</span></span>

> [!NOTE]  
>   <span data-ttu-id="86c3a-128">Du kan også bogføre anskaffelsespriser som kreditposter.</span><span class="sxs-lookup"><span data-stu-id="86c3a-128">You can also post acquisition cost as credits.</span></span> <span data-ttu-id="86c3a-129">I så fald skal du huske, at værdien i feltet **Anskaffelsespris inkl. moms** skal have et minustegn for at angive en kredit.</span><span class="sxs-lookup"><span data-stu-id="86c3a-129">In that case, remember that the value in the **Acquisition Cost Incl. VAT** field must be with a minus sign to indicate a credit.</span></span>

<span data-ttu-id="86c3a-130">Når du vælger **Udfør**, udfyldes feltet **Bogført værdi** i vinduet **Anlægskort**, hvilket angiver, at anlægsaktivet er anskaffet til den angivne anskaffelsespris.</span><span class="sxs-lookup"><span data-stu-id="86c3a-130">When you choose **Finish**, the **Book Value** field in the **Fixed Asset Card** window is filled, indicating that the fixed asset has been acquired at the specified acquisition cost.</span></span>  

## <a name="to-set-up-a-component-list-for-a-main-asset"></a><span data-ttu-id="86c3a-131">Sådan konfigureres en komponentliste for et hovedanlæg</span><span class="sxs-lookup"><span data-stu-id="86c3a-131">To set up a component list for a main asset</span></span>
<span data-ttu-id="86c3a-132">Du kan gruppere anlægsaktiverne i hovedanlæg og de tilhørende komponenter.</span><span class="sxs-lookup"><span data-stu-id="86c3a-132">You can group your fixed assets into main assets and their components.</span></span> <span data-ttu-id="86c3a-133">Du kan f.eks. have en produktionsmaskine, som består af mange dele, som du vil gruppere på denne måde.</span><span class="sxs-lookup"><span data-stu-id="86c3a-133">For example, you may have a production machine that consists of many parts that you want to group in this manner.</span></span>  

<span data-ttu-id="86c3a-134">Både hovedanlægget og alle dets komponenter skal oprettes som individuelle anlægskort.</span><span class="sxs-lookup"><span data-stu-id="86c3a-134">Both the main asset and all its components must be set up as individual fixed asset cards.</span></span> <span data-ttu-id="86c3a-135">Når du har oprettet en komponentliste, udfylder [!INCLUDE[d365fin](includes/d365fin_md.md)] felterne **Hovedanlæg/underanl.** og **Hovedanlæg/underanl.** på anlægskortene.</span><span class="sxs-lookup"><span data-stu-id="86c3a-135">After you have set up a component list, [!INCLUDE[d365fin](includes/d365fin_md.md)] automatically fills in the **Main Assets/Component** and **Components of Main Asset** fields on the fixed asset cards.</span></span>

1. <span data-ttu-id="86c3a-136">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Anlægsaktiver**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="86c3a-136">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.</span></span>
2. <span data-ttu-id="86c3a-137">Vælg det anlægsaktiv, der er hovedanlægget, og vælg derefter handlingen **Hovedanlæg**.</span><span class="sxs-lookup"><span data-stu-id="86c3a-137">Select the fixed asset that is the main asset, and then choose the **Main Asset Components** action.</span></span>
3. <span data-ttu-id="86c3a-138">I vinduet **Hovedanlæg** skal du vælge feltet **Anlægsnr**. og derefter vælge de anlægsaktiver, der skal tilføjes som en komponent i hovedanlægget.</span><span class="sxs-lookup"><span data-stu-id="86c3a-138">In the **Main Asset Components** window, choose the **FA No**. field, and then select the fixed asset that you want to add as a component of the main asset.</span></span>
4. <span data-ttu-id="86c3a-139">Luk vinduet.</span><span class="sxs-lookup"><span data-stu-id="86c3a-139">Close the window.</span></span>
5. <span data-ttu-id="86c3a-140">Gentag trin 3 til 4 for hver underdel til anlægget, du vil tilføje.</span><span class="sxs-lookup"><span data-stu-id="86c3a-140">Repeat steps 3 and 4 for each component asset that you want to add.</span></span>
6. <span data-ttu-id="86c3a-141">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Anlægsopsætning**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="86c3a-141">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Asset Setup**, and then choose the related link.</span></span>
7. <span data-ttu-id="86c3a-142">Markér afkrydsningsfeltet **Tillad bogf. på hovedanlæg**.</span><span class="sxs-lookup"><span data-stu-id="86c3a-142">Select the **Allow Posting to Main Assets** check box.</span></span>

## <a name="to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal"></a><span data-ttu-id="86c3a-143">Sådan bogføres anskaffelse af et anlægsaktiv manuelt med finanskassekladden</span><span class="sxs-lookup"><span data-stu-id="86c3a-143">To post a fixed asset acquisition manually with the fixed asset G/L journal</span></span>
<span data-ttu-id="86c3a-144">Følgende fremgangsmåde bruges til at anskaffe et anlægsaktiv manuelt ved at oprette og bogføre linjerne i vinduet **Anlægsfinanskladde**.</span><span class="sxs-lookup"><span data-stu-id="86c3a-144">The following procedure describes how to acquire a fixed asset manually by creating and posting lines in the **Fixed Asset G/L Journal** window.</span></span> <span data-ttu-id="86c3a-145">Du kan også anskaffe et anlægsaktiv automatisk ved hjælp af vinduet **Bistået anskaffelse af anlægsaktiver**.</span><span class="sxs-lookup"><span data-stu-id="86c3a-145">You can also acquire a fixed asset automatically by using the **Assisted Fixed Asset Acquisition** window.</span></span> <span data-ttu-id="86c3a-146">Flere oplysninger under trin 5 i afsnittet "Sådan oprettes og anskaffes et anlægsaktiv automatisk".</span><span class="sxs-lookup"><span data-stu-id="86c3a-146">For more information, see step 5 in the "To create a fixed asset and acquire it automatically" section.</span></span>

> [!NOTE]  
>   <span data-ttu-id="86c3a-147">Du kan også bogføre anskaffelsespriser som kreditposter.</span><span class="sxs-lookup"><span data-stu-id="86c3a-147">You can also post acquisition cost as credits.</span></span> <span data-ttu-id="86c3a-148">I så fald skal du huske, at værdien i feltet **Beløb** skal have et minustegn for at angive en kredit.</span><span class="sxs-lookup"><span data-stu-id="86c3a-148">In that case, remember that the value in the **Amount** field must be with a minus sign to indicate a credit.</span></span>

1. <span data-ttu-id="86c3a-149">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Anlægsfinanskladder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="86c3a-149">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA G/L Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="86c3a-150">I vinduet **Anlægskassekladde** i feltet **Anlægsbogføringstype** skal du vælge **Anskaffelsespris**.</span><span class="sxs-lookup"><span data-stu-id="86c3a-150">In the **Fixed Asset G/L Journal** window, in the **FA Posting Type** field, select **Acquisition Cost**.</span></span>
3. <span data-ttu-id="86c3a-151">Udfyld de resterende felter efter behov.</span><span class="sxs-lookup"><span data-stu-id="86c3a-151">Fill in the remaining fields as necessary.</span></span>
4. <span data-ttu-id="86c3a-152">Vælg handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="86c3a-152">Choose the **Post** action.</span></span>  

> [!TIP]  
>   <span data-ttu-id="86c3a-153">Hvis du udfylder feltet **Forsikringsnr.** i anlægskassekladden, når du bogfører en anskaffelse, vil [!INCLUDE[d365fin](includes/d365fin_md.md)] også bogføre anskaffelsesprisen på anlægsaktivet på forsikringsposterne.</span><span class="sxs-lookup"><span data-stu-id="86c3a-153">If you fill in the **Insurance No.** field in the fixed asset G/L journal when you post an acquisition cost, then [!INCLUDE[d365fin](includes/d365fin_md.md)] will also post the acquisition cost of the fixed asset to the insurance coverage ledger.</span></span> <span data-ttu-id="86c3a-154">Du kan finde flere oplysninger i [Forsikre anlægsaktiver](fa-how-insure.md).</span><span class="sxs-lookup"><span data-stu-id="86c3a-154">For more information, see [Insure Fixed Assets](fa-how-insure.md).</span></span>

## <a name="to-cancel-an-acquisition-cost-posting-for-one-fixed-asset"></a><span data-ttu-id="86c3a-155">Sådan annulleres bogføringen af en anskaffelsespris for et anlægsaktiv</span><span class="sxs-lookup"><span data-stu-id="86c3a-155">To cancel an acquisition cost posting for one fixed asset</span></span>
<span data-ttu-id="86c3a-156">Hvis du laver en fejl under bogføring af en anskaffelsespris, kan du fjerne posten vha. kørslen **Annuller anlægsposter** og derefter bogføre den korrekte anskaffelsespost.</span><span class="sxs-lookup"><span data-stu-id="86c3a-156">If you make an error when posting an acquisition cost, you can remove the entry with the **Cancel FA Entries** batch job and then post the correct acquisition entry.</span></span> <span data-ttu-id="86c3a-157">De forkerte poster overføres til vinduet **Anlægsfejlposter**.</span><span class="sxs-lookup"><span data-stu-id="86c3a-157">The erroneous entries are transferred to the **FA Error Ledger Entries** window.</span></span>

<span data-ttu-id="86c3a-158">Hvis du f.eks, bogfører en anskaffelse med den forkerte dato, skal du rette den snarest muligt, fordi bogføringsdatoen for anlægsaktivet bruges i mange vigtige beregninger.</span><span class="sxs-lookup"><span data-stu-id="86c3a-158">For example, if you post an acquisition with the wrong date, you must correct it as soon as possible because the fixed asset posting date is used is many critical calculations.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="86c3a-159">Du kan ikke bruge funktionen **Tilbagefør transaktioner** for anlægsposter.</span><span class="sxs-lookup"><span data-stu-id="86c3a-159">You cannot use the **Reverse Transactions** function for fixed asset entries.</span></span>

1. <span data-ttu-id="86c3a-160">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Annuller anlægsposter**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="86c3a-160">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Cancel FA Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="86c3a-161">Udfyld felterne efter behov.</span><span class="sxs-lookup"><span data-stu-id="86c3a-161">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. <span data-ttu-id="86c3a-162">Vælg **OK** for at eksekvere kørslen.</span><span class="sxs-lookup"><span data-stu-id="86c3a-162">Choose the **OK** button to run the batch job.</span></span>
4. <span data-ttu-id="86c3a-163">Når den eller de forkerte poster annulleres, kan du fortsætte med at bogføre den korrekte anskaffelsespris.</span><span class="sxs-lookup"><span data-stu-id="86c3a-163">When the incorrect entry or entries are canceled, proceed to post the correct acquisition cost.</span></span>

<span data-ttu-id="86c3a-164">Hvis du vil annullere poster for flere anlæg samtidigt, kan du bruge kørslen **Annuller anlægsposter**.</span><span class="sxs-lookup"><span data-stu-id="86c3a-164">To cancel ledger entries for multiple fixed assets at a time, use the **Cancel FA Ledger Entries** batch job.</span></span>

## <a name="to-post-the-salvage-value-together-with-the-acquisition-cost"></a><span data-ttu-id="86c3a-165">Sådan bogføres skrapværdien sammen med anskaffelsesprisen</span><span class="sxs-lookup"><span data-stu-id="86c3a-165">To post the salvage value together with the acquisition cost</span></span>
<span data-ttu-id="86c3a-166">Du kan bogføre skrapværdien sammen med anskaffelsesprisen fra en anlægskassekladde.</span><span class="sxs-lookup"><span data-stu-id="86c3a-166">You can post the salvage value together with the acquisition cost from a fixed asset G/L journal.</span></span>    

1. <span data-ttu-id="86c3a-167">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Annuller anlægsposter**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="86c3a-167">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Cancel FA Entries**, and then choose the related link.</span></span>
2. <span data-ttu-id="86c3a-168">Opret anskaffelseskladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="86c3a-168">Create the acquisition journal line.</span></span> <span data-ttu-id="86c3a-169">Du kan finde flere oplysninger i afsnittet "Sådan bogføres anskaffelse af et anlægsaktiv manuelt med anlægskassekladden".</span><span class="sxs-lookup"><span data-stu-id="86c3a-169">For more information, see the "To post a fixed asset acquisition manually with the fixed asset G/L journal" section.</span></span>
3. <span data-ttu-id="86c3a-170">Angiv beløbet for skrapværdien som en kreditpost (med et minustegn) i feltet **Skrapværdi** på kladdelinjen.</span><span class="sxs-lookup"><span data-stu-id="86c3a-170">In the **Salvage Value** field on the journal line, enter the salvage value amount as a credit (with a minus sign).</span></span>
4. <span data-ttu-id="86c3a-171">Vælg handlingen **Bogfør**.</span><span class="sxs-lookup"><span data-stu-id="86c3a-171">Choose the **Post** action.</span></span>

> [!NOTE]  
>   <span data-ttu-id="86c3a-172">Du kan kun vælge bogføringstypen **Skrapværdi** i vinduet **Anlægskladde**.</span><span class="sxs-lookup"><span data-stu-id="86c3a-172">The **Salvage Value** posting type is an option in the **Fixed Asset Journal** window only.</span></span> <span data-ttu-id="86c3a-173">Det er ikke tilgængeligt i vinduet **Anlægskassekladde**, fordi skrapværdi aldrig bogføres i finansregnskabet.</span><span class="sxs-lookup"><span data-stu-id="86c3a-173">It is not available in the **Fixed Asset G/L Journal** window because salvage value is never posted to the general ledger.</span></span>

## <a name="see-also"></a><span data-ttu-id="86c3a-174">Se også</span><span class="sxs-lookup"><span data-stu-id="86c3a-174">See Also</span></span>
[<span data-ttu-id="86c3a-175">Anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="86c3a-175">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="86c3a-176">Opsætning af anlægsaktiver</span><span class="sxs-lookup"><span data-stu-id="86c3a-176">Setting Up Fixed Assets</span></span>](fa-setup.md)  
[<span data-ttu-id="86c3a-177">Finans</span><span class="sxs-lookup"><span data-stu-id="86c3a-177">Finance</span></span>](finance.md)  
<span data-ttu-id="86c3a-178">[Velkommen til [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="86c3a-178">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="86c3a-179">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="86c3a-179">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
