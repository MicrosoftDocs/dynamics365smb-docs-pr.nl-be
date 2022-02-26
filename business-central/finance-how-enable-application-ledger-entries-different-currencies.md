---
title: Posten vereffenen in verschillende valuta's
description: U kunt posten in meerdere valuta's vereffenen, bijvoorbeeld als u verkoopt in een bepaalde valuta en een betaling in een andere ontvangt.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.search.form: 148, 460
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 9b2d1f66ff5b43832fada681320a99ef2b7c06bf
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/14/2022
ms.locfileid: "7971131"
---
# <a name="enable-application-of-ledger-entries-in-different-currencies"></a>Vereffening van posten in verschillende valuta's inschakelen

Als de betaling in een andere valuta dan de valuta van de inkoop wordt ingediend, kunt u de betaling met de inkoop vereffenen.

Als u aan een klant verkoopt in een bepaalde valuta en een betaling in een andere valuta ontvangt, kunt u de betaling ook vereffenen met de verkoopfactuur.

In de volgende procedure wordt beschreven hoe u dit instelt voor leveranciersposten op de pagina **Inkoopinstellingen**. De instelling is soortgelijk voor klantenposten op de pagina **Verkoopinstellingen**.

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a>Vereffening van leveranciersposten in verschillende valuta's inschakelen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Inkoopinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer een van de volgende opties in het veld **Valuta's vereffenen**.

| Optie | Omschrijving |
| --- | --- |
| Geen |De vereffening tussen valuta's is niet toegestaan. |
| EMU |De vereffening tussen EMU-valuta's is toegestaan. |
| Alle |De vereffening tussen alle valuta's is toegestaan. |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a>Grootboekrekeningen voor afrondingsverschillen bij valutaberekeningen instellen

Als u posten in verschillende valuta's vereffent, moet u instellen naar welke grootboekrekening u de afrondingsverschillen wilt boeken.  

> [!NOTE]  
> U moet de grootboekrekeningen instellen voordat u de taak kunt voltooien. Zie voor meer informatie [Het grootboek en het rekeningschema begrijpen](finance-general-ledger.md).

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Klantboekingsgroepen** in en kies vervolgens de gerelateerde koppeling.  
2. In de velden **Afr.-rek. valutavereff. (Deb.)** en  **Afr.-rek. val.-vereff. (Cred.)** voert u de grootboekrekeningen waarnaar u de afrondingsverschillen wilt boeken in.  
3. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Leveranciersboekingsgroepen** in en kies vervolgens de gerelateerde koppeling.  
4. In de velden **Afr.-rek. valutavereff. (Deb.)** en  **Afr.-rek. val.-vereff. (Cred.)** voert u de grootboekrekeningen waarnaar u de afrondingsverschillen wilt boeken in.  

## <a name="see-also"></a>Zie ook

[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Tegoeden beheren](receivables-manage-receivables.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]