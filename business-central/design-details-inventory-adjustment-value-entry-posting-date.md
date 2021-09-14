---
title: Boekingsdatum in waardeposten
description: Leren hoe de batchverwerking Kostprijs herwaarderen - Artikelposten een boekingsdatum bepaalt en toewijst aan de waardeposten die de batchverwerking gaat maken.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 08/19/2021
ms.author: edupont
ms.openlocfilehash: 3dcda7f44797f52e50babe4dbec90e3b2be6f19d
ms.sourcegitcommit: e891484daad25f41c37b269f7ff0b97df9e6dbb0
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 08/27/2021
ms.locfileid: "7440750"
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a>Ontwerpdetails: Boekingsdatum op herwaarderingswaardepost  

Dit artikel begeleidt gebruikers bij de functionaliteit Voorraadwaardering in [!INCLUDE[prod_short](includes/prod_short.md)]. Het specifieke artikel legt uit hoe de batchverwerking **Kostprijs herwaarderen - Artikelposten** een boekingsdatum bepaalt en toewijst aan de waardeposten die de batchverwerking gaat maken.  

Eerst wordt het concept van het proces bekeken, hoe de batchverwerking de boekingsdatum bepaalt en toewijst aan de waardepost die wordt gemaakt. Daarna zijn er enkele gedeelde scenario's die we in het ondersteuningsteam van tijd tot tijd tegenkomen en uiteindelijk is er een lijst met de begrippen die worden gebruikt.  

## <a name="the-concept"></a>Het concept  

De batchverwerking **Kostprijs herwaarderen - Artikelposten** wijst een boekingsdatum toe aan de waardepost die gaat worden gemaakt in de volgende stappen:  

1.  Eerst is de boekingsdatum van de post die wordt gemaakt, hetzelfde als de datum van de post die wordt aangepast.  

2.  De boekingsdatum wordt gevalideerd tegen voorraadperioden en/of boekhoudinstellingen.  

3.  Toewijzing van boekingsdatum; als de oorspronkelijke boekingsdatum niet binnen het toegestane boekingsdatumbereik ligt, wijst de batchverwerking een toegestane boekingsdatum uit Boekhoudinstellingen of Voorraadperiode toe. Als zowel voorraadperioden als toegestane boekingsdatums in grootboekinstellingen zijn gedefinieerd, wordt de latere datum van de twee toegewezen aan de herwaarderingswaardepost.  

 Laten we dit proces eens in de praktijk bekijken. Stel dat we een artikelpost Verkoop hebben. Het artikel is verzonden op 5 september 2020 en de dag erna gefactureerd.  


**Artikelpost**  
Datumnotatie JJJJ-MM-DD

|Volgnummer  |Artikelnr.  |Boekingsdatum  |Boekingssoort  | Documentnr. |Vestiging  |Aantal  |Tot. werk. kosten  |Geboekt aantal  |Resterend aantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |A         |09-2020-05     |  Verkoop       |102033     |  Blauw       | -1    |    -11     |-1     |    0     |

Hieronder vertegenwoordigt de eerste waardepost (379) de verzending en heeft dezelfde boekingsdatum als de bovenliggende artikelpost.  
  
De tweede artikelpost (381) vertegenwoordigt de factuur.  

De derde waardepost (391) is een herwaardering van de factuurwaardepost (381).  
  

|Volgnummer  |Artikelnr.  |Boekingsdatum  |Artikelpostsoort  |Boekingssoort  |Documentnr.  |Artikelpostnr.  |Vestiging  |Aantal op artikelpost  |Geboekt aantal  |Tot. werk. kosten  |Tot. verw. kosten  |Herwaardering  |Vereffenen met post  |Broncode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|--------|---------|---------|---------|---------|
|379     |  A       |    09-2020-05     |    Verkoop     | Directe kosten   | 102033        |319     | Blauw        | -1       |0         |  0       |     -10   |Nee   |0    |Verkoop          |
|381     |  A       |    09-2020-06     |    Verkoop     | Directe kosten   | 103022        |319     | Blauw        |  0       |-1        |-10       |    10     | Nee  |0      |       Verkoop   |
|391     |  A       |    09-2020-10     |    Verkoop     | Directe kosten   | 103022        |319     | Blauw        |  0       |0         |-1        |    0     |Ja   |    181   | VRDWAARDNG   |

