---
title: 'Ontwerpdetails: Planningsparameters'
description: In dit artikel worden de verschillende planningsparameters beschreven die u kunt gebruiken en hoe deze het planningssysteem beïnvloeden.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 04/26/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="design-details-planning-parameters"></a>Ontwerpdetails: Planningsparameters

Dit artikel beschrijft de verschillende planningsparameters die u kunt gebruiken in [!INCLUDE[prod_short](includes/prod_short.md)].  

Hoe het planningssysteem de artikelvoorziening controleert, wordt bepaald door verschillende instellingen op de pagina **Artikelkaart**, **SKU** en **Productie-instellingen**. In de volgende tabel wordt uitgelegd hoe de planning deze instellingen gebruikt.  

|Doel|Instellingen|
|-------------|---------------|
|Definiëren of het artikel wordt gepland|Bestelbeleid = leeg|
|Definiëren wanneer moet worden besteld|Tijdsinterval<br /><br /> Bestelpunt<br /><br /> Veiligheidstijd|
|Definiëren hoeveel moet worden besteld|Veiligheidsvoorraad<br /><br /> Bestelbeleid:<br /><br /> -   Vast bestelaantal plus bestelaantal<br />-   Maximum aantal plus Maximale voorraad<br />-   Order<br />-   Lot-voor-lot|
|Optimaliseren wanneer en hoe u bestelt|Herplanningsperiode<br /><br /> Lotaccumulatieperiode<br /><br /> Dempingsperiode|
|De voorzieningenorders wijzigen|Min. bestelaantal<br /><br /> Max. bestelaantal<br /><br /> Vaste lotgrootte|
|Het geplande artikel beperken|Productiebeleid:<br /><br /> -  Op voorraad produceren<br />- Op order produceren|

## <a name="define-whether-the-item-is-planned"></a>Definiëren of het artikel wordt gepland

Om een artikel of SKU in het planningsproces op te nemen moet u er een bestelbeleid aan toewijzen. Anders moet het handmatig worden gepland, bijvoorbeeld met behulp van de functie Orderplanning.  

## <a name="define-when-to-reorder"></a>Definiëren wanneer moet worden besteld

Voorstellen voor opnieuw bestellen worden normaal gesproken alleen vrijgegeven wanneer de verwachte beschikbare hoeveelheid op of onder een bepaalde hoeveelheid komt. Het bestelpunt wordt bepaald door de hoeveelheid. Anders wordt het nul. Nul kan worden aangepast door een veiligheidsvoorraad in te voeren. Als u een veiligheidstijd hebt opgegeven, wordt het voorstel gedaan in de periode vóór de vereiste vervaldatum.  

Het veld **Tijdsinterval** wordt gebruikt door bestelpuntbeleid (**Vast bestelaantal** en **Maximum aantal**). Na elk tijdsinterval wordt het voorraadniveau gecontroleerd. Het eerste tijdsinterval begint op de begindatum van de planning.  

> [!NOTE]  
> Bij de berekening van tijdsintervallen negeert het planningssysteem werkagenda's die zijn gedefinieerd in het veld **Basisagendacode** op de pagina's **Bedrijfsgegevens** en **Vestiging**.  

Op de **Productie-instellingen** moet u het standaardveiligheidsbeleid instellen op ten minste één dag. De vervaldatum van de vraag kan bekend zijn, maar niet de vervaltijd. De planning plant achterwaarts om aan de brutovraag te voldoen. Als u geen veiligheidsdoorlooptijd definieert, kunnen de goederen te laat aankomen om aan de vraag te voldoen.  

