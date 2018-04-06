---
title: Personalisatie beheren als beheerder in Financials | Microsoft Docs
description: Meer informatie over hoe u de gebruikersinterface kunt aanpassen aan uw manier van werken.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customize, personalize, personalization, hide columns, remove fields, move fields
ms.date: 07/26/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: d6ab880e7fbce361863140e634ea065a31e3aa70
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="managing-personalization-as-an-administrator"></a>Personalisaties beheren als beheerder
<!--NAV in the Web client-->
Gebruikers kunnen hun werkruimte aan hun eigen voorkeuren aanpassen. Als beheerder kunt u personalisaties bewaken en beheren door voor gebruikers de mogelijkheid uit te schakelen om pagina´s te personaliseren, en door alle personalisaties die door gebruikers zijn gemaakt, te wissen.

## <a name="disable-personalization-for-a-profile"></a>Personalisatie uitschakelen voor een profiel
U kunt voorkomen dat alle gebruikers die tot een bepaald profiel behoren, in staat zijn hun pagina's te personaliseren.
1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Profielen** in en klik vervolgens op de gerelateerde koppeling.
2.  Selecteer in de lijst het profiel dat u wilt wijzigen.
3. Selecteer het selectievakje **Personalisering deactiveren** en kies vervolgens de knop **OK**.

## <a name="clear-user-personalizations"></a>Gebruikerspersonalisaties wissen

Door paginapersonalisaties te wissen wordt de pagina teruggezet naar de oorspronkelijke layout die deze had voordat de personalisatie werd doorgevoerd. Er zijn twee manieren om de personalisaties te wissen die door gebruikers aan pagina's zijn aangebracht: met de pagina **Pers. gebruikersinstellingen verwijderen** en met de pagina **Gebruikerspersonalisatiekaart**.

### <a name="clear-user-personalizations-by-using-the-delete-user-personalization-page"></a>Personalisaties wissen met de pagina Pers. gebruikersinstellingen verwijderen.

Met de pagina **Pers. gebruikersinstellingen verwijderen** kunt u personalisaties voor elke gebruiker afzonderlijk per pagina wissen.

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Pers. gebruikersinstellingen verwijderen** in en klik vervolgens op de gerelateerde koppeling.

    De pagina bevat alle pagina's die zijn gepersonaliseerd en gebruiker waartoe ze behoren.

    >[!NOTE]
    > Een vinkje in de kolommen **Oude persoonlijke instellingen** geeft aan dat de personalisatie is uitgevoerd in een oudere versie van [!INCLUDE[d365fin](includes/d365fin_md.md)], die anders met personalisatie omging dan nu het geval is. Gebruikers die proberen deze pagina's te personaliseren zijn hiertoe niet in staat, tenzij ze ervoor kiezen de pagina te ontgrendelen. Zie voor meer informatie [Waarom is een pagina vergrendeld voor personaliseren?](ui-personalization-locked.md).

2. Selecteer het gegeven dat u wilt verwijderen en kies de actie **Verwijderen**.

    De gebruiker ziet de wijzigingen de volgende keer dat hij of zij zich aanmeldt.

### <a name="clear-user-personalizations-by-using-the-user-personalization-card-page"></a>Personalisaties wissen met de pagina Gebruikerspersonalisatiekaart.

Met de pagina **Gebruikerspersonalisatiekaart** kunt u de personalisaties op alle pagina´s voor een bepaalde gebruiker wissen. Hiervoor hebt u schrijfmachtiging nodig voor tabel 2000000072 **Profiel**.

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Gebruikerspersonalisatie** in en klik vervolgens op de gerelateerde koppeling.

    De pagina **Gebruikerspersonalisatie** bevat alle gebruikers waarvoor mogelijk gepersonaliseerde pagina's voorkomen. Als u een gebruikers-ID niet kunt vinden in de lijst, bestaan er geen gepersonaliseerde pagina´s voor.

2. Selecteer de gebruiker in de lijst en kies vervolgens de actie **Bewerken**.

3.  Op het tabblad **Acties** kiest **Aangepaste pagina's wissen**.

    De gebruiker ziet de wijzigingen de volgende keer dat hij of zij zich aanmeldt.

## <a name="see-also"></a>Zie ook
[Het personaliseren van uw werkruimte](ui-personalization-user.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Basisinstellingen wijzigen](ui-change-basic-settings.md)  
[Uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-ervaring aanpassen](ui-experiences.md)  

