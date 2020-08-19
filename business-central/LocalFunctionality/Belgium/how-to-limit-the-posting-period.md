---
title: De boekingsperiode beperken
description: 'U kunt de periode waarop boeking is toegestaan op drie verschillende niveaus beperken: op bedrijf, op gebruiker en op sjabloon.'
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 19a5d43126fd9071c89d91cd834b15551d6fd0cb
ms.sourcegitcommit: 007b331b6974983ee614db0406f00777da359ecb
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 08/10/2020
ms.locfileid: "3677159"
---
# <a name="limit-the-posting-period"></a><span data-ttu-id="3b77d-103">De boekingsperiode beperken</span><span class="sxs-lookup"><span data-stu-id="3b77d-103">Limit the Posting Period</span></span>
<span data-ttu-id="3b77d-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kunt u de periode waarop boeking is toegestaan op drie verschillende niveaus beperken: **op bedrijf**, **op gebruiker** en **op sjabloon**.</span><span class="sxs-lookup"><span data-stu-id="3b77d-104">In [!INCLUDE[d365fin](../../includes/d365fin_md.md)], you can limit the period by which posting is permitted on three different levels: **by company**, **by user**, and **by template**.</span></span>  

<span data-ttu-id="3b77d-105">Boekingsperioden beperken kan handig zijn als een bedrijf zijn verkoopdagboek aan het einde van elke maand sluit.</span><span class="sxs-lookup"><span data-stu-id="3b77d-105">Limiting posting periods can be useful when a company closes its sales journal at the end of each month.</span></span> <span data-ttu-id="3b77d-106">Dit voorkomt dat verkopers verkoopdocumenten van de vorige maand registreren.</span><span class="sxs-lookup"><span data-stu-id="3b77d-106">This keeps salespeople from registering sales documents from the previous month.</span></span> <span data-ttu-id="3b77d-107">Tegelijkertijd kan het inkoopdagboek open blijven om inkomende inkoopfacturen van de vorige maand te registreren.</span><span class="sxs-lookup"><span data-stu-id="3b77d-107">At the same time, the purchase journal may stay open to register incoming purchase invoices from the previous month.</span></span>  

<span data-ttu-id="3b77d-108">Wanneer u op de pagina **Financieel-dagboeksjablonen** boekt, wordt de inhoud van het veld **Boeken toegest. vanaf** en het veld **Boeken toegest. tot** gecontroleerd op een datuminterval.</span><span class="sxs-lookup"><span data-stu-id="3b77d-108">When you post on the **General Journal Templates** page, the contents of the **Allow Posting From** field and **Allow Posting To** field are checked for a date interval.</span></span> <span data-ttu-id="3b77d-109">Het datuminterval geeft aan wanneer u een dagboeksjabloon kunt boeken.</span><span class="sxs-lookup"><span data-stu-id="3b77d-109">The date interval indicates when you can post to a journal template.</span></span> <span data-ttu-id="3b77d-110">Als het veld leeg is, wordt de pagina **Gebruikersinstellingen** gecontroleerd op een datuminterval voor de huidige gebruiker.</span><span class="sxs-lookup"><span data-stu-id="3b77d-110">If the field is blank, the **User Setup** page is checked for a date interval for the current user.</span></span> <span data-ttu-id="3b77d-111">Als de pagina **Gebruikersinstellingen** geen interval bevat, wordt het veld **Boeken toegest. vanaf** en het veld **Boeken toegest. tot** op de pagina **Boekhoudinstellingen** gecontroleerd op een datuminterval op het bedrijfsniveau.</span><span class="sxs-lookup"><span data-stu-id="3b77d-111">If the **User Setup** page does not contain an interval, the **Allow Posting From** field and the **Allow Posting To** field on the **General Ledger Setup** page is checked for a date interval at the company level.</span></span>  

## <a name="to-limit-the-posting-periods-by-company"></a><span data-ttu-id="3b77d-112">De boekingsperioden per bedrijf beperken</span><span class="sxs-lookup"><span data-stu-id="3b77d-112">To limit the posting periods by company</span></span>  

