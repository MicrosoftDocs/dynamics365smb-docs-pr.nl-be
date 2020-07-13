---
title: Administratieve taken in Business Central | Microsoft Docs
description: Sommige taken in Business Central moeten centraal worden beheerd en ingesteld. Zie om welke taken het gaat en wat u hiermee doet.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/26/2020
ms.author: sgroespe
ms.openlocfilehash: 464a1b7b06e4d656e8542655ab307ba0108425c4
ms.sourcegitcommit: 836b232d0149f9732884c9f44d53928725a8759d
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/26/2020
ms.locfileid: "3506318"
---
# <a name="administration"></a>Beheer

Centrale beheertaken worden meestal uitgevoerd door één rol in het bedrijf. De omvang van deze taken kan afhangen van de bedrijfsgrootte en de functieverantwoordelijkheden van de beheerder. Deze taken kunnen het beheer van databasesynchronisatie van verwerkings- en e-mailwachtrijen, instellen van gebruikers en aanpassen van de gebruikersinterface zijn.  

Voor het succes van nieuwe zakelijke software is het van belang dat vanaf het begin de juiste instellingswaarden worden ingevoerd. [!INCLUDE[d365fin](includes/d365fin_md.md)] bevat een aantal begeleide instellingen waarmee u hoofdgegevens kunt instellen. Zie [Business Central instellen](setup.md) voor meer informatie.

Ongeacht of u RapidStart Services gebruikt om instellingswaarden te implementeren of ze handmatig invoert in het nieuwe bedrijf, u kunt uw installatiebeslissingen ondersteunen met enkele algemene aanbevelingen voor bepaalde instellingsvelden die, als ze niet goed zijn ingesteld, de oplossing inefficiënt laten werken.  

Een supergebruiker of gebruiker kan het kader voor gegevensuitwisseling instellen zodat gebruikers gegevens in bank- en salarisbestanden kunnen importeren en exporteren. bijvoorbeeld voor verschillende processen in kasbeheer. Zie [Gegevens elektronische uitwisselen](across-data-exchange.md) voor meer informatie.

> [!NOTE]
> U kunt een nieuw bedrijf instellen in [!INCLUDE[d365fin](includes/d365fin_md.md)] met behulp van RapidStart Services, een hulpmiddel dat is ontworpen om implementatietijden te verkorten, de kwaliteit van de implementatie te verbeteren, een herhaalbare aanpak van implementaties te introduceren en de productiviteit te verbeteren door terugkerende taken te automatiseren en vereenvoudigen. Zie voor meer informatie [Een bedrijf instellen met RapidStart Services](admin-set-up-a-company-with-rapidstart.md).

De volgende tabel beschrijft een reeks taken, met koppelingen naar de onderwerpen waarin deze worden beschreven.  

|**Als u dit wilt doen**|**Zie**|  
|------------|-------------|  
|Definiëren wie zich mag aanmelden bij [!INCLUDE[d365fin](includes/d365fin_md.md)] door gebruikers te maken in het Microsoft 365-beheercentrum volgens de productlicenties.|[Gebruikers maken volgens licenties](ui-how-users-permissions.md)|
|Machtigingen toewijzen aan gebruikers, machtigingssets wijzigen en gebruikers groeperen voor eenvoudig machtigingsbeheer.|[Machtigingen toewijzen aan gebruikers en groepen](ui-how-users-permissions.md)|
|Gebruikers toevoegen, machtigingen en de toegang tot gegevens beheren en rollen toewijzen.|[Profielen beheren](admin-users-profiles-roles.md)|
|Beheer gebruikersinstellingen, zoals bedrijf, rol, taal, regio en tijdzone.|[Gebruikersinstellingen](admin-manage-user-settings-preferences.md)|
|Stel printers in en geef op welke rapporten op welke printers moeten worden afgedrukt.|[Printers instellen](ui-specify-printer-selection-reports.md)|
|Gegevensgevoeligheden classificeren voor velden, zodat u kunt reageren op aanvragen van gegevensonderwerpen met betrekking tot hun persoonlijke gegevens.|[Gegevensvertrouwelijkheid classificeren](admin-classifying-data-sensitivity.md)|
|Reageren op aanvragen van gegevensobjecten met betrekking tot hun persoonlijke gegevens.|[Reageren op aanvragen over persoonlijke gegevens](admin-responding-to-requests-about-personal-data.md)|
|Een nieuwe bedrijfsunit instellen op basis van sjablonen|[Nieuwe bedrijven maken](about-new-company.md)|
|Alle rechtstreekse wijzigingen bijhouden die gebruikers aanbrengen in databasegegevens, zodat de herkomst van fouten en wijzigingen in gegevens kan worden vastgesteld.|[Wijzigingen registreren](across-log-changes.md)|  
|Eenmalige of periodieke verzoeken voor het uitvoeren van rapporten of code-units invoeren.|[Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md)|  
|Documenten beheren, verwijderen of comprimeren|[Documenten verwijderen](admin-manage-documents.md)|  
|Stel pagina's, code-units en query's open als webservices.|[Een webservice publiceren](across-how-publish-web-service.md)|
|In het kader van het maken van Connect Apps tussen [!INCLUDE[d365fin](includes/d365fin_md.md)] en oplossingen van andere fabrikanten via REST API's, definieert u sjablonen die worden gebruikt om lege eigenschappen in een entiteit te vullen wanneer u een POST-actie maakt via een API.|[API-sjablonen configureren](admin-configuring-api-template.md)|
|Versleutel gegevens op de [!INCLUDE[d365fin](includes/d365fin_md.md)]-server door nieuwe coderingssleutels te genereren of bestaande sleutels te importeren die u op de server inschakelt.|[Gegevensversleuteling beheren](admin-manage-data-encryption.md)|
|Verbind Dynamics 365 Sales met [!INCLUDE[d365fin](includes/d365fin_md.md)] om naadloze integratie te krijgen tussen klantrelaties en orderverwerking in het potentiële klant-naar-contanten proces.|[Integreren met Dynamics 365 Sales](admin-prepare-dynamics-365-for-sales-for-integration.md)|
|Aanpassen welke velden en acties worden weergegeven in de gebruikersinterface, zodat deze bij de bedrijfsprocessen van uw bedrijf passen en de oplossing uitbreiden met apps.|[Aanpassen [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)|
|Controleer het gebruik en probleemoplossingssessies.|[Omgevingstelemetrie in het Business Central-beheercentrum](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-telemetry)|
|Beheer gebruikerssessies, inclusief het annuleren van een sessie als de gebruiker is geblokkeerd.|[Sessies beheren](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments#managing-sessions)|  

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/paths/deploy-configure-dynamics-365-business-central/)

## <a name="see-also"></a>Zie ook

[Bedrijfsfunctionaliteit](across-business-functionality.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Aan de slag](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
