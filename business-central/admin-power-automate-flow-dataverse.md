---
title: Gebruik een Power Automate-stroom voor waarschuwingen voor entiteitswijzigingen
description: Leer hoe u een stroom in Power Automate maakt die u waarschuwt wanneer een entiteit wordt gewijzigd in de Dataverse-omgeving.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Power Automate, Flow, Dataverse
ms.search.form: ''
ms.date: 09/05/2022
ms.author: bholtorf
ROBOTS: NOINDEX, NOFOLLOW
ms.openlocfilehash: fb5b2fa88289ff3d9d491f9b8ee7d73706740020
ms.sourcegitcommit: 8b95e1700a9d1e5be16cbfe94fdf7b660f1cd5d7
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2022
ms.locfileid: "9461331"
---
# <a name="use-a-power-automate-flow-for-alerts-to-dataverse-entity-changes"></a>Gebruik een Power Automate-stroom voor waarschuwingen voor Dataverse-entiteitswijzigingen

> [!IMPORTANT]
> Dit artikel beschrijft functionaliteit die beschikbaar komt in releasewave 2 van 2022. Totdat die release beschikbaar is, kunt u een Power Automate-stroom om gewaarschuwd te worden wanneer een entiteit in Dataverse is gewijzigd.

Beheerders kunnen een geautomatiseerde stroom in Power Automate maken die uw [!INCLUDE[prod_short](includes/prod_short.md)] informeert over wijzigingen in records in uw [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-organisatie.

> [!NOTE]
> In dit artikel wordt ervan uitgegaan dat u uw online versie van [!INCLUDE[prod_short](includes/prod_short.md)] met [!INCLUDE [cds_long_md](includes/cds_long_md.md)] hebt verbonden en synchronisatie hebt gepland tussen de twee toepassingen.

## <a name="define-the-flow-trigger"></a>De stroomtrigger definiëren

1. Meld u aan bij [Power Automate](https://flow.microsoft.com).
2. Maak een geautomatiseerde cloudstroom die begint wanneer een rij voor een [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-entiteit wordt toegevoegd, gewijzigd of verwijderd. Voor meer informatie zie [Stromen activeren wanneer een rij wordt toegevoegd, gewijzigd of verwijderd](/power-automate/dataverse/create-update-delete-trigger). Dit voorbeeld gebruikt de entiteit **Rekeningen**. De volgende afbeelding toont de instellingen voor de eerste stap bij het definiëren van een stroomtrigger.

:::image type="content" source="media/power-automate-flow-dataverse-trigger.png" alt-text="Instellingen voor de stroomtrigger":::

3. Gebruik de knop **AssistEdit (...)** in de rechterbovenhoek om de verbinding toe te voegen aan uw [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-omgeving.
4. Kies **Geavanceerde weergeven** en voer in het veld **Rijen filteren** **customertypecode eq 3** of **customertypecode eq 11** en **statecode eq 0** in. Deze waarden betekenen dat de trigger alleen reageert wanneer er wijzigingen worden aangebracht in actieve accounts van het type **klant** of **leverancier**.

## <a name="define-the-flow-condition"></a>De stroomvoorwaarde definiëren

Gegevens worden gesynchroniseerd tussen [!INCLUDE[prod_short](includes/prod_short.md)] en [!INCLUDE [cds_long_md](includes/cds_long_md.md)] via een integratiegebruikersaccount. Als u de wijzigingen die door de synchronisatie zijn aangebracht, wilt negeren, maakt u een voorwaardestap in uw stroom die wijzigingen uitsluit die zijn aangebracht door het integratiegebruikersaccount.  

1. Voeg een **Een rij ophalen uit Dataverse**-stap na de stroomtrigger toe met de volgende instellingen. Zie voor meer informatie [Een rij ophalen uit Dataverse op id](/power-automate/dataverse/get-row-id).
    1. Kies in het veld **Tabelnaam** de optie **Gebruikers**
    2. Kies in het veld **Rij-id** de **Gewijzigd door (waarde)** van de stroomtrigger.  
2. Voeg een voorwaardestap toe met de volgende **of**-instellingen om het integratiegebruikersaccount te identificeren.
    1. Het **Primaire e-mailadres** van de gebruiker bevat **contoso.com** 
    2. De **Volledige naam** van de gebruiker bevat **[!INCLUDE[prod_short](includes/prod_short.md)]**. 
3. Voeg een beëindigingsbesturingselement toe om de stroom te stoppen als aan de voorwaarde wordt voldaan. Dat wil zeggen: als aan de voorwaarde is voldaan en een entiteit is gewijzigd door het integratiegebruikersaccount.

De volgende afbeelding toont de informatie die moet worden toegevoegd om de stroomtrigger en de stroomvoorwaarde te definiëren.

:::image type="content" source="media/power-automate-flow-dataverse.png" alt-text="Overzicht van stroomtrigger- en voorwaarde-instellingen":::

## <a name="notify-business-central-about-a-change"></a>Business Central op de hoogte stellen van een wijziging

Als de stroom niet wordt gestopt door de voorwaarde, moet u aan [!INCLUDE[prod_short](includes/prod_short.md)] doorgeven dat er een verandering heeft plaatsgevonden. Gebruik daarvoor de [!INCLUDE[prod_short](includes/prod_short.md)]-connector

1. Voeg in de **Nee**-vork van de voorwaardestap een actie toe en zoek naar **Dynamics 365 [!INCLUDE[prod_short](includes/prod_short.md)]**. Kies het connectorpictogram in de lijst. 
2. Kies de actie **Record maken (V3)**.

:::image type="content" source="media/power-automate-flow-dataverse-connector.png" alt-text="Instellingen vragen voor de [!INCLUDE[prod_short](includes/prod_short.md)]-connector":::

3. Gebruik de knop **AssistEdit (...)** in de rechterbovenhoek om de verbinding toe te voegen aan uw [!INCLUDE[prod_short](includes/prod_short.md)]-omgeving.
4. Vul wanneer u verbonden bent de velden **Omgevingsnaam** en **Bedrijfsnaam** in.
5. Voer in het veld **API-categorie** **Microsoft/dataverse/v1.0** in.
6. Voer in het veld **Tabelnaam** **dataverseEntityChanges** in.
7. Voer in het veld **entityName** **account** in.
8. Sla de stroom op.

De stroom zou eruit moeten zien als de volgende afbeelding.

:::image type="content" source="media/power-automate-flow-dataverse-summary.png" alt-text="Overzicht van alle instellingen voor de stroom":::

Wanneer u een account toevoegt, verwijdert of wijzigt in uw [!INCLUDE [cds_long_md](includes/cds_long_md.md)]-omgeving, voert deze stroom de volgende acties uit:

1. Roep de [!INCLUDE[prod_short](includes/prod_short.md)]-omgeving aan die u hebt opgegeven in de [!INCLUDE[prod_short](includes/prod_short.md)]-connector. 
2. Gebruik de [!INCLUDE[prod_short](includes/prod_short.md)] API om een record in te voegen met de **Entiteitsnaam** ingesteld op **account** in de tabel **Wijziging van Dataverse-invoer**. 3. [!INCLUDE[prod_short](includes/prod_short.md)] start het taakwachtrij-item dat klanten synchroniseert met accounts.

## <a name="see-also"></a>Zie ook

[Business Central gebruiken in Power Automate-stromen](across-how-use-financials-data-source-flow.md)  
[Geautomatiseerde werkstromen instellen](/business-central/dev-itpro/powerplatform/automate-workflows)  
[Integreren met Microsoft Dataverse](admin-common-data-service.md)  
[Gegevens synchroniseren in Business Central met Microsoft Dataverse](admin-synchronizing-business-central-and-sales.md)  
