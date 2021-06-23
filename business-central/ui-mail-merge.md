---
title: Word-sjablonen gebruiken voor bulkcommunicatie | Microsoft Docs
description: Met Word-sjablonen kunt u gemakkelijk bulksgewijs documenten maken die zijn gepersonaliseerd voor specifieke entiteiten.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: document, mail, merge, Word, template, email
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: d29e29eca7dfc24ded51aed994ac7003fb4d30ab
ms.sourcegitcommit: 6bce51954f17b80491e180f25d67ff18b1618a88
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 05/27/2021
ms.locfileid: "6110966"
---
# <a name="using-word-templates-for-bulk-communication"></a><span data-ttu-id="61f00-103">Word-sjablonen gebruiken voor bulkcommunicatie</span><span class="sxs-lookup"><span data-stu-id="61f00-103">Using Word Templates for Bulk Communication</span></span>
<span data-ttu-id="61f00-104">Microsoft Word-sjablonen kunnen het gemakkelijker maken om massaal te communiceren met entiteiten zoals klanten en leveranciers.</span><span class="sxs-lookup"><span data-stu-id="61f00-104">Microsoft Word templates can make it easier to mass communicate with entities such as customers and vendors.</span></span> <span data-ttu-id="61f00-105">U kunt bijvoorbeeld brochures maken om klanten te attenderen op een verkoopcampagne, brieven om leveranciers te informeren over een nieuw aankoopbeleid of uitnodigingen om contacten aan te trekken voor een aankomend evenement.</span><span class="sxs-lookup"><span data-stu-id="61f00-105">For example, you can create brochures to alert customers about a sales campaign, letters to inform vendors about a new purchasing policy, or invitations to attract contacts to an upcoming event.</span></span>

> [!NOTE]
> <span data-ttu-id="61f00-106">U kunt Word-sjablonen alleen gebruiken op apparaten met Microsoft Word 2019 en het Windows-besturingssysteem geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="61f00-106">You can use Word templates only on devices with Microsoft Word 2019 and the Windows operating system installed.</span></span>

<span data-ttu-id="61f00-107">U kunt entiteiten gebruiken in [!INCLUDE[prod_short](includes/prod_short.md)] als de gegevensbron voor de sjabloon en samenvoegvelden toevoegen om documenten voor elke entiteit te personaliseren.</span><span class="sxs-lookup"><span data-stu-id="61f00-107">You can use entities in [!INCLUDE[prod_short](includes/prod_short.md)] as the data source for the template, and add merge fields to personalize documents for each entity.</span></span> <span data-ttu-id="61f00-108">De samenvoegvelden zijn afkomstig van de entiteit in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="61f00-108">The merge fields come from the entity in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="61f00-109">Wanneer u een Word-sjabloon toepast op een entiteit, worden gegevens uit de samenvoegvelden in het document ingevoegd.</span><span class="sxs-lookup"><span data-stu-id="61f00-109">When you apply a Word template to an entity, data from the merge fields is inserted in the document.</span></span>

<span data-ttu-id="61f00-110">Op de pagina **Word-sjablonen** kunt u een begeleide instelling gebruiken om een ZIP-bestand te downloaden dat een DataSource.txt en een Word-sjabloonbestand voor een entiteit bevat.</span><span class="sxs-lookup"><span data-stu-id="61f00-110">On the **Word Templates** page, you can use an assisted setup guide to download a ZIP file that contains a DataSource.txt and a Word template file for an entity.</span></span> <span data-ttu-id="61f00-111">Nadat u de sjabloon heeft ingesteld en samenvoegvelden heeft toegevoegd, gebruikt u dezelfde guide om de sjabloon te uploaden.</span><span class="sxs-lookup"><span data-stu-id="61f00-111">After you set up the template and add merge fields, you use the same guide to upload the template.</span></span> <span data-ttu-id="61f00-112">U kunt alleen de Word-sjabloon- en gegevensbronbestanden gebruiken die u downloadt van [!INCLUDE[prod_short](includes/prod_short.md)] en u moet de bestanden op dezelfde locatie opslaan.</span><span class="sxs-lookup"><span data-stu-id="61f00-112">You can only use the Word template and data source files that you download from [!INCLUDE[prod_short](includes/prod_short.md)], and you must store the files in the same location.</span></span>

