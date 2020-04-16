---
title: Verkoop- en inkoopdocumenten archiveren | Microsoft Docs
description: U kunt verkoop- en inkooporders, offertes, raamcontracten, retourorders en raamcontracten archiveren en u kunt het gearchiveerde document gebruiken om het document waaruit het is gearchiveerd, opnieuw te maken.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: sgroespe
ms.openlocfilehash: 5e8aa5a7baaf8ef8ce6d0352bbfd8cd01c77e01d
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3188456"
---
# <a name="archive-documents"></a>Documenten archiveren
U kunt verkoop- en inkooporders, offertes, retourorders en raamcontracten comprimeren, bijvoorbeeld omdat u een kopie van een document voor hergebruik later wilt opslaan. U kunt een verkoop- of inkoopdocument meerdere keren archiveren, waarbij u steeds een verschillende gearchiveerde versie opslaat.

Voor gearchiveerde documenten waarvan het origineel nog bestaat en niet is geboekt, kunt u de functie **Herstellen** gebruiken om het origineel te overschrijven met de gearchiveerde versie van het document. Dit is handig als u de inhoud van een document naar een eerdere status moet herstellen.

Voor gearchiveerde documenten waarvan het origineel is verwijderd, kunt u de inhoud alleen opnieuw gebruiken door de gegevens te kopiëren, bijvoorbeeld met de functie **Kopiëren uit document**.   

## <a name="to-set-up-automatic-document-archiving"></a>Automatische documentarchivering instellen  
U kunt automatische archivering van verkoop- en inkooporders, offertes, raamcontracten en retourorders instellen voordat u documenten verwijdert.

In de volgende procedure wordt beschreven hoe u automatische archivering van verkoopdocumenten instelt. De stappen zijn vergelijkbaar voor inkoopdocumenten.
1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopinstellingen** in en kies de desbetreffende koppeling.
2. Vul op de pagina **Instellingen van verkoop en tegoeden** de velden als volgt in:

|Veld|Description|
|-----|-----------|
|**Verkoopoffertes archiveren**|**Nooit** om verkoopoffertes nooit te archiveren wanneer deze worden verwijderd. **Vraag** om de gebruiker te laten kiezen of verkoopoffertes moeten worden gearchiveerd wanneer ze worden verwijderd. **Altijd** om verkoopoffertes automatisch te archiveren wanneer deze worden verwijderd.|
|**Raamcontractorders archiveren**|Selecteer dit om raamcontactorders steeds automatisch te archiveren wanneer ze worden verwijderd.|
|**Orders en retourorders archiveren**|Selecteer dit om steeds automatisch verkooporders te archiveren wanneer ze worden verwijderd.|

## <a name="to-archive-a-sales-order"></a>Een verkooporder archiveren
In de volgende procedure wordt beschreven hoe u een verkooporder archiveert. De stappen zijn vergelijkbaar voor alle orders, raamcontracten, retourorders en offertes.

1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies de gerelateerde koppeling.  
2.  Open een verkooporder die u wilt archiveren.  
3.  Kies de actie **Document archiveren**.

De verkooporder wordt gearchiveerd. U kunt deze bekijken op de pagina **Gearchiveerde verkooporders**.

## <a name="to-restore-a-non-posted-sales-order-from-the-archive"></a>Een niet-geboekte verkooporder vanuit het archief herstellen
In de volgende procedure wordt beschreven hoe de inhoud van een gearchiveerde verkooporder terug wordt gebracht tot de oorspronkelijke verkooporder. Dit kan alleen als het oorspronkelijke document niet is geboekt. De stappen zijn vergelijkbaar voor alle orders, raamcontracten, retourorders en offertes.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gearchiveerde verkooporders** in en kies de gerelateerde koppeling.
2. Selecteer de gearchiveerde verkooporder of versie ervan die u wilt herstellen en kies vervolgens de actie **Herstellen**.  

De inhoud van de oorspronkelijke verkooporder wordt vervangen door die van de geselecteerde gearchiveerde versie.

## <a name="to-delete-archived-sales-orders"></a>Gearchiveerde verkooporders verwijderen
In de volgende procedure wordt beschreven hoe gearchiveerde verkooporders verwijdert. De stappen lijken op andere gearchiveerde inkoop- en verkoopdocumenten.

1.  Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gearch. verk.-orderversies verwijderen** in en kies de gerelateerde koppeling.  
2.  Selecteer op de pagina **Gearch. verk.-orderversies verwijderen** de gewenste filters.  
3.  Kies de knop **OK**.

## <a name="see-also"></a>Zie ook
[Documentregels traceren](across-how-to-track-document-lines.md)  
[Verkoop](sales-manage-sales.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
