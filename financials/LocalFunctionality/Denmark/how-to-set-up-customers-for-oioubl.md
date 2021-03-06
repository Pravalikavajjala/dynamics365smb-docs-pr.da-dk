fhow-register-new-customers---title: Sådan opsættes kunder til OIOUBL | Microsoft Docs-beskrivelse: Hvis du vil oprette Offentlig Information Online UBL (OIOUBL)-dokumenter for debitorer i den offentlige sektor, skal du tilføje OIOUBL-oplysninger til de relevante debitorer.
tjenester: projekt madeira documentationcenter: "forfatter: SorenGP

    ms.service: dynamics365-financials
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 07/01/2017
    ms.author: sgroespe

---
# <a name="how-to-set-up-customers-for-oioubl"></a>Fremgangsmåde: Konfigurere kunder til OIOUBL
Hvis du vil oprette OIOUBL-dokumenter (Offentlig Information Online UBL) for debitorer i den offentlige sektor, skal du tilføje OIOUBL-oplysninger for de relevante debitorer.  

 I dette emne beskrives kun de felter, der gælder for OIOUBL. Du kan finde flere oplysninger i [Fremgangsmåde: Registrere nye debitorer](../../sales-how-register-new-customers.md).  

### <a name="to-set-up-customers-for-oioubl"></a>Sådan konfigureres kunder til OIOUBL  

1.  Vælg ikonet ![Søg efter side eller rapport](../../media/ui-search/search_small.png "Ikonet Søg efter side eller rapport"), angiv **Debitorer**, og vælg derefter det relaterede link.  
2.  Åbn den kunde, du vil konfigurere aktivere til OIOUBL.  
3.  Udfyld felterne i oversigtspanelet **Fakturering** som beskrevet i følgende tabel.  

    |Felt|Description|  
    |---------------------------------|---------------------------------------|  
    |**EAN-nr.**|Angiv EAN-lokationsnummeret (European Article Numbering) for kunden. Du kan finde flere oplysninger under [EAN-lokationsnummer](ean-location-number.md).|  
    |**Kontokode**|Angiv kontokoden for kunden.<br /><br /> Kunder i den offentlige sektor angiver en kontokode, når de afgiver en bestilling eller rekvisition. Baseret på værdien i dette felt medtages kontokoden i OIOUBL-dokumenter, du opretter i [!INCLUDE[d365fin](../../includes/d365fin_md.md)]. Ifølge **Lov om Offentlige Betalinger** og relaterede love har kunden ret til at tilbageholde betaling, indtil der modtages en faktura med den relevante kontokode. Du kan finde flere oplysninger i Kontokode.|  
    |**OIOUBL-profilkode**|Angiver den profil, som denne kunde kræver for elektroniske dokumenter, hvis den er anderledes end den standardprofil, du har angivet i vinduet **Salgsopsætning**.|  
    |**OIOUBL-profilkode kræves**|Angiver, om debitoren kræver en profilkode til elektroniske dokumenter. **Tip:** Hvis feltet **OIOUBL-profilkode kræves** er markeret, kan du ikke bogføre et salgsdokument for debitoren, medmindre du har angivet en profil.|  

 Disse felter er specifikke for OIOUBL. De værdier, der bruges i alle OIOUBL-dokumenter, du opretter for denne kunde. Du kan finde flere oplysninger i [Oversigt over elektronisk OIOUBL-fakturering](oioubl-electronic-invoicing-overview.md).  

## <a name="see-also"></a>Se også  
[Lokal funktionalitet for Danmark](denmark-local-functionality.md)  
 [Fremgangsmåde: Registrere nye debitorer](../../sales-how-register-new-customers.md)   
 [Fremgangsmåde: Konfigurere OIOUBL](how-to-set-up-oioubl.md)   
 [Fremgangsmåde: Oprette elektroniske dokumenter ved hjælp af OIOUBL](how-to-create-electronic-documents-by-using-oioubl.md)   
 [Oversigt over elektronisk OIOUBL-fakturering](oioubl-electronic-invoicing-overview.md)   
 [EAN-lokationsnummer](ean-location-number.md)
