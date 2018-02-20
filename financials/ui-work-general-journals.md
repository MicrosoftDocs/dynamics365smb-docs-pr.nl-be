---
title: Dagboeken gebruiken om direct naar grootboek te boeken| Microsoft Docs
description: "Leren over het gebruik van diversendagboeken om financiële transacties naar grootboekrekeningen en andere rekeningen te boeken, zoals bank-, klant- en leveranciersrekeningen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 07/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 2aac957fc253f6c7d2f621ea2e5e039733081a19
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---
# <a name="working-with-general-journals"></a>Werken met diversendagboeken
De meeste financiële transacties worden geboekt naar het grootboek door bepaalde bedrijfsdocumenten, zoals inkoopfacturen en verkooporders. Voor zakelijke activiteiten die niet door een document worden vertegenwoordigd in [!INCLUDE[d365fin](includes/d365fin_md.md)], zoals kleinere ontvangsten of kasontvangsten, kunt u de gerelateerde transacties maken door dagboekregels te boeken in het venster **Diversendagboek**. Zie voor meer informatie [Transacties direct naar het grootboek boeken](finance-how-post-transactions-directly.md).

U kunt bijvoorbeeld de uitgaven boeken die werknemers uit eigen portemonnee doen, zodat u hen later kunt terugbetalen. Zie voor meer informatie [Uitgaven van werknemers vastleggen en terugbetalen](finance-how-record-reimburse-employee-expenses.md).

Met diversendagboeken kunt u financiële transacties direct naar grootboekrekeningen en andere rekeningen boeken, zoals bank-, klant-, leveranciers- en werknemersrekeningen. Door te boeken met een dagboek worden er altijd posten gemaakt in grootboekrekeningen. Dit geldt zelfs ook als u bijvoorbeeld een dagboekregel naar een klantrekening boekt, omdat een post via een boekingsgroep is geboekt naar een rekening met vorderingen in het grootboek.

De informatie die u invoert in een dagboek is tijdelijk en kan in het dagboek worden gewijzigd. Wanneer u het dagboek boekt, wordt de informatie overgedragen naar de posten van afzonderlijke rekeningen, waar de informatie niet meer kan worden gewijzigd. U kunt echter de vereffening van geboekte posten ongedaan maken en u kunt tegenboekingen of corrigerende boekingen maken. Zie voor meer informatie [Boekingen tegenboeken](finance-how-reverse-journal-posting.md).

## <a name="using-journal-templates-and-batches"></a>Dagboeksjablonen en -batches gebruiken
Er zijn verschillende sjablonen voor diversendagboeken. Elk dagboeksjabloon wordt vertegenwoordigd door een speciaal venster met specifieke functies en de velden die nodig zijn om die functies te ondersteunen, zoals het venster **Dagboek betalingsreconciliatie**, om bankbetalingen te verwerken en het venster **Betalingsdagboek** om uw leveranciers te betalen en kosten van uw werknemers te vergoeden. Zie voor meer informatie [Betalingen doen](payables-make-payments.md) en [Klantbetalingen handmatig reconciliëren](receivables-how-apply-sales-transactions-manually.md).

Voor elke dagboeksjabloon kunt u uw eigen persoonlijke dagboek instellen als een dagboekbatch. U kunt bijvoorbeeld uw eigen dagboekbatch definiëren voor het betalingsdagboek dat uw persoonlijke lay-out en instellingen heeft. De volgende tip is een voorbeeld van hoe u een dagboek aanpast.

> [!TIP]  
> Als u het selectievakje **Salderingsbedrag voorstellen** inschakelt op de regel voor uw batch in het venster **Fin. dagboekbatches**, wordt het veld **Bedrag** op bijvoorbeeld diversendagboekregels voor hetzelfde documentnummer automatisch vooraf ingevuld met de waarde die is vereist om het document sluitend te maken. Zie voor meer informatie [[!INCLUDE[d365fin](includes/d365fin_md.md)] waarden laten voorstellen](ui-let-system-suggest-values.md).

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Hoofdrekeningen en tegenrekeningen
Als u op de pagina **Dagboeken** standaardtegenrekeningen hebt ingesteld voor de dagboekbatches, wordt de tegenrekening automatisch ingevuld wanneer u het veld **Rekeningnr.** invult. Anders vult u zowel het veld **Rekeningnr.** als het veld **Tegenrekeningnr.** handmatig in. Een positief bedrag in het veld **Bedrag** wordt gedebiteerd van de hoofdrekening en gecrediteerd naar de tegenrekening. Een negatief bedrag wordt gecrediteerd naar de hoofdrekening en gedebiteerd van de tegenrekening.

> [!NOTE]  
>   Btw wordt afzonderlijk berekend voor de hoofdrekening en de tegenrekening, zodat er gebruik kan worden gemaakt van verschillende percentages.

