---
title: Wijzigingen controleren
description: U kunt een gebruikerslogboek activeren zodat u een historie hebt van eventuele wijzigingen in gegevens in getraceerde tabellen. U kunt ook activiteiten volgen met bepaalde soorten activiteitenlogboeken.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'user log, user activity, tracking'
ms.search.form: '592, 593, 594, 595, 710, 1366, 1367, 1368, 1369'
ms.date: 05/03/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Wijzigingen controleren

Een veelvoorkomende uitdaging bij veel bedrijfsbeheertoepassingen is het vermijden van ongewenste wijzigingen in gegevens. Het probleem kan variëren van een foutief telefoonnummer van een klant tot een foutieve boeking naar het grootboek. In dit artikel worden de mogelijkheden beschreven om erachter te komen wat er is gewijzigd, wie het heeft gewijzigd en wanneer de wijziging is aangebracht.

## Over het wijzigingslogbestand

Met het wijzigingslogbestand kunt u alle directe wijzigingen bijhouden die een gebruiker aanbrengt in de databasegegevens. U moet elke tabel en elk veld opgeven dat u door het systeem wilt laten registreren. Vervolgens activeert u het wijzigingslogbestand. Het wijzigingslogbestand is gebaseerd op wijzigingen die worden aangebracht in gegevens in de tabellen die u bijhoudt. Op de pagina **Wijzigingslogposten** worden posten chronologisch geordend en worden alle wijzigingen weergeven die worden aangebracht in de waarden in velden in tabellen die u opgeeft.

Het bijhouden van wijzigingen kan invloed hebben op de prestaties, doordat het tijd kan kosten en de database groter kan maken, wat u geld kan kosten. Houd rekening met het volgende om die kosten te verlagen:

- Wees voorzichtig met het kiezen van tabellen en bewerkingen.
- Voeg geen grootboekposten en geboekte documenten toe. Geef in plaats daarvan prioriteit aan systeemvelden zoals Gemaakt door en Aanmaakdatum.
- Gebruik niet het trackingtype **Alle velden**. Kies in plaats daarvan **Sommige velden** en volg alleen de belangrijkste velden.

> [!NOTE]
> In het wijzigingslogbestand worden geen wijzigingen bijgehouden voor velden die gebruikmaken van de `autoIncrement property`. Een voorbeeld van een veld dat de eigenschap gebruikt, is het veld Integer in de tabellen Foutmeldingen en Btw-rapportregel.

Ook om prestatieredenen wordt het wijzigingslogboek uitgeschakeld tijdens het upgradeproces van [!INCLUDE [prod_short](includes/prod_short.md)] naar de volgende versie. Naast het versnellen van het upgradeproces, helpt uitschakelen van het logboek ook om de rommel in het wijzigingslogboek te verminderen. Zodra de upgrade is voltooid, begint het logboek opnieuw met het bijhouden van wijzigingen.

> [!Important]
> Wijzigingen worden pas op de pagina **Wijzigingslogposten** weergegeven nadat de sessie van de gebruiker opnieuw is gestart, wat als volgt gebeurt:
>
> - De sessie is verlopen en vernieuwd.
> - De gebruiker heeft een ander bedrijf of rolcentrum geselecteerd.
> - De gebruiker heeft zich af- en weer aangemeld.

## Het wijzigingslogboek instellen

Op de pagina **Wijzigingslogbestandinstellingen** kunt u het wijzigingslogboek in- of uitschakelen. Wanneer u dat doet, wordt de activiteit geregistreerd, zodat u altijd kunt zien wie de wijziging heeft aangebracht.

Op de pagina **Wijzigingslogbestandinstellingen** kunt u als u de actie **Tabellen** kiest, opgeven voor welke tabellen u wijzigingen wilt bijhouden en welke wijzigingen moeten worden bijgehouden. [!INCLUDE[prod_short](includes/prod_short.md)] houdt ook verschillende systeemtabellen bij.

