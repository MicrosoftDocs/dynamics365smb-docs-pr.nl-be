---
title: Gedetailleerde machtigingen definiëren
description: In dit artikel wordt beschreven hoe u gedetailleerde machtigingen definieert en elke gebruiker de machtigingensets toewijst die ze nodig hebben om hun werk te doen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'access, right, security'
ms.search.form: '1, 119, 8930, 9800, 9807, 9808, 9830, 9831, 9802, 9855, 9862'
ms.date: 02/08/2023
---

# <a name="assign-permissions-to-users-and-groups"></a>Machtigingen toewijzen aan gebruikers en groepen

[!INCLUDE [2023rw1-sec-group-long](includes/2023rw1-sec-group-long.md)]

Het beveiligingssysteem van [!INCLUDE[prod_short](includes/prod_short.md)] bepaalt tot welke objecten een gebruiker toegang heeft binnen elke database of omgeving, in combinatie met de licentie van de gebruiker. U kunt voor elke gebruiker opgeven of deze gegevens in de databaseobjecten mag lezen, wijzigen of invoeren. Zie [Gegevensbeveiliging](/dynamics365/business-central/dev-itpro/security/data-security?tabs=object-level) in inhoud voor ontwikkelaars en beheerders voor [!INCLUDE[prod_short](includes/prod_short.md)] voor meer informatie.

Voordat u machtigingen toewijst aan gebruikers en gebruikersgroepen, moet u definiëren wie zich mag aanmelden door gebruikers te maken volgens hun licentie. Zie [Gebruikers maken volgens licenties](ui-how-users-permissions.md) voor meer informatie.

[!INCLUDE[prod_short](includes/prod_short.md)] bevat twee machtigingsniveaus voor databaseobjecten:

- Algemene machtigingen volgens de licentie, ook wel een recht genoemd.

  De licenties bevatten standaard machtigingensets. Vanaf releasewave 1 van 2022 kunnen beheerders deze standaardmachtigingen aanpassen voor de relevante licentietypen. Zie [Machtigingen configureren op basis van licenties](ui-how-users-permissions.md#licensespermissions) voor meer informatie.  

- Gedetailleerde machtigingen die u toewijst in [!INCLUDE[prod_short](includes/prod_short.md)].

In dit artikel wordt beschreven hoe u machtigingen in [!INCLUDE [prod_short](includes/prod_short.md)] kunt definiëren, gebruiken en toepassen om de standaardconfiguratie te wijzigen.  

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]  
Zie voor meer informatie [Gedelegeerde beheerderstoegang tot Business Central Online](/dynamics365/business-central/dev-itpro/administration/delegated-admin).  

[!INCLUDE [prod_short](includes/prod_short.md)] online bevat standaard gebruikersgroepen die automatisch aan gebruikers worden toegewezen op basis van hun licentie. U kunt de standaardconfiguratie wijzigen beveiligingsgroepen, machtigingensets en machtigingen aan te passen of toe te voegen. De volgende tabel geeft een overzicht van de belangrijkste scenario's voor het wijzigen van de standaardmachtigingen.  

