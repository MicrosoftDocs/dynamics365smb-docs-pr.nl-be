---
title: 'Ontwerpdetails: Herwaardering'
description: U kunt de voorraad herwaarderen op basis van de waarderingsbasis die de voorraadwaarde het nauwkeurigst weergeeft.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 07/07/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# <a name="design-details-revaluation"></a>Ontwerpdetails: Herwaardering

U kunt de voorraad herwaarderen op basis van de waarderingsbasis die de voorraadwaarde het nauwkeurigst weergeeft. U kunt een herwaardering ook antedateren, zodat de kostprijs van verkochte goederen (KPV) correct wordt bijgewerkt voor artikelen die u al hebt verkocht. Artikelen die de waarderingsmethode Standaard gebruiken en die niet volledig zijn gefactureerd, kunnen ook worden geherwaardeerd.  

In [!INCLUDE[prod_short](includes/prod_short.md)] wordt de volgende flexibiliteit ondersteund met betrekking tot herwaardering:  

- Het herwaardeerbare aantal kan voor elke datum opnieuw worden berekend, ook terug in de tijd.  
- Voor artikelen waarvoor de standaardwaarderingsmethode wordt gebruikt, worden verwachte kosten opgenomen in de herwaardering.  
- Negatieve voorraadmutaties die worden beïnvloed door herwaardering, worden gedetecteerd.  

## <a name="calculate-the-revaluable-quantity"></a>De herwaardeerbare hoeveelheid berekenen

De hoeveelheid die u kunt herwaarderen, is de resterende voorraad die beschikbaar is op een bepaalde datum. De hoeveelheid is het totaal van volledig gefactureerde artikelposten die u boekt op of vóór de herwaarderingsdatum.  

> [!NOTE]  
>  Artikelen die de waarderingsmethode Standaard gebruiken, worden anders behandeld wanneer het herwaardeerbare aantal wordt berekend per artikel, vestiging en variant. De hoeveelheden en waarden van artikelposten die nog niet volledig zijn gefactureerd, worden opgenomen in het herwaardeerbare aantal.  

Nadat een herwaardering is geboekt, kunt u een positieve of een negatieve voorraadmutatie boeken met een boekingsdatum die vóór de herwaarderingboekingsdatum ligt. Dit aantal wordt echter niet beïnvloed door de herwaardering. Om de voorraad in evenwicht te brengen, wordt alleen rekening gehouden met het oorspronkelijke herwaardeerbare aantal.  

Omdat u op elke datum kunt herwaarderen, moet u conventies hebben voor wanneer u een artikel als onderdeel van de voorraad beschouwt. Wanneer het artikel bijvoorbeeld in voorraad is en wanneer het artikel onderhanden werk (WIP) is.  

### <a name="example"></a>Opmerking

In het volgende voorbeeld ziet u wanneer een OHW-artikel evolueert om deel van de voorraad te worden. Het voorbeeld is gebaseerd op de productie van een ketting met 150 schakels.  

![OHW-voorraad en -herwaardering.](media/design_details_inventory_costing_10_revaluation_wip.png "OHW-voorraad en -herwaardering")  

**1A**: De gebruiker boekt de ingekochte schakels als ontvangen. De volgende tabel toont de resulterende artikelpost.  

|Boekingsdatum|Artikel|Boekingssoort|Aantal|Volgnummer|  
|------------------|----------|----------------|--------------|---------------|  
|01-01-20|KOPPELING|Inkoop|150|1|  

> [!NOTE]  
>  Nu is een artikel dat de waarderingsmethode Standaard gebruikt, beschikbaar voor herwaardering.  

**1W**: De gebruiker boekt de ingekochte schakels als gefactureerd en de schakels worden onderdeel van de voorraad, vanuit een financieel oogpunt. De volgende tabel toont de twee soorten resulterende waardeposten.  

|Boekingsdatum|Boekingssoort|Waarderingsdatum|Tot. werk. kosten|Artikelpostnr.|Volgnummer|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|15-01-20|Directe kosten|01-01-20|150,00|1|1|  

 **2A + 2W**: De gebruiker boekt de ingekochte schakels als verbruikt voor de productie van de ijzeren ketting. Vanuit een financieel oogpunt worden de koppelingen een deel van OHW-voorraad.  De volgende tabel toont de resulterende artikelpost.  

|Boekingsdatum|Artikel|Boekingssoort|Aantal|Volgnummer|  
|------------------|----------|----------------|--------------|---------------|  
|01-02-20|KOPPELING|Verbruik|-150|1|  

