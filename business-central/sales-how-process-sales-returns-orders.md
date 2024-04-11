---
title: Verkoopretourorders verwerken
description: 'Beschrijft hoe u een verkoopretourorder maakt om een retour, een annulering of terugbetaling te verwerken voor artikelen of diensten waarvoor u betaling hebt ontvangen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'undo, credit memo, return, order'
ms.search.form: '44, 134, 144, 6629, 6630, 6633, 6662, 9302, 9304, Report_6646'
ms.date: 03/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="process-sales-return-orders"></a>Verkoopretourorders verwerken

Als u meer controle wilt hebben over het verkoopretourproces, zoals magazijndocumenten voor het hanteren van het artikel of beter overzicht bij het ontvangen van artikelen van meerdere verkoopdocumenten bij één enkele verkoopretourzending, kunt u verkoopretourorders maken. Een verkoopretourorder geeft automatisch de gerelateerde verkoopcreditnota en andere retourgerelateerde documenten uit, zoals een vervangende verkooporder, indien noodzakelijk.

Naast de oorspronkelijke geboekte verkoopfactuur kunt u de verkoopcreditnota of verkoopretourorder op andere verkoopdocumenten toepassen, bijvoorbeeld een andere geboekte verkoopfactuur, omdat de klant ook artikelen terugzendt die met die factuur zijn geleverd.

## <a name="create-a-sales-return-order-based-on-one-or-more-posted-sales-documents"></a>Een verkoopretourorder maken op basis van een of meer geboekte verkoopdocumenten

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopretourorders** in en kies vervolgens de gerelateerde koppeling
2. Kies de actie **Nieuw**.  
3. Vul de velden op het sneltabblad **Algemeen** in met de benodigde gegevens.
4. Vul op het sneltabblad **Regels** de regels handmatig in of kopieer informatie vanuit andere documenten om de regels automatisch in te vullen:

    - Met de functie **Geboekte documentregels ophalen voor tegenboeking** kopieert u een of meer geboekte documentregels uit een of meer geboekte documenten. Deze functie boekt altijd exact de kosten tegen vanuit de geboekte documentregel. Deze functie wordt in de volgende stappen beschreven.    
    - Met de functie **Kopiëren uit document** kunt u een bestaand document kopiëren naar de retourorder. Gebruik deze functie om het volledige document te kopiëren. Dit kan een geboekt document zijn of een document dat nog niet is geboekt. Deze functie maakt exact tegenboeken van de kosten alleen mogelijk als het selectievakje **Precieze kostenvereff. verplicht** op de pagina **Verkoopinstellingen** is ingeschakeld.  

5. Kies de actie **Verwerken** en kies dan de actie **Geboekte documentregels ophalen om terug te draaien**.
6. Schakel bovenaan de pagina **Geboekte verkoopdocumentregels** het selectievakje **Alleen tegengeboekte regels weergeven** in als u alleen regels wilt weergeven die aantallen bevatten die nog niet zijn geretourneerd. Als een aantal op een geboekte verkoopfactuur bijvoorbeeld al is geretourneerd, wilt u dat aantal bijvoorbeeld mogelijk niet retourneren op een nieuw verkoopretourdocument.

    > [!NOTE]  
    >  Dit veld werkt alleen voor geboekte verzendingen en geboekte factuurregels, en niet voor geboekte retouren of geboekte creditnotaregels.

    Links op de pagina worden de andere documenttypen weergegeven. Het aantal tussen haakjes geeft aan hoeveel documenten beschikbaar zijn van elk documenttype.

