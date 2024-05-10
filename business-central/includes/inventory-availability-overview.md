---
author: brentholtorf
ms.topic: include
ms.date: 04/23/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

Verhoog de efficiëntie in uw magazijn met nauwkeurige, realtime informatie over factoren die de beschikbare hoeveelheden kunnen beïnvloeden. Voorbeeld: 

* Voorraadniveaus
* Locaties
* Verwerkingsstadia
* Quarantaineartikelen
* Reserveringen

U kunt informatie over de beschikbaarheid van artikelen opvragen via de volgende brondocumenten:

* Verkooporders
* Productieorders
* Assemblageorders
* Projecten

De informatie houdt ook rekening met andere factoren die de beschikbaarheid beïnvloeden. Bijvoorbeeld toegewezen opslaglocaties, afgesloten opslaglocaties en artikelen die niet beschikbaar zijn voor picken. Artikelen kunnen bijvoorbeeld zijn gereserveerd of in afwachting van opslag of verzending zijn. Met de pagina **Overzicht van pick** kunt u de items bekijken die [!INCLUDE [prod_short](prod_short.md)] niet heeft opgenomen in pickdocumenten en de nodige acties ondernemen.

> [!NOTE]
> Deze mogelijkheid vereist dat u de schakelaar **Gestuurde opslag en pick** aanzet voor de vestigingen die u gebruikt in uw pickproces.

### <a name="set-up-previews"></a>Voorbeelden instellen

Voor meer informatie over wat er wel en niet wordt gepickt, schakelt u de optie **Overzicht weergeven (gestuurde opslag en pick)** in op de aanvraagpagina **Mag. - Document maken** of **Mag.-verzending - Pick maken**.

### <a name="determine-the-quantity-you-can-pick"></a>De hoeveelheid bepalen die u kunt picken

Op regels op de pagina **Overzicht van magazijnpick maken** toont het veld **Te verwerken hoeveelheid (basis)** welke en hoeveel artikelen [!INCLUDE [prod_short](prod_short.md)] probeerde te picken. Het feitenblok **Overzicht** biedt meer details.

Voor eenvoudige onderzoeken geeft de **Pickbare hoev.** wellicht voldoende informatie. In het veld wordt weergegeven hoeveel artikelen er beschikbaar zijn. Als de pickbare hoeveelheid minder is dan verwacht, onderzoek dan de inhoud van de opslaglocatie.

De **Pickbare hoev.** is de maximale hoeveelheid die [!INCLUDE [prod_short](prod_short.md)] in aanmerking kan nemen voor picken. Deze hoeveelheid bestaat uit artikelen in pickbare opslaglocaties. De hoeveelheid omvat geen hoeveelheden die zich in geblokkeerde of toegewezen opslaglocaties bevinden, of artikelen die worden gepickt in magazijnpickdocumenten. Als het artikel dat u wilt picken artikeltracering vereist, worden geblokkeerde partij- of serienummers die zijn opgeslagen in pickbare opslaglocaties, uitgesloten van de pickbare hoeveelheid.

Als de pickbare hoeveelheid afwijkt van de hoeveelheid in de pickbare opslaglocaties, is er mogelijk een probleem. Verken de opslaglocatie-inhoud om geblokkeerde opslaglocaties of hoeveelheden in actieve documenten te vinden.

In het veld **Hoev. in magazijn** wordt de totale hoeveelheid weergegeven die u in uw magazijn aantreft als u een fysieke telling uitvoert. Vanuit dit veld kunt u inzoomen op de magazijnposten. Als in het veld een hoeveelheid wordt weergegeven die kleiner is dan de hoeveelheid in **Hoev. in pickbare opslaglocaties**, is er sprake van een verkeerde afstemming tussen de magazijn- en voorraadhoeveelheden. Gebruik in dat geval de actie **Magazijnherwaardering berekenen** op de pagina **Artikeldagboek** en maak vervolgens de magazijnpick opnieuw.

De volgende afbeelding illustreert de maximale hoeveelheid die in aanmerking komt voor picking.

:::image type="content" source="../media/pickable-qty.png" alt-text="Maximale hoeveelheid die in aanmerking komt voor picking.":::

**Legenda**

