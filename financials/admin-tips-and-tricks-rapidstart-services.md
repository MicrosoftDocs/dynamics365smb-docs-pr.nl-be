---
title: Tips en trucs - RapidStart Services | Microsoft Docs
description: Wanneer u bedrijven configureert met RapidStart Services, zijn er enkele tips en trucs die u kunt gebruiken om uw implementatie vlot te laten verlopen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e43859a6095f0087c12d0f9c071c0504d3781ad2
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="tips-and-tricks-rapidstart-services"></a><span data-ttu-id="5773b-103">Tips en trucs: RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="5773b-103">Tips and Tricks: RapidStart Services</span></span>
<span data-ttu-id="5773b-104">Wanneer u bedrijven configureert met RapidStart Services, zijn er enkele tips en trucs die u kunt gebruiken om uw implementatie vlot te laten verlopen.</span><span class="sxs-lookup"><span data-stu-id="5773b-104">When you configure companies using RapidStart Services, there are some tips and tricks that you can take advantage of to help your implementation go smoothly.</span></span>  

## <a name="take-advantage-of-configuration-templates"></a><span data-ttu-id="5773b-105">Gebruikmaken van configuratiesjablonen</span><span class="sxs-lookup"><span data-stu-id="5773b-105">Take advantage of configuration templates</span></span>  
<span data-ttu-id="5773b-106">Configuratiesjablonen kunnen u helpen uw implementatie te stroomlijnen.</span><span class="sxs-lookup"><span data-stu-id="5773b-106">Configuration templates can help you streamline your implementation process.</span></span> <span data-ttu-id="5773b-107">U kunt via deze sjablonen vergelijkbare klanten opnemen in segmenten en een implementatieprotocol ontwikkelen die alle klanten in een segment op een vergelijkbare wijze behandelt.</span><span class="sxs-lookup"><span data-stu-id="5773b-107">By using them, you can include similar customers in segments and then develop an implementation protocol that treats all customers in a segment in a similar manner.</span></span> <span data-ttu-id="5773b-108">Op die manier kunt u meteen een preconfiguratie toepassen op elk segment en doorgaan met een snelle implementatie.</span><span class="sxs-lookup"><span data-stu-id="5773b-108">In that way, you can apply a level of preconfiguration to each segment and continue with a rapid implementation.</span></span>  

## <a name="configuration-questionnaires"></a><span data-ttu-id="5773b-109">Configuratievragenlijsten</span><span class="sxs-lookup"><span data-stu-id="5773b-109">Configuration questionnaires</span></span>  
<span data-ttu-id="5773b-110">Om het invullen van een configuratievragenlijst sneller te laten verlopen, kunt u standaardantwoorden definiëren om aanbevolen procedures aan te geven.</span><span class="sxs-lookup"><span data-stu-id="5773b-110">To aid the process of filling out a configuration questionnaire, consider defining default answers to indicate best practices.</span></span>  

## <a name="batch-creation-of-journal-lines"></a><span data-ttu-id="5773b-111">Dagboekregels in batch aanmaken</span><span class="sxs-lookup"><span data-stu-id="5773b-111">Batch creation of journal lines</span></span>  
<span data-ttu-id="5773b-112">Het is raadzaam dat u de hulpprogramma's voor gegevensmigratie gebruikt voor het migreren van dagboekposten.</span><span class="sxs-lookup"><span data-stu-id="5773b-112">We recommend that you use the data migration tools provided to migrate journal entries.</span></span> <span data-ttu-id="5773b-113">Als u een batchtaak gebruikt om dagboekregels te maken, heeft deze een beperkt bereik en maakt deze enkel pre-standaardvelden in een dagboek.</span><span class="sxs-lookup"><span data-stu-id="5773b-113">Otherwise, if you use a batch job to create journal lines, that has a limited scope and only generates pre-default fields into a journal.</span></span> <span data-ttu-id="5773b-114">De rest van het dagboek moet vervolgens handmatig worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="5773b-114">The rest of the journal then has to be completed manually.</span></span>  

## <a name="migrating-transactions"></a><span data-ttu-id="5773b-115">Transacties migreren</span><span class="sxs-lookup"><span data-stu-id="5773b-115">Migrating transactions</span></span>  
<span data-ttu-id="5773b-116">Het is raadzaam om beginsaldi in de volgende volgorde te migreren.</span><span class="sxs-lookup"><span data-stu-id="5773b-116">We recommend that you migrate opening balances in the following order.</span></span>  

1.  <span data-ttu-id="5773b-117">Migreer beginsaldi uit het grootboek zonder de subgrootboeken van de grootboekrekening te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="5773b-117">Migrate general ledger opening balances without using the general ledger account subledgers.</span></span> <span data-ttu-id="5773b-118">Gebruik specifieke uitstellende rekeningen voor beginsaldi, waarbij voor elk subgrootboek een rekening is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="5773b-118">Use specific opening balance offsetting accounts, one set up for each subledger.</span></span> <span data-ttu-id="5773b-119">Stel de uitstellende rekeningen in zodat ze directe boekingen toestaan.</span><span class="sxs-lookup"><span data-stu-id="5773b-119">Set up the offsetting accounts to enable direct postings.</span></span>  
2.  <span data-ttu-id="5773b-120">Migreer open klantenposten.</span><span class="sxs-lookup"><span data-stu-id="5773b-120">Migrate open customer ledger entries.</span></span>  
3.  <span data-ttu-id="5773b-121">Migreer open artikelposten.</span><span class="sxs-lookup"><span data-stu-id="5773b-121">Migrate open item ledger entries.</span></span>  
4.  <span data-ttu-id="5773b-122">Migreer open vaste-activumposten.</span><span class="sxs-lookup"><span data-stu-id="5773b-122">Migrate open fixed asset entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5773b-123">Zie ook</span><span class="sxs-lookup"><span data-stu-id="5773b-123">See Also</span></span>  
[<span data-ttu-id="5773b-124">Een bedrijf met RapidStart Services instellen</span><span class="sxs-lookup"><span data-stu-id="5773b-124">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="5773b-125">Beheer</span><span class="sxs-lookup"><span data-stu-id="5773b-125">Administration</span></span>](admin-setup-and-administration.md)

