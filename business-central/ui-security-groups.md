---
title: Toegang beheren met behulp van beveiligingsgroepen
description: In dit artikel wordt beschreven hoe u beveiligingsgroepen gebruikt om gebruikersmachtigingen te definiëren.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'access, right, security, permissions'
ms.search.form: '1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862'
ms.date: 02/08/2023
---

# Toegang tot Business Central beheren met behulp van beveiligingsgroepen

[!INCLUDE[azure-ad-to-microsoft-entra-id](~/../shared-content/shared/azure-ad-to-microsoft-entra-id.md)]

Beveiligingsgroepen maken het voor beheerders eenvoudiger om gebruikersmachtigingen te beheren. Voor [!INCLUDE [prod_short](includes/prod_short.md)] online zijn ze bijvoorbeeld herbruikbaar in Dynamics 365-applicaties, zoals SharePoint Online, CRM Online en [!INCLUDE [prod_short](includes/prod_short.md)]. Beheerders voegen machtigingen toe aan hun [!INCLUDE [prod_short](includes/prod_short.md)]-beveiligingsgroepen en wanneer ze gebruikers aan de groep toevoegen, gelden de machtigingen voor alle leden. Een beheerder kan bijvoorbeeld een [!INCLUDE [prod_short](includes/prod_short.md)]-beveiligingsgroep maken waarmee verkopers verkooporders kunnen maken en boeken. Of laat inkopers hetzelfde doen voor inkooporders.

## Business Central Online en on-premises

U kunt beveiligingsgroepen gebruiken voor de online en on-premises versies van [!INCLUDE [prod_short](includes/prod_short.md)]. Maak op een van de volgende manieren groepen, afhankelijk van uw versie:

* Gebruik Microsoft Entra-beveiligingsgroepen voor de online versie. Ga voor meer informatie over het maken van de groep naar [Een beveiligingsgroep maken, bewerken of verwijderen in het Microsoft 365 beheercentrum](/microsoft-365/admin/email/create-edit-or-delete-a-security-group).
* Gebruik voor on-premises Windows Active Directory-groepen. Ga voor meer informatie naar [Een groepsaccount maken in Microsoft Entra ID](/windows/security/operating-system-security/network-security/windows-firewall/create-a-group-account-in-active-directory).

