---
title: Prijzen en kosten voor services instellen
description: 'Leer hoe u prijsstellingsfuncties gebruikt om uw toepassing zo in te stellen en aan te passen dat u prijzen voor serviceartikelen, herstelbewerkingen en orders kunt toepassen en wijzigen.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'service, cost, service order'
ms.date: 06/25/2021
ms.author: edupont
---

# <a name="set-up-pricing-and-additional-costs-for-services"></a>Prijzen en aanvullende kosten voor services instellen
Met de prijsstellingsfuncties van [!INCLUDE[prod_short](includes/prod_short.md)] kunt u uw toepassing zo instellen en aanpassen dat u prijzen voor serviceartikelen, herstelbewerkingen en orders kunt toepassen en wijzigen. Deze prijsbeslissingen kunnen vervolgens gemakkelijk worden overgebracht naar het factureringsproces.  
  
Desgewenst kunt u prijsgroepen instellen en deze toewijzen aan specifieke perioden, klanten of valuta. U kunt vaste prijzen, minimum- of maximumprijzen instellen op basis van de servicecontracten die u hebt opgesteld voor klanten. Ten slotte kunt u tijdens het aanpassen van uw prijzen de wijzigingen weergeven en goedkeuren voordat u ze in het grootboek opneemt.  

## <a name="to-set-up-a-service-price-group"></a>Serviceprijsgroepen instellen
U kunt groepen met serviceartikelen instellen waarvoor dezelfde speciale serviceprijzen moeten gelden. U wijst serviceprijsgroepen toe aan serviceartikelen op serviceartikelregels. U kunt ook serviceprijsgroepen toewijzen aan serviceartikelgroepen.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Serviceprijsgroepen** in en kies vervolgens de gerelateerde koppeling.  
2. Maak een nieuwe serviceprijsgroep.  
3. Vul de velden **Code** en **Omschrijving** in.  
4. Kies de actie **Instellingen**.  
2. Vul de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

 > [!Tip]
 > Op basis van de velden **Herwaarderingssoort** en **Bedrag** wordt bepaald of een herwaardering om een vast bedrag gaat of alleen van toepassing is als de totale serviceprijs hoger of lager is dan het bedrag in het veld **Bedrag**.  

## <a name="to-set-up-a-service-price-adjustment-group"></a>Serviceprijsherwaarderingsgroepen instellen
U kunt prijsaanpassingsgroepen instellen om de serviceprijzen van serviceartikelen aan te passen. U kunt bijvoorbeeld de prijsaanpassingsgroep instellen om de prijzen van vracht of reserveonderdelen aan te passen.  
  
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Serviceprijsherwaarderingsgroepen** in en kies vervolgens de gerelateerde koppeling.  
2. Maak een nieuwe serviceprijsherwaarderingsgroep.  
3. Vul de velden **Code** en **Omschrijving** in.  
4. Voer in het veld **Soort** de soort post in die u wilt aanpassen.  
  
    * Als u slechts één bepaalde post wilt aanpassen, moet u het nummer van deze post in het veld **Nr.** invoeren. Als u dit veld leeg laat, worden met de herwaarderingsgroep alle posten aangepast van de soort die is gedefinieerd in het veld **Soort**.  
    * Vul het veld **Werksoort** in als u serviceprijzen wilt aanpassen die zijn gerelateerd aan slechts één bepaalde service. Als u dit veld leeg laat, wordt het genegeerd.  
  
5. In het veld **Omschrijving** voert u een korte omschrijving van de serviceprijsherwaardering in.  
6. Als u serviceprijzen wilt aanpassen die aan slechts één bepaalde productboekingsgroep zijn gerelateerd, vult u het veld **Productieboekingsgroep** in.

> [!Tip]
> U kunt **Details** kiezen om aanvullende informatie over de herwaarderingsgroep toe te voegen. U kunt bijvoorbeeld aangeven welke items horen bij de serviceprijsherwaarderingsgroep en of het hierbij gaat om een artikel, resource, resourcegroep of administratiekosten.  

## <a name="to-set-up-additional-costs-for-services"></a>Aanvullende kosten voor services instellen
Wanneer u met serviceartikelen en -orders werkt, moet u mogelijk aanvullende kosten, zoals reiskosten naar bepaalde serviceregio's of starttarieven, registreren. Wanneer u een serviceorder maakt, kunt u deze kosten invoegen en wordt er een regel van het type **Kosten** aan de order toegevoegd. Als u de kosten wilt toepassen op alle serviceorders, kunt u standaardkosten instellen. Dit kunt u bijvoorbeeld doen als u een starttarief wilt toepassen.
  
### <a name="to-set-up-service-costs"></a>Servicekosten instellen
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Servicekosten** in en kies vervolgens de gerelateerde koppeling. 
2. Vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

### <a name="to-specify-a-default-cost-for-service-orders"></a>Standaardkosten opgeven voor serviceorders
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Service-instellingen** in en kies vervolgens de gerelateerde koppeling. 
2. In het veld **Starttarief serviceorder** kiest u de betreffende servicekosten.

## <a name="see-also"></a>Zie ook
[CRM - Service instellen](service-setup-service.md)  
[Servicebeheer](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
