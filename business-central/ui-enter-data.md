---
title: Gegevens invoeren in Business Central
description: 'Er zijn allerlei algemene functies die u helpen gegevens sneller, gemakkelijker en accurater in te voeren. De basisprincipes en geavanceerde functies worden hier beschreven.'
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'decimal separator, data entry, focus'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 03/23/2022
ms.author: jswymer
---
# <a name="entering-data"></a>Gegevens invoeren

Er zijn allerlei algemene functies die u helpen gegevens sneller, gemakkelijker en accurater in te voeren. De basisprincipes en geavanceerde functies voor het invoeren van gegevens worden in dit artikel beschreven.  

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

In de voorbeelden in dit artikel worden de demonstratiegegevens gebruikt.

## <a name="work-with-editable-fields"></a>Werken met bewerkbare velden

Velden in [!INCLUDE[prod_short](includes/prod_short.md)] kunnen verschillende bewerkbare gegevens bevatten, zoals tekst of valutabedragen. Bewerkbare velden geven doorgaans een invoervak weer waarin u kunt typen of een waarde kunt kiezen. Niet-bewerkbare velden worden doorgaans weergegeven met een grijze achtergrond.   

Sommige bewerkbare velden bevatten een kiezer waarmee u een waarde kunt specificeren.  

<!-- TODO: Add illustrations or images of each picker -->
|**Picker**        |**Hoe het u helpt een waarde op te geven**|
|------------------|------------------------------------|
|Datumkiezer       |Deze kiezer geeft een kalender weer die is gebaseerd op uw huidige regionale instellingen. Het helpt u bij het kiezen van een enkele datum.|
|Vervolgkeuzelijst          |Vervolgkeuzelijsten bieden een keuze uit vaste waarden of verwijzen naar records uit een andere tabel|
|Schakelaar of selectievakje|Sommige velden bieden een eenvoudige keuze uit *Ja*- of *Nee*-waarden. De schakelaar wordt gebruikt om deze waarde op te geven en wordt altijd weergegeven als een selectievakje in lijsten|
|AssistEdit       |Sommige velden bieden aangepaste kiezers die geschikt zijn om de beste waarde op te zoeken en voor dat veld te kiezen, zoals een pop-upvenster|

### <a name="modifying-a-field-value"></a>Een veldwaarde wijzigen

Om de waarde van een veld te wijzigen, moet u eerst de focus op dat veld instellen. U stelt de focus in door de volgende acties uit te voeren:

- Gebruik de <kbd>Tab</kbd>-toets. De actie selecteert de volledige waarde.
- Klik met de linkerknop van de muis of vergelijkbaar invoerapparaat. Deze actie selecteert alleen de volledige veldwaarde als het veld in een lijst staat.  

Wanneer u interactie hebt met velden in de gebruikersinterface, selecteert [!INCLUDE[prod_short](includes/prod_short.md)] meestal de volledige veldwaarde, zodat u die gemakkelijker kunt vervangen.

Wanneer de volledige veldwaarde is geselecteerd:
- Vervang de waarde door gewoon te typen om een nieuwe waarde op te geven. Als het veld een kiezer biedt, kunt u deze activeren met de sneltoets <kbd>Alt</kbd>+<kbd>Pijl-omlaag</kbd>.
- Gebruik de toets <kbd>Delete</kbd> of <kbd>Backspace</kbd> om de waarde te wissen.

selecteer de toets <kbd>F2</kbd> om te wisselen tussen het selecteren van de volledige veldwaarde of het plaatsen van de cursor achter de veldwaarde. Door de cursor aan het einde van de waarde te plaatsen, kunt u gemakkelijker aan de bestaande waarde toevoegen.

Als de cursor wordt weergegeven aan het einde van de veldwaarde:
- Voeg toe aan de waarde door gewoon te typen.
- Gebruik de toetsen <kbd>Home</kbd>, <kbd>End</kbd>, <kbd>Pijl-links</kbd> en <kbd>Pijl-rechts</kbd> om de cursor binnen de waarde te verplaatsen. Als u een veld in een lijst bewerkt en u nogmaals u de toets <kbd>Pijl-links</kbd> selecteert wanneer de cursor aan het begin van de waarde staat, wordt de focus ingesteld op het vorige veld. Als u nogmaals de toets <kbd>Pijl-rechts</kbd> selecteert wanneer de cursor aan het einde van de waarde staat, wordt de focus op het volgende veld gezet.

