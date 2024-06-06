---
title: Herwaarderingen van artikelkosten traceren
description: Meer informatie over hoe het bijhouden van artikelkostenherwaarderingen u kan helpen uw artikelkostengegevens accuraat te houden.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.search.keywords: null
ms.search.form: null
ms.date: 03/08/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="track-item-cost-adjustments"></a>Herwaarderingen van artikelkosten traceren

Het is belangrijk om de artikelkosten accuraat te houden en de tijd te verkorten tussen het moment waarop u een post boekt en het moment waarop het grootboek de kosten weergeeft. U kunt de prestaties van de kostenherwaarderingen voor individuele herwaarderingen en artikelen volgen. Als er fouten optreden, kunt u de problematische artikelen identificeren en correcties aanbrengen. U kunt de artikelen bijvoorbeeld uitsluiten van berekeningen om ervoor te zorgen dat herwaarderingen niet worden onderbroken voor andere artikelen. U kunt de kosten voor afzonderlijke artikelen aanpassen, of batches van artikelen aanmaken en deze allemaal tegelijk aanpassen.

## <a name="start-tracking-cost-adjustments"></a>Beginnen met het bijhouden van kostenherwaarderingen

Het is gemakkelijk om aan de slag te gaan. Op de pagina **Voorraad instellen** bevat het veld **Logboekregistratie van kostenherwaardering** een aantal opties:

* **Uitgeschakeld** betekent dat u geen kostenherwaardering registreert.
* **Alleen fouten** betekent dat alleen kostenherwaarderingen worden geregistreerd die zijn mislukt.
* **Alle** betekent dat alle kostenherwaarderingen worden geregistreerd.

> [!NOTE]
> Om de grootte van het logboek te minimaliseren, worden in [!INCLUDE [prod_short](includes/prod_short.md)] niet de herwaarderingen geregistreerd die automatisch plaatsvinden wanneer iemand een artikel boekt.

U moet ook de taakwachtrijpost **Voorraadkosten boeken naar grootboek (1002)** instellen. Met deze taakwachtrijpost worden de kosten automatisch aangepast volgens een schema. Ga voor meer informatie over taakwachtrijposten naar [Taakwachtrijen gebruiken om taken te plannen](admin-job-queues-schedule-tasks.md).

## <a name="manage-cost-adjustments"></a>Kostenherwaarderingen beheren

Gebruik de pagina **Herwaardering van voorraadkosten** om het kostenherwaarderingsproces te beheren en te controleren. Op deze pagina worden de artikelen weergegeven, samen met hun kostprijsparameters en de status van de kostenherwaardering. U kunt de lijst filteren om te focussen op artikelen die moeten worden aangepast of die zijn uitgesloten van het kostenherwaarderingsproces.

### <a name="about-item-batches"></a>Over artikelbatches

U kunt voor meerdere artikelen een kostenherwaardering uitvoeren door ze in batches te groeperen. Door batches is het eenvoudig om sommige artikelen afzonderlijk aan te passen, omdat de herwaardering ervan bijvoorbeeld langer duurt. Batches kunnen ook helpen bij het identificeren van artikelen met problemen.

Als u een batch wilt maken, voert u op de pagina **Herwaardering van voorraadkosten** een van de volgende handelingen uit:

* Selecteer de artikelen in de lijst, kies **Kostenherwaardering uitvoeren** en kies vervolgens **Batch toevoegen**.
* Als u een batch wilt maken en de kostenherwaardering onmiddellijk wilt uitvoeren, selecteert u de artikelen in de lijst en kiest u **Kostenherwaardering uitvoeren** en vervolgens **Batch toevoegen en uitvoeren**.
* Kies **Kostenherwaardering uitvoeren**, kies **Artikelbatches** en voer vervolgens een filter in het veld **Artikelfilter** in.
  
