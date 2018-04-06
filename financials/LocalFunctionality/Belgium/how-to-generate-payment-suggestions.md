---
title: Betalingsvoorstellen genereren
description: Als u elektronisch bankieren hebt ingesteld, kunt u beginnen met het genereren van betalingsvoorstellen. U kunt dit doen in het betalingsdagboek.
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
ms.openlocfilehash: 1c7a748f48cb36b30851795119a072ab6d77c961
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="generate-payment-suggestions"></a>Betalingsvoorstellen genereren
Als u elektronisch bankieren hebt ingesteld, kunt u beginnen met het genereren van betalingsvoorstellen. U kunt dit doen in het betalingsdagboek.  

## <a name="to-generate-payment-suggestions"></a>Betalingsvoorstellen genereren  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Betalingsdagboeken** in en klik vervolgens op de gerelateerde koppeling.  
2.  Selecteer de juiste dagboekbatch en kies vervolgens de actie **Leveranciersbetalingen voorstellen**.  
3.  Vul in het venter **Leveranciersbetalingen voorstellen** op het tabblad **Opties** de velden in zoals wordt beschreven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Uiterste vervaldatum**|Typ de uiterste vervaldatum voor de leveranciersposten in de batchverwerking.|  
    |**Creditnota's maken**|Selecteer deze optie om openstaande creditnota's voor leveranciers op te nemen. De creditnota's worden van het verschuldigde bedrag afgetrokken. Wanneer u creditnota's selecteert, wordt de vervaldatum niet gebruikt.|  
    |**Contantkorting nemen**|Selecteer deze optie om op te geven of u in de batchverwerking posten wilt opnemen waarvoor u een contantkorting kunt krijgen.|  
    |**Kortingsvervaldatum betaling**|Typ de datum die wordt gebruikt om een contantkorting te berekenen.|  
    |**Beschikbaar bedrag**|Typ hier eventueel een maximumbedrag dat beschikbaar is voor betalingen. Tijdens de batchverwerking wordt dan een betalingsvoorstel op basis van dit bedrag en de prioriteit van leveranciers gedaan.|  
    |**Boekingsdatum**|typ hier de datum die als boekingsdatum verschijnt op de regels die tijdens de batchverwerking in het betalingsdagboek worden ingevoegd.|  

4.  Voer de filtercriteria op het sneltabblad **Leverancier** in.  
5.  Kies **OK** om de batchverwerking te starten.  

Wanneer de batchverwerking is uitgevoerd, bevat het betalingsdagboek alle leveranciersposten die overeenkomen met de filters.  

## <a name="see-also"></a>Zie ook  
 [Belgische elektronische betalingen](belgian-electronic-payments.md)   
 [Leveranciers voor automatische betalingsvoorstellen instellen](how-to-set-up-vendors-for-automatic-payment-suggestions.md)   
 [Betalingsdagboeksjablonen en -batches maken](how-to-create-payment-journal-templates-and-batches.md)   
 [Elektronische betalingen testen](how-to-test-electronic-payments.md)   
 [Regels voor elektronische betalingen beheren](how-to-manage-electronic-payment-lines.md)   
 [Betalingsbestanden afdrukken](how-to-print-payment-files.md)

