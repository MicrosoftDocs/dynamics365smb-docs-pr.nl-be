---
title: Wijzigingen controleren | Microsoft Docs
description: U kunt een gebruikerslogboek activeren zodat u een historie hebt van eventuele wijzigingen in gegevens in getraceerde tabellen. U kunt ook activiteiten volgen met bepaalde soorten activiteitenlogboeken.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 1497051beebd01839dfc4b4fe2dce6b46977eef4
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922679"
---
# <a name="auditing-changes-in-business-central"></a>Wijzigingen controleren in Business Central
Een veelvoorkomende uitdaging bij veel bedrijfsbeheertoepassingen is het vermijden van ongewenste wijzigingen in gegevens. Het probleem kan variëren van een foutief telefoonnummer van een klant tot een foutieve boeking naar het grootboek. In dit onderwerp worden de mogelijkheden beschreven om erachter te komen wat er is gewijzigd, wie het heeft gewijzigd en wanneer de wijziging is aangebracht.

## <a name="about-the-change-log"></a>Over het wijzigingslogbestand 
Met het wijzigingslogbestand kunt u alle directe wijzigingen bijhouden die een gebruiker aanbrengt in de databasegegevens. U moet elke tabel en elk veld opgeven dat u door het systeem wilt laten registreren. Vervolgens moet u het wijzigingslogbestand instellen.  

Het wijzigingslogbestand is gebaseerd op wijzigingen die worden aangebracht in gegevens in de tabellen die u bijhoudt. Op de pagina **Wijzigingslogposten** worden posten chronologisch geordend en worden alle wijzigingen weergeven die worden aangebracht in de waarden in velden in tabellen die u opgeeft.

> [!Important]
> Wijzigingen worden pas op de pagina **Wijzigingslogposten** weergegeven nadat de sessie van de gebruiker opnieuw is gestart, wat als volgt gebeurt:
<br />
> * De sessie is verlopen en vernieuwd.
> * De gebruiker heeft een ander bedrijf of rolcentrum geselecteerd.
> * De gebruiker heeft zich af- en weer aangemeld.

### <a name="working-with-the-change-log"></a>Werken met het wijzigingslogbestand
U activeert en deactiveert het wijzigingslogbestand op de pagina **Wijzigingslogbestandinstellingen** . Wanneer een gebruiker het wijzigingslogbestand activeert of deactiveert, wordt deze activiteit geregistreerd, zodat u altijd kunt zien welke gebruiker het wijzigingslogbestand heeft gedeactiveerd of opnieuw heeft geactiveerd.

Op de pagina **Wijzigingslogbestandinstellingen** kunt u als u de actie **Tabellen** kiest, opgeven voor welke tabellen u wijzigingen wilt bijhouden en welke wijzigingen moeten worden bijgehouden. [!INCLUDE[d365fin](includes/d365fin_md.md)] houdt ook een aantal systeemtabellen bij.

