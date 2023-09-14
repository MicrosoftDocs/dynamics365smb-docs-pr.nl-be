---
title: API-sjablonen configureren
description: De stappen beschrijven die u moet doorlopen om API-sjablonen te configureren voor Dynamics 365 Business Central.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'API templates, configuring templates'
ms.search.form: 5469
ms.date: 06/07/2022
ms.author: bholtorf
---

# API-sjablonen configureren

De API-bibliotheek voor [!INCLUDE[prod_short_md](includes/prod_short.md)] biedt een vereenvoudigde weergave van de onderliggende entiteiten. Niet alle eigenschappen in de toepassing zijn beschikbaar via de bijbehorende API. Met de pagina **API-instelling** kunt u sjablonen definiëren die worden gebruikt om lege eigenschappen te vullen van een entiteit wanneer u een POST-actie maakt met behulp van de API. 

Als bijvoorbeeld een configuratiesjabloon voor de artikelentiteit wordt gedefinieerd, wanneer een nieuwe artikelrecord wordt gemaakt met de artikelen-API, worden eigenschappen van het nieuwe artikel die niet zijn gedefinieerd in de API-aanroep, gevuld vanuit de geselecteerde sjabloon. Als met de API bijvoorbeeld geen waarde wordt gedefinieerd voor het veld **Productieboekingsgroep**, maar een waarde is gedefinieerd in de geselecteerde sjabloon, wordt de boekingsgroepswaarde die in de sjabloon is gedefinieerd, toegepast op het nieuwe artikel. 

## De entiteitsjabloon instellen

Als u sjablonen wilt gebruiken met de API-bibliotheek, moet u eerst eigenschappen voor de sjablonen instellen en definiëren. U kunt deze sjablonen instellen op de pagina **Configuratiesjablonen**. Zie [On-premises gegevens migreren naar Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) (alleen in het Engels) in de beheerdersinhoud.  

## De sjabloon toewijzen aan een API

Als u een sjabloon wilt toewijzen aan een API, moet u de volgende stappen uitvoeren.

> [!NOTE]  
> API-sjablonen kunnen alleen worden ingesteld met de volgende API-pagina's: contacten, landen/regio's, valuta's, klanten, werknemers, artikelcategorieën, betalingsmethoden, betalingsvoorwaarden, verzendmethoden, maateenheden en leveranciers.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **API-instelling** in en kies vervolgens de gerelateerde koppeling.
2. Kies **Nieuw** en kies de waarde **Volgorde** voor de record.  

    Als er meer dan één sjabloon is geselecteerd voor een API (Pagina-id), worden de sjablonen toegepast in de volgorde die is gedefinieerd in de kolom **Volgorde**.  

    Wanneer elke sjabloon wordt toegepast, worden veldwaarden die in de sjabloon zijn gedefinieerd, alleen toegepast op velden waarvoor nog geen waarde is gedefinieerd, hetzij expliciet in de sjabloon, hetzij in een eerder toegepaste sjabloon in de volgorde.  
3. Selecteer een waarde voor **Pagina-id**.  

    Dit is de pagina voor de API waarop de sjabloon wordt toegepast. De opzoekactie **Pagina-id** biedt een overzicht van alle API's die beschikbaar zijn in de bibliotheek.
4. Selecteer een waarde in het veld **Sjablooncode**.  

    De sjablooncode is de code voor de sjabloon die op de pagina **Sjablonen voor configuratie** is gedefinieerd. De gedefinieerde sjabloonwaarden worden toegepast op de API.  
5. Geef in het veld **Voorwaarden** op welke sjabloon moet worden toegepast.  

    De gedefinieerde sjabloon wordt toegepast op een nieuwe record die met de API wordt gemaakt als en alleen als aan de voorwaarden die in het veld **Voorwaarden** zijn gedefinieerd, wordt voldaan door de waarden die al zijn gedefinieerd voor het nieuwe exemplaar van de entiteit.

## Zie ook

[API-documentatie](/dynamics-nav/fin-graph)  
[Connect Apps ontwikkelen voor [!INCLUDE[prod_short_md](includes/prod_short.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
[De API's inschakelen](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[Eindpunten voor de API's](/dynamics-nav/endpoints-apis-for-dynamics)  
[Beheer](admin-setup-and-administration.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]