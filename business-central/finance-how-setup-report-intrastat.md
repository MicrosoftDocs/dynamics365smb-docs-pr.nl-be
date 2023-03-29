---
title: Intrastat-rapportage instellen
description: Leren hoe u Intrastat-rapportagefuncties instelt om handel met bedrijven in andere EU-landen/regio's te rapporteren.
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/20/2022
ms.custom: bap-template
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077'
---
# Intrastat-rapportage instellen

Bedrijven uit landen in de Europese Unie (EU) moeten handel met bedrijven uit andere landen/regio's in de EU rapporteren. Bedrijven moeten het goederenverkeer elke maand doorgeven aan de autoriteiten in hun land/regio en de aangifte moet bij de belastingdienst worden ingediend. Intrastat is het systeem voor het verzamelen van statistische handelsgegevens van goederen binnen deze landen/regio's. U gebruikt **Intrastat-rapport** voor het voltooien van de periodieke Intrastat-rapportage (meestal maandelijks), het verzamelen, registreren en rapporteren van de handel in goederen conform lokale wetgeving.

Intrastat-rapportage is gebaseerd op fundamentele EU-regelgeving die voor alle landen/regio's geldt. In de praktijk zijn er echter enkele verschillen binnen de afzonderlijke landen/regio's. Elk land/regio heeft zijn eigen regels voor wat er precies moet worden gerapporteerd en hoe.

> [!NOTE]
> Intrastat-informatie is niet van toepassing op het dienstenverkeer tussen landen/regio's, maar alleen op goederen (artikelen en vaste activa). Als de lokale overheid registratie van dienstenverkeer tussen landen/regio's verplicht stelt, kunt u dit doen met de functie **Dienstendeclaratie**.
>
> Deze functie is naar verwachting vanaf november 2022 beschikbaar als app op [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646), dus als u de functie wilt gebruiken, moet u deze eerst installeren op de pagina **Extensiebeheer**.

> [!IMPORTANT]
> Dit artikel behandelt de nieuwe Intrastat-ervaring die beschikbaar is vanaf [!INCLUDE[prod_short](includes/prod_short.md)] versie 21. Neem contact op met uw beheerder als u wilt weten welke versie uw bedrijf gebruikt en voor het inschakelen van de nieuwe functionaliteit.
>
> Lees het artikel over installatie en gebruik van Intrastat van de vorige versie op [Intrastat instellen en rapporteren](finance-how-setup-report-intrastat-v20.md).

## De nieuwe Intrastat-ervaring inschakelen

