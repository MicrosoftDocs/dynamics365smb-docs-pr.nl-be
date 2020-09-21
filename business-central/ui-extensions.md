---
title: Extensies installeren om Business Central aan te passen | Microsoft Docs
description: Meer informatie over het toevoegen van functionaliteit en het aanpassen van Business Central door extensies te installeren.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 08/12/2020
ms.author: edupont
ms.openlocfilehash: 2011728e8e036442418c6a2d8b51477b45b02d1e
ms.sourcegitcommit: 43284728c34b72ad1984a516273dc80e4cdc99ab
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/04/2020
ms.locfileid: "3765933"
---
# <a name="customizing-business-central-using-extensions"></a><span data-ttu-id="610d7-103">Business Central aanpassen met extensies</span><span class="sxs-lookup"><span data-stu-id="610d7-103">Customizing Business Central Using Extensions</span></span>

<span data-ttu-id="610d7-104">U kunt [!INCLUDE[d365fin](includes/d365fin_md.md)] wijzigen door extensies te installeren die bijvoorbeeld functionaliteit toevoegen, gedrag wijzigen of u toegang verlenen tot nieuwe online services.</span><span class="sxs-lookup"><span data-stu-id="610d7-104">You can change [!INCLUDE[d365fin](includes/d365fin_md.md)] by installing extensions that add functionality, changes behavior, or gives you access to new online services, for example.</span></span>

> [!NOTE]
> <span data-ttu-id="610d7-105">Als u extensies wilt installeren vanuit AppSource extensies per tenant wilt toevoegen, moet u de juiste machtigingen hebben.</span><span class="sxs-lookup"><span data-stu-id="610d7-105">To install extensions from AppSource or add per-tenant extensions, you must have the right permissions.</span></span> <span data-ttu-id="610d7-106">U moet lid zijn van de gebruikersgroep D365 EXTENSIEBEHEER of u moet beschikken over de machtigingenset D365 EXTENSIEBEHEER.</span><span class="sxs-lookup"><span data-stu-id="610d7-106">You must either be a member of the D365 EXTENSION MGMT user group or you must have the D365 EXTENSION MGMT permission set.</span></span> <span data-ttu-id="610d7-107">Als u een beheerder bent, kunt u gebruikersgroepen en machtigingen toewijzen aan andere gebruikers in uw bedrijf.</span><span class="sxs-lookup"><span data-stu-id="610d7-107">If you are an administrator, you can assign user groups and permissions to other users in your company.</span></span><br /><br />
<span data-ttu-id="610d7-108">Als u de functionaliteit van een extensie wilt gebruiken, zoals pagina's openen, rapporten uitvoeren, acties selecteren, enzovoort, moeten aan u de machtigingensets zijn toegewezen die als onderdeel van de extensie zijn geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="610d7-108">To use the functionality that is provided by an extension, such as opening pages, running reports, selecting actions, and so on, you must be assigned the permission sets that are installed as part of the extension.</span></span>

> [!IMPORTANT]  
> <span data-ttu-id="610d7-109">Het uploaden van extensies per huurder en de installatie van AppSource-extensies wordt niet ondersteund via de pagina **Extensiebeheer** voor lokale installaties.</span><span class="sxs-lookup"><span data-stu-id="610d7-109">The upload of per-tenant extensions and the installation of AppSource extensions is not supported through the **Extension Management** page for on-premise installations.</span></span>

<span data-ttu-id="610d7-110">Wanneer u [!INCLUDE[d365fin](includes/d365fin_md.md)] voor het eerst start, zijn bepaalde extensies al voor u geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="610d7-110">When you first launch [!INCLUDE[d365fin](includes/d365fin_md.md)], some extensions are already installed for you.</span></span> <span data-ttu-id="610d7-111">In de loop van de tijd zullen meer extensies beschikbaar voor u worden gemaakt en u kunt dan zelf bepalen of u de extensie wilt gebruiken of niet.</span><span class="sxs-lookup"><span data-stu-id="610d7-111">Over time, more extensions will be made available to you, and you can then choose if you want to use the extension or not.</span></span>

<span data-ttu-id="610d7-112">Zo verschaft Microsoft een extensie die integratie met PayPal Payments Standard biedt.</span><span class="sxs-lookup"><span data-stu-id="610d7-112">For example, Microsoft provides an extension that provides integration with PayPal Payments Standard.</span></span> <span data-ttu-id="610d7-113">Deze extensie is standaard geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="610d7-113">This extension is installed by default.</span></span>
<span data-ttu-id="610d7-114">Maar als er een andere extensie beschikbaar komt die integratie met een andere betalingsservice biedt, kunt u de nieuwe extensie installeren en vervolgens bepalen welke van de services moeten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="610d7-114">But if another extension is made available that offers integration with another payment service, you can install the new extension and then choose which of the two services to use.</span></span>  

