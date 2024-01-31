---
title: Aankopen registreren met inkoopfacturen (bevat video)
description: 'Hierin wordt beschreven hoe u voorraad, niet-voorraadartikelen of resources inkoopt door inkoopfacturen of inkooporders te maken en te boeken.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: procurement
ms.search.form: '50 ,51, 53, 56, 146, 147, 9307, 9309, 9306, 9308, 9310'
ms.date: 12/19/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Aankopen registreren met inkoopfacturen en orders

U maakt een inkoopfactuur of inkooporder om de kosten van inkopen vast te leggen en leveranciers te volgen. Inkoopfacturen en inkooporders worden ook gebruikt om voorraadniveaus dynamisch aan te passen zodat u uw voorraadkosten kunt beperken en betere klantenservice kunt bieden. De inkoopkosten, inclusief servicekosten en voorraadwaarden die resulteren uit boekingsinkoopfacturen of orders, dragen bij aan winstcijfers en andere financiële KPI's in uw rolcentrum.

## Aankopen registreren met inkoopfacturen

Wanneer u de voorraadartikelen ontvangt of wanneer de ingekochte service is voltooid, boekt u de inkoopfactuur om de voorraad en financiële records bij te werken en betaling aan de leverancier te activeren volgens de betalingscondities. [Betalingen uitvoeren](payables-make-payments.md).

> [!CAUTION]  
> Boek geen inkoopfactuur voor fysieke artikelen totdat u de fysieke artikelen ontvangt en de uiteindelijke kosten van de inkoop kent, inclusief eventuele toeslagen. Anders kloppen uw voorraadwaarde en winstcijfers mogelijk niet.

### Een inkoopfactuur maken en boeken

Hieronder wordt beschreven hoe u een inkoopfactuur maakt. De stappen voor het maken van een inkooporder zijn vergelijkbaar. Het belangrijkste verschil is dat inkooporders enkele extra velden en acties hebben voor de fysieke afhandeling van artikelen.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopfacturen** in en kies vervolgens de gerelateerde koppeling.  
2. Voer in het veld **Leverancier** de naam in van een bestaande leverancier.

    Overige velden op de pagina **Inkoopfactuur** worden nu ingevuld met de standaardinformatie voor de geselecteerde leverancier. Als de leverancier niet is geregistreerd, volgt u deze stappen:

    1. Voer in het veld **Leverancier** de naam van de nieuwe leverancier in.
    2. Kies in dialoogvenster voor het registreren van de nieuwe leverancier **Ja**.
    3. Zie voor meer informatie over het invullen van de leverancierskaart [Nieuwe leveranciers registreren](purchasing-how-register-new-vendors.md).  
    4. Wanneer u de leverancierskaart hebt voltooid, kiest u **OK** om terug te keren naar de pagina **Inkoopfactuur**.

3. Vul desgewenst de overige velden op de pagina **Inkoopfactuur** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    U kunt nu de inkoopfactuurregels invullen met voorraadartikelen of resources die u hebt gekocht van de leverancier.

    > [!NOTE]  
    > Als u terugkerende inkoopregels voor de leverancier hebt ingesteld, zoals een maandelijkse aanvullingsorder, kunt u deze regels invoegen op de factuur door de actie **Terugkerende inkoopregels ophalen** te kiezen.
4. Voer op het sneltabblad **Regels** in het veld **Artikelnr.** het nummer van een voorraadartikel of een service in.
5. Voer in het veld **Aantal** het in te kopen aantal van een artikel in.

    Het veld **Regelbedrag** wordt bijgewerkt met de waarde in het veld **Directe kostprijs**, vermenigvuldigd met de waarde in het veld **Aantal**.

    De prijs en het regelbedrag worden weergegeven met of zonder btw afhankelijk van wat u selecteert in het veld **Prijzen inclusief btw** op de leverancierskaart.

    De totalenvelden onder de regels worden automatisch bijgewerkt wanneer u regels maakt of wijzigt om de bedragen weer te geven die naar de grootboeken worden geboekt.

6. In het veld **Kortingsbedrag op factuur** voert u een bedrag in dat moet worden afgetrokken van de waarde in het veld **Totaal incl. btw** onder in de factuur.

    > [!NOTE]  
    > Als u factuurkortingen voor de leverancier hebt opgegeven, wordt het percentage automatisch ingevoegd in het veld **Leveranciersfactuurkortingen %** als aan de voorwaarden wordt voldaan. Het gerelateerde bedrag wordt vervolgens ingevoegd in het veld **Bedrag factuurkorting**.
7. Als u de ingekochte artikelen of diensten ontvangt, kiest u **Boeken**.

