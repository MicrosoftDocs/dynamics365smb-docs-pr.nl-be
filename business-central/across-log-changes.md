---
title: Wijzigingen controleren | Microsoft Docs
description: U kunt een gebruikerslogboek activeren zodat u een historie hebt van eventuele wijzigingen in gegevens in getraceerde tabellen. U kunt ook activiteiten volgen met bepaalde soorten activiteitenlogboeken.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user log, user activity, tracking
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: cffa7d23b7c09561914cc00a8a4b9820ed743c29
ms.sourcegitcommit: cd5d3d288feee76d058d325720135275f4c8ad85
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 11/08/2019
ms.locfileid: "2775367"
---
# <a name="auditing-changes-in-business-central"></a><span data-ttu-id="a119c-104">Wijzigingen controleren in Business Central</span><span class="sxs-lookup"><span data-stu-id="a119c-104">Auditing Changes in Business Central</span></span>

<span data-ttu-id="a119c-105">U kunt het wijzigingslogbestand in [!INCLUDE[d365fin](includes/d365fin_md.md)] inschakelen, zodat u een overzicht van activiteiten hebt.</span><span class="sxs-lookup"><span data-stu-id="a119c-105">You can enable the change log in [!INCLUDE[d365fin](includes/d365fin_md.md)] so you have a history of activities.</span></span> <span data-ttu-id="a119c-106">Het logboek is gebaseerd op wijzigingen die worden aangebracht in gegevens in de tabellen die u bijhoudt. Op de pagina **Wijzigingslogposten** worden posten chronologisch geordend en worden wijzigingen weergeven die worden aangebracht in de velden in de opgegeven tabellen.</span><span class="sxs-lookup"><span data-stu-id="a119c-106">The log is based on changes that are made to data in the tables that you track. On the **Change Log Entries** page, entries are chronologically ordered and show changes that are made to the fields on the specified tables.</span></span> <span data-ttu-id="a119c-107">In het wijzigingslogbestand verzamelt alle wijzigingen die in de tabel worden aangebracht.</span><span class="sxs-lookup"><span data-stu-id="a119c-107">The change log collects all changes that are made to the table.</span></span>

> [!Important]
> <span data-ttu-id="a119c-108">Wijzigingen van een gebruiker zijn pas zichtbaar in de **Wijzigingslogposten** als de sessie van de gebruiker opnieuw wordt gestart, wat in de volgende gevallen gebeurt:</span><span class="sxs-lookup"><span data-stu-id="a119c-108">A user's changes are not visible in the **Change Log Entries** until the user's session is restarted, which happens in the following cases:</span></span>
<br />
> * <span data-ttu-id="a119c-109">De sessie is verlopen en vernieuwd.</span><span class="sxs-lookup"><span data-stu-id="a119c-109">The session expired and was refreshed.</span></span>
> * <span data-ttu-id="a119c-110">De gebruiker heeft een ander bedrijf of rolcentrum geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="a119c-110">The user selected another company or Role Center.</span></span>
> * <span data-ttu-id="a119c-111">De gebruiker heeft zich af- en weer aangemeld.</span><span class="sxs-lookup"><span data-stu-id="a119c-111">The user signed out and back in.</span></span>

## <a name="working-with-the-change-log"></a><span data-ttu-id="a119c-112">Werken met het wijzigingslogbestand</span><span class="sxs-lookup"><span data-stu-id="a119c-112">Working with the Change Log</span></span>

<span data-ttu-id="a119c-113">Een vaak voorkomend probleem in veel financiële systemen is het lokaliseren van de oorzaak van fouten en wijzigingen in gegevens.</span><span class="sxs-lookup"><span data-stu-id="a119c-113">A common problem in many financial systems is to locate the origin of errors and changes in data.</span></span> <span data-ttu-id="a119c-114">Het probleem kan variëren van een foutief telefoonnummer van een klant tot een foutieve boeking naar het grootboek.</span><span class="sxs-lookup"><span data-stu-id="a119c-114">It could be anything from an incorrect customer telephone number to an incorrect posting to the general ledger.</span></span> <span data-ttu-id="a119c-115">Met het wijzigingslogbestand kunt u alle directe wijzigingen bijhouden die een gebruiker aanbrengt in de databasegegevens.</span><span class="sxs-lookup"><span data-stu-id="a119c-115">The change log lets you track all direct modifications a user makes to data in the database.</span></span> <span data-ttu-id="a119c-116">U moet elke tabel en elk veld opgeven dat u door het systeem wilt laten registreren. Vervolgens moet u het wijzigingslogbestand instellen.</span><span class="sxs-lookup"><span data-stu-id="a119c-116">You must specify each table and field that you want the system to log, and then you must activate the change log.</span></span>  

