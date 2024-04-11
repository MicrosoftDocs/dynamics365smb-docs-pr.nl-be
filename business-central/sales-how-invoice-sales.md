---
title: Verkopen factureren
description: 'Beschrijft hoe u een koopbrief, of een verkoopfactuur of verkooporder maakt, om de overeenkomst met een klant vast te leggen om producten onder bepaalde voorwaarden te verkopen.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'bill, sale, invoice, order'
ms.search.form: '43, 48, 9301'
ms.date: 03/21/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="invoice-sales"></a>Verkopen factureren

U kunt meestal een verkoopfactuur of een verkooporder maken om uw overeenkomst met een klant vast te leggen om bepaalde producten tegen bepaalde leverings- en betalingsvoorwaarden te verkopen.  

U moet echter een verkooporder gebruiken in plaats van een verkoopfactuur als u:  

* Slechts een deel van een bestelaantal nodig hebt, bijvoorbeeld omdat het totale aantal niet beschikbaar is.  
* Producten verzendt nadat u de bijbehorende verkoopfacturen hebt geboekt.
* Artikelen verkoopt die uw leverancier rechtstreeks aan uw klant levert, via zogeheten doorverzending. Meer informatie op [Doorverzendingen uitvoeren](sales-how-drop-shipment.md).  

In alle andere situaties werken verkooporders en verkoopfacturen op dezelfde wijze. Zie [Producten verkopen](sales-how-sell-products.md) voor meer informatie over hoe u verkooporders gebruikt.

U kunt met de klant onderhandelen door eerst een verkoopofferte te maken, die u kunt omzetten in een verkoopfactuur wanneer er een overeenkomst is. Ga voor meer informatie naar [Verkoopoffertes maken](sales-how-make-offers.md).

## <a name="create-sales-invoices"></a>Verkoopfacturen maken

