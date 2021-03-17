---
title: 'Gedetailleerde machtigingen definiëren | Microsoft Docs '
description: Beschrijft hoe u gebruikers toegang tot objecten geeft door machtigingen aan hen toe te wijzen.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 10/01/2020
ms.author: edupont
ms.openlocfilehash: 48547fbe3cb2bb7cf509c1b0720cb6ccfc58cd97
ms.sourcegitcommit: ff2b55b7e790447e0c1fcd5c2ec7f7610338ebaa
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5385886"
---
# <a name="assign-permissions-to-users-and-groups"></a>Machtigingen toewijzen aan gebruikers en groepen

In het beveiligingssysteem van [!INCLUDE[prod_short](includes/prod_short.md)] kunt u bepalen tot welke objecten binnen elke database of omgeving een gebruiker toegang krijgt. U kunt voor elke gebruiker opgeven of deze gegevens in de geselecteerde databaseobjecten mag lezen, wijzigen of invoeren. Zie [Gegevensbeveiliging](/dynamics365/business-central/dev-itpro/security/data-security?tabs=object-level) in de Help voor ontwikkelaars en IT-professionals voor [!INCLUDE[prod_short](includes/prod_short.md)] voor meer informatie.

Voordat u machtigingen toewijst aan gebruikers en gebruikersgroepen, moet u definiëren wie zich mag aanmelden door gebruikers te maken volgens de licentie die in het Microsoft 365 Beheercentrum is gedefinieerd. Zie [Gebruikers maken volgens licenties](ui-how-users-permissions.md) voor meer informatie.

[!INCLUDE[prod_short](includes/prod_short.md)] bevat twee machtigingsniveaus voor databaseobjecten:

- Algemene machtigingen volgens de licentie, ook wel een recht genoemd.
- Meer gedetailleerde machtigingen, zoals deze zijn toegewezen vanuit [!INCLUDE[prod_short](includes/prod_short.md)].

