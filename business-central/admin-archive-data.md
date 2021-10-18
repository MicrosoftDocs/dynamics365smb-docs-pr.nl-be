---
title: De extensie Gegevensarchief
description: Door gegevens te archiveren maakt u een goedkope back-up van uw records.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/14/2021
ms.author: bholtorf
ms.openlocfilehash: 032c425f10bae29416cf8602d0c339f3ffaa3043
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2021
ms.locfileid: "7589646"
---
# <a name="the-data-archive-extension"></a>De extensie Gegevensarchief
Na verloop van tijd zal uw bedrijf een aanzienlijke hoeveelheid gegevens verzamelen en als beheerder is het waarschijnlijk een goed idee om een strategie te hebben voor het archiveren van gegevens. Het hebben van veel gegevens kan zaken vertragen. Het kan bijvoorbeeld iets langer duren om rapporten te genereren of zelfs records te vergrendelen. Bovendien kunnen grote hoeveelheden gegevens leiden tot hogere opslagkosten.

De extensie Gegevensarchief biedt een basisraamwerk voor het archiveren en back-uppen van gegevens als onderdeel van datumcompressie. Wanneer u datumcompressie gebruikt, worden gerelateerde items samengevoegd tot één item en worden de originelen verwijderd. Zie voor meer informatie [Gegevens comprimeren met datumcompressie](admin-manage-documents.md#compress-data-with-date-compression). Het kan echter waardevol zijn om die gegevens te bewaren, dus in plaats van ze te verwijderen, kunt u ze archiveren voor later gebruik.

## <a name="start-archiving-data"></a>Begin met het archiveren van gegevens
De extensie is vooraf geïnstalleerd en beschikbaar in het **Extensiebeheer**, dus u hoeft niets te doen om aan de slag te gaan. De extensie is ook beschikbaar op Microsoft AppSource. 

Uw gegevensarchieven staan vermeld op de pagina **Lijst gegevensarchief**. Elk archief kan gegevens uit meerdere tabellen bevatten en kan maximaal 10.000 records bevatten. Als een tabel meer dan 10.000 records bevat, wordt een tweede archief gemaakt voor de volgende 10.000 records, enzovoort. Als u bijvoorbeeld 10.100 grootboekposten archiveert, maakt Business Central één grootboekpostarchief voor de eerste 10.000 posten en vervolgens een tweede archief voor de resterende 100 posten. 

Nadat u gegevens hebt gearchiveerd, kunt u deze verkennen met Microsoft Excel of als een CSV-bestand.

* Als u de Excel-optie gebruikt, bevat de werkmap één werkblad voor elke gegevensarchieftabel.
* Als u de CSV-optie gebruikt, krijgt u een ZIP-bestand met één CSV-bestand voor elke gegevensarchieftabel.

> [!TIP]
> De Excel- en CSV-optie maken het gemakkelijker om een andere app of service te gebruiken om de gegevens naar een andere locatie te verplaatsen, zoals Azure Blob-opslag of een analysetool, zoals Microsoft Power BI.

De gegevensarchiefextensies worden door de volgende batchverwerkingen gebruikt voor datumcompressie.

|Batchverwerkingen  |
|---------|
|Datumcomp. Artikelbudgetposten     |
|Bankposten comprimeren     |
|Klantposten comprimeren     |
|VA-posten comprimeren     |
|Grootboekposten comprimeren     |
|Verzekeringsposten comprimeren     |
|Onderhoudsposten comprimeren     |
|Onderhoudsposten comprimeren     |
|Resourceposten comprimeren     |
|Btw-posten comprimeren     |
|Leverancierspost comprimeren     |
|Magazijnposten comprimeren     |
|Grootboekbudgetposten comprimeren     |

Om te beginnen met het archiveren van gegevens wanneer u een van de batchverwerkingen uitvoert, zet u de schakelaar **Verwijderde posten archiveren** aan.

## <a name="storage-considerations"></a>Overwegingen bij opslag
De gearchiveerde gegevens worden opgeslagen in de tabel **Tenantmedia**. Deze tabel wordt niet opgenomen wanneer de databasegrootte wordt berekend, volgens uw licentievoorwaarden. In plaats daarvan telt het als bestandsopslag. We raden u echter aan om oude archieven te exporteren naar bijvoorbeeld een CSV-bestand en vervolgens de oude archiefrecords te verwijderen.

## <a name="see-also"></a>Zie ook
[Opslag beheren door documenten te verwijderen of gegevens te comprimeren](admin-manage-documents.md)
