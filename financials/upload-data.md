---
title: Uw oude bedrijfsgegevens in Financials importeren | Microsoft Docs
description: Hierin wordt beschreven hoe u uw eigen gegevens kunt importeren in Dynamics 365 for Financials.
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: migrate, initialize, implement
ms.date: 04/27/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 001dccf7935f38dd2f409e4fea31598a279472d4
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="importing-business-data-from-other-finance-systems"></a>Bedrijfsgegevens importeren uit andere financiële systemen
Wanneer u zich registreert voor [!INCLUDE[d365fin](includes/d365fin_md.md)], kunt u ervoor kiezen een leeg bedrijf te maken zodat u uw eigen gegevens kunt uploaden en uw nieuwe [!INCLUDE[d365fin](includes/d365fin_md.md)]-bedrijf kunt testen. Afhankelijk van de financiële oplossing die uw bedrijf tegenwoordig gebruikt, kunt u gegevens over klanten, leveranciers en bankrekeningen overbrengen.  

Vanaf de startpagina kunt u een handleiding voor begeleide instelling starten die u helpt de bedrijfsgegevens vanuit een Excel-bestand of vanuit andere indelingen over te brengen. Het type van de bestanden die u kunt uploaden, is afhankelijk van de extensies die beschikbaar zijn. U kunt bijvoorbeeld gegevens van QuickBooks migreren, omdat [!INCLUDE[d365fin](includes/d365fin_md.md)] een extensie bevat die de conversie van QuickBooks-gegevens uitvoert. Als u gegevens vanuit andere financiële oplossingen wilt migreren, moet u controleren of er een extensie beschikbaar is voor die oplossing of u moet vanuit Excel importeren.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] bevat sjablonen voor rekeningen, klanten, leveranciers en voorraadartikelen die u desgewenst kunt toepassen wanneer u uw gegevens importeert.  

## <a name="importing-data-from-quickbooks-or-dynamics-gp"></a>Gegevens importeren uit QuickBooks of Dynamics GP
Als uw bedrijf momenteel QuickBooks of Dynamics GP gebruikt, kunt u de relevante gegevens naar een bestand exporteren. Vervolgens kunt u de handleiding voor begeleide instelling openen om de gegevens over te brengen.
Als uw bestand bijvoorbeeld klanten en leveranciers bevat, kunt u ervoor kiezen alleen de klantgegevens over te brengen. U kunt de rest van de gegevens later overbrengen.  

De begeleide instelling bevat een optie om de standaardconfiguratie van de overdracht te wijzigen, maar het is raadzaam deze geavanceerde instelling alleen in te voeren als u met databasetabellen vertrouwd bent. In de meeste bedrijven zet de standaardtoewijzing van QuickBooks of Dynamics GP aan [!INCLUDE[d365fin](includes/d365fin_md.md)] de gewenste informatie over.  

## <a name="importing-data-from-configuration-packages"></a>Gegevens importeren uit configuratiepakketten
[!INCLUDE[d365fin](includes/d365fin_md.md)] bevat een configuratiepakket dat u naar Excel kunt exporteren, waar u dan de gegevens kunt instellen. Vervolgens kunt u de gegevens weer uit Excel importeren. Het pakket bestaat uit 27 tabellen, met hoofdgegevens zoals klanten, leveranciers, artikelen en rekeningen, overige tabellen met basisinstellingen zoals verzendmethoden en transactiestabellen zoals verkoopkoptekst en regels.  

> [!NOTE]  
>  Werken met configuratiepakketten is geavanceerde functionaliteit, en het wordt aanbevolen om hiervoor contact op te nemen met uw beheerder. Zie voor meer informatie [Gegevens importeren uit oudere boekhoudsoftware door middel van een configuratiepakket](across-import-data-configuration-packages.md).  

## <a name="see-also"></a>Zie ook
[Financiën](finance.md)  
[Gegevens importeren uit oudere boekhoudsoftware door middel van een configuratiepakket](across-import-data-configuration-packages.md).  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met extensies](ui-extensions.md)   
[[!INCLUDE[d365fin](includes/d365fin_md.md)] instellen](setup.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]
