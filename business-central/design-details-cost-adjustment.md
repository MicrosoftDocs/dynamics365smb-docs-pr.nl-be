---
title: 'Ontwerpdetails: Kostenwaardering'
description: 'Kostenherwaardering stuurt wijzigingen in kosten van kostenbronnen door naar kostenontvangers, volgens de waarderingsmethode van een artikel, om de juiste voorraadwaardering te bieden.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/14/2021
ms.author: edupont
---
# <a name="design-details-cost-adjustment"></a>Ontwerpdetails: Kostenwaardering

Het belangrijkste doel van kostenherwaardering is wijzigingen in kosten van kostenbronnen door te sturen naar kostenontvangers, volgens de waarderingsmethode van een artikel, om de juiste voorraadwaardering te bieden.  

Een artikel kan als verkoop worden gefactureerd voordat het als inkoop wordt gefactureerd, zodat de vastgelegde voorraadwaarde van de verkoop niet overeenkomt met de werkelijke inkoopkosten. Kostenherwaardering werkt de kosten van verkochte goederen (KPV) bij voor historische verkoopkosten om te zorgen dat ze overeenkomen met de inkomende transacties waarmee ze worden vereffend. Zie [Ontwerpdetails: artikelvereffening](design-details-item-application.md) voor meer informatie.  

Hierna volgen secundaire doelen, of functies, van kostenherwaardering:  

* Gereedgemelde productieorders factureren:  

  * Wijzig de status van waardeposten van **Verwacht** in **Werkelijk**.  
  * Wis OHW-rekeningen. Zie [Ontwerpdetails: Productieorderboeking](design-details-production-order-posting.md) voor meer informatie.  
  * Verschil boeken. Zie voor meer informatie [Ontwerpdetails: Verschil](design-details-variance.md).  
  * Werk de kostprijs op de artikelkaart bij.  

Voorraadkosten moeten worden bijgewerkt als de gerelateerde waardeposten kunnen worden afgestemd met het grootboek. Zie voor meer informatie [Ontwerpdetails: reconciliatie met het grootboek](design-details-reconciliation-with-the-general-ledger.md).  

## <a name="detecting-the-adjustment"></a>De correctie detecteren

De taak van het detecteren of kostenwaardering moet worden uitgevoerd, wordt hoofdzakelijk uitgevoerd door de routine Artikeldagboek. - Regel boeken. De taak van het berekenen en genereren van kostenherwaarderingsposten wordt uitgevoerd door de batchverwerking **Kostprijs herwaarderen - Artikelposten**.  

Voor het doorsturen van kosten bepaalt het detectiemechanisme welke bronnen zijn gewijzigd wat betreft kosten en naar welke bestemming deze kosten moeten worden doorgestuurd. Er zijn de volgende drie detectiefuncties in [!INCLUDE[prod_short](includes/prod_short.md)]:  

* Artikelvereffeningspost  
* Invoerpunt gemiddelde kostprijscorrectie  
* Orderniveau  

### <a name="item-application-entry"></a>Artikelvereffeningspost

Deze detectiefunctie wordt gebruikt voor artikelen die de waarderingsmethoden FIFO, LIFO, Standaard en Specifiek gebruiken en voor vaste vereffeningenscenario's. De functie werkt als volgt:  

* Kostenherwaardering wordt gedetecteerd door de bronartikelposten te markeren als *Vereff. post herwaarderen* wanneer een artikelpost of waardepost wordt geboekt.  
* Kosten worden doorgestuurd volgens de ketens van de kosten die zijn vastgelegd in de tabel **Artikelvereffeningspost**.  

### <a name="average-cost-adjustment-entry-point"></a>Invoerpunt gemiddelde kostprijscorrectie

Deze detectiefunctie wordt gebruikt voor artikelen die de waarderingsmethode Gemiddeld gebruiken. De functie werkt als volgt:  

* Kostenherwaardering wordt gedetecteerd door een record in de tabel **Gem. kostprijsaanpassing invoerhaven** te markeren wanneer een waardepost wordt geboekt.  
* Kosten wordt doorgestuurd door de kosten toe te passen op waardeposten met een latere waarderingsdatum.  

