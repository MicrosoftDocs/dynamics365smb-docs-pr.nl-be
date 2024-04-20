---
title: Bankrekeningen reconciliëren met reconciliatiehulp
description: Meer informatie over hoe u Copilot gebruikt om bankrekeningen in Business Central af te stemmen.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 03/27/2024
ms.custom: bap-template
---

# Bankrekeningen reconciliëren met Copilot (preview)

[!INCLUDE[preview-banner](includes/preview-banner.md)]

In dit artikel wordt uitgelegd hoe u hulp bij het afstemmen van bankrekeningen kunt gebruiken om banktransacties af te stemmen met grootboekposten in Business Central.

[!INCLUDE[production-ready-preview-dynamics365](includes/production-ready-preview-dynamics365.md)]

## Over hulp bij bankrekeningreconciliatie

Hulp bij bankrekeningreconciliatie is een reeks door AI aangedreven functies die u helpen bij het reconciliëren van bankrekeningen. Hulp bij bankrekeningreconciliatie biedt u twee verschillende taken via Copilot:

- Verbeterde afstemming van transacties met grootboekposten

   U bent wellicht al vertrouwd met de actie **Automatisch afstemmen** op de pagina **Bankreconciliatie**, waarmee de meeste banktransacties automatisch worden afgestemd met grootboekposten. We noemen deze bewerking *automatisch afstemmen*. Hoewel automatisch afstemmen goed werkt, kunnen de algoritmen die het gebruikt, soms resulteren in veel niet-afgestemde transacties. Copilot gebruikt AI-technologie om resterende transacties te inspecteren en meer overeenkomsten te identificeren, op basis van de datums, bedragen en beschrijvingen. Als bijvoorbeeld meerdere facturen als één forfaitair bedrag door een klant zijn betaald, stemt Copilot de enkele bankafschriftregel af met de meerdere factuurposten.

   Ga naar [Bankrekeningen reconciliëren met Copilot](#reconcile-bank-accounts-with-copilot).

- Voorgestelde grootboekrekeningen

  Voor resterende banktransacties die niet met grootboekposten kunnen worden afgestemd, vergelijkt Copilot de transactiebeschrijving met grootboekrekeningnamen, waarbij de meest waarschijnlijke grootboekrekening wordt voorgesteld waarnaar moet worden geboekt. Copilot kan bijvoorbeeld voorstellen dat transacties met het verhaal 'Brandstofstop 24' worden geboekt naar het account 'Transport'.
  
   Ga naar [Niet-afgestemde banktransacties overbrengen naar voorgestelde grootboekrekeningen](#transfer-unmatched-bank-transactions-to-suggested-general-ledger-accounts).

## Vereisten

- Hulp bij bankrekeningreconciliatie is geactiveerd. Deze taak wordt uitgevoerd door een beheerder. [Meer informatie over het configureren van Copilot- en AI-mogelijkheden](enable-ai.md).
- Bankrekeningen in Business Central die u wilt reconciliëren, zijn gekoppeld aan een online bankrekening of zijn ingesteld met het importformaat voor bankafschriften. 
- U bent bekend met bankrekeningreconciliatie in Business Central, zoals beschreven in [Bankrekeningen reconciliëren](bank-how-reconcile-bank-accounts-separately.md). 

<!--H2s. Required. A how-to article explains how to do a task. The bulk of each H2 should be a procedure.-->
## Bankrekeningen reconciliëren met Copilot

<!-- Similar to the **Match Automatically** capability on the **Bank Acc. Reconciliation** page, Bank account reconciliation assist can also automatically matches transactions in banks statements with bank entries. The difference is that **Match Automatically** uses a native rules-based algorithm, while Bank account reconciliation assist is based AI technology though Copilot. Bank account reconciliation assist is intended to supplement the **Match Automatically** capability. While **Match Automatically** is fairly successful at matching transactions, there are some instances where it can't&mdash;which is where Bank account reconciliation assist comes. By using the **Reconcile with Copilot** action on **Bank Acc. Reconciliation** page, you can find even more matches.-->

Copilot bij bankrekeningreconciliatie is bedoeld om te worden gebruikt als aanvulling op automatisch afstemmen. Daarom wordt, wanneer u Copilot gebruikt, eerst de automatische afstemming uitgevoerd om de eerste afstemmingen te maken. Vervolgens wordt Copilot uitgevoerd om te proberen transacties af te stemmen die de automatische afstemming niet heeft verwerkt.   

Er zijn twee benaderingen voor het reconciliëren van bankrekeningen met Copilot. U kunt Copilot gebruiken om een nieuwe reconciliatie op een bankrekening te starten rechtstreeks vanuit de lijst **Bankreconciliatie** of u kunt Copilot gebruiken in een nieuwe of bestaande reconciliatie op de kaart **Bankreconciliatie**.

# [Vanuit de lijst Bankreconciliatie](#tab/fromlist) 

Met deze aanpak creëert en reconcilieert u een geheel nieuwe bankrekeningreconciliatie. Bij deze aanpak moet u de bankrekening selecteren en het bankafschriftbestand importeren als de bankrekening niet aan een online rekening is gekoppeld.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bankreconciliaties** in en kies vervolgens de gerelateerde koppeling. 
1. Selecteer de actie **Reconciliëren met Copilot** om het venster **Reconciliëren met Copilot** te openen.
1. Stel het veld **Reconciliatie uitvoeren voor deze bankrekening** in op de bankrekening die u wilt reconciliëren.

   ![Toont het venster Reconciliëren met Copilot, zodat u een nieuwe reconciliatie kunt uitvoeren](media/reconcile-bank-accounts-new-copilot.svg) 
 
1. Als de geselecteerde bankrekening niet is gekoppeld aan een online bankrekening, moet u het bankafschriftbestand importeren. Om het bestand te importeren selecteert u de waarde in het veld **Transactiegegevens gebruiken uit** of selecteert u de paperclipknop naast de knop **Genereren**. Gebruik dan **Selecteer het bestand om te importeren** om het bankafschriftbestand te importeren door het vanaf uw apparaat te slepen of door op uw apparaat te bladeren.
1. Selecteer om af te stemmen met Copilot **Genereren**.

   Copilot begint met het genereren van voorgestelde afstemmingen. Wanneer dit voltooid is, wordt het venster Reconciliëren met Copilot geopend met de resultaten van de afstemming.

1. Bekijk de voorgestelde afstemmingen zoals beschreven in de volgende sectie.

# [Vanaf een bankrekeningreconciliatiekaart](#tab/fromcard) 

Met deze aanpak gebruikt u Copilot voor een nieuwe bankrekeningreconciliatie die u handmatig maakt, of door een bestaande afstemming te bewerken. 


1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bankreconciliaties** in en kies vervolgens de gerelateerde koppeling. 
1. Ga op een van de volgende manieren te werk:

   - Selecteer **Nieuw** om een nieuwe reconciliatie te starten. 
   - Selecteer en open een bestaande reconciliatie in de lijst.
1. Selecteer op de kaart **Bankreconciliatie** **Reconciliëren met Copilot**

   ![Toont de actie Reconciliëren met Copilot op de bankreconciliatiekaart](media/bank-reconciliation-copilot-card.svg) 

   Copilot begint met het genereren van voorgestelde afstemmingen. Wanneer dit voltooid is, wordt het venster **Reconciliëren met Copilot** geopend met de resultaten van de afstemming. 

1. Bekijk de voorgestelde afstemmingen zoals beschreven in de volgende sectie. 
---

### Voorgestelde afstemmingen bekijken, opslaan of negeren

Nadat u Copilot hebt uitgevoerd, toont het venster **Reconciliëren met Copilot** de gedetailleerde resultaten, inclusief eventuele voorgestelde afstemmingen. Op dit moment zijn er geen door Copilot voorgestelde afstemmingen opgeslagen, dus u kunt de voorstellen bekijken, en opslaan of verwijderen, verwijderen zoals u wilt.

![Toont het venster Reconciliëren met Copilot met voorgestelde afstemmingen](media/bank-reconciliation-copilot-window.png) 

Het Copilot-venster bestaat uit twee secties. Het bovenste gedeelte biedt enkele algemene details over het resultaat, zoals beschreven in de volgende tabel.  In het onderste gedeelte **Afgestemd voorstel** worden de door Copilot voorgestelde afstemmingen vermeld.

|Veld|Omschrijving|
|-|-|
|Automatisch afgestemd|Specificeert hoeveel regels in het bankafschrift zijn afgestemd door de automatische afstemming. Selecteer de waarde om de reconciliatiekaart te bekijken.  |
|Copilot afgestemd|Specificeert hoeveel regels in het bankafschrift door Copilot voorgestelde afstemmingen hebben. U kunt details van de afstemmingen bekijken in het gedeelte **Voorgestelde afstemmingen**.|
|Eindsaldo van afschrift|Hiermee wordt het eindsaldo opgegeven op het bankafschrift waarmee u reconcilieert|
|Boeken indien volledig vereffend|Zet deze schakelaar aan als u de bankrekeningreconciliatie automatisch wilt boeken wanneer alle regels (100%) zijn afgestemd en u **Behouden** hebt geselecteerd.|

#### Voorgestelde afstemmingen opslaan of negeren

Bekijk in het gedeelte **Afgestemde voorstellen** de voorgestelde afstemmingen regel voor regel en onderneem vervolgens de juiste actie:

- Als u één voorgestelde afstemming wilt verwijderen, selecteert u deze in de lijst en selecteert u vervolgens de actie **Regel verwijderen**.

- Om alle voorgestelde overeenkomsten te verwijderen en het Copilot-venster te sluiten, selecteert u de knop voor weggooien (prullenbak) ![Toont het prullenbakpictogram voor het verwijderen van alle Copilot-voorstellen voor bankrekeningreconciliatie](media/copilot-delete-trash-can.png) naast de knop **Behouden** onder aan het venster.

- Als u de volledig afgestemde reconciliatie automatisch wilt boeken wanneer u deze opslaat, zet u de schakelaar **Boeken indien volledig vereffend** aan.  
- Als u de afstemmingen die momenteel in het Copilot-venster worden weergegeven, wilt opslaan, selecteert u **Behouden**.


## Niet-afgestemde banktransacties overbrengen naar voorgestelde grootboekrekeningen

In deze sectie leert u hoe u Copilot kunt gebruiken om niet-gereconcilieerde bankrekeningafschriften over te brengen van het bankrekeninggrootboek naar een grootboekrekening. Deze taak kan alleen worden uitgevoerd vanuit een bestaande reconciliatie. 

1. Ga naar de lijst **Bankreconciliaties** en open de bestaande reconciliatie die de niet-gereconcilieerde regels bevat.

   Begin met het openen van een bestaande bankrekeningreconciliatie. Met deze stap krijgt u een duidelijk beeld van eventuele niet-gereconcilieerde bankafschriftregels die naar de grootboekrekening moeten worden overgebracht.

2. Identificeer in het deelvenster **Bankafschriftregels** het deelvenster met niet-afgestemde bankafschriftregels en selecteer een of meer regels die u wilt reconciliëren.

   Deze regels zijn de afschriftregels waarop Copilot zich richt voor de overdracht naar de grootboekrekening.

3. Selecteer **Overboeken naar grootboekrekening** om het proces te starten.

   ![Toont de actie Naar GB overboeken met Copilot op de bankreconciliatiekaart](media/bank-reconciliation-transfer-gl-copilot-card.svg) 

   Deze stap zorgt ervoor dat Copilot begint met het genereren van voorstellen voor de overdracht.

4. Zodra Copilot klaar is met het genereren van voorstellen, wordt het venster **Copilot-overboekingsvoorstellen voor grootboekrekening** geopend.

   In dit venster worden de voorstellen weergegeven in de sectie **Afgestemd voorstel**. De ervaring is vergelijkbaar met reconciliëren met Copilot.

   ![Toont de pagina Overboeken naar GB met door Copilot voorgestelde afstemmingen voor bankrekeningreconciliatie](media/bank-reconciliation-gl-transfer-proposed-matches.png) 

5. Controleer elk voorstelregel voor regel om de juistheid van de voorgestelde overdrachten te garanderen.

   - Als u dieper ingaat op het voorstel door het in de lijst te selecteren, wordt u naar een lijst met accounts geleid. Hier kunt u een ander account kiezen. Dit soort handmatige correctie is alleen mogelijk bij gebruik van de stroom **Overboeken naar grootboekrekening**, niet in de afstemmingsstroom. 
   - Als u **Opslaan...** selecteert naast een voorstel, kunt u de toewijzing toevoegen aan de pagina **Toewijzing tekst aan rekening**, zodat de volgende keer dat deze tekst verschijnt tijdens afstemming, het wordt toegewezen aan het voorgestelde account.

6. Negeer of bewaar voorstellen.

   - Als u een specifiek voorstel wilt negeren, selecteert u het in de lijst en selecteert u vervolgens de actie **Regel verwijderen**. Om alle voorstellen te verwijderen en Copilot te sluiten, selecteert u de knop voor weggooien (prullenbak) ![Toont het prullenbakpictogram voor het verwijderen van alle Copilot-voorstellen voor bankrekeningreconciliatie](media/copilot-delete-trash-can.png) naast de knop **Behouden** onder aan het venster.
   
   - Als de voorstellen aan uw wensen voldoen en u ze wilt opslaan, selecteert u **Behouden**. 

      Deze stap bevestigt de overdracht van de momenteel geselecteerde voorstellen vanuit het bankrekeninggrootboek naar de grootboekrekening. Het boekt nieuwe betalingen naar de voorgestelde grootboekrekeningen en past overeenkomstige regels toe op de resulterende bankrekeningposten.

## Volgende stappen

[Uw bankrekeningreconciliatie valideren](bank-how-reconcile-bank-accounts-separately.md#validate-your-bank-reconciliation)  

## Zie ook
[Problemen oplossen met Copilot- en AI-mogelijkheden](ai-copilot-troubleshooting.md)  
[Veelgestelde vragen over verantwoordelijke AI voor hulp bij bankreconciliatie](faqs-bank-reconciliation.md)  
[Bankieren instellen](bank-setup-banking.md)  
[Bankrekeningen reconciliëren](bank-how-reconcile-bank-accounts-separately.md)  
[Betalingen automatisch vereffenen en bankrekeningen reconciliëren](receivables-apply-payments-auto-reconcile-bank-accounts.md) 
