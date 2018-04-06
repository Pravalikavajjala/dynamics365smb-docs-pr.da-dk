---
title: Definere forretningsrelationskode for kontakter | Microsoft Docs
description: "Brug forretningsrelationer i Business Central til at hjælpe med marketing og til at angive det forretningsforhold, som findes mellem din virksomhed og dine kundeemner og kunder, f.eks. en bank eller serviceleverandør."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f879d933822e061913975c1dbac2bf883ad9bbc1
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-business-relations-on-contact-companies"></a><span data-ttu-id="7fb4e-103">Opsætning af forretningsrelationer i kontaktvirksomheder</span><span class="sxs-lookup"><span data-stu-id="7fb4e-103">Setting Up Business Relations on Contact Companies</span></span>
<span data-ttu-id="7fb4e-104">Du kan bruge forretningsrelationer til at angive det forretningsforhold, som findes mellem din virksomhed og dine kontakter, f.eks. et kundeemne, bank, konsulent, serviceleverandør osv.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-104">You can use business relations to indicate the business relationship you have with your contacts, for example, a prospect, bank, consultant, service supplier, and so on.</span></span>

<span data-ttu-id="7fb4e-105">Brug af forretningsrelationer i kontakter er en totrinsproces.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-105">Using business relations on contacts is a two-step process.</span></span> <span data-ttu-id="7fb4e-106">Først skal du definere koden for forretningsrelationen.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-106">First, you define the business relation code.</span></span> <span data-ttu-id="7fb4e-107">Du behøver kun at udføre dette trin én gang for hver forretningsrelation.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-107">You only have to perform this step one time for each business relation.</span></span> <span data-ttu-id="7fb4e-108">Når du har en forretningsrelationskode, kan du begynde at tildele koden til kontaktvirksomheder.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-108">Once you have a business relation code, you can start to assign the code to contact companies.</span></span>

> [!NOTE]  
>   <span data-ttu-id="7fb4e-109">Hvis du har planer om at synkronisere kontakter med kreditorer, debitorer eller bankkonti i andre dele af programmet, kan det være en god idé at definere forretningsrelationer for dem.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-109">If you plan to synchronize your contacts with vendors, customers, or bank accounts in other parts of the application, you may want to set up a business relation for them.</span></span>

## <a name="to-define-a-business-relation-code"></a><span data-ttu-id="7fb4e-110">Sådan defineres en forretningsrelationskode</span><span class="sxs-lookup"><span data-stu-id="7fb4e-110">To define a business relation code</span></span>
<span data-ttu-id="7fb4e-111">Forretningsrelationskoden definerer en kategori eller type af forretningsrelation, f.eks BANK eller Law.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-111">The business relation code defines a category or type of the business relationship, such as BANK or Law.</span></span> <span data-ttu-id="7fb4e-112">Du kan have flere forretningsrelationskoder.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-112">You can have several business relation codes.</span></span> <span data-ttu-id="7fb4e-113">Du kan definere forretningsrelationen fra vinduet **Forretningsrelationer**.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-113">To define the business relation, you use the **Business Relations** window.</span></span>

1. <span data-ttu-id="7fb4e-114">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Forretningsrelationer**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Business Relations**, and then choose the related link.</span></span>
2. <span data-ttu-id="7fb4e-115">Vælg handlingen **Ny**, og indtast en kode og beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-115">Choose the **New** action, and fill in a code and description.</span></span> <span data-ttu-id="7fb4e-116">Du kan bruge op til 11 tegn til koden, som skal være en kombination af tal og bogstaver.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-116">The code can be a maximum of 11 characters, and can be any combination of numbers and letters.</span></span>

## <a name="AssignBusRelContact"></a> <span data-ttu-id="7fb4e-117">Sådan tildeles forretningsrelationer til en kontakt</span><span class="sxs-lookup"><span data-stu-id="7fb4e-117">To assign business relations to a contact</span></span>
<span data-ttu-id="7fb4e-118">Du kan ikke tildele forretningsrelationer til en kontaktperson – kun til virksomheder.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-118">You cannot assign business relations to a contact person - only companies.</span></span>

1. <span data-ttu-id="7fb4e-119">Åbn kontakten.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-119">Open the contact.</span></span>
2. <span data-ttu-id="7fb4e-120">Vælg handlingen **Virksomhed**, og vælg derefter handlingen **Forretningsrelationer**.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-120">Choose the **Company** action, and then the **Business Relations** action.</span></span>

    <span data-ttu-id="7fb4e-121">Vinduet **Kontakt til forretningsrelation** åbnes.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-121">The **Contact Business Relations** window opens.</span></span>
3. <span data-ttu-id="7fb4e-122">I feltet **Forretningsrelationskode** skal du vælge den forretningsrelation, du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-122">In the **Business Relation Code** field, select the business relation you want to assign.</span></span>

<span data-ttu-id="7fb4e-123">Gentag disse trin for hver forretningsrelation, du vil tildele.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-123">Repeat these steps to assign as many business relations as you want.</span></span> <span data-ttu-id="7fb4e-124">Du kan også tildele forretningsrelationer fra kontaktoversigten ved at udføre samme procedure.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-124">You can also assign business relations from the contact list by following the same procedure.</span></span>

<span data-ttu-id="7fb4e-125">Det antal relationer, du har tildelt kontakten, vises i feltet **Antal forretningsrelationer** i sektionen **Segmentering** i vinduet **Kontakt**.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-125">The number of business relations you have assigned to the contact is displayed in the **No. of Business Relations** field in the **Segmentation** section in the **Contact** window.</span></span>

<span data-ttu-id="7fb4e-126">Når du har tildelt forretningsrelationer til kontakter, kan du bruge oplysningerne til at udvælge kontakter til dine målgrupper.</span><span class="sxs-lookup"><span data-stu-id="7fb4e-126">After you have assigned business relations to your contacts, you can use this information to select contacts for your segments.</span></span> <span data-ttu-id="7fb4e-127">Du kan finde flere oplysninger i [Tilføje kontakter til målgrupper](marketing-add-contact-segment.md).</span><span class="sxs-lookup"><span data-stu-id="7fb4e-127">For more information, see [Add Contacts to Segments](marketing-add-contact-segment.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7fb4e-128">Se også</span><span class="sxs-lookup"><span data-stu-id="7fb4e-128">See Also</span></span>
[<span data-ttu-id="7fb4e-129">Oprette kontaktvirksomheder</span><span class="sxs-lookup"><span data-stu-id="7fb4e-129">Creating Contact Companies</span></span>](marketing-create-contact-companies.md)  
<span data-ttu-id="7fb4e-130">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7fb4e-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
