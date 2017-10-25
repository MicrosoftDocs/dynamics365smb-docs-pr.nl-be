---
title: 'Procedure: Vooruitbetalingen verkoop instellen en factureren | Microsoft Docs'
description: "Vooruitbetalingen zijn betalingen die worden gefactureerd en geboekt naar een verkoop- of inkoopvooruitbetalingsorder vóór de definitieve facturering. U kunt een aanbetaling vragen voordat u bestelde artikelen fabriceert, of u kunt een betaling vragen voordat u artikelen naar een klant verzendt. Met de vooruitbetalingsfunctionaliteit in [!INCLUDE[d365fin](includes/d365fin_md.md)] kunt u vereiste borgsommen factureren en innen van klanten of kunt u borgsommen overmaken aan leveranciers. Zodoende zorgt u dat alle betalingen worden geboekt tegen een factuur."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 14c4c4a9d4a9ef9149ded77343fa385ae8038f83
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="walkthrough-setting-up-and-invoicing-sales-prepayments"></a>Procedure: Vooruitbetalingen verkoop instellen en factureren
Vooruitbetalingen zijn betalingen die worden gefactureerd en geboekt naar een verkoop- of inkoopvooruitbetalingsorder vóór de definitieve facturering. U kunt een aanbetaling vragen voordat u bestelde artikelen fabriceert, of u kunt een betaling vragen voordat u artikelen naar een klant verzendt. Met de vooruitbetalingsfunctionaliteit in [!INCLUDE[d365fin](includes/d365fin_md.md)] kunt u vereiste borgsommen factureren en innen van klanten of kunt u borgsommen overmaken aan leveranciers. Zodoende zorgt u dat alle betalingen worden geboekt tegen een factuur.  

 Vooruitbetalingsvereisten kunnen worden gedefinieerd voor een klant of leverancier, voor alle artikelen of bepaalde artikelen. Nadat u de benodigde instellingen hebt gemaakt, kunt u vooruitbetalingsfacturen genereren van verkoop- en inkooporders voor het berekende vooruitbetalingsbedrag. U kunt indien nodig de standaardbedragen op de facturen wijzigen. U kunt bijvoorbeeld tevens aanvullende vooruitbetalingsfacturen versturen, als er extra artikelen worden toegevoegd aan de order.  

## <a name="about-this-walkthrough"></a>Informatie over deze procedure  
 In deze procedure komen de volgende scenario's aan de orde:  

-   Vooruitbetalingen instellen  
-   Een order maken waarvoor een vooruitbetaling vereist is  
-   Een vooruitbetalingsfactuur maken  
-   De vooruitbetalingsvereisten voor een order aanpassen  
-   Vooruitbetalingen vereffenen met een order  
-   Het uiteindelijke bedrag van een order met vooruitbetaling factureren  

### <a name="roles"></a>Rollen  
 Deze procedure bevat taken voor de volgende rollen:  

-   Administrateur (Phyllis)  
-   Orderverwerker (Susan)  
-   Administratie vorderingen (Arnie)  

## <a name="story"></a>Scenario  
 Phyllis is administrateur. Ze is administrateur en bepaalt welke klanten een aanbetaling moeten doen voordat artikelen worden gefabriceerd of verzonden. Phyllis stelt [!INCLUDE[d365fin](includes/d365fin_md.md)] in op het automatisch berekenen van vooruitbetalingen.  

 Susan is verkooporderverwerker. Als een klant belt om een order te plaatsen, voert ze de order in het systeem in terwijl ze de klant aan de telefoon heeft. Op deze manier kan ze prijzen en betalingsvoorwaarden meteen met de klant controleren en ze kan de order aanpassen terwijl ze met de klant onderhandelt.  

 Arnie werkt op de afdeling Vorderingen, waar hij facturen en betalingen boekt.  

 In dit scenario stelt Phyllis de vereisten voor vooruitbetalingen in voor de klant Selangorian. Ze baseert dit op hun historische betalingsgegevens en geeft Susan instructies voor het afhandelen van hun orders.  

 Wanneer de klant belt, onderhandelt Susan met de klant totdat een overeenkomst wordt bereikt. Ze kan de vooruitbetaling vervolgens op verschillende manieren berekenen.  

 Nadat Susan de vooruitbetalingsfactuur heeft verstuurd, bestelt te klant een extra artikel. Susan werkt de order bij en maakt een tweede vooruitbetalingsfactuur.  

 Arnie registreert de betaling van de klant en past deze toe op de facturen, waarna hij de uiteindelijke factuur stuurt.  

