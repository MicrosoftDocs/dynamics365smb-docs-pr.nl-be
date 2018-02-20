---
title: Statussen instellen voor serviceorders en reparaties | Microsoft Docs
description: U moet negen herstelstatusopties instellen waarmee u de voortgang van herstel en onderhoud van serviceartikelen in serviceorders kunt aangeven.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 8ffd5d6893b2b6c8ce7b7377c586f4f5414279b5
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a><span data-ttu-id="46cba-103">Statussen instellen voor serviceorders en reparaties</span><span class="sxs-lookup"><span data-stu-id="46cba-103">Set Up Statuses for Service Orders and Repairs</span></span>
<span data-ttu-id="46cba-104">U moet herstelstatusopties instellen waarmee u de voortgang van herstel en onderhoud van serviceartikelen in serviceorders kunt aangeven.</span><span class="sxs-lookup"><span data-stu-id="46cba-104">You must set up repair status options that identify the progress of repair and maintenance of service items in service orders.</span></span> <span data-ttu-id="46cba-105">U moet minimaal negen herstelstatusopties instellen om situaties of ondernomen acties met betrekking tot de service voor serviceartikelen aan te duiden.</span><span class="sxs-lookup"><span data-stu-id="46cba-105">You must set up at least nine repair status options that identify situations or actions taken when servicing service items.</span></span>  

<span data-ttu-id="46cba-106">U kunt het prioriteitsniveau voor serviceorderstatusopties instellen.</span><span class="sxs-lookup"><span data-stu-id="46cba-106">You can set the priority level for service order status options.</span></span> <span data-ttu-id="46cba-107">De vier prioriteiten zijn Hoog, Relatief hoog, Relatief laag en Laag.</span><span class="sxs-lookup"><span data-stu-id="46cba-107">There four priorities are High, Medium High, Medium Low, and Low.</span></span>  
  
<span data-ttu-id="46cba-108">Wanneer u de herstelstatus van een serviceartikel in een serviceorder wijzigt, wordt de serviceorderstatus bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="46cba-108">When you change the repair status of a service item in a service order, the service order status is updated.</span></span> <span data-ttu-id="46cba-109">De herstelstatus van elk serviceartikel is gekoppeld aan de serviceorderstatus.</span><span class="sxs-lookup"><span data-stu-id="46cba-109">The repair status of each service item is linked to the service order status.</span></span> <span data-ttu-id="46cba-110">Als de serviceartikelen zijn gekoppeld aan twee of meer opties voor serviceorderstatus, wordt de serviceorderstatus met de hoogste prioriteit geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="46cba-110">If the service items are linked to two or more service order status options, the service order status with the highest priority is selected.</span></span>  

## <a name="to-set-up-a-repair-status"></a><span data-ttu-id="46cba-111">Herstelstatus instellen</span><span class="sxs-lookup"><span data-stu-id="46cba-111">To set up a repair status</span></span>  
1. <span data-ttu-id="46cba-112">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Herstelstatus** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="46cba-112">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Repair Status**, and then choose the related link.</span></span> <span data-ttu-id="46cba-113">2.</span><span class="sxs-lookup"><span data-stu-id="46cba-113">2.</span></span> <span data-ttu-id="46cba-114">Maak een nieuwe herstelstatus.</span><span class="sxs-lookup"><span data-stu-id="46cba-114">Create a new repair status.</span></span>  
3. <span data-ttu-id="46cba-115">Vul de velden **Code** en **Omschrijving** in.</span><span class="sxs-lookup"><span data-stu-id="46cba-115">Fill in the **Code** and **Description** fields.</span></span>  
4. <span data-ttu-id="46cba-116">In het veld **Serviceorderstatus** kiest u de orderstatus waaraan u de herstelstatus wilt koppelen.</span><span class="sxs-lookup"><span data-stu-id="46cba-116">In the **Service Order Status** field, choose the order status to link the repair status to.</span></span> <span data-ttu-id="46cba-117">In het veld **Prioriteit** wordt de prioriteit weergegeven van de serviceorderstatus die u hebt gekozen.</span><span class="sxs-lookup"><span data-stu-id="46cba-117">The **Priority** field displays the priority of the service order status you have chosen.</span></span>  
5. <span data-ttu-id="46cba-118">Kies een herstelstatus.</span><span class="sxs-lookup"><span data-stu-id="46cba-118">Choose a repair status.</span></span> <span data-ttu-id="46cba-119">U kunt er slechts één kiezen.</span><span class="sxs-lookup"><span data-stu-id="46cba-119">You can choose only one.</span></span>  
6. <span data-ttu-id="46cba-120">Kies het veld **Boeken toegestaan** als u serviceorders wilt boeken met serviceartikelen met deze herstelstatus.</span><span class="sxs-lookup"><span data-stu-id="46cba-120">To be able to post service orders, including service items, with this repair status, choose the **Posting Allowed** field.</span></span>  
7. <span data-ttu-id="46cba-121">Schakel het selectievakje **Status Wachtend toegestaan** in als u de optie voor serviceorderstatus handmatig wilt wijzigen in **In behandeling** op serviceorders met serviceartikelen met deze herstelstatus.</span><span class="sxs-lookup"><span data-stu-id="46cba-121">To be able to manually change the service order status option to **Pending** in service orders including service items with this repair status, choose the **Pending Status Allowed** check box.</span></span>  
8. <span data-ttu-id="46cba-122">Schakel de selectievakjes **Status In verwerking toegestaan**, **Status Gereedgemeld toegestaan** en **Status Afwachten toegestaan** op dezelfde manier in.</span><span class="sxs-lookup"><span data-stu-id="46cba-122">Choose the **In Process Status Allowed**, **Finished Status Allowed**, and **On Hold Status Allowed** check boxes in the same way.</span></span>
  
## <a name="to-set-up-service-status-priorities"></a><span data-ttu-id="46cba-123">Servicestatusprioriteiten instellen</span><span class="sxs-lookup"><span data-stu-id="46cba-123">To set up service status priorities</span></span>  
1. <span data-ttu-id="46cba-124">Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Serviceorderstatus** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="46cba-124">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Order Status**, and then choose the related link.</span></span>  
2. <span data-ttu-id="46cba-125">Selecteer de serviceorderstatus waarvoor u een prioriteit wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="46cba-125">Select the service order status you want to set a priority for.</span></span>  
3. <span data-ttu-id="46cba-126">Kies de gewenste prioriteit voor deze serviceorderstatus in het veld **Prioriteit**.</span><span class="sxs-lookup"><span data-stu-id="46cba-126">In the **Priority** field, choose the priority you want for this service order status.</span></span> <span data-ttu-id="46cba-127">Herhaal deze stap voor elke status.</span><span class="sxs-lookup"><span data-stu-id="46cba-127">Repeat this step for each status.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="46cba-128">Zie ook</span><span class="sxs-lookup"><span data-stu-id="46cba-128">See Also</span></span>  
[<span data-ttu-id="46cba-129">Serviceorderstatus en herstelstatus begrijpen</span><span class="sxs-lookup"><span data-stu-id="46cba-129">Understanding Service Order Status and Repair Status</span></span>]()  
[<span data-ttu-id="46cba-130">CRM - Service instellen</span><span class="sxs-lookup"><span data-stu-id="46cba-130">Setting Up Service Management</span></span>](service-setup-service.md)  

