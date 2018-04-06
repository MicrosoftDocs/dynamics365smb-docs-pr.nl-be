---
title: Posten vereffenen in verschillende valuta's| Microsoft Docs
description: U kunt posten in meerdere valuta's vereffenen, bijvoorbeeld als u verkoopt in een bepaalde valuta en een betaling in een andere ontvangt.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: multiple currencies, payment, reconcile
ms.date: 01/25/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 960ae581a3f933c6e9c2ed5183944ddf62ca5965
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="enable-application-of-ledger-entries-in-different-currencies"></a>Vereffening van posten in verschillende valuta's inschakelen
Als de betaling in een andere valuta dan de valuta van de inkoop wordt ingediend, kunt u de betaling met de inkoop vereffenen.

Als u aan een klant verkoopt in een bepaalde valuta en een betaling in een andere valuta ontvangt, kunt u de betaling ook vereffenen met de verkoopfactuur.

In de volgende procedure wordt beschreven hoe u dit instelt voor leveranciersposten in het venster **Inkoopinstellingen**. De instelling is soortgelijk voor klantenposten in het venster **Verkoopinstellingen**.

## <a name="to-enable-application-of-vendor-ledger-entries-in-different-currencies"></a>Vereffening van leveranciersposten in verschillende valuta's inschakelen
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Inkoopinstellingen** in en klik vervolgens op de gerelateerde koppeling.
2. Selecteer een van de volgende opties in het veld **Valuta's vereffenen**.

| Optie | Omschrijving |
| --- | --- |
| Geen |De vereffening tussen valuta's is niet toegestaan. |
| EMU |De vereffening tussen EMU-valuta's is toegestaan. |
| Alle |De vereffening tussen alle valuta's is toegestaan. |

## <a name="to-set-up-gl-accounts-for-currency-application-rounding-differences"></a>Grootboekrekeningen voor afrondingsverschillen bij valutaberekeningen instellen  
Als u posten in verschillende valuta's vereffent, moet u instellen naar welke grootboekrekening u de afrondingsverschillen wilt boeken.  

> [!NOTE]  
>  U moet de grootboekrekeningen instellen voordat u de taak kunt voltooien. Zie voor meer informatie [Het grootboek en het rekeningschema begrijpen](finance-general-ledger.md).

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Klantboekingsgroepen** in en klik vervolgens op de gerelateerde koppeling.  
2. In de velden **Afr.-rek. valutavereff. (Deb.)** en  **Afr.-rek. val.-vereff. (Cred.)** voert u de grootboekrekeningen waarnaar u de afrondingsverschillen wilt boeken in.  
3. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Leveranciersboekingsgroepen** in en klik vervolgens op de gerelateerde koppeling.  
4. In de velden **Afr.-rek. valutavereff. (Deb.)** en  **Afr.-rek. val.-vereff. (Cred.)** voert u de grootboekrekeningen waarnaar u de afrondingsverschillen wilt boeken in.  

## <a name="see-also"></a>Zie ook
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Tegoeden beheren](receivables-manage-receivables.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

