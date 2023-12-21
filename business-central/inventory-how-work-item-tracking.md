---
title: 'Artikelen traceren met serie-, partij- en pakketnummers'
description: 'U kunt serie-, lotnummers en pakketnummers toevoegen aan elk uitgaand of inkomend document en de bijbehorende geboekte artikeltraceringsposten worden in de artikelposten weergegeven.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.search.forms: '6503, 6515, 6513, 6512, 6502, 6506, 6501, 6510, 6507, 6500, 6505, 6508, 9126, 6526, 6516, 6511, 6504, 6509, 163, 6550,'
ms.date: 12/19/2023
ms.custom: bap-template
---
# <a name="track-items-with-serial-lot-and-package-numbers"></a>Artikelen traceren met serie-, partij- en pakketnummers

U kunt serie-, lotnummers en pakketnummers toewijzen aan elk uitgaand of inkomend document en de bijbehorende geboekte artikeltraceringsposten worden in de artikelposten weergegeven. U traceert artikelen op de pagina **Artikeltraceringsregels**, die u opent vanuit inkomende of uitgaande documenten.

De hoeveelheidsvelden boven aan de pagina **Artikeltraceringsregels** geven de aantallen en totalen van artikeltraceringsnummers weer die op de regels worden gedefinieerd. De hoeveelheden moeten overeenkomen met die op de documentregel. **Niet gedefinieerde** velden hebben hierbij de waarde 0.

[!INCLUDE [prod_short](includes/prod_short.md)] werkt de beschikbaarheidsinformatie op de pagina **Artikeltraceringsregels** bij wanneer u de pagina opent. De informatie wordt niet bijgewerkt terwijl u de pagina geopend heeft, zelfs niet als er gedurende die tijd wijzigingen optreden in de voorraad of in andere documenten.

> [!NOTE]  
> Om de functies die in dit artikel worden beschreven te laten werken, moet u artikeltracering instellen. Ga voor meer informatie naar [Artikeltracering instellen met serie, lot- en pakketnummers](inventory-how-setup-item-tracking.md).

## <a name="item-tracking-availability"></a>Beschikbaarheid van artikeltracering

Wanneer u met serie-, lotnummers en pakketnummers werkt, berekent [!INCLUDE[prod_short](includes/prod_short.md)] beschikbaarheidsinformatie en geeft dit weer op de artikeltraceringspagina's. Het laat zien hoeveel van een lot-, pakket- of serienummer op andere documenten wordt gebruikt. Deze informatie vermindert fouten en onzekerheid veroorzaakt door dubbele toewijzingen.

Op de pagina **Artikeltraceringsregels** wordt mogelijk een waarschuwingspictogram weergegeven in het veld **Beschikbaarheid, Lotnr.** of **Beschikbaarheid, Serienr.** om de volgende redenen:

* Als een deel of het geheel van de door u geselecteerde hoeveelheid al in andere documenten wordt gebruikt.
* Als het lot- of serienummer niet beschikbaar is.

Op de pagina's **Lotnr./Serienr.-Overzicht**, **Lotnr./Serienr.-Overzicht** en **Artikeltracering - Posten selecteren** wordt de hoeveelheid van een artikel weergegeven die in gebruik is. De volgende tabel bevat de relevante velden.

|Veld|Omschrijving|
|-----|-----------|  
|**Totale hoeveelheid**|het totale aantal van een artikel dat momenteel in voorraad is.|
|**Totaal verzocht aantal**|het totale aantal artikelen waarom wordt verzocht in dit document en in andere documenten.|
|**Huidig wachtend aantal**|Het aantal artikelen waarom wordt verzocht in het huidige document, maar dat niet is geboekt.|
|**Huidig aangevraagd aantal**|Het aantal artikelen waarvoor een gebruiksverzoek is ingediend in het huidige document.|
|**Totaal beschikbaar aantal**|Het totale aantal artikelen in voorraad minus de hoeveelheid artikelen waarvoor een verzoek is ontvangen voor dit document of voor andere documenten (totaal verzochte hoeveelheid) en minus het aantal waarom is verzocht, maar dat nog niet is geboekt voor dit document (huidige wachtende hoeveelheid).|

