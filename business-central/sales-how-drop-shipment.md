---
title: Een verkooporder koppelen aan een inkooporder voor een directe verzending (bevat video) | Microsoft Docs
description: Hierin wordt beschreven hoe u een verkooporder kunt maken die is gekoppeld aan een inkooporder om verzending direct van de leverancier naar de klant mogelijk te maken.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: direct shipment
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1e4ce5185ba1a672784f2a1c893de82c3da69ee5
ms.sourcegitcommit: 4c97f38fc53c1c1ec534054a4a100d8cfb73175b
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/20/2021
ms.locfileid: "7939988"
---
# <a name="make-drop-shipments"></a>Doorverzendingen uitvoeren

Een doorverzending is de directe verzending van artikelen van een van uw leveranciers naar een van uw klanten.

Wanneer een verkooporder gemarkeerd is voor doorverzending en u een inkooporder maakt met de klant in het veld **Verzenden naar**, **Klantadres**, kunt u de twee documenten koppelen en zo de leverancier instrueren om rechtstreeks naar de klant te verzenden.
<br><br>  
  
> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4mOyM?rel=0]

## <a name="to-create-a-sales-order-for-drop-shipment"></a>Een verkooporder voor doorverzending maken

Ter voorbereiding op een doorverzending maakt u een verkooporder voor een artikel en geeft u op de verkoopregel aan dat voor de verkoop doorverzending vereist is.

1. Maak een verkooporder voor een artikel. Zie [Producten verkopen](sales-how-sell-products.md) voor meer informatie.
2. Op de verkooporderregel voor de doorverzending schakelt u het selectievakje **Doorverzending** in. Gebruik de functie **Kolommen kiezen** als het veld niet zichtbaar is. Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.

## <a name="to-create-the-purchase-order-for-drop-shipment"></a>De inkooporder voor doorverzendingen maken

Om een doorverzending voor te bereiden geeft u op de inkooporder aan dat deze naar uw klant moet worden verzonden, niet naar uzelf.

1. Inkooporder maken. Vul geen velden op de regels in. Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md).
2. Selecteer in het veld **Verzenden naar**, **Klantadres**.
3. Selecteer in het veld **Klant** de klant aan wie u verkoopt.
4. Kies de actie **Doorverzendingen** en kies vervolgens de actie **Verkooporder ophalen**.
5. Selecteer op de pagina **Verkoopoverzicht** de verkooporder die u hebt voorbereid in [Een verkooporder voor doorverzending maken](sales-how-drop-shipment.md#to-create-a-sales-order-for-drop-shipment).
6. Kies de knop **OK**.

De regelgegevens van de verkooporder worden ingevoegd op de inkooporderregel(s).

U kunt de leverancier nu opdragen om de artikelen naar de klant te verzenden, bijvoorbeeld door de inkooporder als een PDF via e-mail te verzenden.     

## <a name="to-create-multiple-purchase-orders-for-drop-shipments"></a>Meerdere inkooporders voor doorverzendingen maken

U kunt ook het inkoopvoorstel gebruiken om de inkooporder voor de leverancier te maken. Het voordeel van het gebruik van het inkoopvoorstel is dat het inkooporders kan maken voor alle openstaande doorverzendingen, zodat u ze niet allemaal afzonderlijk hoeft te maken.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Inkoopvoorstellen** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Doorverzendingen** en kies vervolgens de actie **Verkooporder ophalen**.
3. Kies de knop **Ok**.
4. Bekijk de inkooporderregels en selecteer in het veld **Leveranciersnr.** de leverancier die de benodigde goederen levert. 
5. Kies de actie **Planningsboodschap uitvoeren** om beoordeelde regels om te zetten in een inkooporder.

## <a name="to-view-the-linked-purchase-order-from-the-sales-order"></a>De gekoppelde inkooporder weergeven op basis van de verkooporder

* Selecteer de verkooporderregel van de doorverzending, kies de actie **Order**, kies de actie **Doorverzending** en kies vervolgens de actie **Inkooporder**.

## <a name="to-post-a-drop-shipment"></a>Een doorverzending boeken

Nadat de leverancier de artikelen heeft verzonden, kunt u de verkooporder boeken als verzonden. U kunt de inkooporder ook boeken, maar alleen met de optie **Ontvangen**, totdat de verkooporder is gefactureerd.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.
2. Open de verkooporder die u hebt gemaakt in [Een verkooporder voor een doorverzending maken](#to-create-a-sales-order-for-drop-shipment).
3. Geef in het veld **Te verzenden aantal** op hoeveel van de orderhoeveelheid moet worden verzonden, de volledige of gedeeltelijke orderhoeveelheid.
4. Kies de actie **Boeken** of **Boeken en verzenden**.
5. Kies vervolgens **de optie Verzenden** om later te factureren of de optie **Verzenden en factureren** om meteen te factureren.

## <a name="see-also"></a>Zie ook

[Speciale orders maken:](sales-how-to-create-special-orders.md)  
[Artikelen kopen voor een verkoop](purchasing-how-purchase-products-sale.md)  
[Producten verkopen](sales-how-sell-products.md)  
[Inkopen vastleggen](purchasing-how-record-purchases.md)  
[Verkoop](sales-manage-sales.md)  
[Voorraad](inventory-manage-inventory.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]