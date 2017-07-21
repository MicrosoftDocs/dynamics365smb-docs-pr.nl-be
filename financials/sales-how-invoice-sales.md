---
title: Een verkoopfactuur of verkooporder maken | Microsoft Docs
description: Beschrijft hoe u een koopbrief, of een verkoopfactuur of verkooporder maakt, om de overeenkomst met een klant vast te leggen om producten onder bepaalde voorwaarden te verkopen.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bill, sale, invoice, order
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: fb4b1ad14dfedaeca38293e0e0b4496300090c17
ms.contentlocale: nl-be
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-invoice-sales"></a>Procedure: Verkoopbewerkingen
U maakt een verkoopfactuur of een verkooporder om uw overeenkomst met een klant vast te leggen om bepaalde producten tegen bepaalde leverings- en betalingsvoorwaarden te verkopen.  

> [!NOTE]  
>   Er zijn enkele scenario's waarin u een verkooporder moet gebruiken in plaats van een verkoopfactuur:  

* Als u slechts een deel van een bestelaantal moet verzenden, bijvoorbeeld omdat het totale aantal niet beschikbaar is.  
* Als u artikelen verkoopt die uw leverancier rechtstreeks aan uw klant levert, via zogeheten doorverzending. Zie [Procedure: Doorverzendingen maken](sales-how-drop-shipment.md) voor meer informatie.  

Wat betreft alle andere aspecten werken verkooporders en verkoopfacturen op dezelfde wijze. Zie [Procedure: Producten verkopen](sales-how-sell-products.md) voor meer informatie.

U kunt met de klant onderhandelen door eerst een verkoopofferte te maken, die u kunt omzetten in een verkoopfactuur wanneer er een overeenkomst is. Zie [Procedure: Voorstellen maken](sales-how-make-offers.md) voor meer informatie.

Als de klant wilt kopen, boekt u de verkoopfactuur om de gerelateerde aantallen en waarden in te voeren. Wanneer u de verkoopfactuur boekt, kunt u ook het document als een PDF-bijlage via e-mail versturen. U kunt ook de hoofdtekst van de e-mail vooraf invullen met een overzicht van de factuur- en betalingsgegevens, zoals een koppeling naar PayPal. Zie [Procedure: Documenten per e-mail verzenden](ui-how-send-documents-email.md) voor meer informatie.

In bedrijfsomgevingen waar de klant moet betalen voordat producten worden geleverd, zoals in de detailhandel, moet u wachten op de betalingsontvangst voordat u de producten levert. In de meeste gevallen verwerkt u inkomende betalingen enkele weken na levering door de betalingen te vereffenen met de gerelateerde geboekte, niet-betaalde verkoopfacturen. Zie voor meer informatie [Procedure: Betalingen reconciliëren met automatische vereffening](receivables-how-reconcile-payments-auto-application.md).

U kunt een geboekte verkoopfactuur gemakkelijk corrigeren of annuleren voordat het is betaald. Dit is bijvoorbeeld handig als u een typfout wilt corrigeren of als de klant in het begin van het orderproces verzoekt om een wijziging. Zie [Procedure: Onbetaalde verkoopfacturen corrigeren of annuleren](sales-how-correct-cancel-sales-invoice.md) voor meer informatie. Als de geboekte verkoopfactuur is betaald, moet u een verkoopcreditnota maken om de verkoop tegen te boeken. Zie [Procedure: Verkoopretouren of annuleringen verwerken](sales-how-process-sales-returns-cancellations.md) voor meer informatie.

Artikelen kunnen zowel voorraadartikelen als services zijn, aangeduid met de typen **Artikel - Voorraad** en **Artikel - Service** op de verkoopregels. Het verkoopfactureringsproces is hetzelfde voor beide artikeltypen. Zie [Procedure: Nieuwe artikelen registreren](inventory-how-register-new-items.md) voor meer informatie.

U kunt klantvelden op de verkoopfactuur op twee manieren invullen afhankelijk van de vraag of de klant reeds is geregistreerd. Zie de stappen 2 en 3 in de volgende procedure.

## <a name="to-create-a-sales-invoice"></a>Een verkoopfactuur maken
1. Kies op de startpagina de actie **Verkoopfactuur**.  
2. Voer in het veld **Klant** de naam in van een bestaande klant.

   Overige velden in het venster **Verkoopfactuur** bevatten standaardinformatie over de geselecteerde klant. Als de klant niet is geregistreerd, volgt u deze stappen:
3. Voer in het veld **Klant** de naam van de nieuwe klant in.
4. Kies in dialoogvenster voor het registreren van de nieuwe klant de knop **Ja**.
5. Kies in het venster **Selecteer een sjabloon voor een nieuwe klant** een sjabloon waarop u de nieuwe klantenkaart wilt baseren en kies vervolgens de knop **OK**.
6. In een nieuwe klantenkaart wordt de informatie uit de geselecteerde klantensjabloon getoond. Vul de overige velden in. Zie [Procedure: Nieuwe klanten registreren](sales-how-register-new-customers.md) voor meer informatie.  
7. Wanneer u de klantenkaart hebt voltooid, kiest u de knop **OK** om terug te keren naar het venster **Verkoopfactuur**.

   Verschillende velden op de verkoopfactuur worden nu ingevuld met gegevens die u hebt opgegeven op de nieuwe klantenkaart.  
