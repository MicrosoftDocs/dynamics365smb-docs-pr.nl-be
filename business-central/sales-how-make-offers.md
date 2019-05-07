---
title: Een verkoopaanbod voor een klant maken | Microsoft Docs
description: Beschrijft hoe u een verkoopaanbieding of een offerteaanvraagdocument maakt om uw aanbod aan een klant vast te leggen om producten onder bepaalde voorwaarden te verkopen.
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: rfq
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: 6083e5ff57ebfb57a31d294e5c565b5bc6a3f8c6
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "930464"
---
# <a name="make-sales-quotes"></a>Verkoopoffertes maken
U maakt een verkoopofferte aan om uw aanbod aan een klant vast te leggen om producten tegen bepaalde leverings- en betalingscondities te verkopen. U kunt de verkoopofferte aan de klant verzenden om het aanbod te bevestigen. U kunt het document als een PDF-bijlage via e-mail versturen. U kunt ook de hoofdtekst van de e-mail vooraf laten invullen met een overzicht van de offerte. Zie [Documenten per e-mail verzenden](ui-how-send-documents-email.md) voor meer informatie.

Terwijl u met de klant onderhandelt, kunt u zo veel als u wenst de verkoopofferte wijzigen en opnieuw zenden. Als de klant de offerte accepteert, zet u de verkoopofferte om in een verkoopfactuur of een verkooporder waarin u de verkoop verwerkt. Zie [Verkopen factureren](sales-how-invoice-sales.md) of [Producten verkopen](sales-how-sell-products.md) voor meer informatie.

U kunt klantvelden op de verkoopofferte op twee manieren invullen afhankelijk van de vraag of de klant reeds is geregistreerd. Zie de stappen 2 en 3 in de volgende procedure.

## <a name="to-create-a-sales-quote"></a>Een verkoopofferte maken
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Verkoopoffertes** in en kies vervolgens de gerelateerde koppeling.
2. Voer in het veld **Klant** de naam in van een bestaande klant.

   Overige velden op de pagina **Verkoopofferte** bevatten standaardinformatie over de geselecteerde klant. Als de klant niet is geregistreerd, volgt u deze stappen:
3. Voer in het veld **Klant** de naam van de nieuwe klant in.
4. Kies in dialoogvenster voor het registreren van de nieuwe klant de knop **Ja**.
5. Kies op de pagina **Selecteer een sjabloon voor een nieuwe klant** een sjabloon waarop u de nieuwe klantenkaart wilt baseren en kies vervolgens de knop **OK**.
6. In een nieuwe klantenkaart wordt de informatie uit de geselecteerde klantensjabloon getoond. Vul de overige velden in. Zie voor meer informatie [Nieuwe klanten registreren](sales-how-register-new-customers.md).  
7. Wanneer u de klantenkaart hebt voltooid, kiest u de knop **OK** om terug te keren naar de pagina **Verkoopofferte**.

   Verschillende velden op de verkoopofferte worden nu ingevuld met gegevens die u hebt opgegeven op de nieuwe klantenkaart.  
8. Vul desgewenst de overige velden op de pagina **Verkoopofferte** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    U kunt nu verkooporderregels invullen voor producten die u aan de klant verkoopt of voor elke transactie met de klant die u in een grootboekrekening wilt registreren.   

    Als u terugkerende verkoopregels voor de klant hebt ingesteld, zoals een maandelijkse aanvullingsorder, kunt u deze regels invoegen op de order door de actie **Terugkerende verkoopregels ophalen** te kiezen.  

9. Selecteer op het sneltabblad **Regels** in het veld **Soort** het type product, kosten of transactie die u wilt boeken voor de klant met deze verkoopregel.
10. Voer in het veld **Nr.** een record die u wilt boeken op basis van de waarde in het veld **Soort**.

    Laat het veld **Nr.** leeg in de volgende gevallen:
    - Als de regel voor een opmerking is. Schrijf de opmerking in het veld **Omschrijving**.
    - Als de regel voor een catalogusartikel is. Kies de actie **Catalogusartikelen selecteren**. Zie voor meer informatie [Werken met catalogusartikelen](inventory-how-work-nonstock-items.md).

