---
title: Boekingsdatum op correctiewaardepost in vergelijking met de bronpost
description: 'Lees meer over het scenario "Boekingsdatum op Herwaarderingswaardepost versus Boekingsdatum op post die de correctie veroorzaakt, zoals Herwaardering of Artikeltoeslag." bij het uitvoeren van de batchverwerking Kostprijs herwaarderen - Artikelposten.'
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: edupont
---

# <a name="posting-date-on-adjustment-value-entry-compared-to-the-source-entry"></a><a name="posting-date-on-adjustment-value-entry-compared-to-the-source-entry"></a>Boekingsdatum op correctiewaardepost in vergelijking met de bronpost

In dit artikel wordt Boekingsdatum op Herwaarderingswaardepost vergeleken met Boekingsdatum op post die de uitvoering veroorzaakt van de batchverwerking Kostprijs herwaarderen - Artikelposten, met name een herwaarderingsscenario en een artikeltoeslagscenario.

De batchverwerking **Kostprijs herwaarderen - Artikelposten** verwerkt uw gegevens afhankelijk van uw scenario en configuratie van [!INCLUDE[prod_short](includes/prod_short.md)]. In deze sectie beschrijven we twee afzonderlijke processen, en voor elk proces tonen we het type impact dat de batchverwerking Kostprijs herwaarderen - Artikelposten heeft op de gegevens.

## <a name="revaluation-scenario"></a><a name="revaluation-scenario"></a>Herwaarderingsscenario

### <a name="prerequisites"></a><a name="prerequisites"></a>Vereisten

Voer de volgende waarden in:

**Voorraadinstellingen**:  

- Autom. voorraadwaarde boeken = Ja  

- Automatische kostenwaardering = Altijd  

- Gem. kostprijsberekeningsoort = Artikel  

- Periode gemiddelde kostprijsberekening = Dag  

**Grootboekinstellingen**:  

- Boeken toegest. vanaf = 1 januari 2021  

- Boeken toegest. tot = leeg  

**Gebruikersinstellingen**:  

- Boeken toegest. vanaf = 1 december 2020  

- Boeken toegest. tot = leeg  

### <a name="to-test-the-scenario"></a><a name="to-test-the-scenario"></a>Het scenario testen

Test dit scenario door de volgende stappen uit te voeren.

1. Maak een **artikel** genaamd TEST met de volgende waarden:  

     - Basiseenheid = Stuks  

     - Waarderingsmethode = Gemiddelde  

     - Selecteer optionele boekingsgroepen.  

2. Open een **artikeldagboek**, maak en boek een nieuwe post als volgt:  

     - Boekingsdatum = 15 december 2020  

     - Artikel = TEST  

     - Boekingssoort = Inkoop  

     - Aantal = 100  

     - Eenheidsprijs = 10  

3. Open een **artikeldagboek**, maak en boek een nieuwe post als volgt:  

     - Datum = 20 december 2020  

     - Artikel = TEST  

     - Boekingssoort = Negatieve herwaardering  

     - Aantal = 2  

4. Open een **artikeldagboek**, maak en boek een nieuwe post als volgt:  

     - Datum = 15 januari 2021  

     - Artikel = TEST  

     - Boekingssoort = Negatieve herwaardering  

     - Aantal = 3  

5. Open een **artikelherwaarderingsdagboek**, maak en boek een nieuwe post als volgt:  

     - Artikel = TEST  

     - Vereffenen met post = selecteer inkooppost die is geboekt in stap 2. De boekingsdatum van de herwaardering is dezelfde als van de post die wordt aangepast.  

     - Kostprijs (Geherwaardeerd) = 40  

De volgende **artikelposten** en **waardeposten** zijn geboekt:  

**Artikelpost - inkoop**:  

|Volgnummer  |Artikelnr.  |Boekingsdatum  |Boekingssoort  |Documentnr.  |Aantal  |Tot. werk. kosten  |Resterend aantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|317     |TEST         |2020-12-15         |Inkoop         |T00001         |100         |4000         |95        |

**Waardeposten**  

