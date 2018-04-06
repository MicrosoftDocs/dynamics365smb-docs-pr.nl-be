---
title: Serviceartikelen maken | Microsoft Docs
description: Wanneer u een niet-geregistreerd artikel voor service ontvangt, kunt u dit artikel registreren als serviceartikel.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2c9c7796b80d77d3a879ecf9ce2a8af26a0ca5aa
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="create-service-items"></a>Serviceartikelen maken
In [!INCLUDE[d365fin](includes/d365fin_md.md)] verwijst de term serviceartikel naar de apparatuur of artikelen die service vereisen. Wanneer u een serviceorder maakt, geeft u de artikelen op die service nodig hebben. In de order kunt u een serviceartikel aan een artikel in de voorraad of aan een serviceartikelgroep koppelen.    

Wanneer u een artikel ontvangt dat service vereist, kunt u dit artikel registreren als serviceartikel. Dit kunt u op verschillende manieren doen. U kunt bijvoorbeeld via de pagina **Serviceartikelen** een serviceartikel maken of als onderdeel van een ander proces, bijvoorbeeld wanneer u met een serviceorder werkt.   

## <a name="to-create-a-service-item"></a>Een serviceartikel maken  
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Serviceartikelen** in en klik vervolgens op de gerelateerde koppeling.
2. Vul de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-service-items-within-a-service-order"></a>Serviceartikelen maken in serviceorders  
Wanneer u artikelen voor service ontvangt die u wilt registreren als serviceartikelen, kunt u deze instellen als serviceartikelen in het venster **Serviceorder** of **Serviceofferte**.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Serviceorders** in en klik op de gerelateerde koppeling.  
2. Vul de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Kies de actie **Serviceartikel maken**.  

    Er wordt een nummer aan het serviceartikel toegewezen en een kaart voor het serviceartikel gemaakt. Het nummer van het nieuwe serviceartikel wordt ingevuld in het veld **Serviceartikelnr.**

## <a name="to-create-a-service-item-when-shipping-items"></a>Serviceartikelen maken tijdens het verzenden van artikelen  
Als u artikelen verzendt door serviceorders of servicefacturen te boeken, worden de verzonden artikelen automatisch als serviceartikelen geregistreerd als aan de volgende voorwaarde wordt voldaan. De artikelen moeten behoren tot een serviceartikelgroep waarvoor het selectievakje **Serviceartikel maken** is ingeschakeld. Als voor de artikelen serienummers zijn geregistreerd in het venster Artikeltraceringsregels, worden deze gegevens tijdens het maken van serviceartikelen automatisch gekopieerd naar het veld **Serienummer** op de serviceartikelkaart.  

Hieronder wordt aangegeven hoe u serviceartikelen kunt maken tijdens het verzenden van artikelen in serviceorders.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Serviceorders** in en klik op de gerelateerde koppeling.  
2. Open de betreffende serviceorder.  
3. Kies de actie **Boeken** of **Boeken en afdrukken**.  
4. Kies de actie **Verzenden** of **Verzenden en factureren**.  
5. Er worden automatisch serviceartikelen gemaakt voor de artikelen op de order, wanneer deze behoren tot een serviceartikelgroep die u hebt ingesteld om serviceartikelen te maken. Als u bepaalde serienummers in het venster **Artikeltraceringsregels** hebt geregistreerd, worden deze aan deze serviceartikelen toegewezen.  

> [!NOTE]  
>  Als een artikel is ingesteld als stuklijst en u de stuklijst hebt getoond, worden de getoonde stuklijstartikelen verwerkt als gewone artikelen. Serviceartikelen worden gemaakt op basis van de voorwaarde serviceartikelgroep en optioneel op de voorwaarde serienummers. Als een serviceartikel wordt gemaakt voor een getoond stuklijstartikel waarin andere stuklijstonderdelen zijn opgenomen, worden deze artikelen gemaakt als serviceartikelonderdelen voor het getoonde stuklijstserviceartikel.  
>   
>  Is een artikel ingesteld als stuklijst en hebt u de stuklijst niet getoond, dan wordt hiervoor een serviceartikel gemaakt op basis van de voorwaarde serviceartikelgroep en optioneel de voorwaarde serienummers.  

## <a name="to-insert-a-starting-fee-for-a-service-item"></a>Starttarieven invoegen voor serviceartikelen
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Servicetaken** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Artikelwerkbon**.
3. Kies de serviceregel en kies vervolgens **Acties**, **Functies** en de actie **Starttarief invoegen**.  

    Er wordt een serviceregel van het type **Kosten** ingevoegd met het starttarief. Het starttarief is van toepassing op het geselecteerde serviceartikel.

## <a name="see-also"></a>Zie ook  
[Serviceartikelen en serviceartikelonderdelen instellen](service-how-setup-service-items.md)  
[CRM - Service instellen](service-setup-service.md)  
[CRM - Service](service-service.md)  

