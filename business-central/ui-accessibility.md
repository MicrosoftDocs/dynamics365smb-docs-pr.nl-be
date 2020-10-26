---
title: Ondersteunende functies
description: Sneltoetsen en andere ondersteunende functies.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 69b1dccc88750dca2e2f406554db34357bd8d6db
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912783"
---
# <a name="accessibility-and-keyboard-shortcuts"></a><span data-ttu-id="ffecc-103">Toegankelijkheid en sneltoetsen</span><span class="sxs-lookup"><span data-stu-id="ffecc-103">Accessibility and Keyboard Shortcuts</span></span>
<span data-ttu-id="ffecc-104">Dit onderwerp bevat informatie over de functies die [!INCLUDE[d365fin](includes/d365fin_md.md)] toegankelijk maken voor mensen met een handicap.</span><span class="sxs-lookup"><span data-stu-id="ffecc-104">This topic provides information about the features that make [!INCLUDE[d365fin](includes/d365fin_md.md)] readily available to people with disabilities.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="ffecc-105">ondersteunt de volgende toegankelijkheidsfuncties:</span><span class="sxs-lookup"><span data-stu-id="ffecc-105">supports the following accessibility features:</span></span>  

-   <span data-ttu-id="ffecc-106">Sneltoetsen</span><span class="sxs-lookup"><span data-stu-id="ffecc-106">Keyboard shortcuts</span></span>

    <span data-ttu-id="ffecc-107">Zie voor meer informatie [Toetsenbordsneltoetsen](keyboard-shortcuts.md)</span><span class="sxs-lookup"><span data-stu-id="ffecc-107">For more information, see [Keyboard Shortcuts](keyboard-shortcuts.md)</span></span>

-   <span data-ttu-id="ffecc-108">Navigatie</span><span class="sxs-lookup"><span data-stu-id="ffecc-108">Navigation</span></span>  

-   <span data-ttu-id="ffecc-109">Koppen</span><span class="sxs-lookup"><span data-stu-id="ffecc-109">Headings</span></span>  

-   <span data-ttu-id="ffecc-110">Alternatieve tekst voor afbeeldingen en koppelingen</span><span class="sxs-lookup"><span data-stu-id="ffecc-110">Alternative text for images and links</span></span>  

-   <span data-ttu-id="ffecc-111">Ondersteuning voor algemene ondersteunende technologieën</span><span class="sxs-lookup"><span data-stu-id="ffecc-111">Support for common assistive technologies</span></span>  

<!-- moved to separate article
##  <a name="Keyboard"></a> Keyboard Shortcuts in the browser
 [!INCLUDE[d365fin](includes/d365fin_md.md)] supports the keyboard shortcuts that are supported by most web browsers. The keyboard shortcuts described here refer to the U.S. keyboard layout. The layout of the keys on other keyboards may not correspond exactly to the keys on a U.S. keyboard.  

|To do this|Press|  
|----------------|-----------|  
|To move focus to the next or previous control or element on a page, such as buttons, fields, or items in a list.|Tab, Shift+Tab|  
|To enable or access the element or control that is in focus.|Enter|  
|To scroll items up and down in a list.|Up Arrow, Down Arrow|  
|To scroll columns of an item left and right in a list.|Left Arrow, Right Arrow|  
|To open a drop-down list or look up a value for a field.|Alt+Down Arrow|  
|To move focus to the next element outside the list.|Ctrl + Enter|  
|To see the transactions that resulted in a calculated value in a field.|Alt+Right Arrow|  

-->

##  <a name="navigation"></a><a name="Navigation"></a> <span data-ttu-id="ffecc-112">Navigatie</span><span class="sxs-lookup"><span data-stu-id="ffecc-112">Navigation</span></span>  
 <span data-ttu-id="ffecc-113">Met het toetsenbord kunt u navigeren tussen de tabbladen en acties in het lint, elementen op de navigatiebalk en andere besturingselementen in [!INCLUDE[d365fin](includes/d365fin_md.md)]-pagina's en -rapporten.</span><span class="sxs-lookup"><span data-stu-id="ffecc-113">You can navigate between the tabs and actions in the ribbon, elements in the navigation bar, and other controls on [!INCLUDE[d365fin](includes/d365fin_md.md)] pages and reports using the keyboard.</span></span> <span data-ttu-id="ffecc-114">Als u de focus wilt verplaatsen naar het volgende tabblad, de volgende actie of het volgende besturingselement, drukt u op Tab.</span><span class="sxs-lookup"><span data-stu-id="ffecc-114">To move the focus from one tab, action, or control to another, press the Tab key to move forward.</span></span> <span data-ttu-id="ffecc-115">Druk op Shift+Tab om naar het vorige tabblad, de vorige actie of het vorige besturingselement te gaan.</span><span class="sxs-lookup"><span data-stu-id="ffecc-115">Press Shift+Tab to move backward.</span></span>  

 <span data-ttu-id="ffecc-116">Met Tab kunt u ook schakelen tussen de hoofdbrowserpagina en dialoogvensters waarin bijvoorbeeld om bevestiging wordt gevraagd of de aanmeldingspagina.</span><span class="sxs-lookup"><span data-stu-id="ffecc-116">By using the tab order, you can also switch between the main browser page and dialog boxes that request confirmation, for example, or the login page.</span></span>  

