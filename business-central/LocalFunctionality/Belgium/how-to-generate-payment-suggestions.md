---
title: Betalingsvoorstellen genereren
description: Als u elektronisch bankieren hebt ingesteld, kunt u beginnen met het genereren van betalingsvoorstellen. U kunt dit doen in het betalingsdagboek.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 31804146cca328c7a3155bf2f310b96864135c1a
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5379544"
---
# <a name="generate-payment-suggestions"></a>Betalingsvoorstellen genereren
Als u elektronisch bankieren hebt ingesteld, kunt u beginnen met het genereren van betalingsvoorstellen. U kunt dit doen in het betalingsdagboek.  

## <a name="to-generate-payment-suggestions"></a>Betalingsvoorstellen genereren  

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsdagboeken** in en kies vervolgens de gerelateerde koppeling.  
2.  Selecteer de juiste dagboekbatch en kies vervolgens de actie **Leveranciersbetalingen voorstellen**.  
3.  Vul op de pagina **Leveranciersbetalingen voorstellen** de velden in zoals wordt beschreven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Uiterste vervaldatum**|Typ de uiterste vervaldatum voor de leveranciersposten in de batchverwerking.|  
    |**Creditnota's maken**|Selecteer deze optie om openstaande creditnota's voor leveranciers op te nemen. De creditnota's worden van het verschuldigde bedrag afgetrokken. Wanneer u creditnota's selecteert, wordt de vervaldatum niet gebruikt.|  
    |**Contantkorting nemen**|Selecteer deze optie om op te geven of u in de batchverwerking posten wilt opnemen waarvoor u een contantkorting kunt krijgen.|  
    |**Kortingsvervaldatum betaling**|Typ de datum die wordt gebruikt om een contantkorting te berekenen.|  
    |**Beschikbaar bedrag**|Typ hier eventueel een maximumbedrag dat beschikbaar is voor betalingen. Tijdens de batchverwerking wordt dan een betalingsvoorstel op basis van dit bedrag en de prioriteit van leveranciers gedaan.|  
    |**Boekingsdatum**|typ hier de datum die als boekingsdatum verschijnt op de regels die tijdens de batchverwerking in het betalingsdagboek worden ingevoegd.|  

4.  Voer de filtercriteria in.  
5.  Kies **OK** om de batchverwerking te starten.  

Wanneer de batchverwerking is uitgevoerd, bevat het betalingsdagboek alle leveranciersposten die overeenkomen met de filters.  

## <a name="see-also"></a>Zie ook  
 [Belgische elektronische betalingen](belgian-electronic-payments.md)   
 [Leveranciers voor automatische betalingsvoorstellen instellen](how-to-set-up-vendors-for-automatic-payment-suggestions.md)   
 [Betalingsdagboeksjablonen en -batches maken](how-to-create-payment-journal-templates-and-batches.md)   
 [Elektronische betalingen testen](how-to-test-electronic-payments.md)   
 [Regels voor elektronische betalingen beheren](how-to-manage-electronic-payment-lines.md)   
 [Betalingsbestanden afdrukken](how-to-print-payment-files.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]