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

[!INCLUDE [2023rw1-sec-group-long](includes/2023rw1-sec-group-long.md)]

Beveiligingsgroepen maken het voor beheerders gemakkelijker om gebruikersmachtigingen te beheren in hun Dynamics 365-applicaties, zoals SharePoint Online, CRM Online en de online versie van [!INCLUDE [prod_short](includes/prod_short.md)]. Beheerders voegen machtigingen toe aan hun beveiligingsgroepen en wanneer ze gebruikers aan de groep toevoegen, gelden de machtigingen voor alle leden. Een beheerder kan bijvoorbeeld een beveiligingsgroep maken waarmee verkopers verkooporders kunnen maken en boeken. Of laat inkopers hetzelfde doen voor inkooporders.

Maak uw beveiligingsgroepen in uw Microsoft 365-beheercentrum of Azure Active Directory. Dit artikel beschrijft de stappen in het Microsoft 365-beheercentrum, maar de stappen zijn in beide hetzelfde.

## Een beveiligingsgroep toevoegen in het Microsoft 365-beheercentrum

1. Ga in het Microsoft 365-beheercentrum naar de pagina **Actieve teams en groepen**.
2. Kies **Een groep toevoegen**.
3. Kies het groepstype **Beveiliging** en kies vervolgens **Volgende**.
4. Specificeer de basis voor uw groep.
5. Optioneel: maak de leden van de groep beschikbaar voor roltoewijzing. Ga voor meer informatie over de toewijzingen naar [Azure AD-groepen gebruiken om roltoewijzingen te beheren](/azure/active-directory/roles/groups-concept).
6. Open de groep en gebruik vervolgens het tabblad **Leden toevoegen** om mensen in de groep op te nemen.

## Een beveiligingsgroep in Business Central toevoegen

Maak in [!INCLUDE [prod_short](includes/prod_short.md)] een beveiligingsgroep en koppel deze vervolgens aan de beveiligingsgroep in het Microsoft 365-beheercentrum. Uw nieuwe groep bevat de leden die u hebt toegevoegd in het Microsoft 365-beheercentrum.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent 1.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Beveiligingsgroepen** in en kies vervolgens de gerelateerde koppeling.
2. Kies **Nieuw** om een groep te maken.
3. Voer in het veld **Naam** een naam voor de groep in.
4. Voer in het veld **Naam van AAD-beveiligingsgroep** de naam van de beveiligingsgroep precies zo in als deze wordt weergegeven in het Microsoft 365-beheercentrum. [!INCLUDE [prod_short](includes/prod_short.md)] zal die groep vinden en koppelen aan deze groep.

> [!NOTE]
> De gebruikers worden alleen op de kaart **Leden** in het feitenblokvenster of de pagina **Leden van beveiligingsgroep** weergegeven als ze zijn toegevoegd als gebruikers in [!INCLUDE [prod_short](includes/prod_short.md)]. Zie voor meer informatie over het toevoegen van gebruikers [Gebruikers toevoegen of gebruikersgegevens en licentietoewijzingen bijwerken in Business Central](ui-how-users-permissions.md#adduser).  

### Machtigingen toewijzen aan de groep

1. Kies op de pagina **Beveiligingsgroepen** de groep en kies vervolgens de actie **Machtigingen**.
1. Wijs machtigingen toe op de volgende manieren:
    * Om machtigingensets afzonderlijk toe te wijzen kiest u in het veld **Machtigingenset** de machtigingen die u wilt toewijzen.
    * Om meerdere machtigingensets toe te wijzen, kiest u de actie **Machtigingensets selecteren** en kiest u vervolgens de sets die u wilt toewijzen.

## De machtigingen in een beveiligingsgroep controleren

Op de pagina **Beveiligingsgroepen** toont het feitenblokvenster de **Machtigingensets** die aan de groep zijn toegewezen. Elke gebruiker die op de kaart **Leden** staat, heeft die machtigingen. De actie **Machtigingenset per beveiligingsgroep** biedt een meer gedetailleerd overzicht. Daar kunt u ook de individuele machtigingen in elke beveiligingsgroep bekijken.

Machtigingen zijn ook beschikbaar op de pagina **Gebruikers**. Het feitenblokvenster toont de kaarten **Machtigingensets vanuit beveiligingsgroepen** en **Lidmaatschappen van beveiligingsgroepen** voor de geselecteerde gebruiker.

## Beveiligingsgroepen en gebruikersgroepen

Als u gebruikersgroepen heeft, kunt u de groepen converteren naar machtigingensets in uw tenant met behulp van de begeleide instelling **Migratie van gebruikersgroepen**. Om de handleiding te starten gaat u op de pagina **Functiebeheer** naar **Functie: Machtigingen van gebruikersgroepen converteren** en kiest u **Alle gebruikers** in het veld **Geactiveerd voor** . De begeleide instelling biedt de volgende opties voor de conversie.

|Optie  |Omschrijving  |
|---------|---------|
|Toewijzen aan gebruiker     | De machtigingen in gebruikersgroepen rechtstreeks toewijzen aan de gebruikers die aan de groep zijn toegewezen en hun gebruikersgroeptoewijzingen verwijderen.        |
|Converteren naar een machtigingenset     | Maak een nieuwe machtiging voor de machtigingen in elke gebruikersgroep. De nieuwe machtigingenset wordt toegewezen aan alle leden van elke gebruikersgroep.          |

## Zie ook

[Gebruikers maken volgens licenties](ui-how-users-permissions.md)  
[Business Central-toegang in Teams met Microsoft 365-licenties instellen](admin-access-with-m365-license-setup.md)  
[Meer informatie over groepen en toegangsrechten in Azure Active Directory](/azure/active-directory/fundamentals/concept-learn-about-groups)  
[Active Directory-beveiligingsgroepen](/windows-server/identity/ad-ds/manage/understand-security-groups)  