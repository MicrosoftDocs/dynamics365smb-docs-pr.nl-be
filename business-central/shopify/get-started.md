---
title: Aan de slag met de connector voor Shopify
description: Eerste stappen bij het configureren van verbinding tussen Business Central en Shopify
ms.date: 03/27/2023
ms.topic: article
ms.service: dynamics-365-business-central
ms.reviewer: solsen
ms.search.form: '30100, 30101, 30102, 30103, 30104, 30135,'
author: brentholtorf
ms.author: bholtorf
---

# <a name="get-started-with-the-shopify-connector"></a>Aan de slag met de Shopify-connector

Verbind uw Shopify-winkel met [!INCLUDE [prod_short](../includes/prod_short.md)] en maximaliseer de productiviteit van uw bedrijf. Beheer en bekijk inzichten van uw bedrijf en uw Shopify-winkel als één geheel.

Als u Shopify wilt gebruiken met [!INCLUDE [prod_short](../includes/prod_short.md)], moet u eerst een paar dingen doen. Dit artikel dient als een gids om uw Shopify-winkel te integreren met [!INCLUDE [prod_short](../includes/prod_short.md)].

## <a name="prerequisites-for-shopify"></a>Vereisten voor Shopify

U moet over het volgende beschikken:

- Een Shopify-account
- Een online Shopify-winkel

Meer informatie over het maken van Shopify-proefversies en de aanbevolen instellingen vindt u op [Shopify-account maken en instellen](shopify-account.md).

## <a name="prerequisites-for-business-central"></a>Vereisten voor Business Central

