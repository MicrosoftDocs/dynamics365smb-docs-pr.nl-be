---
title: Voorraad tellen, corrigeren en herindelen| Microsoft Docs
description: Beschrijft hoe u inventarisaties uitvoert, negatieve of positieve correcties uitvoert, en gegevens wijzigt, zoals locatie of lotnummer, in artikelposten of magazijnposten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: adjustment, negative, positive, increase, decrease
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 76a531f7072b1d4082af3c1e82bb78dc2d44ddc3
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="count-adjust-and-reclassify-inventory"></a>Voorraad tellen, corrigeren en herindelen
Minstens eenmaal per jaar moet u inventariseren, dat wil zeggen, alle artikelen tellen die op voorraad zijn, om te controleren of de geregistreerde hoeveelheid in de database gelijk is aan de werkelijke hoeveelheid in de magazijnen. Wanneer de werkelijke hoeveelheid niet bekend is, moet dit in het grootboek worden geboekt in het kader van een voorraadwaardering aan het einde van een boekingsperiode.

Hoewel alle artikelen in het magazijn minimaal een keer per jaar worden geteld, wilt u sommige artikelen misschien vaker tellen omdat ze waardevoller zijn of snel worden omgezet en belangrijk zijn voor het bedrijf. U kunt tellingsperioden instellen en toewijzen aan magazijnartikelen. Voor dit doel kunt u speciale telperioden aan die artikelen toewijzen. Zie voor meer informatie de sectie 'Clustertellingen uitvoeren'.

Als u vastgelegde voorraadhoeveelheden moet aanpassen, in verband met de inventarisatie of om andere redenen, kunt u een artikeldagboek gebruiken om het voorraadgrootboek direct te wijzigen zonder zakelijke transacties te hoeven boeken. U kunt ook een correctie voor één artikel uitvoeren op de artikelkaart.

Als u kenmerken van artikelposten wilt wijzigen, kunt u daarvoor het artikelherindelingsdagboek gebruiken. Typische kenmerken voor herindeling zijn dimensies en verkoopcampagnecodes, maar u kunt ook systeemtransfers uitvoeren door opslaglocatie- en vestigingscodes te herindelen. Speciale stappen zijn van toepassing wanneer u serie- of lotnummers en hun vervaldatums wilt herindelen. Zie voor meer informatie [Werken met serie- en lotnummers](inventory-how-work-item-tracking.md).

> [!NOTE]
> In geavanceerde magazijnconfiguraties worden artikelen in opslaglocaties geregistreerd als magazijnposten, niet als artikelposten. Daarom voert u inventarisaties, aanpassingen en herindelingen uit in speciale magazijndagboeken die opslaglocaties ondersteunen. Vervolgens gebruikt u speciale functies om de nieuwe of gewijzigde magazijnposten met de gerelateerde artikelposten te synchroniseren om de wijzigingen in voorraadaantallen en waarden weer te geven. Dit wordt hieronder in bepaalde procedures beschreven, waar relevant.

## <a name="to-perform-a-physical-inventory"></a>Een inventarisatie uitvoeren
Aan het einde van het boekjaar, zo niet vaker, moet u de inventaris opmaken (de beschikbare artikelen tellen) om te controleren of het geregistreerde aantal gelijk is aan het aantal in voorraad. Als er verschillen zijn, moet u deze naar de artikelrekeningen boeken voordat u de voorraadwaardering uitvoert.

Afgezien van de fysieke tellingstaak omvat het volledige proces de volgende drie taken:

- De verwachte voorraad berekenen.
- Het rapport dat bij het tellen moet worden gebruikt afdrukken.
- Invoeren en boeken van de werkelijk getelde voorraad.

U kunt de inventarisatie op een van de volgende manieren uitvoeren, afhankelijk van de magazijninstellingen. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).  

-   Als u in de vestiging niet met gestuurde opslag en pick werkt (standaardmagazijnconfiguratie), gebruikt u het venster **Inventarisatiedagboek** in het menu **Voorraad**. De procedure is grotendeels hetzelfde als die van een inventarisatie zonder periodieke tellingen.  
-   Als uw locatie gestuurde opslag en pick gebruikt (geavanceerde magazijnconfiguratie), gebruikt u eerst het venster **Mag. inventarisatiedagboek** en vervolgens het venster **Artikeldagboek** voor het uitvoeren van de functie **Magazijnherwaardering berekenen**.

