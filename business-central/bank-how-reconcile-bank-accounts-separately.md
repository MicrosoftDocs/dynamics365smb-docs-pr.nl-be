---
title: Bankrekeningen afstemmen | Microsoft Docs
description: Beschrijft hoe uw voorraadwaarde wordt gereconcilieerd met het grootboek.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: e53c1f7b0b2af4a94579863197ec7348c9b6ff18
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3186320"
---
# <a name="reconcile-bank-accounts"></a>Bankrekeningen afstemmen
U voert bankafstemming uit om ervoor te zorgen dat uw verschillende zakelijke transacties en uitgaven correct worden weergegeven in de bedrijfsboeken. U doet dit door boekingen op uw interne bankrekeningen te vergelijken en af te stemmen met banktransacties bij uw bank en vervolgens de saldi op uw interne bankrekeningen te boeken om totalen beschikbaar te stellen voor financiële managers. Bankafstemming is ook een praktische manier om ontbrekende betalingen en boekhoudfouten te ontdekken en op te lossen.

Hieronder wordt beschreven hoe u bankafstemming met de pagina **Bankreconciliatie**.

> [!TIP]
> U kunt ook bankrekeningen afstemmen op de pagina **Betalingsreconciliatiedagboek** in verband met betalingsverwerking. Eventuele open bankrekeningposten die gerelateerd zijn aan de vereffende klant- of leveranciersposten, worden gesloten wanneer u de actie **Betalingen boeken en bankrekening reconciliëren** kiest. Dit betekent dat de bankrekening automatisch wordt gereconcilieerd voor betalingen die u met het dagboek boekt. Zie voor meer informatie [Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md).

> [!NOTE]  
> In Noord-Amerikaanse versies kunt u dit werk ook doen op de pagina **Werkblad bankreconciliatie**, dat geschikter is voor cheques en borgsommen, maar geen importeren van bankafschriftbestanden biedt. Als u deze pagina wilt gebruiken in plaats van de pagina **Bankreconciliatie**, schakelt u het veld **Bankreconciliatie met automatische afstemming** uit op de pagina **Boekhoudinstellingen**. Zie voor meer informatie het gedeelte "Bankrekeningen reconciliëren" onder Lokale functionaliteit voor de Verenigde Staten.

De regels op de pagina **Bankreconciliatie** zijn verdeeld in twee deelvensters. Het deelvenster **Bankafschriftregels** bevat geïmporteerde bankafschriften of posten met openstaande betalingen. Het deelvenster **Bankposten** bevat de posten op de interne bankrekening.

De activiteit van het afstemmen van banktransacties met interne bankposten wordt *afstemmen* genoemd. U kunt kiezen om afstemming automatisch uit te voeren via de functie **Automatisch afstemmen**. U kunt ook handmatig regels selecteren in beide deelvensters om elke bankafschriftregel te koppelen aan een of meer verwante bankposten, en vervolgens de functie **Handmatig afstemmen** gebruiken. Het selectievakje **Vereffend** is ingeschakeld op regels waar posten overeenkomen. Zie [Regels instellen voor automatische vereffening van betalingen](receivables-how-set-up-payment-application-rules.md) voor meer informatie.

> [!NOTE]  
> Als bankafschriftregels betrekking hebben op chequeposten, kunt u de afstemfuncties niet gebruiken. In plaats hiervan moet u de actie **Posten vereffenen** kiezen en de relevante chequepost selecteren om de bankafschriftregel mee af te stemmen.

Wanneer de waarde in het veld **Totaalsaldo** in het deelvenster **Bankafschriftregels** gelijk is aan de waarde in het veld **Af te stemmen saldo** in het deelvenster **Bankposten**, kunt u de actie **Boeken** kiezen. Niet-afgestemde bankposten blijven op de pagina staan, wat aangeeft dat er een verschil is dat u moet oplossen om de bankrekening af te stemmen.

Regels die niet kunnen worden afgestemd, aangeduid met een waarde in het veld **Verschil**, blijven na boeking op de pagina **Bankreconciliatie** staan. Er is daarmee een verschil geconstateerd dat u moet oplossen voordat u de afstemming van de bankrekening kunt afronden. Veel voorkomende bedrijfssituaties die verschillen kunnen veroorzaken:

