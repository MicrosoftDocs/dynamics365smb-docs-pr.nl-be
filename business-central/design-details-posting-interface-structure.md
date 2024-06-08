---
title: 'Ontwerpdetails: boekingsinterfacestructuur'
description: In dit onderwerp vindt u een overzicht van de algemene procedures en ontwerpdetails in de boekingsinterfacestructuur.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'posting, interface, design'
ms.date: 06/15/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="design-details-posting-interface-structure"></a>Ontwerpdetails: boekingsinterfacestructuur
In de boekingsinterfacestructuur van [!INCLUDE[prod_short](includes/prod_short.md)] zijn er verschillende algemene procedures die dezelfde structuur gebruiken:  
  
* RunWithCheck- en RunWithoutCheck-aanroepprocedurecode - algemene boekingsinterface voor dagboekregel.  
* CustPostApplyCustLedgEntry - klantvereffening boeken, aangeroepen vanaf codeunit 226 custEntry - Geboekte posten vereffenen.  
* VendPostApplyVendLedgEntry - leveranciersvereffening boeken, aangeroepen vanaf codeunit 227 VendEntry - Geboekte posten vereffenen.  
* UnapplyCustLedgEntry - ongedaan maken van klantvereffening boeken, aangeroepen vanaf codeunit 226 custEntry - Geboekte posten vereffenen  
* UnapplyVendLedgEntry - ongedaan maken van leveranciersvereffening boeken, aangeroepen vanaf codeunit 227 VendEntry - Geboekte posten vereffenen  
  
## <a name="see-also"></a>Zie ook
[Ontwerpdetails: boekingsenginestructuur](design-details-posting-engine-structure.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
