---
title: Salaristransacties importeren| Microsoft Docs
description: Als u salaris wilt beheren, importeert en boekt u financiële transacties vanuit uw salarisprovider naar het grootboek, met behulp van een salarisextensie zoals Ceridian of Quickbooks.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Ceridian, Quickbooks, salary
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: b2bd2408152cac52be5e2b22e6568600ceeb96f6
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781593"
---
# <a name="import-payroll-transactions"></a>Salaristransacties importeren
Als u salarisbetalingen en gerelateerde transacties wilt verantwoorden, moet u financiële transacties die zijn uitgevoerd door uw leverancier van salarisverwerking, importeren en boeken naar het grootboek. Hiervoor importeert u eerst een bestand dat u van de leverancier van salarisverwerking ontvangt, op de pagina **Fin. dagboek**. Vervolgens kunt u de externe rekeningen in het loonlijstbestand toewijzen aan de betreffende grootboekrekeningen. Als laatste boekt u de loonlijsttransacties op basis van de rekeningtoewijzing.

> [!NOTE]  
>   Als u deze functionaliteit wilt gebruiken, moet een extensie voor salarisimport zijn geïnstalleerd en ingeschakeld. De extensies voor import van bestanden van Ceridian Payroll en Quickbooks Payroll worden vooraf geïnstalleerd in [!INCLUDE[prod_short](includes/prod_short.md)]. Zie voor meer informatie [[!INCLUDE[prod_short](includes/prod_short.md)] aanpassen met extensies](ui-extensions.md).

## <a name="to-import-a-payroll-file"></a>Een salarisbestand importeren
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Financiële dagboeken** in en kies de desbetreffende koppeling.
2. Kies in de relevante diversendagboekbatch de actie **Salaristransacties importeren**. Er wordt een begeleide instelling geopend.
3. Volg de stappen op de pagina **Salaristransacties importeren**.

    > [!TIP]  
    >   In de stap over het koppelen van de externe salarisrecords aan uw grootboekrekeningen, worden de koppelingen die u maakt, de volgende keer dat dezelfde records worden geïmporteerd, herinnerd. Hierdoor bespaart u tijd omdat u niet handmatig het veld **Rekeningnr.** in het dagboek moet invullen steeds wanneer u doorlopende loonlijsttransacties hebt geïmporteerd.   

    Wanneer u de knop **OK** kiest in de begeleide instelling, wordt de pagina **Dagboek** gevuld met regels die de transacties voorstellen die het salarisbestand bevat, en met de relevante rekeningen vooraf ingevuld in de **Grootboekrekening**-velden volgens de koppelingen die u in de instelling kiest.
4. Bewerk of boek de dagboekregels zoals voor andere grootboektransacties. Zie voor meer informatie [Transacties direct naar het grootboek boeken](finance-how-post-transactions-directly.md).   

## <a name="see-also"></a>Zie ook
[Financiën](finance.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] aanpassen met behulp van extensies](ui-extensions.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]