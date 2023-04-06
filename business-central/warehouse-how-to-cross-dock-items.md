---
title: Artikelen cross-docken
description: De cross-dockfunctionaliteit is beschikbaar als u voor de vestiging hebt ingesteld dat magazijnontvangst- en magazijnopslagverwerking is vereist.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '15, 5703, 7302, 7332, 5768'
ms.date: 04/01/2021
ms.author: edupont
---
# Artikelen cross-docken

Cross-dockartikelen zijn artikelen die u ontvangt en verzendt zonder ze op te slaan. De opslag- en pickprocessen vereisen een beperkte afhandeling van artikelen. Het cross-docken van artikelen is mogelijk voor verzendingen en productieorders.

## Cross-dockopslaglocaties en -zones

Als u opslaglocaties gebruikt, stelt u ten minste één cross-dockopslaglocatie in en specificeert u de opslaglocatie in het veld **Cross-dockopslaglocatie** op uw vestigingen. Stel een cross-dockzone in als u met gestuurde opslag en pick werkt.

Wanneer u een verzending voorbereidt of artikelen voor de productie pickt, wordt het artikel automatisch uit een cross-dockopslaglocatie gepickt, mits u met opslaglocaties werkt. Pas daarna komen andere opslaglocaties in aanmerking voor de pick. Controleer in de cross-dockgebied of de benodigde artikelen beschikbaar zijn. Vervolgens kunt u de artikelen uit de gebruikelijke opslaggebied picken.  

Als u cross-dockaantallen hebt berekend, worden voor de resultaten automatisch opslagregels gemaakt voor de cross-docklocatie wanneer u de ontvangst boekt. De overige opslagregels worden op de gebruikelijke wijze gemaakt.  

## Geselecteerde regels cross-docken voor een ontvangst

<!--If a receipt contains items that you want to store, that is, items that you are not cross-docking, you must register a put-away for those items.-->

Als u de cross-dockartikelen direct wilt boeken zodat u ze kunt picken, moet u ook een opslag registreren voor de overige artikelen op de ontvangstregel die moeten worden opgeslagen. Als slechts een gedeelte van de artikelen op een ontvangstregel bestemd is voor cross-docking, is het van belang dat u de overige artikelen zo snel mogelijk opslaat. Mogelijk is uw magazijnbeleid erop gericht om ontvangstregels waar mogelijk volledig te cross-docken.

Verwijder in de opslaginstructie de instructieregels Nemen en Plaatsen voor elke ontvangstregel voor de artikelen die moeten worden opgeslagen. U kunt de instructieregels later opnieuw maken als opslagregels uit het opslagvoorstel of de geboekte ontvangst. Nadat u de instructieregels hebt verwijderd, kunt u de regels voor cross-dockartikelen opslaan en registreren.  

## Informatie over het opslagvoorstel

Als u de schakelaar **Opslagvoorstel gebruiken** op de pagina voor de vestigingskaart hebt aangezet en de ontvangst met berekende cross-docks hebt geboekt, worden alle ontvangstregels doorgestuurd naar het voorstel. De cross-dockgegevens gaan dan verloren en kunnen niet opnieuw worden gemaakt. Voor het gebruik van de cross-dockfunctie is het daarom beter dat u de regels naar het opslagvoorstel doorstuurt door opslaginstructies te verwijderen en de automatische doorgavefunctie van **Opslagvoorstel gebruiken** uit te schakelen.  

Als u de magazijnontvangst boekt en de schakelaar **Opslagvoorstel gebruiken** uitstaat, worden de cross-dockartikelen afzonderlijke regels op de opslaginstructie. Het veld **Cross-dockinformatie** op elke opslagregel geeft aan of de regel het volgende bevat:

* Cross-dockartikelen.
* Alle artikelen van een ontvangst moeten worden opgeslagen.
* Sommige artikelen van een ontvangst moeten worden opgeslagen en andere moeten worden gecross-dockt.

Medewerkers kunnen gemakkelijk begrijpen waarom niet de volledige hoeveelheid wordt opgeslagen.  

[!INCLUDE [prod_short](includes/prod_short.md)] houdt geen afzonderlijke records bij voor cross-dockartikelen. In plaats daarvan worden ze als gewone opslaginstructies vastgelegd.  

## U kunt als volgt het magazijn instellen voor cross-docking  

