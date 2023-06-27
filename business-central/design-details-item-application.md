---
title: Ontwerpdetails - Artikelvereffening | Microsoft Docs
description: In dit onderwerp wordt beschreven waar het voorraadaantal en de voorraadwaarde worden geregistreerd wanneer u een voorraadtransactie boekt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'design, items, ledger entries, posting, inventory'
ms.date: 06/08/2021
ms.author: edupont
---
# <a name="design-details-item-application"></a>Ontwerpdetails: Artikelvereffening

Wanneer u een voorraadtransactie boekt, wordt het geboekte aantal vastgelegd in de artikelposten, en de waardeboeking in de waardeposten. Zie [Ontwerpdetails: Voorraadboeking](design-details-inventory-posting.md) voor meer informatie.  

Bovendien wordt een artikelvereffening gemaakt om de kostenontvanger aan zijn kostenbron te koppelen om te zorgen voor doorsturen van kosten volgens de waarderingsmethode. Zie [Ontwerpdetails: Waarderingsmethoden](design-details-costing-methods.md) voor meer informatie.  

[!INCLUDE[prod_short](includes/prod_short.md)] maakt twee soorten artikelvereffening.  

|Soort vereffening|Description|  
|----------------------|---------------------------------------|  
|Vereffening van aantal|Gemaakt voor alle voorraadtransacties|  
|Vereffeningskosten|Gemaakt voor inkomende posten samen met een aantalvereffening als resultaat van gebruikersinteractie in speciale processen.|  

Artikelvereffeningen kunnen op de volgende manieren worden uitgevoerd.  

|Methode|Description|Soort vereffening|  
|------------|---------------------------------------|----------------------|  
|Automatisch|Gebeurt als algemeen kosten doorsturen volgens de waarderingsmethode|Vereffening van aantal|  
|Vast|Gemaakt door de gebruiker wanneer:<br /><br /> -   Retouren verwerken<br />-   Boekingscorrecties<br />-   Aantalboekingen ongedaan maken<br />-   Doorverzendingen maken **Opmerking:** de vaste vereffening kan handmatig worden gemaakt door een volgnummer in te voeren in het veld **Vereffenen met artikelpost** of door een functie, zoals **Geboekte documentregels ophalen voor tegenboeking** te gebruiken.|Vereffening van aantal<br /><br /> Kostenvereffening **Opmerking:** kostenvereffening treedt alleen op bij inkomende transacties waarbij het veld **Vereffenen met artikelpost** wordt gevuld om een vaste vereffening te maken. Zie de volgende tabel.|  

Of vereffeningen van aantal of kosten worden gemaakt, hangt af van de richting van de voorraadtransactie en of de artikelvereffening automatisch wordt gemaakt of vast staat, in verband met speciale processen.  

De volgende tabel toont op basis van de centrale vereffeningsvelden op voorraadtransactieregels hoe de kosten stromen, afhankelijk van de transactierichting. De tabel geeft ook aan wanneer en waarom de artikelvereffening van het type aantal of kosten is.  

|-|Veld Vereffeningsnr. artikelpost|Veld Vereffenen met artikelpost|  
|-|--------------------------------|----------------------------------|  
|Vereffening voor uitgaande post|De uitgaande post haalt de kosten uit de open inkomende post.<br /><br /> **Vereffening van aantal**|Niet ondersteund|  
|Vereffening voor inkomende post|De inkomende post brengt de kosten over naar de openstaande uitgaande post.<br /><br /> De inkomende post is de kostenbron.<br /><br /> **Vereffening van aantal**|De inkomende post haalt de kosten uit de uitgaande post. **Opmerking:**  bij het maken van deze vaste vereffening wordt de inkomende transactie behandeld als een verkoopretour. De vereffende uitgaande post blijft daarom open. <br /><br /> De inkomende post is NIET de kostenbron.<br /><br /> **Vereffeningskosten**|  