|Verschil|Reden |Oplossing|
|-|-|
|Een transactie op de interne bankrekening staat niet op het bankafschrift.|De banktransactie heeft niet plaatsgevonden, hoewel er wel een boeking is gedaan in [!INCLUDE[d365fin](includes/d365fin_md.md)].|Voer de ontbrekende geldtransactie uit (of vraag een debiteur om deze uit te voeren) en importeer vervolgens het bankafschriftbestand of voer de transactie handmatig in.|
|Een transactie op het bankafschrift is niet een document of journaalregel in [!INCLUDE[d365fin](includes/d365fin_md.md)].|Er is een banktransactie uitgevoerd zonder een overeenkomstige boeking in [!INCLUDE[d365fin](includes/d365fin_md.md)], bijvoorbeeld een boeking in een dagboekregel voor een uitgave.|Maak en plaats de ontbrekende post. Zie [Ontbrekende posten maken om banktransacties mee af te stemmen](bank-how-reconcile-bank-accounts-separately.md#to-create-missing-ledger-entries-to-match-bank-statement-lines-with) voor informatie over een snelle manier om dit te doen.|
|Een transactie op de interne bankrekening komt overeen met een banktransactie, maar bepaalde informatie is te verschillend om een match te geven.|Informatie, zoals het bedrag of de naam van de klant, ios anders ingevoerd in verband met de banktransactie of de interne boeking.|Controleer de informatie en stem deze vervolgens handmatig af. Corrigeer eventueel de niet-overeenkomende informatie.||

U moet de verschillen oplossen, bijvoorbeeld door ontbrekende posten te maken en niet-overeenkomende informatie te corrigeren, of door ontbrekende geldtransacties in te voeren, totdat de afstemming van de bankrekening is voltooid en geboekt.

U kunt het deelvenster **Bankafschriftregels** op de pagina **Bankreconciliatie** als volgt vullen:

* Automatisch, door de functie **Bankafschrift importeren** te gebruiken om het deelvenster **Bankafschriftregels** in te vullen met banktransacties volgens een geïmporteerd bestand of een stream die door de bank is aangeleverd.
* Handmatig, door de functie **Regels voorstellen** te gebruiken om het deelvenster **Bankafschriftregels** in te vullen volgens facturen in [!INCLUDE[d365fin](includes/d365fin_md.md)] met openstaande betalingen.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Bankreconciliatieregels vullen door een bankafschrift te importeren
Het deelvenster **Bankafschriftregels** wordt gevuld met banktransacties volgens een geïmporteerd bestand of een stream die door de bank is aangeleverd.

Als u de import van bankafschriften als bankfeeds wilt inschakelen, moet u eerst de service Envestnet Yodlee Bank Feeds instellen en inschakelen en vervolgens uw bankrekeningen aan de gerelateerde online bankrekeningen koppelen. Zie voor meer informatie [De Envestnet Yodlee Bank Feeds-service instellen](bank-how-setup-bank-statement-service.md).

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bankreconciliatie** in en kies de desbetreffende koppeling.
2. Kies de actie **Nieuw**.
3. Selecteer in het veld **Bankrekeningnr.** de relevante bankrekening. De bankposten die bestaan voor de bankrekening, worden weergegeven in het deelvenster **Bankposten**.
4. Voer de datum van het rekeningoverzicht van de bank in het veld **Afschriftdatum** in.
5. Voer het saldo van het bankafschrift in het veld **Eindsaldo afschrift** in.
6. Als u een bankafschriftbestand hebt ingesteld, kiest u de actie **Bankafschrift importeren**.
7. Zoek het bestand en kies **Openen** om de banktransacties te importeren in het deelvenster **Bankafschriftregels** op de pagina **Bankreconciliatie**.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>Bankreconciliatieregels vullen met de functie Regels voorstellen
Het deelvenster **Bankafschriftregels** wordt ingevuld volgens facturen in [!INCLUDE[d365fin](includes/d365fin_md.md)] met openstaande betalingen.  
1. Kies op de pagina **Bankreconciliatie** de actie **Regels voorstellen**.
2. Voer in het veld **Begindatum** de vroegste boekingsdatum in voor de posten waarop u de reconciliatie wilt uitvoeren.
3. Voer in het veld **Einddatum** de laatste boekingsdatum in voor de posten waarop u de reconciliatie wilt uitvoeren.
4. Schakel het selectievakje **Inclusief cheques** in om chequeposten voor te stellen in plaats van de corresponderende bankposten.
5. Kies de knop **Ok**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Bankafschriftregels automatisch afstemmen met bankrekeningposten
De pagina **Bankreconciliatie** biedt automatische afstemmingsfunctionaliteit op basis van een afstemming van tekst op een bankafschriftregel (linkerdeelvenster) met tekst in een of meer bankposten (rechterdeelvenster). U kunt de voorgestelde automatische afstemming overschrijven en u kunt ervoor kiezen helemaal geen automatische afstemming te gebruiken. Zie [Bankafschriftregels handmatig afstemmen met bankrekeningposten](bank-how-reconcile-bank-accounts-separately.md#to-match-bank-statement-lines-with-bank-account-ledger-entries-manually) voor meer informatie.

1. Kies op de pagina **Bankreconciliatie** de actie **Automatisch afstemmen**. De pagina **Bankposten afstemmen** verschijnt.
2. Geef in het veld **Datumtolerantie van transactie (dagen)** het aantal dagen op vóór en na de boekingsdatum van de bankpost waarbinnen de functie naar overeenkomstige transactiedatums in het bankafschrift zoekt.

    Als u 0 typt of het veld leeg laat, zoekt de functie **Automatisch afstemmen** alleen naar overeenkomende transactiedatums op de bankpostboekingsdatum.
3. Kies de knop **Ok**.

    Alle bankafschriftregels en bankrekeningposten die kunnen worden afgestemd, worden in groene letters weergegeven, en het selectievakje **Vereffend** wordt geselecteerd.
4. Als u een afstemming wilt verplaatsen, selecteert u de bankafschriftregel en kiest u vervolgens **Afstemming verwijderen**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Bankafschriftregels handmatig afstemmen met bankrekeningposten
1. Selecteer op de pagina **Bankreconciliatie** een niet-vereffende regel in het deelvenster **Bankafschriftregels**.
2. Selecteer in het deelvenster **Bankposten** een of meer bankrekeningposten die met de geselecteerde bankafschriftregel kunnen worden afgestemd. Om meerdere regels te kiezen drukt u op de Ctrl-toets en houdt u deze ingedrukt.
3. Kies de actie **Handmatig afstemmen**.

    De geselecteerde bankafschriftregel en de geselecteerde bankrekeningposten worden in groene letters weergegeven en het selectievakje **Vereffend** in het rechtervenster wordt geselecteerd.
4. Herhaal stap 1 t/m 3 voor alle bankafschriftregels die niet overeenkomen.
5. Als u een afstemming wilt verplaatsen, selecteert u de bankafschriftregel en kiest u vervolgens **Afstemming verwijderen**.

## <a name="to-create-missing-ledger-entries-to-match-bank-statement-lines-with"></a>Ontbrekende posten maken om bankafschriftregels mee af te stemmen
Soms bevat een bankafschrift bedragen voor in rekening gebrachte rente of toeslagen. Dergelijke bankafschriftregels kunnen niet worden afgestemd omdat er geen gerelateerde posten bestaan in [!INCLUDE[d365fin](includes/d365fin_md.md)]. U moet vervolgens voor elke transactie een dagboekregel boeken om een gerelateerde post te maken waarmee deze kan worden afgestemd.

1. Kies op de pagina **Bankreconciliatie** de actie **Naar dagboek overbrengen**.  
2. Geef op de pagina **Bankreconciliatie naar dagboek** op welk dagboek moet worden gebruikt en kies vervolgens de knop **OK**.

    De pagina **Diversendagboek** wordt geopend met nieuwe dagboekregels voor bankafschriftregels met ontbrekende posten.
3. Vul de dagboekregel met de relevante gegevens, zoals de tegenrekening. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.  
4. Als u het resultaat van de boeking wilt controleren voordat u boekt, kiest u de actie **Testrapport**. Het rapport **Bankrekeningafschrift** wordt geopend en bevat dezelfde velden als de koptekst van de pagina **Bankreconciliatie**.
4. Kies de actie **Boeken**.

    Wanneer de post is geboekt, stemt u de bankafschriftregel ermee af.
5. Vernieuw de pagina **Bankreconciliatie** of open deze opnieuw. De nieuwe post wordt in het deelvenster **Bankposten** weergegeven.
6. Stem de bankafschriftregel handmatig of automatisch af met de bankpost.

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/bank-reconciliation-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook
[Bankrekeningen reconciliëren](bank-manage-bank-accounts.md)  
[Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
[Bankieren instellen](bank-setup-banking.md)  
[Regels instellen voor automatische vereffening van betalingen](receivables-how-set-up-payment-application-rules.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
