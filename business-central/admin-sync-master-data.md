---
title: Synchronisatie van hoofdgegevens beheren
description: Leer hoe u synchronisatie van hoofdgegevens beheert.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.service: dynamics-365-business-central
ms.topic: conceptual
ms.date: 01/25/2023
ms.custom: bap-template
ms.search.form: '7230, 7233, 5338, 7236, 672, 7234'
---
# Synchronisatie van hoofdgegevens beheren

Nadat u de synchronisatie van hoofdgegevens hebt ingesteld en voor de eerste keer hebt gesynchroniseerd, worden de records in de geselecteerde tabellen gekoppeld en wordt voor elke tabel een terugkerend taakwachtrij-item gemaakt. De items in de taakwachtrij synchroniseren automatisch gegevens in de dochterondernemingen wanneer iemand een wijziging aanbrengt in het bronbedrijf. Verder hoeft u niets te doen.

> [!NOTE]
> Standaard worden de taakwachtrij-items gepland om elke minuut te worden uitgevoerd en kunt u de planning niet wijzigen.

Soms gaat het echter mis en kunnen er situaties zijn die u moet beheren of onderzoeken. Als mensen bijvoorbeeld dezelfde record wijzigen in zowel het bronbedrijf als een dochteronderneming, mislukt de synchronisatie zodat u de juiste wijziging kunt opgeven. Of het bronbedrijf kan een extensie installeren die het schema wijzigt van een van de tabellen die u synchroniseert door een of twee velden toe te voegen. Als u de nieuwe velden in de dochterondernemingen wilt synchroniseren, moet u dezelfde extensies installeren en de tabelschema's in hun instellingen bijwerken.

Dit artikel beschrijft de hulpprogramma's die u kunt gebruiken om de synchronisatie soepel te laten verlopen.

## De status van synchronisatie onderzoeken

Er zijn twee acties op de pagina **Synchronisatietabellen** die u kunnen helpen uw synchronisatie te controleren:

* **Synchronisatietaken voor integratie**
* **Taakwachtrijposten**

De volgende tabel beschrijft de acties.

|Pagina  |Omschrijving  |
|---------|---------|
|**Synchronisatietaken voor integratie**     | Open de pagina **Synchronisatietaken voor integratie** om te onderzoeken wat er gebeurde elke keer dat een taakwachtrij-item werd uitgevoerd. Om dieper in te gaan op de details over nieuwe records die zijn toegevoegd, of om te onderzoeken waarom een record niet kon worden gesynchroniseerd, kiest u de nummers in de kolommen **Ingevoegd** of **Mislukt**. U kunt deze pagina ook gebruiken om oudere records op te schonen die u mogelijk niet meer nodig hebt. Ga voor meer informatie over het opschonen naar [Oude posten opschonen](#clean-up-old-entries).        |
|**Taakwachtrijposten**     | Krijg toegang tot details over het taakwachtrij-item waarmee gegevens voor een geselecteerde tabel worden gesynchroniseerd. Gebruik deze pagina bijvoorbeeld om de status van het taakwachtrij-item te beheren. Ga voor meer informatie over taakwachtrij-items naar [Taakwachtrijen gebruiken om taken te plannen](admin-job-queues-schedule-tasks.md).     |

> [!NOTE]
> Als u een fout vindt op de pagina **Synchronisatietaken voor integratie** die u niet zelf kunt oplossen, en als u contact opneemt met uw partner of Microsoft voor ondersteuning, is het handig om de foutmelding en de callstack-informatie te vermelden.

## Gewijzigde records synchroniseren

Als u een instelling voor een tabel of veld in een dochteronderneming wijzigt, moet u de synchronisatie bijwerken. Als u bijvoorbeeld besluit om het selectievakje **Lokale wijziging overschrijven** in een veld in te schakelen, zodat gegevens van het bronbedrijf lokale wijzigingen kunnen overschrijven. Gebruik de actie **Gewijzigde records synchroniseren** op de pagina **Synchronisatietabellen** om de synchronisatie bij te werken.

## Tabelschema's bijwerken

Als het bronbedrijf een tabel wijzigt, bijvoorbeeld door een veld toe te voegen dat u wilt synchroniseren, moeten dochterondernemingen hun veldtoewijzingen bijwerken. Gebruik op de pagina **Synchronisatievelden** de actie **Velden bijwerken**. 

## Koppelingen tussen records in- of uitschakelen

Om het koppelen van specifieke records in een tabel te starten of te stoppen kiest u op de pagina **Synchronisatievelden** de velden en gebruikt u vervolgens de actie **Inschakelen** of **Uitschakelen**. 

> [!TIP]
> Een snelle manier om meerdere velden tegelijkertijd in of uit te schakelen, is door ze in de lijst te selecteren en vervolgens de actie **Inschakelen** of **Uitschakelen** te gebruiken.

## Extensies toevoegen

Als het bronbedrijf een nieuwe extensie installeert, moet de dochteronderneming deze ook installeren als ze er gegevens voor willen synchroniseren. De dochteronderneming kan de actie **Velden bijwerken** op de pagina **Synchronisatievelden** gebruiken om de tabellen van de extensie toe te voegen aan de lijst.

> [!NOTE]
> Sommige tabellen halen gegevens uit gerelateerde tabellen. Als u een extensie toevoegt die geen gerelateerde tabellen bevat, zijn de velden in die tabellen niet beschikbaar. Controleer of u alle gerelateerde tabellen hebt toegevoegd.

## Oude posten opruimen

Na verloop van tijd zal het aantal vermeldingen in het synchronisatielogboek groot worden, dus misschien wilt u een beetje opruimen om onnodige posten te verwijderen. Om het opschonen van oude posten gemakkelijker te maken biedt de pagina **Synchronisatietaken voor integratie** de volgende acties:

* **Posten ouder dan 7 dagen verwijderen**
* **Alle posten verwijderen**

<!--
## Recreate a deleted job queue entry

If the recurring job queue entry is deleted for a table, you can quickly recreate it. On the **Synchronization Tables** page, choose the **Use Default Synchronization Setup** action.
-->

## Zie ook

[Voorbereiden om hoofdgegevens te synchroniseren](admin-set-up-data-sync.md)
