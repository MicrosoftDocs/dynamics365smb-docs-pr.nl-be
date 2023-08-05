---
title: Een nieuw bewerkingsplan maken
description: Procedure om te leren hoe u alle informatie voor een nieuw bewerkingsplan handmatig in Business Central invoert.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
---
# Procedure: Een nieuw bewerkingsplan maken

In dit artikel voeren we u door de stappen om de demogegevens voor Contoso Coffee te gebruiken voor het handmatig instellen van een productiebewerkingsplan in [!INCLUDE [prod_short](../../includes/prod_short.md)].  

## Scenario

Oscar, de procestechnicus bij Contoso Coffee, besluit een nieuw bewerkingsplan op te stellen met de naam *Nieuw pad*. Omdat deze routering anders is dan elke andere routering bij Contoso Coffee, moet Oscar alle informatie voor de routering handmatig invoeren.  

## Stappen

1. Maak de bewerkingsplankop.  

    1. Kies het ![Lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), pictogram, voer **bewerkingsplannen** in en kies vervolgens de gerelateerde koppeling.  

    2. Kies de actie **Nieuw** en vul de velden in zoals is beschreven in de volgende tabel.  

        |Veld  |Waarde  |
        |---------|---------|
        |**Nr.** |1099|
        |**Beschrijving** |Nieuw pad|
2. Maak de bewerkingsplanregels.

    1. Voeg op het sneltabblad **Regels** een nieuwe regel toe en vull vervolgens de vulden in, zoals in de volgende tabel is beschreven.  

        |Veld  |Waarde  |
        |---------|---------|
        |**Bewerkingsnr.** |10|
        |**Soort** |Afdeling|
        |**Nr.** |100|
        |**Insteltijd** |20|
        |**Bewerkingstijd** |15|

    2. Voeg een nieuwe regel toe en vull vervolgens de vulden in, zoals in de volgende tabel is beschreven.  

        |Veld  |Waarde  |
        |---------|---------|
        |**Bewerkingsnr.** |20|
        |**Soort** |Afdeling|
        |**Nr.** |200|
        |**Insteltijd** |30|
        |**Bewerkingstijd** |5|
3. Certificeer het bewerkingsplan.

    1. Selecteer in het veld **Status** de optie *Gecertificeerd*.  

Het nieuwe bewerkingsplan is nu ingesteld.  

## Zie ook

[Inleiding tot de demogegevens voor Contoso Coffee](../contoso-coffee-intro.md)  
