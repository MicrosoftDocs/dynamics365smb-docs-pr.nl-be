---
title: 'Artikelen traceren met serie-, partij- en pakketnummers'
description: 'U kunt serie-, lotnummers en pakketnummers toevoegen aan elk uitgaand of inkomend document en de bijbehorende geboekte artikeltraceringsposten worden in de artikelposten weergegeven.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.forms: '6503, 6515, 6513, 6512, 6502, 6506, 6501, 6510, 6507, 6500, 6505, 6508, 9126, 6526, 6516, 6511, 6504, 6509, 163, 6550,'
ms.date: 08/31/2021
ms.author: edupont
---
# <a name="track-items-with-serial-lot-and-package-numbers"></a><a name="track-items-with-serial-lot-and-package-numbers"></a>Artikelen traceren met serie-, partij- en pakketnummers

U kunt serie-, lotnummers en pakketnummers toewijzen aan elk uitgaand of inkomend document en de bijbehorende geboekte artikeltraceringsposten worden in de artikelposten weergegeven. U voert het werk uit op de pagina **Artikeltraceringsregels**, die u opent vanuit een inkomend of uitgaand document.

De matrix van aantalvelden bovenin de pagina **Artikeltraceringsregels** geeft de aantallen en totalen van artikeltraceringsnummers weer die op de regels worden gedefinieerd. De aantallen moeten overeenkomen met de waarden op de documentregel. **Niet gedefinieerde** velden hebben hierbij de waarde 0.

Ten behoeve van de prestaties wordt de beschikbare informatie op de pagina **Artikeltraceringsregels** slechts eenmaal verzameld wanneer u de pagina opent. Dat betekent dat de beschikbaarheidsgegevens niet worden bijgewerkt wanneer de pagina geopend is, zelfs niet wanneer gedurende die tijd wijzigingen optreden in de voorraad of in andere documenten.

> [!NOTE]  
>  Om de functies die in dit artikel worden beschreven te laten werken, moet u eerst artikeltracering instellen. Zie voor meer informatie [Artikeltracering instellen met serie, lot- en pakketnummers](inventory-how-setup-item-tracking.md).

## <a name="item-tracking-availability"></a><a name="item-tracking-availability"></a>Beschikbaarheid van artikeltracering

Wanneer u met serie-, lotnummers en pakketnummers werkt, berekent [!INCLUDE[prod_short](includes/prod_short.md)] beschikbaarheidsinformatie en geeft dit weer op de artikeltraceringspagina's. Zo kunt u zien hoeveel van een lot-, pakket- of serienummer op dit moment wordt gebruikt in andere documenten. Dit vermindert fouten en onzekerheid veroorzaakt door dubbele toewijzingen.

Op de pagina **Artikeltraceringsregels** wordt een waarschuwingspictogram weergegeven naast het veld **Beschikbaarheid lotnr.** of **Beschikbaarheid serienr.**, als enkele of alle van de geselecteerde aantallen al worden gebruikt in andere documenten of als het serie- of lotnummer niet beschikbaar is.

De pagina's **Lotnr./Serienr.-Overzicht** , **Lotnr./Serienr.-Beschikbaarheid** en **Artikeltracering - Posten selecteren** verschaffen informatie over het aantal dat van een artikel wordt gebruikt. U vindt hier onder andere de volgende informatie:

|Veld|Description|
|-----|-----------|  
|**Totaal aantal**|Het totale aantal artikelen dat momenteel in voorraad is.|
|**Totaal verzocht aantal**|Het totale aantal artikelen waarvoor een gebruiksverzoek is ingediend in dit document en in andere documenten.|
|**Huidig wachtend aantal**|Het aantal artikelen waarvoor een gebruiksverzoek voor het huidige document is ingediend, maar dat nog niet is vastgelegd in de database.|
|**Huidig aangevraagd aantal**|Het aantal artikelen waarvoor een gebruiksverzoek is ingediend in het huidige document.|
|**Totaal beschikbaar aantal**|Het totale aantal artikelen in voorraad zonder het aantal artikelen waarvoor een verzoek is ontvangen voor dit document of voor andere documenten (totaal verzocht aantal) en zonder het aantal dat is aangevraagd, maar nog niet is vastgelegd voor dit document (huidig wachtend aantal).|

