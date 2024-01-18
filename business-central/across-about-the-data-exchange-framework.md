---
title: Over het raamwerk voor gegevensuitwisseling
description: In dit artikel wordt uitgelegd hoe u het Data Exchange Framework kunt gebruiken om de uitwisseling van gegevens in zakelijke documenten zoals facturen met uw zakelijke partners te beheren.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Data exchange framework, data files, data exchange, electronic document, invoice, Business Central, business document, standard-compliant file, OCR'
ms.search.form: '189,'
ms.date: 12/13/2023
ms.author: bholtorf
---
# Over het kader voor gegevensuitwisseling

U kunt het raamwerk voor gegevensuitwisseling gebruiken voor het beheren van de uitwisseling van bedrijfsdocumenten, bankbestanden, valutawisselkoersen en andere gegevensbestanden met uw zakelijke partners of autoriteiten.

Als beheerder of Microsoft-partner kunt u het raamwerk in nieuwe integratiefuncties gebruiken door in te stellen welke gegevens moeten worden uitgewisseld en hoe. De indeling van bestanden voor het uitwisselen van gegevens in de bankbestanden, elektronische documenten, valutawisselkoersen en andere met ERP-systemen variëren bijvoorbeeld afhankelijk van de aanbieder van het gegevensbestand of de stream en van het land of de regio. [!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt verschillende bankbestandsindelingen en normen voor gegevensservices. Om ondersteuning te bieden voor elektronische documentindelingen, gebruikt u het kader voor gegevensuitwisseling.

 De volgende diagrammen bevatten de architectuur van het kader voor gegevensuitwisseling.  

 ![Raamwerk voor gegevensuitwisseling &#45; importeren.](media/across-data-exchange/dataexchangeframework_import.png)  

 ![Raamwerk voor gegevensuitwisseling &#45; exporteren.](media/across-data-exchange/dataexchangeframework_export.png)  

## Elektronische documenten

Als alternatief voor het e-mailen van bedrijfsdocumenten kunt u ze elektronisch verzenden en ontvangen. Een elektronisch document is een genormeerd bestand waarin een bedrijfsdocument wordt gerepresenteerd, zoals een factuur van een leverancier die u kunt ontvangen en converteren naar een inkoopfactuur in [!INCLUDE[prod_short](includes/prod_short.md)]. Handelspartners wisselen elektronische documenten uit via externe documentuitwisselingsdiensten. De algemene versie van [!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt standaard het verzenden en ontvangen van elektronische facturen en creditnota's in de PEPPOL-indeling, die wordt ondersteund door de grootste aanbieders van documentuitwisselingsservices. Een belangrijke aanbieder van services voor documentuitwisseling, Tradeshift, is vooraf geconfigureerd en gereed om te worden ingesteld voor uw bedrijf. Als u ondersteuning voor andere elektronisch documentindelingen wilt bieden, moet u nieuwe gegevensuitwisselingsdefinities maken met het kader voor gegevensuitwisseling.  

Vanuit PDF- of afbeeldingsbestanden die inkomende documenten vertegenwoordigen kunt u een externe OCR-service (Optical Character Recognition; optische tekenherkenning) elektronische documenten laten maken die u vervolgens naar documentrecords kunt converteren in [!INCLUDE[prod_short](includes/prod_short.md)], zoals u doet voor elektronische PEPPOL-documenten. Bijvoorbeeld, wanneer u facturen in PDF-indeling van uw leverancier ontvangt, kunt u deze naar de OCR-service verzenden vanaf de pagina **Inkomende documenten**. Na enkele seconden krijgt u het bestand weer terug als elektronische factuur die kan worden geconverteerd naar een inkoopfactuur voor de leverancier. Als u het bestand per e-mail naar de OCR-service verzendt, wordt automatisch een nieuwe inkomende documentrecord gemaakt wanneer u het elektronische document terugkrijgt.  

Als u bijvoorbeeld een verkoopfactuur als elektronisch PEPPOL-document wilt verzenden, selecteert u de optie **Elektronisch document** in het dialoogvenster **Boeken en verzenden**. Van hieruit kunt u tevens het standaardprofiel voor documentverzending van de klant instellen. Eerst moet u diverse stamgegevens instellen, zoals bedrijfsgegevens, klanten, artikelen en eenheden. Deze worden gebruikt om de zakelijke partners en artikelen te identificeren wanneer u gegevens in velden in [!INCLUDE[prod_short](includes/prod_short.md)] converteert naar elementen in het uitgaande documentbestand. De gegevensconversie en -verzending van de PEPPOL-verkoopfactuur worden uitgevoerd door speciale codeunits en XMLports die worden aangegeven door de **PEPPOL**-indeling voor elektronische documenten.  

Als u bijvoorbeeld een factuur van een leverancier wilt ontvangen als elektronisch PEPPOL-document, verwerkt u het document op de pagina **Inkomende documenten** om het te converteren naar een inkoopfactuur in [!INCLUDE[prod_short](includes/prod_short.md)]. U kunt de functie Taakwachtrij instellen om dergelijke bestanden regelmatig te verwerken of u kunt het proces handmatig starten. Eerst moet u diverse stamgegevens instellen, zoals bedrijfsgegevens, leveranciers, artikelen en eenheden. Deze worden gebruikt om de zakelijke partners en artikelen te identificeren wanneer u gegevens en elementen in het inkomende documentbestand converteert naar velden in [!INCLUDE[prod_short](includes/prod_short.md)]. De ontvangst en gegevensconversie van PEPPOL-facturen worden uitgevoerd door het kader voor bestandsuitwisseling dat wordt vertegenwoordigd door de gegevensuitwisselingsdefinitie **PEPPOL- factuur**.  

  Als u bijvoorbeeld, een factuur wilt ontvangen als een elektronisch OCR-document, verwerkt u het als u een elektronisch PEPPOL-document ontvangt. De ontvangst en gegevensconversie van elektronische documenten via OCR worden uitgevoerd door het kader voor bestandsuitwisseling dat wordt vertegenwoordigd door de gegevensuitwisselingsdefinitie **OCR – Factuur**.  

## Bankbestanden

De bestandsindelingen voor de uitwisseling van bankgegevens met toepassingen voor bedrijfsbeheer verschillen, afhankelijk van de leverancier en het land of de regio van het bestand. [!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt import en export van Single Euro Payments Area (SEPA) bankbestanden. Bovendien kunt u met de AMC Banking 365 Fundamentals-extensie verbinding maken met een AMC Banking 365 Fundamentals-extensie geleverd door een externe provider, AMC Consult. Zie voor meer informatie [Betalingen doen met de extensie AMC Banking 365 Fundamentals of SEPA-kredietoverdracht](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md). Om ondersteuning te bieden voor elektronische documentindelingen, gebruikt u het kader voor gegevensuitwisseling.  

Om SEPA-kredietoverboekingen te exporteren, kiest u de knop **Betalingen exporteren naar bestand** op de pagina **Betalingsdagboek** en uploadt u vervolgens het bestand voor verwerking van de betalingen in uw bank. Eerst moet u diverse stamgegevens instellen, zoals bankrekening, leveranciers en betalingswijzen. De conversie en export van SEPA-bankgegevens worden uitgevoerd door een speciale codeunit en XMLport die worden gerepresenteerd door de instelling van bankexport/-import **SEPA-krediettransfer**. U kunt ook de AMC Banking 365 Fundamentals-uitbreiding instellen om de export uit te voeren, met de definitie voor gegevensuitwisseling **AMC Banking 365 Fundamentals-extensie** - Kredietoverdracht.  

 Om SEPA-instructies voor een incasso-opdracht te exporteren, kiest u de knop **Bestand van incasso exporteren** op de pagina **Incasso-opdrachten** en verzendt u deze vervolgens naar uw bank om de betreffende klantbetalingen automatisch te incasseren. Eerst moet u bankrekeningen, klanten, incassomachtigingen en betalingswijzen instellen. De gegevensconversie en export van SEPA-bankgegevens worden uitgevoerd door een speciale codeunit en XMLport die wordt gerepresenteerd door de instelling van bankexport/-import **SEPA-incasso**.  

 Om SEPA-bankafschriften te importeren, kiest u de knop Bankafschrift importeren op de pagina **Betalingsreconciliatiedagboek** en **Bankreconciliatie**. Vervolgens vereffent u elke post op het bankafschrift handmatig of automatisch met betalingen of bankposten. Eerst moet u bankrekeningen instellen. De import en gegevensconversie van SEPA-bankgegevens worden uitgevoerd door het kader voor bestandsuitwisseling dat wordt vertegenwoordigd door de gegevensuitwisselingsdefinitie **SEPA CAMT**. U kunt ook de AMC Banking 365 Fundamentals-uitbreiding instellen om de import uit te voeren, met de definitie voor gegevensuitwisseling **AMC Banking 365 Fundamentals-extensie** - Bankafschrift.  

 Daarnaast ondersteunen lokale versies van [!INCLUDE[prod_short](includes/prod_short.md)] verschillende andere bestandsindelingen voor het importeren en exporteren van bankgegevens, salaristransacties en andere gegevens. Zie voor meer informatie de landingspagina [Lokale functionaliteit](about-localization.md) voor uw land/regio in de Help.  

## Valutawisselkoersen

U kunt een externe service instellen om valutawisselkoersen actueel te houden. De service die de bijgewerkte valutawisselkoersen levert, wordt ingeschakeld door een gegevensuitwisselingsdefinitie. De pagina **Kaart update-instellingen wisselkoersen** is een beknopte weergave van de pagina **Definitie van gegevensuitwisseling** voor de desbetreffende definitie van gegevensuitwisseling.  

Voor alle uitwisselingen van gegevens in XML-bestanden kunt u de instellingen van de gegevensuitwisseling voorbereiden door het XML-schemabestand te laden op de pagina **XML-schemaviewer**. In dit venster kunt u de gegevenselementen selecteren die u wilt uitwisselen met [!INCLUDE[prod_short](includes/prod_short.md)] en vervolgens kunt u een gegevensuitwisselingsdefinitie starten of een XMLport genereren.

## Intrastat

[!INCLUDE[prod_short](includes/prod_short.md)] maakt gebruik van het raamwerk voor gegevensuitwisseling voor Intrastat-rapportage, waar u eenvoudig bestanden met tijdstempel in verschillende indelingen kunt maken om te exporteren. [!INCLUDE[prod_short](includes/prod_short.md)] bevat voorbereide indelingen voor zowel gelokaliseerde landen/regio's als voor standaardversies. Maar u kunt het kant-en-klare rapport wijzigen of uw eigen rapport maken.

## Zie ook

[Gegevens elektronisch uitwisselen](across-data-exchange.md)  
[XML-schema's gebruiken om definities voor gegevensuitwisseling voor te bereiden](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)  
[Gegevensuitwisseling instellen](across-set-up-data-exchange.md)  
[Inkomende documenten](across-income-documents.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
