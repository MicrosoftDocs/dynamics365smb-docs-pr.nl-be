---
title: Verkoopretouren of annuleringen verwerken | Microsoft Docs
description: Beschrijft hoe u een verkoopcreditnota maakt, rechtstreeks of via een verkoopretourorder, om een retour, een annulering of terugbetaling te verwerken voor artikelen of diensten waarvoor u betaling hebt ontvangen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: undo, credit memo, return
ms.date: 03/01/2019
ms.author: sgroespe
ms.openlocfilehash: 46ea7cb3402f65d897cc8519a062ebbf8fb9b383
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "816477"
---
# <a name="process-sales-returns-or-cancellations"></a>Verkoopretouren of annuleringen verwerken
Als een klant artikelen wil retourneren of terugbetaling wil krijgen voor artikelen of services die u klant hebt verkocht en waarvoor u een betaling hebt ontvangen, moet u een verkoopcreditnota maken en boeken waarmee de gevraagde wijziging wordt opgegeven. Als u de correcte verkoopfactuurinformatie wilt opnemen, kunt u de verkoopcreditnota rechtstreeks vanuit de geboekte verkoopfactuur maken, of een nieuwe verkoopcreditnota maken met gekopieerde informatie uit de factuur.

Als u meer controle wilt hebben over het verkoopretourproces, zoals magazijndocumenten voor het hanteren van het artikel of beter overzicht bij het ontvangen van artikelen van meerdere verkoopdocumenten bij één enkele verkoopretourzending, kunt u verkoopretourorders maken. Een verkoopretourorder geeft automatisch de gerelateerde verkoopcreditnota en andere retourgerelateerde documenten uit, zoals een vervangende verkooporder, indien noodzakelijk. Zie voor meer informatie [Een verkoopretourorder maken op basis van een of meer geboekte verkoopdocumenten](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-return-order-based-on-one-or-more-a-posted-sales-documents).

> [!NOTE]  
>   Als een geboekte verkoopfactuur nog niet is voldaan, kunt u de functie **Corrigeren** of **Annuleren** voor de geboekte verkoopfactuur gebruiken om transacties tegen te boeken. Deze functies werken alleen voor niet-betaalde facturen en ze ondersteunen geen gedeeltelijke retouren of annuleringen. Zie voor meer informatie [Onbetaalde verkoopfacturen corrigeren of annuleren](sales-how-correct-cancel-sales-invoice.md).

Een retour of terugbetaling kan betrekking hebben op slechts enkele artikelen of services op de oorspronkelijke verkoopfactuur. In dat geval moet u de gegevens in de regels van de verkoopcreditnota of de verkoopretourorder bewerken. Wanneer u de verkoopcreditnota of de verkoopretourorder boekt, worden de door de wijziging beïnvloede verkoopdocumenten tegengeboekt en een terugbetaling voor de klant kan worden gemaakt. Zie voor meer informatie [Betalingen doen](payables-make-payments.md).  

Naast de oorspronkelijke geboekte verkoopfactuur kunt u de verkoopcreditnota of verkoopretourorder op andere verkoopdocumenten toepassen, bijvoorbeeld een andere geboekte verkoopfactuur, omdat de klant ook artikelen terugzendt die met die factuur zijn geleverd.

U kunt de geboekte verkoopcreditnota naar de klant verzenden om de retournering of annulering te bevestigen en mede te delen dat de betreffende waarde wordt terugbetaald, bijvoorbeeld wanneer de artikelen zijn geretourneerd.

De creditnotaboeking draait ook eventuele artikeltoeslagen terug die aan het geboekte document zijn toegewezen, zodat de waardeposten van het artikel hetzelfde zijn als voordat de artikeltoeslag is toegewezen.

## <a name="inventory-costing"></a>Voorraadwaardering
Om de juiste voorraadwaardering te behouden, wilt u meestal retourartikelen in de voorraad terugzetten tegen de eenheidskostprijs waarvoor ze zijn verkocht en niet tegen de huidige eenheidskostprijs. Dit wordt exacte kostentegenboeking genoemd.

Er zijn twee functies om kosten automatisch exact tegen te boeken.   

