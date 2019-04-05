---
title: 'Ontwerpdetails: Codeunit 408 Dimensiebeheer | Microsoft Docs'
description: Codeunit 408 Dimensiebeheer is een functiebibliotheek die veel voorkomende taken afhandelt die verband houden met dimensies, zoals kopiëren van de ene tabel naar de andere of van het ene document naar het andere.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 95d4afc18b0be620df2f4b2067a093237c7c4df2
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "815749"
---
# <a name="design-details-codeunit-408-dimension-management"></a><span data-ttu-id="a5c4b-103">Ontwerpdetails: Codeunit 408 Dimensiebeheer</span><span class="sxs-lookup"><span data-stu-id="a5c4b-103">Design Details: Codeunit 408 Dimension Management</span></span>
<span data-ttu-id="a5c4b-104">Codeunit 408 Dimensiebeheer is een functiebibliotheek die veel voorkomende taken afhandelt die verband houden met dimensies, zoals kopiëren van de ene tabel naar de andere of van het ene document naar het andere.</span><span class="sxs-lookup"><span data-stu-id="a5c4b-104">Codeunit 408 Dimension Management is a function library that handles common tasks that are related to dimensions, such as copying from one table to another or from one document to another.</span></span> <span data-ttu-id="a5c4b-105">In dit onderwerp worden de functies genoemd die in Microsoft Dynamics NAV 2013 R2 zijn gewijzigd en er wordt aangegeven wat er met de functies moet gebeuren.</span><span class="sxs-lookup"><span data-stu-id="a5c4b-105">This topic lists the functions that are modified in Microsoft Dynamics NAV 2013 R2 and specifies what has to be done to the functions.</span></span> <span data-ttu-id="a5c4b-106">Veel functies zijn verwijderd omdat er geen reden is om te kopiëren tussen dimensietabellen.</span><span class="sxs-lookup"><span data-stu-id="a5c4b-106">Many functions are deleted because there is no need for copying between dimension tables.</span></span>  

## <a name="modified-functions"></a><span data-ttu-id="a5c4b-107">Gewijzigde functies</span><span class="sxs-lookup"><span data-stu-id="a5c4b-107">Modified Functions</span></span>  

