---
title: 'Ontwerpdetails: Stromen voor productie, assemblage en projecten'
description: 'Meer informatie over de stroom tussen opslaglocaties voor het picken van componenten en het opslaan van eindproducten voor assemblage, productie of projectorders.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 12/16/2022
ms.custom: bap-template
---
# <a name="flows-for-production-assembly-and-jobs"></a>Stromen voor productie, assemblage en projecten

Interne stromen, zoals het picken van componenten en het opslaan van eindproducten voor assemblage, projecten en productieorders, zijn vergelijkbaar met inkomende of uitgaande stromen. Veel van de processen kunnen dus bekend voorkomen. Dit artikel bevat informatie over het werken met interne magazijnstromen met verschillende niveaus van complexiteit.

## <a name="overview-of-different-configuration-options"></a>Overzicht van verschillende configuratieopties

U kunt magazijnfuncties op verschillende manieren configureren. Het is belangrijk dat de opties die u kiest, uw processen verbeteren zonder overhead te veroorzaken. De volgende tabellen beschrijven typische configuraties voor het omgaan met fysieke goederen voor productie-, project- en assemblageorders.

### <a name="inbound-flow-put-away"></a>Inkomende stroom (opslag)

|Complexiteitniveau|Omschrijving|Instellingen|Opslaglocatie|Inkomende stroom van productieorder|Inkomende stroom van assemblageorder|Inkomende stroom van projecten|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Geen specifieke magazijnactiviteit.|Boeken van orders en dagboeken.||Optioneel. Bepaald door de instelling **Opslaglocatiecode is verplicht**.|Productiejournaal -> Uitvoerjournaal</br><br/> **OPMERKING**: u kunt output boeken met behulp van **Productiejournaal**.|Assemblageorder|Opslag is niet van toepassing op projecten|  
|Basis|Order-voor-order.|Opslag vereist, </br><br/> **Opmerking**: hoewel de instelling **Opslag vereist** heet, kunt u nog wel output vanuit de brondocumenten boeken op vestigingen waar u dit selectievakje hebt ingeschakeld. |Optioneel. Bepaald door de instelling **Opslaglocatiecode is verplicht**.|Productieorder - Voorraadopslag|Assemblageorder|Opslag is niet van toepassing op projecten|
|Geavanceerd|Geconsolideerde opslagactiviteiten voor meerdere brondocumenten.|Ontvangst vereist + Opslag vereist|Optioneel. Bepaald door de instelling **Opslaglocatiecode is verplicht**.|Productieorder(s) -> Outputdagboek|Assemblageorder(s) -> interne verplaatsingen | Opslag is niet van toepassing op projecten|
|Geavanceerd|Hetzelfde als hierboven + gerichte pick-/opslagactiviteiten|Gerichte pick en opslag (afhankelijke schakelaars worden automatisch ingeschakeld)|Verplicht|Hetzelfde als hierboven.|Hetzelfde als hierboven.| Opslag is niet van toepassing op projecten|

Bij sommige configuraties kunt u geen speciale magazijndocumenten gebruiken om opslag te registreren. Als uw vestiging echter opslaglocaties gebruikt, kunt u generieke verplaatsingsdocumenten gebruiken om geproduceerde of geassembleerde artikelen naar het magazijn te verplaatsen. Zie voor meer informatie [Artikelen intern verplaatsen in basismagazijnconfiguraties](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md).

### <a name="outbound-flow-pick"></a>Uitgaande stroom (pick)

|Complexiteitniveau|Omschrijving|Instellingen|Opslaglocatie|Uitgaande stroom van productieorder|Uitgaande stroom van assemblageorder|Uitgaande stroom van projecten|  
|---|----------------|----------|---------|------------------|------------------|------------------|
|Geen specifieke magazijnactiviteit.|Boeken van orders en dagboeken.||Optioneel. Bepaald door de instelling **Opslaglocatiecode is verplicht**.|Productiejournaal -> Verbruiksdagboek </br><br/> **OPMERKING**: u kunt verbruik boeken met behulp van een **Productiejournaal**.|Assemblageorder|Project -> Projectdagboek|  
|Basis|Order-voor-order.|Pick vereist. </br><br/> **Opmerking**: hoewel de instelling **Pick vereist** heet, kunt u nog wel output vanuit de brondocumenten boeken op vestigingen waar u dit selectievakje hebt ingeschakeld. <!-- ToDo Test prod output-->|Optioneel. Bepaald door de instelling **Opslaglocatiecode is verplicht**.|Productieorder - Voorraadpick|Assemblageorder -> Voorraadverplaatsing</br><br/>De **voorraadverplaatsing** kan alleen worden gebruikt met opslaglocaties.|Project -> Voorraadpick|
|Geavanceerd|Geconsolideerde pickactiviteiten voor meerdere brondocumenten.|Verzending vereist + Pick vereist|Optioneel. Bepaald door de instelling Opslaglocatiecode is verplicht|Productieorder(s) -> Magazijnpick -> Verbruiksdagboek |Assemblageorders -> Magazijnpick| Project(en) -> Magazijnpick -> Projectdagboek |
|Geavanceerd|Hetzelfde als hierboven + gerichte pick-/opslagactiviteiten|Gerichte pick en opslag (afhankelijke schakelaars worden automatisch ingeschakeld)|Verplicht|Hetzelfde als hierboven.|Hetzelfde als hierboven.| Gericht picken en opslaan wordt niet ondersteund voor projecten|

