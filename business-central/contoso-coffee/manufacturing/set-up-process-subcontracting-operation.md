---
title: Een uitbestedingsbewerking instellen en verwerken
description: Procedure om te leren hoe u een uitbestedingsbewerking in Business Central instelt en verwerkt.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# <a name="set-up-and-process-a-subcontracting-operation"></a><a name="set-up-and-process-a-subcontracting-operation"></a>Een uitbestedingsbewerking instellen en verwerken

In dit artikel voeren we u door de stappen om de demogegevens voor Contoso Coffee te gebruiken bij het uitbesteden.

## <a name="scenario"></a><a name="scenario"></a>Scenario

U bent de productieplanner bij Contoso Coffee. Wegens capaciteitsbeperkingen bent u van plan een onderaannemer in te schakelen om het artikel **SP-SCM1009, Airpot** te produceren.

Hier maakt u een nieuwe vrijgegeven productieorder voor 12 eenheden van artikel SP-SCM1009, Airpot, met behulp van Routing - SP-SCM1009-SUB-2. Gebruik het uitbestedingsvoorstel om een inkooporder voor de productie te genereren en voltooi de bewerking door de inkooporder te ontvangen en te factureren.

## <a name="steps"></a><a name="steps"></a>Stappen

1. Maak een nieuwe vrijgegeven productieorder voor 12 eenheden van het artikel SP-SCM1009, Airpot.

    1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vrijgegeven productieorder** in en kies vervolgens de gerelateerde koppeling.  

    2. Kies de actie **Nieuw** en vul de velden in zoals is beschreven in de volgende tabel.  

        |Veld  |Waarde  |
        |---------|---------|
        |**Bronsoort** |Artikel|
        |**Bronnr.** |SP-SCM1009|
        |**Aantal** |100|
    3. Kies de actie **Productieorder vernieuwen**.  

2. Vervang de routing door SP-SCM1009-SUB-2 in de productieorderregel en vernieuw vervolgens de productieorder, maar alleen voor routing.  

    1. Voeg het veld Nummer productierouting toe aan de Regels in de Vrijgegeven productieorder.<!--in code, this is marked as visible=false-->

    2. Verander het veld **Routingnummer** van *SP-SCM1009-SERIAL* in *SP-SCM1009-SUB-2*.  

    3. Kies de actie **Productieorder vernieuwen**.  

    4. Wis op de pagina **Productieorder vernieuwen** de velden **Regels** en **Materiaalbehoefte** zodat de taak alleen voor Routing wordt uitgevoerd, en kies vervolgens de knop **OK**.

3. Gebruik het uitbestedingsvoorstel om een inkooporder te genereren voor de uitbestede bewerking op de productieorder die u in stap 2 hebt gemaakt.  

    1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Uitbestedingsvoorstellen** in en kies vervolgens de gerelateerde koppeling.  

    2. Kies de actie **Uitbestedingen berekenen**.

    3. Selecteer het veld **Planningsboodschap accepteren** voor de nieuwe regel.

    4. Kies de actie **Planningsboodschap uitvoeren**.  

    5. Accepteer op de pagina **Planningsboodschap uitvoeren - Ink.-voorstel** alle standaardwaarden en kies vervolgens de knop **OK**.

    6. Wanneer de batchtaak is voltooid, kiest u de knop **OK** om het uitbestedingsvoorstel te sluiten.  

4. Ontvang en factuureer de inkooporder.  

    1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **inkooporders** in en kies vervolgens de gerelateerde koppeling.  

    2. Zoek in de lijst **Inkooporders** zoek de inkooporder van de leverancier 82000 Onderaannemer.

    3. Vul het veld **Factuurnr. leverancier** *542349* in.

    4. Op het sneltabblad **Regels** de regel en stel vervolgens het veld **Directe kosten** in op *18*.

    5. Kies de actie **Boeken**.  

    6. Kies in het aanvraagbericht de optie **Ontvangen en factureren**.  

De uitvoer van artikel SP-SCM1009 Airpot is nu geregistreerd.

## <a name="see-also"></a><a name="see-also"></a>Zie ook

[Inleiding tot de demogegevens voor Contoso Coffee](../contoso-coffee-intro.md)  
