---
title: Intrastat-rapportage instellen
description: Dit artikel legt uit hoe u Intrastat-rapportagefuncties instelt en hoe u handel rapporteert met bedrijven in andere EU-landen/regio's.
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 04/05/2023
ms.custom: bap-template
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077'
---
# Intrastat-rapportage instellen

Bedrijven uit landen in de Europese Unie (EU) moeten handel met bedrijven uit andere landen/regio's in de EU rapporteren. Bedrijven moeten het goederenverkeer elke maand doorgeven aan de autoriteiten in hun land/regio en de aangifte moet bij de belastingdienst worden ingediend. Intrastat is het systeem dat wordt gebruikt voor het verzamelen van statistische handelsgegevens over goederen binnen deze landen/regio's. Gebruik het Intrastat-rapport voor het voltooien van de periodieke Intrastat-rapportage, het verzamelen, registreren en rapporteren van de handel in goederen conform lokale wetgeving.

Intrastat-rapportage is gebaseerd op de basisregelgeving van de EU die van toepassing is op alle landen/regio's. Er zijn echter verschillen binnen de afzonderlijke landen/regio's. Elk land/regio heeft zijn eigen regels voor wat er precies moet worden gerapporteerd en hoe.

> [!NOTE]
> Intrastat-informatie is niet van toepassing op het verkeer van diensten tussen landen/regio's. In plaats daarvan is de informatie alleen van toepassing op goederen zoals artikelen en vaste activa. Als uw lokale overheid uw registratie van dienstenverkeer tussen landen/regio's verplicht stelt, kunt u dit doen met de functie **Servicedeclaratie**.
>
> Deze functie is vanaf november 2022 beschikbaar als app die u kunt downloaden van [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646). Om deze functie te gebruiken installeert u deze op de pagina **Extensiebeheer**.

> [!IMPORTANT]
> Dit artikel behandelt de nieuwe Intrastat-ervaring die beschikbaar is vanaf [!INCLUDE[prod_short](includes/prod_short.md)] versie 21. Neem contact op met uw beheerder als u wilt weten welke versie uw bedrijf gebruikt en of u de nieuwe functionaliteit moet inschakelen.
>
> Lees het artikel over installatie en gebruik van Intrastat van de vorige versie op [Intrastat instellen en rapporteren](finance-how-setup-report-intrastat-v20.md).

## De nieuwe Intrastat-ervaring inschakelen

In releasewave 2 van 2022 bevat [!INCLUDE[prod_short](includes/prod_short.md)] een opnieuw ontworpen Intrastat-ervaring die uitgebreide functies biedt. Als de nieuwe Intrastat-functionaliteit niet is ingeschakeld in uw omgeving, kan deze handmatig worden ingeschakeld door een beheerder op de pagina **Functiebeheer**.

