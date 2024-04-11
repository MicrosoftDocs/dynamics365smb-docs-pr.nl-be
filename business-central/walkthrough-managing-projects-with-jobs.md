---
title: 'Procedure: Projecten plannen met taken'
description: Deze procedure laat u kennismaken met de projectbeheerfuncties in projecten waarmee u het gebruik van de resources van uw bedrijf en meer kunt plannen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Procedure: Projecten plannen

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

In deze procedure maakt u kennis met de functies voor projectbeheer. Projecten zijn een manier waarop u het verbruik van de bedrijfsresources kunt plannen en de diverse kosten kunt bijhouden die samenhangen met de resources voor een bepaald project. Projecten brengen het verbruik met zich mee van arbeidsuren, machine-uren, voorraadartikelen en andere soorten verbruik die u mogelijk wilt bijhouden terwijl het project voortduurt.  

 In deze procedure wordt het instellen van een nieuw project behandeld en komt een aantal algemene taken aan de orde zoals het werken met vaste prijzen, in termijnen betalen, facturen boeken voor projecten en projecten kopiëren.  

## Informatie over deze procedure

 In deze procedure worden de volgende taken gedemonstreerd:  

### Een project instellen

 Als de budgetstructuur voor projecten is ingesteld, is het eenvoudig om een project te maken. Dit scenario omvat de volgende procedures:  

- Projecttaakregels en planningsregels instellen.  
- Projectspecifieke prijzen voor artikelen, resources en grootboekrekeningen.  
- Factureren vanuit een project.  

### Werken met vaste prijzen

 U kunt werken met vaste prijzen en prijzen voor services of goederen die van tevoren zijn overeengekomen met de klant. In dit scenario kunt u het volgende doen:  

- Bekijken hoe contractuele en gefactureerde waarden worden vastgesteld.  
- Extra (niet gefactureerd) werk dat niet is gefactureerd, in het schema opnemen.  

### Een project kopiëren

 In dit deel van het overzicht wordt besproken hoe u een project geheel of gedeeltelijk kunt kopiëren om het handmatig invoeren van gegevens te beperken en de nauwkeurigheid te verhogen. Dit omvat het volgende:  

- Een deel van een project kopiëren naar een nieuw project.  
- Projectspecifieke prijzen kopiëren.  
- Planningsregels kopiëren.  

### Betalen in termijnen

 Als een groot, duur project lang doorloopt, spreekt de klant vaak met het bedrijf af om in termijnen te betalen. In dit scenario ziet u hoe betaling in termijnen instelt aan de hand van de volgende onderwerpen:  

- Betalingen in termijnen opzetten voor een project.  
- Betalingen aan klanten factureren.  
- Verbruik verantwoorden in een project met termijnbetalingen.  

## Rollen

 Deze procedure bevat taken voor de volgende rollen:  

- Projectmanager  
- Lid van het projectteam  

## Vereisten

 Voordat u de stappen in deze procedure kunt uitvoeren, moet u het volgende doen:  

- Installeer de CRONUS-demonstratiedatabase.
- Maak voorbeeldgegevens met behulp van de stappen in het volgende gedeelte.  

## Scenario

Dit overzicht draait om CRONUS, een design- en consultancyfirma die nieuwe infrastructuren ontwerpt en installeert, zoals conferentiezalen, kantoren, meubels, accessoires en opslagruimten. Het bedrijf werkt meestal met projecten. Prakash, een projectmanager bij CRONUS gebruikt projecten om een overzicht te krijgen van alle lopende taken die met CRONUS zijn gestart, alsmede van de taken die zijn afgerond. Prakash is gewoonlijk degene die afspraken met klanten maakt en het grootste deel van het project, zoals taak- en planningsregels en prijzen, invoert in [!INCLUDE[prod_short](includes/prod_short.md)]. Prakash constateert dat het maken, onderhouden en redigeren van informatie eenvoudig is. Prakash is tevens te spreken over de manier waarop projecten kunnen worden gekopieerd in [!INCLUDE[prod_short](includes/prod_short.md)] en de mogelijkheid om te betalen in termijnen.

 Tricia, een lid van het projectteam dat aan Prakash rapporteert, is verantwoordelijk voor de dagelijkse controle van het project. Tricia voert naast de werkzaamheden van technici bij elke taak ook haar eigen werk in, registreert de artikelen die ze hebben gebruikt en de kosten die ze hebben gemaakt.  

