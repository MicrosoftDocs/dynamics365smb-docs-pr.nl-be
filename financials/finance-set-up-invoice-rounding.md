---
title: Factuurafronding instellen | Microsoft Docs
description: U kunt factuurbedragen afronden wanneer u facturen maakt. Volgens lokale voorschriften of gebruiken moet de factuur mogelijk op een specifieke manier worden afgerond, bijvoorbeeld op een bedrag dat door 0,05 kan worden gedeeld.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/15/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: ceebeeac325c00d6aef25d8ca51fcfee1ab4e1d5
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-invoice-rounding"></a>Factuurafronding instellen
Als u factuurbedragen moet afronden wanneer u facturen maakt, kunt u de automatische afrondingsfunctie gebruiken. Wanneer een factuur wordt afgerond, wordt een extra regel met het afrondingsbedrag toegevoegd. Deze regel wordt tegelijk met andere factuurregels geboekt.

> [!NOTE]  
>  Volgens lokale voorschriften of gebruiken moet de factuur mogelijk op een specifieke manier worden afgerond, bijvoorbeeld op een bedrag dat door 0,05 kan worden gedeeld.  
  
Als u automatische factuurafronding wilt gebruiken, moet u het volgende doen:  
  
* Opgeven naar welke grootboekrekeningen de afrondingsverschillen worden geboekt.  
* Regels voor afrondingsfacturen in lokale en vreemde valuta's instellen.  
* De functie activeren.  
  
> [!NOTE]  
>  U kunt factuurbedragen niet alleen afronden met de functies voor factuurafronding, maar ook met de functie voor prijsafronding en de functie voor bedragafronding.  
 
## <a name="set-up-general-ledger-accounts-for-invoice-rounding-differences"></a>Grootboekrekeningen voor factuurafrondingsverschillen instellen
Als u de functie voor automatische factuurafronding wilt gebruiken, moet u de grootboekrekening(en) instellen waarnaar de afrondingsverschillen moeten worden geboekt. Als u dit wilt doen, moet u Btw-productboekingsgroepen instellen. Zie voor meer informatie [Btw instellen](finance-setup-vat.md).  
  
### <a name="to-set-up-general-ledger-accounts-for-invoice-rounding-differences"></a>Grootboekrekeningen voor factuurafrondingsverschillen instellen  
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Rekeningschema** in en klik vervolgens op de gerelateerde koppeling.  
2. Stel de rekening op de pagina **Rekeningschema** in en geef deze de naam **Factuurafronding** of iets dergelijks. [!INCLUDE[d365fin](includes/d365fin_md.md)] gebruikt de rekeningnaam als tekst voor facturen die worden afgerond.  
3. Afhankelijk van of u btw gebruikt of sales tax, kiest u in de velden **Btw-productboekingsgroep** of **Btw-prod.-boekingsgroep** een boekingsgroep voor afgeronde bedragen. U wilt wellicht een nieuwe groepcode instellen die u kunt gebruiken voor factuurafronding.
4. Laat de velden **Algemeen boekingssoort**, en **Btw-bedrijfsboekingsgroep** of **Btw-bedr.-boekingsgroep** leeg. <!-- Why do we say to leave these blank, when there are a lot of other fields we also leave blank but don't mention? -->  
  
U kunt nu de factuurafrondingsrekening toewijzen aan boekingsgroepen in het venster **Leveranciersboekingsgroepen**.  <!-- Why only the vendor posting groups? -->

## <a name="set-up-rounding-for-foreign-and-local-currencies"></a>Afronding instellen voor vreemde en lokale valuta's
Voordat u de automatische factuurafrondingsfunctie kunt gebruiken, moet u afrondingsregels instellen voor vreemde en lokale valuta's.

### <a name="to-set-up-rounding-for-foreign-currencies"></a>Afronding instellen voor vreemde valuta's  
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Valuta's** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies op de pagina **Valuta's** de vreemde valuta om de **valutakaart** te openen en vul de velden **Bedragafrondingsprecisie**, **Prijsafrondingsprecisie**, **Factuurafrondingsprecisie** en **Factuurafrondingsmethode** in.
  
### <a name="to-set-up-rounding-for-your-local-currency"></a>Afronding instellen voor uw lokale valuta
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Grootboekinstellingen** in en klik vervolgens op de gerelateerde koppeling.  
2. Vul op de pagina **Boekhoudinstellingen** op het sneltabblad **Algemeen** de velden **Factuurafr.-precisie** en **Factuurafr.-methode** in.  

## <a name="activate-the-invoice-rounding-function"></a>Functie voor factuurafronding inschakelen  
Om ervoor te zorgen dat verkoop- en inkoopfacturen automatisch worden afgerond, moet u de functie voor factuurafronding inschakelen. U kunt factuurafronding apart instellen voor verkoopfacturen en inkoopfacturen.

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Instellingen van verkoop en tegoeden** of **Inkoopinstellingen** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies op het sneltabblad **Algemeen** het selectievakje **Factuurafronding**.  
  
## <a name="see-also"></a>Zie ook  
[Verkopen factureren](sales-how-invoice-sales.md)  
[Inkopen vastleggen](purchasing-how-record-purchases.md)
