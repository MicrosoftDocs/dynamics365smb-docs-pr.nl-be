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
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: deb05c6294edeb892606154b38de2aa406abf6a2
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Procedure: Tekst op herhalende betalingen aan rekeningen toewijzen voor automatische afstemming
In het venster **Toewijzing tekst aan rekening**, dat u opent vanuit het venster **Dagboek betalingsreconciliatie** , kunt u toewijzingen instellen tussen tekst op betalingen en specifieke debet-, credit- en tegenrekeningen zodat dergelijke betalingen worden geboekt naar de opgegeven rekeningen wanneer u het betalingsreconciliatiedagboek boekt.

> [!NOTE]  
>   Dit onderwerp is ook van toepassing wanneer u de functie **Tekst afstemmen op rekening** van een inkomende documentrecord gebruikt om u te helpen bij het converteren van elektronische documenten die zijn ontvangen van externe services, naar documenten in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Zie [Procedure: OCR gebruiken om PDF- en afbeeldingsbestanden te converteren naar elektronische documenten](across-how-use-ocr-pdf-images-files.md) voor meer informatie.   

Er bestaat vergelijkbare functionaliteit om te grote bedragen op de dagboekregels voor betalingreconciliatie op ad-hocbasis te reconciliëren. Zie [Procedure: Betalingen reconciliëren die niet automatisch kunnen worden vereffend](receivables-how-reconcile-payments-cannot-apply-auto.md) voor meer informatie.

Betalingen die worden geboekt op basis van tekst-naar-rekening toewijzingen, worden niet vereffend met openstaande posten, maar worden slechts naar de opgegeven rekeningen geboekt, naast het feit dat er bankrekeningposten worden gemaakt. Toewijzing van tekst aan rekeningen is daarom geschikt voor periodieke ontvangsten of kosten, zoals regelmatige aankopen van autobrandstof of bankkosten en -rente, die regelmatig voorkomen op het bankafschrift en geen gerelateerd bedrijfsdocument nodig hebben. Zie de sectie “Voorbeeld - tekst-aan-rekening toewijzing voor brandstofkosten” in dit onderwerp voor meer informatie.

> [!NOTE]  
>   Betalingen op reconciliatiedagboekregels worden alleen op boeken volgens tekst-naar-rekening toewijzing ingesteld als de automatische vereffeningsfunctie slechts een afstemmingszekerheid van **Laag** of **Normaal** kan bieden. Als de automatische vereffeningsfunctie een afstemmingszekerheid van Hoog oplevert, wordt de betaling automatisch vereffend met een of meer openstaande posten en wordt de betaling niet geboekt naar de rekeningen die zijn opgegeven in het venster **Toewijzing tekst aan rekening** . Met andere woorden: een afstemmingszekerheid van **Hoog** heeft voorrang op een tekst-aan-rekening toewijzing.

Op een dagboekregel van een betalingsreconciliatie waar de betaling is ingesteld op boeking volgens de tekst-aan-rekening toewijzing, bevat het veld **Zekerheid afstemming** de waarde **Hoog - Toewijzing tekst aan rekening** en bevatten de velden **Rekeningsoort** en **Rekeningnr.** de toegewezen rekeningen.

## <a name="to-map-text-on-recurring-payments-to-accounts-for-automatic-reconciliation"></a>Tekst op herhalende betalingen aan rekeningen toewijzen voor automatisch reconciliatie
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Betalingsreconciliatiedagboeken** in en klik vervolgens op de gerelateerde koppeling.
2. Open een betalingreconciliatiedagboek. Zie voor meer informatie [Procedure: Betalingen reconciliëren met automatische vereffening](receivables-how-reconcile-payments-auto-application.md).
3. Kies de actie **Tekst afstemmen op rekening**. Het venster **Toewijzing tekst aan rekening** wordt geopend.
4. Voer in het veld **Toewijzingstekst** willekeurige tekst in die voorkomt op betalingen die u, zonder deze met een openstaande post te vereffenen, wilt boeken naar opgegeven rekeningen. U kunt maximaal 50 tekens invoeren.

    > [!NOTE]  
>   Als er geen andere betalingen of inkomende documenten met de betreffende koppelingstekst zijn, vindt de tekst-aan-rekening toewijzing zelfs ook plaats wanneer slechts een deel van de tekst op de betaling of inkomend document als toewijzingstekst bestaat.
5. Voer in het veld **Leveranciersnr.** de leverancier op voor wie inkomende documenten met de toewijzingstekst worden gemaakt of naar wie betalingen worden geboekt. Zie [Procedure: OCR gebruiken om PDF- en afbeeldingsbestanden te converteren naar elektronische documenten](across-how-use-ocr-pdf-images-files.md) voor meer informatie.      
6. Voer in het veld **Debetrekeningnr.** de rekening in waarnaar betalingen die de toewijzingstekst bevatten, worden geboekt als het inkomende betalingen zijn. Voor inkomende voor betalingen is het teken van de waarde in het **Afschrifttotaal** positief.
7. Voer in het veld **Credittrekeningnr.** de rekening in waarnaar betalingen die de toewijzingstekst bevatten, worden geboekt als het uitgaande betalingen zijn. Voor uitgaande betalingen is het teken van de waarde in het **Afschrifttotaal** negatief.
8. Geef in het veld **Bronsoort saldo** op of de betaling naar een grootboekrekening of een klanten- of een leveranciersrekening wordt geboekt.
9. Geef in het veld **Bronnr. saldo** de rekening op waarnaar de betaling wordt geboekt, afhankelijk van uw keuze in het veld **Bronsoort saldo**.
10. Herhaal stap 4 tot en met 8 voor alle tekst op betalingen die u aan rekeningen wilt toewijzen voor directe boeking zonder vereffening.

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
[Procedure: De service Envestnet Yodlee Bank Feeds instellen](bank-how-setup-bank-statement-service.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies](ui-extensions.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

