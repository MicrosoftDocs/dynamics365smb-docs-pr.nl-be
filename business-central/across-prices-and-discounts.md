---
title: Prijzen en kortingen instellen
description: Beschrijft hoe u standaard- en speciale prijs- en kortingsovereenkomsten voor verkopen en aankopen kunt definiëren.
author: brentholtorf
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'price, pricing, discount, discounting, rebate, sale, purchase, invoice'
ms.search.form: '459, 460, 7001, 7011, 7015, 7016, 7017, 7018'
ms.date: 04/01/2021
ms.author: bholtorf
---
# Prijzen en kortingen instellen

> [!NOTE]
> In releasewave 2 van 2020 hebben we gestroomlijnde processen uitgebracht voor het instellen en beheren van prijzen en kortingen. Als u een nieuwe klant bent en die versie gebruikt, gebruikt u de nieuwe ervaring. Als u een bestaande klant bent, hangt of u de nieuwe ervaring gebruikt, af van de vraag of uw beheerder de functie-update **Nieuwe verkoopprijservaring** heeft geactiveerd op de pagina **Functiebeheer**. Zie voor meer informatie [Aankomende functies van tevoren inschakelen](/dynamics365/business-central/dev-itpro/administration/feature-management).

Prijs- en kortingsstrategieën voor de aan- en verkoop van artikelen en diensten zijn fundamentele instrumenten voor succesvolle bedrijven. Nadat u de artikelen en services hebt ingesteld die uw bedrijf koopt en verkoopt, kunt u bepalen wat u ervoor betaalt of in rekening brengt, en die bedragen worden automatisch toegevoegd aan verkoop- en inkoopdocumenten. 

## Prijzen en kortingen instellen

Voordat u prijslijsten maakt, moet u uw prijs- en kortingsstrategieën definiëren op de pagina's **Verkoopinstellingen** en **Instellingen Inkoop en betalingen**.

U kunt twee soorten kortingen instellen:

| Type korting | Omschrijving |
| --- | --- |
| **Regelkorting** |Een kortingsbedrag dat wordt gegeven voor regels in verkoop- en inkoopdocumenten. Regelkortingen zijn doorgaans gebaseerd op een combinatie van klant, artikel, minimumhoeveelheid, maateenheid of tijdsperiode die u definieert voor verkopen en aankopen op de pagina's **Verkoopinstellingen** en **Instellingen Inkoop en betalingen**.|
| **Factuurkorting** |Een kortingspercentage dat van het documenttotaal van de inkoop en verkoop wordt afgetrokken als het totaal van alle regels in het document een bepaald minimum overschrijdt. |

Doordat verkoopprijzen en verkoopregelkortingen worden gebaseerd op een combinatie van artikel en klant, kunt u dit ook configureren vanaf de artikelpagina van het artikel waarop de regels en waarden van toepassing zijn.

> [!TIP]  
> Als u niet wilt dat een artikel ooit met korting wordt verkocht, laat u de kortingsvelden op de artikelpagina leeg en neemt u het artikel niet op in instellingen van regelkorting.

## Over prijslijsten

Prijslijsten zijn flexibel en laten u de zakenpartner of activiteit specificeren waarop ze van toepassing zijn. U kunt bijvoorbeeld één prijslijst opstellen die van toepassing is op alle leveranciers en klanten, of speciale prijzen of kortingen aanbieden voor elke zakenpartner, misschien gebaseerd op een minimumhoeveelheid op inkoop- of verkooporders, of een bepaalde combinatie van klant, artikel, minimumhoeveelheid, maateenheid of tijdsperiode. De prijzen en kortingen die u definieert, worden automatisch toegepast op inkoop- en verkoopdocumenten. 

## Prijzen instellen

Deze stappen verschillen, afhankelijk van of uw beheerder de functie-update **Nieuwe verkoopprijservaring** heeft geactiveerd. 

#### [Huidige ervaring](#tab/current-experience)  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Klanten** in en kies vervolgens de gerelateerde koppeling.
2. Kies de klant en kies vervolgens de actie **Prijzen**.
3. Vul de velden indien nodig op de regel in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Vul een regel in voor elke combinatie waarmee een speciale verkoopprijs aan de klant wordt verleend.

#### [Nieuwe ervaring](#tab/new-experience)  

U kunt voor elke regel handmatig artikelen en services toevoegen, of u kunt de actie **Regels voorstellen** gebruiken om nieuwe prijzen te creëren voor geselecteerde artikelen, artikelkortingsgroepen, resources en andere productsoorten. Als u **Regels voorstellen** kiest, kunt u op de pagina **Prijsregels - Nieuw maken** filters gebruiken om de artikelen of services te selecteren die u in de prijslijst wilt opnemen. U kunt ook aangeven of bij het berekenen van prijzen rekening moet worden gehouden met een minimumhoeveelheid, de correctiefactor die moet worden toegepast voor nieuwe prijslijstregels en de afrondingsmethode die voor prijzen moet worden toegepast. 

