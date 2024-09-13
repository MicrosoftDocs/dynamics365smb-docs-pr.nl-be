---
title: De Shopify-connector instellen en gebruiken
description: Verschillende integratiescenario's voor het demonstreren van de werkstroom tussen Shopify en Business Central
ms.date: 08/30/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30101, 30102, 30106, 30107, 30113, 30115, 30126, 30156, 30157'
ms.reviewer: bholtorf
author: brentholtorf
ms.author: bholtorf
---

# Procedure: de Shopify Connector instellen en gebruiken

Dit gedeelte demonstreert enkele typische scenario's en leidt u door de stappen om gebruikers te testen of te trainen in de werkstroom van de geïntegreerde [!INCLUDE[prod_short](../includes/prod_short.md)] en de Shopify-winkel.

## Vereisten

### Shopify

U moet over het volgende beschikken:

- Een Shopify-account
- Een online Shopify-winkel

Meer informatie over het maken van Shopify-proefversies en aanbevolen instellingen vindt u op [Een Shopify-account maken en instellen](shopify-account.md).

### Business Central

U hebt een [!INCLUDE[prod_short](../includes/prod_short.md)]-account nodig.

U kunt bijvoorbeeld een demo-account maken of een proefversie starten. Lees hier meer over [Demonstratieomgevingen voorbereiden van Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment) en [Aanmelden voor de proefperiode](../trial-signup.md). 

## Business Central verbinden met de online Shopify-winkel

In [!INCLUDE[prod_short](../includes/prod_short.md)] doet u het volgende:

1. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer de actie **Nieuw**.
3. Voer in het veld **Code** het volgende in: **DEMO1**.
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
9. Vul de **Rekening voor verzendkosten** en de **Fooienrekening** in met de opbrengstrekening. In de VS gebruikt u bijvoorbeeld  **40210**.
10. Zet de schakelaar **Automatisch orders maken** aan.
11. Zet de schakelaar **Verkooporders automatisch vrijgeven** uit.

Locatietoewijzing configureren:

1. Selecteer de actie **Vestigingen** om **Shopify-winkellocaties** te openen.
2. Selecteer de actie **Shopify-vestigingen ophalen** om alle vestigingen te importeren die zijn gedefinieerd in Shopify. Selecteer het item waarbij de schakelaar **Is primair** is geselecteerd.
3. Voer in het **Locatiefilter** **''|EAST|MAIN** in.
4. Om een inventarissynchronisatie voor een geselecteerde locatie in te schakelen, selecteert u in het veld  Shopify Voorraadberekening **de optie** Geprojecteerd beschikbaar saldo vandaag **.**

## Procedure: begin met het online verkopen van producten

### Scenario

Stel dat u Shopify als online winkel wilt proberen zonder veel tijd te besteden aan het opzetten van dingen, vooral omdat u uw artikelen al goed in [!INCLUDE[prod_short](../includes/prod_short.md)] onderhoudt. Nadat u uw online Shopify-winkel hebt gestart, krijgt u meteen nieuwe klanten die blij zijn met uw winkel en hun koopervaring. Dus besluiten ze om fooien te geven bij het afrekenen.

### Stappen

Volg deze stappen in [!INCLUDE[prod_short](../includes/prod_short.md)]:

1. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-producten** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer **Artikelen toevoegen**.
3. Voer in het veld **Winkelcode**  **DEMO1** in.
4. Stel in het veld  **Artikelcategoriecode** het filter **STOEL** in.
5. Zet de schakelaar **Productafbeeldingen synchroniseren** aan.
6. Zet de schakelaar **Voorraad synchroniseren** aan.
7. Selecteer **OK** en wacht tot de eerste synchronisatie van artikelen, prijzen, afbeeldingen en inventaris is voltooid.

In de online **Shopify-winkel**:
> [!Tip]  
> Open **Shopify-beheer** door te navigeren naar de URL die is opgegeven in het veld **URL** van de pagina **Shopify - Winkelkaart**. Selecteer het oogpictogram naast het verkoopkanaal **Online winkel**, op de zijbalk van **Shopify-beheer**. 

Open de productcatalogus. Kennisgeving:

* Producttitels, afbeeldingen en prijzen.
* Beschikbaarheidsindicator (uitverkocht voor producten die niet op voorraad zijn).

Kies een product dat verkocht kan worden. Bijvoorbeeld de **BERLIN Draaistoel, geel**. Merk op dat de beschrijving artikelkenmerken bevat.

