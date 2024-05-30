---
title: Pagina's personaliseren (bevat video)
description: Leer hoe u de gebruikersinterface kunt aanpassen en uw werkruimte kunt aanpassen aan uw manier van werken en persoonlijke voorkeuren in Business Central.
author: jswymer
ms.topic: conceptual
ms.service: dynamics-365-business-central
ms.custom: bap-template
ms.reviewer: jswymer
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields, resize column, change column width'
ms.search.form: '9020, 9022, 9026, 9027, 9030, 9000, 9009, 9004, 9005, 9024, 9006, 9007, 9010, 9016, 9017'
ms.date: 01/15/2024
ms.author: jswymer
---
# <a name="personalize-your-workspace"></a>Uw werkruimte personaliseren

U kunt uw werkruimte aanpassen aan uw werk en voorkeuren. Wijzig pagina's zodat ze alleen de informatie weergeven die u nodig hebt, waar u die nodig hebt. Personalisatie heeft alleen invloed op uw werkruimte. Het verandert niets aan hoe anderen werken. U kunt alle soorten pagina's personaliseren, inclusief de pagina [Rolcentrum](ui-change-basic-settings.md#role-center).

> [!NOTE]
> Vanwege beperkingen op ontwerpmogelijkheden in de webclient is het momenteel niet mogelijk om de besturingselementen binnen de `grid`- en `fixed`-syntaxis aan te passen of te personaliseren.
Het geldt voor alle ontwerpmodi, niet alleen voor personalisatie.

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

U kunt verschillende wijzigingen aanbrengen, zoals velden, kolommen, acties en hele delen verplaatsen of verbergen, en nieuwe velden toevoegen. De meeste personalisatie moet worden gedaan door eerst de banner **Personaliseren** te activeren. U kunt eenvoudige aanpassingen, zoals de kolombreedte, direct in elke lijst maken.

> [!NOTE]
> Beheerders kunnen dezelfde indelingswijzigingen maken als gebruikers door het profiel (de rol) aan te passen dat aan meerdere gebruikers is toegewezen. Ga voor meer informatie over pagina's voor rollen naar [Pagina's aanpassen voor rollen](ui-personalization-manage.md)<br /><br />
Beheerders kunnen ook personalisering van gebruikers overschrijven of uitschakelen en ze kunnen definiëren welke functies zelfs door gebruikers in alle of specifieke bedrijven kunnen worden gezien. Zie [Business Central aanpassen](ui-customizing-overview.md) voor meer informatie.

## <a name="video"></a>Video

De volgende video toont enkele manieren waarop u uw rolcentrum kunt personaliseren.

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4ArUB?rel=0]

## <a name="change-the-width-of-a-column"></a>De breedte van een kolom wijzigen

U kunt het formaat van kolommen in elke lijst eenvoudig wijzigen. Sleep gewoon de grens tussen twee kolommen naar links of naar rechts.  

1. Selecteer in de koptekst van een lijst de grens tussen twee kolommen.
2. U kunt ook dubbelklikken op de grens tussen twee kolommen om de breedte van de kolom automatisch aan te passen. De breedte wordt aangepast aan de optimale grootte voor leesbaarheid.

Wat betreft andere personalisatie, worden de wijzigingen die u aanbrengt in de kolombreedte opgeslagen in uw account en volgen deze u ongeacht op welk apparaat u zich aanmeldt.

## <a name="start-personalizing-by-using-the-personalization-mode"></a>Begin met personaliseren door de personalisatiemodus te gebruiken

1. Open een pagina die u wilt personaliseren.
1. Selecteer in de rechterbovenhoek het pictogram ![Instellingen.](media/ui-experience/settings_icon_small.png "Pictogram Instellingen voor rolcentrum") en kies vervolgens de actie **Personaliseren**.

    De banner **Personaliseren** verschijnt bovenin, waarmee wordt aangegeven dat u wijzigingen kunt gaan aanbrengen.

    > [!NOTE]
    > Gebruik <kbd>Ctrl</kbd>+<kbd>klik</kbd> op een actie om te navigeren tijdens personalisatie als de actie wordt gemarkeerd door de pijlpunt.

    Als u een ![Personalisatievergrendeling](media/personalization-lock-icon.png "Personalisatievergrendeling") of ![Personalisatie geblokkeerd](media/personalization-blocked-icon.png "Personalisatie geblokkeerd") ziet op de banner, kunt u de pagina niet personaliseren. Zie voor meer informatie [Waarom is een pagina vergrendeld voor personalisatie?](ui-personalization-locked.md).