> [!NOTE]
> Nadat u een waarde hebt opgegeven, controleert Business Central pas of deze geldig is nadat u buiten het veld hebt geklikt of de focus hebt ingesteld op een ander element, zoals het volgende veld.  

[!INCLUDE [background_doc_journal_check](includes/background_doc_journal_check.md)]

## <a name="keyboard-shortcuts"></a>Toetsenbordsneltoetsen

Er zijn verschillende sneltoetsen waarmee u "muisvrij" kunt werken en uw gegevensinvoer kunt versnellen. Deze sneltoetsen zijn vooral handig bij grootschalige invoer en herhaalde typetaken.

Zie voor meer informatie over sneltoetsen [Toetsenbordsneltoetsen](keyboard-shortcuts.md). Enkele sneltoetsen worden in dit artikel besproken.

## <a name="accelerating-data-entry-using-quick-entry"></a><a name="QuickEntry"></a>Gegevensinvoer versnellen met snelinvoer

Snelinvoer is een functie die bedoeld is voor gegevensinvoer met het toetsenbord. Snelinvoer werkt met velden (bijvoorbeeld op kaartpagina's) en in lijsten (rijen en kolommen). Het is handig bij het uitvoeren van repetitieve typetaken waarbij meerdere opeenvolgende records achter elkaar moeten worden gemaakt. Voorbeelden zijn een batch verkooporders of het registreren van nieuwe artikelen.

U kunt de Tab-toets gebruiken om van het ene veld op een pagina naar het volgende bewerkbare veld te navigeren. Het nadeel van het gebruik van de Tab-toets is dat deze altijd naar het volgende veld gaat. <!-- even if the field is non-editable or seldom filled it in.-->Met snelinvoer kunt u dit pad wijzigen. Met snelinvoer kunt u <kbd>Enter</kbd> gebruiken om alleen door de velden te navigeren waarin u geïnteresseerd bent. Snelinvoer slaat niet-bewerkbare velden en velden die u normaal gesproken niet invult, over. U hebt dit gedrag mogelijk al op bepaalde pagina's opgemerkt. Dit komt omdat de velden die moeten worden opgenomen wanneer op Enter wordt gedrukt en die worden overgeslagen, vooraf is gedefinieerd. U kunt snelinvoer wijzigen door de werkruimte aan te passen en te optimaliseren hoe u gegevens op elke pagina invoert.

### <a name="how-quick-entry-works"></a>Hoe snelinvoer werkt

Elk veld kan worden gemarkeerd als zijnde *opgenomen in snelinvoer* of *uitgesloten van snelinvoer*. Velden die zijn opgenomen in snelinvoer, worden in het pad opgenomen wanneer u <kbd>Enter</kbd> selecteert. Velden die zijn uitgesloten van snelinvoer, worden dat niet.

Wanneer u klaar bent met het invoeren van gegevens in een veld, drukt u gewoon op <kbd>Enter</kbd> om de wijzigingen te bevestigen en naar het volgende veld te gaan. Als u de volgorde wilt omkeren en naar het vorige veld wilt gaan, selecteert u <kbd>Shift</kbd>+<kbd>Enter</kbd>. Zie voor meer informatie over sneltoetsen [Sneltoetsen voor snelinvoer voor velden](keyboard-shortcuts.md#QuickEntry).

#### <a name="tips-and-tricks"></a>Tips en trucs

De volgende lijst bevat wat nuttige informatie over het gebruik van snelinvoer.

- Het is beschikbaar voor bewerkbare velden.
- Het werkt ook over kolommen en rijen.
- Het voorkomt geen toegang tot andere elementen van een pagina, zoals acties. Deze elementen zijn nog toegankelijk met behulp van <kbd>Tab</kbd> en <kbd>Shift</kbd>+<kbd>Tab</kbd>.  
- Het is niet vereist dat sneltabbladen worden uitgevouwen om snelle invoer te laten werken. Als het volgende snelinvoerveld zich in een samengevouwen sneltabblad bevindt, wordt dat sneltabblad automatisch uitgevouwen en gaat de focus naar het gekozen veld. [!INCLUDE[prod_short](includes/prod_short.md)] onthoudt dat het sneltabblad de volgende keer dat u de pagina bezoekt, moet worden uitgevouwen.  
- Snelinvoer werkt ongeacht of velden verplicht zijn. Het is dus een goed idee te zorgen dat verplichte velden zijn opgenomen in snelinvoer.
- Standaard worden de meeste velden automatisch opgenomen in snelinvoer. In eerste instantie moet u dus waarschijnlijk velden uitsluiten van snelinvoer.

### <a name="to-change-quick-entry-fields"></a>Snelinvoervelden wijzigen

Om snelinvoer op velden in te stellen, gebruikt u personalisatie.

1. Start personalisatie door het pictogram ![Instellingen](media/ui-experience/settings_icon_small.png "Pictogram Instellingen voor rolcentrum") te selecteren en vervolgens de actie **Personaliseren**.
2. Selecteer een veld dat u wilt wijzigen. Selecteer in lijsten de bijbehorende kolomkop. Kies dan **Opnemen in snelinvoer** of **Uitsluiten van snelinvoer**.

Zie voor meer informatie over personalisatie [Uw werkruimte personaliseren](ui-personalization-user.md).

## <a name="mandatory-fields"></a>Verplichte velden

Wanneer u gegevens invoert op pagina's, zijn bepaalde velden gemarkeerd met een rode asterisk. Het rode sterretje betekent dat het veld moet worden ingevuld om een bepaald proces te voltooien. Een voorbeeld is wanneer u een transactie boekt die de waarde in het veld gebruikt.  

Hoewel een veld verplicht is, wordt u niet gedwongen het veld te vullen voordat u verdergaat naar andere velden of de pagina sluit. De rode asterisk dient alleen als een herinnering dat u wordt geblokkeerd van het voltooien van een bepaald proces.  

## <a name="finding-data-as-you-type"></a>Gegevens zoeken terwijl u typt

 Als u begint met het typen van tekens in een veld, wordt een vervolgkeuzelijst weergeven met de mogelijke veldwaarden. De lijst verandert naarmate u meer tekens typt en u kunt de juiste waarde selecteren wanneer deze wordt weergegeven.  

 Veel velden hebben een knop met een pijl-omlaag die u kunt kiezen. U kunt op de pijl klikken om een lijst met gegevens te krijgen die u in het veld kunt instellen. De knop heeft twee functies, afhankelijk van het type veld:  

- Opzoeken - Hiermee toont u gegevens uit een andere tabel die u in het veld kunt invoeren. U kunt slechts één gegevensitem tegelijk selecteren.  

- Vervolgkeuze - Hiermee toont u de verzameling opties die beschikbaar zijn voor het veld. U kunt slechts één optie tegelijk selecteren.  

## <a name="copying-and-pasting-faq-fields-and-lines"></a>Velden en regels kopiëren en plakken

U kunt een of meer rijen uit een lijst of een enkel veld op een pagina kopiëren. Plak vervolgens wat u hebt gekopieerd op dezelfde pagina, een andere pagina of een extern document. U zou bijvoorbeeld kunnen plakken in Microsoft Excel of Outlook e-mail. Als u wilt kopiëren, selecteert u <kbd>Ctrl</kbd>+<kbd>C</kbd> (cmd+C in macOS) op het toetsenbord. Als u wilt plakken, selecteert u <kbd>Ctrl</kbd>+<kbd>V</kbd> of <kbd>cmd+V</kbd> in macOS.

Als u in een lijst het veld in dezelfde kolom van de bovenliggende rij wilt selecteren en het in de huidige rij wilt plakken, selecteert u <kbd>F8</kbd>.

Zie voor meer informatie [Veelgestelde vragen over kopiëren en plakken](faq-copy-paste.yml).

## <a name="filtering-line-items"></a>Regelitems filteren

Als u wilt beginnen met filteren, selecteert u het pictogram ![Filterdeelvenster](media/open-filter-pane-icon.png "Pictogram Filterdeelvenster") boven aan de lijst of selecteert u <kbd>Shift</kbd>+<kbd>F3</kbd> om het filterdeelvenster te openen. U werkt met het filterdeelvenster zoals met elke andere lijst. Zie [Filteren](ui-enter-criteria-filters.md#filtering) voor meer informatie.

Filteren is met name handig bij het weergeven en analyseren van langere documenten. Stel dat u een geboekte verkoopfactuur opent. Vervolgens filtert u de regelitems om alle regelitems weer te geven met een individuele korting van meer dan 5%. Of u filtert om alleen fietsaccessoires met 'pro' in de naam weer te geven.

## <a name="focusing-on-line-items"></a><a name="Focus"></a>Focussen op regelartikelen

Wanneer u werkt met documenten die een onderdeel met regelitems bevatten, kunt u de weergave overschakelen om alleen de regelitems weer te geven. Voorbeelddocumenten zijn verkooporder of factuurpagina. Het gedeelte met regelitems breidt zich uit zodat het bijna de hele werkruimte in beslag neemt. Het verbergt andere delen van de pagina behalve het actiegebied bovenaan. Deze lay-out geeft u een beter overzicht van de regelartikelen en biedt meer ruimte om ermee te werken.

U profiteert er vooral van wanneer u met grote lijsten met regelitems werkt en u snel gegevens wilt invoeren. Deze functie biedt ook geavanceerde filtermogelijkheden. Net als in andere lijsten wordt bladeren en zoeken door regelitems nog eenvoudiger.

### <a name="switching-the-focus-on-and-off"></a>De focus aan- en uitzetten

Als u zich wilt concentreren op regelartikelen, selecteert u ergens in het regelartikelgedeelte en kiest u vervolgens het ![pictogram Focusmodus](media/focus-mode.png "Pictogram Focusmodus") In de rechterbovenhoek of selecteert u <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>F12</kbd>.

Om terug te gaan naar de normale weergave, kiest u het ![pictogram Focusmodus](media/focus-mode.png "Pictogram Focusmodus") of selecteer <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>F12</kbd> opnieuw.

## <a name="multitasking-across-multiple-pages"></a>Multitasking over meerdere pagina's

U kunt een kaart- of documentpagina openen in een nieuw venster. Door een nieuw venster te openen, kunt u:

- Aan meerdere taken tegelijk werken
- Onderbrekingen van de huidige taak beheren, zoals het aannemen van een inkomend gesprek.
- Een venster open houden voor een lopende taak terwijl u een andere taak in Windows start of voltooit.

Om de huidige kaart of het huidige document in een nieuw venster te openen, kiest u ![Nieuw venster openen](media/open-new-window-icon.png "Pictogram Nieuw venster openen") In de rechterbovenhoek of selecteert u <kbd>Alt</kbd>+<kbd>Shift</kbd>+<kbd>W</kbd>.

<!--
When working on multiple tasks at a time or when managing interruptions to the current task, such as taking an incoming call, you can open a card or document page in a new window. This allows you to keep a window open for an ongoing task while you start or complete another task in one or more other windows.
-->

> [!NOTE]
> Wanneer u andere pagina's opent vanaf een kaart of document dat in een nieuw venster is geopend, worden die pagina's in een nieuw venster geopend, ook al kiest u niet ![Nieuw venster openen](media/open-new-window-icon.png "Pictogram Nieuw venster openen").

> [!NOTE]
> Als u in de Safari-browser werkt, kan een pop-upblokkering ervoor zorgen dat het nieuwe venster niet wordt geopend. Als dit het geval is, geeft u de product-URL op als een toegestane website. Zie voor informatie [Voorkeuren wijzigen in Safari](https://go.microsoft.com/fwlink/?LinkId=2102965).<br /><br />
> Hetzelfde kan gebeuren in andere browsers, zoals Firefox. Zie [Instellingen voor pop-upblokkering in Firefox](https://go.microsoft.com/fwlink/?LinkId=2116400) voor meer informatie.  

Een andere manier om te multitasken is om [!INCLUDE[prod_short](includes/prod_short.md)] te openen op twee of meer browsertabbladen. Wanneer u dit zo doet, moet u een nieuw tabblad maken en vervolgens de URL van het oorspronkelijke tabblad kopiëren en in het nieuwe tabblad plakken. Dit creëert een nieuwe sessie.   

> [!NOTE]
> Gebruik niet de functie **Dupliceren** van de browser om het nieuwe tabblad te maken, omdat hierdoor acties op één tabblad acties op andere tabbladen kunnen blokkeren omdat ze deel uitmaken van dezelfde sessie.

## <a name="entering-quantities-by-calculation"></a>Hoeveelheden invoeren door berekening

Als u getallen in velden voor hoeveelheden invoert, zoals het veld **Hoeveelheid** op een artikeldagboekregel, kunt u de formule invoeren in plaats van de totale hoeveelheid.  

### <a name="examples"></a>Voorbeelden

- Als u 19+19 invoert, wordt het veld berekend als 38.  

- Als u 41-9, wordt het veld berekend als 32.  

- Als u 12*4 invoert, wordt het veld berekend als 48.  

- Als u 12/4 invoert, wordt het veld berekend als 3.  

## <a name="entering-negative-numbers"></a>Negatieve getallen invoeren

U kunt negatieve getallen op twee manieren invoeren. Nummer -20.5 kan worden ingevoerd als:  

- -20,5  

  of
- 20,5-  

In beide gevallen wordt het bedrag als -20,5 geregistreerd.  

Als het laatste teken van de expressie een **+** of een **-** is, wordt de volledige expressie vastgelegd met dat teken. Een voorbeeld: **10-20+** resulteert in 10 en niet -10.  

## <a name="entering-dates-and-times"></a>Datums en tijden invoeren

U kunt datums en tijden invoeren in alle velden die speciaal zijn toegewezen aan datums (datumvelden). U kunt datums met of zonder scheidingstekens invoeren.

> [!NOTE]  
> Hoe u datums en tijden invoert, hangt af van uw instellingen onder **Regio**. Zie voor meer informatie [Basisinstellingen wijzigen](ui-change-basic-settings.md).  

### <a name="entering-dates"></a>Datums invoeren

U kunt de datumkiezer gebruiken om een datum te selecteren in een kalender of u voert handmatig datums in. Deze sectie geeft een kort overzicht van hoe u datums invoert. Zie voor meer informatie [Werken met kalenderdatums en tijden](ui-enter-date-ranges.md).

Voor handmatige datuminvoer kunt u twee, vier, zes of acht cijfers invoeren:  

- Twee cijfers worden geïnterpreteerd als de dag. Het voegt de maand en het jaar van de werkdatum toe.  

- Vier cijfers worden geïnterpreteerd als de dag en de maand. Het voegt het jaar van de werkdatum toe.  

- Als de gewenste datum tussen 01/01/1950 en 31/12/2049 ligt, voer dan het jaar in met twee cijfers. Voer anders het jaar in met vier cijfers.

  > [!NOTE]
  > Als u [!INCLUDE[prod_short](includes/prod_short.md)] on-premises gebruikt, kan het tweecijferige jaarbereik verschillen. Beheerders kunnen het bereik wijzigen met de instelling **CalendarTwoDigitYearMax** van de [!INCLUDE[prod_short](includes/prod_short.md)]-server. Zie [Business Central Server configureren](/dynamics365/business-central/dev-itpro/administration/configure-server-instance#General) voor meer informatie.

U kunt ook een datum als dag van de week invoeren, gevolgd door een weeknummer. Of u kunt een jaar invoeren. Bijvoorbeeld Maa25 of maa25 betekent maandag in week 25.  

U kunt in plaats van een specifieke datum ook een van deze codes invoeren.  

|Code|Resultaat|  
|--------------|----------------|  
|h|Hiermee wordt de datum van vandaag opgegeven (de systeemdatum voor de computer).|  
|p|Hiermee wordt een boekhoudperiode opgegeven, waarbij p de eerste boekhoudperiode is, p2 de tweede boekhoudperiode is, enzovoort. |
|w|Hiermee wordt de werkdatum opgegeven die is ingesteld in de toepassing. Zie [Basisinstellingen wijzigen](ui-change-basic-settings.md) als u de werkdatum wilt wijzigen. Het gebruik van een werkdatum is handig als u veel transacties hebt met een andere datum dan de huidige.|
|u|Hiermee wordt opgegeven dat de datum na u een ultimodatum is, bijvoorbeeld U311201.|  

## <a name="entering-times"></a>Tijden invoeren

Hoewel het niet vereist is, kunt u bij de invoer van tijden elk willekeurig scheidingsteken tussen de eenheden plaatsen. U hoeft geen minuten, seconden of AM/PM-aanduiding in te voeren.  

In de volgende tabel wordt aangegeven op welke manieren u tijden kunt invoeren en hoe de invoer wordt geïnterpreteerd.  

|Post|Interpretatie|  
|---------------|------------------------|  
|5|05:00:00|  
|5:30|05:30:00|  
|0530|05:30:00|  
|5:30:5|05:30:05|  
|053005|05:30:05|  
|5:30:5.50|05:30:05,5|  
|053005050|05:30:05.05|  

 Als u geen scheidingsteken invoert, voert u twee cijfers in voor elke tijdseenheid.  

## <a name="entering-combined-datetimes"></a>Gecombineerde datums en tijden invoeren

[!INCLUDE [datetimes](includes/datetimes.md)]

## <a name="entering-duration"></a>Duur invoeren

De duur moet worden ingevoerd als een getal gevolgd door de eenheid.  

Hier volgen enkele voorbeelden.  

|Duur|Maateenheid**|  
|------------------|-------------------------|  
|2u|2 uur|  
|6u 30 m|6 uur en 30 minuten|  
|6,5u|6 uur en 30 minuten|  
|90m|1 uur en 30 minuten|  
|2d 6u 30m|2 dagen, 6 uur en 30 minuten|  
|2d 6u 30m 56s 600ms|2 dagen, 6 uur, 30 minuten, 56 seconden en 600 milliseconden|  

 Als u een getal invoert, wordt het getal automatisch omgezet naar een duur. Dit gebeurt op basis van de standaardeenheid die in het veld Duur is ingevoerd.  

 Als u wilt nagaan welke maateenheid wordt gebruikt in het veld Duur, voert u een getal in en bekijkt u in welke eenheid het getal wordt omgezet.  

 Het getal 5 wordt omgezet in 5 uur, als de eenheid uit uren bestaat.  

## <a name="setting-the-decimal-separator-used-by-numeric-keyboards"></a><a name="decimal"></a>Het decimale scheidingsteken instellen dat wordt gebruikt door numerieke toetsenborden

Wanneer u de <kbd>decimaaltekentoets</kbd> op een numeriek toetsenbord gebruikt om gegevens in te voeren, wordt het daadwerkelijke decimaalteken dat in het veld wordt ingevoerd, bepaald door uw regio-instelling in Business Central. De meeste regio's gebruiken de punt (.) of komma (,) als scheidingsteken voor decimale waarden, zoals normaal gesproken wordt gebruikt in valutabedragen. De decimale toets op uw toetsenbord past zich aan uw regio aan. Dit wijkt vaak af van de punt- of kommatoetsen op de rest van het toetsenbord. U stelt de regio in Business Central in op de pagina **Mijn instellingen**.

Stel dat u een numeriek toetsenbord gebruikt dat een punt (.) als <kbd>decimaalteken</kbd> gebruikt. Maar u voert gegevens in voor een regionale taal die een komma gebruikt (**,**) voor het decimaalteken, zoals Frans (Frankrijk). U wilt dus dat decimalen zoals "1.23" worden ingevoerd als "1,23". In dit geval kunt u naar de pagina **Mijn instellingen** gaan en de **Regio** instellen op de regionale doeltaal, zoals **Frans (Frankrijk)**. Zie voor meer informatie [Basisinstellingen wijzigen](ui-change-basic-settings.md#region).

> [!TIP]
> Het kan voorkomen dat u het decimaalteken wilt gebruiken om een punt (.) in te voeren. Stel dat u bijvoorbeeld een datumbereik invoert in een filter, zoals `01/01/2022..04/01/2022`, of iets dat een punt vereist. Selecteer in dit geval de toetsen <kbd>Alt</kbd>+<kbd>Decimaalteken</kbd> op het numerieke toetsenbord. Deze toetsencombinatie wisselt voor het decimaalteken tussen een punt en het decimaalteken zoals bepaald door de instelling **Regio**.

## <a name="see-also"></a>Zie ook

[Lijsten sorteren, doorzoeken en filteren](ui-enter-criteria-filters.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