De velden **Herplanningsperiode**, **Lotaccumulatieperiode** en **Dempingsperiode**, spelen ook een rol bij de definitie van wanneer moet worden herbesteld. Voor meer informatie zie [Optimaliseren wanneer en hoe u bestelt](design-details-planning-parameters.md#optimize-when-and-how-much-to-reorder),  

## <a name="define-how-much-to-reorder"></a>Definiëren hoeveel moet worden besteld

Als het planningssysteem de noodzaak voor een bestelling detecteert, bepaalt het bestelbeleid wanneer en hoeveel moet worden besteld.  

Het planningssysteem volgt, onafhankelijk van het bestelbeleid, meestal deze logica:  

1. Bereken de hoeveelheid van ordervoorstel om te voldoen aan het minimumvoorraadniveau van het artikel, doorgaans de veiligheidsvoorraad. Als er niets is opgegeven, wordt het minimumvoorraadniveau nul.  
2. Als de verwachte beschikbare voorraad onder het veiligheidsvoorraadaantal ligt, wordt een achterwaarts geplande voorzieningenorder voorgesteld. Met het orderaantal wordt ten minste de veiligheidsvoorraad gevuld, en het kan worden verhoogd met de brutovraag binnen het tijdsinterval, met het bestelbeleid en met de bestelvelden.  
3. Als de verwachte voorraad op of onder het bestelpunt ligt (berekend vanaf gecombineerde wijzigingen binnen het tijdsinterval) en boven het veiligheidsvoorraadaantal, wordt een voorwaarts geplande uitzonderingorder voorgesteld. De brutovraag waaraan moet worden voldaan en het bestelbeleid bepalen het orderaantal. Het orderaantal is minstens gelijk aan het bestelpunt.  
4. Als er meer brutovraag vervalt vóór de einddatum van het voorwaarts geplande ordervoorstel en de huidige berekende verwachte beschikbare voorraad door deze vraag onder het veiligheidsvoorraadaantal komt, wordt het orderaantal verhoogd om het tekort te dekken. De voorgestelde voorzieningenorder wordt vervolgens achterwaarts gepland vanaf de vervaldatum voor de brutovraag die de veiligheidsvoorraad zou hebben overschreden.  
5. Als het veld **Tijdsinterval** niet is ingevuld, wordt alleen de brutovraag op dezelfde vervaldatum toegevoegd.  

### <a name="reordering-policies"></a>Bestelbeleid

Het volgende bestelbeleid heeft invloed op de hoeveelheid die wordt besteld. Ga voor meer informatie over bestelbeleid naar [Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md).  

|Bestelbeleid|Beschrijving|  
|-----------------------|---------------------------------------|  
|**Vast bestelaantal**|Het orderaantal zal minimaal gelijk zijn aan het bestelaantal. U kunt de hoeveelheid vergroten om aan de vraag of het gewenste voorraadniveau te voldoen. Dit bestelbeleid wordt gewoonlijk gebruikt met een bestelpunt.|  
|**Maximum aantal**|De orderhoeveelheid wordt berekend om te voldoen aan de maximale voorraad. Als aantalbepalingen worden gebruikt, kan de maximale voorraad worden overschreden. We adviseren het tijdsinterval niet samen met het maximumaantal te gebruiken. Het tijdsinterval wordt meestal genegeerd. Dit bestelbeleid wordt gewoonlijk gebruikt met een bestelpunt.|  
|**Order**|Het orderaantal wordt berekend om aan elke vraaggebeurtenis te voldoen en de vraag-voorzieningcombinatie blijft gekoppeld tot aan het uitvoeren. Er wordt geen rekening gehouden met planningsparameters.|  
|**Lot-for-Lot**|Het aantal wordt berekend om te voldoen aan de som van de vraag die vervalt in het tijdsinterval.|  

## <a name="optimize-when-and-how-much-to-reorder"></a>Optimaliseren wanneer en hoe u bestelt

Een planner kan planningsparameters afstemmen om voorstellen voor herplanning te beperken, vraag te cumuleren (dynamisch bestelaantal) of onbeduidende planningsacties te voorkomen. De volgende velden helpen te optimaliseren wanneer en hoeveel moet worden besteld.  

|Veld|Beschrijving|  
|---------------------------------|---------------------------------------|  
|**Herplanningsperiode**|Dit veld bepaalt of de planningsboodschap een bestaande order opnieuw moet plannen, of moet annuleren en een nieuwe order moet maken. De bestaande order wordt opnieuw gepland binnen één herplanningsperiode vóór de huidige voorziening en tot één herplanningsperiode na de huidige voorziening.<br><br>**Opmerking:** deze parameter werkt alleen met het **Lot-for-Lot** bestelbeleid.|  
|**Lotaccumulatieperiode**|Met het bestelbeleid Lot-voor-Lot wordt dit veld gebruikt om meerdere voorzieningen samen te voegen in één aanvulorder. Vanaf de eerste geplande voorziening worden alle voorzieningsvereisten in de volgende lotaccumulatieperiode samengevoegd in één voorziening, die wordt geplaatst op de datum van de eerste voorziening. Vraag buiten de lotaccumulatieperiode wordt niet gedekt door deze voorziening.|  
|**Dempingsperiode**|Dit veld wordt gebruikt om het op kleine schaal opnieuw plannen van bestaande voorzieningen te voorkomen. Wijzigingen vanaf de voorzieningsdatum tot aan één dempingsperiode vanaf de voorzieningsdatum genereren geen planningsboodschappen.<br /><br /> Met de dempingsperiode wordt een periode opgegeven waarbinnen u niet wilt dat het planningssysteem voorstelt bestaande aanvulorders opnieuw en eerder te plannen. Dit beperkt het aantal onbeduidende herplanningen van bestaande leveringen op een later tijdstip als de opnieuw geplande datum binnen de dempingsperiode valt.<br /><br /> Hierdoor is een positieve delta tussen de voorgestelde nieuwe voorzieningsdatum en de oorspronkelijke voorzieningsdatum altijd groter dan de dempingsperiode.|  

> [!NOTE]
> Met het herbestelbeleid Lot-voor-Lot moet de waarde van het veld **Lotaccumulatieperiode** gelijk zijn aan of groter zijn dan de waarde van het veld **Dempingsperiode**. Anders wordt de dempingsperiode tijdens de planningsroutine automatisch verkort om overeen te komen met de accumulatieperiode van de partij.  

De timing van de herplanningsperiode, dempingsperiode en lotaccumulatieperiode is gebaseerd op een voorzieningsdatum. Het tijdsinterval wordt gebaseerd op de begindatum van de planning, zoals in de onderstaande afbeelding is weergegeven.  

:::image type="content" source="media/supply_planning_5_time_bucket_elements.png" alt-text="Tijdsintervalelementen":::

In de volgende voorbeelden geven de zwarte pijlen bestaand aanbod (omhoog) en bestaande vraag (omlaag) aan. Rode, groene en oranje pijlen zijn planningsuggesties.  

**Voorbeeld 1**: De gewijzigde datum ligt buiten de herplanningsperiode, waardoor de bestaande voorziening wordt geannuleerd. Er wordt een nieuwe voorziening voorgesteld om te voldoen aan de vraag in de lotaccumulatieperiode.  

:::image type="content" source="media/supply_planning_5_recheduling_period_lot_accumulation_period.png" alt-text="Herplanningsperiode en lotaccumulatieperiode":::

**Voorbeeld 2**: De gewijzigde datum ligt in de herplanningsperiode, waardoor de bestaande voorziening opnieuw wordt gepland. Er wordt een nieuwe voorziening voorgesteld om te voldoen aan de vraag buiten de lotaccumulatieperiode.  

:::image type="content" source="media/supply_planning_5_recheduling_period_lot_accum_period_reschedule.png" alt-text="Herplanningsperiode, lotaccumulatieperiode en herplannen.":::

**Voorbeeld 3**: er is vraag in de dempingsperiode en het voorzieningsaantal in de lotaccumulatieperiode komt overeen met het voorzieningsaantal. De volgende vraag wordt blootgelegd en er wordt een nieuwe voorziening voorgesteld.  

:::image type="content" source="media/supply_planning_5_dampener_period_lot_accumulation_period.png" alt-text="Dempingsperiode en lotaccumulatieperiode.":::

**Voorbeeld 4**: Er is vraag in de dempingsperiode en het aanbod blijft op dezelfde datum. De huidige aanbodhoeveelheid dekt echter niet de vraag in de lotaccumulatieperiode. Er wordt een actie voor het wijzigen van de hoeveelheid voor de bestaande aanvulorder voorgesteld.  

:::image type="content" source="media/supply_planning_5_dampener_period_lot_accum_period_change_qty.png" alt-text="Dempingsperiode, lotaccumulatieperiode en hoeveelheid wijzigen.":::

**Standaardwaarden:** de standaardwaarde van het veld **Tijdsinterval** en de drie bestelperiodevelden is leeg. Voor alle velden behalve het veld **Dempingsperiode** betekent dit 0D (nul dagen). Als het veld **Dempingsperiode** leeg is, wordt de globale waarde in het veld **Standaard dempingsperiode** op de pagina **Productie-instellingen** gebruikt.  

## <a name="modify-the-supply-orders"></a>De voorzieningenorders wijzigen

Wanneer het aantal van het ordervoorstel is berekend, kan het worden aangepast door een of meer van de orderwijzigingen. Het maximale orderaantal is bijvoorbeeld groter dan of gelijk aan het minimale orderaantal, dat groter is dan of gelijk is aan de vaste lotgrootte.  

Het aantal wordt verminderd als het maximale bestelaantal wordt overschreden. Het wordt verhoogd als het onder het minimale bestelaantal valt. Ten slotte wordt het naar boven afgerond zodat het overeenkomt met een opgegeven vaste lotgrootte. Voor een eventueel resterend aantal worden dezelfde correcties gebruikt totdat de totale vraag is omgezet in ordervoorstellen.  

## <a name="delimit-the-item"></a>Het artikel beperken

Het veld **Productiebeleid** op de pagina **Artikelkaart** definieert welke andere orders de MRP-berekening voorstelt.  

Als de optie **Op voorraad produceren** wordt gebruikt, hebben de orders alleen betrekking op het artikel.  

Als de optie **Op order produceren** wordt gebruikt, analyseert het planningssysteem de productiestuklijst van het artikel en worden gekoppelde ordervoorstellen op lager niveau gemaakt voor deze artikelen, die ook worden gedefinieerd als op-order-produceren. Dit gaat door zolang er op maat gemaakte producten in de aflopende stuklijststructuren zijn.

## <a name="use-low-level-codes-to-manage-derived-demand"></a>Low-levelcodes gebruiken om afgeleide vraag te beheren

Gebruik low-levelcodes om afgeleide vraag naar componenten de lagere niveaus van de stuklijst te laten doorlopen. Ga voor meer informatie over low-level codes naar [Prioriteit/low-levelcode artikel](design-details-central-concepts-of-the-planning-system.md#item-priority--low-level-code).

U kunt een low-levelcode toewijzen aan elk onderdeel in de productstructuur of de ingesprongen stuklijst. Het hoogste definitieve assemblageniveau wordt aangeduid als niveau 0 - het eindartikel. Hoe hoger het nummer van de low-levelcode, hoe lager het artikel is in de hiërarchie. Eindartikelen hebben bijvoorbeeld low-levelcode 0 en de artikelonderdelen die in de assembly van het eindartikel worden opgenomen, hebben low-levelcodes 1, 2, 3, enzovoort. Het resultaat is de planning van onderdelen, gecoördineerd met de vereisten van alle onderdeelnummers op een hoger niveau. Wanneer u a plan berekent, wordt de stuklijst geëxplodeerd in het planningsvoorstel en de brutobehoeften voor niveau 0 worden doorgegeven in de planningsniveaus als brutobehoeften voor het volgende planningsniveau.

Selecteer op de pagina **Productie-instellingen** de schakelaar **Dynamische low-levelcode** om op te geven of er onmiddellijk codes op laag niveau moeten worden toegewezen en berekend voor elk onderdeel in de productstructuur. Als u grote hoeveelheden gegevens hebt, kan deze functie een negatief effect op de prestaties van het programma hebben, bijvoorbeeld tijdens automatische kostenwaardering. Dit is geen functie met terugwerkende kracht, dus het is raadzaam om het gebruik van deze functie tevoren uit te denken.

In plaats van de automatische berekening die dynamisch plaatsvindt als het veld is geselecteerd, kunt u de batchverwerking **Low-levelcode berekenen** in het menu **Productie** uitvoeren door op **Productontwerp**, **Low-levelcode berekenen** te klikken.

> [!IMPORTANT]
> Als u de schakelaar **Dynamische low-levelcode** niet inschakelt, moet u de batchbewerking **Low-levelcode berekenen** uitvoeren voordat u een leveringsplan berekent (de batchverwerking **Planning berekenen**).  

> [!NOTE]
> Hoewel u het veld **Dynamische low-levelcode** hebt geselecteerd, worden de low-levelcodes van artikelen niet dynamisch gewijzigd als een bovenliggende stuklijst wordt verwijderd of op niet-gecertificeerd is ingesteld. Dit kan het problematisch worden om nieuwe artikelen aan het einde van de productstructuur toe te voegen, omdat de low-levelcodelimiet wordt overschreden. Daarom kunt u voor grote productstructuren die de low-levelcodelimiet bereiken, de batchverwerking **Low-levelcode berekenen** regelmatig uitvoeren om de structuur te behouden.  

## <a name="see-also"></a>Zie ook

[Ontwerpdetails: Bestelbeleid verwerken](design-details-handling-reordering-policies.md)  
[Ontwerpdetails: Vraag en aanbod afstemmen](design-details-balancing-demand-and-supply.md)  
[Ontwerpdetails: Centrale begrippen van het planningssysteem](design-details-central-concepts-of-the-planning-system.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
