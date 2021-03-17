---
title: Artikelen blokkeren vanuit Verkoop of Inkoop
description: U kunt voorkomen dat een artikel bijvoorbeeld wordt gebruikt in verkoop- of inkoopdocumenten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 87628f1983e0bafda9119ef3729dbb142c761b1a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5393136"
---
# <a name="block-items-from-sales-or-purchasing"></a>Artikelen blokkeren vanuit Verkoop of Inkoop
U kunt voorkomen dat een artikel wordt ingevoerd op regels in verkoop- of inkoopdocumenten en u kunt voorkomen dat het wordt geboekt in een transactie. Dit is bijvoorbeeld handig wanneer een artikel een bekend defect heeft. Als iemand een geblokkeerd item kiest voor een verkoop- of aankoopdocument, zal een bericht hen laten weten dat het artikel is geblokkeerd.

De volgende tabel laat zien wat er gebeurt wanneer artikelen worden geblokkeerd.  

|Optie|Omschrijving|  
|--------------------|------------|  
|**Verkoop geblokkeerd**|U kunt het artikel niet invoeren in een verkoopdocument of een verkoopartikeldagboek.|  
|**Inkoop geblokkeerd**|U kunt het artikel niet invoeren in een inkoopdocument, in een inkoopartikeldagboek of in planningsprocessen voor inkoop.|  
|**Geblokkeerd**|U kunt het artikel niet voor een artikeltransactie gebruiken.|  

> [!NOTE]
> Geblokkeerde artikelen kunnen worden geretourneerd. Dit betekent dat geen van de bovenstaande instellingen van toepassing zijn als het artikel wordt gebruikt in retourorders en creditnota's.

Wanneer u de functie **Kopiëren uit document** gebruikt om nieuwe documenten te maken op basis van bestaande documenten, ontvangt u een bericht als er items op de brondocumentregels zijn geblokkeerd. De geblokkeerde documentregels worden uitgesloten van het nieuwe document en een bericht toont een overzicht van alle documentregels die in het brondocument zijn geblokkeerd.

## <a name="to-block-an-item-from-being-entered-on-sales-lines"></a>Voorkomen dat een artikel wordt ingevoerd op verkoopregels  
1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies de gerelateerde koppeling.  
2.  Selecteer het artikel dat u wilt blokkeren en schakel vervolgens het selectievakje **Verkoop geblokkeerd** in.  

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>Voorkomen dat een artikel wordt ingevoerd op inkoopregels  
1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies de gerelateerde koppeling.  
2.  Selecteer het artikel dat u wilt blokkeren en schakel vervolgens het selectievakje **Inkoop geblokkeerd** in.  

## <a name="to-block-an-item-from-being-posted"></a>Voorkomen dat een artikel wordt geboekt
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies de gerelateerde koppeling.
2. Selecteer het artikel dat u wilt blokkeren en schakel vervolgens het selectievakje **Geblokkeerd** in.

## <a name="see-also"></a>Zie ook  
[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Voorraad](inventory-manage-inventory.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]