---
title: Artikelen met artikeltracering traceren | Microsoft Docs
description: U kunt zien waar een artikel met artikeltracering is gebruikt, inclusief hoe en wanneer dit is ontvangen of geproduceerd, overgebracht, verkocht, verbruikt of geretourneerd. U kunt tevens alle huidige exemplaren van een bepaald serie- of lotnummer in de database vinden. Dit doet u met behulp van de functies Artikeltracering en Navigeren.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: cc24989d2cf770cd88bbde23d483e3859ff4a68a
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---
# <a name="trace-item-tracked-items"></a>Artikelen met artikeltracering traceren
U kunt zien waar een artikel met artikeltracering is gebruikt, inclusief hoe en wanneer dit is ontvangen of geproduceerd, overgebracht, verkocht, verbruikt of geretourneerd. U kunt tevens alle huidige exemplaren van een bepaald serie- of lotnummer in de database vinden. Dit doet u met behulp van de functies Artikeltracering en Navigeren.  

 Deze functies zijn vooral handig tijdens het uitvoeren van kwaliteitscontroles wanneer u wilt weten welke klanten producten met een bepaald lotnummer hebben ontvangen of wanneer u wilt weten uit welk lot een defect onderdeel afkomstig is.  

 In het venster **Artikeltracering** kunt u voorwaarts en achterwaarts traceren in een reeks van geboekte voorraadtransacties voor het serie- of lotnummer.  

 In het venster **Navigeren** kunt u niet de reeks transacties bekijken, maar wel alle records van het serie- of lotnummer, zowel geboekte posten als open records.  

 De twee functies kunnen in combinatie worden gebruikt door een getraceerd serie- of lotnummer over te brengen naar het venster **Navigeren** om een volledig traceerscenario te voltooien. Zie [Procedure: Serie-/lotnummers traceren](walkthrough-tracing-serial-lot-numbers.md) voor meer informatie.  

## <a name="to-trace-item-tracked-items"></a>Artikelen met artikeltracering traceren  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Artikeltracering** in en klik vervolgens op de gerelateerde koppeling.  
2.  In de filtervelden boven aan het venster geeft u de specifieke artikelnummers op of een filter voor de artikelnummers die u wilt traceren.  
3.  Selecteer in het veld **Onderdelen weergeven** of u ook wilt zien waar de onderdelen voor de artikelen vandaan komen. U beschikt over de volgende opties in dit veld.  

    |Veld|Description|  
    |----------------------------------|---------------------------------------|  
    |**Nee**|Selecteer deze optie als u geen onderdelen wilt weergeven.|  
    |**Met artikeltracering**:|Selecteer deze optie als u alleen onderdelen met lot- of serienummers wilt weergeven.|  
    |**Alle**|Selecteer deze optie als u alle onderdelen wilt weergeven.|  

4.  Selecteer in het veld **Traceringsmethode** de methode waarmee u het artikel wilt traceren. De volgende opties zijn beschikbaar  

    |Veld|Description|  
    |----------------------------------|---------------------------------------|  
    |**Gebruik->Oorsprong**|Met deze methode wordt het artikel getraceerd vanaf waar het is gebruikt tot waar het vandaan kwam. Als een geproduceerd artikel bijvoorbeeld is verkocht aan een klant, ziet u dat in het venster **Artikeltracering**, waarbij de verkoopverzendingsregel eerst wordt weergegeven. U kunt deze regel uitbreiden om de afkomst van de productieorder te zien.|  
    |**Oorsprong->Gebruik**|Met deze methode wordt het item getraceerd vanaf waar het in de voorraad is opgenomen tot waar het is gebruikt. Als een geproduceerd artikel bijvoorbeeld aan een klant is verkocht, ziet u dit in het venster **Artikeltracering** waarbij de voltooide productieorder eerst wordt weergegeven. U kunt deze order uitbreiden om de verkoopverzendingsregels waarin het artikel wordt gebruikt weer te geven.|  

5.  Kies de actie **Traceren** om de tracering uit te voeren.  

> [!NOTE]  
>  Als u dezelfde partij via meer transacties hebt ontvangen, worden in het venster **Artikeltracering** mogelijk niet alle transacties weergegeven. Alleen vereffende transacties worden weergegeven.  

> [!NOTE]  
>  Als al extra transactiegeschiedenis onder een artikeltraceringsregel is getraceerd door een andere bovenliggende regel, wordt het selectievakje **Al getraceerd** ingeschakeld. Voor een eenvoudiger weergave worden dergelijke onderliggende regels niet weergegeven.  
>   
>  Als u de artikeltraceringsregels wilt zoeken waarin de transactiegeschiedenis al is getraceerd, kiest u de knop **Ga naar Reeds getraceerd**. De desbetreffende artikeltraceringsregel is geselecteerd en alle onderliggende regels zijn uitgevouwen.  

## <a name="to-find-item-tracked-items-with-navigate"></a>Artikelen met artikeltracering zoeken met Navigeren  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Navigeren** in en klik vervolgens op de gerelateerde koppeling.  
2.  Voer op het sneltabblad **Artikeltracering** in de velden **Serienr.** en **Lotnr.** de artikeltraceringsnummers in die u wilt traceren.  
3.  Kies de actie **Zoeken** om alle exemplaren van het serie- of lotnummer in de database te zoeken.  

## <a name="see-also"></a>Zie ook  
[Voorraad](inventory-manage-inventory.md)  
[Ontwerpdetails: Artikeltracering](design-details-item-tracking.md)
[Ontwerpdetails: Artikeltracering en reserveringen](design-details-item-tracking-and-reservations.md)  
[Artikelen reserveren](inventory-how-to-reserve-items.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
[Procedure: Serie-/lotnummers traceren](walkthrough-tracing-serial-lot-numbers.md)

