---
title: Retouren of annuleringen verwerken
description: Legt uit hoe u een inkoopcreditnota maakt en boekt wanneer u artikelen wilt retourneren aan een leverancier of ingekochte services wilt annuleren.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'cancel, undo, correct'
ms.search.form: '6640, 6643, 9307, 9309, 9308, 6652, 145, 147'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Inkoopretouren of annuleringen verwerken

Als u artikelen wilt retourneren naar uw leverancier of services die u hebt aangeschaft, wilt annuleren, kunt u een inkoopcreditnota maken en boeken met de aangevraagde wijziging voor de oorspronkelijke inkoopfactuur. Als u de correcte inkoopfactuurinformatie wilt opnemen, kunt u de inkoopcreditnota rechtstreeks vanuit de geboekte inkoopfactuur maken, of een nieuwe inkoopcreditnota maken met gekopieerde informatie uit de factuur.

Als u meer controle wilt hebben over het inkoopretourproces, zoals magazijndocumenten voor het hanteren van het artikel of beter overzicht bij het terugsturen van meerdere inkoopdocumenten bij één enkele inkoopretourzending, kunt u inkoopretourorders maken. Een inkoopretourorder geeft automatisch de bijbehorende inkoopcreditnota aan. Zie voor meer informatie [Een inkoopretourorder maken op basis van een of meer geboekte inkoopdocumenten](purchasing-how-process-purchase-returns-cancellations.md#to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice).

> [!NOTE]  
> Als een geboekte inkoopfactuur nog niet is voldaan, kunt u de functie **Corrigeren** of **Annuleren** op de geboekte inkoopfactuur gebruiken om de betreffende transacties automatisch tegen te boeken. Deze functies werken alleen voor niet-betaalde facturen en ze ondersteunen geen gedeeltelijke retourneringen of annuleringen. U kunt inkoopfacturen die zijn geboekt met ontvangsten van meer dan één inkooporder ook niet corrigeren of annuleren. Zie voor meer informatie [Onbetaalde inkoopfacturen corrigeren of annuleren](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).

Doorgaans maakt u een inkoopcreditnota of een inkoopretourorder als reactie op een creditnota die u ontvangt van een leverancier. De inkoopcreditnota of de inkoopretourorder vormt uw interne documentatie van het creditnotaproces ten behoeve van de boekhouding of om de verzending van de betrokken artikelen te regelen.

De wijziging kan op alle producten op de oorspronkelijke inkoopfactuur, of slechts op sommige producten, betrekking hebben. Dienovereenkomstig kunt u ontvangen artikelen gedeeltelijk retourneren of gedeeltelijke terugbetaling van ontvangen services aanvragen. In dat geval moet u de gegevens op de inkoopcreditnota of de inkoopretourorder bewerken.

Naast de oorspronkelijke geboekte inkoopfactuur kunt u de inkoopcreditnota of de inkoopretourorder op andere inkoopdocumenten toepassen, bijvoorbeeld een andere geboekte inkoopfactuur, omdat u ook artikelen terugzendt die met die factuur zijn geleverd.

De creditnotaboeking draait ook eventuele artikeltoeslagen terug die aan het geboekte document zijn toegewezen, zodat de waardeposten van het artikel hetzelfde zijn als voordat de artikeltoeslag is toegewezen.

## Voorraadwaardering
Om de juiste voorraadwaardering te behouden, wilt u meestal retourartikelen uit de voorraad picken tegen de eenheidskostprijs waarvoor ze zijn ingekocht en niet tegen de huidige eenheidskostprijs. Dit wordt exacte kostentegenboeking genoemd.

Er zijn twee functies om kosten automatisch exact tegen te boeken.  

|Functie|Description|  
|------------------|---------------------------------------|  
|De functie **Geboekte documentregels ophalen voor tegenboeking** op de pagina **Inkoopretourorder**|Kopieert regels van een of meer geboekte documenten, die in de inkoopretourorder worden tegengeboekt. Zie voor meer informatie [Een inkoopretourorder maken op basis van een of meer geboekte inkoopdocumenten](purchasing-how-process-purchase-returns-cancellations.md#to-create-a-purchase-return-order-based-on-one-or-more-posted-purchase-documents).|  
|De functie **Kopiëren uit document** op de pagina's **Inkoopcreditnota** en **Inkoopretourorder**|Kopieert zowel de kop als de regels van één geboekt document voor tegenboeking.<br /><br /> Vereist dat het selectievakje **Precieze kostenvereff. verplicht** is ingeschakeld op de pagina **Inkoopinstellingen**.|

Als u exacte tegenboeking van kosten handmatig wilt toewijzen, moet u het veld **Vereffenen met artikelpost** selecteren op elk soort retourdocumentregel en vervolgens het nummer van de oorspronkelijke inkooppost selecteren. Hierdoor wordt de inkoopcreditnota of de inkoopretourorder gekoppeld aan de oorspronkelijke inkooppost en wordt het artikel gewaardeerd tegen de oorspronkelijke kostprijs.

Zie voor meer informatie [Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md).

## Een nieuwe inkoopcreditnota maken vanuit een geboekte inkoopfactuur

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Geboekte inkoopfacturen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer op de pagina **Geboekte inkoopfacturen** de geboekte inkoopfactuur die u wilt tegenboeken en kies vervolgens de actie **Corrigerende creditnota maken**.

    De meeste velden op de inkoopcreditnotakop worden ingevuld met de gegevens van de geboekte inkoopfactuur. U kunt alle velden bewerken, bijvoorbeeld met nieuwe gegevens die overeenkomen met de retourovereenkomst.
3. Bewerk informatie op de regels volgens de overeenkomst, zoals het nummer van geretourneerde artikelen of het terug te betalen bedrag.
4. Kies de actie **Posten vereffenen**.
5. Selecteer op de pagina **Leveranciersposten vereffenen** de regel met het geboekte inkoopdocument waarmee u de inkoopcreditnota wilt vereffenen, en kies vervolgens de actie **Vereffenings-id**. Het nummer van de inkoopcreditnota wordt ingevoegd in het veld **Vereffenings-id**.
6. Voer in het veld **Te vereffenen bedrag** het bedrag in dat u wilt vereffenen als het kleiner is dan het oorspronkelijke bedrag.

    Onder op de pagina **Leveranciersposten vereffenen** ziet u het totale te vereffenen bedrag om alle betrokken posten tegen te boeken, namelijk als de waarde in het veld **Saldo** nul is.
7. Kies de knop **Ok**. Wanneer u de inkoopcreditnota boekt, wordt deze vereffend met de opgegeven geboekte inkoopdocumenten.

    Wanneer u de nodige inkoopcreditnotaregels hebt gemaakt of bewerkt en de enkele of meerdere vereffeningen worden opgegeven, kunt u doorgaan om de inkoopcreditnota te boeken.
8. Kies de actie **Boeken**.

De geboekte inkoopfacturen die u met de creditnota vereffent, worden nu tegengeboekt. Als u de oorspronkelijke factuur al hebt betaald, moet de leverancier de betaling nu aan u terugbetalen. Als de creditnota slechts voor een gedeelte van het product op de oorspronkelijke factuur is, kunt u alleen het resterende bedrag op de oorspronkelijke inkoopfactuur betalen om deze te sluiten.

De inkoopcreditnota wordt verwijderd en vervangen door een nieuw document in de lijst met geboekte inkoopcreditnota's.

## Een nieuwe inkoopcreditnota maken door een geboekte inkoopfactuur te kopiëren.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Inkoopcreditnota's** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw** om een nieuwe lege inkoopcreditnota te openen.
3. Voer in het veld **Leverancier** de naam in van een bestaande leverancier.
4. Kies de actie **Kopiëren uit document**.
5. Selecteer op de pagina **Inkoopdocument kopiëren** in het veld **Documentsoort** **Geboekte factuur**.
6. Selecteer het veld **Documentnr.** om de pagina **Geboekte inkoopfacturen** te openen, en selecteer vervolgens de geboekte inkoopfactuur met de regels die u wilt tegenboeken.
7. Schakel het selectievakje **Regels opnieuw berekenen** in als u wilt dat de gekopieerde geboekte inkoopfactuurregels worden bijgewerkt met de wijzigingen in de artikelprijs en kostprijs sinds de factuur is geboekt.
8. Kies de knop **Ok**. De gekopieerde factuurregels worden ingevoegd in de kredietnota van de aankoop.
9. Voltooi de inkoopcreditnota, zoals is uitgelegd in [Een nieuwe inkoopcreditnota maken vanuit een geboekte inkoopfactuur](purchasing-how-process-purchase-returns-cancellations.md#to-create-a-purchase-credit-memo-from-a-posted-purchase-invoice).

## Een inkoopretourorder maken op basis van een of meer geboekte inkoopdocumenten

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopretourorders** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Vul de velden op het sneltabblad **Algemeen** in met de benodigde gegevens.
4. Vul op het sneltabblad **Regels** de regels handmatig in of kopieer informatie vanuit andere documenten om de regels automatisch in te vullen:

    - Met de functie **Geboekte documentregels ophalen voor tegenboeking** kopieert u een of meer geboekte documentregels uit een of meer geboekte documenten. Deze functie boekt altijd exact de kosten tegen vanuit de geboekte documentregel. Deze functie wordt in de volgende stappen beschreven.    
    - Met de functie **Kopiëren uit document** kunt u een bestaand document kopiëren naar de retourorder. Gebruik deze functie om het volledige document te kopiëren. Dit kan een geboekt document zijn of een document dat nog niet is geboekt. Deze functie maakt exact tegenboeken van de kosten alleen mogelijk als het selectievakje **Precieze kostenvereff. verplicht** op de pagina **Verkoopinstellingen** is ingeschakeld.  

5. Kies de actie **Geboekte documentregels ophalen voor tegenboeking**.
6. Schakel bovenaan de pagina **Geboekte inkoopdocumentregels** het selectievakje **Alleen tegengeboekte regels weergeven** in als u alleen regels wilt weergeven die aantallen bevatten die nog niet zijn geretourneerd. Als bijvoorbeeld een aantal op een geboekte inkoopfactuur al is geretourneerd, wilt u dat aantal misschien niet opnemen op een nieuw inkoopretourdocument.

    > [!NOTE]  
    >  Dit veld werkt alleen voor geboekte ontvangsten en geboekte factuurregels, en niet voor geboekte retouren of geboekte creditnotaregels.  

    Links op de pagina worden de andere documenttypen weergegeven. Het aantal tussen haakjes geeft aan hoeveel documenten beschikbaar zijn van elk documenttype.

7. Selecteer in het veld **Documentsoortfilter**, het soort geboekte documentregels dat u wilt gebruiken.  
8. Selecteer de regels die u naar het nieuwe document wilt kopiëren.  

    > [!NOTE]  
    >  Als u <kbd>Ctrl</kbd>+<kbd>A</kbd> gebruikt om alle regels te selecteren, worden alle regels gekopieerd binnen het filter dat u hebt ingesteld, maar wordt geen rekening gehouden met het filter **Alleen tegengeboekte regels weergeven**. Stel dat u bijvoorbeeld de regels hebt gefilterd op een bepaald documentnummer met twee regels, waarvan er een al is geretourneerd. Zelfs als het veld **Alleen tegengeboekte regels weergeven** is geselecteerd, worden als u op <kbd>Ctrl</kbd>+<kbd>A</kbd> drukt om alle regels te kopiëren, twee regels gekopieerd in plaats van alleen de regel die nog niet is tegengeboekt.  

9. Kies de knop **OK** om de regels te kopiëren naar het nieuwe document.  

    De volgende processen worden dan uitgevoerd:  

    - Voor geboekte documentregels van het type **Artikel** wordt een nieuwe documentregel gemaakt die een kopie is van de geboekte documentregel, met het aantal dat nog niet is tegengeboekt. In het veld **Vereffeningsnr. artikelpost** wordt indien nodig het nummer van de artikelpost van de geboekte documentregel ingevuld.  

    - Voor geboekte documentregels die niet van het type **Artikel** zijn, zoals artikeltoeslagen, wordt een nieuwe documentregel gemaakt die een kopie is van de oorspronkelijke geboekte documentregel.  

    - Het veld **Kostprijs (LV)** wordt op de nieuwe regel berekend uit de kosten op de overeenkomstige artikelposten.  

    - Als het gekopieerde document een geboekte verzending, geboekte ontvangst, geboekte retourontvangst of geboekte retourzending is, wordt de kostprijs berekend uit de artikelkaart.  

    - Als het gekopieerde document een geboekte factuur of creditnota is, worden de kostprijs, factuurkortingen en regelkortingen gekopieerd uit de geboekte documentregel.  

    - Als de geboekte documentregel artikeltraceringsregels bevat, wordt het veld **Vereffenen met artikelpost** op de artikeltraceringsregel gevuld met de desbetreffende artikelpostnummers uit de geboekte artikeltraceringsregels.  

     Wanneer u vanuit een geboekte factuur of geboekte creditnota kopieert, worden alle relevante factuurkortingen en regelkortingen die geldig zijn op het moment van boeking, gekopieerd van het geboekte document naar de nieuwe documentregel. Houd er echter rekening mee dat als de optie **Factuurkorting berekenen** is geactiveerd op de pagina **Inkoopinstellingen**, de factuurkorting opnieuw wordt berekend als u de nieuwe documentregel boekt. Het kan daardoor gebeuren dat het regelbedrag voor de nieuwe regel afwijkt van het regelbedrag voor de geboekte documentregel, afhankelijk van de nieuwe berekening van de factuurkorting.  

    > [!NOTE]  
    >  Als een deel van de hoeveelheid van de geboekte documentregel als is tegengeboekt of verkocht of geconsumeerd, wordt alleen een regel gemaakt voor de hoeveelheid die nog in voorraad is of die nog niet is geretourneerd. Als de volledige hoeveelheid van de geboekte documentregels al is tegengeboekt, wordt geen nieuwe documentregel gemaakt.  
    >
    >  Als de goederenstroom in het geboekte document gelijk is aan de goederenstroom in het nieuwe document, wordt gewoon een kopie van de oorspronkelijke geboekte documentregel gemaakt in het nieuwe document. Het veld **Vereffenen met artikelpost** wordt niet ingevuld, omdat in dit geval het exact tegenboeken van kosten niet mogelijk is. Als u bijvoorbeeld met de functie **Geboekte documentregels ophalen voor tegenboeking** een geboekte inkoopcreditnotaregel wilt ophalen voor een nieuwe inkoopcreditnota, wordt alleen de oorspronkelijke creditnotaregel naar de nieuwe creditnota gekopieerd.  

10. Selecteer op de pagina **Inkoopretourorder** in het veld **Retourreden** op elke regel de reden voor de retour.
11. Kies de actie **Boeken**.

## Een vervangende inkooporder maken vanuit een inkoopretourorder

U kunt met de leverancier afspreken dat deze een ingekocht artikel vervangt. Het vervangende artikel kan hetzelfde of een ander artikel zijn. Dit kan voorkomen als de leverancier per ongeluk het verkeerde artikel verzendt.  

1.  Maak op de pagina **Inkoopretourorder** voor een actief retourproces op een lege regel een negatieve post aan voor het vervangende artikel, door een negatief bedrag in te voeren in het veld **Aantal**.  
2. Kies de actie **Negatieve regels verplaatsen**.  
3. Vul op de pagina **Neg. inkoopregels verplaatsen** in de velden de gewenste gegevens in.
4. Kies de knop **OK**. De negatieve regel wordt verwijderd uit de inkoopretourorder en er wordt een nieuwe inkooporder gemaakt. Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md).  

## Een inkooptegoed maken

Als u van de leverancier artikelen ontvangt die niet naar wens zijn, bijvoorbeeld omdat ze licht zijn beschadigd, de verkeerde kleur of het verkeerde formaat hebben, biedt de leverancier u misschien een inkooptegoed aan.  

U kunt deze korting op de inkoopkosten als artikeltoeslag op een creditnota of retourorder boeken en deze aan de geboekte ontvangst koppelen. De volgende beschrijving behandelt dit voor een inkoopretourorder, maar dezelfde stappen zijn van toepassing op een inkoopcreditnota.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Inkoopcreditnota's** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw** om een nieuwe lege inkoopcreditnota te openen.  
3. Vul op de creditnotakop de gegevens in van de leverancier die u het inkooptegoed heeft gestuurd.  
4. Selecteer **Toeslag (artikel)** in het veld **Soort** op het sneltabblad **Regels**.  
5. Selecteer in het veld **Nr.** de juiste artikeltoeslagwaarde.  

    Stel desgewenst een speciaal artikeltoeslagnummer voor inkooptegoeden in.  
6. Geef **1** op in het veld **Aantal**.  
7. Typ in het veld **Directe kostprijs** het bedrag van het inkooptegoed.  
8. Nu moet u het inkooptegoed als artikeltoeslag  toewijzen aan de artikelen op de geboekte ontvangst. Zie voor meer informatie [Artikeltoeslagen gebruiken om extra handelskosten te verantwoorden](payables-how-assign-item-charges.md) Wanneer u het tegoed hebt toegewezen, gaat u terug naar de pagina **Inkoopcreditnota**.

Wanneer u de inkoopretourorder boekt, wordt het inkooptegoed opnieuw toegevoegd aan het bedrag van de betreffende inkooppost. Op deze manier kunt u de waardering van uw voorraad correct bijhouden.  

## Retourverzendingen combineren

Als u artikelen wilt retourneren die onder verschillende inkoopretourorders voor dezelfde fabrikant vallen, kunt u de functie **Retourverzendingen combineren** gebruiken.  

Wanneer u de artikelen verzendt, boekt u de bijbehorende inkoopretourorders als verzonden. Er worden dan geboekte inkoopretourverzendingen gemaakt.  

Wanneer u deze artikelen wilt gaan factureren, kunt u in plaats van elke inkoopretourorder afzonderlijk te factureren, een inkoopcreditnota maken en de geboekte inkoopretourverzendingsregels automatisch naar dit document kopiëren. Vervolgens kunt u de inkoopcreditnota boeken en gemakkelijk alle openstaande inkoopretourorders tegelijk factureren.  

Wanneer retourverzendingen zijn gecombineerd op een creditnota en zijn geboekt, wordt een geboekte inkoopcreditnota gemaakt voor de gefactureerde regels. Het veld **Gefactureerd aantal** op de onderliggende inkoopretourorder wordt bijgewerkt op basis van het gefactureerde aantal. Deze oorspronkelijke inkoopretourorder wordt echter niet verwijderd, zelfs als deze volledig is ontvangen en gefactureerd en daarom moet u de inkoopretourorder handmatig verwijderen.

> [!NOTE]  
> In de volgende procedure wordt ervan uitgegaan dat er meerdere inkoopretourorders zijn voor de leverancier en dat deze zijn geboekt als verzonden.     

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Inkoopcreditnota's** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Vul indien nodig de velden op het sneltabblad **Algemeen** in.  
4. Kies de actie **Retourverzendregels ophalen**.  
5. Selecteer meerdere retourverzendregels die u wilt opnemen in de factuur.  

    Als een onjuiste retourverzendregel is geselecteerd of als u opnieuw wilt beginnen, kunt u de regels op de inkoopcreditnota gewoon verwijderen en vervolgens de functie **Retourverzendregels ophalen** opnieuw gebruiken.  
6. Kies de actie **Boeken**.  

### Open inkoopretourorders verwijderen na gecombineerde boeking van retourverzendingen  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Gefactureerde inkoopretourorders verwijderen** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de overige velden desgewenst in en kies de knop **OK**.  
3. U kunt de afzonderlijke inkoopretourorders ook handmatig verwijderen.

## Zie ook
[Inkoop](purchasing-manage-purchasing.md)  
[Inkopen vastleggen](purchasing-how-record-purchases.md)  
[Niet-betaalde inkoopfacturen corrigeren of annuleren](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Verkoopretouren of annuleringen verwerken](sales-how-process-sales-returns-cancellations.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