## Voorbeeldgegevens voorbereiden

 Voordat u met dit scenario begint, moet u Tricia toevoegen als een nieuwe resource.  

### De voorbeeldgegevens voorbereiden  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Resources** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw** om een nieuwe resourcekaart te maken.  
3. Voer op het sneltabblad **Algemeen** de volgende informatie in:  

    - **Nr.**: **Tricia**  
    - **Naam**: **Tricia**  
    - **Soort**: **Persoon**  

4. Kies het veld **Basiseenheid** en kies de actie **Nieuw** om de pagina **Resource-eenheid** te openen. Selecteer **Uur** in het veld **Code**.  
5. Typ in het sneltabblad **Facturering** de volgende gegevens:  

    - **Directe kostprijs**: **5**  
    - **Indirecte kosten %**: **4**  
    - **Kostprijs**: **10**  
    - **Productboekingsgroep**: **Services**  
    - **BTW-productboekingsgroep**: **VAT 25**  

6. De pagina sluiten.

In de volgende procedure maakt u een projectdagboekbatch voor Tricia om het gebruik ervan te boeken.  

### Een projectdagboekbatch maken  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projectdagboeken** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Projectdagboek** het veld **Batchnaam**. De pagina **Projectdagboekbatches** wordt geopend.  
3. Kies de actie **Nieuw** om een nieuwe regel te maken met de volgende informatie:  

    - **Naam**: **Tricia**  
    - **Omschrijving**: **Tricia**  
    - **Nr.-reeks**: **JJNL-GEN**  

4. Kies de knop **OK** om de wijzigingen op te slaan.

## Een project instellen

 In dit scenario heeft CRONUS een contract binnengehaald van de klant Progressive Home Furnishings voor het ontwerpen van een conferentie- en eetzaal. De klant is gevestigd in de Verenigde Staten en voor het project is speciale software nodig. De projectmanager komt tot overeenstemming met de klant en maakt een project dat deze afspraak dekt.  

### Een project instellen  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Projecten** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw** om een nieuwe kaart te maken.  
3. Voer op het sneltabblad **Algemeen** de volgende informatie in:  

    - **Omschrijving**: **Adviseren over de inrichting van een conferentiezaal**  
    - **Factureren aan**: **01445544**  

4. Typ op het sneltabblad **Boeking** de volgende gegevens:  

    - **Status**: **Planning**  
    - **Projectboekingsgroep**: **Instellen**  
    - **OHW-methode**: **Kostprijs**  

5. Geef op het sneltabblad **Duur** de datum van vandaag op in de velden **Begindatum** en **Einddatum**. Deze datums zijn belangrijk voor het toepassen van de valutakoers wanneer het project wordt gefactureerd.  
6. Controleer of in het sneltabblad **Buitenlandse handel** de valutacode **USD** is ingesteld. Als u USD selecteert in het veld **Factuurvalutacode**, wordt het project in Amerikaanse dollars gefactureerd en alleen gepland in de lokale valuta van CRONUS.  

 U kunt de prijzen voor klanten aanpassen per project, afhankelijk van de overeenkomsten die u hebt ingesteld. In de volgende procedure geeft de projectmanager kosten op voor Tricia's tijd, stelt hij de prijs voor de vereiste software in en voegt hij de reiskosten toe die de klant is overeengekomen te betalen.  

### Prijzen aanpassen  

1. Kies vanuit de **Projectkaart** de actie **Resource**.  
2. Geef de volgende gegevens op op de pagina **Resourceprijzen project**:  

    - **Code**: **Tricia**  
    - **Eenheidsprijs**: **20**  

3. De pagina sluiten.  
4. Kies de actie **Artikel**.  
5. Geef de volgende gegevens en aangepaste prijs op op de pagina **Artikelprijzen project**:  

    1. **Artikelnr.**: **80201 (grafisch programma)**  
    2. **Eenheidsprijs**: **200**  

6. De pagina sluiten.  
7. Kies de actie **Grootboekrekening**.  
8. Voer op de pagina **GB-rekeningprijzen project** de volgende informatie en de kosten van reizen in, waarvoor de klant is overeengekomen te betalen, plus 25 procent:  

    1. **Grootboekrekening**: **8430 (reizen)**  
    2. **Kostprijsfactor**: **1,25**  

