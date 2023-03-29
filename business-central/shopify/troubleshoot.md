---
title: Problemen oplossen met de synchronisatie tussen Shopify en Business Central
description: Leer wat u moet doen als er iets mis gaat tijdens de synchronisatie van gegevens tussen Shopify en Business Central
ms.date: 08/19/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.search.form: '30118, 30119, 30120, 30101, 30102'
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
---

# Problemen oplossen met de synchronisatie tussen Shopify en Business Central

Het is mogelijk om situaties tegen te komen waarin u problemen moet oplossen bij het synchroniseren van gegevens tussen Shopify en [!INCLUDE[prod_short](../includes/prod_short.md)]. Deze pagina definieert stappen voor het oplossen van enkele veelvoorkomende probleemscenario's die zich kunnen voordoen.

## Logboeken

Als een synchronisatietaak mislukt, kunt u logboekregistratie activeren door de schakelaar **Logboek inschakelen** in te schakelen op de pagina **Shopify-winkelkaart**. Dan kunt u de synchronisatietaak handmatig activeren en logboeken bekijken.

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-logposten** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de gerelateerde logboekpost en open de pagina **Shopify-logpost**.
3. Bekijk het verzoek, de statuscode, de beschrijving en de reactiewaarden.

Vergeet later niet logboekregistratie later uit te schakelen om negatieve invloed op de prestaties en een toename van de databasegrootte te voorkomen.

Vanaf de pagina **Shopify-logposten** kunt u de verwijdering van alle logposten triggeren of van logposten die ouder zijn dan zeven dagen.

## Gegevensvastlegging

Ongeacht de **Log geactiveerd**-instellingen worden bepaalde reacties vanuit Shopify altijd vastgelegd, zodat u ze kunt inspecteren of downloaden met behulp van de pagina **Lijst voor gegevensvastlegging**.

Kies de actie **Opgehaalde Shopify-gegevens** op een van de volgende pagina's:

- **Shopify-order**
- **Shopify-orderafhandelingen**
- **Verzendkosten voor Shopify-orders**
- **Shopify-ordertransacties**
- **Shopify-uitbetalingen**
- **Shopify-betalingstransacties**
- **Shopify-transacties**

## Synchronisatie opnieuw instellen

Voor optimale prestaties importeert de connector alleen klanten, producten en orders die zijn gemaakt of gewijzigd sinds de laatste synchronisatie. Op de pagina **Shopify-winkelkaart** zijn er functies beschikbaar die de datum/tijd van de laatste synchronisatie wijzigen of volledig resetten. Deze functie zorgt ervoor dat wanneer de synchronisatie wordt uitgevoerd, alle gegevens worden gesynchroniseerd en niet alleen de wijzigingen sinds de laatste synchronisatie.

Deze functie is alleen van toepassing op synchronisaties van Shopify naar [!INCLUDE[prod_short](../includes/prod_short.md)]. Het kan handig zijn als u verwijderde gegevens zoals producten, klanten of verwijderde bestellingen moet herstellen.

## Om het toegangstoken verzoeken

Als [!INCLUDE[prod_short](../includes/prod_short.md)] geen verbinding kan maken met uw Shopify-account, probeer dan het toegangstoken opnieuw in te stellen vanuit Shopify. Dit verzoek kan nodig zijn als er een rotatie van beveiligingssleutels of wijzigingen in de vereiste machtigingen (bereiken) is.

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u het toegangstoken wilt ophalen om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Toegang aanvragen**.
4. Als daarom wordt gevraagd, logt u in bij uw Shopify-account.

De schakelaar **Heeft toegangssleutel** wordt geactiveerd.

### Verifieer en activeer machtigingen om http-verzoeken te doen bij gebruik in een niet-productieomgeving

Om correct te kunnen werken vereist de extensie Shopify-connector toestemming om http-verzoeken te doen. Bij het testen in een sandbox zijn de http-verzoeken voor alle extensies verboden.

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **extensiebeheer** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de extensie **Shopify-connector**.
3. Kies de actie **Configureren** om de pagina **Extensie-instellingen** te openen.
4. Zorg ervoor dat de schakelaar **HttpClient-aanvragen toestaan** is ingeschakeld.

## Het Shopify-toegangstoken roteren

De volgende procedures beschrijven hoe u het toegangstoken kunt roteren dat wordt gebruikt door de Shopify-connector om toegang te krijgen tot uw online Shopify-winkel.

### In Shopify

1. Ga vanuit uw **Shopify-beheer** naar [Apps](https://www.shopify.com/admin/apps).
2. Selecteer **Verwijderen** in de rij met de app **Dynamics 365 Business Central**.
3. Selecteer **Verwijderen** in het bericht dat wordt weergegeven.

### In [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u het toegangstoken wilt roteren om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Toegang aanvragen**.
4. Meld u desgevraagd aan bij uw Shopify-account, controleer de privacy en machtigingen en kies vervolgens de knop **App installeren**.

## Bekende problemen

### De *Bedrijfsboekingsgroep* kan niet nul of leeg zijn. Er moet een waarde in het klantveld staan

Vul het veld **Klantensjablooncode** op de pagina **Shopify -winkelkaart** met de sjabloon waarin **Bedrijfsboekingsgroep** is ingevuld. De klantensjabloon wordt niet alleen gebruikt voor het maken van klanten, maar ook voor het berekenen van verkoopprijzen en tijdens het maken van verkoopdocumenten.

### Gegevens importeren naar uw Shopify-winkel is niet ingeschakeld. Ga naar de winkelkaart om deze in te schakelen

Zet in het venster **Shopify-winkelkaart** de schakelaar **Gegevenssynchronisatie naar Shopify toestaan** aan. Deze schakelaar is bedoeld om de online winkel te beschermen tegen het verkrijgen van demogegevens van [!INCLUDE[prod_short](../includes/prod_short.md)].

### Oauth-fout invalid_request: Kan Shopify API-toepassing niet vinden met api_key

Het lijkt erop dat u [App insluiten](/dynamics365/business-central/dev-itpro/deployment/embed-app-overview) gebruikt, waarbij de client-URL deze indeling heeft: `https://[application name].bc.dynamics.com`. De Shopify-connector werkt niet voor Insluiten-apps. Zie voor meer informatie [Voor welke Microsoft-producten is de Shopify connector beschikbaar](shopify-faq.md#what-microsoft-products-is-the-shopify-connector-available-for).

## Zie ook

[Aan de slag met de connector voor Shopify](get-started.md)
