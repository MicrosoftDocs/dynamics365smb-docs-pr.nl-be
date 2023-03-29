---
title: Ontwerpdetails - Gemiddelde kostprijs
description: 'De gemiddelde kostprijs van een artikel wordt berekend met een periodiek gewogen gemiddelde, dat wordt gebaseerd op de periode voor gemiddelde kostprijsberekening die in Business Central is ingesteld.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: 8645
ms.date: 06/08/2021
ms.author: edupont
---
# Ontwerpdetails: Gemiddelde kostprijs
De gemiddelde kostprijs van een artikel wordt berekend met een periodiek gewogen gemiddelde, dat wordt gebaseerd op de periode voor gemiddelde kostprijsberekening die in [!INCLUDE[prod_short](includes/prod_short.md)] is ingesteld.  

 De herwaarderingsdatum wordt automatisch ingesteld.  

## Berekening voor de gemiddelde kosten instellen  
 In de volgende tabel worden de twee velden op de pagina **Voorraadinstelling** beschreven die moet worden ingevuld om berekening van de gemiddelde kosten mogelijk te maken.  

|Veld|Omschrijving|  
|---------------------------------|---------------------------------------|  
|**Periode gemiddelde kostprijsberekening**|Geeft op in welke periode de gemiddelde kostprijs is berekend. De volgende opties zijn mogelijk:<br /><br /> -   **Dag**<br />-   **Week**<br />-   **Maand**<br />-   **Boekingsperiode**<br /><br /> Aan alle voorraadafnamen die tijdens de gemiddelde-kostprijsperiode zijn geboekt, wordt de gemiddelde kostprijs toegewezen die voor die periode is berekend.|  
|**Gem. kostprijsberekeningsoort**|Geeft aan hoe de gemiddelde kostprijs wordt berekend. De volgende opties zijn mogelijk:<br /><br /> -   **Artikel**<br />-   **Artikel, variant en vestiging**<br /> Met deze optie wordt de gemiddelde inkoopprijs berekend voor elk artikel, voor elke vestiging en voor elke variant van het artikel. Dit betekent dat de gemiddelde kostprijs van het artikel afhankelijk is van waar het is opgeslagen en van de variant die u hebt geselecteerd (bijvoorbeeld de kleur).|  

> [!NOTE]  
>  U kunt slechts één periode voor gemiddelde kostprijsberekening en één soort berekening voor de gemiddelde kostprijs gebruiken in een boekjaar.  
>   
>  De pagina **Boekingsperioden** toont welke gemiddelde periode voor kostprijsberekeningen en welk soort berekening voor de gemiddelde kosten actief is gedurende die periode, voor elke boekhoudperiode.  

## Gemiddelde kosten berekenen  
 Wanneer u een transactie boekt voor een artikel dat de waarderingsmethode Gemiddeld gebruikt, wordt een post gemaakt in de tabel **Gem. kostprijsaanpassing invoerhaven**. Deze post bevat het artikelnummer, de variantcode en de vestigingscode van de transactie. De vermelding bevat ook het veld **Waarderingsdatum**, dat de laatste datum opgeeft van de periode voor gemiddelde kostprijsberekening waarin de transactie is geboekt.  

> [!NOTE]  
>  Dit veld moet niet worden verward met het veld **Waarderingsdatum** in de tabel **Waardepost**, waarin de datum wordt getoond wanneer de waarde van kracht wordt en wordt gebruikt om de gemiddelde-kostprijsperiode te bepalen waartoe de waardepost hoort.  

 De gemiddelde kostprijs van een transactie wordt berekend wanneer de kosten van het artikel worden aangepast. Zie [Ontwerpdetails: kostenwaardering](design-details-cost-adjustment.md) voor meer informatie. Een kostenwaardering gebruikt de posten in de tabel **Gem. kostprijsaanpassing invoerhaven** om te bepalen voor welke artikelen of artikelen, vestigingen en varianten gemiddelde kosten moeten worden berekend. Voor elke post waarvan de kosten niet zijn gecorrigeerd, wordt voor kostenherwaardering het volgende gebruikt om de gemiddelde kosten vast te stellen:  

