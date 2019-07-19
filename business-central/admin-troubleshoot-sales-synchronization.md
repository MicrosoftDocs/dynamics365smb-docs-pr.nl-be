---
title: Problemen met synchronisatiefouten oplossen | Microsoft Docs
description: Geeft een leidraad voor het identificeren en oplossen van synchronisatiefouten.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/11/2019
ms.author: bholtorf
ms.openlocfilehash: bb6d0837f91240eb31abc7c02895cf2da420bf7d
ms.sourcegitcommit: 8fe694b7bbe7fc0456ed5a9e42291218d2251b05
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/04/2019
ms.locfileid: "1726802"
---
# <a name="troubleshooting-synchronization-errors"></a><span data-ttu-id="26d2b-103">Problemen met synchronisatiefouten oplossen</span><span class="sxs-lookup"><span data-stu-id="26d2b-103">Troubleshooting Synchronization Errors</span></span>
<span data-ttu-id="26d2b-104">Er zijn veel factoren betrokken bij de integratie van [!INCLUDE[d365fin](includes/d365fin_md.md)] met [!INCLUDE[crm_md](includes/crm_md.md)]en soms gaat het mis.</span><span class="sxs-lookup"><span data-stu-id="26d2b-104">There are lots of moving parts involved in integrating [!INCLUDE[d365fin](includes/d365fin_md.md)] with [!INCLUDE[crm_md](includes/crm_md.md)], and sometimes things go wrong.</span></span> <span data-ttu-id="26d2b-105">In dit onderwerp worden enkele van de veel voorkomende fouten beschreven en worden enkele tips gegeven voor het oplossen van deze fouten.</span><span class="sxs-lookup"><span data-stu-id="26d2b-105">This topic points out some of the typical errors that occur and gives some pointers for how to fix them.</span></span>

<span data-ttu-id="26d2b-106">Fouten komen vaak voor als gevolg van iets wat een gebruiker heeft gedaan met gekoppelde records of er is iets mis met de manier waarop de integratie is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="26d2b-106">Errors often occur either because of something that a user has done to coupled records or something is wrong with how the integration is set up.</span></span> <span data-ttu-id="26d2b-107">Fouten met betrekking tot gekoppelde records kunnen gebruikers zelf oplossen.</span><span class="sxs-lookup"><span data-stu-id="26d2b-107">For errors related to coupled records, users can resolve those themselves.</span></span> <span data-ttu-id="26d2b-108">Deze fouten worden veroorzaakt door acties zoals het verwijderen van een record in één, maar niet beide, zakelijke apps en vervolgens synchroniseren.</span><span class="sxs-lookup"><span data-stu-id="26d2b-108">These errors are caused by actions such as deleting a record in one, but not both, business apps and then synchronizing.</span></span> <span data-ttu-id="26d2b-109">Zie voor meer informatie [De status van een synchronisatie weergeven](admin-how-to-view-synchronization-status.md),</span><span class="sxs-lookup"><span data-stu-id="26d2b-109">For more information, see [View the Status of a Synchronization](admin-how-to-view-synchronization-status.md).</span></span>

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2097304]

<span data-ttu-id="26d2b-110">Fouten die gerelateerd zijn aan hoe de integratie is ingesteld, vereisen doorgaans de aandacht van een beheerder.</span><span class="sxs-lookup"><span data-stu-id="26d2b-110">Errors that are related to how the integration is set up typically require an administrator's attention.</span></span> <span data-ttu-id="26d2b-111">U kunt deze fouten bekijken op de pagina **Synchronisatiefouten bij integratie**.</span><span class="sxs-lookup"><span data-stu-id="26d2b-111">You can view these errors on the **Integration Synchronization Errors** page.</span></span> <span data-ttu-id="26d2b-112">Voorbeelden van enkele typische problemen zijn:</span><span class="sxs-lookup"><span data-stu-id="26d2b-112">Examples of some typical issues include:</span></span>  
  
