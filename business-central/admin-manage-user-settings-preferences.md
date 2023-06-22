---
title: Gebruikersinstellingen en voorkeuren beheren als beheerder
description: Gebruikersinstellingen en voorkeuren beheren in Dynamics 365 Business Central.
author: sorenfriisalexandersen
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: 'user settings, preferences, language, region, time zone, regional settings'
ms.search.form: '9204,'
ms.date: 04/01/2021
ms.author: soalex
---
# <a name="manage-user-settings-and-preferences" />Gebruikersinstellingen en voorkeuren beheren

Als beheerder kunt u gebruikersinstellingen configureren in [!INCLUDE[prod_short](includes/prod_short.md)], vergelijkbaar met hoe individuele gebruikers hun eigen voorkeuren kunnen beheren op de pagina **Mijn instellingen**.  

Krijg een overzicht van alle gebruikers in de lijst **Gebruikers** en verander individuele instellingen door de actie **Gebruikersinstellingen** te kiezen voor de relevante gebruiker.

> [!TIP]
> De lijst **Gebruikersinstellingen** toont de huidige instellingen voor elke gebruiker. Als u afzonderlijke gebruikers wilt weergeven of bewerken, kiest u de actie **Weergeven** of **Bewerken**.

De pagina **Gebruikersinstellingenkaart** is vergelijkbaar met de pagina **Mijn instellingen** waartoe elke gebruiker toegang heeft, en het is een krachtig hulpmiddel voor u als beheerder om bijvoorbeeld standaardinstellingen in te stellen en gepersonaliseerde pagina's te wissen.  

## <a name="types-of-user-settings" />Soorten gebruikersinstellingen

*Gebruikersinstellingen* is niet hetzelfde als *gebruikersinstelling*, dat gaat over de gebruiker als entiteit en de toegang van de gebruiker tot het systeem. Bovendien hebben gebruikersinstellingen niets te maken met de personalisatie van een gebruiker, zoals kleine wijzigingen in de gebruikersinterface. Gebruikersinstellingen bepalen de vooraf gedefinieerde instellingen voor elke gebruiker in verschillende aspecten van de manier waarop de toepassing zich aan de gebruiker presenteert. De volgende paragraaf bevat de vijf soorten gebruikersinstellingen en voorkeuren die kunnen worden ingesteld door de gebruiker of centraal door de beheerder:

* **Bedrijf**  

  Deze instelling bepaalt het bedrijf waarbij moet worden aangemeld bij de volgende aanmelding. Een gebruiker kan toegang hebben tot meerdere bedrijven en kan actief zijn in meerdere bedrijven.

* **Rol**  

  De rol of het profiel beschrijft de functie van de gebruiker in het bedrijf, zoals *Verkoopmanager*, *Boekhouder* of *Inkoper*. Het profiel bepaalt vervolgens het rolcentrum van de gebruiker, de homepage die gebruikers zien wanneer ze zich aanmelden. Het profiel heeft geen invloed op de toegangsrechten tot functionaliteit in [!INCLUDE[prod_short](includes/prod_short.md)].  

* **Taal**  

  Definieert de toepassingstaal waarin [!INCLUDE[prod_short](includes/prod_short.md)] tekst, bijschriften en foutmeldingen presenteert. Als [!INCLUDE[prod_short](includes/prod_short.md)]-gebruikers worden gesynchroniseerd vanuit Microsoft 365, worden de taalinstellingen van Microsoft 365 gebruikt, ervan uitgaande dat de gebruiker dezelfde instellingen in Office-producten en [!INCLUDE[prod_short](includes/prod_short.md)] wil gebruiken. De beheerder kan de standaardinstelling wijzigen en elke gebruiker kan kiezen tussen beschikbare talen op de pagina Mijn instellingen. Maar ze worden gereset naar de waarde vanuit Microsoft 365 zodra de volgende synchronisatie wordt uitgevoerd.

  Als de taalinstelling van Microsoft 365 overeenkomt met een ondersteunde taal in [!INCLUDE[prod_short](includes/prod_short.md)], wordt deze taal gekozen voor de gebruiker.  

  > [!NOTE]
  > Mogelijk moet u een taal-app installeren voor [!INCLUDE[prod_short](includes/prod_short.md)] om de taal correct weer te geven. Daarom is het een goede gewoonte om de benodigde taal-apps te installeren voordat gebruikers zich de eerste keer aanmelden, zodat ze vanaf hun eerste dag een goede ervaring hebben. Zie voor meer informatie de lijst met [ondersteunde talen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations).  
  
