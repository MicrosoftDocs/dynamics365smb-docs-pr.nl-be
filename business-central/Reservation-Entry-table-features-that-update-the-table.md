---
title: Reserveringsinvoertabel - Functies die de reserveringsinvoertabel bijwerken | Microsoft Docs
description: Deze handleiding helpt u bij het begrijpen en oplossen van problemen met inconsistente gegevens in de tabel Reserveringsinvoer.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/26/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# Reserveringsinvoertabel - Inleiding

In dit technische whitepaper vindt u richtlijnen waarmee u problemen met inconsistente gegevens in de tabel  *Reserveringspost*  (tabel 337) in kunt begrijpen en oplossen Microsoft Dynamics NAV. Het eerste deel is een introductie tot de functies die gegevens in deze tabel genereren of wijzigen. Het bestrijkt ook verschillende velden in de tabel  *Reserveringsinvoer* die het vermelden waard zijn in relatie tot deze functies. Het tweede deel laat aan de hand van voorbeelden zien hoe vermeldingen in de tabel  *Reserveringsvermelding* worden gegenereerd, verwijderd of gewijzigd wanneer overdrachtsorders worden verwerkt of planningsfuncties worden uitgevoerd.

De tabel  *Reserveringsinvoer* wordt gebruikt om informatie over reserveringen, artikeltracering en ordertracering te verwerken en op te slaan.

Bij het verwerken van artikeltracering met gedeeltelijke boeking werkt de tabel samen met de tabel  *Trackingspecificaties*  (tabel 336). Gegevens die door de gebruiker op de pagina  **Artikeltraceringsregels**  zijn ingevoerd, worden in een tijdelijke versie van tabel 336 gemaakt en worden vastgelegd in tabel 337 en de traceringsspecificatietabel wanneer de pagina wordt gesloten.

Over het algemeen zijn de gegevens die in de tabel  *Reserveringsinvoer* worden gegenereerd, afhankelijk van welke functies u gebruikt en welke parameters u hebt geselecteerd voor het item kaart. Deze omvatten:

- Beleid voor het volgen van bestellingen
- Reserveringsbeleid
- Planningsfuncties uitgevoerd
- Herbestel- en productiebeleid
- Planningsparameters op het artikel of de voorraadbeheereenheid kaart
- Artikeltraceringscode

## Functies die de reserveringsinvoertabel bijwerken

### Beleid voor het volgen van bestellingen

Als het veld  **Order Tracking Policy** voor een artikel is ingesteld op None, Microsoft Dynamics NAV worden er nooit reserveringsposten aangemaakt in de tabel  *Reserveringspost*, tenzij het Net Change Plan of Regeneratief Plan, Reservering of Artikel Tracking wordt uitgevoerd. Als ordertracking niet is ingeschakeld, kunt u bovendien reserveringsposten hebben wanneer u het beleid Manufacturing-to-Order of Assembly-to-Order gebruikt.

U kunt overwegen om het  **Order Tracking Policy** in te stellen op None als u niet wilt dat vraag en aanbod direct worden vergeleken of andersom. Het vergelijken van aanbod en vraag wordt afgehandeld via de ordertrackingfunctionaliteit of de planningsengine. Wij raden u af om ordertracking te gebruiken in combinatie met planningsfunctionaliteit.

Wanneer u het veld  **Ordertraceringsbeleid** instelt op Alleen traceren, Microsoft Dynamics NAV worden er altijd vermeldingen in tabel 337 gemaakt wanneer er een bestelling voor het artikel wordt gemaakt, maar de **Reserveringsstatus** in tabel 337 wordt niet altijd strikt ingesteld op Traceren. Stel je het volgende scenario voor:

> [!NOTE]  
> Voor alle voorbeelden is de werkdatum ingesteld op 23-01-2014 (MM/DD/JJJJ). 
  
1. Maak een artikel aan met het veld  **Order Tracking Policy** ingesteld op Alleen Tracking.  
1. Inkooporder maken. Microsoft Dynamics NAV zal een reserveringspost aanmaken met de **Reserveringsstatus** Overschot, aangezien de inkooporder nog niet aan een vraag is toegewezen.
1. Een verkooporder maken. Microsoft Dynamics NAV zal nu een nieuwe reserveringsinvoer aanmaken met de status **Tracking** van de reservering.

De **reserveringsstatus** die is gemaakt in stap 2 wordt bijgewerkt naar Tracking; dit wordt Microsoft Dynamics NAV automatisch afgehandeld. Dit concept heet Dynamische Tracking.
Door het veld  **Order Tracking Policy** op het artikel in te stellen op Alleen Tracking, kan een eindgebruiker gebruikmaken van de functie voor ordertracking om een overzicht te krijgen van aan welke levering de vraag is toegewezen en vice versa.

> [!NOTE]  
> De trackingfunctionaliteit vervangt niet de planningsfunctionaliteit. Deze functionaliteit bekijkt alle artikelen, eisen en voorraden samen om optimale planningsvoorstellen te bieden waarmee u het serviceniveau voor klanten kunt optimaliseren en de voorraadniveaus in evenwicht kunt brengen.

### Reserveringsbeleid

Een reservering bestaat uit een paar records in de tabel *Reserveringsinvoer* met de **Reserveringsstatus** Reservering, die hetzelfde invoernummer delen. Eén record heeft het veld Positief ingeschakeld en verwijst naar de levering. In het andere record is het veld  **Positief** niet ingeschakeld en verwijst naar de vraag. De velden **Brontype**, **Bronref.nr.** en **Bron-ID** markeren de reservering koppelen tussen vraag en aanbod.

De informatie in het veld  **Brontype** is de tabel waaraan het reserveringsveld  **Invoernummer** is gekoppeld. Als het bijvoorbeeld een vraagpost (negatief) betreft, kan het de tabel  *Verkooporder* (tabel 37) of de tabel  *Planningcomponent* (tabel 99000829) zijn.

Het veld  **Bron-ID** bevat de ID van het document in de tabel waarnaar wordt verwezen door het brontype.

De **Bron Ref. Nr.** Veld bevat een referentienummer voor de lijn, die de reservering bevat **Invoernummer**  is gerelateerd aan. Als de post betrekking heeft op een verkoop- of inkoopregel, een journaalregel of een aanvraagregel, wordt de informatie in dit veld gekopieerd van de **Lijn nr.** . Als het betrekking heeft op een post in de tabel  *Artikelpost*  (tabel 32), wordt de informatie in dit veld gekopieerd uit het veld  **Postnr.** van de tabel  *Artikelpost* .

