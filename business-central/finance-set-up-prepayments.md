---
title: Vooruitbetalingen instellen
description: Leer hoe u Business Central zo configureert dat u vooruitbetalingen in Business Central kunt gebruiken om borgsommen te factureren en te innen van klanten en borgsommen over te maken aan leveranciers.
author: edupont04
ms.topic: conceptual
ms.search.keyword: prepayment
ms.search.form: '314, 459, 460, 664'
ms.date: 10/27/2021
ms.author: edupont
---
# <a name="set-up-prepayments" />Vooruitbetalingen instellen

Als uw klanten u moeten betalen voordat u een order naar ze verzendt of als uw leverancier wil dat u betaalt voordat een order naar u wordt verzonden, kunt u de functie Vooruitbetaling gebruiken. Met de functionaliteit voor vooruitbetalingen kunt u vereiste borgsommen factureren en innen van klanten of kunt u borgsommen overmaken aan leveranciers, en ervoor zorgen dat alle gedeeltelijke betalingen worden geboekt tegen een factuur. Zie voor meer informatie [Vooruitbetalingsfacturen maken](finance-how-to-create-prepayment-invoices.md).

Voor u vooruitbetalingsfacturen kunt boeken, moet u de boekingsrekening instellen in het grootboek en moet u nummerreeksen instellen voor de vooruitbetalingsdocumenten. U moet een account opgeven voor vooruitbetalingen met betrekking tot verkopen en een account voor vooruitbetalingen met betrekking tot aankopen. U kunt dezelfde boekingsrekeningen opgeven die moeten worden gebruikt voor alle vooruitbetalingen die betrekking hebben op alle algemene bedrijfsboekingsgroepen of algemene productboekingsgroepen, of u kunt specifieke accounts voor specifieke boekingsgroepen opgeven voor respectievelijk verkoop en inkoop. Dit is afhankelijk van de vereisten van uw bedrijf voor het bijhouden van vooruitbetalingen.  

U kunt het percentage van het regelbedrag definiëren dat wordt gefactureerd voor een vooruitbetaling. Nadat u de instellingen hebt gemaakt, kunt u vooruitbetalingsfacturen genereren van verkoop- en inkooporders. U kunt de standaardpercentages gebruiken voor elke verkoop- of inkoopregel, of u kunt de bedragen op de factuur wijzigen zoals gewenst. U kunt bijvoorbeeld een totaalbedrag specificeren voor de volledige order.  

> [!NOTE]
> We raden u aan om in de volgende gevallen geen vooruitbetalingspercentage van 100 te hanteren:
>
> * Als u zich in Noord-Amerika bevindt. Vanwege de manier waarop belastingen worden berekend, kan een vooruitbetalingspercentage van 100 leiden tot problemen met vooruitbetalingsfacturen.
> * In alle regio's, als u handmatig een contantkorting van de factuur aftrekt. Bij een vooruitbetalingspercentage van 100 blijft er niet automatisch een bedrag over waarvan de korting kan worden afgetrokken.
>
> Als u een vooruitbetalingspercentage van 100 gebruikt, moet [!INCLUDE[prod_short](includes/prod_short.md)] mogelijk compenserende afrondingsposten maken. Als dat gebeurt, moet u een grootboekrekening kiezen in het veld **Factuurafrondingsrekening** op de pagina **Klantenboekingsgroepen**. Dit geldt zelfs als u de schakelaar **Factuurafronding** op de pagina **Verkoopinstellingen** niet hebt ingeschakeld. Als u geen rekening opgeeft, kunt u geen vooruitbetalingsfacturen boeken. 

Omdat het vooruitbetaalde bedrag bij de koper hoort totdat deze de goederen of diensten heeft ontvangen, moet u grootboekrekeningen instellen waarop de vooruitbetaalde bedragen staan totdat de uiteindelijke factuur wordt geboekt. Vooruitbetaalde verkopen moeten worden vastgelegd op een passivarekening totdat de artikelen worden verzonden. Vooruitbetaalde inkopen moeten worden vastgelegd op een activarekening totdat de artikelen worden ontvangen. Daarnaast moet u een afzonderlijke grootboekrekening instellen voor elke btw-id.  

[!INCLUDE[local-func-setup-link](includes/local-func-setup-link.md)]

## <a name="to-add-prepayment-accounts-to-the-general-posting-setup" />Vooruitbetalingsrekeningen toevoegen aan de boekingsgroepinstellingen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Boekingsgroepinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Vul op de pagina **Boekingsgroepinstellingen** de volgende velden in voor de relevante regels:  

    * **Vooruitbetalingsrekening verkoop**  
    * **Vooruitbetalingsrekening inkoop**  

> [!TIP]
> Als u de velden niet kunt zien op de pagina **Boekingsgroepinstellingen**, gebruikt u de horizontale schuifbalk onder aan de pagina om naar rechts te schuiven.  

Als u nog geen grootboekrekeningen hebt ingesteld voor vooruitbetalingen, kunt u de pagina **Grootboekrekeningoverzicht** openen vanuit het relevante rekeningveld.  

## <a name="to-set-up-number-series-for-prepayment-documents" />Nummerreeks instellen voor vooruitbetalingsdocumenten

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Vul op de pagina **Verkoopinstellingen** op het sneltabblad **Nummerreeks** de volgende velden in:  

   * **Geboekte vooruitbetalingsfactuurnrs.**
   * **Geboekte vooruitbetalingscreditnotanrs.**

3. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopinstellingen** in en kies vervolgens de gerelateerde koppeling.
4. Vul op de pagina **Inkoopinstellingen** op het sneltabblad **Nummerreeks** de volgende velden in:

    * **Geboekte vooruitbetalingsfactuurnrs.**
    * **Geboekte vooruitbetalingscreditnotanrs.**

