---
title: Aan de slag met de connector voor Shopify
description: Eerste stappen bij het configureren van verbinding tussen Business Central en Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
ms.search.form: 30100, 30101, 30102, 30103, 30104, 30135,
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: e59dd0dcf757fbcf76d4068756adfe7bc9475f54
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 08/29/2022
ms.locfileid: "9361568"
---
# <a name="get-started-with-the-shopify-connector"></a>Aan de slag met de Shopify-connector

Verbind uw Shopify-winkel (of -winkels) met [!INCLUDE [prod_short](../includes/prod_short.md)] en maximaliseer de productiviteit van uw bedrijf. Beheer en bekijk inzichten van uw bedrijf en uw Shopify-winkel als één geheel. 

De Shopify-connector bevat de volgende mogelijkheden:

- Ondersteuning voor meer dan één Shopify-winkel  

  - Elke winkel heeft zijn eigen opzet, waaronder een verzameling producten, locaties die worden gebruikt om de voorraad te berekenen en prijslijsten.  
- Bidirectionele synchronisatie van artikelen of producten  

  - De connector synchroniseert afbeeldingen, artikelvarianten, streepjescodes, artikelnummers van leveranciers, uitgebreide teksten en tags.  
  -    Artikelkenmerken exporteren naar Shopify.  
  -    Gebruik geselecteerde klantprijsgroepen en kortingen om prijzen te definiëren die worden geëxporteerd naar Shopify.  
  -    Bepaal of items automatisch kunnen worden gemaakt of alleen updates van bestaande producten toestaan.  
- Synchronisatie van voorraadniveaus  

  -    Kies enkele of alle beschikbare locaties in [!INCLUDE [prod_short](../includes/prod_short.md)].  
  -    Werk voorraadniveaus op meerdere locaties bij in Shopify.  
- Bidirectionele synchronisatie van klanten  

  -    Wijs klanten slim toe per telefoon en e-mail.  
  -    Gebruik landspecifieke sjablonen bij het maken van klanten, zodat u zeker weet dat de belastinginstellingen correct zijn.  
- Importeren van bestellingen uit Shopify  

  -    Tijdens het importeren kunt u automatisch klanten maken in [!INCLUDE [prod_short](../includes/prod_short.md)] of besluiten de klanten te beheren in Shopify.  
  -    Neem orders op die in andere kanalen zijn gemaakt, zoals Shopify POS of Amazon.  
  -    Verzendkosten, cadeaubonnen, fooien, verzend- en betaalmethoden, transacties en risico op fraude.  
  - Uitbetalingsinformatie ontvangen van Shopify Payments.  
- Eenvoudig volgen van afhandelingsinformatie  

  -    Kies er optioneel voor om trackinginformatie voor artikelen te schrijven van [!INCLUDE [prod_short](../includes/prod_short.md)] naar Shopify.  

Als u Shopify wilt gebruiken met [!INCLUDE [prod_short](../includes/prod_short.md)], moet u eerst een paar dingen doen. Dit artikel dient als een gids om de integratie van uw Shopify-winkel met [!INCLUDE [prod_short](../includes/prod_short.md)] te voltooien.

## <a name="prerequisites-for-shopify"></a>Vereisten voor Shopify

U moet over het volgende beschikken:

- Een Shopify-account
- Een online Shopify-winkel

Als u een nieuw Shopify-account wilt maken of u aan wilt melden voor een gratis proefperiode van 14 dagen, gaat u naar [Shopify](https://www.shopify.com/). Voor meer informatie over het maken en personaliseren van uw online winkel zie [Shopify Helpcentrum](https://help.shopify.com/).
  
Andere verkoopkanalen worden ondersteund, bijvoorbeeld Shopify POS.

### <a name="recommended-settings"></a>Aanbevolen instellingen

- Deactiveer **De order automatisch archiveren** in het gedeelte **Orderverwerking** van de [**Afrekening**-instellingen](https://www.shopify.com/admin/settings/checkout) in uw **Shopify-beheer**.

Als u meer wilt weten over Shopify-instellingen voor demo- en proefscenario's raadpleegt u [Test- en trainingsscenario's](/dynamics365/business-central/dev-itpro/administration/admin-shopify-connector#preparation).

## <a name="prerequisites-for-business-central"></a>Vereisten voor Business Central

- Zorg ervoor dat de app **[Shopify-connector](https://go.microsoft.com/fwlink/?linkid=2196238)** is geïnstalleerd.

De app is vooraf geïnstalleerd voor alle nieuwe aanmeldingen en proefversies. Leer meer over het installeren van apps vanuit de marktplaats in [Extensies installeren en verwijderen](../ui-extensions-install-uninstall.md#install). Volg de onderstaande stappen als u [!INCLUDE[prod_short](../includes/prod_short.md)] niet hebt.

## <a name="installing-the-dynamics-365-business-central-app-to-your-shopify-online-store"></a>De **Dynamics 365 Business Central**-app installeren in uw online Shopify-winkel

Voor bestaande [!INCLUDE[prod_short](../includes/prod_short.md)] is stap optioneel en kan deze worden overgeslagen.

1. Zoek de [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central)-app in de [Shopify AppStore](https://apps.shopify.com/)
2. Kies de knop **App toevoegen**. Als daarom wordt gevraagd, meld u dan aan bij uw Shopify-account. Selecteer de gewenste webshop als u er meerdere hebt.
3. Na het bekijken van privacy en machtigingen, kiest u de knop **App installeren**.
  U kunt de geïnstalleerde **Dynamics 365 Business Central** vinden en openen in de sectie **Apps** op de zijbalk van **Shopify-beheer**.
4. Kies **Nu aanmelden** om de [!INCLUDE[prod_short](../includes/prod_short.md)]-proef te starten of kies **Aanmelden** als u [!INCLUDE[prod_short](../includes/prod_short.md)] al hebt. U wordt omgeleid naar uw proefversie van [!INCLUDE[prod_short](../includes/prod_short.md)] in [Business Central](https://businesscentral.dynamics.com).
5. De volgende stappen moeten worden gedaan in [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="connecting-business-central-to-the-shopify-online-store"></a>Business Central verbinden met de online Shopify-winkel

1. Ga naar het pictogram zoeken ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-winkel** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.  
3. Voer in het veld **Code** de gewenste code in.  
4. Typ in het veld **Shopify-URL** de URL van uw online winkel die moet worden verbonden. Gebruik de volgende indeling: `https://{shop}.myshopify.com/`.
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

