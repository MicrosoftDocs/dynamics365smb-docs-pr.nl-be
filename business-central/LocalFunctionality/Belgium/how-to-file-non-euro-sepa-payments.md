---
title: SEPA-betalingen in andere valuta's dan de euro indienen
description: In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kunt u SEPA-betalingen in andere valuta's dan de euro indienen bij de bank. Dit is handig als u betalingen verzendt naar andere landen die SEPA niet gebruiken en voor andere valuta's dan de euro.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 82cebd103d551f297020d40d4dd97a60eae4da09
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="file-non-euro-sepa-payments"></a>SEPA-betalingen in andere valuta's dan de euro indienen
In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kunt u SEPA-betalingen in andere valuta's dan de euro indienen bij de bank. Dit is handig als u betalingen verzendt naar andere landen die SEPA niet gebruiken en voor andere valuta's dan de euro.  

Voordat u een dergelijke SEPA-betalingen kunt indienen, moet u de volgende beheertaken uitvoeren:  

- Stel een nieuw exportprotocol voor een niet-euro-SEPA in. Zie Exportprotocol voor meer informatie.  
- Schakel in de tabel **Land/regio** het veld **SEPA toegestaan** uit voor elk land in de EEA-zone.  
- Controleer of de waarde in het veld **Valuta Euro** in de tabel **Boekhoudinstellingen** niet in euro's is.  
- Controleer of het veld **Bankrekening van voorkeur** in de tabel **Leverancier** de IBAN en SWIFT-code bevat.  

## <a name="to-file-a-non-euro-sepa-payment"></a>Een SEPA-betaling in andere valuta's dan de euro indienen  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **SEPA-betalingen in andere valuta's dan de euro indienen** in en klik vervolgens op de gerelateerde koppeling.  
2.  Vul de velden in zoals beschreven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Dagboeksjabloon**|Geef de dagboeksjabloon voor het SEPA-betalingsrapport op.|  
    |**Dagboekbatch**|Geef de dagboekbatch voor het SEPA-betalingsrapport op.|  
    |**Dagboekregels boeken**|Geef op of u de betalingsregels naar het grootboek wilt overbrengen.|  
    |**Dimensies opnemen**|Hier kunt u de dimensies invoeren die u in het SEPA-betalingsrapport wilt opnemen. De optie is alleen beschikbaar als het veld **Alg. dagb.regels samenvatten** in het veld **Elektronisch bankieren instellen** is geselecteerd.|  
    |**Uitvoeringsdatum**|Voer een uitvoeringsdatum in als u op de betalingsregels een datum wilt hebben die afwijkt van de boekingsdatum.|  
    |**Bestandsnaam**|Voer de naam in van het bestand, inclusief station en map, waarin u het rapport wilt afdrukken.|  

3.  Kies de knop **OK**.  

## <a name="see-also"></a>Zie ook  
 [SEPA-betalingen indienen](how-to-file-sepa-payments.md)   
 [SEPA-betalingen activeren](how-to-activate-sepa-payments.md)   
 [SEPA-betalingen](sepa-payments.md)

