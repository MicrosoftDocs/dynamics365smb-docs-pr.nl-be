---
title: Invoicing en Business Central gebruiken | Microsoft Docs
description: Oplossing om Microsoft Invoicing te kunnen openen wanneer u zich hebt aangemeld voor Dynamics 365 Business Central.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/26/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: add32e82465610830b68a979e238103bfa10d438
ms.openlocfilehash: 95213b7d5881945bb2880e6288eef1b415427ca5
ms.contentlocale: nl-be
ms.lasthandoff: 11/29/2018

---
# <a name="using-the-same-office-365-account-in-included365finincludesd365finlongmdmd-and-microsoft-invoicing"></a>Dezelfde Office 365-account gebruiken in [!INCLUDE[d365fin](includes/d365fin_long_md.md)] en Microsoft Invoicing
Wanneer u zich aanmeldt voor de proefversie van [!INCLUDE[d365fin](includes/d365fin_md.md)], kunt u kiezen voor de evaluatiefase van 30 dagen, het abonnement laten ingaan of stoppen met het gebruiken van [!INCLUDE[d365fin](includes/d365fin_md.md)]. In alle gevallen kan er bij het aanmelden bij de Office-portal een tegel met de naam **Microsoft Invoicing** worden weergegeven. Klik hierop. Deze tegel maakt deel uit van het Office 365 Business Premium-abonnement, dus niet iedereen krijgt deze tegel te zien in de Office-portal.  

Als u Microsoft Invoicing opent, wordt het bericht weergegeven dat u geen toegang tot Microsoft Invoicing hebt omdat uw account wordt gebruikt in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Er wordt een vergelijkbaar bericht weergegeven als u de mobiele app voor Invoicing installeert.  

## <a name="workaround"></a>Oplossing
Invoicing en [!INCLUDE[d365fin](includes/d365fin_md.md)] delen een platform. Dit betekent dat u als een bestaande gebruiker van [!INCLUDE[d365fin](includes/d365fin_md.md)] wordt herkend wanneer u op Invoicing klikt in het Business center. De reden hiervoor is dat Invoicing niet hetzelfde bedrijf kan gebruiken als [!INCLUDE[d365fin](includes/d365fin_md.md)].  

U moet u daarom aanmelden bij [!INCLUDE[d365fin](includes/d365fin_md.md)], de naam van uw bestaande bedrijf wijzigen en vervolgens een nieuw bedrijf maken om in Invoicing te gebruiken. Er worden geen gegevens verplaatst of overschreven tijdens deze oplossingsprocedure.

### <a name="to-rename-your-company"></a>De naam van uw bedrijf wijzigen
1.  Meld u aan bij uw [!INCLUDE[d365fin](includes/d365fin_md.md)].  
2.  Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bedrijven** in en kies vervolgens de gerelateerde koppeling.  
3.  Kies op de pagina **Bedrijven** de knop **Lijst bewerken**.  
4.  Wijzig de naam van het item *Mijn bedrijf*.  

    Wacht een aantal minuten. Er wordt een aantal wijzigingen doorgevoerd in de onderliggende database, wat enige tijd kost.
5.  Wanneer het systeem klaar is, kiest u de knop **Nieuw bedrijf maken**.  
6.  Geef in het dialoogvenster dat verschijnt de naam op als *Mijn bedrijf* en kies de optie **Productie - Alleen instellingsgegevens**.  

Dit kost opnieuw een aantal minuten. Wanneer het proces is voltooid, kunt u Invoicing openen als onderdeel van uw Office 365 Business Premium-ervaring.  

### <a name="what-about-my-data"></a>Hoe zit het met mijn gegevens?
Wanneer u de naam van het oorspronkelijke Mijn bedrijf wijzigt, wordt de naam gewijzigd van de databasetabellen met de bestaande [!INCLUDE[d365fin](includes/d365fin_md.md)]-gegevens, maar de gegevens zelf blijven ongewijzigd.  

Als u zowel Invoicing als [!INCLUDE[d365fin](includes/d365fin_md.md)] gebruikt, worden de gegevens in twee verschillende containers (de twee bedrijven) opgeslagen. Er wordt niets gedeeld, dus u moet de klanten en artikelen in beide bedrijven beheren.  

## <a name="see-also"></a>Zie ook
[Veelgestelde vragen](across-faq.md)  
[Beheer](admin-setup-and-administration.md)  

