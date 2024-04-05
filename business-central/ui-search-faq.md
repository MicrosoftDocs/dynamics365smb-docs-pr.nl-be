---
title: Veelgestelde vragen over Vertel me
description: Dit artikel bevat antwoorden op vragen die onze partners en klanten vaak hebben over de functie Vertel me.
author: brentholtorf
ms.topic: conceptual
ms.service: dynamics-365-business-central
ms.search.keywords: 'find, search, Tell Me'
ms.search.form: TellMe
ms.date: 09/21/2023
ms.author: bholtorf
ms.reviewer: bholtorf
ms.custom: bap-template
---
# Veelgestelde vragen over Vertel me

Dit artikel beantwoordt vragen die onze geavanceerde gebruikers vaak stellen over de functie Vertel me wat u wilt doen.

## Zijn alle acties vanaf mijn huidige pagina detecteerbaar in Vertel me?

Nee. Acties in gedeelten, zoals het gedeelte Verkoopregels of feitenblokken, worden niet weergegeven in Vertel me.

## Kan ik naar een specifieke record zoeken?

Ja. Als u bijvoorbeeld snel een verkooporder wilt vinden, voert u de identificatie ervan in en kiest u vervolgens de actie **Zoeken in bedrijfsgegevens**. Als u alleen de naam van de klant weet, voert u die in. Vertel me rangschikt de resultaten op type, zodat u de order kunt vinden onder de categorie Verkooporders.

## Worden de resultaten in Vertel me gefilterd door machtigingen?

Als de gebruiker geen AccessByPermissions heeft, worden acties niet weergegeven. Pagina's en rapporten worden echter in de resultaten weergegeven, maar vereisen dat de gebruiker de machtiging heeft om er toegang toe te krijgen. Er wordt een bericht weergegeven als de gebruiker geen machtiging heeft om het object weer te geven.

## Geeft Vertel me ook inhoud weer uit mijn aanpassingen of geïnstalleerde extensies?

Acties, pagina's en rapporten die afkomstig zijn uit extensies worden opgepikt door Vertel me, maar aangepaste Help-documentatie niet. Voor technische informatie over hoe u aangepaste pagina's en rapporten detecteerbaar maakt, raadpleegt u [Pagina's en rapporten toevoegen aan zoekacties](/dynamics365/business-central/dev-itpro/developer/devenv-al-menusuite-functionality)

## Wat maakt dit anders dan de eerdere paginazoekfunctie?

De paginazoekfunctie is tot Vertel me geëvolueerd om u te helpen sneller te werken. De paginazoekfunctie kon u alleen helpen navigeren naar pagina's of rapporten. Op technisch niveau is Vertel me niet meer gebaseerd op het oude MenuSuite-concept.

## Ik gebruik on-premises [!INCLUDE[prod_short](includes/prod_short.md)]. Omvat dat Vertel me?

U kunt Vertel me gebruiken in de on-premises webclient om acties, pagina's en rapporten, maar geen apps en consultingservices te vinden in AppSource.

## Is Vertel me beschikbaar voor alle formulierfactoren?

Ja. Het werd geïntroduceerd op telefoons en tablets in Business Central 2023 releasewave 2, maar moet worden ingeschakeld in [Functiebeheer](/dynamics365/business-central/dev-itpro/administration/feature-management) met de schakelaar **Functie: Pagina's en gegevens zoeken in de mobiele app**. 

<!-- removed in v20 because of Help pane
### Are the documentation results available in any language?
The help articles display in the language you have specified in **My Settings**, if help is available in that language.
-->

## Geeft Vertel me hulp bij het gebruik van pagina's, rapporten en andere dingen?

Nee, maar u kunt deze informatie gemakkelijk verkrijgen via het Help-venster. Selecteer gewoon de actie **Zoeken in Help** op de pagina **Vertel me wat u wilt doen** of selecteer <kbd>Ctrl</kbd>+<kbd>F1</kbd> op uw toetsenbord. Ga voor meer informatie over het Help-venster naar [Help-venster](product-help-and-support.md#help-pane).

### Waarom zie ik geen bladwijzerpictogram voor mijn zoekresultaten?

Het bladwijzerpictogram wordt niet weergegeven in het venster Vertel me wanneer personalisatie is uitgeschakeld voor een gebruikersrol.

## Zie ook  

[Lijstweergaven opslaan en personaliseren](ui-views.md)  
[Pagina's en informatie zoeken met Vertel me](ui-search.md)  
[Pagina's zoeken met de Rolverkenner](ui-role-explorer.md)  
[Een bladwijzer van een pagina of rapport maken in uw rolcentrum](ui-bookmarks.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]