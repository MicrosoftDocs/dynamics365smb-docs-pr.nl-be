---
title: Vaste activa instellen| Microsoft Docs
description: Leren over de reeks taken die u moet uitvoeren om vaste activa in te stellen, zoals machines of gebouwen.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 9dea8be0f5b0200f97082dc25dbaa2483ad6c735
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-fixed-assets"></a><span data-ttu-id="1ec4f-103">Vaste activa instellen</span><span class="sxs-lookup"><span data-stu-id="1ec4f-103">Setting Up Fixed Assets</span></span>
<span data-ttu-id="1ec4f-104">Voordat u met vaste activa kunt werken, moet u enkele zaken definiëren:</span><span class="sxs-lookup"><span data-stu-id="1ec4f-104">Before you can work with Fixed Assets, you need to define a few things:</span></span>  

* <span data-ttu-id="1ec4f-105">Hoe u vaste activa verzekert, onderhoudt en afschrijft.</span><span class="sxs-lookup"><span data-stu-id="1ec4f-105">How you insure, maintain, and depreciate fixed assets.</span></span>  
* <span data-ttu-id="1ec4f-106">Hoe u kosten en andere waarden in het grootboek registreert.</span><span class="sxs-lookup"><span data-stu-id="1ec4f-106">How you record costs and other values in the general ledger.</span></span>  

