---
title: Gebruik uw gegevens om een app te maken| Microsoft Docs
description: U kunt uw Business Central-gegevens als gegevensbron beschikbaar maken en een OData-URL van uw webservices opgeven om een bedrijfsapp te maken met Power Apps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: OData, Power App, SOAP
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: f6b771b0107214702785d2b124983eb369741a84
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187928"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-power-apps"></a>Verbinding met uw Business Central-gegevens maken om een bedrijfsapp te maken met Power Apps

U kunt uw [!INCLUDE[prodshort](includes/prodshort.md)]-gegevens als gegevensbron beschikbaar maken in Power Apps.  

> [!NOTE]  
> U moet een geldig account bij [!INCLUDE[prodshort](includes/prodshort.md)] en Power Apps hebben.  

## <a name="to-add-prodshort-as-a-data-source-in-power-apps"></a>[!INCLUDE[prodshort](includes/prodshort.md)] als gegevensbron toevoegen in Power Apps

1. Navigeer in de browser naar [powerapps.microsoft.com](https://powerapps.microsoft.com/) en meld u aan.
2. Kies op de startpagina **Apps**, **Een app maken** en **Canvas** om een nieuwe canvas-app te maken. Deze app wordt ontworpen voor gebruik op een mobiel apparaat, maar u kunt ook een andere sjabloon gebruiken.

    De volgende stap om een Power App te maken bestaat eruit uw gegevens te selecteren. Kies het pijlpictogram en kies vervolgens de optie **Nieuwe verbinding** linksboven in de pagina.
3. Kies in de lijst met beschikbare verbindingen **Business Central** en kies de knop **Maken**.

    Power Apps maakt verbinding met uw [!INCLUDE [prodshort](includes/prodshort.md)] met behulp van de aanmeldingsgegevens waarmee u bent aangemeld. Als u geen beheerder hebt van uw [!INCLUDE [prodshort](includes/prodshort.md)], kunt u zich met een ander account aanmelden.  

4. Met Power Apps wordt een lijst met *omgevingen en bedrijven* weergegeven die beschikbaar zijn in [!INCLUDE [prodshort](includes/prodshort.md)]. Kies de omgeving en het bedrijf met de gegevens waarmee u verbinding wilt maken. Vervolgens krijgt u een lijst met API's te zien. Selecteer de **API** waarmee u verbinding wilt maken.

Deze zogenaamde tabellen maken deel uit van de [!INCLUDE [prodshort](includes/prodshort.md)] API. U hoeft de eindpunten niet zelf te configureren. De [!INCLUDE [prodshort](includes/prodshort.md)]-connector voor Power Apps doet dat voor u.  

> [!NOTE]
> Als u gegevens uit andere tabellen in [!INCLUDE [prodshort](includes/prodshort.md)] in uw app wilt opnemen, moet u met een ontwikkelaar werken om een aangepaste API te maken in [!INCLUDE [prodshort](includes/prodshort.md)] en vervolgens die aangepaste API gebruiken via een aangepaste connector in Power Apps. Zie voor meer informatie [Een nieuwe aangepaste connector maken](/connectors/custom-connectors/define-blank).  

Nu hebt u met succes een koppeling gemaakt naar uw [!INCLUDE [prodshort](includes/prodshort.md)]-gegevens en kunt u uw PowerApp gaan maken. U kunt extra schermen toevoegen en verbinding met extra gegevens maken vanuit uw [!INCLUDE [prodshort](includes/prodshort.md)]. Zie voor meer informatie [Een canvasapp maken vanuit een sjabloon in Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive).  

Wanneer u de app hebt ontworpen en gemaakt, u deze met uw collega's delen. Zie voor meer informatie [Een canvasapp opslaan en publiceren in Power Apps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Als u verbinding wilt maken met [!INCLUDE [prodshort](includes/prodshort.md)] on-premises, moet u de connector **Business Central (on-premises)** kiezen in stap 3.  

## <a name="see-also"></a>Zie ook

[Een canvasapp maken vanuit een sjabloon in Power Apps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Aan de slag](product-get-started.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Financiën](finance.md)  
[Aan de slag met het ontwikkelen van verbindingsapps voor Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
