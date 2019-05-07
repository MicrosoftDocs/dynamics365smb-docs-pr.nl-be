---
title: Pagina's aanpassen | Microsoft Docs
description: Meer informatie over hoe u de gebruikersinterface kunt aanpassen aan uw manier van werken in Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 16f334548d9831507970a1b74ba5fa1716611380
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "922100"
---
# <a name="personalizing-your-workspace"></a>Het personaliseren van uw werkruimte

U kunt uw werkruimte aanpassen aan uw werk- en *persoonlijke voorkeuren*, door pagina's te wijzigen zodat deze alleen de gegevens weergeven die u nodig hebt en waar u die nodig hebt. De personalisatiewijzigingen die u maakt, hebben alleen effect op wat u ziet, niet wat andere gebruikers kunnen zien.

Afhankelijk van het soort pagina en wat de pagina bevat, kunt u verschillende dingen doen, zoals velden, kolommen en acties verplaatsen of verbergen, hele onderdelen verplaatsen en verbergen en meer.
<!--
-   Add, move, and remove fields.
-   Add, move, and remove columns in a list.
-   Change the freeze pane of columns in a list. The freeze pane locks one or more columns to the left side of a list so that are always present, even when you scroll horizontally.
-   Adjust the width of columns in a list.
-   Move and remove Cues (tiles).
-   Move and remove parts. Parts are subdivisions or areas on a page that contain things like multiple fields, another page, a chart, or tiles.

-->
> [!NOTE]
> Naast wat gebruikers kunnen personaliseren kunnen beheerders en supergebruikers personalisaties van gebruikers overschrijven en definiëren welke functies beschikbaar zijn in alle of specifieke bedrijven. Zie [Business Central aanpassen](ui-customizing-overview.md) voor meer informatie.

## <a name="to-personalize-a-page"></a>Een pagina personaliseren

1. In de rechterbovenhoek selecteert u ![Instellingen](media/ui-experience/settings_icon_small.png "instellingenpictogram voor rolcentrum") en vervolgens kiest u **Personaliseren**.

    De banner **Personaliseren** verschijnt bovenin, waarmee wordt aangegeven dat u wijzigingen kunt gaan aanbrengen.

    ![Personalisatiemodus](media/ui_personalize_mode_small.png "Personalisatiemodus")

2. Open de pagina die u wilt personaliseren.

    Als u een ![Personaliseringsvergrendeling](media/personalization-lock-icon.png "Personaliseringsvergrendeling") of ![Personalisatie geblokkeerd](media/personalization-blocked-icon.png "Personalisatie geblokkeerd") in de banner ziet, kunt u de pagina niet personaliseren. Zie voor meer details [Waarom kan ik een pagina niet personaliseren](ui-personalization-locked.md).

