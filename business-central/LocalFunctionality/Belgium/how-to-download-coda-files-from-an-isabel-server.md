---
title: CODA-bestanden van een Isabel-server downloaden
description: CODA-bestanden kunnen handmatig of in de modus Met toezicht worden gedownload.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2018
ms.author: sgroespe
ms.openlocfilehash: d7b81574cefed5da4b6520733365f689f0aec933
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "826404"
---
# <a name="download-coda-files-from-an-isabel-server"></a>CODA-bestanden van een Isabel-server downloaden
> [!Note]
> [!INCLUDE[onprem_only](../../includes/onprem_only_md.md)]

CODA-bestanden kunnen handmatig of in de modus Met toezicht worden gedownload.  

Als u CODA-bestanden handmatig wilt downloaden, meldt u zich aan bij de Isabel-server en selecteert u de bestanden die u wilt downloaden. De gedownloade bestanden kunnen vervolgens worden geïmporteerd vanuit de tabel **Bankrekening**. Zie [CODA-afschriften importeren](how-to-import-coda-statements.md) voor meer informatie.  

## <a name="to-download-coda-files-in-attended-mode"></a>CODA-bestanden downloaden in de modus Met toezicht  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **IBS-logboeken** in en klik vervolgens op de gerelateerde koppeling.  
2.  Kies de actie **Downloaden**.  
3.  Vul op de pagina **Opties voor IBS-downloadaanvraag** de velden in zoals wordt beschreven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Van datum**|Geef de begindatum van de download op.|  
    |**T/m datum**|Geef de einddatum van de download op.|  
    |**Bestandsindeling**|Selecteer **Coda** als de bestandsindeling.|  
    |**Bestandsstatus**|Selecteer de bestandsstatus van de download. U kunt kiezen uit **Niet gedownload**, **Gedownload** en **Alle**. Doorgaans gebruikt u **Niet gedownload** omdat u de CODA-bestanden downloadt die niet naar uw systeem zijn gedownload.|  

4.  Kies de knop **OK**.  

    > [!NOTE]  
    >  U kunt geen bestanden van de Isabel-server verwijderen op de pagina **Opties voor IBS-downloadaanvraag**. U moet de bestanden handmatig verwijderen door u aan te melden bij de Isabel-server.  

     Als de CODA-bestanden zijn gedownload, wordt in het veld **Verwerkingsstatus** de waarde **Gemaakt** weergegeven op de pagina **IBS-logboeken**. U kunt u aanmelden op de Isabel-server om de bestanden handmatig op te halen. Zie [CODA-afschriften importeren](how-to-import-coda-statements.md) voor meer informatie.  

## <a name="see-also"></a>Zie ook  
[Belgische lokale functionaliteit](belgium-local-functionality.md)
