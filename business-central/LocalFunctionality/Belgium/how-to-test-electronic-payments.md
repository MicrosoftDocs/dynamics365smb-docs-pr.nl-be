---
title: 'Elektronische betalingen testen [BE]'
description: 'Nadat u elektronisch bankieren hebt ingesteld en betalingsvoorstellen hebt gegenereerd, kunt u de betalingsdagboekregels op fouten testen voordat u ze boekt.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 2000001
ms.date: 06/17/2021
ms.author: bholtorf
---
# <a name="test-electronic-payments-in-the-belgian-version"></a>Elektronische betalingen testen in de Belgische versie

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
> U moet alle fouten corrigeren voordat u de regels kunt boeken.  

## <a name="to-test-payment-journal-lines"></a>Betalingsdagboekregels testen

1. Kies het pictogram ![lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Betalingsdagboeken** in en kies de koppelingen om de pagina **EB-betalingsdagboeken** te openen.  
2. Selecteer in het veld **Batchnaam** de vereiste dagboekbatch.  
3. Selecteer in het veld **Exportprotocol** het exportprotocol.  
4. Voer de betalingsdagboekregelinformatie in en kies vervolgens de actie **Betalingsregels controleren** om de betalingsdagboekregels te valideren. Welke validatie op de dagboekregels wordt uitgevoerd, is afhankelijk van de soort controle die op de pagina **Exportprotocollen** is opgegeven.  

## <a name="see-also"></a>Zie ook

[Betalingsdagboeksjablonen en -batches maken](how-to-create-payment-journal-templates-and-batches.md)  
[Belgische elektronische betalingen](belgian-electronic-payments.md)  
[Leveranciers voor automatische betalingsvoorstellen instellen](how-to-set-up-vendors-for-automatic-payment-suggestions.md)  
[Leveranciersbetalingen voorstellen](../../payables-how-suggest-vendor-payments.md)  
[Betalingsbestanden afdrukken](how-to-print-payment-files.md)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
