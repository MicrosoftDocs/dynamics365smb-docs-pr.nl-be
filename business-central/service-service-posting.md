---
title: Serviceboekingen
description: Met de functionaliteit voor serviceboekingen kunt u uw documenten op een efficiënte manier verwerken en zorgen voor een geslaagd klantenservicebeleid.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# Serviceboekingen
Met de functionaliteit voor serviceboekingen kunt u uw documenten op een efficiënte manier verwerken en zorgen voor een geslaagd klantenservicebeleid. U kunt geboekte documenten maken en bijwerken, en posten maken zowel in het servicegebied als in andere modules om een juiste updateprocedure te waarborgen.  

> [!NOTE]  
>  Het volgende beschrijft serviceboekingen, ongeacht hoe artikelen fysiek worden verwerkt in het magazijn.  
>   
>  Op een locatie waarvoor magazijnverwerking niet is ingesteld, boekt u rechtstreeks vanaf de pagina **Serviceregels**. In vestigingen met magazijnverwerking, worden de beschreven boekingen, met uitzondering van verzenden en verbruiken, indirect uitgevoerd met variërende verzendfuncties, afhankelijk van de instellingen. Zie voor meer informatie [Artikelen picken met een voorraadpick](warehouse-how-to-pick-items-with-inventory-picks.md).  

## Verzenden  
Met de optie Verzenden kunt u de betreffende artikelen en perioden registreren die zijn ingevoerd op de regels van een serviceorder nadat de service is uitgevoerd. Er wordt een geboekte verzending gemaakt en het uit voorraad halen van de artikelen en verzenden hiervan naar de klanten wordt bijgewerkt in de voorraadmodule en in andere modules in [!INCLUDE[prod_short](includes/prod_short.md)]. Dit houdt in dat er artikelposten, waardeposten, serviceposten en garantieposten worden geproduceerd.  

Als magazijnverwerking verplicht is voor de vestiging, dan verloopt het verzenden en verplaatsen van serviceregelartikelen net zoals bij andere brondocumenten. Het enige verschil is dat serviceregelartikelen extern of intern kunnen worden verbruikt, wat twee verschillende functies vereist voor het vrijgeven van orders.

## Factureren  
U gebruikt de optie Factureren om een factuur te verzenden naar de klant waarbij u de kosten voor de service in rekening wilt brengen. In de meeste gevallen wordt het verschil gefactureerd tussen het verzonden aantal dat wordt vastgelegd door de functie **Verzending boeken** en het verbruikte aantal dat wordt vastgelegd door de functie **Verbruik boeken**. Wat niet is verzonden, kan niet worden gefactureerd. Wanneer de functie **Facturen boeken** wordt uitgevoerd, wordt een geboekte servicefactuur gemaakt en worden de eerder geboekte documenten bijgewerkt zodat ze overeenkomen met de aantallen die zijn vermeld in de verzonden factuur. Net als bij andere boekingsprocedures worden de desbetreffende posten gemaakt (met inbegrip van de grootboekposten).  

## Verzenden en factureren  
Met de optie verzenden en factureren kunt u tegelijkertijd een serviceverzending en een factuur verzenden.  

## Verzenden en verbruiken  
Met de optie verzenden en verbruiken kunt u artikelen, kosten of uren registreren en boeken die zijn gebruikt voor serviceverlening maar die niet in de factuur voor de klant kunnen worden opgenomen. Er wordt geen factuur verzonden, maar u kunt wel gelijktijdig een serviceverzending en een serviceverbruik boeken om vast te leggen dat enkele artikelen of uren gratis aan de klant zijn gegeven. Ook worden de bijbehorende posten gemaakt om het verbruik te registreren.  

> [!NOTE]  
>  Met de procedure voor serviceboekingen kunt u gedeeltelijke boekingen uitvoeren. U kunt een gedeeltelijke verzending of een gedeeltelijke factuur maken door de velden **Te verzenden aantal** en/of **Te factureren aantal** op de afzonderlijke serviceregels van de serviceorders in te vullen vóór de boeking. U kunt geen factuur maken voor zaken die niet zijn verzonden. Voordat u een factuur kunt opstellen, moet u dus een verzending hebben geregistreerd (of u kunt ervoor kiezen tegelijk te verzenden en factureren).  

Nadat de boeking is voltooid, kunt u de geboekte servicedocumenten bekijken vanaf de desbetreffende pagina's (**Geboekte serviceverzending** en **Geboekte servicefactuur**). Er zijn verschillende pagina's met geboekte posten waarin u kunt zien welke geboekte posten er zijn gemaakt, zoals **Grootboekposten**, **Artikelposten**, **Magazijnposten**, **Serviceposten**, **Projectposten** en **Garantieposten**.  

## Informatie over een geboekt servicedocument bekijken  
Wanneer u een servicefactuur, een serviceverzending of een servicecreditnota boekt, worden de gegevens in het document overgebracht naar de respectieve pagina's **Geboekte servicefactuur**, **Geboekte serviceverzending** of **Geboekte servicecreditnota**. Op deze pagina's kunt u geen gegevens invoeren, wijzigen of verwijderen. U kunt een verzending, factuur of creditnota vanaf deze pagina's afdrukken.  

In de volgende procedure wordt een geboekte servicefactuur als voorbeeld gebruikt, maar dezelfde procedure kan worden toegepast op geboekte serviceverzendingen en geboekte creditnota's.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Geboekte servicefactuur** in en kies vervolgens de gerelateerde koppeling  
2. Open de geboekte servicefactuur die u wilt bekijken.  
3. Voor een overzicht van de geboekte factuur kiest u de actie **Statistieken**.  

    De pagina **Serviceorderstatistiek** verschijnt. De pagina bevat informatie over aantallen, bedragen, btw, kosten, winst en klantkredietlimiet voor het geboekte document.

## Zie ook  
[Serviceorders boeken](service-how-to-post-service-orders.md)   
[Serviceorders maken](service-how-to-create-service-orders.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]