Als u gedurende lange tijd op de pagina **Artikeltraceringsregels** werkt of als er veel activiteiten plaatsvinden voor het artikel waarmee u werkt, kunt u de actie **Beschikbaarheid vernieuwen** gebruiken. Daarnaast wordt de beschikbaarheid van het artikel automatisch opnieuw gecontroleerd als u de pagina sluit om te bevestigen dat er geen beschikbaarheidsproblemen zijn.

## <a name="to-assign-serial-or-lot-numbers-during-an-inbound-transaction"></a><a name="to-assign-serial-or-lot-numbers-during-an-inbound-transaction"></a>Serie- of lotnummers toewijzen tijdens inkomende transacties

Bedrijven willen artikelen mogelijk bijhouden vanaf het moment dat ze het bedrijf binnenkomen. In deze situatie is de inkooporder vaak het centrale document. Artikeltracering kan echter vanaf elk inkomend document worden verwerkt. De geboekte posten worden dan weergegeven in de bijbehorende artikelposten.

Op deze manier worden de nummers automatisch door alle uitgaande magazijnactiviteiten overgedragen zonder tussenkomst van magazijnmedewerkers.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkooporders** in en kies vervolgens de gerelateerde koppeling  
2. Open een bestaande inkooporder of maak een nieuwe.
3. Selecteer de relevante documentregel en kies vervolgens op het sneltabblad **Regels** de actie **Regel** en vervolgens de actie **Artikeltraceringsregels** om de pagina **Bewerken - Artikeltraceringsregels** te openen.  

    U kunt nu op een van de volgende manieren serie- of lotnummers toewijzen:  
    -   Automatisch, door **Verwerken** te selecteren, vervolgens **Serienr. toekennen** of **Lotnr. toekennen** te kiezen om serie- of lotnummers toe te kennen uit voorgedefinieerde nummerreeksen.  
    -   Automatisch, door **Verwerken** te selecteren en vervolgens **Aangepast serienr. maken** te kiezen om serie- of lotnummers toe te kennen die zijn gebaseerd op de nummerreeks die u specifiek voor de gearriveerde artikelen hebt gedefinieerd.  
    -   Handmatig, door rechtstreeks serie- of lotnummers in te voeren. U kunt bijvoorbeeld de nummers van de leverancier gebruiken.  
    -   Handmatig, door aan iedere artikeleenheid een specifiek nummer toe te kennen.  

4. Als u deze automatisch wilt laten toewijzen, kiest u de actie **Aangepast serienr. maken**.  
5. In het veld **Aangepast serienr.** voert u het beginnummer in van een omschrijvende serienummerreeks, bijvoorbeeld **S/N-Lev0001**.  
6. In het veld **Interval** typt u 1, om aan te geven dat de volgnummers steeds met één worden verhoogd.  

    Het veld **Te maken aantal** bevat standaard het regelaantal, maar u kunt dit wijzigen.  

7. Schakel het selectievakje **Nieuw lotnr. maken** in om de nieuwe serienummers te ordenen in een ander lot.  
7. Kies de knop **OK**.  

Er wordt een lotnummer aangemaakt met een reeks losse serienummers (gebaseerd op het totale aantal op de documentregel), te beginnen met **S/N-Lev0001**.  

De matrix van aantalvelden op de kop geeft een dynamische weergave van de aantallen en totalen van de artikeltraceringsnummers die u op de pagina definieert. De aantallen moeten overeenkomen met de waarden op de documentregel. **Niet gedefinieerde** velden hebben hierbij de waarde 0.  

Als het document wordt geboekt, worden de artikeltraceringsposten overgebracht naar de bijbehorende artikelposten.

### <a name="to-handle-serial-and-lot-numbers-when-getting-receipt-lines-from-a-purchase-invoice"></a><a name="to-handle-serial-and-lot-numbers-when-getting-receipt-lines-from-a-purchase-invoice"></a>Serie- en lotnummers verwerken bij het ophalen van ontvangstregels vanuit een inkoopfactuur

Wanneer u functionaliteit gebruikt om geboekte ontvangst- of verzendregels op te halen uit verwante facturen of creditnota's, worden alle artikeltraceringsregels op de magazijndocumenten automatisch overgebracht. Hierbij worden zij echter op een speciale manier verwerkt.

