---
title: Ontwerpdetails voor Waarderingsmethoden
description: Dit onderwerp beschrijft hoe de waarderingsmethode bepaalt of werkelijke of gebudgetteerde waarden worden gekapitaliseerd en gebruikt in de kostenberekening.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 05/12/2023
ms.author: bholtorf
---
# <a name="design-details-costing-methods"></a>Ontwerpdetails: Waarderingsmethoden

De waarderingsmethode bepaalt of een werkelijke of gebudgetteerde waarde wordt gekapitaliseerd en gebruikt in de kostenberekening. Samen met de boekingsdatum en de volgorde wordt door de waarderingsmethode ook bepaald hoe de kostenstroom wordt vastgelegd.

> [!NOTE]
> U kunt de waarderingsmethode van een artikel niet wijzigen als er artikelposten voor het artikel bestaan. Zie voor meer informatie [Ontwerpdetails: de waarderingsmethode voor artikelen wijzigen](design-details-changing-costing-methods.md).

De volgende methoden worden ondersteund in [!INCLUDE[prod_short](includes/prod_short.md)]:  

| Waarderingsmethode | Omschrijving | Gebruik |
|--|--|--|
| FIFO | De kostprijs van een artikel is de werkelijke waarde van de ontvangst van het artikel dat met de FIFO-regel is geselecteerd.<br /><br /> In voorraadwaardering wordt verondersteld dat de artikelen die als eerste in voorraad worden geplaatst, als eerst worden verkocht. | In ondernemingsomgevingen waar de productkosten stabiel zijn.<br /><br /> (Wanneer de prijzen stijgen, wordt in de balans een grotere waarde weergegeven. Dit betekent dat de belastingschulden toenemen, maar de creditscores en de mogelijkheid om contanten te lenen beter worden.)<br /><br /> Voor artikelen met een beperkte houdbaarheid, omdat de oudste goederen moeten worden verkocht voordat ze hun uiterste houdbaarheidsdatum overschrijden. |
| LIFO | De kostprijs van een artikel is de werkelijke waarde van de ontvangst van het artikel dat met de LIFO-regel is geselecteerd.<br /><br /> In voorraadwaardering wordt verondersteld dat de artikelen die als laatste in voorraad worden geplaatst, als eerst worden verkocht. | Verboden in veel landen/regio's, aangezien het kan worden gebruikt voor het drukken van winst.<br /><br /> (Wanneer de prijzen stijgen, vermindert de waarde op de resultatenrekening. Dit betekent dat de belastingschulden verminderen, maar de mogelijkheid om contanten te lenen verslechtert.) |
| Gemiddelde | De kostprijs van een artikel wordt berekend als de gemiddelde kostprijs op elk tijdstip na de inkoop.<br /><br /> Voor voorraadwaardering wordt aangenomen dat alle voorraden tegelijkertijd zijn verkocht. | In ondernemingsomgevingen waar de productkosten instabiel zijn.<br /><br /> Wanneer voorraden worden gestapeld of samengevoegd en niet kunnen worden onderscheiden, zoals chemische producten. |
| Specifiek | De kostprijs van een artikel bestaat uit de exacte kosten waarmee de betreffende eenheid is ontvangen. | In productie of handel van gemakkelijk identificeerbare artikelen met tamelijk hoge kostprijs.<br /><br /> Voor artikelen die onder wetgeving vallen.<br /><br /> Voor artikelen met serienummers. |
| Standaard | De kostprijs van een artikel is vooraf ingesteld op basis van de geschatte prijs.<br /><br /> Wanneer de werkelijke kosten later gerealiseerd zijn, moet de vaste verrekenprijs aan de werkelijke aangepast worden door verschilwaarden. | Waar kostenbeheersing essentieel is.<br /><br /> In herhaalde productie, om de directe materiaal-, arbeids- en productieoverheadkosten te waarderen.<br /><br /> Waar er discipline en personeel zijn om normen na te volgen. |

De volgende afbeelding toont hoe de kosten door de voorraad stromen voor elke waarderingsmethode.  

![Waarderingsmethoden gevisualiseerd.](media/design_details_inventory_costing_7_costing_methods.png "Waarderingsmethoden gevisualiseerd")  