De boekingsdatum van de correctiepost is in eerste instantie ingesteld op de boekingsdatum van de post die ermee wordt gecorrigeerd.

 Stap 1: De te maken herwaarderingspost krijgt dezelfde boekingsdatum toegewezen als de post die ermee wordt geherwaardeerd, hierboven geïllustreerd door waardepost 391.  
  
 Stap 2: Validatie van in eerste instantie toegewezen boekingsdatum.  

De batchverwerking **Kostprijs herwaarderen - Artikelposten** bepaalt of de oorspronkelijke boekingsdatum van de herwaarderingswaardepost binnen het toegestane boekingsdatumbereik ligt, op basis van voorraadperioden en/of boekhoudinstellingen.  

Laten we de hierboven genoemde Verkoop bekijken door instelling van toegestane boekingsdatumbereiken toe te voegen.  
  
**Voorraadperioden**

|Einddatum  |Name  |Gesloten  |
|---------|---------|---------|
|01-2020-31     |2020 januari      |  Ja    |
|02-2020-28     |Februari 2020     |  Ja    |
|03-2020-31     |Maart 2020        |  Ja    |
|04-2020-30     |April 2020        |  Ja    |
|05-2020-31     |Mei   2020        |  Ja    |
|06-2020-30     |Juni   2020       |  Ja    |
|07-2020-31     |Juli  2020        |   Ja   |
|08-2020-31     |Augustus  2020     |   Ja   |
|09-2020-30     |September   2020  |         |
|10-2020-31     |Oktober   2020    |         |
|11-2020-30     |November   2020   |         |
|12-2020-31     |December   2020   |         |

De eerste toegestane boekingsdatum is de eerste dag van de eerste open periode. 1 september 2020.  

**Grootboekinstellingen**

|Veld|Waarde  |
|---------|---------|
|Boeken toegest. vanaf:  |  09-2020-10      |
|Boeken toegest. tot:    |  09-2020-30      |
|Registratietijd:       |         |
|Lokale adresnotatie:|   Postcode      |  

 De eerste toegestane boekingsdatum is de datum in het veld Boeken toegest. vanaf: 10 september 2020.  
 Als zowel voorraadperioden als toegestane boekingsdatums in grootboekinstellingen zijn gedefinieerd, definieert de latere datum van de twee het toegestane boekingsdatumbereik.  

 Stap 3: Toewijzing van een toegestane boekingsdatum;  

 De aanvankelijke toegewezen Boekingsdatum was 6 september, zoals in stap 1 wordt beschreven. Echter, in de tweede stap identificeert de batchverwerking Kostprijs herwaarderen - Artikelposten dat de vroegste toegestane boekingsdatum 10 september is en wijst dus 10 september toe aan de herwaarderingswaardepost, onder.  

   
|Volgnummer  |Artikelnr.  |Boekingsdatum  |Artikelpostsoort  |Boekingssoort  |Documentnr.  |Artikelpostnr.  |Vestiging  |Aantal op artikelpost  |Geboekt aantal  |Tot. werk. kosten  |Tot. verw. kosten  |Herwaardering  |Vereffenen met post  |Broncode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|379     |  A       |    09-2020-05     |    Verkoop     | Directe kosten   | 102033        |319     | Blauw        | -1       |0         |  0       |     -10   |Nee   |0    |Verkoop          |
|381     |  A       |    09-2020-06     |    Verkoop     | Directe kosten   | 103022        |319     | Blauw        |  0       |-1        |-10       |    10     | Nee  |0      |       Verkoop   |
|391     |  A       |    **2020-09-10**     |    Verkoop     | Directe kosten   | 103022        |319     | Blauw        |  0       |0         |-1        |    0     |Ja   |    181   | VRDWAARDNG   |

 We hebben nu het concept bekeken voor het toewijzen van Boekingsdatums aan waardeposten die worden gemaakt door de batchverwerking Kostprijs herwaarderen - Artikelposten.  

 Laten we enkele scenario's bekijken die we in het ondersteuningsteam van tijd tot tijd tegenkomen in verband met toegewezen boekingsdatums in de batchverwerking Kostprijs herwaarderen - Artikelposten en gerelateerde instellingen.  

