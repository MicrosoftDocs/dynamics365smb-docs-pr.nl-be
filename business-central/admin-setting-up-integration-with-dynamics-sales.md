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
ms.openlocfilehash: 0f59324e41695e35e09a2dd970492acb3a8dba58
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726894"
---
# <a name="setting-up-user-accounts-for-integrating-with-dynamics-365-for-sales"></a>Gebruikersaccounts instellen voor integratie met Dynamics 365 for Sales
Dit artikel geeft een overzicht van hoe u de gebruikersaccounts instelt die vereist zijn om [!INCLUDE[crm_md](includes/crm_md.md)] te integreren met [!INCLUDE[d365fin](includes/d365fin_md.md)].  

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2085500]

## <a name="setting-up-the-administrator-user-account-in-sales"></a>Het beheerdersaccount instellen in Sales
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

## <a name="minimum-permissions-for-user-accounts-in-includecrmmdincludescrmmdmd"></a>Minimale machtigingen voor gebruikersaccounts in [!INCLUDE[crm_md](includes/crm_md.md)]
Wanneer u de integratieoplossing installeert, worden machtigingen voor het integratiegebruikersaccount geconfigureerd in [!INCLUDE[crm_md](includes/crm_md.md)]. Als deze machtigingen zijn gewijzigd, moet u deze mogelijk opnieuw instellen. U kunt dat doen door de integratieoplossing opnieuw te installeren of door deze handmatig opnieuw in te stellen. De volgende tabellen bevatten de minimale machtigingen voor de gebruikersaccounts in [!INCLUDE[crm_md](includes/crm_md.md)].

### <a name="integration-administrator"></a>Integratiebeheerder
In de volgende tabel worden de minimale machtigingen voor elk tabblad weergegeven voor elke beveiligingsrol die vereist is voor de beheerder.

##### <a name="customization"></a>Aanpassing
|Beveiligingsrol|Toegangsniveau|Dynamics NAV 2018 en eerder|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Modelgestuurde app|Globaal|||Lezen|
|Invoegtoepassingsassembly|Globaal|Lezen|Lezen|Lezen|
|Type invoegtoepassing|Globaal|Lezen|Lezen|Lezen|
|Relatie|Globaal|||Lezen|
|SDK-bericht|Globaal|Lezen|Lezen|Lezen|
|Verwerkingsstap van SDK-bericht|Globaal|Lezen|Lezen|Lezen|
|Afbeelding van verwerkingsstap van SDK-bericht|Globaal|Lezen|Lezen|Lezen|
|Systeem van|Globaal|||Schrijven|

##### <a name="custom-entities"></a>Aangepaste entiteiten
|Beveiligingsrol|Toegangsniveau|Dynamics NAV 2018 en eerder|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Business Central-accountstatistieken|Globaal|Lezen|Lezen|Lezen|
|Business Central-verbinding|Globaal|Maken, lezen, schrijven, verwijderen|Maken, lezen, schrijven, verwijderen|Maken, lezen, schrijven, verwijderen|
|Configuratie boeken|Globaal|||Schrijven|

#### <a name="integration-user"></a>Integratiegebruiker
In de volgende tabel worden de minimale machtigingen voor elk tabblad weergegeven voor elke beveiligingsrol die vereist is voor de integratiegebruiker.

##### <a name="core-records"></a>Kernrecords
|Beveiligingsrol|Toegangsniveau|Dynamics NAV 2018 en eerder|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Rekening|Globaal|Maken, lezen, schrijven, toevoegen, toevoegen aan, toewijzen|Maken, lezen, schrijven, toevoegen, toevoegen aan, toewijzen|Maken, lezen, schrijven, toevoegen, toevoegen aan, toewijzen|
|Actiekaart|Globaal||Lezen|Lezen|
|Verbinding|Globaal|Lezen|Lezen|Lezen|
|Contactpersoon|Globaal|Maken, lezen, schrijven, toevoegen, toevoegen aan|Maken, lezen, schrijven, toevoegen, toevoegen aan|Maken, lezen, schrijven, toevoegen, toevoegen aan|
|Opmerking|Globaal|||Maken, lezen, schrijven, verwijderen, toevoegen, toewijzen|
|Opportunity|Globaal||Maken, lezen, schrijven, toevoegen, toevoegen aan|Maken, lezen, schrijven, toevoegen, toevoegen aan|
|Post|Globaal|||Maken, lezen, toevoegen aan|
|UI van gebruikersentiteit|Gebruiker|Maken, lezen, schrijven|Maken, lezen, schrijven|Maken, lezen, schrijven|

