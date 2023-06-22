---
title: Uitstel in rapporten van het Verkoopdagboek en Inkoopdagboek
description: Leer hoe u uitstellingen kunt instellen en gebruiken in rapporten van het Verkoopdagboek en Inkoopdagboek in de Belgische versie van Business Central.
author: altotovi
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'deferral, sales ledger, purchase ledger'
ms.search.form: '279, 1700, 1701'
ms.date: 03/13/2023
ms.author: altotovi
---

# <a name="deferrals-in-sales-ledger-and-purchase-ledger-reports" />Uitstel in rapporten van het Verkoopdagboek en Inkoopdagboek

Wanneer u uitstellingen gebruikt, moeten de rapporten van het Verkoopdagboek en Inkoopdagboek in de Belgische versie van Dynamics 365 Business Central alleen de originele vermeldingen weergeven uit facturen en creditnota´s en niet de vermeldingen die zijn gemaakt met uitstellingen.

## <a name="set-up-deferrals" />Uitstellingen instellen

1. Selecteer het pictogram ![lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Broncode instellen** in en selecteer vervolgens de gerelateerde koppeling.  
2. Vul op het sneltabblad **Algemeen** de vereiste veldgegevens in, zoals in de volgende tabel is beschreven.  

    |      Veld   |         Beschrijving        |
    |--------------|----------------------------|
    | **Algemeen uitstel** | De **Broncode** die het systeem gebruikt voor uitstellingen die worden gemaakt door boekingen in Algemene dagboeken. |
    | **Verkoopuitstel** | De **Broncode** die het systeem gebruikt voor uitstellingen die worden gemaakt door boekingen in Verkoopdocumenten. |
    | **Inkoopuitstel** | De **Broncode** die het systeem gebruikt voor uitstellingen die worden gemaakt door boekingen in Inkoopdocumenten. |
    
3. Selecteer **OK**.

> [!NOTE]
> U kunt specifieke broncodes configureren voor uitstelboekingen of dezelfde broncode gebruiken voor het algemene dagboek, verkoopdagboeken en inkoopdagboeken.  

## <a name="belgium-sales-ledger-and-purchase-ledger-reports" />Belgische rapporten van het Verkoopdagboek en Inkoopdagboek

Als de uitstelvermeldingen een specifieke broncode hebben, kunt u de rapportweergave aanpassen door **Uitstelvermeldingen uitsluiten** te selecteren in de rapporten van het Verkoopdagboek en het Inkoopdagboek. 

Wanneer u de optie instelt op **Uit**, geeft het rapport alle vermeldingen weer die betrekking hebben op een specifieke periode. Als de schakelaar is ingesteld op **Aan**, sluit het rapport de uitstelvermeldingen uit.  

> [!NOTE]
> De volgende perioden van één maand bevat geen uitstelvermeldingen als de schakelaar op **Aan** staat.

## <a name="see-also" />Zie ook

[Belgische lokale functionaliteit](belgium-local-functionality.md)
[Dagboeksjablonen verplicht maken in de Belgische versie](specify-journal-template-mandatory.md)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
