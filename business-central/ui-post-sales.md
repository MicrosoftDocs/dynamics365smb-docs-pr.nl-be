---
title: Begrijpen hoe u verkoopdocumenten boekt | Microsoft Docs
description: Leren over de verschillende boekingsfuncties om verkoopdocumenten te boeken.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2018
ms.author: solsen
ms.openlocfilehash: 7ada688f7946d7f857dc6d4a6518b8bcb4e5c707
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "816357"
---
# <a name="posting-sales"></a><span data-ttu-id="2e43e-103">Verkopen boeken</span><span class="sxs-lookup"><span data-stu-id="2e43e-103">Posting Sales</span></span>
<span data-ttu-id="2e43e-104">In de **Boekingsgroep** op een verkoopdocument kunt u kiezen uit de volgende boekingsfuncties:</span><span class="sxs-lookup"><span data-stu-id="2e43e-104">In the **Posting group** on a sales document, you can choose between the following posting functions:</span></span>

* <span data-ttu-id="2e43e-105">**Boeken**</span><span class="sxs-lookup"><span data-stu-id="2e43e-105">**Post**</span></span>
* <span data-ttu-id="2e43e-106">**Testrapport**</span><span class="sxs-lookup"><span data-stu-id="2e43e-106">**Test Report**</span></span>
* <span data-ttu-id="2e43e-107">**Boeken en verzenden**</span><span class="sxs-lookup"><span data-stu-id="2e43e-107">**Post and Send**</span></span>
* <span data-ttu-id="2e43e-108">**Boeken en afdrukken**</span><span class="sxs-lookup"><span data-stu-id="2e43e-108">**Post and Print**</span></span>
* <span data-ttu-id="2e43e-109">**Boeken en e-mailen**</span><span class="sxs-lookup"><span data-stu-id="2e43e-109">**Post and Email**</span></span>
* <span data-ttu-id="2e43e-110">**Batchboeken**</span><span class="sxs-lookup"><span data-stu-id="2e43e-110">**Post Batch**</span></span>
* <span data-ttu-id="2e43e-111">**Voorbeeld van boeking weergeven**</span><span class="sxs-lookup"><span data-stu-id="2e43e-111">**Preview Posting**</span></span>

<span data-ttu-id="2e43e-112">Wanneer u alle regels hebt ingevuld en alle informatie hebt ingevoerd op de verkooporder, kunt u de order boeken.</span><span class="sxs-lookup"><span data-stu-id="2e43e-112">When you have completed all the lines and entered all the information on the sales order, you can post it.</span></span> <span data-ttu-id="2e43e-113">Hiermee worden een verzending en een factuur gemaakt.</span><span class="sxs-lookup"><span data-stu-id="2e43e-113">This creates a shipment and an invoice.</span></span>

<span data-ttu-id="2e43e-114">Wanneer een verkooporder wordt geboekt, worden de rekening van de klant, het grootboek en de artikelposten bijgewerkt.</span><span class="sxs-lookup"><span data-stu-id="2e43e-114">When a sales order is posted, the customer's account, the general ledger, and the item ledger entries are updated.</span></span>

<span data-ttu-id="2e43e-115">Voor elke verkooporder wordt een verkooppost gemaakt in de tabel **Grootboekpost**.</span><span class="sxs-lookup"><span data-stu-id="2e43e-115">For each sales order, a sales entry is created in the **G/L Entry** table.</span></span> <span data-ttu-id="2e43e-116">Ook wordt er een post in de klantrekening in de tabel **Klantpost** en een grootboekpost wordt in de desbetreffende rekening voor tegoeden gemaakt.</span><span class="sxs-lookup"><span data-stu-id="2e43e-116">An entry is also created in the customer's account in the **Cust. Ledger Entry** table and a general ledger entry is created in the relevant receivables account.</span></span> <span data-ttu-id="2e43e-117">Bovendien kan het boeken van de order resulteren in een btw-post en een grootboekpost voor de totale korting.</span><span class="sxs-lookup"><span data-stu-id="2e43e-117">In addition, posting the order may result in a VAT entry and a general ledger entry for the discount amount.</span></span> <span data-ttu-id="2e43e-118">Of er een post voor de korting wordt geboekt hangt af van de inhoud van het veld **Korting boeken** op de pagina **Verkoopinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="2e43e-118">Whether an entry for the discount is posted depends on the contents of the **Discount Posting** field on the **Sales & Receivables Setup** page.</span></span>

