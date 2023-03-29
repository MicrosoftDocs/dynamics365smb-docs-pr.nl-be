---
title: Aan de slag met de connector voor Shopify
description: Eerste stappen bij het configureren van verbinding tussen Business Central en Shopify
ms.date: 05/27/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
ms.search.form: '30100, 30101, 30102, 30103, 30104, 30135,'
author: AndreiPanko
ms.author: andreipa
---

# Aan de slag met de Shopify-connector

Verbind uw Shopify-winkel (of -winkels) met [!INCLUDE [prod_short](../includes/prod_short.md)] en maximaliseer de productiviteit van uw bedrijf. Beheer en bekijk inzichten van uw bedrijf en uw Shopify-winkel als één geheel.

Als u Shopify wilt gebruiken met [!INCLUDE [prod_short](../includes/prod_short.md)], moet u eerst een paar dingen doen. Dit artikel dient als een gids om uw Shopify-winkel te integreren met [!INCLUDE [prod_short](../includes/prod_short.md)].

## Vereisten voor Shopify

U moet over het volgende beschikken:

- Een Shopify-account
- Een online Shopify-winkel

Meer informatie over het maken van Shopify-proefversies en aanbevolen instellingen vindt u op [Shopify-account maken en instellen](shopify-account.md).

## Vereisten voor Business Central

- Zorg ervoor dat de app **[Shopify-connector](https://go.microsoft.com/fwlink/?linkid=2196238)** is geïnstalleerd.

  De app is vooraf geïnstalleerd voor alle nieuwe aanmeldingen en proefversies. Voor meer informatie over het installeren van apps vanuit AppSource zie [Extensies installeren en verwijderen](../ui-extensions-install-uninstall.md#install). Volg de onderstaande stappen als u [!INCLUDE[prod_short](../includes/prod_short.md)] niet hebt.

- Zorg ervoor dat de gebruiker voldoende machtigingen heeft. Shopify-connector valt onder de machtigingenset *Shopify – beheer (SHPFY – ADMIN)*. Lees meer op [Gebruikers maken volgens licenties](../ui-how-users-permissions.md) en [Machtigingen toewijzen aan gebruikers en groepen](../ui-define-granular-permissions.md)


## De Dynamics 365 Business Central-app installeren in uw online Shopify-winkel

Voor bestaande [!INCLUDE[prod_short](../includes/prod_short.md)] is stap optioneel en kan deze worden overgeslagen.

1. Zoek de [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central)-app in de [Shopify AppStore](https://apps.shopify.com/)
2. Kies de knop **App toevoegen**. Als daarom wordt gevraagd, logt u in bij uw Shopify-account. Selecteer de gewenste webshop als u er meerdere hebt.
3. Na het bekijken van privacy en machtigingen, kiest u de knop **App installeren**.

   U kunt de geïnstalleerde **Dynamics 365 Business Central**-app vinden en openen in de sectie **Apps** op de zijbalk van de pagina **Shopify-beheer**.
4. Kies **Nu aanmelden** om de [!INCLUDE[prod_short](../includes/prod_short.md)]-proef te starten of kies **Aanmelden** als u [!INCLUDE[prod_short](../includes/prod_short.md)] al hebt. U wordt omgeleid naar uw pagina [Business Central](https://businesscentral.dynamics.com).
5. De volgende stappen moeten worden gedaan in [!INCLUDE[prod_short](../includes/prod_short.md)].

## Business Central verbinden met de online Shopify-winkel

1. Kies het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkel** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.  
3. Voer in het veld **Code** de code in die het gemakkelijk te vinden maakt in [!INCLUDE[prod_short](../includes/prod_short.md)]. Een naam kan bijvoorbeeld weerspiegelen wat een winkel verkoopt, zoals 'Meubels' of 'Koffie', of het land/regio die de winkel bedient.
4. Typ in het veld **Shopify-URL** de URL van uw online winkel die moet worden verbonden. Gebruik de volgende indeling: `https://{shop}.myshopify.com/`.
5. Activeer de schakelaar **Geactiveerd**, bekijk en accepteer de algemene voorwaarden.
6. Meld u desgevraagd aan bij uw Shopify-account, controleer de privacyvoorwaarden en machtigingen en kies vervolgens de knop **App installeren**.

Herhaal stap 2-6 voor alle webshops die u wilt verbinden.

### Bekende problemen

- De browser blokkeert het pop-upvenster. Wanneer u de schakelaar **Geactiveerd** inschakelt, opent het systeem de pagina **Wachten op een reactie. Sluit deze pagina niet**, die wacht op een toegangstoken van Shopify. Als die pagina is gesloten of geblokkeerd, kunt u geen verbinding maken met Shopify. Meer informatie op [Om het toegangstoken verzoeken](troubleshoot.md#request-the-access-token)
- [Oauth-fout invalid_request: Kan Shopify API-toepassing niet vinden met api_key](troubleshoot.md#oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key)
- [Kan geen verbinding maken vanuit sandbox](troubleshoot.md#verify-and-enable-permissions-to-make-http-requests-when-running-in-a-non-production-environment)


## Volgende stappen

Nu is uw online winkel verbonden met [!INCLUDE[prod_short](../includes/prod_short.md)]. In de volgende stappen definieert u hoe en wat u wilt synchroniseren.

- [Artikelen synchroniseren](synchronize-items.md)
- [Klanten synchroniseren](synchronize-customers.md)
- [Orders synchroniseren](synchronize-orders.md)

## Zie ook

[Procedure: Shopify-connector instellen en gebruiken](walkthrough-setting-up-and-using-shopify.md)  

