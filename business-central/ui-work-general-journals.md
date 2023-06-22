---
title: Werken met dagboeken om direct naar het grootboek te boeken
description: 'Leren over het gebruik van dagboeken om financiële transacties naar grootboekrekeningen en andere rekeningen te boeken, zoals bank-, klant- en leveranciersrekeningen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 12/27/2022
ms.custom: bap-template
ms.search.keywords: 'journals, recurring, accrual, renumber, bulk-post'
ms.search.form: '39, 101, 102, 182, 184, 185, 201, 207, 250, 251, 253, 255, 256, 261, 262, 283, 519, 750, 751, 752, 753, 754, 755, 12409, 12410, 12411, 1290, 10101, 11400, 11402, 11403, 11405, 11300, 2000000, 2000001, 2000003, 2000020, 2000021, 2000022'
---
# <a name="work-with-general-journals" />Werken met diversendagboeken

De meeste financiële transacties worden geboekt naar het grootboek door bedrijfsdocumenten, zoals inkoopfacturen en verkooporders. U kunt echter ook bedrijfsactiviteiten verwerken zoals:

* Inkoop
* Betalingen
* Periodieke dagboeken gebruiken om transitoria te boeken
* Personeelskosten terugbetalen door journaalregels in journaals te boeken  

De meeste dagboeken zijn gebaseerd op het diversendagboek en u kunt alle transacties op de pagina **Diversendagboek** verwerken. Zie voor meer informatie [Transacties direct naar het grootboek boeken](finance-how-post-transactions-directly.md).  

U kunt bijvoorbeeld personeelskosten boeken voor vergoedingen. Zie voor meer informatie [Kosten van werknemers registreren en terugbetalen](finance-how-record-reimburse-employee-expenses.md).

Maar [!INCLUDE [prod_short](includes/prod_short.md)] biedt ook dagboeken die voor bepaalde soorten transacties zijn geoptimaliseerd, zoals het **Betalingsdagboek** voor het registreren van betalingen. Zie voor meer informatie [Betalingen en terugbetalingen vastleggen in het betalingsdagboek](payables-how-post-payments-refunds.md).  

Met dagboeken kunt u financiële transacties boeken naar grootboekrekeningen en verschillende andere rekeningen. De andere rekeningen omvatten bank-, klant-, leveranciers- en werknemersrekeningen. Boeken met een dagboek maakt posten op grootboekrekeningen, zelfs wanneer u bijvoorbeeld een journaalregel naar een klantrekening boekt. De post wordt via een boekingsgroep geboekt op een grootboekvorderingen.

De informatie die u invoert in een dagboek is tijdelijk en kan in het dagboek worden gewijzigd. Wanneer u het dagboek boekt, wordt de informatie overgedragen naar posten op afzonderlijke rekeningen, waar de informatie niet meer kan worden gewijzigd. U kunt echter de vereffening van geboekte posten ongedaan maken en u kunt tegenboekingen of corrigerende boekingen maken. Zie voor meer informatie [Journaalboekingen tegenboeken en ontvangsten/zendingen ongedaan maken](finance-how-reverse-journal-posting.md).

> [!NOTE]
> [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]  

## <a name="use-journal-templates-and-batches" />Dagboeksjablonen en -batches gebruiken

Er zijn verschillende sjablonen voor diversendagboeken. Elk dagboeksjabloon wordt vertegenwoordigd door een speciale pagina met specifieke functies en de velden die nodig zijn om die functies te ondersteunen, zoals de pagina **Dagboek betalingsreconciliatie**, om bankbetalingen te verwerken en de pagina **Betalingsdagboek** om uw leveranciers te betalen en kosten van uw werknemers te vergoeden. Zie voor meer informatie [Betalingen doen](payables-make-payments.md) en [Klantbetalingen reconciliëren met het ontvangstendagboek of vanuit klantposten](receivables-how-apply-sales-transactions-manually.md).

