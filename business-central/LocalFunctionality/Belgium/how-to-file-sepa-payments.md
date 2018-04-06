---
title: SEPA-betalingen indienen
description: In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kunt u SEPA-kredietoverboekingen (Single Euro Payments Area) gebruiken om SEPA-betalingen in te dienen bij de bank.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: effecef4471b12032fb4e3d2ab3b198fd0e1a249
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="file-sepa-payments"></a>SEPA-betalingen indienen
In [!INCLUDE[d365fin](../../includes/d365fin_md.md)] kunt u SEPA-kredietoverboekingen (Single Euro Payments Area) gebruiken om SEPA-betalingen in te dienen bij de bank.  

SEPA verenigt de betalingsmethoden in deelnemende Europese landen/regio's, zodat internationale betalingen even gemakkelijk te verwerken worden als binnenlandse betalingen. Europese burgers en bedrijven kunnen betalingen in euro's verrichten en ontvangen, binnen of buiten nationale grenzen, onder dezelfde basisomstandigheden, -rechten en -verplichtingen, ongeacht de locatie.  

Voordat u een SEPA-betaling kunt indienen, moet u de volgende beheertaken uitvoeren:  

- Stel een nieuw exportprotocol in. Zie Exportprotocol voor meer informatie.  
- Schakel in de tabel **Land/regio** het veld **SEPA toegestaan** in voor elk land in de EEA-zone.  
- Controleer of de waarde in het veld **Valuta Euro** in de tabel **Boekhoudinstellingen** overeenkomt met de valuta op de betalingsregels.  
- Controleer of het veld **Bankrekening van voorkeur** in de tabel **Leverancier** de IBAN en SWIFT-code bevat.  

## <a name="to-file-a-sepa-payment"></a>Een SEPA-betaling indienen  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **SEPA-betalingen indienen** in en klik vervolgens op de gerelateerde koppeling.  
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
 [Exportprotocollen instellen](how-to-set-up-export-protocols.md)   
 [SEPA-betalingen in andere valuta's dan de euro indienen](how-to-file-non-euro-sepa-payments.md)   
 [SEPA-betalingen activeren](how-to-activate-sepa-payments.md)

