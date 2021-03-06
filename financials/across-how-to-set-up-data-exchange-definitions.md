---
title: Definere, hvordan data udveksles elektronisk | Microsoft Docs
description: Du kan bruge en ekstern udbyder af OCR-tjenester til at omdanne PDF- eller billedfiler til elektroniske dokumenter.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ba26b354d235981bd7291f9ac6402779f554ac7a
ms.openlocfilehash: 1f35debace937a04b8f4174131fd72cde6610b7a
ms.contentlocale: da-dk
ms.lasthandoff: 11/10/2017

---
# <a name="how-to-set-up-data-exchange-definitions"></a>Fremgangsmåde: Konfigurere dataudvekslingsdefinitioner
Du kan konfigurere [!INCLUDE[d365fin](includes/d365fin_md.md)] til at udveksle data i bestemte tabeller med data i eksterne filer, f.eks. at sende og modtage elektroniske dokumenter, importere og eksportere bankoplysninger eller andre data, f.eks. løn, valutakurser og varekataloger. Du kan finde flere oplysninger under [Udveksle data elektronisk](across-data-exchange.md).  

Som forberedelse til oprettelse af en dataudvekslingsdefinition for en datafil eller -stream, kan du bruge det relaterede XML-skema til at definere, hvilke dataelementer der skal indgå, i oversigtspanelet **Kolonnedefinitioner**. Se trin 6 i afsnittet "Sådan beskrives formateringen af linjer og kolonner i filen". Du kan finde flere oplysninger i [Fremgangsmåde: Bruge XML-skemaer til at forberede dataudvekslingsdefinitioner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

Normalt angives dataudvekslingsdefinitioner i vinduet **Dataudvekslingsdefinition**. Men når du konfigurerer en dataudvekslingsdefinition til tjenesten for opdatering af valutakurser, starter du processen i det forenklede vindue **Opsætning af valutakursopdatering**.  

> [!NOTE]  
>  Hvis den fil, der konverteres, er i XML-format, skal udtrykket *"kolonne"* i dette emne fortolkes som *"et XML-element, der indeholder data"*.  

Dette emne indeholder følgende procedurer:  

* Sådan oprettes en dataudvekslingsdefinition  
* Sådan eksporteres en dataudvekslingsdefinition som en XML-fil, som andre kan bruge  
* Sådan importeres en XML-fil til en eksisterende dataudvekslingsdefinition  

## <a name="to-create-a-data-exchange-definition"></a>Sådan oprettes en dataudvekslingsdefinition  
Opretter en dataudvekslingsdefinition, der omfatter to opgaver:  

1. I vinduet **Dataudvekslingsdefinition** skal du beskrive formateringen af linjer og kolonner i filen.  
2. I vinduet **Dataudvekslingskobling** skal du knytte kolonner i datafilen til felter i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

     Dette beskrives i følgende fremgangsmåder.  

#### <a name="to-describe-the-formatting-of-lines-and-columns-in-the-file"></a>Sådan beskrives formateringen af linjer og kolonner i filen  
1. I feltet **Søg** skal du indtaste **Dataudvekslingsdefinitioner** og derefter vælge det relaterede link.  
2. Vælg handlingen **Ny**.  
3. Brug oversigtspanelet **Generelt** til at beskrive dataudvekslingsdefinitionen og datafiltypen ved at udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Definition|  
    |---------------------------------|---------------------------------------|  
    |**Kode**|Angiv en kode, der identificerer dataudvekslingsdefinitionen.|  
    |**Navn**|Angiv et navn for dataudvekslingsdefinitionen.|  
    |**Filtype**|Angiv hvilken filtype, som dataudvekslingsdefinitionen bruges til. Du kan vælge mellem tre filtyper:<br /><br /> -   **XML**: Lagdelte strenge bestående af indhold og markeringer omgivet af koder, der angiver funktionen.<br />-   **Variabeltekst**: Poster har variabel længde og adskilles af et tegn, f.eks komma eller semi\-kolon. Også kendt som *afgrænset fil*.<br />-   **Fast tekst**: Poster har samme længde ved brug af numeriske tegn, og hver post er placeret på en separat linje. Også kendt som *fil med fast bredde*.|  
    |**Type**|Angiv, hvilken type forretningsaktiviteter dataudvekslingsdefinitionen bruges til, f.eks. **eksport af betaling**.|  
    |**Codeunit til datahåndtering**|Angiv den kodeenhed, der overfører data til og fra tabellerne i [!INCLUDE[d365fin](includes/d365fin_md.md)].|  
    |**Valideringscodeunit**|Angiv den kodeenhed, der bruges til at validere data mod foruddefinerede forretningsregler.|  
    |**Læser/skriver codeunit**|Angiv den kodeenhed, der behandler importerede data før tilknytning og eksporterede data efter tilknytning.|  
    |**Læser/skriver XMLport**|Angiv den XMLport, gennem hvilken en importeret datafil eller en tjeneste går forud for tilknytning, og gennem hvilken udlæste data går, når de er skrevet til en datafil eller tjeneste efter tilknytning.|  
    |**Codeunit til ekstern datahåndtering**|Angiv den kodeenhed, der overfører eksterne data ind og ud af dataudvekslingsstrukturen.|  
    |**Codeunit til brugerfeedback**|Angiv den kodeenhed, der udfører forskellige rensning efter tilknytning, f.eks markerer linjerne som eksporteret og sletter midlertidige poster.|  
    |**Filkodning**|Angiv kodning af filen. **Bemærk:** Dette felt er kun relevant for import.|  
    |**Kolonneseparator**|Angiv, hvordan kolonner adskilles i datafilen, hvis filen er af typen **Variabel tekst**.|  
    |**Antal linjer i filhoved**|Angiv, hvor mange hovedlinjer der findes i filen.<br /><br /> Dette sikrer, at sidehoveddataene ikke importeres. **Bemærk:** Dette felt er kun relevant for import.|  
    |**Identifikation af hovedlinje**|Hvis der findes en sidehovedlinje i flere positioner i filen, skal du indtaste teksten i den første kolonne på linjen i sidehovedet.<br /><br /> Dette sikrer, at sidehoveddataene ikke importeres. **Bemærk:** Dette felt er kun relevant for import.|  
    |**Identifikation af fodlinje**|Hvis der findes en sidefodslinje i flere positioner i filen, skal du indtaste teksten i den første kolonne på linjen i sidefoden.<br /><br /> Dette sikrer, at sidefodsdataene ikke importeres. **Bemærk:** Dette felt er kun relevant for import.|  

4. Brug oversigtspanelet **Linjedefinitioner** til at beskrive formatering af linjer i datafilen ved at udfylde felterne som beskrevet i følgende tabel.  

    > [!NOTE]  
    >  I forbindelse med import af kontoudtog kan du kun oprette én linje for det enkelte format for bankkontoudtogsfilen, som du vil importere.  
    >   
    >  I forbindelse med eksport betalinger kan du oprette en linje for hver betalingstype, du vil eksportere. I så fald viser oversigtspanelet **Kolonnedefinitioner** forskellige kolonner for hver betalingstype.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Kode**|Angiv en kode, der identificerer linjen i filen.|  
    |**Navn**|Angiv et navn, der beskriver linjen i filen.|  
    |**Antal kolonner**|Angiv, hvor mange kolonner linjen i datafilen har. **Bemærk:** Dette felt er kun relevant for import.|  
    |**Identifikation af datalinje**|Angiv placeringen i det tilknyttede XML-skema for det element, der repræsenterer hovedposten i datafilen. **Bemærk:** Dette felt er kun relevant for import.|  
    |**Navneområde**|Angiv det navneområde, der forventes i filen, for at aktivere validering af navneområde. Du kan lade dette felt være tomt, hvis du ikke vil aktivere validering af navneområdet.|  

5. Gentag trin 4 for at oprette en linje for hver type fildata, du vil eksportere.  

     Fortsæt til at beskrive formateringen af kolonner i datafilen ved at udfylde felterne i oversigtspanelet **Kolonnedefinitioner**, som beskrevet i nedenstående tabel. Du kan bruge strukturfilen, f.eks en . XSD-fil, så datafilen forhåndsudfylder oversigtspanelet med de relevante elementer. Du kan finde flere oplysninger i [Fremgangsmåde: Bruge XML-skemaer til at forberede dataudvekslingsdefinitioner](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

6. I oversigtspanelet **Kolonnedefinitioner** skal du vælge **Hent filstruktur**.  
7. I vinduet **Hent filstruktur** skal du vælge den relaterede strukturfil og derefter klikke på knappen **OK**. Linjerne i oversigtspanelet **Kolonnedefinitioner** udfyldes i overensstemmelse med datafilens struktur.  
8. Rediger eller udfyld felterne i oversigtspanelet **Kolonnedefinitioner** som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Kolonnenr.**|Angiv det nummer, der afspejler kolonnens placering på linjen i filen.<br /><br /> For XML-filer, skal du angive det tal, der afspejler elementtypen i den fil, der indeholder dataene.|  
    |**Navn**|Angiv navnet på kolonnen.<br /><br /> For XML-filer skal du angive koden, der markerer de data, der skal udveksles.|  
    |**Datatype**|Angiv, om data, der skal udveksles, er af typen **Tekst**, **Dato** eller **Decimal**.|  
    |**Dataformat**|Angiv dataformatet, hvis relevant. Det kan f.eks. være **MM-dd-åååå**, hvis datatypen er **Dato**. **Bemærk:** Hvis du vil eksportere, skal du angive dataformatet i overensstemmelse med [!INCLUDE[d365fin](includes/d365fin_md.md)]. I forbindelse med import skal du angive dataformatet i overensstemmelse med .NET Framework. Du kan finde flere oplysninger i [Standarddato- og tidsformatstrenge](http://go.microsoft.com/fwlink/?LinkID=323466).|  
    |**Dataformatering**|Angiv dataformatets kultur, hvis relevant. Det kan f.eks. være **en-US**, hvis datatypen er **Decimal**, så du sikrer, at komma bruges som .000-separator i henhold til det amerikanske format. Du kan finde flere oplysninger i [Standarddato- og tidsformatstrenge](http://go.microsoft.com/fwlink/?LinkID=323466). **Bemærk:** Dette felt er kun relevant for import.|  
    |**Længde**|Angiv længden af fast bredde for linjen, der indeholder kolonnen, hvis datafilen er af typen **Fast tekst**.|  
    |**Beskrivelse**|Angiv en beskrivelse af kolonnen, hvis du ønsker flere oplsyninger.|  
    |**Sti**|Angiv placeringen af elementet i det tilknyttede XML-skema.|  
    |**Identifikator for minustegn**|Angiv den værdi, der bruges i datafilen til at identificere negative beløb i datafiler, der ikke kan indeholde negative tegn. Dette id bruges derefter til at tilbageføre de identificerede beløb til negative tegn under import. **Bemærk:** Dette felt er kun relevant for import.|  
    |**Konstant**|Angiv de data, du vil eksportere i denne kolonne, som f.eks. ekstra oplysninger om betalingstypen. **Bemærk:** Dette felt er kun relevant for eksport.|  

9. Gentag trin 8 for hver kolonne eller hvert XML-element i den datafil, der indeholder data, du vil udveksle med [!INCLUDE[d365fin](includes/d365fin_md.md)].  

 Det næste trin i oprettelsen af en definition til udveksling af data er at beslutte, hvilke kolonner eller XML-elementer i datafilen, der skal knyttes til hvilke felter i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!NOTE]  
>  Den bestemte tilknytning afhænger af forretningsformålet med den datafil, der skal udveksles, og af lokale variationer. Selv SEPA-bankstandarden har lokale variationer. [!INCLUDE[d365fin](includes/d365fin_md.md)] understøtter import af SEPA CAMT-bankkontoudtogsfiler out\-of\-the\-box. Dette repræsenteres ved registreringskoden til dataudvekslingsdefinitionen **SEPA CAMT** i vinduet **Dataudvekslingsdefinitioner**. Du kan finde oplysninger om den specifikke felttilknytning for denne SEPA CAMT-understøttelse i [Feltkobling, når du importerer SEPA-CAMT-filer](across-field-mapping-when-importing-sepa-camt-files.md).  

#### <a name="to-map-columns-in-the-data-file-to-fields-in-included365finincludesd365finmdmd"></a>Sådan tilknyttes kolonner i datafilen til felter i [!INCLUDE[d365fin](includes/d365fin_md.md)]  
1. Brug oversigtspanelet **Linjedefinitioner** til at vælge den linje, du vil knytte kolonner til felter for, og vælg derefter **Feltkobling**. Vinduet **Dataudvekslingskobling** åbnes.  
2. På oversigtspanelet **Generelt** skal du angive tilknytningsopsætningen ved at udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Tabel-id**|Angiv den tabel, der indeholder felterne, til eller fra hvilke data udveksles i henhold til tilknytningen.|  
    |**Brug som midlertidig tabel**|Angiv, om den tabel, du vælger i feltet **Tabel-id**, er en midlertidig tabel, hvor de importerede data gemmes, før de knyttes til måltabellen.<br /><br /> Du kan bruge en midlertidige tabel, når dataudvekslingsdefinitionen bruges til at importere og konvertere elektroniske dokumenter, f.eks kreditorfakturaer til købsfakturaer i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Du kan finde flere oplysninger under [Udveksle data elektronisk](across-data-exchange.md).|  
    |**Navn**|Angiv et navn for tilknytningsopsætningen.|  
    |**Codeunit til førtilknytning**|Angiv den kodeenhed, der klargør tilknytningen mellem felter i [!INCLUDE[d365fin](includes/d365fin_md.md)] og eksterne data.|  
    |**Koblings-codeunit**|Angiv den kodeenhed, der bruges til at knytte de angivne kolonner eller XML-dataelementer til felter i [!INCLUDE[d365fin](includes/d365fin_md.md)].|  
    |**Codeunit til eftertilknytning**|Angiv den kodeenhed, der fuldfører tilknytningen mellem felter i [!INCLUDE[d365fin](includes/d365fin_md.md)] og eksterne data. **Bemærk:** Når funktionen Tjeneste til konvertering af bankdata anvendes, konverterer kodeenheden eksporterede data fra [!INCLUDE[d365fin](includes/d365fin_md.md)] til et generisk format, der er klar til eksport. I forbindelse med import konverterer kodeenheden eksterne data til et format, der er klar til import i [!INCLUDE[d365fin](includes/d365fin_md.md)].|  

3.  Brug oversigtspanelet **Feltkobling** til at angive, hvilke kolonner der knyttes til hvilke felter i [!INCLUDE[d365fin](includes/d365fin_md.md)] ved at udfylde felterne som beskrevet i følgende tabel.  

    |Felt|Beskrivelse|  
    |---------------------------------|---------------------------------------|  
    |**Kolonnenr.**|Angiv, hvilken kolonne i datafilen, som du vil definere en tilknytning til.<br /><br /> Du kan kun vælge de kolonner, der repræsenteres af linjer, i oversigtspanelet **Kolonnedefinitioner** i vinduet **Dataudvekslingsdefinition**.|  
    |**Felt-id**|Angiv, hvilket felt kolonnen i feltet **Kolonnenr.** er tilknyttet.<br /><br /> Du kan kun vælge felter, der findes i den tabel, du angav i feltet **Tabel** i oversigtspanelet **Generelt**.|  
    |**Eventuelt**|Angiv, at tilknytningen ignoreres, hvis feltet er tomt. **Bemærk:** Hvis du ikke markerer dette afkrydsningsfelt, opstår der en fejl i eksporten, hvis feltet er tomt. **Bemærk:** Dette felt er kun relevant for eksport.|  
    |**Måltabel-id**|Er kun synlig, når afkrydsningsfeltet **Brug som midlertidig tabel** er markeret.<br /><br /> Angiv den tabel, som værdien i feltet **Kolonnetitel** er knyttet til, når du bruger en midlertidig tabel til dataimport.|  
    |**Titel på måltabel**|Er kun synlig, når afkrydsningsfeltet **Brug som midlertidig tabel** er markeret.<br /><br /> Angiv navnet på den tabel i feltet **Måltabel-id**, som er den tabel, som værdien i feltet **Kolonnetitel** er knyttet til, når du bruger en midlertidig tabel til dataimport.|  
    |**Målfelt-id**|Er kun synlig, når afkrydsningsfeltet **Brug som midlertidig tabel** er markeret.<br /><br /> Angiv det felt i måltabellen, som værdien i feltet **Kolonnetitel** er knyttet til, når du bruger en midlertidig tabel til dataimport.|  
    |**Titel på målfelt**|Er kun synlig, når afkrydsningsfeltet **Brug som midlertidig tabel** er markeret.<br /><br /> Angiv det navn i feltet i måltabellen, som værdien i feltet **Kolonnetitel** er knyttet til, når du bruger en midlertidig tabel til dataimport.|  
    |**Eventuelt**|Er kun synlig, når afkrydsningsfeltet **Brug som midlertidig tabel** er markeret.<br /><br /> Angiv, om tilknytningen skal ignoreres, hvis feltet er tomt. Hvis du ikke markerer dette afkrydsningsfelt, opstår der en fejl i eksporten, hvis feltet er tomt.|  

 Dataudvekslingsdefinitionen er nu klar til at blive aktiveret for brugere. Du kan finde flere oplysninger i [Fremgangsmåde: Konfigurere afsendelse og modtagelse af elektroniske dokumenter](across-how-to-set-up-electronic-document-sending-and-receiving.md), [Fremgangsmåde: Opsætte SEPA-kreditoverførsel](finance-how-to-set-up-sepa-credit-transfer.md), [Fremgangsmåde: Konfigurere SEPA Direct Debit](finance-how-to-set-up-sepa-direct-debit.md) og [Foretag indbetalinger med tjenesten til konvertering af bankdata eller SEPA Kreditoverførsel](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).  

    Når du har oprettet dataudvekslingsdefinitionen for en bestemt datafil, kan du eksportere dataudvekslingsdefinitionen som en XML-fil, der kan bruges til hurtigt at aktivere import af den pågældende datafil. Dette beskrives i følgende fremgangsmåde:  

### <a name="to-export-a-data-exchange-definition-as-an-xml-file-for-use-by-others"></a>Sådan eksporteres en dataudvekslingsdefinition som en XML-fil, som andre kan bruge  
1. I feltet **Søg** skal du indtaste **Dataudvekslingsdefinitioner** og derefter vælge det relaterede link.  
2. Vælg den dataudvekslingsdefinition, som du vil udlæse.  
3. Vælg handlingen **Eksporter dataudvekslingsdefinition**.  
4. Gem den XML-fil, der repræsenterer dataudvekslingsdefinitionen i en passende lokation.  

    Hvis en definition til udveksling af data allerede er oprettet, skal du kun importere XML-filen til Data Exchange Framework. Dette beskrives i følgende fremgangsmåde:  

### <a name="to-import-an-existing-data-exchange-definition"></a>Sådan importeres en eksisterende dataudvekslingsdefinition  
1. Gem den XML-fil, der repræsenterer dataudvekslingsdefinitionen i en passende lokation.  
2. I feltet **Søg** skal du indtaste **Dataudvekslingsdefinitioner** og derefter vælge det relaterede link.  
3. Vælg handlingen **Ny**. Vinduet **Dataudvekslingsdefinition** åbnes.  
4. Vælg handlingen **Importer dataudvekslingsdefinition**.  
5. Vælg den fil, du gemte i trin 1.  

## <a name="see-also"></a>Se også  
[Konfigurere dataudveksling](across-set-up-data-exchange.md)  
[Fremgangsmåde: Konfigurere afsendelse og modtagelse af elektroniske dokumenter](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Fremgangsmåde: Opsætte SEPA-kreditoverførsel](finance-how-to-set-up-sepa-credit-transfer.md)  
[Fremgangsmåde: Konfigurere SEPA Direct Debit](finance-how-to-set-up-sepa-direct-debit.md)  
[Foretag indbetalinger med tjenesten til konvertering af bankdata eller SEPA Kreditoverførsel](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Indgående bilag](across-income-documents.md)  
[Generelle forretningsfunktioner](ui-across-business-areas.md)  

