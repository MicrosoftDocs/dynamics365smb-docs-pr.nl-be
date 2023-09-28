---
title: Picken en verzenden in standaardmagazijnconfiguraties
description: Dit artikel beschrijft verschillende niveaus van complexiteit in pick- en verzendprocessen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 02/27/2023
ms.custom: bap-template
ms.search.form: '7335, 7337, 7339, 7340, 7341, 7362, 9008'
---
# <a name="walkthrough-picking-and-shipping-in-basic-warehouse-configurations"></a>Procedure: picken en verzenden in standaardmagazijnconfiguraties

In [!INCLUDE[prod_short](includes/prod_short.md)] gebeurt het ontvangen en opslaan op een van de volgende vier manieren, zoals beschreven in de volgende tabel.

|Methode|Uitgaand proces|Pick vereist|Verzending vereist|Complexiteitsniveau (meer informatie op [Overzicht van magazijnbeheer](design-details-warehouse-management.md))|  
|------|----------------|-----|---------|-------------------------------------------------------------------------------------|  
|A|Picken en verzending vanaf de orderregel boeken|||Geen specifieke magazijnactiviteit.|  
|B|Picken en verzending vanuit een voorraadpickdocument boeken|Ingeschakeld||Basis: Order voor order|  
|H|Picken en verzending vanuit een magazijnverzendingdocument boeken||Ingeschakeld|Basis: Geconsolideerde boeking voor ontvangen/verzenden voor meerdere orders.|  
|D|Picken vanuit een magazijnpickdocument boeken en verzending vanuit een magazijnverzendingdocument boeken|Ingeschakeld|Ingeschakeld|Geavanceerd|  

Lees meer op [Uitgaande magazijnstroom](design-details-outbound-warehouse-flow.md).

De volgende procedure geeft methode B in de vorige tabel weer.  

## <a name="about-this-walkthrough"></a>Informatie over deze procedure

In standaardmagazijnconfiguraties waarbij voor uw vestiging wel een pickverwerking vereist is, maar geen verzendingsverwerking, gebruikt u de pagina **Voorraadpick** om pick- en verzendingsinformatie voor de uitgaande brondocumenten te verzamelen en boeken. Het uitgaand brondocument kan een verkooporder zijn, maar ook een inkoopretourorder, een uitgaande transferorder of een productieorder met daarop de materiaalbehoefte.  

In deze procedure worden de volgende taken gedemonstreerd:  

- Locatie ZUID instellen voor voorraadpicks.  
- Maak een verkooporder voor klant 10000 voor 30 lampen.  
- De verkooporder vrijgeven voor magazijnverwerking.  
- Een voorraadpick maken op basis van een vrijgegeven brondocument.  
- De magazijnverplaatsing van het magazijn vastleggen en tegelijkertijd de verkoopverzending voor de bronverkooporder boeken.  

## <a name="roles"></a>Rollen

In dit overzicht worden taken gedemonstreerd voor de volgende gebruikersrollen:  

- Magazijnbeheerder  
- Orderverwerker  
- Magazijnmedewerker  

<!-- ## Prerequisites

To complete this walkthrough, you will need:  

- For [!INCLUDE[prod_short](includes/prod_short.md)] online, a company based on the **Advanced Evaluation - Complete Sample Data** option in a sandbox environment. For [!INCLUDE[prod_short](includes/prod_short.md)] on-premises, CRONUS installed.
 -->

## <a name="story"></a>Scenario

Ellen, de magazijnmanager bij CRONUS, stelt magazijn ZUID in voor basispickverwerking waarbij magazijnmedewerkers uitgaande orders afzonderlijk verwerken. De orderverwerker Suzanne maakt een verkooporder voor 30 eenheden van het artikel 1928-S om aan klant 10000 vanuit het magazijn ZUID te worden verzonden. De magazijnmedewerker John zorgt ervoor dat de verzending wordt voorbereid en aan de klant geleverd. John beheert alle betrokken taken op de pagina **Voorraadpick**, die automatisch verwijst naar de opslaglocaties waar 1928-S is opgeslagen.

[!INCLUDE[set_up_location.md](includes/set_up_location.md)]

### <a name="setting-up-the-bin-codes"></a>De opslaglocatiecodes instellen

Nadat u de locatie hebt ingesteld, moet u twee opslaglocaties toevoegen.

#### <a name="to-setup-the-bin-codes"></a>De opslaglocatiecodes instellen

1. Selecteer de acties **Opslaglocaties**.
2. Maak twee opslaglocaties met de codes *S-01-0001* en *S-01-0002*.

### <a name="making-yourself-a-warehouse-employee-at-location-south"></a>Uzelf magazijnmedewerker maken op locatie ZUID

Om van deze functionaliteit gebruik te kunnen maken, moet u zichzelf als magazijnmedewerker toevoegen aan de locatie. 

