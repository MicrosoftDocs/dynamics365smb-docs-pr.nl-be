---
title: Definiëren hoe gegevens elektronisch worden uitgewisseld
description: 'Definieer hoe Business Central gegevens uitwisselt met externe bestanden zoals elektronische documenten, bankgegevens, artikelcatalogi en meer.'
author: brentholtorf
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.search.form: '1210, 1211, 1213, 1214, 1215, 1216, 1217'
ms.date: 11/03/2022
ms.author: bholtorf
---
# <a name="set-up-data-exchange-definitions"></a><a name="set-up-data-exchange-definitions"></a>Definities voor gegevensuitwisseling instellen

U kunt [!INCLUDE[prod_short](includes/prod_short.md)] instellen om gegevens in specifieke tabellen uit te wisselen met gegevens in externe bestanden. Bijvoorbeeld voor het verzenden en ontvangen van elektronische documenten, het importeren en exporteren van bankgegevens of andere gegevens, zoals loonlijst, en artikelcatalogi. Meer informatie vindt u in [Gegevens elektronisch uitwisselen](across-data-exchange.md).  

Als u een gegevensuitwisselingdefinitie voor een gegevensbestand of -stroom wilt maken, kunt u het gerelateerde XML-schema gebruiken om te definiëren welke gegevenselementen moeten worden opgenomen op het sneltabblad **Kolomdefinities**. Zie stap 6 in [De opmaak van regels en kolommen in het bestand beschrijven](across-how-to-set-up-data-exchange-definitions.md#to-describe-the-formatting-of-lines-and-columns-in-the-file). Meer informatie vindt u in [XML-schema's gebruiken om definities voor gegevensuitwisseling voor te bereiden](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).  

Doorgaans stelt u gegevensuitwisselingsdefinities op de pagina **Definitie van gegevensuitwisseling** in. Voor het bijwerken van wisselkoersen is het echter sneller om een wisselkoersservice te gebruiken. Meer informatie vindt u in [Valutawisselkoersen bijwerken](finance-how-update-currencies.md#to-set-up-a-currency-exchange-rate-service).

> [!NOTE]  
> Als het bestand dat wordt geconverteerd, in de XML-indeling is, moet de term *kolom* in dit artikel worden geïnterpreteerd als een *"XML-element dat gegevens bevat"*.  

Dit artikel bevat de volgende procedures:  

* Definitie van gegevensuitwisseling maken.
* De definitie van een gegevensuitwisseling exporteren als een XML-bestand voor gebruik door anderen.
* Een XML-bestand importeren voor een bestaande definitie van gegevensuitwisseling.

## <a name="create-a-data-exchange-definition"></a><a name="create-a-data-exchange-definition"></a>Definitie van gegevensuitwisseling maken

Een definitie voor gegevensuitwisseling maken bestaat uit twee taken:  

1. Op de pagina **Definitie van gegevensuitwisseling** beschrijft u de opmaak van regels en kolommen in het bestand. Meer informatie vindt u in het gedeelte [De opmaak van regels en kolommen in het bestand beschrijven](#formatlinescolumns).  
2. Op de pagina **Toewijzing gegevensuitwisseling** wijst u kolommen in het gegevensbestand toe aan velden in [!INCLUDE[prod_short](includes/prod_short.md)]. Meer informatie vindt u in het gedeelte [Kolommen in het gegevensbestand toewijzen aan velden in [!INCLUDE[prod_short](includes/prod_short.md)]](#mapfields).  

### <a name="to-describe-the-formatting-of-lines-and-columns-in-the-file"></a><a name="to-describe-the-formatting-of-lines-and-columns-in-the-file"></a><a name=formatlinescolumns></a>De opmaak van regels en kolommen in het bestand beschrijven

1. Kies het pictogram ![Lampje dat de functie Vertel me opent 1.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gegevensuitwisselingsdefinities** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Nieuw**.  
3. Geef op het sneltabblad **Algemeen** de definitie voor gegevensuitwisseling en de soort gegevensbestand op door de velden in te vullen zoals beschreven in de volgende tabel.  

    |Veld|Definitie|  
    |---------------------------------|---------------------------------------|  
    |**Code**|Voer een code in ter identificatie van de definitie van de gegevensuitwisseling.|  
    |**Naam**|Voer een naam in voor de definitie van gegevensuitwisseling.|  
    |**Bestandssoort**|Geef op voor welk soort bestand de definitie van gegevensuitwisseling wordt gebruikt. U kunt kiezen uit vier bestandstypen:<br /><br /> -   **XML**: laagsgewijze strings met inhoud en opmaak, omringd door labels die functies aangeven.<br />-   **Variabele tekst**: records hebben een variabele lengte en worden gescheiden door een teken, zoals een komma of punt\-komma, ook wel *gescheiden bestand* genoemd.<br />-   **Vaste tekst**: records hebben dezelfde lengte, gebruiken opvultekens en elke record staat op een afzonderlijke regel, ook wel bekend als *bestand met vaste breedte*.<br />- **Json**: gelaagde strings met inhoud in JavaScript.|  
    |**Soort**|Geef op voor welke soort bedrijfsactiviteit de gegevensuitwisselingdefinitie wordt gebruikt, bijvoorbeeld **Betalingsexport**.|  
    |**Codeunit geg.afhandeling**|Geef de codeunit op die gegevens overbrengt in en uit tabellen in [!INCLUDE[prod_short](includes/prod_short.md)].|  
    |**Codeunit validatie**|Geef de codeunit op die wordt gebruikt om gegevens te valideren tegen vooraf bepaalde bedrijfsregels.|  
    |**Codeunit lezen/schrijven**|Geef de codeunit op die geïmporteerde gegevens verwerkt vóór het toewijzen en geëxporteerde gegevens na het toewijzen.|  
    |**Lezen/schrijven XMLport**|De XMLport opgeven waardoor een geïmporteerd gegevensbestand of een service binnenkomt vóór de toewijzing en waardoor geëxporteerde gegevens naar buiten gaan wanneer deze na de toewijzing naar een gegevensbestand of een service worden geschreven.|  
    |**Codeunit ext. geg.afhandeling**|Geef de codeunit op die externe gegevens overbrengt in en uit het kader voor gegevensuitwisseling.|  
    |**Codeunit feedback gebruiker**|Geef de codeunit op die opschoning verzorgt na het koppelen, zoals de regels markeren als geëxporteerd en tijdelijke records verwijderen.|  
    |**Bestandscodering**|Geef de codering van het bestand op. **Opmerking:** dit veld is alleen relevant voor importeren.|  
    |**Kolomscheidingsteken**|Geef op hoe kolommen in het gegevensbestand van elkaar zijn gescheiden, als het bestand het type **Variabele tekst** is.|  
    |**Kopregels**|Geef op hoeveel kopregels in het bestand zijn opgenomen.<br /><br /> Met deze instelling wordt ervoor gezorgd dat de koptekstgegevens niet worden geïmporteerd. **Opmerking:** dit veld is alleen relevant voor importeren.|  
    |**Koptag**|Als er op verschillende posities in het bestand een koptekstregel bestaat, voert u de tekst van de eerste kolom op de koptekstregel in.<br /><br /> Met deze optie wordt ervoor gezorgd dat de koptekstgegevens niet worden geïmporteerd. **Opmerking:** dit veld is alleen relevant voor importeren.|  
    |**Voetteksttag**|Als er op verschillende posities in het bestand een voettekstregel bestaat, voert u de tekst van de eerste kolom op de voettekstregel in.<br /><br /> Met deze optie wordt ervoor gezorgd dat de voettekstgegevens niet worden geïmporteerd. **Opmerking:** dit veld is alleen relevant voor importeren.|  

   > [!TIP]
   > Als u wilt zien welke codeunits Microsoft gebruikt in bestaande definities in het standaardproduct, controleert u voor elke definitie de drie **Codeunit**-velden op de pagina **Veldtoewijzing** onder het sneltabblad **Algemeen**.  

4. Geef op het sneltabblad **Regeldefinities** de opmaak van regels in het gegevensbestand op door de velden in te vullen zoals beschreven in de volgende tabel.  

    > [!NOTE]  
    > Voor importeren van bankafschriften kunt u slechts één regel maken voor de enkele notatie van het bankafschriftbestand dat u wilt importeren.  
    >
    > Voor export van betalingen kunt u een regel voor elk betalingstype maken dat u wilt exporteren. In dat geval toont het sneltabblad **Kolomdefinities** verschillende kolommen voor elke betalingssoort.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Regelsoort**|Hiermee wordt het soort opgegeven van de regel in het bestand.|  
    |**Code**|Voer een code in om de regel in het bestand te identificeren.|  
    |**Naam**|Voer een naam in die de regel in het bestand beschrijft.|  
    |**Kolomtelling**|Geef op hoeveel kolommen de regel in het gegevensbestand heeft. **Opmerking:** dit veld is alleen relevant voor importeren.|  
    |**Label voor gegevensregel**|Geef de positie op in het gerelateerde XML-schema van het onderdeel dat de belangrijkste post van het gegevensbestand vertegenwoordigt. **Opmerking:** dit veld is alleen relevant voor importeren.|  
    |**Naamruimte**|Geef de naamruimte op die wordt verwacht in het bestand, om naamruimtevalidatie mogelijk te maken. U kunt dit veld leeg laten als u geen naamruimtevalidatie mogelijk wilt maken.|  
    |**Hoofdcode**|Geef het bovenliggende element van de regel op, zoals in het veld **Code** wordt weergegeven, in gevallen waarin de instelling van gegevensuitwisseling bedoeld is voor bestanden met bovenliggende en onderliggende posten, zoals een documentkoptekst en regels.

5. Herhaal stap 4 om een regel te maken voor elk type bestandsgegevens dat u wilt exporteren.  

     Geef op het sneltabblad **Kolomdefinities** de opmaak van kolommen in het gegevensbestand op door de velden in te vullen zoals beschreven in de onderstaande tabel. U kunt het structuurbestand, zoals een .xsd-bestand, voor het gegevensbestand gebruiken om het sneltabblad vooraf te vullen met de relevante elementen. Meer informatie vindt u in [XML-schema's gebruiken om definities voor gegevensuitwisseling voor te bereiden](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md).

6. Kies op het sneltabblad **Kolomdefinities** de actie **Bestandsstructuur ophalen**.  
7. Selecteer op de pagina **Bestandsstructuur ophalen** het gerelateerde structuurbestand en kies vervolgens **OK**. De regels op het sneltabblad **Kolomdefinities** worden ingevuld op basis van de structuur van het gegevensbestand.  
8. Vul op het sneltabblad **Kolomdefinities** de velden in of bewerk ze zoals in de volgende tabel wordt beschreven.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Kolomnr.**|Geef het nummer op dat de kolompositie op de regel in het bestand aangeeft.<br /><br /> Geef voor XML-bestanden het nummer op dat het type element in het bestand aangeeft dat de gegevens bevat.|  
    |**Naam**|Geef de naam van de kolom op.<br /><br /> Geef voor XML-bestanden de markering op waarmee de uit te wisselen gegevens worden gemarkeerd.|  
    |**Gegevenstype**|Geef op of de uit te wisselen gegevens van het type **Tekst**, **Datum** of **Decimaal** zijn.|  
    |**Gegevensopmaak**|Geef de eventuele indeling van de gegevens op. Bijvoorbeeld **MM-dd-yyyy** als de gegevenssoort **Datum** is. **Opmerking:** voor exporteren geeft u de gegevensindeling op volgens [!INCLUDE[prod_short](includes/prod_short.md)]. Voor importeren geeft u de gegevensindeling op volgens .NET Framework. Meer informatie vindt u in [Standaardnotaties voor datum en tijd](/dotnet/standard/base-types/standard-date-and-time-format-strings).|  
    |**Cultuur gegevensopmaak**|Geef de eventuele regionale indeling van de gegevens op. Bijvoorbeeld **en-US** als het gegevenstype **Decimaal** is om te zorgen dat de komma wordt gebruikt als .000-scheidingsteken, volgens de Amerikaanse indeling. Meer informatie vindt u in [Standaardnotaties voor datum en tijd](/dotnet/standard/base-types/standard-date-and-time-format-strings). **Opmerking:** dit veld is alleen relevant voor importeren.|  
    |**Lengte**|Geef de lengte op van de regel met vaste breedte die de kolom bevat als het gegevensbestand het type **Vaste tekst** is.|  
    |**Beschrijving**|Hiermee wordt een omschrijving van de kolom opgegeven, ter informatie.|  
    |**Pad**|Geef de positie op van het element in het gerelateerde XML-schema.|  
    |**Identificatie voor een negatief teken**|Voer de waarde in die in het gegevensbestand wordt gebruikt om negatieve bedragen te identificeren in gegevensbestanden die geen negatieftekens kunnen bevatten. Deze id wordt vervolgens gebruikt om de geïdentificeerde aantallen naar negatieftekens tegen te boeken tijdens het importeren. **Opmerking:** dit veld is alleen relevant voor importeren.|  
    |**Constant**|Geef alle gegevens op die u wilt exporteren in deze kolom, zoals extra informatie over het betalingstype. **Opmerking:** dit veld is alleen relevant voor exporteren.|  
    |**Opvulling van tekst vereist**|Geef op dat de gegevens tekstopvulling moeten bevatten.|  
    |**Opvullingsteken**|Geef het tekstopvullingsteken op.|  
    |**Uitvulling**|Geef op of de kolomuitvulling links of rechts is.|  

9. Herhaal stap 8 voor alle kolommen of XML-elementen in het gegevensbestand met gegevens die u wilt uitwisselen met [!INCLUDE[prod_short](includes/prod_short.md)].  

De volgende stap bij het maken van de definitie van een gegevensuitwisseling bestaat uit het bepalen van welke kolommen of XML-elementen in het gegevensbestand worden gekoppeld aan welke velden in [!INCLUDE[prod_short](includes/prod_short.md)].  

> [!NOTE]  
> De specifieke koppeling is afhankelijk van het bedrijfsdoel van het gegevensbestand dat wordt uitgewisseld, en van lokale variaties. Zelfs de SEPA-bankstandaard heeft lokale variaties. [!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt standaard de import van SEPA CAMT-bankafschriftbestanden.\-\-\- Dit wordt aangeduid door de code in de definitierecord voor gegevensuitwisseling **SEPA CAMT** op de pagina **Definities van gegevensuitwisseling**. Zie [Veldtoewijzing bij het importeren van SEPA CAMT-bestanden](across-field-mapping-when-importing-sepa-camt-files.md) voor informatie over de specifieke veldtoewijzing van deze CAMT SEPA-ondersteuning.  

### <a name="to-map-columns-in-the-data-file-to-fields-in-"></a><a name="to-map-columns-in-the-data-file-to-fields-in-"></a><a name=mapfields></a>Kolommen in de gegevensbestanden toewijzen aan velden in [!INCLUDE[prod_short](includes/prod_short.md)]

> [!TIP]
> Soms verschillen de waarden in de velden die u wilt toewijzen. In de ene zakelijke app is de taalcode voor de Verenigde Staten bijvoorbeeld 'V.S.', maar in de andere 'VS'. Dat betekent dat u de waarde moet transformeren wanneer u gegevens uitwisselt. Dit gebeurt door middel van transformatieregels die u voor de velden definieert. Meer informatie vindt u in [Transformatieregels](across-how-to-set-up-data-exchange-definitions.md#transformation-rules).

Vanaf releasewave 2 van 2022 kunt u ook groeperen op elk veld, de sleutelindex gebruiken om resultaten te sorteren en de nieuwe transformatietypen **Afronding** en **Veld opzoeken**.

1. Selecteer op het sneltabblad **Regeldefinities** de regel waarvoor u kolommen aan velden wilt toewijzen en kies vervolgens **Veldtoewijzing**. De pagina **Toewijzing gegevensuitwisseling** wordt geopend.  
2. Geef op het sneltabblad **Algemeen** de toewijzingsinstelling op door de velden in te vullen zoals beschreven in de volgende tabel.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Tabel-id**|Geef de tabel op met de velden waarheen of vanwaar gegevens worden uitgewisseld volgens de toewijzing.|  
    |**Gebruiken als tussentijdse tabel**|Geef op dat de tabel die u selecteert in het veld **Tabel-id** een tussentijdse tabel is waarin de geïmporteerde gegevens worden opgeslagen voordat deze aan de doeltabel worden toegewezen.<br /><br /> Meestal gebruikt u een tijdelijke tabel als de definitie van de gegevensuitwisseling wordt gebruikt om elektronische documenten te importeren en om te zetten, zoals leveranciersfacturen naar inkoopfacturen in [!INCLUDE[prod_short](includes/prod_short.md)]. Meer informatie vindt u in [Gegevens elektronisch uitwisselen](across-data-exchange.md).|  
    |**Naam**|Voer een naam in voor de instelling van de toewijzing.|  
    |**Sleutelindex**|Geef de sleutelindex op om de bronrecords te sorteren voordat deze worden geëxporteerd.|
    |**Codeunit toewijzing vooraf**|Geef de codeunit aan die de koppeling voorbereidt tussen velden in [!INCLUDE[prod_short](includes/prod_short.md)] en externe gegevens.|  
    |**Toewijzing van codeunit**|Geef de codeunit op die wordt gebruikt om de opgegeven kolommen of XML-gegevenselementen toe te wijzen aan velden in [!INCLUDE[prod_short](includes/prod_short.md)].|  
    |**Codeunit toewijzing achteraf**|Geef de codeunit op die de koppeling voltooit tussen velden in [!INCLUDE[prod_short](includes/prod_short.md)] en externe gegevens. **Opmerking:** wanneer de extensiefunctie AMC Banking 365 Fundamentals wordt gebruikt, zet de codeunit geëxporteerde gegevens uit [!INCLUDE[prod_short](includes/prod_short.md)] om in een algemene indeling die gereed is voor export. Voor het importeren zet de codeunit externe gegevens om in een indeling die gereed is voor importeren in [!INCLUDE[prod_short](includes/prod_short.md)].|
3. Op het sneltabblad **Veldtoewijzing** geeft u op welke kolommen zijn toegewezen aan welke velden in [!INCLUDE[prod_short](includes/prod_short.md)] door de velden in te vullen zoals beschreven in de volgende tabellen, afhankelijk van de vraag of het veld **Gebruiken als tussentijdse tabel** is ingeschakeld of niet.  
   * Met de schakelaar **Gebruiken als tussentijdse tabel** uitgeschakeld:

     |Veld|Omschrijving|  
     |--------------------------------- |---------------------------------------|  
     |**Kolomnr.**|Geef op voor welke kolom in het gegevensbestand u een toewijzing wilt definiëren.<br /><br /> U kunt alleen kolommen selecteren die worden vertegenwoordigd door regels op het sneltabblad **Kolomdefinities** op de pagina **Definitie van gegevensuitwisseling**.|
     |**Kolombijschrift**|Geef het bijschrift van de kolom in het externe bestand op, die aan het veld in het veld **Doeltabel-id** wordt toegewezen wanneer u een tussentijdse tabel gebruikt voor gegevensimport.|
     |**Veld-id**|Geef op aan welk veld de kolom in het veld **Kolomnr.** wordt toegewezen.<br /><br /> U kunt alleen velden selecteren die bestaan in de tabel die u hebt opgegeven in het veld **Tabel-id** op het sneltabblad **Algemeen**.|
     |**Veldbijschrift**|Geef het bijschrift op van het veld in het externe bestand dat aan het veld in het veld **Doeltabel-id** wordt toegewezen wanneer u een tussentijdse tabel gebruikt voor gegevensimport.|
     |**Optioneel**|Geef aan of de toewijzing moet worden overgeslagen als het veld leeg is. Als u deze optie niet selecteert, treedt een exportfout op als het veld leeg is.|  
     |**Transformatieregel**|Geef de regel op die geïmporteerde tekst omzet in een ondersteunde waarde voordat deze kan worden gekoppeld aan een opgegeven veld. Wanneer u een waarde in dit veld kiest, wordt dezelfde waarde ingevoerd in het veld **Transformatieregel** in **Veldtoewijzingsbuf. gegevensuitwisseling** en omgekeerd. Zie het volgende gedeelte voor meer informatie over beschikbare transformatieregels die kunnen worden toegepast.|
     |**Waarde overschrijven**|Geef op dat de huidige waarde wordt overschreven door een nieuwe waarde.|
     |**Prioriteit**|Geef de volgorde op waarin de veldtoewijzingen moeten worden verwerkt. De veldtoewijzing met het hoogste prioriteitsnummer wordt als eerste verwerkt.|
     |**Vermenigvuldigingsfactor**|Geef een vermenigvuldigingsfactor op die moet worden toegepast op numerieke gegevens, inclusief negatieve waarden.|

   * Met de schakelaar **Gebruiken als tussentijdse tabel** ingeschakeld:

     |Veld|Omschrijving|  
     |---------------------------------|---------------------------------------|  
     |**Kolomnr.**|Geef op voor welke kolom in het gegevensbestand u een toewijzing wilt definiëren.<br /><br /> U kunt alleen kolommen selecteren die worden vertegenwoordigd door regels op het sneltabblad **Kolomdefinities** op de pagina **Definitie van gegevensuitwisseling**.|
     |**Kolombijschrift**|Geef het bijschrift van de kolom in het externe bestand op, die aan het veld in het veld **Doeltabel-id** wordt toegewezen wanneer u een tussentijdse tabel gebruikt voor gegevensimport.|
     |**Doeltabel-id**|Geef de tabel op waaraan de waarde in het veld **Kolomomschrijving** wordt toegewezen wanneer u een tussentijdse tabel gebruikt voor gegevensimport.|
     |**Tabelbijschrift**|Geef de naam op van de tabel in het veld **Doeltabel-id**. Dit is de tabel waaraan de waarde in het veld **Kolomomschrijving** wordt toegewezen wanneer u een tussentijdse tabel gebruikt voor gegevensimport.|
     |**Doelveld-id**|Geef het veld in de doeltabel op waaraan de waarde in het veld **Kolomomschrijving** wordt toegewezen wanneer u een tussentijdse tabel gebruikt voor gegevensimport.|
     |**Veldbijschrift**|Geef de naam van het veld in de doeltabel op waaraan de waarde in het veld **Kolomomschrijving** wordt toegewezen wanneer u een tussentijdse tabel gebruikt voor gegevensimport.|
     |**Alleen valideren**|Geef op dat de toewijzing van element aan veld niet wordt gebruikt om gegevens te converteren, maar alleen om gegevens te valideren.|
     |**Transformatieregel**|Geef de regel op die geïmporteerde tekst omzet in een ondersteunde waarde voordat deze kan worden gekoppeld aan een opgegeven veld. Wanneer u een waarde in dit veld kiest, wordt dezelfde waarde ingevoerd in het veld **Transformatieregel** in **Veldtoewijzingsbuf. gegevensuitwisseling** en omgekeerd. Zie het volgende gedeelte voor meer informatie over beschikbare transformatieregels die kunnen worden toegepast.|
     |**Prioriteit**|Geef de volgorde op waarin de veldtoewijzingen moeten worden verwerkt. De veldtoewijzing met het hoogste prioriteitsnummer wordt als eerste verwerkt.|

4. Geef op het sneltabblad **Veldgroepering** regels op die u wilt gebruiken om uw velden te groeperen wanneer u het bestand maakt door de velden in te vullen zoals beschreven in de onderstaande tabel.  

     |Veld|Omschrijving|  
     |--------------------------------- |---------------------------------------|  
     |**Veld-id**|Geef het nummer op van het veld in het externe bestand dat wordt gebruikt om te groeperen, dit veld moet worden ingesteld door de gebruiker.|
     |**Veldbijschrift**|Geef het bijschrift op van het veld in het externe bestand dat wordt gebruikt voor groepering.|

## <a name="transformation-rules"></a><a name="transformation-rules"></a>Transformatieregels

Als de waarden in de velden die u toewijst, verschillen, moet u transformatieregels gebruiken voor definities van gegevensuitwisseling om ze hetzelfde te maken. U definieert transformatieregels voor gegevensuitwisselingsdefinities door een bestaande definitie te openen of een nieuwe definitie te maken en vervolgens op het sneltabblad **Regeldefinities** de optie **Beheren** en **Veldtoewijzing** te kiezen. Er zijn vooraf gedefinieerde regels beschikbaar, maar u kunt ook uw eigen regels maken. De volgende tabel beschrijft de soorten transformaties die u kunt uitvoeren.

|Optie|Omschrijving|
|---------|---------|
|**Hoofdletters**|Alle letters zijn hoofdletters.|
|**Kleine letters**|Alle letters zijn kleine letters.|
|**Beginhoofdletters**|Elk woord heeft een beginhoofdletter.|
|**Afkappen**|Verwijder spaties voor en na de waarde.|
|**Subtekenreeks**|Transformeer een specifiek gedeelte van een waarde. Als u wilt aangeven waar de transformatie moet starten, kiest u een **Beginpositie** of **Begintekst**. De beginpositie is een nummer dat staat voor het eerste te transformeren teken. De begintekst is de letter direct vóór de te vervangen letter. Als u met de eerste letter in de waarde wilt beginnen, gebruikt u in plaats daarvan een beginpositie. Als u wilt opgeven waar u de transformatie wilt stoppen, kiest u **Lengte** (het aantal tekens dat moet worden vervangen) of **Eindtekst** (het teken direct na het laatste te transformeren teken).|
|**Vervangen**|Zoek een waarde en vervang deze door een andere. Deze transformatie is handig wanneer u eenvoudige waarden vervangt, zoals een bepaald woord.|
|**Reguliere expressie - Vervangen**|Gebruik een reguliere expressie als onderdeel van een opdracht voor zoeken en vervangen. Deze transformatie is handig wanneer u meerdere of meer complexe waarden wilt vervangen.|
|**Niet-alfanumerieke tekens verwijderen**|Verwijder tekens die geen letters of cijfers zijn, zoals symbolen of speciale tekens.|
|**Datumindeling**|Geef op hoe datums moeten worden weergegeven. U kunt bijvoorbeeld DD-MM-JJJJ transformeren naar JJJJ-MM-DD.|
|**Decimale notatie**|Definieer regels voor de plaatsing van decimalen en afrondingsprecisie.|
|**Reguliere expressie - Afstemmen**|Gebruik een reguliere expressie om een of meer waarden te vinden. Deze regel is vergelijkbaar met de opties **Subtekenreeks** en **Reguliere expressie - Vervangen**.|
|**Aangepast**|Deze transformatieregel is een geavanceerde optie waarvoor u de hulp van een ontwikkelaar moet inroepen. Het maakt een integratie-gebeurtenis mogelijk waarop u zich kunt abonneren als u uw eigen transformatiecode wilt gebruiken. Zie het gedeelte hieronder als u een ontwikkelaar bent en deze optie wilt gebruiken.|
|**Datum- en tijdindeling**|Definieer hoe de huidige datum en het tijdstip van de dag worden weergegeven.|
|**Veld opzoeken**|Gebruik velden uit verschillende tabellen. Als u dit wilt gebruiken moet u enkele regels volgen. Gebruik eerst **Tabel-id** om de id op te geven van de tabel die de record voor het opzoeken van velden bevat. Geef vervolgens in het veld **Bronveld-id** de id op van het veld dat de record voor het opzoeken van velden bevat. Geef tot slot in het veld **Doelveld-id** de id op van het veld om de record voor het opzoeken van velden te vinden. Gebruik eventueel het veld **Regel voor veldopzoekactie** om het type veldopzoekactie op te geven. Voor het veld **Doel** wordt de waarde van het veld **Doelveld-id** gebruikt, zelfs als het leeg is. Voor het veld **Origineel als doel leeg is**, wordt de oorspronkelijke waarde gebruikt als het doel leeg is.|
|**Afronden**|Rond de waarde in dit veld af met behulp van enkele aanvullende regels. Geef eerst in het veld **Precisie** een afrondingsprecisie op. Geef vervolgens in het veld **Richting** de afrondingsrichting op.|

> [!NOTE]  
> Meer informatie over datum- en tijdnotatie vindt u in [Standaardnotaties voor datum en tijd](/dotnet/standard/base-types/standard-date-and-time-format-strings).

### <a name="tip-for-developers-example-of-the-custom-option"></a><a name="tip-for-developers-example-of-the-custom-option"></a>Tip voor ontwikkelaars: voorbeeld van de aangepaste optie

Het volgende voorbeeld laat zien hoe u uw eigen transformatiecode implementeert.

```AL
codeunit 60100 "Hello World"
{
    [EventSubscriber(ObjectType::Table, Database::"Transformation Rule", 'OnTransformation', '', false, false)]
    procedure OnTransformation(TransformationCode: Code[20]; InputText: Text; var OutputText: Text)
    begin
        if TransformationCode = 'CUST' then
            OutputText := InputText + ' testing';
    end;
}
```

Nadat u uw regels hebt gedefinieerd, kunt u ze testen. Op het sneltabblad **Test** voert u een voorbeeld in van een waarde die u wilt transformeren en vervolgens controleert u de resultaten door **Bijwerken** te kiezen.

## <a name="export-a-data-exchange-definition-as-an-xml-file-for-use-by-others"></a><a name="export-a-data-exchange-definition-as-an-xml-file-for-use-by-others"></a>De definitie van een gegevensuitwisseling exporteren als een XML-bestand voor gebruik door anderen

Wanneer u de definitie van gegevensuitwisseling hebt gemaakt voor een specifiek gegevensbestand, kunt u de definitie van gegevensuitwisseling exporteren als XML-bestand dat u kunt importeren. Deze taak wordt in de volgende procedure beschreven.  

1. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gegevensuitwisselingsdefinities** in en kies vervolgens de gerelateerde koppeling.  
2. Selecteer de definitie van de gegevensuitwisseling die u wilt exporteren.  
3. Kies de actie **Definitie van gegevensuitwisseling exporteren**.  
4. Sla het XML-bestand dat de definitie van de gegevensuitwisseling vertegenwoordigt, op een geschikte locatie op.  

    Als er al een definitie voor gegevensuitwisseling is gemaakt, hoeft u slechts het XML-bestand in het kader voor gegevensuitwisseling te importeren. Deze taak wordt in de volgende procedure beschreven.  

## <a name="import-an-existing-data-exchange-definition"></a><a name="import-an-existing-data-exchange-definition"></a>Een bestaande definitie van gegevensuitwisseling importeren

1. Sla het XML-bestand dat de definitie van de gegevensuitwisseling vertegenwoordigt, op een geschikte locatie op.  
2. Kies het pictogram ![Lampje dat de functie Vertel me 1 opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gegevensuitwisselingsdefinities** in en kies vervolgens de gerelateerde koppeling.  
3. Kies de actie **Definitie van gegevensuitwisseling importeren**.  
4. Kies het bestand dat u in stap 1 hebt opgeslagen.  

## <a name="see-also"></a><a name="see-also"></a>Zie ook

[Gegevensuitwisseling instellen](across-set-up-data-exchange.md)  
[Verzending en ontvangst van elektronische documenten instellen](across-how-to-set-up-electronic-document-sending-and-receiving.md)  
[Betalingen incasseren met automatische incasso via SEPA](finance-collect-payments-with-sepa-direct-debit.md)  
[Betalingen doen met de extensie AMC Banking 365 Fundamentals of SEPA-kredietoverdracht](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)  
[Inkomende documenten](across-income-documents.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
