---
title: Procedure van basistaken
description: Dit artikel leidt u door verschillende kernprocessen in projectmanagement.
author: andreipanko
ms.author: andreipa
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# Procedure van basistaken

Deze procedure demonstreert verschillende kernprocessen:

- Projecttaken aan projecten toevoegen
- Registratie van tijd en materiaalkosten voor een project
- Een project factureren

## Een projecttaak aan een project toevoegen

### Scenario  

Simon, de projectmanager, wil tijd die wordt besteed aan het opleiden van de klant in het gebruik van espressomachines, registreren in een aparte taak in het project voor het ter plaatse installeren van een commerciële machine.

### Stappen

1. De projecttaak maken  

    1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projecten** in en kies vervolgens de gerelateerde koppeling.  
    2. Selecteer het project *J00010*.
    3. Kies in het gebied **Taken** de actie **Nieuwe regel**.  Voer de volgende waarden in:
 
    |Projecttaaknr.|Omschrijving|Soort projecttaak|
    |------------|-----------|-------------|  
    |220|Klantentraining|Boeking|

2. Inspringen van projecttaken
   1. Zoek in het gebied Taken de actie **Projecttaken inspringen**
   2. Bevestig dat u taken wilt laten inspringen door **Ja** te selecteren.

### Resultaten

 - Nu kunnen tijd en kosten worden vastgelegd voor de nieuwe projecttaak

## Registratie van tijd en materiaalkosten voor een project

### Scenario  

Edgin, de technicus die de machine installeert, moet zijn tijd en de gebruikte materialen tijdens de installatie voor het project registreren voor de facturering.  Hij heeft de reiskosten en materialen al toegevoegd, en moet nu ook de tijd toevoegen voor het onderwijzen van het personeel om de machine te gebruiken.

### Stappen

1. De aanvullende projectdagboekregels maken

    1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projectjournalen** in en kies vervolgens de gerelateerde koppeling.  
    2. Selecteer de batch *CONTOSO*.  U ziet verschillende regels met resource- en artikeltypen, die de gebruikte tijd (voor de technicus en het voertuig) en materialen (de machine en benodigdheden) weerspiegelen.
    3. Een nieuwe regel maken. Voer de volgende waarden in:
 
    |Taaknr.|Projecttaaknr.|Type|Nr.|Omschrijving|Hoeveelheid|
    |-------|------------|----|---|-----------|--------|  
    |J00010|220|Resource|EDGIN|Klantentraining|1|

2. De tijd en kosten boeken
   1. Kies de actie **Boeken**
   2. Bevestig dat u de regels wilt boeken door **Ja** te selecteren.

### Resultaten

 - Projectposten en resourceposten van het type *Gebruik* worden gemaakt
 - Er worden artikelposten gemaakt om de voorraad negatief aan te passen
 - Op de projectkaart geven de kosten en prijzen in het gebied Taken de nieuwe saldi weer die wachten om te worden gefactureerd
 - Op de projectkaart geeft het feitenblok Projectdetails de totalen van de prijzen weer

## Een verkoopfactuur voor een project maken

### Scenario  
Simon moet een factuur maken en boeken die met de tijd en kosten van het project naar de klant moet worden verzonden.

### Stappen
1. De verkoopfactuur maken

    1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projecten** in en kies vervolgens de gerelateerde koppeling.  
    2. Kies in de lijst met projecten de actie **Projectverkoopfactuur maken**.
    3. Stel het filter **Projectnr.** in op *J00010*.
    4. Kies **OK** om de verkoopfactuur te genereren.  U ontvangt een bevestiging van het aantal facturen dat is gegenereerd

2. De factuur met tijd en kosten boeken
   1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopfacturen** in en kies vervolgens de gerelateerde koppeling.  
   2. Selecteer de laatste factuur om deze ter beoordeling te openen.
   3. Kies de actie **Boeken**.

### Resultaten

 - Projectposten en resourceposten van het type *Verkoop* worden gemaakt
 - Op de projectkaart geven de kosten en prijzen in het gebied Taken de nieuwe gefactureerde saldi weer
 - Op de projectkaart geeft het feitenblok Projectdetails de totalen van de prijzen in de sectie Gefactureerde prijs weer
