---
title: Sandboxomgevingen
description: Ontdek hoe een speciale omgeving u kan helpen om Business Central veilig te verkennen, te leren, te demonstreren, te ontwikkelen, problemen op te lossen en te testen.
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.reviewer: edupont
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sandbox, demo, develop
ms.date: 07/27/2021
ms.author: solsen
ms.openlocfilehash: f704afaf8e7c581aa1f8e65bd06e04fd31d0056a
ms.sourcegitcommit: 769d20d299155cba30c35636d02b2ef021e4ecc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/29/2021
ms.locfileid: "6688357"
---
# <a name="sandbox-environments-in-prod_short"></a>Sandboxomgevingen in [!INCLUDE[prod_short](includes/prod_short.md)]

Met [!INCLUDE[prod_short](includes/prod_short.md)] online kunt u eenvoudig een veilige omgeving krijgen waar u kunt testen, trainen of problemen oplossen zonder de werkprocessen of bedrijfsgegevens van uw bedrijf te verstoren. Een dergelijke niet-productieomgeving wordt een *sandbox* genoemd. Geïsoleerd van de productieomgeving is een sandboxomgeving de plaats om de service te ontdekken, te leren kennen, te demonstreren, te ontwikkelen en te testen, zonder het risico te lopen dat de gegevens en instellingen van uw productieomgeving worden beïnvloed.  

Uw beheerder beheert sandboxomgevingen in het [beheercentrum](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments?toc=/dynamics365/business-central/toc.json).  

Als u bijvoorbeeld een sandbox voor benchmarking wilt maken, kan uw beheerder een speciale omgeving maken in het beheercentrum. Zie voor meer informatie [Productie- en sandbox-omgevingen](/dynamics365/business-central/dev-itpro/administration/environment-types) in de ontwikkelaar- en beheercontent.  

U kunt sandboxes ook veilig gebruiken voor training, bijvoorbeeld voor het volgen van een leertraject vanuit [Microsoft Learn](/learn/dynamics365/business-central?WT.mc_id=dyn365bc_landingpage-docs), omdat het een veilige omgeving is om mee te experimenteren. Als er iets misgaat, verwijdert u gewoon de sandbox en begint u opnieuw.  

Als u klaar bent, kunt u de sandbox verwijderen met behulp van het beheercentrum.  

> [!NOTE]
> Technisch gezien zijn sandbox-omgevingen heel anders dan productieomgevingen. Uw beheerder kan een sandbox maken die productiegegevens bevat, maar het blijft een sandbox en u kunt bijvoorbeeld geen database-export aanvragen. Zie voor meer informatie [Sandbox-omgevingen](/dynamics365/business-central/dev-itpro/administration/environment-types#sandbox-environments) in de ontwikkelaar- en beheercontent.

De sandboxomgeving is onder andere nuttig omdat deze een aantal handige functies bevat:

* [Geavanceerde gebruikerservaring](#advanced-user-experience)  
<!--* [Complete sample data](#complete-sample-data)  -->
* [Ontwerper](#designer)  

## <a name="advanced-user-experience"></a>Geavanceerde gebruikerservaring

Het is mogelijk de volledige functionaliteit van de standaardversie van [!INCLUDE[prod_short](includes/prod_short.md)] in een sandboxtenant in te schakelen en uit te proberen door het veld **Ervaring** op de pagina **Bedrijfsgegevens** in te stellen op *Premium*. Zoek de pagina **Bedrijfsgegevens** in het menu van het :::image type="content" source="media/ui-experience/settings_icon_small.png" alt-text="pictogram Instellingen.":::    

Nadat u de *Premium*-gebruikerservaring hebt ingeschakeld, krijgt u toegang tot alle standaardprofielen (rollen) en Rolcentra in de standaardversie. U kunt ook contact opnemen met een wederverkoper voor een demonstratie van de mogelijkheden. Zie [Hoe vind ik een partner-reseller?](across-faq.yml#how-do-i-find-a-reselling-partner) voor meer informatie.  

### <a name="complete-sample-data"></a>Volledige voorbeeldgegevens

Neem voor situaties waarin u aanvullende voorbeeldgegevens nodig heeft, contact op met uw wederverkoper.
<!-- In the sandbox environment, you can also create a new company with the **Advanced Evaluation - Complete Sample Data** option so that you can take training or step through walkthroughs that require additional sample data, such as [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md).   -->

<!--#### To create a company with complete sample data in a sandbox

1. Choose the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Companies**, and then choose the related link.  
2. Choose the **New** action, and then choose **Create New Company**.  
3. In the **Assisted Setup for Creating a Company** page, choose **Next**.  
4. Specify a name for the new company, and then, in the **Select the data and setup to get started** field, choose **Advanced Evaluation - Complete Sample Data**.  
5. Complete the rest of the assisted setup guide.  

When the assisted setup guide completes, you can start exploring the new company with the complete sample data. For more information, see [Creating New Companies in [!INCLUDE[prod_short](includes/prod_short.md)]](about-new-company.md).  -->

## <a name="designer"></a>Ontwerper

In een sandboxomgeving is de **Ontwerper** ingeschakeld. U kunt Designer activeren door het ontwerppictogram te selecteren ![Ontwerper](./media/across-sandbox/sandbox-inclient-design-icon.png) op een pagina of door het menu-item **Ontwerp** te kiezen in het menu ![Instellingen](media/ui-experience/settings_icon_small.png) Instellingen.  

Voor meer informatie zie [Designer gebruiken](/dynamics365/business-central/dev-itpro/developer/devenv-inclient-designer) in de inhoud voor ontwikkelaars en beheerders (alleen in het Engels).  

<!-- ![In-client Designer.](./media/across-sandbox/sandbox-inclient-designer.png) -->

## <a name="see-also"></a>Zie ook

[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[[!INCLUDE[prod_long](includes/prod_long.md)]-proefversies en -abonnementen](across-preview.md)  
[Omgevingen beheren in het Business Central-beheercentrum](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)  
[Productie- en sandbox-omgevingen](/dynamics365/business-central/dev-itpro/administration/environment-types)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
