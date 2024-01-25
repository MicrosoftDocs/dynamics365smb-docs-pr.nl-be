---
title: De Shopify-connector instellen en gebruiken
description: Verschillende integratiescenario's voor het demonstreren van de werkstroom tussen Shopify en Business Central
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '30101, 30102, 30106, 30107, 30113, 30115, 30126'
ms.reviewer: solsen
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

Meer informatie over het maken van Shopify-proefversies en aanbevolen instellingen vindt u op [Shopify-account maken en instellen](shopify-account.md).

### Business Central

U hebt een [!INCLUDE[prod_short](../includes/prod_short.md)]-account nodig. 

U kunt bijvoorbeeld een demo-account maken of een proefversie starten. Lees hier meer over [Demonstratieomgevingen voorbereiden van Dynamics 365 Business Central](/dynamics365/business-central/dev-itpro/administration/demo-environment) en [Aanmelden voor de proefperiode](../trial-signup.md). 

## Business Central verbinden met de online Shopify-winkel

Ga in [!INCLUDE[prod_short](../includes/prod_short.md)] op een van de volgende manieren te werk:

1. Kies het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Voer `DEMO1` in het veld **Code** in.
4. Voer in het veld **Shopify-URL** de URL in van de online winkel waarmee u verbinding wilt maken.
5. Activeer de schakelaar **Geactiveerd** en bekijk en accepteer de algemene voorwaarden.

Configureer de Shopify-winkel zoals beschreven in de volgende stappen:

1. Zet de schakelaar **Synchronisatie op achtergrond toestaan** uit.
2. Selecteer *Naar Shopify* in het veld **Artikel synchroniseren**.
3. Selecteer *Naar Shopify* in het veld **Artikelafbeeldingen synchroniseren**.
4. Zet de schakelaar **Artikelkenmerken synchroniseren** aan.
5. Zet de schakelaar **Voorraad getraceerd** aan.
6. Selecteer *Weigeren* in het veld **Standaardvoorraadbeleid** .
7. Zet de schakelaar **Automatisch onbekende klanten maken** aan.
8. Vul in het veld **Klantensjablooncode** de juiste sjabloon in.
9. Vul de **Rekening voor verzendkosten** en de **Fooienrekening** in met de opbrengstrekening. Gebruik in de VS bijvoorbeeld `40100`.
10. Zet de schakelaar **Automatisch orders maken** aan.

Locatietoewijzing configureren:

1. Kies de actie **Vestigingen** om **Shopify-winkellocaties** te openen.
2. Kies de actie **Shopify-vestigingen ophalen** om alle vestigingen te importeren die zijn gedefinieerd in Shopify. Uw standaardlocatie selecteren in Shopify
3. Voer in het **Vestigingsfilter** `''|EAST|MAIN` in.
4. Zet de schakelaar **Standaardproductvestiging** aan.
5. Selecteer *Gepland beschikbaar saldo vandaag* in het veld **Voorraadberekening** om voorraadsynchronisatie in te schakelen voor de geselecteerde Shopify-vestiging.

## Procedure: begin met het online verkopen van producten

### Scenario

Stel dat u Shopify als online winkel wilt proberen zonder veel tijd te besteden aan het opzetten van dingen, vooral omdat u uw artikelen al goed in [!INCLUDE[prod_short](../includes/prod_short.md)] onderhoudt. Nadat u uw online Shopify-winkel hebt gestart, krijgt u meteen nieuwe klanten die blij zijn met uw winkel en hun koopervaring. Dus besluiten ze om fooien te geven bij het afrekenen.

### Stappen

Doorloop in [!INCLUDE[prod_short](../includes/prod_short.md)] de volgende stappen:

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-producten** in en kies de gerelateerde koppeling.
2. Kies de actie **Artikelen toevoegen**.
3. Voer *DEMO1* in het veld **Code** in.
4. Stel het filter `CHAIR` in op het veld **Artikelcategoriecode** (voeg indien nodig een filterveld toe).
5. Selecteer **OK** en wacht tot de eerste synchronisatie van artikelen en prijzen is voltooid.
6. Kies de actie **Productafbeeldingen synchroniseren**.
7. Kies de actie **Voorraad synchroniseren**.

In online **Shopify-winkel**
> [!Tip]  
> Open **Shopify-beheer** door te navigeren naar de URL die is opgegeven in het veld **URL** van de pagina **Shopify - Winkelkaart**. Kies vervolgens het oogpictogram naast het verkoopkanaal **Online winkel**, op de zijbalk van **Shopify-beheer**. 

