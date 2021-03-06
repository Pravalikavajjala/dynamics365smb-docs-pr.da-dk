---
title: Vise objekter som webtjenester | Microsoft Docs
description: "Publicer [!INCLUDE[d365fin](includes/d365fin_md.md)]-objekter som webtjenester, de er tilgængelige på netværket med det samme."
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: af1aef6ec730083c49b17ae8c0c9e39c7f663244
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-publish-a-web-service"></a>Fremgangsmåde: Udgive en webtjeneste
Webtjenester er en nem måde at gøre programfunktionalitet tilgængelig for en række eksterne systemer og brugere. [!INCLUDE[d365fin](includes/d365fin_md.md)] indeholder en lang række objekter, der vises som webtjenester som standard, på grund af integration med andre Microsoft-tjenester, men du kan også tilføje andre webtjenester.  

Du kan oprette en webtjeneste i Windows-klienten eller i webklienten. Du skal derefter publicere webtjenesten, så den er tilgængelig for serviceanmodninger via netværket. Brugere kan se webtjenester ved at pege på en browser på serverplaceringen og anmode om en oversigt over tilgængelige tjenester. Når du publicerer en webtjeneste, bliver den straks tilgængelig over netværket for godkendte brugere. Alle godkendte brugere kan få adgang til metadata til webtjenester, men kun brugere med tilstrækkelige -tilladelser kan få adgang til de faktiske data.

## <a name="creating-and-publishing-a-web-service"></a>Oprettelse og publicering af en webtjeneste  
 Følgende trin forklarer, hvordan du opretter og publicerer en webtjeneste.  

#### <a name="to-create-and-publish-a-web-service"></a>Sådan oprettes og publiceres en webtjeneste  

1.  Vælg ikonet ![Søg efter side eller rapport](media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Webtjenester**, og vælg derefter det relaterede link.  

2.  På siden **Webtjeneste** skal du vælge **Ny**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    >  **Codeunit** og **Side** er gyldige typer for SOAP-webtjenester. **Side** og **Forespørgsel** er gyldige typer for OData-webtjenester.  
    Hvis databasen indeholder flere firmaer, kan du også vælge et objekt-id, der er specifikt for ét af firmaerne.  
    Endelig er servicenavnet synligt for brugerne af webtjenesten og bruges som grundlag til at identificere og skelne mellem webtjenester, så du bør gøre navnet meningsfyldt.

3.  Marker afkrydsningsfeltet i kolonnen **Udgivet**.  

     Når du publicerer en webtjeneste, kan du i felterne **URL-adresse til OData** og **URL-adresse til SOAP** se de URL'er, der er genereret for webtjenesten. Du kan teste webtjenesten straks ved at vælge linksene i felterne **URL-adresse til OData** og **URL-adresse til SOAP**. Du kan vælge at kopiere værdien af feltet og gemme det til senere brug.  

Når du udgiver en webtjeneste, er den tilgængelig for eksterne parter. Du kan kontrollere tilgængeligheden af denne webtjeneste ved hjælp af en browser, eller du kan vælge linket i vinduet **URL-adresse til OData** og **URL-adresse til SOAP** i vinduet **Webtjenester**. Følgende procedure illustrerer, hvordan du kan kontrollere tilgængeligheden af webtjenesten til senere brug.  

#### <a name="to-verify-the-availability-of-a-web-service"></a>Sådan kontrolleres tilgængeligheden af en webtjeneste  

1.  Indtast den relevante URL-adresse i din browser Følgende tabel viser de typer URL'er, som du kan angive.  

    >    [!div class="mx-tdBreakAll"]
    >    |Webtjenestetype|Syntaks|Eksempel|  
    >    |----------------|------|-------|
    >    |SOAP |https://*Server*:*SOAPWebServicePort*/*ServerInstance*/WS/*CompanyName*/salesDocuments/ |https://mycompany.financials.dynamics.com:7047/MS/WS/MyCompany/Page/salesDocuments?tenant=mycompany.financials.dynamics.com |  
    >    |OData |https://*Server*:*ODataWebServicePort*/*ServerInstance*/OData/Company('*CompanyName*')|[https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com](https://MyCompany.financials.dynamics.com:7048/MS/OData/Company('MyCompany')/salesDocuments?tenant=MyCompany.financials.dynamics.com) <br />    Der skelnes mellem små og store bogstaver i firmanavnet.|

2.  Gennemse de oplysninger, der vises i browseren. Kontroller, at du kan se navnet på den webtjeneste, du har oprettet.  

 Når du får adgang til en webtjeneste, og du vil skrive data tilbage til [!INCLUDE[d365fin](includes/d365fin_md.md)], skal du angive firmanavnet. Du kan angive virksomheden som en del af URI'en som vist i følgende eksempler, eller du kan angive virksomhedens som en del af forespørgselsparametrene. F.eks. peger følgende URI'er på den samme OData-webtjeneste, og begge er gyldige URI'er.  

```  
https://localhost:7048/server/OData/Company('CRONUS International Ltd.')/Customer  
```  

```  
https://localhost:7048/server/OData/Customer?company='CRONUS International Ltd.'  
```  

## <a name="see-also"></a>Se også  
[Opsætning og administration til Dynamics 365 for Financials](admin-setup-and-administration.md)  

