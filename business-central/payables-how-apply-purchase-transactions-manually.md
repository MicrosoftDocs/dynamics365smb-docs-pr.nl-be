---
title: Betalingsontvangsten of terugbetalingen van leveranciers reconciliëren in het betalingsjournaal
description: 'Als u leveranciersbetalingen of terugbetalingen handmatig wilt verwerken, vereffent u het bedrag met een of meer openstaande leveranciersposten.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment application, payment processing, match payments'
ms.search.form: '62, 233, 522, 623'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="reconcile-vendor-payments-with-the-payment-journal-or-from-vendor-ledger-entries"></a>Leveranciersbetalingen reconciliëren met het betalingsdagboek of vanuit leveranciersposten
Wanneer u een betaling of terugbetaling van een leverancier ontvangt, moet u beslissen of u de betaling of terugbetaling vereffent met een of meer openstaande posten. U kunt het exacte bedrag opgeven waarmee u de betalingsontvangst of terugbetaling wilt vereffenen, en de leveranciersposten vervolgens slechts gedeeltelijk vereffenen. U moet alle leveranciersposten vereffenen om correcte leverancierstatistieken en -rapporten te verkrijgen van de rekeningoverzichten en rentefacturen.

> [!NOTE]  
>   Leveranciers geven soms een terugbetaling in plaats van een creditnota die als tegenrekening dient voor toekomstige facturen, met name wanneer u artikelen terugzendt die u al hebt betaald of wanneer u te veel hebt betaald voor een factuur.

U kunt als volgt leveranciersposten vereffenen op drie verschillende manieren:

* Door gegevens op bepaalde pagina's in te voeren, zoals de pagina **Betalingsdagboek** en de pagina **Dagboek betalingsreconciliatie**.
* Vanuit inkoopcreditnotadocumenten.
* Vanuit leveranciersposten, nadat inkoopdocumenten zijn geboekt maar nog niet vereffend.

> [!NOTE]  
>   Als het veld **Vereffeningsmethode** op de leverancierskaart **Saldo** bevat, kunnen betalingen handmatig worden vereffend met de oudste openstaande creditpost, als u niet handmatig opgeeft met welke post moet worden vereffend. Als de vereffeningsmethode voor een klant **Handmatig** is, moet u posten handmatig vereffenen.

U kunt leveranciersbetalingen handmatig op de gerelateerde inkoopdocumenten toepassen wanneer u de betalingen boekt op de pagina **Betalingsdagboek**. Zie voor meer informatie over het invullen van het betalingsdagboek [Betalingen uitvoeren](payables-make-payments.md).

U kunt ook leveranciersbetalingen en klantbetalingen vereffenen nadat de betalingen worden weergegeven als negatieve banktransacties bij uw bank. Op de pagina **Dagboek betalingsreconciliatie** kunt u functies voor het importeren van bankafschriften, automatische vereffening en bankrekeningvereffening gebruiken. Zie voor meer informatie [Betalingen vereffenen met automatische vereffening](receivables-how-reconcile-payments-auto-application.md).

## <a name="to-apply-a-payment-to-a-single-or-multiple-vendor-ledger-entries"></a>Een betaling vereffenen met een of meer leveranciersposten
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Betalingsdagboek** in en kies vervolgens de gerelateerde koppeling.
2. Voer op de pagina **Betalingsdagboek** op de eerste dagboekregel de betreffende gegevens over de betalingspost in.
3. Eén leverancierspost vereffenen:
   1. Selecteer in het veld **Vereffeningsnr.** het veld voor het openen van de pagina **Leveranciersposten vereffenen**.
   2. Selecteer op de pagina **Leveranciersposten vereffenen** de post waarmee de betaling moet worden vereffend.
   3. Voer op de regel in het veld **Te vereffenen bedrag** het bedrag in waarmee u de post wilt vereffenen.
4. Of meerdere leveranciersposten vereffenen:

   1. Kies de actie **Posten vereffenen**.
   2. Op de pagina **Leveranciersposten vereffenen** selecteert u de regels met de posten die u met de betaling wilt vereffenen.
   3. Kies de actie **Id toekennen**.  
   4. Voer op elke regel in het veld **Te vereffenen bedrag** het bedrag in waarmee u de afzonderlijke post wilt vereffenen.

      Als u geen bedrag opgeeft, wordt automatisch het maximumbedrag gebruikt. Onder aan de pagina **Leveranciersposten vereffenen** ziet u het bedrag in het veld Vereffend bedrag en kunt u controleren of de vereffening sluitend is.
5. Kies de knop **Ok**.
6. Kies de actie **Boeken** om het betalingsdagboek te boeken.

## <a name="to-apply-a-credit-memo-to-a-single-or-multiple-vendor-ledger-entries"></a>Een creditnota vereffenen met een of meer leveranciersposten:
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Inkoopcreditnota** in en kies vervolgens de gerelateerde koppeling.
2. Open de creditnota die u wilt vereffenen.
3. Voer de betreffende gegevens in de kop in.
4. Als u een enkele leverancierspost wilt vereffenen, selecteert u op het sneltabblad **Vereffening** in het veld **Vereffeningsnr.**, de post waarmee u het krediet wilt vereffenen. In het veld **Te vereffenen bedrag** voert u vervolgens het bedrag in waarmee de post moet worden vereffend.
5. Of meerdere leveranciersposten vereffenen:

   1. Kies de actie **Posten vereffenen**.
   2. Selecteer de regels met de posten waarmee u de creditnota wilt vereffenen.
   3. Kies de actie **Id toekennen**.  
   4. Voer op elke regel in het veld **Te vereffenen bedrag** het bedrag in waarmee u de afzonderlijke post wilt vereffenen.

       Als u geen bedrag opgeeft, wordt automatisch het maximumbedrag gebruikt. Onder aan de pagina **Leveranciersposten vereffenen** ziet u het bedrag in het veld **Vereffend bedrag** en kunt u controleren of de vereffening sluitend is.