De functionaliteit ondersteunt de volgende inkomende processen:  
-   **Ontvangstregels ophalen**: van een inkoopfactuur.  
-   **Retourverzendregels ophalen**: van een inkoopcreditnota.  

De functionaliteit ondersteunt de volgende uitgaande processen:  
-   **Verzendregels ophalen**: van een verkoopfactuur of van verzamelfacturen.  
-   **Retourontvangstregels ophalen**: van een verkoopcreditnota.  

In deze gevallen worden de bestaande artikeltraceringsregels automatisch gekopieerd naar de factuur of creditnota. Op de pagina **Artikeltraceringsregels** worden echter geen wijzigingen toegestaan in de serie- of lotnummers. Alleen de hoeveelheden kunnen worden gewijzigd.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Inkoopfacturen** in en selecteer vervolgens de gerelateerde koppeling  
2. Open een inkoopfactuur voor artikelen die zijn aangekocht met serie- of lotnummers.  
3. Ga vanuit een inkoopfactuur naar het sneltabblad **Regels** en kies de actie **Ontvangstregels ophalen**.  
4. Selecteer op de pagina **Ontvangstregels ophalen** een ontvangstregel met artikeltraceringsregels en kies vervolgens de knop **OK**.  

    Het brondocument wordt als een nieuwe regel naar de inkoopfactuur gekopieerd en de bijbehorende artikeltraceringsregels worden overgenomen op de pagina **Artikeltraceringsregels**.  

5. Selecteer in de inkoopfactuur de overgebrachte ontvangstregel.  
6. Kies op het sneltabblad **Regels** de actie **Regel** en vervolgens de actie **Artikeltraceringsregels** om de overgenomen artikeltraceringsregels te bekijken.  

U kunt de velden **Serienummer** en **Lotnr.** niet bewerken. U kunt echter volledige regels verwijderen of de aantallen wijzigen, zodat deze overeenkomen met de wijzigingen op de bronregel.  

## <a name="to-assign-a-serial-or-lot-number-during-an-outbound-transaction"></a><a name="to-assign-a-serial-or-lot-number-during-an-outbound-transaction"></a>Serie- of lotnummers toewijzen tijdens een uitgaande transactie

Het verwerken van uitgaande serie- of lotnummers is een taak die vaak plaatsvindt tijdens vele verschillende magazijnprocessen. Er zijn twee manieren om serie- en lotnummers aan uitgaande transacties toe te voegen:  

-   Nummers selecteren uit bestaande serie- of lotnummers. Dit is van toepassing als er al traceringsnummers zijn toegekend tijdens een inkomende transactie.
-   Nieuwe serie- of lotnummers toewijzen tijdens uitgaande transacties. Dit is van toepassing wanneer artikeltraceringsnummers pas worden toegekend aan items op het moment dat ze worden verkocht en klaar zijn voor verzending.

### <a name="to-select-from-existing-serial-or-lot-numbers"></a><a name="to-select-from-existing-serial-or-lot-numbers"></a>U kunt als volgt nummers selecteren uit bestaande serie- of lotnummers

Wanneer u werkt met artikelen waarvoor artikeltracering is vereist en u uitgaande transacties maakt, d.w.z. transacties waarmee artikelen uit de voorraad worden gehaald, dient u meestal de lot- of serienummers te selecteren van artikelen die al in de voorraad staan.

1. Selecteer vanuit een uitgaand document de regel waarvoor u serie- of lotnummers wilt selecteren.  
2. Kies op het sneltabblad **Regels** de actie **Regel**, dan **Verwante gegevens** en selecteer vervolgens **Artikeltraceringsregels**.  
3. De pagina **Artikeltraceringsregels** beschikt over drie opties voor het opgeven van lot- of serienummers:  

    - Selecteer het veld **Serienr.** en vervolgens een nummer op de pagina **Serienr. - Lijst**.
    - Selecteer het veld **Lotnr.** en vervolgens een nummer op de pagina **Lotnr. - Lijst**. Selecteer vervolgens het veld **Serienr.** en vervolgens een nummer op de pagina **Serienr. - Lijst**.
    - Selecteer de actie **Verwerken** en kies dan **Posten selecteren**. De pagina **Posten selecteren** toont alle lot- en serienummers samen met beschikbaarheidsinformatie.