De volgende tabel toont de resulterende waardepost.  

|Boekingsdatum|Boekingssoort|Waarderingsdatum|Tot. werk. kosten|Artikelpostnr.|Volgnummer|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|01-02-20|Directe kosten|01-02-20|-150,00|2|2|  

De waarderingsdatum wordt ingesteld op de datum van de verbruikboeking (01-02-20), als reguliere negatieve voorraadmutatie.  

**3A**: De gebruiker boekt de ketting als output en beëindigt de productieorder. De volgende tabel toont de resulterende artikelpost.  

|Boekingsdatum|Artikel|Boekingssoort|Aantal|Postnr.|  
|------------------|----------|----------------|--------------|---------------|  
|15-02-20|KETTING|Output|1|3|  

**3W:** de gebruiker voert de batchverwerking **Kostprijs herwaarderen - Artikelposten** uit, waarmee de keten wordt geboekt als gefactureerd om aan te geven dat alle materiaalverbruik volledig is gefactureerd. Vanuit een financieel oogpunt zijn de koppelingen niet langer deel van OHW-voorraad wanneer de output volledig is gefactureerd en geherwaardeerd. De volgende tabel toont de twee soorten resulterende waardeposten.  

|Boekingsdatum|Boekingssoort|Waarderingsdatum|Tot. werk. kosten|Artikelpostnr.|Volgnummer|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|15-01-20|Directe kosten|01-01-20|150,00|2|2|  
|01-02-20|Directe kosten|01-02-20|-150,00|2|2|  
|15-02-20|Directe kosten|15-02-20|150.00|3|3|  

## <a name="expected-cost-in-revaluation"></a>Verwachte kosten in herwaardering

De hoeveelheid die u kunt herwaarderen, is de som van de hoeveelheid voor volledig gefactureerde artikelposten die u hebt geboekt op of vóór de herwaarderingsdatum. Wanneer sommige artikelen zijn ontvangen of verzonden maar nog niet gefactureerd, kan de voorraadwaarde ervan niet kan worden berekend. Artikelen die de waarderingsmethode Standaard gebruiken, zijn in dit opzicht niet beperkt.  

