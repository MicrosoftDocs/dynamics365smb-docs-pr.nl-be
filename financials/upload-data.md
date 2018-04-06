---
title: Uw oude bedrijfsgegevens importeren in Finance and Operations, Business edition | Microsoft Docs
description: U kunt gegevens voor klanten, leveranciers en voorraad importeren, bijvoorbeeld uit Excel, QuickBooks of Dynamics GP, in Finance and Operations, Business edition.
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: QuickBooks, transfer, import, migrate, initialize, implement
ms.date: 03/07/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: fe1f89ee875924370a206359a3f7238f0224ab80
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="importing-business-data-from-other-finance-systems"></a>Bedrijfsgegevens importeren uit andere financiële systemen
Wanneer u zich registreert voor [!INCLUDE[d365fin](includes/d365fin_md.md)], kunt u ervoor kiezen een leeg bedrijf te maken zodat u uw eigen gegevens kunt uploaden en uw nieuwe [!INCLUDE[d365fin](includes/d365fin_md.md)]-bedrijf kunt testen. Afhankelijk van de financiële oplossing die uw bedrijf tegenwoordig gebruikt, kunt u gegevens over klanten, leveranciers en bankrekeningen overbrengen.  

Vanuit het rolcentrum kunt u een begeleide instelling starten die u helpt de bedrijfsgegevens vanuit een Excel-bestand of vanuit andere indelingen over te brengen. Het type van de bestanden die u kunt uploaden, is afhankelijk van de extensies die beschikbaar zijn. U kunt bijvoorbeeld gegevens van QuickBooks migreren, omdat [!INCLUDE[d365fin](includes/d365fin_md.md)] een extensie bevat die de conversie van QuickBooks-gegevens uitvoert. Als u gegevens vanuit andere financiële oplossingen wilt migreren, moet u controleren of er een extensie beschikbaar is voor die oplossing of u moet vanuit Excel importeren.  

[!INCLUDE[d365fin](includes/d365fin_md.md)] bevat sjablonen voor rekeningen, klanten, leveranciers en voorraadartikelen die u desgewenst kunt toepassen wanneer u uw gegevens importeert.

> [!NOTE]  
> Voor groter implementatiewerk kunt u RapidStart Services voor [!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken. Dat is een uitgebreide werkset voor het instellen van nieuwe oplossingen op basis van de bedrijfsvereisten en instellingsgegevens van de klant. RapidStart Services bieden ook functionaliteit voor het importeren van bedrijfsgegevens. Zie voor meer informatie [Een bedrijf instellen met RapidStart Services](admin-set-up-a-company-with-rapidstart.md).  

## <a name="importing-data-from-quickbooks-desktop-quickbooks-online-or-dynamics-gp"></a>Gegevens importeren uit QuickBooks Desktop, QuickBooks Online of Dynamics GP
Als uw bedrijf momenteel QuickBooks of Dynamics GP gebruikt, kunt u de relevante gegevens naar een bestand exporteren. Vervolgens kunt u de handleiding voor begeleide instelling openen om de gegevens over te brengen.
Als uw bestand bijvoorbeeld klanten en leveranciers bevat, kunt u ervoor kiezen alleen de klantgegevens over te brengen. U kunt de rest van de gegevens later overbrengen.  

De begeleide instelling bevat een optie om de standaardconfiguratie van de overdracht te wijzigen, maar het is raadzaam deze geavanceerde instelling alleen in te voeren als u met databasetabellen vertrouwd bent. In de meeste bedrijven zet de standaardtoewijzing van QuickBooks of Dynamics GP aan [!INCLUDE[d365fin](includes/d365fin_md.md)] de gewenste informatie over.  

Zie [QuickBooks Desktop-gegevensmigratie](ui-extensions-quickbooks-data-migration.md), [QuickBooks Online-gegevensmigratie](ui-extensions-quickbooks-online-data-migration.md) of [Dynamics GP-gegevensmigratie](ui-extensions-dynamicsgp-data-migration.md).  

## <a name="importing-data-from-configuration-packages"></a>Gegevens importeren uit configuratiepakketten
[!INCLUDE[d365fin](includes/d365fin_md.md)] bevat een configuratiepakket dat u naar Excel kunt exporteren, waar u dan de gegevens kunt instellen. Vervolgens kunt u de gegevens weer uit Excel importeren. Het pakket bestaat uit 27 tabellen, met hoofdgegevens zoals klanten, leveranciers, artikelen en rekeningen, overige tabellen met basisinstellingen zoals verzendmethoden en transactiestabellen zoals verkoopkoptekst en regels.  

> [!NOTE]  
>   Werken met configuratiepakketten is geavanceerde functionaliteit, en het wordt aanbevolen om hiervoor contact op te nemen met uw beheerder. Zie voor meer informatie [Gegevens importeren uit oudere boekhoudsoftware door middel van een configuratiepakket](across-import-data-configuration-packages.md).  

## <a name="see-also"></a>Zie ook
[Financiën](finance.md)  
[Gegevens importeren uit oudere boekhoudsoftware door middel van een configuratiepakket](across-import-data-configuration-packages.md).  
[Een bedrijf met RapidStart Services instellen](admin-set-up-a-company-with-rapidstart.md)  
[QuickBooks Desktop-gegevensmigratie](ui-extensions-quickbooks-data-migration.md)  
[QuickBooks Online-gegevensmigratie](ui-extensions-quickbooks-online-data-migration.md)  
[Dynamics GP Data Migration](ui-extensions-dynamicsgp-data-migration.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies](ui-extensions.md)   
[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
## [!INCLUDE[d365fin](includes/training_link_md.md)]

