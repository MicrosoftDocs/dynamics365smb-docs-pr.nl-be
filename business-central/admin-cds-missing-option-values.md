---
title: Ontbrekende optiewaarden verwerken
description: Leer hoe u kunt voorkomen dat volledige synchronisatie mislukt omdat de opties verschillen in toegewezen velden. Dit proces vereist de hulp van een ontwikkelaar.
author: brentholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.topic: conceptual
ms.date: 03/23/2022
---

# <a name="handling-missing-option-values"></a><a name="handling-missing-option-values"></a><a name="handling-missing-option-values"></a>Ontbrekende optiewaarden verwerken
> [!NOTE]
> In releasewave 1 van 2022 kunt u uw eigen optietoewijzingen maken. Zie [Optietoewijzingen met Microsoft Dataverse aanpassen](/dynamics365/business-central/dev-itpro/administration/administration-custom-option-mapping) voor meer informatie. De nieuwe mogelijkheden vereisen dat uw beheerder **Functie-update: toewijzen aan optiesets in Dataverse zonder code** op de pagina **Functiebeheer** inschakelt. Zie voor meer informatie [Aankomende functies van tevoren inschakelen](/dynamics365/business-central/dev-itpro/administration/feature-management).

Dit onderwerp is bedoeld voor een technisch publiek. De processen die het beschrijft, hebben de hulp van een ontwikkelaar nodig.

[!INCLUDE[prod_short](includes/cds_long_md.md)] bevat drie optiesetvelden die waarden bevatten die u kunt toewijzen aan [!INCLUDE[prod_short](includes/prod_short.md)]-velden van het type Optie, voor geautomatiseerde synchronisatie. Tijdens synchronisatie worden niet-toegewezen opties genegeerd en worden de ontbrekende opties toegevoegd aan de gerelateerde [!INCLUDE[prod_short](includes/prod_short.md)]-tabel en toegevoegd aan de systeemtabel **Dataverse-optietoewijzing** om later handmatig af te handelen. Bijvoorbeeld door de ontbrekende opties in beide producten toe te voegen en vervolgens de toewijzing bij te werken.

De pagina **Toewijzing van integratietabel** bevat drie velden die een of meer toegewezen optiewaarden bevatten. Na een volledige synchronisatie bevat de pagina **Dataverse-optietoewijzing** de niet-toegewezen opties in de drie velden.

|         Record             | Optiewaarde | Bijschrift optiewaarde |
|----------------------------|--------------|----------------------|
| Betalingsvoorwaarden: NETTO30       | 1            | Netto 30               |
| Betalingsvoorwaarden: 2%10NETTO30   | 2            | 2% 10; netto 30        |
| Betalingsvoorwaarden: NETTO45       | 3            | Netto 45               |
| Betalingsvoorwaarden: NETTO60       | 4            | Netto 60               |
| Verzendwijze: FOB       | 1            | FOB                  |
| Verzendmethode: GEENKOSTEN  | 2            | Geen kosten            |
| Expediteur: LUCHT   | 1            | Lucht             |
| Expediteur: DHL        | 2            | DHL                  |
| Expediteur: FEDEX      | 3            | FedEx                |
| Expediteur: UPS        | 4            | UPS                  |
| Expediteur: POST | 5            | Post          |
| Expediteur: VOLLEDIGELADING   | 6            | Volledige lading            |
| Expediteur: AFHALEN   | 7            | Afhalen            |

De inhoud van de pagina **Dataverse-optietoewijzing** is gebaseerd op opsommingswaarden in de tabel **CRM-account**. In [!INCLUDE[prod_short](includes/cds_long_md.md)] worden de volgende velden van de accounttabel toegewezen aan velden in de klant- en leveranciersrecords:

- **Adres 1: vrachtvoorwaarden** van het gegevenstype Enum, waar waarden als volgt worden gedefinieerd:

```
enum 5335 "CDS Shipment Method Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "FOB") { Caption = 'FOB'; }
    value(2; "NoCharge") { Caption = 'No Charge'; }
}
```

- **Adres 1: verzendmethode** van het gegevenstype Enum, waar waarden als volgt worden gedefinieerd:

```
enum 5336 "CDS Shipping Agent Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "Airborne") { Caption = 'Airborne'; }
    value(2; "DHL") { Caption = 'DHL'; }
    value(3; "FedEx") { Caption = 'FedEx'; }
    value(4; "UPS") { Caption = 'UPS'; }
    value(5; "PostalMail") { Caption = 'Postal Mail'; }
    value(6; "FullLoad") { Caption = 'Full Load'; }
    value(7; "WillCall") { Caption = 'Will Call'; }
}
```

- **Betalingsvoorwaarden** van het gegevenstype Enum, waar waarden als volgt worden gedefinieerd:

```
enum 5334 "CDS Payment Terms Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "Net30") { Caption = 'Net 30'; }
    value(2; "2%10Net30") { Caption = '2% 10; Net 30'; }
    value(3; "Net45") { Caption = 'Net 45'; }
    value(4; "Net60") { Caption = 'Net 60'; }
}
```

Alle bovenstaande [!INCLUDE[prod_short](includes/prod_short.md)]-enums zijn toegewezen aan optiesets in [!INCLUDE[prod_short](includes/cds_long_md.md)].

### <a name="extending-option-sets-in-"></a><a name="extending-option-sets-in-"></a><a name="extending-option-sets-in-"></a>Optiesets uitbreiden in [!INCLUDE[prod_short](includes/prod_short.md)]
1. Maak een nieuwe AL-extensie.

