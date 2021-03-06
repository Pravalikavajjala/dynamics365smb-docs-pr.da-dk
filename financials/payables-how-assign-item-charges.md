---
title: "Tildele varegebyrer til salg og køb | Microsoft Docs"
description: "Hvis du vil have, at dine lagervarer skal pålægges de ekstra omkostninger, f.eks. fragt, fysisk håndtering, forsikring og transport, som du har ved køb eller salg af varer, kan du bruge funktionen Varegebyrer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: transportation, added cost
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: a97f56eeeb61aa94485dc4ec73f19a01e21e055a
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-use-item-charges-to-account-for-additional-trade-costs"></a>Fremgangsmåde: Bruge varegebyrer til at angive ekstra handelsomkostninger
For at sikre korrekt værdiansættelse, skal dine lagervarer pålægges evt. ekstra omkostninger, f.eks. fragt, fysisk håndtering, forsikring og transport, som du har ved køb eller salg af varer. Ved køb består hjemtagelsesprisen for en indkøbt vare af købsprisen til leverandøren og alle ekstra, direkte varegebyrer, som det er muligt at tildele til individuelle leverancer eller returvareleverancer. Ved salg kan det være lige så vigtigt at kende omkostningerne ved forsendelse af solgte varer som at kende omkostningen ved levering af købte varer.

Ud over at registrere ekstra omkostninger i lagerværdien kan du bruge funktionen Varegebyrer til følgende:

- Identificere en vares hjemtagelsespris for på den baggrund at kunne træffe mere nøjagtige beslutninger om, hvordan distributionsnetværket kan optimeres.
- Opdele en vares kostpris eller salgspris til brug i analyser.
- Indregne nedslag i prisen i kostprisen og salgsdekort i salgsprisen.

Når du vil tildele varegebyrer, skal du først opsætte varegebyrnumre for forskellige typer varegebyrer, herunder hvilke finanskonti omkostninger vedrørende salg, køb og lagerreguleringer skal bogføres på. Et varegebyrnummer består af en kombination af produktbogføringsgruppe, skattegruppekode, momsproduktbogføringsgruppe og varegebyr. Når du angiver varegebyrnummeret i et købs- eller salgsdokument, hentes den relevante finanskonto på basis af opsætningen af varegebyrkoden og de oplysninger, der er i det enkelte dokument.

For både købs- og salgsdokumenter, kan du tildele et varegebyr på to måder:
- I det dokument, hvor de varer, som varegebyret vedrører, er angivet. Det gør du typisk for dokumenter, der endnu ikke fuldt ud er bogført.
- I en separat faktura ved at knytte varegebyret til en bogført kvittering eller leverance, hvor de varer, gebyret vedrører, er anført.

> [!NOTE]  
>   Du kan tildele varegebyrer til ordrer, fakturaer og kreditnotaer for både køb og salg. I følgende procedurer beskrives, hvordan du arbejder med varegebyrer for en købsfaktura. Trinene er de samme for alle andre købs- og salgsdokumenter.

## <a name="to-set-up-item-charge-numbers"></a>Sådan oprettes varegebyrnumre
Varegebyrnumre bruges til at skelne mellem de forskellige typer varegebyrer, som bruges i din virksomhed.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varegebyrer**, og vælg derefter det relaterede link.
2. I vinduet **Varegebyrer** skal du vælge handlingen **Ny** for at oprette en ny linje.
3. Udfyld felterne efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-assign-an-item-charge-directly-to-the-purchase-invoice-for-the-item"></a>Sådan tildeles et varegebyr direkte til købsfakturaen for varen
Hvis du kender varegebyret på det tidspunkt, hvor du bogfører en købsfaktura for varen, skal du følge nedenstående procedure.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Købsfakturaer**, og vælg derefter det relaterede link.
2. Opret en ny købsfaktura. Du kan finde flere oplysninger under [Fremgangsmåde: Registrere køb](purchasing-how-record-purchases.md).
3. Kontroller, at købsfakturaen har en eller flere linjer af typen vare.
4. På en ny linje skal du vælge **Gebyr (Vare)** i feltet **Type**.
5. Angiv enheder af varegebyret, som du er blevet faktureret for, i feltet **Antal**.
6. Angiv varegebyret i feltet **Købspris**.
7. Udfyld de resterende felter efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    I følgende procedure skal du foretage den faktiske tildeling. Indtil varegebyret er fuldt tildelt, er værdien i feltet **Antal, der skal tildeles** med rød skrift.
8. Under fanen **Linjer** skal du vælge **Varegebyrtildeling**.

    Vinduet **Varegebyrtildeling** åbnes og viser én linje for hver linje af typen Vare på købsfakturaen. Når du vil tildele et varegebyr til en eller flere fakturalinjer, kan du bruge en funktion, som tildeler og distribuerer det for dig, eller du kan manuelt udfylde feltet **Antal, der skal tildeles**. I følgende procedure beskrives, hvordan du bruger funktionen Foreslå varegebyrtildeling.

9. I vinduet **Varegebyrtildeling** skal du vælge handlingen **Foreslå varegebyrtildeling**.
10. Hvis der er mere end én fakturalinje af typen vare, kan du vælge en af de fire indstillinger for fordeling.  

Hvis varegebyret er fuldt tildelt, er værdien i feltet **Antal, der skal tildeles** på købsfakturaen nul.

Varegebyret tildeles nu købsfakturaen. Når du bogfører modtagelsen af købsfakturaen, opdateres varens lagerværdier med omkostningen ved varegebyret.  

## <a name="to-assign-an-item-charge-from-a-separate-invoice-to-the-purchase-invoice-for-the-item"></a>Sådan tildeles et varegebyr fra en separat faktura til købsfakturaen for varen
Hvis du har modtaget en faktura for varegebyret, når du har bogført den originale købsleverance, skal du benytte denne fremgangsmåde.
1. Gentag trin 1 til 8 i afsnittet "Sådan tildeles et varegebyr direkte til købsfakturaen for varen".
2. Vælg handlingen **Hent købsleverancelinjer** i vinduet **Varegebyrtildeling**.
3. I vinduet **Købsmodtagelseslinjer** skal du vælge den bogførte købsleverance for den vare, du vil tildele varegebyret til, og vælg derefter knappen **OK**.
4. Vælg handlingen **Foreslå varegebyrtildeling**.

Omkostningen ved varegebyret på den separate købsfaktura er nu tildelt til varen på den bogførte købsleverance, og dermed opdateres varens lagerværdi med omkostningen ved varegebyret.

## <a name="see-also"></a>Se også
[Administrere skyldige beløb](payables-manage-payables.md)  
[Fremgangsmåde: Registrere køb](purchasing-how-record-purchases.md)  
[Fremgangsmåde: Fakturere salg](sales-how-invoice-sales.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

