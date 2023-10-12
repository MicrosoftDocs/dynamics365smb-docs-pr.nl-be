---
title: 'Ontwerpdetails: Inkomende magazijnstroom'
description: 'Ontdek hoe u artikelen in uw magazijn ontvangt, registreert en koppelt aan inkomende brondocumenten.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: warehouse
ms.date: 09/18/2023
ms.author: bholtorf
---
# Ontwerpdetails: Inkomende magazijnstroom

De inkomende stroom in een magazijn begint wanneer artikelen in het magazijn van de bedrijfsvestiging arriveren, ofwel ontvangen via externe bronnen of van een andere bedrijfsvestiging. U kunt fysieke artikelen en artikelen die niet op voorraad zijn, ontvangen. Voor meer informatie over het ontvangen van artikelen die niet op voorraad zijn, gaat u naar [Artikelen boeken die niet op voorraad zijn](#post-non-inventory-items).

Het proces van het ontvangen van inkomende orders bestaat in principe uit twee activiteiten:

* Artikelen ontvangen in het dok, ze identificeren, ze koppelen aan een brondocument en de ontvangen hoeveelheid registreren.
* Artikelen in voorraad opslaan en vastleggen waar u ze opslaat.

De brondocumenten voor de inkomende magazijnstroom zijn:

* Inkooporders  
* Inkomende transferorders  
* Verkoopretourorders  

> [!NOTE]
> Productie- en assemblageoutput vertegenwoordigen ook inkomende brondocumenten. Lees meer over het afhandelen van productie- en assemblage-output voor interne processen op [Ontwerpdetails: Interne magazijnstromen](design-details-internal-warehouse-flows.md).  

In [!INCLUDE[prod_short](includes/prod_short.md)] gebeurt het ontvangen en opslaan op een van de volgende vier manieren, zoals beschreven in de volgende tabel.

|Methode|Inkomend proces|Ontvangst vereist|Opslag vereist|Complexiteitsniveau (meer informatie op [Overzicht van magazijnbeheer](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Ontvangst en opslag van de orderregel boeken|||Geen specifieke magazijnactiviteit.|  
|B|Ontvangst en opslag van een voorraadopslagdocument boeken||Ingeschakeld|Basis: Order voor order|  
|H|Ontvangst en opslag van een magazijnontvangstdocument boeken|Ingeschakeld||Basis: Geconsolideerde boeking voor ontvangen/verzenden voor meerdere orders.|  
|D|Ontvangst van een magazijnontvangstdocument en opslag van een magazijnopslagdocument boeken|Ingeschakeld|Ingeschakeld|Geavanceerd|  

Het selecteren van een aanpak hangt af van de toegestane praktijken van uw bedrijf en het niveau van de organisatorische complexiteit. De volgende zijn enkele voorbeelden die u kunnen helpen beslissen.

* In een order-voor-order magazijnomgeving, waar de meeste magazijnmedewerkers direct met orderdocumenten werken, zou u kunnen besluiten om methode A te gebruiken. 
* Een order-voor-order magazijn met een complexer opslagproces, of waar magazijnpersoneel hun opslagactiviteiten scheidt van het orderdocument, kan methode B worden gebruikt.
* Bedrijven die de afhandeling van meerdere bestellingen moeten plannen, kunnen het handig vinden om magazijnontvangstdocumenten, methoden C en D, te gebruiken.  

Bij methode A, B en C worden ontvangen en opslaan in één stap gecombineerd wanneer documenten als ontvangen worden geboekt. Bij methode D wordt eerst de ontvangst geboekt om de positieve voorraadmutatie vast te leggen en dat artikelen beschikbaar zijn voor verkoop. De magazijnmedewerker registreert vervolgens de opslag om de artikelen beschikbaar te maken voor uitgaande orders. 

> [!NOTE]
> Hoewel magazijnopslag en voorraadopslag vergelijkbaar klinken, zijn het verschillende documenten en worden ze in verschillende processen gebruikt.
> * De voorraadopslag die wordt gebruikt in methode B, samen met het registreren van opslaginformatie, boekt ook de ontvangst van het brondocument.
> * De magazijnopslag die wordt gebruikt in methode D, kan niet worden geboekt en registreert alleen de opslag. De registratie maakt de artikelen beschikbaar voor de verdere verwerking, maar boekt de ontvangst niet. In de inkomende stroom vereist de magazijnopslag een magazijnontvangst.

## Geen specifieke magazijnactiviteit

De volgende artikelen bevatten informatie over het verwerken van ontvangsten voor brondocumenten als u geen specifieke magazijnactiviteiten hebt.

* [Inkopen vastleggen](purchasing-how-record-purchases.md)
* [Transferorders](inventory-how-transfer-between-locations.md)
* [Verkoopretourorders verwerken](sales-how-process-sales-returns-orders.md)

## Standaardmagazijnconfiguraties  

In een basismagazijnconfiguratie is de schakelaar **Opslag vereist** aangezet, maar de schakelaar **Ontvangst vereisen** is uitgeschakeld op de pagina **Vestiging** van de vestiging.

In het volgende diagram worden de inkomende magazijnstromen aangegeven op documentsoort in standaardmagazijnconfiguraties. De nummers in het diagram komen overeen met de stappen in de gedeelten na het diagram.  

:::image type="content" source="media/design_details_warehouse_management_inbound_basic_flow.png" alt-text="De inkomende basisstroom in magazijn.":::

### 1. Een brondocument vrijgeven om een aanvraag te maken van een voorraadopslag  

Wanneer u artikelen ontvangt, geeft u het brondocument vrij, zoals een inkooporder of een inkomende transferorder. Door het document vrij te geven worden de artikelen beschikbaar om te worden opgeslagen. U kunt ook via pushen voorraadopslagdocumenten voor afzonderlijke orderregels maken op basis van opslaglocaties en te verwerken aantallen.  

### 2: Een voorraadopslag maken  

Op de pagina **Voorraadopslag** haalt de magazijnmedewerker door middel van pulling de wachtende brondocumentregels op, op basis van inkomende magazijnverzoeken. Op een push-manier kunt u ook voorraadopslagregels maken wanneer u het brondocument maakt.  

### 3: Een voorraadopslag boeken  

Op elke regel voor artikelen die gedeeltelijk of volledig zijn opgeslagen, vult u het veld **Aantal** in en boekt u vervolgens de voorraadopslag. Brondocumenten met betrekking tot de voorraadopslag worden geboekt als ontvangen.  

* Er worden positieve artikelposten gemaakt.
* Magazijnboekingen worden gemaakt voor vestigingen die een opslaglocatiecode vereisen voor alle artikeltransacties.
* Het opslagverzoek wordt verwijderd als het volledig is afgehandeld. Het veld **Ontvangen aantal** in het inkomende brondocument wordt bijvoorbeeld bijgewerkt.
* Er wordt een geboekt ontvangstdocument gemaakt voor bijvoorbeeld de inkooporder en de ontvangen artikelen.  

## Geavanceerde magazijnconfiguraties  

Als u een geavanceerde magazijnconfiguratie wilt gebruiken, zet u de schakelaar **Ontvangst vereisen** aan op de pagina Vestiging voor de vestiging. De schakelaar **Opslag vereist** is optioneel.

In het volgende diagram wordt de inkomende magazijnstroom aangegeven op documentsoort. De nummers in het diagram komen overeen met de stappen in de gedeelten na het diagram.  

:::image type="content" source="media/design_details_warehouse_management_inbound_advanced_flow.png" alt-text="De geavanceerde inkomende stroom in een magazijn":::

### 1: Het brondocument vrijgeven  

Wanneer u artikelen ontvangt, geeft u het brondocument vrij, zoals de inkooporder of een inkomende transferorder. Door het document vrij te geven worden de artikelen beschikbaar om te worden opgeslagen. De opslag bevat verwijzingen naar het brondocument en het nummer.

### 2: Een magazijnontvangst maken  

De brondocumentregels verschijnen op de pagina **Magazijnontvangst**. U kunt verschillende brondocumentregels combineren in één magazijnontvangstdocument. Vul het veld **Te verwerken aantal** in en selecteert de ontvangstzone en opslaglocatie, indien nodig.  

### 3. Boek de magazijnontvangst  

Boek de magazijnontvangst om positieve artikelposten te maken. Het veld **Ontvangen aantal** in het inkomende brondocument wordt bijgewerkt.  

Als de schakelaar **Opslag vereist** niet is ingeschakeld op de vestigingskaart, stopt het proces hier. Anders maakt het boeken van het inkomende brondocument de artikelen beschikbaar om te worden opgeslagen. De opslag bevat verwijzingen naar het brondocument en het nummer.  

### 4: (optioneel) Opslagvoorstelregels genereren

Haal magazijnopslagregels op in het **Opslagvoorstel** op basis van geboekte magazijnontvangsten of bewerkingen die output produceren. Geef op de regels die u wilt opslaan, de volgende informatie op:

* De opslaglocaties om artikelen uit te halen.
* De opslaglocaties om artikelen in op te slaan.
* Hoeveel eenheden moeten worden verwerkt.

De opslaglocaties kunnen vooraf worden gedefinieerd door de instelling van de magazijnvestiging of de resource die de bewerking heeft uitgevoerd.  

Wanneer alle opslagactiviteiten zijn gepland en toegewezen aan magazijnmedewerkers, genereert u de magazijnopslagdocumenten. Volledig toegewezen opslagregels worden verwijderd uit het **Opslagvoorstel**.  

> [!NOTE]  
> Als het veld **Opslagvoorstel gebruiken** niet op de vestigingskaart is ingeschakeld, worden magazijnopslagdocumenten gemaakt die direct zijn gebaseerd op geboekte magazijnontvangsten. In dat geval is deze stap niet nodig.  

### 5. Een magazijnopslagdocument maken

Maak een magazijnopslagdocument op een pull-manier, op basis van de geboekte magazijnontvangst. Of maak het magazijnopslagdocument en wijs het door pushing toe aan een magazijnmedewerker.  

### 6: Een magazijnopslag registreren

Op elke regel voor artikelen die gedeeltelijk of volledig zijn opgeslagen, vult u het veld **Aantal** op de pagina **Magazijnopslag** in en registreert u vervolgens de magazijnopslag.  

* Magazijnboekingen worden gemaakt voor vestigingen die een opslaglocatiecode vereisen voor alle artikeltransacties.
* De magazijnopslagregels worden verwijderd als ze volledig zijn afgehandeld.
* Het magazijnopslagdocument blijft geopend totdat u het totale aantal van de gerelateerde geboekte magazijnontvangst registreert.
* Het veld **Opgeslagen aantal** op de magazijnontvangstorderregels wordt bijgewerkt.

## Verwante taken

De volgende tabel beschrijft een reeks taken, met koppelingen naar de artikelen waarin deze worden beschreven.

|**Als u dit wilt doen**|**Onderwerp**|  
|------------|-------------|  
|Ontvang artikelen op magazijnlocaties met een magazijnontvangst voor geheel of gedeeltelijk geautomatiseerde magazijnverwerking.|[Artikelen ontvangen](warehouse-how-receive-items.md)|
|Sla artikelen op een order-voor-order basis op en boek de ontvangst in één activiteit in standaardmagazijnconfiguraties.|[Artikelen opslaan met voorraadopslag](warehouse-how-to-put-items-away-with-inventory-put-aways.md)|  
|Sla artikelen die uit meerdere aankopen, verkoopretouren of transferorders zijn ontvangen, op in een geavanceerde magazijnconfiguratie.|[Artikelen opslaan met magazijnopslag](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)|  

## Niet-voorraadartikelen boeken

[!INCLUDE [post-non-inventory-items](includes/post-non-inventory-items.md)]

## Zie ook

[!INCLUDE[footer-include](includes/footer-banner.md)]