1.  <span data-ttu-id="3b77d-113">Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Grootboekinstellingen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="3b77d-113">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Ledger Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="3b77d-114">Als u het begin van de periode wilt opgeven, kiest u het veld **Boeken toegest. vanaf** en voert u vervolgens de vroegste datum in waarop boeken naar het bedrijf is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="3b77d-114">To specify the start of the period, choose the **Allow Posting From** field, and then enter the earliest date on which posting to the company is enabled.</span></span>  
3.  <span data-ttu-id="3b77d-115">Als u het einde van de periode wilt opgeven, kiest u het veld **Boeken toegest. tot** en voert u vervolgens de laatste datum in waarop boeken naar het bedrijf is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="3b77d-115">To specify the end of the period, choose the **Allow Posting To** field, and then enter the last date on which posting to the company is enabled.</span></span>  

## <a name="to-limit-the-posting-periods-by-user"></a><span data-ttu-id="3b77d-116">De boekingsperioden per gebruiker beperken</span><span class="sxs-lookup"><span data-stu-id="3b77d-116">To limit the posting periods by user</span></span>  

1.  <span data-ttu-id="3b77d-117">Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikersinstellingen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="3b77d-117">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **User Setup**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="3b77d-118">Als u het begin van de periode wilt opgeven, kiest u het veld **Boeken toegest. vanaf** en voert u vervolgens de vroegste datum in waarop de gebruiker naar het bedrijf kan boeken.</span><span class="sxs-lookup"><span data-stu-id="3b77d-118">To specify the start of the period, choose the **Allow Posting From** field, and then enter the earliest date on which the user can post to the company.</span></span>  
3.  <span data-ttu-id="3b77d-119">Als u het einde van de periode wilt opgeven, kiest u het veld **Boeken toegest. tot** en voert u vervolgens de laatste datum in waarop de gebruiker naar het bedrijf kan boeken.</span><span class="sxs-lookup"><span data-stu-id="3b77d-119">To specify the end of the period, choose the **Allow Posting To** field, and then enter the last date the user will be able to post to the company.</span></span>  

## <a name="to-limit-the-posting-periods-by-template"></a><span data-ttu-id="3b77d-120">De boekingsperioden per sjabloon beperken</span><span class="sxs-lookup"><span data-stu-id="3b77d-120">To limit the posting periods by template</span></span>  

1.  <span data-ttu-id="3b77d-121">Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Diversendagboeksjablonen** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="3b77d-121">Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Journal Templates**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="3b77d-122">Als u het begin van de periode wilt opgeven, kiest u het veld **Boeken toegest. vanaf** en voert u vervolgens de vroegste datum in waarop de gebruiker naar het bedrijf kan boeken.</span><span class="sxs-lookup"><span data-stu-id="3b77d-122">To specify the start of the period, choose the **Allow Posting From** field, and then enter the earliest date on which the user can post to the company.</span></span>  
3.  <span data-ttu-id="3b77d-123">Als u het einde van de periode wilt opgeven, kiest u het veld **Boeken toegest. tot** en voert u vervolgens de laatste datum in waarop de gebruiker naar het bedrijf kan boeken.</span><span class="sxs-lookup"><span data-stu-id="3b77d-123">To specify the end of the period, choose the **Allow Posting To** field, and then enter the last date the user will be able to post to the company.</span></span>  

## <a name="see-also"></a><span data-ttu-id="3b77d-124">Zie ook</span><span class="sxs-lookup"><span data-stu-id="3b77d-124">See Also</span></span>  
 <span data-ttu-id="3b77d-125">[Belgische lokale functionaliteit](belgium-local-functionality.md) </span><span class="sxs-lookup"><span data-stu-id="3b77d-125">[Belgium Local Functionality](belgium-local-functionality.md) </span></span>  
 [<span data-ttu-id="3b77d-126">Boekingsperioden opgeven</span><span class="sxs-lookup"><span data-stu-id="3b77d-126">Specify Posting Periods</span></span>](../../finance-how-specify-posting-periods.md)
