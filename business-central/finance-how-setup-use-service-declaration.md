---
title: De extensie Servicedeclaratie instellen en gebruiken
description: Leer hoe u Servicedeclaratie (Intrastat voor Services) instelt en gebruikt om servicehandel te rapporteren met bedrijven in andere EU-landen/regio's.
author: altotovi
ms.author: altotovi
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/21/2022
ms.custom: bap-template
ms.search.keywords: 'electronic document, Intrastat, trade, EU, service, declaration,'
ms.search.form: '30, 76, 5010, 5022, 5023, 5024, 5800'
---
# <a name="the-service-declaration-extension"></a>De extensie Servicedeclaratie

In sommige EU-landen/regio's eisen de autoriteiten dat bedrijven de uitvoer van diensten naar andere EU-landen rapporteren. Met de extensie **Servicedeclaratie** kunt u informatie verzamelen over servicehandel in de EU en deze rapporteren aan de autoriteiten. Hoewel het **Servicedeclaratie** heet, kunt u het ook gebruiken als **Intrastat voor services**. Deze extensie is beschikbaar voor alle EU-landen/regio's als een W1-versie en kan in de huidige vorm in België worden gebruikt. Voor andere landen/regio's is een land/regio-specifieke extensie vereist. Als een land/regio alleen een ander formaat nodig heeft, kunt u de rapportconfiguratie in het **Raamwerk voor gegevensuitwisseling** gebruiken om het formaat te wijzigen.

## <a name="enable-the-service-declaration-extension"></a>De extensie Servicedeclaratie inschakelen

Nadat u de extensie in uw omgeving hebt geïnstalleerd, moet u deze inschakelen.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Functiebeheer** in en kies vervolgens de gerelateerde koppeling.
2. Zoek **Functie: Gebruik inschakelen van servicedeclaratie (Intrastat voor Services)** en kies in het veld **Geactiveerd voor** **Alle gebruikers**. Meer informatie over functiebeheer op [Aankomende functies van tevoren inschakelen](/dynamics365/business-central/dev-itpro/administration/feature-management) in de beheer-inhoud.
3. Wanneer u de functie inschakelt, moet u de stappen in het installatieproces volgen via de installatiewizard. De meeste velden zijn standaard geconfigureerd.
4. Voeg alleen **Servicetransactietypen** in de tweede stap toe door de optie **De pagina met servicetransactietypen openen om de lijst met codes op te geven** te kiezen.
5. Voordat u begint, controleert u het **Totaal aantal codes** om te zien hoeveel typen servicetransacties er al zijn opgegeven.
6. Kies **Voltooien** in de laatste stap om de configuratie te voltooien.

## <a name="set-up-the-service-declaration-extension"></a>De extensie Servicedeclaratie instellen

U kunt de extensie handmatig instellen of met behulp van een rapportagebestand in Definities voor gegevensuitwisseling.

### <a name="to-set-up-service-declaration-manually"></a>Servicedeclaratie handmatig instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Servicedeclaratie instellen** in en kies vervolgens de gerelateerde koppeling.
2. Configureer op het sneltabblad **Algemeen** de velden zoals beschreven in de volgende tabel:

    |Veld  |Omschrijving  |
    |---------|---------|
    |**Nummerreeks van declaratie**     | Specificeert de nummerreeks die moet worden gebruikt om id's aan nieuwe records toe te wijzen.        |
    |**Artikeltoeslagen rapporteren**  | Geeft aan of artikeltoeslagen moeten worden gerapporteerd. Indien geactiveerd controleert [!INCLUDE [prod_short](includes/prod_short.md)] de servicetransactiecode op artikelkosten en neemt deze op in servicedeclaraties.        |
    |**Nr. van order/factuur-klant**     | Specificeert de klant die moet worden gebruikt om zijn of haar land/regio-code te vergelijken met de land/regio-code op de pagina **Bedrijfsgegevens**. Alleen documenten waarbij deze twee codes verschillend zijn, worden opgenomen in de servicedeclaratie.<br><br>* **Factureren aan**: gebruik de land/regio-code van de **factuurklant** <br<br>* **Verkopen aan**: gebruik de land/regio-code van de **orderklant**.        |
    |**Koop/betalings-leverancier**  | Specificeert welke leverancier moet worden gebruikt om zijn of haar land/regio-code te vergelijken met de land/regio-code op de pagina **Bedrijfsgegevens**. Alleen documenten waarbij deze twee codes verschillend zijn, worden opgenomen in de servicedeclaratie.<br><br> * **Kopen van**: gebruik de land/regio-code van de **Orderleverancier**. <br><br> * **Betalen aan**: gebruik de land/regio-code van de **factuurleverancier**.         |
    |**Code van definitie van gegevensuitwisseling**  | Hiermee wordt de code opgegeven van de gegevensuitwisselingsdefinitie die wordt gebruikt om het geëxporteerde bestand voor de servicedeclaratie te genereren.        |
    |**Btw-nr. activeren**     |  Hiermee wordt opgegeven of het **btw-nummer** is geactiveerd voor de servicedeclaratie.       |

3. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Servicetransactietypen** in en kies vervolgens de gerelateerde koppeling.
4. Geef op de regels **Codes** en **Beschrijvingen** op voor de servicetransactietypen die u gaat gebruiken.

### <a name="set-up-a-reporting-file"></a>Een rapportagebestand instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Definities van gegevensuitwisseling** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Geef op het sneltabblad **Algemeen** de definitie van gegevensuitwisseling op door het type gegevensbestand, kolomscheidingsteken, gerelateerde code-eenheden en XMLport op te geven en de andere velden in te vullen.
4. Beschrijf op het sneltabblad **Regeldefinities** de opmaak van regels in het gegevensbestand door de velden in te vullen die zijn gebaseerd op het veld **Regeltype** en waar u het aantal kolommen voor deze regel moet definiëren.
5. Vul op het snelttabblad **Kolomdefinities** de regel in voor elke geplande kolom.
6. Kies de actie **Veldtoewijzing** op het sneltabblad **Regeldefinities** om de pagina **Veldtoewijzing** te openen.
7. Maak de nieuwe invoer en kies op het sneltabblad **Algemeen** de juiste **tabel-id** (kies **5024** voor **Servicedeclaratieregel**) en vul dan de velden als volgt in:
   1. Geef in het veld **Sleutelindex** de sleutelindex op om de bronrecords te sorteren alvorens te exporteren.
   2. Selecteer de juiste **Toewijzing van codeunit**.
8. Voeg op het sneltabblad **Veldtoewijzing** de kolommen toe die u eerder hebt geconfigureerd op het sneltabblad **Kolomdefinities** en voeg dan het volgende toe:
   1. Geef voor elk van de kolommen de **Veld-id** op.
   2. Geef indien nodig de **Transformatieregel** voor elke kolom op. De regel transformeert geïmporteerde tekst in een ondersteunde waarde voordat deze kan worden toegewezen aan een opgegeven veld in [!INCLUDE[prod_short](includes/prod_short.md)]. Wanneer u een waarde in dit veld kiest, wordt de exacte waarde ingevoerd in het veld **Transformatieregel** in de tabel **Veldtoewijzingsbuf. gegevensuitwisseling** en omgekeerd.
9. Als u invoer wilt groeperen op basis van kolommen, kunt u op het sneltabblad **Veldgroepering** de velden kiezen die u wilt gebruiken voor groepering.

> [!NOTE]
> [!INCLUDE[prod_long](includes/prod_long.md)] wordt geleverd met een vooraf geconfigureerde definitie van gegevensuitwisseling voor **Servicedeclaratie** voor alle gelokaliseerde landen/regio's. Voor meer informatie over het maken van een nieuwe definitie van gegevensuitwisseling raadpleegt u [Definities van gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md).

## <a name="other-related-configurations"></a>Andere gerelateerde configuraties

Voordat u de extensie Servicedeclaratie gebruikt, configureert u enkele velden voor artikelen, resources en artikeltoeslagen.

### <a name="items"></a>Artikelen

Informatie met betrekking tot Servicedeclaratie instellen op artikelkaartpagina's:

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer het artikel dat u wilt configureren.
3. Vouw het sneltabblad **Artikel** uit en configureer de volgende velden:
   1. Kies in het veld **Soort** de optie **Service**.
   2. Geef in het veld **Code van servicetransactietype** de code op voor een **servicetransactietype**.
   3. Als u dit serviceartikel niet wilt opnemen in servicedeclaraties, kiest u het veld **Uitsluiten van servicedeclaratie**.

### <a name="resources"></a>Resources

Informatie met betrekking tot Servicedeclaratie instellen op resourcekaartpagina's:

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Resources** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de resource die u wilt configureren.
3. Vouw het sneltabblad **Algemeen** uit en configureer de volgende velden:
   1. Geef in het veld **Code van servicetransactietype** de code op voor een **servicetransactietype**.
   2. Als u deze resource niet wilt opnemen in servicedeclaraties, kiest u het veld **Uitsluiten van servicedeclaratie**.

### <a name="item-charges"></a>Artikeltoeslagen

Informatie met betrekking tot Servicedeclaratie instellen voor artikeltoeslagen:

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikeltoeslagen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de artikeltoeslag die u wilt configureren.
3. Geef in het veld **Code van servicetransactietype** de code op voor een **servicetransactietype**.
4. Als u deze artikeltoeslag niet wilt opnemen in servicedeclaraties, selecteert u het veld **Uitsluiten van servicedeclaratie**.

