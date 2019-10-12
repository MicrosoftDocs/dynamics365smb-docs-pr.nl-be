---
title: 'Ontwerpdetails: Inkomende magazijnstromen | Microsoft Docs'
description: De artikelenstroom tussen opslaglocaties op een bedrijfsvestiging is gericht op het picken van onderdelen en het opslaan van eindartikelen voor assemblage of productieorders en ad hoc verplaatsingen, zoals opslaglocatieaanvullingen, zonder een relatie met brondocumenten.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: bce55cda1ba5fd5dd89ad75b224651df719d76d5
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303472"
---
# <a name="design-details-internal-warehouse-flows"></a>Ontwerpdetails: Inkomende magazijnstromen
De artikelenstroom tussen opslaglocaties op een bedrijfsvestiging is gericht op het picken van onderdelen en het opslaan van eindartikelen voor assemblage of productieorders en ad hoc verplaatsingen, zoals opslaglocatieaanvullingen, zonder een relatie met brondocumenten. De omvang en aard van de betrokken activiteiten verschillen tussen de basis- en geavanceerde magazijnfuncties.  

 Enkele interne stromen overlappen met inkomende of uitgaande stromen. Een gedeelte van deze overlapping wordt weergegeven als stap 4 en 5 in de grafische diagrammen voor respectievelijk geavanceerde inkomende en uitgaande stromen. Zie voor meer informatie [Ontwerpdetails: Inkomende magazijnstroom](design-details-outbound-warehouse-flow.md).  

## <a name="internal-flows-in-basic-warehousing"></a>Interne stromen in elementaire magazijnomgevingen  
 In elementaire magazijnconfiguraties draait de stroom van artikelen tussen opslaglocaties binnen het bedrijf om het picken van onderdelen en het opslaan van eindartikelen voor productie- of assemblageorders en ad-hoc verplaatsingen, zoals aanvullingen van opslaglocaties, zonder relatie met brondocumenten.  

### <a name="flows-to-and-from-production"></a>Stroomt naar en van productie  
 De belangrijkste integratie tussen productieorders en standaardmagazijnactiviteiten wordt vertegenwoordigd door de mogelijkheid productiecomponenten te picken via de pagina's **Voorraadpick** of **Voorraadverplaatsing**.  

> [!NOTE]  
>  Op de pagina **Voorraadpick** wordt het componentverbruik geboekt met de pickboeking. Met de pagina **Voorraadverplaatsing** worden alleen opslaglocatiecorrecties geregistreerd; er worden geen artikelboekingen uitgevoerd.  

 Naast verwerking van onderdelen bestaat de integratie uit het vermogen geproduceerde artikelen op te slaan met de pagina **Voorraadopslag**.  

 De velden **Code verbruikslocatie**, **Code opslaglocatie gereed product** en **Code grijpvoorraadlocatie** op de vestigingskaart of de kaart van afdelingen/bewerkingsplaatsen definiëren de standaardstromen van en naar productiegebieden.  

 Voor meer informatie over hoe componentenverbruik wordt afgeboekt vanuit de opslaglocaties Naar-productie of Grijpvoorraad raadpleegt u het gedeelte "Productiecomponenten afboeken in het magazijn" in dit onderwerp.  

### <a name="flows-to-and-from-assembly"></a>Stroomt naar en van assemblage  
 De belangrijkste integratie tussen assemblageorders en standaardmagazijnactiviteiten wordt vertegenwoordigd door de mogelijkheid assemblagecomponenten te verplaatsen naar het assemblagegebied.  

 Hoewel er geen specifieke magazijnfunctionaliteit bestaat voor de opslag van componenten, kan de opslaglocatiecode op de assemblageorderkop worden ingesteld op een standaardopslaglocatie. Het boeken van de assemblageorder fungeert dan als het boeken van een opslag. De magazijnactiviteit van het verplaatsen van componenten in het magazijn kan worden beheerd op de pagina **Interne verplaatsing**, zonder relatie met de assemblageorder.  

 Er zijn de volgende assemblagestromen.  

|Workflow|Omschrijving|  
|----------|---------------------------------------|  
|Op voorraad assembleren|De onderdelen zijn nodig voor een assemblageorder waar de output wordt opgeslagen in het magazijn.<br /><br /> Deze magazijnstroom wordt beheerd op de pagina **Voorraadverplaatsing**. Een nemen-regel specificeert waar de onderdelen moeten worden genomen. Een plaatsen-regel specificeert waar de onderdelen moeten worden geplaatst.|  
|Op order assembleren|De onderdelen zijn nodig voor een assemblageorder die is gekoppeld aan een verkooporder die wordt verzonden wanneer het verkochte artikel wordt geassembleerd.|  

