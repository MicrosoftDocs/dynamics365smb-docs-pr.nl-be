---
title: Vooruitbetalingen verkoop instellen en factureren
description: Vooruitbetalingen zijn betalingen die worden gefactureerd en geboekt naar een verkoop- of inkoopvooruitbetalingsorder vóór de definitieve facturering.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 12/03/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Procedure: Vooruitbetalingen verkoop instellen en factureren

Deze procedure leidt u door het proces van het instellen en gebruiken van vooruitbetalingen in [!INCLUDE [prod_short](includes/prod_short.md)]. [!INCLUDE [prepayment_def](includes/prepayment_def.md)]

[!INCLUDE [prepayment_req](includes/prepayment_req.md)]

U kunt bijvoorbeeld meer vooruitbetalingsfacturen versturen, als er meer artikelen worden toegevoegd aan de order.  

## Informatie over deze procedure  

In deze procedure komen de volgende scenario's aan de orde:  

- Vooruitbetalingen instellen  
- Een order maken waarvoor een vooruitbetaling vereist is  
- Een vooruitbetalingsfactuur maken  
- De vooruitbetalingsvereisten voor een order aanpassen  
- Vooruitbetalingen vereffenen met een order  
- Het uiteindelijke bedrag van een order met vooruitbetaling factureren  

### Rollen

Deze procedure bevat taken voor de volgende rollen:  

- Administrateur (Phyllis)  
- Orderverwerker (Susan)  
- Administratie vorderingen (Arnie)  

## Scenario

 Phyllis is administrateur en bepaalt welke klanten een aanbetaling moeten doen voordat artikelen worden gefabriceerd of verzonden. Phyllis stelt [!INCLUDE[prod_short](includes/prod_short.md)] in op het automatisch berekenen van vooruitbetalingen.  

 Susan is verkooporderverwerker. Als een klant belt om een order te plaatsen, voert Susan de order in het systeem in terwijl ze de klant aan de telefoon heeft. Op deze manier kan Susan prijzen en betalingsvoorwaarden meteen met de klant controleren en ze kan wijzigingen in de order aanbrengen terwijl ze met de klant onderhandelt.  

 Arnie werkt op de afdeling Vorderingen en boekt facturen en betalingen.  

 In dit scenario stelt Phyllis vooruitbetalingsvereisten op voor de klant Selangorian op basis van hun kredietgeschiedenis. Phyllis geeft Susan instructies voor het afhandelen van hun bestellingen.  

 Wanneer de klant belt, onderhandelt Susan met de klant totdat ze een overeenkomst bereiken. Ze kiest er vervolgens voor om de vooruitbetaling op verschillende manieren te berekenen.  

 Nadat Susan de vooruitbetalingsfactuur heeft verstuurd, bestelt te klant een extra artikel. Susan werkt de order bij en maakt een tweede vooruitbetalingsfactuur.  

 Arnie registreert de betaling van de klant en past deze toe op de facturen, waarna hij de uiteindelijke factuur stuurt.  

## Vooruitbetalingen instellen

Als administrateur stelt Phyllis het systeem in voor het verwerken van vooruitbetalingen van klanten.  

- Phyllis besluit voor de vooruitbetalingen dezelfde nummerreeks te gebruiken als voor de verkoopfacturen.  
- Phyllis stelt de toepassing in om te controleren of vooruitbetalingen zijn vereist voordat de uiteindelijke factuur voor een order wordt verzonden.  
- Phyllis stelt standaardwaarden in voor een vereist vooruitbetalingspercentage voor bepaalde artikelen en klanten.  

In de volgende procedures wordt beschreven hoe de taken van Phyllis worden uitgevoerd:  

### Nummerreeks voor vooruitbetalingen instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopinstellingen** in en kies vervolgens de gerelateerde koppeling.  
2. Vouw op de pagina **Verkoopinstellingen** het sneltabblad **Nummerreeks** uit.  
3. Controleer of de nummerreeks voor geboekte vooruitbetalingsfacturen in het veld **Geboekte vooruitbetalingsfactuurnrs.** overeenkomt met de reeks voor geboekte verkoopfacturen (**Factuurnrs. (Geboekt)**) en of de nummerreeks voor geboekte vooruitbetalingscreditnota's (**Geboekte vooruitbetalingscreditnotanrs.**) overeenkomt met de reeks voor geboekte creditnota's (**Creditnotanrs. (Geboekt)**).  