|Volgnummer  |Artikelnr.  |Boekingsdatum  |Artikelpostnr.  |Artikelpostsoort  |Boekingssoort  |Documentnr.  |Aantal op artikelnummerpost  |Tot. werk. kosten  |Kosten geboekt naar grootboek  |Herwaardering  |Wordt vereffend met post  |Broncode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|376     |TEST|   2020-12-15    |317         |Inkoop         |Directe kosten         |T00001         |100         |1 000,00          |1 000,00    |Nee         |0         |ITEMNL         |
|379     |TEST   |**2020-12-15**    |317         |Inkoop         |Herwaardering         |T04002         |0         |3 000,00         |3 000,00         |Nee         |0         |REVALINL         |

**Artikelpost - negatieve correctie, stap 3**  

|Volgnummer  |Artikelnr.  |Boekingsdatum  |Boekingssoort  |Documentnr.  |Aantal  |Tot. werk. kosten  |Resterend aantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|318     |TEST      |2020-12-20   |Negatieve correctie  |T00002         |-2         |-80         | 0        |

**Waardeposten**  

|Volgnummer  |Artikelnr.  |Boekingsdatum  |Artikelpostnr.  |Artikelpostsoort  |Boekingssoort  |Documentnr.  |Aantal op artikelnummerpost  |Tot. werk. kosten  |Kosten geboekt naar grootboek  |Herwaardering  |Wordt vereffend met post  |Broncode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|377     |TEST|   12-2020-20    |318         |Negatieve correctie         |Directe kosten         |T00002         |-2         |-20          |-20    |Nee         |0         |ITEMNL         |
|380     |TEST   |**2021-01-01**    |318         |Negatieve correctie         |Directe kosten         |T04002         |0         |-60         |-60         |Ja         |377         |VRDWAARDNG         |

**Artikelpost - negatieve correctie, stap 4**  

|Volgnummer  |Artikelnr.  |Boekingsdatum  |Boekingssoort  |Documentnr.  |Aantal  |Tot. werk. kosten  |Resterend aantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |TEST      |2021-01-15   |Negatieve correctie  |T00003         |-3         |-120         | 0        |

**Waardeposten**  

|Volgnummer  |Artikelnr.  |Boekingsdatum  |Artikelpostnr.  |Artikelpostsoort  |Boekingssoort  |Documentnr.  |Aantal op artikelnummerpost  |Tot. werk. kosten  |Kosten geboekt naar grootboek  |Herwaardering  |Wordt vereffend met post  |Broncode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|378     |TEST|   2021-01-15    |319         |Negatieve correctie         |Directe kosten         |T00003         |-3         |-30          |-30    |Nee         |0         |ITEMNL         |
|381     |TEST   |**2021-01-15**    |319         |Negatieve correctie         |Directe kosten         |T04003         |0         |-90         |-90         |Ja         |378         |VRDWAARDNG         |

De batchverwerking **Kostprijs herwaarderen - Artikelposten** heeft een wijziging in kosten herkend en de negatieve herwaarderingen aangepast.  

**Controle van boekingsdatums in gemaakte correctiewaardeposten:** de vroegste toegestane boekingsdatum waarop de batchverwerking Kostprijs herwaarderen - Artikelposten betrekking moet hebben is 1 januari 2021, zoals gesteld in de grootboekinstellingen.  

**Negatieve herwaardering in stap 3:** toegewezen boekingsdatum is 1 januari, bepaald door boekhoudinstellingen. De boekingsdatum van de waardepost in het bereik voor herwaardering is 20 december 2020. Volgens de boekhoudinstellingen ligt de datum niet binnen het toegestane boekingsdatumbereik. Daarom wordt de boekingsdatum in het veld Boeken toegest. vanaf in de boekhoudinstellingen toegewezen aan de herwaarderingswaardepost.  

**Negatieve herwaardering in stap 4:** toegewezen boekingsdatum is 15 januari. De waardepost in het bereik van herwaardering heeft boekingsdatum 15 januari, wat ligt binnen het toegestane boekingsdatumbereik, volgens de boekhoudinstellingen.  

