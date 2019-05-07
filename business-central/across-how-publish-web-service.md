---
title: Objecten openstellen als webservices | Microsoft Docs
description: Publiceer objecten als webservices om ze meteen beschikbaar te maken voor uw Business Central-oplossing.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: edupont
ms.openlocfilehash: 952f2b9dc301b6941d13b4c23ac55f83b781739f
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "922443"
---
# <a name="publish-a-web-service"></a><span data-ttu-id="dbe7e-103">Een webservice publiceren</span><span class="sxs-lookup"><span data-stu-id="dbe7e-103">Publish a Web Service</span></span>

<span data-ttu-id="dbe7e-104">Webservices zijn een lichtgewicht manier om toepassingsfunctionaliteit aan allerlei externe systemen en gebruikers beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-104">Web services are a lightweight way to make application functionality available to a variety of external systems and users.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)] <span data-ttu-id="dbe7e-105">bevat een aantal objecten die standaard als webservices worden opengesteld vanwege de integratie met andere Microsoft-services, maar u kunt ook andere webservices toevoegen.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-105">includes an number of objects that are exposed as web services by default due to integration with other Microsoft services, but you can also add other web services.</span></span>  

<span data-ttu-id="dbe7e-106">U kunt een webservice in de Windows-client of de webclient instellen.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-106">You can set up a web service in the Windows client or in the Web client.</span></span> <span data-ttu-id="dbe7e-107">U moet vervolgens de webservice publiceren zodat deze beschikbaar is voor service-aanvragen via het netwerk.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-107">You must then publish the web service so that it is available to service requests over the network.</span></span> <span data-ttu-id="dbe7e-108">Gebruikers kunnen controleren of webservices actief zijn door een browser te laten kijken naar de serverlocatie en een overzicht van de beschikbare services aan te vragen.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-108">Users can discover web services by pointing a browser at the server location and requesting a list of available services.</span></span> <span data-ttu-id="dbe7e-109">Wanneer u een webservice publiceert, is deze onmiddellijk beschikbaar via het netwerk voor geverifieerde gebruikers.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-109">When you publish a web service, it is immediately available over the network for authenticated users.</span></span> <span data-ttu-id="dbe7e-110">Alle bevoegde gebruikers hebben toegang tot metagegevens voor webservices, maar alleen gebruikers die beschikken over voldoende machtigingen hebben toegang tot de werkelijke gegevens.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-110">All authorized users can access metadata for web services, but only users who have sufficient permissions can access actual data.</span></span>

## <a name="creating-and-publishing-a-web-service"></a><span data-ttu-id="dbe7e-111">Een webservice maken en publiceren</span><span class="sxs-lookup"><span data-stu-id="dbe7e-111">Creating and Publishing a Web Service</span></span>  
<span data-ttu-id="dbe7e-112">In de volgende stappen wordt uitgelegd hoe u een webservice maakt en publiceert.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-112">The following steps explain how to create and publish a web service.</span></span>  

### <a name="to-create-and-publish-a-web-service"></a><span data-ttu-id="dbe7e-113">Een webservice maken en publiceren</span><span class="sxs-lookup"><span data-stu-id="dbe7e-113">To create and publish a web service</span></span>  

1. <span data-ttu-id="dbe7e-114">Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Webservices** in en kies vervolgens de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-114">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="dbe7e-115">Kies op de pagina **Webservices** de optie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-115">On the **Web Services** page, choose **New**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > <span data-ttu-id="dbe7e-116">**Codeunit** en **Pagina** zijn geldige typen voor SOAP-webservices.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-116">**Codeunit** and **Page** are valid types for SOAP web services.</span></span> <span data-ttu-id="dbe7e-117">**Pagina** en **Query** zijn geldige typen voor OData-webservices.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-117">**Page** and **Query** are valid types for OData web services.</span></span>  
    > <span data-ttu-id="dbe7e-118">Als de database meerdere bedrijven bevat, kunt u een specifieke object-id voor een van de bedrijven kiezen.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-118">Also, if the database contains multiple companies, you can choose an object ID that is specific to one of the companies.</span></span>  
    > <span data-ttu-id="dbe7e-119">De servicenaam is zichtbaar voor consumenten die uw webservice gebruiken en is de basis voor het identificeren en onderscheiden van webservices. Zorg dus dat de naam duidelijk is.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-119">Finally, the service name is visible to consumers of your web service and is the basis for identifying and distinguishing web services, so you should make the name meaningful.</span></span>

3. <span data-ttu-id="dbe7e-120">Schakel het selectievakje in de kolom **Gepubliceerd** in.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-120">Select the check box in the **Published** column.</span></span>  

<span data-ttu-id="dbe7e-121">Wanneer u de webservice publiceert, ziet u in de velden **OData-URL** en **SOAP-URL** de URL's die voor de webservice zijn gegenereerd.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-121">When you publish the web service, in the **OData URL** and **SOAP URL** fields, you can see the URLs that are generated for the web service.</span></span> <span data-ttu-id="dbe7e-122">U kunt de webservice direct controleren door de koppelingen in de velden **OData-URL** en **SOAP-URL** te kiezen.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-122">You can test the web service immediately by choosing the links in the **OData URL** and **SOAP URL** fields.</span></span> <span data-ttu-id="dbe7e-123">U kunt eventueel de waarde van het veld kopiëren en opslaan voor later gebruik.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-123">Optionally, you can copy the value of the field and save it for later use.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="dbe7e-124">Voor codeunits die als SOAP-webservice worden gepubliceerd, moeten de beschikbare methoden in de codeunit worden gemarkeerd als `[External]` in de code.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-124">For codeunits that are published as a SOAP web service, the methods exposed in the codeunit must be marked as `[External]` in the code.</span></span>