4. Voer in het veld **Geselecteerd aantal** de hoeveelheid van elk lot- of serienummer in dat u wilt gebruiken.
5. Kies de knop **OK** om de geselecteerde artikeltraceringsgegevens over te brengen naar de pagina **Artikeltraceringsregels**.  

De matrix van aantalvelden op de kop geeft een dynamische weergave van de aantallen en totalen van de artikeltraceringsnummers die u op de pagina definieert. De aantallen moeten overeenkomen met de waarden op de documentregel. **Niet gedefinieerde** velden hebben hierbij de waarde **0**.  

Als u de documentregel boekt, worden de artikeltraceringsposten overgebracht naar de bijbehorende artikelposten.

### <a name="to-assign-new-serial-or-lot-numbers"></a><a name="to-assign-new-serial-or-lot-numbers"></a>Nieuwe serie- of lotnummers toewijzen

Dit alternatief is van toepassing wanneer de voorraadartikelen geen serie- of lotnummers hebben en in plaats daarvan de artikeltraceringsnummers wanneer de artikelen worden verkocht en klaar zijn om te worden verzonden. In dit scenario worden de nummers meestal toegewezen vanuit een vooraf gedefinieerde nummerreeks.

1. Selecteer het relevante document, bijvoorbeeld een verkoopfactuur of verkooporder, en kies op het tabblad **Regels** de actie **Lijn**, dan **Verwante gegevens** en kies vervolgens de actie **Artikeltraceringsregels**.  

    U kunt op een van de volgende manieren artikeltraceringsnummers toewijzen:  
    -   Automatisch, uit voorgedefinieerde nummerreeksen: kies de actie **Serienr. toekennen** of **Lotnr. toekennen**.  
    -   Automatisch, op basis van parameters die u speciaal voor het uitgaande artikel definieert: kies de actie **Aangepast serienr. maken**.  
    -   Handmatig, door de serie- of lotnummers rechtstreeks in te voeren, zonder een nummerreeks te gebruiken.  

2. Voor deze procedure moet u automatisch een serienummer toekennen door te kiezen voor **Serienr. toekennen**  

    Het veld **Te maken aantal** bevat standaard het regelaantal, maar u kunt dit wijzigen.  
3. Schakel het selectievakje **Nieuw lotnr. maken** in om de nieuwe serienummers te ordenen in een ander lot.  
4. Kies de knop **OK** om een nieuw lotnummer en nieuwe reeks losse serienummers te maken op basis van het aantal te verwerken artikelen op de documentregel in kwestie.  

De matrix van aantalvelden bovenin geeft een dynamische weergave van de aantallen en totalen van de artikeltraceringsnummers die u op de pagina definieert. De aantallen moeten overeenkomen met de waarden op de documentregel. **Niet gedefinieerde** velden hebben hierbij de waarde **0**.  

Als het document wordt geboekt, worden de artikeltraceringsposten overgebracht naar de bijbehorende artikelposten.

### <a name="assign-tracking-numbers-on-source-documents"></a><a name="assign-tracking-numbers-on-source-documents"></a>Traceringsnummers toewijzen in brondocumenten

In speciale gevallen voor voorraad met een serie- of lotnummer, worden op het brondocument (zoals een verkooporder) specifieke serie- of lotnummers gedefinieerd die de magazijnmedewerker aan moet houden tijdens uitgaande magazijnverwerking. De reden kan zijn dat de klant tijdens het orderproces een specifieke partij heeft verzocht. Als het voorraad-pickdocument of magazijn-pickdocument gemaakt wordt vanuit een uitgaand brondocument, waarbij serie- of lotnummers voor artikelen al bepaald zijn, kan geen enkel veld op de pagina **Artikeltraceringsregels** onder de voorraadpick overschreven worden, behalve het veld **Te verwerken aantal**. In dat geval worden in de voorraadpickregels de artikeltraceringsnummers gespecificeerd op afzonderlijke Nemen- en Plaatsen-regels. Het aantal is reeds gesplitst in unieke serie- of lotnummercombinaties, omdat in de verkooporder wordt gespecificeerd dat de artikeltraceringsnummers worden verzonden.