Selecteer **Nu kopen** en ga verder met afrekenen.

1. Voer in het veld **e-mailadres of mobiel telefoonnummer** het volgende in **cl@contoso.com** (of een e-mailadres waarop u order- en verzendbevestigingen wilt ontvangen).
2. Voer in de velden **Voornaam** en **Achternaam** de volgende namen in: **Claudia** en **Lawson**.
3. Voer het lokale adres in.
4. Selecteer het vakje **Deze informatie opslaan voor de volgende keer**.
6. Houd *Standaard* aan als verzendmethode.
8. Voer in het veld **Creditnummer kaart** 1 **in** als u **(voor het testen) Bogus Gateway** gebruikt, of voer **5555 5555 5555 4444** in **Shopify als u betalingen** in de testmodus gebruikt.
9. Vul het veld **Naam op kaart** in.
10. Voer in het veld **Vervaldatum** de huidige maand/jaar in.
11. Voer in het veld  **Beveiligingscode** **111** in.
12. Optioneel: Selecteer **10%** fooi.
13. Selecteer **Nu betalen**.

Voer in [!INCLUDE[prod_short](../includes/prod_short.md)] de volgende stappen uit:

1. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-orders** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer de actie **Orders synchroniseren vanuit Shopify**.
3. Selecteer **OK**.

De geïmporteerde order is klaar voor verwerking.

1. Selecteer de geïmporteerde order om het venster **Shopify-order** te openen.
2. U ziet dat de nieuwe klant en verkooporders zijn gemaakt.
3. Verken de **Risico's** en **Verzendkosten** acties.
4. Selecteer **Verkooporder** om het venster **Verkooporder** te openen. Verkooporder is een vraag, die indien nodig kan worden gedekt door assemblage, productie of inkoop met behulp van de planningsengine. Het ondersteunt ook verschillende magazijnafhandelingsprocessen met volledige scheiding van taken.
6. Voer in het veld  **Agent**  **DHL** in. Heropen de order indien nodig door de actie **Heropenen** te kiezen.
7. Voer in het **Pakket Tracking Nr.**, **123456789** in.
8. Selecteer **Boeken**, houd de optie **Verzenden en factureren** en selecteer vervolgens **OK**.

Nu worden fysieke en financiële gegevens geregistreerd [!INCLUDE[prod_short](../includes/prod_short.md)]. Het is tijd om aan Shopify de wijzigingen door te geven.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verzendingen combineren met Shopify** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer **OK**.

U ziet in **Shopify-beheer** dat de order nu is gemarkeerd als *Afgehandeld*. U kunt daar ook de verzendgegevens bekijken en de tracerings-URL zien. Als u **Orders synchroniseren vanuit Shopify** opnieuw uitvoert, wordt de order in beide systemen gearchiveerd.

## Procedure: Uw klanten toevoegen aan uw nieuwe online winkel

### Scenario

Na een succesvolle snelle opening van uw nieuwe online winkel, wilt u dat uw huidige klanten deze bezoeken en beginnen met het plaatsen van orders. Afhankelijk van uw Shopify-plan en -proces kunt u B2B- en DTC-stromen proberen.

### DTC-stappen

In [!INCLUDE[prod_short](../includes/prod_short.md)] doet u het volgende:

1. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-Klanten** in en selecteer de gerelateerde koppeling.
2. Selecteer **Klanten toevoegen**.
3. Voer in het veld **Winkelcode**  **DEMO1** in.
4. Voer in het veld **Nr.** Veld, stel het filter **20000** in.
5. Selecteer **OK** en wacht tot de eerste synchronisatie van klanten is voltooid.

U ziet in **Shopify-beheer** dat de klant is geïmporteerd. Open de klanten en zie dat de voor- en achternaam van de klant afkomstig zijn uit het veld **Contactnaam** van de **Klantenkaart**. De bedrijfsnaam is terug te vinden in het standaardadres, gekoppeld aan de klant. Als u  **klassieke klantaccounts** gebruikt, kunt u  **Accountuitnodiging verzenden** selecteren om de klant uit te nodigen. Bij  **nieuwe klantaccounts** is er geen wachtwoord nodig om in te loggen. In plaats daarvan Shopify kunnen uw klanten inloggen met een eenmalige verificatiecode van 6 cijfers die per e-mail wordt verzonden. 

### B2B-stappen

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

In [!INCLUDE[prod_short](../includes/prod_short.md)] doet u het volgende:

1. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-bedrijven** in en selecteer de gerelateerde koppeling.
2. Selecteer **Bedrijf toevoegen**.
3. Voer in het veld Winkel **Code**  **DEMO1** in.
4. Stel het filter **30000** in op **nr.** .
5. Selecteer **OK** en wacht tot de eerste synchronisatie van klanten is voltooid.

Merk op dat in  **Shopify Admin** zowel het bedrijf als de klant zijn geïmporteerd. Open de klantenpagina en zie dat het Company FactBox koppelingen bevat naar het bedrijf, de locatie en de toegewezen rechten.
Om de klant uit te nodigen, selecteert u  **[...]** in het **Bedrijfsfeitenvak** en selecteert u vervolgens  **B2B-toegangs-e-mail verzenden**.

## Procedure: Artikelbeheer fijn afstemmen

### Scenario 

U wilt graag meer flexibiliteit en controle toevoegen aan uw processen rondom artikelbeheer. U wilt productbeschrijvingen verbeteren en meer beoordelingsstappen toevoegen voordat producten beschikbaar komen voor alle klanten.

### Stappen

In [!INCLUDE[prod_short](../includes/prod_short.md)] doet u het volgende:

Bereid gegevens voor.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klantenprijsgroep** in en selecteer vervolgens de gerelateerde koppeling.
2. Voeg een nieuwe prijsgroep toe. Voer in het veld  **Code** het volgende in: **SHOPIFY**.
3. Sluit het venster **Klantenprijsgroep**.
4. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en selecteer de gerelateerde koppeling.
5. Selecteer item **1896-S, Athens Desk** en voer vervolgens volgen deze stappen uit:

6. Selecteer de actie **Varianten** en voeg vervolgens twee varianten toe: **premium, Athens Desk, Premium-editie** en **ESSENTIAL, Athens Desk, Essential-editie**.
7. Selecteer de actie **Marketingtekst** en gebruik **Opstellen met Copilot** om creatieve en boeiende tekst te krijgen. Als de suggestie voor marketingtekst niet is ingeschakeld, voert u gewoon het volgende in: '**Eenvoudig, stijlvol ontwerp** past bij elke outfit. *Verkrijgbaar in twee edities.*.
8. Selecteer de actie **Verkoopprijzen** en voeg nieuwe prijzen toe zoals weergegeven in de volgende tabel:

   |Regel|Verkoopsoort|Verkoopscode|Type|Code|Variantcode<br>(voeg het veld toe via personalisatie)|Eenheidsprijs|
   |------|------------|------------|------------|----------------|------------|------------|
   |0|Klantenprijsgroep|SHOPIFY|Artikel|1896-S|ESSENTIAL|700|
   |2|Klantenprijsgroep|SHOPIFY|Artikel|1896-S|PREMIUM|1000|

9. Selecteer de actie **Verkoopkortingen** en voeg een nieuwe korting toe:

   * **Verkoopsoort** *Klantenkortingsgroep*
   * **Verkoopcode** *DET.HANDEL*
   * **Soort** *Artikel*
   * **Code** *1896-S*
   * **Code van maateenheid** *Per stuk*
   * **Regelkorting %** *10*

10. Selecteer de actie  **Itemverwijzingen**  en voeg de volgende regels toe:

   |Regel|Referentiesoort|Verwijzingsnr.|Variantcode|
   |------|------------|------------|------------|
   |0|Barcode|77777777|ESSENTIAL|
   |2|Barcode|11111111|PREMIUM|

11. Selecteer het artikel **1920-S, ANTWERP Conferentietafel** en voer daarna de volgende stappen uit:
12. Selecteer **Aanpassen Inventaris** en voer in het veld **Nieuwe inventaris**  **100** in voor de locaties **OOST** en **WEST**.
13. Selecteer **OK**.

Pas de synchronisatie-instellingen aan.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer de **DEMO1** winkel waarvoor u artikelen wilt synchroniseren om de pagina **Shopify Winkel kaart**  te openen.
3. Schakel het veld **Marketingtekst synchroniseren** in.
4. Selecteer in het veld  **SKU toewijzing** de optie **Artikelnummer+ Variantcode**.
5. Selecteer in het veld **Standaardvoorraadbeleid** de optie **Doorgaan**.
6. Selecteer in het veld **Status voor gemaakte producten** de optie **concept**.
7. Selecteer in het veld **Actie voor verwijderd product** de status **naar Gearchiveerd**.
8. Selecteer in het veld  **Klantprijsgroep** de optie  **SHOPIFY**.
9. Selecteer in het veld **Klantenkortingsgroep** de optie **RETAIL**.

