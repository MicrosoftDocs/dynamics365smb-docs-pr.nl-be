---
title: Tabelgegevens weergeven
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/20/2020
ms.author: jswymer
ms.openlocfilehash: de93063a60e6b64405b1491a67489c8bfa4657ad
ms.sourcegitcommit: 99915b493a7e49d12c530f2f9fda1fcedb518b6e
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275330"
---
# <a name="viewing-table-information"></a><span data-ttu-id="4c38d-102">Tabelgegevens weergeven</span><span class="sxs-lookup"><span data-stu-id="4c38d-102">Viewing Table Information</span></span>

<span data-ttu-id="4c38d-103">De pagina **Gegevens van tabel 8700** biedt informatie over alle systeem- en bedrijfstabellen in een Business Central-oplossing.</span><span class="sxs-lookup"><span data-stu-id="4c38d-103">The page **8700 Table Information** provides information about all system and business tables in a Business Central solution.</span></span> <span data-ttu-id="4c38d-104">Op de pagina wordt met name informatie weergegeven over de hoeveelheid gegevens die de tabellen bevatten.</span><span class="sxs-lookup"><span data-stu-id="4c38d-104">In particular, the page displays information about the amount of data the tables contain.</span></span>

<span data-ttu-id="4c38d-105">Deze informatie is handig voor het oplossen van prestatieproblemen, omdat het u de verdeling van de gegevensgrootte over tabellen laat zien.</span><span class="sxs-lookup"><span data-stu-id="4c38d-105">This information is useful for troubleshooting performance problems, because let's you see the distribution of data size across tables.</span></span>

## <a name="viewing-table-information"></a><span data-ttu-id="4c38d-106">Tabelgegevens weergeven</span><span class="sxs-lookup"><span data-stu-id="4c38d-106">Viewing table information</span></span>

<span data-ttu-id="4c38d-107">Als u deze pagina wilt openen, selecteert u het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Pagina of rapport zoeken"), voert u **Tabelgegevens** in en kiest u vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="4c38d-107">To open this page, select the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Table Information**, and then choose the related link.</span></span>

<span data-ttu-id="4c38d-108">In de volgende tabel wordt de informatie voor elke tabel beschreven:</span><span class="sxs-lookup"><span data-stu-id="4c38d-108">The following table describes the information provided for each table:</span></span>

|<span data-ttu-id="4c38d-109">Kolom</span><span class="sxs-lookup"><span data-stu-id="4c38d-109">Column</span></span>|<span data-ttu-id="4c38d-110">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="4c38d-110">Description</span></span>|
|------|-----------|
|<span data-ttu-id="4c38d-111">Bedrijfsnaam</span><span class="sxs-lookup"><span data-stu-id="4c38d-111">Company Name</span></span>|<span data-ttu-id="4c38d-112">De naam van het bedrijf, als er een is, waartoe de tabel behoort.</span><span class="sxs-lookup"><span data-stu-id="4c38d-112">The name of the company, if any, that the table belongs to.</span></span>|
|<span data-ttu-id="4c38d-113">Tabelnaam</span><span class="sxs-lookup"><span data-stu-id="4c38d-113">Table Name</span></span>|<span data-ttu-id="4c38d-114">De naam van de tabel.</span><span class="sxs-lookup"><span data-stu-id="4c38d-114">The name of the table.</span></span>|
|<span data-ttu-id="4c38d-115">Tabelnr.</span><span class="sxs-lookup"><span data-stu-id="4c38d-115">Table No.</span></span>|<span data-ttu-id="4c38d-116">De id van de tabel</span><span class="sxs-lookup"><span data-stu-id="4c38d-116">The ID of the table</span></span>|
|<span data-ttu-id="4c38d-117">Nee.</span><span class="sxs-lookup"><span data-stu-id="4c38d-117">No.</span></span> <span data-ttu-id="4c38d-118">records</span><span class="sxs-lookup"><span data-stu-id="4c38d-118">of Records</span></span>|<span data-ttu-id="4c38d-119">Het totale aantal records dat is opgeslagen in de brontabel.</span><span class="sxs-lookup"><span data-stu-id="4c38d-119">The total number of records stored in the table.</span></span>|
|<span data-ttu-id="4c38d-120">Recordgrootte</span><span class="sxs-lookup"><span data-stu-id="4c38d-120">Record Size</span></span>|<span data-ttu-id="4c38d-121">De gemiddelde recordgrootte in KB/record.</span><span class="sxs-lookup"><span data-stu-id="4c38d-121">The average record size in KB/record.</span></span> <span data-ttu-id="4c38d-122">De waarde wordt berekend met de volgende formule: 1024 (grootte)/(aantal</span><span class="sxs-lookup"><span data-stu-id="4c38d-122">The value is calculated using the following formula: 1024(Size)/(No.</span></span> <span data-ttu-id="4c38d-123">records).</span><span class="sxs-lookup"><span data-stu-id="4c38d-123">of Records)\`.</span></span> |

## <a name="see-also"></a><span data-ttu-id="4c38d-124">Zie ook</span><span class="sxs-lookup"><span data-stu-id="4c38d-124">See Also</span></span>

[<span data-ttu-id="4c38d-125">Pagina's inspecteren</span><span class="sxs-lookup"><span data-stu-id="4c38d-125">Inspecting Pages</span></span>](across-inspect-page.md)  
[<span data-ttu-id="4c38d-126">Prestatieartikelen voor ontwikkelaars</span><span class="sxs-lookup"><span data-stu-id="4c38d-126">Performance Articles For Developers</span></span>](/dynamics365/business-central/dev-itpro/performance/performance-developer)  
