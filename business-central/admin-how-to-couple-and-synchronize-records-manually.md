---
title: Koppelen en synchroniseren | Microsoft Docs
description: Als een integratietabeltoewijzing wordt gesynchroniseerd, kunnen gegevens in alle records in een tabel in Business Central en Dynamics 365 Sales worden gesynchroniseerd die zijn gekoppeld.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: b9ea85ea320aea35d1df661be9a9d16502d33776
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5378360"
---
# <a name="coupling-and-synchronizing"></a><span data-ttu-id="6978a-103">Koppelen en synchroniseren</span><span class="sxs-lookup"><span data-stu-id="6978a-103">Coupling and Synchronizing</span></span>
<span data-ttu-id="6978a-104">In dit onderwerp wordt beschreven hoe u een of meer records in [!INCLUDE[prod_short](includes/prod_short.md)] koppelt aan records in Dataverse of [!INCLUDE[crm_md](includes/crm_md.md)].</span><span class="sxs-lookup"><span data-stu-id="6978a-104">This topic describes how to couple one or more records in [!INCLUDE[prod_short](includes/prod_short.md)] with records in Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="6978a-105">Door records te koppelen kunt u Dataverse-informatie vanuit [!INCLUDE[prod_short](includes/prod_short.md)]bekijken en andersom.</span><span class="sxs-lookup"><span data-stu-id="6978a-105">Coupling records lets you view Dataverse information from [!INCLUDE[prod_short](includes/prod_short.md)], and vice versa.</span></span> <span data-ttu-id="6978a-106">Door de koppeling kunt u ook gegevens synchroniseren tussen de records.</span><span class="sxs-lookup"><span data-stu-id="6978a-106">The coupling also enables you to synchronize data between the records.</span></span> <span data-ttu-id="6978a-107">U kunt bestaande records koppelen of nieuwe records maken en koppelen.</span><span class="sxs-lookup"><span data-stu-id="6978a-107">You can couple existing records, or create and couple new records.</span></span>

> [!Note]
> <span data-ttu-id="6978a-108">Gegevens koppelen en synchroniseren is alleen beschikbaar als de systeembeheerder een verbinding tussen [!INCLUDE[prod_short](includes/prod_short.md)] en Dataverse of [!INCLUDE[crm_md](includes/crm_md.md)] heeft gemaakt.</span><span class="sxs-lookup"><span data-stu-id="6978a-108">Coupling and synchronizing data is available only if your system administrator has created a connection between [!INCLUDE[prod_short](includes/prod_short.md)] and Dataverse or [!INCLUDE[crm_md](includes/crm_md.md)].</span></span> <span data-ttu-id="6978a-109">Een snelle manier om dat te controleren is de **Klant**-kaart te openen en de actie **Koppeling instellen** te zoeken.</span><span class="sxs-lookup"><span data-stu-id="6978a-109">A quick way to check is to open the **Customer** card and look for the **Set Up Coupling** action.</span></span> <span data-ttu-id="6978a-110">Als de actie beschikbaar is, zijn de apps verbonden.</span><span class="sxs-lookup"><span data-stu-id="6978a-110">If the action is available, the apps are connected.</span></span>   

