---
title: Rapportselectie in Business Central
description: Leer hoe u de rapporten instelt die u gebruikt om verschillende soorten documenten af te drukken in Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: setup, reporting
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ba15a65317ebf52579c285c93dd59eba1b65ae1b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5787119"
---
# <a name="report-selection-in-business-central"></a><span data-ttu-id="7aee0-103">Rapportselectie in Business Central</span><span class="sxs-lookup"><span data-stu-id="7aee0-103">Report Selection in Business Central</span></span>

<span data-ttu-id="7aee0-104">U kunt standaardrapporten instellen die worden gebruikt om de verschillende documenten af te drukken voor inkopen en verkopen, zoals orders, offertes, facturen en creditnota's.</span><span class="sxs-lookup"><span data-stu-id="7aee0-104">You can set up default reports that will be used to print the various documents for sales and purchases, such as orders, quotes, invoices, and credit memos.</span></span> <span data-ttu-id="7aee0-105">Als u bijvoorbeeld een specifieke lay-out voor verkoopfacturen heeft, kunt u dat rapport specificeren op de pagina **Rapportselecties - Verkoop**, zodat het wordt gebruikt om verkoopfacturen te verzenden of af te drukken.</span><span class="sxs-lookup"><span data-stu-id="7aee0-105">For example, if you have a specific layout for sales invoices, you can specify that report in the **Report Selections - Sales** page so that it will be used to send or print sales invoices.</span></span>  

<span data-ttu-id="7aee0-106">De **Rapportselecties**-pagina's specificeren welk rapport in verschillende situaties zal worden afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="7aee0-106">The **Report Selections** pages specify which report will be printed in different situations.</span></span> <span data-ttu-id="7aee0-107">[!INCLUDE [prod_short](includes/prod_short.md)] bevat standaardconfiguraties, maar u kunt deze standaardinstellingen natuurlijk wijzigen.</span><span class="sxs-lookup"><span data-stu-id="7aee0-107">[!INCLUDE [prod_short](includes/prod_short.md)] includes default configurations, but of course you can change these defaults.</span></span> <span data-ttu-id="7aee0-108">U kunt bijvoorbeeld ook lijsten aan de **Rapportselecties**-pagina's toevoegen als u meer dan één rapport per documentsoort wilt afdrukken.</span><span class="sxs-lookup"><span data-stu-id="7aee0-108">You can also add reports to the **Report Selection** pages if you want to print more than one report per document type, for example.</span></span>  

## <a name="available-report-selections"></a><span data-ttu-id="7aee0-109">Beschikbare rapportselecties</span><span class="sxs-lookup"><span data-stu-id="7aee0-109">Available report selections</span></span>

<span data-ttu-id="7aee0-110">[!INCLUDE [prod_short](includes/prod_short.md)] bevat verschillende **Rapportselectie**-pagina's voor verschillende gebieden.</span><span class="sxs-lookup"><span data-stu-id="7aee0-110">[!INCLUDE [prod_short](includes/prod_short.md)] includes different **Report Selection** pages for different areas.</span></span> <span data-ttu-id="7aee0-111">In de volgende tabellen wordt beschreven waar u informatie over de verschillende pagina's kunt vinden.</span><span class="sxs-lookup"><span data-stu-id="7aee0-111">The following tables describes where you can find information about the different pages.</span></span>  