> [!IMPORTANT]
> U kunt oude en nieuwe ervaringen niet naast elkaar gebruiken. Voordat u de extensie activeert in een productieomgeving, is het raadzaam deze functie te testen in een sandbox-omgeving met een kopie van productiegegevens. Nadat u een nieuwe gebruikerservaring in uw productieomgeving hebt geactiveerd, kunt u niet meer teruggaan naar de oude Intrastat-functionaliteit.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Functiebeheer** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer op de pagina **Functiebeheer** de regel voor **Functie-update: de bestaande Intrastat-functionaliteit vervangen door de nieuwe Intrastat-extensie**. U vindt meer informatie over functiebeheer op [Aankomende functies van tevoren inschakelen](/dynamics365/business-central/dev-itpro/administration/feature-management) in de beheer-inhoud.
3. Selecteer in de kolom **Inschakelen voor**, **Alle gebruikers**.
4. Lees de uitleg over hoe het systeem wordt geüpgraded en selecteer **Ja** als u akkoord gaat.
5. Selecteer **Volgende**. U krijgt de basisinstelling voor Intrastat. Zie voor meer informatie over de Intrastat-instelling de sectie [Intrastat-configuratie](#intrastat-configuration), verderop in dit artikel.
6. Kies na het voltooien van de installatie **Voltooien** om de nieuwe Intrastat-ervaring te gaan gebruiken.

    > [!NOTE]
    > Afhankelijk van uw bedrijfslocatie is het voldoende om de eerder beschreven functie in te schakelen. Voor landen/regio's met specifieke functies voor Intrastat-rapportage, moet u naast de kernextensie ook de land/regio-specifieke Intrastat-app inschakelen.

## Intrastat-configuratie

Voordat u Intrastat-rapporten kunt gebruiken, moeten er verschillende configuraties worden geïnstalleerd.

### Intrastat-rapportage-instellingen

Gebruik de pagina **Intrastat-rapportage-instellingen** om het standaardgedrag in te schakelen en in te stellen voor Intrastat-rapportage. U kunt opgeven of u Intrastat moet rapporteren vanuit verzendingen, ontvangsten (aankomsten) of beide, afhankelijk van drempelwaarden die door uw lokale verordeningen zijn ingesteld. U kunt ook standaardtransactiesoorten instellen voor de normale en retourdocumenten, die worden gebruikt voor transactierapportage.

Volg deze stappen om Intrastat-rapportage in te stellen.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Intrastat-rapportage-instellingen** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer op het tabblad **Algemeen** indien nodig veldinformatie of voer deze in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] In de volgende tabel worden enkele van de belangrijkste velden beschreven.

   | Veld | Omschrijving |
   | --- | --- |
   | **Ontvangsten rapporteren** | Hiermee wordt opgegeven dat u aankomsten van ontvangen goederen in Intrastat-rapporten moet opnemen. |
   | **Verzendingen rapporteren** | Hiermee wordt opgegeven dat u verzendingen van verzonden artikelen in Intrastat-rapporten moet opnemen. |
   | **Verzendingen op basis van**  | Hiermee wordt de land/regio-code opgegeven op basis waarvan rapportregels worden gebruikt.  |
   | **Btw-nummer op basis van** | Hiermee wordt de klant- of leverancierscode opgegeven op basis waarvan het btw-nummer wordt gekozen voor het Intrastat-rapport.  |
   | **Btw-nummer van bedrijf in bestand** | Hiermee wordt opgegeven hoe het btw-nummer van het bedrijf naar het Intrastat-bestand wordt geëxporteerd.  |
   | **Btw-nummer van leverancier in bestand** | Hiermee wordt opgegeven hoe het btw-registratienummer van een leverancier naar het Intrastat-bestand wordt geëxporteerd.  |
   | **Btw-nummer van klant in bestand** | Hiermee wordt opgegeven hoe het btw-registratienummer van een klant naar het Intrastat-bestand wordt geëxporteerd.  |
   | **Partner-btw ophalen** | Hiermee wordt opgegeven vanuit welk type Intrastat-rapportregel het btw-nummer van de partner wordt bijgewerkt. Afhankelijk van uw lokale vereisten kunt u kiezen voor alleen voor ontvangstregels, alleen verzendingregels of beide soorten regels. |

3. Selecteer op het sneltabblad **Standaardtransacties** veldinformatie of voer deze indien nodig in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] In de volgende tabel worden enkele van de belangrijkste velden beschreven.

   | Veld | Omschrijving |
   | --- | --- |
   | **Standaardtransactietype** | Hiermee wordt de standaardtransactiesoort opgegeven voor reguliere verkoopverzendingen, serviceverzendingen en inkoopontvangsten. |
   | **Standaardtransactietype - retouren** | Hiermee wordt de standaardtransactiesoort opgegeven voor verkoopretouren, serviceretouren en inkoopretouren. |
   | **Standaard-btw-nummer van particulier** | Hiermee wordt het standaard btw-nummer van de particulier opgegeven als de particulier een specifiek btw-nummer moet hebben op het Intrastat-rapport. |
   | **Standaard-btw-nummer voor handel van derden** | Hiermee wordt het standaard btw-nummer voor handel van derden opgegeven als u het btw-nummer niet hebt. |
   | **Standaard-btw voor onbekende status** | Hiermee wordt het standaard-btw-nummer voor een onbekende status opgegeven. |
   | **Standaardcode van land/regio** | Hiermee wordt de code van het ontvangende standaardland of de ontvangende standaardregio opgegeven. |

