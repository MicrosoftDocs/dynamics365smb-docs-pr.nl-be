---
title: Overzicht van uitgaande magazijnprocessen
description: In dit artikel wordt de werkstroom van het uitgaande magazijn beschreven.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 11/25/2022
ms.custom: bap-template
---
# Uitgaande magazijnprocessen

Uitgaande processen in magazijnen beginnen wanneer u een brondocument vrijgeeft om artikelen uit een magazijnlocatie te halen. Bijvoorbeeld om de artikelen ergens naartoe te verzenden of om ze naar een andere bedrijfsvestiging te verhuizen. U kunt fysieke artikelen en artikelen die niet op voorraad zijn, verzenden. Voor meer informatie over het ontvangen van artikelen die niet op voorraad zijn, gaat u naar [Artikelen boeken die niet op voorraad zijn](#post-non-inventory-items). 

Het proces van het verzenden van uitgaande orders bestaat in principe uit twee activiteiten:

* Artikelen uit de schappen picken.
* Artikelen uit het magazijn verzenden.

De brondocumenten voor de uitgaande magazijnstroom zijn:  

* Verkooporder  
* Uitgaande transferorder  
* Inkoopretourorder  
* Serviceorder  

> [!NOTE]
> Productie- en assemblageorders met materiaalbehoeften vertegenwoordigen ook uitgaande brondocumenten. Productie- en assemblageorders zijn een beetje anders omdat het typisch interne processen zijn waarbij geen verzending betrokken is. In plaats daarvan worden ze gebruikt om geproduceerde artikelen op te slaan of om het materiaal dat nodig is om een artikel te assembleren, naar een assemblageruimte te verplaatsen. Lees meer over deze processen op [Ontwerpdetails: Interne magazijnstromen](design-details-internal-warehouse-flows.md).  

In [!INCLUDE[prod_short](includes/prod_short.md)] gebeurt het ontvangen en opslaan op een van de volgende vier manieren, zoals beschreven in de volgende tabel.

|Methode|Uitgaand proces|Pick vereist|Verzending vereist|Complexiteitsniveau (meer informatie op [Overzicht van magazijnbeheer](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Picken en verzending vanaf de orderregel boeken|||Geen specifieke magazijnactiviteit.|  
|B|Picken en verzending vanuit een voorraadpickdocument boeken|Ingeschakeld||Basis: Order voor order|  
|H|Picken en verzending vanuit een magazijnverzendingdocument boeken||Ingeschakeld|Basis: Geconsolideerde boeking voor ontvangen/verzenden voor meerdere orders.|  
|D|Picken vanuit een magazijnpickdocument boeken en verzending vanuit een magazijnverzendingdocument boeken|Ingeschakeld|Ingeschakeld|Geavanceerd|  

De te selecteren aanpak hangt af van de magazijnpraktijken van uw bedrijf en het niveau van organisatorische complexiteit. De volgende zijn enkele voorbeelden die u kunnen helpen beslissen.

* In een per-order omgeving met duidelijke processen en een eenvoudige opslaglocatiestructuur is methode A, picken en verzenden vanaf de orderregel, geschikt.
* Als artikelen voor een orderregel uit meer dan één opslaglocatie komen, of als magazijnmedewerkers niet met orderdocumenten kunnen werken, is het gebruik van afzonderlijke pickdocumenten geschikt, methode B.
* Als uw pick- en verzendprocessen meerdere orders omvatten en meer controle en overzicht vereisen, kunt u ervoor kiezen om een magazijnverzendingsdocument en een magazijnpickdocument te gebruiken om de pick- en verzendtaken, methoden C en D, te scheiden.  

Bij methode A, B en C worden de acties picken en verzenden in één stap gecombineerd wanneer het corresponderende document als verzonden wordt geboekt. Bij methode D wordt eerst de pick geregistreerd en wordt de verzending vervolgens op een later moment geboekt vanuit een ander document.

> [!NOTE]
> Hoewel magazijn- en voorraadpicks vergelijkbaar klinken, zijn het verschillende documenten en worden ze in verschillende processen gebruikt.
> * De voorraadpick die wordt gebruikt in methode B, samen met het registreren van pickinformatie, boekt ook de verzending van het brondocument.
> * De magazijnpick die wordt gebruikt in methode D, kan niet worden geboekt en registreert alleen de pick. Met deze registratie wordt de verzending niet geboekt, maar maakt u de artikelen beschikbaar voor de magazijnverzending. In de uitgaande stroom vereist de magazijnpick een magazijnverzending.

## Geen specifieke magazijnactiviteit

De volgende artikelen bevatten informatie over het verwerken van ontvangsten voor brondocumenten als u geen specifieke magazijnactiviteiten hebt.

* [Producten verkopen](sales-how-sell-products.md)
* [Transferorders](inventory-how-transfer-between-locations.md)
* [Inkoopretouren of annuleringen verwerken](purchasing-how-process-purchase-returns-cancellations.md)
* [Serviceorders maken](service-how-to-create-service-orders.md)

## Standaardmagazijnconfiguraties

In het volgende diagram worden de uitgaande magazijnprocessen aangegeven voor verschillende soorten documenten in standaardmagazijnconfiguraties. De nummers in het diagram komen overeen met de stappen in de gedeelten na het diagram.  

:::image type="content" source="media/design-details-warehouse-management-outbound-basic-flow.png" alt-text="Toont de stappen in een standaard uitgaande stroom in een magazijn.":::

### 1: Een brondocument vrijgeven

Wanneer u de actie **Vrijgeven** gebruikt voor een brondocument, zoals een verkoop- of transferorder, zijn de artikelen in het document klaar om te worden verwerkt in het magazijn. Bijvoorbeeld gepickt en in de op het document aangegeven opslaglocatie opgeslagen. Of u maakt door pushing voorraadpickdocumenten voor afzonderlijke orderregels, op basis van te verwerken opgegeven opslaglocaties en aantallen.  

### 2: Een voorraadpick maken

Op de pagina **Voorraadpick** haalt de magazijnmedewerker op pull-manier de brondocumentregels op. De voorraadpickregels kunnen ook al door pushing zijn gemaakt door de gebruiker die verantwoordelijk is voor het brondocument.  

### 3: Een voorraadpick boeken

Op elke regel voor artikelen die gedeeltelijk of volledig zijn gepickt of verplaatst, vult u het veld **Aantal** in en boekt u vervolgens de voorraadpick. Brondocumenten met betrekking tot de voorraadpick worden geboekt als verzonden of verbruikt.  

Voor voorraadpicks worden negatieve artikelposten gemaakt, worden magazijnposten gemaakt en wordt het pickverzoek verwijderd als het volledig is verwerkt. Het veld **Verzonden aantal** in het uitgaande brondocument wordt bijvoorbeeld bijgewerkt. Er wordt een geboekt verzendingsdocument gemaakt voor bijvoorbeeld de verkooporder en de verzonden artikelen.  

## Geavanceerde magazijnconfiguraties

In het volgende diagram worden de uitgaande magazijnprocessen aangegeven voor verschillende soorten documenten in geavanceerde magazijnconfiguraties. De nummers in het diagram komen overeen met de stappen in de gedeelten na het diagram.  

:::image type="content" source="media/design_details_warehouse_management_outbound_advanced_flow.png" alt-text="Toont de stappen in een geavanceerde uitgaande magazijnstroom.":::

### 1: Een brondocument vrijgeven

Het vrijgeven van een brondocument in geavanceerde configuraties doet hetzelfde als voor basisconfiguraties. De artikelen komen beschikbaar voor verwerking in het magazijn. Ze kunnen bijvoorbeeld worden opgenomen in een verzending.  

### 2: Een magazijnverzending maken

De regels van de brondocumenten verschijnen op de pagina **Magazijnverzending**. U kunt regels combineren uit verschillende brondocumenten in één magazijnverzending.  

### 3: Maak een magazijnpick

Maak op de pagina **Magazijnverzending** magazijnpickactiviteiten voor magazijnverzendingen op een van de volgende twee manieren:

- Op een push-manier, waarbij u de actie **Pick maken** gebruikt. Selecteer de te picken regels en bereidt de picks voor door bijvoorbeeld op te geven uit welke opslaglocaties moet worden gepickt en in welke moet worden opgeslagen en hoeveel eenheden moeten worden verwerkt. De opslaglocaties kunnen vooraf worden gedefinieerd voor de magazijnlocatie of resource.
- Op een pull-manier, waarbij u de actie **Vrijgeven** gebruikt. Magazijnmedewerkers gebruiken op de pagina **Pickvoorstel** de actie **Magazijndocumenten ophalen** om hun toegewezen picks te krijgen. Wanneer de magazijnpicks volledig zijn geregistreerd, worden de regels in het venster **Pickvoorstel** verwijderd.

### 4: Een magazijnpick registreren

Op de pagina **Magazijnpick** vult een magazijnmedewerker het veld **Aantal** in voor elke regel die deze volledig of gedeeltelijk heeft gepickt en registreert de medewerker vervolgens de pick.

Magazijnposten worden gemaakt en de magazijnpickregels worden verwijderd, als het hele aantal is gepickt. Het magazijnpickdocument blijft geopend totdat het totale aantal van de magazijnverzending is geregistreerd. Het veld **Gepickt aantal** op de magazijnverzendregels wordt dan overeenkomstig bijgewerkt.  

### 5: De magazijnverzending boeken

Wanneer alle artikelen in het magazijnverzendingsdocument zijn geregistreerd als gepickt, boekt de magazijnmedewerker de verzending. Door te boeken worden de artikelposten bijgewerkt om de vermindering van de voorraad weer te geven. Het veld **Verzonden aantal** in het uitgaande brondocument wordt bijvoorbeeld bijgewerkt.  

## Niet-voorraadartikelen boeken

[!INCLUDE [post-non-inventory-items](includes/post-non-inventory-items.md)]

## Zie ook

[Magazijnbeheer](design-details-warehouse-management.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
