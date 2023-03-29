---
title: 'Kits verkopen, assembleren en verzenden'
description: Ter ondersteuning van just-in-time voorraad kunnen assemblageorders automatisch worden gemaakt en gekoppeld zodra de verkooporderregel is gemaakt.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: edupont
---
# Procedure: kits verkopen, assembleren en verzenden

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

Ter ondersteuning van just-in-time voorraadbeheer en de mogelijkheid tot het aanpassen van producten op basis van klantaanvragen, kunnen assemblageorders automatisch worden gemaakt en worden gekoppeld zodra de verkooporderregel is gemaakt. De koppeling tussen de verkoopvraag en het assemblage-aanbod stelt de verkooporderverwerkers in staat om het assemblageartikel aan te passen en leveringsdatums af te spreken op basis van de beschikbaarheid van componenten. Bovendien worden assemblageverbruik en -uitvoer automatisch geboekt bij de verzending van de gekoppelde verkooporder.  

Er zijn speciale functies beschikbaar om de verzending van aantallen voor assembleren op basis van orders te bepalen, zoals in basis- als in geavanceerde magazijnconfiguraties. Wanneer werknemers die verantwoordelijk zijn voor het assembleren, klaar zijn met het assembleren van onderdelen of het gehele op-order-assembleren-aantal, registreren ze dit in het veld **Te verzenden aantal** op de magazijnverzendregel in geavanceerde configuraties en kiezen ze vervolgens **Verzending boeken**. Het resultaat is dat de bijbehorende assemblageuitvoer, met inbegrip van het gerelateerde materiaalverbruik, wordt geboekt en dat een verkoopverzending voor de hoeveelheid wordt geboekt voor de gekoppelde verkooporder. In dit scenario wordt het geavanceerde magazijnproces geïllustreerd.  