-   De prijs van het artikel aan het begin van de periode voor gemiddelde kostprijsberekening wordt bepaald.  
-   Voegt de som van de inkomende kosten toe die zijn geboekt tijdens de periode voor gemiddelde kostprijsberekening. Deze omvatten aankopen, verkoopretouren, positieve herwaarderingen, en productie- en assemblyuitvoeren.  
-   Trekt de som van de kosten van uitgaande transacties af die vast werden vereffend met ontvangsten in de periode voor gemiddelde kostprijsberekening. Deze bestaan vaak uit inkoopretouren en negatieve resultaten.  
-   Deelt door het totale voorraadaantal voor het einde van de gemiddelde kostprijsberekeningsperiode, exclusief negatieve voorraadmutaties die worden gewaardeerd.  

 De berekende gemiddelde kosten worden vervolgens vereffend met de afname van de voorraad voor het artikel (of artikel, vestiging en variant) met boekingsdatums in de periode voor gemiddelde kostprijsberekening. Als er positieve voorraadmutaties bestaan die vast zijn vereffend met negatieve voorraadmutaties in de periode voor gemiddelde kosten, worden de berekende gemiddelde kosten van de positieve mutatie naar de negatieve doorgestuurd.  

### Voorbeeld: Periode gemiddelde kostprijsberekening = Dag  
 In het volgende voorbeeld wordt het effect getoond van het berekenen van de gemiddelde kosten op basis van een periode voor gemiddelde kosten van één dag. Het veld **Gem. kostprijsberekeningsoort** op de pagina **Voorraadinstelling** is ingesteld op **Artikel**.  

 De volgende tabel toont artikelposten voor het voorbeeldartikel van gemiddelde kostprijsberekening, ART1, voordat de batchverwerking **Kostprijs herwaarderen - Artikelposten** is uitgevoerd.  

| **Boekingsdatum** | **Artikelboekingssoort** | **Aantal** | **Tot. werk. kosten** | **Postnr.** |
|--|--|--|--|--|
| 01-01-20 | Inkoop | 1 | 20.00 | 1 |
| 01-01-20 | Inkoop | 1 | 40.00 | 2 |
| 01-01-20 | Verkoop | -1 | -20,00 | 3 |
| 01-02-20 | Verkoop | -1 | -40,00 | 4 |
| 02-02-20 | Inkoop | 1 | 100.00 | 5 |
| 03-02-20 | Verkoop | -1 | -100,00 | 6 |

> [!NOTE]  
>  Omdat de kostprijscorrectie nog niet is opgetreden, worden de waarden in het veld **Tot. werk. kosten** van de voorraad verlaagd in overeenstemming met de positieve voorraadmutatie waarop ze worden toegepast.  

 De volgende tabel toont de posten in de tabel **Gem. kostprijsaanpassing invoerhaven** die van toepassing zijn op de waardeposten die afkomstig zijn uit de artikelposten in de voorgaande tabel.  

| **Artikelnr.** | **Variant** | **Vestiging** | **Waarderingsdatum** | **Kostprijs geherwaardeerd** |
|--|--|--|--|--|
| ART1 |  | BLAUW | 01-01-20 | Nee |
| ART1 |  | BLAUW | 01-02-20 | Nee |
| ART1 |  | BLAUW | 02-02-20 | Nee |
| ART1 |  | BLAUW | 03-02-20 | Nee |

 De volgende tabel toont dezelfde artikelposten nadat de batchverwerking **Kostprijs herwaarderen - Artikelposten** is uitgevoerd. De gemiddelde kosten per dag worden berekend en toegepast op de voorraadafnames.  

