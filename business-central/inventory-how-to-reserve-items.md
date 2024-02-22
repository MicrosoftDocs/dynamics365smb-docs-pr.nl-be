---
title: Artikelen reserveren
description: 'Meer informatie over het reserveren van artikelen voor verkooporders, inkooporders en productieorders.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.keywords: null
ms.search.forms: '498, 497'
ms.date: 09/19/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Artikelen reserveren

U kunt artikelen reserveren voor verkooporders, inkooporders, serviceorders, assemblageorders, transferorders en productieorders. U kunt artikelen ook in voorraad reserveren of inkomend op openstaande document- of dagboekregels. Dit doet u op de pagina **Reservering**.

Elke regel die u opent om artikelen te reserveren op de pagina **Reservering**, geeft informatie over één soort regel (verkoop, inkoop of dagboek) of voorraadpost. Op de regels wordt beschreven hoeveel artikelen van elk soort regel of post beschikbaar zijn voor reservering.

> [!TIP]
> Op basis van de hoeveelheden die u in voorraad heeft gereserveerd, geeft [!INCLUDE [prod_short](includes/prod_short.md)] een status weer bij de documenten, zodat u snel op de hoogte bent van de volgende stap. Om bijvoorbeeld aan te geven dat u een verkooporder kunt verzenden of aan de slag kunt gaan met een project-, assemblage- of productieorder. De status helpt ook het risico te verminderen van onbedoelde deelzendingen of vertragingen als gevolg van ontbrekende voorraad voor productie- en assemblageorders.
>
> Het veld **Gereserveerd uit voorraad** geeft u inzicht of u voor een specifieke order of orderregel kunt verzenden of picken. Voor regels is het veld Gereserveerd uit voorraad beschikbaar in feitenblokken. Om toegang te krijgen tot de informatie voor de hele bestelling bevindt het veld zich op de pagina **Statistieken**.

## Artikelen reserveren voor verkopen

In de volgende procedure wordt beschreven hoe u artikelen reserveert vanuit een verkooporder. De stappen voor inkoop-, service-, transfer- en assemblageorders komen hiermee overeen.
  
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de verkooporder.
3. Kies op het sneltabblad **Regels** de actie **Reserveren**. De pagina **Reservering** verschijnt.  
4. Selecteer de regel waarvan u de artikelen wilt reserveren.  
5. Kies een van de volgende acties.  

    |**Functie**|**Beschrijving**|
    |------------------|---------------------|  
    |**Autom. reservering**|Hiermee reserveert u automatisch de artikelen op de pagina **Reservering**.|  
    |**Huidige regel reserveren**|Artikelen uit het document op de geselecteerde regel worden gereserveerd.|  
    |**Huidige regel annuleren**|De reservering van artikelen in het document op de regel die u hebt geselecteerd, annuleren.|