4. Selecteer op het tabblad **Rapportage** indien nodig veldinformatie of voer deze in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] In de volgende tabel worden enkele van de belangrijkste velden beschreven.

   | Veld | Omschrijving |
   | --- | --- |
   | **Code van definitie van gegevensuitwisseling** | Hiermee wordt de code van de definitie van gegevensuitwisseling opgegeven om het Intrastat-bestand te genereren. Dit veld is alleen beschikbaar als het veld **Bestanden met ontvangsten/verzendingen splitsen** is ingesteld op **Nee**. |
   | **Bestanden met ontvangsten/verzendingen splitsen** | Hiermee wordt opgegeven of ontvangsten en verzendingen moeten worden gerapporteerd in twee afzonderlijke bestanden. |
   | **Zip-bestand(en)** | Hiermee wordt opgegeven of de rapportbestanden moeten worden toegevoegd aan het zip-bestand. |
   | **Code van def. van geg.uitw. - Ontvangst** | Hiermee wordt de code van de definitie van gegevensuitwisseling opgegeven om het Intrastat-bestand te genereren voor ontvangen goederen. Dit veld is alleen beschikbaar als het veld **Bestanden met ontvangsten/verzendingen splitsen** is ingesteld op **Ja**. |
   | **Code van def. van geg.uitw. - Verzending** | Hiermee wordt de code van de definitie van gegevensuitwisseling opgegeven om het Intrastat-bestand te genereren voor verzonden goederen. Dit veld is alleen beschikbaar als het veld **Bestanden met ontvangsten/verzendingen splitsen** is ingesteld op **Ja**. |

5. Voer op het sneltabblad **Nummering** een waarde in het veld **Intrastat-nummers** in.

### Een rapportagebestand instellen

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Definities van gegevensuitwisseling** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer **Nieuw** en voer vervolgens indien nodig op het sneltabblad **Algemeen** de definitie van gegevensuitwisseling, het type gegevensbestand, het kolomscheidingsteken, gerelateerde codeunits, XMLport en andere velden in.
3. Voer op het sneltabblad **Regeldefinities** een waarde in het veld **Regelsoort** in om de opmaak van regels in het gegevensbestand te beschrijven en waar u het aantal kolommen voor deze regel moet definiëren.
4. Vul op het snelttabblad **Kolomdefinities** de regel in voor elke geplande kolom. U kunt kolomnamen, gegevenstypen (tekst, datum of decimaal), de lengte van de regel met vaste breedte die de kolom bevat als het bestand van het type *Vaste tekst* is, en andere parameters definiëren.
5. Selecteer op het sneltabblad **Regeldefinities** **Veldtoewijzing**.
6. Maak een nieuw item op de pagina **Veldtoewijzing**. 
7. Selecteer op het sneltabblad **Algemeen** de waarde **Tabel-id** (kies voor **Intrastat-rapportregel** **4812**) en voer de volgende veldinformatie in:

   1. Geef in het veld **Sleutelindex** de sleutelindex op om de bronrecords te sorteren alvorens te exporteren.
   2. Selecteer een waarde in het veld **Toewijzing van codeunit**.

8. Voeg op het sneltabblad **Veldtoewijzing** de kolommen toe die u eerder hebt geconfigureerd op het sneltabblad **Kolomdefinities** en voeg dan de volgende veldinformatie toe:

   1. Geef voor elk van de kolommen de **Veld-id** op.
   2. Geef indien nodig de **Transformatieregel** voor elke kolom op. Met deze waarde wordt de regel opgegeven die geïmporteerde tekst omzet in een ondersteunde waarde voordat deze kan worden toegewezen aan een opgegeven veld in [!INCLUDE[prod_short](includes/prod_short.md)]. Wanneer u een waarde in dit veld kiest, wordt de exacte waarde ingevoerd in het veld **Transformatieregel** in de **Veldtoewijzingsbuf. gegevensuitwisseling** tabel. (Wanneer daarentegen een exacte waarde wordt ingevoerd in het veld **Transformatieregel** in de tabel **Veldtoewijzingsbuf. gegevensuitwisseling**, wordt in dit veld een waarde gekozen.)

