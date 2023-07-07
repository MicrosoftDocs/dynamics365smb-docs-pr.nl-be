---
title: Verkoopoffertes maken
description: Lees hoe u een verkoopaanbieding of een offerteaanvraagdocument maakt om uw aanbod aan een klant of prospect vast te leggen om producten onder bepaalde voorwaarden te verkopen.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.search.form: '41, 9300'
ms.date: 07/12/2021
ms.author: edupont
---
# <a name="make-sales-quotes"></a>Verkoopoffertes maken

U maakt een verkoopofferte om uw aanbod aan een klant of prospect vast te leggen om producten tegen bepaalde leverings- en betalingscondities te verkopen. U kunt de verkoopofferte aan de klant verzenden om het aanbod te bevestigen. U kunt het document als een PDF-bijlage via e-mail versturen. U kunt ook de hoofdtekst van de e-mail vooraf laten invullen met een overzicht van de offerte. Zie [Documenten per e-mail verzenden](ui-how-send-documents-email.md) voor meer informatie.

Terwijl u met de klant of prospect onderhandelt, kunt u zo veel als u wenst de verkoopofferte wijzigen en opnieuw zenden. Als de klant de offerte accepteert, zet u de verkoopofferte om in een verkoopfactuur of een verkooporder waarin u de verkoop verwerkt. Zie [Verkopen factureren](sales-how-invoice-sales.md) of [Producten verkopen](sales-how-sell-products.md) voor meer informatie.

In de meeste gevallen stuurt u verkoopoffertes naar potentiële klanten. Vaak hebt u een contactpersoon met wie u onderhandelt. Als zij uw aanbod vervolgens accepteren, maakt u van de verkoopofferte een order en registreert u de prospect als klant in [!INCLUDE [prod_short](includes/prod_short.md)]. In de volgende procedure richten we ons op contacten, maar u kunt ook offertes sturen naar bestaande klanten.  

## <a name="to-create-a-sales-quote"></a>Een verkoopofferte maken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Verkoopoffertes** in en kies vervolgens de gerelateerde koppeling.
2. Geef het contact of de klant op naar wie u de verkoopofferte wilt sturen.

    - Als de verkoopofferte voor een bestaand contact is, geef dan de naam op in het veld **Contactnr.** toevoegen.  

        Als de verkoopofferte voor een bestaande klant is, geeft u de naam op in het veld **Klant**.
    - Als het contact niet is geregistreerd, volgt u deze stappen:

        1. Kies in het veld **Contractnr.** de knop Bewerken :::image type="icon" source="media/assist-edit-icon.png" border="false":::.
        2. Kies in het dialoogvenster over het selecteren van het contact de actie **Nieuw** en vul vervolgens de relevante velden in. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)] Zie voor meer informatie [Contacten maken](marketing-create-contact-companies.md).  
        3. Wanneer u de contactkaart hebt ingevuld, selecteert u het nieuw gemaakte contact in de lijst met contacten en kiest u vervolgens de knop OK om terug te keren naar de verkoopofferte.

        Verschillende velden in de verkoopofferte worden nu ingevuld met gegevens die u hebt opgegeven op de nieuwe contactkaart.

        > [!NOTE]
        > Om de belastingen en prijzen voor een offerte correct te berekenen, moet u de relevante klantsjabloon kiezen in het veld **Klantensjablooncode**. De sjabloon wordt gebruikt om het contact naar een klant te converteren zodra de offerte is geconverteerd naar een verkooporder of factuur.
    -  Als de offerte voor een nieuwe klant is, moet u de klant toevoegen. Zie voor meer informatie [Nieuwe klanten registreren](sales-how-register-new-customers.md).  

3. Vul desgewenst de overige velden op de pagina **Verkoopofferte** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    U kunt nu de verkoopregels invullen voor producten die u verkoopt of voor elke transactie met de klant of prospect die u in een grootboekrekening wilt registreren.  

    Als u terugkerende verkoopregels voor de klant hebt ingesteld, zoals een maandelijkse aanvullingsorder, kunt u deze regels invoegen op de order door de actie **Terugkerende verkoopregels ophalen** te kiezen.  

4. Selecteer op het sneltabblad **Regels** in het veld **Soort** het type product, kosten of transactie die u wilt boeken voor de klant met deze verkoopregel.
5. Voer in het veld **Nr.** een record die u wilt boeken op basis van de waarde in het veld **Soort**.

    Laat het veld **Nr.** leeg in de volgende gevallen:
    - Als de regel voor een opmerking is. Schrijf de opmerking in het veld **Omschrijving**.
    - Als de regel voor een catalogusartikel is. Kies de actie **Catalogusartikelen selecteren**. Zie voor meer informatie [Werken met catalogusartikelen](inventory-how-work-nonstock-items.md).

