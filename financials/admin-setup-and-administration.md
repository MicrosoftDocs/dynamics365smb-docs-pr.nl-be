---
title: Beheertaken in Dynamics 365 | Microsoft Docs
description: Sommige taken in [!INCLUDE[d365fin](includes/d365fin_md.md)] moeten centraal worden beheerd en ingesteld. Zie om welke taken het gaat en wat u hiermee doet.
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 09c3460a50088098bfe5c2fb633e76dccbac0794
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="setup-and-administration-in-dynamics-365-for-financials"></a>Installatie en beheer in Dynamics 365 for Financials
Centrale beheertaken worden meestal uitgevoerd door één rol in het bedrijf. De omvang van deze taken kan afhangen van de bedrijfsgrootte en de functieverantwoordelijkheden van de beheerder. Deze taken kunnen het beheer van databasesynchronisatie van verwerkings- en e-mailwachtrijen, instellen van gebruikers, aanpassen van de gebruikersinterface en het beheer van encryptiesleutels zijn.  

Voor het succes van nieuwe zakelijke software is het van belang dat vanaf het begin de juiste instellingswaarden worden ingevoerd. [!INCLUDE[d365fin](includes/d365fin_md.md)] bevat een aantal begeleide instellingen waarmee u hoofdgegevens kunt instellen. Zie [Dynamics 365 for Financials instellen](setup.md) voor meer informatie.

<!--Whether you use [!INCLUDE[rim](../../includes/rim_md.md)] to implement setup values or you manually enter them in the new company, you can support your setup decisions with some general recommendations for selected setup fields that are known to potentially cause the solution to be inefficient if defined incorrectly.-->  

Een supergebruiker of gebruiker kan het kader voor gegevensuitwisseling instellen zodat gebruikers gegevens in bank- en salarisbestanden kunnen importeren en exporteren. bijvoorbeeld voor verschillende processen in kasbeheer.  

In de volgende tabel wordt een reeks taken beschreven, met koppelingen naar de beschrijvende onderwerpen.   

|**Als u dit wilt doen**|**Zie**|  
|------------|-------------|  
|Gebruikers toevoegen, machtigingen en de toegang tot gegevens beheren en rollen toewijzen.|[Gebruikers, profielen en rolcentra in Dynamics 365 for Financials](admin-users-profiles-roles.md)|  
|Alle rechtstreekse wijzigingen bijhouden die gebruikers aanbrengen in databasegegevens, zodat de herkomst van fouten en wijzigingen in gegevens kan worden vastgesteld.|[Wijzigingen in Dynamics 365 for Financials registreren](across-log-changes.md)|  
|Steun uw instellingsbeslissingen met aanbevelingen voor geselecteerde velden waarvan bekend is dat ze mogelijkerwijs de oplossing inefficiënt maken wanneer ze onjuist zijn ingesteld|[Complexe toepassingsgebieden instellen met aanbevolen procedures](set-up-complex-application-areas-using-best-practices.md)|  
|Stel pagina's, code-units en query's open als webservices.|[Procedure: Een webservice publiceren](across-how-publish-web-service.md)|  
|Een SMTP-server instellen om communicatie per e-mail in en vanuit Dynamics 365 for Financials in te stellen| [Procedure: E-mail handmatig instellen of de begeleide instelling gebruiken](madeira-how-setup-email.md)|  
|Eenmalige of periodieke verzoeken voor het uitvoeren van rapporten of code-units invoeren.|[Gebruik van taakwachtrijen om taken te plannen](admin-job-queues-schedule-tasks.md)|  
|Documenten beheren, verwijderen of comprimeren|[Documenten beheren](admin-manage-documents.md)|  
|Een nieuwe bedrijfsunit instellen op basis van sjablonen|[Nieuwe bedrijven maken in [!INCLUDE[d365fin](includes/d365fin_md.md)]](about-new-company.md)|  

## <a name="see-also"></a>Zie ook
[Overzicht van bedrijffunctionaliteit](madeira-business-functionality.md)  
[Algemene bedrijfsfunctionaliteit](ui-across-business-areas.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
[Welkom bij [!INCLUDE[d365fin](includes/d365fin_md.md)]](index.md)  