9. De pagina sluiten.  

 De laatste stappen bij het instellen van een project is het toevoegen van de projecttaken en de planningsregels die deel van elke taak uitmaken. De planningregels bepalen wat aan de klant wordt gefactureerd.  

### Projecttaken toevoegen  

1.  Kies op de kaart **Project** voor het nieuwe project de actie **Projecttaakregels**.  
2.  De volgende tabel beschrijft de informatie die u moet invoeren in de velden.  

    |Projecttaaknr.|Omschrijving|Projecttaaktype|  
    |------------------|---------------------------------------|-------------------|  
    |1000|Adviezen voor zaalontwerp|Begintotaal|  
    |1010|Bespreking met klant|Rekening|  
    |1020|Ontwikkeling|Rekening|  
    |1090|Consultancy totaal|Eindtotaal|  

3.  Kies de actie **Projecttaken inspringen** om te laten zien dat sommige taken subcategorieën van andere taken zijn.  

 De volgende soorten planningsregel zijn beschikbaar:  

- **Budget**: wordt toegevoegd aan de planning, maar niet gefactureerd.  
- **Factureerbaar**: gefactureerd, maar niet toegevoegd aan de planning.  
- **Budget en factureerbaar**: gefactureerd en toegevoegd aan de planning.  

 In dit scenario maakt de projectmanager gebruik van **Budget en factureerbaar**. Ze maken drie planningsregels voor taak 1010 en twee planningsregels voor taak 1020.  

### Planningsregels maken  

1. Selecteer regel 1010 en kies vervolgens de actie **Projectplanningsregels**.  

2. Maak planningsregels met de volgende informatie:  

    | Regel | Regelsoort | Planningsdatum  | Soort        | Nee.   | Aantal | Eenheidsprijs |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Zowel Budget als Factureerbaar | (datum van vandaag) | Bron | Tricia | 40        |     |
    | 2    | Zowel Budget als Factureerbaar | (datum van vandaag) | Bron | Timothy | 40        |     |
    | 3    | Zowel Budget als Factureerbaar | (datum van vandaag) | Grootboekrekening | 8430 (reizen) | 2 | 400    |

     De pagina sluiten. De totalen worden bijgewerkt op de pagina **Projecttaakregels**.  
3. Selecteer regel 1020 en kies vervolgens de actie **Projectplanningsregels**. Geef de volgende informatie op:  

    | Regel | Regelsoort | Planningsdatum  | Soort        | Nee.   | Aantal | Eenheidsprijs |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Zowel Budget als Factureerbaar | (datum van vandaag) | Bron | Tricia | 80        |     |
    | 2    | Zowel Budget als Factureerbaar | (datum van vandaag) | Artikel | 80201 (Grafisch programma) | 1 |     |

4. De pagina sluiten. De totalen worden bijgewerkt op de pagina **Projecttaakregels**.  

## Resterend gebruik berekenen

 Tricia, het projectlid van het team, is al een tijdje aan het werk en wil de uren en gebruik tijdens het project registreren. Tricia heeft niet meer uren gewerkt dan van tevoren met de klant is afgesproken. Tricia gebruikt de batchverwerking **Resterend gebruik berekenen** om het resterende verbruik voor het project te berekenen in een projectdagboek. De batchverwerking berekent voor elke projecttaak het verschil tussen het geplande gebruik van artikelen, resources en grootboekkosten en het werkelijke gebruik dat in de projectposten is geboekt. Het resterende gebruik kan zij vervolgens boeken vanuit het projectdagboek waarin het wordt weergegeven.  

