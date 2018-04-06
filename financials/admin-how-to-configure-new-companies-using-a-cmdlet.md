---
title: Nieuwe bedrijven configureren met een cmdlet | Microsoft Docs
description: In een aantal scenario's kunt u een configuratiepakket laden en importeren zonder uw gebruikers hierbij te betrekken of de gebruikersinterface van RapidStart Services te gebruiken. Hiervoor kunt u een Windows PowerShell-cmdlet gebruiken.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/06/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 8b91c3b91e07f5ad96dcfc65152062054fc13c01
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="configure-new-companies-using-a-cmdlet"></a><span data-ttu-id="aee83-104">Nieuwe bedrijven configureren met een cmdlet</span><span class="sxs-lookup"><span data-stu-id="aee83-104">Configure New Companies using a Cmdlet</span></span>
<span data-ttu-id="aee83-105">In een aantal scenario's kunt u een configuratiepakket laden en importeren zonder uw gebruikers hierbij te betrekken of de gebruikersinterface van RapidStart Services te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="aee83-105">In a number of scenarios, you may want to load and import a configuration package without involving your users or using the RapidStart Services user interface.</span></span> <span data-ttu-id="aee83-106">Hiervoor kunt u een Windows PowerShell-cmdlet gebruiken.</span><span class="sxs-lookup"><span data-stu-id="aee83-106">You can do so by using a Windows PowerShell cmdlet.</span></span> <span data-ttu-id="aee83-107">Scenario's waarbij dit handig kan zijn:</span><span class="sxs-lookup"><span data-stu-id="aee83-107">Scenarios where this may be useful include:</span></span>  

- <span data-ttu-id="aee83-108">Import van gegevens implementeren in meerdere [!INCLUDE[d365fin](includes/d365fin_md.md)]-installaties.</span><span class="sxs-lookup"><span data-stu-id="aee83-108">Performing data import across multiple [!INCLUDE[d365fin](includes/d365fin_md.md)] installations.</span></span>
- <span data-ttu-id="aee83-109">Aanvullende toepassingsgebieden configureren voor meerdere klanten.</span><span class="sxs-lookup"><span data-stu-id="aee83-109">Configuring additional application areas for multiple customers.</span></span>  

## <a name="to-deploy-a-configuration-package-using-a-cmdlet"></a><span data-ttu-id="aee83-110">Een configuratiepakket implementeren met een cmdlet</span><span class="sxs-lookup"><span data-stu-id="aee83-110">To deploy a configuration package using a cmdlet</span></span>  

1. <span data-ttu-id="aee83-111">Een RapidStart Services-pakket voorbereiden.</span><span class="sxs-lookup"><span data-stu-id="aee83-111">Prepare a RapidStart Services package.</span></span> <span data-ttu-id="aee83-112">U kunt bijvoorbeeld een pakket maken om bepaalde waarden, de namen van de tabel en de velden waar deze waarden in moeten worden geplaatst, te importeren.</span><span class="sxs-lookup"><span data-stu-id="aee83-112">For example, you can create a package to import certain values and the names of the table and the fields to insert these values into.</span></span>  
2. <span data-ttu-id="aee83-113">Plaats het pakket op een computer waarop u de cmdlet zult uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="aee83-113">Place the package on a computer where you will run the cmdlet.</span></span>  
3. <span data-ttu-id="aee83-114">Open de [!INCLUDE[d365fin](includes/d365fin_md.md)]-beheershell.</span><span class="sxs-lookup"><span data-stu-id="aee83-114">Open the [!INCLUDE[d365fin](includes/d365fin_md.md)] administration shell.</span></span>  
4. <span data-ttu-id="aee83-115">Voer **Aanroepen-NAVCodeUnit** in en geef informatie op zoals in het volgende voorbeeld.</span><span class="sxs-lookup"><span data-stu-id="aee83-115">Enter **Invoke-NAVCodeUnit**, and specify information similar to the following example.</span></span>  
    ```  
    Invoke-NAVCodeunit -Tenant Default -CompanyName "CRONUS International Ltd." -CodeunitId 8620 -MethodName ImportRapidStartPackage -Argument "C:TEMPRS_CONFIG.rapidstart" -ServerInstance DynamicsNAV71  

    ```
<span data-ttu-id="aee83-116">De cmdlet importeert het pakket in elk bedrijf.</span><span class="sxs-lookup"><span data-stu-id="aee83-116">The cmdlet imports the package into each company.</span></span> <span data-ttu-id="aee83-117">Gebruikers kunnen de nieuwe functies direct gebruiken.</span><span class="sxs-lookup"><span data-stu-id="aee83-117">Users can start to use the new functionality immediately.</span></span>  

## <a name="see-also"></a><span data-ttu-id="aee83-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="aee83-118">See Also</span></span>  
[<span data-ttu-id="aee83-119">Nieuwe bedrijven configureren</span><span class="sxs-lookup"><span data-stu-id="aee83-119">Configure New Companies</span></span>](admin-how-to-configure-new-companies.md)  
[<span data-ttu-id="aee83-120">Configuraties toepassen op nieuwe bedrijven</span><span class="sxs-lookup"><span data-stu-id="aee83-120">Apply Configurations to New Companies</span></span>](admin-apply-configuration-to-new-companies.md)  
[<span data-ttu-id="aee83-121">Een bedrijf met RapidStart Services instellen</span><span class="sxs-lookup"><span data-stu-id="aee83-121">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="aee83-122">Beheer</span><span class="sxs-lookup"><span data-stu-id="aee83-122">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="aee83-123">Microsoft Dynamics NAV Windows PowerShell-cmdlets</span><span class="sxs-lookup"><span data-stu-id="aee83-123">Microsoft Dynamics NAV Windows PowerShell Cmdlets</span></span>](/dynamics-nav/microsoft-dynamics-nav-windows-powershell-cmdlets)

