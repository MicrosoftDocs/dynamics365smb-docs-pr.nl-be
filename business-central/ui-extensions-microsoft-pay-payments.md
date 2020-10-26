---
title: Microsoft Pay Standaard| Microsoft Docs
description: Bevat informatie over de extensie Microsoft Pay
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 5885674316e082323462cbad9fce3f20590f06d5
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3915047"
---
# <a name="the-microsoft-pay-extension"></a><span data-ttu-id="d9d09-103">De extensie Microsoft Pay</span><span class="sxs-lookup"><span data-stu-id="d9d09-103">The Microsoft Pay Extension</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d9d09-104">Met ingang van 8 februari 2020 hebben wijzigingen in de Microsoft Pay-service invloed op de Microsoft Pay-uitbreiding in Microsoft [!INCLUDE[d365fin](includes/d365fin_long_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d9d09-104">Effective February 8 2020, changes in the Microsoft Pay service will affect the Microsoft Pay extension in Microsoft [!INCLUDE[d365fin](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="d9d09-105">Vanwege de wijzigingen zullen na 8 februari de betalingskoppelingen **Nu betalen** die de Microsoft Pay-uitbreiding genereert voor facturen in [!INCLUDE[d365fin](includes/d365fin_md.md)], Microsoft Pay niet openen.</span><span class="sxs-lookup"><span data-stu-id="d9d09-105">Due to the changes, after February 8, the **Pay now** payment links that the Microsoft Pay extension generates for invoices in [!INCLUDE[d365fin](includes/d365fin_md.md)] will not open Microsoft Pay.</span></span> <span data-ttu-id="d9d09-106">Klanten die de uitbreiding gebruiken, moeten hun betalingsservices instellen om in plaats daarvan de PayPal-uitbreiding te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="d9d09-106">Customers who are using the extension should change their Payment Services setup to start using the PayPal extension instead.</span></span><br /></br>
>
> <span data-ttu-id="d9d09-107">Vanaf 8 januari zullen we een melding weergeven in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d9d09-107">From January 8, we will display a notification in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="d9d09-108">De melding bevat een koppeling naar de instellingen die u moet wijzigen en naar meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d9d09-108">The notification will contain a link to the settings that you need to change and to more information.</span></span> <span data-ttu-id="d9d09-109">Na 8 februari is de Microsoft Pay-uitbrieding niet meer beschikbaar in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="d9d09-109">After February 8, the Microsoft Pay extension will no longer be available in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span><br /></br>
>
> <span data-ttu-id="d9d09-110">De wijzigingen zijn van invloed op de volgende versies van Business Central:</span><span class="sxs-lookup"><span data-stu-id="d9d09-110">The changes impact the following versions of Business Central:</span></span>
> - <span data-ttu-id="d9d09-111">Microsoft Dynamics 365 Business Central oktober 2018</span><span class="sxs-lookup"><span data-stu-id="d9d09-111">Microsoft Dynamics 365 Business Central October 2018</span></span>
> - <span data-ttu-id="d9d09-112">Microsoft Dynamics 365 Business Central april 2019</span><span class="sxs-lookup"><span data-stu-id="d9d09-112">Microsoft Dynamics 365 Business Central April 2019</span></span>
> - <span data-ttu-id="d9d09-113">Microsoft Dynamics 365 Business Central 2019 releasewave 2</span><span class="sxs-lookup"><span data-stu-id="d9d09-113">Microsoft Dynamics 365 Business Central 2019 Release Wave 2</span></span>

<span data-ttu-id="d9d09-114">Klanten stellen steeds meer eisen aan de klantenservice, zowel met betrekking tot productkwaliteit als met betrekking tot services voor betaling en levering.</span><span class="sxs-lookup"><span data-stu-id="d9d09-114">Customers continuously require higher customer service, both in terms of the quality of product but also in terms of delivery and payment services.</span></span> <span data-ttu-id="d9d09-115">De service Microsoft Pay helpt u uw klantenservice te verbeteren.</span><span class="sxs-lookup"><span data-stu-id="d9d09-115">The Microsoft Pay service helps you increase your customer service.</span></span>

