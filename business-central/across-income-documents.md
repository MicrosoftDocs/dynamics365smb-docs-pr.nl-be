---
title: Werken met inkomende documenten
description: 'U kunt inkomende externe bedrijfsdocumenten, zoals betalingsontvangsten of PDF''s beheren, OCR-taken beheren en elektronische bestanden naar documenten en records omzetten.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="incoming-documents" />Inkomende documenten

Externe zakelijke documenten kunnen uw bedrijf binnenkomen als e-mailbijlage of als papieren exemplaar dat u kunt scannen. Dit scenario is meestal bij aankopen, waarbij dergelijke inkomende documentbestanden betalingsontvangsten voor kosten of kleine inkopen vertegenwoordigen.

Op de pagina **Inkomende documenten** kunt u verschillende functies gebruiken om onkostenbewijzen te controleren, OCR-taken te beheren en inkomende documentbestanden handmatig of automatisch te converteren naar de relevante documenten of dagboekregels. De externe bestanden kunnen worden gekoppeld in elke procesfase, inclusief naar geboekte documenten en naar de resulterende leverancier, klant en grootboekposten.

## <a name="usage-scenario" />Gebruiksscenario

U kunt bestanden of papieren exemplaren die u van uw handelspartners hebt ontvangen, registreren in [!INCLUDE[prod_short](includes/prod_short.md)] en een documentrecord maken. Bijvoorbeeld een inkoop- of verkoopfactuur, creditnota of een dagboekregel.

