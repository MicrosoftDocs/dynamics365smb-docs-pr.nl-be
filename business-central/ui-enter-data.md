---
title: Gegevens invoeren in velden | Microsoft Docs
description: Er zijn veel algemene functies waarmee u snel en gemakkelijk gegevens kunt invoeren. De algemene functies voor het invoeren van gegevens worden allemaal in dit onderwerp beschreven.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/19/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 4354e28522d359cf9fa6178c4a1919831dcc52db
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---

# <a name="entering-data"></a>Gegevens invoeren
Er zijn veel algemene functies waarmee u snel en gemakkelijk gegevens kunt invoeren. De algemene functies voor het invoeren van gegevens worden in dit artikel beschreven.  

In de voorbeelden in dit artikel worden de demonstratiegegevens gebruikt.

## <a name="mandatory-fields"></a>Verplichte velden
Wanneer u gegevens invoert op pagina's, zijn bepaalde velden gemarkeerd met een rode asterisk. De rode asterisk betekent dat het veld moet worden ingevuld om een bepaald proces te voltooien dat het veld gebruikt, zoals het boeken van een transactie die de waarde in het veld gebruikt.  

Zelfs als het veld een rode asterisk bevat, wordt u niet gedwongen het veld te vullen voordat u verdergaat naar andere velden of de pagina sluit. De rode asterisk dient alleen als een herinnering dat u wordt geblokkeerd van het voltooien van een bepaald proces.  


## <a name="finding-data-as-you-type"></a>Gegevens zoeken terwijl u typt  
 Als u begint met het typen van tekens in een veld, wordt een vervolgkeuzelijst weergeven met de mogelijke veldwaarden. De lijst verandert naarmate u meer tekens typt en u kunt de juiste waarde selecteren wanneer deze wordt weergegeven.  

 Veel velden hebben een knop met een pijl-omlaag die u kunt kiezen. U kunt op de pijl klikken om een lijst met gegevens te krijgen die u in het veld kunt instellen. De knop heeft twee functies, afhankelijk van het type veld:  

-   Opzoeken - Hiermee toont u gegevens uit een andere tabel die u in het veld kunt invoeren. U kunt slechts één gegevensitem tegelijk selecteren.  

-   Vervolgkeuze - Hiermee toont u de verzameling opties die beschikbaar zijn voor het veld. U kunt slechts één optie tegelijk selecteren.  

<!--Onprem ## Copy Fields or Lines  
 Depending on the type of writable document, you can copy individual line fields or whole lines to other lines in the document. Read-only data, such as posted entries, cannot be copied.  

 Several database dependencies are used to determine if fields or lines can be copied. One way to determine these dependencies is to view the shortcut menu. The content of the shortcut menu indicates which copy functions are supported by displaying either of these functions:  

-   Copy Cell  

-   Copy Rows  

-   Paste Rows  

 For example, database records, such as lines on a sales order, and master data, such as cards in the **Items** window, cannot be duplicated. For this kind of data, the shortcut menu typically has the **Copy Cell** or **Copy Rows**  functions. If the **Paste** function is not available this indicates that you can only paste the data into external documents. Single fields on a sales line, however, can be copied to the same column in other sales lines.  

 Journal lines are very flexible and can be copied freely in the same journal, indicated by the presence of **Paste** on the shortcut menu.  

> [!NOTE]  
>   If you copy a journal line or document line, the fields that are not in your view are not copied to the new line.

#### To copy previous field  

-   To enter the value of the field immediately above the active field, select **Copy Previous** from the shortcut menu.-->

## <a name="entering-quantities-by-calculation"></a>Hoeveelheden invoeren door berekening  
 Als u getallen in velden voor hoeveelheden invoert, zoals het veld **Hoeveelheid** op een artikeldagboekregel, kunt u de formule invoeren in plaats van de totale hoeveelheid.  

## <a name="examples"></a>Voorbeelden  

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
 Een datumveld kan twee, vier, zes of acht cijfers bevatten:  

-   Als u slechts twee cijfers invoert, wordt dit als een dag beschouwd en wordt de maand en het jaar van de werkdag automatisch toegevoegd.  

-   Als u vier cijfers invoert, wordt dit als een dag en een maand beschouwd en wordt het jaar van de werkdag automatisch toegevoegd.  

-   Als de ingevoerde datum in de reeks 01/01/1930 tot en met 31/12/2029 valt, hoeft u slechts twee cijfers voor het jaartal in te voeren; anders moet u vier cijfers voor het jaartal invoeren.  

 U kunt een datum ook invoeren als een weekdag gevolgd door een weeknummer en eventueel het jaar (Ma25 of ma25 duidt bijvoorbeeld op maandag in week 25).  

 U kunt in plaats van een specifieke datum ook een van de volgende codes invoeren.  

|Code|Resultaat|  
|--------------|----------------|  
|h|Dit is de datum van vandaag (de systeemdatum voor de computer).|  
|w|Dit is de werkdatum die is ingesteld in de toepassing. Zie [Basisinstellingen wijzigen](ui-change-basic-settings.md) als u de werkdatum wilt wijzigen. Het gebruik van een werkdatum is handig als u veel transacties hebt met een andere datum dan de huidige.|  