In releasewave 2 van 2022 bevat [!INCLUDE[prod_short](includes/prod_short.md)] een opnieuw ontworpen Intrastat-ervaring met uitgebreide functies. Als de nieuwe Intrastat-functionaliteit niet is ingeschakeld in uw omgeving, kan deze handmatig worden ingeschakeld door een beheerder op de pagina **Functiebeheer**.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Functiebeheer** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer op de pagina **Functiebeheer** de regel **Functie-update: de bestaande Intrastat-functionaliteit vervangen door de nieuwe Intrastat-extensie**. Meer informatie over functiebeheer op [Aankomende functies van tevoren inschakelen](/dynamics365/business-central/dev-itpro/administration/feature-management) in de beheer-inhoud.
3. Kies in de kolom **Inschakelen voor**, **Alle gebruikers**.
4. Lees de uitleg over hoe het systeem wordt geüpgraded en kies **Ja** als u akkoord gaat.
5. Selecteer **Volgende**, dan krijgt u een basisconfiguratie voor Intrastat. Lees meer over de Intrastat-configuratie in de sectie [Intrastat-configuratie](#intrastat-configuration).
6. Kies na het voltooien van de installatie **Voltooien** om de nieuwe Intrastat-ervaring te gaan gebruiken.

> [!IMPORTANT]
> Houd er rekening mee dat u oude en nieuwe ervaringen niet naast elkaar kunt gebruiken. Voordat u de extensie activeert in een productieomgeving, is het raadzaam deze functie eerst in te schakelen en te testen in een sandbox-omgeving met een kopie van de productiegegevens voordat u dit in een productieomgeving doet. Zodra u een nieuwe gebruikerservaring in uw productieomgeving activeert, kunt u niet meer teruggaan naar de oude Intrastat-functionaliteit.

> [!NOTE]
> Afhankelijk van uw bedrijfslocatie is het voldoende om de hierboven beschreven functie in te schakelen. Voor landen/regio's met specifieke functies voor Intrastat-rapportage, moet u naast de kernextensie ook de land-/regiospecifieke Intrastat-app inschakelen.

## Intrastat-configuratie

Voordat u Intrastat-rapporten kunt gebruiken, moeten er verschillende configuraties worden geïnstalleerd.

### Intrastat-rapportage-instellingen

De pagina **Intrastat-rapportage-instellingen** wordt gebruikt om Intrastat-rapportage in te schakelen en er standaarden voor in te stellen. U kunt opgeven of u Intrastat moet rapporteren vanuit verzendingen, ontvangsten (aankomsten) of beide, afhankelijk van drempelwaarden die door uw lokale verordeningen zijn ingesteld. U kunt ook standaardtransactiesoorten instellen voor normale en retourdocumenten, die worden gebruikt voor de aard van transactierapportage.

Intrastat-rapportage instellen:

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Intrastat-rapportage-instellingen** in en kies vervolgens de gerelateerde koppeling.
2. Open het sneltabblad **Algemeen** en vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] In de onderstaande tabel worden enkele van de belangrijkste velden beschreven:

   | Veld | Omschrijving |
   | --- | --- |
   | **Ontvangsten rapporteren** | Hiermee wordt opgegeven dat u aankomsten van ontvangen goederen in Intrastat-rapporten moet opnemen. |
   | **Verzendingen rapporteren** | Hiermee wordt opgegeven dat u verzendingen van verzonden artikelen in Intrastat-rapporten moet opnemen. |
   | **Verzendingen op basis van**  | Hiermee wordt opgegeven op basis van welke land/regio-code Intrastat-rapportregels worden gebruikt. U kunt een van de opties kiezen: **Verkopen aan land/regio**, **Factureren aan land/regio** of **Verzenden naar land/regio**. |
   | **Btw-nummer op basis van** | Hiermee wordt opgegeven op basis van welke klant/leverancierscode het btw-nummer wordt gekozen voor het Intrastat-rapport. U kunt een van de opties kiezen: **Verkopen aan btw** of **Factureren aan btw**. |
   | **Btw-nummer van bedrijf in bestand** | Hiermee wordt opgegeven hoe het btw-registratienummer van het bedrijf naar het Intrastat-bestand wordt geëxporteerd. U kunt een van de opties kiezen: btw-registratienr., toevoegen van de EU-land/-regiocode als voorvoegsel en het verwijderen van de EU-land-/regiocode uit btw-registratienr. |
   | **Btw-nummer van leverancier in bestand** | Hiermee wordt opgegeven hoe het btw-registratienummer van een leverancier naar het Intrastat-bestand wordt geëxporteerd. U kunt een van de opties kiezen: btw-registratienr., toevoegen van de EU-land/-regiocode als voorvoegsel en het verwijderen van de EU-land-/regiocode uit btw-registratienr. |
   | **Btw-nummer van klant in bestand** | Hiermee wordt opgegeven hoe het btw-registratienummer van een klant naar het Intrastat-bestand wordt geëxporteerd. U kunt een van de opties kiezen: btw-registratienr., toevoegen van de EU-land/-regiocode als voorvoegsel en het verwijderen van de EU-land-/regiocode uit btw-registratienr. |
   | **Partner-btw ophalen** | Hiermee wordt opgegeven vanuit welk type regel van het **Intrastat-rapport** het btw-nummer van de partner wordt bijgewerkt. Afhankelijk van uw lokale vereisten kunt u kiezen voor alleen voor ontvangst, alleen voor verzending of voor beide soorten regels. |
