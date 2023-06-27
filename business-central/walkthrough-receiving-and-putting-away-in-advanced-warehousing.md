---
title: Ontvangen en opslaan bij geavanceerd magazijnbeheer
description: 'De inkomende processen voor ontvangst en opslag kunnen op vier manieren worden uitgevoerd met verschillende functionaliteiten, afhankelijk van het complexiteitsniveau van het magazijn.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/24/2021
ms.author: edupont
---
# <a name="walkthrough-receiving-and-putting-away-in-advanced-warehouse-configurations"></a>Procedure: Ontvangen en opslaan in geavanceerde magazijnconfiguraties

<!-- [!INCLUDE[complete_sample_data](includes/complete_sample_data.md)]   -->

In [!INCLUDE[prod_short](includes/prod_short.md)] gebeurt het ontvangen en wegzetten op een van de volgende vier manieren, zoals beschreven in de volgende tabel.

|Methode|Inkomend proces|Ontvangst vereist|Opslag vereist|Complexiteitsniveau (meer informatie op [Overzicht van magazijnbeheer](design-details-warehouse-management.md))|  
|------------|---------------------|--------------|----------------|------------|  
|A|Ontvangst en opslag van de orderregel boeken|||Geen specifieke magazijnactiviteit.|  
|B|Ontvangst en opslag van een voorraadopslagdocument boeken||Ingeschakeld|Basis: Order voor order|  
|H|Ontvangst en opslag van een magazijnontvangstdocument boeken|Ingeschakeld||Basis: Geconsolideerde boeking voor ontvangen/verzenden voor meerdere orders.|  
|D|Ontvangst van een magazijnontvangstdocument en opslag van een magazijnopslagdocument boeken|Ingeschakeld|Ingeschakeld|Geavanceerd|  

Lees meer op [Inkomende magazijnstroom](design-details-inbound-warehouse-flow.md).

De volgende procedure geeft methode D in de vorige tabel weer.  

## <a name="about-this-walkthrough"></a>Informatie over deze procedure

In geavanceerde magazijnconfiguraties waarbij voor uw vestiging is ingesteld dat naast de opslag ook de ontvangst moet worden verwerkt, gebruikt u de pagina **Magazijnontvangst** om de ontvangst van artikelen op meerdere inkomende orders vast te leggen en te boeken. Wanneer de magazijnontvangst wordt geboekt, worden een of meer magazijnopslagdocumenten gemaakt om magazijnmedewerkers te instrueren de ontvangen artikelen op aangewezen locaties te plaatsen, op basis van opslaglocatie-instellingen of in verschillende opslaglocaties. De specifieke plaatsing van de artikelen wordt geregistreerd wanneer de magazijnopslag wordt geregistreerd. Het inkomende brondocument kan een inkooporder zijn, maar ook een verkoopretourorder, een inkomende transferorder, assemblageorder of productieorder met output die kan worden opgeslagen. Als de ontvangst van een inkomende order is gemaakt, kan meer dan een inkomend brondocument worden opgehaald voor de ontvangst. Met deze methode kunt u diverse artikelen die worden afgeleverd van verschillende aankomend inkomende orders, registreren met één ontvangst.  

In deze procedure worden de volgende taken gedemonstreerd:  

-   Vestiging WIT instellen voor het ontvangen en opslaan.  
-   Twee inkooporders voor volledige magazijnverwerking maken en vrijgeven.  
-   Een magazijnontvangstdocument voor meerdere inkooporderregels van specifieke leveranciers maken en boeken.  
-   Een magazijnopslag voor de ontvangen artikelen registreren.  

## <a name="roles"></a>Rollen

In dit overzicht worden taken gedemonstreerd voor de volgende gebruikersrollen:  

-   Magazijnbeheerder  
-   Inkoper  
-   Ontvangend personeel  
-   Magazijnmedewerker  

## <a name="prerequisites"></a>Vereisten

U moet het volgende doen om deze procedure uit te voeren:  

-   CRONUS geïnstalleerd.  
-   U maakt van uzelf een magazijnwerknemer bij vestiging WIT door de volgende stappen uit te voeren:  

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Magazijnmedewerkers** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies het veld **Gebruikers-ID** en selecteer uw eigen gebruikersaccount op de pagina **Gebruikers**.  
3.  Voer WIT in het veld **Vestiging** in.  
4.  Selecteer het veld **Standaard**.  

## <a name="story"></a>Scenario

