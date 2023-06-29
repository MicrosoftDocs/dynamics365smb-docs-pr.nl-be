---
title: Afschrijvingsmethoden voor vaste activa
description: 'Lees meer over de verschillende ingebouwde methoden om vaste activa af te schrijven of in waarde te verminderen in de standaardversie van Business Central, die acht methoden bevat.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: write down
ms.search.form: '5629, 5633'
ms.date: 07/05/2021
ms.author: edupont
---
# <a name="depreciation-methods-for-fixed-assets"></a><a name="depreciation-methods-for-fixed-assets"></a>Afschrijvingsmethoden voor vaste activa

Er zijn acht afschrijvingsmethoden beschikbaar in de standaardversie van [!INCLUDE [prod_short](includes/prod_short.md)]​:  

* Lineair  
* Boekwaarde-afschrijving 1  
* Boekwaarde-afschrijving 2  
* Boekwaarde 1  
* Boekwaarde 2  
* Eigen definitie  

  > [!NOTE]  
  > Specificeer uw eigen afschrijvingsmethode door afschrijvingstabellen te definiëren. Voor informatie over het toepassen van een door de gebruiker gedefinieerde afschrijvingsmethode zie [Door de gebruiker gedefinieerde afschrijvingsmethode instellen](fa-how-setup-user-defined-depreciation-method.md).
* Handmatig  

  > [!NOTE]  
  > Gebruik deze methode voor activa waarop niet wordt afgeschreven, bijvoorbeeld grond. U moet afschrijving invoeren in het VA-financiële dagboek. Uit de batchverwerking **Afschrijving berekenen** worden de vaste activa weggelaten die deze afschrijvingsmethode gebruiken.  
* Halfjaarlijkse afspraak  

  > [!NOTE]  
  > Wanneer u deze methode gebruikt, wordt een vast activum elk jaar met hetzelfde bedrag afgeschreven.  

## <a name="straight-line-depreciation"></a><a name="straight-line-depreciation"></a>Lineaire afschrijving

Als u de lineaire afschrijvingsmethode gebruikt, moet u een van de volgende opties opgeven in het afschrijvingsboek voor vaste activa:  

* De afschrijvingsperiode (jaren of maanden) of een einddatum voor de afschrijving  
* Een vast jaarpercentage  
* Een vast jaarbedrag  
* Afschrijvingsperiode  

### <a name="depreciation-period"></a><a name="depreciation-period"></a>Afschrijvingsperiode

Als u de afschrijvingsperiode invoert (aantal afschrijvingsjaren, aantal afschrijvingsmaanden of de einddatum voor de afschrijving), wordt de volgende formule gebruikt om het afschrijvingsbedrag te berekenen:  

*Afschrijvingsbedrag = ((Boekwaarde - Restwaarde) x Aantal afschrijvingsdagen) / Resterende afschrijvingsdagen*  

Resterende afschrijvingsdagen zijn het aantal afschrijvingsdagen min het aantal dagen tussen de begindatum van de afschrijving en de datum van de laatste post voor vaste activa.  

De boekwaarde kan worden verminderd door de geboekte waardevermeerdering, waardevermindering, bedragen voor vrij 1 en vrij 2. Bepalend hiervoor is of het veld **Opnemen in afschr.-berekening** is uitgeschakeld en of het veld **Deel v. boekwaarde** op de pagina **VA-boekingssoortinstellingen** is ingeschakeld. Deze berekening zorgt ervoor dat het vaste activum volledig is afgeschreven op de einddatum van de afschrijving.  

### <a name="fixed-yearly-percentage"></a><a name="fixed-yearly-percentage"></a>Vast jaarpercentage

Als u een vast jaarpercentage invult, wordt de volgende formule gebruikt om het afschrijvingsbedrag te berekenen:  

*Afschrijvingsbedrag = (Lineair % x Afschrijvingsbasis x Aantal afschrijvingsdagen) / (100 x 360)*  

### <a name="fixed-yearly-amount"></a><a name="fixed-yearly-amount"></a>Vast jaarbedrag

Als u een vast jaarbedrag invult, wordt de volgende formule gebruikt om het afschrijvingsbedrag te berekenen:  

*Afschrijvingsbedrag = (Vast afschrijvingsbedrag x Aantal afschrijvingsdagen) /360*  

### <a name="example---straight-line-depreciation"></a><a name="example---straight-line-depreciation"></a>Voorbeeld: lineaire afschrijving

De aanschafkosten van een vast activum bedragen LV 100.000. De verwachte levensduur is acht jaar. De batchverwerking **Afschrijving berekenen** wordt elk half jaar uitgevoerd.  

