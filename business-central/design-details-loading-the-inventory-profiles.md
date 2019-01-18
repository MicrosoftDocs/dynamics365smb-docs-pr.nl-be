---
title: 'Ontwerpdetails: De voorraadprofielen laden | Microsoft Docs'
description: Om de vele bronnen van vraag en voorzieningen te sorteren, ordent het planningssysteem deze op twee tijdpaden die voorraadprofielen worden genoemd.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
redirect_url: design-details-balancing-demand-and-supply
ms.translationtype: HT
ms.sourcegitcommit: caf7cf5afe370af0c4294c794c0ff9bc8ff4c31c
ms.openlocfilehash: 10d41fd87408a4dfe8d1b5de368c1a32a45e489b
ms.contentlocale: nl-be
ms.lasthandoff: 11/22/2018

---
# <a name="design-details-loading-the-inventory-profiles"></a>Ontwerpdetails: Voorraadprofielen laden
Om de vele bronnen van vraag en voorzieningen te sorteren, ordent het planningssysteem deze op twee tijdpaden die voorraadprofielen worden genoemd.  

 De normale soorten vraag en voorziening met vervaldatums op of na de begindatum van de planning worden in elk voorraadprofiel geladen. Na het laden worden de verschillende soorten vraag en voorziening gesorteerd op basis van algemene prioriteiten, zoals vervaldatum, low-levelcodes, vestiging en variant. Daarnaast worden orderprioriteiten toegepast op de verschillende soorten om ervoor te zorgen dat aan de belangrijkste vraag het eerst wordt voldaan. Zie [Ontwerpdetails: Prioriteit geven aan orders](design-details-prioritizing-orders.md) voor meer informatie.  

 Zoals eerder gezegd, kan vraag ook negatief zijn. Dit betekent dat het moet worden verwerkt als voorraad. In tegenstelling tot de normale soorten voorziening wordt negatieve vraag echter gezien als vaste voorziening. Het planningssysteem kan hier rekening mee houden, maar er worden geen wijzigingen voorgesteld.  

 Over het algemeen beschouwt het planningssysteem alle voorzieningenorders na de begindatum van de planning als vatbaar voor wijziging om aan vraag te voldoen. Zodra echter een aantal vanuit een voorzieningenorder is geboekt, kan deze niet meer in het planningssysteem worden gewijzigd. De volgende verschillende orders kunnen niet opnieuw worden gepland:  

-   Vrijgegeven productieorders waarbij het verbruik of de output is geboekt.  

-   Assemblageorders waarbij het verbruik of de output is geboekt.  

-   Transferorders waarop verzending is geboekt.  

-   Inkooporders waarop ontvangst is geboekt.  

 Afgezien van het laden van typen vraag en aanbod, worden bepaalde soorten geladen met het oog op speciale regels en afhankelijkheden die worden beschreven in het volgende.  

## <a name="item-dimensions-are-separated"></a>Artikeldimensies worden gescheiden  
 Het voorzieningenplan moet worden berekend per combinatie van artikeldimensies, zoals variant en vestiging. Er is echter geen reden om elke theoretische combinatie te berekenen. Alleen combinaties met vraag en/of aanbod moeten worden berekend.  

 Het planningssysteem bepaalt dit via het voorraadprofiel. Wanneer een nieuwe combinatie wordt gevonden, wordt een interne besturingsrecord gemaakt die de werkelijke combinatiegegevens bevat. De SKU wordt automatisch ingevoerd als besturingsrecord, of buitenste lus. Daarom worden de juiste planningsparameters op basis van een combinatie van variant en vestiging ingesteld en kan het programma doorgaan naar de binnenlus.  

> [!NOTE]  
>  De gebruiker hoeft geen SKU-record in te voeren tijdens het invoeren van vraag en/of voorziening voor een bepaalde combinatie van variant en vestiging. Wanneer er geen SKU bestaat voor een bepaalde combinatie, maakt het programma een eigen tijdelijke SKU op basis van de artikelkaartgegevens. Als Vestiging verplicht op Ja is ingesteld op de pagina Voorraadinstellingen, moet een SKU worden gemaakt of moet Onderdelen op vestiging worden ingesteld op Ja. Zie [Ontwerpdetails: Vraag op lege vestiging](design-details-demand-at-blank-location.md) voor meer informatie.  

