---
title: Aan de slag met de connector voor Shopify
description: Eerste stappen bij het configureren van verbinding tussen Business Central en Shopify
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: 2b88995cad8cfe0c3688ca062643f2d339fed9bf
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768208"
---
# <a name="get-started-with-the-shopify-connector"></a>Aan de slag met de Shopify-connector

[!INCLUDE [prod_short](../includes/prod_short.md)] geeft u de flexibiliteit om uw Shopify-winkel (of winkels) ermee te verbinden om uw bedrijfsproductiviteit te maximaliseren. U kunt inzichten uit uw bedrijf en uw online Shopify-winkel als één eenheid bekijken met behulp van de Shopify-connector. Als u Shopify wilt gebruiken met [!INCLUDE [prod_short](../includes/prod_short.md)], moet u enkele stappen volgen. Deze pagina dient als een gids om de integratie van uw Shopify-winkel met [!INCLUDE [prod_short](../includes/prod_short.md)] te voltooien.

## <a name="prerequisites-for-shopify"></a>Vereisten voor Shopify

U moet over het volgende beschikken:

- Een Shopify-account
- Een online Shopify-winkel

Als u een nieuw Shopify-account wilt maken of u aan wilt melden voor een gratis proefperiode van 14 dagen, gaat u naar [Shopify](https://www.shopify.com/). Voor meer informatie over het maken en personaliseren van uw online winkel zie [Shopify Helpcentrum](https://help.shopify.com/).
  
- Andere verkoopkanalen worden ondersteund, bijvoorbeeld Shopify POS.

### <a name="recommended-settings"></a>Aanbevolen instellingen

- Deactiveer **De order automatisch archiveren** in het gedeelte **Orderverwerking** van de [**Afrekening**-instellingen](https://www.shopify.com/admin/settings/checkout) in uw **Shopify-beheer**.

Als u meer wilt weten over Shopify-instellingen voor demo- en proefscenario's raadpleegt u [Test- en trainingsscenario's](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector#preparation).

## <a name="prerequisites-for-business-central"></a>Vereisten voor Business Central

- Zorg dat de extensie **Verbinden met Shopify voor [!INCLUDE[prod_short](../includes/prod_short.md)]** is geïnstalleerd.

De extensie is vooraf geïnstalleerd voor alle nieuwe aanmeldingen en proefversies. Als u extensies van de marktplaats moet installeren, gaat u naar [Extensies installeren en verwijderen](../ui-extensions-install-uninstall.md#install). Volg de onderstaande stappen als u [!INCLUDE[prod_short](../includes/prod_short.md)] niet hebt.
<!--
## Installing the **Dynamics 365 Business Central** app to your Shopify online store

For existing [!INCLUDE[prod_short](../includes/prod_short.md)], this step is optional and can be skipped.

1. Locate the [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central) app on the [Shopify AppStore](https://apps.shopify.com/)
2. Choose the **Add App** button. Sign-in into your Shopify account if prompted. Select the required online shop if you've more than one.
3. After reviewing privacy and permissions, choose the **Install App** button.
  You can find and open the installed **Dynamics 365 Business Central** app in the **Apps** section on the sidebar of **Shopify admin**.
4. Choose **Sign up now** to start [!INCLUDE[prod_short](../includes/prod_short.md)] trial or **Sign in** if you already have [!INCLUDE[prod_short](../includes/prod_short.md)]. You'll be redirected to your [!INCLUDE[prod_short](../includes/prod_short.md)] at [Business Central](https://businesscentral.dynamics.com).
5. The next steps should be done in [!INCLUDE[prod_short](../includes/prod_short.md)].
-->
## <a name="connecting-business-central-to-the-shopify-online-store"></a>Business Central verbinden met de online Shopify-winkel

1. Ga naar het pictogram zoeken ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-winkel** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.  
3. Voer in het veld **Code** de gewenste code in.  
4. Typ in het veld **Shopify-URL** de URL van uw online winkel die moet worden verbonden.
5. Activeer de schakelaar **Ingeschakeld**, bekijk en accepteer de algemene voorwaarden.
6. Meld u desgevraagd aan bij uw Shopify-account, controleer de privacy en machtigingen en kies vervolgens de knop **App installeren**.

Herhaal stap 2-6 voor alle webshops die u wilt verbinden.

### <a name="next-steps"></a>Volgende stappen

Nu is uw online winkel verbonden met [!INCLUDE[prod_short](../includes/prod_short.md)]. In de volgende stappen definieert u hoe en wat u wilt synchroniseren.

- [Artikelen synchroniseren](synchronize-items.md)
- [Klanten synchroniseren](synchronize-customers.md)
- [Orders synchroniseren](synchronize-orders.md)

## <a name="see-also"></a>Zie ook

[Test- en trainingsscenario's](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector).

