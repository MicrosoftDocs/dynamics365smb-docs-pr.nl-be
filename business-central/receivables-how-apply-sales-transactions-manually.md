---
title: Klantbetalingen reconciliëren met het ontvangstendagboek of vanuit klantenposten
description: Beschrijft hoe u kasontvangsten of terugbetalingen van klanten vereffent met een of meer openstaande klantposten. Dit maakt deel uit van het afstemmen van klantbetalingen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'payment process, cash receipt'
ms.search.form: '25, 255'
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="reconcile-customer-payments-with-the-cash-receipt-journal-or-from-customer-ledger-entries"></a>Klantbetalingen reconciliëren met het ontvangstendagboek of vanuit klantenposten

Wanneer u een betaling ontvangt van een klant of een terugbetaling doet, kunt u de ontvangst of betaling toepassen om openstaande debet- of creditposten te sluiten. U kunt het exacte te vereffenen bedrag opgeven. U kunt bijvoorbeeld gedeeltelijke betalingen vereffenen met klantenposten. Het sluiten van klantenposten garandeert dat gegevens zoals bijvoorbeeld klantstatistieken, rekeningoverzichten en rente actueel zijn.

> [!TIP]  
>   Op de pagina **Klantenposten** betekent een rood lettertype dat de gerelateerde betaling over de vervaldatum is. Als te late betalingen een probleem worden, kunnen we u helpen de frequentie ervan te verminderen. U kunt de extensie **Voorspelling van te late betalingen** inschakelen, die een voorspellend model gebruikt dat is ontwikkeld in Azure Machine Learning om de timing van betalingen te voorspellen. Deze voorspellingen helpen u openstaande tegoeden te reduceren en uw inningsstrategie te verfijnen. Als bijvoorbeeld wordt voorspeld dat een betaling te laat zal zijn, kunt u besluiten de betalingsvoorwaarden of de betalingsmethode voor de klant aan te passen. Zie [Voorspelling van te late betalingen](ui-extensions-late-payment-prediction.md) voor meer informatie.  

U kunt klantposten vereffenen op verschillende manieren:

* Door gegevens op specifieke pagina's in te voeren:
    * De pagina **Betalingsreconciliatiedagboek**. Zie voor meer informatie [Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md).
    * De pagina **Betalingsregistratie**. Zie [Klantbetalingen uit een lijst met onbetaalde verkoopdocumenten reconciliëren](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) voor meer informatie.
    * Het **Ontvangstendagboek**. Deze optie wordt hieronder beschreven.
* Door het veld **Vereffeningsnr.** op verkoopcreditnotadocumenten in te vullen. Deze optie wordt hieronder beschreven.
* Door de actie **Vereffenings-id instellen** op een klantenpost te gebruiken. Deze optie wordt hieronder beschreven.
* Door gebruik te maken van de actie **Posten vereffenen** op de pagina **Bankstorting** en vervolgens het factuurnummer invoeren in het veld **Vereffenings-id**. Zie [Bankstortingen maken](bank-create-bank-deposits.md) voor meer informatie.

> [!NOTE]  
>   Als het veld **Vereffeningsmethode** op de klantenkaart **Saldo** bevat, worden betalingen handmatig vereffend met de oudste openstaande creditpost als u niet handmatig een andere post opgeeft. Als de vereffeningsmethode **Handmatig** is, moet u posten altijd handmatig vereffenen.

## <a name="to-fill-and-post-a-cash-receipt-journal"></a>Een ontvangstendagboek invullen en boeken
Een kasontvangstjournaal is een soort dagboek. U kunt het gebruiken om transacties te boeken naar grootboek-, bank-, klant- en leveranciersrekeningen en rekeningen voor vaste activa. U kunt de betaling met een of meer debetposten vereffenen wanneer u de betaling boekt. U kunt deze ook later vanuit de geboekte posten vereffenen.
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Ontvangstendagboek** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Dagboek bewerken**.
3. Selecteer in het veld **Batchnaam** de juiste batch.
4. Vul het veld **Boekingsdatum** in.  
5. Selecteer **Betaling** in het veld **Documentsoort**.

    In het veld **Documentnr.** wordt de nummerreeks ingevuld die aan de batch is toegewezen.  
