---
title: Een sandboxomgeving maken
description: Maak een sandboxomgeving voor verkennen, leren, demonstreren, ontwikkelen, problemen oplossen en testen vanuit Business Central.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 06/08/2021
ms.author: solsen
ms.openlocfilehash: 2f4ca6a98aac49fa5fea7d8658ef51a9510c97d7
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6437689"
---
# <a name="creating-a-sandbox-environment-in-prod_short"></a>Een sandboxomgeving maken in [!INCLUDE[prod_short](includes/prod_short.md)]

Met [!INCLUDE[prod_short](includes/prod_short.md)] kunt u eenvoudig een veilige omgeving creëren waar u kunt testen, trainen of problemen oplossen zonder de werkprocessen of bedrijfsgegevens van uw bedrijf te verstoren. Een dergelijke niet-productieomgeving wordt een *sandbox* genoemd. Geïsoleerd van de productieomgeving is een sandboxomgeving de plaats om de service te ontdekken, te leren kennen, te demonstreren, te ontwikkelen en te testen, zonder het risico te lopen dat de gegevens en instellingen van uw productieomgeving worden beïnvloed.  

Uw beheerder beheert sandboxomgevingen in het [beheercentrum](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json), maar als u snel iets wilt testen, kunt u een sandboxomgeving maken vanuit [!INCLUDE[prod_short](includes/prod_short.md)]. Als u klaar bent, kunt u de sandbox verwijderen met behulp van het beheercentrum.  

> [!NOTE]
> Technisch gezien zijn sandbox-omgevingen heel anders dan productieomgevingen, zelfs als uw beheerder een sandbox maakt die productiegegevens bevat. U kunt geen sandbox gebruiken voor benchmarking en u kunt bijvoorbeeld geen database-export aanvragen. Als uw beheerder een sandbox voor benchmarking wilt maken, kan hij of zij een speciale omgeving maken in het beheercentrum. Zie voor meer informatie [Productie- en sandbox-omgevingen](/dynamics365/business-central/dev-itpro/administration/environment-types).

## <a name="to-create-a-sandbox-environment-in-your-prod_short"></a>Een sandboxomgeving maken in uw [!INCLUDE[prod_short](includes/prod_short.md)]

1. Meld u aan bij uw productie-exemplaar van [!INCLUDE[prod_short](includes/prod_short.md)].

2. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Sandboxomgeving** in en kies vervolgens de gerelateerde koppeling.
    <!-- ![Sandbox Environment Setup.](./media/across-sandbox/sandbox-environment-setup.png) -->
3. Kies de knop **Maken**.  

    Er wordt een ander tabblad met [!INCLUDE[prod_short](includes/prod_short.md)] geopend, waar u de installatie van uw sandbox-omgeving kunt voltooien.

    > [!NOTE]  
    >  Als u pop-upblokkering hebt ingeschakeld in uw browser, wijzigt u deze om URL's van het adres *.businesscentral.dynamics.com toe te staan.

Wanneer de sandboxomgeving gereed is, wordt u omgeleid naar de welkomstwizard van de sandboxomgeving.
<!-- ![Sandbox Welcome Wizard.](./media/across-sandbox/sandbox-wizard.png) -->

U kunt de knop **Meer informatie** kiezen om te lezen over ontwikkelaarsscenario's die u in een sandboxomgeving kunt proberen of kies de knop **Sluiten** om door te gaan naar het rolcentrum van uw [!INCLUDE[prod_short](includes/prod_short.md)]-sandboxexemplaar.

Boven in het rolcentrum verschijnt een bericht om u te laten weten dat dit een sandboxomgeving is. Ook in de titelbalk van de client wordt de soort omgeving weergegeven.
    <!-- ![Sandbox RoleCenter Notification.](./media/across-sandbox/sandbox-rolecenter-notification.png) -->

> [!NOTE]
> Een sandbox-omgeving die op deze manier is gemaakt, bevat alleen de standaarddemonstratiegegevens voor het CRONUS-bedrijf. Er worden geen gegevens gekopieerd of anderszins overgedragen vanuit de productieomgeving.
>
> U kunt ook een sandbox-omgeving maken op basis van productiegegevens. U moet dit doen via het beheercentrum. Zie voor meer informatie [Omgevingen beheren](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments) in de ontwikkelaar- en beheercontent.  

