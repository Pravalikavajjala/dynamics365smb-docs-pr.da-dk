---
title: Bruge fakturering og Business Central | Microsoft Docs
description: "Løsning, der giver adgang til Microsoft Invoicing, når du har fået Dynamics 365 Business Central."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/22/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 7c23fdd29b8fa4da0d5eb4d86e244bd847e9e9fb
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="using-the-same-office-365-account-in-included365finincludesd365finlongmdmd-and-microsoft-invoicing"></a><span data-ttu-id="d6338-103">Bruge den samme Office 365-konto i [!INCLUDE[d365fin](includes/d365fin_long_md.md)] og Microsoft Invoicing</span><span class="sxs-lookup"><span data-stu-id="d6338-103">Using the same Office 365 Account in [!INCLUDE[d365fin](includes/d365fin_long_md.md)] and Microsoft Invoicing</span></span>
<span data-ttu-id="d6338-104">Når du tilmelder dig en prøveversion af [!INCLUDE[d365fin](includes/d365fin_md.md)], kan du gå til en 30-dages evalueringsfase, påbegynde et abonnement eller afslutte din brug af [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d6338-104">When you sign up for a trial with [!INCLUDE[d365fin](includes/d365fin_md.md)], you can move to a 30-day evaluation phase, you can start a subscription, or you can stop using [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="d6338-105">I alle tilfælde kan du, hvis du logger på Office-portalen, se et felt med navnet **Business-center**, som du skal klikke på.</span><span class="sxs-lookup"><span data-stu-id="d6338-105">In all cases, if you log into the Office Portal, you might see a tile called **Business center** and click it.</span></span> <span data-ttu-id="d6338-106">Dette er en del af Office 365 Business Premium-abonnementet, så ikke alle ser dette felt i Office-portalen.</span><span class="sxs-lookup"><span data-stu-id="d6338-106">This is part of the Office 365 Business Premium subscription, so not everyone will see that tile in the Office Portal.</span></span>  

<span data-ttu-id="d6338-107">Hvis du får adgang til Business-centeret, kan du se afsnittet **Invoicing**.</span><span class="sxs-lookup"><span data-stu-id="d6338-107">If you do access the Business center, you will see a section called **Invoicing**.</span></span> <span data-ttu-id="d6338-108">Hvis du åbner dette afsnit, vises en meddelelse om, at du ikke kan få adgang til Microsoft Invoicing, fordi kontoen bruges i [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d6338-108">If you access that section, you will see a message that you cannot access Microsoft Invoicing because your account is used in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="d6338-109">En lignende meddelelse vises, hvis du installerer mobilappen til Invoicing.</span><span class="sxs-lookup"><span data-stu-id="d6338-109">You see a similar message if you install the mobile app for Invoicing.</span></span>  

## <a name="workaround"></a><span data-ttu-id="d6338-110">Løsning</span><span class="sxs-lookup"><span data-stu-id="d6338-110">Workaround</span></span>
<span data-ttu-id="d6338-111">Invoicing og [!INCLUDE[d365fin](includes/d365fin_md.md)] har en fælles platform.</span><span class="sxs-lookup"><span data-stu-id="d6338-111">Invoicing and [!INCLUDE[d365fin](includes/d365fin_md.md)] have a shared platform.</span></span> <span data-ttu-id="d6338-112">Det betyder, at du genkendes som en eksisterende bruger af [!INCLUDE[d365fin](includes/d365fin_md.md)], når du klikker på Invoicing i Business center.</span><span class="sxs-lookup"><span data-stu-id="d6338-112">That means that you are recognized as an existing user of [!INCLUDE[d365fin](includes/d365fin_md.md)] when you click Invoicing in the Business center.</span></span> <span data-ttu-id="d6338-113">Det skyldes, at Invoicing ikke kan bruge den samme virksomhed som [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d6338-113">The reason is that Invoicing cannot use the same company as [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  

<span data-ttu-id="d6338-114">Så du skal logge på [!INCLUDE[d365fin](includes/d365fin_md.md)] og omdøbe din eksisterende virksomhed og derefter oprette en ny virksomhed, som du kan bruge i Invoicing.</span><span class="sxs-lookup"><span data-stu-id="d6338-114">So you will have to log into [!INCLUDE[d365fin](includes/d365fin_md.md)] and rename your existing company, and then create a new company that you can then use in Invoicing.</span></span> <span data-ttu-id="d6338-115">Ingen data flyttes eller overskrives under denne løsningsprocedure.</span><span class="sxs-lookup"><span data-stu-id="d6338-115">No data is moved or overwritten during this workaround.</span></span>

### <a name="to-rename-your-company"></a><span data-ttu-id="d6338-116">Sådan omdøber du din virksomhed</span><span class="sxs-lookup"><span data-stu-id="d6338-116">To rename your company</span></span>
1.  <span data-ttu-id="d6338-117">Log på dit [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d6338-117">Sign in to your [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>  
2.  <span data-ttu-id="d6338-118">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Virksomheder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="d6338-118">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Companies**, and then choose the related link.</span></span>  
3.  <span data-ttu-id="d6338-119">I vinduet **Virksomheder** skal du vælge knappen **Rediger liste**.</span><span class="sxs-lookup"><span data-stu-id="d6338-119">In the **Companies** window, choose the **Edit List** button.</span></span>  
4.  <span data-ttu-id="d6338-120">Giv posten *Min virksomhed* et andet navn.</span><span class="sxs-lookup"><span data-stu-id="d6338-120">Change the name of the *My Company* entry to something else.</span></span>  

    <span data-ttu-id="d6338-121">Vent nogle minutter.</span><span class="sxs-lookup"><span data-stu-id="d6338-121">Wait a number of minutes.</span></span> <span data-ttu-id="d6338-122">Vi foretager en række ændringer i den underliggende database, og det tager et stykke tid.</span><span class="sxs-lookup"><span data-stu-id="d6338-122">We’ll be making a number of changes in the underlying database, and that takes a while.</span></span>
5.  <span data-ttu-id="d6338-123">Når systemet er klar igen, skal du vælge knappen **Opret ny virksomhed**.</span><span class="sxs-lookup"><span data-stu-id="d6338-123">When the system is ready again, choose the **Create New Company** button.</span></span>  
6.  <span data-ttu-id="d6338-124">I den dialogboks, der vises, skal du angive navnet som *Min virksomhed* og vælge indstillingen **Produktion – Kun konfigurationsdata**.</span><span class="sxs-lookup"><span data-stu-id="d6338-124">In the dialog that appears, specify the name as *My Company*, and choose the **Production – Setup Data Only** option.</span></span>  

<span data-ttu-id="d6338-125">Der går igen nogle minutter.</span><span class="sxs-lookup"><span data-stu-id="d6338-125">This again takes a number of minutes.</span></span> <span data-ttu-id="d6338-126">Når processen er fuldført, kan du få adgang til Invoicing som en del af din Office 365 Business Premium-oplevelse.</span><span class="sxs-lookup"><span data-stu-id="d6338-126">When the process completes, you will be able to access Invoicing as part of your Office 365 Business Premium experience.</span></span>  

### <a name="what-about-my-data"></a><span data-ttu-id="d6338-127">Hvad med mine data?</span><span class="sxs-lookup"><span data-stu-id="d6338-127">What about my data?</span></span>
<span data-ttu-id="d6338-128">Når du omdøber det oprindelige Min virksomhed, omdøbes de tabeller i databasen, der indeholder din eksisterende [!INCLUDE[d365fin](includes/d365fin_md.md)]-data, men selve dataene ændres ikke.</span><span class="sxs-lookup"><span data-stu-id="d6338-128">When you rename the original My Company, the database tables that store your existing [!INCLUDE[d365fin](includes/d365fin_md.md)] data are renamed, but the data itself is not touched.</span></span>  

<span data-ttu-id="d6338-129">Hvis du bruger både Invoicing og [!INCLUDE[d365fin](includes/d365fin_md.md)], gemmes dataene i to forskellige beholdere (de to virksomheder).</span><span class="sxs-lookup"><span data-stu-id="d6338-129">If you use both Invoicing and [!INCLUDE[d365fin](includes/d365fin_md.md)], the data is stored in two different containers (the two companies).</span></span> <span data-ttu-id="d6338-130">Intet deles, så du skal administrere kunder og varer i begge virksomheder.</span><span class="sxs-lookup"><span data-stu-id="d6338-130">Nothing is shared, so you'll have to manage customers and items in both companies.</span></span>  

## <a name="see-also"></a><span data-ttu-id="d6338-131">Se også</span><span class="sxs-lookup"><span data-stu-id="d6338-131">See Also</span></span>
[<span data-ttu-id="d6338-132">Ofte stillede spørgsmål</span><span class="sxs-lookup"><span data-stu-id="d6338-132">Frequently Asked Questions</span></span>](across-faq.md)  
[<span data-ttu-id="d6338-133">Installation og administration</span><span class="sxs-lookup"><span data-stu-id="d6338-133">Setup and Administration</span></span>](admin-setup-and-administration.md)  
