---
title: Artikelen reserveren | Microsoft Docs
description: U kunt artikelen reserveren voor verkooporders, inkooporders en productieorders. U kunt artikelen in voorraad reserveren of inkomend op openstaande documentregels.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: b03209b5681c264f7d788d3d731d32b60f1709b6
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-reserve-items"></a>Procedure: Artikelen reserveren
U kunt artikelen reserveren voor verkooporders, inkooporders, serviceorders, assemblageorders en productieorders. U kunt artikelen in voorraad reserveren of inkomend op openstaande document- of dagboekregels. U voert de handelingen hiervoor uit in het venster **Reservering**.

Elke regel in het venster **Reservering**, dat u opent om artikelen te reserveren, geeft informatie over één soort regel (verkoop, inkoop, dagboek) of voorraadpost. Op de regels wordt beschreven hoeveel artikelen van elk soort regel of post beschikbaar zijn voor reservering.

## <a name="to-reserve-items-for-sales"></a>Artikelen reserveren voor verkopen
Hieronder wordt beschreven hoe u artikelen reserveert vanuit een verkooporder. De stappen voor inkoop-, service- en assemblageorders komen hiermee overeen.  
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verkooporders** in en klik vervolgens op de gerelateerde koppeling.  
2.  Kies in een verkooporder op het sneltabblad **Regels** de actie **Reserveren**. Het venster **Reservering** verschijnt.  
3. Klik op de regel waarvan u de artikelen wilt reserveren.  
4. Kies een van de volgende acties.  

    |**Functie**|**Beschrijving**|
    |------------------|---------------------|  
    |**Autom. reservering**|Automatisch artikelen reserveren in het venster **Reservering**.|  
    |**Huidige regel reserveren**|Artikelen uit het document op de geselecteerde regel worden gereserveerd.|  
    |**Huidige regel annuleren**|De reservering van artikelen uit het document op de geselecteerde regel wordt geannuleerd.|

> [!NOTE]  
>  Als u artikeltracering hebt ingesteld voor de verkooporder, moet u een speciale reserveringsprocedure uitvoeren: Zie voor meer informatie het gedeelte "Reserveren van een bepaald serie- of lotnummer".  

## <a name="to-reserve-an-item-for-a-production-order-line"></a>Een artikel voor een productieorderregel reserveren  
U kunt artikelen voor productieorders reserveren. U moet hierbij onderscheid maken tussen productieorderregels (het bovenliggende artikel) en productieordermaterialen.

In de volgende procedure wordt een vast geplande productieorder gebruikt.   
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Vast geplande productieorder** in en klik op de gerelateerde koppeling.  
2. Open de vast geplande productieorder waarvoor u bovenliggende artikelen wilt reserveren.  
3. Selecteer de relevante productieorderregel.  
4. Kies op het sneltabblad **Regels** de actie **Reserveren**.
5. Selecteer in het venster **Reservering** de regel **Verkoopregel, Order** en kies vervolgens de actie **Vanuit huidige regel** reserveren.  

Het aantal dat u hebt ingevoerd op de vast geplande productieorderregel is nu gereserveerd.

## <a name="to-reserve-items-for-production-order-components"></a>Artikelen reserveren voor productieordermaterialen  
U kunt artikelen voor productieorders reserveren. U moet hierbij onderscheid maken tussen productieorderregels (het bovenliggende artikel) en productieordermaterialen.

In de volgende procedure wordt een vast geplande productieorder gebruikt.    
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Vast geplande productieorder** in en klik op de gerelateerde koppeling.  
2. Open de vast geplande productieorder waarvoor u artikelonderdelen wilt reserveren.  
3. Selecteer de relevante productieorderregel.  
4. Klik op het sneltabblad **Regels** op **Regel** en vervolgens op **Materialen**.  
5. Selecteer de betreffende materiaalregel.  
6. Kies op het sneltabblad **Regels** de actie **Reserveren**.  
7. Selecteer in het venster **Reservering** een regel en kies vervolgens de actie **Vanuit huidige regel reserveren**.  

