---
title: 'Ontwerpdetails: Magazijnoverzicht | Microsoft Docs'
description: Om de fysieke verwerking van artikelen op het niveau van zones en opslaglocaties te ondersteunen, moeten alle gegevens worden getraceerd van elke transactie of verplaatsing in het magazijn. Dit wordt beheerd in de tabel **Magazijnpost**. Elke transactie wordt opgeslagen in een magazijnjournaal.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 8842bd23f6d2d470599afe9b4382b35cec3d9251
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4749555"
---
# <a name="design-details-warehouse-overview"></a>Ontwerpdetails: Magazijnoverzicht
Om de fysieke verwerking van artikelen op het niveau van zones en opslaglocaties te ondersteunen, moeten alle gegevens worden getraceerd van elke transactie of verplaatsing in het magazijn. Dit wordt beheerd in de tabel **Magazijnpost**. Elke transactie wordt opgeslagen in een magazijnjournaal.  

Magazijndocumenten en een magazijndagboek worden gebruikt om artikelmutaties in het magazijn te registreren. Telkens wanneer een artikel in het magazijn wordt verplaatst, ontvangen, opgeslagen, gepickt, verzonden of aangepast, worden magazijnposten vastgelegd om de fysieke informatie op te slaan over zone, opslaglocatie en aantal.

De tabel **Opslaglocatie-inhoud** wordt gebruikt om alle verschillende dimensies van de inhoud van een opslaglocatie per artikel, zoals eenheid, en maximum- en minimumaantal te verwerken. De tabel **Opslaglocatie-inhoud** bevat ook stroomvelden naar de magazijnposten, magazijninstructies en magazijndagboekregels, die ervoor zorgen dat de beschikbaarheid van een artikel per opslaglocatie en een opslaglocatie voor een artikel snel kunnen worden berekend. Zie voor meer informatie [Ontwerpdetails: Beschikbaarheid in het magazijn](design-details-availability-in-the-warehouse.md).  

Wanneer artikelboekingen buiten de magazijnmodule plaatsvinden, wordt een standaardherwaarderingsopslaglocatie per vestiging gebruikt om magazijnposten te synchroniseren met voorraadposten. Tijdens fysieke inventarisatie van het magazijn worden eventuele verschillen tussen de berekende en getelde aantallen geregistreerd in de correctieopslaglocatie en vervolgens als corrigerende artikelposten geboekt. Zie [Ontwerpdetails: Integratie met voorraad](design-details-integration-with-inventory.md) voor meer informatie.  

De volgende illustratie geeft gebruikelijke magazijnstromen aan.  

![Overzicht van magazijnprocessen](media/design_details_warehouse_management_overview.png "Overzicht van magazijnprocessen")  

## <a name="basic-or-advanced-warehousing"></a>Elementaire of geavanceerde magazijnfuncties  
De magazijnfunctionaliteit in [!INCLUDE[prod_short](includes/prod_short.md)] kan in verschillende complexiteitsniveaus worden geïmplementeerd, afhankelijk van de processen en het ordervolume van een bedrijf. Het belangrijkste verschil is dat de activiteiten per order worden uitgevoerd bij standaardmagazijnbeheer, terwijl ze worden samengevoegd voor meerdere orders bij geavanceerd magazijnbeheer.  

 Om te onderscheiden tussen de verschillende complexiteitniveaus wordt in deze documentatie verwezen naar twee algemene denominaties, elementaire en geavanceerde magazijnfuncties. Dit eenvoudig onderscheid omvat meerdere verschillende complexiteitniveaus zoals gedefinieerd door productgranules en vestigingsinstellingen, waarbij elk wordt ondersteund door verschillende UI-documenten. Zie voor meer informatie [Ontwerpdetails: Magazijninstelling](design-details-warehouse-setup.md).  

> [!NOTE]  
>  Het meest geavanceerde niveau van magazijnbeheer wordt in deze documentatie "WMS-installaties" genoemd, aangezien voor dit niveau de meest geavanceerde granule is vereist: Warehouse Management System.  

 De volgende verschillende UI-documenten worden gebruikt in standaard- en geavanceerde magazijnfuncties.  

## <a name="basic-ui-documents"></a>Elementaire UI-documenten  

-   **Voorraadopslag**  
-   **Voorraadpick**  
-   **Voorraadverplaatsing**  
-   **Artikeldagboek**  
-   **Artikelherindelingsdagboek**  
-   (Diverse lijsten)  

## <a name="advanced-ui-documents"></a>Geavanceerde UI-documenten  

-   **Magazijnontvangst**  
-   **Opslagvoorstel**  
-   **Magazijnopslag**  
-   **Pickvoorstel**  
-   **Magazijnpick**  
-   **Verplaatsingsvoorstel**  
-   **Magazijnverplaatsing**  
-   **Interne mag.-pick**  
-   **Interne mag.-opslag**  
-   **Voorstel opslaglocatieaanmaak**  
-   **Voorstel opslaglocatie-inhoudaanmaak**  
-   **Mag.-artikeldagboek**  
-   **Mag.-herindelingsdagboek**  
-   (Diverse lijsten)  

Voor meer informatie over elk document raadpleegt u de respectievelijke paginaonderwerpen.  

### <a name="terminology"></a>Terminologie  
Ter afstemming met de financiële begrippen van inkopen en verkopen verwijst de [!INCLUDE[prod_short](includes/prod_short.md)]-magazijndocumentatie naar de volgende termen voor artikelstromen in het magazijn.  

|Term|Description|  
|----------|---------------------------------------|  
|Inkomende stroom|Artikelen die naar de magazijnvestiging worden verplaatst, zoals inkopen en inkomende transfers.|  
|Interne stroom|Artikelen die binnen de magazijnvestiging worden verplaatst, zoals productiecomponenten en output.|  
|Uitgaande stroom|Artikelen die uit de magazijnvestiging worden verplaatst, zoals verkopen en uitgaande transfers.|  

## <a name="see-also"></a>Zie ook  
 [Ontwerpdetails: Magazijnbeheer](design-details-warehouse-management.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]