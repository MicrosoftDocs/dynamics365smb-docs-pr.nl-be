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
ms.openlocfilehash: f6afaa9ade29c955033914b608806c3fb0f5a310
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3912233"
---
# <a name="send-remittance-advice"></a><span data-ttu-id="a3e0f-103">Afdrachtsadvies verzenden</span><span class="sxs-lookup"><span data-stu-id="a3e0f-103">Send Remittance Advice</span></span>

<span data-ttu-id="a3e0f-104">Als afdrachtsadvies wordt gebruikt om leveranciers te informeren over gedane betalingen, kunt u nu afdrachtsadviezen in bulk verzenden vanuit het betalingsdagboek en deze opnieuw verzenden nadat betalingen vanuit leveranciersposten zijn gedaan, met behulp van documentverzendprofielen.</span><span class="sxs-lookup"><span data-stu-id="a3e0f-104">Where remittance advice is used to notify vendors of payments being made, you can now email remittance advice in bulk from the payment journal as well as resend after payments are made from vendor ledger entries by using document sending profiles.</span></span>

> [!NOTE]
> <span data-ttu-id="a3e0f-105">Deze functionaliteit wordt alleen ondersteund in Business Central online en on-premises in de volgende landen/regio's: Verenigd Koninkrijk, Verenigde Staten, Canada, Australië, Nieuw Zeeland en Zuid-Afrika.</span><span class="sxs-lookup"><span data-stu-id="a3e0f-105">This functionality is only supported in Business Central online and on-premises in following countries: United Kingdom, United States, Canada, Australia, New Zealand, and South Africa.</span></span>  

<span data-ttu-id="a3e0f-106">U kunt afdrachtsadvies op twee verschillende manieren verzenden:</span><span class="sxs-lookup"><span data-stu-id="a3e0f-106">You can send remittance advice in two different ways:</span></span>

* <span data-ttu-id="a3e0f-107">Kies in het **Betalingsdagboek** **Gerelateerd** , **Betalingen** , **Afdrachtsadvies verzenden** om afdrachtsadvies te verzenden voor een of meer betalingsdagboekregels</span><span class="sxs-lookup"><span data-stu-id="a3e0f-107">In the **Payment Journal** page, choose **Related** , **Payments** , **Send Remittance Advice** to email remittance advice for one or multiple payment journal lines</span></span>
* <span data-ttu-id="a3e0f-108">Kies op de pagina **Leveranciersposten** op **Acties** , **Functies** , **Afdrachtsadvies verzenden** om afdrachtsadvies te e-mailen na boeking van leveranciersbetalingen voor een of meer leveranciersposten</span><span class="sxs-lookup"><span data-stu-id="a3e0f-108">In the **Vendor Ledger Entries** page, choose **Actions** , **Functions** , **Send Remittance Advice** to email remittance advice after posting of vendor payments, for one or multiple vendor ledger entries</span></span>

## <a name="see-also"></a><span data-ttu-id="a3e0f-109">Zie ook</span><span class="sxs-lookup"><span data-stu-id="a3e0f-109">See Also</span></span>

[<span data-ttu-id="a3e0f-110">Leveranciersbetalingen voorstellen</span><span class="sxs-lookup"><span data-stu-id="a3e0f-110">Suggest Vendor Payments</span></span>](payables-how-suggest-vendor-payments.md)  
<span data-ttu-id="a3e0f-111">[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="a3e0f-111">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)</span></span>  
<span data-ttu-id="a3e0f-112">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="a3e0f-112">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  
[<span data-ttu-id="a3e0f-113">Documenten per e-mail verzenden</span><span class="sxs-lookup"><span data-stu-id="a3e0f-113">Send Documents by Email</span></span>](ui-how-send-documents-email.md)  
