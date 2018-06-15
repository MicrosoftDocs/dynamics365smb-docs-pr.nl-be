---
title: API-sjablonen configureren | Microsoft Docs
description: De stappen beschrijven die u moet doorlopen om API-sjablonen te configureren voor Dynamics 365 Business Central.
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: API templates, configuring templates
ms.date: 05/16/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 1695a6950dabc1b2f0a2f85ad9e0c565012c92e1
ms.contentlocale: nl-be
ms.lasthandoff: 05/17/2018

---

# <a name="configuring-api-templates"></a><span data-ttu-id="c2c9a-103">API-sjablonen configureren</span><span class="sxs-lookup"><span data-stu-id="c2c9a-103">Configuring API Templates</span></span>
<span data-ttu-id="c2c9a-104">De API-bibliotheek voor [!INCLUDE[d365fin_md](includes/d365fin_md.md)] biedt een vereenvoudigde weergave van de onderliggende entiteiten.</span><span class="sxs-lookup"><span data-stu-id="c2c9a-104">The API library for [!INCLUDE[d365fin_md](includes/d365fin_md.md)] provides a simplified representation of the underlying entities.</span></span> <span data-ttu-id="c2c9a-105">Niet alle eigenschappen in de toepassing zijn beschikbaar via de bijbehorende API.</span><span class="sxs-lookup"><span data-stu-id="c2c9a-105">All the properties in the application are not exposed through the associated API.</span></span> <span data-ttu-id="c2c9a-106">Met het venster **API-instelling** kunt u sjablonen definiëren die worden gebruikt om lege eigenschappen te vullen van een entiteit wanneer u een POST-actie maakt met behulp van de API.</span><span class="sxs-lookup"><span data-stu-id="c2c9a-106">The **API Setup** window allows you to define templates that are used to populate empty properties on an entity when you create a POST action through the API.</span></span> 

<span data-ttu-id="c2c9a-107">Als bijvoorbeeld een configuratiesjabloon voor de artikelentiteit wordt gedefinieerd, wanneer een nieuwe artikelrecord wordt gemaakt met de artikelen-API, worden eigenschappen van het nieuwe artikel die niet zijn gedefinieerd in de API-aanroep, gevuld vanuit de geselecteerde sjabloon.</span><span class="sxs-lookup"><span data-stu-id="c2c9a-107">For example, if a configuration template is defined for the item entity, when a new item record is created through the items API, any properties for the new item that are not defined in the API call will be populated from the selected template.</span></span> <span data-ttu-id="c2c9a-108">Als met de API bijvoorbeeld geen waarde wordt gedefinieerd voor het veld **Productieboekingsgroep**, maar een waarde is gedefinieerd in de geselecteerde sjabloon, wordt de boekingsgroepswaarde die in de sjabloon is gedefinieerd, toegepast op het nieuwe artikel.</span><span class="sxs-lookup"><span data-stu-id="c2c9a-108">If, for example, no value is defined for the **Gen. Prod. Posting Group** field through the API, but a value is defined in the selected template, then the posting group value defined in the template will be applied to the new item.</span></span> 

## <a name="setting-up-the-entity-template"></a><span data-ttu-id="c2c9a-109">De entiteitsjabloon instellen</span><span class="sxs-lookup"><span data-stu-id="c2c9a-109">Setting up the Entity Template</span></span>
<span data-ttu-id="c2c9a-110">Als u sjablonen wilt gebruiken met de API-bibliotheek, moet u eerst eigenschappen voor de sjablonen instellen en definiëren.</span><span class="sxs-lookup"><span data-stu-id="c2c9a-110">To use templates with the API library, you must first set up and define properties for the templates.</span></span> <span data-ttu-id="c2c9a-111">U kunt deze sjablonen instellen in het venster **Configuratiesjablonen**.</span><span class="sxs-lookup"><span data-stu-id="c2c9a-111">You can set up these templates in the **Configuration Templates** window.</span></span> <span data-ttu-id="c2c9a-112">Zie voor meer informatie [Klantgegevens migreren voorbereiden](admin-use-templates-to-prepare-customer-data-for-migration.md).</span><span class="sxs-lookup"><span data-stu-id="c2c9a-112">For more information, see [Prepare to Migrate Customer Data](admin-use-templates-to-prepare-customer-data-for-migration.md).</span></span> 

## <a name="assign-the-template-to-an-api"></a><span data-ttu-id="c2c9a-113">De sjabloon toewijzen aan een API</span><span class="sxs-lookup"><span data-stu-id="c2c9a-113">Assign the template to an API</span></span>

<span data-ttu-id="c2c9a-114">Als u een sjabloon wilt toewijzen aan een API, moet u de volgende stappen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="c2c9a-114">To assign a template to an API, you must go through the following steps.</span></span>