> [!IMPORTANT]  
> Een verkoopretour wordt NIET beschouwd als een kostenbron als deze vast wordt toegepast.  
>
> De verkooppost blijft echter open tot de echte bron is geboekt.  

Een artikelvereffeningspost legt de volgende informatie vast.  

|Veld|Description|  
|---------------------------------|---------------------------------------|  
|**Artikelpostnr.**|Het nummer van de artikelpost voor de transactie waarvoor deze vereffeningspost is gemaakt.|  
|**Inkomend art.-postnr.**|Het artikelpostnummer van de positieve voorraadmutatie waaraan de transactie moet worden gekoppeld, indien van toepassing.|  
|**Uitgaand art.-postnr.**|Het artikelpostnummer van de negatieve voorraadmutatie waaraan de transactie moet worden gekoppeld, indien van toepassing.|  
|**Aantal**|Het toegepaste aantal.|  
|**Boekingsdatum**|De boekingsdatum van de transactie.|  

## <a name="inventory-increase"></a>Positieve voorraadmutatie
Wanneer u een positieve voorraadmutatie boekt, wordt een eenvoudige artikelvereffeningspost vastgelegd zonder een vereffening naar een uitgaande post.  

### <a name="example"></a>Opmerking
De volgende tabel toont de artikelvereffeningspost die wordt gemaakt wanneer u een inkoopontvangst van 10 artikelen boekt.  

|Boekingsdatum|Inkomend art.-postnr.|Uitgaand art.-postnr.|Aantal|Artikelpostnr.|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01-01-20|1|0|10|1|  

## <a name="inventory-decrease"></a>Negatieve voorraadmutatie
Wanneer u een negatieve voorraadmutatie boekt, wordt een artikelvereffeningspost gemaakt die de negatieve voorraadmutatie koppelt aan een positieve voorraadmutatie. Deze koppeling wordt door de waarderingsmethode van het artikel gebruikt als een richtlijn. Voor artikelen die de waarderingsmethoden FIFO, Standaard en Gemiddeld gebruiken, wordt de koppeling gebaseerd op het FIFO-principe. De negatieve voorraadmutatie wordt vereffend met de positieve voorraadmutatie met de vroegste boekingsdatum. Voor artikelen die de waarderingsmethoden LIFO gebruiken, wordt de koppeling gebaseerd op het LIFO-principe. De negatieve voorraadmutatie wordt vereffend met de positieve voorraadmutatie met de meest recente boekingsdatum.  

Het veld **Resterend aantal** in de tabel **Artikelpost** geeft het aantal aan dat nog niet is vereffend. Als het resterende aantal groter is dan 0, wordt het selectievakje **Open** ingeschakeld.  

### <a name="example-1"></a>Opmerking
Het volgende voorbeeld toont de artikelvereffeningspost die ontstaat wanneer u een verkoopverzending boekt voor vijf eenheden van de artikelen die in het vorige voorbeeld zijn ontvangen. De eerste artikelvereffeningspost is de inkoopontvangst. De tweede vereffeningspost is de verkoopverzending.  

De volgende tabel toont de twee artikelvereffeningsposten die resulteren uit respectievelijk de positieve en de negatieve voorraadmutatie.  

|Boekingsdatum|Inkomend art.-postnr.|Uitgaand art.-postnr.|Aantal|Artikelpostnr.|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|01-01-20|1|0|10|1|  
|03-01-20|1|2|-5|2|  

## <a name="fixed-application"></a>Vaste toepassing
U maakt een vaste vereffening wanneer u opgeeft dat de kosten van een positieve voorraadmutatie moeten worden vereffend met een specifieke negatieve voorraadmutatie, of andersom. De vaste vereffening beïnvloedt de resterende aantallen van de posten, en zorgt tevens voor een tegenboeking van de precieze kosten van de oorspronkelijke post waarmee of waarnaar u vereffent.  

