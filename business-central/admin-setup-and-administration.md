---
title: Beheertaken in Business Central
description: Sommige taken in Business Central moeten centraal worden beheerd en ingesteld. Zie om welke taken het gaat en wat u hiermee doet.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.date: 01/11/2023
ms.custom: bap-template
---
# <a name="administration-tasks"></a><a name="administration-tasks"></a>Beheertaken

Centrale beheertaken worden meestal uitgevoerd door één rol in het bedrijf. De omvang van deze taken kan afhangen van de bedrijfsgrootte en de functieverantwoordelijkheden van de beheerder. Deze taken kunnen het beheer van databasesynchronisatie van verwerkings- en e-mailwachtrijen, instellen van gebruikers en aanpassen van de gebruikersinterface zijn.  

Voor het succes van nieuwe zakelijke software is het van belang dat vanaf het begin de juiste instellingswaarden worden ingevoerd. [!INCLUDE[prod_short](includes/prod_short.md)] bevat een aantal begeleide instellingen waarmee u hoofdgegevens kunt instellen. Zie [Business Central instellen](setup.md) voor meer informatie.

> [!NOTE]
> U kunt de hulpprogramma's voor gegevensmigratie gebruiken om bestaande gegevens te migreren naar [!INCLUDE [prod_short](includes/prod_short.md)] online. U kunt ook een nieuw bedrijf instellen in [!INCLUDE[prod_short](includes/prod_short.md)] met behulp van configuratiepakketten om implementatietijden te verkorten, de kwaliteit van de implementatie te verbeteren, een herhaalbare aanpak van implementaties te introduceren en de productiviteit te verbeteren door terugkerende taken te automatiseren en vereenvoudigen. Zie [On-premises gegevens migreren naar Business Central Online](/dynamics365/business-central/dev-itpro/administration/migrate-data) voor meer informatie.

U kunt uw instellingsbeslissingen ondersteunen met enkele algemene aanbevelingen voor geselecteerde instellingsvelden waarvan bekend is dat ze mogelijkerwijs de oplossing inefficiënt maken wanneer ze onjuist zijn ingesteld.  

Een supergebruiker of gebruiker kan het kader voor gegevensuitwisseling instellen zodat gebruikers gegevens in bank- en salarisbestanden kunnen importeren en exporteren. bijvoorbeeld voor verschillende processen in kasbeheer. Zie [Gegevens elektronische uitwisselen](across-data-exchange.md) voor meer informatie.

De volgende tabel beschrijft een reeks taken, met koppelingen naar de artikelen waarin deze worden beschreven.  