1. Als u een UI-element wilt wijzigen, wijst u naar het element, zoals een actie, een veld of een onderdeel. Het element wordt onmiddellijk gemarkeerd met een pijlpunt of rand. Kies het element en kies vervolgens **Verplaatsen**, **Verwijderen**, **Verbergen**, **Weergeven**, **Weergeven onder 'Meer tonen'**, **Weergeven wanneer samengevouwen**, **Altijd weergeven**, **Bevroren deelvenster instellen/wissen** of **Opnemen in/Uitsluiten van snelinvoer**, afhankelijk van het type en de status van het UI-element.
1. Als u een veld wilt toevoegen, kiest u de actie **+ Veld**. Sleep vanuit het deelvenster **Veld toevoegen aan pagina** een veld naar de gewenste positie op de pagina.
1. Wanneer u klaar bent met het wijzigen van de indeling van een of meer pagina's, kiest u de knop **Gereed** in de banner **Personaliseren**.

Zie [Wat kunt u personaliseren](#What) voor meer informatie.

## <a name="what-you-can-personalize"></a><a name="What"></a>Wat kunt u personaliseren

|Wat u wilt doen?|Hoe kunt u het doen?|Opmerkingen|
|----|------------|-------|
|Iets zoals een veld, een kolom in een lijst, een tegel, een actie of een onderdeel verplaatsen op de pagina|Wijs naar alles wat u wilt verplaatsen en sleep dit naar de nieuwe positie. De positie wordt aangegeven door een dikke horizontale of verticale lijn.<br /><br />![Pictogram Kan niet hierheen verplaatsen](media/personalization-cannot-move-here.png "Personalisatiemodus - Pictogram Kan niet hierheen verplaatsen") geeft aan dat u het element niet naar de geselecteerde positie kunt verplaatsen.|De onderdelen zijn onderverdelingen of gebieden op een pagina met objecten als meerdere velden, een andere pagina, een grafiek of tegels.<br /><br />[Meer informatie over het personaliseren van acties](#Actions)<br>[Meer informatie over het personaliseren van onderdelen](#Parts)|
|Verberg een element dat momenteel wordt weergegeven, zoals een veld, kolom in een lijst, tegel, actie of onderdeel.|Selecteer het element, selecteer de pijlpunt en selecteer vervolgens <b>Verbergen</b>.|In de personalisatiemodus worden verborgen acties grijs weergegeven met cursieve tekst en worden verborgen delen gearceerd door diagonale lijnen. Verborgen velden en kolommen worden niet direct op de pagina aangegeven, maar u kunt ze vinden via het deelvenster <b>Veld aan pagina toevoegen</b> ([meer informatie over werkvelden](#fields)).<br><br>Wanneer u de personalisatiemodus verlaat, verdwijnen alle elementen uit het zicht. Als het veld dat u verbergt ook in de sneltabbladkop wordt weergegeven wanneer het sneltabblad is samengevouwen, wordt het veld daar niet meer weergegeven.|
|Een actie of onderdeel weergeven dat momenteel verborgen is|Kies voor een grijs (verborgen) element de pijlpunt en kies vervolgens <b>Weergeven</b>.|Het verborgen element is weer zichtbaar.|
|Een veld toevoegen dat momenteel verborgen is|Kies in de banner <b>Personaliseren</b> de actie <b>+ Veld</b>.<br /></br>Het deelvenster <b>Veld aan pagina toevoegen</b> wordt aan de rechterkant van de pagina geopend. Als u een veld in het deelvenster selecteert, wordt de verborgen locatie ervan op de pagina weergegeven.<br /><br />Om een veld toe te voegen, sleept u het vanuit het deelvenster of vanuit de verborgen locatie naar de gewenste positie. De positie wordt aangegeven door een dikke horizontale of verticale lijn.<br><br> Een andere manier is om de pijlpunt op de verborgen locatie van het veld te selecteren en **Weergeven** te selecteren. |Elke pagina bevat een vooraf bepaalde set velden die u kunt laten weergeven.<br /><br />[Meer informatie over werken met velden](#fields) |
|Een veld weergeven in de kop van een sneltabblad wanneer dit is samengevouwen.|Kies de pijlpunt en kies vervolgens <b>Weergeven wanneer samengevouwen</b>. <br /> <br />Als u deze optie niet ziet, is deze al ingesteld. In dit geval kunt u de weergave van het veld in de sneltabbladkop stoppen door <b>Altijd weergeven</b> te kiezen.|*Sneltabblad* is de term die wordt gebruikt voor een groep velden die onder een gezamenlijke kop worden weergegeven. Gebruik de optie <b>Weergeven wanneer samengevouwen</b> om de belangrijkste velden weer te geven. Als u een veld in de kop selecteert, wordt het sneltabblad geopend met de focus op het geselecteerde veld.<br /><br />Deze optie is alleen van toepassing als een pagina meerdere sneltabbladen bevat. Als er slechts één sneltabblad is, kan het niet worden samengevouwen, dus is de optie <b>Weergeven wanneer samengevouwen</b> niet beschikbaar.|
|Een veld alleen-weergeven maken wanneer u **Meer tonen** selecteert.|Kies de pijlpunt en kies vervolgens <b>Weergeven onder 'Meer tonen'</b>.|Als u de optie <b>Weergeven onder Meer tonen</b> niet ziet, is het veld al ingesteld. In dit geval kunt u een veld altijd laten weergeven, en niet alleen wanneer u **Meer tonen** selecteert, door <b>Altijd weergeven</b> te kiezen.|
|Wijzig of een veld wel of niet kan worden bewerkt.|Selecteer het veld, selecteer de pijlpunt op het veld en selecteer vervolgens <b>Bewerking vergrendelen</b> om te voorkomen dat de waarde van het veld wordt gewijzigd, of <b>Bewerking ontgrendelen</b> om het wijzigen van de veldwaarde mogelijk te maken.|U kunt alleen velden ontgrendelen die u eerder zelf hebt vergrendeld. Sommige velden zijn standaard vergrendeld, hetzij door het ontwerp, hetzij door een profielbeheerder die [de pagina heeft aangepast](ui-personalization-manage.md). Deze velden kunnen niet worden ontgrendeld.|
|Het bevroren deelvenster in een lijst in een andere kolom wijzigen. |Kies de pijlpunt van de kolom die u als laatste van het bevroren deelvenster hebben wilt, en kies vervolgens <b>Bevroren deelvenster instellen</b>.<br /><br/>Als u het bevroren deelvenster terug wilt verplaatsen naar de oorspronkelijke positie waarvoor het bestemd was, kiest u de pijlpunt voor de kolom met het huidige bevroren deelvenster en kiest u <b>Bevroren deelvenster wissen</b>. Opmerking: u kunt dit bevroren deelvenster niet verwijderen.|Het bevroren deelvenster geeft de kolommen aan die altijd links van de lijst worden weergegeven, zelfs als u horizontaal schuift.|  
|Een veld overslaan wanneer u op Enter drukt.|Kies de pijlpunt naast het veld of de kolomkop in een lijst en kies **Uitsluiten van snelinvoer**.  | Als **Uitsluiten van snelinvoer** niet wordt weergegeven, is het veld al overgeslagen. In dit geval kunt u het overslaan van het veld stoppen door **Opnemen in snelinvoer** te kiezen.<br><br>[Meer informatie over snelinvoer](ui-enter-data.md#QuickEntry)|
|Weergaven die gefilterde lijsten vertegenwoordigen, opnieuw rangschikken en verwijderen.|Kies de pijlpunt naast een weergave en kies vervolgens **Verplaatsen**, **Verwijderen** of **Verbergen**.|[Meer informatie over het opslaan en personaliseren van lijstweergaven](ui-views.md)|  
|Voeg een nieuwe actie toe aan een pagina of rapport in uw rolcentrum.|Kies op de doelpagina, de rapportverzoekpagina of het venster Vertel me het bladwijzerpictogram.|[Meer informatie over het maken van bladwijzers van pagina's en rapporten](ui-bookmarks.md)|
|Start een lijst altijd uitgevouwen of samengevouwen|Kies in de linkerbovenhoek van de lijst **Alles uitvouwen** of **Alles samenvouwen**. U kunt ook de actie **Alles uitvouwen** of **Alles samenvouwen** kiezen in het menu van de eerste kolom. |Is van toepassing op samenvouwbare hiërarchielijsten|

## <a name="personalize-action-bar-and-menus"></a><a name="Actions"></a>De actiebalk en menu's personaliseren

Met personalisatie kunt u bepalen welke acties op de navigatie- en actiebalk en in rolcentra worden weergegeven en waar deze worden weergegeven. U kunt afzonderlijke acties of actiegroepen weergeven, verbergen of verplaatsen.

De volgende video laat zien hoe u acties op pagina's en rolcentra kunt personaliseren.

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE594m2]

De navigatie- en actiebalk personaliseren gebeurt in wezen op dezelfde manier als met andere elementen van de gebruikersinterface. Wat u precies kunt doen met een actie of groep, hangt er echter vanaf waar de actie of groep zich bevindt. De beste manier om daar achter te komen is de personaliseringsmodus te activeren en de pijlpunten u te laten leiden.

Er zijn enkele termen waarmee u vertrouwd moet zijn om actiepersonalisatie beter te begrijpen: *actiegroep* en *gepromoveerde categorie*.  

Een *actiegroep* is een element dat wordt vergroot om meer acties of groepen weer te geven. Op de pagina **Verkooporders** is één actiegroep bijvoorbeeld de actie **Functies**, die wordt weergegeven wanneer u de actie **Acties** kiest.

Een *gepromoveerde categorie* is een actiegroep die vóór de verticale lijn `|` op de actiebalk wordt weergegeven. De categorieën omvatten meestal de meest gebruikte acties, zodat u deze snel kunt vinden. Op de pagina **Verkooporders** zijn bijvoorbeeld de acties **Order**, **Vrijgeven** en **Boeken** gepromoveerde categorieën.

> [!NOTE]  
> Om personalisatie te wissen selecteert u de pijlpunt rond het ontwerpermenu van het onderdeel en kiest u vervolgens **Personalisatie wissen**.

### <a name="remove-hide-and-show-actions-and-action-groups"></a>Acties en actiegroepen verwijderen, verbergen en weergeven

Als u een actie wilt weergeven of verbergen, definiëren de opties onder de pijlpunt wat u kunt doen, afhankelijk van de status van de actie. 

1. Kies de pijlpunt voor een actie of actiegroep.
2. Kies een van de volgende opties:

|Optie|Wat het doet|
|------|------------|
|**Verwijderen**|Deze optie verschijnt als de geselecteerde actie ook ergens anders op de navigatie- of actiebalk wordt weergegeven. Als u deze optie kiest, verwijdert u de actie van de geselecteerde locatie, zodat deze niet meer wordt weergegeven. De actie of actiegroep blijft op de andere locaties. |
|**Verbergen**|Deze optie wordt weergegeven als de actie of groep zich niet ergens anders op de navigatie- of actiebalk bevindt. Net als **Verwijderen** laat het kiezen van deze optie de actie of actiegroep verdwijnen van de navigatie- of actiebalk. In de personalisatiemodus wordt de actie of actiegroep echter nog op de huidige positie weergegeven, behalve dat deze lichtgekleurd wordt weergegeven.|
|**Weergeven**|Deze optie wordt weergegeven als de actie of actiegroep is verborgen (lichtgekleurd). Als u deze optie kiest, wordt de actie of actiegroep weergegeven op de navigatie- of actiebalk.|

### <a name="move-actions-and-action-groups"></a>Acties en actiegroepen verplaatsen

Waar u acties of actiegroepen kunt neerzetten wordt aangegeven door een horizontale lijn tussen twee acties of een rand rond een actiegroep. Hier gelden de volgende beperkingen:

- U kunt individuele acties verplaatsen naar gepromoveerde categorieën, maar u kunt de volgorde van de acties in de categorie niet wijzigen.
- U kunt een actiegroep niet naar een gepromoveerde categorie verplaatsen.

1. Als u een actie of actiegroep wilt verplaatsen, sleept u deze naar de gewenste positie, net als met velden en kolommen.
2. Als u een actie of actiegroep verplaatst naar een andere actiegroep die leeg is, sleept u de actie of actiegroep naar de nieuwe groep en zet u deze neer in het kader **Hier een actie neerzetten**.

### <a name="about-the-automate-menu"></a>Over het menu Automatiseren

- U kunt het menu **Automatiseren** of het **Power Automate**-submenu en de bijbehorende acties niet verbergen of verplaatsen.
- U kunt stromen verplaatsen die zijn opgenomen onder de optie **Automatiseren**, maar u kunt ze niet verbergen met behulp van personalisatie. Als u de stroom verplaatst, wordt de stroom naar de bestemming gekopieerd Deze wordt niet verwijderd uit de optie **Automatiseren**.

> [!TIP]
> Als beheerder kunt u de optie **Automatisering** verbergen voor gebruikers. Zie voor meer informatie [Power Automate-integratie instellen](/dynamics365/business-central/dev-itpro/powerplatform/power-automate-setup).

## <a name="personalize-parts"></a><a name="Parts"></a>Onderdelen personaliseren

Wijs naar of selecteer <kbd>Alt</kbd>+<kbd>Pijl-omhoog</kbd> Onderdelen zijn gebieden op een pagina die doorgaans zijn samengesteld uit meerdere velden, grafieken of andere inhoud. Een onderdeel toont een gekleurde rand wanneer u op het onderdeel focust. Een startscherm van een rolcentrum bestaat bijvoorbeeld uit meerdere delen. Vanwege hun goed gedefinieerde grens kunt u het hele onderdeel en de inhoud ervan personaliseren.

- Om een onderdeel te verplaatsen, sleept u het naar de gewenste positie. Een gekleurde lijn geeft geldige posities op het scherm aan. Feitenblokken kunnen bijvoorbeeld alleen worden verplaatst naast andere feitenblokken in het deelvenster Feitenblok.
- U kunt een onderdeel verbergen door de optie **Verbergen** te kiezen onder de pijlpunt.
- Wanneer u begint met personaliseren of naar een nieuwe pagina navigeert, worden alle onderdelen die momenteel verborgen zijn, op de pagina weergegeven met onderscheidende afbeeldingen om aan te geven dat ze verborgen zijn. U kunt een onderdeel zichtbaar maken door de optie **Weergeven** te kiezen onder de pijlpunt.

U kunt alle personalisatiewijzigingen die u in één onderdeel hebt aangebracht, wissen door de optie **Personalisatie wissen** te kiezen onder de pijlpunt van het onderdeel. Personalisatie van een onderdeel wissen heeft alleen invloed op wijzigingen in de inhoud van het onderdeel, niet op de plaatsing of zichtbaarheid van het onderdeel op de pagina.  

## <a name="work-with-fields-and-columns"></a><a name="fields"></a>Werken met velden en kolommen

Wanneer u een pagina personaliseert, gebruikt u het deelvenster **Veld aan pagina toevoegen** om velden of kolommen op de pagina op te nemen die momenteel verborgen zijn in de weergave. Selecteer de actie **+ Veld** bovenaan de pagina om dit venster te openen. In tegenstelling tot andere verborgen elementen worden verborgen velden in de personalisatiemodus niet op de pagina zelf aangegeven. U kunt verborgen velden echter identificeren via het deelvenster **Veld toevoegen aan pagina**.

Hier volgen hier enkele algemene richtlijnen die u moet volgen bij het gebruik van het deelvenster **Veld toevoegen aan pagina**:

- Standaard worden in het deelvenster alle verborgen velden weergegeven. Verborgen velden worden gemarkeerd door het pictogram ![Toont het verborgen veldpictogram](media/hidden-icon.png "Toont het verborgen veldpictogram").
- U kunt de lijst filteren om andere velden weer te geven, bijvoorbeeld de velden die momenteel op de pagina worden weergegeven, door de knop **Aanbevolen velden** boven de lijst te selecteren en een filteroptie te kiezen. De naam van de knop verandert op basis van de filteroptie die u kiest.
  
   :::image type="content" source="media/personlaization-filter.svg" alt-text="Toont de filterknop in het deelvenster Een veld toevoegen in de personalisatiemodus.":::
- Als u een veld in de lijst selecteert, wordt de locatie ervan op de pagina gemarkeerd. Als het veld momenteel verborgen is, wordt de ontworpen locatie gearceerd weergegeven. 
- Voor meer details over een veld in de lijst wijst u het aan of selecteert u <kbd>Alt</kbd>+<kbd>Pijl omhoog</kbd> om knopinfo weer te geven.
- De velden die beschikbaar zijn in het deelvenster **Veld toevoegen aan pagina** worden bepaald door de ontwikkelaar van de pagina en de brontabel, of door een profielbeheerder die [de pagina heeft aangepast](ui-personalization-manage.md). U kunt geen nieuwe maken.
- Sommige pagina's hebben meerdere paginavelden die aan dezelfde brontabel zijn toegewezen. In het deelvenster worden beide/al deze paginavelden onafhankelijk weergegeven. Het tonen/verbergen/verplaatsen van deze velden is ook onafhankelijk, zonder dat de een de ander beïnvloedt.

### <a name="add-a-field-so-its-visible-on-the-page"></a>Een veld toevoegen zodat het zichtbaar is op de pagina

In het deelvenster **Veld aan pagina toevoegen** kunt u op twee manieren een veld opnemen dat momenteel verborgen is op de pagina:

- Sleep het veld naar de gewenste positie. De doellocatie wordt aangegeven door een dikke horizontale of verticale lijn.
- Selecteer het veld in de lijst, ga vervolgens naar het gearceerde veld op de pagina en selecteer de optie **Weergeven**.

> [!NOTE]
> Sommige velden die u toevoegt, kunnen niet meer worden bewerkt op de pagina als u klaar bent met personaliseren. Deze velden zijn oorspronkelijk op deze manier ontworpen of een beheerder [heeft de pagina aangepast](ui-personalization-manage.md) om te voorkomen dat u deze kunt bewerken.

## <a name="clear-personalization"></a>Personalisatie wissen

Op een bepaald moment wilt u mogelijk sommige of alle personalisatiewijzigingen ongedaan maken die u in de loop van de tijd op een pagina hebt aangebracht.

1. Kies op de banner **Personaliseren** de actie **Personalisatie wissen**.
2. Kies een van de volgende opties.  

> [!CAUTION]
> Het wissen van personalisatie kan niet ongedaan worden gemaakt.

|Optie|Wat het doet|
|------|------------
|**Alleen navigatiemenu**|Wist alle personalisatiewijzigingen die u ooit hebt aangebracht in het navigatiemenu dat wordt gedeeld door het rolcentrum en andere pagina's. Dergelijke wijzigingen omvatten alle nieuwe acties die als bladwijzers zijn toegevoegd en eventuele wijzigingen in koppelingen en groepen in het menu.|  
|**Alleen acties**|Wist alle personalisatiewijzigingen die u ooit hebt aangebracht in de navigatie- of actiebalk op de pagina.|
|**Alleen velden en kolommen**|Wist alle personalisatiewijzigingen die u ooit hebt aangebracht op de pagina, behalve wijzigingen in de navigatie- of actiebalk. Dergelijke wijzigingen omvatten wijzigingen in velden, kolommen, onderdelen en tegels. |
|**Alle**|Wist alle personalisatie die u ooit in de pagina hebt aangebracht, zodat de pagina weer de oorspronkelijke weergave krijgt. Dergelijke wijzigingen omvatten wijzigingen in de navigatie- en actiebalk, velden, kolommen, onderdelen en tegels.|

## <a name="tips-and-other-points-of-interest"></a>Tips en andere interessante zaken

Er zijn een aantal punten die u in gedachten moet houden als u beter wilt begrijpen hoe personaliseren in zijn werk gaat.

- Als u wijzigingen aanbrengt in een kaartpagina die u kunt openen vanuit een lijst, worden de wijzigingen doorgevoerd voor alle records die u vanuit die lijst opent. Als u bijvoorbeeld vanuit de lijstpagina Klanten een bepaalde klant opent en vervolgens de pagina personaliseert door een veld toe te voegen. Als u andere klanten vanuit die lijst opent, wordt het veld dat u hebt toegevoegd ook weergegeven.
- Wijzigingen die u aanbrengt, worden op al uw rolcentra toegepast. Als u bijvoorbeeld een wijziging in de lijst Klant aanbrengt wanneer het rolcentrum op Bedrijfsleider is ingesteld, kunt u de wijziging op de pagina **Klanten** zien wanneer het rolcentrum op Verkooporderverwerker wordt ingesteld.
- Wijzigingen in een deelvenster van een pagina worden op de pagina toegepast overal waar deze wordt weergegeven.  
- U kunt een pagina die zich in de [analysemodus](analysis-mode.md) bevindt, niet personaliseren. De schakelaar **Analyseren** is gedeactiveerd. Als u naar de personalisatiemodus overschakelt terwijl de pagina zich in de analysemodus bevindt, wordt de analysemodus automatisch uitgeschakeld. 
- Sommige pagina's hebben meerdere paginavelden die aan dezelfde brontabel zijn toegewezen. In het deelvenster worden beide/al deze paginavelden onafhankelijk weergegeven. Het tonen/verbergen/verplaatsen van deze velden is ook onafhankelijk, zonder dat de een de ander beïnvloedt.
- Als een onderdeel of groep verborgen is, worden er nog steeds vage velden in weergegeven, maar u kunt dat veld niet verslepen of toevoegen/tonen totdat u de groep/het onderdeel zichtbaar maakt.

## <a name="see-also"></a>Zie ook

[Pagina's aanpassen voor profielen](ui-personalization-manage.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Basisinstellingen wijzigen](ui-change-basic-settings.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