Voor elke dagboeksjabloon kunt u uw eigen persoonlijke dagboek instellen als een dagboekbatch. U kunt bijvoorbeeld uw eigen dagboekbatch definiëren voor het betalingsdagboek dat uw persoonlijke lay-out en instellingen heeft. De volgende tip is een voorbeeld van hoe u een dagboek aanpast.

> [!TIP]  
> Als u het selectievakje **Salderingsbedrag voorstellen** inschakelt op de regel voor uw batch op de pagina **Fin. dagboekbatches**, wordt het veld **Bedrag** op bijvoorbeeld diversendagboekregels voor hetzelfde documentnummer automatisch vooraf ingevuld met de waarde die is vereist om het document sluitend te maken. Lees meer op [[!INCLUDE[prod_short](includes/prod_short.md)] waarden laten voorstellen](ui-let-system-suggest-values.md).

> [!TIP]
> U kunt velden in dagboeken toevoegen of verwijderen door ze te personaliseren. Zie voor meer informatie [Uw werkruimte personaliseren](ui-personalization-user.md).

### <a name="validating-general-journal-batches" />Algemene dagboekbatches valideren

U kunt een achtergrondcontrole inschakelen om vertragingen bij het boeken te voorkomen. De controle geeft een melding wanneer een fout in het financiële journaal waaraan u werkt, ervoor zorgt dat u het journaal niet kunt boeken. Op de pagina **Batch van algemeen dagboek** kunt u **Foutcontrole op achtergrond** kiezen om [!INCLUDE[prod_short](includes/prod_short.md)] financiële dagboeken te laten valideren, zoals algemene of betalingsdagboeken, terwijl u eraan werkt.

Wanneer u de validatie inschakelt, toont het feitenblok **Dagboekcontrole** problemen op de huidige regel en in de hele batch. Validatie vindt plaats wanneer u een financiële dagboekbatch laadt en wanneer u een andere dagboekregel kiest. De tegel **Totaal aantal problemen** in het feitenblok toont het totale aantal problemen dat [!INCLUDE[prod_short](includes/prod_short.md)] heeft gevonden en u kunt ervoor kiezen om een overzicht van de problemen te openen.

U kunt de acties **Regels met problemen weergeven** en **Alle regels weergeven** gebruiken om te schakelen tussen dagboekregels die wel of geen problemen hebben. Het feitenblok **Details van dagboekregel** biedt een snel overzicht van en toegang tot gegevens uit dagboekregels, zoals de grootboekrekening, klant of leverancier, en de boekingsinstellingen voor specifieke rekeningen.

[!INCLUDE [background_doc_journal_check](includes/background_doc_journal_check.md)]  

## <a name="understanding-main-accounts-and-balancing-accounts" />Hoofdrekeningen en tegenrekeningen

Als u op de pagina **Dagboeken** standaardtegenrekeningen hebt ingesteld voor de dagboekbatches, wordt de tegenrekening automatisch ingevuld wanneer u het veld **Rekeningnr.** invult. Anders vult u zowel het veld **Rekeningnummer** als het veld **Tegenrekeningnummer** handmatig in. Een positief bedrag in het veld **Bedrag** wordt gedebiteerd van de hoofdrekening en gecrediteerd naar de tegenrekening. Een negatief bedrag wordt gecrediteerd naar de hoofdrekening en gedebiteerd van de tegenrekening.

> [!NOTE]  
> Btw wordt afzonderlijk berekend voor de hoofdrekening en de tegenrekening, zodat er gebruik kan worden gemaakt van verschillende percentages.

## <a name="work-with-recurring-journals" />Werken met periodieke dagboeken

