---
title: Boekingsdatum in waardeposten
description: Leren hoe de batchverwerking Kostprijs herwaarderen - Artikelposten een boekingsdatum bepaalt en toewijst aan de waardeposten die de batchverwerking gaat maken.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 09/17/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a>Ontwerpdetails: Boekingsdatum op herwaarderingswaardepost

Dit artikel biedt richtlijnen voor gebruikers van de functionaliteit Voorraadwaardering in [!INCLUDE[prod_short](includes/prod_short.md)] en in het bijzonder voor hoe de batchverwerking **Kostprijs herwaarderen - Artikelposten** een boekingsdatum identificeert en toewijst aan de waardeposten die de batchtaak gaat maken.

## <a name="how-posting-dates-are-assigned"></a>Hoe boekingsdatums worden toegewezen

De batchverwerking **Kostprijs herwaarderen - Artikelposten** wijst een boekingsdatum toe aan de waardepost die gaat worden gemaakt in de volgende stappen:  

1. Eerst is de boekingsdatum van de post die wordt gemaakt, hetzelfde als de datum van de post die wordt aangepast.  

2. De boekingsdatum wordt gevalideerd tegen voorraadperioden en/of boekhoudinstellingen.  

3. Toewijzing van boekingsdatum; als de oorspronkelijke boekingsdatum niet binnen het toegestane boekingsdatumbereik ligt, wijst de batchverwerking een toegestane boekingsdatum uit Boekhoudinstellingen of Voorraadperiode toe. Als zowel voorraadperioden als toegestane boekingsdatums in grootboekinstellingen zijn gedefinieerd, wordt de latere datum van de twee toegewezen aan de herwaarderingswaardepost.  

Laten we dit proces eens in de praktijk bekijken. Stel dat we een artikelpost Verkoop hebben. Het artikel is verzonden op 5 september 2020 en de dag erna gefactureerd.  

#### <a name="item-ledger-entry"></a>Artikelpost

|Postnr.  |Artikelnr.  |Boekingsdatum  |Postsoort  | Documentnr. |Vestigingscode  |Hoeveelheid  |Kostenbedrag (werkelijk)  |Gefact. aantal  |Resterend aantal  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|319     |A         |2020-09-05     |  Verkoop       |102033     |  Blauw       | -1    |    -11     |-1     |    0     |

Hieronder staan de gerelateerde waardeposten:

- **Postnr. 379** vertegenwoordigt de verzending en heeft dezelfde boekingsdatum als de bovenliggende artikelpost.  
- **Postnr. 381** vertegenwoordigt de factuur.  
- **Postnr. 391** is een herwaardering van de factuurwaardepost (postnr. 381 hierboven).  

|Postnr.  |Artikelnr.  |Boekingsdatum  |Artikelboekingssoort  |Postsoort  |Documentnr.  |Artikelpostnr.  |Vestigingscode  |Aantal op artikelpost  |Gefact. aantal  |Kostenbedrag (werkelijk)  |Kostenbedrag (Verw.)  |Aanpassing  |Vereffenen met post  |Broncode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|--------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Verkoop     | Directe kosten   | 102033        |319     | Blauw        | -1       |0         |  0       |     -10   |Nr.   |0    |Verkoop          |
|381     |  A       |    2020-09-06     |    Verkoop     | Directe kosten   | 103022        |319     | Blauw        |  0       |-1        |-10       |    10     | Nr.  |0      |       Verkoop   |
|391     |  A       |    2020-09-10     |    Verkoop     | Directe kosten   | 103022        |319     | Blauw        |  0       |0         |-1        |    0     |Ja   |    181   | VRDWAARDNG   |

Om de boekingsdatum toe te wijzen voor **Postnr. 391** zijn de volgende stappen toegepast:

1. De te maken **herwaarderingspost** (**postnr. 391**) krijgt dezelfde **boekingsdatum** toegewezen als de post die ermee wordt geherwaardeerd.

2. De batchverwerking **Kostprijs herwaarderen - Artikelposten** bepaalt of de oorspronkelijke boekingsdatum van de herwaarderingswaardepost binnen het toegestane boekingsdatumbereik ligt, op basis van voorraadperioden en/of boekhoudinstellingen.  

Laten we de hierboven genoemde Verkoop bekijken door instelling van toegestane boekingsdatumbereiken toe te voegen.  
  
