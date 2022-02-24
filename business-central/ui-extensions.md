---
title: Extensies installeren om Business Central aan te passen | Microsoft Docs
description: Meer informatie over het toevoegen van functionaliteit en het aanpassen van Business Central door extensies te installeren.
documentationcenter: ''
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 1cf5c08f00565bbaea914405397f340cd281fcef
ms.sourcegitcommit: 6aa830e3286729bac3cbe5e911d72a2c69d50f73
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428359"
---
# <a name="customizing-business-central-using-extensions"></a>Business Central aanpassen met extensies
U kunt [!INCLUDE[d365fin](includes/d365fin_md.md)] wijzigen door extensies te installeren die bijvoorbeeld functionaliteit toevoegen, gedrag wijzigen of u toegang verlenen tot nieuwe online services.

> [!NOTE]
> Als u extensies wilt installeren vanuit AppSource extensies per tenant wilt toevoegen, moet u de juiste machtigingen hebben. U moet lid zijn van de gebruikersgroep D365 EXTENSIEBEHEER of u moet beschikken over de machtigingenset D365 EXTENSIEBEHEER. Als u een beheerder bent, kunt u gebruikersgroepen en machtigingen toewijzen aan andere gebruikers in uw bedrijf.<br /><br />
Als u de functionaliteit van een extensie wilt gebruiken, zoals pagina's openen, rapporten uitvoeren, acties selecteren, enzovoort, moeten aan u de machtigingensets zijn toegewezen die als onderdeel van de extensie zijn geïnstalleerd.

> [!IMPORTANT]  
> Het uploaden van extensies per huurder en de installatie van AppSource-extensies wordt niet ondersteund via de pagina **Extensiebeheer** voor lokale installaties.

Wanneer u [!INCLUDE[d365fin](includes/d365fin_md.md)] voor het eerst start, zijn bepaalde extensies al voor u geïnstalleerd. In de loop van de tijd zullen meer extensies beschikbaar voor u worden gemaakt en u kunt dan zelf bepalen of u de extensie wilt gebruiken of niet.

Zo verschaft Microsoft een extensie die integratie met PayPal Payments Standard biedt. Deze extensie is standaard geïnstalleerd.
Maar als er een andere extensie beschikbaar komt die integratie met een andere betalingsservice biedt, kunt u de nieuwe extensie installeren en vervolgens bepalen welke van de services moeten worden gebruikt.  

U beheert de extensies op de pagina **Extensiebeheer**. U kunt tot deze pagina toegang krijgen via de startpagina. Of kies het pictogram **Zoeken naar pagina of rapport** ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen") in de rechterbovenhoek, voer **Extensie** in en kies vervolgens de gerelateerde koppeling.  

> [!NOTE]  
>   Als u denkt u dat toegang tot een extensie zou moeten hebben maar de functionaliteit ervan niet vindt, kijk dan op de pagina **Extensiebeheer**. Als de extensie daar niet wordt vermeld, kunt u de extensie installeren zoals beschreven in het volgende gedeelte.  

## <a name="installing-an-extension"></a>Een extensie installeren
U kunt nieuwe extensies verkrijgen via de marktplaats op [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1). Hier kunt u alle beschikbare extensies voor [!INCLUDE[d365fin](includes/d365fin_md.md)] bekijken en kunt u apps, extensies en inhoudpakketten voor andere Microsoft-producten verkrijgen. Stel de gewenste filters in, bekijk de gegevens voor elke extensie en haal een extensie voor uw [!INCLUDE[d365fin](includes/d365fin_md.md)] op.  
> [!NOTE]  
>   Meld u bij [AppSourceAppSource.microsoft.com](https://appsource.microsoft.com/) aan met het e-mailaccount dat u gebruikt voor [!INCLUDE[d365fin](includes/d365fin_md.md)]. Gebruik voor het gemak dezelfde e-mailaccount voor andere producten en services.  

U kunt ook naar de marktplaats gaan vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)]. Op de pagina **Extensiebeheer** kunt u de extensies bekijken die momenteel zijn geïnstalleerd en kunt u de pagina **Extensiemarktplaats** openen waarop de extensies van [!INCLUDE[d365fin](includes/d365fin_md.md)] worden weergegeven die momenteel beschikbaar zijn in AppSource. Als u de koppeling *Meer apps* kiest, komt u terecht op [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).  

