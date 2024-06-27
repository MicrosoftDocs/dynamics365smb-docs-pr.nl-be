---
title: Betalingen doen aan onbetaalde verkoopdocumenten
description: 'U vereffent door klanten betaalde bedragen met gerelateerde verkoopdocumenten en boekt de betaling om de klant, het grootboek en bankposten bij te werken.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'payment process, cash receipts, customer payment'
ms.search.form: '1290, 1294, 1287'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# <a name="reconcile-customer-payments-from-a-list-of-unpaid-sales-documents"></a>Klantbetalingen uit een lijst met onbetaalde verkoopdocumenten reconciliëren

Nadat klanten elektronische betalingen naar uw bankrekening hebben gedaan, moet u de volgende acties ondernemen:

* Elk betaald bedrag vereffenen met het bijbehorende verkoopdocument.
* De betaling boeken om de klant- grootboek- en bankposten bij te werken.

Afhankelijk van uw zakelijke behoeften kunt u op verschillende manieren betalingen registreren: handmatig, automatisch en door middel van betalingsservices.  

> [!NOTE]  
> U kunt dezelfde taken uitvoeren, inclusief leveranciersbetalingen, op de pagina **Betalingsreconciliatiedagboek**. U kunt bijvoorbeeld bankafschriften importeren, automatische vereffening gebruiken en bankrekeningen afstemmen. Zie voor meer informatie [Betalingen vereffenen met automatische vereffening](receivables-how-reconcile-payments-auto-application.md).

Gebruik de pagina **Klantbetalingen registreren** om interne rekeningen in balans te brengen door gebruik te maken van actuele contante cijfers om ervoor te zorgen dat betalingen worden geïnd. U kunt snel individuele of lump-sumbetalingen verifiëren en boeken, kortingsbetalingen verwerken en de onbetaalde documenten vinden.

U moet betalingen boeken voor verschillende klanten met verschillende betalingsdatums als afzonderlijke betalingen. Betalingen voor dezelfde klant met dezelfde betaaldatum kunnen worden geboekt als lump-sum bedrag. Lump-sumbetalingen zijn handig, bijvoorbeeld, als een klant een enkele betaling heeft gedaan die meerdere verkoopfacturen omvat.

## <a name="to-set-up-the-payment-registration-journal"></a>Instellen van het betalingregistratiedagboek

Omdat u verschillende betalingssoorten naar verschillende tegenrekeningen kunt boeken, moet u een tegenrekening op de pagina **Instelling van betalingsregistratie** selecteren voordat u betalingen begint te verwerken. Als u altijd naar dezelfde tegenrekening boekt, kunt u die rekening instellen als de standaard en deze stap elke keer dat u de pagina **Klantbetalingen registreren** opent, vermijden.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Instelling van betalingsregistratie** in en kies vervolgens de gerelateerde koppeling. U kunt ook de actie **Instellingen** kiezen op de pagina **Klantbetalingen registreren**.
2. Vul de velden van de pagina **Instelling van betalingsregistratie** in. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)].  

> [!TIP]
> U kunt het gemakkelijker te maken om later boekingen te identificeren die via het journaal zijn geboekt door een specifieke nummerreeks aan het betalingsdagboek toe te wijzen. De nummerreeks is handig als u betalingsreconciliatiedagboeken gebruikt om betalingen te registreren en te vereffenen.

## <a name="to-register-customer-payments-individually"></a>Klantbetalingen afzonderlijk registreren

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klantbetalingen registreren** in en kies vervolgens de gerelateerde koppeling.  

    De pagina **Klantbetalingen registreren** bevat alle geboekte documenten waarvoor een betaling kan worden geregistreerd. U kunt de pagina ook openen vanaf de pagina's **Klanten** en **Klantenkaart**, gefilterd voor de opgegeven klant.  
2. Schakel het selectievakje **Is betaald** in op de regel die het geboekte document vertegenwoordigt waarvoor een betaling is gedaan.
3. Voer in het veld **Ontvangen op** de datum in waarop de betaling is gedaan. Deze datum kan van de werkdatum verschillen.  

   Als het selectievakje **Ontvangstdatum automatisch invullen** op de pagina **Instelling van betalingsregistratie** is geselecteerd, bevat het veld **Ontvangen op** de werkdatum.  
4. Voer in het veld **Ontvangen bedrag** het bedrag in dat is betaald.

    Voor volledige betalingen is dit bedrag gelijk aan het bedrag in het veld **Restbedrag** op de regel. Voor gedeeltelijke betalingen is dit bedrag lager dan het bedrag in het veld **Restbedrag** op de regel.
