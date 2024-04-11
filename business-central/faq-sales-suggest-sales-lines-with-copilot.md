---
title: Veelgestelde vragen over suggesties voor verkoopregels met Copilot
description: Deze veelgestelde vragen bieden informatie over de AI-technologie die wordt gebruikt in Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: article
ms.search.form: null
ms.date: 02/02/2024
ms.service: dynamics-365-business-central
ms.collection: bap-ai-copilot
ms.custom: responsible-ai-faqs
---

# <a name="faq-for-sales-line-suggestions-with-copilot-preview"></a>Veelgestelde vragen over suggesties voor verkoopregels met Copilot (preview)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

Deze veelgestelde vragen (FAQ) beschrijven de AI-impact van de functie voor verkoopregelsuggesties in [!INCLUDE [prod_short](includes/prod_short.md)].

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## <a name="what-is-sales-line-suggestions-with-copilot"></a>Wat houdt Suggesties voor verkoopregels met Copilot in?

Verkoopregelsuggesties met Copilot kunnen helpen bij het maken van regels in verkoopdocumenten zoals verkoopoffertes, orders en facturen op basis van gestructureerde invoer of natuurlijke taal. De functie is geen chat voor algemene doeleinden, maar een zeer specifieke en geïntegreerde ervaring die u kunt gebruiken voor verkoopdocumenten. De functie biedt twee verschillende vaardigheden waarmee u gegevens over afzonderlijke producten of volledige documenten kunt vinden.

## <a name="what-are-capabilities-of-sales-line-suggestions-with-copilot"></a>Wat zijn de mogelijkheden van verkoopregelsuggesties met Copilot?

* Producten vinden

  Informatie die producten beschrijft, wordt op meerdere plaatsen opgeslagen in [!INCLUDE [prod_short](includes/prod_short.md)]. Zo worden artikelnummers en omschrijvingen opgeslagen in de tabel **Artikel**, worden meerdere barcodes opgeslagen in de tabel **Artikelreferentie** en worden producteigenschappen opgeslagen in de tabel **Artikelkenmerken**. Terwijl u misschien vraagt naar een *Rode fiets*, kan het daadwerkelijke product een *karmozijnrode toerfiets*, waar *Fiets* is een productcategorie en *rood* een kenmerk.

* Een document zoeken op verwijzing

  Vaak herhalen mensen een eerdere bestelling of gebruiken ze deze op zijn minst als uitgangspunt. Maar het kan lastig zijn om de juiste volgorde in een reeks bestellingen te vinden. Mogelijk herinnert u zich een deel van de id van de bestelling. Dit kan een door het bedrijf toegewezen nummer zijn of een referentienummer dat u van een klant hebt ontvangen. Als u prompts kunt gebruiken als *Laatste factuur van april nodig*, zou u een bestelling sneller moeten kunnen vinden.

## <a name="what-is-the-intended-use-of-sales-line-suggestions-with-copilot"></a>Wat is het beoogde gebruik van verkoopregelsuggesties met Copilot?

* Producten vinden

  Ze zijn bedoeld om gebruikersvragen te beantwoorden om producten te vinden op basis van vage, onvolledige of onnauwkeurige beschrijvingen.

  Omdat het gemiddelde aantal artikelen (producten/services) voor [!INCLUDE [prod_short](includes/prod_short.md)]-klanten 10.000 is, kan het vinden van de juiste artikelen lastig zijn zonder reeds opgedane ervaring of kennis. De manier waarop gegevens worden opgeslagen in [!INCLUDE [prod_short](includes/prod_short.md)] maakt het er niet eenvoudiger op, omdat u meerdere zoekopdrachten of filters moet uitvoeren op de verschillende pagina's waarop productgegevens worden opgeslagen.

  Copilot extraheert de gevraagde producten en hoeveelheden en identificeert de belangrijkste zoekterm en kenmerken, zodat u uw vraag sneller kunt invoeren. Vervolgens voert Copilot een geavanceerde zoekopdracht uit in meerdere gerelateerde tabellen, past synoniemen toe, corrigeert typefouten en evalueert de kwaliteit van de zoekuitvoer.

