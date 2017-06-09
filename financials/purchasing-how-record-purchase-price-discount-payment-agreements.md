---
title: 'Procedure: Speciale inkoopprijzen en kortingen registreren | Microsoft Docs'
description: 'Procedure: Inkoopprijzen en kortingen registreren'
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 67625231d62a72bb0a62ab362bce92aa16b8956e
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-record-special-purchase-prices-and-discounts"></a>Procedure: Speciale inkoopprijzen en kortingen registreren
De verschillende prijs- en kortingsovereenkomsten die van toepassing zijn wanneer u koopt van verschillende leveranciers, moeten worden gedefinieerd, zodat de overeengekomen regels en waarden worden toegepast op documenten die u voor de leveranciers maakt.

Wanneer u speciale prijzen en regelkortingen voor verkopen en inkopen hebt geregistreerd, wordt er in [!INCLUDE[d365fin](includes/d365fin_md.md)] voor gezorgd dat uw winst op artikelhandel altijd optimaal is door de beste prijs op verkoop- en inkoopdocumenten en op project- en artikeldagboekregels automatisch te berekenen. Zie voor meer informatie [Geavanceerd: De beste prijs berekenen](advanced-best-price-calculation.md).

U kunt een speciale inkoopprijs op inkoopregels laten invoegen als een bepaalde combinatie bestaat van leverancier, artikel, minimumaantal, maateenheid of begin- en einddatum.

U kunt twee soorten inkoopkortingen instellen en gebruiken:

| Type korting | Omschrijving |
| --- | --- |
| **Inkoopregelkorting** |Een kortingsbedrag dat op inkoopregels wordt ingevoegd als een bepaalde combinatie bestaat van leverancier, artikel, minimumaantal, maateenheid of begin- en einddatum. Dit werkt op dezelfde manier als bij inkoopprijzen. |
| **Factuurkorting** |Een percentagekorting die van het documenttotaal wordt afgetrokken als het waardebedrag van alle regels in een inkoopdocument een bepaald minimum overschrijdt. |

Omdat inkoopregelkortingen en inkoopprijzen gebaseerd zijn op een combinatie van artikel en leverancier, kunt u deze configuratie ook invoeren vanuit de artikelkaart, waarop de regels en waarden zijn gedefinieerd. Zie [Procedure: Nieuwe artikelen registreren](inventory-how-register-new-items.md) voor meer informatie.

## <a name="to-set-up-a-special-purchase-price-for-a-vendor"></a>Een speciale inkoopprijs voor een leverancier instellen
1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Leveranciers** in en kies vervolgens de gerelateerde koppeling.
2. Open de desbetreffende leverancierskaart en kies vervolgens de actie **Prijzen**.

    Het veld **Soort inkoop** wordt vooraf ingevuld met **Leverancier** en het veld **Inkoopcode** wordt vooraf ingevuld met het leveranciersnummer.
3. Vul de velden indien nodig op de regel in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vul een regel in voor elke combinatie waarvoor de leverancier u een inkoopregelkorting verleent.

## <a name="to-set-up-a-line-discount-for-a-vendor"></a>Een speciale regelkorting voor een leverancier instellen
1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Leveranciers** in en kies vervolgens de gerelateerde koppeling.
2. Open de desbetreffende leverancierskaart en kies vervolgens de actie **Regelkortingen**.

    Het veld **Soort inkoop** wordt vooraf ingevuld met **Leverancier** en het veld **Inkoopcode** wordt vooraf ingevuld met het leveranciersnummer.
3. Vul de velden indien nodig op de regel in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vul een regel in voor elke combinatie waarvoor de leverancier u een inkoopregelkorting verleent.

## <a name="to-set-up-an-invoice-discount-for-a-vendor"></a>Een factuurkorting voor een leverancier instellen
Wanneer uw leveranciers u hebben geïnformeerd welke factuurkortingen ze verlenen, voert u de factuurkortingscodes op de leverancierskaarten in en stelt u de condities voor elke code in.

1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Leveranciers** in en kies vervolgens de gerelateerde koppeling.
2. Open de leverancierskaart voor een leverancier die voor factuurkortingen in aanmerking komt.
3. Selecteer in het veld **Factuurkortingscode** een code voor de desbetreffende factuurkortingscondities om te gebruiken voor het berekenen van factuurkortingen voor de leverancier.

    **Opmerking**: factuurkortingscodes worden weergegeven door bestaande leverancierskaarten. Zo kunt u snel factuurkortingscondities aan leveranciers toewijzen door de naam van een andere leverancier te kiezen die dezelfde condities heeft.

    Ga door met het instellen van de condities voor de nieuwe inkoopfactuurkorting.
4. Kies in het venster **Leverancierskaart** de actie **Factuurkortingen**. Het venster **Inkoopfactuurkortingen** verschijnt.
5. Geef in het veld **Valutacode** de code op voor een valuta waarvoor de factuurkortingscondities op de regel van toepassing zijn. Laat het veld leeg als u factuurkortingscondities in de lokale valuta wilt instellen.
6. Geef in het veld **Minimumbedrag** op hoe hoog het factuurbedrag minimaal moet zijn voordat een korting wordt berekend.
7. Voer in het veld **Korting %** de factuurkorting in als percentage van het factuurbedrag.
8. Herhaal stap 5 tot en met 7 voor elke valuta waarvoor de leverancier een andere factuurkorting ontvangt.

De factuurkorting is nu ingesteld en toegewezen aan de leverancier in kwestie. Wanneer u de leveranciercode selecteert in het veld **Factuurkortingscode** op andere leverancierskaarten, wordt dezelfde factuurkorting toegewezen aan die leverancier.

## <a name="see-also"></a>Zie ook
[Geavanceerd: De beste prijs berekenen](advanced-best-price-calculation.md)  
[Inkoop instellen](purchasing-setup-purchasing.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

