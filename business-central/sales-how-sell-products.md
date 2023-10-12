---
title: Een klantverkooporder maken en producten verkopen
description: Beschrijft hoe u een verkooporder maakt om uw overeenkomst vast te leggen met een klant om producten onder bepaalde voorwaarden te verkopen of te verhandelen.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'trade, partial deliveries, customer sales order, shipping advice, partial shipments,'
ms.search.form: '42, 48, 9305'
ms.date: 09/02/2022
ms.author: bholtorf
---
# <a name="sell-products-with-a-customer-sales-order"></a>Producten verkopen met een klantverkooporder

Dit artikel biedt gebruikers richtlijnen over wanneer u een klantverkooporder zou moeten gebruiken naast een factuur. Als uw verkoopproces vereist dat u alleen delen van een orderaantal verzendt, bijvoorbeeld omdat de volledige hoeveelheid niet in één keer beschikbaar is, moet u die verkoop verwerken door een verkooporder te maken.

Als u artikelen verkoopt door rechtstreeks van uw leverancier bij de klant te leveren, als een doorverzending, moet u ook verkooporders gebruiken. Meer informatie op [Doorverzendingen uitvoeren](sales-how-drop-shipment.md). Wat betreft alle andere aspecten werken verkooporders op dezelfde manier als verkoopfacturen. Zie voor meer informatie [Verkopen factureren](sales-how-invoice-sales.md).

Als u de producten volledig of gedeeltelijk levert, boekt u de verkooporder als verzonden of als verzonden en gefactureerd om het gerelateerde artikel en de klantposten in uw systeem te maken. Wanneer u de verkooporder boekt, kunt u deze ook als een PDF-bijlage via e-mail versturen. U kunt de hoofdtekst van de e-mail vooraf invullen met een overzicht van de orde- en betalingsgegevens, zoals een koppeling naar PayPal. Zie voor meer informatie [Artikelen verzenden](warehouse-how-ship-items.md) en [Documenten per e-mail verzenden](ui-how-send-documents-email.md).

In ondernemingsomgevingen waar de klant direct betaalt, bijvoorbeeld met PayPal of contant, wordt de betaling direct geregistreerd wanneer u de verkooporder als gefactureerd boekt, dat wil zeggen, de geboekte verkoopfactuur wordt gesloten als volledig vereffend. U selecteert de relevante methode in het veld **Betalingswijze** in de verkooporder. Zie stap 5 hieronder. Voor elektronische betalingen, zoals PayPal, moet u ook het veld **Betalingsservice** invullen. Zie [Klantbetalingen via betalingsservices inschakelen](sales-how-enable-payment-service-extensions.md) voor meer informatie.

U kunt zelfs direct betaalde orders voor niet-geregistreerde klanten maken door eerst een kaart voor een contant betalende klant te maken, waarnaar u verwijst op de verkooporder. Meer informatie op [Contant betalende klanten instellen](finance-how-to-set-up-cash-customers.md).

## <a name="create-a-sales-order"></a>Een verkooporder maken

> [!NOTE]  
> Bij de volgende procedure wordt ervan uitgegaan dat de klant al is ingesteld. Voor instructies om dit te doen raadpleegt u [Nieuwe klanten registreren](sales-how-register-new-customers.md).

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkooporders** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer **Nieuw** om een nieuwe post te maken.
3. Voer in het veld **Klant** de naam in van een bestaande klant.

    Overige velden op de pagina **Verkooporder** worden nu ingevuld met de standaardinformatie over de geselecteerde klant.  

4. Vul desgewenst de overige velden op de pagina **Verkooporder** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    > [!NOTE]  
    > Als u toestaat dat de klant direct betaalt, bijvoorbeeld met creditcard of PayPal, vult u het veld **Betalingswijze** in. De betaling wordt vervolgens geregistreerd zodra u de verkooporder als gefactureerd boekt. Als u *contant* selecteert, wordt de betaling geregistreerd in een opgegeven tegenrekening.

    U kunt nu de verkooporderregels invullen met voorraadartikelen of services die u de klant wilt laten kopen.

    Als u terugkerende verkoopregels voor de klant hebt ingesteld, zoals een maandelijkse aanvullingsorder, kunt u deze regels invoegen op de order door de actie **Periodieke verkoopregels ophalen** te kiezen.
5. Selecteer op het sneltabblad **Regels** in het veld **Soort** het type product, kosten of transactie die u wilt boeken naar de klant op de verkoopregel.

6. Kies in het veld **Nr.** het nummer in van een voorraadartikel of service.

    Laat het veld **Nr.** leeg als de regel is voor een:

    * Opmerking. Schrijf de opmerking in het veld **Omschrijving**.
    * Catalogusartikel. Kies de actie **Catalogusartikelen selecteren**. Meer informatie op [Werken met catalogusartikelen](inventory-how-work-nonstock-items.md).
