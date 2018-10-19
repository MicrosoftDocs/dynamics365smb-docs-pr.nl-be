---
title: Speciale en alternatieve leveranciersprijzen en -kortingen instellen | Microsoft Docs
description: "U kunt verschillende alternatieve prijzen en kortingen definiëren en deze toepassen op inkoopdocumenten voor leveranciers."
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: ea247c762749c108ede8679bb622f71d2dd67f51
ms.contentlocale: nl-be
ms.lasthandoff: 09/28/2018

---
# <a name="record-special-purchase-prices-and-discounts"></a>Speciale inkoopprijzen en kortingen registreren
De verschillende prijs- en kortingsovereenkomsten die van toepassing zijn wanneer u koopt van verschillende leveranciers, moeten worden gedefinieerd, zodat de overeengekomen regels en waarden worden toegepast op documenten die u voor de leveranciers maakt.

Wanneer u speciale prijzen en regelkortingen voor verkopen en inkopen hebt geregistreerd, wordt er in [!INCLUDE[d365fin](includes/d365fin_md.md)] voor gezorgd dat uw winst op artikelhandel altijd optimaal is door de beste prijs op verkoop- en inkoopdocumenten en op project- en artikeldagboekregels automatisch te berekenen. Zie voor meer informatie de sectie "De beste prijs berekenen".

U kunt een speciale inkoopprijs op inkoopregels laten invoegen als een bepaalde combinatie bestaat van leverancier, artikel, minimumaantal, maateenheid of begin- en einddatum.

U kunt twee soorten inkoopkortingen instellen en gebruiken:

| Type korting | Omschrijving |
| --- | --- |
| **Inkoopregelkorting** |Een kortingsbedrag dat op inkoopregels wordt ingevoegd als een bepaalde combinatie bestaat van leverancier, artikel, minimumaantal, maateenheid of begin- en einddatum. Dit werkt op dezelfde manier als bij inkoopprijzen. |
| **Factuurkorting** |Een percentagekorting die van het documenttotaal wordt afgetrokken als het waardebedrag van alle regels in een inkoopdocument een bepaald minimum overschrijdt. |

Omdat inkoopregelkortingen en inkoopprijzen gebaseerd zijn op een combinatie van artikel en leverancier, kunt u deze configuratie ook invoeren vanuit de artikelkaart, waarop de regels en waarden zijn gedefinieerd. Zie voor meer informatie [Nieuwe artikelen registreren](inventory-how-register-new-items.md).

## <a name="to-set-up-a-special-purchase-price-for-a-vendor"></a>Een speciale inkoopprijs voor een leverancier instellen
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Leveranciers** in en kies vervolgens de gerelateerde koppeling.
2. Open de desbetreffende leverancierskaart en kies vervolgens de actie **Prijzen**.

    Het veld **Soort inkoop** wordt vooraf ingevuld met **Leverancier** en het veld **Inkoopcode** wordt vooraf ingevuld met het leveranciersnummer.
3. Vul de velden indien nodig op de regel in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vul een regel in voor elke combinatie waarvoor de leverancier u een inkoopregelkorting verleent.

## <a name="to-set-up-a-line-discount-for-a-vendor"></a>Een speciale regelkorting voor een leverancier instellen
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Leveranciers** in en kies vervolgens de gerelateerde koppeling.
2. Open de desbetreffende leverancierskaart en kies vervolgens de actie **Regelkortingen**.

    Het veld **Soort inkoop** wordt vooraf ingevuld met **Leverancier** en het veld **Inkoopcode** wordt vooraf ingevuld met het leveranciersnummer.
3. Vul de velden indien nodig op de regel in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Vul een regel in voor elke combinatie waarvoor de leverancier u een inkoopregelkorting verleent.

## <a name="to-set-up-an-invoice-discount-for-a-vendor"></a>Een factuurkorting voor een leverancier instellen
Wanneer uw leveranciers u hebben geïnformeerd welke factuurkortingen ze verlenen, voert u de factuurkortingscodes op de leverancierskaarten in en stelt u de condities voor elke code in.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Leveranciers** in en kies vervolgens de gerelateerde koppeling.
2. Open de leverancierskaart voor een leverancier die voor factuurkortingen in aanmerking komt.
3. Selecteer in het veld **Factuurkortingscode** een code voor de desbetreffende factuurkortingscondities om te gebruiken voor het berekenen van factuurkortingen voor de leverancier.

    > [!NOTE]  
    >   Factuurkortingscodes worden weergegeven door bestaande leverancierskaarten. Zo kunt u snel factuurkortingscondities aan leveranciers toewijzen door de naam van een andere leverancier te kiezen die dezelfde condities heeft.

    Ga door met het instellen van de condities voor de nieuwe inkoopfactuurkorting.
