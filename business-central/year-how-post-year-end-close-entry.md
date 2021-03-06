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
ms.date: 10/01/2020
ms.author: jswymer
ms.openlocfilehash: ca92d9535a9a15d46d93de6febdfd169c3d7d17a
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4755554"
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
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]