Wanneer u de optie Reserveringsbeleid Altijd in combinatie met ordertracking gebruikt, zijn beide normaal gesproken gesynchroniseerd. Wanneer de reservering echter wordt verwijderd of de ontvangstdatum van de levering wordt verplaatst voorbij de vervaldatum van de vraag, wordt de ordertracking verwijderd. U kunt ook een foutmelding tegenkomen, waarin u wordt gevraagd wat er met bestaande reserveringen moet gebeuren. Microsoft Dynamics NAV  Dit scenario wordt geïllustreerd in het volgende voorbeeld:

1. Maak een nieuw item met de naam COMP. Stel de volgende velden in:
  - **Aanvulsysteem**: Aankoop
  - **Beleid voor het volgen van bestellingen**: Alleen volgen
  - **Reserve**: Altijd
2. Maak een tweede item met de naam FG. Stel de volgende velden in:
  - **Aanvulsysteem**: Prod. Order
  - **Beleid voor het volgen van bestellingen**: Alleen volgen
  - **Reserve**: Altijd
3. Maak een tweede item met de naam FG. Stel de volgende velden in:
  - **Artikel**: COMP
  - **hoeveelheid per**: 1
4. Certificeer het productiestuklijstnummer, stuklijst FG en wijs dit toe aan artikel FG.
5. Inkooporder maken. Stel de volgende velden in:
  - **Artikel**: COMP
  - **hoeveelheid**: 10
  - **Locatiecode**: BLAUW
  - **Verwachte ontvangstdatum**: 24-01-2014
6. Een verkooporder maken. Stel de volgende velden in:
  - **Verzenddatum**: 14-02-2014
  - **Locatiecode**: BLAUW
  - **Artikel**: COMP
  - **hoeveelheid**: 10

> [!NOTE]  
> Er is een automatische reservering uitgevoerd tussen de inkoop- en verkooporder. Bovendien is er een ordertracking gecreëerd tussen de inkoop- en verkooporders.

7. Maak een handmatig vrijgegeven productieorder aan. Stel de volgende velden in:
  - **Artikel**: 14-02-2014
  - **hoeveelheid**: 10
  - **Locatie**: BLAUW
  - **Vervaldatum**: 02/01/2014
8. Selecteer op het tabblad  **Start** in de groep Proces de optie  **productieorder vernieuwen**.
9. Open de componentenlijst en zoek Item COMP op.

> [!NOTE]  
> Er wordt geen reservering of ordertracking aangemaakt door Microsoft Dynamics NAV. De reden hiervoor is dat er al een reservering bestaat voor de verkooporder die is aangemaakt in stap 6.

Stel dat het artikel om zakelijke redenen dringender nodig is op de vrijgegeven productieorder die is aangemaakt in stap 7. In de volgende stappen verwerken we de reservering van de verkooporder die is aangemaakt in stap 6 en kijken we hoe de ordertracking wordt afgehandeld.

10. Zoek de verkooporder voor artikel COMP op in stap 6 en Annuleren de reservering.
11. Open de inkooporder van stap 5 en zie dat er nu ordertracking wordt aangemaakt tussen de inkooporder en het benodigde onderdeel van de vrijgegeven productieorder.
12. Maak de reservering opnieuw aan tussen het benodigde onderdeel van de vrijgegeven productieorder en de levering van de inkooporder in stap 5.

> [!NOTE]  
> De reservering wordt niet opnieuw aangemaakt, er moet handmatig Gereed worden ingevoerd.

13. Wijzig het veld  **Verwachte ontvangstdatum** in de koptekst van de inkooporder op stap 5 van 24-01-2014 naar 05-02-2014.

Microsoft Dynamics NAV zal het volgende waarschuwingsbericht weergeven:

   Er zijn reserveringen voor deze bestelling. Deze reserveringen worden geannuleerd als er door deze wijziging een gegevensconflict ontstaat. Wilt u doorgaan?

14. Kies Ja. Zoek de reserverings- en ordervolggegevens op in de inkooporder.

> [!NOTE]  
> De bestaande reservering is geannuleerd en moet handmatig opnieuw worden aangemaakt. De order is echter dynamisch en is opnieuw aangemaakt door Microsoft Dynamics NAV om te bestaan tussen de inkooporder en de verkooporder. De reden hiervoor is dat de vraag naar de vrijgegeven productieorder (02/01/2014) vóór de verwachte ontvangstdatum van de levering ligt.

Hiermee is de demonstratie van de interactie tussen het gebruik van automatische reserveringen en ordertracking afgerond. In de voorbeelden ziet u ook wat er gebeurt als u vervaldatums wijzigt en welke foutmelding wordt weergegeven als er een reserveringsconflict is.

### Planning berekend

Als u Gereed plant met behulp van orderplanning, het aanvraagwerkblad of het planningswerkblad, worden er posten gegenereerd in de tabel  *Reserveringspost*  met het veld  **Reserveringsstatus** ingesteld op Tracking, Reservering of Overschot. Er moet altijd een bijpassend paar zijn met hetzelfde invoernummer van positieve en negatieve waarde in het veld  **hoeveelheid (basis)** wanneer de status Tracking of Reservering is. Het veld  **Brontype** is het vraagtype, dat wil zeggen tabel 37 voor de negatieve hoeveelheid en een planningstabel, bijvoorbeeld tabel 246, voor de positieve hoeveelheid. Het veld  **Bron-ID** is PLANNING.

In het geval van niet-toegewezen vraag of aanbod, wordt het veld  Microsoft Dynamics NAV Reserveringsstatus **ingesteld op Overschot.**  U kunt bijvoorbeeld een reserveringsstatus van Overschot hebben wanneer de bestaande voorraad onder de veiligheidsvoorraadhoeveelheid ligt of wanneer de vraag is gekoppeld aan de prognose.

De tabel  *Niet-getraceerde planningselementen* (tabel 99000855) bevat informatie over niet-getraceerde hoeveelheden die worden weergegeven wanneer de gebruiker een opzoekactie uitvoert op de ordertraceringspagina om niet-getraceerde hoeveelheden te bekijken of een waarschuwingspictogram kiest in het planningswerkblad. De tabel bevat posten die betrekking hebben op een niet-getraceerde overtollige hoeveelheid in het ordertraceringsnetwerk.