### <a name="to-calculate-the-expected-inventory-in-basic-warehouse-configurations"></a>De verwachte voorraad in standaardmagazijnconfiguraties berekenen
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inventarisatiedagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Voorraad berekenen**.
3. Specificeer in het venster **Voorraad berekenen** de voorwaarden die moeten worden gebruikt om de dagboekregels te maken, zoals of artikelen die niet op voorraad zijn al dan niet moeten worden opgenomen.
4. Stel alleen filters in als u de voorraad voor bepaalde artikelen, opslaglocaties, vestigingen of dimensies wilt berekenen.
5. Kies de knop **Ok**.

> [!NOTE]  
>   De artikelposten worden verwerkt volgens de informatie die u hebt opgegeven en de regels in het inventarisatiedagboek worden gemaakt. U ziet dat het veld **Aantal (inventaris)** automatisch wordt ingevuld met hetzelfde aantal als het veld **Aantal (Berekend)**. Met deze functie hoeft u de getelde voorraad niet handmatig in te voeren voor artikelen die overeenkomen met de berekende hoeveelheid. Als het aantal echter afwijkt van wat is ingevoerd in het veld **aantal (Berekend)**, moet u deze overschrijven met de hoeveelheid die daadwerkelijk is geteld.

### <a name="to-calculate-the-expected-inventory-in-advanced-warehouse-configurations"></a>De verwachte voorraad in geavanceerde magazijnconfiguraties berekenen
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikeldagboek** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Magazijnherwaardering berekenen**.  
3.  Vul in het opvraagvenster voor de batchtaak de nummers van de artikelen in die u wilt tellen en uw locatie.
4. Kies de knop **OK** en boek eventuele aanpassingen.

    Indien u dit niet doet voordat u de magazijninventarisatie uitvoert, zullen de resultaten die u in het tweede deel van het proces naar het voorraaddagboek en naar de artikelposten boekt bestaan uit de inventarisatieresultaten en andere magazijnaanpassingen voor de artikelen die zijn geteld.  
5.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Mag. inventarisatiedagboek** in en kies vervolgens de gerelateerde koppeling.  
6. Kies de actie **Voorraad berekenen**. Het aanvraagvenster voor batchverwerking **Voorraad berekenen** verschijnt.  
7.  Stel de gewenste filters in om het aantal artikelen dat wordt geteld in het dagboek te beperken en klik vervolgens op **OK**.

    Er wordt een regel gemaakt voor elke opslaglocatie die voldoet aan de filtercriteria. Op dit moment kunt u nog enkele regels verwijderen, maar als u het resultaat wilt boeken als inventarisatie, moet u alle opslaglocaties opnemen in de artikeltelling.  

     Als u alleen tijd hebt om het artikel in sommige opslaglocaties te tellen, kunt u alsnog discrepanties tegenkomen die u kunt registreren en op een later tijdstip in het artikeldagboek boeken met de functie **Magazijncorrectie** berekenen.  
8.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Mag. - Inventarisatielijst** in en kies vervolgens de gerelateerde koppeling.  
9.  Open de rapportaanvraagpagina en druk de lijsten af waarin de werknemers het getelde aantal artikelen voor elke opslaglocatie moeten vastleggen.  
10. Wanneer de artikelen zijn geteld, geeft u de aantallen op in het veld **Aantal (Inventarisatie)** in het inventarisatiedagboek van het magazijn.  

    > [!NOTE]  
    >  In het magazijninventarisatiedagboek wordt het veld **Aantal (Berekend)** automatisch gevuld op basis van gegevens van magazijn-opslaglocaties en worden deze hoeveelheden gekopieerd naar het veld **Aantal (Fysiek)** op elke regel. Indien het aantal dat de magazijnwerknemer geteld heeft, afwijkt van wat het programma heeft ingevoerd in het veld Aantal (Fysiek), moet u het werkelijk getelde aantal invoeren.  

