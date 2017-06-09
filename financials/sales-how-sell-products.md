---
title: 'Procedure: Producten verkopen | Microsoft Docs'
description: Hierin wordt beschreven hoe u verkooporders kunt gebruiken.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade
ms.date: 03/09/2017
ms.author: sgroespe
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: a587a9eab63223f7fab94bc4f513d2b6816f0d14
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="how-to-sell-products"></a>Procedure: Producten verkopen
U maakt een verkoopfactuur of een verkooporder om uw overeenkomst met een klant vast te leggen om bepaalde producten tegen bepaalde leverings- en betalingsvoorwaarden te verkopen.

**Opmerking**: u gebruikt verkooporders als uw verkoopproces vereist dat u delen van een orderhoeveelheid kunt verzenden, bijvoorbeeld omdat de volledige hoeveelheid niet in één keer beschikbaar is. Als u artikelen verkoopt door rechtstreeks van uw leverancier bij de klant te leveren, als een doorverzending, moet u ook verkooporders gebruiken. Zie [Procedure: Doorverzendingen maken](sales-how-drop-shipment.md) voor meer informatie. Wat betreft alle andere aspecten werken verkooporders op dezelfde manier als verkoopfacturen. Zie [Procedure: Verkopen factureren](sales-how-invoice-sales.md) voor meer informatie.

U kunt met de klant onderhandelen door eerst een verkoopofferte te maken, die u kunt omzetten in een verkooporder wanneer er een overeenkomst is. Zie [Procedure: Voorstellen maken](sales-how-make-offers.md) voor meer informatie.

Nadat de klant de overeenkomst heeft bevestigd, bijvoorbeeld na een offerteproces, kunt u een orderbevestiging verzenden om uw verplichting vast te leggen dat de producten worden geleverd zoals is overeengekomen.

Als u de producten volledig of gedeeltelijk levert, boekt u de verkooporder als verzonden of als verzonden en gefactureerd om het gerelateerde artikel en de klantposten in uw systeem te maken. Wanneer u de verkooporder boekt, kunt u ook het document als een PDF-bijlage via e-mail versturen. U kunt ook de hoofdtekst van de e-mail vooraf invullen met een overzicht van de orde- en betalingsgegevens, zoals een koppeling naar PayPal. Zie [Procedure: Documenten per e-mail verzenden](ui-how-send-documents-email.md) voor meer informatie.

In bedrijfsomgevingen waar de klant moet betalen voordat producten worden geleverd, zoals in de detailhandel, moet u wachten op de betalingsontvangst voordat u de producten levert. In de meeste gevallen verwerkt u inkomende betalingen enkele weken na levering door de betalingen te vereffenen met de gerelateerde geboekte, niet-betaalde verkoopfacturen. Zie voor meer informatie [Procedure: Betalingen reconciliëren met automatische vereffening](receivables-how-reconcile-payments-auto-application.md).

U kunt een geboekte verkoopfactuur die het resultaat is van een verkooporder gemakkelijk corrigeren of annuleren voordat deze wordt betaald. Dit is handig als u een typfout wilt corrigeren of als de klant om een wijziging in het begin van het orderproces verzoekt. Zie [Procedure: Onbetaalde verkoopfacturen corrigeren of annuleren](sales-how-correct-cancel-sales-invoice.md) voor meer informatie. Als de geboekte verkoopfactuur is betaald, moet u een verkoopcreditnota maken om de verkoop tegen te boeken. Zie [Procedure: Verkoopretouren of annuleringen verwerken](sales-how-process-sales-returns-cancellations.md) voor meer informatie.

Artikelen kunnen zowel voorraadartikelen als services zijn, aangeduid met de typen **Artikel - Voorraad** en **Artikel - Service** op de verkoopregels. Het verkooporderproces is hetzelfde voor beide artikeltypen. Zie [Procedure: Nieuwe artikelen registreren](inventory-how-register-new-items.md) voor meer informatie.

U kunt klantvelden op de verkooporder op twee manieren invullen afhankelijk van de vraag of de klant reeds is geregistreerd. Zie de stappen 2 en 3 in de volgende procedure.

## <a name="to-create-a-sales-order"></a>Een verkooporder maken
1. Kies op de startpagina de actie **Verkooporder**.  
2. Voer in het veld **Klant** de naam in van een bestaande klant.

    Overige velden in het venster **Verkooporder** worden nu ingevuld met de standaardinformatie over de geselecteerde klant. Als de klant niet is geregistreerd, volgt u deze stappen:
