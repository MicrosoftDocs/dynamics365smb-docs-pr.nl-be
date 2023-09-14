---
title: Vaste activa aanschaffen
description: 'U kunt een vast activum instellen, een afschrijvingsboek toewijzen en de aanschafkosten van het vaste activum vastleggen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: purchase fixed asset
ms.search.form: '5605, 5551, 5600, 5628, 5629, 5633'
ms.date: 12/03/2021
ms.author: bholtorf
---
# Vaste activa aanschaffen

Voor elk vast activum moet u een kaart maken met informatie over het activum. U kunt gebouwen of productiemateriaal instellen als een hoofdactivum met een onderdelenlijst en u kunt ze op verschillende manieren groeperen, bijvoorbeeld per categorie, afdeling of locatie. Een afschrijvingsboek moeten eerst worden ingesteld en toegewezen aan elk vast activum voordat u het kunt aanschaffen.

Wanneer een vast activum is ingesteld en een afschrijvingsboek is toegewezen, moet u het vaste activum aanschaffen. Als u een vast activum wilt aanschaffen, registreert u de bijbehorende aanschafkosten in de betreffende grootboekrekening, bankrekening of leverancier door een aanschaftransactie te boeken op de pagina **Financieel dagboek voor vaste activa**. U kunt de pagina **Begeleide aanschaf van vast activum** gebruiken om de vereiste dagboekregels automatisch te maken en te boeken.

De restwaarde is de resterende waarde van een vast activum als dit niet langer meer kan worden gebruikt. U kunt de restwaarde tegelijk met het boeken van de aanschafkosten boeken. Zie [Vaste activa afschrijven of aflossen](fa-how-depreciate-amortize.md) voor meer informatie.

Indexering wordt gebruikt om waarden aan te passen voor algemene prijswijzigingen. De batchverwerking **Vast activum indexeren** kan worden gebruikt om de aanschafkosten te berekenen bij vervangingskosten.

## Een vast activum maken en automatisch aanschaffen

