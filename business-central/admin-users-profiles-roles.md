---
title: Gebruikers en rollen beheren
description: Leer hoe u gebruikersprofielen en rolcentra beheert in Business Central. Met profielen kunnen beheerders centraal definiëren en beheren wat gebruikers kunnen zien en doen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 01/11/2023
ms.custom: bap-template
ms.search.form: 9171
---
# <a name="manage-user-profiles"></a>Gebruikersprofielen beheren

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Wijs alle gebruikers toe aan profielen die het volgende weerspiegelen:

* Hun zakelijke rol
* De afdeling waar ze werken
* Een ander type categorisatie

Met profielen kunnen beheerders centraal definiëren en beheren waartoe verschillende soorten gebruikers toegang hebben in [!INCLUDE[prod_short](includes/prod_short.md)].

> [!NOTE]
> Het typische zakelijke gebruik van een profiel is een rol. Een profiel wordt daarom genoemd *Profiel (rol)* in de gebruikersinterface.

Als beheerder maakt en beheert u profielen op de pagina **Profielen (rollen)**. Elk profiel heeft een kaart waarop u de instellingen voor de gerelateerde rol beheert. De kaart bevat bijvoorbeeld de volgende informatie:

* Naam van de rol
* Gebruikersconfiguratie
* Het rolcentrum dat door het profiel wordt gebruikt

Zie voor meer informatie over gebruikersinstellingen en rolcentra [Basisinstellingen wijzigen](ui-change-basic-settings.md).

Voordat u gebruikersprofielen kunt beheren, moeten de gebruikers worden gemaakt en toegevoegd via het Microsoft 365-beheercentrum. U kunt vervolgens machtigingen toewijzen aan elke gebruiker of gebruikersgroep. Machtigingen definiëren de functies waartoe gebruikers toegang hebben. Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie.

## <a name="page-customization"></a>Pagina-aanpassing

U kunt paginalay-outs voor een profiel aanpassen, zodat alle gebruikers aan wie het profiel is toegewezen de aangepaste pagina's kunnen zien. Als beheerder kunt u pagina's aanpassen met dezelfde functionaliteit die gebruikers gebruiken wanneer ze personaliseren. Zie voor meer informatie [Pagina's aanpassen voor profielen](ui-personalization-manage.md).

## <a name="to-create-a-profile"></a>Een profiel maken

Als u geen bestaand profiel kunt kopiëren, kunt u handmatig een nieuw profiel maken.

1. Kies het pictogram ![Pagina of rapport zoeken.](media/ui-search/search_small.png "Pictogram Pagina of rapport zoeken"), voer **Profielen (rollen)** in en kies vervolgens de gerelateerde koppeling.  
2. Kies op de pagina **Profielen (rollen)** de actie **Nieuw**.  
3. Vul de vereiste velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]
> Als u wilt dat een bepaald profiel alleen beschikbaar is voor zeer specifieke gebruikers, kunt u het veld **Beschrijving** instellen op `Navigation menu only.`. Op deze manier wordt het profiel uitgesloten van de lijst met beschikbare rollen in **Mijn instellingen**.

## <a name="to-copy-a-profile"></a>Een profiel kopiëren

Om tijd te besparen kunt u een nieuw profiel maken door een bestaand profiel te kopiëren. Kopieer er een met vergelijkbare instellingen als die u wilt maken.

> [!NOTE]
> Wanneer u een profiel kopieert, worden ook alle gerelateerde pagina-aanpassingen gekopieerd, zowel de door de gebruiker gemaakte aanpassingen als de aanpassingen die van uitbreidingen zijn afgeleid.

1. Selecteer op de pagina **Profielen (rollen)** de regel die u voor het profiel wilt kopiëren en kies de actie **Profiel kopiëren**.
2. Vul de velden **Profiel-id** en **Weergavenaam** in en kies vervolgens de knop **OK**.
3. Open op de pagina **Profielen (rollen)** de nieuw gemaakte profielkaart en bewerk vervolgens andere velden indien nodig.

## <a name="to-edit-a-profile"></a>Een profiel bewerken

U kunt een profiel bewerken door de velden te wijzigen op de pagina **Profiel (rol)**. De wijzigingen worden pas zichtbaar voor de gebruiker aan wie het profiel is toegewezen na af- en weer aanmelden.

> [!Caution]
> Wijzig de naam van het profiel niet terwijl er gebruikers aan wie het profiel is toegewezen, aangemeld zijn, omdat het product dan kan vastlopen en opnieuw opgestart moet worden.

