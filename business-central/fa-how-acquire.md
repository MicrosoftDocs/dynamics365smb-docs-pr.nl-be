---
title: Vaste activa aanschaffen
description: 'U kunt een vast activum instellen, een afschrijvingsboek toewijzen en de aanschafkosten van het vaste activum vastleggen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: purchase fixed asset
ms.search.form: '5605, 5551, 5600, 5628, 5629, 5633'
ms.date: 05/15/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# Vaste activa aanschaffen

Gebruik de pagina **Vaste activakaart** om informatie over een item in te voeren. U kunt gebouwen of productiemateriaal instellen als een hoofdactivum met een onderdelenlijst en u kunt ze op verschillende manieren groeperen, bijvoorbeeld per categorie, afdeling of locatie. U moet een afschrijvingsboek instellen en aan elk vast activum toewijzen voordat u het kunt aanschaffen.

Nadat u een vast activum hebt ingesteld en een afschrijvingsboek hebt toegewezen, moet u het vaste activum aanschaffen. Als u een vast activum wilt aanschaffen, registreert u de bijbehorende aanschafkosten in de betreffende grootboekrekening, bankrekening of leverancier door een aanschaftransactie te boeken op de pagina **Financieel dagboek voor vaste activa**. U kunt de pagina **Begeleide aanschaf van vast activum** gebruiken om de vereiste dagboekregels automatisch te maken en te boeken.

Gebruik indexering om waarden aan te passen aan algemene veranderingen in het prijsniveau. Gebruik de batchtaak **Index Vaste Activa** om de aanschafkosten en vervangingskosten te berekenen.

## Voeg een vast activum toe aan uw lijst met vaste activa

Voordat u een vast activum kunt aanschaffen, moet u het aan uw lijst met activa toevoegen. Er zijn verschillende manieren om vaste activa aan uw lijst toe te voegen:

* Voer informatie over de activa in op de pagina **Vaste activakaart** .
* Gebruik de actie **Bewerken in Excel** om uw lijst met middelen naar een werkblad te downloaden, nieuwe middelen aan de lijst toe te voegen en vervolgens de update te publiceren [!INCLUDE [prod_short](includes/prod_short.md)].
* Gebruik een inkooporder om activa toe te voegen.
* Gebruik de actie **Vaste activa kopiëren** .

