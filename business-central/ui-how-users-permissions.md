---
title: Gebruikersmachtigingen toewijzen of bewerken | Microsoft Docs
description: Hier wordt beschreven hoe u Office 365-gebruikers toevoegt aan Business Central en vervolgens machtigingen, toegangsrechten en beveiligingsinstellingen toewijst.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: access, right, security
ms.date: 11/08/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: add32e82465610830b68a979e238103bfa10d438
ms.openlocfilehash: 78e83ee0740531935bd30a5988a72d1421a1fd89
ms.contentlocale: nl-be
ms.lasthandoff: 11/29/2018

---
# <a name="managing-users-and-permissions"></a>Gebruikers en machtigingen beheren
Als u gebruikers wilt toevoegen in [!INCLUDE[d365fin](includes/d365fin_md.md)], moet de Office 365-beheerder van uw bedrijf eerst de gebruikers in het Office 365-beheercentrum maken. Zie voor meer informatie [Gebruikers aan Office 365 toevoegen voor bedrijven](https://aka.ms/CreateOffice365Users).

Als gebruikers in Office 365 zijn gemaakt, kunnen ze op de pagina **Gebruikers** worden geïmporteerd in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Aan gebruikers worden machtigingensets toegewezen op basis van het plan dat aan de gebruiker is toegewezen in Office 365. Voor gedetailleerde informatie over licenties raadpleegt u de [Microsoft Dynamics 365 Business Central Licentiehandleiding](https://aka.ms/BusinessCentralLicensing).

U kunt vervolgens machtigingensets aan gebruikers toewijzen om te bepalen tot welke databaseobjecten (en daardoor tot welke UI-elementen) zij toegang hebben en in welke bedrijven. U kunt gebruikers toevoegen aan gebruikersgroepen. Hierdoor wordt het gemakkelijker om dezelfde machtigingensets aan meerdere gebruikers toe te wijzen.

Een machtigingenset is een verzameling machtigingen voor bepaalde objecten in de database. Aan alle gebruikers moeten een of meer machtigingensets worden toegewezen voordat ze toegang hebben tot [!INCLUDE[d365fin](includes/d365fin_md.md)].

Vanuit de pagina **Gebruikerskaart**, kunt u de pagina **Effectieve machtigingen** openen om te zien welke machtigingen de gebruiker heeft en welke machtigingensets aan hen zijn verleend. Hier kunt u machtigingsdetails wijzigen voor machtigingensets van het type **Door gebruiker gedefinieerd**. Zie voor meer informatie het gedeelte "Machtigingen van een gebruiker weergeven of bewerken".

Beheerders kunnen de pagina **Gebruikersinstellingen** gebruiken om perioden te definiëren waarin opgegeven gebruikers kunnen boeken en ook kunnen opgeven of het systeem de tijdsduur vastlegt gedurende welke gebruikers zijn aangemeld.

Een ander systeem dat definieert waartoe gebruikers toegang hebben, is de instelling Ervaring. Zie voor meer informatie [Wijzigen welke functies worden weergegeven](ui-experiences.md).

## <a name="to-add-a-user-in-business-central"></a>Een gebruiker in Business Central toevoegen
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikers** in en kies vervolgens de gerelateerde koppeling.
2. Kies de actie **Gebruikers ophalen uit Office 365**.

Elke nieuwe gebruiker die wordt gemaakt voor uw Office 365-abonnement, wordt op de pagina **Gebruikers** toegevoegd.

## <a name="to-group-users-in-a-user-group"></a>Gebruikers in gebruikersgroepen samenvoegen
U kunt gebruikersgroepen instellen om u te helpen machtigingensets te beheren voor groepen gebruikers in uw bedrijf.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikersgroepen** in en kies vervolgens de gerelateerde koppeling.
2. U kunt ook op de pagina **Gebruikers** de actie **Gebruikersgroepen** kiezen.
3. Kies op de pagina **Gebruikersgroep** de actie **Gebruikersgroepsleden**.
4. Kies op de pagina **Gebruikersgroep** de actie **Gebruikers toevoegen**.

Wanneer gebruikers of gebruikersgroepen worden gemaakt, moet u machtigingensets aan elke groep toewijzen om te definiëren tot welk object een gebruiker toegang heeft. Eerst moet u de juiste machtigingen ordenen in machtigingensets. Zie voor meer informatie het gedeelte "Een machtigingset maken of bewerken".

## <a name="to-copy-a-user-group-and-all-its-permission-sets"></a>Een gebruikersgroep en alle bijbehorende machtigingensets kopiëren
Als u snel een nieuwe gebruikersgroep wilt definiëren, kopieert u alle machtigingensets van een bestaande gebruikersgroep naar de nieuwe gebruikersgroep.

De leden van de gebruikersgroep worden niet gekopieerd naar de nieuwe gebruikersgroep. Dit moet u handmatig achteraf doen.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikersgroepen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de gebruikersgroep die u wilt kopiëren, en kies vervolgens de actie **Gebruikersgroep kopiëren**.
3. Voer in het veld **Nieuwe gebruikersgroepcode** een naam voor de groep in en kies vervolgens de knop **OK**.

De nieuwe gebruikersgroep wordt toegevoegd aan de pagina **Gebruikersgroepen**. Voeg gebruikers toe. Zie voor meer informatie het gedeelte "Gebruikers in gebruikersgroepen samenvoegen".  

## <a name="to-set-up-user-time-constraints"></a>Tijdsbeperkingen voor gebruikers instellen
Beheerders kunnen perioden definiëren waarin opgegeven gebruikers kunnen boeken en ook kunnen opgeven of het systeem de tijdsduur vastlegt gedurende welke gebruikers zijn aangemeld. Beheerders kunnen ook divisies toewijzen aan gebruikers. Zie [Werken met divisies](inventory-responsibility-centers.md) voor meer informatie.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikersinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Kies op de pagina **Gebruikersinstellingen** die wordt geopend, de actie **Nieuw**.
3. Voer in het veld **Gebruikers-id** de id van een gebruiker in of kies het veld om alle huidige Windows-gebruikers in het systeem te zien.
4. Vul de benodigde velden in.

## <a name="to-create-or-modify-a-permission-set"></a>Een machtigingenset maken of wijzigen
Machtigingensets fungeren als containers met machtigingen, zodat u gemakkelijk meerdere machtigingen in één record kunt beheren. Wanneer u een machtigingenset hebt gemaakt, moet u de werkelijke machtigingen toevoegen. Zie voor meer informatie het gedeelte "Machtigingen maken of bewerken".

> [!NOTE]  
> Een [!INCLUDE[d365fin](includes/d365fin_md.md)]-oplossing bevat doorgaans een aantal vooraf gedefinieerde machtigingensets die door Microsoft of door uw softwareprovider worden toegevoegd. Deze machtigingensets zijn van het type **Systeem** of **Extensie**. U kunt deze typen machtigingensets of de machtigingen die zich erin bevinden, niet maken of bewerken. U kunt ze echter kopiëren om uw eigen machtigingensets en machtigingen te definiëren. <br /><br />
Machtigingensets die gebruikers maken, nieuw of als kopieën, zijn van het type **Door gebruiker gedefinieerd** en kunnen worden bewerkt.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Machtigingensets** in en kies vervolgens de gerelateerde koppeling.
2. Als u een nieuwe machtigingenset wilt maken, kiest u de actie **Nieuw**.
3. Vul op de nieuwe regel de velden indien nodig in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### <a name="to-copy-a-permission-set"></a>Een machtigingenset kopiëren
Wanneer u nieuwe machtigingensets maakt, kunt u een kopieerfunctie gebruiken om snel alle machtigingen van een andere machtigingenset naar een nieuwe over te dragen.

> [!NOTE]  
> Als een systeemmachtigingenset die u hebt gekopieerd wordt gewijzigd, wordt u geïnformeerd (afhankelijk van uw selectie), zodat u kunt overwegen of de wijzigingen relevant zijn om naar uw door de gebruiker gedefinieerde machtigingenset te kopiëren of te schrijven.

1. Op de pagina **Machtigingensets** selecteert u de naam van een machtigingenset die u wilt kopiëren en kiest u vervolgens de actie **Machtigingenset kopiëren**.
2. Op de pagina **Machtigingenset kopiëren** geeft u de naam op van de nieuwe machtigingenset en kies de knop **OK**.
3. Selecteer het selectievakje **Informeren bij gewijzigde machtigingenset** als u een koppeling tussen de oorspronkelijke en gekopieerde machtigingensets wilt bijhouden. De koppeling wordt vervolgens gebruikt om u te melden als de naam of inhoud van de oorspronkelijke machtigingenset in een toekomstige versie van de oplossing verandert.

De nieuwe machtigingenset, die alle machtigingen van de gekopieerde machtigingenset bevat, wordt toegevoegd als nieuwe regel op de pagina **Machtigingensets**. De regels worden alfabetisch gesorteerd binnen elk type.

## <a name="to-create-or-modify-permissions-manually"></a>Machtigingen handmatig maken of wijzigen
In deze procedure wordt uitgelegd hoe u handmatig machtigingen toevoegt of bewerkt. U kunt machtigingensets ook automatisch laten genereren vanuit uw acties in de gebruikersinterface. Zie voor meer informatie de sectie "Machtigingensets maken of bewerken door uw acties op te nemen".

1. Op de pagina **Machtigingensets** selecteert u de regel voor een machtigingenset en kiest u vervolgens de actie **Machtigingen**.
2. Maak op de pagina **Machtigingen** een nieuwe regel of bewerk de velden op een bestaande regel.

In elk van de vijf toegangstypevelden, **Lezen**, **Invoegen**, **Wijzigen**, **Verwijderen** en **Uitvoeren** kunt u een van de volgende drie machtigingsopties selecteren:

|Optie|Description|Volgorde|
|------|-----------|
|**Ja**|De gebruiker kan de actie op het betreffende object uitvoeren.|Hoogste|
|**Indirect**|De gebruiker kan de actie op het betreffende object uitvoeren maar alleen via een ander, gerelateerd object waartoe de gebruiker volledige toegang heeft.|Op een na hoogste|
|**Leeg**|De gebruiker kan de actie niet op het betreffende object uitvoeren.|Laagste|

### <a name="example---indirect-permission"></a>Voorbeeld: indirecte machtiging
U kunt een indirecte machtiging toewijzen om een object enkel door middel van een ander object te laten gebruiken.
Een gebruiker kan bijvoorbeeld machtiging hebben om codeunit 80, verkoop-boeken uit te voeren. De codeunit Verkoop-boeken voert veel taken uit, waaronder het wijzigen van tabel 37, Inkoopregel. Wanneer de gebruiker een verkoopdocument boekt, de codeunit Verkoop-boeken, controleert [!INCLUDE[d365fin](includes/d365fin_md.md)] of de gebruiker de machtiging heeft om de tabel Verkoopregel te wijzigen. Als dat niet het geval is, kan de codeunit de taken niet uitvoeren en ontvangt de gebruiker een foutmelding. Indien dit wel zo is, wordt de codeunit uitgevoerd.

De gebruiker hoeft echter geen volledige toegang te hebben tot de tabel Inkoopregel om de codeunit uit te voeren. Als de gebruiker indirecte machtiging heeft voor de tabel Verkoopregel, kan de codeunit Verkoop-boeken worden uitgevoerd. Wanneer een gebruiker een indirecte machtiging heeft, kan die gebruiker enkel de tabel Inkoopregel wijzigen door de codeunit Verkoop-boeken of een ander object uit te voeren dat machtiging heeft om de tabel Inkoopregel te wijzigen. De gebruiker kan alleen de tabel Inkoopregel wijzigen vanuit de ondersteunde toepassingsgebieden. De gebruiker kan de functie niet per ongeluk of opzettelijk op andere manieren uitvoeren.

## <a name="to-create-or-modify-permission-sets-by-recording-your-actions"></a>Machtigingensets maken of bewerken door uw acties op te nemen
1.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Machtigingensets** in en kies vervolgens de gerelateerde koppeling.
2.  U kunt ook op de pagina **Gebruikers** de actie **Machtigingensets** kiezen.
3.  Kies op de pagina **Machtigingensets** de actie **Nieuw**.
4.  Vul op een nieuwe regel de velden indien nodig in.
5.  Kies de actie **Machtigingen**.
6.  Kies op de pagina **Machtigingen** de actie **Machtigingen registreren** en kies de actie **Starten**.

    Hierdoor wordt een opnameproces wordt gestart dat al uw acties in de gebruikersinterface vastlegt.
7.  Ga naar de verschillende pagina's en activiteiten in [!INCLUDE[d365fin](includes/d365fin_md.md)] waartoe u gebruikers met deze machtigingenset toegang wilt verlenen. U moet de taken uitvoeren waarvoor u machtigingen wilt opnemen.
8.  Om de opname te stoppen, gaat u terug naar de pagina **Machtigingen** en kiest u de actie **Stoppen**.
9.  Kies de knop **Ja** om de opgenomen toegangsrechten aan de nieuwe machtigingenset toe te voegen.
10. Geef voor elk object in de opgenomen lijst aan of gebruikers records mogen invoegen, wijzigen of verwijderen in de opgenomen tabellen.

> [!NOTE]  
> Wanneer u een machtiging bewerkt en daarmee de gerelateerde machtigingenset, worden de wijzigingen ook toegepast op andere gebruikers aan wie de machtigingenset is toegewezen.

## <a name="to-assign-permission-sets-to-users-or-user-groups"></a>Machtigingensets toewijzen aan gebruikers of gebruikersgroepen
U kunt machtigingen op twee manieren aan gebruikers toewijzen:
- Machtigingensets definiëren op de gebruikerskaart van een gebruiker.
- Schakel op de pagina **Machtigingenset per gebruiker** het selectievakje voor een gebruiker in een kolom in en voor een gerelateerde machtigingenset in een rij in.
    Met deze methode kunt u ook machtigingensets aan gebruikersgroepen toewijzen.

### <a name="to-assign-a-permission-set-on-a-user-card"></a>Een machtigingenset op een gebruikerskaart toewijzen
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikers** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de gebruiker waaraan u machtigingen wilt toewijzen.
Alle machtigingensets die al zijn toegewezen aan de gebruiker worden weergegeven in het feitenblok **Machtigingensets**.
3. Kies de actie **Bewerken** om de pagina **Gebruikerskaart** te openen.
4. Vul op het sneltabblad **Gebruikersmachtigingensets** waar nodig de velden in op een nieuwe regel. Zie voor meer informatie het gedeelte "Een machtigingset maken of bewerken".

### <a name="to-assign-a-permission-set-on-the-permission-set-by-user-page"></a>Een machtigingenset op de pagina **Machtigingenset per gebruiker** toewijzen  
In de volgende procedure wordt uitgelegd hoe u machtigingensets aan een gebruiker toewijst op de pagina **Machtigingenset per gebruiker**. De stappen zijn vergelijkbaar op de pagina **Machtigingenset per gebruikersgroep**.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikers** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer op de pagina **Gebruikers** de betreffende gebruiker en kies de actie **Machtigingenset per gebruiker**.
3. Selecteer op de pagina **Machtigingenset per gebruiker** het selectievakje **[gebruikersnaam]** op een regel voor de betreffende machtigingenset om de set aan de gebruiker toe te wijzen.
4. Selecteer het selectievakje **Alle gebruikers** om de machtigingenset aan alle gebruikers toe te wijzen.

## <a name="to-get-an-overview-of-a-users-permissions"></a>Een overzicht krijgen van de machtigingen van een gebruiker
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Gebruikers** in en kies vervolgens de gerelateerde koppeling.
2. Open de kaart van de betreffende gebruiker.
3. Kies de actie **Effectieve machtigingen**.

    Het deel **Machtigingen** bevat alle databaseobjecten waartoe de gebruiker toegang heeft. U kunt dit gedeelte niet bewerken.

    Het deel **Op machtigingenset-id** bevat de toegewezen machtigingensets waarmee de machtigingen aan de gebruiker worden verleend, de bron en het type van de machtigingenset en de mate waarin de verschillende toegangstypen toegestaan zijn.

    Voor elke rij die u selecteert in de sectie **Machtigingen**, bevat de sectie **Op machtigingenset-id** de machtigingenset of -sets waarmee de machtiging wordt verleend. In dit gedeelte kunt u de waarde wijzigen in elk van de vijf toegangstypevelden, **Lezen**, **Invoegen**, **Wijzigen**, **Verwijderen** en **Uitvoeren**.   

    > [!NOTE]  
    > U kunt alleen machtigingensets van het soort **Door gebruiker gedefinieerd** bewerken.<br /><br />
    > Bronrechtrijen zijn afkomstig uit het abonnementsplan. De machtigingswaarden van het recht hebben voorrang op waarden in andere machtigingensets als deze een hogere volgorde hebben. Een waarde in een niet-recht machtigingenset met een hogere volgorde dan de gerelateerde waarde in het recht worden geplaatst tussen haakjes om aan te geven dat het niet effectief is omdat het wordt overschreven door het recht. Zie voor een uitleg van volgorde het gedeelte "Machtigingen maken of bewerken".  

4. Als u een machtigingenset wilt bewerken, kiest u in het gedeelte **Op machtigingenset-id**, op de regel voor een relevante machtigingenset van het soort **Door gebruiker gedefinieerd**, een van de vijf toegangstypevelden en selecteert u een andere waarde.

5. Als u afzonderlijke toegangsrechten binnen de machtigingenset wilt bewerken, kiest u de waarde in het veld **Machtigingenset** om de pagina **Machtigingen** te openen. Volg de stappen die worden beschreven bij "Machtigingen maken of bewerken".  

> [!NOTE]  
> Wanneer u een machtiging bewerkt, worden de wijzigingen ook toegepast op andere gebruikers aan wie de machtigingenset is toegewezen.

## <a name="see-also"></a>Zie ook
[Gebruikers, profielen en rolcentra](admin-users-profiles-roles.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)  
[Beheer](admin-setup-and-administration.md)  
[Gebruikers aan Office 365 toevoegen voor bedrijven](https://aka.ms/CreateOffice365Users)  
[Microsoft Dynamics 365 Business Central Licentiehandleiding](https://aka.ms/BusinessCentralLicensing)

