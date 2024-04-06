---
title: De Shopify-connector instellen en gebruiken
description: Verschillende integratiescenario's voor het demonstreren van de werkstroom tussen Shopify en Business Central
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30101, 30102, 30106, 30107, 30113, 30115, 30126, 30156, 30157'
ms.reviewer: solsen
author: brentholtorf
ms.author: bholtorf
---

# <a name="walkthrough-set-up-and-use-the-shopify-connector"></a>Procedure: de Shopify Connector instellen en gebruiken

Dit gedeelte demonstreert enkele typische scenario's en leidt u door de stappen om gebruikers te testen of te trainen in de werkstroom van de geïntegreerde [!INCLUDE[prod_short](../includes/prod_short.md)] en de Shopify-winkel.

## <a name="prerequisites"></a>Vereisten

### <a name="shopify"></a>Shopify

U moet over het volgende beschikken:

- Een Shopify-account
- Een online Shopify-winkel

Meer informatie over het maken van Shopify-proefversies en aanbevolen instellingen vindt u op [Een Shopify-account maken en instellen](shopify-account.md).

### <a name="business-central"></a>Business Central

U hebt een [!INCLUDE[prod_short](../includes/prod_short.md)]-account nodig. 

U kunt bijvoorbeeld een demo-account maken of een proefversie starten. Lees hier meer over [Demonstratieomgevingen voorbereiden van Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment) en [Aanmelden voor de proefperiode](../trial-signup.md). 

## <a name="connect-business-central-to-the-shopify-shop"></a>Business Central verbinden met de online Shopify-winkel

In [!INCLUDE[prod_short](../includes/prod_short.md)] doet u het volgende:

1. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer de actie **Nieuw**.
3. Voer `DEMO1` in het veld **Code** in.
4. Voer in het veld **Shopify-URL** de URL in van de online winkel waarmee u verbinding wilt maken.
5. Activeer de schakelaar **Geactiveerd** en bekijk en accepteer vervolgens de algemene voorwaarden.

Volg deze stappen om Shopify-dashboards te configureren:

1. Zet de schakelaar **Synchronisatie op achtergrond toestaan** uit.
2. Selecteer *Naar Shopify* in het veld **Artikel synchroniseren**.
3. Selecteer *Naar Shopify* in het veld **Artikelafbeeldingen synchroniseren**.
4. Zet de schakelaar **Artikelkenmerken synchroniseren** aan.
5. Zet de schakelaar **Voorraad getraceerd** aan.
6. Selecteer *Weigeren* in het veld **Standaardvoorraadbeleid** .
7. Zet de schakelaar **Automatisch onbekende klanten maken** aan.
8. Vul het veld **Klant-/bedrijfssjablooncode** in met de juiste sjabloon.
9. Vul de **Rekening voor verzendkosten** en de **Fooienrekening** in met de opbrengstrekening. Gebruik in de VS bijvoorbeeld `40210`.
10. Zet de schakelaar **Automatisch orders maken** aan.
11. Zet de schakelaar **Verkooporders automatisch vrijgeven** uit.

Locatietoewijzing configureren:

1. Selecteer de actie **Vestigingen** om **Shopify-winkellocaties** te openen.
2. Selecteer de actie **Shopify-vestigingen ophalen** om alle vestigingen te importeren die zijn gedefinieerd in Shopify. Selecteer het item waarbij de schakelaar **Is primair** is geselecteerd.
3. Voer in het **Vestigingsfilter** `''|EAST|MAIN` in.
4. Selecteer *Gepland beschikbaar saldo vandaag* in het veld **Voorraadberekening** om een voorraadsynchronisatie in te schakelen voor een geselecteerde Shopify-vestiging.

## <a name="walkthrough-start-selling-products-online"></a>Procedure: begin met het online verkopen van producten

### <a name="scenario"></a>Scenario