* Een document zoeken op verwijzing

  Bedoeld om vragen van gebruikers te beantwoorden om bestaande verkoopdocumenten voor een specifieke klant te vinden met behulp van gedeeltelijke informatie of gegevens bij benadering.

  In B2B-omgevingen hebben mensen vaak te maken met terugkerende verzoeken, en orderverwerkers kunnen verzoeken krijgen om een vorig document te herhalen of op zijn minst als uitgangspunt te gebruiken. Maar het kan om verschillende redenen lastig zijn om er een te vinden:

  - Gedurende de levenscyclus kan een verkoopdocument evolueren van offerte naar order tot geboekte factuur of verzending. Documenten kunnen ook worden gearchiveerd.
  - Het kan zijn dat u een exacte id hebt, maar niet kunt zeggen wat deze vertegenwoordigt. Is het bijvoorbeeld een ordernummer, factuurnummer of externe verwijzing?
  - Soms hebt u wel een datum of een periode, maar geen id voor document.

  Om handmatig een brondocument te vinden, moet u meerdere pagina's openen en meerdere keren zoeken en filteren. Copilot kan dit echter vereenvoudigen in één enkele zoekopdracht in natuurlijke taal, waarmee u op uw eigen manier kunt uitdrukken wat u zoekt. 

  * *Haal producten van order 103031 op*
  * *Producten nodig van laatste factuur in augustus*

## <a name="how-was-sales-line-suggestions-with-copilot-evaluated-what-metrics-are-used-to-measure-performance"></a>Hoe is de evaluatie van verkoopregelsuggesties met Copilot verlopen? Welke statistieken worden gebruikt om de prestaties te meten?

De functie is uitgebreid getest, waarbij talloze prompts in het Amerikaans-Engels zowel typisch gebruik als gebruik door slechte actoren vertegenwoordigden. Het testen was gebaseerd op de demonstratiegegevens van [!INCLUDE [prod_short](includes/prod_short.md)] en een grote gelabelde productcatalogus die beschikbaar was als open source.

