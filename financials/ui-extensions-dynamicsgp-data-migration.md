---
title: De extensie Dynamics GP Data Migration | Microsoft Docs
description: Bevat informatie over de extensie Dynamics GP Data Migration
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: a94afbd0ee689f6bd9157d0b441959f252230f08
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="the-dynamics-gp-data-migration-extension-for-dynamics-365-for-financials"></a>De extensie Dynamics GP Data Migration voor Dynamics 365 for Financials
Met deze extensie kunt u gemakkelijk klanten, leveranciers, voorraadartikelen en accounts vanuit Dynamics GP naar [!INCLUDE[d365fin](includes/d365fin_md.md)] migreren. Als uw bedrijf momenteel Dynamics GP gebruikt, kunt u de relevante masterrecords exporteren en vervolgens een handleiding voor begeleide instelling openen om de gegevens toe te voegen aan [!INCLUDE[d365fin](includes/d365fin_md.md)]. Zie [Bedrijfsgegevens migreren uit andere financiële systemen](upload-data.md) voor meer informatie.

## <a name="exporting-data-from-dynamics-gp"></a>Gegevens exporteren uit Dynamics GP
U moet gegevens van sommige of alle bestaande klanten, leveranciers, voorraadartikelen en rekeningen naar een bestand geëxporteerd hebben door middel van de Dynamics GP-functionaliteit voor gegevensexport. Voor de doelen in [!INCLUDE[d365fin](includes/d365fin_md.md)] kunt u de volgende soorten gegevens exporteren:

* Rekening  
* Klant  
* Artikel  
* Leverancier  

De extensie Dynamics GP Data Migration wijst automatisch de geëxporteerde gegevens toe, zodat de gegevens snel beschikbaar zijn in uw nieuwe [!INCLUDE[d365fin](includes/d365fin_md.md)]-bedrijf. Tijdens het proces worden ondersteunende configuratiegegevens gemaakt, zoals boekingsgroepen. Voorraadartikelen worden in het systeem ingevoerd met FIFO als methode voor kostenwaardering. Rekeningen worden ingesteld als de hoofdrekeningsegment uit Dynamics GP met dimensies, omdat [!INCLUDE[d365fin](includes/d365fin_long_md.md)] geen rekeningsegmenten kent.

## <a name="see-also"></a>Zie ook
[Bedrijfsgegevens importeren uit andere financiële systemen](upload-data.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met extensies](ui-extensions.md)  