Deze posten worden gegenereerd tijdens het planningsproces en verklaren waar het niet-getraceerde overschotaantal in de ordertraceringsregels vandaan kwam. Dit niet-getraceerde overschot kan afkomstig zijn uit:

- Productieprognose
- Raamcontractenorders
- Veiligheidsvoorraad
- Bestelpunt
- Maximale voorraad
- Bestelaantal
- Max. bestelaantal
- Min. bestelaantal
- Vaste lotgrootte
- Demping (% van lotgrootte)

In de tabel  *Reserveringspost* is er,.Net als bij de inkoop-, overdrachts- en productieorders, een veld  **Planningsflexibiliteit** . Met dit optieveld definieert u of de levering die door deze leveringsorders wordt vertegenwoordigd, door het planningssysteem wordt meegenomen bij het berekenen van Actieberichten. Als het veld de optie Onbeperkt bevat, wordt de regel door het planningssysteem meegenomen bij het berekenen van Actieberichten. Als het veld de optie Geen bevat, is de regel vast en onveranderlijk en neemt het planningssysteem de regel niet op bij het berekenen van Actieberichten. De functie wordt beheerd in de tabel  *Reserveringsitem* met het gelijknamige veld.

### Herbestel- en productiebeleid

Als een planningsfunctie wordt uitgevoerd voor een artikelenset waarvan het bestelbeleid is ingesteld op Bestellen, worden er vermeldingen gemaakt in de tabel Reserveringsvermelding met de reserveringsstatus van het type Reservering in plaats van Tracking. Microsoft Dynamics NAV  *·* 

De velden  **Brontype** en  **Bron-ID** worden op dezelfde manier behandeld als andere volgordebeleidsregels. In het veld  **Binding** in de tabel  *Reserveringsinvoer* wordt echter Order-to-Order ingevoerd. Microsoft Dynamics NAV 

Het veld  **Binding** wordt ingevuld om leveringsorders te beheren die aan een specifieke vraag zijn gekoppeld, bijvoorbeeld productieorders die rechtstreeks vanuit een verkooporder worden gemaakt. In dit veld wordt Order-to-Order weergegeven als de invoer specifiek aan vraag of aanbod is gekoppeld (automatische reservering). De vraag kan betrekking hebben op de verkoop of de behoefte aan componenten.

### Itemtracking en reservering van prospects invoeren

De reserveringsstatus van de prospect kan worden aangemaakt in de tabel Reserveringsinvoer wanneer u geen ordernetwerkentiteiten gebruikt, dat wil zeggen ordertracering. Microsoft Dynamics NAV  *·*  U kunt bijvoorbeeld op een verbruiksdagboekregel Artikeltracering aan het onderdeel toewijzen. Als het artikel echter al een ordertracering heeft, Microsoft Dynamics NAV kunnen er meer reserveringsitems voor prospects worden aangemaakt. Dit wordt geïllustreerd in VOORBEELD 2 met betrekking tot overdrachtsopdrachten in het tweede deel van dit document.

Wanneer u de pagina  **Artikeltraceringsregels**  bekijkt of wijzigt, wordt de gezamenlijke inhoud van de tabel  *Trackingspecificaties* (tabel 336) en de tabel  *Reserveringspost* weergegeven in een tijdelijke versie van tabel 336. Hierdoor wordt gezorgd dat de historische en actieve artikeltraceringsgegevens gezamenlijk toegankelijk zijn.

Reserveringen vallen in twee categorieën: Niet-specifieke reserveringen, waarbij de lot- en serienummers niet worden opgegeven op het moment van reserveren, en Specifieke reserveringen, waarbij u specifieke lot- of serienummers uit de voorraad reserveert.

Bij een niet-specifieke reservering is het veld  **Lotnr.** of **Serienr.** in het  **Invoernr.** van tabel 337 leeg, wat wijst naar de vraag (bijvoorbeeld de verkoop). Vanwege de structuur van de reserveringslogica in  Microsoft Dynamics NAV moet u, wanneer u een niet-specifieke reservering plaatst op een artikel in de voorraad met artikeltracering, toch specifieke artikelposten selecteren om te reserveren. Microsoft Dynamics NAV 

Omdat de artikelboekposten de artikeltraceringsinformatie bevatten, reserveert de reservering indirect specifieke partij- of serienummers, ook al was dit niet de bedoeling van de gebruiker. Bij Late Binding worden er echter nog steeds reserveringen gemaakt tegen specifieke vermeldingen, maar wordt er bij het plaatsen een herschikkingsmechanisme gebruikt. Microsoft Dynamics NAV  Microsoft Dynamics NAV 

Voor meer informatie kunt u de Microsoft Dynamics NAV technische whitepapers raadplegen die vermeld staan in de aanvullende bronnen aan het einde van dit document.

### Bronsubtype, onderdrukte actiemelding, actieberichtaanpassing en velden voor annulering niet toestaan

De velden  **Subtype van bron**, **Onderdrukt actiebericht**, **Aanpassing actiebericht** en **Annulering niet toestaan** in de tabel *Reserveringsitem* worden in deze sectie beschreven. Er worden scenario's gegeven om het gebruik van de velden  **Onderdrukt actiebericht**, **Aanpassing actiebericht** en **Annulering niet toestaan** te demonstreren. Het veld  **Aanpassing actiebericht** wordt gebruikt voor de functie Tracking en actiebericht van het ordertrackingbeleid. Het veld  **Annulering niet toestaan** wordt gebruikt voor de functie Assemblage-op-order in Microsoft Dynamics NAV 2013.

#### Bronsubsoort

Het veld  **Bron-subtype** geeft aan op welk bron-subtype de reserveringsinvoer betrekking heeft. Als de invoer betrekking heeft op een inkoop- of verkoopregel, wordt het veld gekopieerd uit het veld  **documenttype** op de regel. Als het betrekking heeft op een journaalregel, wordt het veld gekopieerd uit het veld  **Invoertype**  op de journaalregel.

#### Genegeerde planningsboodschap

In het veld  **Onderdrukt actiebericht**  wordt vastgelegd wanneer een bestaande levering al gedeeltelijk is verwerkt, bijvoorbeeld wanneer een inkooporder al gedeeltelijk is ontvangen of wanneer er verbruiken zijn geboekt op een productieorder.

