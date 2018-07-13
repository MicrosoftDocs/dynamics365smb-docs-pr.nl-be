---
title: Opgeslagen instellingen wijzigen en toepassen | Microsoft Docs
description: Beschrijft het gebruik van vooraf gedefinieerde opties en filters om een lijst aan te passen en de juiste gegevens te genereren.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customization, personalization
ms.date: 09/08/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: f5225d1f6d0d4ac0020fb073d5df6da83b5c0f5b
ms.contentlocale: nl-be
ms.lasthandoff: 06/28/2018

---
# <a name="managing-saved-settings-on-reports"></a>Opgeslagen instellingen in rapporten beheren
Afhankelijk van het rapport dat wordt uitgevoerd, ziet u wellicht een pagina waarmee u bepaalde opties en filters kunt instellen om de gegevens te wijzigen die in het gegenereerde rapport worden opgenomen. Deze pagina wordt de rapportaanvraagpagina genoemd. Een rapport kan een of meer *opgeslagen instellingen* bevatten die u op het rapport kunt toepassen vanaf de aanvraagpagina. *Opgeslagen instellingen* zijn in wezen vooraf gedefinieerde opties en filters. Met behulp van opgeslagen instellingen kunt u snel en betrouwbaar rapporten genereren die de juiste gegevens bevatten.

U kunt de opgeslagen instellingen die beschikbaar voor u zijn voor een rapport, zien in het gedeelte **Opgeslagen instellingen** van de rapportaanvraagpagina.  

## <a name="apply-saved-settings-to-a-report"></a>Opgeslagen instellingen toepassen op een rapport
1. Open het rapport.

   Het rapportaanvraagvenster verschijnt.    
2. Stel in het gedeelte **Opgeslagen instellingen** van de pagina het veld **Naam** in op de opgeslagen instellingen die u wilt gebruiken.

   De sectie **Opgeslagen instellingen** wordt alleen weergegeven als het rapport eerder is uitgevoerd of als er bestaande, opgeslagen instellingen zijn. De opgeslagen instelling met de naam **Laatst gebruikte opties en filters** is altijd beschikbaar. Deze instellingen zijn de optie- en filterwaarden die de laatste keer dat u het rapport uitvoerde, zijn gebruikt.

## <a name="create-and-modify-saved-settings-for-all-users"></a>Opgeslagen instellingen maken en wijzigen voor alle gebruikers
Als u de juiste machtigingen hebt, kunt u de opgeslagen instellingen voor alle gebruikers in een bedrijf weergeven, maken en wijzigen. U kunt opgeslagen instellingen voor een rapport toewijzen aan afzonderlijke gebruikers of aan alle gebruikers in het bedrijf.

U beheert opgeslagen instellingen vanaf pagina 1506 **Rapportinstellingen**. Als u deze pagina wilt openen, kiest u het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voert u **Rapportinstellingen** in en kiest u vervolgens de gerelateerde koppeling.

Vanaf de pagina **Rapportinstellingen** kunt u nieuwe instellingen maken of kunt u een kopie maken en bestaande instellingen wijzigen. Om de opties en filters voor een instelling te wijzigen, kiest u de actie **Bewerken**.

> [!NOTE]
> De functie voor opgeslagen instellingen voor rapporten is alleen relevant wanneer de eigenschap SaveValues van de aanvraagpagina is ingesteld op Ja. De eigenschap SaveValues wordt ingesteld in de ontwikkelomgeving.  

> [!Important]
> Als u een opgeslagen instelling voor alle gebruikers maakt en deze dezelfde naam heeft als een bestaande, opgeslagen instelling voor een specifieke gebruiker, kan die gebruiker de opgeslagen instellingen die aan iedereen zijn toegewezen, niet gebruiken.  In het veld Opgeslagen instellingen op de rapportaanvraagpagina ziet de gebruiker de twee opgeslagen instellingsopties met dezelfde naam. Ongeacht welke optie de gebruiker echter kiest, de gebruikersspecifieke opgeslagen instelling wordt gebruikt.

## <a name="see-also"></a>Zie ook
[Werken met rapporten](ui-work-report.md)  

