---
title: Jaareinde-ultimopost controleren en boeken | Microsoft Docs
description: Beschrijft hoe u het dagboek opent dat u hebt opgegeven in de batchverwerking Afsluiten WenV-rekening en vervolgens de jaareinde-ultimopost controleert en boekt.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 04/01/2020
ms.author: jswymer
ms.openlocfilehash: 1fa624ecda5914c0ba4e395025f051bc5d8cc457
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3191751"
---
# <a name="post-the-year-end-closing-entry"></a>De jaareinde-ultimopost boeken
Nadat u de batchverwerking **Afsluiten WenV-rekening** hebt gebruikt om de jaareinde-ultimopost of -posten te boeken, moet u het dagboek openen dat u in de batchverwerking hebt opgegeven en vervolgens de posten herzien en boeken.

## <a name="to-post-the-year-end-closing-entry"></a>De jaareinde-ultimopost boeken
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Dagboek** in en kies de desbetreffende koppeling.
2. Selecteer op de pagina **Diversendagboek** in het veld **Batchnaam** de batch die de ultimoposten bevat.
3. Controleer de posten.
4. Kies de actie **Boeken** om het dagboek te boeken.

> [!NOTE]  
>   Als een fout wordt gedetecteerd, wordt een foutbericht weergegeven. Als de boeking is geslaagd, worden de geboekte posten uit het dagboek gehaald. Nadat de boeking is voltooid, wordt een post geboekt in elke resultatenrekening zodat het saldo nul wordt en het jaarresultaat wordt overgebracht naar de balans.

## <a name="see-also"></a>Zie ook
[Boekhoudperioden afsluiten](year-close-account-periods.md)  
[Boeken afsluiten](year-close-books.md)  
[Afsluiten WenV-rekening](year-close-income-statement.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