Wanneer de planning wordt uitgevoerd, wordt dit veld gemarkeerd en wordt het veld  Microsoft Dynamics NAV Status reserveringsinvoer **ingesteld op *Surplus8.**  Het volgende voorbeeld dient ter illustratie:

1. Open Item 80001. Stel de volgende velden in:
  - **Herbestelbeleid**: Lot-voor-Lot
  - **Reserve**: Optioneel
  - **Beleid voor het volgen van bestellingen**: Geen
2. Een verkooporder maken. Stel de volgende velden in:
  - **Artikel**: 80001
  - **Locatie**: Leeg/Geen
  - **hoeveelheid**: 10
  - **Verzenddatum**: 15-02-2014
3. Open de **Aanvraagwerkbladen** en voer de batchtaak **Plan berekenen** uit voor artikel 80001.
  - **Startdatum**: 23-01-2014
  - **Einddatum**: 03/01/2014
4. Er wordt een planningsvoorstel gedaan om de hoeveelheid van 10 aan te vullen met een nieuwe inkooporder en  **vervaldatum** 02/15/2014.
5. Kies op het tabblad  **Acties** in de groep Functies de optie  **Actie uitvoeren** Bericht om een inkooporder te maken met  **Verwachte ontvangstdatum** 02/15/2014.
6. Open de inkooporder van stap 5 en stel  **Te ontvangen aantal** in op 2 en boek alleen Ontvangst.
7. Open de verkooporder van stap 2 en wijzig de  **Verzenddatum** in 02/10/2014.
8. Open de **Aanvraagwerkbladen** en voer **Plan berekenen** uit voor artikel 80001
  - **Startdatum**: 23-01-2014
  - **Einddatum**: 03/01/2014
9. Er wordt een planningsvoorstel gedaan om de hoeveelheid van 8 aan te vullen met een nieuwe inkooporder en  **vervaldatum** 02/10/2014.

De statusinformatie in tabel 337 wordt weergegeven in de volgende afbeelding.

Postnummer 28 in tabel 337 heeft de reserveringsstatus Tracking om de bestaande voorraad, geregistreerd in artikelpost 318 voor 2 eenheden, en de openstaande vraag in verkoopordertabel 37, te matchen. De daaropvolgende post nr. 29 heeft ook de reserveringsstatus Tracking en koppelt de resterende hoeveelheid van 8 eenheden tussen de vraag in tabel 37 van de verkooporder en de voorgestelde levering in tabel 246 van de aanvraagregel.

Postnummer 30 betreft de bestaande bestelling die gedeeltelijk is ontvangen met hoeveelheid 2. Als gevolg hiervan is het veld  **Reserveringsstatus** op Overschot ingesteld en wordt het veld  Microsoft Dynamics NAV Aantal (basis) **op** 8 *(resterend saldo) ingesteld en wordt het veld* Onderdrukt actiebericht **ingeschakeld.** 

#### Planningsboodschapaanpassing

In het veld  **Aanpassing actiebericht** wordt de wijziging in de aanbodzijde van de ordertracking weergegeven die ontstaat wanneer u de gerelateerde actieberichten accepteert. Er wordt hier alleen een waarde weergegeven als de functies voor zowel ordertracering als actieberichten actief zijn (het beleid Ordertracering is ingesteld op Tracering en actiebericht). De waarde wordt berekend op basis van de gegevens in de tabel  *Action Message Entry* (tabel 99000849). Het volgende voorbeeld dient ter illustratie:
1. Open item 80002. Stel het volgende veld in:
 - **Beleid voor het volgen van bestellingen**: Tracking- en actiebericht.
2. Een verkooporder maken. Stel de volgende velden in:
  - **Artikel**: 80002
  - **Locatie**: BLAUW
  - **hoeveelheid**: 100
3. Open de pagina **Orderplanning**  en voer de batchtaak **Plan berekenen**  uit.
4. Selecteer de verkooporder uit stap 2 en voer de batchtaak  **Orders maken**  uit.
5. Wijzig in de verkooporder van stap 2 het veld  **Aantal** van 100 naar 105.
De statusinformatie in tabel 337 wordt weergegeven in de volgende afbeelding.
6. In tabel 337 is bij boekingsnummer 34 het veld  **Actiebericht Aanpassing**  ingeschakeld voor 5 eenheden met de reserveringsstatus Overschot. Omdat de verkooporder is verhoogd met stap 5, Microsoft Dynamics NAV is deze reservering aangemaakt omdat er meer voorraad nodig is.
7. Open de pagina  **Planningswerkbladen**  en kies op het tabblad  **Start** in de groep  **Proces** de optie  **Actieberichten ophalen**. Microsoft Dynamics NAV zal voorstellen om de inkooporderhoeveelheid te verhogen van 100 naar 105.

#### Annulering niet toestaan

Het veld  **Annulering niet toestaan** geeft aan dat de reserveringsinvoer de koppelen vertegenwoordigt tussen een verkooporderregel en een assemblageorder. U kunt deze reservering niet verwijderen, omdat deze nodig is om de synchronisatie te behouden die plaatsvindt wanneer een artikel op bestelling wordt geassembleerd. Het volgende voorbeeld dient ter illustratie:

1. Inkooporder maken. Stel de volgende velden in:
  - **Basiseenheid van meting**: PCS
  - Alle standaardpostinggroepen
  - **Aanvulsysteem**: Assemblage
  - **Montagebeleid**: Assembleren op bestelling
  - **Beleid voor het volgen van bestellingen**: Alleen volgen
2. Maak een nieuw item met de naam Assemble COMP. Stel de volgende velden in:
  - **Basiseenheid van meting**: PCS
  - Alle standaardpostinggroepen
  - **Aanvulsysteem**: Aankoop
  - **Beleid voor het volgen van bestellingen**: Alleen volgen
3. Open het item Assemble FG en kies op het tabblad  **Navigeren** in de groep  **Assemblage/productie** de optie  **Assemblage** en kies vervolgens  **Assemblagestuklijst**. Stel de volgende velden in op de Assembly BOM:
  - **Type**: Item
  - **Nee.**: COMP samenstellen
  - **hoeveelheid per**: 1 Kies de **OK** knop.
4. Open een artikeljournaal en verhoog de voorraad Assemble COMP naar hoeveelheid 10 voor locatie BLAUW en boek de journaalregel.
5. Een verkooporder maken. Stel de volgende velden in:
  - **Item**: FG monteren
  - **Locatie**: BLAUW
  - **hoeveelheid**: 1 De statusinformatie in tabel 337 wordt weergegeven in de volgende afbeelding.