3. Open het sneltabblad **Algemene transacties** en vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] In de onderstaande tabel worden enkele van de belangrijkste velden beschreven:

   | Veld | Omschrijving |
   | --- | --- |
   | **Standaardtransactietype** | Hiermee wordt de standaardtransactiesoort opgegeven voor reguliere verkoopverzendingen, serviceverzendingen en inkoopontvangsten. |
   | **Standaardtransactietype - retouren** | Hiermee wordt de standaardtransactiesoort opgegeven voor verkoopretouren, serviceretouren en inkoopretouren. |
   | **Standaard-btw-nummer van particulier** | Hiermee wordt het standaard btw-nummer van de particulier opgegeven in het geval de particulier een specifiek btw-nummer moet hebben op het Intrastat-rapport. |
   | **Standaard-btw-nummer voor handel van derden** | Hiermee wordt het standaard btw-nummer voor handel van derden opgegeven voor het geval u het btw-nummer niet hebt. |
   | **Standaard-btw voor onbekende status** | Hiermee wordt het standaard-btw-nummer voor een onbekende status opgegeven. |
   | **Standaardcode van land/regio** | Hiermee wordt de code van het ontvangende standaardland of de ontvangende standaardregio opgegeven. |
4. Open het sneltabblad **Rapportage** en vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] In de onderstaande tabel worden enkele van de belangrijkste velden beschreven:

   | Veld | Omschrijving |
   | --- | --- |
   | **Code van definitie van gegevensuitwisseling** | Hiermee wordt de code van de definitie van gegevensuitwisseling opgegeven om het Intrastat-bestand te genereren. Dit werkt alleen als het veld **Bestanden met ontvangsten/verzendingen splitsen** is ingesteld op **Nee**. |
   | **Bestanden met ontvangsten/verzendingen splitsen** | Hiermee wordt opgegeven of ontvangsten en verzendingen worden gerapporteerd in twee afzonderlijke bestanden. |
   | **Zip-bestand(en)** | Hiermee wordt opgegeven of een of meer rapportbestanden worden toegevoegd aan het zip-bestand. |
   | **Code van def. van geg.uitw. - Ontvangst** | Hiermee wordt de code van de definitie van gegevensuitwisseling opgegeven om het Intrastat-bestand te genereren voor ontvangen goederen. Dit werkt alleen als het veld **Bestanden met ontvangsten/verzendingen splitsen** is ingesteld op **Ja**. |
   | **Code van def. van geg.uitw. - Verzending** | Hiermee wordt de code van de definitie van gegevensuitwisseling opgegeven om het Intrastat-bestand te genereren voor verzonden goederen. Dit werkt alleen als het veld **Bestanden met ontvangsten/verzendingen splitsen** is ingesteld op **Ja**. |
5. Open het sneltabblad **Nummering** om **Intrastat-nummers** in te stellen.

### Een rapportagebestand instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Definities van gegevensuitwisseling** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Geef op het sneltabblad **Algemeen** de definitie van gegevensuitwisseling en het type gegevensbestand, kolomscheidingsteken, gerelateerde code-eenheden, XMLport en andere velden op door de velden in te vullen.
4. Beschrijf op het sneltabblad **Regeldefinities** de opmaak van regels in het gegevensbestand door de velden in te vullen die zijn gebaseerd op het veld **Regeltype** en waar u het aantal kolommen voor deze regel moet definiëren.
5. Vul op het snelttabblad **Kolomdefinities** de regel in voor elke geplande kolom. U kunt kolomnamen, gegevenstypen (*Tekst*, *Datum* of *Decimaal*), lengte van de regel met vaste breedte die de kolom bevat als het bestand van het type Vaste tekst is, en enkele andere parameters.
6. Kies de actie **Veldtoewijzing** op het sneltabblad **Regeldefinities** om de pagina **Veldtoewijzing** te openen.
7. Maak de nieuwe invoer en kies op het sneltabblad **Algemeen** de juiste **Tabel-id** (kies 4812 voor **Intrastat-rapportregel**) en vul dan meer velden in:
   1. Geef de sleutelindex op om de bronrecords te sorteren alvorens te exporteren in het veld **Sleutelindex**.
   2. Selecteer de juiste **Codeunit voor toewijzing**.
