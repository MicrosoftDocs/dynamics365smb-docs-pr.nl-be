---
title: "Btw-nummers verifiëren | Microsoft Docs"
description: U kunt een EU-webservice gebruiken om te controleren of btw-nummers die u op klanten-, leveranciers- of contactkaarten invoert, geldig zijn.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/10/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 7180c7823055dba52a398584ed2f4c2952d08492
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-verify-vat-registration-numbers"></a><span data-ttu-id="68920-103">Procedure: btw-nummers verifiëren</span><span class="sxs-lookup"><span data-stu-id="68920-103">How to: Verify VAT Registration Numbers</span></span>
<span data-ttu-id="68920-104">U kunt een EU-webservice gebruiken om te controleren of btw-nummers die u op klanten-, leveranciers- of contactkaarten invoert, geldig zijn.</span><span class="sxs-lookup"><span data-stu-id="68920-104">You can use an EU web service to verify that VAT registration numbers that you enter on customer, vendor, or contact cards are valid.</span></span>  

 <span data-ttu-id="68920-105">Wanneer u het veld **VAT Registration No.** wijzigt op een kaart waar de waarde in het veld **Land-/regiocode** een EU-land/regio is, worden het nieuwe btw-nummer en uw gebruikers-ID vastgelegd in het venster **Btw-log**.</span><span class="sxs-lookup"><span data-stu-id="68920-105">When you modify the **VAT Registration No.** field on a card where the value in the **Country/Region Code** field is an EU country/region, then the new VAT registration number and your user ID are logged in the **VAT Registration Log** window.</span></span> <span data-ttu-id="68920-106">U controleert een btw-nummer door te klikken op de knop **Btw-nummer controleren** controleren in het venster **Btw-log**.</span><span class="sxs-lookup"><span data-stu-id="68920-106">You verify a VAT registration number by choosing the **Verify Registration No.** button in the **VAT Registration Log** window.</span></span> <span data-ttu-id="68920-107">Er wordt een nieuwe regel gemaakt wanneer u de verificatiefunctie gebruikt.</span><span class="sxs-lookup"><span data-stu-id="68920-107">A new line is created every time you use the verification function.</span></span> <span data-ttu-id="68920-108">Als het nummer geverifieerd kan worden, bevat het veld **Status** de waarde **Geldig**.</span><span class="sxs-lookup"><span data-stu-id="68920-108">If the number could be verified, the **Status** field contains **Valid**.</span></span> <span data-ttu-id="68920-109">Als het nummer niet geverifieerd kan worden, bevat het veld **Status** de waarde **Ongeldig** en moet u het nummer in het veld **Btw-nummer** op de kaart wijzigen en de verificatiefunctie opnieuw starten.</span><span class="sxs-lookup"><span data-stu-id="68920-109">If the number could not be verified, the **Status** field contains **Invalid**, and you must then change the number in the **VAT Registration No.** field on the card and start the verification function again.</span></span>  

 <span data-ttu-id="68920-110">De URL van de standaardwebservice is ingesteld in het veld **Validatie-URL btw-nummer** in het venster **Grootboekinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="68920-110">The URL of the default web service is set up in the **VAT Reg. No. Validation URL** field in the **General Ledger Setup** window.</span></span>  

 <span data-ttu-id="68920-111">In de tabel **Btw-nummerformaat** kunt u voor elk land/regio de verschillende indelingen van het btw-registratienummer kiezen die gebruikers mogen invoeren in het veld **Btw-nummer**.</span><span class="sxs-lookup"><span data-stu-id="68920-111">In the **VAT Registration No. Format** table, you can change for each country/region the different formats of VAT registration number that users are allowed to enter in the **VAT Registration No.** field.</span></span>  

> [!WARNING]  
>  <span data-ttu-id="68920-112">Deze webservice gebruikt het http-protocol, wat betekent dat gegevens die door de server worden overgebracht, niet zijn versleuteld.</span><span class="sxs-lookup"><span data-stu-id="68920-112">This web service uses the http protocol, which means that data transferred through the service is not encrypted.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="68920-113">Er kunnen onderbrekingen optreden voor deze service waarvoor Microsoft niet verantwoordelijk is, aangezien de service onderdeel is van een breed EU-netwerk van nationale btw-journalen.</span><span class="sxs-lookup"><span data-stu-id="68920-113">You may experience downtime for this service for which Microsoft is not responsible, as the service is part of a broad EU network of national VAT registers.</span></span>  

