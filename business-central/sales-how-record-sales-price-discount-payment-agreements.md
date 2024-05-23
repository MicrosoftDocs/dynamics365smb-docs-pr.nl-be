---
title: Speciale verkoopprijzen en kortingen registreren
description: Beschrijft hoe u prijs- en kortingsovereenkomsten voor verkoopdocumenten definieert.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: how-to
ms.date: 06/13/2023
ms.custom: bap-template
ms.search.keywords: 'special price, alternate price, pricing'
ms.search.form: '7022, 7024'
ms.service: dynamics-365-business-central
---

# <a name="record-special-sales-prices-and-discounts"></a>Speciale verkoopprijzen en kortingen registreren

> [!NOTE]
> In releasewave 2 van 2020 hebben we nieuwe, gestroomlijnde processen geïntroduceerd voor het instellen en beheren van prijzen en kortingen. Als u een nieuwe klant bent en de meest recente versie gebruikt, gebruikt u de nieuwe ervaring. Als u een bestaande klant bent, hangt of u de nieuwe ervaring gebruikt, af van de vraag of uw beheerder de functie-update **Nieuwe verkoopprijservaring** heeft geactiveerd in **Functiebeheer**. Meer informatie op [Aankomende functies van tevoren inschakelen](/dynamics365/business-central/dev-itpro/administration/feature-management) in de beheer-inhoud.

