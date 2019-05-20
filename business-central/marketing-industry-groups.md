---
title: Sectoren voor contactbedrijven instellen | Microsoft Docs
description: Beschrijft hoe u een sector instelt en aan een contactbedrijf toewijst, bijvoorbeeld de detailhandel of de auto-industrie.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-setup-contacts
ms.openlocfilehash: 6f4fd9ef35c9a5287b01740861ad0b835c319ff4
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239205"
---
# <a name="set-up-industry-groups-for-contact-companies"></a>Sectoren instellen voor contactbedrijven
U gebruikt sectoren om het soort industrie aan te geven waartoe uw contacten behoren, bijvoorbeeld de detailhandel of de automobielindustrie.

Sectoren gebruiken voor contacten is een proces van twee stappen. Eerst definieert u de sectorcode. U hoeft deze stap slechts eenmaal uit te voeren voor elke sector. Als u een sectorcode hebt, kunt u beginnen de code toe te wijzen aan contactbedrijven.

> [!NOTE]  
>   Als u de contacten wilt synchroniseren met leveranciers, klanten of bankrekeningen in een ander onderdeel van de toepassing, kunt u een zakenrelatie instellen.

## <a name="to-define-an-industry-group-code"></a>Een sectorcode definiëren
De sectorcode bepaalt het type of de categorie van de groep, zoals ADVERTENTIE voor reclame of PERS voor tv en radio. U kunt meerdere sectorcodes hebben. Als u de sectoren wilt definiëren, gebruikt u de pagina **Sectoren**.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Sectoren** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw** en vul een code en een beschrijving in. De code kan maximaal uit 11 tekens bestaan en kan elke combinatie zijn van cijfers en letters.

## <a name="AssignIndustryGroupContact">Sectoren toewijzen aan een contact</a>
U kunt geen sectoren toewijzen aan een contactpersoon, alleen aan contactbedrijven.

1. Open het contact.
2. Kies de actie **Bedrijf** en kies vervolgens de actie **Sectoren**. De pagina **Contact sectoren** wordt geopend.
3. Selecteer in het veld **Sectorcode** de sectorgroepen die u wilt toewijzen.

Herhaal deze stappen om het gewenste aantal sectoren toe te wijzen. U kunt sectoren ook toewijzen vanuit het contactoverzicht door dezelfde procedure te volgen.

Het aantal sectoren dat u aan het contact hebt toegewezen, wordt weergegeven in het veld **Aantal sectoren** in het gedeelte **Segmentatie** op de pagina **Contact**.

Nadat u sectoren hebt toegewezen aan de contacten, kunt u deze gegevens gebruiken om contacten voor de segmenten te selecteren. Zie voor meer informatie [Contacten toevoegen aan segmenten](marketing-add-contact-segment.md).

## <a name="see-also"></a>Zie ook
[Contacten maken](marketing-create-contact-companies.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
