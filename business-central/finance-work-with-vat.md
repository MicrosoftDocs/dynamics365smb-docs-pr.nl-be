---
title: Met btw werken bij verkoop en inkoop
description: 'Dit onderwerp beschrijft de verschillende manieren om met btw te werken, zowel handmatig als met automatische instellingen, om u te helpen aan de landspecifieke regelgeving te voldoen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'VAT, sales, purchases'
ms.search.form: '7, 118, 130, 142, 459, 460, 525'
ms.date: 06/16/2021
ms.author: bholtorf
---
# <a name="work-with-vat-on-sales-and-purchases" />Werken met btw op verkoop en inkoop

Als uw land of regio vereist dat u belasting over de toegevoegde waarde (btw) op verkoop- en aankooptransacties berekent en rapporteert, kunt u [!INCLUDE[prod_short](includes/prod_short.md)] instellen voor het berekenen van btw. Zie [Berekeningen en boekingsmethoden voor btw instellen](finance-setup-vat.md) voor meer informatie.

Er zijn echter enkele taken met betrekking tot de berekening van btw die u handmatig kunt uitvoeren. Het kan bijvoorbeeld voorkomen dat u een geboekt bedrag moet corrigeren als u ontdekt dat een leverancier een andere afrondingsmethode gebruikt.  

> [!TIP]
> U kunt [!INCLUDE[prod_short](includes/prod_short.md)] btw-registratienummers en andere bedrijfsinformatie laten valideren wanneer u documenten maakt of bijwerkt. Zie voor meer informatie [Btw-registratienummers valideren](finance-how-validate-vat-registration-number.md).

## <a name="calculating-and-displaying-vat-amounts-on-sales-and-purchase-documents" />Btw-bedragen berekenen en weergeven in verkoop- en inkoopdocumenten

Wanneer u een artikelnummer kiest in het veld **Nr.** veld in een verkoop- of inkoopdocument, vult [!INCLUDE[prod_short](includes/prod_short.md)] de velden **Eenheidsprijs** en **Regelbedrag** in. De eenheidsprijs is afkomstig van de kaart **Artikel** of van de artikelprijzen die zijn toegestaan voor het artikel en de klant. [!INCLUDE[prod_short](includes/prod_short.md)] berekent het regelbedrag wanneer u een hoeveelheid opgeeft voor de regel.  