<span data-ttu-id="a119c-117">U activeert en deactiveert het wijzigingslogbestand op de pagina **Wijzigingslogbestandinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="a119c-117">You activate and deactivate the change log on the **Change Log Setup** page.</span></span> <span data-ttu-id="a119c-118">Wanneer een gebruiker het wijzigingslogbestand activeert of deactiveert, wordt deze activiteit geregistreerd, zodat u altijd kunt zien welke gebruiker het wijzigingslogbestand heeft gedeactiveerd of opnieuw heeft geactiveerd.</span><span class="sxs-lookup"><span data-stu-id="a119c-118">When a user activates or deactivates the change log, this activity is logged, so you can always see which user deactivated or reactivated the change log.</span></span>

<span data-ttu-id="a119c-119">Op de pagina **Wijzigingslogbestandinstellingen** kunt u als u de actie **Tabellen** kiest, opgeven voor welke tabellen u wijzigingen wilt bijhouden en welke wijzigingen moeten worden bijgehouden. [!INCLUDE[d365fin](includes/d365fin_md.md)] houdt ook een aantal systeemtabellen bij.</span><span class="sxs-lookup"><span data-stu-id="a119c-119">On the **Change Log Setup** page, if you choose the **Tables** action, you can specify which tables you want to track changes for, and which changes to track. [!INCLUDE[d365fin](includes/d365fin_md.md)] also tracks a number of system tables.</span></span>

<span data-ttu-id="a119c-120">Nadat u het wijzigingslogbestand hebt ingesteld, hebt geactiveerd en gegevens hebt gewijzigd, kunt u de wijzigingen weergeven en filteren op de pagina **Wijzigingslogposten**.</span><span class="sxs-lookup"><span data-stu-id="a119c-120">After you have set up the change log, activated it, and made a change to data, you can view and filter the changes on the **Change Log Entries** page.</span></span> <span data-ttu-id="a119c-121">Als u posten wilt verwijderen, kunt u dat doen op de pagina **Wijzigingslogposten verwijderen**, waar u filters kunt instellen op basis van datums en tijd.</span><span class="sxs-lookup"><span data-stu-id="a119c-121">If you want to delete entries, you can do that on the **Delete Change Log Entries** page, where you can set filters based on dates and time.</span></span>  

## <a name="working-with-activity-logs"></a><span data-ttu-id="a119c-122">Werken met activiteitenlogboeken</span><span class="sxs-lookup"><span data-stu-id="a119c-122">Working with Activity Logs</span></span>

<span data-ttu-id="a119c-123">Vanaf enkele pagina's in [!INCLUDE [prodshort](includes/prodshort.md)] kunt u een activiteitenlogboek bekijken dat de status en eventuele fouten weergeeft van bestanden waarnaar u exporteert vanuit of importeert in [!INCLUDE [prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="a119c-123">From some pages in [!INCLUDE [prodshort](includes/prodshort.md)], you can view an activity log that shows the status and any errors from files that you export from or import into [!INCLUDE [prodshort](includes/prodshort.md)].</span></span>  

<span data-ttu-id="a119c-124">De informatie wordt weergegeven in het venster **Activiteitenlogboek**, volgens de context van waaruit het wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="a119c-124">The information is displayed in the **Activity Log** page, according to the context that it is opened from.</span></span> <span data-ttu-id="a119c-125">U kunt het venster bijvoorbeeld openen vanuit de pagina's **Documentuitwisselingsservice instellen**, **Inkomend document**, **Geboekte verkoopfactuur**en **Geboekte verkoopkredietnota**.</span><span class="sxs-lookup"><span data-stu-id="a119c-125">You can open the window from the **Document Exchange Service Setup**, **Incoming Document**, **Posted Sales Invoice**, and **Posted Sales Credit Memo** pages, for example.</span></span> <span data-ttu-id="a119c-126">U kunt de lijst met logboekvermeldingen leegmaken of gewoon de lijst met vermeldingen ouder dan 7 dagen wissen.</span><span class="sxs-lookup"><span data-stu-id="a119c-126">You can empty the list of log entries, or just clear the list of entries older than 7 days.</span></span>  

## <a name="see-also"></a><span data-ttu-id="a119c-127">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a119c-127">See Also</span></span>
[<span data-ttu-id="a119c-128">Basisinstellingen wijzigen</span><span class="sxs-lookup"><span data-stu-id="a119c-128">Change Basic Settings</span></span>](ui-change-basic-settings.md)  
[<span data-ttu-id="a119c-129">Sorteervolgorde</span><span class="sxs-lookup"><span data-stu-id="a119c-129">Sorting</span></span>](ui-sorting.md)  
[<span data-ttu-id="a119c-130">Pagina's en informatie zoeken met Vertel me</span><span class="sxs-lookup"><span data-stu-id="a119c-130">Finding Pages and Information with Tell Me</span></span>](ui-search.md)  
<span data-ttu-id="a119c-131">[Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md)  </span><span class="sxs-lookup"><span data-stu-id="a119c-131">[Assign Permissions to Users and Groups](ui-define-granular-permissions.md)  </span></span>  
<span data-ttu-id="a119c-132">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a119c-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
