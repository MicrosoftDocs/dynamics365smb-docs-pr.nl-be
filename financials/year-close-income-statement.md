---
title: 'Procedure: Afsluiten WenV-rekening | Microsoft Docs'
description: Hierin wordt uitgelegd hoe u een WenV-rekening afsluit.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 03/29/2017
ms.author: jswymer
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: dde7b93c6a3dcf78173494f1c6fa09a38207e676
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="close-income-statement"></a>Afsluiten WenV-rekening
Wanneer een boekjaar is afgelopen, moet u de hierin opgenomen perioden afsluiten. Voer hiervoor de batchverwerking **Afsluiten WenV-rekening** uit. Met deze taak wordt het jaarresultaat overgeboekt naar een rekening op de balans en worden de resultatenrekeningen afgesloten. In een dagboek worden regels gemaakt die u vervolgens kunt boeken.

## <a name="to-run-the-close-income-statement-batch-job"></a>De batchverwerking Afsluiten WenV-rekening uitvoeren
1. Sluit het boekjaar. Het boekjaar moet zijn afgesloten voordat u de batchverwerking kunt uitvoeren. Zie [Procedure: Boekingsperioden afsluiten](year-close-account-periods.md) voor meer informatie.
2. In de rechterbovenhoek, kies het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Afsluiten WenV-rekening** in en klik op de gerelateerde koppeling.
3. Kies **OK** om de batchverwerking te starten.

## <a name="about-the-close-income-statement-batch-job"></a>Informatie over de batchverwerking Afsluiten WenV-rekening
De batchverwerking verwerkt alle grootboekrekeningen van het soort Resultaten en maakt tegenboekingen voor de bijbehorende saldo's. Dat wil zeggen, dat elke post de som is van alle grootboekposten op de rekening van het boekjaar. Deze nieuwe posten worden geplaatst in een dagboek waarin u een tegenrekening en resultatenrekening in de balans moet opgeven voordat u boekt. Wanneer u het dagboek boekt, wordt een post geboekt in elke resultatenrekening zodat het saldo nul wordt en het jaarresultaat tegelijkertijd wordt overgebracht naar de balans.

U moet het dagboek zelf boeken. De batchverwerking boekt de posten niet automatisch, behalve wanneer een extra rapportagevaluta wordt gebruikt. Wanneer een extra rapportagevaluta wordt gebruikt, boekt de batchverwerking posten direct naar het grootboek.

De datum op de regels die tijdens de batchverwerking in het dagboek worden opgenomen, is altijd een ultimodatum voor het boekjaar. De ultimodatum is een fictieve datum tussen de laatste dag van het oude boekjaar en de eerste dag van het nieuwe jaar. Het voordeel van boeken op een ultimodatum is dat u de juiste saldo's behoudt voor de gewone datums van het boekjaar.

U kunt de batchverwerking **Afsluiten WenV-rekening** meerdere keren gebruiken. Als u de batchverwerking opnieuw uitvoert, kunt ook naar vorige boekjaren boeken, zelfs nadat de WenV-rekeningen zijn afgesloten.

## <a name="see-also"></a>Zie ook
[Boeken afsluiten](year-close-books.md)  
[Procedure: de jaareinde-ultimopost boeken](year-how-post-year-end-close-entry.md)  
[Procedure: Nieuw boekjaar openen](finance-how-open-new-fiscal-year.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

