---
title: Artikelen reserveren
description: U kunt artikelen reserveren voor verkooporders, inkooporders en productieorders. U kunt artikelen in voorraad reserveren of inkomend op openstaande documentregels.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.forms: 498, 497
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 385003db0d0fe8b121e6512257f0ed448596225e
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8519712"
---
# <a name="reserve-items"></a>Artikelen reserveren
U kunt artikelen reserveren voor verkooporders, inkooporders, serviceorders, assemblageorders en productieorders. U kunt artikelen in voorraad reserveren of inkomend op openstaande document- of dagboekregels. U voert de handelingen hiervoor uit op de pagina **Reservering**.

Elke regel op de pagina **Reservering**, die u opent om artikelen te reserveren, geeft informatie over één soort regel (verkoop, inkoop, dagboek) of voorraadpost. Op de regels wordt beschreven hoeveel artikelen van elk soort regel of post beschikbaar zijn voor reservering.

## <a name="to-reserve-items-for-sales"></a>Artikelen reserveren voor verkopen
Hieronder wordt beschreven hoe u artikelen reserveert vanuit een verkooporder. De stappen voor inkoop-, service- en assemblageorders komen hiermee overeen.  
1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies in een verkooporder op het sneltabblad **Regels** de actie **Reserveren**. De pagina **Reservering** verschijnt.  
3. Klik op de regel waarvan u de artikelen wilt reserveren.  
4. Kies een van de volgende acties.  

    |**Functie**|**Beschrijving**|
    |------------------|---------------------|  
    |**Autom. reservering**|Hiermee reserveert u automatisch de artikelen op de pagina **Reservering**.|  
    |**Huidige regel reserveren**|Artikelen uit het document op de geselecteerde regel worden gereserveerd.|  
    |**Huidige regel annuleren**|De reservering van artikelen uit het document op de geselecteerde regel wordt geannuleerd.|

