---
title: Werken met diversendagboeken | Microsoft Docs
description: Leren hoe diversendagboeken werken.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 02/03/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 13257a5d82d742d92fb22da9da7ff7f773d7d2f8
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="working-with-general-journals"></a>Werken met diversendagboeken
Met diversendagboeken kunt u financiële transacties naar grootboekrekeningen en andere rekeningen boeken, zoals bank-, klant- en leveranciersrekeningen. Door te boeken met een dagboek worden er altijd posten gemaakt in grootboekrekeningen. Dit geldt zelfs ook als u bijvoorbeeld een dagboekregel naar een klantrekening boekt, omdat een post via een boekingsgroep is geboekt naar een rekening met vorderingen in het grootboek.

[!INCLUDE[d365fin](includes/d365fin_md.md)] heeft ook niet-financiële dagboeken, zoals het artikeldagboek en het inventarisatiedagboek, maar deze dagboeken zijn niet zichtbaar in de gebruikersinterface.

De informatie die u invoert in een dagboek is tijdelijk en kan in het dagboek worden gewijzigd. Wanneer u het dagboek boekt, wordt de informatie overgedragen naar de posten van afzonderlijke rekeningen, waar de informatie niet meer kan worden gewijzigd. U kunt echter de vereffening van geboekte posten ongedaan maken en u kunt tegenboekingen of corrigerende boekingen maken.

## <a name="journal-templates-and-batches"></a>Dagboeksjablonen en -batches
Er zijn verschillende sjablonen voor diversendagboeken. Elk dagboeksjabloon wordt vertegenwoordigd door een speciaal venster met specifieke functies en de velden die nodig zijn om die functies te ondersteunen, zoals het venster **Dagboek betalingsreconciliatie**, om bankbetalingen te verwerken en het venster **Betalingsdagboek** om uw leveranciers te betalen.

**Opmerking**: Als u betalingbestanden naar uw bank exporteert vanuit het betalingsdagboek, moet u het selectievakje **Exporteren betaling toestaan** inschakelen voor de dagboekbatch in kwestie in het venster **Fin. dagboekbatches**. Zie voor meer informatie [Procedure: Betalingen naar een bankbestand exporteren](payables-how-export-payments-bank-file.md).

Voor elke dagboeksjabloon kunt u uw eigen persoonlijke dagboek instellen als een dagboekbatch. U kunt bijvoorbeeld uw eigen dagboekbatch definiëren voor het betalingsdagboek dat uw persoonlijke lay-out en instellingen heeft.

Een voorbeeld van een persoonlijke instelling die u in uw diversendagboekbatch kunt definiëren, is dat u het systeem kunt laten helpen om bedragvelden in te vullen. Als u het selectievakje **Salderingsbedrag voorstellen** inschakelt op de regel voor uw batch in het venster **Fin. dagboekbatches**, wordt het veld **Bedrag** op bijvoorbeeld diversendagboekregels voor hetzelfde documentnummer automatisch vooraf ingevuld met de waarde die is vereist om het document sluitend te maken. Zie voor meer informatie [[!INCLUDE[d365fin](includes/d365fin_md.md)] waarden laten voorstellen](ui-let-system-suggest-values.md)

## <a name="main-accounts-and-balancing-accounts"></a>Hoofdrekeningen en tegenrekeningen
Als u standaardtegenrekeningen hebt ingesteld voor de dagboekbatches, wordt de tegenrekening automatisch ingevuld wanneer u **Rekeningnr.** invult. in. Vul anders zowel het veld **Rekeningnr.** als het veld **Tegenrekeningnr.** handmatig in. Een positief bedrag in het veld **Bedrag** wordt gedebiteerd van de hoofdrekening en gecrediteerd naar de tegenrekening. Een negatief bedrag wordt gecrediteerd naar de hoofdrekening en gedebiteerd van de tegenrekening.

**Opmerking**: btw wordt afzonderlijk berekend voor de hoofdrekening en de tegenrekening, zodat er gebruik kan worden gemaakt van verschillende percentages.

## <a name="recurring-journals"></a>Periodieke dagboeken
Een periodiek dagboek is een dagboek met specifieke velden voor het beheer van transacties die u regelmatig boekt met weinig of geen wijzigingen. Met de speciale velden voor periodieke transacties kunt u zowel vaste als variabele bedragen boeken. U kunt ook automatische tegenboekingsposten specificeren op de dag na de boekingsdatum en toewijzingssleutels gebruiken voor de periodieke transacties.

## <a name="see-also"></a>Zie ook
[Procedure: Verdeelsleutels in dagboeken gebruiken](ui-how-use-allocation-keys-general-journals.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