> [!NOTE]  
> Als u artikeltracering hebt ingesteld voor de verkooporder, moet u een speciale reserveringsprocedure uitvoeren: Zie voor meer informatie de sectie [Reserveren van een bepaald serie- of lotnummer](inventory-how-to-reserve-items.md#reserve-a-specific-serial-or-lot-number).  

## Een artikel voor een productieorderregel reserveren

U kunt artikelen voor productieorders reserveren. U moet hierbij onderscheid maken tussen productieorderregels (het bovenliggende artikel) en productieordermaterialen.

In de volgende procedure wordt een vast geplande productieorder gebruikt.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vast geplande productieorder** in en kies vervolgens de gerelateerde koppeling.  
2. Open de vast geplande productieorder waarvoor u bovenliggende artikelen wilt reserveren.  
3. Selecteer de relevante productieorderregel.  
4. Kies op het sneltabblad **Regels** de actie **Reserveren**.
5. Selecteer op de pagina **Reservering** de regel **Verkoopregel, Order** en kies vervolgens de actie **Huidige regel reserveren**.  

Het aantal dat u hebt ingevoerd op de vast geplande productieorderregel is nu gereserveerd.

## Artikelen reserveren voor productieordermaterialen

U kunt artikelen voor productieorders reserveren. U moet hierbij onderscheid maken tussen productieorderregels (het bovenliggende artikel) en productieordermaterialen.

In de volgende procedure wordt een vast geplande productieorder gebruikt.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vast geplande productieorder** in en kies vervolgens de gerelateerde koppeling.  
2. Open de vast geplande productieorder waarvoor u artikelonderdelen wilt reserveren.  
3. Selecteer de relevante productieorderregel.  
4. Klik op het sneltabblad **Regels** op **Regel** en vervolgens op **Materialen**.  
5. Selecteer de betreffende materiaalregel.  
6. Kies op het sneltabblad **Regels** de actie **Reserveren**.  
7. Selecteer op de pagina **Reservering** een regel en kies vervolgens de actie **Huidige regel reserveren**.  

Het aantal dat u hebt ingevoerd op de materiaalregel van de vast geplande productieorder is nu gereserveerd.

## Artikelen in bulk reserveren

Gebruik de pagina **Reserveringswerkblad** om binnenkomende goederen in bulk te reserveren en toe te wijzen. Bulkreserveringen kunnen er bijvoorbeeld voor zorgen dat er hoeveelheden beschikbaar zijn voor uw verkoop- en productieorders. U kunt meerdere batches hebben voor verschillende doeleinden. U kunt bijvoorbeeld productieorders wekelijks toewijzen, maar dagelijks reserveren voor verkoop.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Reserveringswerkblad** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Vraag ophalen** en geef vervolgens het soort vraag op dat u wilt reserveren uit de beschikbare voorraad.
3. Vul de vereiste filters in. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
4. Optioneel: als u de artikelen meteen wilt toewijzen, kiest u de actie **Toewijzen**.
5. Kies op de pagina **Toewijzingsbeleid** een beleid voor elke stap

   |Toewijzingsbeleid  |Omschrijving  |
   |---------|---------|
   |Basis     | Wijst voorraad toe aan een vraag als er geen conflicten zijn en de vraag volledig kan worden gedekt. U hebt bijvoorbeeld verkooporder A met een hoeveelheid van 10 en een project met een hoeveelheid van 7. Als u er 20 op voorraad heeft, ontvangen beide aanvragen de volledige hoeveelheid. Als uw voorraad 12 is, wordt er geen voorraad toegewezen. U moet de hoeveelheid handmatig toewijzen.        |
   |Evenredig    | Verdeelt de beschikbare voorraad gelijkmatig over de vraag. U hebt bijvoorbeeld een verkooporder A met een hoeveelheid van 10 en een project met een hoeveelheid van 7. Als uw voorraadniveau 20 is, ontvangen beide vragen de volledige hoeveelheid. Als uw voorraad 12 is, krijgen beide vragen er 6.        |
   |Op klantprioriteit|Verdeling op basis van het veld Prioriteit in de klantenkaart. In geval van onvoldoende hoeveelheden geeft het systeem prioriteit aan het leveren van klanten met de hoogste prioriteit.|

6. Als u alle regels wilt reserveren waarvoor **Accepteren** is ingeschakeld, kiest u de actie **Reservering maken** .
    
## Een reservering wijzigen

U kunt een artikelreservering wijzigen.

1. Kies vanuit de documentregel vanwaar u de reservering hebt gemaakt, op het sneltabblad **Regels** de actie **Reserveren**.  
2. Kies op de pagina **Reservering** de actie **Reserveringsposten**.
3. Werk op de pagina **Reserveringsposten** het veld **Aantal** bij op de regel op die u wilt wijzigen.
4. Bevestig het volgende bericht door de knop **OK** te kiezen.

## Een reservering annuleren

U kunt een artikelreservering annuleren.

1. Kies vanuit de documentregel vanwaar u een reservering wilt annuleren, op het sneltabblad **Regels** de actie **Reserveren**.  
2. Kies op de pagina **Reservering** de actie **Reserveringsposten**.  
3. Kies op de pagina **Reservering** de actie **Reservering annuleren**.  
4. Bevestig het volgende bericht door de knop **OK** te kiezen.  

## Reserveren van een bepaald serie- of lotnummer

Van uitgaande documenten voor getraceerde artikelen, zoals verkooporders of productiecomponentlijsten, kunt u specifieke serie- of lotnummers reserveren. Het reserveren van specifieke serie- of lotnummers kan bijvoorbeeld handig zijn in de volgende situaties:

* Als u productiecomponenten uit een specifieke partij nodig heeft om consistentie met eerdere productiebatches te garanderen.
* Omdat een klant om een specifiek serienummer heeft gevraagd. 

Zie voor meer informatie [Werken met serie- en lotnummers](inventory-how-work-item-tracking.md).

Dit heet een specifieke reservering, omdat u reserveert vanuit het aantal van artikel X dat hoort bij partij X. Als u daarentegen alleen uit aantallen van artikel X reserveert, is het een normale, niet-specifieke, reservering. Zie voor meer informatie [Ontwerpdetails: Artikeltracering en reservering](design-details-item-tracking-and-reservations.md).

De volgende procedure is gebaseerd op een verkooporder.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en selecteer vervolgens de gerelateerde koppeling.  
2. Maak een verkooporderregel voor een artikel met artikeltracering.  
3. Wijs serie- en lotnummers toe aan de verkooporderregel. Zie voor meer informatie [Werken met serie- en lotnummers](inventory-how-work-item-tracking.md).
4. Kies op de verkooporderregel de actie **Reserveren**.  
5. Klik op de knop **Ja** om specifieke serie- of lotnummers te reserveren.  
6. Selecteer op de pagina **Artikeltraceringsoverzicht** de combinatie van serie- en lotnummer die u zojuist hebt toegekend.  
7. Kies de knop **OK** om de pagina **Reservering** te openen met alleen aanvoer met het opgegeven artikeltraceringsnummer. Als er niet-specifieke reserveringen zijn voor de artikeltraceringsnummers die u hebt opgegeven voor deze regel, ontvangt u een bericht over het reeds gereserveerde aantal.  
8. Kies de actie **Autom. reservering** of **Huidige regel reserveren** om de reservering van de specifieke artikeltraceringsnummers te maken.

## Zie ook

[Voorraad](inventory-manage-inventory.md)  
[Ontwerpdetails: Reservering, ordertracering en planningsboodschappen](design-details-reservation-order-tracking-and-action-messaging.md)  
[Ontwerpdetails: Artikeltracering en reserveringen](design-details-item-tracking-and-reservations.md)  
[Werken met serie- en lotnummers](inventory-how-work-item-tracking.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