3. Wijs naar een gebied dat u wilt personaliseren, zoals een veld of kolomkop in een lijst. Alles wat u kunt personaliseren wordt onmiddellijk gemarkeerd met een pijlpunt of rand. Zie het [volgende gedeelte](#What) voor details over wat u kunt doen.

4. U kunt doorgaan met het aanbrengen van wijzigingen op dezelfde pagina of een andere pagina openen. Uw wijzigingen worden automatisch opgeslagen terwijl u ze aanbrengt. Als u klaar bent in de banner **Personaliseren** kiest u **Gereed**.

## <a name="What"></a>Wat kunt u personaliseren

|Wat u wilt doen?|Hoe kunt u het doen?|Opmerkingen|
|----|------------|-------|
|Iets verplaatsen, zoals een veld, een kolom in een lijst, een tegel, een actie of een onderdeel|Wijs naar alles wat u wilt verplaatsen en sleep dit naar de nieuwe locatie. De locatie wordt aangegeven door een dikke horizontale of verticale lijn.<br /><br />![Pictogram Kan niet hierheen verplaatsen](media/personalization-cannot-move-here.png "Personalisatiemodus - Pictogram Kan niet hierheen verplaatsen") geeft aan dat u het element niet naar de geselecteerde locatie kunt verplaatsen.|De onderdelen zijn onderverdelingen of gebieden op een pagina met objecten als meerdere velden, een andere pagina, een grafiek of tegels.<br /><br />Zie het [volgende gedeelte](ui-personalization-user.md#Actions) voor meer details over actiepersonalisatie. |
|Iets verbergen, zoals een veld, een kolom in een lijst, een tegel of een onderdeel.|Selecteer de pijlpunt en kies <b>Verbergen</b>.|Als het veld dat u verbergt ook in de sneltabbladkop wordt weergegeven wanneer het sneltabblad is samengevouwen, wordt het veld daar niet meer weergegeven.|
|Een kolom of veld toevoegen.|In de banner <b>Personaliseren</b> kiest u <b>Meer</b> en kiest u <b>Veld</b>.<br /></br>Het deelvenster <b>Veld toevoegen aan pagina</b> wordt aan de rechterkant weergegeven. Hier staan de velden die u aan de pagina kunt toevoegen.<br /><br />Als u een veld wilt toevoegen, moet u het uit het deelvenster slepen naar de locatie waar u het hebben wilt. De locatie wordt aangegeven door een dikke horizontale of verticale lijn.|Elke pagina bevat een vooraf bepaalde set velden die u kunt weergeven. Gebruik deze procedure om velden of kolommen toe te voegen die niet eerder zijn weergegeven of om velden weer te geven die u hebt verborgen.|
|Een veld weergeven in de kop van een sneltabblad wanneer dit is samengevouwen.|Selecteer de pijlpunt en kies <b>Weergeven wanneer samengevouwen</b>. <br /> <br />Als u deze optie niet ziet, is deze al ingesteld. In dit geval kunt u de weergave van het veld in de sneltabbladkop stoppen door <b>Altijd weergeven</b> te kiezen.|*Sneltabblad* is de term die wordt gebruikt voor een groep velden die onder een gezamenlijke kop worden weergegeven. Gebruik de optie <b>Weergeven wanneer samengevouwen</b> om de belangrijkste velden weer te geven. Als u een veld in de kop selecteert, wordt het sneltabblad geopend met de focus op het geselecteerde veld.<br /><br />Deze optie is alleen van toepassing als een pagina meerdere sneltabbladen bevat. Als er slechts één sneltabblad is, kan het niet worden samengevouwen, dus is de optie <b>Weergeven wanneer samengevouwen</b> niet beschikbaar.|
|Een veld alleen-weergeven maken wanneer u **Meer tonen** selecteert.|Selecteer de pijlpunt en kies <b>Weergeven onder "Meer tonen"</b>. <br /> <br />Als u de optie <b>Weergeven onder "Meer tonen"</b> niet ziet, is deze al ingesteld. In dit geval kunt u een veld altijd laten weergeven, en niet alleen wanneer u **Meer tonen** selecteert, door <b>Altijd weergeven</b> te kiezen.||
|Het bevroren deelvenster in een lijst in een andere kolom wijzigen. |Selecteer de pijlpunt van de kolom die u als laatste van het bevroren deelvenster hebben wilt, en kies vervolgens <b>Bevroren deelvenster instellen</b>.<br /><br/>Als u het bevroren deelvenster terug wilt verplaatsen naar de oorspronkelijke locatie waarvoor het bestemd was, selecteert u de pijlpunt voor de kolom met het huidige bevroren deelvenster en kiest u <b>Bevroren deelvenster wissen</b>. Opmerking: u kunt dit bevroren deelvenster niet verwijderen.|Het bevroren deelvenster geeft de kolommen aan die altijd links worden weergegeven, zelfs als u horizontaal schuift.|  
|De breedte van een kolom wijzigen.|Versleep in de tabelkoprij de rechterrand van de kolom. <br /><br />Als u de kolombreedte wilt maximaliseren om de langste regel van tekst in de kolom in te passen, dubbelklikt u op de juiste rand.||
|Een veld overslaan wanneer u op Enter drukt.|Selecteer de pijlpunt naast het veld of de kolomkop in een lijst en kies **Uitsluiten van snelinvoer**. <br /><br /> Als u deze optie niet ziet, is het veld al ingesteld om te worden overgeslagen. In dit geval kunt u het overslaan van het veld stoppen door **Opnemen in snelinvoer** te kiezen. |Zie [Gegevensinvoer versnellen met snelinvoer](ui-enter-data.md#QuickEntry)|

## <a name="Actions"></a>Acties personaliseren

U kunt de actiebalk personaliseren die zich boven aan de pagina bevindt, zoals aangegeven door het gemarkeerde gebied in de volgende illustratie.

![Actiebalk personaliseren](media/personalize-action-bar.png "Actiebalk personaliseren")

Met personalisatie kunt u bepalen welke acties op de actiebalk worden weergegeven en waar deze worden weergegeven. U kunt afzonderlijke acties of actiegroepen weergeven, verbergen of verplaatsen. De actiebalk personaliseren gebeurt in wezen op dezelfde manier als met andere elementen van de werkruimte. Wat u precies kunt doen met een actie of groep, hangt er echter vanaf waar de actie of groep zich bevindt op de actiebalk. De beste manier om daar achter te komen is dingen te proberen en het scherm u te laten leiden. In het volgende gedeelte worden enkele nuances uitgelegd van het personaliseren van de actiebalk.

### <a name="action-bar-overview"></a>Overzicht van actiebalk

Er zijn enkele termen waarmee u vertrouwd moet zijn om actiepersonalisatie beter te begrijpen: *actiegroep* en *gepromoveerde categorie*.  

Een *actiegroep* is een item dat wordt vergroot om meer acties of groepen weer te geven. Bijvoorbeeld in de volgende illustratie is **Boeken** een actiegroep.

Een *gepromoveerde categorie* is een actiegroep die tussen de twee verticale lijnen `|` op de actiebalk wordt weergegeven. De categorieën omvatten meestal de meest gebruikte acties, zodat u deze snel kunt vinden. Bijvoorbeeld in de volgende illustratie zijn **Vrijgeven**, **Boeken**, **Factuur** en **Navigeren** gepromoveerde categorieën.

![Actiebalkgroep personaliseren](media/personalize-action-bar-group-clip.png "Actiebalkgroep personaliseren ")

### <a name="to-remove-hide-and-show-actions-and-groups"></a>Acties en groepen verwijderen, verbergen en weergeven

Als u een actie of actiegroep wilt weergeven of verbergen, selecteert u deze en kiest u vervolgens een van de volgende opties:

|Optie|Wat het doet|
|------|------------
|**Verwijderen**|Deze optie verschijnt als de geselecteerde actie ook ergens anders op de actiebalk wordt weergegeven. Als u deze optie kiest, verwijdert u de actie van de geselecteerde locatie, zodat deze niet meer wordt weergegeven. De actie of actiegroep blijft op de andere locaties. |
|**Verbergen**|Deze optie wordt weergegeven als de actie of groep zich niet ergens anders op de actiebalk bevindt. Net als **Verwijderen** laat het kiezen van deze optie de actie of actiegroep verdwijnen van de actiebalk. In de personalisatiemodus wordt de actie of actiegroep echter nog op de huidige locatie weergegeven, behalve dat deze lichtgekleurd wordt weergegeven.|
|**Weergeven**|Deze optie wordt weergegeven als de actie of actiegroep eerder is verborgen (lichtgekleurd). Als u deze optie kiest, wordt de actie of actiegroep weergegeven op de actiebalk.|

### <a name="to-move-actions-and-action-groups"></a>Acties en actiegroepen verplaatsen

Als u een actie of actiegroep wilt verplaatsen, sleept u deze naar de gewenste locatie, net als met velden en kolommen.

Waar u acties of actiegroepen kunt neerzetten wordt aangegeven door een horizontale lijn tussen twee acties of een rand rond een actiegroep.

- U kunt individuele acties verplaatsen naar gepromoveerde categorieën, maar u kunt de volgorde van de acties in de categorie niet wijzigen.
- U kunt een actiegroep niet naar een gepromoveerde categorie verplaatsen.
- Als u een actie of actiegroep verplaatst naar een andere actiegroep die leeg is, sleept u de actie of actiegroep naar de nieuwe groep en zet u deze neer in het kader **Hier een actie neerzetten**.

## <a name="additional-points-of-interest"></a>Aanvullende interessante zaken

Er zijn een aantal punten die u in gedachten moet houden als u beter wilt begrijpen hoe personaliseren in zijn werk gaat.

- Als u wijzigingen aanbrengt in een kaartpagina die u kunt openen vanuit een lijst, worden de wijzingen doorgevoerd voor alle records die vanuit die lijst worden geopend. Als u bijvoorbeeld vanuit de lijstpagina Klanten een bepaalde klant opent en vervolgens de pagina personaliseert door een veld toe te voegen. Als u andere klanten vanuit die lijst opent, wordt het veld dat u hebt toegevoegd ook weergegeven.
- De wijzigingen die u aanbrengt worden op al uw rolcentra toegepast. Als u bijvoorbeeld een wijziging in de lijst Klant aanbrengt wanneer het rolcentrum op Bedrijfsleider is ingesteld, kunt u de wijzigingen in de lijst Klant ook zien wanneer het rolcentrum op Verkooporderverwerker wordt ingesteld.
- Wijzigingen in een deelvenster van een pagina worden op de pagina toegepast overal waar deze wordt weergegeven.  
- U kunt alleen velden en kolommen toevoegen uit een vooraf gedefinieerde lijst die op de pagina is gebaseerd. U kunt geen nieuwe maken.

## <a name="to-clear-personalization"></a>Personalisatie wissen

Op een bepaald moment wilt u mogelijk sommige of alle personalisatiewijzigingen ongedaan maken die u in de loop van de tijd op een pagina hebt aangebracht. Hiervoor kiest u in de banner **Personaliseren** **Meer**, **Personalisatie wissen** en kiest u vervolgens een van de volgende opties. Het wissen van personalisatie kan niet ongedaan worden gemaakt.

|Optie|Wat het doet|
|------|------------
|Alleen acties|Wist alle personalisatiewijzigingen die u ooit hebt aangebracht in de actiebalk op de pagina.|
|Alles behalve acties|Wist alle personalisatiewijzigingen die u ooit hebt aangebracht op de pagina, behalve wijzigingen in de actiebalk. Dit omvat wijzigingen in velden, kolommen, onderdelen en tegels. |
|Alle|Wist alle personalisatie die u ooit in de pagina hebt aangebracht, zodat de pagina weer de oorspronkelijke weergave krijgt. Dit omvat wijzigingen in de actiebalk, velden, kolommen, onderdelen en tegels.|

## <a name="see-also"></a>Zie ook

[Personalisatie beheren](ui-personalization-manage.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Basisinstellingen wijzigen](ui-change-basic-settings.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)  