## <a name="to-assign-a-profile-to-a-user"></a>Een profiel aan een gebruiker toewijzen

Gebruikers kunnen zichzelf een rol toewijzen (die een profiel vertegenwoordigt) door het veld **Rol** te kiezen op de pagina **Mijn instellingen**. Als beheerder kunt u hetzelfde doen via de pagina **Profielen (rollen)**.

1. Selecteer op de pagina **Profielen (rollen)** het profiel dat u wilt toewijzen en kies vervolgens de actie **Overzicht persoonlijke gebruikersinstellingen**.
2. Selecteer op de pagina **Persoonlijke gebruikersinstellingen** de gebruiker aan wie u het profiel wilt toewijzen en kies vervolgens de actie **Bewerken**.
3. Selecteer in het veld **Profiel-id** het relevante profiel.

> [!NOTE]
> Als u een ander profiel aan een gebruiker toewijst, blijven eventuele aanpassingen die door de gebruiker met het vorige profiel zijn aangebracht, behouden.

## <a name="to-define-user-settings-for-a-profile"></a>Gebruikersinstellingen voor een profiel definiëren

Op de pagina **Mijn instellingen** kunnen gebruikers basisgedrag van hun account definiëren, zoals het rolcentrum, de taal en welke meldingen ze ontvangen. Zie voor meer informatie [Basisinstellingen wijzigen](ui-change-basic-settings.md).

Als beheerder kunt u instellingen voor een profiel definiëren. De instellingen zijn van toepassing op alle gebruikers die aan de rol zijn toegewezen.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Profielen (rollen)** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de regel voor het profiel waarvoor u de gebruikersinstellingen wilt wijzigen, kies de actie Navigeren en kies vervolgens de actie **Lijst persoonlijke gebruikersinstellingen**.
3. Open op de pagina **Persoonlijke gebruikersinstellingen** de kaart voor de gebruiker van wie u de instellingen wilt wijzigen.
4. Bewerk indien nodig op de pagina **Gebruikerspersonalisatiekaart** de velden.

## <a name="to-activate-a-profile"></a>Een profiel activeren

Wanneer u een profiel maakt, kunt u bepalen of, waar en hoe het profiel en de bijbehorende informatie beschikbaar zijn voor gebruikers.

Schakel op de pagina **Profiel (rol)** de volgende selectievakjes in:

* **Ingeschakeld** om aan te geven of de gerelateerde rol zichtbaar is op de pagina **Beschikbare rollen** voor gebruikers om uit te kiezen.  
* **Als standaardprofiel gebruiken** om het profiel op te geven dat van toepassing is op gebruikers aan wie geen specifieke rol is toegewezen.
* **Personalisatie uitschakelen** om aan te geven of gebruikers van de gerelateerde rol hun werkruimte kunnen personaliseren.
* **Weergeven in Rollenverkenner** om op te geven of acties op zakelijke functies in het profiel moeten worden weergegeven in de uitgebreide weergave van de rollenverkenner, een functieoverzicht. Zie voor meer informatie [Pagina's zoeken met de rolverkenner](ui-role-explorer.md).

## <a name="to-export-profiles"></a>Profielen exporteren

U kunt profielen exporteren uit [!INCLUDE[prod_short](includes/prod_short.md)], bijvoorbeeld om ze te hergebruiken in een andere tenant. De profielen worden geëxporteerd naar een zipbestand dat AL-bestanden bevat. U kunt de AL-bestanden opnieuw gebruiken om extensies te ontwikkelen. Zie [De client gebruiken om profielen en pagina-aanpassingen te maken](/dynamics365/business-central/dev-itpro/developer/devenv-design-profiles-using-client) voor meer informatie.

* Kies op de pagina **Profielen (rollen)** de actie **Profielen exporteren**.

    Deze actie exporteert een zipbestand dat AL-bestanden voor alle profielen bevat.

## <a name="to-import-profiles"></a>Profielen importeren

U kunt profielen importeren die zijn geëxporteerd vanuit [!INCLUDE[prod_short](includes/prod_short.md)]. De stappen zijn min of meer het tegenovergestelde van de stappen om profielen te exporteren. Zie [Profielen exporteren](admin-users-profiles-roles.md#to-export-profiles) voor meer informatie.

1. Kies op de pagina **Profielen (rollen)** de actie **Profielen importeren**.
2. Volg de stappen in de wizard **Profielen importeren**.

    Als u alleen geselecteerde profielen wilt importeren, gebruikt u het selectievakje **Geselecteerd** om aan te geven welke u wilt importeren.
3. Kies de knop **Selectie importeren**.

    Deze actie importeert een zipbestand dat AL-bestanden voor de geselecteerde profielen.

## <a name="to-delete-a-profile"></a>Een profiel verwijderen

U kunt een profiel verwijderen door de actie **Verwijderen** te kiezen op de pagina **Profielen (rollen)**. De volgende beperkingen zijn echter van toepassing:

* U kunt een profiel dat aan een gebruiker of een gebruikersgroep is toegewezen, niet verwijderen.
*-* U kunt geen profielen verwijderen die afkomstig zijn van extensies. De extensie moet eerst worden verwijderd.
*-* U kunt slechts één profiel tegelijk verwijderen.

## <a name="to-delete-all-personalizations-made-by-a-user"></a>Alle aanpassingen verwijderen die door een gebruiker zijn aangebracht.

U kunt alle wijzigingen verwijderen die een gebruiker op pagina's heeft aangebracht. Wijzigingen verwijderen kan bijvoorbeeld handig zijn als een werknemer van rol is veranderd en ze niet langer nodig heeft. Door verwijderingen wordt de paginalay-out teruggezet naar wat door het profiel wordt gedefinieerd.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Persoonlijke gebruikersinstellingen** in en kies vervolgens de gerelateerde koppeling.

    De pagina **Persoonlijke gebruikersinstellingen** bevat alle gebruikers die persoonlijke instellingen hebben aangebracht.

2. Open de kaart voor een gebruiker wiens personalisaties u wilt verwijderen.
3. Kies op de pagina **Gebruikerspersonalisatiekaart** de actie **Aangepaste pagina's wissen** en accepteer het bericht dat verschijnt.

De gebruiker ziet de wijzigingen de volgende keer dat hij of zij zich aanmeldt.

U kunt ook alle pagina-aanpassingen voor een profiel verwijderen. Zie voor meer informatie [Alle aanpassingen voor een profiel verwijderen](ui-personalization-manage.md#to-delete-all-customizations-for-a-profile).

## <a name="to-delete-personalizations-for-specific-pages"></a>Personalisaties voor specifieke pagina's verwijderen

U kunt personalisaties verwijderen die een of meer gebruikers hebben aangebracht op specifieke pagina's. Personalisaties verwijderen kan bijvoorbeeld handig zijn als een gewijzigd bedrijfsproces betekent dat een personalisatie niet langer moet worden gebruikt. Door verwijderingen wordt de paginalay-out teruggezet naar wat door het profiel wordt gedefinieerd.

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Persoonlijke gebruikersinstellingen van pagina** in en kies vervolgens de gerelateerde koppeling.

    De pagina **Persoonlijke gebruikersinstellingen van pagina** bevat alle pagina's die zijn gepersonaliseerd en de gebruiker waartoe ze behoren.

    > [!Note]
    > Een vinkje in het veld **Oude persoonlijke instellingen** geeft aan dat de personalisatie is uitgevoerd in een oudere versie van [!INCLUDE[prod_short](includes/prod_short.md)], die anders met personalisatie omging dan nu het geval is. Gebruikers die proberen deze pagina's te personaliseren zijn hiertoe niet in staat, tenzij ze ervoor kiezen de pagina te ontgrendelen. Zie voor meer informatie [Waarom is een pagina vergrendeld voor personaliseren?](ui-personalization-locked.md).

2. Selecteer de regel voor de paginapersonalisatie die u wilt verwijderen en kies de actie **Verwijderen**.

De gebruiker ziet de wijzigingen de volgende keer dat hij of zij zich aanmeldt.  

U kunt ook afzonderlijke pagina-aanpassingen voor een profiel verwijderen. Zie voor meer informatie [Aanpassingen voor specifieke pagina's voor een profiel verwijderen](ui-personalization-manage.md#to-delete-customization-for-specific-pages-for-a-profile).

## <a name="managing-user-sessions"></a>Gebruikerssessies beheren

Als beheerder van [!INCLUDE[prod_short](includes/prod_short.md)] online kunt u gebruikerssessies beheren in het beheercentrum. Zie voor meer informatie [Sessies beheren](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-sessions) in de beheerinhoud.  

Voor [!INCLUDE[prod_short](includes/prod_short.md)] on-premises kunt u sessies beheren met bijvoorbeeld SQL Server Management Studio. Zie voor meer informatie [Technische documentatie over SQL Server](/sql/sql-server).  

## <a name="see-also"></a>Zie ook

[Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md)  
[Pagina's aanpassen voor profielen](ui-personalization-manage.md)  
[Uw werkruimte personaliseren](ui-personalization-user.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
