---
title: Gegevens uitwisselen | Microsoft Docs
description: U kunt gegevens uitwisselen tussen Business Central en externe bestanden of streams voor veelvoorkomende bedrijfstaken, zoals het verzenden en ontvangen van elektronische documenten en het importeren en exporteren van bankbestanden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 29f7cbd99c867d01e6697aa87e39509a0d5b105e
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4753429"
---
# <a name="exchanging-data"></a>Gegevens uitwisselen
U kunt gegevens uitwisselen tussen [!INCLUDE[prod_short](includes/prod_short.md)] en externe bestanden of streams voor veelvoorkomende bedrijfstaken, zoals het verzenden en ontvangen van elektronische documenten en het importeren en exporteren van bankbestanden.  

Voordat u elektronische documenten kunt verzenden en ontvangen of bankbestanden kunt importeren en exporteren, moet u eerst het kader voor gegevensuitwisseling instelling om de gegevensbestanden of -stromen te verwerken. Daarnaast moet u gerelateerde gebieden instellen, zoals de klanten naar wie u elektronische facturen stuurt en de extensie AMC Banking 365 Fundamentals als u geconverteerde bankbestanden naar een externe serviceprovider verzendt. Zie voor meer informatie [Gegevensuitwisseling instellen](across-set-up-data-exchange.md).  

 In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.  

|**Als u dit wilt doen**|**Onderwerp**|  
|------------|-------------|  
|Converteer records van verkoopdocumenten in [!INCLUDE[prod_short](includes/prod_short.md)] naar een gestandaardiseerde indeling en verstuur ze als elektronische documenten die uw klanten kunnen ontvangen in hun systeem.|[Elektronische documenten verzenden](sales-how-to-send-electronic-documents.md)|  
|Verzend PDF- of afbeeldingsbestanden naar een aanbieder van OCR-services en ontvang deze terug als elektronische documenten die kunnen worden geconverteerd naar documentrecords in [!INCLUDE[prod_short](includes/prod_short.md)].|[OCR gebruiken om PDF- en afbeeldingsbestanden te converteren naar elektronische documenten](across-how-use-ocr-pdf-images-files.md)|  
|Elektronische documenten van de OCR-service of de service voor documentuitwisseling ontvangen in een gestandaardiseerde indeling die u kunt converteren naar de relevante documentrecords in [!INCLUDE[prod_short](includes/prod_short.md)].|[Elektronische documenten ontvangen en converteren](purchasing-how-to-receive-and-convert-electronic-documents.md)|  
|Voorbereiden van het importeren van een bankafschriftbestand importeren in de pagina **Betalingsreconciliatiedagboek** als de eerste stap bij de afstemming van betalingen of op de pagina **Bankreconciliatie** als eerste stap bij het afstemmen van bankrekeningen.|[De Envestnet Yodlee Bank Feeds-service instellen](bank-how-setup-bank-statement-service.md)|  
|Betalingen uit de pagina **Betalingsdagboek** exporteren naar een bankbestand dat u uploadt naar uw elektronische bankrekening voor verwerking.|[Betalingen naar een bankbestand exporteren](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)|
|Elektronische betalingen doen op basis van de EU-norm voor SEPA-krediettransfers.|[Betalingen doen met de extensie AMC Banking 365 Fundamentals of SEPA-kredietoverdracht](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)|  
|Vraag uw bank bedragen van betalingen van bankrekeningen van uw klanten over te brengen naar uw bedrijfsrekening volgens uw instellingen voor automatische incasso van SEPA.|[SEPA-verzamelingsposten van automatische incasso maken en exporteren naar een bankbestand](finance-collect-payments-with-sepa-direct-debit.md#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file)|  
|Gebruik een serviceprovider van valutawisselkoersen om de pagina **Valuta's** bij te werken.|[Valutawisselkoersen bijwerken](finance-how-update-currencies.md)|  
|Bekijk welke bestandselementen worden toegewezen aan velden in [!INCLUDE[prod_short](includes/prod_short.md)] tijdens het importeren van SEPA CAMT-afschriftbestanden.|[Veldtoewijzing bij het importeren van SEPA CAMT-bestanden](across-field-mapping-when-importing-sepa-camt-files.md)|  
|Bekijk welke velden in [!INCLUDE[prod_short](includes/prod_short.md)] zijn toegewezen aan bestandselementen wanneer u betalingsbestanden exporteert met behulp van de extensie AMC Banking 365 Fundamentals.|[Veldtoewijzing bij de export van betalingsbestanden met behulp van de extensie AMC Banking 365 Fundamentals](across-field-mapping-when-exporting-payment-files-using-bank-data-conversion-service.md)|  

## <a name="see-also"></a>Zie ook  
[Gegevensuitwisseling instellen](across-set-up-data-exchange.md)  
[Gegevens elektronisch uitwisselen](across-data-exchange.md)  
[Verkopen factureren](sales-how-invoice-sales.md)   
[Inkopen vastleggen](purchasing-how-record-purchases.md)  
[Inkomende documenten](across-income-documents.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)  