6. In het veld **Extern documentnr.** kunt u een identificatie opslaan, bijvoorbeeld het chequenummer van de klant.
7. Selecteer **Klant** in het veld **Rekeningsoort** .
8. Selecteer in het veld **Bankrekeningnr.** de relevante grootboekrekening.
9. Als u de vereffening tegelijkertijd met het dagboek wilt boeken, kunt u op een van de volgende manieren te werk gaan.
10. Selecteer in het veld **Tegenrekeningsoort** de optie **Grootboekrekening** voor contante betalingen en **Bankrekening** voor andere betalingen.
11. Selecteer in het veld **Tegenrekeningnr.** de grootboekrekening voor contante betalingen of de desbetreffende bankrekening voor andere betalingen.
12. Boek het dagboek.

## <a name="to-apply-a-payment-to-a-single-customer-ledger-entry"></a>Een betaling vereffenen met één klantenpost
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Ontvangstendagboek** in en kies de gerelateerde koppeling.
2. Kies de actie **Dagboek bewerken**.
3. Geef op de eerste dagboekregel de betreffende gegevens op over de post die u wilt vereffenen.
4. Voer **Betaling** in het veld **Documentsoort** in.
5. Voer **Klant** in het veld **Rekeningsoort** in.
6. Voer **Bank** in het veld **Tegenrekeningsoort** in.
7. Selecteer in het veld **Vereffeningsnr.** het veld voor het openen van de pagina **Klantposten vereffenen**.
8. Selecteer op de pagina **Klantposten vereffenen** de post waarmee de betaling moet worden vereffend.
9. Voer in het veld **Te vereffenen bedrag** het bedrag in waarmee u de post wilt vereffenen. Als u geen bedrag invoert, wordt automatisch het maximumbedrag gebruikt.

    Onder aan de pagina **Klantposten vereffenen** kunt u het specifieke bedrag in het veld **Vereffend bedrag** zien en ook of de vereffening sluitend is.  
10. Kies de knop **Ok**. Op de pagina **Ontvangstendagboek** ziet u nu de post in de velden **Vereffeningssoort** en **Vereffeningsnr.**
11. Boek het ontvangstendagboek.

## <a name="to-apply-a-payment-to-multiple-customer-ledger-entries"></a>Een betaling vereffenen met meerdere klantenposten
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Ontvangstendagboek** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Dagboek bewerken**.
3. Geef op de eerste dagboekregel de betreffende gegevens op over de post die u wilt vereffenen.
4. Voer **Betaling** in het veld **Documentsoort** in.
5. Voer **Klant** in het veld **Rekeningsoort** in.
6. Voer **Bank** in het veld **Tegenrekeningsoort** in.
7. Voer in het veld **Bedrag** de volledige betaling in als een negatief bedrag.
8. Kies de actie **Posten vereffenen** als u de betaling tijdens het boeken wilt vereffenen met meerdere klantposten.  
9. Selecteer de regels met de posten die u met de vereffeningspost wilt vereffenen en kies de actie **Id toekennen** .  
10. Voer op elke regel in het veld **Te vereffenen bedrag** het bedrag in waarmee u de afzonderlijke post wilt vereffenen. Als u geen bedrag invoert, wordt automatisch het maximumbedrag gebruikt.

    Onder aan de pagina **Klantposten vereffenen** kunt u het specifieke bedrag in het veld **Vereffend bedrag** zien en ook of de vereffening sluitend is.  
11. Kies de knop **Ok**.
12. Boek het ontvangstendagboek.

