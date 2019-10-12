---
title: Gebruik uw gegevens om een app te maken| Microsoft Docs
description: U kunt uw Business Central-gegevens als gegevensbron beschikbaar maken en een OData-URL van uw webservices opgeven om een bedrijfsapp te maken met PowerApps.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 4b8005154afb988cf25c6a04b7beeaafd199afca
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2305047"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-powerapps"></a>Verbinding met uw Business Central-gegevens maken om een bedrijfsapp te maken met PowerApps
U kunt uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-gegevens als gegevensbron beschikbaar maken in PowerApps.  

> [!NOTE]  
>   U moet een geldig account bij [!INCLUDE[d365fin](includes/d365fin_md.md)] en PowerApps hebben.  

## <a name="to-add-included365finincludesd365fin_mdmd-as-a-data-source-in-powerapps"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)] als gegevensbron toevoegen in PowerApps
1. Navigeer in de browser naar [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/) en meld u aan.
2. Kies op de startpagina **Apps**, **Een app maken** en **Canvas** om een nieuwe canvas-app te maken. Deze app wordt ontworpen voor gebruik op een mobiel apparaat, maar u kunt ook een andere sjabloon gebruiken.

    De volgende stap om een PowerApp te maken bestaat eruit uw gegevens te selecteren. Kies het pijlpictogram en kies vervolgens de optie **Nieuwe verbinding** linksboven in de pagina.
3. Kies in de lijst met beschikbare verbindingen **Business Central** en kies de knop **Maken**.

    PowerApps maakt verbinding met uw [!INCLUDE [prodshort](includes/prodshort.md)] met behulp van de aanmeldingsgegevens waarmee u bent aangemeld. Als u geen beheerder hebt van uw [!INCLUDE [prodshort](includes/prodshort.md)], kunt u zich met een ander account aanmelden.  

4.  Met PowerApps wordt een lijst met *omgevingen en bedrijven* weergegeven die beschikbaar zijn in [!INCLUDE [prodshort](includes/prodshort.md)]. Kies de omgeving en het bedrijf met de gegevens waarmee u verbinding wilt maken. Vervolgens krijgt u een lijst met API's te zien. Selecteer de **API** waarmee u verbinding wilt maken.

Deze zogenaamde tabellen maken deel uit van de [!INCLUDE [prodshort](includes/prodshort.md)] API. U hoeft de eindpunten niet zelf te configureren. De [!INCLUDE [prodshort](includes/prodshort.md)]-connector voor PowerApps doet dat voor u.  

    If you want to include data from other tables in [!INCLUDE [prodshort](includes/prodshort.md)] in your app, then you must work with a developer to define a custom API in [!INCLUDE [prodshort](includes/prodshort.md)] and then consume that custom API through a custom connector in PowerApps. For more information, see [Create a custom connector from scratch](/connectors/custom-connectors/define-blank).  

Nu hebt u met succes een koppeling gemaakt naar uw [!INCLUDE [prodshort](includes/prodshort.md)]-gegevens en kunt u uw PowerApp gaan maken. U kunt extra schermen toevoegen en verbinding met extra gegevens maken vanuit uw [!INCLUDE [prodshort](includes/prodshort.md)]. Zie voor meer informatie [Een canvasapp maken vanuit een sjabloon in PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive).  

Wanneer u de app hebt ontworpen en gemaakt, u deze met uw collega's delen. Zie voor meer informatie [Een canvasapp opslaan en publiceren in PowerApps](/powerapps/maker/canvas-apps/save-publish-app).  

> [!NOTE]
> Als u verbinding wilt maken met [!INCLUDE [prodshort](includes/prodshort.md)] on-premises, moet u de connector **Business Central (on-premises)** kiezen in stap 3.  

## <a name="see-also"></a>Zie ook

[Een canvasapp maken vanuit een sjabloon in PowerApps](/powerapps/maker/canvas-apps/get-started-test-drive)  
[Aan de slag](product-get-started.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Financiën](finance.md)  
[Aan de slag met het ontwikkelen van verbindingsapps voor Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)  