11. Wanneer u alle getelde aantallen hebt ingevoerd, kiest u de actie **Registreren**.  

    Wanneer u het dagboek registreert, worden er twee magazijnposten gemaakt in het magazijnregister voor elke getelde en geregistreerde regel.  

    -   Als de berekende aantallen niet overeenkomen met de getelde aantallen, wordt een negatief of positief aantal geregistreerd voor de opslaglocatie. Vervolgens wordt een tegengesteld aantal geboekt naar de correctieopslaglocatie van de vestiging.  
    -   Als het berekende aantal wel overeenkomt met het getelde aantal, wordt een post met de waarde 0 geregistreerd voor zowel de opslaglocatie als de correctieopslaglocatie. De post bestaat uit de record dat een inventarisatie heeft plaatsgevonden op de registratiedatum en dat er geen verschillen zijn aangetroffen voor het artikel.  

Wanneer u de magazijninventarisatie registreert, boekt u niet naar de artikelposten, de inventarisatieposten of de waardeposten, maar de gegevens zijn er voor het geval deze nodig zijn. Indien u echter nauwkeurige administratie bij wilt houden van wat er in het magazijn gebeurt en u alle opslaglocaties waar de artikelen zijn geregistreerd zou tellen, moet u onmiddellijk de magazijnresultaten als een voorraadinventarisatie boeken. Zie de sectie De werkelijk getelde voorraad in standaardmagazijnconfiguraties invoeren en boeken voor meer informatie.

### <a name="to-print-the-report-to-be-used-when-counting"></a>Het rapport afdrukken dat bij het tellen moet worden gebruikt
1. Klik in het venster **Inventarisatiedagboek** met de berekende verwachte voorraad op de actie **Afdrukken**.
2. Specificeer in het veld **Inventarisatielijst** of het rapport het berekende aantal moet tonen en of het rapport voorraadartikelen op serie-/lotnummers moet tonen.
3. Stel filters in als u het rapport alleen wilt afdrukken voor bepaalde artikelen, opslaglocaties, vestigingen of dimensies.
4. Klik op **Afdrukken**.

Medewerkers kunnen nu verder met het tellen van de voorraad en eventuele afwijkingen in het afgedrukte rapport vastleggen.

### <a name="to-enter-and-post-the-actual-counted-inventory-in-basic-warehouse-configurations"></a>De werkelijk getelde voorraad in standaardmagazijnconfiguraties invoeren en boeken
1. Voer op elke regel in het venster **Inventarisatiedagboek** waar de werkelijk beschikbare voorraad, zoals bepaald door de telling, afwijkt van de berekende hoeveelheid, de werkelijk beschikbare voorraad handmatig in het veld **Aantal (Inventarisatie)** in.

    De gerelateerde velden worden dienovereenkomstig bijgewerkt.

    > [!NOTE]  
    >   Als de verschillen in de telling worden veroorzaakt door artikelen die met de verkeerde vestigingscode zijn geboekt, moet u de verschillen niet invoeren in het inventarisatiedagboek. Gebruik in plaats daarvan het herindelingsdagboek of een transferorder om items om te leiden naar de juiste vestigingen. Zie voor meer informatie Art.-herindelingsdagboek of Transferorders maken.

2. Als de berekende aantallen wilt aanpassen aan de feitelijk getelde aantallen, kiest u de actie **Boeken**.

    Zowel de artikelposten als de inventarisatieposten worden gemaakt. Open de artikelkaart om de resulterende inventarisatieposten te bekijken.

3. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.
4. Als u de inventarisatie wilt controleren, opent u de betreffende artikelkaart en kiest u de actie **Inventarisatieposten**.

### <a name="to-enter-and-post-the-actual-counted-inventory-in-advanced-warehouse-configurations"></a>De werkelijk getelde voorraad in geavanceerde magazijnconfiguraties invoeren en boeken

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikeldagboek** in en kies vervolgens de gerelateerde koppeling.  
2.  Kies de actie **Magazijnherwaardering berekenen**.  
3.  Selecteer dezelfde artikelen die u hebt geteld in de inventarisatie door middel van periodieke tellingen die u zojuist hebt uitgevoerd en andere artikelen die moeten worden aangepast en kies vervolgens de knop **OK**.  

     Het venster **Voorraaddagboek** wordt geopend en voor deze artikelen worden regels gemaakt. Merk op dat de netto aantallen die u zojuist per opslaglocatie hebt geteld en geregistreerd nu gereed zijn om als artikelposten geconsolideerd en gesynchroniseerd te worden.  