Als u gedurende lange tijd op de pagina **Artikeltraceringsregels** werkt of als er veel activiteit plaatsvindt voor het artikel waarmee u werkt, kunt u de actie **Beschikbaarheid vernieuwen** gebruiken. De beschikbaarheid van het artikel wordt ook automatisch opnieuw gecontroleerd als u de pagina sluit om te bevestigen dat er geen beschikbaarheidsproblemen zijn.

## <a name="to-assign-serial-or-lot-numbers-during-an-inbound-transaction"></a>Serie- of lotnummers toewijzen tijdens inkomende transacties

Misschien wilt u artikelen traceren vanaf het moment dat ze arriveren. Vaak is de inkooporder dan het centrale document. U kunt echter artikeltracering uitvoeren vanuit elk inkomend document en de bijbehorende geboekte posten worden weergegeven in de gerelateerde artikelposten

De traceringsnummers worden automatisch overgedragen naar alle uitgaande magazijnactiviteiten.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkooporders** in en kies vervolgens de gerelateerde koppeling  
2. Open een bestaande inkooporder of maak een nieuwe.
3. Selecteer de documentregel en kies vervolgens op het sneltabblad **Regels** de actie **Regel** en vervolgens de actie **Artikeltraceringsregels** om de pagina **Bewerken - Artikeltraceringsregels** te openen.  

   U kunt nu op een van de volgende manieren serie- of lotnummers toewijzen:  
   - Automatisch, door **Verwerken** te selecteren, vervolgens **Serienr. toekennen** of **Lotnr. toekennen** te kiezen om serie- of lotnummers toe te kennen uit voorgedefinieerde nummerreeksen.  
   - Automatisch, door **Verwerken** te selecteren en vervolgens **Aangepast serienr. maken** te kiezen om serie- of lotnummers toe te kennen die zijn gebaseerd op de nummerreeks die u specifiek voor de gearriveerde artikelen hebt gedefinieerd.  
   - Handmatig, door rechtstreeks serie- of lotnummers in te voeren. U kunt bijvoorbeeld de nummers van de leverancier gebruiken.  
   - Handmatig, door aan iedere artikeleenheid een specifiek nummer toe te kennen.  

4. Als u deze automatisch wilt laten toewijzen, kiest u de actie **Aangepast serienr. maken**.  
5. In het veld **Aangepast serienr.** voert u het beginnummer in van een omschrijvende serienummerreeks. Bijvoorbeeld **S/N-Vend0001**.  
6. In het veld **Interval** typt u 1, om aan te geven dat de volgnummers steeds met één worden verhoogd.  

    Het veld **Te maken aantal** bevat standaard het regelaantal, maar u kunt dit wijzigen.  

7. Schakel het selectievakje **Nieuw lotnr. maken** in om de nieuwe serienummers te ordenen in een andere lot.  
7. Kies de knop **Ok**.  

[!INCLUDE [prod_short](includes/prod_short.md)] maakt een lotnummer met een reeks losse serienummers gebaseerd op de artikelhoeveelheid op de documentregel. Het nummer wordt voorafgegaan door de waarde die u heeft ingevoerd in het veld **Aangepast serienr.** Bijvoorbeeld vanaf **S/N-Vend0001**.  

De hoeveelheidsvelden in de kop geven een dynamische weergave van de hoeveelheden en totalen van de artikeltraceringsnummers die u op de pagina definieert. De hoeveelheden moeten overeenkomen met die op de documentregel, wat wordt aangegeven door **0** in het veld **Niet gedefinieerd**.  

Wanneer u het document boekt, worden de artikeltraceringsposten overgebracht naar de artikelposten.

### <a name="to-handle-serial-and-lot-numbers-when-getting-receipt-lines-from-a-purchase-invoice"></a>Serie- en lotnummers verwerken bij het ophalen van ontvangstregels vanuit een inkoopfactuur

Wanneer u geboekte ontvangst- of verzendingsregels ontvangt van gerelateerde facturen of creditnota's, worden artikeltraceringsregels op de magazijndocumenten automatisch overgedragen. Ze worden echter op een speciale manier verwerkt.

De functionaliteit ondersteunt de volgende inkomende processen:  

- **Ontvangstregels ophalen**: van een inkoopfactuur.  
- **Retourverzendregels ophalen**: van een inkoopcreditnota.  

