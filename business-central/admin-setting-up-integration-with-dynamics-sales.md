---
title: Gebruikersaccounts instellen voor integratie met Dynamics 365 for Sales | Microsoft Docs
description: Leer hoe u gebruikersaccounts instelt die de apps gebruiken om gegevens uit te wisselen, en die personen gebruiken om toegang te krijgen tot gegevens in de apps en deze te synchroniseren.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 3163389cb0818133fba9ab8c55b8d0cf662130f1
ms.sourcegitcommit: 04581558f6c5488c705a7ac392cf297be10b5f4f
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/06/2019
ms.locfileid: "1620965"
---
# <a name="setting-up-user-accounts-for-integrating-with-dynamics-365-for-sales"></a>Gebruikersaccounts instellen voor integratie met Dynamics 365 for Sales
Dit artikel geeft een overzicht van hoe u de gebruikersaccounts instelt die vereist zijn om [!INCLUDE[crm_md](includes/crm_md.md)] te integreren met [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085500]

## <a name="setting-up-the-admininstrator-user-account-in-sales"></a>Het beheerdersaccount instellen in Sales
U moet het beheerdersaccount voor [!INCLUDE[d365fin](includes/d365fin_md.md)] toevoegen als een gebruiker in [!INCLUDE[crm_md](includes/crm_md.md)] en vervolgens de gebruiker promoveren tot beheerder in [!INCLUDE[crm_md](includes/crm_md.md)]. Het beheerdersaccount moet ook de rol van systeemaanpasser hebben en ten minste één andere niet-beheerdersrol, zoals Verkoopmanager in [!INCLUDE[crm_md](includes/crm_md.md)].

## <a name="setting-up-the-user-account-for-the-integration"></a>Het gebruikersaccount instellen voor de integratie
U moet een speciaal gebruikersaccount in uw Office 365-abonnement maken dat zowel [!INCLUDE[d365fin](includes/d365fin_md.md)] als [!INCLUDE[crm_md](includes/crm_md.md)] kan gebruiken om gegevens te synchroniseren. Dit gebruikersaccount moet zich kunnen aanmelden bij [!INCLUDE[crm_md](includes/crm_md.md)], wat betekent dat deze gebruiker een licentie moet hebben voor [!INCLUDE[crm_md](includes/crm_md.md)] en dat ten minste één beveiligingsrol in [!INCLUDE[crm_md](includes/crm_md.md)] aan het account moet zijn toegewezen, zoals [hier](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-user-account) beschreven. Zie voor meer informatie over hoe u gebruikers maakt in [!INCLUDE[crm_md](includes/crm_md.md)] [Beveiliging, gebruikers en teams beheren](http://go.microsoft.com/fwlink/?LinkID=616518). Nadat de verbinding is ingesteld, wijst [!INCLUDE[d365fin](includes/d365fin_md.md)] aan het gebruikersaccount de beveiligingsrollen toe die nodig zijn in [!INCLUDE[d365fin](includes/d365fin_md.md)] en kan dit account worden ingesteld op de [niet-interactieve toegangsmodus](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account) in [!INCLUDE[crm_md](includes/crm_md.md)]

![Begeleide instelling toont waar gebruikersreferenties voor synchronisatie moeten worden ingevoerd](media/sync-user-setup.png "Door visualisatie ondersteunde instellingswizardpagina toont de plaats waar gebruikersreferenties voor synchronisatie moeten worden ingevoerd")

> [!IMPORTANT]  
> Gebruik het beheerdersaccount niet voor [!INCLUDE[crm_md](includes/crm_md.md)] voor synchronisatie. Als u dat doet wordt de synchronisatie verstoord.
> Om constante synchronisatie te voorkomen worden wijzigingen in gegevens die worden aangebracht door het integratiegebruikersaccount niet gesynchroniseerd. <!--What changes would this account make?--> Als de verbinding is gemaakt, is het raadzaam de toegangsmodus voor het gebruikersaccount voor integratie in te stellen op de niet-interactieve modus in [!INCLUDE[crm_md](includes/crm_md.md)]. Zie voor meer informatie [Een niet-interactief gebruikersaccount maken](https://docs.microsoft.com/en-us/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles#create-a-non-interactive-user-account).

## <a name="setting-up-accounts-for-sales-people"></a>Accounts instellen voor verkopers
U moet gebruikersaccounts maken in [!INCLUDE[crm_md](includes/crm_md.md)] voor de verkoper uit [!INCLUDE[d365fin](includes/d365fin_md.md)]. Om het gemakkelijker te maken biedt het Microsoft 365-beheercentrum een Excel-sjabloon die u kunt gebruiken. Kies op de pagina **Actieve gebruikers** **Meer** en vervolgens **Meerdere gebruikers importeren**. Kies **Een CSV-bestand downloaden met alleen koppen** en voer vervolgens de informatie voor de verkoper in. Als u een voorbeeld wilt zien, kiest u **Een CSV-bestand downloaden met koppen en voorbeeldgegevens van gebruikers**. Nadat u de gegevens hebt ingevoerd over de gebruikers, is de volgende stap bij het importproces de gebruikerslicenties toe te wijzen aan het Dynamics 365 Customer Engagement-plan.  

Nadat u gebruikers hebt geïmporteerd en aan hen licenties hebt toegewezen voor Dynamics 365 Customer Engagement, moet u de gebruikers aan de rol **Verkoper** toewijzen in [!INCLUDE[crm_md](includes/crm_md.md)].

![Verkopers koppelen aan gebruikers in Dynamics 365 for Sales](media/couple-salespeople.png "Visualisatie van koppeling van verkopers aan gebruikers in Dynamics 365 for Sales")

## <a name="see-also"></a>Zie ook  
[Integreren met Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
