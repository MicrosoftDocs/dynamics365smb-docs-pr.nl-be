---
title: Informatie over het berekenen van vaste verrekenprijzen
description: In een vaste-verrekenprijssysteem wordt de voorraadkostprijs bepaald op basis van redelijkerwijs te verwachten of historische kosten.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 5841
ms.author: bholtorf
ms.date: 10/10/2023
---
# <a name="about-calculating-standard-cost"></a>Informatie over het berekenen van vaste verrekenprijzen

Veel productiebedrijven kiezen een waarderingsbasis voor de vaste verrekenprijs. Dit geldt ook voor bedrijven die lichte productie zoals assemblage en kitting uitvoeren. In een vaste-verrekenprijssysteem wordt de voorraadkostprijs bepaald op basis van redelijkerwijs te verwachten of historische kosten. Onderzoek van in het verleden gebruikte en voor de toekomst geschatte kosten vormen de basis voor de vaste verrekenprijs. Deze prijs ligt vast totdat wordt besloten deze prijs te wijzigen. Het is mogelijk dat de feitelijke productiekosten van een product afwijken van de geschatte vaste verrekenprijs. Vanuit managementoverwegingen wordt de feitelijke prijs voor een bepaald artikel vergeleken met de vaste verrekenprijs en worden eventuele *verschillen* geïdentificeerd en geanalyseerd.  

Vaste verrekenprijzen kunnen worden gehanteerd voor artikelen die worden aangevuld via inkoop, assemblage en productie. Voor elke aanvullingsmethode kunnen vaste verrekenprijzen uit de volgende elementen bestaan.  

|Aanvullingsmethode|Standaardkostenelementen|  
|--------------------------|----------------------------|  
|**Inkoop**|Directe materiaalkosten en overhead-materiaalkosten indien nodig.|  
|**Assembleren**|Directe materiaalkosten, directe of vaste arbeidskosten en overheadkosten.|  
|**Prod.-order**|Directe materiaalkosten, arbeidskosten, uitbestedingskosten en overheadkosten.|  

## <a name="setting-up-standard-costs"></a>Vaste verrekenprijzen instellen

Aangezien de vaste verrekenprijs van een geproduceerd of geassembleerd artikel uit meerdere kostenelementen bestaat, zoals materiaal-, capaciteits- en uitbestedingskosten (directe kosten en overheadkosten), moet de vaste verrekenprijs worden vastgelegd voor al deze elementen.  

Een productiebedrijf dat vaste verrekenprijzen gebruikt, dient twee accountingtaken uit te voeren:  

- Een vaste verrekenprijs schatten voor een voltooid artikel en deze prijs instellen op de artikelkaart.  
- De feitelijke kosten van de belangrijke kostenelementen vastleggen en toewijzen, en een verantwoording afleggen voor verschillen  

De kosten van alle onderdelen moeten bij elkaar worden opgeteld om de directe kosten van een voltooid artikel te kunnen bepalen. Een geassembleerd of geproduceerd artikel kan halffabricaten bevatten, die ook uit meerdere onderdelen bestaan.  

De volgende belangrijke kostenelementen vormen samen de totale directe kosten van een afgewerkt artikel:  

- Materiaalkosten.  
- Capaciteitskosten.  
- Kosten voor uitbesteden van enkel geproduceerde artikelen.  

### <a name="material-costs"></a>Materiaalkosten

Onder materiaalkosten worden de kosten verstaan die te maken hebben met de subassemblages en de aangeschafte grondstoffen. Materiaalkosten kunnen bestaan uit directe en indirecte kostenelementen.  

- Directe materiaalkosten worden gevormd door een gefactureerd bedrag voor aangeschafte grondstoffen of de verwerkingskosten van een subassemblage.  
- Indirecte materiaalkosten of *overhead* kunnen bijvoorbeeld bestaan uit de opslagkosten voor voltooide artikelen nadat deze zijn geproduceerd.  