Waarderingsmethoden verschillen in de manier waarop ze voorraadafnamen waarderen en of ze werkelijke kosten of standaardkosten gebruiken als de waarderingsbasis. In de volgende tabel worden de verschillende kenmerken toegelicht. (De LIFO-methode is uitgesloten, omdat deze erg lijkt op de FIFO-methode.)  
<!--Old  table
|Category|FIFO|Average|Standard|Specific|  
|-|----------|-------------|--------------|--------------|  
|General characteristic|Easy to understand|Based on period options: **Day**/**Week**/**Month**/**Quarter**/**Accounting Period**.<br /><br /> Can be calculated per item or per item/location/variant.|Easy to use, but requires qualified maintenance.|Requires item tracking on both inbound and outbound transaction.<br /><br /> Typically used for serialized items.|  
|Application/Adjustment|Application keeps track of **the remaining quantity**.<br /><br /> Adjustment forwards costs according to quantity application.|Application keeps track of the **remaining quantity**.<br /><br /> Costs are calculated and forwarded per the **valuation date**.|Application keeps track of the **remaining quantity**.<br /><br /> Application is based on FIFO.|All applications are fixed.|  
|Revaluation|Revalues invoiced quantity only.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|Revalues invoiced quantity only.<br /><br /> Can be done per item only.<br /><br /> Can be done backward in time.|Revalues invoiced and un-invoiced quantities.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|Revalues invoiced quantity only.<br /><br /> Can be done per item or per item ledger entry.<br /><br /> Can be done backward in time.|  
|Miscellaneous|If you back-date an inventory decrease, then existing entries are NOT reapplied to provide a correct FIFO cost flow.|If you back-date an inventory increase or decrease, then the average cost is recalculated, and all affected entries are adjusted.<br /><br /> If you change the period or calculation type, then all affected entries must be adjusted.|Use the **Standard Worksheet** page to periodically update and roll up standard costs.<br /><br /> Is NOT supported per SKU.<br /><br /> No historic records exist for standard costs.|You can use specific item tracking without using the Specific costing method. Then the cost will NOT follow the lot number, but the cost assumption of the selected costing method.|  
-->
<!--Table flipped for slightly better readability -->

||Algemeen kenmerk|Vereffening/Herwaardering |Herwaardering|Diversen |
|-|---------|---------|---------|---------|
|**FIFO**     |Gemakkelijk te begrijpen|Vereffening houdt **het resterende aantal** bij.<br /><br /> De correctie stuurt kosten door op basis van aantalvereffening. |Hiermee worden alleen gefactureerde aantallen geherwaardeerd.<br /><br /> Kan per artikel of per artikelpost worden gedaan.<br /><br /> Kan terug in de tijd worden uitgevoerd.|Als u een negatieve voorraadmutatie antidateert, worden de bestaande posten NIET opnieuw toegepast om een juiste FIFO-kostenstroom te bieden.|
|**Gemiddeld**     |Gebaseerd op periodeopties: **Dag**/**Week**/**Maand**/**Kwartaal**/**Boekingsperiode**.<br /><br /> Kan worden berekend per artikel of per artikel/vestiging/variant.|Vereffening houdt het **resterende aantal** bij.<br /><br /> De kosten worden berekend en doorgegeven op de **waarderingsdatum**. |Hiermee worden alleen gefactureerde aantallen geherwaardeerd.<br /><br /> Kan alleen per artikel worden gedaan.<br /><br /> Kan terug in de tijd worden uitgevoerd. |Als u een negatieve of een positieve voorraadmutatie antidateert, worden de gemiddelde kosten opnieuw berekend en worden alle betrokken posten aangepast.<br /><br /> Als u de periode of het type berekening wijzigt, moeten alle betrokken posten worden aangepast.|
|**Standaard**     |Gemakkelijk te gebruiken, maar vereist gekwalificeerd onderhoud|Vereffening houdt het **resterende aantal** bij.<br /><br /> Vereffening wordt gebaseerd op FIFO.|Hiermee worden gefactureerde en niet-gefactureerde aantallen geherwaardeerd.<br /><br /> Kan per artikel of per artikelpost worden gedaan.<br /><br /> Kan terug in de tijd worden uitgevoerd.|Gebruik de pagina **Standaardvoorstel** om de vaste verrekenprijs regelmatig bij te werken en te berekenen.<br /><br /> Wordt NIET ondersteund per SKU.<br /><br /> Er bestaan geen historische records voor standaardkosten.|
|**Specifiek**     |Hiervoor is artikeltracering vereist op zowel inkomende als uitgaande transacties.<br /><br /> Meestal gebruikt voor artikelen met een serienummer.|Alle vereffeningen zijn vast.|Hiermee worden alleen gefactureerde aantallen geherwaardeerd.<br /><br /> Kan per artikel of per artikelpost worden gedaan.<br /><br /> Kan terug in de tijd worden uitgevoerd.|U kunt specifieke artikeltracering gebruiken zonder de waarderingsmethode Specifiek te gebruiken. De kosten volgen NIET het lotnummer, maar de kostenveronderstelling van de geselecteerde waarderingsmethode.|

