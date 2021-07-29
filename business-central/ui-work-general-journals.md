---
title: Werken met dagboeken om direct naar het grootboek te boeken
description: Leren over het gebruik van dagboeken om financiële transacties naar grootboekrekeningen en andere rekeningen te boeken, zoals bank-, klant- en leveranciersrekeningen. Gebruik periodieke dagboeken om transitoria te boeken en saldi toe te wijzen op dimensiewaarden.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: journals, recurring, accrual, renumber, bulk-post
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 349dd312ae709c29138555ba6e8554a4f5e18122
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6445488"
---
# <a name="working-with-general-journals"></a>Werken met diversendagboeken

De meeste financiële transacties worden geboekt naar het grootboek door bepaalde bedrijfsdocumenten, zoals inkoopfacturen en verkooporders. Maar u kunt ook zakelijke activiteiten zoals inkoop, betaling, gebruik van periodieke dagboeken om transitoria te boeken of terugbetaling van werknemersonkosten, verwerken door dagboekregels te boeken in de verschillende dagboeken in [!INCLUDE[prod_short](includes/prod_short.md)].  

De meeste dagboeken zijn gebaseerd op het *Diversendagboek* en u kunt alle transacties op de pagina **Diversendagboek** verwerken. Zie voor meer informatie [Transacties direct naar het grootboek boeken](finance-how-post-transactions-directly.md).  

U kunt bijvoorbeeld de uitgaven boeken die werknemers uit eigen portemonnee doen, zodat u hen later kunt terugbetalen. Zie voor meer informatie [Uitgaven van werknemers vastleggen en terugbetalen](finance-how-record-reimburse-employee-expenses.md).

Maar in veel gevallen kunt u de dagboeken willen gebruiken die voor bepaalde soorten transacties zijn geoptimaliseerd, zoals het **Betalingsdagboek** voor het registreren van betalingen. Zie voor meer informatie [Betalingen en terugbetalingen vastleggen in het betalingsdagboek](payables-how-post-payments-refunds.md).  

Met diversendagboeken kunt u financiële transacties direct naar grootboekrekeningen en andere rekeningen boeken, zoals bank-, klant-, leveranciers- en werknemersrekeningen. Door te boeken met een dagboek worden er altijd posten gemaakt in grootboekrekeningen. Dit geldt zelfs ook als u bijvoorbeeld een dagboekregel naar een klantrekening boekt, omdat een post via een boekingsgroep is geboekt naar een rekening met vorderingen in het grootboek.

De informatie die u invoert in een dagboek is tijdelijk en kan in het dagboek worden gewijzigd. Wanneer u het dagboek boekt, wordt de informatie overgedragen naar de posten van afzonderlijke rekeningen, waar de informatie niet meer kan worden gewijzigd. U kunt echter de vereffening van geboekte posten ongedaan maken en u kunt tegenboekingen of corrigerende boekingen maken. Zie voor meer informatie [Journaalboekingen tegenboeken en ontvangsten/zendingen ongedaan maken](finance-how-reverse-journal-posting.md).

> [!NOTE]
> [!INCLUDE[journal-showhide-columns-inline-tip](includes/journal-showhide-columns-inline-tip.md)]  

## <a name="using-journal-templates-and-batches"></a>Dagboeksjablonen en -batches gebruiken

Er zijn verschillende sjablonen voor diversendagboeken. Elk dagboeksjabloon wordt vertegenwoordigd door een speciale pagina met specifieke functies en de velden die nodig zijn om die functies te ondersteunen, zoals de pagina **Dagboek betalingsreconciliatie**, om bankbetalingen te verwerken en de pagina **Betalingsdagboek** om uw leveranciers te betalen en kosten van uw werknemers te vergoeden. Zie voor meer informatie [Betalingen doen](payables-make-payments.md) en [Klantbetalingen reconciliëren met het ontvangstendagboek of vanuit klantposten](receivables-how-apply-sales-transactions-manually.md).

