---
title: Microsoft Pay Standaard| Microsoft Docs
description: Bevat informatie over de extensie Microsoft Pay
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 58c7ff08a7359b4f577b7ba40b23bc1f6310da4c
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787339"
---
# <a name="the-microsoft-pay-extension"></a><span data-ttu-id="c354c-103">De extensie Microsoft Pay</span><span class="sxs-lookup"><span data-stu-id="c354c-103">The Microsoft Pay Extension</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c354c-104">Met ingang van 8 februari 2020 hebben wijzigingen in de Microsoft Pay-service invloed op de Microsoft Pay-uitbreiding in Microsoft [!INCLUDE[prod_short](includes/prod_long.md)].</span><span class="sxs-lookup"><span data-stu-id="c354c-104">Effective February 8 2020, changes in the Microsoft Pay service will affect the Microsoft Pay extension in Microsoft [!INCLUDE[prod_short](includes/prod_long.md)].</span></span> <span data-ttu-id="c354c-105">Vanwege de wijzigingen zullen na 8 februari de betalingskoppelingen **Nu betalen** die de Microsoft Pay-uitbreiding genereert voor facturen in [!INCLUDE[prod_short](includes/prod_short.md)], Microsoft Pay niet openen.</span><span class="sxs-lookup"><span data-stu-id="c354c-105">Due to the changes, after February 8, the **Pay now** payment links that the Microsoft Pay extension generates for invoices in [!INCLUDE[prod_short](includes/prod_short.md)] will not open Microsoft Pay.</span></span> <span data-ttu-id="c354c-106">Klanten die de uitbreiding gebruiken, moeten hun betalingsservices instellen om in plaats daarvan de PayPal-uitbreiding te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="c354c-106">Customers who are using the extension should change their Payment Services setup to start using the PayPal extension instead.</span></span><br /></br>
>
> <span data-ttu-id="c354c-107">Vanaf 8 januari zullen we een melding weergeven in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="c354c-107">From January 8, we will display a notification in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="c354c-108">De melding bevat een koppeling naar de instellingen die u moet wijzigen en naar meer informatie.</span><span class="sxs-lookup"><span data-stu-id="c354c-108">The notification will contain a link to the settings that you need to change and to more information.</span></span> <span data-ttu-id="c354c-109">Na 8 februari is de Microsoft Pay-uitbrieding niet meer beschikbaar in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="c354c-109">After February 8, the Microsoft Pay extension will no longer be available in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span><br /></br>
>
> <span data-ttu-id="c354c-110">De wijzigingen zijn van invloed op de volgende versies van Business Central:</span><span class="sxs-lookup"><span data-stu-id="c354c-110">The changes impact the following versions of Business Central:</span></span>
> - <span data-ttu-id="c354c-111">Microsoft Dynamics 365 Business Central oktober 2018</span><span class="sxs-lookup"><span data-stu-id="c354c-111">Microsoft Dynamics 365 Business Central October 2018</span></span>
> - <span data-ttu-id="c354c-112">Microsoft Dynamics 365 Business Central april 2019</span><span class="sxs-lookup"><span data-stu-id="c354c-112">Microsoft Dynamics 365 Business Central April 2019</span></span>
> - <span data-ttu-id="c354c-113">Microsoft Dynamics 365 Business Central 2019 releasewave 2</span><span class="sxs-lookup"><span data-stu-id="c354c-113">Microsoft Dynamics 365 Business Central 2019 Release Wave 2</span></span>

<span data-ttu-id="c354c-114">Klanten stellen steeds meer eisen aan de klantenservice, zowel met betrekking tot productkwaliteit als met betrekking tot services voor betaling en levering.</span><span class="sxs-lookup"><span data-stu-id="c354c-114">Customers continuously require higher customer service, both in terms of the quality of product but also in terms of delivery and payment services.</span></span> <span data-ttu-id="c354c-115">De service Microsoft Pay helpt u uw klantenservice te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="c354c-115">The Microsoft Pay service helps you increase your customer service.</span></span>

