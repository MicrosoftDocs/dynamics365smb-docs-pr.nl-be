---
title: Gebruikerstoegangsstroom voor Microsoft 365-licenties
description: Krijg een overzicht van wat er gebeurt als een gebruiker voor het eerst Business Central-gegevens opent met zijn Microsoft 365-licentie.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---
# <a name="user-access-flow-for-microsoft-365-licenses"></a><a name="user-access-flow-for-microsoft-365-licenses"></a><a name="user-access-flow-for-microsoft-365-licenses"></a>Gebruikerstoegangsstroom voor Microsoft 365-licenties

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

In dit artikel is beschreven wat er gebeurt als een gebruiker voor het eerst Business Central-gegevens opent met zijn Microsoft 365-licentie. Door deze stroom te begrijpen, kunnen beheerders hun aanpak plannen en Business Central overeenkomstig hun zakelijke behoeften configureren.

1. Eerst wordt de identiteit van de gebruiker geverifieerd 
2. Business Central controleert of aan alle [minimumvereisten](admin-access-with-m365-license.md#minimum-requirements) zijn voldaan.
3. Business Central controleert of deze gebruiker geen hogere licentie heeft, zoals een Business Central-licentie of een beheerdersrol zoals een gedelegeerde beheerdersrol. 
4. Business Central controleert of de gebruiker gegevens wil inzien die behoren tot een omgeving waarvoor toegang met Microsoft 365-licenties is ingeschakeld. 
5. De gebruikersrecord wordt ingericht in Business Central, waarbij de Gebruikersgroep, het Profiel en de Machtigingensets worden toegewezen die zijn gedefinieerd op de Microsoft 365-licentie configuratiepagina. Standaard wordt de gebruikersgroep Teams-gebruikers toegewezen, wordt het profiel Medewerker toegewezen en wordt alleen de machtigingenset Aanmelden toegewezen. Elke andere standaardinstelling van gebruikersinstellingen wordt ook toegepast, net als een gelicentieerde Business Central-gebruiker. 
6. Het volledige Business Central-beveiligingsmodel wordt toegepast om te bepalen of de gebruiker toegang zou moeten hebben tot de record, pagina, in het opgegeven bedrijf en de opgegeven omgeving. 

Als alle stappen succesvol worden voltooid, kan de gebruiker deze Business Central-gegevens nu bekijken in Teams. De Business Central-service zorgt automatisch voor alleen-lezen-toegang en vereenvoudigt de UI. 

De gebruikersaccount is nu geregistreerd in Business Central en kan worden beheerd zoals elke andere Business Central-gebruiker.

> [!NOTE]
> De stappen kunnen variëren, afhankelijk van eventuele aanvullende beveiligingsconfiguraties die u hebt opgegeven in Microsoft 365 of Business Central.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Zie ook

[Toegang tot Business Central met Microsoft 365-licenties](admin-access-with-m365-license.md#minimum-requirements)  
[Toegang met Microsoft 365-licenties instellen](admin-access-with-m365-license-setup.md)  