[!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt verschillende prijsstrategieën, zoals:

* One-price-fits-all-modellen waarbij een artikel altijd voor dezelfde prijs wordt verkocht.
* Speciale prijsafspraken met specifieke klanten, of groepen klanten.
* Campagnes wanneer een verkoop voldoet aan de criteria voor een speciale aanbieding. U kunt bijvoorbeeld de volgende criteria voor een order hebben:

  * Het voldoet aan een minimale hoeveelheid
  * Het is voor een bepaalde datum
  * Het omvat een bepaald type artikel  

Om een basisprijsmodel te gebruiken hoeft u alleen een eenheidsprijs op te geven wanneer u een artikel of resource instelt. Die prijs wordt altijd gebruikt op verkoopdocumenten. Voor meer geavanceerde modellen, wanneer u bijvoorbeeld speciale prijzen wilt aanbieden voor een verkoopcampagne, kunt u daarvoor criteria opgeven op de pagina **Verkoopprijzen**. U kunt speciale prijzen aanbieden op basis van combinatie van de volgende gegevens:  

* Klant
* Artikel
* Eenheid
* Minimumhoeveelheid
* Datums die de periode bepalen waarvoor de prijzen geldig zijn.

Nadat u speciale prijzen heeft ingesteld, kan [!INCLUDE[prod_short](includes/prod_short.md)] de beste prijzen berekenen op verkoop- en inkoopdocumenten, en voor regels van projecten en artikeljournalen. Meer informatie op [Beste prijsberekening](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation).

Voor verkoopkortingen kunt twee soorten instellen:

| Kortingsoort | Omschrijving |
| --- | --- |
| **Verkoopregelkorting** |Voeg een bedrag toe aan verkoopregels die een bepaalde combinatie hebben van klant, artikel, minimumhoeveelheid, maateenheid of begin- en einddatum. Dit type werkt op dezelfde manier als bij verkoopprijzen. |
| **Factuurkorting** |Een kortingspercentage dat van het verkoopdocumenttotaal wordt afgetrokken als het totaal van alle regels in het document een bepaald minimum overschrijdt. |

> [!TIP]  
> Als u niet wilt dat een artikel ooit met korting wordt verkocht, laat u de kortingsvelden op de artikelpagina leeg en neemt u het artikel niet op in instellingen van regelkorting.

## <a name="to-set-up-a-sales-price-for-a-customer"></a>Een verkoopprijs voor een klant instellen

Deze stappen verschillen, afhankelijk van of uw beheerder de functie-update **Nieuwe verkoopprijservaring** heeft geactiveerd. Als de functie-update niet is ingeschakeld, volgt u de stappen op het tabblad Huidige ervaring. 

#### [Huidige ervaring](#tab/current-experience/)

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies de gerelateerde koppeling.
2. Kies de klant en kies vervolgens de actie **Prijzen**.
3. Vul de velden indien nodig op de regel in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Vul een regel in voor elke combinatie waarmee een speciale verkoopprijs aan de klant wordt verleend.

#### [Nieuwe ervaring](#tab/new-experience/)  

Standaard is de status van nieuwe prijslijsten **Concept**. Conceptprijslijsten worden niet meegenomen in prijsberekeningen. Als u klaar bent met het toevoegen van regels en u wilt de prijzen gaan gebruiken, wijzigt u de status in **Actief**.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies de gerelateerde koppeling.
2. Kies de klant en kies vervolgens de actie **Verkoopprijslijsten**. 
3. Kies **Nieuw** om een nieuwe verkoopprijslijst te maken.
4. Vul indien nodig de velden in op de sneltabbladen **Algemeen** en **Btw**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Voer een van de volgende handelingen uit om items aan de lijst toe te voegen:
   * Kies om veel items toe te voegen **Regels voorstellen** en voer vervolgens filtercriteria in om de typen items op te geven die moeten worden toegevoegd. Optioneel kunt u ook andere instellingen invoeren voor de artikelen die specifiek zijn voor de prijslijst. U kunt deze instellingen later indien nodig wijzigen.
   * Kies om items uit een andere prijslijst te kopiëren **Regels kopiëren** en kies vervolgens de prijslijst die u wilt kopiëren.
   * Als u handmatig artikelen wilt toevoegen, kiest u in het raster in het veld **Producttype** het type product waarvoor de prijslijst bedoeld is. Vul indien nodig de overige velden in, afhankelijk van uw selectie. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Om de prijslijst te gaan gebruiken, kiest u in het veld **Status** **Actief**.  

---

## <a name="using-sales-and-purchase-price-lists"></a>Verkoop- en inkoopprijslijsten gebruiken

> [!NOTE]
> Voor het gebruik van prijslijsten moet uw beheerder de functie-update **Nieuwe verkoopprijservaring** in **Functiebeheer** hebben ingeschakeld. Meer informatie op [Aankomende functies van tevoren inschakelen](/dynamics365/business-central/dev-itpro/administration/feature-management) in de beheer-inhoud.

Het grootste deel van de nieuwe ervaring met verkoopprijzen is vergelijkbaar met de huidige ervaring, maar er zijn een paar verschillen. Deze verschillen worden beschreven in de volgende secties.

De velden **Toepassingstype** en **Toepassingsnr.** laten u kiezen waarop een prijslijst van toepassing is, zoals klant of klantprijsgroep. Met **Kolommen weergeven voor** kunt u kolommen weergeven of verbergen die relevant zijn voor het instellen van prijzen, kortingen of prijzen en kortingen.

### <a name="converting-existing-prices-when-you-turn-on-the-pricing-feature-update"></a>Bestaande prijzen converteren wanneer u de update van de prijsfunctie inschakelt

Wanneer u de functie-update **Nieuwe verkoopprijservaring** op de pagina **Functiebeheer** inschakelt, wordt de guide **Gegevensupdatefunctie** geopend. Gebruik de schakelaar **Standaardprijzen gebruiken** als volgt:

* Als u met alle prijzen op één pagina wilt werken, schakelt u deze in. Bestaande prijzen worden geconverteerd naar één standaardprijslijst voor elk van de volgende documenten:

  * Verkoop
  * Inkopen
  * Projectomzet
  * Projectinkopen

  U kunt alle prijzen voor deze gebieden bewerken op de pagina **Prijsvoorstel**. De standaardprijslijsten worden ingesteld op de pagina's **Verkoopinstellingen**, **Inkoopinstellingen** en **Projectinstellingen**.

> [!NOTE]
> Als prijzen alleen op artikel- of resourcekaarten worden ingesteld, worden tijdens de gegevensupdate geen standaardprijslijsten met die prijzen ingevuld. U kunt echter elk van de standaardprijslijsten of de pagina **Prijsvoorstel** openen en de actie **Regels voorstellen** gebruiken om de prijzen toe te voegen die zijn ingesteld op artikel- of resourcekaarten.

* Schakel dit uit om verkoopprijslijsten te gebruiken. Bestaande prijzen worden geconverteerd naar een nieuwe prijs voor elke combinatie van de volgende:

  * Klant
  * Klantengroep of campagne
  * Begin- en einddatum
  * Valuta's

Als u veel combinaties hebt, hebt u veel prijslijsten.

Als u de nieuwe prijservaring al hebt ingeschakeld, kunt u handmatig standaardprijslijsten maken of een bestaande prijslijst als standaard opgeven. Om een bestaande prijslijst als standaard in te stellen zet u de schakelaar **Bijwerken van standaardinstellingen toestaan** aan in de prijslijst. Vervolgens stelt u de prijslijst als de standaard in op de pagina **Verkoopinstellingen**, **Inkoopinstellingen** of **Projectinstellingen**.

### <a name="editing-active-price-lists"></a>Actieve prijslijsten bewerken

Om mensen in staat te stellen prijzen te bewerken op actieve prijslijsten voor artikelen, resources, klanten, leveranciers of andere entiteiten die prijzen gebruiken, zet u de schakelaar **Bewerken van actieve prijs toestaan** aan op de pagina **Verkoopinstellingen** en **Inkoopinstellingen**.

Wanneer de schakelaar **Bewerken van actieve prijs toestaan** is uitgeschakeld, moet u om prijzen in een prijslijst bij te werken, de status van de prijslijst wijzigen in **Concept**, uw wijziging aanbrengen en de prijslijst vervolgens weer activeren.

De pagina **Overzicht van prijzen** geeft een overzicht van alle prijzen over prijslijsten heen. U kunt filters instellen om de lijst met prijzen die u mogelijk wilt wijzigen of aanvullen, te verfijnen. Nadat u de prijzen heeft gewijzigd, moet u de actie **Regels controleren** gebruiken om de prijzen te controleren met andere prijslijstregels. Door prijzen te verifiëren worden duplicaten en dubbelzinnigheid tijdens de prijsberekening voorkomen.

> [!NOTE]
> Wanneer u een regel in een actieve prijslijst bewerkt, wordt de status van de regel **Concept** en wordt de regel pas in prijsberekeningen meegenomen als u de actie **Regels controleren** gebruikt. Nadat u de prijs heeft geverifieerd, wordt de status van de regel **Actief** en wordt deze meegenomen in prijsberekeningen.

Om nieuwe prijzen toe te voegen gebruikt u op de pagina **Overzicht van prijzen** de actie **Nieuwe regels toevoegen**. De pagina **Prijsvoorstel** wordt geopend en u kunt prijsregels toevoegen door ze voor te stellen op basis van criteria, ze te kopiëren van andere prijslijsten of ze handmatig in te voeren. Daarna kunt u de actie **Prijswijziging doorvoeren** gebruiken om de nieuwe prijzen te vergelijken met andere prijslijsten om duplicaten en verwarring tijdens de prijsberekening te voorkomen.

#### <a name="create-sales-price-lines-based-on-the-unit-price"></a>Verkoopprijsregels maken op basis van de eenheidsprijs

1. Kies op de pagina **Prijsvoorstel** de actie **Regels voorstellen**.
2. Vul op de pagina **Prijsregels - Nieuw maken** in de velden de gewenste gegevens in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Definieer in het veld **Productfilter** filters voor het geselecteerde **Producttype**.
4. Kies het veld **Standaardinstellingen** om instellingen op te geven, zoals:
   * Aan welke entiteiten de prijslijst wordt toegewezen.
   * Datums waarop de prijs geldig is.
   * De valutacode.
   * Het bedragtypefilter dat bepaalt welke kolommen worden weergegeven op de prijslijstregels.
5. Klik op **OK**. Nieuwe regels worden toegevoegd aan de pagina **Prijsvoorstel** met de geselecteerde instellingen en de eenheidsprijzen van de artikelkaarten.
6. Bewerk de gemaakte regels met de nieuwe eenheidsprijzen of kortingen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

#### <a name="create-sales-price-lines-based-on-existing-price-lists"></a>Verkoopprijsregels maken op basis van bestaande prijslijsten

1. Kies op de pagina **Prijsvoorstel** de actie **Regels kopiëren**.
2. Selecteer op de pagina **Prijsregels - Bestaande kopiëren** een bestaande prijslijst in het veld **Van prijslijst**.
3. Definieer in het veld **Prijsregelfilter** filters voor de producten op de geselecteerde prijslijst.
4. Kies het veld **Standaardinstellingen** om instellingen op te geven, zoals:
   * Aan welke entiteiten de prijslijst wordt toegewezen.
   * Datums waarop de prijs geldig is.
   * De valutacode.
   * Het bedragtypefilter dat bepaalt welke kolommen worden weergegeven op de prijslijstregels.
5. Vul indien nodig de overige velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Klik op **OK**. Nieuwe regels worden toegevoegd aan de pagina **Prijsvoorstel** met de geselecteerde instellingen.
7. Bewerk de gemaakte regels met de nieuwe eenheidsprijzen of kortingen. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-copy-sales-prices"></a>Verkoopprijzen kopiëren

Deze stappen verschillen, afhankelijk van of uw beheerder de functie-update **Nieuwe verkoopprijservaring** heeft geactiveerd. Als de functie-update niet is ingeschakeld, volgt u de stappen op het tabblad Huidige ervaring.

#### [Huidige ervaring](#tab/current-experience/)  

Als u verkoopprijzen wilt kopiëren, bijvoorbeeld om de verkoopprijzen van een individuele klant voor een klantenprijsgroep te gebruiken, moet u de batchverwerking **Verkoopprijsvoorstellen maken**. uitvoeren op de pagina **Verkoopprijsvoorstel**.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopprijsvoorstel** in en kies de desbetreffende koppeling.  
2. Kies de actie **Verkoopprijsvoorstellen maken** .  
3. Vul op het sneltabblad **Verkoopprijzen** in de velden **Verkoopsoort** en **Verkoopcode** de waarden in van de oorspronkelijke verkoopprijzen die u wilt kopiëren.  
4. Vul in het bovenste gedeelte van de aanvraagpagina de velden **Verkoopsoort** en **Verkoopcode** in met het type en de naam waarnaar u de verkoopprijzen wilt kopiëren.  
5. Als u nieuwe prijzen wilt maken met de batchverwerking, schakelt u het selectievakje **Nieuwe prijzen maken** in.  
6. Kies de knop **OK** om de regels op de pagina **Verkoopprijsvoorstel** in te vullen met de voorgestelde nieuwe prijzen. Hiermee geeft u aan dat deze prijzen geldig zijn voor de geselecteerde Verkoopsoort.  

   > [!NOTE]  
   > Met deze batchverwerking worden alleen suggesties gemaakt en worden de voorgestelde wijzigingen niet geïmplementeerd. Als u tevreden bent met de suggesties en deze wilt implementeren (invoegen op de pagina **Verkoopprijzen**), kiest u de actie **Prijsaanpassing doorvoeren** op de pagina **Verkoopprijsvoorstel**.

#### [Nieuwe ervaring](#tab/new-experience/)  

U kunt de instellingen opgeven die de prijslijst zal gebruiken:

* Gebruik de instellingen uit de koptekst van de lijst die u kopieert.
* Gebruik de instellingen uit de koptekst van de lijst waarnaar u kopieert. Als u de instellingen wilt gebruiken van de prijslijst waarnaar u prijzen kopieert, schakelt u de schakelaar **Standaardinstellingen van doel gebruiken** in.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopprijslijsten** in en kies de desbetreffende koppeling.
2. Kies de prijslijst die u wilt kopiëren en kies vervolgens **Regels kopiëren**.
3. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > U kunt geen twee artikelen hebben met dezelfde instellingen maar verschillende prijzen. Als dat gebeurt, wordt er een bericht weergegeven wanneer u de prijslijst activeert. U kunt de te gebruiken prijs kiezen door de lijst te openen en de verkeerde prijs te verwijderen.  
  
---

## <a name="to-bulk-update-item-prices"></a>Artikelprijzen bulksgewijs bijwerken

Deze stappen verschillen, afhankelijk van of uw beheerder de functie-update **Nieuwe verkoopprijservaring** heeft geactiveerd. Als de functie-update niet is ingeschakeld, volgt u de stappen op het tabblad Huidige ervaring.

#### [Huidige ervaring](#tab/current-experience/)

Als u artikelprijzen in bulk wilt bijwerken, bijvoorbeeld om alle artikelprijzen met een percentage te verhogen, kunt u de pagina Verkoopprijsvoorstel invullen door de volgende batchtaken te gebruiken:

* **Verkoopprijsvoorstellen maken** stelt veranderingen op twee manieren voor:

  * Door een correctiefactor toe te passen op bestaande verkoopprijzen.
  * Door bestaande verkoopprijsafspraken te kopiëren naar andere klanten, klantprijsgroepen of verkoopcampagnes.

* **Artikelprijsvoorstellen maken** stelt veranderingen op twee manieren voor:

  * Door een correctiefactor toe te passen op bestaande eenheidsprijzen op artikelkaarten.
  * Door prijzen voor te stellen voor nieuwe combinaties van valuta, maateenheden, enzovoort.

  Deze batchverwerking wijzigt de eenheidsprijzen van artikelen niet.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopprijsvoorstel** in en kies de desbetreffende koppeling.  
2. Kies de actie **Artikelprijsvoorstellen maken** .  
3. Voer op het sneltabblad **Artikel** het veld **Nr.** of **Voorraadboekingsgroep** of overige velden in met de oorspronkelijke artikelprijzen die u wilt bijwerken.  
4. Gebruik in het bovenste gedeelte van de aanvraagpagina de velden **Verkoopsoort** en **Verkoopcode** om aan te geven waarnaar u de verkoopprijzen wilt kopiëren.
5. Als u de batchverwerking automatisch voorgestelde artikelprijzen wilt laten aanpassen, voert u in het veld **Herwaarderingsfactor** de herwaardering in. Typ bijvoorbeeld 1,15 in het veld **Herwaarderingsfactor** voor een 15%-toename van de artikelprijs.  
6. Als u nieuwe prijzen wilt maken met de batchverwerking, zet u de schakelaar **Nieuwe prijzen maken** aan.  
7. Kies de knop **OK** om de regels op de pagina **Verkoopprijsvoorstel** in te vullen met de voorgestelde nieuwe prijzen.
8. Gebruik om de suggesties te implementeren de actie **Prijsaanpassing doorvoeren**. De batchtaak doet suggesties, maar implementeert ze niet. 

#### [Nieuwe ervaring](#tab/new-experience/)

Om prijzen voor meerdere artikelen bij te werken moet u een nieuwe prijslijst maken en vervolgens de regels uit een bestaande prijslijst kopiëren. Wanneer u de regels kopieert, kunt u filters gebruiken om aan te geven wat u wilt kopiëren, en u kunt een geheel getal of decimaal getal specificeren in het veld **Herwaarderingsfactor** om prijzen te verhogen of te verlagen. De status van de prijslijst moet **Concept** zijn. Indien nodig kunt u vervolgens de oude prijslijst deactiveren.

> [!NOTE]
> U kunt geen twee regels hebben met dezelfde instellingen maar verschillende prijzen. Als dat gebeurt, wordt er een bericht weergegeven wanneer u een prijslijst activeert. U kunt de te gebruiken prijs kiezen door de lijst te openen en de verkeerde prijs te verwijderen.  

---

## <a name="best-price-calculation"></a>Berekening van beste prijs

Nadat u speciale prijzen en regelkortingen voor verkopen en aankopen hebt vastgelegd, berekent [!INCLUDE[prod_short](includes/prod_short.md)] de beste prijs op verkoop- en inkoopdocumenten en op project- en artikeldagboekregels.

De beste prijs is de laagst prijs met de hoogst regelkorting die toegestaan is op een bepaalde datum. In [!INCLUDE[prod_short](includes/prod_short.md)] worden de beste prijzen berekend wanneer eenheidsprijzen en de regelkortingspercentages worden opgeteld op document- en dagboekregels.

> [!NOTE]  
> Hierna wordt beschreven hoe de beste prijs voor verkoop wordt berekend. Voor aankopen is de berekening vergelijkbaar, maar gebaseerd op de beschikbare parameters. Artikelkortingsgroepen worden bijvoorbeeld niet ondersteund voor inkoop.

1. In [!INCLUDE[prod_short](includes/prod_short.md)] wordt de combinatie van de factuurklant en het artikel gecontroleerd en vervolgens worden de eenheidsprijs en het regelkortingspercentage die van toepassing zijn berekend op basis van de volgende criteria:

    * Is er een prijs-/kortingsafspraak voor de klant of behoort de klant tot een groep waarvoor een dergelijke afspraak geldt?
    * Zijn er dergelijke prijs-/kortingsafspraken van toepassing op het artikel of de artikelkortingsgroep op de regel?
    * Valt de datum binnen de begin- en einddatum van de prijs-/kortingsovereenkomst? Voor facturen en creditnota's is dit de datum in het veld **Boekingsdatum** in de documentkop. Voor alle andere documenten is dit de datum in het veld **Orderdatum** in de kopteksten ervan.
    * Is er een eenheidscode opgegeven? In dat geval controleert [!INCLUDE[prod_short](includes/prod_short.md)] op prijzen/kortingen met dezelfde eenheidscode en op prijzen/kortingen zonder eenheidscode.

2. [!INCLUDE[prod_short](includes/prod_short.md)] controleert of er prijs-/kortingsafspraken van toepassing zijn op informatie op de document- of journaalregel. Vervolgens worden de toepasselijke eenheidsprijs en het regelkortingspercentage ingevoegd met behulp van de volgende criteria:

    * Is er een minimale hoeveelheidsvereiste in de prijs-/kortingsafspraak waaraan wordt voldaan?
    * Is er een valutavereiste in de prijs-/kortingsafspraak waaraan wordt voldaan? Zo ja, dan worden de laagste prijs en de hoogste regelkorting voor deze valuta ingevoegd, zelfs als de lokale valuta een betere prijs oplevert. Als er geen prijs-/kortingsafspraak voor de opgegeven valutacode is, worden in [!INCLUDE[prod_short](includes/prod_short.md)] de laagste prijs en de hoogste regelkorting in lokale valuta ingevoegd.

Als er geen speciale prijs kan worden berekend voor het artikel op de regel, worden de laatste directe kosten of de eenheidsprijs van de artikelkaart ingevoegd.

## <a name="sales-invoice-discounts-and-service-charges"></a>Verkoopfactuurkortingen en administratiekosten

Wanneer u factuurkortingen gebruikt, wordt op basis van het totale bedrag op de factuur bepaald welke korting wordt verleend. Op de pagina **Verkoopfactuurkortingen** kunt u ook een bepaald bedrag aan administratiekosten toevoegen aan facturen.  

U kunt factuurkortingen bij verkopen pas gebruiken nadat u bepaalde gegevens hebt opgegeven. U moet de volgende beslissingen nemen:  

* Welke klanten in aanmerking komen voor dit soort korting?  
* Welke kortingspercentages u gebruikt?  

Als u factuurkortingen automatisch wilt berekenen, kunt u op de pagina **Verkoopinstellingen** de schakelaar **Factuurkorting berekenen** inschakelen.  

U kunt opgeven of u factuurkortingen toestaat als aan bepaalde factuurcriteria wordt voldaan voor elke klant. Bijvoorbeeld als het factuurbedrag groot genoeg is. Factuurkortingen kunnen worden opgegeven in lokale valuta voor binnenlandse klanten en in een vreemde valuta voor buitenlandse klanten.  

U koppelt kortingspercentages aan specifieke factuurbedragen op de pagina **Verkoopfactuurkortingen** voor elke klant. U kunt elk aantal percentages invoeren. Elke klant kan een eigen pagina hebben of u kunt verschillende klanten aan dezelfde pagina koppelen.  

Naast (of in plaats van) een kortingspercentage kunt u administratiekosten aan een specifiek factuurbedrag koppelen.  

> [!TIP]  
> Voordat u deze gegevens invoert, kunt u het beste een ontwerp maken van de kortingsstructuur die u wilt gebruiken. De structuur maakt het gemakkelijker te bepalen welke klanten kunnen worden gekoppeld aan dezelfde factuurkortingspagina. Hoe minder pagina's u hebt ingesteld, des te sneller kunt u de basisgegevens opgeven.

Zie [Kortingen instellen voor uw klanten](/training/modules/customer-discounts-dynamics-365-business-central/index) voor training in kortingen bij verkopen.

### <a name="calculating-invoice-discounts-on-sales"></a>Factuurkortingen op verkopen berekenen

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="to-set-up-a-sales-line-discount-for-a-customer"></a>Een verkoopregelkorting instellen voor een klant

Deze stappen verschillen, afhankelijk van of uw beheerder de functie-update **Nieuwe verkoopprijservaring** heeft geactiveerd. Als de functie-update niet is ingeschakeld, volgt u de stappen op het tabblad Huidige ervaring.

#### [Huidige ervaring](#tab/current-experience/)  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies de gerelateerde koppeling.
2. Open de desbetreffende klantenkaart en kies vervolgens de actie **Regelkortingen**.
3. Vul de velden indien nodig op de regel in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Vul een regel in voor elke combinatie waarmee een speciale verkoopregelkorting aan de klant wordt verleend.

> [!NOTE]
> Wanneer u de pagina's **Verkoopprijzen** en **Verkoopregelkortingen** vanuit een specifieke klant opent, zijn de velden **Verkoopsoortfilter** en **Verkoopcodefilter** ingesteld voor de klant en kunnen deze niet worden gewijzigd of verwijderd.
>
> Als u prijzen of regelkortingen voor alle klanten, een klantprijsgroep of een campagne wilt instellen, moet u de pagina's vanuit een artikelkaart openen. Als alternatief kunt u voor verkoopprijzen de pagina **Verkoopprijsvoorstel** gebruiken. Meer informatie op [Artikelprijzen bulksgewijs bijwerken](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

#### [Nieuwe ervaring](#tab/new-experience/)  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies de gerelateerde koppeling.
2. Kies de klant en kies vervolgens de actie **Verkoopprijslijsten**.
3. Open de prijslijst waarvoor u de regelkorting wilt opgeven.
4. Maak een nieuwe regel of kies een bestaande regel en vul de velden indien nodig in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Kies in het veld **Definieert** de optie **Prijs en korting** of alleen **Korting**. 
6. Geef in het veld **Regelkorting %** het kortingspercentage op.

    > [!TIP]
    > Als u een bestaande regel bewerkt, kunt u de regels filteren door de juiste optie te kiezen in het veld **Kolommen weergeven voor**.

    > [!NOTE]  
    > Factuurkortingscodes worden vertegenwoordigd door bestaande klantenkaarten. Zo kunt u snel factuurkortingsvoorwaarden aan klanten toewijzen door de naam van een andere klant te kiezen die dezelfde voorwaarden heeft. Om klantspecifieke kortingsvoorwaarden voor facturen in te stellen, stelt u het veld **Factuurkortingscode** in op de klantcode van de klant en gaat u verder met de volgende stap.

---

## <a name="to-set-up-an-invoice-discount-for-a-customer"></a>Een factuurkorting voor een klant instellen

Nadat u hebt bepaald welke klanten in aanmerking komen voor factuurkortingen, geeft u de factuurkortingscode op de pagina's voor klantenkaarten. Stel vervolgens de voorwaarden voor elke code in.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies de gerelateerde koppeling.
2. Open de klantenpagina voor een klant die voor factuurkortingen in aanmerking komt.
3. Selecteer in het veld **Factuurkortingscode** een code voor de desbetreffende factuurkortingsvoorwaarden die moeten worden gehanteerd voor het berekenen van factuurkortingen voor de klant.

> [!NOTE]  
> Factuurkortingscodes worden vertegenwoordigd door bestaande klantenkaarten. Zo kunt u snel factuurkortingsvoorwaarden aan klanten toewijzen door de naam van een andere klant te kiezen die dezelfde voorwaarden heeft.

Ga door met het instellen van de voorwaarden voor de nieuwe verkoopfactuurkorting.

1. Kies op de pagina **Klanten** de actie **Factuurkortingen**. De pagina **Verkoopfactuurkorting** verschijnt.
2. Geef in het veld **Valutacode** de code op voor een valuta waarvoor de factuurkortingscondities op de regel van toepassing zijn. Laat het veld leeg als u factuurkortingscondities in de lokale valuta wilt instellen.
3. Geef in het veld **Minimumbedrag** op hoe hoog het factuurbedrag minimaal moet zijn voordat een korting wordt berekend.
4. Voer in het veld **Korting %** de factuurkorting in als percentage van het factuurbedrag.
5. Herhaal stap 5 tot en met 7 voor elke valuta waarvoor de klant een andere factuurkorting ontvangt.

## <a name="see-also"></a>Zie ook

[Verkopen instellen](sales-setup-sales.md)  
[Verkoop](sales-manage-sales.md)  
[Klantenprijsgroepen instellen](sales-how-to-set-up-customer-price-groups.md)  
[Klantenkortingsgroepen instellen](sales-how-to-set-up-customer-discount-groups.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
