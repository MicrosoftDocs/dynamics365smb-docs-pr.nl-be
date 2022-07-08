---
title: Problemen oplossen met de synchronisatie tussen Shopify en Business Central
description: Leer wat u moet doen als er iets mis is gegaan tijdens de synchronisatie van gegevens tussen Shopify en Business Central
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 83678c6c81b29a524405699425be877459b6568d
ms.sourcegitcommit: 00a8acc82cdc90e0d0db9d1a4f98a908944fd50a
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9075329"
---
# <a name="troubleshooting-the-shopify-and-business-central-synchronization"></a>Problemen oplossen met de synchronisatie tussen Shopify en Business Central

Het is mogelijk om situaties tegen te komen waarin u problemen moet oplossen bij het synchroniseren van gegevens tussen Shopify en [!INCLUDE[prod_short](../includes/prod_short.md)]. Deze pagina definieert stappen voor het oplossen van enkele veelvoorkomende scenario's die zich kunnen voordoen.

## <a name="logs"></a>Logboeken

Als een synchronisatietaak mislukt, kunt u logboekregistratie activeren door de schakelaar **Logboek inschakelen** in te schakelen op de **Shopify-winkelkaart**. Activeer handmatig de synchronisatietaak en bekijk logboeken.

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-logposten** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de gerelateerde logboekpost en open het venster **Shopify-logpost**.
3. Bekijk het verzoek, de statuscode, de beschrijving en de reactie.

Vergeet niet logboekregistratie later uit te schakelen om negatieve invloed op de prestaties en een toename van de databasegrootte te voorkomen.

Vanuit het venster **Shopify-logposten** kunt u de verwijdering van alle logposten triggeren of van logposten die ouder zijn dan zeven dagen.

## <a name="data-capture"></a>Gegevensvastlegging

Ongeacht de **Log geactiveerd**-instellingen worden bepaalde reacties vanuit Shopify altijd vastgelegd en kunt u ze inspecteren of downloaden met behulp van het venster **Lijst voor gegevensvastlegging**.

Kies de actie **Opgehaalde Shopify-gegevens** op een van de volgende pagina's:

- **Shopify-order**
- **Shopify-orderafhandelingen**
- **Verzendkosten voor Shopify-orders**
- **Shopify-ordertransacties**
- **Shopify-uitbetalingen**
- **Shopify-betalingstransacties**
- **Shopify-transacties**

## <a name="reset-sync"></a>Synchronisatie opnieuw instellen

Voor optimale prestaties importeert de connector alleen klanten, producten en orders die zijn gemaakt of gewijzigd sinds de laatste synchronisatie. Op de **Shopify-winkelkaart** zijn er functies beschikbaar om de datum/tijd van de laatste synchronisatie te wijzigen of volledig te resetten. Deze functie zorgt ervoor dat wanneer de synchronisatie wordt uitgevoerd, alle gegevens worden gesynchroniseerd en niet alleen de wijzigingen sinds de laatste synchronisatie.

Deze functie is alleen van toepassing op synchronisaties van Shopify naar [!INCLUDE[prod_short](../includes/prod_short.md)] en kan handig zijn als u verwijderde gegevens zoals producten, klanten of verwijderde bestellingen moet herstellen.

## <a name="request-the-access-token"></a>Om het toegangstoken verzoeken

Als [!INCLUDE[prod_short](../includes/prod_short.md)] geen verbinding kan maken met uw Shopify-account, probeer dan het toegangstoken opnieuw in te stellen vanuit Shopify. Dit verzoek kan nodig zijn als er een rotatie van beveiligingssleutels of wijzigingen in de vereiste machtigingen (bereiken) is.

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u het toegangstoken wilt ophalen om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Toegang aanvragen**.
4. Als daarom wordt gevraagd, logt u in bij uw Shopify-account.

De schakelaar **Heeft toegangssleutel** wordt geactiveerd.

### <a name="verify-and-enable-permissions-to-make-http-requests-when-running-in-a-non-production-environment"></a>Verifieer en schakel machtigingen in om Http-verzoeken te doen bij gebruik in een niet-productieomgeving

Om correct te kunnen werken vereist de extensie Shopify-connector toestemming om HTTP-verzoeken te doen. Bij het testen in Sandboxes zijn de HTTP-verzoeken voor alle extensies verboden.

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Extensiebeheer** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de extensie *Shopify-connector*.
3. Kies de actie **Configureren** om de pagina **Extensie-instellingen** te openen.
4. Zorg ervoor dat de schakelaar **HttpClient-aanvragen toestaan** is ingeschakeld.

## <a name="rotate-the-shopify-access-key"></a>De Shopify-toegangssleutel roteren

De volgende procedures beschrijven hoe u het toegangstoken kunt roteren dat wordt gebruikt door de Shopify-connector om toegang te krijgen tot uw online Shopify-winkel.

### <a name="in-shopify"></a>In Shopify

1. Ga vanuit uw **Shopify-beheer** naar [Apps](https://www.shopify.com/admin/apps).
2. Selecteer in de rij met de app *Dynamics 365 Business Central* **Verwijderen**.
3. Selecteer in het bericht dat wordt weergegeven de optie **Verwijderen**.

### <a name="in-prod_short"></a>In [!INCLUDE[prod_short](../includes/prod_short.md)]

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u het toegangstoken wilt roteren om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Toegang aanvragen**.
4. Meld u desgevraagd aan bij uw Shopify-account, controleer de privacy en machtigingen en kies vervolgens de knop **App installeren**.

## <a name="see-also"></a>Zie ook

[Aan de slag met de connector voor Shopify](get-started.md)  