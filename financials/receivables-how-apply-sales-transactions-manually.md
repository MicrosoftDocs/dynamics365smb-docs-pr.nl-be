---
title: "Klantenposten vereffenen om handmatig klantbetalingen te reconciliëren | Microsoft Docs"
description: Beschrijft hoe u kasontvangsten of terugbetalingen van klanten vereffent met een of meer openstaande klantposten en klantbetalingen reconcilieert.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipt
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 6e00e9cbc1b1dc8674ccf83876809496a563b0be
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---
# <a name="reconcile-customer-payments-manually"></a>Klantbetalingen handmatig reconciliëren
Wanneer u een bedrag ontvangt van een klant of een terugbetaling doet, moet u bedenken of de ontvangst of betaling moet worden vereffend om een of meer openstaande debet- of creditposten te sluiten. U kunt het exacte bedrag opgeven dat u wilt vereffenen. U kunt bijvoorbeeld gedeeltelijke betalingen vereffenen met klantenposten. Het sluiten van klantenposten garandeert dat gegevens zoals bijvoorbeeld klantstatistieken, rekeningoverzichten, en rente correct zijn.

> [!NOTE]  
>   In het venster **Klantenposten** betekent een rood lettertype dat de gerelateerde betaling over de vervaldatum is.

U kunt klantposten vereffenen op verschillende manieren:

* Door gegevens in bepaalde vensters in te voeren, zoals de vensters **Ontvangstendagboek** of **Dagboek betalingsreconciliatie**.
* Vanuit verkoopcreditnotadocumenten.
* Vanuit klantposten worden after sales-documenten geboekt, maar niet vereffend.

> [!NOTE]  
>   Als het veld **Vereffeningsmethode** op de klantenkaart **Saldo** bevat, worden betalingen handmatig vereffend met de oudste openstaande creditpost als u niet handmatig een andere post opgeeft. Als de vereffeningsmethode **Handmatig** is, moet u posten altijd handmatig vereffenen.

In het venster **Ontvangstendagboek** kunt u klantbetalingen handmatig vereffenen. Een ontvangstendagboek is een soort algemeen dagboek, waarmee u transacties boekt naar grootboek-, bank-, klanten-, leveranciers- en vaste-activumrekeningen. U kunt de betaling met een of meer debetposten vereffenen wanneer u de betaling boekt of u kunt deze later vanuit de geboekte posten vereffenen.

U kunt klantbetalingen en leveranciersbetalingen in het venster **Dagboek betalingsreconciliatie** vereffenen door middel van functies voor import van bankafschriften, automatische vereffening en bankrekeningreconciliatie. Zie voor meer informatie [Betalingen vereffenen met automatische vereffening](receivables-how-reconcile-payments-auto-application.md). U kunt klantbetalingen ook reconciliëren op basis van een lijst met onbetaalde verkoopdocumenten in het venster **Betalingsregistratie**. Zie [Klantbetalingen van een lijst met onbetaalde verkoopdocumenten reconciliëren](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md) voor meer informatie

## <a name="to-fill-and-post-a-cash-receipt-journal"></a>Een ontvangstendagboek invullen en boeken
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Ontvangstendagboek** in en klik vervolgens op de gerelateerde koppeling.
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
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Ontvangstendagboek** in en klik op de gerelateerde koppeling.
2. Kies de actie **Dagboek bewerken**.
3. Geef op de eerste dagboekregel de betreffende gegevens op over de post die u wilt vereffenen.
4. Voer **Betaling** in het veld **Documentsoort** in.
5. Voer **Klant** in het veld **Rekeningsoort** in.
6. Voer **Bank** in het veld **Tegenrekeningsoort** in.
7. Selecteer in het veld **Vereffeningsnr.** het veld voor het openen van het venster **Klantenposten vereffenen**.
8. Selecteer in het venster **Klantposten vereffenen** de post waarmee de betaling moet worden vereffend.
9. Voer in het veld **Te vereffenen bedrag** het bedrag in waarmee u de post wilt vereffenen. Als u geen bedrag invoert, wordt automatisch het maximumbedrag gebruikt.

    Onder aan het venster **Klantposten vereffenen** kunt u het specifieke bedrag in het veld **Vereffend bedrag** zien en ook of de vereffening sluitend is.  
10. Kies de knop **Ok**. In het venster **Ontvangstendagboek** ziet u nu de post die u hebt geselecteerd in de velde **Vereffeningssoort** en **Vereffeningsnr.**
11. Boek het ontvangstendagboek.

