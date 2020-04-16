---
title: Gegevens invoeren in Business Central | Microsoft Docs
description: Leer over algemene functies die u helpen gegevens in velden in te voeren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 9405e285613c95e6c3bfcf19a5fc57e109b3f419
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3194439"
---
# <a name="entering-data"></a>Gegevens invoeren

Er zijn allerlei algemene functies die u helpen gegevens sneller, gemakkelijker en accurater in te voeren. De algemene functies voor het invoeren van gegevens worden in dit artikel beschreven.  

In de voorbeelden in dit artikel worden de demonstratiegegevens gebruikt.

## <a name="keyboard-shortcuts"></a>Toetsenbordsneltoetsen

Er zijn verschillende sneltoetsen waarmee u 'muisvrij' kunt werken en de gegevensinvoer kunt versnellen, vooral bij grootschalige invoer en herhaald typewerk.

Zie voor meer informatie over sneltoetsen [Toetsenbordsneltoetsen](keyboard-shortcuts.md). Enkele sneltoetsen worden in dit artikel besproken.

## <a name="accelerating-data-entry-using-quick-entry"></a><a name="QuickEntry"></a>Gegevensinvoer versnellen met snelinvoer

Snelinvoer is een functie die bedoeld is voor gegevensinvoer met het toetsenbord. Snelinvoer werkt met velden (bijvoorbeeld op kaartpagina's) en in lijsten (rijen en kolommen). Het kan handig zijn bij herhalend typewerk, waarbij meerdere records achter elkaar moeten worden gemaakt, zoals een batch verkooporders of registratie van nieuwe artikelen.

U bent mogelijk al vertrouwd met het gebruik van de Tab-toets om van het ene veld op een pagina naar het volgende bewerkbare veld te navigeren. Het nadeel van het gebruik van de Tab-toets is dat deze altijd naar het volgende veld gaat. <!-- even if the field is non-editable or seldom filled it in.-->Met snelinvoer kunt u dit pad wijzigen. Met snelinvoer gebruikt u de Enter-toets om alleen te navigeren naar de velden waarin u geïnteresseerd bent. U slaat niet-bewerkbare velden en velden die u meestal niet invult, over. U hebt dit gedrag mogelijk al op bepaalde pagina's opgemerkt. Dit komt omdat de toepassing al aangeeft welke velden moeten worden opgenomen wanneer op Enter wordt gedrukt en welke worden overgeslagen. U kunt snelinvoer wijzigen door de werkruimte aan te passen en te optimaliseren hoe u gegevens op elke pagina invoert.

### <a name="how-quick-entry-works"></a>Hoe snelinvoer werkt

Elk veld kan worden gemarkeerd als zijnde *opgenomen in snelinvoer* of *uitgesloten van snelinvoer*. Velden die in snelinvoer zijn opgenomen, worden opgenomen in het pad wanneer u op Enter drukt; velden die zijn uitgesloten van snelinvoer, worden dat niet.

Wanneer u klaar bent met het invoeren van gegevens in een veld, drukt u gewoon op Enter om de wijzigingen te bevestigen en naar het volgende veld te gaan. Als u de volgorde wilt omkeren en naar het vorige veld wilt gaan, drukt u op Shift+Enter. Zie voor meer informatie over sneltoetsen [Sneltoetsen voor snelinvoer voor velden](keyboard-shortcuts.md#QuickEntry).

#### <a name="tips-and-tricks"></a>Tips en trucs
Hieronder volgt wat nuttige informatie over het gebruik van snelinvoer.

- Het is beschikbaar voor bewerkbare velden.
- Het werkt ook over kolommen en rijen.
- Het voorkomt geen toegang tot andere elementen van een pagina, zoals acties. Deze zijn nog toegankelijk met behulp van Tab en Shift+Tab.  
- Sneltabbladen hoeven niet uitgevouwen te zijn om snelinvoer te gebruiken. Als het volgende snelinvoerveld zich in een samengevouwen sneltabblad bevindt, wordt dat sneltabblad automatisch uitgevouwen en gaat de focus naar het juiste veld.
- Snelinvoer werkt ongeacht of velden verplicht zijn. Het is dus een goed idee te zorgen dat verplichte velden zijn opgenomen in snelinvoer.
- Standaard worden de meeste velden automatisch opgenomen in snelinvoer. In eerste instantie moet u dus waarschijnlijk velden uitsluiten van snelinvoer.

### <a name="to-change-quick-entry-fields"></a>Snelinvoervelden wijzigen

Als u wilt wijzigen welke velden zijn opgenomen in of uitgesloten van snelinvoer op een pagina, gebruikt u personalisatie.

1. Start personalisatie door het pictogram ![Instellingen](media/ui-experience/settings_icon_small.png "Pictogram Instellingen voor rolcentrum") te selecteren en vervolgens de actie **Personaliseren**.
2. Selecteer een veld dat u wilt wijzigen of selecteer in lijsten de corresponderende kolomkop en kies vervolgens **Opnemen in snelinvoer** of **Uitsluiten van snelinvoer**.

Zie voor meer informatie over personalisatie [Uw werkruimte personaliseren](ui-personalization-user.md).

## <a name="mandatory-fields"></a>Verplichte velden

Wanneer u gegevens invoert op pagina's, zijn bepaalde velden gemarkeerd met een rode asterisk. De rode asterisk betekent dat het veld moet worden ingevuld om een bepaald proces te voltooien dat het veld gebruikt, zoals het boeken van een transactie die de waarde in het veld gebruikt.  

Zelfs als het veld een rode asterisk bevat, wordt u niet gedwongen het veld te vullen voordat u verdergaat naar andere velden of de pagina sluit. De rode asterisk dient alleen als een herinnering dat u wordt geblokkeerd van het voltooien van een bepaald proces.  

## <a name="finding-data-as-you-type"></a>Gegevens zoeken terwijl u typt

 Als u begint met het typen van tekens in een veld, wordt een vervolgkeuzelijst weergeven met de mogelijke veldwaarden. De lijst verandert naarmate u meer tekens typt en u kunt de juiste waarde selecteren wanneer deze wordt weergegeven.  

 Veel velden hebben een knop met een pijl-omlaag die u kunt kiezen. U kunt op de pijl klikken om een lijst met gegevens te krijgen die u in het veld kunt instellen. De knop heeft twee functies, afhankelijk van het type veld:  

-   Opzoeken - Hiermee toont u gegevens uit een andere tabel die u in het veld kunt invoeren. U kunt slechts één gegevensitem tegelijk selecteren.  

-   Vervolgkeuze - Hiermee toont u de verzameling opties die beschikbaar zijn voor het veld. U kunt slechts één optie tegelijk selecteren.  

## <a name="copying-and-pasting-faq-fields-and-lines"></a>Velden en regels kopiëren en plakken

U kunt een of meer rijen uit een lijst of een enkel veld op een pagina kopiëren en vervolgens wat u hebt gekopieerd, plakken op dezelfde pagina, een andere pagina of een extern document (zoals Microsoft Excel en Outlook-e-mail). Als u wilt kopiëren, drukt u op CTRL+C (cmd+C in MacOs) op het toetsenbord. Als u wilt plakken, drukt u op CTRL+V (cmd+V in MacOs).

Als u in een lijst het veld in dezelfde kolom van de bovenliggende rij wilt selecteren en het in de huidige rij wilt plakken, drukt u op F8.

Zie voor meer informatie [Veelgestelde vragen over kopiëren en plakken](ui-copy-paste.md).

## <a name="filtering-line-items"></a>Regelitems filteren

Als u wilt beginnen met filteren, selecteert u het ![pictogram Filterdeelvenster](media/open-filter-pane-icon.png "Pictogram Filterdeelvenster") boven aan de lijst of drukt u op Shift+F3 om het filterdeelvenster te openen. U werkt met het filterdeelvenster zoals met elke andere lijst. Zie [Filteren](ui-enter-criteria-filters.md#filtering) voor meer informatie.

Filteren is met name handig bij het weergeven en analyseren van langere documenten. Stel dat u een geboekte verkoopfactuur opent en de regelartikelen filtert om alle regelartikelen weer te geven die een individuele korting van meer dan 5% hebben, of dat u filtert om alleen fietsaccessoires met 'pro' in de naam weer te geven.

## <a name="focusing-on-line-items"></a><a name="Focus"></a>Focussen op regelartikelen

Wanneer u werkt aan documenten die een regelitemgedeelte bevatten, zoals een verkooporder of factuurpagina, kunt u uw weergave zo instellen dat deze zich alleen op de regelitems concentreert. Het gedeelte met regelitems wordt vervolgens uitgevouwen zodat het vrijwel de hele werkruimte in beslag neemt en andere delen van de pagina verbergt behalve het actiegebied bovenaan. Dit geeft u een beter overzicht van de regelartikelen en biedt meer ruimte om ermee te werken.

Dit is met name voordelig bij het werken met grote regelartikellijsten en wanneer snelle gegevensinvoer gewenst is. Een ander voordeel is dat het ook geavanceerde filtermogelijkheden biedt, zoals in andere lijsten, waardoor bladeren en zoeken door regelartikelen nog gemakkelijker wordt.

### <a name="switching-the-focus-on-and-off"></a>De focus aan- en uitzetten

Als u op regelartikelen wilt focussen, selecteert u iets in het onderdeel met regelitems en kiest u vervolgens het ![pictogram Focusmodus](media/focus-mode.png "Pictogram Focusmodus") in de rechterbovenhoek of drukt u op Ctrl+Shift+F12.

Als u terug wilt naar de gewone weergave, kiest u opnieuw het ![pictogram Focusmodus](media/focus-mode.png "Pictogram Focusmodus") of drukt opnieuw op Ctrl+Shift+F12.

## <a name="multitasking-across-multiple-pages"></a>Multitasking over meerdere pagina's
Wanneer u aan meerdere taken tegelijk werkt of wanneer u onderbrekingen in de huidige taak beheert, zoals het aannemen van een inkomende oproep, kunt u een kaart- of documentpagina in een nieuw venster openen. Hiermee kunt u een venster openhouden voor een lopende taak terwijl u een andere taak in een of meer andere vensters start of voltooit.

Kies om de huidige kaart of het huidige document in een nieuw venster te openen ![Nieuw venster openen](media/open-new-window-icon.png "Pictogram Nieuw venster openen") in de rechterbovenhoek of druk op Alt + Shift+W.

> [!NOTE]
> Wanneer u andere pagina's opent vanaf een kaart of document dat in een nieuw venster is geopend, worden die pagina's in een nieuw venster geopend, ook al kiest u niet ![Nieuw venster openen](media/open-new-window-icon.png "Pictogram Nieuw venster openen").

> [!NOTE]
> Als u in de Safari-browser werkt, kan een pop-upblokkering ervoor zorgen dat het nieuwe venster niet wordt geopend. Als dit het geval is, geeft u de product-URL op als een toegestane website. Zie voor informatie [Voorkeuren wijzigen in Safari](https://go.microsoft.com/fwlink/?LinkId=2102965).<br /><br />
> Hetzelfde kan gebeuren in andere browsers, zoals Firefox. Zie voor meer informatie [Instellingen voor pop-upblokkering in Firefox](https://go.microsoft.com/fwlink/?LinkId=2116400).  

Een andere manier om te multitasken is om [!INCLUDE[d365fin](includes/d365fin_md.md)] te openen op twee of meer browsertabbladen. Wanneer u dit doet, moet u een nieuw tabblad maken en vervolgens de URL van het oorspronkelijke tabblad kopiëren en in het nieuwe tabblad plakken. Dit creëert een nieuwe sessie.   

> [!NOTE]
> Gebruik niet de functie **Dupliceren** van de browser om het nieuwe tabblad te maken, omdat hierdoor acties op één tabblad acties op andere tabbladen kunnen blokkeren omdat ze deel uitmaken van dezelfde sessie.

## <a name="entering-quantities-by-calculation"></a>Hoeveelheden invoeren door berekening

Als u getallen in velden voor hoeveelheden invoert, zoals het veld **Hoeveelheid** op een artikeldagboekregel, kunt u de formule invoeren in plaats van de totale hoeveelheid.  

### <a name="examples"></a>Voorbeelden  

-   Als u 19+19 invoert, wordt het veld berekend als 38.  

-   Als u 41-9, wordt het veld berekend als 32.  

-   Als u 12*4 invoert, wordt het veld berekend als 48.  

-   Als u 12/4 invoert, wordt het veld berekend als 3.  

## <a name="entering-negative-numbers"></a>Negatieve getallen invoeren

U kunt negatieve getallen op twee manieren invoeren. Nummer -20.5 kan worden ingevoerd als:  

-   -20,5  

    of
-   20,5-  

 In beide gevallen wordt het bedrag als -20,5 geregistreerd.  

 Als het laatste teken van de expressie een **+** of een **-** is, wordt de volledige expressie vastgelegd met dat teken. Een voorbeeld: **10-20+** resulteert in 10 en niet -10.  

## <a name="entering-dates-and-times"></a>Datums en tijden invoeren

U kunt datums en tijden invoeren in alle velden die speciaal zijn toegewezen aan datums (datumvelden). U kunt datums met of zonder scheidingstekens invoeren.

> [!NOTE]  
> Hoe u datums en tijden invoert, hangt af van uw instellingen onder **Regio**. Zie voor meer informatie [Basisinstellingen wijzigen](ui-change-basic-settings.md).  

### <a name="entering-dates"></a>Datums invoeren

Voor datumvelden kunt u de datumselectie gebruiken. Hiermee selecteert u een datum in een kalender of voert u handmatig datums in. Deze sectie geeft een kort overzicht van hoe u datums invoert. Zie voor meer informatie [Werken met kalenderdatums en tijden](ui-enter-date-ranges.md).

Voor handmatige datuminvoer kunt u twee, vier, zes of acht cijfers invoeren:  

-   Als u slechts twee cijfers invoert, wordt dit als een dag beschouwd en wordt de maand en het jaar van de werkdag automatisch toegevoegd.  

-   Als u vier cijfers invoert, wordt dit als een dag en een maand beschouwd en wordt het jaar van de werkdag automatisch toegevoegd.  

-   Als de ingevoerde datum in de reeks 01.01.1930 tot en met 31.12.2029 valt, hoeft u slechts twee cijfers voor het jaartal in te voeren; anders moet u vier cijfers voor het jaartal invoeren.  

U kunt een datum ook invoeren als een weekdag gevolgd door een weeknummer en eventueel het jaar (Ma25 of ma25 duidt bijvoorbeeld op maandag in week 25).  

U kunt in plaats van een specifieke datum ook een van deze codes invoeren.  

|Code|Resultaat|  
|--------------|----------------|  
|h|Dit is de datum van vandaag (de systeemdatum voor de computer).|  
|p|Hiermee wordt een boekhoudperiode opgegeven, waarbij p de eerste boekhoudperiode is, p2 de tweede boekhoudperiode is, enzovoort. |
|w|Dit is de werkdatum die is ingesteld in de toepassing. Zie [Basisinstellingen wijzigen](ui-change-basic-settings.md) als u de werkdatum wilt wijzigen. Het gebruik van een werkdatum is handig als u veel transacties hebt met een andere datum dan de huidige.|
|u|Hiermee geeft u op dat de datum na u een ultimodatum is, bijvoorbeeld U311201.|  

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

 Als u geen scheidingsteken invoert, moet u twee cijfers invoeren voor elke eenheid.  

## <a name="entering-datetimes"></a>Datum/tijd invoeren

Wanneer u datum/tijd invoert, moet u een spatie plaatsen tussen de datum en de tijd.  

In de volgende tabel wordt aangegeven op welke manier u de datum/tijd kunt invoeren en hoe de verschillende manieren worden geïnterpreteerd.  

|Post|Interpretatie|  
|---------------|------------------------|  
|`131202` 132455|13.12.02 13:24:55|  
|1-12-02 10|01.12.02 10:00:00|  
|1.12.02 5|01.12.02 05:00:00|  
|1.12.02|01.12.02 00:00:00|  
|11 12|11.huidige maand.huidig jaar 12:00:00|  
|1112 12|11.12.huidig jaar 12:00:00|  
|h of huidige datum|huidige datum 00:00:00|  
|h tijd|huidige datum werkelijke tijd|  
|h 10:30|huidige datum 10:30:00|  
|h 3:3:3|huidige datum 03:03:03|  
|w of werkdatum|de werkdatum 00:00:00|  
|ma of maandag|Maandag van de huidige week 00:00:00|  
|di of dinsdag|Dinsdag van de huidige week 00:00:00|  
|wo of woensdag|Woensdag van de huidige week 00:00:00|  
|do of donderdag|Donderdag van de huidige week 00:00:00|  
|vr of vrijdag|Vrijdag van de huidige week 00:00:00|  
|za of zaterdag|Zaterdag van de huidige week 00:00:00|  
|zo of zondag|Zondag van de huidige week 00:00:00|  
|di 10:30|Dinsdag van de huidige week 10:30:00|  
|di 3:3:3|Dinsdag van de huidige week 03:03:03|  

## <a name="entering-duration"></a>Duur invoeren
De duur moet worden ingevoerd als een getal gevolgd door de eenheid.  

Hier volgen enkele voorbeelden.  

|Duur|Eenheid**|  
|------------------|-------------------------|  
|2u|2 uur|  
|6u 30 m|6 uur en 30 minuten|  
|6,5u|6 uur en 30 minuten|  
|90m|1 uur en 30 minuten|  
|2d 6u 30m|2 dagen, 6 uur en 30 minuten|  
|2d 6u 30m 56s 600ms|2 dagen, 6 uur, 30 minuten, 56 seconden en 600 milliseconden|  

 Als u een getal invoert, wordt het getal automatisch omgezet naar een duur. Dit gebeurt op basis van de standaardeenheid die in het veld Duur is ingevoerd.  

 Als u wilt nagaan welke eenheid wordt gebruikt in het veld Duur, voert u een getal in en bekijkt u in welke eenheid het getal wordt omgezet.  

 Het getal 5 wordt omgezet in 5 uur, als de eenheid uit uren bestaat.  

## <a name="see-also"></a>Zie ook  
 [Lijsten sorteren, doorzoeken en filteren](ui-enter-criteria-filters.md)  
 [Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