## <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Scenario I: "De boekingsdatum ligt niet binnen het bereik van toegestane boekingsdatums."  

 Dit is een scenario waarin een gebruiker het genoemde foutbericht krijgt wanneer de batchverwerking Kostprijs herwaarderen - Artikelposten wordt uitgevoerd.  

 In de vorige sectie, waar het concept van het toewijzen van boekingsdatums wordt besproken, is het de bedoeling van de batchverwerking Kostprijs herwaarderen - Artikelposten een waardepost te maken met de boekingsdatum 10 september.  

![Foutbericht over boekingsdatum.](media/helene/TechArticleAdjustcost6.png "Foutbericht over boekingsdatum")

 We gaan door op de gebruikersinstelling:  

**Gebruikersinstellingen**  

Sorteren: gebruikers-id  

|Gebruikers-ID  |Boeken toegest. vanaf  | Boeken toegest. tot  |
|---------|---------|--------|
|EUROPA  |  09-2020-11      |09-2020-30      |

 De gebruiker heeft in dit geval een toegestane boekingsdatumreeks van 11 september tot 30 september en mag daardoor de herwaarderingswaardepost niet boeken met boekingsdatum 10 september.  

### <a name="overview-of-involved-posting-date-setup"></a>Overzicht van betrokken instelling van boekingsdatum:

**Voorraadperioden**  

|Einddatum  |Name  |Gesloten  |
|---------|---------|---------|
|01-2020-31     |2020 januari      |  Ja    |
|02-2020-28     |Februari 2020     |  Ja    |
|03-2020-31     |Maart 2020        |  Ja    |
|04-2020-30     |April 2020        |  Ja    |
|05-2020-31     |Mei   2020        |  Ja    |
|06-2020-30     |Juni   2020       |  Ja    |
|07-2020-31     |Juli  2020        |   Ja   |
|08-2020-31     |Augustus  2020     |   Ja   |
|09-2020-30     |September   2020  |         |
|10-2020-31     |Oktober   2020    |         |
|11-2020-30     |November   2020   |         |
|12-2020-31     |December   2020   |         |  

**Grootboekinstellingen**  

|Veld|Waarde|
|---------|---------|
|Boeken toegest. vanaf:  |  09-2020-10      |
|Boeken toegest. tot:    |  09-2020-30      |
|Registratietijd:       |         |
|Lokale adresnotatie:|   Postcode      |  

**Gebruikersinstellingen**    

|Gebruikers-ID  |Boeken toegest. vanaf  | Boeken toegest. tot  |
|---------|---------|--------|
|GEBRUIKERSNAAM |  09-2020-10      |09-2020-30      |

 Als aan de gebruiker een ruimer (of identiek) boekingsdatumbereik wordt toegewezen als in de instelling van de voorraadperiode of het grootboek, wordt het genoemde conflict vermeden. De correctiewaardepost met boekingsdatum 10 september wordt met deze instelling succesvol geboekt.