> [!TIP]
> Als u snel een nieuwe batch wilt maken voor alle artikelen die nog niet in een batch zijn opgenomen, kiest u op de pagina **Kostenherwaardering - artikelbatches** **Ontbrekende artikelen toevoegen**.

Wanneer een herwaardering voor een batch wordt voltooid, heeft de batch een van de volgende statuswaarden op de pagina **Artikelbatches**:

* **Geslaagd**: de kostenherwaardering is gelukt.
* **Mislukt**: als de kostenherwaardering mislukt, identificeert [!INCLUDE [prod_short](includes/prod_short.md)] het artikel dat de fout heeft veroorzaakt en splitst vervolgens de huidige batch in tweeën op. Eén batch met het problematische artikel en een andere met de overige artikelen. Nieuwe uitvoeringen van kostenherwaardering voor de batch met de resterende artikelen. Als het opnieuw mislukt, herhaalt het proces zich. U definieert het maximale aantal splitsingen in het veld **Maximum aantal pogingen**. De standaardwaarde voor nieuwe pogingen is 10, maar u kunt een nieuwe limiet invoeren.
* **Time-out**: als de kostenherwaardering voor een batch niet wordt voltooid binnen de periode die is opgegeven in het veld **Time-out (minuten)** (variërend van 1 tot 720 minuten), wordt de sessie beëindigd en worden de wijzigingen teruggedraaid. [!INCLUDE [prod_short](includes/prod_short.md)] splitst vervolgens de huidige batch in tweeën op en voert het kostenherwaarderingsproces voor elke helft opnieuw uit. Dit proces gaat door totdat de kostenherwaardering succesvol is of het maximale aantal nieuwe pogingen is bereikt.

> [TIP!] Elke batch wordt in een aparte sessie uitgevoerd. Gebruik de actie **Vernieuwen** om de voortgang te volgen.

### <a name="run-cost-adjustment"></a>Kostenherwaardering uitvoeren

