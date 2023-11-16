---
title: Artikelen ontvangen
description: Dit artikel is een overzicht van de verschillende manieren om artikelen in een magazijn te ontvangen met een magazijnontvangst.
author: brentholtorf
ms.author: bholtorf
ms.topic: how-to
ms.date: 09/02/2022
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5768, 7330, 7332, 7333, 7342, 7363, 8510, 9008'
---
# <a name="receive-items-with-warehouse-receipts"></a>Artikelen ontvangen met magazijnontvangsten

In [!INCLUDE[prod_short](includes/prod_short.md)] gebeurt het ontvangen en opslaan op een van de volgende vier manieren, zoals beschreven in de volgende tabel.

|Methode|Inkomend proces|Ontvangst vereist|Opslag vereist|Complexiteitsniveau (meer informatie op [Overzicht van magazijnbeheer](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Ontvangst en opslag van de orderregel boeken|||Geen specifieke magazijnactiviteit.|  
|B|Ontvangst en opslag van een voorraadopslagdocument boeken||Ingeschakeld|Basis: Order voor order|  
|H|Ontvangst en opslag van een magazijnontvangstdocument boeken|Ingeschakeld||Basis: Geconsolideerde boeking voor ontvangen/verzenden voor meerdere orders.|  
|D|Ontvangst van een magazijnontvangstdocument en opslag van een magazijnopslagdocument boeken|Ingeschakeld|Ingeschakeld|Geavanceerd|  

Ga voor meer informatie over het afhandelen van inkomende artikelen naar [Inkomende magazijnstroom](design-details-inbound-warehouse-flow.md).

Het volgende artikel verwijst naar methoden C en D in de vorige tabel.

## <a name="receive-items-with-a-warehouse-receipt"></a>Artikelen ontvangen met een magazijnontvangst

Bij ontvangst van artikelen in een magazijn waarvoor magazijnontvangstverwerking is ingesteld, moet u de regels ophalen van het vrijgegeven brondocument waaruit de ontvangst voortkomt. Als u opslaglocaties gebruikt, kunt u de standaardopslaglocatie accepteren of de opslaglocatie specificeren om de items weg te zetten. Dit laatste kan nodig zijn wanneer u een artikel voor de eerste keer ontvangt. Vervolgens moet u de aantallen van de ontvangen artikelen invullen en de ontvangst boeken.  

U kunt een magazijnontvangst op twee manieren maken:

* Met pushing wanneer er per order wordt gewerkt. Kies de actie **Magazijnontvangst maken** in het brondocument, zoals Inkooporder, Verkoopretourorder of Transferorder om magazijnontvangst voor één brondocument aan te maken.
* Door middel van pushing, waarbij u de actie **Vrijgeven** in het brondocument gebruikt, zoals een inkooporder, verkoopretourorder of transferorder, om het document vrij te geven aan het magazijn. Een magazijnmedewerker maakt een **magazijnontvangst** voor een of meer vrijgegeven brondocumenten. In de volgende procedure wordt beschreven hoe u een magazijnontvangst met pushing maakt. In de volgende procedure wordt beschreven hoe u een magazijnontvangst met pushing maakt.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Magazijnontvangsten** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  

    Vul het veld **Vestiging** op het sneltabblad **Algemeen** in. Bij het ophalen van brondocumentregels worden bepaalde gegevens automatisch naar elke regel gekopieerd.

    Voor een vestiging waarvoor opslaglocaties vereist zijn, vult u het veld **Opslaglocatie** in. Afhankelijk van uw configuratie kan [!INCLUDE[prod_short](includes/prod_short.md)] de locatie voor u toevoegen. Ga voor meer informatie naar [Zonecodes en opslaglocatiecodes](warehouse-how-receive-items.md#zone-and-bin-codes).  

3. U kunt een brondocument op twee manieren ophalen:

    1. Kies de actie **Brondocumenten ophalen**. De pagina **Brondocumenten - Inkomend** verschijnt. Hier kunt u een of meer brondocumenten selecteren die zijn vrijgegeven naar het magazijn waarvoor ontvangst vereist is.
    2. Kies de actie **Filters om brondoc. op te halen gebruiken**. De pagina **Filters om brondocumenten op te halen - Inkomend** wordt geopend. Hier kunt u een brondocumentfilter selecteren en uitvoeren. Alle vrijgegeven brondocumentregels die aan de filtercriteria voldoen, worden toegevoegd op de pagina **Magazijnontvangst**. Meer info op [Procedure: Filters gebruiken om brondocumenten op te halen](warehouse-how-receive-items.md#how-to-use-filters-to-get-source-documents).

4. Stel de te ontvangen hoeveelheid in.

    Het veld **Te ontvangen aantal** bevat de openstaande hoeveelheid voor elke regel, maar u kunt het aantal wijzigen indien nodig. 

    Als u de waarde in het veld **Te ontvangen aantal** op alle regels wilt instellen op nul, kiest u de actie **Te ontvangen aantal verwijderen**. Het op nul zetten van de hoeveelheden is bijvoorbeeld handig als u een streepjescodescanner gebruikt om de ontvangen hoeveelheden bij te werken. Als u de openstaande hoeveelheden van het brondocument opnieuw wilt toevoegen, kiest u de actie **Te ontvangen aantal automatisch invullen**.  

    Op een magazijnontvangstdocument waarbij de ontvangen hoeveelheid hoger is dan besteld, voert u de werkelijk ontvangen hoeveelheid in het veld **Te ontvangen aantal** in. Als de verhoging binnen de tolerantie valt die is gespecificeerd door de toegewezen meerontvangstcode, wordt het veld **Meer ontvangen hoeveelheid** bijgewerkt om de hoeveelheid weer te geven waarmee de waarde in het veld **Aantal** is overschreden. Als de verhoging hoger is dan de opgegeven tolerantie, is de meerontvangst niet toegestaan.

5. Boek de magazijnontvangst. De velden met aantallen in de brondocumenten worden bijgewerkt en de artikelen worden aan de voorraad toegevoegd.  

    [!INCLUDE [preview-posting-shipment](includes/preview-posting-shipment.md)]

    > [!TIP]
    > Als u magazijnopslag gebruikt, wat verwijst naar methode D in de tabel aan het begin van dit artikel, worden de artikelen ontvangen maar kunnen ze pas worden gepickt nadat ze zijn opgeslagen. Ga voor meer informatie over het opslaan van artikelen naar [Artikelen opslaan met magazijnopslag](warehouse-how-to-put-items-away-with-warehouse-put-aways.md).
    >
    > Overweeg anders de actie **Boeken en afdrukken**. De actie boekt de ontvangst en drukt deze af als een opslaginstructie die aangeeft waar het artikel moet worden opgeslagen.

    > [!NOTE]  
    > Als uw magazijn crossdocking gebruikt, kunt u controleren of u artikelen kunt crossdocken zonder ze op te slaan. Ga voor meer informatie over cross-docking naar [Artikelen cross-docken](warehouse-how-to-cross-dock-items.md).

## <a name="how-to-use-filters-to-get-source-documents"></a>Filters gebruiken om brondocumenten op te halen

U kunt vanuit een magazijnontvangst de pagina **Filters om brondocumenten op te halen** gebruiken voor het ophalen van de vrijgegeven brondocumentregels die bepalen welke artikelen moeten worden ontvangen.

1. Kies in de magazijnontvangst de actie **Filters om brondocumenten op te halen gebruiken**.
2. U stelt een nieuw filter in door een omschrijvende code in te voeren in het veld **Code** en vervolgens de actie **Wijzigen** te kiezen.

    De pagina **Brondocumentfilterkaart - Inkomend** verschijnt.

3. Gebruik de filters om het type brondocumentregels te definiëren dat moet worden opgehaald. U kunt bijvoorbeeld soorten brondocumenten selecteren, zoals inkoop- of transferorders.
4. Kies **Uitvoeren**.  

Alle vrijgegeven brondocumentregels die voldoen aan de filtercriteria worden toegevoegd op de pagina **Magazijnontvangst** van waaruit u de filters hebt geactiveerd.

U kunt een onbeperkt aantal filtercombinaties maken. Filters worden opgeslagen op de pagina **Filters om brondocumenten op te halen** en ze zijn beschikbaar als u ze nodig hebt. U kunt de criteria op elk moment wijzigen door de actie **Wijzigen** te kiezen.

## <a name="zone-and-bin-codes"></a>Zone- en opslaglocatiecodes

Als u artikelen wilt ontvangen met andere magazijnklassen dan de magazijnklasse van de opslaglocatie in het veld **Opslaglocatie** op de documentkop, wist u het veld **Opslaglocatie** op de kop voordat u de brondocumentregels voor de artikelen ophaalt.  
<!-- TBD, table with comparison of various options-->

Als opslaglocaties verplicht zijn voor een locatie, worden zone- en opslaglocatiecodes als volgt toegevoegd aan magazijnontvangstdocumenten:

* Voor geavanceerde configuraties die gestuurde opslag en pick gebruiken, gebruikt [!INCLUDE [prod_short](includes/prod_short.md)] de ontvangstopslaglocatie van de pagina **Vestiging** voor de vestiging. Als er geen ontvangstopslaglocatie is opgegeven, wordt er geen opslaglocatie opgegeven. Als het artikel en de ontvangstopslaglocaties niet overeenkomen, is de ontvangstopslaglocatie leeg.
* In andere configuraties, als er geen ontvangstopslaglocatie is opgegeven, gebruikt [!INCLUDE [prod_short](includes/prod_short.md)] de opslaglocatie van het brondocument.

## <a name="see-also"></a>Zie ook

[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
