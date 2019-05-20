---
title: Zakenrelatiecodes definiëren voor contacten | Microsoft Docs
description: Gebruik zakenrelaties in Business Central om met marketing te helpen en de zakenrelatie aan te geven die u hebt met uw prospects, cliënten, en klanten, bijvoorbeeld, een bank- of serviceleverancier.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: marketing, prospect, contact, client, customer
ms.date: 04/01/2019
ms.author: jswymer
redirect_url: marketing-create-contact-companies
ms.openlocfilehash: ffeb19820b29453750ca9c03258d455dddff287c
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239349"
---
# <a name="setting-up-business-relations-on-contacts"></a>Bedrijfsrelaties instellen voor contacten
U kunt zakenrelaties gebruiken om de zakenrelatie aan te geven die u hebt met uw contacten bijvoorbeeld een prospect, bank, serviceleverancier, enzovoort.

Zakenrelaties gebruiken voor contacten is een proces van twee stappen. Eerst definieert u de zakenrelatiecode. U hoeft deze stap slechts eenmaal uit te voeren voor elke zakenrelatie. Als u een zakenrelatie hebt, kunt u beginnen de code toe te wijzen aan contactbedrijven.

> [!NOTE]  
>   Als u de contacten wilt synchroniseren met leveranciers, klanten of bankrekeningen in een ander onderdeel van de toepassing, kunt u een zakenrelatie instellen.

## <a name="to-define-a-business-relation-code"></a>Een zakenrelatiecode definiëren
De zakenrelatiecode geeft een categorie of soort aan van de zakenrelatie, zoals BANK of JURIDISCH. U kunt meerdere zakenrelatiecodes hebben. Als u de zakenrelatie wilt definiëren, gebruikt u de pagina **Zakenrelaties**.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Zakenrelaties** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw** en vul een code en een beschrijving in. De code kan maximaal uit 11 tekens bestaan en kan elke combinatie zijn van cijfers en letters.

## <a name="AssignBusRelContact"></a> Zakenrelaties toewijzen aan contacten
U kunt geen zakenrelaties toewijzen aan een contactpersoon, alleen aan contactbedrijven.

1. Open het contact.
2. Kies de actie **Bedrijf** en kies vervolgens de actie **Zakenrelaties**.

    De pagina **Zakenrelaties (Relatie)** wordt weergegeven.
3. Selecteer in het veld **Zakenrelatiecode** de zakenrelatie die u wilt toewijzen.

Herhaal deze stappen om het gewenste aantal zakenrelaties toe te wijzen. U kunt zakenrelaties ook toewijzen in het contactoverzicht door dezelfde procedure te volgen.

Het aantal zakenrelaties dat u aan het contact hebt toegewezen, wordt weergegeven in het veld **Aantal zakenrelaties** in het gedeelte **Segmentatie** van de pagina **Contact**.

Nadat u zakenrelaties hebt toegewezen aan de contacten, kunt u deze gegevens gebruiken om contacten voor de segmenten te selecteren. Zie voor meer informatie [Contacten toevoegen aan segmenten](marketing-add-contact-segment.md).

## <a name="see-also"></a>Zie ook
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
