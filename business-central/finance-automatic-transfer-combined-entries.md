---
title: Automatische overdracht en gecombineerde posten | Microsoft Docs
description: In kostprijsboekhouding kunt u grootboekposten overbrengen naar een kostensoort door middel van een gecombineerde boeking. U kunt opgeven of een kostensoort gecombineerde posten ontvangt in het veld **Posten combineren** in de definitie van het kostensoort. De volgende tabel beschrijft de verschillende opties.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
redirect_url: finance-transfer-and-post-cost-entries
ms.openlocfilehash: 8f6b5328b3a7b8cdcb4582deda363bdd0361ed9a
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239004"
---
# <a name="automatic-transfer-and-combined-entries"></a>Automatische overdracht en gecombineerde posten
In kostprijsboekhouding kunt u grootboekposten overbrengen naar een kostensoort door middel van een gecombineerde boeking. U kunt opgeven of een kostensoort gecombineerde posten ontvangt in het veld **Posten combineren** in de definitie van het kostensoort. De volgende tabel beschrijft de verschillende opties.  

|Posten combineren|Omschrijving|  
|---------------------|-----------------|  
|Geen|Elke grootboekpost wordt afzonderlijk overgebracht naar het bijbehorende kostensoort.|  
|Dag|Grootboekposten met dezelfde boekingsdatum worden als één post overgeboekt naar de bijbehorende kostensoort.|  
|Maand|Alle grootboekposten in dezelfde kalendermaand worden als één post overgeboekt naar de bijbehorende kostensoort.|  

> [!IMPORTANT]  
>  Als u het selectievakje **Automatisch overdragen van GB** op de pagina **Instelling kostprijsboekhouding** hebt ingeschakeld, wordt de kostprijsboekhouding automatisch bijgewerkt in [!INCLUDE[d365fin](includes/d365fin_md.md)] na elke boeking in het grootboek. Gecombineerde posten zijn niet mogelijk.  

## <a name="see-also"></a>Zie ook  
 [Kostenposten overbrengen en boeken](finance-transfer-and-post-cost-entries.md)   
 [Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