Standaard is de status van nieuwe prijslijsten **Concept**. Als u klaar bent om de lijst te gebruiken, kunt u de status wijzigen in **Actief**.

Als u prijslijsten en prijzen wilt bekijken die van toepassing zijn op specifieke klanten of leveranciers, kiest u op de pagina **Klant** of **Verkoper** de actie **Verkoopprijslijsten** of **Inkoopprijslijsten**. Voor artikelen en resources kunt u prijslijstregels bekijken door **Verkoopprijzen** of **Inkoopprijzen** te kiezen op de pagina's **Artikel** en **Resource**.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Klanten** in en kies vervolgens de gerelateerde koppeling.
2. Kies de klant en kies vervolgens de actie **Verkoopprijslijsten**. 
3. Kies **Nieuw** om een nieuwe verkoopprijslijst te maken.
4. Vul indien nodig de velden in op de sneltabbladen **Algemeen** en **Btw**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
5. Voer een van de volgende handelingen uit om items aan de lijst toe te voegen:
   * Kies om veel items toe te voegen **Regels voorstellen** en voer vervolgens filtercriteria in om de typen items op te geven die moeten worden toegevoegd. Optioneel kunt u ook enkele aanvullende instellingen invoeren voor de artikelen die specifiek zijn voor de prijslijst. U kunt dit later indien nodig wijzigen.
   * Kies om items uit een andere prijslijst te kopiëren **Regels kopiëren** en kies vervolgens de prijslijst die u wilt kopiëren.
   * Als u handmatig artikelen wilt toevoegen, kiest u in het veld **Producttype** het type product waarvoor de prijslijst bedoeld is. Vul indien nodig de overige velden in, afhankelijk van uw selectie. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Om de prijslijst te gaan gebruiken, kiest u in het veld **Status** **Actief**.  

---

## Een verkoopregelkorting instellen voor een klant

Deze stappen verschillen, afhankelijk van of uw beheerder de functie-update **Nieuwe verkoopprijservaring** heeft geactiveerd. 

#### [Huidige ervaring](#tab/current-experience/)  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies vervolgens de gerelateerde koppeling.
2. Open de desbetreffende klantenkaart en kies vervolgens de actie **Regelkortingen**.
3. Vul de velden indien nodig op de regel in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Vul een regel in voor elke combinatie waarmee een speciale verkoopregelkorting aan de klant wordt verleend.

> [!Note]
> Wanneer u de pagina's **Verkoopprijzen** en **Verkoopregelkortingen** vanuit een specifieke klant opent, zijn de velden **Verkoopsoortfilter** en **Verkoopcodefilter** ingesteld voor de klant en kunnen deze niet worden gewijzigd of verwijderd.
>
> Als u prijzen of regelkortingen voor alle klanten, een klantprijsgroep of een campagne wilt instellen, moet u de pagina's vanuit een artikelkaart openen. Als alternatief kunt u voor verkoopprijzen de pagina **Verkoopprijsvoorstel** gebruiken. Zie voor meer informatie [Artikelprijzen in bulk bijwerken](sales-how-record-sales-price-discount-payment-agreements.md#to-bulk-update-item-prices).  

#### [Nieuwe ervaring](#tab/new-experience/)  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Klanten** in en kies vervolgens de gerelateerde koppeling.
2. Kies de klant en kies vervolgens de actie **Verkoopprijslijsten**.
3. Open de prijslijst waarvoor u de regelkorting wilt opgeven.
4. Zet de schakelaar **Regelkorting toestaan** aan.
5. Maak een nieuwe regel of kies een bestaande regel en vul de velden indien nodig in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
6. Kies in het veld **Definieert** de optie **Prijs en korting** of alleen **Korting**. 
7. Geef in het veld **Regelkorting %** het kortingspercentage op.

   > [!TIP]
   > Als u een bestaande regel bewerkt, kunt u de regels filteren door de juiste optie te kiezen in het veld **Kolommen weergeven voor**.

---

## Werken met factuurkortingen en administratiekosten

Wanneer u factuurkortingen gebruikt, wordt op basis van het factuurbedrag bepaald welke korting wordt verleend. Op de pagina **Factuurkortingen** kunt u ook een bepaald bedrag aan administratiekosten toevoegen aan facturen.  <!--The Invoice Discounts page is hard to find.-->

U kunt factuurkortingen bij verkopen pas gebruiken nadat u bepaalde gegevens hebt opgegeven in de toepassing. U moet beslissen welke klanten dit type korting krijgen en welke kortingspercentages u gaat gebruiken.  

Als u factuurkortingen automatisch wilt berekenen, kunt u dit opgeven op de pagina **Verkoopinstellingen**.  

