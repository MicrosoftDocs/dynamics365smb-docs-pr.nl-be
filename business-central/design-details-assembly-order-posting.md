---
title: 'Ontwerpdetails: Assemblageorderboeking'
description: Assemblageorderboeking wordt gebaseerd op dezelfde principes als wanneer de soortgelijke activiteiten van verkooporders en productieverbruik/-output worden geboekt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# Ontwerpdetails: Assemblageorderboeking
Assemblageorderboeking wordt gebaseerd op dezelfde principes als wanneer de soortgelijke activiteiten van verkooporders en productieverbruik/-output worden geboekt. De principes worden echter gecombineerd in de zin dat assemblageorders hun eigen boeking-UI hebben, zoals die voor verkooporders, terwijl de feitelijke postboeking op de achtergrond wordt uitgevoerd als directe artikel- en resourcedagboekboekingen, zoals die voor productieverbruik, output en capaciteit.  

Net als bij productieorderboeking worden de verbruikte materialen en de gebruikte resources omgezet en uitgevoerd als de component wanneer de productieorder is voltooid. Zie [Ontwerpdetails: Productieorderboeking](design-details-production-order-posting.md) voor meer informatie. De kostenstroom voor assemblageorders is echter minder complex, met name omdat de assemblagekostenboeking slechts eenmaal plaatsvindt en daarom geen OHW-voorraad genereert.  

De volgende dagboekboekingen treden op tijdens assemblageorderboekingen:  

-   Het artikeldagboek boekt positieve artikelposten, die output van het assemblageartikel vertegenwoordigen, uit de assemblageorderkop.  
-   Het artikeldagboek boekt negatieve artikelposten, die verbruik van assemblagecomponenten vertegenwoordigen, uit de assemblageorderregels.  
-   Het resourcedagboek boekt gebruik van assemblageresources (tijdseenheden) vanaf de assemblageorderregels.  
-   Het capaciteitsdagboek boekt waardeposten die betrekking hebben op het resourceverbruik, vanaf de assemblageorderregels.  

Het volgende diagram bevat de structuur van artikel- en resourceposten die het gevolg zijn van assemblageorderboeking.  

![Artikel-, resource- en capaciteitsboekingen als gevolg van het boeken van assemblageorders.](media/design_details_assembly_posting_1.png "Artikel-, resource- en capaciteitsboekingen als gevolg van het boeken van assemblageorders")  

> [!NOTE]  
>  Bewerkingsplaatsen en afdelingen zijn opgenomen om te illustreren dat capaciteitsposten zowel worden gemaakt vanuit productie als vanuit assemblage.  

In het volgende diagram wordt aangegeven hoe assemblagegegevens in posten stromen tijdens het boeken:  

![Aan assemblage gerelateerde invoerstroom tijdens boeken.](media/design_details_assembly_posting_2.png "Aan assemblage gerelateerde invoerstroom tijdens boeken")  

## Boekingsvolgorde  
De boeking van een assemblageorder vindt plaats in de volgende volgorde:  

1.  De assemblageorderregels zijn geboekt.  
2.  De assemblageorderkop is geboekt.  

De volgende tabel toont de volgorde van de acties.  

|Actie|Description|  
|------------|-----------------|  
|Boeking initialiseren|1. Voer voorlopige controles uit.<br />2. Voeg een boekingsnummer toe en wijzig de assemblageorderkop.<br />3. Geef de assemblageorder vrij.|  
|Post|<ol><li>Maak de geboekte assemblageorderkop.</li><li>Kopieer opmerkingsregels.</li><li>Boek assemblageorderregels (verbruik):<br /><br /> <ol><li>Maak een statuspagina om assemblageverbruik te berekenen.</li><li>Haal het resterende aantal op waarop de artikeldagboekregel wordt gebaseerd.</li><li>Stel de verbruikte en resterende aantallen opnieuw in.</li><li>Voor assemblageorderregels van de soort Artikel:<br /><br /> <ol><li>Vul velden op de artikeldagboekregel in.</li><li>Breng reserveringen over naar de artikeldagboekregel.</li><li>Boek de artikeldagboekregel om de artikelposten te maken.</li><li>Maak magazijndagboekregels en boek ze.</li></ol></li><li>Voor assemblageorderregels van de soort Resource:<br /><br /> <ol><li>Vul velden op de artikeldagboekregel in.</li><li>Boek de artikeldagboekregel. Hierdoor ontstaan capaciteitsposten.</li><li>Maak en boek een resourcedagboekregel.</li></ol></li><li>Breng veldwaarden van de assemblageorderregel over naar een zojuist gemaakte, geboekte assemblageorderregel.</li></ol></li><li>Boek de assemblageorderkop (output):<br /><br /> <ol><li>Vul velden op de artikeldagboekregel in.</li><li>Breng reserveringen over naar de artikeldagboekregel.</li><li>Boek de artikeldagboekregel om de artikelposten te maken.</li><li>Maak magazijndagboekregels en boek ze.</li><li>Stel de assemblageaantallen en de resterende aantallen opnieuw in.</li></ol></li></ol>|  

