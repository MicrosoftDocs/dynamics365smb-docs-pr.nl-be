---
title: "Voorbeeldscenario: Dynamische toewijzingen op basis van de verkochte artikelen definiëren | Microsoft Docs"
description: "Dit onderwerp bevat een voorbeeld van het definiëren van toewijzingen met behulp van de methode voor dynamische toewijzing."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 85d58264b14d191389bdf23a792dff7ad30bf9c3
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="scenario-example-defining-dynamic-allocations-based-on-items-sold"></a>Voorbeeld scenario: dynamische toewijzingen op basis van de verkochte artikelen definiëren
Dit onderwerp bevat een voorbeeld van het definiëren van toewijzingen met behulp van de methode voor dynamische toewijzing. In het voorbeeld wijzigt u de dynamische toewijzing van de kosten voor kostenplaats VERKOOP ter ondersteuning van het nieuwe kostenobject IT-APPARATUUR. Pakketten voor IT-APPARATUUR hebben artikelnummers in het bereik van 8904-W t/m 8924-W. De verkoopcijfers van het vorige jaar kunt u gebruiken om het aandeel te berekenen. De toewijzing wordt geboekt op het ondersteunende kostensoort 9903.  

> [!NOTE]  
>  In het voorbeeld worden de demogegevens in de [!INCLUDE[d365fin](includes/d365fin_md.md)] gebruikt.  

## <a name="to-define-dynamic-allocations-based-on-items-sold-in-the-previous-year"></a>Dynamische toewijzingen definiëren op basis van artikelen die het vorige jaar zijn verkocht  

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Kostenverdelingen** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies in het venster **Kostenverdeling** de actie **Nieuw**.  
3.  Druk in het veld **ID** op Enter of voer een id in.  
4.  Geef **1** op in het veld **Niveau**.  
5.  Voer in de velden **Geldig vanaf** en **Geldig tot** juiste datums in.  
6.  Voer in het veld **Kostenplaatscode** **SALES** in.  
7.  Voer in het veld **Credit naar kostensoort** het kostensoort **9903** in.  
8.  Voer in het veld **Doelkostensoort** het kostensoort **9903** in.  
9. Kies in het veld **Doelkostenobject** de optie **Nieuw** om een nieuw kostenobject IT-APPARATUUR te maken en vul waar nodig de velden in. Selecteer **IT-APPARATUUR**. Laat het veld **Doelkostenplaats** leeg.  
10. Selecteer in het veld **Verdelingsdoelsoort** de optie **Alle kosten** om te definiëren hoe alle gecumuleerde kosten moeten worden toegewezen.  
11. In het veld **Basis** selecteert u de toewijzingsbasis **Artikelen verkocht (bedrag)**.  
12. Voer in het veld **Nr.-filter** **8904-W..8924-W** in.  
13. Voer in het veld **Datumfiltercode** **Vorig jaar** in.  
14. Kies de actie **Verdeelsleutel berekenen** om het aandeel te berekenen.  

    > [!IMPORTANT]  
    >  [!INCLUDE[d365fin](includes/d365fin_md.md)] gebruikt de verkoopcijfers van de voorgaande jaren voor het berekenen van een aandeel van 1596,50 LV met 100 procent voor de pakketten voor IT-APPARATUUR. Dit betekent dat alle artikelen die vorig jaar zijn verkocht, worden toegewezen aan kostenobject IT-APPARATUUR.  

## <a name="see-also"></a>Zie ook  
 [Filters instellen voor dynamische toewijzingsgrondslagen](finance-setting-filters-for-dynamic-allocation-bases.md)   
 [Een verdelingsbron en de doelen ervoor instellen](finance-how-to-set-up-allocation-source-and-targets.md)   
 [Kosten definiëren en toewijzen](finance-define-and-allocate-costs.md)   
 [Terminologie in kostprijsboekhouding](finance-terminology-in-cost-accounting.md)   
 [Kostprijsboekhouding](finance-about-cost-accounting.md)

