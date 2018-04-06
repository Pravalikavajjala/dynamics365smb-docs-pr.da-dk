---
title: Konfigurere virksomhedskonfiguration | Microsoft dokumenter
description: "Implementeringsprocessen, der begynder med Business Central-løsningen, kræver. Du kan samle alle disse oplysninger i konfigurationspakker."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 518acdc1733a526f1b0b4c5caa3a7644d762b72c
ms.contentlocale: da-dk
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-company-configuration"></a><span data-ttu-id="94cf1-104">Konfigurere virksomhedskonfiguration</span><span class="sxs-lookup"><span data-stu-id="94cf1-104">Set Up Company Configuration</span></span>
<span data-ttu-id="94cf1-105">Implementeringsprocessen, der begynder med Microsoft-partneren.</span><span class="sxs-lookup"><span data-stu-id="94cf1-105">The implementation process begins with the Microsoft partner.</span></span> <span data-ttu-id="94cf1-106">Partneren er ansvarlig for at gennemtænke konfigurationsdetaljerne og oprettelse af en pakke, der let kan anvendes af en kunde.</span><span class="sxs-lookup"><span data-stu-id="94cf1-106">The partner is responsible for thinking through the configuration details and creating a package that a customer can easily apply.</span></span> <span data-ttu-id="94cf1-107">Før du opretter en ny virksomhed, skal du planlægge, hvordan den konfigureres.</span><span class="sxs-lookup"><span data-stu-id="94cf1-107">Before you create a new company, you should plan how it will be configured.</span></span> <span data-ttu-id="94cf1-108">Du skal overveje grundlæggende konfigurationsdata og de datatyper, som din [!INCLUDE[d365fin](includes/d365fin_md.md)]-løsning kræver.</span><span class="sxs-lookup"><span data-stu-id="94cf1-108">You must consider basic setup data and the types of data that your [!INCLUDE[d365fin](includes/d365fin_md.md)] solution will require.</span></span> <span data-ttu-id="94cf1-109">Du kan samle alle disse oplysninger i konfigurationspakker.</span><span class="sxs-lookup"><span data-stu-id="94cf1-109">You bundle all of this information in configuration packages.</span></span>

<span data-ttu-id="94cf1-110">RapidStart Services giver dig også de værktøjer, du skal bruge til at overflytte ældre data, f.eks. kunder og kreditorer.</span><span class="sxs-lookup"><span data-stu-id="94cf1-110">RapidStart Services also provides you with the tools that you will use to migrate your legacy data, such as customers and vendors.</span></span>  

<span data-ttu-id="94cf1-111">Vi anbefaler, at du opretter konfigurationspakker med de fleste af de konfigurationstabeller, som allerede udfyldt, så kunder behøver kun at ændre nogle få indstillinger, når pakken er installeret.</span><span class="sxs-lookup"><span data-stu-id="94cf1-111">We recommend that you create configuration packages with most of the setup tables already filled in, so that customers only have to change a few settings after the package is applied.</span></span> <span data-ttu-id="94cf1-112">Når du f.eks. opretter en ny virksomhed, udfyldes tabellerne **Nummerserie** og **Nummerserielinje**, med et sæt nummerserie og starttal.</span><span class="sxs-lookup"><span data-stu-id="94cf1-112">For example, when you create a new company, the **No. Series** and the **No. Series Line** tables are filled in with a set of number series and starting numbers.</span></span> <span data-ttu-id="94cf1-113">De tilsvarende **Nummerserie**-felter i opsætningstabellerne udfyldes også automatisk.</span><span class="sxs-lookup"><span data-stu-id="94cf1-113">The corresponding **No. Series** fields in the setup tables are also filled in automatically.</span></span> <span data-ttu-id="94cf1-114">Du behøver ikke at indtaste nummerserier og andre grundlæggende opsætningsdata.</span><span class="sxs-lookup"><span data-stu-id="94cf1-114">You do not have to do the work of entering number series and other basic setup data.</span></span> <span data-ttu-id="94cf1-115">Du kan også manuelt ændre alle standarddata, der bruges med RapidStart Services ved at bruge konfigurationsregnearket.</span><span class="sxs-lookup"><span data-stu-id="94cf1-115">You can also manually change all default data that is used with RapidStart Services by using the configuration worksheet.</span></span>  

