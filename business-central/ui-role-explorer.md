---
title: Pagina's en rapporten per rol verkennen en navigeren
description: U kunt een overzicht krijgen van alle zakelijke functies die beschikbaar zijn voor uw rol en voor andere rollen met de Rolverkenner.
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'role explorer, find features, navigate'
ms.search.form: 'RoleExplorer, 9020, 9022, 9027, 9024'
ms.date: 08/01/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# <a name="finding-pages-and-reports-with-the-role-explorer"></a>Pagina's en rapporten zoeken met de Rolverkenner

U kunt een overzicht krijgen van alle zakelijke functies die beschikbaar zijn voor uw rol en voor andere rollen als u nog een stap verder gaat. In dit artikel wordt dit functieoverzicht de *Rolverkenner* genoemd.

Elk element in de rolverkenner is een actie waarmee een pagina of rapport wordt geopend. Dienovereenkomstig kunt u de rolverkenner ook gebruiken als middel om te navigeren in [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="open-the-role-explorer"></a>De rollenverkenner openen

U kunt de rolverkenner openen vanuit het rolcentrum en alle lijstpagina's en vanuit het venster **Vertel me**.

- Kies in uw rolcentrum of op een lijstpagina de ![Menuknop.](media/ui_menu_button.png "Menu-knop") knop rechts van de navigatiebalk of selecteer <kbd>Shift</kbd>+<kbd>F12</kbd>.
- Kies in het venster **Vertel me** de actie **Verkennen** onderaan.

Wanneer u het rolcentrum voor het eerst opent, toont het koppelingen naar de meeste functies die beschikbaar zijn voor uw rol.

## <a name="open-the-role-explorer-filtered-to-show-reports"></a>Open de gefilterde rolverkenner om rapporten weer te geven

U kunt de rolverkenner openen in een gefilterde weergave waarin rapporten worden getoond vanuit het rolcentrum en alle lijstpagina's en vanuit het venster **Vertel me**:

- Kies in uw rolcentrum of op een lijstpagina de koppeling **Alle rapporten** rechts van de navigatiebalk.
- Kies in het venster **Vertel me** de actie **Rapporten verkennen** onderaan.

## <a name="navigate-features"></a>Door functies navigeren

De acties waarmee pagina's of rapporten worden geopend, zijn georganiseerd onder knooppunten die zijn genoemd naar de functies of toepassingsgebieden. U kunt elk knooppunt afzonderlijk of alle knooppunten tegelijk samenvouwen/uitvouwen.

- Kies een afzonderlijk knooppunt om het uit of samen te vouwen. Dit is van toepassing op knooppunten op het hoogste niveau en subknooppunten.
- Als u alle knooppunten op het hoogste niveau op de pagina wilt uitvouwen/samenvouwen, maar de subknooppunten wilt laten zoals ze zijn, kiest u **...** bovenaan en kiest u vervolgens **Uitbreiden** of **Samenvouwen**.
- Als u alle knooppunten op het hoogste niveau en alle subknooppunten eronder wilt uitvouwen/samenvouwen, kiest u **...** bovenaan en kiest u vervolgens **Uitbreiden** of **Samenvouwen**.

## <a name="search-for-features"></a>Zoeken naar functies

Om snel functies te vinden selecteert u **Zoeken** en voer vervolgens een woord of woordgroep in voor de functie die u zoekt. Het rolcentrum zal alle overeenkomende tekst markeren. Als een functie in een samengevouwen knooppunt is verborgen, wordt het samengevouwen knooppunt gemarkeerd met een punt. 

## <a name="explore-other-roles"></a>Andere rollen ontdekken

Als u andere rollen dan die van uzelf wilt verkennen, selecteert u **Meer rollen verkennen**. Het rolcentrum geeft elke rol weer onder een eigen kop, met links naar de bijbehorende functies. U kunt functies vindenen ernaartoe gaan, net zoals u doet bij het verkennen van uw rol.

> [!NOTE]
> U hebt alleen toegang tot rollen die zijn ingesteld om te worden weergegeven in de rolverkenner. Als een rol niet beschikbaar is, is deze er waarschijnlijk niet voor ingesteld. Zie [Profielen beheren](admin-users-profiles-roles.md) voor meer informatie. 

Wanneer u andere rollen verkent, kunt u de verkenning ook verfijnen door de acties **Rapport en analyse** en **Beheer** boven aan het rolcentrum te gebruiken.

- **Rapport en analyse** toont alleen die functies die zijn gecategoriseerd als rapporten en analysefuncties.
- **Beheer** toont alleen die functies die zijn gecategoriseerd als beheerfuncties.

> [!TIP]
> Voor ontwikkelaars: u categoriseert pagina's en rapporten door de [Eigenschap UsageCategory](/dynamics365/business-central/dev-itpro/developer/properties/devenv-usagecategory-property) in de AL-code van het object in te stellen.
<!--
 
## <a name="role-explorer-actions"></a>Role explorer actions

There a several actions along the top of the role explorer to help you locate features of your role and other roles.

|Action|Description|
|------|------|
|**All**|Shows all features that are related to the role.|
|**Find**|Lets you enter a word or phrase to quickly locate feature names that match.|
|**Explore more roles**|All business features that are available for all roles including your own. When exploring all roles, the other actions work the same way, except for all roles shown. **NOTE:** You can only access roles that are set up to show in role explorer. For more information, see [Manage Profiles](admin-users-profiles-roles.md).  |
|**Report & Analysis**|This action Shows only those features that are categorized as reports and analysis features.|
|**Administration**|Shows only those features that are categorized as administration features.|



<!--
Choose the **Find** action at the top of the role explorer to quickly locate feature names that contain a certain term.

Choose the **Explore more roles** action at the top of the role explorer to get an overview of all business features that are available for all roles including your own.

> [!NOTE]
> Only Role Center actions for profiles where the **Show in Role Explorer** check box is selected will appear on the extended version of the role explorer (shown with the **Explore more roles** action). For more information, see [Manage Profiles](admin-users-profiles-roles.md).
-->

## <a name="expand-and-collapse-nodes-on-the-role-explorer"></a>Knooppunten in de rolverkenner uitvouwen en samenvouwen

De acties waarmee pagina's worden geopend, zijn georganiseerd onder knooppunten die zijn genoemd naar de functies of toepassingsgebieden. Elk knooppunt kan afzonderlijk worden samengevouwen of uitgebreid en u kunt alle knooppunten samenvouwen/uitvouwen.

- Kies een knooppunt om een knooppunt uit of samen te vouwen. Dit is van toepassing op knooppunten op het hoogste niveau en subknooppunten.
- Als u alle knooppunten op het hoogste niveau op de pagina wilt uitvouwen/samenvouwen, kiest u de actie **Uitbreiden** of **Samenvouwen** in de rechterbovenhoek.
- Voer een van de volgende stappen uit om alle knooppunten op het hoogste niveau en alle onderliggende knooppunten uit te vouwen/samen te vouwen:
  - Selecteer de toetsen <kbd>Ctrl</kbd>+<kbd>Shift</kbd> terwijl u de actie **Uitvouwen** of **Samenvouwen** kiest in de rechterbovenhoek.
  - Kies **...** in de rechterbovenhoek en kies vervolgens de actie **Alles uitvouwen** of **Alles samenvouwen**.

## <a name="see-also"></a>Zie ook

[Pagina's en informatie zoeken met Vertel me](ui-search.md)  
[Profielen beheren](admin-users-profiles-roles.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