Stel dat u Shopify als online winkel wilt proberen zonder veel tijd te besteden aan het opzetten van dingen, vooral omdat u uw artikelen al goed in [!INCLUDE[prod_short](../includes/prod_short.md)] onderhoudt. Nadat u uw online Shopify-winkel hebt gestart, krijgt u meteen nieuwe klanten die blij zijn met uw winkel en hun koopervaring. Dus besluiten ze om fooien te geven bij het afrekenen.

### <a name="steps"></a>Stappen

Volg deze stappen in [!INCLUDE[prod_short](../includes/prod_short.md)]:

1. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-producten** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer **Artikelen toevoegen**.
3. Voer `DEMO1` in het veld **Winkelcode** in.
4. Stel het filter `CHAIR` in op het veld **Artikelcategoriecode**.
5. Zet de schakelaar **Productafbeeldingen synchroniseren** aan.
6. Zet de schakelaar **Voorraad synchroniseren** aan.
7. Selecteer **OK** en wacht tot de eerste synchronisatie van artikelen, prijzen, afbeeldingen en voorraad is voltooid.

In de online **Shopify-winkel**:
> [!Tip]  
> Open **Shopify-beheer** door te navigeren naar de URL die is opgegeven in het veld **URL** van de pagina **Shopify - Winkelkaart**. Selecteer het oogpictogram naast het verkoopkanaal **Online winkel**, op de zijbalk van **Shopify-beheer**. 

Open de productcatalogus. Kennisgeving:

* Producttitels, afbeeldingen en prijzen.
* Beschikbaarheidsindicator (uitverkocht voor producten die niet op voorraad zijn).

Kies elk product dat kan worden verkocht, bijvoorbeeld de `BERLIN Swivel Chair, yellow`. Merk op dat de beschrijving artikelkenmerken bevat.

Selecteer **Nu kopen** en ga verder met afrekenen.

1. Voer in het veld **E-mail of mobiel telefoonnummer** `cl@contoso.com` in (of het e-mailadres waarop u bestel- en verzendbevestigingen wilt ontvangen).
2. In de velden **Voornaam** en **Achternaam** voert u `Claudia Lawson` in.
3. Voer het lokale adres in.
4. Selecteer het vakje **Deze informatie opslaan voor de volgende keer**.
6. Houd *Standaard* aan als verzendmethode.
8. Voer in het veld **Creditcardnummer** `1` in als u *(voor testen) Bogus Gateway* gebruikt, of voer `5555 5555 5555 4444` in als u *Shopify Payments* in de testmodus gebruikt.
9. Vul het veld **Naam op kaart** in.
10. Voer in het veld **Vervaldatum** de huidige maand/jaar in.
11. Voer `111` in het veld **Beveiligingscode** in.
7. Optioneel: selecteer `10%` tip.
8. 12. Selecteer **Nu betalen**.

Voer in [!INCLUDE[prod_short](../includes/prod_short.md)] de volgende stappen uit:

1. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-orders** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer de actie **Orders synchroniseren vanuit Shopify**.
3. Selecteer **OK**.

De geïmporteerde order is klaar voor verwerking.

1. Selecteer de geïmporteerde order om het venster **Shopify-order** te openen.
2. U ziet dat de nieuwe klant en verkooporders zijn gemaakt.
3. Verken de acties **Risico** en **Verzendkosten**.
4. Selecteer **Verkooporder** om het venster **Verkooporder** te openen. Verkooporder is een vraag, die indien nodig kan worden gedekt door assemblage, productie of inkoop met behulp van de planningsengine. Het ondersteunt ook verschillende magazijnafhandelingsprocessen met volledige scheiding van taken.
6. Voer in het veld **Agent** `DHL` in. Heropen de order indien nodig door de actie **Heropenen** te kiezen.
7. Voer in het veld **Traceringsnummer (zending)** `123456789` in.
8. Selecteer **Boeken**, houd de optie **Verzenden en factureren** en selecteer vervolgens **OK**.

Nu worden fysieke en financiële gegevens geregistreerd [!INCLUDE[prod_short](../includes/prod_short.md)]. Het is tijd om aan Shopify de wijzigingen door te geven.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verzendingen combineren met Shopify** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer **OK**.

