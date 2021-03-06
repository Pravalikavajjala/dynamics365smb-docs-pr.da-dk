---
title: "Rette eller annullere en bogført salgsfaktura | Microsoft Docs"
description: "Beskriver, hvordan du kan rette, fortryde eller annullere en bogført salgsfaktura og anvende en salgskreditnota."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 08/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 6de89bc0865fbe8617e33288b9c0c8fe7da802ef
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-correct-or-cancel-unpaid-sales-invoices"></a>Fremgangsmåde: Rette eller annullere ubetalte salgsfakturaer
Du kan rette eller annullere en bogført salgsfaktura. Dette er nyttigt, hvis du laver en fejl, eller hvis debitoren anmoder om en ændring.

> [!NOTE]  
>   Efter en bogført salgsfaktura er blevet helt eller delvist betalt, kan du ikke rette eller annullere den fra selve den bogførte salgsfaktura. I stedet for skal du manuelt oprette en salgskreditnota for at gøre salget ugyldigt og tilbagebetale debitoren, evt. administreret med en salgsreturvareordre. Du kan finde flere oplysninger i [Fremgangsmåde: Behandle salgsreturvarer eller annulleringer](sales-how-process-sales-returns-cancellations.md).

I vinduet **Bogført salgsfaktura** skal du vælge handlingen **Ret** eller **Annuller** for at udføre de handlinger, der er beskrevet i den følgende tabel.

| Handling | Beskrivelse |
| --- | --- |
| **Ret** |Den bogførte salgsfaktura er annulleret. En ny salgsfaktura med de samme oplysninger oprettes. Du kan foretage rettelsen og derefter fortsætte salget. Den nye salgsfaktura har et andet nummer end den første salgsfaktura. En rettelsessalgskreditnota oprettes og bogføres automatisk for at annullere den oprindelige bogførte salgsfaktura. På den oprindeligt bogførte salgsfaktura er afkrydsningsfelterne Annuller og Betalt markeret. |
| **Annuller** |Den bogførte salgsfaktura er annulleret. En rettelsessalgskreditnota oprettes og bogføres automatisk for at annullere den oprindelige bogførte salgsfaktura. På den oprindeligt bogførte salgsfaktura er afkrydsningsfelterne Annuller og Betalt markeret. |

Når du retter eller annullerer en bogført salgsfaktura, anvendes den rettede salgskreditnota på alle finanskonti og lageropgørelsesposter, der blev oprettet, da den oprindelige salgsfaktura blev bogført. På denne måde tilbageføres den bogførte salgsfaktura i dine finansposter, og rettelsessalgskreditnotaen efterlades til revisionsspor.

## <a name="to-correct-a-posted-sales-invoice"></a>Hvis du vil rette en bogført salgsfaktura
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bogf. salgsfakturaer**, og vælg derefter det relaterede link.  
2. Vælg den bogførte salgsfaktura, som du vil rette.

    > [!NOTE]  
>   Hvis afkrydsningsfeltet **Annulleret** er markeret, kan du ikke rette den bogførte salgsfaktura, da den allerede er rettet eller annulleret.
3. I vinduet **Bogført salgsfaktura** skal du vælge handlingen **Ret**.  
4. En ny salgsfaktura med de samme oplysninger oprettes, hvor du kan foretage en rettelse. Feltet **Annulleret** på den første bogførte salgsfaktura ændres til **Ja**.

    En salgskreditnota oprettes og bogføres automatisk for at annullere den oprindelige bogførte salgsfaktura.
5. Vælg handlingen **Vis rettelseskreditnota** for at få vist den bogførte salgskreditnota, som gør den oprindelige bogførte salgsfaktura ugyldig.

## <a name="to-cancel-a-posted-sales-invoice"></a>Hvis du vil annullere en bogført salgsfaktura
1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bogf. salgsfakturaer**, og vælg derefter det relaterede link.  
2. Vælg den bogførte salgsfaktura, som du vil annullere.

    > [!NOTE]  
>   Hvis afkrydsningsfeltet **Annulleret** er markeret, kan du ikke annullere den bogførte salgsfaktura, da den allerede er rettet eller annulleret.
3. I vinduet **Bogført salgsfaktura** skal du vælge handlingen **Annuller**.

    En salgskreditnota oprettes og bogføres automatisk for at annullere den oprindelige bogførte salgsfaktura. Feltet **Annulleret** på den første bogførte salgsfaktura ændres til **Ja**.
4. Vælg **Vis rettelseskreditnota** for at få vist den bogførte salgskreditnota, som gør den oprindelige bogførte salgsfaktura ugyldig.

## <a name="see-also"></a>Se også
[Salg](sales-manage-sales.md)  
[Konfigurere salg](sales-setup-sales.md)  
[Fremgangsmåde: Sende dokumenter via mail](ui-how-send-documents-email.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