Ellen, de magazijnmanager bij CRONUS International Ltd., maakt twee inkooporders voor accessoires van leverancier 10000 en 20000 om te worden afgeleverd bij magazijn WIT. Als de leveringen in het magazijn aankomen, gebruikt Sammy, die verantwoordelijk is voor de ontvangst van artikelen van leveranciers 10000 en 20000, een filter om ontvangstregels te maken voor inkooporders van de twee leveranciers. Sammy boekt de artikelen als ontvangen in voorraad in een magazijnontvangst en maakt de artikelen beschikbaar voor verkoop of andere vraag. De magazijnmedewerker Johanna neemt de artikelen uit de opslaglocatie en zet ze weg. Hij zet alle eenheden in hun standaardopslaglocaties, behalve 40 van 100 ontvangen scharnieren die hij opslaat in de montageafdeling door de opslagregel te splitsen. Wanneer John de opslag registreert, wordt de inhoud van de opslaglocatie bijgewerkt en worden de artikelen beschikbaar gemaakt om vanuit het magazijn te worden gepickt.  

## <a name="reviewing-the-white-location-setup"></a>Instellingen van de vestiging WIT controleren

De instellingen van de pagina **Vestiging** definiëren de magazijnstromen van het bedrijf.  

### <a name="to-review-the-location-setup"></a>De vestigingsinstellingen controleren

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Locaties** in en kies vervolgens de gerelateerde koppeling.  
2.  Open de vestigingskaart WIT.  
3.  Controleer op het sneltabblad **Magazijn** of het selectievakje **Gestuurde opslag en pick** is ingeschakeld.  

    Dit betekent dat de vestiging wordt ingesteld voor het hoogste complexiteitniveau, wat wordt aangegeven door het feit dat alle selectievakjes voor magazijnverwerking op het sneltabblad zijn ingeschakeld.  

4.  Controleer op het sneltabblad **Opslaglocaties** of de opslaglocaties in de velden **Ontvangstopslaglocatie** en **Verzendopslaglocatie** zijn opgegeven.  

Dit betekent dat als u een magazijnontvangst maakt, deze opslaglocatiecode standaard naar de koptekst van het magazijnontvangstdocument wordt gekopieerd en naar de regels van de resulterende magazijnopslag.  

## <a name="creating-the-purchase-orders"></a>De inkooporders maken

Inkooporders zijn de meest gebruikte soort inkomend brondocument.  

### <a name="to-create-the-purchase-orders"></a>De inkooporders maken

1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkooporders** in en kies vervolgens de gerelateerde koppeling  
2.  Kies de actie **Nieuw**.  
3.  Maak een inkooporder voor leverancier 10000 op 23 januari (werkdatum) met de volgende inkooporderregels.  

    |Artikel|Vestiging|Aantal|  
    |----------|-------------------|--------------|  
    |70200|WIT|100 stuks|  
    |70201|WIT|50 stuks|  

    Ga door om het magazijn te informeren dat de inkooporder klaar is voor de magazijnverwerking wanneer de bezorging aankomt.  

4.  Kies de actie **Vrijgeven**. De status verandert van Open in Vrijgegeven.

    U kunt nu doorgaan om de tweede inkooporder te genereren.  

5.  Kies de actie **Nieuw**.  
6.  Maak een inkooporder voor leverancier 20000 op 23 januari (werkdatum) met de volgende inkooporderregels.  

    |Artikel|Vestiging|Aantal|  
    |----------|-------------------|--------------|  
    |70100|WIT|10 CAN|  
    |70101|WIT|12 CAN|  

    Kies de actie **Vrijgeven**. De status verandert van Open in Vrijgegeven.

    De leveringen van artikelen van leveranciers 10000 en 20000 zijn aangekomen in magazijn WIT en Sammy begint inkoopontvangsten te verwerken.  

## <a name="receiving-the-items"></a>De artikelen ontvangen

Op de pagina **Magazijnontvangst** kunt u meerdere inkomende orders beheren voor brondocumenten, zoals een inkooporder.  