#### <a name="to-make-yourself-a-warehouse-employee"></a>Uzelf magazijnmedewerker maken

  1. Kies het ![Lampje dat de functie Vertel me opent eerste.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Magazijnmedewerkers** in en kies vervolgens de gerelateerde koppeling.  
  2. Kies het veld **Gebruikers-ID** en selecteer uw eigen gebruikersaccount op de pagina **Magazijnmedewerkers**.
  3. Kies ZUID in het veld **Vestiging**.  
  4. Selecteer het veld **Standaard** en selecteer vervolgens de knop **Ja**.  

### <a name="making-item-1928-s-available"></a>Artikel 1928-S beschikbaar maken

Als u artikel 1928-S op locatie ZUID beschikbaar wilt maken, volgt u deze stappen:  

  1. Kies het ![Lampje dat de functie Vertel me opent tweede.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikeldagboeken** in en kies vervolgens de gerelateerde koppeling.  
  2. Open het standaarddagboek en maak twee artikeldagboekregels met de volgende informatie over de werkdatum (23 januari).  

        |Boekingssoort|Artikelnummer|Vestiging|Opslaglocatie|Aantal|  
        |----------------|-----------------|-------------------|--------------|--------------|  
        |Pos. correctie|1928-S|ZUID|S-01-0001|20|  
        |Pos. correctie|1928-S|ZUID|S-01-0002|20|  

        Standaard is het veld **Opslaglocatie** op de verkoopregels verborgen, dus u moet het weergeven. Hiervoor moet u de pagina personaliseren. Zie voor meer informatie [Een pagina personaliseren via de banner Personaliseren](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

  3. Kies **Acties**, vervolgens **Boeking** en kies vervolgens **Boeken**.  
  4. Selecteer de knop **Ja**.  

## <a name="creating-the-sales-order"></a>De verkooporder maken

Verkooporders zijn de meest gebruikte soort uitgaand brondocument.  

### <a name="to-create-the-sales-order"></a>De verkooporder maken

1. Kies het ![Lampje dat de functie Vertel me opent derde.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Maak een verkooporder voor klant 10000 op 23 januari (werkdatum) met de volgende verkooporderregel.  

    |Artikel|Vestiging|Aantal|  
    |----|-------------|--------|  
    |1928-S|ZUID|30|  

     Ga door om het magazijn te informeren dat de verkooporder klaar is voor magazijnverwerking.  

4. Kies de actie **Vrijgeven**.  

    John gaat door met het picken en verzenden van de verkochte artikelen.  

## <a name="picking-and-shipping-items"></a>Artikelen picken en verzenden

Op de pagina **Voorraadpick** kunt u alle uitgaande magazijnactiviteiten voor een bepaald brondocument, zoals een verkooporder, beheren. [!INCLUDE[tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

### <a name="to-pick-and-ship-items"></a>U kunt als volgt artikels picken en verzenden

1. Kies het ![Lampje dat de functie Vertel me opent vierde.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Voorraadpicks** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  

    Zorg ervoor dat het veld **Nee.** op het sneltabblad **Algemeen** is ingevuld.
3. Selecteer het veld **Brondocument** en selecteer vervolgens **Verkooporder**.  
4. Selecteer het veld **Bronnr.**, selecteer de regel voor de verkoop aan klant 10000, en kies vervolgens de knop **OK**.  

    U kunt ook de actie **Brondocument ophalen** kiezen en de verkooporder kiezen.  
5. Kies de actie **Te verwerken aantal autom. invullen**.  

    Of voer in het veld **Te verwerken aantal** respectievelijk 10 en 20 in op de twee voorraadpickregels.  
6. Kies de actie **Boeken**, selecteer **Verzenden** en kies de knop **OK**.  

    Nu zijn de 30 lampen geregistreerd als gepickt uit de opslaglocaties S-01-0001 en S-01-0002, en een negatieve artikelpost is gemaakt om de geboekte verkoopverzending te weerspiegelen.  

## <a name="see-also"></a>Zie ook

[Artikelen picken met voorraadpicks](warehouse-how-to-pick-items-with-inventory-picks.md)  
[Artikelen picken voor magazijnverzending](warehouse-how-to-pick-items-for-warehouse-shipment.md)  
[Standaardmagazijnen met bewerkingsgebieden instellen](warehouse-how-to-set-up-basic-warehouses-with-operations-areas.md)  
[Picken voor productie of assemblage](warehouse-how-to-pick-for-production.md)  
[Artikelen ad hoc verplaatsen in standaardmagazijnconfiguraties](warehouse-how-to-move-items-ad-hoc-in-basic-warehousing.md)  
[Ontwerpdetails: Uitgaande magazijnstroom](design-details-outbound-warehouse-flow.md)  
[Procedures voor bedrijfsprocessen](walkthrough-business-process-walkthroughs.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
