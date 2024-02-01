---
title: Tabelinformatie weergeven
description: Lees hoe u informatie over de databasetabellen rechtstreeks vanuit Business Central kunt bekijken.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.form: 8700
ms.date: 10/11/2023
ms.author: jswymer
ms.service: dynamics-365-business-central
---

# Tabelgegevens weergeven

De pagina **8700 Tabelgegevens** geeft informatie over het aantal records in alle systeem- en bedrijfstabellen in [!INCLUDE[prod_short](includes/prod_short.md)], en hoeveel gegevens elke tabel bevat.

Deze informatie is handig voor het oplossen van prestatieproblemen, omdat het u de verdeling van de gegevensgrootte over tabellen laat zien.

## Tabelinformatie weergeven

Om deze pagina te openen, selecteert u het pictogram ![Pagina of rapport zoeken.](media/ui-search/search_small.png "Pictogram Pagina of rapport zoeken"), voert u **Tabelgegevens** in en kiest u vervolgens de gerelateerde koppeling.

In de volgende tabel wordt de informatie voor elke tabel beschreven:

|Kolom|Omschrijving|
|------|-----------|
|Bedrijfsnaam|De naam van het bedrijf, als er een is, waartoe de tabel behoort.|
|Tabelnaam|De naam van de tabel.|
|Tabelnr.|De id van de tabel.|
|Nr. records|Het totale aantal records dat is opgeslagen in de brontabel.|
|Recordgrootte|De gemiddelde recordgrootte in KB/record. De waarde wordt berekend met de volgende formule: 1024 (grootte)/(aantal records). |
|Bestandsgrootte (KB)|De totale hoeveelheid ruimte die de tabel inneemt in de database. Deze waarde is de som van de waarden in de velden Gegevensgrootte en Indexgrootte.|
|Gegevensgrootte (KB)|Hoeveel ruimte de gegevens in de tabel innemen in de database.|
|Indexgrootte (KB)|Hoeveel ruimte de tabelindexen (sleutels) innemen in de database.|
|Compressie|Het type compressie, **Rij**, **Pagina**, of **Geen**, dat wordt toegepast op de tabel in de database. Zie [Gegevenscompressie](/sql/relational-databases/data-compression/data-compression?) voor meer informatie.|

> [!NOTE]
> Als u gegevens in een tabel verwijdert, start [!INCLUDE[prod_short](includes/prod_short.md)] verschillende processen achter de schermen om ervoor te zorgen dat alles in uw database wordt opgeschoond. De waarden op de pagina Tabelgegevens worden niet bijgewerkt totdat deze processen zijn voltooid, wat enige tijd kan duren. Hoe lang u moet wachten kan variëren, afhankelijk van de grootte van uw database.

> [!IMPORTANT]  
> De pagina **Tabelgegevens** toont gegevens en indexgroottes, en de som van de tabelgroottes komt niet overeen met de totale gebruikte capaciteit, omdat deze de gegevensgrootte weergeeft, en niet de daadwerkelijk toegewezen grootte. Toegewezen ruimte is altijd groter dan gebruikte ruimte om te voorkomen dat bij elke invoeging ruimte moet worden toegewezen, wat de prestaties aanzienlijk zou beperken


## Zie ook

[Pagina's inspecteren](across-inspect-page.md)  
[Prestatieartikelen voor ontwikkelaars](/dynamics365/business-central/dev-itpro/performance/performance-developer)  


[!INCLUDE[footer-include](includes/footer-banner.md)]