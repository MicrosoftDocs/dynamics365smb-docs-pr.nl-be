---
title: Boekingsdatum in waardeposten
description: Leren hoe de batchverwerking Kostprijs herwaarderen - Artikelposten een boekingsdatum bepaalt en toewijst aan de waardeposten die de batchverwerking gaat maken.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 2595efa188aed593bf1d112f984acf411446959b
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2307144"
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a>Ontwerpdetails: Boekingsdatum op herwaarderingswaardepost
Dit artikel begeleidt gebruikers bij de functionaliteit Voorraadwaardering in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Het specifieke artikel legt uit hoe de batchverwerking **Kostprijs herwaarderen - Artikelposten** een boekingsdatum bepaalt en toewijst aan de waardeposten die de batchverwerking gaat maken.  

Eerst wordt het concept van het proces bekeken, hoe de batchverwerking de boekingsdatum bepaalt en toewijst aan de waardepost die wordt gemaakt. Daarna zijn er enkele gedeelde scenario's die we in het ondersteuningsteam van tijd tot tijd tegenkomen en uiteindelijk is er een lijst met de begrippen die vanaf versie 3.0 worden gebruikt.  

## <a name="the-concept"></a>Het concept  
Vanaf versie 5.0 wijst de batchverwerking **Kostprijs herwaarderen - Artikelposten** een boekingsdatum toe aan de waardepost die gaat worden gemaakt in de volgende stappen:  

1.  Eerst is de boekingsdatum van de post die wordt gemaakt, hetzelfde als de datum van de post die wordt aangepast.  

2.  De boekingsdatum wordt gevalideerd tegen voorraadperioden en/of boekhoudinstellingen.  

3.  Toewijzing van boekingsdatum; als de oorspronkelijke boekingsdatum niet binnen het toegestane boekingsdatumbereik ligt, wijst de batchverwerking een toegestane boekingsdatum uit Boekhoudinstellingen of Voorraadperiode toe. Als zowel voorraadperioden als toegestane boekingsdatums in grootboekinstellingen zijn gedefinieerd, wordt de latere datum van de twee toegewezen aan de herwaarderingswaardepost.  

 Laten we dit proces eens in de praktijk bekijken. Stel dat we een artikelpost Verkoop hebben. Het artikel is verzonden op 5 september 2013 en de dag erna gefactureerd.  

![Status van artikelposten in het scenario](media/helene/TechArticleAdjustcost1.png "Status van artikelposten in het scenario")  

Hieronder vertegenwoordigt de eerste waardepost (379) de verzending en heeft dezelfde boekingsdatum als de bovenliggende artikelpost.  

De tweede artikelpost (381) vertegenwoordigt de factuur.  

 De derde waardepost (391) is een herwaardering van de factuurwaardepost (381)  

 ![Status van waardeposten in het scenario](media/helene/TechArticleAdjustcost2.png "Status van waardeposten in het scenario")  

 Stap 1: De te maken herwaarderingspost krijgt dezelfde boekingsdatum toegewezen als de post die ermee wordt geherwaardeerd, hierboven geïllustreerd door waardepost 391.  

 Stap 2: Validatie van in eerste instantie toegewezen boekingsdatum.  

De batchverwerking **Kostprijs herwaarderen - Artikelposten** bepaalt of de oorspronkelijke boekingsdatum van de herwaarderingswaardepost binnen het toegestane boekingsdatumbereik ligt, op basis van voorraadperioden en/of boekhoudinstellingen.  

 Laten we de hierboven genoemde Verkoop bekijken door instelling van toegestane boekingsdatumbereiken toe te voegen.  

 Voorraadperioden:  

![Voorraadperioden in het scenario](media/helene/TechArticleAdjustcost3.png "Voorraadperioden in het scenario")

 De eerste toegestane boekingsdatum is de eerste dag van de eerste open periode. 1 September 2013.  

 Grootboekinstellingen:  

