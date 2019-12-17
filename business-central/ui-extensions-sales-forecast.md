---
title: De extensie Verkoop- en voorraadprognose gebruiken om voorraad te beheren | Microsoft Docs
description: Deze extensie helpt verkopen voorspellen om een duidelijk overzicht te krijgen van verwachte nulvoorraden en helpt u zelfs aanvullingsorders voor leveranciers te maken.
services: project-madeira
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, budget
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: 0b1353631aa9e727c25fd6e47dcb7f5699f3e9e1
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2877099"
---
# <a name="the-sales-and-inventory-forecast-extension"></a>De extensie Verkoop- en voorraadprognose
Voorraadbeheer is een wisselwerking tussen klantenservice en het beheren van uw kosten. Enerzijds is voor weinig voorraad minder werkkapitaal nodig, maar anderzijds leiden nulvoorraden mogelijk tot gemiste verkopen. De extensie Verkoop- en voorraadprognose voorspelt potentiële verkopen aan de hand van historische gegevens en biedt een helder overzicht van verwachte nulvoorraden. Op basis van de prognose helpt de extensie aanvullingsaanvragen aan leveranciers te maken en bespaart u tijd.  

## <a name="setting-up-forecasting"></a>Prognoses instellen
De verbinding met [Azure AI](https://azure.microsoft.com/overview/ai-platform/) is al voor u ingesteld in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Maar u kunt de prognose configureren voor gebruik van een ander soort rapportageperiode. Zo kunt u overschakelen van prognose per maand naar prognose per kwartaal. U kunt ook het aantal perioden kiezen op basis waarvan de prognose moet worden berekend, afhankelijk van hoe specifiek u de prognose wilt. We stellen voor dat u een prognose maakt per maand en met een horizon van 12 maanden voor de prognose.  

## <a name="using-the-forecasts"></a>De prognoses gebruiken
De extensie gebruikt Azure AI om toekomstige verkoop op basis van uw verkoophistorie te voorspellen om u te helpen voorraadtekort te voorkomen. Wanneer u bijvoorbeeld een artikel op de pagina **Artikelen** kiest, wordt in het diagram in het deelvenster **Artikelprognose** de geschatte verkoop van dit artikel in de komende periode getoond. Op deze manier kunt u zien of uw voorraad van het artikel waarschijnlijk binnenkort op raakt.  

U kunt de extensie ook gebruiken om voorstellen te doen met betrekking tot bevoorrading. Als u bijvoorbeeld een inkooporder maakt voor Fabrikam omdat u de nieuwe bureaustoel wilt kopen, doet de extensie Verkoop- en voorraadprognose het voorstel om ook de LONDON-draaistoel te herbevoorraden die u gewoonlijk van deze leverancier koopt. Dit komt omdat de extensie voorspelt dat uw voorraad van de LONDON-draaistoel in de komende twee maanden op raakt. U kunt dus eventueel nu al meer stoelen bestellen.  

## <a name="see-also"></a>Zie ook
[Verkoop](sales-manage-sales.md)  
[Voorraad](inventory-manage-inventory.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met behulp van extensies](ui-extensions.md)  