De functionaliteit ondersteunt de volgende uitgaande processen:  

- **Verzendregels ophalen**: van een verkoopfactuur of van verzamelfacturen.  
- **Retourontvangstregels ophalen**: van een verkoopcreditnota.  

In deze gevallen worden de artikeltraceringsregels overgedragen naar de factuur of creditnota, maar op de pagina **Artikeltraceringsregels** kunt u de serie- of lotnummers niet wijzigen. U kunt alleen de hoeveelheden wijzigen.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopfacturen** in en selecteer vervolgens de gerelateerde koppeling  
2. Open een inkoopfactuur voor artikelen die zijn aangekocht met serie- of lotnummers.  
3. Ga vanuit een inkoopfactuur naar het sneltabblad **Regels** en kies de actie **Ontvangstregels ophalen**.  
4. Selecteer op de pagina **Ontvangstregels ophalen** een ontvangstregel met artikeltraceringsregels en kies vervolgens de knop **OK**.  

    Het brondocument wordt als een nieuwe regel naar de inkoopfactuur gekopieerd en de bijbehorende artikeltraceringsregels worden overgenomen op de pagina **Artikeltraceringsregels**.  

5. Selecteer in de inkoopfactuur de overgebrachte ontvangstregel.  
6. Kies op het sneltabblad **Regels** de actie **Regel** en kies vervolgens de actie **Artikeltraceringsregels** om de overgebrachte artikeltraceringsregels te vinden.  

U kunt de velden **Serienummer** en **Lotnummer** niet wijzigen. U kunt echter volledige regels verwijderen of de hoeveelheden wijzigen, zodat deze overeenkomen met wijzigingen op de bronregel.  

## <a name="to-assign-a-serial-or-lot-number-during-an-outbound-transaction"></a>Serie- of lotnummers toewijzen tijdens een uitgaande transactie

Het verwerken van uitgaande serie- of lotnummers is een taak die vaak plaatsvindt tijdens vele verschillende magazijnprocessen. Er zijn twee manieren om serie- en lotnummers aan uitgaande transacties toe te voegen:  

- Selecteren uit bestaande serie- of lotnummers. Dit is van toepassing als er al traceringsnummers zijn toegekend tijdens een inkomende transactie.
- Wijs nieuwe serie- of lotnummers toe voor uitgaande transacties: Dit is van toepassing wanneer artikeltraceringsnummers pas worden toegekend aan artikelen wanneer ze worden verkocht en klaar zijn voor verzending.

### <a name="to-select-from-existing-serial-or-lot-numbers"></a>U kunt als volgt nummers selecteren uit bestaande serie- of lotnummers

Wanneer u werkt met artikelen waarvoor artikeltracering vereist is en u uitgaande transacties maakt, moet u doorgaans lot- of serienummers selecteren die al bestaan.

1. Selecteer vanuit een uitgaand document de regel waarvoor u serie- of lotnummers wilt selecteren.  
2. Kies op het sneltabblad **Regels** de actie **Regel**, dan **Verwante gegevens** en selecteer vervolgens **Artikeltraceringsregels**.  
3. De pagina **Artikeltraceringsregels** beschikt over drie opties voor het opgeven van lot- of serienummers:  

   - Selecteer het veld **Serienr.** en vervolgens een nummer op de pagina **Serienr. - Lijst**.
   - Selecteer het veld **Lotnr.** en vervolgens een nummer op de pagina **Lotnr. - Lijst**. Selecteer vervolgens het veld **Serienr.** en selecteer een nummer op de pagina **Serienr. - Lijst**.
   - Selecteer de actie **Verwerken** en kies dan **Posten selecteren**. De pagina **Posten selecteren** toont alle lot- en serienummers samen met beschikbaarheidsinformatie.

4. Voer in het veld **Geselecteerd aantal** de te gebruiken hoeveelheid van elk lot- of serienummer in.
5. Kies de knop **Ok**. De trackinginformatie van het artikel wordt overgebracht naar de pagina **Artikeltraceringsregels**.  

