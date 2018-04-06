---
title: Betalingen vereffenen met onbetaalde verkoopdocumenten | Microsoft Docs
description: U vereffent door klanten betaalde bedragen met gerelateerde verkoopdocumenten en boekt de betaling om de klant, het grootboek en bankposten bij te werken.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, cash receipts, customer payment
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: aa2accb5b03fd55c96b046ca6b61582ed5b8a142
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="reconcile-customer-payments-manually-from-a-list-of-unpaid-sales-documents"></a>Klantbetalingen van een lijst met onbetaalde verkoopdocumenten handmatig reconciliëren
Als uw klanten betalingen naar uw elektronische bankrekening hebben gedaan, moet u ieder betaald bedrag vereffenen met het gerelateerde verkoopdocument en vervolgens de betaling boeken om de klant-, dagboek- en bankposten bij te werken.

> [!NOTE]  
>   U kunt dezelfde taken, zoals leveranciersbetalingen, uitvoeren in het venster **Betalingsreconciliatiedagboek** met functies voor import van bankafschriften, automatische vereffening en bankrekeningreconciliatie. Zie voor meer informatie [Betalingen vereffenen met automatische vereffening](receivables-how-reconcile-payments-auto-application.md).

Het venster **Betalingsregistratie** is gemaakt om u te ondersteunen bij taken die deel uitmaken van het controleren van interne rekeningen met actuele geldcijfers om te zorgen voor effectieve inning bij klanten. Met dit hulpmiddel voor betalingsverwerking kunt u snel individuele of lump-sum betalingen boeken, gekorte betalingen verwerken en specifieke onbetaalde documenten vinden waarvoor een betaling is gemaakt.

Betalingen voor verschillende klanten met verschillende betalingsdatums moeten als afzonderlijke betalingen worden geboekt. Betalingen voor dezelfde klant met dezelfde betaaldatum kunnen worden geboekt als lump-sum bedrag. Dit is handig, bijvoorbeeld een klant een enkele betaling heeft gemaakt die over meerdere verkoopfacturen is verspreid.

## <a name="to-set-up-the-payment-registration-journal"></a>Instellen van het betalingregistratiedagboek
Omdat u verschillende betalingssoorten naar verschillende tegenrekeningen kunt boeken, moet u een tegenrekening in het venster **Instelling van betalingsregistratie** selecteren voordat u betalingen begint te verwerken. Als u altijd naar dezelfde tegenrekening boekt, kunt u die rekening instellen als standaard en deze stap elke keer dat u het venster **Betalingsregistratie** opent, vermijden.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Instellingen van betalingsregistratie** in en klik vervolgens op de gerelateerde koppeling.

    U kunt ook in het venster **Betalingsregistratie** de actie **Instellingen** kiezen.    
2. Vul de velden van het venster **Instelling van betalingsregistratie** in. Kies een veld om een korte omschrijving van het veld of een koppeling naar gerelateerde informatie te lezen.  

## <a name="to-reconcile-payments-individually"></a>Betalingen afzonderlijk reconciliëren
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Betalingsregistratie** in en klik vervolgens op de gerelateerde koppeling.  
2. Schakel het selectievakje **Is betaald** in op de regel die het geboekte document vertegenwoordigt waarvoor een betaling is gemaakt.

    Als het selectievakje **Ontvangstdatum automatisch invullen** in het venster **Instelling van betalingsregistratie** is geselecteerd, wordt de werkdatum ingevoerd in het veld **Ontvangen op** .  
3. Voer in het veld **Ontvangen op** de datum in waarop de betaling is gedaan. Deze datum kan van de werkdatum verschillen.  
4. Voer in het veld **Ontvangen bedrag** het bedrag in dat is betaald.

    Voor volledige betalingen is dit gelijk aan het bedrag in het veld **Restbedrag** op de regel. Voor gedeeltelijke betalingen is dit lager dan het bedrag in het veld **Restbedrag** op de regel.    
5. Herhaal stap 2-4 voor andere regels die geboekte documenten vertegenwoordigen waarvoor betalingen zijn verricht.  
6. Kies de actie **Betalingen boeken**.  

De betalingsgegevens worden geboekt voor documenten die worden vertegenwoordigd door regels waarvoor het selectievakje **Is betaald** is geselecteerd.  

Betalingenposten worden geboekt naar grootboek-, bank- en klantrekeningen. Elke betaling wordt toegepast op het bijbehorende geboekte verkoopdocument.  

## <a name="to-reconcile-lump-payments"></a>Lump-sum betalingen reconciliëren
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Betalingsregistratie** in en klik vervolgens op de gerelateerde koppeling.
2. Schakel het selectievakje **Is betaald** in op de regels die geboekte documenten vertegenwoordigen voor dezelfde klant voor wie een lump-sum betaling is verricht.  

    > [!NOTE]  