### <a name="order-level"></a>Orderniveau

Deze detectiefunctie wordt gebruikt voor conversiescenario's, productie en assemblage. De functie werkt als volgt:  

* Kostenherwaardering wordt gedetecteerd door de order te markeren telkens wanneer een materiaal/resource wordt geboekt als verbruikt/gebruikt voor de order.  
* Kosten wordt doorgestuurd door de kosten voor het materiaal/de resource toe te passen op de uitvoerposten die aan dezelfde order zijn gekoppeld.  

De functie op orderniveau wordt gebruikt om correcties in assemblageboekingen te detecteren. De volgende afbeelding toont de structuur van de herwaarderingspost:  

![Stroom van posten in kostencorrectie.](media/design_details_assembly_posting_3.png "Stroom van posten in kostencorrectie")  

Zie [Ontwerpdetails: assemblageorderboeking](design-details-assembly-order-posting.md) voor meer informatie.  

## <a name="manual-versus-automatic-cost-adjustment"></a>Handmatige versus automatische kostenwaardering

Kostenherwaardering kan op twee manieren worden uitgevoerd:  

* Handmatig door de batchverwerking **Kostprijs herwaarderen - Artikelposten** uit te voeren. U kunt deze batchverwerking uitvoeren voor alle artikelen of alleen voor bepaalde artikelen of artikelcategorieën. Met deze batchverwerking wordt een kostenherwaardering uitgevoerd voor de artikelen op voorraad waarvoor een inkomende transactie is gemaakt, zoals een aankoop. Voor artikelen die de gemiddelde waarderingsmethode gebruiken, maakt de batchverwerking ook een correctie als uitgaande transacties worden gemaakt.  
* Automatisch, door telkens kosten aan te passen wanneer u een voorraadtransactie boekt en wanneer u een productieorder beëindigt. De kostenherwaardering wordt alleen uitgevoerd voor specifieke artikel(en) die worden beïnvloed door het boeken. Dit wordt ingesteld wanneer u het selectievakje **Automatische kostenwaardering** op de pagina **Voorraadinstelling** inschakelt.  

Het is goed om de kostenwaardering automatisch uit te voeren wanneer u boekt, omdat eenheidskosten vaker worden bijgewerkt en daarom accurater zijn. Het nadeel is dat de prestaties van de database kunnen worden beïnvloed door de kostenherwaardering zo vaak uit te voeren.  

Omdat het belangrijk is de kostprijs van een artikel bijgewerkt te houden, wordt het aangeraden de batchverwerking **Kostprijs herwaarderen - Artikelposten** zo vaak mogelijk gedurende vrije uren uit te voeren. Of u gebruikt automatische kostenwaardering. Hierdoor wordt gezorgd dat de kostprijs dagelijks wordt bijgewerkt voor artikelen.  

Ongeacht of u kostenwaardering handmatig of automatisch uitvoert, het waarderingsproces en de gevolgen ervan zijn hetzelfde. [!INCLUDE[prod_short](includes/prod_short.md)] berekent de waarde van de inkomende transactie en stuurt die kosten door naar uitgaande transacties, zoals verkopen of verbruik, die met de inkomende transactie zijn vereffend. Door de kostenherwaardering worden waardeposten gemaakt die correctiebedragen bevatten en bedragen die afrondingen compenseren.  

De nieuwe waardeposten voor herwaardering en afronding hebben de boekingsdatum van de bijbehorende factuur. Uitzonderingen zijn als de waardeposten in een afgesloten voorraadperiode of boekhoudperiode vallen of als de boekingsdatum eerder is dan de datum in het veld **Boeken toegest. vanaf** op de pagina **Grootboekinstellingen**. Als dit gebeurt, wordt door de batchverwerking de boekingsdatum toegewezen als de eerste datum van de volgende open periode.  

## <a name="adjust-cost---item-entries-batch-job"></a>Batchverwerking Voorraadwaarde (Werk.-kosten)

Wanneer u de batchverwerking **Kostprijs herwaarderen - Artikelposten** uitvoert, hebt u de mogelijkheid de batchverwerking voor alle artikelen of alleen voor bepaalde artikelen of categorieën uit te voeren.  