Deze functie is gebouwd in overeenstemming met de Responsible AI Standard van Microsoft. [Lees meer over verantwoorde AI van Microsoft](https://aka.ms/RAI).

## <a name="what-are-the-limitations-of-sales-line-suggestions-with-copilot-how-can-users-minimize-the-impact-of-the-sales-line-suggestions-with-copilot-limitations-when-using-the-system"></a>Wat zijn de beperkingen van verkoopregelsuggesties met Copilot? Hoe kunnen gebruikers de impact van de beperkingen van verkoopregelsuggesties met Copilot minimaliseren wanneer het systeem wordt gebruikt?

* Producten vinden
  
  Producten zoeken werkt het beste in de Engelse taal. Hoewel u deze functie in elke taal kunt gebruiken die [!INCLUDE [prod_short](includes/prod_short.md)] ondersteunt, kunnen zoekopdrachten naar items in andere talen minder nauwkeurig zijn.

Als uw branche of domein overlapt met wat Microsoft als gevoelige onderwerpen beschouwt (zoals drugs, geweld, entertainment voor volwassenen, enzovoort), kan Copilot overgaan op neutrale, samengestelde antwoorden of onnauwkeurige antwoorden geven.

Met suggesties voor verkoopregels worden alleen velden voor **Type** als **Artikel**, **Nr.** en **Hoeveelheid** ingevuld zoals beschreven. Andere velden, zoals **Maateenheid**, **Eenheidsprijs** en **Locatie** gebruiken de huidige logica en worden ingevuld op basis van artikelinstellingen of overgenomen waarden uit de documentkop.

**Variantcode** wordt momenteel niet ondersteund. Als u een product bijvoorbeeld in twee verschillende kleuren kunt verzenden, zoekt Copilot het benodigde product op, maar laat het veld **Variantcode** leeg. U moet het veld handmatig invullen.

Hoe u uw producten benoemt, kan de uitvoer beïnvloeden. Het gebruik van cryptische afkortingen in plaats van gebruiksvriendelijke namen kan bijvoorbeeld de uitvoerkwaliteit verminderen.

Voor producten bevat de volgende tabel de tabellen en velden waarin Copilot zoekt.

|Tafel  |Velden  |
|---------|---------|
|**Artikelen**     |  * Nr.<br>* Beschrijving<br>* Beschrijving 2<br>* Zoekbeschrijving<br>* GTIN<br>* Leveranciersartikelnummer       |
|**Artikelvariant**     | * Code<br>* Beschrijving<br>* Beschrijving 2          |
|**Artikelreferentie**     | * Verwijzingsnr.<br>* Beschrijving<br>* Beschrijving 2        |
|**Artikelkenmerken**     | * Naam<br>* Waarde        |
|**Artikelcategorie**     |  * Code<br>* Beschrijving<br>* Bovenliggende categorie - 1 niveau           |
|**Artikelvertaling**     | * Taal<br>* Beschrijving<br>* Beschrijving 2          |
|**Artikelidentificatie**     |  * Code       |
|**Uitgebreide tekstregel**     |  * Tekst      |

* Documenten zoeken op verwijzing

  Momenteel kunt u de suggestie voor verkoopregels starten vanuit verkooporders, facturen en offertes, en de volgende documenten doorzoeken:

  * Verkooporders
  * Verkoopoffertes
  * Verkoopfacturen
  * Geboekte verkoopfacturen
  * Geboekte verkoopverzendingen

  Copilot doorzoekt de volgende velden

  * Documentnr.
  * Extern documentnr.
  * Uw referentie
  * Offertenr.
  * Documentdatum
  * Klantnr. verkoopadres

  Copilot retourneert niet alle regels van het type Artikel. Alleen artikelnummers, variantcodes en hoeveelheden worden overgebracht. Hoeveelheden uit het brondocument worden omgezet naar de **Verkoopeenheid**.

## <a name="in-which-geographies-and-languages-is-sales-lines-suggestions-available"></a>In welke geografieën en talen zijn verkoopregelsuggesties beschikbaar?

Met uitzondering van Canada is deze functie beschikbaar voor alle land-/regiolokalisaties in de omgeving en in alle ondersteunde talen. Vanwege de beperkte taalondersteuning is de functie in eerste instantie niet beschikbaar voor Canadese klanten omdat niet wordt voldaan aan de regelgeving voor taal. Om deze mogelijkheid beschikbaar te maken voor klantomgevingen in landen/regio's waar de Azure OpenAI-service niet wordt geïmplementeerd, moeten beheerders eerst toestemming geven om verplaatsing van hun gegevens over de grenzen heen toe te staan voor [!INCLUDE [prod_short](includes/prod_short.md)] om verbinding te maken met de Azure OpenAI-service.  

## <a name="what-operational-factors-and-settings-allow-for-effective-and-responsible-use-of-the-feature"></a>Welke operationele factoren en instellingen maken een effectief en verantwoordelijk gebruik van de functie mogelijk?

Suggesties op basis van AI kunnen soms onjuist of onvolledig zijn. U dient altijd de juistheid van de suggesties van Copilot te beoordelen voordat u beslist of u deze wilt behouden. Suggesties van Copilot worden pas in de [!INCLUDE [prod_short](includes/prod_short.md)]-database opgeslagen als u de knop **Behouden** kiest en het Copilot-venster sluit. U kunt suggesties bewerken en corrigeren voordat u ervoor kiest deze te behouden, of nadat ze in een verkoopdocument zijn ingevoegd.

### <a name="what-is-expected-of-administrators-and-end-users-when-using-sales-lines-suggestions"></a>Wat wordt er van beheerders en eindgebruikers verwacht bij het gebruik van verkoopregelsuggesties?

Elke individuele gebruiker kiest zelf voor het wel of niet gebruiken van **Suggesties voor verkoopregels**. Zelfs als de functie is ingeschakeld door beheerders en beschikbaar is, kunt u ervoor kiezen deze altijd, soms of nooit te gebruiken.  

Beheerders nemen de algemene beslissing over het al dan niet gebruiken van de Copilot-mogelijkheden in [!INCLUDE [prod_short](includes/prod_short.md)]. Als beheerders Copilot inschakelen, moeten ze ervoor zorgen dat ze toegang verlenen aan de juiste gebruikers.   

> [OPMERKING!]
> - We ondersteunen deze functie niet in [!INCLUDE [prod_short](includes/prod_short.md)] on-premises of in de privécloud.
> - Partners kunnen deze functie niet uitbreiden. Dat betekent dat partnerontwikkelaars de functie niet kunnen wijzigen, vervangen of uitbreiden.

## <a name="is-copilot-the-only-means-to-create-sales-lines"></a>Is Copilot het enige middel om verkoopregels te maken?

Nee, het gebruik van Copilot is optioneel. [!INCLUDE [prod_short](includes/prod_short.md)] biedt niet door AI aangestuurde manieren om verkoopregels in te voegen of documenten te kopiëren. Organisaties kunnen beide benaderingen tegelijkertijd gebruiken.  

## <a name="how-do-i-give-feedback-about-ai-generated-content"></a>Hoe geef ik feedback over door AI gegenereerde inhoud?

Elke keer dat Copilot suggesties biedt, kunt u rechtstreeks vanuit het Copilot-venster feedback aan Microsoft geven met behulp van de knoppen Vind ik leuk en Niet leuk. Uw feedback blijft anoniem en wij gebruiken deze gegevens om de kwaliteit van de dienstverlening te verbeteren.  

## <a name="see-also"></a>Zie ook

[Regels op verkooporders voorstellen met Copilot](sales-suggest-sales-lines-with-copilot.md)  
[Copilot- en AI-mogelijkheden configureren](enable-ai.md)  
[Veelgestelde vragen over verantwoorde AI voor Dynamics 365 Business Central](responsible-ai-overview.md)  