## <a name="to-apply-a-credit-memo-to-a-single-customer-ledger-entry"></a>Een creditnota vereffenen met één klantenpost
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopcreditnota's** in en kies vervolgens de gerelateerde koppeling.
2. Open de relevante verkoopcreditnota.
3. Als u de creditnota tijdens het boeken wilt toepassen op één klantenpost, selecteert u in het veld **Vereffeningsnr.** de post waarop u de betaling wilt toepassen.
4. Voer op de regel in het veld **Te vereffenen bedrag** het bedrag op waarmee u de post wilt vereffenen.  

    Als u geen bedrag opgeeft, wordt automatisch het maximumbedrag gebruikt. Onder aan de pagina **Klantposten vereffenen** kunt u het specifieke bedrag in het veld **Vereffend bedrag** zien en ook of de vereffening sluitend is.    
5. Kies de knop **OK**. Op de pagina **Verkoopcreditnota** ziet u nu de post die u hebt geselecteerd in de velden **Vereffeningssoort** en **Vereffeningsnr.** En het bedrag van de creditnota dat moet worden geboekt, geherwaardeerd voor de mogelijke contantkortingen.
6. Boek de creditnota.

## <a name="to-apply-a-credit-memo-to-multiple-customer-ledger-entries"></a>Een creditnota vereffenen met meerdere klantenposten
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopcreditnota's** in en kies vervolgens de gerelateerde koppeling.
2. Open de relevante verkoopcreditnota.
3. Kies de actie **Posten vereffenen** als u de creditnota tijdens het boeken wilt vereffenen met meerdere klantposten.
4. Selecteer de regels met de posten die u met de vereffeningspost wilt vereffenen en kies de actie **Id toekennen** .
5. Voer op elke regel in het veld **Te vereffenen bedrag** het bedrag in waarmee u de afzonderlijke post wilt vereffenen. Als u geen bedrag invoert, wordt automatisch het maximumbedrag gebruikt.  

    Onder aan de pagina **Klantposten vereffenen** kunt u het specifieke bedrag in het veld **Vereffend bedrag** zien en ook of de vereffening sluitend is.  
6. Kies de knop **OK**. De pagina **Verkoopcreditnota** bevat nu het bedrag van de creditnota die moet worden geboekt, geherwaardeerd voor alle mogelijke contantkortingen.
7. Boek de creditnota.

## <a name="to-apply-posted-customer-ledger-entries"></a>Geboekte klantenposten vereffenen
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Klanten** in en kies vervolgens de gerelateerde koppeling.
2. Open de klantenkaart voor de klant met de posten die u wilt vereffenen.
3. Kies de actie **Posten** en selecteer de regel met de post die u als de vereffeningspost wilt gebruiken.
4. Kies de actie **Posten vereffenen**. De pagina **Klantposten vereffenen** wordt geopend met daarin de openstaande posten voor de klant.
5. Selecteer de regels met de posten die u met de vereffeningspost wilt vereffenen en kies de actie **Id toekennen** .
6. Voer voor elke regel in het veld **Te vereffenen bedrag** het bedrag in waarmee u de afzonderlijke post wilt vereffenen. Als u geen bedrag invoert, wordt automatisch het maximumbedrag gebruikt.  

    U ziet het specifieke bedrag in het veld **Vereffend bedrag** onder aan de pagina **Klantposten vereffenen**.  
7. Kies de actie **Vereffening boeken**. De pagina **Vereffening boeken** verschijnt met het documentnummer van de vereffeningspost en de boekingsdatum van de post met de meest recente boekingsdatum.  
8. Kies de knop **OK** om de vereffening te boeken.

    Als de vereffening geboekt is en dit heeft tot resultaat gehad dat klantenposten zijn afgesloten, staat er geen vinkje meer bij deze grootboekposten in het veld **Open**.    
9. Als u de posten wilt zien, kiest u het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies vervolgens de gerelateerde koppeling. Ga naar de kaart voor de relevante klant om de posten te zien.  

In het overzicht met posten kunt u zien dat het selectievakje **Open** is uitgeschakeld op de regel met de post die volledig is vereffend.  

