---
title: Gegevens uitwisselen | Microsoft Docs
description: U kunt gegevens uitwisselen tussen [!INCLUDE[d365fin](includes/d365fin_md.md)] en externe bestanden of streams voor veelvoorkomende bedrijfstaken, zoals het verzenden en ontvangen van elektronische documenten en het importeren en exporteren van bankbestanden.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 81781676adf27a4f1c1d478bb2b4bd8248551468
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="exchanging-data"></a>Gegevens uitwisselen
U kunt gegevens uitwisselen tussen [!INCLUDE[d365fin](includes/d365fin_md.md)] en externe bestanden of streams voor veelvoorkomende bedrijfstaken, zoals het verzenden en ontvangen van elektronische documenten en het importeren en exporteren van bankbestanden.  

Voordat u documenten elektronisch kunt verzenden en ontvangen of bankbestanden kunt importeren en exporteren, moet u het kader voor gegevensuitwisseling instellen om de betreffende gegevensbestanden of streams te verwerken. Daarnaast moet u gerelateerde gebieden instellen. Dit zijn bijvoorbeeld stamgegevens voor klanten aan wie u elektronische facturen verzendt, of de conversieservice voor bankgegevens als u conversies van bankbestanden stuurt naar een externe serviceprovider. Zie voor meer informatie [Gegevensuitwisseling instellen](across-set-up-data-exchange.md).  

 In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.  

|**Als u dit wilt doen**|**Onderwerp**|  
|------------|-------------|  
|Converteer records van verkoopdocumenten in [!INCLUDE[d365fin](includes/d365fin_md.md)] naar een gestandaardiseerde indeling en verstuur ze als elektronische documenten die uw klanten kunnen ontvangen in hun systeem.|[Procedure: Elektronische documenten verzenden](sales-how-to-send-electronic-documents.md)|  
|Verzend PDF- of afbeeldingsbestanden naar een aanbieder van OCR-services en ontvang deze terug als elektronische documenten die kunnen worden geconverteerd naar documentrecords in [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Procedure: OCR gebruiken om PDF- en afbeeldingsbestanden te converteren naar elektronische documenten](across-how-use-ocr-pdf-images-files.md)|  
|Elektronische documenten van de OCR-service of de service voor documentuitwisseling ontvangen in een gestandaardiseerde indeling die u kunt converteren naar de relevante documentrecords in [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Procedure: Elektronische documenten ontvangen en converteren](purchasing-how-to-receive-and-convert-electronic-documents.md)|  
|Een bankafschriftbestand importeren in het venster **Betalingsreconciliatiedagboek** als de eerste stap bij de afstemming van betalingen of in het venster **Bankreconciliatie** als eerste stap bij het afstemmen van bankrekeningen.|[Procedure: De service Envestnet Yodlee Bank Feeds instellen](bank-how-setup-bank-statement-service.md)|  
|Betalingen uit het venster **Betalingsdagboek** exporteren naar een bankbestand dat u uploadt naar uw elektronische bankrekening voor verwerking.|[Procedure: Betalingen naar een bankbestand exporteren](payables-how-export-payments-bank-file.md)|  
|Vraag uw bank bedragen van betalingen van bankrekeningen van uw klanten over te brengen naar uw bedrijfsrekening volgens uw instellingen voor automatische incasso van SEPA.|[Procedure: SEPA-verzamelingsposten van automatische incasso maken en exporteren naar een bankbestand](finance-how-create-sepa-direct-debit-collection-entries-export-bank-file.md)|  
|Gebruik een serviceprovider van valutawisselkoersen om het venster **Valuta's** bij te werken.|[Procedure: Valutawisselkoersen bijwerken](finance-how-update-currencies.md)|  
|Bekijk welke bestandselementen worden toegewezen aan velden in [!INCLUDE[d365fin](includes/d365fin_md.md)] tijdens het importeren van SEPA CAMT-afschriftbestanden.|[Veldtoewijzing bij het importeren van SEPA CAMT-bestanden](across-field-mapping-when-importing-sepa-camt-files.md)|  
|Bekijk welke velden in [!INCLUDE[d365fin](includes/d365fin_md.md)] worden toegewezen aan bestandselementen bij het exporteren van betalingsbestanden via de conversieservice voor bankgegevens.|[Veldtoewijzing bij het exporteren van betalingsbestanden via conversieservice bankgegevens](across-field-mapping-when-exporting-payment-files-using-bank-data-conversion-service.md)|  

## <a name="see-also"></a>Zie ook  
[Gegevensuitwisseling instellen](across-set-up-data-exchange.md)  
[Gegevens als elektronische documenten uitwisselen](across-data-exchange.md)  
[Procedure: Verkoopbewerkingen](sales-how-invoice-sales.md)   
[Procedure: Inkopen vastleggen](purchasing-how-record-purchases.md)  
[Inkomende documenten](across-income-documents.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)  