Invoernummer 82 heeft een reserveringsstatus van 9 eenheden van de Assemble Comp op voorraad en er is geen vraag naar. Postnummer 84 volgt reserveringsposten tussen de vraag op de assemblagelijntabel 901 en het aanbod op artikelpost 346. *·* 

Postnummer 86 heeft een bindende volgorde van bestelling met de reserveringsstatus Reservering. Bovendien is het veld  **Annulering niet toestaan**  ingeschakeld, omdat het assemblagebeleid is ingesteld op Op order assembleren voor het item Assemblage FG. Ten slotte wordt het veld  **Planningsflexibiliteit** op Geen gezet, omdat Microsoft Dynamics NAV de planninglogica de reservering niet kan verwijderen.

#### Beschikbare hoeveelheid om te plukken en te reserveren

Het veld  **Gereserveerde pick- en verzendhoeveelheid**  in tabel 337 dat bestaat in versies vóór Microsoft Dynamics NAV 2013, beheert de beschikbaarheid van artikelen binnen een beheerd magazijn. In elke installatie van Microsoft Dynamics NAV magazijnbeheer bestaan artikelhoeveelheden zowel als magazijnposten als als artikelgrootboekposten. Deze twee invoertypen bevatten verschillende informatie over waar items zich bevinden en of ze beschikbaar zijn. Met magazijnposten wordt de beschikbaarheid van een artikel per (soort) opslaglocatie gedefinieerd, wat opslaglocatie-inhoud wordt genoemd. Artikelposten definiëren de beschikbaarheid van een artikel op basis van de reservering hiervan voor uitgaande documenten. Er is een speciale functionaliteit in het pickalgoritme om de hoeveelheid te berekenen die beschikbaar is om te picken wanneer de bakinhoud is gekoppeld aan reserveringen. Het pickalgoritme trekt hoeveelheden af die gereserveerd zijn voor andere uitgaande documenten, hoeveelheden op bestaande pickdocumenten en hoeveelheden die zijn gepickt maar nog niet verzonden of verbruikt. Het resultaat wordt weergegeven in het veld  **Beschikbare hoeveelheid om te picken** op de pagina  **Pickwerkblad**, waar het veld dynamisch wordt berekend. De waarde wordt ook berekend wanneer een gebruiker magazijnpicks rechtstreeks vanuit uitgaande documenten zoals verkooporders, productieconsumptie of uitgaande transfers creëert.

*Beschikbare hoeveelheid om te picken = hoeveelheid in pickbakken - hoeveelheid bij picks en bewegingen – (gereserveerde hoeveelheid in pickbakken + gereserveerde hoeveelheid bij picks en bewegingen).*

Het volgende voorbeeld illustreert hoe de waarde van de beschikbare hoeveelheid om te plukken wordt berekend in Microsoft Dynamics NAV:

1. Maak een nieuw item met de naam Warehouse Item. Stel de volgende velden in:
  - **Basiseenheid van meting**: PCS
  - Alle standaardpostinggroepen
  - **Aanvulsysteem**: Aankoop
  - **Reserveringsbeleid**: Altijd
  - **Beleid voor het volgen van bestellingen**: Alleen volgen
2. Maak een inkooporder aan voor leverancier 60000. Stel de volgende velden in:
  - **Artikel**: Magazijnartikel
  - **Locatie**: WIT
  - **hoeveelheid**: 100
3. Geef de inkooporder vrij en maak de magazijnontvangst aan.
4. Boek de magazijnontvangst en registreer de magazijnopslag voor hoeveelheid 100.
5. Maak een tweede inkooporder aan voor leverancier 60000. Stel de volgende velden in:
  - **Artikel**: Magazijnartikel
  - **Locatie**: WIT
  - **hoeveelheid**: 10
6. Geef de inkooporder vrij en maak de magazijnontvangst aan.
7. Verstuur ALLEEN het magazijnontvangstbewijs. Registreer de opslag in het magazijn niet.
8. Een verkooporder maken. Stel de volgende velden in:
  - **Artikel**: Magazijnartikel
  - **Locatie**: WIT
  - **hoeveelheid**: 10 De gereserveerde hoeveelheid wordt automatisch ingesteld op 10, omdat het reserveringsbeleid is ingesteld op Altijd.
9. Een verkooporder maken. Stel de volgende velden in:
  - **Artikel**: Magazijnartikel
  - **Locatie**: WIT
  - **hoeveelheid**: 100 De gereserveerde hoeveelheid wordt automatisch ingesteld op 100, omdat het Reserveringsbeleid is ingesteld op Altijd.
10. Geef de eerste verkooporder vrij vanuit stap 8 en maak een magazijnzending aan.
11. Geef de magazijnzending vrij en kies op het tabblad  **Acties** de optie  **Pick maken**.
Het volgende foutbericht wordt weergegeven: *Niets om te verwerken.*
  De reden hiervoor is dat de beschikbare hoeveelheid om te plukken nul is. Dit wordt als volgt berekend: Hoeveelheid op voorraad = 110 hoeveelheid beschikbaar om te picken = 100

> [!NOTE]  
> De hoeveelheid in de wegzet- of ontvangstbak is niet beschikbaar om te picken.
   
   Totaal gereserveerd voor verkooporders is 110. Beschikbare hoeveelheid om te picken = 100 – 110 = nul.

Wanneer de magazijnopzet wordt geregistreerd in stap 7, wordt het aanmaken van de magazijnpick in stap 11 mogelijk. In versies vóór Microsoft Dynamics NAV 2013 wordt het veld Gereserveerde **Pick & Ship Qty.**  in tabel 337 ingevuld op basis van de reservering voor hoeveelheid 10.

De volgende illustratie is afkomstig uit Microsoft Dynamics NAV 2009 R2.

## Illustraties met behulp van overdrachtsopdrachten en planning

### Transferorders

Wanneer u gebruikmaakt van overdrachtsopdrachten en het artikel is verzonden maar nog niet volledig ontvangen, krijgt u in de tabel  *Reserveringsinvoer* de reserveringsstatus Overschot. De locatiecode is de Transfer-to-locatie.

De **Bron Ref. Nr.** Veld wordt berekend door het laatste regelinvoernummer + regelinvoernummer van het artikel op de geboekte transferzending.

