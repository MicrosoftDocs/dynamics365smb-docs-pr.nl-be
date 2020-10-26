---
title: Gebruikersinstellingen en voorkeuren beheren in Dynamics 365 Business Central
description: Gebruikersinstellingen en voorkeuren beheren in Dynamics 365 Business Central.
author: sorenfriisalexandersen
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: user settings, preferences, language, region, time zone, regional settings
ms.date: 10/01/2020
ms.author: soalex
ms.openlocfilehash: a08845f3465e24036abcb82ea6d2917deda24663
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911317"
---
# <a name="manage-user-settings-and-preferences"></a>Gebruikersinstellingen en voorkeuren beheren

Als beheerder kunt u gebruikersinstellingen invoeren in [!INCLUDE[d365fin](includes/d365fin_md.md)], vergelijkbaar met hoe individuele gebruikers hun eigen voorkeuren kunnen beheren op de pagina **Mijn instellingen** .  

## <a name="types-of-user-settings"></a>Soorten gebruikersinstellingen

*Gebruikersinstellingen* is niet hetzelfde als *gebruikersinstelling* , dat gaat over de gebruiker als entiteit en de toegang van de gebruiker tot het systeem. Bovendien hebben gebruikersinstellingen niets te maken met de personalisatie van een gebruiker, zoals kleine wijzigingen in de gebruikersinterface. Gebruikersinstellingen bepalen de voorkeuren van de gebruiker in verschillende aspecten van de manier waarop de toepassing zich aan de gebruiker presenteert. De volgende paragraaf bevat de vijf soorten gebruikersinstellingen en voorkeuren die kunnen worden ingesteld door de gebruiker of centraal door de beheerder:

- **Bedrijf**  

  Deze instelling bepaalt het bedrijf waarbij moet worden aangemeld bij de volgende aanmelding. Een gebruiker kan toegang hebben tot meerdere bedrijven en kan actief zijn in meerdere bedrijven.

- **Profiel (rollen)**  

  Het profiel beschrijft de functie van de gebruiker in het bedrijf, zoals *Verkoopmanager* , *Boekhouder* , of *Inkoper* . Het profiel bepaalt vervolgens het rolcentrum van de gebruiker, de homepage die gebruikers zien wanneer ze zich aanmelden. Het profiel heeft geen invloed op de toegangsrechten tot functionaliteit in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

- **Landinstellings-id (regionale instellingen)**  

  Definieert hoe datums en getallen worden gepresenteerd in de [!INCLUDE[d365fin](includes/d365fin_md.md)]-client, zoals of Europese of Amerikaanse datumnotaties moeten worden gebruikt of hoe het decimaalteken en scheidingstekens voor duizendtallen in bedragen moeten worden weergegeven. Als [!INCLUDE[d365fin](includes/d365fin_md.md)]-gebruikers worden gesynchroniseerd vanuit Microsoft 365, worden de regionale instellingen van Microsoft 365 gebruikt, ervan uitgaande dat de gebruiker dezelfde instellingen in Office-producten en [!INCLUDE[d365fin](includes/d365fin_md.md)] wil gebruiken. Een beheerder of gebruiker kan deze instellingen handmatig wijzigen in [!INCLUDE[d365fin](includes/d365fin_md.md)], maar ze worden gereset naar de waarde van Microsoft 365 zodra de volgende synchronisatie wordt uitgevoerd.

- **Taal**  

  Definieert de toepassingstaal waarin [!INCLUDE[d365fin](includes/d365fin_md.md)] tekst, bijschriften en foutmeldingen presenteert. Als [!INCLUDE[d365fin](includes/d365fin_md.md)]-gebruikers worden gesynchroniseerd vanuit Microsoft 365, worden de taalinstellingen van Microsoft 365 gebruikt, ervan uitgaande dat de gebruiker dezelfde instellingen in Office-producten en [!INCLUDE[d365fin](includes/d365fin_md.md)] wil gebruiken. Een beheerder of gebruiker kan deze instellingen handmatig wijzigen in [!INCLUDE[d365fin](includes/d365fin_md.md)], maar ze worden gereset naar de waarde van Microsoft 365 zodra de volgende synchronisatie wordt uitgevoerd.

  Als de taalinstelling van Microsoft 365 overeenkomt met een ondersteunde taal in [!INCLUDE[d365fin](includes/d365fin_md.md)], wordt deze taal gekozen voor de gebruiker.  

  > [!NOTE]
  > Mogelijk moet u een taal-app installeren voor [!INCLUDE[d365fin](includes/d365fin_md.md)] om de taal correct weer te geven. Daarom is het een goede gewoonte om de benodigde taal-apps te installeren voordat gebruikers zich de eerste keer aanmelden, zodat ze vanaf hun eerste dag een goede ervaring hebben. Zie voor meer informatie de lijst met [ondersteunde talen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations).  
  
- **Tijdzone**  

  Definieert de tijdzone waarin de gebruiker zich bevindt. Momenteel wordt dit niet gesynchroniseerd vanuit Microsoft 365 en moet het handmatig worden ingesteld.  

> [!NOTE]
> Als een Microsoft 365-gebruikerssynchronisatie wordt uitgevoerd terwijl gebruikers zijn aangemeld bij [!INCLUDE[d365fin](includes/d365fin_md.md)], moeten deze gebruikers de browser vernieuwen of zich afmelden en weer aanmelden bij [!INCLUDE[d365fin](includes/d365fin_md.md)] om een mogelijk andere taal te zien die is ingesteld door de synchronisatieactie.

## <a name="overview-of-all-user-settings"></a>Overzicht van alle gebruikersinstellingen

Beheerders hebben de mogelijkheid om deze instellingen voor gebruikers in elk bedrijf in te stellen of te wijzigen. Dit wordt gedaan op de pagina **Persoonlijke gebruikersinstellingen** . Records op deze pagina weerspiegelen de keuzes van de individuele gebruiker voor de bovenstaande instellingen, één record per gebruiker. Als gebruikers hun instellingen wijzigen op de pagina **Mijn instellingen** , zullen deze wijzigingen worden weerspiegeld in de lijst **Persoonlijke gebruikersinstellingen** . Beheerders kunnen deze instellingen ook voor gebruikers instellen voordat ze zich voor de eerste keer aanmelden, zodat gebruikers dit niet zelf hoeven te doen, waardoor ze een betere *beginervaring* krijgen.

> [!NOTE]
> Persoonlijke gebruikersinstellingen hebben niets te maken met de *persoonlijke* kleine veranderingen die een gebruiker kan aanbrengen in de gebruikerservaring.

## <a name="to-review-or-make-changes-to-user-settings"></a>Gebruikersinstellingen bekijken of wijzigen

1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Pagina of rapport zoeken"), voer **Persoonlijke gebruikersinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Dit toont de lijst met gebruikers en hun instellingen. Klik op om de instellingen van een gebruiker te wijzigen op **Gebruikers-ID** of kies **Beheren** en dan **Bewerken** .
3. De kaart **Persoonlijke gebruikersinstellingen** voor de specifieke gebruiker wordt weergegeven en gewenste wijzigingen kunnen worden aangebracht.  

## <a name="see-also"></a>Zie ook

[Aan de slag](product-get-started.md)  
[Beschikbaarheid in landen/regio's en ondersteunde vertalingen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Taal en landinstellingen wijzigen](about-locale-language.md)  