Gebruik de pagina **Herwaardering van voorraadkosten** om herwaarderingen door te voeren.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Herwaardering van voorraadkosten** in en kies vervolgens de gerelateerde koppeling.
1. Afhankelijk van wat u wilt doen, gebruikt u een van de volgende opties:

  * Voor een of meer artikelen selecteert u onmiddellijk de artikelen in de lijst en kiest u vervolgens **Kostenherwaardering uitvoeren**.
  * Voor batches gebruikt u een van de volgende opties:

    * Als u een batch wilt maken en de kostenherwaardering onmiddellijk wilt uitvoeren, kiest u de artikelen in de lijst en kiest u **Kostenherwaardering uitvoeren** en vervolgens **Batch toevoegen en uitvoeren**.
    * Als u dit voor alle batches wilt uitvoeren, kiest u **Kostenherwaardering uitvoeren**, **Artikelbatches** en vervolgens **Uitvoeren**.
    
    Ga voor meer informatie over batches naar [Over artikelbatches](#about-item-batches).

### <a name="explore-item-details"></a>Artikeldetails verkennen

Gebruik het menu **Artikel** voor toegang tot informatie over kostenherwaarderingen voor een geselecteerd artikel.

* **Artikelposten**: geef artikelposten voor het artikel weer. Met de actie **Markeren voor herwaardering** kunt u de nieuwe uitvoering van de kostenherwaardering afdwingen voor artikelen die direct of indirect zijn gekoppeld aan de inkomende posten die u selecteert. Het forceren van een nieuwe uitvoering kan nuttig zijn als eerdere uitvoeringen tot onjuiste kosten hebben geleid.
* **Waardeposten**: geef waardeposten voor het artikel weer.
* **Startpunten van kostenherwaardering**: open de pagina **Startpunt gemiddelde kostenherwaardering** die u voornamelijk gebruikt om de gemiddelde kosten te berekenen. Op de pagina worden combinaties van artikelen, locaties, varianten en waarderingsdatums weergegeven waarvoor kostenherwaarderingen worden of moeten worden uitgevoerd.
* **Kostenherwaarderingsorders**: open de pagina **Voorraadherwaarderingspost (order)**, waar u productie- en assemblageorders aanpast. Het laat zien dat de orders zijn aangepast of aanpassing behoeven.

### <a name="view-the-outcome"></a>Het resultaat weergeven

Gebruik het menu **Logboek per** om het resultaat van kostenherwaarderingen weer te geven:

* **Uitvoeren**: geef logboeken van kostenwaarderingen voor elke uitvoering weer. Het logboek bevat gegevens over het artikelfilter, de status (Geslaagd/Mislukt/Time-out), begin- en einddatum/-tijd, duur en de kostenverschillen die door de uitvoering worden veroorzaakt.
* **Artikel**: geef gedetailleerde informatie weer over het herwaarderingsproces voor het geselecteerde artikel.

### <a name="include-or-exclude-items-from-adjustments"></a>Artikelen opnemen in of uitsluiten van herwaarderingen

Als een of meer artikelen mislukken, kunt u de artikelen uitsluiten van de herwaarderingsuitvoering en ze vervolgens opnemen in latere uitvoeringen. Kies een van de volgende mogelijkheden in het menu **Functies**.

* **Artikel van herwaardering uitsluiten** en **Artikel opnemen in herwaardering**: schakel kostenherwaardering tijdelijk uit en weer in voor een geselecteerd artikel. Met kostenherwaardering blijven de kosten voor andere artikelen accuraat terwijl u een probleem met een specifiek artikel onderzoekt.

## <a name="post-adjusted-costs-to-the-general-ledger"></a>Geherwaardeerde kosten naar het grootboek boeken

Doorgaans worden nieuwe waardeposten naar het grootboek geboekt volgens het schema voor de taakwachtrijpost **Voorraadkosten boeken naar grootboek (1002)** . U kunt herwaarderingen echter onmiddellijk in het grootboek boeken vanaf de pagina **Herwaardering van voorraadkosten**. Kies in het menu **Functies** **Voorraadkosten boeken naar grootboek**.

## <a name="troubleshoot-cost-adjustments"></a>Problemen met kostenherwaarderingen oplossen

Gebruik de volgende opties in het menu **Diagnose** om problemen met kostenherwaarderingen op te lossen.

* **Artikelgegevens exporteren**: exporteer artikelgerelateerde gegevens naar een tekstbestand. U kunt het bestand gebruiken voor verdere analyse in een sandbox-omgeving of het toevoegen aan een ondersteuningsverzoek bij het onderzoeken van problemen met de kostenberekening.
* **Artikelgegevens importeren**: importeer het eerder geëxporteerde tekstbestand weer in de database. Deze actie wordt alleen ingeschakeld in sandbox-omgevingen of evaluatiebedrijven.
* **Kostprijs geherwaardeerd opnieuw instellen**: stel de schakeloptie **Kostprijs geherwaardeerd** opnieuw in voor artikelen, productieorders of assemblageorders. Met deze instelling kunt u het opnieuw uitvoeren van de kostenherwaardering ervoor forceren.
* **Rapport Waarderingsproblemen detecteren**: stel een diagnose voor typische gegevensproblemen waarmee berekeningsfouten bij de kostenberekening worden veroorzaakt. Er wordt gecontroleerd of de artikelposten, waardeposten, artikelvereffeningsposten en capaciteitsposten correct zijn.
* **Artikelgegevens verwijderen**: wis alle artikelgerelateerde tabellen in de database. Deze actie is alleen beschikbaar in sandbox-omgevingen of evaluatiebedrijven.

## <a name="see-also"></a>Zie ook

[Artikelprijzen herwaarderen](inventory-how-adjust-item-costs.md)  
[Ontwerpdetails: Kostenwaardering](design-details-cost-adjustment.md)  
