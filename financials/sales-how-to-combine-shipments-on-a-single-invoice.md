---
title: "Procedure: Verzendingen combineren op één factuur | Microsoft Docs"
description: Als u meerdere verzendingen tegelijkertijd wilt factureren, kunt u de functie Verzamelfacturering gebruiken.
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
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: c9f2464014f2078f2a86f2e7d8a72873fa4015a8
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="combine-shipments-on-a-single-invoice"></a>Verzendingen combineren op één factuur
Als u meerdere verzendingen tegelijkertijd wilt factureren, kunt u de functie Verzamelfacturering gebruiken.  

 Voordat u een verzamelfactuur kunt maken, moet u meerdere verkoopverzendingen voor dezelfde klant in dezelfde valuta boeken. U moet dus twee of meer verkooporders invullen en deze als verzonden maar niet als gefactureerd boeken. Om verzendingen te combineren moet het selectievakje **Verzendingen combineren** zijn ingeschakeld op het sneltabblad **Verzending** van de **klantenkaart**.  

## <a name="to-manually-combine-shipments-on-a-single-invoice"></a>Verzendingen handmatig op één factuur combineren  
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verkoopfacturen** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies de actie **Nieuw**. Zie [Verkopen factureren](sales-how-invoice-sales.md) voor meer informatie.
3. Voer in het veld **Orderklantnr.** de klant in die de factuur voor de verzonden artikelen zal ontvangen.  
4. Selecteer op het sneltabblad **Regels** de actie **Verzendregels ophalen**.  
5. Selecteer de verzendregels die u wilt opnemen in de factuur:  

    - Als u alle regels wilt invoegen, selecteert u alle regels en klikt u op **OK**.  
    - Als u specifieke regels wilt invoegen, selecteert u deze regels en klikt u op **OK**. Gebruik de Ctrl-toets om meerdere niet-aaneengesloten regels te selecteren.  

    Als u de verkeerde verzendregel hebt geselecteerd of als u opnieuw wilt beginnen, kunt u de regels op de factuur verwijderen en de functie **Verzendregels ophalen** opnieuw uitvoeren.  
7. Kies de actie **Boeken** om de factuur te boeken.  

## <a name="to-automatically-combine-shipments-on-a-single-invoice"></a>Verzendingen automatisch op één factuur combineren  
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verzamelfacturering** in en klik vervolgens o de gerelateerde koppeling. Het opvraagvenster voor de batchverwerking wordt geopend.  
2. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Schakel het selectievakje **Facturen boeken** in.  
4.  Kies de knop **OK**.  

> [!NOTE]  
>  U moet de facturen handmatig boeken als het selectievakje **Facturen boeken** niet was ingeschakeld bij de batchverwerking.  

## <a name="to-remove-open-sales-orders-after-combined-shipment-posting"></a>Openstaande verkooporders verwijderen na boeking van een verzamelfactuur 
Als verzendingen worden gecombineerd op een factuur en worden geboekt, wordt er een geboekte verkoopfactuur gemaakt voor de gefactureerde regel. Het veld **Verzonden aantal** op het oorspronkelijke verkoopraamcontract of de oorspronkelijke verkooporder wordt bijgewerkt op basis van het gefactureerde aantal.  

Als u op deze manier verzendingen factureert, blijven de orders van waaruit de verzending zijn geboekt bestaan, ook als ze volledig zijn verzonden en gefactureerd.   

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Gefact. verk.-orders verwijderen** in en klik vervolgens op de gerelateerde koppeling.  
2. Geef in het filterveld **Nr.** op welke verkooporders moeten worden verwijderd.  
3. Kies de knop **Ok**.  

U kunt afzonderlijke verkooporders ook handmatig verwijderen.  

Herhaal stap 1 t/m 3 voor alle andere betrokken documenten, zoals verkoopraamcontracten.

## <a name="see-also"></a>Zie ook  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

