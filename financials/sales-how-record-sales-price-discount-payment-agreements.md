---
title: Speciale verkoopprijzen en kortingen voor klanten instellen | Microsoft Docs
description: Beschrijft hoe u de alternatieve prijsstelling en kortingsovereenkomsten definieert die u op verkoopdocumenten wilt toepassen tijdens de verkoop aan verschillende klanten.
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e6e662ee13db1f9002e1c3e74a0d15e2aa2e2a98
ms.openlocfilehash: a130d946a7efa1d49584d4756fe6cd622c409827
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="record-special-sales-prices-and-discounts"></a>Speciale verkoopprijzen en kortingen registreren
De verschillende prijs- en kortingsovereenkomsten voor de verkoop aan verschillende klanten moeten zijn vastgesteld zodat de overeengekomen regels en waarden worden toegepast op verkoopdocumenten die u maakt voor de klanten.

Wanneer u speciale prijzen en regelkortingen voor verkopen en inkopen hebt geregistreerd, wordt er in [!INCLUDE[d365fin](includes/d365fin_md.md)] voor gezorgd dat uw winst op artikelhandel altijd optimaal is door de beste prijs op verkoop- en inkoopdocumenten en op project- en artikeldagboekregels automatisch te berekenen. Zie voor meer informatie de sectie 'De beste prijs berekenen'.

U kunt een speciale verkoopprijs op verkoopregels laten invoegen als een bepaalde combinatie bestaat van klant, artikel, minimumaantal, maateenheid of begin- en einddatum.

U kunt twee soorten verkoopkortingen instellen en gebruiken:

| Type korting | Omschrijving |
| --- | --- |
| **Verkoopregelkorting** |Een kortingsbedrag dat op verkoopregels wordt ingevoegd als een bepaalde combinatie bestaat van klant, artikel, minimumaantal, maateenheid of begin- en einddatum. Dit werkt op dezelfde manier als bij verkoopprijzen. |
| **Factuurkorting** |Een percentagekorting die van het documenttotaal wordt afgetrokken als het waardebedrag van alle regels in een verkoopdocument een bepaald minimum overschrijdt. |

Doordat verkoopprijzen en verkoopregelkortingen worden gebaseerd op een combinatie van artikel en klant, kunt u dit ook configureren vanaf de artikelkaart van het artikel waarop de regels en waarden van toepassing zijn.

> [!NOTE]  
> Als u niet wilt dat een artikel ooit met korting wordt verkocht, laat u kortingsvelden op de artikelkaart leeg en neemt u het artikel niet op in instellingen van regelkorting.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Een verkoopprijs voor een klant instellen
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Klanten** in en klik vervolgens op de gerelateerde koppeling.
2. Open de desbetreffende klantenkaart en kies vervolgens de actie **Prijzen**.

    Het veld **Verkoopsoort** wordt vooraf ingevuld met de waarde **Klant** en het veld **Verkoopcode** wordt vooraf ingevuld met het klantnummer.
3. Vul de velden indien nodig op de regel in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Vul een regel in voor elke combinatie waarmee een speciale verkoopprijs aan de klant wordt verleend.

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Een verkoopregelkorting instellen voor een klant
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Klanten** in en klik vervolgens op de gerelateerde koppeling.
2. Open de desbetreffende klantenkaart en kies vervolgens de actie **Regelkortingen**.

    Het veld **Verkoopsoort** wordt vooraf ingevuld met de waarde **Klant** en het veld **Verkoopcode** wordt vooraf ingevuld met het klantnummer.
3. Vul de velden indien nodig op de regel in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Vul een regel in voor elke combinatie waarmee een speciale verkoopregelkorting aan de klant wordt verleend.

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Een factuurkorting voor een klant instellen
Wanneer u hebt bepaald welke klanten in aanmerking komen voor factuurkortingen, geeft u de factuurkortingscode op de klantenkaarten op en stelt u de voorwaarden voor elke code in.

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Klanten** in en klik vervolgens op de gerelateerde koppeling.
2. Open de klantenkaart voor een klant die voor factuurkortingen in aanmerking komt.
3. Selecteer in het veld **Factuurkortingscode** een code voor de desbetreffende factuurkortingsvoorwaarden die moeten worden gehanteerd voor het berekenen van factuurkortingen voor de klant.

