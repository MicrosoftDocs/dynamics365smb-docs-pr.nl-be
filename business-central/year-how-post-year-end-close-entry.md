---
title: De jaareinde-ultimopost boeken
description: Beschrijft hoe u het dagboek opent dat u hebt opgegeven in de batchverwerking Afsluiten WenV-rekening en vervolgens de jaareinde-ultimopost controleert en boekt.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.search.form: 100
ms.date: 06/25/2021
ms.author: edupont
ms.openlocfilehash: 6290bf334e3b309f1b4ed3eec426e6b3f60d6041
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/14/2022
ms.locfileid: "7971770"
---
# <a name="posting-the-year-end-closing-entry"></a>De jaareinde-ultimopost boeken

Nadat u de batchverwerking **Afsluiten WenV-rekening** hebt gebruikt om de jaareinde-ultimopost of -posten te boeken, moet u het dagboek openen dat u in de batchverwerking hebt opgegeven en vervolgens de posten herzien en boeken.  

> [!TIP]
> Afhankelijk van de werkprocessen van uw organisatie, kunt u ervoor kiezen om boekhoudkundige perioden en boekjaren wel of niet af te sluiten in [!INCLUDE [prod_short](includes/prod_short.md)]. Bij de volgende procedure wordt ervan uitgegaan dat u het boekjaar hebt afgesloten met de optie *Boekhoudperioden*, een jaarafsluitingspost hebt gegenereerd met behulp van de batchverwerking **Resultatenrekeningen sluiten** en nu klaar bent om de jaarafsluitingspost te boeken samen met de uitstellende vermogensrekeningboekingen. Uw organisatie kan ervoor kiezen om anders te werken, zoals het boeken van de jaarafsluitingspost als onderdeel van het afsluiten van het boekjaar.

## <a name="to-post-the-year-end-closing-entry"></a>De jaareinde-ultimopost boeken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Dagboek** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer op de pagina **Diversendagboek** in het veld **Batchnaam** de batch die de ultimoposten bevat.
3. Controleer de posten.
4. Kies de actie **Boeken** om het dagboek te boeken.

> [!NOTE]  
> Als een fout wordt gedetecteerd, wordt een foutbericht weergegeven. Als de boeking is geslaagd, worden de geboekte posten uit het dagboek gehaald. Nadat de boeking is voltooid, wordt een post geboekt in elke resultatenrekening zodat het saldo nul wordt en het jaarresultaat wordt overgebracht naar de balans.

## <a name="see-also"></a>Zie ook

[Boekhoudperioden afsluiten](year-close-account-periods.md)  
[Boeken afsluiten](year-close-books.md)  
[Afsluiten WenV-rekening](year-close-income-statement.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]