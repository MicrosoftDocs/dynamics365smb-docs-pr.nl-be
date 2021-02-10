---
title: Extensie Afdrachtsadvies verzenden | Microsoft Docs
description: Beschrijft de extensie Afdrachtsadvies verzenden, waarmee afdrachtsadviezen kunnen worden ge-e-maild en opnieuw worden verzonden vanuit de betalingsdagboek- en leveranciersposten.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, remittance, advice
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 3ae8d131b714b0d7ffb60727d1a991cd6e4ab692
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4757079"
---
# <a name="send-remittance-advice"></a><span data-ttu-id="4b113-103">Afdrachtsadvies verzenden</span><span class="sxs-lookup"><span data-stu-id="4b113-103">Send Remittance Advice</span></span>

<span data-ttu-id="4b113-104">Als afdrachtsadvies wordt gebruikt om leveranciers te informeren over gedane betalingen, kunt u nu afdrachtsadviezen in bulk verzenden vanuit het betalingsdagboek en deze opnieuw verzenden nadat betalingen vanuit leveranciersposten zijn gedaan, met behulp van documentverzendprofielen.</span><span class="sxs-lookup"><span data-stu-id="4b113-104">Where remittance advice is used to notify vendors of payments being made, you can now email remittance advice in bulk from the payment journal as well as resend after payments are made from vendor ledger entries by using document sending profiles.</span></span>

> [!NOTE]
> <span data-ttu-id="4b113-105">Deze functionaliteit wordt alleen ondersteund in Business Central online en on-premises in de volgende landen/regio's: Verenigd Koninkrijk, Verenigde Staten, Canada, Australië, Nieuw Zeeland en Zuid-Afrika.</span><span class="sxs-lookup"><span data-stu-id="4b113-105">This functionality is only supported in Business Central online and on-premises in following countries: United Kingdom, United States, Canada, Australia, New Zealand, and South Africa.</span></span>  

<span data-ttu-id="4b113-106">U kunt afdrachtsadvies op twee verschillende manieren verzenden:</span><span class="sxs-lookup"><span data-stu-id="4b113-106">You can send remittance advice in two different ways:</span></span>

* <span data-ttu-id="4b113-107">Kies in het **Betalingsdagboek** **Gerelateerd**, **Betalingen**, **Afdrachtsadvies verzenden** om afdrachtsadvies te verzenden voor een of meer betalingsdagboekregels</span><span class="sxs-lookup"><span data-stu-id="4b113-107">In the **Payment Journal** page, choose **Related**, **Payments**, **Send Remittance Advice** to email remittance advice for one or multiple payment journal lines</span></span>
* <span data-ttu-id="4b113-108">Kies op de pagina **Leveranciersposten** op **Acties**, **Functies**, **Afdrachtsadvies verzenden** om afdrachtsadvies te e-mailen na boeking van leveranciersbetalingen voor een of meer leveranciersposten</span><span class="sxs-lookup"><span data-stu-id="4b113-108">In the **Vendor Ledger Entries** page, choose **Actions**, **Functions**, **Send Remittance Advice** to email remittance advice after posting of vendor payments, for one or multiple vendor ledger entries</span></span>

## <a name="see-also"></a><span data-ttu-id="4b113-109">Zie ook</span><span class="sxs-lookup"><span data-stu-id="4b113-109">See Also</span></span>

[<span data-ttu-id="4b113-110">Leveranciersbetalingen voorstellen</span><span class="sxs-lookup"><span data-stu-id="4b113-110">Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md)  
<span data-ttu-id="4b113-111">[[!INCLUDE[prod_short](includes/prod_short.md)] aanpassen met behulp van extensies](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="4b113-111">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)</span></span>  
<span data-ttu-id="4b113-112">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="4b113-112">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="4b113-113">Documenten per e-mail verzenden</span><span class="sxs-lookup"><span data-stu-id="4b113-113">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