Als de klant wilt kopen, boekt u de verkoopfactuur om de gerelateerde aantallen en waarden in te voeren. Wanneer u de verkoopfactuur boekt, kunt u het ook als een PDF-bijlage via e-mail versturen. U kunt ook de hoofdtekst van de e-mail vooraf invullen met een overzicht van de factuur- en betalingsgegevens, zoals een koppeling naar PayPal opgeven. Meer informatie op [Documenten per e-mail verzenden](ui-how-send-documents-email.md#to-send-documents-by-email). Als de klant de factuur betaalt, kunt u die betaling op verschillende manieren registreren, afhankelijk van de grootte en de geprefereerde werkstromen van uw organisatie. Meer informatie de sectie [Betalingen registreren](#register-payments).  

Artikelkaarten kunnen van het type **Voorraad**, **Service** en **Niet-voorraad** zijn om op te geven of het artikel respectievelijk een fysieke voorraadeenheid, een eenheid voor arbeidskosten of een fysieke eenheid die niet in voorraad wordt gehouden, is. Meer informatie op [Nieuwe artikelen registreren](inventory-how-register-new-items.md). Het verkoopfactureringsproces is hetzelfde voor alle drie de artikeltypen.

U kunt klantvelden op de verkoopfactuur op een van twee manieren invullen afhankelijk van de vraag of de klant reeds is geregistreerd. Zie stap 2 in de volgende procedure.

### <a name="to-create-a-sales-invoice"></a>Een verkoopfactuur maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopfacturen** in en kies vervolgens de gerelateerde koppeling.  
2. Voer in het veld **Klantnaam** de naam in van een bestaande klant. Als de klant echter nieuw is en daarom niet is geregistreerd, volg dan deze stappen om standaardklantinformatie in te vullen op de pagina **Verkoopfactuur**:

    1. Voer in het veld **Klantnaam** de naam van de nieuwe klant in.
    2. Kies in het dialoogvenster voor het registreren van de nieuwe klant **OK**.
    3. Kies op de pagina **Selecteer een sjabloon voor een nieuwe klant** een sjabloon waarop u de nieuwe klantenkaart wilt baseren en kies vervolgens **OK**.
    4. In een nieuwe klantenkaart wordt de informatie uit de geselecteerde klantensjabloon getoond. Vul de overige velden in. Meer informatie op [Nieuwe klanten registreren](sales-how-register-new-customers.md).  
    5. Wanneer u de klantenkaart hebt voltooid, kiest u de knop **Sluiten** om terug te keren naar de pagina **Verkoopfactuur**.

   Verschillende velden op de verkoopfactuur worden nu ingevuld met gegevens die u hebt opgegeven op de nieuwe klantenkaart.  
3. Vul desgewenst de overige velden op de pagina **Verkoopfactuur** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Als u toestaat dat de klant direct betaalt, bijvoorbeeld contant of met PayPal, vult u het veld **Betalingswijze** in. De betaling wordt vervolgens geregistreerd zodra u de verkoopfactuur boekt. Als u *Contant* selecteert, wordt de betaling geregistreerd in een opgegeven tegenrekening.

    U kunt nu het sneltabblad **Regels** invullen met producten die u aan de klant verkoopt of voor elke transactie met de klant die u in een grootboekrekening wilt registreren.

4. Selecteer op het sneltabblad **Regels** in het veld **Soort** het type product, kosten of transactie die u wilt boeken voor de klant op de verkoopregel.
   > [!TIP]
   > Als u terugkerende verkoopregels voor de klant hebt ingesteld, zoals een maandelijkse aanvullingsorder, kunt u deze regels invoegen op de order door de actie **Periodieke verkoopregels ophalen** te kiezen.
5. Kies in het veld **Nr.** een record die u wilt boeken op basis van de waarde in het veld **Soort**.

    Laat het veld **Nr.** leeg in de volgende gevallen:

    * Als de regel voor een opmerking is. Schrijf de opmerking in het veld **Omschrijving**.
    * Als de regel voor een catalogusartikel is. Kies de actie **Catalogusartikelen selecteren**. Meer informatie op [Werken met catalogusartikelen](inventory-how-work-nonstock-items.md).

6. Voer in het veld **Aantal** in hoeveel eenheden van het product, de kosten of de transactie met de regel voor de klant moeten worden geregistreerd.  

    > [!NOTE]  
    > Als het een artikel van de soort **Service** betreft of als het veld **Type** de waarde **Resource** bevat, is de hoeveelheid een tijdseenheid, bijvoorbeeld uren, zoals aangegeven in het veld **Eenheidscode** op de regel. Zie [Artikeleenheden instellen](inventory-how-setup-units-of-measure.md) voor meer informatie

    De waarde in het veld **Regelbedrag** wordt berekend als *Eenheidsprijs* x *Aantal*.  

    De prijs en de regelbedragen worden weergegeven met of zonder btw, afhankelijk van wat u hebt geselecteerd in het veld **Prijzen inclusief btw** op de klantenkaart.  
7. Als u een korting wilt geven, kunt u een percentage invoeren in het veld **Regelkorting %**. De waarde in het veld **Regelbedrag** wordt dienovereenkomstig bijgewerkt.  

    Als u speciale artikelprijzen hebt ingesteld op het sneltabblad **Verkoopprijzen en verkoopregelkortingen** op de klantenkaart of de artikelkaart en als aan de prijscriteria wordt voldaan, worden de prijs en het bedrag op de offerteregel automatisch bijgewerkt. Zie [Afspraken over prijzen, kortingen en betalingen van verkopen vastleggen](sales-how-record-sales-price-discount-payment-agreements.md) voor meer informatie.  
8. Herhaal stap 4 t/m 7 voor elk product of kosteneenheid waarvoor u de klant wilt factureren.

    De totalenvelden onder de regels worden automatisch bijgewerkt wanneer u regels maakt of wijzigt om de bedragen weer te geven die naar de grootboeken worden geboekt.

    > [!NOTE]
    > In zeer zeldzame gevallen kunnen de geboekte bedragen afwijken van wat wordt weergegeven in de totalenvelden. Dit is meestal het gevolg van afrondingsberekeningen met betrekking tot btw of omzetbelasting.<br /><br />Gebruik het feitenblok de **Klantstatistieken** om de bedragen die u boekt te verifiëren. Als u de actie **Vrijgeven** kiest, worden de waarden in de totalenvelden bijgewerkt met afrondingsberekeningen.

9. In het veld **Factuurkortingsbedrag excl. btw** voert u een bedrag in dat moet worden afgetrokken van de waarde in het veld **Totaal incl. btw**.

    Als u factuurkortingen voor de klant instelt, wordt het opgegeven percentage automatisch ingevoegd in het veld **Factuurkorting %** als aan de kortingsvoorwaarden wordt voldaan, en het gerelateerde bedrag wordt ingevoegd in het veld **Factuurkortingsbedrag excl. btw**. Zie [Afspraken over prijzen, kortingen en betalingen van verkopen vastleggen](sales-how-record-sales-price-discount-payment-agreements.md) voor meer informatie.

10. Wanneer de verkoopfactuurregels zijn ingevuld, kiest u de actie **Boeken en verzenden**.  

Het dialoogvenster **Boeken en verzenden bevestigen** geeft de manier aan waarop de klant de documenten wil ontvangen. U kunt de verzendmethode wijzigen door de opzoekknop voor het veld **Document verzenden naar** te kiezen. Zie [Verzendprofielen van documenten instellen](sales-how-setup-document-send-profiles.md) voor meer informatie.

Het gerelateerde artikel en de gerelateerde klantposten worden nu gemaakt in het systeem en de verkoopfactuur is uitvoer als een PDF-document. De verkoopfactuur wordt verwijderd uit de lijst met verkoopfacturen en wordt vervangen door een nieuw document in de lijst met geboekte verkoopfacturen.  

### <a name="calculate-invoice-discounts-on-sales"></a>Factuurkortingen op verkopen berekenen

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="posted-invoices"></a>Geboekte facturen

[!INCLUDE [posted-invoices](includes/posted-invoices.md)]

U kunt een geboekte verkoopfactuur gemakkelijk corrigeren of annuleren vóór de definitieve betaling. Dit is handig als u een typfout wilt corrigeren of als de klant om een wijziging in het begin van het orderproces verzoekt. Zie [Niet-betaalde verkoopfacturen corrigeren of annuleren](sales-how-correct-cancel-sales-invoice.md) voor meer informatie. Als de geboekte verkoopfactuur is betaald, moet u een verkoopcreditnota maken om de verkoop tegen te boeken. Zie [Verkoopretouren of annuleringen verwerken](sales-how-process-sales-returns-cancellations.md) voor meer informatie.  

[Open de lijst **Geboekte verkoopfacturen**](https://businesscentral.dynamics.com/?page=143) in [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="register-payments"></a>Betalingen registreren

Afhankelijk van uw zakelijke behoeften kunt u op verschillende manieren betaald krijgen en die betaling registreren: handmatig, automatisch en door middel van betalingsservices.  

U kunt de betalingen rechtstreeks van de klantenkaart verwerken. Gebruik de actie **Klantbetalingen registreren** om een overzicht te krijgen van onbetaalde facturen voor die klant. Markeer de factuur vervolgens als volledig of gedeeltelijk betaald. Deze betalingsreconciliatie verwerkt uw klantbetalingen door op uw bankrekening ontvangen bedragen te vergelijken met de gerelateerde onbetaalde verkoopfacturen. Vervolgens worden de betalingen geboekt. Zie voor meer informatie de sectie [Betalingen afzonderlijk reconciliëren](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-register-customer-payments-individually).  

In zakelijke omgevingen waar de klant enige tijd na levering betaalt. Volgens de betalingsvoorwaarden blijft een geboekte verkoopfactuur open (onbetaald) totdat de afdeling Debiteurenadministratie de betaling verifieert en toepast op de geboekte verkoopfactuur. Dit kan handmatig of automatisch worden uitgevoerd. Zie voor meer informatie [Klantbetalingen reconciliëren met het ontvangstendagboek of vanuit klantposten](receivables-how-apply-sales-transactions-manually.md) en [Betalingen reconciliëren met automatische vereffening](receivables-how-reconcile-payments-auto-application.md).  

In ondernemingsomgevingen waar de klant direct betaalt, bijvoorbeeld met PayPal of contant, wordt de betaling direct geregistreerd wanneer u de verkoopfactuur boekt, dat wil zeggen, de geboekte verkoopfactuur wordt gesloten als volledig vereffend. U selecteert de relevante methode in het veld **Betalingswijze** in de verkooporder. Voor elektronische betalingen, zoals PayPal, moet u ook het veld **Betalingsservice** invullen. Zie [Klantbetalingen via betalingsservices inschakelen](sales-how-enable-payment-service-extensions.md) voor meer informatie.

U kunt zelfs direct betaalde facturen voor niet-geregistreerde klanten maken door een kaart voor een contant betalende klant voor hen te maken, waarnaar u verwijst op de verkoopfactuur. Meer informatie op [Contant betalende klanten instellen](finance-how-to-set-up-cash-customers.md).  

> [!TIP]
> Als u uw klanten aanmaningen wilt sturen over achterstallige betalingen, moet u eerst aanmaningsniveaus en -voorwaarden instellen. Zie [De termijnen en niveaus van aanmaningen instellen](finance-setup-reminders.md) voor meer informatie.  

## <a name="external-document-numbers"></a>Externe documentnummers

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-also"></a>Zie ook

[Verkoop](sales-manage-sales.md)  
[Verkopen instellen](sales-setup-sales.md)  
[De picklijst afdrukken](sales-how-print-picking-list.md)  
[Voorraad](inventory-manage-inventory.md)  
[Documenten per e-mail verzenden](ui-how-send-documents-email.md#to-send-documents-by-email)  
[Openstaande saldi innen](receivables-collect-outstanding-balances.md)  
[Massaal factureren vanuit Microsoft Bookings in Business Central ](finance-bookings.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
