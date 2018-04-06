---
title: "Sådan sammenkædes poster med eksterne oplysninger eller programmer | Microsoft Docs"
description: "Indsæt et hyperlink i et dokument eller websted til en bestemt post, f.eks. en debitor eller et dokument."
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: a513f6e62c4ef8dcf9e484d0211feb3e857dc0f7
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="adding-links-to-websites-documents-or-programs-on-records"></a><span data-ttu-id="dae84-103">Sådan føjes links til websteder, dokumenter eller programmer på poster</span><span class="sxs-lookup"><span data-stu-id="dae84-103">Adding Links to Websites, Documents, or Programs on Records</span></span>
<span data-ttu-id="dae84-104">På en bestemt post, f.eks. en debitor, et dokument eller en salgsordre, kan du tilføje et link til et eksternt dokument, websted eller program.</span><span class="sxs-lookup"><span data-stu-id="dae84-104">On a specific record, such as a customer, document, or sales order, you can add a link to an external document, website, or program.</span></span> <span data-ttu-id="dae84-105">Det kan også være, at du ønsker et link, der åbner en ny tom mail til en bestemt modtager, når du vælger det.</span><span class="sxs-lookup"><span data-stu-id="dae84-105">Or, you may want a link that opens a new empty email to a specific recipient when you select it.</span></span> <span data-ttu-id="dae84-106">På kortsiden på nogle poster, f.eks. debitor- og kreditorkort, er der et felt **Hjemmeside**, hvor du kan angive en URL-adresse (internetadresse).</span><span class="sxs-lookup"><span data-stu-id="dae84-106">The card page for some records, such as customer and vendor cards, include a **Home Page** field where you can enter an Internet address (URL).</span></span> <span data-ttu-id="dae84-107">Hvis du vil medtage andre links, kan du bruge den metode, der er beskrevet i denne artikel.</span><span class="sxs-lookup"><span data-stu-id="dae84-107">To include other links, you can use the method described in this article.</span></span>

<span data-ttu-id="dae84-108">Et andet eksempel kan være, når du modtager en trykt faktura fra kreditorer.</span><span class="sxs-lookup"><span data-stu-id="dae84-108">Another example could be when you receive printed invoices from vendors.</span></span> <span data-ttu-id="dae84-109">Du kan scanne den og gemme den som en .pdf-fil på et SharePoint-websted.</span><span class="sxs-lookup"><span data-stu-id="dae84-109">You can scan them and store them as .pdf files on a SharePoint site.</span></span> <span data-ttu-id="dae84-110">Derefter kan du oprette et link fra en købsfaktura i [!INCLUDE[d365fin_md](includes/d365fin_md.md)] til den tilsvarende faktura i SharePoint.</span><span class="sxs-lookup"><span data-stu-id="dae84-110">Then you can make a link from a purchase invoice in [!INCLUDE[d365fin_md](includes/d365fin_md.md)] to the corresponding invoice on  SharePoint.</span></span> <span data-ttu-id="dae84-111">Eller du kan oprette et link fra et varekort til den tilsvarende side i kreditorens onlinekatalog.</span><span class="sxs-lookup"><span data-stu-id="dae84-111">Or, you can make a link from an item card to the corresponding page in your vendor's online catalog.</span></span>

## <a name="to-add-a-link-on-a-record"></a><span data-ttu-id="dae84-112">Sådan tilføjes et link til en post</span><span class="sxs-lookup"><span data-stu-id="dae84-112">To add a link on a record</span></span>   

1.  <span data-ttu-id="dae84-113">Åbn den post, du vil oprette linket til, f.eks. et debitorkort eller en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="dae84-113">Open the record that you want to attach the link to, such as a customer card or sales order.</span></span> <span data-ttu-id="dae84-114">Hvis linket skal knyttes til en bestemt linje, f.eks. en kladdelinje, skal du placere markøren på linjen.</span><span class="sxs-lookup"><span data-stu-id="dae84-114">If you want to attach the link to a specific line, such as a journal line, select the line.</span></span>  

2.  <span data-ttu-id="dae84-115">Vælg handlingen **Links** for at åbne vinduerne **Links**, der viser de aktuelle kæder, der føjes til posten.</span><span class="sxs-lookup"><span data-stu-id="dae84-115">Choose the **Links** action to open the **Links** windows that shows all the current links that are added to the record.</span></span>

3. <span data-ttu-id="dae84-116">Hvis du vil tilføje et nyt link, skal du vælge **+ny**.</span><span class="sxs-lookup"><span data-stu-id="dae84-116">To add a new link, choose **+new**.</span></span>