![Grootboekinstelling in het scenario](media/helene/TechArticleAdjustcost4.png "Grootboekinstelling in het scenario")

 De eerste toegestane boekingsdatum is de datum in het veld Boeken toegest. vanaf: 10 september 2013.  

 Als zowel voorraadperioden als toegestane boekingsdatums in grootboekinstellingen zijn gedefinieerd, definieert de latere datum van de twee het toegestane boekingsdatumbereik.  

 Stap 3: Toewijzing van een toegestane boekingsdatum;  

 De aanvankelijke toegewezen Boekingsdatum was 6 september, zoals in stap 1 wordt beschreven. Echter, in de tweede stap identificeert de batchverwerking Kostprijs herwaarderen - Artikelposten dat de vroegste toegestane boekingsdatum 10 september is en wijst dus 10 september toe aan de herwaarderingswaardepost, onder.  

 ![Status van waardeposten in het scenario 2](media/helene/TechArticleAdjustcost5.png "Status van waardeposten in het scenario 2")

 We hebben nu het concept bekeken voor het toewijzen van Boekingsdatums aan waardeposten die worden gemaakt door de batchverwerking Kostprijs herwaarderen - Artikelposten.  

 Laten we enkele scenario's bekijken die we in het ondersteuningsteam van tijd tot tijd tegenkomen in verband met toegewezen boekingsdatums in de batchverwerking Kostprijs herwaarderen - Artikelposten en gerelateerde instellingen.  

## <a name="scenarios"></a>Scenario's  

### <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Scenario I: "De boekingsdatum ligt niet binnen het bereik van toegestane boekingsdatums."  
 Dit is een scenario waarin een gebruiker het genoemde foutbericht krijgt wanneer de batchverwerking Kostprijs herwaarderen - Artikelposten wordt uitgevoerd.  

 In de vorige sectie, waar het concept van het toewijzen van boekingsdatums wordt besproken, is het de bedoeling van de batchverwerking Kostprijs herwaarderen - Artikelposten een waardepost te maken met de boekingsdatum 10 september.  

![Foutmelding over boekingsdatum](media/helene/TechArticleAdjustcost6.png "Foutmelding over boekingsdatum")

 We gaan door op de gebruikersinstelling:  

![Instelling van toegestane boekingsdatum van gebruiker](media/helene/TechArticleAdjustcost7.png "Instelling van toegestane boekingsdatum van gebruiker")

 De gebruiker heeft in dit geval een toegestane boekingsdatumreeks van 11 september tot 30 september en mag daardoor de herwaarderingswaardepost niet boeken met boekingsdatum 10 september.  

![Overzicht van betrokken instelling van boekingsdatum](media/helene/TechArticleAdjustcost8.png "Overzicht van betrokken instelling van boekingsdatum")

 Knowledge Base-artikel [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) bespreekt aanvullende scenario's in verband met het genoemde foutbericht.  

### <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a>Scenario II: Boekingsdatum op Herwaarderingswaardepost versus Boekingsdatum op post die de correctie veroorzaakt, zoals Herwaardering of productie Artikeltoeslag.  

### <a name="revaluation-scenario"></a>Herwaarderingsscenario:  
 Vereisten:  

 Voorraadinstelling:  

-   Autom. voorraadwaarde boeken = Ja  

-   Automatische kostenwaardering = Altijd  

-   Gem. kostprijsberekeningsoort = artikel  

-   Periode gemiddelde kostprijsberekening = Dag  

 Grootboekinstellingen:  

-   Boeken toegest. vanaf = 1 januari 2014  

-   Boeken toegest. tot = leeg  

 Gebruikersinstellingen:  

-   Boeken toegest. vanaf = 1 december 2013.  

-   Boeken toegest. tot = leeg  

##### <a name="to-test-the-scenario"></a>Het scenario testen  

