---
title: Betalingsreconciliatie met de extensie Envestnet Yodlee Bank Feeds
description: Beschrijft de extensie Envestnet Yodlee Bank Feeds, die bankrekeningen koppelt, zodat u snel betalingen kunt reconciliëren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, stream, bank account link
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 946958669f4554869e171286927bf498fe62a7ed
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5394036"
---
# <a name="the-envestnet-yodlee-bank-feeds-extension"></a><span data-ttu-id="af84a-103">De extensie Envestnet Yodlee Bank Feeds</span><span class="sxs-lookup"><span data-stu-id="af84a-103">The Envestnet Yodlee Bank Feeds Extension</span></span>

<span data-ttu-id="af84a-104">Om betalingen die naar aan uw bankrekeningen zijn overgemaakt snel te reconciliëren, biedt de service Envestnet Yodlee Bank Feeds u de mogelijkheid om uw systeembankrekening aan uw online bankrekening te koppelen.</span><span class="sxs-lookup"><span data-stu-id="af84a-104">To quickly reconcile payments made to your bank accounts, the Envestnet Yodlee Bank Feeds service allows you to link your system bank account to your online bank account.</span></span> <span data-ttu-id="af84a-105">Dit betekent dat het laatste bankafschrift automatisch of handmatig in uw reconciliatiedagboek wordt gevoerd, ervoor zorgend dat u altijd de laatste betalingen verwerkt met minimaal risico of minimale fouten.</span><span class="sxs-lookup"><span data-stu-id="af84a-105">This means that the latest bank statement is automatically or manually fed into your reconciliation journal, ensuring that you are always processing the latest payments with minimal risk of errors.</span></span>

<span data-ttu-id="af84a-106">De Envestnet Yodlee Bank Feeds-service wordt alleen ondersteund in de VS en Canada.</span><span class="sxs-lookup"><span data-stu-id="af84a-106">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>

> [!NOTE]
> <span data-ttu-id="af84a-107">De Envestnet Yodlee Bank Feeds-service wordt alleen ondersteund in de online versie van Business Central.</span><span class="sxs-lookup"><span data-stu-id="af84a-107">The Envestnet Yodlee Bank Feeds service is only supported in the online version of Business Central.</span></span> <span data-ttu-id="af84a-108">Als u deze functionaliteit on-premises wilt gebruiken, moet u een cobrand-account verkrijgen bij Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="af84a-108">To use this functionality on-premises, you must obtain a cobrand account from Envestnet Yodlee.</span></span><br /><br />
> <span data-ttu-id="af84a-109">De Envestnet Yodlee Bank Feeds-service wordt alleen ondersteund in de VS en Canada.</span><span class="sxs-lookup"><span data-stu-id="af84a-109">The Envestnet Yodlee Bank Feeds service is only supported in the United States and Canada.</span></span>
> <span data-ttu-id="af84a-110">Alleen banken die in deze landen/regio's zijn gevestigd, worden ondersteund, ook al kunnen banken uit andere landen/regio's ook worden vermeld in het bankselectievenster van Envestnet Yodlee Bank Feeds in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="af84a-110">Only banks residing in these countries are supported, even though banks from other countries may appear in the Envestnet Yodlee Bank Feeds bank selection window in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>

> [!IMPORTANT]
> <span data-ttu-id="af84a-111">Vanwege de nieuwe Payment Services Directive in Europa (PSD2) kunt u na 14 september 2019 niet langer automatisch bankafschriften van banken in het Verenigd Koninkrijk importeren in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="af84a-111">Due to the new Payment Services Directive in Europe (PSD2), after September 14, 2019, you will no longer be able to automatically import bank statements from banks in the United Kingdom into [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="af84a-112">We onderzoeken de mogelijkheid om deze functie in de toekomst opnieuw aan te bieden.</span><span class="sxs-lookup"><span data-stu-id="af84a-112">We are looking into the possibility of offering this feature again in the future.</span></span>

<span data-ttu-id="af84a-113">De service Envestnet Yodlee Bank Feeds biedt de volgende voordelen:</span><span class="sxs-lookup"><span data-stu-id="af84a-113">The Envestnet Yodlee Bank Feeds service provides the following benefits:</span></span>

* <span data-ttu-id="af84a-114">Handmatige invoer is niet meer nodig.</span><span class="sxs-lookup"><span data-stu-id="af84a-114">Removes the need for manual entry.</span></span>
* <span data-ttu-id="af84a-115">Verbetering van de efficiëntie en nauwkeurigheid bij het uitvoeren van betalingreconciliatie.</span><span class="sxs-lookup"><span data-stu-id="af84a-115">Improves efficiency and accuracy when doing payment reconciliation.</span></span>
* <span data-ttu-id="af84a-116">Ondersteuning van een groot aantal banken.</span><span class="sxs-lookup"><span data-stu-id="af84a-116">Supports a large number of banks.</span></span>
* <span data-ttu-id="af84a-117">Mogelijkheid voor actuele informatie over banktransacties binnen [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="af84a-117">Allows up-to-date information about bank transactions from within [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>
* <span data-ttu-id="af84a-118">Ondersteuning van handmatige en automatische bankfeeds.</span><span class="sxs-lookup"><span data-stu-id="af84a-118">Supports manual as well as automatic bank feeds.</span></span>
* <span data-ttu-id="af84a-119">Mogelijkheid van uitbesteding van betalingsreconciliatie aan een accountant door toegang tot bankafschriften te bieden.</span><span class="sxs-lookup"><span data-stu-id="af84a-119">Enables outsourcing of payment reconciliation to an accountant by providing access to bank statements.</span></span>

## <a name="available-bank-feeds"></a><span data-ttu-id="af84a-120">Beschikbare bankfeeds</span><span class="sxs-lookup"><span data-stu-id="af84a-120">Available Bank Feeds</span></span>
<span data-ttu-id="af84a-121">U kunt controleren of een bank wordt ondersteund door de Envestnet Yodlee Bank Feeds-service in te stellen en er verbinding mee te maken.</span><span class="sxs-lookup"><span data-stu-id="af84a-121">You can check whether a bank is supported by setting up and connecting to the Envestnet Yodlee Bank Feeds service.</span></span> <span data-ttu-id="af84a-122">De bank zal op de lijst verschijnen als deze wordt ondersteund door Envestnet Yodlee.</span><span class="sxs-lookup"><span data-stu-id="af84a-122">The bank will appear on the list if it is supported by Envestnet Yodlee.</span></span>

<span data-ttu-id="af84a-123">Zie voor meer informatie [De Envestnet Yodlee Bank Feeds-service instellen](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="af84a-123">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="af84a-124">Zie ook</span><span class="sxs-lookup"><span data-stu-id="af84a-124">See Also</span></span>
<span data-ttu-id="af84a-125">[[!INCLUDE[prod_short](includes/prod_short.md)] aanpassen met behulp van extensies ](ui-extensions.md)  </span><span class="sxs-lookup"><span data-stu-id="af84a-125">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)  </span></span>  
[<span data-ttu-id="af84a-126">Betalingen automatisch vereffenen en bankrekeningen reconciliëren</span><span class="sxs-lookup"><span data-stu-id="af84a-126">Applying Payments Automatically and Reconciling Bank Accounts</span></span>](receivables-apply-payments-auto-reconcile-bank-accounts.md)  
<span data-ttu-id="af84a-127">[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="af84a-127">[Working with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)</span></span>


[!INCLUDE[footer-include](includes/footer-banner.md)]