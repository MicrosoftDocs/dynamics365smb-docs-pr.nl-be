---
title: Niet-betaalde inkoopfacturen wijzigen of annuleren | Microsoft Docs
description: Verklaart hoe u een geboekte inkoopfactuur corrigeert, annuleert of ongedaan maakt, en hoe u automatisch een inkoopcreditnota gemaakt.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 08/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 41f82da76989cd0e9367b4f19b69546304c6de6d
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="correct-or-cancel-unpaid-purchase-invoices"></a>Niet-betaalde inkoopfacturen corrigeren of annuleren
U kunt een geboekte inkoopfactuur corrigeren of annuleren. Dit is handig als u een typefout wilt corrigeren of als u de aankoop in het begin van het orderproces wilt wijzigen.

Als u al hebt betaald voor producten op de geboekte inkoopfactuur, kunt u deze niet corrigeren of annuleren vanuit de geboekte inkoopfactuur zelf. In plaats hiervan moet u handmatig een inkoopcreditnota maken om de aankoop tegen te boeken, optioneel aangestuurd met een inkoopretourorder. Zie voor meer informatie [Inkoopretouren of annuleringen verwerken](purchasing-how-process-purchase-returns-cancellations.md).

In het venster **Geboekte inkoopfacturen** kunt u de knop **Corrigeren** of de knop **Annuleren** kiezen. Wanneer u een geboekte inkoopfactuur wijzigt of annuleert, wordt de corrigerende inkoopcreditnota toegepast op alle algemene grootboekposten en inventarisatieposten die werden gemaakt toen de aanvankelijke inkoopfactuur werd geboekt. Hiermee voert u een tegenboeking uit van de geboekte inkoopfactuur in uw financiële records en laat u de gecorrigeerde inkoopcreditnota staan voor uw auditcontrole. Hieronder wordt het gebruik van **Corrigeren** en **Annuleren** beschreven.

## <a name="to-correct-a-posted-purchase-invoice"></a>Een geboekte inkoopfactuur corrigeren
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Geboekte inkoopfacturen** in en klik vervolgens op de gerelateerde koppeling.  
2. Selecteer de geboekte inkoopfactuur die u wilt corrigeren.  

    > [!NOTE]  
   >   Als het selectievakje **Geannuleerd** is geselecteerd, kunt u de geboekte inkoopfactuur niet corrigeren omdat deze al is gecorrigeerd of geannuleerd.
3. Kies in het venster **Geboekte inkoopfactuur** **Corrigeren**.

    Een nieuwe inkoopfactuur met dezelfde gegevens wordt gemaakt waar u de correctie kunt maken. Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md). Het veld **Geannuleerd** op de eerste geboekte inkoopfactuur is gewijzigd in **Ja**.

    Een inkoopcreditnota wordt automatisch gemaakt en geboekt om de oorspronkelijke geboekte inkoopfactuur nietig te verklaren.
4. Kies **Corrigerende creditnota tonen** om de geboekte inkoopcreditnota weer te geven die de in eerste instantie geboekte inkoopfactuur nietig verklaart.

## <a name="to-cancel-a-posted-purchase-invoice"></a>Een geboekte inkoopfactuur annuleren
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Geboekte inkoopfacturen** in en klik vervolgens op de gerelateerde koppeling.  
2. Selecteer de geboekte inkoopfactuur die u wilt annuleren.

    > [!NOTE]  
   >   Als het selectievakje **Geannuleerd** is geselecteerd, kunt u de geboekte inkoopfactuur niet annuleren omdat deze al is geannuleerd of gecorrigeerd.
3. Kies in het venster **Geboekte inkoopfactuur** **Annuleren**.

    Een inkoopcreditnota wordt automatisch gemaakt en geboekt om de oorspronkelijke geboekte inkoopfactuur nietig te verklaren. Het veld **Geannuleerd** op de eerste geboekte inkoopfactuur is gewijzigd in **Ja**.
4. Kies **Corrigerende creditnota tonen** om de geboekte inkoopcreditnota weer te geven die de in eerste instantie geboekte inkoopfactuur nietig verklaart.

## <a name="see-also"></a>Zie ook
[Inkoop](purchasing-manage-purchasing.md)  
[Inkopen vastleggen](purchasing-how-record-purchases.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

