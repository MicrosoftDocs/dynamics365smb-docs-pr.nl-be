---
title: Betalingsreconciliatie met de Envestnet Yodlee Bank Feeds-uitbreiding | Microsoft Docs
description: Beschrijft de extensie Envestnet Yodlee Bank Feeds, die bankrekeningen koppelt, zodat u snel betalingen kunt reconciliëren.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: ca384d58046bd0c798038878a3ed93f5a00eeec5
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3189855"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="5c08e-103">De extensie Envestnet Yodlee Bank Feeds</span><span class="sxs-lookup"><span data-stu-id="5c08e-103">The Envestnet Yodlee Bank Feeds Extension</span></span>
<span data-ttu-id="5c08e-104">Om betalingen die naar aan uw bankrekeningen zijn overgemaakt snel te reconciliëren, biedt de service Envestnet Yodlee Bank Feeds u de mogelijkheid om uw systeembankrekening aan uw online bankrekening te koppelen.</span><span class="sxs-lookup"><span data-stu-id="5c08e-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="5c08e-105">Dit betekent dat het laatste bankafschrift automatisch of handmatig in uw reconciliatiedagboek wordt gevoerd, ervoor zorgend dat u altijd de laatste betalingen verwerkt met minimaal risico of minimale fouten.</span><span class="sxs-lookup"><span data-stu-id="5c08e-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

<span data-ttu-id="5c08e-106">De Envestnet Yodlee Bank Feeds-service wordt alleen ondersteund in de VS en Canada.</span><span class="sxs-lookup"><span data-stu-id="5c08e-106">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>

> [!NOTE]
> <span data-ttu-id="5c08e-107">De Envestnet Yodlee Bank Feeds-service wordt alleen ondersteund in de online versie van Business Central.</span><span class="sxs-lookup"><span data-stu-id="5c08e-107">The Envestnet Yodlee Bank Feeds service is only supported in the online version of Business Central.</span></span> <span data-ttu-id="5c08e-108">Als u deze functionaliteit on-premises wilt gebruiken, moet u een cobrand-account verkrijgen bij Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="5c08e-108">To use this functionality on-premises, you must obtain a cobrand account from Envestnet Yodlee.</span></span><br /><br />
> <span data-ttu-id="5c08e-109">De Envestnet Yodlee Bank Feeds-service wordt alleen ondersteund in de VS en Canada.</span><span class="sxs-lookup"><span data-stu-id="5c08e-109">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>
> <span data-ttu-id="5c08e-110">Alleen banken die in deze landen zijn gevestigd, worden ondersteund, ook al kunnen banken uit andere landen ook worden vermeld in het bankselectievenster van Envestnet Yodlee Bank Feeds in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5c08e-110">Only banks residing in these countries are supported, even though banks from other countries may appear in the Envestnet Yodlee Bank Feeds bank selection window in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5c08e-111">Vanwege de nieuwe Payment Services Directive in Europa (PSD2) kunt u na 14 september 2019 niet langer automatisch bankafschriften van banken in het Verenigd Koninkrijk importeren in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5c08e-111">Due to the new Payment Services Directive in Europe (PSD2), after September 14, 2019, you will no longer be able to automatically import bank statements from banks in the United Kingdom into [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="5c08e-112">We onderzoeken de mogelijkheid om deze functie in de toekomst opnieuw aan te bieden.</span><span class="sxs-lookup"><span data-stu-id="5c08e-112">We are looking into the possibility of offering this feature again in the future.</span></span>

<span data-ttu-id="5c08e-113">De service Envestnet Yodlee Bank Feeds biedt de volgende voordelen:</span><span class="sxs-lookup"><span data-stu-id="5c08e-113">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="5c08e-114">Handmatige invoer is niet meer nodig.</span><span class="sxs-lookup"><span data-stu-id="5c08e-114">Removes the need for manual entry.</span></span>
* <span data-ttu-id="5c08e-115">Verbetering van de efficiëntie en nauwkeurigheid bij het uitvoeren van betalingreconciliatie.</span><span class="sxs-lookup"><span data-stu-id="5c08e-115">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="5c08e-116">Ondersteuning van een groot aantal banken.</span><span class="sxs-lookup"><span data-stu-id="5c08e-116">Supports a large number of banks.</span></span>
* <span data-ttu-id="5c08e-117">Mogelijkheid voor actuele informatie over banktransacties binnen [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="5c08e-117">Allows up-to-date information about bank transactions from within [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>
* <span data-ttu-id="5c08e-118">Ondersteuning van handmatige en automatische bankfeeds.</span><span class="sxs-lookup"><span data-stu-id="5c08e-118">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="5c08e-119">Mogelijkheid van uitbesteding van betalingsreconciliatie aan een accountant door toegang tot bankafschriften te bieden.</span><span class="sxs-lookup"><span data-stu-id="5c08e-119">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

<span data-ttu-id="5c08e-120">Zie voor meer informatie [De Envestnet Yodlee Bank Feeds-service instellen](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="5c08e-120">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5c08e-121">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5c08e-121">See Also</span></span>
<span data-ttu-id="5c08e-122">[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="5c08e-122">[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="5c08e-123">Betalingen automatisch vereffenen en bankrekeningen reconciliëren</span><span class="sxs-lookup"><span data-stu-id="5c08e-123">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="5c08e-124">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5c08e-124">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
