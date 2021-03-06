---
title: Administrere lager | Microsoft Docs
description: "Bruges til at styre de fysiske produkter, som du handler med, f.eks. håndtering af lagerbeholdning på lagerstedet."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse, stock
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: c3cfae3d52cbb25882c5986ad4aedaef7939a8b6
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---

# <a name="inventory"></a>Lagerbeholdning
For hvert fysisk produkt, som du vil handle med, skal du oprette et varekort af typen **Lager**. De varer, du tilbyder kunderne, men ikke lagerfører, kan du registrere som katalogvarer, som du kan konvertere til lagervarer, når det er nødvendigt. Du kan øge eller mindske antallet af en vare på lager ved at bogføre direkte til vareposterne, f.eks. efter en fysisk optælling eller hvis du ikke registrerer indkøb.

Lagerforøgelser og -reduktioner registreres naturligt også, når du bogfører købs- og salgsdokumenter. Du kan finde flere oplysninger i [Fremgangsmåde: Registrere køb](purchasing-how-record-purchases.md) og [Fremgangsmåde: Sælge produkter](sales-how-sell-products.md) og [Fremgangsmåde: Fakturere salg](sales-how-invoice-sales.md). Overførsler mellem lokationer ændrer lagerbeholdningen på tværs af virksomhedens lagersteder.   

Hvis du vil øge dit overblik over varerne og lettere kunne finde dem, kan du kategorisere varer og give dem attributter, du kan søge og sortere efter.

> [!NOTE]
> Den fysiske håndtering af varer kaldes lageraktiviteter. Du kan finde flere oplysninger i [Logistik](warehouse-manage-warehouse.md).

## <a name="inventory-reconciliation"></a>Lagerafstemning
Når du bogfører lagertransaktioner, f.eks. salgsleverancer, købsfakturaer eller lagerreguleringer, registreres ændringen i varepriser i værdiposterne. For at afspejle ændringen af lagerværdien i dine finansielle regnskaber bogføres lagerværdien automatisk i de relaterede lagerkonti i finansbogholderiet. For hver lagertransaktion du bogfører, bogføres den relevante værdi på lagerkontoen, reguleringskontoen og vareforbrugskontoen i finansregnskabet. Du kan finde flere oplysninger i [Fremgangsmåde: Afstemme kostpriser med finansregnskabet](finance-how-to-post-inventory-costs-to-the-general-ledger.md).

Selvom lagerværdien automatisk bogføres i Finans, er det stadig nødvendigt at sikre, at værdien af varerne overføres til de relaterede udgående transaktioner, f.eks salg eller overflytninger. Dette er især vigtigt i de situationer, hvor du sælger varer, inden du fakturerer købet af varerne. Dette omtales som omkostningsregulering. Varepriser reguleres automatisk, når du bogfører transaktioner, men du kan også justere varepriser manuelt. Du kan finde flere oplysninger i [Fremgangsmåde: Regulere varepriser](inventory-how-adjust-item-costs.md).

|Hvis du vil |Se |
|---|----|
|Opret varekort for lagervarer, som du handler med.|[Fremgangsmåde: Registrere nye varer](inventory-how-register-new-items.md)|
|Strukturer overordnede varer, du sælger som pakker, der består af den overordnede vares komponenter eller af montage til ordre- eller montage til lager-pakker.|[Fremgangsmåde: Arbejde med styklister](inventory-how-work-BOMs.md)|
|Hav altid overblik over varer, og få hjælp til at finde og sortere varer ved at arrangere dem i kategorier.|[Fremgangsmåde: Kategorisere varer](inventory-how-categorize-items.md)|
|Tildel vareattributter af forskellige værdityper til dine varer for lettere at kunne sortere og finde varer.|[Fremgangsmåde: Arbejde med vareattributter](inventory-how-work-item-attributes.md)|
|Opret særlige varekort for de varer, du tilbyder kunderne, men ikke lagerfører.|[Fremgangsmåde: Arbejde med katalogvarer](inventory-how-work-nonstock-items.md)|
|Foretag fysisk optælling, foretag negative eller positive reguleringer, og rediger oplysninger, f.eks. placering eller lotnummer, på vareposter.|[Fremgangsmåde: Tælle, justere og ompostere lager](inventory-how-count-adjust-reclassify.md)|
|Få vist tilgængeligheden af varer pr. lokation og pr. periode efter salgs- eller købshændelse eller efter deres brug i montage- eller produktionsstyklister.|[Sådan gør du: Vise varedisponering](inventory-how-availability-overview.md)|
|Overflyt lagervarer mellem lokationer med overflytningsordrer for at styre lageraktiviteter eller med vareomposteringskladden.|[Fremgangsmåde: Overflytte lagerbeholdning mellem lokationer](inventory-how-transfer-between-locations.md)|
|Reservere lagervarer eller indgående varer til salgsordrer, købsordrer, serviceordrer, montageordrer eller produktionsordrer.|[Sådan reserverer du varer](inventory-how-to-reserve-items.md)|
|Tildel serienumre eller lotnumre til en udgående eller indgående dokument- eller kladdelinje, for eksempel for at spore varer i tilfælde af tilbagekaldelser.|[Fremgangsmåde: Arbejde med serienumre og lotnumre](inventory-how-work-item-tracking.md)|
|Find, hvor et serie- eller lotnummer blev brugt i forsyningskæden, f.eks. i tilfælde af tilbagekaldelse.|[Sådan gør du: Spore varesporede varer](inventory-how-to-trace-item-tracked-items.md)|
|Administrer forretningsaktiviteter på salgskontorer, indkøbsafdelinger eller fabriksplanlægningskontor på tværs af flere lokationer.|[Fremgangsmåde: Arbejde med ansvarscentre](inventory-responsibility-centers.md)|

## <a name="see-also"></a>Se også  
[Køb](purchasing-manage-purchasing.md)  
[Salg](sales-manage-sales.md)    
[Arbejde med [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