> [!NOTE]
> U kunt specifieke velden controleren op wijzigingen, zoals velden die gevoelige gegevens bevatten, door veldbewaking in te stellen. Als u dat doet, zal om redundantie te voorkomen de tabel met het veld niet beschikbaar zijn voor het instellen van het wijzigingslogboek. Zie voor meer informatie [Vertrouwelijke velden bewaken](across-log-changes.md#monitor-sensitive-fields).

Nadat u het wijzigingslogboek hebt ingesteld, hebt geactiveerd en gegevens hebt gewijzigd, kunt u de wijzigingen weergeven en filteren op de pagina **Wijzigingslogposten**. Als u posten wilt verwijderen, stelt u een bewaarbeleid in, waarbij u filters kunt instellen op basis van datums en tijden. Zie voor meer informatie over het bewaarbeleid in [Bewaarbeleid definiëren](admin-data-retention-policies.md).  

## Gegevens in het wijzigingslogboek analyseren

U kunt de functie **Gegevensanalyse** gebruiken om gegevens in het Wijzigingslogboek te analyseren op de pagina [Wijzigingslogposten](https://businesscentral.dynamics.com/?page=595) . U hoeft geen rapport uit te voeren of een andere toepassing, zoals Excel, te openen. De functie biedt een interactieve en veelzijdige manier om gegevens te berekenen, samen te vatten en te onderzoeken. In plaats van rapporten uit te voeren met opties en filters, kunt u meerdere tabbladen toevoegen die verschillende taken of weergaven van de gegevens vertegenwoordigen. Enkele voorbeelden zijn 'Wie heeft welke gegevens gewijzigd, en wanneer', of 'Gegevenswijzigingen per tabel/veld', of welke andere weergave dan ook die u maar kunt bedenken. Voor meer informatie over het gebruik van de functie **Gegevensanalyse** gaat u naar [Lijst- en querygegevens analyseren met de analysemodus](analysis-mode.md).

### Ad-hocanalysescenario's voor wijzigingslogboek

In de volgende secties vindt u voorbeelden van scenario's waarin het analyseren van het wijzigingslogboek u kan helpen bij het bewaken en controleren van belangrijke wijzigingen.

| Vlak | Actie | Deze pagina openen in de analysemodus | Deze velden gebruiken |
| ---- | ----- | ------------------------------- |------------------- |
| [Wie heeft welke gegevens gewijzigd, en wanneer](#example-who-changed-what-data-and-when) | Zien wie heeft welke gegevens heeft gewijzigd. | [Wijzigingslogposten](https://businesscentral.dynamics.com/?page=595) | **Gebruikers-id**, **Datum en tijd**, **Tabelbijschrift**, **Veldbijschrift**, **Primaire sleutelwaarde 2**, **Primaire sleutelwaarde 3**, **Wijzigingssoort**, **Oude waarde** en **Nieuwe waarde**. |
| [Gegevenswijzigingen per tabel/veld](#example-data-changes-by-tablefield) | Bekijk gegevenswijzigingen per tabel/veld en wie de wijziging heeft aangebracht. | [Wijzigingslogposten](https://businesscentral.dynamics.com/?page=595) | **Tabelbijschrift**, **Veldbijschrift**, **Gebruikers-id**, **Datum en tijd**, **Primaire sleutelwaarde 2**, **Primaire sleutelwaarde 3**, **Wijzigingssoort**, **Oude waarde** en **Nieuwe waarde**. |

### Voorbeeld: Wie heeft welke gegevens gewijzigd, en wanneer

Om te analyseren wie welke gegevens wanneer heeft gewijzigd, volgt u deze stappen:

1. Open de lijst [Wijzigingslogposten](https://businesscentral.dynamics.com/?page=595) en kies het pictogram :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus openen"::: om de analysemodus in te schakelen.
1. Verwijder in het menu **Kolommen** alle kolommen (selecteer het vakje naast het veld **Zoeken**, rechts).
1. Sleep het veld **Gebruikers-ID** (wie heeft dit gedaan) naar het gebied **Rijgroepen**.
1. Kies nu de volgende velden:
   - Kies om te laten zien wanneer het gebeurde **Datum en tijd**.
   - Kies om de tabel weer te geven waar het gebeurde **Tabelbijschrift**. 
   - Kies om weer te geven welk veld **Veldbijschrift**.
   - Om de veldcode weer te geven kiest u **Primaire sleutelwaarde 2**. 
   - Om de bedrijfsnaam weer te geven kiest u **Primaire sleutelwaarde 3**.
   - Als u wilt weergeven of de wijziging een actie voor invoegen, bijwerken of verwijderen was, kiest u **Wijzigingssoort**.
   - Om de wijziging weer te geven, kiest u **Oude waarde** en **Nieuwe waarde**.
1. Hernoem uw analysetabblad naar **Wie heeft welke gegevens wanneer gewijzigd** of iets dat deze analyse voor u beschrijft.

De volgende afbeelding toont het resultaat van deze stappen.

:::image type="content" source=" media/data-analysis-change-log-entries-Who-changed-What-data-When.png" alt-text="Voorbeeld van hoe u gegevensanalyse uitvoert op de pagina Wijzigingslogposten (wie heeft welke gegevens wanneer gewijzigd)." lightbox="media/data-analysis-change-log-entries-Who-changed-What-data-When.png":::

### Voorbeeld: gegevenswijzigingen per tabel/veld

Volg deze stappen om gegevenswijzigingen per tabel/veld te analyseren:

1. Open de lijst [Wijzigingslogposten](https://businesscentral.dynamics.com/?page=595) en kies het pictogram :::image type="content" source="media/analysis-mode-icon.png" alt-text="Analysemodus openen"::: om de analysemodus in te schakelen.
1. Verwijder in het menu **Kolommen** alle kolommen (selecteer het vakje naast het veld **Zoeken**, rechts).
1. Sleept de velden **Tabelbijschrift** (in welke tabel) en **Veldbijschrift** (in welk veld) naar het gebied **Rijgroepen**.
1. Kies nu de volgende velden:
   - Kies om te laten zien wanneer het gebeurde **Datum en tijd**
   - Kies om te laten zien wie de wijziging heeft aangebracht **Gebruikers-id**.
   - Om de veldcode voor het veld weer te geven kiest u **Primaire sleutelwaarde 2**.
   - Om de bedrijfsnaam weer te geven kiest u **Primaire sleutelwaarde 3** (meestal de bedrijfsnaam). 
   - Als u wilt weergeven of de wijziging een actie voor invoegen, bijwerken of verwijderen was, kiest u **Wijzigingssoort**.
   - Om de wijziging weer te geven, kiest u **Oude waarde** en **Nieuwe waarde**.
1. Hernoem uw analysetabblad naar **Gegevenswijzigingen per tabel + veld** of iets dat deze analyse voor u beschrijft.

De volgende afbeelding toont het resultaat van deze stappen.

:::image type="content" source=" media/data-analysis-change-log-entries-data-changes-by-table-field.png" alt-text="Voorbeeld van hoe u gegevensanalyse uitvoert op de pagina Wijzigingslogposten (gegevenswijzigingen per tabel/veld)." lightbox="media/data-analysis-change-log-entries-data-changes-by-table-field.png":::

## Over activiteitenlogboeken

Vanaf enkele pagina's in [!INCLUDE [prod_short](includes/prod_short.md)] kunt u een activiteitenlogboek bekijken dat de status en eventuele fouten weergeeft van bestanden waarnaar u exporteert vanuit of importeert in [!INCLUDE [prod_short](includes/prod_short.md)].  

### Werken met activiteitenlogboeken

De informatie wordt weergegeven op de pagina **Activiteitenlogboek**, volgens de context van waaruit u deze hebt geopend. U kunt de pagina bijvoorbeeld openen vanuit de pagina's **Documentuitwisselingsservice instellen**, **Inkomend document**, **Geboekte verkoopfactuur** en **Geboekte verkoopcreditnota**. U kunt de lijst met logboekvermeldingen leegmaken of gewoon de lijst met vermeldingen ouder dan zeven dagen wissen.  

## Vertrouwelijke velden bewaken

Het veilig en privé houden van gevoelige gegevens is voor de meeste bedrijven een belangrijk aandachtspunt. Om een beveiligingslaag toe te voegen kunt u belangrijke velden controleren en een e-mail ontvangen wanneer iemand een waarde wijzigt. U wilt bijvoorbeeld een melding ontvangen als iemand het IBAN-nummer van uw bedrijf wijzigt.

> [!NOTE]
> Voor het verzenden van meldingen per e-mail moet u de e-mailfunctie instellen in [!INCLUDE[prod_short](includes/prod_short.md)]. Zie [E-mail instellen](admin-how-setup-email.md) voor meer informatie.

### Veldcontrole instellen

U kunt de begeleide instelling **Instelling van controle van veldwijziging** gebruiken om de velden te specificeren die u wilt bewaken op basis van filtercriteria, zoals de gegevensgevoeligheidsclassificatie voor de velden. Zie voor meer informatie [Vertrouwelijkheid van gegevens classificeren](admin-classifying-data-sensitivity.md). In de handleiding kunt u ook de persoon specificeren die een e-mailmelding ontvangt wanneer er een wijziging plaatsvindt, en het e-mailaccount dat de e-mailmelding verzendt. Geef zowel de te informeren gebruiker op als het account van waaruit het bericht moet worden verzonden. Nadat u de begeleide instelling hebt voltooid, kunt u instellingen voor veldbewaking beheren op de pagina **Instelling van veldcontrole**.

> [!NOTE]
> Wanneer u het e-mailaccount opgeeft van waaruit u berichten wilt verzenden, moet u het accounttype **Microsoft 365** of **SMTP** toevoegen. Berichten moeten worden verzonden vanaf een account dat niet is gekoppeld aan een daadwerkelijke gebruiker. Daarom kunt u niet kiezen voor het accounttype **Huidige gebruiker**. Als u dit doet, worden er geen berichten verzonden.

Na verloop van tijd zal de lijst met vermeldingen op de pagina **Logboekvermeldingen van gecontroleerde velden** groeien. Om het aantal posten te verminderen kunt u een bewaarbeleid maken dat posten na een bepaalde tijd verwijdert. Zie voor meer informatie [Bewaarbeleid definiëren](admin-data-retention-policies.md).

Als u veldbewaking instelt of iets in de instellingen wijzigt, worden er vermeldingen gemaakt voor uw wijzigingen. U kunt aangeven of vermeldingen met betrekking tot de bewakingsinstellingen moeten worden weergegeven of verborgen.

U kunt instellingen voor veldbewaking beheren, zoals of u een e-mailmelding wilt verzenden of alleen de wijziging wilt vastleggen, voor elk veld op de pagina **Werkblad Velden controleren**. De pagina is ook waar u velden kunt toevoegen of verwijderen om te controleren.

> [!NOTE]
> Nadat u een of meer velden hebt toegevoegd en de controle hebt gestart, moet u zich afmelden bij [!INCLUDE[prod_short](includes/prod_short.md)] en u opnieuw aanmelden om uw instellingen toe te passen.

### Werken met veldbewaking

Invoer voor alle gewijzigde waarden voor bewaakte velden is beschikbaar op de pagina **Logboekvermeldingen van gecontroleerde velden**. Posten bevatten bijvoorbeeld de volgende informatie:

- Het veld waarvoor de waarde is gewijzigd.
- De oorspronkelijke en nieuwe waarden.
- Wie de verandering heeft aangebracht en wanneer ze dat hebben gedaan.

Om een wijziging verder te onderzoeken kiest u een waarde om de pagina te openen waarop deze is aangebracht. Kies om een lijst met alle vermeldingen weer te geven **Veldwijzigingsposten**.

### Veldbewakingstelemetrie bekijken

U kunt [!INCLUDE[prod_short](includes/prod_short.md)] instellen om veldbewakingsactiviteit naar een Application Insights-bron in Microsoft Azure te sturen. Vervolgens maakt u met behulp van Azure Monitor rapporten en stelt u waarschuwingen in voor de verzamelde gegevens. Zie voor meer informatie de volgende artikelen in de [!INCLUDE[prod_short](includes/prod_short.md)] Ontwikkelaar en IT Pro Help:

- [Telemetrie bewaken en analyseren - inschakelen Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview?toc=/dynamics365/business-central/toc.json#enable)
- [Veldbewakingstelemetrie bekijken](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace?toc=/dynamics365/business-central/toc.json)

## Bewaarbeleid definiëren

U kunt bewaarbeleid maken om onnodige gegevens in logboeken te verwijderen na een door u opgegeven periode. Zo kan het aantal vermeldingen in een logboek na verloop van tijd toenemen. Door oude vermeldingen op te schonen kunt u het gemakkelijker maken om u te concentreren op recentere en waarschijnlijk relevantere vermeldingen. Zie voor meer informatie over het bewaarbeleid [Bewaarbeleid definiëren](admin-data-retention-policies.md).

## Zie ook

[Vertrouwelijke velden bewaken](across-log-changes.md#monitor-sensitive-fields)  
[Veldbewakingstelemetrie bekijken](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace?toc=/dynamics365/business-central/toc.json)  
[Bewaarbeleid definiëren](admin-data-retention-policies.md)  
[Basisinstellingen wijzigen](ui-change-basic-settings.md)  
[Sorteren, zoeken en filteren](ui-enter-criteria-filters.md)  
[Pagina's en informatie zoeken met Vertel me](ui-search.md)  
[Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