|**Als u dit wilt doen**|**Zie**|  
|------------|-------------|
|Definiëren wie zich mag aanmelden bij [!INCLUDE[prod_short](includes/prod_short.md)] door gebruikers te maken in het Microsoft 365-beheercentrum volgens de productlicenties.|[Gebruikers maken volgens licenties](ui-how-users-permissions.md)|
|Machtigingen toewijzen aan gebruikers, machtigingssets wijzigen en gebruikers groeperen voor eenvoudig machtigingsbeheer.|[Machtigingen toewijzen aan gebruikers en groepen](ui-how-users-permissions.md)|
|Gebruikers toevoegen, machtigingen en de toegang tot gegevens beheren en rollen toewijzen.|[Profielen beheren](admin-users-profiles-roles.md)|
|Beheer gebruikersinstellingen, zoals bedrijf, rol, taal, regio en tijdzone.|[Gebruikersinstellingen](admin-manage-user-settings-preferences.md)|
|Stel printers in en geef op welke rapporten op welke printers moeten worden afgedrukt.|[Printers instellen](ui-specify-printer-selection-reports.md)|
|Gegevensgevoeligheden classificeren voor velden, zodat u kunt reageren op aanvragen van gegevensonderwerpen met betrekking tot hun persoonlijke gegevens.|[Gegevensvertrouwelijkheid classificeren](admin-classifying-data-sensitivity.md)|
|Reageren op aanvragen van gegevensobjecten met betrekking tot hun persoonlijke gegevens.|[Reageren op aanvragen over persoonlijke gegevens](admin-responding-to-requests-about-personal-data.md)|
|Een nieuwe bedrijfsunit instellen op basis van sjablonen|[Nieuwe bedrijven maken](about-new-company.md)|
|Alle rechtstreekse wijzigingen bijhouden die gebruikers aanbrengen in databasegegevens, zodat de herkomst van fouten en wijzigingen in gegevens kan worden vastgesteld.|[Wijzigingen registreren](across-log-changes.md)|  
|Eenmalige of periodieke verzoeken voor het uitvoeren van rapporten of code-units invoeren.|[Taakwachtrijen gebruiken om taken te plannen](admin-job-queues-schedule-tasks.md)|  
|Documenten beheren, verwijderen of comprimeren|[Documenten verwijderen](admin-manage-documents.md)|  
|Stel pagina's, code-units en query's open als webservices.|[Een webservice publiceren](across-how-publish-web-service.md)|
|In het kader van het maken van Connect Apps tussen [!INCLUDE[prod_short](includes/prod_short.md)] en oplossingen van andere fabrikanten via REST API's, definieert u sjablonen die worden gebruikt om lege eigenschappen in een entiteit te vullen wanneer u een POST-actie maakt via een API.|[API-sjablonen configureren](admin-configuring-api-template.md)|
|Versleutel gegevens op de [!INCLUDE[prod_short](includes/prod_short.md)]-server door nieuwe coderingssleutels te genereren of bestaande sleutels te importeren die u op de server inschakelt.|[Gegevensversleuteling beheren](admin-manage-data-encryption.md)|
|Verbind Dynamics 365 Sales met [!INCLUDE[prod_short](includes/prod_short.md)] om naadloze integratie te krijgen tussen klantrelaties en orderverwerking in het potentiële klant-naar-contanten proces.|[Integreren met Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)|
|Aanpassen welke velden en acties worden weergegeven in de gebruikersinterface, zodat deze bij de bedrijfsprocessen van uw bedrijf passen en de oplossing uitbreiden met apps.|[[!INCLUDE[prod_short](includes/prod_short.md)]](ui-customizing-overview.md) aanpassen|

## <a name="administration-in-the-admin-center"></a><a name="administration-in-the-admin-center"></a>Beheer in het beheercentrum

Interne en gedelegeerde beheerders hebben toegang tot het [!INCLUDE [prod_short](includes/prod_short.md)]-beheercentrum, waar ze [!INCLUDE [prod_short](includes/prod_short.md)]-omgevingen kunnen configureren, bewaken en er problemen mee kunnen oplossen. De volgende tabel beschrijft enkele van de taken, met koppelingen naar de artikelen waarin deze worden beschreven.  

|**Als u dit wilt doen**|**Zie**|  
|------------|-------------|
|Lees meer over de tools die voor u beschikbaar zijn om u te helpen bij het oplossen van problemen.|[Technische ondersteuning](/dynamics365/business-central/dev-itpro/technical-support)|
|Gebruik bewaken en problemen met sessies oplossen|[Omgevingstelemetrie in het Business Central-beheercentrum](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-telemetry)|
|Beheer gebruikerssessies, inclusief het annuleren van een sessie als de gebruiker is geblokkeerd.|[Sessies beheren](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-manage-sessions)|
|Configureer de tenant om telemetriegegevens naar Azure Application Insights te verzenden voor een betere analyse en probleemoplossing.|[Verzenden van telemetrie inschakelen naar Application Insights](/dynamics365/business-central/dev-itpro/administration/telemetry-enable-application-insights)|

## <a name="see-related-microsoft-training"></a><a name="see-related-microsoft-training"></a>Zie gerelateerde [Microsoft-training](/training/paths/deploy-configure-dynamics-365-business-central/)

## <a name="see-also"></a><a name="see-also"></a>Zie ook

[Bedrijfsfunctionaliteit](across-business-functionality.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
