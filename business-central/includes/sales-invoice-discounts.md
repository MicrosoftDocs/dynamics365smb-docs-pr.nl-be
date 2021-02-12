---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/20/2021
ms.author: edupont
ms.openlocfilehash: 718845561c1a18701d20b93ebdc8339308ce7ac8
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035809"
---
<span data-ttu-id="08882-101">Wanneer alle artikelen op de verkooporderregels zijn ingevoerd, kunt u de factuurkorting voor het hele verkoopdocument berekenen door de actie **Factuurkorting berekenen**.</span><span class="sxs-lookup"><span data-stu-id="08882-101">When all the items have been entered on the sales order lines, you can calculate the invoice discount for the entire sales document by choosing the **Calculate Invoice Discount** action.</span></span>

<span data-ttu-id="08882-102">Als het veld **Factuurkorting berekenen** is ingeschakeld in het venster **Verkoopinstellingen**, wordt de factuurkorting automatisch berekend als een van de volgende doet in een verkoopdocument:</span><span class="sxs-lookup"><span data-stu-id="08882-102">If the **Calc. Inv. Discount** field is selected in the **Sales and Receivables Setup** window, then the invoice discount is calculated automatically when you do either of the following on a sales document:</span></span>

* <span data-ttu-id="08882-103">Statistieken weergeven</span><span class="sxs-lookup"><span data-stu-id="08882-103">View statistics</span></span>
* <span data-ttu-id="08882-104">Een testrapport weergeven</span><span class="sxs-lookup"><span data-stu-id="08882-104">View a test report</span></span>
* <span data-ttu-id="08882-105">Afdrukken</span><span class="sxs-lookup"><span data-stu-id="08882-105">Print</span></span>
* <span data-ttu-id="08882-106">Post</span><span class="sxs-lookup"><span data-stu-id="08882-106">Post</span></span>

<span data-ttu-id="08882-107">De korting wordt evenredig verdeeld over alle regels op het verkoopdocument voor artikelen waarvan het veld **Factuurkorting berekenen** op de verkooporderregel is ingesteld op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="08882-107">The discount is apportioned over all the lines in the sales document for items where the **Allow Invoice Disc.** field on the sales order line contains **Yes**.</span></span> <span data-ttu-id="08882-108">Dit is de standaardinstelling voor artikelen.</span><span class="sxs-lookup"><span data-stu-id="08882-108">This is the default setting for items.</span></span>

<span data-ttu-id="08882-109">De factuurkortingscondities worden gedefinieerd op de pagina **Factuurkortingen berekenen** om de factuurkorting te berekenen.</span><span class="sxs-lookup"><span data-stu-id="08882-109">The invoice discount terms are defined in the **Cust. Invoice Discounts** page to calculate the invoice discount.</span></span> <span data-ttu-id="08882-110">De valutacode op het verkoopdocument wordt gebruikt om de factuurkortingscondities in de bijbehorende valuta te zoeken.</span><span class="sxs-lookup"><span data-stu-id="08882-110">The currency code on the sales document is used to find the invoice discount terms in the corresponding currency.</span></span>

<span data-ttu-id="08882-111">Als u geen factuurkortingen hebt gedefinieerd voor vreemde valuta's, worden de factuurkortingscondities die op de pagina **Factuurkortingen berekenen** zijn gedefinieerd, met bedragen in uw lokale valuta en de wisselkoers op de boekingsdatum in het verkoopdocument gebruikt om de factuurkorting in de vreemde valuta te berekenen.</span><span class="sxs-lookup"><span data-stu-id="08882-111">If invoice discounts have not been defined for foreign currencies, then the invoice discount terms defined in the **Cust. Invoice Discounts** page with amounts in your local currency and the exchange rate on the posting date on the sales document are used to calculate the invoice discount in the foreign currency.</span></span>