<span data-ttu-id="d9d09-116">De extensie Microsoft Pay voegt een Microsoft Pay-koppeling aan uw verkoopdocumenten toe, zodat klanten gemakkelijk kunnen betalen met Microsoft Pay.</span><span class="sxs-lookup"><span data-stu-id="d9d09-116">The Microsoft Pay extension adds a Microsoft Pay link to your sales documents so customers can easily pay using Microsoft Pay.</span></span> <span data-ttu-id="d9d09-117">Vervolgens kunt u de documenten per e-mail verzenden. U biedt zo een betere klantenservice en ontvangt betalingen van uw klanten sneller op uw bankrekening.</span><span class="sxs-lookup"><span data-stu-id="d9d09-117">Then you can send the documents by email to provide higher customer service and shorten the time it takes for customers’ payments to arrive on your bank account.</span></span>

<span data-ttu-id="d9d09-118">De extensie Microsoft Pay biedt de volgende voordelen:</span><span class="sxs-lookup"><span data-stu-id="d9d09-118">The Microsoft Pay extension provides the following benefits:</span></span>
- <span data-ttu-id="d9d09-119">Klantbetalingen komen sneller binnen op uw bankrekening.</span><span class="sxs-lookup"><span data-stu-id="d9d09-119">Customer payments appear faster on your bank account.</span></span>
- <span data-ttu-id="d9d09-120">Klanten kunnen op meer manieren facturen betalen.</span><span class="sxs-lookup"><span data-stu-id="d9d09-120">Customers have more ways to pay invoices.</span></span>
- <span data-ttu-id="d9d09-121">Microsoft Pay biedt een betrouwbare betalingsservice, die klanten liever gebruiken dan dat ze creditcardinformatie op onbekende websites invoeren.</span><span class="sxs-lookup"><span data-stu-id="d9d09-121">Microsoft Pay offers a trustworthy payment service, which customers prefer to entering credit card information on unknown web sites.</span></span>
- <span data-ttu-id="d9d09-122">Microsoft Pay biedt meerdere manieren om betalingen te verwerken, inclusief creditcardverwerking, zoals PayPal en Stripe.</span><span class="sxs-lookup"><span data-stu-id="d9d09-122">Microsoft Pay offers multiple ways of handling payments, including credit card processing, such as PayPal and Stripe.</span></span>
- <span data-ttu-id="d9d09-123">De Microsoft Pay-koppeling kan automatisch worden ingesloten op elk factuurdocument of door de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="d9d09-123">The Microsoft Pay link can be embedded automatically on every invoice document or by the user.</span></span>
- <span data-ttu-id="d9d09-124">Aangezien deze functie als extensie wordt samengesteld, hebt u de volledige controle om deze in te schakelen wanneer uw bedrijfsprocessen dit vereisen.</span><span class="sxs-lookup"><span data-stu-id="d9d09-124">Because this functionality is built as an extension, it gives you full control to enable it when and if your business processes require it.</span></span>

<span data-ttu-id="d9d09-125">Het inschakelen van extensies voor betalingsservices is in [!INCLUDE[d365fin](includes/d365fin_md.md)] gratis. U moet wel contact opnemen met de betalingsservice om een rekening aan te vragen.</span><span class="sxs-lookup"><span data-stu-id="d9d09-125">Enabling payment service extensions is free in [!INCLUDE[d365fin](includes/d365fin_md.md)], however, you will need to contact the payment service to get an account.</span></span> <span data-ttu-id="d9d09-126">Zie [Klantbetalingen via betalingsservices inschakelen](sales-how-enable-payment-service-extensions.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d9d09-126">For more information, see [Enable Customer Payment Through Payment Services](sales-how-enable-payment-service-extensions.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d9d09-127">Zie ook</span><span class="sxs-lookup"><span data-stu-id="d9d09-127">See Also</span></span>
<span data-ttu-id="d9d09-128">[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="d9d09-128">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions](ui-extensions.md)</span></span>  
[<span data-ttu-id="d9d09-129">Verkopen instellen</span><span class="sxs-lookup"><span data-stu-id="d9d09-129">Setting Up Sales</span></span>](sales-setup-sales.md)  
<span data-ttu-id="d9d09-130">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="d9d09-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