|Letter  |Omschrijving  |
|---------|---------|
|P     |Opslaglocaties met inhoud van het type Pick         |
|D     |Opslaglocaties met inhoud van het type Pick gemarkeerd als toegewezen opslaglocaties        |
|A     |Opslaglocaties met inhoud van het type Pick in de actieve documenten (zoals een andere pick)       |
|T     |Opslaglocaties met inhoud van het type Pick met artikelen met geblokkeerde tracering         |
|B     |Opslaglocaties met inhoud van het type Pick met geblokkeerde uitgaande verplaatsing         |
|O     |Overige opslaglocaties         |

### <a name="reservations"></a>Reserveringen

Als er reserveringen zijn voor het artikel dat wordt gepickt, gaat de berekening verder. Het idee is dat gereserveerde vraag een hogere prioriteit heeft dan niet-gereserveerde vraag, wat betekent dat picken voor niet-gereserveerde vraag niet mag verhinderen dat er later voor gereserveerde vraag wordt gepickt.

Om te controleren of uw hoeveelheid aan een vraag kan voldoen, vergelijkt u de waarde **Pickbare hoev.** in het feitenblok **Overzicht** met de waarde in het veld **Te verwerken hoeveelheid (basis)** op de regels.

U vindt reserveringen in het veld **Totaal gereserveerde hoev. in magazijn**. Gereserveerde hoeveelheden die al zijn gepickt en gereed zijn voor verzending, gebruik of verbruik, hebben geen invloed op de beschikbaarheid. Het veld **Gereserveerde hoev. in pick-/verzendopslaglocaties** toont deze hoeveelheid.

Het veld **Beschikbare hoev. exclusief verzendopslaglocatie** toont de hoeveelheid die beschikbaar is, met uitzondering van hoeveelheden waarvoor het volgende geldt:

* Ze zijn al gepickt voor verzendingen.
* Ze bevinden zich in geblokkeerde artikelpartijen of serienummers.
* Ze zitten in geblokkeerde opslaglocaties.
* Ze zitten in speciale opslaglocaties.

Deze hoeveelheden zijn mogelijk beschikbaar, maar u kunt ze mogelijk nog niet picken. Ze kunnen zich nog steeds in de ontvangst-, opslag- of kwaliteitscontroleruimte bevinden. U kunt ze naar het pickgebied verplaatsen door een opslag- of verplaatsingsvoorstel te verwerken.

Het verschil tussen **Beschikbare hoev. exclusief verzendopslaglocatie** en gereserveerde hoeveelheid in het magazijn is de hoeveelheid die beschikbaar is voor picken zonder dat dit invloed heeft op de gereserveerde voorraad.

De volgende afbeelding illustreert de toewijzing van beschikbare hoeveelheid aan gereserveerde hoeveelheid.

:::image type="content" source="../media/Warehouse_Reservation_Pick.png" alt-text="Maximale hoeveelheid die in aanmerking komt voor picken als er sprake is van een reservering.":::

**Legenda**

|Letter  |Omschrijving  |
|---------|---------|
|P     |Te picken hoeveelheid         |
|TR    |Totaal gereserveerde hoev. in magazijn.         |
|RS    |Gereserveerde hoeveelheden die al zijn gepickt en gereed zijn voor verzending, gebruik of verbruik       |
|A     |Beschikbare hoev. exclusief verzendopslaglocatie         |
|B     |Hoeveelheid in speciale of geblokkeerde opslaglocaties, geblokkeerde artikelpartijen of serienummers         |

Hoewel er voldoende beschikbare hoeveelheid in het magazijn is om volledig aan de pick te voldoen, zal dit ertoe leiden dat de totale gereserveerde hoeveelheid wordt toegewezen aan de hoeveelheden in speciale of geblokkeerde opslaglocaties, waardoor picken voor deze vraag wordt voorkomen. Omdat de gereserveerde vraag een hogere prioriteit heeft, vermindert [!INCLUDE [prod_short](prod_short.md)] de te verzamelen hoeveelheid om negatieve gevolgen, zoals het onvermogen om te picken, op de gereserveerde vraag te voorkomen.

### <a name="other-details"></a>Overige details

Als voor artikelen artikeltracering vereist is, kunt u de hoeveelheid ook vinden in geblokkeerde partijen of serienummers, wat de volgende reducties veroorzaakt:

* De pickbare hoeveelheid
* Beschikbare hoeveelheid exclusief verzendopslaglocatie
* De gereserveerde hoeveelheid in het magazijn 

Als u hetzelfde artikel pickt voor meerdere brondocumenten of regels, wat ook het geval is wanneer u serienummers pickt, wordt er ook informatie over picks voor andere regels weergegeven omdat hierdoor de pickbare hoeveelheid wordt verminderd.
