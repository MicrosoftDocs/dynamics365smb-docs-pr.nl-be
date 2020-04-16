---
title: Weergeven en bewerken in Excel vanuit Business Central | Microsoft Docs
description: Leer hoe u de pagina's in Microsoft Excel opent vanuit Business Central voor betere gegevensanalyse.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: accountant, accounting, financial report
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 2c6600ac7fe9f6e0aa44554883209039faabbd99
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187520"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="fbb0c-103">Weergeven en bewerken in Excel vanuit Business Central</span><span class="sxs-lookup"><span data-stu-id="fbb0c-103">Viewing and Editing in Excel From Business Central</span></span>

<span data-ttu-id="fbb0c-104">Met pagina's die een lijst met records in rijen en kolommen weergeven, zoals een lijst met klanten, verkooporders of facturen, kunt u ook de records weergeven met Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="fbb0c-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="fbb0c-105">U hebt hiervoor twee opties.</span><span class="sxs-lookup"><span data-stu-id="fbb0c-105">To do this, you have two options.</span></span> <span data-ttu-id="fbb0c-106">U kunt de actie **Openen in Excel** of de actie **Bewerken in Excel** op de pagina selecteren.</span><span class="sxs-lookup"><span data-stu-id="fbb0c-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="fbb0c-107">Dit zijn de verschillen tussen de twee methoden:</span><span class="sxs-lookup"><span data-stu-id="fbb0c-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="fbb0c-108">Openen in Excel</span><span class="sxs-lookup"><span data-stu-id="fbb0c-108">Open in Excel</span></span>

