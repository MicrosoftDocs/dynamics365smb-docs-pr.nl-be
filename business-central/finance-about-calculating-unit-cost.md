---
title: Over kostprijsberekening
description: Ontdek hoe de waarderingsmethode en andere factoren het veld Kostprijs op de artikelkaart beïnvloeden.
author: brentholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 03/06/2022
ms.author: bholtorf
---
# <a name="about-unit-cost-calculation"></a>Over kostprijsberekening

Elk artikel heeft een eenheidsprijs die wordt berekend op basis van de waarderingsmethode van het bedrijf en andere factoren. In het algemeen wordt de waarde van het veld **Kostprijs** met de waarderingsmethode *Standaard* gebaseerd op de vaste verrekenprijs van het artikel. Voor alle andere berekeningsmethoden (*FIFO*, *LIFO*, *Specifiek* en *Gemiddeld*), wordt de kostprijs berekend op basis van de gemiddelde kostprijs over een bepaalde periode.  

Zie [Voorraadkosten beheren](finance-manage-inventory-costs.md) voor meer informatie.  

## <a name="when-is-the-unit-cost-field-updated"></a>Wanneer het kostprijsveld wordt bijgewerkt

De gekozen berekeningsmethode beïnvloedt wanneer het veld **Kostprijs** wordt bijgewerkt.

Wanneer de kostprijsberekeningsmethode is ingesteld als *Standaard*, wordt het veld **Kostprijs** bijgewerkt wanneer de vaste verrekenprijs wordt gewijzigd en kunnen gebruikers het veld **Kostprijs** niet bewerken. Zie [Vaste verrekenprijs bijwerken](finance-how-to-update-standard-costs.md) voor meer informatie.

Als de waarderingsmethode *FIFO*, *LIFO*, *Specifiek* of *Gemiddeld* is, wordt het veld **Kostprijs** in de volgende gevallen bijgewerkt:

* Wanneer de kosten van het artikel worden aangepast, automatisch of door een [Kostprijs herwaarderen:](inventory-how-adjust-item-costs.md#to-adjust-item-costs-manually)-taak.
* Als tijdens het boeken van inkoopfacturen, uitvoer of positieve herwaardering aan een van de volgende voorwaarden wordt voldaan:
  * Het geboekte aantal van het artikel verandert van negatief of nul in positief.
  * De huidige kostprijs is nul.

Als aan een van deze voorwaarden wordt voldaan, wordt het veld **Kostprijs** bijgewerkt met de waarde in het veld **Laatste directe kosten** op de artikelkaart.

> [!NOTE]
> Het veld **Kostprijs** wordt niet bijgewerkt als de huidige kostprijs hoger is dan nul en de nieuwe kostprijs nul is. Een kostprijs van nul wordt beschouwd als een uitzondering op de reguliere bedrijfsvoering. Daarom wordt de huidige kostprijs behouden om de laatst bekende, relevante waarde te leveren. Deze uitzondering geldt zelfs als de bestaande voorraad op nul is geherwaardeerd.

In het veld **Kostprijs** op de artikelkaart kunt u inzoomen om de transactiehistorie te bekijken waaruit de gemiddelde kostprijs van voorraad wordt berekend in het venster **Overzicht gemiddelde-kostenberekening**.

## <a name="unit-cost-calculation-for-purchases"></a>Kostprijsberekening voor inkopen

Wanneer u artikelen inkoopt, wordt de waarde in het veld **Laatste directe kosten** op de artikelkaart naar het veld **Directe kostprijs** op een inkoopregel of de regel **Eenheidsprijs** op een artikeldagboekregel gekopieerd.

Wat u in het veld **Waarderingsmethode** invult, beïnvloedt hoe [!INCLUDE[prod_short](includes/prod_short.md)] de inhoud van het veld **Kostprijs** berekent op de regels.

### <a name="costing-method-fifo-lifo-specific-or-average"></a>Waarderingsmethode FIFO, LIFO, Specifiek of Gemiddeld

De inhoud van het veld **Kostprijs (LV)** op de inkoopregel of het veld **Kostprijs** op de artikeldagboekregel wordt door [!INCLUDE[prod_short](includes/prod_short.md)] berekend volgens deze formule:

*Kostprijs (LV) = (Directe kostprijs - (Kortingsbedrag/Aantal)) x (1 + Indirecte kosten % / 100) + Overheadtarief*

### <a name="costing-method-standard"></a>Waarderingsmethode Standaard

De waarde in het veld **Kostprijs** op de artikelkaart wordt naar het veld **Kostprijs (LV)** op de inkoopregel of het veld **Kostprijs** op de artikeldagboekregel gekopieerd. Wanneer de waarderingsmethode *Standaard* is ingesteld, is deze altijd gebaseerd op de vaste verrekenprijs.

Wanneer u de aankoop boekt, gebruikt [!INCLUDE[prod_short](includes/prod_short.md)] de kostprijs van de inkoopregel of artikeldagboekregel voor de inkoopartikelfactuurpost. U kunt het zien in het overzicht met posten voor het artikel.

### <a name="all-costing-methods"></a>Alle waarderingsmethoden

De inhoud van het veld **Tot. werk. kosten** of, indien van toepassing, het veld **Tot. verw. kosten** voor deze artikelpost wordt altijd berekend op basis van de kostprijs van de brondocumentregel, ongeacht de waarderingsmethode van het artikel.

## <a name="unit-cost-calculation-for-sales"></a>Kostprijsberekening voor verkopen

Wanneer u artikelen verkoopt, wordt de kostprijs altijd uit het veld **Kostprijs** op de artikelkaart naar de verkoopregel of de artikeldagboekregel gekopieerd.

Tijdens het boeken wordt de kostprijs naar de verkoopfactuurpost gekopieerd en weergegeven in het overzicht met artikelposten. De inhoud van het veld **Tot. werk. kosten** of indien van toepassing het veld **Tot. verw. kosten** in de waardepost voor deze artikelpost wordt door [!INCLUDE[prod_short](includes/prod_short.md)] berekend op basis van de kostprijs van de brondocumentregel.

## <a name="see-also"></a>Zie ook

[Voorraadkosten beheren](finance-manage-inventory-costs.md)  
[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Over voorraadwaardering](finance-learn-about-costing.md)  
[Voorraad](inventory-manage-inventory.md)  
[Verkoop](sales-manage-sales.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Ontwerpdetails: Niet-aftrekbare btw](design-details-nondeductible-vat.md)
[Aanbevolen procedures instellen: Waarderingsmethode](setup-best-practices-costing-method.md)  
[Ontwerpdetails: Waarderingsmethoden](design-details-costing-methods.md)  
[Ontwerpdetails: Kostenwaardering](design-details-cost-adjustment.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
