---
title: Btw instellen
description: 'Controleer of u btw voor verkopen en inkopen op de juiste wijze berekent, boekt en aangeeft. Het is raadzaam de begeleide instelling te gebruiken om btw in te stellen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'VAT, posting, tax, value-added tax'
ms.search.form: '10, 118, 391, 470, 471, 472, 575, 734, 747, 748, 1877,'
ms.date: 01/31/2023
ms.author: bholtorf
---

# <a name="set-up-calculations-and-posting-methods-for-value-added-tax"></a>Berekeningen en boekingsmethoden voor btw instellen

Consumenten en bedrijven betalen btw wanneer deze goederen of services inkopen. Het bedrag dat aan btw moet worden betaald, is afhankelijk van een aantal factoren. In [!INCLUDE[prod_short](includes/prod_short.md)] stelt u btw in om de tarieven op te geven die moeten worden gebruikt om belastingbedragen te berekenen op basis van de volgende parameters:

* Aan wie u verkoopt  
* Van wie u koopt  
* Wat u verkoopt  
* Wat u koopt  

U kunt handmatig btw-berekeningen instellen, maar dit kan lastig en tijdrovend zijn. Dat komt doordat het erg gemakkelijk is per ongeluk andere btw-tarieven te gebruiken en onjuiste btw-gerelateerde rapporten te maken. Om het instellen van de btw te vergemakkelijken, raden we u aan de begeleide instelling **Btw instellen** te gebruiken die bij het product wordt geleverd. 

Als u echter de btw-berekeningen zelf wilt instellen of alleen meer informatie wilt over elke stap, bevat dit artikel beschrijvingen van elke stap:  

[!INCLUDE [finance-vat](includes/finance-vat.md)]

## <a name="set-up-vat-using-the-assisted-setup-guide-recommended"></a>Btw instellen met behulp van de begeleide instelling (aanbevolen)

> [!NOTE]
> U kunt de begeleide instelling **Btw instellen** alleen gebruiken als u een *Mijn bedrijf* hebt gemaakt en geen transacties hebt geboekt die inclusief btw zijn.

Ga als volgt te werk om de begeleide instelling te starten:

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), en voer **Begeleide instelling** in. 
2. Kies **Btw instellen** en voer de stappen uit.
3. Wanneer u de begeleide instelling hebt voltooid, gaat u naar de pagina **Btw-boekingsgroepinstellingen** en controleert u of u meer velden moet invullen volgens de lokale vereisten in uw versie van [!INCLUDE [prod_short](includes/prod_short.md)]. Meer informatie op [Lokale functionaliteit in Business Central](about-localization.md)  

### <a name="check-the-vat-posting-setup"></a>De btw-boekingsinstellingen controleren

Om uw snelle start te ondersteunen informeert [!INCLUDE [prod_short](includes/prod_short.md)] u over ontbrekende grootboekrekeningen in boekingsgroepen of boekingsinstellingen, zoals op de pagina **Btw-boekingsinstellingen**. U kunt dit type bericht in- of uitschakelen met *Grootboekrekening ontbreekt in boekingsgroep of instelling* op de pagina **Mijn berichten**. Ga simpelweg naar de pagina **Mijn instellingen** en kies de optie *Wijzigen wanneer ik berichten ontvang*. koppeling.  

Als u voor een dergelijke melding kiest, maakt [!INCLUDE [prod_short](includes/prod_short.md)] automatisch die boekingsinstellingen op basis van de boekingsgroepen in het document of journaal waaraan u momenteel werkt.  

Op dit punt kunt u gewoon de ontbrekende grootboekrekeningen invullen. Later, wanneer u de instellingen verder verfijnt, realiseert u zich echter misschien dat deze initiële instelling onjuist was. En [!INCLUDE [prod_short](includes/prod_short.md)] staat het verwijderen van btw-boekingsinstellingen en algemene boekingsinstellingen niet toe wanneer er boekingen zijn gemaakt op basis van dergelijke configuraties. Dus vanaf releasewave 1 in 2022 kunt u het veld **Geblokkeerd** op de pagina **Btw-boekingsgroepinstellingen** gebruiken om te voorkomen dat gebruikers per ongeluk een instelling gebruiken die niet langer relevant is voor nieuwe boekingen.