Wanneer ordertracking is geactiveerd en er geen vraag is (verkooporder of verbruik), worden er twee boekingen gemaakt in tabel 337 met de reserveringsstatus Overschot. Microsoft Dynamics NAV  De ene is tegen de  *Transfer Line* tabel 5741 en de andere is tegen de Item Ledger Post tabel 32.

Dit wordt geïllustreerd in het eerste voorbeeld.

#### Voorbeeld 1

1. Open items 80003 en 80004 en stel het veld  **Trackingbeleid**  in op  *Alleen tracking*. Laat de overige velden op hun standaardwaarden staan.
2. Open een artikeljournaal en verhoog de voorraad van deze artikelen naar 10 per stuk op locatie ROOD en boek de journaalregels.
3. Maak een overdrachtsorder van locatie ROOD naar BLAUW voor deze twee artikelen: artikel 80003 op overdrachtsorderregel 10000 en artikel 80004 op de tweede regel 20000, beide voor 10 eenheden.
4. Verstuur alleen het verzendgedeelte van de overdrachtsorder zonder enige magazijnfuncties.
De geboekte transferzending wordt in de volgende afbeelding weergegeven.
De statusinformatie in tabel 337 wordt weergegeven in de volgende afbeelding.
5. Vergelijk de resultaten van de geboekte transferzending met de posten in tabel 337.

De volgende tabel beschrijft wat er in bepaalde velden gebeurt met reserveringsinvoer 40.

|Veld|Beschrijving|  
|---------------------------------|---------------------------------------|  
|**Reserveringsstatus**|Er is een overschot omdat artikel 80003 is ingesteld met ordertracering, maar er is geen vraag.|  
|**Vestiging**|Overdrachtscodelocatie BLAUW.|  
|**Bronsoort**|Overdrachtslijntabel 5741.|  
|**Bron-ID**|Documentnummer van de overdrachtsopdracht 1011.|
|**Bron Ref. Nr.**|Totaal aantal lijnen 20000 + Regelnr. 10000 tegen Item 80003 = 30000.|

De uitleg voor de volgende velden voor Reserveringsinvoer 43 is als volgt.

|Veld|Beschrijving|  
|---------------------------------|---------------------------------------|  
|**Reserveringsstatus**|Er is een overschot omdat artikel 80003 is ingesteld met ordertracering, maar er is geen vraag.|  
|**Vestiging**|De locatie tijdens het transport EIGEN LOGBOEK is de locatie waar het item zich bevindt.|  
|**Bronsoort**|Tabel 32 van de postenboeking.|  
|**Bron Ref. Nr.**|Het openstaande Post grootboekpostnummer 322.|

#### Voorbeeld 2

Het volgende voorbeeld illustreert wat er gebeurt als een component tussen locaties wordt verplaatst, maar tegelijkertijd wordt getraceerd tussen een vraagbehoefte en het beschikbare aanbod. De componenten worden overgebracht van locatie ROOD naar BLAUW, waar ze worden verbruikt op een vrijgegeven productieorder. Het onderdeel maakt gebruik van Order Tracking, Order Planning en Item Tracking.

In het voorbeeld wordt de gedetecteerde stroom in tabel 337 gemarkeerd in relatie tot de velden **Reserveringsstatus**, **Locatiecode**, **Brontype**, **Bron-ID**, **Bronref.nr.** en type **Binding**.

1. Stel op de pagina  **productie-instellingen** het veld  **Componenten op locatie**  in op ROOD.
2. Maak een nieuw Itemcomponent. Stel de volgende velden in:
  - **Basiseenheid van meting**: PCS
  - Alle standaardpostinggroepen
  - **Aanvulsysteem**: Aankoop
  - **productiebeleid**: Make-to-Stock
  - **Beleid voor het volgen van bestellingen**: Alleen volgen
  - **Item Tracking Code**: LOTALL
3. Verhoog met behulp van het artikeljournaal de voorraad voor artikelcomponenten op locatie ROOD naar 100 eenheden. Stel de volgende lotnummers in:
  - Lotnummer Lot A, hoeveelheid 30
  - Lotnummer Lot B, hoeveelheid 70
4. Maak een nieuw item Geproduceerd. Stel de volgende velden in:
  - **Basiseenheid van meting**: PCS
  - Alle standaardpostinggroepen
  - **Aanvulsysteem**: Productie
  - **productiebeleid**: Make-to-Stock
  - **Beleid voor het volgen van bestellingen**: Alleen volgen
5. Maak een  **productiestuklijst** met 1 hoeveelheid per artikelcomponent.
6. Wijs de productiestuklijst toe aan het geproduceerde artikel.
7. Een verkooporder maken. Stel de volgende velden in:
  - **Item**: Geproduceerd
  - **Locatie**: BLAUW
  - **hoeveelheid**: 100
8. Op het tabblad  **Acties** van de verkooporder, in de groep  **Plan**, kiest u  **Planning** om een gekoppelde vrijgegeven productieorder aan te maken voor de verkooporder.
9. Open de vrijgegeven productieorder/componentbehoefte en zie dat de locatie is ingesteld als ROOD.
De reden hiervoor is dat  **Componenten op locatie** ROOD is in de **productie-instellingen** kaart.
Het geproduceerde item krijgt de uitvoer op locatie BLAUW.

De statusinformatie in tabel 337 wordt weergegeven in de volgende afbeelding.

##### Reserveringsgegevens met nummers 55 en 56

Voor de componentbehoefte voor respectievelijk Lot A en Lot B worden ordertrackinglinks gemaakt van de vraag in tabel 5407, Prod. Order Component, naar het aanbod in tabel 32, Item Ledger Entry. De **Reserveringsstatus**  veld bevat Tracking voor alle vier de vermeldingen om aan te geven dat deze dynamische ordertracking is gekoppeld aan vraag en aanbod.

De vraag in tabel 5407, Prod. Order Component, is gekoppeld aan de Source ID van de vrijgegeven productieorder 101006. Het aanbod in tabel 32, Artikelgrootboekpost, is gekoppeld aan Bronref.nr. Zijnde de artikelboekingsnummers 325 en 326 waaronder de eenheden bestaan.

> [!NOTE]  
> Het veld **Lotnr.** is leeg op de vraagregels, omdat de lotnummers niet zijn opgegeven op de materiaalregels van de vrijgegeven productieorder.

