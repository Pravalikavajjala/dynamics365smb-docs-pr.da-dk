---
title: "Opsætning af marketingkampagner i Business Central | Microsoft Docs"
description: "Beskriver, hvordan du kan oprette og styre marketingkampagner i Business Central som en hjælp til at identificere og tiltrække potentielle kunder og bibeholde kunder."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, campaign, promo, prospect
ms.date: 06/06/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 4c3f0f612c13d9fe84cffc4862641301795bcebd
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="managing-marketing-campaigns"></a><span data-ttu-id="b76ee-103">Administration af marketingkampagner</span><span class="sxs-lookup"><span data-stu-id="b76ee-103">Managing Marketing Campaigns</span></span>
<span data-ttu-id="b76ee-104">Når du har fastlagt en stærk marketingplan, kan du identificere og tiltrække kunder og holde på dem.</span><span class="sxs-lookup"><span data-stu-id="b76ee-104">Having a strong marketing plan in place enables you to identify, attract, and retain customers.</span></span> <span data-ttu-id="b76ee-105">En marketingplan består af forskellige kampagner og andre interaktioner i forbindelse med salgs- og marketingaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="b76ee-105">A marketing plan consists of various campaigns and other interactions in connection with your sales and marketing activities.</span></span> <span data-ttu-id="b76ee-106">Mens du planlægger en kampagne, skal du beslutte, hvilke kontaktpersoner der skal være målet, hvilken type kampagne kampagnen skal være (f.eks. en messe eller direct mail), og hvilke sælgere der skal udføre de enkelte opgaver.</span><span class="sxs-lookup"><span data-stu-id="b76ee-106">While planning a campaign, you need to decide which contacts to target, what type of campaign (such as trade show or direct mail), and what salespeople will perform each task.</span></span>

<span data-ttu-id="b76ee-107">Hver kampagne består af forskellige aktiviteter eller opgaver.</span><span class="sxs-lookup"><span data-stu-id="b76ee-107">Each campaign consists of various activities or tasks.</span></span> <span data-ttu-id="b76ee-108">Du kan samle flere opgaver, for eksempel opgaver, der hver repræsenterer et trin, i aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="b76ee-108">You can combine multiple task, for example tasks that each represent a step, in activities.</span></span> <span data-ttu-id="b76ee-109">Aktivitetsopgaver er forbundet med hinanden vha. en datoformel.</span><span class="sxs-lookup"><span data-stu-id="b76ee-109">Activity tasks are related to each other by a date formula.</span></span> <span data-ttu-id="b76ee-110">Individuelle opgaver kan kun tildeles til sælgere.</span><span class="sxs-lookup"><span data-stu-id="b76ee-110">Individual tasks can only be assigned to salespeople.</span></span> <span data-ttu-id="b76ee-111">Aktiviteter kan tildeles til leads, sælgere, grupper af sælgere og kontaktpersoner.</span><span class="sxs-lookup"><span data-stu-id="b76ee-111">Activities can be assigned to opportunities, salespeople, groups of sales people, and contacts.</span></span> <span data-ttu-id="b76ee-112">Du kan finde flere oplysninger i [Konfigurere salgsprocesser og -procesfaser for leads](marketing-how-setup-opportunity-sales-cycles-stages.md).</span><span class="sxs-lookup"><span data-stu-id="b76ee-112">For more information, see [Set Up Opportunity Sales Cycles and Cycle Stages](marketing-how-setup-opportunity-sales-cycles-stages.md).</span></span>

## <a name="defining-individual-campaigns"></a><span data-ttu-id="b76ee-113">Definere individuelle kampagner</span><span class="sxs-lookup"><span data-stu-id="b76ee-113">Defining individual campaigns</span></span>
<span data-ttu-id="b76ee-114">Når du vil oprette en kampagne, skal du først definere *statuskoder for kampagnen*.</span><span class="sxs-lookup"><span data-stu-id="b76ee-114">Before you can create a campaign, you must set up *campaign status codes*.</span></span> <span data-ttu-id="b76ee-115">Via. disse koder kan du styre dine kampagner ved at tildele kampagnen en status.</span><span class="sxs-lookup"><span data-stu-id="b76ee-115">Using these codes will help you manage your campaigns by assigning a status to the campaign.</span></span> <span data-ttu-id="b76ee-116">Efterhånden som du arbejder dig gennem faserne i en kampagne, kan du se, hvilket trin en kampagne er på, og hvilket trin der følger efter.</span><span class="sxs-lookup"><span data-stu-id="b76ee-116">As you work through the stages of a campaign, you are able to see what step a campaign is at and what step comes next.</span></span> <span data-ttu-id="b76ee-117">Du kan definerer statuskoder for kampagner i vinduet **Kampagnestatus**.</span><span class="sxs-lookup"><span data-stu-id="b76ee-117">You set up campaign status codes in the **Campaign Status** window.</span></span>

