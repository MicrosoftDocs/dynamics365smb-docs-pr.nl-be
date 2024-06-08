---
title: Facturen of creditnota's voor services maken
description: Leer hoe u facturen en creditnota's maakt voor uw services.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 02/27/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="create-service-invoices-or-credit-memos"></a>Servicefacturen of creditnota's maken

Gemakkelijke facturering van uw serviceorders is een van de belangrijkste kenmerken van [!INCLUDE[prod_short](includes/prod_short.md)]. U kunt uw [!INCLUDE[prod_short](includes/prod_short.md)] ook zo instellen dat een servicetechnicus op locatie een factuur kan maken voor een service die niet aan een contract of order is verbonden. U kunt [!INCLUDE[prod_short](includes/prod_short.md)] ook instellen zodat u periodiek servicecontracten factureert. Met de factuurperiode voor elk contract wordt bepaald hoe vaak u dit factureert.

## <a name="to-invoice-several-service-contracts"></a>Meerdere servicecontracten factureren

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Servicecontractfacturen maken** in en kies vervolgens de gerelateerde koppeling.  
2. Stel de filters in die u wilt toepassen.  
3. Voer in het veld **Boekingsdatum** de boekingsdatum in voor de gemaakte servicefacturen.  
4. Geef in het veld **Factureren tot datum** aan tot welke datum u contracten wilt factureren. In de batchverwerking worden de contracten met de volgende factuurdatums tot deze datum opgenomen.  
5. Kies in het veld **Actie** de optie **Facturen maken**.  
6. Kies **OK** om de servicefacturen te maken.  
  
U kunt een servicecontract ook rechtstreeks factureren vanaf de pagina **Servicecontract**, als de volgende factuurdatum op het contract eerder is dan de werkdatum.

## <a name="to-invoice-a-service-contract-from-the-service-contract-page"></a>Een servicecontract factureren via de pagina Servicecontract

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Servicecontracten** in en kies vervolgens de gerelateerde koppeling.  
2. Kies het servicecontract waarvoor u wilt factureren en open de contractkaart.  
3. Kies de actie **Servicefactuur maken**. 
4. Kies **Ja** om de servicefacturen te maken.  
  
  > [!NOTE]  
  > U kunt geen servicefacturen maken voor het servicecontract als de waarde van het veld **Wijzigingsstatus** is ingesteld op **Open**.  

## <a name="to-post-an-invoice-from-a-service-order"></a>Een factuur boeken vanuit een serviceorder

In de volgende procedure wordt beschreven hoe u het servicedeel opgeeft dat u aan de klant in rekening brengt.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Serviceorders** in en kies vervolgens de gerelateerde koppeling  
2. Kies de serviceorder waarvoor u wilt factureren en open de orderkaart.  
3. Kies de actie **Serviceregels**.  
4. Zoek de gewenste posten en geef in het veld **Te factureren aantal** het aantal op dat u in rekening gaat brengen aan de klant.  
  
   > [!NOTE]  
   > U kunt de klant voor de geregistreerde service factureren geheel of in delen. Als u ervoor kiest de klant volledig te factureren, moet de waarde in het veld **Te factureren aantal** gelijk zijn aan de waarde in het veld **Aantal**. U kunt een volledige factuur samen met een totaalverzending boeken en u kunt een volledige factuur boeken voor een reeds geboekte totaalverzending die nog niet is gefactureerd of verbruikt.  
   >  
   > Wanneer u een gedeeltelijke factuur boekt, zijn er twee manieren om het te factureren aantal op te geven. Als u de service gaat boeken met de optie **Verzenden en factureren** moet de waarde in het veld **Te factureren aantal** gelijk zijn aan die in het veld **Te verzenden aantal** veld. Als u een al geboekte verzending wilt factureren, mag het te factureren aantal niet groter zijn dan de waarde in het veld **Verzonden aantal**.  
  
5. Kies **Boeken** en klik vervolgens op **Factuur** of **Verzenden en factureren**. Ga voor informatie naar [Boeken in Servicebeheer](service-service-posting.md).  
  
 De serviceregel die u hebt geselecteerd wordt geboekt. U kunt meerdere regels tegelijk selecteren door ze allemaal te selecteren en **Boeken** te kiezen Als u dit doet, zorg er dan voor dat u alle benodigde gegevens hebt ingevuld op de regels.  
  
 Wanneer u de order boekt met de optie **Factureren** wordt een geboekte servicefactuur gemaakt samen met de overeenkomende posten en updates van de relevante velden op de serviceregels van de order. Bovendien worden de eerder geboekte verzendingsdocumenten bijgewerkt met de gefactureerde aantallen. Als u de optie **Verzenden en factureren** selecteert, wordt een geboekte verzending gemaakt.

## <a name="to-create-a-service-invoice-manually"></a>Een servicefactuur handmatig maken