4.  <span data-ttu-id="dae84-117">I feltet **Hyperlinkadresse** skal du angive</span><span class="sxs-lookup"><span data-stu-id="dae84-117">In the **Link Address** field, enter</span></span>

    -   <span data-ttu-id="dae84-118">Hvis du vil sammenkæde med en fil på din computer eller dit netværk, skal du angive den fulde sti og filnavn, f.eks. **C: Min dokumentfaktura1.doc**.</span><span class="sxs-lookup"><span data-stu-id="dae84-118">To link to a file on your computer or network, enter the full path and file name, such as  **C:My Documentsinvoice1.doc**.</span></span>
    -   <span data-ttu-id="dae84-119">Hvis du vil sammenkæde med et websted, skal du angive URL-adressen (internetadressen), f.eks. **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="dae84-119">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span>
    -   <span data-ttu-id="dae84-120">Hvis du vil sammenkæde med et websted, skal du angive URL-adressen (internetadressen), f.eks. **www.microsoft.com**.</span><span class="sxs-lookup"><span data-stu-id="dae84-120">To link to website, enter the Internet address (URL), such as **www.microsoft.com**.</span></span>
    -   <span data-ttu-id="dae84-121">Hvis du vil sammenkæde med et program, skal du angive en bestemt streng for at åbne programmet.</span><span class="sxs-lookup"><span data-stu-id="dae84-121">To link to a program, enter a specific string to open the program.</span></span> <span data-ttu-id="dae84-122">Hvis du f.eks. vil åbne OneNote med en bestemt side, skal du angive **onenote:///C:Min dokumenttest.one**.</span><span class="sxs-lookup"><span data-stu-id="dae84-122">For example, to open OneNote with a specific page, enter **onenote:///C:My Documentstest.one**.</span></span> <span data-ttu-id="dae84-123">Eller hvis du vil åbne Outlook med en ny tom mail til et bestemt alias, skal du angive **mailto:testalias**.</span><span class="sxs-lookup"><span data-stu-id="dae84-123">Or, to open Outlook with a new empty email to a specific alias, enter **mailto:testalias**.</span></span>  

5.  <span data-ttu-id="dae84-124">Angiv oplysninger om linket i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="dae84-124">Fill in the **Description** field with information about the link.</span></span>  

6.  <span data-ttu-id="dae84-125">Vælg knappen **Gem**.</span><span class="sxs-lookup"><span data-stu-id="dae84-125">Choose the **Save** button.</span></span>  

## <a name="to-delete-a-link-from-a-record"></a><span data-ttu-id="dae84-126">Sådan slettes et link fra en post</span><span class="sxs-lookup"><span data-stu-id="dae84-126">To delete a link from a record</span></span>  

<span data-ttu-id="dae84-127">Hvis du vil slette et link, kan du i vinduet **Links** vælge **...** og derefter **Slet**.</span><span class="sxs-lookup"><span data-stu-id="dae84-127">To delete a link, in the **Links** window, you can select **...** and then **Delete**.</span></span>

<span data-ttu-id="dae84-128">Hvis du sletter en enkelt post, f.eks. en salgsordrelinje, en salgsordre eller en debitor, så slettes alle links med tilknytning til denne post.</span><span class="sxs-lookup"><span data-stu-id="dae84-128">If you delete a single record, such as a sales order line, a sales order, or a customer, then all the links attached to the record are deleted.</span></span> <span data-ttu-id="dae84-129">Men hvis du sletter poster med en kørsel, f.eks. kørslen **Slet fakturerede salgsordrer**, så lagres linksene stadig i databasen.</span><span class="sxs-lookup"><span data-stu-id="dae84-129">However, if you delete records using a batch job, such as the **Delete Invoiced Sales Orders** batch job, then the links are still stored in the database.</span></span> <span data-ttu-id="dae84-130">Hvis du vil slette linkene fra databasen, skal du køre codeunit **Slet underordnede postlinks**.</span><span class="sxs-lookup"><span data-stu-id="dae84-130">To delete the links from the database, run the **Delete Orphaned Record Links** codeunit.</span></span> <span data-ttu-id="dae84-131">For at gøre dette skal du vælge ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angive **Slet fakturerede købsreturvareordrer** og derefter vælge det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="dae84-131">To do this, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Delete Orphaned Record Links**, and then choose the related link.</span></span>   

<!-- ### To run delete orphaned record links  

1.  Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Data Deletion**, and then choose the related link.  

2.  On the **Data Deletion** page, choose **Tasks**, and then choose **Delete Orphaned Record Links**.  -->

## <a name="see-also"></a><span data-ttu-id="dae84-132">Se også</span><span class="sxs-lookup"><span data-stu-id="dae84-132">See Also</span></span>  
<span data-ttu-id="dae84-133">[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="dae84-133">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
