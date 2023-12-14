---
title: IC-transactieboeking instellen
description: Leer hoe u een IC-partnerschap instelt.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bnielse
ms.topic: how-to
ms.date: 09/27/2023
ms.custom: bap-template
ms.search.keywords: 'IC, group, consolidation, affiliate, subsidiary'
ms.search.form: '605, 620, 602, 603, 601, 600, 652, 653, 606, 607, 609, 608, 621'
---
# <a name="set-up-intercompany-transactions"></a>IC-transacties beheren

IC-partnerschappen maken het gemakkelijker om boekhoudprocessen af te handelen wanneer twee of meer dochterondernemingen van een bedrijf regelmatig zaken met elkaar doen. Partners kunnen transacties, zoals verkopen en inkopen, uitwisselen en handmatig of automatisch afhandelen. Wanneer een partner bijvoorbeeld een verkoopdagboekregel naar een andere partner stuurt, wordt er een inkoopdagboekregel gemaakt voor de ontvangende partner.

Het IC-rekeningschema kan bijvoorbeeld een versie van het rekeningschema van de synchronisatiepartner zijn. Elke partner wijst hun rekeningen toe aan het IC-rekeningschema. Elke partner wijst ook zijn dimensies en dimensiewaarden toe aan de IC-dimensies.

> [!NOTE]
> In releasewave 1 van 2023 hebben we een verbeterde pagina **Intercompany-instelling** geïntroduceerd. De nieuwe pagina maakt het gemakkelijker om een IC-partnerschap in te stellen door alle instellingstaken op één pagina te consolideren. Als u een nieuwe gebruiker van [!INCLUDE [prod_short](includes/prod_short.md)] bent, gebruikt u de nieuwe ervaring al. Als u een bestaande klant bent, kan uw beheerder de functieschakelaar **Automatisch IC-dagboektransacties accepteren** inschakelen op de pagina **Functiebeheer**.
>
> Bij de taken in dit artikel wordt ervan uitgegaan dat de functieschakelaar is ingeschakeld. Als u al een IC-partnerschap hebt ingesteld, kunt u dit blijven gebruiken.

## <a name="before-you-start"></a>Voordat u begint

Voordat u begint met het instellen van uw IC-partnerschap, moet u een aantal beslissingen nemen.