## <a name="set-up-a-default-vat-date-for-documents-and-journals"></a>Een standaard btw-datum instellen voor documenten en dagboeken

Btw aangifte in [!INCLUDE [prod_short](includes/prod_short.md)] is gebaseerd op de **btw-datum** om btw-posten in btw-aangiften in een btw-periode op te nemen. De btw-datum kan op alle documenten en dagboeken worden gewijzigd, maar u moet een standaardwaarde voor de btw-datum opgeven.

> [!NOTE]
> Na het boeken van het document of dagboek wordt de **btw-datum** weergegeven in **btw-posten** en **grootboekposten**, evenals op het geboekte document indien aanwezig.

Volg deze stappen om een standaardwaarde voor een btw-datum in te stellen:

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), en voer **Grootboekinstellingen** in. Kies vervolgens de gerelateerde koppeling.  
2. Kies op het sneltabblad **Algemeen**, in het veld **Standaard btw-datum** de optie **Boekingsdatum** of **Documentdatum**.
3. De pagina sluiten.  

> [!NOTE]
> Standaard is de **standaard-btw-datum** gelijk aan de **boekingsdatum**.

### <a name="enabling-or-disabling-the-vat-date-feature"></a>De functie btw-datum in- of uitschakelen

Sommige landen/regio's vereisen dat bedrijven een specifieke btw-datum gebruiken, maar andere landen/regio's niet. Sommige landen/regio's vereisen ook dat bedrijven de btw-datum in specifieke situaties wijzigen nadat ze documenten hebben geboekt, maar andere landen/regio's staan geen wijzigingen in btw-datums toe. Om rekening te houden met verschillende contexten kunt u kiezen of u deze functionaliteit wilt gebruiken en zo ja, in welke mate.

Volg deze stappen om het niveau van btw-datumgebruik in te stellen:

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), en voer **Grootboekinstellingen** in. Kies vervolgens de gerelateerde koppeling.  
2. Geef op het sneltabblad **Algemeen** in het veld **Gebruik van btw-datum** op in welke mate u de btw-datumfunctie wilt gebruiken. U kunt een van de volgende opties kiezen:

| Soort | Omschrijving |
|--------------------|-----------------------------------------|
| **Volledige btw-datumfunctionaliteit gebruiken** | Alles met betrekking tot **btw-datum** werkt standaard, waardoor u de maximale **btw-datum** functionaliteit krijgt. U kunt de datum instellen, wijzigen in documenten, op basis daarvan rapporteren en de datum na boeking wijzigen, zolang de periode niet is afgesloten of beschermd met toegestane boekingsdatums. |
| **Gebruiken maar geen wijzigingen toestaan** | Alles met betrekking tot **btw-datum** werkt standaard, met één uitzondering. U kunt de **btw-datum** in **btw-posten** niet wijzigen. |
| **Geen btw-datumfunctionaliteit gebruiken** | [!INCLUDE [prod_short](includes/prod_short.md)] zal de **btw-datum**-velden verbergen en niet beschikbaar maken voor documenten, dagboeken en boekingen. De **standaard btw-datum** wordt geconfigureerd als de **boekingsdatum**. |

3. De pagina sluiten.

> [!IMPORTANT]
> Zelfs als u de optie **Geen btw-datumfunctionaliteit gebruiken** kiest, gebruikt [!INCLUDE [prod_short](includes/prod_short.md)] de **btw-datum** op de achtergrond. Omdat de **standaard btw-datum** is geconfigureerd als de **boekingsdatum** en u deze in dit geval niet kunt wijzigen, krijgt u dezelfde ervaring als zonder deze functie. **Btw-datum**-velden worden verwijderd van alle pagina's, maar dit veld blijft bestaan in tabellen en rapporten werken op basis daarvan.

