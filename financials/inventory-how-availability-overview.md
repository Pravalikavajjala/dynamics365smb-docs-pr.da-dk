---
title: "Få en oversigt over disponering | Microsoft Docs"
description: "Du kan få vist oplysninger om varedisponeringen eller -beholdningen på tværs af lokationer pr. salg eller købshændelser, efter en periode eller efter varens placering på en montage- eller produktionsstykliste."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: stock
ms.date: 08/15/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 986f1b00f1a8db237944ec8579d9401ca85dfd8a
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-view-the-availability-of-items"></a>Sådan gør du: Vise varedisponering
Fra konteksten for en virksomhedsopgave kan du få avancerede oplysninger om, hvornår og hvor en vare er tilgængelig, f.eks, når du taler med en kunde om en leveringsdato.

Du kan få vist disponeringen for alle varer pr. lokation, og du kan få vist disponeringen for hver enkelt vare ud fra hændelse, periode eller lokation. En hændelse er enhver planlagt varetransaktion, f.eks en salgsleverance eller modtagelse af en indgående overflytning.

> [!NOTE]  
>   Visninger af tilgængelighed pr. lokation kræver, at du har lager på mere end én lokation. Du kan finde flere oplysninger i [Fremgangsmåde: Opsætning af lokationer](inventory-how-setup-locations.md).

I [!INCLUDE[d365fin](includes/d365fin_md.md)] skal tilgængelighedstal vises i to forskellige felter, med hver sin definition:

* Feltet **Lager** viser den faktiske lagerbeholdning i dag ud fra de bogførte vareposter.
* Feltet **Planlagt disponibel balance** beregnes og viser lagerbeholdningen plus fastlagte tilgange minus bruttobehovet. (I [!INCLUDE[d365fin](includes/d365fin_md.md)] inkluderer fastlagte tilgange antal på købsordrer og indgående overflytningsordrer. Bruttobehov omfatter antal på salgsordrer og udgående overflytningsordrer).

> [!TIP]  
>   Den planlagte disponible balance er især relevant at få vist i vinduerne **Varedisponering pr. periode** og **Varedisponering pr. hændelse**, da de indeholder datedimensionen.  

> [!NOTE]  
>   De følgende procedurer beskriver, hvordan du får vist avancerede tilgængelighedsoplysninger fra varelisten og varekortet. Du kan også få adgang til oplysninger fra salgsdokumentlinjer for varen på linjen. Du kan finde flere oplysninger i [Fremgangsmåde: Sælge produkter](sales-how-sell-products.md).

## <a name="to-view-the-availability-of-an-item-according-to-when-it-will-be-received-or-shipped"></a>Sådan får du vist tilgængeligheden for en vare, ud fra hvornår den er modtages eller leveres
Du får vist tilgængeligheden for en vare i overensstemmelse med planlagte varetransaktioner i vinduet **Disponering pr. hændelse**.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varer**, og vælg derefter det relaterede link.
2. Åbn kortet for en vare, som du vil have vist tilgængeligheden for.
3. Vælg handlingen **Varedisponering pr.**, og vælg derefter handlingen **Hændelse**.

    Vinduet **Varedisponering pr. hændelse** viser, hvordan lagerantallet for varen udvikler sig over tid i overensstemmelse med planlagt levering og modtagelse. Vinduet giver en komprimeret visning, der viser én linje med akkumulerede oplysninger pr. tidsinterval, hvor lagermængderne ændres. Tidsintervaller, hvor der ikke opstod nogen begivenheder, vises ikke. Du kan udvide hver linje for at få vist detaljer om den eller de begivenheder, der forårsagede det akkumulerede antal på linjen.
4. Vælg værdien i feltet **Planlagt disponibel balance** for at få vist vareposterne eller åbne dokumenter, der udgør værdien.

