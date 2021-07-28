---
title: Betalingsbestanden exporteren in de Belgische versie
description: Als u een testrapport hebt afgedrukt en alle fouten hebt gecorrigeerd, kunt u betalingsdagboekregels naar een betalingsbestand afdrukken in de Belgische versie van Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: ''
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 73c142f460f208a6350e48bba54535fd2d77c7d6
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6435205"
---
# <a name="export-payment-files-in-the-belgian-version"></a>Betalingsbestanden exporteren in de Belgische versie

Als u een testrapport hebt afgedrukt en alle fouten hebt gecorrigeerd, kunt u betalingsdagboekregels naar een betalingsbestand exporteren.  

Een betalingsbestand bevat binnenlandse, internationale of SEPA-betalingen (in euro's of in een andere valuta). Het bestand kan elektronisch naar een bank worden verzonden. U kunt slechts één bestand per boekingsdatum en valutacode maken. Wanneer u de betalingen naar een bestand exporteert, wordt er een bijbehorende notitie afgedrukt die ook naar de bank kan worden verzonden.  

In het betalingsdagboek wordt het veld **Status** op de geëxporteerde regels ingesteld op **Geboekt**.  

## <a name="to-print-a-payment-file"></a>Een betalingsbestand afdrukken  

1. Kies het pictogram ![lampje dat de functie Vertel me opent.](../../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Betalingsdagboek** in en kies de koppelingen om de pagina **EB-betalingsdagboek** te openen.  
2. Selecteer in het veld **Batchnaam** de vereiste dagboekbatch.  
3. Selecteer in het veld **Exportprotocol** het exportprotocol.  

    Exportprotocollen bepalen welk betalingsbestand in het betalingsdagboek wordt gegenereerd. U kunt een combinatie van exportindelingen in één batch hebben, bijvoorbeeld binnenlandse, internationale en SEPA-betalingen. Wanneer u de betalingsregels naar een bestand exporteert, kunt u slechts één exportindeling, of exportprotocol, gebruiken.  

    > [!NOTE]
    > Door het exportprotocol op te geven, geeft u ook het validatietype op dat wordt uitgevoerd in het betalingsdagboek.
4. Voer de betalingsdagboekregelinformatie in en kies vervolgens de actie **Betalingsregels controleren**.

    De pagina **Logboeken voor controlefouten exporteren** bevat eventuele fouten. Als er fouten zijn, moet u deze oplossen voordat u kunt doorgaan.

5. Als er geen fouten zijn, kiest u de actie **Betalingsregels exporteren**.  

    Het rapport dat u in het betreffende exportprotocol hebt opgegeven, verwerkt de betalingregels en genereert het bestand.  

## <a name="see-also"></a>Zie ook

[Elektronisch bankieren voor België](belgian-electronic-banking.md)  
[Belgische elektronische betalingen](belgian-electronic-payments.md)  
[Leveranciers voor automatische betalingsvoorstellen instellen](how-to-set-up-vendors-for-automatic-payment-suggestions.md)  
[Leveranciersbetalingen voorstellen](../../payables-how-suggest-vendor-payments.md)  
[Betalingsdagboeksjablonen en -batches maken](how-to-create-payment-journal-templates-and-batches.md)  
[Elektronische betalingen testen](how-to-test-electronic-payments.md)  