11. Voer in het veld **Aantal** in hoeveel eenheden van het product, de kosten of de transactie met de regel voor de klant worden geregistreerd.

    > [!NOTE]  
    >   Als het een artikel van de soort **Artikel - Service** of **Resource** betreft, is de hoeveelheid een tijdseenheid, bijvoorbeeld uren, zoals aangegeven in het veld **Eenheidscode** op de regel.  

    De waarde in het veld **Regelbedrag** wordt berekend als *Eenheidsprijs* x *Aantal*.  

    De prijs en de regelbedragen worden weergegeven met of zonder btw, afhankelijk van wat u hebt geselecteerd in het veld **Prijzen inclusief btw** op de klantenkaart.  
12. Als u een korting wilt geven, kunt u een percentage invoeren in het veld **Regelkorting %**. De waarde in het veld **Regelbedrag** wordt dienovereenkomstig bijgewerkt.  

    Als u speciale artikelprijzen hebt ingesteld op het sneltabblad **Verkoopprijzen en verkoopregelkortingen** op de klantenkaart of de artikelkaart, worden de prijs en het bedrag op de offerteregel automatisch bijgewerkt als aan de overeengekomen prijscriteria wordt voldaan. Zie voor meer informatie [Afspraken over prijzen, kortingen en betalingen van verkopen vastleggen](sales-how-record-sales-price-discount-payment-agreements.md).  
13. Herhaal stap 9 t/m 12 voor elk product dat u aan de klant wilt aanbieden.

    De totalen onder de regels worden automatisch berekend wanneer u regels maakt of wijzigt.  
14. In het veld **Kortingsbedrag op factuur** voert u een bedrag in dat moet worden afgetrokken van de waarde in het veld **Totaal incl. btw**.

    Als u factuurkortingen voor de klant hebt opgegeven, wordt het opgegeven percentage automatisch ingevoegd in het veld **Factuurkorting %** als aan de voorwaarden wordt voldaan, en het gerelateerde bedrag wordt ingevoegd in het veld **Factuurkortingsbedrag excl. btw** . Zie voor meer informatie [Afspraken over prijzen, kortingen en betalingen van verkopen vastleggen](sales-how-record-sales-price-discount-payment-agreements.md).

    > [!TIP]
    > Als u het veld **Offerte geldig tot datum** automatisch wilt laten invullen met een bepaald aantal dagen na het maken van de offerte, kunt u het veld **Berekening van geldigheid van offerte** op de pagina **Verkopen en Klanten** invullen. 

15. Wanneer de verkoopofferteregels zijn ingevuld, kiest u de actie **Verzenden via e-mail**.
16. Vul op de pagina **E-mail verzenden** eventuele overige velden in en controleer de ingesloten verkoopofferte. Zie [Documenten per e-mail verzenden](ui-how-send-documents-email.md) voor meer informatie.
17. Als de klant de offerte accepteert, kiest u de actie **Factuur maken** of de actie **Order maken**.

De verkoopofferte wordt verwijderd uit de database. Een verkoopfactuur of een verkooporder wordt gemaakt op basis van de informatie in de verkoopofferte waarin u de verkoop kunt verwerken. Op de verkoopfactuur of verkooporder vermeldt het veld **Offertenr.** het nummer van de verkoopofferte van waaruit het is gemaakt. Zie [Verkopen factureren](sales-how-invoice-sales.md) of [Producten verkopen](sales-how-sell-products.md) voor meer informatie.

## <a name="see-also"></a>Zie ook
[Verkoop](sales-manage-sales.md)  
[Verkopen instellen](sales-setup-sales.md)  
[Documenten per e-mail verzenden](ui-how-send-documents-email.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
