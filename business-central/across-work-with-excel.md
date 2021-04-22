---
title: Weergeven en bewerken in Excel vanuit Business Central
description: Leer hoe u de pagina's in Microsoft Excel opent vanuit Business Central voor betere gegevensanalyse.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: 7e3abf36444c4701229ffaac7ceade11bb1879cc
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5786944"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="6bfd4-103">Weergeven en bewerken in Excel vanuit Business Central</span><span class="sxs-lookup"><span data-stu-id="6bfd4-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="6bfd4-104">Met pagina's die een lijst met records in rijen en kolommen weergeven, zoals een lijst met klanten, verkooporders of facturen, kunt u ook de records weergeven met Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="6bfd4-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="6bfd4-105">U hebt hiervoor twee opties.</span><span class="sxs-lookup"><span data-stu-id="6bfd4-105">To do this, you have two options.</span></span> <span data-ttu-id="6bfd4-106">U kunt de actie **Openen in Excel** of de actie **Bewerken in Excel** op de pagina selecteren.</span><span class="sxs-lookup"><span data-stu-id="6bfd4-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="6bfd4-107">Dit zijn de verschillen tussen de twee acties:</span><span class="sxs-lookup"><span data-stu-id="6bfd4-107">The differences between the two actions are as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="6bfd4-108">Openen in Excel</span><span class="sxs-lookup"><span data-stu-id="6bfd4-108">Open in Excel</span></span>

- <span data-ttu-id="6bfd4-109">Met deze actie houdt Excel rekening met alle filters op de pagina waarmee de weergegeven records worden beperkt.</span><span class="sxs-lookup"><span data-stu-id="6bfd4-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="6bfd4-110">De Excel-werkmap zal dezelfde rijen en kolommen bevatten die worden weergegeven op de pagina in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="6bfd4-110">The Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

