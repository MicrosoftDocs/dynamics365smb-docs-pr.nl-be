---
title: Business Central gebruiken in Power Automate-stromen
description: Stel Power Automate-stromen en gebruik ze die Business Central-gegevens maken of wijzigen.
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, OData, Power App, SOAP, Entity set not found, workflowWebhookSubscriptions
ms.date: 05/12/2022
ms.author: edupont
author: jswymer
ms.openlocfilehash: f1128a9fb4e9643286e4305695e1d40719d86301
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9079336"
---
# <a name="use-prod_short-in-power-automate-flows"></a>[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken in Power Automate-stromen

U kunt uw [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens als onderdeel van een werkstroom in Microsoft Power Automate gebruiken. Creëer uw eigen stromen en maak verbinding met uw gegevens met de [!INCLUDE [prod_short](includes/prod_short.md)]-connector.  

> [!NOTE]  
> U moet een geldig account bij [!INCLUDE[prod_short](includes/prod_short.md)] en Power Automate hebben.  

> [!TIP]
> Naast Power Automate kunt u sjablonen voor goedkeuringswerkstromen gebruiken in [!INCLUDE[prod_short](includes/prod_short.md)]. Hoewel het twee aparte werkstroomsystemen zijn, wordt elke goedkeuringswerkstroomsjabloon die u maakt met Power Automate, toegevoegd aan de lijst met werkstromen in [!INCLUDE[prod_short](includes/prod_short.md)]. Zie [Werkstromen](across-workflow.md) voor meer informatie.  

## <a name="automated-workflows"></a>Geautomatiseerde werkstromen

Met Power Automate kunt u direct in-house bedrijfsstromen creëren en vertrouwen op citizen-ontwikkelaars. Zie voor meer informatie [Geautomatiseerde werkstromen instellen](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) in de beheerinhoud.  

## <a name="manual-instant-flows"></a>Handmatige directe stromen

Vanaf mei 2022 kan een beheerder van [!INCLUDE [prod_short](includes/prod_short.md)] online [een functie inschakelen](admin-feature-management.md) om het mogelijk te maken om een Power Automate-stroom uit te voeren vanuit de meeste pagina's. Zie voor meer informatie [Geautomatiseerde werkstromen instellen](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows) in de beheerinhoud.  

Zodra de beheerder [!INCLUDE [prod_short](includes/prod_short.md)] heeft verbonden met Power Automate, ziet u alle stromen die uw organisatie heeft toegevoegd wanneer u de actie **Automatiseren** kiest op de betreffende pagina's. U voert de stromen uit zonder weg te gaan uit [!INCLUDE [prod_short](includes/prod_short.md)].  

Deze geautomatiseerde werkstromen openen in een deelvenster binnen [!INCLUDE [prod_short](includes/prod_short.md)] online zodat u binnen de context blijft van het bedrijfsproces waar u middenin zat. Op sommige pagina's wordt de actie **Automatiseren** verborgen onder het menu **Meer opties**, maar vind het, kies de menuoptie **Power Automate** en kies vervolgens de relevante koppeling om de werkstroom te activeren. De verbinding met Power Automate is al voor u ingesteld.  

Bij de meeste stromen moet u een of twee velden invullen voordat u de actie **Stroom uitvoeren** kiest.  

> [!TIP]
> Als u geen actie **Automatiseren** ziet, is uw [!INCLUDE [prod_short](includes/prod_short.md)] waarschijnlijk nog niet ingesteld voor gebruik van Power Automate. Neem voor meer informatie contact op met uw beheerder.

## <a name="add-more-automated-flows-and-manual-instant-flows"></a>Meer geautomatiseerde stromen en handmatige directe stromen toevoegen

U kunt stromen maken op de website [powerautomate.microsoft.com](https://powerautomate.microsoft.com). Als uw beheerder echter de mogelijkheid heeft ingeschakeld om Power Automate-stromen uit te voeren vanuit [!INCLUDE [prod_short](includes/prod_short.md)] online, kunt u het proces van het maken van een stroom starten vanuit de actie **Automatiseren** op de betreffende pagina's. Op sommige pagina's wordt de actie **Automatiseren** verborgen onder het menu **Meer opties**, maar vind het, kies de menuoptie **Power Automate** en kies vervolgens de actie **Een stroom maken**. Power Automate wordt vervolgens geopend in een nieuw browsertabblad en u wordt automatisch ingelogd.

## <a name="manage-workflows"></a>Werkstromen beheren

U kunt een overzicht krijgen van alle werkstromen waartoe u toegang hebt door te kiezen voor de actie **Werkstromen beheren** in het menu **Power Automate**. De lijst wordt geopend in een nieuw browsertabblad en u wordt automatisch aangemeld bij Power Automate. Daar kunt u zien wanneer elke stroom voor het laatst is uitgevoerd.  

## <a name="see-related-training-at-microsoft-learn"></a>Zie gerelateerde training op [Microsoft Learn](/learn/modules/use-power-automate/)

## <a name="see-also"></a>Zie ook

[Problemen met uw [!INCLUDE[prod_short](includes/prod_short.md)] geautomatiseerde werkstromen](across-flow-troubleshoot.md) oplossen  
[Zich voorbereiden om zaken te doen](ui-get-ready-business.md)  
[Werkstromen](across-workflow.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]](setup.md) instellen  
[Financiën](finance.md)  
[Geautomatiseerde werkstromen instellen](/dynamics365/business-central/dev-itpro/powerplatform/automate-workflows)  

[!INCLUDE[footer-include](includes/footer-banner.md)]