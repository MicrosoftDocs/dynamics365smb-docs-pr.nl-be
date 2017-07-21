---
title: Sales tax in Canada | Microsoft Docs
description: Leren over lokale sales tax en Goods and Services Tax in Canada.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: sales tax, local
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 571b11f4f18ffd194bdfe1d1d412bca87df4b868
ms.contentlocale: nl-be
ms.lasthandoff: 07/07/2017


---
# <a name="reporting-sales-tax-and-goodsservices-tax-in-canada"></a>Sales tax en Goods and Services Tax in Canada aangeven
In Canada, wanneer een leverancier geen zakelijke aanwezigheid in de provincie heeft waarin inkopen worden gedaan, brengt de leverancier alleen de Goods and Services Tax (GST) of Harmonized Sales Tax (HST) in rekening. Als de provincie echter een Provincial Sales Tax (PST) heeft, moet de inkoper toch de PST berekenen en deze direct aan de provincie betalen. Wanneer een Provincial Tax Area Code wordt geselecteerd, gebruikt [!INCLUDE[d365fin](includes/d365fin_md.md)] deze om de PST te berekenen en te boeken, zodat er een belastingschuld is in zowel het grootboek als de belastingpostrecords. De hier geselecteerde tax area code moet er daarom een zijn waarin alleen de PST is opgenomen, niet de GST.  

Zie voor meer informatie over sales tax [Sales tax en belastinggroepen in de VS en Canada](us-finance-sales-tax.md).  

## <a name="submitting-the-gsthst-file"></a>Het GST/HST-bestand verzenden
De belastinggegevens in inkoopdocumenten worden gebruikt om een online GST/HST-bestandsoverdracht te genereren dat u moet verschaffen aan de belastingdienst. Dit bestand bevat Goods and Services Tax (GST) en Harmonized Sales TAX (HST). Het bestand wordt gemaakt in een .tax-bestandsindeling, dat online kan worden verzonden.  

## <a name="see-also"></a>Zie ook
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Sales tax en belastinggroepen in de VS en Canada](us-finance-sales-tax.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

