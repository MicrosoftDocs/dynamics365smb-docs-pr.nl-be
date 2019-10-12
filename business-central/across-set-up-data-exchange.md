---
title: Gegevensuitwisseling instellen | Microsoft Docs
description: Het kader voor gegevensuitwisseling instellen in Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 851d5359513d1fe744d265b21f13a3abd9c6867b
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304816"
---
# <a name="setting-up-data-exchange"></a>Gegevensuitwisseling instellen
Voordat u documenten elektronisch kunt verzenden en ontvangen of bankbestanden kunt importeren en exporteren, moet u het kader voor gegevensuitwisseling instellen om de betreffende bestanden te verwerken. Daarnaast moet u gerelateerde gebieden instellen, zoals stamgegevens voor klanten aan wie u elektronische facturen verzendt, of de conversieservice voor bankgegevens als u de externe serviceprovider gebruikt om uw bankbestanden te converteren. Zie [Gegevens elektronische uitwisselen](across-data-exchange.md) voor meer informatie.  

 Wanneer [!INCLUDE[d365fin](includes/d365fin_md.md)] is ingesteld voor gegevensuitwisseling met externe bestanden, kunnen gebruikers de instellingen gebruiken in algemene bedrijfstaken, zoals het verzenden en ontvangen van elektronische documenten en het importeren en exporteren van bankbestanden.  

 In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.  

|**Als u dit wilt doen**|**Onderwerp**|  
|------------|-------------|  
|Stel de vooraf geconfigureerde service voor documentuitwisseling in voor het verzenden en ontvangen van elektronische documenten van en naar [!INCLUDE[d365fin](includes/d365fin_md.md)].|[Een service voor documentuitwisseling instellen](across-how-to-set-up-a-document-exchange-service.md)|  
|De vooraf geconfigureerde OCR-service instellen om PDF- of afbeeldingsbestanden in elektronische documenten om te zetten die kunnen worden geconverteerd naar documentrecords in [!INCLUDE[d365fin](includes/d365fin_md.md)]|[Inkomende documenten instellen](across-how-setup-income-documents.md)|  
|Stel één van twee vooraf geconfigureerde services voor bijgewerkte wisselkoersen in om de meest recente valutawisselkoersen op de pagina **Valuta's** te bekijken.|[Valutawisselkoersen bijwerken](finance-how-update-currencies.md)|  
|Diverse hoofdgegevens instellen, zoals bedrijfsgegevens, klanten, leveranciers, artikelen en eenheden, die betrekking hebben op het toewijzen van gegevens in [!INCLUDE[d365fin](includes/d365fin_md.md)]|[Verzending en ontvangst van elektronische documenten instellen](across-how-to-set-up-electronic-document-sending-and-receiving.md)|  
|Stel een bankrekening, leverancier en betalingsdagboek in voor SEPA-kredietoverboeking.|[SEPA-krediettransfer instellen](finance-how-to-set-up-sepa-credit-transfer.md)|  
|Bankrekening-indelingen, betalingsmethoden en klant overeenkomsten voor automatische incasso van SEPA voorbereiden.|[Automatische incasso via SEPA instellen](finance-how-to-set-up-sepa-direct-debit.md)|  
|Gebruikersverificatie en de URL van de conversieserviceprovider van de bankgegevens instellen, die is vereist om bankbestanden om te zetten in de indeling van uw bank.|[Conversieservice voor bankgegevens instellen](bank-how-setup-bank-data-conversion-service.md)|  
|Stel en schakel een externe service in waarmee u bankafschriften direct kunt importeren als bankfeeds.|[De bankafschriftservice instellen](bank-how-setup-bank-statement-service.md)|  
|Bankrekeningen koppelen in [!INCLUDE[d365fin](includes/d365fin_md.md)] als de bankafschriftservice is ingeschakeld|[Bankrekeningen instellen](bank-how-setup-bank-accounts.md)|  
|Bereid de configuratie van een nieuwe gegevensuitwisselingsdefinitie voor een gegevensbestand of een gegevensstroom voor door met behulp van het XML-schema van het bestand het sneltabblad **Kolomdefinities** op de pagina **Uitwisselingsdefinitie van boeking** vooraf te vullen.|[XML-schema's gebruiken om gegevensuitwisselingsdefinities voor te bereiden](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)|  
|Stel het kader voor gegevensuitwisseling in zodat gebruikers een nieuwe inkoopdocumentindeling kunnen ontvangen, een nieuwe verkoopdocumentindeling kunnen verzenden, een nieuw bankbestand kunnen importeren of een andere gegevensuitwisseling kunnen uitvoeren.|[Definities voor gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md)|  

## <a name="see-also"></a>Zie ook  
[Gegevens elektronisch uitwisselen](across-data-exchange.md)  
[Gegevens uitwisselen](across-exchange-data.md)   
[Inkomende documenten](across-income-documents.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)  
