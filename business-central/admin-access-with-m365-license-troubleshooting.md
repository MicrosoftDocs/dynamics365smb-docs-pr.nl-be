---
title: Problemen met toegang met Microsoft 365-licenties oplossen
description: Leer hoe u problemen met toegang tot Business Central met enkel een Microsoft 365-licentie kunt oplossen.
author: mikebc
ms.author: mikebc
ms.reviewer: jswymer
ms.topic: troubleshooting
ms.date: 02/07/2023
ms.custom: bap-template
ms.search.keywords: 'License, access, Microsoft 365, collaborate, collaboration, Teams, Microsoft Teams'
---

# Problemen met toegang met Microsoft 365-licenties oplossen

## "Deze pagina gebruikt gegevens uit gerelateerde tabellen waartoe u geen toegang hebt" foutbericht

### Symptomen

Wanneer u een record in Teams opent, krijgt u een foutmelding te zien in een tabblad of kaartgegevens die lijkt op:

"Deze pagina gebruikt gegevens uit gerelateerde tabellen waartoe u geen toegang hebt. Neem contact op met uw beheerder om met alle functies van deze pagina te werken."

### Oorzaak

U mist hoogstwaarschijnlijk objectmachtigingen voor tabellen waarnaar de huidige pagina of record verwijst.

## Microsoft 365-toegang is ingeschakeld, maar gebruikers krijgen een toestemmingsfout

### Symptomen

Toegang met Microsoft 365 is ingeschakeld in het Business Central-beheercentrum, maar gebruikers krijgen een toestemmingsfout bij het openen van een record.

### Oorzaak

Als u toegang inschakelt in het Business Central-beheercentrum, maar geen machtigingen toewijst op de pagina **Licentieconfiguratie**, wordt voor iedereen die Business Central-records probeert te openen in Teams de gebruikersrecord ingericht zonder machtiging voor objecten. Business Central is van nature veilig: beheerders moeten eerst configureren welke gegevens toegankelijk zijn in Teams. 

### Oplossing

Het aanpassen van machtigingen op de pagina Licentieconfiguratie heeft alleen invloed op nieuw aangemaakte gebruikers. U moet ook de ontbrekende machtigingen toewijzen aan gebruikers die al zijn gemaakt via de lijstpagina Gebruikers. 

## U hebt een link gedeeld in Teams, maar gebruikers krijgen een bericht dat ze alleen gegevens kunnen inzien

### Symptomen

Als u een koppeling deel in Teams als gebruiker van Business Central, krijgen anderen de foutmelding "Wanneer u Business Central met enkel een Microsoft 365-licentie opent, kunt u alleen gegevens bekijken in Microsoft Teams".

### Oorzaak

Bij het delen van een Business Central-koppeling naar een Teams-chat of -kanalen, verlaat u Microsoft Teams altijd wanneer u een koppeling opent. Daar zijn de gegevens niet meer toegankelijk voor iemand met een Microsoft 365-licentie.

### Oplossing

Neem bij het delen van pagina's of records het koppelingsvoorbeeld op als kaart of deel gegevens als een tabblad in de chat of het kanaal.

## Kaart van gedeelde link is minimaal en bevat geen Details-knop

### Symptomen 

Wanneer een Microsoft 365-licentiehouder zonder Business Central-licentie een Business Central-link deelt in Teams, wordt deze automatisch uitgevouwen tot een kaart zonder bruikbare informatie en toont alleen Business Central zonder **Details**-knop.

### Oorzaak

Gebruikers die een Microsoft 365-licentie hebben maar geen Business Central-licentie mogen geen links als kaarten delen. Als de gebruiker de Business Central-app voor Teams heeft geïnstalleerd en een koppeling in het opstelgebied plakt, wordt slechts een minimale kaart weergegeven. 

## Zie ook

[Toegang tot Business Central met Microsoft 365-licenties](admin-access-with-m365-license.md#minimum-requirements)  
[Toegang met Microsoft 365-licenties instellen](admin-access-with-m365-license-setup.md)  
[Business Central en Microsoft Teams-integratie](across-teams-overview.md)
[Business Central-records en paginakoppelingen delen in Microsoft Teams](across-working-with-teams.md)  
[Problemen met integratie van Teams oplossen](admin-teams-troubleshooting.md)  