|Als u dit wilt doen:  |Zie  |
|---------|---------|
|Om het gemakkelijker te maken om machtigingen voor meerdere gebruikers te beheren, kunt u ze organiseren in beveiligingsgroepen en dan in één actie één machtigingsset voor meerdere gebruikers toewijzen of wijzigen.| [Machtigingen beheren via gebruikersgroepen](#to-manage-permissions-through-user-groups) |
|Machtigingensets beheren voor specifieke gebruikers | [Machtigingssets toewijzen aan gebruikers](#to-assign-permission-sets-to-users) |
|Leren hoe u een machtigingenset definieert|[Een machtigingenset maken](#to-create-a-permission-set)|
|Machtigingen van een gebruiker weergeven of problemen oplossen|[Een overzicht krijgen van de machtigingen van een gebruiker](#to-get-an-overview-of-a-users-permissions)|
|Voor meer informatie over beveiliging op recordniveau|[Beveiligingsfilters beperken de toegang van een gebruiker tot specifieke records in een tabel](#security-filters-limit-a-users-access-to-specific-records-in-a-table)|

> [!NOTE]
> Een bredere manier om te definiëren welke functies voor gebruikers toegankelijk zijn, is via het veld **Ervaring** op de pagina **Bedrijfsgegevens**. Zie voor meer informatie [Wijzigen welke functies worden weergegeven](ui-experiences.md).
>
> U kunt ook definiëren welke functies voor gebruikers beschikbaar zijn en hoe ze ermee omgaan op pagina's. Dit doet u door middel van profielen die u toewijst aan verschillende soorten gebruikers, afhankelijk van hun functie of afdeling. Zie voor meer informatie [Profielen beheren](admin-users-profiles-roles.md) en [Aanpassen [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md).

## <a name="to-create-a-permission-set"></a>Een machtigingenset maken

> [!NOTE]
> In releasewave 2 van 2022 hebben we het gemakkelijker gemaakt om machtigingen toe te voegen aan machtigingensets. In plaats van afzonderlijke machtigingen toe te voegen, kunt u volledige machtigingensets toevoegen. Indien nodig kunt u vervolgens individuele machtigingen daarin uitsluiten. Zie [Andere machtigingensets toewijzen](#to-add-other-permission-sets) voor meer informatie. Om dat mogelijk te maken, hebben we de pagina Machtigingenset vervangen door een nieuwe. De belangrijkste verschillen zijn de nieuwe deelvensters **Machtigingensets** en **Resultaten** en het feitenblok **Opgenomen machtigingen**. Om door te gaan met het gebruiken van de vervangen pagina **Machtigingensets** kiest u de actie **Machtigingen (verouderd)**.

Het onderhoud is ook gemakkelijker. Wanneer u een systeemmachtiging toevoegt, wordt uw door de gebruiker gedefinieerde machtigingenset automatisch bijgewerkt met alle wijzigingen die Microsoft in die machtigingen aanbrengt.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Machtigingensets** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Nieuw**.
3. Vul op de nieuwe regel de velden indien nodig in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
4. Kies de actie **Machtigingen**.
5. Op de pagina **Machtigingenset** kunt u in het veld **Type** als volgt machtigingen opnemen of uitsluiten:

  Om de toestemming op te nemen, kiest u **Opnemen** en kiest u vervolgens het toegangsniveau dat u wilt geven, in de velden **Leesmachtiging**, **Invoegmachtiging**, **Wijzigmachtiging**, **Verwijdermachtiging** en **Uitvoermachtiging**. De volgende tabel beschrijft de opties.

  |Optie|Omschrijving|Volgorde|
  |------|-----------|-------|
  |**Leeg**|De gebruiker kan de actie niet op het betreffende object uitvoeren.|Laagste|  
  |**Ja**|De gebruiker kan de actie op het betreffende object uitvoeren.|Hoogste|
  |**Indirect**|De gebruiker kan de actie op het object uitvoeren maar alleen via een ander, gerelateerd object waartoe de gebruiker volledige toegang heeft. Zie [Voorbeeld: indirecte machtiging](#example---indirect-permission) in dit artikel en [Eigenschap Machtigingen](/dynamics365/business-central/dev-itpro/developer/properties/devenv-permissions-property#example---indirect-permission) in de Help voor ontwikkelaars en IT-Pro voor meer informatie|Op een na hoogste|
  
  Om de machtiging of een of meer toegangsniveaus uit te sluiten, kiest u **Uitsluiten** en kiest u vervolgens het toegangsniveau dat u wilt geven. De volgende tabel beschrijft de opties.

  |Optie|Omschrijving|
  |------|-----------|-------|
  |**Leeg**|Gebruik het toegangsniveau op basis van de hiërarchie van machtigingen in de set.  |
  |**Uitsluiten**|Het specifieke toegangsniveau voor het object verwijderen.|
  |**Reduceren tot indirect**|Het toegangsniveau in wijzigen Indirect als machtigingensets directe toegang tot het object geven. Kies deze optie bijvoorbeeld als de machtigingenset directe toegang geeft tot grootboekposten, maar u niet wilt dat gebruikers volledige toegang tot de posten hebben.|
  
  > [!NOTE]
  > Als een machtiging zich in een machtigingenset bevindt die is opgenomen, en ook in een machtigingenset die is uitgesloten, wordt de machtiging uitgesloten.

6. Gebruik de velden **Objecttype** en **Object-id** om het object op te geven waartoe u toegang geeft.

  > [!TIP]
  > Nieuwe regels tonen standaardwaarden. Bijvoorbeeld het veld **Objecttype** bevat **Tabelgegevens** en het veld **Object-id** bevat **0**. De standaardwaarden zijn slechts tijdelijke aanduidingen en worden niet gebruikt. U moet een type object en een object kiezen in het veld **Object-id** voordat u nog een nieuwe regel kunt maken.

7. Optioneel: als u machtigingen definieert voor een objecttype Tabelgegevens, kunt u in het veld **Beveiligingsfilter** de gegevens filteren waartoe een gebruiker toegang heeft in velden in de geselecteerde tabel. U kunt bijvoorbeeld opgeven dat een gebruiker alleen toegang heeft tot de records die gegevens over een bepaalde klant bevatten. Zie voor meer informatie [Beveiligingsfilters beperken de toegang van een gebruiker tot specifieke records in een tabel](#security-filters-limit-a-users-access-to-specific-records-in-a-table) en [Beveiligingsfilters gebruiken](/dynamics365/business-central/dev-itpro/security/security-filters).
8. Optioneel: voeg in het deelvenster **Machtigingensets** een of meer andere machtigingensets toe. Zie [Andere machtigingensets toewijzen](#to-add-other-permission-sets) voor meer informatie.

> [!IMPORTANT]
> Wees voorzichtig bij het toewijzen van **Invoegmachtiging** of **Wijzigmachtiging** aan de tabel **9001 Gebruikersgroepslid** of **9003 Machtigingenset van gebruikersgroep**. Alle gebruikers die aan de machtigingenset zijn toegewezen, kunnen zichzelf mogelijk toewijzen aan andere gebruikersgroepen, die hen op hun beurt onbedoelde machtigingen kunnen geven.

### <a name="example---indirect-permission"></a>Voorbeeld: indirecte machtiging

U kunt een indirecte machtiging toewijzen om een gebruiker toe te staan een object te gebruiken, maar alleen door middel van een ander object. Een gebruiker kan bijvoorbeeld de machtiging hebben om codeunit 80, Verkoop-boeken uit te voeren. De codeunit Verkoop-boeken voert veel taken uit, waaronder het wijzigen van tabel 37, Inkoopregel. Wanneer de gebruiker een verkoopdocument boekt met de codeunit Verkoop-boeken, controleert [!INCLUDE[prod_short](includes/prod_short.md)] of de gebruiker de machtiging heeft om de tabel Verkoopregel te wijzigen. Als dat niet het geval is, kan de codeunit de taken niet uitvoeren en ontvangt de gebruiker een foutmelding. Indien dit wel zo is, wordt de codeunit uitgevoerd.

De gebruiker hoeft echter geen volledige toegang te hebben tot de tabel Inkoopregel om de codeunit uit te voeren. Als de gebruiker een indirecte machtiging heeft voor de tabel Verkoopregel, kan de codeunit Verkoop-boeken worden uitgevoerd. Wanneer een gebruiker een indirecte machtiging heeft, kan die gebruiker enkel de tabel Inkoopregel wijzigen door de codeunit Verkoop-boeken of een ander object uit te voeren dat de machtiging heeft om de tabel Inkoopregel te wijzigen. De gebruiker kan alleen de tabel Inkoopregel wijzigen vanuit de ondersteunde toepassingsgebieden. De gebruiker kan de functie niet per ongeluk of opzettelijk op andere manieren uitvoeren.

### <a name="to-add-other-permission-sets"></a>Andere machtigingensets toevoegen

Breid een machtigingenset uit door er andere machtigingensets aan toe te voegen. Daarna kunt u specifieke machtigingen of volledige machtigingensets opnemen of uitsluiten in elke set die u toevoegt. Dit omvat machtigingen in de machtigingensets Extensie en Systeemtype, die anders niet zijn toegestaan. Uitsluitingen zijn alleen van toepassing op de machtigingenset die u uitbreidt. De originele set wordt niet aangetast.

Voeg op de pagina **Machtigingenset** een machtigingenset toe aan het deelvenster **Machtigingensets**. Het deelvenster **Resultaat** toont alle toegevoegde machtigingensets. Als u de machtigingen wilt bekijken die zijn opgenomen in een set die u hebt toegevoegd, kiest u de set in het deelvenster Resultaat en toont het feitenblok **Opgenomen machtigingen** de machtigingen.

Gebruik in het deelvenster **Resultaat** het veld **Opnamestatus** om de machtigingensets te identificeren waarin u machtigingen of machtigingensets hebt uitgesloten. Als iets is uitgesloten, is de status **Gedeeltelijk**.

Voor een algemeen overzicht van machtigingen in de machtigingenset kiest u de actie **Alle machtigingen weergeven**. De pagina **Uitgebreide machtigingen** toont alle machtigingen die al waren toegewezen aan de machtigingenset en de machtigingen in de toegevoegde machtigingensets.

Als u alle machtigingen volledig wilt uitsluiten van een machtigingenset,, selecteert u in het deelvenster **Resultaat** de regel, en kiest u vervolgens **Meer opties weergeven**, gevolgd door **Uitsluiten**. Wanneer u een machtigingenset uitsluit, wordt er in het deelvenster **Machtigingensets** een regel gemaakt van het type Uitgesloten. Als u een machtigingenset hebt uitgesloten, maar deze weer wilt opnemen, verwijdert u de regel in het deelvenster **Machtigingensets**.

Als u een specifieke machtiging volledig of gedeeltelijk wilt uitsluiten in een set die u heeft toegevoegd, maakt u onder **Machtigingen** een regel voor het object. De velden voor toegangsniveau, Machtigingen invoegen, Machtigingen wijzigen, enzovoort, bevatten allemaal **Uitsluiten**. Kies de juiste optie om een bepaald toegangsniveau toe te staan.

Als u een machtigingenset uitsluit, worden alle machtigingen in de set uitgesloten. [!INCLUDE [prod_short](includes/prod_short.md)] berekent machtigingen als volgt:

1. Bereken de volledige lijst met opgenomen machtigingen
2. Bereken de volledige lijst met uitgesloten machtigingen
3. Verwijder uitgesloten machtigingen uit de lijst met opgenomen machtigingen (het verwijderen van een indirecte machtiging is hetzelfde als Reduceren tot indirect)

## <a name="to-copy-a-permission-set"></a>Een machtigingenset kopiëren

Maak een nieuwe machtigingenset door een andere te kopiëren. De nieuwe set bevat alle machtigingen en machtigingensets van de set die u hebt gekopieerd. Hoe de machtigingen en machtigingensets in de nieuwe machtigingenset zijn gerangschikt, verschilt, afhankelijk van uw keuze in het veld **Kopieerbewerking**. De volgende tabel beschrijft de opties.

|Optie  |Omschrijving  |
|---------|---------|
|**Kopiëren via referentie**     | De originele machtigingenset en alle machtigingensets die eraan zijn toegevoegd, staan vermeld in het deelvenster **Resultaten**.       |
|**Platte machtigingkopie**  | Alle machtigingen van alle machtigingensets zijn opgenomen in een platte lijst in het **deelvenster Machtigingen**. Machtigingen zijn niet geordend op machtigingenset.        |
|**Klonen**     | Een exacte kopie van de originele machtigingenset maken.        |

1. Op de pagina **Machtigingensets** selecteert u de naam van een machtigingenset die u wilt kopiëren en kiest u vervolgens de actie **Machtigingenset kopiëren**.
2. Op de pagina **Machtigingenset kopiëren** geeft u de naam op van de nieuwe machtigingenset en kiest u de knop OK.
3. In het veld **Kopieerbewerking** geeft u op hoe de machtiging in de nieuwe machtigingenset moet worden geordend.
4. Optioneel: als u een systeemmachtigingenset toevoegt, wilt u wellicht een melding ontvangen als de naam of inhoud van de oorspronkelijke machtigingenset in een toekomstige versie verandert. Hiermee kunt u overwegen of u uw door de gebruiker gedefinieerde machtigingenset wilt bijwerken. Om een bericht te ontvangen, zet u de schakelaar **Informeren bij gewijzigde machtigingenset** aan.

> [!NOTE]
> Het bericht vereist dat het bericht **Oorspronkelijke systeemmachtigingenset gewijzigd** is ingeschakeld op de pagina **Mijn berichten**.

## <a name="to-create-or-modify-permissions-by-recording-your-actions"></a>Machtigingen maken of wijzigen door uw acties op te nemen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Machtigingensets** in en kies vervolgens de gerelateerde koppeling.

    U kunt ook op de pagina **Gebruikers** de actie **Machtigingensets** kiezen.
2. Kies op de pagina **Machtigingensets** de actie **Nieuw**.
3. Vul op een nieuwe regel de velden indien nodig in.
4. Kies de actie **Machtigingen**.
5. Kies op de pagina **Machtigingen** de actie **Machtigingen registreren** en kies de actie **Starten**.  
    Opnemen moet worden gedaan met behulp van de functie **Deze pagina openen in een nieuw venster** (pop-out) om het opnamevenster **Machtigingen** naast elkaar te krijgen, of door binnen hetzelfde tabblad te werken.  
    Er wordt nu een opnameproces gestart dat al uw acties in de gebruikersinterface vastlegt.
6. Ga naar de verschillende pagina's en activiteiten in [!INCLUDE[prod_short](includes/prod_short.md)] waartoe u gebruikers met deze machtigingenset toegang wilt verlenen. U moet de taken uitvoeren waarvoor u machtigingen wilt opnemen.
7. Om de opname te stoppen, gaat u terug naar de pagina **Machtigingen** en kiest u de actie **Stoppen**.
8. Kies de knop **Ja** om de opgenomen toegangsrechten aan de nieuwe machtigingenset toe te voegen.
9. Geef voor elk object in de opgenomen lijst aan of gebruikers records mogen invoegen, wijzigen of verwijderen in de opgenomen tabellen.

### <a name="to-export-and-import-a-permission-set"></a>Een machtigingenset exporteren en importeren

Om snel machtigingen in te stellen kunt u machtigingensets importeren die u vanuit een andere [!INCLUDE[prod_short](includes/prod_short.md)]-tenant hebt geëxporteerd.

In multitenant-omgevingen wordt een machtigingenset geïmporteerd in een specifieke tenant. Met andere woorden, het bereik van de import is: *Tenant*.

1. Selecteer in tenant 1 op de pagina **Machtigingensets** de regel of regels van de machtigingensets die u wilt kopiëren en kies vervolgens de actie **Machtigingensets exporteren**.

    Er wordt een XML-bestand gemaakt in de downloadmap op uw computer. Standaard heet het *Export Permission Sets.xml*.

2. Selecteer in tenant 2 op de pagina **Machtigingensets** de actie **Machtigingensets importeren**.
3. Bedenk op de dialoogpagina **Machtigingensets importeren** of u bestaande machtigingensets wilt samenvoegen met nieuwe machtigingensets in het XML-bestand.

    Als u het selectievakje **Bestaande machtigingen bijwerken** inschakelt, worden bestaande machtigingensets met dezelfde naam als die in het XML-bestand samengevoegd met de geïmporteerde machtigingensets.

    Als u het selectievakje **Bestaande machtigingen bijwerken** niet inschakelt, worden bestaande machtigingensets met dezelfde naam als die in het XML-bestand overgeslagen tijdens import. In dat geval wordt u op de hoogte gesteld van machtigingensets die worden overgeslagen.

4. Zoek en selecteer op de dialoogpagina **Importeren** het XML-bestand dat u wilt importeren en kies vervolgens de actie **Openen**.

De machtigingensets worden geïmporteerd.

## <a name="to-remove-obsolete-permissions-from-all-permission-sets"></a>Verouderde machtigingen uit alle machtigingensets verwijderen

Kies op de pagina **Machtigingensets** de actie **Verouderde machtigingen verwijderen**.

## <a name="to-set-up-time-constraints-for-users"></a>Tijdsbeperkingen voor gebruikers instellen

Beheerders kunnen perioden definiëren waarin bepaalde gebruikers kunnen posten. Beheerders kunnen ook specificeren of het systeem registreert hoe lang gebruikers zijn ingelogd. Zo kunnen beheerders ook divisies toewijzen aan gebruikers. Zie [Werken met divisies](inventory-responsibility-centers.md) voor meer informatie.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Gebruikersinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Kies op de pagina **Gebruikersinstellingen** die wordt geopend, de actie **Nieuw**.
3. Voer in het veld **Gebruikers-id** de id van een gebruiker in of kies het veld om alle huidige Windows-gebruikers in het systeem te zien.
4. Vul de vereiste velden in.

## <a name="to-manage-permissions-through-user-groups"></a>Machtigingen beheren via gebruikersgroepen

Met gebruikersgroepen kunt u machtigingensets in het hele bedrijf beheren. [!INCLUDE [prod_short](includes/prod_short.md)] online bevat standaard gebruikersgroepen die automatisch aan gebruikers worden toegewezen op basis van hun licentie. U kunt gebruikers handmatig toevoegen aan een gebruikersgroep en u kunt nieuwe gebruikersgroepen maken als kopieën van bestaande.  

Maak eerst een gebruikersgroep. Wijs daarna machtigingssets toe aan de groep om te definiëren welk object toegankelijk is voor gebruikers van de groep. Wanneer u gebruikers aan de groep toevoegt, gelden de machtigingssets die voor de groep zijn ingesteld, ook voor deze gebruikers.

Machtigingensets die via een gebruikersgroep aan een gebruiker zijn toegewezen, blijven gesynchroniseerd. Een wijziging in de gebruikersgroeprechten wordt automatisch doorgegeven aan de gebruikers. Als u een gebruiker uit een gebruikersgroep verwijdert, worden de desbetreffende machtigingen automatisch ingetrokken.

### <a name="to-add-users-to-a-user-group"></a>Gebruikers aan een gebruikersgroep toevoegen

De onderstaande procedure licht toe hoe u handmatig gebruikersgroepen maakt. Zie [Een gebruikersgroep en alle bijbehorende machtigingssets kopiëren](#to-copy-a-user-group-and-all-its-permission-sets) als u automatisch gebruikersgroepen wilt maken.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Gebruikersgroepen** in en kies vervolgens de gerelateerde koppeling.

    1. U kunt ook op de pagina **Gebruikers** de actie **Gebruikersgroepen** kiezen.
2. Kies op de pagina **Gebruikersgroep** de actie **Gebruikersgroepsleden**.
3. Kies op de pagina **Gebruikersgroep** de actie **Gebruikers toevoegen**.

### <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Een gebruikersgroep en alle bijbehorende machtigingensets kopiëren

Als u snel een nieuwe gebruikersgroep wilt definiëren, kopieert u alle machtigingensets van een bestaande gebruikersgroep naar de nieuwe gebruikersgroep.

> [!NOTE]
> De leden van de gebruikersgroep worden niet gekopieerd naar de nieuwe gebruikersgroep. Dit moet u handmatig achteraf doen. Zie voor meer informatie het gedeelte [Gebruikers toevoegen aan een gebruikersgroep](#to-add-users-to-a-user-group).

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikersgroepen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de gebruikersgroep die u wilt kopiëren, en kies vervolgens de actie **Gebruikersgroep kopiëren**.
3. Voer in het veld **Nieuwe gebruikersgroepcode** een naam voor de groep in en kies vervolgens de knop **OK**.

De nieuwe gebruikersgroep wordt toegevoegd aan de pagina **Gebruikersgroepen**. Voeg gebruikers toe. Zie voor meer informatie het gedeelte [Gebruikers toevoegen aan een gebruikersgroep](#to-add-users-to-a-user-group).  

> [!IMPORTANT]
> U krijgt een validatiefout als u probeert een gebruikersgroep aan de gebruiker toe te wijzen die verwijst naar een machtigingenset die is gedefinieerd in een niet-geïnstalleerde extensie. Dit komt doordat de app-ID van de extensie wordt gevalideerd wanneer ernaar wordt verwezen. Als u die gebruikersgroep aan een gebruiker wilt toewijzen, kunt u de extensie opnieuw installeren, de verwijzing naar de niet-geïnstalleerde extensie uit de machtigingenset verwijderen of die machtigingenset uit de gebruikersgroep verwijderen.

### <a name="to-assign-permission-sets-to-user-groups"></a>Machtigingssets toewijzen aan gebruikersgroepen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Gebruikersgroepen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de gebruikersgroep waaraan u een machtiging wilt toewijzen.  

    Alle machtigingensets die al zijn toegewezen aan de gebruiker worden weergegeven in het feitenblok **Machtigingensets**.
3. Kies de actie **Machtigingssets voor gebruikers** om de pagina **Machtigingssets voor gebruikers** te openen.
4. Vul op de pagina **Machtigingssets voor gebruikers** op een nieuwe regel de vereiste velden in.

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-group-page"></a>Een machtigingsset toewijzen op de pagina **Machtigingsset per gebruikersgroep**

De volgende procedure licht toe hoe u machtigingssets aan een gebruikersgroep toewijst vanaf de pagina **Machtigingsset per gebruikersgroep**.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Gebruikers** in en kies vervolgens de gerelateerde koppeling
2. Selecteer de desbetreffende gebruiker op de pagina **Gebruikers** en kies de actie **Machtigingsset per gebruikersgroep**.
3. Selecteer op de pagina **Machtigingsset per gebruikersgroep** het veld **[naam van gebruikersgroep]** op een regel voor de desbetreffende machtigingsset om de set aan de gebruikersgroep toe te wijzen.
4. Schakel het selectievakje **Alle gebruikersgroepen** in om de machtigingenset aan alle gebruikersgroepen toe te wijzen.

U kunt machtigingssets ook rechtstreeks aan een gebruiker toewijzen.

## <a name="to-assign-permission-sets-to-users"></a>Machtigingssets toewijzen aan gebruikers

Een machtigingsset is een verzameling machtigingen voor specifieke databaseobjecten. Aan alle gebruikers moeten een of meer machtigingensets worden toegewezen voordat ze toegang hebben tot [!INCLUDE[prod_short](includes/prod_short.md)].  

Een [!INCLUDE[prod_short](includes/prod_short.md)]-oplossing bevat vooraf gedefinieerde machtigingssets die door Microsoft of uw oplossingsprovider zijn toegevoegd. U kunt ook nieuwe machtigingssets toevoegen die zijn afgestemd op de behoeften van uw organisatie. Zie voor meer informatie het gedeelte [Een machtigingset maken](#to-create-a-permission-set).

> [!NOTE]
> Als u de toegang van een gebruiker niet meer wilt beperken dan in de licentie is gedefinieerd, kunt u een speciale machtigingsset met de naam SUPER toewijzen aan de gebruiker. Deze machtigingsset zorgt ervoor dat de gebruiker toegang heeft tot alle objecten die in de licentie zijn opgegeven.
>
> Een gebruiker met de Essential-licentie en de SUPER-machtigingsset heeft toegang tot meer functionaliteit dan gebruikers met de Team Member-licentie en de SUPER-machtigingsset.

U kunt machtigingssets op twee manieren aan gebruikers toewijzen:

- Vanaf de pagina **Gebruikerskaart** door machtigingssets te selecteren om aan de gebruiker toe te wijzen.
- Vanaf de pagina **Machtigingsset per gebruiker** door gebruikers te selecteren aan wie een machtigingsset is toegewezen.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Een machtigingenset op een gebruikerskaart toewijzen

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikers** in en kies vervolgens de gerelateerde koppeling
2. Selecteer de gebruiker waaraan u machtigingen wilt toewijzen.
Alle machtigingensets die al zijn toegewezen aan de gebruiker worden weergegeven in het feitenblok **Machtigingensets**.
3. Kies de actie **Bewerken** om de pagina **Gebruikerskaart** te openen.
4. Vul op het sneltabblad **Gebruikersmachtigingensets** waar nodig de velden in op een nieuwe regel. Zie voor meer informatie [Een machtigingenset maken of bewerken](ui-define-granular-permissions.md#to-create-a-permission-set).

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Een machtigingenset op de pagina Machtigingenset per gebruiker toewijzen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Gebruikers** in en kies vervolgens de gerelateerde koppeling
2. Kies op de pagina **Gebruikers** de actie **Machtigingenset per gebruiker**.
3. Selecteer op de pagina **Machtigingenset per gebruiker** het selectievakje **[gebruikersnaam]** op een regel voor de betreffende machtigingenset om de set aan de gebruiker toe te wijzen.

    Selecteer het selectievakje **Alle gebruikers** om de machtigingenset aan alle gebruikers toe te wijzen.

## <a name="to-get-an-overview-of-a-users-permissions"></a>Een overzicht krijgen van de machtigingen van een gebruiker

U kunt effectieve machtigingen van andere gebruikers alleen zien als u bent toegewezen aan de machtiging SECURITY of SUPER. 

De pagina **Effectieve machtigingen** biedt aanvullende informatie over de bron van elke toestemming. Bijvoorbeeld of de bron een beveiligingsgroep is, of dat een machtiging wordt overgenomen. De pagina bevat ook een kolom waarin beheerders de toegepaste beveiligingsfilters kunnen bekijken. Zie voor meer informatie over beveiligingsfilters [Beveiligingsfilters beperken de toegang van een gebruiker tot specifieke records in een tabel](#security-filters-limit-a-users-access-to-specific-records-in-a-table).

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikers** in en kies vervolgens de gerelateerde koppeling.
2. Open de kaart van de betreffende gebruiker.
3. Kies de actie **Effectieve machtigingen**.

    Het deel **Machtigingen** bevat alle databaseobjecten waartoe de gebruiker toegang heeft. U kunt dit gedeelte niet bewerken.

    Het onderdeel **Op machtigingenset-id** bevat de toegewezen machtigingensets waarmee de machtigingen aan de gebruiker worden verleend, de bron en het type van de machtigingenset en de mate waarin de verschillende toegangstypen toegestaan zijn.

    Voor elke rij die u selecteert in de sectie **Machtigingen**, bevat de sectie **Op machtigingenset-id** de machtigingenset of -sets waarmee de machtiging wordt verleend. In dit gedeelte kunt u de waarde wijzigen in elk van de vijf toegangstypevelden, **Lezen**, **Invoegen**, **Wijzigen**, **Verwijderen** en **Uitvoeren**.

    > [!NOTE]  
    > U kunt alleen machtigingensets van het soort **Door gebruiker gedefinieerd** bewerken.
    >
    > Rijen bronrechten afkomstig uit de abonnementslicentie. De machtigingswaarden van het recht hebben voorrang op waarden in andere machtigingensets als deze een hogere volgorde hebben. Een waarde in een niet-recht machtigingenset met een hogere volgorde dan de gerelateerde waarde in het recht worden geplaatst tussen haakjes om aan te geven dat het niet effectief is omdat het wordt overschreven door het recht.
    >
    > Zie voor een uitleg van volgorde [Een machtigingenset maken](ui-define-granular-permissions.md#to-create-a-permission-set).  

4. Als u een machtigingenset wilt bewerken, kiest u in het gedeelte **Op machtigingenset-id**, op de regel voor een relevante machtigingenset van het soort **Door gebruiker gedefinieerd**, een van de vijf toegangstypevelden en selecteert u een andere waarde.

5. Als u afzonderlijke toegangsrechten binnen de machtigingenset wilt bewerken, kiest u de waarde in het veld **Machtigingenset** om de pagina **Machtigingen** te openen.

> [!NOTE]  
> Wanneer u een machtiging bewerkt, worden de wijzigingen ook toegepast op andere gebruikers aan wie de machtigingenset is toegewezen.

### <a name="security-filters-limit-a-users-access-to-specific-records-in-a-table"></a>Beveiligingsfilters beperken de toegang van een gebruiker tot specifieke records in een tabel

Voor beveiliging op recordniveau in [!INCLUDE[prod_short](includes/prod_short.md)] gebruikt u beveiligingsfilters om de toegang van een gebruiker tot gegevens in een tabel te beperken. U maakt beveiligingsfilters voor tabelgegevens. Een beveiligingsfilter beschrijft een set records in een tabel waarvoor een gebruiker toegangsrechten heeft. U kunt bijvoorbeeld opgeven dat een gebruiker alleen de records kan lezen die gegevens over een bepaalde klant bevatten. Zo heeft de gebruiker geen toegang tot de records die informatie over andere klanten bevatten. Zie voor meer informatie [Beveiligingsfilters gebruiken](/dynamics365/business-central/dev-itpro/security/security-filters) in de beheerinhoud.

## <a name="viewing-permission-changes-telemetry"></a>Telemetrie van machtigingswijzigingen weergeven

U kunt [!INCLUDE[prod_short](includes/prod_short.md)] instellen om wijzigingen die zijn aangebracht in een machtiging, naar een Application Insights-resource in Microsoft Azure te sturen. Vervolgens maakt u met behulp van Azure Monitor rapporten en stelt u waarschuwingen in voor de verzamelde gegevens. Zie voor meer informatie de volgende artikelen in de [!INCLUDE[prod_short](includes/prod_short.md)] Help voor ontwikkelaar en beheerders:

- [Telemetrie bewaken en analyseren - inschakelen Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Veldbewakingstelemetrie bekijken](/dynamics365/business-central/dev-itpro/administration/telemetry-permission-changes-trace)

## <a name="delegated-admin-users"></a>Gedelegeerde beheerders

[!INCLUDE [admin-gdap-users](includes/admin-gdap-users.md)]

## <a name="see-also"></a>Zie ook

[Gebruikers maken volgens licenties](ui-how-users-permissions.md)  
[Profielen beheren](admin-users-profiles-roles.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)  
[Aanpassen [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Beheer](admin-setup-and-administration.md)  
[Gebruikers aan Microsoft 365 toevoegen voor bedrijven](/microsoft-365/admin/add-users/add-users)  
[Beveiliging en bescherming in Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) in de Help voor ontwikkelaars en IT-professionals  
[Een telemetrie-id toewijzen aan gebruikers](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights#assign-a-telemetry-id-to-users)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
