---
title: Ontwerpdetails - Waarderingsmethoden voor artikelen wijzigen
description: 'Leer hoe u een andere waarderingsmethode aan een artikel kunt toewijzen, hoewel u het artikel al in transacties hebt gebruikt.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'costing methods, costing, item cost'
ms.search.form: 8645
ms.date: 06/08/2021
ms.author: bholtorf
---

# <a name="design-details-change-the-costing-method-for-items"></a><a name="design-details-change-the-costing-method-for-items"></a>Ontwerpdetails - De waarderingsmethode voor artikelen wijzigen

In [!INCLUDE[prod_short](includes/prod_short.md)] kunt u een waarderingsmethode voor een artikel niet wijzigen nadat u het artikel in een transactie hebt opgenomen. Bijvoorbeeld nadat u het artikel hebt gekocht of verkocht. Als aan het artikel of de artikelen een onjuiste waarderingsmethode is toegewezen, ontdekt u het probleem mogelijk pas wanneer u uw financiële rapportage uitvoert.

In dit onderwerp wordt beschreven hoe u deze situatie kunt oplossen. De aanbevolen aanpak is om het artikel met de onjuiste waarderingsmethode te vervangen door een nieuw artikel en een assemblageorder te gebruiken om de voorraad van het oude artikel naar het nieuwe over te dragen.

> [!NOTE]
> Door gebruik te maken van assemblageorders kunnen de kosten blijven lopen, hoewel er nog te boeken inkoopfacturen of verzendkosten zijn. Bovendien kunt u de conversie ongedaan maken en indien nodig de hoeveelheden van de originele artikelen terugkrijgen.

> [!TIP]
> Om vertrouwd te raken met het proces raden we u aan het conversieproces te starten met een enkel artikel of een kleine set artikelen.

## <a name="about-costing-methods"></a><a name="about-costing-methods"></a>Over waarderingsmethoden

Waarderingsmethode bepalen de kostenberekeningen wanneer goederen worden gekocht, ontvangen in voorraad en verkocht. Waarderingsmethoden zijn van invloed op de timing van in KPV geregistreerde bedragen die van invloed zijn op de brutowinst. Het is deze stroom die KPV berekent. De kosten van verkochte goederen (KPV) en inkomsten worden als volgt gebruikt om de brutowinst te bepalen:

*brutowinst* = *inkomsten - KPV*

Wanneer u voorraadartikelen instelt, moet u een waarderingsmethode toewijzen. De methode kan van bedrijf tot bedrijf en van artikel tot artikel verschillen, dus het is belangrijk om de juiste te kiezen. De volgende waarderingsmethoden worden ondersteund in [!INCLUDE[prod_short](includes/prod_short.md)]:

* Gemiddelde
* FIFO
* LIFO
* Standaard
* Specifiek

Zie [Ontwerpdetails: Waarderingsmethoden](design-details-costing-methods.md) voor meer informatie.

## <a name="use-assembly-orders-to-change-costing-method-assignments"></a><a name="use-assembly-orders-to-change-costing-method-assignments"></a>Assemblageorders gebruiken om toewijzingen van waarderingsmethoden te wijzigen

In deze sectie worden de volgende stappen beschreven voor het wijzigen van de waarderingsmethode die aan een artikel is toegewezen:

1. Een standaardwaarderingsmethode opgeven.
2. De artikelen identificeren waarvoor u de waarderingsmethode wilt wijzigen en deze hernummeren.
3. Handmatig nieuwe artikelen met het oude nummeringsschema maken en de hoofdgegevens in een batch kopiëren.
4. Handmatig gerelateerde hoofdgegevens van het bestaande artikel naar het nieuwe artikel kopiëren.
5. De voorraadhoeveelheid bepalen die u wilt converteren van het oorspronkelijke artikel naar het nieuwe artikel.
6. De inventaris overbrengen naar het nieuwe artikel.
7. Voorraadhoeveelheden verwerken die zijn toegewezen aan de vraag.
8. Het oorspronkelijke artikel voor verder gebruik blokkeren.  