>   De klant in het veld **Naam** moet hetzelfde zijn op alle regels die als partijbetaling worden geboekt.  

    Als het selectievakje **Ontvangstdatum automatisch invullen** in het venster **Instelling van betalingsregistratie** is geselecteerd, wordt de werkdatum ingevuld in het veld **Ontvangen op** .  
3. Voer in het veld **Ontvangen op** de datum in waarop de betaling is gedaan. Deze datum kan van de werkdatum verschillen.  

    > [!NOTE]  
>   Deze datum moet hetzelfde zijn op alle regels die als stukbetaling worden geboekt.  
4. Voer in het veld **Ontvangen bedrag** bedragen in op meerdere regels die samen het lump-sum bedrag vormen.  

    > [!TIP]  
>   Probeer zoveel mogelijk volledige betalingen te boeken met het partijbedrag. Voer op zoveel mogelijk regels bedragen in die hetzelfde zijn als het bedrag in het veld **Restbedrag**.  
5. Herhaal stap 2-4 voor andere regels die geboekte documenten vertegenwoordigen voor dezelfde klant voor wie een totaalbetaling is verricht.  
6. Kies de actie **Als lump-sum betaling boeken**. De ingevoerde betalingsgegevens worden geboekt voor documenten die worden vertegenwoordigd door regels waarvoor het selectievakje **Is betaald** is geselecteerd.  

Betalingsposten worden geboekt naar grootboek-, bank- en klantrekeningen. Elke betaling wordt toegepast op het bijbehorende geboekte verkoopdocument.  

Als de betaling in de bank niet op een regel in het venster **Betalingsregistratie** wordt weergegeven, komt dat mogelijk doordat het betreffende document nog niet is geboekt. In dat geval kunt u een zoekfunctie gebruiken om het document snel te vinden en te boeken om de betaling te verwerken. Zie voor meer informatie de sectie Een specifiek verkoopdocument zoeken dat niet volledig is gefactureerd.  

Als een betaling in een bank niet wordt weergegeven in een document in [!INCLUDE[d365fin](includes/d365fin_md.md)], dan kunt u een vooraf ingevulde diversendagboekregel in het venster **Betalingsregistratie** openen om de betaling direct bij de tegenrekening te boeken zonder de betaling in een document te verwerken. U kunt de betaling ook in het dagboek registreren tot de oorsprong van de betaling is opgelost. Zie de sectie "Een betaling zonder een gekoppeld document registreren of boeken" voor meer informatie.  

## <a name="to-process-customer-payments-with-discounts-manually"></a>Klantbetalingen met kortingen handmatig verwerken
Als u een contantkorting bent overeengekomen met de klant, dan kunnen de betalingsbedragen lager zijn dan de factuurbedragen als betalingen plaatsvinden voor de afgesproken kortingsdatum.  

In de onderstaande procedure worden vier verschillende procedures uitgelegd voor het boeken van betalingen met korting in het venster **Betalingsregistratie**.  

* Het betalingsbedrag is gelijk aan het overgebleven gekorte bedrag en de betaaldatum is voor de kortingsdatum. U boekt de betaling in de huidige hoedanigheid.  
* Het betalingsbedrag is gelijk aan het overgebleven gekorte bedrag maar de betaaldatum is na de kortingsdatum. U boekt de betaling als gedeeltelijk. Het document blijft openstaan om her restbedrag te innen/betalen. U kunt de kortingsdatum ook later instellen om de volledige betaling toe te staan.  
* Het betalingsbedrag is lager dan het resterende gekorte bedrag. U boekt de betaling als gedeeltelijk. Het document blijft openstaan om her restbedrag te innen/betalen.  
* Het betalingsbedrag is hoger dan het resterende gekorte bedrag. U boekt de betalingen in de huidige hoedanigheid. Alleen het restbedrag wordt geboekt. Het bijkomende bedrag is gecrediteerd aan de klant.  

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-and-where-the-payment-date-is-before-the-discount-date"></a>Een betalingsbedrag verwerken dat gelijk is aan het gekorte bedrag en waar de betaaldatum voor de kortingsdatum is
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Betalingsregistratie** in en klik vervolgens op de gerelateerde koppeling.  
2. Voer het betalingsbedrag in het veld **Ontvangen bedrag** in. Het bedrag is gelijk aan het bedrag in het veld **Rest. bedrag na korting**.

    Het selectievakje **Is betaald** wordt automatisch ingeschakeld en het veld **Ontvangen op** wordt ingevuld met de werkdatum.    
