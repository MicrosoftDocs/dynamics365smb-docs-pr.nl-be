---
title: WIP-methoden voor het berekenen en vastleggen van de voortgang van projecten
description: 'Beschrijft de verschillende OHW-methoden die u kunt gebruiken om financiële gegevens voor lopende projecten te boeken, te controleren en te berekenen die bezig zijn.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'work in process, work in progress, calculate project WIP'
ms.search.form: '1010,'
ms.date: 08/19/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="understanding-wip-methods-in-project-management"></a>Inzicht in WIP-methoden in projectmanagement

Naarmate een project vordert, worden materialen, resources en overige zaken verbruikt en moeten hiervoor boekingen plaatsvinden op het project. Onderhanden werk (OHW) is een functie waarmee u de financiële waarde van projecten in het grootboek kunt schatten gedurende de projecten. In veel gevallen kunt u kosten voor een project boeken voordat u het project factureert. Als u alleen kosten boekt, is uw financiële overzicht onjuist.

Als u de waarde in het grootboek wilt volgen, kunt u het OHW-bedrag berekenen en de waarde boeken in het grootboek. Zie voor meer informatie [Voortgang en prestaties van projecten bewaken](projects-how-monitor-progress-performance.md).

Standaard ondersteunt [!INCLUDE[prod_short](includes/prod_short.md)] de volgende methoden voor het berekenen en vastleggen van de waarde van werk in uitvoering.

| OHW-methode | Beschrijving | Verantwoorde kosten | Verantwoorde verkoop |
| --- | ------- |--- | --- |
| Kostenwaarde |Herkent de kosten wanneer de klant een factuur ontvangt. Herkent verkopen op basis van de gefactureerde verkopen. |Kostenwaarde|Contract (Factuurprijs)|
| Kosten van verkoop |Herkent de kosten wanneer de klant een factuur ontvangt. Herkent verkopen op basis van de gefactureerde verkopen.|Kosten van verkoop|Contract (gefactureerde prijs)|
| Verkoopwaarde |Herkent kosten zodra ze worden gerapporteerd. Erkent de omzet in verhouding tot de gerapporteerde kosten.|Gebruik (totale kostprijs)|Verkoopwaarde|
| Percentage van voltooiing |Herkent kosten zodra ze worden gerapporteerd. Erkent de omzet in verhouding tot de gerapporteerde kosten.|Gebruik (totale kostprijs)|Percentage van voltooiing|
| Voltooid contract |Er zijn geen verkopen of kosten opgenomen in de WIP-berekening. Bij een voltooid contract worden de opbrengsten en kosten pas erkend als het project is afgerond. Deze optie is bijvoorbeeld handig als er veel onzekerheid bestaat over de ramingen van de kosten en opbrengsten van het project.|Bij voltooiing|Bij voltooiing|