Voor elke klant kunt u opgeven of u factuurkortingen verleent als aan de voorwaarde is voldaan (als dus het factuurbedrag hoog genoeg is). U kunt de voorwaarden voor factuurkortingen definiëren in de lokale valuta voor binnenlandse klanten en in een vreemde valuta voor buitenlandse klanten.  

U koppelt kortingspercentages aan specifieke factuurbedragen op de pagina **Factuurkortingen**. U kunt zo veel percentages als nodig opgeven. Elke klant kan een eigen pagina hebben of u kunt verschillende klanten aan dezelfde pagina koppelen.  

Naast (of in plaats van) een kortingspercentage kunt u administratiekosten aan een specifiek factuurbedrag koppelen.  

> [!TIP]  
> Voordat u begint met het invoeren van deze informatie, is het een goed idee om van tevoren uw kortingsstructuur voor te bereiden, zodat u gemakkelijker kunt zien welke klanten aan dezelfde factuurkortingspagina moeten worden gekoppeld. Zie [Kortingen instellen voor uw klanten](/training/modules/customer-discounts-dynamics-365-business-central/index) voor meer informatie over kortingen bij verkopen.

### Een factuurkorting voor een klant instellen

Nadat u hebt bepaald welke klanten in aanmerking komen voor factuurkortingen, geeft u de factuurkortingscode op de klantenkaarten op en stelt u de voorwaarden voor elke code in.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Klanten** in en kies vervolgens de gerelateerde koppeling.
2. Open de klantenpagina voor een klant die voor factuurkortingen in aanmerking komt.
3. Selecteer in het veld **Factuurkortingscode** een code voor de desbetreffende factuurkortingsvoorwaarden die moeten worden gehanteerd voor het berekenen van factuurkortingen voor de klant. <!--Looks like I can only choose customers in this list-->

> [!NOTE]  
> Factuurkortingscodes worden vertegenwoordigd door bestaande klantenkaarten. Zo kunt u snel factuurkortingsvoorwaarden aan klanten toewijzen door de naam van een andere klant te kiezen die dezelfde voorwaarden heeft.

Ga door met het instellen van de voorwaarden voor de nieuwe verkoopfactuurkorting.

1. Kies op de pagina **Klanten** de actie **Factuurkortingen**. De pagina **Verkoopfactuurkorting** verschijnt.
2. Geef in het veld **Valutacode** de code op voor een valuta waarvoor de factuurkortingscondities op de regel van toepassing zijn. Laat het veld leeg als u factuurkortingscondities in de lokale valuta wilt instellen.
3. Geef in het veld **Minimumbedrag** op hoe hoog het factuurbedrag minimaal moet zijn voordat een korting wordt berekend.
4. Voer in het veld **Korting %** de factuurkorting in als percentage van het factuurbedrag.
5. Herhaal stap 5 tot en met 7 voor elke valuta waarvoor de klant een andere factuurkorting ontvangt.

De factuurkorting is nu ingesteld en toegewezen aan de klant in kwestie. Wanneer u de klantcode selecteert in het veld **Factuurkortingscode** op andere klantenkaarten, wordt dezelfde factuurkorting toegewezen aan die klanten.

## Verkoopprijzen kopiëren

Deze stappen verschillen, afhankelijk van of uw beheerder de functie-update **Nieuwe verkoopprijservaring** heeft geactiveerd. 

#### [Huidige ervaring](#tab/current-experience/)  

Als u verkoopprijzen wilt kopiëren, bijvoorbeeld om de verkoopprijzen van een individuele klant voor een klantenprijsgroep te gebruiken, moet u de batchverwerking **Verkoopprijsvoorstellen maken**. uitvoeren op de pagina **Verkoopprijsvoorstel**.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopprijsvoorstel** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Verkoopprijsvoorstellen maken** .  
3. Vul op het sneltabblad **Verkoopprijzen** in de velden **Verkoopsoort** en **Verkoopcode** de waarden in van de oorspronkelijke verkoopprijzen die u wilt kopiëren.  
4. Vul in het bovenste gedeelte van de aanvraagpagina de velden **Verkoopsoort** en **Verkoopcode** in met het type en de naam waarnaar u de verkoopprijzen wilt kopiëren.  
5. Als u nieuwe prijzen wilt maken met de batchverwerking, schakelt u het selectievakje **Nieuwe prijzen maken** in.  
6. Kies de knop **OK** om de regels op de pagina **Verkoopprijsvoorstel** in te vullen met de voorgestelde nieuwe prijzen. Hiermee geeft u aan dat deze prijzen geldig zijn voor de geselecteerde Verkoopsoort.  

   > [!NOTE]  
   > Met deze batchverwerking worden alleen suggesties gemaakt en worden de voorgestelde wijzigingen niet geïmplementeerd. Als u tevreden bent met de suggesties en deze wilt implementeren (invoegen op de pagina **Verkoopprijzen**), kiest u de actie **Prijsaanpassing doorvoeren** op de pagina **Verkoopprijsvoorstel**.