### <a name="define-a-default-costing-method"></a><a name="define-a-default-costing-method"></a>Een standaardwaarderingsmethode opgeven

Om toekomstige fouten te voorkomen kunt u een standaardwaarderingsmethode voor nieuwe artikelen specificeren. Telkens wanneer iemand een nieuw artikel maakt, stelt [!INCLUDE[prod_short](includes/prod_short.md)] de standaardwaarderingsmethode voor. U specificeert de standaardmethode in het veld **Standaardwaarderingsmethode** op de pagina **Voorraadinstellingen**. 

### <a name="identify-the-items-to-change-the-costing-method-for-and-renumber-them"></a><a name="identify-the-items-to-change-the-costing-method-for-and-renumber-them"></a>De artikelen identificeren waarvoor u de waarderingsmethode wilt wijzigen en deze hernummeren

Mogelijk wilt u uw nieuwe artikelen dezelfde nummers geven als de artikelen die ze vervangen. Wijzig hiervoor de nummers van de bestaande artikelen. Als het bestaande artikelnummer bijvoorbeeld 'P1000' is, kunt u dit wijzigen in 'X-P1000'. Dit is een handmatige wijziging die u voor elk artikel moet aanbrengen.

### <a name="create-new-items-with-the-old-numbering-scheme-and-copy-the-master-data-in-a-batch"></a><a name="create-new-items-with-the-old-numbering-scheme-and-copy-the-master-data-in-a-batch"></a>Handmatig nieuwe artikelen met het oude nummeringsschema maken en de hoofdgegevens in een batch kopiëren

Maak de nieuwe artikelen met het huidige nummeringschema. Met uitzondering van het veld **Waarderingsmethode** moeten de nieuwe artikelen dezelfde stamgegevens bevatten als de bestaande. Gebruik om de hoofdgegevens voor het artikel en gerelateerde gegevens van andere functies over te dragen de actie **Item kopiëren** op de pagina **Artikelkaart**. Zie voor meer informatie [Bestaande items kopiëren om nieuwe items te maken](inventory-how-copy-items.md).

Nadat u de nieuwe artikelen hebt gemaakt en de hoofdgegevens hebt overgedragen, wijst u de juiste waarderingsmethode toe.

### <a name="manually-copy-related-master-data-from-the-original-item-to-the-new-item"></a><a name="manually-copy-related-master-data-from-the-original-item-to-the-new-item"></a>Handmatig gerelateerde hoofdgegevens van het oorspronkelijke artikel naar het nieuwe artikel kopiëren

Om de nieuwe artikelen volledig bruikbaar te maken moet u sommige hoofdgegevens uit andere gebieden handmatig kopiëren, zoals beschreven in de volgende tabel.

