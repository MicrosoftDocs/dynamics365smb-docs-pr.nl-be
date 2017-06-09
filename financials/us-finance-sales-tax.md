---
title: Sales tax en belastinggroepen in de VS en Canada | Microsoft Docs
description: Leer meer over hoe u btw instelt en hoe belastinggroepen, belastinggebieden, belastingjurisdicties en belastingdetails werken.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: local
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ff1981a428a2cd3b3864b7f0cc795a1abeab7a10
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="sales-tax-and-tax-groups-in-the-us-and-canada"></a>Sales tax en belastinggroepen in de VS en Canada
Wanneer u voor het eerst gaat werken met [!INCLUDE[d365fin](includes/d365fin_md.md)], kunt u een begeleide instelling uitvoeren om snel en gemakkelijk btw-gegevens voor uw bedrijf, klanten en leveranciers in te stellen. In enkele minuten bent u gereed om verkoopdocumenten en inkoopdocumenten te maken waarvoor de btw correct is berekend. Dit wordt uitgelegd [in onze blogpost](https://madeira.microsoft.com/blog/sales-tax-setup-made-easy).
Als u naar het lege Mijn bedrijf gaat, is het raadzaam dat u elke handleiding voor begeleide instelling gaat gebruiken, inclusief de handleiding voor btw. Als u btw liever zelf instelt, wordt in dit artikel uitgelegd waarmee u rekening moet houden.  

## <a name="tax-groups-tax-areas-and-tax-jurisdictions"></a>Belastinggroepen, belastinggebieden en belastingjurisdicties
In [!INCLUDE[d365fin](includes/d365fin_md.md)] vertegenwoordigt een tax group een groep voorraadartikelen of resources die onder dezelfde belastingvoorwaarden vallen. U kunt bijvoorbeeld een belastinggroep instellen voor belastbare artikelen en een andere belastinggroep voor niet-belastbare artikelen. U moet belastinggroepscodes toewijzen aan voorraadartikelen en grootboekrekeningen. Op dezelfde manier moet u belastinggebiedcodes toewijzen aan klanten, locaties en aan uw eigen bedrijfsinstellingen. De handleiding voor begeleide instelling helpt u hierbij.  

Elk belastinggebied is een groepering van btw-jurisdicties die zijn gebaseerd op een bepaalde geografische locatie. Het belastinggebied Miami, Florida, bevat bijvoorbeeld drie btw-jurisdicties: plaats (Miami) county (Dade) en provincie (Florida). [!INCLUDE[d365fin](includes/d365fin_md.md)] bevat een beperkte set belastinggebieden met een standaardconfiguratie, maar u kunt deze wijzigen en nieuwe belastinggebieden toevoegen.  

Als u de tax area's en belastingjurisdicties instelt, moet u ervoor zorgen dat u de velden correct invult. In de Verenigde Staten kunnen staten, county's, steden en districten btw heffen. In Canada kan de federale overheid en de provincies btw heffen. Bedrijven innen btw en dragen deze af aan overheidsinstanties voor producten die zijn verkocht aan eindgebruikers. Btw kan ook worden berekend over bestaande btw. Belasting kan bijvoorbeeld worden berekend over een verkoopfactuurbedrag dat reeds de belasting van andere jurisdicties bevat.  

In Canada moeten belastingbedragen gedetailleerd worden beschreven in documenten voor elke belastingjurisdictie. Maximaal vier jurisdicties kunnen worden weergegeven in een document en jurisdicties met dezelfde afdrukvolgorde worden gecombineerd wanneer ze worden afgedrukt.  

## <a name="tax-details"></a>Belastingdetails
In het venster **Belastingdetails** worden verschillende combinaties weergegeven van btw-jurisdicties en btw-groepen om btw-tarieven in te stellen. Voor elke belastingjurisdictie is het raadzaam dat u één belastinggroep instelt voor normale btw, een andere belastinggroep voor artikelen of services die niet worden belast en een extra belastinggroep voor elk type artikel of service met een ander btw-tarief in die jurisdictie.  

Wanneer u in de Verenigde Staten verkoopt aan een klant op een locatie waar u geen *situs* hebt, of een juridische locatie in die provincie, int u geen btw. Voor locaties waarin u geen situs hebt, moet u ervoor zorgen dat de beiden velden **Belasting onder minimum** en **Belasting boven maximum** 0,00 zijn.  

## <a name="see-also"></a>Zie ook
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Sales tax en Goods and Services Tax in Canada](ca-finance-tax.md)  
[Btw-instellingen gemakkelijk gemaakt](https://madeira.microsoft.com/blog/sales-tax-setup-made-easy)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