### Het resterende gebruik berekenen  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projectdagboeken** in en kies vervolgens de gerelateerde koppeling.  
2. Open op de pagina **Projectdagboek** in het veld **Batchnaam** de lijst **Projectdagboekbatches**. Selecteer de projectdagboekbatch **Tricia**.  
3. Kies de actie **Resterend gebruik berekenen**.  
4. Kies op de pagina **Resterend projectgebruik berekenen** op het sneltabblad **Projecttaak** het veld **Projectnr.** en selecteer het relevante projectnummer, doorgaans J00010.  
5. Typ **J00001** in het veld **Document nr.** op het sneltabblad **Opties**. Zo kunt u toekomstige boekingen gemakkelijker bijhouden.  
6. Voer de datum van vandaag in als de boekingsdatum.  
7. Kies de knop **Ok**. Hiermee genereert u projectdagboekregels die zijn gebaseerd op de planningsregels die Prakash heeft gemaakt.  
8. Kies de knop **OK** op de bevestigingspagina. De gegenereerde regels worden toegevoegd aan het projectdagboek.  
9. Controleer of alle documentnummers J00001 zijn. Kies vervolgens de actie **Boeken**. Kies **Ja** om de boeking te bevestigen.  

De regels worden nu geboekt.  

## Een projectverkoopfactuur maken en boeken

 Tricia kan vervolgens een nieuwe factuur maken voor het hele project of voor een deel van een project. Tricia kan de factuur ook aan een andere factuur voor dezelfde klant en voor hetzelfde project koppelen. In dit geval factureert Tricia voor het volledige project, aangezien het project nu is voltooid.  

### Een projectverkoopfactuur maken  

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Projecten** in en kies vervolgens de gerelateerde koppeling.  
2.  Selecteer het project dat u eerder hebt gemaakt en kies de actie **Projectverkoopfactuur maken**.  
3.  Schakel op het sneltabblad **Projecttaak** alle filters voor **Projecttaaknr.** uit om het project te factureren. Kies in het veld **Projectnr.** het relevante project.  
4.  Vul op het sneltabblad **Opties** de boekingsdatum in en of u één factuur per taak wilt maken of slechts één factuur voor alle taken.  
5.  Kies de knop **OK** om de factuur te maken en kies vervolgens de knop **OK** op de bevestigingspagina.  

 Nadat Tricia de factuur heeft gemaakt, heeft ze hiertoe toegang vanuit bijvoorbeeld het Rolcentrum van de **Verkooporderverwerker**. 

### Een nieuwe verkoopfactuur boeken  

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopfacturen** in en kies vervolgens de gerelateerde koppeling.  
2.  Open de factuur voor klantnr. 01445544. U ziet de gegevens die zijn ingevoerd op de planningsregels.  
3.  Kies de actie **Boeken**. Kies **Ja** om de boeking te bevestigen.  

### De geboekte factuur weergeven  

1.  Open het project en kies vervolgens de actie **Projectplanningsregels**.  
2.  Selecteer een van de planningsregels die zijn gefactureerd en kies de actie **Verkoopfactuur/creditnota**.
3. Kies op de pagina **Projectfacturen** de actie **Verkoopfactuur/creditnota openen**.  

 Als Tricia een vraag heeft over de prijzen, de kosten en de winst die relevant zijn voor dit specifieke project, kan Tricia deze informatie opvragen op de pagina **Statistiek**.  

### De pagina Statistiek openen  

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Projecten** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Statistieken**. U kunt gedetailleerde informatie over de projectprijzen, -kosten en -winsten bekijken in zowel lokale als vreemde valuta's.  
3.  Kies de knop **Sluiten** om de pagina **Projectstatistiek** te sluiten.  

## Werken met vaste prijzen

 CRONUS heeft een contract afgesloten voor het opzetten van vergaderruimten. Als projectleider wil Prakash een goed overzicht hebben van de taken die nodig zijn voor het project met de bijbehorende gebudgetteerde en gemaakte kosten voor elke taak. Bovendien wil Prakash weten wat de totale contractprijs voor het project is en wat het bedrag is dat tot nu toe is gefactureerd. Ze hebben met de klant een vaste prijs voor een project afgesproken.  

### Vaste prijzen beheren in projecten  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Projecten** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer het projectnummer **Guildford** en kies de actie **Projecttaakregels**.  
3. Selecteer regel 1120 en klik in het veld **Budget (totale kostprijs)** met de rechtermuisknop op het bedrag en kies **DrillDown**.  

     Door de projectplanningsregels te bekijken, is vastgesteld dat Prakash ook Tricia gedurende 30 uur nodig heeft voor deze fase van het project. Prakash spreekt een vaste prijs af met de klant.  

