---
title: Over zoeken en filteren in Business Central
description: Beantwoordt veelgestelde vragen over zoeken en filteren.
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: article
ms.reviewer: edupont04
ms.search.keywords: keyboarding, productivity, how do i, filter pane
ms.date: 04/05/2019
ms.author: mikebc
ms.openlocfilehash: 0f9f5db0e7031156848a5bd15c711d3108f3490b
ms.sourcegitcommit: addfb47612cc2e4e98dfd7e338b6f41cde405d5c
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/16/2019
ms.locfileid: "969867"
---
# <a name="searching-and-filtering-faq"></a>Veelgestelde vragen over zoeken en filteren
In dit artikel worden veelgestelde vragen beantwoord over zoeken en filteren.

## <a name="is-there-a-difference-between-searching-and-filtering"></a>Is er een verschil tussen zoeken en filteren?
Ja.
- Zoeken is eenvoudig en breed: er worden records gezocht die de zoektekst bevatten in zichtbare velen op de pagina. Er wordt geen onderscheid gemaakt tussen hoofdletters en kleine letters.
- Filteren is zeer flexibel en kan op specifieke velden worden toegepast, inclusief velden die niet zichtbaar zijn op de pagina: er worden records weergegeven met exacte, hoofdlettergevoelige overeenkomsten, maar filtering kan worden aangepast met krachtige zoeksymbolen, tokens en formules. Voor meer informatie over hoe u deze functies gebruikt raadpleegt u [Sorteren, zoeken en filteren in lijsten](ui-enter-criteria-filters.md).

## <a name="is-there-a-keyboard-experience-for-search-and-filter"></a>Is er een toetsenbordervaring voor zoeken en filteren?
Zoeken en filteren zijn zeer geoptimaliseerd voor gebruikers die muisvrije interactie prefereren om efficiënt met hun gegevens te werken. Er zijn allerlei sneltoetsen die na elkaar worden gebruikt om zeer snel te werken. Zie voor meer informatie [Toetsenbordsneltoetsen](keyboard-shortcuts.md#KeyboardFilter).

## <a name="is-the-filter-pane-available-on-all-lists"></a>Is het filterdeelvenster beschikbaar voor alle lijsten?
Het filterdeelvenster is beschikbaar op pagina's waar de lijst de primaire inhoud op de pagina is, zoals werkbladen en lijstpagina's, inclusief lijsten die bereikbaar zijn vanaf de navigatiebalk. Het filterdeelvenster is nog niet beschikbaar voor ingesloten lijsten, zoals verkoopregels op verkooporders, of voor lijsten met dynamische kolommen (vaak matrixpagina's genoemd).

## <a name="how-can-i-save-my-filters"></a>Hoe kan ik mijn filters opslaan?

Uw filters en wijzigingen in vooraf gedefinieerde filters worden de hele sessie onthouden (zolang u aangemeld blijft), zelfs als u van de pagina weg navigeert. Het is momenteel niet mogelijk filters permanent op te slaan. In tegenstelling tot filters wordt zoektekst niet onthouden wanneer u van een pagina weg navigeert.

## <a name="is-this-the-same-as-advanced-filters-and-limit-totals-in-microsoft-dynamics-nav"></a>Is dit hetzelfde als Geavanceerde Filters en Limiettotalen in Microsoft Dynamics NAV?

[!INCLUDE[d365fin](includes/d365fin_md.md)] bouwt voort op deze populaire functies en levert een moderne en zeer praktische ervaring voor het zoeken en analyseren van uw gegevens. Dankzij meer toetsenbordsneltoetsen en de invoering van zoeken overtreft [!INCLUDE[d365fin](includes/d365fin_md.md)] de functionaliteit in Dynamics NAV.  

Zie ook [Is het filterdeelvenster beschikbaar om rapporten te filteren?](#is-the-filter-pane-available-for-filtering-reports)  

## <a name="can-i-search-and-filter-using-the-companion-apps-and-outlook-addin"></a>Kan ik zoeken en filteren met de bijbehorende apps en de Outlook-Invoegtoepassing?
Op verschillende weergavebestemmingen, zoals mobiele apparaten of in Outlook, kunt u zoeken in lijsten, maar kunt u meestal niet filteren op afzonderlijke velden.

## <a name="is-the-filter-pane-available-for-filtering-reports"></a>Is het filterdeelvenster beschikbaar om rapporten te filteren?
Nee. Het rapportfilterdialoogvenster, dat vaak de aanvraagpagina wordt genoemd, gebruikt momenteel een andere ervaring die sommige, maar niet alle van de mogelijkheden van het filterdeelvenster biedt.

## <a name="will-microsoft-extend-the-filter-pane-experience"></a>Zal Microsoft het filterdeelvenster uitbreiden?
Bij Microsoft luisteren we constant naar feedback van onze zeer uiteenlopende gebruikers en handelen we naar de beste suggesties. Als u geïnteresseerd bent in het uitbreiden van het filterdeelvenster naar meer formulierfactoren, meer typen lijsten en rapporten, of een goed idee hebt om het te verbeteren, voegt u een idee of een stem op bestaande ideeën toe aan [aka.ms/BusinessCentralIdeas](https://aka.ms/businesscentralideas)

## <a name="can-i-do-anything-about-the-searching-for-rows-is-taking-too-long-message"></a>Kan ik niets doen aan het bericht "Zoeken naar rijen duurt te lang"?

Er is een tijdslimiet voor hoe lang een zoekbewerking kan duren. Probeer eerst de zoekcriteria te wijzigen en opnieuw te zoeken. Als u [!INCLUDE[prodshort](includes/prodshort.md)] on-premises gebruikt, neemt u contact op met de systeembeheerder, omdat een beheerder de tijdslimiet voor zoekopdrachten kan verlengen.

Als on-premises beheerder verlengt u de tijdslimiet voor zoekopdrachten door de instelling **Time-out voor zoeken** van de [!INCLUDE[prodshort](includes/prodshort.md)]-server te wijzigen. Zie voor meer informatie [Business Central Server configureren](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance?#Database) in de Business Central Developer en IT Pro Help.

## <a name="see-also"></a>Zie ook

[Aan de slag](product-get-started.md)  
[Sorteren, zoeken en filteren in lijsten](ui-enter-criteria-filters.md)  
