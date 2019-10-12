---
title: Dagboeken gebruiken om direct naar grootboek te boeken| Microsoft Docs
description: Leren over het gebruik van dagboeken om financiële transacties naar grootboekrekeningen en andere rekeningen te boeken, zoals bank-, klant- en leveranciersrekeningen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 635e53040ab9920780cd1cf05a14f6dfa17496d9
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2314976"
---
# <a name="working-with-general-journals"></a>Werken met diversendagboeken

De meeste financiële transacties worden geboekt naar het grootboek door bepaalde bedrijfsdocumenten, zoals inkoopfacturen en verkooporders. Maar u kunt ook zakelijke activiteiten zoals inkoopprocessen, betaling of terugbetaling van werknemersonkosten verwerken door dagboekregels te boeken in de verschillende dagboeken in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

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
> Als u het selectievakje **Salderingsbedrag voorstellen** inschakelt op de regel voor uw batch op de pagina **Fin. dagboekbatches**, wordt het veld **Bedrag** op bijvoorbeeld diversendagboekregels voor hetzelfde documentnummer automatisch vooraf ingevuld met de waarde die is vereist om het document sluitend te maken. Zie voor meer informatie [[!INCLUDE[d365fin](includes/d365fin_md.md)] waarden laten voorstellen](ui-let-system-suggest-values.md).

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Hoofdrekeningen en tegenrekeningen
Als u op de pagina **Dagboeken** standaardtegenrekeningen hebt ingesteld voor de dagboekbatches, wordt de tegenrekening automatisch ingevuld wanneer u het veld **Rekeningnr.** invult. Anders vult u zowel het veld **Rekeningnr.** als het veld **Tegenrekeningnr.** handmatig in. Een positief bedrag in het veld **Bedrag** wordt gedebiteerd van de hoofdrekening en gecrediteerd naar de tegenrekening. Een negatief bedrag wordt gecrediteerd naar de hoofdrekening en gedebiteerd van de tegenrekening.

> [!NOTE]  
>   Btw wordt afzonderlijk berekend voor de hoofdrekening en de tegenrekening, zodat er gebruik kan worden gemaakt van verschillende percentages.