## <a name="to-view-the-availability-of-an-item-in-different-periods"></a>Sådan får du vist disponeringen for en vare i forskellige perioder
Du får vist disponeringen for en vare over tid for angivne perioder i vinduet **Varedisponering pr. periode**.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varer**, og vælg derefter det relaterede link.
2. Åbn kortet for en vare, som du vil have vist tilgængeligheden for.
3. Vælg handlingen **Varedisponering pr.**, og vælg derefter handlingen **Periode**.

    Vinduet **Varedisponering pr. periode** viser, hvordan lagerbeholdningen for varen udvikler sig over tid, vist for en periode, du vælger, f.eks. Dag, Uge eller Kvartal.
4. Vælg værdien i feltet **Planlagt disponibel balance** for at få vist vareposterne eller åbne dokumenter, der udgør værdien.

## <a name="to-view-the-availability-of-an-item-at-the-locations-where-it-is-stored"></a>Sådan får du vist disponeringen for en vare på de lokationer, hvor den opbevares
I vinduet **Varedisponering pr. lokation** får du vist disponeringen for en vare på de forskellige steder, hvor den opbevares.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varer**, og vælg derefter det relaterede link.
2. Åbn kortet for en vare, som du vil have vist tilgængeligheden for.
3. Vælg handlingen **Varedisponering pr.**, og vælg derefter handlingen **Lokation**.

    Vinduet **Varedisponering pr. lokation** viser, hvordan lagerbeholdningen for varen udvikler sig i fremtiden, vist for hver lokation, hvor varen opbevares.
4. Vælg værdien i feltet **Beholdning** for at få vist de vareposter, der udgør værdien.
5. Vælg værdien i feltet **Planlagt disponibel balance** for at få vist vareposterne eller åbne dokumenter, der udgør værdien.

## <a name="to-view-the-availability-of-all-items-by-the-location-where-they-are-stored"></a>Sådan får du vist disponeringen for alle varer ud fra den lokation, hvor de opbevares
Du får vist disponeringen for alle dine varer på tværs af alle dine lokationer i vinduet **Varer pr. lokation**.

1. Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Varer**, og vælg derefter det relaterede link.
2. Vælg handlingen **Varer pr. lokation**.

    Vinduet **Varer pr. lokation** viser for alle varer, hvor mange er tilgængelige på hver enkelt lokation.
3. Vælg værdien i feltet **Beholdning** for at få vist de vareposter, der udgør værdien.

## <a name="to-view-the-availability-of-an-item-by-its-use-in-assembly-or-production-boms"></a>Sådan får du vist tilgængeligheden af en vare ud fra brugen af den på montage- eller produktionsstyklister
Hvis en vare findes på montage- eller produktionsstyklister, enten som en overordnet vare eller som en komponent, kan du se, hvor mange enheder af den der er påkrævet, i vinduet **Varedisponering pr. styklisteniveau**. Vinduet angiver, hvor mange enheder af en overordnet vare, du kan fremstille, baseret på tilgængeligheden af underordnede varer eller underliggende linjer. En vare med en montage- eller produktionsstykliste vises i vinduet som en linje, der kan skjules. Du kan udvide denne linje for at få vist de underliggende komponenter og halvfabrikata på lavere niveau med deres egne styklister.

Du kan bruge vinduet til at finde ud af, om du kan opfylde en salgsordre for en vare på en bestemt dato ved at kigge på den aktuelle tilgængelighed og de mængder, der kan leveres med dens komponenter. Du kan også bruge vinduet til at identificere flaskehalse i relaterede styklister.

På hver linje i vinduet for både overordnede og underordnede varer angiver følgende nøglefelter tilgængelighedstallene. Du kan bruge disse tal til at love, hvor mange enheder af en overordnet vare, du kan levere, hvis du starter den relaterede montageproces.