### Verzendingen blokkeren voor niet voldane vooruitbetalingen

1. Schakel op de pagina **Verkoopinstellingen** op het sneltabblad **Algemeen** het selectievakje **Vooruitbetaling controleren bij boeken** in.

Nu kunt u geen orders verzenden of factureren waarvoor een niet-betaald vooruitbetalingsbedrag openstaat.  

Phyllis stelt in dat bij klant 20000 standaard een aanbetaling van 30% voor alle orders moet worden gefactureerd. Daarom voert Phyllis een standaardpercentage voor vooruitbetaling in voor de klant.  

Phyllis stelt in dat bij alle klanten een aanbetaling van 20% wordt gefactureerd voor artikel 1896-S. Klant 20000 heeft een slechte betalingsgeschiedenis, dus vereist Phyllis van klant 20000 een aanbetaling van 40% voor artikel 1896-S. In de volgende procedure wordt beschreven hoe de aanbetalingspercentages worden ingesteld.  

### Standaardpercentages voorvooruitbetaling toewijzen aan klanten en artikelen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Klanten** in en kies vervolgens de gerelateerde koppeling.  
2. Open de kaart voor klant 20000 (Trey Research).
3. Voer op het sneltabblad **Betalingen** in het veld **Vooruitbetaling %** de waarde **30** in.  
4. Kies de actie **Gerelateerd**, selecteer de menuoptie **Verkoop** en kies vervolgens de menuoptie **Vooruitbetalingspercentages**.  
5. Vul twee regels op de pagina **Vooruitbetalingspercentages verkoop** als volgt in.  

    |**Verkoopsoort**|**Verkoopscode**|**Artikelnr.**|**Vooruitbetaling %**|  
    |--------------------|--------------------|------------------|----------------------|  
    |**Klant**|**20000**|**1896-S**|**40**|
    |**Klant**|**20000**|**1900-S**|**30**|  
    
    > [!TIP]
    > Afhankelijk van uw land/regio, moet u voor artikel 1896-S ook een belastinggroepcode opgeven op het sneltabblad **Kosten en boeking**. Wanneer u het demonstratiebedrijf gebruikt, is dit veld al ingesteld.

6. Sluit alle pagina's.  

### Een vooruitbetalingsrekening verkoop opgeven in de boekingsgroepinstellingen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Boekingsgroepinstellingen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de regel waar de **Bedrijfsboekingsgroep** is ingesteld op **BINNENLAND** en de **Productboekingsgroep** op **DETAILHANDEL**.  
3. Geef in het veld **Vooruitbetalingsrekening verkoop** de relevante rekening op. Uw selectie wordt automatisch opgeslagen.  

> [!TIP]
> Als u de velden niet kunt zien op de pagina **Boekingsgroepinstellingen**, gebruikt u de horizontale schuifbalk onder aan de pagina om naar rechts te schuiven.  

## Een order maken waarvoor vooruitbetaling is vereist

 In het volgende scenario maakt Susan, de orderprocessor, een order terwijl ze met een klant praat. Voor de artikelen die de klant bestelt, is een vooruitbetaling vereist. Bovendien heeft de klant in het verleden een aantal late betalingen gedaan. Susan heeft daarom de instructie gekregen om een vast bedrag van **800** als vooruitbetaling op de order te eisen.  

De klant vraagt om 35% te betalen, waar Susan mee instemt, en dus wijzigt ze de order.  

Susan maakt de vooruitbetalingsfactuur en verzendt deze naar de klant.  

