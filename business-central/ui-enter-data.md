---
title: Gegevens invoeren in velden | Microsoft Docs
description: Leer over algemene functies die u helpen gegevens in velden in te voeren.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 00143454cf0b0da9b111f92bcdb7879c7e6743d2
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "929085"
---
# <a name="entering-data"></a><span data-ttu-id="7b076-103">Gegevens invoeren</span><span class="sxs-lookup"><span data-stu-id="7b076-103">Entering Data</span></span>

<span data-ttu-id="7b076-104">Er zijn allerlei algemene functies die u helpen gegevens sneller, gemakkelijker en accurater in te voeren.</span><span class="sxs-lookup"><span data-stu-id="7b076-104">There are many general features that help you enter data easier, faster, and more accurate.</span></span> <span data-ttu-id="7b076-105">De algemene functies voor het invoeren van gegevens worden in dit artikel beschreven.</span><span class="sxs-lookup"><span data-stu-id="7b076-105">The general features for entering data are described in this article.</span></span>  

<!-- The examples in this article use the demonstration data.-->

## <a name="keyboard-shortcuts"></a><span data-ttu-id="7b076-106">Toetsenbordsneltoetsen</span><span class="sxs-lookup"><span data-stu-id="7b076-106">Keyboard Shortcuts</span></span>

<span data-ttu-id="7b076-107">Er zijn verschillende sneltoetsen waarmee u 'muisvrij' kunt werken en de gegevensinvoer kunt versnellen, vooral bij grootschalige invoer en herhaald typewerk.</span><span class="sxs-lookup"><span data-stu-id="7b076-107">There are several keyboard shortcuts that let you to work "mouse-free" and speed up your data entry, especially with large scale entries and repetitive typing tasks.</span></span>

<span data-ttu-id="7b076-108">Zie voor meer informatie over sneltoetsen [Toetsenbordsneltoetsen](keyboard-shortcuts.md).</span><span class="sxs-lookup"><span data-stu-id="7b076-108">For more information about shortcuts, see [Keyboard Shortcuts](keyboard-shortcuts.md).</span></span> <span data-ttu-id="7b076-109">Enkele sneltoetsen worden in dit artikel besproken.</span><span class="sxs-lookup"><span data-stu-id="7b076-109">A few of the shortcuts are discussed in this article.</span></span>

## <a name="QuickEntry"></a><span data-ttu-id="7b076-110">Gegevensinvoer versnellen met snelinvoer</span><span class="sxs-lookup"><span data-stu-id="7b076-110">Accelerating Data Entry Using Quick Entry</span></span>