9. Als u items moet groeperen op basis van enkele kolommen, selecteert u op het sneltabblad **Veldgroepering** de velden die u wilt gebruiken voor groepering.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] wordt geleverd met de vooraf geconfigureerde definitie van gegevensuitwisseling voor Intrastat voor alle gelokaliseerde landen/regio's. Voor meer informatie over het maken van een nieuwe definitie van gegevensuitwisseling raadpleegt u [Definities van gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md).

### Stel verplichte velden in met de checklist voor Intrastat-rapporten

In sommige landen/regio's vereist de belastingdienst dat Intrastat-rapporten bijvoorbeeld de verzendmethode bevatten voor inkopen of andere waarden wanneer de verkoop boven een bepaalde drempel ligt.

Als u verplichte velden of waarden wilt instellen op de pagina **Intrastat-rapport**, volgt u deze stappen:

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Intrastat-rapportage-instellingen** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer **Controlelijst van Intrastat-rapport**.
3. Volg deze stappen om de benodigde regels voor controle toe te voegen:
   1. Stel het veld **Veld nr.** in op een veld dat moet worden gecontroleerd op een niet-lege waarde.
   2. Voer een waarde in het veld **Filterexpressie** in, op basis van de volgende regels:

        1. Wanneer u de **Filterpagina** opent, selecteert u het filter dat u moet gebruiken om te controleren.
        2. Selecteer een waarde die gerelateerd is aan het geselecteerde filter.
        3. Als u meer filters voor het gekozen veld moet invullen, herhaalt u de vorige twee stappen om nog een filter toe te voegen.
        4. Wanneer u klaar bent met het invoeren van de filters voor het gekozen veld, selecteert u **OK**.

   3. Schakel het selectievakje **Omgekeerde filterexpressie** in om op te geven dat de controle voor velden alleen wordt uitgevoerd op regels die niet overeenkomen met de filterexpressie. Als de regel niet wordt gefilterd, wordt dit veld genegeerd.

> [!NOTE]
> Wanneer u de **Filterpagina** opent van de regel **Filterexpressie** kunt u alle standaard filterexpressies gebruiken die betrekking hebben op het specifieke veld dat u wilt filteren.
>
> Wees voorzichtig bij het instellen van validatieregels, omdat deze per land/regio kunnen verschillen.

## Aangepaste codeunits gebruiken in Intrastat-rapporten

Als u de werking van Intrastat wilt wijzigen en de standaardconfiguratie niet voldoende is, kunt u het systeem aanpassen door de standaardfuncties uit te breiden. Als u het Intrastat-gedrag verder moet wijzigen, kunt u uw eigen codeunits ontwikkelen. Wanneer u codeunits maakt, moet u aanvullende wijzigingen aanbrengen om deze te gebruiken. Als u het systeem wilt configureren om uw eigen objecten te gebruiken, volgt u deze stappen.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Configuratie van btw-rapporten** in en selecteer vervolgens de gerelateerde koppeling.
2. Voeg op de pagina **Configuratie van btw-rapporten** een nieuwe regel toe.
3. Selecteer in het veld **Type btw-rapport** en selecteer **Intrastat-rapport**.
4. Geef in het veld **Versie van btw-rapport** de versie van het rapport op.
5. Voeg uw codeunits toe voor de volgende opties:
   1. Geef in het veld **Codeunit-id voor regels voorstellen** de nieuwe codeunit op voor het voorstellen van regels op de Intrastat-rapportregels.
   2. Geef in het veld **Inhoud codeunit-id** de nieuwe codeunit op voor het exporteren van gegevens als een bestand met behulp van een definitie van gegevensuitwisseling.
   3. Geef in het veld **Codeunit-id valideren** de nieuwe codeunits op voor het valideren van resultaten binnen Intrastat-rapportregels.