Maak daarna een corresponderende beveiligingsgroep in [!INCLUDE [prod_short](includes/prod_short.md)] en koppel deze vervolgens aan de groep die u hebt gemaakt. Ga voor meer informatie naar [Een beveiligingsgroep toevoegen in Business Central](#add-a-security-group-in-business-central).

> [!NOTE]
> Als u een speciaal type gebruiker hebt ingesteld met een Windows Group-licentietype in een versie van [!INCLUDE [prod_short](includes/prod_short.md)] on-premises die ouder is dan releasewave 1 van 2023 en u een upgrade uitvoert, converteert [!INCLUDE [prod_short](includes/prod_short.md)] de gebruiker naar een beveiligingsgroep. De nieuwe beveiligingsgroep heeft dezelfde naam als de Windows-groepsnaam. De beveiligingsgroep geeft u een beter overzicht van de groepsleden en hun effectieve machtigingen.

## Een beveiligingsgroep in Business Central toevoegen

1. Kies het pictogram ![Lampje dat de functie Vertel me opent 1.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Beveiligingsgroepen** in en kies vervolgens de gerelateerde koppeling.
1. Kies **Nieuw** om een groep te maken.
1. Maak de link naar uw groep als volgt:

    * Kies voor [!INCLUDE [prod_short](includes/prod_short.md)] Online de groep in het veld **Naam van Microsoft Entra-beveiligingsgroep**.
    * Kies voor [!INCLUDE [prod_short](includes/prod_short.md)] on-premises de groep in het veld **Windows-groepsnaam**.

> [!NOTE]
> De gebruikers worden alleen op de kaart **Leden** in het feitenblokvenster of de pagina **Leden van beveiligingsgroep** weergegeven als ze zijn toegevoegd als gebruikers in [!INCLUDE [prod_short](includes/prod_short.md)]. Zie voor meer informatie over het toevoegen van gebruikers [Gebruikers toevoegen of gebruikersgegevens en licentietoewijzingen bijwerken in Business Central](ui-how-users-permissions.md#adduser).  

### Machtigingen aan een beveiligingsgroep toewijzen

1. Kies op de pagina **Beveiligingsgroepen** de groep en kies vervolgens de actie **Machtigingen**.
1. Wijs machtigingen toe op de volgende manieren:

    * Om machtigingensets afzonderlijk toe te wijzen kiest u in het veld **Machtigingenset** de machtigingen die u wilt toewijzen.
    * Om meerdere machtigingensets toe te wijzen, kiest u de actie **Machtigingensets selecteren** en kiest u vervolgens de sets die u wilt toewijzen.

## De machtigingen in een beveiligingsgroep controleren

Op de pagina **Beveiligingsgroepen** toont het feitenblokvenster de **Machtigingensets** die aan de groep zijn toegewezen. Elke gebruiker die op de kaart **Leden** staat, heeft die machtigingen. De actie **Machtigingenset per beveiligingsgroep** biedt een meer gedetailleerd overzicht. Daar kunt u ook de individuele machtigingen in elke beveiligingsgroep bekijken.

Machtigingen zijn ook beschikbaar op de pagina **Gebruikers**. Het feitenblokvenster toont de kaarten **Machtigingensets vanuit beveiligingsgroepen** en **Lidmaatschappen van beveiligingsgroepen** voor de geselecteerde gebruiker.

## Beveiligingsgroepen en gebruikersgroepen

> [!NOTE]
> Gebruikersgroepen zullen in een toekomstige release niet meer beschikbaar zijn.

Beveiligingsgroepen zijn zeer vergelijkbaar met de gebruikersgroepen die momenteel beschikbaar zijn. Gebruikersgroepen zijn echter alleen relevant voor [!INCLUDE [prod_short](includes/prod_short.md)]. Beveiligingsgroepen zijn gebaseerd op groepen in Microsoft Entra ID of Windows Active Directory, afhankelijk van of u respectievelijk [!INCLUDE [prod_short](includes/prod_short.md)] Online of on-premises gebruikt. Groepen komen beheerders ten goede omdat ze die kunnen gebruiken met andere Dynamics 365-apps. Als verkopers bijvoorbeeld [!INCLUDE [prod_short](includes/prod_short.md)]en SharePoint gebruiken, hoeven beheerders de groep en de leden niet opnieuw te maken.

### Optioneel: converteer gebruikersgroepen naar machtigingssets

In releasewave 1 van 2023 en later kunt u gebruikersgroepen converteren naar machtigingensets in uw tenant. De machtigingensets bieden dezelfde functionaliteit als gebruikersgroepen. Enkele voorbeelden:

* U kunt het feitenblok **Gebruikers** gebruiken om machtigingen voor gebruikers te beheren.
* U kunt inzoomen op de naam van de machtigingenset om andere machtigingensets toe te voegen aan de set waaraan u werkt. Ga voor meer informatie naar [Andere machtigingensets toevoegen](ui-define-granular-permissions.md#to-add-other-permission-sets).

Gebruik de begeleide instelling **Migratie van gebruikersgroepen** om uw groepen te converteren. Om de handleiding te starten gaat u op de pagina **Functiebeheer** naar **Functie: Machtigingen van gebruikersgroepen converteren** en kiest u **Alle gebruikers** in het veld **Geactiveerd voor** . De begeleide instelling biedt de volgende opties voor de conversie.

|Optie  |Omschrijving  |
|---------|---------|
|Toewijzen aan gebruiker     | De machtigingen in gebruikersgroepen rechtstreeks toewijzen aan de gebruikers die aan de groep zijn toegewezen en hun gebruikersgroeptoewijzingen verwijderen.        |
|Converteren naar een machtigingenset     | Maak een nieuwe machtiging voor de machtigingen in elke gebruikersgroep. De nieuwe machtigingenset wordt toegewezen aan alle leden van elke gebruikersgroep.          |

### Licentieconfiguraties zijn nog steeds van toepassing

U kunt machtigingen configureren in [!INCLUDE [prod_short](includes/prod_short.md)] op basis van licenties. Deze machtigingen worden rechtstreeks toegewezen aan nieuwe gebruikers. Deze configuraties zijn nog steeds van toepassing, zelfs als u beveiligingsgroepen gaat gebruiken.

Als u uitsluitend beveiligingsgroepen wilt gebruiken, raden we u aan de licentieconfiguraties te verwijderen. Ga voor meer informatie over licentieconfiguraties naar [Gebruikers maken volgens licenties](ui-how-users-permissions.md).

U kunt licentieconfiguraties verwijderen op de pagina **Licentieconfiguratie**. Kies een licentie en verwijder vervolgens alle machtigingensets die eraan zijn toegewezen.

## Zie ook

[Gebruikers maken volgens licenties](ui-how-users-permissions.md)  
[Business Central-toegang in Teams met Microsoft 365-licenties instellen](admin-access-with-m365-license-setup.md)  
[Meer informatie over groepen en toegangsrechten in Microsoft Entra ID](/azure/active-directory/fundamentals/concept-learn-about-groups)  
[Microsoft Entra-beveiligingsgroepen](/windows-server/identity/ad-ds/manage/understand-security-groups)  