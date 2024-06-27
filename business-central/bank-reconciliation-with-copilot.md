---
title: Bankrekeningen reconciliëren met Copilot (preview)
description: Meer informatie over hoe u Copilot gebruikt om bankrekeningen in Business Central te reconciliëren.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.collection:
  - get-started
  - bap-ai-copilot
ms.date: 06/13/2024
ms.custom: bap-template
---

# Bankrekeningen reconciliëren met Copilot (preview)

[!INCLUDE [preview-banner](~/../shared-content/shared/preview-includes/preview-banner.md)]

In dit artikel wordt uitgelegd hoe u hulp bij het afstemmen van bankrekeningen kunt gebruiken om banktransacties af te stemmen met grootboekposten in Microsoft Dynamics 365 Business Central.

[!INCLUDE [preview-note](~/../shared-content/shared/preview-includes/production-ready-preview-dynamics365.md)]

## Over hulp bij bankrekeningreconciliatie

Hulp bij bankrekeningreconciliatie is een reeks door AI aangedreven functies die u helpen bij het reconciliëren van bankrekeningen. Het biedt twee verschillende taken via Copilot:

- Verbeterde afstemming van transacties met grootboekposten

    U bent wellicht al vertrouwd met de actie **Automatisch afstemmen** op de pagina **Bankreconciliatie**, waarmee de meeste banktransacties automatisch worden afgestemd met grootboekposten. We noemen deze bewerking *automatisch afstemmen*. Hoewel automatisch afstemmen goed werkt, kunnen de algoritmen die het gebruikt, soms resulteren in veel niet-afgestemde transacties. Copilot gebruikt AI-technologie om deze niet-afgestemde transacties te inspecteren en meer overeenkomsten te identificeren, op basis van de datums, bedragen en beschrijvingen. Als een klant bijvoorbeeld meerdere facturen als één lump-sum heeft betaald, stemt Copilot de afzonderlijke bankafschriftregel af met de meerdere factuurposten.

    [Meer informatie over deze taak](#reconcile-bank-accounts-with-copilot).

- Voorgestelde grootboekrekeningen

    Voor resterende banktransacties die niet met grootboekposten kunnen worden afgestemd, vergelijkt Copilot de transactiebeschrijving met grootboekrekeningnamen, en worden vervolgens de meest waarschijnlijke grootboekrekening voorgesteld waarnaar moet worden geboekt. A;s niet-afgestemde transacties bijvoorbeeld vallen onder *Brandstofstop 24*, kan Copilot bijvoorbeeld voorstellen dat u ze boekt naar het account *Transport*.

    [Meer informatie over deze taak](#post-unmatched-bank-transaction-amounts-to-suggested-gl-accounts).

## Beschikbare talen

[!INCLUDE[bank-recon-assist-language-support](includes/bank-recon-assist-language-support.md)]

## Vereisten

- Hulp bij bankrekeningreconciliatie is geactiveerd. Deze taak moet worden uitgevoerd door een beheerder. [Meer informatie over het configureren van Copilot- en AI-mogelijkheden](enable-ai.md).
- De bankrekeningen in Business Central die u wilt reconciliëren, zijn gekoppeld aan een online bankrekening of zijn ingesteld met de importindeling voor bankafschriften.
- U bent bekend met bankrekeningreconciliatie in Business Central, zoals beschreven in [Bankrekeningen reconciliëren](bank-how-reconcile-bank-accounts-separately.md).

## Bankrekeningen reconciliëren met Copilot

<!-- Similar to the **Match Automatically** capability on the **Bank Acc. Reconciliation** page, Bank account reconciliation assist can also automatically matches transactions in banks statements with bank entries. The difference is that **Match Automatically** uses a native rules-based algorithm, while Bank account reconciliation assist is based AI technology though Copilot. Bank account reconciliation assist is intended to supplement the **Match Automatically** capability. While **Match Automatically** is fairly successful at matching transactions, there are some instances where it can't&mdash;which is where Bank account reconciliation assist comes. By using the **Reconcile with Copilot** action on **Bank Acc. Reconciliation** page, you can find even more matches.-->

Copilot bij bankrekeningreconciliatie is bedoeld om te worden gebruikt als aanvulling op automatisch afstemmen. Daarom wordt, wanneer u Copilot gebruikt, eerst de automatische afstemming uitgevoerd om de eerste afstemmingen te maken. Vervolgens wordt Copilot uitgevoerd om te proberen transacties af te stemmen die de automatische afstemming niet heeft verwerkt.

Er zijn twee benaderingen voor het reconciliëren van bankrekeningen met Copilot:

- Gebruik Copilot om een nieuwe reconciliatie op een bankrekening te starten, rechtstreeks vanuit de lijst **Bankreconciliatie**.
- Gebruik Copilot voor een nieuwe of bestaande reconciliatie op een kaart **Bankreconciliatie**.

# [Vanuit de lijst Bankreconciliatie](#tab/fromlist)

Met deze aanpak creëert en reconcilieert u een geheel nieuwe bankrekeningreconciliatie. Deze aanpak vereist dat u de bankrekening selecteert. Als de bankrekening niet is gekoppeld aan een online bankrekening, moet u ook het bankafschriftbestand importeren.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bankreconciliaties** in en selecteer vervolgens de gerelateerde koppeling.
1. Selecteer de actie **Reconciliëren met Copilot** om het venster **Reconciliëren met Copilot** te openen.
1. Stel het veld **Reconciliatie uitvoeren voor deze bankrekening** in op de bankrekening die u wilt reconciliëren.

    ![Schermopname met het venster Reconciliëren met Copilot, zodat u een nieuwe reconciliatie kunt uitvoeren.](media/reconcile-bank-accounts-new-copilot.svg)

1. Als de geselecteerde bankrekening niet is gekoppeld aan een online bankrekening, moet u het bankafschriftbestand importeren. Om het bestand te importeren selecteert u de waarde in het veld **Transactiegegevens gebruiken uit** of selecteert u de paperclipknop naast de knop **Genereren**. Gebruik dan **Selecteer het bestand om te importeren** om het bankafschriftbestand te importeren door het vanaf uw apparaat te slepen of door op uw apparaat te bladeren.
1. Selecteer om af te stemmen met Copilot **Genereren**.

    Copilot begint met het genereren van voorgestelde afstemmingen. Wanneer dit voltooid is, wordt het venster **Reconciliëren met Copilot** geopend met de resultaten van de afstemming.

1. Bekijk de voorgestelde afstemmingen zoals beschreven in de volgende sectie.

# [Vanaf een bankreconciliatiekaart](#tab/fromcard)

Met deze aanpak gebruikt u Copilot voor een nieuwe bankrekeningreconciliatie die u handmatig maakt, of door een bestaande afstemming te bewerken.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bankreconciliaties** in en selecteer vervolgens de gerelateerde koppeling.
1. Volg een van deze stappen:

    - Selecteer **Nieuw** om een nieuwe reconciliatie te starten.
    - Selecteer en open een bestaande reconciliatie in de lijst.

1. Selecteer op de kaart **Bankreconciliatie** **Reconciliëren met Copilot**.

    ![Schermopname met de knop Reconciliëren met Copilot op de bankreconciliatiekaart.](media/bank-reconciliation-copilot-card.svg)

    Copilot begint met het genereren van voorgestelde afstemmingen. Wanneer dit voltooid is, wordt het venster **Reconciliëren met Copilot** geopend met de resultaten van de afstemming.

1. Bekijk de voorgestelde afstemmingen zoals beschreven in de volgende sectie.
---

### Voorgestelde afstemmingen bekijken, opslaan of negeren

Nadat u Copilot hebt uitgevoerd, toont het venster **Reconciliëren met Copilot** de gedetailleerde resultaten, inclusief eventuele voorgestelde afstemmingen. Op dit moment is er geen afstemming opgeslagen die Copilot heeft voorgesteld. Daarom heeft u de mogelijkheid om de voorstellen te inspecteren en deze naar wens op te slaan of te verwijderen.

![Schermopname met het venster Reconciliëren met Copilot met voorgestelde afstemmingen](media/bank-reconciliation-copilot-window.png)

Het venster **Afstemmen met Copilot** is verdeeld in twee secties. In het bovenste gedeelte vindt u enkele algemene details over het resultaat. In het onderste gedeelte **Afstemmingsvoorstellen** worden de door Copilot voorgestelde afstemmingen vermeld.

In de volgende tabel worden de velden in het bovenste gedeelte beschreven.

| Veld | Omschrijving |
|---|---|
| Automatisch afgestemd | Het aantal bankafschriftregels waarmee de automatische bewerking overeenkwam. Selecteer de waarde om de reconciliatiekaart te bekijken. |
| Copilot afgestemd | Het aantal bankafschriftregels waarvoor Copilot afstemmingen heeft voorgesteld. U kunt details van de afstemmingen bekijken in het gedeelte **Afstemmingsvoorstellen**. |
| Eindsaldo van afschrift | Het eindsaldo dat wordt weergegeven opgegeven op het bankafschrift waarmee u reconcilieert. |
| Boeken indien volledig vereffend | Zet deze optie aan als u de bankrekeningreconciliatie automatisch wilt boeken wanneer alle regels (100%) zijn afgestemd en u **Behouden** hebt geselecteerd. |

In de sectie **Afstemmingsvoorstellen** bekijkt u de voorgestelde afstemmingen regel voor regel. Onderneem dan de juiste actie:

- Als u één voorgestelde afstemming wilt verwijderen, selecteert u deze in de lijst en selecteert u vervolgens de actie **Regel verwijderen**.
- Om alle voorgestelde regels te verwijderen en het venster **Afstemmen met Copilot** te sluiten, kiest u de ![knop Verwijderen (prullenbak).](media/copilot-delete-trash-can.png) naast de knop **Bewaar het** onder aan het venster.
- Als u de volledig afgestemde reconciliatie automatisch wilt boeken wanneer u deze opslaat, zet u de optie **Boeken indien volledig vereffend** aan.
- Als u de afstemmingen wilt opslaan die momenteel worden weergegeven in het venster **Afstemmen met Copilot**, selecteert u **Behouden**.

## Niet-afgestemde banktransactiebedragen boeken naar voorgestelde grootboekrekeningen

In deze sectie leert u hoe u Copilot kunt gebruiken om niet-gereconcilieerde regelbedragen van bankrekeningafschriften (opgegeven in het veld **Verschil**) te boeken naar een grootboekrekening. Deze taak kan alleen worden uitgevoerd vanuit een bestaande reconciliatie.

1. Ga naar de lijst **Bankreconciliaties** en open de bestaande reconciliatie die de niet-gereconcilieerde regels bevat.

    Met deze stap krijgt u een duidelijk beeld van eventuele niet-gereconcilieerde bankafschriftregels die naar de grootboekrekening moeten worden overgebracht.

1. Identificeer in het deelvenster **Bankafschriftregels** het deelvenster met niet-afgestemde bankafschriftregels en selecteer een of meer regels die u wilt reconciliëren.

    Copilot richt zich op de geselecteerde regels om nieuwe betalingen naar de grootboekrekening te boeken.

1. Selecteer **Verschil naar grootboekrekening boeken** om het proces te starten.

    ![Schermopname met de knop Verschil boeken naar grootboekrekening op de kaart Bankreconciliatie.](media/bank-reconciliation-transfer-gl-copilot-card.png)

    Copilot begint met het genereren van voorstellen voor het boeken van nieuwe betalingen.

1. Zodra Copilot klaar is met het genereren van voorstellen, wordt het venster **Copilot-voorstellen voor het boeken van verschillen naar grootboekrekeningen** geopend.

    In de sectie **Afstemmingsvoorstellen** van dit venster worden de voorstellen weergegeven. De ervaring lijkt op de ervaring voor het reconciliëren met Copilot.

    ![Schermopname met het venster Copilot-voorstellen voor het boeken van verschillen naar grootboekrekeningen.](media/bank-reconciliation-gl-transfer-proposed-matches.png)

1. Controleer elke voorstelregel om de juistheid van de voorgestelde te boeken betalingen te garanderen.

    - Als u dieper ingaat op het voorstel door het in de lijst te selecteren, wordt u naar een lijst met accounts geleid. Hier kunt u een ander account kiezen. U kunt dit soort handmatige correctie alleen uitvoeren als u de stroom **Verschil naar grootboekrekening boeken** gebruikt, niet de afstemmingsstroom.
    - Als u **Opslaan** naast een voorstel selecteert, kunt u de toewijzing toevoegen aan de pagina **Toewijzing tekst aan rekening**. De volgende keer dat deze tekst tijdens het afstemmen verschijnt, wordt deze toegewezen aan het voorgestelde account.

1. Negeer of bewaar voorstellen.

    - Als u een specifiek voorstel wilt negeren, selecteert u het in de lijst en selecteert u vervolgens de actie **Regel verwijderen**. Om alle voorstellen te verwijderen en Copilot te sluiten, selecteert u de knop ![Verwijderen.](media/copilot-delete-trash-can.png) naast de knop **Bewaar het** onder aan het venster.
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