6. Voer in het veld **Aantal** in hoeveel eenheden van het product, de kosten of de transactie met de regel voor de klant worden geregistreerd.

    > [!NOTE]  
    >  Als het een artikel van de soort **Service** betreft of als het veld **Type** de waarde **Resource** bevat, is de hoeveelheid een tijdseenheid, bijvoorbeeld uren, zoals aangegeven in het veld **Eenheidscode** op de regel. Zie [Artikeleenheden instellen](inventory-how-setup-units-of-measure.md) voor meer informatie

    De waarde in het veld **Regelbedrag** wordt berekend als *Eenheidsprijs* x *Aantal*.  

    De prijs en de regelbedragen worden weergegeven met of zonder btw, afhankelijk van wat u hebt geselecteerd in het veld **Prijzen inclusief btw** op de klantenkaart.  
7. Als u een korting wilt geven, kunt u een percentage invoeren in het veld **Regelkorting %**. De waarde in het veld **Regelbedrag** wordt dienovereenkomstig bijgewerkt.  

    Als u speciale artikelprijzen hebt ingesteld op het sneltabblad **Verkoopprijzen en verkoopregelkortingen** op de klantenkaart of de artikelkaart, worden de prijs en het bedrag op de offerteregel automatisch bijgewerkt als aan de overeengekomen prijscriteria wordt voldaan. Zie voor meer informatie [Afspraken over prijzen, kortingen en betalingen van verkopen vastleggen](sales-how-record-sales-price-discount-payment-agreements.md).  
8. Herhaal stap 4 t/m 7 voor elk product dat u aan het contact wilt aanbieden.

    De totalen onder de regels worden automatisch berekend wanneer u regels maakt of wijzigt.  
9. In het veld **Kortingsbedrag op factuur** voert u een bedrag in dat moet worden afgetrokken van de waarde in het veld **Totaal incl. btw**.

    Als u factuurkortingen voor de klant hebt opgegeven, wordt het opgegeven percentage automatisch ingevoegd in het veld **Factuurkorting %** als aan de voorwaarden wordt voldaan, en het gerelateerde bedrag wordt ingevoegd in het veld **Factuurkortingsbedrag excl. btw** . Zie voor meer informatie [Afspraken over prijzen, kortingen en betalingen van verkopen vastleggen](sales-how-record-sales-price-discount-payment-agreements.md).

    > [!TIP]
    > Als u het veld **Offerte geldig tot datum** automatisch wilt laten invullen met een bepaald aantal dagen na het maken van de offerte, kunt u het veld **Berekening van geldigheid van offerte** op de pagina **Verkopen en Klanten** invullen.

10. Wanneer de verkoopofferteregels zijn ingevuld, kiest u de actie **Verzenden via e-mail**.
11. Vul op de pagina **E-mail verzenden** eventuele overige velden in en controleer de ingesloten verkoopofferte. Zie [Documenten per e-mail verzenden](ui-how-send-documents-email.md) voor meer informatie.
12. Als het contact de offerte accepteert, kiest u de actie **Order maken**.  

    Als uw organisatie de voorkeur geeft aan dat proces, kiest u de actie **Factuur maken**.  
    > [!NOTE]
    > Als u in stap 2 een klant heeft toegevoegd, wordt u gevraagd om de omzetting van de offerte naar een order te bevestigen.  
    >
    > Als u in stap 2 een contact van een potentiële klant heeft toegevoegd, wordt u gevraagd de volgende stappen uit te voeren:
    >
    >  - Converteer het contact of de prospect naar een klant door een van de contactconversiesjablonen te kiezen. Zie voor meer informatie [Een klant, leverancier, werknemer of bankrekening maken van een contact](marketing-create-contact-companies.md#to-create-a-customer-vendor-employee-or-bank-account-from-a-contact).  
    > - Bevestig de conversie van de offerte naar een order.

De conversie verwijdert de verkoopofferte uit de database. Een verkoopfactuur of een verkooporder wordt gemaakt op basis van de informatie in de verkoopofferte, zodat u de verkoop kunt verwerken. Op de verkoopfactuur of verkooporder vermeldt het veld **Offertenr.** het nummer van de verkoopofferte van waaruit het is gemaakt. Zie [Verkopen factureren](sales-how-invoice-sales.md) of [Producten verkopen](sales-how-sell-products.md) voor meer informatie.  

## <a name="external-document-number"></a>Externe documentnummer

[!INCLUDE [ext-doc-no-sales](includes/ext-doc-no-sales.md)]

## <a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/modules/create-sales-documents-dynamics-365-business-central/)

## <a name="see-also"></a>Zie ook

[Verkoop](sales-manage-sales.md)  
[Verkopen instellen](sales-setup-sales.md)  
[Documenten per e-mail verzenden](ui-how-send-documents-email.md)  
[Documenten archiveren](across-how-to-archive-documents.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