De herwaardering die wordt aangebracht voor de Negatieve herwaardering in stap 3 leidt tot discussie. De gunstige boekingsdatum voor de herwaarderingswaardepost zou 20 december zijn of ten minste in december liggen aangezien de herwaardering die de wijziging in KPV heeft veroorzaakt, is geboekt in december.  

Om herwaardering in december te bereiken van de negatieve correctie in stap 3, moet het veld Boeken toegest. vanaf in de boekhoudinstellingen een datum in december bevatten.  

### <a name="conclusion"></a><a name="conclusion"></a>Conclusie

Met de ervaring die in dit scenario is opgedaan, kunt u bij het overwegen van de meest geschikte instelling voor een toegestane boekingsperiode voor een bedrijf rekening houden met het volgende. Zolang u toestaat dat wijzigingen in de voorraadwaarde worden geboekt in een periode, zoals in dit geval december, moet de instelling die het bedrijf gebruikt voor toegestane boekingsdatumbereiken worden afgestemd op deze beslissing. Het veld Boeken toegest. in de boekhoudinstellingen, dat 1 december bevat, zou toestaan dat de herwaardering die in december is aangebracht, wordt doorgestuurd naar betrokken uitgaande posten in dezelfde periode.  

Gebruikersgroepen die niet in december mogen boeken, maar in januari, een beperking die waarschijnlijk de bedoeling was van de boekhoudinstellingen in dit scenario, moeten in plaats daarvan worden geregeld met de gebruikersinstellingen.  

## <a name="item-charge-scenario"></a><a name="item-charge-scenario"></a>Artikeltoeslagscenario

### <a name="prerequisites-1"></a><a name="prerequisites-1"></a>Vereisten

Voer de volgende waarden in:

**Voorraadinstellingen**:  

- Autom. voorraadwaarde boeken = Ja  

- Automatische kostenwaardering = Altijd  

- Gem. kostprijsberekeningsoort = Artikel  

- Periode gemiddelde kostprijsberekening = Dag  

**Grootboekinstellingen**:  

- Boeken toegest. vanaf = 1 december 2020.  

- Boeken toegest. tot = leeg  

**Gebruikersinstellingen**:  

- Boeken toegest. vanaf = 1 december 2020.  

- Boeken toegest. tot = leeg  

### <a name="to-test-the-scenario-1"></a><a name="to-test-the-scenario-1"></a>Het scenario testen

Test dit scenario door de volgende stappen uit te voeren:

1.  Maak een **artikel**toeslag genaamd TEST met de volgende waarden:  

     - Basiseenheid = Stuks  

     - Waarderingsmethode = Gemiddelde  

     - Selecteer optionele boekingsgroepen.  

2.  Maak een nieuwe **Inkooporder** met de volgende waarden:  

     - Leveranciersnr.: 10000  

     - Boekingsdatum = 15 december 2020

     - Leveranciersfactuurnr.: 1234  

     Selecteer op de inkooporderregel de volgende waarden:  

     - Artikel = TOESLAG  

     - Aantal = 1  

     - Directe kostprijs = 100  

     Om de stap te voltooien, boekt u het document als ontvangen en gefactureerd.  

3.  Maak een nieuwe **Verkooporder** met de volgende waarden:  

     - Orderklantnr.: 10000  

     - Boekingsdatum = 16 december 2020  

     Op de verkooporderregel:  

     - Artikel = TOESLAG  

     - Aantal = 1  

     - Eenheidsprijs - 135  

     Om de stap te voltooien, boekt u het document als ontvangen en gefactureerd.  

4.  Voer waarden in voor de pagina **Grootboekinstellingen**:  

     - Boeken toegest. vanaf = 1 januari 2021  

    -  Boeken toegest. tot = leeg  

