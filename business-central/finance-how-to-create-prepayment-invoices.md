---
title: Vooruitbetalingsfacturen maken
description: Leer omgaan met situaties waarin u of uw leverancier vooruitbetaling vereist. Gebruik de standaardpercentages voor elke verkoop- of inkoopregel, of u kunt het bedrag naar wens aanpassen.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 42, 50, 9305, 9307
ms.date: 12/02/2021
ms.author: edupont
ms.openlocfilehash: ebce3f22b4977b9dfca506ce536abb8c7e5ad46b
ms.sourcegitcommit: 2ab6709741be16ca8029e2afadf19d28cf00fbc7
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/14/2022
ms.locfileid: "7972030"
---
# <a name="create-prepayment-invoices"></a>Vooruitbetalingsfacturen maken

Als u van uw klanten wilt dat ze betalen voordat u een bestelling naar hen verzendt, kunt u de vooruitbetalingsfunctie gebruiken. Hetzelfde geldt als uw leverancier van u verlangt dat u een betaling doet voordat zij een bestelling naar u verzenden.  

U kunt het vooruitbetalingsproces starten wanneer u een verkoop- of inkooporder maakt. Als u een standaard vooruitbetalingspercentage heeft voor een bepaald artikel in de order of voor de klant of leverancier, wordt dat automatisch opgenomen in de resulterende vooruitbetalingsfactuur. U kunt ook een percentage voor vooruitbetaling opgeven voor het hele document.

Nadat u een verkoop- of inkooporder hebt gemaakt, kunt u een vooruitbetalingsnota maken. U kunt de standaardpercentages gebruiken voor elke verkoop- of inkoopregel, of u kunt het bedrag naar wens aanpassen. U kunt bijvoorbeeld een totaalbedrag opgeven voor de hele order.  

In de volgende procedure wordt beschreven hoe u een vooruitbetaling voor een verkooporder factureert. De stappen zijn vergelijkbaar voor inkooporders.  

## <a name="to-create-a-prepayment-invoice"></a>Een vooruitbetalingsfactuur maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.  
2. Maak een nieuwe verkooporder voor de relevante klant. Zie [Producten verkopen](sales-how-sell-products.md) voor meer informatie.  

    Op het sneltabblad **Vooruitbetaling** geeft het veld **Vooruitbetaling %** het percentage aan dat moet worden gebruikt om het vooruitbetalingsbedrag te berekenen. Als er een standaard vooruitbetalingspercentage is op de klantenkaart, wordt het veld automatisch ingevuld. U kunt het percentage wijzigen. <!--This percentage is applied to lines where the item on that line does not already specify a prepayment percentage. The prepayment percentage is only copied from the header to lines that do not copy the default prepayment percentage from the item.-->  

    Kies het veld **Vooruitbetaling comprimeren** als u regels op de vooruitbetalingsfactuur wilt maken die regels uit de verkooporder combineren als:  

    - Ze hebben dezelfde grootboekrekening voor vooruitbetalingen zoals bepaald door de boekingsgroepinstellingen.  
    - Ze hebben dezelfde dimensies.  

    Als u een vooruitbetalingsfactuur wilt opgeven met één regel voor elke verkooporderregel die een vooruitbetalingspercentage heeft, kiest u het veld **Vooruitbetaling comprimeren** niet.  

    De vervaldatum voor de vooruitbetaling wordt automatisch berekend op basis van de waarde van de **Code betalingscond. vooruitbetaling**.

3. Vul de verkoopregels in.  

    Als u een standaard vooruitbetalingspercentage heeft opgegeven voor de klant of op het sneltabblad **Vooruitbetaling** voor dit document, wordt deze waarde naar elke regel gekopieerd. U kunt de inhoud van het veld **Vooruitbetaling %** op de regel wijzigen.  

    > [!TIP]
    > Als u het veld **Vooruitbetaling %** niet ziet, kunt u het toevoegen via personalisatie.  Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.

4. Als u het totale vooruitbetalingsbedrag wilt weergeven, kiest u de actie **Statistieken**.

    Als u het totale vooruitbetaalde bedrag voor de order wilt aanpassen, kunt u de inhoud van het veld **Vooruitbetaling** op de pagina **Verkooporderstatistiek** wijzigen.  

    Als het veld **Prijzen inclusief btw** is geselecteerd, kan het veld **Vooruitbetalingsbedrag incl. btw** worden bewerkt.  

    Als u de inhoud van het veld **Vooruitbetalingsbedrag** wijzigt, wordt het bedrag proportioneel verdeeld over alle regels, met uitzondering van de regels met een **0** in het veld **Vooruitbetalingsbedrag %**.  

5. Als u een testrapport wilt afdrukken voordat u de vooruitbetalingsfactuur boekt, kiest u de actie **Vooruitbetaling** en kiest u vervolgens de actie **Testrapport vooruitbetaling**.  
6. Als u de vooruitbetalingsfactuur wilt boeken, kiest u de actie **Vooruitbetaling** en kiest u vervolgens de actie **Vooruitbetalingsfactuur boeken**.  

    Als u de vooruitbetalingsfactuur wilt boeken en afdrukken, kiest u de actie **Vooruitbetalingsfactuur boeken en afdrukken**.  

U kunt extra vooruitbetalingsnota's verzenden voor de order. Verhoog hiervoor het vooruitbetalingsbedrag op een of meer regels, pas zo nodig de documentdatum aan en boek de vooruitbetalingsfactuur. Er wordt een nieuwe factuur gemaakt voor het verschil tussen de tot nu toe gefactureerde vooruitbetalingsbedragen en het nieuwe vooruitbetalingsbedrag.  

> [!NOTE]  
> Als u zich in Noord-Amerika bevindt, kunt u het vooruitbetalingspercentage niet wijzigen nadat de vooruitbetalingsfactuur is geboekt. Dit wordt voorkomen in de Noord-Amerikaanse versie van [!INCLUDE[prod_short](includes/prod_short.md)] omdat de berekening van de sales tax anders niet correct is.  

 Als u klaar bent om de rest van de factuur te boeken, boekt u deze net zoals andere facturen. Het vooruitbetalingsbedrag wordt automatisch afgetrokken van het verschuldigde bedrag.  

## <a name="see-also"></a>Zie ook

[Vooruitbetalingen factureren](finance-invoice-prepayments.md)  
[Procedure: Vooruitbetalingen verkoop instellen en factureren](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Uw werkruimte personaliseren](ui-personalization-user.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]