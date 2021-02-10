---
title: Een verkoopfactuur of verkooporder maken
description: Beschrijft hoe u een koopbrief, of een verkoopfactuur of verkooporder maakt, om de overeenkomst met een klant vast te leggen om producten onder bepaalde voorwaarden te verkopen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bill, sale, invoice, order
ms.date: 01/21/2021
ms.author: edupont
ms.openlocfilehash: b417ed7a4ef520ab652a66ac6f961c7c2f1a970e
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035418"
---
# <a name="invoice-sales"></a>Verkopen factureren

U maakt een verkoopfactuur of een verkooporder om uw overeenkomst met een klant vast te leggen om bepaalde producten tegen bepaalde leverings- en betalingsvoorwaarden te verkopen.  

Er zijn enkele scenario's waarin u een verkooporder moet gebruiken in plaats van een verkoopfactuur:  

* Als u slechts een deel van een bestelaantal moet verzenden, bijvoorbeeld omdat het totale aantal niet beschikbaar is.  
* Als u producten verzendt nadat u de bijbehorende verkoopfacturen hebt geboekt.
* Als u artikelen verkoopt die uw leverancier rechtstreeks aan uw klant levert, via zogeheten doorverzending. Zie [Doorverzendingen maken](sales-how-drop-shipment.md) voor meer informatie.  

Wat betreft alle andere aspecten werken verkooporders en verkoopfacturen op dezelfde wijze. Zie [Producten verkopen](sales-how-sell-products.md) voor meer informatie.

U kunt met de klant onderhandelen door eerst een verkoopofferte te maken, die u kunt omzetten in een verkoopfactuur wanneer er een overeenkomst is. Zie voor meer informatie [Verkoopoffertes maken](sales-how-make-offers.md).

