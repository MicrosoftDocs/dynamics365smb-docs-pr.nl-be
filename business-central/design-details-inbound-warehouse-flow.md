---
title: 'Ontwerpdetails: Inkomende magazijnstroom | Microsoft Docs'
description: De inkomende stroom in een magazijn begint wanneer artikelen in het magazijn van de bedrijfsvestiging arriveren, ofwel ontvangen via externe bronnen of van een andere bedrijfsvestiging. Een werknemer registreert de artikelen, meestal door een barcode te scannen. Vanuit het ontvangstdok worden magazijnactiviteiten uitgevoerd op verschillende complexiteitsniveaus om de artikelen in het opslaggebied te brengen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/08/2021
ms.author: edupont
ms.openlocfilehash: c2a78d585f949922e9f05e42a6ab61dcd7adc521
ms.sourcegitcommit: 0953171d39e1232a7c126142d68cac858234a20e
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/09/2021
ms.locfileid: "6215190"
---
# <a name="design-details-inbound-warehouse-flow"></a>Ontwerpdetails: Inkomende magazijnstroom
De inkomende stroom in een magazijn begint wanneer artikelen in het magazijn van de bedrijfsvestiging arriveren, ofwel ontvangen via externe bronnen of van een andere bedrijfsvestiging. Een werknemer registreert de artikelen, meestal door een barcode te scannen. Vanuit het ontvangstdok worden magazijnactiviteiten uitgevoerd op verschillende complexiteitsniveaus om de artikelen in het opslaggebied te brengen.  

 Elk artikel wordt geïdentificeerd en aan een corresponderend inkomend brondocument gekoppeld. Er zijn de volgende inkomende brondocumenten:  

- Inkooporder  
- Inkomende transferorder  
- Verkoopretourorder  

Bovendien bestaan de volgende interne brondocumenten die fungeren als inkomende bronnen:  

- Productieorder met outputboeking  
- Assemblageorder met outputboeking  

De laatste twee vertegenwoordigen inkomende stromen naar het magazijn vanuit interne bewerkingsgebieden. Voor meer informatie over magazijnverwerking voor interne inkomende en uitgaande processen raadpleegt u [Ontwerpdetails: Inkomende magazijnstromen](design-details-internal-warehouse-flows.md)..  

Processen en UI-documenten in inkomende magazijnstromen zijn verschillend voor standaard- en geavanceerde magazijnconfiguraties. Het belangrijkste verschil is dat de activiteiten per order worden uitgevoerd in standaardmagazijnconfiguraties en dat ze worden samengevoegd voor meerdere orders in geavanceerde magazijnconfiguraties. Voor meer informatie over de verschillende niveaus van de magazijncomplexiteit raadpleegt u [Ontwerpdetails: Magazijnoverzicht](design-details-warehouse-setup.md).  

In [!INCLUDE[prod_short](includes/prod_short.md)] kunnen inkomende processen voor ontvangst en opslag op vier manieren worden uitgevoerd met verschillende functionaliteiten, afhankelijk van het complexiteitsniveau van het magazijn.  

|Methode|Inkomend proces|Opslaglocaties|Ontvangsten|Magazijnopslag|Complexiteitsniveau (zie [Ontwerpdetails: Magazijninstelling](design-details-warehouse-setup.md))|  
|------------|---------------------|----------|--------------|----------------|--------------------------------------------------------------------------------------------------------------------|  
|A|Ontvangst en opslag van de orderregel boeken|X|||2|  
|B|Ontvangst en opslag van een voorraadopslagdocument boeken|||X|3|  
|L|Ontvangst en opslag van een magazijnontvangstdocument boeken||X||5-4-6|  
|D|Ontvangst van een magazijnontvangstdocument en opslag van een magazijnopslagdocument boeken||X|X|5-4-6|  

Het selecteren van een aanpak hangt af van de toegestane praktijken van het bedrijf en het niveau van de organisatorische complexiteit. In een per-order magazijnomgeving, waarbij de meeste magazijnmedewerkers direct met orderdocumenten werken, kan een bedrijf besluiten methode A te gebruiken. Een per-order magazijn dat een complexer opslagproces hanteert of waar specifieke magazijnmedewerkers magazijnfuncties uitvoeren, kan besluiten de opslagfuncties te scheiden van het orderdocument. Dat is methode B. Bovendien kunnen bedrijven die de verwerking van meerdere orders moeten plannen, het handig vinden magazijnontvangstdocumenten te gebruiken. Dat zijn methoden C en D.  

