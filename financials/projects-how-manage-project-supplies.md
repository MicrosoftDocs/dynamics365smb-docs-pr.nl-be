---
title: Artikelen of services inkopen voor een project en voorzieningen beheren| Microsoft Docs
description: Beschrijft hoe u de voorraad en aankoop van materiaal en services voor projecten beheert.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: project management, material, purchase
ms.date: 06/06/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 46cae53022ba5d65a370694c9818f52a7bf45525
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-manage-job-supplies"></a>Procedure: Projectvoorraden beheren
Het beheren van projectgoederen van artikelen, services en onkosten is een integraal en zeer belangrijk aspect van de uitvoering van alle projecten. U kunt voorraadhoeveelheden gebruiken of projectspecifieke inkopen doen met behulp van inkooporders of inkoopfacturen. Stel bijvoorbeeld dat bij een serviceproject voor een computer een nieuwe schijf vereist is. U maakt een inkoopfactuur om een nieuwe schijf te kopen en legt het project vast waarvoor deze wordt gebruikt.

Als voor het inkoopproces de fysieke transactie niet apart hoeft te worden vastgelegd, kan een aankoop worden verwerkt in het venster **GB-dagboek project**. Zie voor meer informatie [Procedure: Gebruik vastleggen voor projecten](projects-how-record-job-usage.md).

## <a name="to-purchase-items-or-services-for-a-job"></a>Artikelen of services inkopen voor een project
In de volgende procedure wordt beschreven hoe u een inkoopfactuur gebruikt om producten voor een project te kopen. Dezelfde stappen gelden bij gebruik van een inkooporder.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Inkoopfacturen** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies de actie **Nieuw** en vul indien nodig de velden in. Zie voor meer informatie [Procedure: Inkopen vastleggen](purchasing-how-record-purchases.md).
3. Selecteer in de velden **Projectnr.** en **Projecttaaknr.** de gegevens van het project waarvoor u artikelen of services wilt inkopen. Gebruik de functie **Kolommen kiezen** als het veld niet zichtbaar is. Zie [Persoonlijke gebruikersinstellingen](ui-user-personalization.md) voor meer informatie.

    De waarde die u selecteert in het veld **Projectregelsoort** definieert of een planningsregel wordt gemaakt wanneer u het gebruik van het artikel boekt. Als het veld **Factureerbaar** bevat, worden projectplanningsregels gemaakt die gereed zijn om te worden gefactureerd aan de klant. Zie [Procedure: Projecten factureren](projects-how-invoice-jobs.md) voor meer informatie.
4. Kies de actie **Boeken**.

## <a name="to-view-the-value-of-purchases-for-a-job"></a>De waarde van aankopen voor een project weergeven
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Projecten** in en klik vervolgens op de gerelateerde koppeling.
2. Open de betreffende projectkaart.

    In het sneltabblad **Taken** bevat het veld **Openstaande orders** het totale uitstaande bedrag in de lokale valuta van voorraadartikelen en -services op inkoopdocumenten voor de projecttaakregel.  

    Het veld **Ontv./Niet gefact. bedrag** bevat de waarde van artikelen die worden geleverd op inkoopdocumenten, maar die nog niet zijn gefactureerd.  
3. Kies een van de velden om het venster **Inkoopregels** te openen. In dit venster kunt u informatie bekijken over de gerelateerde inkoopdocumentregels, inclusief welke artikelen of services zijn ontvangen.

## <a name="to-post-a-job-related-expense"></a>Projectkosten boeken
Als u buitengewone of eenmalige projectkosten maakt, kunt u het venster **GB-dagboek project** gebruiken om ze direct te boeken naar de relevante projectrekening.

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **GB-dagboeken voor project** in en klik vervolgens op de gerelateerde koppeling.  
2. Maak een nieuwe regel en voer gegevens voor de kosten in, zoals in de velden **Projectnr.** en **Projecttaaknr**.  
3. Wanneer het dagboek compleet is, kiest u de actie **Boeken**.

## <a name="see-also"></a>Zie ook
[Projectbeheer](projects-manage-projects.md)  
[Financiën](finance.md)  
[Inkoop](purchasing-manage-purchasing.md)         
[Verkoop](sales-manage-sales.md)      
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