1.  ArtikelTEST maken:  

     Basiseenheid = Stuks  

     Waarderingsmethode = Gemiddelde  

     Selecteer optionele boekingsgroepen.  

2.  Open artikeldagboek, maak en boek een regel als volgt:  

     Boekingsdatum = 15 december 2013  

     Artikel = TEST  

     Boekingssoort = Inkoop  

     Aantal = 100  

     Eenheidsprijs = 10  

3.  Open artikeldagboek, maak en boek een regel als volgt:  

     Datum = 20 december 2013  

     Artikel = TEST  

     Boekingssoort = Negatieve herwaardering  

     Aantal = 2  

4.  Open artikeldagboek, maak en boek een regel als volgt:  

     Datum = 15 januari 2014  

     Artikel = TEST  

     Boekingssoort = Negatieve herwaardering  

     Aantal = 3  

5.  Open herwaarderingsdagboek, maak en boek een regel als volgt:  

     Artikel = TEST  

     Vereffenen met post = selecteer inkooppost die is geboekt in stap 2. De boekingsdatum van de herwaardering is dezelfde als van de post die wordt aangepast.  

     Kostprijs (Geherwaardeerd) = 40  

 De volgende artikel- en waardeposten zijn geboekt:  

![Overzicht van resulterende artikel- en waardeposten 1](media/helene/TechArticleAdjustcost9.png "Overzicht van resulterende artikel- en waardeposten 1")

 ![Overzicht van resulterende artikel- en waardeposten 2](media/helene/TechArticleAdjustcost10.png "Overzicht van resulterende artikel- en waardeposten 2")

 De batchverwerking Kostprijs herwaarderen - Artikelposten heeft een wijziging in kosten herkend en de negatieve herwaarderingen aangepast.  

 **Controle van boekingsdatums in gemaakte herwaarderingswaardeposten:** De vroegste toegestane boekingsdatum waarop de batchverwerking Kostprijs herwaarderen - Artikelposten betrekking moet hebben is 1 januari 2014, zoals gesteld in de boekhoudinstellingen.  

 **Negatieve herwaardering in stap 3:** toegewezen boekingsdatum is 1 januari, bepaald door boekhoudinstellingen. De boekingsdatum van de waardepost in het bereik voor herwaardering is 20 december 2013. Volgens de boekhoudinstellingen ligt de datum niet binnen het toegestane boekingsdatumbereik. Daarom wordt de boekingsdatum in het veld Boeken toegest. vanaf in de boekhoudinstellingen toegewezen aan de herwaarderingswaardepost.  

 **Negatieve herwaardering in stap 4:** toegewezen boekingsdatum is 15 januari. De waardepost in het bereik van herwaardering heeft boekingsdatum 15 januari, wat ligt binnen het toegestane boekingsdatumbereik, volgens de boekhoudinstellingen.  

 De herwaardering die wordt aangebracht voor de Negatieve herwaardering in stap 3 leidt tot discussie. De gunstige boekingsdatum voor de Herwaarderingswaardepost zou 20 december zijn of ten minste in december liggen aangezien de herwaardering die de wijziging in COGS heeft veroorzaakt, is geboekt in december.  

 Om herwaardering in december te bereiken van de negatieve correctie in stap 3, moet het veld Boeken toegest. vanaf in de boekhoudinstellingen een datum in december bevatten.  

 **Conclusie:**  

 Overweeg met de ervaringen uit dit scenario de geschiktste instelling van toegestane boekingsdatumbereik voor een bedrijf. Het volgende kan nuttig zijn: zolang wijzigingen in voorraadwaarde in een periode mogen worden geboekt, december in dit geval, moet de instelling die het bedrijf gebruikt voor toegestane boekingsdatumbereiken, overeenstemmen met deze beslissing. Het veld Boeken toegest. vanaf in de boekhoudinstellingen, dat 1 december bevat, zou toestaan dat de herwaardering die in december is aangebracht, wordt doorgestuurd naar betrokken uitgaande posten in dezelfde periode.  

 Gebruikersgroepen die niet in december mogen boeken, maar in januari, een beperking die waarschijnlijk de bedoeling was van de boekhoudinstellingen in dit scenario, moeten in plaats daarvan worden geregeld met de gebruikersinstellingen.  

