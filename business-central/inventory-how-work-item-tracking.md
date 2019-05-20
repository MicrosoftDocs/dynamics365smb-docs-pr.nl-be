---
title: Serie- en lotnummers toewijzen aan artikelen voor tracering | Microsoft Docs
description: U kunt serie- en lotnummers toevoegen aan elk uitgaand of inkomend document en de bijbehorende geboekte artikeltraceringsposten worden in de artikelposten weergegeven.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: sgroespe
ms.openlocfilehash: c7a5aa7d768a4fe2fae111b04ffc1fdab65d07dc
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1240384"
---
# <a name="work-with-serial-and-lot-numbers"></a>Werken met serie- en lotnummers
U kunt serie- en lotnummers toewijzen aan elk uitgaand of inkomend document en de bijbehorende geboekte artikeltraceringsposten worden in de artikelposten weergegeven. U voert het werk uit op de pagina **Artikeltraceringsregels**, die u opent vanuit een inkomend of uitgaand document.

De matrix van aantalvelden bovenin de pagina **Artikeltraceringsregels** geeft de aantallen en totalen van artikeltraceringsnummers weer die op de regels worden gedefinieerd. De aantallen moeten overeenkomen met de waarden op de documentregel. **Niet gedefinieerde** velden hebben hierbij de waarde 0.

Ten behoeve van de prestaties wordt de beschikbare informatie op de pagina **Artikeltraceringsregels** slechts eenmaal verzameld wanneer u de pagina opent. Dat betekent dat de beschikbaarheidsgegevens niet worden bijgewerkt wanneer de pagina geopend is, zelfs niet wanneer gedurende die tijd wijzigingen optreden in de voorraad of in andere documenten.

Artikelen met serie-/lotnummers kunnen voorwaarts en achterwaarts worden getraceerd in de toeleveringsketen. Dit is handig voor algemene kwaliteitsmeting en voor terugroepacties. Zie voor meer informatie [Artikelen met artikeltracering traceren](inventory-how-to-trace-item-tracked-items.md).

## <a name="about-picking-serial-or-lot-numbers-in-the-warehouse"></a>Serie- of lotnummers picken in het magazijn
Het verwerken van uitgaande serie- of lotnummers is een taak die vaak plaatsvindt tijdens vele verschillende magazijnprocessen.  

Bij sommige processen hebben de voorraadartikelen geen serie- of lotnummers en moeten de magazijnmedewerkers deze tijdens de uitgaande activiteiten toekennen, waarbij zij meestal kiezen uit een vooraf bepaalde nummerreeks.

Bij eenvoudige processen heeft elk voorraadartikel al een serie- of lotnummer (die bijvoorbeeld bij het opslaan zijn toegewezen) en deze nummers worden automatisch bij alle uitgaande magazijnactiviteiten doorgegeven zonder tussenkomst van magazijnmedewerkers.

In speciale gevallen voor voorraad met een serie- of lotnummer, worden op het brondocument (zoals een verkooporder) specifieke serie- of lotnummers gedefinieerd die de magazijnmedewerker aan moet houden tijdens uitgaande magazijnverwerking. De reden kan zijn dat de klant tijdens het orderproces een specifieke partij heeft verzocht. Als het voorraad-pickdocument of magazijn-pickdocument gemaakt wordt vanuit een uitgaand brondocument, waarbij serie- of lotnummers voor artikelen al bepaald zijn, kan geen enkel veld op de pagina **Artikeltraceringsregels** onder de voorraadpick overschreven worden, behalve het veld **Te verwerken aantal**. In dat geval worden in de voorraadpickregels de artikeltraceringsnummers gespecificeerd op afzonderlijke Nemen- en Plaatsen-regels. Het aantal is reeds gesplitst in unieke serie- of lotnummercombinaties, omdat in de verkooporder wordt gespecificeerd dat de artikeltraceringsnummers worden verzonden.  

## <a name="item-tracking-availability"></a>Beschikbaarheid van artikeltracering
Wanneer u met serie- of lotnummers werkt, berekent [!INCLUDE[d365fin](includes/d365fin_md.md)] beschikbaarheidsinformatie voor serie- en lotnummers en geeft dit weer op de artikeltraceringspagina's. Zo kunt u zien hoeveel van een lotnummer of serienummer op dit moment wordt gebruikt op andere documenten. Dit vermindert fouten en onzekerheid veroorzaakt door dubbele toewijzingen.

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