> [!IMPORTANT]  
>  In tegenstelling tot productieoutput, die wordt geboekt tegen verwachte kosten, wordt assemblyuitvoer tegen de feitelijke prijs geboekt.  

## Kostenherwaardering  
 Zodra een assemblageorder is geboekt, wat inhoudt dat materiaal (onderdelen) en resources in een nieuw artikel worden geassembleerd, moet het mogelijk zijn om de werkelijke kosten van dat assemblageartikel en de werkelijke voorraadkosten van de betrokken onderdelen te bepalen. Hiervoor worden kosten van de geboekte posten van de bron (de onderdelen en resources) naar de geboekte posten van het doel (de component) doorgestuurd. Het doorsturen van kosten wordt uitgevoerd door het berekenen en genereren van nieuwe posten, zogenaamde herwaarderingsposten, die aan de doelposten worden gekoppeld.  

 De door te sturen assemblagekosten worden gedetecteerd met het detectiemechanisme op orderniveau. Zie voor informatie over andere mechanismen voor herwaarderingsdetectie [Ontwerpdetails: Kostenwaardering](design-details-cost-adjustment.md)  

### De correctie detecteren  
De detectiefunctie op orderniveau wordt gebruikt voor conversiescenario's, productie en assemblage. De functie werkt als volgt:  

-   Kostenherwaardering wordt gedetecteerd door de order te markeren telkens wanneer een materiaal/resource wordt geboekt als verbruikt/gebruikt voor de order.  
-   Kosten wordt doorgestuurd door de kosten voor het materiaal/de resource toe te passen op de uitvoerposten die aan dezelfde order zijn gekoppeld.  

De volgende afbeelding toont de structuur van de herwaarderingspost en hoe assemblagekosten worden aangepast.  

![Aan assemblage gerelateerde invoerstroom tijdens kostenwaardering.](media/design_details_assembly_posting_3.png "Aan assemblage gerelateerde invoerstroom tijdens boeken")  

### De aanpassing doorvoeren  
De spreiding van gedetecteerde correcties van materiaal en resourcekosten op de assemblyuitvoerposten wordt uitgevoerd door de batchverwerking **Kostprijs herwaarderen - Artikelposten**. Deze bevat de functie Aanpassing op meerdere niveaus aanbrengen, die bestaat uit de volgende twee elementen:  

-   Assemblageordercorrectie aanbrengen - hiermee worden kosten van materiaal en resourcegebruik doorgestuurd naar de assemblage-uitvoerpost. Regel 5 en 6 in het algoritme hieronder zijn hiervoor verantwoordelijk.  
-   Correcties op één niveau aanbrengen - hiermee worden kosten voor afzonderlijke artikelen doorgestuurd met behulp van de waarderingsmethode ervan. Regels 9 en 10 in het algoritme hieronder zijn hiervoor verantwoordelijk.  

![Samenvatting van het kostenwaarderingsalgoritme voor assemblageboeking.](media/design_details_assembly_posting_4.jpg "Samenvatting van het kostenwaarderingsalgoritme voor assemblageboeking")  