De inkoop wordt nu weerspiegeld in de voorraad, resourcejournalen en financiële records, en de leveranciersbetaling wordt geactiveerd. De inkoopfactuur wordt verwijderd uit het overzicht met inkoopfacturen en wordt vervangen door een nieuw document in het overzicht van geboekte inkoopfacturen.  Zie [Inkopen boeken](purchasing-how-record-purchases.md#posting-purchases) voor meer informatie over wat er gebeurt als u inkoopdocumenten boekt.

> [!NOTE]
> In zeldzame gevallen kunnen de geboekte bedragen afwijken van wat wordt weergegeven in de totalenvelden. Dit is meestal het gevolg van afrondingsberekeningen met betrekking tot btw of omzetbelasting.
>
> Om de bedragen te controleren die daadwerkelijk worden geboekt, gaat u naar de pagina **Statistieken**, die rekening houdt met de afrondingsberekeningen. Als u de actie **Vrijgeven** kiest, worden de totalenvelden ook bijgewerkt met afrondingsberekeningen.

## Geboekte facturen

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

U kunt een geboekte inkoopfactuur gemakkelijk corrigeren of annuleren voordat u de leverancier betaalt. Dit is handig als u een typefout moet corrigeren of als u de aankoop in het begin van het orderproces wilt wijzigen. Zie [Niet-betaalde inkoopfacturen corrigeren of annuleren](purchasing-how-correct-cancel-unpaid-purchase-invoices.md) voor meer informatie. Als u een inkoop ongedaan wilt maken voor artikelen of services op de geboekte inkoopfactuur waarvoor de betaling wordt verwerkt, moet u een inkoopcreditnota maken. Zie [Inkoopretouren of annuleringen verwerken](purchasing-how-process-purchase-returns-cancellations.md) voor meer informatie.

[Open de lijst **Geboekte inkoopfacturen**](https://businesscentral.dynamics.com/?page=146) in [!INCLUDE [prod_short](includes/prod_short.md)].


## Niet-voorraadartikelen inkopen

De regels op een inkoopfactuur kunnen van het type **Bron** of **Artikel** zijn. Artikelkaarten kunnen verder worden geclassificeerd als van het type **Voorraad**, **Service** of **Niet-voorraad**, waarmee wordt opgegeven of het artikel een fysieke voorraadeenheid is, een eenheid voor arbeidskosten (ook van toepassing op resources) is of een fysieke eenheid is die niet in voorraad wordt gehouden. Meer informatie op [Nieuwe artikelen registreren](inventory-how-register-new-items.md). Het inkoopfactureringsproces is hetzelfde voor alle genoemde typen.

> [!NOTE]
> Met de inkoopregelsoort **Resource** kunt u ook externe resources aanschaffen, bijvoorbeeld om een leverancier te factureren voor geleverd werk. Meer informatie op [Resources instellen](projects-how-setup-resources.md).
>
> Om een gekochte resource te gebruiken moet u mogelijk de capaciteit van de resource instellen en deze handmatig aan een taak toewijzen. Als u een resource koopt, wordt er een resourcepost gemaakt, maar resourceposten worden niet bijgehouden voor hoeveelheid en waarde, zoals bijvoorbeeld artikelen. Als het bijhouden van hoeveelheden en waarden vereist is, overweeg dan om andere typen regelartikelen te gebruiken.

## Wanneer inkooporders gebruiken?

U moet inkooporders gebruiken als uw inkoopproces vereist dat u gedeeltelijke ontvangsten van een orderhoeveelheid registreert, bijvoorbeeld omdat de volledige hoeveelheid niet beschikbaar is bij de leverancier. Als u verkochte artikelen rechtstreeks van uw leverancier bij de klant levert als een doorverzending, moet u ook inkooporders gebruiken. Meer informatie op [Doorverzendingen uitvoeren](sales-how-drop-shipment.md).

Wat betreft alle andere aspecten werken inkooporders op dezelfde manier als inkoopfacturen. De volgende procedure is gebaseerd op een inkoopfactuur. De stappen zijn vergelijkbaar met de stappen voor een inkooporder.

<br><br>

> [!Video https://www.microsoft.com/videoplayer/embed/RE4b3tt?rel=0]

## Artikelen ontvangen met een inkooporder

Hieronder wordt beschreven hoe u artikelen ontvangt met een inkooporder. 

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **inkooporders** in en kies vervolgens de gerelateerde koppeling.
2. Open een bestaande inkooporder of maak een nieuwe.
3. Voer in het veld **Te ontvangen aantal** het aantal in dat u hebt ontvangen.

   > [!NOTE]
   > Als het ontvangen aantal groter is dan het aantal op de inkooporder, en als voor de leverancier is ingesteld dat meerontvangsten zijn toegestaan, gebruikt u het veld **Te veel ontvangen** om het overtollige aantal te verwerken. Zie voor meer informatie de sectie [Meer artikelen ontvangen dan besteld](purchasing-how-record-purchases.md#receive-more-items-than-ordered).
4. Kies de actie **Boeken**.

  De waarde in het veld **Ontvangen aantal** wordt dienovereenkomstig bijgewerkt. Als het een gedeeltelijke ontvangst is, is de waarde lager dan de waarde in het veld **Aantal**.

> [!NOTE]
> Als u een magazijnverwerking gebruikt, kunt u de actie **Boeken** voor de inkooporder niet gebruiken om ontvangst te registreren. Dit is omdat een magazijnmedewerker de inkooporderhoeveelheid al heeft geboekt als ontvangen. Meer informatie in [Ontwerpdetails: Inkomende magazijnstroom](design-details-inbound-warehouse-flow.md).

## Meer artikelen ontvangen dan besteld

Wanneer meer goederen aankomen dan zijn besteld, wilt u deze misschien ontvangen in plaats van de ontvangst te annuleren. Het kan bijvoorbeeld goedkoper zijn om de extra artikelen in voorraad te houden dan ze terug te sturen of uw leverancier kan u korting geven om ze te bewaren.

<!--move the over-receipt setup info to an article about purchasing. Keep the concept info here and link to the steps-->
### Meerontvangsten instellen

Maak meerontvangstcodes aan om een percentage te definiëren waarmee een ontvangen hoeveelheid de bestelde hoeveelheid kan overschrijden. Geef in het veld **Tolerantiepercentage voor meerontvangst** het percentage op. Vervolgens wijst u de code toe op de pagina's Artikelkaart of Leverancierskaart voor artikelen en leveranciers.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") pictogram, voer **Meerontvangstcodes** in en kies vervolgens de gerelateerde koppeling.
2. Vul de vereiste velden in. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### De meerontvangstcode toewijzen aan een artikel

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.
2. Open de pagina **Artikelkaart** voor het artikel.
3. Kies in het veld **Meerontvangstcode** de code met het percentage dat u wilt toestaan voor meerontvangsten.

De meerontvangstcode wordt toegewezen aan het artikel. Met inkooporders of magazijnontvangsten voor het artikel kunt u nu meer ontvangen dan de bestelde hoeveelheid volgens het opgegeven tolerantiepercentage voor meerontvangst.

> [!NOTE]
> U kunt een goedkeuringswerkstroom instellen die vereist dat meerontvangsten worden goedgekeurd voordat ze kunnen worden afgehandeld. Schakel het selectievakje **Goedkeuring vereist** in op de pagina **Meerontvangstcodes**. Zie voor meer informatie [Werkstromen maken](across-how-to-create-workflows.md).

### Teveel ontvangen voor een order

Op inkoopregels en magazijnontvangstregels wordt het veld **Meer ontvangen hoeveelheid** gebruikt om meer ontvangen hoeveelheden vast te leggen, dat wil zeggen hoeveelheden die het orderaantal in het veld **Aantal** overschrijden.

Wanneer u een meerontvangst afhandelt, kunt u de waarde in het veld **Te ontvangen aantal** verhogen tot het werkelijk ontvangen aantal. Het veld **Meer ontvangen hoeveelheid** wordt bijgewerkt om de overtollige hoeveelheid weer te geven. U kunt ook de overtollige hoeveelheid invoeren in het veld **Meer ontvangen hoeveelheid**. Het veld **Te ontvangen aantal** wordt bijgewerkt om het bestelde aantal plus de overtollige hoeveelheid aan te geven. In de volgende procedure wordt beschreven hoe u het veld **Te ontvangen aantal** invult.  

1. Op een inkooporder of een magazijnontvangstdocument waarbij de ontvangen hoeveelheid hoger is dan besteld, voert u de werkelijk ontvangen hoeveelheid in het veld **Te ontvangen aantal** in.

    Als de verhoging binnen de tolerantie valt die is gespecificeerd door de toegewezen meerontvangstcode, wordt het veld **Meer ontvangen hoeveelheid** bijgewerkt om de hoeveelheid weer te geven waarmee de waarde in het veld **Aantal** is overschreden.

    Als de verhoging hoger is dan de opgegeven tolerantie, is de meerontvangst niet toegestaan. Onderzoek of een andere meerontvangstcode dit toestaat. Anders kan alleen de bestelde hoeveelheid worden ontvangen en moet de overtollige hoeveelheid anders worden afgehandeld, bijvoorbeeld door deze terug te sturen naar de leverancier.

2. Boek de ontvangst zoals u zou doen voor elke andere ontvangst.

> [!NOTE]
> [!INCLUDE[prod_short](includes/prod_short.md)] verwerkt niet automatisch de financiële aspecten van meerontvangsten. U moet dit handmatig afhandelen in overleg met de leverancier, bijvoorbeeld doordat de leverancier een nieuwe of bijgewerkte factuur stuurt.

## Externe documentnummer

[!INCLUDE [ext-doc-no-purch](includes/ext-doc-no-purch.md)]

## Inkopen boeken

In een inkoopdocument kunt u kiezen uit de volgende boekingsacties:

* **Boeken**
* **Voorbeeld van boeking weergeven**
* **Boeken en afdrukken**
<!--* **Test Report**-->
* **Batchboeken**

Wanneer een inkoopdocument wordt geboekt, worden de rekening van de leverancier, het grootboek, de artikelposten en de resourceposten bijgewerkt.

Voor elk inkoopdocument wordt een inkooppost gemaakt in de tabel **Grootboekpost**. Ook wordt een post in de leveranciersrekening in de tabel **Leverancierspost** gemaakt en wordt er een grootboekpost in de betreffende schuldenrekening gemaakt. Bovendien kan het boeken van de inkoop resulteren in een btw-post en een grootboekpost voor de totale korting. Of er een post voor de korting wordt geboekt, wordt bepaald door de inhoud van het veld **Korting boeken** op de pagina **Inkoopinstellingen**.

Voor elke inkoopregel worden, indien van toepassing, boekingen gemaakt in de:

* tabel **Artikelpost** als de inkoopregel van het type **Artikel** is.
* tabel **Grootboekpost** als de inkoopregel van het type **Grootboekrekening** is
* tabel **Resourcepost** als de inkoopregel van het type **Resource** is.

Daarnaast worden inkoopdocumenten altijd vastgelegd in de tabellen **Inkoopontvangst** en **Inkoopfactuur**.

U kunt altijd verschillende grootboekposten bekijken die worden gemaakt als gevolg van boekingen. Kies **Voorbeeld van boeking weergeven** om het document te valideren en verwachte grootboekposten te inspecteren.


> [!IMPORTANT]  
> Tijdens het boeken van een inkooporder voor artikelen kunt u zowel een ontvangst als een factuur maken. Deze kunt u tegelijkertijd, maar ook onafhankelijk van elkaar maken. U kunt ook een gedeeltelijke ontvangst en een gedeeltelijke factuur maken door de velden **Te ontvangen aantal** en **Te factureren aantal** op de afzonderlijke inkooporderregels in te vullen voordat u de boeking uitvoert. Houd er rekening mee dat u geen inkoopfactuur kunt maken van een inkooporder voor producten of diensten die niet zijn ontvangen. Dit betekent dat u pas kunt factureren als er een ontvangst is vastgelegd, of u moet tegelijkertijd ontvangen en factureren.

U kunt boeken of boeken en afdrukken. Als u ervoor kiest om te boeken en af te drukken, wordt een lijst afgedrukt nadat de order is geboekt. U kunt ook de actie **Batchboeken** kiezen, waarmee u verschillende orders tegelijkertijd kunt boeken. Zie voor meer informatie [Meerdere documenten tegelijkertijd boeken](ui-batch-posting.md).

## Posten bekijken

Na de boeking worden de geboekte inkoopregels verwijderd uit de order. Er verschijnt een bericht als de boeking is voltooid. Hierna kunt u de geboekte posten bekijken op de verschillende pagina's inclusief de pagina's **Leveranciersposten**, **Grootboekposten**, **Artikelposten**, **Resourceposten**, **Inkoopontvangsten** en **Geboekte inkoopfacturen**.

In de meeste gevallen kunt u posten openen vanaf de betrokken kaart of het betreffende document. Kies bijvoorbeeld op de pagina **Leverancierskaart** de actie **Posten**.

## Posten bewerken

U kunt bepaalde velden in geboekte inkoopdocumenten bewerken, zoals het veld **Betalingsreferentie**. Zie voor meer informatie [Geboekte documenten bewerken](across-edit-posted-document.md). Voor kritiekere velden die van invloed zijn op het controlespoor, moet u het boeken omkeren of ongedaan maken. Zie voor meer informatie [Journaalboekingen tegenboeken en ontvangsten/zendingen ongedaan maken](finance-how-reverse-journal-posting.md).

## Zie ook

[Offertes aanvragen](purchasing-how-request-quotes.md)  
[Artikelen inkopen voor een verkoop](purchasing-how-purchase-products-sale.md)  
[Doorverzendingen voorbereiden](sales-how-drop-shipment.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Inkoop instellen](purchasing-setup-purchasing.md)  
[Resources instellen](projects-how-setup-resources.md)  
[Nieuwe leveranciers registreren](purchasing-how-register-new-vendors.md)  
[Geboekte documenten bewerken](across-edit-posted-document.md)  
[Meerdere documenten tegelijkertijd boeken](ui-batch-posting.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Documenten en dagboeken boeken](ui-post-documents-journals.md)  
[Niet-betaalde inkoopfacturen corrigeren of annuleren](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Pagina's en informatie zoeken met Vertel me](ui-search.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