> [!NOTE]  
>  Een ander soort verwachte kosten dat kan worden geherwaardeerd is OHW-voorraad, binnen bepaalde regels. Zie [OHW-voorraadherwaardering](design-details-revaluation.md#wip-inventory-revaluation) voor meer informatie.  

Wanneer u de herwaardeerbare hoeveelheid berekent voor artikelen die de waarderingsmethode Standaard gebruiken, omvat de berekening artikelposten die nog niet volledig zijn gefactureerd. Deze posten worden bijgewerkt wanneer u de herwaardering boekt. Wanneer u de geherwaardeerde post factureert, makt u de volgende waardeposten:  

- De gebruikelijke gefactureerde waardepost met de boekingssoort **Directe kosten**. Het kostenbedrag van deze post is de directe kosten van de bronregel.  
- Een waardepost met de boekingssoort **Verschil**. Met deze post wordt het verschil tussen de gefactureerde kosten en de geherwaardeerde vaste verrekenprijs vastgelegd.  
- Een waardepost met de boekingssoort **Herwaardering**. Met deze post wordt de tegenboeking van de herwaardering van de verwachte kosten vastgelegd.

### <a name="example-1"></a>Opmerking

Het volgende voorbeeld is gebaseerd op de productie van de ketting in het vorige voorbeeld. Dit voorbeeld illustreert hoe de drie typen posten worden gemaakt, op basis van het volgende scenario:  

1.  U boekt de ingekochte schakels als ontvangen met een kostprijs van LV 2,00.  
2.  U boekt een herwaardering van de schakels met een nieuwe kostprijs van LV 3,00, waarmee de vaste verrekenprijs wordt bijgewerkt naar LV 3,00.  
3.  U boekt de oorspronkelijke inkoop van de kettingschakels als gefactureerd, wat de volgende waardeposten oplevert:  

    1.  Een gefactureerde waardepost met de boekingssoort **Directe kosten**.  
    2.  Een waardepost met de boekingssoort **Herwaardering** om de tegenboeking vast te leggen van de herwaardering van de verwachte kosten.  
    3.  Een waardepost met de boekingssoort Verschil, waarmee het verschil wordt vastgelegd tussen de gefactureerde kosten en de geherwaardeerde standaardkosten.  

De volgende tabel laat de resultaten zien.  

|Stap|Boekingsdatum|Postsoort|Waarderingsdatum|Kostenbedrag (Verw.)|Tot. werk. kosten|Artikelpostnr.|Volgnummer|  
|----------|------------------|----------------|--------------------|------------------------------|----------------------------|---------------------------|---------------|  
|1.|15-01-20|Directe kosten|15-01-20|300,00|  0.00|1|1|  
|2.|20-01-20|Herwaardering|20-01-20|150,00|  0.00|1|2|  
|3.a.|15-01-20|Directe kosten|15-01-20|-300,00|  0.00|1|3|  
|3.b.|15-01-20|Herwaardering|20-01-20|-150,00|  0.00|1|4|  
|3.c.|15-01-20|Verschil|15-01-20|  0.00|450.00|1|5|  

## <a name="determine-whether-revaluation-affects-an-inventory-decrease"></a>Bepalen of een negatieve voorraadmutatie wordt beïnvloed door herwaardering

Gebruik de datum van de boeking of de herwaardering om te bepalen of een negatieve voorraadmutatie wordt beïnvloed door een herwaardering.  

De volgende tabel toont de criteria die worden gebruikt voor een artikel dat de waarderingsmethode Gemiddeld niet gebruikt.  

|Scenario|Postnr.|Tijd|Beïnvloed door herwaardering|  
|--------------|---------------|------------|-----------------------------|  
|A|Eerder dan herwaarderingpostnummer|Eerder dan herwaarderingboekingsdatum|Nee|  
|B|Eerder dan herwaarderingspost nr.|Gelijk aan herwaarderingboekingsdatum|Nee|  
|L|Eerder dan herwaarderingspost nr.|Later dan herwaarderingboekingsdatum|Ja|  
|D|Later dan herwaarderingspost nr.|Eerder dan herwaarderingboekingsdatum|Ja|  
|O|Later dan herwaarderingspost nr.|Gelijk aan herwaarderingboekingsdatum|Ja|  
|V|Later dan herwaarderingspost nr.|Later dan herwaarderingboekingsdatum|Ja|  

### <a name="example-2"></a>Opmerking

Het volgende voorbeeld illustreert de herwaardering van een artikel dat de FIFO-waarderingsmethode gebruikt. Het voorbeeld is gebaseerd op het volgende scenario:  

1.  Op 01-01-20 boekt u een aankoop van 6 eenheden.  
2.  Op 02-01-20 boekt u een verkoop van 1 eenheid.  
3.  Op 03-01-20 boekt u een verkoop van 1 eenheid.  
4.  Op 04-01-20 boekt u een verkoop van 1 eenheid.  
5.  Op 03-01-20 berekent u de voorraadwaarde van het artikel en boekt u een herwaardering van de kostprijs van het artikel van LV 10,00 naar LV 8,00.  
6.  Op 02-01-20 boekt u een verkoop van 1 eenheid.  
7.  Op 03-01-20 boekt u een verkoop van 1 eenheid.  
8.  Op 04-01-20 boekt u een verkoop van 1 eenheid.  
9. U voert de batchverwerking **Kostprijs herwaarderen - Artikelposten** uit.  

De volgende tabel toont de twee soorten resulterende waardeposten.  

|Scenario|Boekingsdatum|Boekingssoort|Waarderingsdatum|Gewaardeerd aantal|Tot. werk. kosten|Artikelpostnr.|Volgnummer|  
|--------------|------------------|----------------|--------------------|---------------------|----------------------------|---------------------------|---------------|  
||01-01-20|Inkoop|01-01-20|6|60.00|1|1|  
||01-03-20|Herwaardering|01-03-20|4|-8,00|1|5|  
|A|01-02-20|Verkoop|01-02-20|-1|-10,00|2|2|  
|B|01-03-20|Verkoop|01-03-20|-1|-10,00|3|3|  
|L|01-04-20|Verkoop|01-04-20|-1|-10,00|4|4|  
||01-04-20|Verkoop|01-04-20|-1|2.00|4|9|  
|D|01-02-20|Verkoop|01-03-20|-1|-10,00|5|6|  
||01-02-20|Verkoop|01-03-20|-1|2.00|5|10|  
|O|01-03-20|Verkoop|01-03-20|-1|-10,00|6|7|  
||01-03-20|Verkoop|01-03-20|-1|2.00|6|11|  
|V|01-04-20|Verkoop|01-04-20|-1|-10,00|7|8|  
||01-04-20|Verkoop|01-04-20|-1|2.00|7|12|  

## <a name="wip-inventory-revaluation"></a>OHW-voorraadherwaardering

Het herwaarderen van OHW-voorraad houdt in dat u componenten herwaardeert die als OHW-voorraad zijn geregistreerd.  

Het is belangrijk om conventies te hebben die bepalen wanneer een artikel vanuit financieel oogpunt OHW-voorraad is. In [!INCLUDE[prod_short](includes/prod_short.md)], bestaan de volgende conventies:  

- Een ingekocht onderdeel wordt een deel van de grondstoffenvoorraad wanneer u een inkoop als gefactureerd boekt.  
- Een ingekocht onderdeel of onderdeel via subassemblage wordt een deel van de OHW-voorraad wanneer u het verbruik ervan in verband met een productieorder boekt.  
- Een ingekocht onderdeel of onderdeel via subassemblage blijft deel van de OHW-voorraad totdat u een productieorder (geproduceerd artikel) factureert.  

De manier waarop de herwaarderingsdatum van de waardepost van verbruik is ingesteld, volgt dezelfde regels als bij niet-OHW-voorraad. Ga voor meer informatie naar [Bepalen of een negatieve voorraadmutatie wordt beïnvloed door herwaardering](#determine-whether-revaluation-affects-an-inventory-decrease).  

U kunt OHW-voorraad herwaarderen onder de volgende voorwaarden:

- De herwaarderingsdatum ligt vóór de boekingsdatums van de overeenkomstige artikelposten van de soort Verbruik.
- U hebt de productieorder niet gefactureerd.  

> [!CAUTION]  
> De lijst **Voorraadwaardering - OHW** toont de waarde van geboekte productieorderposten en kan daarom een beetje verwarrend zijn voor OHW-artikelen die opnieuw zijn gewaardeerd.  

## <a name="revaluate-items-with-the-average-costing-method"></a>Artikelen herwaarderen met de waarderingsmethode Gemiddeld

U kunt alleen items herwaarderen die gebruikmaken van de waarderingsmethode Gemiddeld als **Berekenen per** is ingesteld op *Artikel*.

U kunt alleen herwaardering uitvoeren aan het einde van de periode die is geselecteerd in het veld **Periode gemiddelde kostprijsberekening** op de pagina **Voorraadinstellingen**.

Herwaardering heeft geen invloed op negatieve transacties in de huidige maand. Daarom worden volledig vereffende inkomende posten ook niet opgenomen.

### <a name="example-3"></a>Opmerking

Dit voorbeeld laat zien wat er gebeurt als u de voorraadwaarde berekent op de pagina **Artikelherwaarderingsdagboek** . Op de pagina **Voorraadinstellingen** wordt **Artikel** gekozen in het veld **Gem. kostprijsberekeningsoort** en **Maand** wordt gekozen in het veld **Periode gemiddelde kostprijsberekening** .

De volgende tabel bevat artikelposten voor het voorbeeldartikel met gemiddelde kostprijs, ARTIKEL1.

|Boekingsdatum|Artikelboekingssoort|Hoeveelheid|Kostenbedrag (werkelijk)|Postnr.|
|----|----|----|----|----|
04-25-23|Inkoop|5|5.00|1
04-26-23|Inkoop|3|3.00|2
04-27-23|Verkoop|-5|-5,00|3
04-28-23|Verkoop|-1|-1,00|4
05-13-23|Inkoop|2|20.00|5
06-17-23|Verkoop|-6|-22,00|6

De volgende tabel toont het resultaat van het uitvoeren van het rapport **Voorraadwaarde berekenen** met verschillende boekingsdatums.

|Boekingsdatum|Hoeveelheid|Opmerking|
|---|---|-------------|
04-30-23|2|Omvat alleen de resterende hoeveelheid van post 2. Post 1 wordt volledig vereffend vóór de boekingsdatum en post 5 is na de boekingsdatum.
05-31-23|4|Omvat alleen de resterende hoeveelheden van post 2 en 13.
06-30-23|0|Geen resterende hoeveelheid op boekingsdatum.

Het resultaat van de volgende posten is 0, ongeacht de boekingsdatum.

|Boekingsdatum|Artikelboekingssoort|Hoeveelheid|Kostenbedrag (werkelijk)|Postnr.|
|----|----|----|----|----|
05-13-23|Inkoop|5|5.00|1
04-26-23|Verkoop|-5|5.00|2

## <a name="see-also"></a>Zie ook

[Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md)   
[Ontwerpdetails: Waarderingsmethoden](design-details-costing-methods.md)   
[Ontwerpdetails: Voorraadwaardering](design-details-inventory-valuation.md)
[Voorraadkosten beheren](finance-manage-inventory-costs.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
