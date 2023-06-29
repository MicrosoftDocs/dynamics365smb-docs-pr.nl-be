---
title: Toegang tot Business Central beheren
description: Beheerders gebruiken een gelaagde aanpak om de toegang tot Business Central en de bijbehorende mogelijkheden te beheren.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: jswymer
ms.topic: overview
ms.date: 04/04/2023
ms.custom: bap-template
---

# <a name="manage-access-to-business-central"></a><a name="manage-access-to-business-central"></a>Toegang tot Business Central beheren

Dit artikel geeft beheerders en app-ontwikkelaars een algemeen overzicht van hoe ze de toegang tot [!INCLUDE [prod_short](includes/prod_short.md)] en zijn functies kunnen beheren. Gebruik de koppelingen om naar andere artikelen te gaan die meer details over de onderwerpen geven.

## <a name="layered-access"></a><a name="layered-access"></a>Gelaagde toegang

[!INCLUDE [prod_short](includes/prod_short.md)] maakt gebruik van een gelaagde benadering van applicatiebeveiliging, zoals weergegeven in het volgende diagram. Ga voor meer informatie over elke laag naar [Toepassingsbeveiliging in Business Central](/dynamics365/business-central/dev-itpro/security/security-application).

:::image type="content" source="media/security-overview.png" alt-text="Gelaagde toepassingsbeveiliging in Business Central.":::

## <a name="licenses"></a><a name="licenses"></a>Licenties

Wijs [!INCLUDE [prod_short](includes/prod_short.md)]-gebruikers toe aan een **Dynamics 365 Business Central**-licentie zodat ze hun bedrijfsgegevens kunnen bekijken, wijzigen en gebruiken vanuit elke gebruikersinterface. Ga voor meer informatie over licenties naar [Licenties in Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/deployment/licensing).

Echter, mensen die af en toe alleen-lezen toegang nodig hebben tot informatie in [!INCLUDE [prod_short](includes/prod_short.md)] kunnen een **Microsoft 365**-licentie gebruiken. Ga voor meer informatie over het verlenen van beperkte toegang naar [Business Central-toegang met Microsoft 365-licenties](admin-access-with-m365-license.md).

Voor uitgebreide informatie over de verschillende soorten licenties en hoe licenties werken in [!INCLUDE[prod_short](includes/prod_short.md)] [downloadt u de Dynamics 365 Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544).

## <a name="business-central-administrator-tasks"></a><a name="business-central-administrator-tasks"></a>Beheertaken in Business Central

De volgende tabel laat zien hoe beheerders de toegang kunnen beheren tot [!INCLUDE [prod_short](includes/prod_short.md)] en de functies die mensen zullen gebruiken. Sommige taken helpen ook om de toegangsinstellingen up-to-date te houden.

|Taak| Meer informatie |
|--|--|--|
|Elke persoon moet een gebruikersaccount hebben voordat ze zich kunnen aanmelden bij [!INCLUDE [prod_short](includes/prod_short.md)]. De eenvoudigste manier om gebruikers in te stellen, is door ze één voor één toe te voegen in het [Microsoft 365 beheercentrum](https://go.microsoft.com/fwlink/p/?linkid=2024339). |[Gebruikers toevoegen en tegelijkertijd licenties toewijzen](/microsoft-365/admin/add-users/add-users)|
|Beheer de toegang voor alle gebruikers op omgevingsniveau. Maak een Azure Active Directory (Azure AD)-beveiligingsgroep en wijs deze toe aan de omgeving.<br><br> U kunt ook beveiligingsgroepen gebruiken om de toegang voor specifieke groepen gebruikers te beheren. | [Toegang tot omgevingen beheren](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-access)<br><br>[Toegang tot Business Central beheren met behulp van beveiligingsgroepen](ui-security-groups.md) |
|Maak gebruikers in [!INCLUDE [prod_short](includes/prod_short.md)] en bepaal wie kan inloggen. | [Gebruikers maken volgens licenties](ui-how-users-permissions.md) |
|In combinatie met gebruikerslicenties definiëren machtigingen de objecten waartoe een gebruiker toegang heeft binnen elke database of omgeving. Geef op of mensen gegevens in database-objecten kunnen lezen, wijzigen of invoeren. |[Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md)|
|Als een externe accountant uw boeken en financiële rapportages beheert, nodig deze dan uit in uw [!INCLUDE [prod_short](includes/prod_short.md)]. Zij kunnen dan nauwer met u samenwerken aan uw fiscale gegevens.|[Accountantervaringen binnen [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)|
|Als u een [!INCLUDE [prod_short](includes/prod_short.md)]-wederverkooppartner bent, kunt u een e-mail sturen naar een klant om een wederverkoperrelatie aan te vragen. U kunt gedelegeerde beheerrechten voor Azure Active Directory en Microsoft 365 in de e-mail opnemen.| [Gedelegeerde beheerderstoegang tot Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin)|
|Een Azure-servicetag vertegenwoordigt een groep IP-adressen waar verkeer voor een service vandaan kan komen of naartoe kan gaan. Gebruik servicetags om firewalls zo in te stellen dat alleen verkeer van bepaalde services wordt toegestaan. Met de tag **Dynamics365BusinessCentral** kunt u firewall- en netwerkbeveiligingsgroepregels gebruiken om het verkeer van en naar [!INCLUDE [prod_short](includes/prod_short.md)] te beperken.| [Tags voor Azure-beveiligingsservices](/dynamics365/business-central/dev-itpro/security/security-service-tags)|
|Als u Azure Active Directory-verificatie gebruikt met [!INCLUDE [prod_short](includes/prod_short.md)], raden we u aan om gebruik te maken van [Azure AD-multifactorverificatie (MFA)](/azure/active-directory/authentication/concept-mfa-howitworks). MFA waarborgt verder de toegang tot de applicatie en gegevens.|[Multifactorverificatie voor Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/security/multifactor-authentication)|

## <a name="business-central-developer-tasks"></a><a name="business-central-developer-tasks"></a>Business Central-ontwikkelaarstaken

Er is ook een ontwikkelaarsverhaal voor het beheren van de toegang tot [!INCLUDE [prod_short](includes/prod_short.md)]. Ontwikkelaars en beheerders kunnen bijvoorbeeld toepassingen maken en verbinden met [!INCLUDE [prod_short](includes/prod_short.md)] die het bedrijf ten goede komen:  

* Bedrijfsprocessen stroomlijnen
* Klantinteracties verbeteren
* Sneller betere beslissingen nemen

De volgende tabel bevat koppelingen naar informatie over hoe u apps en extensies toegang kunt geven tot [!INCLUDE [prod_short](includes/prod_short.md)]-gegevens.

| Taak | Meer informatie |
|--|--|
|De twee belangrijkste concepten voor het definiëren van toegang tot functies zijn rechten en machtigingen. Rechten geven brede toegang tot objecten volgens licenties of Azure Active Directory-rollen. Met machtigingen en machtigingensets kunt u de toegang tot objecten verfijnen. |[Overzicht van rechten en machtigingensets](/dynamics365/business-central/dev-itpro/developer/devenv-entitlements-and-permissionsets-overview)|

## <a name="see-also"></a><a name="see-also"></a>Zie ook

[Beveiliging in Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection)
