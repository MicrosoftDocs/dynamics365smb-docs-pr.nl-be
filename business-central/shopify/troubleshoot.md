---
title: Problemen oplossen met de synchronisatie tussen Shopify en Business Central
description: Leer wat u moet doen als er iets mis is tijdens de synchronisatie van gegevens tussen Shopify en Business Central
ms.date: 05/16/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: ff2e4aca52f479e461dab0d9d0f0ce4958d19353
ms.sourcegitcommit: fb43bc843be4ea9c0c674a14945df727974d9bb9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 05/27/2022
ms.locfileid: "8808886"
---
# <a name="troubleshooting-the-shopify-and-business-central-synchronization"></a>Problemen oplossen met de synchronisatie tussen Shopify en Business Central

Het is mogelijk om situaties tegen te komen waarin u problemen moet oplossen. Deze pagina definieert stappen voor het oplossen van enkele veelvoorkomende scenario's die zich kunnen voordoen.

## <a name="logs"></a>Logboeken

Als een synchronisatietaak mislukt, kunt u logboekregistratie activeren door de schakelaar **Logboek inschakelen** in te schakelen op de **Shopify-winkelkaart**. Activeer handmatig een synchronisatietaak en bekijk logboeken.

1. Ga naar het pictogram zoeken ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-logposten** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de gerelateerde logboekpost en open het venster **Shopify-logpost**.
3. Bekijk het verzoek, de statuscode, de beschrijving en de reactie.

Vergeet niet logboekregistratie uit te schakelen om negatieve invloed op de prestaties en een toename van de databasegrootte te voorkomen.

Vanuit het venster **Shopify-logposten** kunt u verwijdering van alle logposten triggeren of van logposten die ouder zijn dan zeven dagen.

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

## <a name="update-the-access-token"></a>Het toegangstoken bijwerken

Als [!INCLUDE[prod_short](../includes/prod_short.md)] geen verbinding kan maken met uw Shopify-account, probeer dan het toegangstoken opnieuw in te stellen.

1. Ga naar het pictogram zoeken ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-winkel** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u het toegangstoken wilt ophalen om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Toegang aanvragen**.
4. Als daarom wordt gevraagd, logt u in bij uw Shopify-account.

## <a name="see-also"></a>Zie ook

[Aan de slag met de connector voor Shopify](get-started.md)  
