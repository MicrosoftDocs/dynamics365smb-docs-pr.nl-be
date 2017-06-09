---
title: Verkoop- en voorraadprognose | Microsoft Docs
description: Bevat informatie over de extensie Verkoop- en voorraadprognose.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, budget
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: ebaea8b98264e981f9ad2e0abda592e2e4a72427
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="sales-and-inventory-forecast-for-dynamics-365-for-financials"></a>Verkoop- en voorraadprognose voor Dynamics 365 for Financials
Voorraadbeheer is een wisselwerking tussen klantenservice en het beheren van uw kosten. Enerzijds is voor weinig voorraad minder werkkapitaal nodig, maar anderzijds leiden nulvoorraden mogelijk tot gemiste verkopen. De extensie Verkoop- en voorraadprognose voorspelt potentiële verkopen aan de hand van historische gegevens en biedt een helder overzicht van verwachte nulvoorraden. Op basis van de prognose helpt de extensie aanvullingsaanvragen aan leveranciers te maken en bespaart u tijd.  

## <a name="setting-up-forecasting"></a>Prognose instellen
In [!INCLUDE[d365fin](includes/d365fin_md.md)] is de verbinding met [Cortana Intelligence](https://www.microsoft.com/en-us/cloud-platform/what-is-cortana-intelligence-suite) al voor u ingesteld. Maar u kunt de prognose configureren voor gebruik van een ander soort rapportageperiode. Zo kunt u overschakelen van prognose per maand naar prognose per kwartaal. U kunt ook het aantal perioden kiezen op basis waarvan de prognose moet worden berekend, afhankelijk van hoe specifiek u de prognose wilt. We stellen voor dat u een prognose maakt per maand en met een horizon van 12 maanden voor de prognose.  

## <a name="using-the-forecasts"></a>De prognoses gebruiken
De extensie gebruikt Cortana Intelligence om toekomstige verkoop op basis van uw verkoophistorie te voorspellen om u te helpen voorraadtekort te voorkomen. Wanneer u bijvoorbeeld een artikel in het venster **Artikelen** kiest, wordt in het diagram in het deelvenster **Artikelprognose** de geschatte verkoop van dit artikel in de komende periode getoond. Op deze manier kunt u zien of uw voorraad van het artikel waarschijnlijk binnenkort op raakt.  

U kunt de extensie ook gebruiken om voorstellen te doen met betrekking tot bevoorrading. Als u bijvoorbeeld een inkooporder maakt voor Fabrikam omdat u de nieuwe bureaustoel wilt kopen, doet de extensie Verkoop- en voorraadprognose het voorstel om ook de LONDON-draaistoel te herbevoorraden die u gewoonlijk van deze leverancier koopt. Dit komt omdat de extensie voorspelt dat uw voorraad van de LONDON-draaistoel in de komende twee maanden op raakt. U kunt dus eventueel nu al meer stoelen bestellen.  

## <a name="see-also"></a>Zie ook
[Verkoop](sales-manage-sales.md)  
[Voorraad](inventory-manage-inventory.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen met extensies](ui-extensions.md)  