> [!NOTE]  
> U kunt dezelfde nummerreeks gebruiken voor vooruitbetalingsnota's en normale facturen, of u kunt verschillende nummerreeksen gebruiken. Als u verschillende reeksen gebruikt, mogen deze elkaar niet overlappen omdat er geen nummers mogen zijn die in beide reeksen voorkomen.  

## <a name="to-set-up-prepayment-percentages-for-items-customers-and-vendors" />Vooruitbetalingspercentages instellen voor artikelen, klanten en leveranciers

Voor een artikel kunt u een standaardvooruitbetalingspercentage instellen voor alle klanten, een specifieke klant of een klantenprijsgroep. Als u niet voor alle klanten hetzelfde vooruitbetalingspercentage wilt toepassen, moet u aangeven voor welke klanten of voor welke klantprijsgroepen het vooruitbetalingspercentage geldt.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer een artikel en kies vervolgens de actie **Vooruitbetalingspercentages**.  
3. Vul op de pagina **Vooruitbetalingspercentages verkoop** de benodigde velden in: [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

Voor een klant of leverancier kunt u één standaardvooruitbetalingspercentage instellen voor alle artikelen en alle typen verkoopregels. U voert dit op de klanten- of leverancierskaart in. De volgende procedure laat zien hoe u een vooruitbetalingspercentage voor een klant opgeeft, maar soortgelijke stappen zijn van toepassing op leveranciers.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies vervolgens de gerelateerde koppeling.
2. Open de kaart voor een klant.
3. Vul het veld **Vooruitbetaling %** in.
4. Herhaal de stappen voor andere voor klanten of leveranciers.  

> [!TIP]
> U kunt ook toegang krijgen tot de pagina **Inkoopinstellingen** van de klanten- of leverancierskaart.

### <a name="to-determine-which-prepayment-percentage-has-first-priority" />Bepalen welk vooruitbetalingspercentage de hoogste prioriteit heeft

Een order kan een vooruitbetalingspercentage hebben in de verkoopkop en een ander percentage voor de artikelen op de regels. Om te bepalen welk vooruitbetalingspercentage van toepassing is voor elke verkoopregel, zoekt het systeem voor elke verkoopregel in de volgende volgorde naar het vooruitbetalingspercentage. De eerste gevonden standaardwaarde wordt toegepast:  

1. Een vooruitbetalingspercentage voor het artikel op de regel en de klant waarvoor de order is.  
2. Een vooruitbetalingspercentage voor het artikel op de regel en de klantenprijsgroep waar de klant bij hoort.  
3. Een vooruitbetalingspercentage voor het artikel op de regel voor alle klanten.  
4. Het vooruitbetalingspercentage op de verkoop- of inkoopkop.  

Met andere woorden: het vooruitbetalingspercentage op de klantenkaart geldt alleen als er geen vooruitbetalingspercentage is ingesteld voor het artikel. Als u echter de inhoud van het veld **Vooruitbetaling %** wijzigt in de verkoop- of de inkoopkop nadat u de regels hebt gemaakt, wordt het vooruitbetalingspercentage op alle regels bijgewerkt. Hierdoor wordt het gemakkelijk om een order te maken met een vast vooruitbetalingspercentage, ongeacht het percentage dat is ingesteld op artikelen.

## <a name="to-automatically-release-sales-orders-when-prepayments-are-applied" />Verkooporders automatisch vrijgeven wanneer vooruitbetalingen worden toegepast

U kunt tijd besparen door een taakwachtrij-item in te stellen dat automatisch verkooporders vrijgeeft waarvoor vooruitbetaling is vereist nadat de betalingen zijn toegepast. Het automatiseren van het proces bespaart u de stap van het vrijgeven van de verkooporder.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Geef in het veld **Frequentie van automatische update van vooruitbetaling** op hoe vaak u het taakwachtrij-item wilt laten uitvoeren.

> [!TIP]
> Overweeg, terwijl u hier bent, een beveiliging toe te voegen tegen verzending of facturering van verkooporders met onbetaalde vooruitbetalingen. Als u de schakelaar **Voortbet. cntr. bij boeken** aanzet, voorkomt [!INCLUDE[prod_short](includes/prod_short.md)] dat mensen orders plaatsen met openstaande vooruitbetalingsbedragen.

3. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Taakwachtrijposten** in en kies vervolgens de gerelateerde koppeling.
4. Stel het taakwachtrij-item **Verkopen wachtend op vooruitbetaling bijwerken** bijvoorbeeld in door de instellingen op het tabblad **Herhaling** te gebruiken om te plannen hoe vaak u het item wilt uitvoeren. Zie voor meer informatie [Taakwachtrijen gebruiken om taken te plannen](admin-job-queues-schedule-tasks.md).

## <a name="see-related-microsoft-trainingtrainingmodulesprepayment-invoices-dynamics-365-business-central" />Zie gerelateerde [Microsoft-training](/training/modules/prepayment-invoices-dynamics-365-business-central/)

## <a name="see-also" />Zie ook

[Vooruitbetalingen factureren](finance-invoice-prepayments.md)  
[Procedure: Vooruitbetalingen verkoop instellen en factureren](walkthrough-setting-up-and-invoicing-sales-prepayments.md)  
[GST op vooruitbetalingen berekenen in Australië](LocalFunctionality/Australia/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[GST op vooruitbetalingen berekenen in Nieuw-Zeeland](LocalFunctionality/NewZealand/how-to-calculate-goods-and-services-tax-on-prepayments.md)  
[Het grootboek en COA begrijpen](finance-general-ledger.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
