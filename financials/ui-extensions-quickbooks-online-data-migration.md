---
title: "Bruge udvidelsen QuickBooks-overførsel | Microsoft Docs"
description: "Beskriver, hvordan du bruger udvidelsen til at overføre debitorer, kreditorer, varer og konti fra QuickBooks Online til Dynamics 365."
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: extension, migrate, data, QuickBooks, import
ms.date: 05/24/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: e73db91a37fd5aee249de032d231df2c5e36b4ba
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---

# <a name="the-quickbooks-online-data-migration-extension-for-dynamics-365-business-edition"></a>Udvidelsen QuickBooks Online-dataoverførsel til Dynamics 365 Business edition
Denne udvidelse er inkluderet i den assisterede opsætningsvejledning **Dataoverførsel** for at hjælpe dig med at overføre vigtige forretningsdata fra QuickBooks Online til [!INCLUDE[d365fin](includes/d365fin_md.md)]. F.eks. er dette nyttigt, når virksomheden vokser, og du har besluttet at opgradere din virksomheds administrationsapp ved at starte med at bruge [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="what-data-can-i-import-from-quickbooks-online"></a>Hvilke data kan jeg importere fra QuickBooks Online?
Du kan importere følgende data fra QuickBooks Online til [!INCLUDE[d365fin](includes/d365fin_md.md)]:  

* Kunder (Debitorer)
* Leverandører (Kreditorer)
* Varer
* Kontoplan
* Primosaldopostering i regnskabet
* Disponible antal for lagervarer
* Åbne dokumenter for debitorer og kreditorer, f.eks. fakturaer, kreditnotaer og betalinger

Vi overfører kun fulde beløb på salgs- og købsdokumenter. Delvist betalte beløb opdateres ikke. F.eks. hvis en debitor har indbetalt 300 af i alt 500 dollar på en salgsfaktura, overfører vi hele 500. Hvis du har modtaget delbetalinger, skal du opdatere dem manuelt, før eller efter at du overfører data. Det anbefales, at du anvender udestående transaktioner, inden du overfører, for at gøre tingene nemmere bagefter.

> [!NOTE]  
>   Vi overfører ikke indkøbsordrer eller salgsordrer.

## <a name="before-you-start"></a>Før du starter
Det er en vigtig del af overførslen at angive de konti, transaktioner skal overføres til. Det er en god ide at planlægge denne tilknytning, før du overfører data. F.eks. de konti, hvor du bogfører poster for:  

* Salget af varer eller servicer til debitorer.
* Køb af varer eller servicer fra kreditorer.  
* Ændringer i finansbogholderiet.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] kræver, at finanskonti har kontonumre tilknyttet. Sørg for, at kontonumre er tildelt til kontiene i QuickBooks Online.

Hvis der er transaktioner i QuickBooks Online, der har momsbeløb, du skal oprette en momskonto for dine skatteregioner i [!INCLUDE[d365fin](includes/d365fin_md.md)], før du kan bogføre transaktioner.

## <a name="how-do-i-start-using-the-extension"></a>Hvordan begynder jeg at bruge udvidelsen?
Det er nemt at komme i gang. Du skal blot køre den assisterede opsætningsvejledning **Dataoverførsel**. Sådan gør du:

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Assisteret opsætning**, og vælg derefter **Overflyt virksomhedsdata**.
2. Følg vejledningen på de enkelte trin i den assisterede opsætningsvejledning.

## <a name="what-do-i-do-after-i-migrate-data"></a>Hvad gør jeg gøre, når jeg har overført data?
Når du har overført data, har transaktioner status **Ikke-bogførte**, så du kan gennemgå dem og foretage ændringer. For at få vist transaktionerne skal du gå til siden, hvor du vil finde dem normalt. F.eks. for at få vist ikke-bogførte salgsfakturaer, skal du gå til siden **Salgsfakturaer**. For at få vist udbetalingskladder skal du gå til siden **Udbetalingskladder**.   

Der er især et par ting, du skal gøre:

* Hvis transaktioner i QuickBooks Online havde avance- eller rabatbeløb, skal du manuelt føje beløbene til de relaterede transaktioner i [!INCLUDE[d365fin](includes/d365fin_md.md)], før du bogfører dem.
* Hvis du bruger moms, skal du evt. tilføje en virksomhedsbogføringsgruppe og en produktbogføringsgruppe i bogføringsopsætningen, så du kan bogføre momsbeløb.
* Kontroller primosaldi for konti i finansbogholderiet. QuickBooks Online gemmer ikke den aktuelle saldo for alle konti, så det kan være nødvendigt at rette primosaldi.

## <a name="see-also"></a>Se også
[Importere virksomhedsdata fra andre økonomisystemer](upload-data.md)  
[Tilpasse [!INCLUDE[d365fin](includes/d365fin_md.md)] ved hjælp af udvidelser](ui-extensions.md)  

