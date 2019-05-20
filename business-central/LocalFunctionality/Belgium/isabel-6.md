---
title: Isabel 6
description: De Isabel-organisatie heeft een CIS-platform (Client Isabel Synchronizer) ontwikkeld waarmee Business Central veilig met Isabel kan worden geïntegreerd. CIS verwerkt de uitwisseling van documenten met en van de Isabel-server.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 09ba8d6320ac27ab79d349bea79e271d8d2a56fd
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1237514"
---
# <a name="isabel-6"></a><span data-ttu-id="0aed5-104">Isabel 6</span><span class="sxs-lookup"><span data-stu-id="0aed5-104">Isabel 6</span></span>
<span data-ttu-id="0aed5-105">De Isabel-organisatie heeft een CIS-platform (Client Isabel Synchronizer) ontwikkeld waarmee [!INCLUDE[d365fin](../../includes/d365fin_md.md)] veilig met Isabel kan worden geïntegreerd.</span><span class="sxs-lookup"><span data-stu-id="0aed5-105">The Isabel organization has developed a Client Isabel Synchronizer (CIS) platform that allows [!INCLUDE[d365fin](../../includes/d365fin_md.md)] to securely integrate with Isabel.</span></span> <span data-ttu-id="0aed5-106">CIS verwerkt de uitwisseling van documenten met en van de Isabel-server.</span><span class="sxs-lookup"><span data-stu-id="0aed5-106">CIS handles document exchange to and from the Isabel server.</span></span>  

<span data-ttu-id="0aed5-107">Als u de bankbestanden wilt uploaden of downloaden, moet u uw omgeving instellen om met Isabel te werken.</span><span class="sxs-lookup"><span data-stu-id="0aed5-107">To upload or download the bank files, you will have to set up your environment to work with Isabel.</span></span> [!INCLUDE[d365fin](../../includes/d365fin_md.md)] <span data-ttu-id="0aed5-108">communiceert met de CIS.dll via een COM-wrapper.</span><span class="sxs-lookup"><span data-stu-id="0aed5-108">communicates to the CIS.dll through a COM wrapper.</span></span>  

<span data-ttu-id="0aed5-109">Ga als volgt te werk om uw systeem geschikt te maken voor samenwerking met Isabel:</span><span class="sxs-lookup"><span data-stu-id="0aed5-109">To set up your system to work with Isabel, complete the following:</span></span>  

- <span data-ttu-id="0aed5-110">Installeer de Isabel-beveiligingsonderdelen.</span><span class="sxs-lookup"><span data-stu-id="0aed5-110">Install the Isabel security components.</span></span> <span data-ttu-id="0aed5-111">Raadpleeg voor meer informatie het downloadgedeelte op de [Isabel-website](https://go.microsoft.com/fwlink/?LinkId=210323).</span><span class="sxs-lookup"><span data-stu-id="0aed5-111">For more information, see the download area on the [Isabel website](https://go.microsoft.com/fwlink/?LinkId=210323).</span></span>  

- <span data-ttu-id="0aed5-112">Installeer de COM-wrapper van de Isabel-organisatie.</span><span class="sxs-lookup"><span data-stu-id="0aed5-112">Install the COM wrapper that is manufactured by the Isabel organization.</span></span> <span data-ttu-id="0aed5-113">Deze wrapper is opgenomen in het Isabel GO 6.20-pakket.</span><span class="sxs-lookup"><span data-stu-id="0aed5-113">This wrapper is included with the Isabel GO 6.20 package.</span></span>  

- <span data-ttu-id="0aed5-114">Registreer de COM-wrapper op uw computer.</span><span class="sxs-lookup"><span data-stu-id="0aed5-114">Register the COM wrapper on your computer.</span></span> <span data-ttu-id="0aed5-115">Zoek de CIS.dll bij de opdrachtprompt en voer vervolgens de opdracht **regsvr32 CISComWrapper.dll** uit.</span><span class="sxs-lookup"><span data-stu-id="0aed5-115">At the command prompt, locate the CIS.dll and then execute the **regsvr32 CISComWrapper.dll** command.</span></span>  

## <a name="see-also"></a><span data-ttu-id="0aed5-116">Zie ook</span><span class="sxs-lookup"><span data-stu-id="0aed5-116">See Also</span></span>  
 <span data-ttu-id="0aed5-117">[Isabel-website](https://go.microsoft.com/fwlink/?LinkId=210323) </span><span class="sxs-lookup"><span data-stu-id="0aed5-117">[Isabel website](https://go.microsoft.com/fwlink/?LinkId=210323) </span></span>  
 <span data-ttu-id="0aed5-118">[Elektronisch bankieren voor België](belgian-electronic-banking.md) </span><span class="sxs-lookup"><span data-stu-id="0aed5-118">[Belgian Electronic Banking](belgian-electronic-banking.md) </span></span>  
 [<span data-ttu-id="0aed5-119">Elektronisch bankieren instellen</span><span class="sxs-lookup"><span data-stu-id="0aed5-119">Set Up Electronic Banking</span></span>](how-to-set-up-electronic-banking.md)
