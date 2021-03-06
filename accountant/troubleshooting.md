---
title: "Metoder til at fejlfinde eller løse problemer | Microsoft Docs"
description: "Få at vide, hvordan du kan løse problemerne med Accountant Hub til Dynamics 365."
author: edupont04
ms.service: dynamics365-accountant
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, troubleshoot
ms.date: 10/23/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: a9753b00b47fc4d74583482b2da92aae5e2f8a74
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---
# <a name="troubleshooting-included365acclongincludesd365acclongmdmd"></a>Fejlfinding [!INCLUDE[d365acc_long](includes/d365acc_long_md.md)]
[!INCLUDE[d365fin_early_release](includes/d365fin_early_release.md.md)]

Tilmelding til [!INCLUDE[d365acc](includes/d365acc_md.md)] er nemt og kan udføres hurtigt. Det er også nemt at føje kunder til dashboardet, men denne artikel vedrører problemer, der eventuelt opstår undervejs.

## <a name="what-email-address-can-i-use-with-included365accincludesd365accmdmd"></a>Hvilken mailadresse kan jeg bruge til [!INCLUDE[d365acc](includes/d365acc_md.md)]?
[!INCLUDE[d365acc](includes/d365acc_md.md)] kræver, at du bruger en arbejds- eller skolemailadresse til at tilmelde dig. [!INCLUDE[d365acc](includes/d365acc_md.md)] understøtter ikke mailadresser, som leveres af forbrugermailtjenester eller telekommunikationsudbydere. Dette omfatter outlook.com, hotmail.com, gmail.com og andre.  

Hvis du forsøger at tilmelde dig med en privat mailadresse, får du en meddelelse om, at du skal bruge en arbejds- eller skolemailadresse.  

## <a name="why-cant-i-connect-to-my-clients-data"></a>Hvorfor kan jeg ikke oprette forbindelse til min kundes data?
Der kan være en række årsager, herunder følgende:

- URL-adressen i feltet **Kundens URL-adresse** er ikke gyldig.  

  Gå til **Administrere kunder**, åbn den kunde, du ikke kan oprette forbindelse til, og vælg derefter **Test kundes URL-adresse**.  
- Kundens virksomhed er offline, f.eks. hvis den er ved at blive opgraderet

  På dashboardet skal du vælge menupunktet **Værktøjer** og derefter vælge **Kontroller fejl**. Dermed åbnes en liste med tekniske oplysninger, så du skal måske kontakte systemadministratoren, hvis du får vist fejl. Meddelelsen "Serveren har afvist kundens legitimationsoplysninger" angiver f.eks., at du ikke har adgang.  
- Du har ikke modtaget en mail fra din kunde, der inviterer dig til at deltage i deres [!INCLUDE[d365fin](includes/d365fin_md.md)], eller du har ikke åbnet linket i mailen, eller du ikke har accepteret invitationen

  Du skal åbne linket i invitationen og acceptere de trin, der tilføjer dig til kundens [!INCLUDE[d365fin](includes/d365fin_md.md)]. Indtil da har du ikke adgang til deres data.  
- Du har ikke adgang til alle regnskaber i din kundes [!INCLUDE[d365fin](includes/d365fin_md.md)]

  Din kunde kan have flere afdelinger eller virksomheder i [!INCLUDE[d365fin](includes/d365fin_md.md)], og invitationen inkluderer ikke altid alle regnskaber. Arbejd sammen med kunden for at sikre, at du har adgang til de virksomheder, som kunden ønsker, at du skal arbejde i.  

## <a name="why-doesnt-the-data-refresh-in-my-dashboard"></a>Hvorfor opdateres dataene i mit dashboard ikke?
Når du tilføjer en kunde eller anmoder om en opdatering af dataene, henter [!INCLUDE[d365acc](includes/d365acc_md.md)] dataene. Men du skal selv opdatere vinduet, f.eks. ved at vælge handlingen "Vis alle virksomheder igen", opdatere browservinduet, navigere væk fra dashboardet og derefter tilbage igen eller noget lignende. Dette er et kendt problem, som vi arbejder på at forbedre i en senere opdatering.  

## <a name="see-also"></a>Se også
[Kom i gang med [!INCLUDE[d365acc](includes/d365acc_md.md)]](get-started.md)  
[Tilføje kunder til dit dashboard i [!INCLUDE[d365acc](includes/d365acc_md.md)]](add-client.md)  

