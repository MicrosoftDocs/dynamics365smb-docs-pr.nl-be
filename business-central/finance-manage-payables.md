---
title: Crediteuren beheren| Microsoft Docs
description: Overzicht van hoe u crediteuren (AP) beheert, inclusief leveranciersbetalingen, crediteuren, schuld en verschuldigd saldo.
services: project-madeira
documentationcenter: ''
author: bholtorf
manager: edupont
editor: ''
ms.service: dynamics365-business-central
ms.workload: na
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 04/01/2019
ms.author: bholtorf
redirect_url: finance-set-up-cost-accounting
ms.openlocfilehash: f7556b204403f0abdb6361a0e1650b90e58810e1
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "931711"
---
# <a name="managing-payables"></a>Betalingsverplichtingen beheren
[!INCLUDE[d365fin](includes/d365fin_md.md)] heeft alles wat u nodig hebt om uw betalingsverplichtingen efficiënt te beheren.  

## <a name="payments"></a>Betalingen
U kunt eenvoudig betalingen prioriteit geven, rekening houden met boetes voor late betalingen en kortingen voor tijdige betalingen verwerken.

U kunt betalingen registreren in een diversendagboek en vervolgens cheques afdrukken voordat het betalingsdagboek wordt geboekt.

U kunt betalingen vereffenen om facturen te sluiten wanneer u de betaling boekt of nadat u de betaling hebt geboekt. Met het veld **Vereffeningsmethode** dat is opgegeven voor de leverancier (op de **Leverancierskaart**), wordt bepaald of u de betaling handmatig of automatisch vereffend. U kunt transacties altijd handmatig vereffenen. Als de vereffeningsmethode voor de leverancier echter is ingesteld op **Toepassen op oudste** en u geen document opgeeft waarmee de betaling wordt vereffend, wordt de betaling vereffend met de oudste open post van de leverancier.

## <a name="suggest-vendor-payments"></a>Leveranciersbetalingen voorstellen
[!INCLUDE[d365fin](includes/d365fin_md.md)] heeft een functie die voorstellen kan doen voor betalingen aan leveranciers. Zo krijgt u bijvoorbeeld een bericht als de vervaldatum voor een betaling nadert of als voor een betaling een korting mogelijk is. In het betalingsvoorstel kan een bedrag worden meegenomen dat u opgeeft als beschikbaar kapitaal, en geschiktheid voor contantkortingen.

## <a name="issue-checks"></a>Cheques uitgeven
Met [!INCLUDE[d365fin](includes/d365fin_md.md)] kunt u cheques elektronisch en handmatig uitgeven aan leveranciers. Dit doet u beide op de pagina **Betalingsdagboeken**, waarin u cheques ook ongeldig kunt maken en chequeposten kunt bekijken.

## <a name="export-payments-to-a-bank-file"></a>Betalingen naar een bankbestand exporteren
Wanneer u klaar bent om een leverancier te betalen, kunt u met behulp van de pagina **Betalingsdagboek** een bestand met de betalingsgegevens exporteren van de dagboekregels. Vervolgens kunt u het bestand uploaden naar uw elektronische bank voor verwerking van de overboekingen.

Als u geen betalingsdagboekregel voor een geëxporteerde betaling wilt boeken, bijvoorbeeld omdat u op bevestiging wacht dat de transactie door de bank is verwerkt, kunt u de dagboekregel gewoon verwijderen. Wanneer u later een betalingsdagboekregel maakt om het restbedrag op de factuur te betalen, bevat het veld **Totaal geëxporteerd bedrag** het gedeelte van het betalingsbedrag dat al is geëxporteerd. U kunt ook gedetailleerde gegevens vinden over het geëxporteerde totaal door de knop **Krediettransferregisterposten** te kiezen.

Als u wacht met het boeken van betalingen totdat uw bank bevestigt dat transacties zijn verwerkt, kunt u op twee manieren voorkomen dat betalingen voor open documenten per ongeluk opnieuw worden geëxporteerd:  

* U kunt in een betalingsdagboek met voorgestelde betalingsregels sorteren op de kolom **Naar betalingsbestand geëxporteerd** of **Totaal geëxporteerd bedrag** en vervolgens betalingsvoorstellen verwijderen voor openstaande facturen waarvoor al betalingen zijn verricht en waarvoor u geen betalingen meer wilt verrichten.

    **Opmerking**: u moet deze kolommen mogelijk aan de lijst toevoegen. Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.  
* Zo kunt u ook in de batchverwerking **Leveranciersbetalingen voorstellen**, waarmee u opgeeft welke betalingen in het betalingsdagboek moeten worden opgenomen, opgeven dat dagboekregels voor betalingen die al zijn geëxporteerd, niet moeten worden ingevoegd door het selectievakje **Geëxporteerde betalingen overslaan** te kiezen.

## <a name="see-also"></a>Zie ook
[Betalingsmethoden](finance-payment-methods.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
