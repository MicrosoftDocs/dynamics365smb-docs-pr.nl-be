---
title: Tekst-aan-rekening koppeling instellen voor periodieke betalingen
description: 'Koppel tekst aan betalingen met bepaalde rekeningen, zodat betalingen naar de rekeningen geboekt worden als u het betalingsreconciliatiedagboek boekt.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'account linking, direct payment posting, automatic payment processing, reconcile payment, recurring expense, recurring cash receipt'
ms.search.form: '1290, 1294, 1287'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation" />Tekst op herhalende betalingen aan rekeningen toewijzen voor automatisch reconciliatie

Op de pagina **Toewijzing tekst aan rekening**, die u opent vanuit de pagina **Dagboek betalingsreconciliatie** , kunt u toewijzingen instellen tussen tekst op betalingen en specifieke debet-, credit- en tegenrekeningen zodat dergelijke betalingen worden geboekt naar de opgegeven rekeningen wanneer u het betalingsreconciliatiedagboek boekt.

Er bestaat vergelijkbare functionaliteit om te grote bedragen op de dagboekregels voor betalingreconciliatie op ad-hocbasis te reconciliëren. Zie [Betalingen reconciliëren die niet automatisch kunnen worden vereffend](receivables-how-reconcile-payments-cannot-apply-auto.md) voor meer informatie.

Betalingen die worden geboekt op basis van tekst-naar-rekening toewijzingen, worden niet vereffend met openstaande posten, maar worden slechts naar de opgegeven rekeningen geboekt, naast het feit dat er bankrekeningposten worden gemaakt. Toewijzing van tekst aan rekeningen is daarom geschikt voor periodieke ontvangsten of kosten, zoals regelmatige aankopen van autobrandstof of bankkosten en -rente, die regelmatig voorkomen op het bankafschrift en geen gerelateerd bedrijfsdocument nodig hebben. Zie de sectie 'Voorbeeld - tekst-aan-rekening toewijzing voor brandstofkosten' in dit onderwerp voor meer informatie.

> [!NOTE]  
>   Betalingen op reconciliatiedagboekregels worden alleen op boeken volgens tekst-naar-rekening toewijzing ingesteld als de automatische vereffeningsfunctie slechts een afstemmingszekerheid van **Laag** of **Normaal** kan bieden. Als de automatische vereffeningsfunctie een afstemmingszekerheid van Hoog oplevert, wordt de betaling automatisch vereffend met een of meer openstaande posten en wordt de betaling niet geboekt naar de rekeningen die zijn opgegeven op de pagina **Toewijzing tekst aan rekening** . Met andere woorden: een afstemmingszekerheid van **Hoog** heeft voorrang op een tekst-aan-rekening toewijzing.

Op een dagboekregel van een betalingsreconciliatie waar de betaling is ingesteld op boeking volgens de tekst-aan-rekening toewijzing, bevat het veld **Zekerheid afstemming** de waarde **Hoog - Toewijzing tekst aan rekening** en bevatten de velden **Rekeningsoort** en **Rekeningnr.** de toegewezen rekeningen.

## <a name="to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation" />Tekst op herhalende betalingen aan rekeningen toewijzen voor automatisch reconciliatie

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Betalingsreconciliatiedagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Open een betalingreconciliatiedagboek. Zie voor meer informatie [Betalingen vereffenen met automatische vereffening](receivables-how-reconcile-payments-auto-application.md).
3. Kies de actie **Tekst afstemmen op rekening**. De pagina **Toewijzing tekst aan rekening** wordt geopend.
4. Voer in het veld **Toewijzingstekst** willekeurige tekst in die voorkomt op betalingen die u, zonder deze met een openstaande post te vereffenen, wilt boeken naar opgegeven rekeningen. U kunt maximaal 50 tekens invoeren.

    > [!NOTE]  
    >   Als er geen andere betalingen met de betreffende koppelingstekst zijn, vindt de toewijzing van tekst aan rekening ook plaats wanneer slechts een deel van de tekst op de betaling als toewijzingstekst bestaat.
5. Voer in het veld **Leveranciersnr.** de leverancier in waarnaar de betalingen worden geboekt.
6. Geef in het veld **Bronsoort saldo** op of de betaling naar een grootboekrekening of een klanten- of een leveranciersrekening wordt geboekt.
7. Geef in het veld **Bronnr. saldo** de rekening op waarnaar de betaling wordt geboekt, afhankelijk van uw keuze in het veld **Bronsoort saldo**.

    > [!NOTE]
    > Gebruik de velden **Debetrekeningnr.** en **Creditrekeningnr.** niet in combinatie met betalingsreconciliatie. Deze worden alleen gebruikt voor inkomende documenten. Zie [OCR gebruiken om PDF- en afbeeldingsbestanden te converteren naar elektronische documenten](across-how-use-ocr-pdf-images-files.md) voor meer informatie.

8. Herhaal stap 3 tot en met 7 voor alle tekst op betalingen die u aan rekeningen wilt toewijzen voor directe boeking zonder vereffening.

De volgende keer dat u een bankafschriftbestand importeert of de actie **Automatisch vereffenen** kiest op de pagina **Dagboek betalingsreconciliatie**, zullen dagboekregels voor de betalingen die de opgegeven toewijzingstekst bevatten, de toegewezen rekeningen bevatten in de velden **Rekeningsoort** en **Rekeningnr.** Het veld **Zekerheid afstemming** bevat **Hoog - Toewijzing tekst aan rekening**. Hiervoor geldt de voorwaarde dat de automatische vereffeningsfunctie slechts een afstemmingszekerheid van **Laag** of **Gemiddeld** kan bieden.

## <a name="example-text-to-account-mapping-for-bank-fees" />Voorbeeld: tekst-aan-rekening toewijzing voor bankkosten

Om uitgaven die verband houden met vergoedingen van een specifieke bank, MyBank, altijd te boeken naar de grootboekrekening voor bankkosten en vergoedingen (rekening 60400), vult u een regel op de pagina **Toewijzing tekst aan rekening** als volgt in.

| Toewijzing tekst | Debetrekeningnr. | Creditrekeningnr. | Bronsoort saldo | Bronnr. saldo |
| --- | --- | --- | --- | --- |
| MyBank |LEEG |60400|Grootboekrekening |LEEG |

## <a name="see-related-microsoft-trainingtrainingmodulesuse-journals-dynamics-365-business-central" />Zie gerelateerde [Microsoft-training](/training/modules/use-journals-dynamics-365-business-central/)

## <a name="see-also" />Zie ook

[Tegoeden beheren](receivables-manage-receivables.md)  
[Verkoop](sales-manage-sales.md)  
[De Envestnet Yodlee Bank Feeds-service instellen](bank-how-setup-bank-statement-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] aanpassen met behulp van extensies](ui-extensions.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
