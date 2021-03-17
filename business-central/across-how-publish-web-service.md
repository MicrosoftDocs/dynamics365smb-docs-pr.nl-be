---
title: Objecten openstellen als webservices
description: Publiceer objecten als webservices om ze meteen beschikbaar te maken voor uw Business Central-oplossing.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 10/08/2020
ms.author: edupont
ms.openlocfilehash: 94a4752abc133e59169209b94a145d2195ce783d
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5384636"
---
# <a name="publish-a-web-service"></a><span data-ttu-id="1a873-103">Een webservice publiceren</span><span class="sxs-lookup"><span data-stu-id="1a873-103">Publish a Web Service</span></span>

<span data-ttu-id="1a873-104">Webservices zijn een lichtgewicht manier om toepassingsfunctionaliteit aan allerlei soorten externe systemen en gebruikers beschikbaar te maken.</span><span class="sxs-lookup"><span data-stu-id="1a873-104">Web services are a lightweight way to make application functionality available to different kinds of external systems and users.</span></span> <span data-ttu-id="1a873-105">Standaard stelt [!INCLUDE[prod_short](includes/prod_short.md)] een aantal objecten bloot als webservices voor een betere integratie met andere Microsoft-services.</span><span class="sxs-lookup"><span data-stu-id="1a873-105">By default, [!INCLUDE[prod_short](includes/prod_short.md)] exposes a number of objects as web services for better integration with other Microsoft services.</span></span> <span data-ttu-id="1a873-106">U kunt andere webservices toevoegen als uw bedrijf dit vereist.</span><span class="sxs-lookup"><span data-stu-id="1a873-106">You can add other web services as your business requires.</span></span>  

<span data-ttu-id="1a873-107">Stel een webservice in [!INCLUDE[prod_short](includes/prod_short.md)] in en publiceer vervolgens de webservice zodat deze beschikbaar is voor geverifieerde gebruikers.</span><span class="sxs-lookup"><span data-stu-id="1a873-107">Set up a web service in [!INCLUDE[prod_short](includes/prod_short.md)], and then publish the web service so that it is available to authenticated users.</span></span> <span data-ttu-id="1a873-108">Alle bevoegde gebruikers hebben toegang tot metagegevens voor webservices, maar alleen gebruikers die beschikken over voldoende machtigingen hebben toegang tot de werkelijke gegevens.</span><span class="sxs-lookup"><span data-stu-id="1a873-108">All authorized users can access metadata for web services, but only users who have sufficient permissions can access actual data.</span></span>  

## <a name="creating-and-publishing-a-web-service"></a><span data-ttu-id="1a873-109">Een webservice maken en publiceren</span><span class="sxs-lookup"><span data-stu-id="1a873-109">Creating and Publishing a Web Service</span></span>

<span data-ttu-id="1a873-110">In de volgende stappen wordt uitgelegd hoe u een webservice maakt en publiceert.</span><span class="sxs-lookup"><span data-stu-id="1a873-110">The following steps explain how to create and publish a web service.</span></span>  

### <a name="to-create-and-publish-a-web-service"></a><span data-ttu-id="1a873-111">Een webservice maken en publiceren</span><span class="sxs-lookup"><span data-stu-id="1a873-111">To create and publish a web service</span></span>  

1. <span data-ttu-id="1a873-112">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Webservices** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="1a873-112">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Web Services**, and then choose the related link.</span></span>  
2. <span data-ttu-id="1a873-113">Kies op de pagina **Webservices** de optie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="1a873-113">On the **Web Services** page, choose **New**.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    > [!NOTE]  
    > <span data-ttu-id="1a873-114">**Codeunit** en **Pagina** zijn geldige typen voor SOAP-webservices.</span><span class="sxs-lookup"><span data-stu-id="1a873-114">**Codeunit** and **Page** are valid types for SOAP web services.</span></span> <span data-ttu-id="1a873-115">**Pagina** en **Query** zijn geldige typen voor OData-webservices.</span><span class="sxs-lookup"><span data-stu-id="1a873-115">**Page** and **Query** are valid types for OData web services.</span></span> <span data-ttu-id="1a873-116">Vanaf versie 16.3, is **Codeunit** ook een geldig type voor OData v4-webservices, maar dan wordt er geen URL weergegeven in de gebruikersinterface.</span><span class="sxs-lookup"><span data-stu-id="1a873-116">Starting with version 16.3, **Codeunit** is also a valid type for OData v4 web services, but then no URL is shown in the user interface.</span></span> <span data-ttu-id="1a873-117">Als de database meerdere bedrijven bevat, kunt u een specifieke object-id voor een van de bedrijven kiezen.</span><span class="sxs-lookup"><span data-stu-id="1a873-117">Also, if the database contains multiple companies, you can choose an object ID that is specific to one of the companies.</span></span>  
    > <span data-ttu-id="1a873-118">De servicenaam is zichtbaar voor consumenten die uw webservice gebruiken en is de basis voor het identificeren en onderscheiden van webservices. Zorg dus dat de naam duidelijk is.</span><span class="sxs-lookup"><span data-stu-id="1a873-118">Finally, the service name is visible to consumers of your web service and is the basis for identifying and distinguishing web services, so you should make the name meaningful.</span></span>

