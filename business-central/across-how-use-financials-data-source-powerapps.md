---
title: Gebruik uw gegevens om een app te maken| Microsoft Docs
description: U kunt uw Business Central-gegevens als gegevensbron beschikbaar maken en een OData-URL van uw webservices opgeven om een bedrijfsapp te maken met Power Apps.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'OData, Power App, SOAP'
ms.date: 04/01/2021
ms.author: edupont
---
# Verbinding met uw Business Central-gegevens maken om een bedrijfsapp te maken met Power Apps

U kunt uw [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens als gegevensbron beschikbaar maken in Power Apps.  

> [!NOTE]  
> U moet een geldig account bij [!INCLUDE[prod_short](includes/prod_short.md)] en Power Apps hebben.  

## [!INCLUDE[prod_short](includes/prod_short.md)] als gegevensbron toevoegen in Power Apps

1. Navigeer in de browser naar [powerapps.microsoft.com](https://powerapps.microsoft.com/) en meld u aan.
2. Kies op de startpagina in de sectie **Start vanuit gegevens** de tegel **Andere gegevensbronnen**.  

    Dit opent Power Apps Studio. Bij de eerste aanmelding moet u het land/regio specificeren.  
3. Kies in de lijst met beschikbare verbindingen **Business Central** en kies de knop **Maken**.

    Power Apps maakt verbinding met uw [!INCLUDE[prod_short](includes/prod_short.md)] met behulp van de aanmeldingsgegevens waarmee u bent aangemeld. Als u geen beheerder hebt van uw [!INCLUDE[prod_short](includes/prod_short.md)], kunt u zich met een ander account aanmelden.  

4. Met Power Apps wordt een lijst met *omgevingen en bedrijven* weergegeven die beschikbaar zijn in [!INCLUDE[prod_short](includes/prod_short.md)]. Kies de omgeving en het bedrijf met de gegevens waarmee u verbinding wilt maken, bijvoorbeeld *PRODUCTIE - Mijn bedrijf*.  

5. Vervolgens krijgt u een lijst met tabellen te zien die worden weergegeven als onderdeel van de API voor uw omgeving. Selecteer de tabel waarmee u verbinding wilt maken en kies vervolgens **Verbinden**.

Deze zogenaamde tabellen worden door de [!INCLUDE[prod_short](includes/prod_short.md)]-connector voor Power Apps als eindpunten beschikbaar gemaakt.  

> [!NOTE]
> Als u gegevens uit andere tabellen in [!INCLUDE[prod_short](includes/prod_short.md)] in uw app wilt opnemen, moet u met een ontwikkelaar werken om een aangepaste API te maken in [!INCLUDE[prod_short](includes/prod_short.md)] en vervolgens die aangepaste API gebruiken via een aangepaste connector in Power Apps. Zie voor meer informatie [Een nieuwe aangepaste connector maken](/connectors/custom-connectors/define-blank).  

Nu hebt u met succes een koppeling gemaakt naar uw [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens en kunt u uw PowerApp gaan maken. U kunt extra schermen toevoegen en verbinding met extra gegevens maken vanuit uw [!INCLUDE[prod_short](includes/prod_short.md)]. Zie voor meer informatie [Een canvasapp maken vanuit een voorbeeld in Power Apps](/powerapps/maker/canvas-apps/open-and-run-a-sample-app).  

Wanneer u de app hebt ontworpen en gemaakt, u deze met uw collega's delen. Zie voor meer informatie [Een canvasapp opslaan en publiceren in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Als u verbinding wilt maken met [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, moet u de connector **Business Central (on-premises)** kiezen in stap 3.  

## Zie gerelateerde [Microsoft-training](/training/paths/power-apps-power-automate-business-central/)

## Zie ook

[Een canvasapp maken vanuit een sjabloon in Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Instellen van [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Aan de slag met het ontwikkelen van verbindingsapps voor Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