De hoeveelheidsvelden in de kop geven een dynamische weergave van de hoeveelheden en totalen van de artikeltraceringsnummers die u op de pagina definieert. De hoeveelheden moeten overeenkomen met de waarden op de documentregel, wat wordt aangegeven met **0** in het veld **Niet gedefinieerd**.  

Wanneer u de documentregel boekt, worden de artikeltraceringsposten overgebracht naar de bijbehorende artikelposten.

### <a name="to-assign-new-serial-or-lot-numbers"></a>Nieuwe serie- of lotnummers toewijzen

Dit proces is van toepassing als artikelen geen serie- of lotnummer hebben terwijl ze op voorraad zijn. In plaats daarvan wijst u traceringsnummers van artikelen toe wanneer de artikelen zijn verkocht en gereed zijn voor verzending. In dit geval worden de nummers meestal toegewezen vanuit een vooraf gedefinieerde nummerreeks.

1. Selecteer het relevante document, bijvoorbeeld een verkoopfactuur of verkooporder, en kies op het tabblad **Regels** de actie **Lijn**, dan **Verwante gegevens** en kies vervolgens de actie **Artikeltraceringsregels**.  

    U kunt op een van de volgende manieren artikeltraceringsnummers toewijzen:  
    - Automatisch, uit een voorgedefinieerde nummerreeks: kies de actie **Serienr. toekennen** of **Lotnr. toekennen**.  
    - Automatisch, op basis van parameters die u speciaal voor het uitgaande artikel definieert: kies de actie **Aangepast serienr. maken**.  
    - Handmatig, door de serie- of lotnummers in te voeren, zonder een nummerreeks te gebruiken.  

2. Voor deze procedure moet u automatisch een serienummer toekennen door te kiezen voor **Serienr. toekennen**  

    Het veld **Te maken aantal** bevat standaard het regelaantal, maar u kunt dit wijzigen.  
3. Schakel het selectievakje **Nieuw lotnr. maken** in om de nieuwe serienummers te ordenen in een ander lot.  
4. Kies de knop **OK** om een nieuw lotnummer en nieuwe reeks losse serienummers te maken op basis van het aantal te verwerken artikelen op de documentregel in kwestie.  

De hoeveelheidsvelden bovenaan geven een dynamische weergave van de hoeveelheden en totalen van de artikeltraceringsnummers die u op de pagina definieert. De hoeveelheden moeten overeenkomen met de waarden op de documentregel, wat wordt aangegeven met **0** in het veld **Niet gedefinieerd**.  

Wanneer het document wordt geboekt, worden de artikeltraceringsposten overgebracht naar de artikelposten.

### <a name="assign-tracking-numbers-on-source-documents"></a>Traceringsnummers toewijzen in brondocumenten

Sommige bedrijven definiëren specifieke serie- of lotnummers op het brondocument, zoals verkooporders. Bijvoorbeeld als een klant een specifieke lot aanvraagt. Als u het voorraad-pickdocument of magazijn-pickdocument maakt vanuit een uitgaand brondocument, waarbij serie- of lotnummers voor artikelen al bepaald zijn, kunt u geen van de velden op de pagina **Artikeltraceringsregels** onder de voorraadpick wijzigen. De enige uitzondering is het veld **Te verwerken aantal**. In dat geval worden in de voorraadpickregels de artikeltraceringsnummers gespecificeerd op afzonderlijke Nemen- en Plaatsen-regels. Het aantal is reeds gesplitst in unieke serie- of lotnummercombinaties, omdat in de verkooporder wordt gespecificeerd dat de artikeltraceringsnummers worden verzonden.

## <a name="to-handle-serial-and-lot-numbers-on-transfer-orders"></a>Serie- en lotnummers verwerken op transferorders

De procedures voor het verwerken van serie- en lotnummers die tussen verschillende vestigingen worden verplaatst, zijn gelijk aan de procedures die worden toegepast bij de inkoop en verkoop van artikelen.  

