---
title: Betalingen doen met de extensie AMC Banking (US) of SEPA-kredietoverdracht (EU)
description: Verwerk betalingen aan uw leveranciers door samen met de betalingsgegevens van de dagboekregels een bestand te exporteren.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '256, 1205, 1206, 1209, 10810, 10811'
ms.date: 07/06/2021
ms.author: bholtorf
---
# <a name="make-payments-with-the-amc-banking-365-fundamentals-extension-or-sepa-credit-transfer" />Betalingen doen met de extensie AMC Banking 365 Fundamentals of SEPA-kredietoverdracht

U kunt op de pagina **Betalingsdagboek** betalingen naar uw leveranciers verwerken door samen met de betalingsgegevens van de dagboekregels een bestand te exporteren. Vervolgens kunt u het bestand uploaden naar uw elektronische banksite waar de gerelateerde overboekingen worden verwerkt. [!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt de indeling voor SEPA-kredietoverboekingen, maar in uw land of regio kunnen andere indelingen voor elektronische betalingen beschikbaar zijn.

> [!NOTE]
> In de algemene versie van [!INCLUDE[prod_short](includes/prod_short.md)] wordt een algemene provider van services ingesteld en verbonden die bankgegevens converteert naar een bestandsindeling die uw bank vereist. In Noord-Amerikaanse versies kan dezelfde service worden gebruikt om betalingsbestanden te verzenden als elektronische overboeking (EFT), bijvoorbeeld het veelgebruikte ACH-netwerk (Automated Clearing House), maar met een iets ander proces. Zie stap 6 in [Betalingen naar een bankbestand exporteren](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).  

 Voor het mogelijk maken van SEPA-kredietoverboekingen moet u eerst een bankrekening, leverancier, en dagboekbatch instellen waarop het betalingsdagboek is gebaseerd. Bereid vervolgens betalingen aan leveranciers voor door de pagina **Betalingsdagboek** automatisch te vullen met verschuldigde betalingen met een opgegeven boekingsdatum.  

> [!NOTE]  
> Wanneer u hebt gecontroleerd dat de betalingen zijn verwerkt door de bank, kunt u doorgaan met het boeken van de betalingsdagboekregels.  

## <a name="setting-up-the-amc-banking-365-fundamentals-extension" />De extensie AMC Banking 365 Fundamentals instellen

Activeer de extensie AMC Banking 365 Fundamentals om eventuele bankafschriften te laten converteren in een indeling die u kunt importeren of om de geëxporteerde betalingsbestanden te laten converteren naar de indeling die uw bank vereist. Zie voor meer informatie [De extensie AMC Banking 365 Fundamentals gebruiken](ui-extensions-amc-banking.md).

## <a name="setting-up-sepa-credit-transfer" />SEPA-krediettransfer instellen

Vanuit de pagina **Betalingsdagboek** kunt u betalingen exporteren naar een bestand om deze te uploaden naar uw elektronische bank voor verwerking van de gekoppelde geldtransfers. [!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt de indeling voor SEPA-kredietoverboekingen, maar in uw land of regio kunnen andere indelingen voor elektronische betalingen beschikbaar zijn.  

Als u de export van bankbestandsindelingen die niet standaard worden ondersteund in [!INCLUDE[prod_short](includes/prod_short.md)] mogelijk wilt maken, kunt u een gegevensuitwisselingsdefinitie instellen met behulp van het kader voor gegevensuitwisseling. Zie [Definities voor gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md) voor meer informatie.  

Voordat u elektronische betaling kunt verwerken door betalingsbestanden te exporteren in de SEPA-overmakingsindeling, moet u de volgende instellingenstappen uitvoeren:  

* De betreffende bankrekening instellen om de indeling voor SEPA-kredietoverboekingen te verwerken  
* Leverancierskaarten instellen om betalingen te verwerken door bestanden te exporteren in de indeling voor SEPA-kredietoverboekingen  
* De gerelateerde dagboekbatch instellen om betalingexports via de pagina **Betalingsdagboek** in te schakelen  
* De definitie van gegevensuitwisseling voor een of meer betalingstypen verbinden met de relevante betalingsmethode(n)  

> [!TIP]
> Dit artikel is van toepassing op de generieke versie van [!INCLUDE [prod_short](includes/prod_short.md)]. In uw land of regio zijn mogelijk extra verplichte velden toegevoegd aan de verschillende pagina's. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="to-set-up-a-bank-account-for-sepa-credit-transfer" />Een bankrekening instellen voor SEPA-kredietoverboekingen

1. Voer in het tekstvak **Zoeken** de tekst **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.  
2. Open de kaart van de bankrekening waaruit u betalingsbestanden gaat exporteren in de SEPA-overmakingsindeling.  
3. Kies op het sneltabblad **Transfer** in het veld **Exportindeling betaling** de optie **SEPACT**.  
4. Kies op het tabblad **Algemeen** in het veld **Berichtnummers krediettransfer** een nummerreeks waaruit nummers worden toegewezen aan SEPA-overmakingsposten.  
5. Zorg dat het veld **IBAN** is ingevuld.  

    > [!NOTE]  
    > Het veld **Valutacode** moet worden ingesteld op **EUR**, omdat SEPA-kredietoverboekingen alleen kunnen worden gemaakt in de valuta EURO.  

### <a name="to-set-up-a-vendor-card-for-sepa-credit-transfer" />Een leverancierskaart instellen voor SEPA-kredietoverboekingen

1. Geef in het vak **Zoeken** **Leveranciers** op en kies vervolgens de gerelateerde koppeling.  
2. Open de kaart van de leverancier die u elektronisch gaat betalen door betalingsbestanden te exporteren in de SEPA-overmakingsindeling.  
3. Kies op het sneltabblad **Betaling** in het veld **Betalingswijze** de optie **BANK**.  
4. In het veld **Bankrekeningcode van voorkeur** kiest u de bank waarnaar het geld wordt overgemaakt wanneer het door uw elektronische bank wordt verwerkt.  

    Als u voor deze leverancier nog geen bank heeft opgezet, kunt u dat nu doen. Zie voor meer informatie [Bankrekeningen van leveranciers instellen voor het exporteren van bankbestanden](bank-how-setup-bank-accounts.md#to-set-up-vendor-bank-accounts-for-export-of-bank-files). De waarde in het veld **Bankrekeningcode van voorkeur** wordt gekopieerd naar het veld **Bankrekening ontvanger** op de pagina **Betalingsdagboek**.  

### <a name="to-set-the-payment-journal-up-to-export-payment-files" />Het betalingsdagboek instellen om betalingsbestanden te exporteren

1. Voer in het tekstvak **Zoeken** **Betalingsdagboeken** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de vervolgkeuzeknop in het veld **Batchnaam**.  
3. Kies op de pagina **Algemene journaalbatches** de actie **Lijst bewerken**.  
4. Op de regel voor het betalingsdagboek dat u wilt gebruiken om betalingen te exporteren, schakelt u het selectievakje **Exporteren betaling toestaan** in.  

### <a name="to-connect-the-data-exchange-definition-for-one-or-more-payment-types-with-the-relevant-payment-method-or-methods" />De definitie van gegevensuitwisseling voor een of meer betalingstypen verbinden met de relevante betalingsmethode(n)

1. Voer in het tekstvak **Zoeken** de tekst **Betalingswijzen** in en kies vervolgens de gerelateerde koppeling.  
2. Op de pagina **Betalingsmethoden** selecteert u de betalingswijze die wordt gebruikt om betalingen te exporteren en vervolgens kiest u het veld **Regeldefinitie betalingsexport**.  
3. Selecteer op de pagina **Regeldefinities betalingsexport** de code die u hebt opgegeven in het veld **Code** op het sneltabblad **Regeldefinities** in stap 4 van de sectie 'De opmaak van regels en kolommen in het bestand beschrijven' van [Definities voor gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md).  

## <a name="preparing-the-payment-journal" />Het betalingsdagboek voorbereiden

Vul het betalingsdagboek met regels voor verschuldigde betalingen aan leveranciers, met de mogelijkheid boekingsdatums in te voegen op basis van de vervaldatum van de verwante inkoopdocumenten. Zie [Betalingsverplichtingen beheren](payables-manage-payables.md) voor meer informatie.

## <a name="exporting-payments-to-a-bank-file" />Betalingen naar een bankbestand exporteren

Wanneer u klaar bent om betalingen aan uw leveranciers of vergoedingen aan uw werknemers uit te voeren, kunt u een bestand met de betalingsgegevens op de dagboekregels exporteren vanuit de pagina **Betalingsdagboek**. Vervolgens kunt u het bestand uploaden naar uw bank voor verwerking van de betreffende overboekingen.

De extensie AMC Banking 365 Fundamentals is beschikbaar in de algemene versie van [!INCLUDE[prod_short](includes/prod_short.md)]. In Noord-Amerikaanse versies kan dezelfde uitbreiding worden gebruikt om betalingsbestanden als EFT's (elektronische overboekingen) worden gebruikt, zij het met een iets ander proces. Zie stap 6 in [Betalingen naar een bankbestand exporteren](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).

> [!NOTE]  
> Voordat u betalingsbestanden uit het betalingenjournaal kunt exporteren, moet u de elektronische indeling voor de desbetreffende bankrekening opgeven en moet u de extensie AMC Banking 365 Fundamentals inschakelen. Zie [Bankrekeningen instellen](bank-how-setup-bank-accounts.md) en [De extensie AMC Banking 365 Fundamentals gebruiken](ui-extensions-amc-banking.md) voor meer informatie. Bovendien moet u het selectievakje **Exporteren betaling toestaan** op de pagina **Fin. dagboekbatches** inschakelen. Zie [Werken met diversendagboeken](ui-work-general-journals.md) voor meer informatie.  

U gebruikt de pagina **Krediettransferregisters** om de betalingsbestanden weer te geven die vanuit het betalingsdagboek zijn geëxporteerd. Vanuit deze pagina kunt u ook betalingsbestanden opnieuw exporteren, in het geval van technische fouten of bestandswijzigingen. Let er echter op dat geëxporteerde EFT-bestanden niet op deze pagina worden weergegeven en niet opnieuw kunnen worden geëxporteerd.  

### <a name="to-export-payments-to-a-bank-file" />Betalingen naar een bankbestand exporteren

Hierna wordt beschreven hoe u een leverancier per cheque betaalt. De stappen zijn vergelijkbaar met het terugbetalen van een klant per cheque.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Betalingsdagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Vul de betalingsdagboekregels in. Zie voor meer informatie [Betalingen en terugbetalingen vastleggen](payables-how-post-payments-refunds.md).

    > [!NOTE]
    > Als u EFT gebruikt, moet u **Elektronische betaling** of **Elektronische betaling-IAT** in het veld **Betalingssoort** selecteren. Andere services voor bestandsexport en de verschillende indelingen vereisen andere waarden op de pagina's **Bankrekeningkaart** en **Bankrekeningkaart leverancier**. U wordt over verkeerde of ontbrekende instellingswaarden geïnformeerd als u het bestand probeert te exporteren.
    >
    > De EFT-functie kan alleen worden gebruikt voor bankrekeningen in de lokale valuta. Het kan niet worden gebruikt met een vreemde valuta, aangegeven door een waarde in het veld **Valutacode**. (Lege veldwaarde betekent lokale valuta.)

3. Wanneer u alle betalingsdagboekregels hebt voltooid, kiest u de actie **Exporteren**.
4. Vul op de pagina **Elektronische betalingen exporteren** de vereiste waarden in.

    Eventuele foutmeldingen worden weergegeven in het feitenblok **Fouten betalingsbestand**, waar u ook een foutbericht kunt kiezen om gedetailleerde gegevens te bekijken. U moet alle fouten oplossen voordat het betalingsbestand kan worden geëxporteerd.

    > [!TIP]  
    > Wanneer u de extensie AMC Banking 365 Fundamentals gebruikt, wordt in een veel voorkomend foutbericht gemeld dat het bankrekeningnummer niet de juiste lengte voor uw bank heeft. Als u de fout wilt voorkomen of oplossen, moet u de waarde verwijderen uit het veld **IBAN** op de pagina **Bankrekeningkaart** en vervolgens in het veld **Bankrekeningnr.** een bankrekeningnummer invoeren in de indeling die uw bank vereist.

5. Geef op de pagina **Opslaan als** de locatie op waar het bestand naartoe wordt geëxporteerd en kies vervolgens **Opslaan**.

    > [!NOTE]  
    > Als u EFT gebruikt, sla dan het resulterende remiseformulier voor de leverancier op als Word-document of geef aan dat het rechtstreeks naar de leverancier moet worden gezonden. De betalingen worden nu toegevoegd aan de pagina **EFT-bestand genereren**, van waaruit u meerdere betaalopdrachten kunt genereren om de transmissiekosten te drukken. Zie de volgende stappen voor meer informatie.
6. Kies op de pagina **Betalingsdagboek** de actie **EFT-bestand genereren**.

    Op de pagina **EFT-bestand genereren** worden op het sneltabblad **Regels** alle betalingen vermeld die voor EFT zijn geconfigureerd die u vanuit het betalingsdagboek voor een bepaalde rekening hebt geëxporteerd maar die nog niet zijn gegenereerd.
7. Kies de actie **EFT-bestand genereren** om één bestand voor alle EFT-betalingen te exporteren.
8. Geef op de pagina **Opslaan als** de locatie op waar het bestand naartoe wordt geëxporteerd en kies vervolgens **Opslaan**.

Het bankbetalingsbestand wordt geëxporteerd naar de locatie die u opgeeft, en u kunt doorgaan met uploaden naar uw elektronische bankrekening en de werkelijke betalingen doen. Vervolgens kunt u de geëxporteerde betalingsdagboekregels boeken.

### <a name="to-plan-when-to-post-exported-payments" />Plannen wanneer geëxporteerde betalingen worden geboekt

Als u geen betalingsdagboekregel voor een geëxporteerde betaling wilt boeken, bijvoorbeeld omdat u op bevestiging wacht dat de transactie door de bank is verwerkt, kunt u eenvoudig de dagboekregel verwijderen. Wanneer u later een betalingsdagboekregel maakt om het restbedrag op de factuur te betalen, bevat het veld **Tot. geëxporteerd bedrag** hoeveel van het betalingsbedrag al is geëxporteerd. U kunt ook gedetailleerde gegevens vinden over het geëxporteerde totaal door de knop **Krediettransferregisterposten** te kiezen om details over geëxporteerde betalingsbestanden te bekijken.

Als u een proces volgt waarbij u geen betalingen boekt totdat u bevestiging hebt dat ze zijn verwerkt in de bank, kunt u dit op twee manieren bepalen.

* U kunt in een betalingsdagboek met voorgestelde betalingsregels sorteren op de kolom **Naar betalingsbestand geëxporteerd** of **Tot. geëxporteerd bedrag** en vervolgens betalingsvoorstellen verwijderen voor openstaande facturen waarvoor al betalingen zijn verricht en waarvoor u geen betalingen meer wilt verrichten.
* Op de pagina **Leveranciersbetalingen voorstellen**, waar u ook opgeeft welke betalingen in het betalingsdagboek worden ingevoegd, kunt u het selectievakje **Geëxporteerde betalingen overslaan** inschakelen als u geen dagboekregels wilt invoegen voor betalingen die al zijn geëxporteerd.

Als u informatie over geëxporteerde gegevens wilt bekijken, kiest u de actie **Historie betalingsexport**.

### <a name="to-re-export-payments-to-a-bank-file" />Betalingen naar een bankbestand opnieuw exporteren

U kunt betalingsbestanden opnieuw exporteren vanuit de pagina **Krediettransferregisters**. Voordat u betalingsdagboekregels verwijdert of boekt, kunt u het betalingsbestand ook opnieuw exporteren vanuit de pagina **Betalingsdagboek** door het nogmaals te importeren. Als u betalingsdagboekregels hebt verwijderd of geboekt nadat u deze hebt geëxporteerd, kunt u hetzelfde betalingsbestand opnieuw exporteren vanuit de pagina **Krediettransferregisters**. Selecteer de regel voor de batch kredietoverboekingen die u opnieuw wilt exporteren, en gebruik vervolgens de actie **Betalingen opnieuw exporteren naar bestand**.

> [!NOTE]  
> Geëxporteerde EFT-bestanden worden niet op de pagina **Krediettransferregisters** weergegeven en kunnen niet opnieuw worden geëxporteerd.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Krediettransferregisters** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer een betalingexport die u opnieuw wilt exporteren en kies de actie **Betalingen opnieuw exporteren naar bestand**.

## <a name="posting-the-payments" />De betalingen boeken

Wanneer de elektronische betaling is verwerkt door de bank, boekt u de betalingen. Zie voor meer informatie [Betalingen doen](payables-make-payments.md).

## <a name="see-also" />Zie ook

[De AMC Banking 365 Fundamentals-extensie gebruiken](ui-extensions-amc-banking.md)  
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Betalingen incasseren met automatische incasso via SEPA](finance-collect-payments-with-sepa-direct-debit.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
