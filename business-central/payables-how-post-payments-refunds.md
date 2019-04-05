---
title: Betalingen vereffenen met gerelateerde documenten en deze boeken | Microsoft Docs
description: Beschrijft hoe u betalingen vastlegt die u doet aan leveranciers en terugbetalingen die u doet aan klanten.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment journal, print check, vendor payment, customer refund, creditor, debt, balance due, AP
ms.date: 10/01/2018
ms.author: edupont
ms.openlocfilehash: 7b3065dd0528588fec4c05e4e9c391a3beb1cc9a
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "816785"
---
# <a name="record-payments-and-refunds-in-the-payment-journal"></a>Betalingen en terugbetalingen vastleggen in het betalingsdagboek

Op de pagina **Betalingsdagboek** legt u betalingen vast die u doet aan leveranciers en terugbetalingen die u doet aan klanten. Wanneer u een betalingsdagboekregel boekt, wordt het betaalde bedrag geregistreerd op de opgegeven systeembankrekening. U moet vier stappen uitvoeren om de werkelijke geldovermaking vanaf de gerelateerde bankrekening uit te voeren.  

Het betalingsdagboek is een dagboek dat voor het doen van betalingen is geoptimaliseerd. U kunt snel handmatig regels toevoegen, u kunt [!INCLUDE[d365fin](includes/d365fin_md.md)] leveranciersbetalingen laten voorstellen en u kunt de betaling vereffenen met geboekte documenten. Zelfs wanneer u betalingen doet, voert u een positief bedrag in het veld **Documentbedrag** in. Afhankelijk van de documentsoort voor de dagboekregel wordt dit bedrag vervolgens naar een negatief bedrag geconverteerd in de onderliggende transacties. Zodoende is het sneller voor u om dagboekregels handmatig toe te voegen. Als u liever negatieve bedragen invoert, kunt u het betalingsdagboek personaliseren om in plaats daarvan het veld **Bedrag** weer te geven.  

- Betalingen vereffenen met facturen of creditnota's

    Als u het veld **Vereffeningsnr.** vult met de factuur of creditnota die moet worden betaald of terugbetaald, wordt het document in kwestie ingesteld op betaald wanneer u het dagboek boekt. Dit wordt 'vereffend' genoemd. Als alternatief voor vereffenen tijdens betalingsboeking kunt u de pagina **Leveranciersposten vereffenen** en **Klantenposten vereffenen** gebruiken nadat u de betalingsboeking hebt gemaakt. Zie voor meer informatie bijvoorbeeld [Leveranciersbetalingen reconciliëren met het betalingsdagboek of vanuit leveranciersposten](payables-how-apply-purchase-transactions-manually.md).  

- Voorgestelde betalingen doen aan leveranciers of werknemers

    De functies **Leveranciersbetalingen voorstellen** en **Werknemersbetalingen voorstellen** kunnen u helpen betalingsdagboekregels automatisch te vullen volgens leveranciersprioritering en vervaldatums. Zie voor meer informatie [Leveranciersbetalingen voorstellen](payables-how-suggest-vendor-payments.md). Met deze functie, wordt het veld **Vereffeningsnr.** altijd ingevuld.  

- Cheques afdrukken en elektronisch betalingen doen aan uw bank

    Naast registratie dat de betaling wordt verricht kunt u de pagina **Betalingsdagboek** gebruiken om de betaling uit te voeren voor verdere verwerking door uw bank. Zie voor meer informatie [Chequebetalingen doen](payables-how-work-checks.md) en [Elektronische betalingen doen](payables-how-export-payments-bank-file.md).  

## <a name="to-make-payments-in-the-payment-journal"></a>Betalingen in het betalingsdagboek doen

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsdagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Open de dagboekbatch die bedoeld is voor betalingen.
3. Als u weet wie u wilt betalen of terugbetalen, vult u de velden handmatig in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Als u de betaling wilt vereffenen met de gerelateerde factuur of creditnota, kiest u het veld **Vereffeningsnr.** op de pagina **Leveranciersposten vereffenen**, selecteert u de desbetreffende factuur of creditnota en kiest u vervolgens de knop **OK**.

    Veel velden, zoals **Documentbedrag** en **Vervaldatum** worden nu ingevuld met gegevens uit het geselecteerde document.
5. U kunt ook de functie **Leveranciersbetalingen voorstellen** gebruiken. Alle vereffeningsinformatie en bedragen worden vervolgens ook ingevoerd op de dagboekregels. Zie voor meer informatie [Leveranciersbetalingen voorstellen](payables-how-suggest-vendor-payments.md).

    Berichten begeleiden u bij het juist invullen van de vereiste velden.
6.  Wanneer alle betalingsdagboekregels zijn ingevuld, kiest u de actie **Boeken**.

## <a name="see-also"></a>Zie ook
[Chequebetalingen doen](payables-how-work-checks.md)  
[Elektronische betalingen doen](payables-how-export-payments-bank-file.md)  
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Bankieren instellen](bank-setup-banking.md)  
[Een Positive Pay-bestand exporteren](finance-how-positive-pay.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Het personaliseren van uw werkruimte](ui-personalization-user.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
