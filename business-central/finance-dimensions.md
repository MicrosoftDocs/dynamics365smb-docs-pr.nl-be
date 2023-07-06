---
title: Werken met dimensies om gegevens te volgen en te analyseren
description: 'Gebruik dimensies om posten te categoriseren, bijvoorbeeld per afdeling of project, zodat u gemakkelijker gegevens kunt volgen en analyseren zodat u goede zakelijke beslissingen kunt nemen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/27/2023
ms.custom: bap-template
ms.search.keywords: 'analysis, history, track, business intelligence'
ms.search.form: '408, 479, 480, 481, 484, 536, 537, 538, 539, 540, 541, 542, 543, 544, 545, 548, 560, 562, 564, 567, 568, 577, 578, 580, 699, 1343, 2580, 2581, 2582, 2583, 2584, 2585, 2586, 2587, 2588, 2590, 2591, 2592, 2593, 9083, 9233, 9251, 9252, 9253'
---
# <a name="work-with-dimensions"></a><a name="work-with-dimensions"></a><a name="work-with-dimensions"></a>Werken met dimensies

Dimensies zijn waarden waarmee posten worden gecategoriseerd, zodat u ze kunt bijhouden en analyseren in documenten, zoals verkooporders. Dimensies kunnen bijvoorbeeld aangeven tot welk project of welke afdeling een post behoort.  

Dus in plaats van voor elke afdeling en project aparte grootboekrekeningen in te stellen, kunt u bijvoorbeeld dimensies gebruiken als basis voor analyse en hoeft u geen ingewikkeld rekeningschema te maken. Meer informatie vindt u op [Bedrijfsinformatie](bi.md).

Een ander voorbeeld is een dimensie in te stellen met de naam *Afdeling* en die dimensie vervolgens te gebruiken wanneer u verkoopdocumenten boekt. Zo kunt u BI-programma´s gebruiken om te bekijken welke afdeling welke artikelen heeft verkocht. Hoe meer dimensies u gebruikt, hoe gedetailleerder de rapporten waarop u uw bedrijfsbeslissingen kunt baseren zijn. Eén verkooppost kan zelfs informatie uit meerdere dimensies bevatten, zoals:  

* De rekening waarnaar de artikelverkoop is geboekt.  
* Waar het artikel is verkocht.
* Wie het heeft verkocht.
* Welke klant het heeft gekocht.

## <a name="analyzing-by-dimensions"></a><a name="analyzing-by-dimensions"></a><a name="analyzing-by-dimensions"></a>Analyseren per dimensies

Dimensies spelen een belangrijke rol in bedrijfsinformatie, zoals bij het definiëren van analyseweergaven. Meer informatie vindt u op [Gegevens analyseren per dimensie](bi-how-analyze-data-dimension.md).

> [!TIP]
> Een snelle manier om transactiegegevens te analyseren per dimensie is om de actie **Dimensiefilter instellen** te gebruiken om de totalen per dimensie te filteren in het rekeningschema en op pagina's voor posten.