|District  |Wat te kopiëren  |Hoe u dit doet  |
|---------|---------|---------|
|Voorraad |SKU's |Controleer of er een SKU is gespecificeerd voor het originele artikel. Als voor elke SKU-kaart planningsparameters zijn ingevoerd, moet u de SKU voor het nieuwe artikel handmatig maken. Als de parameters niet zijn gespecificeerd, kunt u de batchtaak **SKU maken** vanaf de pagina **Artikelkaart** gebruiken om de gegevens te maken.|
| |Artikelvervangingen |Controleer of er artikelvervangingen zijn gedefinieerd voor het oorspronkelijke artikel. Als dat zo is, breng die gegevens dan over naar het nieuwe artikel. Als u vervangende artikelen wilt weergeven, gebruikt u de actie **Vervangingen** op de pagina **Artikelkaart**. |
| |Analyserapporten |Bekijk de rapporten Artikelanalyse, Verkoopanalyse en Inkoopanalyse. Voor als naar de oorspronkelijke artikelen wordt verwezen kunt u een nieuw analyserapport maken met een verwijzing naar het nieuwe artikel (en het originele analyserapport behouden om als historie te gebruiken) of de rapporten aanpassen zodat deze naar het nieuwe artikel verwijzen. |
| |Standaarddagboeken |Controleer of standaarddagboeken verwijzen naar het oorspronkelijke artikel en breng die gegevens indien nodig over naar het nieuwe artikel. Deze informatie is te vinden in de standaarddagboeken, die beschikbaar zijn in het artikeldagboek.  |
|Verkoop |Vooruitbetalingspercentages verkoop | Controleer of er voor het oorspronkelijke artikel verkoopvooruitbetalingspercentages zijn gedefinieerd en breng die gegevens over naar het nieuwe artikel. Om de vooruitbetalingspercentages te bekijken kiest u op de pagina **Artikelkaart** **Verkoop** en dan **Vooruitbetalingspercentages**.|
|Inkoop |Vooruitbetalingspercentage inkoop |Controleer of er voor het oorspronkelijke artikel inkoopvooruitbetalingspercentages zijn gedefinieerd en breng die gegevens over naar het nieuwe artikel. Om de vooruitbetalingspercentages te bekijken kiest u op de pagina **Artikelkaart** **Inkopen** en dan **Vooruitbetalingspercentages**. |
|Magazijn |Opslaglocatie-inhoud |Bekijk de opslaglocatie-inhoud die voor het originele artikel is gedefinieerd. Als kolommen zoals Min. aantal, Max. aantal, Standaard en Speciaal afzonderlijk zijn ingevoerd, moet u handmatig opslaglocatie-inhoud maken voor het nieuwe artikel. Als dat niet het geval is, is er geen actie vereist. [!INCLUDE[prod_short](includes/prod_short.md)] houdt records bij wanneer u magazijndocumenten en tijdschriften registreert.|
|Project |Projectprijzen |Controleer of er voor het oorspronkelijke artikel projectprijzen zijn gedefinieerd en breng die gegevens over naar het nieuwe artikel. Deze informatie is beschikbaar op de pagina **Projectkaart** in het gedeelte **Projectdetails - Aantal prijzen** in het **deelvenster Feitenblok**. |
|Service |Serviceresourcevaardigheid |Controleer of er serviceresourcevaardigheden voor het oorspronkelijke artikel zijn gedefinieerd en breng die gegevens over naar het nieuwe artikel. Als u resourcevaardigheden wilt weergeven, gebruikt u de actie **Resourcevaardigheden** op de pagina **Artikelkaart**.  |
| |Serviceartikelonderdelen |Controleer of er onderdelen voor het oorspronkelijke serviceartikel zijn gedefinieerd en breng die gegevens over naar het nieuwe artikel. Om onderdelen van serviceartikelen te bekijken gebruikt u op de pagina **Artikelkaart** de actie **Serviceartikel** om de lijst met gerelateerde serviceartikelen te openen en kiest u vervolgens de actie **Materialen**.  |
|Productie |Productiestuklijsten |Controleer of productiestuklijsten het originele artikel bevatten en vervang het door het nieuwe artikel. Om het originele artikel te vervangen kiest u op de pagina **Productiestuklijsten** de actie **Prod.-stuklijstartikel vervangen**. |
|Assemblage |Assemblagestuklijsten |Controleer of assemblagestuklijsten het originele artikel bevatten en vervang het handmatig door het nieuwe artikel. |

> [!IMPORTANT]
> Als de nieuwe waarderingsmethode Standaard is, moet u een waarde invoeren in het veld **Vaste verrekenprijs** op de pagina **Artikelkaart**. U kunt de pagina **Vaste-verrekenprijsvoorstel** gebruiken om de kostenaandelen dienovereenkomstig in te stellen. Zie [Vaste verrekenprijzen aanpassen](finance-how-to-update-standard-costs.md) voor meer informatie.

### <a name="determine-the-inventory-quantity-to-convert-from-the-original-item-to-the-new-item"></a><a name="determine-the-inventory-quantity-to-convert-from-the-original-item-to-the-new-item"></a>De voorraadhoeveelheid bepalen die u wilt converteren van het oorspronkelijke artikel naar het nieuwe artikel