7. Geef in het veld **Aantal** op hoeveel artikelen u wilt verkopen.

    > [!NOTE]  
    > Voor artikelen van de soort *Resource* of *Service* is de hoeveelheid een tijdseenheid, bijvoorbeeld uren, zoals aangegeven in het veld **Eenheidscode** op de regel. Zie [Artikeleenheden instellen](inventory-how-setup-units-of-measure.md) voor meer informatie.

    Het veld **Regelbedrag** wordt bijgewerkt met de waarde in het veld **Eenheidsprijs**, vermenigvuldigd met het getal in het veld **Aantal**.

    De prijs en de regelbedragen worden weergegeven met of zonder btw afhankelijk van wat u hebt geselecteerd in het veld **Prijzen inclusief btw** op de klantenkaart.
8. In het veld **Regelkorting %** voert u een percentage in als u de klant een korting op het product wilt verlenen. De waarde in het veld **Regelbedrag** wordt dienovereenkomstig bijgewerkt.

    Als u speciale artikelprijzen hebt ingesteld op het sneltabblad **Verkoopprijzen en verkoopregelkortingen** op de klantenkaart of de artikelkaart, worden de prijs en het bedrag op de offerteregel automatisch bijgewerkt als aan de overeengekomen prijscriteria is voldaan. Zie [Afspraken over prijzen, kortingen en betalingen van verkopen vastleggen](sales-how-record-sales-price-discount-payment-agreements.md) voor meer informatie.
9. Als u een opmerking over de orderregel wilt toevoegen die de klant op de afgedrukte verkooporder kan zien, schrijft u een opmerking op een lege regel in het veld **Omschrijving**.  
10. Herhaal stap 5 tot en met 9 voor elk artikel dat u de klant wilt laten kopen.

    De totalenvelden onder de regels worden automatisch bijgewerkt wanneer u regels maakt of wijzigt om de bedragen weer te geven die naar de grootboeken worden geboekt.

    > [!NOTE]
    > In zeer zeldzame gevallen kunnen de geboekte bedragen afwijken van wat wordt weergegeven in de totalenvelden. Dit is meestal het gevolg van afrondingsberekeningen met betrekking tot btw of omzetbelasting.
    >
    > Om de bedragen te controleren die daadwerkelijk worden geboekt, kunt u de pagina **Statistieken** gebruiken, die rekening houdt met de afrondingsberekeningen. Als u de actie **Vrijgeven** kiest, worden de totalenvelden ook bijgewerkt met afrondingsberekeningen.  

11. Voer desgewenst in het veld **Kortingsbedrag op factuur** het bedrag in dat moet worden afgetrokken van de waarde in het veld **Totaal incl. btw**.

    Als u factuurkortingen voor de klant hebt opgegeven, wordt het opgegeven percentage automatisch ingevoegd in het veld **Factuurkorting %** als aan de voorwaarden wordt voldaan, en het gerelateerde bedrag wordt ingevoegd in het veld **Factuurkortingsbedrag excl. btw**. Zie [Afspraken over prijzen, kortingen en betalingen van verkopen vastleggen](sales-how-record-sales-price-discount-payment-agreements.md) voor meer informatie.
12. Als u slechts een deel van het orderaantal wilt verzenden, voert u dat aantal in het veld **Te verzenden aantal** in. De waarde wordt automatisch gekopieerd naar **Te factureren aantal**.

    > [!NOTE]
    > Als het veld **Verzendadvies** is ingesteld als **Compleet** op het sneltabblad **Verzending en facturering**, u kunt geen deelzendingen boeken. Zie voor meer informatie [Gedeeltelijke verzendingen verwerken](sales-how-send-partial-shipments.md).
13. Als u slechts een deel van het verzonden aantal wilt factureren, voert u dat aantal in het veld **Te factureren aantal** in. Het aantal moet lager zijn dan de waarde in het veld **Te verzenden aantal**.  
14. Wanneer de verkooporderregels zijn ingevuld, kiest u de actie **Boeken en verzenden**.

[!INCLUDE [order-ship-invoice](includes/order-ship-invoice.md)]

Het dialoogvenster **Boeken en verzenden bevestigen** geeft de manier aan waarop de klant de documenten wil ontvangen. U kunt de verzendmethode wijzigen door de opzoekknop voor het veld **Document verzenden naar** te kiezen. Zie [Verzendprofielen van documenten instellen](sales-how-setup-document-send-profiles.md) voor meer informatie.

Het gerelateerde artikel en de gerelateerde klantposten worden nu gemaakt in het systeem en de verkooporder is uitvoer als een PDF-document. Als de verkooporder volledig is geboekt, wordt deze verwijderd uit de lijst met verkooporders en vervangen door nieuwe documenten in de lijst met geboekte verkoopfacturen en de lijst met van geboekte verkoopverzendingen.  

## <a name="external-document-number"></a>Externe documentnummer

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-also"></a>Zie ook

[Verkopen factureren](sales-how-invoice-sales.md)  
[Verkopen boeken](ui-post-sales.md)  
[Artikelen verzenden](warehouse-how-ship-items.md)  
[Doorverzendingen maken](sales-how-drop-shipment.md)  
[Verkoop](sales-manage-sales.md)  
[Verkopen instellen](sales-setup-sales.md)  
[De picklijst afdrukken](sales-how-print-picking-list.md)  
[Gedeeltelijke verzendingen verwerken](sales-how-send-partial-shipments.md)  
[Voorraad](inventory-manage-inventory.md)  
[Documenten per e-mail verzenden](ui-how-send-documents-email.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
