---
title: Verkopen aan klanten blokkeren en artikelen blokkeren voor verkoop of inkoop
description: In Business Central kan een artikel worden gemarkeerd als geblokkeerd voor verkoop, geblokkeerd voor inkoop of geblokkeerd voor alle doeleinden.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: c1b055e5101b99f0b0e1b69169d5c9f2f7e21d09
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2883006"
---
# <a name="block-customers"></a>Klanten blokkeren
U kunt een klant blokkeren, bijvoorbeeld vanwege insolventie, zodat de klant niet aan verkoopdocumenten kan worden toegevoegd of zodat geen transacties voor de klant kunnen worden geboekt.

Naast het blokkeren van een klant kunt u een klanttransactie voor de klant op afwachten instellen in verband met aanmaningen. Zie voor meer informatie [Openstaande saldi innen](receivables-collect-outstanding-balances.md).   

De volgende tabel beschrijft de verschillende blokkeeropties.  

|Optie|Description|  
|--------------------|------------|  
|**Leeg**|Transacties zijn toegestaan voor deze klant.|
|**Verzending**|Voor deze klant kunnen geen nieuwe orders en nieuwe verzendingen worden gemaakt. Bestaande verzendingen die nog niet zijn gefactureerd, kunnen worden gefactureerd.|  
|**Factureren**|Voor deze klant kunnen geen nieuwe orders, nieuwe verzendingen en nieuwe facturen worden gemaakt. Bestaande verzendingen die nog niet zijn gefactureerd, kunnen niet worden gefactureerd.|  
|**Alle**|Voor deze klant is geen enkele transactie, inclusief betalingen, toegestaan.|  

## <a name="to-block-a-customer"></a>Een klant blokkeren  
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies de gerelateerde koppeling.
2. Selecteer een klant en kies vervolgens de actie **Bewerken**.
3. Vul het veld **Geblokkeerd** in met een van de hierboven beschreven opties.

## <a name="see-also"></a>Zie ook  
[Nieuwe klanten registreren](sales-how-register-new-customers.md)  
[Openstaande saldi innen](receivables-collect-outstanding-balances.md)  
[Tegoeden beheren](receivables-manage-receivables.md)  
