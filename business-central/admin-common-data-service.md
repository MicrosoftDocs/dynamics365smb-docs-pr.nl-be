---
title: Werken met Common Data Service
description: Inleiding tot Common Data Service en zijn componenten.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 10/01/2020
ms.openlocfilehash: 85823e93b1d239bf4e59ec6a8872cdc4a2cef9c1
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911592"
---
# <a name="integrating-with-common-data-service"></a>Integreren met Common Data Service

Zakelijke apps gebruiken vaak gegevens van meer dan één bron. [!INCLUDE[d365fin](includes/cds_long_md.md)] combineert gegevens in één set logica die het gemakkelijker maakt om andere Dynamics 365-toepassingen, zoals [!INCLUDE[crm_md](includes/crm_md.md)] of uw eigen applicatie bovenop [!INCLUDE[d365fin](includes/cds_long_md.md)], te verbinden met [!INCLUDE[d365fin_md](includes/d365fin_md.md)]. Zie voor meer informatie over [!INCLUDE[d365fin](includes/cds_long_md.md)] [Wat is Common Data Service?](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)

De volgende stappen geven een overzicht van de stappen om [!INCLUDE[d365fin](includes/cds_long_md.md)] te integreren met [!INCLUDE[d365fin](includes/d365fin_md.md)].