<!--Onprem ## Closing Date  
 When you close a fiscal year, you can use closing dates to indicate that an entry is a closing entry. A closing date technically is between two dates, for example between Dec 31 and Jan 1.  

 To specify that a date is a closing date, put C just before the date: C123101. -->

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
|131202 132455|13-12-02 13:24:55|  
|1-12-02 10|01-12-02 10:00:00|  
|1.12.02 5|01-12-02 05:00:00|  
|1.12.02|01-12-02 00:00:00|  
|11 12|11-huidige maand-huidig jaar 12:00:00|  
|1112 12|11-12-huidig jaar 12:00:00|  
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

<!--OnPrem  ##  <a name="BKMK_SettingDateRanges"></a> Setting Date Ranges  
 You can set filters containing a start date and an end date to display only the data contained in that date range or time interval. Special rules apply to the way you set date ranges.  

|**Meaning**|**Sample expression**|**Entries included**|  
|-----------------|---------------------------|--------------------------|  
|**Equal to**|12 15 00|Only those posted on 12 15 00.|  
|**Interval**|12 15 00..01 15 01<br /><br /> ..12 15 00|Those posted on dates between and including 12 15 00 and 01 15 01.<br /><br /> Those posted on 12 15 00 or earlier.|  
|**Either/or**|12 15 00&#124;12 16 00|Those posted on either 12 15 00 or 12 16 00. If there are entries posted on both days, they will all be displayed.|  

 You can also combine the various format types.  

|**Sample expression**|**Entries included**|  
|---------------------------|--------------------------|  
|12 15 00&#124;12 01 00..12 10 00|Entries posted either on 12 15 00 or on dates between and including 12 01 00 and 12 10 00.|  
|..12 14 00&#124;12 30 00..|Entries posted on 12 14 00 or earlier, or entries posted on 12 30 00 or later - that is, all entries except those posted on dates between and including 12 15 00 and 12 29 00.|  -->

## <a name="using-date-formulas"></a>Datumformules gebruiken  
 Een datumformule is een korte, afgekorte combinatie van letters en cijfers op basis waarvan datums worden berekend. U kunt datumformules invoeren in verschillende datumberekeningsvelden en in de frequentievelden van periodieke dagboeken.  

> [!NOTE]  
>  In alle datumformulevelden wordt automatisch één dag opgenomen om ervoor te zorgen dat de huidige dag wordt gebruikt als begindatum van de periode. Als u bijvoorbeeld 1W invoert, zal de periode in feite acht dagen bestrijken omdat vandaag ook is opgenomen. Als u een periode van zeven dagen (exact één week) wilt opgeven, inclusief de begindatum van de periode, moet u 6D of 1W-1D opgeven.  

 Hier volgen enkele voorbeelden van het gebruik van datumformules:  

-   De datumformule in de frequentievelden van periodieke dagboeken geeft aan hoe vaak de dagboekregel moet worden geboekt.  

-   De datumformule in het veld Respijtperiode van een bepaald aanmaningsniveau bepaalt hoelang de vervaldatum (of de datum van de vorige aanmaning) moet zijn verstreken voordat een aanmaning wordt gemaakt.  

-   De datumformule in het veld Vervaldatumformule bepaalt hoe de vervaldatum voor de aanmaning wordt berekend.  

 In de berekeningsformule voor de datum kunt u maximaal 20 tekens gebruiken (cijfers en/of letters). U kunt de volgende letters gebruiken als afkorting voor tijdsaanduidingen.  

|||  
|-|-|  
|L|Lopend|  
|D|Dag|  
|W|Week|  
|M|Maand|  
|K|Kwartaal|  
|J|Jaar|  

 Er zijn drie soorten datumformules.  

 In het volgende voorbeeld wordt weergegeven hoe huidig en een getal.  

|||  
|-|-|  
|LW|Lopende week|  
|LM|Lopende maand|  

 In het volgende voorbeeld wordt weergegeven hoe een getal en een tijdseenheid. Nummers mogen niet groter zijn dan 9999.  

|||  
|-|-|  
|10D|10 dagen vanaf vandaag|  
|2W|2 weken vanaf vandaag|  

 In het volgende voorbeeld wordt weergegeven hoe een tijdseenheid en een getal.  

|||  
|-|-|  
|D10|De volgende tiende dag van een maand|  
|WD4|De volgende vierde dag van een week (donderdag)|  

 Het volgende voorbeeld geeft weer hoe u deze drie soorten naar wens kunt combineren.  

|||  
|-|-|  
|LM+10D|Lopende maand + 10 dagen|  

 In het volgende voorbeeld ziet u hoe u een minteken gebruikt om een datum in het verleden aan te duiden.  

|||  
|-|-|  
|-1J|1 jaar geleden vanaf vandaag|  

<!--OnPrem > [!CAUTION]  
>  If the location uses a base calendar, then the date formula that you enter in, for example, the **Shipping Time** field is interpreted according to the calendar working days. For example, a 1W means seven working days. For more information, see Base Calendar Card.-->  
## <a name="see-also"></a>Zie ook  
 [Gegevens zoeken, filteren en sorteren](ui-enter-criteria-filters.md)  
 [Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

