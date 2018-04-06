---
title: CODA-bestanden van een Isabel-server downloaden
description: CODA-bestanden kunnen handmatig of in de modus Met toezicht worden gedownload.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: df740364646240f1b3512b7adb975b73106721ab
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="download-coda-files-from-an-isabel-server"></a>CODA-bestanden van een Isabel-server downloaden
> [!Note]
> [!INCLUDE[onprem_only](../../includes/onprem_only_md.md)]

CODA-bestanden kunnen handmatig of in de modus Met toezicht worden gedownload.  

Als u CODA-bestanden handmatig wilt downloaden, meldt u zich aan bij de Isabel-server en selecteert u de bestanden die u wilt downloaden. De gedownloade bestanden kunnen vervolgens worden geïmporteerd vanuit de tabel **Bankrekening**. Zie [CODA-afschriften importeren](how-to-import-coda-statements.md) voor meer informatie.  

## <a name="to-download-coda-files-in-attended-mode"></a>CODA-bestanden downloaden in de modus Met toezicht  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **IBS-logboeken** in en klik vervolgens op de gerelateerde koppeling.  
2.  Kies de actie **Downloaden**.  
3.  Vul in het venster **Opties voor IBS-downloadaanvraag** de velden in zoals wordt beschreven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Van datum**|Geef de begindatum van de download op.|  
    |**T/m datum**|Geef de einddatum van de download op.|  
    |**Bestandsindeling**|Selecteer **Coda** als de bestandsindeling.|  
    |**Bestandsstatus**|Selecteer de bestandsstatus van de download. U kunt kiezen uit **Niet gedownload**, **Gedownload** en **Alle**. Doorgaans gebruikt u **Niet gedownload** omdat u de CODA-bestanden downloadt die niet naar uw systeem zijn gedownload.|  

4.  Kies de knop **OK**.  

    > [!NOTE]  
    >  U kunt geen bestanden van de Isabel-server verwijderen in het venster **Opties voor IBS-downloadaanvraag**. U moet de bestanden handmatig verwijderen door u aan te melden bij de Isabel-server.  

     Als de CODA-bestanden zijn gedownload, wordt in het veld **Verwerkingsstatus** de waarde **Gemaakt** weergegeven in het venster **IBS-logboeken**. U kunt u aanmelden op de Isabel-server om de bestanden handmatig op te halen. Zie [CODA-afschriften importeren](how-to-import-coda-statements.md) voor meer informatie.  

## <a name="see-also"></a>Zie ook  
[Belgische lokale functionaliteit](belgium-local-functionality.md)

