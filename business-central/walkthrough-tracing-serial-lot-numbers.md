---
title: 'Procedure: Serie-/lotnummers traceren'
description: 'Dit onderwerp beschrijft de acties die moeten worden ondernomen om te voorkomen dat een defect artikel wordt verkocht, en ook hoe artikelen te traceren en terug te roepen wanneer dat nodig is.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: bholtorf
---
# <a name="walkthrough-tracing-seriallot-numbers" />Procedure: Serie-/lotnummers traceren

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Als er productdefecten optreden, moeten de fouten worden opgespoord en de betreffende artikelen mogen het bedrijf niet verlaten. Als er al defecte artikelen zijn geleverd, is het belangrijk om bij te houden wie ze heeft ontvangen, zodat ze zo nodig kunnen worden teruggehaald.  

De eerste taak van defectenbeheer is om te onderzoeken waar de defecte artikelen vandaan zijn gekomen en waar ze zijn gebruikt. Dit onderzoek is gebaseerd op historische gegevens en het wordt vergemakkelijkt als er kan worden gezocht via vermeldingen voor het traceren van artikelen op de pagina **Artikeltracering**.  

De tweede taak van defectenbeheer is vaststellen of de getraceerde artikelen zijn gepland in open documenten zoals niet-geboekte verkooporders of verbruiksdagboeken. Dit werk wordt uitgevoerd op de pagina **Posten zoeken**. U kunt de functie Posten zoeken gebruiken om alle soorten databaserecords te zoeken.  

## <a name="about-this-walkthrough" />Informatie over deze procedure

In dit overzicht wordt uitgelegd hoe u kunt achterhalen welke artikelen defect zijn, welke leverancier ze heeft geleverd en waar ze worden gebruikt, zodat deze orders kunnen worden stopgezet of teruggehaald.  

In deze procedure worden de volgende taken beschreven:  

- Traceren van gebruik naar oorsprong.  
- Traceren van oorsprong naar gebruik.  
- Zoeken naar alle huidige records waarin het getraceerde serie-/lotnummer voorkomt.  

## <a name="roles" />Rollen

In dit overzicht worden taken gedemonstreerd voor de volgende gebruikersrollen:  

- Kwaliteitscontroleur  
- Magazijnbeheerder  
- Orderverwerker  
- Inkoper  

## <a name="prerequisites" />Vereisten

U moet het volgende doen om deze procedure uit te voeren:  