|Beslissing  |Omschrijving  |
|---------|---------|
|Welk rekeningschema moet de basis zijn voor het IC-rekeningschema?     | Alle bedrijven in het partnerschap moeten hetzelfde IC-rekeningschema gebruiken. U kunt uw IC-rekeningschema baseren op het rekeningschema van een van de bedrijven in het partnerschap of een nieuw IC-rekeningschema maken. U wijst de rekeningen die u in het partnerschap wilt gebruiken in beide richtingen toe, zodat elke partner transacties op de juiste rekeningen verzendt en ontvangt. Meer informatie over het instellen van het IC-rekeningschema vindt u op [Het IC-rekeningschema instellen](#set-up-the-intercompany-charts-of-accounts).         |
|Welke dimensies moeten de basis vormen voor de IC-dimensies?     | Als u IC-dimensies gebruikt, moeten deze voor alle bedrijven in het partnerschap hetzelfde zijn. Nadat u uw IC-dimensies hebt opgegeven, wijst u hun dimensiewaarden toe. Ga voor meer informatie over het toewijzen van dimensiewaarden naar [IC-dimensies instellen](#set-up-intercompany-dimensions).        |
|Welke partners zijn klanten of leveranciers, of beide?     |  Meer informatie over het instellen van klanten en leveranciersbedrijven in een IC-partnerschap vindt u op [IC-partners instellen als klanten en leveranciers](#set-up-intercompany-partners-as-customers-and-vendors).       |
|Wilt u bankrekeningen opgeven om te gebruiken in het partnerschap?| U kunt het proces van het registreren van betalingstransacties versnellen door de bankrekening op te geven die voor elk partnerbedrijf moet worden gebruikt. Ga voor meer informatie naar [De bankrekeningen opgeven die moeten worden gebruikt voor IC-partners](#specify-the-bank-accounts-to-use-for-intercompany-partners). |
|Hoe wilt u de bedrijven in het partnerschap identificeren?     | Alle partijen moeten het eens worden over een unieke IC-partneridentificatiecode voor elk bedrijf. U wijst de code toe aan klanten- en leverancierskaarten om gerelateerde transacties te identificeren. Ga voor meer informatie over identifiers naar [Nummerreeksen maken](ui-create-number-series.md).        |
|Hoe wilt u artikelnummers verwerken?     | Als IC-regels artikelen bevatten, kunt u uw eigen artikelnummer gebruiken of kunt u de artikelnummers van uw partner instellen voor elk gewenst artikel. Dit kunt u doen in het veld **Artikelnr. leverancier** of in het veld **Gemeenschappelijk artikelnr.** op de artikelkaart. U kunt ook de actie **Artikelreferentie** gebruiken om de nummers van uw artikelen toe te wijzen aan de omschrijvingen van de artikelen van uw IC-partners. Ga voor meer informatie over artikelreferenties naar [Artikelreferenties gebruiken](inventory-how-use-item-cross-refs.md).        |
|Zijn er resources bij betrokken?     | Als IC-verkooptransacties resources zullen bevatten, moet u het veld **IC-partner Ink. Grootb.rek.nr.** invullen op de resourcekaart van elke resource. Het veld bevat het nummer van de IC-grootboekrekening waarnaar het bedrag voor deze resource wordt geboekt in het partnerbedrijf. Ga voor meer informatie over resources naar [Resources instellen](projects-how-setup-resources.md).<br><br>**OPMERKING**<br>Intercompany-inkooptransacties die resources, vaste activa en artikeltoeslagen omvatten, worden niet volledig ondersteund. In het partnerbedrijf is het veld **Regelsoort** leeg op inkoopdocumentregels die deze entiteiten bevatten. U moet het veld handmatig bijwerken.        |

## <a name="overview-of-the-steps-to-get-started"></a>Overzicht van de stappen om aan de slag te gaan

Gebruik de pagina **Intercompany-instelling** om de volgende componenten van IC-transacties in te stellen:

* De IC-instellingen van uw bedrijf.
* Het bedrijf dat de synchronisatiepartner wordt.
* Het IC-rekeningschema dat alle partners gebruiken om transacties uit te wisselen.
* De toewijzingen tussen rekeningen in het rekeningschema en het IC-rekeningschema voor inkomende en uitgaande transacties voor elke partner.
* De te gebruiken IC-dimensies en dimensiewaarden en hoe ze worden toegewezen aan dimensies voor elke partner.
* De bedrijven die de IC-partners zijn.
* De bedrijven die leverancier of klant zijn, of beide.

## <a name="set-up-a-synchronization-partner"></a>Een synchronisatiepartner instellen

Alle partners moeten hetzelfde IC-rekeningschema gebruiken en, indien nodig, dezelfde IC-dimensies. U kunt tijd besparen bij het instellen van het partnerschap door het rekeningschema en de dimensies van een van de partners te gebruiken als basis voor het IC-rekeningschema en de dimensies. Het bedrijf dat u als basis gebruikt, wordt de *synchronisatiepartner* genoemd. Meestal is de synchronisatiepartner het hoofdkantoor, maar dat hoeft niet zo te zijn.

Op de pagina **Intercompany-instelling** specificeert elke partner de synchronisatiepartner in het veld **Synchronisatiepartner**. Daarna worden het IC-rekeningschema en de IC-dimensies automatisch voor hen opgegeven, op basis van de instellingen voor de synchronisatiepartner. De partners gebruiken vervolgens de pagina's **Toewijzing intercompany-rekeningschema** en **IC-dimensietoewijzing** om hun rekeningschema en dimensies toe te wijzen aan het IC-rekeningschema en de IC-dimensies, en andersom. 

> [!NOTE]
> Het is belangrijk om rekeningen en dimensies in beide richtingen toe te wijzen. Dat wil zeggen aan het IC-rekeningschema en de IC-dimensies, en van daaruit ook aan uw rekeningen en dimensies.

### <a name="connect-with-partners-in-another-tenant-or-environment"></a>Contact met partners maken in een andere tenant of omgeving

Als [!INCLUDE [prod_short](includes/prod_short.md)] van een of meer partners zich in een andere tenant of omgeving bevindt, zijn er een paar extra stappen om de verbinding tot stand te brengen. De stappen zijn van toepassing op alle partners in een andere tenant of omgeving.

* Stel [!INCLUDE [prod_short](includes/prod_short.md)] als een geregistreerde app in Azure Portal in.
* Voeg de app-registratie toe en schakel deze in [!INCLUDE [prod_short](includes/prod_short.md)] in.
* Wissel informatie uit over hun intercompany-instellingen. Elke partner kan deze informatie verkrijgen uit de begeleide instelling **Instellingen van meerdere omgevingen voor IC-partner**.

   |Kopieer vanuit de instellingen van de partner  |Kopieer naar uw instelling  |
   |---------|---------|
   |Huidige verbindings-URL     |Verbindings-URL van IC-partner         |
   |Huidige bedrijfs-id     |Bedrijfs-id van IC-partner         |
   |IC-id     |IC-id van IC-partner         |
   |Bedrijfsnaam     |Bedrijfsnaam van IC-partner         |

* Wissel de volgende verificatie-instellingen uit, zodat [!INCLUDE [prod_short](includes/prod_short.md)] kan verifiëren wanneer er verbinding wordt gemaakt. Elke partner kan deze informatie verkrijgen via hun geregistreerde app. Voor meer informatie over het maken van een geregistreerde app gaat u naar [Een geregistreerde app maken in Azure Portal](#create-a-registered-app-in-azure-portal).  

  * Client-id
  * Clientgeheim
  * Tokeneindpunt
  * Omleidings-URL

Voer in alle bedrijven de begeleide instelling **Instellingen van meerdere omgevingen voor IC-partner** uit om de informatie op te geven. Om de guide te starten, gebruikt u op de pagina **IC-partner** de actie **Instelling van extern verbinden**.

#### <a name="create-a-registered-app-in-azure-portal"></a>Maak een geregistreerde app in Azure Portal

Dit proces is alleen nodig als u verbinding wilt maken met een partner wiens [!INCLUDE [prod_short](includes/prod_short.md)] zich in een andere tenant of omgeving bevindt.

> [!TIP]
> Het is een goed idee om een teksteditor geopend te hebben, zoals Kladblok, terwijl u uw geregistreerde app maakt. U heeft een deel van deze informatie nodig wanneer u de begeleide instelling **Instellingen van meerdere omgevingen voor IC-partner** uitvoert, dus het is prettig om de informatie bij de hand te hebben.

1. Ga naar [Azure Portal](https://portal.azure.com/#home).
2. Kies de service **Microsoft Entra ID**.
3. Kies in het navigatievenster de optie **App-registraties**.
4. Kies op de pagina **App-registraties** **nieuwe registratie**.
5. Geef de nieuwe toepassing een naam.
6. Kies het accounttype **Accounts in elke organisatorische directory (Elke Microsoft Entra ID-tenant - Multitenant)**.
7. Voor de omleidings-URI kiest u in het veld **Een platform selecteren** **Web** en geeft u vervolgens de URI op. Bijvoorbeeld \**https://businesscentral.dynamics.com/OAuthLanding.htm**.

  Als u met een ingesloten ISV werkt, heeft u mogelijk een andere URI nodig.

8. Registreer de app..
9. Op de pagina **IC-app** kiest u in het navigatievenster **API-machtigingen**.
10. Kies de actie **Een machtiging toevoegen**.
11. Kies op het tabblad **Microsoft API's** **Dynamics 365 Business Central**.
12. In het deelvenster **API-machtigingen aanvragen** kiest u **Toepassingsmachtigingen** en kiest u vervolgens de machtiging **API.ReadWrite.All**.
13. Op de **IC-app | API-machtigingen** kiest u de actie **Beheerdertoestemming verlenen voor Contoso** en geeft u vervolgens toestemming.
14. Kies in het navigatiedeelvenster **Certificaten en geheimen**.
15. Kies het tabblad **Clientgeheimen** en kies vervolgens **Nieuw clientgeheim**.
16. Voer in het deelvenster **Een clientgeheim toevoegen** een naam in voor het geheim en geef op wanneer het geheim verloopt.

  > [!NOTE]
  > Alle partners die zich in verschillende omgevingen bevinden, moeten het geheim vernieuwen voordat het verloopt.

  > [!IMPORTANT]
  > Kopieer de id in het veld **Waarde** voordat u de pagina **IC-app | Certificaten en geheimen** verlaat. U hebt het in een latere stap nodig en het is niet meer beschikbaar nadat u de pagina hebt verlaten. Plak de waarde bijvoorbeeld in een teksteditor.

17. Kies in het navigatiedeelvenster **Overzicht**.
18. Kopieer de waarde van het veld **Id van toepassing (client)**. Plak de waarde bijvoorbeeld in een teksteditor.
19. Kies de actie **Eindpunten** en kopieer vervolgens de waarde in het veld **OAuth 2.0-tokeneindpunt (v2)**. Plak de waarde bijvoorbeeld in een teksteditor.
20. Kopieer de waarde in het veld **Id van directory (tenant)**. Plak de waarde bijvoorbeeld in een teksteditor.
21. Vervang **organisaties** in de tokenwaarde die u heeft gekopieerd, door de waarde die u heeft gekopieerd uit het veld **Id van directory (tenant)** in de vorige stap.

#### <a name="add-and-enable-your-registered-app-in-business-central"></a>Voeg uw geregistreerde app toe en schakel deze in Business Central in

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Microsoft Entra-toepassingskaart** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de vereiste velden in. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]
3. Kies in het veld **Status** de optie **Geactiveerd**. 
4. Kies de actie **Toestemming geven**. 
5. Kies in het veld **Machtigingenset** de machtigingenset **API - IC meerdere omgevingen**.

## <a name="set-up-the-intercompany-charts-of-accounts"></a>Het IC-rekeningschema instellen

Alle partners moeten hetzelfde IC-rekeningschema gebruiken en de rekeningen in hun eigen rekeningschema hieraan toewijzen. Als het rekeningschema voor uw bedrijf het IC-rekeningschema voor uw partnerbedrijven definieert, volgt u de stappen in deze sectie.

Als u een XML-bestand gebruikt dat het IC-rekeningschema bevat, volgt u de stappen in [Een IC-rekeningschema importeren of exporteren](intercompany-how-setup.md#import-or-export-an-intercompany-chart-of-accounts).  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), pictogram, voer **Intercompany-instelling** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **IC-rekeningschema**.
3. Om accounts toe te voegen voert u een van de volgende handelingen uit op de pagina **IC-rekeningschema**:
    * Kies **Nieuw** en voer vervolgens elke rekening in op een regel op de pagina.  
    * Als uw IC-rekeningschema identiek is aan uw normale rekeningschema of erop lijkt, kunt u de pagina automatisch invullen door de actie **Kopiëren uit rekeningschema** te kiezen. U kunt de nieuwe regels zo nodig bewerken.
    * Als u een IC-rekeningschema hebt ingesteld voor een synchronisatiepartner, gebruikt u de actie **Synchronisatie instellen** om die accounts te kopiëren.

    > [!TIP]
    > Als u het IC-rekeningschema van een synchronisatiepartner kopieert, kunt u de actie **Synchronisatie instellen** gebruiken om uw IC-rekeningen bij te werken met eventuele wijzigingen die de partner in hun rekeningschema aanbrengt.

De volgende stap is uw rekeningschema toe te wijzen aan het IC-rekeningschema. Leer meer op [Het IC-rekeningstelsel koppelen aan het rekeningstelsel van uw bedrijf](#map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts).

### <a name="import-or-export-an-intercompany-chart-of-accounts"></a>Het IC-rekeningschema importeren of exporteren

Het synchronisatiebedrijf kan zijn rekeningschema delen met partners door het naar een bestand te exporteren. Partners kunnen het bestand importeren om het rekeningschema te krijgen.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), pictogram, voer **Intercompany-instelling** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **IC-rekeningschema**.
3. Kies op de pagina **IC-rekeningschema** de actie **Importeren/exporteren** en kies **Importeren** of **Exporteren**.
4. Kies het bestand dat u wilt importeren of exporteren.  

De pagina **IC-rekeningschema** wordt gevuld met nieuwe of bewerkte grootboekrekeningregels volgens het IC-rekeningschema in het bestand. Bestaande niet-gerelateerde regels op de pagina blijven ongewijzigd.

## <a name="map-the-intercompany-chart-of-accounts-to-your-companys-chart-of-accounts"></a>Het IC-rekeningschema toewijzen aan het rekeningschema van uw bedrijf

Wanneer u het IC-rekeningschema hebt gedefinieerd of geïmporteerd, wijst u elke IC-rekening toe aan een van uw rekeningen. Geef op de pagina **IC-rekeningschema** op hoe IC-grootboekrekeningen van inkomende transacties worden toegewezen aan grootboekrekeningen uit het rekeningschema van uw bedrijf.

Als de IC-rekeningen en uw rekeningen dezelfde nummers hebben, kunt u de rekeningen automatisch toewijzen.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") pictogram, voer **Intercompany-instelling** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **IC-rekeningschema**.

    > [!TIP]
    > Om toegang te krijgen tot de acties op de pagina moet u de pagina mogelijk uitvouwen naar de brede lay-outweergave.

3. Kies op de pagina **IC-rekeningschema** de actie **Toewijzing van rekeningschema**.
4. U kunt de rekeningen automatisch of handmatig toewijzen.

    * Om de toewijzing handmatig te maken in de deelvensters **IC-rekeningschema** en **Grootboekrekeningschema**, kiest u een rekening en kiest u vervolgens een rekening in de **Grootboekrekeningnr.** en **IC-nummer** velden.
    * Om rekeningen met dezelfde nummers automatisch toe te wijzen selecteert u de regels die u wilt toewijzen, kiest u de actie **Koppelen aan schema met hetzelfde nr.** en kiest u vervolgens het rekeningschema dat u wilt bijwerken.

    > [!TIP]
    > Wilt u veel of misschien wel alle rekeningen toewijzen, kies dan een regel, kies :::image type="icon" source="media/show-more-options-icon.png" border="false"::: en kies dan **Meer selecteren**.

## <a name="set-up-intercompany-dimensions"></a>IC-dimensies instellen

Als partners transacties uitwisselen met daaraan gekoppelde dimensies, spreek dan de dimensies af die u allemaal gaat gebruiken. Het synchronisatiebedrijf kan bijvoorbeeld een vereenvoudigde versie van hun dimensies maken, deze naar een XML-bestand exporteren en het bestand vervolgens naar elke partner distribueren. Elke partner kan het XML-bestand importeren op de pagina **IC-dimensies** en vervolgens de IC-dimensies toewijzen aan hun dimensies. Leer meer op [IC-dimensies koppelen aan dimensies van uw bedrijf](#map-intercompany-dimensions-to-your-companys-dimensions).

> [!NOTE]
> Elk bedrijf moet zijn dimensies toewijzen aan de IC-dimensies voor uitgaande documenten en inkomende documenten. Rekeningen in beide richtingen toewijzen is belangrijk en helpt de consistentie tussen de bedrijven te behouden.

Als partners de IC-dimensies van de synchronisatiepartner zullen gebruiken, volgt u de stappen in deze sectie. Als u wilt delen met behulp van een XML-bestand dat de IC-dimensies bevat, volgt u de stappen in [IC-dimensies importeren of exporteren](#import-or-export-intercompany-dimensions).

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") pictogram, voer **Intercompany-instelling** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **IC-dimensies**.
3. Om dimensies toe te voegen voert u een van de volgende handelingen uit op de pagina **IC-dimensies** :
    * Kies **Nieuw** en voer vervolgens elke dimensie op een regel in.  
    * Als uw IC-dimensies identiek zijn aan uw normale dimensies of erop lijken, kunt u de pagina automatisch invullen door de actie **Kopiëren uit dimensies** te kiezen. U kunt de regels achteraf zo nodig bewerken.
    * Als u IC-dimensies hebt opgegeven voor een synchronisatiepartner, gebruikt u de actie **Synchronisatie-instelling** om die dimensies te kopiëren.

    > [!TIP]
    > Als u de IC-dimensies van een synchronisatiepartner kopieert, kunt u de actie **Synchronisatie-instelling** gebruiken om uw IC-dimensies bij te werken met eventuele wijzigingen die de partner in hun dimensies aanbrengt.  

### <a name="import-or-export-intercompany-dimensions"></a>IC-dimensies importeren of exporteren

Het synchronisatiebedrijf kan zijn dimensies delen met partners door ze naar een bestand te exporteren. Partners kunnen het bestand importeren om de dimensies te krijgen.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), pictogram, voer **Intercompany-instelling** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **IC-dimensies**.  
3. Kies op de pagina **IC-dimensies** de actie **Importeren/exporteren** en kies **Importeren** of **Exporteren**.
4. Kies het bestand dat u wilt importeren of exporteren.

De volgende stap is de dimensies toe te wijzen aan de IC-dimensies. Leer meer op [IC-dimensies koppelen aan dimensies van uw bedrijf](#map-intercompany-dimensions-to-your-companys-dimensions).

### <a name="map-intercompany-dimensions-to-your-companys-dimensions"></a>IC-dimensies toewijzen aan dimensies van uw bedrijf

Nadat u de dimensies hebt opgegeven die u gaat gebruiken, wijst u elke IC-dimensie toe aan een van de dimensies van uw bedrijf, en vice versa. Gebruik de pagina **Toewijzing van IC-dimensies** om de toewijzing op te geven. Herhaal daarna het proces voor de dimensiewaarden.

* Geef op hoe IC-dimensies voor inkomende transacties worden toegewezen aan dimensies uit de lijst met dimensies van uw bedrijf.
* Geef op hoe uw dimensies worden vertaald in IC-dimensies voor *uitgaande transacties*.

Als IC-dimensies dezelfde code hebben als de corresponderende dimensies in uw bedrijf, kunt u de dimensies automatisch toewijzen.  

In de volgende stappen wijst u eerst IC-dimensies toe aan dimensies voor inkomende documenten in het deelvenster **IC-dimensies**. Vervolgens wijst u dimensies toe aan IC-dimensies voor uitgaande documenten op de pagina **Dimensies van huidig bedrijf**.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") pictogram, voer **Intercompany-instelling** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **IC-dimensies**.
3. Kies op de pagina **IC-dimensies** de actie **Dimensietoewijzing**.
4. U kunt de dimensies automatisch of handmatig toewijzen.

    * Om de toewijzing handmatig te maken kiest u in de deelvensters **IC-dimensies** en **Huidige bedrijfsdimensies** een dimensie en kiest u vervolgens een dimensie in de velden **Dim.code** en **IC-dim.code**.
    * Om dimensies met dezelfde code automatisch toe te wijzen selecteert u de regels die u wilt toewijzen, kiest u de actie **Dimensies met dezelfde code toewijzen** en kiest u vervolgens de dimensies die u wilt bijwerken. 

    > [!TIP]
    > Wilt u veel of misschien wel alle dimensies toewijzen, kies dan een regel, kies :::image type="icon" source="media/show-more-options-icon.png" border="false"::: en kies dan **Meer selecteren**.

5. Kies de actie **Toewijzing van dimensiewaarden**.
6. Op de pagina **Toewijzing van IC-dimensiewaarden** zijn de stappen voor het maken van de toewijzing vergelijkbaar met wat u zojuist deed voor dimensies.

## <a name="set-up-intercompany-general-journal-templates-and-batches"></a>IC-dagboeksjablonen en -batches instellen

U moet een dagboeksjabloon en een dagboekbatch instellen om standaard te gebruiken voor IC-transacties. De sjabloon en de batch zijn vooral belangrijk als u IC-transacties van uw partners automatisch accepteert. Ga voor meer informatie over automatisch accepteren van transacties naar [Transacties van intercompany-partners automatisch accepteren](#auto-accept-transactions-from-intercompany-partners).   

* Met dagboeken kunt u naar grootboekrekeningen en andere rekeningen zoals bank-, klant- en leveranciersrekeningen boeken. Door te boeken met een dagboek worden er altijd posten gemaakt in grootboekrekeningen.  Gebruik de pagina **Intercompany-dagboek** om de te gebruiken dagboekbatch in te stellen. De instellingen die specifiek zijn voor IC-transacties zijn de rekeningen die u opgeeft in de velden **IC-rekeningtype** en **IC-rekeningnr.**.
* Dankzij dagboeksjablonen kunt u met een dagboekpagina werken die speciaal voor een bepaalde taak is ontworpen. Elke dagboeksjabloon bevat exact de velden die voor een bepaald deel van het programma nodig zijn. Gebruik de pagina **Fin. dagboeksjablonen** om een sjabloon in te stellen voor IC-transacties.

Ga voor meer informatie over dagboeksjablonen en -batches naar [Dagboeksjablonen en -batches gebruiken](ui-work-general-journals.md#use-journal-templates-and-batches).

## <a name="set-up-a-company-for-intercompany-transactions"></a>Een bedrijf instellen voor IC-transacties

Bij de volgende stappen wordt ervan uitgegaan dat er een synchronisatiepartner is ingesteld met het rekeningschema en de dimensies waarop u het IC-rekeningschema en de IC-dimensies baseert. U kunt ze zelf instellen, maar het is doorgaans sneller om aan de slag te gaan en het onderhoud is eenvoudiger als u een synchronisatiepartner gebruikt. Ga voor meer informatie over de synchronisatiepartner naar [Een synchronisatiepartner instellen](#set-up-a-synchronization-partner).

> [!TIP]
> Het is een goed idee om de velden in te vullen op het sneltabblad **Algemeen** op de pagina **Intercompany-instelling** voor elke partner voordat u hun partners toevoegt. Wanneer u partnerbedrijven toevoegt die zich in dezelfde tenant bevinden, krijgt [!INCLUDE [prod_short](includes/prod_short.md)] de IC-code en de bedrijfsnaam ervan uit hun instelling op het sneltabblad Algemeen. Het veld **Bedrijfsnaam** verifieert dat hun IC-code uniek is.

> [!NOTE]
> Als u een synchronisatiepartner gebruikt, laat u het veld **Synchronisatiepartner** leeg wanneer u dat bedrijf instelt voor het partnerschap.

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), pictogram, voer **Intercompany-instelling** in en kies vervolgens de gerelateerde koppeling.  
2. Vul op de pagina **Intercompany-instelling** de velden in op het sneltabblad **Algemeen**. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!NOTE]
> In [!INCLUDE[prod_short](includes/prod_short.md)] online kunt u geen bestandslocaties gebruiken om transacties over te brengen naar uw partners omdat [!INCLUDE[prod_short](includes/prod_short.md)] geen toegang heeft tot uw lokale netwerk. Daarom is als u **Bestandslocatie** kiest in het veld **Overdrachtstype**, het veld **Pad naar map** niet beschikbaar. In plaats daarvan wordt het bestand gedownload naar de map **Downloads** op uw computer. U kunt het bestand vervolgens bijvoorbeeld per e-mail naar iemand in het partnerbedrijf sturen. Voor een directer proces raden we u aan **E-mail** te kiezen.

De volgende stap is het opzetten van de partnerbedrijven.

## <a name="set-up-intercompany-partners"></a>IC-partners instellen

Elke partner moet alle andere bedrijven in het partnerschap als partner toevoegen.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") pictogram, voer **Intercompany-instelling** in en kies vervolgens de gerelateerde koppeling.
2. Kies op het sneltabblad **IC-partners** **Toevoegen**.
3. Vul op de pagina **IC-partner** de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Herhaal stap 2 en 3 voor alle bedrijven in het partnerschap.

> [!NOTE]
> Voor IC-boekingen, wanneer u de schakeloptie **Transactie automatisch accepteren** hebt ingeschakeld op de pagina **IC-partner**, onderdrukt [!INCLUDE[prod_short](includes/prod_short.md)] waarschuwingsberichten over inkoopfacturen die de oorspronkelijke inkooporder dupliceren. Daarom is het belangrijk om een bedrijfsproces te hebben voor het beheren van duplicaten. Bijvoorbeeld door dergelijke inkooporders te verwijderen wanneer de inkoopfactuur wordt ontvangen van de intercompany-partner.

### <a name="set-up-intercompany-partners-as-customers-and-vendors"></a>IC-partners instellen als klanten en leveranciers

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), pictogram, voer **Intercompany-instelling** in en kies vervolgens de gerelateerde koppeling.
2. Open op het sneltabblad **IC-partners** de kaartpagina voor de partner.
3. Kies, afhankelijk van wat u wilt doen, de klant of partner in het veld **Klantnummer** of **Leveranciersnummer**.

    > [!NOTE]
    > Als de klant of leverancier nog niet is gemaakt, kunt u **+Nieuw** kiezen in het vervolgkeuzemenu om ze in te stellen. Ga voor meer informatie over het maken van klanten en leveranciers naar [Nieuwe klanten registreren](sales-how-register-new-customers.md) en [Nieuwe leveranciers registreren](purchasing-how-register-new-vendors.md).

    > [!TIP]
    > U kunt ook een klant of leverancier als een IC-partner opgeven door het veld **IC-partnercode** in te vullen op de pagina's **Klantenkaart** en **Leverancierskaart**.

### <a name="set-up-default-intercompany-partner-general-ledger-accounts"></a>Standaardgrootboekrekeningen voor IC-partners instellen

Wanneer u een IC-verkoopregel of -inkoopregel maakt om te verzenden als uitgaande transactie, voert u een rekening uit het IC-rekeningschema in als standaardrekening waarop het bedrag in het bedrijf van uw partner wordt geboekt. Op de pagina **Grootboekrekening** kunt u een standaard IC-grootboekrekening voor partners opgeven voor rekeningen die u regelmatig gebruikt op uitgaande IC-verkoop- of -inkoopregels. Voor uw tegoedenrekeningen kunt u bijvoorbeeld de corresponderende schuldenrekeningen opgeven uit het IC-rekeningschema. De debiteuren- en crediteurenrekeningen worden gebruikt als tegenrekening voor de IC-partner wanneer u transacties boekt in IC-dagboeken.  

Wanneer u nu een grootboekrekening opgeeft in het veld **Tegenrekeningnr.** op een IC-regel met **IC-partner** in het veld **Rekeningsoort**, wordt het veld **Grootboekrekeningnr. IC-partner** automatisch ingevuld.  

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Rekeningschema** in en kies de gerelateerde koppeling.  
2. Open de grootboekrekening die wordt gebruikt voor IC-transacties en voer in het veld **Standaard IC-partnergrootboekrekening** de IC-grootboekrekening in waarnaar uw partner boekt wanneer u boekt naar de grootboekrekening op de regel.
3. Herhaal stap 2 voor elke rekening die u vaak invoert in het veld **Tegenrekeningnr.** op een regel in een IC-dagboek of -document.

### <a name="auto-accept-transactions-from-intercompany-partners"></a>Transacties van IC-partners automatisch accepteren

Om intercompany-transacties sneller te kunnen verwerken, kunt u opgeven dat u automatisch dagboekregels wilt maken op basis van boekingen van een IC-partner op de pagina **IC-diversendagboek**. Om automatisch inkomende en uitgaande transacties te maken moet u de volgende schakelaars voor elke partner inschakelen:

* Schakel op de pagina **Intercompany-instelling** de schakelaar **Transacties automatisch verzenden** voor de synchronisatiepartner in. Geef vervolgens op waar ontvangen IC-dagboektransacties moeten worden gemaakt door de velden **Standaard-IC-dagboeksjabloon** en **Standaard-IC-dagboekbatch** in te vullen.

    > [!TIP]
    > Als het veld **Standaard-IC-dagboeksjabloon** leeg is, moet u een dagboeksjabloon instellen om te gebruiken voor uw IC-dagboeken. Ga voor meer informatie over dagboeksjablonen en -batches naar [IC-dagboeksjablonen en -batches instellen](#set-up-intercompany-general-journal-templates-and-batches)    

* Schakel op de pagina **IC-partner** de schakelaar **Transacties automatisch accepteren** in.

De journaalregels worden voor u gemaakt, maar niet geboekt.

> [!NOTE]
> Als uw organisatie intercompany-functies heeft gebruikt in [!INCLUDE [prod_short](includes/prod_short.md)] vóór 2022 release wave 1, om transacties automatisch te accepteren, moet uw beheerder de functieschakelaar **Automatisch IC-dagboektransacties accepteren** op de pagina **Functiebeheer** aanzetten.

### <a name="specify-the-bank-accounts-to-use-for-intercompany-partners"></a>De bankrekeningen opgeven die moeten worden gebruikt voor IC-partners

Om snelle betalingen mogelijk te maken geeft u een of meer bankrekeningen op die u wilt gebruiken voor IC-partners. Wanneer een partner een IC-dagboek gebruikt om een betaling uit te voeren, kan deze de bankrekening op de regel opgeven. De bankrekening wordt gebruikt als tegenrekening in het ontvangende bedrijf, waardoor de noodzaak om transacties handmatig in te voeren tot een minimum wordt beperkt.

* Om de te gebruiken bankrekening op te geven kiest u op de pagina **IC-partners** de actie **Bankrekeningen**. Voer op de **IC-bankrekeningkaart** de rekeninggegevens in.

## <a name="troubleshoot-your-intercompany-setup"></a>Problemen met uw IC-instellingen oplossen

Op de pagina **Intercompany-instelling** bevat het deelvenster **Diagnose van intercompany-instellingen** tegels die aangeven of u alle componenten hebt ingesteld die nodig zijn om IC-transacties uit te wisselen. De tegels zijn ook beschikbaar in het rolcentrum Bedrijfsmanager. Kies de tegels om erachter te komen wat er ontbreekt. Ga voor een overzicht van de vereiste componenten naar [Overzicht van de stappen om aan de slag te gaan](#overview-of-the-steps-to-get-started).

## <a name="see-also"></a>Zie ook

[Intercompany-transacties beheren](intercompany-manage.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Werken met diversendagboeken](ui-work-general-journals.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