|Functie|Description|  
|------------------|---------------------------------------|  
|De functie **Geboekte documentregels ophalen voor tegenboeking** op de pagina **Verkoopretourorder**|Kopieert regels van een of meer geboekte documenten, die in de verkoopretourorder worden tegengeboekt. Zie voor meer informatie [Een verkoopretourorder maken op basis van een of meer geboekte verkoopfacturen](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-return-order-based-on-one-or-more-a-posted-sales-documents).|  
|De functie **Document kopiëren** op de pagina's **Verkoopcreditnota** en **Verkoopretourorder**|Kopieert zowel de kop als de regels van één geboekt document voor tegenboeking.<br /><br /> Vereist dat het selectievakje **Precieze kostenvereff. verplicht** is ingeschakeld op de pagina **Instellingen van verkoop en tegoeden**.|

Als u exacte tegenboeking van kosten handmatig wilt toewijzen, moet u het veld **Vereffenen met artikelpost** selecteren op elk soort retourdocumentregel en vervolgens het nummer van de oorspronkelijke verkooppost selecteren. Hierdoor wordt de verkoopcreditnota gekoppeld aan de oorspronkelijke verkooppost en wordt het artikel gewaardeerd op de oorspronkelijke kostprijs.

Zie voor meer informatie [Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md).

## <a name="to-create-a-sales-credit-memo-from-a-posted-sales-invoice"></a>Een verkoopcreditnota maken op basis van een geboekte verkoopfactuur
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Geboekte verkoopfacturen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer op de pagina **Geboekte verkoopfacturen** de geboekte verkoopfactuur die u wilt tegenboeken en kies vervolgens de actie **Corrigerende creditnota maken**.

    De koptekst van de verkoopcreditnota bevat enkele gegevens uit de geboekte verkoopfactuur. U kunt deze gegevens bewerken, bijvoorbeeld met nieuwe gegevens die overeenkomen met de retourovereenkomst.  
3. Bewerk de informatie op de regels volgens de overeenkomst, zoals het aantal geretourneerde artikelen of het terug te betalen bedrag.
4. Kies de actie **Posten vereffenen**.
5. Selecteer op de pagina **Klantposten vereffenen** de regel met het geboekte verkoopdocument waarmee u de verkoopcreditnota wilt vereffenen, en kies vervolgens de actie **Vereffenings-id**.

    De id van de verkoopcreditnota is zichtbaar in het veld **Vereffenings-id**.
6. Voer in het veld **Te vereffenen bedrag** het bedrag in dat u wilt vereffenen, als dit lager is dan het oorspronkelijke bedrag.  

    Onder op de pagina **Klantposten vereffenen** ziet u het totale te vereffenen bedrag om alle betrokken posten tegen te boeken, namelijk als de waarde in het veld **Saldo** nul is.
7. Kies de knop **Ok**. Wanneer u de verkoopcreditnota boekt, wordt deze vereffend met de geboekte verkoopdocumenten.

    Nadat u de nodige verkoopcreditnotaregels hebt gemaakt of bewerkt en de enkele of meerdere vereffeningen zijn opgegeven, kunt u de verkoopcreditnota boeken.   
8. Kies de actie **Boeken en verzenden**.  

Het dialoogvenster **Boeken en verzenden bevestigen** wordt geopend met de geprefereerde verzendmethode voor de klant. U kunt de verzendmethode wijzigen door de opzoekknop voor het veld **Document verzenden naar** te kiezen. Zie [Verzendprofielen voor documenten instellen](sales-how-setup-document-send-profiles.md) voor meer informatie.  

De geboekte verkoopdocumenten die u op de creditnota hebt vereffend, worden nu tegengeboekt en een terugbetaling kan worden gemaakt voor de klant. De verkoopcreditnota wordt verwijderd en vervangen door een nieuw document in de lijst met geboekte verkoopcreditnota's.

