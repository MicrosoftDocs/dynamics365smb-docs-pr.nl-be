---
title: Inkomende documenten instellen| Microsoft Docs
description: Gebruik de functie inkomende documenten om elektronische documenten te maken, OCR-taken te beheren, facturen te importeren en afbeeldingsbestanden te converteren.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 69cb1037da2f3873ecb9a3f498ce5fadfeabac1d
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-set-up-incoming-documents"></a>Procedure: Inkomende documenten instellen
Als u dagboekregels van inkomende documentrecords maakt, moet u in het venster **Instellingen van inkomende documenten** vastleggen welke dagboeksjabloon en batch moeten worden gebruikt.

Als u niet wilt dat gebruikers facturen of dagboekregels maken van inkomende documentrecords, tenzij de documenten zijn goedgekeurd, moet u fiatteurs instellen in het venster **Fiatteurs inkomende documenten**.

Als u PDF- en afbeeldingsbestanden naar elektronische documenten wilt omzetten waarnaar u kunt converteren, bijvoorbeeld inkoopfacturen in [!INCLUDE[d365fin](includes/d365fin_md.md)], moet u eerst de OCR-functie instellen en de service inschakelen.

Wanneer de functie Inkomende documenten is ingesteld, kunt u verschillende functies gebruiken om onkostenbewijzen te controleren, OCR-taken te beheren en inkomende documentbestanden handmatig of automatisch te converteren naar de relevante documenten of dagboekregels. De externe bestanden kunnen worden gekoppeld in elke procesfase, inclusief naar geboekte documenten en naar de resulterende leverancier, klant en grootboekposten. Zie [Inkomende documenten verwerken](across-process-income-documents.md) voor meer informatie.

## <a name="to-set-up-the-incoming-documents-feature"></a>De functie Inkomende documenten instellen
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Instellingen inkomende documenten** en klik op de gerelateerde koppeling.
2. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-approvers-of-incoming-document-records"></a>Fiatteurs van inkomende documentrecords instellen
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Instellingen inkomende documenten** en klik op de gerelateerde koppeling.  
2. Kies in het venster **Instellingen van inkomende documenten** de actie **Fiatteurs**.

    Het venster **Fiatteurs inkomende documenten** bevat alle gebruikers die zijn ingesteld in [!INCLUDE[d365fin](includes/d365fin_md.md)].  
3. Selecteer een of meer gebruikers die een inkomend document kunnen goedkeuren voordat een verwant document of verwante dagboekregel kan worden gemaakt.

Wanneer fiatteurs zijn ingesteld in het venster **Fiatteurs inkomende documenten**, kunnen alleen die gebruikers een inkomend document goedkeuren als het selectievakje **Goedkeuring vereist voor maken** is ingeschakeld in het venster **Instellingen inkomende documenten**.

> [!NOTE]  
>   Deze goedkeuringsinstellingen zijn niet gerelateerd aan goedkeuringswerkstromen. Zie voor meer informatie [Procedure: Goedkeuringswerkstromen gebruiken](across-how-use-approval-workflows.md).

## <a name="to-set-up-an-ocr-service"></a>Een OCR-service instellen
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Instellingen van OCR-service** in en klik vervolgens op de gerelateerde koppeling.
2. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-encrypt-your-login-information"></a>Uw aanmeldgegevens versleutelen
We raden u aan de aanmeldgegevens te beveiligen die u invoert in het venster **Instellingen van OCR-service**. U kunt gegevens op de server versleutelen door nieuwe encryptiesleutels te genereren of bestaande sleutels te importeren die u inschakelt op de serverinstantie die verbinding maakt met de database.

1. Kies in het venster **Instellingen van OCR-service** de actie **Versleutelingsbeheer**.
2. Schakel in het venster **Beheer gegevensversleuteling** versleuteling van uw gegevens in.

## <a name="see-also"></a>Zie ook
[Inkomende documenten verwerken](across-process-income-documents.md)  
[Inkomende documenten](across-income-documents.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