Bij methode A, B en C worden de acties ontvangen en opslaan in één stap gecombineerd wanneer de corresponderende documenten als ontvangen worden geboekt. Bij methode D wordt eerst de ontvangst geboekt om de positieve voorraadmutatie te onderkennen en het feit dat artikelen beschikbaar zijn voor verkoop. De magazijnmedewerker registreert vervolgens de opslag om artikelen beschikbaar te maken voor picken.  

## <a name="basic-warehouse-configurations"></a>Standaardmagazijnconfiguraties  
In het volgende diagram worden de inkomende magazijnstromen aangegeven op documentsoort in standaardmagazijnconfiguraties. De nummers in het diagram komen overeen met de stappen in de gedeelten na het diagram.  

![Inkomende stroom in standaardmagazijnconfiguraties](media/design_details_warehouse_management_inbound_basic_flow.png "Inkomende stroom in standaardmagazijnconfiguraties")  

### <a name="1-release-source-document--create-inventory-put-away"></a>1: Brondocument vrijgeven/Voorraadopslag maken  
Wanneer artikelen worden ontvangen in het magazijn, geeft de gebruiker die verantwoordelijk is voor ontvangst, het brondocument vrij (zoals een inkooporder of inkomende transferorder) als teken voor magazijnmedewerkers dat de ontvangen artikelen in voorraad kunnen worden opgeslagen. Of de gebruiker maakt door pushing voorraadopslagdocumenten voor afzonderlijke orderregels, op basis van te verwerken specifieke opslaglocaties en aantallen.  

### <a name="2-create-inbound-request"></a>2: Inkomend verzoek maken  
Wanneer het inkomende brondocument wordt vrijgegeven, wordt automatisch een inkomend magazijnverzoek gemaakt. Deze bevat verwijzingen naar het brondocumenttype en -aantal en is niet zichtbaar voor de gebruiker.  

### <a name="3-create-inventory-put-away"></a>3: Voorraadopslag maken  
Op de pagina **Voorraadopslag** haalt de magazijnmedewerker door middel van pulling de wachtende brondocumentregels op, op basis van inkomende magazijnverzoeken. De voorraadopslagregels kunnen ook al door pushing zijn gemaakt door de gebruiker die verantwoordelijk is voor het brondocument.  

### <a name="4-post-inventory-put-away"></a>4: Voorraadopslag boeken  
Op elke regel voor artikelen die gedeeltelijk of volledig zijn opgeslagen, vult de magazijnmedewerker het veld **Aantal** in en boekt deze vervolgens de voorraadopslag. Brondocumenten met betrekking tot de voorraadopslag worden geboekt als ontvangen.  

Er worden positieve artikelposten gemaakt, er worden magazijnposten gemaakt en het opslagverzoek wordt verwijderd als het volledig is verwerkt. Het veld **Ontvangen aantal** in het inkomende brondocument wordt bijvoorbeeld bijgewerkt. Er wordt een geboekt ontvangstdocument gemaakt voor bijvoorbeeld de inkooporder en de ontvangen artikelen.  

## <a name="advanced-warehouse-configurations"></a>Geavanceerde magazijnconfiguraties  
In het volgende diagram wordt de inkomende magazijnstroom aangegeven op documentsoort in geavanceerde magazijnconfiguraties. De nummers in het diagram komen overeen met de stappen in de gedeelten na het diagram.  

![Inkomende stroom in geavanceerde magazijnconfiguraties](media/design_details_warehouse_management_inbound_advanced_flow.png "Inkomende stroom in geavanceerde magazijnconfiguraties")  

### <a name="1-release-source-document"></a>1: Brondocument vrijgeven  
Wanneer artikelen worden ontvangen in het magazijn, geeft de gebruiker die verantwoordelijk is voor ontvangst, het brondocument vrij (zoals een inkooporder of inkomende transferorder) als teken voor magazijnmedewerkers dat de ontvangen artikelen in voorraad kunnen worden opgeslagen.  

### <a name="2-create-inbound-request"></a>2: Inkomend verzoek maken  
Wanneer het inkomende brondocument wordt vrijgegeven, wordt automatisch een inkomend magazijnverzoek gemaakt. Deze bevat verwijzingen naar het brondocumenttype en -aantal en is niet zichtbaar voor de gebruiker.  