<span data-ttu-id="b76ee-118">Du kan oprette et kampagnekort til hver kampagne, som du vil holde styr på.</span><span class="sxs-lookup"><span data-stu-id="b76ee-118">You can create a campaign card for each campaign that you want to keep track of.</span></span> <span data-ttu-id="b76ee-119">Du kan også få vist disse kampagnekort, så du kan se generelle oplysninger om dine kampagner.</span><span class="sxs-lookup"><span data-stu-id="b76ee-119">You can also view these campaign cards to view general information about your campaigns.</span></span>
<span data-ttu-id="b76ee-120">Du kan slette kampagneposter, f.eks. hvis de registrerer en handling, der er annulleret.</span><span class="sxs-lookup"><span data-stu-id="b76ee-120">You can delete campaign entries, such as if the entry records an action that has been canceled.</span></span> <span data-ttu-id="b76ee-121">Kun annullerede kampagneposter kan slettes.</span><span class="sxs-lookup"><span data-stu-id="b76ee-121">Only canceled campaign entries can be deleted.</span></span>

### <a name="selecting-the-target-audience"></a><span data-ttu-id="b76ee-122">Vælge målgruppen</span><span class="sxs-lookup"><span data-stu-id="b76ee-122">Selecting the target audience</span></span>
<span data-ttu-id="b76ee-123">Når du har oprettet en kampagne, kan du begynde at oprette målgrupper, der specificerer målgruppen for kampagnen.</span><span class="sxs-lookup"><span data-stu-id="b76ee-123">After you have created a campaign, you can start creating segments that specify the target audience of the campaign.</span></span> <span data-ttu-id="b76ee-124">Der kan finde flere oplysninger under [Administrere målgrupper](marketing-segments.md).</span><span class="sxs-lookup"><span data-stu-id="b76ee-124">For more information, see [Managing Segments](marketing-segments.md).</span></span>

### <a name="registering-discount-percentages"></a><span data-ttu-id="b76ee-125">Registrere rabatprocenter</span><span class="sxs-lookup"><span data-stu-id="b76ee-125">Registering discount percentages</span></span>
<span data-ttu-id="b76ee-126">Når du har oprettet en kampagne, besluttet, hvilken målgruppe kampagnen skal rettes mod, og angivet start- og slutdato, skal du registrere den rabatprocent, som kunden får på de individuelle varer på linjerne i vinduet **Salgslinjerabatter**.</span><span class="sxs-lookup"><span data-stu-id="b76ee-126">When you have set up your campaign, decided what segments you want the campaign to cover, and set the starting and ending dates, you register the discount percentage that the customer will receive on the individual items on the lines in the **Sales Line Discounts** window.</span></span> <span data-ttu-id="b76ee-127">Du kan også registrere salgsprisen for de enkelte varer på linjerne i vinduet **Salgspriser**.</span><span class="sxs-lookup"><span data-stu-id="b76ee-127">You can also register the sales prices for the individual items on the lines in the **Sales Prices** window.</span></span> <span data-ttu-id="b76ee-128">Du kan få adgang til begge vinduer fra kampagnekortet.</span><span class="sxs-lookup"><span data-stu-id="b76ee-128">You can access both windows from the campaign card.</span></span>

 <span data-ttu-id="b76ee-129">Når du har angivet salgspriserne/linjerabatterne og målgrupperne på kampagnekortet, skal de aktiveres, så kampagnepriserne og -rabatterne vises på linjerne.</span><span class="sxs-lookup"><span data-stu-id="b76ee-129">When you have set up the sales prices/line discounts and the segments on the campaign card, you must activate them so that the campaign prices/discounts will be reflected on the lines.</span></span>