> [!NOTE]  
>  Het element voor het maken van OHW- herwaarderingen op regel 7 en 8 is verantwoordelijk voor het doorsturen van productiemateriaal en capaciteitsverbruik naar de output van onvoltooide productieorders. Dit wordt niet gebruikt bij het aanpassen van assemblageorderkosten aangezien het concept OHW niet van toepassing is op assemblage.  

Voor informatie over hoe kosten van assemblage en productie worden geboekt naar het grootboek raadpleegt u [Ontwerpdetails: voorraadboeking](design-details-inventory-posting.md).  

## Assemblagekosten zijn altijd werkelijk  
 Het concept van onderhanden werk (OHW) geldt niet voor assemblageorderboeking. Assemblagekosten worden alleen geboekt als werkelijke kosten, nooit als verwachte kosten. Zie [Ontwerpdetails: verwachte-kostenboeking](design-details-expected-cost-posting.md) voor meer informatie.  

Dit wordt ingeschakeld door de volgende gegevensstructuur.  

-   In het veld **Soort** op artikeldagboekregels in de tabellen **Capaciteitspost** en **Waardepost** wordt *Resource* gebruikt om posten van assemblageresources te identificeren.  
-   In het veld **Artikelboekingssoort** op artikeldagboekregels in de tabellen **Capaciteitspost** en **Waardepost** worden *Assemblage-uitvoer* en *Assemblageverbruik* gebruikt om respectievelijk de artikelposten van assemblage-uitvoer en de posten van verbruikte assemblagecomponenten te identificeren.  

Daarnaast worden boekingsgroepsvelden in de assemblageorderkop en de assemblageorderregels standaard als volgt ingevuld.  

|Entiteit|Soort|Boekingsgroep|Dagb. Productboekingsgroep|  
|------------|----------|-------------------|------------------------------|  
|Assemblageorderkop|Artikel|Voorraadboekingsgroep|Dagb. Productboekingsgroep|  
|Assemblageorderregel|Artikel|Voorraadboekingsgroep|Dagb. Productboekingsgroep|  
|Assemblageorderregel|Resource||Dagb. Productboekingsgroep|  

Alleen werkelijke kosten worden geboekt naar het grootboek en er worden geen interimrekeningen gevuld vanuit assemblageorderboeking. Zie voor meer informatie [Ontwerpdetails: rekeningen in het grootboek](design-details-accounts-in-the-general-ledger.md).  

## Op order assembleren  
De artikelpost die het resultaat is van het boeken van een op-order-assembleren-verkoop wordt vast toegepast op de bijbehorende artikelpost voor de assemblageuitvoer. Dienovereenkomstig, worden de kosten van een op-order-assembleren-verkoop afgeleid van de assemblageorder waaraan deze verkoop is gekoppeld.  

Artikelposten van de soort Verkoop die het gevolg zijn van het boeken van op-order-assembleren aantallen, worden gemarkeerd met **Ja** in het veld **Op order assembleren**.  

Bij het boeken van verkooporderregels waarbij een gedeelte afkomstig is uit voorraad en een ander gedeelte een op-order-assembleren aantal is, worden afzonderlijke artikelposten gemaakt, één voor het voorraadaantal en één voor het op-order-assembleren aantal.  

### Boekingsdatums

Over het algemeen worden boekingsdatums gekopieerd van een verkooporder naar de gekoppelde assemblageorder. De boekingsdatum in de assemblageorder wordt automatisch bijgewerkt wanneer u de boekingsdatum in de verkooporder direct of indirect wijzigt, bijvoorbeeld als u de boekingsdatum wijzigt in de magazijnverzending, voorraadpick of als onderdeel van een bulkboeking.

U kunt de boekingsdatum in de assemblageorder handmatig wijzigen. Het kan echter niet later zijn dan de boekingsdatum in de gekoppelde verkooporder. Het systeem behoudt deze datum, tenzij u de boekingsdatum in de verkooporder bijwerkt.


## Zie ook  
 [Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md)   
 [Ontwerpdetails: Productieorderboeking](design-details-production-order-posting.md)   
 [Ontwerpdetails: Waarderingsmethoden](design-details-costing-methods.md)  
 [Voorraadkosten beheren](finance-manage-inventory-costs.md)  
 [Financiën](finance.md)  
 [Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
