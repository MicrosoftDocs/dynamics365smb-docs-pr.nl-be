---
title: Bankrekeningen afstemmen
description: In dit onderwerp wordt beschreven hoe u de transacties op uw interne bankrekeningen afstemt met de transacties op afschriften van uw bank.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.search.form: 379, 388, 1290, 10124
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: 7880227a09696b6de8411a09ba04ebd3e2395543
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/14/2022
ms.locfileid: "7971495"
---
# <a name="reconcile-bank-accounts"></a>Bankrekeningen afstemmen

U voert bankafstemming uit om ervoor te zorgen dat uw verschillende zakelijke transacties en uitgaven correct worden weergegeven in de bedrijfsboeken. U doet dit door boekingen op uw interne bankrekeningen te vergelijken en af te stemmen met banktransacties bij uw bank en vervolgens de saldi op uw interne bankrekeningen te boeken om totalen beschikbaar te stellen voor financiële managers. Bankafstemming is ook een praktische manier om ontbrekende betalingen en boekhoudfouten te ontdekken en op te lossen.

Hieronder wordt beschreven hoe u bankafstemming met de pagina **Bankreconciliatie**.

> [!TIP]
> U kunt ook bankrekeningen afstemmen op de pagina **Betalingsreconciliatiedagboek** wanneer u betalingen verwerkt. Eventuele open bankrekeningposten die gerelateerd zijn aan de vereffende klant- of leveranciersposten, worden gesloten wanneer u de actie **Betalingen boeken en bankrekening reconciliëren** kiest. Dit betekent dat de bankrekening automatisch wordt gereconcilieerd voor de betalingen die u met het dagboek boekt. Zie voor meer informatie [Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> In de Noord-Amerikaanse versies kunt u dit werk ook doen op de pagina **Werkblad bankreconciliatie**, dat geschikter is voor cheques en borgsommen, maar geen importeren van bankafschriftbestanden biedt. Als u deze pagina wilt gebruiken in plaats van de pagina **Bankreconciliatie**, schakelt u het veld **Bankreconciliatie met automatische afstemming** uit op de pagina **Boekhoudinstellingen**. Zie voor meer informatie [Bankrekeningen reconciliëren](LocalFunctionality/UnitedStates/how-to-reconcile-bank-accounts.md) onder Lokale functionaliteit voor de Verenigde Staten.

De regels op de pagina **Bankreconciliatie** zijn verdeeld in twee deelvensters. Het deelvenster **Bankafschriftregels** bevat geïmporteerde bankafschriften of posten met openstaande betalingen. Het deelvenster **Bankposten** bevat de posten op de interne bankrekening.

Het reconciliëren van banktransacties met interne bankposten wordt *afstemmen* genoemd. U kunt kiezen om afstemming automatisch uit te voeren via de functie **Automatisch afstemmen**. U kunt ook handmatig regels selecteren in beide deelvensters om elke bankafschriftregel te koppelen aan een of meer verwante bankposten, en vervolgens de functie **Handmatig afstemmen** gebruiken. Het selectievakje **Vereffend** is ingeschakeld op regels waar posten overeenkomen. Zie [Regels instellen voor automatische vereffening van betalingen](receivables-how-set-up-payment-application-rules.md) voor meer informatie.

> [!NOTE]  
> Als bankafschriftregels betrekking hebben op chequeposten, kunt u de afstemfuncties niet gebruiken. In plaats hiervan moet u de actie **Posten vereffenen** kiezen en de relevante chequepost selecteren om de bankafschriftregel mee af te stemmen.

Wanneer de waarde in het veld **Totaalsaldo** in het deelvenster **Bankafschriftregels** gelijk is aan de totale waarde in het veld **Af te stemmen saldo** plus het veld **Saldo laatste afschrift** in het deelvenster **Bankposten**, kunt u de actie **Boeken** kiezen. Niet-afgestemde bankposten blijven op de pagina staan, wat aangeeft dat er een verschil is dat u moet oplossen om de bankrekening af te stemmen.

Regels die niet kunnen worden afgestemd, aangeduid met een waarde in het veld **Verschil**, blijven na boeking op de pagina **Bankreconciliatie** staan. Er is daarmee een verschil geconstateerd dat u moet oplossen voordat u de afstemming van de bankrekening kunt afronden. Veel voorkomende bedrijfssituaties die verschillen kunnen veroorzaken:

| Verschil | Reden  | Oplossing |
|------------|--------|------------|
| Een transactie op de interne bankrekening staat niet op het bankafschrift. | De banktransactie heeft niet plaatsgevonden, hoewel er wel een boeking is gedaan in [!INCLUDE[prod_short](includes/prod_short.md)]. | Voer de ontbrekende geldtransactie uit (of vraag een debiteur om deze uit te voeren) en importeer vervolgens het bankafschriftbestand opnieuw of voer de transactie handmatig in. |
| Een transactie op het bankafschrift is niet een document of journaalregel in [!INCLUDE[prod_short](includes/prod_short.md)]. | Er is een banktransactie uitgevoerd zonder een overeenkomstige boeking in [!INCLUDE[prod_short](includes/prod_short.md)], bijvoorbeeld een boeking in een dagboekregel voor een uitgave. | Maak en plaats de ontbrekende post. Zie [Ontbrekende posten maken om banktransacties mee af te stemmen](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines-with) voor informatie over een snelle manier om dit te doen. |
| Een transactie op de interne bankrekening komt overeen met een banktransactie, maar bepaalde informatie is te verschillend om een match te geven. | Informatie, zoals het bedrag of de naam van de klant, ios anders ingevoerd in verband met de banktransactie of de interne boeking. | Controleer de informatie en stem deze vervolgens handmatig af. Corrigeer eventueel de niet-overeenkomende informatie. |

U moet de verschillen oplossen, bijvoorbeeld door ontbrekende posten te maken en niet-overeenkomende informatie te corrigeren, of door ontbrekende geldtransacties in te voeren, totdat de afstemming van de bankrekening is voltooid en geboekt.

U kunt het deelvenster **Bankafschriftregels** op de pagina **Bankreconciliatie** als volgt vullen:

* Automatisch, door de functie **Bankafschrift importeren** te gebruiken om het deelvenster **Bankafschriftregels** in te vullen met banktransacties volgens een geïmporteerd bestand of een stream die door de bank is aangeleverd.
* Handmatig, door de functie **Regels voorstellen** te gebruiken om het deelvenster **Bankafschriftregels** in te vullen volgens facturen in [!INCLUDE[prod_short](includes/prod_short.md)] met openstaande betalingen.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Bankreconciliatieregels vullen door een bankafschrift te importeren

Het deelvenster **Bankafschriftregels** wordt gevuld met banktransacties volgens een geïmporteerd bestand of een stream die door de bank is aangeleverd.

Als u de import van bankafschriften als bankfeeds wilt inschakelen, moet u eerst de service Envestnet Yodlee Bank Feeds instellen en inschakelen en vervolgens uw bankrekeningen aan de gerelateerde online bankrekeningen koppelen. Zie voor meer informatie [De Envestnet Yodlee Bank Feeds-service instellen](bank-how-setup-bank-statement-service.md).  

> [!TIP]
> U kunt ook bankafschriftbestanden importeren in een door komma's of puntkomma's gescheiden indeling (.CSV). Gebruik de begeleide instelling **Een importindeling voor het bankafschriftbestand instellen** om de importindelingen voor bankafschriften te definiëren en de indeling aan een bankrekening te koppelen. U kunt deze indelingen vervolgens gebruiken wanneer u bankafschriften importeert op de pagina **Bankreconciliatie**.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Bankreconciliatie** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Selecteer in het veld **Bankrekeningnr.** de relevante bankrekening. De bankposten die bestaan voor de bankrekening, worden weergegeven in het deelvenster **Bankposten**.
4. Voer de datum van het rekeningoverzicht van de bank in het veld **Afschriftdatum** in.
5. Voer het saldo van het bankafschrift in het veld **Eindsaldo afschrift** in.
6. Als u een bankafschriftbestand hebt ingesteld, kiest u de actie **Bankafschrift importeren**.
7. Zoek het bestand en kies **Openen** om de banktransacties te importeren in het deelvenster **Bankafschriftregels** op de pagina **Bankreconciliatie**.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>Bankreconciliatieregels vullen met de functie Regels voorstellen

Het deelvenster **Bankafschriftregels** wordt ingevuld volgens facturen in [!INCLUDE[prod_short](includes/prod_short.md)] met openstaande betalingen.  

1. Kies op de pagina **Bankreconciliatie** de actie **Regels voorstellen**.
2. Voer in het veld **Begindatum** de vroegste boekingsdatum in voor de posten waarop u de reconciliatie wilt uitvoeren.
3. Voer in het veld **Einddatum** de laatste boekingsdatum in voor de posten waarop u de reconciliatie wilt uitvoeren.

> [!NOTE]
> Doorgaans komt de einddatum overeen met de datum die is opgegeven in het veld **Afschriftdatum**. Als u echter transacties voor slechts een deel van een periode wilt afstemmen, kunt u een andere einddatum invoeren. 

1. Schakel het selectievakje **Inclusief cheques** in om chequeposten voor te stellen in plaats van de corresponderende bankposten.
1. Kies de knop **Ok**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Bankafschriftregels automatisch afstemmen met bankrekeningposten

De pagina **Bankreconciliatie** biedt automatische afstemmingsfunctionaliteit op basis van een afstemming van tekst op een bankafschriftregel (linkerdeelvenster) met tekst in een of meer bankposten (rechterdeelvenster). U kunt de voorgestelde automatische afstemming overschrijven en u kunt ervoor kiezen helemaal geen automatische afstemming te gebruiken. Zie [Bankafschriftregels handmatig afstemmen met bankrekeningposten](bank-how-reconcile-bank-accounts-separately.md#to-match-bank-statement-lines-with-bank-account-ledger-entries-manually) voor meer informatie.

Met automatisch afstemmen worden posten afgestemd op basis van een set regels voor betalingsvereffening. Zie [Regels instellen voor automatische vereffening van betalingen](receivables-how-set-up-payment-application-rules.md) voor meer informatie. U kunt de basis voor overeenkomsten onderzoeken met behulp van de actie **Afstemmingsdetails**. De details bevatten bijvoorbeeld de namen van de velden die overeenkomende waarden bevatten.  

1. Kies op de pagina **Bankreconciliatie** de actie **Automatisch afstemmen**. De pagina **Bankposten afstemmen** verschijnt.
2. Geef in het veld **Datumtolerantie van transactie (dagen)** het aantal dagen op vóór en na de boekingsdatum van de bankpost waarbinnen de functie naar overeenkomstige transactiedatums in het bankafschrift zoekt.

    Als u 0 typt of het veld leeg laat, zoekt de actie **Automatisch afstemmen** alleen naar overeenkomende transactiedatums op de bankpostboekingsdatum.
3. Kies de knop **Ok**.

    Alle bankafschriftregels en bankrekeningposten die kunnen worden afgestemd, worden in groene letters weergegeven, en het selectievakje **Vereffend** wordt geselecteerd.
4. Als u een afstemming wilt verplaatsen, selecteert u de bankafschriftregel en kiest u vervolgens **Afstemming verwijderen**.

> [!TIP]
> U kunt een mix van handmatige en automatische afstemming gebruiken. Als u handmatig afgestemde posten hebt, zal automatische afstemming uw selecties niet overschrijven. 

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Bankafschriftregels handmatig afstemmen met bankrekeningposten
1. Selecteer op de pagina **Bankreconciliatie** een niet-vereffende regel in het deelvenster **Bankafschriftregels**.
2. Selecteer in het deelvenster **Bankposten** een of meer bankrekeningposten die met de geselecteerde bankafschriftregel kunnen worden afgestemd. Om meerdere regels te kiezen drukt u op de Ctrl-toets en houdt u deze ingedrukt.

   > [!TIP]
   > U kunt ook handmatig meerdere bankafschriftregels afstemmen met één bankrekeningpost. Dit kan bijvoorbeeld handig zijn als uw bankdeposito verschillende betaalmethoden bevat, zoals creditcards van verschillende uitgevers, en uw bank deze als afzonderlijke regels vermeldt. 
3. Kies de actie **Handmatig afstemmen**.

    De geselecteerde bankafschriftregel en de geselecteerde bankrekeningposten worden in groene letters weergegeven en het selectievakje **Vereffend** in het rechtervenster wordt geselecteerd.
4. Herhaal stap 1 t/m 3 voor alle bankafschriftregels die niet overeenkomen.

> [!TIP]
> Als u een afstemming wilt verplaatsen, selecteert u de bankafschriftregel en kiest u vervolgens **Afstemming verwijderen**. Als u meerdere bankafschriftregels op een grootboekpost hebt afgestemd en een of meer van de afgestemde regels moet verwijderen, worden alle handmatige afstemmingen voor de grootboekboeking verwijderd wanneer u **Afstemming verwijderen** kiest. 

## <a name="to-create-missing-ledger-entries-to-match-bank-statement-lines-with"></a>Ontbrekende posten maken om bankafschriftregels mee af te stemmen

Soms bevat een bankafschrift bedragen voor in rekening gebrachte rente of toeslagen. Dergelijke bankafschriftregels kunnen niet worden afgestemd omdat er geen gerelateerde posten bestaan in [!INCLUDE[prod_short](includes/prod_short.md)]. U moet vervolgens voor elke transactie een dagboekregel boeken om een gerelateerde post te maken waarmee deze kan worden afgestemd.

1. Kies op de pagina **Bankreconciliatie** de actie **Naar dagboek overbrengen**.  
2. Geef op de pagina **Bankreconciliatie naar dagboek** op welk dagboek moet worden gebruikt en kies vervolgens de knop **OK**.

    De pagina **Diversendagboek** wordt geopend met nieuwe dagboekregels voor bankafschriftregels met ontbrekende posten.
3. Vul de dagboekregel met de relevante gegevens, zoals de tegenrekening. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.  
4. Als u het resultaat van de boeking wilt controleren voordat u boekt, kiest u de actie **Testrapport**. Het rapport **Bankrekeningafschrift** wordt geopend en bevat dezelfde velden als de koptekst van de pagina **Bankreconciliatie**.
5. Kies de actie **Boeken**.

    Wanneer de post is geboekt, stemt u de bankafschriftregel ermee af.
6. Vernieuw de pagina **Bankreconciliatie** of open deze opnieuw. De nieuwe post wordt in het deelvenster **Bankposten** weergegeven.
7. Stem de bankafschriftregel handmatig of automatisch af met de bankpost.

## <a name="undo-a-bank-account-reconciliation"></a>Een bankrekeningreconciliatie ongedaan maken
Als u een fout ontdekt in een geboekte bankreconciliatie, kunt u de actie **Ongedaan maken** op de pagina **Bankrekeningafschrift** gebruiken om de fout te corrigeren. Wanneer u een geboekte bankreconciliatie ongedaan maakt, worden de boekingen verplaatst naar de pagina **Bankreconciliatie** en gemarkeerd als **Open**, wat betekent dat ze niet gereconcilieerd zijn. U kunt vervolgens de bankreconciliatie corrigeren en opnieuw boeken.

> [!NOTE]
> Als u in de Noord-Amerikaanse versie de functie Ongedaan maken wilt gebruiken voor geboekte bankreconciliaties en bankafschriften, moet u de schakelaar **Bankreconciliatie met automatische afstemming** inschakelen op de pagina **Grootboekinstellingen**. De functie Ongedaan maken is niet beschikbaar voor bankafschriften die zijn geboekt vanuit werkbladen voor bankreconciliatie.

### <a name="reusing-the-bank-statement-number"></a>Het bankafschriftnummer opnieuw gebruiken
Het nummer van het bankafschrift dat wordt gebruikt voor de nieuwe bankreconciliatie, wordt van de bankrekening overgenomen, evenals het laatste overzicht van het saldo. U kunt deze waarden wijzigen voordat u een nieuwe bankreconciliatie start. Wanneer u echter een nieuwe bankreconciliatie maakt, controleert [!INCLUDE[d365fin](includes/d365fin_md.md)] of het afschriftnummer al is toegewezen aan een geboekt bankafschrift. Als het nummer in gebruik is, maar u wilt dat het nieuwe bankafschrift het gebruikt, kunt u de actie **Afschriftnr. wijzigen** gebruiken op de pagina **Reconciliatie van bankrekening**.

### <a name="examples"></a>Voorbeelden
Hieronder volgen enkele voorbeelden van hoe u een fout kunt herstellen in een geboekte bankreconciliatie met of zonder gebruik van hetzelfde afschriftnummer.

#### <a name="example-1"></a>Voorbeeld 1
U hebt bankreconciliaties uitgevoerd voor januari, februari en maart. Het bankafschriftnummer voor maart was 100. Later ontdekt u dat maart alleen vermeldingen tot en met de 30e bevatte, wat betekent dat vermeldingen voor de 31e ontbreken. U moet dus de bankreconciliatie voor maart opnieuw uitvoeren. In dit geval opent u de pagina **Bankrekeningafschrift**, kiest u het afschrift voor maart en kiest u vervolgens **Ongedaan maken**. 

De nieuwe bankreconciliatie krijgt afschriftnummer 101. Als u het nummer 100 opnieuw wilt toewijzen, kiest u **Afschriftnr. wijzigen** en voert u **100** in. 

> [!TIP]
> Vergeet niet om de juiste einddatum van het afschrift in te stellen (in dit voorbeeld is dat 31 maart) en het veld **Saldo laatste afschrift** te bewerken. 

#### <a name="example-2"></a>Voorbeeld 2
U hebt bankreconciliaties uitgevoerd voor januari, februari, juni en juli. U ontdekt dat februari niet klopte. Stel dat het afschriftnummer 100 had. Net als in voorbeeld 1 gebruikt u de acties Ongedaan maken en Afschriftnr. wijzigen om het afschriftnummer te wijzigen zoals in voorbeeld 1 hierboven en u kunt nu de bankreconciliatie van februari opnieuw uitvoeren.  

Nadat u de gecorrigeerde bankreconciliatie voor februari hebt geboekt op de bijbehorende bankrekeningkaart, bevat het veld **Laatste afschriftnr.** de waarde **100** en bevat het veld **Saldo laatste afschrift** het eindsaldo voor het februari-afschrift. 

Als de volgende bankreconciliatie die u uitvoert voor maart is, zal [!INCLUDE[d365fin](includes/d365fin_md.md)] 101 toewijzen als het afschriftnummer en het het juiste **Saldo laatste afschrift** geven.

Als de volgende bankreconciliatie die u uitvoert voor augustus is, kunt u overwegen de waarden in de velden **Laatste afschriftnr.** en **Saldo laatste afschrift** op de **Bankrekening** kaart te wijzigen voordat u de volgende bankreconciliatie maakt, of de actie Afschriftnr. wijzigen gebruiken en ook de waarde in het veld "Saldo laatste afschrift" op de bankreconciliatiepagina wijzigen.

> [!NOTE]
> Het afschriftnummer is belangrijk wanneer u bankreconciliaties uitvoert met geïmporteerde CAMT-bestanden die afschriftnummers bevatten, of wanneer u reconcilieert op basis van afgedrukte bankafschriften. Als u gewoon een reeks banktransacties van uw online bank downloadt, is het afschriftnummer meestal niet belangrijk. 
>
>Het saldo laatste afschrift wordt in de bankrekening bewaard om fouten bij het uitvoeren van bankreconciliaties te minimaliseren, maar het is ook bewerkbaar, zodat u uw bankreconciliaties in elke gewenste volgorde kunt uitvoeren. Dit betekent ook dat als u een bankafschrift ongedaan maakt, het nieuwe eindsaldo mogelijk niet het laatste afschriftsaldo op het volgende bankafschrift is. Er is geen functie waarmee u een saldo naar alle volgende bankafschriften kunt verplaatsen, dus houd hier rekening mee wanneer u Ongedaan maken gebruikt. 

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/bank-reconciliation-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Bankrekeningen reconciliëren](bank-manage-bank-accounts.md)  
[Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Bankieren instellen](bank-setup-banking.md)  
[Regels instellen voor automatische vereffening van betalingen](receivables-how-set-up-payment-application-rules.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]