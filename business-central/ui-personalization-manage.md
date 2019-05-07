---
title: Personalisatie beheren als beheerder in Business Central | Microsoft Docs
description: Meer informatie over hoe u de gebruikersinterface kunt aanpassen aan uw manier van werken.
services: project-madeira
documentationcenter: ''
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 04/01/2019
ms.author: jswymer
ms.openlocfilehash: 37cdf2d7dcc46b1286cbb7a5ad620547e364309e
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "910874"
---
# <a name="managing-personalization-as-an-administrator"></a>Personalisaties beheren als beheerder

 Gebruikers kunnen hun werkruimte aan hun eigen voorkeuren aanpassen. Als beheerder bepaalt en beheert u personalisatie door:

-   De personalisatie in of uit te schakelen voor de hele toepassing (alleen on-premises installatie).
-   De personalisatiefunctie in of uit te schakelen voor gebruikers van een specifiek profiel.
-   Paginapersonalisaties te wissen die gebruikers hebben aangebracht.

## <a name="EnablePersonalization"></a>Personalisatie in- of uitschakelen (alleen on-premises)

Standaard is personalisatie niet ingeschakeld in de client. U schakelt personalisatie in of uit door het configuratiebestand te wijzigen (navsettings.json) van het Business Central-webserverexemplaar dat de clients bedient.

1. Als u personalisatie wilt inschakelen, voegt u de volgende regel toe aan het bestand navsettings.json:

    ```
    "PersonalizationEnabled": "true"
    ```

    Als u personalisatie wilt uitschakelen, verwijdert u deze regel of wijzigt u deze in:

    ```
    "PersonalizationEnabled": "false"
    ```

    Voor meer informatie over hoe u het navsettings.json-bestand wijzigt raadpleegt u [Het bestand navsettings.json rechtstreeks wijzigen](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-web-server?branch=master#Settings)

2. De toepassingssymbolen genereren en downloaden.

    Deze stap is optioneel en is niet vereist om personalisatie in te schakelen. Het zorgt echter dat nieuwe pagina's die worden gemaakt door ontwikkelaars, kunnen worden gepersonaliseerd.

    1. Eerst genereert u de symbolen door finsql.exe uit te voeren met de opdracht `generatesymbolreference`. Het finsql.exe-bestand bevindt zich in de installatiemap voor de [!INCLUDE[server](includes/server.md)] Dynamics NAV ontwikkelingsomgeving (CSIDE). Als u de symbolen wilt genereren, opent u een opdrachtprompt, wijzigt u de map waar het bestand is opgeslagen en voert u de volgende opdracht uit:

        ```
        finsql.exe Command=generatesymbolreference, Database="<Database Name>", ServerName=<SQL Server Name\<Server Instance>
        ```
    Voorbeeld:

        ```
        finsql.exe Command=generatesymbolreference, Database="Demo Database BC", ServerName=MySQLServer\BCDEMO
        ```

    Zie voor meer informatie [C/SIDE en AL naast elkaar uitvoeren](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-running-cside-and-al-side-by-side).

    2. Configureer het [!INCLUDE[nav_server_md](includes/nav_server_md.md)]-exemplaar zodat het **toepassingssymboolverwijzingen laadt bij opstarten van de server** (EnableSymbolLoadingAtServerStartup). Zie [Business Central Server configureren](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance#development-settings) voor meer informatie.

## <a name="to-disable-personalization-for-a-profile"></a>Personalisatie uitschakelen voor een profiel

U kunt voorkomen dat alle gebruikers die tot een bepaald profiel behoren, in staat zijn hun pagina's te personaliseren.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Profielen** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer in de lijst het profiel dat u wilt wijzigen.
3. Selecteer het selectievakje **Personalisering deactiveren** en kies vervolgens de knop **OK**.

## <a name="to-clear-user-personalizations"></a>Gebruikerspersonalisaties wissen

Door paginapersonalisaties te wissen wordt de pagina teruggezet naar de oorspronkelijke layout die deze had voordat de personalisatie werd doorgevoerd. Er zijn twee manieren om de personalisaties te wissen die door gebruikers aan pagina's zijn aangebracht: met de pagina **Pers. gebruikersinstellingen verwijderen** en met de pagina **Gebruikerspersonalisatiekaart**.

### <a name="to-clear-user-personalizations-by-using-the-delete-user-personalization-page"></a>Gebruikerspersonalisaties wissen met de pagina Pers. gebruikersinstellingen verwijderen.

Met de pagina **Pers. gebruikersinstellingen verwijderen** kunt u personalisaties voor elke gebruiker afzonderlijk per pagina wissen.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Pers. gebruikersinstellingen verwijderen** in en kies vervolgens de gerelateerde koppeling.

    De pagina bevat alle pagina's die zijn gepersonaliseerd en gebruiker waartoe ze behoren.

    >[!NOTE]
    > Een vinkje in de kolommen **Oude persoonlijke instellingen** geeft aan dat de personalisatie is uitgevoerd in een oudere versie van [!INCLUDE[d365fin](includes/d365fin_md.md)], die anders met personalisatie omging dan nu het geval is. Gebruikers die proberen deze pagina's te personaliseren zijn hiertoe niet in staat, tenzij ze ervoor kiezen de pagina te ontgrendelen. Zie voor meer informatie [Waarom is een pagina vergrendeld voor personaliseren?](ui-personalization-locked.md).

2. Selecteer het gegeven dat u wilt verwijderen en kies de actie **Verwijderen**.

    De gebruiker ziet de wijzigingen de volgende keer dat hij of zij zich aanmeldt.

### <a name="to-clear-user-personalizations-by-using-the-user-personalization-card-page"></a>Gebruikerspersonalisaties wissen met de pagina Gebruikerspersonalisatiekaart.

Met de pagina **Gebruikerspersonalisatiekaart** kunt u de personalisaties op alle pagina´s voor een bepaalde gebruiker wissen. Hiervoor hebt u schrijfmachtiging nodig voor tabel 2000000072 **Profiel**.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Pers. gebruikersinstellingen** in en kies vervolgens de gerelateerde koppeling.

    De pagina **Gebruikerspersonalisatie** bevat alle gebruikers waarvoor mogelijk gepersonaliseerde pagina's voorkomen. Als u een gebruikers-ID niet kunt vinden in de lijst, bestaan er geen gepersonaliseerde pagina´s voor.

2. Selecteer de gebruiker in de lijst en kies vervolgens de actie **Bewerken**.

3. Op het tabblad **Acties** kiest **Aangepaste pagina's wissen**.

    De gebruiker ziet de wijzigingen de volgende keer dat hij of zij zich aanmeldt.

## <a name="see-also"></a>Zie ook
[Het personaliseren van uw werkruimte](ui-personalization-user.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Basisinstellingen wijzigen](ui-change-basic-settings.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)  
