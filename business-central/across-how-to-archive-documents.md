---
title: Verkoop- en inkoopdocumenten archiveren | Microsoft Docs
description: U kunt verkoop- en inkooporders, offertes, raamcontracten, retourorders en raamcontracten archiveren en u kunt het gearchiveerde document gebruiken om het document waaruit het is gearchiveerd, opnieuw te maken.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 12/21/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 74460bfcff36d293006229f4a89719f8c05c2631
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="archive-documents"></a>Documenten archiveren
U kunt verkoop- en inkooporders, offertes, raamcontracten, retourorders en raamcontracten archiveren en u kunt het gearchiveerde document gebruiken om het document waaruit het is gearchiveerd, opnieuw te maken.

## <a name="to-set-up-automatic-document-archiving"></a>Automatische documentarchivering instellen  
U kunt automatische archivering van verkoop- en inkooporders, offertes, raamcontracten en retourorders instellen voordat u documenten verwijdert.

In de volgende procedure wordt beschreven hoe u automatische archivering van verkoopdocumenten instelt. De stappen zijn vergelijkbaar voor inkoopdocumenten.
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Instellingen van verkoop en tegoeden** in en klik vervolgens op de gerelateerde koppeling.
2. Vul in het venster **Instellingen van verkoop en tegoeden** de velden als volgt in:

|Veld|Description|
|-----|-----------|
|**Verkoopoffertes archiveren**|**Nooit** om verkoopoffertes nooit te archiveren wanneer deze worden verwijderd. **Vraag** om de gebruiker te laten kiezen of verkoopoffertes moeten worden gearchiveerd wanneer ze worden verwijderd. **Altijd** om verkoopoffertes automatisch te archiveren wanneer deze worden verwijderd.|
|**Raamcontractorders archiveren**|Selecteer dit om raamcontactorders steeds automatisch te archiveren wanneer ze worden verwijderd.|
|**Orders en retourorders archiveren**|Selecteer dit om steeds automatisch verkooporders te archiveren wanneer ze worden verwijderd.|

## <a name="to-archive-a-sales-order"></a>Een verkooporder archiveren
In de volgende procedure wordt beschreven hoe u een verkooporder archiveert. De stappen zijn vergelijkbaar voor alle orders, raamcontracten, retourorders en offertes.

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verkooporders** in en klik vervolgens op de gerelateerde koppeling.  
2.  Open een verkooporder die u wilt archiveren.  
3.  Kies de actie **Document archiveren**.

De verkooporder wordt gearchiveerd. U kunt deze bekijken in het venster **Gearchiveerde verkooporders**. Van hieruit kunt u deze ook gebruiken om de verkooporder waaruit deze is gearchiveerd, opnieuw te maken.

## <a name="to-recreate-a-sales-order-from-the-archive"></a>Een verkooporder maken vanuit het archief
In de volgende procedure wordt beschreven hoe u een verkooporder opnieuw maakt. De stappen zijn vergelijkbaar voor alle orders, raamcontracten, retourorders en offertes.

1.  Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Gearchiveerde verkooporders** in en klik vervolgens op de gerelateerde koppeling.
2.  Selecteer de gearchiveerde verkooporder die u opnieuw wilt maken en kies vervolgens de actie **Herstellen**.  

De verkooporder wordt gemaakt en toegevoegd aan het venster **Verkooporders**.

## <a name="to-delete-archived-sales-orders"></a>Gearchiveerde verkooporders verwijderen
In de volgende procedure wordt beschreven hoe gearchiveerde verkooporders verwijdert. De stappen lijken op andere gearchiveerde inkoop- en verkoopdocumenten.

1.  Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Gearch. verk.-orderversies verwijderen** in en klik vervolgens op de gerelateerde koppeling.  
2.  Selecteer in het venster **Gearch. verk.-orderversies verwijderen** de gewenste filters.  
3.  Kies de knop **OK**.

## <a name="see-also"></a>Zie ook
[Documentregels traceren](across-how-to-track-document-lines.md)  
[Verkoop](sales-manage-sales.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