Om het gemakkelijker te maken om machtigingen voor meerdere gebruikers te beheren, kunt u ze organiseren in gebruikersgroepen en zo in één actie één machtigingsset voor meerdere gebruikers toewijzen of wijzigen. Zie [Machtigingen beheren via gebruikersgroepen](ui-define-granular-permissions.md#to-manage-permissions-through-user-groups) voor meer informatie.

> [!NOTE]
> Nog een methode om te definiëren welke functies voor een gebruiker toegankelijk zijn, is via het veld **Ervaring** op de pagina **Bedrijfsinformatie**. Zie voor meer informatie [Wijzigen welke functies worden weergegeven](ui-experiences.md).
>
> U kunt ook definiëren wat gebruikers in de gebruikersinterface kunnen zien en hoe ze omgaan met hun toegestane functionaliteit. Dit doet u door middel van profielen die u toewijst aan verschillende soorten gebruikers, afhankelijk van hun functie of afdeling. Zie voor meer informatie [Profielen beheren](admin-users-profiles-roles.md) en [Aanpassen [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md).

## <a name="to-assign-permission-sets-to-users"></a>Machtigingssets toewijzen aan gebruikers

Een machtigingsset is een verzameling machtigingen voor specifieke databaseobjecten. Aan alle gebruikers moeten een of meer machtigingensets worden toegewezen voordat ze toegang hebben tot [!INCLUDE[prod_short](includes/prod_short.md)].

Een [!INCLUDE[prod_short](includes/prod_short.md)]-oplossing bevat een aantal vooraf gedefinieerde machtigingssets die door Microsoft of uw oplossingsprovider zijn toegevoegd. U kunt ook nieuwe machtigingssets toevoegen die zijn afgestemd op de behoeften van uw organisatie. Zie voor meer informatie [Een machtigingenset maken of bewerken](ui-define-granular-permissions.md#to-create-or-modify-a-permission-set).

> [!NOTE]
> Als u de toegang van een gebruiker niet meer wilt beperken dan in de licentie is gedefinieerd, kunt u een speciale machtigingsset met de naam SUPER toewijzen aan de gebruiker. Deze machtigingsset zorgt ervoor dat de gebruiker toegang heeft tot alle objecten die in de licentie zijn opgegeven.
>
> Een gebruiker met de Essential-licentie en de SUPER-machtigingsset heeft toegang tot meer functionaliteit dan gebruikers met de Team Member-licentie en de SUPER-machtigingsset.

U kunt machtigingssets op twee manieren aan gebruikers toewijzen:

- Vanaf de pagina **Gebruikerskaart** door machtigingssets te selecteren om aan de gebruiker toe te wijzen.
- Vanaf de pagina **Machtigingsset per gebruiker** door gebruikers te selecteren aan wie een machtigingsset is toegewezen.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Een machtigingenset op een gebruikerskaart toewijzen

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikers** in en kies de desbetreffende koppeling.
2. Selecteer de gebruiker waaraan u machtigingen wilt toewijzen.
Alle machtigingensets die al zijn toegewezen aan de gebruiker worden weergegeven in het feitenblok **Machtigingensets**.
3. Kies de actie **Bewerken** om de pagina **Gebruikerskaart** te openen.
4. Vul op het sneltabblad **Gebruikersmachtigingensets** waar nodig de velden in op een nieuwe regel. Zie voor meer informatie [Een machtigingenset maken of bewerken](ui-define-granular-permissions.md#to-create-or-modify-a-permission-set).

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Een machtigingenset op de pagina Machtigingenset per gebruiker toewijzen

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikers** in en kies de desbetreffende koppeling.
2. Selecteer op de pagina **Gebruikers** de betreffende gebruiker en kies de actie **Machtigingenset per gebruiker**.
3. Selecteer op de pagina **Machtigingenset per gebruiker** het selectievakje **[gebruikersnaam]** op een regel voor de betreffende machtigingenset om de set aan de gebruiker toe te wijzen.
4. Selecteer het selectievakje **Alle gebruikers** om de machtigingenset aan alle gebruikers toe te wijzen.

## <a name="to-get-an-overview-of-a-users-permissions"></a>Een overzicht krijgen van de machtigingen van een gebruiker

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikers** in en kies de desbetreffende koppeling.
2. Open de kaart van de betreffende gebruiker.
3. Kies de actie **Effectieve machtigingen**.

    Het deel **Machtigingen** bevat alle databaseobjecten waartoe de gebruiker toegang heeft. U kunt dit gedeelte niet bewerken.

    Het deel **Op machtigingenset-id** bevat de toegewezen machtigingensets waarmee de machtigingen aan de gebruiker worden verleend, de bron en het type van de machtigingenset en de mate waarin de verschillende toegangstypen toegestaan zijn.

    Voor elke rij die u selecteert in de sectie **Machtigingen**, bevat de sectie **Op machtigingenset-id** de machtigingenset of -sets waarmee de machtiging wordt verleend. In dit gedeelte kunt u de waarde wijzigen in elk van de vijf toegangstypevelden, **Lezen**, **Invoegen**, **Wijzigen**, **Verwijderen** en **Uitvoeren**.

    > [!NOTE]  
    > U kunt alleen machtigingensets van het soort **Door gebruiker gedefinieerd** bewerken.
    >
    > Rijen bronrechten afkomstig uit de abonnementslicentie. De machtigingswaarden van het recht hebben voorrang op waarden in andere machtigingensets als deze een hogere volgorde hebben. Een waarde in een niet-recht machtigingenset met een hogere volgorde dan de gerelateerde waarde in het recht worden geplaatst tussen haakjes om aan te geven dat het niet effectief is omdat het wordt overschreven door het recht.
    >
    > Zie voor een uitleg van volgorde [Machtigingen handmatig maken of wijzigen](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).  

4. Als u een machtigingenset wilt bewerken, kiest u in het gedeelte **Op machtigingenset-id**, op de regel voor een relevante machtigingenset van het soort **Door gebruiker gedefinieerd**, een van de vijf toegangstypevelden en selecteert u een andere waarde.

5. Als u afzonderlijke toegangsrechten binnen de machtigingenset wilt bewerken, kiest u de waarde in het veld **Machtigingenset** om de pagina **Machtigingen** te openen. Volg de stappen die worden beschreven bij [Machtigingen maken of bewerken](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).  

> [!NOTE]  
> Wanneer u een machtiging bewerkt, worden de wijzigingen ook toegepast op andere gebruikers aan wie de machtigingenset is toegewezen.

## <a name="to-create-or-modify-a-permission-set"></a>Een machtigingenset maken of wijzigen

Machtigingensets fungeren als containers met machtigingen, zodat u gemakkelijk meerdere machtigingen in één record kunt beheren.

> [!NOTE]  
> Een [!INCLUDE[prod_short](includes/prod_short.md)]-oplossing bevat doorgaans een aantal vooraf gedefinieerde machtigingensets die door Microsoft of door uw softwareprovider worden toegevoegd. Deze machtigingensets zijn van het type **Systeem** of **Extensie**. U kunt deze typen machtigingensets of de machtigingen die zich erin bevinden, niet maken of bewerken. U kunt ze echter kopiëren om uw eigen machtigingensets en machtigingen te definiëren.
>
> Machtigingensets die gebruikers maken, nieuw of als kopieën, zijn van het type **Door gebruiker gedefinieerd** en kunnen worden bewerkt.

### <a name="to-create-new-permission-set-from-scratch"></a>Een geheel nieuwe machtigingsset maken

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Machtigingssets** in en kies de desbetreffende koppeling.
2. Als u een nieuwe machtigingenset wilt maken, kiest u de actie **Nieuw**.
3. Vul op de nieuwe regel de velden indien nodig in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] Wanneer u een machtigingsset hebt gemaakt, moet u de feitelijke machtigingen toevoegen. Zie voor meer informatie [Machtigingen handmatig maken of wijzigen](ui-define-granular-permissions.md#to-create-or-modify-permissions-manually).

### <a name="to-copy-a-permission-set"></a>Een machtigingenset kopiëren

U kunt ook een kopieerfunctie gebruiken om snel alle machtigingen uit een andere machtigingsset naar een nieuwe machtigingsset over te brengen.

> [!NOTE]  
> Als een systeemmachtigingenset die u hebt gekopieerd wordt gewijzigd, wordt u geïnformeerd (afhankelijk van uw selectie), zodat u kunt overwegen of de wijzigingen relevant zijn om naar uw door de gebruiker gedefinieerde machtigingenset te kopiëren of te schrijven.

1. Op de pagina **Machtigingensets** selecteert u de naam van een machtigingenset die u wilt kopiëren en kiest u vervolgens de actie **Machtigingenset kopiëren**.
2. Op de pagina **Machtigingenset kopiëren** geeft u de naam op van de nieuwe machtigingenset en kies de knop **OK**.
3. Selecteer het selectievakje **Informeren bij gewijzigde machtigingenset** als u een koppeling tussen de oorspronkelijke en gekopieerde machtigingensets wilt bijhouden. De koppeling wordt vervolgens gebruikt om u te melden als de naam of inhoud van de oorspronkelijke machtigingenset in een toekomstige versie van de oplossing verandert.

De nieuwe machtigingenset, die alle machtigingen van de gekopieerde machtigingenset bevat, wordt toegevoegd als nieuwe regel op de pagina **Machtigingensets**. Nu kunt u machtigingen in de nieuwe machtigingsset wijzigen. De regels worden alfabetisch gesorteerd binnen elk type.

### <a name="to-export-and-import-a-permission-set"></a>Een machtigingenset exporteren en importeren

Om snel machtigingen in te stellen, kunt u machtigingensets importeren die u vanuit een andere [!INCLUDE[prod_short](includes/prod_short.md)]-tenant hebt geëxporteerd.

In omgevingen met meerdere tenants wordt een machtigingenset geïmporteerd in een specifieke tenant, dus het bereik van de import is 'Tenant'.

1. Selecteer in tenant 1 op de pagina **Machtigingensets** de regel of regels van de machtigingensets die u wilt kopiëren en kies vervolgens de actie **Machtigingensets exporteren**.

    Er wordt een XML-bestand gemaakt in de downloadmap op uw computer. Standaard heet het 'Export Permission Sets.xml'

2. Selecteer in tenant 2 op de pagina **Machtigingensets** de actie **Machtigingensets importeren**.
3. Bedenk op de dialoogpagina **Machtigingensets importeren** of u bestaande machtigingensets wilt samenvoegen met nieuwe machtigingensets in het xml-bestand.

    Als u het selectievakje **Bestaande machtigingen bijwerken** inschakelt, worden bestaande machtigingensets met dezelfde naam als die in het xml-bestand samengevoegd met de geïmporteerde machtigingensets.

    Als u het selectievakje **Bestaande machtigingen bijwerken** niet inschakelt, worden bestaande machtigingensets met dezelfde naam als die in het xml-bestand overgeslagen tijdens import. In dat geval wordt u op de hoogte gesteld van machtigingensets die worden overgeslagen.

4. Zoek en selecteer op de dialoogpagina **Importeren** het XML-bestand dat u wilt importeren en kies vervolgens de actie **Openen**.

De machtigingensets worden geïmporteerd.

## <a name="to-create-or-modify-permissions-manually"></a>Machtigingen handmatig maken of wijzigen

In deze procedure wordt uitgelegd hoe u handmatig machtigingen toevoegt of bewerkt. U kunt ook automatisch machtigingen laten genereren vanuit uw acties in de UI. Zie [Machtigingen maken of wijzigen door uw acties op te nemen](ui-define-granular-permissions.md#to-create-or-modify-permissions-by-recording-your-actions) voor meer informatie.

> [!NOTE]
> Wanneer u een machtiging bewerkt en daarmee de gerelateerde machtigingenset, worden de wijzigingen ook toegepast op andere gebruikers aan wie de machtigingenset is toegewezen.

1. Op de pagina **Machtigingensets** selecteert u de regel voor een machtigingenset en kiest u vervolgens de actie **Machtigingen**.
2. Maak op de pagina **Machtigingen** een nieuwe regel of bewerk de velden op een bestaande regel.

In elk van de vijf toegangstypevelden, **Lezen**, **Invoegen**, **Wijzigen**, **Verwijderen** en **Uitvoeren** kunt u een van de volgende drie machtigingsopties selecteren:

|Optie|Description|Volgorde|
|------|-----------|-------|
|**Ja**|De gebruiker kan de actie op het betreffende object uitvoeren.|Hoogste|
|**Indirect**|De gebruiker kan de actie op het betreffende object uitvoeren maar alleen via een ander, gerelateerd object waartoe de gebruiker volledige toegang heeft. Zie [Eigenschap Machtigingen](/dynamics365/business-central/dev-itpro/developer/properties/devenv-permissions-property) in Help voor ontwikkelaars en IT-Pro voor meer informatie over indirecte machtigingen|Op een na hoogste|
|**Leeg**|De gebruiker kan de actie niet op het betreffende object uitvoeren.|Laagste|

### <a name="example---indirect-permission"></a>Voorbeeld: indirecte machtiging

U kunt een indirecte machtiging toewijzen om een object enkel door middel van een ander object te laten gebruiken.
Een gebruiker kan bijvoorbeeld machtiging hebben om codeunit 80, verkoop-boeken uit te voeren. De codeunit Verkoop-boeken voert veel taken uit, waaronder het wijzigen van tabel 37, Inkoopregel. Wanneer de gebruiker een verkoopdocument boekt, de codeunit Verkoop-boeken, controleert [!INCLUDE[prod_short](includes/prod_short.md)] of de gebruiker de machtiging heeft om de tabel Verkoopregel te wijzigen. Als dat niet het geval is, kan de codeunit de taken niet uitvoeren en ontvangt de gebruiker een foutmelding. Indien dit wel zo is, wordt de codeunit uitgevoerd.

De gebruiker hoeft echter geen volledige toegang te hebben tot de tabel Inkoopregel om de codeunit uit te voeren. Als de gebruiker indirecte machtiging heeft voor de tabel Verkoopregel, kan de codeunit Verkoop-boeken worden uitgevoerd. Wanneer een gebruiker een indirecte machtiging heeft, kan die gebruiker enkel de tabel Inkoopregel wijzigen door de codeunit Verkoop-boeken of een ander object uit te voeren dat machtiging heeft om de tabel Inkoopregel te wijzigen. De gebruiker kan alleen de tabel Inkoopregel wijzigen vanuit de ondersteunde toepassingsgebieden. De gebruiker kan de functie niet per ongeluk of opzettelijk op andere manieren uitvoeren.

## <a name="to-create-or-modify-permissions-by-recording-your-actions"></a>Machtigingen maken of wijzigen door uw acties op te nemen

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Machtigingssets** in en kies de desbetreffende koppeling.
2. U kunt ook op de pagina **Gebruikers** de actie **Machtigingensets** kiezen.
3. Kies op de pagina **Machtigingensets** de actie **Nieuw**.
4. Vul op een nieuwe regel de velden indien nodig in.
5. Kies de actie **Machtigingen**.
6. Kies op de pagina **Machtigingen** de actie **Machtigingen registreren** en kies de actie **Starten**.

    Hierdoor wordt een opnameproces wordt gestart dat al uw acties in de gebruikersinterface vastlegt.
7. Ga naar de verschillende pagina's en activiteiten in [!INCLUDE[prod_short](includes/prod_short.md)] waartoe u gebruikers met deze machtigingenset toegang wilt verlenen. U moet de taken uitvoeren waarvoor u machtigingen wilt opnemen.
8. Om de opname te stoppen, gaat u terug naar de pagina **Machtigingen** en kiest u de actie **Stoppen**.
9. Kies de knop **Ja** om de opgenomen toegangsrechten aan de nieuwe machtigingenset toe te voegen.
10. Geef voor elk object in de opgenomen lijst aan of gebruikers records mogen invoegen, wijzigen of verwijderen in de opgenomen tabellen.

## <a name="security-filters---to-limit-a-users-access-to-specific-records-in-a-table"></a>Beveiligingsfilters - De toegang van een gebruiker tot specifieke records in een tabel beperken

Voor beveiliging op recordniveau in [!INCLUDE[prod_short](includes/prod_short.md)] gebruikt u beveiligingsfilters om de toegang van een gebruiker tot gegevens in een tabel te beperken. U maakt beveiligingsfilters voor tabelgegevens. Een beveiligingsfilter beschrijft een set records in een tabel waarvoor een gebruiker toegangsrechten heeft. U kunt bijvoorbeeld opgeven dat een gebruiker alleen de records kan lezen die gegevens over een bepaalde klant bevatten. Dit betekent dat de gebruiker geen toegang heeft tot de records die informatie over andere klanten bevatten. Zie voor meer informatie [Beveiligingsfilters gebruiken](/dynamics365/business-central/dev-itpro/security/security-filters) in de Help voor ontwikkelaars en IT-pro.

## <a name="to-manage-permissions-through-user-groups"></a>Machtigingen beheren via gebruikersgroepen

U kunt gebruikersgroepen instellen om machtigingssets voor groepen gebruikers in uw bedrijf te beheren.

Maak eerst een gebruikersgroep. Wijs daarna machtigingssets toe aan de groep om te definiëren welk object toegankelijk is voor gebruikers van de groep. Wanneer u gebruikers aan de groep toevoegt, gelden de machtigingssets die voor de groep zijn ingesteld, ook voor deze gebruikers.

Machtigingssets die via een gebruikersgroep aan een gebruiker zijn toegewezen, blijven gesynchroniseerd, zodat een wijziging in de gebruikersgroepmachtigingen automatisch naar de gebruiker wordt doorgevoerd. Als u een gebruiker uit een gebruikersgroep verwijdert, worden de desbetreffende machtigingen automatisch ingetrokken.

### <a name="to-group-users-in-user-groups"></a>Gebruikers in gebruikersgroepen samenvoegen

De onderstaande procedure licht toe hoe u handmatig gebruikersgroepen maakt. Zie [Een gebruikersgroep en alle bijbehorende machtigingssets kopiëren](ui-define-granular-permissions.md#to-copy-a-user-group-and-all-its-permission-sets) als u automatisch gebruikersgroepen wilt maken.

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikersgroepen** in en kies de desbetreffende koppeling.
2. U kunt ook op de pagina **Gebruikers** de actie **Gebruikersgroepen** kiezen.
3. Kies op de pagina **Gebruikersgroep** de actie **Gebruikersgroepsleden**.
4. Kies op de pagina **Gebruikersgroep** de actie **Gebruikers toevoegen**.

### <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Een gebruikersgroep en alle bijbehorende machtigingensets kopiëren

Als u snel een nieuwe gebruikersgroep wilt definiëren, kopieert u alle machtigingensets van een bestaande gebruikersgroep naar de nieuwe gebruikersgroep.

> [!NOTE]
> De leden van de gebruikersgroep worden niet gekopieerd naar de nieuwe gebruikersgroep. Dit moet u handmatig achteraf doen. Zie voor meer informatie [Gebruikers in gebruikersgroepen samenvoegen](ui-define-granular-permissions.md#to-group-users-in-user-groups).

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikersgroepen** in en kies de desbetreffende koppeling.
2. Selecteer de gebruikersgroep die u wilt kopiëren, en kies vervolgens de actie **Gebruikersgroep kopiëren**.
3. Voer in het veld **Nieuwe gebruikersgroepcode** een naam voor de groep in en kies vervolgens de knop **OK**.

De nieuwe gebruikersgroep wordt toegevoegd aan de pagina **Gebruikersgroepen**. Voeg gebruikers toe. Zie [Gebruikers in gebruikersgroepen groeperen](ui-define-granular-permissions.md#to-group-users-in-user-groups) voor meer informatie.  

### <a name="to-assign-permission-sets-to-user-groups"></a>Machtigingssets toewijzen aan gebruikersgroepen

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikersgroepen** in en kies de desbetreffende koppeling.
2. Selecteer de gebruikersgroep waaraan u een machtiging wilt toewijzen.
Alle machtigingensets die al zijn toegewezen aan de gebruiker worden weergegeven in het feitenblok **Machtigingensets**.
3. Kies de actie **Machtigingssets voor gebruikers** om de pagina **Machtigingssets voor gebruikers** te openen.
4. Vul op de pagina **Machtigingssets voor gebruikers** op een nieuwe regel de vereiste velden in.

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-group-page"></a>Een machtigingsset toewijzen op de pagina **Machtigingsset per gebruikersgroep**

De volgende procedure licht toe hoe u machtigingssets aan een gebruikersgroep toewijst vanaf de pagina **Machtigingsset per gebruikersgroep**.

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikers** in en kies de desbetreffende koppeling.
2. Selecteer de desbetreffende gebruiker op de pagina **Gebruikers** en kies de actie **Machtigingsset per gebruikersgroep**.
3. Selecteer op de pagina **Machtigingsset per gebruikersgroep** het selectievakje **[naam van gebruikersgroep]** op een regel voor de desbetreffende machtigingsset om de set aan de gebruikersgroep toe te wijzen.
4. Schakel het selectievakje **Alle gebruikersgroepen** in om de machtigingsset aan alle gebruikersgroepen toe te wijzen.

## <a name="to-remove-obsolete-permissions-from-all-permission-sets"></a>Verouderde machtigingen uit alle machtigingensets verwijderen

1. Kies op de pagina **Machtigingensets** de actie **Verouderde machtigingen verwijderen**.

## <a name="to-set-up-user-time-constraints"></a>Tijdsbeperkingen voor gebruikers instellen

Beheerders kunnen perioden definiëren waarin opgegeven gebruikers kunnen boeken en ook kunnen opgeven of het systeem de tijdsduur vastlegt gedurende welke gebruikers zijn aangemeld. Beheerders kunnen ook divisies toewijzen aan gebruikers. Zie [Werken met divisies](inventory-responsibility-centers.md) voor meer informatie.

1. Kies het pictogram ![Gloeilamp om de Vertel mij-functie te openen](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruiker instellen** in en kies de desbetreffende koppeling.
2. Kies op de pagina **Gebruikersinstellingen** die wordt geopend, de actie **Nieuw**.
3. Voer in het veld **Gebruikers-id** de id van een gebruiker in of kies het veld om alle huidige Windows-gebruikers in het systeem te zien.
4. Vul de vereiste velden in.


## <a name="viewing-permission-changes-telemetry"></a>Telemetrie van machtigingswijzigingen weergeven 

U kunt [!INCLUDE[prod_short](includes/prod_short.md)] instellen om wijzigingen die zijn aangebracht in een machtiging, naar een Application Insights-resource in Microsoft Azure te sturen. Vervolgens maakt u met behulp van Azure Monitor rapporten en stelt u waarschuwingen in voor de verzamelde gegevens. Zie voor meer informatie de volgende artikelen in de [!INCLUDE[prod_short](includes/prod_short.md)] Ontwikkelaar en IT Pro Help:

- [Telemetrie bewaken en analyseren - inschakelen Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-overview#enable)
- [Veldbewakingstelemetrie bekijken](/dynamics365/business-central/dev-itpro/administration/telemetry-permission-changes-trace)

## <a name="see-also"></a>Zie ook

[Gebruikers maken volgens licenties](ui-how-users-permissions.md)  
[Profielen beheren](admin-users-profiles-roles.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)  
[Aanpassen [!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Beheer](admin-setup-and-administration.md)  
[Gebruikers toevoegen aan Microsoft 365 voor bedrijven](https://aka.ms/CreateOffice365Users)  
[Beveiliging en bescherming in Business Central](/dynamics365/business-central/dev-itpro/security/security-and-protection) in de Help voor ontwikkelaars en IT-professionals


[!INCLUDE[footer-include](includes/footer-banner.md)]