5.  Maak een nieuwe **Inkooporder** met de volgende waarden:  

     - Leveranciersnr.: 10000  

     - Boekingsdatum = 2 januari 2021  

     - Leveranciersfactuurnr.: 2345  

     Op de inkooporderregel:  

     - Artikeltoeslag = JB-VRACHT  

     - Aantal = 1  

     - Directe kostprijs = 3  

     - Wijs de artikeltoeslag toe aan de inkoopontvangst uit stap 2.  

     Om de stap te voltooien, boekt u het document als ontvangen en gefactureerd.  


**Statusartikelpost van inkoop stap 2**:  
  
|Volgnummer  |Artikelnr.  |Boekingsdatum  |Boekingssoort  |Documentnr.  |Aantal  |Tot. werk. kosten  |Resterend aantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |TOESLAG         |2020-12-15         |Inkoop         |107030         |1         |105         |0        |

**Waardeposten**  

|Volgnummer |Artikelnr.  |Boekingsdatum  |Artikelpostnr.  |Artikelpostsoort  |Boekingssoort  |Documentnr.  | Artikeltoeslagnr.    |  Aantal op artikelpost   |Tot. werk. kosten     |Kosten geboekt naar grootboek |Herwaardering |Vereffenen met post |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |TOESLAG|   2020-12-15    |324         |Inkoop         |Directe kosten         |108029         |         |1          |100    |100         |NEE         |0         |
|399      |TOESLAG   |2021-01-02    |324         |Inkoop         |Directe kosten         |108009         |JB-VRACHT         |0         |3         |3         |NEE         |0         |

**Statusartikelpost verkoop**:  
  
|Volgnummer  |Artikelnr.  |Boekingsdatum  |Boekingssoort  |Documentnr.  |Aantal  |Tot. werk. kosten  |Resterend aantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |TOESLAG         |2020-12-16         |Verkoop         |102035         |-1         |-105         |0        |

**Waardeposten**  

|Volgnummer |Artikelnr.  |Boekingsdatum  |Artikelpostnr.  |Artikelpostsoort  |Boekingssoort  |Documentnr.  | Artikeltoeslagnr.    |  Aantal op artikelpost   |Tot. werk. kosten     |Kosten geboekt naar grootboek |Herwaardering |Vereffenen met post |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |TOESLAG|   2020-12-16    |325         |Verkoop         |Directe kosten         |109024         |         |-1          |-100    |-100         |NEE         |0         |
|400      |TOESLAG   |2021-01-01    |325         |Verkoop         |Directe kosten         |109024         |         |0         |-3         |-3         |Ja         |398         |

6.  Op werkdatum 3 januari arriveert een inkoopfactuur met een aanvullende artikeltoeslag boven op de inkoop die in stap 2 is gedaan. Deze factuur heeft documentdatum 30 december en is dus geboekt met boekingsdatum 30 december 2020.  

     Maak een nieuwe **Inkooporder** met de volgende waarden:  

     - Leveranciersnr.: 10000  

     - Boekingsdatum = 30 december 2020  

     - Leveranciersfactuurnr.: 3456  

     Selecteer op de inkooporderregel de volgende waarden:  

     - Artikeltoeslag = JB-VRACHT  

     - Aantal = 1  

     - Directe kostprijs = 2  

     Wijs de artikeltoeslag toe aan de inkoopontvangst uit stap 2  

     Om de stap te voltooien, boekt u het document als ontvangen en gefactureerd.  


**Statusartikelpost van inkoop**:  

|Volgnummer  |Artikelnr.  |Boekingsdatum  |Boekingssoort  |Documentnr.  |Aantal  |Tot. werk. kosten  |Resterend aantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|324     |TOESLAG         |2020-12-15         |Inkoop         |107030         |1         |105         |0        |

**Waardeposten**  

|Volgnummer |Artikelnr.  |Boekingsdatum  |Artikelpostnr.  |Artikelpostsoort  |Boekingssoort  |Documentnr.  | Artikeltoeslagnr.    |  Aantal op artikelpost   |Tot. werk. kosten     |Kosten geboekt naar grootboek |Herwaardering |Vereffenen met post |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|397      |TOESLAG   |2020-12-15    |324         |Inkoop         |Directe kosten         |108029         |            |1         |100    |100         |Nee         |0         |
|399      |TOESLAG   |2021-01-02    |324         |Inkoop         |Directe kosten         |108030         |JB-VRACHT   |0         |3         |3         |Nee         |0         |
|401      |TOESLAG   |**2020-12-30**    |324         |Inkoop         |Directe kosten         |108031         |JB-VRACHT   |0         |2         |2         |Nee         |0         |

