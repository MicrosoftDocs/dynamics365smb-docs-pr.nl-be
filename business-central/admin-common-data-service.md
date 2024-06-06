---
title: Integreren met Microsoft Dataverse via gegevenssynchronisatie
description: Inleiding tot integratie en gebruik van Microsoft Dataverse en de componenten ervan om verbinding te maken met andere Dynamics 365-toepassingen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 03/08/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---

# Integreren met Microsoft Dataverse via gegevenssynchronisatie

Zakelijke apps gebruiken vaak gegevens van meer dan één bron. [!INCLUDE[prod_short](includes/cds_long_md.md)] combineert gegevens in een enkele set logica die het gemakkelijker maakt om [!INCLUDE[prod_short](includes/prod_short.md)] te verbinden met andere Dynamics 365-applicaties. Bijvoorbeeld [!INCLUDE[crm_md](includes/crm_md.md)] of uw eigen applicatie gebouwd op [!INCLUDE[prod_short](includes/cds_long_md.md)]. Ga naar [Wat is Dataverse?](/powerapps/maker/common-data-service/data-platform-intro) voor meer informatie over [!INCLUDE[prod_short](includes/cds_long_md.md)].

De volgende stappen geven een overzicht van de stappen om [!INCLUDE[prod_short](includes/cds_long_md.md)] te integreren met [!INCLUDE[prod_short](includes/prod_short.md)].

> [!Note]  
> Deze taken vereisen de beveiligingsrol **Systeembeheerder** in [!INCLUDE[prod_short](includes/cds_long_md.md)] en [!INCLUDE[prod_short](includes/prod_short.md)].  

1. Wijs licenties voor [!INCLUDE[prod_short](includes/cds_long_md.md)] toe aan de [!INCLUDE[prod_short](includes/prod_short.md)]-gebruikers die de geïntegreerde apps zullen gebruiken.

2. Een verbinding instellen met [!INCLUDE[prod_short](includes/cds_long_md.md)]. Zie voor meer informatie [Verbinden met Dataverse](admin-how-to-set-up-a-dynamics-crm-connection.md).  

3. Gegevens synchroniseren tussen de apps. Zie voor meer informatie [Business Central en Dataverse synchroniseren](admin-synchronizing-business-central-and-sales.md). 

## Aan de slag met [!INCLUDE[prod_short](includes/cds_long_md.md)]

