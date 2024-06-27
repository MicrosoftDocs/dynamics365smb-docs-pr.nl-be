---
title: Foutbericht "De boekingsdatum ligt niet binnen het bereik van toegestane boekingsdatums"
description: Los de fout op achter het bericht "Boekingsdatum valt niet binnen uw bereik van toegestane boekingsdatums" bij het uitvoeren van de batchverwerking Kostprijs herwaarderen - Artikelposten.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
---

# <a name="error-message-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Foutbericht: "De boekingsdatum ligt niet binnen het bereik van toegestane boekingsdatums..."

Wanneer u de batchverwerking **Kosten aanpassen - Artikelinvoer** gebruikt, kunt u de volgende foutmelding tegenkomen:

**De boekingsdatum ligt niet binnen het bereik van toegestane boekingsdatums**

Dit bericht geeft aan dat u geen posten mag boeken voor de datum die u heeft ingevoerd. U kunt dit probleem omzeilen door uw gebruikersinstellingen te wijzigen.

## <a name="change-the-user-setup"></a>De gebruikersinstellingen wijzigen

|Gebruikers-ID  |Boeken toestaan vanaf  | Boeken toestaan tot  |
|---------|---------|--------|
|EUROPA  |  09-2020-11      |09-2020-30      |

In dit geval mag u boeken in het datumbereik van 11 september tot en met 30 september. U mag de correctiewaardepost echter niet boeken met een boekingsdatum van 10 september.  

### <a name="overview-of-the-posting-date-setup"></a>Overzicht van de instelling van de boekingsdatum

#### <a name="inventory-periods"></a>Voorraadperioden

|Einddatum  |Naam  |Gesloten  |
|---------|---------|---------|
|01-2020-31     |2020 januari      |  Ja    |
|02-2020-28     |Februari 2020     |  Ja    |
|03-2020-31     |Maart 2020        |  Ja    |
|04-2020-30     |April 2020        |  Ja    |
|05-2020-31     |Mei   2020        |  Ja    |
|06-2020-30     |Juni   2020       |  Ja    |
|07-2020-31     |Juli  2020        |   Ja   |
|08-2020-31     |Augustus  2020     |   Ja   |
|09-2020-30     |September   2020  |         |
|10-2020-31     |Oktober   2020    |         |
|11-2020-30     |November   2020   |         |
|12-2020-31     |December   2020   |         |  

#### <a name="general-ledger-setup"></a>Grootboekinstellingen

|Veld|Waarde|
|---------|---------|
|Boeken toegest. vanaf:  |  09-2020-10      |
|Boeken toegest. tot:    |  09-2020-30      |
|Registratietijd:       |         |
|Lokale adresnotatie:|   Postcode      |  

#### <a name="user-setup"></a>Gebruikersinstellingen

|Gebruikers-ID  |Boeken toegest. vanaf  | Boeken toestaan tot  |
|---------|---------|--------|
|GEBRUIKERSNAAM |  09-2020-10      |09-2020-30      |

Als een ruimer datumbereik waar boeking is toegestaan wordt toegewezen op de pagina **Voorraadperiode** of **Boekhoudinstellingen**, kan het conflict worden vermeden dat het foutbericht veroorzaakt. Dankzij het bredere bereik kunt u de correctiewaardepost bijvoorbeeld boeken met een boekingsdatum van 10 september.
  
## <a name="see-also"></a>Zie ook

[Ontwerpdetails: Boekingsdatum van herwaarderingswaardepost](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md)  
[Ontwerpdetails: Artikelvereffening](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