4. Selecteer op de pagina **Projecttaakregels** regel 1120 en kies de actie **Projectplanningsregels**. Maak een planningsregel met de volgende informatie:  

    | Regel | Regelsoort | Soort        | Nee.   | Aantal |
    |------|-----------|-------------|-------|----------|
    | 1    | Zowel Budget als Factureerbaar  | Bron | Tricia | 30 |

     Sluit de pagina.  
5. Klik met de rechtermuisknop in het veld **Budget (totale kostprijs)** en kies opnieuw **Drilldown** op de pagina **Projecttaakregels**. Geef de wijzigingen in de planning weer. U ziet dat de 30 uur aan de planning zijn toegevoegd.  
6. Sluit de pagina's.  

Na te zijn toegevoegd aan het schema voor deze taakregel, werkt Tricia 25 uur aan het project en voert deze uren in het projectdagboek in.  

### Uren invoeren in het projectdagboek  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Projectdagboeken** in en kies vervolgens de gerelateerde koppeling.  
2. Maak een nieuwe regel met de volgende informatie:  

    - **Regelsoort**: **(blanco)**  
    - **Boekingsdatum**: **(datum van vandaag)**  
    - **Documentnr.**: **J00002**  
    - **Projectnr.**: **Guildford**  
    - **Projecttaaknr.**: **1120**  
    - **Soort**: **Bron**  
    - **Nr.**: **Tricia**  
    - **Aantal**: **25**  

3. Kies de actie **Boeken**.  

     Een paar dagen later werkt Tricia nog 10 uur aan het project en heeft er nu in totaal 35 uur aan gewerkt. Aangezien 30 uur zijn afgesproken met de klant, worden slechts vijf uur aan de klant in rekening gebracht. Tricia voegt de vijf extra gewerkte uren handmatig toe aan het schema.  

4. Kies op de pagina **Projectdagboek** de actie **Resterend gebruik berekenen**.  
5. Voer op de pagina **Resterend projectgebruik berekenen** de volgende informatie in op het sneltabblad **Opties**:  

    - **Documentnr.**: **J00003**  
    - **Boekingsdatum**: **(datum van vandaag)**  

6. Voer het volgende in op het sneltabblad **Projecttaak**:  

    - **Projectnr.**: **Guildford**  
    - **Projecttaaknr.**: **1120**  

7. Kies de knop **OK** om de berekening uit te voeren.

    Er zijn vijf uur werk die resteren voor Tricia. Het veld **Regelsoort** is leeg, wat betekent dat alleen het gebruik nog moet worden geboekt omdat het werk al is gepland.  

8. Maak in het venster **Projectdagboek** een nieuwe regel met de volgende gegevens. Zorg ervoor dat beide projectnummers opeenvolgend zijn met de projectnummers die u al hebt gebruikt:  

    - **Regelsoort**: **Budget**  
    - **Projectnr.**: **Guildford**  
    - **Projecttaaknr.**: **1120**  
    - **Soort**: **Bron**  
    - **Nr.**: **Tricia**  
    - **Aantal**: **5**  

     Door **Budget** te kiezen als regelsoort werkt het programma de geplande kosten en prijzen bij zonder de contractkosten en prijzen aan te passen die aan de klant worden gefactureerd.  

9. Kies de actie **Boeken**. Kies de knop **OK** om de pagina te sluiten.  
10. Open het overzicht **Projecten**.  
11. Selecteer de GUILDFORD-taak en selecteer vervolgens in het gedeelte **Projecttaakregels** regel 1120 en klik in het veld **Budget (totale kosten)** met de rechtermuisknop op het bedrag. Kies **Drilldown** om de gegevens weer te geven.  

     Wijzigingen worden automatisch ingevoerd op de regel voor Projecttaaknr. 1120. In de totale kosten voor gepland werk, zijn vijf extra uren werk door Tricia toegevoegd aan de planning.  

12. Kies de knop **Sluiten** om de pagina te sluiten.  
13. Klik nu met de rechtermuisknop op het bedrag in het veld **Contract (totale kostprijs)** en kies **Drilldown** om de informatie weer te geven.  

In de totale prijs van het contract, zijn alleen de oorspronkelijk afgesproken 30 uur opgenomen aangezien die met de klant zijn overeengekomen.  

## Projecten kopiëren

