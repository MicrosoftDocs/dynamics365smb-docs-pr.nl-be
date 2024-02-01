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

# Foutbericht: "De boekingsdatum ligt niet binnen het bereik van toegestane boekingsdatums..."

Bij gebruik van de batchverwerking **Kosten aanpassen - Artikelinvoer** kunt u de volgende foutmelding tegenkomen:

**De boekingsdatum ligt niet binnen het bereik van toegestane boekingsdatums**

Deze foutmelding geeft aan dat de gebruiker geen boekingen mag plaatsen voor de betreffende datum en dit kan worden verholpen door de gebruikersinstellingen te wijzigen.

## De gebruikersinstellingen wijzigen  

|Gebruikers-ID  |Boeken toegest. vanaf  | Boeken toegest. tot  |
|---------|---------|--------|
|EUROPA  |  09-2020-11      |09-2020-30      |

De gebruiker heeft in dit geval een toegestane boekingsdatumreeks van 11 september tot 30 september en mag daarom de herwaarderingswaardepost niet boeken met boekingsdatum 10 september.  

### Overzicht van betrokken instelling van boekingsdatum

#### Voorraadperioden

|Einddatum  |Name  |Gesloten  |
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

#### Grootboekinstellingen

|Veld|Waarde|
|---------|---------|
|Boeken toegest. vanaf:  |  09-2020-10      |
|Boeken toegest. tot:    |  09-2020-30      |
|Registratietijd:       |         |
|Lokale adresnotatie:|   Postcode      |  

#### Gebruikersinstellingen

|Gebruikers-ID  |Boeken toegest. vanaf  | Boeken toegest. tot  |
|---------|---------|--------|
|GEBRUIKERSNAAM |  09-2020-10      |09-2020-30      |

Als een ruimer boekingsdatumbereik wordt toegewezen, zoals in de instelling van de voorraadperiode of het grootboek, kan het conflict worden vermeden dat het foutbericht veroorzaakt. De correctiewaardepost met boekingsdatum 10 september wordt met deze instelling succesvol geboekt.
  
## Zie ook  

[Ontwerpdetails: Boekingsdatum op herwaarderingswaardepost](design-details-inventory-adjustment-value-entry-posting-date.md)  
[Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md)  
[Ontwerpdetails: Artikelvereffening](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
