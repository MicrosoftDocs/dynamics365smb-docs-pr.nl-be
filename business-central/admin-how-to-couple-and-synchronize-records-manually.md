---
title: Records handmatig koppelen en synchroniseren | Microsoft Docs
description: Als een integratietabeltoewijzing wordt gesynchroniseerd, kunnen gegevens in alle records in een tabel in Business Central en Dynamics 365 for Sales worden gesynchroniseerd die zijn gekoppeld.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 36f1a0fe8c50744d9ce13d1e6c3c899f4ceaf5e4
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1245417"
---
# <a name="couple-and-synchronize-records-manually"></a><span data-ttu-id="ef5f3-103">Records handmatig koppelen en synchroniseren</span><span class="sxs-lookup"><span data-stu-id="ef5f3-103">Couple and Synchronize Records Manually</span></span>
<span data-ttu-id="ef5f3-104">In dit onderwerp wordt beschreven hoe u een of meer records in [!INCLUDE[d365fin](includes/d365fin_md.md)] koppelt aan records in [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="ef5f3-104">This topic describes how to couple one or more records in [!INCLUDE[d365fin](includes/d365fin_md.md)] with records in [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="ef5f3-105">Door records te koppelen kunt u [!INCLUDE[crm_md](includes/crm_md.md)]-informatie vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)]bekijken en andersom.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-105">Coupling records lets you view [!INCLUDE[crm_md](includes/crm_md.md)] information from [!INCLUDE[d365fin](includes/d365fin_md.md)], and vice versa.</span></span> <span data-ttu-id="ef5f3-106">Door de koppeling kunt u ook gegevens synchroniseren tussen de records.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="ef5f3-107">U kunt bestaande records koppelen of nieuwe records maken en koppelen.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="ef5f3-108">Gegevens koppelen en synchroniseren met [!INCLUDE[crm_md](includes/crm_md.md)] is alleen beschikbaar als de systeembeheerder een verbinding tussen [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] heeft gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-108">Coupling and synchronizing data with [!INCLUDE[crm_md](includes/crm_md.md)] is available only if your system administrator has created a connection between [!INCLUDE[d365fin](includes/d365fin_md.md)] and [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="ef5f3-109">Een snelle manier om dat te controleren is de **Klant**-kaart te openen en de actie **Koppeling instellen** te zoeken.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="ef5f3-110">Als de actie beschikbaar is, zijn de apps verbonden.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-110">If the action is available, the apps are connected.</span></span>   

## <a name="to-couple-a-record"></a><span data-ttu-id="ef5f3-111">Een record koppelen</span><span class="sxs-lookup"><span data-stu-id="ef5f3-111">To couple a record</span></span>  
1.  <span data-ttu-id="ef5f3-112">In [!INCLUDE[d365fin](includes/d365fin_md.md)] opent u de kaart voor de record die moeten worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-112">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="ef5f3-113">Bijvoorbeeld de klant- of contactkaart.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-113">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="ef5f3-114">U kunt ook slechts de lijstpagina openen en de record selecteren die u wilt koppelen.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-114">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="ef5f3-115">Kies de actie **Koppeling instellen**.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-115">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="ef5f3-116">Vul de velden in en kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-116">Fill in the fields, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="ef5f3-117">Eén record synchroniseren</span><span class="sxs-lookup"><span data-stu-id="ef5f3-117">To synchronize a single record</span></span>  
1.  <span data-ttu-id="ef5f3-118">In [!INCLUDE[d365fin](includes/d365fin_md.md)] opent u de kaart voor de record die moeten worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-118">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="ef5f3-119">Bijvoorbeeld de klant- of contactkaart.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-119">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="ef5f3-120">Kies de actie **Nu synchroniseren**.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-120">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="ef5f3-121">Als een record kan worden gesynchroniseerd vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)] of vanuit [!INCLUDE[crm_md](includes/crm_md.md)] naar [!INCLUDE[d365fin](includes/d365fin_md.md)], selecteert u de optie die de richting van gegevensupdate opgeeft, en kiest u vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-121">If a record can be synchronized either from [!INCLUDE[d365fin](includes/d365fin_md.md)] to [!INCLUDE[crm_md](includes/crm_md.md)] or from [!INCLUDE[crm_md](includes/crm_md.md)] to [!INCLUDE[d365fin](includes/d365fin_md.md)], select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="ef5f3-122">Meerdere records synchroniseren</span><span class="sxs-lookup"><span data-stu-id="ef5f3-122">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="ef5f3-123">Open in [!INCLUDE[d365fin](includes/d365fin_md.md)] de lijstpagina voor de record, zoals lijstpagina Klanten of Contact.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-123">In [!INCLUDE[d365fin](includes/d365fin_md.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="ef5f3-124">Selecteer de records die u wilt synchroniseren en kies vervolgens de actie **Nu synchroniseren**.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-124">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="ef5f3-125">Als records kunnen worden gesynchroniseerd vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)] of vanuit [!INCLUDE[crm_md](includes/crm_md.md)] naar [!INCLUDE[d365fin](includes/d365fin_md.md)], selecteert u de optie die de richting van gegevensupdate opgeeft, en kiest u vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef5f3-125">If records can be synchronized either from [!INCLUDE[d365fin](includes/d365fin_md.md)] to [!INCLUDE[crm_md](includes/crm_md.md)] or from [!INCLUDE[crm_md](includes/crm_md.md)] to [!INCLUDE[d365fin](includes/d365fin_md.md)], select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ef5f3-126">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ef5f3-126">See Also</span></span>  
[<span data-ttu-id="ef5f3-127">Dynamics 365 for Sales gebruiken vanuit Business Central</span><span class="sxs-lookup"><span data-stu-id="ef5f3-127">Using Dynamics 365 for Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)
