---
title: 'Procedure: Speciale verkoopprijzen en kortingen registreren | Microsoft Docs'
description: 'Procedure: Speciale verkoopprijzen en kortingen registreren'
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
ms.openlocfilehash: 5ceddded2f95e15a6a7449bf2776b7776ce8a55c
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-record-special-sales-prices-and-discounts"></a>Procedure: Speciale verkoopprijzen en kortingen registreren
De verschillende prijs- en kortingsovereenkomsten voor de verkoop aan verschillende klanten moeten zijn vastgesteld zodat de overeengekomen regels en waarden worden toegepast op verkoopdocumenten die u maakt voor de klanten.

Wanneer u speciale prijzen en regelkortingen voor verkopen en inkopen hebt geregistreerd, wordt er in [!INCLUDE[d365fin](includes/d365fin_md.md)] voor gezorgd dat uw winst op artikelhandel altijd optimaal is door de beste prijs op verkoop- en inkoopdocumenten en op project- en artikeldagboekregels automatisch te berekenen. Zie voor meer informatie [Geavanceerd: De beste prijs berekenen](advanced-best-price-calculation.md).

U kunt een speciale verkoopprijs op verkoopregels laten invoegen als een bepaalde combinatie bestaat van klant, artikel, minimumaantal, maateenheid of begin- en einddatum.

U kunt twee soorten verkoopkortingen instellen en gebruiken:

| Type korting | Omschrijving |
| --- | --- |
| **Verkoopregelkorting** |Een kortingsbedrag dat op verkoopregels wordt ingevoegd als een bepaalde combinatie bestaat van klant, artikel, minimumaantal, maateenheid of begin- en einddatum. Dit werkt op dezelfde manier als bij verkoopprijzen. |
| **Factuurkorting** |Een percentagekorting die van het documenttotaal wordt afgetrokken als het waardebedrag van alle regels in een verkoopdocument een bepaald minimum overschrijdt. |

Doordat verkoopprijzen en verkoopregelkortingen worden gebaseerd op een combinatie van artikel en klant, kunt u dit ook configureren vanaf de artikelkaart van het artikel waarop de regels en waarden van toepassing zijn.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Een verkoopprijs voor een klant instellen
1. In de rechterbovenhoek, kies het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Klanten** in en klik op de gerelateerde koppeling.
2. Open de desbetreffende klantenkaart en kies vervolgens de actie **Prijzen**.

    Het veld **Verkoopsoort** wordt vooraf ingevuld met de waarde **Klant** en het veld **Verkoopcode** wordt vooraf ingevuld met het klantnummer.
3. Vul de velden indien nodig op de regel in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Vul een regel in voor elke combinatie waarmee een speciale verkoopprijs aan de klant wordt verleend.

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Een verkoopregelkorting instellen voor een klant
1. In de rechterbovenhoek, kies het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Klanten** in en klik op de gerelateerde koppeling.
2. Open de desbetreffende klantenkaart en kies vervolgens de actie **Regelkortingen**.

    Het veld **Verkoopsoort** wordt vooraf ingevuld met de waarde **Klant** en het veld **Verkoopcode** wordt vooraf ingevuld met het klantnummer.
3. Vul de velden indien nodig op de regel in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Vul een regel in voor elke combinatie waarmee een speciale verkoopregelkorting aan de klant wordt verleend.

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Een factuurkorting voor een klant instellen
Wanneer u hebt bepaald welke klanten in aanmerking komen voor factuurkortingen, geeft u de factuurkortingscode op de klantenkaarten op en stelt u de voorwaarden voor elke code in.

1. In de rechterbovenhoek, kies het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Klanten** in en klik op de gerelateerde koppeling.
2. Open de klantenkaart voor een klant die voor factuurkortingen in aanmerking komt.
3. Selecteer in het veld **Factuurkortingscode** een code voor de desbetreffende factuurkortingsvoorwaarden die moeten worden gehanteerd voor het berekenen van factuurkortingen voor de klant.

    **Opmerking**: factuurkortingscodes worden vertegenwoordigd door bestaande klantenkaarten. Zo kunt u snel factuurkortingsvoorwaarden aan klanten toewijzen door de naam van een andere klant te kiezen die dezelfde voorwaarden heeft.

    Ga door met het instellen van de nieuwe voorwaarden voor de nieuwe verkoopfactuurkorting.
4. Kies in het venster **Klantenkaart** de actie **Factuurkortingen**. Het venster **Verkoopfactuurkorting** verschijnt.
5. Geef in het veld **Valutacode** de code op voor een valuta waarvoor de factuurkortingscondities op de regel van toepassing zijn. Laat het veld leeg als u factuurkortingscondities in de lokale valuta wilt instellen.
6. Geef in het veld **Minimumbedrag** op hoe hoog het factuurbedrag minimaal moet zijn voordat een korting wordt berekend.
7. Voer in het veld **Korting %** de factuurkorting in als percentage van het factuurbedrag.
8. Herhaal stap 5 tot en met 7 voor elke valuta waarvoor de klant een andere factuurkorting ontvangt.

De factuurkorting is nu ingesteld en toegewezen aan de klant in kwestie. Wanneer u de klantcode selecteert in het veld **Factuurkortingscode** op andere klantenkaarten, wordt dezelfde factuurkorting toegewezen aan die klanten.

## <a name="see-also"></a>Zie ook
[Geavanceerd: De beste prijs berekenen](advanced-best-price-calculation.md)  
[Verkopen instellen](sales-setup-sales.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