Voer de synchronisatie uit.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer de **DEMO1** winkel waarvoor u artikelen wilt synchroniseren om de pagina **Shopify Winkel kaart**  te openen.
3. Selecteer  **producten** om de pagina  **Shopify producten** te openen.
4. Selecteer de actie **Artikelen toevoegen**.
5. Stel het filter **TABLE|DESK** in op het veld **Artikelcategoriecode** .
6. Zet de schakelaar **Productafbeeldingen synchroniseren** aan.
7. Zet de schakelaar **Voorraad synchroniseren** aan.
8. Selecteer **OK** en wacht tot de eerste synchronisatie van artikelen, prijzen, afbeeldingen en inventaris is voltooid.

Producten worden toegevoegd. Let op, de status is ingesteld op  **concept** en daarom zijn de items niet zichtbaar in de Shopify online winkel.

1. Selecteer de regel met item **1920-S, ANTWERPEN Vergadertafel**. Voer in de **SEO-titel** **Rechthoekige vergadertafel Antwerpen, 10 zitplaatsen, zwart** in.
2. Selecteer in het veld **Status** de optie **Actief**.
3. Selecteer de regel met item **1906-S, ATHENS, Mobiel voetstuk** en selecteer vervolgens **Verwijderen**.

U ziet in **Shopify-beheer** dat alle producten verschillende statussen hebben.

* *ANTWERP Conference Table* is *Actief* omdat we de status ervan hebben gewijzigd op de **Shopify product** pagina.
* *ATHENS Desk* is *Concept* omdat we de standaardstatus voor alle toegevoegde producten hebben geconfigureerd als *Concept*.
* *ATHENS Mobile Pedestal* is *Gearchiveerd* omdat we de winkel hebben geconfigureerd om automatisch de status *Gearchiveerd* toe te wijzen voor verwijderde producten.

Let op dat de inventaris voor de ANTWERP Conference Table 100 bedraagt, omdat we het systeem zo hebben geconfigureerd dat de inventaris van alleen twee locaties wordt gebruikt: MAIN en EAST. Voorraad op een andere vestiging (WEST) wordt genegeerd.

* Open *ANTWERP Conference Table*, let op de velden **Aangepast type**, **Leverancier**, **Gewicht** en **Kosten per artikel** en het gedeelte **Voorbeeld van zoekprogrammavermelding**.
* Open *Athens Desk*, schuif omlaag naar het gedeelte **Varianten** en kijk hoe **SKU** is gevuld.
* Om de streepjescode en prijzen te bekijken, selecteert u  **Bewerken**.
* Wijzig de status van **Athens Desk** naar **Actief** en selecteer **preview**.

Open in de Shopify online winkel de productcatalogus en zoek het **ATHENS Desk** product. Merk op dat er verschillende opties beschikbaar zijn. Voor verschillende opties zijn de prijzen verschillend. Let op kortingsinformatie.

### Extra stappen voor B2B

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

U kunt de connector configureren om automatisch een catalogus voor geëxporteerde bedrijven te maken en toe te wijzen. De onderstaande stappen zijn handig als u preciezere controle wilt over wat er beschikbaar is voor B2B-klanten.

Maak in  **Shopify Admin** een catalogus en wijs deze toe.

1. Selecteer **Producten** en vervolgens **Catalogi** op de zijbalk van **Shopify-beheer**.
2. Maak een catalogus voor specifieke producten. Geef het de titel 'B2B'. 
3. Kies  **Beheren** en vervolgens  **producten en prijzen beheren**.
4. Selecteer het filter  **Uitgesloten**, zoek **ATHENS Desk** en kies  **Opnemen in catalogus**.
5. Selecteer  **Klanten** en vervolgens  **Bedrijven** in de zijbalk van  **Shopify beheer**.
6. Selecteer **School of Fine Art**, kies **[...]** en vervolgens **Catalogi toevoegen** en voeg de **B2B** catalogus toe die u eerder hebt gemaakt.

In [!INCLUDE[prod_short](../includes/prod_short.md)] doet u het volgende:

Bereid gegevens voor.

1. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en selecteer de gerelateerde koppeling.
2. Selecteer item **1896-S, Athens Desk** en voer vervolgens volgen deze stappen uit:
3. Selecteer de actie **Verkoopkortingen** en voeg een nieuwe korting toe:

   * **Verkoopsoort** *Klantenkortingsgroep*
   * **Verkoopcode** *GROOTHDL*
   * **Soort** *Artikel*
   * **Code** *1896-S*
   * **Code van maateenheid** *Per stuk*
   * **Regelkorting %** *25*

4. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-catalogi** in en selecteer de gerelateerde koppeling.
5. Selecteer **Catalogi ophalen**.
6. Voer in het veld **Winkelcode**  **DEMO1** in.
7. Selecteer de invoer met de *B2B* catalogus waarvoor u de prijzen wilt synchroniseren.
8. Schakel de schakelaar **Prijzen synchroniseren** in.
9. Selecteer in het veld  **Klantprijsgroep** de optie  **SHOPIFY**.
10. Selecteer in het veld **Klantenkortingsgroep** de optie **GROTE ACC**.
11. Kies **Prijzen synchroniseren** en wacht tot de synchronisatie van de prijzen is voltooid.

Bekijk in  **Shopify Beheer** de prijzen voor de **B2B** catalogus.

Open in de **online Shopify-winkel** de productcatalogus en zoek het product *ATHENS Desk*. Let op de prijs- en kortingsinformatie.

## Procedure: Afrekenen en ordersynchronisatie voor individuele kopers en bedrijfsvertegenwoordigers

Dit is een voortzetting van [Procedure: begin met het online verkopen van producten](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online). U kunt het ook met uw eigen gegevens proberen, bijvoorbeeld via uw Shopify store of sandbox.

Individuele koper

1. In de online **Shopify-winkel**. Kies het pictogram **Rekening** . Voer het e-mailadres in waartoe u toegang hebt.
2. Meld u aan met een eenmalige verificatiecode van 6 cijfers die u per e-mail heeft ontvangen.
3. Verken de productcatalogus. U zou alle producten met detailhandelsprijzen moeten kunnen zien.
4. Selecteer de Essential-variant, selecteer **Nu kopen** en ga door naar afrekenen.
5. Vul de velden **Voornaam** en **Achternaam** in.
6. Voer het lokale adres in.
7. Houd *Standaard* aan als verzendmethode.
8. Voer in het veld **Creditnummer kaart** 1 **in** als u **(voor het testen) Bogus Gateway** gebruikt, of voer **5555 5555 5555 4444** in als u **Shopify betalingen** in de testmodus gebruikt.
9. Voer in het veld **Vervaldatum** de huidige maand/jaar in.
10. Voer in het veld  **Beveiligingscode** **111** in.
11. Vul het veld **Naam op kaart** in.
12. Selecteer **Nu betalen**.

Bedrijfsvertegenwoordiger

[!INCLUDE [shopify-preview](../includes/shopify-preview.md)]

1. In **Shopify-beheer**.
2. Selecteer **Klanten** en vervolgens **Bedrijven** op de zijbalk van **Shopify-beheer**.
3. Open het item *School of Fine Art*.
4. Selecteer **[...]** in het **feitenvak van de** School of Fine Art, vervolgens **Betaalvoorwaarden bewerken** en selecteer vervolgens **Vervaldatum afhandeling**.
5. Kies  **[...]** in het **feitenvak Klanten**, vervolgens  **Klant toevoegen** en voeg vervolgens de klant toe met het e-mailadres dat u eerder hebt gebruikt om in te loggen in de winkel.
6. In de online **Shopify-winkel**. Kies het pictogram **Rekening** . Voer het e-mailadres in waartoe u toegang hebt.
7. Meld u aan met een eenmalige verificatiecode van 6 cijfers die u per e-mail heeft ontvangen.
8. Bekijk de productcatalogus. U ziet alleen producten die aan de B2B-catalogus zijn toegevoegd en die speciale verkoopprijzen hebben.
9. Selecteer de essentiële variant, selecteer  **Nu kopen** en ga naar de kassa.
10. Merk op dat de velden Account, Verzenden naar en Betaalmethode zijn ingevuld.
11. Vul het veld **PO-nummer** in met **PO-12345**.
12. Selecteer **Order verzenden**.

Voer in [!INCLUDE[prod_short](../includes/prod_short.md)] de volgende stappen uit:

1. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-orders** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer de actie **Orders synchroniseren vanuit Shopify**.
3. Selecteer **OK**.

De geïmporteerde order is klaar voor verwerking.