> [!NOTE]
> <span data-ttu-id="61f00-113">Wanneer u een entiteit kiest waarvoor u een sjabloon wilt maken, toont de lijst alle entiteiten in [!INCLUDE[prod_short](includes/prod_short.md)].</span><span class="sxs-lookup"><span data-stu-id="61f00-113">When you choose an entity for which to create a template, the list shows all entities in [!INCLUDE[prod_short](includes/prod_short.md)].</span></span> <span data-ttu-id="61f00-114">U kunt echter niet voor alle entiteiten sjablonen maken.</span><span class="sxs-lookup"><span data-stu-id="61f00-114">However, you cannot create templates for all entities.</span></span> <span data-ttu-id="61f00-115">Als de naam van een entiteit speciale tekens bevat, zoals **/**, **.**, **_** of **-**, kunt u er geen sjabloon voor maken.</span><span class="sxs-lookup"><span data-stu-id="61f00-115">If the name of an entity contains special characters, such as **/**, **.**, **_**, or **-**, you cannot create a template for it.</span></span> <span data-ttu-id="61f00-116">De naam van de entiteit wordt weergegeven in de kolom **Objectbijschrift**.</span><span class="sxs-lookup"><span data-stu-id="61f00-116">The name of the entity is shown in the **Object Caption** column.</span></span>

<span data-ttu-id="61f00-117">Wanneer u de sjabloon in Word instelt, kunt u op het tabblad **Mailings** samenvoegvelden toevoegen door **Samenvoegveld invoegen** te kiezen.</span><span class="sxs-lookup"><span data-stu-id="61f00-117">When you are setting up the template in Word, on the **Mailings** tab you can add merge fields by choosing **Insert Merge Field**.</span></span>

> [!NOTE]
> <span data-ttu-id="61f00-118">U kunt geen samenvoegvelden gebruiken als de naam van het veld 40 tekens of meer bevat.</span><span class="sxs-lookup"><span data-stu-id="61f00-118">You cannot use merge fields if the name of the field contains 40 characters or more.</span></span> <span data-ttu-id="61f00-119">U kunt bijvoorbeeld het veld Company__Information_Customs_Permit_Date niet gebruiken omdat het 40 tekens heeft.</span><span class="sxs-lookup"><span data-stu-id="61f00-119">For example, you cannot use the Company__Information_Customs_Permit_Date field because it has 40 characters.</span></span> 

<span data-ttu-id="61f00-120">Als uw Word-sjabloon klaar is, kunt u op de pagina **Word-sjablonen** **Toepassen** kiezen om de documenten te genereren.</span><span class="sxs-lookup"><span data-stu-id="61f00-120">When your Word template is ready, on the **Word Templates** page you can choose **Apply** to generate the documents.</span></span> <span data-ttu-id="61f00-121">U kunt één document maken dat secties voor elke entiteit bevat, of de bewerking splitsen om voor elke entiteit een nieuw document te maken.</span><span class="sxs-lookup"><span data-stu-id="61f00-121">You can either create one document that contains sections for each entity, or split the operation to create a new document for each entity.</span></span>

## <a name="to-create-a-word-template"></a><span data-ttu-id="61f00-122">Een Word-sjabloon maken</span><span class="sxs-lookup"><span data-stu-id="61f00-122">To create a Word template</span></span>
1. <span data-ttu-id="61f00-123">Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Word-sjablonen** in en kies de desbetreffende koppeling.</span><span class="sxs-lookup"><span data-stu-id="61f00-123">Choose the ![Lightbulb that opens the Tell Me feature](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Word Templates**, and then choose the related link.</span></span>
2. <span data-ttu-id="61f00-124">Volg de stappen in het begeleide instelling.</span><span class="sxs-lookup"><span data-stu-id="61f00-124">Follow the steps in the assisted setup guide.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="see-also"></a><span data-ttu-id="61f00-125">Zie ook</span><span class="sxs-lookup"><span data-stu-id="61f00-125">See Also</span></span>
[<span data-ttu-id="61f00-126">Indelingen van rapporten en documenten beheren</span><span class="sxs-lookup"><span data-stu-id="61f00-126">Managing Report and Document Layouts</span></span>](ui-manage-report-layouts.md)  