#### [Nieuwe ervaring](#tab/new-experience/)  

De status van de prijslijstregel moet **Concept** zijn. 

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopprijslijsten** in en kies vervolgens de gerelateerde koppeling. 
2. Kies de prijslijst die u wilt kopiëren en kies vervolgens **Regels kopiëren**.
3. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

   > [!NOTE]
   > U kunt geen twee regels hebben met dezelfde instellingen maar verschillende prijzen. Als dat gebeurt, wordt er een bericht weergegeven wanneer u een prijslijst activeert. U kunt de te gebruiken prijs kiezen door de lijst te openen en de verkeerde prijs te verwijderen.  
  
---

## Artikelprijzen bulksgewijs bijwerken

Deze stappen verschillen, afhankelijk van of uw beheerder de functie-update **Nieuwe verkoopprijservaring** heeft geactiveerd. 

#### [Huidige ervaring](#tab/current-experience/)

Als u artikelprijzen bulksgewijs wilt bijwerken, bijvoorbeeld alle artikelprijzen met een bepaald percentage wilt verhogen, moet u de batchverwerking **Artikelprijsvoorstellen maken**. uitvoeren. U vindt een koppeling voor de batchverwerking op de pagina **Verkoopprijsvoorstel**.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopprijsvoorstel** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Artikelprijsvoorstellen maken** .  
3. Voer op het sneltabblad **Artikel** het veld **Nr.** of **Voorraadboekingsgroep** of overige velden in met de oorspronkelijke artikelprijzen die u wilt bijwerken.  
4. Gebruik in het bovenste gedeelte van de aanvraagpagina de velden **Verkoopsoort** en **Verkoopcode** om aan te geven waarnaar u de verkoopprijzen wilt kopiëren.
5. Als u de batchverwerking automatisch voorgestelde artikelprijzen wilt laten aanpassen, voert u in het veld **Herwaarderingsfactor** de herwaardering in. Typ bijvoorbeeld 1,15 in het veld **Herwaarderingsfactor** voor een 15%-toename van de artikelprijs.  
6. Als u nieuwe prijzen wilt maken met de batchverwerking, schakelt u het selectievakje **Nieuwe prijzen maken** in.  
7. Kies de knop **OK** om de nieuwe prijsvoorstellen in te vullen op de pagina **Verkoopprijsvoorstel**. Hiermee geeft u aan dat deze prijzen geldig zijn voor het geselecteerde **Artikel**.  

> [!NOTE]
> Met deze batchverwerking worden alleen suggesties gemaakt en worden de voorgestelde wijzigingen niet geïmplementeerd. Als u de voorstellen wilt toepassen, voegt u de gegevens in de tabel **Verkoopprijzen** in. Hiervoor kunt u de batchverwerking **Prijsaanpassing doorvoeren** gebruiken onder **Acties**, in de groep **Functies** op de pagina **Verkoopprijsvoorstel**.

#### [Nieuwe ervaring](#tab/new-experience/)

Om prijzen voor meerdere artikelen bij te werken moet u een nieuwe prijslijst maken en vervolgens de regels uit een bestaande prijslijst kopiëren. Wanneer u de regels kopieert, kunt u filters gebruiken om aan te geven wat u wilt kopiëren, en u kunt een geheel getal of decimaal getal specificeren in het veld **Herwaarderingsfactor** om prijzen te verhogen of te verlagen. De status van de prijslijst moet **Concept** zijn. Indien nodig kunt u vervolgens de oude prijslijst deactiveren.

> [!NOTE]
> U kunt geen twee regels hebben met dezelfde instellingen maar verschillende prijzen. Als dat gebeurt, wordt er een bericht weergegeven wanneer u een prijslijst activeert. U kunt de te gebruiken prijs kiezen door de lijst te openen en de verkeerde prijs te verwijderen.  

---

## De beste prijs berekenen

Wanneer u speciale prijzen en regelkortingen voor verkopen en inkopen hebt geregistreerd, wordt er in [!INCLUDE[d365fin](includes/d365fin_md.md)] voor gezorgd dat uw winst op artikelhandel altijd optimaal is door de beste prijs op verkoop- en inkoopdocumenten en op project- en artikeldagboekregels automatisch te berekenen. Zie [De beste prijs berekenen](sales-how-record-sales-price-discount-payment-agreements.md#best-price-calculation) voor meer informatie.

## Zie gerelateerde [Microsoft-training](/training/modules/customer-discounts-dynamics-365-business-central/)

## Zie ook

[Verkopen instellen](sales-setup-sales.md)  
[Verkoop](sales-manage-sales.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