Exacte formules en grootboek-transacties worden gedefinieerd door de selectie in de velden  [**Erkende kosten**](#recognized-cost) en  [**Erkende verkopen**](#recognized-sales) .

## <a name="create-a-project-wip-method"></a>Een OHW-methode voor een project maken

Maak een OHW-methode voor een project taken die voldoet aan de behoeften van uw organisatie en stel deze in als standaard.  

> [!NOTE]
> Nadat u een methode hebt gebruikt om WIP-vermeldingen te maken, kunt u de methode niet meer wijzigen of verwijderen.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), Pictogram, voer  **project WIP Methods** in en kies vervolgens de gerelateerde koppelen.  
2. Kies de actie  **Nieuw**, selecteer de juiste waarden voor de velden  **Erkende kosten** en  **Erkende verkopen**  en vul vervolgens de overige velden in, indien nodig. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. De pagina sluiten.
4. Om deze methode de standaardmethode te maken, kiest u de ![gloeilamp die de Vertel het me-functie opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") Pictogram, voer  **projecten instellen** in en kies vervolgens de gerelateerde koppelen.  
5. Kies in het veld **Standaard OHW-methode** de methode uit de lijst.

### <a name="recognized-cost"></a>Erkende kosten

| Erkende kosten | Formule voor erkende kostenberekening | Grootboekposten |
| --- | --- | ---------- |
|Bij voltooiing|0 (nul)|Dt **Rekening erkende kosten** Cr **Rekening WIP-kosten** </br>Bedrag: Erkende kosten </br></br>Dt **WIP-kostenrekening** Cr **projectkosten toegepaste rekening** </br>Bedrag: MAX[Erkende kosten; Werkelijke (totale kosten)]|
|Kosten van verkoop|Werkelijk (totale kosten) - budget (totale kosten) * Gefactureerd%, waarbij:</br></br> Gefactureerd% = Gefactureerd (Totale prijs) / Factureerbaar (Totale prijs)</br></br>**Let op:** Voor deze berekening is het nodig dat het factureerbare bedrag (totale prijs) en het budget (totale kosten) voor het hele project correct worden ingevoerd.|Dt **Rekening erkende kosten** Cr **Rekening WIP-kosten** </br>Bedrag: Erkende kosten </br></br>Dt **WIP-kostenrekening** Cr **projectkosten toegepaste rekening** </br>Bedrag: MAX[Erkende kosten; Werkelijke (totale kosten)] </br></br>Dt **projectkosten aanpassingsrekening** Cr **WIP-opgelopen kostenrekening** </br>Bedrag: Erkende kosten – Werkelijk (totale kosten), als Erkende kosten > Werkelijk (totale kosten)|
|Kostenwaarde|Werkelijk (totale kosten) – [Voltooiing% – Gefactureerd%] * Factureerbaar (totale prijs) * budgetCostPriceRatio, waarbij: </br></br> BudgetCostPriceRatio = budget (Totale kosten) / budget (Totale prijs)</br>Gefactureerd% = Gefactureerd (Totale prijs) / Factureerbaar (Totale prijs)</br>Voltooiing% = Werkelijk (totale kosten)/budget (totale kosten)</br></br>**Let op:** Voor deze berekening is het nodig dat de Factureerbare (Totale prijs), budget (Totale prijs) en budget (Totale kosten) voor het hele project correct worden ingevoerd.|Dt **Rekening erkende kosten** Cr **Rekening WIP-kosten** </br>Bedrag: Erkende kosten</br></br>Dt **WIP-kostenrekening** Cr **projectkosten toegepaste rekening** </br>Bedrag: MAX[Erkende kosten; Werkelijke (totale kosten)] </br></br>Dt **projectkosten aanpassingsrekening** Cr **WIP-opgelopen kostenrekening** </br>Bedrag: Erkende kosten – Werkelijk (totale kosten), als Erkende kosten > Werkelijk (totale kosten)|
|Contract (gefactureerde kosten)|Gefactureerd (totale kostprijs) |Dt **Rekening erkende kosten** Cr **Rekening WIP-kosten** </br>Bedrag: Erkende kosten </br></br> Dt **WIP-kostenrekening** Cr **projectkosten toegepaste rekening** </br>Bedrag: MAX[Erkende kosten; Werkelijke (totale kosten)] </br></br>Dt **projectkosten aanpassingsrekening** Cr **WIP-opgelopen kostenrekening** </br>Bedrag: Erkende kosten – Werkelijk (totale kosten), als Erkende kosten > Werkelijk (totale kosten)|
|Gebruik (totale kostprijs)|Werkelijk (totale kosten) |Dt **Rekening erkende kosten** Cr **Rekening WIP-kosten** </br>Bedrag: Erkende kosten </br></br>Dt **WIP-kostenrekening** Cr **projectkosten toegepaste rekening** </br>Bedrag: MAX[Erkende kosten; Werkelijke (totale kosten)]|

Wanneer de projectstatus wordt gewijzigd in Voltooid, draait de  **Bereken WIP** taak de WIP-transactie terug en boekt in plaats daarvan.

Dt **Erkende kostenrekening** Cr **projectkosten toegepaste rekening**, bedrag: **Werkelijke (totale kosten)**

> [!NOTE]
> Afhankelijk van de selectie in het veld  **gebruikte WIP-boekingsmethode** kunnen de  **Rekening toegepaste artikelkosten**,  **Rekening toegepaste resourcekosten** of  **Rekening toegepaste grootboekkosten** worden gebruikt in plaats van de  **Rekening toegepaste projectkosten**. Zie  [projectboekingsgroepen](projects-how-setup-jobs.md#to-set-general-information-for-projects) voor meer informatie.

### <a name="recognized-sales"></a>Erkende verkopen

| Verantwoorde verkoop | Formule voor de berekening van erkende verkopen | Grootboekposten |
| --- | --- | ---------- |
|Bij voltooiing|0 (nul)|Dt **WIP gefactureerde verkooprekening** Cr **erkende verkooprekening** </br>Bedrag: ErkendeVerkopen</br></br>Dt **project Sales Toegepaste Account** Cr **WIP Gefactureerde Verkoop Account** </br>Bedrag: Gefactureerd (Totaalprijs)|
|Contract (gefactureerde prijs)|Gefactureerd (totale prijs)|Dt **WIP gefactureerde verkooprekening** Cr **erkende verkooprekening** </br>Bedrag: ErkendeVerkopen</br></br>Dt **project Sales Toegepaste Account** Cr **WIP Gefactureerde Verkoop Account** </br>Bedrag: Gefactureerd (Totaalprijs)|
|Gebruik (totale kostprijs)|Werkelijk (totale kosten)|Dt **WIP gefactureerde verkooprekening** Cr **erkende verkooprekening** </br>Bedrag: ErkendeVerkopen</br></br>Dt **project Sales Toegepaste Account** Cr **WIP Gefactureerde Verkoop Account** </br>Bedrag: Gefactureerd (Totaalprijs)
|Percentage van voltooiing|MIN[Factureerbaar (Totale prijs) * Voltooiings%; Factureerbaar (Totale prijs)], waarbij:</br></br>Voltooiing% = Werkelijk (totale kosten)/budget (totale kosten)</br></br>**Let op:** Voor deze berekening is het nodig dat het factureerbare bedrag (totale prijs) en het budget (totale kosten) voor het hele project correct worden ingevoerd.|Dt **WIP Accrued Sales Account** Cr **Erkende verkooprekening** </br>Bedrag: ErkendeVerkopen</br></br>Dt **project Sales Toegepaste Account** Cr **WIP Gefactureerde Verkoop Account** </br>Bedrag: Gefactureerd (Totaalprijs)|
|Gebruik (totale verkoopprijs)|Werkelijk (totale prijs)|Dt **WIP gefactureerde verkooprekening** Cr **erkende verkooprekening** </br>Bedrag: ErkendeVerkopen </br></br>Dt **project Sales Toegepaste Account** Cr **WIP Gefactureerde Verkoop Account** </br>Bedrag: MAX[Erkende verkoop; Gefactureerd (Totale prijs)]</br></br>Dt **WIP Accrued Sales Account** Cr **project Sales Adjustment Account** </br>Bedrag: MAX[ErkendeVerkopen; Gefactureerd (Totale Prijs)] - Gefactureerd (Totale Prijs)|
|Verkoopwaarde| Werkelijk (Totale prijs) * Factureerbaar (Totale prijs)/budget (Totale prijs)</br></br>**Let op:** Voor deze berekening is het nodig dat het factureerbare bedrag (totale prijs) en het budget (totale prijs) voor het hele project correct worden ingevoerd.|Dt **WIP gefactureerde verkooprekening** Cr **erkende verkooprekening** </br>Bedrag: ErkendeVerkopen</br></br>Dt **project Sales Toegepaste Account** Cr **WIP Gefactureerde Verkoop Account** </br>Bedrag: MAX[Erkende verkoop; Gefactureerd (Totale prijs)]</br></br>Dt **WIP Accrued Sales Account** Cr **project Sales Adjustment Account** </br>Bedrag: MAX[ErkendeVerkopen; Gefactureerd (Totale Prijs)] - Gefactureerd (Totale Prijs)|

Wanneer de projectstatus wordt gewijzigd in Voltooid, draait de  **Bereken WIP** taak de WIP-transactie terug en boekt in plaats daarvan.

Dt **project Sales Applied Account** Cr **Recognized Sales Account**, bedrag: **Gefactureerd (Totale prijs)**

## <a name="see-also"></a>Zie ook

[Projectbeheer](projects-manage-projects.md)  
[Financiën](finance.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