## <a name="setting-up-prepayments"></a>Vooruitbetalingen instellen  
 Als administrateur stelt Phyllis het systeem in voor het verwerken van vooruitbetalingen van klanten.  

-   Phyllis besluit voor de vooruitbetalingen dezelfde nummerreeks te gebruiken als voor de verkoopfacturen.  
-   Phyllis stelt het programma in om te controleren of vooruitbetalingen zijn vereist voordat de uiteindelijke factuur voor een order wordt verzonden.  
-   Phyllis stelt standaardwaarden in voor een vereist vooruitbetalingspercentage voor bepaalde artikelen en klanten.  

In de volgende procedures wordt beschreven hoe de taken van Phyllis worden uitgevoerd:  

#### <a name="to-set-up-number-series-for-prepayments"></a>Nummerreeks voor vooruitbetalingen instellen  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Instellingen van verkoop en tegoeden** in en klik vervolgens op de gerelateerde koppeling.  
2.  Vouw in het venster **Verkoopinstellingen** het sneltabblad **Nummering** uit.  
3.  Controleer of de nummerreeks voor geboekte vooruitbetalingsfacturen in het veld **Geboekte vooruitbetalingsfactuurnrs.** overeenkomt met de reeks voor geboekte verkoopfacturen (**Factuurnrs. (Geboekt)**) en of de nummerreeks voor geboekte vooruitbetalingscreditnota's (**Geboekte vooruitbetalingscreditnotanrs.**) overeenkomt met de reeks voor geboekte creditnota's (**Creditnotanrs. (Geboekt)**).  

#### <a name="to-block-shipments-for-unpaid-prepayment"></a>Verzendingen blokkeren voor niet voldane vooruitbetalingen  
1.  Schakel in het venster **Verkoopinstellingen** op het sneltabblad **Algemeen** het selectievakje **Vooruitbetaling controleren bij boeken** in.

    Vanaf dit moment kunt geen orders verzenden of factureren waarvoor een niet-betaald vooruitbetalingsbedrag openstaat.  

Phyllis stelt in dat bij klant 20000 standaard een aanbetaling van 30% voor alle orders moet worden gefactureerd. Daarom voert ze een standaardpercentage voor vooruitbetaling in voor de klant.  

Phyllis stelt in dat bij alle klanten een aanbetaling van 20% wordt gefactureerd voor artikel 1100. Klant 20000 heeft een slechte betalingsgeschiedenis. Daarom vereist zij een 40%-vooruitbetaling van klant 20000 voor artikel 1100. In de volgende procedure wordt beschreven hoe de aanbetalingspercentages worden ingesteld.  

#### <a name="to-assign-default-prepayment-percentages-to-customers-and-items"></a>Standaardpercentages voorvooruitbetaling toewijzen aan klanten en artikelen  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Klanten** in en klik vervolgens op de gerelateerde koppeling.  
2.  Open de kaart voor klant 20000 (Selangorian)
3.  Typ **30** in het veld **Vooruitbetaling %**.  
4.  Kies de knop **OK** om de klantenkaart te sluiten.  
5.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Artikelen** in en klik vervolgens op de gerelateerde koppeling.  
6.  Open de kaart voor klant 1100.
7.  Kies de actie **Vooruitbetalingspercentages**.  
8.  Vul twee regels in het venster **Vooruitbetalingspercentages verkoop** als volgt in.  

    |**Verkoopsoort**|**Verkoopscode**|**Artikelnr.**|**Vooruitbetaling %**|  
    |--------------------|--------------------|------------------|----------------------|  
    |**Klant**|**20000**|**1100**|**40**|  
    |**Alle klanten**||**1100**|**20**|  

    > [!IMPORTANT]  
    >  Afhankelijk van uw land/regio, moet u voor artikelen 1000 en 1100 ook een belastinggroepcode opgeven op het sneltabblad **Facturering**.  

9. Sluit alle vensters.  

#### <a name="to-specify-an-account-for-sales-prepayments-in-general-posting-setup"></a>Een vooruitbetalingsrekening verkoop opgeven in de boekingsgroepinstellingen  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Boekingsgroepinstellingen** in en klik vervolgens op de gerelateerde koppeling.  
2.  Selecteer de regel waar de **Bedrijfsboekingsgroep** is ingesteld op **EXPORTEREN** en de **Productboekingsgroep** op **DETAILHANDEL** en kies vervolgens de actie **Bewerken**.  
3.  Geef in het venster **Boekingsgroepinstellingen** in het veld **Vooruitbetalingsrekening** verkoop de desbetreffende rekening op.  
4.  Kies de knop **Ok**.  