3. Voer de betalingsdatum in het veld **Ontvangen op** in. De datum is eerder dan de datum in het veld **Vervaldatum contantkort.**
4. Controleer of het veld **Restbedrag** nul (0) bevat.  
5. Kies de actie **Betalingen boeken** om de volledige gehele betaling te boeken naar de grootboek-, bank-, en klantrekeningen.

### <a name="to-process-a-payment-amount-that-is-equal-to-the-discounted-amount-but-where-the-payment-date-is-after-the-discount-date"></a>Een betalingsbedrag verwerken dat gelijk is aan het gekorte bedrag, maar waar de betaaldatum na de kortingsdatum is
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Betalingsregistratie** in en klik vervolgens op de gerelateerde koppeling.  
2. Voer het betalingsbedrag in het veld **Ontvangen bedrag** in. Het bedrag is gelijk aan het bedrag in het veld **Rest. bedrag na korting**.

    Het selectievakje **Is betaald** wordt automatisch ingeschakeld en het veld **Ontvangen op** wordt ingevuld met de werkdatum.
3. In het veld **Ontvangen op** voert u een betaaldatum in die na de datum in het veld **Vervaldatum contantkort.** ligt. De datumvelden worden rood weergegeven en een foutbericht wordt weergegeven onder in het venster.

    > [!TIP]  
>   Als u een uitzondering wilt maken en de korting wilt verlenen hoewel de betaling te laat is, dan voert u de volgende stappen uit:
4. Kies de actie **Details**.  
5. Voer in het venster **Betalingsregistratiegegevens** in het veld **Vervaldatum contantkort.** op het sneltabblad **Contantkorting** een datum in die later is dan de datum in het veld **Ontvangen op** in het venster **Betalingsregistratie**.  

    De foutmelding en het rode lettertype verdwijnen en u kunt doorgaan met de verminderde betaling te verwerken.    
6. Controleer of het veld **Restbedrag** het bedrag bevat dat resteert om het volledige factuurbedrag te betalen.  
7. Kies de actie **Betalingen boeken** om de gedeeltelijke betaling te boeken naar de grootboek-, bank-, en klantrekeningen.  

Het bijbehorende document blijft open.

### <a name="to-process-a-payment-that-is-lower-than-the-remaining-discounted-amount"></a>Een betaling verwerken die lager is dan het resterende gekorte bedrag
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Betalingsregistratie** in en klik vervolgens op de gerelateerde koppeling.  
2. Voer het betalingsbedrag in het veld **Ontvangen bedrag** in. Het bedrag is lager dan het bedrag in het veld **Rest. bedrag na korting**.

    Het selectievakje **Is betaald** wordt automatisch ingeschakeld en het veld **Ontvangen op** wordt ingevuld met de werkdatum.  
3. Voer de betalingsdatum in het veld **Ontvangen op** in. De datum is eerder dan de datum in het veld **Vervaldatum contantkort.**
4. Controleer of het veld **Restbedrag** het bedrag bevat dat resteert om het gekorte bedrag te betalen.  
5. Kies de actie **Betalingen boeken** om de gedeeltelijke betaling te boeken naar de grootboek-, bank-, en klantrekeningen.  

Het bijbehorende document blijft open.

### <a name="to-process-a-payment-that-is-more-than-the-remaining-discounted-amount"></a>Een betaling verwerken die groter is dan het resterende gekorte bedrag
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Betalingsregistratie** in en klik vervolgens op de gerelateerde koppeling.  
2. Voer het betalingsbedrag in het veld **Ontvangen bedrag** in. Het bedrag is hoger dan het bedrag in het veld **Rest. bedrag na korting**.  

    Het selectievakje **Is betaald** wordt automatisch ingeschakeld en het veld **Ontvangen op** wordt ingevuld met de werkdatum.    
3. Voer de betalingsdatum in het veld **Ontvangen op** in. De datum is eerder dan de datum in het veld **Vervaldatum contantkort.**
4. Controleer of het veld **Restbedrag** nul (0) bevat.  
5. Kies de actie **Betalingen boeken** om de volledige gehele betaling te boeken naar de grootboek-, bank-, en klantrekeningen.  

Het bijbehorende document is gesloten, en het overtollige betalingsbedrag is gecrediteerd aan de klant.  

## <a name="to-find-a-specific-sales-document-that-is-not-fully-invoiced"></a>Een specifiek verkoopdocument zoeken dat niet volledig is gefactureerd
Het venster **Betalingsregistratie** ondersteunt u bij taken die nodig zijn om interne rekeningen in overeenstemming te brengen met werkelijke geldcijfers om effectieve inning van klanten te garanderen. Het bevat openstaande inkomende betalingen als regels die verkoopdocumenten vertegenwoordigen waar een betalingstermijn voor een bedrag is verstreken.  