### <a name="item-charge-scenario"></a>Artikeltoeslagscenario:  
 Vereisten:  

 Voorraadinstelling:  

-   Autom. voorraadwaarde boeken = Ja  

-   Automatische kostenwaardering = Altijd  

-   Gem. kostprijsberekeningsoort = artikel  

-   Periode gemiddelde kostprijsberekening = Dag  

 Grootboekinstellingen:  

-   Boeken toegest. vanaf = 1 december 2013.  

-   Boeken toegest. tot = leeg  

 Gebruikersinstellingen:  

-   Boeken toegest. vanaf = 1 december 2013.  

-   Boeken toegest. tot = leeg  

##### <a name="to-test-the-scenario"></a>Het scenario testen  

1.  Artikeltoeslag maken:  

     Basiseenheid = Stuks  

     Waarderingsmethode = Gemiddelde  

     Selecteer optionele boekingsgroepen.  

2.  Nieuwe inkooporder maken  

     Orderleveranciersnr.: 10000  

     Boekingsdatum = 15 december 2013  

     Leveranciersfactuurnr.: 1234  

     Op de inkooporderregel:  

     Artikel = TOESLAG  

     Aantal = 1  

     Directe kostprijs = 100  

     Ontvangst en factuur boeken.  

3.  Nieuwe verkooporder maken:  

     Orderklantnr.: 10000  

     Boekingsdatum = 16 december 2013  

     Op de verkooporderregel:  

     Artikel = TOESLAG  

     Aantal = 1  

     Eenheidsprijs - 135  

     Verzenden en factureren boeken.  

4.  Grootboekinstellingen:  

     Boeken toegest. vanaf = 1 januari 2014  

     Boeken toegest. tot = leeg  

5.  Nieuwe inkooporder maken:  

     Orderleveranciersnr.: 10000  

     Boekingsdatum = 2 januari 2014  

     Leveranciersfactuurnr.: 2345  

     Op de inkooporderregel:  

     Artikeltoeslag = JB-VRACHT  

     Aantal = 1  

     Directe kostprijs = 3  

     Wijs artikeltoeslag toe aan inkoopontvangst uit stap 2.  

     Ontvangst en factuur boeken.  

     ![Overzicht van resulterende artikel- en waardeposten 3](media/helene/TechArticleAdjustcost11.png "Overzicht van resulterende artikel- en waardeposten 3")

6.  Op werkdatum 3 januari arriveert een inkoopfactuur met een aanvullende artikeltoeslag bovenop de inkoop die in stap 2 is gedaan. Deze factuur heeft documentdatum 30 december en is dus geboekt met boekingsdatum 30 december 2013.  

     Nieuwe inkooporder maken:  

     Orderleveranciersnr.: 10000  

     Boekingsdatum = 30 december 2013  

     Leveranciersfactuurnr.: 3456  

     Op de inkooporderregel:  

     Artikeltoeslag = JB-VRACHT  

     Aantal = 1  

     Directe kostprijs = 2  

     Wijs artikeltoeslag toe aan inkoopontvangst uit stap 2  

     Ontvangst en factuur boeken.  

   ![Overzicht van resulterende artikel- en waardeposten 4](media/helene/TechArticleAdjustcost12.png "Overzicht van resulterende artikel- en waardeposten 4")

 Het rapport Voorraadwaardering wordt afgedrukt vanaf 31 december 2013  

