---
title: Speciale verkoopprijzen en kortingen voor klanten instellen | Microsoft Docs
description: Beschrijft hoe u de alternatieve prijsstelling en kortingsovereenkomsten definieert die u op verkoopdocumenten wilt toepassen tijdens de verkoop aan verschillende klanten.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.date: 07/07/2020
ms.author: sgroespe
ms.openlocfilehash: 16d88ee490b5e9115ed22a12297fcf35b5739984
ms.sourcegitcommit: 8b2f02dd5189c46ecff33c07223ed62b36842d34
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/08/2020
ms.locfileid: "3542629"
---
# <a name="record-special-sales-prices-and-discounts"></a>Speciale verkoopprijzen en kortingen registreren

De verschillende prijs- en kortingsovereenkomsten voor de verkoop aan verschillende klanten moeten zijn vastgesteld zodat de overeengekomen regels en waarden worden toegepast op verkoopdocumenten die u maakt voor de klanten.

Wanneer u speciale prijzen en regelkortingen voor verkopen en inkopen hebt geregistreerd, wordt er in [!INCLUDE[d365fin](includes/d365fin_md.md)] voor gezorgd dat uw winst op artikelhandel altijd optimaal is door de beste prijs op verkoop- en inkoopdocumenten en op project- en artikeldagboekregels automatisch te berekenen. Zie voor meer informatie [De beste prijs berekenen](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

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

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies de gerelateerde koppeling.
2. Open de desbetreffende klantenkaart en kies vervolgens de actie **Prijzen**.

    Op de pagina **Verkoopprijzen** wordt het veld **Verkoopsoort** vooraf ingevuld met **Klant** en wordt het veld **Verkoopscode** vooraf ingevuld met het klantnummer.
3. Vul de velden indien nodig op de regel in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Vul een regel in voor elke combinatie waarmee een speciale verkoopprijs aan de klant wordt verleend.

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Een verkoopregelkorting instellen voor een klant

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies de gerelateerde koppeling.
2. Open de desbetreffende klantenkaart en kies vervolgens de actie **Regelkortingen**.

    Op de pagina **Verkoopregelkortingen** wordt het veld **Verkoopsoort** vooraf ingevuld met **Klant** en wordt het veld **Verkoopscode** vooraf ingevuld met het klantnummer.
3. Vul de velden indien nodig op de regel in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Vul een regel in voor elke combinatie waarmee een speciale verkoopregelkorting aan de klant wordt verleend.

> [!Note]
> Wanneer u de vensters **Verkoopprijzen** en **Verkoopregelkortingen** vanuit een specifieke klant opent, zijn de velden **Verkoopsoortfilter** en **Verkoopcodefilter** ingesteld voor de klant en kunnen deze niet worden gewijzigd of verwijderd, aangegeven door de grijze waarde in het veld **Verkoopcodefilter**.
>
> Als u prijzen of regelkortingen voor alle klanten, een klantprijsgroep of een campagne wilt instellen, moet u de vensters van een artikelkaart openen. Als alternatief kunt u voor verkoopprijzen de pagina **Verkoopprijsvoorstel** gebruiken. Zie voor meer informatie [Artikelprijzen in bulk bijwerken](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Een factuurkorting voor een klant instellen

Wanneer u hebt bepaald welke klanten in aanmerking komen voor factuurkortingen, geeft u de factuurkortingscode op de klantenkaarten op en stelt u de voorwaarden voor elke code in.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies de gerelateerde koppeling.
2. Open de klantenkaart voor een klant die voor factuurkortingen in aanmerking komt.
3. Selecteer in het veld **Factuurkortingscode** een code voor de desbetreffende factuurkortingsvoorwaarden die moeten worden gehanteerd voor het berekenen van factuurkortingen voor de klant.

> [!NOTE]  
> Factuurkortingscodes worden vertegenwoordigd door bestaande klantenkaarten. Zo kunt u snel factuurkortingsvoorwaarden aan klanten toewijzen door de naam van een andere klant te kiezen die dezelfde voorwaarden heeft.

Ga door met het instellen van de nieuwe voorwaarden voor de nieuwe verkoopfactuurkorting.

1. Kies op de pagina **Klantenkaart** de actie **Factuurkortingen**. De pagina **Verkoopfactuurkorting** verschijnt.
2. Geef in het veld **Valutacode** de code op voor een valuta waarvoor de factuurkortingscondities op de regel van toepassing zijn. Laat het veld leeg als u factuurkortingscondities in de lokale valuta wilt instellen.
3. Geef in het veld **Minimumbedrag** op hoe hoog het factuurbedrag minimaal moet zijn voordat een korting wordt berekend.
4. Voer in het veld **Korting %** de factuurkorting in als percentage van het factuurbedrag.
5. Herhaal stap 5 tot en met 7 voor elke valuta waarvoor de klant een andere factuurkorting ontvangt.

De factuurkorting is nu ingesteld en toegewezen aan de klant in kwestie. Wanneer u de klantcode selecteert in het veld **Factuurkortingscode** op andere klantenkaarten, wordt dezelfde factuurkorting toegewezen aan die klanten.

## <a name="to-work-with-sales-invoice-discounts-and-service-charges"></a>Werken met verkoopfactuurkortingen en servicekosten

Wanneer u factuurkortingen gebruikt, wordt op basis van het factuurbedrag bepaald welke korting wordt verleend.  

Op de pagina **Verkoopfactuurkortingen** kunt u ook een bepaald bedrag aan administratiekosten toevoegen aan facturen.  

U kunt factuurkortingen bij verkopen pas gebruiken nadat u bepaalde gegevens hebt opgegeven in de toepassing. U moet bepalen:  

- welke klanten in aanmerking komen voor dit soort korting;  
- welke kortingspercentages u gebruikt.  

Als u factuurkortingen automatisch wilt berekenen, kunt u dit opgeven op de pagina **Verkoopinstellingen**.  

Voor elke klant kunt u opgeven of u factuurkortingen verleent als aan de voorwaarde is voldaan (als dus het factuurbedrag hoog genoeg is). U kunt de voorwaarden voor factuurkortingen definiëren in de lokale valuta voor binnenlandse klanten en in een vreemde valuta voor buitenlandse klanten.  

U koppelt kortingspercentages aan specifieke factuurbedragen op **Verkoopfactuurkortingen**-pagina's. U kunt een willekeurig aantal percentages invoeren op elke pagina. Elke klant kan een eigen pagina hebben, of u kunt verschillende klanten aan dezelfde pagina koppelen.  

Naast (of in plaats van) een kortingspercentage kunt u administratiekosten aan een specifiek factuurbedrag koppelen.  

> [!TIP]  
> Voordat u deze gegevens invoert, kunt u het beste een ontwerp maken van de kortingsstructuur die u wilt gebruiken. Zodoende kunt u gemakkelijker zien welke klanten u kunt koppelen aan dezelfde pagina Factuurkorting. Hoe minder pagina's u hebt ingesteld, des te sneller kunt u de basisgegevens opgeven.

Zie [Kortingen instellen voor uw klanten](/learn/modules/customer-discounts-dynamics-365-business-central/index) op Microsoft Learn voor meer informatie over kortingen bij verkopen.  

## <a name="best-price-calculation"></a>Berekening van beste prijs

Wanneer u speciale prijzen en regelkortingen voor verkopen en inkopen hebt geregistreerd, wordt er in [!INCLUDE[d365fin](includes/d365fin_md.md)] voor gezorgd dat uw winst op artikelhandel altijd optimaal is door de beste prijs op verkoop- en inkoopdocumenten en op project- en artikeldagboekregels automatisch te berekenen.

De beste prijs is de laagst toegestane prijs met de hoogst toegestane regelkorting op een bepaalde datum. In [!INCLUDE[d365fin](includes/d365fin_md.md)] wordt dit automatisch berekend wanneer de eenheidsprijs en het regelkortingspercentage voor artikelen op nieuwe document- en dagboekregels worden ingevoegd.

> [!NOTE]  
> Hierna wordt beschreven hoe de beste prijs voor verkoop wordt berekend. De berekening is hetzelfde voor inkopen.

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

Als u verkoopprijzen wilt kopiëren, zoals de verkoopprijzen van een individuele klant naar een klantenprijsgroep, moet u de batchverwerking **Verkoopprijsvoorstellen maken** uitvoeren, die u start vanaf de pagina **Verkoopprijsvoorstel**.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopprijsvoorstel** in en kies de desbetreffende koppeling.  
2. Kies de actie **Verkoopprijsvoorstellen maken** .  
3. Vul op het sneltabblad **Verkoopprijzen** in de velden **Verkoopsoort** en **Verkoopcode** de waarden in van de oorspronkelijke verkoopprijzen die u wilt kopiëren.  
4. Vul in het bovenste gedeelte van de aanvraagpagina de velden **Verkoopsoort** en **Verkoopcode** in met het type en de naam waarnaar u de verkoopprijzen wilt kopiëren.  
5. Als u nieuwe prijzen wilt maken met de batchverwerking, schakelt u het selectievakje **Nieuwe prijzen maken** in.  
6. Kies de knop **OK** om de regels op de pagina **Verkoopprijsvoorstel** in te vullen met de voorgestelde nieuwe prijzen. Hiermee geeft u aan dat deze prijzen geldig zijn voor de geselecteerde Verkoopsoort.  

> [!NOTE]  
> Met deze batchverwerking worden alleen suggesties gemaakt en worden de voorgestelde wijzigingen niet geïmplementeerd. Als u tevreden bent met de suggesties en deze wilt implementeren (invoegen op de pagina **Verkoopprijzen**), kiest u de actie **Prijsaanpassing doorvoeren** op de pagina **Verkoopprijsvoorstel**.

## <a name="to-bulk-update-item-prices"></a>Artikelprijzen bulksgewijs bijwerken

Als u artikelprijzen bulksgewijs wilt bijwerken, bijvoorbeeld alle artikelprijzen met een bepaald percentage wilt verhogen, moet u de batchverwerking **Artikelprijsvoorstellen maken** uitvoeren. U vindt een koppeling voor de batchverwerking op de pagina **Verkoopprijsvoorstel**.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopprijsvoorstel** in en kies de desbetreffende koppeling.  
2. Kies de actie **Artikelprijsvoorstellen maken** .  
3. Voer op het sneltabblad **Artikel** het veld **Nr.** of **Voorraadboekingsgroep** of overige velden in met de oorspronkelijke artikelprijzen die u wilt bijwerken.  
4. Gebruik in het bovenste gedeelte van de aanvraagpagina de velden **Verkoopsoort** en **Verkoopcode** om aan te geven waarnaar u de verkoopprijzen wilt kopiëren.
5. Als u de batchverwerking automatisch voorgestelde artikelprijzen wilt laten aanpassen, voert u in het veld **Herwaarderingsfactor** de herwaardering in. Typ bijvoorbeeld 1,15 in het veld **Herwaarderingsfactor** voor een 15%-toename van de artikelprijs.  
6. Als u nieuwe prijzen wilt maken met de batchverwerking, schakelt u het selectievakje **Nieuwe prijzen maken** in.  
7. Kies de knop **OK** om de nieuwe prijsvoorstellen in te vullen op de pagina **Verkoopprijsvoorstel**. Hiermee geeft u aan dat deze prijzen geldig zijn voor het geselecteerde **Artikel**.  

> [!NOTE]
> Met deze batchverwerking worden alleen suggesties gemaakt en worden de voorgestelde wijzigingen niet geïmplementeerd. Als u de voorstellen wilt toepassen, voegt u de gegevens in de tabel **Verkoopprijzen** in. Hiervoor kunt u de batchverwerking **Prijsaanpassing doorvoeren** gebruiken onder **Acties**, in de groep **Functies** op de pagina **Verkoopprijsvoorstel**.

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/manage-sales-prices-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Verkopen instellen](sales-setup-sales.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