7. Selecteer in het veld **Documentsoortfilter**, het soort geboekte documentregels dat u wilt gebruiken.  
8. Selecteer de regels die u naar het nieuwe document wilt kopiëren.  

    > [!NOTE]  
    >  Als u <kbd>Ctrl</kbd>+<kbd>A</kbd> gebruikt om alle regels te selecteren, worden alle regels gekopieerd binnen het filter dat u hebt ingesteld, maar wordt geen rekening gehouden met het filter **Alleen tegengeboekte regels weergeven**. Stel dat u bijvoorbeeld de regels hebt gefilterd op een bepaald documentnummer met twee regels, waarvan er een al is geretourneerd. Zelfs als het veld **Alleen tegengeboekte regels weergeven** is geselecteerd, worden als u op <kbd>Ctrl</kbd>+<kbd>A</kbd> drukt om alle regels te kopiëren, twee regels gekopieerd in plaats van alleen de regel die nog niet is tegengeboekt.  

9. Kies de knop **OK** om de regels te kopiëren naar het nieuwe document.  

    De volgende processen worden dan uitgevoerd:  

    -   Voor geboekte documentregels van het type **Artikel** wordt een nieuwe documentregel gemaakt die een kopie is van de geboekte documentregel, met het aantal dat nog niet is tegengeboekt. In het veld **Vereffenen met artikelpost** wordt indien nodig het nummer van de artikelpost van de geboekte documentregel ingevuld.  

    -   Voor geboekte documentregels die niet van het type **Artikel** zijn, zoals artikeltoeslagen, wordt een nieuwe documentregel gemaakt die een kopie is van de oorspronkelijke geboekte documentregel.  

    -   Het veld **Kostprijs (LV)** wordt op de nieuwe regel berekend uit de kosten op de overeenkomstige artikelposten.  

    -   Als het gekopieerde document een geboekte verzending, geboekte ontvangst, geboekte retourontvangst of geboekte retourzending is, wordt de kostprijs berekend uit de artikelkaart.  

    -   Als het gekopieerde document een geboekte factuur of creditnota is, worden de kostprijs, factuurkortingen en regelkortingen gekopieerd uit de geboekte documentregel.  

    -   Als de geboekte documentregel artikeltraceringsregels bevat, wordt het veld **Vereffenen met artikelpost** op de artikeltraceringsregel gevuld met de desbetreffende artikelpostnummers uit de geboekte artikeltraceringsregels.  

     Wanneer u vanuit een geboekte factuur of geboekte creditnota kopieert, worden alle relevante factuurkortingen en regelkortingen die geldig zijn op het moment van boeking, gekopieerd van het geboekte document naar de nieuwe documentregel. Houd er echter rekening mee dat als de optie **Factuurkorting berekenen** is geactiveerd op de pagina **Verkoopinstellingen**, de factuurkorting opnieuw wordt berekend als u de nieuwe documentregel boekt. Het kan daardoor gebeuren dat het regelbedrag voor de nieuwe regel afwijkt van het regelbedrag voor de geboekte documentregel, afhankelijk van de nieuwe berekening van de factuurkorting.  

     > [!NOTE]  
     >  Als een deel van de hoeveelheid van de geboekte documentregel als is tegengeboekt of verkocht of geconsumeerd, wordt alleen een regel gemaakt voor de hoeveelheid die nog in voorraad is of die nog niet is geretourneerd. Als de volledige hoeveelheid van de geboekte documentregels al is tegengeboekt, wordt geen nieuwe documentregel gemaakt.  
     >   
     >  Als de goederenstroom in het geboekte document gelijk is aan de goederenstroom in het nieuwe document, wordt gewoon een kopie van de oorspronkelijke geboekte documentregel gemaakt in het nieuwe document. Het veld **Vereffenen met artikelpost** wordt niet ingevuld, omdat in dit geval het exact tegenboeken van kosten niet mogelijk is. Als u bijvoorbeeld de functie **Geboekte documentregels ophalen voor tegenboeking** wilt gebruiken om een geboekte verkoopcreditnotaregel op te halen voor een nieuwe verkoopcreditnota, wordt alleen de oorspronkelijke creditnotaregel naar de nieuwe creditnota gekopieerd.  

10. Selecteer op de pagina **Verkoopretourorder** in het veld **Retourreden** op elke regel de reden voor de retour.
11. Kies de actie **Boeken**.

