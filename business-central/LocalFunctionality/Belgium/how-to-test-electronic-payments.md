---
title: Elektronische betalingen testen
description: Nadat u elektronisch bankieren hebt ingesteld en betalingsvoorstellen hebt gegenereerd, kunt u de betalingsdagboekregels op fouten testen voordat u ze boekt.
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
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: 9edf27caaea179b1a8fb62dcc34e2e7fe097a157
ms.contentlocale: nl-be
ms.lasthandoff: 11/26/2018

---
# <a name="test-electronic-payments"></a>Elektronische betalingen testen
> [!Note]
> [!INCLUDE[onprem_only](../../includes/onprem_only_md.md)]

Nadat u elektronisch bankieren hebt ingesteld en betalingsvoorstellen hebt gegenereerd, kunt u de betalingsdagboekregels op fouten testen voordat u ze boekt.  

Hierbij wordt onder andere het volgende gevalideerd:  

- Bankrekeningnummers zijn geldig.  
- Positieve betalingsregels zijn aanwezig.  
- Of binnenlandse en internationale betalingen via slechts één rekening worden uitgevoerd.  
- Of slechts één bankrekening kan worden gebruikt voor Isabel.  
- Of betalingsregels in euro's worden weergegeven voor SEPA.  
- Of er een nummerreeks voor SEPA is gedefinieerd.  

U kunt de fouten bekijken op de pagina **Logboeken voor controlefouten exporteren**.  

> [!IMPORTANT]  
>  U moet alle fouten corrigeren voordat u de regels kunt boeken.  

## <a name="to-test-payment-journal-lines"></a>Betalingsdagboekregels testen  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Betalingsdagboeken** in en klik vervolgens op de gerelateerde koppeling.  
2.  Selecteer in het veld **Batchnaam** de vereiste dagboekbatch.  
3.  Selecteer in het veld **Exportprotocol** het exportprotocol.  
4.  Voer de betalingsdagboekregelinformatie in en kies vervolgens de actie **Betalingsregels controleren** om de betalingsdagboekregels te valideren. Welke validatie op de dagboekregels wordt uitgevoerd, is afhankelijk van de soort controle die op de pagina **Exportprotocollen** is opgegeven.  

## <a name="see-also"></a>Zie ook  
 [Belgische elektronische betalingen](belgian-electronic-payments.md)   
 [Leveranciers voor automatische betalingsvoorstellen instellen](how-to-set-up-vendors-for-automatic-payment-suggestions.md)   
 [Betalingsvoorstellen genereren](how-to-generate-payment-suggestions.md)   
 [Betalingsbestanden afdrukken](how-to-print-payment-files.md)

