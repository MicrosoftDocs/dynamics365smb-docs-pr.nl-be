---
title: Betalingen en terugbetalingen vastleggen in betalingsdagboeken
description: Lees hoe u op de pagina Betalingsdagboek betalingen vastlegt die u doet aan leveranciers en terugbetalingen die u doet aan klanten.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment journal, print check, vendor payment, customer refund, refund check, creditor, debt, balance due, AP'
ms.search.form: '256, 233, 624, 1228'
ms.date: 06/06/2024
ms.service: dynamics-365-business-central
---
# Betalingen en terugbetalingen vastleggen in het betalingsdagboek

Op de pagina **Betalingsdagboek** legt u betalingen vast die u doet aan leveranciers en terugbetalingen die u doet aan klanten. Wanneer u een betalingsdagboekregel boekt, wordt het betaalde bedrag geregistreerd op de opgegeven bankrekening. U moet vier stappen uitvoeren om de werkelijke geldovermaking vanaf de gerelateerde bankrekening uit te voeren.  

Betalingsdagboeken zijn dagboeken die voor het doen van betalingen zijn geoptimaliseerd. U kunt snel handmatig regels toevoegen, u kunt [!INCLUDE[prod_short](includes/prod_short.md)] leveranciersbetalingen laten voorstellen en u kunt de betaling vereffenen met geboekte documenten. Hoewel u betalingen doet, voert u een positief bedrag in het veld **Documentbedrag** in. Afhankelijk van de documentsoort voor de dagboekregel wordt dit bedrag vervolgens naar een negatief bedrag geconverteerd in de onderliggende transacties. Zodoende is het sneller voor u om dagboekregels handmatig toe te voegen. Als u liever negatieve bedragen invoert, kunt u het betalingsdagboek personaliseren om in plaats daarvan het veld **Bedrag** weer te geven. Ga voor meer informatie over het personaliseren van pagina's naar [Begin met personaliseren door de personalisatiemodus te gebruiken](ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode).  

- Betalingen vereffenen met facturen of creditnota's

    Als u het veld **Vereffeningsnr.** vult met de factuur of creditnota die moet worden betaald of terugbetaald, wordt het document in kwestie ingesteld op **Betaald** wanneer u het dagboek boekt. Deze instelling wordt 'vereffend' genoemd. Als alternatief voor vereffenen wanneer u een betaling boekt, kunt u de pagina **Leveranciersposten vereffenen** en **Klantenposten vereffenen** gebruiken nadat u de betaling hebt geboekt. Zie voor meer informatie bijvoorbeeld [Leveranciersbetalingen reconciliëren met het betalingsdagboek of vanuit leveranciersposten](payables-how-apply-purchase-transactions-manually.md).  

- Voorgestelde betalingen doen aan leveranciers of werknemers

    De acties **Leveranciersbetalingen voorstellen** en **Werknemersbetalingen voorstellen** kunnen u helpen betalingsdagboekregels automatisch te vullen volgens leveranciersprioritering en vervaldatums. Ga voor meer informatie naar [Leveranciersbetalingen voorstellen](payables-how-suggest-vendor-payments.md). Met deze functie, wordt het veld **Vereffeningsnr.** altijd ingevuld.  

- Cheques afdrukken en elektronisch betalingen doen aan uw bank

    Naast registratie dat de betaling wordt verricht kunt u de pagina **Betalingsdagboek** gebruiken om de betaling uit te voeren voor verdere verwerking door uw bank. Ga voor meer informatie naar [Chequebetalingen doen](payables-how-work-checks.md) en [Elektronische betalingen doen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file).  

## Betalingen in het betalingsdagboek doen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Betalingsdagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Open de dagboekbatch die u gebruikt voor betalingen.
3. Als u weet wie u wilt betalen, vult u de velden handmatig in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Als u de betaling wilt vereffenen met de gerelateerde factuur of creditnota, kiest u het veld **Vereffeningsnr.** op de pagina **Leveranciersposten vereffenen**, selecteert u de desbetreffende factuur of creditnota en kiest u vervolgens de knop **OK**.

    Veel velden, zoals **Documentbedrag** en **Vervaldatum** bevatten nu gegevens uit het geselecteerde document.
5. U kunt ook de actie **Leveranciersbetalingen voorstellen** gebruiken. Alle vereffeningsinformatie en bedragen worden ook ingevoerd op de dagboekregels. Ga voor meer informatie naar [Leveranciersbetalingen voorstellen](payables-how-suggest-vendor-payments.md).
6. Wanneer u alle betalingsdagboekregels hebt ingevuld, kiest u de actie **Boeken**.

## Een terugbetalingscheque uitgeven

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsdagboeken** in en kies de gerelateerde koppeling.
2. Selecteer **Terugbetaling** in het veld **Documentsoort**.  
3. Voer in het veld **Extern documentnr.** een referentie in voor de terugbetalingscontrole (bijvoorbeeld het retourordernummer).  
4. Selecteer **Klant** in het veld **Rekeningsoort** .  
5. In het veld **Rekeningnummer** selecteert u het rekeningnummer van de klant waaraan de terugbetalingscheque wordt uitgegeven.  
6. Voer in het veld **Bedrag** het bedrag in dat u wilt terugbetalen.  
7. Selecteer in het veld **Tegenrekeningsoort** **Bankrekening**.  
8. Selecteer in het veld **Tegenrekeningnr.** de bankrekening waarvan de cheque afkomstig zal zijn.  
9. Kies in het veld **Vereffeningsnr.** selecteer de documenten die een terugbetaling vereisen.  
10. Wanneer u alle betalingsdagboekregels hebt voltooid, kiest u de actie **Boeken/afdrukken**. Kies dan de actie **Boeken en afdrukken** en kies **Ja**.  
  
## Zie ook

[Chequebetalingen doen](payables-how-work-checks.md)  
[Elektronische betalingen doen](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Bankieren instellen](bank-setup-banking.md)  
[Een Positive Pay-bestand exporteren](finance-how-positive-pay.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Uw werkruimte personaliseren](ui-personalization-user.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
