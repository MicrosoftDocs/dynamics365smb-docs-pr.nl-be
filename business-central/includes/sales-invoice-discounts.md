---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/25/2021
ms.author: edupont
ms.openlocfilehash: 539ee2eb2c9e4a71eacfb78d95320870128fb1d9
ms.sourcegitcommit: cb06aa973f5c767df774b0e1e199c6fbe0e85b88
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470299"
---
<span data-ttu-id="c5f31-101">Wanneer alle artikelen op de orderregels zijn ingevoerd, kunt u de factuurkorting voor het hele document berekenen door de actie **Factuurkorting berekenen** te kiezen.</span><span class="sxs-lookup"><span data-stu-id="c5f31-101">When all the items have been entered on the sales lines, you can calculate the invoice discount for the entire document by choosing the **Calculate Invoice Discount** action.</span></span>

<span data-ttu-id="c5f31-102">De korting wordt berekend op basis van alle regels in het verkoopdocument voor artikelen waarvan het veld **Factuurkorting toestaan** op de verkooporderregel **Ja** bevat.</span><span class="sxs-lookup"><span data-stu-id="c5f31-102">The discount is calculated based on all the lines in the sales document for items where the **Allow Invoice Disc.** field on the sales order line contains **Yes**.</span></span> <span data-ttu-id="c5f31-103">Dit is de standaardinstelling voor artikelen.</span><span class="sxs-lookup"><span data-stu-id="c5f31-103">This is the default setting for items.</span></span> <span data-ttu-id="c5f31-104">Regels met artikeltoeslagen worden bijvoorbeeld niet meegenomen in de berekening van de factuurkorting.</span><span class="sxs-lookup"><span data-stu-id="c5f31-104">Lines with item charges, for example, are not included in the calculation of the invoice discount.</span></span> <span data-ttu-id="c5f31-105">Als u op dergelijke regels een korting wilt toepassen, moet u het veld **Regelkorting %** instellen op de relevante regels.</span><span class="sxs-lookup"><span data-stu-id="c5f31-105">If you want to apply a discount to such lines, you must set the **Line Discount %** field on the relevant lines.</span></span>  

> [!TIP]
> <span data-ttu-id="c5f31-106">Als het veld **Factuurkorting berekenen** is ingeschakeld op de pagina **Verkoopinstellingen**, wordt de factuurkorting automatisch berekend als u een van de volgende doet in een verkoopdocument:</span><span class="sxs-lookup"><span data-stu-id="c5f31-106">If the **Calc. Inv. Discount** field is selected in the **Sales and Receivables Setup** page, then the invoice discount is calculated automatically when you do either of the following on a sales document:</span></span>
>
> * <span data-ttu-id="c5f31-107">Statistieken weergeven</span><span class="sxs-lookup"><span data-stu-id="c5f31-107">View statistics</span></span>
> * <span data-ttu-id="c5f31-108">Een testrapport weergeven</span><span class="sxs-lookup"><span data-stu-id="c5f31-108">View a test report</span></span>
> * <span data-ttu-id="c5f31-109">Afdrukken</span><span class="sxs-lookup"><span data-stu-id="c5f31-109">Print</span></span>
> * <span data-ttu-id="c5f31-110">Post</span><span class="sxs-lookup"><span data-stu-id="c5f31-110">Post</span></span>

<span data-ttu-id="c5f31-111">De factuurkortingscondities voor een klant worden gedefinieerd op de pagina **Verkoopfactuurkorting** voor de klant.</span><span class="sxs-lookup"><span data-stu-id="c5f31-111">The invoice discount terms for a customer are defined in the **Cust. Invoice Discounts** page for the customer.</span></span> <span data-ttu-id="c5f31-112">De valutacode op het verkoopdocument wordt gebruikt om de factuurkortingscondities in de bijbehorende valuta te zoeken.</span><span class="sxs-lookup"><span data-stu-id="c5f31-112">The currency code on the sales document is used to find the invoice discount terms in the corresponding currency.</span></span>

<span data-ttu-id="c5f31-113">Als u geen factuurkortingen hebt gedefinieerd voor vreemde valuta's, worden de factuurkortingscondities die op de pagina **Factuurkortingen berekenen** zijn gedefinieerd, met bedragen in uw lokale valuta en de wisselkoers op de boekingsdatum in het verkoopdocument gebruikt om de factuurkorting in de vreemde valuta te berekenen.</span><span class="sxs-lookup"><span data-stu-id="c5f31-113">If invoice discounts have not been defined for foreign currencies, then the invoice discount terms defined in the **Cust. Invoice Discounts** page with amounts in your local currency and the exchange rate on the posting date on the sales document are used to calculate the invoice discount in the foreign currency.</span></span>