## <a name="creating-an-order-that-requires-a-prepayment"></a>Een order maken waarvoor vooruitbetaling is vereist  
 In het volgende scenario maakt Susan, de orderprocessor, een order terwijl ze met een klant praat. Voor de artikelen die de klant bestelt is een vooruitbetaling vereist en de klant heeft in het verleden een aantal keer te laat betaald. Susan heeft daarom de instructie gekregen om een vast bedrag van 2.000 als vooruitbetaling op de order te eisen.  

De klant vraagt of het goed is als hij 35% betaalt, een voorstel waarin Susan zich kan vinden. Zij wijzigt daarom de order.  

Susan maakt de vooruitbetalingsfactuur en verzendt deze naar de klant.  

#### <a name="to-create-a-sales-order-with-a-prepayment"></a>Een verkooporder maken met een vooruitbetaling  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verkooporders** in en klik vervolgens op de gerelateerde koppeling.  
2.  Kies de actie **Nieuw**.  
3.  Selecteer in het veld **Orderklantnr.** de waarde **20000**.  
5.  Accepteer de waarschuwing voor saldo-overschrijding die verschijnt.  
6.  Vul op twee verkoopregels de volgende gegevens in.  

    |**Soort**|**Nr.**|**Aantal**|  
    |--------------|-------------|------------------|  
    |**Artikel**|**1000**|**1**|  
    |**Artikel**|**1100**|**1**|

    De vooruitbetalingsvelden op de verkoopregel zijn standaard verborgen, dus u moet ze weergeven.  

7. Controleer of het veld **Vooruitbetaling %** op de regel voor artikel **1000** op **30** staat. Dit is standaard overgenomen van de verkoopkop die wordt gevuld op basis van de klantkaart.  

    Het veld **Vooruitbetaling %** op de regel voor artikel **1100** is **40**. Dit is het percentage dat u hebt ingevoerd in het venster **Vooruitbetalingspercentages verkoop** voor artikel **1100** en klant **20000**.  

    Zie voor meer informatie [Procedure: Vooruitbetalingen instellen](finance-set-up-prepayments.md).  
8. Kies de actie **Statistieken**.  
9. Op het sneltabblad **Vooruitbetaling** bevat het veld **Vooruitbetalingsregelbedrag excl. btw** het bedrag **1.560**. Als u nu een vooruitbetalingsfavtuur voor de order maakt, is dit het bedrag dat op de factuur wordt weergegeven.  

    In dit scenario heeft Susan instructies ontvangen om een totale vooruitbetaling van 2000 voor te stellen voor de order.  

    > [!IMPORTANT]  
    >  De volgende stap kunt u in uw land\regio misschien niet uitvoeren.  
10. Wijzig het bedrag in het veld **Vooruitbetalingsregelbedrag excl. btw** in **2000** en sluit het venster.  
11. Controleer het veld **Vooruitbetaling %** op de verkoopregels en u ziet dat dit is herberekend als **40,81625**.  

    Bij de herberekening zijn alle regels meegenomen die een vooruitbetalingspercentage hebben dat hoger is dan 0.  

    De klant vraagt nu of het vooruitbetalingspercentage op 35% kan worden gezet. De leidinggevende van Susan keurt de wijziging goed.  

12. Voer in het venster **Verkooporder** in het veld **Vooruitbetaling** de waarde **35** in.  
13. In de waarschuwing die wordt weergegeven, kiest u de knop **Ja**. Er wordt een tarief van 35% toegepast als het betalingspercentage voor de hele order.  
14. Controleer of de regels juist zijn bijgewerkt.  

## <a name="creating-a-prepayment-invoice"></a>Een vooruitbetalingsfactuur maken  
Nadat de juiste vooruitbetalingswaarden voor de order zijn ingevoerd, maakt Susan de vooruitbetalingsfactuur en stuurt ze deze naar de klant.  

#### <a name="to-create-a-prepayment-invoice"></a>Een vooruitbetalingsfactuur maken  

1.  Kies in het venster **Verkooporder** de actie **Vooruitbetalingsfactuur boeken**.  

> [!NOTE]  
>  Susan kan het beste **Vooruitbetalingsfactuur boeken en afdrukken** kiezen en de factuur naar de klant verzenden.  

