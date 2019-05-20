---
title: De gebruikerservaring kiezen om geavanceerde functies weer te geven of te verbergen | Microsoft Docs
description: Meer weten over wat de ervaringslagen Essential en Premium betekenen voor de gebruikersinterface, toepassingsgebieden en uw bedrijf.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: essential, basic, user interface, application area, experience
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 9110ee79e4d1788f41c8f1960f282cb490a3cc8a
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1251435"
---
# <a name="changing-which-features-are-displayed"></a>Wijzigen welke functies worden weergegeven
[!INCLUDE[d365fin](includes/d365fin_md.md)] is ontworpen om u te helpen uw bedrijf te runnen, ongeacht in welke branche u actief bent. In de kern van [!INCLUDE[d365fin](includes/d365fin_md.md)] vindt u financiële rapportage en verkoop- en inkoopprocessen. U voegt daar ervaringen aan toe op basis van uw zakelijke behoeften dor extensies toe te voegen uit AppSource of door de instelling Ervaring te wijzigen voor uw bedrijf. Zie voor meer informatie [[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met extensies](ui-extensions.md) of [Een gebruikerservaring kiezen om functies weer te geven of te verbergen](ui-experiences.md#choosing-a-user-experience-to-show-or-hide-features) hieronder.

## <a name="choosing-a-user-experience-to-show-or-hide-features"></a>Een gebruikerservaring kiezen om functies weer te geven of te verbergen
De gebruikerservaring bepaalt hoeveel van de kernfunctionaliteit beschikbaar is wanneer u en uw collega's met [!INCLUDE[d365fin](includes/d365fin_md.md)] werken. In het veld **Ervaring** op de pagina **Bedrijfsgegevens** kunt u de gebruikerservaring instellen voor uw bedrijf.

> [!NOTE]  
> Deze instelling is van toepassing op alle gebruikers in uw bedrijf. Gebruikers kunnen hun eigen ervaring nog verder aanpassen door pagina-indelingen en inhoud te wijzigen. Zie [Uw werkruimte en pagina's personaliseren](ui-personalization-user.md) voor meer informatie.  

In de volgende tabel worden de ervaringen beschreven die momenteel beschikbaar zijn.

| Ervaring | Effect op gebruikersinterface |
| --- | --- |
| **Essential** |Hier worden alle acties en velden voor alle gemeenschappelijke bedrijfsfuncties weergegeven.|
| **Premium** |Hier worden alle acties en velden voor alle bedrijfsfuncties weergegeven, inclusief Productie en Servicebeheer.|

> [!NOTE]  
> Welke ervaringen u kunt selecteren in [!INCLUDE[d365fin](includes/d365fin_md.md)], is afhankelijk van uw oplossingslicentie, een abonnement genaamd. Voor informatie over de abonnementen **Essentieel** en **Premium** raadpleegt u [Business Central](https://go.microsoft.com/fwlink/?linkid=870242) op de marketingsite van Microsoft Dynamics 365. Zie ook de [[!INCLUDE[d365fin](includes/d365fin_md.md)] Licentiehandleiding](https://go.microsoft.com/fwlink/?linkid=2068931) (vereist toegang tot CustomerSource of PartnerSource).

> [!IMPORTANT]  
> Alle normale gebruikers in een oplossing moeten aan hetzelfde plan worden toegewezen, Essential of Premium, voordat die ervaring kan worden geselecteerd voor het bedrijf. Een gebruiker kan daarom geen Premium-functies gebruiken als een of meer andere gebruikers alleen toegang hebben tot Essential-functies. Dit geldt niet voor niet-normale gebruikers van het type Teamlid, Interne admin, Externe accountant en Gedelegeerde admin, die allemaal aan een ander plan kunnen zijn toegewezen dan andere gebruikers in de oplossing.

## <a name="enabling-premium-features-after-upgrading-a-plan"></a>Premium-functies inschakelen na een upgrade van het plan
Gebruikers worden aan plannen toegewezen in Office 365, in verband met het algemene werk om de Business Central-gebruikers te maken. Zie voor meer informatie [Gebruikers aan Office 365 toevoegen voor bedrijven](https://support.office.com/en-us/article/Add-users-to-Office-365-for-business-435ccec3-09dd-4587-9ebd-2f3cad6bc2bc).

Vervolgens kunt u definiëren tot welke specifieke functies en pagina's binnen de ervaring die gebruikers toegang hebben, door machtigingensets toe te wijzen. Zie [Gebruikers en machtigingen beheren](ui-how-users-permissions.md) voor meer informatie.

### <a name="to-update-plan-changes-in-users-groups"></a>Planwijzigingen bijwerken in gebruikersgroepen
Wanneer u een wijziging in gebruikersplannen hebt aangebracht in het Office 365-beheercentrum , zoals meer gebruikers toewijzen aan het Premium-plan, moet u de wijziging doorvoeren in [!INCLUDE[d365fin](includes/d365fin_md.md)].

1. Meld u aan als beheerder.
2. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikers** in en kies vervolgens de gerelateerde koppeling.
3. U kunt ook op de pagina **Gebruikers** de actie **Alle gebruikersgroepen vernieuwen** kiezen.

Alle nieuwe informatie over de plannen van gebruikers en hun toegewezen gebruikersgroepen worden nu bijgewerkt volgens de planwijzigingen.

### <a name="to-select-the-premium-experience"></a>De Premium-ervaring selecteren
U kunt nu doorgaan met de nieuwe ervaring te selecteren.
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bedrijfsgegevens** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer op de pagina **Bedrijfsgegevens** op het sneltabblad **Gebruikerservaring** de optie Premium in het veld **Ervaring**.

## <a name="help-assumes-premium-experience"></a>In de Help wordt uitgegaan van de Premium-ervaring
Alle functiebeschrijvingen in de gebruikersdocumentatie voor [!INCLUDE[d365fin](includes/d365fin_md.md)] gaan uit van de **Premium-** ervaring, wat inhoudt dat de beschrijvingen het hele scala aan UI-elementen omvatten. Er wordt een tekstnotitie in Help-onderwerpen op hoog niveau ingevoegd voor de functiegebieden Productie en Servicebeheer die aangeeft dat deze de **Premium**-ervaring vereisen.

## <a name="see-also"></a>Zie ook
[Nieuwe bedrijven maken](about-new-company.md)  
[Gebruikers en machtigingen beheren](ui-how-users-permissions.md)    
[Basisinstellingen wijzigen](ui-change-basic-settings.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies](ui-extensions.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] Licentiehandleiding](https://go.microsoft.com/fwlink/?LinkId=871590&clcid=0x409)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
