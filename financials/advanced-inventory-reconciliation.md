---
title: 'Geavanceerd: Voorraadreconciliatie| Microsoft Docs'
description: Beschrijft hoe uw voorraadwaarde wordt gereconcilieerd met het grootboek.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: post inventory cost to G/L, reconcile inventory
ms.date: 02/15/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 7eb07530fe80f871ef113c95e48bf89da6c29db0
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
## <a name="advanced-inventory-reconciliation"></a>Geavanceerd: Voorraadreconciliatie
Als u voorraadtransacties (bijvoorbeeld verkoopverzendingen, inkoopfacturen of voorraadherwaarderingen) boekt, worden de gewijzigde artikelkosten vastgelegd in artikelwaardeposten. Om deze wijziging van voorraadwaarde door te voeren in uw financiële boeken, worden de voorraadkosten automatisch geboekt naar de gerelateerde voorraadrekeningen in het grootboek. Voor iedere voorraadtransactie die u boekt, worden overeenkomende waarden naar de voorraadrekening geboekt, de correctierekening en de KPV-rekening in het grootboek.

Hoewel voorraadkosten automatisch naar het grootboek worden geboekt, moeten de kosten van goederen toch worden doorgestuurd naar de gerelateerde uitgaande verkooptransactie, vooral in situaties waarin u goederen verkoopt voordat u de inkoop van die goederen factureert. Dit wordt kostenwaardering genoemd. Artikelkosten worden automatisch aangepast als u artikeltransacties boekt, maar u kunt artikelkosten ook handmatig wijzigen. Zie [Procedure: Artikelkosten herwaarderen](inventory-how-adjust-item-costs.md) voor meer informatie.

## <a name="see-also"></a>Zie ook
[Voorraad](inventory-manage-inventory.md)  
[Geavanceerd: De beste prijs berekenen](advanced-best-price-calculation.md)

