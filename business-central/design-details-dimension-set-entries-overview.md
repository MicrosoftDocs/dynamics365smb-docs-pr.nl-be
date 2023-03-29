---
title: Overzicht dimensiesetposten
description: Dit artikel geeft u een overzicht van hoe dimensiesetposten worden opgeslagen als dimensiesetposten en hoe ze worden geboekt.
author: SorenGP
ms.topic: overview
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 06/14/2021
ms.author: edupont
---
# Overzicht dimensiesetposten
In dit onderwerp wordt beschreven hoe dimensiesetposten worden opgeslagen en geboekt in [!INCLUDE[prod_short](includes/prod_short.md)].  

## Dimensiesets  
Een dimensieset is een unieke combinatie dimensiewaarden. Een dimensieset wordt als dimensiesetposten in de database opgeslagen. Elke dimensiesetpost vertegenwoordigt één dimensiewaarde. De dimensiesetpost wordt geïdentificeerd door een gemeenschappelijke dimensieset-id die is toegewezen aan elke dimensiesetpost die tot de dimensieset behoort.  

In het volgende voorbeeld ziet u een dimensieset met drie dimensiesetposten. De dimensieset wordt geïdentificeerd door een dimensieset-id 108.  

|Dimensieset-id|Dimensiecode|Dimensiewaardecode|Dimensiewaardenaam|  
|----------------------|--------------------|--------------------------|--------------------------|  
|108|DISTRICT|70|Noord-Amerika|  
|108|BEDRIJFSGROEP|HOME|Home|  
|108|KSTNPLAATS|VERKOOP|Verkoop|  

## Dimensiesetposten  
Dimensiesets worden opgeslagen in de tabel **Dimensiesetpost** als dimensiesetposten met dezelfde dimensieset-id.  

![Stroom van dimensiesetposten.](media/dimensionentrynav7.png "Stroom van dimensiesetposten")  

Wanneer u een nieuwe dagboekregel, documentkop of documentregel maakt, kunt u een combinatie van dimensiewaarden opgeven. In plaats van elke dimensiewaarde expliciet in de database op te slaan, wordt een dimensieset-id toegewezen aan de dagboekregel, documentkop of documentregel om zo de dimensieset op te geven.  

Wanneer u de pagina **Dimensiesetposten bewerken** bewerkt en sluit, wordt gecontroleerd of de combinatie van dimensiewaarden als een dimensieset in de tabel voorkomt. Als de combinatie in de tabel voorkomt, wordt de overeenkomende dimensieset-id toegewezen aan de dagboekregel, documentkop of documentregel. Anders wordt een nieuwe dimensieset toegevoegd aan de tabel en wordt de nieuwe dimensieset-id toegewezen aan de dagboekregel, documentkop of documentregel.

## Codeunit 408 Dimensiebeheer
Codeunit 408, Dimensiebeheer, is een functiebibliotheek die veel voorkomende taken afhandelt die verband houden met dimensies, zoals kopiëren van de ene tabel naar de andere of van het ene document naar het andere.

## Prestatieverbetering  
Door dimensiesets eenmalig in de database op te slaan, wordt databaseruimte bespaard en wordt de algehele prestatie verbeterd.  

## Zie ook
[Ontwerpdetails: Dimensiecombinaties zoeken](design-details-searching-for-dimension-combinations.md)   
[Ontwerpdetails: Tabelstructuur](design-details-table-structure.md)   
[Ontwerpdetails: Dimensiesetposten](/dynamics365/business-central/design-details-dimension-set-entries-overview)   


[!INCLUDE[footer-include](includes/footer-banner.md)]