Prakash heeft een overeenkomst bereikt met de klant Selagorian Ltd om 10 conferentieruimten in te richten. De overeenkomst lijkt op een eerder project. Daarom kan tijd worden bespaard door dat eerdere project te kopiëren.  

Op de pagina **Project kopiëren** kunt u het project en de taakregels selecteren die u wilt kopiëren. U kunt ook kiezen om de bronprojectboekingen te kopiëren, waardoor planningsregels worden gemaakt op basis van het daadwerkelijke gebruik, of u kunt de bronprojectplanningsregels kopiëren, waarmee de oorspronkelijke planningsregels worden gekopieerd naar het nieuwe project. Vervolgens kunt u kiezen welk type planningsregel of boeking u wilt opnemen en alleen datgene selecteren wat relevant is voor dit nieuwe project. Ten slotte kunt u het project selecteren waarnaar u wilt kopiëren, en definiëren of prijzen en aantallen eveneens moeten worden gekopieerd.  

### Een project kopiëren  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projecten** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw** om een nieuw project te maken. Geef de volgende informatie op:  

    - **Omschrijving**: **10 conferentieruimten inrichten**  
    - **Factureren aan**: **20000**  

3. Kies de actie **Projecttaken kopiëren vanuit**.  
4. Voer op de pagina **Projecttaken kopiëren** het volgende in:  

    - **Projectnr.**: **Guildford**  
    - **Van projecttaaknr.**: **1000**  
    - **Bron**: **Projectplanningsregels**  
    - **Incl. planningsregelsoort**: **Budget + Factureerbaar**  
    - **Naar projectnr.**: **Guildford 10 conferentieruimten inrichten**  
    - Selecteer de velden **Dimensies kopiëren** en **Aantal kopiëren**.  

5. Kies de knop **OK** om de taak te kopiëren en kies vervolgens de knop **OK** om de bevestigingspagina te sluiten.  

Door prijzen, projecttaakregels en projectplanningsregels voor twee taken te vergelijken, kunt u zien of de informatie met succes is gekopieerd.  

## Betalen in termijnen

CRONUS heeft net een groot project binnengehaald dat een jaar gaat duren. Omdat hiervoor veel resources nodig zijn, stelt de projectmanager het contract zo in dat de klant een gedeelte van de prijs vooraf betaalt, een tweede deel wanneer het project half is voltooid en de laatste betaling na voltooiing.  

### Een nieuwe rekening instellen  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Rekeningschema** in en kies de gerelateerde koppeling.  
2. Kies op de pagina **Rekeningschema** de actie **Nieuw** om een nieuwe kaart te maken.  
3. Geef op de kaart **Nieuwe grootboekrekening** de volgende gegevens op:  

    - **Nr.**: **40255**  
    - **Naam**: **Projectbetaling**  

4. Selecteer op het sneltabblad **Boeken** in het veld **Prod.-boekingsgroep** de optie **Services**. Sluit de pagina.  
5. Selecteer op de pagina **Rekeningschema** de optie **Nr. 40255 Projectbetaling** en kies de actie **Inspringen**. Kies **Ja** om te bevestigen.  

De volgende procedures laten zien hoe u een nieuw project kunt maken, prijzen kunt instellen en vervolgens betaling in termijnen kunt instellen. U kunt in de projecttaakregels specifieke regels opnemen voor de betalingen in termijnen. Al het voltooide werk voor het project dat aan de planning wordt toegevoegd, wordt op de verbruiksregels ingevoerd. Voor elke betalingstaakregel in de planningsregels is de regelsoort **Factureerbaar**, wat betekent dat de klant wordt gefactureerd. Voer een nieuwe regel in voor de aanbetaling. Geef op de taakregel voor verbruik de gegevens op voor de artikelen en resources die in dit project zijn gebruikt. Hierdoor wordt de planning uitgebreid met de arbeidsuren en de artikelen die voor het project zijn gebruikt.  

### Betalen in termijnen  

1. Maak een nieuw project.  
2. Vul op de nieuwe **projectkaart** de volgende gegevens in:  

    - **Omschrijving**: **Opknappen receptie**  
    - **Factureren aan**: **30000**  
    - **Projectboekingsgroep**: **Instellen**  
    - **OHW-methode**: **Kostprijs**  