> [!Note]  
> Deze taken vereisen de beveiligingsrol **Systeembeheerder** in [!INCLUDE[d365fin](includes/cds_long_md.md)] en [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1. Wijs licenties voor [!INCLUDE[d365fin](includes/cds_long_md.md)] toe aan de [!INCLUDE[d365fin](includes/d365fin_md.md)]-gebruikers die de geïntegreerde apps zullen gebruiken.

2. Een verbinding instellen met [!INCLUDE[d365fin](includes/cds_long_md.md)]. Zie voor meer informatie [Verbinden met Common Data Service](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Gegevens synchroniseren tussen de apps. Zie voor meer informatie [Business Central en Common Data Service synchroniseren](admin-synchronizing-business-central-and-sales.md). 

## <a name="getting-started-with-d365fin"></a>Aan de slag met [!INCLUDE[d365fin](includes/cds_long_md.md)]
Om mee te beginnen met [!INCLUDE[d365fin](includes/cds_long_md.md)] hebt u een Microsoft Power Apps-account nodig. Als u nog geen Power Apps-account hebt, kunt u er een gratis krijgen door te gaan naar [powerapps.com](https://web.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) en de koppeling **Ga gratis aan de slag** te kiezen. Voor meer informatie over hoe u aan de slag kunt gaan met [!INCLUDE[d365fin](includes/cds_long_md.md)] raadpleegt u de module [Aan de slag met Common Data Service](https://docs.microsoft.com/learn/modules/get-started-with-powerapps-common-data-service/) van Microsoft Learn.

## <a name="bi-directional-or-uni-directional-data-synchronization"></a>Bidirectionele of unidirectionele gegevenssynchronisatie
Afhankelijk van uw zakelijke behoeften kunt u de integratie instellen om gegevens te synchroniseren van of naar de ene Dynamics 365-bedrijfsapp naar de andere, of in beide richtingen in bijna realtime via [!INCLUDE[d365fin](includes/cds_long_md.md)]. Als u [!INCLUDE[d365fin](includes/d365fin_md.md)] bijvoorbeeld met [!INCLUDE[crm_md](includes/crm_md.md)] integreert via [!INCLUDE[d365fin](includes/cds_long_md.md)], kan een verkoper een verkooporder aanmaken in [!INCLUDE[crm_md](includes/crm_md.md)] en de order wordt dan gesynchroniseerd met [!INCLUDE[d365fin](includes/d365fin_md.md)]. Omgekeerd vanuit [!INCLUDE[crm_md](includes/crm_md.md)], kan de verkoper informatie bekijken uit [!INCLUDE[d365fin](includes/d365fin_md.md)] over de beschikbaarheid van het artikel op de order. 

## <a name="standard-and-custom-entities"></a>Standaard- en aangepaste entiteiten
[!INCLUDE[d365fin](includes/cds_long_md.md)] slaat gegevens veilig op in een set van entiteiten. Dat zijn sets records die vergelijkbaar zijn met hoe een tabel gegevens opslaat in een database. [!INCLUDE[d365fin](includes/cds_long_md.md)] bevat een basisset standaardentiteiten die typische scenario's dekken, maar u kunt ook aangepaste entiteiten maken die specifiek zijn voor uw organisatie. In [!INCLUDE[d365fin](includes/d365fin_md.md)] kunt u op de pagina Toewijzingen van integratietabellen standaard- en aangepaste entiteiten bekijken die worden gesynchroniseerd.

## <a name="about-the-base-cds-integration-solution"></a>Over de Basis-CDS-integratieoplossing

De Basis-CDS-integratieoplossing is een belangrijk onderdeel van de integratie. De oplossing voegt de vereiste rollen en toegangsniveaus toe aan de gebruikersaccounts voor de integratie en creëert entiteiten die nodig zijn om een [!INCLUDE[d365fin](includes/d365fin_md.md)]-bedrijf toe te wijzen aan bedrijfsunits in [!INCLUDE[d365fin](includes/cds_long_md.md)]. 

Standaard importeert de begeleide instelling **[!INCLUDE[d365fin](includes/cds_long_md.md)]-verbinding instellen** de oplossing. De begeleide instelling gebruikt daarvoor een beheerdersaccount dat u opgeeft. Dit account moet ook een geldige gebruiker in [!INCLUDE[d365fin](includes/cds_long_md.md)] zijn met de volgende beveiligingsrol:

* Systeembeheerder  

Zie voor meer informatie [Gebruikersaccounts instellen voor integratie met [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) en [Gebruikers maken in Microsoft Dynamics 365 (online) en beveiligingsrollen toewijzen](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles). 

Het beheerdersaccount wordt tijdens de installatie slechts één keer gebruikt vanwege configuratiewijzigingen die de Basis-CDS-integratieoplossing aanbrengt [!INCLUDE[d365fin](includes/cds_long_md.md)]. Nadat de oplossing is geïmporteerd, is het account niet meer nodig. Integratie gaat door met het gebruikersaccount te gebruiken dat automatisch specifiek voor de integratie is gemaakt.

Naast het aanpassen van [!INCLUDE[d365fin](includes/cds_long_md.md)] maakt de oplossing ook de volgende rollen in [!INCLUDE[d365fin](includes/cds_long_md.md)] voor de integratie:

* **Integratiebeheerder** - Biedt gebruikers de mogelijkheid de verbinding te beheren tussen [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[d365fin](includes/cds_long_md.md)]. Meestal is dit alleen toegewezen aan het automatisch gemaakte gebruikersaccount voor synchronisatie.  
* **Integratiegebruiker** - Geeft gebruikers toegang tot gesynchroniseerde gegevens. Meestal is dit toegewezen aan het automatisch gemaakte gebruikersaccount voor synchronisatie en andere gebruikers die de gesynchroniseerde gegevens moeten kunnen bekijken of openen.

Zie voor informatie over elke rol, zoals de machtigingen en toegangsniveaus, [Gebruikersaccounts instellen voor integratie met [!INCLUDE[d365fin](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Tijdens het instellen van de verbinding worden integratietabeltoewijzingen gemaakt die nodig zijn om gegevens te synchroniseren. Entiteiten in Common Data Service worden toegewezen aan tabellen en tabelvelden in Business Central via integratietabellen. Zie voor meer informatie [Standaardtoewijzing van entiteit voor synchronisatie](admin-synchronizing-business-central-and-sales.md#standard-entity-mapping-for-synchronization).

## <a name="see-also"></a>Zie ook
[Modellen voor gegevenseigendom](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Common Data Service](docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/administration-custom-cds-integration) -->