> [!NOTE]  
>   <span data-ttu-id="b76ee-130">Hvis du vil aktivere salgspriserne/linjerabatterne, skal du angive, om kampagnen er henvendt til hele målgruppen eller kun bestemte kontakter.</span><span class="sxs-lookup"><span data-stu-id="b76ee-130">In order to activate the sales prices/line discounts, you must specify if the whole segment or only some contacts are targets of the campaign.</span></span> <span data-ttu-id="b76ee-131">Hvis salgspriserne/linjerabatterne dækker alle kontakter i målgruppen, skal du markere feltet **Kampagnemålgruppe** i oversigtspanelet **Kampagne** på **målgruppekortet**.</span><span class="sxs-lookup"><span data-stu-id="b76ee-131">If the sales prices/line discounts covers all the contacts in the segment, select the **Campaign Target** field on the **Campaign** FastTab of the **Segment** card.</span></span>

<span data-ttu-id="b76ee-132">Hvis salgspriserne/linjerabatterne ikke skal tilbydes til alle kontakter i målgruppen, skal markeringen fjernes fra feltet **Kampagnemålgruppe** for de relevante kontakter.</span><span class="sxs-lookup"><span data-stu-id="b76ee-132">If the sales prices/line discounts are not to be offered to all the contacts in the segment, you can clear the **Campaign Target** field for the relevant contacts.</span></span> <span data-ttu-id="b76ee-133">Hvis feltet ikke vises, kan du føje det til visningen.</span><span class="sxs-lookup"><span data-stu-id="b76ee-133">If you cannot see this field, you can add it to your view.</span></span> <span data-ttu-id="b76ee-134">Du kan finde flere oplysninger under [Tilpasse dit arbejdsområde](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="b76ee-134">For more information, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>

## <a name="conducting-campaigns"></a><span data-ttu-id="b76ee-135">Udføre kampagner</span><span class="sxs-lookup"><span data-stu-id="b76ee-135">Conducting campaigns</span></span>
<span data-ttu-id="b76ee-136">Efterhånden som en kampagne kører, registreres alle interaktioner med kontaktpersonerne, eller målgruppen, så du kan få vist statistik og andre oplysninger om kostpriser og kampagnens succeshyppigheder.</span><span class="sxs-lookup"><span data-stu-id="b76ee-136">As a campaign runs, all interactions with your contacts, or segment, are recorded so that you can get statistics and other information about the costs and success rates of the campaign.</span></span>

<span data-ttu-id="b76ee-137">Kampagner udføres af sælgere, og du skal oprette aktiviteter, der repræsenterer hver opgave, og tildele dem til de relevante sælgere.</span><span class="sxs-lookup"><span data-stu-id="b76ee-137">Campaigns are conducted by salespeople, and you must create activities to represent each task and assign them to the relevant salespeople.</span></span> <span data-ttu-id="b76ee-138">Du kan finde flere oplysninger i [Konfigurere salgsprocesser og -procesfaser for leads](marketing-how-setup-opportunity-sales-cycles-stages.md).</span><span class="sxs-lookup"><span data-stu-id="b76ee-138">For more information, see [Set Up Opportunity Sales Cycles and Cycle Stages](marketing-how-setup-opportunity-sales-cycles-stages.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="b76ee-139">Se også</span><span class="sxs-lookup"><span data-stu-id="b76ee-139">See Also</span></span>
[<span data-ttu-id="b76ee-140">Administrere kontakter</span><span class="sxs-lookup"><span data-stu-id="b76ee-140">Managing Contacts</span></span>](marketing-contacts.md)  
[<span data-ttu-id="b76ee-141">Administrere målgrupper</span><span class="sxs-lookup"><span data-stu-id="b76ee-141">Managing Segments</span></span>](marketing-segments.md)  
[<span data-ttu-id="b76ee-142">Administrere salgsleads</span><span class="sxs-lookup"><span data-stu-id="b76ee-142">Managing Sales Opportunities</span></span>](marketing-manage-sales-opportunities.md)  
[<span data-ttu-id="b76ee-143">Arbejde med Business Central</span><span class="sxs-lookup"><span data-stu-id="b76ee-143">Working with Business Central</span></span>](ui-work-product.md)  
