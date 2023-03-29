---
title: Artikelen verzenden
description: In dit artikel wordt beschreven hoe u artikelen verzendt vanuit uw magazijn.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
ms.search.form: '7335, 7337, 7339, 7340, 7341, 7362, 9008'
---

# Artikelen verzenden met een magazijnverzending

In [!INCLUDE[prod_short](includes/prod_short.md)] gebeurt het ontvangen en opslaan op een van de volgende vier manieren, zoals beschreven in de volgende tabel.

|Methode|Uitgaand proces|Pick vereist|Verzending vereist|Complexiteitsniveau (meer informatie op [Overzicht van magazijnbeheer](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Picken en verzending vanaf de orderregel boeken|||Geen specifieke magazijnactiviteit.|  
|B|Picken en verzending vanuit een voorraadpickdocument boeken|Ingeschakeld||Basis: Order voor order|  
|H|Picken en verzending vanuit een magazijnverzendingdocument boeken||Ingeschakeld|Basis: Geconsolideerde boeking voor ontvangen/verzenden voor meerdere orders.|  
|D|Picken vanuit een magazijnpickdocument boeken en verzending vanuit een magazijnverzendingdocument boeken|Ingeschakeld|Ingeschakeld|Geavanceerd|  

Ga voor meer informatie over het verzenden van artikelen naar [Uitgaande magazijnstroom](design-details-outbound-warehouse-flow.md).

Dit artikel verwijst naar methoden C en D in de tabel. Bij beide methoden maakt u eerst een verzendingsdocument op basis van een bedrijfsbrondocument. Vervolgens pickt u de opgegeven artikelen voor de verzending.

Wanneer een vestiging magazijnverzendingen vereist, kunt u artikelen verzenden op basis van brondocumenten die zijn vrijgegeven voor het magazijn. Door brondocumenten vrij te geven, zijn de artikelen die erop staan gereed voor verwerking in het magazijn. Het volgende zijn voorbeelden van brondocumenten:

* Verkooporders
* Inkoopretourorders
* Transferorders
* Serviceorders

U kunt een magazijnverzending op twee manieren maken:

* Met pushing wanneer er per order wordt gewerkt. Kies de actie **Magazijnverzending maken** in het brondocument om een magazijnverzending voor het document aan te maken.
* Door pushing, waarbij u de actie **Vrijgeven** in het brondocument gebruikt om vrij te geven aan het magazijn. Een magazijnmedewerker maakt een **magazijnverzending** voor een of meer vrijgegeven brondocumenten. In de volgende procedure wordt beschreven hoe u een magazijnverzending met pushing maakt.

## Artikelen verzenden met een magazijnverzendingsdocument

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Magazijnverzendingen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies **Nieuwe**.  
3. In het veld **Nr.** kiest u de nummerreeks die u wilt gebruiken om een ID voor de zending aan te maken.  
4. Kies in het veld **Vestiging** de vestiging van waaruit u verzendt. 

    Bij het ophalen van brondocumentregels worden bepaalde gegevens van de vestiging naar elke regel gekopieerd.  
5. Als de vestiging opslaglocaties vereist, vult u het veld **Opslaglocatie** in. Afhankelijk van uw configuratie kan [!INCLUDE[prod_short](includes/prod_short.md)]] de opslaglocatie voor u toevoegen. Ga voor meer informatie naar [Zonecodes en opslaglocatiecodes](warehouse-how-ship-items.md#zone-and-bin-codes).  
6. U kunt het brondocument op twee manieren ophalen:

    * Kies de actie **Brondocumenten ophalen**. De pagina **Brondocumenten - Uitgaand** verschijnt. Hier kunt u een of meer brondocumenten selecteren die zijn vrijgegeven naar het magazijn waarvoor verzending vereist is.
    * Kies de actie **Filters om brondoc. op te halen gebruiken**. De pagina **Filters om brondocumenten op te halen** wordt geopend. U kunt het brondocumentfilter selecteren en uitvoeren. Alle vrijgegeven brondocumentregels die aan de filtercriteria voldoen, worden toegevoegd op de pagina **Magazijnverzending**. Meer info op [Procedure: Filters gebruiken om brondocumenten op te halen](warehouse-how-ship-items.md#how-to-use-filters-to-get-source-documents).

    > [!NOTE]
    > Als uw vestiging cross-docking en opslaglocaties voor elke regel gebruikt, kunt u de hoeveelheid artikelen die in de cross-dockopslaglocaties zijn geplaatst controleren. [!INCLUDE [prod_short](includes/prod_short.md)] berekent de aantallen wanneer de velden op de verzending worden bijgewerkt. Als dit de artikelen op de verzending zijn die u voorbereidt, kunt u een pick maken voor alle artikelen en de verzending vervolgens voltooien. Zie voor meer informatie [Artikelen cross-docken](warehouse-how-to-cross-dock-items.md).

7. Maak een magazijnpick. Als de vestiging picken vereist, kunt u op twee manieren pickactiviteiten voor magazijnverzendingen maken:

    * Op een push-manier, waarbij u de actie **Pick maken** gebruikt. Selecteer de te picken regels en geef informatie over de picks op. Bijvoorbeeld de opslaglocaties waaruit u wilt halen en waarin u wilt plaatsen en hoeveel eenheden u wilt verwerken. De opslaglocaties kunnen vooraf worden gedefinieerd voor de magazijnlocatie of resource.
    * Op een pull-manier, waarbij u de actie **Vrijgeven** gebruikt. Gebruik op de pagina **Pickvoorstel** de actie **Magazijndocumenten ophalen** om uw toegewezen picks te krijgen. Wanneer de magazijnpicks volledig zijn geregistreerd, worden de regels in het venster **Pickvoorstel** verwijderd. Meer info op [Picken van artikelen voor magazijnverzending](warehouse-how-to-pick-items-for-warehouse-shipment.md).

> [!TIP]
> Voor een vestiging waarvoor picken niet nodig is, kunt u magazijnverzending afdrukken en gebruiken als picklijst.

8. Geef het te verzenden aantal op.  

    Voor een vestiging die picken vereist, wordt het veld **Te verzenden aantal** automatisch bijgewerkt wanneer het picken wordt geregistreerd. Anders wordt het veld **Te verzenden aantal** ingevuld met de openstaande hoeveelheid voor elke regel, wanneer de magazijnverzendingsregel wordt gemaakt.

    U kunt de hoeveelheid wijzigen, maar u kunt niet meer artikelen verzenden dan het aantal in het veld **Openstaand aantal** op de brondocumentregel of het veld **Gepickt aantal** als picken vereist is.

    Als u de waarde in het veld **Te verzenden aantal** op alle regels wilt instellen op nul, kiest u de actie **Te verzenden aantal verwijderen**. Het op nul zetten van de hoeveelheden is bijvoorbeeld handig als u een streepjescodescanner gebruikt om de te verzenden hoeveelheden bij te werken. Om de beschikbare hoeveelheid voor verzending toe te voegen, kiest u de actie **Te verzenden aantal automatisch invullen**.

9. Boek de verzending.

## Filters gebruiken om brondocumenten op te halen

U kunt vanuit een magazijnverzending de pagina **Filters om brondocumenten op te halen** gebruiken voor het ophalen van de vrijgegeven brondocumentregels die bepalen welke artikelen moeten worden verzonden.

1. Kies in de magazijnverzending de actie **Filters om brondocumenten op te halen gebruiken**. 
2. U stelt een nieuw filter in door een omschrijvende code in te voeren in het veld **Code** en vervolgens de actie **Wijzigen** te kiezen.

    De pagina **Brondocumentfilterkaart - Uitgaand** verschijnt.

3. Gebruik de filters om het type brondocumentregels te definiëren dat moet worden opgehaald. U kunt bijvoorbeeld soorten brondocumenten selecteren, zoals verkoop- of transferorders.
4. Kies **Uitvoeren**.  

Alle vrijgegeven brondocumentregels die voldoen aan de filtercriteria worden toegevoegd op de pagina **Magazijnverzending** waarop u de filters instelt.

U kunt een onbeperkt aantal filtercombinaties maken. Filters worden opgeslagen op de pagina **Filters om brondocumenten op te halen** en zijn beschikbaar als u ze nodig hebt. U kunt de criteria op elk moment wijzigen door de actie **Wijzigen** te kiezen.

## Zone- en opslaglocatiecodes

Als opslaglocaties verplicht zijn op de vestiging, stelt [!INCLUDE [prod_short](includes/prod_short.md)] een zone- en opslaglocatiecode voor op het magazijnverzendingsdocument.

* Voor geavanceerde configuraties waarbij een vestiging gestuurde opslag en pick gebruikt, gebruikt [!INCLUDE [prod_short](includes/prod_short.md)] de opslaglocatie die is opgegeven in het veld **Verzendopslaglocatie** op de **vestigingskaart**. Als er geen **verzendopslaglocatie** is opgegeven, is het veld leeg. Als het artikel en de verzendopslaglocatie niet overeenkomen, laat [!INCLUDE [prod_short](includes/prod_short.md)] de verzendopslaglocatie leeg.
* In andere gevallen gebruikt [!INCLUDE [prod_short](includes/prod_short.md)] altijd eerst de opslaglocatie die is opgegeven in het veld **Verzendopslaglocatie** op de **vestigingskaart**. Als er geen verzendopslaglocatie is opgeven, gebruikt [!INCLUDE [prod_short](includes/prod_short.md)] de opslaglocatie van het brondocument.

## Op-order-assembleren-artikelen in magazijnverzendingen afhandelen

In scenario's voor het assembleren op order, gebruik het veld **Te verzenden aantal** op magazijnverzendingsregels om vast te leggen hoeveel eenheden worden geassembleerd. Het aantal wordt geboekt als assemblageuitvoer wanneer u de magazijnverzending boekt. Voor andere magazijnverzendingsregels is de waarde in het veld **Te verzenden aantal** nul.

Wanneer werknemers (gedeeltelijk) klaar zijn met het assembleren van de hoeveelheid voor op order assembleren, registreren ze de hoeveelheid in het veld **Te verzenden aantal** op de magazijnverzendingsregel. Kies vervolgens de actie **Verzending boeken**. De assemblyuitvoer wordt geboekt, inclusief het materiaalverbruik. Een verkoopverzending voor de hoeveelheid wordt geboekt voor de verkooporder.

Op de assemblageorder kunt u **Magazijnverzendregel op order assembleren** om toegang te krijgen tot de magazijnverzendregel.

Als u de magazijnverzending boekt, worden verschillende velden op de verkooporderregel bijgewerkt om de voortgang in het magazijn weer te geven. De volgende velden worden ook bijgewerkt om weer te geven hoeveel op-order-assembleren-aantallen nog moeten worden geassembleerd en verzonden:

* **AoO-mag. uitstaand aantal**
* **AoO-mag. uitst. aant. (basis)**

> [!NOTE]
> In combinatiescenario's waarbij een deel van de hoeveelheid moet worden geassembleerd en een ander deel uit voorraad moet worden verzonden, worden twee magazijnverzendregels gemaakt. Eén voor het op-order-assembleren-aantal, en één voor het voorraadaantal.
>
> De op-order-assembleren-hoeveelheid wordt afgehandeld zoals beschreven in dit artikel. De voorraadhoeveelheid wordt afgehandeld als een normale magazijnverzendingsregel. Zie voor meer informatie over combinatiescenario's [Op voorraad assembleren of Op order assembleren begrijpen](assembly-assemble-to-order-or-assemble-to-stock.md).

## Zie gerelateerde [Microsoft-training](/training/modules/ship-invoice-items-dynamics-365-business-central/)

## Zie ook

[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Assemblagebeheer](assembly-assemble-items.md)  
[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
