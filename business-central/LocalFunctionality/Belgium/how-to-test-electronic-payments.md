---
title: Elektronische betalingen testen
description: Nadat u elektronisch bankieren hebt ingesteld en betalingsvoorstellen hebt gegenereerd, kunt u de betalingsdagboekregels op fouten testen voordat u ze boekt.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: f4c3fb422a4e34a6c16a17db6b2a3f13a898e547
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3778410"
---
# <a name="test-electronic-payments"></a>Elektronische betalingen testen
Nadat u elektronisch bankieren hebt ingesteld en betalingsvoorstellen hebt gegenereerd, kunt u de betalingsdagboekregels op fouten testen voordat u ze boekt.  

Hierbij wordt onder andere het volgende gevalideerd:  

- Of bankrekeningnummers geldig zijn.  
- Of positieve betalingsregels aanwezig zijn.  
- Of binnenlandse en internationale betalingen via slechts één rekening worden uitgevoerd.  
- Of er slechts één bankrekening kan worden gebruikt voor Isabel (Interbanks Standards Association Belgium).  
- Of betalingsregels in euro zijn voor SEPA (Single Euro Payments Area).  
- Of er een nummerreeks voor SEPA is gedefinieerd.  

U kunt de fouten bekijken op de pagina **Logboeken voor controlefouten exporteren**.  

> [!IMPORTANT]  
>  U moet alle fouten corrigeren voordat u de regels kunt boeken.  

## <a name="to-test-payment-journal-lines"></a>Betalingsdagboekregels testen  

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsdagboeken** in en kies vervolgens de gerelateerde koppeling.  
2.  Selecteer in het veld **Batchnaam** de vereiste dagboekbatch.  
3.  Selecteer in het veld **Exportprotocol** het exportprotocol.  
4.  Voer de betalingsdagboekregelinformatie in en kies vervolgens de actie **Betalingsregels controleren** om de betalingsdagboekregels te valideren. Welke validatie op de dagboekregels wordt uitgevoerd, is afhankelijk van de soort controle die op de pagina **Exportprotocollen** is opgegeven.  

## <a name="see-also"></a>Zie ook  
 [Belgische elektronische betalingen](belgian-electronic-payments.md)   
 [Leveranciers voor automatische betalingsvoorstellen instellen](how-to-set-up-vendors-for-automatic-payment-suggestions.md)   
 [Betalingsvoorstellen genereren](how-to-generate-payment-suggestions.md)   
 [Betalingsbestanden afdrukken](how-to-print-payment-files.md)