> [!NOTE]
> U kunt specifieke velden controleren op wijzigingen, zoals velden die gevoelige gegevens bevatten, door veldbewaking in te stellen. Als u dat doet, zal om redundantie te voorkomen de tabel met het veld niet beschikbaar zijn voor het instellen van het wijzigingslogboek. Zie voor meer informatie [Vertrouwelijke velden bewaken](across-log-changes.md#monitoring-sensitive-fields).

Nadat u het wijzigingslogbestand hebt ingesteld, hebt geactiveerd en gegevens hebt gewijzigd, kunt u de wijzigingen weergeven en filteren op de pagina **Wijzigingslogposten** . Als u posten wilt verwijderen, kunt u dat doen op de pagina **Wijzigingslogposten verwijderen** , waar u filters kunt instellen op basis van datums en tijd.  

## <a name="about-activity-logs"></a>Over activiteitenlogboeken
Vanaf enkele pagina's in [!INCLUDE [prodshort](includes/prodshort.md)] kunt u een activiteitenlogboek bekijken dat de status en eventuele fouten weergeeft van bestanden waarnaar u exporteert vanuit of importeert in [!INCLUDE [prodshort](includes/prodshort.md)].  

### <a name="working-with-activity-logs"></a>Werken met activiteitenlogboeken
De informatie wordt weergegeven op de pagina **Activiteitenlogboek** , volgens de context van waaruit deze wordt geopend. U kunt de pagina bijvoorbeeld openen vanuit de pagina's **Documentuitwisselingsservice instellen** , **Inkomend document** , **Geboekte verkoopfactuur** en **Geboekte verkoopcreditnota** . U kunt de lijst met logboekvermeldingen leegmaken of gewoon de lijst met vermeldingen ouder dan zeven dagen wissen.  

## <a name="monitoring-sensitive-fields"></a>Vertrouwelijke velden controleren
Het veilig en privé houden van gevoelige gegevens is voor de meeste bedrijven een belangrijk aandachtspunt. Om een beveiligingslaag toe te voegen kunt u belangrijke velden controleren en per e-mail een melding ontvangen wanneer iemand een waarde wijzigt. U wilt bijvoorbeeld een melding ontvangen als iemand het IBAN-nummer van uw bedrijf wijzigt.

> [!NOTE]
> Voor het verzenden van meldingen per e-mail moet u de e-mailfunctie instellen in [!INCLUDE[prodshort](includes/prodshort.md)]. Zie [E-mail instellen](admin-how-setup-email.md) voor meer informatie.

### <a name="setting-up-field-monitoring"></a>Veldcontrole instellen
U kunt de begeleide instelling **Instelling van controle van veldwijziging** gebruiken om de velden te specificeren die u wilt bewaken op basis van filtercriteria, zoals de gegevensgevoeligheidsclassificatie voor de velden. Zie voor meer informatie [Vertrouwelijkheid van gegevens classificeren](admin-classifying-data-sensitivity.md). In de handleiding kunt u ook de persoon specificeren die een e-mailmelding ontvangt wanneer er een wijziging plaatsvindt, en het e-mailaccount dat de e-mailmelding zal verzenden. U moet zowel de gebruikersmelding opgeven als het account van waaruit de melding moet worden verzonden. Nadat u de begeleide instelling hebt voltooid, kunt u instellingen voor veldbewaking beheren op de pagina **Instelling van veldcontrole** . 

Na verloop van tijd zal de lijst met vermeldingen op de pagina **Logboekvermeldingen van gecontroleerde velden** groeien. Om het aantal vermeldingen te verminderen kunt u een bewaarbeleid maken dat vermeldingen na een bepaalde tijd verwijdert. Zie voor meer informatie [Bewaarbeleid definiëren](admin-data-retention-policies.md).

Als u veldbewaking instelt of iets in de instellingen wijzigt, worden er vermeldingen gemaakt voor uw wijzigingen. U kunt aangeven of vermeldingen met betrekking tot de bewakingsinstellingen moeten worden weergegeven of verborgen. 

U kunt instellingen voor veldbewaking beheren, zoals of u een e-mailmelding wilt verzenden of alleen de wijziging wilt vastleggen, voor elk veld op de pagina **Werkblad Velden controleren** . De pagina is ook waar u velden kunt toevoegen of verwijderen om te controleren.

> [!NOTE]
> Nadat u een of meer velden hebt toegevoegd en de controle hebt gestart, moet u zich afmelden bij [!INCLUDE[prodshort](includes/prodshort.md)] en u opnieuw aanmelden om uw instellingen toe te passen.

### <a name="working-with-field-monitoring"></a>Werken met veldcontrole
Invoer voor alle gewijzigde waarden voor bewaakte velden is beschikbaar op de pagina **Logboekvermeldingen van gecontroleerde velden** . Vermeldingen bevatten bijvoorbeeld informatie zoals het veld waarvoor de waarde is gewijzigd, de oorspronkelijke en de nieuwe waarde en wie de wijziging heeft aangebracht en wanneer. Om een wijziging verder te onderzoeken kiest u een waarde om de pagina te openen waarop deze is aangebracht. Kies om een lijst met alle vermeldingen weer te geven **Veldwijzigingsposten** .

## <a name="defining-retention-policies"></a>Bewaarbeleid definiëren
U kunt bewaarbeleid maken om onnodige gegevens in logboeken te verwijderen na een door u opgegeven periode. Zo kan het aantal vermeldingen in een logboek na verloop van tijd toenemen. Door oude vermeldingen op te schonen kunt u het gemakkelijker maken om u te concentreren op recentere en waarschijnlijk relevantere vermeldingen. Zie voor meer informatie [Bewaarbeleid definiëren](admin-data-retention-policies.md).

## <a name="see-also"></a>Zie ook
[Basisinstellingen wijzigen](ui-change-basic-settings.md)  
[Sorteren, zoeken en filteren](ui-enter-criteria-filters.md)  
[Pagina's en informatie zoeken met Vertel me](ui-search.md)  
[Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md)    
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Bewaarbeleid definiëren](admin-data-retention-policies.md)  