## <a name="to-verify-a-vat-registration-number-from-a-customer-card"></a><span data-ttu-id="68920-114">Btw-nummer van een klantenkaart verifiëren</span><span class="sxs-lookup"><span data-stu-id="68920-114">To verify a VAT registration number from a customer card</span></span>  
<span data-ttu-id="68920-115">Hierna wordt beschreven hoe u een btw-nummer voor een klant kunt verifiëren.</span><span class="sxs-lookup"><span data-stu-id="68920-115">The following describes how to verify a VAT registration number for a customer.</span></span> <span data-ttu-id="68920-116">De stappen zijn voor contactpersonen en leveranciers vergelijkbaar.</span><span class="sxs-lookup"><span data-stu-id="68920-116">The steps are similar for a vendor and a contact.</span></span>   
1.  <span data-ttu-id="68920-117">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Klanten** in en klik vervolgens op de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="68920-117">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>  

2.  <span data-ttu-id="68920-118">Open de kaart van een klant waarvan u het btw-nummer wilt verifiëren.</span><span class="sxs-lookup"><span data-stu-id="68920-118">Open the card of a customer where you want to verify the VAT registration number.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="68920-119">Het veld **Land-/regiocode** op de klantenkaart moet een EU-land/regio bevatten.</span><span class="sxs-lookup"><span data-stu-id="68920-119">The **Country/Region Code** field on the customer card must contain an EU country/region.</span></span>  
3.  <span data-ttu-id="68920-120">Klik op het sneltabblad **Facturering** op de detailknop naast het veld **Btw-nummer**.</span><span class="sxs-lookup"><span data-stu-id="68920-120">On the **Invoicing** FastTab, choose the DrillDown button next to the **VAT Registration No.** field.</span></span>  

    <span data-ttu-id="68920-121">Het venster **Btw-log** wordt geopend met één regel waar het veld **Status** de tekst **Niet gecontroleerd** bevat.</span><span class="sxs-lookup"><span data-stu-id="68920-121">The **VAT Registration Log** window opens showing one line where the **Status** field contains **Not Verified**.</span></span>  
4.  <span data-ttu-id="68920-122">Kies de actie **Btw-nummer controleren**.</span><span class="sxs-lookup"><span data-stu-id="68920-122">Choose the **Verify Registration No.** action.</span></span>  

     <span data-ttu-id="68920-123">Er wordt een nieuwe regel gemaakt waarbij het veld **Status** de waarde **Geldig** of **Ongeldig** bevat.</span><span class="sxs-lookup"><span data-stu-id="68920-123">A new line is created where the **Status** field contains either **Valid** or **Invalid**.</span></span>  
5.  <span data-ttu-id="68920-124">Als het veld **Status** de tekst **Ongeldig** bevat, wijzigt u het nummer in het veld **Btw-nummer** op de kaart en herhaalt u stap 3 en 4.</span><span class="sxs-lookup"><span data-stu-id="68920-124">If the **Status** field contains **Invalid**, change the number in the **VAT Registration No.** field on the card, and then repeat steps 3 through 4.</span></span>  

## <a name="see-also"></a><span data-ttu-id="68920-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="68920-125">See Also</span></span>  
[<span data-ttu-id="68920-126">Financiën</span><span class="sxs-lookup"><span data-stu-id="68920-126">Finance</span></span>](finance.md)  
[<span data-ttu-id="68920-127">Procedure: Nieuwe klanten registreren</span><span class="sxs-lookup"><span data-stu-id="68920-127">How to: Register New Customers</span></span>](sales-how-register-new-customers.md)  
[<span data-ttu-id="68920-128">Procedure: Nieuwe leveranciers registreren</span><span class="sxs-lookup"><span data-stu-id="68920-128">How to: Register New Vendors</span></span>](purchasing-how-register-new-vendors.md)  
<span data-ttu-id="68920-129">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="68920-129">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