U ziet in **Shopify-beheer** dat de order nu is gemarkeerd als *Afgehandeld*. U kunt daar ook de verzendgegevens bekijken en de tracerings-URL zien. Als u **Orders synchroniseren vanuit Shopify** opnieuw uitvoert, wordt de order in beide systemen gearchiveerd.

## <a name="walkthrough-add-your-customers-to-your-new-online-store"></a>Procedure: Uw klanten toevoegen aan uw nieuwe online winkel

### <a name="scenario-1"></a>Scenario

Na een succesvolle snelle opening van uw nieuwe online winkel, wilt u dat uw huidige klanten deze bezoeken en beginnen met het plaatsen van orders. Afhankelijk van uw Shopify-plan en -proces kunt u B2B- en D2C-stromen proberen.

### <a name="dtc-steps"></a>D2C-stappen

In [!INCLUDE[prod_short](../includes/prod_short.md)] doet u het volgende:

1. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-Klanten** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer **Klanten toevoegen**.
3. Voer `DEMO1` in het veld **Winkelcode** in.
4. Zet het filter `20000` in op het **Nr.** veld.
5. Selecteer **OK** en wacht tot de eerste synchronisatie van klanten is voltooid.

U ziet in **Shopify-beheer** dat de klant is geïmporteerd. Open de klanten en zie dat de voor- en achternaam van de klant afkomstig zijn uit het veld **Contactnaam** van de **Klantenkaart**. De bedrijfsnaam is terug te vinden in het standaardadres, gekoppeld aan de klant. Als u *Klassieke klantrekeningen* gebruikt, kunt u **Accountuitnodiging verzenden** selecteren om de klant uit te nodigen. Met *Nieuwe klantrekeningen* is er geen wachtwoord vereist voor klanten om in te loggen, maar Shopify laat uw klanten inloggen met een eenmalige 6- cijferige verificatiecode, verzonden per e-mail. 

### <a name="b2b-steps"></a>B2B-stappen

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

In [!INCLUDE[prod_short](../includes/prod_short.md)] doet u het volgende:

1. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-bedrijven** in en selecteer de gerelateerde koppeling.
2. Selecteer **Bedrijf toevoegen**.
3. Voer `DEMO1` in het veld **Winkelcode** in.
4. Zet het filter `30000` in op het **Nr.** veld.
5. Selecteer **OK** en wacht tot de eerste synchronisatie van klanten is voltooid.

In **Shopify-beheer** ziet u dat zowel het bedrijf als de klant zijn geïmporteerd. Open de klanten en bekijk het bedrijfsfeitenvak met een koppeling naar Bedrijf, vestiging en toegewezen machtigingen. Selecteer **[...]** in het feitenvak **Bedrijf en selecteer vervolgens **E-mail met B2B-toegang verzenden** om de klant uit te nodigen.

## <a name="walkthrough-fine-tuning-of-item-management"></a>Procedure: Artikelbeheer fijn afstemmen

### <a name="scenario-2"></a>Scenario

U wilt graag meer flexibiliteit en controle toevoegen aan uw processen rondom artikelbeheer. U wilt productbeschrijvingen verbeteren en meer beoordelingsstappen toevoegen voordat producten beschikbaar komen voor alle klanten.

### <a name="steps-1"></a>Stappen

In [!INCLUDE[prod_short](../includes/prod_short.md)] doet u het volgende:

Bereid gegevens voor.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klantenprijsgroep** in en selecteer vervolgens de gerelateerde koppeling.
2. Voeg een nieuwe prijsgroep toe. Voer `SHOPIFY` in het veld **Code** in.
3. Sluit het venster **Klantenprijsgroep**.
4. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en selecteer de gerelateerde koppeling.
5. Selecteer artikel *1896-S, Athens Desk* en voer daarna de volgende stappen uit:

6. Selecteer de actie **Varianten** en voeg vervolgens twee varianten toe: `PREMIUM, Athens Desk, Premium edition` en `ESSENTIAL, Athens Desk, Essential edition`.
7. Selecteer de actie **Marketingtekst** en gebruik **Opstellen met Copilot** om creatieve en boeiende tekst te krijgen. Als marketingtekstsuggestie niet is ingeschakeld, voert u gewoon het volgende in: **Eenvoudig, stijlvol ontwerp** past bij elk ensemble. *Verkrijgbaar in twee edities.*'. 
8. Selecteer de actie **Verkoopprijzen** en voeg nieuwe prijzen toe zoals weergegeven in de volgende tabel:

   |Lijn|Verkoopsoort|Verkoopscode|Type|Code|Variantcode<br>(voeg het veld toe via personalisatie)|Eenheidsprijs|
   |------|------------|------------|------------|----------------|------------|------------|
   |1|Klantenprijsgroep|SHOPIFY|Artikel|1896-S|ESSENTIAL|700|
   |2|Klantenprijsgroep|SHOPIFY|Artikel|1896-S|PREMIUM|1000|

9. Selecteer de actie **Verkoopkortingen** en voeg een nieuwe korting toe:

   * **Verkoopsoort** *Klantenkortingsgroep*
   * **Verkoopcode** *DET.HANDEL*
   * **Soort** *Artikel*
   * **Code** *1896-S*
   * **Code van maateenheid** *Per stuk*
   * **Regelkorting %** *10*

10. Selecteer de actie **Artikelverwijzingen** en voeg de volgende regels toe:

   |Regel|Referentiesoort|Referentienr.|Variantcode|
   |------|------------|------------|------------|
   |1|Barcode|77777777|ESSENTIAL|
   |2|Barcode|11111111|PREMIUM|

11. Selecteer het artikel *1920-S, ANTWERP Conferentietafel* en voer daarna de volgende stappen uit:
12. Selecteer **Voorraad aanpassen** en voer in het veld **Nieuwe voorraad** `100` in voor de vestigingen *OOST* en *WEST*. 
13. Selecteer **OK**.

Pas de synchronisatie-instellingen aan.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer de `DEMO1`-winkel waarvoor u artikelen wilt synchroniseren om de pagina **Shopify-winkelkaart** te openen.
3. Schakel het veld **Marketingtekst synchroniseren** in.
4. Selecteer *Artikelnr. + variant* in het veld **SKU-toewijzing**.
5. Selecteer *Doorgaan* in het veld **Standaardvoorraadbeleid**.
6. Selecteer **Concept** in het veld *Status voor gemaakte producten*.
7. Selecteer **Status naar gearchiveerd** in het veld *Actie voor verwijderd product*.
8. Selecteer *SHOPIFY* in het veld **Klantenprijsgroep**.
9. Selecteer *DET.HANDEL* in het veld **Klantenkortingsgroep**.
 
Voer de synchronisatie uit.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en selecteer de gerelateerde koppeling.
2. Selecteer de `DEMO1`-winkel waarvoor u artikelen wilt synchroniseren om de pagina **Shopify-winkelkaart** te openen.
3. Selecteer de actie **Producten** om het venster **Shopify-producten** te openen.
4. Selecteer de actie **Artikelen toevoegen**.
5. Stel het filter **TABEL|BUREAU** in op het veld *Artikelcategoriecode*.
6. Zet de schakelaar **Productafbeeldingen synchroniseren** aan.
7. Zet de schakelaar **Voorraad synchroniseren** aan.
8. Selecteer **OK** en wacht tot de eerste synchronisatie van artikelen, prijzen, afbeeldingen en voorraad is voltooid.

Producten worden toegevoegd. Merk op dat de status is ingesteld op *Concept* en dat artikelen daarom niet zichtbaar zijn in de online Shopify-winkel.

1. Selecteer de regel met het artikel *1920-S, ANTWERP Conference Table*. Voer bij de **SEO-titel** `Rectangular meeting table Antwerp, 10 seats, black` in.
2. Selecteer in het veld **Status** de optie *Actief*.
3. Selecteer de regel met artikel *1906-S, ATHENS, Mobile Pedestal* en selecteer vervolgens de actie **Verwijderen**.

U ziet in **Shopify-beheer** dat alle producten verschillende statussen hebben.