## <a name="to-set-up-item-tracking-codes"></a>Artikeltraceringscodes instellen
Een artikeltraceringscode weerspiegelt de verschillende overwegingen die een bedrijf moet maken met betrekking tot het gebruik van serie- en lotnummers voor artikelen die in de voorraad worden verplaatst.  

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikeltraceringscodes** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.
3. Vul indien nodig de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Definieer op de sneltabbladen **Serienummer** en **Lotnr.** beleid voor artikeltracering via respectievelijk serie- of lotnummers.  

> [!NOTE]  
>  Als u bepaalde artikelen of bepaalde lots tijdens hun levensduur wilt bijhouden, moet u respectievelijk de velden **Specifieke serienr.-tracering** en **Specifieke lottracering** kiezen. Wanneer u een uitgaande eenheid van een artikel met deze artikeltraceringscode verwerkt, moet u daarom altijd opgeven welk bestaand serienummer of lotnummer moet worden verwerkt. Dit betekent dat elke verkochte eenheid van het artikel moet worden vereffend met een bepaalde reeks serienummers of een specifiek lotnummer in de voorraad. Met andere woorden: het serienummer of lotnummer dat bij de invoer in de voorraad aan het artikel is toegewezen, moet samen met dat artikelsoort uit de voorraad worden geboekt.

Omdat dit bepaalde configuratieveld alle mogelijke artikeltransacties omvat, worden de afzonderlijke inkomende/uitgaande velden ook geselecteerd. De afzonderlijke inkomende/uitgaande velden hebben echter geen invloed op voorraadvereffening. Ze geven uitsluitend aan wanneer artikeltraceringsnummers worden toegewezen in de werkstroom van uw bedrijf.  

### <a name="to-set-up-expiration-rules-for-serial-or-lot-numbers"></a>Vervalregels instellen voor serie- of lotnummers  
Voor sommige artikelen wilt u mogelijk bepaalde vervaldatums en regels instellen in de artikeltraceringscode. Met deze functie kunt u bijhouden wanneer bepaalde serie- of lotnummers vervallen.

1. Selecteer een bestaande artikeltraceringscode en kies de actie **Bewerken**.  
2.  Schakel op het sneltabblad **Diversen** de volgende selectievakjes in.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Strikte verloopdatumboeking**|Hiermee wordt opgegeven dat de vervaldatum van het artikeltraceringsnummer dat bij binnenkomst in de voorraad is toegewezen, strikt moet worden nagekomen bij het verlaten van de voorraad.|  
    |**Vervaldatum handmatig invoeren**|Hiermee wordt opgegeven dat u de vervaldatum op de artikeltraceringsregel handmatig moet invoeren.|  
    |**Vervaldatums negeren**|Hiermee wordt opgegeven dat u geen vervaldatums wilt berekenen. |  

### <a name="to-set-up-warranties-for-serial-or-lot-numbers"></a>Garanties instellen voor serie- of lotnummers  
Mogelijk wilt u voor bepaalde artikelen bepaalde garanties instellen in de artikeltraceringscode. Met deze functie kunt u bijhouden wanneer de garanties op bepaalde serie- en lotnummers in de voorraad verlopen.        
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikeltraceringscodes** in en kies vervolgens de gerelateerde koppeling.  

1. Selecteer een bestaande artikeltraceringscode en kies de actie **Bewerken**.  
2.  Vul het veld **Garantiedatumformule** op het sneltabblad **Overig** in en schakel de volgende selectievakjes in.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Garantiedatumformule**|Bevat de laatste dag van de garantie voor het artikel.|  
    |**Garantiedatum handmatig invoeren**|Geeft aan dat u een garantiedatum op de artikeltraceringsregel handmatig moet invoeren.|  

## <a name="to-record-serial-or-lot-number-information"></a>Gegevens over serie-/lotnummers vastleggen  
Op een informatiekaart voor serie- of lotnummers kunt u gegevens koppelen aan een specifiek artikeltraceringsnummer (bijvoorbeeld voor kwaliteitscontrole).

1. Open een document waaraan veel serie- of lotnummers zijn toegewezen.
2. Open de pagina **Artikeltraceringsregels** voor het document.
3. Kies bijvoorbeeld de actie **Serienr.-informatie**.  

    De velden **Serienr.** en **Lotnr.** zijn al ingevuld op de artikeltraceringsregel.  
4. Geef een kort stukje informatie in het veld **Omschrijving**, bijvoorbeeld over de staat van het artikel.  
5. Kies de actie **Opmerking** om een aparte record met een opmerking maken.  
6. Schakel het selectievakje **Geblokkeerd** in om het serie- of lotnummer uit te sluiten van transacties.  