##### Reserveringsinvoer met nummer 57

Vanuit de verkoopvraag in tabel 37, Verkoopregel, wordt een ordertracking koppelen aangemaakt voor het aanbod in tabel 5406, Prod. Orderregel. Het veld  **Reserveringsstatus** bevat Reservering en het veld  **Binding** bevat Order-to-Order. Dit komt doordat de vrijgegeven productieorder specifiek voor de verkooporder is gegenereerd en gekoppeld moet blijven, in tegenstelling tot ordertrackingkoppelingen met de reserveringsstatus Tracking, die dynamisch worden gemaakt en gewijzigd.

> [!NOTE]  
> Het veld  **Binding** kan ook  *Order-to-Order* bevatten wanneer u Make-to-Order als productiebeleid en/of Order als herorderbeleid gebruikt.

10. Bij deze aanwijzen in het scenario worden de 100 eenheden van het onderdeel overgebracht van de RODE locatie naar de BLAUWE locatie met behulp van een overdrachtsorder.

Selecteer Lot A en Lot B voor de zending.

Geef voor het totale uitstaande bedrag aan dat het ALLEEN verzonden is.

> [!NOTE]  
> Componenten kunnen op locatie ROOD worden verbruikt, maar om in het voorbeeld de stroom van reserveringsinvoeren te illustreren, worden de eenheden handmatig overgebracht naar locatie BLAUW.

De statusinformatie in tabel 337 wordt weergegeven in de volgende afbeelding.

##### Reserveringsinschrijvingen met nummer 55 en 56

De ordertrackingposten voor de twee partijen van het onderdeel dat de vraag in tabel 5407 weerspiegelt, zijn gewijzigd van een reserveringsstatus Tracking naar Overschot. De reden is dat de goederen waaraan ze eerder zijn gekoppeld, in tabel 32, zijn gebruikt door de verzending van de transferorder. Werkelijk overschot, zoals in dit geval, is een reflectie van bovenmatig aanbod of vraag die niet-getraceerd blijft. Het is een indicatie van een onevenwicht in het ordernetwerk. Als het niet dynamisch wordt opgelost, genereert het planningssysteem een actiemelding.

##### Reserveringsnummers 59 tot en met 63

Omdat de twee partijen van het onderdeel op de overdrachtsorder zijn geboekt als verzonden maar nog niet ontvangen, zijn alle gerelateerde positieve ordertrackingposten van het reserveringstype Surplus, wat aangeeft dat ze niet aan enige vraag zijn toegewezen. Voor elk lotnummer heeft één post betrekking op tabel 5741, Transferregel, en één post op de artikelpost op de in-transitlocatie waar de artikelen zich nu bevinden.

Tabel 5741, **Transferlijn**, is het brontype. **Bron-ID** is het overdrachtsopdrachtdocumentnummer 1012 en **bronref.nr.** Is 20000 = 10000 + 10000 zoals gedetailleerd in Voorbeeld 1. De locatie is ingesteld als BLAUW voor de overdrachtslocatiecode.

De resterende twee posten met **Reserveringsstatus** Overschot hebben tabel 32, **Artikelpost**, als Brontype en **Bronref.nr.** 328 en 330, inclusief hun lotnummers, bevinden zich momenteel in de UITGANGSLOGBOEK op de In-transit locatie.

11. Boek de openstaande overdrachtsopdracht als Ontvangen.

De statusinformatie in tabel 337 wordt weergegeven in de volgende afbeelding.

De ordertracking-vermeldingen lijken nu op de eerste aanwijzen in het scenario, voordat de transferorder alleen als verzonden werd geboekt. De vermeldingen voor het onderdeel hebben nu alleen de reserveringsstatus Overschot in plaats van Tracking. Dit komt doordat de componentbehoefte zich nog steeds op de RODE locatie bevindt, wat aangeeft dat het veld  **Locatiecode**  op de componentregel van de productieorder ROOD bevat, zoals ingesteld in het instellingsveld  **Componenten op locatie** .

De levering die eerder aan deze vraag was toegewezen, was overgebracht naar de BLAUWE locatie en kan nu niet volledig worden getraceerd, tenzij de componentbehoefte op de productieorderregel wordt gewijzigd naar de BLAUWE locatie. Dit wordt vastgelegd in de laatste twee reserveringsvermeldingen met de ingevulde lotnummers, waarbij het veld  **Brontype** Tabel 32 is en het veld  **Bronref.nr.** Veld bestaande uit artikelposten 333 en 334.

12. Wijzig in de componentenlijst die is toegewezen aan de vrijgegeven productieorder de locatie voor het component naar BLAUW.

12. Open het **Verbruiksjournaal** en voer de batchtaak **Calc. Verbruik** uit.
Wijs aan lot A hoeveelheid 30 toe en aan lot B hoeveelheid 70.

Sluiten het Item tracking formulier.

De statusinformatie in tabel 337 wordt weergegeven in de volgende afbeelding.

##### Reserveringsgegevens met nummers 68 en 69

Omdat de componentbehoefte is gewijzigd naar de BLAUWE locatie en de levering beschikbaar is als artikelboekposten op de BLAUWE locatie, worden alle ordertrackingposten voor de twee lotnummers nu volledig getraceerd, wat wordt aangegeven door de reserveringsstatus van Tracking. De lotnummers worden niet ingevuld in het veld  **Lotnr.** tegenover de vraag in tabel 5406, **Prod. Orderregel**, omdat we geen lotnummers hebben opgegeven voor het onderdeel op de vrijgegeven productieorder.

##### Reserveringsinvoer met nummers 70 en 71

In tabel 337 worden boekingen met de reserveringsstatus Prospect gegenereerd. De reden hiervoor is dat beide lotnummers aan het onderdeel zijn toegewezen in het verbruiksjournaal, maar dat het journaal nog niet is geboekt.

Hiermee is het gedeelte afgerond over hoe ordertrackingposten in de tabel  **Reserveringspost** worden gegenereerd, gewijzigd en verwijderd bij gebruik van meerdere functies in combinatie met overdrachtsorders.

### Planning berekend

