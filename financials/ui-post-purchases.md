---
title: "Om bogføring af købsdokumenter | Microsoft Docs"
description: "Få mere at vide om de forskellige bogføringsfunktioner, der bruges til at bogføre købsdokumenter."
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 05/12/2017
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 06c22658518d504c80a5a379d579cf7f7e8a0757
ms.contentlocale: da-dk
ms.lasthandoff: 09/22/2017

---
# <a name="posting-purchases"></a>Bogføring af køb
I **Prod.bogf.gruppe** på et købsdokument kan du vælge mellem følgende bogføringsfunktioner:

* **Bogfør**
* **Vis bogføring**
* **Bogfør og udskriv**
* **Testrapport**
* **Massebogfør**

Når du har udfyldt alle linjer og har indsat alle oplysninger i købsordren, kan du bogføre den, dvs. modtage og fakturere.

Når en købsordre bogføres, opdateres kreditorens konto, regnskabet og vareposterne.

For hver købsordre bliver der oprettet en købspost i tabellen **Finanspost**. Der oprettes også en post i kreditorkontoen i tabellen **Kreditorpost**, og der oprettes en finanspost i den relevante samlekonto. Desuden kan der eventuelt blive dannet en momspost og en finanspost med rabat. Om der bogføres en post med rabat, afhænger af oplysningerne i feltet **Bogføring med rabat** i vinduet **Købsopsætning**.

For hver købsordrelinje bliver der oprettet en varepost i tabellen **Varepost** (hvis købslinjerne indeholder varenumre) eller en finanspost i tabellen **Finanspost** (hvis der er indsat en finanskonto på købslinjerne). Købsordrer bliver desuden altid registreret i tabellerne **Købsleverancehoved** og **Købsfakturahoved**.

Inden du starter på selve bogføringen, kan du udskrive en kontrolrapport med alle oplysninger i købsordren og eventuelle fejl. Hvis du vil udskrive rapporten, skal du vælge **Bogføring** og derefter vælge **Kontrollér rapport**.

> [!IMPORTANT]  
>   Når du bogfører en ordre, har du mulighed for både at modtage og fakturere. Det kan gøres samtidigt eller hver for sig. Du kan også oprette en delkvittering og en delfaktura ved at udfylde felterne **Modtag (antal)** og **Fakturer (antal)** på de enkelte købsordrelinjer, før du bogfører. Bemærk, at du ikke kan oprette en faktura for noget, der ikke er modtaget. For at kunne fakturere er det altså nødvendigt, at du på forhånd har registreret en modtagelse, eller at du nu vælger at modtage og fakturere samtidigt.

Du kan enten bogføre eller bogføre og udskrive. Hvis du vælger at bogføre og udskrive, udskrives der en rapport, når ordren bogføres. Du kan også vælge funktionen **Massebogfør**, der giver mulighed for at bogføre flere ordrer samtidig.

Når bogføringen er gennemført, fjernes de bogførte købslinjer fra ordren. Der vises en meddelelse, når bogføringen er gennemført. Herefter kan du se de bogførte poster i forskellige vinduer, der indeholder bogførte poster, f.eks. **Kreditorposter**, **Finansposter**, **Vareposter**, **Købsleverance** og **Bogf. købsfakturaer**.

## <a name="see-also"></a>Se også
[Køb](purchasing-manage-purchasing.md)  
[Bogføre dokumenter og kladder](ui-post-documents-journals.md)  
[Arbejde med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)