- <span data-ttu-id="fbb0c-109">Met deze actie houdt Excel rekening met alle filters op de pagina waarmee de weergegeven records worden beperkt.</span><span class="sxs-lookup"><span data-stu-id="fbb0c-109">With this action, Excel respects any filters on the page that limit the records shown.</span></span> <span data-ttu-id="fbb0c-110">Dit betekent dat de Excel-werkmap dezelfde rijen en kolommen bevat die worden weergegeven op de pagina in [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="fbb0c-110">This means that the Excel workbook will contain the same rows and columns that appear on the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="fbb0c-111">U kunt wijzigingen in de records aanbrengen in Excel, maar u kunt de wijzigingen niet terug publiceren naar [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="fbb0c-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="fbb0c-112">U kunt de wijzigingen alleen opslaan in het Excel-bestand op uw computer.</span><span class="sxs-lookup"><span data-stu-id="fbb0c-112">You can only save the changes to Excel file on your computer.</span></span>

- <span data-ttu-id="fbb0c-113">Deze actie werkt zowel onder Windows als MacOS.</span><span class="sxs-lookup"><span data-stu-id="fbb0c-113">This action works on both on Windows and macOS.</span></span>

> [!NOTE]
> <span data-ttu-id="fbb0c-114">Voor [!INCLUDE[prodshort](includes/prodshort.md)] on-premises is de actie **Openen in Excel** standaard beschikbaar.</span><span class="sxs-lookup"><span data-stu-id="fbb0c-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is available by default.</span></span> <span data-ttu-id="fbb0c-115">Als u echter [!INCLUDE [prodshort](includes/prodshort.md)] on-premises instelt om gegevens in Excel te bewerken, wordt de actie **Openen in Excel** vervangen door de actie **Bewerken in Excel**.</span><span class="sxs-lookup"><span data-stu-id="fbb0c-115">However, if you set up [!INCLUDE [prodshort](includes/prodshort.md)] on-premises for editing data in Excel, then the **Open in Excel** action is replaced by the **Edit in Excel** action.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="fbb0c-116">Bewerken in Excel</span><span class="sxs-lookup"><span data-stu-id="fbb0c-116">Edit in Excel</span></span>

- <span data-ttu-id="fbb0c-117">Met deze actie houdt Excel rekening met de meeste filters op de pagina waarmee de weergegeven records worden beperkt.</span><span class="sxs-lookup"><span data-stu-id="fbb0c-117">With this action, Excel respects most filters on the page that limit the records shown.</span></span> <span data-ttu-id="fbb0c-118">Dit betekent dat de Excel-werkmap nagenoeg dezelfde records en kolommen bevat.</span><span class="sxs-lookup"><span data-stu-id="fbb0c-118">This means that the Excel workbook will contain almost the same records and columns.</span></span>

- <span data-ttu-id="fbb0c-119">Het voordeel van de actie **Bewerken in Excel** is dat u er wijzigingen in records in Excel mee kunt aanbrengen en de wijzigingen weer naar [!INCLUDE[prodshort](includes/prodshort.md)] kunt publiceren.</span><span class="sxs-lookup"><span data-stu-id="fbb0c-119">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

- <span data-ttu-id="fbb0c-120">Dit werkt alleen onder Windows, niet onder MacOS.</span><span class="sxs-lookup"><span data-stu-id="fbb0c-120">It only works on Windows; not macOS.</span></span>

- <span data-ttu-id="fbb0c-121">U kunt het bedrijf waarmee u werkt wijzigen.</span><span class="sxs-lookup"><span data-stu-id="fbb0c-121">You can switch the company that your are working with.</span></span> <span data-ttu-id="fbb0c-122">Selecteer hiervoor het pictogram **Opties** ![Opties voor Excel-invoegtoepassingen](media/cogwheel.png "Opties van Excel-invoegtoepassing") in het Excel-invoegtoepassingsvenster en selecteer vervolgens het bedrijf in het veld **Bedrijf**.</span><span class="sxs-lookup"><span data-stu-id="fbb0c-122">To do this, select the **Options** icon ![Excel add-in options](media/cogwheel.png "Excel add-in options") in the Excel Add-in pane, then select the company from the **Company** field.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="fbb0c-123">Zorg er bij het veranderen van bedrijf voor dat het veld **Omgeving** niet leeg is.</span><span class="sxs-lookup"><span data-stu-id="fbb0c-123">When changing the company, make sure that the **Environment** field is not empty.</span></span> <span data-ttu-id="fbb0c-124">Als dat zo is, stel het dan in op een van de beschikbare opties; anders werkt de invoegtoepassing niet correct.</span><span class="sxs-lookup"><span data-stu-id="fbb0c-124">If it is, then set it to one of the available options; otherwise, the add-in will not work correctly.</span></span>  

<span data-ttu-id="fbb0c-125">De Excel-invoegtoepassing is verbeterd in releasewave 2 van 2019.</span><span class="sxs-lookup"><span data-stu-id="fbb0c-125">The Excel Add-in was enhanced in 2019 release wave 2.</span></span> <span data-ttu-id="fbb0c-126">Zie [Verbeteringen aan Excel-integratie](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="fbb0c-126">For more information, see [Enhancements to Excel integration](/dynamics365-release-plan/2019wave2/dynamics365-business-central/enhancements-excel-integration).</span></span>

> [!NOTE]
> <span data-ttu-id="fbb0c-127">Voor [!INCLUDE[prodshort](includes/prodshort.md)] on-premises is de actie **Bewerken in Excel** alleen beschikbaar als de Excel-invoegtoepassing door uw systeembeheerder is geconfigureerd, en alleen beschikbaar voor de webclient.</span><span class="sxs-lookup"><span data-stu-id="fbb0c-127">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been configured by your administrator, and only available for the Web client.</span></span> <span data-ttu-id="fbb0c-128">Voor systeembeheerders: Zie [De Excel-invoegtoepassing instellen om Business Central-gegevens te bewerken](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin) voor meer informatie over de installatie van de Excel-invoegtoepassing.</span><span class="sxs-lookup"><span data-stu-id="fbb0c-128">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In for Editing Business Central Data](/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span> <span data-ttu-id="fbb0c-129">Voor [!INCLUDE[prodshort](includes/prodshort.md)] on-premises.</span><span class="sxs-lookup"><span data-stu-id="fbb0c-129">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises.</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="fbb0c-130">Zie de verschillen tussen de opties</span><span class="sxs-lookup"><span data-stu-id="fbb0c-130">See the differences between the options</span></span>
<br><br>  

> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-related-training-at-microsoft-learn"></a><span data-ttu-id="fbb0c-131">Zie Gerelateerde training op [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span><span class="sxs-lookup"><span data-stu-id="fbb0c-131">See Related Training at [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)</span></span>

## <a name="see-also"></a><span data-ttu-id="fbb0c-132">Zie ook</span><span class="sxs-lookup"><span data-stu-id="fbb0c-132">See Also</span></span>
[<span data-ttu-id="fbb0c-133">Werken met Business Central</span><span class="sxs-lookup"><span data-stu-id="fbb0c-133">Working with Business Central</span></span>](ui-work-product.md)  