Upload de ontvangen bestanden - of gebruik de camera van het apparaat om een foto te maken - en maak items om de externe documenten voor te stellen. In PDF- of afbeeldingsbestanden die inkomende documenten vertegenwoordigen, kunt u desgewenst een externe OCR-service (Optical Character Recognition - optische tekenherkenning) elektronische documenten laten genereren die naar documentrecords kunnen worden geconverteerd binnen [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> De OCR-functie wordt geleverd door externe providers. Kies een servicepakket dat past bij uw organisatie en/of land/regio. U vindt services die compatibel zijn met [!INCLUDE[prod_short](includes/prod_short.md)] en details over beschikbare functies op [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

Bijvoorbeeld, wanneer u facturen in PDF-indeling van uw leverancier ontvangt, kunt u deze naar de OCR-service verzenden vanaf de pagina **Inkomende documenten**. Als alternatief bieden sommige OCR-providers de mogelijkheid om bestanden te verwerken die zijn doorgestuurd naar een speciaal e-mailadres, dat vervolgens automatisch een gerelateerde inkomende documentrecord maakt. Na enkele seconden krijgt u het bestand weer terug van de OCR-service als een elektronische factuur die kan worden geconverteerd naar een inkoopfactuur voor de leverancier.

> [!TIP]
> Maak inkomende documentrecords in [!INCLUDE[prod_short](includes/prod_short.md)] rechtstreeks vanuit e-mails verzonden door leveranciers met behulp van de Outlook-invoegtoepassing. Zie [Business Central als uw bedrijfsinbox gebruiken in Outlook](work-outlook-addin.md) voor meer informatie.

## <a name="incoming-document-features" />Functies voor inkomende documenten

Het proces voor inkomende documenten kan bestaan uit de volgende voornaamste activiteiten:

* Registreer op een van de volgende manieren de externe documenten in [!INCLUDE[prod_short](includes/prod_short.md)] door regels te maken op de pagina **Inkomende documenten**:
  * Handmatig vanaf een pc of een mobiel apparaat, op een van de volgende manieren:
    * Gebruik de knop **Maken van bestand**, upload een bestand en vul vervolgens de relevante velden op de pagina **Inkomend document** in.
    * Gebruik de knop **Nieuw**, vul de relevante velden op de pagina **Inkomend document** in en koppel het gerelateerde bestand handmatig.
    * Gebruik vanaf een tablet of een telefoon de knop **Maken van camera** om een nieuwe inkomende documentrecord te maken met de ingebouwde camera van het apparaat.
  * Automatisch, door het document van de OCR-service te ontvangen als een elektronisch document nadat u het gerelateerde PDF- of afbeeldingsbestand hebt geüpload naar een OCR-service. Het sneltabblad **Financiële informatie** wordt automatisch ingevuld op de pagina **Inkomend document**.
* Gebruik een externe OCR-service om PDF- of afbeeldingsbestanden te laten omzetten naar elektronische documenten die kunnen worden geconverteerd naar documentrecords in [!INCLUDE[prod_short](includes/prod_short.md)].
* Maak nieuwe documenten of dagboekregels voor inkomende documentrecords door de informatie in te voeren die u leest uit inkomende documentbestanden.
* Koppel inkomende documentbestanden aan inkoop- en verkoopdocumenten van elke status, inclusief de leveranciers-, klant- en grootboekposten die het resultaat zijn van boeking.
* Bekijk inkomende documentrecords en de bijlagen ervan vanuit elk inkoop- en verkoopdocument of elke post, of zoek alle grootboekposten zonder inkomende documentrecords op de pagina **Rekeningschema**.

> [!NOTE]
> Bestanden bij kaarten en documenten op het tabblad **Bijlagen** worden niet opgenomen op de pagina **Inkomende documenten**. Zie voor meer informatie [Bijlagen, koppelingen en notities op kaarten en in documenten beheren](ui-how-add-link-to-record.md).

| Tot | Zie |
| --- | --- |
| Stel de functie **Inkomende documenten** in en stel de OCR-service in. |[Inkomende documenten instellen](across-how-setup-income-documents.md) |
| Maak inkomende documentrecords handmatig of automatisch door een foto te maken van een papieren ontvangstbewijs, bijvoorbeeld. |[Inkomende documentrecords maken](across-how-create-income-document-records.md) |
| Gebruik een OCR-service om PDF- en afbeeldingsbestanden naar elektronische documenten om te zetten die bijvoorbeeld kunnen worden geconverteerd naar inkoopfacturen in [!INCLUDE[prod_short](includes/prod_short.md)]. Train de OCR-service om fouten te voorkomen als de volgende keer vergelijkbare gegevens worden verwerkt. |[OCR gebruiken om PDF- en afbeeldingsbestanden te converteren naar elektronische documenten](across-how-use-ocr-pdf-images-files.md) |
| Verbind of verwijder inkomende documentrecords voor elk niet-geboekte verkoop- of inkoopdocument en voor elke klant- of grootboekpost uit het document of de post. |[Inkomende documentrecords maken direct van documenten en posten](across-how-connect-disconnect-income-document-records.md) |
| Vanuit de pagina's **Rekeningschema** en **Grootboekposten** zoekt u naar grootboekposten voor geboekte documenten die geen inkomende documentrecords hebben, en koppelt u deze centraal aan bestaande records of maakt u nieuwe records met gekoppelde documentbestanden. |[Geboekte documenten zonder inkomende documentrecords zoeken](across-how-find-posted-documents-without-income-document-records.md) |
| Krijg beter overzicht krijgen door inkomende documentrecords in te stellen op *Verwerkt* en ze te verwijderen uit de standaardweergave. |[Vele inkomende documentrecords beheren](across-how-manage-many-income-document-records.md) |

## <a name="see-related-microsoft-trainingtrainingmodulesincoming-documents-dynamics-365-business-central" />Zie gerelateerde [Microsoft-training](/training/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also" />Zie ook

[Inkoop](purchasing-manage-purchasing.md)  
[Geboekte documenten bewerken](across-edit-posted-document.md)  
[Gegevens elektronisch uitwisselen](across-data-exchange.md)  
[Business Central en integratie met OneDrive voor Bedrijven](across-onedrive-overview.md)  
[Business Central gebruiken als uw bedrijfsinbox in Outlook](work-outlook-addin.md)  
[Documenten en e-mails verzenden](ui-how-send-documents-email.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