### <a name="3-create-warehouse-receipt"></a>3: Magazijnontvangst maken  
Op de pagina **Magazijnontvangst** haalt de gebruiker die verantwoordelijk is voor het ontvangen van artikelen, de wachtende brondocumentregels op, op basis van het inkomende magazijnverzoek. Verschillende brondocumentregels kunnen worden gecombineerd in één magazijnontvangstdocument.  

De gebruiker vult het veld **Te verwerken aantal** in en selecteert de ontvangstzone en opslaglocatie, indien nodig.  

### <a name="4-post-warehouse-receipt"></a>4: Magazijnontvangst boeken  
De gebruiker boekt de magazijnontvangst. Er worden positieve artikelposten gemaakt. Het veld **Ontvangen aantal** in het inkomende brondocument wordt bijvoorbeeld bijgewerkt.  

### <a name="5-create-warehouse-internal-put-away"></a>5: Interne magazijnopslag maken  
De gebruiker die verantwoordelijk is voor de opslag van interne bewerkingen, maakt een interne magazijnopslag voor artikelen die moeten worden opgeslagen in het magazijn, zoals productie- of assemblyuitvoer. De gebruiker geeft aantal, zone en opslaglocatie op waar de artikelen moeten worden opgeslagen, eventueel met de functie **Opslaglocatie-inhoud ophalen**. De gebruiker geeft de interne magazijnopslag vrij, waardoor een inkomend magazijnverzoek wordt gemaakt zodat de taak kan worden opgehaald in magazijnopslagdocumenten of het opslagvoorstel.  

### <a name="6-create-put-away-request"></a>6: Opslagaanvraag maken  
Wanneer het inkomende brondocument wordt geboekt, wordt automatisch een verzoek om magazijnopslag gemaakt. Deze bevat verwijzingen naar het brondocumenttype en -aantal en is niet zichtbaar voor de gebruiker. Afhankelijk van de instellingen leidt output van een productieorder ook tot een opslagaanvraag om de voltooide artikelen in voorraad op te slaan.  

### <a name="7-generate-put-away-worksheet-lines-optional"></a>7: Opslagvoorstelregels genereren (optioneel)  
De gebruiker die verantwoordelijk is voor het coördineren van opslagactiviteiten, haalt opslagregels op in het **Opslagvoorstel**, op basis van geboekte magazijnontvangsten of interne bewerkingen met output. De gebruiker selecteert de op te slaan regels en bereidt de opslag voor door op te geven uit welke opslaglocaties moeten worden gepickt, naar welke opslaglocaties moet worden geplaatst en hoeveel eenheden moeten worden verwerkt. De opslaglocaties kunnen door de instelling van de magazijnvestiging of bewerkingresource vooraf worden gedefinieerd.  

Wanneer alle opslagactiviteiten zijn gepland en toegewezen aan magazijnmedewerkers, genereert de gebruiker de magazijnopslagdocumenten. Volledig toegewezen opslagregels worden verwijderd uit het **Opslagvoorstel**.  

> [!NOTE]  
>  Als het veld **Opslagvoorstel gebruiken** niet op de vestigingskaart is geselecteerd, worden magazijnopslagdocumenten gemaakt die direct zijn gebaseerd op geboekte magazijnontvangsten. In dat geval wordt stap 7 overgeslagen.  

### <a name="8-create-warehouse-put-away-document"></a>8: Magazijnopslagdocument maken  
De magazijnmedewerker die opslagactiviteiten uitvoert, maakt een magazijnopslagdocument met pull-functionaliteit, op basis van de geboekte magazijnontvangst. Of het magazijnopslagdocument wordt door pushing gemaakt en toegewezen aan een magazijnmedewerker.  

### <a name="9-register-warehouse-put-away"></a>9: Magazijnopslag registreren  
Op elke regel voor artikelen die gedeeltelijk of volledig zijn opgeslagen, vult de magazijnmedewerker het veld **Aantal** op de pagina **Magazijnopslag** in en registreert deze vervolgens de magazijnopslag.  

Magazijnposten worden gemaakt en de magazijnopslagregels worden verwijderd, als deze volledig zijn verwerkt. Het magazijnopslagdocument blijft geopend totdat het totale aantal van het gerelateerde geboekte magazijnontvangst is geregistreerd. Het veld **Opgeslagen aantal** op de magazijnontvangstorderregels wordt bijgewerkt.  

## <a name="see-also"></a>Zie ook  
[Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]