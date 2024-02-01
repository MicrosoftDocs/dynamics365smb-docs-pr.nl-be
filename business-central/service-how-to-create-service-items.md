---
title: Serviceartikelen maken
description: 'Lees over de verschillende manieren waarop u serviceartikelen kunt maken in Business Central, bijvoorbeeld binnen een serviceorder of bij het verzenden van artikelen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="create-service-items"></a>Serviceartikelen maken

In [!INCLUDE[prod_short](includes/prod_short.md)] verwijst de term serviceartikel naar de apparatuur of artikelen die service vereisen. Wanneer u een serviceorder maakt, geeft u de artikelen op die service nodig hebben. In de order kunt u een serviceartikel aan een artikel in de voorraad of aan een serviceartikelgroep koppelen.    

Wanneer u een artikel ontvangt dat service vereist, kunt u dit artikel registreren als serviceartikel. Dit kunt u op verschillende manieren doen. U kunt bijvoorbeeld via de pagina **Serviceartikelen** een serviceartikel maken of als onderdeel van een ander proces, bijvoorbeeld wanneer u met een serviceorder werkt.   

## <a name="to-create-a-service-item"></a>Een serviceartikel maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Serviceartikelen** in en kies vervolgens de gerelateerde koppeling
2. Vul de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-create-service-items-within-a-service-order"></a>Serviceartikelen maken in serviceorders

Wanneer u artikelen voor service ontvangt die u wilt registreren als serviceartikelen, kunt u deze instellen als serviceartikelen op de pagina **Serviceorder** of **Serviceofferte**.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Serviceorders** in en kies vervolgens de gerelateerde koppeling  
2. Vul de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
3. Kies de actie **Serviceartikel maken**.  

    Er wordt een nummer aan het serviceartikel toegewezen en een kaart voor het serviceartikel gemaakt. Het nummer van het nieuwe serviceartikel wordt ingevuld in het veld **Serviceartikelnr.**

## <a name="to-create-a-service-item-when-shipping-items"></a>Serviceartikelen maken tijdens het verzenden van artikelen

Als u artikelen verzendt door verkooporders of verkoopfacturen te boeken, worden de verzonden artikelen automatisch als serviceartikelen geregistreerd als aan de volgende voorwaarde wordt voldaan. De artikelen moeten behoren tot een serviceartikelgroep waarvoor het selectievakje **Serviceartikel maken** is ingeschakeld. Als voor de artikelen serienummers zijn geregistreerd op de pagina Artikeltraceringsregels, worden deze gegevens tijdens het maken van serviceartikelen automatisch gekopieerd naar het veld **Serienummer** op de serviceartikelkaart.  

Hieronder wordt aangegeven hoe u serviceartikelen kunt maken tijdens het verzenden van artikelen in verkooporders.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.  
2. Open de betreffende verkooporder.  
3. Kies de actie **Boeken** of **Boeken en afdrukken**.  
4. Kies de actie **Verzenden** of **Verzenden en factureren**.  
5. Er worden automatisch serviceartikelen gemaakt voor de artikelen op de order, wanneer deze behoren tot een serviceartikelgroep die u hebt ingesteld om serviceartikelen te maken. Als u bepaalde serienummers op de pagina **Artikeltraceringsregels** hebt geregistreerd, worden deze dienovereenkomstig aan deze serviceartikelen toegewezen.  

> [!NOTE]  
>  Als een artikel is ingesteld als stuklijst en u de stuklijst hebt getoond, worden de getoonde stuklijstartikelen verwerkt als gewone artikelen. Serviceartikelen worden gemaakt op basis van de voorwaarde serviceartikelgroep en optioneel op de voorwaarde serienummers. Als een serviceartikel wordt gemaakt voor een getoond stuklijstartikel waarin andere stuklijstonderdelen zijn opgenomen, worden deze artikelen gemaakt als serviceartikelonderdelen voor het getoonde stuklijstserviceartikel.  
>   
>  Is een artikel ingesteld als stuklijst en hebt u de stuklijst niet getoond, dan wordt hiervoor een serviceartikel gemaakt op basis van de voorwaarde serviceartikelgroep en optioneel de voorwaarde serienummers.  

## <a name="to-insert-a-starting-fee-for-a-service-item"></a>Starttarieven invoegen voor serviceartikelen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Servicetaken** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Artikelwerkbon**.
3. Kies de serviceregel en kies vervolgens **Acties**, **Functies** en de actie **Starttarief invoegen**.  

    Er wordt een serviceregel van het type **Kosten** ingevoegd met het starttarief. Het starttarief is van toepassing op het geselecteerde serviceartikel.

## <a name="see-also"></a>Zie ook

[Serviceartikelen en serviceartikelonderdelen instellen](service-how-setup-service-items.md)  
[CRM - Service instellen](service-setup-service.md)  
[Servicebeheer](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