## <a name="to-create-a-sales-credit-memo-by-copying-a-posted-sales-invoice"></a>Een verkoopcreditnota maken door een geboekte verkoopfactuur te kopiëren
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopcreditnota's** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw** om een nieuwe lege verkoopcreditnota te openen.
3. Voer in het veld **Klant** de naam in van een bestaande klant.
4. Kies de actie **Document kopiëren**.
5. Selecteer op de pagina **Verkoopdocument kopiëren** in het veld **Documentsoort** **Geboekte factuur**.
6. Selecteer het veld **Documentnr.** om de pagina **Geboekte verkoopfacturen** te openen, en selecteer vervolgens de geboekte verkoopfactuur met de regels die u wilt tegenboeken.
7. Schakel het selectievakje **Regels opnieuw berekenen** in als u wilt dat de gekopieerde geboekte verkoopfactuurregels worden bijgewerkt met de wijzigingen in de artikelprijs en kostprijs sinds de factuur is geboekt.
8. Kies de knop **Ok**. De gekopieerde factuurregels worden ingevoegd in de kredietnota van de verkoop.
9. Voltooi de verkoopcreditnota zoals is uitgelegd in [Een verkoopcreditnota maken op basis van een geboekte verkoopfactuur](sales-how-process-sales-returns-cancellations.md#to-create-a-sales-credit-memo-from-a-posted-sales-invoice).

## <a name="to-create-a-sales-return-order-based-on-one-or-more-posted-sales-documents"></a>Een verkoopretourorder maken op basis van een of meer geboekte verkoopdocumenten
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopretourorders** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.  
3. Vul de velden op het sneltabblad **Algemeen** in met de benodigde gegevens.
4. Vul op het sneltabblad **Regels** de regels handmatig in of kopieer informatie vanuit andere documenten om de regels automatisch in te vullen:

    - Met de functie **Geboekte documentregels ophalen voor tegenboeking** kopieert u een of meer geboekte documentregels uit een of meer geboekte documenten. Deze functie boekt altijd exact de kosten tegen vanuit de geboekte documentregel. Deze functie wordt in de volgende stappen beschreven.    
    - Met de functie **Document kopiëren** kunt u een bestaand document kopiëren naar de retourorder. Gebruik deze functie om het volledige document te kopiëren. Dit kan een geboekt document zijn of een document dat nog niet is geboekt. Deze functie maakt exact tegenboeken van de kosten alleen mogelijk als het selectievakje **Precieze kostenvereff. verplicht** op de pagina **Verkoopinstellingen** is ingeschakeld.  

5. Kies de actie **Geboekte documentregels ophalen voor tegenboeking**.
6. Schakel bovenaan de pagina **Geboekte verkoopdocumentregels** het selectievakje **Alleen tegengeboekte regels weergeven** in als u alleen regels wilt weergeven die aantallen bevatten die nog niet zijn geretourneerd. Als een aantal op een geboekte verkoopfactuur bijvoorbeeld al is geretourneerd, wilt u dat aantal bijvoorbeeld mogelijk niet retourneren op een nieuw verkoopretourdocument.

    > [!NOTE]  
    >  Dit veld werkt alleen voor geboekte verzendingen en geboekte factuurregels, en niet voor geboekte retouren of geboekte creditnotaregels.

    Links op de pagina worden de andere documenttypen weergegeven. Het aantal tussen haakjes geeft aan hoeveel documenten beschikbaar zijn van elk documenttype.

7. Selecteer in het veld **Documentsoortfilter**, het soort geboekte documentregels dat u wilt gebruiken.  
8. Selecteer de regels die u naar het nieuwe document wilt kopiëren.  

    > [!NOTE]  
    >  Als u Ctrl+A gebruikt om alle regels te selecteren, worden alle regels gekopieerd binnen het filter dat u hebt ingesteld, maar wordt geen rekening gehouden met het filter **Alleen tegengeboekte regels** weergeven. Stel dat u bijvoorbeeld de regels hebt gefilterd op een bepaald documentnummer met twee regels, waarvan er een al is geretourneerd. Zelfs als het veld **Alleen tegengeboekte regels weergeven** is geselecteerd, worden als u op Ctrl+A drukt om alle regels te kopiëren, twee regels gekopieerd in plaats van alleen de regel die nog niet is tegengeboekt.  

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

## <a name="to-create-a-sales-allowance"></a>Een verkoopprijskorting maken
U kunt een klant een creditnota sturen met een korting omdat de klant de artikelen bijvoorbeeld met lichte beschadigingen of te laat heeft ontvangen.  
U kunt deze gereduceerde prijs als artikeltoeslag boeken in een creditnota of retourorder en vervolgens toewijzen aan de geboekte verzending. De volgende beschrijving behandelt dit voor een verkoopcreditnota, maar dezelfde stappen zijn van toepassing op een verkoopretourorder.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopcreditnota's** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw** om een nieuwe lege verkoopcreditnota te openen.
3. Vul in de creditnotakop de betreffende gegevens in over de klant aan wie u de verkoopprijskorting wilt geven.  
4. Selecteer **Toeslag (artikel)** in het veld **Soort** op het sneltabblad **Regels**.  
5.  Selecteer in het veld **Nr.** de juiste artikeltoeslagwaarde.  
     Mogelijk wilt u een speciaal artikeltoeslagnummer toewijzen voor verkoopprijskortingen.  
6.  Geef **1** op in het veld **Aantal**.  
7.  Geef het bedrag voor de verkoopprijskorting op in het veld **Eenheidsprijs**.  
8.  Nu kunt u de verkoopprijskorting als artikeltoeslag  toewijzen aan de artikelen op de geboekte verzending. Zie voor meer informatie [Artikeltoeslagen gebruiken om extra handelskosten te verantwoorden](payables-how-assign-item-charges.md) Wanneer u het tegoed hebt toegewezen, gaat u terug naar de pagina **Creditnota**.  

Wanneer u de verkoopretourorder boekt, wordt de verkoopprijskorting toegevoegd aan het bijbehorende verkooppostbedrag. Op deze manier kunt u de waardering van uw voorraad correct bijhouden.

## <a name="to-combine-return-receipts"></a>Retourontvangsten combineren
U kunt retourontvangsten combineren als de klant meerdere artikelen, waarvoor verschillende verkoopretourorders zijn aangemaakt, retourneert.  

Wanneer de artikelen zijn aangekomen in het magazijn, boekt u de betreffende verkoopretourorders als ontvangen. Er worden dan geboekte retourontvangsten aangemaakt.  

Wanneer u deze klant wilt gaan factureren, kunt u in plaats van elke verkoopretourorder afzonderlijk te factureren, een verkoopcreditnota maken en de geboekte retourontvangstregels automatisch naar dit document kopiëren. Vervolgens kunt u de verkoopcreditnota boeken en gemakkelijk alle openstaande verkoopretourorders tegelijk factureren.  

Om retourverzendingen te combineren moet het selectievakje **Verzendingen combineren** zijn ingeschakeld op de pagina **Klantenkaart**.  

### <a name="to-manually-combine-return-receipts"></a>Retourontvangsten handmatig combineren  

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopcreditnota** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.
3. Vul indien nodig de velden op het sneltabblad **Algemeen** in.  
4. Kies de actie **Retourontvangstregels ophalen**.  
5. Selecteer de retourontvangstregels die u in de creditnota wilt opnemen:  

    -   Als u alle regels wilt invoegen, selecteert u alle regels en klikt u op **OK**.  

    -   Als u specifieke regels wilt invoegen, selecteert u deze regels en klikt u op **OK**.  

6.  Als u de verkeerde verzendregel hebt geselecteerd of als u opnieuw wilt beginnen, kunt u de regels op de creditnota verwijderen en de functie **Retourontvangstregels ophalen** opnieuw uitvoeren.  
7.  Boek de factuur.  

### <a name="to-automatically-combine-return-receipts"></a>Retourontvangsten automatisch combineren  
U kunt retourontvangsten automatisch combineren en beschikken over de optie om de creditnota's automatisch te boeken met de functie **Retourontvangsten combineren**.  

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Retourontvangsten combineren** in en kies vervolgens de gerelateerde koppeling.
2. Vul op de pagina **Retourontvangsten combineren** de velden in om de relevante retourontvangsten te selecteren.
3. Schakel het selectievakje **Creditnota's boeken** in. Als u dit niet doet, moet u de resulterende inkoopcreditnota's handmatig boeken.
4.  Kies de knop **OK**.  

### <a name="to-remove-a-received-and-invoiced-return-order"></a>Ontvangen en gefactureerde retourorders verwijderen  
Als u op deze manier retourontvangsten factureert, blijven de retourorders van waaruit de retourontvangsten zijn geboekt bestaan, ook als ze volledig zijn ontvangen en gefactureerd.  

Als retourontvangsten worden gecombineerd op een creditnota en worden geboekt, wordt er een geboekte verkoopcreditnota gemaakt voor de gecrediteerde regels. Het veld **Verzonden aantal** op de oorspronkelijke verkoopretourorder wordt bijgewerkt op basis van het gefactureerde aantal.   
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gefact. verk.-retourorders verwijderen** in en selecteer vervolgens de gerelateerde koppeling.  
2.  Geef in het filterveld **Nr.** op welke retourorders moeten worden verwijderd.  
3.  Kies de knop **Ok**.  

U kunt afzonderlijke retourorders ook handmatig verwijderen.   

## <a name="see-also"></a>Zie ook
[Verkoop](sales-manage-sales.md)  
[Verkopen instellen](sales-setup-sales.md)  
[Documenten per e-mail verzenden](ui-how-send-documents-email.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