8. Voeg op het snelttablad **Veldtoewijzing** kolommen toe die u eerder hebt geconfigureerd in het sneltabblad **Kolomdefinities** en voeg vervolgens het volgende toe:
   1. Geef voor elk van de kolommen de **Veld-id** op.
   2. Geef de **Transformatieregel** voor elke kolom waarin u deze nodig hebt. Hiermee wordt de regel opgegeven die geïmporteerde tekst omzet in een ondersteunde waarde voordat deze kan worden toegewezen aan een opgegeven veld in [!INCLUDE[prod_short](includes/prod_short.md)]. Wanneer u een waarde in dit veld kiest, wordt de exacte waarde ingevoerd in het veld **Transformatieregel** in de tabel **Veldtoewijzingsbuf. gegevensuitwisseling** en omgekeerd.
9. Als u invoer moet groeperen op basis van enkele kolommen, kunt u op het snelttabblad **Veldgroepering** de velden kieze die u wilt gebruiken voor groepering.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] wordt geleverd met de vooraf geconfigureerde definitie van gegevensuitwisseling voor Intrastat voor alle gelokaliseerde landen/regio's. Voor meer informatie over het maken van een nieuwe definitie van gegevensuitwisseling raadpleegt u het artikel [Definities van gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md).

### Stel verplichte velden in met de checklist voor Intrastat-rapporten

In sommige landen/regio's vereist de belastingdienst dat Intrastat-rapporten bijvoorbeeld de verzendmethode bevatten voor inkopen of andere waarden wanneer de verkoop boven een bepaalde drempel ligt.

Verplichte velden en/of waarden instellen op de pagina **Intrastat-rapport**:

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Intrastat-rapportinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Intrastat-rapportcontrolelijst**.
3. Voeg de benodigde regels voor controle toe aan de hand van de volgende instructies:
   1. Stel het veld **Veld nr.** in op een veld dat moet worden gecontroleerd op een niet-lege waarde.
   2. Vul indien nodig het veld **Filterexpressie** in, op basis van de volgende regels:
      1. Kies wanneer u de **Filterpagina** open het **Filter** dat u moet gebruiken om te controleren.
      2. Kies in de volgende stap een waarde gerelateerd aan het gebruikte **Filter**.
      3. Als u meer filters moet invullen voor dit specifieke veld, kunt u nog een filter toevoegen door dezelfde stappen te volgen.
      4. Wanneer u klaar bent met het invoeren van de filters voor het gekozen veld, kiest u **OK**.
   3. Selecteer het veld **Omgekeerde filterexpressie**, hiermee geeft u op dat de controle voor velden alleen wordt uitgevoerd op regels die niet overeenkomen met de filterexpressie. Als de regel niet wordt gefilterd, wordt dit veld genegeerd.

> [!NOTE]
> Wanneer u de **Filterpagina** opent van de regel **Filterexpressie** kunt u alle standaard filterexpressies gebruiken die betrekking hebben op het specifieke veld dat u wilt filteren.
>
> Wees voorzichtig bij het instellen van validatieregels. Ze kunnen van land/regio tot land/regio verschillen.

## Aangepaste codeunits gebruiken in Intrastat-rapporten

