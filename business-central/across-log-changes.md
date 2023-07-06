---
title: Wijzigingen controleren
description: U kunt een gebruikerslogboek activeren zodat u een historie hebt van eventuele wijzigingen in gegevens in getraceerde tabellen. U kunt ook activiteiten volgen met bepaalde soorten activiteitenlogboeken.
author: edupont04
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'user log, user activity, tracking'
ms.search.form: '592, 593, 594, 595, 710, 1366, 1367, 1368, 1369'
ms.date: 03/24/2022
ms.author: edupont
---
# <a name="auditing-changes-in-business-central"></a><a name="auditing-changes-in-business-central"></a><a name="auditing-changes-in-business-central"></a>Wijzigingen controleren in Business Central

Een veelvoorkomende uitdaging bij veel bedrijfsbeheertoepassingen is het vermijden van ongewenste wijzigingen in gegevens. Het probleem kan variëren van een foutief telefoonnummer van een klant tot een foutieve boeking naar het grootboek. In dit onderwerp worden de mogelijkheden beschreven om erachter te komen wat er is gewijzigd, wie het heeft gewijzigd en wanneer de wijziging is aangebracht.

## <a name="about-the-change-log"></a><a name="about-the-change-log"></a><a name="about-the-change-log"></a>Over het wijzigingslogbestand

Met het wijzigingslogbestand kunt u alle directe wijzigingen bijhouden die een gebruiker aanbrengt in de databasegegevens. U moet elke tabel en elk veld opgeven dat u door het systeem wilt laten registreren. Vervolgens activeert u het wijzigingslogbestand. Het wijzigingslogbestand is gebaseerd op wijzigingen die worden aangebracht in gegevens in de tabellen die u bijhoudt. Op de pagina **Wijzigingslogposten** worden posten chronologisch geordend en worden alle wijzigingen weergeven die worden aangebracht in de waarden in velden in tabellen die u opgeeft. 

Het bijhouden van wijzigingen kan invloed hebben op de prestaties, doordat het tijd kan kosten en de database groter kan maken, wat u geld kan kosten. Houd rekening met het volgende om die kosten te verlagen:

- Wees voorzichtig met het kiezen van tabellen en bewerkingen.
- Voeg geen grootboekposten en geboekte documenten toe. Geef in plaats daarvan prioriteit aan systeemvelden zoals Gemaakt door en Aanmaakdatum.
- Gebruik niet het trackingtype Alle velden. Kies in plaats daarvan Sommige velden en volg alleen de belangrijkste velden.

Ook om prestatieredenen wordt het wijzigingslogboek uitgeschakeld tijdens het upgradeproces van [!INCLUDE [prod_short](includes/prod_short.md)] naar de volgende versie. Naast het versnellen van het upgradeproces, helpt dit ook om de rommel in het wijzigingslogboek te verminderen. Zodra de upgrade is voltooid, begint het logboek opnieuw met het bijhouden van wijzigingen.

> [!Important]
> Wijzigingen worden pas op de pagina **Wijzigingslogposten** weergegeven nadat de sessie van de gebruiker opnieuw is gestart, wat als volgt gebeurt:
>
> * De sessie is verlopen en vernieuwd.
> * De gebruiker heeft een ander bedrijf of rolcentrum geselecteerd.
> * De gebruiker heeft zich af- en weer aangemeld.

### <a name="work-with-the-change-log"></a><a name="work-with-the-change-log"></a><a name="work-with-the-change-log"></a>Werken met het wijzigingslogbestand
U activeert en deactiveert het wijzigingslogbestand op de pagina **Wijzigingslogbestandinstellingen**. Wanneer een gebruiker het wijzigingslogbestand activeert of deactiveert, wordt deze activiteit geregistreerd, zodat u altijd kunt zien welke gebruiker het wijzigingslogbestand heeft gedeactiveerd of opnieuw heeft geactiveerd.

Op de pagina **Wijzigingslogbestandinstellingen** kunt u als u de actie **Tabellen** kiest, opgeven voor welke tabellen u wijzigingen wilt bijhouden en welke wijzigingen moeten worden bijgehouden. [!INCLUDE[prod_short](includes/prod_short.md)] houdt ook verschillende systeemtabellen bij.