* *ANTWERP Conference Table* is *Actief* omdat we de status hebben gewijzigd in het venster **Shopify-product**.
* *ATHENS Desk* is *Concept* omdat we de standaardstatus voor alle toegevoegde producten hebben geconfigureerd als *Concept*.
* *ATHENS Mobile Pedestal* is *Gearchiveerd* omdat we de winkel hebben geconfigureerd om automatisch de status *Gearchiveerd* toe te wijzen voor verwijderde producten.

Merk op dat de voorraad voor ANTWERP Conference Table 100 is, omdat we het systeem hebben geconfigureerd om alleen voorraad te gebruiken uit twee vestigingen, HOOFD en OOST. Voorraad op een andere vestiging (WEST) wordt genegeerd.

* Open *ANTWERP Conference Table*, let op de velden **Aangepast type**, **Leverancier**, **Gewicht** en **Kosten per artikel** en het gedeelte **Voorbeeld van zoekprogrammavermelding**.
* Open *Athens Desk*, schuif omlaag naar het gedeelte **Varianten** en kijk hoe **SKU** is gevuld.
* Selecteer **Bewerken** om de streepjescode en prijzen te bekijken.
* Wijzig de status van *Athens Desk* in *Actief* en selecteer de actie **Voorbeeld**.

Open in de **online Shopify-winkel** de productcatalogus en zoek het product *ATHENS Desk*. Merk op dat er verschillende opties beschikbaar zijn. Voor verschillende opties zijn de prijzen verschillend. Let op kortingsinformatie.

### <a name="additional-steps-for-b2b"></a>Extra stappen voor B2B

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

U kunt de connector configureren om automatisch een catalogus voor geëxporteerde bedrijven te maken en toe te wijzen. De onderstaande stappen zijn handig als u preciezere controle wilt over wat er beschikbaar is voor B2B-klanten.

Maak in **Shopify-beheer** een catalogus en wijs deze toe.

1. Selecteer **Producten** en vervolgens **Catalogi** op de zijbalk van **Shopify-beheer**.
2. Catalogus maken voor specifieke producten. Vermeld titel 'B2B'. 
3. Kies **Beheren** en vervolgens **Producten en prijzen beheren**.
4. Selecteer het filter *Uitgesloten*, zoek *ATHERN Desk* en kies **Opnemen in catalogus**.
5. Selecteer **Klanten** en vervolgens **Bedrijven** op de zijbalk van **Shopify-beheer**.
6. Selecteer *School of Fine Art* en kies **[...]** en vervolgens **Catalogi toevoegen** en voeg de *B2B* catalogus toe die eerder is gemaakt.

In [!INCLUDE[prod_short](../includes/prod_short.md)] doet u het volgende:

Bereid gegevens voor.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en selecteer de gerelateerde koppeling.

2. Selecteer artikel **1896-S, Athens Desk** en voer daarna de volgende stappen uit:

3. Selecteer de actie **Verkoopkortingen** en voeg een nieuwe korting toe:

   * **Verkoopsoort** *Klantenkortingsgroep*
   * **Verkoopcode** *GROOTHDL*
   * **Soort** *Artikel*
   * **Code** *1896-S*
   * **Code van maateenheid** *Per stuk*
   * **Regelkorting %** *25*

4. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-catalogi** in en selecteer de gerelateerde koppeling.
5. Selecteer **Catalogi ophalen**.
6. Voer `DEMO1` in het veld **Winkelcode** in.
7. Selecteer het item met de naam *B2B*-catalogus waarvoor u de prijzen wilt synchroniseren.
8. Schakel de schakelaar **Prijzen synchroniseren** in.
9. Selecteer *SHOPIFY* in het veld **Klantenprijsgroep**.
10. Selecteer *GROOTHDL* in het veld **Klantenkortingsgroep**.
11. Kies **Prijzen synchroniseren** en wacht tot de synchronisatie van de prijzen is voltooid.

Bekijk in **Shopify-beheer** prijzen voor de *B2B*-catalogus.