<span data-ttu-id="1ec4f-107">De onderstaande tabel heeft koppelingen naar meer informatie.</span><span class="sxs-lookup"><span data-stu-id="1ec4f-107">The table below has links to more information.</span></span> <span data-ttu-id="1ec4f-108">Als u deze zaken hebt ingesteld, kunt u verschillende activiteiten starten.</span><span class="sxs-lookup"><span data-stu-id="1ec4f-108">After you set those things up, you can start various activities.</span></span> <span data-ttu-id="1ec4f-109">Zie [Vaste activa](fa-manage.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="1ec4f-109">For more information, see [Fixed Assets](fa-manage.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="1ec4f-110">U kunt transacties voor vaste activa registreren in het venster **VA fin. dagboek** of **VA-dagboek**, afhankelijk van de vraag of de transacties zijn bedoeld voor financiële rapportage of intern beheer.</span><span class="sxs-lookup"><span data-stu-id="1ec4f-110">You can record fixed asset transactions in the **Fixed Asset G/L Journal** or **Fixed Asset Journal** windows, depending on whether the transactions are for financial reporting or for internal management.</span></span> <span data-ttu-id="1ec4f-111">In de Help voor vaste activa wordt alleen het gebruik van het venster **Financieel dagboek voor vaste activa** beschreven.</span><span class="sxs-lookup"><span data-stu-id="1ec4f-111">Help for Fixed Assets only describes how to use the **Fixed Asset G/L Journal** window.</span></span>  

<span data-ttu-id="1ec4f-112">Als u een activiteit van een vast activum inschakelt in de sectie **Grootboekintegratie** in het venster **Afschrijvingsboek**, wordt het venster **Financieel dagboek voor vaste activa** gebruikt om transacties voor de activiteit te boeken.</span><span class="sxs-lookup"><span data-stu-id="1ec4f-112">When you enable a fixed asset activity in the **G/L Integration** section in the **Depreciation Book Card** window, the **Fixed Asset G/L Journal** window is used to post transactions for the activity.</span></span>

> [!NOTE]  
>  <span data-ttu-id="1ec4f-113">Deze functionaliteit vereist dat de ervaring is ingesteld op **Suite**.</span><span class="sxs-lookup"><span data-stu-id="1ec4f-113">This functionality requires that the experience is set to **Suite**.</span></span> <span data-ttu-id="1ec4f-114">Zie [Uw Financials-ervaring aanpassen](ui-experiences.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="1ec4f-114">For more information, see [Customizing Your Financials Experience](ui-experiences.md).</span></span>  

<span data-ttu-id="1ec4f-115">In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.</span><span class="sxs-lookup"><span data-stu-id="1ec4f-115">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

| <span data-ttu-id="1ec4f-116">Als u dit wilt doen</span><span class="sxs-lookup"><span data-stu-id="1ec4f-116">To</span></span> | <span data-ttu-id="1ec4f-117">Zie</span><span class="sxs-lookup"><span data-stu-id="1ec4f-117">See</span></span> |
| --- | --- |
| <span data-ttu-id="1ec4f-118">De standaardgrootboekrekeningen, de verdeelsleutels, de dagboeksjablonen en - batches instellen voor boeking van vaste activa en klassen en subklassen voor vaste activa instellen, zoals materiële en immateriële activa.</span><span class="sxs-lookup"><span data-stu-id="1ec4f-118">Set up default G/L accounts, allocation keys, journal templates and batches for fixed asset posting, and set up fixed asset classes and subclasses, such as Tangible and Intangible.</span></span> |[<span data-ttu-id="1ec4f-119">Procedure: Algemene gegevens voor vaste activa instellen</span><span class="sxs-lookup"><span data-stu-id="1ec4f-119">How to: Set Up General Fixed Assets Information</span></span>](fa-how-setup-general.md) |
| <span data-ttu-id="1ec4f-120">Afschrijvingsboeken maken, diverse afschrijvingsmethoden definiëren, integreren met het grootboek en duplicatie van posten in verschillende afschrijvingsboeken inschakelen.</span><span class="sxs-lookup"><span data-stu-id="1ec4f-120">Create depreciation books, define various depreciation methods, integrate with the general ledger, and enable duplication of entries in several depreciation books.</span></span> |[<span data-ttu-id="1ec4f-121">Procedure: Afschrijving van vaste activa instellen</span><span class="sxs-lookup"><span data-stu-id="1ec4f-121">How to: Set Up Fixed Asset Depreciation</span></span>](fa-how-setup-depreciation.md) |
| <span data-ttu-id="1ec4f-122">Verzekering van vaste activa inschakelen, algemene verzekeringsinformatie en een verzekeringskaart per polis instellen en dagboeken voorbereiden om verzekeringskosten te boeken.</span><span class="sxs-lookup"><span data-stu-id="1ec4f-122">Enable insurance of fixed assets, set up general insurance information, an insurance card per policy, and prepare journals to post insurance costs.</span></span> |[<span data-ttu-id="1ec4f-123">Procedure: Verzekering voor vaste activa instellen</span><span class="sxs-lookup"><span data-stu-id="1ec4f-123">How to: Set Up Fixed Asset Insurance</span></span>](fa-how-setup-insurance.md) |
| <span data-ttu-id="1ec4f-124">Onderhoud van vaste activa inschakelen, algemene onderhoudsgegevens instellen, boekingsrekeningen voor onderhoud instellen en soorten onderhoudswerk definiëren.</span><span class="sxs-lookup"><span data-stu-id="1ec4f-124">Enable maintenance of fixed assets, set up general maintenance information, set up maintenance posting accounts, and define types of maintenance work.</span></span> |[<span data-ttu-id="1ec4f-125">Procedure: Onderhoud van vaste activa instellen</span><span class="sxs-lookup"><span data-stu-id="1ec4f-125">How to: Set Up Fixed Asset Maintenance</span></span>](fa-how-setup-maintenance.md) |
| <span data-ttu-id="1ec4f-126">Meer informatie over andere afschrijvingsmethoden voor vaste activa.</span><span class="sxs-lookup"><span data-stu-id="1ec4f-126">Learn about different fixed asset depreciation methods.</span></span> |[<span data-ttu-id="1ec4f-127">Afschrijvingsmethoden</span><span class="sxs-lookup"><span data-stu-id="1ec4f-127">Depreciation Methods</span></span>](fa-depreciation-methods.md) |

## <a name="see-also"></a><span data-ttu-id="1ec4f-128">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1ec4f-128">See Also</span></span>
[<span data-ttu-id="1ec4f-129">Vaste activa</span><span class="sxs-lookup"><span data-stu-id="1ec4f-129">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="1ec4f-130">Financiën</span><span class="sxs-lookup"><span data-stu-id="1ec4f-130">Finance</span></span>](finance.md)  
<span data-ttu-id="1ec4f-131">[Welkom bij [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="1ec4f-131">[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span></span>  
<span data-ttu-id="1ec4f-132">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1ec4f-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