> [!NOTE]  
>   Factuurkortingscodes worden vertegenwoordigd door bestaande klantenkaarten. Zo kunt u snel factuurkortingsvoorwaarden aan klanten toewijzen door de naam van een andere klant te kiezen die dezelfde voorwaarden heeft.

    Proceed to set up new the sales invoice discount terms.
4. Kies in het venster **Klantenkaart** de actie **Factuurkortingen**. Het venster **Verkoopfactuurkorting** verschijnt.
5. Geef in het veld **Valutacode** de code op voor een valuta waarvoor de factuurkortingscondities op de regel van toepassing zijn. Laat het veld leeg als u factuurkortingscondities in de lokale valuta wilt instellen.
6. Geef in het veld **Minimumbedrag** op hoe hoog het factuurbedrag minimaal moet zijn voordat een korting wordt berekend.
7. Voer in het veld **Korting %** de factuurkorting in als percentage van het factuurbedrag.
8. Herhaal stap 5 tot en met 7 voor elke valuta waarvoor de klant een andere factuurkorting ontvangt.

De factuurkorting is nu ingesteld en toegewezen aan de klant in kwestie. Wanneer u de klantcode selecteert in het veld **Factuurkortingscode** op andere klantenkaarten, wordt dezelfde factuurkorting toegewezen aan die klanten.

## <a name="to-work-with-sales-invoice-discounts-and-service-charges"></a>Werken met verkoopfactuurkortingen en servicekosten
Wanneer u factuurkortingen gebruikt, wordt op basis van het factuurbedrag bepaald welke korting wordt verleend.  

In het venster **Verkoopfactuurkorting** kunt u ook een bepaald bedrag aan administratiekosten toevoegen aan facturen.  

U kunt factuurkortingen bij verkopen pas gebruiken nadat u bepaalde gegevens hebt opgegeven. U moet bepalen:  

- welke klanten in aanmerking komen voor dit soort korting;  
- welke kortingspercentages u gebruikt.  

Als u factuurkortingen automatisch wilt berekenen, kunt u dit opgeven in het venster **Verkoopinstellingen**.  

Voor elke klant kunt u opgeven of u factuurkortingen verleent als aan de voorwaarde is voldaan (als dus het factuurbedrag hoog genoeg is). U kunt de voorwaarden voor factuurkortingen definiëren in de lokale valuta voor binnenlandse klanten en in een vreemde valuta voor buitenlandse klanten.  

U koppelt kortingspercentages aan specifieke factuurbedragen in **Verkoopfactuurkortingen**-vensters. U kunt een willekeurig aantal percentages invoeren in elk venster. Elke klant kan een eigen venster hebben, of u kunt verschillende klanten aan hetzelfde venster koppelen.  

Naast (of in plaats van) een kortingspercentage kunt u administratiekosten aan een specifiek factuurbedrag koppelen.  

> [!TIP]  
>  Voordat u deze gegevens opgeeft, kunt u het beste een ontwerp maken van de kortingsstructuur die u wilt gebruiken. Zodoende kunt u gemakkelijker zien welke klanten u kunt koppelen aan hetzelfde venster Factuurkorting. Hoe minder vensters u hebt ingesteld, des te sneller kunt u de basisgegevens opgeven.  

## <a name="best-price-calculation"></a>Berekening van beste prijs
Wanneer u speciale prijzen en regelkortingen voor verkopen en inkopen hebt geregistreerd, wordt er in [!INCLUDE[d365fin](includes/d365fin_md.md)] voor gezorgd dat uw winst op artikelhandel altijd optimaal is door de beste prijs op verkoop- en inkoopdocumenten en op project- en artikeldagboekregels automatisch te berekenen.

De beste prijs is de laagst toegestane prijs met de hoogst toegestane regelkorting op een bepaalde datum. In [!INCLUDE[d365fin](includes/d365fin_md.md)] wordt dit automatisch berekend wanneer de eenheidsprijs en het regelkortingspercentage voor artikelen op nieuwe document- en dagboekregels worden ingevoegd.

