---
title: Gebruikers en rollen beheren | Microsoft Docs
description: Leren hoe u gebruikers en rolcentra beheert in Business Central.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.search.keywords: profiles, users
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 00a07acfb455b9b1ddf714f7ca7e49a56a8aebbc
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2304272"
---
# <a name="manage-profiles"></a>Profielen beheren
Alle gebruikers van [!INCLUDE[d365fin](includes/d365fin_md.md)] krijgen een profiel toegewezen dat een afspiegeling is van hun zakelijke rol, de afdeling waarin ze werken of een andere categorisatie. Met profielen kunnen beheerders centraal definiëren en beheren wat verschillende gebruikerstypen in de gebruikersinterface kunnen zien en doen, zodat zij hun zakelijke taken efficiënt kunnen uitvoeren.

> [!NOTE]
> Het typische zakelijke gebruik van een profiel is een rol. Een profiel wordt daarom genoemd *Profiel (rol)* in de gebruikersinterface.

Als beheerder maakt en beheert u profielen op de pagina **Profielen (rollen)**. Elk profiel heeft een kaart waarop u verschillende instellingen voor de gerelateerde rol beheert, zoals de rolnaam, de gebruikersinstellingen en welk rolcentrum het profiel gebruikt. Zie voor meer informatie over gebruikersinstellingen en rolcentra [Basisinstellingen wijzigen](ui-change-basic-settings.md).

Voordat u gebruikersprofielen kunt beheren, moeten de gebruikers worden gemaakt en toegevoegd via het Office 365 Beheercentrum. Vervolgens kunt u machtigingen toewijzen aan elke gebruiker of gebruikersgroep om te definiëren welke functies ze mogen bekijken en/of bewerken. Zie [Gebruikers en machtigingen beheren](ui-how-users-permissions.md) voor meer informatie.