Voor dit voorbeeld ziet de post voor vaste activa er als volgt uit:  

| Datum | VA-boekingssoort | Dagen | Bedrag | Boekwaarde |
| --- | --- | --- | --- | --- |
| 01/01/20 |Aanschafkosten |(Begindatum afschrijving) |100,000.00 |100,000.00 |
| 06/30/20 |Afschrijvingen |180 |-6.250,00 |93,750.00 |
| 12/31/20 |Afschrijvingen |180 |-6.250,00 |87,500.00 |
| 06/30/21 |Afschrijvingen |180 |-6.250,00 |81,250.00 |
| 12/31/21 |Afschrijvingen |180 |-6.250,00 |75,000.00 |
| 06/30/27 |Afschrijvingen |180 |-6.250,00 |6,250.00 |
| 12/31/27 |Afschrijvingen |180 |-6.250,00 |0 |

## <a name="declining-balance-1-depreciation"></a><a name="declining-balance-1-depreciation"></a>Boekwaarde-afschrijving 1

Dit is een versnelde afschrijvingsmethode waarbij het grootste gedeelte van de kostprijs van een activum wordt verdeeld over de eerste jaren van de gebruiksduur. Als u deze methode gebruikt, moet u een vast jaarpercentage invullen.  

Met de volgende formule worden afschrijvingsbedragen berekend:  

*Afschrijvingsbedrag = (Boekwaarde afschr. % x Aantal afschrijvingsdagen x Afschrijvingsbasis) / (100 x 360)*  

De afschrijvingsbasis is de boekwaarde, verminderd met de geboekte afschrijving sinds de begindatum van het lopende boekjaar.  

De geboekte afschrijving kan posten met verschillende boekingssoorten bevatten (waardevermindering, vrij 1 en vrij 2), die zijn geboekt sinds de begindatum van het lopende boekjaar. Deze boekingssoorten worden opgenomen in het geboekte afschrijvingsbedrag als de velden **Afschrijvingssoort** en **Deel v. boekwaarde** op de pagina **VA-boekingssoortinstellingen** zijn ingeschakeld.  

### <a name="example---declining-balance-1-depreciation"></a><a name="example---declining-balance-1-depreciation"></a>Voorbeeld - boekwaarde-afschrijving 1 afschrijving

De aanschafkosten van een vast activum bedragen LV 100.000. Het veld **Boekwaarde afschr. %** is 25. De batchverwerking **Afschrijving berekenen** wordt elk half jaar uitgevoerd.  

In de volgende tabel ziet u hoe de posten van een vast activum eruit zien.  

| Datum | VA-boekingssoort | Dagen | Bedrag | Boekwaarde |
| --- | --- | --- | --- | --- |
| 01/01/20 |Aanschafkosten |(Begindatum afschrijving) |100,000.00 |100,000.00 |
| 06/30/20 |Afschrijvingen |180 |-12.500,00 |87,500.00 |
| 12/31/20 |Afschrijvingen |180 |-12.500,00 |75,000.00 |
| 06/30/21 |Afschrijvingen |180 |-9.375,00 |65,625.00 |
| 12/31/21 |Afschrijvingen |180 |-9.375,00 |56,250.00 |
| 06/30/22 |Afschrijvingen |180 |-7.031,25 |49,218.75 |
| 12/31/22 |Afschrijvingen |180 |-7.031,25 |42,187.50 |
| 06/30/23 |Afschrijvingen |180 |-5.273,44 |36,914.06 |
| 12/31/23 |Afschrijvingen |180 |-5.273,44 |31,640.62 |
| 06/30/24 |Afschrijvingen |180 |-3.955,08 |27,685.54 |
| 12/31/24 |Afschrijvingen |180 |-3.955,08 |23,730.46 |

Berekeningsmethode:  

* Jaar 1: *25% van 100.000 = 25.000 = 12.500 + 12.500*

* Jaar 2: *25% van 75.000 = 18.750 = 9.375 + 9.375*

* Jaar 3: *25% van 56.250 = 14.062,50 = 7.031,25 + 7.031,25*

De berekening gaat door totdat de boekwaarde gelijk is aan het maximale restbedrag na afschrijving of aan de opgegeven restwaarde.  

## <a name="declining-balance-2-depreciation"></a><a name="declining-balance-2-depreciation"></a>Boekwaarde-afschrijving 2