## <a name="working-with-recurring-journals"></a>Werken met periodieke dagboeken
Een periodiek dagboek is een dagboek met specifieke velden voor het beheer van transacties die u regelmatig boekt met weinig of geen wijzigingen. Met de speciale velden voor periodieke transacties kunt u zowel vaste als variabele bedragen boeken. U kunt ook automatische tegenboekingsposten specificeren op de dag na de boekingsdatum en toewijzingssleutels gebruiken voor de periodieke transacties.

## <a name="working-with-standard-journals"></a>Werken met standaarddagboeken
Wanneer u artikeldagboekregels hebt gemaakt waarvan u weet dat u ze waarschijnlijk later opnieuw moet maken, kunt u ze als een standaarddagboek opslaan voordat u het artikeldagboek boekt. Deze functie geldt voor artikeldagboeken en diversendagboeken.

> [!NOTE]  
>   De volgende procedure heeft betrekking op het artikeldagboek, maar de informatie is ook van toepassing op het standaarddagboek.

### <a name="to-save-a-standard-journal"></a>Opslaan als standaarddagboek
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Artikeldagboeken** in en klik vervolgens op de gerelateerde koppeling.
2. Voer een of meer dagboekregels in.
3. Selecteer de dagboekregels die u opnieuw wilt gebruiken.
4. Kies de actie **Opslaan als standaarddagboek**.
5. In het aanvraagvenster **Opslaan als standaardartikeldagboek** definieert u een nieuw of bestaand standaardartikeldagboek waarin de regels moeten worden opgeslagen.

    Als u al een of meer standaardartikeldagboeken hebt gemaakt en u een van deze dagboeken wilt vervangen door de nieuwe reeks artikeldagboekregels, selecteert u in het veld Code de desbetreffende code.
6. Klik op **OK** om het overschrijven van het bestaande standaardartikeldagboek en het vervangen van de volledige inhoud te bevestigen.
7. Selecteer het veld **Eenheidsprijs opslaan** als u de waarden in het veld **Eenheidsprijs** van het standaardartikeldagboek wilt opslaan.
8. Selecteer het veld **Aantal opslaan** als u wilt dat het programma de waarden in het veld **Aantal** opslaat.
9. Klik op **OK** om het standaardartikeldagboek op te slaan.

Wanneer u het standaardartikeldagboek hebt opgeslagen, wordt het venster Artikeldagboek weergegeven zodat u het dagboek kunt boeken met in uw achterhoofd dat het dagboek eenvoudig opnieuw kan worden gemaakt als u later dezelfde of vergelijkbare regels opnieuw moet boeken.

### <a name="to-reuse-a-standard-journal"></a>Een standaarddagboek opnieuw gebruiken
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Artikeldagboeken** in en klik vervolgens op de gerelateerde koppeling.
2. Kies de actie **Standaarddagboeken ophalen**.

    Het venster Standaardartikeldagboeken wordt weergegeven, met de codes en omschrijvingen van alle standaardartikeldagboeken.
3. Als u een standaardartikeldagboek wilt controleren voordat u het selecteert voor hergebruik, kiest u de actie **Dagboek tonen**.

    Wijzigingen die u in een standaardartikeldagboek maakt, worden meteen geïmplementeerd. De volgende keer dat u het standaardartikeldagboek opent of opnieuw gebruikt, zijn deze meteen zichtbaar. Daarom moet u ervoor zorgen dat de wijziging belangrijk genoeg is om algemeen toepassen. Breng de specifieke wijziging in het artikeldagboek anders pas aan nadat de standaardartikeldagboekregels zijn ingevoegd. Zie stap 4 hieronder.
4. Selecteer in het venster **Standaardartikeldagboeken** het standaardartikeldagboek dat u opnieuw wilt gebruiken en kies vervolgens de knop **OK**.

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

De volgende procedure is gebaseerd op het venster **Diversendagboek**, maar is van toepassing op alle overige journalen die u op het dagboek zijn gebaseerd, zoals het venster **Betalingsdagboek**.

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Dagboeken** in en klik vervolgens op de gerelateerde koppeling.
2. Als u klaar bent om het dagboek te boeken, kiest u de actie **Documentnummers opnieuw nummeren**.

De waarden in het veld **Documentnr.** worden gewijzigd, wanneer dit is vereist, zodat het documentnummer op afzonderlijke of gegroepeerde dagboekregels in sequentiële volgorde wordt weergegeven. Nadat de documenten opnieuw zijn genummerd, kunt u doorgaan met het boeken van het dagboek.

## <a name="see-also"></a>Zie ook
[Transacties direct naar het grootboek boeken](finance-how-post-transactions-directly.md)  
[Boekingen tegenboeken](finance-how-reverse-journal-posting.md)  
[Kosten en inkomsten toewijzen](year-allocate-costs-income.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