| **Boekingsdatum** | **Artikelboekingssoort** | **Aantal** | **Tot. werk. kosten** | **Postnr.** |
|--|--|--|--|--|--|
| 01-01-20 | Inkoop | 1 | 20.00 | 1 |
| 01-01-20 | Inkoop | 1 | 40.00 | 2 |
| 01-01-20 | Verkoop | -1 | -30,00 | 3 |
| 01-02-20 | Verkoop | -1 | -30,00 | 4 |
| 02-02-20 | Inkoop | 1 | 100.00 | 5 |
| 03-02-20 | Verkoop | -1 | -100,00 | 6 |

### Voorbeeld: Periode gemiddelde kostprijsberekening = Maand  
 In het volgende voorbeeld wordt het effect getoond van het berekenen van de gemiddelde kosten op basis van een periode voor gemiddelde kosten van één maand. Het veld **Gem. kostprijsberekeningsoort** op de pagina **Voorraadinstelling** is ingesteld op **Artikel**.  

 Als de gemiddelde-kostprijsperiode één maand is, wordt één post gemaakt voor elke combinatie van artikelnummer, variant, vestigingscode en waarderingsdatum.  

 De volgende tabel toont artikelposten voor het voorbeeldartikel van gemiddelde kostprijsberekening, ART1, voordat de batchverwerking **Kostprijs herwaarderen - Artikelposten** is uitgevoerd.  

| **Boekingsdatum** | **Artikelboekingssoort** | **Aantal** | **Tot. werk. kosten** | **Postnr.** |
|--|--|--|--|--|
| 01-01-20 | Inkoop | 1 | 20.00 | 1 |
| 01-01-20 | Inkoop | 1 | 40.00 | 2 |
| 01-01-20 | Verkoop | -1 | -20,00 | 3 |
| 01-02-20 | Verkoop | -1 | -40,00 | 4 |
| 02-02-20 | Inkoop | 1 | 100.00 | 5 |
| 03-02-20 | Verkoop | -1 | -100,00 | 6 |

> [!NOTE]  
>  Omdat de kostprijscorrectie nog niet is opgetreden, worden de waarden in het veld **Tot. werk. kosten** van de voorraad verlaagd in overeenstemming met de positieve voorraadmutatie waarop ze worden toegepast.  

 De volgende tabel toont de posten in de tabel **Gem. kostprijsaanpassing invoerhaven** die van toepassing zijn op de waardeposten die afkomstig zijn uit de artikelposten in de voorgaande tabel.  

| **Artikelnr.** | **Variant** | **Vestiging** | **Waarderingsdatum** | **Kostprijs geherwaardeerd** |
|--|--|--|--|--|
| ART1 |  | BLAUW | 31-01-20 | Nee |
| ART1 |  | BLAUW | 28-02-20 | Nee |

> [!NOTE]  
>  De waarderingsdatum wordt ingesteld op de laatste dag in de periode voor gemiddelde kostprijsberekening, in dit geval de laatste dag van de maand.  

 De volgende tabel toont dezelfde artikelposten nadat de batchverwerking **Kostprijs herwaarderen - Artikelposten** is uitgevoerd. De gemiddelde kosten per maand worden berekend en toegepast op de voorraadafnames.  

|**Boekingsdatum**|**Artikelboekingssoort**|**Aantal**|**Tot. werk. kosten**|**Postnr.**|  
|---------------------------------------|---------------------------------------------------|------------------------------------|----------------------------------------------------|------------------------------------|  
|01-01-20|Inkoop|1|20.00|1|  
|01-01-20|Inkoop|1|40.00|2|  
|01-01-20|Verkoop|-1|-30,00|3|  
|01-02-20|Verkoop|-1|-65,00|4|  
|02-02-20|Inkoop|1|100.00|5|  
|03-02-20|Verkoop|-1|-65,00|6|  

 De gemiddelde kosten van volgnummer 3 worden berekend voor de gemiddelde kostprijsperiode Januari en de gemiddelde kosten voor posten 4 en 6 worden berekend in de periode voor de gemiddelde kostprijsberekening Februari.  

 Om de gemiddelde inkoopprijs voor februari te krijgen, wordt de gemiddelde inkoopprijs van het in voorraad ontvangen artikel (100,00) toegevoegd aan de gemiddelde inkoopprijs aan het begin van de periode (30,00). De som van de twee (130,00) wordt vervolgens gedeeld door het totale aantal op voorraad (2). Dit geeft de resulterende gemiddelde kostprijs van het artikel gedurende de periode Februari (65,00). De gemiddelde kosten worden toegewezen aan de afname van de voorraad in de periode (posten 4 en 6).  

