---
title: Visuele signalen aanpassen over de activiteit van een indicatiestapel | Microsoft Docs
description: Stel een gekleurde indicator op een indicatiestapeltegel in om een aangepast visueel signaal van de activiteit van de indicatiestapel te bieden.
services: project-madeira
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: personalize, customize
ms.date: 10/01/2019
ms.author: solsen
redirect_url: admin-how-set-up-colored-indicator-on-cues
ms.openlocfilehash: 69defdcec64cfaa710af7d3f5b9b35e072c7c3d6
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2315192"
---
# <a name="set-up-a-colored-indicator-on-cues"></a>Een gekleurde indicator instellen voor indicatiestapels
U kunt indicatiestapels instellen die in het Rolcentrum worden weergegeven en die een indicator bevatten die van kleur verandert afhankelijk van de gegevenswaarden in de indicatiestapels.

De indicator wordt als een gekleurde balk weergegeven langs de bovenrand van de indicatiestapeltegel. Het geeft een visueel signaal van de status van de activiteit van de indicatiestapel. Het signaal kan gunstige of ongunstige condities aangeven om de gebruiker tot actie te laten overgaan. Als een indicatiestapel bijvoorbeeld doorlopende verkoopfacturen weergeeft, kunt u de indicator zo instellen dat deze groen (gunstig) is wanneer het totale aantal doorlopende verkoopfacturen kleiner is dan 10 en dat deze rood (ongunstig) is wanneer het totaal groter is dan 20.

Vanuit de pagina **Instelling indicatiestapel** kunt u indicatoren instellen voor alle indicatiestapels die beschikbaar zijn in de bedrijfsdatabase.

Als u de indicator wilt instellen, geeft u maximaal twee drempelwaarden op die de drie bereiken van gegevenswaarden definiëren (laag, gemiddeld en hoog) waarop u een andere kleur (of stijl) kunt toepassen.

## <a name="to-set-up-colored-indicators-on-cues"></a>Gekleurde indicatoren instellen voor indicatiestapels
1. Kies onder **Activiteiten** in uw rolcentrum **Indicatiestapels instellen**.  
   De pagina **Instelling indicatiestapel** wordt geopend. De pagina bevat de indicatoren die op het moment zijn ingesteld voor indicatiestapels.
2. Als u een indicator wilt wijzigen, bewerkt u de velden en wijzigt u bijvoorbeeld de waarden voor de verschillende drempelwaarden.  

De volgende tabel bevat de kleuren die overeenkomen met de opties van de velden **Stijl laag bereik**, **Stijl middenbereik** en **Stijl hoog bereik**.

| Optie | Kleur |
| --- | --- |
| **Geen** |Geen kleur (dezelfde kleur als de indicatiestapeltegel)|
| **Gunstig** |Groen |
| **Ongunstig** |Rood |
| **Dubbelzinnig** |Geel |
| **Ondergeschikt** |Grijs |

## <a name="see-also"></a>Zie ook
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