|<span data-ttu-id="a5c4b-108">Functienaam</span><span class="sxs-lookup"><span data-stu-id="a5c4b-108">Function Name</span></span>|<span data-ttu-id="a5c4b-109">Beschrijving wijziging</span><span class="sxs-lookup"><span data-stu-id="a5c4b-109">Modification Description</span></span>|  
|-------------------|------------------------------|  
|<span data-ttu-id="a5c4b-110">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="a5c4b-110">CheckDimSetIDComb</span></span>|<span data-ttu-id="a5c4b-111">Nieuwe functie die de overige controlefuncties vervangt en die een dimensieset-id als argument gebruikt in plaats van een dimensietabel.</span><span class="sxs-lookup"><span data-stu-id="a5c4b-111">New function that substitutes the other check functions and takes a Dimension Set ID as an argument instead of a dimension table.</span></span>|  
|<span data-ttu-id="a5c4b-112">CheckDimSetIDComb</span><span class="sxs-lookup"><span data-stu-id="a5c4b-112">CheckDimSetIDComb</span></span><br /><br /> <span data-ttu-id="a5c4b-113">CheckDocDimComb</span><span class="sxs-lookup"><span data-stu-id="a5c4b-113">CheckDocDimComb</span></span><br /><br /> <span data-ttu-id="a5c4b-114">CheckServContractDimComb</span><span class="sxs-lookup"><span data-stu-id="a5c4b-114">CheckServContractDimComb</span></span><br /><br /> <span data-ttu-id="a5c4b-115">CheckDimBuffer</span><span class="sxs-lookup"><span data-stu-id="a5c4b-115">CheckDimBuffer</span></span><br /><br /> <span data-ttu-id="a5c4b-116">CheckDimComb</span><span class="sxs-lookup"><span data-stu-id="a5c4b-116">CheckDimComb</span></span><br /><br /> <span data-ttu-id="a5c4b-117">CheckDimValueComb</span><span class="sxs-lookup"><span data-stu-id="a5c4b-117">CheckDimValueComb</span></span>|<span data-ttu-id="a5c4b-118">Wissen.</span><span class="sxs-lookup"><span data-stu-id="a5c4b-118">Delete.</span></span> <span data-ttu-id="a5c4b-119">Al het gebruik moet worden gewijzigd in CheckDimSetIDComb.</span><span class="sxs-lookup"><span data-stu-id="a5c4b-119">All usage should be changed to CheckDimSetIDComb.</span></span>|  
|<span data-ttu-id="a5c4b-120">GetDefaultDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-120">GetDefaultDim</span></span>|<span data-ttu-id="a5c4b-121">Wijzigen om een geheel-getal dimensieset-id te retourneren in plaats van een set records.</span><span class="sxs-lookup"><span data-stu-id="a5c4b-121">Modify to return an integer Dimension Set ID instead of a set of records.</span></span>|  
|<span data-ttu-id="a5c4b-122">CopyJnlLineDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-122">CopyJnlLineDimToICJnlDim</span></span><br /><br /> <span data-ttu-id="a5c4b-123">CopyICJnlDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-123">CopyICJnlDimToJnlLineDim</span></span><br /><br /> <span data-ttu-id="a5c4b-124">CopyDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-124">CopyDocDimtoICDocDim</span></span><br /><br /> <span data-ttu-id="a5c4b-125">CopyICDocDimtoICDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-125">CopyICDocDimtoICDocDim</span></span>|<span data-ttu-id="a5c4b-126">Wijzigen voor gebruik met DimSetID > ICJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-126">Modify to work with DimSetID -> ICJnlLineDim</span></span>|  