> [!NOTE]
> Analyseweergaven gebruiken vaak gegevens uit dimensies. Als u ontdekt dat een onjuiste dimensie is gebruikt voor geboekte grootboekposten (GB), kunt u de dimensiewaarden corrigeren en uw analyseweergaven bijwerken. Zo blijven uw financiële rapporten en analyses nauwkeurig. Meer informatie vindt u op [Problemen met dimensies oplossen en dimensies corrigeren](finance-troubleshooting-correcting-dimensions.md#changing-dimension-assignments-after-posting).

## <a name="dimension-sets"></a><a name="dimension-sets"></a><a name="dimension-sets"></a>Dimensiesets

Een dimensieset is een unieke combinatie dimensiewaarden. Deze worden opgeslagen als dimensiesetposten in de database. Elke dimensiesetpost vertegenwoordigt één dimensiewaarde. Bovendien wordt elke dimensieset en de dimensiesetpost daarin geïdentificeerd door een gemeenschappelijke dimensieset-id.  

Wanneer u een dagboekregel, documentkop of documentregel maakt, kunt u een combinatie van dimensiewaarden opgeven. In plaats van elke dimensiewaarde expliciet in de database op te slaan, wordt een dimensieset-id toegewezen aan de dagboekregel, documentkop of documentregel om zo de dimensieset op te geven.  

## <a name="setting-up-dimensions"></a><a name="setting-up-dimensions"></a><a name="setting-up-dimensions"></a>Dimensies instellen

U kunt dimensies en dimensiewaarden definiëren om dagboeken en documenten te categoriseren, zoals verkooporders en inkooporders. U stelt dimensies op de pagina **Dimensies** in. Op deze pagina maakt u één regel voor elke dimensie, zoals *Project*, *Afdeling*, *District* en *Verkoper*.

U stelt ook waarden voor dimensies in. Stel dat waarden de afdelingen van uw bedrijf vertegenwoordigen. Dimensiewaarden kunnen worden ingesteld in een hiërarchische structuur die vergelijkbaar is met het rekeningschema. Dat betekent dat gegevens kunnen worden opgesplitst in verschillende niveaus en dat subsets van dimensiewaarden kunnen worden opgeteld. U kunt zoveel dimensies en dimensiewaarden definiëren als u nodig hebt en iedereen in uw bedrijf kan deze gebruiken.

Wanneer dimensies en waarden worden ingesteld kunt u globale en shortcutdimensies definiëren op de pagina **Grootboekinstellingen**. Deze dimensies zijn dan altijd beschikbaar voor u om te selecteren als velden op journaal- en documentregels en grootboekposten, zonder eerst de pagina **Dimensies** te openen. Meer informatie vindt u in de sectie [Globale dimensies en shortcutdimensies instellen](finance-dimensions.md#to-set-up-global-and-shortcut-dimensions).

* **Globale dimensies** worden als filters gebruikt, bijvoorbeeld in rapporten, batchverwerkingen en XMLports. U kunt slechts twee globale dimensies gebruiken. Kies dus dimensies die u vaak gebruikt.
* **Shortcutdimensies** zijn beschikbaar als velden in dagboeken, en documentregels en posten. U kunt er maximaal acht maken.  

> [!NOTE]
> Nadat u een nieuwe dimensie in een post hebt gebruikt, zoals een regel of een nieuwe record, kunt u de dimensie niet verwijderen, zelfs niet als u de post niet boekt. Dit komt doordat [!INCLUDE[prod_short](includes/prod_short.md)] onmiddellijk een dimensieset voor de regel of record maakt. Meer informatie vindt u in de sectie [Dimensiesets](finance-dimensions.md#dimension-sets).

### <a name="to-set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a><a name="to-set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a><a name="to-set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Standaarddimensies voor klanten, leveranciers en andere accounts instellen

U kunt een standaarddimensie toewijzen voor een specifieke rekening. De dimensie wordt naar het dagboek of document gekopieerd wanneer u het rekeningnummer op een regel invoert, maar u kunt de code op de regel desgewenst verwijderen of wijzigen. U kunt ook een dimensie maken die is vereist om een post te boeken in een specifiek rekeningsoort. > 

> [!NOTE]
> Standaarddimensieprioriteiten openen zich voor scenario's in verkoop en inkoop waaraan u misschien speciale aandacht wilt besteden. Wanneer u standaarddimensieprioriteiten gebruikt voor verkoop- en inkoopdocumenten, beschouwt [!INCLUDE [prod_short](includes/prod_short.md)] altijd de dimensies in de koptekst altijd als afkomstig van de klant of leverancier. Dit geldt voor dimensies die u handmatig of standaard instelt, en is met name relevant wanneer u standaarddimensies gebruikt voor vestigingen en artikelen, maar niet voor klanten of leveranciers.
>
> **Voorbeeld**
>
> U hebt een scenario met de volgende dimensie-instellingen:
>
> * Een klant zonder standaarddimensies
> * Een artikel met ADM als de dimensiewaarde voor de AFDELING-dimensie
> * Een vestiging met PROD als de dimensiewaarde voor de AFDELING-dimensie
> * Standaarddimensieprioriteiten worden ingesteld als Klant > Artikel > Vestiging
>
> Wanneer u in dit scenario een nieuw document maakt, worden dimensies als volgt gebruikt:
>
> * Als u een nieuw document maakt en een vestiging toevoegt, is de standaardwaarde voor nieuwe regels PROD. Wanneer u regels met artikelen toevoegt, behoudt [!INCLUDE [prod_short](includes/prod_short.md)] PROD omdat het uit de koptekst van het document komt.
>
> * Als u een nieuw document maakt en artikelen toevoegt die de ADM-dimensiewaarde hebben, en vervolgens een vestiging specificeert in de koptekst van het document, vraagt [!INCLUDE [prod_short](includes/prod_short.md)] of u de bestaande regels wilt overschrijven omdat er een conflict is.
>
> We raden u aan uw standaarddimensie-instellingen, dimensieprioriteiten en de volgorde waarin u gegevens in documenten invoert, te testen.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Dimensies** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer op de pagina **Dimensies** de relevante dimensie en kies vervolgens de actie **Std. dimensierekeningsoort**.  
3. Vul een regel in voor elke nieuwe standaarddimensie die u wilt instellen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
> Als u een dimensie verplicht wilt maken maar geen standaardwaarde aan de dimensie wilt toewijzen, laat u het veld **Dimensiewaardecode** leeg en selecteert u vervolgens **Code verplicht** in het veld **Waardeboeking**.  

> [!WARNING]  
> Als een rekening wordt gebruikt in een batchverwerking **Wisselkoers herwaarderen** of batchverwerking **Voorraadwaarde boeken**, selecteert u **Code verplicht** of **Zelfde code** niet. U kunt geen dimensiecodes gebruiken voor deze batchverwerkingen.  

> [!NOTE]  
> Als een rekening een andere dimensie moet hebben dan de standaarddimensie die aan de rekeningsoort is toegewezen, moet u een nieuwe standaarddimensie voor de rekening instellen. De standaarddimensie voor de rekening vervangt dan de standaarddimensie voor het rekeningtype.  

### <a name="to-set-up-default-dimension-priorities"></a><a name="to-set-up-default-dimension-priorities"></a><a name="to-set-up-default-dimension-priorities"></a>Standaarddimensieprioriteiten instellen

Verschillende rekeningsoorten, bijvoorbeeld een klantrekening en een artikelrekening, kunnen verschillende standaarddimensies hebben. Er kunnen dus meerdere standaarddimensies worden voorgesteld voor een post. Als u dergelijke conflicten wilt voorkomen, kunt u prioriteitregels toepassen op verschillende bronnen.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Standaarddimensieprioriteiten** in en kies vervolgens de gerelateerde koppeling.  
2. Voer op de pagina **Standaarddimensieprioriteiten** in het veld **Broncode** de broncode voor de invoertabel in waarop de prioriteiten voor standaarddimensies van toepassing zijn.  
3. Vul een regel in voor elke prioriteit voor standaarddimensies die u wilt instellen voor de geselecteerde broncode.
4. Herhaal de procedure voor elke broncode waarvoor u prioriteiten voor standaarddimensies wilt instellen.  

> [!IMPORTANT]  
> Als u twee tabellen instelt met dezelfde prioriteit voor dezelfde broncode, selecteert [!INCLUDE[prod_short](includes/prod_short.md)] altijd de tabel met de laagste tabel-id.  

### <a name="to-set-up-dimension-combinations"></a><a name="to-set-up-dimension-combinations"></a><a name="to-set-up-dimension-combinations"></a>Dimensiecombinaties instellen

U kunt bepaalde combinaties van twee dimensies blokkeren of beperken om te voorkomen dat u posten boekt met tegenstrijdige of onjuiste dimensies. Een geblokkeerde dimensiecombinatie betekent dat u beide dimensies niet naar dezelfde post kunt boeken, ongeacht de dimensiewaarden. Daar tegenover betekent een beperkte dimensiecombinatie dat u beide dimensies naar dezelfde post kunt boeken, maar alleen voor bepaalde combinaties van dimensiewaarden.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Dimensiecombinaties** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Dimensiecombinaties** het veld met de gewenste dimensiecombinatie uit de volgende opties.  

    |Veld|Omschrijving|
    |----------------------------------|---------------------------------------|  
    |**Geen beperking**|Deze dimensiecombinatie heeft geen beperkingen. Alle dimensiewaarden zijn toegestaan.|  
    |**Beperkt**|Deze dimensiecombinatie heeft beperkingen afhankelijk van de dimensiewaarden die u invoert. U moet de beperkingen opgeven op de pagina **Dimensiewaardecombinatie**.|  
    |**Geblokkeerd**|Deze dimensiecombinatie is niet toegestaan.|  

3. Als u de optie **Beperkt** hebt geselecteerd, moet u opgeven welke combinaties van dimensiewaarden u wilt blokkeren. Kies hiervoor het veld om de dimensiewaardecombinatie te definiëren.  
4. Selecteer vervolgens de dimensiewaardecombinatie die is geblokkeerd en voer **Geblokkeerd** in het veld in. Met een leeg veld geeft u aan dat de dimensiewaardecombinatie is toegestaan. Herhaal deze stap als meerdere combinaties zijn geblokkeerd.  

> [!NOTE]  
> In rijen en kolommen worden dezelfde dimensies weergegeven, wat inhoudt dat alle dimensiecombinaties twee keer voorkomen. [!INCLUDE[prod_short](includes/prod_short.md)] geeft de instelling automatisch in beide velden weer. U kunt niets in de velden in de linkerbovenhoek en daaronder selecteren, omdat die velden dezelfde dimensie bevatten in de rijen en de kolommen.  
>
> De geselecteerde optie is niet zichtbaar voordat u het veld sluit.  
>
> Als u de naam van de dimensies wilt weergeven en niet de code, klikt u op het veld **Kolomnaam weergeven**.

### <a name="to-set-up-global-and-shortcut-dimensions"></a><a name="to-set-up-global-and-shortcut-dimensions"></a><a name="to-set-up-global-and-shortcut-dimensions"></a>Globale dimensies en shortcutdimensies instellen

Globale dimensies en shortcutdimensies kunnen als filter worden gebruikt in [!INCLUDE[prod_short](includes/prod_short.md)], inclusief in rapporten, batchverwerkingen, pagina's met posten en analyseweergaven. Globale dimensies en shortcutdimensies kunnen altijd direct worden ingevoegd zonder eerst de pagina **Dimensies** te openen. Op dagboek- en documentregels kunt u globale dimensies en shortcutdimensies selecteren in een veld op de regel. U kunt twee globale dimensies en acht shortcutdimensies instellen. Kies de dimensies die u het vaakst gebruikt.

> [!IMPORTANT]
> Het wijzigen van een globale of shortcutdimensie vereist dat alle posten met de dimensie worden bijgewerkt. Als u een globale dimensie wilt wijzigen, kunt u de functie **Globale dimensies wijzigen** gebruiken, maar dat kan enige tijd duren, kan vertragend werken en tabellen kunnen tijdens de update worden vergrendeld. Zorg dat uw globale dimensies en shortcutdimensies zorgvuldig kiest, zodat u deze niet later moet wijzigen. Als u een shortcutdimensie wilt wijzigen, gebruikt u de actie **Dimensies wijzigen**.
>
> Meer informatie vindt u in de sectie [Globale dimensies wijzigen](finance-dimensions.md#to-change-global-dimensions).

> [!NOTE]
> Wanneer u een globale of shortcutdimensie toevoegt of wijzigt, wordt u automatisch afgemeld en weer aangemeld, zodat de nieuwe waarde voorbereid is voor gebruik.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Grootboekinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Vul de velden van het sneltabblad **Dimensies** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="to-change-global-dimensions"></a><a name="to-change-global-dimensions"></a><a name="to-change-global-dimensions"></a>Globale dimensies wijzigen

Wanneer u een globale of shortcutdimensie wijzigt, worden alle met die dimensie geboekte posten bijgewerkt. Omdat dit proces tijdrovend kan zijn en de prestaties kan beïnvloeden, zijn er twee verschillende modi beschikbaar om het proces aan te passen aan de grootte van de database.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Grootboekinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Globale dimensies wijzigen**.
3. Selecteer bovenaan de pagina een van de volgende twee modi voor uitvoering van de batchtaak.

    |Optie|Omschrijving|
    |-|-|
    |**Sequentieel**|(Standaard) De wijziging wordt in één transactie uitgevoerd, waarbij alle posten worden teruggebracht naar de dimensies die ze hadden vóór de wijziging.<br /><br />Deze optie wordt aanbevolen als het bedrijf relatief weinig geboekte posten bevat, in welk geval de uitvoering van de batchtaak zo kort mogelijk duurt. Het proces vergrendelt meerdere tabellen en blokkeert andere gebruikers totdat het klaar is. Let op, bij grote databases kan het proces mogelijk niet worden voltooid in deze modus. Gebruik in dat geval de optie **Parallel**.|
    |**Parallel**|De dimensiewijziging vindt plaats in meerdere achtergrondsessies en de bewerking wordt opgesplitst in meerdere transacties. Om deze optie te gebruiken, zet u de schakelaar **Parallelle verwerking** aan. <br /><br />Deze optie wordt aanbevolen voor grote databases of bedrijven met veel geboekte posten, omdat de voltooiing ervan zo kort mogelijk duurt. Let op, in deze modus start het updateproces niet als er meer dan één actieve databasesessie is.|  

4. Voer in de velden **Code globale dimensie 1** en/of **Code globale dimensie 2** de nieuwe dimensiecode(s) in. De huidige afmetingen worden grijs weergegeven achter de velden.
5. Voer, afhankelijk van de modus, een van de volgende handelingen uit:
    * Kies in de modus **Sequentieel** de actie **Starten**.
    * Kies in de modus **Parallel** de actie **Voorbereiden**.

    Het tabblad **Logposten** wordt gevuld met informatie over de dimensies die worden gewijzigd.
6. Meld u af bij [!INCLUDE[prod_short](includes/prod_short.md)] en meld u vervolgens weer aan.
7. Kies de actie **Starten** om de parallelle verwerking van de dimensieveranderingen te starten.

### <a name="example-of-dimension-setup"></a><a name="example-of-dimension-setup"></a><a name="example-of-dimension-setup"></a>Voorbeeld van dimensie-instelling

Stel dat uw bedrijf transacties wil traceren op basis van organisatorische structuur en geografische locaties. Daarvoor kunt u twee dimensies instellen op de pagina **Dimensies**:

* **DISTRICT**  
* **AFDELING**  

| Code | Name | Codebijschrift | Filterbijschrift |
| --- | --- | --- | --- |
| DISTRICT |District |Districtcode |Districtfilter |
| KSTNPLAATS |Kostenplaats |Afdelingscode |Kostenplaatsfilter |

Voeg voor **DISTRICT** de volgende dimensiewaarden toe:

| Code | Naam | Dimensiewaardesoort |
| --- | --- | --- |
| 10 |Noord- en Zuid-Amerika |Begintotaal |
| 20 |Noord-Amerika |Standaard |
| 30 |Stille Oceaan |Standaard |
| 40 |Zuid-Amerika |Standaard |
| 50 |Noord- en Zuid-Amerika, totaal |Eindtotaal |
| 60 |Europa |Begintotaal |
| 70 |EU |Standaard |
| 80 |Niet-EU |Standaard |
| 90 |Europa, totaal |Eindtotaal |

Voor de twee belangrijke geografische gebieden, Noord- en Zuid-Amerika en Europa, voegt u subcategorieën toe voor regio's door de dimensiewaarden te laten inspringen. Zo kunt u rapporteren over verkoop of kosten in regio's en totalen ophalen voor de grotere geografische gebieden. U kunt er ook voor kiezen landen, regio's, provincies of steden te gebruiken als uw dimensiewaarden. Dit hangt af van uw bedrijf.

> [!NOTE]  
> Als u een hiërarchie wilt instellen, moeten de codes op alfabetische volgorde staan Dit omvat de codes van de dimensiewaarden die zijn opgegeven in [!INCLUDE[prod_short](includes/prod_short.md)].  

Voeg voor **AFDELING** de volgende dimensiewaarden toe:

| Code | Naam | Dimensiewaardesoort |
| --- | --- | --- |
| ADMIN |Beheer |Standaard |
| PROD |Productie |Standaard |
| VERKOOP |Verkoop |Standaard |

Met deze instellingen kunt u uw twee dimensies toevoegen als twee globale dimensies op de pagina **Grootboekinstellingen**. Dit betekent dat u DISTRICT en AFDELING kunt gebruiken als filters voor grootboekposten en voor alle rapporten. Beide globale dimensies kunnen ook automatisch worden gebruikt als shortcutdimensies in postregels en documentkoppen.

## <a name="getting-an-overview-of-dimensions-used-multiple-times"></a><a name="getting-an-overview-of-dimensions-used-multiple-times"></a><a name="getting-an-overview-of-dimensions-used-multiple-times"></a>Een overzicht krijgen van dimensies die meerdere keren zijn gebruikt

Op de pagina **Standaarddimensies - Multi** wordt opgegeven hoe een groep rekeningen gebruikmaakt van dimensies en dimensiewaarden. U kunt dit instellen door meerdere rekeningen te markeren en er vervolgens standaarddimensies en dimensiewaarden voor op te geven. Daarna stelt de toepassing automatisch deze dimensies en dimensiewaarden voor wanneer een van deze rekeningen wordt gebruikt, bijvoorbeeld op een dagboekregel. Dit maakt het boeken van een post eenvoudiger voor de gebruiker, omdat de dimensievelden automatisch worden ingevuld. Let echter wel ook op dat de voorgestelde dimensiewaarden kunnen worden gewijzigd, bijvoorbeeld op een dagboekregel.

De pagina **Standaarddimensies - Multi** bevat de volgende velden:

|Veld|Omschrijving|
|-----|-----------|  
|**Dimensiecode**|Bevat alle dimensies die zijn ingesteld als standaarddimensies in een of meer gemarkeerde rekeningen. Kies dit veld voor een overzicht van de beschikbare dimensies. Als u een dimensie selecteert, wordt die dimensie voor de gemarkeerde rekeningen ingesteld als standaarddimensie.|
|**Dimensiewaardecode**|Bevat een dimensiewaarde of de term (Conflict). Als het veld een dimensiewaarde bevat, hebben de gemarkeerde rekeningen dezelfde standaard dimensiewaarde voor een dimensie. Bevat het veld de term (Conflict), dan hebben niet alle gemarkeerde rekeningen dezelfde standaard dimensiewaarde voor een dimensie. Zodra u het veld **Dimensiecode** kiest, ziet u een overzicht van alle beschikbare dimensiewaarden voor een dimensie. Als u een dimensiewaarde selecteert, wordt deze ingesteld als standaard dimensiewaarde voor de gemarkeerde rekeningen.|
|**Waardeboeking**|Bevat een regel voor waardeboeking of de term (Conflict). Als het veld een regel voor waardeboeking bevat, hebben de gemarkeerde rekeningen dezelfde regel voor waardeboeking voor een dimensiewaarde. Bevat het veld de term (Conflict), dan hebben niet alle gemarkeerde rekeningen dezelfde regel voor waardeboeking voor een dimensiewaarde. Zodra u het veld **Waardeboeking** kiest, ziet u een overzicht van de regels voor waardeboeking voor een dimensie. Als u een regel voor waardeboeking selecteert, wordt deze toegepast op alle gemarkeerde rekeningen.|

## <a name="use-dimensions"></a><a name="use-dimensions"></a><a name="use-dimensions"></a>Dimensies gebruiken

In een document zoals een verkooporder kunt u dimensiegegevens toevoegen voor een afzonderlijke documentregel en voor het document zelf. Op de pagina **Verkooporder** zou u dus dimensiewaarden kunnen invoeren voor de eerste twee shortcutdimensies op de afzonderlijke verkoopregels en vervolgens meer dimensiegegevens toevoegen als u de knop **Dimensies** kiest.  

Als u in plaats daarvan in een dagboek werkt, kunt u ook op dezelfde manier dimensiegegevens toevoegen aan een post als u shortcutdimensies direct als velden hebt ingesteld op dagboekregels.  

U kunt ook standaarddimensies instellen voor rekeningen of rekeningsoorten, zodat dimensies en dimensiewaarden automatisch worden ingevuld.

### <a name="to-view-global-dimensions-in-ledger-entry-pages"></a><a name="to-view-global-dimensions-in-ledger-entry-pages"></a><a name="to-view-global-dimensions-in-ledger-entry-pages"></a>Globale dimensies bekijken op pagina's met posten

Globale dimensies zijn altijd gedefinieerd en benoemd door het bedrijf. Als u de globale dimensies voor het bedrijf wilt bekijken, opent u de pagina **Boekhoudinstellingen**.

Op een pagina met posten kunt u bekijken of er globale dimensies van toepassing zijn op de posten. In tegenstelling tot uw andere dimensies kunnen de twee globale dimensies overal in [!INCLUDE[prod_short](includes/prod_short.md)] als filter worden toegepast.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Rekeningschema** in en kies de gerelateerde koppeling.  
2. Kies op de pagina **Rekeningschema** de actie **Posten**.  
3. Stel een of meer filters op de pagina in om alleen de gewenste posten weer te geven.  
4. Als u alle dimensies voor een post wilt zien, selecteert u de post en kiest u vervolgens de actie **Dimensies**.  

> [!NOTE]  
> Op de pagina **Postdimensies** worden de dimensies per post weergegeven. Als u de posten doorloopt, ziet u dat de inhoud op de pagina **Postdimensies** hieraan aangepast.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/modules/dimensions-dynamics-365-business-central/index)

## <a name="see-also"></a><a name="see-also"></a><a name="see-also"></a>Zie ook

[Bedrijfsinformatie](bi.md)  
[Financiën](finance.md)  
[Gegevens analyseren per dimensie](bi-how-analyze-data-dimension.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