De transferorders zijn echter uniek, omdat voor zowel verzending als ontvangst dezelfde transferregel wordt gebruikt, en dezelfde instantie van de pagina **Artikeltraceringsregels**. Artikeltraceringsnummers die op de ene vestiging worden verzonden, moeten ongewijzigd worden ontvangen op de andere vestiging.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Transferorders** in en kies vervolgens de gerelateerde koppeling  
2. Open de transferorder die u wilt verwerken. Kies op het sneltabblad **Regels** de actie **Regel**, kies de actie **Artikeltraceringsregels** en vervolgens de actie **Verzending**.  
3. Voer de toewijzing of selectie van serie-/lotnummers op de pagina **Artikeltraceringsregels** op dezelfde wijze uit als bij andere uitgaande artikeltransacties.  

    Wanneer u serie- en lotnummers voor transferartikelen verwerkt, zijn nummers meestal al toegewezen. Daarom kiest u vaak uit bestaande serie- of lotnummers.  

4. Boek de transferorder (eerst de verzending, daarna de ontvangst) om vast te leggen dat de artikelen zijn overgebracht en hun artikeltraceringsposten hebben.  

Tijdens de overdracht kunt u de waarden op de pagina **Artikeltraceringsregels** niet wijzigen.  

## <a name="to-record-additional-serial-or-lot-number-information"></a>Aanvullende gegevens over serie-/lotnummers vastleggen

Als u speciale informatie aan een artikeltraceringsnummer wilt koppelen, bijvoorbeeld voor kwaliteitscontrole, kunt u dat doen op een serie- of lotnummerinformatiekaart.

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

## <a name="to-modify-existing-serial-or-lot-number-information"></a>Gegevens over bestaande serie- of lotnummers wijzigen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer een artikel met een artikeltraceringscode en met serie- of lotnummergegevens.
3. Kies op de pagina **Artikel** de actie **Posten** en kies daarna **Posten**.
4. Kies het veld **Lotnr.** of **Serienr.**. Als er informatie over dit artikeltraceringsnummer bestaat, wordt de pagina **Gegevensoverzicht lotnr.** of **Gegevensoverzicht serienr.** geopend.  
5. Selecteer een kaart en kies de actie **Lotnr.-informatie/Serienr.-informatie**.  
6. De korte omschrijving, de opmerkingrecord of het veld **Geblokkeerd** wijzigen.  

U kunt de serie- of lotnummers of de hoeveelheden niet wijzigen. Hiervoor moet u de artikelpost herindelen. Ga voor meer informatie over herclassificatie naar [Lot- of serienummers opnieuw classificeren](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).

## <a name="to-reclassify-serial-or-lot-numbers"></a>Serie- of lotnummers herindelen

Het herindelen van artikeltracering wil zeggen dat u een lot- of serienummer wijzigt in een nieuw lot- of serienummer of de vervaldatum wijzigt in een nieuwe vervaldatum. Als u met lots werkt, is het ook mogelijk om meerdere lots samen te voegen tot één lot. Gebruik een artikelherindelingsjournaal om deze taken uit te voeren.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Mag.-herindelingsdagboek** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de betreffende informatie in op de regel. Zie voor meer informatie [Voorraad tellen met documenten](inventory-how-count-inventory-with-documents.md) of [Voorraad tellen, corrigeren en herindelen met dagboeken](inventory-how-count-adjust-reclassify.md).
3. Kies de actie **Artikeltraceringsregels**.  
4. Selecteer in het veld **Serienummer** of **Lotnr.** het huidige serie- of lotnummer.  
5. Als u een nieuw artikeltraceringsnummer wilt opgeven, doet u dat in het veld **Nieuw serienr.** of **Nieuw lotnummer**. U kunt ook meerdere lots samenvoegen tot één nieuw of bestaand lot.  

    > [!NOTE]  
    > Wanneer u vervaldatums opnieuw indeelt, moeten artikelen met de vroegste vervaldatum voor uitgaande transacties eerst worden voorgesteld. Ga voor meer informatie naar [Picken volgens FEFO](warehouse-picking-by-fefo.md).  

6. Als u een nieuwe vervaldatum voor het serie- of lotnummer wilt opgeven, doet u dat in het veld **Nieuwe verloopdatum**.  

    > [!IMPORTANT]  
    > * Als u een lot herindeelt naar hetzelfde lotnummer, maar met een andere vervaldatum, moet u het volledige lot herindelen met gebruik van één regel in het artikelherindelingsdagboek. 
    > * Als u meerdere lots herindeelt naar één nieuw lotnummer, dat wil zeggen als u meerdere lots samenvoegt tot één nieuw lot, dient u dezelfde nieuwe vervaldatum op te geven voor alle lots. 
    > * Als u een bestaande lot herindeelt naar een tweede bestaande lot met een andere vervaldatum, moet u de vervaldatum van de tweede lot gebruiken. 
    > * Als u het veld **Nieuwe verloopdatum** niet invult, wordt het lot- of serienummer heringedeeld met een lege vervaldatum.  