## <a name="deleted-functions"></a><span data-ttu-id="a5c4b-127">Verwijderde functies</span><span class="sxs-lookup"><span data-stu-id="a5c4b-127">Deleted Functions</span></span>  
 <span data-ttu-id="a5c4b-128">De functies die uit codeunit 408 met de Dimensiesetpostenfunctie zijn verwijderd worden hieronder weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a5c4b-128">Functions that are deleted from codeunit 408 in connection with the Dimension Set Entries feature are listed below.</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="a5c4b-129">Tijdens de upgrade van de vereffeningcode van Microsoft Dynamics NAV 2009 of eerdere versies naar Microsoft Dynamics NAV 2016 zijn de volgende functies niet beschikbaar in Microsoft Dynamics NAV 2016.</span><span class="sxs-lookup"><span data-stu-id="a5c4b-129">During the upgrade of application code from Microsoft Dynamics NAV 2009 or earlier versions to Microsoft Dynamics NAV 2016, the following functions are not available in Microsoft Dynamics NAV 2016.</span></span> <span data-ttu-id="a5c4b-130">Als u aanpassingen hebt die een of meer van de functies gebruiken, moet u die code upgraden.</span><span class="sxs-lookup"><span data-stu-id="a5c4b-130">If you have customizations that use one or more of the functions, you must upgrade that code accordingly.</span></span>

 <span data-ttu-id="a5c4b-131">InsertJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-131">InsertJnlLineDim</span></span>  

 <span data-ttu-id="a5c4b-132">UpdateJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-132">UpdateJnlLineDefaultDim</span></span>  

 <span data-ttu-id="a5c4b-133">GetJnlLineDefaultDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-133">GetJnlLineDefaultDim</span></span>  

 <span data-ttu-id="a5c4b-134">GetPreviousDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-134">GetPreviousDocDefaultDim</span></span>  

 <span data-ttu-id="a5c4b-135">GetPreviousProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-135">GetPreviousProdDocDefaultDim</span></span>  

 <span data-ttu-id="a5c4b-136">InsertDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-136">InsertDocDim</span></span>  

 <span data-ttu-id="a5c4b-137">UpdateDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-137">UpdateDocDefaultDim</span></span>  

 <span data-ttu-id="a5c4b-138">ExtractDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-138">ExtractDocDefaultDim</span></span>  

 <span data-ttu-id="a5c4b-139">InsertProdDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-139">InsertProdDocDim</span></span>  

 <span data-ttu-id="a5c4b-140">UpdateProdDocDefaultDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-140">UpdateProdDocDefaultDim</span></span>  

 <span data-ttu-id="a5c4b-141">InsertServContractDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-141">InsertServContractDim</span></span>  

 <span data-ttu-id="a5c4b-142">UpdateServcontractDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-142">UpdateServcontractDim</span></span>  

 <span data-ttu-id="a5c4b-143">UpdateDefaultDimNewDimValue</span><span class="sxs-lookup"><span data-stu-id="a5c4b-143">UpdateDefaultDimNewDimValue</span></span>  

 <span data-ttu-id="a5c4b-144">GetDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-144">GetDocDim</span></span>  

 <span data-ttu-id="a5c4b-145">GetProdDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-145">GetProdDocDim</span></span>  

 <span data-ttu-id="a5c4b-146">TypeToTableID1</span><span class="sxs-lookup"><span data-stu-id="a5c4b-146">TypeToTableID1</span></span>  

 <span data-ttu-id="a5c4b-147">TypeToTableID2</span><span class="sxs-lookup"><span data-stu-id="a5c4b-147">TypeToTableID2</span></span>  

 <span data-ttu-id="a5c4b-148">TypeToTableID3</span><span class="sxs-lookup"><span data-stu-id="a5c4b-148">TypeToTableID3</span></span>  

 <span data-ttu-id="a5c4b-149">TypeToTableID4</span><span class="sxs-lookup"><span data-stu-id="a5c4b-149">TypeToTableID4</span></span>  

 <span data-ttu-id="a5c4b-150">TypeToTableID5</span><span class="sxs-lookup"><span data-stu-id="a5c4b-150">TypeToTableID5</span></span>  

 <span data-ttu-id="a5c4b-151">DeleteJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-151">DeleteJnlLineDim</span></span>  

 <span data-ttu-id="a5c4b-152">DeleteDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-152">DeleteDocDim</span></span>  

 <span data-ttu-id="a5c4b-153">DeletePostedDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-153">DeletePostedDocDim</span></span>  

 <span data-ttu-id="a5c4b-154">DeleteProdDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-154">DeleteProdDocDim</span></span>  

 <span data-ttu-id="a5c4b-155">DeleteServContractDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-155">DeleteServContractDim</span></span>  

 <span data-ttu-id="a5c4b-156">ShowJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-156">ShowJnlLineDim</span></span>  

 <span data-ttu-id="a5c4b-157">SaveJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-157">SaveJnlLineDim</span></span>  

 <span data-ttu-id="a5c4b-158">ShowJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-158">ShowJnlLineNewDim</span></span>  

 <span data-ttu-id="a5c4b-159">SaveJnlLineNewDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-159">SaveJnlLineNewDim</span></span>  

 <span data-ttu-id="a5c4b-160">ShowDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-160">ShowDocDim</span></span>  

 <span data-ttu-id="a5c4b-161">SaveDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-161">SaveDocDim</span></span>  

 <span data-ttu-id="a5c4b-162">ShowProdDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-162">ShowProdDocDim</span></span>  

 <span data-ttu-id="a5c4b-163">SaveProdDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-163">SaveProdDocDim</span></span>  

 <span data-ttu-id="a5c4b-164">ShowTempDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-164">ShowTempDim</span></span>  

 <span data-ttu-id="a5c4b-165">SaveTempDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-165">SaveTempDim</span></span>  

 <span data-ttu-id="a5c4b-166">ShowTempNewDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-166">ShowTempNewDim</span></span>  

 <span data-ttu-id="a5c4b-167">SaveTempNewDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-167">SaveTempNewDim</span></span>  

 <span data-ttu-id="a5c4b-168">SaveServContractDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-168">SaveServContractDim</span></span>  

 <span data-ttu-id="a5c4b-169">MoveJnlLineDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-169">MoveJnlLineDimToLedgEntryDim</span></span>  

 <span data-ttu-id="a5c4b-170">MoveDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-170">MoveDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="a5c4b-171">MoveOneDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-171">MoveOneDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="a5c4b-172">MoveLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-172">MoveLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="a5c4b-173">MoveDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-173">MoveDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="a5c4b-174">MoveDimBufToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-174">MoveDimBufToLedgEntryDim</span></span>  

 <span data-ttu-id="a5c4b-175">MoveDimBufToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-175">MoveDimBufToPostedDocDim</span></span>  

 <span data-ttu-id="a5c4b-176">MoveDimBufToGLBudgetDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-176">MoveDimBufToGLBudgetDim</span></span>  

 <span data-ttu-id="a5c4b-177">CopyJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-177">CopyJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="a5c4b-178">CopyLedgEntryDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-178">CopyLedgEntryDimToJnlLineDim</span></span>  

 <span data-ttu-id="a5c4b-179">CopyDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-179">CopyDocDimToDocDim</span></span>  

 <span data-ttu-id="a5c4b-180">CopyPostedDocDimToPostedDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-180">CopyPostedDocDimToPostedDocDim</span></span>  

 <span data-ttu-id="a5c4b-181">CopyDocDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-181">CopyDocDimToJnlLineDim</span></span>  

 <span data-ttu-id="a5c4b-182">CopyDimBufToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-182">CopyDimBufToJnlLineDim</span></span>  

 <span data-ttu-id="a5c4b-183">CopyDimBufToDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-183">CopyDimBufToDocDim</span></span>  

 <span data-ttu-id="a5c4b-184">CopySCDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-184">CopySCDimToDocDim</span></span>  

 <span data-ttu-id="a5c4b-185">MoveDocDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-185">MoveDocDimToLedgEntryDim</span></span>  

 <span data-ttu-id="a5c4b-186">MoveDocDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-186">MoveDocDimToDocDim</span></span>  

 <span data-ttu-id="a5c4b-187">MoveDocDimArchvToDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-187">MoveDocDimArchvToDocDim</span></span>  

 <span data-ttu-id="a5c4b-188">MoveLedgEntryDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-188">MoveLedgEntryDimToDocDim</span></span>  

 <span data-ttu-id="a5c4b-189">MoveProdDocDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-189">MoveProdDocDimToProdDocDim</span></span>  

 <span data-ttu-id="a5c4b-190">MoveJnlLineDimToProdDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-190">MoveJnlLineDimToProdDocDim</span></span>  

 <span data-ttu-id="a5c4b-191">MoveJnlLineDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-191">MoveJnlLineDimToDocDim</span></span>  

 <span data-ttu-id="a5c4b-192">MoveJnlLineDimToJnlLineDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-192">MoveJnlLineDimToJnlLineDim</span></span>  

 <span data-ttu-id="a5c4b-193">CopyLedgEntryDimToLedgEntryDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-193">CopyLedgEntryDimToLedgEntryDim</span></span>  

 <span data-ttu-id="a5c4b-194">MoveTempFromDimToTempToDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-194">MoveTempFromDimToTempToDim</span></span>  

 <span data-ttu-id="a5c4b-195">TransferTempToDimToDocDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-195">TransferTempToDimToDocDim</span></span>  

 <span data-ttu-id="a5c4b-196">MoveJnlLineDimToBuf</span><span class="sxs-lookup"><span data-stu-id="a5c4b-196">MoveJnlLineDimToBuf</span></span>  

 <span data-ttu-id="a5c4b-197">CopyICJnlDimToICJnlDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-197">CopyICJnlDimToICJnlDim</span></span>  

 <span data-ttu-id="a5c4b-198">TestDimValue</span><span class="sxs-lookup"><span data-stu-id="a5c4b-198">TestDimValue</span></span>  

 <span data-ttu-id="a5c4b-199">TestNewDimValue</span><span class="sxs-lookup"><span data-stu-id="a5c4b-199">TestNewDimValue</span></span>  

 <span data-ttu-id="a5c4b-200">MoveDimBufToItemBudgetDim.</span><span class="sxs-lookup"><span data-stu-id="a5c4b-200">MoveDimBufToItemBudgetDim.</span></span> <span data-ttu-id="a5c4b-201">(Verwijderen omdat de tabel ItemBudgetDim wordt verwijderd.)</span><span class="sxs-lookup"><span data-stu-id="a5c4b-201">(Delete because the ItemBudgetDim Table is deleted.)</span></span>  

 <span data-ttu-id="a5c4b-202">GetServContractDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-202">GetServContractDim</span></span>  

 <span data-ttu-id="a5c4b-203">MoveTempDimToBuf</span><span class="sxs-lookup"><span data-stu-id="a5c4b-203">MoveTempDimToBuf</span></span>  

 <span data-ttu-id="a5c4b-204">UpdateSCInvLineDim</span><span class="sxs-lookup"><span data-stu-id="a5c4b-204">UpdateSCInvLineDim</span></span>  

 <span data-ttu-id="a5c4b-205">CopyJnlLineDimToBuffer</span><span class="sxs-lookup"><span data-stu-id="a5c4b-205">CopyJnlLineDimToBuffer</span></span>  

 <span data-ttu-id="a5c4b-206">UpdateDocDefaultDim2</span><span class="sxs-lookup"><span data-stu-id="a5c4b-206">UpdateDocDefaultDim2</span></span>  