Net als bij de inkomende stroom kunt u bij sommige configuraties geen speciale magazijndocumenten gebruiken om opslag te registreren. Als uw vestiging opslaglocaties gebruikt, kunt u generieke verplaatsingsdocumenten gebruiken om geproduceerde of geassembleerde artikelen te verplaatsen. Zie voor meer informatie [Artikelen verplaatsen](warehouse-move-items.md).

## <a name="warehouses-without-dedicated-warehouse-activity"></a>Magazijnen zonder speciale magazijnactiviteit

Zelfs als u geen speciale magazijnactiviteiten hebt, wilt u waarschijnlijk toch zaken als verbruik en productie-output bijhouden. De volgende artikelen bevatten informatie over het verwerken van ontvangsten voor brondocumenten.

* [Verbruik en output registreren voor één vrijgegeven productieorderregel](production-how-to-register-consumption-and-output.md)
* [Artikelen samenstellen](assembly-how-to-assemble-items.md)
* [Verbruik of gebruik voor projecten registreren](projects-how-record-job-usage.md)

## <a name="basic-warehouse-configuration"></a>Standaardmagazijnconfiguratie

De inkomende en uitgaande stromen in een basismagazijnconfiguratie omvatten de volgende instellingen op de pagina **Vestiging** voor de vestiging:

* Voor de inkomende stroom (opslag), zet u de instelling **Opslag vereist** aan, maar zet u de instelling **Ontvangst vereist** uit.
* Voor de uitgaande stroom (picken), zet u de instelling **Pick vereist** aan, maar zet u de instelling **Verzenden vereist** uit.

### <a name="flows-to-and-from-production-in-a-basic-warehouse-configuration"></a>Stromen naar en van productie in een standaardmagazijnconfiguratie

Gebruik **Voorraadpick**-documenten om productiecomponenten in de stroom naar productie te picken. Gebruik **Voorraadopslag**-documenten om de producten die u produceert op te slaan.