* **Regio**  

  Definieert hoe datums en getallen worden gepresenteerd in de [!INCLUDE[prod_short](includes/prod_short.md)]-client, zoals of Europese of Amerikaanse datumnotaties moeten worden gebruikt of hoe het decimaalteken en scheidingstekens voor duizendtallen in bedragen moeten worden weergegeven. Als [!INCLUDE[prod_short](includes/prod_short.md)]-gebruikers worden gesynchroniseerd vanuit Microsoft 365, worden de regionale instellingen van Microsoft 365 gebruikt, ervan uitgaande dat de gebruiker dezelfde instellingen in Office-producten en [!INCLUDE[prod_short](includes/prod_short.md)] wil gebruiken. Een beheerder of gebruiker kan deze instellingen handmatig wijzigen in [!INCLUDE[prod_short](includes/prod_short.md)], maar ze worden gereset naar de waarde van Microsoft 365 zodra de volgende synchronisatie wordt uitgevoerd.

* **Tijdzone**  

  Definieert de tijdzone waarin de gebruiker zich bevindt. Momenteel wordt dit niet gesynchroniseerd vanuit Microsoft 365 en moet het handmatig worden ingesteld.  

* **Instructietips**

  [!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)] Als beheerder kunt u instructietips voor alle gebruikers uitschakelen, bijvoorbeeld als u bezig bent met onboarding van gebruikers die al bekend zijn met [!INCLUDE [prod_short](includes/prod_short.md)].  

> [!NOTE]
> Als een Microsoft 365-gebruikerssynchronisatie wordt uitgevoerd terwijl gebruikers zijn aangemeld bij [!INCLUDE[prod_short](includes/prod_short.md)], moeten deze gebruikers de browser vernieuwen of zich afmelden en weer aanmelden bij [!INCLUDE[prod_short](includes/prod_short.md)] om een mogelijk andere taal te zien die is ingesteld door de synchronisatieactie.

## <a name="overview-of-all-user-specific-changes" />Overzicht van alle gebruikersspecifieke wijzigingen

Als beheerder krijgt u een overzicht van individuele wijzigingen in [!INCLUDE [prod_short](includes/prod_short.md)] die elke gebruiker mogelijk heeft aangebracht op verschillende pagina's in [!INCLUDE [prod_short](includes/prod_short.md)]. Als gebruikers hun ervaring wijzigen in [!INCLUDE [prod_short](includes/prod_short.md)], zullen deze wijzigingen worden weerspiegeld in de lijst **Persoonlijke gebruikersinstellingen**. <!--Administrators can also set these settings for users before they log in the first time, so users do not have to do it themselves, providing them a better *getting started* experience.-->

<!-- >[!NOTE]
> User personalizations do not have anything to do with the *personal* lightweight changes a user can make to the user experience.-->

## <a name="to-review-or-delete-user-personalizations" />Gebruikerspersonalisaties bekijken of verwijderen

1. Kies het pictogram ![Pagina of rapport zoeken.](media/ui-search/search_small.png "Pictogram Pagina of rapport zoeken"), voer **Gepersonaliseerde pagina's** in en kies vervolgens de gerelateerde koppeling.
2. Dit toont de lijst met gebruikers en hun aangepaste pagina's. Om de personalisatie van een gebruiker te wissen, klikt u op de relevante rij of kiest u **Beheren** en kiest u vervolgens **Verwijderen**.

Hierdoor wordt de personalisatie verwijderd en keert de gebruikerservaring van de relevante pagina terug naar de standaardstatus.

## <a name="see-also" />Zie ook

[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Beschikbaarheid in landen/regio's en ondersteunde vertalingen](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Taal en landinstellingen wijzigen](about-locale-language.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
