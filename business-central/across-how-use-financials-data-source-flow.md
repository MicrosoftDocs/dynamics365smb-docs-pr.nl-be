---
title: Power Automate-stromen gebruiken in Business Central
description: Configureer en gebruik Power Automate-stromen om Business Central-gegevens te maken of wijzigen.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Power Automate,
ms.search.form: 1500,
ms.date: 09/13/2022
ms.author: edupont
ms.openlocfilehash: 5fe089c0330a8d2b7a71f4907212665722d27d38
ms.sourcegitcommit: 8ad79e0ec6e625796af298f756a142624f514cf3
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/30/2022
ms.locfileid: "9606534"
---
# <a name="use-power-automate-flows-in-prod_short"></a>Power Automate-stromen gebruiken in [!INCLUDE[prod_short](includes/prod_short.md)]

U kunt uw [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens als onderdeel van een werkstroom in Microsoft Power Automate gebruiken. Maak uw eigen stromen en maak verbinding met uw gegevens uit interne en externe bronnen met de [!INCLUDE [prod_short](includes/prod_short.md)]-connector.

> [!NOTE]
> U moet een geldig account bij zowel [!INCLUDE[prod_short](includes/prod_short.md)] als Power Automate hebben.  

> [!TIP]
> Naast Power Automate kunt u sjablonen voor goedkeuringswerkstromen gebruiken in [!INCLUDE[prod_short](includes/prod_short.md)]. Hoewel het twee aparte werkstroomsystemen zijn, wordt elke goedkeuringswerkstroomsjabloon die u maakt met Power Automate, toegevoegd aan de lijst met werkstromen in [!INCLUDE[prod_short](includes/prod_short.md)]. Zie voor meer informatie [Werkstromen](across-workflow.md).

Power Automate-stromen worden geactiveerd door gebeurtenissen zoals het maken, wijzigen of verwijderen van records en documenten (geautomatiseerde stromen). De stromen kunnen ook worden uitgevoerd volgens een door de gebruiker gedefinieerd schema (geplande stromen) of op aanvraag (directe stromen).

## <a name="power-automate-features-in-prod_short"></a>Power Automate-functies in [!INCLUDE[prod_short](includes/prod_short.md)]

Stromen zijn een uitbreiding op de ingebouwde functies voor goedkeuringswerkstromen die beschikbaar zijn in [!INCLUDE[prod_short](includes/prod_short.md)] zonder codeerkennis te vereisen, en kunnen worden geassocieerd met een breed scala aan gebeurtenissen en reacties, zoals recordwijzigingen, updates van externe bestanden, geboekte documenten, en verschillende services van Microsoft en derden, zoals Microsoft Outlook, Microsoft Excel, Microsoft Dataverse, Microsoft Teams, Microsoft SharePoint, Microsoft Power Apps en meer.

Een nieuwe verkoopfactuur kan bijvoorbeeld een werkstroom activeren voor een goedkeuringsverzoek, waarvoor verschillende gebeurtenissen kunnen worden ingesteld, afhankelijk van het antwoord van de fiatteur. Een negatieve reactie stuurt een bericht en e-mail naar de aanvrager van de goedkeuring. Een positieve reactie werkt tegelijkertijd een Excel-spreadsheet bij die zich in een SharePoint bevindt en stuurt een update naar een Teams-chat.

Directe stromen werken op dezelfde manier als batchsnelkoppelingen, waarbij meerdere lange stappen worden uitgevoerd met een paar drukken op een knop en worden gestart vanaf specifieke pagina's of tabellen. Een stroom kan bijvoorbeeld een knop toevoegen aan het actiemenu op de pagina **Leveranciers** om betalingen aan een leverancier te blokkeren en tegelijkertijd aanpasbare e-mails te verzenden naar de contactpersoon van de leverancier en de inkopers van uw bedrijf, en om het contact in Outlook bij te werken.

## <a name="automated-workflows"></a>Geautomatiseerde werkstromen

Met Power Automate kunt u direct in-house bedrijfsstromen creëren en vertrouwen op citizen-ontwikkelaars. Geautomatiseerde werkstromen kunnen worden gestart door zowel interne als externe gebeurtenissen in [!INCLUDE[prod_short](includes/prod_short.md)], en kunnen ook worden ingesteld om periodiek te worden uitgevoerd. Lees meer en krijg instructies over het maken van werkstromen in het artikel [Geautomatiseerde werkstromen instellen](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) in de beheerdersinhoud.

## <a name="instant-flows"></a>Directe stromen

Met [!INCLUDE [prod_short](includes/prod_short.md)] kan een Power Automate-stroom worden uitgevoerd via de meeste lijst-, kaart- en documentpagina's. Zodra de beheerder [!INCLUDE [prod_short](includes/prod_short.md)] heeft verbonden met Power Automate, ziet u alle stromen die uw organisatie heeft toegevoegd wanneer u de actie **Automatiseren** kiest op de betreffende pagina's. Directe stromen worden uitgevoerd zonder [!INCLUDE [prod_short](includes/prod_short.md)] te verlaten. Zie voor meer informatie het artikel [Geautomatiseerde werkstromen instellen](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) in de beheerinhoud.

Deze directe werkstromen worden geopend op een pagina binnen [!INCLUDE [prod_short](includes/prod_short.md)] online, zodat u binnen de context kunt blijven van het bedrijfsproces waar u middenin zat. Kies de actie **Automatiseren** (op sommige pagina's genest in het menu **Meer opties**), kies de menuoptie **Power Automate** en kies vervolgens de relevante koppeling om de werkstroom te activeren. De verbinding met Power Automate is al voor u ingesteld.

Bij de meeste stromen moet u een of twee velden invullen voordat u de actie **Stroom uitvoeren** kiest.

> [!TIP]
> Als u geen actie **Automatiseren** ziet, is uw [!INCLUDE [prod_short](includes/prod_short.md)] waarschijnlijk nog niet ingesteld voor gebruik van Power Automate. Meer informatie van uw beheerder.

## <a name="add-more-automated-flows-and-instant-flows"></a>Meer geautomatiseerde stromen en directe stromen toevoegen

U kunt stromen maken op de website [powerautomate.microsoft.com](https://powerautomate.microsoft.com). Als uw beheerder echter de mogelijkheid heeft ingeschakeld om Power Automate-stromen uit te voeren vanuit [!INCLUDE [prod_short](includes/prod_short.md)] online, kunt u het proces van het bouwen van een stroom starten vanuit de actie **Automatiseren** op de betreffende pagina's, die te vinden is in het menu **Meer opties**, afhankelijk van de pagina. Kies dan de menuoptie **Power Automate** en kies vervolgens de actie **Een stroom maken**. Power Automate wordt vervolgens geopend in een nieuw browsertabblad en u wordt automatisch ingelogd.

U kunt voorbeeldsjablonen vinden om aan te passen aan uw bedrijf en alle beschikbare triggergebeurtenissen, met behulp van zowel [!INCLUDE [prod_short](includes/prod_short.md)] als externe tools, door het menu **Connectors** te kiezen op de Power Automate-website. Lees meer over beschikbare sjablonen en triggers in het artikel [Geautomatiseerde werkstromen instellen](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) in de beheerdersinhoud.

## <a name="manage-automated-workflows"></a>Geautomatiseerde werkstromen beheren

U kunt nieuwe stromen maken of bestaande Power Automate-stromen beheren in [!INCLUDE [prod_short](includes/prod_short.md)], op de pagina **Power Automate-stromen beheren**. Zie voor meer informatie het artikel [Power Automate-stromen beheren](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows) in de beheerinhoud.

U kunt ook beschikbare Power Automate-werkstromen beheren op de pagina **Werkstromen** in [!INCLUDE[prod_short](includes/prod_short.md)]. De pagina vermeldt zowel ingebouwde goedkeuring als Power Automate-werkstromen, met opties voor de laatste om de werkstroom in/uit te schakelen, te verwijderen en te bekijken op de Power Automate-website.

## <a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/modules/use-power-automate/)

## <a name="see-also"></a>Zie ook

[Problemen met uw [!INCLUDE[prod_short](includes/prod_short.md)] geautomatiseerde werkstromen](across-flow-troubleshoot.md) oplossen  
[Zich voorbereiden om zaken te doen](ui-get-ready-business.md)  
[Werkstromen](across-workflow.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]](setup.md) instellen  
[Financiën](finance.md)  
[Power Automate-stromen beheren](/dynamics365/business-central/dev-itpro/powerplatform/manage-power-automate-flows)  
[Geautomatiseerde werkstromen instellen](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  
[Directe stromen inschakelen](/dynamics365/business-central/dev-itpro/powerplatform/instant-flows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
