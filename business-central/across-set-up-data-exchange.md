---
title: Gegevensuitwisseling instellen om bestanden te verzenden en ontvangen
description: 'Stel het raamwerk voor gegevensuitwisseling in om gegevens uit te wisselen met externe bestanden, om elektronische documenten te verzenden en ontvangen of om bankbestanden te importeren en exporteren.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/11/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="setting-up-data-exchange"></a>Gegevensuitwisseling instellen

Voordat u documenten elektronisch kunt verzenden en ontvangen of bankbestanden kunt importeren en exporteren, moet u het kader voor gegevensuitwisseling instellen om de betreffende bestanden te verwerken. Daarnaast moet u gerelateerde gebieden instellen, zoals de klanten naar wie u elektronische facturen stuurt of de extensie AMC Banking 365 Fundamentals als u de externe serviceprovider gebruikt om uw bankbestanden te converteren. Zie [Gegevens elektronische uitwisselen](across-data-exchange.md) voor meer informatie.  

 Wanneer [!INCLUDE[prod_short](includes/prod_short.md)] is ingesteld voor gegevensuitwisseling met externe bestanden, kunnen gebruikers de instellingen gebruiken in algemene bedrijfstaken, zoals het verzenden en ontvangen van elektronische documenten en het importeren en exporteren van bankbestanden.  

 In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.  

|**Als u dit wilt doen**|**Onderwerp**|  
|------------|-------------|  
|De vooraf geconfigureerde service voor documentuitwisseling instellen voor het verzenden en ontvangen van elektronische documenten van en naar [!INCLUDE[prod_short](includes/prod_short.md)].|[Een service voor documentuitwisseling instellen](across-how-to-set-up-a-document-exchange-service.md)|  
|De vooraf geconfigureerde OCR-service instellen om PDF- of afbeeldingsbestanden in elektronische documenten om te zetten die kunnen worden geconverteerd naar documentrecords in [!INCLUDE[prod_short](includes/prod_short.md)]|[Inkomende documenten instellen](across-how-setup-income-documents.md)|  
|Stel één van twee vooraf geconfigureerde services voor bijgewerkte wisselkoersen in om de meest recente valutawisselkoersen op de pagina **Valuta's** te bekijken.|[Valutawisselkoersen bijwerken](finance-how-update-currencies.md)|  
|Diverse hoofdgegevens instellen, zoals bedrijfsgegevens, klanten, leveranciers, artikelen en eenheden, die betrekking hebben op het toewijzen van gegevens in [!INCLUDE[prod_short](includes/prod_short.md)]|[Verzending en ontvangst van elektronische documenten instellen](across-how-to-set-up-electronic-document-sending-and-receiving.md)|  
|Stel een bankrekening, leverancier en betalingsdagboek in voor SEPA-kredietoverboeking.|[SEPA-krediettransfer instellen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#setting-up-sepa-credit-transfer)|  
|Bankrekening-indelingen, betalingsmethoden en klant overeenkomsten voor automatische incasso van SEPA voorbereiden.|[Betalingen incasseren met automatische incasso via SEPA](finance-collect-payments-with-sepa-direct-debit.md)|  
|Gebruikersverificatie en de URL van de extensie AMC Banking 365 Fundamentals instellen, die vereist zijn om bankbestanden converteren naar de indeling van uw bank.|[De AMC Banking 365 Fundamentals-extensie gebruiken](ui-extensions-amc-banking.md)|  
|Stel en schakel een externe service in waarmee u bankafschriften direct kunt importeren als bankfeeds.|[De bankafschriftservice instellen](bank-how-setup-bank-statement-service.md)|  
|Bankrekeningen koppelen in [!INCLUDE[prod_short](includes/prod_short.md)] als de bankafschriftservice is ingeschakeld|[Bankrekeningen instellen](bank-how-setup-bank-accounts.md)|  
|Gegevensexport instellen voor Intrastat-rapportage in [!INCLUDE[prod_short](includes/prod_short.md)].|[Intrastat-rapportage instellen](finance-how-setup-report-intrastat.md)|
|Bereid de configuratie van een nieuwe gegevensuitwisselingsdefinitie voor een gegevensbestand of een gegevensstroom voor door met behulp van het XML-schema van het bestand het sneltabblad **Kolomdefinities** op de pagina **Uitwisselingsdefinitie van boeking** vooraf te vullen.|[XML-schema's gebruiken om gegevensuitwisselingsdefinities voor te bereiden](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)|  
|Stel het kader voor gegevensuitwisseling in zodat gebruikers een nieuwe inkoopdocumentindeling kunnen ontvangen, een nieuwe verkoopdocumentindeling kunnen verzenden, een nieuw bankbestand kunnen importeren of een andere gegevensuitwisseling kunnen uitvoeren.|[Definities voor gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md)|  

## <a name="see-also"></a>Zie ook

[Gegevens elektronisch uitwisselen](across-data-exchange.md)  
[Inkomende documenten](across-income-documents.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