Voor elke dagboeksjabloon kunt u uw eigen persoonlijke dagboek instellen als een dagboekbatch. U kunt bijvoorbeeld uw eigen dagboekbatch definiëren voor het betalingsdagboek dat uw persoonlijke lay-out en instellingen heeft. De volgende tip is een voorbeeld van hoe u een dagboek aanpast.

> [!TIP]  
> Als u het selectievakje **Salderingsbedrag voorstellen** inschakelt op de regel voor uw batch op de pagina **Fin. dagboekbatches**, wordt het veld **Bedrag** op bijvoorbeeld diversendagboekregels voor hetzelfde documentnummer automatisch vooraf ingevuld met de waarde die is vereist om het document sluitend te maken. Zie voor meer informatie [[!INCLUDE[prod_short](includes/prod_short.md)] waarden laten voorstellen](ui-let-system-suggest-values.md).

> [!TIP]
> Als u velden in dagboeken wilt toevoegen of verwijderen, gebruikt u de banner **Personaliseren**. Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.

### <a name="validating-general-journal-batches"></a>Algemene dagboekbatches valideren
Om vertragingen bij het boeken te voorkomen kunt u een achtergrondcontrole inschakelen die u op de hoogte stelt als er een fout in het financiële dagboek waaraan u werkt optreedt waardoor u het dagboek niet kunt boeken. Op de pagina **Batch van algemeen dagboek** kunt u **Foutcontrole op achtergrond** kiezen om [!INCLUDE[prod_short](includes/prod_short.md)] financiële dagboeken te laten valideren, zoals algemene of betalingsdagboeken, terwijl u eraan werkt. 

Wanneer u de validatie inschakelt, wordt het feitenblok **Journaalcontrole** naast de dagboekregels weergegeven en bevat het problemen op de huidige regel en in de hele batch. Validatie vindt plaats wanneer u een financiële dagboekbatch laadt en wanneer u een andere dagboekregel kiest. De tegel **Totaal aantal problemen** in het feitenblok toont het totale aantal problemen dat [!INCLUDE[prod_short](includes/prod_short.md)] heeft gevonden en kunt u ervoor kiezen om een overzicht van de problemen te openen. 

U kunt de acties **Regels met problemen weergeven** en **Alle regels weergeven** gebruiken om te schakelen tussen dagboekregels die wel of geen problemen hebben. Het nieuwe feitenblok **Details van dagboekregel** biedt een snel overzicht van en toegang tot gegevens uit dagboekregels, zoals de grootboekrekening, klant of leverancier, evenals de boekingsinstellingen voor specifieke rekeningen.     

### <a name="reversing-journals-to-correct-mistakes"></a>Dagboeken terugdraaien om fouten te corrigeren
Wanneer u werkt met dagboeken met veel regels en er gaat iets mis, is het belangrijk om een gemakkelijke manier te hebben om fouten te corrigeren. De pagina **Geboekt financieel dagboek** biedt een aantal acties die kunnen helpen.

* **Geselecteerde regels naar dagboek kopiëren**: alleen de regels kopiëren die u selecteert.
* **Grootboekjournaal kopiëren naar dagboek**: alle regels kopiëren die behoren tot hetzelfde grootboekregister.

Met deze acties kunt u een kopie van een dagboekregel of een batch maken en vervolgens het volgende specificeren:

* Het dagboek waarnaar de regels moeten worden gekopieerd
* Of het met tegengestelde tekens moet gebeuren (een tegenboekingsdagboek)
* Een andere boekingsdatum of documentnummer

