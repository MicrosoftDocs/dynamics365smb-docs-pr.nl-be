---
title: Kosten van werknemers registreren en terugbetalen
description: Boek onkosten van werknemers met het dagboek naar de rekening van de werknemer en boek dan een betaling naar hun bankrekening om bedrijfsgerelateerde onkosten terug te betalen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: reimbursement
ms.search.form: '63, 234, 625, 5224, 5237, 5238, 5239, 5240'
ms.date: 06/16/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Kosten van werknemers registreren en terugbetalen

[!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt transacties voor werknemers op dezelfde manier als voor leveranciers. Daarom zijn er werknemersboekingsgroepen om te zorgen dat werknemersposten worden geboekt naar de relevante rekeningen in het grootboek.

> [!NOTE]  
> Werknemerstransacties kunnen alleen in de lokale valuta worden geboekt. Terugbetalingen aan werknemers ondersteunen geen kortingen en betalingstoleranties.

Als medewerkers hun eigen geld uitgeven tijdens zakelijke activiteiten, kunt u de kosten boeken naar de rekening van de werknemer. Vervolgens kunt u de werknemer terugbetalen door een betaling te doen naar de bankrekening van de werknemer, net zoals u leveranciers betaalt.  

> [!TIP]
> In dit artikel wordt uitgelegd hoe u de kosten in de boeken registreert en hoe u de werknemer vergoedt. Uw organisatie heeft mogelijk een portal of app waar medewerkers hun onkostendeclaraties kunnen indienen.

[!INCLUDE [prod_short](includes/prod_short.md)] is flexibel genoeg voor veel verschillende praktijken. De exacte rekeningnummers die moeten worden gebruikt, zijn afhankelijk van de configuratie en processen van uw organisatie.  

## Onkosten van een werknemer registreren

U boekt onkosten van een werknemer op de pagina **Diversendagboek**.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Financiële dagboeken** in en kies vervolgens de gerelateerde koppeling.  
2. Open de relevante dagboekbatch. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.
3. Vul op een nieuwe dagboekregel de velden indien nodig in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]
    > [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]
4. Herhaal stap 3 voor alle kosten die de werknemer heeft betaald.

    > [!TIP]  
    > Als u meerdere onkostenregels boven één tegenrekeningsregel wilt invoeren voor de bankrekening van de werknemer, selecteert u het selectievakje **Salderingsbedrag voorstellen** op de regel voor uw batch op de pagina **Fin. dagboekbatches**. Vervolgens wordt het veld **Bedrag** op de tegenrekeningsregel automatisch ingevuld met de waarde die nodig is om de onkosten in balans te brengen.
5. Kies de actie **Boeken** om de kosten op de rekening van de werknemer te registreren.

## Een werknemer terugbetalen

U betaalt werknemers terug door betalingen te boeken naar hun bankrekening op de pagina **Betalingsdagboek**.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Betalingsdagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Open de relevante betalingsdagboekbatch. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.
3. Vul de vereiste velden in. Zie [Betalingen doen](payables-make-payments.md) voor meer informatie.
4. Of kies de actie **Werknemersbetalingen voorstellen** om automatisch dagboekregels in te voegen voor werknemersterugbetalingen die in behandeling zijn.
5. Kies de actie **Boeken** om de terugbetaling te registreren.  

## Terugbetalingen reconciliëren met werknemersposten

U vereffent werknemersbetalingen met de gerelateerde open werknemersposten op dezelfde manier als u dat doet voor leveranciersbetalingen, bijvoorbeeld op de pagina **Betalingsreconciliatiedagboek**, op basis van de gerelateerde bankafschriftposten. Zie voor meer informatie [Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md). U kunt ook handmatig vereffenen op de pagina **Werknemerposten**. Zie voor meer informatie het gerelateerde [Leveranciersbetalingen reconciliëren met het betalingsdagboek of vanuit leveranciersposten](payables-how-apply-purchase-transactions-manually.md).  

## Zie ook

[Transacties direct naar het grootboek boeken](finance-how-post-transactions-directly.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Journaalboekingen tegenboeken en ontvangsten/zendingen ongedaan maken](finance-how-reverse-journal-posting.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]