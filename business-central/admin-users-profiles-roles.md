---
title: Gebruikers en rollen beheren | Microsoft Docs
description: Leren hoe u gebruikers en rolcentra beheert in Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: profiles, users
ms.date: 10/01/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 1a94d023424c6eceb93af6e9ca89a90a3a94e996
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="understanding-users-profiles-and-role-centers"></a>Gebruikers, profielen en rolcentra

In [!INCLUDE[d365fin](includes/d365fin_md.md)] worden gebruikers toegevoegd door een beheerder die gebruikers tevens toegang geeft tot de gebieden van [!INCLUDE[d365fin](includes/d365fin_md.md)] die ze voor hun werk nodig hebben.  

Toegang tot functionaliteit wordt beheerd door middel van *gebruikersgroepen* en *profielen*. Als beheerder kunt u profielen toevoegen en verwijderen als onderdeel van uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-abonnement en kunt u gebruikersmachtigingen toewijzen met behulp van gebruikersgroepen.  

## <a name="adding-users"></a>Gebruikers toevoegen

Als u gebruikers wilt toevoegen in [!INCLUDE[d365fin](includes/d365fin_md.md)] online, moet de Office 365-beheerder van uw bedrijf eerst de gebruikers in het Office 365-beheercentrum maken. Zie voor meer informatie [Gebruikers aan Office 365 toevoegen voor bedrijven](https://aka.ms/CreateOffice365Users).

Vervolgens kan de beheerder machtigingen toewijzen aan elke gebruiker en groep gebruikers. Zie [Gebruikers en machtigingen beheren](ui-how-users-permissions.md) voor meer informatie.  

### <a name="users-of-on-premises-deployments"></a>Gebruikers van on-premises implementaties

Voor on-premises implementaties van [!INCLUDE[d365fin](includes/d365fin_md.md)] kan de beheerder kiezen tussen verschillende autorisatiemechanismen voor referenties voor gebruikers. Wanneer u dan een gebruiker maakt, geeft u verschillende informatie op, afhankelijk van het referentietype dat u in de specifieke [!INCLUDE[server](includes/server.md)]-instantie gebruikt. Zie voor meer informatie [Verificatie en referentietypen](/dynamics365/business-central/dev-itpro/administration/users-credential-types) in het gedeelte Beheer van de ontwikkelaars- en ITPro-inhoud voor [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="profiles"></a>Profielen

Aan alle personen in het bedrijf die toegang tot [!INCLUDE[d365fin](includes/d365fin_md.md)] hebben, wordt een *profiel* toegewezen dat ze toegang biedt tot een *rolcentrum*.

Profielen zijn verzamelingen [!INCLUDE[d365fin](includes/d365fin_md.md)]-gebruikers die hetzelfde rolcentrum delen. Een rolcentrum is het invoerpunt en de homepage voor [!INCLUDE[d365fin](includes/d365fin_md.md)], waarmee u snel toegang krijgt tot de belangrijkste taken en verschillende inzichten en KPI's over uw werk kunt weergeven.  

> [!NOTE]  
>  In de huidige versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] online kunt u geen profielen toevoegen, bewerken of verwijderen.  

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

