---
title: Bankrekeningen afstemmen
description: Meer informatie over hoe transacties in Business Central afstemt met transacties in afschriften van uw bank.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/13/2022
ms.custom: bap-template
---
# <a name="reconcile-bank-accounts"></a>Bankrekeningen afstemmen

Bankreconciliatie helpt ervoor te zorgen dat wat er in uw boeken staat, overeenkomt met de afschriften die u van uw bank ontvangt. Met bankrekeningreconciliatie worden boekingen in de bankrekeningen die u hebt ingesteld in [!INCLUDE[prod_short](includes/prod_short.md)] vergeleken en afgestemd met banktransacties bij uw bank. Met reconciliatie kunnen de saldi vervolgens naar uw bankrekeningen worden geboekt in[!INCLUDE[prod_short](includes/prod_short.md)] om ze beschikbaar te stellen aan financiële managers. Bankafstemming is ook een praktische manier om ontbrekende betalingen en boekhoudfouten te ontdekken en op te lossen.

In dit artikel wordt beschreven hoe u bankrekeningen afstemt op de pagina **Bankreconciliatie**.

U kunt bankrekeningen echter ook afstemmen op de pagina **Betalingsreconciliatiedagboek** wanneer u betalingen verwerkt. Als u de actie **Betalingen boeken en bankrekening reconciliëren** kiest, worden open bankrekeningposten gesloten die zijn gerelateerd aan de vereffende klant- of leveranciersposten. Dit betekent dat de bankrekening automatisch wordt gereconcilieerd voor de betalingen die u met het dagboek boekt. Zie voor meer informatie [Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> In de Noord-Amerikaanse versies vindt u ook de pagina **Werkblad bankreconciliatie**. Dit is geschikter voor cheques en borgsommen, maar u kunt er geen bankafschriftbestanden mee importeren. Als u deze pagina wilt gebruiken in plaats van de pagina **Bankreconciliatie**, schakelt u het veld **Bankreconciliatie met automatische afstemming** uit op de pagina **Boekhoudinstellingen**. Zie voor meer informatie [Bankrekeningen reconciliëren](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) onder Lokale functionaliteit voor de Verenigde Staten.

De regels op de pagina **Bankreconciliatie** zijn verdeeld in twee deelvensters. Het deelvenster **Bankafschriftregels** bevat geïmporteerde bankafschriften of posten met openstaande betalingen. Het deelvenster **Bankposten** bevat de posten op de interne bankrekening.

Reconciliatie van transacties in afschriften van uw bank met bankposten in [!INCLUDE[prod_short](includes/prod_short.md)] wordt *afstemmen* genoemd. Er zijn twee manieren om transacties af te stemmen met bankposten:

* Automatisch, via de actie **Automatisch afstemmen**.
* Handmatig, door regels te selecteren in beide deelvensters om elke bankafschriftregel te koppelen aan een of meer gerelateerde bankposten, en vervolgens de functie **Handmatig afstemmen** te gebruiken.

Het selectievakje **Vereffend** is ingeschakeld op regels waar posten overeenkomen. Zie [Regels instellen voor automatische vereffening van betalingen](receivables-how-set-up-payment-application-rules.md) voor meer informatie. Als u een einddatum voor het afschrift invoert op de bankreconciliatie, nadat u de regels ervan hebt afgestemd met posten, maakt [!INCLUDE [prod_short](includes/prod_short.md)] de afstemmingen ongedaan voor regels en posten die na die datum zijn.

> [!NOTE]
> Nadat u een datum hebt ingevoerd in het veld Einddatum afschrift, filtert de pagina Bankreconciliatie de bankposten om alleen posten tot die datum weer te geven. U kunt alleen bankreconciliaties boeken met bankposten op of vóór de einddatum van het afschrift. Het filter zorgt ervoor dat uw grootboek op de einddatum van het afschrift in evenwicht is met uw bankafschrift, met als verschil de openstaande betalingen en cheques.

Wanneer de waarde in het veld **Totaalsaldo** in het deelvenster **Bankafschriftregels** gelijk is aan de totale waarde in het veld **Af te stemmen saldo** plus het veld **Saldo laatste afschrift** in het deelvenster **Bankposten**, kunt u de actie **Boeken** kiezen. Niet-afgestemde bankposten blijven op de pagina staan, wat aangeeft dat er een verschil is dat u moet oplossen om de bankrekening af te stemmen.

Regels die niet kunnen worden afgestemd, aangeduid met een waarde in het veld **Verschil**, blijven na boeking op de pagina **Bankreconciliatie** staan. Er is daarmee een verschil geconstateerd dat u moet oplossen voordat u de afstemming van de bankrekening kunt afronden. In de onderstaande tabel worden enkele typische bedrijfssituaties beschreven die tot verschillen kunnen leiden.

| Verschil | Reden | Oplossing |
|------------|--------|------------|
| Een transactie op uw bankrekening in [!INCLUDE[prod_short](includes/prod_short.md)] staat niet op het bankafschrift. | De banktransactie is niet gemaakt, hoewel er wel een boeking is gedaan in [!INCLUDE[prod_short](includes/prod_short.md)]. | Maak de ontbrekende transactie (of vraag een debiteur om deze te maken). Importeer vervolgens het bankafschriftbestand opnieuw of voer de transactie handmatig in. |
| Een transactie op het bankafschrift is niet aanwezig als een document of journaalregel in [!INCLUDE[prod_short](includes/prod_short.md)]. | Er is een banktransactie uitgevoerd zonder een overeenkomstige boeking in [!INCLUDE[prod_short](includes/prod_short.md)], bijvoorbeeld een boeking in een dagboekregel voor een uitgave. | Maak en plaats de ontbrekende post. Zie [Ontbrekende posten maken om banktransacties mee af te stemmen](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines) voor informatie over een snelle manier om dit te doen. |
| Een transactie op de interne bankrekening komt overeen met een banktransactie, maar bepaalde informatie is te verschillend om een match te geven. | Informatie, zoals het bedrag of de naam van de klant, is anders ingevoerd in de banktransactie of de interne boeking. | Controleer de informatie en stem deze vervolgens handmatig af. Corrigeer desgewenst de onjuiste informatie. |

U moet de verschillen oplossen, bijvoorbeeld door de ontbrekende posten te maken en niet-overeenkomende informatie te corrigeren, of door ontbrekende geldtransacties in te voeren, totdat de reconciliatie van de bankrekening is voltooid en geboekt.

U kunt het deelvenster **Bankafschriftregels** op de pagina **Bankreconciliatie** als volgt vullen:

* Automatisch, door de functie **Bankafschrift importeren** te gebruiken om het deelvenster **Bankafschriftregels** in te vullen met banktransacties volgens een geïmporteerd bestand of een stream die door de bank is aangeleverd.
* Handmatig, door de functie **Regels voorstellen** te gebruiken om het deelvenster **Bankafschriftregels** in te vullen volgens facturen in [!INCLUDE[prod_short](includes/prod_short.md)] met openstaande betalingen.

## <a name="to-add-bank-statement-lines-by-importing-a-bank-statement"></a>Bankafschriftregels toevoegen door een bankafschrift te importeren

Het deelvenster **Bankafschriftregels** wordt gevuld met banktransacties volgens een geïmporteerd bestand of een stream die door de bank is aangeleverd.

Om bankafschriften als bankfeeds te importeren, moet u de service Envestnet Yodlee Bank Feeds instellen. Hiermee worden uw bankrekeningen in [!INCLUDE[prod_short](includes/prod_short.md)] gekoppeld aan de gerelateerde online bankrekeningen. Zie voor meer informatie [De Envestnet Yodlee Bank Feeds-service instellen](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> U kunt ook bankafschriftbestanden importeren in een door komma's of puntkomma's gescheiden indeling (.CSV). Gebruik de begeleide instelling **Een importindeling voor het bankafschriftbestand instellen** om de importindelingen voor bankafschriften te definiëren en de indeling aan een bankrekening te koppelen. U kunt deze indelingen vervolgens gebruiken wanneer u bankafschriften importeert op de pagina **Bankreconciliatie**.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Bankreconciliatie** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Selecteer in het veld **Bankrekeningnr.** de relevante bankrekening. De bankposten die bestaan voor de bankrekening, worden weergegeven in het deelvenster **Bankposten**.
4. Voer de datum van het rekeningoverzicht van de bank in het veld **Afschriftdatum** in.
5. Voer het saldo van het bankafschrift in het veld **Eindsaldo afschrift** in.
6. Als u een bankafschriftbestand hebt ingesteld, kiest u de actie **Bankafschrift importeren**.
7. Zoek het bestand en kies **Openen** om de banktransacties te importeren in het deelvenster **Bankafschriftregels** op de pagina **Bankreconciliatie**.

## <a name="to-fill-in-bank-reconciliation-lines-with-the-suggest-lines-action"></a>Bankreconciliatieregels invullen met de actie Regels voorstellen

Het deelvenster **Bankafschriftregels** wordt ingevuld volgens facturen in [!INCLUDE[prod_short](includes/prod_short.md)] met openstaande betalingen.  

1. Kies op de pagina **Bankreconciliatie** de actie **Regels voorstellen**.
2. Voer in het veld **Begindatum** de vroegste boekingsdatum in voor de posten waarop u de reconciliatie wilt uitvoeren.
3. Voer in het veld **Einddatum** de laatste boekingsdatum in voor de posten waarop u de reconciliatie wilt uitvoeren.

    > [!NOTE]
    > Doorgaans komt de einddatum overeen met de datum die is opgegeven in het veld **Afschriftdatum**. Als u echter transacties voor slechts een deel van een periode wilt afstemmen, kunt u een andere einddatum invoeren.

4. Als u niet wilt dat de bankrekeningposten niet-afgestemde open tegengeboekte posten bevatten, kiest u de schakelaar **Tegengeboekte posten uitsluiten**. De lijst met bankrekeningposten bevat standaard tegengeboekte posten tot de afschriftdatum.
5. Kies de knop **Ok**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Bankafschriftregels automatisch afstemmen met bankrekeningposten

De pagina **Bankreconciliatie** biedt automatische afstemmingsfunctionaliteit op basis van een afstemming van tekst op een bankafschriftregel (linkerdeelvenster) met tekst in een of meer bankposten (rechterdeelvenster). U kunt de voorgestelde automatische afstemming overschrijven en u kunt ervoor kiezen helemaal geen automatische afstemming te gebruiken. Zie [Bankafschriftregels handmatig afstemmen met bankrekeningposten](bank-how-reconcile-bank-accounts-separately.md#to-match-bank-statement-lines-with-bank-account-ledger-entries-manually) voor meer informatie.

U kunt de basis voor overeenkomsten onderzoeken met behulp van de actie **Afstemmingsdetails**. De details bevatten bijvoorbeeld de namen van de velden die overeenkomende waarden bevatten.  

1. Kies op de pagina **Bankreconciliatie** de actie **Automatisch afstemmen**. De pagina **Bankposten afstemmen** wordt geopend.
2. Geef in het veld **Datumtolerantie van transactie (dagen)** het aantal dagen op vóór en na de boekingsdatum van de bankpost waarbinnen de actie naar overeenkomstige transactiedatums in het bankafschrift zoekt.

    Als u 0 typt of het veld leeg laat, zoekt de actie **Automatisch afstemmen** alleen naar overeenkomende transactiedatums op de bankpostboekingsdatum.
3. Kies de knop **Ok**.

    De lijnen zijn kleurgecodeerd om het gemakkelijker te maken te begrijpen wat u ermee moet doen. Bankafschriftregels en bankrekeningposten die overeenkomen met de huidige bankreconciliatie, worden gewijzigd in vetgedrukt groen lettertype. Bankrekeningposten die al zijn afgestemd in andere bankreconciliaties, worden weergegeven in cursief blauw lettertype.
4. Als u een afstemming wilt verplaatsen, selecteert u de bankafschriftregel en kiest u vervolgens **Afstemming verwijderen**.

> [!TIP]
> U kunt een mix van handmatige en automatische afstemming gebruiken. Als u handmatig afgestemde posten hebt, zal automatische afstemming uw selecties niet overschrijven.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Bankafschriftregels handmatig afstemmen met bankrekeningposten

> [!TIP]
> Bij het handmatig afstemmen van regels en posten kunt u met de acties **Alles weergeven**, **Tegengeboekte posten weergeven**, **Tegengeboekte posten verbergen** en **Niet-afgestemd weergeven** gemakkelijker een overzicht krijgen. Standaard bevatten de bankrekeningposten geen niet-afgestemde tegengeboekte posten. Als u deze posten in de lijst wilt opnemen en ze handmatig wilt afstemmen, kiest u de actie **Tegengeboekte posten weergeven**. Als u ervoor kiest om tegengeboekte posten te verbergen nadat u een of meer afstemmingen hebt gedaan, worden de afgestemde posten nog steeds weergegeven.

> [!NOTE]
> U kunt geen bankreconciliatie boeken als u veel-op-een-afstemming uitvoert en de gecombineerde bedragen verschillen bevatten. Dit geldt zelfs als de gecombineerde verschillen nul zijn.
>
> Hier is een voorbeeld van een veel-op-een-overeenkomst met verschillen. De waarde van 200 voor bankafschriftpost 1 wordt gekoppeld aan twee bankposten met een totale waarde van 180. Het verschil is 20. De waarde van 350 voor bankafschriftpost 2 wordt gekoppeld aan twee andere bankposten met een totale waarde van 370. Het verschil is -20, wat de waarde van 20 voor bankafschrift 1 in evenwicht brengt.  
>
> Om een bankreconciliatie met verschillen op de regels te boeken, boekt u de verschillen en vergelijkt u ze met de geboekte posten.

1. Selecteer op de pagina **Bankreconciliatie** een niet-vereffende regel in het deelvenster **Bankafschriftregels**.
2. Selecteer in het deelvenster **Bankposten** een of meer bankrekeningposten die met de geselecteerde bankafschriftregel kunnen worden afgestemd. Om meerdere regels te kiezen drukt u op de <kbd>CTRL</kbd>-toets en kiest u vervolgens de regels.

   > [!TIP]
   > U kunt ook handmatig meerdere bankafschriftregels afstemmen met één bankrekeningpost. Dit kan bijvoorbeeld handig zijn als uw bankdeposito verschillende betaalmethoden bevat, zoals creditcards van verschillende uitgevers, en uw bank deze als afzonderlijke regels vermeldt.
3. Kies de actie **Handmatig afstemmen**.

    De geselecteerde bankafschriftregel en de geselecteerde bankrekeningposten worden in groene letters weergegeven en het selectievakje **Vereffend** in het rechter venster wordt geselecteerd.
4. Herhaal stap 1 t/m 3 voor alle bankafschriftregels die niet zijn afgestemd.

> [!TIP]
> Als u een afstemming wilt verplaatsen, selecteert u de bankafschriftregel en kiest u vervolgens **Afstemming verwijderen**. Als u meerdere bankafschriftregels op een grootboekpost hebt afgestemd en een of meer van de afgestemde regels moet verwijderen, worden alle handmatige afstemmingen voor de grootboekboeking verwijderd wanneer u **Afstemming verwijderen** kiest.

## <a name="to-validate-your-bank-reconciliation"></a>Uw bankreconciliatie valideren

Om de reconciliatie van uw bankrekening nogmaals te controleren voordat u deze boekt, gebruikt u de actie **Testrapport** om een voorbeeld van de reconciliatie te bekijken. Het rapport is beschikbaar in de volgende contexten:

* Wanneer u een bankreconciliatie voorbereidt op de pagina **Bankreconciliatie**.
* Wanneer u betalingen afstemt op de pagina **Betalingsreconciliatiedagboeken**.

Regels die niet kunnen worden afgestemd, blijven na boeking op de pagina **Bankreconciliatie** staan. Deze regels bevatten een waarde in het veld **Verschil**. Het verschil vertegenwoordigt een discrepantie die u moet oplossen voordat u de reconciliatie van de bankrekening kunt voltooien. In de onderstaande tabel worden enkele typische bedrijfssituaties beschreven die tot verschillen kunnen leiden.

| Verschil | Reden | Oplossing |
|------------|--------|------------|
| Een transactie op uw bankrekening in [!INCLUDE[prod_short](includes/prod_short.md)] staat niet op het bankafschrift. | De banktransactie is niet gemaakt, hoewel er wel een boeking is gedaan in [!INCLUDE[prod_short](includes/prod_short.md)]. | Maak de ontbrekende transactie (of vraag een debiteur om deze te maken). Importeer vervolgens het bankafschriftbestand opnieuw of voer de transactie handmatig in. |
| Een transactie op het bankafschrift is niet aanwezig als een document of journaalregel in [!INCLUDE[prod_short](includes/prod_short.md)]. | Er is een banktransactie uitgevoerd zonder een overeenkomstige boeking in [!INCLUDE[prod_short](includes/prod_short.md)], bijvoorbeeld een boeking in een dagboekregel voor een uitgave. | Maak en plaats de ontbrekende post. Zie [Ontbrekende posten maken om banktransacties mee af te stemmen](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines) voor informatie over een snelle manier om dit te doen. |
| Een transactie op de interne bankrekening komt overeen met een banktransactie, maar bepaalde informatie is te verschillend om een match te geven. | Informatie, zoals het bedrag of de naam van de klant, is anders ingevoerd in de banktransactie of de interne boeking. | Controleer de informatie en stem deze vervolgens handmatig af. Corrigeer desgewenst de onjuiste informatie. |

U moet de verschillen oplossen, bijvoorbeeld door de ontbrekende posten te maken en niet-overeenkomende informatie te corrigeren, of door ontbrekende geldtransacties in te voeren, totdat de reconciliatie van de bankrekening is voltooid en geboekt.

> [!NOTE]
> De pagina Bankreconciliatie en het testrapport gaan ervan uit dat u alleen aan het reconciliëren bent binnen de periode tot de einddatum van het afschrift. Als u een bankafschriftregel koppelt aan een bankpost voordat u een einddatum voor een afschrift invoert, en vervolgens een einddatum voor een afschrift invoert die na de einddatum van de bankpost valt, zijn de gegevens in het testrapport onjuist.

In de volgende tabel worden de velden in het testrapport beschreven die u kunnen helpen bij het voltooien van de bankreconciliatie.

|Veld  |Omschrijving  |
|---------|---------|
|Afschriftdatum| De datum die is opgegeven in het veld **Afschriftdatum** op de pagina **Bankreconciliatie**.|
|Saldo van laatste afschrift|Het saldo dat is opgegeven in het veld **Saldo laatste afschrift** op de pagina **Bankreconciliatie**. Deze wordt automatisch ingevuld vanaf de meest recente reconciliatie voor dezelfde bankrekening. De waarde is nul als dit uw eerste reconciliatie van uw bankrekening is.|
|Eindsaldo van afschrift|Het saldo dat is opgegeven in het veld **Eindsaldo afschrift** op de pagina **Bankreconciliatie**. |
|Grootboekrekeningnr. <*nummer*> Saldo op <*datum*> | Het saldo op de grootboekrekening op de einddatum van het afschrift. Dit is het ongefilterde saldo per die datum. Als uw bank uw lokale valuta gebruikt, moet dit saldo gelijk zijn aan het saldo van uw bankrekening (weergegeven aan de rechterkant van de rapportkop) wanneer u alle afschriftregels hebt afgestemd. Een lege **()** in de naam van dit veld betekent dat uw bank de lokale valuta gebruikt.<br><br>Een verschil in dit en de voorgaande velden kan erop duiden dat u rechtstreeks op de grootboekrekening hebt geboekt of dat u dezelfde grootboekrekening voor meerdere banken gebruikt, wat niet wordt aanbevolen. Banken zijn aan het grootboek gekoppeld via de bankrekeningboekingsgroep die voor de rekening is opgegeven.<br><br>Het testrapport toont een waarschuwing als u directe boekingen hebt, zelfs als het saldo voor de boeking nul is. Directe boekingen die niet in evenwicht zijn, leiden vaak tot geaccumuleerde verschillen voor toekomstige bankreconciliaties. U moet het grootboeksaldo en de grootboekposten controleren voordat u de bankreconciliatie boekt. Ga voor meer informatie over direct boeken naar [Direct boeken voorkomen](#avoid-direct-posting).|
|Grootboekrekeningnr. <*nummer*> Saldo (<*LV*>) op <*datum*>| Het saldo op de grootboekrekening op de einddatum van het afschrift in lokale valuta. Het saldo wordt omgerekend naar de valuta van de bankrekening met behulp van de wisselkoers die gold op de einddatum van het afschrift. Dit is het ongefilterde saldo per die datum. U vergelijkt dit met het veld **Grootboekrekeningnr. <* nummer *> Saldo op <* datum*>* als uw bank een vreemde valuta gebruikt. De waarde in het veld Grootboekrekeningnr. <* nummer *> Saldo op <* datum*> voor lokale valuta kan iets afwijken omdat valutaconversie tot kleine verschillen kan leiden. Het saldo van uw bank moet dit saldo zeer dicht benaderen.  |
|Bankrekeningsaldo op <*datum*>| Het saldo op de bankrekening op de einddatum van het afschrift.|
|Som van verschillen    | De som van de verschillen voor de afschriftregels. Om toegang te krijgen tot de details zet u de schakelaar **Openstaande transacties afdrukken** aan wanneer u criteria voor het rapport invoert. Een verschil is een bankafschriftregel die niet volledig is afgestemd met een of meer bankposten. U kunt geen reconciliatie boeken van een bankrekening die verschillen bevat. U kunt een bankreconciliatie boeken die bankposten bevat die niet zijn afgestemd met afschriftregels. Deze waarde wordt weergegeven in het veld **Openstaande banktransacties** en in een apart gedeelte als u de schakelaar Openstaande transacties afdrukken inschakelt.      |
|Saldo afschrift     | De waarde die is opgegeven in het veld **Eindsaldo afschrift** op de pagina **Bankreconciliatie**.  |
|Openstaande banktransacties     | De som van niet-afgestemde, niet-cheque bankposten met een boekingsdatum op of voor de einddatum van het afschrift. Dit gebeurt wanneer u transacties registreert voordat ze bij uw bank worden geregistreerd. Bijvoorbeeld aan het einde van een periode. Wanneer u de volgende bankreconciliatie maakt, kunt u deze posten reconciliëren.        |
|Openstaande cheques     | De som van niet-afgestemde, bankposten voor cheques met een boekingsdatum op of voor de einddatum van het afschrift. Dit gebeurt wanneer u transacties registreert voordat ze bij uw bank worden geregistreerd. Dit kan bijvoorbeeld gebeuren voor cheques als een verkoper een cheque niet incasseert in dezelfde periode waarin u deze hebt geregistreerd. Wanneer u de volgende bankreconciliatie maakt, kunt u deze posten reconciliëren.        |
|Bankrekeningsaldo     | De som van de waarden voor het eindsaldo van het bankafschrift, uitstaande banktransacties en uitstaande cheques. Nadat u alle verschillen in afgestemde posten hebt afgehandeld, komt dit saldo overeen met uw banksaldo. U hebt bijvoorbeeld alle afgestemde posten verantwoord, evenals de posten die u niet kon afstemmen voor dit bankafschrift. U kunt nu de reconciliatie boeken.        |

> [!TIP]
> Als u het **Testrapport** van de pagina **Betalingsreconciliatiedagboek** uitvoert, berekent [!INCLUDE [prod_short](includes/prod_short.md)] de waarde in het **Eindsaldo afschrift** als volgt:
>
> * saldo laatste afschrift + som van alle regels in het betalingsreconciliatiedagboek
>
> U kunt de waarde gebruiken om te vergelijken met uw bankafschrift.

## <a name="to-create-missing-ledger-entries-to-match-bank-statement-lines"></a>Ontbrekende posten maken om bankafschriftregels af te stemmen

Soms bevat een bankafschrift bedragen voor in rekening gebrachte rente of toeslagen. Dergelijke bankafschriftregels kunnen niet worden afgestemd omdat er geen gerelateerde posten bestaan in [!INCLUDE[prod_short](includes/prod_short.md)]. U moet vervolgens voor elke transactie een dagboekregel boeken om een gerelateerde post te maken waarmee deze kan worden afgestemd.

1. Kies op de pagina **Bankreconciliatie** de actie **Naar dagboek overbrengen**.  
2. Geef op de pagina **Bankreconciliatie naar dagboek** op welk dagboek moet worden gebruikt en kies vervolgens de knop **OK**.

    De pagina **Diversendagboek** wordt geopend met nieuwe dagboekregels voor bankafschriftregels met ontbrekende posten.
3. Vul de dagboekregel met de informatie, zoals de tegenrekening. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.  
4. Om het resultaat van boeking te bekijken voordat u boekt, kiest u de actie **Testrapport** en kiest u vervolgens een optie voor toegang tot het rapport. Het rapport **Bankrekeningafschrift** wordt geopend en bevat dezelfde velden als de koptekst van de pagina **Bankreconciliatie**.
5. Kies de actie **Boeken**.

    Nadat de post is geboekt, stemt u deze af met de bankafschriftregel.
6. Vernieuw de pagina **Bankreconciliatie** of open deze opnieuw. De nieuwe post wordt in het deelvenster **Bankposten** weergegeven.
7. Stem de bankafschriftregel handmatig of automatisch af met de bankpost.

## <a name="find-outstanding-transactions-in-previous-periods"></a>Openstaande transacties in vorige perioden zoeken

U kunt het bankafschriftrapport gebruiken om openstaande transacties in vorige perioden te zoeken. Openstaande transacties zijn geopend vóór de afschriftdatum en zijn niet afgesloten, of ze zijn gesloten nadat de bankreconciliatie is geboekt.

Wanneer u het bankafschiftrapport via de pagina Bankafschriftlijst uitvoert, kunt u de schakelaar **Openstaande posten** inschakelen, het rapport bevat dan een sectie met een lijst van openstaande posten.

**Voorbeeld**: we hebben bankrekeningposten A, B en C op onze bankrekening voor de maand augustus. Wanneer we onze bankrekening voor augustus reconciliëren, vinden we een bankafschriftregel die overeenkomt met post A, maar geen voor B en C. Dus boeken we de reconciliatie met post A afgestemd en B en C als openstaande posten.

In september ontvangen we een betaling voor post B en besluiten onze bankrekening te reconciliëren. Als we het bankafschriftrapport uitvoeren voordat we de reconciliatie boeken, hebben we één afgestemde transactie en één openstaande transactie.

Als we het rapport voor augustus afdrukken, hebben we openstaande transacties voor onze B- en C-posten, ook al hebben we post B in september gesloten.

## <a name="undo-a-bank-account-reconciliation"></a>Een bankrekeningreconciliatie ongedaan maken

Als u een fout vindt in een geboekte bankreconciliatie, kunt u de actie **Ongedaan maken** op de pagina **Dagschriftenoverzicht** gebruiken om de fout te corrigeren. Wanneer u een geboekte bankreconciliatie ongedaan maakt, worden de posten verplaatst naar de pagina **Bankreconciliatie** en gemarkeerd als **Open**, wat betekent dat ze niet gereconcilieerd zijn. U kunt vervolgens de bankreconciliatie corrigeren en opnieuw boeken.

> [!NOTE]
> Als u in de Noord-Amerikaanse versie de functie Ongedaan maken wilt gebruiken voor geboekte bankreconciliaties en bankafschriften, moet u de schakelaar **Bankreconciliatie met automatische afstemming** inschakelen op de pagina **Grootboekinstellingen**. De functie Ongedaan maken is niet beschikbaar voor bankafschriften die zijn geboekt vanuit werkbladen voor bankreconciliatie.

### <a name="reusing-the-bank-statement-number"></a>Het bankafschriftnummer opnieuw gebruiken

Het nummer van het bankafschrift dat wordt gebruikt voor de nieuwe bankreconciliatie, wordt van de bankrekening overgenomen, evenals het laatste overzicht van het saldo. U kunt deze waarden wijzigen voordat u een nieuwe bankreconciliatie start. Wanneer u echter een nieuwe bankreconciliatie maakt, controleert [!INCLUDE[d365fin](includes/d365fin_md.md)] of het afschriftnummer al is toegewezen aan een geboekt bankafschrift. Als het nummer in gebruik is, maar u wilt dat het nieuwe bankafschrift het gebruikt, kunt u de actie **Afschriftnr. wijzigen** gebruiken op de pagina **Bankreconciliatie**.

### <a name="examples"></a>Voorbeelden

De volgende voorbeelden laten zien hoe u een fout kunt herstellen in een geboekte bankreconciliatie met of zonder gebruik van hetzelfde afschriftnummer.

#### <a name="example-1"></a>Voorbeeld 1

U hebt bankreconciliaties uitgevoerd voor januari, februari en maart. Het bankafschriftnummer voor maart was 100. Later ontdekt u dat maart alleen vermeldingen tot en met de 30e bevatte, wat betekent dat vermeldingen voor de 31e ontbreken. U moet dus de bankreconciliatie voor maart opnieuw uitvoeren. In dit geval opent u de pagina **Bankrekeningafschrift**, kiest u het afschrift voor maart en kiest u vervolgens **Ongedaan maken**. 

De nieuwe bankreconciliatie krijgt afschriftnummer 101. Als u het nummer 100 opnieuw wilt toewijzen, kiest u **Afschriftnr. wijzigen** en voert u **100** in. 

> [!TIP]
> Vergeet niet om de juiste einddatum van het afschrift in te stellen (in dit voorbeeld is dat 31 maart) en het veld **Saldo laatste afschrift** te bewerken. 

#### <a name="example-2"></a>Voorbeeld 2

U hebt bankreconciliaties uitgevoerd voor januari, februari, juni en juli. U ontdekt dat februari niet klopte. Stel dat het afschriftnummer 100 had. Net als in voorbeeld 1 gebruikt u de acties Ongedaan maken en Afschriftnr. wijzigen om het afschriftnummer te wijzigen zoals in voorbeeld 1 hierboven en u kunt nu de bankreconciliatie van februari opnieuw uitvoeren.  

Nadat u de gecorrigeerde bankreconciliatie voor februari hebt geboekt op de bijbehorende bankrekeningkaart, bevat het veld **Laatste afschriftnr.** de waarde **100** en bevat het veld **Saldo laatste afschrift** het eindsaldo voor het februari-afschrift. 

Als de volgende bankreconciliatie die u uitvoert voor maart is, zal [!INCLUDE[d365fin](includes/d365fin_md.md)] 101 toewijzen als het afschriftnummer en het het juiste **Saldo laatste afschrift** geven.

Als de volgende bankreconciliatie die u uitvoert voor augustus is, kunt u overwegen de waarden in de velden **Laatste afschriftnr.** en **Saldo laatste afschrift** op de kaart **Bankrekening** te wijzigen voordat u de volgende bankreconciliatie maakt, of gebruik de actie **Afschriftnr. wijzigen** en wijzig ook de waarde in het veld **Saldo laatste afschrift** op de bankreconciliatiepagina.

> [!NOTE]
> Het afschriftnummer is belangrijk wanneer u bankreconciliaties uitvoert met geïmporteerde CAMT-bestanden die afschriftnummers bevatten, of wanneer u reconcilieert op basis van afgedrukte bankafschriften. Als u gewoon een reeks banktransacties van uw online bank downloadt, is het afschriftnummer meestal niet belangrijk.  
>
> Het saldo laatste afschrift wordt in de bankrekening bewaard om fouten bij het uitvoeren van bankreconciliaties te minimaliseren, maar het is ook bewerkbaar, zodat u uw bankreconciliaties in elke gewenste volgorde kunt uitvoeren. Dit betekent ook dat als u een bankafschrift ongedaan maakt, het nieuwe eindsaldo mogelijk niet het laatste afschriftsaldo op het volgende bankafschrift is. Er is geen functie waarmee u een saldo naar alle volgende bankafschriften kunt verplaatsen, dus houd hier rekening mee wanneer u Ongedaan maken gebruikt.  

## <a name="avoid-direct-posting"></a>Direct boeken voorkomen

Gebruik geen grootboekrekening waarop direct boeken in uw boekingsgroep voor bankrekeningen toegestaan is. Direct boeken verbreekt de verbinding tussen de bankrekeningpost en de grootboekrekeningpost. Wanneer u uw bankrekening afstemt, worden de posten die rechtstreeks naar de grootboekrekening zijn geboekt, niet opgenomen en is het moeilijk om de reconciliatie te voltooien.

Deze fout komt vaak voor bij het invoeren van een beginsaldo voor een bankrekening. Het is belangrijk dat u het beginsaldo niet rechtstreeks in het grootboek boekt. Posten op de grootboekrekening die rechtstreeks naar de grootboekrekening worden geboekt, veroorzaken problemen. Deze posten kunnen er bijvoorbeeld voor zorgen dat u uw bankrekening niet kunt afstemmen. Voor bankrekeningen in vreemde valuta kunnen de posten verschillen veroorzaken nadat u meer bankreconciliaties hebt geboekt als gevolg van wisselkoersaanpassingen. Vaak boekt u het beginsaldo direct op de bankrekening en komt het bedrag dan op de grootboekrekening terecht. U kunt het ook later terugboeken naar de grootboekrekening die u gebruikt om het openingsgrootboeksaldo te compenseren. In beide gevallen moet u eventuele directe boekingen op de grootboekrekening salderen voordat u uw eerste bankafstemming start, en vooral als de bankrekening in een vreemde valuta is.

## <a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/modules/bank-reconciliation-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Bankrekeningen reconciliëren](bank-manage-bank-accounts.md)  
[Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Bankieren instellen](bank-setup-banking.md)  
[Regels instellen voor automatische vereffening van betalingen](receivables-how-set-up-payment-application-rules.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