U maakt een vaste vereffening door de velden **Vereffeningsnr. artikelpost** of **Vereffenen met artikelpost** te gebruiken om in de documentregel de artikelpost op te geven waarnaar of waarmee u de transactie wilt vereffenen. U kunt bijvoorbeeld een vaste vereffening maken wanneer u vereffeningskosten wilt maken waarin wordt bepaald dat een verkoopreturn moet worden vereffend met een specifieke verkoopverzending voor een precieze tegenboeking van de kosten van de verkoopverzending. In dit geval wordt de waarderingsmethode genegeerd door [!INCLUDE[prod_short](includes/prod_short.md)] en wordt de negatieve voorraadmutatie (of de positieve voorraadmutatie voor een verkoopretour) vereffend met de artikelpost die u opgeeft. Het voordeel van een vaste vereffening is dat de kosten van de oorspronkelijke transactie worden doorgegeven aan de nieuwe transactie.  

### <a name="example--fixed-application-in-purchase-return"></a>Voorbeeld - Vaste vereffening in inkoopretour
Het volgende voorbeeld, dat het effect toont van vaste vereffening van een inkoopretour van een artikel met de waarderingsmethode FIFO, is gebaseerd op het volgende scenario:  

1. In post 1 boekt de gebruiker een inkoop tegen kosten van LV 10,00.  
2. In post 2 boekt de gebruiker een inkoop tegen kosten van LV 20,00.  
3. In post 3 boekt de gebruiker een inkoopretour. De gebruiker maakt een vaste vereffening voor de tweede inkoop door het artikelpostnummer in te voeren in het veld **Vereffeningsnr. artikelpost** op de inkoopretourorderregel.  

De volgende tabel toont artikelposten die afkomstig zijn uit het scenario.  

|**Boekingsdatum**|**Artikelboekingssoort**|**Aantal**|**Tot. werk. kosten**|**Artikelpostnr.**|  
|----------------------|---------------------------------------------------|------------------|----------------------------------------------------|---------------------------------------------------|  
|04-01-20|Inkoop|10|10.00|1|  
|05-01-20|Inkoop|10|20.00|2|  
|06-01-20|Inkoop (retour)|-10|-20,00|3|  

Aangezien een vaste vereffening wordt uitgevoerd van de inkoopretour naar de tweede inkooppost, worden de artikelen tegen de juiste kosten geretourneerd. Als de gebruiker niet de vaste vereffening had uitgevoerd, zou het geretourneerde artikel onjuist zijn gewaardeerd op LV 10,00 omdat de retournering zou zijn toegepast op de eerste inkooppost, volgens het FIFO-principe.  

De volgende tabel toont de artikelvereffeningspost die resulteert uit de vaste vereffening.  

|Boekingsdatum|Inkomend art.-postnr.|Uitgaand art.-postnr.|Aantal|Artikelpostnr.|  
|------------------|----------------------------------------------|-----------------------------------------------|--------------|---------------------------------------------|  
|06-01-20|2|3|10|3|  

De kosten van de tweede inkoop, LV 20,00, worden dan op de juiste wijze doorgegeven aan de inkoopretour.  

### <a name="example--fixed-application-with-average-cost"></a>Voorbeeld - Vaste vereffening met gemiddelde kosten
Het volgende voorbeeld, dat het effect toont van vaste vereffening, is gebaseerd op het volgende scenario voor een artikel met de waarderingsmethode Gemiddeld:  

1. In post nummer 1 en 2 boekt de gebruiker twee inkoopfacturen. De tweede factuur heeft de foutieve directe kostprijs van LV 1000,00.  
2. In postnummer 3 boekt de gebruiker een inkoopcreditnota met een vaste vereffening die met de inkooppost wordt vereffend met de verkeerde directe kostprijs. De som van het veld **Tot. werk. kosten** voor de twee vast vereffende waardeposten wordt 0,00  
3. In post nummer 4 boekt de gebruiker een andere inkoopfactuur met de juiste directe kostprijs van LV 100,00  
4. In post nummer 5 boekt de gebruiker een verkoopfactuur.  
5. Het voorraadaantal is 0 en de voorraadwaarde is ook 0,00  

