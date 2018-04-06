---
title: Betalingsbestanden uploaden naar een Isabel-server
description: "Betalingsbestanden kunnen worden geüpload via het venster **IBS-logboeken**. U kunt alleen betalingsbestanden uploaden als de velden **Uploadintegratiemodus** en **Downloadintegratiemodus** in het venster **Elektronisch bankieren instellen** zijn ingesteld op **Met toezicht**."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: f442088e4244880cfa6f856f332a0f7985237062
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="upload-payment-files-to-an-isabel-server"></a><span data-ttu-id="db91f-104">Betalingsbestanden uploaden naar een Isabel-server</span><span class="sxs-lookup"><span data-stu-id="db91f-104">Upload Payment Files to an Isabel Server</span></span>
> [!Note]
> [!INCLUDE[onprem_only](../../includes/onprem_only_md.md)]

<span data-ttu-id="db91f-105">Betalingsbestanden kunnen worden geüpload via het venster **IBS-logboeken**.</span><span class="sxs-lookup"><span data-stu-id="db91f-105">Payment files can be uploaded using the **IBS Logs** window.</span></span> <span data-ttu-id="db91f-106">U kunt alleen betalingsbestanden uploaden als de velden **Uploadintegratiemodus** en **Downloadintegratiemodus** in het venster **Elektronisch bankieren instellen** zijn ingesteld op **Met toezicht**.</span><span class="sxs-lookup"><span data-stu-id="db91f-106">The **Upload Integration Mode** and **Download Integration Mode** fields in the **Electronic Banking Setup** window must be set to **Attended** to upload payment files.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="db91f-107">Voordat u betalingbestanden kunt uploaden, moet u zijn aangemeld bij de Isabel-server.</span><span class="sxs-lookup"><span data-stu-id="db91f-107">Before you can upload payment files you must be logged on to the Isabel server.</span></span>  

## <a name="to-upload-payment-files-in-attended-mode"></a><span data-ttu-id="db91f-108">Betalingsbestanden uploaden in de modus Met toezicht</span><span class="sxs-lookup"><span data-stu-id="db91f-108">To upload payment files in attended mode</span></span>  

1.  <span data-ttu-id="db91f-109">Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **IBS-logboeken** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="db91f-109">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **IBS Logs**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="db91f-110">Kies de actie **Contract en gebruiker ophalen**.</span><span class="sxs-lookup"><span data-stu-id="db91f-110">Choose the **Get Contract and User** action.</span></span>  
3.  <span data-ttu-id="db91f-111">Na het verifiëren van de betalingbestanden worden een gebruikers- en contract- id weergegeven in de velden **IBS-gebruikers-id** en **IBS-contract-id**.</span><span class="sxs-lookup"><span data-stu-id="db91f-111">After verifying the payment files, a user ID and contract ID will be displayed in the **IBS User ID** and **IBS Contract ID** fields.</span></span>  

    <span data-ttu-id="db91f-112">Het veld **Uploadstatus** wordt ingesteld op **Gereed voor uploaden**.</span><span class="sxs-lookup"><span data-stu-id="db91f-112">The **Upload Status** field will be set to **Ready for Upload**.</span></span> <span data-ttu-id="db91f-113">Als op de Isabel-server meerdere contracten voor de bankrekening bestaan, wordt **Uploadstatus** ingesteld op **Conflict bestaat**.</span><span class="sxs-lookup"><span data-stu-id="db91f-113">If more than one contract exists on the Isabel server for the bank account, the **Upload Status** will be set to **Conflict Exists**.</span></span> <span data-ttu-id="db91f-114">Selecteer het juiste contract.</span><span class="sxs-lookup"><span data-stu-id="db91f-114">Select the correct contract.</span></span>  

4.  <span data-ttu-id="db91f-115">Kies de actie **Downloaden**.</span><span class="sxs-lookup"><span data-stu-id="db91f-115">Choose the **Perform Download** action.</span></span> <span data-ttu-id="db91f-116">De betalingsbestanden worden geüpload naar de Isabel-server en het veld **Verwerkingsstatus** wordt ingesteld op **Verwerkt**.</span><span class="sxs-lookup"><span data-stu-id="db91f-116">The payment files will be uploaded to the Isabel server and the **Process Status** field will be set to **Processed**.</span></span>  
5.  <span data-ttu-id="db91f-117">Vervolg het verwerken van de betalingsbestanden door de bestanden op de Isabel-server te ondertekenen en te verzenden.</span><span class="sxs-lookup"><span data-stu-id="db91f-117">Continue processing the payment files by signing and sending the files on the Isabel server.</span></span>  

## <a name="see-also"></a><span data-ttu-id="db91f-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="db91f-118">See Also</span></span>  
 [<span data-ttu-id="db91f-119">IBS-logposten archiveren</span><span class="sxs-lookup"><span data-stu-id="db91f-119">Archive IBS Log Entries</span></span>](how-to-archive-ibs-log-entries.md)

