---
title: 'Procedure: VK-postcode-extensie GetAddress.io UK instellen | Microsoft Docs'
description: Beschrijft de algemene functies die u gebruikt om te werken met gegevens in Financials, zoals waarden invoeren, gegevens sorteren en weergaven wijzigen.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: getaddress.io, postcodes, extension
ms.date: 06/02/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: c5a99f7a90b2f832bba3eb088d0faa7514c14708
ms.contentlocale: nl-be
ms.lasthandoff: 09/11/2017

---
# <a name="how-to-set-up-the-getaddressio-uk-postcodes-extension"></a><span data-ttu-id="72689-103">Procedure: De VK-postcode-extensie GetAddress.io UK instellen</span><span class="sxs-lookup"><span data-stu-id="72689-103">How to: Set Up the GetAddress.io UK Postcodes Extension</span></span>
<span data-ttu-id="72689-104">De extensie maakt het eenvoudig om adressen in het VK in te voeren voor entiteiten zoals klanten, contactpersonen, medewerkers, leveranciers, bankrekeningen e.d.</span><span class="sxs-lookup"><span data-stu-id="72689-104">This extension makes it easy to enter addresses in the UK for entities like customers, contacts, employees, vendors, bank accounts, and so on.</span></span> 

<span data-ttu-id="72689-105">De extensie GetAddress.io UK Postcodes gebruikt de getAddress-API om adressen te vinden in postcodes in het VK.</span><span class="sxs-lookup"><span data-stu-id="72689-105">The GetAddress.io UK Postcodes extension uses the getAddress API to find addresses in postcodes in the UK.</span></span> <span data-ttu-id="72689-106">Als u de extensie wilt gebruiken, moet u een abonnement en een API-sleutel voor de getAddress-API hebben.</span><span class="sxs-lookup"><span data-stu-id="72689-106">To use the extension, you need to get a plan and an API Key for the getAddress API.</span></span> <span data-ttu-id="72689-107">Dat is heel eenvoudig. Wij helpen u deze te krijgen wanneer u de extensie GetAddress.io UK Postcodes configureert.</span><span class="sxs-lookup"><span data-stu-id="72689-107">That's easy, and we help you do that when you set up the GetAddress.io UK Postcodes extension.</span></span> <span data-ttu-id="72689-108">Het abonnement is gebaseerd op gebruik, of wat wordt aangeduid als ´calls´.</span><span class="sxs-lookup"><span data-stu-id="72689-108">Plans are based on use, or what's sometimes referred to as calls.</span></span> <span data-ttu-id="72689-109">Een call (of aanroep) is in dit geval wanneer [!INCLUDE[d365fin](includes/d365fin_md.md)] een lijst met adressen in een postcode weergeeft.</span><span class="sxs-lookup"><span data-stu-id="72689-109">A call, in this case, is when [!INCLUDE[d365fin](includes/d365fin_md.md)] displays a list of addresses in a postcode.</span></span> <span data-ttu-id="72689-110">U kiest het meest geschikte abonnement op basis van hoe vaak u adressen moet toevoegen.</span><span class="sxs-lookup"><span data-stu-id="72689-110">Depending on how often you add addresses, choose the plan that is best for you.</span></span> <span data-ttu-id="72689-111">Als u op de pagina alleen **Get API Key** kiest, krijgt u een **Free** abonnement. Daarmee kunt u 20 adressen per dag toevoegen en het is geldig voor 30 dagen.</span><span class="sxs-lookup"><span data-stu-id="72689-111">If you just choose **Get API Key** in the page, you'll use the **Free** plan, which lets you add 20 addresses per day, and is valid for 30 days.</span></span> 

##<a name="to-set-up-the-getaddressio-uk-postcodes-extension"></a><span data-ttu-id="72689-112">De extensie GetAddress.io UK Postcodes instellen</span><span class="sxs-lookup"><span data-stu-id="72689-112">To set up the GetAddress.io UK Postcodes extension</span></span> 
1. <span data-ttu-id="72689-113">Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Serviceverbindingen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="72689-113">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Connections**, and then choose the related link.</span></span>  
2. <span data-ttu-id="72689-114">Kies in het venster **Serviceverbindingen** de waarde **UK Postcode Service**.</span><span class="sxs-lookup"><span data-stu-id="72689-114">In the **Service Connections** window, choose **UK Postcode Service**.</span></span>
3. <span data-ttu-id="72689-115">Kies op de pagina **Postcode provider configuration** de optie **Disabled** (uitgeschakeld).</span><span class="sxs-lookup"><span data-stu-id="72689-115">In the **Postcode provider configuration** page, choose **Disabled**.</span></span>
4. <span data-ttu-id="72689-116">Kies in het venster **Postal code service selection** de optie **GetAddress.io**.</span><span class="sxs-lookup"><span data-stu-id="72689-116">In the **Postal code service selection** window, choose **GetAddress.io**.</span></span>
5. <span data-ttu-id="72689-117">Kies in het venster **GetAddress.io Config** de optie **Get API Key**. De pagina **Plans** op de website van getAddress API wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="72689-117">In the **GetAddress.io Config** window, choose **Get API Key** to open the **Plans** page on the website for the getAddress API.</span></span>  

    > [!NOTE]  
>   <span data-ttu-id="72689-118">U moet mogelijk pop-ups in uw browser toestaan.</span><span class="sxs-lookup"><span data-stu-id="72689-118">You might need to allow pop-ups in your browser.</span></span>
6. <span data-ttu-id="72689-119">Schaf een abonnement aan of kies **Get API Key** en geef uw e-mailadres op.</span><span class="sxs-lookup"><span data-stu-id="72689-119">Purchase a plan, or just choose **Get API Key**, and then provide your email address.</span></span>
7. <span data-ttu-id="72689-120">Open de e-mail die u van getAddress.io krijgt en kopieer de API-code.</span><span class="sxs-lookup"><span data-stu-id="72689-120">Open the email from getAddress.io, and copy the API key.</span></span> <span data-ttu-id="72689-121">De code vindt u onder de koptekst **Your API Key**.</span><span class="sxs-lookup"><span data-stu-id="72689-121">The key is under the **Your API Key** heading.</span></span>
8. <span data-ttu-id="72689-122">Plak in het venster **GetAddress.io Config** de API-code in het veld **API key** en kies **OK**.</span><span class="sxs-lookup"><span data-stu-id="72689-122">In the **GetAddress.io Config** window, paste the API key in the **API Key** field, and then choose **OK**.</span></span>
9. <span data-ttu-id="72689-123">Controleer of op de pagina **Serviceverbindingen** in het veld **Address Provider** de waarde **GetAddress.io** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="72689-123">In the **Service Connections** page, verify that the **Address Provider** field shows **GetAddress.io**.</span></span> <span data-ttu-id="72689-124">Als dit zo is, is de service ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="72689-124">If it does, the service is enabled.</span></span>

## <a name="see-also"></a><span data-ttu-id="72689-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="72689-125">See Also</span></span>
<span data-ttu-id="72689-126">[VK-postcodes GetAddress.io](ui-extensions-getaddressio.md)
[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met extensies](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="72689-126">[GetAddress.io UK Postcodes](ui-extensions-getaddressio.md)
[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="72689-127">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="72689-127">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
