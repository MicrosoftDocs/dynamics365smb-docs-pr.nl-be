---
title: Gebruikersmachtigingen toewijzen of bewerken | Microsoft Docs
description: Hier wordt beschreven hoe u Office 365-gebruikers toevoegt aan Business Central en vervolgens machtigingen, toegangsrechten en beveiligingsinstellingen toewijst.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 11/07/2019
ms.author: sgroespe
ms.openlocfilehash: c64a14ed66668f8c3cbe09e8db3430a7dc25db5c
ms.sourcegitcommit: 2a6d629cf290645606356b714a77ef2872bdec64
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 11/07/2019
ms.locfileid: "2774831"
---
# <a name="create-users-according-to-licenses"></a>Gebruikers maken volgens licenties
Hieronder wordt beschreven hoe u als beheerder gebruikers maakt en definieert die zich kunnen aanmelden bij [!INCLUDE[d365fin](includes/d365fin_md.md)] en welke fundamentele rechten verschillende gebruikerstypen hebben volgens de licenties.

Wanneer gebruikers worden gemaakt in [!INCLUDE[d365fin](includes/d365fin_md.md)], kunt u doorgaan met het toewijzen van specifieke machtigingen aan gebruikers via machtigingensets en het organiseren van gebruikers in gebruikersgroepen voor eenvoudig machtigingsbeheer. Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie.  

> [!NOTE]
> Het proces van het beheren van gebruikers en licenties is afhankelijk van of uw oplossing online of on-premises wordt geïmplementeerd. In online implementaties bijvoorbeeld kunt u een gebruiker alleen uitschakelen en inschakelen nadat deze is toegevoegd aan [!INCLUDE[d365fin](includes/d365fin_md.md)]. In on-premises implementaties kunt u gebruikers maken, bewerken en verwijderen.  