> [!NOTE]  
>  Als de artikelen op order worden geassembleerd, activeert de voorraadpick van de gekoppelde verkooporder een voorraadverplaatsing voor alle betreffende assemblagecomponenten, niet alleen voor het verkochte artikel zoals wanneer voorraadartikelen worden verzonden.  

 De velden **Opslaglocatie Naar-assemblage**, **Opslagloc.code Vanuit-assembl.** en **Opslagloc. verz. asm.-op-order** op de vestigingskaart definiëren standaardstromen van en naar assemblagegebieden.  

> [!NOTE]  
>  Het veld **Opslagloc. verz. asm.-op-order** werkt als de opslaglocatie vanuit assemblage in op-order-assembleren-scenario's.  

### <a name="ad-hoc-movements"></a>Ad hoc verplaatsingen  
 In standaardmagazijnomgevingen wordt de verplaatsing van artikelen van opslaglocatie naar opslaglocatie, zonder relatie met brondocumenten, uitgevoerd op de pagina **Interne verplaatsing**, dat werkt in combinatie met de pagina **Voorraadverplaatsing**.  

 Een andere manier om artikelen ad hoc te verplaatsen tussen opslaglocaties is door positieve posten te boeken in het veld **Nieuwe opslaglocatie** op de pagina **Art.-herindelingsdagboek**.  

## <a name="internal-flows-in-advanced-warehousing"></a>Interne stromen in geavanceerde magazijnomgevingen  
 In geavanceerde magazijnconfiguraties draait de stroom van artikelen tussen opslaglocaties in het bedrijf om het picken van onderdelen en het opslaan van eindartikelen voor productieorders en het picken van onderdelen voor assemblageorders. Bovendien doen interne stromen zich voor als ad-hoc verplaatsingen, zoals opslaglocatieaanvullingen, zonder relatie met brondocumenten.  

### <a name="flows-to-and-from-production"></a>Stroomt naar en van productie  
 De belangrijkste integratie tussen productieorders en geavanceerde magazijnactiviteiten wordt vertegenwoordigd door de mogelijkheid productiecomponenten te picken, op de pagina **Magazijnpick** en de pagina **Pickvoorstel**, en de mogelijkheid geproduceerde artikelen op te slaan via de pagina **Interne mag.-opslag**.  

 Een ander integratiepunt in productie wordt verschaft door de pagina **Magazijnverplaatsing**, samen met de pagina Verplaatsingsvoorstel, waarmee u onderdelen kunt plaatsen en geproduceerde artikelen kunt kiezen voor vrijgegeven productieorders.  

 De velden **Code verbruikslocatie**, **Code opslaglocatie gereed product** en **Code grijpvoorraadlocatie** op de vestigingskaart of de kaart van afdelingen/bewerkingsplaatsen definiëren de standaardstromen van en naar productiegebieden.  

 Voor meer informatie over hoe componentenverbruik wordt afgeboekt vanuit de opslaglocaties Naar productie of Grijpvoorraad raadpleegt u het gedeelte "Productiecomponenten afboeken in het magazijn" in dit onderwerp.  

### <a name="flows-to-and-from-assembly"></a>Stroomt naar en van assemblage  
 De belangrijkste integratie tussen assemblageorders en geavanceerde magazijnactiviteiten wordt vertegenwoordigd door de mogelijkheid assemblagecomponenten te picken, zowel via de pagina **Magazijnpick** als de pagina **Pickvoorstel**. Deze functionaliteit werkt net als bij het picken van onderdelen voor productieorders.  

 Hoewel er geen specifieke magazijnfunctionaliteit bestaat voor de opslag van componenten, kan de opslaglocatiecode op de assemblageorderkop worden ingesteld op een standaardopslaglocatie. Het boeken van de assemblageorder fungeert dan als het boeken van een opslag. De magazijnactiviteit van het verplaatsen van componenten in het magazijn kan worden beheerd op de pagina **Verplaatsingsvoorstel** of de pagina **Interne mag.-opslag**, zonder relatie met de assemblageorder.  

> [!NOTE]  
>  Als artikelen op order worden geassembleerd, activeert de magazijnverzending van de gekoppelde verkooporder een magazijnpick voor alle betreffende assemblagecomponenten, niet alleen voor het verkochte artikel zoals wanneer voorraadartikelen worden verzonden.  

 De velden **Opslaglocatie Naar-assemblage** en **Opslagloc.code Vanuit-assembl.** op de vestigingskaart definiëren standaardstromen van en naar assemblagegebieden.  

