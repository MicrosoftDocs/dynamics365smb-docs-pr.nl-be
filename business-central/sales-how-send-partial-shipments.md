---
title: Deelverzendingen verwerken
description: Verzendingen van verkooporders kunnen in Business Central worden verwerkt met deelverzendingen met behulp van Verzendadvies en Te verzenden aantal.
author: brentholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: 'shipping advice, partial shipments, partial deliveries, trade, customer sales order'
ms.date: 08/12/2022
ms.author: bholtorf
---
# <a name="process-partial-shipments"></a>Deelverzendingen verwerken

Bij een deelverzending wordt een order niet allemaal tegelijk verzonden. Bij een order voor 100 eenheden verzendt u bijvoorbeeld 40 eenheden direct en 60 eenheden later. U kunt een onbeperkt aantal verzendingen voor een order maken.

Voordat u echter deelverzendingen kunt gebruiken in [!INCLUDE [prod_short](includes/prod_short.md)], moet u aangeven dat de klant deelverzendingen accepteert door het veld **Verzendadvies** in te stellen op de pagina **Klantenkaart**. Als de klant gewoonlijk alleen volledige zendingen accepteert, maar vervolgens verzoekt om of akkoord gaat met een deelverzending voor een specifieke verkooporder, kunt u het veld **Verzendadvies** wijzigen voordat u boekt.

Standaard stelt [!INCLUDE [prod_short](includes/prod_short.md)] het veld op de pagina **Klantenkaart** in op **Gedeeltelijk**, wat deelverzendingen mogelijk maakt. Als het veld echter is aangepast om **Compleet** op te geven, is het veld **Te verzenden aantal** geblokkeerd in verkooporders voor die klant.

[!INCLUDE [order-ship-invoice_md](includes/order-ship-invoice.md)]

## <a name="see-also"></a>Zie ook

[Producten verkopen met een klantverkooporder](sales-how-sell-products.md)  
[Artikelen verzenden](warehouse-how-ship-items.md)  
[Doorverzendingen uitvoeren](sales-how-drop-shipment.md)  
[Verkoop](sales-manage-sales.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Beheer](admin-setup-and-administration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