## <a name="see-also"></a><span data-ttu-id="a5c4b-207">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a5c4b-207">See Also</span></span>
 <span data-ttu-id="a5c4b-208">[Ontwerpdetails: Dimensiesetposten](design-details-dimension-set-entries.md) </span><span class="sxs-lookup"><span data-stu-id="a5c4b-208">[Design Details: Dimension Set Entries](design-details-dimension-set-entries.md) </span></span>  
 <span data-ttu-id="a5c4b-209">[Ontwerpdetails: Dimensiesetposten - overzicht](design-details-dimension-set-entries-overview.md) </span><span class="sxs-lookup"><span data-stu-id="a5c4b-209">[Design Details: Dimension Set Entries Overview](design-details-dimension-set-entries-overview.md) </span></span>  
 <span data-ttu-id="a5c4b-210">[Ontwerpdetails: Dimensiecombinaties zoeken](design-details-searching-for-dimension-combinations.md) </span><span class="sxs-lookup"><span data-stu-id="a5c4b-210">[Design Details: Searching for Dimension Combinations](design-details-searching-for-dimension-combinations.md) </span></span>  
 <span data-ttu-id="a5c4b-211">[Ontwerpdetails: Tabelstructuur](design-details-table-structure.md) </span><span class="sxs-lookup"><span data-stu-id="a5c4b-211">[Design Details: Table Structure](design-details-table-structure.md) </span></span>  
 [<span data-ttu-id="a5c4b-212">Ontwerpdetails: Codevoorbeelden van gewijzigde patronen in wijzigingen</span><span class="sxs-lookup"><span data-stu-id="a5c4b-212">Design Details: Code Examples of Changed Patterns in Modifications</span></span>](design-details-code-examples-of-changed-patterns-in-modifications.md)