Als u de werking van Intrastat wilt wijzigen en de standaardconfiguratie niet voldoende is, kunt u het systeem aanpassen door de standaardfuncties uit te breiden. Als u het Intrastat-gedrag verder moet wijzigen, kunt u uw eigen codeunits ontwikkelen. Wanneer u codeunits maakt, moet u echter aanvullende wijzigingen aanbrengen om deze te gebruiken. Het systeem configureren om uw eigen objecten te gebruiken:

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Configuratie van btw-rapporten** in en kies vervolgens de gerelateerde koppeling.
2. Voeg op de pagina **Configuratie van btw-rapporten** een nieuwe regel toe.
3. Kies in het veld **Type btw-rapport** de optie **Intrastat-rapport**.
4. Geef in het veld **Versie van btw-rapport** de versie van het rapport op.
5. Daarna kunt u uw codeunits toevoegen voor de volgende opties: a. Geef in het veld **Codeunit-id voor regels voorstellen** de nieuwe codeunit op voor het voorstellen van regels op de Intrastat-rapportregels.
   b. Geef in het veld **Inhoud codeunit-id** de nieuwe codeunit op voor het exporteren van gegevens als een bestand met behulp van een definitie van gegevensuitwisseling.
   c. Geef in het veld **Codeunit-id valideren** de nieuwe codeunits op voor het valideren van resultaten binnen Intrastat-rapportregels.

> [!IMPORTANT]
>
> Deze regel moet leeg zijn als u de standaard codeunits gebruikt. U moet alleen een regel maken en configureren als u aangepaste codeunits heeft ontwikkeld.

## Overige Intrastat-configuraties

> [!IMPORTANT]
> Klantenkaarten en leverancierskaarten bevatten een veld, **Intrastat-partnertype**, dat dezelfde optiewaarden heeft als het veld **Partnertype**: "" (leeg), *Bedrijf* en *Persoon*. Het veld **Intrastat-partnertype** vervangt het veld **Partnertype** in Intrastat-rapportage. Het veld **Partnertype** wordt gebruikt in de Single euro Payments Area (SEPA) om het SEPA Direct Debit Scheme (Core of B2B) te definiëren. Het veld **Intrastat-partnertype** wordt alleen gebruikt voor Intrastat-rapportage. Op deze manier kunt u indien nodig verschillende waarden voor de twee velden opgeven.
>
> Als het veld **Intrastat-partnertype** leeg wordt gelaten, wordt de waarde van het veld **Partnertype** gebruikt voor Intrastat-rapportage.

Naast **Intrastat-rapport instellen**, **Definities van gegevensuitwisseling** en **Controlelijst voor Intrastat-rapporten**, moet u ook andere instellingen configureren:

| Pagina | Omschrijving |
| ---- | ----------- |
| **Landen/Regio's** | Voordat u Intrastat-rapporten gaat gebruiken, moet u ook de pagina **Landen/Regio's** instellen. Op deze pagina moet u de **EU-land-/regiocode** en **Intrastat-code** toevoegen om een code op te geven voor het land/de regio waarmee u handelt, aangezien deze zullen worden gebruikt in Intrastat-rapporten. |
| **Tariefcodes** | In veel landen/regio's hanteren de belastingdienst en de douane codes van acht tekens voor verschillende artikelen. Om ervoor te zorgen dat artikelposten de benodigde informatie bevatten wanneer het programma ze van de Intrastat-dagboekregel importeert, moet u de artikelcode invoeren op de pagina **Tariefcodes**. Zoek de codes voor de artikelen waar uw bedrijf in handelt en geef ze op de pagina **Tariefcodes** op. |
| **Transportmethodes** | Er zijn zeven eencijferige codes voor Intrastat-transportmethoden. **1** voor zee, **2** voor spoor, **3** voor weg, **4** voor lucht, **5** voor de post, **7** voor vaste installaties en **9** voor eigen voortdrijving (bijvoorbeeld, een auto verplaatsen door ermee te rijden). [!INCLUDE[prod_short](includes/prod_short.md)] vereist deze specifieke codes niet, maar we raden aan dat de beschrijvingen een soortgelijke betekenis hebben. |
| **Transactiesoorten** | Landen/regio's hebben verschillende codes voor soorten Intrastat-transacties, zoals de gewone inkoop en verkoop, het ruilen van geretourneerde goederen en het ruilen van niet-geretourneerde goederen. Stel alle codes in die van toepassing zijn op uw land of regio. Deze codes worden vervolgens op het sneltabblad **Buitenlandse handel** gebruikt in verkoop- en inkoopdocumenten, en bij de verwerking van retouren. |
| **Transactieomschrijvingen** | Stel codes in als aanvulling op de transactiesoortbeschrijvingen. |
  > [!NOTE]
  > Vanaf januari 2022 vereist Intrastat andere transactie-aardcodes voor verzendingen naar particulieren of niet-btw-geregistreerde bedrijven en btw-geregistreerde bedrijven. Om aan deze vereiste te voldoen raden we u aan om nieuwe transactie-aardcodes te bekijken en/of toe te voegen op de pagina **Transactiesoorten** volgens de vereisten in uw land/regio. U moet ook het veld **Intrastat-partnertype** controleren en bijwerken naar *Persoon* voor een particulier of niet-btw-geregistreerde zakelijke klanten op de relevante pagina **Klant**. Als u niet zeker weet welk Intrastat-partnertype of transactiesoort u moet gebruiken, raden we u aan een expert in uw land of regio te raadplegen.

| **Veld** | **Beschrijving** |
| --------- | --------------- |
| **Nettogewicht** | Gewicht is een van de basisconfiguraties met betrekking tot Intrastat-rapporten aangezien **Totale gewicht** verplicht is voor rapportage. Om aan deze eis te kunnen voldoen, moet u ook het veld **Nettogewicht** invullen op de artikel- of vaste-activakaart. |
| **Code van land/regio van oorsprong** | Gebruik de tweeletterige ISO-alfacodes op de artikel- of vaste-activakaart voor het land/de regio waar het goed is verkregen of geproduceerd. Als het goed in meer dan één land is geproduceerd, is het land van herkomst het laatste land waar het in belangrijke mate is verwerkt. |
| **Btw-identificatienummer van de partneroperator in de lidstaat van invoer** | Dit is het btw-identificatienummer van de partneroperator in de lidstaat van invoer. Het btw-nummer wordt ook gebruikt bij de uitwisseling van intra-EU exportgegevens tussen de lidstaten en stelt de lidstaten in staat de ontvangen gegevens toe te wijzen aan het importerende bedrijf in hun eigen land/regio. Rapporterende eenheden moeten het btw-nummer rapporteren van het bedrijf dat de intra-unie verwerving van goederen heeft aangegeven in de lidstaat van invoer. |

Eventueel kunt u ook het volgende instellen:

* **Basisproductcodes**: de belastingdienst en de douane hebben numerieke codes om artikelen en service te classificeren. U geeft deze codes op voor artikelen.
* **Districten**: extra informatie over landen/regio's.
* **Invoer-/uitvoerhavens**: geef op naar welke locaties u artikelen wilt verzenden of wilt ontvangen naar of uit andere landen/regio's. Een luchthaven is een voorbeeld van een invoer-/uitvoerhaven. U voert invoer- of uitvoerhavens in op verkoop- of inkoopdocumenten op het sneltabblad **Buitenlandse handel**. Deze gegevens worden tevens gekopieerd van de artikelposten wanneer u het Intrastat-dagboek maakt.
* **Aanvullende maateenheid**: de hoeveelheid goederen voor Intrastat-rapportage kan zowel nettogewicht (in kilogram) als een aanvullende eenheid zijn. Als er aanvullende eenheden nodig zijn, moet u deze configureren voor artikelen en vaste activa.

