---
title: Vaste activa instellen| Microsoft Docs
description: Leren over de reeks taken die u moet uitvoeren om vaste activa in te stellen, zoals machines of gebouwen.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: 3e610461a78ec2a4cebb60350236e17fe3d7e9cf
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "816455"
---
# <a name="setting-up-fixed-assets"></a><span data-ttu-id="ca65b-103">Vaste activa instellen</span><span class="sxs-lookup"><span data-stu-id="ca65b-103">Setting Up Fixed Assets</span></span>
<span data-ttu-id="ca65b-104">Voordat u met vaste activa kunt werken, moet u enkele zaken definiëren:</span><span class="sxs-lookup"><span data-stu-id="ca65b-104">Before you can work with Fixed Assets, you need to define a few things:</span></span>  

* <span data-ttu-id="ca65b-105">Hoe u vaste activa verzekert, onderhoudt en afschrijft.</span><span class="sxs-lookup"><span data-stu-id="ca65b-105">How you insure, maintain, and depreciate fixed assets.</span></span>  
* <span data-ttu-id="ca65b-106">Hoe u kosten en andere waarden in het grootboek registreert.</span><span class="sxs-lookup"><span data-stu-id="ca65b-106">How you record costs and other values in the general ledger.</span></span>  

<span data-ttu-id="ca65b-107">De onderstaande tabel heeft koppelingen naar meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ca65b-107">The table below has links to more information.</span></span> <span data-ttu-id="ca65b-108">Als u deze zaken hebt ingesteld, kunt u verschillende activiteiten starten.</span><span class="sxs-lookup"><span data-stu-id="ca65b-108">After you set those things up, you can start various activities.</span></span> <span data-ttu-id="ca65b-109">Zie [Vaste activa](fa-manage.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ca65b-109">For more information, see [Fixed Assets](fa-manage.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="ca65b-110">U kunt transacties voor vaste activa registreren op de pagina **VA fin. dagboek** of **VA-dagboek**, afhankelijk van de vraag of de transacties zijn bedoeld voor financiële rapportage of intern beheer.</span><span class="sxs-lookup"><span data-stu-id="ca65b-110">You can record fixed asset transactions in the **Fixed Asset G/L Journal** or **Fixed Asset Journal** pages, depending on whether the transactions are for financial reporting or for internal management.</span></span> <span data-ttu-id="ca65b-111">In de Help voor vaste activa wordt alleen het gebruik van de pagina **Financieel dagboek voor vaste activa** beschreven.</span><span class="sxs-lookup"><span data-stu-id="ca65b-111">Help for Fixed Assets only describes how to use the **Fixed Asset G/L Journal** page.</span></span>  

<span data-ttu-id="ca65b-112">Als u een activiteit van een vast activum inschakelt in de sectie **Grootboekintegratie** op de pagina **Afschrijvingsboek**, wordt de pagina **Financieel dagboek voor vaste activa** gebruikt om transacties voor de activiteit te boeken.</span><span class="sxs-lookup"><span data-stu-id="ca65b-112">When you enable a fixed asset activity in the **G/L Integration** section on the **Depreciation Book Card** page, the **Fixed Asset G/L Journal** page is used to post transactions for the activity.</span></span>

<span data-ttu-id="ca65b-113">In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.</span><span class="sxs-lookup"><span data-stu-id="ca65b-113">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

| <span data-ttu-id="ca65b-114">Als u dit wilt doen</span><span class="sxs-lookup"><span data-stu-id="ca65b-114">To</span></span> | <span data-ttu-id="ca65b-115">Zie</span><span class="sxs-lookup"><span data-stu-id="ca65b-115">See</span></span> |
| --- | --- |
| <span data-ttu-id="ca65b-116">De standaardgrootboekrekeningen, de verdeelsleutels, de dagboeksjablonen en - batches instellen voor boeking van vaste activa en klassen en subklassen voor vaste activa instellen, zoals materiële en immateriële activa.</span><span class="sxs-lookup"><span data-stu-id="ca65b-116">Set up default G/L accounts, allocation keys, journal templates and batches for fixed asset posting, and set up fixed asset classes and subclasses, such as Tangible and Intangible.</span></span> |[<span data-ttu-id="ca65b-117">Algemene gegevens voor vaste activa instellen</span><span class="sxs-lookup"><span data-stu-id="ca65b-117">Set Up General Fixed Assets Information</span></span>](fa-how-setup-general.md) |
| <span data-ttu-id="ca65b-118">Afschrijvingsboeken maken, diverse afschrijvingsmethoden definiëren, integreren met het grootboek en duplicatie van posten in verschillende afschrijvingsboeken inschakelen.</span><span class="sxs-lookup"><span data-stu-id="ca65b-118">Create depreciation books, define various depreciation methods, integrate with the general ledger, and enable duplication of entries in several depreciation books.</span></span> |[<span data-ttu-id="ca65b-119">Afschrijving van vaste activa instellen</span><span class="sxs-lookup"><span data-stu-id="ca65b-119">Set Up Fixed Asset Depreciation</span></span>](fa-how-setup-depreciation.md) |
| <span data-ttu-id="ca65b-120">Verzekering van vaste activa inschakelen, algemene verzekeringsinformatie en een verzekeringskaart per polis instellen en dagboeken voorbereiden om verzekeringskosten te boeken.</span><span class="sxs-lookup"><span data-stu-id="ca65b-120">Enable insurance of fixed assets, set up general insurance information, an insurance card per policy, and prepare journals to post insurance costs.</span></span> |[<span data-ttu-id="ca65b-121">Verzekering van vaste activa instellen</span><span class="sxs-lookup"><span data-stu-id="ca65b-121">Set Up Fixed Asset Insurance</span></span>](fa-how-setup-insurance.md) |
| <span data-ttu-id="ca65b-122">Onderhoud van vaste activa inschakelen, algemene onderhoudsgegevens instellen, boekingsrekeningen voor onderhoud instellen en soorten onderhoudswerk definiëren.</span><span class="sxs-lookup"><span data-stu-id="ca65b-122">Enable maintenance of fixed assets, set up general maintenance information, set up maintenance posting accounts, and define types of maintenance work.</span></span> |[<span data-ttu-id="ca65b-123">Onderhoud van vaste activa instellen</span><span class="sxs-lookup"><span data-stu-id="ca65b-123">Set Up Fixed Asset Maintenance</span></span>](fa-how-setup-maintenance.md) |
| <span data-ttu-id="ca65b-124">Meer informatie over andere afschrijvingsmethoden voor vaste activa.</span><span class="sxs-lookup"><span data-stu-id="ca65b-124">Learn about different fixed asset depreciation methods.</span></span> |[<span data-ttu-id="ca65b-125">Afschrijvingsmethoden</span><span class="sxs-lookup"><span data-stu-id="ca65b-125">Depreciation Methods</span></span>](fa-depreciation-methods.md) |

## <a name="see-also"></a><span data-ttu-id="ca65b-126">Zie ook</span><span class="sxs-lookup"><span data-stu-id="ca65b-126">See Also</span></span>
[<span data-ttu-id="ca65b-127">Vast activum</span><span class="sxs-lookup"><span data-stu-id="ca65b-127">Fixed Assets</span></span>](fa-manage.md)  
[<span data-ttu-id="ca65b-128">Financiën</span><span class="sxs-lookup"><span data-stu-id="ca65b-128">Finance</span></span>](finance.md)  
[<span data-ttu-id="ca65b-129">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="ca65b-129">Getting Started</span></span>](product-get-started.md)  
<span data-ttu-id="ca65b-130">[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ca65b-130">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>