|<span data-ttu-id="7aee0-112">Gebied of taak</span><span class="sxs-lookup"><span data-stu-id="7aee0-112">Area or task</span></span>  |<span data-ttu-id="7aee0-113">Meer informatie</span><span class="sxs-lookup"><span data-stu-id="7aee0-113">Learn more</span></span>|
|--------------|----------|
|<span data-ttu-id="7aee0-114">Voorbeeld van hoe rapportselectie werkt (verkoop)</span><span class="sxs-lookup"><span data-stu-id="7aee0-114">Example of how report selection works (Sales)</span></span>|[<span data-ttu-id="7aee0-115">Rapportselectie voor verkoopdocumenten</span><span class="sxs-lookup"><span data-stu-id="7aee0-115">Report selection for sales documents</span></span>](#example-report-selection-for-sales-documents)|
|<span data-ttu-id="7aee0-116">Standaardlay-out voor e-mails met verkoop- en inkoopdocumenten</span><span class="sxs-lookup"><span data-stu-id="7aee0-116">Default layout for emails with sales and purchase documents</span></span>  |[<span data-ttu-id="7aee0-117">Herbruikbare e-mailteksten en lay-outs instellen voor verkoop- en inkoopdocumenten</span><span class="sxs-lookup"><span data-stu-id="7aee0-117">Set Up Reusable Email Texts and Layouts for Sales and Purchase Documents</span></span>](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents) |
|<span data-ttu-id="7aee0-118">Cheque-indelingen definiëren</span><span class="sxs-lookup"><span data-stu-id="7aee0-118">Define check layouts</span></span>     |[<span data-ttu-id="7aee0-119">Een cheque-indeling selecteren</span><span class="sxs-lookup"><span data-stu-id="7aee0-119">Select a Check Layout</span></span>](finance-how-define-check-layouts.md) |
|<span data-ttu-id="7aee0-120">Rapporten definiëren voor btw-rapportage (Duitsland)</span><span class="sxs-lookup"><span data-stu-id="7aee0-120">Define reports for VAT reporting (Germany)</span></span>|[<span data-ttu-id="7aee0-121">Rapporten voor btw en Intrastat instellen</span><span class="sxs-lookup"><span data-stu-id="7aee0-121">Set Up Reports for VAT and Intrastat</span></span>](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md) |

> [!TIP]
> <span data-ttu-id="7aee0-122">Uw [!INCLUDE [prod_short](includes/prod_short.md)] kan extra **Rapportselectie**-pagina's bevatten, bijvoorbeeld afhankelijk van uw locatie en branche.</span><span class="sxs-lookup"><span data-stu-id="7aee0-122">Your [!INCLUDE [prod_short](includes/prod_short.md)] can include additional **Report Selection** pages, depending on your location and industry, for example.</span></span> <span data-ttu-id="7aee0-123">U kunt uw instellingen altijd controleren door het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen") te kiezen, **Rapportselecties** in te voeren en vervolgens de relevante koppeling te kiezen.</span><span class="sxs-lookup"><span data-stu-id="7aee0-123">You can always check your setup by choosing the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, entering **Report Selections**, and then choose the relevant link.</span></span>

<span data-ttu-id="7aee0-124">De standaardversie van [!INCLUDE [prod_short](includes/prod_short.md)] omvat het volgende **Rapportselectie**-pagina's:</span><span class="sxs-lookup"><span data-stu-id="7aee0-124">The default version of [!INCLUDE [prod_short](includes/prod_short.md)] includes the following **Report Section** pages:</span></span>

* <span data-ttu-id="7aee0-125">**Rapportselectie - Verkoop**</span><span class="sxs-lookup"><span data-stu-id="7aee0-125">**Report Selection - Sales**</span></span>  
* <span data-ttu-id="7aee0-126">**Rapportselectie - Inkoop**</span><span class="sxs-lookup"><span data-stu-id="7aee0-126">**Report Selection - Purchase**</span></span>  
* <span data-ttu-id="7aee0-127">**Rapportselectie - Voorraad**</span><span class="sxs-lookup"><span data-stu-id="7aee0-127">**Report Selection - Inventory**</span></span>  
* <span data-ttu-id="7aee0-128">**Rapportselectie - Cashflow**</span><span class="sxs-lookup"><span data-stu-id="7aee0-128">**Report Selection - Cash Flow**</span></span>  
* <span data-ttu-id="7aee0-129">**Rapportselectie - Magazijn**</span><span class="sxs-lookup"><span data-stu-id="7aee0-129">**Report Selection - Warehouse**</span></span>  
* <span data-ttu-id="7aee0-130">**Rapportselectie - Bankrekening**</span><span class="sxs-lookup"><span data-stu-id="7aee0-130">**Report Selection - Bank Account**</span></span>  
* <span data-ttu-id="7aee0-131">**Rapportselecties - Aanmaning/rentefactuur**</span><span class="sxs-lookup"><span data-stu-id="7aee0-131">**Report Selections Reminder/Finance Charge**</span></span>  

## <a name="example-report-selection-for-sales-documents"></a><span data-ttu-id="7aee0-132">Voorbeeld: Rapportselectie voor verkoopdocumenten</span><span class="sxs-lookup"><span data-stu-id="7aee0-132">Example: Report selection for sales documents</span></span>

<span data-ttu-id="7aee0-133">De pagina **Rapportselectie - Verkoop** definieert de standaardrapporten die in verschillende scenario's voor elk gerelateerd documenttype moeten worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="7aee0-133">The **Report Selection - Sales** page defines the default reports to use in different scenarios for each related document type.</span></span> <span data-ttu-id="7aee0-134">Kies een documenttype in het veld **Gebruik** en voeg vervolgens de rapportselectie toe of controleer deze.</span><span class="sxs-lookup"><span data-stu-id="7aee0-134">Choose a document type in the **Usage** field, and then add or review the report selection.</span></span> <span data-ttu-id="7aee0-135">U kunt meer dan één rapport instellen en de volgorde bepalen waarin de rapporten moeten worden verzonden of afgedrukt.</span><span class="sxs-lookup"><span data-stu-id="7aee0-135">You can set up more than one report and the order of sequence that the reports must be sent or printed in.</span></span>  

[!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

<span data-ttu-id="7aee0-136">Sommige typen documenten kunnen als e-mailbijlagen worden verzonden en andere niet.</span><span class="sxs-lookup"><span data-stu-id="7aee0-136">Some types of document can be sent as email attachments, and others cannot.</span></span> <span data-ttu-id="7aee0-137">Elke **Rapportselectie**-pagina toont extra velden als het type e-mail standaard ondersteunt.</span><span class="sxs-lookup"><span data-stu-id="7aee0-137">Each **Report Selection** page shows additional fields if the type support email out of the box.</span></span>  

<span data-ttu-id="7aee0-138">Op de pagina's **Rapportselectie - Verkoop** en **Rapportselectie - Aankoop** helpen de volgende velden u bijvoorbeeld bij het instellen van e-mail:</span><span class="sxs-lookup"><span data-stu-id="7aee0-138">For example, in the **Report Selection - Sales** and **Report Selection - Purchase** pages, the following fields help you set up emailing:</span></span>

|<span data-ttu-id="7aee0-139">Veldnaam</span><span class="sxs-lookup"><span data-stu-id="7aee0-139">Field name</span></span> |<span data-ttu-id="7aee0-140">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="7aee0-140">Description</span></span>  |
|-----------|-------------|
|<span data-ttu-id="7aee0-141">**Gebruiken voor hoofdtekst van e-mailbericht**</span><span class="sxs-lookup"><span data-stu-id="7aee0-141">**Use for Email Body**</span></span>| <span data-ttu-id="7aee0-142">Hiermee wordt opgegeven dat overzichtsgegevens, zoals het factuurnummer, de vervaldatum en de koppeling naar de betalingsservice, worden ingevoegd in de hoofdtekst van de e-mail die u verzendt.</span><span class="sxs-lookup"><span data-stu-id="7aee0-142">Specifies that summarized information, such as invoice number, due date, and payment service link, will be inserted in the body of the email that you send.</span></span>        |
|<span data-ttu-id="7aee0-143">**Gebruiken voor e-mailbijlage**</span><span class="sxs-lookup"><span data-stu-id="7aee0-143">**Use for Email Attachment**</span></span>| <span data-ttu-id="7aee0-144">Hiermee wordt opgegeven dat het gerelateerde document aan de e-mail wordt gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="7aee0-144">Specifies that the related document will be attached to the email.</span></span>|
|<span data-ttu-id="7aee0-145">**Indelingsomschrijving van hoofdtekst van e-mailbericht**</span><span class="sxs-lookup"><span data-stu-id="7aee0-145">**Email Body Layout Description**</span></span>|<span data-ttu-id="7aee0-146">Specificeert de lay-out van de hoofdtekst van de e-mail die wordt gebruikt, meestal een aangepaste rapportlay-out.</span><span class="sxs-lookup"><span data-stu-id="7aee0-146">Specifies the email body layout that is used, typically a custom report layout.</span></span> |

## <a name="see-also"></a><span data-ttu-id="7aee0-147">Zie ook</span><span class="sxs-lookup"><span data-stu-id="7aee0-147">See also</span></span>

[<span data-ttu-id="7aee0-148">Herbruikbare e-mailteksten en lay-outs instellen voor verkoop- en inkoopdocumenten</span><span class="sxs-lookup"><span data-stu-id="7aee0-148">Set Up Reusable Email Texts and Layouts for Sales and Purchase Documents</span></span>](admin-how-setup-email.md#set-up-reusable-email-texts-and-layouts-for-sales-and-purchase-documents)  
[<span data-ttu-id="7aee0-149">Een cheque-indeling selecteren</span><span class="sxs-lookup"><span data-stu-id="7aee0-149">Select a Check Layout</span></span>](finance-how-define-check-layouts.md)  
[<span data-ttu-id="7aee0-150">Rapporten voor btw en Intrastat instellen (Duitsland)</span><span class="sxs-lookup"><span data-stu-id="7aee0-150">Set Up Reports for VAT and Intrastat (Germany)</span></span>](LocalFunctionality/Germany/how-to-set-up-reports-for-vat-and-intrastat.md)  
[<span data-ttu-id="7aee0-151">Indelingen van rapporten en documenten beheren</span><span class="sxs-lookup"><span data-stu-id="7aee0-151">Managing Report and Document Layouts</span></span>](ui-manage-report-layouts.md)  
[<span data-ttu-id="7aee0-152">Documentlay-outs definiëren voor klanten en leveranciers</span><span class="sxs-lookup"><span data-stu-id="7aee0-152">Define Document Layouts for Customers and Vendors</span></span>](ui-define-customer-vendor-document-layouts.md)  
[<span data-ttu-id="7aee0-153">Printers instellen</span><span class="sxs-lookup"><span data-stu-id="7aee0-153">Set Up Printers</span></span>](ui-specify-printer-selection-reports.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]