## <a name="to-handle-serial-and-lot-numbers-on-transfer-orders"></a><a name="to-handle-serial-and-lot-numbers-on-transfer-orders"></a>Serie- en lotnummers verwerken op transferorders

De procedures voor het verwerken van serie- en lotnummers die tussen verschillende vestigingen worden verplaatst, zijn gelijk aan de procedures die worden toegepast bij de inkoop en verkoop van artikelen.  

De transferorder is echter uniek, omdat voor zowel verzending als ontvangst dezelfde transferregel wordt gebruikt, en dus dezelfde informatie op de pagina **Artikeltraceringsregels**. Dit betekent dat alle artikeltraceringsnummers die op de ene vestiging worden verzonden, ongewijzigd moeten worden ontvangen op de andere vestiging.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Transferorders** in en kies vervolgens de gerelateerde koppeling  
2. Open de transferorder die u wilt verwerken. Kies op het sneltabblad **Regels** de actie **Regel**, kies de actie **Artikeltraceringsregels** en vervolgens de actie **Verzending**.  
3. Voer de toewijzing of selectie van serie-/lotnummers op de pagina **Artikeltraceringsregels** op dezelfde wijze uit als bij andere uitgaande artikeltransacties.  

    Bij het verwerken van serie- en lotnummers voor transferartikelen hebben de artikelen meestal al een nummer. Daarom zult u normaal gesproken alleen nummers selecteren uit bestaande serie- of lotnummers.  

4. Boek de transferorder (eerst de verzending, daarna de ontvangst) om vast te leggen dat de artikelen zijn verplaatst met hun artikeltraceringsposten.  

Tijdens de transfer is de pagina **Artikeltraceringsregels** beveiligd tegen schrijven.  

## <a name="to-record-additional-serial-or-lot-number-information"></a><a name="to-record-additional-serial-or-lot-number-information"></a>Aanvullende gegevens over serie-/lotnummers vastleggen

Op een informatiekaart voor serie- of lotnummers kunt u gegevens koppelen aan een specifiek artikeltraceringsnummer (bijvoorbeeld voor kwaliteitscontrole).

1. Open een document waaraan veel serie- of lotnummers zijn toegewezen.
2. Open de pagina **Artikeltraceringsregels** voor het artikel waarvoor u informatie wilt invoeren.
3. Kies de actie **Regel** actie en dan bijvoorbeeld de actie **Serienr.-informatie**.  
4. Kies het plusteken **(+)** boven aan de lijst om een nieuw item aan te maken. De velden **Serienr.** en **Lotnr.** zijn al ingevuld op de artikeltraceringsregel.
5. Geef een kort stukje informatie in het veld **Omschrijving**, bijvoorbeeld over de staat van het artikel.  
6. Kies de actie **Verwant**, kies de actie **Serienr.**, en kies vervolgens de actie **Opmerking** om een afzonderlijke opmerkingsrecord te maken.  
7. Schakel het veld **Geblokkeerd** in om het serie- of lotnummer uit te sluiten van transacties.  

<!--If you create serial numbers in bulk by using the **Create Customized SN** or **Assign Serial No.** actions, you can enable **Create SN Information** and an information card will be created for each tracking line.

Alternatively, you can create an information card when you post journals or documents. On the **Item Tracking Code** page, turn on the **Create SN Info. on posting** or **Create SN Info. on posting** toggles. -->

U kunt aangemaakte serie- of partijinformatiekaarten later wijzigen.

## <a name="to-modify-existing-serial-or-lot-number-information"></a><a name="to-modify-existing-serial-or-lot-number-information"></a>Gegevens over bestaande serie- of lotnummers wijzigen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer een artikel met een artikeltraceringscode en met serie- of lotnummergegevens.
3. Kies op de pagina **Artikel** de actie **Posten** en kies daarna **Posten**.
4. Kies het veld **Lotnr.** of **Serienr.**. Als er informatie over dit artikeltraceringsnummer bestaat, wordt de pagina **Gegevensoverzicht lotnr.** of **Gegevensoverzicht serienr.** geopend.  
5. Selecteer een kaart en kies de actie **Lotnr.-informatie/Serienr.-informatie**.  
6. De korte omschrijving, de opmerkingrecord of het veld **Geblokkeerd** wijzigen.  