8. Vul indien nodig de overige velden in het venster **Verkoopfactuur** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

U kunt nu verkoopfactuurregels invullen voor producten die u aan de klant verkoopt of voor elke transactie met de klant die u in een grootboekrekening wilt registreren.   

Als u terugkerende verkoopregels voor de klant hebt ingesteld, zoals een maandelijkse aanvullingsorder, kunt u deze regels invoegen op de order door de actie **Terugkerende verkoopregels ophalen** te kiezen.  
9. Selecteer op het sneltabblad **Regels** in het veld **Soort** het type product, kosten of transactie die u wilt boeken voor de klant met deze verkoopregel.
10. Voer in het veld **Nr.** een record die u wilt boeken op basis van de waarde in het veld **Soort**.

 Laat het veld **Nr.** leeg in de volgende gevallen: - Als de regel voor een opmerking is. Schrijf de opmerking in het veld **Omschrijving**.
 - Als de regel voor een niet-voorraadartikel is. Kies de actie **Niet-voorraadartikelen selecteren**. Zie voor meer informatie [Procedure: Werken met niet-voorraadartikelen](inventory-how-work-nonstock-items.md).

11. Voer in het veld **Aantal** hoeveel eenheden van het artikel, de kosten of de transactie met de regel voor de klant worden geregistreerd.  

    > [!NOTE]  
>   Als het een artikel van de soort **Artikel - Service** of **Resource** betreft, is de hoeveelheid een tijdseenheid, bijvoorbeeld uren, zoals aangegeven in het veld **Eenheidscode** op de regel.  

    De waarde in het veld **Regelbedrag** wordt berekend als *Eenheidsprijs* x *Aantal*.  

    De prijs en de regelbedragen worden weergegeven met of zonder btw, afhankelijk van wat u hebt geselecteerd in het veld **Prijzen inclusief btw** op de klantenkaart.  
12. Als u een korting wilt geven, kunt u een percentage invoeren in het veld **Regelkorting %**. De waarde in het veld **Regelbedrag** wordt dienovereenkomstig bijgewerkt.  

    Als u speciale artikelprijzen hebt ingesteld op het sneltabblad **Verkoopprijzen en verkoopregelkortingen** op de klantenkaart of de artikelkaart, worden de prijs en het bedrag op de offerteregel automatisch bijgewerkt als aan de overeengekomen prijscriteria wordt voldaan. Zie voor meer informatie [Afspraken over prijzen, kortingen en betalingen van verkopen vastleggen](sales-how-record-sales-price-discount-payment-agreements.md).  
13. Herhaal stap 9 t/m 12 voor elk product of kosteneenheid dat/die u aan de klant wilt verkopen.  

    De totalen onder de regels worden automatisch berekend wanneer u regels maakt of wijzigt.  
14. In het veld **Kortingsbedrag op factuur** voert u een bedrag in dat moet worden afgetrokken van de waarde in het veld **Totaal incl. btw**.

    Als u factuurkortingen voor de klant hebt opgegeven, wordt het opgegeven percentage automatisch ingevoegd in het veld **Factuurkorting %**als aan de voorwaarden wordt voldaan, en het gerelateerde bedrag wordt ingevoegd in het veld **Factuurkortingsbedrag excl. btw** . Zie voor meer informatie [Afspraken over prijzen, kortingen en betalingen van verkopen vastleggen](sales-how-record-sales-price-discount-payment-agreements.md).  
15. Wanneer de verkoopfactuurregels zijn ingevuld, kiest u de actie **Boeken en verzenden**.  

Het dialoogvenster **Boeken en verzenden bevestigen** geeft de manier aan waarop de klant de documenten wil ontvangen. U kunt de verzendmethode wijzigen door de opzoekknop voor het veld **Document verzenden naar** te kiezen. Zie [Procedure: Verzendprofielen voor documenten instellen](sales-how-setup-document-send-profiles.md) voor meer informatie.

Het gerelateerde artikel en de gerelateerde klantposten worden nu gemaakt in het systeem en de verkoopfactuur is uitvoer als een PDF-document. De verkoopfactuur wordt verwijderd uit de lijst met verkoopfacturen en wordt vervangen door een nieuw document in de lijst met geboekte verkoopfacturen.

## <a name="see-also"></a>Zie ook
[Verkoop](sales-manage-sales.md)  
[Verkopen instellen](sales-setup-sales.md)  
[Voorraad](inventory-manage-inventory.md)  
[Procedure: Documenten per e-mail verzenden](ui-how-send-documents-email.md)  
[Massaal factureren vanuit Microsoft Bookings in Dynamics 365 for Financials](finance-bookings.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

