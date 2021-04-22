---
title: XML-schema's gebruiken om gegevensuitwisselingsdefinities voor te bereiden
description: Gebruik XML-schema's om het kader voor documentuitwisseling in te stellen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 70e80403175c6a77d120a3b405b1b5758410c227
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781374"
---
# <a name="use-xml-schemas-to-prepare-data-exchange-definitions"></a><span data-ttu-id="f4116-103">XML-schema's gebruiken om gegevensuitwisselingsdefinities voor te bereiden</span><span class="sxs-lookup"><span data-stu-id="f4116-103">Use XML Schemas to Prepare Data Exchange Definitions</span></span>

<span data-ttu-id="f4116-104">Om het importeren/exporteren van gegevens in XML-bestanden via het kader voor gegevensuitwisseling in [!INCLUDE[prod_short](includes/prod_short.md)] mogelijk te maken, kunt u XML-schema's gebruiken om te bepalen welke gegevenselementen u wilt uitwisselen met [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="f4116-104">To enable import/export of data in XML files through the data exchange framework in [!INCLUDE[prod_short](includes/prod_short.md)], you can use XML schemas to define which data elements you want to exchange with [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="f4116-105">Hiertoe opent u de pagina **XML-schemaviewer** en laadt u het XML-schemabestand, selecteert u de relevante gegevenselementen en initialiseert u vervolgens een definitie van gegevensuitwisseling.</span><span class="sxs-lookup"><span data-stu-id="f4116-105">You perform this work on the **XML Schema Viewer** page by loading the XML schema file, selecting the relevant data elements, and then initializing a data exchange definition.</span></span>  

 <span data-ttu-id="f4116-106">Wanneer u hebt gedefinieerd welke gegevenselementen moeten worden opgenomen op basis van het XML-schema, kunt u de actie **Definities van gegevensuitwisseling genereren** gebruiken om een definitie van gegevensuitwisseling te initialiseren die is gebaseerd op de geselecteerde gegevenselementen, die u vervolgens voltooit in het kader voor gegevensuitwisseling.</span><span class="sxs-lookup"><span data-stu-id="f4116-106">When you have defined which data elements to include based on the XML schema, you can use the **Generate Data Exchange Definition** action to initialize a data exchange definition based on the selected data elements, which you then complete in the Data Exchange Framework.</span></span> <span data-ttu-id="f4116-107">Hiermee wordt een record gemaakt op de pagina **Uitwisselingsdefinitie van boeking** waar u verdergaat door te bepalen welke elementen in het bestand worden gekoppeld aan welke velden in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="f4116-107">This creates a record on the **Posting Exchange Definition** page where you continue by defining which elements in the file map to which fields in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="f4116-108">Zie [Definities voor gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f4116-108">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

 <span data-ttu-id="f4116-109">Dit onderwerp bevat de volgende procedures:</span><span class="sxs-lookup"><span data-stu-id="f4116-109">This topic contains the following procedures:</span></span>  

- <span data-ttu-id="f4116-110">Een XML-schemabestand laden</span><span class="sxs-lookup"><span data-stu-id="f4116-110">To load an XML schema file</span></span>  

- <span data-ttu-id="f4116-111">Knooppunten in een XML-schema selecteren of wissen</span><span class="sxs-lookup"><span data-stu-id="f4116-111">To select or clear nodes in an XML schema</span></span>  

- <span data-ttu-id="f4116-112">De definitie van een gegevensuitwisseling genereren die is gebaseerd op een XML-schema</span><span class="sxs-lookup"><span data-stu-id="f4116-112">To generate a data exchange definition that is based on an XML schema</span></span>  

## <a name="to-load-an-xml-schema-file"></a><span data-ttu-id="f4116-113">Een XML-schemabestand laden</span><span class="sxs-lookup"><span data-stu-id="f4116-113">To load an XML schema file</span></span>

1. <span data-ttu-id="f4116-114">Zorg dat het relevante XML-schemabestand beschikbaar is.</span><span class="sxs-lookup"><span data-stu-id="f4116-114">Make sure that the relevant XML schema file is available.</span></span> <span data-ttu-id="f4116-115">De bestandextensie is .xsd.</span><span class="sxs-lookup"><span data-stu-id="f4116-115">The file extension is .xsd.</span></span>  

2. <span data-ttu-id="f4116-116">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **XML-schema's** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="f4116-116">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schemas**, and then choose the related link.</span></span>  

3. <span data-ttu-id="f4116-117">Kies de actie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="f4116-117">Choose the **New** action.</span></span>  

4. <span data-ttu-id="f4116-118">Vul de velden in zoals beschreven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="f4116-118">Fill the fields as described in the following table.</span></span>  

    |<span data-ttu-id="f4116-119">Veld</span><span class="sxs-lookup"><span data-stu-id="f4116-119">Field</span></span>|<span data-ttu-id="f4116-120">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="f4116-120">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="f4116-121">**Code**</span><span class="sxs-lookup"><span data-stu-id="f4116-121">**Code**</span></span>|<span data-ttu-id="f4116-122">Geef een code op ter identificatie van het XML-schema.</span><span class="sxs-lookup"><span data-stu-id="f4116-122">Specify a code to identify the XML schema.</span></span>|  
    |<span data-ttu-id="f4116-123">**Beschrijving**</span><span class="sxs-lookup"><span data-stu-id="f4116-123">**Description**</span></span>|<span data-ttu-id="f4116-124">Geef een omschrijving op van het XML-schema.</span><span class="sxs-lookup"><span data-stu-id="f4116-124">Specify a description of the XML schema.</span></span>|  

     <span data-ttu-id="f4116-125">Het veld **Doelnaamspace** bevat elke naamruimte in het XML-schemabestand dat is geladen voor de regel.</span><span class="sxs-lookup"><span data-stu-id="f4116-125">The **Target Namespace** field specifies any namespace in the XML schema file that has been loaded for the line.</span></span>  

5. <span data-ttu-id="f4116-126">Kies de actie **Schema laden** en selecteer het XML-schemabestand.</span><span class="sxs-lookup"><span data-stu-id="f4116-126">Choose the **Load Schema** action, and then select the XML schema file.</span></span>  

     <span data-ttu-id="f4116-127">Wanneer het bestand is geladen, worden de overige velden op de regel gevuld met informatie uit het bestand en wordt het selectievakje **Schema is geladen** ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="f4116-127">When the file is loaded, the rest of the fields on the line are filled with information from the file, and the **Schema is Loaded** check box is selected.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="f4116-128">De structuur van het geladen XML-schema is standaard samengevouwen.</span><span class="sxs-lookup"><span data-stu-id="f4116-128">The tree of the loaded XML schema is collapsed by default.</span></span> <span data-ttu-id="f4116-129">U kunt een knooppunt uitvouwen door de knop **+** op het knooppunt te kiezen.</span><span class="sxs-lookup"><span data-stu-id="f4116-129">You expand each node by choosing the **+** button on the node.</span></span> <span data-ttu-id="f4116-130">Kies **Alles uitvouwen** op het lint om alle knooppunten uit te vouwen.</span><span class="sxs-lookup"><span data-stu-id="f4116-130">To expand all nodes, choose **Expand All** on the ribbon.</span></span>  

### <a name="to-select-or-clear-nodes-in-an-xml-schema"></a><span data-ttu-id="f4116-131">Knooppunten in een XML-schema selecteren of wissen</span><span class="sxs-lookup"><span data-stu-id="f4116-131">To select or clear nodes in an XML schema</span></span>  

1. <span data-ttu-id="f4116-132">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **XML-schemaviewer** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="f4116-132">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **XML Schema Viewer**, and then choose the related link.</span></span>  

2. <span data-ttu-id="f4116-133">Vul de velden in voor de kop, zoals in de volgende tabel is beschreven.</span><span class="sxs-lookup"><span data-stu-id="f4116-133">Fill the fields on the header as described in the following table.</span></span>  

    |<span data-ttu-id="f4116-134">Veld</span><span class="sxs-lookup"><span data-stu-id="f4116-134">Field</span></span>|<span data-ttu-id="f4116-135">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="f4116-135">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="f4116-136">**Schemacode XML**</span><span class="sxs-lookup"><span data-stu-id="f4116-136">**XML Schema Code**</span></span>|<span data-ttu-id="f4116-137">Geef het XML-schemabestand op dat u hebt geladen in stap 5 in het gedeelte 'Een XML-schemabestand laden'.</span><span class="sxs-lookup"><span data-stu-id="f4116-137">Specify the XML schema file that you loaded in step 5 in the "To load an XML schema file" section.</span></span>|  
    |<span data-ttu-id="f4116-138">**Nieuw XMLport-nr.**</span><span class="sxs-lookup"><span data-stu-id="f4116-138">**New XMLport No.**</span></span>|<span data-ttu-id="f4116-139">Geef het nummer op van de XMLport die wordt gemaakt op basis van dit XML-schema wanneer u de actie **XMLport genereren** kiest.</span><span class="sxs-lookup"><span data-stu-id="f4116-139">Specify the number of the XMLport that is created from this XML schema when you choose the **Generate XMLport** action.</span></span>|  

     <span data-ttu-id="f4116-140">De regels worden nu gevuld met knooppunten die alle onderdelen in het XML-schema vertegenwoordigen.</span><span class="sxs-lookup"><span data-stu-id="f4116-140">The lines are now filled with nodes representing all elements in the XML schema.</span></span> <span data-ttu-id="f4116-141">Knooppunten voor elementen die verplicht zijn volgens het XML-schema, worden standaard geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="f4116-141">Nodes for elements that are mandatory according to the XML schema are selected by default.</span></span>  

3. <span data-ttu-id="f4116-142">Vouw op de eerste regel in de kolom **Knooppuntnaam** het knooppunt **Document** uit en vouw vervolgens geleidelijk onderliggende knooppunten uit die u wilt controleren.</span><span class="sxs-lookup"><span data-stu-id="f4116-142">On the first line, in the **Node Name** column, expand the **Document** node, and then gradually expand underlying nodes that you want to review.</span></span>  

     <span data-ttu-id="f4116-143">U kunt ook met de rechtermuisknop op een knooppunt klikken en **Alles uitvouwen** kiezen.</span><span class="sxs-lookup"><span data-stu-id="f4116-143">Alternatively, right-click on a node and then choose **Expand All**.</span></span>  

4. <span data-ttu-id="f4116-144">Kies een van de volgende acties om te wijzigen welke knooppunten moeten worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f4116-144">Choose either of the following actions to change which nodes are displayed.</span></span>  

    |<span data-ttu-id="f4116-145">**Actie**</span><span class="sxs-lookup"><span data-stu-id="f4116-145">**Action**</span></span>|<span data-ttu-id="f4116-146">Omschrijving</span><span class="sxs-lookup"><span data-stu-id="f4116-146">Description</span></span>|  
    |----------------|---------------------------------------|  
    |<span data-ttu-id="f4116-147">**Alles weergeven**</span><span class="sxs-lookup"><span data-stu-id="f4116-147">**Show All**</span></span>|<span data-ttu-id="f4116-148">Alle knooppunten worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f4116-148">All nodes are shown.</span></span>|  
    |<span data-ttu-id="f4116-149">**Niet-verplicht verbergen**</span><span class="sxs-lookup"><span data-stu-id="f4116-149">**Hide Non-Mandatory**</span></span>|<span data-ttu-id="f4116-150">Alleen knooppunten die elementen vertegenwoordigen die vereist zijn volgens het XML-schema, worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f4116-150">Only nodes representing elements that are required according to the XML schema are shown.</span></span> <span data-ttu-id="f4116-151">Deze knooppunten worden doorgaans aangegeven met een **1** in het veld **MinOccurs**.</span><span class="sxs-lookup"><span data-stu-id="f4116-151">These nodes are typically indicated by a **1** in the **MinOccurs** field.</span></span><br /><br /> <span data-ttu-id="f4116-152">Kies **Alles weergeven** om de weergave om te keren.</span><span class="sxs-lookup"><span data-stu-id="f4116-152">Choose **Show All** to reverse the view.</span></span>|  
    |<span data-ttu-id="f4116-153">**Niet-geselecteerd verbergen**</span><span class="sxs-lookup"><span data-stu-id="f4116-153">**Hide Non-Selected**</span></span>|<span data-ttu-id="f4116-154">Alleen knooppunten waarbij het selectievakje **Geselecteerd** is ingeschakeld, worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f4116-154">Only nodes where the **Selected** check box is selected are shown.</span></span><br /><br /> <span data-ttu-id="f4116-155">Kies **Alles weergeven** om de weergave om te keren.</span><span class="sxs-lookup"><span data-stu-id="f4116-155">Choose **Show All** to reverse the view.</span></span>|  

5. <span data-ttu-id="f4116-156">Kies de actie **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="f4116-156">Choose the **Edit** action.</span></span>  

6. <span data-ttu-id="f4116-157">Geef met het selectievakje **Geselecteerd** voor elk knooppunt aan of u wilt dat het element wordt ondersteund in de definitie voor gegevensuitwisseling voor het gerelateerde SEPA-bankbestand.</span><span class="sxs-lookup"><span data-stu-id="f4116-157">In the **Selected** check box, specify for each node if you want the element to be supported in the data exchange definition for the related SEPA bank file.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="f4116-158">Wanneer u een verplicht onderliggend knooppunt selecteert, worden alle bovenliggende knooppunten ook geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="f4116-158">When you select a mandatory child node, all parent nodes above it are also selected.</span></span>  

7. <span data-ttu-id="f4116-159">Kies de actie **Alle verplichte elementen selecteren** om alle knooppunten opnieuw te selecteren die elementen voorstellen die verplicht zijn volgens het XML-schema.</span><span class="sxs-lookup"><span data-stu-id="f4116-159">Choose the **Select All Mandatory Elements** action to reselect all nodes that represent elements that are mandatory according to the XML schema.</span></span>  

8. <span data-ttu-id="f4116-160">Kies de actie **Alles deselecteren** om alle selecties te wissen.</span><span class="sxs-lookup"><span data-stu-id="f4116-160">Choose the **Deselect All** action to clear all selections.</span></span>  

     <span data-ttu-id="f4116-161">Het veld **Keuze** geeft aan of het knooppunt twee of meer knooppunten op hetzelfde niveau heeft die functioneren als opties.</span><span class="sxs-lookup"><span data-stu-id="f4116-161">The **Choice** field specifies that the node has two or more sibling nodes that function as options.</span></span>  

### <a name="to-generate-a-data-exchange-definition-that-is-based-on-an-xml-schema"></a><span data-ttu-id="f4116-162">De definitie van een gegevensuitwisseling genereren die is gebaseerd op een XML-schema</span><span class="sxs-lookup"><span data-stu-id="f4116-162">To generate a data exchange definition that is based on an XML schema</span></span>  

1. <span data-ttu-id="f4116-163">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **XML-schema's** in en kies de gerelateerde koppeling.</span><span class="sxs-lookup"><span data-stu-id="f4116-163">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter  **XML Schemas**, and then choose the related link.</span></span>  

2. <span data-ttu-id="f4116-164">Selecteer het desbetreffende XML-schema en kies de actie **XML-schemaviewer openen**.</span><span class="sxs-lookup"><span data-stu-id="f4116-164">Select the relevant XML schema, and then choose the **Open XML Schema Viewer** action.</span></span>  

3. <span data-ttu-id="f4116-165">Zorg dat de relevante knooppunten zijn geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="f4116-165">Make sure the relevant nodes are selected.</span></span> <span data-ttu-id="f4116-166">Zie het gedeelte 'Knooppunten selecteren of wissen in een XML-schema' voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f4116-166">For more information, see the "To select or clear nodes in an XML schema" section.</span></span>  

4. <span data-ttu-id="f4116-167">Kies op de pagina **XML-schemaviewer** de actie **Definitie voor gegevensuitwisseling genereren**.</span><span class="sxs-lookup"><span data-stu-id="f4116-167">On the **XML Schema Viewer** page, choose the **Generate Data Exchange Definition** action.</span></span>  

 <span data-ttu-id="f4116-168">Op de pagina **Uitwisselingsdefinitie van boeking** wordt een definitie voor gegevensuitwisseling gemaakt die u kunt invullen om op te geven welke elementen in het bestand moeten worden toegewezen aan welke velden in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="f4116-168">A data exchange definition is created on the **Posting Exchange Definition** page, which you can complete by specifying which elements in the file map to which fields in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="f4116-169">Zie [Definities voor gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f4116-169">For more information, see [Set Up Data Exchange Definitions](across-how-to-set-up-data-exchange-definitions.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="f4116-170">U kunt ook de functie **Bestandstructuur ophalen** op de pagina **Uitwisselingsdefinitie van boeking** gebruiken. Deze maakt gebruik van de functionaliteit van de pagina **XML-schemaviewer** om het sneltabblad **Kolomdefinities** vooraf te vullen.</span><span class="sxs-lookup"><span data-stu-id="f4116-170">You can also use the **Get File Structure** function from the **Posting Exchange Definition** page, which uses the functionality of the **XML Schema Viewer** page to prefill the **Column Definitions** TastTab.</span></span>  

> [!NOTE]
> <span data-ttu-id="f4116-171">In releasewave 1 van 2019 en eerdere versies kon u een XMLport genereren die was gebaseerd op het schema en die vervolgens importeren in uw oplossing.</span><span class="sxs-lookup"><span data-stu-id="f4116-171">In 2019 release wave 1 and earlier versions, you could generate an XMLport that was based on the schema and then import that into your solution.</span></span> <span data-ttu-id="f4116-172">Dit wordt niet langer ondersteund.</span><span class="sxs-lookup"><span data-stu-id="f4116-172">This is no longer supported.</span></span>

## <a name="see-also"></a><span data-ttu-id="f4116-173">Zie ook</span><span class="sxs-lookup"><span data-stu-id="f4116-173">See Also</span></span>

[<span data-ttu-id="f4116-174">Definities voor gegevensuitwisseling instellen</span><span class="sxs-lookup"><span data-stu-id="f4116-174">Set Up Data Exchange Definitions</span></span>](across-how-to-set-up-data-exchange-definitions.md)  
[<span data-ttu-id="f4116-175">Betalingen naar een bankbestand exporteren</span><span class="sxs-lookup"><span data-stu-id="f4116-175">Export Payments to a Bank File</span></span>](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#exporting-payments-to-a-bank-file)  
[<span data-ttu-id="f4116-176">Betalingen verzamelen via automatische incasso van SEPA</span><span class="sxs-lookup"><span data-stu-id="f4116-176">Collect Payments with SEPA Direct Debit</span></span>](finance-collect-payments-with-sepa-direct-debit.md)  
[<span data-ttu-id="f4116-177">Over het kader voor gegevensuitwisseling</span><span class="sxs-lookup"><span data-stu-id="f4116-177">About the Data Exchange Framework</span></span>](across-about-the-data-exchange-framework.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]