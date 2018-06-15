---
title: "Bankrekeningen apart reconciliëren| Microsoft Docs"
description: Beschrijft hoe uw voorraadwaarde wordt gereconcilieerd met het grootboek.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank account balance, bank statement
ms.date: 05/15/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 32f5b2b19dc74d3849a313e3d93fdb70146cdb23
ms.contentlocale: nl-be
ms.lasthandoff: 05/17/2018

---
# <a name="reconcile-bank-accounts-separately"></a>Bankrekeningen apart reconciliëren
Als u bankrekeningen in [!INCLUDE[d365fin](includes/d365fin_md.md)] wilt reconciliëren met afschriften die worden ontvangen van de bank, begint u met het linkerdeelvenster in het venster **Bankreconciliatie** in te vullen met bankafschriftgegevens die u dan reconcilieert met bankrekeningposten in het rechterdeelvenster. Een slimme manier om bankafschriftregels in te vullen is een bankafschriftbestand of -feed te importeren.

> [!NOTE]  
> In Noord-Amerikaanse versies kunt u dit werk ook doen in het venster **Werkblad bankreconciliatie**, dat geschikter is voor cheques en borgsommen, maar geen importeren van bankafschriftbestanden biedt. Als u dit venster wilt gebruiken in plaats van het venster **Bankreconciliatie**, schakelt u het veld **Bankreconciliatie met automatische afstemming** uit in het venster **Boekhoudinstellingen**. Zie voor meer informatie het gedeelte "Bankrekeningen reconciliëren" onder Lokale functionaliteit voor de Verenigde Staten.

> [!TIP]  
> U kunt bankrekeningen ook reconciliëren in het venster **Betalingsreconciliatiedagboek**. Eventuele open bankrekeningposten die gerelateerd zijn aan de vereffende klant- of leveranciersposten, worden gesloten wanneer u de actie **Betalingen boeken en bankrekening reconciliëren** kiest. Dit betekent dat de bankrekening automatisch wordt gereconcilieerd voor betalingen die u met het dagboek boekt. Zie voor meer informatie [Betalingen vereffenen met automatische vereffening](receivables-how-reconcile-payments-auto-application.md).

Als u de import van bankafschriften als bankfeeds wilt inschakelen, moet u eerst de feedservice van de Envestnet Yodlee Bank instellen en inschakelen en vervolgens uw bankrekeningen aan de gerelateerde online bankrekeningen koppelen. Zie voor meer informatie [De feedservice van de Envestnet Yodlee Bank instellen](bank-how-setup-bank-statement-service.md).

De regels in het venster **Bankreconciliatie** zijn verdeeld in twee deelvensters. Het deelvenster **Bankafschriftregels** bevat geïmporteerde bankafschriften of posten met openstaande betalingen. Het deelvenster **Bankposten** bevat de posten op de bankrekening.

Het opzoeken en vereffenen van posten die moeten worden gereconcilieerd, wordt *afstemmen* genoemd. U kunt kiezen om afstemming automatisch uit te voeren via de functie **Automatisch afstemmen**. U kunt ook handmatig regels selecteren in beide deelvensters om elke bankafschriftregel te koppelen aan een of meer verwante bankposten, en vervolgens de functie **Handmatig afstemmen** gebruiken. Het selectievakje **Vereffend** is ingeschakeld op regels waar posten overeenkomen.

U kunt het deelvenster **Bankafschriftregels** in het venster **Bankreconciliatie** als volgt vullen:

* Automatisch, door de functie **Bankafschrift importeren** te gebruiken om de regels in te vullen overeenkomstig werkelijke bankafschriften op basis van een bestand dat door de bank wordt geleverd.
* Handmatig, door de functie **Regels voorstellen** te gebruiken om de regels in te vullen met posten voor facturen die openstaande betalingen hebben.

Wanneer de waarde in het veld **Totaalsaldo** in het deelvenster **Bankafschriftregels** gelijk is aan de waarde in het veld **Af te stemmen saldo** in het deelvenster **Bankposten**, kunt u de actie **Boeken** kiezen om de vereffende bankposten te vereffenen. Niet-vereffende bankposten blijven in het venster. Dit geeft aan dat betalingen die zijn verwerkt voor de bankrekening, niet worden weergegeven op het laatste bankafschrift of dat voor sommige betalingen cheques zijn ontvangen.

> [!NOTE]  
>   Als bankafschriftregels op chequeposten betrekking hebben, kunt u de gewenste afstemfuncties niet gebruiken. In plaats hiervan moet u de actie **Posten vereffenen** kiezen en de relevante chequepost selecteren om de bankafschriftregel mee af te stemmen.

## <a name="to-fill-bank-reconciliation-lines-by-importing-a-bank-statement"></a>Bankreconciliatieregels vullen door een bankafschrift te importeren
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Bankreconciliatie** in en klik vervolgens op de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Selecteer in het veld **Bankrekeningnr.** de relevante bankrekening. De bankposten die bestaan voor de bankrekening, worden weergegeven in het deelvenster **Bankposten**.
4. Voer de datum van het rekeningoverzicht van de bank in het veld **Afschriftdatum** in.
5. Voer het saldo van het bankafschrift in het veld **Eindsaldo afschrift** in.
6. Als u een bankafschriftbestand hebt ingesteld, kiest u de actie **Bankafschrift importeren**.
7. Zoek het bestand en kies **Openen** om de banktransacties te importeren in de regels van het venster **Bankreconciliatie**.