## <a name="seriallot-numbers-are-loaded-by-specification-level"></a>Serie-/lotnummers worden geladen op specificatieniveau  
 Kenmerken in de vorm van serie-/lotnummers worden in de voorraadprofielen geladen met de vraag en het aanbod waaraan ze zijn toegewezen.  

 Vraag- en voorzieningskenmerken worden gerangschikt op orderprioriteit en op het niveau van specificatie. Omdat serie-/lotnummers het specificatieniveau aangeven, wordt bij een specifiekere vraag, zoals een lotnummer dat specifiek is geselecteerd voor een verkoopregel, een overeenkomst gezocht vóór minder specifieke vraag, bijvoorbeeld een verkoop vanuit een willekeurig geselecteerd lotnummer.  

> [!NOTE]  
>  Er zijn geen speciale prioriteitsregels voor vraag en voorzieningen met serie-/lotnummers, behalve het specificatieniveau dat wordt gedefinieerd door de combinatie van serie- en lotnummer en de instelling voor artikeltracering van de betreffende artikelen.  

 Tijdens het sluitend maken beschouwt het planningssysteem voorzieningen met serie-/lotnummers als inflexibel en wordt niet geprobeerd om dergelijke voorzieningenorders te verhogen of opnieuw te plannen (tenzij ze worden gebruikt in een order-naar-order relatie). Zie Order-naar-order koppelingen worden nooit verbroken). Dit beschermt de voorziening van het ontvangen van meerdere, mogelijk strijdige planningsboodschappen wanneer een voorziening variërende kenmerken heeft, zoals een verzameling verschillende serienummers.  

 Een andere reden dat voorziening met serienummers/lotnummers inflexibel is, is dat serienummers/lotnummers over het algemeen zo laat in het proces worden toegewezen dat het verwarrend zou zijn als er wijzigingen werden voorgesteld.  

 Het vereffenen van serie-/lotnummers heeft geen betrekking op de [vaste zone](design-details-dealing-with-orders-before-the-planning-starting-date.md). Als de vraag en het aanbod niet zijn gesynchroniseerd, zal het planningssysteem wijzigingen of nieuwe orders voorstellen, ongeacht de geplande begindatum.  

## <a name="order-to-order-links-are-never-broken"></a>Order-naar-order koppelingen worden nooit verbroken  
 Bij het plannen van een order-naar-order-artikel moet de gekoppelde voorziening alleen worden gebruikt voor de vraag waarvoor het oorspronkelijk is bedoeld. De gekoppelde vraag moet niet door een willekeurige andere voorziening worden verwerkt, zelfs wanneer het in de huidige situatie beschikbaar is wat betreft tijd en aantal. Een assemblageorder die is gekoppeld aan een verkooporder in een op-order-assembleren scenario, kan bijvoorbeeld niet worden gebruikt om aan andere vraag te voldoen.  

 Order-naar-order vraag en aanbod moeten precies afgestemd zijn. Het planningssysteem waarborgt de voorziening onder alle omstandigheden, zonder rekening te houden met parameters voor ordergrootte, velden en aantallen in de voorraad (buiten de aantallen die betrekking hebben op de gekoppelde orders). Om dezelfde reden stelt het systeem voor overschotaanbod te verlagen als de gekoppelde vraag wordt verlaagd.  

 Deze vereffening heeft ook invloed op de timing. Er wordt geen rekening gehouden met de beperkte horizon die wordt opgegeven door het tijdsinterval; de voorziening wordt opnieuw gepland als het tijdschema van de vraag wordt gewijzigd. Er wordt echter rekening gehouden met de dempingstijd en het wordt voorkomen dat order-naar-order voorzieningen worden uitgepland, behalve de interne voorzieningen van een productieorder met meerdere niveaus (projectorder).  

> [!NOTE]  
>  Serie-/lotnummers kunnen ook worden opgegeven op order-op-order vraag. In dat geval wordt het aanbod niet standaard beschouwd als inflexibel, wat normaal wel het geval is met serie-/lotnummers. In dit geval brengt het systeem een verhoging of verlaging aan afhankelijk van wijzigingen in de vraag. Als één vraag bovendien variërende serie-/lotnummers heeft, zoals meerdere lotnummers, wordt per lot één voorraadorder voorgesteld.  

> [!NOTE]  
>  Prognoses moeten niet leiden tot het maken van voorzieningenorders die zijn gebonden door een order-op-order koppeling. Als de prognose wordt gebruikt, moet deze alleen worden gebruikt als generator van afhankelijke vraag in een productieomgeving.  