![Inhoud van het voorraadwaarderingsrapport](media/helene/TechArticleAdjustcost13.png "Inhoud van het voorraadwaarderingsrapport")

 **Overzicht van scenario:**  

 Het beschreven scenario eindigt met een rapport Voorraadwaardering dat Aantal = 0 aangeeft terwijl de waarde = 2. De artikeltoeslag die in stap 11 is geboekt, maakt deel uit van de positieve voorraadmutatiewaarde van december terwijl de negatieve voorraadmutatie van dezelfde periode niet wordt beïnvloed.  

 Dat de boekhoudinstellingen Boeken toegest. vanaf 1 januari aangeven, was goed voor de eerste artikeltoeslag. De kosten van de positieve en de negatieve voorraadmutatie zijn in dezelfde periode vastgelegd. Voor de tweede artikeltoeslag leiden de boekhoudinstellingen er echter toe dat de wijziging in COGS in de volgende periode wordt herkend.  

 **Conclusie:**  

 Het is een uitdaging om het rapport Voorraadwaardering Aantal = 0 aan te laten geven terwijl de Waarde <> 0. In dat geval is het ook moeilijker de optimale instellingen aan te geven, wanneer inkoopfacturen op dezelfde dag arriveren, maar verschillende perioden of zelfs boekjaren betreffen. De overgang naar een nieuw boekjaar vereist meestal enige planning en als onderdeel daarvan moet het proces Kostprijs herwaarderen - Artikelposten, rekening houdend met COGS, worden overwogen.  

 In dit scenario zou één scenario kunnen zijn het veld Boekhoudinstellingen, Boeken toegest. vanaf voor enkele dagen een datum in december te geven en de boeking van de eerste artikeltoeslag uit te stellen om mogelijk te maken dat alle kosten voor de vorige periode/boekjaar eerst worden herkend voor de periode waartoe ze behoren, de batchverwerking Kosten herwaarderen - Artikelposten uit te voeren en daarna de toegestane boekingsdatum te verplaatsen naar de nieuwe periode\/boekjaar. De eerste artikeltoeslag met boekingsdatum 2 januari kan dan worden geboekt.  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a>Historie van batchverwerking Kostprijs herwaarderen - Artikelposten  
 Hieronder vindt u een overzicht van het concept boekingsdatums toewijzen aan herwaarderingswaardeposten door de batchverwerking Kostprijs herwaarderen - Artikelposten, sinds versie 3.0.  

### <a name="from-version-30370a"></a>Vanaf versie 3.0..3.70.A  
 In het aanvraagformulier van de batchverwerking Kostprijs herwaarderen - Artikelposten moet een boekingsdatum worden ingevoerd door de gebruiker. De batchverwerking doorloopt alle benodigde wijzigingen en maakt waardeposten met de boekingsdatum ingevoerd in het aanvraagformulier. Te gebruiken voorgestelde boekingsdatum is de datum van vandaag.  

### <a name="version-370b40"></a>Versie 3.70.B..4.0  
 In het aanvraagformulier van de batchverwerking Kostprijs herwaarderen - Artikelposten moet een Boekingsdatum post afgesloten periode worden ingevoerd door de gebruiker. De batchverwerking doorloopt alle noodzakelijke wijzigingen en maakt waardeposten met de boekingsdatum van de hoofdartikelpost (verzenddatum van de verkoop waarop de herwaardering betrekking heeft). Als de boekingsdatum van de hoofdartikelpost niet binnen het toegestane boekingsdatumbereik ligt, krijgt de postboekingsdatum die is vermeld als Boekingsdatum post afgesloten periode de Herwaarderingswaardepost toegewezen. De datum wordt geacht zich in een afgesloten periode te bevinden wanneer deze eerder ligt dan de datum in het veld Boeken toegest. vanaf in de Boekhoudinstellingen.  