#### Transportmethoden instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Transportmethoden** in en kies vervolgens de gerelateerde koppeling.
2. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### Transactieaardcodes instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Transactiesoorten** in en kies vervolgens de gerelateerde koppeling.
2. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### Andere gerelateerde configuraties

Voordat u de Intrastat-rapportagefunctie gebruikt, moet u enkele velden configureren op de artikel-, vaste activa-, klant- en leverancierskaarten.

#### Artikelkaarten

Om alle benodigde informatie met betrekking tot Intrastat op artikelkaarten in te stellen:

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer het artikel dat u wilt configureren.
3. Vul op het sneltabblad **Kosten en boeking** de velden **Tariefnr.**, **Aanvullende maateenheid** en **Code voor land/regio van herkomst** in.
4. Vouw op het sneltabblad **Voorraad** de decimale waarde in het veld **Nettogewicht** in.

> [!NOTE]
> U kunt verschillende maateenheden gebruiken als aanvullende maateenheid. Als dit niet hetzelfde is als de **Basismaateenheid**, moet u deze maateenheid configureren op de pagina **Artikeleenheden**.

#### Vaste activa

Om alle benodigde informatie met betrekking tot Intrastat op vaste activa in te stellen:

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Vaste activa** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer het vaste activum dat u wilt configureren.
3. Vouw op het sneltabblad **Intrastat** de velden **Tariefnr.**, **Nettogewicht** en **Aanvullende maateenheid** in.

> [!NOTE]
> U kunt verschillende maateenheden gebruiken als aanvullende maateenheid. Maar welke **Code van eenheid** u ook kiest, de **Hoeveelheid** ervan in Intrastat-rapporten is altijd 1.

#### Leveranciers

Voordat u een leverancier in Intrastat-rapportage gebruikt, moet u een speciale **Land-/regiocode** en **Btw-registratienr.** voor elke leverancier invullen, naast verdere informatie over hun pagina **Leverancier**:

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Leveranciers** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de leverancier die u wilt configureren.
3. Op het sneltabblad **Intrastat** kunt u standaardwaarden instellen voor de velden **Standaard transactiesoort**, **Standaard transactiesoort - Retouren** en **Standaard transportmethode**.
4. Geef op het sneltabblad **Betalingen** in het veld **Intrastat-partnertype** op of de leverancier een persoon of een bedrijf is.

#### Klantenkaarten

Voordat u een klant in Intrastat-rapportage gebruikt, moet u een speciale **Land-/regiocode** en **Btw-registratienr.** voor elke klant invullen, naast verdere informatie over hun pagina **Klantenkaart**:

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Klanten** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de klant die u wilt configureren.
3. Op het sneltabblad **Intrastat** kunt u standaardwaarden instellen voor de velden **Standaard transactiesoort**, **Standaard transactiesoort - Retouren** en **Standaard transportmethode**.
4. Geef op het sneltabblad **Betalingen** in het veld **Intrastat-partnertype** op of de leverancier een persoon of een bedrijf is.

#### Artikelen en vaste activa uitsluiten van Intrastat-rapportage

Als er een reden is om een specifiek artikel of vast activum uit te sluiten van Intrastat-rapportage, moet u een optie op hun kaart wijzigen.

##### Uitsluiten van een artikel voor Intrastat-rapportage

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer het artikel dat u wilt configureren.
3. Selecteer op het sneltabblad **Kosten en boeking** het veld **Uitsluiten van Intrastat-rapport**.

##### Een vast activum uitsluiten van Intrastat-rapportage

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Vaste activa** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer het vaste activum dat u wilt configureren.
3. Selecteer op het sneltabblad **Intrastat** het veld **Uitsluiten van Intrastat-rapport**.

## Land-/regiospecifieke Intrastat-configuratie

