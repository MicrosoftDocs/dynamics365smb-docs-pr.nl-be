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
ms.date: 05/13/2019
ms.author: edupont
ms.openlocfilehash: 67d7129e32ccde3154a02dd12b806d712f470833
ms.sourcegitcommit: 92c7b6c5f0a5d8becbef106ab85258906765bc3e
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 05/13/2019
ms.locfileid: "1540281"
---
# <a name="connecting-to-your-business-central-data-to-build-a-business-app-using-powerapps"></a>Verbinding met uw Business Central-gegevens maken om een bedrijfsapp te maken met PowerApps
U kunt uw gegevens [!INCLUDE[d365fin](includes/d365fin_md.md)] als gegevensbron beschikbaar maken in PowerApps.  

> [!NOTE]  
>   U moet een geldig account bij [!INCLUDE[d365fin](includes/d365fin_md.md)] en PowerApps hebben.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-powerapps"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)] als gegevensbron in PowerApps toevoegen
1. Navigeer in de browser naar [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/) en meld u aan.
2. Kies op de homepage de sjabloon **Start vanuit gegevens** om een nieuwe canvasapp te maken. Deze app wordt ontworpen voor gebruik op een mobiel apparaat, maar u kunt ook een andere sjabloon gebruiken.

    De volgende stap om een PowerApp te maken bestaat eruit uw gegevens te selecteren. Kies het pijlpictogram en kies vervolgens de optie **Nieuwe verbinding** linksboven in de pagina.
3. Kies in de lijst met beschikbare verbindingen **Business Central** en kies de knop **Maken**.

    PowerApps maakt verbinding met uw [!INCLUDE [prodshort](includes/prodshort.md)] met behulp van de aanmeldingsgegevens waarmee u bent aangemeld. Als u geen beheerder hebt van uw [!INCLUDE [prodshort](includes/prodshort.md)], kunt u zich met een ander account aanmelden.  

4. Als u meer dan één bedrijf in uw [!INCLUDE [prodshort](includes/prodshort.md)] hebt, moet u het bedrijf kiezen om verbinding mee te maken. PowerApps geeft dan een lijst met *tabellen* weer die beschikbaar zijn vanuit [!INCLUDE [prodshort](includes/prodshort.md)]. Deze zogenaamde tabellen maken deel uit van de [!INCLUDE [prodshort](includes/prodshort.md)] API. U hoeft de eindpunten niet zelf te configureren. De [!INCLUDE [prodshort](includes/prodshort.md)]-connector voor PowerApps doet dat voor u.  

    Als u gegevens uit andere tabellen in [!INCLUDE [prodshort](includes/prodshort.md)] in uw app wilt opnemen, moet u met een ontwikkelaar werken om een aangepaste API te maken in [!INCLUDE [prodshort](includes/prodshort.md)] en vervolgens die aangepaste API gebruiken via een aangepaste connector in PowerApps. Zie voor meer informatie [Een nieuwe aangepaste connector maken](/connectors/custom-connectors/define-blank).  

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