## <a name="creating-an-additional-prepayment-invoice"></a>Een extra vooruitbetalingsfactuur maken  
De volgende dag belt de klant op en vraagt Susan om een wijziging in de order te maken. De klant wil twee stuks van artikel 1100. Susan opent de order en wijzigt deze en maakt vervolgens een tweede vooruitbetalingsfactuur voor de order en stuurt deze naar de klant.  

#### <a name="to-create-an-additional-prepayment-invoice"></a>Een extra vooruitbetalingsfactuur maken  

1.  Kies in het venster **Verkooporder** de actie **Opnieuw openen**.  
2.  Typ **2** in het veld **Aantal** voor artikel **1100**.  

    Ga naar de velden vooruitbetaling. Het veld **Vooruitbetalingsregelbedrag excl. btw** bevat nu **630** en het veld **Gefactureerd vooruitbetalingsbedrag excl. btw** bevat **315**. Dit geeft aan dat er een extra vooruitbetalingsbedrag bestaat dat nog niet is gefactureerd.  
3.  Als u een factuur wilt boeken voor het extra vooruitbetalingsbedrag, klikt u op **Acties**, wijst u **Boeken** en **Vooruitbetaling** aan en klikt u vervolgens op **Vooruitbetalingsfactuur boeken**.  

## <a name="applying-the-prepayments"></a>Vooruitbetalingen vereffenen  
De klant betaalt het vooruitbetalingsbedrag en Arnie, die op de afdeling Vorderingen werkt, registreert de betaling en vereffent deze met de vooruitbetalingsfacturen.  

#### <a name="to-apply-a-payment-to-the-prepayment-invoices"></a>Een betaling vereffenen met vooruitbetalingsfacturen  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Ontvangstendagboeken** in en klik vervolgens op de gerelateerde koppeling.  
2.  Vul op een dagboekregel de volgende gegevens in.  

    |Veldnaam|Voer in|  
    |----------------|-----------|  
    |**Documentsoort**|**Betaling**|  
    |**Rekeningsoort**|**Klant**|  
    |**Rekeningnr.**|**20000**|  
3. Kies de actie **Posten vereffenen**.  
4.  In het venster **Klantenposten vereffenen** selecteert u de eerste vooruitbetalingsfactuur en vervolgens kiest u de optie **Vereffenings-id instellen**.  
5.  Herhaal de vorige stap voor de tweede vooruitbetaling.  
6.  Kies de knop **OK**.  

    In het bedragveld is nu het totaal van de twee vooruitbetalingsfacturen ingevuld.  

7.  Boek het dagboek.  

## <a name="invoicing-the-remaining-amount"></a>Het resterende bedrag factureren  
Arnie heeft nu doorgekregen dat de artikelen voor de order zijn verzonden en dat de order gereed is voor facturering. Arnie maakt de factuur voor de order.  

#### <a name="to-invoice-the-remaining-amount"></a>Het resterende bedrag factureren  
1. Open de verkooporder.  
2. Kies hierin **Verzenden en factureren** en klik vervolgens de knop **OK**.  

> [!NOTE]  
>  Gewoonlijk heeft de verzendafdeling de verzending al geboekt.  

Arnie kan de geschiedenis bekijken om te controleren of de verkoopfactuur volgens plan is gemaakt.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Geboekte verkoopfacturen** in en klik vervolgens op de gerelateerde koppeling.  

## <a name="next-steps"></a>Volgende stappen  
In dit overzicht hebt u de stappen doorlopen om [!INCLUDE[d365fin](includes/d365fin_md.md)] in te stellen voor het afhandelen van vooruitbetalingen. U hebt gezien hoe u standaard vooruitbetalingspercentages voor klanten en artikelen kunt instellen, en u hebt verschillende methoden gebruikt om de vooruitbetalingen van een order te berekenen. U hebt geprobeerd één totaal vooruitbetalingsbedrag aan de order toe te wijzen en u hebt het vooruitbetalingsbedrag laten berekenen als een percentage van de gehele order.  

Ook hebt u geleerd hoe u een vooruitbetalingsfactuur boekt, een tweede vooruitbetalingsfactuur maakt als de order wordt gewijzigd en de uiteindelijke factuur boekt voor het resterende bedrag.  

De functie voor vooruitbetalingen in [!INCLUDE[d365fin](includes/d365fin_md.md)] maakt het eenvoudig om vooruitbetalingsregels voor klanten en artikelen in te stellen en stelt u in staat om alle betalingen tegen een factuur te boeken.  

## <a name="see-also"></a>Zie ook  
[Vooruitbetalingen factureren](finance-invoice-prepayments.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Procedures voor bedrijfsprocessen](walkthrough-business-process-walkthroughs.md)