## <a name="to-apply-a-payment-to-multiple-customer-ledger-entries"></a>Een betaling vereffenen met meerdere klantenposten
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Ontvangstendagboek** in en klik vervolgens op de gerelateerde koppeling.
2. Kies de actie **Dagboek bewerken**.
3. Geef op de eerste dagboekregel de betreffende gegevens op over de post die u wilt vereffenen.
4. Voer **Betaling** in het veld **Documentsoort** in.
5. Voer **Klant** in het veld **Rekeningsoort** in.
6. Voer **Bank** in het veld **Tegenrekeningsoort** in.
7. Voer in het veld **Bedrag** de volledige betaling in als een negatief bedrag.
8. Kies de actie **Posten vereffenen** als u de betaling tijdens het boeken wilt vereffenen met meerdere klantposten.  
9. Selecteer de regels met de posten die u met de vereffeningspost wilt vereffenen en kies de actie **Id toekennen** .  
10. Voer op elke regel in het veld **Te vereffenen bedrag** het bedrag in waarmee u de afzonderlijke post wilt vereffenen. Als u geen bedrag invoert, wordt automatisch het maximumbedrag gebruikt.

    Onder aan het venster **Klantposten vereffenen** kunt u het specifieke bedrag in het veld **Vereffend bedrag** zien en ook of de vereffening sluitend is.  
11. Kies de knop **Ok**.
12. Boek het ontvangstendagboek.

## <a name="to-apply-a-credit-memo-to-a-single-customer-ledger-entry"></a>Een creditnota vereffenen met één klantenpost
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verkoopcreditnota's** in en klik vervolgens op de gerelateerde koppeling.
2. Open de relevante verkoopcreditnota.
3. Als u de creditnota tijdens het boeken wilt toepassen op één klantenpost, selecteert u in het veld **Vereffeningsnr.** de post waarop u de betaling wilt toepassen.
4. Voer op de regel in het veld **Te vereffenen bedrag** het bedrag op waarmee u de post wilt vereffenen.  

    Als u geen bedrag opgeeft, wordt automatisch het maximumbedrag gebruikt. Onder aan het venster **Klantposten vereffenen** kunt u het specifieke bedrag in het veld **Vereffend bedrag** zien en ook of de vereffening sluitend is.    
5. Kies de knop **Ok**. In het venster **Verkoopcreditnota** ziet u nu de post die u hebt geselecteerd in de velden **Vereffeningssoort** en **Vereffeningsnr.** En het bedrag van de creditnota dat moet worden geboekt, geherwaardeerd voor de mogelijke contantkortingen.
6. Boek de creditnota.

## <a name="to-apply-a-credit-memo-to-multiple-customer-ledger-entries"></a>Een creditnota vereffenen met meerdere klantenposten
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verkoopcreditnota's** in en klik vervolgens op de gerelateerde koppeling.
2. Open de relevante verkoopcreditnota.
3. Kies de actie **Posten vereffenen** als u de creditnota tijdens het boeken wilt vereffenen met meerdere klantposten.
4. Selecteer de regels met de posten die u met de vereffeningspost wilt vereffenen en kies de actie **Id toekennen** .
5. Voer op elke regel in het veld **Te vereffenen bedrag** het bedrag in waarmee u de afzonderlijke post wilt vereffenen. Als u geen bedrag invoert, wordt automatisch het maximumbedrag gebruikt.  

    Onder aan het venster **Klantposten vereffenen** kunt u het specifieke bedrag in het veld **Vereffend bedrag** zien en ook of de vereffening sluitend is.  
6. Kies de knop **Ok**. Het venster **Verkoopcreditnota** bevat nu het bedrag van de creditnota die moet worden geboekt, geherwaardeerd voor alle mogelijke contantkortingen.
7. Boek de creditnota.

## <a name="to-apply-posted-customer-ledger-entries"></a>Geboekte klantenposten vereffenen
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Klanten** in en klik vervolgens op de gerelateerde koppeling.
2. Open de klantenkaart voor de klant met de posten die u wilt vereffenen.
3. Kies de actie **Posten** en selecteer de regel met de post die u als de vereffeningspost wilt gebruiken.
4. Kies de actie **Posten vereffenen**. Het venster **Klantposten vereffenen** wordt geopend met daarin de openstaande posten voor de klant.
5. Selecteer de regels met de posten die u met de vereffeningspost wilt vereffenen en kies de actie **Id toekennen** .
6. Voer voor elke regel in het veld **Te vereffenen bedrag** het bedrag in waarmee u de afzonderlijke post wilt vereffenen. Als u geen bedrag invoert, wordt automatisch het maximumbedrag gebruikt.  

    U ziet het specifieke bedrag in het veld **Vereffend bedrag** onder aan het venster **Klantposten vereffenen**.  