## <a name="example"></a>Opmerking

In deze sectie worden voorbeelden gegeven van hoe verschillende waarderingsmethoden invloed hebben op de voorraadwaarde.  

De volgende tabel toont de positieve en negatieve voorraadmutaties waarop de voorbeelden zijn gebaseerd.  

|Boekingsdatum|Aantal|Volgnummer|  
|------------------|--------------|---------------|  
|01-01-20|1|1|  
|01-01-20|1|2|  
|01-01-20|1|3|  
|01-02-20|-1|4|  
|01-03-20|-1|5|  
|01-04-20|-1|6|  

> [!NOTE]  
> Het resulterende aantal op voorraad is nul. Daarom moet de voorraadwaarde ook nul zijn, ongeacht de waarderingsmethode.  

### <a name="effect-of-costing-methods-on-valuing-inventory-increases"></a>Het effect van waarderingsmethoden op de waardering van positieve voorraadmutaties

Voor artikelen met waarderingsmethoden die werkelijke kosten als de waarderingsbasis gebruiken (**FIFO**, **LIFO**, **Gemiddelde** of **Specifiek**), worden positieve voorraadmutaties gewaardeerd tegen de aanschafkosten van het artikel.  

- **Standaard**  

    Voor artikelen waarvoor de waarderingsmethode **Standaard** wordt gebruikt, worden positieve voorraadmutaties gewaardeerd tegen de huidige vaste verrekenprijs van het artikel.  

#### <a name="standard"></a>Standaard

Voor artikelen waarvoor de waarderingsmethode **Standaard** wordt gebruikt, worden positieve voorraadmutaties gewaardeerd tegen de huidige vaste verrekenprijs van het artikel.  

### <a name="effect-of-costing-methods-on-valuing-inventory-decreases"></a>Het effect van waarderingsmethoden op de waardering van negatieve voorraadmutaties

- **FIFO**  

    Voor artikelen die de waarderingsmethode **FIFO** gebruiken, worden artikelen die als eerste zijn ingekocht, altijd als eerste verkocht (volgnummers 3, 2, 1 in dit voorbeeld.) Negatieve voorraadmutaties worden gewaardeerd doordat de waarde wordt genomen van de eerste positieve voorraadmutatie.  

     De KPV wordt berekend met de waarde van de eerste voorraadaanwinsten.  

     De volgende tabel toont hoe negatieve voorraadmutaties wordt gewaardeerd voor de waarderingsmethode **FIFO**.  

    |Boekingsdatum|Aantal|Tot. werk. kosten|Volgnummer|  
    |------------------|--------------|----------------------------|---------------|  
    |01-02-20|-1|-10,00|4|  
    |01-03-20|-1|-20,00|5|  
    |01-04-20|-1|-30,00|6|  