De Intrastat-vereisten zijn vergelijkbaar in alle lidstaten van de EU, hoewel er belangrijke uitzonderingen zijn. In theorie zouden de regels in alle lidstaten uniform moeten worden toegepast. Er zijn echter verschillen in de uitvoering omdat sommige lidstaten richtlijnen geven hoe de algemene beginselen in de verordening in specifieke situaties kunnen worden toegepast. Bijvoorbeeld commerciële samples, retourzendingen van goederen, enzovoort. Deze richtlijnen kunnen verschillende resultaten opleveren voor verschillende situaties in EU-lidstaten. Daarom hebben sommige landen/regio's wat extra specifieke informatie die los staat van andere landen/regio's. Ook gebruiken ze een ander bestandsformaat voor rapportage.

### Oostenrijk

Intrastat-rapportage in Oostenrijk vereist twee verschillende bestanden voor ontvangsten en verzendingen. Volg deze stappen om te controleren of uw instellingen correct zijn:

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Intrastat-rapportage-instellingen** in en kies vervolgens de gerelateerde koppeling.  
2. Controleer op het sneltabblad **Rapportage** of **Bestanden met ontvangsten/verzendingen splitsen** is geselecteerd. In verband daarmee vindt u twee afzonderlijke **Codes van definitie van gegevensuitwisseling** geconfigureerd. Het veld **Zip-bestand(en)** is ook geselecteerd om ervoor te zorgen dat rapportbestanden worden toegevoegd aan het zip-bestand.

Het proces van werken met Intrastat-rapporten is hetzelfde als de globale functie.

<!-- ### Belgium-->

### Tsjechië

De nieuwe Intrastat-rapportervaring voor Tsjechië is beschikbaar vanaf releasewave 1 van 2023. In de tussentijd kunt u de functie **Intrastat-dagboek** blijven gebruiken.

### Finland

In Finland zijn er een paar extra stappen om Intrastat in te stellen. Intrastat-rapportage in Finland vereist twee verschillende bestanden voor ontvangsten en verzendingen. In verband daarmee vindt u twee afzonderlijke **Codes van definitie van gegevensuitwisseling** geconfigureerd.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Intrastat-rapportage-instellingen** in en kies vervolgens de gerelateerde koppeling.  
2. Vul op de pagina **Intrastat-rapportinstellingen** op het sneltabblad **Bestand instellen** de velden in zoals beschreven in de volgende tabel:

    |Veld|Omschrijving|  
    |------------------------------------|---------------------------------------|
    | **Aangepaste code**|Specificeert een aangepaste code voor de instellingsinformatie van het Intrastat-bestand. |
    | **Serienummer van bedrijf**|Specificeert een serienummer van een bedrijf voor de instellingsinformatie van het Intrastat-bestand. |

3. Controleer op het sneltabblad **Rapportage** of **Bestanden met ontvangsten/verzendingen splitsen** is geselecteerd.

Het proces van werken met Intrastat-rapporten is hetzelfde als de globale functie.

<!-- ### Germany-->

### Italië

De nieuwe Intrastat-rapportervaring voor Italië is beschikbaar vanaf februari 2023. In de tussentijd kunt u de functie **Intrastat-dagboek** blijven gebruiken.

<!-- ### France-->

### Zweden

Intrastat-rapportage in Zweden vereist twee verschillende bestanden voor ontvangsten en verzendingen. Volg deze stappen om te controleren of uw instellingen correct zijn:

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Intrastat-rapportage-instellingen** in en kies vervolgens de gerelateerde koppeling.  
2. Controleer op het sneltabblad **Rapportage** of **Bestanden met ontvangsten/verzendingen splitsen** is geselecteerd. In verband daarmee vindt u twee afzonderlijke **Codes van definitie van gegevensuitwisseling** geconfigureerd.

Het proces van werken met Intrastat-rapporten is hetzelfde als in de globale functie.

<!-- ### United Kingdom-->

## Zie gerelateerde training op [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## Zie ook

[Intrasta-rapporten in Business Central](finance-how-report-intrastat.md)  
[Financieel beheer](finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
