---
title: Overzicht van dimensiesetposten | Microsoft Docs
description: In dit onderwerp wordt beschreven hoe dimensiesetposten worden opgeslagen en geboekt in Dynamics 365.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dimension
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8ed544486af6949932814bf97d99293f1ef17ee2
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2303592"
---
# <a name="dimension-set-entries-overview"></a>Overzicht dimensiesetposten
In dit onderwerp wordt beschreven hoe dimensiesetposten worden opgeslagen en geboekt in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="dimension-sets"></a>Dimensiesets  
Een dimensieset is een unieke combinatie dimensiewaarden. Een dimensieset wordt als dimensiesetposten in de database opgeslagen. Elke dimensiesetpost vertegenwoordigt één dimensiewaarde. De dimensiesetpost wordt geïdentificeerd door een gemeenschappelijke dimensieset-id die is toegewezen aan elke dimensiesetpost die tot de dimensieset behoort.  

In het volgende voorbeeld ziet u een dimensieset met drie dimensiesetposten. De dimensieset wordt geïdentificeerd door een dimensieset-id 108.  

|Dimensieset-id|Dimensiecode|Dimensiewaardecode|Dimensiewaardenaam|  
|----------------------|--------------------|--------------------------|--------------------------|  
|108|DISTRICT|70|Noord-Amerika|  
|108|BEDRIJFSGROEP|HOME|Home|  
|108|KSTNPLAATS|VERKOOP|Verkoop|  

## <a name="dimension-set-entries"></a>Dimensiesetposten  
Dimensiesets worden opgeslagen in de tabel **Dimensiesetpost** als dimensiesetposten met dezelfde dimensieset-id.  

![Stroom van dimensiesetposten](media/dimensionentrynav7.png "Stroom van dimensiesetposten")  

Wanneer u een nieuwe dagboekregel, documentkop of documentregel maakt, kunt u een combinatie van dimensiewaarden opgeven. In plaats van elke dimensiewaarde expliciet in de database op te slaan, wordt een dimensieset-id toegewezen aan de dagboekregel, documentkop of documentregel om zo de dimensieset op te geven.  

Wanneer u de pagina **Dimensiesetposten bewerken** bewerkt en sluit, wordt gecontroleerd of de combinatie van dimensiewaarden als een dimensieset in de tabel voorkomt. Als de combinatie in de tabel voorkomt, wordt de overeenkomende dimensieset-id toegewezen aan de dagboekregel, documentkop of documentregel. Anders wordt een nieuwe dimensieset toegevoegd aan de tabel en wordt de nieuwe dimensieset-id toegewezen aan de dagboekregel, documentkop of documentregel.

## <a name="codeunit-408-dimension-management"></a>Codeunit 408 Dimensiebeheer
Codeunit 408, Dimensiebeheer, is een functiebibliotheek die veel voorkomende taken afhandelt die verband houden met dimensies, zoals kopiëren van de ene tabel naar de andere of van het ene document naar het andere.

## <a name="performance-improvement"></a>Prestatieverbetering  
Door dimensiesets eenmalig in de database op te slaan, wordt databaseruimte bespaard en wordt de algehele prestatie verbeterd.  

## <a name="see-also"></a>Zie ook  
[Ontwerpdetails: Dimensiecombinaties zoeken](design-details-searching-for-dimension-combinations.md)   
[Ontwerpdetails: Tabelstructuur](design-details-table-structure.md)   
[Ontwerpdetails: Dimensiesetposten](design-details-dimension-set-entries.md)   