### <a name="limiting-periods-for-posting-and-changing-the-vat-date"></a>Beperkende termijnen voor het boeken en wijzigen van de btw-datum

U kunt voorkomen dat mensen btw-boekingen in specifieke datumbereiken boeken of wijzigen. U stelt de beperking in met behulp van twee instellingen:

* Op basis van gesloten **btw-aangifteperiode**
* Gebaseerd op de velden **Boeken toegest. vanaf** en **Boeken toegest. tot** .

#### <a name="to-limit-posting-based-on-vat-return-period"></a>Boeking beperken op basis van btw-aangifteperiode

1. Kies het pictogram ![Lampje dat de functie Vertel me opent 1.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Grootboekinstellingen** in en kies vervolgens de gerelateerde koppeling.  
2. Geef op het **Algemeen** sneltabblad in het veld **Btw-periode controleren** de mate van controle van de btw-aangifteperiode op. De volgende tabel beschrijft de opties.

| Soort | Omschrijving |
|--------------------|-----------------------------------------|
| **Boeking in afgesloten periode blokkeren en waarschuwen bij vrijgave** | Voorkom dat mensen een document of dagboek boeken of btw-boekingen wijzigen met een btw-datum binnen een gesloten **btw-aangifteperiode**. [!INCLUDE [prod_short](includes/prod_short.md)] zal ook een waarschuwing tonen als uw **btw-aangifteperiode** open is, maar de status van **btw-aangifte** **Vrijgegeven** of **Verzonden** is. |
| **Boeking in afgesloten periode blokkeren** | Voorkom dat mensen een document of dagboek boeken of btw-boekingen wijzigen met een btw-datum binnen de gesloten **btw-aangifteperiode**. |
| **Waarschuwen bij boeking in afgesloten periode** | Geef een waarschuwing weer, maar blokkeer het boeken niet als u een document of journaal wilt boeken met een btw-datum binnen een gesloten **btw-aangifteperiode**. |
| **Uitgeschakeld** | Geen actie ondernemen op basis van een afgesloten **btw-aangifteperiode**. |

#### <a name="to-limit-posting-based-on-allow-fromto-period"></a>Om boeken te beperken op basis van Toegest. vanaf/tot-periode

U kunt beperkingen instellen op bedrijfs- of specifieke gebruikersniveaus.

Alle boekingen voor het hele bedrijf beperken:

1. Kies het pictogram ![Lampje dat de functie Vertel me opent 1.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Grootboekinstellingen** in en kies vervolgens de gerelateerde koppeling.  
2. Geef op het sneltabblad **Algemeen** in het veld **Boeken toegest. vanaf** de btw-datum op vanaf wanneer u boekingen toestaat. Het boeken van een document of dagboek met een btw-datum vóór deze datum is niet toegestaan.  
3. Geef op het sneltabblad **Algemeen** in het veld **Boeken toegest. tot** de btw-datum tot wanneer u boekingen toestaat. Het boeken van een document of dagboek met een btw-datum na deze datum is niet toegestaan.

Boeking voor de specifieke gebruiker beperken:

1. Kies het pictogram ![Lampje dat de functie Vertel me opent 1.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikersinstellingen** in en kies vervolgens de gerelateerde koppeling.  
2. Geef in het veld **Gebruikers-id** de gebruiker op die u toestemming wilt geven om in een bepaalde periode te boeken.  
3. Geef in het veld **Boeken toegest. vanaf** de btw-datum op vanaf wanneer u boekingen toestaat. Het boeken van een document of dagboek met een btw-datum vóór deze datum is niet toegestaan.
4. Geef in het veld **Boeken toegest. tot** de btw-datum op tot wanneer u boekingen toestaat. Het boeken van een document of dagboek met een btw-datum na deze datum is niet toegestaan.

## <a name="set-up-vat-registration-numbers-for-your-country-or-region"></a>Btw-nummers instellen voor uw land/regio

Als u ervoor wilt zorgen dat gebruikers geldige btw-nummers invoeren, kunt u notaties definiëren voor de btw-nummers die worden gebruikt in de landen of regio's waar u zaken doet. [!INCLUDE[prod_short](includes/prod_short.md)] geeft een foutbericht weer wanneer iemand een fout maakt of een notatie gebruikt die onjuist is voor het land/regio.

Als u btw-nummers wilt instellen, gaat u als volgt te werk:

1. Kies het pictogram ![Lampje dat de functie Vertel me 2 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Landen/regio's** in.
2. Kies het land/regio, en kies de actie **Btw-nummernotaties**.
3. Definieer in het veld **Notaties** de notatie door een of meer van de volgende tekens in te voeren:  

* **#** Vereist een getal van één cijfer.  
* **@** Vereist een letter. Deze notatie is niet hoofdlettergevoelig.  
* **?** Staat elk teken toe.  

    > [!TIP]
    > U kunt andere tekens gebruiken zolang deze aanwezig zijn in de notatie van het land/regio. Als u dus een punt of een streepje wilt opnemen in een reeks cijfers, kunt u de notatie definiëren als ##.####.### of @@-###-###.  

## <a name="set-up-vat-business-posting-groups"></a>Btw-bedrijfsboekingsgroepen instellen

Met btw-bedrijfsboekingsgroepen worden de markten vertegenwoordigd waarin u zaken doet met klanten en leveranciers en wordt bepaald hoe u btw in elke markt berekent en boekt. Voorbeelden van btw-bedrijfsboekingsgroepen zijn **Binnenlands** en **Europese Unie (EU)**.  

Gebruik codes die eenvoudig te onthouden zijn en die de bedrijfsboekinggroep beschrijven, zoals **EU**, **Niet-EU** of **Binnenlands**. Elke code moet uniek zijn dus u kunt zoveel codes instellen als u nodig hebt, maar u kunt dezelfde code niet meer dan één keer in een tabel gebruiken.

Ga als volgt te werk om een btw-groep voor zakelijke boekingen in te stellen:

1. Kies het pictogram ![Lampje dat de functie Vertel me 3 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-bedrijfsboekingsgroepen** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de vereiste velden in.

U kunt standaard btw-bedrijfsboekingsgroepen instellen door deze aan bedrijfsboekingsgroepen te koppelen. [!INCLUDE[prod_short](includes/prod_short.md)] wijst de btw-bedrijfsboekingsgroep automatisch toe wanneer u de bedrijfsboekingsgroep toewijst aan een klant, leverancier of grootboekrekening.

## <a name="set-up-vat-product-posting-groups"></a>Btw-productboekingsgroepen instellen

Met btw-productboekingsgroepen worden de artikelen en resources vertegenwoordigd die u koopt of verkoopt en wordt bepaald hoe btw wordt berekend en geboekt volgens het soort artikel of resource.

Het is aan te raden codes te gebruiken die u gemakkelijk kunt onthouden en waarmee het tarief wordt beschreven, zoals **Geen btw** of **Nul**, **Btw10** of **Gereduceerd** voor 10 procent btw en **Btw25** of **Standaard** voor 25 procent.

Ga als volgt te werk om een btw-groep voor zakelijke boekingen in te stellen:

1. Kies het pictogram ![Lampje dat de functie Vertel me 4 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-bedrijfsboekingsgroepen** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de vereiste velden in.

## <a name="combine-vat-posting-groups-in-vat-posting-setups"></a>Btw-boekingsgroepen in btw-boekingsinstellingen combineren

In [!INCLUDE[prod_short](includes/prod_short.md)] worden btw-bedragen berekend op verkopen en inkopen op basis van btw-boekingsinstellingen, die combinaties zijn van btw-bedrijfsboekingsgroepen en btw-productboekingsgroepen. Voor elke combinatie kunt u het btw-percentage, het soort btw-berekening en grootboekrekeningen opgeven voor het boeken van btw voor verkopen, inkopen en btw-verlegging. U kunt ook opgeven of btw moet worden herberekend wanneer een betalingskorting wordt toegepast of ontvangen.  

U kunt zo veel combinaties instellen als u nodig hebt. Als u combinaties van btw-boekingsinstellingen met soortgelijke kenmerken wilt groeperen, kunt u een **Btw-identificatie** definiëren voor elke groep en de identificatie toewijzen aan de groepsleden.

Ga als volgt te werk om btw-boekingsinstellingen te combineren:

1. Kies het pictogram ![Lampje dat de functie Vertel me opent 5.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **VAT-e-mailinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Vul de vereiste velden in. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

## <a name="assign-vat-posting-groups-by-default-to-multiple-entities"></a>Standaard btw-boekingsgroepen toewijzen aan meerdere entiteiten

Als u dezelfde btw-boekingsgroepen op meerdere entiteiten wilt toepassen, kunt u [!INCLUDE[prod_short](includes/prod_short.md)] instellen om dat standaard te doen. Er zijn enkele manieren om dit te doen:

* U kunt btw-bedrijfsboekingsgroepen toewijzen aan algemene bedrijfsboekingsgroepen of klant- of leveranciersjablonen
* U kunt btw-productboekingsgroepen in algemene productboekingsgroepen toewijzen  

De btw-bedrijfsboekingsgroep of btw-productboekingsgroep wordt toegewezen wanneer u een bedrijfs- of productboekingsgroep voor een klant, leverancier, artikel of resource kiest.

## <a name="assign-vat-posting-groups-to-accounts-customers-vendors-items-and-resources"></a>Btw-boekingsgroepen toewijzen aan accounts, klanten, leveranciers, artikelen en resources

In de volgende gedeelten wordt beschreven hoe u btw-boekingsgroepen aan afzonderlijke entiteiten kunt toewijzen.

### <a name="to-assign-vat-posting-groups-to-individual-general-ledger-accounts"></a>Btw-boekingsgroepen toewijzen aan afzonderlijke grootboekrekeningen

1. Kies het pictogram ![Lampje dat de functie Vertel me opent 6.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rekeningschema** in en kies de gerelateerde koppeling.  
2. Open de **Grootboekrekening** voor de rekening.  
3. Kies op het sneltabblad **Boeken** in het veld **Algemeen boekingssoort** **Verkoop** of **Inkoop**.  
4. Kies de btw-boekingsgroepen die u wilt gebruiken voor de verkoop- of inkooprekening.  

### <a name="to-assign-vat-business-posting-groups-to-customers-and-vendors"></a>Btw-bedrijfsboekingsgroepen toewijzen aan klanten en leveranciers

1. Kies het pictogram ![Lampje dat de functie Vertel me opent 7.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klant** of **Leverancier** in en kies vervolgens de gerelateerde koppeling.  
2. Vouw op de kaart **Klant** of **Leverancier** het sneltabblad **Facturering** uit.  
3. Kies de btw-bedrijfsboekingsgroep.  

### <a name="to-assign-vat-product-posting-groups-to-individual-items-and-resources"></a>Btw-productboekingsgroepen toewijzen aan afzonderlijke artikelen en resources.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent 8.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikel** of **Bron** in en kies vervolgens de gerelateerde koppeling.  
2. Ga op een van de volgende manieren te werk:  

    * Vouw op de **Artikel**kaart het sneltabblad **Prijs en boeking** uit en kies vervolgens **Meer weergeven** om het veld **Btw-productboekingsgroep** weer te geven.  
    * Vouw op de kaart **Resource** het sneltabblad **Facturering** uit.  
3. Kies de btw-productboekingsgroep.  

## <a name="set-up-clauses-to-explain-vat-exemption-or-non-standard-vat-rates"></a>Clausules instellen om btw-vrijstelling of niet-standaard btw-tarieven uit te leggen

U stelt een btw-clausule in om informatie te geven over het soort btw dat wordt toegepast. De informatie kan nodig zijn voor overheidsregelgeving. Nadat u een btw-clausule hebt ingesteld en deze hebt gekoppeld aan een btw-boekingsinstelling, wordt de btw-clausule weergegeven op afgedrukte verkoopdocumenten waarin de btw-boekingsinstellingengroep wordt gebruikt.

Indien nodig kunt u ook opgeven hoe u btw-clausules naar andere talen vertaalt. Vervolgens wordt wanneer u een verkoopdocument maakt dat een btw-identificatie bevat, de vertaalde btw-clausule in het afgedrukte document opgenomen. De taalcode die op de klantkaart is opgegeven, bepaalt de gebruikte taal.

Wanneer in verschillende soorten documenten (bijvoorbeeld facturen of creditnota's) niet-standard btw-tarieven worden gebruikt, moeten bedrijven meestal een vrijstellingstekst (btw-clausule) bijvoegen waarin wordt uitgelegd waarom een verlaagd btw-tarief wordt gehanteerd of waarom het bedrijf van btw is vrijgesteld. U kunt per type document verschillende btw-clausules voor uw bedrijfsdocumenten definiëren, zoals een factuur of creditnota. U doet dit op de pagina **Btw-clausules per documenttype**.

U kunt een btw-clausule wijzigen of verwijderen, en uw wijzigingen worden in een gegenereerde lijst weergegeven. [!INCLUDE[prod_short](includes/prod_short.md)] houdt echter geen historie van de wijziging bij. Op de lijst worden de omschrijvingen van btw-clausules afgedrukt en weergegeven voor alle regels in de lijst naast het btw-bedrag en het btw-basisbedrag. Als er geen btw-clausule is gedefinieerd voor de regels op het verkoopdocument, wordt het hele gedeelte weggelaten wanneer de lijst wordt afgedrukt.

### <a name="to-set-up-vat-clauses"></a>Btw-clausules instellen

1. Kies het pictogram ![Lampje dat de functie Vertel me opent 9.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-clausules** in en kies vervolgens de gerelateerde koppeling.  
2. Maak een nieuwe regel op de pagina **Btw-clausules**.  
3. Voer in het veld **Code** een ID voor de clausule in. U gebruikt deze code om de clausule toe te wijzen aan btw-boekingsgroepen.  
4. Voer in het veld **Omschrijving** tekst voor de btw-vrijstelling die u wilt weergeven in documenten waarop btw-bedragen kunnen worden vermeld. Geef indien nodig in het veld **Omschrijving 2** meer tekst op. De tekst wordt weergegeven in nieuwe documentregels.
5. Kies de actie **Omschrijving per documenttype**.
6. Vul op de pagina **Btw-clausules per documenttype** de velden in waarmee u wilt aangeven welke btw-tekst moet worden weergegeven voor welk documenttype.  
7. Optioneel: als u de btw-clausule direct wilt toewijzen aan de instelling van btw-boekingen, kiest u **Setup** en daarna de clausule. Als u dit niet direct wilt doen, kunt u de clausule later toevoegen op de pagina **Btw-boekingen instellen**.  
8. Optioneel: als u wilt opgeven hoe de btw-clausule moet worden vertaald, kiest u de actie **Vertalingen**.

### <a name="to-assign-a-vat-clause-to-a-vat-posting-setup"></a>Een btw-clausule aan een btw-boekingsgroepinstelling toewijzen

1. Kies het pictogram ![Lampje dat de functie Vertel me opent 10.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **VAT-e-mailinstellingen** in en kies vervolgens de gerelateerde koppeling.  
2. Kies in de kolom **Btw-clausule** de clausule die u wilt gebruiken voor elke btw-boekingsinstelling waarop deze van toepassing is.  

### <a name="to-specify-translations-for-vat-clauses"></a>Vertalingen opgeven voor btw-clausules

1. Kies het pictogram ![Lampje dat de functie Vertel me opent 11.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-clausules** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Vertalingen**.  
3. Kies in het veld **Taalcode** de taal waarin u vertaalt.  
4. Voer de vertalingen van de omschrijvingen in de velden **Omschrijving** en **Omschrijving 2** in. Deze tekst wordt weergegeven in de vertaalde btw-rapportdocumenten.  

### <a name="to-specify-extended-text-for-vat-clauses"></a>Uitgebreide tekst voor btw-clausules specificeren

> [!NOTE]  
> Als uw land/regio langere tekst voor de btw-clausules vereist dan de standaardversie ondersteunt, kunt u de langere tekst voor de btw-clausules opgeven als *uitgebreide tekst* zodat deze wordt afgedrukt op de verkoop- en inkooprapporten.  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent 11.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-clausules** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Uitgebreide teksten**.  
3. Kies de actie **Nieuw**.  
4. Vul de velden **Taalcode** en **Omschrijving** in.  
5. Selecteer desgewenst het veld **Alle taalcodes** of geef de relevante taal op in het veld **Taalcode** als u taalcodes gebruikt.  
6. Vul de velden **Begindatum** en **Einddatum** in als u een beperking wilt instellen voor de data waarop de tekstuitbreiding kan worden gebruikt.  
7. Schrijf op de **Tekst**-regels de uitgebreide tekst voor uw btw-clausules.  
8. Schakel de relevante velden in voor de documentsoorten waarvoor u de uitgebreide tekst wilt afdrukken.  
9. De pagina sluiten.  

## <a name="create-a-vat-posting-setup-to-handle-import-vat"></a>Een btw-boekingsinstelling maken om import-btw te verwerken

U gebruikt de functie *Import-btw* wanneer u een document moet boeken waarbij het volledige bedrag btw is. U gebruikt dit als u een factuur van de belastingdienst ontvangt voor btw op geïmporteerde goederen.  

Ga als volgt te werk om codes voor import-btw in te stellen:  

1. Kies het pictogram ![Lampje dat de functie Vertel me opent 12.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Btw-bedrijfsboekingsgroepen** in en kies vervolgens de gerelateerde koppeling.  
2. Stel op de pagina Btw-productboekingsgroepen een nieuwe btw-productboekingsgroep in voor import-btw.  
3. Kies het pictogram ![Lampje dat de functie Vertel me opent 13.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **VAT-e-mailinstellingen** in en kies vervolgens de gerelateerde koppeling.  
4. Open de pagina Btw-boekingsinstellingen, maak een nieuwe regel of gebruik een bestaande btw-bedrijfsboekingsgroep in combinatie met de nieuwe btw-productboekingsgroep voor import-btw.  
5. Kies in het veld **Btw-berekening** **Volledig**.  
6. Voer in het veld **Inkoop-btw-rekening** de grootboekrekening in die moet worden gebruikt om import-btw te boeken. Alle andere rekeningen zijn optioneel.  

## <a name="use-reverse-charge-vat-for-trade-between-eu-countries-or-regions"></a>Verlegging van btw gebruiken voor handel tussen EU-landen of -regio's

Sommige bedrijven moeten verlegging van btw gebruiken wanneer zaken worden gedaan met andere bedrijven. Deze regel is bijvoorbeeld van toepassing op inkopen van EU-landen/-regio's en verkopen aan EU-landen/-regio's.  

> [!NOTE]  
> Deze regel geldt wanneer u zakendoet met bedrijven die in een ander EU-land/-regio btw-plichtig zijn. Als u rechtstreeks zakendoet met consumenten in andere EU-landen/-regio's, moet u contact opnemen met de belastingdienst over de geldende btw-regels.  

> [!TIP]  
> U kunt controleren of een bedrijf btw-plichtig is in een ander EU-land/regio door de EU-service voor btw-nummervalidatie te gebruiken. De service is gratis beschikbaar in [!INCLUDE[prod_short](includes/prod_short.md)]. Zie voor meer informatie [Btw-nummers controleren](finance-how-validate-vat-registration-number.md).

### <a name="sales-to-eu-countries-or-regions"></a>Verkopen aan EU-landen of -regio's

Btw wordt niet berekend op verkopen aan btw-plichtige bedrijven in andere EU-landen/-regio's. U moet de waarde van deze verkopen aan EU-landen/-regio's apart op uw btw-aangifte vermelden.  

Om op de juiste wijze btw op verkopen aan EU-landen/regio's te berekenen, moet u:  

* Stel een regel in voor verkopen met dezelfde informatie voor inkopen. Als u al regels hebt ingesteld op de pagina **Btw-boekingsinstellingen** voor inkopen uit EU-landen/regio's, kunt u de regels ook voor verkopen gebruiken.  
* De btw-bedrijfsboekingsgroepen toewijzen in het veld **Btw-bedrijfsboekingsgroep** op het sneltabblad **Facturering** van de klantenkaart van elke leverancier van de EU. U moet het u btw-nummer van de klant invoeren in het veld **Btw-nummer** op het sneltabblad **Buitenlandse handel**.  

Wanneer u een verkoop aan een klant in een ander EU-land/-regio boekt, wordt het btw-bedrag berekend en wordt een btw-post gemaakt met de informatie over de btw-verlegging en het btw-basisbedrag (het bedrag dat gebruikt wordt om het btw-bedrag te berekenen). In het grootboek worden geen posten naar de btw-rekeningen geboekt.

Als u een combinatie van btw-bedrijfsboekingsgroep en btw-productboekingsgroep wilt gebruiken voor rapportage als services in de periodieke btw-rapporten, schakelt u het veld **EU-service** in.

> [!NOTE]  
> Het veld **EU-service** is alleen van toepassing op btw-rapporten. Het veld is niet gerelateerd aan de functies **Servicedeclaratie** of **Intrastat voor services**.

## <a name="vat-rounding-for-documents"></a>Btw-afronding voor documenten

Bedragen in documenten die nog niet zijn geboekt, worden afgerond en weergegeven zodat ze overeenkomen met de uiteindelijke afronding van bedragen die daadwerkelijk zijn geboekt. Btw wordt berekend voor een volledig document, wat betekent dat de btw die in het document is berekend, is gebaseerd op de som van alle regels met dezelfde btw-identificatie in het document.  

## <a name="set-up-vat-reporting"></a>Btw-aangifte instellen

U moet informatie instellen over hoe de belastingdienst in uw land/regio u verplicht om btw-aangiften in te dienen. De volgende stappen illustreren de meest gebruikte informatie. Voor uw land/regio zijn mogelijk echter aanvullende stappen vereist. Zie voor meer informatie het betreffende artikel in de sectie *Lokale functionaliteit* in het paneel aan de linkerkant.

[!INCLUDE [vat-report-setup](includes/vat-report-setup.md)]

## <a name="see-also"></a>Zie ook

[Sjablonen voor btw-overzichten en namen voor btw-aangiften instellen](finance-how-setup-vat-statement.md)  
[Ongerealiseerde btw instellen](finance-setup-unrealized-vat.md)  
[Btw-aangifte doen bij een belastingdienst](finance-how-report-vat.md)  
[Werken met btw op verkoop en inkoop](finance-work-with-vat.md)  
[Werken met Wijzigingstool btw-tarief](finance-how-use-vat-rate-change-tool.md)  
[Btw-nummers controleren](finance-how-validate-vat-registration-number.md)  
[Lokale functionaliteit in Business Central](about-localization.md)  
[Btw-aangifte in de Duitse versie](LocalFunctionality/Germany/vat-reporting.md)  
[Belgische btw](LocalFunctionality/Belgium/belgian-vat.md)  
[Italiaanse btw](LocalFunctionality/Italy/italian-vat.md)  
[Elektronische btw- en ICP-aangiften instellen in de Nederlandse versie](LocalFunctionality/Netherlands/how-to-set-up-electronic-vat-and-icp-declarations.md)  
[Btw-rapporten in de Spaanse versie](LocalFunctionality/Spain/vat-reports.md)  
[Boeking van Goods and Services Tax instellen in de Australische versie](LocalFunctionality/Australia/how-to-set-up-goods-and-service-tax-posting.md)  
[Btw in de Tsjechische versie](LocalFunctionality/Czech/finance-vat.md)  
[Btw-aangifte in de Noorse versie](LocalFunctionality/Norway/norwegian-vat-reporting.md)  
[Aangifte van Goods/Services Tax en Harmonized Sales Tax in Canada](LocalFunctionality/Canada/sales-tax-goods-services.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
