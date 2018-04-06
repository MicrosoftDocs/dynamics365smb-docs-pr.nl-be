---
title: De QuickBooks-extensie Migratie gebruiken | Microsoft Docs
description: Beschrijft hoe u de extensie gebruikt om klanten, leveranciers, artikelen en rekeningen van QuickBooks Desktop naar Business Central te importeren.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: e53db4c1eef2a2f158f289e9f89ad291436a9b1a
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="the-quickbooks-data-migration-extension-for-business-central"></a>De extensie QuickBooks-gegevensmigratie voor Business Central
Met deze extensie kunt u gemakkelijk klanten, leveranciers, artikelen en accounts vanuit QuickBooks naar [!INCLUDE[d365fin](includes/d365fin_md.md)] migreren. Als uw bedrijf momenteel QuickBooks gebruikt, kunt u de relevante gegevens exporteren en vervolgens een begeleide instelling openen om de gegevens naar [!INCLUDE[d365fin](includes/d365fin_md.md)] te uploaden.  
Zie [Gegevens importeren uit andere financiële systemen](upload-data.md) voor meer informatie.

## <a name="exporting-data-from-quickbooks-desktop"></a>Gegevens vanuit QuickBooks Desktop exporteren
U moet een gedeelte van of al uw bestaande klanten, leveranciers, voorraadartikelen en accounts exporteren naar een IIF-bestand (Intuit Interchange Format). De extensie QuickBooks Data Migration bevat een standaardtoewijzing van QuickBooks-gegevens zodat u uw bestaande gegevens kunt gebruiken om uw nieuwe [!INCLUDE[d365fin](includes/d365fin_md.md)]-bedrijf te testen. De standaardtoewijzing is in de meeste gevallen voldoende, maar u kunt de toewijzing in de handleiding voor begeleide instelling wijzigen.  
In QuickBooks bevat het menu Bestand een hulpprogramma om lijsten te exporteren. Voor de doelen in [!INCLUDE[d365fin](includes/d365fin_md.md)] kunt u de volgende lijsten exporteren:

* Klantenoverzicht  
* Leveranciersoverzicht  
* Artikeloverzicht  
* Rekeningoverzicht  

De geëxporteerde gegevens worden opgeslagen als een IIF-bestand dat u vervolgens kunt uploaden naar [!INCLUDE[d365fin](includes/d365fin_md.md)].

## <a name="finding-the-quickbooks-data-migration-extension"></a>De extensie QuickBooks-gegevensmigratie vinden
De extensie QuickBooks-gegevensmigratie is geïnstalleerd en kan worden gebruikt als geïntegreerd onderdeel van de begeleide instelling Gegevensmigratie. Als u klaar bent om aan de slag te gaan en u uw gegevens hebt geëxporteerd vanuit QuickBooks, klikt u op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voert u **Begeleide instelling** in en klikt u op de gerelateerde koppeling. Kies **Bedrijfsgegevens migreren** en voer de stappen in de handleiding uit.  

## <a name="see-also"></a>Zie ook
[Bedrijfsgegevens importeren uit andere financiële systemen](upload-data.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies](ui-extensions.md)  

