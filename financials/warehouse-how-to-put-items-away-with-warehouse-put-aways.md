---
title: "Sådan lægges varer på lager med Læg-på-lager (lager) | Microsoft Docs"
description: "Hvis lokationen kræver læg-på-lager (logistik) og lagermodtagelse, skal du bruge funktionen læg-på-lager-dokumenterne til at styre, hvordan varer lægges på lager."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/31/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 28ff0073c75136f31153327a70a8f7c0bb9176aa
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-put-items-away-with-warehouse-put-aways"></a>Fremgangsmåde: Lægge varer på lager med Læg-på-lager (lager)
Hvis lokationen kræver læg-på-lager (logistik) og lagermodtagelse, skal du bruge funktionen læg-på-lager-dokumenterne til at styre, hvordan varer lægges på lager.  

Når du bogfører en lagermodtagelse, opdateres kildedokumenterne, f.eks. købsordre, indgående overflytningsordre eller salgsreturvareordre, det modtagne antal bogføres på varekladden og linjerne vedrørende de modtagende varer sendes til lagerstedets læg-på-lager-funktion. Hvis du har interne læg-på-lager og pluk, kan den interne læg-på-lager også oprette linjer for læg-på-lager.  

Afhængigt af logistikopsætningen bliver linjerne enten tilgængelige for læg-på-lager-kladden, eller der oprettes læg-på-lager-instruktioner straks. Du kan finde flere oplysninger i [Fremgangsmåde: Planlægge læg-på-lager-aktiviteter i kladder](warehouse-how-to-plan-put-aways-in-worksheets.md).  

Foruden de almindelige måder at oprette lagerets læg-på-lager, der er beskrevet i dette emne, kan du oprette læg-på-lager fra den relaterede bogførte lagermodtagelse. Dette er nyttigt, hvis du har slettet læg-på-lager-linjer, eller hvis du bruger styret læg-på-lager og pluk og har besluttet dig til ikke at bruge læg-på-lager-kladden, fordi du kan oprette eller genoprette læg-på-lager-vejledninger fra de bogførte købsleverancelinjer.  

## <a name="to-put-items-away-without-directed-put-away-and-pick"></a>Sådan lægges varer på lager uden styret læg-på-lager og pluk  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Læg-på-lager-aktiviteter**, og vælg derefter det relaterede link.  
2.  Åbn den læg-på-lager-aktivitet, der er klar til håndtering.  

    Du kan sortere på læg-på-lager-linjerne ud fra forskellige kriterier, f.eks. efter vare, placeringsnummer eller forfaldsdato, og dermed gøre processen mere effektiv.  
3.  Indtast det antal varer, der skal lægges på lager, i feltet **Håndteringsantal** på hver linje.  
4.  Vælg handlingen **Registrer læg-på-lager**, når du har lagt varerne på plads, for at registrere, at aktiviteten er udført, og for at gøre varerne disponible til pluk.  

## <a name="to-put-items-away-with-directed-put-away-and-pick"></a>Sådan lægges varer på lager med styret læg-på-lager og pluk  
1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Læg-på-lager-aktiviteter**, og vælg derefter det relaterede link.
    Hvis der er oprettet læg-på-lager-instruktioner, vises læg-på-lager-aktiviteten.  
2.  Åbn den læg-på-lager-aktivitet, du vil arbejde på.  
3.  Indtast dit bruger-id i oversigtspanelet **Generelt**, når du skal starte en læg-på-lager-aktivitet, hvis det kræves.  
4.  Udfør handlingerne Hent og Placer som angivet i feltet **Handlingstype** på linjerne.  

    Bemærk, at hver modtagelseslinje mindst er blevet til to linjer i instruktionen:  

    -   Den første linje med **handlingstypen** **Hent** angiver, hvor varerne er placeret i modtagelsesområdet. Du kan ikke ændre felterne for zone og placering på denne linje.  
    -   Den næste linje med **Placer** i feltet **Handlingstype** viser, hvor du skal placere varerne på lageret. Hvis der er modtaget et stort antal varer på en modtagelseslinje, skal de evt. lægges på lager på flere forskellige placeringer, så der er en Placer-linje for hver placering.  

        Hvis Hent- og Placer-linjerne til hver modtagelseslinje ikke står umiddelbart efter hinanden, og du gerne vil have det sådan, kan du sortere linjerne ved at vælge **Vare** i feltet **Sorteringsmetode** i oversigtspanelet **Generelt**.  

        Hvis placeringsniveauerne afspejler den fysiske udformning af lagerstedet, kan du bruge sorteringsmetoden **Placeringsniv.** til at lave den kortest mulige runde på lagerstedet.  

5.  Vælg handlingen **Registrer læg-på-lager**, når du har placeret alle varer på de korrekte placeringer.  

På lokationer, der er konfigureret til at bruge styret læg-på-lager og pluk, er følgende indstillinger forudsætninger for ovenstående fremgangsmåde:  

- Der oprettes en læg-på-lager-skabelon. Du kan finde flere oplysninger i [Sådan oprettes læg-på-lager-skabeloner](warehouse-how-to-set-up-put-away-templates.md).  
- Varens eller lagervarens vægt, rummål og andre særlige forudsætninger defineres. Du kan også finde flere oplysninger i Bruttovægt.  
- Placeringernes kapacitet, type og niveau. Du kan finde flere oplysninger i Placeringsniveau.  

Der tages hensyn til placeringsniveau, når mere end én placering opfylder kriterierne for læg-på-lager-skabelonen. Hvis kriterierne i læg-på-lager-skabelonen og placeringsniveauet er ens for mere end én placering, vælges placeringen med det højeste nummer.

## <a name="to-create-a-put-away-from-a-posted-receipt"></a>Sådan oprettes en læg-på-lager-aktivitet fra en bogført modtagelse  
 Hvis din lokation bruger både læg-på-lager-behandling og modtagelsesbehandling, og du har slettet læg-på-lager-linjer, eller hvis du bruger styret læg-på-lager og pluk og har besluttet dig til ikke at bruge læg-på-lager-kladden, kan du oprette eller genoprette læg-på-lager-vejledninger til de bogførte købsleverancelinjer.

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Bogførte lagermodtagelser**, og vælg derefter det relaterede link.  
2.  Vælg en bogført modtagelse, der evt. skal lægges på lager.  
3.  Vælg handlingen **Kort**.  

    Hvis feltet **Bilagsstatus** er tomt, er modtagelsen ikke lagt på lager overhovedet. Ellers står der i feltet, at modtagelsen er delvist lagt på lager eller fuldt lagt på lager.  

4.  Vælg handlingen **Opret læg-på-lager**, hvis modtagelsen er lagt delvist på lager eller slet ikke er lagt på lager.  
5.  Udfyld felterne i kørselsvinduet for at oprette læg-på-lager-aktiviteten, og klik på knappen **OK**.   

## <a name="see-also"></a>Se også  
[Logistik](warehouse-manage-warehouse.md)  
[Lagerbeholdning](inventory-manage-inventory.md)  
[Sådan konfigureres logistikfunktioner](warehouse-setup-warehouse.md)     
[Montagestyring](assembly-assemble-items.md)    
[Designoplysninger: Logistik](design-details-warehouse-management.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