3. Kies op de projectkaart de actie **Prijzen** en kies vervolgens de actie **Bron**. Geef de volgende informatie op:  

    - **Code**: **Tricia**  
    - **Eenheidsprijs**: **10**  

     De pagina sluiten.  

4. Voeg op de **project**kaart in het gedeelte **Taken** projecttaakregels toe zoals beschreven in de volgende tabel:  

    | Regel | Projecttaaknr. | Omschrijving          | Projecttaaktype |
    |------|--------------|----------------------|---------------|
    | 1    | 1000         | Betaling - Aanbetaling | Boeking       |
    | 2    | 2000         | Gebruik                | Boeking       |
    | 3    | 3000         | Betaling - Halverwege     | Boeken       |
    | 4    | 4000         | Betaling - Voltooiing | Boeking       |

5. Kies taak 1000 en kies vervolgens de actie **Projectplanningsregels**.  

6. Maak een planningsregel met de volgende informatie:  

    | Regel | Regelsoort | Planningsdatum  | Soort        | Nee.   | Aantal | Eenheidsprijs |
    |------|-----------|----------------|-------------|-------|----------|------------|
    | 1    | Factureerbaar  | (datum van vandaag) | Grootboekrekening | 40255 | 1        | 5000       |

     De pagina sluiten.  

7. Kies taak 2000 en kies vervolgens de actie **Projectplanningsregels**.  

8. Maak een planningsregel met de volgende informatie:

    | Regel | Regelsoort | Planningsdatum  | Soort     | Nee.    | Aantal |
    |------|-----------|----------------|----------|--------|----------|
    | 1    | Budget    | (datum van vandaag) | Bron | Tricia | 120      |
    | 2    | Budget    | (datum van vandaag) | Artikel     | 70104  | 10       |

     De pagina sluiten. U ziet op de pagina **Projecttaakregels** dat de planningsbedragen zijn bijgewerkt.  

9. Kies taak 32000 en kies vervolgens de actie **Projectplanningsregels**.  

10. Maak een planningsregel met de volgende informatie:

    | Regel | Regelsoort | Planningsdatum   | Soort        | Nee.   | Aantal | Eenheidsprijs |
    |------|-----------|-----------------|-------------|-------|----------|------------|
    | 1    | Factureerbaar  | (een toekomstige datum) | Grootboekrekening | 40255 | 1        | 5000       |

     De pagina sluiten.  

11. Maak een soortgelijke planningsregel voor projecttaak 4000.  

 Nu de taak- en planningsregels zijn ingevoerd kan Prakash een factuur voor de eerste betaling maken. Prakash doet dit op basis van de projecttaakregels om er zeker van te zijn dat de factuur alleen de regels voor de eerste betaling bevat. Open de verkooporder vanuit de planningsregels of de taakregels.  

### Een factuur maken  

1.  Selecteer op de pagina **Projecttaakregels** regel 1000 en kies de actie **Verkoopfactuur maken**.  
2.  Stel op de pagina **Verkoopfactuur maken** de datum van vandaag in als de boekingsdatum, geef **Per taak** op en kies de knop **OK** om een factuur te maken met de standaardinformatie. Kies de knop **OK** om de bevestigingspagina te sluiten.  
3.  Kies de actie **Verkoopfactuur/creditnota**. U ziet op de verkoopfactuur dat alleen de aanbetaling in de factuur is opgenomen. Verstuur de factuur nu aan de klant zoals is overeengekomen.  

## Volgende stappen

 In dit scenario heeft u enkele van de basisstappen voor het werken met projecten in [!INCLUDE[prod_short](includes/prod_short.md)] doorlopen. U hebt geleerd over hoe u een nieuw project kunt maken, een project kunt kopiëren en betalingen kunt verwerken. Ook hebt u een demonstratie gekregen van het bijhouden van uren en het opstellen van facturen.  

## Zie ook

 [Procedures voor bedrijfsprocessen](walkthrough-business-process-walkthroughs.md)  
 [Projectbeheer instellen](projects-setup-projects.md)  
 [Resources gebruiken](projects-how-use-resources.md)  
 [Voortgang en prestaties bewaken](projects-how-monitor-progress-performance.md)  
 [Projecten factureren](projects-how-invoice-jobs.md)  
 [Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