4.  Boek het dagboek zonder de aantallen te wijzigen.  

De aantallen op de artikel- en de magazijnposten zijn nu wederom gelijk voor deze artikelen. Het programma heeft de laatste tellingsdatum van het artikel of de SKU bijgewerkt.  

## <a name="to-perform-cycle-counting"></a>Clustertelling uitvoeren
Hoewel alle artikelen in het magazijn minimaal een keer per jaar worden geteld, wilt u sommige artikelen misschien vaker tellen omdat ze waardevoller zijn of snel worden omgezet en belangrijk zijn voor het bedrijf. U kunt tellingsperioden instellen en toewijzen aan magazijnartikelen. Voor dit doel kunt u speciale telperioden aan die artikelen toewijzen.

U kunt de periodieke tellingen op een van de volgende manieren uitvoeren, afhankelijk van de magazijninstellingen. Zie voor meer informatie [Magazijnbeheer instellen](warehouse-setup-warehouse.md).  

-   Als u in de vestiging niet met gestuurde opslag en pick werkt (standaardmagazijnconfiguratie), gebruikt u het venster **Inventarisatiedagboek** in het menu **Voorraad**. De procedure is grotendeels hetzelfde als die van een inventarisatie zonder periodieke tellingen.  
-   Als uw locatie gestuurde opslag en pick gebruikt (geavanceerde magazijnconfiguratie), gebruikt u eerst het venster **Mag. inventarisatiedagboek** en vervolgens het venster **Artikeldagboek** voor het uitvoeren van de functie **Magazijnherwaardering berekenen**.  

### <a name="to-set-up-counting-periods"></a>U kunt als volgt tellingsperioden instellen
Een inventarisatie wordt gewoonlijk periodiek uitgevoerd, bijvoorbeeld maandelijks, per kwartaal of jaarlijks. U kunt elke gewenste periode instellen.

U stelt de inventarisatieperioden in die u wilt gebruiken en wijst er vervolgens één toe aan elk artikel. Wanneer u een inventarisatie uitvoert en **Tellingsperiode berekenen** in het inventarisatiedagboek gebruikt, worden de regels voor de artikelen automatisch gemaakt.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorraadtellingsperioden** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-assign-a-counting-period-to-an-item"></a>Een tellingsperiode toewijzen aan een artikel  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer het artikel waaraan u een tellingsperiode wilt toewijzen.  
3. Selecteer in het veld **Voorraadtellingsperiode** de gewenste tellingsperiode.  
4. Kies de knop **Ja** om de code te wijzigen en de eerste tellingsperiode voor het artikel te berekenen. De volgende keer dat u een tellingsperiode in het magazijninventarisatiedagboek berekent, wordt het item als een regel in het venster **Inventarisatieartikelselectie** weergegeven. U kunt vervolgens beginnen met tellen van het item op een periodieke basis.

### <a name="to-initiate-a-count-based-on-counting-periods-in-basic-warehouse-configurations"></a>Een inventarisatie uitvoeren op basis van tellingsperioden in standaardmagazijnconfiguraties
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inventarisatiedagboek** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Tellingsperiode berekenen**.

    Het venster **Inventarisatieartikelselectie** wordt geopend en bevat de artikelen waaraan tellingsperioden zijn toegewezen en die op basis daarvan moeten worden geteld.
3. Voer de inventarisatie uit. Zie voor meer informatie de sectie 'Een magazijninventarisatie uitvoeren'.

### <a name="to-initiate-a-count-based-on-counting-periods-in-advanced-warehouse-configurations"></a>Een inventarisatie uitvoeren op basis van tellingsperioden in geavanceerde magazijnconfiguraties
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Mag. inventarisatiedagboek** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Tellingsperiode berekenen**.

    Het venster **Inventarisatieartikelselectie** wordt geopend en bevat de artikelen waaraan tellingsperioden zijn toegewezen en die op basis daarvan moeten worden geteld.
