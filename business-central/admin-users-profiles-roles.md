---
title: Gebruikers en rollen beheren | Microsoft Docs
description: Leren hoe u gebruikers en rolcentra beheert in Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: fc52d943938616041881c55f70c510e4c63b5de6
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245821"
---
# <a name="understanding-users-profiles-and-role-centers"></a>Gebruikers, profielen en rolcentra

In [!INCLUDE[d365fin](includes/d365fin_md.md)] worden gebruikers toegevoegd door een beheerder die gebruikers tevens toegang geeft tot de gebieden van [!INCLUDE[d365fin](includes/d365fin_md.md)] die ze voor hun werk nodig hebben.  

Toegang tot functionaliteit wordt beheerd door middel van *gebruikersgroepen* en *profielen*. Als beheerder kunt u profielen toevoegen en verwijderen als onderdeel van uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-abonnement en kunt u gebruikersmachtigingen toewijzen met behulp van gebruikersgroepen.  

## <a name="adding-users"></a>Gebruikers toevoegen

Als u gebruikers wilt toevoegen in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, moet de Office 365-beheerder van uw bedrijf eerst de gebruikers in het Office 365-beheercentrum maken. Zie voor meer informatie [Gebruikers aan Office 365 toevoegen voor bedrijven](https://aka.ms/CreateOffice365Users).

Vervolgens kan de beheerder machtigingen toewijzen aan elke gebruiker en groep gebruikers. Zie [Gebruikers en machtigingen beheren](ui-how-users-permissions.md) voor meer informatie.  

De krachtigste machtigingen die een gebruiker kan hebben, is de machtigingenset SUPER. Elk bedrijf moet minimaal één gebruiker met deze machtigingenset hebben, maar het is een best practice om elke gebruiker machtigingen te geven die overeenkomen met hun werkbehoeften in [!INCLUDE[prodshort](includes/prodshort.md)] en niet meer dan dat. Dit helpt zorgen dat gebruikers bijvoorbeeld alleen toegang hebben tot gegevens die relevant zijn voor hun werk.  

> [!TIP]
> Het is een best practice om ervoor te zorgen dat de Office 365-beheerder ook de machtigingenset SUPER heeft in [!INCLUDE[prodshort](includes/prodshort.md)] omdat dat veel beheertaken eenvoudiger maakt, inclusief het instellen van integratie met andere apps.

### <a name="users-of-on-premises-deployments"></a>Gebruikers van on-premises implementaties

Voor on-premises implementaties van [!INCLUDE[d365fin](includes/d365fin_md.md)] kan de beheerder kiezen tussen verschillende autorisatiemechanismen voor referenties voor gebruikers. Wanneer u dan een gebruiker maakt, geeft u verschillende informatie op, afhankelijk van het referentietype dat u in de specifieke [!INCLUDE[server](includes/server.md)]-instantie gebruikt. Zie voor meer informatie [Verificatie en referentietypen](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in het gedeelte Beheer van de ontwikkelaars- en ITPro-inhoud voor [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="profiles"></a>Profielen

Aan alle personen in het bedrijf die toegang tot [!INCLUDE[d365fin](includes/d365fin_md.md)] hebben, wordt een *profiel* toegewezen dat ze toegang biedt tot een *rolcentrum*.

Profielen zijn verzamelingen [!INCLUDE[d365fin](includes/d365fin_md.md)]-gebruikers die hetzelfde rolcentrum delen. Een rolcentrum is het invoerpunt en de homepage voor [!INCLUDE[d365fin](includes/d365fin_md.md)], waarmee u snel toegang krijgt tot de belangrijkste taken en verschillende inzichten en KPI's over uw werk kunt weergeven.  

> [!NOTE]  
>  In de huidige versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] online kunt u geen profielen toevoegen, bewerken of verwijderen.  

### <a name="CreateProfile"></a>Een profiel maken

1.  Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Profieloverzicht** in en klik vervolgens op de gerelateerde koppeling.  

2.  Kies op de pagina **Profieloverzicht** de actie **Nieuw** om de pagina **Nieuwe profielkaart** te openen.  

3.  Voer in het veld **Profiel-id** een naam in die de beoogde rol van de gebruikers beschrijft.  

4.  Voer in het veld **Beschrijving** een beschrijving in van de profiel-id in, bijvoorbeeld **Orderverwerker**.  

5.  Stel het veld **Rolcentrum-id** in op het rolcentrum dat u aan het profiel wilt toewijzen.  

De procedure voor het wijzigen van een bestaand profiel is hetzelfde, behalve dat u een bestaand profiel selecteert op de pagina **Profieloverzicht** in plaats van de actie **Nieuw** te kiezen.  


### <a name="copy-a-profile"></a>Een profiel kopiëren
Een profiel kopiëren kan u tijd besparen als u dezelfde instellingen voor een profiel wilt gebruiken en u slechts enkele instellingen wilt wijzigen.

1.  Open het profiel dat u wilt kopiëren en kies vervolgens de actie **Profiel kopiëren**.

2.  Voer in het veld **Nieuwe profiel-id** een naam in voor het profiel dat u wilt kopiëren.

3.  Stel het veld **Nieuw profielbereik** op een van de volgende waarden in:

    - **Systeem** om het profiel voor de nieuwe tenantdatabases beschikbaar te maken die de toepassing gebruikt.
    - **Tenant** om het nieuwe profiel alleen voor de huidige tenantdatabase beschikbaar te maken.
4. Kies de knop **OK** als u gereed bent.

### <a name="ExportImportProfile"></a>Profielen exporteren en importeren

U kunt profielen als XML-bestanden van en naar een [!INCLUDE[d365fin](includes/d365fin_md.md)] database exporteren en importeren. Het exporteren en importeren van een profiel kan u tijd besparen als u de gebruikersinterface configureert, omdat u een bestaande profielconfiguratie opnieuw gebruikt in plaats van dat een profiel helemaal vanaf het begin moet worden geconfigureerd. Als u een profiel hebt dat in een [!INCLUDE[d365fin](includes/d365fin_md.md)] database is geconfigureerd en u alle of een aantal van dezelfde profielconfiguraties in een andere database opnieuw wilt gebruiken, kunt u het profiel naar een XML-bestand exporteren. Vervolgens kunt u het XML-profielbestand in een andere database importeren.

-   Als u een profiel wilt exporteren, kunt u de actie **Profielen exporteren** in het **Profieloverzicht** of de pagina **Profielkaart** kiezen of u kunt zoeken naar de pagina **Profielen exporteren** en deze openen. Sla het XML-bestand op op een locatie op uw computer of netwerk.

-   Als u een profiel wilt importeren, kunt u de actie **Profiel importeren** op de pagina **Profieloverzicht** kiezen of kunt u de pagina **Profielen importeren** kiezen. 

    > [!NOTE]  
    >  U kunt geen profiel importeren dat al bestaat in de database, zelfs als het XML-bestand anders is genoemd of andere inhoud heeft. U moet het bestaande profiel verwijderen voordat u het nieuwe profiel kunt importeren.


## <a name="configuration-and-personalization"></a>Configuratie en personalisatie
<!--The concept of UI customization in [!INCLUDE[d365fin](includes/d365fin_md.md)] is divided in two:  

-   Configuration, performed by the administrator  

-   Personalization, performed by users  

The administrator configures the user interface for multiple users by customizing the user interface for a profile that the users are assigned to.  -->

Gebruikers passen de gebruikersinterface van hun persoonlijke versie aan door de gebruikersinterface onder hun eigen gebruikersaanmelding te wijzigen. Deze personalisatie kan worden verwijderd door de beheerder. Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.  

## <a name="see-also"></a>Zie ook  
[Gebruikers en machtigingen beheren](ui-how-users-permissions.md)  
[Personalisaties beheren als beheerder](ui-personalization-manage.md)  
[Het personaliseren van uw werkruimte](ui-personalization-user.md)  