Een periodiek dagboek is een dagboek met specifieke velden voor het beheer van transacties die u vaak boekt met weinig of geen wijzigingen. Bijvoorbeeld transacties voor uitgaven als huur, abonnementen, elektriciteit en verwarming. Door periodieke dagboeken te gebruiken kunt u vaste en variabele bedragen boeken en automatische tegenboekingen opgeven voor de dag na de boekingsdatum. U kunt verdeelsleutels gebruiken om de periodieke posten over verschillende rekeningen te verdelen. Meer informatie op [Periodieke dagboekbedragen toewijzen aan meerdere rekeningen](#allocating-recurring-journal-amounts-to-several-accounts).

Met een periodiek dagboek maakt u de posten die regelmatig worden geboekt, slechts eenmaal. De rekeningen, dimensies, dimensiewaarden enzovoort worden bijvoorbeeld na het boeken in het dagboek bewaard. Als er wijzigingen nodig zijn, kunt u deze elke keer dat u een bericht plaatst, aanbrengen.

### <a name="recurring-method-field" />Veld Methode

Het veld **Periodieke methode** is belangrijk. Het bepaalt hoe het bedrag op de dagboekregel na het boeken wordt behandeld. Wanneer u de regel bijvoorbeeld altijd met hetzelfde bedrag wilt boeken, kunt u het bedrag ongewijzigd laten. Wilt u dezelfde rekeningen en dezelfde tekst gebruiken, maar een ander bedrag, dan kunt u het bedrag na het boeken verwijderen.

| Als u dit wilt doen: | Zie |
| --- | --- |
|V Vast|het bedrag op de dagboekregel wordt na het boeken bewaard.|
|V Variabel|het bedrag op de dagboekregel wordt na het boeken verwijderd.|
|S Saldo|Het geboekte bedrag op de rekening op de regel wordt verdeeld over de rekeningen die zijn opgegeven voor de regel in de tabel Dagboekverdeelsleutel. Het saldo op de rekening wordt op nul ingesteld. Vul het veld **Verdeelsleutel %** op de pagina **Verdeelsleutels** in. Zie voor meer informatie [Periodieke dagboekbedragen toewijzen aan meerdere rekeningen](#allocating-recurring-journal-amounts-to-several-accounts).|
|OV Omgekeerd vast|Het bedrag wordt na het boeken bewaard en de tegenboeking wordt de volgende dag geboekt.|
|OR Omgekeerd vaRiabel|Het bedrag wordt na het boeken verwijderd en de tegenboeking wordt de volgende dag geboekt.|
|OS Omgekeerd saldo|Het geboekte bedrag op de rekening op de regel wordt verdeeld over de rekeningen die zijn opgegeven voor de regel op de pagina **Verdeelsleutels**. Het saldo op de rekening moet op nul zijn ingesteld en een tegenrekeningspost wordt de dag erop geboekt.|
|SD Saldo per dimensie|De dagboekregel wijst kosten toe op basis van het saldo van een grootboekrekening per dimensie. U wordt gevraagd de dimensiefilters in te stellen die moeten worden gebruikt om het saldo van de brongrootboekrekening te berekenen per dimensie waaruit u kosten wilt toewijzen. U kunt ook later als alternatief de actie **Dimensiefilters instellen** kiezen.|
|OSD Omgekeerd saldo per dimensie|De dagboekregel wijst kosten toe op basis van het omgekeerd saldo van een grootboekrekening per dimensie. U wordt gevraagd de dimensiefilters in te stellen die moeten worden gebruikt om het saldo van de brongrootboekrekening te berekenen per dimensie waaruit u kosten wilt toewijzen. U kunt ook later de actie **Dimensiefilters instellen** kiezen.|

> [!NOTE]  
> De btw-velden kunnen worden ingevuld op de periodieke dagboekregel of op de verdelingsdagboekregel, maar niet op beide. De btw-velden kunt u alleen invullen op de pagina **Verdeelsleutels** als de overeenkomende regels in het periodieke dagboek niet zijn ingevuld.

### <a name="recurring-frequency-field" />Veld Frequentie

Dit veld voor de datumformule bepaalt hoe vaak de boeking op de journaalregel moet worden geboekt en moet worden ingevuld. Zie voor meer informatie [Datumformules gebruiken](ui-enter-date-ranges.md#use-date-formulas).

#### <a name="examples" />Voorbeelden

Als de dagboekregel bijvoorbeeld elke maand moet worden geboekt, voert u "1M" in. Na elke boeking wordt de datum in het veld **Boekingsdatum** automatisch bijgewerkt met een maand.

Wanneer u een bepaalde post wilt boeken op de laatste dag van elke maand, kunt u dit op een van de volgende manieren doen:

* Boek de eerste post op de laatste dag van een maand door 1D+1M-1D (1 dag + 1 maand - 1 dag) in te vullen. Met deze formule wordt de boekingsdatum correct berekend, ongeacht het aantal dagen in de maand.

* Boek de eerste post op een willekeurige dag van de maand door 1M+LM in te voeren. Met deze formule ligt de boekingsdatum na een hele maand + de resterende dagen van de huidige maand.

### <a name="expiration-date-field" />Veld Vervaldatum

Dit veld is de datum waarop de regel voor het laatst wordt geboekt. De regel wordt niet geboekt na deze datum.

Voordeel van gebruik van het veld Vervaldatum is dat de regel niet onmiddellijk uit het dagboek wordt verwijderd. U kunt een latere datum invoeren, zodat u de regel in de toekomst kunt gebruiken.

Als het veld leeg is, wordt de regel steeds geboekt totdat deze uit het dagboek wordt verwijderd.

### <a name="allocating-recurring-journal-amounts-to-several-accounts" />Periodieke dagboekbedragen toewijzen aan meerdere rekeningen

Op de pagina **Periodiek dagboek** kunt u de actie **Verdeelsleutels** kiezen om op te geven hoe bedragen op de periodieke dagboekregel worden toegewezen aan verschillende rekeningen en dimensies. Een verdeelsleutel fungeert als tegenrekeningregel voor de periodieke dagboekregel.

Net als bij een periodiek journaal voert u een toewijzing één keer in en blijft deze na het boeken in het toewijzingsjournaal. U hoeft niet telkens bedragen en toewijzingen in te voeren wanneer u de periodieke dagboekregel boekt.

Als de periodieke methode in het periodieke dagboek is ingesteld op **Saldo** of **Omgekeerd saldo**, wordt geen rekening gehouden met dimensiewaardecodes in het periodieke dagboek als de rekening is ingesteld op nul. Dit betekent dat als u op de pagina **Verdeelsleutels** een periodieke regel verdeelt over verschillende dimensiewaarden, er slechts één tegenpost wordt gemaakt.

> [!NOTE]
> Wanneer u een periodieke dagboekregel verdeelt die een dimensiewaardecode bevat, moet u dezelfde code daarom niet invoeren op de pagina **Verdeelsleutels**. Als u dat wel doet, zijn de dimensiewaarden onjuist.  

Om periodieke dagboekbedragen toe te wijzen op basis van dimensies, stelt u het veld **Periodieke methode** in op **Saldo per dimensie** of **Omgekeerd saldo per dimensie**. Als de periodieke methode in het periodieke dagboek is ingesteld op **Saldo per dimensie** of **Omgekeerd saldo per dimensie**, wordt rekening gehouden met dimensiewaardecodes in het periodieke dagboek als de rekening is ingesteld op nul. Als u een terugkerende regel toewijst aan verschillende dimensiewaarden op de pagina **Toewijzingen**, worden tegenboekingen gemaakt die overeenkomen met het aantal dimensiewaardecombinaties waaruit het saldo bestaat. Als u rekeningsaldo toewijst via het periodieke dagboek dat een dimensiewaardecode bevat, vergeet dan niet om **Saldo per dimensie** of **Omgekeerd saldo per dimensie** te gebruiken om ervoor te zorgen dat de dimensiewaarden correct in evenwicht zijn of worden omgekeerd ten opzichte van de bronaccount.  

Uw bedrijf heeft bijvoorbeeld een aantal bedrijfsunits en een handvol afdelingen die uw controllers als dimensies hebben ingesteld. Om het invoerproces van inkoopfacturen te versnellen besluit u dat de crediteurenadministratie alleen bedrijfsunitdimensies moet invoeren. Aangezien elke bedrijfsunit specifieke verdeelsleutels heeft voor de dimensie Afdeling, bijvoorbeeld op basis van het aantal werknemers, kunt u de periodieke methoden **Saldo per dimensie** of **Omgekeerd saldo per dimensie** gebruiken om kosten voor elke bedrijfsunit opnieuw toe te wijzen aan de juiste afdelingen op basis van de verdeelsleutels.  

> [!NOTE]
> Dimensies die u op verdeelsleutelregels instelt, worden niet automatisch berekend en u moet specificeren welke dimensiewaarden moeten worden ingesteld voor de verdelingsrekeningen. Als u de koppeling tussen de dimensie van de bronrekening en de dimensie van de verdelingsrekening wilt behouden, raden we u aan in plaats daarvan de mogelijkheden van [Kostprijsboekhouding](finance-about-cost-accounting.md) te gebruiken.

#### <a name="example-allocating-rent-payments-to-different-departments" />Voorbeeld: huurbetalingen aan verschillende kostenplaatsen toewijzen

U betaalt elke maand huur en u hebt het huurbedrag dus ingevoerd op de kasrekening op een periodieke dagboekregel. Op de pagina **Verdeelsleutels** kunt u de dimensie Afdeling gebruiken om de onkosten over verschillende afdelingen te verdelen. Bijvoorbeeld op basis van het aantal vierkante meter dat elke afdeling in beslag neemt. De berekening is gebaseerd op het verdelingspercentage op elke regel. U kunt op verschillende manieren toewijzen:

* Voer verschillende rekeningen in op verschillende toewijzingsregels om de huurkosten over meerdere rekeningen te verdelen.
* Voer dezelfde rekening in, maar gebruik op elke regel verschillende dimensiewaardecodes voor de dimensie Afdeling.

[!INCLUDE [rev-general-journal](includes/rev-general-journal.md)]

### <a name="calculate-the-reversal-date" />De tegenboekingsdatum berekenen

Wanneer u periodieke dagboeken gebruikt om transitoria aan het einde van een periode te boeken, is het belangrijk om volledige controle te hebben over tegenboekingsposten. Op de pagina **Periodieke dagboeken** kunt u met het veld **Berekening van tegenboekingsdatum** bepalen op welke datum tegenboekingsposten worden geboekt wanneer periodieke tegenboekingsmethoden worden gebruikt.

#### <a name="example" />Opmerking

Transitoria worden meestal geboekt met periodieke methoden **Vast**, **Variabel** of **Saldo** op de dagboekregel. De boekingsdatum van het geboekte bedrag op de rekening op de dagboekregel wordt berekend met de periodieke frequentie. De boekingsdatum voor de tegenboeking wordt als volgt berekend met behulp van het veld **Berekening van tegenboekingsdatum**:

* Als het veld leeg is, wordt de tegenboekingspost de volgende dag geboekt.
* Als het veld een datumformule bevat (bijvoorbeeld **5D** voor vijf dagen), wordt de tegenboekingspost geboekt met een boekingsdatum die wordt berekend op basis van de berekening van de tegenboekingsdatum.

> [!NOTE]
> Standaard is het veld **Berekening van tegenboekingsdatum** niet beschikbaar op de pagina **Periodieke dagboeken**. Om het veld te gebruiken moet u het toevoegen door de pagina te personaliseren. Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.

## <a name="work-with-standard-journals" />Werken met standaarddagboeken

Wanneer u artikeldagboekregels hebt gemaakt waarvan u weet dat u ze waarschijnlijk later opnieuw moet maken, kunt u ze als een standaarddagboek opslaan voordat u het artikeldagboek boekt. Hetzelfde geldt voor artikeldagboeken en diversendagboeken.

> [!NOTE]
> Standaarddagboeken bevatten mogelijk niet alle velden die u wilt opnemen in de resulterende grootboekposten. Als u bijvoorbeeld een standaarddagboek gebruikt om een betaling te registreren, bevatten de grootboekposten niet het veld Betalingsmethodecode.

> [!NOTE]  
> De volgende procedures hebben betrekking op het artikeldagboek, maar de informatie is ook van toepassing op het algemene dagboek.

### <a name="to-save-a-standard-journal" />Opslaan als standaarddagboek

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikeldagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Voer een of meer dagboekregels in.
3. Selecteer de dagboekregels die u opnieuw wilt gebruiken.
4. Kies de actie **Opslaan als standaarddagboek**.
5. Op de aanvraagpagina **Opslaan als standaardartikeldagboek** definieert u een nieuw of bestaand standaardartikeldagboek waarin de regels moeten worden opgeslagen.

    Als u al een of meer standaardartikeldagboeken hebt gemaakt en u een van deze dagboeken wilt vervangen door de nieuwe reeks artikeldagboekregels, selecteert u het artikeldagboek in het veld **Code**.
6. Klik op **OK** om te controleren dat u de inhoud van het bestaande standaardartikeldagboek wilt vervangen.
7. Selecteer het veld **Eenheidsprijs opslaan** als u de waarden in het veld **Eenheidsprijs** van het standaardartikeldagboek wilt opslaan.
8. Om de waarden op te slaan in het veld **Aantal** kiest u het veld **Aantal opslaan**.
9. Kies **OK** om het standaardartikeldagboek op te slaan.

Wanneer u het standaardartikeldagboek opslaat, wordt de pagina Artikeldagboek weergegeven zodat u het kunt boeken.

### <a name="to-reuse-a-standard-journal" />Een standaarddagboek opnieuw gebruiken

> [!NOTE]
> Standaardjournalen hebben niet altijd dezelfde velden als algemene dagboeken. Wanneer u de actie Standaarddagboeken ophalen gebruikt om de velden naar het algemene dagboek te kopiëren, bevat het algemene dagboek mogelijk minder informatie dan wanneer u het dagboek handmatig zou maken. 

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikeldagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Standaarddagboeken ophalen**.
3. Als u een standaardartikeldagboek wilt controleren voordat u het selecteert voor hergebruik, kiest u de actie **Dagboek tonen**.

    Wijzigingen die u aanbrengt in een standaardartikeljournaal worden meteen doorgevoerd en zijn er de volgende keer dat u het standaard artikeljournaal opent of opnieuw gebruikt. Zorg dat de wijziging belangrijk genoeg is om algemeen toe te passen. Breng de specifieke wijziging in het artikeldagboek anders pas aan nadat de standaardartikeldagboekregels zijn toegevoegd. Zie stap 4.
4. Selecteer op de pagina **Standaardartikeldagboeken** het standaardartikeldagboek dat u opnieuw wilt gebruiken en kies vervolgens de knop **OK**.

    Het artikeljournaal bevat de regels die u hebt opgeslagen. Als het artikeldagboek al regels heeft, verschijnen de nieuwe regels erna.

    Als u de schakelaar **Eenheidsbedrag opslaan** niet inschakelt bij het opslaan van het dagboek, bevat het veld **Eenheidsbedrag** op regels die zijn toegevoegd vanuit het standaarddagboek, de waarde uit het veld **Kostprijs** op de artikelkaart.

    > [!NOTE]  
    > Als u de schakelaars **Eenheidsbedrag opslaan** of **Aantal opslaan** hebt ingeschakeld bij het opslaan van het dagboek, zorg er dan voor dat de nieuwe waarden correct zijn voordat u het artikeljournaal boekt.
    >
    > Als de ingevoegde artikeldagboekregels opgeslagen eenheidsprijzen bevatten die u niet wilt boeken, kunt u deze wijzigen in de huidige waarde van het artikel.

5. Selecteer de dagboekregels die u wilt aanpassen en kies vervolgens de actie **Eenheidsprijs opnieuw berekenen**. Deze actie werkt het veld Eenheidsprijs bij met de huidige kostprijs van het artikel.
6. Kies de actie **Boeken**.

## <a name="to-renumber-document-numbers-in-journals" />Documentnummers in dagboeken opnieuw nummeren

Om er zeker van te zijn dat u geen boekingsfouten ontvangt vanwege de documentvolgorde, kunt u de actie **Documentnummers opnieuw nummeren** gebruiken voordat u een journaal boekt.

In alle dagboeken die zijn gebaseerd op het algemene dagboek, kan het veld **Documentnr.** worden bewerkt, zodat u voor verschillende dagboekregels verschillende documentnummers of hetzelfde documentnummer voor verwante dagboekregels kunt opgeven.

Als het veld **Nr.-reeksen** op de dagboekbatch is gevuld, vereist de boekingsfunctie in dagboeken dat de documentnummers op de afzonderlijke of gegroepeerde dagboekregels in sequentiële volgorde worden weergegeven. Kies gewoon de actie **Documentnummers hernummeren** en de relevante **Documentnr.**-velden worden dan bijgewerkt. Als verwante dagboekregels zijn gegroepeerd op documentnummer voordat u de functie gebruikte, blijven ze gegroepeerd, maar wordt er mogelijk een ander documentnummer aan toegewezen.  

Deze functie werkt ook op de gefilterde weergaven.

Het wijzigen van documentnummers houdt rekening met verwante vereffeningen, zoals een betalingsaanvraag die is ingediend vanuit het document op de dagboekregel naar een leveranciersrekening. De velden **Vereffenings-id** en **Vereffeningsnr.** worden overeenkomstig bijgewerkt in de posten.

### <a name="to-renumber-documents-in-journals" />Documentnummers in dagboeken opnieuw nummeren

De volgende procedure is gebaseerd op de pagina **Diversendagboek**, maar is van toepassing op alle overige journalen die u op het dagboek zijn gebaseerd, zoals de pagina **Betalingsdagboek**.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Financiële dagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Als u klaar bent om het dagboek te boeken, kiest u de actie **Documentnummers opnieuw nummeren**.

De waarden in het veld **Documentnr.** worden gewijzigd, wanneer dit is vereist, zodat het documentnummer op afzonderlijke of gegroepeerde dagboekregels in sequentiële volgorde wordt weergegeven. Nadat documenten opnieuw zijn genummerd, kunt u het dagboek boeken.

## <a name="see-related-microsoft-trainingtrainingpathsuse-journals-dynamics--business-central" />Zie gerelateerde [Microsoft-training](/training/paths/use-journals-dynamics-365-business-central/)

## <a name="see-also" />Zie ook

[Transacties direct naar het grootboek boeken](finance-how-post-transactions-directly.md)  
[Journaalboekingen tegenboeken en ontvangsten/zendingen ongedaan maken](finance-how-reverse-journal-posting.md)  
[Kosten en inkomsten toewijzen](year-allocate-costs-income.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Open artikelposten die uit een vaste vereffening in het artikeldagboek voortkomen sluiten](finance-how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)  
[Voorraad herwaarderen in het herwaarderingsjournaal](inventory-how-revalue-inventory.md)  
[Voorraad tellen, corrigeren en herindelen met dagboeken](inventory-how-count-adjust-reclassify.md)  
[Klantbetalingen reconciliëren met het ontvangstendagboek of vanuit klantenposten](receivables-how-apply-sales-transactions-manually.md)  
[Leveranciersbetalingen reconciliëren met het betalingsdagboek of vanuit leveranciersposten](payables-how-apply-purchase-transactions-manually.md)  
[Werken met intercompany-documenten en -dagboeken](intercompany-how-work-documents-journals.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
