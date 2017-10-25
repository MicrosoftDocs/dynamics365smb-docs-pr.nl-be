---
title: "Statische toewijzingen op basis van de verdeelsleutel definiëren | Microsoft Docs"
description: De methode voor statische toewijzingen baseert zich op een vaste waarde voor bijvoorbeeld gebruikte vierkante meters of een vastgestelde verdeelsleutel, zoals 5:2:4.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b48d7f73b640b98d0cdab6e2e7e7486a3bdb39db
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="scenario-example-defining-static-allocations-based-on-allocation-ratio"></a>Voorbeeld scenario: statische toewijzingen op basis van de verdeelsleutel definiëren
De methode voor statische toewijzingen baseert zich op een vaste waarde voor bijvoorbeeld gebruikte vierkante meters of een vastgestelde verdeelsleutel, zoals 5:2:4.  

In dit onderwerp wordt beschreven hoe u drie nieuwe verdeeldoelen voor kostenobjecten kunt definiëren voor de verdelingsbron van kostenplaats PROD met behulp van de vastgestelde verdeelsleutel 5: 2: 4. De drie doelkostenobjecten zijn ACCESSO, VERF en TOEBEHOREN.  

> [!NOTE]  
>  In het voorbeeld worden de demogegevens in de [!INCLUDE[d365fin](includes/d365fin_md.md)] gebruikt.  

## <a name="to-define-the-allocation-source-prod-cost-center-on-the-general-fasttab"></a>De verdelingsbron van kostenplaats PROD op het sneltabblad Algemeen definiëren  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Kostenverdeling** in en klik vervolgens op de gerelateerde koppeling.  
2.  Kies in het venster **Kostenverdeling** de actie **Nieuw**.  
3.  Druk in het veld **ID** op Enter of voer een id in.  
4.  Geef **1** op in het veld **Niveau**.  
5.  Voer in de velden **Geldig vanaf** en **Geldig tot** juiste datums in.  
6.  Voer in het veld **Kostenplaatscode** **PROD** in.  
7.  Voer in het veld **Credit naar kostensoort** het kostensoort **9903** in.  

## <a name="to-define-the-allocation-target-cost-objects-on-the-lines-fasttab"></a>Verdeeldoelen voor kostenobjecten op de sneltabblad Regels definiëren  

1.  Voer op de eerste regel in het veld **Doelkostensoort** **9903** in.  
2.  Selecteer op de eerste regel in het veld **Doelkostenobject** **ACCESSO**.  
3.  Selecteer op de eerste regel in het veld **Verdelingsdoelsoort** de optie **Alle kosten** om te definiëren hoe te betalen kosten moeten worden toegewezen.  
4.  Op de eerste regel in het veld **Basis** selecteert u **Statisch** om de statische toewijzingsmethode te gebruiken.  
5.  Op de eerste regel in het veld **Deel** voert u de verdeelsleutel **5** in.  
6.  Voer op de tweede regel in het veld **Doelkostensoort** **9903** in.  
7.  Selecteer op de tweede regel in het veld **Doelkostenobject** **PAINT**.  
8.  Selecteer op de tweede regel in het veld **Verdelingsdoelsoort** de optie **Alle kosten** om te definiëren hoe te betalen kosten moeten worden toegewezen.  
9. Op de tweede regel in het veld **Basis** selecteert u **Statisch** om de statische toewijzingsmethode te gebruiken.  
10. Op de tweede regel in het veld **Deel** voert u de verdeelsleutel **2** in.  
11. Voer op de derde regel in het veld **Doelkostensoort** **9903** in.  
12. Selecteer op de derde regel in het veld **Doelkostenobject** **FITTINGS**.  
13. Selecteer op de derde regel in het veld **Verdelingsdoelsoort** de optie **Alle kosten** om te definiëren hoe te betalen kosten moeten worden toegewezen.  
14. Op de derde regel in het veld **Basis** selecteert u **Statisch** om de statische toewijzingsmethode te gebruiken.  
15. Op de derde regel in het veld **Deel** voert u de verdeelsleutel **4** in.  

> [!IMPORTANT]  
>  [!INCLUDE[d365fin](includes/d365fin_md.md)] berekent automatisch het veld **Percentage** met een percentage dat wordt bepaald door alle drie de verdeelsleutels die zijn ingevoerd in het veld **Deel** voor alle drie de regels.  

## <a name="see-also"></a>Zie ook  
[Procedure: een verdelingsbron en verdeeldoelen instellen.](finance-how-to-set-up-allocation-source-and-targets.md)   
[Kosten definiëren en toewijzen](finance-define-and-allocate-costs.md)   
[Voorbeeldscenario: dynamische toewijzingen op basis van de verkochte artikelen definiëren](finance-scenario-example-defining-dynamic-allocations-based-on-items-sold.md)   
[Kosten definiëren en toewijzen](finance-define-and-allocate-costs.md)