1. Als u met opslaglocaties werkt, moet u ten minste één cross-dockopslaglocatie instellen. Stel een cross-dockzone in als u met gestuurde opslag en pick werkt.  

    Bij een cross-dockopslaglocatie is het veld **Cross-dockopslaglocatie** ingeschakeld en zijn de opslaglocatietypen **Ontvangen** en **Picken** geselecteerd. Zie [Opslaglocaties maken](warehouse-how-to-create-individual-bins.md) en [Opslaglocatiesoorten instellen](warehouse-how-to-set-up-bin-types.md).  

    Als u zones gebruikt, maakt u een zone voor de cross-dockopslaglocaties en selecteert u het veld **Cross-dockopslaglocatiezone**. Zie voor meer informatie [Gebruik van opslaglocaties voor locaties instellen](warehouse-how-to-set-up-locations-to-use-bins.md).  

2. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Locatie** in en kies vervolgens de gerelateerde koppeling.  
3. Op de pagina **Vestiging** selecteert u de vestiging waar u het magazijn voor cross-docken wilt instellen. Vervolgens kiest u de actie **Bewerken**.  
4. Zet op het sneltabblad **Magazijn** de schakelaar **Cross-docken gebruiken** aan en vul in het veld **Cross-dockvervaldatum berekenen** de periode in waarin er moet worden gezocht naar cross-dockmogelijkheden.

    De optie **Cross-docken** gebruiken is alleen beschikbaar als u de velden **Ontvangst vereist**, **Verzending vereist**, **Pick vereist** en **Opslag vereist** selecteert.  

5.  Als u met opslaglocaties werkt, vult u in het veld **Cross-dockopslaglocatie** op het sneltabblad **Opslaglocaties** de code in van de opslaglocatie die u als standaardcross-dockopslaglocatie wilt gebruiken.  
6.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **SKU** in en selecteer vervolgens de gerelateerde koppeling.  
7.  Selecteer alle items of SKU's die in aanmerking komen voor cross-docking en kies de actie **Bewerken**.
8. Schakel op de pagina **SKU** het selectievakje **Cross-docken gebruiken** in.  

> [!NOTE]  
>  Cross-docken is alleen mogelijk als voor de vestiging magazijnontvangst- en magazijnopslagverwerking is vereist.  

## U kunt als volgt artikelen cross-docken zonder de mogelijkheden te bekijken  
1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Magazijnontvangsten** in en kies vervolgens de gerelateerde koppeling.  
2.  Maak een magazijnontvangst voor een artikel dat is aangekomen en dat misschien kan worden gecross-dockt. Zie [Artikelen ontvangen](warehouse-how-receive-items.md) voor meer informatie.  
3.  Vul het veld **Te ontvangen aantal** in en kies de actie **Cross-dock berekenen**.  

    Er wordt gezocht naar uitgaande brondocumenten voor het aanvragen van de artikelen die volgens de planning het magazijn binnen de datumformuleperiode verlaten.  [!INCLUDE[prod_short](includes/prod_short.md)] berekent aantallen, zodat u zoveel mogelijk kunt cross-docken en opslag van artikelen kunt vermijden, zonder dat er te veel artikelen in het cross-dockgebied worden opgestapeld. De waarde in het veld **Te cross-docken aantal** is dus de som van alle uitgaande regels waarop het artikel binnen de voorziene periode voorkomt, min het aantal artikelen dat al in het cross-dockgebied is geplaatst, of deze waarde is gelijk aan de waarde in het veld **Te ontvangen aantal** op de ontvangstregel, afhankelijk van wat de kleinste waarde is. U kunt niet meer cross-docken dan u hebt ontvangen.  

4.  Als u het voorgestelde aantal wilt cross-docken, boekt u de ontvangst. U kunt het te cross-docken aantal ook verhogen of verlagen en de ontvangst vervolgens boeken.  

    De waarden voor cross-docking verschijnen nu als regels in de opslaginstructie, als u tenminste het vakje **Opslagvoorstel gebruiken** hebt uitgeschakeld. De aantallen die niet in aanmerking komen voor cross-docking, worden ook als regels weergegeven op de opslaginstructie.  

    Als u met opslaglocaties werkt, worden de cross-dockartikelen toegewezen aan de standaardcross-dockopslaglocatie, die is gedefinieerd op de vestigingskaart.  

5.  Verwijder de **Nemen** en **Plaatsen**-regels voor artikelen die niet in aanmerking komen voor cross-docking.  
6.  Druk de opslaginstructie voor de resterende regels af en plaats de ontvangen aantallen die u wilt opslaan in de betreffende opslaglocaties of betreffende ruimte in het magazijn. Plaats de cross-dockartikelen in de ruimte of de opslaglocatie die daartoe is aangewezen volgens het magazijnbeleid. Soms kan het magazijnbeleid bepalen dat de artikelen op de plaats van ontvangst moeten blijven.  
7.  Klik op de actie **Registreren** om de artikelen na cross-docking als opgeslagen en pickbaar te registreren.  

