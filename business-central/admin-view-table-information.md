---
title: Tabelgegevens weergeven
description: Lees hoe u informatie over de databasetabellen rechtstreeks vanuit de clientinterface in Business Central kunt bekijken.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 72e220aa310515c665ce85bd43f4ebd3aac157d0
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922279"
---
# <a name="viewing-table-information"></a><span data-ttu-id="afd23-103">Tabelgegevens weergeven</span><span class="sxs-lookup"><span data-stu-id="afd23-103">Viewing Table Information</span></span>

<span data-ttu-id="afd23-104">De pagina **Gegevens van tabel 8700** biedt informatie over alle systeem- en bedrijfstabellen in een Business Central-oplossing.</span><span class="sxs-lookup"><span data-stu-id="afd23-104">The page **8700 Table Information** provides information about all system and business tables in a Business Central solution.</span></span> <span data-ttu-id="afd23-105">Op de pagina wordt met name informatie weergegeven over de hoeveelheid gegevens die de tabellen bevatten.</span><span class="sxs-lookup"><span data-stu-id="afd23-105">In particular, the page displays information about the amount of data the tables contain.</span></span>

<span data-ttu-id="afd23-106">Deze informatie is handig voor het oplossen van prestatieproblemen, omdat het u de verdeling van de gegevensgrootte over tabellen laat zien.</span><span class="sxs-lookup"><span data-stu-id="afd23-106">This information is useful for troubleshooting performance problems, because let's you see the distribution of data size across tables.</span></span>

## <a name="viewing-table-information"></a><span data-ttu-id="afd23-107">Tabelgegevens weergeven</span><span class="sxs-lookup"><span data-stu-id="afd23-107">Viewing table information</span></span>

<span data-ttu-id="afd23-108">Als u deze pagina wilt openen, selecteert u het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Pagina of rapport zoeken"), voert u **Tabelgegevens** in en kiest u vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="afd23-108">To open this page, select the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Table Information** , and then choose the related link.</span></span>

<span data-ttu-id="afd23-109">In de volgende tabel wordt de informatie voor elke tabel beschreven:</span><span class="sxs-lookup"><span data-stu-id="afd23-109">The following table describes the information provided for each table:</span></span>

|<span data-ttu-id="afd23-110">Kolom</span><span class="sxs-lookup"><span data-stu-id="afd23-110">Column</span></span>|<span data-ttu-id="afd23-111">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="afd23-111">Description</span></span>|
|------|-----------|
|<span data-ttu-id="afd23-112">Bedrijfsnaam</span><span class="sxs-lookup"><span data-stu-id="afd23-112">Company Name</span></span>|<span data-ttu-id="afd23-113">De naam van het bedrijf, als er een is, waartoe de tabel behoort.</span><span class="sxs-lookup"><span data-stu-id="afd23-113">The name of the company, if any, that the table belongs to.</span></span>|
|<span data-ttu-id="afd23-114">Tabelnaam</span><span class="sxs-lookup"><span data-stu-id="afd23-114">Table Name</span></span>|<span data-ttu-id="afd23-115">De naam van de tabel.</span><span class="sxs-lookup"><span data-stu-id="afd23-115">The name of the table.</span></span>|
|<span data-ttu-id="afd23-116">Tabelnr.</span><span class="sxs-lookup"><span data-stu-id="afd23-116">Table No.</span></span>|<span data-ttu-id="afd23-117">De id van de tabel</span><span class="sxs-lookup"><span data-stu-id="afd23-117">The ID of the table</span></span>|
|<span data-ttu-id="afd23-118">Nee.</span><span class="sxs-lookup"><span data-stu-id="afd23-118">No.</span></span> <span data-ttu-id="afd23-119">records</span><span class="sxs-lookup"><span data-stu-id="afd23-119">of Records</span></span>|<span data-ttu-id="afd23-120">Het totale aantal records dat is opgeslagen in de brontabel.</span><span class="sxs-lookup"><span data-stu-id="afd23-120">The total number of records stored in the table.</span></span>|
|<span data-ttu-id="afd23-121">Recordgrootte</span><span class="sxs-lookup"><span data-stu-id="afd23-121">Record Size</span></span>|<span data-ttu-id="afd23-122">De gemiddelde recordgrootte in KB/record.</span><span class="sxs-lookup"><span data-stu-id="afd23-122">The average record size in KB/record.</span></span> <span data-ttu-id="afd23-123">De waarde wordt berekend met de volgende formule: 1024 (grootte)/(aantal</span><span class="sxs-lookup"><span data-stu-id="afd23-123">The value is calculated using the following formula: 1024(Size)/(No.</span></span> <span data-ttu-id="afd23-124">records).</span><span class="sxs-lookup"><span data-stu-id="afd23-124">of Records)\`.</span></span> |

## <a name="see-also"></a><span data-ttu-id="afd23-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="afd23-125">See Also</span></span>

[<span data-ttu-id="afd23-126">Pagina's inspecteren</span><span class="sxs-lookup"><span data-stu-id="afd23-126">Inspecting Pages</span></span>](across-inspect-page.md)  
[<span data-ttu-id="afd23-127">Prestatieartikelen voor ontwikkelaars</span><span class="sxs-lookup"><span data-stu-id="afd23-127">Performance Articles For Developers</span></span>](/dynamics365/business-central/dev-itpro/performance/performance-developer)  