De volgende tabel toont het resultaat van het scenario op de waardeposten van het artikel.  

De volgende tabel toont het resultaat van het scenario op de waardeposten van het artikel nadat de boeking is voltooid en de kostencorrectie is uitgevoerd.

|Boekingsdatum|Artikelpostsoort|Gewaardeerd aantal|Tot. werk. kosten|Vereffeningsnr. artikelpost|Gewaardeerd volgens gem. ink.-prijs|Artikelpostnr.|Postnr.|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|--------------------------------------------|-------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Inkoop|1|200.00||Nr.|1|1|  
|01-01-20|Inkoop|1|1000.00||Nee|2|2|  
|01-01-20|Inkoop|-1|-1000|2|Nee|3|3|  
|01-01-20|Inkoop|1|100.00||Nee|4|4|  
|01-01-20|Verkoop|-2|-300,00||Ja|5|5|  

Als de gebruiker niet de vaste vereffening tussen de inkoopcreditnota en de inkoop had uitgevoerd met de onjuiste directe kostprijs (stap 2 in het vorige scenario), waren de kosten anders bijgewerkt.  

De volgende tabel toont het resultaat van de waardeposten van het artikel als stap 2 in het vorige scenario zonder een vaste vereffening wordt uitgevoerd.  

|Boekingsdatum|Artikelboekingssoort|Gewaardeerd aantal|Tot. werk. kosten|Vereffeningsnr. artikelpost|Gewaardeerd volgens gem. ink.-prijs|Artikelpostnr.|Postnr.|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|--------------------------------------------|-------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Inkoop|1|200.00||Nr.|1|1|  
|01-01-20|Inkoop|1|1000.00||Nee|2|2|  
|01-01-20|Inkoop|-1|433,33||Ja|3|3|  
|01-01-20|Inkoop|1|100.00||Nee|4|4|  
|01-01-20|Verkoop|-2|866,67||Ja|5|5|  

In post nummer 3 wordt de waarde in het veld **Tot. werk. kosten** gewaardeerd op gemiddelde en daarom bevat deze de onjuiste boeking van 1000,00. Het wordt dus -433.33, wat een verhoogd kostenbedrag is. De berekening is 1300 / 3 = .-433,33.  

In post nummer 5 is de waarde van het veld **Tot. werk. kosten** voor deze post om dezelfde reden ook onjuist.  

> [!NOTE]  
>  Als u een vaste vereffening maakt voor een negatieve voorraadmutatie van een artikel dat de waarderingsmethode Gemiddeld gebruikt, ontvangt de negatieve mutatie niet, zoals gebruikelijk, de gemiddelde kosten voor het artikel, maar de kosten van de door u opgegeven negatieve voorraadmutatie. Deze mutatie maakt dan niet langer deel uit van de berekening van de gemiddelde inkoopprijs.  

### <a name="example--fixed-application-in-sales-return"></a>Voorbeeld - Vaste vereffening in verkoopretour
Vaste vereffeningen zijn ook een goede manier om kosten exact tegen te boeken, zoals bij verkoopretouren.  

In het volgende voorbeeld wordt getoond hoe een vaste vereffening zorgt voor exacte kostentegenboeking en is gebaseerd op het volgende scenario:  

1.  De gebruiker boekt een inkoopfactuur.  
2.  De gebruiker boekt een verkoopfactuur.  
3.  De gebruiker boekt een verkoopcreditnota voor het geretourneerde artikel, dat van toepassing is op de verkooppost, om de kosten correct tegen te boeken.  
4.  Er komen vrachtkosten in verband met de inkooporder die eerder is geboekt. De gebruiker boekt het als een artikeltoeslag.  

