---
title: Voorkeursmethoden voor verzending van verkoopdocumenten instellen | Microsoft Docs
description: Beschrijft hoe u voor elke klant de voorkeursmethode voor het verzenden van verkoopdocumenten instelt, bijvoorbeeld e-mailadres, PDF, elektronisch document, enzovoort.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: email, PDF, electronic document
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7f7499e6e501207ed5fd6ebbee5b94d18c1d008e
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-document-sending-profiles"></a><span data-ttu-id="863c5-103">Procedure: Verzendprofielen voor documenten instellen</span><span class="sxs-lookup"><span data-stu-id="863c5-103">How to: Set Up Document Sending Profiles</span></span>
<span data-ttu-id="863c5-104">U kunt elke klant instellen met een voorkeursmethode voor de verzending van verkoopdocumenten, zodat u niet elke keer dat u de actie **Boeken en verzenden** kiest een verzendoptie hoeft te selecteren.</span><span class="sxs-lookup"><span data-stu-id="863c5-104">You can set each customer up with a preferred method of sending sales documents, so that you do not have to select a sending option every time you choose the **Post and Send** action.</span></span>

<span data-ttu-id="863c5-105">In het venster **Verzendprofielen van documenten** kunt u verschillende verzendprofielen instellen waaruit u kunt kiezen in het veld **Verzendprofiel van document** op een klantenkaart.</span><span class="sxs-lookup"><span data-stu-id="863c5-105">In the **Document Sending Profiles** window, you set up different sending profiles that you can select from in the **Document Sending Profile** field on a customer card.</span></span> <span data-ttu-id="863c5-106">U kunt het selectievakje **Standaard** selecteren om aan te geven dat het verzendprofiel van het document het standaardprofiel is voor alle klanten, behalve voor klanten waarvoor in het veld **Verzendprofiel van document** een ander profiel staat.</span><span class="sxs-lookup"><span data-stu-id="863c5-106">You can select the **Default** check box to specify that the document sending profile is the default profile for all customers, except for customers where the **Document Sending Profile** field is filled with another sending profile.</span></span>

<span data-ttu-id="863c5-107">Wanneer u de actie **Boeken en verzenden** in een verkoopdocument kiest, wordt in het dialoogvenster **Boeken en verzenden bevestigen** het gebruikte verzendprofiel getoond. Dit is het voor de klant ingestelde profiel of het standaardprofiel voor alle klanten.</span><span class="sxs-lookup"><span data-stu-id="863c5-107">When you choose the **Post and Send** action on a sales document, the **Post and Send Confirmation** dialog box shows the sending profile used, either the one set up for the customer or the default for all customers.</span></span> <span data-ttu-id="863c5-108">In het dialoogvenster kunt u het verzendprofiel voor het verkoopdocument wijzigen.</span><span class="sxs-lookup"><span data-stu-id="863c5-108">In the dialog box, you can change the sending profile for the sales document.</span></span> <span data-ttu-id="863c5-109">Zie [Procedure: Verkopen factureren](sales-how-invoice-sales.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="863c5-109">For more information, see [How to: Invoice Sales](sales-how-invoice-sales.md).</span></span>

## <a name="to-set-up-a-document-sending-profile"></a><span data-ttu-id="863c5-110">Een verzendprofiel voor documenten instellen</span><span class="sxs-lookup"><span data-stu-id="863c5-110">To set up a document sending profile</span></span>
1. <span data-ttu-id="863c5-111">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verzendprofielen van documenten** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="863c5-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Document Sending Profiles**, and then choose the related link.</span></span>
2. <span data-ttu-id="863c5-112">Kies in het venster **Verzendprofielen van documenten** de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="863c5-112">In the **Document Sending Profiles** window, choose the **New** action.</span></span>
3. <span data-ttu-id="863c5-113">Vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="863c5-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a><span data-ttu-id="863c5-114">Een verzendprofiel op een klantenkaart opgeven</span><span class="sxs-lookup"><span data-stu-id="863c5-114">To specify a sending profile on a customer card</span></span>
1. <span data-ttu-id="863c5-115">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Klanten** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="863c5-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="863c5-116">Open de kaart van de klant voor wie u een verzendprofiel wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="863c5-116">Open the card of the customer who you want to set up a sending profile for.</span></span>
3. <span data-ttu-id="863c5-117">Selecteer op het sneltabblad **Verzendprofiel van document** een profiel dat u hebt ingesteld, zoals beschreven in de vorige procedure.</span><span class="sxs-lookup"><span data-stu-id="863c5-117">In the **Document Sending Profile** field, select a profile that you have set up as described in the previous procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="863c5-118">Zie ook</span><span class="sxs-lookup"><span data-stu-id="863c5-118">See Also</span></span>
[<span data-ttu-id="863c5-119">Verkopen instellen</span><span class="sxs-lookup"><span data-stu-id="863c5-119">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="863c5-120">Verkoop</span><span class="sxs-lookup"><span data-stu-id="863c5-120">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="863c5-121">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="863c5-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

