---
title: Tips en trucs - RapidStart Services | Microsoft Docs
description: Wanneer u bedrijven configureert met RapidStart Services, zijn er enkele tips en trucs die u kunt gebruiken om uw implementatie vlot te laten verlopen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: ef836fce45dc2347f716d298207708caa54689f0
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3186584"
---
# <a name="tips-and-tricks-rapidstart-services"></a><span data-ttu-id="cb63d-103">Tips en trucs: RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="cb63d-103">Tips and Tricks: RapidStart Services</span></span>
<span data-ttu-id="cb63d-104">Wanneer u bedrijven configureert met RapidStart Services, zijn er enkele tips en trucs die u kunt gebruiken om uw implementatie vlot te laten verlopen.</span><span class="sxs-lookup"><span data-stu-id="cb63d-104">When you configure companies using RapidStart Services, there are some tips and tricks that you can take advantage of to help your implementation go smoothly.</span></span>  

## <a name="take-advantage-of-configuration-templates"></a><span data-ttu-id="cb63d-105">Gebruikmaken van configuratiesjablonen</span><span class="sxs-lookup"><span data-stu-id="cb63d-105">Take advantage of configuration templates</span></span>  
<span data-ttu-id="cb63d-106">Configuratiesjablonen kunnen u helpen uw implementatie te stroomlijnen.</span><span class="sxs-lookup"><span data-stu-id="cb63d-106">Configuration templates can help you streamline your implementation process.</span></span> <span data-ttu-id="cb63d-107">U kunt via deze sjablonen vergelijkbare klanten opnemen in segmenten en een implementatieprotocol ontwikkelen die alle klanten in een segment op een vergelijkbare wijze behandelt.</span><span class="sxs-lookup"><span data-stu-id="cb63d-107">By using them, you can include similar customers in segments and then develop an implementation protocol that treats all customers in a segment in a similar manner.</span></span> <span data-ttu-id="cb63d-108">Op die manier kunt u meteen een preconfiguratie toepassen op elk segment en doorgaan met een snelle implementatie.</span><span class="sxs-lookup"><span data-stu-id="cb63d-108">In that way, you can apply a level of preconfiguration to each segment and continue with a rapid implementation.</span></span>  

## <a name="configuration-questionnaires"></a><span data-ttu-id="cb63d-109">Configuratievragenlijsten</span><span class="sxs-lookup"><span data-stu-id="cb63d-109">Configuration questionnaires</span></span>  
<span data-ttu-id="cb63d-110">Om het invullen van een configuratievragenlijst sneller te laten verlopen, kunt u standaardantwoorden definiëren om aanbevolen procedures aan te geven.</span><span class="sxs-lookup"><span data-stu-id="cb63d-110">To aid the process of filling out a configuration questionnaire, consider defining default answers to indicate best practices.</span></span>  

## <a name="batch-creation-of-journal-lines"></a><span data-ttu-id="cb63d-111">Dagboekregels in batch aanmaken</span><span class="sxs-lookup"><span data-stu-id="cb63d-111">Batch creation of journal lines</span></span>  
<span data-ttu-id="cb63d-112">Het is raadzaam dat u de hulpprogramma's voor gegevensmigratie gebruikt voor het migreren van dagboekposten.</span><span class="sxs-lookup"><span data-stu-id="cb63d-112">We recommend that you use the data migration tools provided to migrate journal entries.</span></span> <span data-ttu-id="cb63d-113">Als u een batchtaak gebruikt om dagboekregels te maken, heeft deze een beperkt bereik en maakt deze enkel pre-standaardvelden in een dagboek.</span><span class="sxs-lookup"><span data-stu-id="cb63d-113">Otherwise, if you use a batch job to create journal lines, that has a limited scope and only generates pre-default fields into a journal.</span></span> <span data-ttu-id="cb63d-114">De rest van het dagboek moet vervolgens handmatig worden voltooid.</span><span class="sxs-lookup"><span data-stu-id="cb63d-114">The rest of the journal then has to be completed manually.</span></span>  

## <a name="migrating-transactions"></a><span data-ttu-id="cb63d-115">Transacties migreren</span><span class="sxs-lookup"><span data-stu-id="cb63d-115">Migrating transactions</span></span>  
<span data-ttu-id="cb63d-116">Het is raadzaam om beginsaldi in de volgende volgorde te migreren.</span><span class="sxs-lookup"><span data-stu-id="cb63d-116">We recommend that you migrate opening balances in the following order.</span></span> <!--Be aware that you cannot insert ledger entries directly. Instead you must use journals to post the journal lines--> 

1.  <span data-ttu-id="cb63d-117">Migreer beginsaldi uit het grootboek zonder de subgrootboeken van de grootboekrekening te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="cb63d-117">Migrate general ledger opening balances without using the general ledger account subledgers.</span></span> <span data-ttu-id="cb63d-118">Gebruik specifieke uitstellende rekeningen voor beginsaldi, waarbij voor elk subgrootboek een rekening is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="cb63d-118">Use specific opening balance offsetting accounts, one set up for each subledger.</span></span> <span data-ttu-id="cb63d-119">Stel de uitstellende rekeningen in zodat ze directe boekingen toestaan.</span><span class="sxs-lookup"><span data-stu-id="cb63d-119">Set up the offsetting accounts to enable direct postings.</span></span>  
2.  <span data-ttu-id="cb63d-120">Migreer open klantenposten.</span><span class="sxs-lookup"><span data-stu-id="cb63d-120">Migrate open customer ledger entries.</span></span>  <!--work on these-->
3.  <span data-ttu-id="cb63d-121">Migreer open artikelposten.</span><span class="sxs-lookup"><span data-stu-id="cb63d-121">Migrate open item ledger entries.</span></span>  
4.  <span data-ttu-id="cb63d-122">Migreer open vaste-activumposten.</span><span class="sxs-lookup"><span data-stu-id="cb63d-122">Migrate open fixed asset entries.</span></span>  

## <a name="see-also"></a><span data-ttu-id="cb63d-123">Zie ook</span><span class="sxs-lookup"><span data-stu-id="cb63d-123">See Also</span></span>  
[<span data-ttu-id="cb63d-124">Een bedrijf instellen met RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="cb63d-124">Setting Up a Company With RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="cb63d-125">Beheer</span><span class="sxs-lookup"><span data-stu-id="cb63d-125">Administration</span></span>](admin-setup-and-administration.md)
