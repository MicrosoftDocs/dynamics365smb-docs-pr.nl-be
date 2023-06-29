---
title: Werken met Microsoft Dataverse
description: Inleiding tot integratie en gebruik van Microsoft Dataverse en de componenten ervan om verbinding te maken met andere Dynamics 365-toepassingen.
author: brentholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.topic: conceptual
ms.date: 06/14/2021
---

# <a name="integrating-with-microsoft-dataverse"></a><a name="integrating-with-microsoft-dataverse"></a>Integreren met Microsoft Dataverse

Zakelijke apps gebruiken vaak gegevens van meer dan één bron. [!INCLUDE[prod_short](includes/cds_long_md.md)] combineert gegevens in één set logica die het gemakkelijker maakt om andere Dynamics 365-toepassingen, zoals [!INCLUDE[crm_md](includes/crm_md.md)] of uw eigen applicatie bovenop [!INCLUDE[prod_short](includes/cds_long_md.md)], te verbinden met [!INCLUDE[prod_short_md](includes/prod_short.md)]. Zie voor meer informatie over [!INCLUDE[prod_short](includes/cds_long_md.md)] [Wat is Dataverse?](/powerapps/maker/common-data-service/data-platform-intro)

De volgende stappen geven een overzicht van de stappen om [!INCLUDE[prod_short](includes/cds_long_md.md)] te integreren met [!INCLUDE[prod_short](includes/prod_short.md)].

