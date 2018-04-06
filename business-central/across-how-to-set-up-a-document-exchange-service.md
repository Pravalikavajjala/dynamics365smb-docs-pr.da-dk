---
title: "Sådan konfigureres en dokumentudvekslingstjeneste | Microsoft Docs"
description: Du kan bruge en ekstern tjenesteudbyder til at udveksle elektroniske dokumenter med dine handelspartnere.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 043034d281eb4b58fab8ab4344987d5d3ca5f494
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-a-document-exchange-service"></a><span data-ttu-id="276ac-103">Konfigurere en dokumentudvekslingstjeneste</span><span class="sxs-lookup"><span data-stu-id="276ac-103">Set Up a Document Exchange Service</span></span>
<span data-ttu-id="276ac-104">Du kan bruge en ekstern tjenesteudbyder til at udveksle elektroniske dokumenter med dine handelspartnere.</span><span class="sxs-lookup"><span data-stu-id="276ac-104">You use an external service provider to exchange electronic documents with your trading partners.</span></span> <span data-ttu-id="276ac-105">Du kan finde flere oplysninger under [Udveksle data elektronisk](across-data-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="276ac-105">For more information, see [Exchanging Data Electronically](across-data-exchange.md).</span></span>  

## <a name="to-set-up-a-document-exchange-service"></a><span data-ttu-id="276ac-106">Sådan konfigureres en dokumentudvekslingstjeneste</span><span class="sxs-lookup"><span data-stu-id="276ac-106">To set up a document exchange service</span></span>  
1. <span data-ttu-id="276ac-107">Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Opsætning af dok.udv.tjen.**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="276ac-107">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Doc. Exch. Service Setup**, and then choose the related link.</span></span>  
2. <span data-ttu-id="276ac-108">Udfyld felterne som beskrevet i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="276ac-108">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="276ac-109">Felt</span><span class="sxs-lookup"><span data-stu-id="276ac-109">Field</span></span>|<span data-ttu-id="276ac-110">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="276ac-110">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="276ac-111">**Brugeragent**</span><span class="sxs-lookup"><span data-stu-id="276ac-111">**User Agent**</span></span>|<span data-ttu-id="276ac-112">Skriv en tekst, der kan bruges til at identificere din virksomhed i dokumentudvekslingsprocesser.</span><span class="sxs-lookup"><span data-stu-id="276ac-112">Enter any text that can be used to identify your company in document exchange processes.</span></span>|  
    |<span data-ttu-id="276ac-113">**Lejer-id for dok.udv.**</span><span class="sxs-lookup"><span data-stu-id="276ac-113">**Doc. Exch. Tenant ID**</span></span>|<span data-ttu-id="276ac-114">Angiv lejeren i dokumentudvekslingstjenesten, der repræsenterer din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="276ac-114">Enter the tenant in the document exchange service that represents your company.</span></span> <span data-ttu-id="276ac-115">Den leveres af udbyderen af dokumentudvekslingstjenesten.</span><span class="sxs-lookup"><span data-stu-id="276ac-115">This is provided by the document exchange service provider.</span></span>|  
    |<span data-ttu-id="276ac-116">**Aktiveret**</span><span class="sxs-lookup"><span data-stu-id="276ac-116">**Enabled**</span></span>|<span data-ttu-id="276ac-117">Angiv, om tjenesten er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="276ac-117">Specify if the service is enabled.</span></span> <span data-ttu-id="276ac-118">**Bemærk:** Når du har aktiveret tjenesten, oprettes der mindst to opgavekøposter til behandling af den elektroniske dokumenttrafik ind og ud af [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="276ac-118">**Note:**  As soon as you enable the service, at least two job queue entries are created to process the traffic of electronic documents in and out of [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="276ac-119">Når du deaktiverer tjenesten, slettes posterne i opgavekøen.</span><span class="sxs-lookup"><span data-stu-id="276ac-119">When you disable the service, the job queue entries are deleted.</span></span>|  
    |<span data-ttu-id="276ac-120">**URL-adresse til tilmelding**</span><span class="sxs-lookup"><span data-stu-id="276ac-120">**Signup URL**</span></span>|<span data-ttu-id="276ac-121">Angiv den webside, hvor du tilmelder dig dokumentudvekslingstjenesten.</span><span class="sxs-lookup"><span data-stu-id="276ac-121">Specify the web page where you sign up for the document exchange service.</span></span>|  
    |<span data-ttu-id="276ac-122">**URL-adresse for tjeneste**</span><span class="sxs-lookup"><span data-stu-id="276ac-122">**Service URL**</span></span>|<span data-ttu-id="276ac-123">Angiv adressen på den dokumentudvekslingstjeneste, som bliver kaldt, når du sender og modtager elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="276ac-123">Specify the address of the document exchange service, which will be called when you send and receive electronic documents.</span></span>|  
    |<span data-ttu-id="276ac-124">**URL-adresse til logon**</span><span class="sxs-lookup"><span data-stu-id="276ac-124">**Login URL**</span></span>|<span data-ttu-id="276ac-125">Angiv logonsiden for dokumentudvekslingstjenesten, hvor du angiver virksomhedens brugernavn og adgangskode for at logge på tjenesten.</span><span class="sxs-lookup"><span data-stu-id="276ac-125">Specify the logon page for the document exchange service, which is where you enter your company’s user name and password to log on to the service.</span></span>|  
    |<span data-ttu-id="276ac-126">**Forbrugernøgle**</span><span class="sxs-lookup"><span data-stu-id="276ac-126">**Consumer Key**</span></span>|<span data-ttu-id="276ac-127">Angiv trebenede OAuth-nøgle til forbrugernøglen.</span><span class="sxs-lookup"><span data-stu-id="276ac-127">Enter the 3-legged OAuth key for the consumer key.</span></span> <span data-ttu-id="276ac-128">Den leveres af udbyderen af dokumentudvekslingstjenesten.</span><span class="sxs-lookup"><span data-stu-id="276ac-128">This is provided by the document exchange service provider.</span></span>|  
    |<span data-ttu-id="276ac-129">**Forbrugerhemmelighed**</span><span class="sxs-lookup"><span data-stu-id="276ac-129">**Consumer Secret**</span></span>|<span data-ttu-id="276ac-130">Angiv den hemmelighed, der beskytter forbrugernøglen.</span><span class="sxs-lookup"><span data-stu-id="276ac-130">Enter the secret that protects the consumer key.</span></span> <span data-ttu-id="276ac-131">Den leveres af udbyderen af dokumentudvekslingstjenesten.</span><span class="sxs-lookup"><span data-stu-id="276ac-131">This is provided by the document exchange service provider.</span></span>|  
    |<span data-ttu-id="276ac-132">**Token**</span><span class="sxs-lookup"><span data-stu-id="276ac-132">**Token**</span></span>|<span data-ttu-id="276ac-133">Angiv den trebenede OAuth-nøgle for tokenet.</span><span class="sxs-lookup"><span data-stu-id="276ac-133">Enter the 3-legged OAuth key for the token.</span></span> <span data-ttu-id="276ac-134">Den leveres af udbyderen af dokumentudvekslingstjenesten.</span><span class="sxs-lookup"><span data-stu-id="276ac-134">This is provided by the document exchange service provider.</span></span>|  
    |<span data-ttu-id="276ac-135">**Tokenhemmelighed**</span><span class="sxs-lookup"><span data-stu-id="276ac-135">**Token Secret**</span></span>|<span data-ttu-id="276ac-136">Angiv den hemmelighed, der beskytter tokenet.</span><span class="sxs-lookup"><span data-stu-id="276ac-136">Enter the secret that protects the token.</span></span> <span data-ttu-id="276ac-137">Den leveres af udbyderen af dokumentudvekslingstjenesten.</span><span class="sxs-lookup"><span data-stu-id="276ac-137">This is provided by the document exchange service provider.</span></span>|  

> [!NOTE]  
>  <span data-ttu-id="276ac-138">Det anbefales, at du beskytter de logonoplysninger, du angiver i vinduet **Opsætning af VAN-tjeneste**.</span><span class="sxs-lookup"><span data-stu-id="276ac-138">It is recommended that you protect the logon information that you enter in the **VAN Service Setup** window.</span></span> <span data-ttu-id="276ac-139">Du kan kryptere data på serveren ved at oprette nye eller importere eksisterende krypteringsnøgler, som du aktiverer på den serverforekomst, som opretter forbindelse til databasen.</span><span class="sxs-lookup"><span data-stu-id="276ac-139">You can encrypt data on the server by generating new or importing existing encryption keys that you enable on the server instance that connects to the database.</span></span> <span data-ttu-id="276ac-140">Dette beskrives i følgende fremgangsmåde:</span><span class="sxs-lookup"><span data-stu-id="276ac-140">This is described in the following procedure.</span></span>  

## <a name="to-encrypt-your-logon-information"></a><span data-ttu-id="276ac-141">Sådan krypterer du logonoplysningerne</span><span class="sxs-lookup"><span data-stu-id="276ac-141">To encrypt your logon information</span></span>  
1. <span data-ttu-id="276ac-142">I vinduet **Opsætning af VAN-tjeneste** skal du vælge handlingen **Administration af kryptering**.</span><span class="sxs-lookup"><span data-stu-id="276ac-142">In the **VAN Service Setup** window, choose the **Encryption Management** action.</span></span>  
2. <span data-ttu-id="276ac-143">Aktiver kryptering af dine data i vinduet **Administration af datakryptering**.</span><span class="sxs-lookup"><span data-stu-id="276ac-143">In the **Data Encryption Management** window, enable encryption of your data.</span></span> <!--For more information, see [Manage Data Encryption](../manage-data-encryption.md).-->  

## <a name="see-also"></a><span data-ttu-id="276ac-144">Se også</span><span class="sxs-lookup"><span data-stu-id="276ac-144">See Also</span></span>  
[<span data-ttu-id="276ac-145">Konfigurere dataudveksling</span><span class="sxs-lookup"><span data-stu-id="276ac-145">Setting Up Data Exchange</span></span>](across-set-up-data-exchange.md)  
[<span data-ttu-id="276ac-146">Udveksle data elektronisk</span><span class="sxs-lookup"><span data-stu-id="276ac-146">Exchanging Data Electronically</span></span>](across-data-exchange.md)