5. Herhaal stap 2-4 voor andere regels voor geboekte documenten waarvoor betalingen zijn verricht.  
6. Kies de actie **Betalingen boeken**.  

De betalingsgegevens worden geboekt voor documenten op regels waarvoor het selectievakje **Is betaald** is geselecteerd. Betalingenposten worden geboekt naar grootboek-, bank- en klantrekeningen.

## <a name="to-reconcile-lump-sum-payments"></a>Lump-sum betalingen reconciliëren

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Klantbetalingen registreren** in en kies vervolgens de gerelateerde koppeling.
2. Schakel het selectievakje **Is betaald** in op de regels voor geboekte documenten voor dezelfde klant en voor wie een lump-sum betaling is verricht.  

    > [!NOTE]  
    > De klant in het veld **Naam** moet hetzelfde zijn op alle regels om de lump-sum betaling te bevatten.  

    Als het selectievakje **Ontvangstdatum automatisch invullen** op de pagina **Instelling van betalingsregistratie** is geselecteerd, bevat het veld **Ontvangen op** de werkdatum.  
3. Voer in het veld **Ontvangen op** de datum in waarop de betaling is gedaan. Deze datum kan van de werkdatum verschillen.  

    > [!NOTE]  
    > Deze datum moet hetzelfde zijn op alle regels die als lump-sum betaling worden geboekt.  
4. Voer in het veld **Ontvangen bedrag** bedragen in op meerdere regels die samen het lump-sum bedrag vormen.  

    > [!TIP]  
    > Probeer zoveel mogelijk volledige betalingen te boeken met het lump-sum bedrag. Voer op zoveel mogelijk regels bedragen in die hetzelfde zijn als het bedrag in het veld **Restbedrag**.  
5. Herhaal stap 2-4 voor andere regels die geboekte documenten vertegenwoordigen voor dezelfde klant voor wie een lump-sum betaling is verricht.  
6. Kies de actie **Als lump-sum betaling boeken**.

   De betalingsgegevens worden geboekt voor documenten op regels waarvoor het selectievakje **Is betaald** is geselecteerd. Betalingsposten worden geboekt naar grootboek-, bank- en klantrekeningen. Elke betaling wordt toegepast op het bijbehorende geboekte verkoopdocument.  

