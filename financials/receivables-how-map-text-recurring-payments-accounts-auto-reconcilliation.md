---
title: Tekst-aan-rekening koppeling instellen voor periodieke betalingen | Microsoft Docs
description: Koppel tekst aan betalingen met bepaalde rekeningen, zodat betalingen naar de rekeningen geboekt worden als u het betalingsreconciliatiedagboek boekt.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account linking, direct payment posting, automatic payment processing, reconcile payment, recurring expense, recurring cash receipt
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: c5f6f041083e291feca4544f42d43d5ebe3b7e9c
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Tekst op herhalende betalingen aan rekeningen toewijzen voor automatisch reconciliatie
In het venster **Toewijzing tekst aan rekening**, dat u opent vanuit het venster **Dagboek betalingsreconciliatie** , kunt u toewijzingen instellen tussen tekst op betalingen en specifieke debet-, credit- en tegenrekeningen zodat dergelijke betalingen worden geboekt naar de opgegeven rekeningen wanneer u het betalingsreconciliatiedagboek boekt.

Er bestaat vergelijkbare functionaliteit om te grote bedragen op de dagboekregels voor betalingreconciliatie op ad-hocbasis te reconciliëren. Zie [Betalingen reconciliëren die niet automatisch kunnen worden vereffend](receivables-how-reconcile-payments-cannot-apply-auto.md) voor meer informatie.

Betalingen die worden geboekt op basis van tekst-naar-rekening toewijzingen, worden niet vereffend met openstaande posten, maar worden slechts naar de opgegeven rekeningen geboekt, naast het feit dat er bankrekeningposten worden gemaakt. Toewijzing van tekst aan rekeningen is daarom geschikt voor periodieke ontvangsten of kosten, zoals regelmatige aankopen van autobrandstof of bankkosten en -rente, die regelmatig voorkomen op het bankafschrift en geen gerelateerd bedrijfsdocument nodig hebben. Zie de sectie “Voorbeeld - tekst-aan-rekening toewijzing voor brandstofkosten” in dit onderwerp voor meer informatie.

> [!NOTE]  
>   Betalingen op reconciliatiedagboekregels worden alleen op boeken volgens tekst-naar-rekening toewijzing ingesteld als de automatische vereffeningsfunctie slechts een afstemmingszekerheid van **Laag** of **Normaal** kan bieden. Als de automatische vereffeningsfunctie een afstemmingszekerheid van Hoog oplevert, wordt de betaling automatisch vereffend met een of meer openstaande posten en wordt de betaling niet geboekt naar de rekeningen die zijn opgegeven in het venster **Toewijzing tekst aan rekening** . Met andere woorden: een afstemmingszekerheid van **Hoog** heeft voorrang op een tekst-aan-rekening toewijzing.

Op een dagboekregel van een betalingsreconciliatie waar de betaling is ingesteld op boeking volgens de tekst-aan-rekening toewijzing, bevat het veld **Zekerheid afstemming** de waarde **Hoog - Toewijzing tekst aan rekening** en bevatten de velden **Rekeningsoort** en **Rekeningnr.** de toegewezen rekeningen.

## <a name="to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Tekst op herhalende betalingen aan rekeningen toewijzen voor automatisch reconciliatie
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Betalingsreconciliatiedagboeken** in en klik vervolgens op de gerelateerde koppeling.
2. Open een betalingreconciliatiedagboek. Zie voor meer informatie [Betalingen vereffenen met automatische vereffening](receivables-how-reconcile-payments-auto-application.md).
3. Kies de actie **Tekst afstemmen op rekening**. Het venster **Toewijzing tekst aan rekening** wordt geopend.
4. Voer in het veld **Toewijzingstekst** willekeurige tekst in die voorkomt op betalingen die u, zonder deze met een openstaande post te vereffenen, wilt boeken naar opgegeven rekeningen. U kunt maximaal 50 tekens invoeren.

    > [!NOTE]  
   >   Als er geen andere betalingen met de betreffende koppelingstekst zijn, vindt de toewijzing van tekst aan rekening ook plaats wanneer slechts een deel van de tekst op de betaling als toewijzingstekst bestaat.
5. Voer in het veld **Leveranciersnr.** de leverancier in waarnaar de betalingen worden geboekt.
6. Geef in het veld **Bronsoort saldo** op of de betaling naar een grootboekrekening of een klanten- of een leveranciersrekening wordt geboekt.
7. Geef in het veld **Bronnr. saldo** de rekening op waarnaar de betaling wordt geboekt, afhankelijk van uw keuze in het veld **Bronsoort saldo**.

    > [!NOTE]
    > Gebruik de velden **Debetrekeningnr.** en **Creditrekeningnr.** niet in combinatie met betalingsreconciliatie. Deze worden alleen gebruikt voor inkomende documenten. Zie [OCR gebruiken om PDF- en afbeeldingsbestanden te converteren naar elektronische documenten](across-how-use-ocr-pdf-images-files.md) voor meer informatie.

8. Herhaal stap 3 tot en met 7 voor alle tekst op betalingen die u aan rekeningen wilt toewijzen voor directe boeking zonder vereffening.

De volgende keer dat u een bankafschriftbestand importeert of de actie **Automatisch vereffenen** kiest in het venster **Dagboek betalingsreconciliatie**, zullen dagboekregels voor de betalingen die de opgegeven toewijzingstekst bevatten, de toegewezen rekeningen bevatten in de velden **Rekeningsoort** en **Rekeningnr.** Het veld **Zekerheid afstemming** bevat **Hoog - Toewijzing tekst aan rekening**. Hiervoor geldt de voorwaarde dat de automatische vereffeningsfunctie slechts een afstemmingszekerheid van **Laag** of **Gemiddeld** kan bieden.

## <a name="example-text-to-account-mapping-for-fuel-expense"></a>Voorbeeld: tekst-aan-rekening toewijzing voor brandstofkosten
Als u brandstofkosten die bij Shell-benzinestations worden betaald, altijd wilt boeken naar de grootboekrekening voor benzine (rekening 8510), vult u een regel in het venster **Toewijzing tekst aan rekening** als volgt.

| Toewijzing tekst | Debetrekeningnr. | Creditrekeningnr. | Bronsoort saldo | Bronnr. saldo |
| --- | --- | --- | --- | --- |
| Shell |LEEG |8510 |Grootboekrekening |LEEG |

> [!TIP]
>   Zie voor meer informatie over het werken met velden en kolommen [Werken met [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md). Zie [Zoeken](ui-search.md) voor meer informatie over het zoeken naar specifieke pagina's.

## <a name="see-also"></a>Zie ook
[Tegoeden beheren](receivables-manage-receivables.md)  
[Verkoop](sales-manage-sales.md)  
[De service Envestnet Yodlee Bank Feeds instellen](bank-how-setup-bank-statement-service.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies](ui-extensions.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

