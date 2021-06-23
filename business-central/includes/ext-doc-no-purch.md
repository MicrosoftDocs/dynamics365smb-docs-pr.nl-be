---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 05/27/2021
ms.author: edupont
ms.openlocfilehash: 59376b96dcd6f755040b07784ceca53e157bcf14
ms.sourcegitcommit: f9a190933eadf4608f591e2f1b04c69f1e5c0dc7
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116054"
---
<span data-ttu-id="50809-101">Op inkoopdocumenten en dagboeken kunt u een documentnummer opgeven dat verwijst naar het nummeringssysteem van de leverancier.</span><span class="sxs-lookup"><span data-stu-id="50809-101">On purchase documents and journals, you can specify a document number that refers to the vendor's numbering system.</span></span> <span data-ttu-id="50809-102">Gebruik dit veld om het nummer vast te leggen dat de leverancier aan de order, factuur of creditnota heeft toegewezen.</span><span class="sxs-lookup"><span data-stu-id="50809-102">Use this field to record the number that the vendor assigned to the order, invoice, or credit memo.</span></span> <span data-ttu-id="50809-103">U kunt dit externe documentnummer later gebruiken als u om de een of andere reden de geboekte post moet zoeken met dit nummer.</span><span class="sxs-lookup"><span data-stu-id="50809-103">You can then use the number later if, for some reason, you need to search for the posted entry using this number.</span></span>

<span data-ttu-id="50809-104">Het veld **Extern documentnr. verplicht** op de pagina **Inkoopinstellingen** geeft aan of het verplicht is om een extern documentnummer in te voeren in de volgende situaties:</span><span class="sxs-lookup"><span data-stu-id="50809-104">The **Ext. Doc. No. Mandatory** field in the **Purchases & Payables Setup** page specifies whether it is mandatory to enter an external document number in the following situations:</span></span>

* <span data-ttu-id="50809-105">In het veld **Leveranciersfactuurnr.**, het veld **Ordernr. leverancier**</span><span class="sxs-lookup"><span data-stu-id="50809-105">In the **Vendor Invoice No.** field, **Vendor Order No.**</span></span> <span data-ttu-id="50809-106">of het veld **Creditnotanr. leverancier**</span><span class="sxs-lookup"><span data-stu-id="50809-106">field, or the **Vendor Cr. Memo No.**</span></span> <span data-ttu-id="50809-107">in een inkoopkop</span><span class="sxs-lookup"><span data-stu-id="50809-107">field on a purchase header</span></span>

* <span data-ttu-id="50809-108">In het veld **Extern documentnr.** op een dagboekregel, waarbij *Factuur*, *Creditnota* of *Rentefactuur* in het veld **Documentsoort** staat en *Leverancier* in het veld **Rekeningsoort**.</span><span class="sxs-lookup"><span data-stu-id="50809-108">In the **External Document No.** field on a general journal line, where the **Document Type** field is set to *Invoice*, *Credit Memo*, or *Finance Charge Memo*, and the **Account Type** field is set to *Vendor*.</span></span>

<span data-ttu-id="50809-109">Als u dit veld selecteert, is het niet mogelijk om een factuur, een creditnota of het bovengenoemde soort dagboekregel te boeken zonder een extern documentnummer.</span><span class="sxs-lookup"><span data-stu-id="50809-109">If you select this field, it will not be possible to post an invoice, a credit memo, or the type of general journal line described above without an external document number.</span></span>

<span data-ttu-id="50809-110">Het externe documentnummer wordt opgenomen in geboekte documenten waar u kunt zoeken op het betreffende nummer.</span><span class="sxs-lookup"><span data-stu-id="50809-110">The external document number is included in posted documents where you can search by the relevant number.</span></span> <span data-ttu-id="50809-111">U kunt ook zoeken met behulp van het externe documentnummer wanneer u door leveranciersposten navigeert.</span><span class="sxs-lookup"><span data-stu-id="50809-111">You can also search using the external document number when navigating on vendor ledger entries.</span></span>

<span data-ttu-id="50809-112">Een andere manier om met externe documentnummers om te gaan is het veld **Uw referentie** te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="50809-112">A different way to handle external document numbers is to use the **Your Reference** field.</span></span> <span data-ttu-id="50809-113">Als u het veld **Uw referentie** gebruikt, wordt het nummer opgenomen in geboekte documenten en kunt u er op dezelfde manier op zoeken als naar waarden van **Extern documentnr.**-velden.</span><span class="sxs-lookup"><span data-stu-id="50809-113">If you use the **Your Reference** field, the number will be included in posted documents, and you can search by it in the same way as for values from **External Document No.** fields.</span></span> <span data-ttu-id="50809-114">Maar het veld is niet beschikbaar op journaalregels.</span><span class="sxs-lookup"><span data-stu-id="50809-114">But the field is not available on journal lines.</span></span>