Normaal gesproken, wanneer u een serviceorder boekt met de optie **Factureren** of **Verzenden en factureren**, wordt automatisch een servicefactuur geboekt. Toch kan het nodig zijn dat u een factuur moet verzenden die niet is gekoppeld aan een servicecontract of aan een order. In deze procedure wordt uitgelegd hoe u een factuur verzendt op hetzelfde moment dat de klant de service ontvangt.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Servicefacturen** in en kies vervolgens de gerelateerde koppeling.  
2. Maak een nieuwe servicefactuur.  
3. Vul het veld **Nr.** toe te wijzen.  
  
    > [!NOTE]  
    >  Als u nummerreeksen voor servicefacturen op de pagina **Servicebeheerinstellingen** hebt ingesteld, kunt u op **Enter** drukken om het eerstvolgende beschikbare servicefactuurnummer te selecteren.  
  
4. Voer in het veld **Klantnr.** het nummer van een klant in. Selecteer de betreffende klant uit de lijst.  
  
    De klantvelden worden automatisch ingevuld met gegevens uit de **Klantenkaart**.  
  
5. Geef een datum op in het veld **Boekingsdatum**. Deze datum wordt in de geboekte posten weergegeven. In dit veld wordt uw huidige werkdatum weergegeven, maar u kunt de datum wijzigen.  
6. Vul het veld **Documentdatum** een datum in die op de afgedrukte factuur wordt weergegeven en wordt gebruikt om de vervaldatum te bereken.  
7. Vul de serviceregels van de factuur in. Vul de velden **Soort**, **Nr.** en **Aantal** in om artikelen, resources en kosten te registreren die zijn gebruikt voor de serviceverlening.

## <a name="to-create-an-invoice-that-combines-posted-shipment-lines-from-one-or-more-service-orders"></a>Een factuur maken die geboekte verzendingsregels van een of meer serviceorders combineert

Het kan voorkomen dat u een servicefactuur moet opstellen voor een service die al is geleverd, vanuit één of verschillende serviceorders, maar die nog niet is gefactureerd of verbruikt. U kunt de geselecteerde geboekte verzendregels voor een bepaalde klant automatisch laten invullen op de factuurregels.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Servicefacturen** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de velden indien nodig op de regel in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 
3. Maak factuurregels voor services die zijn verzonden maar die nog niet gefactureerd. U kunt ook de actie **Verzendregels ophalen** gebruiken om geboekte verzendregels aan de factuur toe te voegen.  
4. Boek de servicefactuur.  
  
 De geboekte servicefactuur en de bijbehorende posten worden gemaakt. De eerder geboekte verzendingsdocumenten worden bijgewerkt met de gefactureerde aantallen, en de aantallen worden bijgewerkt op de serviceregels van de bronorders.  

## <a name="to-create-a-service-credit-memo"></a>Een servicecreditnota maken

Normaal gesproken gebruikt u een document met een servicecreditnota wanneer een klant een artikel retourneert. U kunt ze echter ook gebruiken om een ​​klant terug te betalen of om een ​​foutieve factuur te corrigeren.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Servicecreditnota's** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de velden indien nodig op de regel in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. In de velden **Boekingsdatum** en **Documentdatum** wordt de werkdatum weergegeven. Indien nodig kunt u deze wijzigen.    
4. Voer op de creditnotaregels gegevens in over de artikelen die zijn teruggestuurd of verwijderd of over de vergoeding die aan de klant zal worden gegeven.  

## <a name="correct-errors-in-service-invoices"></a>Fouten corrigeren in servicefacturen

U kunt servicefacturen verwijderen waaraan serviceposten zijn gekoppeld. Dit betekent dat u fouten kunt corrigeren of servicefacturen kunt wijzigen zonder dat u vastloopt of gegevens verliest. Als u bijvoorbeeld vergeet om een productboekingsgroep aan een grootboekrekening toe te wijzen, kunt u deze later toevoegen en de servicefactuur opnieuw aanmaken.

Gebruik de actie :::image type="content" source="media/copilot-delete-trash-can.png" alt-text="Actiepictogram verwijderen"::: om een ​​servicefactuur te verwijderen. 

Wanneer u een servicefactuur verwijdert, gebeurt het volgende:

* Een corrigerende servicepost boeken
* Herstel de factuurdatum en -periode in het contract, waardoor u de factuur opnieuw kunt aanmaken.

> [!NOTE]
> U kunt meerdere facturen terugboeken, maar u moet dit wel opeenvolgend doen, te beginnen bij de laatste factuur.
>
> U kunt een servicefactuur niet verwijderen als de details ervan, zoals de factureringsperiode of de schakelaar **Vooraf betaald** zijn gewijzigd in het bijbehorende servicecontract. Zorg ervoor dat u facturen verwijdert voordat u instellingen in het servicecontract wijzigt.

## <a name="see-also"></a>Zie ook

[Servicefacturen boeken](service-how-to-post-service-orders.md)  
[CRM - Service instellen](service-setup-service.md)  
[Serviceboeking](service-service-posting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
