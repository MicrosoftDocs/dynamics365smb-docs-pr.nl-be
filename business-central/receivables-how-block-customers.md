---
title: Verkoop aan klanten blokkeren
description: Indien nodig kunt u voorkomen dat een klant wordt opgenomen in verkoopdocumenten en andere verkooptransacties.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 1caf2fb0586cf704e5fc1354b3b4a0be096dc709
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5781750"
---
# <a name="block-customers"></a>Klanten blokkeren
U kunt een klant blokkeren, bijvoorbeeld vanwege insolventie, zodat de klant niet aan verkoopdocumenten kan worden toegevoegd of zodat geen transacties voor de klant kunnen worden geboekt.

Naast het blokkeren van een klant kunt u een klanttransactie voor de klant op afwachten instellen in verband met aanmaningen. Zie voor meer informatie [Openstaande saldi innen](receivables-collect-outstanding-balances.md).   

De volgende tabel beschrijft de opties voor het blokkeren van klanten.  

|Optie|Omschrijving|  
|--------------------|------------|  
|**Leeg**|Transacties zijn toegestaan voor deze klant.|
|**Verzending**|Voor deze klant kunnen geen nieuwe orders en nieuwe verzendingen worden gemaakt. Bestaande verzendingen die nog niet zijn gefactureerd, kunnen worden gefactureerd.|  
|**Factureren**|Voor deze klant kunnen geen nieuwe orders, nieuwe verzendingen en nieuwe facturen worden gemaakt. Bestaande verzendingen die nog niet zijn gefactureerd, kunnen niet worden gefactureerd. U kunt nog steeds herinneringen en rentefacturen naar de klant sturen.|  
|**Alle**|Voor deze klant is geen enkele transactie, inclusief betalingen, toegestaan.|  

## <a name="to-block-a-customer"></a>Een klant blokkeren  
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies de gerelateerde koppeling.
2. Selecteer een klant en kies vervolgens de actie **Bewerken**.
3. Kies in het veld **Geblokkeerd** wat u wilt blokkeren, zoals beschreven in de bovenstaande tabel.

## <a name="see-also"></a>Zie ook  
[Nieuwe klanten registreren](sales-how-register-new-customers.md)  
[Openstaande saldi innen](receivables-collect-outstanding-balances.md)  
[Tegoeden beheren](receivables-manage-receivables.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]