3. <span data-ttu-id="1a873-119">Schakel het selectievakje in de kolom **Gepubliceerd** in.</span><span class="sxs-lookup"><span data-stu-id="1a873-119">Select the check box in the **Published** column.</span></span>  

<span data-ttu-id="1a873-120">Wanneer u de webservice publiceert, bevatten de velden **OData-URL** en **SOAP-URL** de nieuwe URL's.</span><span class="sxs-lookup"><span data-stu-id="1a873-120">When you publish the web service, the **OData URL** and **SOAP URL** fields show the new URLs.</span></span> <span data-ttu-id="1a873-121">Voor codeunits die worden weergegeven als ongebonden OData v4-acties, worden de URL-velden echter niet weergegeven.</span><span class="sxs-lookup"><span data-stu-id="1a873-121">However, for codeunits that are exposed as OData v4 unbound actions, the URL fields are not shown.</span></span>  

<span data-ttu-id="1a873-122">U kunt de webservice direct controleren door de koppelingen in de velden **OData-URL** en **SOAP-URL** te kiezen.</span><span class="sxs-lookup"><span data-stu-id="1a873-122">You can test the web service immediately by choosing the links in the **OData URL** and **SOAP URL** fields.</span></span> <span data-ttu-id="1a873-123">U kunt eventueel de waarde van het veld kopiëren en opslaan voor later gebruik.</span><span class="sxs-lookup"><span data-stu-id="1a873-123">Optionally, copy the value of the field and save it for later use.</span></span> <span data-ttu-id="1a873-124">Om codeunits te testen die worden weergegeven als ongebonden OData v4-acties, volgt u de instructies in de sectie [Beschikbaarheid van webservice verifiëren](/dynamics365/business-central/dev-itpro/developer/devenv-creating-and-interacting-with-odatav4-unbound-action#verifying-web-service-availability) in de ontwikkelaarscontent.</span><span class="sxs-lookup"><span data-stu-id="1a873-124">To test codeunits that are exposed as OData v4 unbound actions, follow the instructions in the [Verifying web service availability](/dynamics365/business-central/dev-itpro/developer/devenv-creating-and-interacting-with-odatav4-unbound-action#verifying-web-service-availability) section in the developer content.</span></span>

> [!NOTE]
> <span data-ttu-id="1a873-125">Als de objecten die u beschikbaar maakt als webservices, niet toegankelijk mogen zijn vanuit [!INCLUDE[prod_short](includes/prod_short.md)] online, moet u de methoden die in de code beschikbaar worden gemaakt, markeren als `[Scope('OnPrem')]`.</span><span class="sxs-lookup"><span data-stu-id="1a873-125">If the objects that you expose as web services must not be accessible from [!INCLUDE[prod_short](includes/prod_short.md)] online, you must mark the methods exposed in the code as `[Scope('OnPrem')]`.</span></span> <span data-ttu-id="1a873-126">Zie voor meer informatie [Bereikkenmerk](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).</span><span class="sxs-lookup"><span data-stu-id="1a873-126">For more information, see [Scope Attribute](/dynamics365/business-central/dev-itpro/developer/methods/devenv-scope-attribute).</span></span>

<span data-ttu-id="1a873-127">Wanneer u een webservice publiceert, is deze beschikbaar voor externe partijen.</span><span class="sxs-lookup"><span data-stu-id="1a873-127">After you publish a web service, it is available to external parties.</span></span> <span data-ttu-id="1a873-128">U kunt de beschikbaarheid van die webservice verifiëren door een browser te gebruiken of u kunt de koppeling in de velden **OData-URL** en **SOAP-URL** kiezen op de pagina **Webservices**.</span><span class="sxs-lookup"><span data-stu-id="1a873-128">You can verify the availability of that web service by using a browser, or choose the link in the **OData URL** and **SOAP URL** fields on the **Web Services** page.</span></span> <span data-ttu-id="1a873-129">In de volgende procedure wordt beschreven hoe u de beschikbaarheid van de webservice kunt controleren voor later gebruik.</span><span class="sxs-lookup"><span data-stu-id="1a873-129">The following procedure illustrates how you can verify the availability of the web service for later use.</span></span>  

### <a name="to-verify-the-availability-of-a-web-service"></a><span data-ttu-id="1a873-130">De beschikbaarheid van een webservice verifiëren</span><span class="sxs-lookup"><span data-stu-id="1a873-130">To verify the availability of a web service</span></span>  

1. <span data-ttu-id="1a873-131">Voer in de browser de relevante URL in.</span><span class="sxs-lookup"><span data-stu-id="1a873-131">In your browser, enter the relevant URL.</span></span> <span data-ttu-id="1a873-132">De volgende tabel illustreert de soorten URL's die u kunt invullen voor verschillende soorten webservices.</span><span class="sxs-lookup"><span data-stu-id="1a873-132">The following table illustrates the types of URLs that you can enter for different web service types.</span></span>  

    > [!div class="mx-tdBreakAll"]
    > |<span data-ttu-id="1a873-133">Soort</span><span class="sxs-lookup"><span data-stu-id="1a873-133">Type</span></span>|<span data-ttu-id="1a873-134">Syntaxis</span><span class="sxs-lookup"><span data-stu-id="1a873-134">Syntax</span></span>|<span data-ttu-id="1a873-135">Voorbeeld</span><span class="sxs-lookup"><span data-stu-id="1a873-135">Example</span></span>|
    > |----------------|------|-------|
    > |<span data-ttu-id="1a873-136">SOAP</span><span class="sxs-lookup"><span data-stu-id="1a873-136">SOAP</span></span>|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/WS/*CompanyName*/*entity*/` |`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/WS/CRONUS%20USA%2C%20Inc./Page/InvoiceDocument`|
    > |<span data-ttu-id="1a873-137">OData V4</span><span class="sxs-lookup"><span data-stu-id="1a873-137">OData V4</span></span>|`https://api.businesscentral.dynamics.com/*version*/*tenant*/Production/ODataV4/Company('*CompanyName*')/*entity*`|`https://api.businesscentral.dynamics.com/v2.0/7acc9d3d-d354-4616-8bbd-c4fc9f2b15b3/Production/ODataV4/Company('CRONUS%20USA%2C%20Inc.')/InvoiceDocument`<br/>    <span data-ttu-id="1a873-138">De bedrijfsnaam is hoofdlettergevoelig.</span><span class="sxs-lookup"><span data-stu-id="1a873-138">The company name is case-sensitive.</span></span>|

2. <span data-ttu-id="1a873-139">Controleer de informatie die verschijnt in de browser.</span><span class="sxs-lookup"><span data-stu-id="1a873-139">Review the information that is displayed in the browser.</span></span> <span data-ttu-id="1a873-140">Controleer of u de naam ziet van de webservice die u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="1a873-140">Verify that you can see the name of the web service that you have created.</span></span>  

<span data-ttu-id="1a873-141">Als u toegang hebt tot een webservice en gegevens wilt terugschrijven naar [!INCLUDE[prod_short](includes/prod_short.md)], moet u de bedrijfsnaam opgeven.</span><span class="sxs-lookup"><span data-stu-id="1a873-141">When you access a web service, and you want to write data back to [!INCLUDE[prod_short](includes/prod_short.md)], you must specify the company name.</span></span> <span data-ttu-id="1a873-142">U kunt het bedrijf opgeven als onderdeel van de URI zoals weergegeven in de volgende voorbeelden, of u kunt het bedrijf opgeven als onderdeel van de queryparameters.</span><span class="sxs-lookup"><span data-stu-id="1a873-142">You can specify the company as part of the URI as shown in the examples; alternatively, specify the company as part of the query parameters.</span></span> <span data-ttu-id="1a873-143">De volgende URI's wijzen bijvoorbeeld naar dezelfde OData-webservice en zijn beide geldige URI's.</span><span class="sxs-lookup"><span data-stu-id="1a873-143">For example, the following URIs point to the same OData web service and are both valid URIs.</span></span>  

```
https://api.businesscentral.dynamics.com/v1.0/OData/Company('CRONUS International Ltd.')/Customer  
```

```
https://api.businesscentral.dynamics.com/v1.0/OData/Customer?company='CRONUS International Ltd.'  
```

## <a name="see-also"></a><span data-ttu-id="1a873-144">Zie ook</span><span class="sxs-lookup"><span data-stu-id="1a873-144">See Also</span></span>

[<span data-ttu-id="1a873-145">Beheer</span><span class="sxs-lookup"><span data-stu-id="1a873-145">Administration</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="1a873-146">Business Central-webservices voor ontwikkelaars</span><span class="sxs-lookup"><span data-stu-id="1a873-146">Business Central Web Services for developers</span></span>](/dynamics365/business-central/dev-itpro/webservices/web-services)  
[<span data-ttu-id="1a873-147">OData-aanvraaglimieten</span><span class="sxs-lookup"><span data-stu-id="1a873-147">OData request limits</span></span>](/dynamics365/business-central/dev-itpro/administration/operational-limits-online#ODataServices)  


[!INCLUDE[footer-include](includes/footer-banner.md)]