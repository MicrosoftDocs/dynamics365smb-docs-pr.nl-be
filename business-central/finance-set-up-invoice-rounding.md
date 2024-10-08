---
title: Factuurafronding instellen
description: 'Als u factuurbedragen moet afronden wanneer u facturen maakt, kunt u de automatische afrondingsfunctie gebruiken die hier wordt uitgelegd.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: '5, 16, 118, 459, 460, 495'
ms.date: 06/10/2024
ms.service: dynamics-365-business-central
---
# <a name="set-up-invoice-rounding"></a>Factuurafronding instellen

Als u factuurbedragen moet afronden wanneer u facturen maakt, kunt u de automatische afrondingsfunctie gebruiken. Wanneer een factuur wordt afgerond, wordt een extra regel met het afrondingsbedrag toegevoegd. Deze regel wordt tegelijk met andere factuurregels geboekt.

> [!NOTE]  
> Lokale regelgeving of lokaal gebruik vereisen mogelijk dat u factuurbedragen op een specifieke manier moet afronden. Bijvoorbeeld tot een bedrag dat deelbaar is door 0,05.  

Als u automatische factuurafronding wilt gebruiken, moet u het volgende doen:  

* Opgeven naar welke grootboekrekeningen de afrondingsverschillen worden geboekt.  
* Regels voor afrondingsfacturen in lokale en vreemde valuta's instellen.  
* De functie activeren.  

> [!NOTE]  
>  U kunt factuurbedragen niet alleen afronden met de functies voor factuurafronding, maar ook met de functie voor prijsafronding en de functie voor bedragafronding.  

## <a name="set-up-general-ledger-accounts-for-invoice-rounding-differences"></a>Grootboekrekeningen voor factuurafrondingsverschillen instellen

Als u de functie voor automatische factuurafronding wilt gebruiken, moet u de grootboekrekening(en) instellen waarnaar de afrondingsverschillen moeten worden geboekt. Als u dit wilt doen, moet u eerst btw-productboekingsgroepen instellen. Zie voor meer informatie [Btw instellen](finance-setup-vat.md).  

### <a name="to-set-up-general-ledger-accounts-for-invoice-rounding-differences"></a>Grootboekrekeningen voor factuurafrondingsverschillen instellen
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Rekeningschema** in en kies de gerelateerde koppeling.  
2. Stel de rekening op de pagina **Rekeningschema** in en geef deze de naam **Factuurafronding** of iets dergelijks. [!INCLUDE[prod_short](includes/prod_short.md)] gebruikt de rekeningnaam als tekst voor facturen die worden afgerond.  
3. Afhankelijk van of u btw gebruikt of sales tax, kiest u in de velden **Btw-productboekingsgroep** of **Btw-prod.-boekingsgroep** een boekingsgroep voor afgeronde bedragen. U wilt wellicht een nieuwe groepscode instellen die u kunt gebruiken voor factuurafronding.
4. Laat de velden **Algemeen boekingssoort**, en **Btw-bedrijfsboekingsgroep** of **Btw-bedr.-boekingsgroep** leeg. <!-- Why do we say to leave these blank, when there are a lot of other fields we also leave blank but don't mention? -->  

U kunt nu de factuurafrondingsrekening toewijzen aan boekingsgroepen in het venster **Leveranciersboekingsgroepen**.  <!-- Why only the vendor posting groups? -->

## <a name="set-up-rounding-for-foreign-and-local-currencies"></a>Afronding instellen voor vreemde en lokale valuta's
Voordat u de automatische factuurafrondingsfunctie kunt gebruiken, moet u afrondingsregels instellen voor vreemde en lokale valuta's.

### <a name="to-set-up-rounding-for-foreign-currencies"></a>Afronding instellen voor vreemde valuta's
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Valuta's** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Valuta's** de vreemde valuta om de **valutakaart** te openen en vul de velden **Bedragafrondingsprecisie**, **Prijsafrondingsprecisie**, **Factuurafrondingsprecisie** en **Factuurafrondingsmethode** in.

### <a name="to-set-up-rounding-for-your-local-currency"></a>Afronding instellen voor uw lokale valuta
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Grootboekinstellingen** in en kies vervolgens de gerelateerde koppeling.  
2. Vul op de pagina **Boekhoudinstellingen** op het sneltabblad **Algemeen** de velden **Factuurafr.-precisie** en **Factuurafr.-methode** in.  

## <a name="activate-the-invoice-rounding-function"></a>Functie voor factuurafronding inschakelen
Om ervoor te zorgen dat verkoop- en inkoopfacturen automatisch worden afgerond, moet u de functie voor factuurafronding inschakelen. U kunt factuurafronding apart instellen voor verkoopfacturen en inkoopfacturen.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopinstellingen** of **Inkoopinstellingen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op het sneltabblad **Algemeen** het selectievakje **Factuurafronding**.  

## <a name="see-also"></a>Zie ook
[Verkopen factureren](sales-how-invoice-sales.md)  
[Inkopen vastleggen](purchasing-how-record-purchases.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
