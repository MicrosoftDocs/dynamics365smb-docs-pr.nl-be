---
title: 'Procedure: Vooruitbetalingsfacturen maken | Microsoft Docs'
description: Leer omgaan met situaties waarin u of uw leverancier vooruitbetaling verlangt.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: dd090720943d0d7271200e087642a80157cbdbbd
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="create-prepayment-invoices"></a>Vooruitbetalingsfacturen maken
Als uw klanten u moeten betalen voordat u een order naar ze verzendt of als uw leverancier wil dat u betaalt voordat een order naar u wordt verzonden, kunt u de functie voor vooruitbetalingen gebruiken.  

Nadat u een verkoop- of inkooporder hebt gemaakt, kunt u een vooruitbetalingsnota maken. U kunt de standaardpercentages gebruiken voor elke verkoop- of inkoopregel, of u kunt het bedrag naar wens aanpassen. U kunt bijvoorbeeld een totaalbedrag opgeven voor de hele order.  

In de volgende procedure wordt beschreven hoe u een vooruitbetaling voor een verkooporder factureert. De stappen zijn vergelijkbaar voor inkooporders.  

## <a name="to-create-a-prepayment-invoice"></a>Een vooruitbetalingsfactuur maken  
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verkooporders** in en klik vervolgens op de gerelateerde koppeling.  
2. Een nieuwe verkooporder maken. Zie [Producten verkopen](sales-how-sell-products.md) voor meer informatie.  

    Op het sneltabblad **Vooruitbetaling**, wordt het veld **vooruitbetaling %** op de kop automatisch ingevuld als de klantenkaart een standaardvooruitbetalingspercentage bevat. U kunt de inhoud van het veld wijzigen. Het vooruitbetalingspercentage wordt alleen vanuit de kop gekopieerd naar regels waarnaar het standaardvooruitbetalingspercentage van het artikel niet wordt gekopieerd.  

    Een vinkje in het veld **Vooruitbetaling comprimeren** betekent dat regels worden gecombineerd op de factuur in de volgende gevallen:  
    - Ze hebben dezelfde grootboekrekening voor vooruitbetalingen zoals bepaald door de boekingsgroepinstellingen.  
    - Ze hebben dezelfde dimensies.  

    Laat het veld leeg als u een vooruitbetalingsnota wilt opgeven met één regel voor elke verkooporderregel die een vooruitbetalingspercentage heeft.  

3. Vul de verkoopregels in.  

    Als er standaardvooruitbetalingspercentages zijn ingesteld voor uw artikelen, wordt de standaardwaarde automatisch naar het veld **Vooruitbetaling %** op de regel gekopieerd. Zo niet, dan wordt het vooruitbetalingspercentage gekopieerd uit de kop. U kunt de inhoud van het veld **Vooruitbetaling %** op de regel wijzigen.  
4. Als u één vooruitbetalingspercentage wilt toepassen op de hele order, wijzigt u het veld **Vooruitbetaling %** op de kop nadat u de regels hebt ingevuld.  
5. Als u het totale vooruitbetalingsbedrag wilt weergeven, kiest u de actie **Statistieken**.

    Als u het totale vooruitbetaalde bedrag voor de order wilt aanpassen, kunt u de inhoud van het veld **Vooruitbetaling** in het venster **Verkooporderstatistiek** wijzigen.  

    Als het veld **Prijzen inclusief btw** is geselecteerd, kan het veld **Vooruitbetalingsbedrag incl. btw** worden bewerkt.  

    Als u de inhoud van het veld **Vooruitbetalingsbedrag** wijzigt, wordt het bedrag proportioneel verdeeld over alle regels, met uitzondering van de regels met een **0** in het veld **Vooruitbetalingsbedrag %**.  
6. Als u een testrapport wilt afdrukken voordat u de vooruitbetalingsfactuur boekt, kiest u de actie **Vooruitbetaling** en kiest u vervolgens de actie **Testrapport vooruitbetaling**.  
7. Als u de vooruitbetalingsfactuur wilt boeken, kiest u de actie **Vooruitbetaling** en kiest u vervolgens de actie **Vooruitbetalingsfactuur boeken**.  

    Als u de vooruitbetalingsfactuur wilt boeken en afdrukken, kiest u de actie **Vooruitbetalingsfactuur boeken en afdrukken**.  

U kunt extra vooruitbetalingsnota's verzenden voor de order. Verhoog hiervoor het vooruitbetalingsbedrag op een of meer regels, pas zo nodig de documentdatum aan en boek de vooruitbetalingsfactuur. Er wordt een nieuwe factuur gemaakt voor het verschil tussen de tot nu toe gefactureerde vooruitbetalingsbedragen en het nieuwe vooruitbetalingsbedrag.  

> [!NOTE]  
>  Als u zich in Noord-Amerika bevindt, kunt u het vooruitbetalingspercentage niet wijzigen nadat de vooruitbetalingsfactuur is geboekt. Dit wordt voorkomen in de Noord-Amerikaanse versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] omdat de berekening van de sales tax anders niet correct is.  

 Als u klaar bent om de rest van de factuur te boeken, boekt u deze net zoals andere facturen. Het vooruitbetalingsbedrag wordt automatisch afgetrokken van het verschuldigde bedrag.  

## <a name="see-also"></a>Zie ook  
[Vooruitbetalingen factureren](finance-invoice-prepayments.md)  
[Procedure: Vooruitbetalingen verkoop instellen en factureren](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