## Artikelen cross-docken na de mogelijkheden bekeken te hebben  
1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Magazijnontvangsten** in en kies vervolgens de gerelateerde koppeling.  
2.  Maak een magazijnontvangst voor een artikel dat is aangekomen en dat misschien kan worden gecross-dockt. Zie [Artikelen ontvangen](warehouse-how-receive-items.md) voor meer informatie.  

    U wilt de ontvangst mogelijk pas boeken nadat u hebt weergegeven op welke regels in de brondocumenten de artikelen voorkomen.  
3.  Kies de actie **Cross-dock berekenen**.  

    Op de pagina **Cross-dockmogelijkheden** ziet u de belangrijkste gegevens over de regels waarin het artikel wordt opgevraagd, zoals het soort document, het gevraagde aantal en de vervaldatum. Aan de hand van deze gegevens kunt u mogelijk bepalen hoeveel u wilt cross-docken, op welke plek in het cross-dockgebied u de artikelen wilt plaatsen of hoe u de artikelen wilt groeperen.  

4.  Kies de actie **Te cross-docken aantal autom. invullen** om weer te geven hoe de aantallen op de ontvangstregels worden berekend. Wanneer u het aantal artikelen in het veld **Te cross-docken aantal** op afzonderlijke regels wijzigt, wordt de berekening bijgewerkt terwijl u wijzigingen aanbrengt. Dit betekent niet dat de verzendingsorder of productieorder de artikelen die voor cross-docken werden voorgesteld, werkelijk ontvangt. Deze bewerkingen zijn enkel als test. Het resultaat kan echter erg informatief zijn, zeker als er meer dan één eenheid bij betrokken is.  
5.  Plaats de cursor op de regel en kies de actie **Reserveren** als u een aantal artikelen voor een bepaalde orderregel wilt reserveren. U kunt nu op de pagina **Reservering** een beschikbaar aantal van het artikel reserveren voor deze specifieke order. Deze reservering is net als elke andere reservering en heeft geen hogere prioriteit omdat deze is gemaakt in verband met cross-docken. Zie [Artikelen reserveren](inventory-how-to-reserve-items.md) voor meer informatie.   
6.  Als u de herberekening of reservering hebt uitgevoerd, klikt u op **OK** om de herziene berekening naar het veld **Cross-dockaantal** op de ontvangstregel te kopiëren. Klik anders op **Annuleren** om terug te gaan naar de magazijnontvangst en de cross-dock desgewenst opnieuw te berekenen.  
7.  U kunt vervolgens de ontvangst boeken en doorgaan in de opslaginstructie, zoals is beschreven in stap 3 tot en met 7 in de sectie U kunt als volgt artikelen cross-docken zonder de mogelijkheden te bekijken.  

> [!NOTE]  
>  In de magazijnopslag kunt u desgewenst verdere wijzigingen aanbrengen in de aantallen die u wilt opslaan of cross-docken. U zou bijvoorbeeld een extra aantal kunnen cross-docken om de registratie te bespoedigen.  

## Cross-dockartikelen bekijken in verzendingen of pickvoorstellen  
Als u met opslaglocaties werkt, kunt u, telkens wanneer u een verzending of pickvoorstel opent, een bijgewerkte berekening weergeven van de artikelaantallen in de cross-dockopslaglocaties. Deze informatie is vooral van belang als u aan het wachten bent op de binnenkomst van een artikel. Zodra u ziet dat het artikel beschikbaar is op de opslaglocatie voor cross-docking, kunt u snel een pick maken voor alle artikelen in de verzending. In het pickvoorstel kunt u de regels desgewenst wijzigen en daarna een pick maken.  

Als u te verzenden artikelen wilt picken, moet u eerst zoeken in de cross-dockruimte. Als u tijdens het ontvangstproces hebt gecontroleerd uit welke brondocumenten de cross-docking voortkomt, kunt u beter bepalen of het artikel zich al dan niet op de cross-dockplaats bevindt.  

Na de vrijgave van een productieorder zijn de regels beschikbaar in het pickvoorstel en kunt u in het veld **Aantal in cross-dockopslagloc.** zien of de artikelen zijn gearriveerd en in de cross-dockopslaglocaties zijn geplaatst. Als u een pickinstructie maakt, wordt automatisch voorgesteld dat u eerst de cross-dockartikelen pickt. De opslaglocaties met voorraad worden daarna pas doorzocht.  

Als u geen opslaglocaties gebruikt, is het verstandig de cross-dockruimte regelmatig te controleren. Anders bent u afhankelijk van de berichten over de ontvangst van artikelen voor productieorders.  

## Zie ook  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)     
[Assemblagebeheer](assembly-assemble-items.md)    
[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]