Wanneer een betaling is gemaakt, geregistreerd in de bank of anderszins, wordt meestal het gerelateerde verkoop- of inkoopdocument als een regel weergegeven in het venster **Betalingsregistratie**, omdat het document in kwestie in afwachting is van de boeking van de betaling tegen het openstaande bedrag. Soms wordt een uitgevoerde betaling echter niet weergegeven op een regel in het venster **Betalingsregistratie**. Dit gebeurt meestal omdat het document in kwestie facturen bevat die niet volledig zijn geboekt.

In het venster **Documenten zoeken** kunt u zoeken in documenten die nog niet volledig zijn gefactureerd. U kunt zoeken op basis van een of meer van de volgende criteria:  

* Documentnummer  
* Bedrag of bedragreeks  

De volgende procedure laat zien hoe u een specifiek document kunt vinden door beide zoekcriteria te gebruiken.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Betalingsregistratie** in en klik vervolgens op de gerelateerde koppeling.
2. Kies met de aanwijzer op een regel de actie **Documenten zoeken**.
3. In het venster **Documenten zoeken** voert u een zoekwaarde in het veld **Documentnr.** in.  

    > [!NOTE]  
>   De waarde die u in dit veld invoert is ingesloten in verborgen jokertekens. Dit betekent dat de functie zoekt voor alle documentnummers die de ingevoerde waarde bevatten.    
4. In het veld **Bedrag** voert u het specifieke bedrag in dat voorkomt in het document dat u wilt zoeken.  
5. In het veld **Betalingstolerantie %** voert u een percentage in om het bereik van bedragen te definiëren die u wilt doorzoeken om het geopende document te zoeken.  

    Als u 10 invoert, zoekt de functie in een bereik van tien procent hoger tot tien procent lager dan de waarde in het veld **Bedrag**.    
6. Kies de actie **Zoeken**.  

Met de zoekfunctie wordt gezocht in documenten die niet volledig zijn gefactureerd op basis van de opgegeven criteria.  

Als een of meer documenten overeenkomen met de criteria, wordt het venster **Resultaat van documenten zoeken** geopend met daarin regels die deze documenten weergeven. Elke regel bevat een documentnummer, omschrijving en bedrag, zodat u gemakkelijk een specifiek document kunt vinden, bijvoorbeeld op basis van de gegevens op uw bankafschrift.  

Als een betaling in een bank niet wordt weergegeven in een document in [!INCLUDE[d365fin](includes/d365fin_md.md)], dan kunt u een vooraf ingevulde diversendagboekregel in het venster **Betalingsregistratie** openen om de betaling direct bij de tegenrekening te boeken zonder de betaling in een document te verwerken. U kunt de betaling ook in het dagboek registreren tot de oorsprong van de betaling is opgelost.  

## <a name="to-record-or-post-a-payment-without-a-related-document"></a>Een betaling zonder een gekoppeld document registreren of boeken
Als een betaling in een bank niet wordt weergegeven in een document in [!INCLUDE[d365fin](includes/d365fin_md.md)], dan kunt u een vooraf ingevulde diversendagboekregel in het venster **Betalingsregistratie** openen om de betaling direct bij de tegenrekening te boeken zonder de betaling in een document te verwerken. U kunt de betaling ook in het dagboek registreren tot de oorsprong van de betaling duidelijk is.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Betalingsregistratie** in en klik vervolgens op de gerelateerde koppeling.  

Ga door om een niet gedocumenteerde betaling te registreren.  

1. Kies de actie **Diversendagboek**.  

    Het venster **Dagboek** wordt geopend met een vooraf ingevulde regel met de tegenrekening van de dagboekbatch die is ingesteld in het venster **Instelling van betalingsregistratie**.  
2. Vul de overige velden op de dagboekregel in, zoals het bedrag en het klantnummer of andere informatie van het bankafschrift. Zie voor meer informatie [Transacties direct naar het grootboek boeken](finance-how-post-transactions-directly.md).  

U kunt evenwel de dagboekregel boeken om het totaal op de tegenrekening bij te werken. U kunt de journaalregel ook ongeboekt laten en deze misschien toevoegen met een notitie dat voor de betaling meer analyse nodig is.  

Als u de dagboekregel ongeboekt laat, wordt deze toegevoegd aan de waarde in het veld **Niet-geboekt saldo** onder in het venster **Betalingsregistratie**.  

## <a name="see-also"></a>Zie ook
[Tegoeden beheren](receivables-manage-receivables.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

