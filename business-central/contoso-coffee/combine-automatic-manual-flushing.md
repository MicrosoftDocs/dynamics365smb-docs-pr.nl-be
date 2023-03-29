---
title: Automatisch en handmatig afboeken combineren
description: Procedure voor een productieplanner bij Contoso Coffee die automatisch en handmatig afboeken wil combineren.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# Procedure: Automatisch en handmatig afboeken combineren

In dit artikel voeren we u door de stappen om de demogegevens voor Contoso Coffee te gebruiken bij het afboeken.  

## Scenario

U bent de productieplanner bij Contoso Coffee. U moet een nieuwe productieorder maken voor tien eenheden van artikel SP-SCM1004, AutoDrip. Sommige componenten en bewerkingen worden voorwaarts afgeboekt, terwijl andere achterwaarts worden afgeboekt op basis van verschillende omstandigheden.

## Stappen

> [Opmerking!] Vergeet niet om de voorraad aan te passen door het artikeldagboek met beginsaldi te boeken.

1. Maak een vast geplande productieorder voor vijf eenheden van artikel **SP-SCM1004, AutoDrip** in vestiging *NOORD*. Zie [Procedure: Een nieuwe vast geplande productieorder maken en deze wijzigen](create-firm-planned-production-order-change.md) voor richtlijnen.  

2. Geef de productieorder vrij.

    1. Kies de actie **Status wijzigen**.  

    2. Stel op de pagina die verschijnt het veld **Nieuwe status** in op *Vrijgegeven* en kies vervolgens de knop **Ja**.  

        Er verschijnt een bericht met een statusbalk dat verwijst naar automatisch verbruik. Dit wordt gevolgd door een bevestigingsbericht dat de order is gewijzigd zodat deze de status *Vrijgegeven* heeft.  

    3. Kies de knop **OK** om de bevestigingsbericht te sluiten.

3. Bekijk de artikel- en capaciteitsposten voor de productieorder.

    1. Kies het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Vrijgegeven productieorder** in en kies vervolgens de gerelateerde koppeling.  

    2. Open de productieorder met de vijf eenheden van de AutoDrip-koffiemachine.  

    3. Kies de actie **Artikelposten**.  

        Het item **SP-BOM1305 Schroef Hex M3 Zink** wordt onmiddellijk afgeboekt met de volledige verwachte hoeveelheid. Sluit de pagina **Artikelposten**.  

    4. Kies de actie **Capaciteitsposten**.  Houd er rekening mee dat ook een post voor carrosseriemontage werd voltooid op het moment dat de order werd vrijgegeven. Sluit het venster **Capaciteitsposten**.

    U kunt componentartikelen handmatig afboeken met behulp van het verbruiks- of productiejournaal. Met handmatig afboeken kunt u de hoeveelheid aanpassen voordat u deze boekt. Bijvoorbeeld als er extra hoeveelheid nodig is om grondstoffen van lage kwaliteit te dekken.
4. Boek componenten handmatig af.  
    1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verbruiksdagboek** in en kies vervolgens de gerelateerde koppeling.  

    2. Kies de actie **Verbruik berekenen**.  

    3. Definieer op de aanvraagpagina **Verbruik berekenen**, op het sneltabbald **Productieorder**, een filter voor de specifieke order in het veld **Ordernr.** een kies vervolgens de knop **OK**. Nadat de pagina voor het aanvragen van batchtaken is gesloten, ziet u dat de pagina **Verbruiksdagboek** wordt gevuld met de componenten die handmatig moeten worden verbruikt.

    4. Kies de actie **Boeken**. Sluit het verbruiksdagboek.

5. Registreer handmatig output voor elektrische bedrading.  

    U moet de velden **Insteltijd** en **Bewerkingstijd** handmatig invullen. U kunt ook de werkelijk geproduceerde hoeveelheid en uitval opgeven. Voer *3* in als outputhoeveelheid en boek de output.

    1. Kies het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Outputdagboek** in en kies vervolgens de gerelateerde koppeling.  

    2. Maak op de pagina **Outputdagboek** een nieuwe journaalregel.  

    3. Geef in het veld **Ordernr.** de order op.  

    4. Kies de actie **Bewerkingsplan weergeven**.  

        De pagina **Outputdagboek** wordt alleen gevuld met de bewerkingsregel voor elektrische bedrading.

    5. Stel het veld **Bewerkingstijd** in op *10*.  

    6. Wijzig het veld **Hoeveelheid** van *5* naar *3*.

    7. Kies **Boeken**.  
    8. Sluit het outputdagboek.

6. Bekijk de artikelposten voor de productieorder.

    1. Kies op de pagina voor de productieorder de actie **Artikelposten**.  

    Het artikel **SP-BOM1302, Display bedieningspaneel** wordt geboekt met een hoeveelheid van *3*, gebaseerd op de werkelijke output, terwijl **SP-BOM1303, knop** wordt geboekt met de volledige verwachte hoeveelheid. Sluit de pagina **Artikelposten**.

7. Voltooi de productieorder.  

    1. Kies de actie **Status wijzigen**.
    2. Stel op de pagina die verschijnt het veld **Nieuwe status** in op *Voltooid* en kies vervolgens de knop **Ja**.  

        Er verschijnt een bericht met een statusbalk die het automatische verbruik weergeeft. Dit wordt gevolgd door een bevestigingsbericht dat de order is gewijzigd in een order met de status *Voltooid*. De voltooide productieorder heeft hetzelfde nummer als bij de status *Vrijgegeven*.
    3. Kies de knop **OK** om de bevestigingsbericht te sluiten.

8. Bekijk nogmaals de artikel- en capaciteitsposten voor de productieorder.

    1. Kies de actie **Capaciteitsposten**.  

        De invoer van de verpakkingshandelingen is voltooid op het moment dat de order werd vrijgegeven. De geproduceerde (output)hoeveelheid bedraagt *5*, ongeacht de output van de vorige stap. Sluit de pagina **Capaciteitsposten**.

    2. Kies de actie **Artikelposten**.  

        De hoeveelheid in de artikelpost van het type *Output* is gelijk is aan de outputhoeveelheid in de capaciteitspost. De verbruikte hoeveelheid van **SP-BOM1301 Behuizing AutoDrip**, en **SP-BOM1304, thermische karaf van RVS**, bedraagt 5 voor beide omdat de verwachte output en de werkelijke output hetzelfde zijn. 

    3. Sluit de pagina **Artikelposten**.  

Dat is alles voor het handmatig en automatisch afboeken van componenten.

## Zie ook

[Componenten afboeken op basis van de output van een bewerking](../production-how-to-flush-components-according-to-operation-output.md)  
[Inleiding tot de demogegevens voor Contoso Coffee](contoso-coffee-intro.md)  
