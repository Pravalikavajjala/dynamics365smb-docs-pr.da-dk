---
title: "Tilpasse visuelle signaler om en køindikators aktivitet | Microsoft Docs"
description: "Du kan oprette et farvet symbol i et Køindikator-felt for at levere et tilpasset visuelt signal om køindikatorens aktivitet."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, customize
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: c93bd33d972b030ede02ad7b24a8127ff2174141
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-a-colored-indicator-on-cues"></a><span data-ttu-id="8bfec-103">Oprette en farvet indikator på køindikatorer</span><span class="sxs-lookup"><span data-stu-id="8bfec-103">Set Up a Colored Indicator on Cues</span></span>
<span data-ttu-id="8bfec-104">Du kan oprette køindikatorer, der vises på siden **Start**, for at medtage en indikator, der skifter farve ud fra dataværdierne i køerne.</span><span class="sxs-lookup"><span data-stu-id="8bfec-104">You can set up Cues that appear on the **Home** page to include an indicator that changes color based on the data values in the Cues.</span></span>

<span data-ttu-id="8bfec-105">Indikatoren vises som en farvet streg langs den øverste kant af feltet Køindikator.</span><span class="sxs-lookup"><span data-stu-id="8bfec-105">The indicator appears as a colored bar along the top border of the Cue tile.</span></span> <span data-ttu-id="8bfec-106">Det indeholder et visuelt signal af status for køindikatorens aktivitet, som kan indikere favorable eller ikke-favorable betingelser for at bede brugeren om at handle.</span><span class="sxs-lookup"><span data-stu-id="8bfec-106">It provides a visual signal of the status of the Cue's activity, which can indicate favorable or unfavorable conditions to prompt the user to take action.</span></span> <span data-ttu-id="8bfec-107">Hvis en køindikator f.eks. viser løbende salgsfakturaer, kan du oprette indikatoren som grøn (favorabel), når det samlede antal løbende salgsfakturaer er under 10, og rød (ikke-favorabel), når det samlede antal er større end 20.</span><span class="sxs-lookup"><span data-stu-id="8bfec-107">For example, if a Cue displays ongoing sales invoices, you can set up the indicator to appear green (favorable) when total number of ongoing sales invoices is below 10, and appears red (unfavorable) when the total is greater than 20.</span></span>

<span data-ttu-id="8bfec-108">Fra vinduet **Opsætning af køindikator** kan du konfigurere indikatorer for alle køindikatorer, der findes i regnskabsdatabasen.</span><span class="sxs-lookup"><span data-stu-id="8bfec-108">From the **Cue Setup** window, you set up indicators for all the Cues that are available in the company database.</span></span>

<span data-ttu-id="8bfec-109">Hvis du vil konfigurere indikatoren, kan du angive op til to tærskelværdier, der definerer tre områder af dataværdier (lav, mellem og høj), hvor du kan anvende en anden farve (eller type).</span><span class="sxs-lookup"><span data-stu-id="8bfec-109">To set up the indicator, you specify up to two threshold values that define three ranges of data values (low, middle, and high) to which you can apply a different color (or style).</span></span>

## <a name="to-set-up-colored-indicators-on-cues"></a><span data-ttu-id="8bfec-110">Sådan opretter farveindikatorer på køindikatorer</span><span class="sxs-lookup"><span data-stu-id="8bfec-110">To set up colored indicators on Cues</span></span>
1. <span data-ttu-id="8bfec-111">Under **Aktiviteter** på din **Startside** skal du vælge **Konfigurer køindikatorer**.</span><span class="sxs-lookup"><span data-stu-id="8bfec-111">Under **Activities** on your **Home** page, choose **Set Up Cues**.</span></span>  
   <span data-ttu-id="8bfec-112">Vinduet **Opsætning af køindikator** vises.</span><span class="sxs-lookup"><span data-stu-id="8bfec-112">The **Cue Setup** window appears.</span></span> <span data-ttu-id="8bfec-113">Vinduet viser de indikatorer, der aktuelt er konfigureret på køindikatorer.</span><span class="sxs-lookup"><span data-stu-id="8bfec-113">The window lists the indicators that are currently setup up on Cues.</span></span>
2. <span data-ttu-id="8bfec-114">Hvis du vil ændre en indikator skal du redigere felterne og ændre f.eks. værdierne for de forskellige intervalgrænser.</span><span class="sxs-lookup"><span data-stu-id="8bfec-114">To modify an indicator, edit the fields and modify, for example, the values for the different thresholds.</span></span>  

<span data-ttu-id="8bfec-115">Følgende tabel viser de farver, der svarer til indstillingerne for felterne **Typen Lavt interval**, **Typen Mellem interval** og **Typen Højt interval**.</span><span class="sxs-lookup"><span data-stu-id="8bfec-115">The following table lists the colors that correspond to the options of the **Low Range Style**, **Middle Range Style**, and **High Range Style** fields.</span></span>

| <span data-ttu-id="8bfec-116">Indstilling</span><span class="sxs-lookup"><span data-stu-id="8bfec-116">Option</span></span> | <span data-ttu-id="8bfec-117">Farve</span><span class="sxs-lookup"><span data-stu-id="8bfec-117">Color</span></span> |
| --- | --- |
| <span data-ttu-id="8bfec-118">**Ingen**</span><span class="sxs-lookup"><span data-stu-id="8bfec-118">**None**</span></span> |<span data-ttu-id="8bfec-119">Ingen farve (samme farve som feltet Køindikator)</span><span class="sxs-lookup"><span data-stu-id="8bfec-119">No color (same color as the Cue tile)</span></span>|
| <span data-ttu-id="8bfec-120">**Favorabel**</span><span class="sxs-lookup"><span data-stu-id="8bfec-120">**Favorable**</span></span> |<span data-ttu-id="8bfec-121">Grøn</span><span class="sxs-lookup"><span data-stu-id="8bfec-121">Green</span></span> |
| <span data-ttu-id="8bfec-122">**Ikke-favorabel**</span><span class="sxs-lookup"><span data-stu-id="8bfec-122">**Unfavorable**</span></span> |<span data-ttu-id="8bfec-123">Rød</span><span class="sxs-lookup"><span data-stu-id="8bfec-123">Red</span></span> |
| <span data-ttu-id="8bfec-124">**Tvetydig**</span><span class="sxs-lookup"><span data-stu-id="8bfec-124">**Ambiguous**</span></span> |<span data-ttu-id="8bfec-125">Gul</span><span class="sxs-lookup"><span data-stu-id="8bfec-125">Yellow</span></span> |
| <span data-ttu-id="8bfec-126">**Underordnet**</span><span class="sxs-lookup"><span data-stu-id="8bfec-126">**Subordinate**</span></span> |<span data-ttu-id="8bfec-127">Grå</span><span class="sxs-lookup"><span data-stu-id="8bfec-127">Gray</span></span> |

## <a name="see-also"></a><span data-ttu-id="8bfec-128">Se også</span><span class="sxs-lookup"><span data-stu-id="8bfec-128">See Also</span></span>
<span data-ttu-id="8bfec-129">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8bfec-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
