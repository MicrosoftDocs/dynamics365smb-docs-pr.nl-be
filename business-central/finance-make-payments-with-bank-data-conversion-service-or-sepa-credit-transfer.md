---
title: Betalingen doen met AMC banking (VS) of SEPA-overschrijving (EU)
description: Verwerk betalingen aan uw leveranciers door samen met de betalingsgegevens van de dagboekregels een bestand te exporteren.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.search.form: '256, 1205, 1206, 1209, 10810, 10811'
ms.date: 08/26/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---
# <a name="make-payments-with-the-amc-banking-365-fundamentals-extension-or-sepa-credit-transfer"></a>Betalingen uitvoeren met de AMC banking 365 fundamentals-extensie of SEPA-overschrijving

Op de pagina  **Betalingsjournalen** kunt u betalingen aan uw leveranciers verwerken door een bestand te exporteren met de betalingsgegevens uit de journaalregels. Vervolgens kunt u het bestand uploaden naar uw elektronische banksite waar de gerelateerde overboekingen worden verwerkt. [!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt het SEPA Credit Transfer-formaat, maar in uw land/regio zijn mogelijk andere formaten voor elektronische betalingen beschikbaar.

> [!NOTE]
> In de algemene versie van [!INCLUDE[prod_short](includes/prod_short.md)] wordt een algemene provider van services ingesteld en verbonden die bankgegevens converteert naar een bestandsindeling die uw bank vereist. In Noord-Amerikaanse versies kan dezelfde service worden gebruikt om betalingsbestanden te verzenden als elektronische overboeking (EFT), bijvoorbeeld het veelgebruikte ACH-netwerk (Automated Clearing House), maar met een iets ander proces. Zie stap 6 in [Betalingen naar een bankbestand exporteren](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).  

 Voor het mogelijk maken van SEPA-kredietoverboekingen moet u eerst een bankrekening, leverancier, en dagboekbatch instellen waarop het betalingsdagboek is gebaseerd. Vervolgens bereidt u betalingen aan leveranciers voor door de pagina  **Betalingsjournalen** automatisch te vullen met verschuldigde betalingen met opgegeven boekingsdatums.  

Nadat u hebt gecontroleerd of de bank de betalingen heeft verwerkt, kunt u de betalingsjournaalregels boeken.  

## <a name="setting-up-the-amc-banking-365-fundamentals-extension"></a>De AMC Banking 365 Fundamentals extensie instellen

Activeer de AMC Banking 365 Fundamentals extensie om:

* Converteer bankafschriftbestanden naar een formaat dat u kunt importeren.
* Converteer uw geëxporteerde betalingsbestanden naar het formaat dat uw bank vereist.

Zie voor meer informatie [De extensie AMC Banking 365 Fundamentals gebruiken](ui-extensions-amc-banking.md).

## <a name="setting-up-sepa-credit-transfer"></a>SEPA-overschrijving instellen

Op de pagina  **Betalingslogboeken** kunt u betalingen exporteren naar een bestand. Vervolgens kunt u het bestand uploaden naar uw elektronische bank voor verwerking van de bijbehorende geldtransfers. [!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt het SEPA Credit Transfer-formaat, maar in uw land/regio zijn mogelijk andere formaten voor elektronische betalingen beschikbaar.  

Om een bankbestandsformaat te kunnen exporteren dat niet standaard wordt ondersteund in  [!INCLUDE[prod_short](includes/prod_short.md)], kunt u een definitie voor gegevensuitwisseling instellen. Zie [Definities voor gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md) voor meer informatie.  

Voordat u elektronische betaling kunt verwerken door betalingsbestanden te exporteren in de SEPA-overmakingsindeling, moet u de volgende instellingenstappen uitvoeren:  

* De betreffende bankrekening instellen om de indeling voor SEPA-kredietoverboekingen te verwerken  
* Leverancierskaarten instellen om betalingen te verwerken door bestanden te exporteren in de indeling voor SEPA-kredietoverboekingen  
* Stel de gerelateerde algemene dagboekbatch in om betalingsexport mogelijk te maken vanaf de pagina  **Betalingsjournalen**   
* De definitie van gegevensuitwisseling voor een of meer betalingstypen verbinden met de relevante betalingsmethode(n)  

> [!NOTE]
> Business Central ondersteunt zowel het SEPA-formaat CT pain.001.001.03 als CT pain.001.001.09. U kunt elk formaat kiezen op de pagina  **Bankrekeningnummer kaart** .  

> [!TIP]
> Dit artikel is van toepassing op de generieke versie van [!INCLUDE [prod_short](includes/prod_short.md)]. In uw land of regio zijn mogelijk extra verplichte velden toegevoegd aan de verschillende pagina's. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]

### <a name="to-set-up-a-bank-account-for-sepa-credit-transfer"></a>Een bankrekening instellen voor SEPA-kredietoverboekingen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Bankrekeningen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de bankrekening waarvan u betalingsbestanden in het SEPA-overschrijvingsformaat wilt exporteren.
3. Kies op het tabblad **Algemeen** in het veld **Berichtnummers krediettransfer** een nummerreeks waaruit nummers worden toegewezen aan SEPA-overmakingsposten.
4. Voer op het sneltabblad **Communicatie** het adres en de contactgegevens van de bank in. 

   > [!NOTE]
   > U moet het veld  **Land-/regiocode** invullen. Als het veld leeg is, kunt u geen betalingen voor de rekening exporteren. Bovendien moet het land/de regio een geldige ISO-code hebben.

5. Geef op het sneltabblad  **Boekingen** in het veld  **Valutacode**  de valuta voor de bankrekening op.  

   > [!NOTE]  
   > Het veld **Valutacode** moet worden ingesteld op **EUR**, omdat SEPA-kredietoverboekingen alleen kunnen worden gemaakt in de valuta EURO.  

6. Kies op het sneltabblad  **Overboeking** in het veld  **Exportformaat betaling**  het SEPA-formaat dat u wilt gebruiken.  
7. Geef in het veld  **IBAN** het internationale bankrekeningnummer voor de rekening op.  

### <a name="to-set-up-a-vendor-card-for-sepa-credit-transfer"></a>Een leverancierskaart instellen voor SEPA-kredietoverboekingen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Leveranciers** in en kies vervolgens de gerelateerde koppeling.  
2. Open het bestand kaart van de leverancier die u elektronisch betaalt door betalingsbestanden te exporteren in het SEPA-overschrijvingsformaat.  
3. Selecteer op het sneltabblad  **Betalingen** in het veld  **Betaalmethodecode** de optie  **BANK**.  
4. In het veld  **Gewenste bankrekening** kiest u de bank waarnaar het geld wordt overgemaakt wanneer het door uw elektronische bank wordt verwerkt.  

    Als u nog geen bank rekeningengroep voor deze leverancier heeft, kunt u dat nu doen. Zie voor meer informatie [Bankrekeningen van leveranciers instellen voor het exporteren van bankbestanden](bank-how-setup-bank-accounts.md#to-set-up-vendor-bank-accounts-for-export-of-bank-files). De waarde in het veld **Bankrekeningcode van voorkeur** wordt gekopieerd naar het veld **Bankrekening ontvanger** op de pagina **Betalingsdagboek**.  

### <a name="to-set-the-payment-journal-up-to-export-payment-files"></a>Het betalingsdagboek instellen om betalingsbestanden te exporteren

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Betalingsdagboeken** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de vervolgkeuzeknop in het veld **Batchnaam**.  
3. Kies op de pagina **Algemene journaalbatches** de actie **Lijst bewerken**.  
4. Selecteer het selectievakje  **Betalingsexport toestaan**  op de regel voor het betalingsjournaal dat u gebruikt om betalingen te exporteren.  

### <a name="to-connect-the-data-exchange-definition-for-one-or-more-payment-types-with-the-relevant-payment-method-or-methods"></a>De definitie van gegevensuitwisseling voor een of meer betalingstypen verbinden met de relevante betalingsmethode(n)

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsmethoden** in en kies vervolgens de gerelateerde koppeling.  
2. Op de pagina **Betalingsmethoden** selecteert u de betalingswijze die wordt gebruikt om betalingen te exporteren en vervolgens kiest u het veld **Regeldefinitie betalingsexport**.  
3. Selecteer op de pagina **Regeldefinities betalingsexport** de code die u hebt opgegeven in het veld **Code** op het sneltabblad **Regeldefinities** in stap 4 van de sectie 'De opmaak van regels en kolommen in het bestand beschrijven' van [Definities voor gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md).  

## <a name="preparing-the-payment-journal"></a>Het betalingsjournaal voorbereiden

Vul het betalingsdagboek met regels voor verschuldigde betalingen aan leveranciers, met de mogelijkheid boekingsdatums in te voegen op basis van de vervaldatum van de verwante inkoopdocumenten. Zie [Betalingsverplichtingen beheren](payables-manage-payables.md) voor meer informatie.

## <a name="exporting-payments-to-a-bank-file"></a>Betalingen exporteren naar een bankbestand

Wanneer u klaar bent om betalingen aan uw leveranciers of vergoedingen aan uw werknemers te doen, kunt u een bestand exporteren met de betalingsgegevens op de regels op de pagina  **Betalingsjournalen** . Vervolgens kunt u het bestand uploaden naar uw bank voor verwerking van de betreffende overboekingen.

De extensie AMC Banking 365 Fundamentals is beschikbaar in de algemene versie van [!INCLUDE[prod_short](includes/prod_short.md)]. In Noord-Amerikaanse versies kan dezelfde uitbreiding worden gebruikt om betalingsbestanden als EFT's (elektronische overboekingen) worden gebruikt, zij het met een iets ander proces. Zie stap 6 in [Betalingen naar een bankbestand exporteren](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#to-export-payments-to-a-bank-file).

> [!NOTE]  
> Voordat u betalingsbestanden uit het betalingenjournaal kunt exporteren, moet u de elektronische indeling voor de desbetreffende bankrekening opgeven en moet u de extensie AMC Banking 365 Fundamentals inschakelen. Zie [Bankrekeningen instellen](bank-how-setup-bank-accounts.md) en [De extensie AMC Banking 365 Fundamentals gebruiken](ui-extensions-amc-banking.md) voor meer informatie. Bovendien moet u het selectievakje **Exporteren betaling toestaan** op de pagina **Fin. dagboekbatches** inschakelen. Zie voor meer informatie [Werken met diversendagboeken](ui-work-general-journals.md).  

Gebruik de pagina  **Kredietoverschrijvingsregisters** om de betalingsbestanden te bekijken die uit het betalingsjournaal zijn geëxporteerd. Vanaf deze pagina kunt u ook betalingsbestanden opnieuw exporteren als er technische fouten zijn opgetreden of als er bestandswijzigingen zijn opgetreden. Houd er echter rekening mee dat geëxporteerde EFT-bestanden niet op deze pagina worden weergegeven en niet opnieuw kunnen worden geëxporteerd.  

### <a name="to-export-payments-to-a-bank-file"></a>Betalingen naar een bankbestand exporteren

De volgende stappen beschrijven hoe u een leverancier per cheque betaalt. De stappen zijn vergelijkbaar met het terugbetalen van een klant per cheque.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Betalingsdagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Vul de betalingsdagboekregels in. Zie voor meer informatie [Betalingen en terugbetalingen vastleggen](payables-how-post-payments-refunds.md).

    > [!NOTE]
    > Als u EFT gebruikt, moet u **Elektronische betaling** of **Elektronische betaling-IAT** in het veld **Betalingssoort** selecteren. Andere services voor bestandsexport en de verschillende indelingen vereisen andere waarden op de pagina's **Bankrekeningkaart** en **Bankrekeningkaart leverancier**. U wordt over verkeerde of ontbrekende instellingswaarden geïnformeerd als u het bestand probeert te exporteren.
    >
    > De EFT-functie kan alleen worden gebruikt voor bankrekeningen in de lokale valuta. Het kan niet worden gebruikt met een vreemde valuta, aangegeven door een waarde in het veld **Valutacode**. (Lege veldwaarde betekent lokale valuta.)

3. Nadat u alle betalingsjournaalregels hebt ingevuld, kiest u de actie  **Exporteren** .
4. Vul op de pagina **Elektronische betalingen exporteren** de vereiste waarden in.

    Foutmeldingen worden weergegeven in het feitenvak  **Fouten in betalingsbestand**, waar u ook een foutmelding kunt selecteren om meer details te bekijken. U moet alle fouten oplossen voordat u het betalingsbestand kunt exporteren.

    > [!TIP]  
    > Wanneer u de extensie AMC Banking 365 Fundamentals gebruikt, wordt in een veel voorkomend foutbericht gemeld dat het bankrekeningnummer niet de juiste lengte voor uw bank heeft. Als u de fout wilt voorkomen of oplossen, moet u de waarde verwijderen uit het veld **IBAN** op de pagina **Bankrekeningkaart** en vervolgens in het veld **Bankrekeningnr.** een bankrekeningnummer invoeren in de indeling die uw bank vereist.

5. Geef op de pagina **Opslaan als** de locatie op waar het bestand naartoe wordt geëxporteerd en kies vervolgens **Opslaan**.

    > [!NOTE]  
    > Als u EFT gebruikt, sla dan het resulterende remiseformulier voor de leverancier op als Word-document of geef aan dat het rechtstreeks naar de leverancier moet worden gezonden. De betalingen worden nu toegevoegd aan de pagina **EFT-bestand genereren**, van waaruit u meerdere betaalopdrachten kunt genereren om de transmissiekosten te drukken. Zie de volgende stappen voor meer informatie.
6. Kies op de pagina **Betalingsjournalen** de actie **EFT-bestand genereren** .

    Op de pagina  **EFT-bestand genereren** wordt op het sneltabblad  **Regels** alle EFT-betalingen weergegeven die u hebt geëxporteerd uit het betalingsjournaal voor een bankrekening, maar die nog niet zijn gegenereerd.
7. Kies de actie **EFT-bestand genereren** om één bestand voor alle EFT-betalingen te exporteren.
8. Geef op de pagina **Opslaan als** de locatie op waar het bestand naartoe wordt geëxporteerd en kies vervolgens **Opslaan**.

Het bankbetalingsbestand wordt geëxporteerd naar de door u opgegeven locatie. U kunt het uploaden naar uw elektronische bankrekening en de daadwerkelijke betalingen verrichten. Vervolgens kunt u de geëxporteerde betalingsdagboekregels boeken.

### <a name="to-plan-when-to-post-exported-payments"></a>Plannen wanneer geëxporteerde betalingen worden geboekt

Als u geen betalingsjournaalregel voor een geëxporteerde betaling wilt boeken, kunt u de journaalregel gewoon verwijderen. Bijvoorbeeld omdat u wacht op de bevestiging dat de bank de transactie heeft verwerkt. Wanneer u later een betalingsjournaalregel aanmaakt om het resterende bedrag te betalen, wordt in het veld  **Totaal geëxporteerd bedrag**  weergegeven hoeveel van het betalingsbedrag al is geëxporteerd. U kunt ook gedetailleerde gegevens vinden over het geëxporteerde totaal door de knop **Krediettransferregisterposten** te kiezen om details over geëxporteerde betalingsbestanden te bekijken.

Als u geen betalingen wilt boeken totdat de bank de verwerking ervan heeft bevestigd, kunt u het volgende doen:

* In een betalingsdagboek met voorgestelde betalingsregels kunt u sorteren op: **Geëxporteerd naar betalingsbestand**  kolom of de **Totaal geëxporteerd bedrag**  en verwijder vervolgens betalingsvoorstellen voor openstaande facturen waarvoor al betalingen zijn gedaan.
* Op de **Leveranciersbetalingen voorstellen**  pagina, waar u aangeeft welke betalingen u in het betalingsdagboek wilt invoegen, kunt u de **Geëxporteerde betalingen overslaan**  selectievakje als u geen journaalregels wilt invoegen voor betalingen die al zijn geëxporteerd.

Als u informatie over geëxporteerde gegevens wilt bekijken, kiest u de actie **Historie betalingsexport**.

### <a name="to-re-export-payments-to-a-bank-file"></a>Betalingen naar een bankbestand opnieuw exporteren

U kunt betalingsbestanden opnieuw exporteren vanuit de pagina **Krediettransferregisters**. Voordat u betalingsjournaalregels verwijdert of boekt, kunt u het betalingsbestand ook opnieuw exporteren vanuit de **Betalingsjournaals**  pagina door deze opnieuw te exporteren. Als u de betalingsjournaalregels na uw export verwijdert of boekt, kunt u hetzelfde betalingsbestand opnieuw exporteren vanuit de **Kredietoverdrachtsregisters**  pagina. Selecteer de regel voor de batch kredietoverboekingen die u opnieuw wilt exporteren, en gebruik vervolgens de actie **Betalingen opnieuw exporteren naar bestand**.

> [!NOTE]  
> Geëxporteerde EFT-bestanden worden niet op de pagina **Krediettransferregisters** weergegeven en kunnen niet opnieuw worden geëxporteerd.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Krediettransferregisters** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer een betalingexport die u opnieuw wilt exporteren en kies de actie **Betalingen opnieuw exporteren naar bestand**.

## <a name="posting-the-payments"></a>Het boeken van de betalingen

Nadat uw bank de elektronische betaling heeft verwerkt, boekt u de betalingen. Zie voor meer informatie [Betalingen doen](payables-make-payments.md).

## <a name="see-also"></a>Zie ook

[De AMC Banking 365 Fundamentals-extensie gebruiken](ui-extensions-amc-banking.md)  
[Betalingsverplichtingen beheren](payables-manage-payables.md)  
[Werken met dagboeken](ui-work-general-journals.md)  
[Betalingen incasseren met automatische incasso via SEPA](finance-collect-payments-with-sepa-direct-debit.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