Om toe te staan dat dagboeken naar geboekte algemene dagboeken worden gekopieerd kiest u op de pagina **Financieel-dagboeksjablonen** het selectievakje **Kopiëren naar geboekte dagboekregels**. Nadat u mensen toestemming hebt gegeven om geboekte dagboeken te kopiëren, kunt u indien nodig het kopiëren uitschakelen voor specifieke batches.

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Hoofdrekeningen en tegenrekeningen
Als u op de pagina **Dagboeken** standaardtegenrekeningen hebt ingesteld voor de dagboekbatches, wordt de tegenrekening automatisch ingevuld wanneer u het veld **Rekeningnr.** invult. Anders vult u zowel het veld **Rekeningnr.** als het veld **Tegenrekeningnr.** handmatig in. Een positief bedrag in het veld **Bedrag** wordt gedebiteerd van de hoofdrekening en gecrediteerd naar de tegenrekening. Een negatief bedrag wordt gecrediteerd naar de hoofdrekening en gedebiteerd van de tegenrekening.

> [!NOTE]  
> Btw wordt afzonderlijk berekend voor de hoofdrekening en de tegenrekening, zodat er gebruik kan worden gemaakt van verschillende percentages.

## <a name="working-with-recurring-journals"></a>Werken met periodieke dagboeken
Een periodiek dagboek is een dagboek met specifieke velden voor het beheer van transacties die u regelmatig boekt met weinig of geen wijzigingen, zoals huur, abonnementen en elektriciteit. Met de speciale velden voor periodieke transacties kunt u zowel vaste als variabele bedragen boeken. U kunt ook automatische tegenboekingposten voor de dag na de boekingsdatum opgeven. U kunt ook verdeelsleutels gebruiken om de periodieke posten over verschillende rekeningen te verdelen. Zie voor meer informatie [Periodieke dagboekbedragen toewijzen aan meerdere rekeningen](#allocating-recurring-journal-amounts-to-several-accounts).

Als u een periodiek dagboek gebruikt, hoeft u de gegevens slechts éénmaal in te voeren. De ingevulde gegevens, zoals rekeningen, dimensies en dimensiewaarden, worden na het boeken in het dagboek bewaard. Later kunt u eventueel wijzigingen aanbrengen en de informatie opnieuw boeken.

### <a name="recurring-method-field"></a>Veld Methode

Dit veld bepaalt hoe het bedrag op de dagboekregel na het boeken wordt verwerkt. Wanneer u de regel bijvoorbeeld altijd met hetzelfde bedrag wilt boeken, kunt u het bedrag ongewijzigd laten. Wilt u dezelfde rekeningen en dezelfde tekst gebruiken, maar een ander bedrag, dan kunt u het bedrag na het boeken verwijderen.

| Als u dit wilt doen: | Zie |
| --- | --- |
|V Vast|het bedrag op de dagboekregel wordt na het boeken bewaard.|
|V Variabel|het bedrag op de dagboekregel wordt na het boeken verwijderd.|
|S Saldo|Het geboekte bedrag op de rekening op de regel wordt verdeeld over de rekeningen die zijn opgegeven voor de regel in de tabel Dagboekverdeelsleutel. Het saldo op de rekening wordt zo op nul ingesteld. Vul het veld **Verdeelsleutel %** op de pagina **Verdeelsleutels** in. Zie voor meer informatie [Periodieke dagboekbedragen toewijzen aan meerdere rekeningen](#allocating-recurring-journal-amounts-to-several-accounts).|
|OV Omgekeerd vast|Het bedrag wordt na het boeken bewaard en de tegenboeking wordt de volgende dag geboekt.|
|OR Omgekeerd vaRiabel|Het bedrag wordt na het boeken verwijderd en de tegenboeking wordt de volgende dag geboekt.|
|OS Omgekeerd saldo|Het geboekte bedrag op de rekening op de regel wordt verdeeld over de rekeningen die zijn opgegeven voor de regel op de pagina **Verdeelsleutels**. Het saldo op de rekening moet op nul zijn ingesteld en een tegenrekeningspost wordt de dag erop geboekt.|
|SD Saldo per dimensie|De dagboekregel wijst kosten toe op basis van het saldo van een grootboekrekening per dimensie. U wordt gevraagd de dimensiefilters in te stellen die moeten worden gebruikt om het saldo van de brongrootboekrekening te berekenen per dimensie waaruit u kosten wilt toewijzen. U kunt ook later de actie **Dimensiefilters instellen** kiezen.|
|OSD Omgekeerd saldo per dimensie|De dagboekregel wijst kosten toe op basis van het omgekeerd saldo van een grootboekrekening per dimensie. U wordt gevraagd de dimensiefilters in te stellen die moeten worden gebruikt om het saldo van de brongrootboekrekening te berekenen per dimensie waaruit u kosten wilt toewijzen. U kunt ook later de actie **Dimensiefilters instellen** kiezen.|

> [!NOTE]  
> De btw-velden kunnen worden ingevuld op de periodieke dagboekregel of op de verdelingsdagboekregel, maar niet op beide. De btw-velden kunt u alleen invullen op de pagina **Verdeelsleutels** als de overeenkomende regels in het periodieke dagboek niet zijn ingevuld.

### <a name="recurring-frequency-field"></a>Veld Frequentie
Dit veld bepaalt hoe vaak de dagboekregelpost moet worden geboekt. Dit is een datumformuleveld en het moet worden ingevuld voor periodieke dagboekregels. Zie voor meer informatie [Datumformules gebruiken](ui-enter-date-ranges.md#using-date-formulas).

#### <a name="examples"></a>Voorbeelden
Als de dagboekregel bijvoorbeeld elke maand moet worden geboekt, voert u "1M" in. Na elke boeking wordt de datum in het veld **Boekingsdatum** automatisch bijgewerkt met een maand.

Wanneer u een bepaalde post wilt boeken op de laatste dag van elke maand, kunt u dit op een van de volgende manieren doen:

- Boek de eerste post op de laatste dag van een maand door 1D+1M-1D (1 dag + 1 maand - 1 dag) in te vullen. Met deze formule wordt de boekingsdatum correct berekend, ongeacht het aantal dagen in de maand.

- Boek de eerste post op een willekeurige dag van een maand door 1M+LM in te voeren. Met deze formule ligt de boekingsdatum na een hele maand + de resterende dagen van de huidige maand.

### <a name="expiration-date-field"></a>Veld Vervaldatum
Dit veld is de datum waarop de regel voor het laatst wordt geboekt. De regel wordt niet geboekt na deze datum.

Voordeel van dit veld is dat de regel niet onmiddellijk uit het dagboek wordt verwijderd. Bovendien kunt u de vervaldatum altijd wijzigen, zodat u de regel opnieuw kunt gebruiken.

Als het veld leeg is, wordt de regel geboekt totdat deze uit het dagboek wordt verwijderd.

### <a name="allocating-recurring-journal-amounts-to-several-accounts"></a>Periodieke dagboekbedragen toewijzen aan meerdere rekeningen

Op de pagina **Periodiek dagboek** kunt u de actie **Verdeelsleutels** kiezen om te zien of beheren hoe bedragen op de periodieke dagboekregel worden verdeeld over verschillende rekeningen en dimensies. Een verdeelsleutel fungeert als tegenrekeningregel is voor de periodieke dagboekregel.

Net als in een periodiek dagboek hoeft u een toewijzing maar eenmaal in te voeren. De verdeelsleutel blijft na het boeken in het verdelingsdagboek, zodat u bedragen en toewijzingen niet telkens hoeft in te voeren wanneer u de periodieke dagboekregel boekt.

Als de *periodieke methode* in het periodieke dagboek is ingesteld op **Saldo** of **Omgekeerd saldo**, wordt geen rekening gehouden met dimensiewaardecodes in het periodieke dagboek als de rekening is ingesteld op nul. Dit betekent dat als u op de pagina **Verdeelsleutels** een periodieke regel verdeelt over verschillende dimensiewaarden, er slechts één tegenpost wordt gemaakt. Wanneer u een periodieke dagboekregel verdeelt die een dimensiewaardecode bevat, moet u dezelfde code daarom niet invoeren op de pagina **Verdeelsleutels**. Als u dat wel doet, zijn de dimensiewaarden onjuist.  

Om periodieke journaalbedragen toe te wijzen op basis van dimensies, stelt u in plaats daarvan het veld **Periodieke methode** in op **Saldo per dimensie** of **Omgekeerd saldo per dimensie**. Als de periodieke methode in het periodieke dagboek is ingesteld op **Saldo per dimensie** of **Omgekeerd saldo per dimensie**, wordt rekening gehouden met dimensiewaardecodes in het periodieke dagboek als de rekening is ingesteld op nul. Dus als u een terugkerende regel toewijst aan verschillende dimensiewaarden op de pagina **Toewijzingen**, dan wordt een aantal tegenboekingen gemaakt die overeenkomen met het aantal dimensiewaardecombinaties waaruit het saldo bestaat. Als u rekeningsaldo toewijst via het periodieke dagboek dat een dimensiewaardecode bevat, vergeet dan niet om **Saldo per dimensie** of **Omgekeerd saldo per dimensie** te gebruiken om ervoor te zorgen dat de dimensiewaarden correct in evenwicht zijn of worden omgekeerd ten opzichte van de bronaccount.  

Uw bedrijf heeft bijvoorbeeld een aantal bedrijfsunits en een handvol afdelingen die uw controllers als dimensies hebben ingesteld. Om het invoerproces van inkoopfacturen te versnellen besluit u dat de crediteurenadministratie alleen bedrijfsunitdimensies moet invoeren. Aangezien elke bedrijfsunit specifieke verdeelsleutels heeft voor de dimensie Afdeling, bijvoorbeeld op basis van het aantal werknemers, kunt u de periodieke methoden **Saldo per dimensie** of **Omgekeerd saldo per dimensie** gebruiken om kosten voor elke bedrijfsunit opnieuw toe te wijzen aan de juiste afdelingen op basis van de verdeelsleutels.  

> [!NOTE]
> Dimensies die u op verdeelsleutelregels instelt, worden niet automatisch berekend en u moet specificeren welke dimensiewaarden moeten worden ingesteld voor de verdelingsrekeningen. Als u de koppeling tussen de dimensie van de bronrekening en de dimensie van de verdelingsrekening wilt behouden, raden we u aan in plaats daarvan de mogelijkheden van [Kostprijsboekhouding](finance-about-cost-accounting.md) te gebruiken.

#### <a name="example-allocating-rent-payments-to-different-departments"></a>Voorbeeld: huurbetalingen aan verschillende kostenplaatsen toewijzen
U betaalt elke maand huur en u hebt het huurbedrag dus ingevoerd op de kasrekening op een periodieke dagboekregel. Op de pagina **Verdeelsleutels** kunt u de kosten verdelen over verschillende kostenplaatsen (dimensie Kostenplaats), afhankelijk van het aantal vierkante meter per kostenplaats. De berekening is gebaseerd op het verdelingspercentage op elke regel. U kunt verschillende rekeningen invoeren op verschillende verdelingsdagboekregels (als de huur ook wordt verdeeld over verschillende rekeningen). U kunt ook dezelfde rekening invoeren, maar op elke regel een andere dimensiewaardecode voor de dimensie Kostenplaats opgeven.

### <a name="reversal-date-calculation"></a>Berekening van tegenboekingsdatum
Wanneer u periodieke dagboeken gebruikt om transitoria aan het einde van een periode te boeken, is het belangrijk om volledige controle te hebben over tegenboekingsposten. Op de pagina **Periodieke dagboeken** kunt u met het veld **Berekening van tegenboekingsdatum** bepalen op welke datum tegenboekingsposten worden geboekt wanneer periodieke tegenboekingsmethoden worden gebruikt.

#### <a name="example"></a>Voorbeeld
Transitoria worden meestal geboekt met periodieke vaste, variabele of saldomethoden op de dagboekregel. De boekingsdatum van het geboekte bedrag op de rekening op de dagboekregel wordt berekend met de periodieke frequentie. De boekingsdatum voor de tegenboeking wordt als volgt berekend met behulp van het veld **Berekening van tegenboekingsdatum**:

* Als het veld leeg is, wordt de tegenboekingspost de volgende dag geboekt.
* Als het veld een datumformule bevat (bijvoorbeeld **5D** voor vijf dagen), wordt de tegenboekingspost geboekt met een boekingsdatum die wordt berekend op basis van de berekening van de tegenboekingsdatum.

> [!NOTE]
> Standaard is het veld **Berekening van tegenboekingsdatum** niet beschikbaar op de pagina **Periodieke dagboeken**. Om het veld te gebruiken moet u het toevoegen door de pagina te personaliseren. Zie [Uw werkruimte personaliseren](ui-personalization-user.md) voor meer informatie.

## <a name="working-with-standard-journals"></a>Werken met standaarddagboeken
Wanneer u artikeldagboekregels hebt gemaakt waarvan u weet dat u ze waarschijnlijk later opnieuw moet maken, kunt u ze als een standaarddagboek opslaan voordat u het artikeldagboek boekt. Deze functie geldt voor artikeldagboeken en diversendagboeken.

> [!NOTE]  
>   De volgende procedure heeft betrekking op het artikeldagboek, maar de informatie is ook van toepassing op het standaarddagboek.

### <a name="to-save-a-standard-journal"></a>Opslaan als standaarddagboek
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikeldagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Voer een of meer dagboekregels in.
3. Selecteer de dagboekregels die u opnieuw wilt gebruiken.
4. Kies de actie **Opslaan als standaarddagboek**.
5. Op de aanvraagpagina **Opslaan als standaardartikeldagboek** definieert u een nieuw of bestaand standaardartikeldagboek waarin de regels moeten worden opgeslagen.

    Als u al een of meer standaardartikeldagboeken hebt gemaakt en u een van deze dagboeken wilt vervangen door de nieuwe reeks artikeldagboekregels, selecteert u in het veld Code de desbetreffende code.
6. Klik op **OK** om het overschrijven van het bestaande standaardartikeldagboek en het vervangen van de volledige inhoud te bevestigen.
7. Selecteer het veld **Eenheidsprijs opslaan** als u de waarden in het veld **Eenheidsprijs** van het standaardartikeldagboek wilt opslaan.
8. Selecteer het veld **Aantal opslaan** als u wilt dat de toepassing de waarden in het veld **Aantal** opslaat.
9. Klik op **OK** om het standaardartikeldagboek op te slaan.

Wanneer u het standaardartikeldagboek hebt opgeslagen, wordt de pagina Artikeldagboek weergegeven zodat u het dagboek kunt boeken met in uw achterhoofd dat het dagboek eenvoudig opnieuw kan worden gemaakt als u later dezelfde of vergelijkbare regels opnieuw moet boeken.

### <a name="to-reuse-a-standard-journal"></a>Een standaarddagboek opnieuw gebruiken

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikeldagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Standaarddagboeken ophalen**.

    De pagina Standaardartikeldagboeken wordt weergegeven, met de codes en omschrijvingen van alle standaardartikeldagboeken.
3. Als u een standaardartikeldagboek wilt controleren voordat u het selecteert voor hergebruik, kiest u de actie **Dagboek tonen**.

    Wijzigingen die u in een standaardartikeldagboek maakt, worden meteen geïmplementeerd. De volgende keer dat u het standaardartikeldagboek opent of opnieuw gebruikt, zijn deze meteen zichtbaar. Daarom moet u ervoor zorgen dat de wijziging belangrijk genoeg is om algemeen toepassen. Breng de specifieke wijziging in het artikeldagboek anders pas aan nadat de standaardartikeldagboekregels zijn ingevoegd. Zie stap 4 hieronder.
4. Selecteer op de pagina **Standaardartikeldagboeken** het standaardartikeldagboek dat u opnieuw wilt gebruiken en kies vervolgens de knop **OK**.

    Het artikeldagboek wordt nu gevuld met de regels die u als het standaardartikeldagboek hebt opgeslagen. Als er al dagboekregels in het artikeldagboek voorkomen, worden de ingevoegde regels onder de bestaande dagboekregels geplaatst.

    Als u het veld **Eenheidsprijs opslaan** niet hebt ingeschakeld toen u de functietaak **Opslaan als standaardartikeldagboek** gebruikte, wordt het veld **Eenheidsprijs** op regels die zijn ingevoegd vanuit het standaarddagboek, automatisch gevuld met de huidige waarde van het artikel, gekopieerd van het veld **Kostprijs** op de artikelkaart.

    > [!NOTE]  
    > Als u de velden **Eenheidsprijs opslaan** of **Aantal opslaan** hebt geselecteerd, moet u controleren of de ingevoegde waarden voor deze bepaalde voorraadwijziging correct zijn voordat u het artikeldagboek boekt.

    Als de ingevoegde artikeldagboekregels opgeslagen eenheidsprijzen bevatten die u niet wilt boeken, kunt u deze als volgt snel wijzigen in de huidige waarde van het artikel.

5. Selecteer de dagboekregels die u wilt aanpassen en kies vervolgens de actie **Eenheidsprijs opnieuw berekenen**. Zo werkt u het veld Eenheidsprijs bij met de huidige kostprijs van het artikel.
6. Kies de actie **Boeken**.

## <a name="to-renumber-document-numbers-in-journals"></a>Documentnummers in dagboeken opnieuw nummeren

Om er zeker van te zijn dat u geen boekingsfouten ontvangt vanwege de numerieke documentvolgorde, kunt u de functie **Documentnummers opnieuw nummeren** gebruiken, voordat u een journaal boekt.

In alle dagboeken die zijn gebaseerd op het algemene dagboek, kan het veld **Documentnr.** worden bewerkt, zodat u voor verschillende dagboekregels verschillende documentnummers of hetzelfde documentnummer voor verwante dagboekregels kunt opgeven.

Als het veld **Nr.-reeksen** op de dagboekbatch is gevuld, vereist de boekingsfunctie in dagboeken dat de documentnummers op de afzonderlijke of gegroepeerde dagboekregels in sequentiële volgorde worden weergegeven. Kies gewoon de actie **Documentnummers hernummeren** en de relevante **Documentnr.**-velden worden dan bijgewerkt. Als verwante dagboekregels zijn gegroepeerd op documentnummer voordat u de functie gebruikte, blijven zij gegroepeerd maar wordt er mogelijk een ander documentnummer aan toegewezen.  

Deze functie werkt ook op de gefilterde weergaven.

Het wijzigen van documentnummers in verband met verwante vereffeningen, zoals een betalingsaanvraag die is ingediend vanuit het document op de dagboekregel naar een leveranciersrekening. Zo kunt u ook de velden **Vereffenings-id** en **Vereffeningsnr.** op de betrokken posten bijwerken.

### <a name="to-renumber-documents-in-journals"></a>Documentnummers in dagboeken opnieuw nummeren

De volgende procedure is gebaseerd op de pagina **Diversendagboek**, maar is van toepassing op alle overige journalen die u op het dagboek zijn gebaseerd, zoals de pagina **Betalingsdagboek**.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Financiële dagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Als u klaar bent om het dagboek te boeken, kiest u de actie **Documentnummers opnieuw nummeren**.

De waarden in het veld **Documentnr.** worden gewijzigd, wanneer dit is vereist, zodat het documentnummer op afzonderlijke of gegroepeerde dagboekregels in sequentiële volgorde wordt weergegeven. Nadat de documenten opnieuw zijn genummerd, kunt u doorgaan met het boeken van het dagboek.

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/paths/use-journals-dynamics-365-business-central/)

## <a name="see-also"></a>Zie ook

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