In de volgende procedure wordt beschreven hoe u een vast activum kunt maken en vervolgens kunt aanschaffen met de pagina **Begeleide aanschaf van vast activum** om de vereiste dagboekregels voor vaste activa te maken en te boeken. U kunt de dagboekregels ook handmatig maken en boeken. Zie [De aanschaf van een vast activum handmatig boeken met het financieel dagboek voor vaste activa](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal) voor meer informatie.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Vaste activa** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw** en vul vervolgens indien nodig de velden op het sneltabblad **Algemeen** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Vul op het sneltabblad **Afschrijvingsboek** indien nodig de velden in. Met deze stap wordt een afschrijvingsboek aan het vaste activum toegewezen.  
4. Als u meer dan één afschrijvingsboek aan het vaste activum moet toewijzen, kiest u de actie **Meer afschrijvingsboeken toevoegen**. Zie [Een afschrijvingsboek aan een vast activum toewijzen](fa-how-setup-depreciation.md#to-assign-a-depreciation-book-to-a-fixed-asset) voor meer informatie.

    Wanneer alle velden die nodig zijn om een vast activum aan te schaffen zijn ingevuld, verschijnt boven aan de pagina de melding dat **u het vaste activum nu kunt aanschaffen**.
5. Kies de actie **Aanschaffen** in de melding.
6. Voer de stappen op de pagina **Begeleide aanschaf van vast activum** uit om de automatische aanschaffing van het vaste activum te voltooien.

> [!NOTE]  
>   U kunt ook aanschafkosten als creditbedragen boeken. In dat geval moet u er rekening mee houden dat de waarde in het veld **Aanschafkosten inclusief BTW** met een minteken moet worden ingevuld om een creditbedrag aan te geven.

Wanneer u **Voltooien** kiest, wordt het veld **Boekwaarde** op de pagina **Vast activum** ingevuld waarmee wordt aangegeven dat het vaste activum met de opgegeven aanschafkosten is aangeschaft.  

## Een onderdelenlijst instellen voor een hoofdactivum

U kunt vaste activa groeperen in hoofdactiva en hun onderdelen. U kunt bijvoorbeeld een productiemachine hebben die uit vele onderdelen bestaat die u op deze manier wilt groeperen.  

Zowel het hoofdactivum als alle onderdelen moeten als individueel vast activum worden ingesteld. Nadat u een onderdelenlijst hebt ingesteld, worden in [!INCLUDE[prod_short](includes/prod_short.md)] automatisch de velden **Hoofdactivum/Onderdeel** en **Onderdeel van hoofdactivum** op de VA-kaarten ingevuld.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Vaste activa** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer het vaste activum dat het hoofdactivum is en kies vervolgens de actie **Onderdelen van hoofdactivum**.
3. Kies op de pagina **Onderdelen van hoofdactivum** het veld **VA-nr** en selecteer vervolgens het vaste activum dat u als onderdeel wilt toevoegen van het hoofdactivum.
4. Sluit de pagina.
5. Herhaal stap 3 en 4 voor elk onderdeelactivum dat u wilt toevoegen.
6. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **VA-instellingen** in en kies vervolgens de gerelateerde koppeling.
7. Schakel het selectievakje **Boeken op hoofdactivum toegestaan** in.

## Een aanschaf voor vaste activa handmatig boeken met het financieel dagboek voor vaste activa

In de volgende procedure wordt beschreven hoe u een vast activum handmatig kunt aanschaffen door regels te maken en te boeken op de pagina **Financieel dagboek voor vaste activa**. U kunt een vast activum ook automatisch aanschaffen door de pagina **voor begeleide aanschaf van vaste activa** te gebruiken. Zie stap 5 in [Een vast activum maken en het automatisch aanschaffen](fa-how-acquire.md#to-create-a-fixed-asset-and-acquire-it-automatically) voor meer informatie.

> [!NOTE]  
>   U kunt ook aanschafkosten als creditbedragen boeken. In dat geval moet u er rekening mee houden dat de waarde in het veld **Bedrag** met een minteken moet worden ingevuld om een creditbedrag aan te geven.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **VA-fin. dagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer op de pagina **Financieel dagboek voor vaste activa** in het veld **VA-boekingssoort** **Aanschafkosten**.
3. Vul indien nodig de resterende velden in.
4. Kies de actie **Boeken**.  

> [!TIP]  
>   Als u tijdens het boeken van de aanschafkosten het veld **Verzekeringsnr.** invult in het dagboek, worden de aanschafkosten van het vaste activum door [!INCLUDE[prod_short](includes/prod_short.md)] ook naar de verzekeringsdekkingsposten geboekt. Zie [Vaste activa verzekeren](fa-how-insure.md) voor meer informatie.

## De boeking van aanschafkosten voor één vast activum annuleren

Als u een fout maakt wanneer u aanschafkosten boekt, kunt u de post verwijderen met de batchverwerking **VA-posten annuleren** en vervolgens de juiste aanschafpost boeken. De foutieve posten worden overgebracht naar de pagina **Foutieve VA-posten**.

Als u bijvoorbeeld een aanschaf met een onjuiste datum boekt, moet u dit zo snel mogelijk corrigeren omdat de boekingsdatum van een vast activum in veel berekeningen wordt gebruikt.

> [!IMPORTANT]  
> U kunt de functie **Transacties tegenboeken** niet voor VA-posten gebruiken.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **VA-posten** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer op de pagina **VA-posten** het item of de items die u wilt annuleren.  
3. Kies het menu **Acties** en kies vervolgens de actie **Posten annuleren**.
4. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Kies **OK** om de batchverwerking te starten.
6. Als de foutieve post of posten zijn geannuleerd, gaat u verder met het boeken van de juiste aanschafkosten.

## De restwaarde samen met de aanschafkosten boeken

Het is mogelijk om de restwaarde samen met de aanschafkosten te boeken via een VA-dagboek.

> [!NOTE]
> Voor dit proces moet u mogelijk de pagina VA-dagboeken personaliseren door het veld Restwaarde toe te voegen. Het veld wordt standaard niet weergegeven op de pagina. Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **VA-dagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Maak op de pagina **VA-dagboeken** de acquisitieregel. Zie [De aanschaf van een vast activum handmatig boeken met het financieel dagboek voor vaste activa](fa-how-acquire.md#to-post-a-fixed-asset-acquisition-manually-with-the-fixed-asset-gl-journal) voor meer informatie.
3. Voer in het veld **Restwaarde** op de dagboekregel de restwaarde in als een creditbedrag (plaats een minteken vóór het bedrag, bijvoorbeeld **-** 100).
4. Kies de actie **Boeken**.

> [!NOTE]
> Als er een restwaarde bestaat voor een vast activum, wordt die waarde gebruikt in de afschrijvingsboeking in plaats van de waarde in het veld **Min. boekw. voor afschr.** op de pagina **VA-afschrijvingsboeken**. Zie voor meer informatie [De eindboekwaarde beheren](fa-how-depreciate-amortize.md#to-manage-the-ending-book-value).

## Zie gerelateerde [Microsoft-training](/training/modules/purchase-fixed-assets/)

## Zie ook

[Vaste activa](fa-manage.md) 

[Vaste activa instellen](fa-setup.md)

[Ontwerpdetails over impact van niet-aftrekbare btw op vaste activa](design-details-nondeductible-vat.md)

[Financiën](finance.md)  

[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  

[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