De volgende tabel toont het resultaat van scenariostappen 1 t/m 3 voor de waardeposten van het artikel.  

|Boekingsdatum|Artikelpostsoort|Gewaardeerd aantal|Tot. werk. kosten|Vereffenen met artikelpost|Artikelpostnr.|Postnr.|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Inkoop|1|1000.00||1|1|  
|01-02-20|Verkoop|-1|1000.00||2|2|  
|01-03-20|Verkoop (creditnota)|1|1000|2|3|3|  

De volgende tabel toont de waardepost die resulteert uit scenariostap 4, het boeken van de artikeltoeslag.  

|Boekingsdatum|Artikelboekingssoort|Gewaardeerd aantal|Tot. werk. kosten|Vereffenen met artikelpost|Artikelpostnr.|Postnr.|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-04-20|(Artikeltoeslag)|1|100.00||1|4|  

De volgende tabel toont het effect van de exacte kostenterugboeking op de waardeposten van het artikel.  

|Boekingsdatum|Artikelpostsoort|Gewaardeerd aantal|Tot. werk. kosten|Vereffenen met artikelpost|Artikelpostnr.|Postnr.|  
|-------------------------------------|-----------------------------------------------|-----------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------------|----------------------------------|  
|01-01-20|Inkoop|1|1000.00||1|1|  
|01-02-20|Verkoop|-1|1100.00||2|2|  
|01-03-20|Verkoop (creditnota)|1|1100.00|2|3|3|  
|01-04-20|(Artikeltoeslag)|1|100.00||1|4|  

Wanneer u de batchverwerking **Kostprijs herwaarderen - Artikelposten** uitvoert, worden de toegenomen kosten van de inkooppost als gevolg van de artikeltoeslag doorgestuurd naar de verkooppost volgnummer 2. De verkooppost stuurt vervolgens deze verhoogde kosten door naar de verkoopcreditpost (volgnummer 3). Het eindresultaat is dat de kosten correct zijn tegengeboekt.  

> [!NOTE]  
>  Als u met retouren of creditnota's werkt en u het veld **Precieze kostenvereff. verplicht** hebt ingesteld op de pagina **Inkoopinstellingen** of de pagina **Instellingen van verkoop en tegoeden**, zoals van toepassing in uw situatie, vult [!INCLUDE[prod_short](includes/prod_short.md)] automatisch de verschillende vereffeningspostvelden in wanneer u de functie **Kopiëren uit document** gebruikt. Als u de functie **Geboekte documentregels ophalen voor tegenboeking** gebruikt, worden deze velden altijd automatisch ingevuld.  

> [!NOTE]  
>  Als u een transactie boekt met een vaste vereffening en vereffent met een gesloten artikelpost, hetgeen betekent dat het resterende aantal nul blijft, wordt de oude vereffening automatisch ongedaan gemaakt en wordt de artikelpost nogmaals vereffend met gebruik van de door u opgegeven vaste vereffening.  

## <a name="transfer-application"></a>Transfervereffening
Als een artikel wordt overgebracht van de ene vestiging naar een andere binnen de bedrijfsvoorraad, wordt een vereffening gemaakt tussen de twee transferposten. Het waarderen van een transferpost is afhankelijk van de waarderingsmethode. Voor artikelen die de waarderingsmethode Gemiddeld gebruiken, wordt waardering uitgevoerd in de gemiddelde-kostprijsperiode waarin de herwaarderingsdatum van de transfer ligt. Voor artikelen die andere waarderingsmethoden gebruiken, wordt waardering uitgevoerd door terugtracering naar de kosten van de oorspronkelijke positieve voorraadmutatie.  

### <a name="example--average-costing-method"></a>Voorbeeld - Gemiddelde waarderingsmethode
In het volgende voorbeeld wordt getoond hoe transferposten worden vereffend, en is gebaseerd op het volgende scenario voor een artikel dat de waarderingsmethode Gemiddeld gebruikt en een periode voor gemiddelde kosten van Dag.  

