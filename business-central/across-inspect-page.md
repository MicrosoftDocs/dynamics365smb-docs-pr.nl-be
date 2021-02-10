---
title: Pagina's inspecteren in Business Central
description: Gebruik de pagina-inspectiefunctie om in te zoomen op details over het paginaontwerp en de gegevensbron. Pagina-inspectie is ideaal voor het oplossen van problemen met uw gegevens.
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.service: dynamics365-business-central
author: jswymer
ms.author: jswymer
ms.date: 10/01/2020
ms.openlocfilehash: d80baed51b646b389f9dd86540cc993c212be09b
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4754404"
---
# <a name="inspecting-pages-in-business-central"></a>Pagina's inspecteren in Business Central

Met de pagina-inspectiefunctie kunt u details opvragen over een pagina, wat inzicht biedt in het paginaontwerp, de verschillende onderdelen waaruit de pagina bestaat en de bron achter de gegevens op de pagina. Pagina-inspectie is speciaal ontworpen voor beheerders, geavanceerde gebruikers, ondersteuningsmedewerkers en ontwikkelaars. Het is ideaal voor het leren van het gegevensmodel achter een pagina en voor het oplossen van problemen. Als u bijvoorbeeld een probleem met een pagina hebt, kunt u pagina-inspectie gebruiken om informatie te krijgen die u kunt doorgeven aan uw systeembeheerder of ondersteuningsmedewerkers.

## <a name="working-with-page-inspection"></a>Werken met Pagina-inspectie

U begint pagina-inspectie vanaf de pagina **Help en ondersteuning**. Kies het vraagteken in de rechterbovenhoek, kies **Help en ondersteuning** en kies vervolgens **Pagina's en gegevens inspecteren**. Of u kunt gewoon de sneltoets **Ctrl+Alt+F1** gebruiken.

Het deelvenster **Pagina-inspectie** opent aan de zijkant. In de volgende afbeelding ziet u het deelvenster **Pagina-inspectie** op de pagina **Verkooporder**.

![Pagina-inspectie](media/page-inspection-example.png)

Wanneer het deelvenster **Pagina-inspectie** wordt geopend, bevat het informatie over het hoofdpaginaobject.

Gebruik het toetsenbord of aanwijsapparaat om de focus te verplaatsen naar verschillende elementen op de pagina. Wanneer u een feitenblok of een deel van de hoofdpagina selecteert, worden de grenzen ervan gemarkeerd door een rand en bevat het deelvenster **Pagina-inspectie** informatie over het geselecteerde element. De vorige afbeelding bevat bijvoorbeeld informatie over het lijstonderdeel op de pagina **Verkooporder**. Terwijl u naar andere pagina's in de toepassing navigeert, wordt het deelvenster **Pagina-inspectie** automatisch bijgewerkt met pagina-informatie.

Voor meer informatie over wat wordt weergegeven in pagina-inspectie raadpleegt u [Pagina's inspecteren en er problemen mee oplossen](/dynamics365/business-central/dev-itpro/developer/devenv-inspecting-pages) in de Help van Business Central Developer en IT Pro.

Als u niet de details ziet die u verwacht te zien in het deelvenster **Pagina-inspectie**, hebt u waarschijnlijk niet de vereiste machtigingen, zoals beschreven in het volgende gedeelte.

## <a name="controlling-access-to-page-inspection-details"></a>Toegang bepalen tot details van pagina-inspectie

Als beheerder kunt u toegang bepalen tot alle details die worden weergegeven in het deelvenster **Pagina-inspectie** door de machtigingen te configureren die gebruikers hebben. Als u een gebruikersmachtiging wilt verlenen tot de volledige details, geeft u gebruikers de machtiging **Uitvoeren** voor het **Systeem**-object **5330**. U verleent deze machtiging door een machtigingenset te gebruiken (zoals **Problemen met D365 oplossen**) of een gebruikersgroep (zoals **Problemen met D365 oplossen**). Zie [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md) voor meer informatie over machtigingen.

Gebruikers aan wie geen machtigingen zijn verleend voor **Systeemobject 5330** kunnen wel toegang krijgen tot het deelvenster **Pagina-inspectie**, maar ze zien alleen de velden **Pagina** en **Tabel**, die basisdetails bevatten die ze kunnen doorgeven aan hun ondersteuningsteam.

## <a name="see-also"></a>Zie ook

[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
