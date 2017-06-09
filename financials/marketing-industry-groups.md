---
title: Sectoren voor contactbedrijven instellen | Microsoft Docs
description: Beschrijft het gebruik van sectoren met contacten in Financials
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 03/28/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 34b81ec1e92eea67af13c7a2dfe03bdb97c8c59c
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-industry-groups-for-contact-companies"></a>Sectoren instellen voor contactbedrijven
U gebruikt sectoren om het soort industrie aan te geven waartoe uw contacten behoren, bijvoorbeeld de detailhandel of de automobielindustrie.

Sectoren gebruiken voor contacten is een proces van twee stappen. Eerst definieert u de sectorcode. U hoeft deze stap slechts eenmaal uit te voeren voor elke sector. Als u een sectorcode hebt, kunt u beginnen de code toe te wijzen aan contactbedrijven.

**Opmerking**: als u de contacten wilt synchroniseren met leveranciers, klanten of bankrekeningen in een ander onderdeel van de toepassing, kunt u een zakenrelatie instellen.

## <a name="to-define-an-industry-group-code"></a>Een sectorcode definiëren
De sectorcode bepaalt het type of de categorie van de groep, zoals ADVERTENTIE voor reclame of PERS voor tv en radio. U kunt meerdere sectorcodes hebben. Als u de sectoren wilt definiëren, gebruikt u het venster **Sectoren**.

1. In de rechterbovenhoek, kies het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Sectoren** in en klik op de gerelateerde koppeling.
2. Kies de actie **Nieuw** en vul een code en een beschrijving in. De code kan maximaal uit 11 tekens bestaan en kan elke combinatie zijn van cijfers en letters.

## <a name="AssignIndustryGroupContact">Sectoren toewijzen aan een contact</a>
U kunt geen sectoren toewijzen aan een contactpersoon, alleen aan contactbedrijven.

1. Open het contact.
2. Kies de actie **Bedrijf** en kies vervolgens de actie **Sectoren**. Het venster **Contact sectoren** wordt geopend.
3. Selecteer in het veld **Sectorcode** de sectorgroepen die u wilt toewijzen.

Herhaal deze stappen om het gewenste aantal sectoren toe te wijzen. U kunt sectoren ook toewijzen vanuit het contactoverzicht door dezelfde procedure te volgen.

Het aantal sectoren dat u aan het contact hebt toegewezen, wordt weergegeven in het veld **Aantal sectoren** in het gedeelte **Segmentatie** in het venster **Contact**.

Nadat u sectoren hebt toegewezen aan de contacten, kunt u deze gegevens gebruiken om contacten voor de segmenten te selecteren. Zie voor meer informatie [Procedure: Contacten toevoegen aan segmenten](marketing-add-contact-segment.md).

## <a name="see-also"></a>Zie ook
[Contactbedrijven maken](marketing-create-contact-companies.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

