---
title: Verkoopprijzen en kortingen voor klanten instellen | Microsoft Docs
description: Beschrijft hoe u prijs- en kortingsovereenkomsten voor verkoopdocumenten instelt en toepast.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: special price, alternate price, pricing
ms.search.form: 1345, 7002, 7007, 7015, 7016, 7023
ms.date: 04/01/2021
ms.author: bholtorf
ms.openlocfilehash: acba6dc39b57788541a36540f443d02a25bc610c
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/04/2022
ms.locfileid: "8384188"
---
# <a name="record-sales-prices-and-discounts"></a>Verkoopprijzen en kortingen registreren
> [!NOTE]
> In releasewave 2 van 2020 hebben we gestroomlijnde processen uitgebracht voor het instellen en beheren van prijzen en kortingen. Als u een nieuwe klant bent en die versie gebruikt, gebruikt u de nieuwe ervaring. Als u een bestaande klant bent, hangt of u de nieuwe ervaring gebruikt, af van de vraag of uw beheerder de functie-update **Nieuwe verkoopprijservaring** heeft geactiveerd in **Functiebeheer**. Zie voor meer informatie [Aankomende functies van tevoren inschakelen](/dynamics365/business-central/dev-itpro/administration/feature-management).

[!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt verschillende prijsstrategieën, variërend van one-price-fits-all-modellen waarbij een artikel altijd voor dezelfde prijs wordt verkocht, tot speciale prijsafspraken met specifieke klanten, groepen klanten of speciale aanbiedingen wanneer u een verkoopcampagne voert. U kunt bijvoorbeeld onder de volgende voorwaarden een speciale prijs op een verkooporder aanbieden:

* Wanneer het voor een minimale hoeveelheid is
* Het is voor een bepaald type artikel  
* Als het tijdens een bepaalde periode is gemaakt

Om een basisprijsmodel te gebruiken hoeft u alleen een eenheidsprijs op te geven voor een artikel of resource. Die prijs wordt altijd gebruikt op verkoopdocumenten. Voor meer geavanceerde modellen, wanneer u bijvoorbeeld een verkoopcampagne voert en speciale prijzen wilt aanbieden, kunt u daarvoor criteria opgeven op de pagina **Verkoopprijzen**. U kunt speciale prijzen aanbieden op basis van combinaties van: 

* Klant
* Artikel
* Eenheid
* Minimumhoeveelheid
* Datumbereiken die bepalen wanneer de prijzen geldig zijn

Bovendien, nadat u speciale prijzen heeft ingesteld, kan [!INCLUDE[prod_short](includes/prod_short.md)] automatisch de beste prijs berekenen op verkoop- en inkoopdocumenten en op taak- en artikeljournaalregels. Zie voor meer informatie [De beste prijs berekenen](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).  

U kunt voor verkoopkortingen de volgende typen instellen en gebruiken:

| Type korting | Omschrijving |
| --- | --- |
| **Verkoopregelkorting** |Een bedrag dat op verkoopregels wordt gebruikt als een bepaalde combinatie bestaat van klant, artikel, minimumhoeveelheid, eenheid of begin- en einddatum. Deze combinaties werken op dezelfde manier als bij verkoopprijzen. |
| **Factuurkorting** |Een kortingspercentage dat van het verkoopdocumenttotaal wordt afgetrokken als het totaal van alle regels in het document een bepaald minimum overschrijdt. |

> [!TIP]  
> Als u niet wilt dat een artikel ooit met korting wordt verkocht, laat u de kortingsvelden op de artikelpagina leeg en neemt u het artikel niet op in instellingen van regelkorting.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Een verkoopprijs voor een klant instellen

Deze stappen verschillen, afhankelijk van of uw beheerder de functie-update **Nieuwe verkoopprijservaring** heeft geactiveerd. Als de functie-update niet is ingeschakeld, volgt u de stappen op het tabblad Huidige ervaring. 

## <a name="current-experience"></a>[Huidige ervaring](#tab/current-experience)

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies vervolgens de gerelateerde koppeling.
2. Kies de klant en kies vervolgens de actie **Prijzen**.
3. Vul de velden indien nodig op de regel in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Vul een regel in voor elke combinatie waarmee een speciale verkoopprijs aan de klant wordt verleend.

## <a name="new-experience"></a>[Nieuwe ervaring](#tab/new-experience)  
Standaard is de status van nieuwe prijslijsten Concept. Conceptprijslijsten worden niet meegenomen in prijsberekeningen. Als u klaar bent met het toevoegen van regels en u wilt de prijzen gaan gebruiken, wijzigt u de status in Actief.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Klanten** in en kies vervolgens de gerelateerde koppeling.
2. Kies de klant en kies vervolgens de actie **Verkoopprijslijsten**. 
3. Kies **Nieuw** om een nieuwe verkoopprijslijst te maken.
4. Vul indien nodig de velden in op de sneltabbladen **Algemeen** en **Btw**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. U kunt op de volgende manieren artikelen aan de lijst toevoegen:
   * Kies om veel items toe te voegen **Regels voorstellen** en voer vervolgens filtercriteria in om de typen items op te geven die moeten worden toegevoegd. Optioneel kunt u andere instellingen voor de artikelen invoeren. Deze instellingen zijn specifiek voor de prijslijst. U kunt ze later indien nodig wijzigen.
   * Kies om items uit een andere prijslijst te kopiëren **Regels kopiëren** en kies vervolgens de prijslijst die u wilt kopiëren.
   * Als u handmatig artikelen wilt toevoegen, kiest u in het veld **Producttype** op een regel het type product waarvoor de prijslijst bedoeld is. Vul indien nodig de overige velden in, afhankelijk van uw selectie. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Om de prijslijst te gaan gebruiken, kiest u in het veld **Status** **Actief**.  

---

## <a name="using-sales-and-purchase-price-lists"></a>Verkoop- en inkoopprijslijsten gebruiken
> [!NOTE]
> Voor het gebruik van prijslijsten moet uw beheerder de functie-update **Nieuwe verkoopprijservaring** in **Functiebeheer** hebben ingeschakeld. Zie voor meer informatie [Aankomende functies van tevoren inschakelen](/dynamics365/business-central/dev-itpro/administration/feature-management).

De velden **Toepassingstype** en **Toepassingsnr.** laten u kiezen waarop een prijslijst van toepassing is, zoals klant of klantprijsgroep. Gebruik het veld **Kolommen weergeven voor** om kolommen weer te geven of te verbergen die alleen relevant zijn voor prijzen, kortingen of prijzen en kortingen.

### <a name="converting-existing-prices-when-you-turn-on-the-pricing-feature-update"></a>Bestaande prijzen converteren wanneer u de prijsfunctie-update inschakelt
Wanneer u de functie-update **Nieuwe verkoopprijservaring** op de pagina **Functiebeheer** inschakelt, wordt de guide **Gegevensupdatefunctie** geopend. Gebruik de schakelaar **Standaardprijzen gebruiken** als volgt:

* Als u met alle prijzen op één pagina wilt werken, schakelt u deze in. Bestaande prijzen worden geconverteerd naar één standaardprijslijst voor elk van de volgende zaken:

    * Verkoop
    * Inkopen
    * Projectomzet
    * Projectinkopen 

    Daarna kunt u alle prijzen voor deze gebieden bewerken op de pagina **Prijsvoorstel**. De standaardprijslijsten worden ingesteld op de pagina's **Verkoopinstellingen**, **Inkoopinstellingen** en **Projectinstellingen**. 

    > [!NOTE]
    > Als prijzen alleen op artikel- of resourcekaarten worden ingesteld, worden tijdens de gegevensupdate geen standaardprijslijsten met die prijzen ingevuld. U kunt echter elk van de standaardprijslijsten of de pagina Prijsvoorstel openen en de actie **Regels voorstellen** gebruiken om de prijzen toe te voegen die zijn ingesteld op artikel- of resourcekaarten. 

* Schakel dit uit om verkoopprijslijsten te gebruiken. Bestaande prijzen worden omgezet naar een nieuwe prijslijst voor elke combinatie van klant, klantgroep of campagne, en de start- en einddatum en valuta's. Als u veel combinaties hebt, hebt u veel prijslijsten.

Als u de nieuwe prijservaring al hebt ingeschakeld, kunt u handmatig standaardprijslijsten maken of een bestaande prijslijst als standaard opgeven. Om een bestaande prijslijst als standaard in te stellen zet u de schakelaar **Bijwerken van standaardinstellingen toestaan** aan in de prijslijst. Vervolgens stelt u de prijslijst als de standaard in op de pagina **Verkoopinstellingen**, **Inkoopinstellingen** of **Projectinstellingen**.

## <a name="editing-active-price-lists"></a>Actieve prijslijsten bewerken
Om mensen in staat te stellen prijzen te bewerken op actieve prijslijsten voor artikelen, resources, klanten, leveranciers of andere entiteiten die prijzen gebruiken, zet u de schakelaar **Bewerken van actieve prijs toestaan** aan op de pagina **Verkoopinstellingen** en **Inkoopinstellingen**. 

Wanneer de schakelaar **Bewerken van actieve prijs toestaan** is uitgeschakeld, moet u om prijzen in een prijslijst bij te werken, de status van de prijslijst wijzigen in **Concept**, uw wijziging aanbrengen en de prijslijst vervolgens weer activeren.

De pagina **Overzicht van prijzen** geeft een overzicht van alle prijzen over prijslijsten heen. U kunt filters instellen om de lijst te verfijnen. Nadat u de prijzen heeft gewijzigd, moet u de actie **Regels controleren** gebruiken om de prijzen te controleren met andere prijslijstregels. Het verifiëren van de prijzen helpt bijvoorbeeld dubbele of tegenstrijdige prijzen te voorkomen. 

> [!NOTE]
> Wanneer u een regel in een actieve prijslijst bewerkt, wordt de status van de regel Concept en wordt de regel pas in prijsberekeningen opgenomen als u de actie **Regels controleren** gebruikt. Nadat u de prijs heeft geverifieerd, wordt de status van de regel Actief en wordt deze gebruikt in prijsberekeningen.

Om nieuwe prijzen toe te voegen gebruikt u op de pagina **Overzicht van prijzen** de actie **Nieuwe regels toevoegen**. De pagina **Prijsvoorstel** wordt geopend, waar u op de volgende manieren prijsregels toevoegt:

* Door ze voor te stellen op basis van criteria
* Ze kopiëren van andere prijslijsten
* Ze handmatig invoeren. 

Daarna kunt u de actie **Prijswijziging doorvoeren** gebruiken om de nieuwe prijzen te vergelijken met andere prijslijsten om duplicaten te voorkomen.

## <a name="to-copy-sales-prices"></a>Verkoopprijzen kopiëren
Deze stappen verschillen, afhankelijk van of uw beheerder de functie-update **Nieuwe verkoopprijservaring** heeft geactiveerd. Als de functie-update niet is ingeschakeld, volgt u de stappen op het tabblad Huidige ervaring.

## <a name="current-experience"></a>[Huidige ervaring](#tab/current-experience)  

Als u verkoopprijzen wilt kopiëren, bijvoorbeeld om de verkoopprijzen van een individuele klant voor een klantenprijsgroep te gebruiken, moet u de batchverwerking **Verkoopprijsvoorstellen maken**. uitvoeren op de pagina **Verkoopprijsvoorstel**.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopprijsvoorstel** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Verkoopprijsvoorstellen maken** .  
3. Vul op het sneltabblad **Verkoopprijzen** in de velden **Verkoopsoort** en **Verkoopcode** de waarden in van de oorspronkelijke verkoopprijzen die u wilt kopiëren.  
4. Vul in het bovenste gedeelte van de aanvraagpagina de velden **Verkoopsoort** en **Verkoopcode** in met het type en de naam waarnaar u de verkoopprijzen wilt kopiëren.  
5. Als u nieuwe prijzen wilt maken met de batchverwerking, schakelt u het selectievakje **Nieuwe prijzen maken** in.  
6. Kies de knop **OK** om de regels op de pagina **Verkoopprijsvoorstel** in te vullen met de voorgestelde nieuwe prijzen. Hiermee geeft u aan dat deze prijzen geldig zijn voor de geselecteerde Verkoopsoort.  

   > [!NOTE]  
   > Met deze batchverwerking worden alleen suggesties gemaakt en worden de voorgestelde wijzigingen niet geïmplementeerd. Als u tevreden bent met de suggesties en deze wilt implementeren (invoegen op de pagina **Verkoopprijzen**), kiest u de actie **Prijsaanpassing doorvoeren** op de pagina **Verkoopprijsvoorstel**.

## <a name="new-experience"></a>[Nieuwe ervaring](#tab/new-experience)  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopprijslijsten** in en kies vervolgens de gerelateerde koppeling. 
2. Kies de prijslijst die u wilt kopiëren en kies vervolgens **Regels kopiëren**.
3. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > U kunt geen twee regels hebben met dezelfde instellingen maar verschillende prijzen. Als dat gebeurt, wordt er een bericht weergegeven wanneer u een prijslijst activeert. U kunt de te gebruiken prijs kiezen door de lijst te openen en de verkeerde prijs te verwijderen.  
  
---

## <a name="to-bulk-update-item-prices"></a>Artikelprijzen bulksgewijs bijwerken
Deze stappen verschillen, afhankelijk van of uw beheerder de functie-update **Nieuwe verkoopprijservaring** heeft geactiveerd. Als de functie-update niet is ingeschakeld, volgt u de stappen op het tabblad Huidige ervaring.

### <a name="current-experience"></a>[Huidige ervaring](#tab/current-experience)

Als u artikelprijzen in bulk wilt bijwerken, bijvoorbeeld om alle artikelprijzen met een bepaald percentage te verhogen, kunt u het **Verkoopprijsvoorstel** invullen door de volgende batchtaken te gebruiken:

* **Artikelprijsvoorstellen maken** stelt wijzigingen voor door een aanpassingsfactor toe te passen op bestaande verkoopprijzen, of door bestaande verkoopprijsafspraken te kopiëren naar andere klanten, klantprijsgroepen of verkoopcampagnes.
* **Artikelprijsvoorstellen maken** stelt wijzigingen voor door een aanpassingsfactor toe te passen op bestaande eenheidsprijzen op artikelkaarten, of door prijzen voor te stellen voor nieuwe combinaties van valuta, maateenheden, enzovoort. De eenheidsprijzen op artikelen worden niet gewijzigd.    

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopprijsvoorstel** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Artikelprijsvoorstellen maken** .  
3. Voer op het sneltabblad **Artikel** het veld **Nr.** of **Voorraadboekingsgroep** of overige velden in met de oorspronkelijke artikelprijzen die u wilt bijwerken.  
4. Gebruik in het bovenste gedeelte van de aanvraagpagina de velden **Verkoopsoort** en **Verkoopcode** om aan te geven waarnaar u de verkoopprijzen wilt kopiëren.
5. Als u de batchverwerking automatisch voorgestelde artikelprijzen wilt laten aanpassen, voert u in het veld **Herwaarderingsfactor** de herwaardering in. Typ bijvoorbeeld **1,15** in het veld **Herwaarderingsfactor** voor een toename van **15%** van de artikelprijs.  
6. Als u nieuwe prijzen wilt maken met de batchverwerking, zet u de schakelaar **Nieuwe prijzen maken** aan.  
7. Kies **OK** om de regels op de pagina **Verkoopprijsvoorstel** in te vullen met de voorgestelde nieuwe prijzen.
8. Gebruik om de suggesties te implementeren de actie **Prijsaanpassing doorvoeren**. De batchtaak doet suggesties, maar implementeert ze niet.

## <a name="new-experience"></a>[Nieuwe ervaring](#tab/new-experience)

Om prijzen voor meerdere artikelen bij te werken moet u een nieuwe prijslijst maken en vervolgens de regels uit een bestaande prijslijst kopiëren. Wanneer u de regels kopieert, kunt u filters gebruiken om aan te geven wat u wilt kopiëren, en u kunt een geheel getal of decimaal getal specificeren in het veld **Herwaarderingsfactor** om prijzen te verhogen of te verlagen. De status van de prijslijst moet **Concept** zijn. Indien nodig kunt u vervolgens de oude prijslijst deactiveren.

> [!NOTE]
> U kunt geen twee regels hebben met dezelfde instellingen maar verschillende prijzen. Als dat gebeurt, wordt er een bericht weergegeven wanneer u een prijslijst activeert. U kunt de te gebruiken prijs kiezen door de lijst te openen en de verkeerde prijs te verwijderen.  

---

## <a name="sales-invoice-discounts-and-service-charges"></a>Verkoopfactuurkortingen en administratiekosten
Wanneer u factuurkortingen gebruikt, wordt op basis van het totale bedrag op de factuur bepaald welke korting wordt verleend. Op de pagina **Verkoopfactuurkortingen** kunt u ook een bepaald bedrag aan administratiekosten toevoegen aan facturen.  

Als u factuurkortingen automatisch wilt berekenen, kunt u op de pagina **Verkoopinstellingen** de schakelaar **Factuurkorting berekenen** inschakelen.  

Voor elke klant kunt u opgeven of u factuurkortingen wilt aanbieden als aan de criteria wordt voldaan. Bijvoorbeeld als het factuurbedrag groot genoeg is. U kunt de voorwaarden voor factuurkortingen definiëren in de lokale valuta voor binnenlandse klanten en in een vreemde valuta voor buitenlandse klanten.  

U koppelt kortingspercentages aan specifieke factuurbedragen op de pagina **Verkoopfactuurkortingen** voor elke klant. U kunt elk aantal percentages invoeren. Elke klant kan een eigen pagina hebben of u kunt verschillende klanten aan dezelfde pagina koppelen.  

Naast (of in plaats van) een kortingspercentage kunt u administratiekosten aan een specifiek factuurbedrag koppelen.  

Zie [Kortingen instellen voor uw klanten](/learn/modules/customer-discounts-dynamics-365-business-central/index) op Microsoft Learn voor training in kortingen.  

### <a name="calculating-invoice-discounts-on-sales"></a>Factuurkortingen op verkopen berekenen

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Een verkoopregelkorting instellen voor een klant
Deze stappen verschillen, afhankelijk van of uw beheerder de functie-update **Nieuwe verkoopprijservaring** heeft geactiveerd. Als de functie-update niet is ingeschakeld, volgt u de stappen op het tabblad Huidige ervaring.

## <a name="current-experience"></a>[Huidige ervaring](#tab/current-experience)  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies de gerelateerde koppeling.
2. Open de desbetreffende klantenkaart en kies vervolgens de actie **Regelkortingen**.
3. Vul de velden indien nodig op de regel in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Vul een regel in voor elke combinatie waarmee een speciale verkoopregelkorting aan de klant wordt verleend.

> [!Note]
> Wanneer u de pagina's **Verkoopprijzen** en **Verkoopregelkortingen** vanuit een specifieke klant opent, zijn de velden **Verkoopsoortfilter** en **Verkoopcodefilter** ingesteld voor de klant en kunnen deze niet worden gewijzigd of verwijderd.
>
> Als u prijzen of regelkortingen voor alle klanten, een klantprijsgroep of een campagne wilt instellen, moet u de pagina's vanuit een artikelkaart openen. Als alternatief kunt u voor verkoopprijzen de pagina **Verkoopprijsvoorstel** gebruiken. Zie voor meer informatie [Artikelprijzen in bulk bijwerken](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

## <a name="new-experience"></a>[Nieuwe ervaring](#tab/new-experience)  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies de gerelateerde koppeling.
2. Kies de klant en kies vervolgens de actie **Verkoopprijslijsten**.
3. Open de prijslijst waarvoor u de regelkorting wilt opgeven.
4. Maak een nieuwe regel of kies een bestaande regel en vul de velden indien nodig in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Kies in het veld **Definieert** de optie **Prijs en korting** of alleen **Korting**. 
6. Geef in het veld **Regelkorting %** het kortingspercentage op.

   > [!TIP]
   > U kunt de regels filteren door de juiste optie te kiezen in het veld **Kolommen weergeven voor**.   
  
   > [!NOTE]
   > Factuurkortingscodes worden vertegenwoordigd door bestaande klantenkaarten. Met behulp van klantnamen als codes kunt u snel factuurkortingsvoorwaarden aan klanten toewijzen door de naam van een andere klant te kiezen die dezelfde voorwaarden heeft. Om klantspecifieke kortingsvoorwaarden voor facturen in te stellen, stelt u het veld **Factuurkortingscode** in op de klantcode van de klant en gaat u verder met de volgende stap.

---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Een factuurkorting voor een klant instellen
Wanneer u hebt bepaald welke klanten in aanmerking komen voor factuurkortingen, geeft u de factuurkortingscode op de klantenkaarten op en stelt u de voorwaarden voor elke code in.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies de gerelateerde koppeling.
2. Open de klantenpagina voor een klant die voor factuurkortingen in aanmerking komt.
3. Selecteer in het veld **Factuurkortingscode** een code voor de desbetreffende factuurkortingsvoorwaarden die moeten worden gehanteerd voor het berekenen van factuurkortingen voor de klant. 

> [!NOTE]  
> Factuurkortingscodes worden vertegenwoordigd door bestaande klantenkaarten. Met behulp van klantnamen als codes kunt u snel factuurkortingsvoorwaarden aan klanten toewijzen door de naam van een andere klant te kiezen die dezelfde voorwaarden heeft.

Stel nu de voorwaarden voor de nieuwe verkoopfactuurkorting in.

1. Kies op de pagina **Klanten** de actie **Factuurkortingen**. De pagina **Verkoopfactuurkorting** verschijnt.
2. Geef in het veld **Valutacode** de code op voor een valuta waarvoor de factuurkortingscondities op de regel van toepassing zijn. Laat het veld leeg als u factuurkortingscondities in de lokale valuta wilt instellen.
3. Geef in het veld **Minimumbedrag** op hoe hoog het factuurbedrag minimaal moet zijn voordat een korting wordt berekend.
4. Voer in het veld **Korting %** de factuurkorting in als percentage van het factuurbedrag.
5. Herhaal stap 5 tot en met 7 voor elke valuta waarvoor de klant een andere factuurkorting ontvangt.

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

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/manage-sales-prices-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Verkopen instellen](sales-setup-sales.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]