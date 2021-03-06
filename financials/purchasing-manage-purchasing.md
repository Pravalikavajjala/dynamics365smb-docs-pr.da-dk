---
title: "Oversigt over opgaver til administration af køb | Microsoft Docs"
description: "Beskriver opgaver, du kan bruge til at administrere dine indkøb eller indkøbsprocesser, herunder hvordan købsfakturaer og købsordrer fungerer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: procurement, supply, vendor order
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: f9a932a521cd14e52e2a73e69544d2950235ea35
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="purchasing"></a>Indkøb
Du kan oprette en købsfaktura eller købsordre for at registrere omkostningerne ved køb og spore gæld. Hvis du vil styre en lagerbeholdning, benyttes købsfakturaer også til dynamisk at opdatere lagerniveauer, så du kan minimere lageromkostningerne og yde bedre kundeservice. Købsomkostningerne, herunder serviceudgifter og lagerværdier, der stammer fra bogføring af købsfakturaer, bidrager til avancebeløb og andre finansielle nøgletal i på din startside.

Du skal bruge købsordrer, hvis din købsproces kræver, at du kan registrere delleveringer af et ordreantal, f.eks. fordi hele antallet ikke er tilgængeligt hos leverandøren. Hvis du sælger varer ved at levere direkte fra leverandøren til kunden som en direkte levering, skal du også bruge købsordrer. Du kan finde flere oplysninger i [Fremgangsmåde: Foretage direkte leveringer](sales-how-drop-shipment.md). I alle andre henseender fungerer købsordrer på samme måde som købsfakturaer.

Du kan få købsfakturaer oprettet automatisk ved hjælp af tjenesten OCR (Optical Character Recognition) for at konvertere PDF fakturaer fra dine kreditorer til elektroniske dokumenter, som derefter konverteres til købsfakturaer via et workflow. For at bruge denne funktion skal du først tilmelde dig OCR-tjenesten og derefter udføre forskellige installationer. Du kan finde flere oplysninger under [Fremgangsmåde: Behandle indgående dokumenter](across-process-income-documents.md).      

Produkterne kan være både lagervarer og services. Du kan finde flere oplysninger under [Fremgangsmåde: Registrere nye varer](inventory-how-register-new-items.md).

Ved alle indkøbsprocesser kan du inkludere et godkendelsesworkflow, f.eks. for at kræve, at store køb godkendes af regnskabschefen. Du kan finde flere oplysninger under [Bruge godkendelsesworkflows](across-how-use-approval-workflows.md).

Den følgende tabel indeholder en opgavesekvens med links til de emner, der rummer beskrivelserne af opgaverne.

| Hvis du vil | Se |
| --- | --- |
| Oprette en købsfaktura for at registrere din aftale med en kreditor om at købe produkter på bestemte leverings- og betalingsbetingelser. |[Fremgangsmåde: Registrere køb](purchasing-how-record-purchases.md) |
|Oprette en købsrekvisition for at afspejle en tilbudsanmodning fra en leverandør, som du senere kan konvertere til en købsordre.|[Fremgangsmåde: Anmode om tilbud](purchasing-how-request-quotes.md)|
| Opret en købsfaktura for alle eller markerede linjer i en salgsfaktura. |[Fremgangsmåde: Købe varer til et salg](purchasing-how-purchase-products-sale.md) |
| Udfør en handling på en ubetalt bogført købsfaktura for automatisk at oprette en kreditnota og enten annullere købsfakturaen eller gendanne den, så du kan foretage rettelser. |[Fremgangsmåde: Rette eller annullere ubetalte salgsfakturaer](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) |
| Opret en købskreditnota for at tilbageføre en bestemt bogført købsfaktura, så den afspejler, hvilke produkter du returnerer til kreditoren, og hvilke indbetalte beløb der skal opkræves. |[Fremgangsmåde: Behandle købsreturvarer eller annulleringer](purchasing-how-register-new-vendors.md) |
|Forberede fakturering af flere leverancer fra den samme leverandør på én gang ved at kombinere leverancer på én faktura.|[Sådan kombineres modtagelser på én enkelt faktura](purchasing-how-to-combine-receipts.md)|
| Lær, hvordan [!INCLUDE[d365fin](includes/d365fin_md.md)] beregner, hvornår du skal bestille en vare for at modtage den på en bestemt dato.|[Beregning af forfaldsdato for køb](purchasing-date-calculation-for-purchases.md)|

## <a name="see-also"></a>Se også
[Opsætning af indkøb](purchasing-setup-purchasing.md)  
[Fremgangsmåde: Registrere nye kreditorer](purchasing-how-register-new-vendors.md)  
[Administrere skyldige beløb](payables-manage-payables.md)  
[Administrere projekter](projects-manage-projects.md)    
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]