## <a name="to-modify-existing-serial-or-lot-number-information"></a>Gegevens over bestaande serie- of lotnummers wijzigen  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer een artikel met een artikeltraceringscode en met serie- of lotnummergegevens.
3. Kies op de pagina **Artikel** de actie **Posten** en kies daarna **Posten**.
4. Kies het veld **Lotnr.** of **Serienr.**. Als er informatie over dit artikeltraceringsnummer bestaat, wordt de pagina **Gegevensoverzicht lotnr.** of **Gegevensoverzicht serienr.** geopend.  
5. Selecteer een kaart en kies de actie **Lotnr.-informatie/Serienr.-informatie**.  
6. De korte omschrijving, de opmerkingrecord of het veld **Geblokkeerd** wijzigen.  

U kunt de serienummers of lotnummers of aantallen niet wijzigen. Hiervoor moet u de betreffende artikelpost herindelen. Raadpleeg voor meer informatie [Lot- of serienummers herindelen](inventory-how-work-item-tracking.md#to-reclassify-serial-or-lot-numbers).

## <a name="to-assign-serial-or-lot-numbers-during-an-inbound-transaction"></a>Serie- of lotnummers toewijzen tijdens inkomende transacties  
Bedrijven willen artikelen mogelijk bijhouden vanaf het moment dat ze het bedrijf binnenkomen. In deze situatie is de inkooporder vaak het centrale document. Artikeltracering kan echter vanaf elk inkomend document worden verwerkt. De geboekte posten worden dan weergegeven in de bijbehorende artikelposten.  

Welke regels precies gelden voor de verwerking van artikeltraceringsnummers binnen uw bedrijf, is afhankelijk van de instelling op de pagina **Artikeltraceringscode**.  

> [!NOTE]  
>  Om artikeltraceringsnummers te kunnen gebruiken bij magazijnactiviteiten moeten de instellingsvelden **Magazijnlottracering** en **Magazijnserienr.-tracering** zijn geselecteerd. Hiermee bepaalt u namelijk welke speciale principes gelden voor het verwerken van serie- en lotnummers in magazijnactiviteiten.  

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkooporders** in en kies vervolgens de gerelateerde koppeling.  
2.  Selecteer de relevante documentregel en kies vervolgens op het sneltabblad **Regels** de actie **Regel** en daarin de actie **Artikeltraceringregels**.  

    U kunt nu op een van de volgende manieren serie- of lotnummers toewijzen:  

    -   Automatisch, door **Serienr. toekennen** of **Lotnr. toekennen** te kiezen om serie- of lotnummers toe te kennen uit voorgedefinieerde nummerreeksen.  
    -   Automatisch, door **Aangepast serienr. maken** te kiezen om serie- of lotnummers toe te kennen die zijn gebaseerd op de nummerreeks die u specifiek voor de ontvangen artikelen hebt gedefinieerd.  
    -   Handmatig, door rechtstreeks serie- of lotnummers in te voeren. U kunt bijvoorbeeld de nummers van de leverancier gebruiken.  
    -   Handmatig, door aan iedere artikeleenheid een specifiek nummer toe te kennen.  

3. Als u deze automatisch wilt laten toewijzen, kiest u de actie **Aangepast serienr. maken**.  
4. In het veld **Aangepast serienr.** voert u het beginnummer in van een omschrijvende serienummerreeks, bijvoorbeeld **S/N-Lev0001**.  
5. In het veld **Interval** typt u 1, om aan te geven dat de volgnummers steeds met één worden verhoogd.  

    Het veld **Te maken aantal** bevat standaard het regelaantal, maar u kunt dit wijzigen.  

6. Schakel het selectievakje **Nieuw lotnr. maken** in om de nieuwe serienummers te ordenen in een ander lot.  
7. Kies de knop **OK**.  

Er wordt een lotnummer aangemaakt met een reeks losse serienummers (gebaseerd op het totale aantal op de documentregel), te beginnen met **S/N-Lev0001**.  

De matrix van aantalvelden op de kop geeft een dynamische weergave van de aantallen en totalen van de artikeltraceringsnummers die u op de pagina definieert. De aantallen moeten overeenkomen met de waarden op de documentregel. **Niet gedefinieerde** velden hebben hierbij de waarde 0.  

Als het document wordt geboekt, worden de artikeltraceringsposten overgebracht naar de bijbehorende artikelposten.

## <a name="to-assign-a-serial-or-lot-number-during-an-outbound-transaction"></a>Serie- of lotnummers toewijzen tijdens een uitgaande transactie  
Er zijn twee manieren om serie- en lotnummers aan uitgaande transacties toe te voegen:  

-   Nummers selecteren uit bestaande serie- of lotnummers. Dit is van toepassing als er al traceringsnummers zijn toegekend tijdens een inkomende transactie. Zie voor meer informatie [Keuze maken uit bestaande serie- en lotnummers](inventory-how-work-item-tracking.md#to-select-from-existing-serial-or-lot-numbers).
-   Nieuwe serie- of lotnummers toewijzen tijdens uitgaande transacties. Dit is van toepassing wanneer artikeltraceringsnummers pas worden toegekend aan items op het moment dat ze worden verkocht en klaar zijn voor verzending.  

De verschillende regels voor artikeltraceringsnummers worden ingesteld op de pagina **Artikeltraceringscode**.  

> [!NOTE]  
>  Om tijdens magazijnactiviteiten artikeltraceringsnummers toe te voegen moeten de selectievakjes **Magazijnserienr.-tracering** en **Magazijnlottracering** zijn ingeschakeld op de bij het artikel horende artikeltraceringscodekaart.    

1. Selecteer de relevante documentregel en kies vervolgens op het sneltabblad **Regels** de actie **Order** en daarin de actie **Artikeltraceringregels**.  

    U kunt op een van de volgende manieren artikeltraceringsnummers toewijzen:  
    -   Automatisch, uit voorgedefinieerde nummerreeksen: kies de actie **Serienr. toekennen** of **Lotnr. toekennen**.  
    -   Automatisch, op basis van parameters die u speciaal voor het uitgaande artikel definieert: kies de actie **Aangepast serienr. maken**.  
    -   Handmatig, door de serie- of lotnummers rechtstreeks in te voeren, zonder een nummerreeks te gebruiken.  

2.  Voor deze procedure moet u automatisch een serienummer toekennen door te kiezen voor **Serienr. toekennen**  

    Het veld **Te maken aantal** bevat standaard het regelaantal, maar u kunt dit wijzigen.  
3.  Schakel het selectievakje **Nieuw lotnr. maken** in om de nieuwe serienummers te ordenen in een ander lot.  
4.  Kies de knop **OK** om een nieuw lotnummer en nieuwe reeks losse serienummers te maken op basis van het aantal te verwerken artikelen op de documentregel in kwestie.  

De matrix van aantalvelden bovenin geeft een dynamische weergave van de aantallen en totalen van de artikeltraceringsnummers die u op de pagina definieert. De aantallen moeten overeenkomen met de waarden op de documentregel. **Niet gedefinieerde** velden hebben hierbij de waarde **0**.  

Als het document wordt geboekt, worden de artikeltraceringsposten overgebracht naar de bijbehorende artikelposten.  

## <a name="to-select-from-existing-serial-or-lot-numbers"></a>U kunt als volgt nummers selecteren uit bestaande serie- of lotnummers  
Wanneer u werkt met artikelen waarvoor artikeltracering is vereist en u uitgaande transacties maakt, d.w.z. transacties waarmee artikelen uit de voorraad worden gehaald, dient u meestal de lot- of serienummers te selecteren van artikelen die al in de voorraad staan.  

 Welke regels precies gelden voor de verwerking van artikeltraceringsnummers binnen uw bedrijf, is afhankelijk van de instelling in de tabel **Artikeltraceringscode**.  

> [!NOTE]  
>  U kunt artikeltraceringsnummers verwerken bij magazijnactiviteiten als u het artikel hebt ingesteld met Magazijnserienr.-tracering/Magazijnlottracering. Hiermee bepaalt u namelijk welke speciale principes gelden voor serie- en lotnummers in het magazijn.

1.  Selecteer vanuit een uitgaand document de regel waarvoor u serie- of lotnummers wilt selecteren.  
2.  Kies op het sneltabblad **Regels** de actie **Acties**. Kies de actie **Regel** of **Artikel** en vervolgens de actie **Artikeltraceringsregels**.  
3.  De pagina **Artikeltraceringsregels** beschikt over drie opties voor het opgeven van lot- of serienummers:  

    -   Selecteer het veld **Lotnr.** of **Serienr.** en vervolgens een nummer op de pagina **Artikeltraceringssamenvatting**.  
    -   Kies de actie **Posten selecteren**. De pagina **Posten selecteren** toont alle lot- of serienummers samen met beschikbaarheidsinformatie.

4. Voer in het veld **Geselecteerd aantal** de hoeveelheid van elk lot- of serienummer in dat u wilt gebruiken.   
5. Kies de knop **OK** om de geselecteerde artikeltraceringsgegevens over te brengen naar de pagina **Artikeltraceringsregels**.  
6. Typ of scan het artikeltraceringsnummer.

De matrix van aantalvelden op de kop geeft een dynamische weergave van de aantallen en totalen van de artikeltraceringsnummers die u op de pagina definieert. De aantallen moeten overeenkomen met de waarden op de documentregel. **Niet gedefinieerde** velden hebben hierbij de waarde **0**.  

 Als u de documentregel boekt, worden de artikeltraceringsposten overgebracht naar de bijbehorende artikelposten.

## <a name="to-handle-serial-and-lot-numbers-on-transfer-orders"></a>Serie- en lotnummers verwerken op transferorders  
De procedures voor het verwerken van serie- en lotnummers die tussen verschillende vestigingen worden verplaatst, zijn gelijk aan de procedures die worden toegepast bij de inkoop en verkoop van artikelen.  

De transferorder is echter uniek, omdat voor zowel verzending als ontvangst dezelfde transferregel wordt gebruikt, en dus dezelfde informatie op de pagina **Artikeltraceringsregels**. Dit betekent dat alle artikeltraceringsnummers die op de ene vestiging worden verzonden, ongewijzigd moeten worden ontvangen op de andere vestiging.  

 Welke regels precies gelden voor de verwerking van artikeltraceringsnummers binnen uw bedrijf, is afhankelijk van de instelling in de tabel  **Artikeltraceringscode**.    
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Transferorders** in en kies vervolgens de gerelateerde koppeling.  
2.  Open de transferorder die u wilt verwerken. Kies op het sneltabblad **Regels** de actie **Regel**. Kies de actie **Artikeltraceringsregels** en vervolgens de actie **Verzending**.  
3.  Voer de toewijzing of selectie van serie-/lotnummers op de pagina **Artikeltraceringsregels** op dezelfde wijze uit als bij andere uitgaande artikeltransacties.  

    Bij het verwerken van serie- en lotnummers voor transferartikelen hebben de artikelen meestal al een nummer. Daarom zult u normaal gesproken alleen nummers selecteren uit bestaande serie- of lotnummers.  

4.  Boek de transferorder (eerst de verzending, daarna de ontvangst) om vast te leggen dat de artikelen zijn verplaatst met hun artikeltraceringsposten.  

Tijdens de transfer is de pagina **Artikeltraceringsregels** beveiligd tegen schrijven.  

## <a name="to-handle-serial-and-lot-numbers-when-getting-receipt-lines-from-a-purchase-invoice"></a>Serie- en lotnummers verwerken bij het ophalen van ontvangstregels vanuit een inkoopfactuur  
Wanneer u functionaliteit gebruikt om geboekte ontvangst- of verzendregels op te halen uit verwante facturen of creditnota's, worden alle artikeltraceringsregels op de magazijndocumenten automatisch overgebracht. Hierbij worden zij echter op een speciale manier verwerkt.

De functionaliteit ondersteunt de volgende inkomende processen:  
-   **Ontvangstregels ophalen**: van een inkoopfactuur.  
-   **Retourverzendregels ophalen**: van een inkoopcreditnota.  

De functionaliteit ondersteunt de volgende uitgaande processen:  
-   **Verzendregels ophalen**: van een verkoopfactuur of van verzamelfacturen.  
-   **Retourontvangstregels ophalen**: van een verkoopcreditnota.  

In deze gevallen worden de bestaande artikeltraceringsregels automatisch gekopieerd naar de factuur of creditnota. Op de pagina **Artikeltraceringsregels** worden echter geen wijzigingen toegestaan in de serie- of lotnummers. Alleen de hoeveelheden kunnen worden gewijzigd.  

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkoopfacturen** in en selecteer vervolgens de gerelateerde koppeling.  
2.  Open een inkoopfactuur voor artikelen die zijn aangekocht met serie- of lotnummers.  
3.  Ga vanuit een inkoopfactuur naar het sneltabblad **Regels** en kies de actie **Ontvangstregels ophalen**.  
4.  Selecteer op de pagina **Ontvangstregels ophalen** een ontvangstregel met artikeltraceringsregels en kies vervolgens de knop **OK**.  

    Het brondocument wordt als een nieuwe regel naar de inkoopfactuur gekopieerd en de bijbehorende artikeltraceringsregels worden overgenomen op de pagina **Artikeltraceringsregels**.  

5.  Selecteer in de inkoopfactuur de overgebrachte ontvangstregel.  
6.  Kies op het sneltabblad **Regels** de actie **Regel** en vervolgens de actie **Artikeltraceringsregels** om de overgenomen artikeltraceringsregels te bekijken.  

U kunt de velden **Serienummer** en **Lotnr.** niet bewerken. U kunt echter volledige regels verwijderen of de aantallen wijzigen, zodat deze overeenkomen met de wijzigingen op de bronregel.  

## <a name="to-reclassify-serial-or-lot-numbers"></a>Serie- of lotnummers herindelen  
Het herindelen van artikeltracering wil zeggen dat u een lot- of serienummer wijzigt in een nieuw nummer of de vervaldatum wijzigt in een nieuwe datum. Als u met lots werkt, is het ook mogelijk om meerdere lots samen te voegen tot één lot. U kunt deze taken uitvoeren met behulp van het artikelherindelingsdagboek.

1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Art.-herindelingsdagboek** in en kies vervolgens de gerelateerde koppeling.  
2.  Vul de betreffende informatie in op de regel. Zie voor meer informatie [Voorraad tellen met documenten](inventory-how-count-inventory-with-documents.md) of [Voorraad tellen, corrigeren en herindelen met dagboeken](inventory-how-count-adjust-reclassify.md).
3.  Kies de actie **Artikeltraceringsregels**.  
4.  Selecteer in het veld **Serienummer** of **Lotnr.** het huidige serie- of lotnummer.  
5.  Als u een nieuw artikeltraceringsnummer wilt opgeven, doet u dat in het veld **Nieuw serienr.** of **Nieuw lotnummer**. U kunt ook meerdere lots samenvoegen tot één nieuw of bestaand lot.  

    > [!NOTE]  
    >  Denk eraan dat wanneer u vervaldata opnieuw indeelt, vervolgens de items met de vroegste vervaldatum voor uitgaande transacties eerst worden voorgesteld. Zie voor meer informatie [Picken op basis van FEFO](warehouse-picking-by-fefo.md).  

5.  Als u een nieuwe vervaldatum voor het serie- of lotnummer wilt invoeren, doet u dat in het veld **Nieuwe verloopdatum**.  

    > [!IMPORTANT]  
    >  Als u een lot herindeelt naar hetzelfde lotnummer, maar met een andere vervaldatum, moet u het volledige lot herindelen met gebruik van één regel in het artikelherindelingsdagboek. Als u meerdere lots herindeelt naar één nieuw lotnummer, dat wil zeggen als u meerdere lots samenvoegt tot één nieuw lot, dient u dezelfde nieuwe vervaldatum op te geven voor alle lots. Als u een bestaand lot herindeelt naar een tweede bestaand lot met een andere vervaldatum, moet u de vervaldatum van het tweede lot gebruiken. Als u het veld **Nieuwe verloopdatum** niet invult, wordt het lot- of serienummer heringedeeld met een lege vervaldatum.  

6.  U kunt bestaande informatie over het oude serie- of lotnummer naar het nieuwe serie- of lotnummer kopiëren.  

    1.  Kies op de pagina **Artikeltraceringsregels** de actie **Nieuwe serienummergegevens** of **Nieuwe lotnummergegevens**.  
    2.  Als u informatie wilt kopiëren vanuit het oude lot- of serienummer, kiest u de actie **Gegevens kopiëren**.  
    3.  Selecteer het lot- of serienummer waarvan u gegevens wilt kopiëren op de informatiepagina en klik op **OK**.  

7.  Als u de bestaande gegevens voor het lot- of serienummer wilt wijzigen, kunt u informatie over lot- of serienummers vastleggen.  
8.  Boek het dagboek om de vernieuwde artikeltraceringsnummers of vervaldatums te koppelen aan de bijbehorende artikelpost.

## <a name="see-also"></a>Zie ook
[Artikelen met artikeltracering traceren](inventory-how-to-trace-item-tracked-items.md)   
[Voorraad](inventory-manage-inventory.md)  
[Ontwerpdetails: Artikeltracering](design-details-item-tracking.md)
[Ontwerpdetails: Artikeltracering en reserveringen](design-details-item-tracking-and-reservations.md)  
[Artikelen reserveren](inventory-how-to-reserve-items.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