Wanneer in basismagazijnconfiguraties een aantal voor assembleren op basis van orders klaar is om te worden verzonden, boekt de verantwoordelijke magazijnmedewerker een voorraadpick voor de verkooporderregels. Dit leidt tot het maken van een voorraadverplaatsing voor de componenten, tot het boeken van de assemblage-uitvoer en tot de verkooporderverzending. Zie [Op-order-assembleren-artikelen in voorraadpicks afhandelen](warehouse-how-to-pick-items-with-inventory-picks.md#handling-assemble-to-order-items-with-inventory-picks) voor meer informatie.  

## Informatie over deze procedure

In deze procedure worden de volgende taken gedemonstreerd:  

### Assemblageartikelen instellen

Assemblageartikelen worden gekenmerkt door hun aanvullingsmethode en assemblagestuklijst. Het assemblagebeleid voor het artikel kan assembleren op order (ATO) of assembleren op voorraad (ATS) zijn. In deze sectie komen de volgende taken aan bod:  

-   De juiste aanvullingsmethode en het juiste assemblagebeleid instellen op een nieuwe assemblageartikelkaart.  
-   Een assemblagestuklijst maken die assemblageonderdelen en de resource voor het assemblageartikel aangeeft.  

### Aangepaste assemblageartikelen verkopen

[!INCLUDE[prod_short](includes/prod_short.md)] biedt de flexibiliteit om een voorraadaantal en een hoeveelheid voor assembleren op order in te voeren op één verkooporderregel. In deze sectie komen de volgende taken aan bod:  

-   Er wordt een zuivere ATO-verkooporderregel gemaakt waarbij de volledige aantal niet beschikbaar is en vóór verzending moet worden geassembleerd.  
-   ATO-items aanpassen.  
-   De kostprijs van een aangepaste assemblageartikel herberekenen.  
-   Een gemengde verkooporderregel maken waarbij delen van de verkoophoeveelheid uit voorraad worden geleverd en het resterende deel vóór verzending moet worden geassembleerd.  
-   ATO-beschikbaarheidswaarschuwingen.  

### Assemblageartikelen plannen

Assemblagevraag en -aanbod worden verwerkt door het planningssysteem, net als voor inkoop, transfer en productie. In deze sectie komen de volgende taken aan bod:  

-   Een regeneratief plan voor artikelen uitvoeren met verkoopvraag voor geassembleerde levering.  
-   Een assemblageorder genereren om te voldoen aan een verkoopregelaantal voor de gevraagde verzenddatum.  

### Artikelen samenstellen

Assemblageorders werken op een soortgelijke manier als productieorders, behalve dat het verbruik en de uitvoer rechtstreeks vanuit de order wordt vastgelegd en geboekt. Wanneer de artikelen worden samengesteld voor voorraad, heeft de assemblagemedewerker volledige toegang tot alle kop- en regelvelden. Wanneer de artikelen worden samengesteld voor een order waarbij de hoeveelheid en de datum zijn toegezegd aan de klant, kunnen bepaalde velden in de assemblageorder niet worden bewerkt. In dat geval wordt de assemblageboeking uitgevoerd vanuit de magazijnverzending voor de gekoppelde verkooporder. In deze sectie komen de volgende taken aan bod.  

-   Assemblageverbruik en -uitvoer vastleggen en boeken naar voorraad.  
-   Een magazijnverzendingsregel openen vanuit een ATO-assemblageorder om assemblageactiviteiten vast te leggen.  
-   Een ATO-assemblageorder openen vanuit een magazijnverzendingsregel om de automatisch ingevoerde gegevens te bekijken.  

### Assemblageartikelen vanuit de voorraad en die op order zijn geassembleerd verzenden

Er bestaan speciale functies voor het beheren van aantallen voor assemblage op basis van orders. In deze sectie komen de volgende taken aan bod:  

-   Een magazijnpick maken voor voorraad- en assemblagecomponenten die vóór verzending moeten worden geassembleerd.  
-   Magazijnpicks registreren voor componenten en vervolgens voor assemblageartikelen.  
-   Een assemblageorder openen vanuit een magazijnverzending om gepickte of verbruikte onderdelen te bekijken.  
-   Hoeveelheden voor assembleren op order verzenden.  
-   Voorraadcomponenten verzenden.  

## Rollen

In dit overzicht worden taken gedemonstreerd voor de volgende gebruikersrollen:  

-   Verkooporderverwerker  
-   Planner  
-   Assemblagemedewerker  
-   Picker  
-   Verantwoordelijke voor verzending  

## Vereisten

Voordat u de stappen in deze procedure kunt uitvoeren, moet u het volgende doen:  

-   Installeer [!INCLUDE[prod_short](includes/prod_short.md)].  
-   Maak van uzelf een magazijnwerknemer bij vestiging WIT door de volgende stappen uit te voeren:  

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Magazijnmedewerkers** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies het veld **Gebruikers-ID** en selecteer uw eigen gebruikersaccount op de pagina **Gebruikers**.  
3.  Voer WIT in het veld **Vestiging** in.  
4.  Selecteer het veld **Standaard**.  

> [!NOTE]
> [!INCLUDE [locations-cronus](includes/locations-cronus.md)]

Bereid de vestiging WIT voor assemblageverwerking voor door de volgende stappen uit te voeren:  

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Locaties** in en kies vervolgens de gerelateerde koppeling.  
2.  Open de vestigingskaart voor de vestiging WIT.  
3.  Voer op het sneltabblad **Opslaglocaties** in het veld **Opslaglocatie Naar-assemblage** de waarde **W-10-0001** in.  

    Wanneer u deze niet-pickopslaglocatiecode invoert, kunnen alle assemblageorder hun onderdelen in de opslaglocatie ontvangen.  

4.  Voer in het veld **Opslaglocatie Naar-assemblage** de waarde **W-01-0001** in.  

    Als u deze pick-opslaglocatie invoert, worden voltooide assemblageartikelen uitgevoerd naar de opslaglocatie.  

Verwijder de standaarddoorlooptijd voor interne processen door de volgende stappen uit te voeren:  

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Productie-instellingen** in en kies vervolgens de gerelateerde koppeling.  
2.  Verwijder op de pagina **Productie-instellingen** op het sneltabblad **Planning** de waarde in het veld **Std. veiligheidstijd**.  

<!-- Create inventory for assembly components by following [Prepare Sample Data](walkthrough-selling-assembling-and-shipping-kits.md#prepare-sample-data).   -->

## Scenario

Op 23 januari neemt Susan, de verkooporderprocessor, een order uit de onderdelenwinkel voor drie eenheden van Kit B aan. Dit is een ATO-artikel. Alle drie eenheden worden aangepast en moeten de sterke grafische kaart en een extra RAM-blok bevatten. De schijfstations worden bijgewerkt naar dvd omdat er geen cd-stations beschikbaar zijn. Susan weet dat de eenheden meteen kunnen worden samengevoegd, dus laat ze de voorgestelde verzenddatum op 23 januari staan.  

Tegelijkertijd bestelt de klant vijftien eenheden van Kit A met een speciaal verzoek dat vijf eenheden moeten worden aangepast en voorzien van de sterke grafische kaart. Hoewel Kit A meestal een artikel voor assembleren uit voorraad is, combineert de orderverwerker de verkoopregelaantallen om tien eenheden uit voorraad te verkopen en vijf aangepaste eenheden voor de order samen te stellen. De tien eenheden van Kit A zijn niet beschikbaar en moeten eerst worden geleverd op voorraad via een assemblageorder op basis van het assemblagebeleid van het artikel. Susan hoort van de assemblageafdeling dat Kit A-eenheden niet kunnen worden voltooid in de huidige week. Zij stel de verzenddatum van de tweede verkooporderregel, voor het gemengde ATO- en voorraadaantal, in op 27 januari en meldt aan de klant dat de 15 eenheden van Kit A vier dagen later worden verzonden dan de drie eenheden van Kit B. Teneinde aan de verzendafdeling te melden dat voor deze verkooporder assemblageverwerking is vereist, maakt Susan het magazijnverzendingsdocument vanuit de verkooporder.  

Edward, de planner voert het planningsvoorstel uit en genereert een assemblageorder voor tien standaardeenheden van Kit A met een interne vervaldatum van 27 januari.  

Sammy, die verantwoordelijk is voor de verzending, ontvangt drie magazijnverzendingsregels voor de verkooporder: één regel voor de drie zuivere ATO-eenheden, één regel voor de vijf ATO-eenheden op de gemengde verkooporderregel en één regel voor de tien ATS-eenheden op de gemengde verkooporderregel. Hij maakt een magazijnpickdocument voor alle assemblage onderdelen die nodig zijn voor het samenstellen van het totaal van acht ATO-eenheden op het magazijnverzendingsdocument.  

John, de picker, haalt onderdelen voor alle ATO-hoeveelheden op van het magazijnverzendingsdocument en brengt deze naar het assemblagegebied. Hij voert de te verwerken hoeveelheid en registreert de magazijnpick.  

Linda assembleert de drie ATO-eenheden van Kit B. De onderdelen zijn al gepickt en zij legt niet de uitvoer- en verbruikhoeveelheden vast en boekt niet de order, omdat beide acties automatisch worden uitgevoerd via de bijbehorende magazijnverzendingsregels.  

Sammy legt de geassembleerde hoeveelheid vast op de magazijnverzendingsregel en boekt de verzending van de drie eenheden van Kit B. De eerste regel op de verkooporder wordt bijgewerkt als verzonden. De gekoppelde assemblageorder blijft open totdat de verkooporder volledig is gefactureerd. De twee magazijnverzendingsregels, één ATO en één ATS, voor Kit A met vervaldatum op 27 januari blijven open.  

Op 27 januari verwerkt Linda twee assemblageorders voor kit A. De eerste order is de ATO-order voor vijf eenheden, die ze op andere wijze verwerkt dan de ATO-order voor kit B, die ze op 23 januari heeft verwerkt. Voor deze order is ze gemachtigd om zelf de magazijnverzendingsregel te openen en het voltooide assemblagewerk vast te leggen. De benodigde materialen zijn beschikbaar op de assemblageafdeling, aangezien zij zijn gepickt met de onderdelen voor Kit B.  

De tweede assemblageorder is de ATS-order voor tien eenheden die is gemaakt door het planningssysteem. Op deze ATS-order voert Linda alle betrokken acties uit vanaf de assemblageorder. Zij maakt een magazijnpickdocument voor de assemblageonderdelen die nodig zijn voor het samenstellen van de tien eenheden. Wanneer de pc's zijn geassembleerd, boekt Linda de assemblageorder en geeft daarmee aan dat de artikelen op voorraad zijn en kunnen worden gepickt voor verzending.  

Sammy maakt een magazijnpickdocument voor alle resterende hoeveelheden voordat de magazijnverzending kan worden geboekt. Er wordt een pickdocument gemaakt voor de tien eenheden van Kit A die zojuist zijn voltooid. De onderdelen die nodig zijn voor op order assembleren van de vijf eenheden van Kit A zijn gepickt op 23 januari.  

John brengt de tien eenheden van Kit A vanuit het magazijn naar het opgegeven verzendgebied, legt de te verwerken hoeveelheid vast en registreert vervolgens de pick.  

Sammy pakt de tien ATS-eenheden in met de vijf ATO-eenheden die Linda eerder die dag heeft geassembleerd. Hij vult de te leveren hoeveelheid op beide regels in en boekt vervolgens de laatste verzending voor de Onderdelenwinkel. De gerelateerde assemblageorder voor vijf eenheden van Kit A wordt automatisch geboekt. De tweede regel op de verkooporder wordt bijgewerkt als verzonden. The gekoppelde assemblageorder blijft open totdat de verkooporder volledig is gefactureerd en gesloten.  

Wanneer de verkooporder later als volledig gefactureerd wordt geboekt, worden de verkooporder en de gekoppelde assemblageorders verwijderd.  

## Voorbeeldgegevens voorbereiden

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Mag.-artikeldagboeken** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies het veld **Batchnaam** en selecteer vervolgens het standaarddagboek.  
3.  Maakt positieve voorraadherwaarderingen bij vestiging WIT op de werkdatum, 23 januari, door de volgende informatie in te voeren.  

    |**Artikelnr.**|**Zone**|**Opslaglocatie**|**Aantal**|  
    |-----------------------------------|---------------------------------------|--------------------------------------|------------------------------------|  
    |80001|PICK|W-01-0001|20|  
    |80005|PICK|W-01-0001|20|  
    |80011|PICK|W-01-0001|20|  
    |80014|PICK|W-01-0001|20|  
    |80203|PICK|W-01-0001|20|  
    |80209|PICK|W-01-0001|20|  

4.  Kies de actie **Registreren** en kies vervolgens de knop **Ja**.  

    Synchroniseer vervolgens de nieuwe magazijnposten met de voorraad.  

5.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikeldagboeken** in en kies vervolgens de gerelateerde koppeling. De pagina **Artikeldagboek** wordt geopend.  
6.  Kies de actie **Magazijnherwaardering berekenen**.  
7.  Klik op de pagina **Magazijnherwaardering berekenen** op de knop **OK**.  
8.  Kies op de pagina **Artikeldagboek** de actie **Boeken** en kies vervolgens de knop **Ja**.  

### De assemblageartikelen maken  

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Nieuw**.  
3.  Maak het eerste assemblageartikel op basis van de volgende gegevens.  

    |Veld|Waarde|  
    |---------------------------------|-----------|  
    |**Beschrijving**|Kit A – Basis-pc|  
    |**Basiseenheid**|Stuks|  
    |**Artikelcategoriecode**|Diversen|  
    |**Aanvullingsmethode**|Assemblage|  
    |**Assemblagebeleid**|Op voorraad assembleren|  
    |**Bestelbeleid**|Lot-for-Lot|  

    > [!NOTE]  
    >  Kit A wordt doorgaans geleverd via assembleren op voorraad en heeft daarom een bestelbeleid waardoor het onderdeel vormt van de algemene voorraadplanning.  

4.  Kies de actie **Assembleren** en kies vervolgens **Assemblagestuklijst**.  
5.  Definieer een assemblagestuklijst voor Kit A met de volgende gegevens.  

    |**Soort**|**Nr.**|**Aantal per**|  
    |-------------------------------|------------------------------|---------------------------------------|  
    |Artikel|80001|1|  
    |Artikel|80011|1|  
    |Artikel|80209|1|  
    |Bron|Tsing|1|  

6.  Maak het tweede assemblageartikel op basis van de volgende gegevens.  

    |Veld|Waarde|  
    |---------------------------------|-----------|  
    |**Beschrijving**|Kit B – Pro pc|  
    |**Basiseenheid**|Stuks|  
    |**Artikelcategoriecode**|Diversen|  
    |**Aanvullingsmethode**|Assemblage|  
    |**Assemblagebeleid**|Op order assembleren|  

    > [!NOTE]  
    >  Kit B wordt gewoonlijk geleverd via assemblage op order en heeft daarom geen bestelbeleid, omdat deze geen deel mag uitmaken van de algemene voorraadplanning.  

7.  Kies de actie **Assembleren** en kies vervolgens **Assemblagestuklijst**.  
8.  Definieer een assemblagestuklijst voor Kit B met de volgende gegevens.  

    |**Soort**|**Nr.**|**Aantal per**|  
    |-------------------------------|------------------------------|---------------------------------------|  
    |Artikel|80005|1|  
    |Artikel|80014|1|  
    |Artikel|80210|1|  
    |Bron|Tsing|1|  

### De assemblageartikelen verkopen  

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Nieuw**.  
3.  Maak twee verkooporderregels voor klant 62000, de Onderdelenwinkel, op de werkdatum met de volgende informatie.  

    |**Soort**|**Beschrijving**|**Aantal**|Op order te assembleren aantal|Verzenddatum|  
    |--------------|---------------------|------------------|-------------------------------|-------------------|  
    |Artikel|Kit B – Pro pc|3|3|23 januari|  
    |Artikel|Kit A – Basis-pc|15|5|27 januari|  

    > [!NOTE]  
    >  Het volgende beschikbaarheidsprobleem bestaat voor de verkooporderregel voor Kit B:  
    >   
    >  -   Assemblageonderdeel 80210 is niet beschikbaar. Dit betekent dat de drie opgegeven eenheden van kit B niet kunnen worden geassembleerd. Dit wordt aangegeven met **0** in het veld **Mogelijk te assembleren** op de pagina **Beschikbaarheid assemblage**.  
    >   
    >  Het volgende beschikbaarheidsprobleem bestaat voor de verkooporderregel voor Kit A:  
    >   
    >  -   De tien eenheden van Kit A zijn niet beschikbaar. Dit geeft aan voor de planningssysteem dat de hoeveelheid moet worden geassembleerd op voorraad.  

    Pas vervolgens de verkooporder aan.  

4.  Selecteer de verkooporderregel voor drie eenheden van Kit B.  
5.  Kies op het sneltabblad **Regels** de optie **Regel** en kies vervolgens **Op order assembleren** en **Op orderregels assembleren**.  
6.  Voer op de pagina **Op orderregels assembleren** op de assemblageorderregel voor artikel 80014 in het veld **Aantal per** de waarde **2** in.  
7.  Selecteer in de planningsregel voor artikel 80210 het veld **Nummer**. Selecteer in plaats hiervan artikel 80209.  
8.  Maak een nieuwe assemblageorderregel met de volgende gegevens.  

    |Type|Nr.|Aantal per|  
    |----------|---------|------------------|  
    |Artikel|80203|1|  

9. Sluit de pagina **Op orderregels assembleren**.  

    Werk vervolgens de kostprijs van Kit B bij op basis van de aanpassingen die u zojuist hebt uitgevoerd. Let op de huidige waarde in het veld **Eenheidsprijs excl. btw**.  

10. Kies op het sneltabblad **Regels**, **Regel**, **Op order assembleren** en vervolgnes **Prijs samenvoegen**.  
11. Kies de knop **Ja**. Let op de verhoogde waarde in het veld **Eenheidsprijs excl. btw**.  
12. Selecteer de verkooporderregel voor 15 eenheden van Kit A.  
13. Kies op het sneltabblad **Regels** de optie **Regel** en kies vervolgens **Op order assembleren** en **Op orderregels assembleren**.  
14. Maak op de pagina **Op orderregels assembleren** een nieuwe assemblageorderregel met de volgende gegevens.  

    |Soort|Nr.|Aantal per|  
    |----------|---------|------------------|  
    |Artikel|80203|1|  

     Wijzig vervolgens de verzenddatum van de tweede verkooporderregel op basis van het assemblageschema.  

15. Voer op de verkooporderregel voor 15 eenheden van kit A de waarde **27-01-2014** in het veld **Verzenddatum** in.  
16. Kies de actie **Vrijgeven**.  
17. Kies de actie **Mag.-verzending maken**.  
18. Sluit de verkooporder.  

### Planning voor de niet-beschikbare ATS-artikelen  

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Planningsvoorstel** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Regeneratief plan berekenen**.  
3.  Stel op de pagina **Plan berekenen** de volgende filters in.  

    |Begindatum|Einddatum|Nr.|  
    |-------------------|-----------------|---------|  
    |23-01-2014|27-01-2014|Kit A – Basis-pc|  

4.  Kies de knop **Ok**.  

    Een nieuwe planningsregel wordt gemaakt voor de benodigde assemblageorder van 10 eenheden, die moeten zijn geleverd op 27 januari. Hier hoeft u geen wijzigingen aan te brengen, dus u kunt de order maken.  

5.  Kies de actie **Planningsboodschap uitvoeren**.  
6.  Kies op de pagina **Planningsboodschap uitvoeren** het veld **Assemblageorder** en selecteer vervolgens **Assemblageorders maken**.  
7.  Kies de knop **OK**.  

### Het eerste ATO-aantal assembleren en verzenden  

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Magazijnverzending** in en kies vervolgens de gerelateerde koppeling.  

    > [!NOTE]  
    >  In deze sectie is de persoon die verantwoordelijk is voor de verzending tevens belast met het vastleggen van de voltooide ATO-assemblageactiviteiten op de magazijnverzendingsregel. Deze werkstroom kan optreden in omgevingen waar de assemblageactiviteiten worden uitgevoerd door de persoon die verantwoordelijk is voor verzending of door assemblagemedewerkers op de verzendlocatie.  
    >   
    >  In deze sectie worden acties op de assemblageorder indirect uitgevoerd vanuit de magazijnverzendingsregel. Zie de sectie 'Assemblageartikelen op voorraad' in dit scenario voor meer informatie over het rechtstreeks verwerken van een assemblageorder.  

2.  Open de meest recente magazijnverzending die bij vestiging WIT is gemaakt.  

    Merk op dat er drie magazijnverzendregels zijn: één regel voor het ATO-aantal van kit B, te leveren op 23 januari. Eén regel voor het ATO-aantal van kit A, te leveren op 27 januari. Eén regel voor het voorraadaantal van kit A, te leveren op 27 januari.  

    In het veld **Op order assembleren** wordt de assemblagemethode opgegeven.

    Maak vervolgens een magazijnpickdocument voor alle ATO-assemblageonderdelen die nodig zijn op de magazijnverzending.  

3.  Kies de actie **Pick maken** en kies vervolgens de knop **OK**.  

    Voer vervolgens de taak van de picker uit.  

4.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Picks** in en kies vervolgens de gerelateerde koppeling.  
5.  Open het magazijnpickdocument dat u hebt gemaakt in stap 3 van deze sectie.  

    Let op de waarde in het veld **Brondocument**. Bovendien ziet u dat alle pickregels assemblageonderdelen betreffen.  

    Registreer vervolgens de pick zonder de standaardgegevens te wijzigen.  

6.  Kies de actie **Te verwerken aantal autom. invullen**.  
7.  Kies de actie **Pick registreren**.  

    Ga terug naar het uitvoeren van de verzendtaken.  

8.  Open de pagina **Magazijnverzending** opnieuw.  

    Zoals u ziet, is het veld **Gepickt aantal** nog steeds leeg op alle regels. Dit komt doordat u de te verzenden artikelen nog niet hebt gepickt, maar alleen de onderdelen die nodig zijn voor het assembleren van de ATO-aantallen.  

    Ga door met het bekijke van de bijbehorende assemblageorder.  

9. Selecteer de verzendregel voor drie eenheden van Kit B.  
10. Kies op het sneltabblad **Regels**, de optie **Regel** en kies vervolgens **Op order assembleren**. De pagina **Assemblageorder** wordt geopend.  

    U ziet dat verschillende velden op de assemblageorder niet beschikbaar zijn omdat de order is gekoppeld aan een verkooporder.  

    Zoals u ziet, is het veld **Gepickt aantal** op de assemblageorderregels ingevuld. Dit komt door de pick die u hebt geregistreerd in stap 7 van deze sectie.  

11. Probeer in het veld **Te assembleren aantal** een waarde in te voeren die lager is dan **3**.  

    Lees het foutmelding waarin wordt uitgelegd waarom dit veld alleen kan alleen worden ingevuld via het veld **Te verzenden aantal** op de bijbehorende zending.  

    Het veld **Te verzenden aantal** is bewerkbaar ter ondersteuning van situaties waarin u een voorraadaantal gedeeltelijk wilt verzenden in plaats van meer eenheden op order te assembleren. Zie voor meer informatie de sectie 'Combinatiescenario's' in [Op voorraad assembleren of Op order assembleren begrijpen](assembly-assemble-to-order-or-assemble-to-stock.md).  

12. Sluit de pagina **Assemblageorder** en ga terug naar de pagina **Mag. -verzending**.  
13. Voer op de verzendregel voor de drie eenheden van kit B in het veld **Te verzenden aantal** de waarde **3** in.  
14. Kies de actie **Verzending boeken** en selecteer de knop **Verzending**.  

    Bij deze boeking van een magazijnverzending wordt het volledige verbruiks- en outputaantal van de bijbehorende assemblageorder geboekt, en is het veld **Resterend aantal** leeg. De verkooporderregel voor Kit B wordt bijgewerkt om aan te geven dat de drie eenheden zijn verzonden.  

    Er worden magazijnactiviteiten uitgevoerd om de eerste verkooporderregel op 23 januari te vervullen. Vervul daarna de verkooporderregels die op 27 januari worden verzonden  

### De tweede ATO-hoeveelheid assembleren en vastleggen  

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Assemblageorders** in en kies vervolgens de gerelateerde koppeling  

    Merk op dat de ATO-order voor verzonden eenheden voor kit B nog steeds in de lijst staat, hoewel het veld **Resterend aantal** leeg is. Dit komt omdat de gekoppelde verkooporder nog steeds niet volledig is gefactureerd.  

    > [!NOTE]  
    >  In deze sectie is de assemblagemedewerker verantwoordelijk voor het vastleggen van de voltooide ATO-assemblageactiviteiten op de magazijnverzendingsregel. Deze werkstroom kan optreden in omgevingen waar de assemblageactiviteiten worden uitgevoerd op een aparte assemblageafdeling en assemblagemedewerkers geautoriseerd zijn om de magazijnverzendingsregel te wijzigen.  

2.  Open de ATO-assemblageorder voor vijf eenheden van Kit A.  

    Merk op dat de velden **Te assembleren aantal** en **Te verbruiken aantal** leeg zijn, omdat er nog geen werk is geregistreerd.  

    Zoals u ziet, is het veld **Gepickt aantal** op de assemblageorderregels ingevuld. Dit komt door de pick die werd geregistreerd op 23 januari.  

    Leg vervolgens vast dat de assemblageorder is voltooid.  

3.  Kies de actie **Magazijnverzendregel op order assembleren**.  
4.  Voer op de pagina **Magazijnverzendregel op order assembleren** in het veld **Te verzenden aantal** de waarde **5** in en sluit vervolgens de pagina.  

    U ziet op de pagina **Assemblageorder** dat de velden **Te assembleren aantal** en **Te verbruiken aantal** nu zijn gevuld met de output- en verbruiksaantallen die worden geboekt op de verzending.  

5.  Sluit de pagina **Assemblageorder**.  

### Het ATS-aantal assembleren  

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Assemblageorders** in en kies vervolgens de gerelateerde koppeling  
2.  Open de assemblageorder voor tien eenheden van Kit A.  

    Merk op dat het veld **Te assembleren aantal** wordt gevuld met het verwachte aantal.  

    Maak vervolgens een pickdocument voor het ophalen van de benodigde onderdelen.  

3.  Kies de actie **Vrijgeven**.  
4.  Kies de actie **Magazijnpick maken** en kies de knop **OK**.  

    Voer vervolgens de taak van de picker uit.  

5.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Picks** in en kies vervolgens de gerelateerde koppeling.  
6.  Open het magazijnpickdocument dat u hebt gemaakt in stap 4 van deze sectie.  

     Registreer vervolgens de pick zonder de standaardgegevens te wijzigen.  

7.  Kies de actie **Te verwerken aantal autom. invullen**.  
8.  Kies de actie **Pick registreren**.  

    Ga terug naar de assemblageorder om de laatste assemblagetaak uit te voeren.  

9. Kies in **Assemblageorder** de actie **Boeken** en kies vervolgens de knop **Ja**.  

    Zoals u ziet, wordt de assemblageorder verwijderd uit de lijst met openstaande orders.  

### De overige artikelen verzenden gedeeltelijk uit voorraad en gedeeltelijk geassembleerd op de order  

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Magazijnverzending** in en kies vervolgens de gerelateerde koppeling.  
2.  Open de meest recente magazijnverzending die bij vestiging WIT is gemaakt.  

    Zoals u ziet, zijn de velden **Te verzenden aantal** en **Gepickt aantal** leeg op de regel voor tien eenheden van kit A.  

    Pick vervolgens de resterende artikelen.  

3.  Kies de actie **Pick maken** en kies vervolgens de knop **OK**.  

    Voer daarna de laatste taak van de picker uit voor deze magazijnverzending.  

4.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Picks** in en kies vervolgens de gerelateerde koppeling.  
5.  Open het magazijnpickdocument dat u hebt gemaakt in stap 3 van deze sectie.  

    Zoals u ziet, is deze pickdocument bedoeld voor assemblageartikelen niet voor assemblageonderdelen.  

    Registreer vervolgens de pick zonder de standaardgegevens te wijzigen.  

6.  Kies de actie **Te verwerken aantal autom. invullen**.  
7.  Kies de actie **Pick registreren** en kies vervolgens de knop **Ja**.  

    Ga terug naar de magazijnverzending om de laatste taak uit te voeren.  

8.  Open de pagina **Magazijnverzending** opnieuw.  

    Op de pagina **Mag. -verzending** op de regel voor tien eenheden van kit A ziet u dat de velden **Te verzenden aantal** en **Gepickt aantal** nu de waarde **10** bevatten.  

9. Kies de actie **Verzending boeken** en kies de knop **Verzending**.  

    Het magazijnverzendingsdocument wordt verwijderd, waarmee wordt aangegeven dat de betrokken magazijnactiviteiten zijn voltooid. Controleer vervolgens of de verkooporder is verwerkt.  

10. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling  
11. Open de verkooporder voor de Onderdelenwinkel.  

    Merk op dat op beide regels het veld **Verzonden aantal** het volledige aantal bevat.  

    Wanneer de Onderdelenwinkel betaalt voor de ontvangst van de 18 pc's uit CRONUS, worden de verkooporder en de gekoppelde assemblageorders verwijderd.  

## Zie gerelateerde [Microsoft-training](/training/paths/assemble-items-dynamics-365-business-central/)

## Zie ook

 [Op voorraad assembleren of Op order assembleren begrijpen](assembly-assemble-to-order-or-assemble-to-stock.md)   
 [artikelen samenstellen](assembly-how-to-assemble-items.md)   
 [Picken van artikelen voor magazijnverzending](warehouse-how-to-pick-items-for-warehouse-shipment.md)   
 [Assembleren voor order-artikelen verkopen](assembly-how-to-sell-items-assembled-to-order.md)   
 [artikelen samenstellen](assembly-how-to-assemble-items.md)   
 [Ontwerpdetails: Assemblageorderboeking](design-details-assembly-order-posting.md)   
 [Ontwerpdetails: Inkomende magazijnstromen](design-details-internal-warehouse-flows.md)   
 [Ontwerpdetails: Uitgaande magazijnstroom](design-details-outbound-warehouse-flow.md)   
<!--  [Walkthrough: Planning Supplies Automatically](walkthrough-planning-supplies-automatically.md) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]