Open in de **online Shopify-winkel** de productcatalogus en zoek het product *ATHENS Desk*. Let op: prijzen zijn kortingsinformatie.

## <a name="walkthrough-check-out-and-order-synchronization-for-individual-buyer-and-company-representative"></a>Procedure: Afrekenen en ordersynchronisatie voor individuele kopers en bedrijfsvertegenwoordigers
Dit is een voortzetting van [Procedure: begin met het online verkopen van producten](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online). U kunt het ook proberen met uw eigen gegevens, bijvoorbeeld uw Shopify-winkel of sandbox.

Individuele koper

1. In de online **Shopify-winkel**. Kies het pictogram **Rekening** . Voer het e-mailadres in waartoe u toegang hebt.
2. Log in met een eenmalige verificatiecode van 6 cijfers die u per e-mail hebt verzonden.
3. Verken de productcatalogus. U zou alle producten met detailhandelsprijzen moeten kunnen zien.
4. Selecteer de Essential-variant, selecteer **Nu kopen** en ga door naar afrekenen.
5. Vul de velden **Voornaam** en **Achternaam** in.
6. Voer het lokale adres in.
7. Houd *Standaard* aan als verzendmethode.
8. Voer in het veld **Creditcardnummer** `1` in als u *(voor testen) Bogus Gateway* gebruikt, of voer `5555 5555 5555 4444` in als u *Shopify Payments* in de testmodus gebruikt.
9. Voer in het veld **Vervaldatum** de huidige maand/jaar in.
10. Voer `111` in het veld **Beveiligingscode** in.
11. Vul het veld **Naam op kaart** in.
12. Selecteer **Nu betalen**.
 
Bedrijfsvertegenwoordiger

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

1. In **Shopify-beheer**.
2. Selecteer **Klanten** en vervolgens **Bedrijven** op de zijbalk van **Shopify-beheer**.
3. Open het item *School of Fine Art*.
4. Kies **[...]** in het feitenvak **School for Fine Art** en vervolgens **Betalingsvoorwaarden bewerken** en selecteer *Verschuldigd bij afhandeling*.
5. Kies **[...]** in het feitenvak **Klanten** en vervolgens **Klant toevoegen** en voeg er een toe met het e-mailadres waarmee u eerder bij de winkel inlogde.
6. In de online **Shopify-winkel**. Kies het pictogram **Rekening** . Voer het e-mailadres in waartoe u toegang hebt.
7. Log in met een eenmalige verificatiecode van 6 cijfers die u per e-mail hebt verzonden.
8. Verken de productcatalogus. U zou alleen producten moeten kunnen zien die zijn toegevoegd aan de *B2B*-catalogus met speciale detailhandelsprijzen.
9. Selecteer de Essential-variant, selecteer **Nu kopen** en ga door naar afrekenen.
10. Merk op dat account, Verzenden naar en betalingsmethode zijn ingevuld.
11. Vul het veld **Inkoopordernummer** in met `PO-12345`.
12. Selecteer **Order verzenden**.
 
Voer in [!INCLUDE[prod_short](../includes/prod_short.md)] de volgende stappen uit:

1. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-orders** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer de actie **Orders synchroniseren vanuit Shopify**.
3. Selecteer **OK**.

De geïmporteerde order is klaar voor verwerking.

1. Selecteer de geïmporteerde order om het venster **Shopify-order** te openen.
2. Merk op dat hoewel beide bestellingen door dezelfde persoon zijn verzonden, ze aan twee verschillende klanten zijn gekoppeld. 
3. In de order die namens het bedrijf is verzonden ziet u een waarde in het veld **Inkoopordernummer**, dat ook wordt overgebracht naar het veld **Extern documentnr.** van het gemaakte verkoopdocument.
4. Omdat we B2B-bedrijf hebben geconfigureerd om betalingen buiten Shopify af te handelen, wordt de **Financiële status** ingesteld op *In behandeling*. Zodra u de betaling hebt ontvangen, selecteert u de actie **Markeren als betaald**. De financiële status wordt bijgewerkt in Shopify. 

