---
title: Betalingen exporteren aan een elektronisch betalingsbestand| Microsoft Docs
description: Als u leveranciersbetalingen wilt doen, schakelt u een conversieservice voor bankgegevens in, exporteert u een bankbestand en uploadt u het bestand naar uw elektronische bank om het geld over te maken.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bank file export, re-export, bank transfer, AMC, bank data conversion service, funds transfer
ms.date: 04/26/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: db28ad9a4adb45514b1d1287d269d8daefe64865
ms.openlocfilehash: 68a35c3bbedd0d0f09a9e43269260e98dfa02a59
ms.contentlocale: nl-be
ms.lasthandoff: 04/26/2018

---
# <a name="export-payments-to-a-bank-file"></a>Betalingen naar een bankbestand exporteren
Wanneer u klaar bent om betalingen aan uw leveranciers of vergoedingen aan uw werknemers uit te voeren, kunt u een bestand met de betalingsgegevens op de dagboekregels exporteren vanuit het venster **Betalingsdagboek**. Vervolgens kunt u het bestand uploaden naar uw bank voor verwerking van de betreffende overboekingen.

In de algemene versie van [!INCLUDE[d365fin](includes/d365fin_md.md)] wordt een algemene provider van services ingesteld en verbonden die bankgegevens converteert naar een bestandsindeling die uw bank vereist. In Noordamerikaanse versies kan dezelfde service worden gebruikt om betalingbestanden te verzenden als Elektronische overboeking (EFT), maar met een licht afwijkend proces. Zie stap 6 in het gedeelte "Betalingen naar een bankbestand exporteren".    

> [!NOTE]  
>   Voordat u betalingsbestanden vanuit het betalingsdagboek kunt exporteren, moet u de elektronische indeling voor de betreffende bankrekening opgeven en moet u de conversieservice voor bankgegevens inschakelen. Zie voor meer informatie [Bankrekeningen instellen](bank-how-setup-bank-accounts.md) en [Conversieservice voor bankgegevens instellen](bank-how-setup-bank-data-conversion-service.md). Bovendien moet u het selectievakje **Exporteren betaling toestaan** in het venster **Fin. dagboekbatches** inschakelen. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.  

U gebruikt het venster **Krediettransferregisters** om de betalingsbestanden weer te geven die vanuit het betalingsdagboek zijn geëxporteerd. Vanuit dit venster kunt u ook betalingsbestanden opnieuw exporteren, in het geval van technische fouten of bestandswijzigingen. Let er echter op dat geëxporteerde EFT-bestanden niet in dit venster worden weergegeven en niet opnieuw kunnen worden geëxporteerd.  

## <a name="to-export-payments-to-a-bank-file"></a>Betalingen naar een bankbestand exporteren
Hierna wordt beschreven hoe u een leverancier per cheque betaalt. De stappen zijn vergelijkbaar met het terugbetalen van een klant per cheque.

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Betalingsdagboeken** in en klik vervolgens op de gerelateerde koppeling.
2. Vul de betalingsdagboekregels in. Zie voor meer informatie [Betalingen en terugbetalingen vastleggen](payables-how-post-payments-refunds.md).

> [!NOTE]  
>   Als u EFT gebruikt, moet u **Elektronische betaling** of **Elektronische betaling-IAT** in het veld **Betalingssoort** selecteren. Andere services voor bestandsexport en de verschillende indelingen vereisen andere waarden in de vensters **Bankrekeningkaart** en **Bankrekening leverancier**. U wordt over verkeerde of ontbrekende instellingswaarden geïnformeerd als u het bestand probeert te exporteren.

3. Wanneer u alle betalingsdagboekregels hebt voltooid, kiest u de actie **Exporteren**.
4. Vul in het venster **Elektronische betalingen exporteren** de vereiste waarden in.

    Eventuele foutmeldingen worden weergegeven in het feitenblok **Fouten betalingsbestand**, waar u ook een foutbericht kunt kiezen om gedetailleerde gegevens te bekijken. U moet alle fouten oplossen voordat het betalingsbestand kan worden geëxporteerd.

    > [!TIP]  
    >   Wanneer u de functie voor conversie van bankgegevens gebruikt, wordt een algemeen foutbericht weergegeven met de melding dat het bankrekeningnummer niet de lengte heeft die uw bank vereist. Als u de fout wilt oplossen, moet u de waarde verwijderen uit het veld **IBAN** in het venster **Bankrekeningkaart** en vervolgens in het veld **Bankrekeningnr.** een bankrekeningnummer invoeren in de indeling die uw bank vereist.