|Felt|Beskrivelse|
|------|-----------|
|**Kan blive overordnet**|Viser, hvor mange enheder af halvfabrikata af topvaren, du kan fremstille. Feltet angiver, hvor mange umiddelbart overordnede enheder, du kan samle. Værdien er baseret på tilgængeligheden af varen på linjen.|
|**Kan blive topvare**|Viser, hvor mange enheder af topvaren, du kan fremstille. Feltet angiver, hvor mange enheder af styklistevaren på øverste linje, du kan samle. Værdien er baseret på tilgængeligheden af varen på linjen.|

### <a name="item-availability-by-bom-level-window"></a>Vinduet Varedisponering pr. styklisteniveau
Vinduet **Varedisponering pr. styklisteniveau** viser oplysninger for varen på det kort eller den dokumentlinje, som vinduet åbnes for. Elementet vises altid på den øverste linje. Du kan få vist oplysninger for andre varer eller for alle varer ved at ændre værdien i feltet **Varefilter**.

> [!NOTE]  
>   Som standard viser tilgængelighedstallene på linjerne den samlede tilgængelighed af alle varer under topvaren. Disse tal vises i feltet **Disponibelt antal** og fokuserer på topvaren. Oplysninger om, hvor mange halvfabrikata, du kan fremstille kan dog blive skævt. Hvis du ønsker at få en angivelse af, hvor mange af de viste halvfabrikata, du kan fremstille, skal du rydde feltet **Vis samlet disponering** og derefter se tallet i feltet **Kan blive overordnet**.

Feltet **Flaskehals** angiver, hvilken vare i styklistestrukturen, der begrænser dig i at fremstille en større mængde end den mængde, der vises i feltet **Kan blive topvare**. For eksempel kan flaskehalsvaren være en købt komponent med en forventet modtagelsesdato, der er for sen til, at der kan oprettes supplerende enheder af topvaren efter datoen i feltet **Behovsdato**.

## <a name="assembly-availability-window"></a>Vinduet Montagedisponering
Vinduet **Montagedisponering** indeholder detaljerede disponeringsoplysninger for montageelementet. Vinduet åbnes:

- Automatisk fra en salgsordrelinje i montageordrescenarier, når du angiver et antal, der forårsager et problem med komponentdisponeringen.
- Automatisk fra et montageordrehoved, når du angiver en værdi i feltet Antal, der forårsager et problem med komponentdisponeringen.
- Manuelt, når du åbner den fra en montageordre. Under fanen Handlinger i gruppen Funktion skal du klikke på Vis disponering.

I oversigtspanelet **Detaljer** vises detaljerede disponeringsoplysninger for montageelementet, herunder, hvor mange af montageordreantallet kan monteres ved forfaldsdatoen, der er baseret på tilgængeligheden af de nødvendige komponenter. Dette vises i feltet Mulighed for montage i oversigtspanelet Detaljer.

Værdien i feltet **Mulighed for montage** vises med rød skrift, hvis mængden er lavere end mængden i feltet **Restantal**, hvilket angiver, at der ikke er nok tilgængelige komponenter til at montere hele mængden.

I oversigtspanelet **Linjer** vises detaljerede disponeringsoplysninger for montagekomponenterne.

Hvis en eller flere montagekomponenter ikke er tilgængelig, afspejles dette i feltet **Mulighed for montage** på den pågældende linje som en mindre mængde end mængden i feltet **Restantal** i oversigtspanelet **Detaljer**.

## <a name="see-also"></a>Se også
[Administrere lager](inventory-manage-inventory.md)  
[Montagestyring](assembly-assemble-items.md)  
[Fremgangsmåde: Arbejde med styklister](inventory-how-work-BOMs.md)    
[Sådan oprettes lokationer](inventory-how-setup-locations.md)  
[Fremgangsmåde: Overflytte lagerbeholdning mellem lokationer](inventory-how-transfer-between-locations.md)  
[Fremgangsmåde: Sælge produkter](sales-how-sell-products.md)      
[Arbejde med Dynamics 365](ui-work-product.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)

