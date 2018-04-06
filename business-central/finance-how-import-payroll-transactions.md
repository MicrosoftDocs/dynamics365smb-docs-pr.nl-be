---
title: Salaristransacties importeren| Microsoft Docs
description: "Als u salaris wilt beheren, importeert en boekt u financiële transacties vanuit uw salarisprovider naar het grootboek, met behulp van een salarisextensie zoals Ceridian of Quickbooks."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 06/16/2017
ms.author: SorenGP
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b2ee62429f215792f7cf8a651e4a2ce3c1c60a4d
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="import-payroll-transactions"></a>Salaristransacties importeren
Als u salarisbetalingen en gerelateerde transacties wilt verantwoorden, moet u financiële transacties die zijn uitgevoerd door uw leverancier van salarisverwerking, importeren en boeken naar het grootboek. Hiervoor importeert u eerst een bestand dat u van de leverancier van salarisverwerking ontvangt, in het venster **Fin. dagboek**. Vervolgens kunt u de externe rekeningen in het loonlijstbestand toewijzen aan de betreffende grootboekrekeningen. Als laatste boekt u de loonlijsttransacties op basis van de rekeningtoewijzing.

> [!NOTE]  
>   Als u deze functionaliteit wilt gebruiken, moet een extensie voor salarisimport zijn geïnstalleerd en ingeschakeld. De extensies voor import van bestanden van Ceridian Payroll en Quickbooks Payroll worden vooraf geïnstalleerd in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Zie voor meer informatie [[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met extensies](ui-extensions.md).

## <a name="to-import-a-payroll-file"></a>Een salarisbestand importeren
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Dagboeken** in en klik vervolgens op de gerelateerde koppeling.
2. Kies in de relevante diversendagboekbatch de actie **Salaristransacties importeren**. Er wordt een begeleide instelling geopend.
3. Volg de stappen in het venster **Salaristransacties importeren**.

    > [!TIP]  
    >   In de stap over het koppelen van de externe salarisrecords aan uw grootboekrekeningen, worden de koppelingen die u maakt, de volgende keer dat dezelfde records worden geïmporteerd, herinnerd. Hierdoor bespaart u tijd omdat u niet handmatig het veld **Rekeningnr.** in het dagboek moet invullen steeds wanneer u doorlopende loonlijsttransacties hebt geïmporteerd.   

    Wanneer u de knop **OK** kiest in de begeleide instelling, wordt het venster **Dagboek** gevuld met regels die de transacties voorstellen die het salarisbestand bevat, en met de relevante rekeningen vooraf ingevuld in de **Grootboekrekening**-velden volgens de koppelingen die u in de instelling kiest.
4. Bewerk of boek de dagboekregels zoals voor andere grootboektransacties. Zie voor meer informatie [Transacties direct naar het grootboek boeken](finance-how-post-transactions-directly.md).   

## <a name="see-also"></a>Zie ook
[Financiën](finance.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies](ui-extensions.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  