2. Voeg een Enum-extensie toe voor de opties die u wilt uitbreiden. Zorg ervoor dat u dezelfde waarde gebruikt. 

```
enumextension 50100 "CDS Payment Terms Code Extension" extends "CDS Payment Terms Code"
{
    value(779800001; "Cash Payment") { Caption = 'Cash Payment'; }
    value(779800002; "Transfer") { Caption = 'Transfer'; }
}
```

> [!IMPORTANT]  
> U moet dezelfde optie-ID-waarden gebruiken van [!INCLUDE[prod_short](includes/cds_long_md.md)] wanneer u de [!INCLUDE[prod_short](includes/prod_short.md)]-enum uitbreidt. Anders mislukt de synchronisatie.

> [!IMPORTANT]  
> Gebruik niet het teken "," in de Enum-waarden en bijschriften. Dit wordt momenteel niet ondersteund door de [!INCLUDE[prod_short](includes/prod_short.md)]-runtime.

> [!NOTE]
> De eerste tien tekens van de nieuwe namen en bijschriften van de optiewaarden moeten uniek zijn. Twee opties met de naam "Transfer 20 werkdagen" en "Transfer 20 kalenderdagen" veroorzaken bijvoorbeeld een fout omdat beide dezelfde eerste 10 tekens hebben, "Transfer 2". Noem ze bijvoorbeeld "TRF20 WD" en "TRF20 KD".

### <a name="update--option-mapping"></a><a name="update--option-mapping"></a><a name="update--option-mapping"></a>[!INCLUDE[prod_short](includes/cds_long_md.md)]-optietoewijzing bijwerken
Nu kunt u de toewijzing opnieuw maken tussen [!INCLUDE[prod_short](includes/cds_long_md.md)]-opties en [!INCLUDE[prod_short](includes/prod_short.md)]-records.

Kies op de pagina **Toewijzing van integratietabel** de regel voor de toewijzing **Betalingsvoorwaarden** en kies vervolgens de actie **Gewijzigde records synchroniseren**. De pagina **Dataverse-optietoewijzing** wordt bijgewerkt met de aanvullende records hieronder.

|         Record                 | Optiewaarde   | Bijschrift optiewaarde |
|--------------------------------|----------------|----------------------|
| Betalingsvoorwaarden: NETTO30           | 1              | Netto 30               |
| Betalingsvoorwaarden: 2%10NETTO30       | 2              | 2% 10; netto 30        |
| Betalingsvoorwaarden: NETTO45           | 3              | Netto 45               |
| Betalingsvoorwaarden: NETTO60           | 4              | Netto 60               | 
| **Betalingsvoorwaarden: CONTANTE BETALING**  | **779800001**  | **Contante betaling**     |
| **Betalingsvoorwaarden: TRANSFER**    | **779800002**  | **Transfer**         |

De tabel **Betalingsvoorwaarden** in [!INCLUDE[prod_short](includes/prod_short.md)] bevat dan nieuwe records voor de [!INCLUDE[prod_short](includes/cds_long_md.md)]-opties. In de volgende tabel zijn nieuwe opties vetgedrukt. Cursieve rijen vertegenwoordigen alle opties die nu kunnen worden gesynchroniseerd. Resterende rijen vertegenwoordigen opties die niet in gebruik zijn en worden genegeerd tijdens synchronisatie. U kunt deze verwijderen of Dataverse-opties met dezelfde namen uitbreiden.

| Code       | Vervaldatumberekening | Kortingsdatumberekening | Korting % | Contantkorting op creditnota's berekenen | Omschrijving       |
|------------|----------------------|---------------------------|------------|-------------------------------|-------------------|
| 10 DAGEN    | 10D                  |                           | 0.         | ONWAAR                         | Netto 10 dagen       |
| 14 DAGEN    | 14D                  |                           | 0.         | ONWAAR                         | Netto 14 dagen       |
| 15 DAGEN    | 15D                  |                           | 0.         | ONWAAR                         | Netto 15 dagen       |
| 1M(8D)     | 1M                   | 8D                        | 2.         | ONWAAR                         | 1 maand/2% 8 dagen |
| 2 DAGEN     | 2D                   |                           | 0.         | ONWAAR                         | Netto 2 dagen        |
| *2%10NETTO30* |                      |                           | 0.         | ONWAAR                         |                   |
| 21 DAGEN    | 21D                  |                           | 0.         | ONWAAR                         | Netto 21 dagen       |
| 30 DAGEN    | 30D                  |                           | 0.         | ONWAAR                         | Netto 30 dagen       |
| 60 DAGEN    | 60D                  |                           | 0.         | ONWAAR                         | Netto 60 dagen       |
| 7 DAGEN     | 7D                   |                           | 0.         | ONWAAR                         | Netto 7 dagen        |
| ***CONTANTE BETALING*** |                      |                           | 0.         | ONWAAR                         |                   |
| LM         | LM                   |                           | 0.         | ONWAAR                         | Lopende maand     |
| REMBOURS        | 0D                   |                           | 0.         | ONWAAR                         | Rembours  |
| *NETTO 30*      |                      |                           | 0.         | ONWAAR                         |                   |
| *NETTO45*      |                      |                           | 0.         | ONWAAR                         |                   |
| *NETTO60*      |                      |                           | 0.         | ONWAAR                         |                   |
| ***TRANSFER*** |                      |                           | 0.         | ONWAAR                         |                   |

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Zie ook
[De te synchroniseren tabellen en velden toewijzen](admin-how-to-modify-table-mappings-for-synchronization.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
