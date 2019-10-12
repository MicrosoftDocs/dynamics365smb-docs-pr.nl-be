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
ms.date: 10/01/2019
ms.author: jswymer
ms.openlocfilehash: 2474f83fd9fa137b40756a3d07ac025208f3ac6c
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308272"
---
# <a name="viewing-and-editing-in-excel-from-business-central"></a><span data-ttu-id="6febf-103">Weergeven en bewerken in Excel vanuit Business Central</span><span class="sxs-lookup"><span data-stu-id="6febf-103">Viewing and Editing in Excel From Business Central</span></span> 

<span data-ttu-id="6febf-104">Met pagina's die een lijst met records in rijen en kolommen weergeven, zoals een lijst met klanten, verkooporders of facturen, kunt u ook de records weergeven met Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="6febf-104">With pages that display a list of records in rows and columns, like a list of customers, sale orders, or invoices, you can also view the records using Microsoft Excel.</span></span> <span data-ttu-id="6febf-105">U hebt hiervoor twee opties.</span><span class="sxs-lookup"><span data-stu-id="6febf-105">To do this, you have two options.</span></span> <span data-ttu-id="6febf-106">U kunt de actie **Openen in Excel** of de actie **Bewerken in Excel** op de pagina selecteren.</span><span class="sxs-lookup"><span data-stu-id="6febf-106">You can either select the **Open in Excel** action or the **Edit in Excel** action on the page.</span></span> <span data-ttu-id="6febf-107">Dit zijn de verschillen tussen de twee methoden:</span><span class="sxs-lookup"><span data-stu-id="6febf-107">The differences between the two actions is as follows:</span></span>  

## <a name="open-in-excel"></a><span data-ttu-id="6febf-108">Openen in Excel</span><span class="sxs-lookup"><span data-stu-id="6febf-108">Open in Excel</span></span>

-    <span data-ttu-id="6febf-109">Met deze actie respecteert Excel eventuele filters op de pagina die beperken welke records worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="6febf-109">With this action, Excel respects any filters on the page the limit the records shown.</span></span> <span data-ttu-id="6febf-110">Dit betekent dat de Excel-werkmap dezelfde rijen en kolommen bevat die op de pagina worden weergegeven in [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="6febf-110">This means that the Excel workbook will contain the same rows and columns that appear on the the page in [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

-    <span data-ttu-id="6febf-111">U kunt wijzigingen in de records aanbrengen in Excel, maar u kunt de wijzigingen niet terug publiceren naar [!INCLUDE[prodshort](includes/prodshort.md)].</span><span class="sxs-lookup"><span data-stu-id="6febf-111">You can make changes to the records in Excel, but you cannot publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span> <span data-ttu-id="6febf-112">U kunt de wijzigingen alleen opslaan in het Excel-bestand op uw computer.</span><span class="sxs-lookup"><span data-stu-id="6febf-112">You can only save the changes to Excel file on your computer.</span></span> 

-    <span data-ttu-id="6febf-113">Deze actie werkt zowel onder Windows als MacOS.</span><span class="sxs-lookup"><span data-stu-id="6febf-113">This action works on both on Windows and macOS.</span></span> 

>[!NOTE]
><span data-ttu-id="6febf-114">Voor [!INCLUDE[prodshort](includes/prodshort.md)] on-premises is de actie **Openen in Excel** niet beschikbaar als de actie **Bewerken in Excel** beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="6febf-114">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Open in Excel** action is not available if the **Edit in Excel** action is.</span></span>

## <a name="edit-in-excel"></a><span data-ttu-id="6febf-115">Bewerken in Excel</span><span class="sxs-lookup"><span data-stu-id="6febf-115">Edit in Excel</span></span>

-    <span data-ttu-id="6febf-116">Met deze actie respecteert de Excel-werkmap eventuele filters op de pagina niet die beperken welke records worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="6febf-116">With this action, the Excel workbook does not respect filters on the page the limit the records shown.</span></span> <span data-ttu-id="6febf-117">Dit betekent dat de Excel-werkmap alle beschikbare records en kolommen bevat, ongeacht wat op de pagina wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="6febf-117">This means that the Excel workbook will contain all the available records and columns, regardless of what is shown on the page.</span></span> 

-    <span data-ttu-id="6febf-118">Het voordeel van de actie **Bewerken in Excel** is dat u er wijzigingen in records in Excel mee kunt aanbrengen en de wijzigingen weer naar [!INCLUDE[prodshort](includes/prodshort.md)] kunt publiceren.</span><span class="sxs-lookup"><span data-stu-id="6febf-118">The advantage of the **Edit in Excel** action is that it lets you make changes to records in Excel and then publish the changes back to [!INCLUDE[prodshort](includes/prodshort.md)].</span></span>

-    <span data-ttu-id="6febf-119">Dit werkt alleen onder Windows, niet onder MacOS.</span><span class="sxs-lookup"><span data-stu-id="6febf-119">It only works on Windows; not macOS.</span></span>

>[!NOTE]
><span data-ttu-id="6febf-120">Voor [!INCLUDE[prodshort](includes/prodshort.md)] on-premises is de actie **Bewerken in Excel** alleen beschikbaar als de Excel-invoegtoepassing door uw beheerder is geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="6febf-120">For [!INCLUDE[prodshort](includes/prodshort.md)] on-premises, the **Edit in Excel** action is only available if the Excel add-in has been installed by your administrator.</span></span> <span data-ttu-id="6febf-121">Voor beheerders: als u wilt weten hoe u de Excel-invoegtoepassing installeert, raadpleegt u [De Excel-invoegtoepassing instellen](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span><span class="sxs-lookup"><span data-stu-id="6febf-121">For administrators, if you want to learn how to install the excel add-in, see [Setting up the Excel Add-In](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configuring-excel-addin).</span></span>

### <a name="see-the-differences-between-the-options"></a><span data-ttu-id="6febf-122">Zie de verschillen tussen de opties</span><span class="sxs-lookup"><span data-stu-id="6febf-122">See the differences between the options</span></span> 
> [!Video https://go.microsoft.com/fwlink/?linkid=2086039]

## <a name="see-also"></a><span data-ttu-id="6febf-123">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6febf-123">See Also</span></span>
[<span data-ttu-id="6febf-124">Werken met Business Central</span><span class="sxs-lookup"><span data-stu-id="6febf-124">Working with Business Central</span></span>](ui-work-product.md)  