Met de methoden Boekwaarde-afschrijving 1 en Boekwaarde-afschrijving 2 wordt voor ieder jaar hetzelfde totale afschrijvingsbedrag berekend. Als u de batchverwerking **Afschrijving berekenen** echter meer dan één keer per jaar uitvoert, zorgt de methode Boekwaarde-afschrijving 1 voor gelijke afschrijvingsbedragen per afschrijvingsperiode. De methode Boekwaarde-afschrijving 2 zorgt daarentegen voor afschrijvingsbedragen die bij iedere volgende afschrijvingsperiode lager worden.  

### <a name="example---declining-balance-2-depreciation"></a><a name="example---declining-balance-2-depreciation"></a>Voorbeeld: boekwaarde-afschrijving 2

De aanschafkosten van een vast activum bedragen LV 100.000. Het veld **Boekwaarde afschr. %** is 25. De batchverwerking **Afschrijving berekenen** wordt elk half jaar uitgevoerd. De VA-posten zien er als volgt uit:  

| Datum | VA-boekingssoort | Dagen | Bedrag | Boekwaarde |
| --- | --- | --- | --- | --- |
| 01/01/20 |Aanschafkosten |(Begindatum afschrijving)|100,000.00 |100,000.00 |
| 06/30/20 |Afschrijvingen |180 |-13.397,46 |86,602.54 |
| 12/31/20 |Afschrijvingen |180 |-11.602,54 |75,000.00 |
| 06/30/21 |Afschrijvingen |180 |-10.048,09 |64,951.91 |
| 12/31/21 |Afschrijvingen |180 |-8.701,91 |56,250.00 |

Berekeningsmethode:  

* *BW* = Boekwaarde  
* *AD* = Aantal afschrijvingsdagen  
* *BAP* = Boekwaarde-afschrijvingspercentage  
* *P* = *DBP*/100  
* *D* = *ND*/360  

De formule voor het berekenen van de afschrijvingsbedragen luidt als volgt:  

*AB* = *BW* x (1 – (1 –P)<sup>D</sup>)

De afschrijvingswaarden zijn:  

| Datum | Berekening |
| --- | --- |
| 06/30/20 |AB = 100.000,00 x (1 -(1 - 0,25)<sup>0,5</sup>) = 13.397,46 |
| 12/31/20 |AB = 86.602,54 x (1 - (1 - 0,25)<sup>0,5</sup>) = 11.602,54 |
| 06/30/21 |AB = 75.000,00 x (1 - (1 - 0,25)<sup>0,5</sup>) = 10.048,09 |
| 12/31/21 |AB = 64.951,91 x (1 - (1 - 0,25)<sup>0,5</sup>) = 8.701,91 |

## <a name="db1sl-depreciation"></a><a name="db1sl-depreciation"></a>BW1/Lineaire afschrijving

BW1/Lin is de afkorting voor deze combinatie van boekwaarde-afschrijving 1 en Lineair. De berekening wordt voortgezet totdat de boekwaarde gelijk is aan het maximale restbedrag na afschrijving of aan de opgegeven restwaarde.  

De batchverwerking **Afschrijving berekenen** berekent een lineair bedrag en een boekwaarde-afschrijvingsbedrag, maar alleen het hoogste bedrag wordt naar het dagboek overgebracht.  

U kunt de boekwaarde-afschrijving met meerdere percentages berekenen.  

Als u deze methode gebruikt, moet u de verwachte gebruiksduur en een boekwaarde-afschrijvingspercentage invullen op de pagina **VA-afschrijvingsboeken**.  

### <a name="example---db1-sl-depreciation"></a><a name="example---db1-sl-depreciation"></a>Voorbeeld - Boekwaarde 1/Lineaire afschrijving

De aanschafkosten van een vast activum bedragen LV 100.000. Op de pagina **VA-afschrijvingsboeken** bevat het veld **Boekwaarde afschr. %** 25, en het veld **Aantal afschr.-jaren** 8. De batchverwerking **Afschrijving berekenen** wordt elk half jaar uitgevoerd.  

De VA-posten zien er als volgt uit:  