* <span data-ttu-id="26d2b-113">De machtigingen en rollen die aan gebruikers zijn toegewezen, zijn niet correct.</span><span class="sxs-lookup"><span data-stu-id="26d2b-113">The permissions and roles assigned to users are not correct.</span></span>  
* <span data-ttu-id="26d2b-114">Het beheerdersaccount is opgegeven als de integratiegebruiker.</span><span class="sxs-lookup"><span data-stu-id="26d2b-114">The administrator account was specified as the integration user.</span></span>  
* <span data-ttu-id="26d2b-115">Het wachtwoord van de integratiegebruiker is ingesteld om een wijziging te vereisen wanneer de gebruiker zich aanmeldt.</span><span class="sxs-lookup"><span data-stu-id="26d2b-115">The integration user’s password is set to require a change when the user signs in.</span></span>  
* <span data-ttu-id="26d2b-116">De wisselkoersen voor valuta's zijn niet opgegeven in de ene of de andere app.</span><span class="sxs-lookup"><span data-stu-id="26d2b-116">The exchange rates for currencies are not specified in one or the other app.</span></span>  
  
<span data-ttu-id="26d2b-117">U moet de fouten handmatig oplossen, maar er zijn een paar manieren waarop de pagina u helpt.</span><span class="sxs-lookup"><span data-stu-id="26d2b-117">You must manually resolve the errors, but there are a few ways in which the page helps you.</span></span> <span data-ttu-id="26d2b-118">Voorbeeld:</span><span class="sxs-lookup"><span data-stu-id="26d2b-118">For example:</span></span>  

* <span data-ttu-id="26d2b-119">De velden **Bron** en **Bestemming** kunnen koppelingen bevatten naar de record waar de fout is gevonden.</span><span class="sxs-lookup"><span data-stu-id="26d2b-119">The **Source** and **Destination** fields may contain links to the record where the error was found.</span></span> <span data-ttu-id="26d2b-120">Klik op de koppeling om de record te openen en de fout te onderzoeken.</span><span class="sxs-lookup"><span data-stu-id="26d2b-120">Click the link to open the record and investigate the error.</span></span>  
* <span data-ttu-id="26d2b-121">De acties **Posten ouder dan 7 dagen verwijderen** en **Alle items verwijderen** schonen de lijst op.</span><span class="sxs-lookup"><span data-stu-id="26d2b-121">The **Delete Entries Older than 7 Days** and the **Delete All Entries** actions will clean up the list.</span></span> <span data-ttu-id="26d2b-122">Meestal gebruikt u deze acties nadat u de oorzaak van een fout hebt opgelost die van invloed is op veel records.</span><span class="sxs-lookup"><span data-stu-id="26d2b-122">Typically, you use these actions after you have resolved the cause of an error that affects many records.</span></span> <span data-ttu-id="26d2b-123">Wees echter voorzichtig.</span><span class="sxs-lookup"><span data-stu-id="26d2b-123">Use caution, however.</span></span> <span data-ttu-id="26d2b-124">Met deze acties kunnen fouten worden verwijderd die nog steeds relevant zijn.</span><span class="sxs-lookup"><span data-stu-id="26d2b-124">These actions might delete errors that are still relevant.</span></span>

## <a name="see-also"></a><span data-ttu-id="26d2b-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="26d2b-125">See Also</span></span>
<span data-ttu-id="26d2b-126">[Integreren met [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)</span><span class="sxs-lookup"><span data-stu-id="26d2b-126">[Integrating with [!INCLUDE[crm_md](includes/crm_md.md)]](admin-prepare-dynamics-365-for-sales-for-integration.md)</span></span>  
<span data-ttu-id="26d2b-127">[Gebruikersaccounts instellen voor integratie met [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)</span><span class="sxs-lookup"><span data-stu-id="26d2b-127">[Setting Up User Accounts for Integrating with [!INCLUDE[crm_md](includes/crm_md.md)]](admin-setting-up-integration-with-dynamics-sales.md)</span></span>  
<span data-ttu-id="26d2b-128">[Een verbinding instellen met [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)</span><span class="sxs-lookup"><span data-stu-id="26d2b-128">[Set Up a Connection to [!INCLUDE[crm_md](includes/crm_md.md)]](admin-how-to-set-up-a-dynamics-crm-connection.md)</span></span>  
[<span data-ttu-id="26d2b-129">Records handmatig koppelen en synchroniseren</span><span class="sxs-lookup"><span data-stu-id="26d2b-129">Couple and Synchronize Records Manually</span></span>](admin-how-to-couple-and-synchronize-records-manually.md)  
[<span data-ttu-id="26d2b-130">De status van een synchronisatie weergeven</span><span class="sxs-lookup"><span data-stu-id="26d2b-130">View the Status of a Synchronization</span></span>](admin-how-to-view-synchronization-status.md)  