## De waarderingsdatum instellen  
 Het veld **Waarderingsdatum** in de tabel **Waardepost** wordt gebruikt om te bepalen in welke periode voor gemiddelde kostprijsberekening een negatieve voorraadmutatiepost hoort. Dit geldt ook voor de OHW-voorraad (onderhanden werk).  

 De volgende tabel toont de criteria die worden gebruikt om de waarderingsdatum in te stellen.  

|Scenario|Boekingsdatum|Gewaardeerd aantal|Herwaardering|Waarderingsdatum|  
|--------------|-------------------------------------|-----------------------------------------|-----------------|-----------------------------------------|  
|1||Positief|Nee|Boekingsdatum van artikelpost|  
|2|Later dan de laatste waarderingsdatum van vereffende waardeposten|Negatief|Nee|Boekingsdatum van artikelpost|  
|3|Eerder dan de laatste waarderingsdatum van vereffende waardeposten|Positief|Nee|Laatste waarderingsdatum van de vereffende waardeposten|  
|4||Negatief|Ja|Boekingsdatum van herwaarderingswaardepost|  

### Opmerking  
 In de volgende tabel met waardeposten worden de verschillende scenario's toegelicht.  

|Scenario|Boekingsdatum|Artikelboekingssoort|Waarderingsdatum|Gewaardeerd aantal|Tot. werk. kosten|Artikelpostnr.|Postnr.|  
|--------------|-------------------------------------|-----------------------------------------------|-----------------------------------------|-----------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|1|01-01-20|Inkoop|01-01-20|2|20.00|1|1|  
|2|15-01-20|(Artikeltoeslag)|01-01-20|2|8.00|1|2|  
|3|01-02-20|Verkoop|01-02-20|-1|-14,00|2|3|  
|4|01-03-20|(Herwaardering)|01-03-20|1|-.4.00|1|4|  
|5|01-02-20|Verkoop|01-03-20|-1|-10,00|3|5|  

> [!NOTE]  
>  In post nummer 5 in de vorige tabel heeft de gebruiker een verkooporder ingevoerd met een boekingsdatum (02-01-20) die ligt vóór de laatste waarderingsdatum van vereffende waardeposten (03-01-20). Als de corresponderende waarde in het veld **Tot. werk. kosten** voor deze datum (02-01-20) voor deze post zou worden gebruikt, zou het 14,00 zijn. Dit geeft een situatie waarbij het aantal op voorraad nul is, maar de voorraadwaarde -4,00 is.  
>   
>  Om te voorkomen dat aantal en waarde niet overeenkomen, wordt ingesteld dat de waarderingsdatum gelijk moet zijn aan de laatste waarderingsdatum van de vereffende waardeposten (01-03-20). De waarde in het veld **Tot. werk. kosten** wordt 10,00 (na herwaardering), wat betekent dat het aantal op voorraad nul is, en de voorraadwaarde is ook nul.  

> [!CAUTION]  
>  Omdat de lijst **Voorraadwaardering** op boekingsdatum is gebaseerd, bevat de lijst aantal/waarde-verschillen in scenario's zoals in het bovenstaande voorbeeld. Zie [Ontwerpdetails: Voorraadwaardering](design-details-inventory-valuation.md) voor meer informatie.  

 Als het aantal in voorraad kleiner is dan nul na het boeken van de negatieve voorraadmutatie, wordt eerst de herwaarderingsdatum ingesteld op de boekingsdatum van de negatieve voorraadmutatie. Deze datum kan later worden gewijzigd op basis van de regels die worden beschreven in de notitie eerder in dit gedeelte, wanneer de voorraadtoename wordt vereffend.  