Open de productcatalogus. Kennisgeving:

* Producttitels, afbeeldingen en prijzen.
* Beschikbaarheidsindicator (uitverkocht voor producten die niet op voorraad zijn).

Kies elk product dat kan worden verkocht, bijvoorbeeld de `BERLIN Swivel Chair, yellow`. Merk op dat de beschrijving artikelkenmerken bevat.

Kies de knop **Nu kopen** en ga verder met afrekenen.

1. Voer in het veld **E-mail of mobiel telefoonnummer** `cl@contoso.com` in (of het e-mailadres waarop u bestel- en verzendbevestigingen wilt ontvangen).
2. Bij **Voornaam** en **Achternaam** voert u `Claudia Lawson` in.
3. Voer het lokale adres in.
4. Schakel het selectievakje **Deze informatie opslaan voor de volgende keer** in.
5. Kies de knop **Doorgaan naar verzending**.
6. Houd `Standard` aan als verzendmethode en kies vervolgens de knop **Doorgaan naar betaling** .
7. Selecteer `10%` fooi.
8. Voer in het veld **Creditcard** `1` in als u *(voor testen) Bogus Gateway* gebruikt, of voer `5555 5555 5555 4444` in als u *Shopify payments* in de testmodus gebruikt.
9. Vul het veld **Naam op kaart** in.
10. Voer in het veld **Vervaldatum** de huidige maand/jaar in.
11. Voer `111` in het veld **Beveiligingscode** in.
12. Kies de knop **Nu betalen**.

Voer in [!INCLUDE[prod_short](../includes/prod_short.md)] de volgende stappen uit:

1. Kies het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), **Shopify-orders** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Orders synchroniseren vanuit Shopify**.
3. Klik op **OK**.

De geïmporteerde order is klaar voor verwerking.

1. Selecteer de geïmporteerde order om het venster **Shopify-order** te openen.
2. U ziet dat de nieuwe klant en verkooporder zijn gemaakt.
3. Verken de acties **Risico** en **Verzendkosten**.
4. Kies de actie **Verkooporder** om het venster **Verkooporder** te openen. Verkooporder is een vraag, die indien nodig kan worden gedekt door assemblage, productie of inkoop met behulp van de planningsengine. Het ondersteunt ook verschillende magazijnafhandelingsprocessen met volledige scheiding van taken.
5. Kies de actie **Opnieuw openen**.
6. Voer in het veld **Agent** `DHL` in.
7. Voer in het veld **Traceringsnummer (zending)** `123456789` in.
8. Kies de actie **Boeken**, houd de optie **Verzenden en factureren** en kies vervolgens de knop **OK**.

Nu worden fysieke en financiële gegevens geregistreerd [!INCLUDE[prod_short](../includes/prod_short.md)]. Het is tijd om aan Shopify de wijzigingen door te geven.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verzendingen combineren met Shopify** in en kies vervolgens de gerelateerde koppeling.
2. Klik op **OK**.

U ziet in **Shopify-beheer** dat de order nu is gemarkeerd als *Afgehandeld*. U kunt daar ook de verzendgegevens bekijken en de tracerings-URL zien. Als u **Orders synchroniseren vanuit Shopify** opnieuw uitvoert, wordt de order in beide systemen gearchiveerd.

## Procedure: Nodig uw klanten uit voor uw nieuwe online winkel

### Scenario

Na een succesvolle snelle opening van uw nieuwe online winkel, wilt u dat uw huidige klanten deze bezoeken en beginnen met het plaatsen van orders.

### Stappen

Ga in [!INCLUDE[prod_short](../includes/prod_short.md)] op een van de volgende manieren te werk:

1. Kies het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de **DEMO1**-winkel waarvoor u klanten wilt synchroniseren om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Klanten synchroniseren**.

U ziet in **Shopify-beheer** dat de klanten zijn geïmporteerd. Open een van de klanten en zie dat de voor- en achternaam van de klant afkomstig zijn uit het veld **Contactnaam** van de **Klantenkaart**. De bedrijfsnaam is terug te vinden in het standaardadres, gekoppeld aan de klant. Kies **Accountuitnodiging verzenden** om de klant uit te nodigen.

## Procedure: Artikelbeheer fijn afstemmen

### Scenario 

U wilt graag meer flexibiliteit en controle toevoegen aan uw processen rondom artikelbeheer. U wilt de productbeschrijving verbeteren en meer beoordelingsstappen toevoegen voordat producten beschikbaar komen voor de eindklant.

### Stappen

Ga in [!INCLUDE[prod_short](../includes/prod_short.md)] op een van de volgende manieren te werk:

Bereid gegevens voor.

1. Kies het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Klantenprijsgroep** in en kies vervolgens de gerelateerde koppeling.
2. Voeg een nieuwe prijsgroep toe. Voer `SHOPIFY` in het veld **Code** in.
3. Sluit het venster **Klantenprijsgroep**.
4. Kies het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikelen** in en kies de gerelateerde koppeling.

Selecteer artikel **1896-S, Athens Desk** en voer de volgende stappen uit.

1. Kies de actie **Varianten** en voeg vervolgens twee varianten toe, `PREMIUM, Athens Desk, Premium edition` en `ESSENTIAL, Athens Desk, Essential edition`.
2. Kies de actie **Uitgebreide tekst** en maak een nieuwe uitgebreide tekst die geldig is voor alle taalcodes. Voer in het veld **Beschrijving** `Shopify` in. 
3. Voeg de volgende tekst toe met HTML-tags: `<b>Simple stylish design</b> blends with any ensemble. <i>Available in two editions.</i>`. Sluit de pagina **Uitgebreide tekst** en ga terug naar de artikelkaart.
4. Kies de actie **Verkoopprijzen** en voeg nieuwe prijzen toe zoals weergegeven in de volgende tabel:

  |Lijn|**Verkoopsoort**|**Verkoopscode**|Type|Code|Variantcode<br>(voeg het veld toe via personalisatie)|Eenheidsprijs|
  |------|------------|------------|------------|------------|------------|------------|
  |1|Klantenprijsgroep|SHOPIFY|Artikel|1896-S|ESSENTIAL|700|
  |2|Klantenprijsgroep|SHOPIFY|Artikel|1896-S|PREMIUM|1000|

5. Kies de actie **Verkoopkortingen** en voeg een nieuwe korting toe:

* **Verkoopsoort** *Klantenkortingsgroep*
* **Verkoopcode** *DET.HANDEL*
* **Soort** *Artikel*
* **Code** *1896-S*
* **Code van maateenheid** *Per stuk*
* **Regelkorting %** *10*

6. Kies de actie **Artikelverwijzingen** en voeg de volgende regels toe:

  |Lijn|**Referentiesoort**|**Referentienr.**|Variantcode|
  |------|------------|------------|------------|
  |1|Barcode|77777777|ESSENTIAL|
  |2|Barcode|11111111|PREMIUM|


Selecteer het artikel **1920-S, ANTWERP Conferentietafel** en voer de volgende stappen uit.

1. Kies **Voorraad aanpassen** en voer in het veld **Nieuwe voorraad** `100` in voor de vestigingen *OOST* en *WEST*. 
2. Klik op **OK**.

Pas de synchronisatie-instellingen aan.

1. Kies het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de *DEMO1*-winkel waarvoor u artikelen wilt synchroniseren om de pagina Shopify-winkelkaart te openen.
3. Selecteer *SHOPIFY* in het veld **Klantenprijsgroep**.
4. Selecteer *DET.HANDEL* in het veld **Klantenkortingsgroep**.
5. Schakel het veld **Uitgebreide tekst voor synchronisatieartikel** in.
6. Selecteer *Artikelnr. + variant* in het veld **SKU-toewijzing**.
7. Selecteer **Concept** in het veld *Status voor gemaakte producten*.
8. Selecteer **Status naar gearchiveerd** in het veld *Actie voor verwijderd product*.

Voer de synchronisatie uit.

1. Kies het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de *DEMO1*-winkel waarvoor u artikelen wilt synchroniseren om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Producten** om het venster **Shopify-producten** te openen.
4. Kies de actie **Artikelen toevoegen**.
5. Stel het filter **TABEL|BUREAU** in op het veld *Artikelcategoriecode*.
6. Kies de actie **Productafbeeldingen synchroniseren**.
7. Kies de actie **Voorraad synchroniseren**.

Producten worden toegevoegd. Merk op dat de status is ingesteld op *Concept* en dat artikelen daarom niet zichtbaar zijn in de online Shopify-winkel.

1. Selecteer de regel met het artikel *1920-S, ANTWERP Conference Table*. Voer bij de **SEO-titel** `Rectangular meeting table Antwerp, 10 seats, black` in.
2. Selecteer in het veld **Status** de optie *Actief*.
3. Selecteer de regel met artikel *1906-S, ATHENS, Mobile Pedestal* en kies vervolgens de actie **Verwijderen**.

U ziet in **Shopify-beheer** dat alle producten verschillende statussen hebben.