Als een betaling in de bank niet op een regel op de pagina **Klantbetalingen registreren** wordt weergegeven, komt dat mogelijk doordat het betreffende document niet is geboekt. In dat geval kunt u een zoekfunctie gebruiken om het document snel te vinden en te boeken om de betaling te verwerken. Zie [Een specifiek verkoopdocument zoeken dat niet volledig is gefactureerd](#to-find-a-specific-sales-document-that-isnt-fully-invoiced) voor meer informatie.  

Als een betaling in de bank niet wordt weergegeven door een document, kunt u een vooraf ingevulde diversendagboekregel op de pagina **Klantbetalingen registreren** openen om de betaling direct bij de tegenrekening te boeken zonder de betaling met een document te vereffenen. U kunt de betaling ook in het dagboek registreren tot de oorsprong van de betaling is opgelost. Zie [Een betaling zonder een gekoppeld document registreren of boeken](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-record-or-post-a-payment-without-a-related-document) voor meer informatie.  

## <a name="to-process-customer-payments-with-discounts-manually"></a>Klantbetalingen met kortingen handmatig verwerken

Als u een contantkorting overeenkomt met de klant, kunnen de betalingsbedragen lager zijn dan de factuurbedragen als betalingen plaatsvinden voor de afgesproken kortingsdatum.  

In de onderstaande procedures worden procedures uitgelegd voor het boeken van betalingen met korting op de pagina **Betalingsregistratie**.  

* Het betalingsbedrag is gelijk aan het overgebleven gekorte bedrag en de betaaldatum is voor de kortingsdatum. U boekt de betaling in de huidige hoedanigheid.  
* Het betalingsbedrag is gelijk aan het overgebleven gekorte bedrag maar de betaaldatum is na de kortingsdatum. U boekt de betaling als gedeeltelijk. Het document blijft openstaan om her restbedrag te innen/betalen. U kunt de kortingsdatum ook later instellen om de volledige betaling toe te staan.  
* Het betalingsbedrag is lager dan het resterende gekorte bedrag. U boekt de betaling als gedeeltelijk. Het document blijft openstaan om her restbedrag te innen/betalen.  
* Het betalingsbedrag is hoger dan het resterende gekorte bedrag. U boekt de betalingen in de huidige hoedanigheid. Alleen het restbedrag wordt geboekt. Het extra bedrag wordt gecrediteerd aan de klant.  

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-and-where-the-payment-date-is-before-the-discount-date"></a>Een betalingsbedrag verwerken dat gelijk is aan het gekorte bedrag en waar de betaaldatum voor de kortingsdatum is

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klantbetalingen registreren** in en kies vervolgens de gerelateerde koppeling.  
2. Voer het betalingsbedrag in het veld **Ontvangen bedrag** in. Het bedrag is gelijk aan het bedrag in het veld **Restbedrag incl. korting**.

    Het selectievakje **Is betaald** wordt automatisch ingeschakeld en het veld **Ontvangen op** wordt ingevuld met de werkdatum.
3. Voer de betalingsdatum in het veld **Ontvangen op** in. De datum is eerder dan de datum in het veld **Vervaldatum contantkort.**
4. Controleer of het veld **Restbedrag** nul (0) bevat.  
5. Kies de actie **Betalingen boeken** om de volledige gehele betaling te boeken naar de grootboek-, bank-, en klantrekeningen.

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-but-where-the-payment-date-is-after-the-discount-date"></a>Een betalingsbedrag verwerken dat gelijk is aan het gekorte bedrag, maar waar de betaaldatum na de kortingsdatum is

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klantbetalingen registreren** in en kies vervolgens de gerelateerde koppeling.  
2. Voer het betalingsbedrag in het veld **Ontvangen bedrag** in. Het bedrag is gelijk aan het bedrag in het veld **Restbedrag incl. korting**.

    Het selectievakje **Is betaald** wordt automatisch ingeschakeld en het veld **Ontvangen op** wordt ingevuld met de werkdatum.
3. In het veld **Ontvangen op** voert u een betaaldatum in die na de datum in het veld **Vervaldatum contantkort.** ligt.

   De datumvelden worden rood weergegeven en een foutbericht wordt weergegeven onder op de pagina. De volgende twee stappen lossen dat op.
4. Kies de actie **Details**.  
5. Voer op de pagina **Betalingsregistratiegegevens** in het veld **Vervaldatum contantkort.** op het sneltabblad **Contantkorting** een datum in die later is dan de datum in het veld **Ontvangen op** op de pagina **Betalingsregistratie**.  

    De foutmelding en het rode lettertype verdwijnen en u kunt doorgaan met de verminderde betaling te verwerken.
6. Controleer of het veld **Restbedrag** het bedrag bevat dat resteert om het volledige factuurbedrag te betalen.  
7. Kies de actie **Betalingen boeken** om de gedeeltelijke betaling te boeken naar de grootboek-, bank-, en klantrekeningen.  

Het bijbehorende document blijft open.

### <a name="to-process-a-payment-that-is-lower-than-the-remaining-discounted-amount"></a>Een betaling verwerken die lager is dan het resterende gekorte bedrag

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klantbetalingen registreren** in en kies vervolgens de gerelateerde koppeling.  
2. Voer het betalingsbedrag in het veld **Ontvangen bedrag** in. Het bedrag is lager dan het bedrag in het veld **Rest.bedrag incl. korting**.

    Het selectievakje **Is betaald** wordt automatisch ingeschakeld en het veld **Ontvangen op** wordt ingevuld met de werkdatum.  
3. Voer de betalingsdatum in het veld **Ontvangen op** in. De datum is eerder dan de datum in het veld **Vervaldatum contantkort.**
4. Controleer of het veld **Restbedrag** het bedrag bevat dat resteert om het gekorte bedrag te betalen.  
5. Kies de actie **Betalingen boeken** om de gedeeltelijke betaling te boeken naar de grootboek-, bank-, en klantrekeningen.  

Het bijbehorende document blijft open.

### <a name="to-process-a-payment-that-is-more-than-the-remaining-discounted-amount"></a>Een betaling verwerken die groter is dan het resterende gekorte bedrag

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Klantbetalingen registreren** in en kies vervolgens de gerelateerde koppeling.  
2. Voer het betalingsbedrag in het veld **Ontvangen bedrag** in. Het bedrag is groter dan het bedrag in het veld **Rest.bedrag incl. korting**.  

    Het selectievakje **Is betaald** wordt automatisch ingeschakeld en het veld **Ontvangen op** wordt ingevuld met de werkdatum.
3. Voer de betalingsdatum in het veld **Ontvangen op** in. De datum is eerder dan de datum in het veld **Vervaldatum contantkort.**
4. Controleer of het veld **Restbedrag** nul (0) bevat.  
5. Kies de actie **Betalingen boeken** om de volledige gehele betaling te boeken naar de grootboek-, bank-, en klantrekeningen.  

Het bijbehorende document is gesloten, en het overtollige betalingsbedrag is gecrediteerd aan de klant.  

## <a name="to-find-a-specific-sales-document-that-isnt-fully-invoiced"></a>Een specifiek verkoopdocument zoeken dat niet volledig is gefactureerd

De pagina **Klantbetalingen registreren** ondersteunt u bij taken die nodig zijn om interne rekeningen in overeenstemming te brengen met werkelijke geldcijfers om effectieve inning van klanten te garanderen. Het bevat openstaande inkomende betalingen als regels die verkoopdocumenten vertegenwoordigen waar een betalingstermijn voor een bedrag is verstreken.  

Wanneer een betaling wordt gedaan, vastgelegd bij de bank of anderszins, wordt het verkoop- of inkoopdocument doorgaans weergegeven als een regel op de pagina **Klantbetalingen registreren**. Het document wacht totdat u de betaling naar het openstaande bedrag boekt. Soms wordt een uitgevoerde betaling echter niet weergegeven op een regel op de pagina **Klantbetalingen registreren**. Dit gebeurt meestal omdat het document in kwestie facturen bevat die niet volledig zijn geboekt.

Gebruik de pagina **Documenten zoeken** om te zoeken naar documenten die niet volledig zijn gefactureerd. U kunt zoeken op basis van een of meer van de volgende criteria:  

* Documentnummer  
* Bedrag of bedragreeks  

De volgende procedure laat zien hoe u een specifiek document kunt vinden door beide zoekcriteria te gebruiken.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klantbetalingen registreren** in en kies vervolgens de gerelateerde koppeling.
2. Kies met de aanwijzer op een regel de actie **Documenten zoeken**.
3. Op de pagina **Documenten zoeken** voert u een zoekwaarde in het veld **Documentnr.** in.  

    > [!NOTE]  
    > De waarde die u in dit veld invoert is ingesloten in verborgen jokertekens. Dit betekent dat de actie zoekt voor alle documentnummers die de ingevoerde waarde bevatten.
4. In het veld **Bedrag** voert u het specifieke bedrag in in het document dat u wilt zoeken.  
5. In het veld **Betalingstolerantie %** voert u een percentage in om het bereik van bedragen te definiëren die u wilt doorzoeken om het geopende document te zoeken.  

    Als u 10 invoert, zoekt de actie naar bedragen binnen een bereik van plus of min 10 procent van de waarde in het veld **Bedrag**.
6. Kies de actie **Zoeken**.  

Als een of meer documenten overeenkomen met de criteria, wordt de pagina **Resultaat van documenten zoeken** geopend met daarin regels die deze documenten weergeven. Elke regel bevat een documentnummer, omschrijving en bedrag.

Als een betaling in de bank niet wordt weergegeven door een document, opent u een vooraf ingevuld diversendagboek op de pagina **Klantbetalingen registreren** om de betaling direct bij de tegenrekening te boeken zonder de betaling met een document te vereffenen. U kunt de betaling ook in het dagboek registreren tot de oorsprong van de betaling is opgelost.  

## <a name="to-record-or-post-a-payment-without-a-related-document"></a>Een betaling zonder een gekoppeld document registreren of boeken

Als een betaling bij de bank niet wordt vertegenwoordigd door een document, kunt u de actie **Financieel dagboek** gebruiken om een vooraf ingevulde dagboekregel te openen vanaf de pagina **Klantbetalingen registreren**. Gebruik het dagboek om de betaling rechtstreeks naar de tegenrekening te boeken zonder de betaling met een document te vereffenen. U kunt de betaling ook in het dagboek registreren tot de oorsprong van de betaling is opgelost.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Klantbetalingen registreren** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Diversendagboek**.  

    De pagina **Dagboek** wordt geopend met een enkele regel die de tegenrekening bevat van de dagboekbatch die is ingesteld op de pagina **Instelling van betalingsregistratie**.  
3. Vul de overige velden op de algemene dagboekregel in. Geef bijvoorbeeld het bedrag, het klantnummer of de gegevens van het bankafschrift op. Zie voor meer informatie [Transacties direct naar het grootboek boeken](finance-how-post-transactions-directly.md).  

U kunt de dagboekregel boeken om het totaal op de tegenrekening bij te werken. U kunt ook de dagboekregel ongeboekt laten en deze misschien toevoegen met een notitie dat voor de betaling meer analyse nodig is.  

Als u de dagboekregel niet boekt, wordt de waarde ervan opgeteld bij de waarde in het veld **Restbedrag incl. korting** op de pagina **Betalingsregistratie**.  

## <a name="see-also"></a>Zie ook

[Tegoeden beheren](receivables-manage-receivables.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