7. U kunt bestaande informatie over het oude serie- of lotnummer naar het nieuwe serie- of lotnummer kopiëren.  

    1. Kies op de pagina **Artikeltraceringsregels** de actie **Nieuwe serienummergegevens** of **Nieuwe lotnummergegevens**.  
    2. Als u informatie wilt kopiëren vanuit het oude lot- of serienummer, kiest u de actie **Gegevens kopiëren**.  
    3. Selecteer het lot- of serienummer waarvan u gegevens wilt kopiëren op de informatiepagina en klik op **OK**.  

8. Als u de bestaande gegevens voor het lot- of serienummer wilt wijzigen, kunt u informatie over lot- of serienummers vastleggen.  
9. Boek het dagboek om de vernieuwde artikeltraceringsnummers of vervaldatums te koppelen aan de bijbehorende artikelpost.

## <a name="scan-barcodes-with-the-business-central-mobile-app"></a>Barcodes scannen met de mobiele Business Central-app

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

Als u meerdere serie-, lot- of pakketbarcodes wilt scannen, kunt u op de pagina **Artikeltraceringsregels** de actie **Meerdere scannen** gebruiken. Nadat u een barcode hebt gescand, wordt de waarde ervan in het veld op de pagina ingevoerd en komt het volgende snelinvoerveld beschikbaar. U kunt ook het barcodescannerpictogram gebruiken om een specifiek veld in te vullen.

In de volgende tabellen worden de pagina's vermeld die het scannen van barcodes ondersteunen voor artikeltracering vanuit de mobiele [!INCLUDE [prod_short](includes/prod_short.md)]-app.

|Pagina  |Veldwaarden die u kunt scannen  |
|---------|---------|
|Artikeltraceringsregels     |* Serienr.<br><br>* Nieuw serienr.<br><br>* Lotnr.<br><br>* Nieuw lotnr.<br><br>* Pakketnr.<br><br>* Nieuw pakketnr.|
|Mag. Artikeltraceringsregels     |* Serienr.<br><br>* Nieuw serienr.<br><br>* Lotnr.<br><br>* Nieuw lotnr.<br><br>* Pakketnr.<br><br>* Nieuw pakketnr.|
|Artikeltracering     |* Serienr.-filter<br><br>* Lotnr.-filter<br><br>* Pakketnr. Filteren |
|Artikeldagboek     |* Serienr.<br><br>* Lotnr.<br><br>* Pakketnr.     |
|Magazijnactiviteitsregel     |* Serienr.<br><br>* Lotnr.<br><br>* Pakketnr.<br><br>**Opmerking**: Op de volgende pagina's wordt de pagina Magazijnactiviteitsregel gebruikt:<br><br>* pagina 5780 Subformulier Magazijnpick<br><br>* Pagina 7378 Subformulier Voorraadpick<br><br>* pagina 5771 Subformulier Magazijnopslag<br><br>* Pagina 7316 Subformulier Magazijnverplaatsing<br><br>* Pagina 7376 Subformulier Voorraadopslag<br><br>* Pagina 7383 Subformulier Voorraadverplaatsing        |
|Mag. inventarisatiedagboek     |* Serienr.<br><br>* Lotnr.<br><br>* Pakketnr.         |

## <a name="see-also"></a>Zie ook

[Artikeltracering instellen met serie-, lot- en pakketnummers](inventory-how-setup-item-tracking.md)  
[Artikelen met artikeltracering traceren](inventory-how-to-trace-item-tracked-items.md)  
[Voorraad](inventory-manage-inventory.md)  
[Ontwerpdetails: Artikeltracering](design-details-item-tracking.md)  
[Ontwerpdetails: Artikeltracering en reserveringen](design-details-item-tracking-and-reservations.md)  
[Artikelen reserveren](inventory-how-to-reserve-items.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