3. Voer in het veld **Klant** de naam van de nieuwe klant in.
4. Kies in dialoogvenster voor het registreren van de nieuwe klant de knop **Ja**.
5. Kies in het venster **Selecteer een sjabloon voor een nieuwe klant** een sjabloon waarop u de nieuwe klantenkaart wilt baseren en kies vervolgens de knop **OK**.

    Een nieuwe klantenkaart wordt geopend, die vooraf is ingevuld met de informatie over de geselecteerde klantensjabloon. Het veld **Naam** is vooraf ingevuld met de naam van de nieuwe klant die u op de verkooporder hebt ingevoerd.
6. Ga door met het invullen van de overige velden op de klantenkaart. Zie [Procedure: Nieuwe klanten registreren](sales-how-register-new-customers.md) voor meer informatie.  
7. Wanneer u de klantenkaart hebt ingevuld, kiest u de knop **OK** om terug te keren naar het venster **Verkooporder**.

    Verschillende velden op de verkooporder worden nu ingevuld met gegevens die u hebt opgegeven op de nieuwe klantenkaart.
8. Vul indien nodig de overige velden in het venster **Verkooporder** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

    U kunt nu de verkooporderregels invullen met voorraadartikelen of services die u aan de klant wilt verkopen.

    Als u terugkerende verkoopregels voor de klant hebt ingesteld, zoals een maandelijkse aanvullingsorder, kunt u deze regels invoegen op de order door de actie **Terugkerende verkoopregels ophalen** te kiezen.
9. Voer op het sneltabblad **Regels** in het veld **Artikel** het nummer van een voorraadartikel of een service in.  
10. Geef in het veld **Aantal** op hoeveel artikelen u wilt verkopen.

    **Opmerking**: voor artikelen van de soort Service is de hoeveelheid een tijdseenheid, bijvoorbeeld uren, zoals aangegeven in het veld **Eenheidscode** op de regel.

    Het veld **Regelbedrag** wordt bijgewerkt met de waarde in het veld **Eenheidsprijs**, vermenigvuldigd met de waarde in het veld **Aantal**.

    De prijs en de regelbedragen worden weergegeven met of zonder btw afhankelijk van wat u hebt geselecteerd in het veld **Prijzen inclusief btw** op de klantenkaart.
11. In het veld **Regelkorting %** voert u een percentage in als u de klant een korting op het product wilt verlenen. De waarde in het veld **Regelbedrag** wordt dienovereenkomstig bijgewerkt.

    Als u speciale artikelprijzen hebt ingesteld op het sneltabblad **Verkoopprijzen en verkoopregelkortingen** op de klantenkaart of de artikelkaart, worden de prijs en het bedrag op de offerteregel automatisch bijgewerkt als aan de overeengekomen prijscriteria is voldaan. Zie voor meer informatie [Afspraken over prijzen, kortingen en betalingen van verkopen vastleggen](sales-how-record-sales-price-discount-payment-agreements.md).
12. Als u een opmerking over de offerteregel wilt toevoegen die de klant op de afgedrukte verkoopofferte kan zien, schrijft u een tekst in het veld **Omschrijving** op een lege regel.  
13. Herhaal stap 10 t/m 13 voor elk artikel dat u aan de klant wilt aanbieden.

    De totalen onder de regels worden automatisch berekend wanneer u regels maakt of wijzigt.
6. In een nieuwe klantenkaart wordt de informatie uit de geselecteerde klantensjabloon getoond. Vul de overige velden in. Zie [Procedure: Nieuwe klanten registreren](sales-how-register-new-customers.md) voor meer informatie.  
7. Wanneer u de klantenkaart hebt ingevuld, kiest u de knop **OK** om terug te keren naar het venster **Verkooporder**.

   Verschillende velden op de verkooporder worden nu ingevuld met gegevens die u hebt opgegeven op de nieuwe klantenkaart.  
8. Vul indien nodig de overige velden in het venster **Verkooporder** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

   U kunt nu verkooporderregels invullen voor producten die u aan de klant verkoopt of voor elke transactie met de klant die u in een grootboekrekening wilt registreren.   

   Als u terugkerende verkoopregels voor de klant hebt ingesteld, zoals een maandelijkse aanvullingsorder, kunt u deze regels invoegen op de order door de actie **Terugkerende verkoopregels ophalen** te kiezen.  