<span data-ttu-id="610d7-115">U beheert de extensies op de pagina **Extensiebeheer**.</span><span class="sxs-lookup"><span data-stu-id="610d7-115">You manage the extensions on the **Extension Management** page.</span></span> <span data-ttu-id="610d7-116">U kunt tot deze pagina toegang krijgen via de startpagina.</span><span class="sxs-lookup"><span data-stu-id="610d7-116">You can access this page from Home.</span></span> <span data-ttu-id="610d7-117">Of kies het pictogram **Zoeken naar pagina of rapport** ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen") in de rechterbovenhoek, voer **Extensie** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="610d7-117">Alternatively, choose the **Search for Page or Report** icon ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") in the top right corner, enter **Extension**, and then choose the related link.</span></span> <span data-ttu-id="610d7-118">Zie [Extensies installeren en verwijderen](ui-extensions-install-uninstall.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="610d7-118">For more information, see [Installing and Uninstalling Extensions](ui-extensions-install-uninstall.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="610d7-119">Als u denkt u dat toegang tot een extensie zou moeten hebben maar de functionaliteit ervan niet vindt, kijk dan op de pagina **Extensiebeheer**. Als de extensie daar niet wordt vermeld, kunt u de extensie installeren zoals beschreven in het volgende gedeelte.</span><span class="sxs-lookup"><span data-stu-id="610d7-119">If you think you should have access to an extension but you cannot find its functionality, check the **Extension Management** page - if the extension is not listed there, you can install it as described in the following section.</span></span>  

> [!NOTE]  
> <span data-ttu-id="610d7-120">Nieuwe extensies zijn niet direct in AppSource beschikbaar nadat we een update aankondigen.</span><span class="sxs-lookup"><span data-stu-id="610d7-120">New extensions are not available in AppSource immediately after we announce an update.</span></span> <span data-ttu-id="610d7-121">U kunt de extensies in de gaten houden op [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).</span><span class="sxs-lookup"><span data-stu-id="610d7-121">You can keep an eye out for the extensions at  [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).</span></span>

## <a name="see-also"></a><span data-ttu-id="610d7-122">Zie ook</span><span class="sxs-lookup"><span data-stu-id="610d7-122">See Also</span></span>

[<span data-ttu-id="610d7-123">Dynamics 365 Business Central uitbreiden</span><span class="sxs-lookup"><span data-stu-id="610d7-123">Extending Dynamics 365 Business Central</span></span>](about-develop-extensions.md)  
[<span data-ttu-id="610d7-124">Extensies voor Business Central van andere providers</span><span class="sxs-lookup"><span data-stu-id="610d7-124">Business Central Extensions by Other Providers</span></span>](ui-extensions-other.md)  
[<span data-ttu-id="610d7-125">De Envestnet Yodlee Bank Feeds-service instellen</span><span class="sxs-lookup"><span data-stu-id="610d7-125">Set Up the Envestnet Yodlee Bank Feeds Service</span></span>](bank-how-setup-bank-statement-service.md)  
[<span data-ttu-id="610d7-126">Klantbetalingen inschakelen via PayPal</span><span class="sxs-lookup"><span data-stu-id="610d7-126">Enable Customer Payment Through PayPal</span></span>](sales-how-enable-payment-service-extensions.md)  
[<span data-ttu-id="610d7-127">Bedrijfsgegevens migreren uit andere financiële systemen</span><span class="sxs-lookup"><span data-stu-id="610d7-127">Migrating Business Data from Other Finance Systems</span></span>](across-import-data-configuration-packages.md)  
[<span data-ttu-id="610d7-128">De extensie GetAddress.io UK Postcode instellen</span><span class="sxs-lookup"><span data-stu-id="610d7-128">Setting Up the GetAddress.io UK Postal Code extension</span></span>](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
<span data-ttu-id="610d7-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)] Extensies door andere providers](ui-extensions-other.md)</span><span class="sxs-lookup"><span data-stu-id="610d7-129">[[!INCLUDE[d365fin](includes/d365fin_md.md)] Extensions by Other Providers](ui-extensions-other.md)</span></span>  
[<span data-ttu-id="610d7-130">Aan de slag</span><span class="sxs-lookup"><span data-stu-id="610d7-130">Getting Started</span></span>](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
