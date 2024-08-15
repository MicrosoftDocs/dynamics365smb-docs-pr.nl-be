---
title: Hoe u de verkoop aan klanten kunt blokkeren
description: Indien nodig kunt u voorkomen dat een klant wordt opgenomen in verkoopdocumenten en andere verkooptransacties.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 07/05/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="block-customers"></a>Klanten blokkeren
U kunt een klant blokkeren, bijvoorbeeld vanwege insolventie, zodat de klant niet aan verkoopdocumenten kan worden toegevoegd of zodat er geen transacties voor de klant kunnen worden geboekt.

Naast het blokkeren van een klant kunt u een klanttransactie voor de klant op afwachten instellen in verband met aanmaningen. Zie voor meer informatie [Openstaande saldi innen](receivables-collect-outstanding-balances.md).   

De volgende tabel beschrijft de opties voor het blokkeren van klanten.  

|Optie|Beschrijving|  
|--------------------|------------|  
|**Leeg**|Transacties zijn toegestaan voor deze klant.|
|**Verzending**|Er kunnen geen nieuwe bestellingen en nieuwe leveringen voor deze klant worden aangemaakt. Bestaande verzendingen die nog niet zijn gefactureerd, kunnen worden gefactureerd.|  
|**Factuur**|Er kunnen geen nieuwe bestellingen, nieuwe leveringen en nieuwe facturen voor deze klant worden aangemaakt. Bestaande zendingen die nog niet gefactureerd zijn, kunnen niet gefactureerd worden. U kunt nog steeds herinneringen en rentefacturen naar de klant sturen.|  
|**Alle**|Voor deze klant is geen enkele transactie, inclusief betalingen, toegestaan.|  

## <a name="to-block-a-customer"></a>Een klant blokkeren
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Klanten** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer een klant en kies vervolgens de actie **Bewerken**.
3. Kies in het veld **Geblokkeerd** wat u wilt blokkeren, zoals beschreven in de bovenstaande tabel.

## <a name="see-also"></a>Zie ook
[Nieuwe klanten registreren](sales-how-register-new-customers.md)  
[Openstaande saldi innen](receivables-collect-outstanding-balances.md)  
[Tegoeden beheren](receivables-manage-receivables.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