### <a name="from-version-50"></a>Vanaf versie 5.0:  
 Er hoeft geen boekingsdatum meer te worden vermeld in het aanvraagformulier van de batchverwerking Kostprijs herwaarderen - Artikelposten. De batchverwerking doorloopt alle benodigde wijzigingen en maakt waardeposten met de boekingsdatum van de waardepost die wordt geherwaardeerd. Als de boekingsdatum niet binnen het toegestane boekingsdatumbereik ligt, wordt de boekingsdatum in het veld Boeken toegest. vanaf in de boekhoudinstellingen gebruikt, OF als de voorraadperioden worden gebruikt, wordt de laatste datum van de twee gebruikt. Zie hierboven beschreven concept.  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a>Historie van batchverwerking Voorraadwaarde boeken.  
 De batchverwerking Voorraadwaarde boeken is nauw verbonden met de batchverwerking Kostprijs herwaarderen - Artikelposten. Daarom wordt de historie van deze batchverwerking hier ook samengevat en gedeeld.  

### <a name="from-version-30370a"></a>Vanaf versie 3.0..3.70.A  
 In het aanvraagformulier van de batchverwerking Voorraadwaarde boeken moet een boekingsdatum worden ingevoerd door de gebruiker. De batchverwerking doorloopt alle waardeposten binnen het filter, als die er zijn, en maakt grootboekposten met de boekingsdatum die is ingevoerd in het aanvraagformulier.  

### <a name="version-370b40"></a>Versie 3.70.B..4.0  
 In het aanvraagformulier van de batchverwerking Voorraadwaarde boeken is het veld Boekingsdatum post afgesloten periode beschikbaar. Die datum die u in dit veld invoert, wordt als de boekingsdatum gebruikt voor de grootboekposten die worden gemaakt voor waardeposten waarvan de boekingsdatum in gesloten boekingsperioden ligt. Anders hebben de grootboekposten dezelfde boekingsdatum als de oorspronkelijke waardeposten. De datum wordt geacht zich in een afgesloten periode te bevinden wanneer deze eerder ligt dan de datum in het veld Boeken toegest. vanaf in de Boekhoudinstellingen. Als per boekingsgroep naar het grootboek wordt geboekt, krijgen de grootboekposten de boekingsdatum die is opgegeven in het veld Boekingsdatum op het aanvraagformulier.  

 In versie 3 en 4 worden tijdens de batchverwerking alle waardeposten gescand om te detecteren of er waardeposten zijn waarbij Tot. werk. kosten verschilt van Vrd.-waarde geboekt. Als er een verschil wordt gedetecteerd, wordt het afwijkende bedrag geboekt in een grootboekpost. Als boeking van verwachte kosten wordt gebruikt, worden corresponderende velden op dezelfde manier behandeld.  

![Werkelijke kosten versus verwachte kosten](media/helene/TechArticleAdjustcost14.png "Werkelijke kosten versus verwachte kosten")

### <a name="from-version-50"></a>Vanaf versie 5.0:  
 Er hoeft geen boekingsdatum meer te worden vermeld in het aanvraagformulier van de batchverwerking Voorraadwaarde boeken. De grootboekpost wordt gemaakt met dezelfde boekingsdatum als de gerelateerde waardepost. Als u de batchverwerking wilt voltooien, moet het toegestane boekingsdatumbereik de boekingsdatum van de gemaakte grootboekpost toestaan. Als dit niet het geval is, moet de toegestane boekingsdatumreeks tijdelijk opnieuw worden geopend door de datums in het veld Boeken toegest. vanaf en tot in Boekhoudinstellingen te wijzigen of te verwijderen. Om reconciliatieproblemen te voorkomen is het vereist dat de boekingsdatum van de grootboekpost correspondeert met de boekingsdatum van de waardepost.  

 De batchverwerking scant tabel 5811 - Waardepost naar GB boeken om de waardeposten te bepalen in het bereik voor boeking naar het grootboek. Na een succesvolle uitvoering wordt de tabel geleegd.

## <a name="see-also"></a>Zie ook  
[Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md)  
[Ontwerpdetails: Artikelvereffening](design-details-item-application.md)  
