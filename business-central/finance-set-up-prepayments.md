---
title: Vooruitbetalingen instellen | Microsoft Docs
description: Vooruitbetalingen zijn betalingen die worden gefactureerd en geboekt naar een verkoop- of inkoopvooruitbetalingsorder vóór de definitieve facturering. U vereist mogelijk een borgsom voordat u artikelen produceert in opdracht, of u vereist mogelijk betaling voordat u artikelen naar een klant verscheept. Met de vooruitbetalingsfunctionaliteit kunt u vereiste borgsommen factureren en innen van klanten of kunt u borgsommen overmaken aan leveranciers. Zodoende zorgt u dat alle betalingen worden geboekt tegen een factuur.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: prepayment
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 22afcee500b852395627cc28cb66f8863f8a198b
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5773917"
---
# <a name="set-up-prepayments"></a>Vooruitbetalingen instellen
Als uw klanten u moeten betalen voordat u een order naar ze verzendt of als uw leverancier wil dat u betaalt voordat een order naar u wordt verzonden, kunt u de functie Vooruitbetaling gebruiken. Met de functionaliteit kunt u vereiste borgsommen factureren en innen van klanten of kunt u borgsommen overmaken aan leveranciers, en ervoor zorgen dat alle gedeeltelijke betalingen worden geboekt tegen een factuur. Zie voor meer informatie [Vooruitbetalingsfacturen maken](finance-how-to-create-prepayment-invoices.md).

Voor u vooruitbetalingsfacturen kunt boeken, moet u de boekingsrekening instellen in het grootboek en moet u nummerreeksen instellen voor de vooruitbetalingsdocumenten. U moet een account opgeven voor vooruitbetalingen met betrekking tot verkopen en een account voor vooruitbetalingen met betrekking tot aankopen. U kunt dezelfde boekingsrekeningen opgeven die moeten worden gebruikt voor alle vooruitbetalingen die betrekking hebben op alle algemene bedrijfsboekingsgroepen of algemene productboekingsgroepen, of u kunt specifieke accounts voor specifieke boekingsgroepen opgeven voor respectievelijk verkoop en inkoop. Dit is afhankelijk van de vereisten van uw bedrijf voor het bijhouden van vooruitbetalingen.  

U kunt het percentage van het regelbedrag definiëren dat wordt gefactureerd voor een vooruitbetaling. Nadat u de instellingen hebt gemaakt, kunt u vooruitbetalingsfacturen genereren van verkoop- en inkooporders. U kunt de standaardpercentages gebruiken voor elke verkoop- of inkoopregel, of u kunt de bedragen op de factuur wijzigen zoals gewenst. U kunt bijvoorbeeld een totaalbedrag specificeren voor de volledige order.  

> [!NOTE]
> We raden u aan om in de volgende gevallen geen vooruitbetalingspercentage van 100% te hanteren:
> * Als u zich in Noord-Amerika bevindt. Vanwege de manier waarop belastingen worden berekend, kan een vooruitbetalingspercentage van 100% leiden tot problemen met vooruitbetalingsfacturen.
> * In alle regio's, als u handmatig een contantkorting van de factuur aftrekt. Bij een vooruitbetalingspercentage van 100% blijft er niet automatisch een bedrag over waarvan de korting kan worden afgetrokken. 

Omdat het vooruitbetaalde bedrag bij de koper hoort totdat deze de goederen of diensten heeft ontvangen, moet u grootboekrekeningen instellen waarop de vooruitbetaalde bedragen staan totdat de uiteindelijke factuur wordt geboekt. Vooruitbetaalde verkopen moeten worden vastgelegd op een passivarekening totdat de artikelen worden verzonden. Vooruitbetaalde inkopen moeten worden vastgelegd op een activarekening totdat de artikelen worden ontvangen. Daarnaast moet u een afzonderlijke grootboekrekening instellen voor elke btw-id.  

[!INCLUDE[local-func-setup-link](includes/local-func-setup-link.md)]

## <a name="to-add-prepayment-accounts-to-the-general-posting-setup"></a>Vooruitbetalingsrekeningen toevoegen aan de boekingsgroepinstellingen  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Boekingsgroepinstellingen** in en kies de desbetreffende koppeling.
2. Op de pagina **Boekingsgroepinstellingen** vult u de volgende velden in:  

    - **Vooruitbetalingsrekening verkoop**  
    - **Vooruitbetalingsrekening inkoop**  

> [!TIP]
> Als u de velden niet kunt zien op de pagina **Boekingsgroepinstellingen**, gebruikt u de horizontale schuifbalk onder aan de pagina om naar rechts te schuiven.  

Als u nog geen grootboekrekeningen hebt ingesteld voor vooruitbetalingen, kunt u de pagina **Grootboekrekeningoverzicht** openen vanuit het relevante rekeningveld.  

## <a name="to-set-up-number-series-for-prepayment-documents"></a>Nummerreeks instellen voor vooruitbetalingsdocumenten  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopinstellingen** in en kies de desbetreffende koppeling.
2. Vul op de pagina **Instellingen van verkoop en tegoeden** de volgende velden in:  

   - **Geboekte vooruitbetalingsfactuurnrs.**
   - **Geboekte vooruitbetalingscreditnotanrs.**

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopinstellingen** in en kies de desbetreffende koppeling.
2. Vul op de pagina **Inkoopinstellingen** de volgende velden in:

    - **Geboekte vooruitbetalingsfactuurnrs.**
    - **Geboekte vooruitbetalingscreditnotanrs.**

> [!NOTE]  
> U kunt dezelfde nummerreeks gebruiken voor vooruitbetalingsnota's en normale facturen, of u kunt verschillende nummerreeksen gebruiken. Als u verschillende reeksen gebruikt, mogen deze elkaar niet overlappen omdat er geen nummers mogen zijn die in beide reeksen voorkomen.  

## <a name="to-set-up-prepayment-percentages-for-items-customers-and-vendors"></a>Vooruitbetalingspercentages instellen voor artikelen, klanten en leveranciers  
Voor een artikel kunt u een standaardvooruitbetalingspercentage instellen voor alle klanten, een specifieke klant of een klantenprijsgroep.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies de gerelateerde koppeling.
2. Selecteer een artikel en kies vervolgens de actie **Vooruitbetalingspercentages**.  
3. Vul op de pagina **Vooruitbetalingspercentages verkoop** de benodigde velden in: [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Voor een klant of leverancier kunt u één standaardvooruitbetalingspercentage instellen voor alle artikelen en alle typen verkoopregels. U voert dit op de klanten- of leverancierskaart in.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies de gerelateerde koppeling.
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
[GST op vooruitbetalingen berekenen in Australië](LocalFunctionality/Australia/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[GST op vooruitbetalingen berekenen in Nieuw-Zeeland](LocalFunctionality/NewZealand/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Het grootboek en COA begrijpen](finance-general-ledger.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]