Het aantal dat u hebt ingevoerd op de materiaalregel van de vast geplande productieorder is nu gereserveerd.

## <a name="to-change-a-reservation"></a>Een reservering wijzigen  
Soms wilt u een artikelreservering wijzigen.   
1. Kies vanuit de gereserveerde documentregel op het sneltabblad **Regels** de actie **Reserveren**.  
2. Kies in het venster **Reservering** de actie **Reserveringsposten**.
3. Werk in het venster **Reserveringsposten** het veld **Aantal** bij op de regel op die u wilt wijzigen.
4. Bevestig het volgende bericht met de knop **OK**.

## <a name="to-cancel-a-reservation"></a>Een reservering annuleren  
Soms wilt u een artikelreservering annuleren.   
1. Kies vanuit de documentregel waarvoor u een reservering wilt annuleren op het sneltabblad **Regels** de actie **Reserveren**.  
2. Kies in het venster **Reservering** de actie **Reserveringsposten**.  
3.  Kies in het venster **Reserveringsposten** de actie **Reservering annuleren**.  
4.  Bevestig het volgende bericht met de knop **OK**.  

## <a name="to-reserve-a-specific-serial-or-lot-number"></a>Reserveren van een bepaald serie- of lotnummer  
Van uitgaande documenten voor getraceerde artikelen, zoals verkooporders of productiecomponentlijsten, kunt u specifieke serie- of lotnummers reserveren. Dit kan nuttig zijn als u bijvoorbeeld productiecomponenten van een specifieke partij nodig hebt om consistentie met eerdere productiepartijen te waarborgen of omdat een klant een specifiek serienummer heeft aangevraagd. Meer informatie over het dit onderwerp vindt u in [Procedure: Werken met serie- en lotnummers](inventory-how-work-item-tracking.md)..

Dit heet een specifieke reservering, omdat u reserveert van het aantal van Artikel X dat hoort bij Partij X. Als u gewoon uit aantallen van artikel X reserveert, is het een normale, niet-specifieke, reservering. Zie voor meer informatie [Ontwerpdetails: Artikeltracering en reservering](design-details-item-tracking-and-reservations.md).

De volgende procedure is gebaseerd op een verkooporder.    
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verkooporders** in en klik vervolgens op de gerelateerde koppeling.  
2. Maak een verkooporderregel voor een artikel met artikeltracering.  
3. Wijs serie- en lotnummers toe aan de verkooporderregel. Meer informatie over het dit onderwerp vindt u in [Procedure: Werken met serie- en lotnummers](inventory-how-work-item-tracking.md)..
4. Kies op de verkooporderregel de actie **Reserveren**.  
5. Klik op de knop **Ja** om specifieke serie- of lotnummers te reserveren.  
6. Selecteer in het venster **Artikeltraceringsoverzicht** de combinatie van serie- en lotnummer die u zojuist hebt toegekend.  
7. Klik op de knop **OK** om het venster **Reservering** te openen met alleen aanvoer met het opgegeven artikeltraceringsnummer. Als er niet-specifieke reserveringen zijn voor de artikeltraceringsnummers die u hebt opgegeven voor deze regel, ontvangt u een bericht over het reeds gereserveerde aantal.  
8. Kies de actie **Autom. reservering** of **Vanuit huidige regel reserveren** om de reservering voor de specifieke artikeltraceringsnummers te maken.

## <a name="see-also"></a>Zie ook
[Voorraad](inventory-manage-inventory.md)  
[Ontwerpdetails: Reservering, ordertracering en planningsboodschappen](design-details-reservation-order-tracking-and-action-messaging.md)  
[Ontwerpdetails: Artikeltracering en reserveringen](design-details-item-tracking-and-reservations.md)  
[Procedure: Werken met serie- en lotnummers](inventory-how-work-item-tracking.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