7. Kies de actie **Vereffening boeken**. Het venster **Vereffening boeken** verschijnt met het documentnummer van de vereffeningspost en de boekingsdatum van de post met de meest recente boekingsdatum.  
8. Kies de knop **OK** om de vereffening te boeken.

    Als de vereffening geboekt is en dit heeft tot resultaat gehad dat klantenposten zijn afgesloten, staat er geen vinkje meer bij deze grootboekposten in het veld **Open**.    
9. Als u de posten wilt zien, kiest u het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voert u **Klanten** in en kiest u vervolgens de gerelateerde koppeling. Ga naar de kaart voor de relevante klant om de posten te zien.  

In het overzicht met posten kunt u zien dat het selectievakje **Open** is uitgeschakeld op de regel met de post die volledig is vereffend.  

> [!NOTE]  
>   Nadat u een post hebt geselecteerd in het venster **Klantposten vereffenen** of nadat u diverse posten hebt geselecteerd door de **Vereffenings-id** in te stellen, bevat het veld **Vereffend bedrag** op de dagboekregel de som van de resterende bedragen voor de geboekte posten die u hebt geselecteerd, tenzij het veld al een andere waarde bevat. Als u **Saldo** selecteert in het veld **Vereffeningsmethode** op de klantenkaart, wordt de betaling automatisch vereffend.

## <a name="to-apply-customer-ledger-entries-in-different-currencies-to-one-another"></a>Klantenposten in verschillende valuta's met elkaar vereffenen
Als u een artikel aan een klant verkoopt in een bepaalde valuta en een betaling in een andere valuta ontvangt, kunt u de betaling nog steeds vereffenen met de factuur.  

Als u een post (Post 1) in de ene valuta vereffent met een post (Post 2) in een andere valuta, wordt de boekingsdatum van Post 1 gebruikt om de juiste wisselkoers te bepalen voor de conversie van de bedragen van Post 2. De juiste wisselkoers wordt opgezocht in het venster **Valutawisselkoersen**.  

Het vereffenen van klantposten in verschillende valuta's moet zijn ingeschakeld. Zie voor meer informatie [Vereffening van posten in verschillende valuta's inschakelen](finance-how-enable-application-ledger-entries-different-currencies.md).  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Ontvangstendagboek** in en klik vervolgens op de gerelateerde koppeling.
2. Open het dagboek dat u wilt gebruiken en vul de eerste lege dagboekregel in met een valutacode.
3. Kies de actie **Posten vereffenen**.
4. Selecteer de regel met de post waarmee u de post in het ontvangstendagboek wilt vereffenen, kies de actie **Id toekennen** en selecteer vervolgens de post waarmee u wilt vereffenen.
5. Klik op de knop **OK** om terug te gaan naar het ontvangstendagboek.
6. Boek het verkoopdagboek.  

> [!IMPORTANT]  
>   Wanneer u posten in verschillende valuta's vereffent, worden de posten omgezet in USD. Alhoewel een vaste wisselkoers wordt gehanteerd tussen de twee relevante valuta's, bijvoorbeeld USD en EUR, kan er een klein verschilbedrag ontstaan wanneer bedragen worden omgezet in de lokale valuta. Deze kleine verschilbedragen worden als winst- of verliesbedragen geboekt naar de rekening die u hebt opgegeven in de velden **Gereal. koerswinstrekening** of **Gereal. koersverliesrekening** van het venster **Valuta's**. Het veld **Bedrag (lokale valuta)** wordt ook aangepast in de leveranciersposten.  

## <a name="to-correct-an-application-of-customer-entries"></a>Een vereffening van klantposten corrigeren
Als u een vereffening corrigeert, worden er stornoposten gemaakt die identiek zijn aan de oorspronkelijke post maar met een tegengesteld teken in het bedragveld. Deze stornoposten worden geboekt voor alle posten, inclusief alle GB-boekingen die uit de vereffening voortkomen zoals contantkortingen en valutawinst- en verlies. De posten die waren afgesloten door de toepassing worden heropend.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Klanten** in en klik vervolgens op de gerelateerde koppeling.
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
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