> [!NOTE]  
>   Hierna wordt beschreven hoe de beste prijs voor verkoop wordt berekend. De berekening is hetzelfde voor inkopen.

1. In [!INCLUDE[d365fin](includes/d365fin_md.md)] wordt de combinatie van de factuurklant en het artikel gecontroleerd en vervolgens worden de eenheidsprijs en het regelkortingspercentage die van toepassing zijn berekend op basis van de volgende criteria:

    - Is er een prijs-/kortingsafspraak voor de klant of behoort de klant tot een groep waarvoor een dergelijke afspraak geldt?
    - Zijn er dergelijke prijs-/kortingsafspraken van toepassing op het artikel of de artikelkortingsgroep op de regel?
    - Valt de besteldatum (of de boekingsdatum van de factuur en creditnota) binnen de begin- en einddatum van de prijs-/kortingsafspraak?
    - Is er een eenheidscode opgegeven? In dat geval controleert [!INCLUDE[d365fin](includes/d365fin_md.md)] op prijzen/kortingen met dezelfde eenheidscode en op prijzen/kortingen zonder eenheidscode.

2. [!INCLUDE[d365fin](includes/d365fin_md.md)] controleert of eventuele prijs-/kortingsafspraken van toepassing zijn op gegevens in het document of de dagboekregel, en voegt vervolgens de betreffende eenheidsprijs en het regelkortingspercentage in op basis van de volgende criteria:

    - Is er een minimale hoeveelheidsvereiste in de prijs-/kortingsafspraak waaraan wordt voldaan?
    - Is er een valutavereiste in de prijs-/kortingsafspraak waaraan wordt voldaan? Zo ja, dan worden de laagste prijs en de hoogste regelkorting voor deze valuta ingevoegd, zelfs als de lokale valuta een betere prijs oplevert. Als er geen prijs-/kortingsafspraak voor de opgegeven valutacode is, worden in [!INCLUDE[d365fin](includes/d365fin_md.md)] de laagste prijs en de hoogste regelkorting in lokale valuta ingevoegd.

Als er geen speciale prijs kan worden berekend voor het artikel op de regel, worden de laatste directe kosten of de eenheidsprijs van de artikelkaart ingevoegd.

## <a name="to-copy-sales-prices"></a>Verkoopprijzen kopiëren  
Als u verkoopprijzen wilt kopiëren, zoals de verkoopprijzen van een individuele klant naar een klantenprijsgroep, moet u de batchverwerking **Verkoopprijsvoorstellen maken**  batchverwerking. U vindt de batchverwerking in het venster **Verkoopprijsvoorstel**.    

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Verkoopprijsvoorstel** in en klik vervolgens op de gerelateerde koppeling.  
2.  Kies de actie **Verkoopprijsvoorstellen maken** .  
3.  Vul op het sneltabblad **Verkoopprijzen** in de velden **Verkoopsoort** en **Verkoopcode** de waarden in van de oorspronkelijke verkoopprijzen die u wilt kopiëren.  
4.  Gebruik in het bovenste gedeelte van het aanvraagvenster de velden **Verkoopsoort** en **Verkoopcode** om aan te geven waarnaar u de verkoopprijzen wilt kopiëren.  
5.  Als u nieuwe prijzen wilt maken met de batchverwerking, schakelt u het selectievakje **Nieuwe prijzen maken** in.  
6.  Klik op **OK** om de nieuwe prijsvoorstellen in te vullen in het venster **Verkoopprijsvoorstel**. Hiermee geeft u aan dat deze prijzen geldig zijn voor de geselecteerde **Verkoopsoort**.  

> [!NOTE]  
>  Met deze batchverwerking worden alleen suggesties gemaakt en worden de voorgestelde wijzigingen niet geïmplementeerd. Als u de voorstellen wilt toepassen, voegt u de gegevens in de tabel **Verkoopprijzen** in. Hiervoor kunt u de batchverwerking **Prijsaanpassing doorvoeren** gebruiken onder **Acties**, in de groep **Functies** in het venster **Verkoopprijsvoorstel**.

## <a name="see-also"></a>Zie ook
[Verkopen instellen](sales-setup-sales.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

