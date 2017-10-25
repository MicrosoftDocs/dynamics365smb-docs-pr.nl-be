---
title: "Zakenrelatiecodes definiëren voor contacten | Microsoft Docs"
description: "Gebruik zakenrelaties in Financials om met marketing te helpen en de zakenrelatie aan te geven die u hebt met uw prospects, cliënten, en klanten, bijvoorbeeld, een bank- of serviceleverancier."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 7d0f189ac233ea4da72136858a343dfaa7e88883
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="setting-up-business-relations-on-contact-companies"></a>Zakenrelaties instellen voor contactbedrijven
U kunt zakenrelaties gebruiken om de zakenrelatie aan te geven die u hebt met uw contacten bijvoorbeeld een prospect, bank, serviceleverancier, enzovoort.

Zakenrelaties gebruiken voor contacten is een proces van twee stappen. Eerst definieert u de zakenrelatiecode. U hoeft deze stap slechts eenmaal uit te voeren voor elke zakenrelatie. Als u een zakenrelatie hebt, kunt u beginnen de code toe te wijzen aan contactbedrijven.

> [!NOTE]  
>   Als u de contacten wilt synchroniseren met leveranciers, klanten of bankrekeningen in een ander onderdeel van de toepassing, kunt u een zakenrelatie instellen.

## <a name="to-define-a-business-relation-code"></a>Een zakenrelatiecode definiëren
De zakenrelatiecode geeft een categorie of soort aan van de zakenrelatie, zoals BANK of JURIDISCH. U kunt meerdere zakenrelatiecodes hebben. Als u de zakenrelatie wilt definiëren, gebruikt u het venster **Zakenrelaties**.

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Zakenrelaties** in en klik vervolgens op de gerelateerde koppeling.
2. Kies de actie **Nieuw** en vul een code en een beschrijving in. De code kan maximaal uit 11 tekens bestaan en kan elke combinatie zijn van cijfers en letters.

## <a name="AssignBusRelContact"></a> Zakenrelaties toewijzen aan contacten
U kunt geen zakenrelaties toewijzen aan een contactpersoon, alleen aan contactbedrijven.

1. Open het contact.
2. Kies de actie **Bedrijf** en kies vervolgens de actie **Zakenrelaties**.

    Het venster **Zakenrelaties (Relatie)** wordt weergegeven.
3. Selecteer in het veld **Zakenrelatiecode** de zakenrelatie die u wilt toewijzen.

Herhaal deze stappen om het gewenste aantal zakenrelaties toe te wijzen. U kunt zakenrelaties ook toewijzen in het contactoverzicht door dezelfde procedure te volgen.

Het aantal zakenrelaties dat u aan het contact hebt toegewezen, wordt weergegeven in het veld **Aantal zakenrelaties** in het gedeelte **Segmentatie** van het venster **Contact**.

Nadat u zakenrelaties hebt toegewezen aan de contacten, kunt u deze gegevens gebruiken om contacten voor de segmenten te selecteren. Zie voor meer informatie [Procedure: Contacten toevoegen aan segmenten](marketing-add-contact-segment.md).

## <a name="see-also"></a>Zie ook
[Contactbedrijven maken](marketing-create-contact-companies.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