5. Geef in het venster **Opslaan als** de locatie op waar het bestand naartoe wordt geëxporteerd en kies vervolgens **Opslaan**.

    > [!NOTE]  
    >   Als u EFT gebruikt, sla dan het resulterende remiseformulier voor de leverancier op als Word-document of geef aan dat het rechtstreeks naar de leverancier moet worden gezonden. De betalingen worden nu toegevoegd aan het venster **EFT-bestand genereren**, van waaruit u meerdere betaalopdrachten kunt genereren om de transmissiekosten te drukken. Zie de volgende stappen voor meer informatie.
6. Kies in het venster **Betalingsdagboek** de actie **EFT-bestand genereren**.

    In het venster **EFT-bestand genereren** worden op het sneltabblad **Regels** alle betalingen vermeld die voor EFT zijn geconfigureerd die u vanuit het betalingsdagboek voor een bepaalde rekening hebt geëxporteerd maar die nog niet zijn gegenereerd.
7. Kies de actie **EFT-bestand genereren** om één bestand voor alle EFT-betalingen te exporteren.
8. Geef in het venster **Opslaan als** de locatie op waar het bestand naartoe wordt geëxporteerd en kies vervolgens **Opslaan**.

Het bankbetalingsbestand wordt geëxporteerd naar de locatie die u opgeeft, en u kunt doorgaan met uploaden naar uw elektronische bankrekening en de werkelijke betalingen doen. Vervolgens kunt u de geëxporteerde betalingsdagboekregels boeken.

## <a name="to-plan-when-to-post-exported-payments"></a>Plannen wanneer geëxporteerde betalingen worden geboekt
Als u geen betalingsdagboekregel voor een geëxporteerde betaling wilt boeken, bijvoorbeeld omdat u op bevestiging wacht dat de transactie door de bank is verwerkt, kunt u eenvoudig de dagboekregel verwijderen. Wanneer u later een betalingsdagboekregel maakt om het restbedrag op de factuur te betalen, bevat het veld **Tot. geëxporteerd bedrag** hoeveel van het betalingsbedrag al is geëxporteerd. U kunt ook gedetailleerde gegevens vinden over het geëxporteerde totaal door de knop **Krediettransferregisterposten** te kiezen om details over geëxporteerde betalingsbestanden te bekijken.

Als u een proces volgt waarbij u geen betalingen boekt totdat u bevestiging hebt dat ze zijn verwerkt in de bank, kunt u dit op twee manieren bepalen.

* U kunt in een betalingsdagboek met voorgestelde betalingsregels sorteren op de kolom **Naar betalingsbestand geëxporteerd** of **Tot. geëxporteerd bedrag** en vervolgens betalingsvoorstellen verwijderen voor openstaande facturen waarvoor al betalingen zijn verricht en waarvoor u geen betalingen meer wilt verrichten.
* In het venster **Leveranciersbetalingen voorstellen**, waar u ook opgeeft welke betalingen in het betalingsdagboek worden ingevoegd, kunt u het selectievakje **Geëxporteerde betalingen overslaan** inschakelen als u geen dagboekregels wilt invoegen voor betalingen die al zijn geëxporteerd.

Als u informatie over geëxporteerde gegevens wilt bekijken, kiest u de actie **Historie betalingsexport**.

## <a name="to-re-export-payments-to-a-bank-file"></a>Betalingen naar een bankbestand opnieuw exporteren
U kunt betalingsbestanden opnieuw exporteren vanuit het venster **Krediettransferregisters**. Voordat u betalingsdagboekregels verwijdert of boekt, kunt u het betalingsbestand ook opnieuw exporteren vanuit het venster **Betalingsdagboek** door het nogmaals te importeren. Als u betalingsdagboekregels hebt verwijderd of geboekt nadat u deze hebt geëxporteerd, kunt u hetzelfde betalingsbestand opnieuw exporteren vanuit het venster **Krediettransferregisters**. Selecteer de regel voor de batch kredietoverboekingen die u opnieuw wilt exporteren, en gebruik vervolgens de actie **Betalingen opnieuw exporteren naar bestand**.

> [!NOTE]  
>   Geëxporteerde EFT-bestanden worden niet in het venster **Krediettransferregisters** weergegeven en kunnen niet opnieuw worden geëxporteerd.

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Krediettransferregisters** in en klik vervolgens op de gerelateerde koppeling.
2. Selecteer een betalingexport die u opnieuw wilt exporteren en kies de actie **Betalingen opnieuw exporteren naar bestand**.

## <a name="see-also"></a>Zie ook
[Betalingen uitvoeren](payables-make-payments.md)  
[Schulden](payables-manage-payables.md)  
[Inkoop instellen](purchasing-setup-purchasing.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