> [!Note]  
> Deze taken vereisen de beveiligingsrol **Systeembeheerder** in [!INCLUDE[prod_short](includes/cds_long_md.md)] en [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Wijs licenties voor [!INCLUDE[prod_short](includes/cds_long_md.md)] toe aan de [!INCLUDE[prod_short](includes/prod_short.md)]-gebruikers die de geïntegreerde apps zullen gebruiken.

2. Een verbinding instellen met [!INCLUDE[prod_short](includes/cds_long_md.md)]. Zie voor meer informatie [Verbinden met Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Gegevens synchroniseren tussen de apps. Zie voor meer informatie [Business Central en Dataverse synchroniseren](admin-synchronizing-business-central-and-sales.md). 

## <a name="getting-started-with-"></a><a name="getting-started-with-"></a>Aan de slag met [!INCLUDE[prod_short](includes/cds_long_md.md)]

Om mee te beginnen met [!INCLUDE[prod_short](includes/cds_long_md.md)] hebt u een Microsoft Power Apps-account nodig. Als u nog geen Power Apps-account hebt, kunt u er een gratis krijgen door te gaan naar [powerapps.com](https://make.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) en de koppeling **Ga gratis aan de slag** te kiezen. Voor meer informatie over hoe u aan de slag kunt gaan met [!INCLUDE[prod_short](includes/cds_long_md.md)] raadpleegt u de module [Aan de slag met Dataverse](/training/modules/get-started-with-powerapps-common-data-service/) van Microsoft-training.

## <a name="bi-directional-or-uni-directional-data-synchronization"></a><a name="bi-directional-or-uni-directional-data-synchronization"></a>Bidirectionele of unidirectionele gegevenssynchronisatie

Afhankelijk van uw zakelijke behoeften kunt u de integratie instellen om gegevens te synchroniseren van of naar de ene Dynamics 365-bedrijfsapp naar de andere, of in beide richtingen in bijna realtime via [!INCLUDE[prod_short](includes/cds_long_md.md)]. Als u [!INCLUDE[prod_short](includes/prod_short.md)] bijvoorbeeld met [!INCLUDE[crm_md](includes/crm_md.md)] integreert via [!INCLUDE[prod_short](includes/cds_long_md.md)], kan een verkoper een verkooporder aanmaken in [!INCLUDE[crm_md](includes/crm_md.md)] en de order wordt dan gesynchroniseerd met [!INCLUDE[prod_short](includes/prod_short.md)]. Omgekeerd vanuit [!INCLUDE[crm_md](includes/crm_md.md)], kan de verkoper informatie bekijken uit [!INCLUDE[prod_short](includes/prod_short.md)] over de beschikbaarheid van het artikel op de order. 

## <a name="standard-and-custom-entities"></a><a name="standard-and-custom-entities"></a>Standaard- en aangepaste entiteiten

[!INCLUDE[prod_short](includes/cds_long_md.md)] slaat gegevens veilig op in een set tabellen. Dat zijn sets records die vergelijkbaar zijn met hoe een tabel gegevens opslaat in een database. [!INCLUDE[prod_short](includes/cds_long_md.md)] bevat een basisset standaardtabellen die typische scenario's dekken, maar u kunt ook aangepaste tabellen maken die specifiek zijn voor uw organisatie. In [!INCLUDE[prod_short](includes/prod_short.md)] kunt u op de pagina Toewijzingen van integratietabellen standaard- en aangepaste tabellen bekijken die worden gesynchroniseerd.

## <a name="about-the-business-central-base-integration-solution"></a><a name="about-the-business-central-base-integration-solution"></a>Over de Business Central-basisintegratieoplossing

De basisintegratieoplossing is een belangrijk onderdeel van de integratie. De oplossing voegt de vereiste rollen en toegangsniveaus toe aan de gebruikersaccounts voor de integratie en maakt tabellen die nodig zijn om een [!INCLUDE[prod_short](includes/prod_short.md)]-bedrijf toe te wijzen aan een bedrijfsunit in [!INCLUDE[prod_short](includes/cds_long_md.md)]. 

Standaard importeert de begeleide instelling **[!INCLUDE[prod_short](includes/cds_long_md.md)]-verbinding instellen** de oplossing. De begeleide instelling gebruikt daarvoor een beheerdersaccount dat u opgeeft. Dit account moet ook een geldige gebruiker in [!INCLUDE[prod_short](includes/cds_long_md.md)] zijn met de volgende beveiligingsrol:

* Systeembeheerder  

Zie voor meer informatie [Gebruikersaccounts instellen voor integratie met [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) en [Gebruikers maken in Microsoft Dynamics 365 (online) en beveiligingsrollen toewijzen](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles). 

Het beheerdersaccount wordt tijdens de installatie slechts één keer gebruikt voor de configuratiewijzigingen die de basisintegratieoplossing aanbrengt [!INCLUDE[prod_short](includes/cds_long_md.md)]. Nadat de oplossing is geïmporteerd, is het account niet meer nodig. Integratie gaat door met het gebruikersaccount te gebruiken dat automatisch specifiek voor de integratie is gemaakt.

Naast het aanpassen van [!INCLUDE[prod_short](includes/cds_long_md.md)] maakt de oplossing ook de volgende rollen in [!INCLUDE[prod_short](includes/cds_long_md.md)] voor de integratie:

* **Integratiebeheerder** - Biedt gebruikers de mogelijkheid de verbinding te beheren tussen [!INCLUDE[prod_short](includes/prod_short.md)] en [!INCLUDE[prod_short](includes/cds_long_md.md)]. Meestal is dit alleen toegewezen aan het automatisch gemaakte gebruikersaccount voor synchronisatie.  
* **Integratiegebruiker** - Geeft gebruikers toegang tot gesynchroniseerde gegevens. Meestal is dit toegewezen aan het automatisch gemaakte gebruikersaccount voor synchronisatie en andere gebruikers die de gesynchroniseerde gegevens moeten kunnen bekijken of openen.

Zie voor informatie over elke rol, zoals de machtigingen en toegangsniveaus, [Gebruikersaccounts instellen voor integratie met [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Tijdens het instellen van de verbinding worden integratietabeltoewijzingen gemaakt die nodig zijn om gegevens te synchroniseren. Entiteiten in [!INCLUDE[prod_short](includes/cds_long_md.md)] worden toegewezen aan tabellen en tabelvelden in Business Central via integratietabellen. Zie voor meer informatie [Standaardtoewijzing van entiteit voor synchronisatie](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/modules/use-model-driven-apps-common-data-service/)

## <a name="see-also"></a><a name="see-also"></a>Zie ook

[Modellen voor gegevenseigendom](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Dataverse](\dynamics365\business-central\dev-itpro\administration\administration-custom-cds-integration) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]
