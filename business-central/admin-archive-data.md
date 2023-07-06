---
title: De extensie Gegevensarchief
description: Door gegevens te archiveren maakt u een goedkope back-up van uw records.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bknudsen
ms.topic: conceptual
ms.date: 01/30/2023
ms.custom: bap-template
ms.search.form: 630
---

# <a name="the-data-archive-extension"></a><a name="the-data-archive-extension"></a><a name="the-data-archive-extension"></a>De extensie Gegevensarchief

Na verloop van tijd zal uw bedrijf een aanzienlijke hoeveelheid gegevens verzamelen en als beheerder is het waarschijnlijk een goed idee om een strategie te hebben voor het archiveren van gegevens. Het hebben van veel gegevens kan zaken vertragen. Het kan bijvoorbeeld iets langer duren om rapporten te genereren of zelfs records te vergrendelen. Bovendien kunnen grote hoeveelheden gegevens leiden tot hogere opslagkosten.

De extensie Gegevensarchief biedt een basisraamwerk voor het archiveren en back-uppen van gegevens als onderdeel van datumcompressie. Datumcompressie consolideert gerelateerde posten tot één artikel en verwijdert de originelen. Ga voor meer informatie naar [Gegevens comprimeren met datumcompressie](admin-manage-documents.md#compress-data-with-date-compression). Het kan echter waardevol zijn om die gegevens te bewaren, dus in plaats van ze te verwijderen, kunt u ze archiveren voor later gebruik.

## <a name="start-archiving-data"></a><a name="start-archiving-data"></a><a name="start-archiving-data"></a>Begin met het archiveren van gegevens

De extensie is vooraf geïnstalleerd en beschikbaar in het **Extensiebeheer**, dus u hoeft niets te doen om aan de slag te gaan. De extensie is ook beschikbaar op AppSource.

Uw gegevensarchieven staan vermeld op de pagina **Lijst gegevensarchief**. Elk archief kan gegevens uit meerdere tabellen bevatten en kan maximaal 10.000 records bevatten. Als een tabel meer dan 10.000 records bevat, wordt een tweede archief gemaakt voor de volgende 10.000 records, enzovoort. Als u bijvoorbeeld 10.100 grootboekposten archiveert, maakt Business Central één grootboekpostarchief voor de eerste 10.000 posten en vervolgens een tweede archief voor de resterende 100 posten.

Nadat u gegevens hebt gearchiveerd, kunt u deze verkennen met Microsoft Excel of als een CSV-bestand.

* Als u de Excel-optie gebruikt, bevat de werkmap één werkblad voor elke gegevensarchieftabel.
* Als u de CSV-optie gebruikt, krijgt u een ZIP-bestand dat één CSV-bestand bevat voor elke gegevensarchieftabel.

> [!TIP]
> De Excel- en CSV-optie maken het gemakkelijker om een andere app of service te gebruiken om de gegevens naar een andere vestiging te verplaatsen, zoals Azure Blob-opslag of een analysetool, zoals Microsoft Power BI.

De gegevensarchiefextensie wordt door de volgende batchverwerkingen gebruikt voor datumcompressie.

|Batchverwerkingen  |
|---------|
|Datumcomp. Artikelbudgetposten |
|Bankposten comprimeren |
|Klantposten comprimeren |
|VA-posten comprimeren |
|Grootboekposten comprimeren |
|Verzekeringsposten comprimeren |
|Onderhoudsposten comprimeren |
|Onderhoudsposten comprimeren |
|Resourceposten comprimeren |
|Btw-posten comprimeren |
|Leverancierspost comprimeren |
|Magazijnposten comprimeren |
|Grootboekbudgetposten comprimeren |

Om te beginnen met het archiveren van gegevens wanneer u een van de batchverwerkingen uitvoert, zet u de schakelaar **Verwijderde posten archiveren** aan.

## <a name="storage-considerations"></a><a name="storage-considerations"></a><a name="storage-considerations"></a>Overwegingen bij opslag

De gearchiveerde gegevens worden opgeslagen in de tabel **Tenantmedia**. We raden u echter aan om oude archieven te exporteren naar bijvoorbeeld een CSV-bestand en vervolgens de oude archiefrecords te verwijderen.

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Zie ook

[Opslag beheren door documenten te verwijderen of gegevens te comprimeren](admin-manage-documents.md)