## <a name="video-example"></a><span data-ttu-id="6978a-111">Videovoorbeeld</span><span class="sxs-lookup"><span data-stu-id="6978a-111">Video Example</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a><span data-ttu-id="6978a-112">Een record koppelen</span><span class="sxs-lookup"><span data-stu-id="6978a-112">To couple a record</span></span>  
1.  <span data-ttu-id="6978a-113">In [!INCLUDE[prod_short](includes/prod_short.md)] opent u de kaart voor de record die moeten worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="6978a-113">In [!INCLUDE[prod_short](includes/prod_short.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="6978a-114">Bijvoorbeeld de klant- of contactkaart.</span><span class="sxs-lookup"><span data-stu-id="6978a-114">For example, the Customer or Contact card.</span></span>  

    <span data-ttu-id="6978a-115">U kunt ook slechts de lijstpagina openen en de record selecteren die u wilt koppelen.</span><span class="sxs-lookup"><span data-stu-id="6978a-115">You can also just open the list page and select the record that you want to couple.</span></span>  

2.  <span data-ttu-id="6978a-116">Kies de actie **Koppeling instellen**.</span><span class="sxs-lookup"><span data-stu-id="6978a-116">Choose the **Set Up Coupling** action.</span></span>  
3.  <span data-ttu-id="6978a-117">Vul de velden in en kies de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="6978a-117">Fill in the fields, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record"></a><span data-ttu-id="6978a-118">Eén record synchroniseren</span><span class="sxs-lookup"><span data-stu-id="6978a-118">To synchronize a single record</span></span>  
1.  <span data-ttu-id="6978a-119">In [!INCLUDE[prod_short](includes/prod_short.md)] opent u de kaart voor de record die moeten worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="6978a-119">In [!INCLUDE[prod_short](includes/prod_short.md)], open the card for the record you want to couple.</span></span> <span data-ttu-id="6978a-120">Bijvoorbeeld de klant- of contactkaart.</span><span class="sxs-lookup"><span data-stu-id="6978a-120">For example, the Customer or Contact card.</span></span>  
2.  <span data-ttu-id="6978a-121">Kies de actie **Nu synchroniseren**.</span><span class="sxs-lookup"><span data-stu-id="6978a-121">Choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="6978a-122">Als een record in één richting kan worden gesynchroniseerd, selecteert u de optie die de richting van de gegevensupdate opgeeft, en kiest u vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="6978a-122">If a record can be synchronized in one direction, select the option that specifies the direction of data update, and then choose **OK**.</span></span>  

## <a name="to-synchronize-a-single-record-from-crm_md"></a><span data-ttu-id="6978a-123">Eén record synchroniseren vanuit [!INCLUDE[crm_md](includes/crm_md.md)]</span><span class="sxs-lookup"><span data-stu-id="6978a-123">To synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)]</span></span>  
1.  <span data-ttu-id="6978a-124">In [!INCLUDE[crm_md](includes/crm_md.md)] opent u het formulier voor de record die u wilt koppelen.</span><span class="sxs-lookup"><span data-stu-id="6978a-124">In [!INCLUDE[crm_md](includes/crm_md.md)], open the form for the record you want to couple.</span></span> <span data-ttu-id="6978a-125">Bijvoorbeeld het formulier Accountkaart of Contactkaart.</span><span class="sxs-lookup"><span data-stu-id="6978a-125">For example, the Account card or Contact card form.</span></span>  
2.  <span data-ttu-id="6978a-126">Kies de actie **[!INCLUDE[prod_short](includes/prod_short.md)]** op het lint om een record automatisch te openen en te koppelen.</span><span class="sxs-lookup"><span data-stu-id="6978a-126">Choose the **[!INCLUDE[prod_short](includes/prod_short.md)]** action in the ribbon to open and couple record automatically.</span></span>

> [!Note]
> <span data-ttu-id="6978a-127">U kunt één record alleen automatisch synchroniseren vanuit [!INCLUDE[crm_md](includes/crm_md.md)] wanneer **Alleen gekoppelde records synchr.** is uitgeschakeld en de synchronisatierichting is ingesteld op Bidirectioneel of Van integratietabel op de pagina **Toewijzing van integratietabel** voor de record.</span><span class="sxs-lookup"><span data-stu-id="6978a-127">You can synchronize a single record from [!INCLUDE[crm_md](includes/crm_md.md)] automatically only when **Sync. Only Coupled Records** is disabled and the synchronization direction is set to Bidirectional or From Integration Table on the **Integration Table Mapping** page for the record.</span></span> <span data-ttu-id="6978a-128">Zie voor meer informatie [De tabellen en velden toewijzen voor synchronisatie](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span><span class="sxs-lookup"><span data-stu-id="6978a-128">For more information, see [Mapping the Tables and Fields to Synchronize](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).</span></span>     

## <a name="to-synchronize-multiple-records"></a><span data-ttu-id="6978a-129">Meerdere records synchroniseren</span><span class="sxs-lookup"><span data-stu-id="6978a-129">To synchronize multiple records</span></span>  
1.  <span data-ttu-id="6978a-130">Open in [!INCLUDE[prod_short](includes/prod_short.md)] de lijstpagina voor de record, zoals lijstpagina Klanten of Contact.</span><span class="sxs-lookup"><span data-stu-id="6978a-130">In [!INCLUDE[prod_short](includes/prod_short.md)], open the list page for the record, such as the Customers or Contacts list pages.</span></span>  
2.  <span data-ttu-id="6978a-131">Selecteer de records die u wilt synchroniseren en kies vervolgens de actie **Nu synchroniseren**.</span><span class="sxs-lookup"><span data-stu-id="6978a-131">Select the records that you want to synchronize, and then choose the **Synchronize Now** action.</span></span>  
3.  <span data-ttu-id="6978a-132">Als records in één richting kunnen worden gesynchroniseerd, selecteert u de optie die de richting opgeeft, en kiest u vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="6978a-132">If records can be synchronized in one direction, select the option that specifies the direction, and then choose **OK**.</span></span>  

## <a name="uncoupling-records"></a><span data-ttu-id="6978a-133">Records ontkoppelen</span><span class="sxs-lookup"><span data-stu-id="6978a-133">Uncoupling Records</span></span>
<span data-ttu-id="6978a-134">U kunt een of meer records loskoppelen van lijstpagina's of de pagina **Fouten met gekoppelde gegevenssynchronisatie** door een of meer regels te kiezen en **Koppeling verwijderen** te kiezen.</span><span class="sxs-lookup"><span data-stu-id="6978a-134">You can uncouple one or more records from list pages or the **Coupled Data Synchronization Errors** page by choosing one or more lines and choosing **Delete Coupling**.</span></span> <span data-ttu-id="6978a-135">U kunt ook alle koppelingen verwijderen voor een of meer tabeltoewijzingen op de pagina **Integratietabeltoewijzingen**.</span><span class="sxs-lookup"><span data-stu-id="6978a-135">You can also remove all couplings for one or more table mappings on the **Integration Table Mappings** page.</span></span>

## <a name="see-also"></a><span data-ttu-id="6978a-136">Zie ook</span><span class="sxs-lookup"><span data-stu-id="6978a-136">See Also</span></span>  
[<span data-ttu-id="6978a-137">Microsoft Dynamics 365 Sales gebruiken vanuit Business Central</span><span class="sxs-lookup"><span data-stu-id="6978a-137">Using Dynamics 365 Sales from Business Central</span></span>](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]