Om te beginnen met [!INCLUDE[prod_short](includes/cds_long_md.md)] hebt u een Microsoft Power Apps-account nodig. Als u nog geen Power Apps-account hebt, kunt u er een gratis krijgen door te gaan naar [powerapps.com](https://make.powerapps.com/?utm_source=padocs&utm_medium=linkinadoc&utm_campaign=referralsfromdoc) en de koppeling **Ga gratis aan de slag** te kiezen. Voor meer informatie over hoe u aan de slag kunt gaan met [!INCLUDE[prod_short](includes/cds_long_md.md)] gaat u naar de module [Aan de slag met Dataverse](/training/modules/get-started-with-powerapps-common-data-service/) van Microsoft-training.

## Bidirectionele of unidirectionele gegevenssynchronisatie

U kunt gegevens synchroniseren van of naar de ene Dynamics 365-bedrijfsapp naar de andere, of in beide richtingen in bijna realtime, via [!INCLUDE[prod_short](includes/cds_long_md.md)]. Als u [!INCLUDE[prod_short](includes/prod_short.md)] bijvoorbeeld met [!INCLUDE[crm_md](includes/crm_md.md)] integreert, kan een verkoper een verkooporder maken in [!INCLUDE[crm_md](includes/crm_md.md)] en de order wordt dan gesynchroniseerd met [!INCLUDE[prod_short](includes/prod_short.md)]. Omgekeerd vanuit [!INCLUDE[crm_md](includes/crm_md.md)], kan de verkoper de beschikbaarheid van het artikel in de order controleren in [!INCLUDE[prod_short](includes/prod_short.md)]. 

## Standaard- en aangepaste entiteiten

[!INCLUDE[prod_short](includes/cds_long_md.md)] slaat gegevens veilig op in een set tabellen. Dat zijn sets records die vergelijkbaar zijn met hoe een tabel gegevens opslaat in een database. [!INCLUDE[prod_short](includes/cds_long_md.md)] bevat een basisset standaardtabellen die typische scenario's dekken, maar u kunt ook aangepaste tabellen maken die specifiek zijn voor uw organisatie. In [!INCLUDE[prod_short](includes/prod_short.md)] kunt u op de pagina Toewijzingen van integratietabellen standaard- en aangepaste tabellen bekijken die worden gesynchroniseerd.

## Over de Business Central-basisintegratieoplossing

De basisintegratieoplossing is een belangrijk onderdeel van de integratie. De oplossing voegt de vereiste rollen en toegangsniveaus toe aan de gebruikersaccounts voor de integratie en maakt tabellen die nodig zijn om een [!INCLUDE[prod_short](includes/prod_short.md)]-bedrijf toe te wijzen aan een bedrijfsunit in [!INCLUDE[prod_short](includes/cds_long_md.md)]. 

Standaard importeert de begeleide instelling **[!INCLUDE[prod_short](includes/cds_long_md.md)]-verbinding instellen** de oplossing. De begeleide instelling gebruikt daarvoor een beheerdersaccount dat u opgeeft. Dit account moet ook een geldige gebruiker in [!INCLUDE[prod_short](includes/cds_long_md.md)] zijn met de beveiligingsrol **Systeembeheerder**.  

Ga naar de volgende artikelen voor meer informatie over gebruikersaccounts:

* [Gebruikersaccounts instellen voor integratie met [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md) 
* [Gebruikers maken in Microsoft Dynamics 365 (online) en beveiligingsrollen toewijzen](/dynamics365/customer-engagement/admin/create-users-assign-online-security-roles) 

Het beheerdersaccount wordt tijdens de installatie slechts één keer gebruikt voor de configuratiewijzigingen die de basisintegratieoplossing aanbrengt [!INCLUDE[prod_short](includes/cds_long_md.md)]. Nadat de oplossing is geïmporteerd, is het account niet meer nodig. Integratie gaat door met het gebruikersaccount te gebruiken dat automatisch specifiek voor de integratie is gemaakt.

Naast het aanpassen van [!INCLUDE [cds_long_md](includes/cds_long_md.md)] maakt de oplossing ook een beveiligingsrol in [!INCLUDE [cds_long_md](includes/cds_long_md.md)] voor de integratie:

* **Business Central Dataverse-integratie**: biedt u de mogelijkheid de verbinding te beheren tussen [!INCLUDE [prod_short](includes/prod_short.md)] en [!INCLUDE [cds_long_md](includes/cds_long_md.md)]. Meestal wordt deze rol alleen toegewezen aan het automatisch gemaakte gebruikersaccount voor synchronisatie. Ga voor meer informatie over deze rol naar [gebruikersaccounts instellen voor integratie met [!INCLUDE[prod_short](includes/cds_long_md.md)]](admin-setting-up-integration-with-dynamics-sales.md).

Wanneer u de verbinding instelt, maakt u de integratietabeltoewijzingen die u nodig hebt om gegevens te synchroniseren. Entiteiten in [!INCLUDE[prod_short](includes/cds_long_md.md)] worden toegewezen aan tabellen en tabelvelden in [!INCLUDE [prod_short](includes/prod_short.md)] via integratietabellen. Ga voor meer informatie over toewijzingen naar [Standaardentiteittoewijzingen voor synchronisatie](admin-synchronizing-business-central-and-sales.md#standard-table-mapping-for-synchronization).

## Omgaan met verschillen in lokale en basistransactievaluta's

U kunt verbinding maken met een [!INCLUDE[prod_short](includes/cds_long_md.md)]-omgeving die een andere basisvaluta heeft dan de lokale valuta in [!INCLUDE[prod_short](includes/prod_short.md)]. U maakt de verbinding in [!INCLUDE[prod_short](includes/prod_short.md)], op de pagina **Dataverse-verbinding instellen**, of met de begeleide instelling **Verbinding met Dataverse instellen**.

Om verbinding te kunnen maken moet u ervoor zorgen dat de valuta-instelling van basistransacties in [!INCLUDE[prod_short](includes/cds_long_md.md)] de valuta heeft die is ingesteld op de pagina **Valuta's** in [!INCLUDE [prod_short](includes/prod_short.md)] en dat er ten minste één wisselkoers gespecificeerd voor de valuta op de pagina **Valutawisselkoersen**.

Hier volgt een voorbeeld. U verbindt [!INCLUDE[prod_short](includes/cds_long_md.md)] met euro (EUR) ingesteld als de lokale valuta op de pagina **Grootboekinstellingen** met een [!INCLUDE[prod_short](includes/cds_long_md.md)]-omgeving met een basistransactievaluta ingesteld op Amerikaanse dollar (USD). U moet USD hebben op de pagina **Valuta's** in [!INCLUDE [prod_short](includes/prod_short.md)] en de juiste wisselkoers. 

Wanneer u de verbinding met [!INCLUDE[prod_short](includes/cds_long_md.md)] inschakelt, voegt [!INCLUDE [prod_short](includes/prod_short.md)] de lokale valuta toe aan de entiteit **Valuta** in [!INCLUDE[prod_short](includes/cds_long_md.md)] met de wisselkoers uit het veld **Valutafactor** op de pagina **Valutawisselkoersen**.

Valutasynchronisatie is unidirectioneel, van [!INCLUDE [prod_short](includes/prod_short.md)] naar [!INCLUDE[prod_short](includes/cds_long_md.md)]. Geldbedragen worden als volgt omgerekend en gesynchroniseerd:

* Bedragen in de [!INCLUDE[prod_short](includes/cds_long_md.md)] basisvaluta worden omgerekend naar de [!INCLUDE [prod_short](includes/prod_short.md)] lokale valuta op basis van de laatste wisselkoers die is gesynchroniseerd vanuit [!INCLUDE [prod_short](includes/prod_short.md)].
* Bedragen in de [!INCLUDE [prod_short](includes/prod_short.md)] lokale valuta worden gesynchroniseerd met de [!INCLUDE [prod_short](includes/prod_short.md)] lokale valuta in een van de andere (niet-basis) valuta's in [!INCLUDE[prod_short](includes/cds_long_md.md)].

## Wat er gebeurt als u een bedrijf kopieert

U kunt bedrijven die worden geïntegreerd met [!INCLUDE[prod_short](includes/cds_long_md.md)] of [!INCLUDE[crm_md](includes/crm_md.md)], veilig kopiëren. Het kopiëren van bedrijven helpt het risico op inconsistenties in de gegevens te verminderen en kan u kostbare tijd besparen. Ga voor meer informatie over het kopiëren van bedrijven naar [Een bedrijf kopiëren](about-new-company.md#copy-a-company).

[!INCLUDE [dataverse-copy-company](includes/dataverse-copy-company.md)]

## Zie ook

[Modellen voor gegevenseigendom](admin-cds-company-concept.md)  
<!--needs to be removed as this is moved to dev-itpro docs[Walkthrough: Customizing an Integration with Dataverse](\dynamics365\business-central\dev-itpro\administration\administration-custom-cds-integration) -->


[!INCLUDE[footer-include](includes/footer-banner.md)]
