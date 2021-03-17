---
title: Serviceoffertes maken | Microsoft Docs
description: Op de pagina **Serviceofferte** kunt u documenten maken waarin u op aanvraag van de klant voor serviceartikelen gegevens invoert over een service, als bijvoorbeeld herstel en onderhoud. U kunt een serviceofferte gebruiken als voorlopig ontwerp voor een serviceorder en de offerte vervolgens omzetten in een serviceorder.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 92c93b2e0b876920f1c259d31b4d839a5b2ecbc0
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5388811"
---
# <a name="create-service-quotes"></a><span data-ttu-id="33e78-104">Serviceoffertes maken:</span><span class="sxs-lookup"><span data-stu-id="33e78-104">Create Service Quotes</span></span>
<span data-ttu-id="33e78-105">U kunt serviceoffertes als de basis voor serviceorders zien.</span><span class="sxs-lookup"><span data-stu-id="33e78-105">You can think of service quotes as the basis for service orders.</span></span> <span data-ttu-id="33e78-106">Ze zijn zelfs vrijwel identiek.</span><span class="sxs-lookup"><span data-stu-id="33e78-106">In fact, they are almost identical.</span></span> <span data-ttu-id="33e78-107">Ze bevatten beide informatie, bijvoorbeeld over wie de klant is, het soort order, het artikel dat service vereist, facturerings- en verzendingsgegevens, en informatie over het werkelijke servicewerk.</span><span class="sxs-lookup"><span data-stu-id="33e78-107">They both contain information such as who the customer is, the type of order, the item that needs service, billing and shipping information, and information about the actual service work.</span></span>
 
<span data-ttu-id="33e78-108">U kunt een serviceofferte gebruiken als voorlopig ontwerp voor een serviceorder en de offerte vervolgens omzetten in een serviceorder.</span><span class="sxs-lookup"><span data-stu-id="33e78-108">You can use a service quote as a preliminary draft for a service order, and then convert the quote to a service order.</span></span>  
  
## <a name="to-create-a-service-quote"></a><span data-ttu-id="33e78-109">Serviceoffertes maken</span><span class="sxs-lookup"><span data-stu-id="33e78-109">To create a service quote</span></span>  
1. <span data-ttu-id="33e78-110">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Serviceoffertes** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="33e78-110">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Service Quotes**, and then choose the related link.</span></span>  
2. <span data-ttu-id="33e78-111">Een nieuwe serviceofferte maken.</span><span class="sxs-lookup"><span data-stu-id="33e78-111">Create a new service quote.</span></span>  
3. <span data-ttu-id="33e78-112">Selecteer in het veld **Nr.**</span><span class="sxs-lookup"><span data-stu-id="33e78-112">In the **No.**</span></span> <span data-ttu-id="33e78-113">een nummer op voor de serviceofferte.</span><span class="sxs-lookup"><span data-stu-id="33e78-113">field, enter a number for the service quote.</span></span> <span data-ttu-id="33e78-114">Als u op de pagina **Servicebeheerinstellingen** nummerreeksen voor serviceoffertes hebt ingesteld, kunt u ook op Enter drukken om het eerstvolgende beschikbare serviceoffertenummer in te voeren.</span><span class="sxs-lookup"><span data-stu-id="33e78-114">Alternatively, if you have set up a number series for service quotes on the **Service Mgt. Setup** page, you can press Enter to select the next available service quote number.</span></span>  
4. <span data-ttu-id="33e78-115">Voer in het veld **Klantnr.**</span><span class="sxs-lookup"><span data-stu-id="33e78-115">In the **Customer No.**</span></span>  <span data-ttu-id="33e78-116">de betreffende klant uit de lijst.</span><span class="sxs-lookup"><span data-stu-id="33e78-116">field, select the relevant customer from the list.</span></span>  

  > [!Note]  
  >  <span data-ttu-id="33e78-117">De klantvelden worden automatisch ingevuld met gegevens uit de **Klantenkaart**.</span><span class="sxs-lookup"><span data-stu-id="33e78-117">The customer fields are filled in automatically with information from the **Customer** card.</span></span> <span data-ttu-id="33e78-118">Als er geen **klantenkaart** bestaat voor de klant en u een klantensjabloon hebt ingesteld, kunt u de klant vanuit de serviceofferte maken.</span><span class="sxs-lookup"><span data-stu-id="33e78-118">If a **Customer** card does not exist for the customer, and you have set up a customer template, you can create the customer from the service quote.</span></span> <span data-ttu-id="33e78-119">Vul de relevante velden in en kies de actie **Klant maken**.</span><span class="sxs-lookup"><span data-stu-id="33e78-119">Fill in the relevant fields, and then choose the **Create Customer** action.</span></span>  
  
5. <span data-ttu-id="33e78-120">Afhankelijk van de instellingen op het sneltabblad **Verplichte velden** op de pagina **CRM - Service-instellingen** moet u wellicht het veld **Serviceordersoort** en het veld **Verkoper** invullen.</span><span class="sxs-lookup"><span data-stu-id="33e78-120">Depending on the settings on the **Mandatory Fields** FastTab on the **Service Mgt. Setup** page, you may need to fill in the **Service Order Type** field and the **Salesperson Code** field.</span></span>  
6. <span data-ttu-id="33e78-121">Vul de serviceartikelregels in.</span><span class="sxs-lookup"><span data-stu-id="33e78-121">Fill in the service item lines.</span></span>  
7. <span data-ttu-id="33e78-122">Registreer de geschatte kosten op de serviceregels.</span><span class="sxs-lookup"><span data-stu-id="33e78-122">Register estimated costs on the service lines.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="33e78-123">Zie ook</span><span class="sxs-lookup"><span data-stu-id="33e78-123">See Also</span></span>  
[<span data-ttu-id="33e78-124">Serviceorders maken</span><span class="sxs-lookup"><span data-stu-id="33e78-124">Create Service Orders</span></span>](service-how-to-create-service-orders.md)  
[<span data-ttu-id="33e78-125">Werken aan servicetaken</span><span class="sxs-lookup"><span data-stu-id="33e78-125">Work on Service tasks</span></span>](service-how-to-work-on-service-tasks.md)  

 

[!INCLUDE[footer-include](includes/footer-banner.md)]