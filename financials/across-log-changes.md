---
title: Gebruikersactiviteit bijhouden in een wijzigingslogbestand| Microsoft Docs
Description: You can activate a user log so that you have a history of any changes made to data in tracked tables.
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 8f49e3722f95d4e5a2c8eea83d77175581d93277
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="logging-changes-in-finance-and-operations-business-edition"></a><span data-ttu-id="0251c-102">Wijzigingen registreren in Finance and Operations, Business edition</span><span class="sxs-lookup"><span data-stu-id="0251c-102">Logging Changes in Finance and Operations, Business edition</span></span> 
<span data-ttu-id="0251c-103">U kunt het wijzigingslogbestand in [!INCLUDE[d365fin](includes/d365fin_md.md)] inschakelen, zodat u een overzicht van activiteiten hebt.</span><span class="sxs-lookup"><span data-stu-id="0251c-103">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="0251c-104">Het logboek is gebaseerd op wijzigingen die worden aangebracht in gegevens in de tabellen die u bijhoudt. In het wijzigingslogbestand worden posten chronologisch geordend en worden wijzigingen weergeven die worden aangebracht in de velden in de opgegeven tabellen.</span><span class="sxs-lookup"><span data-stu-id="0251c-104">The log is based on changes that are made to data in the tables that you track. In the change log, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="0251c-105">In het wijzigingslogbestand verzamelt alle wijzigingen die in de tabel worden aangebracht.</span><span class="sxs-lookup"><span data-stu-id="0251c-105">The change log collects all changes that are made to the table.</span></span>  

## <a name="working-with-the-change-log"></a><span data-ttu-id="0251c-106">Werken met het wijzigingslogbestand</span><span class="sxs-lookup"><span data-stu-id="0251c-106">Working with the Change Log</span></span>
<span data-ttu-id="0251c-107">Een vaak voorkomend probleem in veel financiële systemen is het lokaliseren van de oorzaak van fouten en wijzigingen in gegevens.</span><span class="sxs-lookup"><span data-stu-id="0251c-107">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="0251c-108">Het probleem kan variëren van een foutief telefoonnummer van een klant tot een foutieve boeking naar het grootboek.</span><span class="sxs-lookup"><span data-stu-id="0251c-108">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="0251c-109">Met het wijzigingslogbestand kunt u alle directe wijzigingen bijhouden die een gebruiker aanbrengt in de databasegegevens.</span><span class="sxs-lookup"><span data-stu-id="0251c-109">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="0251c-110">U moet elke tabel en elk veld opgeven dat u door het systeem wilt laten registreren. Vervolgens moet u het wijzigingslogbestand instellen.</span><span class="sxs-lookup"><span data-stu-id="0251c-110">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="0251c-111">U activeert en deactiveert het wijzigingslogbestand in het venster **Wijzigingslogbestandinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="0251c-111">You activate and deactivate the change log in the **Change Log Setup** window.</span></span> <span data-ttu-id="0251c-112">Als u het wijzigingslogbestand activeert of deactiveert, wordt deze activiteit geregistreerd, zodat u altijd kunt zien welke gebruiker het wijzigingslogbestand heeft gedeactiveerd of opnieuw heeft geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="0251c-112">When you activate or deactivate the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span> <span data-ttu-id="0251c-113">Dit kan niet worden uitgeschakeld.</span><span class="sxs-lookup"><span data-stu-id="0251c-113">This cannot be turned off.</span></span>  

<span data-ttu-id="0251c-114">In het venster **Wijzigingslogbestandinstellingen** kunt u als u de actie **Tabellen** kiest, opgeven voor welke tabellen u wijzigingen wilt bijhouden en welke wijzigingen moeten worden bijgehouden. [!INCLUDE[d365fin](includes/d365fin_md.md)] houdt ook een aantal systeemtabellen bij.</span><span class="sxs-lookup"><span data-stu-id="0251c-114">In the **Change Log Setup** window, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="0251c-115">Nadat u het wijzigingslogbestand hebt ingesteld, hebt geactiveerd en gegevens hebt gewijzigd, kunt u de wijzigingen weergeven en filteren in het venster **Wijzigingslogposten**.</span><span class="sxs-lookup"><span data-stu-id="0251c-115">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes in the **Change Log Entries** window.</span></span> <span data-ttu-id="0251c-116">Als u posten wilt verwijderen, kunt u dat doen in het venster **Wijzigingslogposten verwijderen**, waar u filters kunt instellen op basis van datums en tijd.</span><span class="sxs-lookup"><span data-stu-id="0251c-116">If you want to delete entries, you can do that in the **Delete Change Log Entries** window, where you can set filters based on dates and time.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0251c-117">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0251c-117">See Also</span></span>
[<span data-ttu-id="0251c-118">Basisinstellingen wijzigen</span><span class="sxs-lookup"><span data-stu-id="0251c-118">Changing Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="0251c-119">Sorteervolgorde</span><span class="sxs-lookup"><span data-stu-id="0251c-119">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="0251c-120">Zoeken naar pagina of rapport gebruiken</span><span class="sxs-lookup"><span data-stu-id="0251c-120">Using Search for Page or Report</span></span>](ui-search.md)  
<span data-ttu-id="0251c-121">[Gebruikers en machtigingen beheren](ui-how-users-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="0251c-121">[Manage Users and Permissions](ui-how-users-permissions.md)  </span></span>  
<span data-ttu-id="0251c-122">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0251c-122">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