##  <a name="headings"></a><a name="Headings"></a> <span data-ttu-id="ffecc-117">Koppen</span><span class="sxs-lookup"><span data-stu-id="ffecc-117">Headings</span></span>  
 <span data-ttu-id="ffecc-118">In de HTML-bron voor [!INCLUDE[d365fin](includes/d365fin_md.md)]-inhoud worden tags gebruikt om gebruikers van ondersteunende technologie te helpen de structuur en inhoud van de pagina te begrijpen.</span><span class="sxs-lookup"><span data-stu-id="ffecc-118">The HTML source for [!INCLUDE[d365fin](includes/d365fin_md.md)] content uses tags to help users of assistive technology to understand the structure and content of the page.</span></span> <span data-ttu-id="ffecc-119">Op pagina's met lijsten worden de kolommen bijvoorbeeld gedefinieerd in TH-tags en de kolomkoppen worden ingesteld met het kenmerk TITLE in de tag.</span><span class="sxs-lookup"><span data-stu-id="ffecc-119">For example, on list pages, the columns are defined in TH tags and the column headings are set with TITLE attribute inside the tag.</span></span> <span data-ttu-id="ffecc-120">Bijschriften voor elementen, zoals sneltabbladen, feitenblokken en velden, zijn opgenomen in koptags (H1, H2, H3 en H4).</span><span class="sxs-lookup"><span data-stu-id="ffecc-120">Captions for elements, such as FastTabs, FactBoxes, and fields are included in heading tags (H1, H2, H3, and H4).</span></span>  

##  <a name="image-and-links"></a><a name="Images"></a> <span data-ttu-id="ffecc-121">Afbeelding en koppelingen</span><span class="sxs-lookup"><span data-stu-id="ffecc-121">Image and Links</span></span>  
 <span data-ttu-id="ffecc-122">Een omschrijvende tekst voor afbeeldingen wordt ingesteld met het kenmerk ALT in de IMG-tag.</span><span class="sxs-lookup"><span data-stu-id="ffecc-122">A descriptive text for images is set with the ALT attribute inside the IMG tag.</span></span> <span data-ttu-id="ffecc-123">Een omschrijvende tekst voor hyperlinks wordt ingesteld met het titelkenmerk in de A-tag.</span><span class="sxs-lookup"><span data-stu-id="ffecc-123">A descriptive text for hyperlinks is set with the title attribute inside the A tag.</span></span>  

##  <a name="assistive-technologies"></a><a name="AssistiveTech"></a> <span data-ttu-id="ffecc-124">Ondersteunende technologieën</span><span class="sxs-lookup"><span data-stu-id="ffecc-124">Assistive Technologies</span></span>  
[!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="ffecc-125">ondersteunt meerdere ondersteunende technologieën, zoals hoog contrast, schermlezers en spraakherkenningssoftware.</span><span class="sxs-lookup"><span data-stu-id="ffecc-125">supports various assistive technologies, such as high contrast, screen readers, and voice recognition software.</span></span> <span data-ttu-id="ffecc-126">Sommige ondersteunende technologieën werken mogelijk niet goed met bepaalde elementen op [!INCLUDE[d365fin](includes/d365fin_md.md)]-pagina's.</span><span class="sxs-lookup"><span data-stu-id="ffecc-126">Some assistive technologies may not work well with certain elements in [!INCLUDE[d365fin](includes/d365fin_md.md)] pages.</span></span>  

## <a name="for-more-accessibility-information"></a><span data-ttu-id="ffecc-127">Meer informatie over toegankelijkheid</span><span class="sxs-lookup"><span data-stu-id="ffecc-127">For more accessibility information</span></span>  
<span data-ttu-id="ffecc-128">Meer informatie over toegankelijkheid voor Microsoft-producten en ondersteunende technologieën vindt u op de site [Microsoft Accessibility](https://go.microsoft.com/fwlink/?LinkId=262160).</span><span class="sxs-lookup"><span data-stu-id="ffecc-128">You can find additional information about accessibility with Microsoft products and assistive technologies on the [Microsoft Accessibility](https://go.microsoft.com/fwlink/?LinkId=262160) site.</span></span>

## <a name="see-also"></a><span data-ttu-id="ffecc-129">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ffecc-129">See Also</span></span>
[<span data-ttu-id="ffecc-130">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="ffecc-130">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="ffecc-131">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ffecc-131">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="ffecc-132">Veelgestelde vragen</span><span class="sxs-lookup"><span data-stu-id="ffecc-132">Frequently Asked Questions</span></span>](across-faq.md)  