De instelling van de materiaalkosten voor aangeschafte artikelen die invloed hebben op directe en indirecte kosten wordt bepaald door de waarderingsmethode die is geselecteerd voor het opgeven artikel. U stelt kostengegevens in voor beide waarderingsmethoden op de artikelkaart. Zie voor meer informatie [Nieuwe artikelen registreren](inventory-how-register-new-items.md).

Ook uitvalkosten (alleen productie) vormen een andere factor die moet worden meegewogen bij de berekening van de totale materiaalkosten. Het uitvallen van een bepaalde hoeveelheid grondstoffen tijdens het assembleren of produceren van artikelen zorgt vaak voor een toename van het aantal onderdelen dat nodig is om het artikel te produceren. Dit leidt tot een toename van de materiaalkosten van de onderdelen die worden gebruikt tijdens het produceren van een hoofdartikel. U kunt uitvalkosten voor materialen instellen in de productiestuklijst of in het bewerkingsplan.  

De materiaalkosten van een geproduceerd artikel kunnen worden weergegeven op twee manieren die overeenkomen met de volgende methoden voor het berekenen van de vaste verrekenprijs.  

|Kostenberekeningsbasis|Berekening van materiaalkosten|  
|----------------------------|-------------------------------|  
|Eén niveau|Geproduceerd artikel is gelijk aan de totale kosten van alle ingekochte of via subassemblage verkregen artikelen op de productiestuklijst van dat artikel.|  
|Alle niveaus of meerdere niveaus|Geproduceerd artikel is de som van de materiaalkosten voor alle subassemblages op de stuklijst van dat artikel en de kosten van alle ingekochte artikelen op de productiestuklijst van dat artikel.|  

### <a name="capacity-costs"></a>Capaciteitskosten

Capaciteitskosten zijn de kosten die te maken hebben met interne kosten voor arbeid en apparatuur. U moet deze kosten voor elke resource (in assemblagebeheer) en werk- of bewerkingsplaats in het bewerkingsplan (in productie) instellen. Net als bij materiaalkosten kunt u directe en indirecte elementen van capaciteitskosten identificeren. De directe kosten van een afdeling kunnen bijvoorbeeld worden gevormd door het vastgestelde tarief voor het uitvoeren van een bepaalde functie. De indirecte kosten van een afdeling kunnen algemene fabrieksonkosten omvatten, zoals verwarming, verlichting en dergelijke. Net als bij de materiaalkosten kunt u capaciteitoverhead uitdrukken als een indirect kostenpercentage of als een vast overheadtarief.  

De instelling van de capaciteitskosten van geassembleerde artikelen bestaat uit de volgende elementen:  

- Directe en indirecte kostprijs van de resource.  
- Soorten vast of direct resourcegebruik.  

De instelling van de capaciteitskosten van geproduceerde artikelen bestaat uit de volgende elementen:  

- Directe en indirecte kostprijs van de bewerkingsplaats of afdeling.  
- Instelling van tijd en lotgrootte.  

Teneinde de standaardcapaciteitskosten te berekenen, moet u de standaardtijdtarieven vaststellen die nodig zijn om bewerkingen uit te voeren in afdelingen en bewerkingsplaatsen. De totale tijd voor het uitvoeren van een bewerking omvat naast de insteltijd en de bewerkingstijd meestal ook de wachttijd na bewerking en de transporttijd.  

U stelt de tarieven voor al deze tijdtypen voor iedere afdeling of bewerkingsplaats in op een afzonderlijke stuklijst.  

> [!NOTE]  
>  Hoewel er tarieven voor de bewerkingstijd worden toegepast per geproduceerd artikel, worden de insteltijdtarieven per lot toegepast. Daarom moet u de insteltijd voor iedere bewerking in de stuklijst evenredig verdelen ten opzichte van de lotgrootte. U geeft de lotgrootte op in het overeenkomstige veld op het sneltabblad **Aanvulling** van de pagina **Artikelkaart**.  

