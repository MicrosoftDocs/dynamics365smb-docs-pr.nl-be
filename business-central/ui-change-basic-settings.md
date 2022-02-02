---
title: Basisinstellingen wijzigen voor de huidige gebruiker
description: Leer hoe u enkele basisinstellingen in Business Central kunt wijzigen, bijvoorbeeld uw rol en rolcentrum, bedrijf, werkdatum en tijdzones.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: change Role Center, notification, change company, change work date, decimal separator
ms.search.form: 9022, 9019, 9027
ms.date: 10/01/2021
ms.author: jswymer
ms.openlocfilehash: 38301359b6f13b809b2f980fdf5dc3b4a678451d
ms.sourcegitcommit: 66c78f6f04bfca6c0794b3299241ed65037b1c08
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/26/2022
ms.locfileid: "8029048"
---
# <a name="change-basic-settings"></a>Basisinstellingen wijzigen

Op de pagina **Mijn instellingen** kunt u basisinstellingen bekijken en wijzigen voor uw [!INCLUDE[prod_short](includes/prod_short.md)]. De wijzigingen die u aanbrengt, hebben alleen invloed op uw werkruimte, niet op de werkruimten van andere gebruikers.  

## <a name="role"></a><a name="role-center"></a>Rol

Het rolcentrum vertegenwoordigt de startpagina, een startscherm dat is ontworpen voor de vereisten van een specifieke rol in een organisatie. Afhankelijk van uw rol krijgt u op de startpagina of in het Rolcentrum een overzicht van het bedrijf, uw afdeling of uw persoonlijke taken. Het helpt u ook navigeren naar uw dagelijkse taken en werk te zoeken dat aan u is toegewezen.

* Bovenaan kunt u met de navigatie schakelen tussen klanten, leveranciers, artikelen en andere belangrijke lijsten met informatie. Op dezelfde manier kunt u met acties taken starten, zoals een nieuwe verkoopfactuur maken, direct vanaf de startpagina.

* In het midden ziet u het gebied **Activiteiten**, dat actuele gegevens toont en waarop kan worden geklikt of getikt om meer gedetailleerde informatie te bekijken. KPI´s (Key Performance Indicators) kunnen worden ingesteld om een geselecteerd diagram weer te geven voor een visuele weergave van bijvoorbeeld cashflow of inkomsten en uitgaven. U kunt ook een lijst met favoriete klanten maken op de startpagina voor bedrijfsaccounts waarmee u vaak zaken doet of waaraan u speciale aandacht moet geven.

### <a name="to-change-the-role"></a>De rol wijzigen

De standaardrol is **Bedrijfsmanager**, maar u kunt een andere rol selecteren om een rolcentrum te selecteren dat beter aan uw behoeften voldoet.  

1. Kies in de rechterbovenhoek het pictogram **Instellingen** ![Instellingen.](media/ui-experience/settings_icon_small.png "Pictogram Instellingen voor rolcentrum") en kies vervolgens de actie **Mijn instellingen**.
2. Selecteer op de pagina **Instellingen** in het veld **Rol** de rol die u als standaard wilt gebruiken. Selecteer bijvoorbeeld **Accountant**.
3. Kies de knop **Ok**.

## <a name="company"></a><a name="company"></a>Bedrijf

Een bedrijf werkt als een container voor gegevens in [!INCLUDE[prod_short](includes/prod_short.md)]. Een database kan meerdere bedrijven bevatten, maar er kan slechts één bedrijf tegelijk worden geselecteerd.

Het standaardbedrijf heet CRONUS en bevat alleen demogegevens. U kunt een nieuw bedrijf met aangepaste gegevens maken. Zie [Nieuwe bedrijven](about-new-company.md) maken voor meer informatie.

### <a name="to-change-the-company-name"></a>De bedrijfsnaam wijzigen

De bedrijfsnaam wordt altijd in de linkerbovenhoek weergegeven en werkt als een actie die u kunt kiezen om terug te gaan naar het rolcentrum. U kunt deze naam wijzigen op de pagina **Bedrijfsgegevens**.

1. Kies het ![pictogram Tand om het menu Instellingen te openen.](media/ui-experience/settings_icon_small.png) en kies vervolgens de actie **Bedrijfsgegevens**.
2. Voer in het veld **Naam** de nieuwe bedrijfsnaam in.
3. Verlaat de pagina. Het systeem start opnieuw op en geeft het nieuwe bedrijf in de linkerbovenhoek weer.

### <a name="to-display-a-company-badge-for-quick-access-to-company-information"></a><a name="badge"></a>Een bedrijfsbadge weergeven voor snelle toegang tot bedrijfsgegevens