<span data-ttu-id="c354c-116">De extensie Microsoft Pay voegt een Microsoft Pay-koppeling aan uw verkoopdocumenten toe, zodat klanten gemakkelijk kunnen betalen met Microsoft Pay.</span><span class="sxs-lookup"><span data-stu-id="c354c-116">The Microsoft Pay extension adds a Microsoft Pay link to your sales documents so customers can easily pay using Microsoft Pay.</span></span> <span data-ttu-id="c354c-117">Vervolgens kunt u de documenten per e-mail verzenden. U biedt zo een betere klantenservice en ontvangt betalingen van uw klanten sneller op uw bankrekening.</span><span class="sxs-lookup"><span data-stu-id="c354c-117">Then you can send the documents by email to provide higher customer service and shorten the time it takes for customers’ payments to arrive on your bank account.</span></span>

<span data-ttu-id="c354c-118">De extensie Microsoft Pay biedt de volgende voordelen:</span><span class="sxs-lookup"><span data-stu-id="c354c-118">The Microsoft Pay extension provides the following benefits:</span></span>
- <span data-ttu-id="c354c-119">Klantbetalingen komen sneller binnen op uw bankrekening.</span><span class="sxs-lookup"><span data-stu-id="c354c-119">Customer payments appear faster on your bank account.</span></span>
- <span data-ttu-id="c354c-120">Klanten kunnen op meer manieren facturen betalen.</span><span class="sxs-lookup"><span data-stu-id="c354c-120">Customers have more ways to pay invoices.</span></span>
- <span data-ttu-id="c354c-121">Microsoft Pay biedt een betrouwbare betalingsservice, die klanten liever gebruiken dan dat ze creditcardinformatie op onbekende websites invoeren.</span><span class="sxs-lookup"><span data-stu-id="c354c-121">Microsoft Pay offers a trustworthy payment service, which customers prefer to entering credit card information on unknown web sites.</span></span>
- <span data-ttu-id="c354c-122">Microsoft Pay biedt meerdere manieren om betalingen te verwerken, inclusief creditcardverwerking, zoals PayPal en Stripe.</span><span class="sxs-lookup"><span data-stu-id="c354c-122">Microsoft Pay offers multiple ways of handling payments, including credit card processing, such as PayPal and Stripe.</span></span>
- <span data-ttu-id="c354c-123">De Microsoft Pay-koppeling kan automatisch worden ingesloten op elk factuurdocument of door de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="c354c-123">The Microsoft Pay link can be embedded automatically on every invoice document or by the user.</span></span>
- <span data-ttu-id="c354c-124">Aangezien deze functie als extensie wordt samengesteld, hebt u de volledige controle om deze in te schakelen wanneer uw bedrijfsprocessen dit vereisen.</span><span class="sxs-lookup"><span data-stu-id="c354c-124">Because this functionality is built as an extension, it gives you full control to enable it when and if your business processes require it.</span></span>

<span data-ttu-id="c354c-125">Het inschakelen van extensies voor betalingsservices is in [!INCLUDE[prod_short](includes/prod_short.md)] gratis. U moet wel contact opnemen met de betalingsservice om een rekening aan te vragen.</span><span class="sxs-lookup"><span data-stu-id="c354c-125">Enabling payment service extensions is free in [!INCLUDE[prod_short](includes/prod_short.md)], however, you will need to contact the payment service to get an account.</span></span> <span data-ttu-id="c354c-126">Zie [Klantbetalingen via betalingsservices inschakelen](sales-how-enable-payment-service-extensions.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="c354c-126">For more information, see [Enable Customer Payment Through Payment Services](sales-how-enable-payment-service-extensions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c354c-127">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c354c-127">See Also</span></span>
<span data-ttu-id="c354c-128">[[!INCLUDE[prod_short](includes/prod_short.md)] aanpassen met behulp van extensies](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="c354c-128">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="c354c-129">Verkopen instellen</span><span class="sxs-lookup"><span data-stu-id="c354c-129">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="c354c-130">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c354c-130">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]