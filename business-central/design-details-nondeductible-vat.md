---
title: Ontwerpdetails - Niet-aftrekbare btw
description: 'Dit artikel bevat informatie over niet-aftrekbare btw die een koper moet betalen, maar die niet aftrekbaar is van de eigen btw-aansprakelijkheid van de koper.'
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 07/04/2023
ms.author: altotovi
---

# Ontwerpdetails: niet-aftrekbare btw

Niet-aftrekbare btw is de btw die een koper moet betalen, maar die niet aftrekbaar is van de eigen btw-aansprakelijkheid van de koper. Omdat het moeilijk kan zijn om te weten waar en hoe een artikel wordt gebruikt, moet u op basis van historische gegevens contact opnemen met de lokale belastingdienst in uw land/regio om te bepalen of een bepaald percentage van de btw aftrekbaar is op basis van historische gegevens. Zelfs als u weet dat een bepaald percentage van de btw niet aftrekbaar is, zijn er verschillende modellen voor het afhandelen van niet-aftrekbare bedragen die verband houden met **artikelen** en **vaste activa**.

## Voorwaarden voor het gebruik van niet-aftrekbare btw

Volg deze stappen om niet-aftrekbare btw te gebruiken en te boeken.

1. Selecteer op de pagina **Btw-instelling** **Niet-aftrekbare btw inschakelen** om de functie in te schakelen.
2. Selecteer op de pagina **Btw-boekingsgroepinstellingen** welke btw-boekingsgroepen niet-aftrekbare btw kunnen gebruiken.

## Voorbeelden

Voor de volgende voorbeelden is niet-aftrekbare btw geactiveerd en zijn de volgende instellingen voltooid:

- Het veld **Btw-productboekingsgroep** is ingesteld op **NDVAT**.
- Op de pagina **Btw-boekingsgroepinstellingen**:

    - **NDVAT** is ingesteld als de btw-productboekingsgroep en **BINNENLAND** is ingesteld als de btw-bedrijfsboekingsgroep.
    - De waarde **Btw-identificatie** moet uniek zijn.
    - Het veld **Btw-percentage** is ingesteld op **25**.
    - Het veld **Niet-aftrekbare btw toestaan** is ingesteld op **Toestaan**.
    - Het veld **Niet-aftrekbaar btw-percentage** is ingesteld op **100**.
    - Het veld **Soort btw-berekening** is ingesteld op **Normale btw**.
    - Alleen de verkoop-btw-rekening en de inkoop-btw-rekening zijn geconfigureerd.

Alle voorbeelden gebruiken artikelen en vaste activa waarbij de btw-productboekingsgroep **NDVAT** is.

### Artikelen

Voor een nieuw artikel is **NDVAT** ingesteld als de btw-productboekingsgroep. In het aankoopdocument is **Aantal** = **1** en **Directe kostprijs excl. btw** = **1.000,00**.

Ongeacht de optie die wordt gebruikt, zijn de resultaten in de **btw-post** hetzelfde.

| Documenttype | Type | Basis | Bedrag | Niet-aftrekbare btw-basis | Niet-aftrekbaar btw-bedrag |
|---|---|---|---|---|---|
| Factureren | Inkoop |   0.00 |   0.00 | 1,000.00 | 250.00 |

De details worden weergegeven in de **waardeposten**.

> [!NOTE]
> U kunt het veld **Gebruiken voor artikelkosten** inschakelen op de pagina **Btw-instelling**.

#### Gebruiken voor artikelkosten is niet geactiveerd

| Artikelboekingssoort | Postsoort | Kostenbedrag (werkelijk) | Aantal op artikelpost |
|---|---|---|---|
| Inkoop | Directe kosten | 1,000.00 | 1 |

#### Gebruiken voor artikelkosten is geactiveerd

| Artikelboekingssoort | Postsoort | Kostenbedrag (werkelijk) | Aantal op artikelpost |
|---|---|---|---|
| Inkoop | Directe kosten | 1,250.00 | 1 |

### Vaste activa

Voor een nieuw vast activum is de aanschafkostenrekening ingesteld om **NDVAT** als de btw-productboekingsgroep te gebruiken. In het aankoopdocument is **Aantal** = **1** en **Directe kostprijs excl. btw** = **1.000,00**.

Ongeacht de optie die wordt gebruikt, zijn de resultaten in de **btw-post** hetzelfde.

| Documenttype | Type | Basis | Bedrag | Niet-aftrekbare btw-basis | Niet-aftrekbaar btw-bedrag |
|---|---|---|---|---|---|
| Factureren | Inkoop |   0.00 |   0.00 | 1,000.00 | 250.00 |

De details worden weergegeven in de **VA-posten**.

> [!NOTE]
> U kunt het veld **Gebruiken voor kosten van vaste activa** inschakelen op de pagina **Btw-instelling**.

#### Gebruiken voor kosten van vaste activa is niet geactiveerd

| Documenttype | VA-boekingssoort | Bedrag | Btw-bedrag |
|---|---|---|---|
| Factureren | Aanschafkosten | 1,000.00 | 250.00 |

#### Gebruiken voor kosten van vaste activa is geactiveerd

| Documenttype | VA-boekingssoort | Bedrag | Btw-bedrag |
|---|---|---|---|
| Factureren | Aanschafkosten | 1,000.00 | 250.00 |
| Factureren | Aanschafkosten | 250.00 |   0.00 |

## Zie ook

[Niet-aftrekbare btw instellen](finance-setup-nondeductible-vat.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