> [!NOTE]  
>  Als u artikeltracering hebt ingesteld voor de verkooporder, moet u een speciale reserveringsprocedure uitvoeren: Zie voor meer informatie [Reserveren van een bepaald serie- of lotnummer](inventory-how-to-reserve-items.md#to-reserve-a-specific-serial-or-lot-number).  

## <a name="to-reserve-an-item-for-a-production-order-line"></a>Een artikel voor een productieorderregel reserveren  
U kunt artikelen voor productieorders reserveren. U moet hierbij onderscheid maken tussen productieorderregels (het bovenliggende artikel) en productieordermaterialen.

In de volgende procedure wordt een vast geplande productieorder gebruikt.   
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Vast geplande productieorder** in en kies vervolgens de gerelateerde koppeling.  
2. Open de vast geplande productieorder waarvoor u bovenliggende artikelen wilt reserveren.  
3. Selecteer de relevante productieorderregel.  
4. Kies op het sneltabblad **Regels** de actie **Reserveren**.
5. Selecteer op de pagina **Reservering** de regel **Verkoopregel, Order** en kies vervolgens de actie **Vanuit huidige regel** reserveren.  

Het aantal dat u hebt ingevoerd op de vast geplande productieorderregel is nu gereserveerd.

## <a name="to-reserve-items-for-production-order-components"></a>Artikelen reserveren voor productieordermaterialen  
U kunt artikelen voor productieorders reserveren. U moet hierbij onderscheid maken tussen productieorderregels (het bovenliggende artikel) en productieordermaterialen.

In de volgende procedure wordt een vast geplande productieorder gebruikt.    
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vast geplande productieorder** in en kies vervolgens de gerelateerde koppeling.  
2. Open de vast geplande productieorder waarvoor u artikelonderdelen wilt reserveren.  
3. Selecteer de relevante productieorderregel.  
4. Klik op het sneltabblad **Regels** op **Regel** en vervolgens op **Materialen**.  
5. Selecteer de betreffende materiaalregel.  
6. Kies op het sneltabblad **Regels** de actie **Reserveren**.  
7. Selecteer op de pagina **Reservering** een regel en kies vervolgens de actie **Vanuit huidige regel reserveren**.  

Het aantal dat u hebt ingevoerd op de materiaalregel van de vast geplande productieorder is nu gereserveerd.

## <a name="to-change-a-reservation"></a>Een reservering wijzigen  
Soms wilt u een artikelreservering wijzigen.   
1. Kies vanuit de gereserveerde documentregel op het sneltabblad **Regels** de actie **Reserveren**.  
2. Kies op de pagina **Reservering** de actie **Reserveringsposten**.
3. Werk op de pagina **Reserveringsposten** het veld **Aantal** bij op de regel op die u wilt wijzigen.
4. Bevestig het volgende bericht met de knop **OK**.

## <a name="to-cancel-a-reservation"></a>Een reservering annuleren  
Soms wilt u een artikelreservering annuleren.   
1. Kies vanuit de documentregel waarvoor u een reservering wilt annuleren op het sneltabblad **Regels** de actie **Reserveren**.  
2. Kies op de pagina **Reservering** de actie **Reserveringsposten**.  
3.  Kies op de pagina **Reservering** de actie **Reservering annuleren**.  
4.  Bevestig het volgende bericht met de knop **OK**.  

## <a name="to-reserve-a-specific-serial-or-lot-number"></a>Reserveren van een bepaald serie- of lotnummer  
Van uitgaande documenten voor getraceerde artikelen, zoals verkooporders of productiecomponentlijsten, kunt u specifieke serie- of lotnummers reserveren. Dit kan nuttig zijn als u bijvoorbeeld productiecomponenten van een specifieke partij nodig hebt om consistentie met eerdere productiepartijen te waarborgen of omdat een klant een specifiek serienummer heeft aangevraagd. Zie voor meer informatie [Werken met serie- en lotnummers](inventory-how-work-item-tracking.md).

Dit heet een specifieke reservering, omdat u reserveert van het aantal van Artikel X dat hoort bij Partij X. Als u gewoon uit aantallen van artikel X reserveert, is het een normale, niet-specifieke, reservering. Zie voor meer informatie [Ontwerpdetails: Artikeltracering en reservering](design-details-item-tracking-and-reservations.md).

De volgende procedure is gebaseerd op een verkooporder.    
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en selecteer vervolgens de gerelateerde koppeling.  
2. Maak een verkooporderregel voor een artikel met artikeltracering.  
3. Wijs serie- en lotnummers toe aan de verkooporderregel. Zie voor meer informatie [Werken met serie- en lotnummers](inventory-how-work-item-tracking.md).
4. Kies op de verkooporderregel de actie **Reserveren**.  
5. Klik op de knop **Ja** om specifieke serie- of lotnummers te reserveren.  
6. Selecteer op de pagina **Artikeltraceringsoverzicht** de combinatie van serie- en lotnummer die u zojuist hebt toegekend.  
7. Kies de knop **OK** om de pagina **Reservering** te openen met alleen aanvoer met het opgegeven artikeltraceringsnummer. Als er niet-specifieke reserveringen zijn voor de artikeltraceringsnummers die u hebt opgegeven voor deze regel, ontvangt u een bericht over het reeds gereserveerde aantal.  
8. Kies de actie **Autom. reservering** of **Vanuit huidige regel reserveren** om de reservering voor de specifieke artikeltraceringsnummers te maken.

## <a name="see-also"></a>Zie ook
[Voorraad](inventory-manage-inventory.md)  
[Ontwerpdetails: Reservering, ordertracering en planningsboodschappen](design-details-reservation-order-tracking-and-action-messaging.md)  
[Ontwerpdetails: Artikeltracering en reserveringen](design-details-item-tracking-and-reservations.md)  
[Werken met serie- en lotnummers](inventory-how-work-item-tracking.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]