6. Kies de knop **OK**.  
   De pagina **Inkoopcreditnota** bevat de post die u hebt geselecteerd in de velden **Vereffeningssoort** en **Vereffeningsnr.** De pagina bevat ook het bedrag van de creditnota dat moet worden geboekt, geherwaardeerd voor de mogelijke contantkortingen.
7. Kies de knop **Boeken** om de inkoopcreditnota te boeken.

## <a name="to-apply-posted-vendor-ledger-entries"></a>Geboekte leveranciersposten vereffenen
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Leveranciers** in en kies vervolgens de gerelateerde koppeling.
2. Open de betreffende leverancier met posten die reeds zijn geboekt.
3. Kies de actie **Posten** en kies vervolgens de actie **Posten vereffenen**.
4. Op de pagina **Leveranciersposten vereffenen** ziet u de openstaande posten voor de leverancier.
5. Selecteer de regel met de post die wordt vereffend.
6. Kies de actie **Id toekennen**.

    Het veld **Vereffenings-id** bevat drie sterretjes als u in een systeem met één gebruiker werkt, of bevat uw gebruikers-id als u in een systeem met meerdere gebruikers werkt.  
7. Voer op elke regel in het veld **Te vereffenen bedrag** het bedrag in waarmee u de afzonderlijke post wilt vereffenen.

    Als u geen bedrag opgeeft, wordt automatisch het maximumbedrag gebruikt. U ziet het bedrag in het veld **Vereffend bedrag**, onder aan de pagina **Leveranciersposten vereffenen**.
8. Kies de actie **Vereffening boeken**.  

    De pagina **Vereffening boeken** verschijnt met het documentnummer van de vereffeningspost en de boekingsdatum van de post met de meest recente boekingsdatum.
9. Kies de knop **OK** om de vereffening te boeken.

## <a name="to-apply-vendor-ledger-entries-in-different-currencies-to-one-another"></a>Leveranciersposten in verschillende valuta's onderling vereffenen
Als u van een leverancier koopt in de ene valuta en betaalt in de andere, kunt u de factuur toch met de betaling vereffenen.

Als u een post (Post 1) in de ene valuta vereffent met een post (Post 2) in een andere valuta, wordt de boekingsdatum van Post 1 gebruikt om de juiste wisselkoers te bepalen voor de conversie van de bedragen van Post 2. De juiste wisselkoers wordt opgezocht op de pagina **Valutawisselkoersen**. In dat geval moet u vereffening van leveranciersposten in verschillende valuta's inschakelen. Zie voor meer informatie [Vereffening van posten in verschillende valuta's inschakelen](finance-how-enable-application-ledger-entries-different-currencies.md)

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Betalingsdagboek** in en kies vervolgens de gerelateerde koppeling.
2. Open het journaal dat u wilt gebruiken en vul de eerste lege dagboekregel in met een valutacode.
3. Kies de actie **Posten vereffenen**.
4. Selecteer de regel met de post waarmee u de post in het betalingsdagboek wilt vereffenen, kies de actie **Id toekennen** en selecteer vervolgens de post waarmee u wilt vereffenen.
5. Klik op **OK** om terug te gaan naar het betalingsdagboek.
6. Boek het betalingsdagboek.

> [!IMPORTANT]  
>   Wanneer u posten in verschillende valuta's onderling vereffent, worden de posten automatisch omgezet in USD. Zelfs bij een vaste wisselkoers tussen de twee relevante valuta's, bijvoorbeeld USD en EUR, kan er een klein verschilbedrag ontstaan wanneer bedragen in de vreemde valuta worden omgezet naar de lokale valuta. Deze kleine verschilbedragen worden als winst- of verliesbedragen geboekt naar de rekening die u hebt opgegeven in de velden **Gereal. koerswinstrekening** of **Gereal. koersverliesrekening** van de pagina **Valuta's**. Het veld **Bedrag (lokale valuta)** wordt ook aangepast in de relevante leveranciersposten.

## <a name="to-unapply-an-application-of-vendor-entries"></a>De vereffening van leveranciersposten ongedaan maken
Als u een verkeerde vereffening ongedaan maakt, worden er stornoposten gemaakt die identiek zijn aan de oorspronkelijke post maar met een tegengesteld teken in het bedragveld, en geboekt voor alle posten, inclusief alle GB-boekingen die uit de vereffening voortkomen zoals contantkortingen en valutawinst- en verlies. De posten die waren afgesloten door de toepassing, worden heropend.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Leveranciers** in en kies vervolgens de gerelateerde koppeling.
2. Open de desbetreffende leverancierskaart.
3. Kies de actie **Posten**.
4. Selecteer de betreffende post en kies de actie **Vereffening posten ongedaan maken**.
5. Of kies de actie **Gedetailleerde post**.
6. Selecteer de vereffeningspost en kies de actie **Vereffening posten ongedaan maken**.
7. Vul de velden in de kop in en klik vervolgens op de knop **Vereffening ongedaan maken**.

> [!IMPORTANT]  
>   Als een post is vereffend door meer dan één vereffeningspost, moet u de vereffening van de laatste vereffeningspost het eerst ongedaan maken.

## <a name="see-also"></a>Zie ook
[Schulden](payables-manage-payables.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
