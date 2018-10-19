---
title: Isabel 6
description: "De Isabel-organisatie heeft een CIS-platform (Client Isabel Synchronizer) ontwikkeld waarmee [!INCLUDE[d365fin](../../includes/d365fin_md.md)] veilig met Isabel kan worden geïntegreerd. CIS verwerkt de uitwisseling van documenten met en van de Isabel-server."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 9a9ac84f3a62a4515568aa017ba5fc5d4ed1e450
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="isabel-6"></a><span data-ttu-id="7a804-104">Isabel 6</span><span class="sxs-lookup"><span data-stu-id="7a804-104">Isabel 6</span></span>
<span data-ttu-id="7a804-105">De Isabel-organisatie heeft een CIS-platform (Client Isabel Synchronizer) ontwikkeld waarmee [!INCLUDE[d365fin](../../includes/d365fin_md.md)] veilig met Isabel kan worden geïntegreerd.</span><span class="sxs-lookup"><span data-stu-id="7a804-105">The Isabel organization has developed a Client Isabel Synchronizer (CIS) platform that allows [!INCLUDE[d365fin](../../includes/d365fin_md.md)] to securely integrate with Isabel.</span></span> <span data-ttu-id="7a804-106">CIS verwerkt de uitwisseling van documenten met en van de Isabel-server.</span><span class="sxs-lookup"><span data-stu-id="7a804-106">CIS handles document exchange to and from the Isabel server.</span></span>  

<span data-ttu-id="7a804-107">Als u de bankbestanden wilt uploaden of downloaden, moet u uw omgeving instellen om met Isabel te werken.</span><span class="sxs-lookup"><span data-stu-id="7a804-107">To upload or download the bank files, you will have to set up your environment to work with Isabel.</span></span> [!INCLUDE[d365fin](../../includes/d365fin_md.md)] <span data-ttu-id="7a804-108">communiceert met de CIS.dll via een COM-wrapper.</span><span class="sxs-lookup"><span data-stu-id="7a804-108">communicates to the CIS.dll through a COM wrapper.</span></span>  

<span data-ttu-id="7a804-109">Ga als volgt te werk om uw systeem geschikt te maken voor samenwerking met Isabel:</span><span class="sxs-lookup"><span data-stu-id="7a804-109">To set up your system to work with Isabel, complete the following:</span></span>  

- <span data-ttu-id="7a804-110">Installeer de Isabel-beveiligingsonderdelen.</span><span class="sxs-lookup"><span data-stu-id="7a804-110">Install the Isabel security components.</span></span> <span data-ttu-id="7a804-111">Raadpleeg voor meer informatie het downloadgedeelte op de [Isabel-website](https://go.microsoft.com/fwlink/?LinkId=210323).</span><span class="sxs-lookup"><span data-stu-id="7a804-111">For more information, see the download area on the [Isabel website](https://go.microsoft.com/fwlink/?LinkId=210323).</span></span>  

- <span data-ttu-id="7a804-112">Installeer de COM-wrapper van de Isabel-organisatie.</span><span class="sxs-lookup"><span data-stu-id="7a804-112">Install the COM wrapper that is manufactured by the Isabel organization.</span></span> <span data-ttu-id="7a804-113">Deze wrapper is opgenomen in het Isabel GO 6.20-pakket.</span><span class="sxs-lookup"><span data-stu-id="7a804-113">This wrapper is included with the Isabel GO 6.20 package.</span></span>  

- <span data-ttu-id="7a804-114">Registreer de COM-wrapper op uw computer.</span><span class="sxs-lookup"><span data-stu-id="7a804-114">Register the COM wrapper on your computer.</span></span> <span data-ttu-id="7a804-115">Zoek de CIS.dll bij de opdrachtprompt en voer vervolgens de opdracht **regsvr32 CISComWrapper.dll** uit.</span><span class="sxs-lookup"><span data-stu-id="7a804-115">At the command prompt, locate the CIS.dll and then execute the **regsvr32 CISComWrapper.dll** command.</span></span>  

## <a name="see-also"></a><span data-ttu-id="7a804-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="7a804-116">See Also</span></span>  
 <span data-ttu-id="7a804-117">[Isabel-website](https://go.microsoft.com/fwlink/?LinkId=210323) </span><span class="sxs-lookup"><span data-stu-id="7a804-117">[Isabel website](https://go.microsoft.com/fwlink/?LinkId=210323) </span></span>  
 <span data-ttu-id="7a804-118">[Elektronisch bankieren voor België](belgian-electronic-banking.md) </span><span class="sxs-lookup"><span data-stu-id="7a804-118">[Belgian Electronic Banking](belgian-electronic-banking.md) </span></span>  
 [<span data-ttu-id="7a804-119">Elektronisch bankieren instellen</span><span class="sxs-lookup"><span data-stu-id="7a804-119">Set Up Electronic Banking</span></span>](how-to-set-up-electronic-banking.md)

