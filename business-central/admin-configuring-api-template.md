---
title: API-sjablonen configureren | Microsoft Docs
description: De stappen beschrijven die u moet doorlopen om API-sjablonen te configureren voor Dynamics 365 Business Central.
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API templates, configuring templates
ms.date: 10/01/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 7420bd1b8c1c246b608910a35a47ac025eec6b8b
ms.contentlocale: nl-be
ms.lasthandoff: 11/26/2018

---

# <a name="configuring-api-templates"></a>API-sjablonen configureren
De API-bibliotheek voor [!INCLUDE[d365fin_md](includes/d365fin_md.md)] biedt een vereenvoudigde weergave van de onderliggende entiteiten. Niet alle eigenschappen in de toepassing zijn beschikbaar via de bijbehorende API. Met de pagina **API-instelling** kunt u sjablonen definiëren die worden gebruikt om lege eigenschappen te vullen van een entiteit wanneer u een POST-actie maakt met behulp van de API. 

Als bijvoorbeeld een configuratiesjabloon voor de artikelentiteit wordt gedefinieerd, wanneer een nieuwe artikelrecord wordt gemaakt met de artikelen-API, worden eigenschappen van het nieuwe artikel die niet zijn gedefinieerd in de API-aanroep, gevuld vanuit de geselecteerde sjabloon. Als met de API bijvoorbeeld geen waarde wordt gedefinieerd voor het veld **Productieboekingsgroep**, maar een waarde is gedefinieerd in de geselecteerde sjabloon, wordt de boekingsgroepswaarde die in de sjabloon is gedefinieerd, toegepast op het nieuwe artikel. 

## <a name="setting-up-the-entity-template"></a>De entiteitsjabloon instellen
Als u sjablonen wilt gebruiken met de API-bibliotheek, moet u eerst eigenschappen voor de sjablonen instellen en definiëren. U kunt deze sjablonen instellen op de pagina **Configuratiesjablonen**. Zie voor meer informatie [Klantgegevens migreren voorbereiden](admin-use-templates-to-prepare-customer-data-for-migration.md). 

## <a name="assign-the-template-to-an-api"></a>De sjabloon toewijzen aan een API

Als u een sjabloon wilt toewijzen aan een API, moet u de volgende stappen uitvoeren.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **API-instelling** in en kies vervolgens de gerelateerde koppeling.
2. Kies **Nieuw** en kies de waarde **Volgorde** voor de record.  
Als er meer dan één sjabloon is geselecteerd voor een API (Pagina-id), worden de sjablonen toegepast in de volgorde die is gedefinieerd in de kolom **Volgorde**.   
Wanneer elke sjabloon wordt toegepast, worden veldwaarden die in de sjabloon zijn gedefinieerd, alleen toegepast op velden waarvoor nog geen waarde is gedefinieerd, hetzij expliciet in de sjabloon, hetzij in een eerder toegepaste sjabloon in de volgorde. 
3. Selecteer een waarde voor **Pagina-id**.  
Dit is de pagina voor de API waarop de sjabloon wordt toegepast. De opzoekactie **Pagina-id** biedt een overzicht van alle API's die beschikbaar zijn in de bibliotheek.
4. Selecteer een waarde in het veld **Sjablooncode**.  
De sjablooncode is de code voor de sjabloon die op de pagina **Sjablonen voor configuratie** is gedefinieerd. De gedefinieerde sjabloonwaarden worden toegepast op de API. 
5. Geef in het veld **Voorwaarden** op welke sjabloon moet worden toegepast.  
De gedefinieerde sjabloon wordt toegepast op een nieuwe record die met de API wordt gemaakt als en alleen als aan de voorwaarden die in het veld **Voorwaarden** zijn gedefinieerd, wordt voldaan door de waarden die al zijn gedefinieerd voor het nieuwe exemplaar van de entiteit.

## <a name="see-also"></a>Zie ook
[API-documentatie](/dynamics-nav/fin-graph)  
[Connect Apps ontwikkelen voor [!INCLUDE[d365fin_md](includes/d365fin_md.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
[De API's inschakelen](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[Eindpunten voor de API's](/dynamics-nav/endpoints-apis-for-dynamics)  
[Een bedrijf instellen met RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Beheer](admin-setup-and-administration.md)