> [!NOTE]  
>   Nadat u een post hebt geselecteerd op de pagina **Klantposten vereffenen** of nadat u diverse posten hebt geselecteerd door de **Vereffenings-id** in te stellen, bevat het veld **Vereffend bedrag** op de dagboekregel de som van de resterende bedragen voor de geboekte posten die u hebt geselecteerd, tenzij het veld al een andere waarde bevat. Als u **Saldo** selecteert in het veld **Vereffeningsmethode** op de klantenkaart, wordt de betaling automatisch vereffend.

## <a name="to-apply-customer-ledger-entries-in-different-currencies-to-one-another"></a>Klantenposten in verschillende valuta's met elkaar vereffenen
Als u een artikel aan een klant verkoopt in een bepaalde valuta en een betaling in een andere valuta ontvangt, kunt u de betaling nog steeds vereffenen met de factuur.  

Hier volgt een voorbeeld. U kunt Post 1 in de ene valuta vereffenen met Post 2 in een andere valuta. De boekingsdatum op Post 1 wordt gebruikt om de wisselkoers te vinden die moet worden gebruikt om bedragen op Post 2 om te rekenen. De wisselkoers wordt opgezocht op de pagina **Valutawisselkoersen**.  

Het vereffenen van klantposten in verschillende valuta's moet zijn ingeschakeld. Zie voor meer informatie [Vereffening van posten in verschillende valuta's inschakelen](finance-how-enable-application-ledger-entries-different-currencies.md).  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voert u **Ontvangstendagboek** in en kiest u vervolgens de gerelateerde koppeling.
2. Open het dagboek dat u wilt gebruiken en vul de eerste lege dagboekregel in met een valutacode.
3. Kies de actie **Posten vereffenen**.
4. Selecteer de regel met de post waarmee u de post in het ontvangstendagboek wilt vereffenen, kies de actie **Id toekennen** en selecteer vervolgens de post waarmee u wilt vereffenen.
5. Klik op de knop **OK** om terug te gaan naar het ontvangstendagboek.
6. Boek het verkoopdagboek.  

> [!IMPORTANT]  
>   Wanneer u posten in verschillende valuta's vereffent, worden de posten omgezet in USD. Alhoewel een vaste wisselkoers wordt gehanteerd tussen de twee relevante valuta's, bijvoorbeeld USD en EUR, kan er een klein verschilbedrag ontstaan wanneer bedragen worden omgezet in de lokale valuta. Deze kleine verschilbedragen worden als winst- of verliesbedragen geboekt naar de rekening die u hebt opgegeven in de velden **Gereal. koerswinstrekening** of **Gereal. koersverliesrekening** van de pagina **Valuta's**. Het veld **Bedrag (lokale valuta)** wordt ook aangepast in de leveranciersposten.  

## <a name="to-correct-an-application-of-customer-entries"></a>Een vereffening van klantposten corrigeren
Wanneer u een vereffening corrigeert, worden corrigerende posten gemaakt en geboekt voor alle posten. De corrigerende posten zijn hetzelfde als de originelen, maar hebben een tegenovergesteld teken in het veld **Bedrag**. De correctieboekingen omvatten alle grootboekposten die zijn afgeleid van de vereffening. Bijvoorbeeld de betalingskorting en valutawinsten/-verliezen. De posten die waren afgesloten door de toepassing, worden heropend.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Klanten** in en kies vervolgens de gerelateerde koppeling.
2. Open de relevante klantenkaart.
3. Kies de actie **Posten**.
4. Selecteer de betreffende post en kies de actie **Vereffening posten ongedaan maken**.
5. Of kies de actie **Gedetailleerde post**.
6. Selecteer de vereffeningspost en kies de actie **Vereffening posten ongedaan maken**.
7. Vul de velden in de kop in en klik vervolgens op de knop **Vereffening ongedaan maken**.  

> [!IMPORTANT]  
>   Als een post is vereffend door meer dan één vereffeningspost, moet u de vereffening van de laatste vereffeningspost het eerst ongedaan maken.  

## <a name="see-also"></a>Zie ook
[Tegoeden beheren](receivables-manage-receivables.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
