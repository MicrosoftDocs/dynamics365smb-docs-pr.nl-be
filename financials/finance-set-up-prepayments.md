---
title: Vooruitbetalingen instellen | Microsoft Docs
description: "Vooruitbetalingen zijn betalingen die worden gefactureerd en geboekt naar een verkoop- of inkoopvooruitbetalingsorder vóór de definitieve facturering. U vereist mogelijk een borgsom voordat u artikelen produceert in opdracht, of u vereist mogelijk betaling voordat u artikelen naar een klant verscheept. Met de vooruitbetalingsfunctionaliteit kunt u vereiste borgsommen factureren en innen van klanten of kunt u borgsommen overmaken aan leveranciers. Zodoende zorgt u dat alle betalingen worden geboekt tegen een factuur."
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
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 11aef4cb4b1d40568b63662239a26993782201a3
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-prepayments"></a>Procedure: Vooruitbetalingen instellen
Als uw klanten u moeten betalen voordat u een order naar ze verzendt of als uw leverancier wil dat u betaalt voordat een order naar u wordt verzonden, kunt u de functie voor vooruitbetalingen gebruiken. Met de functionaliteit kunt u vereiste borgsommen factureren en innen van klanten of kunt u borgsommen overmaken aan leveranciers, en ervoor zorgen dat alle gedeeltelijke betalingen worden geboekt tegen een factuur. Zie voor meer informatie [Procedure: Vooruitbetalingsfacturen maken](finance-how-to-create-prepayment-invoices.md).

Voor u vooruitbetalingsfacturen kunt boeken, moet u de boekingsrekening instellen in het grootboek en moet u nummerreeksen instellen voor de vooruitbetalingsdocumenten.  

U kunt het percentage van het regelbedrag definiëren dat wordt gefactureerd voor een vooruitbetaling. Nadat u de instellingen hebt gemaakt, kunt u vooruitbetalingsfacturen genereren van verkoop- en inkooporders. U kunt de standaardpercentages gebruiken voor elke verkoop- of inkoopregel, of u kunt de bedragen op de factuur wijzigen zoals gewenst. U kunt bijvoorbeeld een totaalbedrag opgeven voor de hele order.  

Omdat het vooruitbetaalde bedrag bij de koper hoort totdat deze de goederen of diensten heeft ontvangen, moet u grootboekrekeningen instellen waarop de vooruitbetaalde bedragen staan totdat de uiteindelijke factuur wordt geboekt. Vooruitbetaalde verkopen moeten worden vastgelegd op een passivarekening totdat de artikelen worden verzonden. Vooruitbetaalde inkopen moeten worden vastgelegd op een activarekening totdat de artikelen worden ontvangen. Daarnaast moet u een afzonderlijke grootboekrekening instellen voor elke btw-id.

## <a name="to-add-prepayment-accounts-to-the-general-posting-setup"></a>Vooruitbetalingsrekeningen toevoegen aan de boekingsgroepinstellingen  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Boekingsgroepinstellingen** in en klik vervolgens op de gerelateerde koppeling.
2. In het venster **Boekingsgroepinstellingen** vult u de volgende velden in:  

    - **Vooruitbetalingsrekening verkoop**  
    - **Vooruitbetalingsrekening inkoop**  

## <a name="to-set-up-number-series-for-prepayment-documents"></a>Nummerreeks instellen voor vooruitbetalingsdocumenten  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Instellingen van verkoop en tegoeden** in en klik vervolgens op de gerelateerde koppeling.
2. Vul in het venster **Instellingen van verkoop en tegoeden** de volgende velden in:  

   - **Geboekte vooruitbetalingsfactuurnrs.**
   - **Geboekte vooruitbetalingscreditnotanrs.**

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Inkoopinstellingen** in en klik vervolgens op de gerelateerde koppeling.
2. Vul in het venster **Inkoopinstellingen** de volgende velden in:

    - **Geboekte vooruitbetalingsfactuurnrs.**
    - **Geboekte vooruitbetalingscreditnotanrs.**

> [!NOTE]  
>  U kunt dezelfde nummerreeks gebruiken voor vooruitbetalingsnota's en normale facturen, of u kunt verschillende nummerreeksen gebruiken. Als u verschillende reeksen gebruikt, mogen deze elkaar niet overlappen omdat er geen nummers mogen zijn die in beide reeksen voorkomen.  

## <a name="to-set-up-prepayment-percentages-for-items-customers-and-vendors"></a>Vooruitbetalingspercentages instellen voor artikelen, klanten en leveranciers  
Voor een artikel kunt u een standaardvooruitbetalingspercentage instellen voor alle klanten, een specifieke klant of een klantenprijsgroep.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Artikelen** in en klik vervolgens op de gerelateerde koppeling.
2. Selecteer een artikel en kies vervolgens de actie **Vooruitbetalingspercentages**.  
3. Vul in het venster **Vooruitbetalingspercentages verkoop** de benodigde velden in: [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Voor een klant of leverancier kunt u één standaardvooruitbetalingspercentage instellen voor alle artikelen en alle typen verkoopregels. U voert dit op de klanten- of leverancierskaart in.

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Klanten** in en klik vervolgens op de gerelateerde koppeling.
2. Open de kaart voor een klant.
3. Vul het veld **Vooruitbetaling %** in.
4. Herhaal de stappen voor andere voor klanten of leveranciers.  

### <a name="to-determine-which-prepayment-percentage-has-first-priority"></a>Bepalen welk vooruitbetalingspercentage de hoogste prioriteit heeft  
Een order kan een vooruitbetalingspercentage hebben in de verkoopkop en een ander percentage voor de artikelen op de regels. Om te bepalen welk vooruitbetalingspercentage van toepassing is voor elke verkoopregel, zoekt het systeem voor elke verkoopregel in de volgende volgorde naar het vooruitbetalingspercentage. De eerste gevonden standaardwaarde wordt toegepast:  
1. Een vooruitbetalingspercentage voor het artikel op de regel en de klant waarvoor de order is.  
2. Een vooruitbetalingspercentage voor het artikel op de regel en de klantenprijsgroep waar de klant bij hoort.  
3. Een vooruitbetalingspercentage voor het artikel op de regel voor alle klanten.  
4. Het vooruitbetalingspercentage op de verkoop- of inkoopkop.  

Met andere woorden: het vooruitbetalingspercentage op de klantenkaart geldt alleen als er geen vooruitbetalingspercentage is ingesteld voor het artikel. Als u echter de inhoud van het veld **Vooruitbetaling %** wijzigt in de verkoop- of de inkoopkop nadat u de regels hebt gemaakt, wordt het vooruitbetalingspercentage op alle regels bijgewerkt. Hierdoor wordt het gemakkelijk om een order te maken met een vast vooruitbetalingspercentage, ongeacht het percentage dat is ingesteld op artikelen.

## <a name="see-also"></a>Zie ook  
[Vooruitbetalingen factureren](finance-invoice-prepayments.md)  
[Procedure: Vooruitbetalingen verkoop instellen en factureren](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

