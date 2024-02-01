---
title: Betalingen en terugbetalingen vastleggen in het betalingsdagboek
description: Lees hoe u op de pagina Betalingsdagboek betalingen vastlegt die u doet aan leveranciers en terugbetalingen die u doet aan klanten.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment journal, print check, vendor payment, customer refund, refund check, creditor, debt, balance due, AP'
ms.search.form: '256, 233, 624, 1228'
ms.date: 07/09/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="record-payments-and-refunds-in-the-payment-journal"></a>Betalingen en terugbetalingen vastleggen in het betalingsdagboek

Op de pagina **Betalingsdagboek** legt u betalingen vast die u doet aan leveranciers en terugbetalingen die u doet aan klanten. Wanneer u een betalingsdagboekregel boekt, wordt het betaalde bedrag geregistreerd op de opgegeven systeembankrekening. U moet vier stappen uitvoeren om de werkelijke geldovermaking vanaf de gerelateerde bankrekening uit te voeren.  

Het betalingsdagboek is een dagboek dat voor het doen van betalingen is geoptimaliseerd. U kunt snel handmatig regels toevoegen, u kunt [!INCLUDE[prod_short](includes/prod_short.md)] leveranciersbetalingen laten voorstellen en u kunt de betaling vereffenen met geboekte documenten. Zelfs wanneer u betalingen doet, voert u een positief bedrag in het veld **Documentbedrag** in. Afhankelijk van de documentsoort voor de dagboekregel wordt dit bedrag vervolgens naar een negatief bedrag geconverteerd in de onderliggende transacties. Zodoende is het sneller voor u om dagboekregels handmatig toe te voegen. Als u liever negatieve bedragen invoert, kunt u het betalingsdagboek personaliseren om in plaats daarvan het veld **Bedrag** weer te geven.  

- Betalingen vereffenen met facturen of creditnota's

    Als u het veld **Vereffeningsnr.** vult met de factuur of creditnota die moet worden betaald of terugbetaald, wordt het document in kwestie ingesteld op betaald wanneer u het dagboek boekt. Dit wordt 'vereffend' genoemd. Als alternatief voor vereffenen tijdens betalingsboeking kunt u de pagina **Leveranciersposten vereffenen** en **Klantenposten vereffenen** gebruiken nadat u de betalingsboeking hebt gemaakt. Zie voor meer informatie bijvoorbeeld [Leveranciersbetalingen reconciliëren met het betalingsdagboek of vanuit leveranciersposten](payables-how-apply-purchase-transactions-manually.md).  

- Voorgestelde betalingen doen aan leveranciers of werknemers

    De functies **Leveranciersbetalingen voorstellen** en **Werknemersbetalingen voorstellen** kunnen u helpen betalingsdagboekregels automatisch te vullen volgens leveranciersprioritering en vervaldatums. Zie voor meer informatie [Leveranciersbetalingen voorstellen](payables-how-suggest-vendor-payments.md). Met deze functie, wordt het veld **Vereffeningsnr.** altijd ingevuld.  

- Cheques afdrukken en elektronisch betalingen doen aan uw bank

    Naast registratie dat de betaling wordt verricht kunt u de pagina **Betalingsdagboek** gebruiken om de betaling uit te voeren voor verdere verwerking door uw bank. Zie voor meer informatie [Chequebetalingen doen](payables-how-work-checks.md) en [Elektronische betalingen doen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).  

## <a name="to-make-payments-in-the-payment-journal"></a>Betalingen in het betalingsdagboek doen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Betalingsdagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Open de dagboekbatch die bedoeld is voor betalingen.
3. Als u weet wie u wilt betalen, vult u de velden handmatig in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Als u de betaling wilt vereffenen met de gerelateerde factuur of creditnota, kiest u het veld **Vereffeningsnr.** op de pagina **Leveranciersposten vereffenen**, selecteert u de desbetreffende factuur of creditnota en kiest u vervolgens de knop **OK**.

    Veel velden, zoals **Documentbedrag** en **Vervaldatum** worden nu ingevuld met gegevens uit het geselecteerde document.
5. U kunt ook de functie **Leveranciersbetalingen voorstellen** gebruiken. Alle vereffeningsinformatie en bedragen worden vervolgens ook ingevoerd op de dagboekregels. Zie voor meer informatie [Leveranciersbetalingen voorstellen](payables-how-suggest-vendor-payments.md).

    Berichten begeleiden u bij het juist invullen van de vereiste velden.
6. Wanneer alle betalingsdagboekregels zijn ingevuld, kiest u de actie **Boeken**.


## <a name="to-issue-a-refund-check"></a>Een terugbetalingscheque uitgeven

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsdagboeken** in en kies de gerelateerde koppeling.
2. Selecteer **Terugbetaling** in het veld **Documentsoort**.  
3. Gebruik in het veld **Extern documentnr.** dit als referentie voor de terugbetalingscontrole (bijvoorbeeld het retourordernummer).  
4. Selecteer **Klant** in het veld **Rekeningsoort** .  
5. In het veld **Rekeningnummer** selecteert u het rekeningnummer van de klant waaraan de terugbetalingscheque wordt uitgegeven.  
6. Voer in het veld **Bedrag** het bedrag in dat u wilt terugbetalen.  
7. Selecteer in het veld **Tegenrekeningsoort** **Bankrekening**.  
8. Selecteer in het veld **Tegenrekeningnr.** de bankrekening waarvan de cheque afkomstig zal zijn.  
9. Kies in het veld **Vereffeningsnr.** de documenten die een terugbetaling vereisen.  
10. Wanneer alle betalingsdagboekregels zijn voltooid, kiest u de actie **Boeken/afdrukken**, kies dan de actie **Boeken en afdrukken** en selecteer **Ja**.  
  

## <a name="see-also"></a>Zie ook
[Chequebetalingen doen](payables-how-work-checks.md)  
[Elektronische betalingen doen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Bankieren instellen](bank-setup-banking.md)  
[Een Positive Pay-bestand exporteren](finance-how-positive-pay.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Uw werkruimte personaliseren](ui-personalization-user.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