- Zorg ervoor dat de app **[Shopify-connector](https://go.microsoft.com/fwlink/?linkid=2196238)** is geïnstalleerd.

  De app is vooraf geïnstalleerd voor alle nieuwe aanmeldingen en proefversies. Voor meer informatie over het installeren van apps vanuit AppSource zie [Extensies installeren en verwijderen](../ui-extensions-install-uninstall.md#install). Volg de onderstaande stappen als u [!INCLUDE[prod_short](../includes/prod_short.md)] niet hebt.

- Zorg ervoor dat de gebruiker de juiste machtigingen heeft. Shopify-connector valt onder de machtigingenset **Shopify – beheer (SHPFY – ADMIN)**. Lees meer op [Gebruikers maken volgens licenties](../ui-how-users-permissions.md) en [Machtigingen toewijzen aan gebruikers en groepen](../ui-define-granular-permissions.md).

## <a name="install-the-dynamics-365-business-central-app-to-your-shopify-online-store"></a>De Dynamics 365 Business Central-app installeren in uw online Shopify-winkel

Voor bestaande instanties van [!INCLUDE[prod_short](../includes/prod_short.md)] is deze stap optioneel en kan deze worden overgeslagen.

1. Zoek de [Dynamics 365 Business Central](https://apps.shopify.com/dynamics-365-business-central)-app in de [Shopify AppStore](https://apps.shopify.com/)
2. Kies de knop **App toevoegen**. Als daarom wordt gevraagd, logt u in bij uw Shopify-account. Selecteer de online winkel als u er meerdere hebt.
3. Na het bekijken van privacy en machtigingen, kiest u de knop **App installeren**.

   U kunt de geïnstalleerde **Dynamics 365 Business Central**-app vinden en openen in de sectie **Apps** op de zijbalk van de pagina **Shopify-beheer**.
4. Kies **Nu aanmelden** om de [!INCLUDE[prod_short](../includes/prod_short.md)]-proef te starten of kies **Aanmelden** als u [!INCLUDE[prod_short](../includes/prod_short.md)] al hebt. U wordt omgeleid naar uw pagina [Business Central](https://businesscentral.dynamics.com).
5. Voer de volgende stappen uit in [!INCLUDE[prod_short](../includes/prod_short.md)].

## <a name="connect-business-central-to-the-shopify-online-store"></a>Business Central verbinden met de online Shopify-winkel

1. Kies het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkel** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.  
3. Voer in het veld **Code** een code in die gemakkelijk te vinden is in [!INCLUDE[prod_short](../includes/prod_short.md)]. De naam kan bijvoorbeeld weerspiegelen wat een winkel verkoopt, zoals 'Meubels' of 'Koffie', of het land/regio die de winkel bedient.
4. Voer in het veld **Shopify-URL** de URL in van de online winkel waarmee u verbinding maakt. Gebruik de volgende indeling: `https://{shop}.myshopify.com/`.

   > [!TIP]
   > U kunt de URL kopiëren van Shopify - Beheerder, zoals `https://admin.shopify.com/store/{shop}`, en met de connector wordt deze naar de vereiste indeling geconverteerd.

5. Activeer de schakelaar **Geactiveerd** en bekijk en accepteer vervolgens de algemene voorwaarden.
6. Als daarom wordt gevraagd, logt u in bij uw Shopify-account. Bekijk de privacyvoorwaarden en machtigingen en kies vervolgens de knop **App installeren**.

Herhaal stap 2-6 voor alle webshops die u wilt verbinden.

### <a name="known-issues"></a>Bekende problemen

- De browser blokkeert het pop-upvenster. Wanneer u de schakelaar **Geactiveerd** aanzet, opent [!INCLUDE [prod_short](../includes/prod_short.md)] de pagina **Wachten op een reactie. Sluit deze pagina niet** terwijl het wacht op een toegangstoken van Shopify. Als die pagina gesloten of geblokkeerd is, kunt u geen verbinding maken met Shopify. Meer informatie op [Om het toegangstoken verzoeken](troubleshoot.md#request-the-access-token).
- Het kan een goed idee zijn om het Shopify-beheer geopend te hebben in dezelfde browser als [!INCLUDE [prod_short](../includes/prod_short.md)]
- [Fout: Oauth-fout invalid_request: Kan Shopify API-toepassing niet vinden met api_key.](troubleshoot.md#error-oauth-error-invalid_request-could-not-find-shopify-api-application-with-api_key)
- [Fout: Oauth-fout invalid_request: Uw account heeft geen machtiging om de gevraagde toegang voor deze app te verlenen.](troubleshoot.md#error-oauth-error-invalid_request-your-account-does-not-have-permission-to-grant-the-requested-access-for-this-app)
- [Kan geen verbinding maken vanuit sandbox](troubleshoot.md#verify-and-enable-permissions-to-make-http-requests-in-a-non-production-environment)
- Zorg ervoor dat u de juiste URL invoert in het veld **Shopify-URL**. U kunt de URL samenstellen door de winkel-id van de beheerders-URL te combineren. Bijvoorbeeld `admin.shopify.com/store/{shop}` en `.myshopify.com` om `https://{shop}.myshopify.com/` te krijgen.

## <a name="next-steps"></a>Volgende stappen

Nu is uw online winkel verbonden met [!INCLUDE[prod_short](../includes/prod_short.md)]. In de volgende stappen definieert u hoe en wat u wilt synchroniseren.

- [Artikelen en voorraad synchroniseren](synchronize-items.md)
- [Klanten synchroniseren](synchronize-customers.md)
- [Orders synchroniseren](synchronize-orders.md)

## <a name="testing-strategies"></a>Strategieën testen

Er zijn verschillende benaderingen voor het testen van een integratie, en elke benadering heeft zijn voor- en nadelen.

U kunt [!INCLUDE[prod_short](../includes/prod_short.md)]- en Shopify-accounts zo vaak u wilt verbinden. De Shopify-connector is alleen van invloed op de omgeving, of om preciezer te zijn, op het bedrijf waar deze is geactiveerd. U kunt verbinding maken met dezelfde online Shopify-winkel vanuit meerdere omgevingen of bedrijven. U kunt de connector uitschakelen en opnieuw inschakelen.

Het is eenvoudig om synchronisatietests opnieuw uit te voeren. Met de connector kunt u geïmporteerde gegevens, zoals producten, klanten en orders, verwijderen en vervolgens weer importeren. U moet gewoon de [synchronisatie resetten](troubleshoot.md#reset-sync).

### <a name="shopify-sandbox-and-business-central-sandbox"></a>Shopify-sandbox en Business Central-sandbox

Dit is waarschijnlijk de veiligste manier om integratie te testen. In plaats van een Shopify-sandbox te gebruiken, kunt u ook een proefabonnement of Ontwikkelingswinkel gebruiken. In [!INCLUDE[prod_short](../includes/prod_short.md)] kunt u ook gebruik maken van een testbedrijf in een productieomgeving.

Ga voor meer informatie over [!INCLUDE[prod_short](../includes/prod_short.md)]-sandboxen naar [Een nieuwe omgeving maken](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#create-a-new-environment).

### <a name="shopify-sandbox-and-business-central-production"></a>Shopify-sandbox en Business Central-productie

Dit is *geen* aanbevolen configuratie om te testen, omdat de Shopify-connector artikelen en klanten kan maken of wijzigen. Het kan ook verkoopdocumenten creëren, zoals orders en facturen. Deze documenten kunnen moeilijk ongedaan te maken zijn.
 
Als u deze configuratie moet gebruiken, raden we u aan de volgende instellingen te bekijken en waarschijnlijk uit te schakelen:

* **Automatisch onbekende artikelen maken** om geen artikelen te maken.
* **Shopify kan artikelen bijwerken** om toegewezen artikelen niet bij te werken.
* **Automatisch onbekende klanten maken** om geen klanten en contacten te maken.
* **Shopify kan klanten bijwerken** om bestaande klanten niet bij te werken.
* **Verkooporder automatisch maken** om geen verkooporders en verkoopfacturen te maken.

Zie [Een omgeving herstellen](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-backup-restore) voor meer informatie.

### <a name="shopify-production-and-business-central-sandbox"></a>Shopify-productie en Business Central-sandbox

Het kan een goed idee zijn om een ​​back-up van uw gegevens te maken. Exporteer bijvoorbeeld uw producten en klanten. Zie voor meer informatie [CSV-bestanden gebruiken om een ​​back-up te maken van winkelinformatie](https://help.shopify.com/en/manual/shopify-admin/duplicate-store#using-csv-files-to-back-up-store-information).

Schakel de schakelaar **Gegevenssynchronisatie naar Shopify toestaan** uit zodat [!INCLUDE[prod_short](../includes/prod_short.md)] niet schrijft naar Shopify. In dit geval kunt u producten, afbeeldingen, klanten en orders importeren uit Shopify. Maar u kunt geen artikelen, prijzen, voorraadniveaus, klanten en afhandelingsinformatie naar Shopify sturen.

Als u de schakelaar **Gegevenssynchronisatie naar Shopify toestaan** ingeschakeld houdt, zijn er extra beschermende maatregelen:

*   Selecteer **Concept** in het veld **Status voor product maken** om ervoor te zorgen dat geëxporteerde producten niet beschikbaar zijn voor kopers. U kunt controleren hoe producten er in de online winkel uitzien en prijzen, opties en voorraadniveaus synchroniseren. Zorg ervoor dat u filters gebruikt op de pagina **Artikel toevoegen aan Shopify** om het aantal geëxporteerde artikelen te beperken.
* Schakel de schakelaar **Klant exporteren naar Shopify** uit, zodat u geen klanten naar Shopify verzendt.

## <a name="see-also"></a>Zie ook

[Procedure: Shopify-connector instellen en gebruiken](walkthrough-setting-up-and-using-shopify.md)  

