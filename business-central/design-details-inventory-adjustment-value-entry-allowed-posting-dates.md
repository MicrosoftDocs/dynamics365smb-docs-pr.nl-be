---
title: Foutbericht "De boekingsdatum ligt niet binnen het bereik van toegestane boekingsdatums"
description: Los de fout op achter het bericht "Boekingsdatum valt niet binnen uw bereik van toegestane boekingsdatums" bij het uitvoeren van de batchverwerking Kostprijs herwaarderen - Artikelposten.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="error-message-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Foutbericht: "De boekingsdatum ligt niet binnen het bereik van toegestane boekingsdatums..."

Bij gebruik van de batchverwerking **Kosten aanpassen - Artikelinvoer** kunt u de volgende foutmelding tegenkomen:

**De boekingsdatum ligt niet binnen het bereik van toegestane boekingsdatums**

Deze foutmelding geeft aan dat de gebruiker geen boekingen mag plaatsen voor de betreffende datum en dit kan worden verholpen door de gebruikersinstellingen te wijzigen.

## <a name="change-the-user-setup"></a>De gebruikersinstellingen wijzigen

|Gebruikers-ID  |Boeken toestaan vanaf  | Boeken toestaan tot  |
|---------|---------|--------|
|EUROPA  |  2020-09-11      |2020-09-30      |

De gebruiker heeft in dit geval een toegestane boekingsdatumreeks van 11 september tot 30 september en mag daarom de herwaarderingswaardepost niet boeken met boekingsdatum 10 september.  

### <a name="overview-of-the-posting-date-setup"></a>Overzicht van betrokken instelling van boekingsdatum

#### <a name="inventory-periods"></a>Voorraadperioden

|Einddatum  |Naam  |Gesloten  |
|---------|---------|---------|
|2020-01-31     |2020 januari      |  Ja    |
|2020-02-28     |Februari 2020     |  Ja    |
|2020-03-31     |Maart 2020        |  Ja    |
|2020-04-30     |April 2020        |  Ja    |
|2020-05-31     |Mei   2020        |  Ja    |
|2020-06-30     |Juni   2020       |  Ja    |
|2020-07-31     |Juli  2020        |   Ja   |
|2020-08-31     |Augustus  2020     |   Ja   |
|2020-09-30     |September   2020  |         |
|2020-10-31     |Oktober   2020    |         |
|2020-11-30     |November   2020   |         |
|2020-12-31     |December   2020   |         |  

#### <a name="general-ledger-setup"></a>Grootboekinstellingen

|Veld|Waarde|
|---------|---------|
|Boeken toegest. vanaf:  |  2020-09-10      |
|Boeken toegest. tot:    |  2020-09-30      |
|Registratietijd:       |         |
|Lokale adresnotatie:|   Postcode      |  

#### <a name="user-setup"></a>Gebruikersinstellingen

|Gebruikers-ID  |Boeken toestaan vanaf  | Boeken toestaan tot  |
|---------|---------|--------|
|GEBRUIKERSNAAM |  2020-09-10      |2020-09-30      |

Als een ruimer boekingsdatumbereik wordt toegewezen, zoals in de instelling van de voorraadperiode of het grootboek, kan het conflict worden vermeden dat het foutbericht veroorzaakt. De correctiewaardepost met boekingsdatum 10 september wordt met deze instelling succesvol geboekt.
  
## <a name="see-also"></a>Zie ook

[Ontwerpdetails: Boekingsdatum van herwaarderingswaardepost](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md)  
[Ontwerpdetails: Artikelvereffening](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