### <a name="to-receive-the-items"></a>De artikelen ontvangen
1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Magazijnontvangsten** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Nieuw**.  
3.  Voer WIT in het veld **Vestiging** in.  
4.  Selecteer **Acties** dan **Functies**, kies dan de actie **Filters om brondoc. op te halen gebruiken**.  
5.  Voer **ACCESSORY** in het veld **Code** in.  
6.  Typ in het veld **Omschrijving** de tekst **Leveranciers 10000 en 20000**.  
7.  Kies de actie **Wijzigen**.  
8.  Voer op het sneltabblad **Inkoop** in het veld **Orderleveranciernr.-filter** de waarde **10000&#124;20000** in.  
9. Kies de actie **Uitvoeren**. De magazijnontvangst wordt gevuld met vier regels die inkooporderregels voor de opgegeven leveranciers vertegenwoordigen. Het veld **Te ontvangen aantal** is ingevuld omdat u niet het selectievakje **Te verwerken aantal niet opvullen** op de pagina **Filters om brondoc. op te halen** hebt ingeschakeld.  
10. Als u een filter wilt gebruiken zoals eerder in dit gedeelte beschreven, kunt u ook de actie **Brondocument ophalen** kiezen en vervolgens inkooporders van de leverancier in kwestie selecteren.  
11. Kies **Boeking** en vervolgens de actie **Ontvangst boeken** en kies vervolgens de knop **Ja**.  

    Er worden positieve artikelposten gemaakt die de geboekte inkoopontvangsten van leveranciers 10000 en 20000 aangeven, en de artikelen zijn gereed om in het magazijn van de ontvangende opslaglocatie te worden opgeslagen.  

## <a name="putting-the-items-away"></a>Artikelen opslaan

Op de pagina **Magazijnopslag** kunt u opslagactiviteiten beheren voor een specifiek magazijnontvangstdocument dat van toepassing is op meerdere brondocumenten. Net als alle magazijnactiviteitsdocumenten wordt elk artikel in de magazijnopslag weergegeven door een Nemen-regel en een Plaatsen-regel. In de volgende procedure is de opslaglocatie op de Nemen-regels de standaardopslaglocatie op vestiging WIT, W-08-0001.  


### <a name="to-put-the-items-away"></a>De artikelen opslaan
1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Opslag** in en kies vervolgens de gerelateerde koppeling.  
2.  Selecteer het enige magazijnopslagdocument in de lijst en kies vervolgens de actie **Bewerken**.  

    Het magazijnopslagdocument wordt geopend met in totaal acht Nemen- of Plaatsen-regels voor de vier inkooporderregels.

    De magazijnmedewerker wordt verteld dat er 40 scharnieren op de montageafdeling nodig zijn. Hij splitst de ene Plaatsen-regel om een tweede Plaatsen-regel voor opslaglocatie W-02-0001 op te geven op de montageafdeling waar de magazijnmedewerker dat een deel van de ontvangen scharnieren plaatst.  

3.  Selecteer de tweede regel op de pagina **Magazijnopslag**, de Plaatsen-regel, voor artikel 70200.  
4.  Wijzig de waarde in het veld **Te verwerken aantal** van 100 in 60.  
5.  Kies op het sneltabblad **Regels** de optie **Functies** en kies vervolgens **Regel splitsen**. Er wordt een nieuwe regel ingevoegd voor artikel 70200 met 40 in veld **Te verwerken aantal**.  
6.  Voer W-02-0001 in het veld **Opslaglocatie** in. Het veld **Zonecode** wordt automatisch ingevuld.  

    Standaard is het veld **Zone** op de verkoopregels verborgen, dus u moet het weergeven. Hiervoor moet u de pagina personaliseren. Zie voor meer informatie [Een pagina personaliseren via de banner Personaliseren](ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner).

    U kunt nu doorgaan om de opslag te registreren.  

7.  Kies de actie **Opslag registreren** en kies vervolgens de knop **Ja**.  

    De ontvangen accessoires worden nu opgeslagen in de standaardopslaglocaties van de artikelen, en 40 scharnieren worden geplaatst in de montageafdeling. De ontvangen artikelen zijn nu beschikbaar voor picken naar interne vraag, zoals assemblageorders, of naar externe de vraag, zoals verkoopverzendingen.  

## <a name="see-also"></a>Zie ook
 [Artikelen opslaan met magazijnopslag](warehouse-how-to-put-items-away-with-warehouse-put-aways.md)   
 [Artikelen verplaatsen in geavanceerde magazijnconfiguraties](warehouse-how-to-move-items-in-advanced-warehousing.md)   
 [Ontwerpdetails: Inkomende magazijnstroom](design-details-inbound-warehouse-flow.md)   
 <!-- [Walkthrough: Receiving and Putting Away in Basic Warehouse Configurations](walkthrough-receiving-and-putting-away-in-basic-warehousing.md)    -->
 [Procedures voor bedrijfsprocessen](walkthrough-business-process-walkthroughs.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
