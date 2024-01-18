---
title: Een nieuwe vast geplande productieorder maken en deze wijzigen
description: Procedure voor een productieplanner bij Contoso Coffee die een vast geplande productieorder wil maken en deze vervolgens wil wijzigen.
ms.date: 12/12/2023
ms.topic: article
ms.service: dynamics365-business-central
author: brentholtorf
ms.author: bholtorf
---

# <a name="walkthrough-create-a-firm-planned-production-order-and-change-it"></a>Procedure: Een nieuwe vast geplande productieorder maken en deze wijzigen

In dit artikel voeren we u door de stappen om de demogegevens voor Contoso Coffee te gebruiken om te werken met productieorders.  

## <a name="scenario"></a>Scenario

Eduardo, de productieplanner bij Contoso Coffee, moet een nieuwe productieorder maken voor 10 eenheden van het artikel **SP-SCM1009, Airpot** die op 28 april moet worden geleverd. Eduardo plant dit met terugwerkende kracht in en bevestigt dat ze op 27 april met de bestelling kunnen beginnen.  

Kort nadat deze taak is voltooid, wordt Eduardo gevraagd om de bestelling te verhogen tot 50 eenheden. Door dit te doen, zorgt de achterwaartse planningsfunctionaliteit ervoor dat de startdatum van de bestelling te vroeg is. Dus plant Eduardo de order voorwaarts vanaf 23 april om een meer realistische einddatum te bepalen.  

## <a name="steps"></a>Stappen

1. Maak de initiële productieorder voor 10 eenheden van het artikel **SP-SCM1009, Airpot**.

    1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), pictogram, voer **vast geplande productieorders** in en kies vervolgens de gerelateerde koppeling.  

    2. Kies de actie **Nieuw** en vul de velden in zoals is beschreven in de volgende tabel.  

        |Veld  |Waarde  |
        |---------|---------|
        |**Bronsoort** |Artikel|
        |**Bronnr.** |SP-SCM1009|
        |**Aantal** |10|
        |**Vervaldatum**|April 28  |

    3. Kies de actie **Productieorder vernieuwen**.  

    4. Accepteer alle standaardinstellingen op de pagina **Productieorder vernieuwen** en kies vervolgens de knop **OK** om het proces te starten.  

        In de huidige opzet maakt dit proces gebruik van achterwaartse planning. In de nieuwe regel op de productieorder is de begindatum 26 april.  

2. Wijzig de hoeveelheid van de productieorder in 50 eenheden en plan de order.  

    1. Selecteer op het sneltabblad **Regels** van de **Productiestuklijst** de recent toegevoegde regel en voer vervolgens in het veld **Hoeveelheid** de waarde *50* in.  

3. Kies de actie **Productieorder vernieuwen**.  

    De begindatum is nu verschoven naar 20 april. Dit is geen acceptabele datum voor Eduardo.

4. Activeer een voorwaartse planning van de productieorder.

    1. Stel op het sneltabblad **Schema** het veld **Begindatum** in op *23 april*.

    De begindatum voor de order is nu 25 april en de einddatum is 2 mei. De vervaldatum voor de order wordt ingesteld op één dag later, namelijk 3 mei. Eduardo weet nu dat het tot 3 mei zal duren voordat de uitgebreide bestelling kan worden geleverd.

> [!NOTE]
> Voor het plannen van een order door de begin- of einddatum te wijzigen, is de batchtaak **Productieorder vernieuwen** niet nodig, omdat alle datums automatisch opnieuw worden berekend.

De nieuwe productieorder is nu ingesteld en er wordt voldaan aan de eisen van Eduardo.  

## <a name="see-also"></a>Zie ook

[Inleiding tot de demogegevens voor Contoso Coffee](../contoso-coffee-intro.md)  