## <a name="create-new-service-declaration"></a>Een nieuwe servicedeclaratie maken

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Servicedeclaraties** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Vul de volgende velden op het sneltabblad **Algemeen** in:
    1. Geef in het veld **Configuratiecode** de configuratiecode op die wordt gebruikt om regels voor te stellen en bestanden te maken. U moet er een kiezen als een **Servicedeclaratie**.
    2. Geef in de velden **Begindatum** en **Einddatum** de begin- en einddatum op van de periode die moet worden opgenomen in de servicedeclaratie.
4. Kies de actie **Regels voorstellen** om een batchverwerking te starten die regels uit documenten verzamelt en de servicedeclaratieregels invult.

De batchverwerking haalt alle boekingen op uit toepasselijke inkoop- en verkoopdocumenten in de vereiste periode en voegt ze toe aan de servicedeclaratieregels. Wijs de velden in regels aan om een korte omschrijving te lezen.

## <a name="modify-a-service-declaration"></a>Een servicedeclaratie wijzigen

Indien nodig kunt u de regels wijzigen of nieuwe toevoegen.

1. Kies op de pagina **Servicedeclaratie** op het sneltabblad **Regels** de actie **Nieuwe regel**.
2. Kies in het veld **Documentsoort** de optie met betrekking tot het document dat u wilt gebruiken.
3. Vul op basis van het **Documentsoort** het veld **Documentnr.** in.
4. Vul de overige velden in.

## <a name="overview-the-service-declaration-lines"></a>Overzicht van de servicedeclaratieregels

Nadat u een servicedeclaratie hebt gemaakt, gebruikt u de actie **Overzicht** om een overzicht te krijgen van de servicedeclaratieregels. U kunt de regels op dezelfde manier groeperen en samenvatten als het geëxporteerde bestand. U kunt de regels ook openen in Excel.

## <a name="report-service-declaration-in-a-file"></a>Servicedeclaratie rapporteren in een bestand

U kunt de servicedeclaratie als bestand indienen op basis van de eisen van verschillende lokale autoriteiten. Een bestand maken:

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Servicedeclaraties** in en kies vervolgens de gerelateerde koppeling.
2. Kies de servicedeclaratie die u als bestand wilt rapporteren.
3. Als u dit nog niet hebt gedaan, vult u de servicedeclaratie handmatig in of kiest u de actie **Regels voorstellen**.
4. Kies de actie **Bestand maken**.
5. Het servicedeclaratiebestand wordt opgeslagen in de vereiste indeling.

## <a name="other-considerations"></a>Overige overwegingen

Als u de extensie **Servicedeclaratie** gebruikt, zijn er nog een paar dingen waarmee u rekening moet houden. Het is bijvoorbeeld belangrijk dat uw groepen voldoen aan eisen van autoriteiten. Het is ook belangrijk dat services correct worden vermeld op verkoop- en inkoopdocumenten.

### <a name="grouping-lines"></a>Regels groeperen

Op serviceaangifteregels is er geen groepering op veld. Alle vermeldingen worden gekopieerd van het originele document als bron.

Groepering vereist door autoriteiten wordt verstrekt in het geëxporteerde bestand. U moet de groepen configureren in de **Definitie van gegevensuitwisseling**, die volledig configureerbaar is. Meer informatie vindt u in [Definities van gegevensuitwisseling instellen](across-how-to-set-up-data-exchange-definitions.md).

### <a name="using-services-in-document-lines"></a>Services gebruiken op documentregels

Wanneer u een inkoop-, verkoop- of servicefactuur maakt, vindt u twee velden met betrekking tot servicedeclaraties op de regels ervan. Beide velden worden ingevuld met de standaardwaarden van uw artikel-, resource- of artikeltoeslaginstellingen.

- **Code van servicetransactietype**: geeft de code op voor een servicetransactietype.
- **Van toepassing op servicedeclaratie**: hiermee wordt opgegeven of een artikel of resource van toepassing is op een servicedeclaratie.

U kunt de waarden in deze velden wijzigen, maar als u het veld **Van toepassing op servicedeclaratie** selecteert, moet u een waarde opgeven in het veld **Code van servicetransactietype**. Als u dat niet doet, kunt u het document niet boeken.

Als u een waarde opgeeft in het veld **Code van servicetransactietype**, maar het veld **Van toepassing op servicedeclaratie** niet selecteert, kunt u het document boeken, maar wordt de regel niet berekend.

## <a name="see-related-training-at-microsoft-learn"></a>Zie gerelateerde training op [Microsoft Learn](/learn/modules/process-intrastat-dynamics-365-business-central/index).

## <a name="see-also"></a>Zie ook

[Intrastat-rapportage instellen](finance-how-setup-report-intrastat.md)
[Intrastat-rapportage in Business Central](finance-how-report-intrastat.md)  
[Financieel beheer](finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
