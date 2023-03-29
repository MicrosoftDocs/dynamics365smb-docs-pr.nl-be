---
title: Een nieuwe productiestuklijst en stuklijstversie maken
description: Procedure om nog een koffiezetapparaat te leren toevoegen aan de productlijn van Contoso Coffee in Business Central.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---

# Procedure: Een nieuwe productiestuklijst en stuklijstversie maken

In dit artikel voeren we u door de stappen om de demogegevens voor Contoso Coffee te gebruiken om te werken met een stuklijst in productieprocessen.  

## Scenario

Contoso Coffee heeft besloten om nog een koffiezetapparaat aan hun productlijn toe te voegen, namelijk **SP-SCM1008 Airpot Lite**. Dit koffiezetapparaat is identiek aan het bestaande artikel **SP-SCM1009 Airpot**, behalve dat de warmhoudplaat, **SP-BOM1104**, niet is inbegrepen. In een aparte stap wordt het aan/uit-lampje, **SP-BOM1106**, verwijderd voor een versie van de Airpot Lite BOM.

Oscar, de procestechnicus bij Contoso Coffee, moet een nieuwe productiestuklijst opzetten om de initiële onderdeelvereisten voor de Airpot Lite te definiëren. Hij moet vervolgens een nieuwe stuklijstversie opzetten, met een begindatum van 1 juli, om in overeenstemming te zijn met verdere plannen voor het uitbrengen van een nieuwe editie.

## Stappen

1. Maak een nieuwe productiestuklijst voor de Airpot Lite.

    1. Kies het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), pictogram, voer **productiestuklijst** in en kies vervolgens de gerelateerde koppeling.  

    2. Kies de actie **Nieuw** en vul de velden in zoals is beschreven in de volgende tabel.  

        |Veld  |Waarde  |
        |---------|---------|
        |**Nr.** |SP-SCM1008|
        |**Beschrijving** |Airpot Lite|
        |**Code van maateenheid**|Per stuk  |

2. Kopieer de stuklijstonderdelen uit productiestuklijst **SP-SCM1009**.

    1. Kies de actie **Stuklijst kopiëren**.

    2. Kies op de pagina **Productiestuklijsten** de regel voor **SP-SCM1009, Airpot** en kies vervolgens de knop **OK**.

3. Wijzig de onderdelen voor de nieuwe productiestuklijst zoals beschreven in het scenario.

    1. Selecteer op het sneltabblad **Regels** de regel voor het artikel **SP-BOM1104** en kies vervolgens de actie **Regel verwijderen**.  

4. Certificeer de nieuwe stuklijst.  

    1. Selecteer in het veld **Status** de optie *Gecertificeerd*.  

5. Maak een nieuwe productiestuklijstversie voor de Airpot Lite.

    1. Kies de actie **Versies**.

    2. Kies op de pagina **Prod.-stuklijstversieoverzicht** de actie **Nieuw** en vul de velden in zoals is beschreven in de volgende tabel.  

        |Veld  |Waarde  |
        |---------|---------|
        |**Versiecode** |02|
        |**Beschrijving** |Airpot Lite, v2|
        |**Code van maateenheid**|Per stuk  |  
        |**Begindatum**|Juli 01  |  

6. Kopieer de onderdeelregels uit de productiestuklijst naar de nieuwe stuklijstversie.

    1. Kies de actie **Stuklijst kopiëren** en kies vervolgens de knop **Ja** om de onderdelen van de originele productiestuklijst te kopiëren.

7. Verwijder het artikel **SP-BOM1106, Aan/uit-lampje** uit de versieonderdelen.

8. Certificeer de nieuwe stuklijstversie.

    1. Selecteer in het veld **Status** de optie *Gecertificeerd*.  

    2. Sluit de stuklijstversie

Het nieuwe koffiezetapparaat is nu opgezet als een productiestuklijst met één versie.  

## Zie ook

[Inleiding tot de demogegevens voor Contoso Coffee](contoso-coffee-intro.md)  