1. <span data-ttu-id="c2c9a-115">Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **API-instelling** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="c2c9a-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **API Setup**, and choose the related link.</span></span>
2. <span data-ttu-id="c2c9a-116">Kies **Nieuw** en kies de waarde **Volgorde** voor de record.</span><span class="sxs-lookup"><span data-stu-id="c2c9a-116">Choose **New**, and then choose the **Order** value for the record.</span></span>  
<span data-ttu-id="c2c9a-117">Als er meer dan één sjabloon is geselecteerd voor een API (Pagina-id), worden de sjablonen toegepast in de volgorde die is gedefinieerd in de kolom **Volgorde**.</span><span class="sxs-lookup"><span data-stu-id="c2c9a-117">If there is more than one template selected for an API (Page ID), the templates are applied in the order defined in the **Order** column.</span></span>   
<span data-ttu-id="c2c9a-118">Wanneer elke sjabloon wordt toegepast, worden veldwaarden die in de sjabloon zijn gedefinieerd, alleen toegepast op velden waarvoor nog geen waarde is gedefinieerd, hetzij expliciet in de sjabloon, hetzij in een eerder toegepaste sjabloon in de volgorde.</span><span class="sxs-lookup"><span data-stu-id="c2c9a-118">When each template is applied, field values defined in the template are only applied to fields that have not already had a value defined, either explicitly in the API, or in a previously applied template in the order.</span></span> 
3. <span data-ttu-id="c2c9a-119">Selecteer een waarde voor **Pagina-id**.</span><span class="sxs-lookup"><span data-stu-id="c2c9a-119">Select a **Page ID** value.</span></span>  
<span data-ttu-id="c2c9a-120">Dit is de pagina voor de API waarop de sjabloon wordt toegepast.</span><span class="sxs-lookup"><span data-stu-id="c2c9a-120">This is the page for the API to which the template will be applied.</span></span> <span data-ttu-id="c2c9a-121">De opzoekactie **Pagina-id** biedt een overzicht van alle API's die beschikbaar zijn in de bibliotheek.</span><span class="sxs-lookup"><span data-stu-id="c2c9a-121">The **Page ID** lookup provides a list of all APIs available in the library.</span></span>
4. <span data-ttu-id="c2c9a-122">Selecteer een waarde in het veld **Sjablooncode**.</span><span class="sxs-lookup"><span data-stu-id="c2c9a-122">Select a value in the **Template Code** field.</span></span>  
<span data-ttu-id="c2c9a-123">De sjablooncode is de code voor de sjabloon die in het venster **Sjablonen voor configuratie** is gedefinieerd.</span><span class="sxs-lookup"><span data-stu-id="c2c9a-123">The template code is the code for the template that was defined in the **Configuration Templates** window.</span></span> <span data-ttu-id="c2c9a-124">De gedefinieerde sjabloonwaarden worden toegepast op de API.</span><span class="sxs-lookup"><span data-stu-id="c2c9a-124">The template values defined are applied to the API.</span></span> 
5. <span data-ttu-id="c2c9a-125">Geef in het veld **Voorwaarden** op welke sjabloon moet worden toegepast.</span><span class="sxs-lookup"><span data-stu-id="c2c9a-125">In the **Conditions** field, specify which template should be applied.</span></span>  
<span data-ttu-id="c2c9a-126">De gedefinieerde sjabloon wordt toegepast op een nieuwe record die met de API wordt gemaakt als en alleen als aan de voorwaarden die in het veld **Voorwaarden** zijn gedefinieerd, wordt voldaan door de waarden die al zijn gedefinieerd voor het nieuwe exemplaar van de entiteit.</span><span class="sxs-lookup"><span data-stu-id="c2c9a-126">The defined template is applied to a new record created through the API if, and only if, the conditions defined in the **Conditions** field are met by the values already defined for the new instance of the entity.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2c9a-127">Zie ook</span><span class="sxs-lookup"><span data-stu-id="c2c9a-127">See Also</span></span>
[<span data-ttu-id="c2c9a-128">API-documentatie</span><span class="sxs-lookup"><span data-stu-id="c2c9a-128">API Documentation</span></span>](/dynamics-nav/fin-graph)  
<span data-ttu-id="c2c9a-129">[Connect Apps ontwikkelen voor [!INCLUDE[d365fin_md](includes/d365fin_md.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)</span><span class="sxs-lookup"><span data-stu-id="c2c9a-129">[Developing Connect Apps for [!INCLUDE[d365fin_md](includes/d365fin_md.md)]](/dynamics365/business-central/dev-itpro/developer/devenv-develop-connect-apps)</span></span>  
[<span data-ttu-id="c2c9a-130">De API's inschakelen</span><span class="sxs-lookup"><span data-stu-id="c2c9a-130">Enabling the APIs</span></span>](/dynamics-nav/enabling-apis-for-dynamics-nav)  
[<span data-ttu-id="c2c9a-131">Eindpunten voor de API's</span><span class="sxs-lookup"><span data-stu-id="c2c9a-131">Endpoints for the APIs</span></span>](/dynamics-nav/endpoints-apis-for-dynamics)  
[<span data-ttu-id="c2c9a-132">Een bedrijf instellen met RapidStart Services</span><span class="sxs-lookup"><span data-stu-id="c2c9a-132">Setting Up a Company with RapidStart Services</span></span>](admin-set-up-a-company-with-rapidstart.md)  
[<span data-ttu-id="c2c9a-133">Beheer</span><span class="sxs-lookup"><span data-stu-id="c2c9a-133">Administration</span></span>](admin-setup-and-administration.md)