Om insteltijd op het bewerkingsplan aan te geven voor de planning maar deze onkosten niet op te nemen in de berekening van de vaste verrekenprijs, wist u het veld **Kosten inclusief instelling** op de pagina **Productie-instelling**.  

Als van één niveau wordt uitgegaan, zijn dit de arbeidskosten die nodig zijn om het afgewerkte productieartikel te produceren en wordt dit aangegeven op het bewerkingsplan van het productieartikel. Als van meerdere niveaus wordt uitgegaan, zijn dit de capaciteitskosten die voor elk afzonderlijk geproduceerd artikel dat is opgenomen in de stuklijst van het hoofdartikel zijn opgegeven.  

### <a name="subcontractor-costs"></a>Uitbestedingskosten

Onder uitbestedingskosten worden de kosten verstaan die betrekking hebben op services die worden geleverd door externe leveranciers of toeleveranciers van een bedrijf. Net als in het geval van de materiaal- en capaciteitskosten kunnen uitbestedingskosten zowel uit directe kosten als uit overheadkosten bestaan. Directe uitbestedingskosten verwijzen naar de feitelijke tarieven voor elke verschafte service. Overheaduitbestedingskosten kunnen bijvoorbeeld transport- of verwerkingskosten zijn die verband houden met een taak die is uitbesteed.  

Aangezien uitbesteding in feite een externe capaciteit is, stelt u de kosten voor uitbestede services (zowel directe als indirecte kosten) in op de afdelingskaart voor de uitbestedingsbewerking.  

## <a name="updating-standard-costs"></a>De vaste verrekenprijzen aanpassen

Om de vaste verrekenprijs van assemblageartikelen bij te werken of te berekenen, gebruikt u de functie van de artikelkaart.  

Het proces van bijwerken of berekenen van vaste verrekenprijzen bestaat gewoonlijk uit de volgende taken:  