> [!IMPORTANT]
> Deze regel moet leeg zijn als u de standaard codeunits gebruikt. U moet alleen een regel maken en configureren als u aangepaste codeunits heeft ontwikkeld.

## Overige Intrastat-configuraties

Klantenkaarten en leverancierskaarten bevatten het veld **Intrastat-partnertype**, dat dezelfde optiewaarden heeft als het veld **Partnertype**: 

- "" (leeg)
- *Bedrijf*
- *Persoon*
    
He veld **Intrastat-partnertype** vervangt het veld **Partnertype** in Intrastat-rapportage. Het veld **Partnertype** wordt gebruikt in de Single euro Payments Area (SEPA) om het SEPA Direct Debit Scheme (Core of B2B) te definiëren. Het veld **Intrastat-partnertype** wordt alleen gebruikt voor Intrastat-rapportage. Daarom kunt u indien nodig verschillende waarden voor de twee velden opgeven.

Als het veld **Intrastat-partnertype** leeg wordt gelaten, wordt de waarde van het veld **Partnertype** gebruikt voor Intrastat-rapportage.

Naast **Intrastat-rapport-instellingen**, **Definities van gegevensuitwisseling** en **Controlelijst voor Intrastat-rapporten** moeten de volgende instellingen ook worden geconfigureerd.

| Pagina | Omschrijving |
| ---- | ----------- |
| **Landen/Regio's** | Voeg op de pagina **Landen/regio's** informatie over de **EU-land/regio-code** en de **Intrastat-code** toe om een code op te geven voor het land/regio waarmee u handelt. Deze informatie wordt gebruikt voor Intrastat-rapportage. |
| **Tariefcodes** | In veel landen/regio's hanteren de belastingdienst en de douane codes van acht tekens voor verschillende artikelen. Om ervoor te zorgen dat artikelposten de benodigde informatie bevatten wanneer het programma ze van de Intrastat-dagboekregel importeert, moet u de artikelcode invoeren op de pagina **Tariefcodes**. Zoek de codes voor de artikelen waar uw bedrijf in handelt en geef ze op de pagina **Tariefcodes** op. |
| **Transportmethodes** | Er zijn zeven codes van één cijfer voor Intrastat-transportmethoden: **1** voor zee, **2** voor spoor, **3** voor weg, **4** voor lucht, **5** voor post, **7** voor vaste installaties en **9** voor eigen voortdrijving (bijvoorbeeld, een auto vervoeren door ermee te rijden). [!INCLUDE[prod_short](includes/prod_short.md)] vereist deze specifieke codes niet. We raden echter aan dat de beschrijvingen een vergelijkbare betekenis hebben. |
| **Transactiesoorten** | Landen/regio's hebben verschillende codes voor soorten Intrastat-transacties, zoals de gewone inkoop en verkoop, het ruilen van geretourneerde goederen en het ruilen van niet-geretourneerde goederen. Stel alle codes in die van toepassing zijn op uw land of regio. Deze codes worden vervolgens op het sneltabblad **Buitenlandse handel** gebruikt in verkoop- en inkoopdocumenten, en bij de verwerking van retouren. |
| **Transactieomschrijvingen** | Stel codes in als aanvulling op de transactiesoortbeschrijvingen. |
  
> [!NOTE]
> Vanaf januari 2022 vereist Intrastat andere transactie-aardcodes voor verzendingen naar particulieren of niet-btw-geregistreerde bedrijven en btw-geregistreerde bedrijven. Om aan deze vereiste te voldoen raden we u aan om nieuwe transactie-aardcodes te bekijken en/of toe te voegen op de pagina **Transactiesoorten**, volgens de vereisten in uw land/regio. U moet ook het veld **Intrastat-partnertype** controleren en bijwerken naar *Persoon* voor een particulier of niet-btw-geregistreerde zakelijke klanten op de relevante pagina **Klant**. Als u niet zeker weet welk Intrastat-partnertype of transactiesoort u moet gebruiken, raden we u aan een expert in uw land/regio te raadplegen.

