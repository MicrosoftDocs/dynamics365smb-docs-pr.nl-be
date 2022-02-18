---
title: Artikelen met artikeltracering traceren
description: U kunt zien waar een artikel met artikeltracering is gebruikt, inclusief hoe en wanneer dit is ontvangen, geproduceerd of geretourneerd, met de functies Artikeltracering en Posten zoeken.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.forms: 6520,
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: cd9ca9b1b3aac2f1c531090342d5c43bfa64943e
ms.sourcegitcommit: 189bf08d7ddf6c8b7ef2c09058c6847aa6e590d3
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8059894"
---
# <a name="trace-item-tracked-items"></a>Artikelen met artikeltracering traceren
U kunt zien waar een artikel met artikeltracering is gebruikt, inclusief hoe en wanneer dit is ontvangen of geproduceerd, overgebracht, verkocht, verbruikt of geretourneerd. U kunt tevens alle huidige exemplaren van een bepaald serie- of lotnummer in de database vinden. Dit doet u met behulp van de functies Artikeltracering en [Posten zoeken](ui-find-entries.md).  

Deze functies zijn vooral handig tijdens het uitvoeren van kwaliteitscontroles wanneer u wilt weten welke klanten producten met een bepaald lotnummer hebben ontvangen of wanneer u wilt weten uit welk lot een defect onderdeel afkomstig is.  

 Op de pagina **Artikeltracering** kunt u voorwaarts en achterwaarts traceren in een reeks van geboekte voorraadtransacties voor het serie- of lotnummer.  

 Op de pagina **Posten zoeken** kunt u niet de reeks transacties bekijken, maar wel alle records van het serie- of lotnummer, zowel geboekte posten als open records.  

 De twee functies kunnen in combinatie worden gebruikt door een getraceerd serie- of lotnummer over te brengen naar de pagina **Posten zoeken** om een volledig traceerscenario te voltooien. <!-- For more information, see [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md).   -->

## <a name="to-trace-item-tracked-items"></a>Artikelen met artikeltracering traceren  

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikeltracering** in en kies vervolgens de gerelateerde koppeling.  
2.  In de filtervelden boven aan de pagina geeft u de specifieke artikelnummers op of een filter voor de artikelnummers die u wilt traceren.  
3.  Selecteer in het veld **Onderdelen weergeven** of u ook wilt zien waar de onderdelen voor de artikelen vandaan komen. De volgende tabel beschrijft de opties.  

    |Veld|Omschrijving|  
    |----------------------------------|---------------------------------------|  
    |**Nee**|Geen onderdelen weergeven.|  
    |**Met artikeltracering**:|Alleen onderdelen met lot- of serienummers weergeven.|  
    |**Alle**|Alle onderdelen weergeven.|  

4.  Selecteer in het veld **Traceringsmethode** de methode waarmee u het artikel wilt traceren. De volgende tabel beschrijft de opties.  

    |Veld|Omschrijving|  
    |----------------------------------|---------------------------------------|  
    |**Gebruik->Oorsprong**|Traceer voor het artikel van waar het is gebruikt tot waar het vandaan kwam. Als een geproduceerd artikel bijvoorbeeld is verkocht aan een klant, ziet u dat op de pagina **Artikeltracering**, waarbij de verkoopverzendingsregel eerst wordt weergegeven. U kunt deze regel uitbreiden om de afkomst van de productieorder te zien.|  
    |**Oorsprong->Gebruik**|Traceer voor het artikel hoe het in voorraad is gekomen tot waar het is gebruikt. Als een geproduceerd artikel bijvoorbeeld aan een klant is verkocht, ziet u dit op de pagina **Artikeltracering** waarbij de voltooide productieorder eerst wordt weergegeven. U kunt deze order uitbreiden om de verkoopverzendingsregels waarin het artikel wordt gebruikt weer te geven.|  

5.  Kies de actie **Traceren** om de tracering uit te voeren.  

> [!NOTE]  
>  Alleen vereffende transacties worden weergegeven. Als u dezelfde partij via meerdere transacties hebt ontvangen, worden op de pagina **Artikeltracering** mogelijk niet alle transacties weergegeven.   

> [!NOTE]  
>  Als al extra transactiegeschiedenis onder een artikeltraceringsregel is getraceerd door een andere bovenliggende regel, wordt het selectievakje **Al getraceerd** ingeschakeld. Voor een eenvoudiger weergave worden dergelijke onderliggende regels niet weergegeven.  
>   
>  Als u de artikeltraceringsregels wilt zoeken waarin de transactiegeschiedenis al is getraceerd, kiest u de knop **Ga naar Reeds getraceerd**. De desbetreffende artikeltraceringsregel is geselecteerd en alle onderliggende regels zijn uitgevouwen.  

## <a name="to-find-item-tracked-items-with-find-entries"></a>Artikelen met artikeltracering zoeken met Posten zoeken  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Posten zoeken** in en selecteer vervolgens de gerelateerde koppeling  
2. Kies **Acties** > **Zoeken op** > **Zoeken op artikelverwijzing**.
3. Voer in de velden **Serienr.** en **Lotnr.** de artikeltraceringsnummers in die u wilt traceren.  
4. Kies de actie **Zoeken** om alle exemplaren van het serie- of lotnummer in de database te zoeken.  

## <a name="see-also"></a>Zie ook

[Voorraad](inventory-manage-inventory.md)  
[Werken met serie-, lot- en pakketnummers](inventory-how-work-item-tracking.md)  
[Ontwerpdetails: Artikeltracering](design-details-item-tracking.md)  
[Ontwerpdetails: Artikeltracering en reserveringen](design-details-item-tracking-and-reservations.md)  
[Artikelen reserveren](inventory-how-to-reserve-items.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
<!-- [Walkthrough: Tracing Serial-Lot Numbers](walkthrough-tracing-serial-lot-numbers.md)   -->
[Posten zoeken](ui-find-entries.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]