## <a name="to-create-a-replacement-sales-order-from-a-sales-return-order"></a>Een vervangingsverkooporder maken vanuit de verkoopretourorder
U kunt een klant compenseren voor een artikel dat u deze hebt verkocht door het artikel te vervangen. U kunt het artikel vervangen door hetzelfde of een ander artikel. Dit kan voorkomen als u bijvoorbeeld per ongeluk het verkeerde artikel verzendt naar de klant.  

1. Maak op de pagina **Verkoopretourorder** voor een actief retourproces op een lege regel een negatieve post aan voor het vervangende artikel, door een negatief bedrag in te voeren in het veld **Aantal**.  
2. Kies de actie **Negatieve regels verplaatsen**.
3. Vul op de pagina **Neg. verkoopregels verplaatsen** in de velden de gewenste gegevens in.
4. Kies de knop **OK**. De negatieve regel voor het vervangende artikel wordt verwijderd uit de verkoopretourorder en toegevoegd op een nieuwe pagina **Verkooporder**. Zie [Producten verkopen](sales-how-sell-products.md) voor meer informatie.

## <a name="to-create-return-related-documents-from-a-sales-return-order"></a>Retourgerelateerde documenten maken uit een verkoopretourorder
U kunt automatisch vervangende verkooporders, verkoopretourorders en vervangingsverkooporders laten aanmeken in het verkoopretourproces. Dit is bijvoorbeeld nuttig in situaties waarin u artikelen wilt verwerken met door de leveranciers aangeboden garantie.

1. Kies op de pagina **Verkoopretourorder** voor een actief retourproces de actie **Retourgerel. documenten maken**.
2. Voer in het veld **Leveranciersnr.** het nummer van een leverancier in, als u leverancierdocumenten automatisch wilt laten maken.
3. Als een geretourneerd artikel moet worden geretourneerd naar de leverancier, schakelt u het selectievakje **Inkoopretourorder maken** in.
4. Als een geretourneerd artikel moet worden besteld bij de leverancier, schakelt u het selectievakje **Inkooporder maken** in.
5. Als een vervangingsverkooporder moet worden gemaakt, schakelt u het selectievakje **Verkooporder maken** in.

## <a name="to-create-a-restock-charge"></a>Een toeslag opnieuw bevoorraden maken
U kunt de klant een herbevoorradingstoeslag berekenen om de kosten van het terugsturen van het artikel te dekken. Dit kan bijvoorbeeld voorkomen als de klant per ongeluk het verkeerde artikel heeft besteld of zich heeft bedacht na ontvangst van het artikel.

U kunt deze verhoogde kosten als artikeltoeslag boeken in een creditnota of retourorder en vervolgens toewijzen aan de geboekte verzending. De volgende beschrijving behandelt dit voor een verkoopretourorder, maar dezelfde stappen zijn van toepassing op een verkoopcreditnota.

1. Open de pagina **Verkoopretourorder** voor een actief retourproces.
2. Selecteer op een nieuwe regel in het veld **Type** **Toeslag (Artikel)**.  
3. Vul de velden in net als voor eventuele artikeltoeslagregels. Zie voor meer informatie [Artikeltoeslagen gebruiken om extra handelskosten te verantwoorden](payables-how-assign-item-charges.md)  

Wanneer u de verkoopretourorder boekt, wordt de toeslag opnieuw bevoorraden toegevoegd aan het bijbehorende verkooppostbedrag. Op deze manier kunt u de waardering van uw voorraad correct bijhouden.  

## <a name="see-also"></a>Zie ook

[Verkoop](sales-manage-sales.md)  
[Verkopen instellen](sales-setup-sales.md)  
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Documenten verzenden via e-mail](ui-how-send-documents-email.md)  
[Inkoopretouren of annuleringen verwerken](purchasing-how-process-purchase-returns-cancellations.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
