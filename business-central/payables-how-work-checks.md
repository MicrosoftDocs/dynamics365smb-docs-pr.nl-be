---
title: 'Cheques afgeven, afdrukken, annuleren, en nietig verklaren'
description: 'Beschrijft hoe u cheques afgeeft met het betalingsdagboek, cheques afdrukt, en chequeposten nietig verklaart of weergeeft in Business Central.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'payment journal, print check, vendor payment, creditor, debt, balance due, AP'
ms.search.form: '256, 404,'
ms.date: 07/17/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="make-check-payments"></a>Chequebetalingen doen

In [!INCLUDE[prod_short](includes/prod_short.md)] kunt u elektronische en handmatige cheques verzenden. Bij beide methoden wordt het betalingsdagboek gebruikt om cheques te verzenden naar leveranciers. Daarnaast kunt u cheques nietig verklaren en chequeposten weergeven.

In de volgende procedure wordt beschreven hoe u een leverancier betaalt met een computercheque door de betaling te vereffenen met de relevante leveranciersfactuur, de cheque af te drukken en vervolgens de betaling te boeken als betaald. Dit leidt tot positieve leveranciersposten die worden vereffend met negatieve bankposten en fysieke cheques voor verwerking in de bank.

U kunt met twee soorten cheques betalen. Voor beide soorten moet het veld **Tegenrekeningtype** of **Rekeningsoort** **Bankrekening** bevatten.

- **Automatische cheque**: selecteer deze optie als u een cheque wilt afdrukken voor het bedrag op de betalingsdagboekregel. U moet de cheques afdrukken voordat u de dagboekregels kunt boeken.
- **Handmatige cheque**: selecteer deze optie als u handmatig een cheque hebt gemaakt en er een bijbehorende chequepost moet worden gemaakt voor dit bedrag. Als u deze optie gebruikt, kunt u de cheque niet afdrukken.

> [!NOTE]  
> Om ervoor te zorgen dat uw bank alleen gevalideerde cheques en bedragen vrijgeeft, kunt u deze verzenden in een bestand dat gegevens over de leverancier, cheque en betaling bevat. Zie voor meer informatie [Een Positive Pay-bestand exporteren](finance-how-positive-pay.md).

> [!IMPORTANT]
> De printer moet correct zijn ingesteld op het afdrukken van chequeformulieren en u moet bepalen welke indeling wordt gebruikt. Zie voor meer informatie [Een cheque-indeling selecteren](finance-how-define-check-layouts.md). Als alternatief kunt u de cheque bijvoorbeeld als PDF-bestand verzenden.  

U kunt maximaal 10 facturen op een pagina voor een chequestrook afdrukken. Als een cheque betrekking heeft op meer dan 10 facturen en u de strook afdrukt, maken we de cheque ongeldig op de eerste pagina en drukken we het woord VERNIETIGD op de cheque af. We drukken vervolgens de rest van de facturen en het totale chequebedrag op de tweede pagina af.

## <a name="to-pay-a-vendor-invoice-with-a-computer-check"></a>Een leverancier betalen met een automatische cheque

Hierna wordt beschreven hoe u een leverancier per cheque betaalt. De stappen zijn vergelijkbaar met het terugbetalen van een klant per cheque.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Betalingsdagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Vul de betalingsdagboekregels in. Zie voor meer informatie [Betalingen en terugbetalingen vastleggen](payables-how-post-payments-refunds.md).
3. Selecteer **Cheque** in het veld **Betalingswijze**.
4. Selecteer **Automatische cheque** in het veld **Betalingssoort**.
5. Kies de actie **Cheque afdrukken**.
6. Vul de vereiste velden op het sneltabblad **Cheque** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
7. Als uw printer is ingesteld om cheques af te drukken, kiest u de knop **Afdrukken**. Anders kiest u de knop **Verzenden naar**, selecteert u de optie **PDF-document**, kiest u de knop **OK** en drukt u het PDF-document af.

    De fysieke cheques kunnen nu naar de leveranciers worden verzonden voor verwerking. Boek de betaling zoals vereffend met de leverancier en daarmee betaald in het systeem.
8. Kies de actie **Boeken**.

Er worden volledig vereffende leveranciersposten en bankposten gemaakt.

> [!NOTE]  
> Als u cheques in meerdere valuta's van verschillende bankrekeningen wilt afdrukken en betalen, moet u de batchverwerking **Cheque afdrukken** voor elke valuta afzonderlijk uitvoeren en de juiste bankrekening opgeven.

## <a name="to-cancel-printed-checks-that-arent-posted"></a>Naar Annuleren afgedrukte cheques die niet zijn geboekt

U kunt niet-geboekte cheques annuleren nadat ze zijn afgedrukt door de actie **Ongeldige cheque** op de pagina **Betalingsdagboek** te gebruiken.

1. Kies op de pagina **Betalingsdagboek** de actie **Ongeldige cheque** en kies vervolgens welke cheques u wilt annuleren.

## <a name="to-void-checks"></a>Cheques nietig verklaren

Wanneer chequebetaling is geboekt, kunt u cheques alleen annuleren (nietig verklaren) vanuit de resulterende bankposten.

> [!IMPORTANT]
> Als de cheque wordt toegepast op een factuur, moet u de cheque eerst tegenboeken zodat de factuur kan worden terugbetaald en vervolgens de cheque nietig verklaren. Als de cheque is afgedrukt en er geen factuur mee is betaald, kiest u **Cheque alleen nietig verklaren** zoals beschreven in deze sectie.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de betreffende bankrekening, kies de actie **Bewerken** en kies vervolgens de actie **Chequeposten**.
3. Kies op de pagina **Chequeposten** de actie **Ongeldige cheque**.
4. Schakel het selectievakje **Cheque alleen nietig verklaren** in.
5. Kies de knop **OK**.

## <a name="to-view-a-summary-of-posted-checks"></a>Een overzicht weergeven van geboekte cheques

Als u geboekte cheques wilt controleren, bijvoorbeeld om meerdere cheques te verifiëren die aan één leverancier zijn betaald, kunt u het rapport **Bank - Cheques Detail** gebruiken.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bank - Cheques Detail** in en kies vervolgens de gerelateerde koppeling.
2. Stel filters als relevant in en kies de knop **Voorbeeld**.

## <a name="see-also"></a>Zie ook

[Betalingen uitvoeren](payables-make-payments.md)  
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Bankieren instellen](bank-setup-banking.md)  
[Een Positive Pay-bestand exporteren](finance-how-positive-pay.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
