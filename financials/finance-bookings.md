---
title: Uw boekingen factureren in Finance and Operations, Business edition | Microsoft Docs
description: Leren hoe u massaal factureert vanuit Microsoft Bookings in Finance and Operations, Business edition.
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: invoicing, bookings
ms.date: 06/14/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: d387bbbf59550a6ca11dff534b76683a07808ca4
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="bulk-invoicing-for-microsoft-bookings-in-included365finincludesd365finmdmd"></a><span data-ttu-id="5af8e-103">Massale facturering voor Microsoft Bookings in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span><span class="sxs-lookup"><span data-stu-id="5af8e-103">Bulk Invoicing for Microsoft Bookings in [!INCLUDE[d365fin](includes/d365fin_md.md)]</span></span>
<span data-ttu-id="5af8e-104">Als uw bedrijf de app Bookings gebruikt in Office 365, kunt u massaal factureren voor afspraken.</span><span class="sxs-lookup"><span data-stu-id="5af8e-104">If your company uses the Bookings app in Office 365, you can do bulk invoicing for appointments.</span></span> <span data-ttu-id="5af8e-105">De pagina **Niet-gefactureerde Bookings** in [!INCLUDE[d365fin](includes/d365fin_md.md)] biedt een overzicht van de voltooide boekingen van het bedrijf.</span><span class="sxs-lookup"><span data-stu-id="5af8e-105">The **Uninvoiced Bookings** page in [!INCLUDE[d365fin](includes/d365fin_md.md)] provides a list of the company's completed bookings.</span></span> <span data-ttu-id="5af8e-106">Op deze pagina kunt u snel afspraken selecteren die u wilt factureren en conceptfacturen maken voor de geleverde services.</span><span class="sxs-lookup"><span data-stu-id="5af8e-106">In this page you can quickly select the appointments that you want to invoice and create draft invoices for the services provided.</span></span>  

## <a name="connect-to-bookings"></a><span data-ttu-id="5af8e-107">Verbinden met Bookings</span><span class="sxs-lookup"><span data-stu-id="5af8e-107">Connect to Bookings</span></span>
<span data-ttu-id="5af8e-108">Als u [!INCLUDE[d365fin](includes/d365fin_md.md)] wilt verbinden met Bookings, moet u uw Bookings-bedrijf opgeven, opgeven wat u wilt synchroniseren met Bookings, hoe vaak moet worden gesynchroniseerd en welke sjablonen moeten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="5af8e-108">To connect your [!INCLUDE[d365fin](includes/d365fin_md.md)] with Bookings, you must specify your Bookings company, what to synchronize with Bookings, how often to synchronize, and which templates to use.</span></span> <span data-ttu-id="5af8e-109">U stelt deze informatie in op de pagina **Instelling van Booking-synchronisatie**, die u kunt starten vanaf de pagina **Instelling van Exchange-synchronisatie**, die u kunt vinden met behulp van [Zoeken](ui-search.md).</span><span class="sxs-lookup"><span data-stu-id="5af8e-109">You set up this information in the **Booking Sync. Setup** page, which you can launch from the **Exchange Sync. Setup** page, which you can find through [Search](ui-search.md).</span></span>  

<span data-ttu-id="5af8e-110">Als u bijvoorbeeld klanten wilt synchroniseren tussen Bookings en [!INCLUDE[d365fin](includes/d365fin_md.md)], moet u de standaardsjabloon opgeven die moet worden gebruikt om nieuwe klanten toe te voegen aan [!INCLUDE[d365fin](includes/d365fin_md.md)], op basis van de klanten in uw Bookings-bedrijf.</span><span class="sxs-lookup"><span data-stu-id="5af8e-110">For example, if you want to synchronize customers between Bookings and [!INCLUDE[d365fin](includes/d365fin_md.md)], you must specify the default template to use to add new customers in [!INCLUDE[d365fin](includes/d365fin_md.md)] based on the customers in your Bookings company.</span></span>  

## <a name="invoice-appointments"></a><span data-ttu-id="5af8e-111">Afspraken factureren</span><span class="sxs-lookup"><span data-stu-id="5af8e-111">Invoice Appointments</span></span>
<span data-ttu-id="5af8e-112">Wanneer het tijd is om facturen te verzenden voor de voltooide boekingen, gaat u naar de pagina **Niet-gefactureerde Bookings**.</span><span class="sxs-lookup"><span data-stu-id="5af8e-112">When it is time to send invoices for the completed bookings, you go to the **Uninvoiced Bookings** page.</span></span> <span data-ttu-id="5af8e-113">Afhankelijk van hoe vaak de gegevens worden gesynchroniseerd, is de lijst lang of kort.</span><span class="sxs-lookup"><span data-stu-id="5af8e-113">Depending on how often the information is synchronized, the list is long or short.</span></span> <span data-ttu-id="5af8e-114">U kunt facturen maken voor alle boekingen in de lijst of voor één tegelijkertijd.</span><span class="sxs-lookup"><span data-stu-id="5af8e-114">You can create invoices for all bookings in the list or one booking at a time.</span></span> <span data-ttu-id="5af8e-115">U kunt een of meer posten in het overzicht selecteren en alleen die factureren.</span><span class="sxs-lookup"><span data-stu-id="5af8e-115">You can select one or more entries in the list and invoice those only.</span></span>  

<span data-ttu-id="5af8e-116">De ondersteuning voor het factureren van afspraken vanuit Bookings is eenvoudiger dan de volledigere werkstroom voor het werken met verkoopoffertes, verkooporders en verkoopfacturen.</span><span class="sxs-lookup"><span data-stu-id="5af8e-116">The support for invoicing appointments from Bookings is simpler than the fuller workflow of working with sales quotes, sales orders, and sales invoices.</span></span> <span data-ttu-id="5af8e-117">Zie [Verkopen factureren](sales-how-invoice-sales.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="5af8e-117">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span> <span data-ttu-id="5af8e-118">U kunt uw services verkopen met [!INCLUDE[d365fin](includes/d365fin_md.md)] of kiezen om Bookings te gebruiken, afhankelijk van uw zakelijke behoeften.</span><span class="sxs-lookup"><span data-stu-id="5af8e-118">You can choose to sell your services using [!INCLUDE[d365fin](includes/d365fin_md.md)] or choose to use Bookings, depending on your business needs.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5af8e-119">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5af8e-119">See Also</span></span>
[<span data-ttu-id="5af8e-120">Financiën</span><span class="sxs-lookup"><span data-stu-id="5af8e-120">Finance</span></span>](finance.md)  
[<span data-ttu-id="5af8e-121">Verkopen factureren</span><span class="sxs-lookup"><span data-stu-id="5af8e-121">Invoice Sales</span></span>](sales-how-invoice-sales.md)  
[<span data-ttu-id="5af8e-122">Verkopen instellen</span><span class="sxs-lookup"><span data-stu-id="5af8e-122">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="5af8e-123">Microsoft Bookings</span><span class="sxs-lookup"><span data-stu-id="5af8e-123">Microsoft Bookings</span></span>](https://products.office.com/en-us/business/scheduling-and-booking-app)  