<span data-ttu-id="7b076-111">Snelinvoer is een functie die bedoeld is voor gegevensinvoer met het toetsenbord.</span><span class="sxs-lookup"><span data-stu-id="7b076-111">Quick Entry is a feature designed for data entry when using the keyboard.</span></span> <span data-ttu-id="7b076-112">Snelinvoer werkt met velden (bijvoorbeeld op kaartpagina's) en in lijsten (rijen en kolommen).</span><span class="sxs-lookup"><span data-stu-id="7b076-112">Quick Entry works on fields (like on card pages) and in lists (rows and columns).</span></span> <span data-ttu-id="7b076-113">Het kan handig zijn bij herhalend typewerk, waarbij meerdere records achter elkaar moeten worden gemaakt, zoals een batch verkooporders of registratie van nieuwe artikelen.</span><span class="sxs-lookup"><span data-stu-id="7b076-113">It is beneficial when performing repetitive typing tasks that require creating multiple records in sequence, such as a batch of sales orders or registering new items.</span></span>

<span data-ttu-id="7b076-114">U bent mogelijk al vertrouwd met het gebruik van de Tab-toets om van het ene veld op een pagina naar het volgende bewerkbare veld te navigeren.</span><span class="sxs-lookup"><span data-stu-id="7b076-114">You might already be familiar with using the Tab key to navigate from one field on a page to the next editable field.</span></span> <span data-ttu-id="7b076-115">Het nadeel van het gebruik van de Tab-toets is dat deze altijd naar het volgende veld gaat.</span><span class="sxs-lookup"><span data-stu-id="7b076-115">A disadvantage of using Tab is that it always goes sequentially to the next field.</span></span> <!-- even if the field is non-editable or seldom filled it in.--><span data-ttu-id="7b076-116">Met snelinvoer kunt u dit pad wijzigen.</span><span class="sxs-lookup"><span data-stu-id="7b076-116">Quick Entry lets you change this path.</span></span> <span data-ttu-id="7b076-117">Met snelinvoer gebruikt u de Enter-toets om alleen te navigeren naar de velden waarin u geïnteresseerd bent. U slaat niet-bewerkbare velden en velden die u meestal niet invult, over.</span><span class="sxs-lookup"><span data-stu-id="7b076-117">With Quick Entry, you use the Enter key to navigate through only those fields that you are interested in, skipping non-editable fields and fields that you typically do not fill in.</span></span> <span data-ttu-id="7b076-118">U hebt dit gedrag mogelijk al op bepaalde pagina's opgemerkt.</span><span class="sxs-lookup"><span data-stu-id="7b076-118">You might have already noticed this behavior on some pages.</span></span> <span data-ttu-id="7b076-119">Dit komt omdat de toepassing al aangeeft welke velden moeten worden opgenomen wanneer op Enter wordt gedrukt en welke worden overgeslagen.</span><span class="sxs-lookup"><span data-stu-id="7b076-119">This is because the application already designates which fields to include when pressing Enter and which ones to skip.</span></span> <span data-ttu-id="7b076-120">U kunt snelinvoer wijzigen door de werkruimte aan te passen en te optimaliseren hoe u gegevens op elke pagina invoert.</span><span class="sxs-lookup"><span data-stu-id="7b076-120">You can customize Quick Entry by personalizing your workspace and optimizing how you enter data on each page.</span></span>

### <a name="how-quick-entry-works"></a><span data-ttu-id="7b076-121">Hoe snelinvoer werkt</span><span class="sxs-lookup"><span data-stu-id="7b076-121">How Quick Entry Works</span></span>

<span data-ttu-id="7b076-122">Elk veld kan worden gemarkeerd als zijnde *opgenomen in snelinvoer* of *uitgesloten van snelinvoer*.</span><span class="sxs-lookup"><span data-stu-id="7b076-122">Every field can be marked as either being *included in Quick Entry* or *excluded from Quick Entry*.</span></span> <span data-ttu-id="7b076-123">Velden die in snelinvoer zijn opgenomen, worden opgenomen in het pad wanneer u op Enter drukt; velden die zijn uitgesloten van snelinvoer, worden dat niet.</span><span class="sxs-lookup"><span data-stu-id="7b076-123">Fields that are included in Quick Entry, will be included in the path when you press Enter; fields that are excluded from Quick Entry, will not.</span></span>

<span data-ttu-id="7b076-124">Wanneer u klaar bent met het invoeren van gegevens in een veld, drukt u gewoon op Enter om de wijzigingen te bevestigen en naar het volgende veld te gaan.</span><span class="sxs-lookup"><span data-stu-id="7b076-124">When you are finished entering data in a field, you simply press Enter to confirm the changes and go to the next field.</span></span> <span data-ttu-id="7b076-125">Als u de volgorde wilt omkeren en naar het vorige veld wilt gaan, drukt u op Shift+Enter.</span><span class="sxs-lookup"><span data-stu-id="7b076-125">If you want to reverse direction, and go the previous field, press Shift+Enter.</span></span> <span data-ttu-id="7b076-126">Zie voor meer informatie over sneltoetsen [Toetsenbordsneltoetsen voor snelinvoer](keyboard-shortcuts.md#QuickEntry).</span><span class="sxs-lookup"><span data-stu-id="7b076-126">For more information about shortcuts, see [Quick Entry keyboard shortcuts](keyboard-shortcuts.md#QuickEntry).</span></span>

#### <a name="tips-and-tricks"></a><span data-ttu-id="7b076-127">Tips en trucs</span><span class="sxs-lookup"><span data-stu-id="7b076-127">Tips and tricks</span></span>
<span data-ttu-id="7b076-128">Hieronder volgt wat nuttige informatie over het gebruik van snelinvoer.</span><span class="sxs-lookup"><span data-stu-id="7b076-128">The following provides some useful information about using Quick Entry.</span></span>

- <span data-ttu-id="7b076-129">Het is beschikbaar voor bewerkbare velden.</span><span class="sxs-lookup"><span data-stu-id="7b076-129">It is available for any editable fields.</span></span>
- <span data-ttu-id="7b076-130">Het werkt ook over kolommen en rijen.</span><span class="sxs-lookup"><span data-stu-id="7b076-130">It also works across columns and rows.</span></span>
- <span data-ttu-id="7b076-131">Het voorkomt geen toegang tot andere elementen van een pagina, zoals acties.</span><span class="sxs-lookup"><span data-stu-id="7b076-131">It does not prevent accessing other elements of a page, such as actions.</span></span> <span data-ttu-id="7b076-132">Deze zijn nog toegankelijk met behulp van Tab en Shift+Tab.</span><span class="sxs-lookup"><span data-stu-id="7b076-132">These are still accessible by using Tab and Shift+Tab.</span></span>  
- <span data-ttu-id="7b076-133">Sneltabbladen hoeven niet uitgevouwen te zijn om snelinvoer te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="7b076-133">FastTabs do not have to be expanded for Quick Entry to work.</span></span> <span data-ttu-id="7b076-134">Als het volgende snelinvoerveld zich in een samengevouwen sneltabblad bevindt, wordt dat sneltabblad automatisch uitgevouwen en gaat de focus naar het juiste veld.</span><span class="sxs-lookup"><span data-stu-id="7b076-134">If the next Quick Entry field is located in a collapsed FastTab, that FastTab will automatically expand and focus on the designated field.</span></span>
- <span data-ttu-id="7b076-135">Snelinvoer werkt ongeacht of velden verplicht zijn.</span><span class="sxs-lookup"><span data-stu-id="7b076-135">Quick Entry works irrespective of whether fields are mandatory.</span></span> <span data-ttu-id="7b076-136">Het is dus een goed idee te zorgen dat verplichte velden zijn opgenomen in snelinvoer.</span><span class="sxs-lookup"><span data-stu-id="7b076-136">So it is a good idea to ensure that mandatory fields are included in Quick Entry.</span></span>
- <span data-ttu-id="7b076-137">Standaard worden de meeste velden automatisch opgenomen in snelinvoer.</span><span class="sxs-lookup"><span data-stu-id="7b076-137">By default, most fields are automatically included in Quick Entry.</span></span> <span data-ttu-id="7b076-138">In eerste instantie moet u dus waarschijnlijk velden uitsluiten van snelinvoer.</span><span class="sxs-lookup"><span data-stu-id="7b076-138">So initially your task will most likely be excluding fields from Quick Entry.</span></span>

### <a name="how-to-change-quick-entry-fields"></a><span data-ttu-id="7b076-139">Hoe u snelinvoervelden wijzigt</span><span class="sxs-lookup"><span data-stu-id="7b076-139">How to Change Quick Entry Fields</span></span>

<span data-ttu-id="7b076-140">Als u wilt wijzigen welke velden zijn opgenomen in of uitgesloten van snelinvoer op een pagina, gebruikt u personalisatie.</span><span class="sxs-lookup"><span data-stu-id="7b076-140">To change which fields are included in or excluded from Quick Entry on a page, you use personalization.</span></span>

1. <span data-ttu-id="7b076-141">Start personalisatie door het pictogram ![Instellingen](media/ui-experience/settings_icon_small.png "pictogram Instellingen voor rolcentrum") te selecteren en vervolgens **Personaliseren**.</span><span class="sxs-lookup"><span data-stu-id="7b076-141">Start personalization by selecting the ![Settings](media/ui-experience/settings_icon_small.png "Settings icon for role center") icon, and then **Personalize**.</span></span>
2. <span data-ttu-id="7b076-142">Selecteer een veld dat u wilt wijzigen of selecteer in lijsten de corresponderende kolomkop en kies vervolgens **Opnemen in snelinvoer** of **Uitsluiten van snelinvoer**.</span><span class="sxs-lookup"><span data-stu-id="7b076-142">Select a field that you want change, or in lists, select the corresponding column heading, and then choose either **Include in Quick Entry** or **Exclude from Quick Entry**.</span></span>

<span data-ttu-id="7b076-143">Zie voor meer informatie over personalisatie [Uw werkruimte personaliseren](ui-personalization-user.md).</span><span class="sxs-lookup"><span data-stu-id="7b076-143">For more information about personalization, see [Personalizing Your Workspace](ui-personalization-user.md).</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="7b076-144">Verplichte velden</span><span class="sxs-lookup"><span data-stu-id="7b076-144">Mandatory Fields</span></span>

<span data-ttu-id="7b076-145">Wanneer u gegevens invoert op pagina's, zijn bepaalde velden gemarkeerd met een rode asterisk.</span><span class="sxs-lookup"><span data-stu-id="7b076-145">When you enter data on pages, certain fields are marked with a red asterisk.</span></span> <span data-ttu-id="7b076-146">De rode asterisk betekent dat het veld moet worden ingevuld om een bepaald proces te voltooien dat het veld gebruikt, zoals het boeken van een transactie die de waarde in het veld gebruikt.</span><span class="sxs-lookup"><span data-stu-id="7b076-146">The red asterisk means that the field must be filled to complete a certain process that uses the field, such as posting a transaction that uses the value in the field.</span></span>  

<span data-ttu-id="7b076-147">Zelfs als het veld een rode asterisk bevat, wordt u niet gedwongen het veld te vullen voordat u verdergaat naar andere velden of de pagina sluit.</span><span class="sxs-lookup"><span data-stu-id="7b076-147">Even though the field contains a red asterisk, you are not forced to fill the field before you continue to other fields or close the page.</span></span> <span data-ttu-id="7b076-148">De rode asterisk dient alleen als een herinnering dat u wordt geblokkeerd van het voltooien van een bepaald proces.</span><span class="sxs-lookup"><span data-stu-id="7b076-148">The red asterisk only serves as a reminder that you will be blocked from completing a certain process.</span></span>  

## <a name="finding-data-as-you-type"></a><span data-ttu-id="7b076-149">Gegevens zoeken terwijl u typt</span><span class="sxs-lookup"><span data-stu-id="7b076-149">Finding Data As You Type</span></span>

 <span data-ttu-id="7b076-150">Als u begint met het typen van tekens in een veld, wordt een vervolgkeuzelijst weergeven met de mogelijke veldwaarden.</span><span class="sxs-lookup"><span data-stu-id="7b076-150">When you start to type characters in a field, a drop-down list is displayed and shows possible field values.</span></span> <span data-ttu-id="7b076-151">De lijst verandert naarmate u meer tekens typt en u kunt de juiste waarde selecteren wanneer deze wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="7b076-151">The list changes as you type more characters, and you can select the correct value when it is displayed.</span></span>  

 <span data-ttu-id="7b076-152">Veel velden hebben een knop met een pijl-omlaag die u kunt kiezen.</span><span class="sxs-lookup"><span data-stu-id="7b076-152">Many fields have a down arrow button that you can choose.</span></span> <span data-ttu-id="7b076-153">U kunt op de pijl klikken om een lijst met gegevens te krijgen die u in het veld kunt instellen.</span><span class="sxs-lookup"><span data-stu-id="7b076-153">You choose the arrow to get a list of data that is available to enter in the field.</span></span> <span data-ttu-id="7b076-154">De knop heeft twee functies, afhankelijk van het type veld:</span><span class="sxs-lookup"><span data-stu-id="7b076-154">The button has two functions depending on the type of field:</span></span>  

-   <span data-ttu-id="7b076-155">Opzoeken - Hiermee toont u gegevens uit een andere tabel die u in het veld kunt invoeren.</span><span class="sxs-lookup"><span data-stu-id="7b076-155">Lookup - Displays information from another table that you can enter in the field.</span></span> <span data-ttu-id="7b076-156">U kunt slechts één gegevensitem tegelijk selecteren.</span><span class="sxs-lookup"><span data-stu-id="7b076-156">You can select one piece of data at a time.</span></span>  

-   <span data-ttu-id="7b076-157">Vervolgkeuze - Hiermee toont u de verzameling opties die beschikbaar zijn voor het veld.</span><span class="sxs-lookup"><span data-stu-id="7b076-157">Drop-down - Displays the set of options that exist for the field.</span></span> <span data-ttu-id="7b076-158">U kunt slechts één optie tegelijk selecteren.</span><span class="sxs-lookup"><span data-stu-id="7b076-158">You can select only one of the options.</span></span>  

## <a name="copying-and-pasting-fields-and-lines"></a><span data-ttu-id="7b076-159">Velden en regels kopiëren en plakken</span><span class="sxs-lookup"><span data-stu-id="7b076-159">Copying and Pasting Fields and Lines</span></span>

<span data-ttu-id="7b076-160">U kunt een of meer rijen uit een lijst of een enkel veld op een pagina kopiëren en vervolgens wat u hebt gekopieerd, plakken op dezelfde pagina, een andere pagina of een extern document (zoals Microsoft Excel en Outlook-e-mail).</span><span class="sxs-lookup"><span data-stu-id="7b076-160">You can copy one or more rows from a list or a single field on a page, and then paste what you copied into the same page, another page, or an external document (like Microsoft Excel and Outlook email).</span></span> <span data-ttu-id="7b076-161">Als u wilt kopiëren, drukt u op CTRL+C (cmd+C in MacOs) op het toetsenbord.</span><span class="sxs-lookup"><span data-stu-id="7b076-161">In short, to copy, you press CTRL+C (cmd+C in macOS) on your keyboard.</span></span> <span data-ttu-id="7b076-162">Als u wilt plakken, drukt u op CTRL+V (cmd+V in MacOs).</span><span class="sxs-lookup"><span data-stu-id="7b076-162">To paste, you press CTRL+V (cmd+V in macOS).</span></span>

<span data-ttu-id="7b076-163">Als u in een lijst het veld in dezelfde kolom van de bovenliggende rij wilt selecteren en het in de huidige rij wilt plakken, drukt u op F8.</span><span class="sxs-lookup"><span data-stu-id="7b076-163">In a list, to copy the field in the same column of the row above, and paste it into the current row, just press F8.</span></span>

<span data-ttu-id="7b076-164">Zie voor meer informatie [Kopiëren en plakken in Business Central](ui-copy-paste.md).</span><span class="sxs-lookup"><span data-stu-id="7b076-164">For more information, see [Copying and Pasting in Business Central](ui-copy-paste.md).</span></span>

## <a name="Focus"></a><span data-ttu-id="7b076-165">Focussen op regelartikelen</span><span class="sxs-lookup"><span data-stu-id="7b076-165">Focusing on Line Items</span></span>

<span data-ttu-id="7b076-166">Wanneer u werkt aan documenten die een onderdeel met regelartikelen bevatten, zoals een verkooporder of een factuurpagina, kunt u de weergave overschakelen om alleen te focussen op de regelartikelen. In wezen vouwt u het onderdeel met regelartikelen uit, zodat het ongeveer de hele werkruimte in beslag neemt. Andere delen van de pagina worden verborgen, behalve het actiegebied bovenin.</span><span class="sxs-lookup"><span data-stu-id="7b076-166">When working on documents that include a line items part, like a sales order or invoice page, you can switch your view to focus only on the line items, essentially expanding the line items part so that it occupies pretty much the entire workspace - hiding other parts of the page except the actions area at the top.</span></span> <span data-ttu-id="7b076-167">Dit geeft u een beter overzicht van de regelartikelen en biedt meer ruimte om ermee te werken.</span><span class="sxs-lookup"><span data-stu-id="7b076-167">This gives you a better overview of the lines items, and provides more room to work on them.</span></span> <span data-ttu-id="7b076-168">Dit is met name voordelig bij het werken met grote regelartikellijsten en als snelle gegevensinvoer gewenst is.</span><span class="sxs-lookup"><span data-stu-id="7b076-168">This is particularly beneficial when working with large line item lists and fast data entry is desired.</span></span>

<span data-ttu-id="7b076-169">Een ander voordeel is dat het ook geavanceerde filtermogelijkheden biedt, zoals in andere lijsten, waardoor bladeren en zoeken door regelartikelen nog gemakkelijker wordt.</span><span class="sxs-lookup"><span data-stu-id="7b076-169">Another advantage is that it also provides advanced filtering capability, like on other lists, so browsing and searching through line items becomes even easier.</span></span>

### <a name="switch-the-focus-on-and-off"></a><span data-ttu-id="7b076-170">De focus aan- en uitzetten</span><span class="sxs-lookup"><span data-stu-id="7b076-170">Switch the Focus On and Off</span></span>

<span data-ttu-id="7b076-171">Als u op regelartikelen wilt focussen, selecteert u iets in het onderdeel met regelartikelen en kiest u vervolgens het ![pictogram Focusmodus](media/focus-mode.png "pictogram Focusmodus") in de rechterbovenhoek of drukt u op Ctrl+Shift+F12.</span><span class="sxs-lookup"><span data-stu-id="7b076-171">To focus on lines items, select anywhere in the line item part, and then choose ![Focus Mode icon](media/focus-mode.png "Focus mode icon") in the upper right corner or press Ctrl+Shift+F12.</span></span>

<span data-ttu-id="7b076-172">Als u terug wilt naar de gewone weergave, kiest u opnieuw het ![pictogram Focusmodus](media/focus-mode.png "pictogram Focusmodus") of drukt opnieuw op Ctrl+Shift+F12.</span><span class="sxs-lookup"><span data-stu-id="7b076-172">To switch back to the normal view, choose ![Focus Mode icon](media/focus-mode.png "Focus mode icon") or press Ctrl+Shift+F12 again.</span></span>

### <a name="filtering-the-line-items"></a><span data-ttu-id="7b076-173">Regelartikelen filteren</span><span class="sxs-lookup"><span data-stu-id="7b076-173">Filtering the Line Items</span></span>

<span data-ttu-id="7b076-174">Als u wilt beginnen met filteren, selecteert u het ![pictogram Filterdeelvenster](media/open-filter-pane-icon.png "pictogram Filterdeelvenster") boven aan de lijst of drukt u op **Shift+F3** om het filterdeelvenster te openen.</span><span class="sxs-lookup"><span data-stu-id="7b076-174">To start filtering, select ![Filter pane icon](media/open-filter-pane-icon.png "Filter pane icon") at the top of the list or press **Shift+F3** to open the filter pane.</span></span> <span data-ttu-id="7b076-175">U werkt met het filterdeelvenster zoals met elke andere lijst.</span><span class="sxs-lookup"><span data-stu-id="7b076-175">You work with the filter pane as you do on any other list.</span></span> <span data-ttu-id="7b076-176">Zie [Filteren](ui-enter-criteria-filters.md#Filtering) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="7b076-176">For more information, see [Filtering](ui-enter-criteria-filters.md#Filtering).</span></span>

<span data-ttu-id="7b076-177">Filteren is met name handig bij het weergeven en analyseren van langere documenten.</span><span class="sxs-lookup"><span data-stu-id="7b076-177">Filtering is especially helpful when viewing and analysing longer documents.</span></span> <span data-ttu-id="7b076-178">Stel dat u een geboekte verkoopfactuur opent en de regelartikelen filtert om alle regelartikelen weer te geven die een individuele korting van meer dan 5% hebben, of dat u filtert om alleen fietsaccessoires met 'pro' in de naam weer te geven.</span><span class="sxs-lookup"><span data-stu-id="7b076-178">For example, imagine you open a posted sales invoice and filter the line items to display all line items that have an individual discount above 5%, or filter to display only bike accessories with 'pro' in the name.</span></span>

## <a name="entering-quantities-by-calculation"></a><span data-ttu-id="7b076-179">Hoeveelheden invoeren door berekening</span><span class="sxs-lookup"><span data-stu-id="7b076-179">Entering Quantities by Calculation</span></span>

<span data-ttu-id="7b076-180">Als u getallen in velden voor hoeveelheden invoert, zoals het veld **Hoeveelheid** op een artikeldagboekregel, kunt u de formule invoeren in plaats van de totale hoeveelheid.</span><span class="sxs-lookup"><span data-stu-id="7b076-180">When entering numbers into quantity fields, such as the **Quantity** field on an item journal line, you can enter the formula instead of the sum quantity.</span></span>  

### <a name="examples"></a><span data-ttu-id="7b076-181">Voorbeelden</span><span class="sxs-lookup"><span data-stu-id="7b076-181">Examples</span></span>  

-   <span data-ttu-id="7b076-182">Als u 19+19 invoert, wordt het veld berekend als 38.</span><span class="sxs-lookup"><span data-stu-id="7b076-182">If you enter 19+19, the field is calculated to 38.</span></span>  

-   <span data-ttu-id="7b076-183">Als u 41-9, wordt het veld berekend als 32.</span><span class="sxs-lookup"><span data-stu-id="7b076-183">If you enter 41-9, the field is calculated to 32.</span></span>  

-   <span data-ttu-id="7b076-184">Als u 12\*4 invoert, wordt het veld berekend als 48.</span><span class="sxs-lookup"><span data-stu-id="7b076-184">If you enter 12\*4, the field is calculated to 48.</span></span>  

-   <span data-ttu-id="7b076-185">Als u 12/4 invoert, wordt het veld berekend als 3.</span><span class="sxs-lookup"><span data-stu-id="7b076-185">If you enter 12/4, the field is calculated to 3.</span></span>  

## <a name="entering-negative-numbers"></a><span data-ttu-id="7b076-186">Negatieve getallen invoeren</span><span class="sxs-lookup"><span data-stu-id="7b076-186">Entering Negative Numbers</span></span>

<span data-ttu-id="7b076-187">U kunt negatieve getallen op twee manieren invoeren.</span><span class="sxs-lookup"><span data-stu-id="7b076-187">You can enter negative numbers in two ways.</span></span> <span data-ttu-id="7b076-188">Nummer -20.5 kan worden ingevoerd als:</span><span class="sxs-lookup"><span data-stu-id="7b076-188">The number -20.5 can be entered as:</span></span>  

-   <span data-ttu-id="7b076-189">-20,5</span><span class="sxs-lookup"><span data-stu-id="7b076-189">-20.5</span></span>  

    <span data-ttu-id="7b076-190">of</span><span class="sxs-lookup"><span data-stu-id="7b076-190">or</span></span>
-   <span data-ttu-id="7b076-191">20,5-</span><span class="sxs-lookup"><span data-stu-id="7b076-191">20.5-</span></span>  

 <span data-ttu-id="7b076-192">In beide gevallen wordt het bedrag als -20,5 geregistreerd.</span><span class="sxs-lookup"><span data-stu-id="7b076-192">In both cases, the amount will be recorded in as -20.5.</span></span>  

 <span data-ttu-id="7b076-193">Als het laatste teken van de expressie een **+** of een **-** is, wordt de volledige expressie vastgelegd met dat teken.</span><span class="sxs-lookup"><span data-stu-id="7b076-193">If the last character of the expression is a **+** or a **-**, the entire expression will be recorded with that sign.</span></span> <span data-ttu-id="7b076-194">Een voorbeeld: **10-20+** resulteert in 10 en niet -10.</span><span class="sxs-lookup"><span data-stu-id="7b076-194">An example, **10-20+** will result in 10 and not -10.</span></span>  

## <a name="entering-dates-and-times"></a><span data-ttu-id="7b076-195">Datums en tijden invoeren</span><span class="sxs-lookup"><span data-stu-id="7b076-195">Entering Dates and Times</span></span>

<span data-ttu-id="7b076-196">U kunt datums en tijden invoeren in alle velden die speciaal zijn toegewezen aan datums (datumvelden).</span><span class="sxs-lookup"><span data-stu-id="7b076-196">You can enter dates and times in all the fields that are specifically assigned to dates (date fields).</span></span> <span data-ttu-id="7b076-197">U kunt datums met of zonder scheidingstekens invoeren.</span><span class="sxs-lookup"><span data-stu-id="7b076-197">You can enter dates with or without separators.</span></span>

> [!NOTE]  
> <span data-ttu-id="7b076-198">Hoe u datums en tijden invoert, hangt af van uw instellingen onder **Regio**.</span><span class="sxs-lookup"><span data-stu-id="7b076-198">How you enter dates and times depends on your **Region** settings.</span></span> <span data-ttu-id="7b076-199">Zie voor meer informatie [Basisinstellingen wijzigen](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="7b076-199">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>  

### <a name="entering-dates"></a><span data-ttu-id="7b076-200">Datums invoeren</span><span class="sxs-lookup"><span data-stu-id="7b076-200">Entering Dates</span></span>

<span data-ttu-id="7b076-201">Voor datumvelden kunt u de datumselectie gebruiken. Hiermee selecteert u een datum in een kalender of voert u handmatig datums in.</span><span class="sxs-lookup"><span data-stu-id="7b076-201">For date fields, you can either use the data picker, which lets you select a date from a calender, or you can enter dates manually.</span></span> <span data-ttu-id="7b076-202">Deze sectie geeft een kort overzicht van hoe u datums invoert.</span><span class="sxs-lookup"><span data-stu-id="7b076-202">This section provides a brief overview of how to enter dates.</span></span> <span data-ttu-id="7b076-203">Zie voor meer informatie [Werken met kalenderdatums en tijden](ui-enter-date-ranges.md).</span><span class="sxs-lookup"><span data-stu-id="7b076-203">For more details, see [Working with Calendar Dates and Times](ui-enter-date-ranges.md).</span></span>

<span data-ttu-id="7b076-204">Voor handmatige datuminvoer kunt u twee, vier, zes of acht cijfers invoeren:</span><span class="sxs-lookup"><span data-stu-id="7b076-204">For manually date entry, you can enter two, four, six, or eight digits:</span></span>  

-   <span data-ttu-id="7b076-205">Als u slechts twee cijfers invoert, wordt dit als een dag beschouwd en wordt de maand en het jaar van de werkdag automatisch toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="7b076-205">If you enter only two digits, this is interpreted as the day, and it will add the month and the year of the work date.</span></span>  

-   <span data-ttu-id="7b076-206">Als u vier cijfers invoert, wordt dit als een dag en een maand beschouwd en wordt het jaar van de werkdag automatisch toegevoegd.</span><span class="sxs-lookup"><span data-stu-id="7b076-206">If you enter four digits, this is interpreted as the day and the month, and it will add the year of the work date.</span></span>  

-   <span data-ttu-id="7b076-207">Als de ingevoerde datum in de reeks 01/01/1930 tot en met 31/12/2029 valt, hoeft u slechts twee cijfers voor het jaartal in te voeren; anders moet u vier cijfers voor het jaartal invoeren.</span><span class="sxs-lookup"><span data-stu-id="7b076-207">If the date you want to enter is in the range 01/01/1930 through 12/31/2029, you can enter the year with two digits; otherwise, enter the year with four digits.</span></span>  

<span data-ttu-id="7b076-208">U kunt een datum ook invoeren als een weekdag gevolgd door een weeknummer en eventueel het jaar (Ma25 of ma25 duidt bijvoorbeeld op maandag in week 25).</span><span class="sxs-lookup"><span data-stu-id="7b076-208">You can also enter a date as a weekday followed by a week number and, optionally, a year (for example, Mon25 or mon25 means Monday in week 25).</span></span>  

<span data-ttu-id="7b076-209">U kunt in plaats van een specifieke datum ook een van deze codes invoeren.</span><span class="sxs-lookup"><span data-stu-id="7b076-209">Instead of entering a specific date, you can enter one of these codes.</span></span>  

|<span data-ttu-id="7b076-210">Code</span><span class="sxs-lookup"><span data-stu-id="7b076-210">Code</span></span>|<span data-ttu-id="7b076-211">Resultaat</span><span class="sxs-lookup"><span data-stu-id="7b076-211">Result</span></span>|  
|--------------|----------------|  
|<span data-ttu-id="7b076-212">h</span><span class="sxs-lookup"><span data-stu-id="7b076-212">t</span></span>|<span data-ttu-id="7b076-213">Dit is de datum van vandaag (de systeemdatum voor de computer).</span><span class="sxs-lookup"><span data-stu-id="7b076-213">This specifies today's date (the system date for the computer).</span></span>|  
|<span data-ttu-id="7b076-214">p</span><span class="sxs-lookup"><span data-stu-id="7b076-214">p</span></span>|<span data-ttu-id="7b076-215">Hiermee geeft u een boekhoudingsperiode op, waarbij `p` de eerste boekhoudingsperiode is, `p2` de tweede boekhoudingsperiode is, enzovoort.</span><span class="sxs-lookup"><span data-stu-id="7b076-215">This specifies an accounting period´, where `p`means the first accounting period, `p2` means the second accountin period, and so on.</span></span> |
|<span data-ttu-id="7b076-216">w</span><span class="sxs-lookup"><span data-stu-id="7b076-216">w</span></span>|<span data-ttu-id="7b076-217">Dit is de werkdatum die is ingesteld in de toepassing.</span><span class="sxs-lookup"><span data-stu-id="7b076-217">This specifies the work date that is setup in the application.</span></span> <span data-ttu-id="7b076-218">Zie [Basisinstellingen wijzigen](ui-change-basic-settings.md) als u de werkdatum wilt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="7b076-218">To change the work date, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span> <span data-ttu-id="7b076-219">Het gebruik van een werkdatum is handig als u veel transacties hebt met een andere datum dan de huidige.</span><span class="sxs-lookup"><span data-stu-id="7b076-219">You may want to use a work date if you have many transactions with a date other than today's date.</span></span>|
|<span data-ttu-id="7b076-220">l</span><span class="sxs-lookup"><span data-stu-id="7b076-220">c</span></span>|<span data-ttu-id="7b076-221">Hiermee geeft u op dat de datum na `c` een ultimodatum is, bijvoorbeeld `C123101`.</span><span class="sxs-lookup"><span data-stu-id="7b076-221">This specifies that the date after `c`is a closing date, for example `C123101`.</span></span>|  

## <a name="entering-times"></a><span data-ttu-id="7b076-222">Tijden invoeren</span><span class="sxs-lookup"><span data-stu-id="7b076-222">Entering Times</span></span>

<span data-ttu-id="7b076-223">Hoewel het niet vereist is, kunt u bij de invoer van tijden elk willekeurig scheidingsteken tussen de eenheden plaatsen.</span><span class="sxs-lookup"><span data-stu-id="7b076-223">When you enter times, you can insert any separator sign that you want between the units, but it is not required.</span></span> <span data-ttu-id="7b076-224">U hoeft geen minuten, seconden of AM/PM-aanduiding in te voeren.</span><span class="sxs-lookup"><span data-stu-id="7b076-224">You do not have to write minutes, seconds, or AM/PM.</span></span>  

<span data-ttu-id="7b076-225">In de volgende tabel wordt aangegeven op welke manieren u tijden kunt invoeren en hoe de invoer wordt geïnterpreteerd.</span><span class="sxs-lookup"><span data-stu-id="7b076-225">The following table lists the various ways in which times can be entered and how they are interpreted.</span></span>  

|<span data-ttu-id="7b076-226">Post</span><span class="sxs-lookup"><span data-stu-id="7b076-226">Entry</span></span>|<span data-ttu-id="7b076-227">Interpretatie</span><span class="sxs-lookup"><span data-stu-id="7b076-227">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="7b076-228">5</span><span class="sxs-lookup"><span data-stu-id="7b076-228">5</span></span>|<span data-ttu-id="7b076-229">05:00:00</span><span class="sxs-lookup"><span data-stu-id="7b076-229">05:00:00</span></span>|  
|<span data-ttu-id="7b076-230">5:30</span><span class="sxs-lookup"><span data-stu-id="7b076-230">5:30</span></span>|<span data-ttu-id="7b076-231">05:30:00</span><span class="sxs-lookup"><span data-stu-id="7b076-231">05:30:00</span></span>|  
|<span data-ttu-id="7b076-232">0530</span><span class="sxs-lookup"><span data-stu-id="7b076-232">0530</span></span>|<span data-ttu-id="7b076-233">05:30:00</span><span class="sxs-lookup"><span data-stu-id="7b076-233">05:30:00</span></span>|  
|<span data-ttu-id="7b076-234">5:30:5</span><span class="sxs-lookup"><span data-stu-id="7b076-234">5:30:5</span></span>|<span data-ttu-id="7b076-235">05:30:05</span><span class="sxs-lookup"><span data-stu-id="7b076-235">05:30:05</span></span>|  
|<span data-ttu-id="7b076-236">053005</span><span class="sxs-lookup"><span data-stu-id="7b076-236">053005</span></span>|<span data-ttu-id="7b076-237">05:30:05</span><span class="sxs-lookup"><span data-stu-id="7b076-237">05:30:05</span></span>|  
|<span data-ttu-id="7b076-238">5:30:5.50</span><span class="sxs-lookup"><span data-stu-id="7b076-238">5:30:5,50</span></span>|<span data-ttu-id="7b076-239">05:30:05,5</span><span class="sxs-lookup"><span data-stu-id="7b076-239">05:30:05.5</span></span>|  
|<span data-ttu-id="7b076-240">053005050</span><span class="sxs-lookup"><span data-stu-id="7b076-240">053005050</span></span>|<span data-ttu-id="7b076-241">05:30:05.05</span><span class="sxs-lookup"><span data-stu-id="7b076-241">05:30:05.05</span></span>|  

 <span data-ttu-id="7b076-242">Als u geen scheidingsteken invoert, moet u twee cijfers invoeren voor elke eenheid.</span><span class="sxs-lookup"><span data-stu-id="7b076-242">You must enter two digits for each unit of time if you do not enter a separator.</span></span>  

## <a name="entering-datetimes"></a><span data-ttu-id="7b076-243">Datum/tijd invoeren</span><span class="sxs-lookup"><span data-stu-id="7b076-243">Entering Datetimes</span></span>

<span data-ttu-id="7b076-244">Wanneer u datum/tijd invoert, moet u een spatie plaatsen tussen de datum en de tijd.</span><span class="sxs-lookup"><span data-stu-id="7b076-244">When you enter datetimes you must enter a space between the date and the time.</span></span>  

<span data-ttu-id="7b076-245">In de volgende tabel wordt aangegeven op welke manier u de datum/tijd kunt invoeren en hoe de verschillende manieren worden geïnterpreteerd.</span><span class="sxs-lookup"><span data-stu-id="7b076-245">The following table lists the various ways in which you can enter datetimes and how they are interpreted.</span></span>  

|<span data-ttu-id="7b076-246">Post</span><span class="sxs-lookup"><span data-stu-id="7b076-246">Entry</span></span>|<span data-ttu-id="7b076-247">Interpretatie</span><span class="sxs-lookup"><span data-stu-id="7b076-247">Interpretation</span></span>|  
|---------------|------------------------|  
|<span data-ttu-id="7b076-248">131202 132455</span><span class="sxs-lookup"><span data-stu-id="7b076-248">131202 132455</span></span>|<span data-ttu-id="7b076-249">13-12-02 13:24:55</span><span class="sxs-lookup"><span data-stu-id="7b076-249">13-12-02 13:24:55</span></span>|  
|<span data-ttu-id="7b076-250">1-12-02 10</span><span class="sxs-lookup"><span data-stu-id="7b076-250">1-12-02 10</span></span>|<span data-ttu-id="7b076-251">01-12-02 10:00:00</span><span class="sxs-lookup"><span data-stu-id="7b076-251">01-12-02 10:00:00</span></span>|  
|<span data-ttu-id="7b076-252">1.12.02 5</span><span class="sxs-lookup"><span data-stu-id="7b076-252">1.12.02 5</span></span>|<span data-ttu-id="7b076-253">01-12-02 05:00:00</span><span class="sxs-lookup"><span data-stu-id="7b076-253">01-12-02 05:00:00</span></span>|  
|<span data-ttu-id="7b076-254">1.12.02</span><span class="sxs-lookup"><span data-stu-id="7b076-254">1.12.02</span></span>|<span data-ttu-id="7b076-255">01-12-02 00:00:00</span><span class="sxs-lookup"><span data-stu-id="7b076-255">01-12-02 00:00:00</span></span>|  
|<span data-ttu-id="7b076-256">11 12</span><span class="sxs-lookup"><span data-stu-id="7b076-256">11 12</span></span>|<span data-ttu-id="7b076-257">11-huidige maand-huidig jaar 12:00:00</span><span class="sxs-lookup"><span data-stu-id="7b076-257">11-current month-current year 12:00:00</span></span>|  
|<span data-ttu-id="7b076-258">1112 12</span><span class="sxs-lookup"><span data-stu-id="7b076-258">1112 12</span></span>|<span data-ttu-id="7b076-259">11-12-huidig jaar 12:00:00</span><span class="sxs-lookup"><span data-stu-id="7b076-259">11-12-current year 12:00:00</span></span>|  
|<span data-ttu-id="7b076-260">h of huidige datum</span><span class="sxs-lookup"><span data-stu-id="7b076-260">t or today</span></span>|<span data-ttu-id="7b076-261">huidige datum 00:00:00</span><span class="sxs-lookup"><span data-stu-id="7b076-261">today's date 00:00:00</span></span>|  
|<span data-ttu-id="7b076-262">h tijd</span><span class="sxs-lookup"><span data-stu-id="7b076-262">t time</span></span>|<span data-ttu-id="7b076-263">huidige datum werkelijke tijd</span><span class="sxs-lookup"><span data-stu-id="7b076-263">today's date actual time</span></span>|  
|<span data-ttu-id="7b076-264">h 10:30</span><span class="sxs-lookup"><span data-stu-id="7b076-264">t 10:30</span></span>|<span data-ttu-id="7b076-265">huidige datum 10:30:00</span><span class="sxs-lookup"><span data-stu-id="7b076-265">today's date 10:30:00</span></span>|  
|<span data-ttu-id="7b076-266">h 3:3:3</span><span class="sxs-lookup"><span data-stu-id="7b076-266">t 3:3:3</span></span>|<span data-ttu-id="7b076-267">huidige datum 03:03:03</span><span class="sxs-lookup"><span data-stu-id="7b076-267">today's date 03:03:03</span></span>|  
|<span data-ttu-id="7b076-268">w of werkdatum</span><span class="sxs-lookup"><span data-stu-id="7b076-268">w or workdate</span></span>|<span data-ttu-id="7b076-269">de werkdatum 00:00:00</span><span class="sxs-lookup"><span data-stu-id="7b076-269">the working date 00:00:00</span></span>|  
|<span data-ttu-id="7b076-270">ma of maandag</span><span class="sxs-lookup"><span data-stu-id="7b076-270">m or Monday</span></span>|<span data-ttu-id="7b076-271">Maandag van de huidige week 00:00:00</span><span class="sxs-lookup"><span data-stu-id="7b076-271">Monday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="7b076-272">di of dinsdag</span><span class="sxs-lookup"><span data-stu-id="7b076-272">tu or Tuesday</span></span>|<span data-ttu-id="7b076-273">Dinsdag van de huidige week 00:00:00</span><span class="sxs-lookup"><span data-stu-id="7b076-273">Tuesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="7b076-274">wo of woensdag</span><span class="sxs-lookup"><span data-stu-id="7b076-274">we or Wednesday</span></span>|<span data-ttu-id="7b076-275">Woensdag van de huidige week 00:00:00</span><span class="sxs-lookup"><span data-stu-id="7b076-275">Wednesday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="7b076-276">do of donderdag</span><span class="sxs-lookup"><span data-stu-id="7b076-276">th or Thursday</span></span>|<span data-ttu-id="7b076-277">Donderdag van de huidige week 00:00:00</span><span class="sxs-lookup"><span data-stu-id="7b076-277">Thursday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="7b076-278">vr of vrijdag</span><span class="sxs-lookup"><span data-stu-id="7b076-278">f or Friday</span></span>|<span data-ttu-id="7b076-279">Vrijdag van de huidige week 00:00:00</span><span class="sxs-lookup"><span data-stu-id="7b076-279">Friday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="7b076-280">za of zaterdag</span><span class="sxs-lookup"><span data-stu-id="7b076-280">s or Saturday</span></span>|<span data-ttu-id="7b076-281">Zaterdag van de huidige week 00:00:00</span><span class="sxs-lookup"><span data-stu-id="7b076-281">Saturday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="7b076-282">zo of zondag</span><span class="sxs-lookup"><span data-stu-id="7b076-282">su or Sunday</span></span>|<span data-ttu-id="7b076-283">Zondag van de huidige week 00:00:00</span><span class="sxs-lookup"><span data-stu-id="7b076-283">Sunday of the current week 00:00:00</span></span>|  
|<span data-ttu-id="7b076-284">di 10:30</span><span class="sxs-lookup"><span data-stu-id="7b076-284">tu 10:30</span></span>|<span data-ttu-id="7b076-285">Dinsdag van de huidige week 10:30:00</span><span class="sxs-lookup"><span data-stu-id="7b076-285">Tuesday of the current week 10:30:00</span></span>|  
|<span data-ttu-id="7b076-286">di 3:3:3</span><span class="sxs-lookup"><span data-stu-id="7b076-286">tu 3:3:3</span></span>|<span data-ttu-id="7b076-287">Dinsdag van de huidige week 03:03:03</span><span class="sxs-lookup"><span data-stu-id="7b076-287">Tuesday of the current week 03:03:03</span></span>|  

## <a name="entering-duration"></a><span data-ttu-id="7b076-288">Duur invoeren</span><span class="sxs-lookup"><span data-stu-id="7b076-288">Entering Duration</span></span>

<span data-ttu-id="7b076-289">De duur moet worden ingevoerd als een getal gevolgd door de eenheid.</span><span class="sxs-lookup"><span data-stu-id="7b076-289">You enter a duration as a number followed by its unit of measure.</span></span>  

<span data-ttu-id="7b076-290">Hier volgen enkele voorbeelden.</span><span class="sxs-lookup"><span data-stu-id="7b076-290">Here are some examples.</span></span>  

|<span data-ttu-id="7b076-291">Duur</span><span class="sxs-lookup"><span data-stu-id="7b076-291">Duration</span></span>|<span data-ttu-id="7b076-292">Eenheid\*\*</span><span class="sxs-lookup"><span data-stu-id="7b076-292">Unit of measure\*\*</span></span>|  
|------------------|-------------------------|  
|<span data-ttu-id="7b076-293">2u</span><span class="sxs-lookup"><span data-stu-id="7b076-293">2h</span></span>|<span data-ttu-id="7b076-294">2 uur</span><span class="sxs-lookup"><span data-stu-id="7b076-294">2 hrs</span></span>|  
|<span data-ttu-id="7b076-295">6u 30 m</span><span class="sxs-lookup"><span data-stu-id="7b076-295">6h 30 m</span></span>|<span data-ttu-id="7b076-296">6 uur en 30 minuten</span><span class="sxs-lookup"><span data-stu-id="7b076-296">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="7b076-297">6,5u</span><span class="sxs-lookup"><span data-stu-id="7b076-297">6.5h</span></span>|<span data-ttu-id="7b076-298">6 uur en 30 minuten</span><span class="sxs-lookup"><span data-stu-id="7b076-298">6 hrs 30 mins</span></span>|  
|<span data-ttu-id="7b076-299">90m</span><span class="sxs-lookup"><span data-stu-id="7b076-299">90m</span></span>|<span data-ttu-id="7b076-300">1 uur en 30 minuten</span><span class="sxs-lookup"><span data-stu-id="7b076-300">1 hr 30 mins</span></span>|  
|<span data-ttu-id="7b076-301">2d 6u 30m</span><span class="sxs-lookup"><span data-stu-id="7b076-301">2d 6h 30m</span></span>|<span data-ttu-id="7b076-302">2 dagen, 6 uur en 30 minuten</span><span class="sxs-lookup"><span data-stu-id="7b076-302">2 days 6 hrs 30 mins</span></span>|  
|<span data-ttu-id="7b076-303">2d 6u 30m 56s 600ms</span><span class="sxs-lookup"><span data-stu-id="7b076-303">2d 6h 30m 56s 600ms</span></span>|<span data-ttu-id="7b076-304">2 dagen, 6 uur, 30 minuten, 56 seconden en 600 milliseconden</span><span class="sxs-lookup"><span data-stu-id="7b076-304">2 days 6 hrs 30 mins 56 secs 600 msecs</span></span>|  

 <span data-ttu-id="7b076-305">Als u een getal invoert, wordt het getal automatisch omgezet naar een duur.</span><span class="sxs-lookup"><span data-stu-id="7b076-305">You can also enter a number and it is automatically converted to a duration.</span></span> <span data-ttu-id="7b076-306">Dit gebeurt op basis van de standaardeenheid die in het veld Duur is ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="7b076-306">The number you enter is converted according to the default unit of measure that has been specified for the duration field.</span></span>  

 <span data-ttu-id="7b076-307">Als u wilt nagaan welke eenheid wordt gebruikt in het veld Duur, voert u een getal in en bekijkt u in welke eenheid het getal wordt omgezet.</span><span class="sxs-lookup"><span data-stu-id="7b076-307">To see what unit of measure is being used in a duration field, enter a number and see which unit of measure it is converted to.</span></span>  

 <span data-ttu-id="7b076-308">Het getal 5 wordt omgezet in 5 uur, als de eenheid uit uren bestaat.</span><span class="sxs-lookup"><span data-stu-id="7b076-308">The number 5 is converted to 5 hrs, if the unit of measure is hours.</span></span>  

<!--OnPrem  ##  <a name="BKMK_SettingDateRanges"></a> Setting Date Ranges  
 You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges.  

|**Meaning**|**Sample expression**|**Entries included**|  
|-----------------|---------------------------|--------------------------|  
|**Equal to**|12 15 00|Only those posted on 12 15 00.|  
|**Interval**|12 15 00..01 15 01<br /><br /> ..12 15 00|Those posted on dates between and including 12 15 00 and 01 15 01.<br /><br /> Those posted on 12 15 00 or earlier.|  
|**Either/or**|12 15 00&#124;12 16 00|Those posted on either 12 15 00 or 12 16 00. If there are entries posted on both days, they will all be displayed.|  

 You can also combine the various format types.  

|**Sample expression**|**Entries included**|  
|---------------------------|--------------------------|  
|12 15 00&#124;12 01 00..12 10 00|Entries posted either on 12 15 00 or on dates between and including 12 01 00 and 12 10 00.|  
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|

## Using Date Formulas

 A date formula is a short, abbreviated combination of letters and numbers that specifies how to calculate dates. You can enter date formulas in various date calculation fields and in recurring frequency fields in recurring journals.  

> [!NOTE]  
>  In all data formula fields, one day is automatically included to cover today as the day when the period starts. Accordingly, if you enter 1W, for example, then the period is actually eight days because today is included. To specify a period of seven days (one true week) including the period starting date, then you must enter 6D or 1W-1D.  

 Here are some examples of how date formulas can be used:  

-   The date formula in the recurring frequency field in recurring journals determines how often the entry on the journal line will be posted.  

-   The date formula in the Grace Period field for a specified reminder level determines the period of time that must pass from the due date (or from the date of the previous reminder) before a reminder will be created.  

-   The date formula in the Due Date Calculation field determines how to calculate the due date on the reminder.  

 The date calculation formula can contain a maximum of 20 characters, both numbers and letters. You can use the following letters, which are abbreviations for time specifications.  

|||  
|-|-|  
|C|Current|  
|D|Day(s)|  
|W|Week(s)|  
|M|Month(s)|  
|Q|Quarter(s)|  
|Y|Year(s)|  

 You can construct a date formula in three ways.  

 The following example shows how current plus a time unit.  

|||  
|-|-|  
|CW|Current week|  
|CM|Current month|  

 The following example shows how a number and a time unit. A number cannot be larger than 9999.  

|||  
|-|-|  
|10D|10 days from today|  
|2W|2 weeks from today|  

 The following example shows how a time unit and a number.  

|||  
|-|-|  
|D10|The next 10th day of a month|  
|WD4|The next 4th day of a week (Thursday)|  

 The following example shows how you can combine these three forms as needed.  

|||  
|-|-|  
|CM+10D|Current month + 10 days|  

 The following example shows how you can use a minus sign to indicate a date in the past.  

|||  
|-|-|  
|-1Y|1 year ago from today|

[!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->

## <a name="see-also"></a><span data-ttu-id="7b076-309">Zie ook</span><span class="sxs-lookup"><span data-stu-id="7b076-309">See Also</span></span>  
 [<span data-ttu-id="7b076-310">Lijsten sorteren, doorzoeken en filteren</span><span class="sxs-lookup"><span data-stu-id="7b076-310">Sorting, Searching, and Filtering Lists</span></span>](ui-enter-criteria-filters.md)  
 <span data-ttu-id="7b076-311">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7b076-311">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
