---
title: Problemen oplossen met Copilot- en AI-mogelijkheden
description: Leer hoe u veelvoorkomende problemen oplost die u kunt tegenkomen tijdens het werken met Copilot- en AI-mogelijkheden in Business Central.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: troubleshooting
ms.collection:
  - bap-ai-copilot
ms.date: 11/15/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Problemen oplossen met Copilot- en AI-mogelijkheden

Copilot is een door AI aangedreven functionaliteit in Business Central die helpt bij verschillende taken, zoals het opstellen van marketingteksten en het reconciliëren van bankrekeningen. Als u problemen ondervindt met Copilot of andere AI-mogelijkheden, kan dit artikel u helpen veelvoorkomende problemen te identificeren en op te lossen.

## Copilot verschijnt niet op pagina's

Als de functionaliteit van Copilot, zoals de actie **Opstellen met Copilot** voor marketingtekstsuggesties of de actie **Reconciliëren met Copilot** voor hulp bij het reconciliëren van bankrekeningen, niet op een pagina verschijnt zoals verwacht, controleert u het volgende:

- Als de functie wordt beheerd onder Functiebeheer, zorg er dan voor dat deze is ingeschakeld. [Meer informatie over functiebeheer](admin-feature-management.md).

- Zorg ervoor dat de functionaliteit niet verborgen blijft door personalisatie. [Meer informatie over personalisatie](ui-personalization-user.md)

## Copilot verschijnt op pagina's, maar u krijgt een foutmelding dat deze niet is geactiveerd

Wanneer u Copilot probeert te gebruiken en u een foutmelding krijgt die lijkt op **Sorry, Copilot is niet geactiveerd voor \[functie\]**, moet u een aantal dingen controleren:

- Zorg er eerst voor dat de functie is geactiveerd op de pagina **Copilot en AI-mogelijkheden**. [Meer informatie over het activeren van Copilot- en AI-mogelijkheden](enable-ai.md#activate-features). 
- Zorg er vervolgens voor dat de privacyverklaring voor Azure OpenAI-integratie niet is ingesteld op **Voor iedereen afwijzen**. Als dat zo is, wijzig dit dan in **Voor iedereen accepteren**. [Meer informatie over privacyverklaringen](privacy-notices-status.md).

## Zie ook

[Copilot- en AI-mogelijkheden configureren](enable-ai.md)  
[Marketingtekstsuggesties met Copilot](ai-overview.md)  
[Bankrekeningen reconciliëren met Copilot](bank-reconciliation-with-copilot.md)  
