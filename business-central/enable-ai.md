---
title: Op AI gebaseerde artikelmarketingtekst (preview) met Copilot configureren
description: In dit artikel wordt uitgelegd hoe u een Copilot-proefversie van Business Central kunt krijgen en Copilot kunt inschakelen in een omgeving
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 03/22/2023
ms.custom: bap-template
---

# Op AI gebaseerde artikelmarketingtekst (preview) met Copilot configureren

[!INCLUDE[ai-preview](includes/ai-preview.md)]

In dit artikel wordt uitgelegd hoe u de mogelijkheid kunt beheren om op AI gebaseerde artikelmarketingtekst te maken met Copilot voor uw organisatie. Deze taak wordt uitgevoerd door een beheerder. Er zijn twee vereisten waaraan u moet voldoen om de functie beschikbaar te maken voor gebruikers:

- De functie **Op AI gebaseerde productbeschrijvingen maken met Copilot** inschakelen.
- Instemmen met de voorwaarden van [preview](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) en [Privacyverklaring van Microsoft](https://go.microsoft.com/fwlink/?LinkId=521839) namens de organisatie.

Als aan een van deze vereisten niet wordt voldaan, is de functie niet beschikbaar voor gebruik.

## Vereisten

U gebruikt een [preview-versie](ai-preview-getstarted.md) van Business Central die is ingeschakeld voor Copilot. Het inschakelen van Copilot wordt gedaan door een beheerder. Ga voor meer informatie naar [Op AI gebaseerde artikelmarketingtekst met Copilot configureren](enable-ai.md).

## De functie Op AI gebaseerde productbeschrijvingen maken met Copilot in- of uitschakelen

1. Zoek in Business Central de pagina **Functiebeheer** en open deze.
2. Stel de kolom **Geactiveerd voor** voor de functie **Functiepreview: Op AI gebaseerde productbeschrijvingen maken met Copilot** in op **Alle gebruikers** om de functie in te schakelen of **Geen** om deze uit te schakelen.

   Ga voor meer informatie over functiebeheer in het algemeen naar [Functiebeheer](/dynamics365/business-central/dev-itpro/administration/feature-management).

## De preview en privacyvoorwaarden accepteren of afwijzen voor alle gebruikers

1. Zoek in Business Central de pagina **Status van privacyverklaringen** en open deze.
2. Selecteer in de kolom **Integratienaam** **Azure OpenAI** en lees de voorwaarden die aan u worden gepresenteerd.
3. Selecteer in de rij **Azure OpenAI** het selectievakje **Voor iedereen accepteren** om toestemming te geven of het selectievakje **Voor iedereen afwijzen** om af te wijzen.

## Volgende stappen

Zodra u een sandbox of proefomgeving heeft, bent u klaar om Copilot uit te proberen op artikelen in Business Central. Ga naar [Marketingtekst aan artikelen toevoegen](item-marketing-text.md).  

## Zie ook

[Overzicht van op AI gebaseerde artikelmarketingtekst met Copilot configureren](ai-overview.md)  
[Marketingteksten voor artikelen maken met Copilot](item-marketing-text.md)  
[Veelgestelde vragen over op AI gebaseerde artikelmarketingtekst met Copilot](ai-faq.md)  