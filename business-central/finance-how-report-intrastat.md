---
title: Werken met Intrastat-rapportage
description: Leren hoe u handel met bedrijven in andere EU-landen/regio's kunt rapporteren met behulp van het Intrastat-systeem.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'electronic document, Intrastat, trade, EU, European Union'
ms.search.form: '308, 309, 310, 311, 325, 326, 327, 328, 405, 406, 4810, 4811, 8451, 12202, 31077'
ms.date: 01/10/2024
ms.author: altotovi
ms.service: dynamics-365-business-central
---
# <a name="work-with-intrastat-reporting"></a>Werken met Intrastat-rapportage

Bedrijven uit landen in de Europese Unie (EU) moeten handel met bedrijven uit andere landen/regio's in de EU rapporteren. In uw land/regio moet u de beweging van goederen elke maand doorgeven aan de autoriteiten en moet aangifte bij de belastingdienst worden gedaan. Intrastat is het systeem voor het verzamelen van statistische handelsgegevens van goederen binnen deze landen/regio's. U gebruikt **Intrastat-rapport** voor het voltooien van de periodieke Intrastat-rapportage (meestal maandelijks), het verzamelen, registreren en rapporteren van de handel in goederen conform de wetgeving van de lokale overheid.

Intrastat-rapportage is gebaseerd op fundamentele EU-regelgeving die voor alle landen/regio's geldt. In de praktijk zijn er echter enkele verschillen binnen de afzonderlijke landen/regio's. Elk land/regio heeft zijn eigen regels voor wat er precies moet worden gerapporteerd en hoe.

