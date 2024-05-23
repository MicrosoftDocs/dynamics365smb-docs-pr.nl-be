---
title: Procedure van serviceorders voor serviceartikelen
description: In dit artikel wordt u door verschillende kernprocessen geleid waarbij serviceorders en artikelen betrokken zijn.
author: andreipa
ms.author: andreipa
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 05/31/2023
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Procedure van serviceorders voor serviceartikelen

Deze procedure demonstreert verschillende kernprocessen:

- Een ad-hocserviceorder maken en de reparatie van het artikel registreren
- Een leenartikel aan de klant geven voor een reparatieperiode
- De serviceorder boeken en factureren
    
## Een serviceorder maken

### Scenario  

Charles, de servicemanager, maakt een serviceorder voor een reparatiescenario en leent een leenauto aan de klant uit voor de reparatietijd.

### Stappen

1. Maak de serviceorder handmatig voor het artikel dat gerepareerd moet worden.
   1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Serviceorders** in
   2. Kies de actie **Nieuw**.
   3. Voer **10000** in het veld Klantnr. in.
   4. Selecteer **REPARATIE** voor het veld **Serviceordersoort**.
   5. Selecteer op de regels **S-100** als **Artikelnr.**
2. Optioneel
   1. Kies de regelactie **Problemen oplossen** om mogelijke oplossingen te bekijken.
   2. Kies de regelactie **Rel. probleem-/oplossingscodes**
   3. Selecteer *GELUID* als **Symptoomcode**
   4. Selecteer *5-2 Hard geluid tijdens het koffiezetten* als **Foutcode** en sluit de pagina. Foutcode en oplossingscode worden op regels bijgewerkt.
3. Leen een vervanging uit terwijl het artikel wordt gerepareerd
   1. Selecteer op de regels **LOANER1** als het uitleenartikelnr. Bevestig de uitgifte van het uitleenartikel door **Ja** te selecteren om het uitleenartikel uit te lenen. 
   2. Kies de Functies-actie **Std. servicecodes ophalen**, selecteer de standaardcode die is gekoppeld aan de servicegroep en selecteer **OK**.
   
### Resultaten

- Er wordt een serviceorder gemaakt voor het artikel
- In het servicedocumentlogboek van de serviceorder worden de leenactiviteiten weergegeven.
- De lener zal een grootboekboeking hebben om de lening weer te geven.
   

## Registreer uitgevoerd werk, markeer lener als geretourneerd.

### Scenario  

De servicemonteur markeert het uitleenartikel als geretourneerd en registreert de uitgevoerde werkzaamheden.

### Stappen

1. Zoek de servicetaak en registreer de tijd 
   1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Servicetaken** in en kies vervolgens de gerelateerde koppeling.
   2. Zoek de serviceorder waarvoor u tijd wilt invoeren.
   3. Kies de actie **Artikelwerkbon**.
   4. Geef de volgende informatie op

    |Type|Nr.|Hoeveelheid|
    |----|---|--------|  
    |Artikel|SER102|2|

   4. Selecteer *VOLTOOID* in het veld **Herstelstatuscode**
    
2. Markeer het uitleenartikel als geretourneerd
   1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Uitleenartikelen** in en kies vervolgens de gerelateerde koppeling.
   2. Zoek het uitleenartikel en markeer het als geretourneerd.
   3. Kies de actie **Ontvangen** 
   4. Bevestig de retournering van het uitleenartikel door **Ja** te selecteren om het uitleenartikel te retourneren.
      
### Resultaten

- In het **Servicedocumentlogboek** van de serviceorder worden de leenactiviteiten weergegeven.
- De lener zal een grootboekpost hebben om de ontvangst weer te geven.


### Scenario  

Charles, de servicemanager, boekt de voltooide serviceorder.

1. De serviceorder zoeken 
   1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Serviceorders** in en kies vervolgens de gerelateerde koppeling.
   2. Zoek de serviceorder die u wilt boeken.

2. Boek de factuur op de serviceorder
   1. Kies de actie **Boeken** om de serviceorder te voltooien, selecteer de actie **Verzenden en factureren** en kies vervolgens de knop **OK**.
   2. Bevestig het openen van de geboekte factuur door **Ja** te selecteren. 
### Resultaten

- de **geboekte servicefactuur** wordt gemaakt.
- de **Serviceposten** die zijn gekoppeld aan het artikel en de resource, worden gemaakt

## Zie ook
[Procedure van servicecontracten voor serviceartikelen](service-contract-flow.md)  
[Onderhoud](../../service-service.md)