- **LIFO**  

    Voor artikelen die de waarderingsmethode **LIFO** gebruiken, worden artikelen die het meest recentelijk zijn ingekocht, altijd als eerste verkocht (volgnummers 3, 2, 1 in dit voorbeeld.) Negatieve voorraadmutaties worden gewaardeerd doordat de waarde wordt genomen van de laatste positieve voorraadmutatie.  

     De KPV wordt berekend met de waarde van de meest recente voorraadaanwinsten.  

     De volgende tabel toont hoe negatieve voorraadmutaties wordt gewaardeerd voor de waarderingsmethode **LIFO**.  

    |Boekingsdatum|Aantal|Tot. werk. kosten|Volgnummer|  
    |------------|--------|--------------------|---------|  
    |01-02-20|-1|-30,00|4|  
    |01-03-20|-1|-20,00|5|  
    |01-04-20|-1|-10,00|6|  

- **Gemiddelde**  

    Voor artikelen waarvoor de waarderingsmethode **Gemiddeld** wordt gebruikt, wordt een negatieve voorraadmutatie gewaardeerd tegen het gewogen gemiddelde van de resterende voorraad op de laatste dag van de gemiddelde prijsperiode waarin de negatieve mutatie is geboekt. Zie [Ontwerpdetails: kostenwaardering](design-details-average-cost.md) voor meer informatie.  

     De volgende tabel toont hoe negatieve voorraadmutaties wordt gewaardeerd voor de waarderingsmethode **Gemiddeld**.  

    | Boekingsdatum | Aantal | Tot. werk. kosten | Volgnummer |
    |--|--|--|--|
    | 01-02-20 | -1 | -20,00 | 4 |
    | 01-03-20 | -1 | -20,00 | 5 |
    | 01-04-20 | -1 | -20,00 | 6 |

- **Standaard**  

    Voor artikelen die de waarderingsmethode **Standaard** gebruiken, worden negatieve voorraadmutaties gewaardeerd zoals bij de waarderingsmethode **FIFO**, behalve dat waardering wordt gebaseerd op standaardkosten , niet op de werkelijke kosten.  

    De volgende tabel toont hoe negatieve voorraadmutaties wordt gewaardeerd voor de waarderingsmethode **Standaard**.  

    |Boekingsdatum|Aantal|Tot. werk. kosten|Volgnummer|  
    |------------------|--------------|----------------------------|---------------|  
    |01-02-20|-1|-15,00|4|  
    |01-03-20|-1|-15,00|5|  
    |01-04-20|-1|-15,00|6|  

- **Specifiek**  

    Met waarderingsmethoden wordt een veronderstelling gemaakt over hoe de kosten van een positieve naar een negatieve voorraadmutatie stromen. Als er echter accuratere informatie beschikbaar is over de kostenstroom, kunt u van dit principe afwijken door een vaste vereffening tussen posten te maken. Een vaste vereffening leidt tot een koppeling tussen een negatieve voorraadmutatie en een specifieke positieve voorraadmutatie en stuurt de kostenstroom dienovereenkomstig.  

    Voor artikelen die de waarderingsmethode **Specifiek** gebruiken, wordt de negatieve voorraadmutatie gewaardeerd op basis van de positieve voorraadmutatie waar deze aan is gekoppeld door de vaste vereffening.  

    De volgende tabel toont hoe negatieve voorraadmutaties wordt gewaardeerd voor de waarderingsmethode **Specifiek**.  

    |Boekingsdatum|Aantal|Tot. werk. kosten|Vereffenen met post|Volgnummer|
    |------------|--------|--------------------|----------------|---------|  
    |01-02-20|-1|-20,00|**2**|4|  
    |01-03-20|-1|-10,00|**1**|5|  
    |01-04-20|-1|-30,00|**3**|6|  

## <a name="see-also"></a>Zie ook

[Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md)  
[Ontwerpdetails: Verschil](design-details-variance.md)  
[Ontwerpdetails: Gemiddelde kosten](design-details-average-cost.md)  
[Ontwerpdetails: Artikelvereffening](design-details-item-application.md)  
[Voorraadkosten beheren](finance-manage-inventory-costs.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Verklarende woordenlijst in Dynamics 365-bedrijfsprocessen](/dynamics365/guidance/business-processes/glossary)  
[Het kostenoverzicht van producten en diensten definiëren](/dynamics365/guidance/business-processes/product-service-define-cost-overview)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