| Datum | VA-boekingssoort | Dagen | Bedrag | Boekwaarde |
| --- | --- | --- | --- | --- |
| 01/01/20 |Aanschafkosten |(Begindatum afschrijving) |100,000.00 |100,000.00 |
| 06/30/20 |Afschrijvingen |180 |-12.500,00 |87,500.00 |
| 12/31/20 |Afschrijvingen |180 |-12.500,00 |75,000.00 |
| 06/30/21 |Afschrijvingen |180 |-9.375,00 |65,625.00 |
| 12/31/21 |Afschrijvingen |180 |-9.375,00 |56,250.00 |
| 06/30/22 |Afschrijvingen |180 |-7.031,25 |49,218.75 |
| 12/31/22 |Afschrijvingen |180 |-7.031,25 |42,187.50 |
| 06/30/23 |Afschrijvingen |180 |-5.273,44 |36,914.06 |
| 12/31/23 |Afschrijvingen |180 |-5.273,44 |31,640.62 |
| 06/30/24 |Afschrijvingen |180 |-3.955,08 |27,685.54 |
| 12/31/24 |Afschrijvingen |180 |-3.955,08 |23,730.46 |
| 06/30/25 |Afschrijvingen |180 |-3.955,08 |19.775,38 Lin |
| 12/31/25 |Afschrijvingen |180 |-3.955,08 |15.820,30 Lin |
| 06/30/26 |Afschrijvingen |180 |-3.955,08 |11.865,22 Lin |
| 12/31/26 |Afschrijvingen |180 |-3.955,07 |7.910,15 Lin |
| 06/30/27 |Afschrijvingen |180 |-3.955,08 |3.955,07 Lin |
| 12/31/27 |Afschrijvingen |180 |-3.955,07 |0,00 Lin |

`SL` achter de boekwaarde betekent dat de lineaire afschrijvingsmethode is gebruikt.  

Berekeningsmethode:  

* Jaar 1 (2020):  

    *Boekwaarde-afschrijvingsbedrag: 25% van 100.000 = 25.000 = 12.500 + 12.500*  

    *Lineair afschrijvingsbedrag = 100.000/8 = 12.500 + 6.250 + 6.250*  

    Het boekwaarde-afschrijvingsbedrag wordt gebruikt, omdat dit het hoogste bedrag is.  

* Jaar 5 (2025):  

    *Boekwaarde-afschrijvingsbedrag: 25% van 23,730.46 = 4,943.85 = 2,471.92 + 2,471.92*  

    *Lineair afschrijvingsbedrag = 23.730,46/3 = 7.910,15 = 3.995,07 + 3.995,08*  

    Het lineaire afschrijvingsbedrag wordt gebruikt, omdat dit het hoogste bedrag is.  

## <a name="half-year-convention-depreciation"></a><a name="half-year-convention-depreciation"></a>Afschrijving volgens halfjaarlijkse afspraak

De halfjaarlijkse afspraak wordt alleen toegepast als het veld **Halfjaarlijkse afspraak nemen** op de pagina **VA-afschrijvingsboeken** is ingeschakeld.  

Deze afschrijvingsmethode kan worden gebruikt in samenhang met de volgende afschrijvingsmethoden in de toepassing:  

* Lineair  
* Boekwaarde-afschrijving 1  
* Boekwaarde 1  

Als u de halfjaarlijkse afspraak toepast, heeft een vast activum een afschrijving van zes maanden in het eerste boekjaar, ongeacht de inhoud van het veld **Begindatum afschrijving**.  

> [!NOTE]  
> De verwachte levensduur van een vast activum na het eerste boekjaar, bedraagt altijd een half jaar bij de halfjaarlijkse afspraak. Om de halfjaarlijkse afspraak dus juist toe te passen, moet het veld **Einddatum afschr.** op de pagina **VA-afschrijvingsboek** altijd een datum bevatten die precies zes maanden voor de laatste datum van het boekjaar ligt waarin het vaste activum volledig wordt afgeschreven.  

### <a name="example---half-year-convention-depreciation"></a><a name="example---half-year-convention-depreciation"></a>Voorbeeld - afschrijving volgens halfjaarlijkse afspraak

De aanschafkosten van een vast activum bedragen LV 100.000. De **Begindatum afschr.** is 03-01-20. De verwachte levensduur is vijf jaar, dus de **Einddatum afschr.** moet 06-30-25 zijn. De batchverwerking **Afschrijving berekenen** wordt jaarlijks uitgevoerd. Dit voorbeeld is gebaseerd op een agendaboekjaar.  

De VA-posten zien er als volgt uit:  

| Datum | VA-boekingssoort | Dagen | Bedrag | Boekwaarde |
| --- | --- | --- | --- | --- |
| 03/01/20 |Aanschafkosten |(Begindatum afschrijving) |100,000.00 |100,000.00 |
| 12/31/20 |Afschrijvingen |270 |-10.000,00 |90,000.00 |
| 12/31/21 |Afschrijvingen |360 |-20.000,00 |70,000.00 |
| 12/31/22 |Afschrijvingen |360 |-20.000,00 |50,000.00 |
| 12/31/23 |Afschrijvingen |360 |-20.000,00 |30,000.00 |
| 12/31/24 |Afschrijvingen |360 |-20.000,00 |10,000.00 |
| 12/31/25 |Afschrijvingen |180 |-10.000,00 |0.00 |

