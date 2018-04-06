---
title: Tips en trucs - RapidStart Services | Microsoft Docs
description: Wanneer u bedrijven configureert met RapidStart Services, zijn er enkele tips en trucs die u kunt gebruiken om uw implementatie vlot te laten verlopen.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/05/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e43859a6095f0087c12d0f9c071c0504d3781ad2
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="tips-and-tricks-rapidstart-services"></a>Tips en trucs: RapidStart Services
Wanneer u bedrijven configureert met RapidStart Services, zijn er enkele tips en trucs die u kunt gebruiken om uw implementatie vlot te laten verlopen.  

## <a name="take-advantage-of-configuration-templates"></a>Gebruikmaken van configuratiesjablonen  
Configuratiesjablonen kunnen u helpen uw implementatie te stroomlijnen. U kunt via deze sjablonen vergelijkbare klanten opnemen in segmenten en een implementatieprotocol ontwikkelen die alle klanten in een segment op een vergelijkbare wijze behandelt. Op die manier kunt u meteen een preconfiguratie toepassen op elk segment en doorgaan met een snelle implementatie.  

## <a name="configuration-questionnaires"></a>Configuratievragenlijsten  
Om het invullen van een configuratievragenlijst sneller te laten verlopen, kunt u standaardantwoorden definiëren om aanbevolen procedures aan te geven.  

## <a name="batch-creation-of-journal-lines"></a>Dagboekregels in batch aanmaken  
Het is raadzaam dat u de hulpprogramma's voor gegevensmigratie gebruikt voor het migreren van dagboekposten. Als u een batchtaak gebruikt om dagboekregels te maken, heeft deze een beperkt bereik en maakt deze enkel pre-standaardvelden in een dagboek. De rest van het dagboek moet vervolgens handmatig worden voltooid.  

## <a name="migrating-transactions"></a>Transacties migreren  
Het is raadzaam om beginsaldi in de volgende volgorde te migreren.  

1.  Migreer beginsaldi uit het grootboek zonder de subgrootboeken van de grootboekrekening te gebruiken. Gebruik specifieke uitstellende rekeningen voor beginsaldi, waarbij voor elk subgrootboek een rekening is ingesteld. Stel de uitstellende rekeningen in zodat ze directe boekingen toestaan.  
2.  Migreer open klantenposten.  
3.  Migreer open artikelposten.  
4.  Migreer open vaste-activumposten.  

## <a name="see-also"></a>Zie ook  
[Een bedrijf met RapidStart Services instellen](admin-set-up-a-company-with-rapidstart.md)  
[Beheer](admin-setup-and-administration.md)
