---
title: Een sandboxomgeving maken | Microsoft Docs
description: Maak een omgeving waarin u kunt ontdekken, leren, demonstreren, ontwikkelen en testen.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 10/01/2020
ms.author: solsen
ms.openlocfilehash: 1e559f5805504ead36ca3c96b4f2d54d4ce0eb39
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384711"
---
# <a name="creating-a-sandbox-environment-in-prod_short"></a>Een sandboxomgeving maken in [!INCLUDE[prod_short](includes/prod_short.md)]

Met [!INCLUDE[prod_short](includes/prod_short.md)] kunt u eenvoudig een veilige omgeving creëren waar u kunt testen, trainen of problemen oplossen zonder de werkprocessen of bedrijfsgegevens van uw bedrijf te verstoren. Een dergelijke niet-productieomgeving wordt een *sandbox* genoemd. Geïsoleerd van de productieomgeving is een sandboxomgeving de plaats om de service te ontdekken, te leren kennen, te demonstreren, te ontwikkelen en te testen, zonder het risico te lopen dat de gegevens en instellingen van uw productieomgeving worden beïnvloed.  

Uw beheerder kan sandbox-omgevingen maken in het [beheercentrum](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), maar als u snel iets wilt testen, kunt u een sandbox-omgeving maken vanuit [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]
> Technisch gezien zijn sandbox-omgevingen heel anders dan productieomgevingen, zelfs als uw beheerder een sandbox maakt die productiegegevens bevat. U kunt geen sandbox gebruiken voor benchmarking en u kunt bijvoorbeeld geen database-export aanvragen. Als u een sandbox voor benchmarking wilt maken, kan uw beheerder een speciale productieomgeving maken in het beheercentrum. Zie [Typen omgevingen](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#types-of-environments) voor meer informatie.

## <a name="to-create-a-sandbox-environment-in-your-prod_short"></a>Een sandboxomgeving maken in uw [!INCLUDE[prod_short](includes/prod_short.md)]

1. Meld u aan bij uw productie-exemplaar van [!INCLUDE[prod_short](includes/prod_short.md)].

2. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Sandboxomgeving** in en kies de gerelateerde koppeling.
    <!-- ![Sandbox Environment Setup](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Kies de knop **Maken**.  

    Er wordt een ander tabblad met [!INCLUDE[prod_short](includes/prod_short.md)] geopend, waar u de installatie van uw sandbox-omgeving kunt voltooien.

    > [!NOTE]  
    >  Als u pop-upblokkering hebt ingeschakeld in uw browser, wijzigt u deze om URL's van het adres *.businesscentral.dynamics.com toe te staan.

Wanneer de sandboxomgeving gereed is, wordt u omgeleid naar de welkomstwizard van de sandboxomgeving.
<!-- ![Sandbox Welcome Wizard](./media/across-sandbox/sandbox-wizard.png) -->

U kunt de knop **Meer informatie** kiezen om te lezen over ontwikkelaarsscenario's die u in een sandboxomgeving kunt proberen of kies de knop **Sluiten** om door te gaan naar het rolcentrum van uw [!INCLUDE[prod_short](includes/prod_short.md)]-sandboxexemplaar.

Boven in het rolcentrum verschijnt een bericht om u te laten weten dat dit een sandboxomgeving is. Ook in de titelbalk van de client wordt de soort omgeving weergegeven.
    <!-- ![Sandbox RoleCenter Notification](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> Een sandbox-omgeving die op deze manier is gemaakt, bevat alleen de standaarddemonstratiegegevens voor het CRONUS-bedrijf. Er worden geen gegevens gekopieerd of anderszins overgedragen vanuit de productieomgeving.<br /><br />
> U kunt ook een sandbox-omgeving maken met de productiegegevens. U moet dit doen via het beheercentrum. Zie voor meer informatie [Omgevingen beheren](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) in de Ontwikkelaar en IT Pro Help.  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

Een beheerder kan voor sommige gebruikers de toegang tot de sandboxomgeving beperken of zelfs blokkeren. Dit kunt u doen met de standaardbeveiligingsfuncties van het product, zoals de gebruikerskaart, gebruikersgroepen en machtigingensets. Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie.  

<!-- ![Sandbox Permission Sets](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Geavanceerde functionaliteit in de sandboxomgeving

De sandboxomgeving is niet alleen nuttig omdat deze een aantal handige functies bevat.

### <a name="to-enable-the-advanced-user-experience"></a>De geavanceerde gebruikerservaring inschakelen

Het is mogelijk de volledige functionaliteit van de standaardversie van [!INCLUDE[prod_short](includes/prod_short.md)] in een sandboxtenant in te schakelen en uit te proberen door het veld **Ervaring** op de pagina **Bedrijfsgegevens** in te stellen op *Premium*. Zoek de pagina **Bedrijfsgegevens** in het menu van het :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="pictogram Instellingen":::.  

Nadat u de *Premium*-gebruikerservaring hebt ingeschakeld, krijgt u toegang tot alle standaardprofielen (rollen) en Rolcentra in de standaardversie. U kunt ook een evaluatiebedrijf maken dat volledig is ingesteld, inclusief demonstratiegegevens en toegang tot de geavanceerde gebieden van het product. U kunt ook contact opnemen met een wederverkoper voor een demonstratie van de mogelijkheden. Zie [Hoe vind ik een partner-reseller?](across-faq.md#findpartner) voor meer informatie.  

### <a name="to-enable-complete-sample-data"></a>Volledige voorbeeldgegevens inschakelen

In de sandboxomgeving kunt u ook een nieuw bedrijf maken met de optie **Geavanceerde evaluatie - volledige voorbeeldgegevens**, zodat u training kunt volgen of procedures kunt doorlopen waarvoor aanvullende voorbeeldgegevens nodig zijn, zoals [Procedure: Ontvangen en opslaan in basismagazijnconfiguraties](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).  

#### <a name="to-create-a-company-with-complete-sample-data-in-a-sandbox"></a>Een bedrijf maken met volledige voorbeeldgegevens in een sandbox

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bedrijven** in en kies de gerelateerde koppeling.  
2. Kies de actie **Nieuw** en kies vervolgens **Nieuw bedrijf maken**.  
3. Kies op de pagina **Begeleide instelling voor het maken van een bedrijf** **Volgende**.  
4. Geef een naam op voor het nieuwe bedrijf en kies vervolgens in het veld **Selecteer de gegevens en de instelling om aan de slag te gaan** **Geavanceerde evaluatie - volledige voorbeeldgegevens**.  
5. Voer de rest van de begeleide instelling uit.  

Wanneer de begeleide instelling is voltooid, kunt u beginnen met het verkennen van het nieuwe bedrijf met de volledige voorbeeldgegevens. Zie [Nieuwe bedrijven maken in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md) voor meer informatie.  

### <a name="designer"></a>Ontwerper

In een sandboxomgeving is de **Ontwerper** ingeschakeld. U kunt de Ontwerper activeren door het ontwerppictogram ![Ontwerper](./media/across-sandbox/sandbox-inclient-design-icon.png) te selecteren op een pagina of door de menuoptie **Ontwerp** te kiezen in het menu ![Instellingen](media/ui-experience/settings_icon_small.png).

<!-- ![In-client Designer](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-also"></a>Zie ook

[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_long](includes/prod_long.md)]-proefversies en -abonnementen](across-preview.md)  
[Omgevingen beheren in het Business Central-beheercentrum](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  


[!INCLUDE[footer-include](includes/footer-banner.md)]