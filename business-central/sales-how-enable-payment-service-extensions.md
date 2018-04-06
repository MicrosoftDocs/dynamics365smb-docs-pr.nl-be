---
title: Klantbetalingen via betalingsservices inschakelen | Microsoft Docs
description: Maak het makkelijker voor klanten om facturen te betalen, door betalingsservices in te schakelen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: online payment
ms.date: 07/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 5853080ef39196e95c293415e9b81502ff03d5ed
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="enable-customer-payments-through-payment-services"></a><span data-ttu-id="ce21c-103">Klantbetalingen via betalingsservices inschakelen</span><span class="sxs-lookup"><span data-stu-id="ce21c-103">Enable Customer Payments Through Payment Services</span></span>
<span data-ttu-id="ce21c-104">Als alternatief voor het innen van betalingen door middel van bankoverschrijving of creditcards kunt u klanten laten betalen via hun account door middel van betalingsservices zoals Microsoft Pay, PayPal of WorldPay.</span><span class="sxs-lookup"><span data-stu-id="ce21c-104">As an alternative to collecting payments through bank transfer or credit cards, your customers can pay you through their account with payment services, such as Microsoft Pay, PayPal, or WorldPay.</span></span>  

<span data-ttu-id="ce21c-105">Nadat u een betalingsservice hebt ingeschakeld in [!INCLUDE[d365fin](includes/d365fin_md.md)], wordt een koppeling naar de service beschikbaar op verkoopdocumenten die u per e-mail naar uw klanten verzendt.</span><span class="sxs-lookup"><span data-stu-id="ce21c-105">After you enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)], a link to the service is available on sales documents that you send by email to your customers.</span></span> <span data-ttu-id="ce21c-106">De klanten kunnen met de koppeling naar de betalingsservice gaan en de factuur betalen, rechtstreeks vanuit het verkoopdocument.</span><span class="sxs-lookup"><span data-stu-id="ce21c-106">Customers can use the link to go to the payment service and pay the bill, directly from the sales document.</span></span> <span data-ttu-id="ce21c-107">Als u de koppeling niet wilt opnemen, bijvoorbeeld wanneer een klant met contant geld betaalt, kunt u de betalingsservice uit de factuur verwijderen voordat u hem boekt.</span><span class="sxs-lookup"><span data-stu-id="ce21c-107">If you don't want to include the link, for example, if a customer will pay with cash, you can remove the payment service from the invoice before posting.</span></span>  

<span data-ttu-id="ce21c-108">De extensies Microsoft Pay, PayPal Payments Standard en WorldPay Payments Standard zijn geïnstalleerd in [!INCLUDE[d365fin](includes/d365fin_md.md)] en u hoeft ze alleen maar in te schakelen.</span><span class="sxs-lookup"><span data-stu-id="ce21c-108">The Microsoft Pay, PayPal Payments Standard, and WorldPay Payments Standard extensions are installed in [!INCLUDE[d365fin](includes/d365fin_md.md)], and are ready for you to enable.</span></span>  

## <a name="to-enable-a-payment-service-in-included365finincludesd365finmdmd"></a><span data-ttu-id="ce21c-109">Een betalingsservice inschakelen in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="ce21c-109">To enable a payment service in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
1. <span data-ttu-id="ce21c-110">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Betalingsservices** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="ce21c-110">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ce21c-111">Kies in het venster **Betalingsservices** de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="ce21c-111">In the **Payment Services** window, choose the **New** action.</span></span>  
3. <span data-ttu-id="ce21c-112">Selecteer de betalingsservice en sluit vervolgens het venster.</span><span class="sxs-lookup"><span data-stu-id="ce21c-112">Select the payment service, and then close the window.</span></span>  
4. <span data-ttu-id="ce21c-113">Kies in het venster **Betalingsservices** de actie **Instellen**.</span><span class="sxs-lookup"><span data-stu-id="ce21c-113">In the **Payment Services** window, choose the **Setup** action.</span></span>  
5. <span data-ttu-id="ce21c-114">Vul indien nodig de velden in.</span><span class="sxs-lookup"><span data-stu-id="ce21c-114">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
6. <span data-ttu-id="ce21c-115">Sluit het venster.</span><span class="sxs-lookup"><span data-stu-id="ce21c-115">Close the window.</span></span>  

## <a name="to-select-a-payment-service-on-a-sales-invoice"></a><span data-ttu-id="ce21c-116">Een betalingsservice selecteren op een verkoopfactuur</span><span class="sxs-lookup"><span data-stu-id="ce21c-116">To select a payment service on a sales invoice</span></span>
1. <span data-ttu-id="ce21c-117">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verkoopfacturen** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="ce21c-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Sales Invoices**, and then choose the related link.</span></span>  
2. <span data-ttu-id="ce21c-118">Open de verkoopfactuur die u wilt betalen door middel van de betalingsservice.</span><span class="sxs-lookup"><span data-stu-id="ce21c-118">Open the sales invoice that you want to pay by using the payment service.</span></span>  
3. <span data-ttu-id="ce21c-119">Kies in het veld **Betalingsservice** de gewenste betalingsservice.</span><span class="sxs-lookup"><span data-stu-id="ce21c-119">In the **Payment Service** field, choose the payment service.</span></span>  

    > [!NOTE]  
    >   <span data-ttu-id="ce21c-120">Het veld **Betalingsservice** is alleen beschikbaar als u betalingsservices hebt ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="ce21c-120">The **Payment Service** field is available only if you've enabled the payment service.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ce21c-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ce21c-121">See Also</span></span>  
[<span data-ttu-id="ce21c-122">Verkopen instellen</span><span class="sxs-lookup"><span data-stu-id="ce21c-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="ce21c-123">Verkoop</span><span class="sxs-lookup"><span data-stu-id="ce21c-123">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="ce21c-124">[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="ce21c-124">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
<span data-ttu-id="ce21c-125">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ce21c-125">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