<span data-ttu-id="2e43e-119">Voor elke verkooporderregel wordt een artikelpost gemaakt in de tabel **Artikelpost** (als de verkoopregels artikelnummers bevatten) of wordt een grootboekpost gemaakt in de tabel **Grootboekpost** (als de verkoopregels een grootboekrekening bevatten).</span><span class="sxs-lookup"><span data-stu-id="2e43e-119">For each sales order line, an item ledger entry will be created in the **Item Ledger Entry** table (if the sales lines contain item numbers) or a general ledger entry will be created in the **G/L Entry** table (if the sales lines contain a general ledger account).</span></span> <span data-ttu-id="2e43e-120">Daarnaast worden verkooporders altijd geregistreerd in de tabellen **Verkoopverzendkop** en **Verkoopfactuurkop**.</span><span class="sxs-lookup"><span data-stu-id="2e43e-120">In addition to this, sales orders are always recorded in the **Sales Shipment Header** and **Sales Invoice Header** tables.</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="2e43e-121">Wanneer u een order boekt, kunt u zowel een verzending als een factuur maken.</span><span class="sxs-lookup"><span data-stu-id="2e43e-121">When you post an order, you can create both a shipment and an invoice.</span></span> <span data-ttu-id="2e43e-122">Deze kunnen tegelijk of afzonderlijk worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="2e43e-122">These can be done at the same time or independently.</span></span> <span data-ttu-id="2e43e-123">U kunt ook een gedeeltelijke verzending en een gedeeltelijke factuur maken door de velden **Te verzenden aantal** en **Te factureren aantal** op de afzonderlijke verkooporderregels in te vullen voordat u de boeking uitvoert.</span><span class="sxs-lookup"><span data-stu-id="2e43e-123">You can also create a partial shipment and a partial invoice by completing the **Qty. to Ship** and **Qty. to Invoice** fields on the individual sales order lines before you post.</span></span> <span data-ttu-id="2e43e-124">U kunt geen factuur maken voor iets wat niet is verzonden.</span><span class="sxs-lookup"><span data-stu-id="2e43e-124">Note that you cannot create an invoice for something that is not shipped.</span></span> <span data-ttu-id="2e43e-125">U kunt dus pas factureren nadat u een verzending hebt geregistreerd, of u moet ervoor kiezen om tegelijkertijd te verzenden en factureren.</span><span class="sxs-lookup"><span data-stu-id="2e43e-125">That is, before you can invoice, you must have recorded a shipment, or you must choose to ship and invoice at the same time.</span></span>

<span data-ttu-id="2e43e-126">Na de boeking worden de geboekte verkoopregels verwijderd uit de order.</span><span class="sxs-lookup"><span data-stu-id="2e43e-126">When the posting is completed, the posted sales lines are removed from the order.</span></span> <span data-ttu-id="2e43e-127">Er verschijnt een bericht als de boeking is voltooid.</span><span class="sxs-lookup"><span data-stu-id="2e43e-127">A message tells you when the posting is completed.</span></span> <span data-ttu-id="2e43e-128">Hierna kunt u de geboekte posten bekijken op de verschillende pagina's die geboekte posten bevatten, zoals de pagina's **Klantposten**, **Grootboekposten**, **Artikelposten**, **Geboekte verkoopverzendingen** en **Geboekte verkoopfacturen**.</span><span class="sxs-lookup"><span data-stu-id="2e43e-128">After this, you will be able to see the posted entries in the various pages that contain posted entries, such as the **Cust. Ledger Entries**, **G/L Entries**, **Item Ledger Entries**, **Posted Sales Shipments**, and **Posted Sales Invoices** pages.</span></span>

## <a name="see-also"></a><span data-ttu-id="2e43e-129">Zie ook</span><span class="sxs-lookup"><span data-stu-id="2e43e-129">See Also</span></span>
[<span data-ttu-id="2e43e-130">Verkoop</span><span class="sxs-lookup"><span data-stu-id="2e43e-130">Sales</span></span>](sales-manage-sales.md)  
[<span data-ttu-id="2e43e-131">Documenten per e-mail verzenden</span><span class="sxs-lookup"><span data-stu-id="2e43e-131">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
<span data-ttu-id="2e43e-132">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="2e43e-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

