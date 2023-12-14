---
title: Problemen met connectiviteit oplossen
description: Beschrijft hoe u de pagina Problemen met connectiviteit oplossen kunt gebruiken om problemen met verbinding met Business Central Online te identificeren en op te lossen.
author: jswymer
ms.topic: get-started
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'connectivity, troubleshooting, connection problems'
ms.date: 11/24/2023
ms.author: jswymer
ROBOTS: NOINDEX
---

# Problemen met connectiviteit voor Business Central oplossen

> **GELDT VOOR:** [!INCLUDE[prod_short](includes/prod_short.md)] Online
>
> Deze functie is momenteel beschikbaar in preview. De functionaliteit en documentatie kunnen in latere releases veranderen. Als u op basis van uw eigen bevindingen wilt bijdragen aan de documentatie, selecteert u ![Artikel bewerken in GitHub](media/github-edit-pencil.png) **Bewerken** en stelt u wijzigingen voor. Dan kijken we ernaar!

[!INCLUDE[prod_short](includes/prod_short.md)] Online bevat de pagina **Problemen met connectiviteit oplossen**, die u kunt gebruiken om problemen met uw verbinding met de online service te identificeren. Er zijn verschillende dingen die van invloed zijn op de connectiviteit met Business Central, zoals de firewallinstellingen van uw netwerk of de configuratie van de domeinnaamservice. Op de pagina kunt u een lijst met controles uitvoeren die een diagnose stellen van veelvoorkomende verbindingsproblemen met Business Central. U kunt de informatie gebruiken om te proberen de problemen zelf op te lossen of deze doorgeven aan uw ondersteuningsvertegenwoordiger.

> [!NOTE]
> De pagina **Problemen met connectiviteit oplossen** test de netwerkprestaties of betrouwbaarheid niet, zoals de snelheid van uw verbinding. Het verifieert alleen de verbinding met verschillende bronnen.

## De verbindingscontrole starten 

1. Open een internetbrowser.
2. Voer in het adres de URL in die u gebruikt om Business Central te openen en voeg `/connectivity` aan het einde toe. 

    Als u bijvoorbeeld `https://businesscentral.dynamics.com` gebruikt, voert u het volgende in:

    ```http
    https://businesscentral.dynamics.com/connectivity
    ```

    Of als de URL de tenant-id bevat, zoals `https://businesscentral.dynamics.com/12345678-1234-1234-1234-1234567890AB`, dan voert u het volgende in:

    ```http
    https://businesscentral.dynamics.com/12345678-1234-1234-1234-1234567890AB/connectivity
    ```
 
3. Kies op de pagina **Problemen met connectiviteit oplossen** **Controle starten**.

    Er wordt een reeks controles uitgevoerd en het resultaat van elke controle wordt weergegeven:

    - ![Verbindingscontrole geslaagd.](media/connectivity-check.png) geeft aan dat de controle is geslaagd.
    - ![Verbindingscontrole mislukt.](media/connectivity-failed.png) geeft aan dat de controle is mislukt. Bekijk het bericht onder de controle voor meer details.
    - ![De verbindingscontrole is niet uitgevoerd.](media/connectivity-blocked.png) geeft aan dat de controle niet is uitgevoerd, meestal vanwege het mislukken van een eerdere controle. Bekijk het bericht onder de controle voor meer details.

4. Om de controle opnieuw uit te voeren kiest u **Controle opnieuw starten**.

In de volgende secties worden de uitgevoerde controles uitgelegd en worden enkele tips gegeven om eventuele problemen op te lossen.

## Basisinternetconnectiviteit

Controleert of u verbinding met internet hebt door te verifiëren dat u toegang hebt tot een bekend openbaar domein, zoals www.bing.com.

