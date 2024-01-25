---
title: Gebruik uw gegevens om een app te maken| Microsoft Docs
description: U kunt uw Business Central-gegevens als gegevensbron beschikbaar maken en een OData-URL van uw webservices opgeven om een bedrijfsapp te maken met Power Apps.
author: jswymer
ms.topic: conceptual
ms.service: dynamics-365-business-central
ms.search.keywords: 'OData, Power App, SOAP'
ms.date: 05/15/2023
ms.author: jswymer
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a>Verbinding met uw Business Central-gegevens maken om een bedrijfsapp te maken met Power Apps

U kunt uw [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens als gegevensbron beschikbaar maken in Power Apps.  

> [!TIP]  
> Business Central biedt nu ontwikkelings- en operationele ondersteuning voor Power Platform in AL-Go en voorbeelden om u op weg te helpen uw eigen apps te maken Power Apps. Deze functies zijn momenteel in preview. Ga voor meer informatie naar [Business Central en Power Apps](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-overview) in de Help voor ontwikkelaars en IT-professionals.

## <a name="prerequisites"></a>Vereisten

U moet een geldig account bij [!INCLUDE[prod_short](includes/prod_short.md)] en Power Apps hebben.  

## <a name="add--as-a-data-source-in-power-apps"></a>[!INCLUDE[prod_short](includes/prod_short.md)] als gegevensbron toevoegen in Power Apps

Deze stappen voegen een Business Central-tabel toe, zoals klanten of artikelen, als de gegevensbron van een Power Apps-app.

1. Ga in de browser naar [powerapps.microsoft.com](https://powerapps.microsoft.com/) en meld u aan.
2. Selecteer **+ Maken** in het navigatievenster aan de linkerkant en selecteer vervolgens **Meer gegevensbronnen** op de pagina **App maken**.
  
   <!-- This step opens Power Apps canavs. On first sign-in, you must specify the country/region.  -->
3. De lijst **Verbindingen** toont alle bestaande gegevensverbindingen die u hebt.

   - Als er al een **Business Central**-verbinding is, selecteert u deze en selecteert u vervolgens **Maken**.

   - Als u geen Business Central-verbinding ziet, selecteert u **+ Nieuwe verbinding**, zoekt en selecteert u **Business Central** en selecteert u vervolgens **Maken**.

   > [!NOTE]
   > Als u verbinding wilt maken met [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, moet u de connector **Business Central (on-premises)** kiezen.  
  
4. Power Apps maakt verbinding met uw [!INCLUDE[prod_short](includes/prod_short.md)]. Meld u aan met de naam en het wachtwoord van het Business Central-account. Als u geen beheerder hebt van uw [!INCLUDE[prod_short](includes/prod_short.md)], kunt u zich met een ander account aanmelden.  
5. Zodra u bent aangemeld, geeft Power Apps een lijst weer met *omgevingen en bedrijven* die beschikbaar zijn in [!INCLUDE[prod_short](includes/prod_short.md)]. Kies de omgeving en het bedrijf met de gegevens waarmee u verbinding wilt maken, bijvoorbeeld *PRODUCTIE - Mijn bedrijf*.  
6. Vervolgens krijgt u een lijst met tabellen te zien die worden weergegeven als onderdeel van de API voor uw omgeving. Selecteer de tabel waarmee u verbinding wilt maken en kies vervolgens **Verbinden**.

Deze zogenaamde tabellen worden door de [!INCLUDE[prod_short](includes/prod_short.md)]-connector voor Power Apps als eindpunten beschikbaar gemaakt.  

> [!NOTE]
> Als u gegevens uit andere tabellen in [!INCLUDE[prod_short](includes/prod_short.md)] in uw app wilt opnemen, moet u met een ontwikkelaar werken om een aangepaste API te definiëren in [!INCLUDE[prod_short](includes/prod_short.md)].  

Nu hebt u met succes een koppeling gemaakt naar uw [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens en kunt u uw Power App gaan maken. U kunt altijd meer schermen toevoegen en verbinding met meer gegevens maken. Ga voor meer informatie naar [Een canvas-app maken vanuit een voorbeeld in Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

Wanneer u de app hebt ontworpen en gemaakt, u deze met uw collega's delen. Zie voor meer informatie [Een canvasapp opslaan en publiceren in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

<!--
## <a name="sample-apps-to-get-started"></a>Sample apps to get started

As a preview version, Business Central offers several sample apps that you can use as a starting point for building your own apps that use Business Central data. These sample apps are available in the [Business Central Demos](https://github.com/BusinessCentralDemos) repo on GitHub. For a quick overview on the apps, go to [Power Apps samples for Business Central](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-samples).

## <a name="develop-and-maintain-apps-application-lifecycle-management"></a>Develop and maintain apps application lifecycle management

As an app developer, you may already be familiar with Business Central AL-Go. AL-Go is set of tools on GiHub that enables you to maintain professional DevOps processes for your Business Central AL projects. AL-Go supports source control and activities, like building, testing, and deploying. As a preview, Business Central now offers an Al-Go version that supports for Power Platform solutions. The preview, for example, includes workflows that let you push and pull Power Platfrom changes to and from enviroments. You can access the tools at [https://github.com/BusinessCentralDemos/AL-Go-PTE](https://github.com/BusinessCentralDemos/AL-Go-PTE). For more information, see [Application lifecycle management for Power Apps in Business Central](/dynamics365/business-central/dev-itpro/powerplatform/power-apps-alm).-->

## <a name="see-also"></a>Zie ook

[Een canvasapp maken vanuit een sjabloon in Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Instellen van [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Aan de slag met het ontwikkelen van verbindingsapps voor Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