3. Voer de inventarisatie uit. Zie voor meer informatie de sectie Een magazijninventarisatie uitvoeren.  

    > [!NOTE]  
    >  U moet het artikel tellen in alle opslaglocaties die het betreffende artikel bevatten. Indien u enkele opslaglocatieregels verwijdert die het programma heeft opgehaald om te tellen in het venster **Mag. Inventarisatie**, worden niet alle artikelen geteld die in het magazijn zijn. Indien u later dergelijke onvolledige resultaten in het inventarisatiedagboek boekt, zijn de geboekte aantallen onjuist.  

## <a name="to-adjust-the-inventory-of-one-item"></a>De voorraad van één artikel aanpassen
Nadat u een fysieke telling hebt uitgevoerd van een artikel in uw voorraadgebied, kunt u de functie **Voorraad wijzigen** gebruiken om het werkelijke voorraadaantal vast te leggen.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer het artikel waarvoor u voorraad wilt aanpassen, en kies vervolgens de actie **Voorraad wijzigen**.
3. Voer in het veld **Nieuwe voorraad** het voorraadaantal in dat u voor het artikel wilt vastleggen.
4. Kies de knop **Ok**.

De voorraad van het artikel is nu aangepast. Het nieuwe aantal wordt weergegeven in het veld **Huidige voorraad** in het venster **Voorraad wijzigen** en in het veld **Voorraad** in het venster **Artikelkaart** .

U kunt ook de functie **Voorraad wijzigen** gebruiken als eenvoudige manier om gekochte artikelen op voorraad te plaatsen als u geen inkoopfacturen of orders gebruikt om uw inkopen te registreren. Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md).

> [!NOTE]  
>   Als u voorraad hebt aangepast, moet u deze bijwerken met de huidige, berekende waarde. Zie [Voorraad herwaarderen](inventory-how-revalue-inventory.md) voor meer informatie.

### <a name="to-adjust-the-inventory-quantity-of-multiple-items-in-basic-warehouse-configurations"></a>Het voorraadaantal van meerdere artikelen in standaardmagazijnconfiguraties aanpassen
In het venster **Artikeldagboek** kunt u rechtstreeks artikeltransacties boeken om uw voorraad aan te passen in verband met inkopen, verkopen en positieve of negatieve mutaties, zonder documenten te gebruiken.

Als u het artikeldagboek vaak gebruikt om dezelfde of vergelijkbare dagboekregels te boeken, bijvoorbeeld met betrekking tot materiële consumptie, kunt u het venster **Standaardartikeldagboek** gebruiken om deze terugkerende taak gemakkelijker te maken. Zie de sectie 'Standaarddagboeken' in [Werken met dagboeken](ui-work-general-journals.md) voor meer informatie.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikeldagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Kies de actie **Boeken** om de voorraadherwaarderingen te maken.

> [!NOTE]  
>   Als u voorraad hebt aangepast, moet u deze bijwerken met de huidige, berekende waarde. Zie [Voorraad herwaarderen](inventory-how-revalue-inventory.md) voor meer informatie.

### <a name="to-adjust-bin-quantities-in-advanced-warehouse-configurations"></a>Opslaglocatieaantallen in geavanceerde magazijnconfiguraties aanpassen  
Als uw locatie met gestuurde opslag en pick werkt, wordt het **Mag.artikeldagboek** gebruikt om, buiten de context van de inventarisatie, alle positieve en negatieve correcties van het artikelaantal te boeken waarbij het gaat om werkelijke winst (bijvoorbeeld "verloren" artikelen die worden teruggevonden) of werkelijk verlies, bijvoorbeeld breekbare artikelen die stukgaan.  