|Probleem|Dingen om te proberen|
|-------|-------------|
|Uw browser ondersteunt deze controle niet|Open de pagina in een ondersteunde browser en probeer het opnieuw. Zie voor een lijst met ondersteunde browsers [Minimumvereisten voor het gebruik van Business Central - Browsers](product-requirements.md#browsers).|
|Kan de server niet pingen op de volgende URL: {url}|Controleer de instellingen van uw firewall.|

## CDN-bronnen (Content Delivery Network) laden

[!INCLUDE[prod_short](includes/prod_short.md)] gebruikt Azure Content Delivery Network (CDN) om resources te bieden die nodig zijn om de Business Central-webclient uit te voeren. Deze controle verifieert of de vereiste bronnen beschikbaar en toegankelijk zijn door het Business Central-exemplaar in CDN te pingen.

|Probleem|Dingen om te proberen|
|-------|-------------|
|Uw browser ondersteunt deze controle niet|Zie controle **Basisinternetconnectiviteit**.|
|Kan de server niet pingen op de volgende URL: {url}|Controleer de instellingen van uw firewall.|

## Gebruikersverificatie

Controleert of de huidige gebruiker is ingelogd met een geldig Business Central-account.

|Probleem|Dingen om te proberen|
|-------|-------------|
|Er is momenteel geen gebruiker geverifieerd|Log in op Business Central met een geldige gebruikersnaam en wachtwoord.|

## Detectie van Business Central-omgevingen

Controleert op Business Central-omgevingen die beschikbaar zijn voor een geverifieerde gebruiker en verifieert vervolgens of de gebruiker kan worden geverifieerd in de omgeving.
<!-- example: Your user name or password is incorrect, or you do not have a valid account.. Request duration: 332 milliseconds)-->

|Probleem|Dingen om te proberen|
|-------|-------------|
|Geen geverifieerde gebruiker om deze controle voor uit te voeren|Zie de controle **Gebruikersverificatie**.|
|Kan de beschikbare omgevingen voor uw account niet ophalen.|Bekijk de lijst met beschikbare omgevingen in het Business Central-beheercentrum.|
|Uw gebruikersnaam of uw wachtwoord is onjuist, of u hebt geen geldig account.| Controleer of u bent ingelogd met de juiste gebruikersnaam en wachtwoord.|

## Connectiviteit van toepassingsservice

Controleert of de geverifieerde gebruiker verbinding kan maken met een gedetecteerde omgeving, meestal beginnend met de productieomgeving.

|Probleem|Dingen om te proberen|
|-------|-------------|
|Geen geverifieerde gebruiker om deze controle voor uit te voeren|Zie de controle **Gebruikersverificatie**.|
|Kan de beschikbare omgevingen voor uw account niet ophalen.|Zie **Detectie van Business Central-omgevingen**.|
|Geen clusteradres om deze controle voor uit te voeren|Bekijk de lijst met beschikbare omgevingen in het Business Central-beheercentrum.|
|Versie-eindpunt bestaat niet|Bekijk de lijst met beschikbare omgevingen in het Business Central-beheercentrum.|

## Verbinding met webserver

Controleert of de geverifieerde gebruiker succesvol verbinding kan maken met de webserver.

|Probleem|Dingen om te proberen|
|-------|-------------|
|Er is geen geverifieerde gebruiker om deze controle voor uit te voeren|Zie de controle **Gebruikersverificatie**.|
|Kan de beschikbare omgevingen voor uw account niet ophalen.|Zie **Detectie van Business Central-omgevingen**.|
|Geen clusteradres om deze controle voor uit te voeren|Bekijk de lijst met beschikbare omgevingen in het Business Central-beheercentrum.|
|Kan geen verbinding maken met de webserver|Wis de cache en laad de pagina opnieuw.|

## Servicestatus

Rapporteert de status van de service van Business Central door te controleren op aangegeven storingen.

|Probleem|Dingen om te proberen|
|-------|-------------|
|Er is geen geverifieerde gebruiker om deze controle voor uit te voeren|Zie de controle **Gebruikersverificatie**.|
|Business Central is tijdelijk niet beschikbaar. Probeer het later nogmaals.|Probeer het later nogmaals.|

## Zie ook

[Resources voor Help en ondersteuning](product-help-and-support.md)  
[Overzicht van taken om Business Central in te stellen](setup.md)  
[Veelgestelde vragen over het gebruik van Business Central](across-faq.yml)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Het beheercentrum van Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center)

[!INCLUDE[footer-include](includes/footer-banner.md)]