9. Selecteer op het sneltabblad **Regels** in het veld **Soort** het type product, kosten of transactie die u wilt boeken voor de klant met deze verkoopregel.
10. Voer in het veld **Nr.** een record die u wilt boeken op basis van de waarde in het veld **Soort**.

    Laat het veld **Nr.** leeg in de volgende gevallen: - Als de regel voor een opmerking is. Schrijf de opmerking in het veld **Omschrijving**.
    - Als de regel voor een niet-voorraadartikel is. Kies de actie **Niet-voorraadartikelen selecteren**. Zie voor meer informatie [Procedure: Werken met niet-voorraadartikelen](inventory-how-work-nonstock-items.md).

11. Voer in het veld **Aantal** hoeveel eenheden van het artikel, de kosten of de transactie met de regel voor de klant worden geregistreerd.  

    **Opmerking:** Als het een artikel van de soort **Artikel - Service** of **Resource** betreft, is de hoeveelheid een tijdseenheid, bijvoorbeeld uren, zoals aangegeven in het veld **Eenheidscode** op de regel.  

    De waarde in het veld **Regelbedrag** wordt berekend als *Eenheidsprijs* x *Aantal*.  

    De prijs en de regelbedragen worden weergegeven met of zonder btw, afhankelijk van wat u hebt geselecteerd in het veld **Prijzen inclusief btw** op de klantenkaart.  
12. Als u een korting wilt geven, kunt u een percentage invoeren in het veld **Regelkorting %**. De waarde in het veld **Regelbedrag** wordt dienovereenkomstig bijgewerkt.  

    Als u speciale artikelprijzen hebt ingesteld op het sneltabblad **Verkoopprijzen en verkoopregelkortingen** op de klantenkaart of de artikelkaart, worden de prijs en het bedrag op de offerteregel automatisch bijgewerkt als aan de overeengekomen prijscriteria wordt voldaan. Zie voor meer informatie [Afspraken over prijzen, kortingen en betalingen van verkopen vastleggen](sales-how-record-sales-price-discount-payment-agreements.md).  
13. Herhaal stap 9 t/m 12 voor elk product of kosteneenheid dat/die u aan de klant wilt verkopen.  

    De totalen onder de regels worden automatisch berekend wanneer u regels maakt of wijzigt.  
14. In het veld **Kortingsbedrag op factuur** voert u een bedrag in dat moet worden afgetrokken van de waarde in het veld **Totaal incl. btw**.

    Als u factuurkortingen voor de klant hebt opgegeven, wordt het opgegeven percentage automatisch ingevoegd in het veld **Factuurkorting %**als aan de voorwaarden wordt voldaan, en het gerelateerde bedrag wordt ingevoegd in het veld **Factuurkortingsbedrag excl. btw** . Zie voor meer informatie [Afspraken over prijzen, kortingen en betalingen van verkopen vastleggen](sales-how-record-sales-price-discount-payment-agreements.md).
15. Als u slechts een deel van het orderaantal wilt verzenden, voert u dat aantal in het veld **Te verzenden aantal** in. De waarde wordt gekopieerd naar **Te factureren aantal**.
16. Als u slechts een deel van het verzonden aantal wilt factureren, voert u dat aantal in het veld **Te factureren aantal** in. Het aantal moet lager zijn dan de waarde in het veld **Te verzenden aantal**.   
17. Wanneer de verkooporderregels zijn ingevuld, kiest u de actie **Boeken en verzenden**.

Het dialoogvenster **Boeken en verzenden bevestigen** geeft de manier aan waarop de klant de documenten wil ontvangen. U kunt de verzendmethode wijzigen door de opzoekknop voor het veld **Document verzenden naar** te kiezen. Zie [Procedure: Verzendprofielen voor documenten instellen](sales-how-setup-document-send-profiles.md) voor meer informatie.

Het gerelateerde artikel en de gerelateerde klantposten worden nu gemaakt in het systeem en de verkooporder is uitvoer als een PDF-document. Als de verkooporder volledig is geboekt, wordt deze verwijderd uit de lijst met verkooporders en vervangen door nieuwe documenten in de lijst met geboekte verkoopfacturen en de lijst met van geboekte verkoopverzendingen.

## <a name="see-also"></a>Zie ook
[Verkoop](sales-manage-sales.md)  
[Verkopen instellen](sales-setup-sales.md)  
[Voorraad](inventory-manage-inventory.md)  
[Procedure: Documenten per e-mail verzenden](ui-how-send-documents-email.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
