---
title: Betalingen vereffenen met gerelateerde documenten en deze boeken | Microsoft Docs
description: Beschrijft hoe u betalingen vastlegt die u doet aan leveranciers en terugbetalingen die u doet aan klanten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, customer refund, creditor, debt, balance due, AP
ms.date: 04/30/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 75501b9402bb1c14fcfeb2fc6e61f055a2247493
ms.openlocfilehash: 3cad699234d95a849bf48f04c8462afa968789f6
ms.contentlocale: nl-be
ms.lasthandoff: 05/15/2018

---
# <a name="record-payments-and-refunds"></a>Betalingen en terugbetalingen vastleggen
In het **Betalingsdagboek** legt u betalingen vast die u doet aan leveranciers en terugbetalingen die u doet aan klanten. Wanneer u een betalingsdagboekregel boekt, wordt het betaalde bedrag geregistreerd op de opgegeven systeembankrekening. U moet vier stappen uitvoeren om de werkelijke geldovermaking vanaf de gerelateerde bankrekening uit te voeren.

Als u het veld **Vereffeningsnr.** vult met de factuur of creditnota die moet worden betaald of terugbetaald, wordt het document in kwestie ingesteld op betaald wanneer u het dagboek boekt. Dit wordt 'vereffend' genoemd. Als alternatief voor vereffenen tijdens betalingsboeking kunt u het venster **Leveranciersposten vereffenen** en **Klantenposten vereffenen** gebruiken nadat u de betalingsboeking hebt gemaakt. Zie voor meer informatie bijvoorbeeld [Leveranciersbetalingen handmatig reconciliëren](payables-how-apply-purchase-transactions-manually.md).

De functie **Leveranciersbetalingen voorstellen** kan u helpen betalingsdagboekregels automatisch te vullen volgens leverancierprioritering en vervaldatums. Zie voor meer informatie [Leveranciersbetalingen voorstellen](payables-how-suggest-vendor-payments.md). Met deze functie, wordt het veld **Vereffeningsnr.** altijd ingevuld.

Naast registratie dat de betaling wordt verricht kunt u het venster **Betalingsdagboek** gebruiken om de betaling uit te voeren voor verdere verwerking door uw bank. Zie voor meer informatie [Chequebetalingen doen](payables-how-work-checks.md) en [Elektronische betalingen doen](payables-how-export-payments-bank-file.md).  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Betalingsdagboeken** in en klik vervolgens op de gerelateerde koppeling.
2. Open de dagboekbatch die bedoeld is voor betalingen.
3. Als u weet wie u wilt betalen of terugbetalen, vult u de velden handmatig in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Als u de betaling wilt vereffenen met de gerelateerde factuur of creditnota, kiest u het veld **Vereffeningsnr.** in het venster **Leveranciersposten vereffenen**, selecteert u de desbetreffende factuur of creditnota en kiest u vervolgens de knop **OK**.

    Veel velden, zoals **Bedrag** en **Vervaldatum**, worden nu ingevuld met gegevens uit het geselecteerde document.
5. U kunt ook de functie **Leveranciersbetalingen voorstellen** gebruiken. Alle vereffeningsinformatie en bedragen worden vervolgens ook ingevoerd op de dagboekregels. Zie voor meer informatie [Leveranciersbetalingen voorstellen](payables-how-suggest-vendor-payments.md).

    Berichten begeleiden u bij het juist invullen van de vereiste velden.
6.  Wanneer alle betalingsdagboekregels zijn ingevuld, kiest u de actie **Boeken**.

## <a name="see-also"></a>Zie ook
[Chequebetalingen doen](payables-how-work-checks.md)  
[Elektronische betalingen doen](payables-how-export-payments-bank-file.md)  
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Bankieren instellen](bank-setup-banking.md)  
[Een Positive Pay-bestand exporteren](finance-how-positive-pay.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