**Statusartikelpost verkoop**:  
  
|Volgnummer  |Artikelnr.  |Boekingsdatum  |Boekingssoort  |Documentnr.  |Aantal  |Tot. werk. kosten  |Resterend aantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|
|325     |TOESLAG         |12-2020-16         |Verkoop         |102035         |-1         |-105         |0        |

**Waardeposten**  

|Volgnummer |Artikelnr.  |Boekingsdatum  |Artikelpostnr.  |Artikelpostsoort  |Boekingssoort  |Documentnr.  | Artikeltoeslagnr.    |  Aantal op artikelpost   |Tot. werk. kosten     |Kosten geboekt naar grootboek |Herwaardering |Vereffenen met post |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|398      |TOESLAG   |12-2020-16        |325         |Verkoop         |Directe kosten         |103024         |            |-1         |-100       |-100         |Nee         |0         |
|400      |TOESLAG   |2021-01-01        |325         |Verkoop         |Directe kosten         |103024         |            |0          |-3         |-3         |Ja         |398         |
|402      |TOESLAG   |**2021-01-01**    |325         |Verkoop         |Directe kosten         |103024         |            |0          |-2         |-2         |Ja         |398         |

Het rapport Voorraadwaardering wordt afgedrukt vanaf 31 december 2020

![Inhoud van het voorraadwaarderingsrapport.](media/helene/TechArticleAdjustcost13.png "Inhoud van het voorraadwaarderingsrapport")

**Overzicht van scenario:**  

Het beschreven scenario eindigt met een rapport Voorraadwaardering dat Aantal = 0 aangeeft terwijl de waarde = 2. De artikeltoeslag die in stap 6 is geboekt, maakt deel uit van de positieve voorraadmutatiewaarde van december terwijl de negatieve voorraadmutatie van dezelfde periode niet wordt beïnvloed.  

Dat de boekhoudinstellingen Boeken toegest. vanaf 1 januari aangeven, was goed voor de eerste artikeltoeslag. De kosten van de positieve en de negatieve voorraadmutatie zijn in dezelfde periode vastgelegd. Voor de tweede artikeltoeslag leiden de boekhoudinstellingen er echter toe dat de wijziging in COGS in de volgende periode wordt herkend.  

**Conclusie:**  

Het is een uitdaging om het rapport Voorraadwaardering Aantal = 0 aan te laten geven terwijl de Waarde <> 0. In dat geval is het ook moeilijker de optimale instellingen aan te geven, wanneer inkoopfacturen op dezelfde dag arriveren, maar verschillende perioden of zelfs boekjaren betreffen. De overgang naar een nieuw boekjaar vereist meestal enige planning en als onderdeel daarvan moet het proces Kostprijs herwaarderen - Artikelposten, rekening houdend met COGS, worden overwogen.  

In dit scenario zou één scenario kunnen zijn het veld Boekhoudinstellingen, Boeken toegest. vanaf voor enkele dagen een datum in december te geven en de boeking van de eerste artikeltoeslag uit te stellen om mogelijk te maken dat alle kosten voor de vorige periode/boekjaar eerst worden herkend voor de periode waartoe ze behoren, de batchverwerking Kosten herwaarderen - Artikelposten uit te voeren en daarna de toegestane boekingsdatum te verplaatsen naar de nieuwe periode\/boekjaar. De eerste artikeltoeslag met boekingsdatum 2 januari kan dan worden geboekt.  

## <a name="see-also"></a><a name="see-also"></a>Zie ook

[Ontwerpdetails: Boekingsdatum op herwaarderingswaardepost](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md)  
[Ontwerpdetails: Artikelvereffening](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
