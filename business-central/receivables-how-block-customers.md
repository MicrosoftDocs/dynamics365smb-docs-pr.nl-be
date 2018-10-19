---
title: Verkopen aan klanten blokkeren en artikelen blokkeren voor verkoop of inkoop
description: In Business Central kan een artikel worden gemarkeerd als geblokkeerd voor verkoop, geblokkeerd voor inkoop of geblokkeerd voor alle doeleinden.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: 268d098318b77cb89a369e8edc14729a44bedae6
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

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
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer een klant en kies vervolgens de actie **Bewerken**.
3. Vul het veld **Geblokkeerd** in met een van de hierboven beschreven opties.

## <a name="see-also"></a>Zie ook  
[Nieuwe klanten registreren](sales-how-register-new-customers.md)  
[Openstaande saldi innen](receivables-collect-outstanding-balances.md)  
[Tegoeden beheren](receivables-manage-receivables.md)  

