---
title: Dimensies| Microsoft Docs
description: Dimensies gebruiken om gegevens te analyseren.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 03/24/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 7552ee2b3398c203a7f3295f3203c83914fbb15f
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="dimensions"></a>Dimensies
Als u analyse in documenten zoals verkooporders eenvoudiger wilt maken, kunt u dimensies gebruiken. Dimensies zijn kenmerken en waarden waarmee posten worden gecategoriseerd, zodat u ze kunt bijhouden en analyseren. Dimensies kunnen bijvoorbeeld aangeven tot welk project of welke afdeling een post behoort.  

U kunt dimensies bijvoorbeeld gebruiken in plaats van aparte grootboekrekeningen voor elke afdeling en elk project in te stellen. Hiermee krijgt u uitgebreide mogelijkheden voor analyse zonder een ingewikkeld rekeningschema te maken.  

Een ander voorbeeld is een dimensie in te stellen met de naam *Afdeling* en deze dimensie te gebruiken wanneer u verkoopdocumenten boekt. Zo kunt u met BI-programma´s bekijken welke afdeling welke artikelen heeft verkocht.
Hoe meer dimensies u gebruikt, hoe gedetailleerder de rapporten waarop u uw bedrijfsbeslissingen kunt baseren. Eén verkooppost kan bijvoorbeeld meerdere dimensiegegevens bevatten, zoals:  

* De rekening waarnaar de artikelverkoop is geboekt  
* Waar het artikel is verkocht
* Wie het heeft verkocht
* Het soort klant die het artikel heeft gekocht  

U kunt zoveel dimensies met zoveel waarden als u wilt maken.  

**Opmerking**: voor deze functionaliteit is vereist dat uw ervaring is ingesteld op **Pakket**. Zie [Uw ervaring in [!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen](ui-experiences.md) voor meer informatie.

## <a name="using-dimensions"></a>Dimensies gebruiken
In een document zoals een verkooporder kunt u dimensiegegevens toevoegen voor een afzonderlijke documentregel en voor het document zelf. In het venster **Verkooporder** kunt u bijvoorbeeld dimensiewaarden invoeren voor de eerste twee shortcutdimensies op de afzonderlijke verkoopregels, en u kunt meer dimensiegegevens toevoegen als u de knop **Dimensies** kiest.  

Als u in plaats daarvan in een dagboek werkt, kunt u ook op dezelfde manier dimensiegegevens toevoegen aan een post als u shortcutdimensies direct als velden hebt ingesteld op dagboekregels.  

U kunt standaarddimensies instellen voor rekeningen of rekeningsoorten, zodat dimensies en dimensiewaarden automatisch worden ingevuld.  

## <a name="dimension-sets"></a>Dimensiesets
Een dimensieset is een unieke combinatie dimensiewaarden. Een dimensieset wordt als dimensiesetposten in de database opgeslagen. Elke dimensiesetpost vertegenwoordigt één dimensiewaarde. De dimensiesetpost wordt geïdentificeerd door een gemeenschappelijke dimensieset-id die is toegewezen aan elke dimensiesetpost die tot de dimensieset behoort.  

Wanneer u een dagboekregel, documentkop of documentregel maakt, kunt u een combinatie van dimensiewaarden opgeven. In plaats van elke dimensiewaarde expliciet in de database op te slaan, wordt een dimensieset-id toegewezen aan de dagboekregel, documentkop of documentregel om zo de dimensieset op te geven.  

## <a name="see-also"></a>Zie ook
[Financiën](finance.md)  
[Dimensies instellen](finance-setup-dimensions.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