> [!NOTE]  
> We adviseren altijd de batchverwerking uit te voeren voor alle artikelen en de filteroptie alleen te gebruiken om de uitvoeringstijd van de batchverwerking te beperken of de kosten van een bepaald artikel te corrigeren.  

### <a name="example"></a>Opmerking

In het volgende voorbeeld wordt getoond dat u een aangeschaft artikel boekt als ontvangen en gefactureerd op 01-01-20. U boekt het verkochte artikel later als verzonden en gefactureerd op 15-01-20. Vervolgens voert u de batchverwerkingen **Kostprijs herwaarderen - Artikelposten** en **Voorraadwaarde boeken** uit. De volgende posten worden gemaakt.  

#### <a name="value-entries-1"></a>Waardeposten (1)

|Boekingsdatum|Artikelboekingssoort|Tot. werk. kosten|Vrd.-waarde geboekt|Geboekt aantal|Volgnummer|  
|------------|----------------------|--------------------|------------------|-----------------|---------|  
|01-01-20|Inkoop|10.00|10.00|1|1|  
|15-01-20|Verkoop|-10,00|-10,00|-1|2|  

#### <a name="relation-entries-in-the-gl--item-ledger-relation-table-1"></a>Relatieposten in het grootboek - tabel Artikelpostrelatie (1)

|Grootboekpostnr.|Waardepostnr.|Grootboekjournaalnr.|  
|-------------|---------------|----------------|  
|1|1|1|  
|2|1|1|  
|3|2|1|  
|4|2|1|  

#### <a name="general-ledger-entries-1"></a>Grootboekposten (1)

|Boekingsdatum|Grootboekrekening|Rekeningnr. (En-US demo)|Bedrag|Volgnummer|  
|------------------|------------------|---------------------------------|------------|---------------|  
|01-01-20|[Voorraadrekening]|2130|10.00|1|  
|01-01-20|[Vereffeningsrekening directe kosten]|7291|-10,00|2|  
|15-01-20|[Voorraadrekening]|2130|-10,00|3|  
|15-01-20|[KPV-rekening]|7290|10.00|4|  

Later boekt u een gerelateerde inkoopartikeltoeslag voor 2,00 LV, gefactureerd op 02-10-20. U voert de batchverwerking **Kostprijs herwaarderen - Artikelposten** uit en voert vervolgens de batchverwerking **Voorraadwaarde boeken** uit. De batchverwerking voor het herwaarderen van de kosten past de kosten van de verkoop dienovereenkomstig aan met 2,00 LV en de batchverwerking **Voorraadwaarde boeken** boekt de nieuwe waardeposten in het grootboek. Dit is het resultaat.  

#### <a name="value-entries-2"></a>Waardeposten (2)

|Boekingsdatum|Artikelpostsoort|Tot. werk. kosten|Kosten geboekt naar grootboek|Geboekt aantal|Herwaardering|Volgnummer|  
|------------|----------------------|--------------------|------------------|-----------------|----------|---------|  
|10-02-20|Inkoop|2.00|2.00|0|Nee|3|  
|15-01-20|Verkoop|-2,00|-2,00|0|Ja|4|  

#### <a name="relation-entries-in-the-gl--item-ledger-relation-table-2"></a>Relatieposten in het grootboek - tabel Artikelpostrelatie (2)

|Grootboekpostnr.|Waardepostnr.|Grootboekjournaalnr.|  
|-------------|---------------|----------------|  
|5|3|2|  
|6|3|2|  
|7|4|2|  
|8|4|2|  

#### <a name="general-ledger-entries-2"></a>Grootboekposten (2)

|Boekingsdatum|Grootboekrekening|Rekeningnr. (En-US demo)|Bedrag|Volgnummer|  
|------------|-----------|------------------------|------|---------|  
|10-02-20|[Voorraadrekening]|2130|2.00|5|  
|10-02-20|[Vereffeningsrekening directe kosten]|7291|-2,00|6|  
|15-01-20|[Voorraadrekening]|2130|-2,00|7|  
|15-01-20|[KPV-rekening]|7290|2.00|8|  

