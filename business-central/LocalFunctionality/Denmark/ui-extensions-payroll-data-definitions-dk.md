---
title: "Definitioner af løndata (DK) | Microsoft Docs"
description: "Denne udvidelse gør det nemt at udveksle data med løntjenesteudbydere i Danmark."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 04/23/2018
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: ba50e74b51148e42dd25752ade5a37d0e3285509
ms.openlocfilehash: 34065229f3833f8e957dcdc4c7c4796bcc4b1be5
ms.contentlocale: da-dk
ms.lasthandoff: 04/26/2018

---

# <a name="the-payroll-data-definitions-dk-extension"></a><span data-ttu-id="3f886-103">Udvidelsen Definitioner af løndata (DK)</span><span class="sxs-lookup"><span data-stu-id="3f886-103">The Payroll Data Definitions (DK) Extension</span></span>
<span data-ttu-id="3f886-104">Hvis dit firma bruger løntjenesteudbyderne Danløn, Dataløn, Lønservice, Multiløn eller Proløn i Danmark, kan udvidelsen Definitioner af løndata(DK) hjælpe dig med hurtigt og nøjagtigt at registrere løntransaktioner fra disse udbydere.</span><span class="sxs-lookup"><span data-stu-id="3f886-104">If your business uses the Danløn, Dataløn, Lønservice, Multiløn, or Proløn payroll service providers in Denmark, the Payroll Data Definitions (DK) extension can help you quickly and accurately register payroll transactions from these providers.</span></span> <span data-ttu-id="3f886-105">Udvidelsen indeholder dataudvekslingsdefinitioner, der gør det muligt at importere løntransaktioner i filer, som udbyderne sender til dig.</span><span class="sxs-lookup"><span data-stu-id="3f886-105">The extension contains data exchange definitions that enable you to import payroll transactions in files that the providers send to you.</span></span> <span data-ttu-id="3f886-106">Du kan finde flere oplysninger om dataudvekslingsdefinitioner under [Konfigurere dataudvekslingsdefinitioner](../../across-how-to-set-up-data-exchange-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="3f886-106">For more information about data exchange definitions, see [Set Up Data Exchange Definitions](../../across-how-to-set-up-data-exchange-definitions.md).</span></span>  

## <a name="getting-started"></a><span data-ttu-id="3f886-107">Introduktion</span><span class="sxs-lookup"><span data-stu-id="3f886-107">Getting Started</span></span>
<span data-ttu-id="3f886-108">Det første trin er at tilknytte de forskellige typer af løntransaktioner til de finanskonti, de skal bogføres på i Business Central.</span><span class="sxs-lookup"><span data-stu-id="3f886-108">The first step is to map the types of payroll transactions to the general ledger accounts that you want to post them to in Business Central.</span></span> <span data-ttu-id="3f886-109">Du kan f.eks. bogføre pensionsbidrag til en konto med navnet Pension, og afgifter, der er betalt som bidrag, til en konto med navnet Pensionsafgift.</span><span class="sxs-lookup"><span data-stu-id="3f886-109">For example, you might want to post retirement plan contributions to an account named Pension, and the taxes paid on the contributions to an account named Pension Tax.</span></span> <span data-ttu-id="3f886-110">Dette sker uden for Business Central, f.eks. kan du bruge et Excel-regneark til at visualisere tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="3f886-110">This happens outside of Business Central, for example, you might use an Excel worksheet to visualize the mapping.</span></span> <span data-ttu-id="3f886-111">Samarbejd med løntjenesteudbyderen for at sikre, at den fil, de eksporterer, indeholder tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="3f886-111">Work with the payroll service provider to ensure that the file they export contains the mapping.</span></span> <span data-ttu-id="3f886-112">Normalt kan du finde oplysninger om, hvordan du konfigurerer eksportfiler på udbyderens websted.</span><span class="sxs-lookup"><span data-stu-id="3f886-112">Typically, you can find information about how to configure export files on the provider's website.</span></span>

<span data-ttu-id="3f886-113">Når du har installeret udvidelsen, er det næste trin at angive formatet for løndatafilen fra løntjenesteudbyderen.</span><span class="sxs-lookup"><span data-stu-id="3f886-113">After you install the extension, the next step is to specify the format for the payroll data file from the payroll service provider.</span></span> <span data-ttu-id="3f886-114">Det gør du ved at gå til siden **Opsætning af Finans** og vælge udbyderen i feltet **Format til import af løntransaktion**.</span><span class="sxs-lookup"><span data-stu-id="3f886-114">To do that, go to the **General Ledger Setup** page and choose the provider in the **Payroll Trans. Import Format** field.</span></span> 

## <a name="how-to-import-a-payroll-file"></a><span data-ttu-id="3f886-115">Fremgangsmåde: Importere en lønfil</span><span class="sxs-lookup"><span data-stu-id="3f886-115">How to: Import a payroll file</span></span>
1.  <span data-ttu-id="3f886-116">Vælg ikonet ![Søg efter side eller rapport](../../media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Finanskladder**, og vælg derefter det relaterede link.</span><span class="sxs-lookup"><span data-stu-id="3f886-116">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journals**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="3f886-117">Vælg den kladde, du skal bruge, og brug derefter handlingen **Importér lønfil** for at indlæse datafilen fra løntjenesteudbyderen.</span><span class="sxs-lookup"><span data-stu-id="3f886-117">Choose the journal to use, and then use the **Import Payroll File** action to import the data file from the payroll service provider.</span></span> 

## <a name="see-also"></a><span data-ttu-id="3f886-118">Se også</span><span class="sxs-lookup"><span data-stu-id="3f886-118">See Also</span></span>
[<span data-ttu-id="3f886-119">Lokal funktionalitet for Danmark</span><span class="sxs-lookup"><span data-stu-id="3f886-119">Denmark Local Functionality</span></span>](denmark-local-functionality.md)  