> [!NOTE]
> U kunt specifieke velden controleren op wijzigingen, zoals velden die gevoelige gegevens bevatten, door veldbewaking in te stellen. Als u dat doet, zal om redundantie te voorkomen de tabel met het veld niet beschikbaar zijn voor het instellen van het wijzigingslogboek. Zie voor meer informatie [Vertrouwelijke velden bewaken](across-log-changes.md#monitoring-sensitive-fields).

Nadat u het wijzigingslogbestand hebt ingesteld, hebt geactiveerd en gegevens hebt gewijzigd, kunt u de wijzigingen weergeven en filteren op de pagina **Wijzigingslogposten**. Als u posten wilt verwijderen, kunt u dat doen op de pagina **Wijzigingslogposten verwijderen**, waar u filters kunt instellen op basis van datums en tijd.  

## <a name="about-activity-logs"></a><a name="about-activity-logs"></a><a name="about-activity-logs"></a>Over activiteitenlogboeken

Vanaf enkele pagina's in [!INCLUDE [prod_short](includes/prod_short.md)] kunt u een activiteitenlogboek bekijken dat de status en eventuele fouten weergeeft van bestanden waarnaar u exporteert vanuit of importeert in [!INCLUDE [prod_short](includes/prod_short.md)].  

### <a name="work-with-activity-logs"></a><a name="work-with-activity-logs"></a><a name="work-with-activity-logs"></a>Werken met activiteitenlogboeken
De informatie wordt weergegeven op de pagina **Activiteitenlogboek**, volgens de context van waaruit deze wordt geopend. U kunt de pagina bijvoorbeeld openen vanuit de pagina's **Documentuitwisselingsservice instellen**, **Inkomend document**, **Geboekte verkoopfactuur** en **Geboekte verkoopcreditnota**. U kunt de lijst met logboekvermeldingen leegmaken of gewoon de lijst met vermeldingen ouder dan zeven dagen wissen.  

## <a name="monitoring-sensitive-fields"></a><a name="monitoring-sensitive-fields"></a><a name="monitoring-sensitive-fields"></a>Vertrouwelijke velden controleren

Het veilig en privé houden van gevoelige gegevens is voor de meeste bedrijven een belangrijk aandachtspunt. Om een beveiligingslaag toe te voegen kunt u belangrijke velden controleren en per e-mail een melding ontvangen wanneer iemand een waarde wijzigt. U wilt bijvoorbeeld een melding ontvangen als iemand het IBAN-nummer van uw bedrijf wijzigt.

> [!NOTE]
> Voor het verzenden van meldingen per e-mail moet u de e-mailfunctie instellen in [!INCLUDE[prod_short](includes/prod_short.md)]. Zie [E-mail instellen](admin-how-setup-email.md) voor meer informatie.

### <a name="setting-up-field-monitoring"></a><a name="setting-up-field-monitoring"></a><a name="setting-up-field-monitoring"></a>Veldcontrole instellen

U kunt de begeleide instelling **Instelling van controle van veldwijziging** gebruiken om de velden te specificeren die u wilt bewaken op basis van filtercriteria, zoals de gegevensgevoeligheidsclassificatie voor de velden. Zie voor meer informatie [Vertrouwelijkheid van gegevens classificeren](admin-classifying-data-sensitivity.md). In de handleiding kunt u ook de persoon specificeren die een e-mailmelding ontvangt wanneer er een wijziging plaatsvindt, en het e-mailaccount dat de e-mailmelding zal verzenden. Geef zowel de te informeren gebruiker op als het account van waaruit het bericht moet worden verzonden. Nadat u de begeleide instelling hebt voltooid, kunt u instellingen voor veldbewaking beheren op de pagina **Instelling van veldcontrole**. 

> [!NOTE]
> Wanneer u het e-mailaccount opgeeft van waaruit u berichten wilt verzenden, moet u het accounttype **Microsoft 365** of **SMTP** toevoegen. Berichten moeten worden verzonden vanaf een account dat niet is gekoppeld aan een daadwerkelijke gebruiker. Daarom kunt u niet kiezen voor het accounttype **Huidige gebruiker**. Als u dit doet, worden er geen berichten verzonden. 

Na verloop van tijd zal de lijst met vermeldingen op de pagina **Logboekvermeldingen van gecontroleerde velden** groeien. Om het aantal posten te verminderen kunt u een bewaarbeleid maken dat posten na een bepaalde tijd verwijdert. Zie voor meer informatie [Bewaarbeleid definiëren](admin-data-retention-policies.md).

Als u veldbewaking instelt of iets in de instellingen wijzigt, worden er vermeldingen gemaakt voor uw wijzigingen. U kunt aangeven of vermeldingen met betrekking tot de bewakingsinstellingen moeten worden weergegeven of verborgen. 

U kunt instellingen voor veldbewaking beheren, zoals of u een e-mailmelding wilt verzenden of alleen de wijziging wilt vastleggen, voor elk veld op de pagina **Werkblad Velden controleren**. De pagina is ook waar u velden kunt toevoegen of verwijderen om te controleren.

> [!NOTE]
> Nadat u een of meer velden hebt toegevoegd en de controle hebt gestart, moet u zich afmelden bij [!INCLUDE[prod_short](includes/prod_short.md)] en u opnieuw aanmelden om uw instellingen toe te passen.

### <a name="work-with-field-monitoring"></a><a name="work-with-field-monitoring"></a><a name="work-with-field-monitoring"></a>Werken met veldcontrole

Invoer voor alle gewijzigde waarden voor bewaakte velden is beschikbaar op de pagina **Logboekvermeldingen van gecontroleerde velden**. Posten bevatten bijvoorbeeld de volgende informatie:

* Het veld waarvoor de waarde is gewijzigd.
* De oorspronkelijke en nieuwe waarden.
* Wie de verandering heeft aangebracht en wanneer ze dat hebben gedaan. 

Om een wijziging verder te onderzoeken kiest u een waarde om de pagina te openen waarop deze is aangebracht. Kies om een lijst met alle vermeldingen weer te geven **Veldwijzigingsposten**.

### <a name="viewing-field-monitoring-telemetry"></a><a name="viewing-field-monitoring-telemetry"></a><a name="viewing-field-monitoring-telemetry"></a>Veldbewakingstelemetrie bekijken

U kunt [!INCLUDE[prod_short](includes/prod_short.md)] instellen om veldbewakingsactiviteit naar een Application Insights-bron in Microsoft Azure te sturen. Vervolgens maakt u met behulp van Azure Monitor rapporten en stelt u waarschuwingen in voor de verzamelde gegevens. Zie voor meer informatie de volgende artikelen in de [!INCLUDE[prod_short](includes/prod_short.md)] Ontwikkelaar en IT Pro Help:

- [Telemetrie bewaken en analyseren - inschakelen Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Veldbewakingstelemetrie bekijken](/dynamics365/business-central/dev-itpro/administration/telemetry-field-monitoring-trace)

## <a name="defining-retention-policies"></a><a name="defining-retention-policies"></a><a name="defining-retention-policies"></a>Bewaarbeleid definiëren

U kunt bewaarbeleid maken om onnodige gegevens in logboeken te verwijderen na een door u opgegeven periode. Zo kan het aantal vermeldingen in een logboek na verloop van tijd toenemen. Door oude vermeldingen op te schonen kunt u het gemakkelijker maken om u te concentreren op recentere en waarschijnlijk relevantere vermeldingen. Zie voor meer informatie [Bewaarbeleid definiëren](admin-data-retention-policies.md).

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Zie ook

[Basisinstellingen wijzigen](ui-change-basic-settings.md)  
[Sorteren, zoeken en filteren](ui-enter-criteria-filters.md)  
[Pagina's en informatie zoeken met Vertel me](ui-search.md)  
[Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md)    
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Bewaarbeleid definiëren](admin-data-retention-policies.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
