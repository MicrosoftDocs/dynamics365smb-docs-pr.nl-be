---
title: 'Problemen oplossen: toegang tot camera en locatie'
description: In dit artikel wordt beschreven hoe u problemen met de toegang tot camera- en locatiegegevens in Business Central oplost.
author: bholtorf
ms.author: bholtorf
ms.date: 04/01/2021
ms.custom: na
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: conceptual
---

# <a name="troubleshooting-accessing-camera-and-location"></a><a name="troubleshooting-accessing-camera-and-location"></a>Problemen oplossen: toegang tot camera en locatie

U kunt enkele problemen tegenkomen wanneer u probeert toegang te krijgen tot de camera en de locatiegegevens van een apparaat [!INCLUDE[prod_short](includes/prod_short.md)]. Hieronder vindt u de mogelijke oorzaken van deze problemen en hoe u ze kunt omzeilen.

## <a name="device-must-have-camera-and-location-capabilities"></a><a name="device-must-have-camera-and-location-capabilities"></a>Het apparaat moet camera- en locatiemogelijkheden hebben

Om toegang te krijgen tot de camera of de locatie van een gebruiker vanaf een apparaat, moet het apparaat respectievelijk een fysieke camera hebben of de mogelijkheid om locatiegegevens op te halen.

Als uw apparaat camera- en locatiemogelijkheden heeft, maar u nog steeds problemen ondervindt, is het mogelijk dat sommige stuurprogramma's moeten worden bijgewerkt of opnieuw moeten worden geïnstalleerd. Zelfs als u het niet zeker weet, raden we u altijd aan om het besturingssysteem, de stuurprogramma's en de browser van uw apparaat bij te werken naar de nieuwste versie voor de beste ervaring.

## <a name="access-permissions-not-enabled"></a><a name="access-permissions-not-enabled"></a>Toegangsmachtigingen niet ingeschakeld

U moet algemene toegang tot de camera en locatie inschakelen vanuit de privacyinstellingen van uw apparaat en u moet daar expliciet toestemming voor geven aan [!INCLUDE[prod_short](includes/prod_short.md)] om er toegang toe te krijgen. Ga bijvoorbeeld om de machtigingen te zien of te wijzigen voor een apparaat dat op Windows draait naar **Instellingen**, kies **Privacy** en dan **App-machtigingen**. 

Voor mobiele apparaten moet u toegangsmachtigingen voor camera en locatie verlenen aan de mobiele [!INCLUDE[prod_short](includes/prod_short.md)]-app. Als u dit wilt doen voor een iOS-apparaat, gaat u naar **Instellingen**, kiest u **Privacy** en vervolgens **Camera** of **Locatie**. Ga voor Android-apparaten naar **Instellingen**, kies **Apps en meldingen**, **Geavanceerd**, **Machtigingenbeheer** en vervolgens **Camera** of **Locatie**.

Bovendien, als u [!INCLUDE[prod_short](includes/prod_short.md)] gebruikt in een browser, moet u ook de [!INCLUDE[prod_short](includes/prod_short.md)]-sitemachtiging voor toegang tot de camera of locatiegegevens verlenen. Als u de machtigingen van een site in de Microsoft Edge-browser wilt wijzigen, gaat u naar **Instellingen**, kiest u **Sitemachtigingen** en vervolgens **Camera** of **Locatie**. Merk op dat dit voor andere browsers anders kan zijn.

Standaard zal het apparaat of de browser een verzoek openen om toegang te krijgen tot deze mogelijkheden wanneer de gebruiker ze voor de eerste keer activeert.

> [!NOTE]  
> Sommige oude browsers geven geen toegang tot camera en locatie. Camera is bijvoorbeeld niet beschikbaar in Internet Explorer of de oudere Edge-browser.

## <a name="web-client-connection-not-secure"></a><a name="web-client-connection-not-secure"></a>Webclient-verbinding niet veilig

De camera- en locatiemogelijkheden zijn alleen beschikbaar bij toegang tot de webclient via SSL-beveiligde HTTP-verbindingen, met behulp van het `https://` URI-schema. 

De enige uitzondering is verbinding maken met `http://localhost`, gebruikt voor ontwikkelings- en testdoeleinden.


## <a name="work-with-virtualization-technologies"></a><a name="work-with-virtualization-technologies"></a>Werken met virtualisatietechnologieën

Bij het verbinden met [!INCLUDE[prod_short](includes/prod_short.md)] via Remote Desktop of andere virtualisatie is de toegang tot camera of locatie mogelijk niet beschikbaar. Als dit het geval is, gebruik dan het fysieke systeem.

## <a name="antivirus-software"></a><a name="antivirus-software"></a>Antivirussoftware
Sommige antivirussoftware blokkeert standaard de toegang tot de camera en de locatie. Vergeet niet om uw antivirussoftware-instellingen te controleren.

## <a name="see-also"></a><a name="see-also"></a>Zie ook
[De camera implementeren in AL](/dynamics365/business-central/dev-itpro/developer/devenv-implement-camera-al)  
[De locatie implementeren in AL](/dynamics365/business-central/dev-itpro/developer/devenv-implement-location-al)


[!INCLUDE[footer-include](includes/footer-banner.md)]