U kunt een aangepaste badge in de rechterbovenhoek toevoegen, die u kunt kiezen om de bedrijfsnaam en tenantinformatie snel in een pop-upvenster te bekijken. De bedrijfsbadge is ook handig wanneer [!INCLUDE[prod_short](includes/prod_short.md)] is ingebed in een andere toepassing, zoals Microsoft Teams of in een andere webtoepassing. In deze gevallen, omdat de [!INCLUDE[web_client](includes/web_client.md)] minder omgevingscontextuele informatie weergeeft, dient de bedrijfsbadge als de enige manier om te bepalen tot welk bedrijf of welke omgeving een record behoort.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Bedrijfsgegevens** in en kies vervolgens de gerelateerde koppeling.
2. Vul op het sneltabblad **Bedrijfsbadge** indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

> [!NOTE]
> Als een bedrijfsbadge is gedefinieerd, kunt u de bedrijfsnaam niet wijzigen zoals beschreven in [De bedrijfsnaam wijzigen](ui-change-basic-settings.md#to-change-the-company-name)

## <a name="work-date"></a><a name="work-date"></a>Werkdatum
De meest gebruikte werkdatum is de datum van vandaag. U moet de werkdatum mogelijk tijdelijk wijzigen om taken te kunnen uitvoeren, zoals het voltooien van transacties voor een datum die niet de datum van vandaag is.

> [!TIP]  
> Typ in alle datumvelden **v** om snel de datum van vandaag in te voeren en typ **w** om snel de werkdatum in te voeren. Dit is de waarde in het veld **Werkdatum** op de pagina **Mijn instellingen**.

> [!IMPORTANT]  
> Nadat u de werkdatum wijzigt, als u zich afmeldt of naar een ander bedrijf gaat, krijgen de werkgegevens weer de standaardwerkdatum. Als u zich de volgende keer aanmeldt of teruggaat naar het originele bedrijf, moet u de werkdatum mogelijk weer instellen.

### <a name="work-date-indication"></a>Indicatie van werkdatum

De werkdatum is van cruciaal belang voor pagina's die kunnen worden bewerkt. Wanneer de werkdatum niet is ingesteld op de datum van vandaag op een bewerkbare pagina, verschijnen er twee soorten indicatoren op de pagina:

* Boven aan de pagina wordt een herinnering weergegeven die aangeeft waar de werkdatum op is ingesteld. De herinnering biedt een directe koppeling naar de instelling van de werkdatum op de pagina **Mijn instellingen**, zodat u de datum kunt wijzigen als u dat wilt. Vanuit de herinnering kunt u er ook voor kiezen om de herinnering voor de rest van uw sessie te negeren. Tenzij u de werkdatum wijzigt in 'vandaag', verschijnt de herinnering de volgende keer dat u zich aanmeldt.

* Als u de herinnering negeert, wordt de werkdatum weergegeven in de titel van de pagina.  

Als de werkdatum niet is ingesteld op de huidige dag (vandaag) wordt op alle pagina's waar u gegevens kunt bewerken, de huidige werkdatum weergegeven in de rechterbovenhoek.

## <a name="region"></a><a name="region"></a> Regio

De instelling bij **Regio** bepaalt de weergave of notatie van datums, tijden, nummers en valuta's. Het bepaalt ook welk teken wordt gebruikt als decimaalteken bij het gebruik van een numeriek toetsenbord om gegevens in te voeren. Zie voor meer informatie [Gegevens invoeren](ui-enter-data.md#decimal).

## <a name="language"></a><a name="language"></a> Taal

Wijzigt de weergavetaal. Dit veld wordt alleen weergegeven als uit meerdere talen kan worden gekozen.

De aanvankelijke taal wordt bepaald door de beheerder of door uw browserinstellingen als u zich aanmeldt voor [!INCLUDE[prod_short](includes/prod_short.md)]. De taal die u instelt, wordt op alle apparaten gebruikt waarop u zich aanmeldt, zoals een telefoon of tablet.

Extra talen voor [!INCLUDE[prod_short](includes/prod_short.md)] kunnen worden geïnstalleerd vanuit AppSource. Hoewel alle ondersteunde weergavetalen in de lijst worden weergegeven, moet de beheerder de relevante taal-app op de tenant installeren voordat gebruikers kunnen overschakelen naar de nieuwe taal in [!INCLUDE[prod_short](includes/prod_short.md)].  

## <a name="time-zone"></a>Tijdzone

Bepaalt de tijdzone waarin u zich bevindt. Wanneer u zich voor het eerst aanmeldt bij [!INCLUDE [prod_short](includes/prod_short.md)], wordt de tijdzone ingesteld op basis van het adres van uw bedrijf. Verander het als het niet overeenkomt met uw fysieke locatie.  

## <a name="notifications"></a>Berichten

Kies de koppeling *Wijzigen wanneer ik berichten ontvang* om de meldingen te zien of aan te passen die u ontvangt over bepaalde gebeurtenissen of statuswijzigingen, bijvoorbeeld wanneer u een klant wilt gaan factureren die een openstaand saldo heeft of wanneer de beschikbare voorraad lager is dan de hoeveelheid die u op het punt staat te verkopen. Zie voor meer informatie [Berichten beheren](ui-smart-notifications.md).

## <a name="teaching-tips"></a>Instructietips

[!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)]

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/personalize-ui-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Nieuwe bedrijven maken](about-new-company.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
