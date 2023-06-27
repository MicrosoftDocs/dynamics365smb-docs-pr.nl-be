---
title: Serviceorders boeken
description: 'Wanneer u een serviceorder hebt gemaakt, de benodigde gegevens hebt ingevuld en eventuele wijzigingen hebt aangebracht, kunt u de serviceorder boeken.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: edupont
---
# <a name="post-service-orders-and-credit-memos"></a>Serviceorders en creditnota's boeken
Wanneer u een serviceorder hebt gemaakt, de benodigde gegevens hebt ingevuld en eventuele wijzigingen hebt aangebracht, kunt u de serviceorder boeken. De order moet minimaal één serviceartikelregel en één serviceregel bevatten voordat u deze kunt boeken. Als de order meer dan één serviceregel bevat, worden alle regels tegelijk geboekt.  

Als u een groot aantal serviceorders hebt, kunt u tijd besparen door deze tegelijkertijd in een batchverwerking te boeken. U kunt de batchverwerking vanuit elke serviceorder uitvoeren.

> [!Tip]
> Voordat u een servicedocument boekt, is het een goed idee om de actie **Testrapport** te gebruiken om het document te controleren op eventuele fouten of ontbrekende gegevens. Als er fouten zijn, moet u het probleem oplossen. U kunt een nieuw testrapport afdrukken om de correctie te controleren en vervolgens kunt u het document boeken.

## <a name="to-post-a-service-order"></a>Serviceorders boeken
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Serviceorders** in en kies vervolgens de gerelateerde koppeling  
2. Open de betreffende serviceorder.  
3. Op de pagina **Serviceorder** kiest u een van de volgende acties.  

    |**Actie**|**Resultaat**|  
    |------------------|----------------|  
    |**Controlelijst** | Alle delen van het document worden gecontroleerd en de resultaten worden in een lijst weergegeven. Als er fouten of ontbrekende gegevens zijn gevonden, moet u de problemen corrigeren. Vervolgens kunt u een nieuwe controlelijst afdrukken.|  
    |**Boeken** | Hiermee boekt u de order zonder dat u een verzending of factuur afdrukt.|  
    |**Boeken en afdrukken** | Hiermee boekt u de order en wordt een verzending afgedrukt (als u de order verzendt zonder deze te factureren) of een factuur afgedrukt (als u de order factureert).|  
    |**Batchboeken** | Hiermee boekt u meerdere serviceorders tegelijkertijd eenmaal.|  

4. Wanneer u de order boekt, moet u een van de volgende opties opgeven voor de manier waarop u de order wilt boeken.  

    |**Boekingsoptie**|**Resultaat**|  
    |------------------------|----------------|  
    |**Verzending** | Hiermee wordt de verzending van de artikelen geboekt.|  
    |**Factuur** | Hiermee factureert u de artikelen die al zijn verzonden.|  
    |**Verzenden en factureren** | Hiermee factureert en verzendt u de artikelen.|  
    |**Verzenden en verbruiken** | De verzending en het verbruik voor de order worden geboekt. De betreffende aantallen op de serviceregels van de order en op het eerder geboekte serviceverzendingsdocument, worden bijgewerkt.|  

U kunt verbruik alleen boeken als de regel een aantal bevat dat is verzonden, maar nog niet is gefactureerd of verbruikt.  

Wanneer de order wordt geboekt, worden de bijbehorende posten en geboekte documenten gemaakt. Tevens worden de betreffende velden in het serviceorderdocument bijgewerkt.  

## <a name="to-batch-post-service-orders"></a>Serviceorders batchboeken
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Serviceorders** in en kies vervolgens de gerelateerde koppeling  
2. Kies de actie **Batch boeken**.  
3.  U kunt een filter instellen om bepaalde serviceordernummers of een interval van ordernummers te selecteren dat u met de batchverwerking wilt verwerken.  
4.  Kies **OK** om de batchverwerking te starten.  

