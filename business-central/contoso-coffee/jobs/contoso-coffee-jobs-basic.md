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

- Projecttaken toevoegen aan projecten
- Kosten voor tijd en materiaal voor een project registreren
- Een project factureren

## Een projecttaak toevoegen

### Scenario  

Simon, de projectmanager, wil de tijd registreren die wordt besteed aan het leren van de klant hoe deze het espressomachineproduct moet gebruiken. Simon wil een aparte taak in het project gebruiken voor het op locatie installeren van een commerciële machine.

### Stappen

1. Maak de projecttaak.

    1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projecten** in en kies vervolgens de gerelateerde koppeling.  
    2. Selecteer het project *J00010*.
    3. Kies in het gebied **Taken** de actie **Nieuwe regel** en voer vervolgens de volgende waarden in:
 
    |Projecttaaknr.|Omschrijving|Projecttaaktype|
    |------------|-----------|-------------|  
    |220|Klantentraining|Boeking|

2. Laat de projecttaken inspringen.
   1. Zoek in het gebied Taken de actie **Projecttaken inspringen**.
   2. Bevestig dat u taken wilt laten inspringen door **Ja** te selecteren.

### Resultaten

 - Nu kunnen tijd en kosten worden geregistreerd voor de nieuwe projecttaak

## Tijd- en materiaalkosten voor een project registreren

### Scenario  

Edgin, de technicus die de machine installeert, moet de tijd en de tijdens de installatie gebruikte materialen voor het project registreren voor de facturering. Hij heeft de reiskosten en materialen al toegevoegd, en moet nu ook de tijd toevoegen die hij heeft besteed om het gebruik van de machine aan het personeel uit te leggen.

### Stappen

1. Maak de extra projectdagboekregels.

    1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projectdagboeken** in en kies vervolgens de gerelateerde koppeling.  
    2. Selecteer de batch *CONTOSO*. U ziet verschillende regels met resource- en artikeltypen, die de gebruikte tijd (voor de technicus en het voertuig) en materialen (de machine en benodigdheden) weerspiegelen.
    3. Maak een nieuwe regel en voer vervolgens de volgende waarden in:
 
    |Projectnr.|Projecttaaknr.|Type|Nr.|Omschrijving|Hoeveelheid|
    |-------|------------|----|---|-----------|--------|  
    |J00010|220|Resource|EDGIN|Klantentraining|1|

2. Boek de tijd en kosten.
   1. Kies de actie **Boeken**.
   2. Bevestig dat u de regels wilt boeken door **Ja** te selecteren.

### Resultaten

- Projectposten en resourceposten van het type *Gebruik* worden gemaakt.
- Er worden artikelposten gemaakt om de voorraad negatief aan te passen.
- Op de projectkaart geven de kosten en prijzen in het gebied Taken de nieuwe saldi weer die in afwachting zijn van facturering.
- Op de projectkaart geeft het feitenblok Projectdetails de totalen van de prijzen weer.

## Een verkoopfactuur voor een project maken

### Scenario  

Simon moet een factuur maken en boeken die met de tijd en kosten van het project naar de klant moet worden verzonden.

### Stappen

1. Maak de verkoopfactuur.

    1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projecten** in en kies vervolgens de gerelateerde koppeling.  
    2. Kies in de lijst met projecten de actie **Projectverkoopfactuur maken**.
    3. Stel het filter **Projectnr.** in op *J00010*.
    4. Kies **OK** om de verkoopfactuur te genereren. U ontvangt een bevestiging van het aantal facturen dat is gegenereerd.

2. Boek de factuur met tijd en kosten.

   1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopfacturen** in en kies vervolgens de gerelateerde koppeling.  
   2. Selecteer de laatste factuur om deze ter beoordeling te openen.
   3. Kies de actie **Boeken**.

### Resultaten

- Projectposten en resourceposten van het type *Verkoop* worden gemaakt.
- Op de projectkaart geven de kosten en prijzen in het gebied Taken de nieuwe gefactureerde saldi weer.
- Op de projectkaart geeft het feitenblok Projectdetails de totalen van de prijzen in de sectie Gefactureerde prijs weer.