Voor vestigingen die opslaglocaties gebruiken, zijn voorraadverplaatsingsdocumenten vooral handig voor het afboeken van materiaal. Voor meer informatie over hoe materiaalverbruik wordt afgeboekt vanuit de opslaglocaties Naar productie of Grijpvoorraad gaat u naar [Productiecomponenten afboeken in het magazijn](warehouse-how-to-pick-for-production.md#flushing-production-components-in-a-basic-warehouse-configuration).

   > [!NOTE]
   > Voorraadverplaatsingen zijn belangrijke documenten als u gebruikmaakt van de afboekmethoden **Picken + voorwaarts** of **Picken + achterwaarts**. Zie voor meer informatie [Afboekingsmethoden](production-how-to-flush-components-according-to-operation-output.md#flushing-methods).

* De velden **Naar productieopslaglocatie**, **Van productieopslaglocatie** en **Code grijpvoorraadlocatie** in de vestiging of de bewerkingsplaats/afdeling definiëren de standaardstromen van en naar productiegebieden.
* Beheer de verplaatsing van geproduceerde artikelen op de pagina **Interne verplaatsing** zonder een relatie met een productieorder.

### <a name="flows-to-and-from-assembly-in-a-basic-warehouse-configuration"></a>Stromen naar en van assemblage in een standaardmagazijnconfiguratie

Boek assemblage-output en -verbruik direct vanuit een assemblageorder.

> [!NOTE]
> **Voorraadpick**- en **voorraadopslag**-documenten worden niet ondersteund voor assemblageorders.

Voor vestigingen die opslaglocaties gebruiken:

* Gebruik **Voorraadverplaatsing**-documenten om assemblagemateriaal naar het assemblagegebied te verplaatsen.
* De velden **Opslaglocatie Naar-assemblage** en **Opslagloc.code Vanuit-assembl.** op de vestigingskaart definiëren standaardstromen van en naar assemblagegebieden.
* Beheer de verplaatsing van geassembleerde artikelen op de pagina **Interne verplaatsing** zonder een relatie met een assemblageorder.

[!INCLUDE [prod_short](includes/prod_short.md)] ondersteunt assembleren-op-voorraad en assembleren-op-order assemblagestromen. Zie voor meer informatie [Op order assembleren of Op voorraad assembleren begrijpen](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock) Met betrekking tot magazijnbeheer maakt op voorraad assembleren deel uit van de interne magazijnstroom en maakt op order assembleren deel uit van de uitgaande magazijnstroom. Zie voor meer informatie [Op-order-assembleren-artikelen met voorraadpicks afhandelen](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks).

### <a name="flows-for-project-management-in-a-basic-warehouse-configuration"></a>Stromen voor projectmanagement in een basismagazijnconfiguratie

Gebruik **Voorraadpick**-documenten om projectmateriaal in de stroom naar productiebeheer te picken.

Voor een vestiging die opslaglocaties gebruikt, definieert het veld **Naar - Opslaglocatiecode van project** op de vestiging de standaardstromen naar projectbeheer.

## <a name="advanced-warehouse-configurations"></a>Geavanceerde magazijnconfiguraties

De inkomende en uitgaande stromen in een geavanceerde magazijnconfiguratie omvatten de volgende instellingen op de pagina **Vestiging** voor de vestiging:

* Voor de inkomende stroom (opslag), zet u de instelling **Ontvangst vereist** en de instelling **Opslag vereist** aan.
* Voor de uitgaande stroom (pick), zet u de instelling **Verzenden vereist** en de instelling **Ontvangst vereist** aan.

### <a name="flows-to-and-from-production-in-advanced-warehouse-configurations"></a>Stromen naar en van productie in geavanceerde magazijnconfiguraties

Gebruik de **Magazijnpick**-documenten en de pagina **Pickvoorstel** om materiaal te picken voor productie.

Voor vestigingen die opslaglocaties gebruiken:

* **Magazijnverplaatsing**-documenten en de pagina **Verplaatsingsvoorstel** zijn vooral handig voor het afboeken van materiaal. Zie voor meer informatie [Productieonderdelen in het magazijn afboeken](warehouse-how-to-pick-for-internal-operations-in-advanced-warehousing.md#flushing-production-components-in-an-advanced-warehouse-configuration).
* De velden **Naar productieopslaglocatie**, **Van productieopslaglocatie** en **Code grijpvoorraadlocatie** op de vestiging of de bewerkingsplaats/afdeling definiëren de standaardstromen van en naar productiegebieden. 
* Beheer de verplaatsing van geproduceerde artikelen op de pagina **Verplaatsingsvoorstel** of **Interne mag.-opslag** zonder een relatie met een productieorder.

### <a name="flows-to-and-from-assembly-in-advanced-warehouse-configurations"></a>Stromen naar en van assemblage in geavanceerde magazijnconfiguraties

Gebruik de **Magazijnpick**-documenten en de pagina **Pickvoorstel** om materiaal te picken voor assemblage.

Voor vestigingen die opslaglocaties gebruiken:

* De velden **Opslaglocatie Naar-assemblage** en **Opslagloc.code Vanuit-assembl.** op de vestiging definiëren standaardstromen van en naar assemblagegebieden.
* Beheer de verplaatsing van componenten op de pagina **Verplaatsingsvoorstel** of **Interne mag.-opslag** zonder een relatie met een assemblageorder.

[!INCLUDE [prod_short](includes/prod_short.md)] ondersteunt assembleren-op-voorraad en assembleren-op-order assemblagestromen. Zie voor meer informatie [Op order assembleren of Op voorraad assembleren begrijpen](assembly-assemble-to-order-or-assemble-to-stock.md#understanding-assemble-to-order-and-assemble-to-stock) 

Op voorraad assembleren maakt deel uit van de interne magazijnstroom en op order assembleren maakt deel uit van de uitgaande magazijnstroom. Zie voor meer informatie [Op-order-assembleren-artikelen in magazijnverzendingen afhandelen](warehouse-how-ship-items.md#handling-assemble-to-order-items-in-warehouse-shipments).

### <a name="flows-to-project-management-in-advanced-warehouse-configurations"></a>Stromen naar projectbeheer in geavanceerde magazijnconfiguraties

Gebruik **Magazijnpick**-documenten en de pagina **Pickvoorstel** om materiaal te picken in de stroom naar projectbeheer.

Voor vestigingen die opslaglocaties gebruiken, definieert het veld **Naar - Opslaglocatiecode van project** op de vestiging de standaardstromen naar het projectgebied.

## <a name="see-also"></a>Zie ook

[Overzicht van magazijnbeheer](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