|   Veld   |   Omschrijving   |
| --------- | --------------- |
| **Nettogewicht** | Gewicht is een van de basisconfiguraties met betrekking tot Intrastat-rapporten, aangezien het totale gewicht verplicht is voor rapportage. Om aan deze eis te kunnen voldoen, voert u een waarde in het veld **Nettogewicht** in op de artikelkaart of VA-kaart. |
| **Code van land/regio van oorsprong** | Gebruik de tweeletterige ISO-alfacodes op de artikel- of vaste-activakaart voor het land/de regio waar het goed is verkregen of geproduceerd. Als het goed in meer dan één land is geproduceerd, is het land van herkomst het laatste land waar het in belangrijke mate is verwerkt. |
| **Btw-identificatienummer van de partneroperator in de lidstaat van invoer** | Dit is het btw-identificatienummer van de partneroperator in de lidstaat van invoer. Het btw-nummer wordt ook gebruikt bij de uitwisseling van intra-EU exportgegevens tussen de lidstaten en stelt de lidstaten in staat de ontvangen gegevens toe te wijzen aan het importerende bedrijf in hun eigen land/regio. Rapporterende eenheden moeten het btw-nummer rapporteren van het bedrijf dat de intra-unie verwerving van goederen heeft aangegeven in de lidstaat van invoer. |

Eventueel kunt u ook het volgende instellen:

* **Basisproductcodes**: de belastingdienst en de douane hebben numerieke codes om artikelen en service te classificeren. U kunt deze codes opgeven voor artikelen.
* **Districten**: extra informatie over landen/regio's.
* **Invoer-/uitvoerhavens**: geef op naar welke locaties u artikelen wilt verzenden of wilt ontvangen naar of uit andere landen/regio's. Een luchthaven is een voorbeeld van een invoer-/uitvoerhaven. U voert invoer- of uitvoerhavens in op verkoop- of inkoopdocumenten op het sneltabblad **Buitenlandse handel**. Deze gegevens worden gekopieerd van de artikelposten wanneer u het Intrastat-dagboek maakt.
* **Aanvullende maateenheid**: de hoeveelheid goederen voor Intrastat-rapportage kan zowel nettogewicht (in kilogram) als een aanvullende eenheid zijn. Als er aanvullende eenheden nodig zijn, moet u deze configureren voor artikelen en vaste activa.

#### Transportmethoden instellen

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Transportmethodes** in en selecteer vervolgens de gerelateerde koppeling.
2. Vul indien nodig de veldinformatie in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### Transactieaardcodes instellen

1. selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Transactietypen** in en selecteer vervolgens de gerelateerde koppeling.
2. Vul indien nodig de veldinformatie in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### Andere gerelateerde configuraties

Voordat u de Intrastat-rapportagefunctie gebruikt, moet u velden definiëren op de artikel-, VA-, klant- en leverancierskaart.

#### Artikelkaarten

Volg deze stappen om alle benodigde informatie met betrekking tot Intrastat op artikelkaarten in te stellen.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer het artikel dat u wilt configureren.
3. Voer op het sneltabblad **Kosten en boeking** de velden **Tariefnr.**, **Aanvullende maateenheid** en **Code voor land/regio van herkomst** in.

    > [!NOTE]
    > Om een maateenheid te gebruiken als aanvulling op de basismaateenheid configureert u de aanvullende maateenheid op de pagina **Artikeleenheden instellen**.

4. Voer op het sneltabblad **Voorraad** een decimale waarde in het veld **Nettogewicht** in.

> [!NOTE]
> Wanneer u het tariefnummer toevoegt aan een maateenheid die voor het artikel is gedefinieerd, vult [!INCLUDE [prod_short](includes/prod_short.md)] automatisch het veld **Aanvullende maateenheid** in, gebaseerd op de configuratie van het tariefnummer. U kunt de waarde van het veld **Aanvullende maateenheid** naar behoefte wijzigen.

#### Vaste activa instellen voor Intrastat

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vaste activa** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer het vaste activum dat u wilt configureren.
3. Voer op het sneltabblad een waarde in de velden **Intrastat** **Tariefnr.**, **Nettogewicht** en **Aanvullende maateenheid** in.