## <a name="working-with-recurring-journals"></a>Werken met periodieke dagboeken
Een periodiek dagboek is een dagboek met specifieke velden voor het beheer van transacties die u regelmatig boekt met weinig of geen wijzigingen, zoals huur, abonnementen en elektriciteit. Met de speciale velden voor periodieke transacties kunt u zowel vaste als variabele bedragen boeken. U kunt ook automatische tegenboekingposten voor de dag na de boekingsdatum opgeven. U kunt ook verdeelsleutels gebruiken om de periodieke posten over verschillende rekeningen te verdelen. Zie voor meer informatie [Periodieke dagboekbedragen toewijzen aan meerdere rekeningen](ui-work-general-journals.md#allocating-recurring-journal-amounts-to-several-accounts).

Als u een periodiek dagboek gebruikt, hoeft u de gegevens slechts éénmaal in te voeren. De ingevulde gegevens, zoals rekeningen, dimensies en dimensiewaarden, worden na het boeken in het dagboek bewaard. Later kunt u eventueel wijzigingen aanbrengen en de informatie opnieuw boeken.

### <a name="recurring-method-field"></a>Veld Methode
Dit veld bepaalt hoe het bedrag op de dagboekregel na het boeken wordt verwerkt. Wanneer u de regel bijvoorbeeld altijd met hetzelfde bedrag wilt boeken, kunt u het bedrag ongewijzigd laten. Wilt u dezelfde rekeningen en dezelfde tekst gebruiken, maar een ander bedrag, dan kunt u het bedrag na het boeken verwijderen.

| Aan | Zie |
| --- | --- |
|Vast|het bedrag op de dagboekregel wordt na het boeken bewaard.|
|Variabel|het bedrag op de dagboekregel wordt na het boeken verwijderd.|
|Saldo|Het geboekte bedrag op de rekening op de regel wordt verdeeld over de rekeningen die zijn opgegeven voor de regel in de tabel Dagboekverdeelsleutel. Het saldo op de rekening wordt zo op nul ingesteld. Vul het veld **Verdeelsleutel %** op de pagina **Verdeelsleutels** in. Zie voor meer informatie [Periodieke dagboekbedragen toewijzen aan meerdere rekeningen](ui-work-general-journals.md#allocating-recurring-journal-amounts-to-several-accounts).|
|Omgekeerd vast|Het bedrag wordt na het boeken bewaard en de tegenboeking wordt de volgende dag geboekt.|
|Omgekeerd variabel|Het bedrag wordt na het boeken verwijderd en de tegenboeking wordt de volgende dag geboekt.|
|Omgekeerd saldo|Het geboekte bedrag op de rekening op de regel wordt verdeeld over de rekeningen die zijn opgegeven voor de regel op de pagina **Verdeelsleutels**. Het saldo op de rekening moet op nul zijn ingesteld en een tegenrekeningspost wordt de dag erop geboekt.|

> [!NOTE]  
>  De btw-velden kunnen worden ingevuld op de periodieke dagboekregel of op de verdelingsdagboekregel, maar niet op beide. De btw-velden kunt u alleen invullen op de pagina **Verdeelsleutels** als de overeenkomende regels in het periodieke dagboek niet zijn ingevuld.

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

Als de periodieke methode in het periodieke dagboek is ingesteld op **Saldo** of **Omgekeerd saldo**, wordt geen rekening gehouden met dimensiewaardecodes in het periodieke dagboek als de rekening is ingesteld op nul. Dit betekent dat als u op de pagina **Verdeelsleutels** een periodieke regel verdeelt over verschillende dimensiewaarden, er slechts één tegenpost wordt gemaakt. Wanneer u een periodieke dagboekregel verdeelt die een dimensiewaardecode bevat, moet u dezelfde code daarom niet invoeren op de pagina **Verdeelsleutels**. Als u dat wel doet, zijn de dimensiewaarden onjuist.

#### <a name="example-allocating-rent-payments-to-different-departments"></a>Voorbeeld: huurbetalingen aan verschillende kostenplaatsen toewijzen
U betaalt elke maand huur en u hebt het huurbedrag dus ingevoerd op de kasrekening op een periodieke dagboekregel. Op de pagina **Verdeelsleutels** kunt u de kosten verdelen over verschillende kostenplaatsen (dimensie Kostenplaats), afhankelijk van het aantal vierkante meter per kostenplaats. De berekening is gebaseerd op het verdelingspercentage op elke regel. U kunt verschillende rekeningen invoeren op verschillende verdelingsdagboekregels (als de huur ook wordt verdeeld over verschillende rekeningen). U kunt ook dezelfde rekening invoeren, maar op elke regel een andere dimensiewaardecode voor de dimensie Kostenplaats opgeven.

## <a name="working-with-standard-journals"></a>Werken met standaarddagboeken
Wanneer u artikeldagboekregels hebt gemaakt waarvan u weet dat u ze waarschijnlijk later opnieuw moet maken, kunt u ze als een standaarddagboek opslaan voordat u het artikeldagboek boekt. Deze functie geldt voor artikeldagboeken en diversendagboeken.

> [!NOTE]  
>   De volgende procedure heeft betrekking op het artikeldagboek, maar de informatie is ook van toepassing op het standaarddagboek.

### <a name="to-save-a-standard-journal"></a>Opslaan als standaarddagboek
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikeldagboeken** in en kies vervolgens de gerelateerde koppeling.
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
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikeldagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Standaarddagboeken ophalen**.

    De pagina Standaardartikeldagboeken wordt weergegeven, met de codes en omschrijvingen van alle standaardartikeldagboeken.
3. Als u een standaardartikeldagboek wilt controleren voordat u het selecteert voor hergebruik, kiest u de actie **Dagboek tonen**.

    Wijzigingen die u in een standaardartikeldagboek maakt, worden meteen geïmplementeerd. De volgende keer dat u het standaardartikeldagboek opent of opnieuw gebruikt, zijn deze meteen zichtbaar. Daarom moet u ervoor zorgen dat de wijziging belangrijk genoeg is om algemeen toepassen. Breng de specifieke wijziging in het artikeldagboek anders pas aan nadat de standaardartikeldagboekregels zijn ingevoegd. Zie stap 4 hieronder.
4. Selecteer op de pagina **Standaardartikeldagboeken** het standaardartikeldagboek dat u opnieuw wilt gebruiken en kies vervolgens de knop **OK**.

    Het artikeldagboek wordt nu gevuld met de regels die u als het standaardartikeldagboek hebt opgeslagen. Als er al dagboekregels in het artikeldagboek voorkomen, worden de ingevoegde regels onder de bestaande dagboekregels geplaatst.

    Als u het veld **Eenheidsprijs opslaan** niet hebt ingeschakeld toen u de functietaak **Opslaan als standaardartikeldagboek** gebruikte, wordt het veld **Eenheidsprijs** op regels die zijn ingevoegd vanaf het standaarddagboek, automatisch gevuld met de huidige waarde van het artikel, gekopieerd van het veld **Kostprijs** op de artikelkaart.

    > [!NOTE]  
    >   Als u de velden **Eenheidsprijs opslaan** of **Aantal opslaan** hebt geselecteerd, moet u controleren of de ingevoegde waarden voor deze bepaalde voorraadwijziging correct zijn voordat u het artikeldagboek boekt.

    Als de ingevoegde artikeldagboekregels opgeslagen eenheidsprijzen bevatten die u niet wilt boeken, kunt u deze als volgt snel wijzigen in de huidige waarde van het artikel.

6. Selecteer de dagboekregels die u wilt aanpassen en kies vervolgens de actie **Eenheidsprijs opnieuw berekenen**. Zo werkt u het veld Eenheidsprijs bij met de huidige kostprijs van het artikel.
7. Kies de actie **Boeken**.

## <a name="to-renumber-document-numbers-in-journals"></a>Documentnummers in dagboeken opnieuw nummeren
Om er zeker van te zijn dat u geen boekingsfouten ontvangt vanwege de numerieke documentvolgorde, kunt u de functie **Documentnummers opnieuw nummeren** gebruiken, voordat u een journaal boekt.

In alle dagboeken die zijn gebaseerd op het algemene dagboek, kan het veld **Documentnr.** worden bewerkt, zodat u voor verschillende dagboekregels verschillende documentnummers of hetzelfde documentnummer voor verwante dagboekregels kunt opgeven.

Als het veld **Nr.-reeksen** op de dagboekbatch is gevuld, vereist de boekingsfunctie in dagboeken dat de documentnummers op de afzonderlijke of gegroepeerde dagboekregels in sequentiële volgorde worden weergegeven. Om er zeker van te zijn dat u geen boekingsfouten ontvangt vanwege de numerieke documentvolgorde, kunt u de functie **Documentnummers opnieuw nummeren** gebruiken, voordat u het dagboek boekt. Als verwante dagboekregels zijn gegroepeerd op documentnummer voordat u de functie gebruikte, blijven zij gegroepeerd maar wordt er mogelijk een ander documentnummer aan toegewezen.

Deze functie werkt ook op de gefilterde weergaven.

Het wijzigen van documentnummers in verband met verwante vereffeningen, zoals een betalingsaanvraag die is ingediend vanuit het document op de dagboekregel naar een leveranciersrekening. Zo kunt u ook de velden **Vereffenings-id** en **Vereffeningsnr.** op de betrokken posten bijwerken.

De volgende procedure is gebaseerd op de pagina **Diversendagboek**, maar is van toepassing op alle overige journalen die u op het dagboek zijn gebaseerd, zoals de pagina **Betalingsdagboek**.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Financiële dagboeken** in en kies vervolgens de gerelateerde koppeling.
2. Als u klaar bent om het dagboek te boeken, kiest u de actie **Documentnummers opnieuw nummeren**.

De waarden in het veld **Documentnr.** worden gewijzigd, wanneer dit is vereist, zodat het documentnummer op afzonderlijke of gegroepeerde dagboekregels in sequentiële volgorde wordt weergegeven. Nadat de documenten opnieuw zijn genummerd, kunt u doorgaan met het boeken van het dagboek.

## <a name="see-also"></a>Zie ook
[Transacties direct naar het grootboek boeken](finance-how-post-transactions-directly.md)  
[Journaalboekingen tegenboeken en ontvangsten/zendingen ongedaan maken](finance-how-reverse-journal-posting.md)  
[Kosten en inkomsten toewijzen](year-allocate-costs-income.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