## <a name="page-customization"></a>Pagina-aanpassing
U kunt paginalay-outs voor een profiel aanpassen, zodat alle gebruikers aan wie het profiel is toegewezen de aangepaste pagina's kunnen zien. Als beheerder kunt u pagina's aanpassen met dezelfde functionaliteit die gebruikers gebruiken wanneer ze personaliseren. Zie voor meer informatie [Pagina's aanpassen voor profielen](ui-personalization-manage.md).

## <a name="to-create-a-profile"></a>Een profiel maken
Als u geen bestaand profiel kunt kopiëren, kunt u handmatig een nieuw profiel maken.

> [!NOTE]
> Alle profielen kunnen worden gekopieerd, maar de aanpassingen van de profielenpagina kunnen alleen worden gekopieerd als ze door de gebruiker zijn gemaakt.

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Profielen (rollen)** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies op de pagina **Profielen (rollen)** de actie **Nieuw**.  
3. Vul de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-copy-a-profile"></a>Een profiel kopiëren
Om tijd te besparen kunt u een nieuw profiel maken door een bestaand profiel te kopiëren. Kopieer er een met vergelijkbare instellingen als die u wilt maken.

1. Op de pagina **Profielen (rollen)** selecteert u de naam van het profiel dat u wilt kopiëren en kiest u vervolgens de actie **Profiel kopiëren**.
2. Vul de velden **Profiel-id** en **Weergavenaam** in en kies vervolgens de knop **OK**.
3. Open op de pagina **Profielen (rollen)** de nieuw gemaakte profielkaart en bewerk vervolgens andere velden indien nodig.

## <a name="to-edit-a-profile"></a>Een profiel bewerken
U kunt een profiel bewerken door de velden te wijzigen op de pagina **Profiel (rol)**.

> [!NOTE]
> U kunt een profiel niet bewerken wanneer aan het profiel toegewezen gebruikers zijn aangemeld.

## <a name="to-assign-a-profile-to-a-user"></a>Een profiel aan een gebruiker toewijzen
Gebruikers kunnen zichzelf een rol toewijzen (die een profiel vertegenwoordigt) door het veld **Rol** te kiezen op de pagina **Mijn instellingen**. Als beheerder kunt u hetzelfde doen via de pagina **Profielen (rollen)**.

1. Selecteer op de pagina **Profielen (rollen)** het profiel dat u wilt toewijzen en kies vervolgens de actie **Overzicht persoonlijke gebruikersinstellingen**.
2. Selecteer op de pagina **Persoonlijke gebruikersinstellingen** de gebruiker aan wie u het profiel wilt toewijzen en kies vervolgens de actie **Bewerken**.
3. Selecteer in het veld **Profiel-id** het relevante profiel.

> [!NOTE]
> Als u een ander profiel aan een gebruiker toewijst, blijven eventuele aanpassingen die door de gebruiker met het vorige profiel zijn aangebracht, behouden.

## <a name="to-define-user-settings-for-a-profile"></a>Gebruikersinstellingen voor een profiel definiëren
Op de pagina **Mijn instellingen** kunnen gebruikers basisgedrag van hun account definiëren, zoals het rolcentrum, de taal en welke meldingen ze ontvangen. Zie voor meer informatie [Basisinstellingen wijzigen](ui-change-basic-settings.md).

Als beheerder kunt u deze instelling voor een profiel definiëren en daarmee de instellingen toepassen op alle gebruikers van de gerelateerde rol.

1. Kies het ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Profielen (rollen)** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de regel voor het profiel waarvoor u de gebruikersinstellingen wilt wijzigen, kies de actie **Navigeren** en kies vervolgens de actie **Persoonlijke gebruikersinstellingen**.
3. Open op de pagina **Persoonlijke gebruikersinstellingen** de kaart voor de gebruiker van wie u de instellingen wilt wijzigen.
4. Bewerk indien nodig op de pagina **Gebruikerspersonalisatiekaart** de velden.

## <a name="to-activate-a-profile"></a>Een profiel activeren
Wanneer een profiel wordt gemaakt, kunt u verschillende selectievakjes selecteren die bepalen of, waar en hoe het profiel en de bijbehorende informatie beschikbaar worden gesteld aan gebruikers.

1. Schakel op de pagina **Profiel (rol)** de volgende selectievakjes in:
    - **Ingeschakeld** om aan te geven of de gerelateerde rol zichtbaar is op de pagina **Beschikbare rollen** voor gebruikers om uit te kiezen.  
    - **Als standaardprofiel gebruiken** om het profiel op te geven dat van toepassing is op gebruikers aan wie geen specifieke rol is toegewezen.
    - **Personalisatie uitschakelen** om aan te geven of gebruikers van de gerelateerde rol hun werkruimte kunnen personaliseren.
    - **Weergeven in Rolverkenner** om aan te geven of menu-items voor zakelijke functies in het profiel worden weergegeven in het functieoverzicht. Zie voor meer informatie [Pagina's zoeken vanuit een functieoverzicht](ui-role-explorer.md).

    ## <a name="to-export-user-created-profiles"></a>Door de gebruiker gemaakte profielen exporteren
    U kunt profielen exporteren die door u of door gebruikers zijn gewijzigd, zoals aangegeven door **(Door gebruiker gemaakt)** in het veld **Bron**. Het profiel wordt geëxporteerd naar een zipbestand met .al-bestanden die opnieuw kunnen worden gebruikt om extensies te ontwikkelen. Zie voor meer informatie [De client gebruiken om profielen en pagina-aanpassingen te maken](/dynamics365/business-central/dev-itpro/developer/devenv-design-profiles-using-client).

    * Kies op de pagina **Profielen (rollen)** de actie **Door gebruiker gemaakte profielen exporteren**.

    Een zipbestand met de .al-bestanden voor profielen die nieuw zijn toegevoegd of gewijzigd, wordt geëxporteerd.

## <a name="to-delete-a-profile"></a>Een profiel verwijderen
U kunt een profiel verwijderen door de actie **Verwijderen** te kiezen op de pagina **Profielen (rollen)**. De volgende beperkingen zijn echter van toepassing:

- U kunt geen profielen verwijderen die afkomstig zijn van extensies. De extensie moet eerst worden verwijderd.
- Het profiel moet uitgeschakeld zijn. Dit zorgt er ook voor dat er geen gebruikers aan wie het profiel is toegewezen, zijn aangemeld wanneer u verwijdert.
- U kunt slechts één profiel tegelijk verwijderen.  

## <a name="to-delete-all-personalizations-made-by-a-user"></a>Alle aanpassingen verwijderen die door een gebruiker zijn aangebracht.
U kunt alle wijzigingen verwijderen die een gebruiker heeft aangebracht in pagina's die deel uitmaken van hun werkruimte. Dit kan bijvoorbeeld handig zijn als een werknemer van rol is veranderd en de personalisaties niet langer nodig heeft. Als u de personalisaties van gebruikers verwijdert, wordt de paginalay-out teruggezet naar wat wordt gedefinieerd door het profiel.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Persoonlijke gebruikersinstellingen** in en kies vervolgens de gerelateerde koppeling.

    De pagina **Persoonlijke gebruikersinstellingen** bevat alle gebruikers die persoonlijke instellingen hebben aangebracht.

2. Open de kaart voor een gebruiker wiens personalisaties u wilt verwijderen.
3. Kies op de pagina **Gebruikerspersonalisatiekaart** de actie **Aangepaste pagina's wissen** en accepteer het bericht dat verschijnt.

De gebruiker ziet de wijzigingen de volgende keer dat hij of zij zich aanmeldt.

U kunt ook alle pagina-aanpassingen voor een profiel verwijderen. Zie voor meer informatie [Alle aanpassingen voor een profiel verwijderen](ui-personalization-manage.md#to-delete-all-customizations-for-a-profile).

## <a name="to-delete-personalizations-for-specific-pages"></a>Personalisaties voor specifieke pagina's verwijderen
U kunt personalisaties verwijderen die een of meer gebruikers hebben aangebracht op specifieke pagina's waaruit hun werkruimte bestaat. Dit kan bijvoorbeeld handig zijn als een gewijzigd bedrijfsproces betekent dat een personalisatie niet langer door gebruikers mag worden gebruikt. Als u de personalisaties van gebruikers verwijdert, wordt de paginalay-out teruggezet naar wat wordt gedefinieerd door het profiel.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Persoonlijke gebruikersinstellingen van pagina** in en kies vervolgens de gerelateerde koppeling.

    De pagina **Persoonlijke gebruikersinstellingen van pagina** bevat alle pagina's die zijn gepersonaliseerd en de gebruiker waartoe ze behoren.

    > [!Note]
    > Een vinkje in het veld **Oude persoonlijke instellingen** geeft aan dat de personalisatie is uitgevoerd in een oudere versie van [!INCLUDE[d365fin](includes/d365fin_md.md)], die anders met personalisatie omging dan nu het geval is. Gebruikers die proberen deze pagina's te personaliseren zijn hiertoe niet in staat, tenzij ze ervoor kiezen de pagina te ontgrendelen. Zie voor meer informatie [Waarom is een pagina vergrendeld voor personaliseren?](ui-personalization-locked.md).

2. Selecteer de regel voor de paginapersonalisatie die u wilt verwijderen en kies de actie **Verwijderen**.

De gebruiker ziet de wijzigingen de volgende keer dat hij of zij zich aanmeldt.    

U kunt ook afzonderlijke pagina-aanpassingen voor een profiel verwijderen. Zie voor meer informatie [Aanpassingen voor specifieke pagina's voor een profiel verwijderen](ui-personalization-manage.md#to-delete-customization-for-specific-pages-for-a-profile).

## <a name="see-also"></a>Zie ook  
[Gebruikers en machtigingen beheren](ui-how-users-permissions.md)  
[Pagina's aanpassen voor profielen](ui-personalization-manage.md)  
[Uw werkruimte personaliseren](ui-personalization-user.md)  