> [!NOTE]
> U kunt verschillende maateenheden gebruiken als aanvullende maateenheid. Maar welke **Code van eenheid** u ook kiest, de **Hoeveelheid** ervan in Intrastat-rapporten is altijd 1.

#### Leveranciers instellen voor Intrastat

Voordat u een leverancier kunt opnemen in Intrastat-rapportage, voert u hun informatie in op de pagina **Leverancierskaart**. Geef bijvoorbeeld een **Land/regio-code** en een **Btw-registratienummer** op.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Leveranciers** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer de leverancier die u wilt configureren.
3. Stel op het sneltabblad **Intrastat** in de velden **Standaardtransactietype**, **Standaardtransactietype - Retouren** en **Standaardtransportmethode** een standaardwaarde voor elk veld in.
4. Geef op het sneltabblad **Betalingen** in het veld **Intrastat-partnertype** op of de leverancier een persoon of een bedrijf is.

#### Klanten instellen voor Intrastat

Voordat u een klant kunt opnemen in Intrastat-rapportage, voert u hun informatie in op de pagina **Klantenkaart**. U moet bijvoorbeeld een **Land/regio-code** en een **Btw-registratienummer** opgeven.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer de klant die u wilt configureren.
3. Stel op het sneltabblad **Intrastat** in de velden **Standaardtransactietype**, **Standaardtransactietype - Retouren** en **Standaardtransportmethode** de standaardwaarde voor elk veld in.
4. Geef op het sneltabblad **Betalingen** in het veld **Intrastat-partnertype** op of de leverancier een persoon of een bedrijf is.

#### Artikelen en vaste activa uitsluiten van Intrastat-rapportage

Als er een reden is om een specifiek artikel of vast activum uit te sluiten van Intrastat-rapportage, moet u een optie op hun kaart wijzigen.

##### Uitsluiten van een artikel voor Intrastat-rapportage

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer het artikel dat u wilt configureren en schakel vervolgens op het sneltabblad **Kosten en boeking** het selectievakje **Uitsluiten van Intrastat-rapport** in.

##### Een vast activum uitsluiten van Intrastat-rapportage

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vaste activa** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer het vaste activum dat u wilt configureren.
3. Selecteer op het sneltabblad **Intrastat** het selectievakje **Uitsluiten van Intrastat-rapport**.

#### Tariefcodes instellen

1. Selecteer het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Tariefcodes** in en selecteer vervolgens de gerelateerde koppeling  
2. Vul op de pagina **Tariefcodes** de velden in zoals wordt beschreven in de volgende tabel.

    | Veld | Omschrijving |  
    |-------|-------------|
    | **Nr.** | Hiermee wordt de tariefcode opgegeven. |
    | **Beschrijving** | Hiermee wordt een omschrijving van de gerelateerde tariefcode opgegeven. |
    | **Aanvullende eenheden** | Hiermee wordt opgegeven of de douane en de belastingdienst informatie vereisen over de hoeveelheid en de maateenheid voor dit artikel. |
    | **Conversiefactor** | Hiermee wordt de conversiefactor opgegeven voor de tariefcode. |
    | **Eenheid** | Hiermee wordt de maateenheid opgegeven voor de tariefcode. |

> [!NOTE]
> Als u een aanvullende maateenheid toevoegt, vraagt [!INCLUDE [prod_short](includes/prod_short.md)] of u gerelateerde artikelen wilt bijwerken. Als u ervoor kiest om gerelateerde artikelen bij te werken, wordt de **Maateenheid** op de pagina **Artikeleenheden instellen** bijgewerkt voor alle artikelen die dezelfde tariefcode hebben.
> 
> Wanneer u een tariefnummer toevoegt dat een gedefinieerde **Maateenheid** aan het artikel toevoegt, voegt [!INCLUDE [prod_short](includes/prod_short.md)] automatisch een nieuwe maateenheid toe aan de waarde **Artikeleenheden instellen** voor het artikel. Het **Aantal in eenheid** is gebaseerd op het veld **Afrondingsprecisie voor aantal** .

## Land/regio-specifieke Intrastat-instellingen invoeren