##### <a name="sales"></a>Verkoop
|Beveiligingsrol|Toegangsniveau|Dynamics NAV 2018 en eerder|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Factureren|Globaal|Maken, lezen, schrijven, toevoegen, toevoegen aan|Maken, lezen, schrijven, toevoegen, toevoegen aan|Maken, lezen, schrijven, toevoegen, toevoegen aan|
|Order|Globaal|Lezen, schrijven, toevoegen aan|Lezen, schrijven, toevoegen aan|Lezen, schrijven, toevoegen, toevoegen aan, toewijzen|
|Product|Globaal|Maken, lezen, schrijven, toevoegen, toevoegen aan|Maken, lezen, schrijven, toevoegen, toevoegen aan|Maken, lezen, schrijven, toevoegen, toevoegen aan|
|Eigenschap|Globaal|Lezen|Lezen|Lezen|
|Eigenschapkoppeling|Globaal|Lezen|Lezen|Lezen|
|Item van eigenschapoptieset|Globaal|Lezen|Lezen|Lezen|
|Offerte|Globaal|Lezen|Lezen|Lezen|

##### <a name="service"></a>Onderhoud
|Beveiligingsrol|Toegangsniveau|Dynamics NAV 2018 en eerder|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Aanvraag|Globaal|Lezen|Lezen|Lezen|

##### <a name="business-management"></a>Bedrijfsmanagement
|Beveiligingsrol|Toegangsniveau|Dynamics NAV 2018 en eerder|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Valuta|Globaal|Maken, lezen, schrijven|Maken, lezen, schrijven|Maken, lezen, schrijven|
|Organisatie|Globaal|Lezen, schrijven|Lezen, schrijven|Lezen, schrijven|
|Beveiligingsrol|Globaal|||Lezen|
|Gebruiker|Globaal|Maken, lezen, schrijven, toevoegen, toevoegen aan|Maken, lezen, schrijven, toevoegen, toevoegen aan|Maken, lezen, schrijven, toevoegen, toevoegen aan|
|Gebruikersinstellingen|Globaal|Maken, lezen, schrijven, verwijderen, toevoegen aan|Maken, lezen, schrijven, verwijderen, toevoegen aan|Maken, lezen, schrijven, verwijderen, toevoegen aan|
|Handelen namens een andere gebruiker|Globaal|Ja|Ja|Ja|

##### <a name="customization"></a>Aanpassing
|Beveiligingsrol|Toegangsniveau|Dynamics NAV 2018 en eerder|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Veld|Globaal||Lezen|Lezen|
|Invoegtoepassingsassembly|Globaal|Lezen|Lezen|Lezen|
|Type invoegtoepassing|Globaal|Lezen|Lezen|Lezen|
|SDK-bericht|Globaal|Lezen|Lezen|Lezen|
|Verwerkingsstap van SDK-bericht|Globaal|Lezen|Lezen|Lezen|
|Webresource|Globaal|Lezen|Lezen|Lezen|

##### <a name="custom-entities"></a>Aangepaste entiteiten
|Beveiligingsrol|Toegangsniveau|Dynamics NAV 2018 en eerder|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central-accountstatistiek|Globaal|Maken, lezen, schrijven, toevoegen aan|Maken, lezen, schrijven, toevoegen aan|Maken, lezen, schrijven, toevoegen aan|
|Dynamics 365 Business Central-verbinding|Globaal|Lezen|Lezen|Lezen|

### <a name="product-availability-user"></a>Gebruiker van productbeschikbaarheid
U kunt verkoopmedewerkers toestaan voorraadniveaus te bekijken voor de artikelen die ze verkopen door ze de machtigingen te verlenen die worden beschreven in de volgende tabel.

##### <a name="custom-entities"></a>Aangepaste entiteiten
|Beveiligingsrol|Toegangsniveau|Dynamics NAV 2018 en eerder|Business Central <br> Oktober 2018|Business Central <br> April 2019|
|----|----|-----|----|----|
|Dynamics 365 Business Central-accountstatistiek|Globaal|Maken, lezen, schrijven, toevoegen aan|Maken, lezen, schrijven, toevoegen aan|Maken, lezen, schrijven, toevoegen aan|
|Dynamics 365 Business Central-verbinding|Globaal|Lezen|Lezen|Lezen|

## <a name="see-also"></a>Zie ook  
[Integreren met Dynamics 365 for Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)  