1.  Kosten bijwerken op het niveau van onderdeel en capaciteit. Zie voor meer informatie de batchverwerkingen **Vaste verrekenprijs artikel voorstellen** en **Vaste verrekenprijs capaciteit voorstellen**.  
2.  Het consolideren en berekenen van de materiaal- en capaciteitskosten om de totale assemblage- of productiekosten van de artikelen te berekenen. Zie voor meer informatie [De vaste verrekenprijs van een assemblageartikel berekenen](assembly-how-work-assembly-boms.md#to-calculate-the-standard-cost-of-an-assembly-item).  
3.  De vaste verrekenprijzen implementeren die worden ingevoerd wanneer u de vorige batchverwerkingen uitvoert. De vaste verrekenprijzen worden pas van kracht nadat ze zijn geïmplementeerd. Gebruik de batchverwerking **Vaste verrekenprijswijzigingen doorvoeren**, die de wijzigingen in de standaardkosten voor artikelen bijwerkt met die in de tabel Standaardkostenwerkblad.  
4.  De wijzigingen implementeren om het veld **Kostprijs** op de artikelkaart bij te werken en voorraadherwaardering uit te voeren. Zie [Voorraad herwaarderen](inventory-how-revalue-inventory.md) voor meer informatie.

## <a name="use-batch-jobs-to-update-standard-costs"></a>Batchverwerkingen gebruiken om vaste verrekenprijzen bij te werken
In de volgende secties worden de batchverwerkingen beschreven die u kunt gebruiken om vaste verrekenprijzen bij te werken.
### <a name="suggest-item-standard-cost"></a>Vaste verrekenprijs artikel voorstellen

 Maakt suggesties voor het wijzigen van de kosten en kostenaandelen van vaste verrekenprijzen op artikelkaarten. Nadat de batchverwerking is voltooid, kunt u de resultaten bekijken in het venster Vaste-verrekenprijsvoorstel.

> [!NOTE]  
> Deze batchverwerking is alleen bedoeld voor aangeschafte artikelen. Als u een artikel wilt bijwerken met een productiestuklijst of assemblagestuklijst, moet u eerst alle onderdelen op het prijsvoorstel invoeren en vervolgens de batchverwerking Vaste verrekenprijs berekenen uitvoeren.

Met deze batchverwerking worden alleen suggesties gegenereerd. De voorgestelde wijzigingen worden niet doorgevoerd. Als u tevreden bent met de suggesties en ze wilt implementeren, dat wil zeggen ze bijwerken op de artikelkaarten en ze invoegen in het venster herwaarderingsjournaal, selecteert u Vaste verrekenprijswijzigingen doorvoeren in het venster Vaste-verrekenprijsvoorstel.
#### <a name="options"></a>Opties

**Vaste verrekenprijs:** Voer de correctiefactor in waarmee u de vaste verrekenprijs wilt bijwerken. U kunt ook een afrondingsmethode voor de nieuwe vaste verrekenprijs selecteren. U moet het veld invullen met een decimaal voor de procentuele toename, bijvoorbeeld 1,1.

**Indirecte kosten %**: voer de factor in waarmee u het percentage indirecte kosten wilt bijwerken. U kunt ook een afrondingsmethode voor het nieuwe percentage indirecte kosten selecteren. U moet het veld invullen met een decimaal voor de procentuele toename, bijvoorbeeld 1,1.

**Overheadtarief**: voer de correctiefactor in waarmee u het overheadtarief wilt bijwerken. U kunt ook een afrondingsmethode voor het nieuwe overheadtarief selecteren. U moet het veld invullen met een decimaal voor de procentuele toename, bijvoorbeeld 1,1.

### <a name="suggest-workmach-ctr-std-cost"></a>Vaste verrekenprijs bew.-plaats/afd. voorstellen

Maakt suggesties voor het wijzigen van de kosten en kostenaandelen van standaardkosten op afdelings-, bewerkingsplaats- of resourcekaarten. Nadat de batchverwerking is voltooid, kunt u de resultaten bekijken in het venster **Vaste-verrekenprijsvoorstel**.

Met deze batchverwerking worden alleen suggesties gegenereerd. De voorgestelde wijzigingen worden niet doorgevoerd. Als u tevreden bent met de suggesties en ze wilt implementeren, dat wil zeggen ze bijwerken op de afdelings-/bewerkingsplaats- en resourcekaarten en ze invoegen in het venster Herwaarderingsjournaal, selecteert u **Vaste verrekenprijswijzigingen doorvoeren** in het venster **Vaste-verrekenprijsvoorstel**.

Wanneer u de batchverwerking hebt voltooid en u het effect ervan op de productie of assemblageafdelingen wilt zien, voert u de batchverwerking **Vaste verrekenprijs berekenen** uit om de vaste verrekenprijs voor afdelingen, bewerkingsplaatsen, assemblageresources, productiestuklijsten en assemblagestuklijsten bij te werken.
#### <a name="options-1"></a>Opties
**Vaste verrekenprijs:** Voer de correctiefactor in waarmee u de vaste verrekenprijs wilt bijwerken. U kunt ook een **afrondingsmethode** voor de nieuwe vaste verrekenprijs selecteren. U moet het veld invullen met een decimaal voor de procentuele toename, bijvoorbeeld 1,1.

**Indirecte kosten %**: voer de factor in waarmee u het percentage indirecte kosten wilt bijwerken. U kunt ook een afrondingsmethode voor het nieuwe percentage indirecte kosten selecteren. U moet het veld invullen met een decimaal voor de procentuele toename, bijvoorbeeld 1,1.

**Overheadtarief**: voer de correctiefactor in waarmee u het overheadtarief wilt bijwerken. U kunt ook een afrondingsmethode voor het nieuwe overheadtarief selecteren. U moet het veld invullen met een decimaal voor de procentuele toename, bijvoorbeeld 1,1.

### <a name="post-inventory-cost-to-gl"></a>Voorraadwaarde boeken naar grootboek

 Registreert de aantal- en waardewijzigingen naar de voorraad in de artikelposten en de waardeposten wanneer u voorraadtransacties boekt, zoals verkoopverzendingen of inkoopontvangsten.

Tenzij u het selectievakje **Autom. voorraadwaarde boeken** hebt ingeschakeld in het venster **Voorraadinstellingen**, worden voorraadkosten niet dynamisch in het grootboek opgenomen en wordt COGS niet berekend in verband met een verkoop. Daarom moet u handmatig naar het grootboek boeken door de batchverwerking **Voorraadwaarde boeken naar GB** uit te voeren om het grootboek bij te werken en mogelijk een rapport afdrukken van de waardeposten die zijn geboekt.

De batchverwerking gebruikt waardeposten als basis. Om de te boeken waarde te berekenen, wordt het verschil tussen het veld **Totale werkelijke kosten** en het veld **Vrd.-waarde geboekt** in de waardeposten gebruikt. Als u het selectievakje **Verw. kostprijs naar GB boeken** hebt ingeschakeld in het venster **Voorraadinstellingen**, wordt met de batchverwerking tevens het verschil tussen het veld **Kostenbedrag (Verw.)** en het veld **Verw kstn geb GB (Rappval)** in interimrekeningen in het grootboek.

> [!NOTE]
> Als u het selectievakje **Verw. kostprijs naar GB boeken** niet hebt ingeschakeld in het venster **Voorraadinstellingen**, bevat de laatste sectie van het rapport een lijst met waarden die zijn overgeslagen omdat ze verwachte kosten vertegenwoordigen.

> [!NOTE] 
> Als bij de batchverwerking een fout met betrekking tot dimensies of dimensie-instellingen optreedt, wordt de fout genegeerd en wordt de post naar het grootboek geboekt, waarbij de dimensies van de waardepost worden gebruikt.

Als u wilt voorkomen dat er fouten worden aangetroffen tijdens het uitvoeren van de batchverwerking, kunt u met het rapport **Voorraadkosten naar GB boeken - Controle** alle fouten bekijken die mogelijk kunnen optreden. U kunt vervolgens de fouten corrigeren. Als u daarna de batchverwerking **Voorraadwaarde boeken naar GB** uitvoert, worden alle posten verwerkt.
 
> [!IMPORTANT]  
> Voordat u deze batchverwerking gebruikt, moet u de batchverwerking **Kostprijs herwaarderen - Artikelposten** uitvoeren. Wanneer u vervolgens deze batchverwerking uitvoert, zijn de kosten bijgewerkt die u in het grootboek hebt geboekt.
#### <a name="options-2"></a>Opties

|Optie  |Omschrijving  |
|--------------|---------|
|**Boekingsmethode**|met de batchverwerking kunnen voorraadwaarden naar het grootboek worden geboekt per boekingsgroep of per geboekte post. Als u per post boekt, wordt in detail getoond hoe de voorraad van invloed is op het grootboek, maar worden ook talrijke grootboekposten gemaakt. Als u per boekingsgroep boekt, wordt per boekingsdatum per boekingsgroepcombinatie een grootboekpost gemaakt. Er wordt dus een grootboekpost gemaakt voor elke combinatie van boekingsdatum, bedrijfsboekingsgroep, voorraadboekingsgroep en vestiging. Bovendien worden afzonderlijke grootboekposten gemaakt voor kosten met andere tekens.|
|**Documentnr.**|als u hebt gekozen voor boeking per voorraadboekingsgroep, kunt u in dit veld het documentnummer invullen. Het documentnummer wordt in geboekte posten weergegeven.|
|**Boeken**|Selecteer dit veld als u automatisch naar het grootboek wilt laten boeken bij de batchverwerking. Als u de voorraad niet wilt boeken, wordt tijdens de batchverwerking alleen een controlelijst afgedrukt met de tekst: **Controlelijst (niet geboekt)**.|

### <a name="roll-up-standard-cost"></a>Vaste verrekenprijs berekenen

Berekent de vaste verrekenprijzen van geassembleerde en geproduceerde artikelen. Deze worden beïnvloed door de wijzigingen in de vaste verrekenprijzen van onderdelen die zijn voorgesteld door de batchverwerking **Vaste verrekenprijs artikel voorstellen**. Bovendien worden ze beïnvloed door de wijzigingen in de vaste verrekenprijzen van de productiecapaciteit en assemblageresources die worden voorgesteld door de batchverwerking **Vaste verrekenprijs bew.-plaats/afd. voorstellen**.

Wanneer deze batchverwerkingen zijn voltooid en u de berekening hebt uitgevoerd, worden alle wijzigingen in de vaste verrekenprijzen op het prijsvoorstel ingevoerd in de bijbehorende productie- of assemblagestuklijsten, en worden de verrekenprijzen vereffend op alle stuklijstniveaus.

> [!NOTE] 
> Met deze functie worden alleen de vaste verrekenprijzen op de artikelkaarten berekend, niet die op de SKU-kaarten.

Met deze batchverwerking worden alleen suggesties gegenereerd. De voorgestelde wijzigingen worden niet doorgevoerd. Als de voorstellen naar wens zijn, kunt u deze doorvoeren met de batchverwerking **Vaste verrekenprijswijziging doorvoeren**, waarmee u de artikelkaarten bijwerkt en de voorstellen invoegt in het venster **Herwaarderingsdagboek**. U hebt toegang tot deze batchverwerking vanuit het venster **Vaste verrekenprijsvoorstel**.
#### <a name="options-3"></a>Opties

**Berekeningsdatum**: voer de datum in die geldt voor de versie van de productiestuklijst waarvoor u de berekening wilt uitvoeren.
 
### <a name="implement-standard-cost-change"></a>Vaste verrekenprijswijziging doorvoeren

Hiermee worden de wijzigingen in de vaste verrekenprijs in de tabel **Artikel** bijgewerkt met de wijzigingen in de tabel **Vaste-verrekenprijsvoorstel**. De suggesties voor standaardkostenwijzigingen kunnen worden gemaakt met de batchverwerkingen **Vaste verrekenprijs artikel voorstellen** en/of **Vaste verrekenprijs bew.-plaats/afd. voorstellen**, en ze kunnen ook worden gewijzigd. De inhoud van alle velden in de voorstellen voor wijziging van de vaste verrekenprijs worden overgebracht. Als u suggesties van wijzigingen in de vaste verrekenprijzen implementeert, ziet u ze op de artikelkaart en/of kaarten van de afdeling of bewerkingsplaats. Een herwaarderingsdagboek wordt ook voor u gemaakt om de waarde van de bestaande voorraad bij te werken.
#### <a name="options-4"></a>Opties

**Boekingsdatum**: voer de datum in waarop de herwaardering moet plaatsvinden.

**Documentnr.**: voer het nummer in van de herwaarderingsdagboekregels. Als voor de artikeldagboekbatch een nummerreeks is ingesteld, volgt het documentnummer de posten die zijn gemaakt tijdens het boeken van het herwaarderingsdagboek. Als dat niet het geval is, kunt u zelf een nummer invoeren.

**Artikeldagboeksjabloon**: voer de naam in van de sjabloon voor het herwaarderingsdagboek.

**Artikeldagboekbatch**: voer de naam in van het feitelijke herwaarderingsdagboek

Selecteer **OK** om de batchverwerking te starten. Klik op **Annuleren** om het venster te sluiten als u de batchverwerking nu niet wilt uitvoeren.

## <a name="see-also"></a>Zie ook

[Ontwerpdetails: Waarderingsmethoden](design-details-costing-methods.md)  
[Vaste verrekenprijzen bijwerken](finance-how-to-update-standard-costs.md)  
[Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md)  
[Werken met assemblagestuklijsten](assembly-how-work-assembly-boms.md)  
[Productiestuklijsten maken](production-how-to-create-production-boms.md)  
[Werken met stuklijsten](inventory-how-work-BOMs.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