<span data-ttu-id="94cf1-116">Konfigurationspakkerne bygger på en forudkonfigureret virksomhed.</span><span class="sxs-lookup"><span data-stu-id="94cf1-116">The configuration packages are built on a preconfigured company.</span></span> <span data-ttu-id="94cf1-117">Når du har konfigureret en virksomhed, der opfylder dine behov, kan du oprette en konfigurationspakke, der indeholder relevante data fra denne virksomhed.</span><span class="sxs-lookup"><span data-stu-id="94cf1-117">After you have set up a company that meets your needs, you can create a configuration package that contains relevant data from this company.</span></span> <span data-ttu-id="94cf1-118">Du kan derefter oprette en ny virksomhed, der skal konfigureres på samme måde.</span><span class="sxs-lookup"><span data-stu-id="94cf1-118">You can then use it when you create a new company that is to be configured in the same way.</span></span>  

<span data-ttu-id="94cf1-119">Som en hjælp til at importere masterdata, f.eks. debitor- og kreditoroplysninger, kan du bruge konfigurationsskabeloner.</span><span class="sxs-lookup"><span data-stu-id="94cf1-119">To facilitate the import of master data, such as customer and vendor information, you can use configuration templates.</span></span> <span data-ttu-id="94cf1-120">Konfigurationsskabeloner indeholder et sæt standardindstillinger, der automatisk tildeles de poster, der importeres til [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="94cf1-120">Configuration templates contain a set of default settings that are automatically assigned to the records imported into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

<span data-ttu-id="94cf1-121">Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.</span><span class="sxs-lookup"><span data-stu-id="94cf1-121">The following table describes a sequence of tasks with links to topics that describe them.</span></span>

|<span data-ttu-id="94cf1-122">**For at**</span><span class="sxs-lookup"><span data-stu-id="94cf1-122">**To**</span></span>|<span data-ttu-id="94cf1-123">**Skal du se**</span><span class="sxs-lookup"><span data-stu-id="94cf1-123">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="94cf1-124">Planlægge en virksomhedskonfiguration ved at udfylde konfigurationsarket.</span><span class="sxs-lookup"><span data-stu-id="94cf1-124">Plan a company configuration by filling in the configuration worksheet.</span></span>|[<span data-ttu-id="94cf1-125">Administrere virksomhedskonfigurationen i et regneark</span><span class="sxs-lookup"><span data-stu-id="94cf1-125">Manage Company Configuration in a Worksheet</span></span>](admin-how-to-manage-company-configuration-in-a-worksheet.md)|  
|<span data-ttu-id="94cf1-126">Oprette en konfigurationspakke, tilpasse en pakke, tildele tabeller til en pakke, gennemse eller redigere eksisterende debitordata, oprette den nye virksomhed og derefter flytte testdata til produktionsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="94cf1-126">Create a configuration package, customize a package, assign tables to a package, review or edit existing customer data, create the new company and then move test data to the production environment.</span></span>|[<span data-ttu-id="94cf1-127">Forberede en konfigurationspakke</span><span class="sxs-lookup"><span data-stu-id="94cf1-127">Prepare a Configuration Package</span></span>](admin-how-to-prepare-a-configuration-package.md)| 

## <a name="see-also"></a><span data-ttu-id="94cf1-128">Se også</span><span class="sxs-lookup"><span data-stu-id="94cf1-128">See Also</span></span>  
[<span data-ttu-id="94cf1-129">Oprette en virksomhed med RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="94cf1-129">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="94cf1-130">Opsætning</span><span class="sxs-lookup"><span data-stu-id="94cf1-130">Administration</span></span>](admin-setup-and-administration.md)