<!--To switch between your production and sandbox environments, you can use the Business Central app launcher.
    ![Sandbox Dynamics365 Menu.](./media/across-sandbox/sandbox-dynamics365-menu.png) -->

Een beheerder kan voor sommige gebruikers de toegang tot de sandboxomgeving beperken of zelfs blokkeren. Dit kunt u doen met de standaardbeveiligingsfuncties van het product, zoals de gebruikerskaart, gebruikersgroepen en machtigingensets. Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie.  

<!-- ![Sandbox Permission Sets.](./media/across-sandbox/sandbox-permission-sets.png) -->

## <a name="advanced-functionality-in-the-sandbox-environment"></a>Geavanceerde functionaliteit in de sandboxomgeving

De sandboxomgeving is onder andere nuttig omdat deze een aantal handige functies bevat:

* [Geavanceerde gebruikerservaring](#advanced-user-experience)  
* [Volledige voorbeeldgegevens](#complete-sample-data)  
* [Ontwerper](#designer)  

### <a name="advanced-user-experience"></a>Geavanceerde gebruikerservaring

Het is mogelijk de volledige functionaliteit van de standaardversie van [!INCLUDE[prod_short](includes/prod_short.md)] in een sandboxtenant in te schakelen en uit te proberen door het veld **Ervaring** op de pagina **Bedrijfsgegevens** in te stellen op *Premium*. Zoek de pagina **Bedrijfsgegevens** in het menu van het :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="pictogram Instellingen.":::    

Nadat u de *Premium*-gebruikerservaring hebt ingeschakeld, krijgt u toegang tot alle standaardprofielen (rollen) en Rolcentra in de standaardversie. U kunt ook een evaluatiebedrijf maken dat volledig is ingesteld, inclusief demonstratiegegevens en toegang tot de geavanceerde gebieden van het product. U kunt ook contact opnemen met een wederverkoper voor een demonstratie van de mogelijkheden. Zie [Hoe vind ik een partner-reseller?](across-faq.yml#how-do-i-find-a-reselling-partner) voor meer informatie.  

### <a name="complete-sample-data"></a>Volledige voorbeeldgegevens

Neem voor situaties waarin u aanvullende voorbeeldgegevens nodig heeft, contact op met uw wederverkoper.
<!-- In the sandbox environment, you can also create a new company with the **Advanced Evaluation - Complete Sample Data** option so that you can take training or step through walkthroughs that require additional sample data, such as [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).   -->

#### <a name="to-create-a-company-with-complete-sample-data-in-a-sandbox"></a>Een bedrijf maken met volledige voorbeeldgegevens in een sandbox

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Bedrijven** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw** en kies vervolgens **Nieuw bedrijf maken**.  
3. Kies op de pagina **Begeleide instelling voor het maken van een bedrijf** **Volgende**.  
4. Geef een naam op voor het nieuwe bedrijf en kies vervolgens in het veld **Selecteer de gegevens en de instelling om aan de slag te gaan** **Geavanceerde evaluatie - volledige voorbeeldgegevens**.  
5. Voer de rest van de begeleide instelling uit.  

Wanneer de begeleide instelling is voltooid, kunt u beginnen met het verkennen van het nieuwe bedrijf met de volledige voorbeeldgegevens. Zie [Nieuwe bedrijven maken in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md) voor meer informatie.  

### <a name="designer"></a>Ontwerper

In een sandboxomgeving is de **Ontwerper** ingeschakeld. U kunt Designer activeren door het ontwerppictogram te selecteren ![Ontwerper](./media/across-sandbox/sandbox-inclient-design-icon.png) op een pagina of door het menu-item **Ontwerp** te kiezen in het menu ![Instellingen](media/ui-experience/settings_icon_small.png) Instellingen.  

Voor meer informatie zie [Designer gebruiken](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) in de inhoud voor ontwikkelaars en beheerders (alleen in het Engels).  

<!-- ![In-client Designer.](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-also"></a>Zie ook

[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_long](includes/prod_long.md)]-proefversies en -abonnementen](across-preview.md)  
[Omgevingen beheren in het Business Central-beheercentrum](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
