---
title: Gebruikers maken op basis van licenties | Microsoft Docs
description: Beschrijft hoe u gebruikers aan Business Central Online of on-premises kunt toevoegen op basis van licenties.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 217b658e6a4c54996d3f0e9cfa7470f02908b380
ms.sourcegitcommit: 5d5451ee618f122c926e3189290f3765052f7077
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/11/2021
ms.locfileid: "4846352"
---
# <a name="create-users-according-to-licenses"></a>Gebruikers maken volgens licenties

Dit artikel beschrijft hoe beheerders gebruikers maken en definiëren wie zich kunnen aanmelden bij [!INCLUDE[prod_short](includes/prod_short.md)] en welke machtigingen worden gegeven aan verschillende gebruikerstypen volgens de licenties.

Wanneer u gebruikers maakt in [!INCLUDE[prod_short](includes/prod_short.md)], kunt u hen specifieke machtigingen toewijzen via machtigingensets en gebruikers in gebruikersgroepen indelen. Gebruikersgroepen maken het gemakkelijker om toestemmingen voor meerdere gebruikers tegelijkertijd te beheren. Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie. 

Voor meer informatie over de verschillende soorten licenties en hoe licenties werken in [!INCLUDE[prod_short](includes/prod_short.md)] raadpleegt u de Dynamics 365 Licensing Guide, die u kunt downloaden van [https://go.microsoft.com/fwlink/?LinkId=866544](https://go.microsoft.com/fwlink/?LinkId=866544).

> [!NOTE]
> Het proces van het beheren van gebruikers en licenties is afhankelijk van of [!INCLUDE[prod_short](includes/prod_short.md)] online of on-premises wordt geïmplementeerd. Voor [!INCLUDE [prod_short](includes/prod_short.md)] online moet u gebruikers toevoegen vanuit Microsoft 365. In on-premises implementaties kunt u rechtstreeks gebruikers maken, bewerken en verwijderen.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Gebruikers en licenties beheren in online implementaties

In de online versie van [!INCLUDE[prod_short](includes/prod_short.md)] wordt het aantal gebruikers bepaald door het abonnement en worden gebruikers aan uw tenant toegevoegd in het Microsoft Partner Center, meestal door uw Microsoft-partner. Zie voor meer informatie [Een nieuwe klant toevoegen](/partner-center/add-a-new-customer) en [Klantabonnementen maken, opschorten of annuleren](/partner-center/create-a-new-subscription) in de Help van het Microsoft Partner Center.

Om te bepalen wie zich kan aanmelden bij [!INCLUDE[prod_short](includes/prod_short.md)], moet u productlicenties toewijzen aan gebruikers op basis van de rollen die zij zullen vervullen in [!INCLUDE[prod_short](includes/prod_short.md)]. Dit kan op de volgende manieren worden gedaan:

- De Microsoft 365-beheerder van uw bedrijf kan dit doen in het [Microsoft 365-beheercentrum](https://admin.microsoft.com). Zie voor meer informatie [Gebruikers afzonderlijk of in bulk toevoegen aan Microsoft 365](https://aka.ms/CreateOffice365Users).  
- Een Microsoft-partner kan licenties toewijzen in het Microsoft 365-beheercentrum of in het Microsoft Partner Center. Zie voor meer informatie [Gebruikersbeheertaken voor klantaccounts](/partner-center/assign-licenses-to-users) in de Microsoft Partner Center Help.

Zie voor meer informatie [Beheer van Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) in de Help voor beheerders.

### <a name="to-add-users-or-update-user-information-and-license-assignments-in-business-central"></a><a name="adduser"></a>Gebruikers toevoegen of gebruikersgegevens en licentietoewijzingen bijwerken in Business Central
Nadat u gebruikers heeft toegevoegd of gebruikersinformatie heeft gewijzigd in het Microsoft 365-beheercentrum, kunt u de gebruikersinformatie snel importeren naar [!INCLUDE[prod_short](includes/prod_short.md)]. Dit omvat licentietoewijzingen. 

1. Meld u met een beheerdersaccount aan bij [!INCLUDE[prod_short](includes/prod_short.md)].
2. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikers** in en kies de desbetreffende koppeling.  
3. Kies **Gebruikers bijwerken vanuit Office 365**.

Als u nieuwe gebruikers toevoegt, is de volgende stap het toewijzen van gebruikersgroepen en machtigingen. Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie. Als u gebruikersinformatie bijwerkt en de update een licentiewijziging omvat, worden de gebruikers toegewezen aan de juiste gebruikersgroep en worden hun machtigingensets bijgewerkt. Zie [Machtigingen beheren via gebruikersgroepen](ui-define-granular-permissions.md) voor meer informatie.  

> [!NOTE]
> Alle gebruikers moeten dezelfde licentie krijgen, Essential of Premium. Zie de Microsoft Dynamics 365 Business Central Licentiehandleiding voor meer informatie. De gids kan worden gedownload op de [Business Central](https://dynamics.microsoft.com/business-central/overview/)-website.

Voor meer informatie over het synchroniseren van gebruikersinformatie met Microsoft 365 raadpleegt u de sectie [Synchronisatie met Microsoft 365](#m365).

> [!NOTE]
> Als u een externe auditor gebruikt om uw boeken en financiële rapportage te beheren, kunt u deze uitnodigen voor uw Business Central, zodat hij of zij met u kan werken aan uw fiscale gegevens. Zie voor meer informatie [Uw externe accountant uitnodigen voor uw Business Central](finance-accounting.md#inviteaccountant).

### <a name="to-remove-a-users-access-to-the-system"></a>De toegang van een gebruiker tot het systeem verwijderen

Bij online implementaties kunt u de toegang van een gebruiker tot [!INCLUDE[prod_short](includes/prod_short.md)] verwijderen. Alle verwijzingen naar de gebruiker worden bewaard, maar de gebruiker kan niet inloggen en actieve sessies voor de gebruiker worden gestopt.

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikers** in en kies de desbetreffende koppeling.
2. Open de pagina **Gebruikerskaart** voor de relevante gebruiker en selecteer in het veld **Status** de optie **Uitgeschakeld**.
3. Als u de gebruiker weer toegang wilt geven, stelt u het veld **Staat** in op **Ingeschakeld**.

U kunt de licentie ook verwijderen van een gebruiker in het Microsoft 365-beheercentrum. De gebruiker kan zich dan niet meer aanmelden. Zie voor meer informatie [Licenties van gebruikers verwijderen](https://docs.microsoft.com/office365/admin/manage/remove-licenses-from-users).

### <a name="synchronization-with-microsoft-365"></a><a name="m365"></a>Synchronisatie met Microsoft 365

Wanneer u een licentie voor [!INCLUDE[prod_short](includes/prod_short.md)] toewijst aan een gebruiker in Microsoft 365, zijn er twee manieren om de gebruiker te maken in [!INCLUDE[prod_short](includes/prod_short.md)].  

- De beheerder kan de gebruiker toevoegen door de actie **Gebruikers bijwerken vanuit Office 365** te kiezen op de pagina **Gebruikers** zoals beschreven in de sectie [Een gebruiker toevoegen of gebruikersgegevens bijwerken in Business Central](#adduser).
- De licentie-informatie wordt automatisch bijgewerkt wanneer de gebruiker zich voor de eerste keer aanmeldt.

In beide gevallen wordt automatisch een aantal instellingen gemaakt. Deze worden vermeld in de tweede en derde kolom in de onderstaande tabel.

Als u gebruikersgegevens wijzigt in Microsoft 365, kunt u [!INCLUDE[prod_short](includes/prod_short.md)] bijwerken om de verandering te weerspiegelen. Gebruik een van de acties op de pagina **Gebruikers**, afhankelijk van wat u wilt bijwerken. Deze acties worden beschreven in de laatste drie kolommen in de onderstaande tabel.

> [!NOTE]
> De acties die in de volgende tabel worden beschreven, zijn nauwkeurig, maar de enige die u nodig heeft, is **Gebruikers bijwerken vanuit Office 365**, die is toegevoegd om het proces te vereenvoudigen. De andere acties worden verwijderd in een toekomstige versie van [!INCLUDE[prod_short](includes/prod_short.md)].

|Wat gebeurt er wanneer:|Eerste gebruiker, eerste aanmelding|Gebruikers ophalen uit Microsoft 365|Gebruikers bijwerken vanuit Microsoft 365|Standaardgebruikersgroepen van gebruiker herstellen|Gebruikersgroepen vernieuwen|Gebruikersgegevens bijwerken vanuit Microsoft 365|
|-|-|-|-|-|-|-|
|Bereik:|Huidige gebruiker|Nieuwe gebruikers in Microsoft 365|Meerdere geselecteerde gebruikers|Eén geselecteerde gebruiker (behalve huidige)|Meerdere geselecteerde gebruikers|Meerdere geselecteerde gebruikers|
|Maak de nieuwe gebruiker en wijs SUPER-machtigingenset toe.<br /><br /><!--Platform-->|**X**||**X** | | | |
|Werk de gebruiker bij op basis van informatie in Microsoft 365: Staat, Volledige naam, Contact-e-mail, E-mailadres voor verificatie.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserFromAzureGraph-->|**X**|**X**|**X**|**X**||**X**|
|Synchroniseer gebruikersplannen (licenties) met toegewezen licenties en rollen in Microsoft 365.<!--<br /><br />Codeunit "Azure AD   Graph User".UpdateUserPlans-->|**X**|**X**|**X**|**X**|**X**| |
|Voeg de gebruiker toe aan gebruikersgroepen volgens de huidige gebruikersplannen. Verwijder de SUPER-machtigingenset voor alle gebruikers behalve de eerste gebruiker die zich aanmeldt en [beheerders](/dynamics365/business-central/dev-itpro/administration/tenant-administration). Er is ten minste één SUPER nodig.<!--<br /><br />Codeunit "Permission Manager". AddUserToDefaultUserGroups-->|**X**|**X**|**X**|**X**<br /><br />Verwijdert handmatig toegewezen gebruikersgroepen en machtigingen.|**X**<br /><br />Werk gebruikersgroepstoewijzingen bij.| |

## <a name="the-device-license"></a>De apparaatlicentie

Met de Dynamics 365 Business Central-apparaatlicentie kunnen meerdere gebruikers tegelijkertijd een apparaat gebruiken dat onder de licentie valt. Dit kan bijvoorbeeld een verkooppunt, winkelvloer of magazijnapparaat zijn. Wanneer u een aantal apparaatlicenties hebt gekocht, kan maximaal dat aantal gebruikers dat is toegewezen aan de groep Dynamics 365 Business Central-apparaatgebruikers, zich gelijktijdig aanmelden. Zie de Microsoft Dynamics 365 Business Central Licentiehandleiding voor meer informatie. De gids kan worden gedownload op de [Business Central](https://dynamics.microsoft.com/business-central/overview/)-website.

De Microsoft 365-beheerder van uw bedrijf of Microsoft-partner kan de groep Dynamics 365 Business Central-apparaatgebruikers maken en apparaatgebruikers toevoegen als leden in het [Microsoft 365-beheercentrum](https://admin.microsoft.com/) of in de [Azure-portal](https://portal.azure.com/).

### <a name="device-user-limitations"></a>Beperkingen apparaatgebruiker

Gebruikers met de apparaatlicentie kunnen de volgende taken niet uitvoeren in [!INCLUDE[prod_short](includes/prod_short.md)]:

- Taken instellen om te worden uitgevoerd als geplande taken in de taakwachtrij. Apparaatgebruikers zijn gelijktijdige gebruikers en daarom kunnen we niet garanderen dat de betrokken gebruiker in het systeem aanwezig is wanneer een taak wordt uitgevoerd, wat vereist is.

- Een apparaatgebruiker kan zich niet als eerste gebruiker aanmelden. Een gebruiker van het type Beheerder, Volledige gebruiker of Externe accountant moet zich als eerste aanmelden om [!INCLUDE[prod_short](includes/prod_short.md)] te kunnen instellen. Zie voor meer informatie [Beheer van Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) in de Help voor beheerders.

### <a name="to-create-a-dynamics-365-business-central-device-users-group"></a>Een Dynamics 365 Business Central-apparaatgebruikersgroep maken

1. Ga in het Microsoft 365-beheercentrum naar de pagina **Groepen**.
2. Kies de actie **Een groep toevoegen**.
3. Kies op de pagina **Een groepstype kiezen** de actie **Beveiliging** en daarna de actie **Toevoegen**.
4. Voer op de pagina **Grondbeginselen** **Dynamics 365 Business Central-apparaatgebruikers** als de naam van de groep in.
  
   >[!NOTE]
   >De naam van de groep moet precies in het Engels worden gespeld zoals weergegeven in stap 4, zelfs als u een andere taal gebruikt.
5. Kies de knop **Sluiten**.

> [!NOTE]
> U kunt ook een groep maken van het type Microsoft 365. Zie [Groepen vergelijken](https://docs.microsoft.com/office365/admin/create-groups/compare-groups) voor meer informatie

### <a name="to-add-members-to-the-group"></a>Leden toevoegen aan de groep

1. Vernieuw in het Microsoft 365-beheercentrum de pagina **Groepen**, zodat uw nieuwe groep wordt weergegeven.
2. Selecteer de groep **Dynamics 365 Business Central-apparaatgebruikers** en kies de actie **Alles weergeven en leden beheren**.
3. Kies de actie **Leden toevoegen**.
4. Selecteer de gebruikers die u wilt toevoegen en kies de knop **Opslaan**.
5. Kies driemaal de knop **Sluiten**.

U kunt zoveel gebruikers aan de groep Dynamics 365 Business Central-apparaatgebruikers toevoegen als u nodig hebt. Het aantal apparaten waarop gebruikers zich tegelijkertijd kunnen aanmelden, wordt echter bepaald door het aantal aangeschafte apparaatlicenties.

> [!NOTE]
> U hoeft geen [!INCLUDE[prod_short](includes/prod_short.md)]-licentie aan gebruikers toe te wijzen die lid zijn van de Dynamics 365 Business Central-apparaatgebruikersgroep.

## <a name="managing-users-and-licenses-in-on-premises-deployments"></a>Gebruikers en licenties beheren in On-premises implementaties

Voor on-premises implementaties wordt het aantal gebruikerslicenties opgegeven in het licentiebestand (.flf). Wanneer een beheerder of Microsoft-partner het licentiebestand uploadt, kan de beheerder opgeven welke gebruikers zich kunnen aanmelden bij [!INCLUDE[prod_short](includes/prod_short.md)].

Voor on-premises implementaties maakt de beheerder gebruikers rechtstreeks op de pagina **Gebruikers**.

### <a name="to-edit-or-delete-a-user-in-an-on-premises-deployment"></a>Een gebruiker in een on-premises implementatie bewerken of verwijderen

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikers** in en kies de gerelateerde koppeling.
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
[Gebruikers toevoegen aan Microsoft 365 voor bedrijven](https://aka.ms/CreateOffice365Users)  
[Beveiliging en bescherming in Business Central (beheerinhoud)](/dynamics365/business-central/dev-itpro/security/security-and-protection)  


[!INCLUDE[footer-include](includes/footer-banner.md)]