## <a name="managing-users-and-licenses-in-online-deployments"></a>Gebruikers en licenties beheren in online implementaties
In [!INCLUDE[d365fin](includes/d365fin_md.md)] online wordt het aantal gebruikers bepaald door het abonnement en worden gebruikers aan uw tenant toegevoegd in het Microsoft Partner Center, meestal door uw Microsoft-partner. Zie voor meer informatie [Een nieuwe klant toevoegen](https://docs.microsoft.com/partner-center/add-a-new-customer) en [Klantabonnementen maken, opschorten of annuleren](https://docs.microsoft.com/partner-center/create-a-new-subscription) in de Help van het Microsoft Partner Center.

Om te bepalen wie zich kan aanmelden bij [!INCLUDE[d365fin](includes/d365fin_md.md)], moeten de productlicenties worden toegewezen aan gebruikers op basis van de rollen die zij zullen vervullen in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dit kan op de volgende manieren worden gedaan:
- De Office 365-beheerder van uw bedrijf kan dit doen in het [Microsoft 365-beheercentrum](https://admin.microsoft.com). Zie voor meer informatie [Gebruikers afzonderlijk of in bulk toevoegen aan Office 365](https://aka.ms/CreateOffice365Users).  
- Een Microsoft-partner kan licenties toewijzen in het Microsoft 365-beheercentrum of in het Microsoft Partner Center. Zie voor meer informatie [Gebruikersbeheertaken voor klantaccounts](https://docs.microsoft.com/partner-center/assign-licenses-to-users) in de Help van Microsoft Partner Center.

Zie voor meer informatie [Beheer van Business Central Online](/dynamics365/business-central/dev-itpro/administration/tenant-administration) in de Help voor ontwikkelaars en IT-pro's.

Als gebruikers met een [!INCLUDE[d365fin](includes/d365fin_md.md)]-licentie in Office 365 zijn gemaakt, kunnen ze op de pagina **Gebruikers** in [!INCLUDE[d365fin](includes/d365fin_md.md)] worden geïmporteerd door middel van de actie **Gebruikers ophalen uit Office 365**.

### <a name="to-add-a-user-in-business-central"></a>Een gebruiker in Business Central toevoegen
Om gebruikers vanuit van het Microsoft 365-beheercentrum toe te voegen aan [!INCLUDE[d365fin](includes/d365fin_md.md)] Online gebruikt u een speciale importfunctie.  
1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikers** in en kies de desbetreffende koppeling.
2. Kies de actie **Gebruikers ophalen uit Office 365**.

Elke nieuwe gebruiker die wordt gemaakt voor uw Office 365-abonnement, wordt op de pagina **Gebruikers** toegevoegd. Aan gebruikers worden machtigingensets toegewezen op basis van de licentie die aan de gebruiker is toegewezen in Office 365. U kunt vervolgens gedetailleerdere machtigingen aan gebruikers toewijzen en gebruikers voor eenvoudig machtigingsbeheer organiseren in gebruikersgroepen. Zie [Machtigingensets toewijzen aan gebruikers](ui-define-granular-permissions.md#to-assign-permission-sets-to-users) voor meer informatie.

### <a name="to-remove-a-users-access-to-the-system"></a>De toegang van een gebruiker tot het systeem verwijderen
In online implementaties kunt u de toegang van een gebruiker tot het systeem verwijderen door het veld **Status** in te stellen op **Uitgeschakeld**. Alle verwijzingen naar de gebruiker blijven behouden, maar de gebruiker kan zich niet meer aanmelden bij het systeem en actieve sessies voor de gebruiker worden beëindigd.

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikers** in en kies de desbetreffende koppeling.
2. Open de pagina **Gebruikerskaart** voor de relevante gebruiker en selecteer in het veld **Status** de optie **Uitgeschakeld**.
3. Als u de gebruiker weer toegang wilt geven, stelt u het veld **Staat** in op **Ingeschakeld**.

Naast het uitschakelen van een gebruiker kunt u ook de toewijzing van een licentie aan een gebruiker opheffen in het Office 365-beheercentrum. De gebruiker kan zich dan niet meer aanmelden. Zie voor meer informatie [Licenties van gebruikers verwijderen](https://docs.microsoft.com/office365/admin/manage/remove-licenses-from-users).

### <a name="to-change-the-assigned-license-for-a-user"></a>De toegewezen licentie voor een gebruiker wijzigen
Soms moet u de licentie wijzigen die aan een gebruiker is toegewezen. Als u bijvoorbeeld besluit de module Servicebeheer te gebruiken en daarom alle Essential-licenties moet upgraden naar Premium. Of als de verantwoordelijkheid van een gebruiker is gewijzigd en u een Teamlid-licentie moet vervangen door Essential.

1. Wijzig de licentie in het Office 365-beheercentrum. Zie voor meer informatie [Gebruikers afzonderlijk of in bulk toevoegen aan Office 365](https://aka.ms/CreateOffice365Users).
2. Meld u als beheerder aan bij [!INCLUDE[d365fin](includes/d365fin_md.md)].
3. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikers** in en kies de desbetreffende koppeling.
4. U kunt ook op de pagina **Gebruikers** de actie **Alle gebruikersgroepen vernieuwen** kiezen.
De gebruikers worden verplaatst naar een geschikte gebruikersgroep en de machtigingensets worden bijgewerkt. Zie [Machtigingen beheren via gebruikersgroepen](ui-define-granular-permissions.md#to-manage-permissions-through-user-groups) voor meer informatie.

> [!NOTE]
> Alle reguliere gebruikers in een oplossing moeten dezelfde licentie krijgen, Essential of Premium.
> Zie voor informatie over licenties [Microsoft Dynamics 365 Business Central Licentiehandleiding](https://aka.ms/BusinessCentralLicensing).

## <a name="managing-users-and-licenses-in-online-deployments"></a>Gebruikers en licenties beheren in online implementaties
Voor on-premises implementaties wordt een aantal gelicentieerde gebruikers opgegeven in het licentiebestand (.flf). Wanneer de beheerder of Microsoft-partner het licentiebestand uploadt, kan de beheerder opgeven welke gebruikers zich kunnen aanmelden bij [!INCLUDE[d365fin](includes/d365fin_md.md)].

Voor on-premises implementaties maakt de beheerder gebruikers rechtstreeks op de pagina **Gebruikers**.

### <a name="to-edit-or-delete-a-user-on-premises"></a>Een gebruiker on-premises bewerken of verwijderen
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikers** in en kies de gerelateerde koppeling.
2. Selecteer de gebruiker die u wilt bewerken en kies vervolgens de actie **Bewerken**.
3. Wijzig indien nodig op de pagina **Gebruikerskaart** de informatie.    
4. Als u een gebruiker wilt verwijderen, selecteert u die gebruiker en kiest u de actie **Verwijderen**.

> [!NOTE]
> Voor on-premises implementaties van [!INCLUDE[d365fin](includes/d365fin_md.md)] kan de beheerder kiezen tussen verschillende autorisatiemechanismen voor referenties voor gebruikers. Wanneer u dan een gebruiker maakt, geeft u verschillende informatie op, afhankelijk van het referentietype dat u in de specifieke [!INCLUDE[server](includes/server.md)]-instantie gebruikt.<br /><br />
> Zie voor meer informatie [Verificatie en referentietypen](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in het gedeelte Beheer van de ontwikkelaars- en ITPro-inhoud voor [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="see-also"></a>Zie ook
[Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md)  
[Profielen beheren](admin-users-profiles-roles.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)  
[Aanpassen [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Beheer](admin-setup-and-administration.md)  
[Gebruikers aan Office 365 toevoegen voor bedrijven](https://aka.ms/CreateOffice365Users)  
[Microsoft Dynamics 365 Business Central Licentiehandleiding](https://aka.ms/BusinessCentralLicensing)  
[Beveiliging en bescherming in Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) in de Help voor ontwikkelaars en IT-professionals