## <a name="to-fill-bank-reconciliation-lines-with-the-suggest-lines-function"></a>Bankreconciliatieregels vullen met de functie Regels voorstellen
1. Kies in het venster **Bankreconciliatie** de actie **Regels voorstellen**.
2. Voer in het veld **Begindatum** de vroegste boekingsdatum in voor de posten waarop u de reconciliatie wilt uitvoeren.
3. Voer in het veld **Einddatum** de laatste boekingsdatum in voor de posten waarop u de reconciliatie wilt uitvoeren.
4. Schakel het selectievakje **Inclusief cheques** in om chequeposten voor te stellen in plaats van de corresponderende bankposten.
5. Kies de knop **Ok**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-automatically"></a>Bankafschriftregels automatisch afstemmen met bankrekeningposten
Het venster biedt automatische afstemmingsfunctionaliteit waarmee betalingen worden vereffend met de gerelateerde open posten op basis van een afstemming van tekst op een bankafschriftregel (linkerdeelvenster) met tekst in een of meer bankrekeningposten (rechterdeelvenster). U kunt de voorgestelde automatische vereffeningen overschrijven en u kunt ervoor kiezen helemaal geen automatische vereffening te gebruiken. Zie de volgende procedure voor meer informatie.

1. Kies in het venster **Bankreconciliatie** de actie **Automatisch afstemmen**. Het venster **Bankposten afstemmen** verschijnt.
2. Geef in het veld **Datumtolerantie van transactie (dagen)** het aantal dagen op vóór en na de boekingsdatum van de bankpost waarbinnen de functie naar overeenkomstige transactiedatums in het bankafschrift zoekt.

    Als u 0 typt of het veld leeg laat, zoekt de functie **Automatisch afstemmen** alleen naar overeenkomende transactiedatums op de bankpostboekingsdatum.
3. Kies de knop **Ok**.

    Alle bankafschriftregels en bankrekeningposten die kunnen worden afgestemd, worden in groene letters weergegeven, en het selectievakje **Vereffend** wordt geselecteerd.
4. Als u een afstemming wilt verplaatsen, selecteert u de bankafschriftregel en kiest u vervolgens **Afstemming verwijderen**.

## <a name="to-match-bank-statement-lines-with-bank-account-ledger-entries-manually"></a>Bankafschriftregels handmatig afstemmen met bankrekeningposten
1. Selecteer in het venster **Bankreconciliatie** een niet-vereffende regel in het deelvenster **Bankafschriftregels**.
2. Selecteer in het deelvenster **Bankposten** een of meer bankrekeningposten die met de geselecteerde bankafschriftregel kunnen worden afgestemd. Om meerdere regels te kiezen drukt u op de Ctrl-toets en houdt u deze ingedrukt.
3. Kies de actie **Handmatig afstemmen**.

    De geselecteerde bankafschriftregel en de geselecteerde bankrekeningposten worden in groene letters weergegeven en het selectievakje **Vereffend** in het rechtervenster wordt geselecteerd.
4. Herhaal stap 1 t/m 3 voor alle bankafschriftregels die niet overeenkomen.
5. Als u een afstemming wilt verplaatsen, selecteert u de bankafschriftregel en kiest u vervolgens **Afstemming verwijderen**.

## <a name="to-create-missing-ledger-entries-to-match-bank-transactions-with"></a>Ontbrekende posten maken om banktransacties mee af te stemmen
Soms bevat een bankafschrift bedragen voor in rekening gebrachte rente of toeslagen. Dergelijke banktransacties kunnen niet worden afgestemd omdat er geen gerelateerde posten bestaan in [!INCLUDE[d365fin](includes/d365fin_md.md)]. U moet vervolgens voor elke transactie een dagboekregel boeken om een gerelateerde post te maken waarmee deze kan worden afgestemd.

1. Kies in het venster **Bankreconciliatie** de actie **Naar dagboek overbrengen**.  
2. Geef in het venster **Bankreconciliatie naar dagboek** op welk dagboek moet worden gebruikt en kies vervolgens de knop **OK**.

    Het venster **Diversendagboek** wordt geopend met nieuwe dagboekregels voor bankafschriftregels met ontbrekende posten.
3. Vul de dagboekregel met de relevante gegevens, zoals de tegenrekening. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.  
4. Als u het resultaat van de boeking wilt controleren voordat u boekt, kiest u de actie **Testrapport**. Het rapport **Bankrekeningafschrift** wordt geopend en bevat dezelfde velden als de koptekst van het venster **Bankreconciliatie**.
4. Kies de actie **Boeken**.

    Wanneer de post wordt geboekt, stemt u de banktransactie ermee af.
5. Het venster **Bankreconciliatie** vernieuwen of opnieuw openen. De nieuwe post wordt in het deelvenster **Bankposten** weergegeven.
6. Stem de bankafschriftregel handmatig of automatisch af met de bankpost.

## <a name="see-also"></a>Zie ook
[Bankrekeningen beheren](bank-manage-bank-accounts.md)  
[Bankieren instellen](bank-setup-banking.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

