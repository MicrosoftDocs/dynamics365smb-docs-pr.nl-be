---
title: Gebruikersactiviteit bijhouden in een wijzigingslogbestand| Microsoft Docs
description: U kunt een gebruikerslogboek activeren zodat u een historie hebt van eventuele wijzigingen in gegevens in getraceerde tabellen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 11/14/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 3f158d7ed56445d6d2acf2ef8e5e9ab8e7487531
ms.openlocfilehash: bd0751ad5a4c0c7d9c3f7d5621bb7e6a62c3be2a
ms.contentlocale: nl-be
ms.lasthandoff: 12/04/2018

---
# <a name="logging-changes-in-business-central"></a><span data-ttu-id="63378-103">Wijzigingen registreren in Business Central</span><span class="sxs-lookup"><span data-stu-id="63378-103">Logging Changes in Business Central</span></span>

<span data-ttu-id="63378-104">U kunt het wijzigingslogbestand in [!INCLUDE[d365fin](includes/d365fin_md.md)] inschakelen, zodat u een overzicht van activiteiten hebt.</span><span class="sxs-lookup"><span data-stu-id="63378-104">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="63378-105">Het logboek is gebaseerd op wijzigingen die worden aangebracht in gegevens in de tabellen die u bijhoudt. Op de pagina **Wijzigingslogposten** worden posten chronologisch geordend en worden wijzigingen weergeven die worden aangebracht in de velden in de opgegeven tabellen.</span><span class="sxs-lookup"><span data-stu-id="63378-105">The log is based on changes that are made to data in the tables that you track. On the **Change Log Entries** page, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="63378-106">In het wijzigingslogbestand verzamelt alle wijzigingen die in de tabel worden aangebracht.</span><span class="sxs-lookup"><span data-stu-id="63378-106">The change log collects all changes that are made to the table.</span></span>

> [!Important]
> <span data-ttu-id="63378-107">Wijzigingen van een gebruiker zijn pas zichtbaar in de **Wijzigingslogposten** als de sessie van de gebruiker opnieuw wordt gestart, wat in de volgende gevallen gebeurt:</span><span class="sxs-lookup"><span data-stu-id="63378-107">A user's changes are not visible in the **Change Log Entries** until the user's session is restarted, which happens in the following cases:</span></span>
<br />
> * <span data-ttu-id="63378-108">De sessie is verlopen en vernieuwd.</span><span class="sxs-lookup"><span data-stu-id="63378-108">The session expired and was refreshed.</span></span>
> * <span data-ttu-id="63378-109">De gebruiker heeft een ander bedrijf of rolcentrum geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="63378-109">The user selected another company or Role Center.</span></span>
> * <span data-ttu-id="63378-110">De gebruiker heeft zich af- en weer aangemeld.</span><span class="sxs-lookup"><span data-stu-id="63378-110">The user signed out and back in.</span></span>

## <a name="working-with-the-change-log"></a><span data-ttu-id="63378-111">Werken met het wijzigingslogbestand</span><span class="sxs-lookup"><span data-stu-id="63378-111">Working with the Change Log</span></span>

<span data-ttu-id="63378-112">Een vaak voorkomend probleem in veel financiële systemen is het lokaliseren van de oorzaak van fouten en wijzigingen in gegevens.</span><span class="sxs-lookup"><span data-stu-id="63378-112">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="63378-113">Het probleem kan variëren van een foutief telefoonnummer van een klant tot een foutieve boeking naar het grootboek.</span><span class="sxs-lookup"><span data-stu-id="63378-113">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="63378-114">Met het wijzigingslogbestand kunt u alle directe wijzigingen bijhouden die een gebruiker aanbrengt in de databasegegevens.</span><span class="sxs-lookup"><span data-stu-id="63378-114">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="63378-115">U moet elke tabel en elk veld opgeven dat u door het systeem wilt laten registreren. Vervolgens moet u het wijzigingslogbestand instellen.</span><span class="sxs-lookup"><span data-stu-id="63378-115">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="63378-116">U activeert en deactiveert het wijzigingslogbestand op de pagina **Wijzigingslogbestandinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="63378-116">You activate and deactivate the change log on the **Change Log Setup** page.</span></span> <span data-ttu-id="63378-117">Wanneer een gebruiker het wijzigingslogbestand activeert of deactiveert, wordt deze activiteit geregistreerd, zodat u altijd kunt zien welke gebruiker het wijzigingslogbestand heeft gedeactiveerd of opnieuw heeft geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="63378-117">When a user activates or deactivates the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span>

<span data-ttu-id="63378-118">Op de pagina **Wijzigingslogbestandinstellingen** kunt u als u de actie **Tabellen** kiest, opgeven voor welke tabellen u wijzigingen wilt bijhouden en welke wijzigingen moeten worden bijgehouden. [!INCLUDE[d365fin](includes/d365fin_md.md)] houdt ook een aantal systeemtabellen bij.</span><span class="sxs-lookup"><span data-stu-id="63378-118">On the **Change Log Setup** page, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="63378-119">Nadat u het wijzigingslogbestand hebt ingesteld, hebt geactiveerd en gegevens hebt gewijzigd, kunt u de wijzigingen weergeven en filteren op de pagina **Wijzigingslogposten**.</span><span class="sxs-lookup"><span data-stu-id="63378-119">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes on the **Change Log Entries** page.</span></span> <span data-ttu-id="63378-120">Als u posten wilt verwijderen, kunt u dat doen op de pagina **Wijzigingslogposten verwijderen**, waar u filters kunt instellen op basis van datums en tijd.</span><span class="sxs-lookup"><span data-stu-id="63378-120">If you want to delete entries, you can do that on the **Delete Change Log Entries** page, where you can set filters based on dates and time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="63378-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="63378-121">See Also</span></span>
[<span data-ttu-id="63378-122">Basisinstellingen wijzigen</span><span class="sxs-lookup"><span data-stu-id="63378-122">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="63378-123">Sorteervolgorde</span><span class="sxs-lookup"><span data-stu-id="63378-123">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="63378-124">Zoeken naar pagina of rapport gebruiken</span><span class="sxs-lookup"><span data-stu-id="63378-124">Using Search for Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="63378-125">[Gebruikers en machtigingen beheren](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="63378-125">[Managing Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="63378-126">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="63378-126">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

