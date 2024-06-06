---
title: Uw browser instellen
description: Beschrijft hoe u browsers instelt om te werken met Business Central en producten die ermee integreren.
author: jswymer
ms.topic: get-started
ms.devlang: al
ms.search.keywords: 'Teams, web client, troubleshooting, errors'
ms.date: 12/04/2023
ms.author: jswymer
ms.service: dynamics-365-business-central
---
# <a name="setting-up-and-troubleshooting-your-browser-to-work-with-business-central-web-client"></a>Uw browser instellen en er problemen mee oplossen om te werken met de Business Central-webclient

In dit artikel wordt uitgelegd hoe u uw browser zo instelt dat de [!INCLUDE[web_client](includes/web_client.md)] en al zijn functies werken naar behoren. Lees dit artikel als u problemen ondervindt bij het openen van de [!INCLUDE[web_client](includes/web_client.md)], omdat sommige problemen kunnen worden veroorzaakt door de instellingen van uw browser.

Het artikel bevat details voor het instellen van Microsoft Edge, maar de vereisten voor JavaScript, cookies en pop-ups zijn hetzelfde voor alle ondersteunde browsers. Raadpleeg voor andere browsers de instructies van de fabrikant.  

## <a name="use-a-supported-browser"></a>Een ondersteunde browser gebruiken

Zorg ervoor dat u een van de ondersteunde browsers gebruikt. Zie [Minimumvereisten om Business Central te gebruiken](product-requirements.md#browsers).

We raden u aan een stabiele kanaalversie van een webbrowser te gebruiken, omdat dit de meest betrouwbare en stabiele versie is die uitgebreide tests en bugfixes heeft ondergaan. Dit zorgt ervoor dat u de beste ervaring hebt en minder snel problemen ondervindt tijdens het gebruik van de webclient.  

## <a name="allow-javascript-from-business-central"></a>JavaScript toestaan vanuit Business Central

*Probleem:*

Als de browser JavaScript niet toestaat, ziet u **NietOndersteund/UitgeschakeldJavaScript** op de adresbalk en een **HTTP-fout 404.0 - niet gevonden** bericht wanneer u probeert [!INCLUDE[prod_short](includes/prod_short.md)] te openen en de 

<!-- http://localhost:8080/NotSupported/DisabledJavaScript HTTP Error 404.0 - Not Found
The resource you are looking for has been removed, had its name changed, or is temporarily unavailable. -->

*Oplossing:*

1. Ga in Microsoft Edge naar **Instellingen** > **Cookies en sitetoestemmingen** > **JavaScript**.
2. Ga op een van de volgende manieren te werk: Kies de stap die wordt aanbevolen door uw organisatie:

    - Verplaats de schakelaar **Toegestaan** naar links (Uit). Selecteer vervolgens **Toevoegen** en typ het adres (URL) voor [!INCLUDE[prod_short](includes/prod_short.md)] in het vak **Site**. Selecteer **Toevoegen** wanneer u klaar bent.
    - Verplaats de schakelaar **Toegestaan** naar rechts (Aan).

## <a name="allow-cookies-from-business-central"></a>Cookies toestaan vanuit Business Central

*Probleem:*

Als de browser geen cookies toestaat, krijgt u de volgende foutmelding:

**De pagina kon niet worden gevonden. Controleer het adres en probeer het opnieuw.** 

*Oplossing:*

1. Ga in Microsoft Edge naar **Instellingen** > **Cookies en sitetoestemmingen** > **Cookies en sitegegevens**.
2. Verplaats de schakelaar **Sites toestaan cookiegegevens op te slaan en te lezen** naar rechts (Aan).  

## <a name="allow-pop-ups-from-business-central"></a><a name="popup"></a>Pop-ups toestaan vanuit Business Central

[!INCLUDE[prod_short](includes/prod_short.md)] integreert met verschillende producten. In sommige gevallen, zoals bij Microsoft Teams, wordt [!INCLUDE[prod_short](includes/prod_short.md)] geopend in een venster binnen het product. Deze mogelijkheid vereist dat uw browser pop-ups toestaat vanuit [!INCLUDE[prod_short](includes/prod_short.md)].

*Probleem:*

Als pop-ups voor [!INCLUDE[prod_short](includes/prod_short.md)] worden geblokkeerd, krijgt u een bericht dat lijkt op het volgende bericht:

**Er is iets fout gegaan. Uw browser blokkeert mogelijk pop-ups die Business Central nodig heeft.**

<!--
Something went wrong
Your browser may be blocking pop-ups needed by Business Central.

Change your browser settings to allow pop-ups or allow this for trusted domains, then try again.
If these settings are managed for your organization, you should contact your administrator for assistance.

Try again
-->
*Oplossing:*

1. Ga in Microsoft Edge naar **Instellingen** > **Cookies en sitetoestemmingen** > **Pop-ups en omleidingen**.
2. Verplaats de schakelaar **Geblokkeerd** naar rechts (Aan).
3. Selecteer **Toevoegen**. Typ in het vak **Site** `https://businesscentral.dynamics.com` en selecteer **Toevoegen**.

## <a name="see-also"></a>Zie ook

[Problemen met Teams oplossen](admin-teams-troubleshooting.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
