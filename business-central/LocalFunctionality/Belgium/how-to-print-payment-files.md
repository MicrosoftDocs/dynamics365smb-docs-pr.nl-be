---
title: Betalingsbestanden afdrukken in de Belgische versie
description: Als u een testrapport hebt afgedrukt en alle fouten hebt gecorrigeerd, kunt u betalingsdagboekregels naar een betalingsbestand afdrukken in de Belgische versie van Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: a2536af3bc33354a782a840c4320cc61a217af7a
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5779221"
---
# <a name="print-payment-files"></a>Betalingsbestanden afdrukken

Als u een testrapport hebt afgedrukt en alle fouten hebt gecorrigeerd, kunt u betalingsdagboekregels naar een betalingsbestand afdrukken.  

Een betalingsbestand bevat binnenlandse, internationale of SEPA-betalingen (in euro's of in een andere valuta). Het bestand kan per schijf of via een modem of Isabel (Interbanks Standards Association Belgium) worden verzonden. U kunt slechts één bestand per boekingsdatum en valutacode maken. Wanneer u de betalingen naar een bestand exporteert, wordt er een bijbehorende notitie afgedrukt die ook naar de bank kan worden verzonden.  

In het betalingsdagboek wordt het veld **Status** op de geëxporteerde regels ingesteld op **Geboekt**.  

## <a name="to-print-a-payment-file"></a>Een betalingsbestand afdrukken  

1. Kies het pictogram ![lampje dat de functie Vertel me opent](../../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsdagboek** in en kies vervolgens de koppeling om de pagina **EB-betalingsdagboek** te openen.  
2. Selecteer in het veld **Batchnaam** de vereiste dagboekbatch.  
3. Selecteer in het veld **Exportprotocol** het exportprotocol.  

    Exportprotocollen bepalen welk betalingsbestand in het betalingsdagboek wordt gegenereerd. U kunt een combinatie van exportindelingen in één batch hebben, bijvoorbeeld binnenlandse, internationale en SEPA-betalingen. Wanneer u de betalingsregels naar een bestand exporteert, kunt u slechts één exportindeling, of exportprotocol, gebruiken.  

    > [!NOTE]
    > Door het exportprotocol op te geven, geeft u ook het validatietype op dat wordt uitgevoerd in het betalingsdagboek.
4. Voer de betalingsdagboekregelinformatie in en kies vervolgens de actie **Betalingsregels controleren**.

    De pagina **Logboeken voor controlefouten exporteren** bevat eventuele fouten. Als er fouten zijn, moet u deze oplossen voordat u kunt doorgaan.

5. Als er geen fouten zijn, kiest u de actie **Betalingsregels exporteren**.  

    Vervolgens wordt het rapport geopend dat u in het veld **Testrapport-id** in **Betalingsdagboeksjablonen** hebt opgegeven.  

6. Klik op **Afdrukken**.  

## <a name="see-also"></a>Zie ook

[Elektronisch bankieren voor België](belgian-electronic-banking.md)  
[Belgische elektronische betalingen](belgian-electronic-payments.md)  
[Leveranciers voor automatische betalingsvoorstellen instellen](how-to-set-up-vendors-for-automatic-payment-suggestions.md)  
[Leveranciersbetalingen voorstellen](../../payables-how-suggest-vendor-payments.md)  
[Betalingsdagboeksjablonen en -batches maken](how-to-create-payment-journal-templates-and-batches.md)  
[Elektronische betalingen testen](how-to-test-electronic-payments.md)  
