---
title: Automatische vereffening gebruiken om betalingen te reconciliëren | Microsoft Docs
description: Beschrijft hoe u de automatische vereffeningsfunctie gebruikt om betalingen of kasontvangsten te vereffenen met de gerelateerde openstaande posten, en om betalingen te reconciliëren.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 16241459bd080b7f1982a42110a834433d9427ea
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1252102"
---
# <a name="reconcile-payments-using-automatic-application"></a>Betalingen reconciliëren met automatische vereffening
Op de pagina **Dagboek betalingsreconciliatie** worden inkomende of uitgaande betalingen opgegeven die als transacties zijn vastgelegd op uw online bankrekening en die u kunt vereffenen met de gerelateerde openstaande, klant-, leveranciers- en bankrekeningposten. De dagboekregels worden ingevuld door een bankafschrift als een bankfeed of bestand te importeren.

> [!NOTE]
> De pagina biedt automatische afstemmingsfunctionaliteit waarmee betalingen worden vereffend met de gerelateerde open posten op basis van een afstemming van tekst op een bankafschriftregel (dagboekregel) met tekst in een of meer open posten. U kunt de voorgestelde automatische vereffeningen overschrijven en u kunt ervoor kiezen helemaal geen automatische vereffening te gebruiken. Zie stap 7 voor meer informatie.

Een betalingsreconciliatiedagboek is gerelateerd aan één bankrekening in [!INCLUDE[d365fin](includes/d365fin_md.md)] waarmee de online bankrekening wordt weergegeven waarin de betalingstransacties worden vastgelegd. Eventuele open bankrekeningposten die gerelateerd zijn aan de vereffende klant- of leveranciersposten, worden gesloten wanneer u de actie **Betalingen boeken en bankrekening reconciliëren** kiest. Dit betekent dat de bankrekening automatisch wordt gereconcilieerd voor betalingen die u met het dagboek boekt.

Als u bankafschriften als bankfeeds wilt importeren, moet u eerst de service Envestnet Yodlee Bank Feeds instellen en vervolgens de bankrekening aan de gerelateerde online bankrekening koppelen. Het dagboek van de betalingreconciliatie detecteert vervolgens automatisch bankfeeds wanneer u de actie **Banktransacties importeren** kiest. Bovendien kunt u een bankrekening zo instellen dat automatisch elk uur nieuwe bankafschriftfeeds worden geïmporteerd. Transacties voor betalingen die reeds zijn geboekt als vereffend en/of gereconcilieerd worden niet geïmporteerd. Zie voor meer informatie [De service Envestnet Yodlee Bank Feeds instellen](bank-how-setup-bank-statement-service.md).

Met de actie **Tekst afstemmen op rekening** kunt u toewijzingen instellen tussen tekst op betalingen en specifieke debet-, credit- en tegenrekeningen zodat dergelijke betalingen worden geboekt naar de opgegeven rekeningen wanneer u het betalingsreconciliatiedagboek boekt. Zie stap 8. Zie [Tekst op herhalende betalingen aan rekeningen toewijzen voor automatisch reconciliëren](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) voor meer informatie.

Er bestaat vergelijkbare functionaliteit om te grote bedragen op de dagboekregels voor betalingreconciliatie op ad-hocbasis te reconciliëren. Zie [Betalingen reconciliëren die niet kunnen worden vereffend](receivables-how-reconcile-payments-cannot-apply-auto.md) voor meer informatie.

U gebruikt de functie **Automatisch vereffenen** automatisch wanneer u een bankbestand of -feed met betalingstransacties importeert of wanneer u de functie activeert, om betalingen te vereffenen met de gerelateerde openstaande posten op basis van een afstemming van tekst op een bankafschriftregel (dagboekregel) met tekst in een of meer openstaande posten.

Op dagboekregels waar een betaling automatisch is vereffend met een of meer openstaande posten, heeft het veld **Zekerheid afstemming** een waarde tussen Laag en Hoog om de kwaliteit aan te geven van de gegevensafstemming waarop de voorgestelde betalingsvereffening is gebaseerd. Bovendien worden de velden **Rekeningtype** en **Rekeningnr.** gevuld met informatie over de klant of leverancier waarmee de betaling wordt vereffend. Als u geen tekst-naar-rekening toewijzing hebt ingesteld, kan de automatische vereffening leiden tot de afstemmingszekerheidswaarde **Hoog - Tekst-aan-rekening toewijzing**.

Voor elke dagboekregel op de pagina **Dagboek betalingsreconciliatie** kunt u de pagina **Betalingsvereffening** openen om alle openstaande kandidaatposten voor de betaling te zien en gedetailleerde informatie voor elke post weer te geven over de gegevensafstemming waarop een betalingsvereffening wordt gebaseerd. Hier kunt u handmatig betalingen vereffenen of betalingen die automatisch met een verkeerde post zijn vereffend, opnieuw vereffenen. Zie [Betalingen controleren of vereffenen na automatische vereffening](receivables-how-review-apply-payments-auto-application.md) voor meer informatie.

> [!NOTE]  
> U kunt het importeren van banktransacties starten op het moment dat u de pagina **Betalingsreconciliatiedagboek** opent voor een bestaand betalingsreconciliatiedagboek op de pagina **Betalingsreconciliatiedagboeken**. In de volgende procedure wordt beschreven hoe u banktransacties importeert op de pagina **Dagboek betalingsreconciliatie** nadat u een nieuw dagboek hebt gemaakt.