1. Selecteer de geïmporteerde order om de pagina  **Shopify Order**  te openen.
2. Merk op dat beide bestellingen door dezelfde persoon zijn geplaatst en aan twee verschillende klanten zijn gekoppeld.
3. In de namens het bedrijf ingediende bestelling ziet u een waarde in het veld  **Inkoopordernummer**, die ook wordt overgebracht naar het veld  **Extern documentnummer** van het aangemaakte verkoopdocument.
4. Omdat we het B2B-bedrijf hebben geconfigureerd om betalingen buiten  Shopify te verwerken, is de  **Financiële status** ingesteld op  **In behandeling**. Nadat u de betaling hebt ontvangen, selecteert u de actie  **Markeren als betaald** . De financiële statusupdates in Shopify.

## Procedure: Artikelen, klanten, bedrijven importeren uit Shopify

### Scenario 

U hebt al een succesvolle online winkel en wilt [!INCLUDE[prod_short](../includes/prod_short.md)] gebruiken als software voor bedrijfsbeheer. U wilt zoveel mogelijk gegevens importeren uit Shopify als mogelijk.

### Stappen

Dit is een vervolg op [Procedure: Beginnen met het online verkopen van producten](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online) en [Procedure: Uw klanten toevoegen aan uw nieuwe online winkel](walkthrough-setting-up-and-using-shopify.md#walkthrough-add-your-customers-to-your-new-online-store). U kunt het ook met uw eigen gegevens proberen, bijvoorbeeld via uw Shopify store of sandbox.

Volg in [!INCLUDE[prod_short](../includes/prod_short.md)] de volgende stappen.

#### Gegevens voorbereiden

1. Schakel over naar een gratis proefperiode van 30 dagen zonder voorbeeldgegevens. Zie voor meer informatie [Uw eigen gegevens toevoegen aan een lege proefversie](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions#add-your-own-data-to-an-empty-trial-company).
2. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en selecteer vervolgens de gerelateerde koppeling.
3. Selecteer **Nieuw**.
4. Voer in het veld  **Code**  **DEMO2** in.
5. Voer in het veld **Shopify-URL** de URL in van de online winkel waarmee u verbinding wilt maken.
6. Activeer de schakelaar **Geactiveerd** en bekijk en accepteer vervolgens de algemene voorwaarden.

Configureer de Shopify-winkel zoals hier beschreven:

1. Zet de schakelaar **Synchronisatie op achtergrond toestaan** uit.
2. Selecteer in het veld **Synchronisatie-item** de optie **Van Shopify**.
3. Schakel de schakelaar  **Automatisch onbekende items maken** in.
4. Vul in het veld **Artikelsjablooncode** de juiste sjabloon in.
5. Selecteer in het veld **Itemafbeeldingen synchroniseren** de optie **Van Shopify**.
6. Selecteer in het veld  **SKU toewijzing** de optie **Artikelnummer+ Variantcode**.
7. Selecteer in het veld  **Klantimport uit Shopify** de optie **Alle klanten**.
8. Zet de schakelaar **Automatisch onbekende klanten maken** aan.
9. Vul het veld **Klant-/bedrijfssjablooncode** in met de juiste sjabloon.
10. Selecteer in het veld  **Bedrijfsimport uit Shopify** de optie  **Alle klanten**.
11. Schakel de schakelaar  **Automatisch onbekend bedrijf maken** in.

#### De synchronisatie uitvoeren

1. Selecteer het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en selecteer vervolgens de gerelateerde koppeling.
2. Selecteer de *DEMO2*-winkel waarvoor u gegevens wilt synchroniseren om de pagina **Shopify-winkelkaart** te openen.
3. Selecteer **Producten synchroniseren**.
4. Selecteer **Productafbeeldingen synchroniseren**.
5. Selecteer **Klanten synchroniseren**.
6. Selecteer **Bedrijven synchroniseren**

### Resultaten

* Shopify-producten worden geïmporteerd. Selecteer ter verificatie het pictogram ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-producten** in en selecteer vervolgens de gerelateerde koppeling.
* Artikelen met afbeeldingen worden gemaakt. Selecteer ter verificatie het pictogram ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikel** in en selecteer de gerelateerde koppeling.
* Shopify klanten worden geïmporteerd. Selecteer ter verificatie het pictogram ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-Klanten** in en selecteer de gerelateerde koppeling.
* Shopify bedrijven worden geïmporteerd. Selecteer ter verificatie het pictogram ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-bedrijven** in en selecteer de gerelateerde koppeling.
* Er worden klanten gemaakt. Selecteer ter verificatie het pictogram ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en selecteer vervolgens de gerelateerde koppeling.

## Zie ook

[Aan de slag met de Shopify-connector](get-started.md)  
