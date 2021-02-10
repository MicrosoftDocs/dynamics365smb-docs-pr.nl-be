---
title: Artikelen of services inkopen voor een project en voorzieningen beheren| Microsoft Docs
description: Beschrijft hoe u de voorraad en aankoop van materiaal en services voor projecten beheert.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, material, purchase
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 7b3abf9ae0cb07e6b3e79fc21ee10467f4f611b6
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4748955"
---
# <a name="manage-job-supplies"></a>Projectvoorraden beheren
Het beheren van projectgoederen van artikelen, services en onkosten is een integraal en zeer belangrijk aspect van de uitvoering van alle projecten. U kunt voorraadhoeveelheden gebruiken of projectspecifieke inkopen doen met behulp van inkooporders of inkoopfacturen. Stel bijvoorbeeld dat bij een serviceproject voor een computer een nieuwe schijf vereist is. U maakt een inkoopfactuur om een nieuwe schijf te kopen en legt het project vast waarvoor deze wordt gebruikt.

Als voor het inkoopproces de fysieke transactie niet apart hoeft te worden vastgelegd, kan een aankoop worden verwerkt op de pagina **GB-dagboek project**. Zie voor meer informatie [Gebruik vastleggen voor projecten](projects-how-record-job-usage.md).

## <a name="to-purchase-items-or-services-for-a-job"></a>Artikelen of services inkopen voor een project
In de volgende procedure wordt beschreven hoe u een inkoopfactuur gebruikt om producten voor een project te kopen. Dezelfde stappen gelden bij gebruik van een inkooporder.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopfacturen** in en kies de gerelateerde koppeling.  
2. Kies de actie **Nieuw** en vul indien nodig de velden in. Zie voor meer informatie [Inkopen vastleggen](purchasing-how-record-purchases.md).
3. Selecteer in de velden **Projectnr.** en **Projecttaaknr.** de gegevens van het project waarvoor u artikelen of services wilt inkopen. Gebruik de personalisatietools als een veld niet zichtbaar is. Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.

    De waarde die u selecteert in het veld **Projectregelsoort** definieert of een planningsregel wordt gemaakt wanneer u het gebruik van het artikel boekt. Als het veld **Factureerbaar** bevat, worden projectplanningsregels gemaakt die gereed zijn om te worden gefactureerd aan de klant. Zie [Projecten factureren](projects-how-invoice-jobs.md) voor meer informatie.
4. Kies de actie **Boeken**.

## <a name="to-view-the-value-of-purchases-for-a-job"></a>De waarde van aankopen voor een project weergeven
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Projecten** in en kies de desbetreffende koppeling.
2. Open de betreffende projectkaart.

    In het sneltabblad **Taken** bevat het veld **Openstaande orders** het totale uitstaande bedrag in de lokale valuta van voorraadartikelen en -services op inkoopdocumenten voor de projecttaakregel.  

    Het veld **Ontv./Niet gefact. bedrag** bevat de waarde van artikelen die worden geleverd op inkoopdocumenten, maar die nog niet zijn gefactureerd.  
3. Kies een van de velden om de pagina **Inkoopregels** te openen. Op deze pagina kunt u informatie bekijken over de gerelateerde inkoopdocumentregels, inclusief welke artikelen of services zijn ontvangen.

## <a name="to-post-a-job-related-expense"></a>Projectkosten boeken
Als u buitengewone of eenmalige projectkosten maakt, kunt u de pagina **GB-dagboek project** gebruiken om ze direct te boeken naar de relevante projectrekening.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **GB-dagboeken voor project** in en kies de gerelateerde koppeling.  
2. Maak een nieuwe regel en voer gegevens voor de kosten in, zoals in de velden **Projectnr.** en **Projecttaaknr**.  
3. Wanneer het dagboek compleet is, kiest u de actie **Boeken**.

## <a name="see-also"></a>Zie ook
[Projectbeheer](projects-manage-projects.md)  
[Financiën](finance.md)  
[Inkoop](purchasing-manage-purchasing.md)         
[Verkoop](sales-manage-sales.md)      
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