U kunt de serienummers of lotnummers of aantallen niet wijzigen. Hiervoor moet u de betreffende artikelpost herindelen. Raadpleeg voor meer informatie [Lot- of serienummers herindelen](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).

## <a name="to-reclassify-serial-or-lot-numbers"></a><a name="to-reclassify-serial-or-lot-numbers"></a>Serie- of lotnummers herindelen

Het herindelen van artikeltracering wil zeggen dat u een lot- of serienummer wijzigt in een nieuw nummer of de vervaldatum wijzigt in een nieuwe datum. Als u met lots werkt, is het ook mogelijk om meerdere lots samen te voegen tot één lot. U kunt deze taken uitvoeren met behulp van het artikelherindelingsdagboek.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Mag.-herindelingsdagboek** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de betreffende informatie in op de regel. Zie voor meer informatie [Voorraad tellen met documenten](inventory-how-count-inventory-with-documents.md) of [Voorraad tellen, corrigeren en herindelen met dagboeken](inventory-how-count-adjust-reclassify.md).
3. Kies de actie **Artikeltraceringsregels**.  
4. Selecteer in het veld **Serienummer** of **Lotnr.** het huidige serie- of lotnummer.  
5. Als u een nieuw artikeltraceringsnummer wilt opgeven, doet u dat in het veld **Nieuw serienr.** of **Nieuw lotnummer**. U kunt ook meerdere lots samenvoegen tot één nieuw of bestaand lot.  

    > [!NOTE]  
    >  Denk eraan dat wanneer u vervaldata opnieuw indeelt, vervolgens de items met de vroegste vervaldatum voor uitgaande transacties eerst worden voorgesteld. Zie voor meer informatie [Picken op basis van FEFO](warehouse-picking-by-fefo.md).  

6. Als u een nieuwe vervaldatum voor het serie- of lotnummer wilt invoeren, doet u dat in het veld **Nieuwe verloopdatum**.  

    > [!IMPORTANT]  
    >  Als u een lot herindeelt naar hetzelfde lotnummer, maar met een andere vervaldatum, moet u het volledige lot herindelen met gebruik van één regel in het artikelherindelingsdagboek. Als u meerdere lots herindeelt naar één nieuw lotnummer, dat wil zeggen als u meerdere lots samenvoegt tot één nieuw lot, dient u dezelfde nieuwe vervaldatum op te geven voor alle lots. Als u een bestaand lot herindeelt naar een tweede bestaand lot met een andere vervaldatum, moet u de vervaldatum van het tweede lot gebruiken. Als u het veld **Nieuwe verloopdatum** niet invult, wordt het lot- of serienummer heringedeeld met een lege vervaldatum.  

7. U kunt bestaande informatie over het oude serie- of lotnummer naar het nieuwe serie- of lotnummer kopiëren.  

    1. Kies op de pagina **Artikeltraceringsregels** de actie **Nieuwe serienummergegevens** of **Nieuwe lotnummergegevens**.  
    2. Als u informatie wilt kopiëren vanuit het oude lot- of serienummer, kiest u de actie **Gegevens kopiëren**.  
    3. Selecteer het lot- of serienummer waarvan u gegevens wilt kopiëren op de informatiepagina en klik op **OK**.  

8. Als u de bestaande gegevens voor het lot- of serienummer wilt wijzigen, kunt u informatie over lot- of serienummers vastleggen.  
9. Boek het dagboek om de vernieuwde artikeltraceringsnummers of vervaldatums te koppelen aan de bijbehorende artikelpost.

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/modules/prepare-item-tracking/)

## <a name="see-also"></a><a name="see-also"></a>Zie ook

[Artikeltracering instellen met serie-, partij- en pakketnummers](inventory-how-setup-item-tracking.md)  
[Artikelen met artikeltracering traceren](inventory-how-to-trace-item-tracked-items.md)  
[Voorraad](inventory-manage-inventory.md)  
[Ontwerpdetails: Artikeltracering](design-details-item-tracking.md)  
[Ontwerpdetails: Artikeltracering en reserveringen](design-details-item-tracking-and-reservations.md)  
[Artikelen reserveren](inventory-how-to-reserve-items.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
