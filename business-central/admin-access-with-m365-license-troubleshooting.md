---
title: Problemen met toegang met Microsoft 365-licenties oplossen
description: Leer hoe u problemen met toegang tot Business Central met enkel een Microsoft 365-licentie kunt oplossen.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.service: dynamics365-business-central
ms.topic: troubleshooting
ms.date: 11/03/2022
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---

# Problemen met toegang met Microsoft 365-licenties oplossen

## Symptomen

Wanneer u een record in Teams opent, krijgt u een foutmelding te zien in een tabblad of kaartgegevens die lijkt op:

"Deze pagina gebruikt gegevens uit gerelateerde tabellen waartoe u geen toegang hebt. Neem contact op met uw beheerder om met alle functies van deze pagina te werken."

## Oorzaak

U mist hoogstwaarschijnlijk objectmachtigingen voor tabellen waarnaar de huidige pagina of record verwijst.

## Symptomen

Toegang is ingeschakeld, maar gebruikers krijgen een toestemmingsfout bij het openen van een record.

## Oorzaak

Als u toegang inschakelt in het Business Central-beheercentrum, maar geen machtigingen toewijst op de pagina Licentieconfiguratie, wordt voor iedereen die Business Central-records probeert te openen in Teams de gebruikersrecord ingericht zonder machtiging voor objecten. Business Central is van nature veilig: beheerders moeten eerst configureren welke gegevens toegankelijk zijn in Teams. 

## Oplossing

Het aanpassen van machtigingen op de pagina Licentieconfiguratie heeft alleen invloed op nieuw aangemaakte gebruikers. U moet ook de ontbrekende machtigingen toewijzen aan gebruikers die al zijn gemaakt via de lijstpagina Gebruikers. 

## Symptomen

Als ik een koppeling deel in Teams, krijgen anderen de foutmelding "Wanneer u Business Central met enkel een Microsoft 365-licentie opent, kunt u alleen gegevens bekijken in Microsoft Teams".

## Oorzaak

Bij het delen van een Business Central-koppeling naar een Teams-chat of -kanalen, verlaat u Microsoft Teams altijd wanneer u een koppeling opent. Daar zijn de gegevens niet meer toegankelijk voor iemand met een Microsoft 365-licentie.

## Oplossing

Neem bij het delen van pagina's of records het koppelingsvoorbeeld op als kaart of deel gegevens als een tabblad in de chat of het kanaal.

## Zie ook

[Toegang tot Business Central met Microsoft 365-licenties](admin-access-with-m365-license.md#minimum-requirements)  
[Toegang met Microsoft 365-licenties instellen](admin-access-with-m365-license-setup.md)  
[Business Central en Microsoft Teams-integratie](across-teams-overview.md)
[Business Central-records en paginakoppelingen delen in Microsoft Teams](across-working-with-teams.md)  
[Problemen met integratie van Teams oplossen](admin-teams-troubleshooting.md)  