In tegenstelling tot bij het boeken van herwaarderingen in het voorraadartikeldagboek, beschikt u bij het magazijnartikeldagboek over extra herwaarderingsmogelijkheden waardoor de records met de aantallen nog nauwkeuriger worden. Op deze manier beschikt het magazijn altijd over een volledig overzicht van het aantal artikelen dat voorradig is en waar de artikelen zijn opgeslagen. Als er een herwaardering wordt geregistreerd, wordt de herwaardering echter niet onmiddellijk naar artikelposten geboekt. Tijdens het registratieproces worden er credit- of debetnota's gemaakt voor de werkelijke opslaglocatie met de aantalherwaardering. Vervolgens wordt er een tegenboekingspost gemaakt in een opslaglocatieherwaardering. Dit is een virtuele opslaglocatie zonder feitelijke artikelen. Deze opslaglocatie wordt opgegeven in het veld **Opslaglocatiecode voorraadherwaardering** op de vestigingskaart.

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Mag.-artikeldagboek** in en kies vervolgens de gerelateerde koppeling.  
2.  Vul de informatie op de kop in.  
3.  Vul het veld **Artikelnr.** op de regel in.  
4.  Voer de naam van de opslaglocatie in waar u de extra artikelen wilt opslaan of waar de artikelen verloren zijn gegaan.  
5.  In het veld **Aantal** voert u het verschil in dat u hebt waargenomen. Als u extra artikelen hebt aangetroffen, voert u een positief aantal in. Bij ontbrekende artikelen voert u een negatieve waarde in.  
6.  Kies de actie **Registreren**.

## <a name="to-synchronize-the-adjusted-warehouse-entries-with-the-related-item-ledger-entries"></a>De aangepaste magazijnposten synchroniseren met de gerelateerde artikelposten
U moet op basis van toepasselijke intervallen, zoals deze via bedrijfsbeleid zijn gedefinieerd, de opslaglocatierecords voor magazijnherwaardering in de artikelpost boeken. In sommige bedrijven worden dergelijke herwaarderingen dagelijks bijgewerkt, terwijl dit proces in andere bedrijven minder vaak plaatsvindt.

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikeldagboek** in en kies vervolgens de gerelateerde koppeling.  
2.  Vul de velden op de dagboekregels in.  
3.  Kies de actie **Magazijnherwaardering berekenen** en vul de gewenste filters in het aanvraagvenster voor de batchtaak in. De herwaarderingen worden alleen berekend voor de posten in de opslaglocatieherwaardering die aan filtervereisten voldoen.  
4.  Op het sneltabblad **Opties** geeft u een waarde op voor het veld **Documentnr.**. Aangezien er geen getalreeks is ingesteld voor deze batchverwerking, kunt u het getalschema aanhouden dat is ingesteld voor het magazijn. Omdat er geen nummerreeks is ingesteld voor deze batchverwerking, moet u het nummerschema gebruiken dat is ingesteld door het magazijn of moet u de datum opgeven, gevolgd door uw initialen.  
5.  Kies de knop **OK**. Vervolgens worden er in het artikeldagboek regels gemaakt voor elk artikel waarvan de totale waarde een positief of negatief aantal is.  
6.  Boek de dagboekregels om de verschillen in aantal in te voeren op de artikelposten. De voorraad in de opslaglocaties van het magazijn komt nu precies overeen met de voorraad op de artikelposten.  

## <a name="to-reclassify-an-items-lot-number"></a>Het lotnummer van een artikel herindelen
Als u kenmerken van artikelposten wilt wijzigen, kunt u daarvoor het artikelherindelingsdagboek gebruiken. Typische kenmerken voor herindeling zijn dimensies en verkoopcampagnecodes, maar u kunt ook systeemtransfers uitvoeren door opslaglocatie- en vestigingscodes te herindelen.

Speciale stappen zijn van toepassing wanneer u serie- of lotnummers en hun vervaldatums wilt herindelen. Zie voor meer informatie [Werken met serie- en lotnummers](inventory-how-work-item-tracking.md).

Het volgende voorbeeld is gebaseerd op een vestigingscode. De stappen zijn vergelijkbaar voor andere soorten artikelkenmerken.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelherindelingsdagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Vul in het venster **Artikelherindelingsdagboeken** indien nodig de velden in.
3. In het veld **Vestiging** voert u de huidige vestigingscode voor het artikel in.
4. In het veld **Nieuwe vestiging** voert u de nieuwe vestigingscode voor het artikel in.
5. Kies de actie **Boeken**.

Zie [Voorraad overbrengen tussen vestigingen](inventory-how-transfer-between-locations.md) voor het overbrengen van artikelen met volledige controle over verzonden en ontvangen hoeveelheden.

## <a name="see-also"></a>Zie ook
[Voorraad](inventory-manage-inventory.md)
[Magazijnbeheer](warehouse-manage-warehouse.md)    
[Verkoop](sales-manage-sales.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

