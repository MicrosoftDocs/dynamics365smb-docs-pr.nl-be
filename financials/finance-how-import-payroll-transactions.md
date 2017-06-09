---
title: 'Procedure: Salaristransacties importeren| Microsoft Docs'
description: Beschrijft hoe u salarisbetalingen en relateerde transacties van uw leverancier van salarisverwerking in het grootboek kunt importeren.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 03/24/2017
ms.author: SorenGP
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 8d7ee87a80b4de2bc90086c188e5a53291c52683
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-import-payroll-transactions"></a>Procedure: Salaristransacties importeren 
Als u salarisbetalingen en gerelateerde transacties wilt verantwoorden, moet u financiële transacties die zijn uitgevoerd door uw leverancier van salarisverwerking, importeren en boeken naar het grootboek. Hiervoor importeert u eerst een bestand dat u van de leverancier van salarisverwerking ontvangt, in het venster **Fin. dagboek**. Vervolgens kunt u de externe rekeningen in het loonlijstbestand toewijzen aan de betreffende grootboekrekeningen. Als laatste boekt u de loonlijsttransacties op basis van de rekeningtoewijzing.

**Opmerking**: als u deze functionaliteit wilt gebruiken, moet een extensie voor salarisimport zijn geïnstalleerd en ingeschakeld. De extensies voor import van bestanden van Ceridian Payroll en Quickbooks Payroll worden vooraf geïnstalleerd in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Zie [[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met extensies](ui-extensions.md) voor meer informatie.

## <a name="to-import-a-payroll-file"></a>Een salarisbestand importeren
1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Financiële dagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Kies in de relevante diversendagboekbatch de actie **Salaristransacties importeren**. Er wordt een begeleide instelling geopend.
3. Volg de stappen in het venster **Salaristransacties importeren**.

    **Tip**: in de stap over het koppelen van de externe salarisrecords aan uw grootboekrekeningen, worden de koppelingen die u maakt, de volgende keer dat dezelfde records worden geïmporteerd, herinnerd. Hierdoor bespaart u tijd omdat u niet handmatig het **Rekeningnr.** hoeft in te vullen in het dagboek als u terugkerende salaristransacties hebt geïmporteerd.   

    Wanneer u de knop **OK** kiest in de begeleide instelling, wordt het venster **Dagboek** gevuld met regels die de transacties voorstellen die het salarisbestand bevat, en met de relevante rekeningen vooraf ingevuld in de **Grootboekrekening**-velden volgens de koppelingen die u in de instelling kiest.
4. Bewerk of boek de dagboekregels zoals voor andere grootboektransacties. Zie [Procedure: Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.   

## <a name="see-also"></a>Zie ook
[Financiën](finance.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met extensies](ui-extensions.md)  
[Procedure: Werken met diversendagboeken](ui-work-general-journals.md)  