#### <a name="inventory-periods"></a>Voorraadperioden

|Einddatum  |Naam  |Gesloten  |
|---------|---------|---------|
|2020-01-31     |2020 januari      |  Ja    |
|2020-02-28     |Februari 2020     |  Ja    |
|2020-03-31     |Maart 2020        |  Ja    |
|2020-04-30     |April 2020        |  Ja    |
|2020-05-31     |Mei   2020        |  Ja    |
|2020-06-30     |Juni   2020       |  Ja    |
|2020-07-31     |Juli  2020        |  Ja    |
|2020-08-31     |Augustus  2020     |  Ja    |
|2020-09-30     |September   2020  |         |
|2020-10-31     |Oktober   2020    |         |
|2020-11-30     |November   2020   |         |
|2020-12-31     |December   2020   |         |

De eerste toegestane boekingsdatum is de eerste dag van de eerste open periode, namelijk 1 september 2020.  

#### <a name="general-ledger-setup"></a>Grootboekinstellingen

|Veld|Waarde  |
|---------|---------|
|Boeken toegest. vanaf:  |  2020-09-10      |
|Boeken toegest. tot:    |  2020-09-30      |
|Registratietijd:       |         |
|Lokale adresnotatie:|   Postcode      |  

De eerste toegestane boekingsdatum is de datum in het veld **Boeken toegest. vanaf**: 10 september 2020. Als zowel voorraadperioden als toegestane boekingsdatums in **grootboekinstellingen** zijn gedefinieerd, definieert de latere datum van de twee het toegestane boekingsdatumbereik.  

**Toewijzing van een toegestane boekingsdatum**  

De aanvankelijke toegewezen Boekingsdatum was 6 september, zoals in stap 1 wordt beschreven. Echter, in de tweede stap identificeert de batchverwerking Kostprijs herwaarderen - Artikelposten dat de vroegste toegestane boekingsdatum 10 september is en wijst dus 10 september toe aan de herwaarderingswaardepost, onder (**postnr. 391**).  


|Postnr.  |Artikelnr.  |Boekingsdatum  |Artikelboekingssoort  |Postsoort  |Documentnr.  |Artikelpostnr.  |Vestigingscode  |Aantal op artikelpost  |Gefact. aantal  |Kostenbedrag (werkelijk)  |Kostenbedrag (Verw.)  |Aanpassing  |Vereffenen met post  |Broncode  |
|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|---------|
|379     |  A       |    2020-09-05     |    Verkoop     | Directe kosten   | 102033        |319     | Blauw        | -1       |0         |  0       |     -10   |Nr.   |0    |Verkoop          |
|381     |  A       |    2020-09-06     |    Verkoop     | Directe kosten   | 103022        |319     | Blauw        |  0       |-1        |-10       |    10     | Nr.  |0      |       Verkoop   |
|391     |  A       |    **2020-09-10**     |    Verkoop     | Directe kosten   | 103022        |319     | Blauw        |  0       |0         |-1        |    0     |Ja   |    181   | VRDWAARDNG   |

## <a name="common-problems-with-the-adjust-cost---item-entries-batch-job"></a>Veelvoorkomende problemen met de batchverwerking Kostprijs herwaarderen - Artikelposten

Er zijn twee scenario's die het ondersteuningsteam vaak genoeg tegenkomt om hun eigen probleemoplossingsartikelen te rechtvaardigen.

### <a name="error-message-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a>Foutbericht: "De boekingsdatum ligt niet binnen het bereik van toegestane boekingsdatums..."

Als u deze fout tegenkomt, moet u de datums aanpassen waarop de gebruiker boekingen mag plaatsen. Zie voor meer informatie [Foutbericht "De boekingsdatum ligt niet binnen het bereik van toegestane boekingsdatums"](design-details-inventory-adjustment-value-entry-allowed-posting-dates.md).

### <a name="posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a>Boekingsdatum op Herwaarderingswaardepost versus Boekingsdatum op post die de correctie veroorzaakt, zoals Herwaardering of Artikeltoeslag

Zie voor meer informatie [Boekingsdatum op correctiewaardepost in vergelijking met de bronpost](design-details-inventory-adjustment-value-entry-source-entry.md).

## <a name="see-also"></a>Zie ook

[Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md)  
[Ontwerpdetails: Artikelvereffening](design-details-item-application.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