## <a name="component-need-is-loaded-according-to-production-order-changes"></a>Materiaalbehoefte wordt geladen op basis van wijzigingen in productieorders  
 Bij de verwerking van productieorders moet het planningssysteem de benodigde materialen controleren voordat ze in het vraagprofiel worden geladen. Materiaalregels die voortvloeien uit een gewijzigde productieorder vervangen regels uit de oorspronkelijke order. Hierdoor wordt gezorgd dat het planningssysteem bepaalt dat planningsregels voor materiaalbehoefte nooit worden gedupliceerd.  

##  <a name="BKMK_SafetyStockMayBeConsumed"></a> Veiligheidsvoorraad kan worden verbruikt  
 De veiligheidsvoorraad is hoofdzakelijk een vraagsoort en wordt daarom in het voorraadprofiel geladen op de begindatum van de planning.  

 De veiligheidsvoorraad is een voorraadhoeveelheid die opzij is gezet om onzekerheden in de vraag te compenseren tijdens de aanvullingslevertermijn. Deze voorraad kan echter worden verbruikt als deze moet worden gebruikt om aan vraag te voldoen. In dat geval zorgt het planningssysteem ervoor dat de veiligheidsvoorraad snel wordt aangevuld, door een voorzieningenorder voor te stellen om het verbruikte deel van de veiligheidsvoorraad aan te vullen op de datum waarop het is verbruikt. Deze planningsregel zal een pictogram van een uitzonderingswaarschuwing bevatten, zodat de planner weet dat de veiligheidsvoorraad gedeeltelijk of volledig is verbruikt door een uitzonderingsorder voor het ontbrekende aantal.  

## <a name="forecast-demand-is-reduced-by-sales-orders"></a>Prognosevraag wordt verlaagd door verkooporders  
 De vraagprognose drukt de verwachte toekomstige vraag uit. Wanneer werkelijke vraag wordt ingevoerd, meestal als verkooporders voor geproduceerde artikelen, wordt de prognose verbruikt.  

 De prognose zelf wordt niet verminderd door verkooporders; deze blijft gelijk. De prognoseaantallen die in de planningsberekening worden gebruikt, worden echter verlaagd (met de verkooporderaantallen) voordat het eventuele resterende aantal in het vraagvoorraadprofiel wordt opgenomen. Wanneer het planningssysteem de werkelijke verkoop in een periode onderzoekt, worden zowel openstaande verkooporders als artikelposten uit verzonden verkoop meegenomen, tenzij ze zijn afgeleid van een raamcontract.  

 Een gebruiker is vereist om een geldige prognoseperiode te definiëren. De datum van het prognoseaantal definieert het begin van de periode, en de datum op de volgende prognose bepaalt het einde van de periode.  

 De prognose voor perioden vóór de planningsperiode wordt niet gebruikt, ongeacht of het is verbruikt of niet. Het eerste belangrijke prognosecijfer is de datum van of de dichtstbijzijnde datum vóór de begindatum van de planning.  

 De prognose kan gelden voor onafhankelijke vraag, zoals verkooporders, of afhankelijke vraag, zoals productieorderonderdelen (moduleprognose). Een artikel kan beide soorten prognoses hebben. Tijdens planning vindt het verbruik afzonderlijk plaats, eerst voor onafhankelijke vraag en dan voor afhankelijke vraag.  

## <a name="blanket-order-demand-is-reduced-by-sales-orders"></a>Raamcontractvraag wordt verlaagd door verkooporders  
 Prognoses worden aangevuld door het verkoopraamcontract, als manier om toekomstige vraag van een specifieke klant op te geven. Net als bij de (niet gespecificeerde) prognose moeten werkelijke verkopen de verwachte vraag verbruiken en moet het resterende aantal in het vraagvoorraadprofiel worden opgenomen. Door het verbruik wordt het raamcontract niet werkelijk verlaagd.  

 De planningsberekening houdt rekening met open verkooporders die zijn gekoppeld aan de specifieke raamcontractregel, maar er wordt geen rekening gehouden met een geldige tijdsperiode. Er wordt ook geen rekening gehouden met geboekte orders, aangezien de boekingsprocedure het openstaande raamcontractaantal al heeft verlaagd.  

## <a name="see-also"></a>Zie ook  
 [Ontwerpdetails: Vraag en aanbod afstemmen](design-details-balancing-demand-and-supply.md)   
 [Ontwerpdetails: Centrale begrippen van het planningssysteem](design-details-central-concepts-of-the-planning-system.md)   
 [Ontwerpdetails: Voorzieningsplanning](design-details-supply-planning.md)   
 [Ontwerpdetails: Planningsparameters](design-details-planning-parameters.md)