## Gemiddelde kosten opnieuw berekenen  
 Het waarderen van negatieve voorraadmutaties als een gewogen gemiddelde zou eenvoudig zijn als inkopen altijd worden gefactureerd voordat verkopen worden gefactureerd, boekingen nooit worden geantedateerd en u nooit fouten zou maken. De realiteit wijkt echter enigszins af van dit ideaal.  

 Zoals geïllustreerd in de voorbeelden in dit onderwerp wordt de waarderingsdatum gedefinieerd als de datum van waaraf de waardepost wordt opgenomen in de berekening van de gemiddelde kosten. Dit geeft u de flexibiliteit om het volgende te doen voor artikelen die de waarderingsmethode Gemiddeld gebruiken:  

-   Factureer de verkoop van een artikel voordat de inkoop van het artikel is gefactureerd.  
-   Antidateer een boeking.  
-   Een onjuiste boeking herstellen.  

> [!NOTE]  
>  Een andere reden voor deze flexibiliteit is vaste vereffening. Zie voor meer informatie over vaste vereffening [Ontwerpdetails: Artikelvereffening](design-details-item-application.md).  

 Vanwege deze flexibiliteit moet u mogelijk de gemiddelde kosten opnieuw berekenen nadat de gerelateerde boeking is uitgevoerd. Als u bijvoorbeeld een positieve of negatieve voorraadmutatie boekt met een waarderingsdatum die ligt vóór een of meer negatieve voorraadmutaties. De herberekening van de gemiddelde kosten wordt automatisch uitgevoerd wanneer u de batchverwerking **Kostprijs herwaarderen - Artikelposten** uitvoert, handmatig of automatisch.  

 Het is mogelijk om de voorraadwaarderingbasis binnen een boekhoudperiode te wijzigen door het veld **Periode gemiddelde kostprijsberekening** en het veld **Gem. kostprijsberekeningsoort** te wijzigen. Dit moet echter zorgvuldig en in overleg met een auditor gebeuren.  

### Opmerking  
 In het volgende voorbeeld ziet u hoe de gemiddelde kosten opnieuw worden berekend wanneer een late boeking wordt geïntroduceerd op een datum die voor een of meer negatieve voorraadmutaties ligt. Het voorbeeld is gebaseerd op een periode voor gemiddelde kosten van **Dag**.  

 De volgende tabel toont de waardeposten die voor het artikel bestaan voordat de boeking wordt geïntroduceerd.  

|Waarderingsdatum|Aantal|Tot. werk. kosten|Postnr.|  
|-----------------------------------------|--------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|1|10.00|1|  
|02-01-20|1|20.00|2|  
|15-02-20|-1|-15,00|3|  
|16-02-20|-1|-15,00|4|  

 De gebruiker boekt een positieve voorraadmutatie (volgnummer 5) met een waarderingsdatum (03-01-20) die voor een of meer negatieve voorraadmutaties ligt. Om de voorraad in evenwicht te brengen, moet de gemiddelde kostprijs opnieuw worden berekend en aangepast naar 17,00.  

 De volgende tabel toont de waardeposten die voor het artikel bestaan nadat volgnummer 5 wordt geïntroduceerd.  

|Waarderingsdatum|Aantal|Tot. werk. kosten|Postnr.|  
|-----------------------------------------|--------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|1|10.00|1|  
|02-01-20|1|20.00|2|  
|03-01-20|1|21.00|5|  
|15-02-20|-1|-17,00|3|  
|16-02-20|-1|-17,00|4|  

## Zie ook  
 [Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md)   
 [Ontwerpdetails: Waarderingsmethoden](design-details-costing-methods.md)   
 [Ontwerpdetails: Kostenwaardering](design-details-cost-adjustment.md)   
 [Ontwerpdetails: Artikelvereffening](design-details-item-application.md)  
 [Voorraadkosten beheren](finance-manage-inventory-costs.md)  
 [Financiën](finance.md)  
 [Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]