## <a name="example---db1sl-depreciation-using-half-year-convention"></a><a name="example---db1sl-depreciation-using-half-year-convention"></a>Voorbeeld - Boekwaarde 1/ lineaire afschrijving met gebruik van halfjaarlijkse afspraak

De aanschafkosten van een vast activum bedragen LV 100.000. De **Begindatum afschr.** is 11-01-20. De verwachte levensduur is vijf jaar, dus de **Einddatum afschr.** moet 06-30-25 zijn. Het veld **Boekwaarde afschr.** op de pagina **Boekwaarde afschr. %** bevat 40. De batchverwerking **Afschrijving berekenen** wordt jaarlijks uitgevoerd. Dit voorbeeld is gebaseerd op een agendaboekjaar.  

De VA-posten zien er als volgt uit:  

| Datum | VA-boekingssoort | Dagen | Bedrag | Boekwaarde |
| --- | --- | --- | --- | --- |
| 11/01/20 |Aanschafkosten |(Begindatum afschrijving) |100,000.00 |100,000.00 |
| 12/31/20 |Afschrijvingen |60 |-20.000,00 |80,000.00 |
| 12/31/21 |Afschrijvingen |360 |-32.000,00 |48,000.00 |
| 12/31/22 |Afschrijvingen |360 |-19.200,00 |28,800.00 |
| 12/31/23 |Afschrijvingen |360 |-11.520,00 |17,280.00 |
| 12/31/24 |Afschrijvingen |360 |-11.520,00 |5.760,00 Lin |
| 12/31/25 |Afschrijvingen |180 |-5.760,00 |0,00 Lin |

`SL` achter de boekwaarde betekent dat de lineaire afschrijvingsmethode is gebruikt.  

Berekeningsmethode:  

* Jaar 1:  

    *Boekwaarde-afschrijvingsbedrag = Volledig jaarbedrag = 40% van 100.000 = 40.000.* Voor een half jaar is dit dus 40.000/2 = 20.000  

    *Lineair bedrag = Volledig jaarbedrag = 100.000/5 = 20.000.* Voor een half jaar is dit dus 20.000/2 = 10.000  

    Het boekwaarde-afschrijvingsbedrag wordt gebruikt omdat dit het hoogste bedrag is.  

* Jaar 5 (2024):  

    *Boekwaarde-afschrijvingsbedrag = 40% van 17.280,00 = 6.912,00*  

    *Lineair afschrijvingsbedrag = 28.800 / 1,5 = 11.520,00*  

    Het lineaire afschrijvingsbedrag wordt gebruikt, omdat dit het hoogste bedrag is.  

## <a name="duplicating-entries-to-more-depreciation-books"></a><a name="duplicating-entries-to-more-depreciation-books"></a>Posten dupliceren naar meer afschrijvingsboeken

Als er drie afschrijvingsboeken zijn, B1, B2 en B3, en u wilt posten uit B1 naar B2 en B3 dupliceren, schakelt u het veld **Deel v. duplicatielijst** in op de kaarten voor de afschrijvingsboeken B2 en B3. Dit kan handig zijn als afschrijvingsboek B1 geïntegreerd is met het grootboek en gebruikmaakt van het financieel dagboek voor vaste activa, en de afschrijvingsboeken B2 en B3 niet geïntegreerd zijn met het grootboek en gebruikmaken van het dagboek voor vaste activa.  

Als u een post boekt in B1 in het financieel dagboek voor vaste activa en het veld **Duplicatielijst gebruiken** inschakelt, wordt de post tijdens het boeken naar B2 en B3 in het dagboek voor vaste activa gedupliceerd.  

> [!NOTE]  
> U kunt niet in hetzelfde dagboek en dezelfde dagboekbatch dupliceren als waar u vanuit dupliceert. Als u posten in het financieel dagboek voor vaste activa boekt, kunt u deze met behulp van een andere batch dupliceren in het dagboek voor vaste activa of in het financieel dagboek voor vaste activa.  

> [!NOTE]  
> U kunt niet dezelfde nummerreeks gebruiken in het financieel dagboek voor vaste activa en het dagboek voor vaste activa. Wanneer u posten in het VA-financieel dagboek boekt, moet u het veld **Documentnr.** leeg laten. Als u een nummer in het veld invoert, wordt het nummer gedupliceerd in het VA-dagboek. U moet het documentnummer handmatig wijzigen voordat u het dagboek kunt boeken.  

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/modules/configure-depreciation-books/)

## <a name="see-also"></a><a name="see-also"></a>Zie ook

[Vaste activa](fa-manage.md)  
[Vaste activa instellen](fa-setup.md)  
[Financiën](finance.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