* *ANTWERP Conference Table* is *Actief* omdat we de status hebben gewijzigd in het venster **Shopify-product**.
* *ATHENS Desk* is *Concept* omdat we de standaardstatus voor alle toegevoegde producten hebben geconfigureerd als *Concept*.
* *ATHENS Mobile Pedestal* is *Gearchiveerd* omdat we de winkel hebben geconfigureerd om automatisch de status *Gearchiveerd* toe te wijzen voor verwijderde producten.

Merk op dat de voorraad voor ANTWERP Conference Table 100 is, omdat we het systeem hebben geconfigureerd om alleen voorraad te gebruiken uit twee vestigingen, HOOFD en OOST. Voorraad op andere vestigingen (WEST) wordt genegeerd.

* Open *ANTWERP Conference Table*, let op de velden **Aangepast type**, **Leverancier**, **Gewicht**, **Kosten per artikel** en het gedeelte **Voorbeeld van zoekprogrammavermelding**.
* Open *Athens Desk*, schuif omlaag naar het gedeelte **Varianten** en kijk hoe **SKU** is gevuld.
* Kies **Bewerken** om de streepjescode en prijzen te bekijken.
* Wijzig de status van *Athens Desk* in *Actief* en kies de actie **Voorbeeld**.

Open in de **online Shopify-winkel** de productcatalogus en zoek het product *ATHENS Desk*. Merk op dat er verschillende opties beschikbaar zijn. Voor verschillende opties zijn de prijzen verschillend. Let op kortingsinformatie.

## Procedure: Artikelen importeren uit Shopify

### Scenario 

U hebt al een succesvolle online winkel en wilt [!INCLUDE[prod_short](../includes/prod_short.md)] gebruiken als software voor bedrijfsbeheer. U wilt zoveel mogelijk gegevens importeren uit Shopify als mogelijk. 

### Stappen

Dit is een voortzetting van [Procedure: begin met het online verkopen van producten](walkthrough-setting-up-and-using-shopify.md#walkthrough-start-selling-products-online). U kunt het ook proberen met uw eigen gegevens, bijvoorbeeld uw Shopify-winkel of sandbox.

Ga in [!INCLUDE[prod_short](../includes/prod_short.md)] op een van de volgende manieren te werk:

#### Gegevens voorbereiden

1. Schakel over naar een gratis proefperiode van 30 dagen zonder voorbeeldgegevens. Zie voor meer informatie [Uw eigen gegevens toevoegen aan een lege proefversie](/dynamics365/business-central/dev-itpro/administration/trials-subscriptions#add-your-own-data-to-an-empty-trial-company).
2. Kies het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
3. Kies de actie **Nieuw**.
4. Voer `DEMO2` in het veld **Code** in.
5. Voer in het veld **Shopify-URL** de URL in van de online winkel waarmee u verbinding wilt maken.
6. Activeer de schakelaar **Geactiveerd** en bekijk en accepteer de algemene voorwaarden.

Configureer de Shopify-winkel zoals hieronder beschreven in de volgende stappen:

7. Zet de schakelaar **Synchronisatie op achtergrond toestaan** uit.
8. Selecteer *Van Shopify* in het veld **Artikel synchroniseren**.
9. Zet de schakelaar **Automatisch onbekende artikelen maken** aan.
10. Vul in het veld **Artikelsjablooncode** de juiste sjabloon in.
11. Selecteer *Van Shopify* in het veld **Artikelafbeeldingen synchroniseren**.
12. Selecteer *Alle klanten* bij **Klant importeren vanuit Shopify**.
13. Zet de schakelaar **Automatisch onbekende klanten maken** aan.

#### De synchronisatie uitvoeren

1. Kies het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Shopify-winkels** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de *DEMO2*-winkel waarvoor u gegevens wilt synchroniseren om de pagina **Shopify-winkelkaart** te openen.
3. Kies de actie **Producten synchroniseren**.
4. Kies de actie **Productafbeeldingen synchroniseren**.
5. Kies de actie **Klanten synchroniseren**.

### Resultaten

* Shopify-producten worden geïmporteerd. Kies ter verificatie het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-producten** in en kies de gerelateerde koppeling.
* Artikelen met afbeeldingen worden gemaakt. Kies ter verificatie het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikel** in en kies de gerelateerde koppeling.
* Shopify-klanten worden geïmporteerd. Kies ter verificatie het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-klanten** in en kies de gerelateerde koppeling.
* Er worden klanten gemaakt. Kies ter verificatie het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** in en kies de gerelateerde koppeling.


## Zie ook

[Aan de slag met de Shopify-connector](get-started.md)  