> [!NOTE]
> Deze stap houdt geen rekening met hoeveelheden die zijn opgenomen in niet-verzonden bestellingen. Zie voor meer informatie [Voorraadhoeveelheden verwerken die zijn toegewezen aan de vraag](design-details-changing-costing-methods.md#handle-inventory-quantities-that-are-allocated-to-demand). 

Gebruik een fysiek voorraadjournaal om een lijst met de hoeveelheden in voorraad te maken. Gebruik een van de volgende opties, afhankelijk van de instelling van de magazijnlocatie:

* Inventarisatiedagboeken
* Magazijninventarisatie dagboeken

Beide dagboeken kunnen de voorraadhoeveelheid van het artikel berekenen, inclusief de locatie, de variant en de opslaglocatie. Zie voor meer informatie [Voorraad tellen, corrigeren en herindelen met dagboeken](inventory-how-count-adjust-reclassify.md)

### <a name="transfer-the-inventory-to-the-new-item"></a><a name="transfer-the-inventory-to-the-new-item"></a>De inventaris overbrengen naar het nieuwe artikel

Maak en boek assemblageorders om de kosten en het voorraadaantal over te dragen van het oorspronkelijke artikel naar het nieuwe artikel. Assemblageorders kunnen het ene artikel naar het andere converteren met behoud van de kosten. Dit helpt ervoor te zorgen dat de nettototalen voor de voorraadrekening en KPV niet worden beïnvloed (behalve wanneer de nieuwe waarderingsmethode Standaard is, in welk geval de kosten kunnen worden verdeeld over verschilrekeningen). Zie voor meer informatie [Assemblagebeheer](assembly-assemble-items.md).

Gebruik bij het maken van assemblageorders de informatie uit het inventarisatiedagboek of het magazijninventarisatiedagboek. De volgende tabellen beschrijven de informatie in de rapporten die in de koptekst en regels van de assemblageorder moeten worden ingevoerd.

#### <a name="header"></a><a name="header"></a>Koptekst

|Veld  |In te voeren waarde  |
|---------|---------|
|Artikelnr. |Het nummer van het nieuwe artikel. |
|Aantal |De hoeveelheid in het fysieke voorraadjournaal.<br> **OPMERKING:** de hoeveelheden berekend door de fysieke voorraadjournalen omvatten niet de hoeveelheden in orders zijn die nog niet zijn verzonden.  |
|Variant |Hetzelfde als in het fysieke voorraadjournaal.  |
|Vestiging |Hetzelfde als in het fysieke voorraadjournaal. |
|Code van maateenheid |Hetzelfde als in het fysieke voorraadjournaal. |
|Opslaglocatie |Hetzelfde als in het fysieke voorraadjournaal. |

#### <a name="lines"></a><a name="lines"></a>Regels

|Veld  |In te voeren waarde  |
|---------|---------|
|Soort |Artikel |
|Nee. |Het nummer van het oorspronkelijke artikel. |
|Aantal per |1 |
|Variant |Hetzelfde als in het fysieke voorraadjournaal. |
|Vestiging |Hetzelfde als in het fysieke voorraadjournaal. |
|Code van maateenheid |Hetzelfde als in het fysieke voorraadjournaal. |

> [!NOTE]
> Een assemblageorder kan slechts één SKU van een artikel tegelijk verwerken. U moet een assemblageorder maken voor elke combinatie van SKU met een hoeveelheid in voorraad.

> [!NOTE]
> Voor een magazijnlocatie moet u mogelijk picks maken voordat u de assemblageorder kunt boeken. Om dat te onderzoeken bekijkt u de instelling voor picken op de pagina **Locatiekaart**. Zie voor meer informatie [Artikelen en locaties instellen voor gestuurde opslag en pick](warehouse-how-to-set-up-items-for-directed-put-away-and-pick.md).

### <a name="handle-inventory-quantities-that-are-allocated-to-demand"></a><a name="handle-inventory-quantities-that-are-allocated-to-demand"></a>Voorraadhoeveelheden verwerken die zijn toegewezen aan vraag

Idealiter zou de voorraad voor het oorspronkelijke artikel naar nul moeten gaan nadat u de voorraadaantallen hebt overgeboekt. Er kunnen echter openstaande orders, werkbladen en dagboeken zijn (zie onderstaande tabel) waarvoor nog steeds een hoeveelheid van het oorspronkelijke artikel nodig is. De hoeveelheid kan ook worden geblokkeerd door een reservering of artikeltracering.

**Voorbeeld** Er zijn 1000 stuks in voorraad en 20 stuks zijn gereserveerd voor een verkooporder die nog niet is verzonden. In dat geval kunt u besluiten de 20 stuks te behouden in het oude artikel zodat u de openstaande order kunt uitvoeren.

> [!NOTE]
> Er zijn functionele gebieden die de hoeveelheid kunnen beïnvloeden, zoals vermeld in de onderstaande tabel, dus het kan lastig zijn om de juiste hoeveelheid te vinden. Om veilig te zijn kunt u met behulp van het bovenstaande voorbeeld 100 stuks behouden en de resterende 900 stuks in plaats daarvan overbrengen. Een andere manier om dit te doen is door de documenten en dagboeken te verwerken, zodat er nog slechts een paar beheersbare overblijven. Nog een ander alternatief is om de volledige hoeveelheid over te dragen naar het nieuwe artikel en vervolgens een deel terug te sturen naar het oorspronkelijke artikel met behulp van de assemblageorder.

De volgende tabel vermeldt functionele gebieden waar er mogelijk uitstaande hoeveelheden zijn.

|District  |Waar te zoeken naar openstaande hoeveelheden  |
|---------|---------|
|Verkoop |Verkoopdocumenten, inclusief orders, retourorders, facturen, offertes, raamcontracten en creditnota's |
|Voorraad |Artikeljournalen, reserveringen, artikeltracering en vaste-verrekenprijsvoorstel |
|Inkoop |Inkoopdocumenten, inclusief orders, retourorders, facturen, offertes, raamcontracten en creditnota's |
|Planning |Inkoopvoorstel, planningsvoorstel en orderplanning |
|Magazijn |Transferorders, magazijnzendingen, magazijnjournalen en magazijnpicks, opslagactiviteiten en verplaatsingen, interne picks en opslagactiviteiten en maakvoorstellen voor opslaglocaties |
|Assemblage |Assemblagedocumenten, inclusief orders, retourorders en raamcontracten |
|Projecten |Projectplanningsregels en projectdagboekregels |
|Service |Servicedocumenten en servicecontracten |
|Productie |Productieorders (gepland, vast gepland en vrijgegeven) |

### <a name="block-the-original-item-from-further-use"></a><a name="block-the-original-item-from-further-use"></a>Het oorspronkelijke artikel voor verder gebruik blokkeren

Als de voorraad voor het oorspronkelijke artikel nul is, kunt u het artikel blokkeren om te voorkomen dat het wordt gebruikt in nieuwe transacties. Om het artikel te blokkeren zet u op de pagina **Artikelkaart** de schakelaar **Geblokkeerd** aan. Zie voor meer informatie [Artikelen blokkeren vanuit Verkoop of Inkoop](inventory-how-block-items.md).

## <a name="summary"></a><a name="summary"></a>Overzicht

Het wijzigen van de waarderingsmethode voor artikelen die in transacties zijn gebruikt, is een proces en geen standaardactie in [!INCLUDE[prod_short](includes/prod_short.md)]. U kunt de in dit onderwerp beschreven stappen gebruiken als sjabloon voor het proces.

Het proces kan tijdrovend zijn omdat er verschillende handmatige stappen zijn. Als u echter de tijd neemt om het te voltooien, wordt de impact van fouten op uw grootboek geminimaliseerd.

We raden het volgende aan:

1. Beoordeel de haalbaarheid van het proces door één of misschien een paar representatieve artikelen door het hele proces te halen.
2. Overweeg contact op te nemen met een ervaren partner die u bij het proces kan helpen.

## <a name="see-also"></a><a name="see-also"></a>Zie ook

[Ontwerpdetails: Waarderingsmethoden](design-details-costing-methods.md)  
[Overzicht](design-details-inventory-costing.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
