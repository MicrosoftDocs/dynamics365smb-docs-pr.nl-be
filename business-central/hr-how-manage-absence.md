---
title: Werknemersafwezigheid beheren | Microsoft Docs
description: Beschrijft hoe u werknemersafwezigheid registreert en afwezigheidsstatistieken analyseert.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 1385545ffa32bbf321c90acf1f27b948a41c4644
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3777678"
---
# <a name="manage-employee-absence"></a>Werknemersafwezigheid beheren
Als u de afwezigheid van een werknemer wilt beheren, moet u de afwezigheid registreren op de pagina **Afwezigheidsregistratie**. Het kan dan op verschillende manieren voor analyse- en rapportagedoeleinden worden weergegeven.

U kunt de werknemersafwezigheid weergeven op twee verschillende pagina's:

* Op de pagina **Afwezigheidsregistratie**, waar u alle werknemersafwezigheid registreert met een regel voor elke afwezigheid.
* De pagina **Werknemersafwezigheid**, waar de afwezigheid van slechts één werknemer wordt weergegeven. Dit zijn de gegevens die u hebt ingevoerd op de pagina **Afwezigheidsregistratie**, gefilterd op de specifieke werknemer.

Gebruik daarbij wel altijd dezelfde tijdseenheid (uren of dagen).

## <a name="to-register-employee-absence"></a>Werknemersafwezigheid registreren
U kunt werknemersafwezigheid per dag of met een ander interval dat voldoet aan de behoeften van uw organisatie registreren.

1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport**, voer **Afwezigheidsregistratie** in en klik vervolgens op de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Vul een regel in voor elke werknemersafwezigheid die u wilt registreren.
4. Sluit de pagina.

    > [!Tip]
    > Om duidelijke statistische gegevens te verkrijgen, is het belangrijk dat u steeds dezelfde eenheid (uur of dag) gebruikt bij de registratie van werknemersafwezigheid.

## <a name="to-view-an-individual-employees-absence"></a>Afwezigheid van een individuele werknemer weergeven
1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport**, voer **Werknemers** in en klik vervolgens op de gerelateerde koppeling.
2. Selecteer de betreffende werknemer en kies vervolgens de actie **Afwezigheid**.

    De pagina **Werknemersafwezigheid** wordt geopend met alle afwezigheid, inclusief de begin- en einddatums van de afwezigheid.

## <a name="to-view-an-employees-absence-by-categories"></a>Afwezigheid van een werknemer weergeven per categorie
1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport**, voer **Werknemers** in en klik vervolgens op de gerelateerde koppeling.
2. Selecteer de betreffende werknemer en kies vervolgens de actie **Afwezigheid per categorie**.
3. Vul op de pagina **Werkn.-afwezigh. per categorie** de benodigde filtervelden in en kies vervolgens de actie **Matrix weergeven**.

    De pagina **Matrix voor werknemerafwezigheid per categorie** wordt geopend met alle afwezigheden, opgesplitst op oorzaken van afwezigheid.

## <a name="to-view-all-employee-absences-by-category"></a>Alle werknemersafwezigheid per categorie weergeven
1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport**, voer **Afwezigheidsregistratie** in en klik vervolgens op de gerelateerde koppeling.
2. Kies op de pagina **Afwezigheidsregistratie** de actie **Overzicht per categorie**.
3. Stel op de pagina **Afwezigheid per categorie** in het veld **Werknemerfilter** een filter in om de afwezigheid te bekijken van een individuele werknemer of een gedefinieerde groep werknemers.
4. Kies de actie **Matrix weergeven**.

    De pagina **Matrix voor afwezigheidsoverzicht per categorie** wordt geopend met de afwezigheid van alle werknemers, gesplitst per afwezigheidsreden.

## <a name="to-view-all-employee-absences-by-period"></a>Alle werknemersafwezigheid per periode weergeven
1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport**, voer **Afwezigheidsregistratie** in en klik vervolgens op de gerelateerde koppeling.
   Kies op de pagina **Afwezigheidsregistratie** de actie **Overzicht per periode**.
2. Stel op de pagina **Afwezigheid per periode** in het veld **Afw.-filter** een filter in om werknemersafwezigheid wegens opgegeven afwezigheidsredenen te bekijken.
3. Kies de actie **Matrix weergeven**.

    De pagina **Matrix voor afwezigheidsoverzicht per periode** wordt geopend met de werknemersafwezigheid, gesplitst op periode.

## <a name="see-also"></a>Zie ook
[Human Resources beheren](hr-manage-human-resources.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)