Als u wilt dat de eenheidsprijzen en regelbedragen inclusief btw zijn, bijvoorbeeld als u aan kleinverbruikers verkoopt, kiest u het selectievakje **Prijzen inclusief btw** in het document. Zie [Prijzen en regelbedragen inclusief/exclusief btw](#including-or-excluding-vat-in-prices-and-line-amounts) voor meer informatie. 

U kunt btw-bedragen op verschillende manieren berekenen en weergeven in verkoop- en inkoopdocumenten, afhankelijk van het type klant of leverancier waarmee u zakendoet. U kunt tevens handmatig het berekende btw-bedrag wijzigen, bijvoorbeeld zodat het overeenkomt met het btw-bedrag dat door uw leverancier voor een bepaalde transactie is berekend.

### <a name="including-or-excluding-vat-in-prices-and-line-amounts" />Prijzen en regelbedragen inclusief of exclusief btw

Als u het selectievakje **Prijzen inclusief btw** kiest in een verkoopdocument, zijn de velden **Eenheidsprijs** en **Regelbedrag** inclusief btw. Standaard zijn de waarden in deze velden exclusief btw. De namen van de velden geven aan of prijzen inclusief btw zijn.  

U kunt de standaardinstelling van **Prijs met btw** instellen voor alle verkoopdocumenten voor een klant in het veld **Prijs met btw** op de **Klant**-kaart. U kunt tevens artikelprijzen inclusief of exclusief btw instellen. Doorgaans zijn de prijzen op de artikelkaart exclusief btw. 

In de volgende tabel staat een overzicht van de manier waarop eenheidsprijsbedragen voor een verkoopdocument worden berekend wanneer u geen prijzen hebt ingesteld op de pagina **Verkoopprijzen**:  

|**Prijs met btw-veld op artikel (kaart)**|**Veld Prijzen inclusief btw**|**Uitgevoerde actie**|  
|-----------------------------------------------|----------------------------------------------------|--------------------------|  
|Niet ingeschakeld|Niet ingeschakeld|De **eenheidsprijs** op de artikelkaart wordt gekopieerd naar het veld **Eenheidsprijs excl. btw** op de verkoopregels.|  
|Niet ingeschakeld|Ingeschakeld|In de toepassing wordt het btw-bedrag berekend per eenheid en toegevoegd aan de **eenheidsprijs** op de artikelkaart. Deze totale eenheidsprijs wordt vervolgens ingevoerd in het veld **Eenheidsprijs incl. btw** op de verkoopregels.|  
|Ingeschakeld|Niet ingeschakeld|De toepassing berekent het btw-bedrag dat is opgenomen in het veld **Eenheidsprijs** op de **artikelkaart** en gebruikt het btw-percentage gerelateerd aan de combinatie Btw-bedr.-boekingsgr. (Prijs) en de Btw-productboekingsgroep. De **Eenheidsprijs** op de artikelkaart, verminderd met het btw-bedrag, wordt vervolgens ingevoerd in het veld **Eenheid prijs excl. btw** in de verkoopregels. Zie [Btw-bedrijfsboekingsgroepen en klantprijsgroepen gebruiken](finance-work-with-vat.md#using-vat-business-posting-groups-and-customer-price-groups) voor meer informatie.|  
|Ingeschakeld|Ingeschakeld|De **eenheidsprijs** op de artikelkaart wordt gekopieerd naar het veld **Eenheidsprijs incl. btw** op de verkoopregels.|

#### <a name="using-vat-business-posting-groups-and-customer-price-groups" />Btw-bedrijfsboekingsgroepen en klantprijsgroepen gebruiken

Als u wilt dat prijzen inclusief btw zijn, kunt u btw-bedrijfsboekingsgroepen gebruiken om het bedrag te berekenen op basis van de btw-boekingsinstellingen voor de groep. Zie [Btw-bedrijfsboekingsgroepen instellen](finance-setup-vat.md#set-up-vat-business-posting-groups) voor meer informatie.

Afhankelijk van wat u wilt doen, kunt u op de volgende manieren een btw-bedrijfsboekingsgroep toewijzen aan klanten of verkoopdocumenten:

* Als u voor alle klanten hetzelfde btw-tarief wilt gebruiken, kunt u een groep kiezen in het veld **Btw-bedrijfsboekingsgroep (Prijs)** veld op de pagina **Verkoopinstellingen**.
* Als u een btw-tarief wilt gebruiken voor een specifieke klant, kunt u een groep kiezen in het veld **Btw-bedrijfsboekingsgroep (Prijs)** op de pagina **Klantenkaart**. 
* Als u een btw-tarief wilt gebruiken voor een specifieke groep klanten, kunt u een groep kiezen in het veld **Btw-bedrijfsboekingsgroep (Prijs)** op de pagina **Klantenprijsgroep**. Dit is bijvoorbeeld handig wanneer u wilt dat een prijs geldt voor alle klanten in een bepaalde geografische regio of een specifieke branche.
* Op alle verkoopdocumenten in het veld **Btw-bedrijfsboekingsgroep**. Het btw-bedrag dat voor de groep is opgegeven, wordt alleen gebruikt voor het document waaraan u momenteel werkt.

> [!NOTE]
> Als u geen groep opgeeft in het veld **Btw-bedrijfsboekingsgroep (Prijs)**, is geen btw inbegrepen in de prijzen.

#### <a name="examples" />Voorbeelden

Factoren zoals het land of de regio waarin u verkoopt of het type bedrijfstakken waaraan u verkoopt, kunnen van invloed zijn op het btw-bedrag dat u moet verantwoorden. Een restaurant kan bijvoorbeeld 6% btw in rekening brengen voor maaltijden die in huis worden gegeten en 17% voor afhaalmaaltijden. Dit kunt u bereiken door een btw-bedrijfsboekingsgroep (prijs) te maken voor in huis en een andere voor afhaalmaaltijden.

## <a name="working-with-vat-date" />Werken met btw-datum

### <a name="vat-date-in-documents" />Btw-datum in documenten

Wanneer u nieuwe verkoop- of inkoopdocumenten maakt, is de **btw-datum** gebaseerd op de instelling in het veld **Standaard btw-datum** op de pagina **Grootboekinstellingen**. Deze standaardwaarde kan hetzelfde zijn als **Boekingsdatum** of **Documentdatum**. Als u een andere btw-datum nodig hebt, kunt u de waarde handmatig wijzigen in het veld **Btw-datum**. Wanneer u het document boekt, wordt de **btw-datum** weergegeven op het boekingsdocument en in de btw- en grootboekposten.

> [!NOTE]
> Als het veld **Btw-datum** niet beschikbaar is in uw documenten of dagboeken, betekent dit dat **Geen btw-datumfunctionaliteit gebruiken** is gekozen in het veld **Gebruik van btw-datum** op de pagina **Grootboekinstellingen**.  

> [!IMPORTANT]
> Als u **Btw-periode controleren** in de **Grootboekinstellingen** configureert als **Boeking in afgesloten periode blokkeren** of **Boeking in afgesloten periode blokkeren en waarschuwen bij vrijgave**, kunt u een document of journaal alleen boeken als de datum in het veld **Btw-datum** zich niet in een afgesloten periode in **Btw-aangifteperioden** bevindt. Zelfs als de periode in **Btw-aangifteperioden** open is, kunt u een waarschuwing krijgen op basis van de **Status van btw-aangifte** en de configuratie in **Btw-periode controleren**.

> [!IMPORTANT]
> U kunt het boeken van de **Btw-datum** voor een specifiek gegevensbereik voorkomen of toestaan met de velden **Boeken toegest. vanaf** en **Boeken toegest. tot** in de **Grootboekinstellingen** en de **Gebruikersinstellingen**.  

> [!NOTE]
> Als u de **Btw-datum** leeg laat, gebruikt [!INCLUDE [prod_short](includes/prod_short.md)] uw standaardinstelling uit **Standaard btw-datum** in de **Grootboekinstellingen** als een **Btw-datum** in de geboekte transactie.  

### <a name="modifying-the-vat-date-in-posted-entries" />De btw-datum wijzigen in geboekte posten

Indien nodig kunt u de btw-datum van geboekte documenten wijzigen. Als u de datum in het veld **Btw-datum** voor geboekte documenten wilt wijzigen, volgt u deze stappen:

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-posten** in en kies vervolgens de gerelateerde koppeling. 
2. Zoek de invoer met de onjuiste btw-datum.  
3. Klik de actie **Lijst bewerken** en voer de juiste datum in het veld **Btw-datum** in.  
4. Wanneer u de pagina sluit, verandert de btw-datum in gerelateerde **Grootboekposten** en in het geboekte document.  

> [!NOTE]
> U kunt het veld **Btw-datum** in **btw-posten** alleen wijzigen als uw huidige datum niet in een gesloten btw-aangifteperiode valt. Zelfs als de periode in **Btw-aangifteperioden** open is, kunt u een waarschuwing krijgen op basis van de **Status van btw-aangifte**.  

> [!NOTE]
> Als uw document meer dan één **btw-post** heeft, hoeft u alleen de waarde in het veld **Btw-datum** te wijzigen in één item met betrekking tot het document. Om boekingen consistent te houden, wijzigt [!INCLUDE[prod_short](includes/prod_short.md)] de btw-datum automatisch in btw-posten met betrekking tot deze transactie. [!INCLUDE [prod_short](includes/prod_short.md)] werkt de **btw-datum** in andere tabellen (GB-posten en documenten) bij, maar alleen gerelateerd aan deze transactie.  

## <a name="correcting-vat-amounts-manually-on-sales-and-purchase-documents" />Btw-bedragen handmatig corrigeren in verkoop- en inkoopdocumenten

U kunt btw-posten corrigeren die zijn geboekt zodat u de totale bedragen voor verkoop- of inkoop-btw kunt wijzigen zonder het btw-basisbedrag aan te passen. Bijvoorbeeld als u een factuur ontvangt van een leverancier met een onjuist btw-bedrag.  

Zelfs als u een of meer combinaties hebt ingesteld voor het afhandelen van import-BTW, moet u minimaal één btw-productboekingsgroep instellen. Deze kunt u bijvoorbeeld **CORRECT** noemen en voor correctiedoeleien gebruiken, tenzij u dezelfde grootboekrekening in het veld **Ink.-btw-rekening** op de regel btw-boekingsinstellingen kunt gebruiken. Zie [Berekeningen en boekingsmethoden voor btw instellen](finance-setup-vat.md) voor meer informatie.

Als u een contantkorting hebt berekend op basis van een factuurbedrag inclusief btw, kunt u de btw over de contantkorting terugboeken wanneer de contantkorting wordt verleend. U moet de optie **Aanpassen bij cont.-korting** zowel op het tabblad Algemeen in het venster Boekhoudinstellingen als in het venster Boekingsgroepinstellingen inschakelen, voor specifieke combinaties van btw-bedrijfsboekingsgroep en btw-productboekingsgroep.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-sales-documents" />Het systeem instellen voor handmatige btw-invoer in verkoopdocumenten
Hieronder wordt beschreven hoe u handmatige btw-wijzigingen in verkoopdocumenten kunt inschakelen. De stappen zijn vergelijkbaar op de pagina **Inkoopinstellingen**.

1. Geef op de pagina **Grootboekinstellingen** een waarde voor **Max. toegestaan btw-verschil** op tussen het bedrag dat door de toepassing wordt berekend en het handmatige bedrag.  
2. Schakel op de pagina **Verkoopinstellingen** het selectievakje **Btw-verschil toegestaan** in.  

### <a name="to-adjust-vat-for-a-sales-document" />Btw wijzigen voor een verkoopdocument

1. Open de betreffende verkooporder.  
2. Kies de actie **Statistieken**.  
3. Kies op het sneltabblad **Facturering** de waarde in het veld **Aantal btw-regels**.
4. Bewerk het veld **Btw-bedrag**.   

> [!NOTE]  
> Het totale btw-bedrag voor de factuur, gegroepeerd op btw-identificatie, wordt op de regels weergegeven. U kunt het bedrag handmatig wijzigen in het veld **Btw-bedrag** op de regels voor elke btw-identificatie. Wanneer u het veld **Btw-bedrag** wijzigt, controleert de toepassing of u de btw niet hebt gewijzigd met meer dan het bedrag dat u hebt opgegeven als het maximum toegestane verschil. Als het bedrag buiten het bereik valt van het **Max. toegestaan btw-verschil**, wordt een waarschuwing weergegeven waarin het maximum toegestane btw-verschil staat. U kunt pas doorgaan nadat u het bedrag hebt gewijzigd en dit binnen de aanvaardbare parameters valt. Klik op **OK** en geef een nieuw **btw-bedrag** op dat binnen het toegestane bereik valt. Als het btw-verschil kleiner dan of gelijk is aan het toegestane maximum, wordt de btw evenredig verdeeld over de documentregels met dezelfde btw-identificatie.  

## <a name="calculating-vat-manually-using-journals" />Btw handmatig berekenen met dagboeken
U kunt btw-bedragen ook aanpassen in algemene, verkoop- en inkoopdagboeken. Het is mogelijk nodig dit te doen wanneer u een leveranciersfactuur boekt in uw dagboek en er een verschil is tussen het btw-bedrag dat in [!INCLUDE[prod_short](includes/prod_short.md)] is berekend en het btw-bedrag in de leveranciersfactuur.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-a-general-journals" />Het systeem instellen voor handmatige btw-invoer in dagboeken
U moet de volgende stappen uitvoeren voordat u btw handmatig invoert in een dagboek.  

1. Geef op de pagina **Grootboekinstellingen** een waarde voor **Max. toegestaan btw-verschil** op tussen het bedrag dat door de toepassing wordt berekend en het handmatige bedrag.  
2. Schakel het selectievakje **Btw-verschil toegestaan** in voor het relevante dagboek op de pagina **Fin. dagboeksjablonen**.  

### <a name="to-set-the-system-up-for-manual-vat-entry-in-a-sales-and-purchase-journals" />Het systeem instellen voor handmatige btw-invoer in verkoop- en inkoopdagboeken

U moet de volgende stappen uitvoeren voordat u btw handmatig invoert in een verkoop- of inkoopdagboek.

1. Schakel op de pagina **Inkoopinstellingen** het selectievakje **Btw-verschil toegestaan** in.  
2. Herhaal stap 1 voor de pagina **Verkoopinstellingen**.
3. Nadat u de hierboven beschreven instellingen hebt voltooid, kunt u het veld **Btw-bedrag** corrigeren in de regel van het algemene dagboek of het veld **Btw-bedrag tegenrek.** in de verkoop- of inkoopdagboekregel. In [!INCLUDE[prod_short](includes/prod_short.md)] wordt gecontroleerd of het verschil niet groter is dan het opgegeven maximum.  

> [!NOTE]  
> Als het verschil groter is, wordt een waarschuwing weergegeven waarin het maximum toegestane btw-verschil wordt aangegeven. Als u wilt doorgaan, moet u het bedrag wijzigen. Kies **OK** en geef een bedrag op dat binnen het toegestane bereik valt. Als het btw-verschil kleiner dan of gelijk is aan het toegestane maximum, wordt het verschil in [!INCLUDE[prod_short](includes/prod_short.md)] weergegeven in het veld **Btw-verschil**.  

## <a name="posting-import-vat-with-purchase-invoices" />Import-btw boeken met inkoopfacturen
In plaats van dagboeken te gebruiken om een import-btw-factuur te boeken, kunt u een inkoopfactuur gebruiken.  

### <a name="to-set-up-purchasing-for-posting-import-vat-invoices" />Inkopen instellen voor het boeken van import-btw-facturen

1. Een leverancierskaart instellen voor de importinstantie die u de import-btw-factuur stuurt. De **Bedrijfsboekingsgroep** en **Btw-bedrijfsboekingsgroep** moeten worden ingesteld op dezelfde manier als de grootboekrekening voor import-btw.  
2. Maak een **Prod.-boekingsgroep** voor de invoerbelasting en stel een **btw-productboekingsgroep** voor invoer-btw in voor de bijbehorende **Prod.-boekingsgroep**.  
3. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema** in en kies de gerelateerde koppeling.  
4. Selecteer de grootboekrekening voor het importeren van btw en kies de actie **Bewerken**.  
5. Selecteer op het sneltabblad **Boeken** de instelling van de **Productboekingsgroep** voor import-btw. [!INCLUDE[prod_short](includes/prod_short.md)] vult automatisch het veld **Btw-productboekingsgroep** in.  
6. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Boekingsgroepinstellingen** in en kies vervolgens de gerelateerde koppeling.  
7. Maak een combinatie van **Bedrijfsboekingsgroep** voor de btw-instantie en **Alg. prod. bkgr.** voor invoer-btw. Selecteer voor deze nieuwe combinatie in het veld **Ink.-rekening** de grootboekrekening voor invoer-btw.  

### <a name="to-create-a-new-invoice-for-the-import-authority-vendor-once-you-have-completed-the-setup" />Een nieuwe factuur voor de importinstantieleverancier maken na het voltooien van de instelling

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Inkoopfacturen** in en kies vervolgens de gerelateerde koppeling.  
2. Maak een nieuwe inkoopfactuur.  
3. Selecteer in het veld **Orderleveranciersnr.** de importinstantieleverancier en kies vervolgens de knop **OK**.  
4. Selecteer op de inkoopregel in het veld **Soort** de optie **Grootboekrekening** en selecteer in het veld **Nr.** de grootboekrekening voor invoer-btw.  
5. Typ **1** in het veld **Aantal** .  
6. Geef het btw-bedrag op in het veld **Directe kostprijs Excl. btw**.  
7. Boek de factuur.  

## <a name="processing-certificates-of-supply" />Certificaten van levering verwerken

Wanneer u goederen aan een klant in een ander EU-land/-regio verkoopt, moet u de klant een certificaat van levering sturen dat de klant moet ondertekenen en aan u moet retourneren. De volgende procedures zijn voor het verwerken van certificaten van levering voor verkoopverzendingen, maar dezelfde stappen gelden voor serviceverzendingen van artikelen en retourzendingen aan leveranciers.  

### <a name="to-view-certificate-of-supply-details" />Details van een certificaat van levering weergeven
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Geboekte verkoopverzendingen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de relevante verkoopverzending aan een klant in een ander EU-land of een andere EU-regio.  
3. Kies **Details certificaat van levering**.  
4. Als in de instelling van de btw-boekingsgroep voor de klant het selectievakje **Certificaat van levering vereist** is ingeschakeld, is het veld **Status** standaard ingesteld op **Vereist**. U kunt het veld bijwerken om aan te geven of de klant het certificaat heeft geretourneerd.  

> [!Note]  
>  Als in de instelling van de btw-boekingsgroepsinstelling het selectievakje **Certificaat van levering vereist** niet is ingeschakeld, wordt een record gemaakt en wordt het veld **Status** ingesteld op **Niet van toepassing**. U kunt het veld bijwerken om de juiste statusinformatie weer te geven. U kunt de status indien nodig handmatig van **Niet van toepassing** instellen op **Vereist** en van **Vereist** op **Niet van toepassing**.  

   Wanneer u het veld **Status** instelt op **Vereist**, **Ontvangen** of **Niet ontvangen**, wordt een certificaat gemaakt.  

> [!TIP]  
>  U kunt de pagina **Certificaten van levering** gebruiken om een weergave te krijgen van de status van alle geboekte verzendingen waarvoor een certificaat van levering is gemaakt.  

5. Kies **Certificaat van levering afdrukken**.  

> [!Note]  
>  U kunt een voorbeeld van het document bekijken of het document afdrukken. Wanneer u **Certificaat van levering afdrukken** kiest en het document afdrukt, wordt het selectievakje **Afgedrukt** automatisch ingeschakeld. Als het nog niet is opgegeven, wordt de status van het certificaat bovendien ingesteld op **Vereist**. Zo nodig neemt u het afgedrukte certificaat in de verzending op.  

### <a name="to-print-a-certificate-of-supply" />Een certificaat van levering afdrukken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Geboekte verkoopverzendingen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de relevante verkoopverzending aan een klant in een ander EU-land of een andere EU-regio.  
3. Kies de actie **Certificaat van levering afdrukken**.  

> [!NOTE]  
>  U kunt ook een certificaat afdrukken vanaf de pagina **Certificaat van levering**.  

4. Als u informatie uit de regels in het verzenddocument wilt opnemen in het certificaat, schakelt u het selectievakje **Regeldetails afdrukken** in.  
5. Schakel het selectievakje **Certificaten van levering maken als deze nog niet zijn gemaakt** in om [!INCLUDE[prod_short](includes/prod_short.md)]-certificaten te maken voor geboekte verzendingen die er op het moment van uitvoering geen hebben. Wanneer u het selectievakje inschakelt, worden nieuwe certificaten gemaakt voor alle geboekte verzendingen die geen certificaten in het geselecteerde bereik hebben.  
6. De filterinstellingen zijn standaard voor het verzenddocument dat u hebt geselecteerd. Vul de filterinformatie in om een specifiek certificaat van levering te selecteren dat u wilt afdrukken.  
7. Kies op de pagina **Certificaat van levering** de actie **Afdrukken** om het rapport af te drukken of kies de actie **Voorbeeld** om deze weer te geven.  

> [!Note]  
> Het veld **Status van certificaat van levering** en het veld **Afgedrukt** worden bijgewerkt voor de verzending op de pagina **Certificaten van levering**.  

8. Verzend het afgedrukte certificaat van levering ter ondertekening naar de klant.  

### <a name="to-update-the-status-of-a-certificate-of-supply-for-a-shipment" />De status van een certificaat van levering voor een verzending bijwerken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Geboekte verkoopverzendingen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de relevante verkoopverzending aan een klant in een ander EU-land of een andere EU-regio.  
3. Kies in het veld **Status** de relevante optie.  

   Als de klant het ondertekende certificaat van levering heeft geretourneerd, kiest u **Ontvangen**. Het veld **Ontvangstdatum** wordt automatisch bijgewerkt. Standaard wordt de ontvangstdatum ingesteld op de huidige werkdatum.  

   U kunt de datum wijzigen in de datum waarop u het ondertekende certificaat van levering van de klant hebt ontvangen. U kunt ook een koppeling naar het ondertekende certificaat maken met standaard [!INCLUDE[prod_short](includes/prod_short.md)]-koppeling.  

   Als de klant het ondertekende certificaat van levering niet retourneert, kiest u **Niet ontvangen**. U moet de klant dan een nieuwe factuur sturen waarin btw is inbegrepen, omdat de oorspronkelijke factuur niet door de belastingdienst wordt geaccepteerd.  

Als u een groep certificaten wilt weergeven, begint u op de pagina **Certificaten van levering** en werkt u de informatie over de status van openstaande certificaten bij wanneer u ze terug ontvangt van uw klanten. Dit kan handig zijn als u wilt zoeken naar alle certificaten die een bepaalde status hebben, bijvoorbeeld **Vereist**, waarvoor u de status wilt bijwerken naar **Niet ontvangen**.  

### <a name="to-update-the-status-of-a-group-of-certificates-of-supply" />De status van een groep certificaten bijwerken

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Certificaten van levering** in en kies vervolgens de gerelateerde koppeling.  
2. Filter het veld **Status** op de waarde die u wilt om de lijst met certificaten te maken die u wilt beheren.  
3. Als u de statusinformatie wilt bijwerken, kiest u **Lijst bewerken**  
4. Kies in het veld **Status** de relevante optie.  

   Als de klant het ondertekende certificaat van levering heeft geretourneerd, kiest u **Ontvangen**. Het veld **Ontvangstdatum** wordt automatisch bijgewerkt. Standaard wordt de ontvangstdatum ingesteld op de huidige werkdatum.  

   U kunt de datum wijzigen in de datum waarop u het ondertekende certificaat van levering hebt ontvangen. U kunt ook een koppeling naar het ondertekende certificaat toevoegen met de standaardkoppeling voor documenten in [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]
> U kunt geen nieuw certificaat van levering op de pagina **Certificaat van levering** maken als u ernaar toe navigeert met deze procedure. Als u een certificaat wilt maken voor een verzending die geen certificaat vereist, opent u de geboekte verkoopverzending en gebruikt u een van de twee hierboven beschreven procedures:  
>
> * Handmatig een certificaat van levering maken  
> * Een certificaat van levering afdrukken.

## <a name="see-related-microsoft-trainingtrainingpathsprocess-vat-dynamics--business-central" />Zie gerelateerde [Microsoft-training](/training/paths/process-vat-dynamics-365-business-central/)

## <a name="see-also" />Zie ook

[Berekeningen en boekingsmethoden voor btw instellen](finance-setup-vat.md)  
[Btw-aangifte doen bij een belastingdienst](finance-how-report-vat.md)  
[Een btw-nummer valideren.](finance-how-validate-vat-registration-number.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