> [!IMPORTANT]  
> Dit artikel beschrijft de nieuwe Intrastat-ervaring die beschikbaar is in [!INCLUDE[prod_short](includes/prod_short.md)] vanaf releasewave 2 van 2022, inclusief uitgebreide functies en [moet worden ingeschakeld voor bestaande bedrijven](finance-how-setup-report-intrastat.md#enable-the-new-intrastat-experience). Neem contact op met uw beheerder om de nieuwe functie in te schakelen en in te stellen.
>
> Lees het artikel over installatie en gebruik van Intrastat van de vorige versie op [Intrastat instellen en rapporteren](finance-how-setup-report-intrastat-v20.md).

> [!NOTE]  
> Intrastat-informatie is niet van toepassing op het dienstenverkeer tussen landen/regio's, maar alleen op goederen (artikelen en vaste activa). Als de lokale overheid registratie van dienstenverkeer tussen landen/regio's verplicht stelt, kunt u dit doen met de functie **Servicedeclaratie**.
>
> Deze functie zal naar verwachting vanaf november 2022 beschikbaar zal zijn als app op [AppSource](https://go.microsoft.com/fwlink/?linkid=2081646). Op dat moment moet u, om de functie te kunnen gebruiken, deze eerst installeren op de pagina **Extensiebeheer**.

## <a name="fill-in-the-intrastat-report"></a>Het Intrastat-rapport invullen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Intrastat-lijst** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw** om een nieuw **Intrastat-rapport** te maken.
3. Als u interne informatie over het **Intrastat-rapport** moet invullen, voert u deze gegevens in het veld **Beschrijving** in.
4. Geef in het veld **Statistische periode** de maand op waarvoor u gegevens wilt rapporteren. Voer de periode in als een viercijferig getal zonder spaties of symbolen. Voer, afhankelijk van uw land/regio, eerst de maand in en daarna het jaar, of omgekeerd. U kunt bijvoorbeeld zowel *2206* als *0622* invoeren voor juni 2022.
5. Kies de actie **Regels voorstellen**. In de velden **Begindatum** en **Einddatum** zijn al de datums opgenomen die voor de statistiekperiode in de koptekst van het Intrastat-rapport zijn opgegeven.
6. U kunt een percentage voor transport en verzekering opgeven in het veld **Indirecte kosten %**. Als u een percentage opgeeft, wordt de inhoud van het veld **Statistiekwaarde** verhoudingsgewijs aangepast op basis van dit percentage. Maar als u deze functie wilt gebruiken, moet u he veld **Bedrag incl. artikeltoeslagen** op **Ja** zetten.
7. U kunt op den duur extra configuraties instellen op het sneltabblad **Aanvullend**:
   1. **Herberekening voor nulbedragen overslaan** om op te geven dat regels zonder bedragen niet opnieuw worden berekend tijdens de batchverwerking.
   2. **Nulbedragen overslaan** om op te geven dat artikelposten zonder aantallen niet worden opgenomen in de batchverwerking.
   3. **Niet-gefactureerde posten overslaan** om op te geven of artikelposten die zijn verzonden of ontvangen maar nog niet zijn gefactureerd moeten worden uitgesloten van het proces.
8. Kies **OK** om de batchverwerking te starten.

Met de batchverwerking worden alle artikelposten in de statistiekperiode opgehaald en als regels in het **Intrastat-rapport** ingevoegd. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="modify-the-intrastat-report"></a>Het Intrastat-rapport wijzigen

Indien nodig kunt u de regels wijzigen, maar telkens wanneer u een waarde in de Intrastat-rapportregel wijzigt, wordt het veld **Correctie** automatisch gemarkeerd als **Ja**. Op den duur kunt u handmatig een nieuwe regel toevoegen als daar een reden voor is. Handmatig een nieuwe regel toevoegen:

1. Kies op de pagina **Intrastat-rapport** op het sneltabblad **Regels** de actie **Nieuwe regel**.
2. Kies de optie **Ontvangst** of **Verzending** in het veld **Type**.
3. Kie sin het veld **Bronsoort** een van de bronnen: **Artikelpost**, **FA-post** of **Projectpost**.
4. Gebaseerd op de **Bronsoort** in het veld **Artikelnr.** kunt u een **Artikel** kiezen (in beide gevallen, **Artikelpost** of **Projectpost**) of **Vaste activa**.
5. Vul andere velden in die u nodig heeft voor de Intrastat-rapportage.

> [!NOTE]  
> Wanneer u handmatig een nieuwe regel aan het Intrastat-rapport toevoegt, moet het veld **Datum** in de regel binnen het bereik voor **Statistische periode** vallen dat u in de koptekst hebt toegevoegd.

## <a name="validate-intrastat-lines"></a>Intrastat-regels valideren

Nadat u het **Intrastat-rapport** hebt ingevuld, kunt u de actie **Controlelijstrapport** uitvoeren om te zorgen dat alle gegevens in het **Intrastat-rapport** correct zijn. Verplichte velden die u op de pagina **Controlelijst van Intrastat-rapport** hebt ingesteld en waarvoor waarden ontbreken, worden weergegeven in het feitenblok **Fouten en waarschuwingen** op de pagina **Intrastat-rapport**.

Voer de **Controlelijst van Intrastat-rapport** uit om Intrastat-regels te controleren voordat deze naar de vereiste indeling worden geëxporteerd. De controle wordt uitgevoerd in het **Intrastat-rapport**.

## <a name="recalculating-weight-or-supplementary-unit-of-measure"></a>Gewicht of aanvullende maateenheid herberekenen

Als u de foutmelding *Totaalgewicht in Intrastat-rapportregel mag niet leeg zijn* hebt gekregen, komt dit waarschijnlijk doordat u het veld **Nettogewicht** voor de gebruikte bron, het artikel of het vaste activum niet hebt ingesteld. Zoek in dit geval naar de kaart van het artikel of het vaste activum en voeg de vereiste waarde toe. Daarna hoeft u alleen het **Intrastat-rapport** opnieuw te openen en deze stappen te volgen:

1. Kies de actie **Gewicht/aanv. maateenheid herberekenen** om het **Totaalgewicht** en/of de **Aanvullende hoeveelheid** opnieuw te berekenen.
2. Kies een van de opties:

    1. **Gewicht** – om alleen het **Totaalgewicht** opnieuw te berekenen, op basis van de huidige informatie over **Nettogewicht** op de kaarten van het artikel en vaste activum.
    2. **Aanvullend aantal maateenheden** – om alleen de **Aanvullende hoeveelheid** op de **Intrastat-rapport** regel opnieuw te berekenen als deze bestaat, op basis van de actuele gegevens over **Aanvullende maateenheid** op de kaarten voor het artikel en vaste activum.
    3. **Beide** – om zowel het **Totaalgewicht** als de **Aanvullende hoeveelheid** opnieuw te berekenen, op basis van de actuele gegevens op de kaarten van het artikel en vaste activum.
3. Kies **OK** om de batchverwerking te starten.

## <a name="report-intrastat-in-a-file"></a>Intrastat in een bestand rapporteren

U kunt het Intrastat-rapport als bestand indienen op basis van de eisen van verschillende lokale autoriteiten. Voordat u het bestand maakt, moet u de **Controlelijstrapport** uitvoeren om te controleren of alle regels alle noodzakelijke en geldige gegevens bevatten. Een bestand maken:

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Intrastat-lijst** in en kies vervolgens de gerelateerde koppeling.
2. Kies **Intrastat-rapport** u wilt rapporteren als een bestand.
3. Als u dit nog niet hebt gedaan, vult u het **Intrastat-rapport** handmatig in of kiest u de actie **Regels voorstellen**.
4. Kies de actie **Bestand maken**.
5. Het Intrastat-bestand wordt opgeslagen in de vereiste indeling.

Zodra u het bestand maakt, vult [!INCLUDE[prod_short](includes/prod_short.md)] automatisch de volgende gegevens over rapportage in:

* De **Exportdatum** om de datum op te geven waarop het rapport is geëxporteerd.
* De **Exporttijd** om het tijdstip op te geven waarop het rapport is geëxporteerd.

> [!NOTE]  
> De volgende keer dat u een bestand aanmaakt, behouden de velden **Exportdatum** en **Exporttijd** alleen gegevens over het laatste bestand dat u hebt gemaakt.

## <a name="intrastat-rules"></a>Intrastat-regels

### <a name="grouping-lines"></a>Regels groeperen

In **Intrastat-rapport** regels is er geen groepering op velden. Alle posten worden gekopieerd vanuit de originele bron, zodat u ze snel kunt vinden op basis van de combinatie van **Bronsoort** en **Bronpostnr.**.

Groepering vereist door autoriteiten wordt verstrekt in het geëxporteerde bestand. U moet dit configureren in de **Definitie van gegevensuitwisseling**, die volledig configureerbaar is. Meer informatie vindt u in [Definities van gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md).

### <a name="fixed-assets-reporting"></a>Vaste activa rapporteren

Vaste activa worden alleen in de Intrastat-regels weergegeven als:

* De **FA-boekingssoort** in het veld **Btw-grootboekpost** **Aanschafkosten** is en als het **Documentsoort** **Factuur** is in het geval van aankopen, en
* De **FA-boekingssoort** in het veld **Btw-grootboekpost** **Opbrengst bij BGS** is en als de **Documentsoort** **Factuur** is in het geval van verlopen.

### <a name="intrastat-report-statuses"></a>Intrastat-rapportstatussen

Wanneer u met het **Intrastat-rapport** werkt ziet u een veld **Status** in de documentkop. Hier kunt u de volgende statussen en bijbehorende regels aantreffen:

* **Open**:deze status wordt automatisch aangemaakt wanneer u een nieuw Intrastat-rapport aanmaakt en u kunt alle bewerkingen uitvoeren in deze status.
* **Vrijgegeven**: [!INCLUDE[prod_short](includes/prod_short.md)] verandert de status automatisch in *Vrijgegeven* wanneer u een bestand aanmaakt. Vanaf dat moment kunt u uw **Intrastat-rapport** niet meer wijzigen. Als u iets moet wijzigen en opnieuw moet rapporteren, kunt u de actie **Heropenen** gebruiken om het Intrastat-rapport opnieuw te openen. Zodra het document opnieuw is geopend, kunt u de actie **Vrijgeven** gebruiken om het document weer vrij te geven.
* **Gerapporteerd**: hiermee wordt aangegeven of de post al is gemeld bij de belastingdienst. Dit is geen normale status maar een onafhankelijk veld, en zelfs als u het Intrastat-rapport opnieuw zou openen, zou het nog steeds aangeven dat het bestand al is gemaakt voor dit rapport.

### <a name="locations-in-intrastat-reporting"></a>Vestigingen in Intrastat-rapportage

[!INCLUDE[prod_short](includes/prod_short.md)] gebruikt altijd de informatie in het veld **Land/regiocode** op de pagina **Vestigingskaart** als het land voor **verzenden van** of voor **ontvangen naar** goederen. Wanneer deze informatie niet bestaat of de vestiging niet is gebruikt, gebruikt het systeem de informatie van de pagina **Bedrijfsgegevens**.   

> [!NOTE]  
> Als het bedrijf vanuit meer dan één land opereert, werkt Intrastat-rapportage niet voor alle landen/regio's waar vestigingen zijn geconfigureerd. De rapportage is alleen gebaseerd op het hoofdland/regio, omdat het momenteel niet mogelijk is om rapportage voor meerdere landen/regio's te gebruiken.  

### <a name="triangular-trade-in-intrastat"></a>Driehoekshandel in Intrastat

Bij driehoekshandel gaat het om handel tussen drie landen of regio's waarbij goederen het land van het rapporterende bedrijf omzeilen. In Business Central kan dit worden gefaciliteerd via de functionaliteit [Doorverzending](sales-how-drop-shipment.md). Om deze optie in te schakelen, activeert u het veld **Doorverzending opnemen** in de **Intrastat-rapportinstellingen**.  

Wanneer u deze optie inschakelt, gebruikt het systeem de volgende regels, maar alleen als u **Doorverzending** hebt gemarkeerd in de **verkooporder**: 

| Ontvangen van | Leveren aan | Verwacht Intrastat-resultaat |
|----------|------------|----------------------|
| Land als in de **bedrijfsgegevens** | Land als in de **bedrijfsgegevens** | Geen Intrastat-regels |  
| Land als in de **bedrijfsgegevens** | EU-land anders dan het land in de **bedrijfsgegevens** | Intrastat-verzendregel | 
| Land als in de **bedrijfsgegevens** | Niet-EU-land | Geen Intrastat-regels |   
| EU-land anders dan het land in de **bedrijfsgegevens** | Land als in de **bedrijfsgegevens** | Intrastat-ontvangstregel | 
| EU-land anders dan het land in de **bedrijfsgegevens** | EU-land anders dan het land in de **bedrijfsgegevens** | Geen Intrastat-regels |
| EU-land anders dan het land in de **bedrijfsgegevens** | Niet-EU-land | Geen Intrastat-regels | 
| Niet-EU-land | Land als in de **bedrijfsgegevens** | Geen Intrastat-regels |  
| Niet-EU-land | EU-land anders dan het land in de **bedrijfsgegevens** | Geen Intrastat-regels |
| Niet-EU-land | Niet-EU-land | Geen Intrastat-regels |   

## <a name="see-also"></a>Zie ook

[Intrastat-rapportage instellen](finance-how-setup-report-intrastat.md)  
[Financieel beheer](finance.md)  
[Doorverzending](sales-how-drop-shipment.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