<span data-ttu-id="dbe7e-125">Wanneer u een webservice publiceert, is deze beschikbaar voor externe partijen.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-125">After you publish a web service, it is available to external parties.</span></span> <span data-ttu-id="dbe7e-126">U kunt de beschikbaarheid van de webservice verifiëren door een browser te gebruiken, of u kunt de koppeling in de velden **OData-URL** en **SOAP-URL** kiezen op de pagina **Webservices**.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-126">You can verify the availability of that web service by using a browser, or you can choose the link in the **OData URL** and **SOAP URL** fields on the **Web Services** page.</span></span> <span data-ttu-id="dbe7e-127">In de volgende procedure wordt beschreven hoe u de beschikbaarheid van de webservice kunt controleren voor later gebruik.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-127">The following procedure illustrates how you can verify the availability of the web service for later use.</span></span>  

### <a name="to-verify-the-availability-of-a-web-service"></a><span data-ttu-id="dbe7e-128">De beschikbaarheid van een webservice verifiëren</span><span class="sxs-lookup"><span data-stu-id="dbe7e-128">To verify the availability of a web service</span></span>  

1. <span data-ttu-id="dbe7e-129">Voer in de browser de relevante URL in.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-129">In your browser, enter the relevant URL.</span></span> <span data-ttu-id="dbe7e-130">De volgende tabel illustreert de soorten URL's die u kunt invullen voor verschillende soorten webservices.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-130">The following table illustrates the types of URLs that you can enter for different web service types.</span></span>  

    > [!div class="mx-tdBreakAll"]
    > |<span data-ttu-id="dbe7e-131">Soort</span><span class="sxs-lookup"><span data-stu-id="dbe7e-131">Type</span></span>|<span data-ttu-id="dbe7e-132">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="dbe7e-132">Syntax</span></span>|<span data-ttu-id="dbe7e-133">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="dbe7e-133">Example</span></span>|
    > |----------------|------|-------|
    > |<span data-ttu-id="dbe7e-134">SOAP</span><span class="sxs-lookup"><span data-stu-id="dbe7e-134">SOAP</span></span> |<span data-ttu-id="dbe7e-135">https://api.businesscentral.dynamics.com/*versie*/*tenant*/WS/*CompanyName*/*entiteit*/</span><span class="sxs-lookup"><span data-stu-id="dbe7e-135">https://api.businesscentral.dynamics.com/*version*/*tenant*/WS/*CompanyName*/*entity*/</span></span> |`https://api.businesscentral.dynamics.com/v1.0/a10b3ee6-d9a2-42fe-926f-946e23bb8ddd/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |<span data-ttu-id="dbe7e-136">OData V4</span><span class="sxs-lookup"><span data-stu-id="dbe7e-136">OData V4</span></span>|<span data-ttu-id="dbe7e-137">https://api.businesscentral.dynamics.com/*versie*/*tenant*/ODataV4/Company('*CompanyName*')/*entiteit*</span><span class="sxs-lookup"><span data-stu-id="dbe7e-137">https://api.businesscentral.dynamics.com/*version*/*tenant*/ODataV4/Company('*CompanyName*')/*entity*</span></span>|`https://api.businesscentral.dynamics.com/v1.0/a10b3ee6-d9a2-42fe-926f-946e23bb8ddd/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    <span data-ttu-id="dbe7e-138">De bedrijfsnaam is hoofdlettergevoelig.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-138">The company name is case-sensitive.</span></span>|

2. <span data-ttu-id="dbe7e-139">Controleer de informatie die verschijnt in de browser.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-139">Review the information that is displayed in the browser.</span></span> <span data-ttu-id="dbe7e-140">Controleer of u de naam ziet van de webservice die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-140">Verify that you can see the name of the web service that you have created.</span></span>  

<span data-ttu-id="dbe7e-141">Als u toegang hebt tot een webservice en gegevens wilt terugschrijven naar [!INCLUDE[d365fin](includes/d365fin_md.md)], moet u de bedrijfsnaam opgeven.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-141">When you access a web service, and you want to write data back to [!INCLUDE[d365fin](includes/d365fin_md.md)], you must specify the company name.</span></span> <span data-ttu-id="dbe7e-142">U kunt het bedrijf opgeven als onderdeel van URI zoals weergegeven in de volgende voorbeelden, of u kunt het bedrijf opgeven als onderdeel van de queryparameters.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-142">You can specify the company as part of the URI as shown in the examples, or you can specify the company as part of the query parameters.</span></span> <span data-ttu-id="dbe7e-143">De volgende URI's wijzen bijvoorbeeld naar dezelfde OData-webservice en zijn beide geldige URI's.</span><span class="sxs-lookup"><span data-stu-id="dbe7e-143">For example, the following URIs point to the same OData web service and are both valid URIs.</span></span>  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a><span data-ttu-id="dbe7e-144">Zie ook</span><span class="sxs-lookup"><span data-stu-id="dbe7e-144">See Also</span></span>

[<span data-ttu-id="dbe7e-145">Beheer</span><span class="sxs-lookup"><span data-stu-id="dbe7e-145">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="dbe7e-146">Business Central-webservices voor ontwikkelaars</span><span class="sxs-lookup"><span data-stu-id="dbe7e-146">Business Central Web Services for developers</span></span>](/dynamics365/business-central/dev-itpro/webservices/web-services)  