Nadat u vaste activa aan uw lijst heeft toegevoegd, is de volgende stap het aanschaffen ervan, zodat u ze in transacties kunt gebruiken. Ga voor meer informatie naar [Een vast activum aanschaffen](#acquire-fixed-assets).

### Voeg een vast activum toe op de pagina Vaste-activakaart

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Vaste activa** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw** en vul vervolgens indien nodig de velden op het sneltabblad **Algemeen** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Vul op het sneltabblad **Afschrijvingsboek** indien nodig de velden in. Met deze stap wordt een afschrijvingsboek aan het vaste activum toegewezen.  
4. Als u meer dan één afschrijvingsboek aan het vaste activum moet toewijzen, kiest u de actie **Meer afschrijvingsboeken toevoegen**. Ga voor meer informatie naar [Een afschrijvingsboek toewijzen aan een vast activum](fa-how-setup-depreciation.md#to-assign-a-depreciation-book-to-a-fixed-asset).

    Nadat u de vereiste velden heeft ingevuld, bent **U klaar om het vaste activum aan te schaffen.** Melding verschijnt bovenaan de pagina. Als u er klaar voor bent om het item nu te verwerven, kiest u de actie  **Verwerven** . Volg de stappen op de  **ondersteunde acquisitie van vaste activa** pagina om de acquisitie te voltooien. Als u er nog niet klaar voor bent, kunt u het actief later altijd verwerven.

### Gebruik Bewerken in Excel om middelen toe te voegen

Als u meerdere vaste activa wilt toevoegen, is Bewerken in Excel een prima tool om te gebruiken. De tool downloadt uw huidige lijst met activa in een werkblad dat de meeste velden bevat die beschikbaar zijn op de pagina Vaste activakaart. U kunt voor elk item enkele of alle velden op een rij invullen en uw wijzigingen publiceren om ze in [!INCLUDE [prod_short](includes/prod_short.md)] aan uw lijst toe te voegen. Als u niet alle verplichte velden kunt invullen, is dat geen probleem. Je kunt ze bijwerken [!INCLUDE [prod_short](includes/prod_short.md)] wanneer je er klaar voor bent.

> [!NOTE]
> Om de actie Bewerken in Excel te gebruiken, moet de  Microsoft Dynamics Office-invoegtoepassing geïnstalleerd zijn. De add-in legt de verbinding tussen Excel en [!INCLUDE [prod_short](includes/prod_short.md)]. Ga voor meer informatie naar [De Business Central-invoegtoepassing voor Excel downloaden](admin-deploy-excel-addin.md).

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vaste activa** in en kies vervolgens de gerelateerde koppeling.
2. Kies het pictogram  :::image type="content" source="media/share-icon.png" alt-text="Deze pagina delen met andere gebruikers of apps."::: Pictogram en kies vervolgens **Bewerken in Excel**.
3. Open het gedownloade bestand en voer informatie in over de nieuwe vaste activa.

   > [!TIP]
   > U hoeft geen identificatie in te voeren in het **nr.** . Wanneer u uw update publiceert, [!INCLUDE [prod_short](includes/prod_short.md)] wordt er een ID toegewezen op basis van de nummerreeks die u gebruikt voor vaste activa.

4. Om [!INCLUDE [prod_short](includes/prod_short.md)] bij te werken, kies je in het **Microsoft Dynamics** paneel **Publiceren**.

### Voeg een vast activum toe uit een inkooporder of factuur

In de volgende stappen wordt beschreven hoe u een vast activum uit een inkooporder toevoegt. Voor een inkoopfactuur zijn de stappen vergelijkbaar.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Inkooporders** in en kies vervolgens de gerelateerde koppeling
2. Kies **Nieuw** om een ​​nieuwe inkooporder te maken.
3. Vul indien nodig de velden op het sneltabblad **Algemeen** in. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]
4. Op het sneltabblad **Regels** in het veld **Type**  kiest u **Vaste activa**.
5. Voer in het veld **Nr.** In het veld kunt u een bestaand vast activum kiezen om een ​​uitgave toe te voegen, of  **Nieuw** om een ​​nieuw activum toe te voegen.
6. Nadat u de gegevens voor het nieuwe activum en de inkooporder heeft ingevoerd, kiest u **Post**.

## Een vast activum verwerven met behulp van een grootboekdagboek voor vaste activa

In de volgende procedure wordt beschreven hoe u kunt verwerven door de vereiste grootboekdagboekregels voor vaste activa te maken en te boeken. U kunt de dagboekregels ook handmatig maken en boeken. Ga voor meer informatie naar [Een vast activum verwerven met behulp van een grootboekdagboek voor vaste activa](#acquire-a-fixed-asset-by-using-a-fixed-asset-gl-journal).

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vaste activa** in en kies vervolgens de gerelateerde koppeling.
1. Kies het item dat je wilt aanschaffen en kies vervolgens de actie **Verwerven** .
1. Volg de stappen op de  **ondersteunde acquisitie van vaste activa** pagina om de acquisitie te voltooien.

> [!NOTE]  
> U kunt ook aanschafkosten als creditbedragen boeken. In dat geval moet u er rekening mee houden dat de waarde in het veld **Aanschafkosten inclusief BTW** met een minteken moet worden ingevuld om een creditbedrag aan te geven.

Wanneer u  **Voltooien** kiest, wordt het veld  **Boekwaarde** op de  **Vaste activakaart** pagina is ingevuld, wat aangeeft dat het vaste activum is aangeschaft tegen de opgegeven aanschaffingswaarde.  

## Een verwerving van vaste activa handmatig boeken met een grootboekdagboek voor vaste activa

In de volgende procedure wordt beschreven hoe u een vast activum handmatig kunt aanschaffen door regels te maken en te boeken op de pagina **Financieel dagboek voor vaste activa**. U kunt ook automatisch een vast activum verwerven op de pagina **Vast activumkaart**  door de actie  **Vast activum verwerven**  te kiezen. Ga voor meer informatie naar [Een vast activum aanschaffen](#acquire-fixed-assets).

> [!NOTE]  
> U kunt ook aanschafkosten als creditbedragen boeken. In dat geval moet u er rekening mee houden dat de waarde in het veld **Bedrag** met een minteken moet worden ingevuld om een creditbedrag aan te geven.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **VA fin. dagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer op de pagina **Financieel dagboek voor vaste activa** in het veld **VA-boekingssoort** **Aanschafkosten**.
3. Vul indien nodig de resterende velden in.
4. Kies de actie **Boeken**.  

> [!TIP]  
> Als u het veld **Verzekeringsnr.** invult, [!INCLUDE[prod_short](includes/prod_short.md)] boekt u ook de aanschafkosten van het vaste activum naar het grootboek van de verzekeringsdekking. Ga voor meer informatie naar [Vaste activa verzekeren](fa-how-insure.md).

## Een onderdelenlijst instellen voor een hoofdactivum

U kunt vaste activa groeperen in hoofdactiva en hun onderdelen. Het kan bijvoorbeeld zijn dat u een productiemachine heeft die uit meerdere onderdelen bestaat en die u op deze manier wilt groeperen.  

U moet het hoofdactivum en alle onderdelen ervan instellen als afzonderlijk vast activum. Nadat u een componentenlijst heeft ingesteld, [!INCLUDE[prod_short](includes/prod_short.md)] wordt automatisch  **Hoofdactiva/Component** en **Componenten van Hoofdactivum** velden op de vaste activa.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Vaste activa** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer het vaste activum dat het hoofdactivum is en kies vervolgens de actie **Onderdelen van hoofdactivum**.
3. Kies op de pagina **Onderdelen van hoofdactivum** het veld **VA-nr** en selecteer vervolgens het vaste activum dat u als onderdeel wilt toevoegen van het hoofdactivum.
4. Sluit de pagina.
5. Herhaal stap 3 en 4 voor elk onderdeelactivum dat u wilt toevoegen.
6. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **VA-instellingen** in en kies vervolgens de gerelateerde koppeling.
7. Zet de schakelaar  **Plaatsen op hoofditems toestaan** aan.

## De boeking van aanschafkosten voor één vast activum annuleren

Als u een fout maakt wanneer u aanschafkosten boekt, kunt u de post verwijderen met de batchverwerking **VA-posten annuleren** en vervolgens de juiste aanschafpost boeken. De foutieve posten worden overgebracht naar de pagina **Foutieve VA-posten**.

Als u bijvoorbeeld een aanschaf met een onjuiste datum boekt, moet u dit zo snel mogelijk corrigeren omdat de boekingsdatum van een vast activum in veel berekeningen wordt gebruikt.

> [!IMPORTANT]  
> U kunt de actie **transacties terugboeken** niet gebruiken voor boekingen van vaste activa.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **VA-posten** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer op de pagina **VA-posten** het item of de items die u wilt annuleren.  
3. Kies het menu **Acties** en kies vervolgens de actie **Posten annuleren**.
4. Vul de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Kies **OK** om de batchverwerking te starten.
6. Als de foutieve post of posten zijn geannuleerd, gaat u verder met het boeken van de juiste aanschafkosten.

## De restwaarde samen met de aanschafkosten boeken

De restwaarde is de resterende waarde van een vast activum als dit niet langer meer kan worden gebruikt. U kunt de restwaarde tegelijk met het boeken van de aanschafkosten boeken. Ga voor meer informatie naar [Vaste activa afschrijven of amortiseren](fa-how-depreciate-amortize.md).

Het is mogelijk om de restwaarde samen met de aanschafkosten te boeken via een VA-dagboek.

> [!NOTE]
> Voor dit proces moet u mogelijk de pagina VA-dagboeken personaliseren door het veld Restwaarde toe te voegen. Het veld wordt standaard niet weergegeven op de pagina. Ga voor meer informatie naar [Uw werkruimte personaliseren](ui-personalization-user.md).

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **VA-dagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Maak op de pagina **VA-dagboeken** de acquisitieregel. Ga voor meer informatie naar [Een verwerving van vaste activa handmatig boeken met een grootboekdagboek voor vaste activa](#to-post-a-fixed-asset-acquisition-manually-with-a-fixed-asset-gl-journal).
3. Voer in het veld **Restwaarde** op de dagboekregel de restwaarde in als een creditbedrag (plaats een minteken vóór het bedrag, bijvoorbeeld **-** 100).
4. Kies de actie **Boeken**.

> [!NOTE]
> Als er een restwaarde bestaat voor een vast activum, wordt die waarde gebruikt bij het boeken van de afschrijving in plaats van de waarde in het veld **Eindboekwaarde** op het  **FA-afschrijvingsboeken** pagina. Ga voor meer informatie naar [De eindboekwaarde beheren](fa-how-depreciate-amortize.md#to-manage-the-ending-book-value).

## Zie ook

[Vaste activa](fa-manage.md)  
[Vaste activa instellen](fa-setup.md)  
[Ontwerpdetails over de niet-aftrekbare btw-impact op vaste activa](design-details-nondeductible-vat.md)  
[Financiën](finance.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