### <a name="ad-hoc-movements"></a>Ad hoc verplaatsingen  
 In geavanceerde magazijnomgevingen wordt de verplaatsing van artikelen van opslaglocatie naar opslaglocatie, zonder relatie met brondocumenten, beheerd op de pagina **Verplaatsingsvoorstel** en geregistreerd op de pagina Magazijnverplaatsing.  

## <a name="flushing-production-components-in-the-warehouse"></a>Productieonderdelen in het magazijn afboeken  
 Indien ingesteld op de artikelkaart worden onderdelen met magazijnpicks geboekt als verbruikt door de consumptieorder wanneer de magazijnpick wordt geregistreerd. Met de afboekingsmethode **Pick + Voorwaarts** en **Pick + Achterwaarts** activeert de pickregistratie de verwante verbruikboeking respectievelijk wanneer de eerste bewerking wordt gestart of wanneer de laatste bewerking wordt beëindigd.  

 Bekijk het volgende scenario op basis van de [!INCLUDE[d365fin](includes/d365fin_md.md)]-demodatabase, de vestiging WIT.  

 Er bestaat een productieorder voor 15 STUKS van artikel LS-100. Enkele artikelen op de onderdelenlijst moeten handmatig in een verbruiksdagboek worden afgeboekt, en andere artikelen in de lijst kunnen automatisch worden gepickt en worden afgeboekt met behulp van de afboekingsmethode **Pick + Achterwaarts**.  

> [!NOTE]  
>  **Pick + Voorwaarts** werkt alleen als de tweede bewerking van de productiebewerkingsplanregel een code van een bewerkingsplankoppeling gebruikt. Het vrijgeven van een geplande productieorder initieert het voorwaarts afboeken van de onderdelenset naar **Pick + Voorwaarts**. Afboeken kan echter pas plaatsvinden als het picken van de onderdelen is geregistreerd, wat weer alleen kan gebeuren wanneer de order wordt vrijgegeven.  

 In de volgende stappen worden de betrokken acties beschreven door verschillende gebruikers en de gerelateerde reactie:  

1.  De winkelsupervisor geeft de productieorder vrij. Artikelen met de afboekingsmethode **Voorwaarts** zonder routeringskoppeling worden afgetrokken van de grijpvoorraadlocatie.  
2.  De winkelsupervisor kiest de knop **Magazijnpick maken** op de productieorder. Er wordt een magazijnpickdocument gemaakt voor artikelen met de afboekingsmethoden **Handmatig**, **Pick + Achterwaarts** en **Pick + Voorwaarts**. Deze artikelen worden in de verbruikslocatie geplaatst.  
3.  De magazijnmanager wijst de picks toe aan een magazijnmedewerker.  
4.  De magazijnmedewerker pickt de artikelen uit de betreffende opslaglocaties en plaatst ze in de verbruikslocatie of in de opslaglocatie die is opgegeven in de magazijnpick. Dit kan de opslaglocatie van een afdeling of bewerkingsplaats zijn.  
5.  De magazijnmedewerker registreert de pick. Het aantal wordt afgetrokken van de opslaglocaties en toegevoegd aan de verbruikopslaglocatie. Het veld **Gepickt aantal** op de onderdelenlijst voor alle gepickte artikelen wordt bijgewerkt.  

    > [!NOTE]  
    >  Alleen het aantal dat wordt gepickt kan worden verbruikt.  

6.  De machineoperator informeert de productieplanner dat de eindproducten gereed zijn.  
7.  De winkelsupervisor gebruikt het verbruiksdagboek of productiedagboek om het verbruik van onderdelen te boeken die de afboekingsmethode **Handmatig**, **Voorwaarts** of **Pick + Voorwaarts** samen met bewerkingsplankoppelingen gebruiken.  
8.  De productieplanner boekt de output van de productieorder en wijzigt de status in **Gereedgemeld**. Het aantal onderdelen dat gebruikmaakt van de afboekingsmethode **Achterwaarts**, wordt afgetrokken van de grijpvoorraadlocatie en het aantal onderdelen dat gebruikmaakt van de afboekingsmethode **Pick + Achterwaarts** wordt afgetrokken van de verbruikslocatie.  

 De volgende illustratie geeft aan wanneer het veld **Opslaglocatie** in de materialenlijst wordt gevuld volgens de instelling van uw vestiging of bewerkingsplaats/afdeling.  

 ![Overzicht van wanneer/hoe het veld Opslaglocatiecode wordt ingevuld](media/binflow.png "Overzicht van wanneer/hoe het veld Opslaglocatiecode wordt ingevuld")  

## <a name="see-also"></a>Zie ook  
 [Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)
