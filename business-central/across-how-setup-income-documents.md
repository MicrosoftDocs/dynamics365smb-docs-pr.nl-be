---
title: Inkomende documenten instellen| Microsoft Docs
description: Gebruik de functie inkomende documenten om elektronische documenten te maken, OCR-taken te beheren, facturen te importeren en afbeeldingsbestanden te converteren.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 7e99f4b33767a1bdea7b942d1b183edbacc829ac
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1241520"
---
# <a name="set-up-incoming-documents"></a>Inkomende documenten instellen
Als u dagboekregels van inkomende documentrecords maakt, moet u op de pagina **Instellingen van inkomende documenten** vastleggen welke dagboeksjabloon en batch moeten worden gebruikt.

Als u niet wilt dat gebruikers facturen of dagboekregels maken van inkomende documentrecords, tenzij de documenten zijn goedgekeurd, moet u fiatteurs instellen op de pagina **Fiatteurs inkomende documenten**.

Als u PDF- en afbeeldingsbestanden naar elektronische documenten wilt omzetten waarnaar u kunt converteren, bijvoorbeeld inkoopfacturen in [!INCLUDE[d365fin](includes/d365fin_md.md)], moet u eerst de OCR-functie instellen en de service inschakelen.

Wanneer de functie Inkomende documenten is ingesteld, kunt u verschillende functies gebruiken om onkostenbewijzen te controleren, OCR-taken te beheren en inkomende documentbestanden handmatig of automatisch te converteren naar de relevante documenten of dagboekregels. De externe bestanden kunnen worden gekoppeld in elke procesfase, inclusief naar geboekte documenten en naar de resulterende leverancier, klant en grootboekposten. Zie [Inkomende documenten verwerken](across-process-income-documents.md) voor meer informatie.

## <a name="to-set-up-the-incoming-documents-feature"></a>De functie Inkomende documenten instellen
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instellingen inkomende documenten** in en kies vervolgens de gerelateerde koppeling.
2. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a>Fiatteurs van inkomende documentrecords instellen
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instellingen inkomende documenten** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Instellingen van inkomende documenten** de actie **Fiatteurs**.

    De pagina **Fiatteurs inkomende documenten** bevat alle gebruikers die zijn ingesteld in [!INCLUDE[d365fin](includes/d365fin_md.md)].  
3. Selecteer een of meer gebruikers die een inkomend document kunnen goedkeuren voordat een verwant document of verwante dagboekregel kan worden gemaakt.

Wanneer fiatteurs zijn ingesteld op de pagina **Fiatteurs inkomende documenten**, kunnen alleen die gebruikers een inkomend document goedkeuren als het selectievakje **Goedkeuring vereist voor maken** is ingeschakeld op de pagina **Instellingen inkomende documenten**.

> [!NOTE]  
>   Deze goedkeuringsinstellingen zijn niet gerelateerd aan goedkeuringswerkstromen. Zie voor meer informatie [Goedkeuringswerkstromen gebruiken](across-how-use-approval-workflows.md).

## <a name="to-set-up-an-ocr-service"></a>Een OCR-service instellen
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instellingen van OCR-service** in en kies vervolgens de gerelateerde koppeling.
2. Vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]  
> Uw aanmeldgegevens worden automatisch versleuteld.

## <a name="see-also"></a>Zie ook
[Inkomende documenten verwerken](across-process-income-documents.md)  
[Inkomende documenten](across-income-documents.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