## <a name="to-reconcile-payments-using-automatic-application"></a>Betalingen reconciliëren met automatische vereffening
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsreconciliatiedagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Als u in een nieuw betalingsreconciliatiedagboek wilt werken, kiest u de actie **Nieuw dagboek**.
3. Selecteer op de pagina **Bankrekeninglijst betaling** de bankrekening waarvoor u betalingen wilt vereffenen en kies vervolgens de knop **OK**.
   De pagina **Dagboek betalingsreconciliatie** wordt geopend en is voorbereid op de geselecteerde bankrekening.
4. Kies de actie **Banktransacties importeren**.
   Als de bankrekening voor het geselecteerde dagboek niet is ingesteld voor het importeren van banktransacties, wordt een dialoogvenster geopend om u te helpen de relevante velden in te vullen.
5. Selecteer op de pagina **Te importeren bestand selecteren** het bestand dat banktransacties voor betalingen bevat die u wilt reconciliëren, en kies vervolgens de knop **Openen**.  
6. Als de bankafschriftservice is ingeschakeld, wordt op de pagina **Bankafschriftfilter** die automatisch wordt geopend, het datuminterval opgegeven voor de bankafschriften die moeten worden geïmporteerd.

    De pagina **Dagboek betalingsreconciliatie** wordt gevuld met regels voor betalingen die banktransacties in het bankafschrift vertegenwoordigen.

    Op regels voor betalingen die automatisch zijn vereffend met de gerelateerde openstaande posten ervan, heeft het veld **Zekerheid afstemming** een waarde tussen **Laag** en **Hoog** om de kwaliteit aan te geven van de gegevensafstemming waarop de voorgestelde betalingsvereffening is gebaseerd. Bovendien worden de velden **Rekeningtype** en **Rekeningnr.** gevuld met informatie over de klant of leverancier waarmee de betaling wordt vereffend.
7. Selecteer een dagboekregel en kies vervolgens de actie **Handmatig afstemmen** om de betaling handmatig te bekijken, opnieuw te vereffenen of te vereffenen op de pagina **Betalingsvereffening**. Zie [Betalingen controleren of vereffenen na automatische vereffening](receivables-how-review-apply-payments-auto-application.md) voor meer informatie.

    Als u klaar bent met de handmatige vereffening, bevat het veld **Zekerheid afstemming** op de dagboekregel die u handmatig hebt verwerkt, **Goedgekeurd**.
8. Selecteer een niet-vereffende dagboekregel voor een periodieke ontvangst of periodieke kosten, zoals een aankoop van autobenzine, en kies vervolgens de actie **Tekst afstemmen op rekening**. Zie [Tekst op herhalende betalingen aan rekeningen toewijzen voor automatisch reconciliëren](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) voor meer informatie.
9. Wanneer u de toewijzing van betalingstekst aan rekeningen hebt voltooid, kiest u de actie **Handmatig vereffenen**.
10. Wanneer u tevreden bent dat alle betalingen op de dagboekregels correct worden vereffend of zijn ingesteld op direct boeken, kiest u de actie **Boeken** en kiest u vervolgens een van de opties:

    - **Betalingen boeken en bankrekening reconciliëren** - Om de betalingen te boeken als vereffend en ook de gerelateerde bankposten te sluiten als gereconcilieerd.
    - **Alleen betalingen boeken** - Om alleen de betalingen te boeken als vereffend, maar de gerelateerde bankrekeningposten open te laten. Vereist dat u de bankrekening afzonderlijk reconcilieert, bijvoorbeeld: zie voor meer informatie [Bankrekeningen apart reconciliëren](bank-how-reconcile-bank-accounts-separately.md).
    - **Testrapport** - Als u het resultaat van de boeking wilt controleren voordat u boekt. Het rapport **Bankrekeningafschrift** wordt geopend en bevat dezelfde velden als de onderzijde van de pagina **Betalingsreconciliatiedagboek**.

Als u het dagboek van de betalingsreconciliatie boekt, worden de vereffende openstaande-postennota's gesloten en worden de gerelateerde klant-, leverancier- of grootboekrekeningen bijgewerkt. Voor betalingen op dagboekregels die zijn gebaseerd op tekst-aan-rekening toewijzing, worden de opgegeven klant-, leveranciers- en grootboekrekeningen bijgewerkt. Voor alle dagboekregels worden bankposten gemaakt. Als u de actie **Betalingen boeken en bankrekening reconciliëren** kiest, worden eventuele open bankrekeningposten gesloten die zijn gerelateerd aan de vereffende klant- of leveranciersposten. Dit betekent dat de bankrekening automatisch wordt gereconcilieerd voor betalingen die u met het dagboek boekt.

U kunt de waarde in het veld **Saldo op bankrekening na boeking** met de waarde in het veld **Eindsaldo afschrift** vergelijken om te traceren wanneer de bankrekening wordt gereconcilieerd op basis van betalingen die u boekt.

> [!NOTE]  
>   Als u de bankrekening vanuit de pagina **Betalingsreconciliatiedagboek** niet wilt reconciliëren, moet u de pagina **Bankreconciliatie** gebruiken. Zie [Bankrekeningen apart reconciliëren](bank-how-reconcile-bank-accounts-separately.md) voor meer informatie.

## <a name="see-also"></a>Zie ook
[Tegoeden beheren](receivables-manage-receivables.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