1. De gebruiker koopt het artikel tegen kosten van LV 10,00.  
2. De gebruiker koopt het artikel nogmaals tegen kosten van LV 20,00.  
3. De gebruiker brengt het artikel over van de OOST naar de WEST vestiging.  

De volgende tabel toont het effect van de transfer op de waardeposten van het artikel.  

|Boekingsdatum|Artikelpostsoort|Vestiging|Gewaardeerd aantal|Tot. werk. kosten|Volgnummer|  
|-------------------------------------|-----------------------------------------------|--------------------------------------|-----------------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|Inkoop|OOST|1|10.00|1|  
|01-01-20|Inkoop|OOST|1|20.00|2|  
|01-02-20|Transfer|OOST|-1|15.00|3|  
|01-02-20|Transfer|WEST|1|15.00|4|  

### <a name="example--standard-costing-method"></a>Voorbeeld: Waarderingsmethode Standaard
In het volgende voorbeeld wordt getoond hoe transferposten worden vereffend, en is gebaseerd op het volgende scenario voor een artikel dat de waarderingsmethode Standaard gebruikt en een periode voor gemiddelde kosten van Dag.  

1. De gebruiker koopt het artikel tegen een vaste verrekenprijs van LV 10,00.  
2. De gebruiker brengt het artikel over van de OOST naar de WEST vestiging tegen een vaste verrekenprijs van LV 12,00.  

De volgende tabel toont het effect van de transfer op de waardeposten van het artikel.  

|Boekingsdatum|Artikelpostsoort|Vestiging|Gewaardeerd aantal|Tot. werk. kosten|Volgnummer|  
|-------------------------------------|-----------------------------------------------|--------------------------------------|-----------------------------------------|------------------------------------------------|----------------------------------|  
|01-01-20|Inkoop|OOST|1|10.00|1|  
|01-02-20|Transfer|OOST|-1|10.00|2|  
|01-02-20|Transfer|WEST|1|10.00|3|  

Aangezien de waarde van de oorspronkelijke voorraadtoename LV 10,00 is, is de verplaatsing gewaardeerd tegen die kosten, niet op LV 12,00.  

## <a name="reapplication"></a>Opnieuw vereffenen
Vanwege de manier waarop de kostprijs van een artikel wordt berekend, kan een onjuiste artikelvereffening leiden tot onjuiste gemiddelde kosten en kostprijs. De volgende scenario's kunnen onjuiste artikelvereffeningen veroorzaken, waardoor u artikelvereffeningen ongedaan moet maken en artikelposten opnieuw moet vereffenen:  

* U bent vergeten een vaste vereffening te maken.  
* U hebt een onjuiste vaste vereffening uitgevoerd.  
* U wilt de vereffening negeren die automatisch wordt gemaakt wanneer u boekt, volgens de waarderingsmethode van het artikel.  
* U moet een artikel retourneren waarop een verkoop al handmatig is toegepast zonder de functie **Geboekte documentregels ophalen voor tegenboeking** te gebruiken en u moet daarom de vereffening ongedaan maken.  

[!INCLUDE[prod_short](includes/prod_short.md)] biedt een functie voor het analyseren en corrigeren van artikelvereffeningen. Dit werk wordt uitgevoerd op de pagina **Vereffeningsvoorstel**.  

## <a name="see-also"></a>Zie ook
[Ontwerpdetails: bekend probleem met artikelvereffening](design-details-inventory-zero-level-open-item-ledger-entries.md)  
[Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md)  
[Ontwerpdetails: Waarderingsmethoden](design-details-costing-methods.md)  
[Ontwerpdetails: Gemiddelde kostprijs](design-details-average-cost.md)   
[Ontwerpdetails: Kostenwaardering](design-details-cost-adjustment.md)  
[Voorraadkosten beheren](finance-manage-inventory-costs.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