Een ouder Knowledge Base-artikel [952996](https://support.microsoft.com/topic/information-about-inventory-adjustment-posting-dates-in-microsoft-dynamics-nav-99e22b2b-5b79-a9b2-3b43-7f3484fa31d9) bespreekt meer scenario's in verband met het genoemde foutbericht.  

## <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a>Scenario II: Boekingsdatum op Herwaarderingswaardepost versus Boekingsdatum op post die de correctie veroorzaakt, zoals Herwaardering of productie Artikeltoeslag.  

### <a name="revaluation-scenario"></a>Herwaarderingsscenario:  

 Vereisten:  

 Voorraadinstelling:  
me
-   Autom. voorraadwaarde boeken = Ja  

-   Automatische kostenwaardering = Altijd  

-   Gem. kostprijsberekeningsoort = artikel  

-   Periode gemiddelde kostprijsberekening = Dag  

 Grootboekinstellingen:  

-   Boeken toegest. vanaf = 1 januari 2021  

-   Boeken toegest. tot = leeg  

 Gebruikersinstellingen:  

-   Boeken toegest. vanaf = 1 december 2020  

-   Boeken toegest. tot = leeg  

### <a name="to-test-the-scenario"></a>Het scenario testen  

1.  ArtikelTEST maken:  

     Basiseenheid = Stuks  

     Waarderingsmethode = Gemiddelde  

     Selecteer optionele boekingsgroepen.  

2.  Open artikeldagboek, maak en boek een regel als volgt:  

     Boekingsdatum = 15 december 2020  

     Artikel = TEST  

     Boekingssoort = Inkoop  

     Aantal = 100  

     Eenheidsprijs = 10  

3.  Open artikeldagboek, maak en boek een regel als volgt:  

     Datum = 20 december 2020  

     Artikel = TEST  

     Boekingssoort = Negatieve herwaardering  

     Aantal = 2  

4.  Open artikeldagboek, maak en boek een regel als volgt:  

     Datum = 15 januari 2021  

     Artikel = TEST  

     Boekingssoort = Negatieve herwaardering  

     Aantal = 3  

5.  Open herwaarderingsdagboek, maak en boek een regel als volgt:  

     Artikel = TEST  

     Vereffenen met post = selecteer inkooppost die is geboekt in stap 2. De boekingsdatum van de herwaardering is dezelfde als van de post die wordt aangepast.  

     Kostprijs (Geherwaardeerd) = 40  

De volgende **artikelposten** en **waardeposten** zijn geboekt:  

**Artikelpost - inkoop**:  
Datumnotatie JJJJ-MM-DD  

|Volgnummer  |Artikelnr.  |Boekingsdatum  |Boekingssoort  |Documentnr.  |Aantal  |Tot. werk. kosten  |Resterend aantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|317     |TEST         |12-2020-15         |Inkoop         |T00001         |100         |4000         |95        |

**Waardeposten**  

|Volgnummer  |Artikelnr.  |Boekingsdatum  |Artikelpostnr.  |Artikelpostsoort  |Boekingssoort  |Documentnr.  |Aantal op artikelnummerpost  |Tot. werk. kosten  |Kosten geboekt naar grootboek  |Herwaardering  |Wordt vereffend met post  |Broncode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|376     |TEST|   12-2020-15    |317         |Inkoop         |Directe kosten         |T00001         |100         |1 000,00          |1 000,00    |Nee         |0         |ITEMNL         |
|379     |TEST   |**2020-12-15**    |317         |Inkoop         |Herwaardering         |T04002         |0         |3 000,00         |3 000,00         |Nee         |0         |REVALINL         |

**Artikelpost - negatieve correctie, stap 3**  

|Volgnummer  |Artikelnr.  |Boekingsdatum  |Boekingssoort  |Documentnr.  |Aantal  |Tot. werk. kosten  |Resterend aantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|318     |TEST      |12-2020-20   |Negatieve correctie  |T00002         |-2         |-80         | 0        |

**Waardeposten**  

|Volgnummer  |Artikelnr.  |Boekingsdatum  |Artikelpostnr.  |Artikelpostsoort  |Boekingssoort  |Documentnr.  |Aantal op artikelnummerpost  |Tot. werk. kosten  |Kosten geboekt naar grootboek  |Herwaardering  |Wordt vereffend met post  |Broncode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|377     |TEST|   12-2020-20    |318         |Negatieve correctie         |Directe kosten         |T00002         |-2         |-20          |-20    |Nee         |0         |ITEMNL         |
|380     |TEST   |**2021-01-01**    |318         |Negatieve correctie         |Directe kosten         |T04002         |0         |-60         |-60         |Ja         |377         |VRDWAARDNG         |

**Artikelpost - negatieve correctie, stap 4**  

|Volgnummer  |Artikelnr.  |Boekingsdatum  |Boekingssoort  |Documentnr.  |Aantal  |Tot. werk. kosten  |Resterend aantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |TEST      |01-2021-15   |Negatieve correctie  |T00003         |-3         |-120         | 0        |

**Waardeposten**  

|Volgnummer  |Artikelnr.  |Boekingsdatum  |Artikelpostnr.  |Artikelpostsoort  |Boekingssoort  |Documentnr.  |Aantal op artikelnummerpost  |Tot. werk. kosten  |Kosten geboekt naar grootboek  |Herwaardering  |Wordt vereffend met post  |Broncode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|378     |TEST|   01-2021-15    |319         |Negatieve correctie         |Directe kosten         |T00003         |-3         |-30          |-30    |Nee         |0         |ITEMNL         |
|381     |TEST   |**2021-01-15**    |319         |Negatieve correctie         |Directe kosten         |T04003         |0         |-90         |-90         |Ja         |378         |VRDWAARDNG         |

De batchverwerking Kostprijs herwaarderen - Artikelposten heeft een wijziging in kosten herkend en de negatieve herwaarderingen aangepast.  

**Controle van boekingsdatums in gemaakte correctiewaardeposten:** de vroegste toegestane boekingsdatum waarop de batchverwerking Kostprijs herwaarderen - Artikelposten betrekking moet hebben is 1 januari 2021, zoals gesteld in de grootboekinstellingen.  

**Negatieve herwaardering in stap 3:** toegewezen boekingsdatum is 1 januari, bepaald door boekhoudinstellingen. De boekingsdatum van de waardepost in het bereik voor herwaardering is 20 december 2020. Volgens de boekhoudinstellingen ligt de datum niet binnen het toegestane boekingsdatumbereik. Daarom wordt de boekingsdatum in het veld Boeken toegest. vanaf in de boekhoudinstellingen toegewezen aan de herwaarderingswaardepost.  

**Negatieve herwaardering in stap 4:** toegewezen boekingsdatum is 15 januari. De waardepost in het bereik van herwaardering heeft boekingsdatum 15 januari, wat ligt binnen het toegestane boekingsdatumbereik, volgens de boekhoudinstellingen.  

De herwaardering die wordt aangebracht voor de Negatieve herwaardering in stap 3 leidt tot discussie. De gunstige boekingsdatum voor de herwaarderingswaardepost zou 20 december zijn of ten minste in december liggen aangezien de herwaardering die de wijziging in KPV heeft veroorzaakt, is geboekt in december.  

Om herwaardering in december te bereiken van de negatieve correctie in stap 3, moet het veld Boeken toegest. vanaf in de boekhoudinstellingen een datum in december bevatten.  

**Conclusie:**  

Overweeg met de ervaringen uit dit scenario de geschiktste instelling van toegestane boekingsdatumbereik voor een bedrijf. U kunt rekening houden met de volgende informatie: zo lang u toestaat dat wijzigingen in voorraadwaarde in een periode worden geboekt, december in dit geval, moet de instelling die het bedrijf gebruikt voor toegestane boekingsdatumbereiken, overeenstemmen met deze beslissing. Het veld Boeken toegest. in de boekhoudinstellingen, dat 1 december bevat, zou toestaan dat de herwaardering die in december is aangebracht, wordt doorgestuurd naar betrokken uitgaande posten in dezelfde periode.  

Gebruikersgroepen die niet in december mogen boeken, maar in januari, een beperking die waarschijnlijk de bedoeling was van de boekhoudinstellingen in dit scenario, moeten in plaats daarvan worden geregeld met de gebruikersinstellingen.  

### <a name="item-charge-scenario"></a>Artikeltoeslagscenario:  

 Vereisten:  

 Voorraadinstelling:  

-   Autom. voorraadwaarde boeken = Ja  

-   Automatische kostenwaardering = Altijd  

-   Gem. kostprijsberekeningsoort = artikel  

-   Periode gemiddelde kostprijsberekening = Dag  

 Grootboekinstellingen:  

-   Boeken toegest. vanaf = 1 december 2020.  

-   Boeken toegest. tot = leeg  

 Gebruikersinstellingen:  

-   Boeken toegest. vanaf = 1 december 2020.  

-   Boeken toegest. tot = leeg  


### <a name="to-test-the-scenario"></a>Het scenario testen  

1.  Artikeltoeslag maken:  

     Basiseenheid = Stuks  

     Waarderingsmethode = Gemiddelde  

     Selecteer optionele boekingsgroepen.  

2.  Nieuwe inkooporder maken  

     Orderleveranciersnr.: 10000  

     Boekingsdatum = 15 december 2020

     Leveranciersfactuurnr.: 1234  

     Op de inkooporderregel:  

     Artikel = TOESLAG  

     Aantal = 1  

     Directe kostprijs = 100  

     Ontvangst en factuur boeken.  

3.  Nieuwe verkooporder maken:  

     Orderklantnr.: 10000  

     Boekingsdatum = 16 december 2020  

     Op de verkooporderregel:  

     Artikel = TOESLAG  

     Aantal = 1  

     Eenheidsprijs - 135  

     Verzenden en factureren boeken.  

4.  Grootboekinstellingen:  

     Boeken toegest. vanaf = 1 januari 2021  

     Boeken toegest. tot = leeg  

5.  Nieuwe inkooporder maken:  

     Leveranciersnr.: 10000  

     Boekingsdatum = 2 januari 2021  

     Leveranciersfactuurnr.: 2345  

     Op de inkooporderregel:  

     Artikeltoeslag = JB-VRACHT  

     Aantal = 1  

     Directe kostprijs = 3  

     Wijs artikeltoeslag toe aan inkoopontvangst uit stap 2.  

     Ontvangst en factuur boeken.  


**Statusartikelpost van inkoop stap 2**:  
  
|Volgnummer  |Artikelnr.  |Boekingsdatum  |Boekingssoort  |Documentnr.  |Aantal  |Tot. werk. kosten  |Resterend aantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |TOESLAG         |12-2020-15         |Inkoop         |107030         |1         |105         |0        |

**Waardeposten**  

|Volgnummer |Artikelnr.  |Boekingsdatum  |Artikelpostnr.  |Artikelpostsoort  |Boekingssoort  |Documentnr.  | Artikeltoeslagnr.    |  Aantal op artikelpost   |Tot. werk. kosten     |Kosten geboekt naar grootboek |Herwaardering |Vereffenen met post |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |TOESLAG|   12-2020-15    |324         |Inkoop         |Directe kosten         |108029         |         |1          |100    |100         |NEE         |0         |
|399      |TOESLAG   |01-2021-02    |324         |Inkoop         |Directe kosten         |108009         |JB-VRACHT         |0         |3         |3         |NEE         |0         |


**Statusartikelpost verkoop**:  
  
|Volgnummer  |Artikelnr.  |Boekingsdatum  |Boekingssoort  |Documentnr.  |Aantal  |Tot. werk. kosten  |Resterend aantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |TOESLAG         |12-2020-16         |Verkoop         |102035         |-1         |-105         |0        |

**Waardeposten**  

|Volgnummer |Artikelnr.  |Boekingsdatum  |Artikelpostnr.  |Artikelpostsoort  |Boekingssoort  |Documentnr.  | Artikeltoeslagnr.    |  Aantal op artikelpost   |Tot. werk. kosten     |Kosten geboekt naar grootboek |Herwaardering |Vereffenen met post |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |TOESLAG|   12-2020-16    |325         |Verkoop         |Directe kosten         |109024         |         |-1          |-100    |-100         |NEE         |0         |
|400      |TOESLAG   |01-2021-01    |325         |Verkoop         |Directe kosten         |109024         |         |0         |-3         |-3         |Ja         |398         |


6.  Op werkdatum 3 januari arriveert een inkoopfactuur met een aanvullende artikeltoeslag bovenop de inkoop die in stap 2 is gedaan. Deze factuur heeft documentdatum 30 december en is dus geboekt met boekingsdatum 30 december 2020.  

     Nieuwe inkooporder maken:  

     Leveranciersnr.: 10000  

     Boekingsdatum = 30 december 2020  

     Leveranciersfactuurnr.: 3456  

     Op de inkooporderregel:  

     Artikeltoeslag = JB-VRACHT  

     Aantal = 1  

     Directe kostprijs = 2  

     Wijs artikeltoeslag toe aan inkoopontvangst uit stap 2  

     Ontvangst en factuur boeken.  


**Statusartikelpost van inkoop**:  

|Volgnummer  |Artikelnr.  |Boekingsdatum  |Boekingssoort  |Documentnr.  |Aantal  |Tot. werk. kosten  |Resterend aantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |TOESLAG         |12-2020-15         |Inkoop         |107030         |1         |105         |0        |

**Waardeposten**  

|Volgnummer |Artikelnr.  |Boekingsdatum  |Artikelpostnr.  |Artikelpostsoort  |Boekingssoort  |Documentnr.  | Artikeltoeslagnr.    |  Aantal op artikelpost   |Tot. werk. kosten     |Kosten geboekt naar grootboek |Herwaardering |Vereffenen met post |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |TOESLAG   |12-2020-15    |324         |Inkoop         |Directe kosten         |108029         |            |1         |100    |100         |Nee         |0         |
|399      |TOESLAG   |01-2021-02    |324         |Inkoop         |Directe kosten         |108030         |JB-VRACHT   |0         |3         |3         |Nee         |0         |
|401      |TOESLAG   |**2020-12-30**    |324         |Inkoop         |Directe kosten         |108031         |JB-VRACHT   |0         |2         |2         |Nee         |0         |

**Statusartikelpost verkoop**:  
  
|Volgnummer  |Artikelnr.  |Boekingsdatum  |Boekingssoort  |Documentnr.  |Aantal  |Tot. werk. kosten  |Resterend aantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |TOESLAG         |12-2020-16         |Verkoop         |102035         |-1         |-105         |0        |

**Waardeposten**  

|Volgnummer |Artikelnr.  |Boekingsdatum  |Artikelpostnr.  |Artikelpostsoort  |Boekingssoort  |Documentnr.  | Artikeltoeslagnr.    |  Aantal op artikelpost   |Tot. werk. kosten     |Kosten geboekt naar grootboek |Herwaardering |Vereffenen met post |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |TOESLAG   |12-2020-16        |325         |Verkoop         |Directe kosten         |103024         |            |-1         |-100       |-100         |Nee         |0         |
|400      |TOESLAG   |01-2021-01        |325         |Verkoop         |Directe kosten         |103024         |            |0          |-3         |-3         |Ja         |398         |
|402      |TOESLAG   |**2021-01-01**    |325         |Verkoop         |Directe kosten         |103024         |            |0          |-2         |-2         |Ja         |398         |

Het rapport Voorraadwaardering wordt afgedrukt vanaf 31 december 2020

![Inhoud van het voorraadwaarderingsrapport.](media/helene/TechArticleAdjustcost13.png "Inhoud van het voorraadwaarderingsrapport")

 **Overzicht van scenario:**  

 Het beschreven scenario eindigt met een rapport Voorraadwaardering dat Aantal = 0 aangeeft terwijl de waarde = 2. De artikeltoeslag die in stap 11 is geboekt, maakt deel uit van de positieve voorraadmutatiewaarde van december terwijl de negatieve voorraadmutatie van dezelfde periode niet wordt beïnvloed.  

 Dat de boekhoudinstellingen Boeken toegest. vanaf 1 januari aangeven, was goed voor de eerste artikeltoeslag. De kosten van de positieve en de negatieve voorraadmutatie zijn in dezelfde periode vastgelegd. Voor de tweede artikeltoeslag leiden de boekhoudinstellingen er echter toe dat de wijziging in COGS in de volgende periode wordt herkend.  

 **Conclusie:**  

 Het is een uitdaging om het rapport Voorraadwaardering Aantal = 0 aan te laten geven terwijl de Waarde <> 0. In dat geval is het ook moeilijker de optimale instellingen aan te geven, wanneer inkoopfacturen op dezelfde dag arriveren, maar verschillende perioden of zelfs boekjaren betreffen. De overgang naar een nieuw boekjaar vereist meestal enige planning en als onderdeel daarvan moet het proces Kostprijs herwaarderen - Artikelposten, rekening houdend met COGS, worden overwogen.  

 In dit scenario zou één scenario kunnen zijn het veld Boekhoudinstellingen, Boeken toegest. vanaf voor enkele dagen een datum in december te geven en de boeking van de eerste artikeltoeslag uit te stellen om mogelijk te maken dat alle kosten voor de vorige periode/boekjaar eerst worden herkend voor de periode waartoe ze behoren, de batchverwerking Kosten herwaarderen - Artikelposten uit te voeren en daarna de toegestane boekingsdatum te verplaatsen naar de nieuwe periode\/boekjaar. De eerste artikeltoeslag met boekingsdatum 2 januari kan dan worden geboekt.  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a>Historie van batchverwerking Kostprijs herwaarderen - Artikelposten  

 Hieronder vindt u een overzicht van het concept boekingsdatums toewijzen aan herwaarderingswaardeposten door de batchverwerking Kostprijs herwaarderen - Artikelposten.  

### <a name="about-the-request-form-posting-date"></a>Over de boekingsdatum van het aanvraagformulier:  

 Er hoeft geen boekingsdatum meer te worden vermeld in het aanvraagformulier van de batchverwerking Kostprijs herwaarderen - Artikelposten. De batchverwerking doorloopt alle benodigde wijzigingen en maakt waardeposten met de boekingsdatum van de waardepost die wordt geherwaardeerd. Als de boekingsdatum niet binnen het toegestane boekingsdatumbereik ligt, wordt de boekingsdatum in het veld Boeken toegest. vanaf in de boekhoudinstellingen gebruikt, OF als de voorraadperioden worden gebruikt, wordt de laatste datum van de twee gebruikt. Zie hierboven beschreven concept.  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a>Historie van batchverwerking Voorraadwaarde boeken.  

 De batchverwerking Voorraadwaarde boeken is nauw verbonden met de batchverwerking Kostprijs herwaarderen - Artikelposten. Daarom wordt de historie van deze batchverwerking hier ook samengevat en gedeeld.  
 
![Werkelijke kosten versus verwachte kosten.](media/helene/TechArticleAdjustcost14.png "Werkelijke kosten versus verwachte kosten")

### <a name="about-the-posting-date"></a>Over de boekingsdatum  

 Er hoeft geen boekingsdatum meer te worden vermeld in het aanvraagformulier van de batchverwerking Voorraadwaarde boeken. De grootboekpost wordt gemaakt met dezelfde boekingsdatum als de gerelateerde waardepost. Als u de batchverwerking wilt voltooien, moet het toegestane boekingsdatumbereik de boekingsdatum van de gemaakte grootboekpost toestaan. Als dit niet het geval is, moet de toegestane boekingsdatumreeks tijdelijk opnieuw worden geopend door de datums in het veld Boeken toegest. vanaf en tot in Boekhoudinstellingen te wijzigen of te verwijderen. Om reconciliatieproblemen te voorkomen is het vereist dat de boekingsdatum van de grootboekpost correspondeert met de boekingsdatum van de waardepost.  

 De batchverwerking scant tabel 5811 - Waardepost naar GB boeken om de waardeposten te bepalen in het bereik voor boeking naar het grootboek. Na een succesvolle uitvoering wordt de tabel geleegd.

## <a name="see-also"></a>Zie ook  

[Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md)  
[Ontwerpdetails: Artikelvereffening](design-details-item-application.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