## <a name="walkthrough-import-items-customers-companies-from-shopify"></a>Procedure: Artikelen, klanten, bedrijven importeren uit Shopify

### <a name="scenario-3"></a>Scenario

U hebt al een succesvolle online winkel en wilt [!INCLUDE[prod_short](../includes/prod_short.md)] gebruiken als software voor bedrijfsbeheer. U wilt zoveel mogelijk gegevens importeren uit Shopify als mogelijk. 

### <a name="steps-2"></a>Stappen

Dit is een vervolg op [Procedure: Beginnen met het online verkopen van producten](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online) en [Procedure: Uw klanten toevoegen aan uw nieuwe online winkel](walkthrough-setting-up-and-using-shopify.md#walkthrough-add-your-customers-to-your-new-online-store). U kunt het ook proberen met uw eigen gegevens, bijvoorbeeld uw Shopify-winkel of sandbox.

Volg in [!INCLUDE[prod_short](../includes/prod_short.md)] de volgende stappen.

#### <a name="prepare-data"></a>Gegevens voorbereiden

1. Schakel over naar een gratis proefperiode van 30 dagen zonder voorbeeldgegevens. Zie voor meer informatie [Uw eigen gegevens toevoegen aan een lege proefversie](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions#add-your-own-data-to-an-empty-trial-company).
2. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en selecteer vervolgens de gerelateerde koppeling.
3. Selecteer **Nieuw**.
4. Voer `DEMO2` in het veld **Code** in.
5. Voer in het veld **Shopify-URL** de URL in van de online winkel waarmee u verbinding wilt maken.
6. Activeer de schakelaar **Geactiveerd** en bekijk en accepteer vervolgens de algemene voorwaarden.

Configureer de Shopify-winkel zoals hier beschreven:

1. Zet de schakelaar **Synchronisatie op achtergrond toestaan** uit.
2. Selecteer *Van Shopify* in het veld **Artikel synchroniseren**.
3. Zet de schakelaar **Automatisch onbekende artikelen maken** aan.
4. Vul in het veld **Artikelsjablooncode** de juiste sjabloon in.
5. Selecteer *Van Shopify* in het veld **Artikelafbeeldingen synchroniseren**.
6. Selecteer *Artikelnr. + variant* in het veld **SKU-toewijzing**.
7. Selecteer *Alle klanten* bij **Klant importeren vanuit Shopify**.
8. Zet de schakelaar **Automatisch onbekende klant maken** aan.
9. Vul het veld **Klant-/bedrijfssjablooncode** in met de juiste sjabloon.
10. Selecteer *Alle klanten* bij **Bedrijf importeren uit Shopify**.
11. Zet de schakelaar **Automatisch onbekend bedrijf maken** aan.

#### <a name="run-the-synchronization"></a>De synchronisatie uitvoeren

1. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer de *DEMO2*-winkel waarvoor u gegevens wilt synchroniseren om de pagina **Shopify-winkelkaart** te openen.
3. Selecteer **Producten synchroniseren**.
4. Selecteer **Productafbeeldingen synchroniseren**.
5. Selecteer **Klanten synchroniseren**.
6. Selecteer **Bedrijven synchroniseren**

### <a name="results"></a>Resultaten

* Shopify-producten worden geïmporteerd. Selecteer ter verificatie het pictogram ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-producten** in en selecteer vervolgens de gerelateerde koppeling.
* Artikelen met afbeeldingen worden gemaakt. Selecteer ter verificatie het pictogram ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikel** in en selecteer de gerelateerde koppeling.
* Shopify-klanten worden geïmporteerd. Selecteer ter verificatie het pictogram ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-Klanten** in en selecteer de gerelateerde koppeling.
* Shopify-bedrijven worden geïmporteerd. Selecteer ter verificatie het pictogram ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-bedrijven** in en selecteer de gerelateerde koppeling.
* Er worden klanten gemaakt. Selecteer ter verificatie het pictogram ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en selecteer vervolgens de gerelateerde koppeling.


## <a name="see-also"></a>Zie ook

[Aan de slag met de Shopify-connector](get-started.md)  