- Het bedrijf [!INCLUDE[prod_short](includes/prod_short.md)].  
<!-- - To create new items and several business transactions by following the [Prepare Sample Data](walkthrough-tracing-serial-lot-numbers.md#prepare-sample-data).   -->

## <a name="story" />Scenario

Ricardo, de kwaliteitscontroleur, is bezig met het teruggegeven artikel 1002, een racefiets. De klant, Selangorian Ltd., heeft geklaagd dat het frame gescheurde lasnaden heeft. Kwaliteitscontroletechnici hebben bevestigd dat het frame van de teruggegeven fiets gebreken vertoont. De kwaliteitscontroleur moet nu de volgende dingen vaststellen:  

- Welke partij raceframes vertoont gebreken?  
- Op welke inkooporder is de defecte partij ontvangen?  

Van de verkoopafdeling weet de kwaliteitscontroleur dat de teruggegeven racefiets, artikel 1002, het serienummer SN1 heeft. Met deze basisinformatie moet ze bepalen waar de voltooide racefiets voor het laatst is gebruikt en dan moeten ze deze traceren naar het eerste begin om vast te stellen van welk partijnummer het defecte onderdeel, het frame, afkomstig is.  

Met de resultaten van deze eerste artikeltraceringstaak wordt vastgesteld welke raceframes defect waren en welke leverancier ze heeft geleverd. Daarna, maar binnen hetzelfde algemene traceringsproces, moet de kwaliteitscontroleur alle verkochte racefietsen opzoeken met raceframes uit de defecte partij, zodat deze orders kunnen worden stopgezet of teruggehaald. Ten slotte moet de kwaliteitscontroleur eventuele open documenten opzoeken waarin de defecte partij wordt gebruikt, zodat er geen verdere transacties worden verricht.  

De twee eerste defectenbeheertaken worden uitgevoerd op de pagina **Artikeltracering**. De laatste taak wordt uitgevoerd op de pagina **Posten zoeken**, in integratie met de pagina **Artikeltracering**.  

## <a name="prepare-sample-data" />Voorbeeldgegevens voorbereiden

U moet de volgende nieuwe artikelen maken:  

- 2000, raceframe: partijspecifieke tracering, onderdeel van 1002  
- 1002, racefiets: serienummerspecifieke tracering  

Vervolgens moet u diverse inkoop-, productie- en verkooptransacties met beide artikelen maken.  

### <a name="to-create-the-items" />De artikelen maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Selecteer in het veld **Nr.** Voer in het veld **2000** in en vul de volgende velden in.  

    |Omschrijving|Basiseenheid|Dagb. Productboekingsgroep|Btw-productboekingsgroep|Voorraadboekingsgroep|Artikeltraceringscode|  
    |-----------|--------------------|------------------------|-----------------------|--------------------|------------------|  
    |Raceframe|Per stuk|GRONDSTOF|BTW25|GRONDSTOF|LOTALL|  

    > [!NOTE]  
    >  U kunt de basiseenheid invoeren door de knop **Nieuw** te kiezen en vervolgens **PSC** te selecteren op de pagina **Artikeleenheden**.  

4. Alle andere velden hebben acceptabele standaardgegevens of hoeven niet te worden ingevuld.  
5. Kies de knop **OK** om de eerste nieuwe artikelkaart te maken, 2000.  
6. Kies **Nieuwe**.  
7. Selecteer in het veld **Nr.** Voer in het veld **1002** in en vul de volgende velden in.  

    |Omschrijving|Basiseenheid|Dagb. Productboekingsgroep|Btw-productboekingsgroep|Voorraadboekingsgroep|Aanvullingsmethode|Artikeltraceringscode|  
    |-----------------|--------------------------|------------------------------|-----------------------------|-----------------------------|--------------------------|------------------------|  
    |Racefiets|Per stuk|DET.HANDEL|BTW25|GEREED|Prod.-order|SNALLE|  

    > [!NOTE]  
    >  U kunt de basiseenheid invoeren door de knop **Nieuw** te kiezen en vervolgens **PSC** te selecteren op de pagina **Artikeleenheden**.  

    Vervolgens moet u de productie-instelling van het artikel definiëren.

8. Voer op het sneltabblad **Aanvulling** de waarde **1000** in het veld **Bew.-plannr.** in.  
9. Kies het veld **Prod.-stuklijstnr.** en kies vervolgens **Geavanceerd**.  
10. Kies op de pagina **Productiestuklijst** de eerste regel **1000** en kies vervolgens de actie **Bewerken**.  
11. Wijzig op de pagina **Productiestuklijst** de waarde in het veld **Status** in **In ontwikkeling**.  
12. Ga naar een lege regel, voer **2000** in het veld **Nr.** in en voer vervolgens **1** in het veld **Aantal per** in.  
13. Wijzig de waarde in het veld **Status** terug naar **Gecertificeerd**.  
14. Kies de knop **OK** om de productiestuklijst in te voegen op de artikelkaart en de pagina **Productiestuklijst** te sluiten.  

    Vervolgens schaft u raceframes van Custom Metals Incorporated aan.  

### <a name="to-purchase-components" />Materialen kopen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Inkooporders** in en kies vervolgens de gerelateerde koppeling  
2. Kies de actie **Nieuw**.  
3. Maak een inkooporder voor de leverancier Custom Metals Incorporated door de volgende regelvelden in te vullen.  

    |Artikel|Aantal|Lotnr.|  
    |----|--------|-------|  
    |2000|10|LOT1|  

4. Als u het lotnummer wilt invoeren, kiest u de actie **Artikeltraceringsregels**.  
5. Vul op de pagina **Artikeltraceringsregels** de velden **Lotnr.** en **Aantal (Basis)** in en sluit de pagina.  
6. Voer in het veld **Factuurnr. leverancier** een waarde in.  
7. Kies de actie **Boeken**, selecteer de optie **Ontvangen en factureren** en kies vervolgens de knop **OK**.  

    Als volgende, koopt u racingframes van Coolwood Technologies.  
8. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkooporders** in en kies vervolgens de gerelateerde koppeling  
9. Kies de actie **Nieuw**.
10. Maak een inkooporder voor de leverancier Coolwood Technologies door de volgende regelvelden in te vullen.  

    |Artikel|Aantal|Lotnr.|  
    |----------|--------------|-------------|  
    |2000|11|LOT2|  

11. Voer het lotnummer in door op het sneltabblad **Regels** in de groep **Regel** de actie **Artikeltraceringsregels** te kiezen.  
12. Vul op de pagina **Artikeltraceringsregels** de velden **Lotnr.** en **Aantal (Basis)** in en sluit de pagina.  
13. Voer in het veld **Factuurnr. leverancier** een waarde in.  
14. Kies de actie **Boeken**, selecteer de optie **Ontvangen en factureren** en kies vervolgens de knop **OK**.  

    Vervolgens maakt u twee racefietsen, SN1 en SN2.  

### <a name="to-produce-end-items" />Eindproducten produceren

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Vrijgegeven prod.-orders** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de groep **Nieuw**.  
3. Maak een nieuwe vrijgegeven productieorder door de volgende velden in te vullen.  

    |Bronnr.|Aantal|Serienr.|  
    |----------|--------|----------|  
    |1002|2|SN1|  
    |1002|2|SN2|  

4. Kies de actie **Productieorder vernieuwen** en kies de knop **OK** om de regel in te vullen.  
5. Als u de serienummers wilt invoeren, kiest u de actie **Artikeltraceringsregels**.  
6. Vul op de pagina **Artikeltraceringsregels** de velden **Serienr.** en **Aantal (Basis)** in en sluit de pagina.  

    Vervolgens moet u het verbruik aan racingframes van LOT1 boeken.  
7. Op de pagina **Vrijgegeven productieorder** kiest u de actie **Productiedagboek**.  
8. Op de pagina **Productiedagboek** selecteert u de verbruiksregel voor artikel 2000 en kiest u de actie **Artikeltraceringsregels**.
9. Kies op de pagina **Artikeltraceringsregels** het veld **Lotnr.**, kies **LOT1** en klik vervolgens op de knop **OK**.  
10. Laat alle andere standaardwaarden op de pagina **Productiedagboek** ongewijzigd en kies de actie **Boeken**.  

    Maak als volgende nog twee racefietsen, SN3 en SN4.  

11. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Vrijgegeven prod.-orders** in en kies vervolgens de gerelateerde koppeling.  
12. Kies de actie **Nieuw**.  
13. Maak een nieuwe vrijgegeven productieorder door de volgende velden in de kop in te vullen.  

    |Bronnr.|Aantal|Serienr.|  
    |----------------|--------------|----------------|  
    |1002|2|SN3|  
    |1002|2|SN4|  

14. Kies de actie **Productieorder vernieuwen** om de regel in te vullen.  
15. Om de serienummers in te voeren, kiest u de actie **Artikeltraceringsregels** en vult u vervolgens de nummers in op twee regels in het veld **Serienr.** op de pagina **Artikeltraceringsregels**.  

    Vervolgens moet u het verbruik aan racingframes van LOT1 boeken.  
16. Op de pagina **Vrijgegeven productieorder** kiest u de actie **Productiedagboek**.  
17. Op de pagina **Productiedagboek** selecteert u de verbruiksregel voor artikel 2000 en kiest u de actie **Artikeltraceringsregels**.
18. Kies op de pagina **Artikeltraceringsregels** het veld **Lotnr.**, kies **LOT1** en klik vervolgens op de knop **OK**.  
19. Laat alle andere standaardwaarden op de pagina **Productiedagboek** ongewijzigd en kies de actie **Boeken**.  

    U hebt nu vier racefietsen gemaakt, SN1 tot en met SN4, en vier van de tien raceframes van LOT1 gebruikt, twee frames per productieorder.  

20. Sluit het productiedagboek en de productieorders.  

    Vervolgens gaat u racefietsen verkopen. Eest verkoopt u de racefiets met SN1 aan Selangorian Ltd.  

### <a name="to-sell-the-end-items" />De eindpoducten verkopen

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Nieuw** en maak vervolgens een verkooporder door de volgende velden in te vullen.  

    |Klant|Artikel|Aantal|Serienr.|  
    |--------------|----------|----------|----------------|  
    |Anton Geestig Adviezen|1002|1|SN1|  

3.  Om het serienummer in te voeren, kiest u de actie **Artikeltraceringsregels** en vult u vervolgens het nummer in het veld **Serienr.** op de pagina **Artikeltraceringsregels** in.  
4.  Kies de actie **Boeken**, selecteer de optie **Verzenden en factureren** en kies vervolgens de knop **OK**.  

    Vervolgens gaat u de racefiets met SN2 aan Cannon Group PLC verkopen.  

5.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.  
6.  Kies de actie **Nieuw** en maak vervolgens een verkooporder door de volgende velden in te vullen.  

    |Klant|Artikel|Aantal|Serienr.|  
    |--------------|----------|----------|----------------|  
    |Van Terp Kantoorinrichting|1002|1|SN2|  

7.  Om het serienummer in te voeren, kiest u de actie **Artikeltraceringsregels** en vult u vervolgens het nummer in het veld **Serienr.** op de pagina **Artikeltraceringsregels** in.  
8.  Kies de actie **Boeken**, selecteer de optie **Verzenden en factureren** en kies vervolgens de knop **OK**.  

    Ten slotte moet u een paar raceframes afzonderlijk verkopen. Van Terp Kantoorinrichting bestelt ook vier afzonderlijke raceframes voor hun eigen assemblagelijn.  

9. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.  
10. Kies de actie **Nieuw** en maak vervolgens een verkooporder door de volgende velden in te vullen.  

    |Klant|Artikel|Aantal|Serienummer|  
    |--------------|----------|----------|----------------|  
    |Van Terp Kantoorinrichting|2000|5|LOT1|  

11. Om het serienummer op het sneltabblad **Regels** in de groep **Regel** in te voeren, kiest u de actie **Artikeltraceringsregels** en typt u vervolgens het nummer in het veld **Serienr.** op de pagina **Artikeltraceringsregels**.  

    > [!NOTE]  
    >  Boek de laatste verkooporder niet (voor vijf raceframes).  

    Hiermee is de voorbereiding van gegevens voltooid voor het demonstreren van de functies Artikeltracering en Posten zoeken.  

## <a name="tracing-from-usage-to-origin" />Traceren van gebruik naar oorsprong

 Van de verkoopafdeling weet de kwaliteitscontroleur dat de teruggegeven racefiets, artikel 1002, het serienummer SN1 heeft. Met deze basisinformatie kunnen ze bepalen waar de voltooide racefiets voor het laatst is gebruikt, in dit geval bij de verkoopverzending aan Selangorian Ltd. Vervolgens moet de kwaliteitscontroleur deze traceren naar het eerste begin om vast te stellen van welk partijnummer het defecte frame afkomstig is en welke leverancier deze heeft geleverd.  

### <a name="to-determine-which-lot-included-the-faulty-frame-and-who-supplied-it" />Vaststellen uit welke partij het defecte frame afkomstig is en wie deze heeft geleverd

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikeltracering** in en kies vervolgens de gerelateerde koppeling.  
2.  Voer op de pagina **Artikeltracering** de tekst **SN1** in het veld **Serienr.-filter** in en voer vervolgens **1002** in het veld **Artikelfilter** in.  
3.  Laat de standaardinstelling **Met artikeltracering** staan in het veld **Onderdelen weergeven** en houd de standaardtraceringsmethode **Gebruik - oorsprong** bij **Traceringsmethode**.  
4.  Kies de actie **Traceren**.  

    U ziet dat een van de verkoopverzendkoppen overeenkomt met de zoekcriteria. Voordat u doorgaat met de tracering, controleert u of dit de verzending met de defecte racefiets aan Selangorian Ltd is.  

5.  Selecteer de traceringsregel en kies de actie **Document weergeven**.  

    Ga nu verder met het traceren van de oorsprong van de verkoopverzending van de racefiets met nummer SN1.  
6.  Klik op het pictogram + op de traceringsregels om geleidelijk de keten van transacties waaruit de verkoopverzending afkomstig is, uit te vouwen en achterwaarts te traceren.  

    U kunt de volgende transactiegeschiedenis traceren:  

    - Het eerste geboekte document terug in de transactieketen is de uitvoerboeking van SN1 van de eerste vrijgegeven productieorder.  
    - Het volgende geboekte document terug in de keten is de verbruiksboeking van de eerste vrijgegeven productieorder. Hier ziet de kwaliteitscontroleur dat er een raceframe van LOT1 is gebruikt.  
    - Het laagste geboekte document in deze keten is de geboekte inkoopontvangst waarop raceframes met LOT1 in de voorraad zijn gekomen.  

    De kwaliteitscontroleur heeft nu vastgesteld welke partij raceframes defect was en ze kunnen zoeken op de laatste traceringsregel om te zien welke leverancier deze heeft geleverd, namelijk Custom Metals Incorporated.  

    > [!NOTE]  
    >  Breng geen verdere wijzigingen aan in het traceringsresultaat, want dit gaat u gebruiken in het volgende gedeelte.  

     Hiermee is de eerste taak voor defectenbeheer met de pagina **Artikeltracering** voltooid. De kwaliteitscontroleur moet nu bepalen of er andere documenten zijn geboekt waarop raceframes uit LOT1 zijn verwerkt.  

## <a name="tracing-from-origin-to-usage" />Traceren van oorsprong naar gebruik

 De kwaliteitscontroleur heeft vastgesteld dat de defecte raceframes afkomstig waren uit LOT1. Ze moeten nu achterhalen welke andere racefietsen eventueel een raceframe uit de defecte partij hebben, zodat deze fietsen kunnen worden stopgezet of teruggehaald.  

 Een manier om deze traceringstaak voor te bereiden op de pagina **Artikeltracering** is om handmatig LOT1 in te voeren in het veld **Lotnr.-filter** en 2000 in het veld **Artikelfilter**. In dit overzicht wordt echter gebruikgemaakt van de functie **Tegengesteld traceren - Van regel**.  

### <a name="to-find-all-usage-of-the-faulty-lot" />Al het gebruik van de defecte partij opsporen

1.  Selecteer op de pagina **Artikeltracering** de regel van de inkoopontvangst, de laatste traceringsregel, en kies vervolgens **Tegengesteld traceren - Van regel**.  

    Het traceringsresultaat is nu gebaseerd op de filters van de traceringsregel voor de inkoopontvangst, LOT1 en artikel 2000, en het resultaat is gebaseerd op de traceringsmethode **Oorsprong - gebruik**.  

    Voor een overzicht van al het gebruik van artikel 2000 met LOT1 blijft u alle traceringsregels uitvouwen.  

2.  Kies de actie **Alles uitvouwen**.  

    De eerste vier traceringsregels verwijzen naar de verkoopverzending aan Selangorian Ltd., die al is opgelost. De laatste regel geeft aan dat er nog een racefiets, SN2, is geproduceerd in dezelfde vrijgegeven productieorder en vervolgens verkocht en verzonden in een andere verkoopverzending.  

    De kwaliteitscontroleur licht direct de verkoopafdeling in, zodat ze kunnen beginnen met het terughalen van de defecte racefiets bij de klant, Cannon Group PLC.  

    Tegelijkertijd kunnen ze aan de laatste drie traceringsregels zien dat er nog twee artikelen, SN3 en SN4, zijn geproduceerd op basis van raceframes uit LOT1. Ze ondernemen actie om deze eindartikelen in de voorraad te blokkeren.  

    Hiermee is de tweede taak voor defectenbeheer met de pagina **Artikeltracering** voltooid. Aangezien de pagina **Artikeltracering** uitsluitend is gebaseerd op geboekte posten, moet de kwaliteitscontroleur naar de pagina **Posten zoeken** gaan om te controleren of LOT1 niet is gebruikt in niet-geboekte documenten.  

## <a name="finding-all-records-of-a-seriallot-number" />Alle records van een serie/lotnummer zoeken

 Op de pagina **Artikeltracering** heeft de kwaliteitscontroleur gezien dat LOT1 de defecte raceframes bevatte, van welke leverancier ze afkomstig zijn en in welke geboekte transactie ze zijn gebruikt. Ze moeten nu bepalen of LOT1 in open documenten voorkomt door te integreren vanuit het traceringsresultaat naar de pagina **Posten zoeken**, waar ze een zoekactie op alle databaserecords kunnen uitvoeren.  

### <a name="to-find-all-occurrences-of-lot1-in-non-posted-records-such-as-open-orders" />Alle gevallen van LOT1 in niet-geboekte records zoeken zoals open orders

1.  Selecteer op de pagina **Artikeltracering** de aanwijzer in de eerste traceringsregel, de inkoopontvangst van LOT1.  
2.  Kies de actie **Posten zoeken**.  

    De pagina **Posten zoeken** is vooraf ingesteld met zoekfilters op basis van het traceringsresultaat voor LOT1. De kwaliteitscontroleur ziet dat de meeste records te maken hebben met documenten die al zijn geïdentificeerd op de pagina **Artikeltracering**. Zo verwijst bijvoorbeeld de laatste Posten zoeken-regel van het type Productieorder naar de twee vrijgegeven productieorders waarvoor raceframes van LOT1 zijn gebruikt.  

    De tweede Posten zoeken-regel van het type **Verkoopregel** is echter een niet-geboekte documentregel, dus de kwaliteitscontroleur gaat verder met onderzoeken.  

3.  Als u de verkoopregelrecord wilt openen, selecteert u de tweede Posten zoeken-regel en kiest u de actie **Weergeven**. U kunt ook klikken op het getal in het veld **Aantal records**.  

    Hier ziet de kwaliteitscontroleur één open verkoopregel voor de defecte raceframes. Ze stellen onmiddellijk aan de verkoopafdeling voor dat ze deze order annuleren en een nieuwe productieorder starten op basis van goede raceframes.  

 Hiermee is het overzicht van het gebruik van de pagina **Posten zoeken** voor defectenbeheer in integratie met de pagina **Artikeltracering** voltooid.  

## <a name="see-related-microsoft-training" />Zie gerelateerde [Microsoft-training](/training/paths/use-serial-lot-numbers/)

## <a name="see-also" />Zie ook

[Werken met serie- en lotnummers](inventory-how-work-item-tracking.md)  
[Artikelen met artikeltracering traceren](inventory-how-to-trace-item-tracked-items.md)  
[Posten zoeken](ui-find-entries.md)  
[Procedures voor bedrijfsprocessen](walkthrough-business-process-walkthroughs.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
