---
title: Nieuwe capaciteit instellen
description: Procedure om te leren hoe u een nieuwe afdeling opzet met een capaciteitskalender voor één ploeg in Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: brentholtorf
ms.author: bholtorf
---

# Procedure: Nieuwe capaciteit instellen

In dit artikel voeren we u door de stappen om de demogegevens voor Contoso Coffee te gebruiken voor beheren van capaciteit.  

## Scenario

U bent de productieplanner bij Contoso Coffee. Als reactie op veranderingen op de werkvloer moet u een nieuwe Testafdeling inrichten. De nieuwe afdeling heeft één bewerkingsplaats: Testing. De nieuwe centra moeten een capaciteitskalender hebben voor één ploeg van 08.00 uur tot 16.00 uur, van maandag tot en met vrijdag.  

## Stappen

1. Stel de afdeling in.

    1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **afdelingen** in en kies vervolgens de gerelateerde koppeling.  

    2. Kies de actie **Nieuw** en vul de velden in zoals is beschreven in de volgende tabel.  

        |Veld  |Waarde  |
        |---------|---------|
        |**Nr.** |700|
        |**Naam** |Testafdeling|
        |**Afdelingsgroepcode** |1, Productieafdeling|
        |**Directe kostprijs**|3.25|
        |**Kostprijsberekening**|Tijd|
        |**Afboekingsmethode**|Handmatig|
        |**Prod.-boekingsgroep**|GEEN BTW</br></br>Houd er rekening mee dat deze selectie afhankelijk is van uw boekhoudconfiguratie en land/regio.|
        |**Eenheidscode** |MINUTEN|
        |**Capaciteit** |1|
        |**Efficiëntie %** |90|
        |**Prod.-agenda** |1|

        In het veld **Productieagendacode** betekent de instelling 1 één ploeg van maandag tot vrijdag.

    3. Sluit de afdelingskaart.

2. Stel de bewerkingsplaatsen in.

    1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **afdelingen** in en kies vervolgens de gerelateerde koppeling.  

    2. Kies de actie **Nieuw** en vul de velden in zoals is beschreven in de volgende tabel.  

        |Veld  |Waarde  |
        |---------|---------|
        |**Nr.** |760|
        |**Naam** |Testen|
        |**Afdelingsnr.** |700, Testafdeling|
        |**Directe kostprijs**|3.25|
        |**Afboekingsmethode**|Handmatig|
        |**Prod.-boekingsgroep**|GEEN BTW</br></br>Houd er rekening mee dat deze selectie afhankelijk is van uw boekhoudconfiguratie en land/regio.|
        |**Capaciteit** |1|
        |**Efficiëntie** |90|
    3. Vouw het sneltabblad **Routering instellen** uit en voer in het veld **Insteltijd** *10* in.  

3. Bereken de agenda voor de capaciteit van de bewerkingsplaats.  

    1. Kies de actie **Agenda**.  

    2. Stel op de pagina **Bewerkingsplaatsagenda** in het sneltabblad **Matrixopties** het veld **Weergeven op** in per *Maand*.  

    3. Kies de actie **Matrix weergeven**.  

    4. Kies op de pagina **Matrix Bewerkingsplaatsagenda** de actie **Berekenen**.  

    5. Stel op de pagina **Bewerkingsplaatsagenda berekenen** in het sneltabblad **Opties** het veld **Begindatum** in op *01 januari*.  

    6. Stel het veld **Einddatum** in op 31 december.  

    7. Selecteer op het sneltabblad **Bewerkingsplaats** in het filterveld **Nr.** de optie *760, testen*.  

    8. Kies de knop **Ok**. Nadat de batchtaak is voltooid, keert het terug naar de pagina **Matrix Bewerkingsplaatsagenda**.  

    9. Kies de actie **Vernieuwen**.  

    10. Ga op de regel voor bewerkingsplaats 760, Testen, naar de waarde in de kolom januari.  

Op de pagina **Agendaposten** zijn de dagelijkse capaciteitsvermeldingen in het veld **Capaciteit (totaal)** voor 480 minuten. Dit komt overeen met één ploeg van acht uur per werkdag. Ook in het veld **Capaciteit (effectief)** staat 432 minuten. Dit weerspiegelt het efficiëntiepercentage van 90 procent dat u aan het bewerkingscentrum hebt toegewezen.  

## Zie ook

[Inleiding tot de demogegevens voor Contoso Coffee](../contoso-coffee-intro.md)  