De Intrastat-vereisten zijn vergelijkbaar in alle lidstaten van de EU, hoewel er belangrijke uitzonderingen zijn. In theorie zouden de regels in alle lidstaten uniform moeten worden toegepast. Er zijn echter verschillen in implementatie omdat sommige lidstaten richtlijnen geven over hoe de algemene beginselen moeten worden toegepast in specifieke situaties (bijvoorbeeld handelsmonsters en retournering van goederen). Deze richtlijnen kunnen verschillende resultaten opleveren voor verschillende situaties. Daardoor kan de informatie die landen/regio's moeten invullen verschillen, evenals de bestandsindeling die ze moeten gebruiken voor rapportage.

### Oostenrijk

Intrastat-rapportage in Oostenrijk vereist twee verschillende bestanden voor ontvangsten en verzendingen. Volg deze stappen om te controleren of uw instellingen correct zijn.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Intrastat-rapportage-instellingen** in en selecteer vervolgens de gerelateerde koppeling.  
2. Controleer op het sneltabblad **Rapportage** of **Bestanden met ontvangsten/verzendingen splitsen** is geselecteerd. Als dat zo is, vindt u twee afzonderlijke waarden van **Code van definitie van gegevensuitwisseling** geconfigureerd. 
3. Controleer of het veld **Zip-bestand(en)** is geselecteerd om ervoor te zorgen dat rapportbestanden worden toegevoegd aan het zip-bestand.

Het proces van werken met Intrastat-rapporten is hetzelfde als de globale functie.

<!-- ### Belgium-->

### Tsjechië

De nieuwe Intrastat-rapportervaring voor Tsjechië is beschikbaar in releasewave 1 van 2023. In de tussentijd kunt u de functie **Intrastat-dagboek** blijven gebruiken.

### Finland

In Finland zijn er een paar extra stappen om Intrastat in te stellen. Intrastat-rapportage in Finland vereist twee verschillende bestanden voor ontvangsten en verzendingen. U vindt ook twee afzonderlijke waarden voor **Code van definitie van gegevensuitwisseling** geconfigureerd.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Intrastat-rapportage-instellingen** in en selecteer vervolgens de gerelateerde koppeling.  
2. Voer op de pagina **Intrastat-rapportinstellingen** op het sneltabblad **Bestand instellen** informatie in zoals beschreven in de volgende tabel.

    |                 Veld              |            Omschrijving                |  
    |------------------------------------|---------------------------------------|
    | **Aangepaste code** | Specificeert een aangepaste code voor de instellingsinformatie van het Intrastat-bestand. |
    | **Serienummer van bedrijf** | Specificeert een serienummer van een bedrijf voor de instellingsinformatie van het Intrastat-bestand. |

3. Controleer op het sneltabblad **Rapportage** of **Bestanden met ontvangsten/verzendingen splitsen** is geselecteerd.

Het proces van werken met Intrastat-rapporten is hetzelfde als de globale functie.

<!-- ### Germany-->

### Italië

De nieuwe Intrastat-rapportervaring voor Italië is beschikbaar vanaf februari 2023. In de tussentijd kunt u de functie **Intrastat-dagboek** blijven gebruiken.

<!-- ### France-->

### Zweden

Intrastat-rapportage in Zweden vereist twee verschillende bestanden voor ontvangsten en verzendingen. Volg deze stappen om te controleren of uw instellingen correct zijn.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Intrastat-rapportage-instellingen** in en selecteer vervolgens de gerelateerde koppeling.  
2. Controleer op het sneltabblad **Rapportage** of **Bestanden met ontvangsten/verzendingen splitsen** is geselecteerd. Als dat zo is, vindt u twee afzonderlijke waarden voor **Code van definitie van gegevensuitwisseling** geconfigureerd.

Het proces van werken met Intrastat-rapporten is hetzelfde als in de globale functie.

<!-- ### United Kingdom-->

## Zie gerelateerde training op [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## Zie ook

[Intrasta-rapporten in Business Central](finance-how-report-intrastat.md)  
[Financieel beheer](finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
