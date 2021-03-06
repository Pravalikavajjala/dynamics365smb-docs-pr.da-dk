---
title: Oprette foretrukne metoder til at sende salgsdokumenter | Microsoft Docs
description: Bruges til at oprette hver debitors foretrukne metode til at sende salgsdokumenter, f.eks. e-mail, PDF-fil, elektronisk dokument osv.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: email, PDF, electronic document
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7f7499e6e501207ed5fd6ebbee5b94d18c1d008e
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-document-sending-profiles"></a>Fremgangsmåde: Konfigurere dokumentafsendelsesprofiler
Du kan oprette hver debitor med en foretrukken metode til afsendelse af salgsdokumenter, så du ikke behøver at vælge en afsendelsesindstilling, hver gang du vælger handlingen **Bogfør og send**.

I vinduet **Profiler for afsendelse af dokumenter** skal du oprette forskellige afsendelsesprofiler, som du kan vælge i feltet **Dokumentafsendelsesprofil** på et debitorkort. Du kan markere afkrydsningsfeltet **Standard** for at angive, at dokumentafsendelsesprofilen er standardprofilen for alle debitorer, bortset fra debitorer, hvor feltet **Dokumentafsendelsesprofil** er udfyldt med en anden afsendelsesprofil.

Når du vælger handlingen **Bogfør og send** i et salgsdokument, viser dialogboksen **Bekræftelse af bogfør og send** den afsendelsesprofil, der bruges, enten den, der er konfigureret for kunden, eller standard for alle debitorer. Du kan ændre afsendelsesprofil for salgsdokumentet i dialogboksen. Du kan finde flere oplysninger under [Fremgangsmåde: Fakturere salg](sales-how-invoice-sales.md).

## <a name="to-set-up-a-document-sending-profile"></a>Sådan konfigurerer du dokumentafsendelsesprofil
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Dokumentafsendelsesprofiler**, og vælg derefter det relaterede link.
2. I vinduet **Dokumentafsendelsesprofil** skal du vælge handlingen **Ny**.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a>Angive en afsendelsesprofil på et debitorkort
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Debitorer**, og vælg derefter det relaterede link.
2. Åbn kortet for den debitor, som du vil angive en afsendelsesprofil for.
3. I feltet **Dokumentafsendelsesprofil** skal du vælge en profil, du har konfigureret som beskrevet ovenfor.

## <a name="see-also"></a>Se også
[Konfigurere salg](sales-setup-sales.md)  
[Salg](sales-manage-sales.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