## <a name="to-post-a-service-credit-memo"></a>Servicecreditnota's boeken
Wanneer u een servicecreditnota hebt gemaakt en ingevuld, kunt u de creditnota boeken. Als er fouten worden aangetroffen of als er gegevens ontbreken op de creditnota bij het boeken, wordt het proces onderbroken door een foutbericht.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Servicecreditnota's** in en kies vervolgens de gerelateerde koppeling.  
2. Maak een nieuwe servicecreditnota. Kies de actie **Nieuw**.  
3. Vul de benodigde velden in.  
4. Kies de actie **Boeken**. Als u de creditnota bij het boeken wilt afdrukken, kiest u in plaats daarvan de actie **Boeken en afdrukken**.  
5. Kies **Controlelijst** om creditnota's te testen voordat u deze boekt. Wanneer u het rapport uitvoert, worden de boekingsdatums die zijn opgegeven in het document gecontroleerd.  
6. Als u verschillende servicecreditnota's tegelijkertijd wilt boeken, voert u de batchverwerking **Batchboeken servicecreditnota's** uit. Dit kan een voordeel zijn als u een groot aantal creditnota's wilt boeken.  

> [!NOTE]  
>  Het is belangrijk dat u alle benodigde gegevens op de creditnota's invoert voordat u deze batchboekt. Anders worden de nota's mogelijk niet geboekt. Wanneer de boeking is uitgevoerd met de batchverwerking, wordt een bericht weergegeven waarin wordt aangegeven hoeveel servicecreditnota´s zijn geboekt.  

## <a name="to-post-consumption-from-a-service-order"></a>Verbruik boeken vanuit een serviceorder
In de volgende procedure wordt beschreven hoe u de artikelen, resource-uren of -kosten boekt die zijn gebruikt voor een bepaalde servicewerkzaamheid die u niet in rekening brengt aan uw klant. Verbruikte artikelen, uren of kosten kunnen alleen worden geboekt voor een geboekte verzending waarvoor geen facturen of verbruik zijn geboekt.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Serviceorders** in en kies vervolgens de gerelateerde koppeling  
2. Open de serviceorder waarvoor u verbruik wilt boeken.  
3. Kies het service-item. Kies de actie **Serviceregels**.  
4. Vind de gewenste posten en geef in het veld **Te verbruiken aantal** het aantal op waarvoor u verbruik gaat boeken. Het aantal mag niet groter zijn dan het reeds verzonden aantal en het resterende aantal dat niet is gefactureerd na een gedeeltelijke facturering van de verzending.  

    > [!NOTE]  
    >  Als u verbruik wilt registeren voor een project, moet u de velden **Projectnr.**, **Projecttaaknr.** en **Projectregelsoort** op de serviceregel invullen.  

5. Kies de te boeken regels en kies vervolgens de actie **Boeken**. Selecteer **Verzenden en verbruiken** op de pagina die wordt geopend.  

De service wordt nu als geheel of gedeeltelijk verbruikt geboekt, afhankelijk van de waarde in het veld **Te verbruiken aantal**, en de desbetreffende posten worden gemaakt. Bovendien worden de eerder geboekte serviceverzendingsdocumenten chronologisch bijgewerkt met de verbruikte aantallen. De desbetreffende aantallen worden bijgewerkt op de serviceregels van de order.  

## <a name="to-post-shipments-from-service-orders"></a>Verzendingen vanuit serviceorders boeken
Nadat u de details van een service hebt opgegeven, kunt u de aantallen aanpassen en boeken voor verbruikte artikelen, opgelopen kosten en tijd die is besteed. Naar aanleiding hiervan worden de noodzakelijke wijzigingen aangebracht in [!INCLUDE[prod_short](includes/prod_short.md)] om ervoor te zorgen dat de gegevens consistent zijn met de nieuwe voorraadstaat en met de huidige verwerkingsstaat van de desbetreffende order.  

