---
title: Invoicing en Finance and Operations, Business edition gebruiken | Microsoft Docs
description: Oplossing voor het krijgen van toegang tot Microsoft Invoicing wanneer u zich hebt aangemeld voor Dynamics 365 for Finance and Operations, Business edition.
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/22/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: abceec5b1bc588e2842d0f512240c30eccbf6f8e
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---
# <a name="using-the-same-office-365-account-in-included365finincludesd365finlongmdmd-and-microsoft-invoicing"></a>Dezelfde Office 365-account gebruiken in [!INCLUDE[d365fin](includes/d365fin_long_md.md)] en Microsoft Invoicing
Wanneer u zich aanmeldt voor de proefversie van [!INCLUDE[d365fin](includes/d365fin_md.md)], kunt u kiezen voor de evaluatiefase van 30 dagen, het abonnement laten ingaan of stoppen met het gebruiken van [!INCLUDE[d365fin](includes/d365fin_md.md)]. In alle gevallen kan er bij het aanmelden bij de Office-portal een tegel met de naam **Business center** worden weergegeven. Klik hierop. Deze tegel maakt deel uit van het Office 365 Business Premium-abonnement, dus niet iedereen krijgt deze tegel te zien in de Office-portal.  

Als u het Business center opent, wordt er een gedeelte met de naam **Invoicing** weergegeven. Als u dat gedeelte opent, wordt het bericht weergegeven dat u geen toegang tot Microsoft Invoicing hebt omdat uw account wordt gebruikt in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Er wordt een vergelijkbaar bericht weergegeven als u de mobiele app voor Invoicing installeert.  

## <a name="workaround"></a>Oplossing
Invoicing en [!INCLUDE[d365fin](includes/d365fin_md.md)] delen een platform. Dit betekent dat u als een bestaande gebruiker van [!INCLUDE[d365fin](includes/d365fin_md.md)] wordt herkend wanneer u op Invoicing klikt in het Business center. De reden hiervoor is dat Invoicing niet hetzelfde bedrijf kan gebruiken als [!INCLUDE[d365fin](includes/d365fin_md.md)].  

U moet u daarom aanmelden bij [!INCLUDE[d365fin](includes/d365fin_md.md)], de naam van uw bestaande bedrijf wijzigen en vervolgens een nieuw bedrijf maken om in Invoicing te gebruiken. Er worden geen gegevens verplaatst of overschreven tijdens deze oplossingsprocedure.

### <a name="to-rename-your-company"></a>De naam van uw bedrijf wijzigen
1.  Meld u aan bij uw [!INCLUDE[d365fin](includes/d365fin_md.md)].  
2.  Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Bedrijven** in en klik vervolgens op de gerelateerde koppeling.  
3.  Kies in het venster **Bedrijven** de knop **Lijst bewerken**.  
4.  Wijzig de naam van het item *Mijn bedrijf*.  

    Wacht een aantal minuten. Er wordt een aantal wijzigingen doorgevoerd in de onderliggende database, wat enige tijd kost.
5.  Wanneer het systeem klaar is, kiest u de knop **Nieuw bedrijf maken**.  
6.  Geef in het dialoogvenster dat verschijnt de naam op als *Mijn bedrijf* en kies de optie **Suite-productie - Alleen instellingsgegevens**.  

Dit kost opnieuw een aantal minuten. Wanneer het proces is voltooid, kunt u Invoicing openen als onderdeel van uw Office 365 Business Premium-ervaring.  

### <a name="what-about-my-data"></a>Hoe zit het met mijn gegevens?
Wanneer u de naam van het oorspronkelijke Mijn bedrijf wijzigt, wordt de naam gewijzigd van de databasetabellen met de bestaande [!INCLUDE[d365fin](includes/d365fin_md.md)]-gegevens, maar de gegevens zelf blijven ongewijzigd.  

Als u zowel Invoicing als [!INCLUDE[d365fin](includes/d365fin_md.md)] gebruikt, worden de gegevens in twee verschillende containers (de twee bedrijven) opgeslagen. Er wordt niets gedeeld, dus u moet de klanten en artikelen in beide bedrijven beheren.  

## <a name="see-also"></a>Zie ook
[Veelgestelde vragen](across-faq.md)  
[Installatie en beheer](admin-setup-and-administration.md)  

