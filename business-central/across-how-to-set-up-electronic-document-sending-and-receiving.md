---
title: Verzending en ontvangst van elektronische documenten instellen | Microsoft Docs
description: Als alternatief voor het e-mailen van bestandsbijlagen kunt u zakelijke documenten elektronisch verzenden en ontvangen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="set-up-electronic-document-sending-and-receiving"></a>Verzending en ontvangst van elektronische documenten instellen

Als alternatief voor het e-mailen van bestandsbijlagen kunt u zakelijke documenten elektronisch verzenden en ontvangen. Een elektronisch document is een standaardbestand dat een bedrijfsdocument vertegenwoordigt, zoals een factuur van een leverancier die kan worden ontvangen en geconverteerd naar een inkoopfactuur in [!INCLUDE[prod_short](includes/prod_short.md)]. De uitwisseling van elektronische documenten tussen twee handelspartners wordt uitgevoerd door een externe provider van services voor documentuitwisseling. De algemene versie van [!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt het verzenden en ontvangen van elektronische facturen en creditnota's in de PEPPOL-indeling, die wordt ondersteund door de grootste aanbieders van documentuitwisselingsservices. Een belangrijke aanbieder van services voor documentuitwisseling is vooraf geconfigureerd en gereed om te worden ingesteld voor uw bedrijf.  

Vanuit PDF- of afbeeldingsbestanden die inkomende documenten vertegenwoordigen kunt u een externe OCR-service (Optical Character Recognition; optische tekenherkenning) elektronische documenten laten maken die u vervolgens naar documentrecords kunt converteren in [!INCLUDE[prod_short](includes/prod_short.md)], zoals u doet voor elektronische PEPPOL-documenten. Bijvoorbeeld, wanneer u facturen in PDF-indeling van uw leverancier ontvangt, kunt u deze naar de OCR-service verzenden vanaf de pagina **Inkomende documenten**. Na enkele seconden krijgt u het bestand weer terug als elektronische factuur die kan worden geconverteerd naar een inkoopfactuur voor de leverancier. Als u het bestand per e-mail naar de OCR-service verzendt, wordt automatisch een nieuwe inkomende documentrecord gemaakt wanneer u het elektronische document terugkrijgt.  

De indeling **PEPPOL** voor elektronische documenten is vooraf geconfigureerd zodat u elektronische facturen en creditnota's kunt verzenden in de PEPPOL-indeling. Eerst moet u diverse stamgegevens instellen, zoals bedrijfsgegevens, klanten, artikelen en eenheden. Deze worden gebruikt om de zakelijke partners en artikelen te identificeren wanneer gegevens in velden in [!INCLUDE[prod_short](includes/prod_short.md)] worden geconverteerd naar elementen in het uitgaande documentbestand. Tot slot moet u de indeling op de pagina **Elektronische documentindeling** selecteren voor elke klant aan wie u elektronische PEPPOL-documenten stuurt. Zie [Elektronische documenten verzenden](sales-how-to-send-electronic-documents.md) voor meer informatie.  

De gegevensuitwisselingsdefinities **PEPPOL – Factuur** en **PEPPOL – Creditnota** zijn vooraf geconfigureerd zodat u elektronische facturen en creditnota's kunt ontvangen in de PEPPOL-indeling. Eerst moet u diverse stamgegevens instellen, zoals bedrijfsgegevens, leveranciers, artikelen en eenheden. Deze worden gebruikt om de zakelijke partners en artikelen te identificeren wanneer gegevens en elementen in het inkomende documentbestand worden geconverteerd naar velden in [!INCLUDE[prod_short](includes/prod_short.md)]. Tot slot moet u de gegevensuitwisselingsdefinitie op de pagina **Inkomende documenten** selecteren voor elk inkomend elektronisch document dat u wilt converteren naar een inkoopdocument in [!INCLUDE[prod_short](includes/prod_short.md)].  

De gegevensuitwisselingsdefinitie **OCR - Factuur** is vooraf geconfigureerd om u in staat te stellen elektronische documenten te ontvangen die zijn gegenereerd door de OCR-service. Als u bijvoorbeeld een factuur wilt ontvangen als een elektronisch OCR-document, stelt u stamgegevens in en verwerkt u het document op dezelfde manier als bij het ontvangen van een elektronisch PEPPOL-document. Zie [OCR gebruiken om PDF- en afbeeldingsbestanden te converteren naar elektronische documenten](across-how-use-ocr-pdf-images-files.md) voor meer informatie.  

De vooraf geconfigureerd services voor documentuitwisseling en OCR moeten zijn ingeschakeld voordat u verzendt of ontvangt. Zie [Een service voor documentuitwisseling instellen](across-how-to-set-up-a-document-exchange-service.md) voor meer informatie.  

Het onderwerp bevat de volgende procedures:  

* Het bedrijf instellen voor verzending en ontvangst van elektronische documenten  
* Btw-boekingen instellen voor verzending en ontvangst van elektronische documenten  
* Landen/regio's instellen voor verzending en ontvangst van elektronische documenten  
* Artikelen instellen voor verzending en ontvangst van elektronische documenten  
* Eenheden instellen voor verzending en ontvangst van elektronische documenten  
* Klanten instellen voor de verzending van elektronische documenten.  
* De indeling **PEPPOL** selecteren voor de verzending van elektronische documenten  
* Leveranciers instellen voor de ontvangst van elektronische documenten.  
* De gegevensuitwisselingsdefinitie **PEPPOL - Factuur** selecteren voor de ontvangst van elektronische documenten  
* De grootboekrekening instellen die moet worden gebruikt voor nieuwe inkoopfactuurregels voor niet\-identificeerbare artikelen en niet\-artikelen  

### <a name="to-set-up-the-company-for-electronic-document-sending-and-receiving"></a>Het bedrijf instellen voor verzending en ontvangst van elektronische documenten

1. Geef in het tekstvak **Zoeken** **Bedrijfsgegevens** op en kies vervolgens de gerelateerde koppeling.  
2. Vul op het sneltabblad **Algemeen** de velden in zoals beschreven in de volgende tabel.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Identificeer uw bedrijf.<br /><br /> Bijvoorbeeld, als u elektronische facturen verstuurt in de bestandsindeling PEPPOL, wordt de waarde in dit veld gebruikt om het element **EndPointID** onder het knooppunt **AccountingSupplierParty** in het bestand in te vullen. Het nummer is gebaseerd op de GS1-norm die voldoet aan ISO 6523.|  
    |**Btw-registratienummer**|Geeft het btw-nummer van uw bedrijf op.|  
    |**Divisie**|Als uw bedrijf is ingesteld met een divisie, moet het veld **Land-/regiocode** worden ingevuld.|  

### <a name="to-set-up-vat-posting-for-electronic-document-sending-and-receiving"></a>Btw-boekingen instellen voor verzending en ontvangst van elektronische documenten

1. Voer in het tekstvak **Zoeken** de tekst **Btw-boekingsinstellingen** in en kies de gerelateerde koppeling.  
2. Voor elke regel voor btw-boekingsinstellingen die u gebruikt voor elektronische documenten, vult u het veld in zoals beschreven in de volgende tabel.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Belastingcategorie**|Geef de btw-categorie op.<br /><br /> Bijvoorbeeld, als u elektronische facturen verstuurt in de bestandsindeling PEPPOL, wordt de waarde in dit veld gebruikt om het element **TaxApplied** onder het knooppunt **AccountingSupplierParty** in het bestand in te vullen. De code is gebaseerd op de UNCL5305-norm.|  

### <a name="to-set-up-countriesregions-for-electronic-document-sending-and-receiving"></a>Landen/regio's instellen voor verzending en ontvangst van elektronische documenten

1. Voer in het tekstvak **Zoeken** **Landen/regio's** in en kies vervolgens de gerelateerde koppeling.  
2. Voor elk land of elke regio waarmee u elektronische documenten uitwisselt, vult u het veld in zoals beschreven in de volgende tabel.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Btw-regeling**|Identificeer de nationale instantie die het btw-nummer van het land\/de regio uitgeeft in verband met het verzenden van elektronische documenten.<br /><br /> Bijvoorbeeld, als u elektronische facturen verstuurt in de bestandsindeling PEPPOL, wordt de waarde in dit veld gebruikt om het kenmerk **SchemeID** voor het element **EndPointID** onder de knooppunten **AccountingSupplierParty** en **AccountingCustomerParty** in het bestand in te vullen.<br /><br /> Het veld **Btw-regeling** wordt alleen gebruikt als het veld **GLN** op de pagina **Bedrijfsgegevens** niet is ingevuld. **Opmerking:** de waarde in het veld **Code** op de pagina **Landen\/regio's** moet voldoen aan ISO 3166\-1:Alpha2.|  

### <a name="to-set-up-items-for-electronic-document-sending-and-receiving"></a>Artikelen instellen voor verzending en ontvangst van elektronische documenten

1. Geef in het vak **Zoeken** **Artikelen** op en kies vervolgens de gerelateerde koppeling.  
2. Voor elk artikel dat u koopt of verkoopt op elektronische documenten, vult u het veld in zoals beschreven in de volgende tabel.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**GTIN**|Identificeert het artikel met betrekking tot het verzenden en ontvangen van elektronische documenten. Voor de PEPPOL-indeling wordt het veld als volgt gebruikt:<br /><br /> Als voor het element **StandardItemIdentification\/ID** het kenmerk **SchemeID** is ingesteld op **GTIN**, wordt het element toegewezen aan het veld **GTIN** op de artikelkaart.|  

### <a name="to-set-up-units-of-measure-for-electronic-document-sending-and-receiving"></a>Eenheden instellen voor verzending en ontvangst van elektronische documenten

1. Voer in het tekstvak **Zoeken** de tekst **Eenheden** in en kies vervolgens de gerelateerde koppeling.  
2. Voor elke eenheid die u gebruikt voor artikelen op elektronische documenten, vult u het veld in zoals beschreven in de volgende tabel.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Internationale standaardcode**|Geef de eenheidscode op volgens de UNECERec20-norm in verband met het verzenden van elektronische documenten.<br /><br /> Bijvoorbeeld, als u elektronische facturen verstuurt in de bestandsindeling PEPPOL, wordt de waarde in dit veld gebruikt om het kenmerk **unitCode** van het element **InvoicedQuantity** onder het knooppunt **InvoiceLine** in het bestand in te vullen. **Opmerking:** als het veld **Maateenheid** op de verkoopregel leeg is, wordt de UNECERe20-standaardwaarde voor 'Stuks' \(H87\) standaard ingevoegd. Zie voor meer informatie en een lijst met geldige eenheidcodes [Aanbeveling nr. 20 \- In internationale handel gebruikte maateenheden](https://www.unece.org/fileadmin/DAM/cefact/recommendations/rec20/rec20_rev3_Annex2e.pdf).|  

### <a name="to-set-up-customers-for-electronic-document-sending"></a>Klanten instellen voor de verzending van elektronische documenten.

1. Geef in het **Zoeken** **Klanten** op en kies vervolgens de gerelateerde koppeling.  
2. Voor elke klant aan wie u elektronische documenten verzendt, vult u de velden in zoals beschreven in de volgende tabel.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Identificeer de klant.<br /><br /> Bijvoorbeeld, als u elektronische facturen verstuurt in de bestandsindeling PEPPOL, wordt de waarde in dit veld gebruikt om het element **EndPointID** onder het knooppunt **AccountingCustomerParty** in het bestand in te vullen. Het nummer is gebaseerd op de GS1-norm die voldoet aan ISO 6523.<br /><br /> Als het veld **GLN** leeg is, wordt de waarde in het veld **Btw-nummer** gebruikt.|  
    |**Btw-registratienummer**|Geef het btw-nummer van de klant op. **Tip:** kies in ondersteunde gelokaliseerde versies de detailknop om de webservice te gebruiken die verifieert of het nummer in het nationale bedrijfregister bestaat.|  
    |**Divisie**|Als de klant is ingesteld met een divisie, moet het veld **Land-/regiocode** worden ingevuld.|  

    U kunt elke klant instellen met een voorkeursmethode voor de verzending van bedrijfsdocumenten, zodat u niet elke keer dat u een document verzendt naar de klant, een verzendoptie hoeft te kiezen. Zie [Verzendprofielen voor documenten instellen](sales-how-setup-document-send-profiles.md) voor meer informatie.  

### <a name="to-select-the-peppol-electronic-document-format-for-electronic-document-sending"></a>De indeling PEPPOL selecteren voor de verzending van elektronische documenten
1. Voer in het vak **Zoeken** de tekst **Verzendprofielen document** in en kies de gerelateerde koppeling.  
2. Open een bestaand verzendprofiel voor documenten, of maak een nieuw profiel. Zie [Verzendprofielen voor documenten instellen](sales-how-setup-document-send-profiles.md) voor meer informatie.  
3. Kies op de pagina **Verzendprofiel van document** de optie **Elektronische indeling**, selecteer de regel voor PEPPOL en klik op **OK**.  
4. Selecteer in het veld **Elektronisch document** de optie **Ja (via service voor documentuitwisseling)**.  

    > [!NOTE]  
    >  [!INCLUDE[prod_short](includes/prod_short.md)] detecteert automatisch of het document een factuur of creditnota is en kiest de bijbehorende PEPPOL-indeling.  

5. Als u dit verzendprofiel wilt toepassen op alle klanten, schakelt u het selectievakje **Standaard** op het sneltabblad **Algemeen** in. Als u het profiel alleen wilt toepassen op specifieke klanten, vult u het veld **Verzendprofiel van document** op de desbetreffende klantenkaarten in. Zie [Verzendprofielen voor documenten instellen](sales-how-setup-document-send-profiles.md) voor meer informatie.  

    U kunt nu het elektronische document met de geconverteerde gegevens verzenden. Zie [Elektronische documenten verzenden](sales-how-to-send-electronic-documents.md) voor meer informatie.  

### <a name="to-set-up-vendors-for-electronic-document-receiving"></a>Leveranciers instellen voor de ontvangst van elektronische documenten.
1. Geef in het vak **Zoeken** **Leveranciers** op en kies vervolgens de gerelateerde koppeling.  
2. Voor elke leverancier van wie u elektronische documenten ontvangt, vult u de velden in zoals beschreven in de volgende tabel.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**GLN**|Identificeer de leverancier.<br /><br /> Bijvoorbeeld, als u elektronische facturen ontvangt in de bestandsindeling PEPPOL, wordt de waarde in dit veld gebruikt om het element **EndPointID** onder het knooppunt **AccountingSupplierParty** in het bestand in te vullen. Het nummer is gebaseerd op de GS1-norm die voldoet aan ISO 6523.<br /><br /> Als het veld **GLN** leeg is, wordt de waarde in het veld **Btw-nummer** gebruikt.|  
    |**Btw-registratienummer**|Geef het btw-nummer van de leverancier op. **Tip:** kies in ondersteunde gelokaliseerde versies de detailknop om de webservice te gebruiken die verifieert of het nummer in het nationale bedrijfregister bestaat.|  
    |**Divisie**|Als de leverancier is ingesteld met een divisie, moet het veld **Land-/regiocode** worden ingevuld.|  

### <a name="to-select-the-peppol---invoice-data-exchange-definition-for-electronic-document-receiving"></a>De gegevensuitwisselingsdefinitie PEPPOL - Factuur selecteren voor de ontvangst van elektronische documenten
1. Voer in het tekstvak **Zoeken** de tekst **Inkomende documenten** in en kies vervolgens de gerelateerde koppeling.  
2. Op de regel voor het elektronische document dat u wilt ontvangen en converteren, kiest u het veld **Soort gegevensuitwisseling** en selecteert u vervolgens **PEPPOLINVOICE**.  

     Als het te ontvangen document een creditnota is, selecteert u **PEPPOLCREDITMEMO**.  

    U kunt het elektronische document nu ontvangen door het proces voor gegevensconversie te starten op de pagina **Inkomende documenten**. Zie voor meer informatie [Elektronische documenten ontvangen en converteren](purchasing-how-to-receive-and-convert-electronic-documents.md).  

### <a name="to-set-up-the-gl-account-to-use-on-new-purchase-invoice-lines-for-non-identifiable-items-and-non-items"></a>De grootboekrekening instellen die moet worden gebruikt voor nieuwe inkoopfactuurregels voor niet-identificeerbare artikelen en niet-artikelen
1. Voer in het vak **Zoeken** de tekst **Inkoopinstellingen** in en kies vervolgens de gerelateerde koppeling.  
2. Vul op het sneltabblad **Standaardrekeningen** het veld in, zoals in de volgende tabel is beschreven.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Grootboekrekening voor niet-artikelregels**|Geeft de Grootboekrekening aan die automatisch wordt ingevoegd op inkoopregels die aan de hand van elektronische documenten worden gemaakt wanneer de inkomende documentregels geen identificeerbaar artikel bevatten. Elke inkomende documentregel die geen GTIN of artikelnummer van de leverancier heeft, wordt geconverteerd naar een inkoopregel van het soort **Grootboekrekening** en het veld **Nr.** op de inkoopregel bevat de rekening die u selecteert in het veld **Grootboekrekening voor niet-artikelregels**.<br /><br /> Als u niets invult in het veld **Grootboekrekening voor niet-artikelregels** en het inkomende document regels heeft zonder identificeerbare artikelen, wordt het inkoopdocument niet gemaakt. In een foutbericht krijgt u de instructie om het veld **Grootboekrekening voor niet-artikelregels** in te vullen voordat u de taak kunt voltooien.|  

## <a name="see-also"></a>Zie ook
[Gegevens elektronisch uitwisselen](across-data-exchange.md)   
[Verkopen factureren](sales-how-invoice-sales.md)   
[Inkopen vastleggen](purchasing-how-record-purchases.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