De volgende procedure laat zien hoe u de verzending van serviceregelartikelen kunt boeken voor vestigingen waarvoor de magazijnverwerking niet vereist is.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Serviceorder** in en kies vervolgens de gerelateerde koppeling 2. op de pagina voor de geselecteerde serviceorder op **Acties**, **Order** en **Serviceregels**.  
3. Zoek op de pagina **Serviceregels** de vereiste posten en geef in het veld **Te verzenden aantal** het te boeken aantal op.  

   > [!NOTE]  
   >  De waarde voor het te verzenden aantal hangt ervan af of u een volledige of gedeeltelijke boeking kiest voor de verzending. Als u kiest voor een volledige verzending, moet de waarde in het veld **Te verzenden aantal** gelijk zijn aan de waarde in het veld **Aantal**. Wanneer u een gedeeltelijke verzending boekt, moet u opgeven welk aantal u aanvankelijk wilt verzenden. Als u een deel van de service op de order al hebt verzonden, moet u de waarde hiervan vastleggen in het veld **Verzonden aantal**. Het maximale aantal dat u kunt opgeven in het veld **Te verzenden aantal** is het aantal eenheden dat nog niet is verzonden.  

4. Kies de actie **Boeken**. Kies de knop **Verzenden** op de pagina die wordt geopend.

In [!INCLUDE[prod_short](includes/prod_short.md)] worden posten gemaakt (garantieposten, artikelposten, serviceposten of grootboekposten). Daarnaast wordt het geboekte serviceverzendingsdocument gemaakt en worden de betreffende velden op de serviceregels van de serviceorder bijgewerkt.  

Als magazijnverwerking verplicht is voor de vestiging, dan verloopt het verzenden en verplaatsen van serviceregelartikelen net zoals bij andere brondocumenten. Het enige verschil is dat serviceregelartikelen extern of intern kunnen worden verbruikt, en er daarom twee verschillende functies vereist zijn voor het vrijgeven van orders.  

Ga voor meer informatie over regelartikelen voor verzendservices in geavanceerde magazijnconfiguraties naar Artikelen picken voor magazijnverzending](warehouse-how-to-pick-items-for-warehouse-shipment.md).  

## <a name="to-undo-posted-consumption"></a>Geboekt verbruik ongedaan maken
U kunt het verbruik annuleren voor de serviceorders. Het kan bijvoorbeeld voorkomen dat u verbruik per ongeluk boekt.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Geboekte serviceverzendingen** in en kies vervolgens de gerelateerde koppeling.  
2. Open de geboekte serviceverzending waarvoor het foutieve verbruik is geboekt.  
3. Kies de actie **Servicezendingsregels**.  
4. Kies de regels die het foutieve verbruik bevatten en kies de actie **Verbruik ongedaan maken**.  

 Er wordt een tegenboekingsregel ingevoegd voor de serviceverzending. Deze regel bevat negatieve waarden in de velden met aantallen voor de geselecteerde regels.  
  
> [!NOTE]  
>  U kunt serviceverbruik niet ongedaan maken als:  

>    * De serviceorder is gesloten.  
>    * Het is geboekt naar de module Projecten, zodat er projectposten aan zijn gekoppeld.  

## <a name="to-post-service-lines"></a>Serviceregels boeken
Als u wat langer aan een serviceorder moet werken voordat u deze kunt boeken, wilt u wellicht enkele van de gekoppelde serviceregels boeken, bijvoorbeeld om de voorraad bijgewerkt te houden. U kunt deze boeken door de betreffende aantallen op de te boeken regels op te geven. U kunt de regels één voor één boeken, of door verschillende regels tegelijk te selecteren.  

De volgende procedure beschrijft het boeken van verzendingen rechtstreeks vanuit een serviceorder van vestigingen zonder ingestelde magazijnverwerkingen. Als een magazijnverwerking verplicht is voor de vestiging, gebeurt het boeken van verzendingen in een ander magazijndocument, afhankelijk van de instellingen van de vestiging.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Serviceorders** in en kies vervolgens de gerelateerde koppeling  
2. Open de serviceorder en kies de actie **Serviceregels**.  
4. Vul op de te boeken regels de velden **Te verzenden aantal**, **Te factureren aantal** en **Te verbruiken aantal** in, afhankelijk van de manier waarop u de regels wilt boeken.  
5. Kies de actie **Boeken**.

## <a name="see-also"></a>Zie ook
[Boeken in CRM - Service](service-service-posting.md)  
[Een serviceorder maken](service-how-to-create-service-orders.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
