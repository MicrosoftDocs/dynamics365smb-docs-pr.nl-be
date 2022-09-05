---
title: Vooruitbetalingsfacturen maken
description: Leer omgaan met situaties waarin u of uw leverancier vooruitbetaling vereist. Gebruik de standaardpercentages voor elke verkoop- of inkoopregel, of u kunt het bedrag naar wens aanpassen.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 42, 50, 9305, 9307
ms.date: 12/02/2021
ms.author: edupont
ms.openlocfilehash: 620a1af0deff6f9615b38706dd3f53f3db285008
ms.sourcegitcommit: 38b1272947f64a473de910fe81ad97db5213e6c3
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 08/29/2022
ms.locfileid: "9362106"
---
# <a name="create-prepayment-invoices"></a>Vooruitbetalingsfacturen maken

Als u wilt dat klanten betalen voordat u hun order verzendt, kunt u de vooruitbetalingsfuncties gebruiken. Hetzelfde geldt als uw leverancier van u verlangt dat u een betaling doet voordat zij een order naar u verzenden.  

U kunt het vooruitbetalingsproces starten wanneer u een verkoop- of inkooporder maakt. Als u een standaard vooruitbetalingspercentage hebt voor een artikel in de order of voor de klant of leverancier, wordt dat percentage automatisch opgenomen in de resulterende vooruitbetalingsfactuur. U kunt ook een percentage voor vooruitbetaling opgeven voor het hele document.

Nadat u een verkoop- of inkooporder hebt gemaakt, kunt u er een vooruitbetalingsfactuur voor maken. Gebruik de standaardpercentages voor elke verkoop- of inkoopregel, of u pas het bedrag naar wens aan. U kunt bijvoorbeeld een totaalbedrag specificeren voor de volledige order.  

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

    Als u een standaard vooruitbetalingspercentage hebt opgegeven voor de klant of op het sneltabblad **Vooruitbetaling** voor dit document, wordt deze waarde naar elke regel gekopieerd. U kunt de inhoud van het veld **Vooruitbetaling %** op de regel wijzigen.  

    > [!TIP]
    > Als u het veld **Vooruitbetaling %** niet ziet, kunt u het toevoegen via personalisatie.  Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.

4. Als u het totale vooruitbetalingsbedrag wilt weergeven, kiest u de actie **Statistieken**.

    Als u het totale vooruitbetaalde bedrag voor de order wilt aanpassen, kunt u de inhoud van het veld **Vooruitbetaling** op de pagina **Verkooporderstatistiek** wijzigen.  

    Als het veld **Prijzen inclusief btw** is geselecteerd, kan het veld **Vooruitbetalingsbedrag incl. btw** worden bewerkt.  

    Als u de inhoud van het veld **Vooruitbetalingsbedrag** wijzigt, wordt het bedrag proportioneel verdeeld over alle regels, met uitzondering van de regels met een **0** in het veld **Vooruitbetaling %**.  

5. Als u een testrapport wilt afdrukken voordat u de vooruitbetalingsfactuur boekt, kiest u de actie **Vooruitbetaling** en kiest u vervolgens de actie **Testrapport vooruitbetaling**.  
6. Als u de vooruitbetalingsfactuur wilt boeken, kiest u de actie **Vooruitbetaling** en kiest u vervolgens de actie **Vooruitbetalingsfactuur boeken**.  

    Als u de vooruitbetalingsfactuur wilt boeken en afdrukken, kiest u de actie **Vooruitbetalingsfactuur boeken en afdrukken**.  

U kunt andere vooruitbetalingsfacturen verzenden voor de order. Als u nog een factuur wilt verzenden, verhoogt u het vooruitbetalingsbedrag op een of meer regels, past u zo nodig de documentdatum aan en boekt u de vooruitbetalingsfactuur. Er wordt een nieuwe factuur gemaakt voor het verschil tussen de tot nu toe gefactureerde vooruitbetalingsbedragen en het nieuwe vooruitbetalingsbedrag.  

> [!NOTE]  
> Als u zich in Noord-Amerika bevindt, kunt u het vooruitbetalingspercentage niet wijzigen nadat de vooruitbetalingsfactuur is geboekt. Dit wordt voorkomen in de Noord-Amerikaanse versie van [!INCLUDE[prod_short](includes/prod_short.md)] omdat de berekening van de sales tax anders niet correct is.  

 Als u klaar bent om de rest van de factuur te boeken, boekt u deze net zoals andere facturen. Het vooruitbetalingsbedrag wordt automatisch afgetrokken van het verschuldigde bedrag.  

## <a name="update-the-status-of-prepaid-orders-and-invoices-automatically"></a>De status van vooruitbetaalde orders en facturen automatisch bijwerken

U kunt de verwerking van orders en facturen versnellen door taakwachtrijen in te stellen die automatisch de status van die documenten bijwerken. Wanneer een vooruitbetalingsfactuur is betaald, kunnen de items in de wachtrij automatisch de documentstatus wijzigen van **In afwachting van vooruitbetaling** in **Vrijgegeven**. Wanneer u de opdrachten in de wachtrij instelt, zijn de codeunits die u moet gebruiken: **383 Verkopen wachtend op vooruitbetaling bijwerken** en **383 Inkopen wachtend op vooruitbetaling bijwerken**. We raden u aan de items zo te plannen dat ze regelmatig worden uitgevoerd, bijvoorbeeld elke minuut. Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md).

## <a name="see-related-training-at-microsoft-learn"></a>Zie gerelateerde training op [Microsoft Learn](/learn/modules/prepayment-invoices-dynamics-365-business-central/)

## <a name="see-also"></a>Zie ook

[Vooruitbetalingen factureren](finance-invoice-prepayments.md)  
[Procedure: Vooruitbetalingen verkoop instellen en factureren](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Uw werkruimte personaliseren](ui-personalization-user.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]