- <span data-ttu-id="6bfd4-111">U kunt wijzigingen in de records aanbrengen in Excel, maar u kunt de wijzigingen niet terug publiceren naar [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="6bfd4-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="6bfd4-112">U kunt de wijzigingen alleen opslaan in het Excel-bestand op uw computer.</span><span class="sxs-lookup"><span data-stu-id="6bfd4-112">You can only save the changes to Excel file on your computer.</span></span>

- <span data-ttu-id="6bfd4-113">Deze actie werkt zowel onder Windows als MacOS.</span><span class="sxs-lookup"><span data-stu-id="6bfd4-113">This action works on both on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="6bfd4-114">Voor [!INCLUDE[prod_short](includes/prod_short.md)] on-premises is de actie **Openen in Excel** standaard beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="6bfd4-114">For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="6bfd4-115">Als u echter [!INCLUDE[prod_short](includes/prod_short.md)] on-premises instelt om gegevens in Excel te bewerken, wordt de actie **Openen in Excel** vervangen door de actie **Bewerken in Excel**.</span><span class="sxs-lookup"><span data-stu-id="6bfd4-115">However, if you set up [!INCLUDE[prod_short](includes/prod_short.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="6bfd4-116">Bewerken in Excel</span><span class="sxs-lookup"><span data-stu-id="6bfd4-116">Edit in Excel</span></span>

- <span data-ttu-id="6bfd4-117">Met deze actie respecteert Excel de meeste filters op de pagina die het aantal weergegeven records beperken, dus de Excel-werkmap bevat bijna dezelfde records en kolommen.</span><span class="sxs-lookup"><span data-stu-id="6bfd4-117">With this action, Excel respects most filters on the page that limit the records shown, so the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="6bfd4-118">Het voordeel van de actie **Bewerken in Excel** is dat u er wijzigingen in records in Excel mee kunt aanbrengen en de wijzigingen weer naar [!INCLUDE[prod_short](includes/prod_short.md)] kunt publiceren.</span><span class="sxs-lookup"><span data-stu-id="6bfd4-118">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

- <span data-ttu-id="6bfd4-119">Dit werkt alleen onder Windows, niet onder MacOS.</span><span class="sxs-lookup"><span data-stu-id="6bfd4-119">It only works on Windows; not macOS.</span></span>

- <span data-ttu-id="6bfd4-120">U kunt het bedrijf waarmee u werkt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="6bfd4-120">You can switch the company that you are working with.</span></span> <span data-ttu-id="6bfd4-121">Als u van bedrijf wilt veranderen, selecteert u het pictogram **Opties** ![Opties voor Excel-invoegtoepassingen](media/cogwheel.png "Opties van Excel-invoegtoepassing") in het Excel-invoegtoepassingsvenster en selecteer vervolgens het bedrijf in het veld **Bedrijf**.</span><span class="sxs-lookup"><span data-stu-id="6bfd4-121">To switch company, select the **Options** icon ![Excel add-in options](media/cogwheel.png "Excel add-in options") in the Excel Add-in pane, then select the company from the **Company** field.</span></span>  

    > [!IMPORTANT]
    > <span data-ttu-id="6bfd4-122">Zorg er bij het veranderen van bedrijf voor dat het veld **Omgeving** niet leeg is.</span><span class="sxs-lookup"><span data-stu-id="6bfd4-122">When changing the company, make sure that the **Environment** field is not empty.</span></span> <span data-ttu-id="6bfd4-123">Als dat zo is, stel het dan in op een van de beschikbare opties; anders werkt de invoegtoepassing niet correct.</span><span class="sxs-lookup"><span data-stu-id="6bfd4-123">If it is, then set it to one of the available options; otherwise, the add-in will not work correctly.</span></span>  

<span data-ttu-id="6bfd4-124">Als u wijzigingen aanbrengt in de invoegtoepassing, moet u deze opnieuw laden om de verbinding bij te werken.</span><span class="sxs-lookup"><span data-stu-id="6bfd4-124">If you make changes to the add-in, you must reload it to update the connection.</span></span> <span data-ttu-id="6bfd4-125">Gebruik om opnieuw te laden het menu ![menu van Excel-invoegtoepassing](media/excel-addin-menu.png "Menu van Excel-invoegtoepassing") in de rechterbovenhoek van de invoegtoepassing.</span><span class="sxs-lookup"><span data-stu-id="6bfd4-125">To reload, use the ![Excel add-in menu](media/excel-addin-menu.png "Excel add-in menu") menu in the top-right corner of the add-in.</span></span> <span data-ttu-id="6bfd4-126">Neem contact op met uw beheerder als u de invoegtoepassing niet kunt laden.</span><span class="sxs-lookup"><span data-stu-id="6bfd4-126">If you cannot load the add-in, talk to your administrator.</span></span> <span data-ttu-id="6bfd4-127">Zie als u de beheerder bent [De Excel-invoegtoepassing instellen om Business Central-gegevens te bewerken](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="6bfd4-127">If you are the administrator, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

> [!NOTE]
> <span data-ttu-id="6bfd4-128">Voor [!INCLUDE[prod_short](includes/prod_short.md)] on-premises is de actie **Bewerken in Excel** alleen beschikbaar als de Excel-invoegtoepassing door uw systeembeheerder is geconfigureerd, en alleen beschikbaar voor de webclient.</span><span class="sxs-lookup"><span data-stu-id="6bfd4-128">For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator, and only available for the Web client.</span></span> <span data-ttu-id="6bfd4-129">Zie voor systeembeheerders [De Excel-invoegtoepassing instellen om Business Central-gegevens te bewerken](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin) voor meer informatie over de installatie van de Excel-invoegtoepassing.</span><span class="sxs-lookup"><span data-stu-id="6bfd4-129">For administrators, if you want to learn how to install the Excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="6bfd4-130">Zie de verschillen tussen de opties</span><span class="sxs-lookup"><span data-stu-id="6bfd4-130">See the differences between the options</span></span>
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="6bfd4-131">Zie Gerelateerde training op [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="6bfd4-131">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="6bfd4-132">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6bfd4-132">See Also</span></span>

[<span data-ttu-id="6bfd4-133">Financiële overzichten analyseren in Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="6bfd4-133">Analyzing Financial Statements in Microsoft Excel</span></span>](finance-analyze-excel.md)  
[<span data-ttu-id="6bfd4-134">Werken met Business Central</span><span class="sxs-lookup"><span data-stu-id="6bfd4-134">Working with Business Central</span></span>](ui-work-product.md)  
[<span data-ttu-id="6bfd4-135">Verbeteringen aan Excel-integratie in releasewave 2 van 2019</span><span class="sxs-lookup"><span data-stu-id="6bfd4-135">Enhancements to Excel integration in 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration)  


[!INCLUDE[footer-include](includes/footer-banner.md)]