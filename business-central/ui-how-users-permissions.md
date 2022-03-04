---
title: Gebruikers maken volgens licenties
description: Beschrijft hoe u gebruikers aan Business Central Online of on-premises kunt toevoegen op basis van licenties.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.search.form: 119, 6300, 6301, 6302, 9800, 9807, 9808, 9830, 9831, 9838, 9818, 9062, 9173
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: f39067f990c80fad751d251ab4dd7ff038ac0cb2
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8148264"
---
# <a name="create-users-according-to-licenses"></a>Gebruikers maken volgens licenties

Dit artikel beschrijft hoe beheerders gebruikers maken en definiëren wie zich kunnen aanmelden bij [!INCLUDE[prod_short](includes/prod_short.md)] en welke machtigingen worden gegeven aan verschillende gebruikerstypen volgens de licenties.

Wanneer u gebruikers maakt in [!INCLUDE[prod_short](includes/prod_short.md)], kunt u hen specifieke machtigingen toewijzen via machtigingensets en gebruikers in gebruikersgroepen indelen. Gebruikersgroepen maken het gemakkelijker om toestemmingen voor meerdere gebruikers tegelijkertijd te beheren. Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie.  

Voor meer informatie over de verschillende soorten licenties en hoe licenties werken in [!INCLUDE[prod_short](includes/prod_short.md)] [downloadt u de Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> Het proces van het beheren van gebruikers en licenties is afhankelijk van of [!INCLUDE[prod_short](includes/prod_short.md)] online of on-premises wordt geïmplementeerd. Voor [!INCLUDE [prod_short](includes/prod_short.md)] online moet u gebruikers toevoegen vanuit Microsoft 365. In on-premises implementaties kunt u rechtstreeks gebruikers maken, bewerken en verwijderen.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Gebruikers en licenties beheren in online implementaties

In de online versie van [!INCLUDE[prod_short](includes/prod_short.md)] wordt het aantal gebruikers bepaald door het abonnement en worden gebruikers aan uw tenant toegevoegd in het Microsoft Partner Center, meestal door uw Microsoft-partner. Zie voor meer informatie [Een nieuwe klant toevoegen](/partner-center/add-a-new-customer) en [Klantabonnementen maken, opschorten of annuleren](/partner-center/create-a-new-subscription) in de Help van het Microsoft Partner Center.

Om te bepalen wie zich kan aanmelden bij [!INCLUDE[prod_short](includes/prod_short.md)], moet u productlicenties toewijzen aan gebruikers op basis van de rollen die zij zullen vervullen in [!INCLUDE[prod_short](includes/prod_short.md)]. Dit kan op de volgende manieren worden gedaan:

- De Microsoft 365-beheerder van uw bedrijf kan dit doen in het [Microsoft 365-beheercentrum](https://admin.microsoft.com). Zie voor meer informatie [Gebruikers afzonderlijk of in bulk toevoegen aan Microsoft 365](/microsoft-365/admin/add-users/add-users).  
- Een Microsoft-partner kan licenties toewijzen in het Microsoft 365-beheercentrum of in het Microsoft Partner Center. Zie voor meer informatie [Gebruikersbeheertaken voor klantaccounts](/partner-center/assign-licenses-to-users) in de Microsoft Partner Center Help.

Zie voor meer informatie [Beheer van Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) in de Help voor beheerders.

### <a name="to-add-users-or-update-user-information-and-license-assignments-in-business-central"></a><a name="adduser"></a>Gebruikers toevoegen of gebruikersgegevens en licentietoewijzingen bijwerken in Business Central
Nadat u gebruikers heeft toegevoegd of gebruikersinformatie heeft gewijzigd in het Microsoft 365-beheercentrum, kunt u de gebruikersinformatie snel importeren naar [!INCLUDE[prod_short](includes/prod_short.md)]. Dit omvat licentietoewijzingen. 

1. Meld u met een beheerdersaccount aan bij [!INCLUDE[prod_short](includes/prod_short.md)].
2. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Gebruikers** in en kies vervolgens de gerelateerde koppeling  
3. Kies **Gebruikers bijwerken vanuit Microsoft 365**.

Als u nieuwe gebruikers toevoegt, is de volgende stap het toewijzen van gebruikersgroepen en machtigingen. Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie. Als u gebruikersinformatie bijwerkt en de update een licentiewijziging omvat, worden de gebruikers toegewezen aan de juiste gebruikersgroep en worden hun machtigingensets bijgewerkt. Zie [Machtigingen beheren via gebruikersgroepen](ui-define-granular-permissions.md) voor meer informatie.  

> [!NOTE]
> Alle gebruikers moeten dezelfde licentie krijgen, Essential of Premium. Zie de Microsoft Dynamics 365 Business Central Licentiehandleiding voor meer informatie. De gids kan worden gedownload op de [Business Central](https://dynamics.microsoft.com/business-central/overview/)-website.

Voor meer informatie over het synchroniseren van gebruikersinformatie met Microsoft 365 raadpleegt u de sectie [Synchronisatie met Microsoft 365](#m365).

> [!NOTE]
> Als u een externe auditor gebruikt om uw boeken en financiële rapportage te beheren, kunt u deze uitnodigen voor uw Business Central, zodat hij of zij met u kan werken aan uw fiscale gegevens. Zie voor meer informatie [Uw externe accountant uitnodigen voor uw Business Central](finance-accounting.md#inviteaccountant).

### <a name="to-remove-a-users-access-to-the-system"></a>De toegang van een gebruiker tot het systeem verwijderen

Bij online implementaties kunt u de toegang van een gebruiker tot [!INCLUDE[prod_short](includes/prod_short.md)] verwijderen. Alle verwijzingen naar de gebruiker worden bewaard, maar de gebruiker kan niet inloggen en actieve sessies voor de gebruiker worden gestopt.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Gebruikers** in en kies vervolgens de gerelateerde koppeling
2. Open de pagina **Gebruikerskaart** voor de relevante gebruiker en selecteer in het veld **Status** de optie **Uitgeschakeld**.
3. Als u de gebruiker weer toegang wilt geven, stelt u het veld **Status** in op **Ingeschakeld**.

U kunt de licentie ook verwijderen van een gebruiker in het Microsoft 365-beheercentrum. De gebruiker kan zich dan niet meer aanmelden. Zie voor meer informatie [Licenties van gebruikers verwijderen](/microsoft-365/admin/manage/remove-licenses-from-users).

### <a name="synchronization-with-microsoft-365"></a><a name="m365"></a>Synchronisatie met Microsoft 365

Wanneer u een licentie voor [!INCLUDE[prod_short](includes/prod_short.md)] toewijst aan een gebruiker in Microsoft 365, zijn er twee manieren om de gebruiker te maken in [!INCLUDE[prod_short](includes/prod_short.md)].  

- De beheerder kan de gebruiker toevoegen door de actie **Gebruikers bijwerken vanuit Microsoft 365** te kiezen op de pagina **Gebruikers** zoals beschreven in de sectie [Een gebruiker toevoegen of gebruikersgegevens bijwerken in Business Central](#adduser).
- De licentie-informatie wordt automatisch bijgewerkt wanneer de gebruiker zich voor de eerste keer aanmeldt.

In beide gevallen wordt automatisch een aantal instellingen gemaakt. Deze worden vermeld in de tweede en derde kolom in de onderstaande tabel.

Als u gebruikersgegevens wijzigt in Microsoft 365, kunt u [!INCLUDE[prod_short](includes/prod_short.md)] bijwerken om de verandering te weerspiegelen. Gebruik een van de acties op de pagina **Gebruikers**, afhankelijk van wat u wilt bijwerken. Deze acties worden beschreven in de laatste drie kolommen in de onderstaande tabel.

> [!NOTE]
> De acties die in de volgende tabel worden beschreven, zijn correct, maar de enige die u nodig heeft, is **Gebruikers bijwerken vanuit Microsoft 365**, die is toegevoegd om het proces te vereenvoudigen. De andere acties worden verwijderd in een toekomstige versie van [!INCLUDE[prod_short](includes/prod_short.md)].

|Wat gebeurt er wanneer:|Eerste gebruiker, eerste aanmelding|Gebruikers ophalen uit Microsoft 365|Gebruikers bijwerken vanuit Microsoft 365|Standaardgebruikersgroepen van gebruiker herstellen|Gebruikersgroepen vernieuwen|Gebruikersgegevens bijwerken vanuit Microsoft 365|
|-|-|-|-|-|-|-|
|Bereik:|Huidige gebruiker|Nieuwe gebruikers in Microsoft 365|Meerdere geselecteerde gebruikers|Eén geselecteerde gebruiker (behalve huidige)|Meerdere geselecteerde gebruikers|Meerdere geselecteerde gebruikers|
|Maak de nieuwe gebruiker en wijs SUPER-machtigingenset toe.<br /><br /><!--Platform-->|**X**||**X** | | | |
|Werk de gebruiker bij op basis van informatie in Microsoft 365: Status, Volledige naam, Contact-e-mail, E-mailadres voor verificatie.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|**X**||**X**|
|Synchroniseer gebruikersplannen (licenties) met toegewezen licenties en rollen in Microsoft 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**|**X**|**X**|**X**| |
|Voeg de gebruiker toe aan gebruikersgroepen volgens de huidige gebruikersplannen. Verwijder de SUPER-machtigingenset voor alle gebruikers behalve de eerste gebruiker die zich aanmeldt en [beheerders](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Er is ten minste één SUPER nodig.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**|**X**|**X**<br /><br />Verwijdert handmatig toegewezen gebruikersgroepen en machtigingen.|**X**<br /><br />Werk gebruikersgroepstoewijzingen bij.| |

<!--
## The Device License
This section has been moved to [Licensing in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing).
-->

## <a name="managing-users-and-licenses-in-on-premises-deployments"></a>Gebruikers en licenties beheren in On-premises implementaties

Voor on-premises implementaties wordt het aantal gebruikerslicenties opgegeven in het licentiebestand (.flf). Wanneer een beheerder of Microsoft-partner het licentiebestand uploadt, kan de beheerder opgeven welke gebruikers zich kunnen aanmelden bij [!INCLUDE[prod_short](includes/prod_short.md)].

Voor on-premises implementaties maakt de beheerder gebruikers rechtstreeks op de pagina **Gebruikers**.

### <a name="to-edit-or-delete-a-user-in-an-on-premises-deployment"></a>Een gebruiker in een on-premises implementatie bewerken of verwijderen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikers** in en kies vervolgens de gerelateerde koppeling
2. Selecteer de gebruiker die u wilt bewerken en kies vervolgens de actie **Bewerken**.
3. Wijzig indien nodig op de pagina **Gebruikerskaart** de informatie.  
4. Als u een gebruiker wilt verwijderen, selecteert u die gebruiker en kiest u de actie **Verwijderen**.

> [!NOTE]
> Voor on-premises implementaties kan een beheerder specificeren hoe gebruikersreferenties in het [!INCLUDE[server](includes/server.md)]-exemplaar worden geverifieerd. Wanneer u een gebruiker maakt, geeft u het type referentie op dat u gebruikt.
>
> Zie voor meer informatie [Verificatie en referentietypen](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in de beheer-Help voor [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="see-also"></a>Zie ook

[Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md)  
[Profielen beheren](admin-users-profiles-roles.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)  
[Aanpassen [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Beheer](admin-setup-and-administration.md)  
[Licenties in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing)  
[Gebruikers aan Microsoft 365 toevoegen voor bedrijven](/microsoft-365/admin/add-users/add-users)  
[Beveiliging en bescherming in Business Central (beheerinhoud)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  


[!INCLUDE[footer-include](includes/footer-banner.md)]