## <a name="automatic-cost-adjustment"></a>Automatische kostenwaardering

Als u kostenwaardering wilt instellen die automatisch wordt uitgevoerd wanneer u een voorraadtransactie boekt, gebruikt u het veld **Automatische kostenwaardering** op de pagina **Voorraadinstelling**. Dit veld biedt u de mogelijkheid te selecteren hoe lang vóór de huidige werkdatum automatische kostenwaardering mag worden uitgevoerd. De volgende opties zijn mogelijk.  

|Optie|Description|
|------|-----------|
|Nooit|De kostprijs wordt niet geherwaardeerd wanneer u boekt.|  
|Dag|De kostprijs wordt geherwaardeerd als de boeking binnen één dag vóór de werkdatum plaatsvindt.|  
|Week|De kostprijs wordt geherwaardeerd als de boeking binnen een week vóór de werkdatum plaatsvindt.|  
|Maand|De kostprijs wordt geherwaardeerd als de boeking binnen een maand vóór de werkdatum plaatsvindt.|  
|Kwartaal|De kostprijs wordt geherwaardeerd als de boeking binnen een kwartaal vóór de werkdatum plaatsvindt.|  
|jaar|De kostprijs wordt geherwaardeerd als de boeking binnen een jaar vóór de werkdatum plaatsvindt.|  
|Altijd|De kostprijs wordt altijd geherwaardeerd wanneer u boekt, ongeacht de boekingsdatum.|  

De keuze die u in het veld **Automatische kostenwaardering** maakt is belangrijk voor de prestaties en nauwkeurigheid van de kosten. Kortere perioden, bijvoorbeeld **Dag** of **Week**, hebben invloed op systeemprestaties omdat hiermee de strengere vereiste geldt dat alleen kosten die op de laatste dag of in de laatste week zijn geboekt, automatisch kunnen worden aangepast. Dit betekent dat de automatische kostenwaardering niet zo frequent wordt uitgevoerd, wat invloed heeft op systeemprestaties. Dit betekent echter ook dat de kostprijs minder nauwkeurig kan zijn.  

### <a name="example-1"></a>Opmerking

In het volgende voorbeeld wordt een automatisch kostenherwaarderingscenario getoond:  

* Op 10 januari boekt u een ingekocht artikel als ontvangen en gefactureerd.  
* Op 15 januari boekt u een verkooporder voor het artikel als verzonden en gefactureerd.
* Op 5 februari ontvangt u een factuur voor verzendkosten op de oorspronkelijke inkoop. U boekt deze verzendkosten, vereffent deze met de oorspronkelijke inkoopfactuur, waardoor de kosten van de oorspronkelijke aankoop worden verhoogd.  

Als u de automatische kostenwaardering hebt ingesteld om toe te passen op boekingen die plaatsvinden binnen een maand of een kwartaal vanaf de huidige werkdatum, wordt de automatische kostprijsaanpassing uitgevoerd, en worden de kosten van de inkoop naar de verkoop doorgestuurd.  

Als u automatische kostenwaardering hebt ingesteld om toe te passen op boekingen die plaatsvinden binnen een dag of een week vanaf de huidige werkdatum, wordt de automatische kostprijsaanpassing niet uitgevoerd, en worden de kosten van de inkoop niet naar de verkoop doorgestuurd totdat u de batchverwerking **Kostprijs herwaarderen - Artikelposten** uitvoert.  

## <a name="see-also"></a>Zie ook

[Artikelkosten herwaarderen](inventory-how-adjust-item-costs.md)  
[Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md)  
[Ontwerpdetails: Reconciliatie met het grootboek](design-details-reconciliation-with-the-general-ledger.md)  
[Ontwerpdetails: Voorraadboeking](design-details-inventory-posting.md)  
[Ontwerpdetails: Verschil](design-details-variance.md)  
[Ontwerpdetails: Assemblageorderboeking](design-details-assembly-order-posting.md)  
[Ontwerpdetails: Productieorderboeking](design-details-production-order-posting.md)  
[Voorraadkosten beheren](finance-manage-inventory-costs.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