### Een verkooporder maken met een vooruitbetaling

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Kies in het veld **Klantnaam** **Trey Research**.  
4. Accepteer de waarschuwing voor openstaand saldo die verschijnt.  
5. Vul op twee verkoopregels de volgende gegevens in.  

    |**Soort**|**Nr.**|**Aantal**|  
    |--------------|-------------|------------------|  
    |**Artikel**|**1896-S**|**1**|  
    |**Artikel**|**1900-S**|**1**|

    De vooruitbetalingsvelden op de verkoopregel zijn standaard verborgen. Om de velden weer te geven moet u de pagina personaliseren. Zie voor meer informatie [Een pagina personaliseren via de banner Personaliseren](ui-personalization-user.md#start-personalizing-by-using-the-personalization-mode).

6. Controleer of het veld **Vooruitbetaling %** op de regel voor artikel **1900-S** op **30** staat. Dit is standaard overgenomen van de verkoopkop die wordt gevuld op basis van de klantkaart.  

    Het veld **Vooruitbetaling %** op de regel voor artikel **1896-S** is **40**. 40 is het percentage dat u hebt ingevoerd op de pagina **Vooruitbetalingspercentages verkoop** voor artikel **1896-S** en klant **20000**.  

    Zie voor meer informatie [Vooruitbetalingen instellen](finance-set-up-prepayments.md) voor meer informatie.  
7. Kies bij de actie **Order** de optie **Statistieken**.  
8. Op het sneltabblad **Vooruitbetaling** bevat het veld **Vooruitbetalingsbedrag excl. btw** het bedrag **458,16**. Als u nu een vooruitbetalingsfactuur voor de order maakt, is 458,16 het bedrag op de factuur.  

    In dit scenario heeft Susan instructies ontvangen om een totale vooruitbetaling van **800** voor te stellen voor de order.  

    > [!IMPORTANT]  
    >  De volgende stap kunt u in uw land\regio misschien niet uitvoeren.  
9. Wijzig het bedrag in het veld **Vooruitbetalingsbedrag excl. btw** in **800** en sluit de pagina.  
10. Controleer het veld **Vooruitbetaling %** op de verkoopregels en u ziet dat dit is herberekend als **67,02438** en **67,02282**.  

     Bij de herberekening zijn alle regels meegenomen die een vooruitbetalingspercentage hebben dat hoger is dan 0.  

     De klant vraagt nu of het vooruitbetalingspercentage op 35% kan worden gezet. De leidinggevende van Susan keurt de wijziging goed.
11. Voer op de pagina **Verkooporder** op het sneltabblad **Vooruitbetaling** in het veld **Vooruitbetaling %** de waarde **35** in.  
12. In de waarschuwing die wordt weergegeven, kiest u de knop **Ja**. Er wordt een tarief van 35% toegepast als het betalingspercentage voor de hele order.  
13. Controleer of de regels juist zijn bijgewerkt.  

## Een vooruitbetalingsfactuur maken

Nadat de juiste vooruitbetalingswaarden voor de order zijn ingevoerd, maakt Susan de vooruitbetalingsfactuur en stuurt ze deze naar de klant.  

### Een vooruitbetalingsfactuur maken

1. Kies op de pagina **Verkooporder** **Acties**, vervolgens **Boeking**, dan **Vooruitbetaling** en selecteer vervolgens **Vooruitbetalingsfactuur boeken en afdrukken**
2. Kies de knop **Ja** om de factuur te boeken.  

> [!NOTE]  
> Susan zou nu de factuur naar de klant sturen.  

## Een extra vooruitbetalingsfactuur maken

De volgende dag belt de klant op en vraagt Susan om een wijziging in de order te maken. De klant wil twee stuks van artikel 1896-S. Susan opent de order, wijzigt deze en maakt vervolgens een tweede vooruitbetalingsfactuur voor de order en stuurt deze naar de klant.  

### Een extra vooruitbetalingsfactuur maken

1. Kies op de pagina **Verkooporder** de actie **Vrijgeven** en dan **Opnieuw openen**.  
2. Typ **2** in het veld **Aantal** voor artikel **1896-S**.  

    Kies bij de actie **Order** **Statistieken**. Het veld **Vooruitbetalingsbedrag excl. btw** bevat nu **768,04** en het veld **Gefactureerd vooruitbetalingsbedrag excl. btw** bevat **417,76**. Deze waarden geven aan dat er een extra vooruitbetalingsbedrag bestaat dat nog niet is gefactureerd.  
3. Als u een factuur wilt boeken voor het extra vooruitbetalingsbedrag, kiest u **Acties**, dan **Boeking**, dan **Vooruitbetaling** en selecteert u **Vooruitbetalingsfactuur boeken en afdrukken**
4. Kies de knop **Ja** om de factuur te boeken.  

## De vooruitbetalingen vereffenen

De klant betaalt het vooruitbetalingsbedrag. Arnie, van de boekhoudafdeling, registreert de betaling en past deze toe op de vooruitbetalingsfacturen.  

### Een betaling vereffenen met vooruitbetalingsfacturen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Ontvangstendagboeken** in en kies vervolgens de gerelateerde koppeling.  
2. Vul op een dagboekregel de volgende gegevens in.  

    |Veldnaam|Voer in|  
    |----------------|-----------|  
    |**Documentsoort**|**Betaling**|  
    |**Rekeningsoort**|**Klant**|  
    |**Rekeningnr.**|**20000**|  
3. Kies de actie **Verwerken** en dan **Posten vereffenen**.  
4. Selecteer op de pagina **Klantenposten vereffenen** de eerste vooruitbetalingsfactuur en kies vervolgens de actie **Verwerken** en dan **Vereffenings-id instellen**.  
5. Herhaal de vorige stap voor de tweede vooruitbetaling.  
6. Kies de knop **Ok**.  

    In de **Bedrag**-velden is nu het totaal ingevuld van de twee vooruitbetalingsfacturen.  

7. Om het journaal te boeken kiest u de actie **Boeken/afdrukken** en selecteert u vervolgens **Boeken**.
8. Kies de knop **Ja**.

## Het resterende bedrag factureren

Arnie heeft nu doorgekregen dat de artikelen voor de order zijn verzonden en dat de order gereed is voor facturering. Arnie maakt de factuur voor de order.  

### Het resterende bedrag factureren

1. Open de verkooporder.
2. Kies de actie **Boeking** en dan **Boeken**.
3. Klik op **Verzenden en factureren** en kies vervolgens **OK**.
4. Klik op de knop **Ja** als u een voorbeeld van de factuur wilt bekijken.

    > [!NOTE]  
    > Gewoonlijk heeft de verzendafdeling de verzending al geboekt.  

    Arnie kan de geschiedenis bekijken om te controleren of de verkoopfactuur volgens plan is gemaakt.

5. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Geboekte verkoopfacturen** in en kies vervolgens de gerelateerde koppeling.  

## De status van vooruitbetaalde orders en facturen automatisch bijwerken

U kunt de verwerking van orders en facturen versnellen door taakwachtrijen in te stellen die automatisch de status van die documenten bijwerken. Wanneer een vooruitbetalingsfactuur is betaald, kunnen de items in de wachtrij automatisch de documentstatus wijzigen van **In afwachting van vooruitbetaling** in **Vrijgegeven**. Wanneer u de opdrachten in de wachtrij instelt, zijn de codeunits die u moet gebruiken: **383 Verkopen wachtend op vooruitbetaling bijwerken** en **383 Inkopen wachtend op vooruitbetaling bijwerken**. We raden u aan de items zo te plannen dat ze regelmatig worden uitgevoerd, bijvoorbeeld elke minuut. Zie voor meer informatie [Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md).

## Volgende stappen

In dit overzicht zijn de stappen behandeld om [!INCLUDE[prod_short](includes/prod_short.md)] in te stellen voor het afhandelen van vooruitbetalingen. 

- Standaardpercentages voor vooruitbetaling toewijzen aan klanten en artikelen.
- Verschillende methoden gebruiken om de vooruitbetalingen op een bestelling te berekenen.  
- Bereken het vooruitbetalingsbedrag als een percentage van het totaal op de bestelling.
- Wijs één totaal vooruitbetalingsbedrag toe aan de bestelling.  

Ook hebt u geleerd hoe u een vooruitbetalingsfactuur boekt, een tweede vooruitbetalingsfactuur maakt als de order wordt gewijzigd en de uiteindelijke factuur boekt voor het resterende bedrag.  

De vooruitbetalingsmogelijkheden maken het gemakkelijk om vooruitbetalingsregels voor klanten en artikelen in te stellen en af te dwingen. Ze laten u ook elke betaling tegen een factuur boeken.  

## Zie ook

[Vooruitbetalingen factureren](finance-invoice-prepayments.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Procedures voor bedrijfsprocessen](walkthrough-business-process-walkthroughs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
