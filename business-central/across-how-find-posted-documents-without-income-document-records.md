---
title: Documenten zonder bijlagen zoeken| Microsoft Docs
Description: U kunt grootboekposten zoeken voor geboekte inkoop- en verkoopdocumenten die geen elektronische inkomende documenten hebben, zoals geïmporteerde facturen.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 79504010d6bb4f2afb0f09f866991dd76f6e35b5
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "923706"
---
# <a name="find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="ebc8b-103">Geboekte documenten zonder inkomende documentrecords zoeken</span><span class="sxs-lookup"><span data-stu-id="ebc8b-103">Find Posted Documents without Incoming Document Records</span></span>
<span data-ttu-id="ebc8b-104">Vanuit de pagina's **Rekeningschema** en **Grootboekposten** kunt u zoeken naar grootboekposten voor geboekte inkoop- en verkoopdocumenten die geen inkomende documentrecords hebben, en deze centraal koppelen aan bestaande records of nieuwe records maken met gekoppelde documentbestanden.</span><span class="sxs-lookup"><span data-stu-id="ebc8b-104">From the **Chart of Accounts** and **General Ledger Entries** pages, you can use a search function to find general ledger entries for posted purchase and sales documents that do not have incoming document records and then centrally link to existing records or create new ones with attached document files.</span></span>

## <a name="to-find-posted-documents-without-incoming-document-records"></a><span data-ttu-id="ebc8b-105">Geboekte documenten zonder inkomende documentrecords zoeken</span><span class="sxs-lookup"><span data-stu-id="ebc8b-105">To find posted documents without incoming document records</span></span>
1. <span data-ttu-id="ebc8b-106">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="ebc8b-106">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Chart of Accounts**, and then choose the related link.</span></span>
2. <span data-ttu-id="ebc8b-107">Selecteer een regel voor een grootboekrekening waarvan de grootboekposten die u wilt zien, geboekte inkoop- en verkoopdocumenten zijn zonder inkomende documentrecords en kies vervolgens de actie **Geboekte documenten zonder inkomend document**.</span><span class="sxs-lookup"><span data-stu-id="ebc8b-107">Select a line for a G/L account for whose general ledger entries you want to see posted purchase and sales documents without incoming document records, and then choose the **Posted Documents without Incoming Document** action.</span></span>
3. <span data-ttu-id="ebc8b-108">U kunt ook de actie **Posten** kiezen.</span><span class="sxs-lookup"><span data-stu-id="ebc8b-108">Alternatively, choose the **Ledger Entries** action.</span></span>
4. <span data-ttu-id="ebc8b-109">Kies op de pagina **Grootboekposten** de actie **Geboekte documenten zonder inkomend document**.</span><span class="sxs-lookup"><span data-stu-id="ebc8b-109">On the **General Ledger Entries** page, choose the **Posted Documents without Incoming Documents** action.</span></span>

<span data-ttu-id="ebc8b-110">De pagina **Geboekte documenten zonder inkomend document** wordt geopend en toont geboekte inkoop- en verkoopdocumenten zonder inkomende documentrecords die worden gerepresenteerd door grootboekposten in de Grootboekrekening waarvoor u de pagina hebt geopend.</span><span class="sxs-lookup"><span data-stu-id="ebc8b-110">The **Posted Documents without Incoming Document** page opens showing posted purchase and sales documents without incoming document records represented by general ledger entries on the G/L account that you opened the page for.</span></span> <span data-ttu-id="ebc8b-111">De pagina kan maximaal 1000 regels weergeven.</span><span class="sxs-lookup"><span data-stu-id="ebc8b-111">The page can show a maximum of 1000 lines.</span></span> <span data-ttu-id="ebc8b-112">Standaard bevat het veld **Datumfilter** daarom een filter dat de regels beperkt tot posten met een boekingsdatum vanaf het begin van de boekhoudperiode tot de werkdatum.</span><span class="sxs-lookup"><span data-stu-id="ebc8b-112">By default, the **Date Filter** field therefore contains a filter that limits the lines to entries with posting dates from the beginning of the accounting period to the work date.</span></span>

## <a name="to-connect-found-documents-to-existing-incoming-document-records"></a><span data-ttu-id="ebc8b-113">Gevonden documenten koppelen aan bestaande inkomende documentrecords</span><span class="sxs-lookup"><span data-stu-id="ebc8b-113">To connect found documents to existing incoming document records</span></span>
1. <span data-ttu-id="ebc8b-114">Selecteer op de pagina **Geboekte documenten zonder inkomend document** de regel voor een geboekt document dat u wilt koppelen aan een bestaande inkomende documentrecord en kies vervolgens de actie **Inkomend document selecteren** .</span><span class="sxs-lookup"><span data-stu-id="ebc8b-114">On the **Posted Documents without Incoming Document** page, select the line for a posted document that you want to connect to an existing incoming document record, and then choose the **Select Incoming Document** action.</span></span>
2. <span data-ttu-id="ebc8b-115">Selecteer op de pagina **Inkomende documenten** de inkomende documentrecord die u wilt koppelen aan het gevonden geboekte document en kies vervolgens de knop **OK**.</span><span class="sxs-lookup"><span data-stu-id="ebc8b-115">On the **Incoming Documents** page, select the incoming document record that you want to connect to posted document found, and then choose the **OK** button.</span></span>
3. <span data-ttu-id="ebc8b-116">Selecteer op de pagina **Geboekte documenten zonder inkomend document** de inkomende documentrecord die nu is gekoppeld aan het geboekte document, zoals u kunt zien in het feitenblok **Inkomende documentbestanden**.</span><span class="sxs-lookup"><span data-stu-id="ebc8b-116">On the **Posted Documents without Incoming Document** page, the selected incoming document record is now connected to the posted document, as you can see in the **Incoming Document Files** FactBox.</span></span>

<span data-ttu-id="ebc8b-117">Als er geen relevante inkomende documentrecord op de pagina **Inkomende documenten** staat, kunt u er een maken.</span><span class="sxs-lookup"><span data-stu-id="ebc8b-117">If a relevant incoming document record does not exist on the **Incoming Documents** page, then you can create it.</span></span> <span data-ttu-id="ebc8b-118">Zie [Inkomende documentrecords maken](across-how-create-income-document-records.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ebc8b-118">For more information, see [Create Incoming Document Records](across-how-create-income-document-records.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ebc8b-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ebc8b-119">See Also</span></span>
[<span data-ttu-id="ebc8b-120">Inkomende documenten verwerken</span><span class="sxs-lookup"><span data-stu-id="ebc8b-120">Process Incoming Documents</span></span>](across-process-income-documents.md)  
[<span data-ttu-id="ebc8b-121">Inkomende documenten</span><span class="sxs-lookup"><span data-stu-id="ebc8b-121">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="ebc8b-122">Inkoop</span><span class="sxs-lookup"><span data-stu-id="ebc8b-122">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="ebc8b-123">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ebc8b-123">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