Als de klant wilt kopen, boekt u de verkoopfactuur om de gerelateerde aantallen en waarden in te voeren. Wanneer u de verkoopfactuur boekt, kunt u ook het document als een PDF-bijlage via e-mail versturen. U kunt ook de hoofdtekst van de e-mail vooraf invullen met een overzicht van de factuur- en betalingsgegevens, zoals een koppeling naar PayPal. Zie [Documenten per e-mail verzenden](ui-how-send-documents-email.md) voor meer informatie. Als de klant de factuur dan betaalt, kunt u die betaling op verschillende manieren registreren, afhankelijk van de grootte en de geprefereerde werkstromen van uw organisatie. Zie voor meer informatie het gedeelte [Betalingen registreren](#registering-payments).  


U kunt een geboekte verkoopfactuur gemakkelijk corrigeren of annuleren voordat het is betaald. Dit is bijvoorbeeld handig als u een typfout wilt corrigeren of als de klant in het begin van het orderproces verzoekt om een wijziging. Zie voor meer informatie [Onbetaalde verkoopfacturen corrigeren of annuleren](sales-how-correct-cancel-sales-invoice.md). Als de geboekte verkoopfactuur is betaald, moet u een verkoopcreditnota maken om de verkoop tegen te boeken. Zie [Verkoopretouren of annuleringen verwerken](sales-how-process-sales-returns-cancellations.md) voor meer informatie.

De artikelkaart kan van het type **Voorraad**, **Service** en **Niet-voorraad** zijn om op te geven of het artikel een fysieke voorraadeenheid, een eenheid voor arbeidskosten of een fysieke eenheid die niet in voorraad wordt gehouden, is. Zie voor meer informatie [Nieuwe artikelen registreren](inventory-how-register-new-items.md). Het verkoopfactureringsproces is hetzelfde voor alle drie de artikeltypen.

U kunt klantvelden op de verkoopfactuur op twee manieren invullen afhankelijk van de vraag of de klant reeds is geregistreerd. Zie de stappen 2 en 3 in de volgende procedure.

## <a name="to-create-a-sales-invoice"></a>Een verkoopfactuur maken
1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopfacturen** in en kies de gerelateerde koppeling  
2. Voer in het veld **Klant** de naam in van een bestaande klant.

   Overige velden op de pagina **Verkoopfactuur** bevatten standaardinformatie over de geselecteerde klant. Als de klant niet is geregistreerd, volgt u deze stappen:
3. Voer in het veld **Klant** de naam van de nieuwe klant in.
4. Kies in dialoogvenster voor het registreren van de nieuwe klant de knop **Ja**.
5. Kies op de pagina **Selecteer een sjabloon voor een nieuwe klant** een sjabloon waarop u de nieuwe klantenkaart wilt baseren en kies vervolgens de knop **OK**.
6. In een nieuwe klantenkaart wordt de informatie uit de geselecteerde klantensjabloon getoond. Vul de overige velden in. Zie voor meer informatie [Nieuwe klanten registreren](sales-how-register-new-customers.md).  
7. Wanneer u de klantenkaart hebt voltooid, kiest u de knop **OK** om terug te keren naar de pagina **Verkoopfactuur**.

   Verschillende velden op de verkoopfactuur worden nu ingevuld met gegevens die u hebt opgegeven op de nieuwe klantenkaart.  
8. Vul desgewenst de overige velden op de pagina **Verkoopfactuur** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Als u toestaat dat de klant direct betaalt, bijvoorbeeld contant of met PayPal, vult u het veld **Betalingswijze** in. De betaling wordt vervolgens geregistreerd zodra u de verkoopfactuur boekt. Als u CONTANT selecteert, wordt de betaling geregistreerd in een opgegeven tegenrekening.

    U kunt nu verkoopfactuurregels invullen voor producten die u aan de klant verkoopt of voor elke transactie met de klant die u in een grootboekrekening wilt registreren.   

    Als u terugkerende verkoopregels voor de klant hebt ingesteld, zoals een maandelijkse aanvullingsorder, kunt u deze regels invoegen op de order door de actie **Terugkerende verkoopregels ophalen** te kiezen.  
9. Selecteer op het sneltabblad **Regels** in het veld **Soort** het type product, kosten of transactie die u wilt boeken voor de klant met deze verkoopregel.
10. Voer in het veld **Nr.** een record die u wilt boeken op basis van de waarde in het veld **Soort**.

    Laat het veld **Nr.** leeg in de volgende gevallen:

    * Als de regel voor een opmerking is. Schrijf de opmerking in het veld **Omschrijving**.
    * Als de regel voor een catalogusartikel is. Kies de actie **Catalogusartikelen selecteren**. Zie voor meer informatie [Werken met catalogusartikelen](inventory-how-work-nonstock-items.md).

11. Voer in het veld **Aantal** in hoeveel eenheden van het product, de kosten of de transactie met de regel voor de klant worden geregistreerd.  

    > [!NOTE]  
    > Als het een artikel van de soort **Service** betreft of als het veld **Type** de waarde **Resource** bevat, is de hoeveelheid een tijdseenheid, bijvoorbeeld uren, zoals aangegeven in het veld **Eenheidscode** op de regel. Zie [Artikeleenheden instellen](inventory-how-setup-units-of-measure.md) voor meer informatie

    De waarde in het veld **Regelbedrag** wordt berekend als *Eenheidsprijs* x *Aantal*.  

    De prijs en de regelbedragen worden weergegeven met of zonder btw, afhankelijk van wat u hebt geselecteerd in het veld **Prijzen inclusief btw** op de klantenkaart.  
12. Als u een korting wilt geven, kunt u een percentage invoeren in het veld **Regelkorting %**. De waarde in het veld **Regelbedrag** wordt dienovereenkomstig bijgewerkt.  

    Als u speciale artikelprijzen hebt ingesteld op het sneltabblad **Verkoopprijzen en verkoopregelkortingen** op de klantenkaart of de artikelkaart, worden de prijs en het bedrag op de offerteregel automatisch bijgewerkt als aan de overeengekomen prijscriteria wordt voldaan. Zie voor meer informatie [Afspraken over prijzen, kortingen en betalingen van verkopen vastleggen](sales-how-record-sales-price-discount-payment-agreements.md).  
13. Herhaal stap 9 t/m 12 voor elk product of kosteneenheid waarvoor u de klant wilt factureren.  

    De totalenvelden onder de regels worden automatisch bijgewerkt wanneer u regels maakt of wijzigt om de bedragen weer te geven die naar de grootboeken worden geboekt.

    > [!NOTE]
    > In zeer zeldzame gevallen kunnen de geboekte bedragen afwijken van wat wordt weergegeven in de totalenvelden. Dit is meestal het gevolg van afrondingsberekeningen met betrekking tot btw of omzetbelasting.<br /><br />Om de bedragen te controleren die daadwerkelijk worden geboekt, kunt u de pagina **Statistieken** gebruiken, die rekening houdt met de afrondingsberekeningen. Als u de actie **Vrijgeven** kiest, worden de totalenvelden ook bijgewerkt met afrondingsberekeningen.
14. In het veld **Kortingsbedrag op factuur** voert u een bedrag in dat moet worden afgetrokken van de waarde in het veld **Totaal incl. btw**.

    Als u factuurkortingen voor de klant hebt opgegeven, wordt het opgegeven percentage automatisch ingevoegd in het veld **Factuurkorting %** als aan de voorwaarden wordt voldaan, en het gerelateerde bedrag wordt ingevoegd in het veld **Factuurkortingsbedrag excl. btw** . Zie voor meer informatie [Afspraken over prijzen, kortingen en betalingen van verkopen vastleggen](sales-how-record-sales-price-discount-payment-agreements.md).  
15. Wanneer de verkoopfactuurregels zijn ingevuld, kiest u de actie **Boeken en verzenden**.  

Het dialoogvenster **Boeken en verzenden bevestigen** geeft de manier aan waarop de klant de documenten wil ontvangen. U kunt de verzendmethode wijzigen door de opzoekknop voor het veld **Document verzenden naar** te kiezen. Zie [Verzendprofielen voor documenten instellen](sales-how-setup-document-send-profiles.md) voor meer informatie.

Het gerelateerde artikel en de gerelateerde klantposten worden nu gemaakt in het systeem en de verkoopfactuur is uitvoer als een PDF-document. De verkoopfactuur wordt verwijderd uit de lijst met verkoopfacturen en wordt vervangen door een nieuw document in de lijst met geboekte verkoopfacturen.  

### <a name="calculating-invoice-discounts-on-sales"></a>Factuurkortingen op verkopen berekenen

[!INCLUDE [sales-invoice-discounts](includes/sales-invoice-discounts.md)]

## <a name="registering-payments"></a>Betalingen registreren

Afhankelijk van uw zakelijke behoeften kunt u op verschillende manieren betaald krijgen en die betaling registreren: handmatig, automatisch en door middel van betalingsservices.  

U kunt de betalingen rechtstreeks van de klantenkaart verwerken. Gebruik de actie **Klantbetalingen registreren** om een overzicht te krijgen van onbetaalde facturen voor die klant. Markeer de factuur vervolgens als volledig of gedeeltelijk betaald. Deze betalingsreconciliatie verwerkt uw klantbetalingen door op uw bankrekening ontvangen bedragen te vergelijken met de gerelateerde onbetaalde verkoopfacturen. Vervolgens worden de betalingen geboekt. Zie voor meer informatie [Betalingen afzonderlijk reconciliëren](receivables-how-reconcile-customer-payments-list-unpaid-sales-documents.md#to-register-customer-payments-individually).  

In ondernemingsomgevingen waar de klant enige tijd na levering betaalt, volgens de betalingsconditie, blijft een geboekte verkoopfactuur open (onbetaald) totdat de afdeling Vorderingen controleert of de betaling is ontvangen en de betaling vereffent met de geboekte verkoopfactuur. Dit kan handmatig of automatisch worden uitgevoerd. Zie voor meer informatie [Klantbetalingen reconciliëren met het ontvangstendagboek of vanuit klantposten](receivables-how-apply-sales-transactions-manually.md) en [Betalingen reconciliëren met automatische vereffening](receivables-how-reconcile-payments-auto-application.md).  

In ondernemingsomgevingen waar de klant direct betaalt, bijvoorbeeld met PayPal of contant, wordt de betaling direct geregistreerd wanneer u de verkoopfactuur boekt, dat wil zeggen, de geboekte verkoopfactuur wordt gesloten als volledig vereffend. U selecteert de relevante methode in het veld **Betalingswijze** in de verkooporder. Zie onder stap 8. Voor elektronische betalingen, zoals PayPal, moet u ook het veld **Betalingsservice** invullen. Zie [Klantbetalingen via betalingsservices inschakelen](sales-how-enable-payment-service-extensions.md) voor meer informatie.  

U kunt zelfs direct betaalde facturen voor niet-geregistreerde klanten maken door eerst een kaart voor een contant betalende klant te maken, waarnaar u verwijst op de verkoopfactuur. Raadpleeg voor meer informatie [Contant betalende klanten instellen](finance-how-to-set-up-cash-customers.md).  

> [!TIP]
> Als u uw klanten herinneringen wilt sturen over achterstallige betalingen, moet u herinneringsniveaus en -voorwaarden instellen. Zie voor meer informatie [De termijnen en niveaus van aanmaningen instellen](finance-setup-reminders.md).  

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/invoicing-customers-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Verkoop](sales-manage-sales.md)  
[Verkopen instellen](sales-setup-sales.md)  
[De picklijst afdrukken](sales-how-print-picking-list.md)  
[Voorraad](inventory-manage-inventory.md)  
[Documenten per e-mail verzenden](ui-how-send-documents-email.md)  
[Openstaande saldi innen](receivables-collect-outstanding-balances.md)  
[Massaal factureren vanuit Microsoft Bookings in Business Central ](finance-bookings.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)
