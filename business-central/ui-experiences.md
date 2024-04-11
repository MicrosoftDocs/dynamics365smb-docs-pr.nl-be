---
title: Wijzigen welke functies worden weergegeven
description: 'Meer weten over wat de ervaringslagen Essential en Premium betekenen voor de gebruikersinterface, toepassingsgebieden en uw bedrijf.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: ivkoleti
ms.topic: conceptual
ms.search.keywords: 'essential, basic, user interface, application area, experience'
ms.search.form: '1,'
ms.date: 03/11/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Wijzigen welke functies worden weergegeven

[!INCLUDE[prod_short](includes/prod_short.md)] is ontworpen om u te helpen uw bedrijf te runnen, ongeacht de grootte en complexiteit. In de kern van het product vindt u essentiële functies, zoals financiële rapportage, verkoop-, inkoop- en voorraadbeheer. Naarmate de bedrijfscomplexiteit toeneemt, kunt u bijvoorbeeld functionaliteit inschakelen voor productie en servicebeheer.

U kunt het complexiteitsniveau van het product definiëren, en daarmee tot welke functies de gebruikers van het bedrijf toegang krijgen. Daartoe stelt u de instelling **Ervaring** in op de pagina **Bedrijfsgegevens**. De ingestelde ervaring kan ook worden gewijzigd door bepaalde extensies uit AppSource toe te voegen. Zie voor meer informatie [[!INCLUDE[prod_short](includes/prod_short.md)] aanpassen met extensies](ui-extensions.md).

In de volgende tabel worden de ervaringen beschreven die momenteel beschikbaar zijn.

| Ervaring | Effect op gebruikersinterface |
| --- | --- |
| **Essential** |Hier worden alle acties en velden voor alle gemeenschappelijke bedrijfsfuncties weergegeven.|
| **Premium** |Hier worden alle acties en velden voor alle bedrijfsfuncties weergegeven, inclusief Productie en Servicebeheer.|

De ervaringen die in [!INCLUDE[prod_short](includes/prod_short.md)] kunnen worden geselecteerd, weerspiegelen de oplossingslicenties, gebruikte plannen, die zijn gedefinieerd voor het product. Informatie over de plannen Essential en Premium vindt u op [Business Central](https://go.microsoft.com/fwlink/?linkid=2264940) de site van Microsoft Dynamics 365 Marketing. Zie ook de [[!INCLUDE[prod_short](includes/prod_short.md)] Licentiehandleiding](https://go.microsoft.com/fwlink/?linkid=2264939).

> [!IMPORTANT]  
> Aan gebruikers van het type Teamlid, Interne admin, Externe accountant en Gedelegeerde admin kunnen aan een ander plan zijn toegewezen dan andere gebruikers in de oplossing. Alleen gebruikers van het type Evaluation of Premium kunnen de waarde in het veld **Ervaring** wijzigen van Essential in Premium.

> [!NOTE]
> In releasewave 1 van 2024 kan een gebruiker met het Premium-abonnement inloggen bij een bedrijf dat het Essentials-abonnement gebruikt. De Premium-gebruiker kan echter geen gebruik maken van de functies die de Premium-licentie biedt. Hetzelfde geldt niet andersom. Gebruikers met het Essentials-abonnement kunnen niet inloggen bij een bedrijf dat het Premium-abonnement gebruikt.

Voordat u de ervaring van een bedrijf instelt, definieert u de toegang van gebruikers tot specifieke functies en pagina's door machtigingensets toe te wijzen. Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie.

De instelling **Ervaring** is van toepassing op alle gebruikers in een bedrijf, maar elke gebruiker kan zijn eigen ervaring verder personaliseren door paginalay-outs en inhoud te wijzigen. Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.

## Premium-functies inschakelen na een upgrade van het abonnement

Gebruikers worden aan plannen toegewezen in het Microsoft 365-beheercentrum, in verband met het algemene werk om de Business Central-gebruikers te maken. Zie voor meer informatie [Tegelijkertijd gebruikers toevoegen en licenties toewijzen](/microsoft-365/admin/add-users/add-users?view=o365-worldwide&preserve-view=true).

### Planwijzigingen bijwerken in gebruikersgroepen

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Wanneer u een wijziging in gebruikersplannen hebt aangebracht in het Microsoft 365-beheercentrum , zoals meer gebruikers toewijzen aan het Premium-plan, moet u [!INCLUDE[prod_short](includes/prod_short.md)] bijwerken om de verandering te weerspiegelen.

1. Meld u aan als beheerder.
2. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikers** in en kies vervolgens de gerelateerde koppeling.
3. Kies op de pagina **Gebruikers** de actie **Gebruikers van Microsoft 365** bijwerken.

### De Premium-ervaring selecteren

U kunt nu doorgaan met de nieuwe ervaring te selecteren.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Bedrijfsgegevens** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer op de pagina **Bedrijfsgegevens** op het sneltabblad **Gebruikerservaring** de optie Premium in het veld **Ervaring**.

## In de Help wordt uitgegaan van de Premium-ervaring

Alle functiebeschrijvingen in de gebruikersdocumentatie voor [!INCLUDE[prod_short](includes/prod_short.md)] gaan uit van de **Premium**-ervaring, wat inhoudt dat de beschrijvingen het hele scala aan UI-elementen omvatten.

## Zie ook

[Uw werkruimte personaliseren](ui-personalization-user.md)  
[Business Central aanpassen](ui-customizing-overview.md)  
[Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md)  
[Nieuwe bedrijven maken](about-new-company.md)  
[Basisinstellingen wijzigen](ui-change-basic-settings.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]