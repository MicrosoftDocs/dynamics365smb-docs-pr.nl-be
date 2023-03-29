---
author: edupont04
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
---
Wanneer u een datumtijd invoert (een datum en een tijd gecombineerd tot één veld), moet u een spatie invoeren tussen de datum en de tijd. Het datumdeel kan alleen spaties in de vorm van het officiële datumscheidingsteken van uw regio-instellingen bevatten. De tijd kan spaties bevatten rond de AM/PM-indicator in relevante regionale instellingen.

<!--It is also possible to enter only a date in a datetime field, but it is not possible to enter only a time.-->

In de volgende tabel wordt aangegeven op welke manier u de datum/tijd kunt invoeren en hoe de verschillende manieren worden geïnterpreteerd.  

|Post|Interpretatie|
|---------------|------------------------|
|08-01-2022 05:48:12 PM|08\-01\-2022 05:48:12 PM|
|131222 132455|13-12-22 13:24:55|
|1-12-22 10|01-12-22 10:00:00|
|1.12.22 5|01-12-22 05:00:00|
|1.12.22|01-12-22 00:00:00|
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
|d23 t|Dinsdag van week 23 van het werkdatumjaar huidige tijd van dag|
|d23|Dinsdag van week 23 van het werkdatumjaar|
|d 23|Vandaag 23:00:00|
|d-1|Dinsdag van week 1 van het werkdatumjaar|


