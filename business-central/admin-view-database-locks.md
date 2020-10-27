---
title: Databasevergrendelingen weergeven
description: Lees hoe u informatie over databasevergrendelingen rechtstreeks vanuit de clientinterface in Business Central kunt bekijken.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: 6880ffa9a2ab42c1af7c22f9cace64697c9f905b
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3922329"
---
# <a name="viewing-database-locks"></a><span data-ttu-id="8d31e-103">Databasevergrendelingen weergeven</span><span class="sxs-lookup"><span data-stu-id="8d31e-103">Viewing Database Locks</span></span>

<span data-ttu-id="8d31e-104">Databasevergrendeling bepaalt de toegang van meerdere gebruikers tot dezelfde gegevens tegelijkertijd.</span><span class="sxs-lookup"><span data-stu-id="8d31e-104">Database locking controls access by multiple users to the same data at the same time.</span></span> <span data-ttu-id="8d31e-105">Om een transactie te beschermen tegen andere transacties die dezelfde gegevens wijzigen, zet de eerste transactie de gegevens op slot.</span><span class="sxs-lookup"><span data-stu-id="8d31e-105">To protect a transaction against other transactions modifying the same data, the first transaction puts a lock on the data.</span></span> <span data-ttu-id="8d31e-106">Het slot blijft staan totdat de transactie is voltooid.</span><span class="sxs-lookup"><span data-stu-id="8d31e-106">The lock remains until the transaction's done.</span></span>

<span data-ttu-id="8d31e-107">Gebruikers kunnen worden geblokkeerd voor het voltooien van transacties op de vergrendelde gegevens.</span><span class="sxs-lookup"><span data-stu-id="8d31e-107">Users may be blocked from completing transactions on the locked data.</span></span> <span data-ttu-id="8d31e-108">Ze krijgen meestal een bericht dat de vergrendelingsconditie aangeeft.</span><span class="sxs-lookup"><span data-stu-id="8d31e-108">They'll typically get a message that indicates the lock condition.</span></span>

## <a name="to-view-database-locks"></a><span data-ttu-id="8d31e-109">Databasevergrendelingen weergeven</span><span class="sxs-lookup"><span data-stu-id="8d31e-109">To view database locks</span></span>

<span data-ttu-id="8d31e-110">Kies het pictogram ![Pagina of rapport zoeken](media/ui-search/search_small.png "Pictogram Pagina of rapport zoeken"), voer **Databasevergrendelingen** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="8d31e-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Database Locks** , and then choose the related link.</span></span>

<span data-ttu-id="8d31e-111">De pagina **Databasevergrendelingen** geeft een momentopname van alle huidige databasevergrendelingen.</span><span class="sxs-lookup"><span data-stu-id="8d31e-111">The **Database Locks** page gives snapshot of all current database locks.</span></span>

<span data-ttu-id="8d31e-112">Zie voor meer informatie over databasevergrendeling [Databasevergrendelingen bewaken](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) in de Help van Business Central Developer en IT Pro.</span><span class="sxs-lookup"><span data-stu-id="8d31e-112">For more information about database locking, see [Monitoring Database Locks](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) in the Business Central Developer and IT Pro help.</span></span>

## <a name="see-also"></a><span data-ttu-id="8d31e-113">Zie ook</span><span class="sxs-lookup"><span data-stu-id="8d31e-113">See Also</span></span>

[<span data-ttu-id="8d31e-114">Databasevergrendelingen bewaken</span><span class="sxs-lookup"><span data-stu-id="8d31e-114">Monitor Database Locks</span></span>](/dynamics365/business-central/dev-itpro/administration/monitor-database-locks) 
