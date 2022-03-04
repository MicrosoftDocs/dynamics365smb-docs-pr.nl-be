---
title: Artikelen blokkeren vanuit Verkoop of Inkoop
description: U kunt voorkomen dat artikelen worden ingevoerd op regels in verkoop- of inkoopdocumenten en u kunt voorkomen dat ze worden geboekt in een transactie.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 10f915a264508a105d449b3057c8c713d1eb25a5
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8130500"
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
1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.  
2.  Selecteer het artikel dat u wilt blokkeren en schakel vervolgens het selectievakje **Verkoop geblokkeerd** in.  

## <a name="to-block-an-item-from-being-entered-on-purchase-lines"></a>Voorkomen dat een artikel wordt ingevoerd op inkoopregels  
1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.  
2.  Selecteer het artikel dat u wilt blokkeren en schakel vervolgens het selectievakje **Inkoop geblokkeerd** in.  

## <a name="to-block-an-item-from-being-posted"></a>Voorkomen dat een artikel wordt geboekt
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer het artikel dat u wilt blokkeren en schakel vervolgens het selectievakje **Geblokkeerd** in.

## <a name="see-also"></a>Zie ook  
[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Voorraad](inventory-manage-inventory.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]