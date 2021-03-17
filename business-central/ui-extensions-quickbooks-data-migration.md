---
title: QuickBooks-extensie Migratie | Microsoft Docs
description: Beschrijft hoe u de extensie gebruikt om klanten, leveranciers, artikelen en rekeningen van QuickBooks Desktop naar Business Central te importeren.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 990aabaaccbf32a5cbd95c09527657757e5182cb
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5391436"
---
# <a name="the-quickbooks-data-migration-extension"></a><span data-ttu-id="832d4-103">De QuickBooks-extensie gegevensmigratie</span><span class="sxs-lookup"><span data-stu-id="832d4-103">The QuickBooks Data Migration Extension</span></span>

<span data-ttu-id="832d4-104">Met deze extensie kunt u gemakkelijk klanten, leveranciers, artikelen en accounts vanuit QuickBooks naar [!INCLUDE[prod_short](includes/prod_short.md)] migreren.</span><span class="sxs-lookup"><span data-stu-id="832d4-104">This extension makes it easy to migrate customers, vendors, items, and accounts from QuickBooks to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="832d4-105">Als uw bedrijf momenteel QuickBooks gebruikt, kunt u de relevante gegevens exporteren en vervolgens een begeleide instelling openen om de gegevens naar [!INCLUDE[prod_short](includes/prod_short.md)] te uploaden.</span><span class="sxs-lookup"><span data-stu-id="832d4-105">If your business uses QuickBooks today, you can export the relevant information and then open an assisted setup guide to upload the data to [!INCLUDE[prod_short](includes/prod_short.md)].</span></span>  
<span data-ttu-id="832d4-106">Zie [Gegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="832d4-106">For more information, see [Importing Business Data from Other Finance Systems](across-import-data-configuration-packages.md).</span></span>

## <a name="data-from-quickbooks-desktop"></a><span data-ttu-id="832d4-107">Gegevens vanuit QuickBooks Desktop</span><span class="sxs-lookup"><span data-stu-id="832d4-107">Data from QuickBooks Desktop</span></span>

<span data-ttu-id="832d4-108">U kunt de volgende gegevens uit QuickBooks Online importeren naar Business Central:</span><span class="sxs-lookup"><span data-stu-id="832d4-108">You can import the following data from QuickBooks Online to Business Central:</span></span>

- <span data-ttu-id="832d4-109">Klanten</span><span class="sxs-lookup"><span data-stu-id="832d4-109">Customers</span></span>  
- <span data-ttu-id="832d4-110">Leveranc.</span><span class="sxs-lookup"><span data-stu-id="832d4-110">Vendors</span></span>  
- <span data-ttu-id="832d4-111">Artikelen</span><span class="sxs-lookup"><span data-stu-id="832d4-111">Items</span></span>  
- <span data-ttu-id="832d4-112">Rekeningschema</span><span class="sxs-lookup"><span data-stu-id="832d4-112">Chart of Accounts</span></span>  
- <span data-ttu-id="832d4-113">Beginsaldotransacties in het grootboek</span><span class="sxs-lookup"><span data-stu-id="832d4-113">Beginning Balance transactions in General Ledger</span></span>  
- <span data-ttu-id="832d4-114">In voorraad aantallen voor voorraadartikelen</span><span class="sxs-lookup"><span data-stu-id="832d4-114">On-hand Quantities for Inventory Items</span></span>  
- <span data-ttu-id="832d4-115">Open documenten voor klanten en leveranciers, zoals facturen, creditnota's en betalingen</span><span class="sxs-lookup"><span data-stu-id="832d4-115">Open documents for customers and vendors, such as invoices, credit memos and payments</span></span>  

<span data-ttu-id="832d4-116">Wij migreren alleen hele bedragen op verkoop- en inkoopdocumenten.</span><span class="sxs-lookup"><span data-stu-id="832d4-116">We migrate only full amounts on sales and purchase documents.</span></span> <span data-ttu-id="832d4-117">We werken geen gedeeltelijk betaalde bedragen bij.</span><span class="sxs-lookup"><span data-stu-id="832d4-117">We do not update partially paid amounts.</span></span> <span data-ttu-id="832d4-118">Als een klant bijvoorbeeld 300 van een totaal van 500 euro op een verkoopfactuur heeft voldaan, migreren we de hele 500.</span><span class="sxs-lookup"><span data-stu-id="832d4-118">For example, if a customer has paid 300 of a total of 500 dollars on a sales invoice, we migrate the full 500.</span></span> <span data-ttu-id="832d4-119">Wanneer u gedeeltelijke betalingen hebt ontvangen, moet u deze handmatig bijwerken, voordat of nadat u gegevens migreert.</span><span class="sxs-lookup"><span data-stu-id="832d4-119">If you have received partial payments, you must update these manually, either before or after you migrate data.</span></span> <span data-ttu-id="832d4-120">Het is raadzaam openstaande transacties te vereffenen voordat u migreert, om zaken achteraf gemakkelijker te maken.</span><span class="sxs-lookup"><span data-stu-id="832d4-120">We recommend that you apply outstanding transactions before you migrate, just to make things easier afterward.</span></span>

> [!NOTE]
> <span data-ttu-id="832d4-121">Wij migreren geen inkooporders of verkooporders.</span><span class="sxs-lookup"><span data-stu-id="832d4-121">We do not migrate purchase orders or sales orders.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="832d4-122">Voordat u begint</span><span class="sxs-lookup"><span data-stu-id="832d4-122">Before You Start</span></span>

<span data-ttu-id="832d4-123">Een belangrijk deel van het migratieproces is de rekeningen opgeven waarnaar transacties moeten worden gemigreerd.</span><span class="sxs-lookup"><span data-stu-id="832d4-123">An important part of the migration process is to specify the accounts to migrate transactions to.</span></span> <span data-ttu-id="832d4-124">Het is aan te raden deze koppeling te plannen voordat u gegevens migreert.</span><span class="sxs-lookup"><span data-stu-id="832d4-124">It's a good idea to plan this mapping before you migrate data.</span></span> <span data-ttu-id="832d4-125">Bijvoorbeeld, de rekeningen waarnaar u transacties boekt voor:</span><span class="sxs-lookup"><span data-stu-id="832d4-125">For example, the accounts where you post transactions for:</span></span>

- <span data-ttu-id="832d4-126">De verkoop van artikelen of services aan klanten</span><span class="sxs-lookup"><span data-stu-id="832d4-126">The sale of items or services to customers</span></span>  
- <span data-ttu-id="832d4-127">De aankoop van artikelen of services van leveranciers</span><span class="sxs-lookup"><span data-stu-id="832d4-127">The purchase of items or services from vendors</span></span>  
- <span data-ttu-id="832d4-128">Herwaarderingen in het grootboek</span><span class="sxs-lookup"><span data-stu-id="832d4-128">Adjustments in the general ledger</span></span>  

<span data-ttu-id="832d4-129">Business Central vereist dat aan grootboekrekeningen rekeningnummers zijn toegewezen.</span><span class="sxs-lookup"><span data-stu-id="832d4-129">Business Central requires that general ledger accounts have account numbers assigned to them.</span></span> <span data-ttu-id="832d4-130">Zorg ervoor dat rekeningnummers zijn toegewezen aan uw rekeningen in QuickBooks.</span><span class="sxs-lookup"><span data-stu-id="832d4-130">Make sure that account numbers are assigned to your accounts in QuickBooks.</span></span>
<span data-ttu-id="832d4-131">Als transacties in QuickBooks belastingbedragen hebben, moet u eerst een belastingrekening instellen voor uw belastingjurisdictie in Business Central, voordat u transacties kunt boeken.</span><span class="sxs-lookup"><span data-stu-id="832d4-131">If transactions in QuickBooks have tax amounts, you must set up a tax account for your tax jurisdictions in Business Central before you can post transactions.</span></span>

<span data-ttu-id="832d4-132">Als u de gegevens uit de QuickBooks Desktop-toepassing wilt ophalen, moet u de Microsoft-tool Data Exporter downloaden.</span><span class="sxs-lookup"><span data-stu-id="832d4-132">In order to get your data out of the QuickBooks desktop application you will need to download the Microsoft Data Exporter Tool.</span></span>  <span data-ttu-id="832d4-133">De instructies voor de tool bevinden zich in de wizard Gegevensmigratie in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="832d4-133">The instructions for the tool are in the Data Migration Wizard in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="832d4-134">Het hulpprogramma maakt verbinding met uw QuickBooks-toepassing en exporteert de toepasselijke gegevens naar een .zip-bestand.</span><span class="sxs-lookup"><span data-stu-id="832d4-134">The tool will connect to your QuickBooks application and export the applicable data to a .zip file.</span></span>  

> [!NOTE]
> <span data-ttu-id="832d4-135">Momenteel werkt de tool Data Exporter alleen met QuickBooks 2017 en 2018.</span><span class="sxs-lookup"><span data-stu-id="832d4-135">Currently the data exporter tool only works with QuickBooks 2017 and 2018.</span></span>

## <a name="finding-the-quickbooks-data-migration-extension"></a><span data-ttu-id="832d4-136">De extensie QuickBooks-gegevensmigratie vinden</span><span class="sxs-lookup"><span data-stu-id="832d4-136">Finding the QuickBooks Data Migration Extension</span></span>

<span data-ttu-id="832d4-137">De extensie QuickBooks-gegevensmigratie is geïnstalleerd en kan worden gebruikt als geïntegreerd onderdeel van de begeleide instelling Gegevensmigratie.</span><span class="sxs-lookup"><span data-stu-id="832d4-137">The QuickBooks Data Migration extension is installed and ready to go as an integrated part of the Data Migration assisted setup guide.</span></span> <span data-ttu-id="832d4-138">Als u klaar bent om nu aan de slag te gaan en uw gegevens uit QuickBooks hebt geëxporteerd, kiest u het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voert u **Begeleide instelling** in en kiest u vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="832d4-138">If you are ready to get started now, and have exported your data from QuickBooks, choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Assisted Setup**, and then choose the related link.</span></span> <span data-ttu-id="832d4-139">Kies **Bedrijfsgegevens migreren** en voer de stappen in de handleiding uit.</span><span class="sxs-lookup"><span data-stu-id="832d4-139">Choose **Migrate business data**, and then follow the steps in the guide.</span></span>  

## <a name="what-do-i-do-after-i-migrate-data"></a><span data-ttu-id="832d4-140">Wat doe ik nadat ik gegevens heb gemigreerd?</span><span class="sxs-lookup"><span data-stu-id="832d4-140">What do I do after I migrate Data?</span></span>

<span data-ttu-id="832d4-141">Nadat u gegevens migreert, hebben transacties de status Niet geboekt, zodat u deze kunt controleren en correcties kunt aanbrengen.</span><span class="sxs-lookup"><span data-stu-id="832d4-141">After you migrate data, transactions have the status Unposted, so you can review them and make adjustments.</span></span> <span data-ttu-id="832d4-142">Als u de transacties wilt controleren, gaat u naar de pagina waar u deze normaal zou vinden.</span><span class="sxs-lookup"><span data-stu-id="832d4-142">To review the transactions, go to the page where you would normally find them.</span></span> <span data-ttu-id="832d4-143">Als u bijvoorbeeld ongeboekte verkoopfacturen wilt controleren, gaat u naar de pagina Verkoopfacturen.</span><span class="sxs-lookup"><span data-stu-id="832d4-143">For example, to review unposted sales invoices, go to the Sales Invoices page.</span></span> <span data-ttu-id="832d4-144">Als u betalingsdagboeken wilt controleren, gaat u naar de pagina Betalingsdagboeken.</span><span class="sxs-lookup"><span data-stu-id="832d4-144">To review payment journals, go to the Payment Journals page.</span></span>
<span data-ttu-id="832d4-145">Er is met name een aantal dingen die u moet doen: als de transacties in QuickBooks opslag of kortingen bevatten, moet u de bedragen handmatig optellen bij de gerelateerde transacties in Business Central voordat u deze boekt.</span><span class="sxs-lookup"><span data-stu-id="832d4-145">There are a few things in particular that you should do: If the transactions in QuickBooks had markup or discount amounts, you must manually add the amounts to the related transactions in Business Central before you post them.</span></span>
<span data-ttu-id="832d4-146">Als u btw gebruikt, hebt u mogelijk een bedrijfsboekingsgroep en een productboekingsgroep in de boekingsinstellingen nodig, zodat u btw-bedragen kunt boeken.</span><span class="sxs-lookup"><span data-stu-id="832d4-146">If you are using value added tax (VAT), you may need to add a business posting group and a product posting group to the posting setup so that you can post VAT amounts.</span></span>
<span data-ttu-id="832d4-147">Controleer de beginsaldi voor de rekeningen in het grootboek.</span><span class="sxs-lookup"><span data-stu-id="832d4-147">Verify the beginning balances for accounts in the general ledger.</span></span> <span data-ttu-id="832d4-148">QuickBooks slaat het huidige saldo van alle rekeningen niet op, dus u moet mogelijk beginsaldi corrigeren.</span><span class="sxs-lookup"><span data-stu-id="832d4-148">QuickBooks does not store the current balance for all accounts, so you might need to correct beginning balances.</span></span>

## <a name="see-also"></a><span data-ttu-id="832d4-149">Zie ook</span><span class="sxs-lookup"><span data-stu-id="832d4-149">See Also</span></span>

[<span data-ttu-id="832d4-150">Bedrijfsgegevens importeren uit andere financiële systemen</span><span class="sxs-lookup"><span data-stu-id="832d4-150">Importing Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
<span data-ttu-id="832d4-151">[[!INCLUDE[prod_short](includes/prod_short.md)] aanpassen met behulp van extensies](ui-extensions.md)</span><span class="sxs-lookup"><span data-stu-id="832d4-151">[Customizing [!INCLUDE[prod_short](includes/prod_short.md)] Using Extensions ](ui-extensions.md)</span></span>  


[!INCLUDE[footer-include](includes/footer-banner.md)]