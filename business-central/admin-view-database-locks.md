---
title: Databasevergrendelingen weergeven
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 1153ffc97d0f22c889ff23c5a27a8c0446b17018
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196404"
---
# <a name="viewing-database-locks"></a><span data-ttu-id="bafdc-102">Databasevergrendelingen weergeven</span><span class="sxs-lookup"><span data-stu-id="bafdc-102">Viewing Database Locks</span></span>

## <a name="about-locks"></a><span data-ttu-id="bafdc-103">Over vergrendelingen</span><span class="sxs-lookup"><span data-stu-id="bafdc-103">About Locks</span></span>

<span data-ttu-id="bafdc-104">Databasevergrendeling bepaalt de toegang van meerdere gebruikers tot dezelfde gegevens tegelijkertijd.</span><span class="sxs-lookup"><span data-stu-id="bafdc-104">Database locking controls access by multiple users to the same data at the same time.</span></span> <span data-ttu-id="bafdc-105">Om een transactie te beschermen tegen andere transacties die dezelfde gegevens wijzigen, zet de eerste transactie de gegevens op slot.</span><span class="sxs-lookup"><span data-stu-id="bafdc-105">To protect a transaction against other transactions modifying the same data, the first transaction puts a lock on the data.</span></span> <span data-ttu-id="bafdc-106">Het slot blijft staan totdat de transactie is voltooid.</span><span class="sxs-lookup"><span data-stu-id="bafdc-106">The lock remains until the transaction's done.</span></span>

<span data-ttu-id="bafdc-107">Gebruikers kunnen worden geblokkeerd voor het voltooien van transacties op de vergrendelde gegevens.</span><span class="sxs-lookup"><span data-stu-id="bafdc-107">Users may be blocked from completing transactions on the locked data.</span></span> <span data-ttu-id="bafdc-108">Ze krijgen meestal een bericht dat de vergrendelingsconditie aangeeft.</span><span class="sxs-lookup"><span data-stu-id="bafdc-108">They'll typically get a message that indicates the lock condition.</span></span>

## <a name="to-view-database-locks"></a><span data-ttu-id="bafdc-109">Databasevergrendelingen weergeven</span><span class="sxs-lookup"><span data-stu-id="bafdc-109">To view database locks</span></span>

<span data-ttu-id="bafdc-110">Kies het pictogram ![Pagina of rapport zoeken](media/ui-search/search_small.png "Pictogram Pagina of rapport zoeken"), voer **Databasevergrendelingen** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="bafdc-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Database Locks**, and then choose the related link.</span></span>

<span data-ttu-id="bafdc-111">De pagina **Databasevergrendelingen** geeft een momentopname van alle huidige databasevergrendelingen.</span><span class="sxs-lookup"><span data-stu-id="bafdc-111">The **Database Locks** page gives snapshot of all current database locks.</span></span>

<span data-ttu-id="bafdc-112">Zie voor meer informatie over databasevergrendeling [Databasevergrendelingen bewaken](/dynamics365/business-central/a/dev-itpro/administration/monitor-database-locks) in de Help van Business Central Developer en IT Pro.</span><span class="sxs-lookup"><span data-stu-id="bafdc-112">For more information about database locking, see [Monitoring Database Locks](/dynamics365/business-central/a/dev-itpro/administration/monitor-database-locks) in the Business Central Developer and IT Pro help.</span></span>

## <a name="see-also"></a><span data-ttu-id="bafdc-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="bafdc-113">See Also</span></span>

[<span data-ttu-id="bafdc-114">Databasevergrendelingen bewaken</span><span class="sxs-lookup"><span data-stu-id="bafdc-114">Monitor Database Locks</span></span>](/dynamics365/business-central/a/dev-itpro/administration/monitor-database-locks) 