4. Kies in het venster **Leverancierskaart** de actie **Factuurkortingen**. Het venster **Inkoopfactuurkortingen** verschijnt.
5. Geef in het veld **Valutacode** de code op voor een valuta waarvoor de factuurkortingscondities op de regel van toepassing zijn. Laat het veld leeg als u factuurkortingscondities in de lokale valuta wilt instellen.
6. Geef in het veld **Minimumbedrag** op hoe hoog het factuurbedrag minimaal moet zijn voordat een korting wordt berekend.
7. Voer in het veld **Korting %** de factuurkorting in als percentage van het factuurbedrag.
8. Herhaal stap 5 tot en met 7 voor elke valuta waarvoor de leverancier een andere factuurkorting ontvangt.

De factuurkorting is nu ingesteld en toegewezen aan de leverancier in kwestie. Wanneer u de leveranciercode selecteert in het veld **Factuurkortingscode** op andere leverancierskaarten, wordt dezelfde factuurkorting toegewezen aan die leverancier.

## <a name="to-choose-a-principle-for-posting-purchase-discounts"></a>Een methode voor het boeken van inkoopkortingen kiezen  
Wanneer u een inkoopfactuur boekt die een of meer kortingen bevat, kunt u de kortingsbedragen op twee manieren boeken. U kunt kortingen apart boeken of kortingen van factuurbedragen aftrekken.  

Voordat u dit kunt doen, moet u de benodigde rekeningen voor het boeken van kortingsbedragen in het rekeningschema al hebben ingesteld. U moet ook controleren of u de juiste rekeningnummers hebt ingevoerd in de boekingsgroepinstellingen in de velden **Inkoopregelkortingsrekening** en **Inkoopfactuurkortingsrekening**.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Kies in het veld **Korting boeken** een van de volgende principes voor het boeken van kortingen.

|**Korting boeken**|**Factuurkorting**|**Regelkorting**|  
|------------------------------------|--------------------------|-----------------------|  
|**Alle**|Afzonderlijk geboekt|Afzonderlijk geboekt|  
|**Factuurkorting**|Afzonderlijk geboekt|Ervan afgetrokken|  
|**Regelkorting**|Ervan afgetrokken|Afzonderlijk geboekt|  
|**Geen kortingen**|Ervan afgetrokken|Ervan afgetrokken|  

## <a name="purchase-invoice-discounts-and-service-charges"></a>Inkoopfactuurkortingen en administratiekosten
Als u vaste afspraken met leveranciers hebt over kwantumkortingen, kunt u voor deze leveranciers de kortingsvoorwaarden invoeren. In dat geval wordt de korting berekend wanneer u een inkoopfactuur invult.  

 Voordat u factuurkortingen voor inkoop kunt gebruiken, moet u aangeven van welke leveranciers u de kortingen ontvangt.  

 U koppelt kortingspercentages aan specifieke factuurbedragen in het venster **Inkoopfactuurkortingen**. U kunt een willekeurig aantal percentages invoeren in elk venster. U kunt voor elke leverancier een eigen venster hebben, of u kunt verschillende leveranciers aan hetzelfde venster koppelen.  

 Naast een kortingspercentage kunt u een bedrag voor administratiekosten aan een specifiek factuurbedrag koppelen.  

 U kunt de condities voor de factuurkorting definiëren in de lokale valuta voor binnenlandse leveranciers en in vreemde valuta's voor buitenlandse leveranciers.  

 U kunt aangeven dat de factuurkortingen automatisch door [!INCLUDE[d365fin](includes/d365fin_md.md)] moeten worden berekend voor offertes, raamcontracten, orders, facturen of creditnota's.  

> [!TIP]  
>  Voordat u deze gegevens invoert, kunt u het beste een ontwerp maken van de kortingsstructuur die u wilt gebruiken. Zo ziet u vrijwel meteen welke leveranciers aan hetzelfde factuurkortingsvenster kunnen worden gekoppeld. Hoe minder vensters u hebt ingesteld, des te sneller kunt u de basisgegevens invoeren.

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
    - Is er een valutavereiste in de prijs-/kortingsafspraak waaraan wordt voldaan? Zo ja, dan worden de laagste prijs en de hoogste regelkorting voor deze valuta ingevoegd, zelfs als de lokale valuta een betere prijs geeft. Als er geen prijs-/kortingsafspraak voor de opgegeven valutacode is, worden in [!INCLUDE[d365fin](includes/d365fin_md.md)] de laagste prijs en de hoogste regelkorting in lokale valuta ingevoegd.

Als er geen speciale prijs kan worden berekend voor het artikel op de regel, worden de laatste directe kosten of de eenheidsprijs van de artikelkaart ingevoegd.

## <a name="see-also"></a>Zie ook
[Inkoop instellen](purchasing-setup-purchasing.md)  
[Inkoop](purchasing-manage-purchasing.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