Bij het gebruik van planningsfuncties, dat wil zeggen het  **Aanvraagwerkblad**, **Planningswerkblad** of **Orderplanning**, kunnen reserveringsposten in  **Reserveringspost** tabel 337 worden gewijzigd of toegevoegd, afhankelijk van de planningsuggestie die wordt gegeven door de logica in Microsoft Dynamics NAV. Voorbeeld 3 zal gebruiken **Beleid voor opnieuw bestellen**  Bestellen met **Productiebeleid**  Op bestelling maken van een geproduceerd artikel. Het onderdeel zal gebruiken **Beleid voor opnieuw bestellen**  Vaste bestelhoeveelheid.

#### Voorbeeld 3

1. In de **Productie-opstelling**  kaart, **Component op locatie**  is ROOD ten opzichte van het vorige voorbeeld.
2. Maak een nieuw bovenliggend Item 70061. Stel de volgende velden in:
  - **Basiseenheid van meting**: PCS
  - Alle standaardpostinggroepen
  - **Aanvulsysteem**: Prod. Order
  - **productiebeleid** : Op bestelling maken
  - **Beleid voor opnieuw bestellen** : Volgorde
  - **Reservebeleid** : Optioneel
  - **Bestelling volgen** : Geen
3. Maak een nieuw componentartikel 70062. Stel de volgende velden in:
  - **Basiseenheid van meting**: PCS
  - Alle standaardpostinggroepen
  - **Aanvulsysteem** : Aankoop
  - **Beleid voor opnieuw bestellen** : Vaste bestelhoeveelheid
  - **Reservebeleid** : Optioneel
  - **Beleid voor het volgen van bestellingen**: Geen
  - **Veiligheidsvoorraadhoeveelheid**: 10
  - **aanwijzen** opnieuw ordenen: 25
  - **Bestelhoeveelheid**: 50
4. Maak een nieuwe productiestuklijst en geef componentartikel 70062 op met een hoeveelheid per 1.
Wijs de productie-BOM toe aan bovenliggend-artikel 70061.
5. Een verkooporder maken. Stel de volgende velden in:
  - **Item**: Vaste bestelhoeveelheid
  - **Locatie**: ROOD
  - **hoeveelheid**: 40
  - **Verzenddatum**: 15-02-2014
6. Open de pagina  **Planningswerkbladen** en voer de batchtaak  **Regeneratief plan berekenen**  uit.
  - **MPS/MRP**: ingeschakeld
  - **Startdatum**: 23-01-2014
  - **Einddatum**: 03/01/2014
  - Filter op items 70061 en 70062
  - Geen voorspelling

De volgende planningssuggesties worden gegeven.

Het eerste planningsvoorstel is om een nieuwe geplande productieorder te creëren om te voldoen aan de openstaande vraag van de verkooporder voor hoeveelheid 40 van het bovenliggend-artikel 70061. Controleer de ordertracering en Microsoft Dynamics NAV toon de openstaande verkooporder. Ordertracking wordt geactiveerd zodra deze door de planningsengine wordt gegenereerd.

De tweede regel is om de inventaris boven Reorder aanwijzen (25) te brengen. Rekening houdend met de bestelhoeveelheid (50), wordt door de planningslogica een hoeveelheid van 50 eenheden voorgesteld. De derde lijn is om de voorraad naar het veiligheidsniveau (10) te brengen.

De vierde regel is bedoeld om de voorraad aan te vullen wanneer de verkooporder wordt verzonden. Op dat moment is de inventaris 20 en dus lager. Bestel opnieuw aanwijzen. Als gevolg hiervan stelt de planningsengine voor om 50 extra componenten aan te schaffen, rekening houdend met de bestelhoeveelheid. Dit is een niet-getraceerde hoeveelheid, dus in tabel 337 van de reserveringsinvoer wordt dit gemarkeerd met de reserveringsstatus Overschot. *·* 

De statusinformatie in tabel 337 wordt weergegeven in de volgende afbeelding.

Het veld  **Reserveringsstatus** is Reservering en er wordt een Order-to-Order Binding gemaakt. De reden hiervoor is dat het productiebeleid voor artikelen is ingesteld op 'Make-to-order' en het herorderbeleid op 'Order'. Als een van de twee is ingesteld op Bestellen, dan wordt de reserveringsstatus Reservering in plaats van Tracking en wordt Binding ingesteld op Bestelling-tot-Bestelling.

De vraag naar 40 eenheden voor het veld  **Bron-ID** is het verkoopordernummer 1005 en het brontype is  *Verkoopregel* tabel 37. De reserveringsinvoer is afgestemd op de planningssuggestie, Bronreferentienr. 10000, Bron-ID is PLANNING en Brontype is  *Aanvraagregel* tabel 246. Er is dus een evenwicht tussen de vraag van de verkooporder en het aanbod dat de planningsengine aangeeft.

##### Reservering toegangsnummers 73 en 74

Door de batchtaak 'Plan berekenen' uit te voeren, worden de volgende vier vermeldingen gegenereerd met een reserveringsstatus 'Tracking' vanwege de instelling van het bestelbeleid 'Vaste bestelhoeveelheid' voor het onderdeel. De benodigde voorraad voor component Item 70062 wordt aangevuld met de gegeven planningsvoorstellen, Bron Ref. Nr. 20000 en 30000, met Bron-ID ingesteld op PLANNING en Brontype uit  *Aanvraagregel* tabel 246. De componentbehoefte is gecreëerd om te voldoen aan de vraag naar bovenliggend Item 70061 voor totale hoeveelheid (basis) 40. Als gevolg van deze vraag is het veld  **Source Prod. Order Line** 10000, met Source Type de  *Component Need* tabel 99000829.

De reserveringsstatus is niet Surplus, omdat er een ordertracering bestaat tussen de vraag naar bovenliggend artikel 70061 en de levering van component artikel 70062.

##### Reservering toegangsnummers 75 en 76

De laatste twee vermeldingen hebben de reserveringsstatus Overschot, omdat dit niet-getraceerde hoeveelheden zijn die zijn gegenereerd op het planningswerkblad en die betrekking hebben op de bestelparameters Bestelnummer aanwijzen en Bestelhoeveelheid.

## Zie ook  
[Ontwerpdetails: Ontwerp van artikeltracering](design-details-item-tracking-design.md)  
[Ontwerpdetails: Vraag en aanbod afstemmen](design-details-balancing-demand-and-supply.md)  
[Ontwerpdetails: Reservering, ordertracering en planningsboodschappen](design-details-reservation-order-tracking-and-action-messaging.md)   
[Ontwerpdetails: Voorraadplanning](design-details-supply-planning.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]