Als u een extensie kiest, kunt u lezen over wat de extensie doet en kunt u Help opvragen voor de extensie voor meer informatie. Wanneer u een extensie wilt verkrijgen, moet u akkoord gaan met de gebruiksvoorwaarden. Als u de extensie van de AppSource-website ophaalt, wordt u aangemeld bij [!INCLUDE[d365fin](includes/d365fin_md.md)] om de installatie uit te voeren.  

Wanneer u een extensie installeert, moet u deze mogelijk instellen. Zo moet u wellicht een rekening opgeven met de **extensie PayPal Payments Standard voor [!INCLUDE[d365fin](includes/d365fin_md.md)]**.
Met andere extensies worden gewoonweg velden aan een bestaande pagina toegevoegd of wordt bijvoorbeeld een nieuwe pagina toegevoegd.   

Als u een extensie verwijdert en vervolgens van gedachten verandert, kunt u deze opnieuw installeren. Wanneer u een extensie verwijdert die u gebruikt, worden de gegevens bewaard zodat deze gegevens nog steeds beschikbaar zijn als u de extensie opnieuw installeert. Er zijn enkele extensies vereist. U kunt deze niet verwijderen vanaf de pagina **Extensiebeheer**. Als u het probeert, verschijnt er een foutmelding.  

Sommige extensies worden verstrekt door Microsoft en andere extensies worden verstrekt door [andere bedrijven](ui-extensions-other.md). Alle extensies worden getest voordat ze voor u beschikbaar worden gemaakt, maar het is raadzaam dat u toegang hebt tot de koppelingen die met elke extensie worden verschaft als u meer wilt weten over de extensie voordat u ervoor kiest deze te installeren.  

Microsoft biedt de volgende extensies:  

* [Accountantportal voor Business Central](ui-extensions-accountant-portal.md)
* [Ceridian Payroll](ui-extensions-ceridian-payroll.md)
* [Dynamics GP-gegevensmigratie](ui-extensions-dynamicsgp-data-migration.md)
* [Envestnet Yodlee Bank Feeds](ui-extensions-yodlee-bank-feeds.md)
* [Essentiële zakelijke inzichten](ui-extensions-essential-business-insights.md)
* [Afbeeldingsanalyse](ui-extensions-image-analyzer.md)
* [Intelligente cloud](ui-extensions-data-replication.md)
* [Intelligente cloud Basis](ui-extensions-intelligent-cloud.md)
* [Voorspelling van te late betalingen](ui-extensions-late-payment-prediction.md)
* [Microsoft Pay](ui-extensions-microsoft-pay-payments.md)
* [PayPal Payments Standard](ui-extensions-paypal-payments-standard.md)
* [QuickBooks-gegevensmigratie](ui-extensions-quickbooks-data-migration.md)
* [QuickBooks Online Gegevensmigratie](ui-extensions-quickbooks-online-data-migration.md)
* [Salarisbestand importeren - Quickbooks](ui-extensions-quickbooks-payroll.md)
* [Verkoop- en voorraadprognose](ui-extensions-sales-forecast.md)
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)
* [Extensie AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)
* [DK - C5 Gegevensmigratie](ui-extensions-c5-data-migration.md)
* [DK - Betalingen en afstemmingen](ui-extensions-payments-reconciliation-formats-dk.md)
* [DK - Btw-bestandsindelingen](ui-extensions-tax-file-formats-dk.md)
* [UK - GetAddress.io postcodes van het Verenigd Koninkrijk](ui-extensions-getaddressio.md)
* [VS/CA/VK/AU/NZ/ZA - Overschrijvingsadvies verzenden](ui-extensions-send-remittance-advice.md)
* [Extensies voor Business Central van andere providers](ui-extensions-other.md)

> [!NOTE]  
>  Nieuwe extensies zijn niet direct in AppSource beschikbaar nadat we een update aankondigen. U kunt de extensies in de gaten houden op [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).

## <a name="see-also"></a>Zie ook
[Dynamics 365 Business Central uitbreiden](about-develop-extensions.md)  
[Extensies voor Business Central van andere providers](ui-extensions-other.md)  
[De Envestnet Yodlee Bank Feeds-service instellen](bank-how-setup-bank-statement-service.md)  
[Klantbetalingen inschakelen via PayPal](sales-how-enable-payment-service-extensions.md)  
[Bedrijfsgegevens migreren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[De extensie GetAddress.io UK Postcode instellen](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[d365fin](includes/d365fin_md.md)] Extensies door andere providers](ui-extensions-other.md)  
[Aan de slag](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
