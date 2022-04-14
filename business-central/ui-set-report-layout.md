---
title: De rapportlay-out instellen
description: Meer informatie over hoe u de lay-out instelt die op een rapport wordt gebruikt bij het bekijken en afdrukken van een rapport.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.search.form: 9652, 9650
ms.date: 03/07/2022
ms.author: jswymer
ms.openlocfilehash: 9cc827630c5acfeba2efc860d8baf67cd31bb404
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8525315"
---
# <a name="setting-the-layout-used-by-a-report"></a>De lay-out instellen die door een rapport wordt gebruikt

> **GELDT VOOR:** Business Central Online, Business Central on-premises releasewave 1 van 2022 en hoger. Ga voor eerdere versies naar [hier](ui-how-change-layout-currently-used-report.md).

Een rapportlay-out bepaalt het uiterlijk van een rapport. Het bepaalt welke gegevensvelden van een rapportgegevensset worden weergegeven, hoe ze zijn gerangschikt, opgemaakt en meer. Een rapport kan meerdere lay-outs hebben, waartussen u indien nodig kunt schakelen.

Wanneer er meerdere bedrijven in de toepassing zijn, worden de lay-outs per bedrijf ingesteld. Dus hetzelfde rapport in het ene bedrijf kan een andere lay-out hebben in een ander bedrijf.

## <a name="get-started"></a>Aan de slag

Er zijn twee manieren om in te stellen welke lay-out een rapport gebruikt. De ene manier is vanaf de pagina **Selectie rapportlay-out**. De andere manier is vanaf de pagina **Rapportlay-outs**. Elke pagina heeft voordelen, bijvoorbeeld: 

- De pagina **Selectie rapportlay-out** toont een lijst met alle rapporten.

  Deze pagina geeft aan wat de huidige lay-out van een rapport is. Bovendien kunt u lay-outs instellen in verschillende bedrijven, zonder dat u hoeft weg te gaan van het bedrijf waarmee u werkt.

- De pagina **Rapportlay-outs** toont alle beschikbare lay-outs voor elk rapport in het huidige bedrijf.

  Het is gemakkelijk om een specifieke lay-out te vinden door de lijst te sorteren of te filteren. Zodra u de lay-out hebt gevonden, kunt u deze instellen voor een rapport met een enkele selectie.

  > [!NOTE]
  > U kunt de pagina **Rapportlay-outs** niet gebruiken voor Word- en RDLC-lay-outs die zijn gemaakt met de verouderde **Aangepaste lay-outs**-functie. U ziet u deze aangepaste lay-outs niet eens vermeld op de pagina **Rapportlay-outs**. Voor deze lay-outs kunt u ze alleen instellen met de pagina **Selectie rapportlay-out**.

## <a name="set-the-layout-from-the-report-layouts-page"></a>De lay-out vanaf de pagina Rapportlay-outs instellen

[!INCLUDE[open-report-layouts-page](includes/open-report-layouts-page.md)]
2. Zoek de lay-out in de lijst, selecteer de lay-out en selecteer vervolgens de actie **Standaard instellen** boven aan de pagina.

## <a name="set-the-layout-from-report-layout-selection-page"></a>De lay-out vanaf de pagina Selectie rapportlay-out instellen

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Selectie rapportlay-out** in en kies vervolgens de gerelateerde koppeling.
  
   De pagina bevat een overzicht van alle rapporten die beschikbaar zijn voor het bedrijf dat in het veld **Bedrijf** boven aan de pagina is aangegeven. Met het veld **Lay-outbeschrijving** wordt de lay-out aangegeven die momenteel door het rapport wordt gebruikt.
2. Stel het veld **Bedrijf** bovenaan in op het bedrijf dat het rapport bevat.
3. Zoek en selecteer het rapport in de lijst en voer een van de volgende stappen uit:

   - Als de lay-out waarnaar u wilt overschakelen van een ander type is dan de huidige lay-out, selecteert u het veld **Lay-outtype** en kiest u vervolgens het type lay-out dat u op het rapport wilt instellen. 
   - Als de lay-out waarnaar u wilt overschakelen van hetzelfde type is als de huidige lay-out, selecteert u de actie **Lay-out selecteren** bovenaan.

4. In de pagina **Rapportlay-outs** selecteert u de lay-out en selecteer vervolgens **OK**.

## <a name="revert-to-the-original-default-layout"></a>Terugkeren naar de oorspronkelijke standaardlay-out

Rapporten zijn ontworpen om standaard een lay-out te gebruiken. U kunt terugschakelen naar de oorspronkelijke standaardlay-out vanaf de pagina **Selectie rapportlay-out**. Selecteer gewoon het rapport en selecteer vervolgens de actie **Standaardselectie herstellen** boven aan de pagina.

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/change-documents-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Rapportlay-outs beheren](ui-manage-report-layouts.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]