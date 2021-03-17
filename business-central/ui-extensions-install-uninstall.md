---
title: Extensies installeren en verwijderen in Business Central | Microsoft Docs
description: Hier krijgt u meer informatie over het installeren en verwijderen van extensies in Business Central.
documentationcenter: ''
author: SusanneWindfeldPedersen
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize, install, uninstall
ms.date: 10/01/2020
ms.author: solsen
ms.openlocfilehash: e0bb0f88fd9b8dd4c4bcf853447009e0b898fd7a
ms.sourcegitcommit: a9d48272ce61e5d512a30417412b5363e56abf30
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5493315"
---
# <a name="installing-and-uninstalling-extensions-in-business-central"></a>Extensies installeren en verwijderen in Business Central

U kunt [!INCLUDE[prod_short](includes/prod_short.md)] wijzigen door extensies te installeren die bijvoorbeeld functionaliteit toevoegen, gedrag wijzigen of u toegang verlenen tot nieuwe online services. Zie [Business Central aanpassen met extensies](ui-extensions.md) voor meer informatie.

> [!NOTE]
> Als u extensies wilt installeren vanuit AppSource of extensies per tenant wilt toevoegen, moet u de juiste machtigingen hebben. U moet lid zijn van de gebruikersgroep D365 EXTENSIEBEHEER of u moet beschikken over de machtigingenset D365 EXTENSIEBEHEER. Als u een beheerder bent, kunt u gebruikersgroepen en machtigingen toewijzen aan andere gebruikers in uw bedrijf.
>
> Als u de functionaliteit van een extensie wilt gebruiken, zoals pagina's openen, rapporten uitvoeren, acties selecteren, enzovoort, moeten aan u de machtigingensets zijn toegewezen die als onderdeel van de extensie zijn geïnstalleerd.

## <a name="installing-an-extension"></a>Een extensie installeren

U beheert de extensies op de pagina **Extensiebeheer**. U kunt tot deze pagina toegang krijgen via de startpagina. Of kies het pictogram **Zoeken naar pagina of rapport** ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen") in de rechterbovenhoek, voer **Extensie** in en kies vervolgens de gerelateerde koppeling.  

U kunt nieuwe extensies verkrijgen via de marktplaats op [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). Hier kunt u alle beschikbare extensies voor [!INCLUDE[prod_short](includes/prod_short.md)] bekijken en kunt u apps, extensies en inhoudpakketten voor andere Microsoft-producten verkrijgen. Stel de gewenste filters in, bekijk de gegevens voor elke extensie en haal een extensie voor uw [!INCLUDE[prod_short](includes/prod_short.md)] op.  

> [!NOTE]  
> Meld u bij [AppSourceAppSource.microsoft.com](https://appsource.microsoft.com/) aan met het e-mailaccount dat u gebruikt voor [!INCLUDE[prod_short](includes/prod_short.md)]. Gebruik voor het gemak dezelfde e-mailaccount voor andere producten en services.  

U kunt ook naar de marktplaats gaan vanuit [!INCLUDE[prod_short](includes/prod_short.md)]. Op de pagina **Extensiebeheer** kunt u de extensies bekijken die momenteel zijn geïnstalleerd en kunt u de pagina **Extensiemarktplaats** openen waarop de extensies van [!INCLUDE[prod_short](includes/prod_short.md)] worden weergegeven die momenteel beschikbaar zijn in AppSource. Als u de koppeling *Meer apps* kiest, komt u terecht op [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).  

Als u een extensie kiest, kunt u lezen over wat de extensie doet en kunt u Help opvragen voor de extensie voor meer informatie. Wanneer u een extensie wilt verkrijgen, moet u akkoord gaan met de gebruiksvoorwaarden. Als u de extensie van de AppSource-website ophaalt, wordt u aangemeld bij [!INCLUDE[prod_short](includes/prod_short.md)] om de installatie uit te voeren.  

Wanneer u een extensie installeert, moet u deze mogelijk instellen. Zo moet u wellicht een rekening opgeven met de **extensie PayPal Payments Standard voor [!INCLUDE[prod_short](includes/prod_short.md)]**.
Met andere extensies worden gewoonweg velden aan een bestaande pagina toegevoegd of wordt bijvoorbeeld een nieuwe pagina toegevoegd.

Als u een extensie verwijdert en vervolgens van gedachten verandert, kunt u deze opnieuw installeren. Wanneer u een extensie verwijdert die u gebruikt, worden de gegevens bewaard zodat deze gegevens nog steeds beschikbaar zijn als u de extensie opnieuw installeert. Er zijn enkele extensies vereist. U kunt deze niet verwijderen vanaf de pagina **Extensiebeheer**. Als u het probeert, verschijnt er een foutmelding.

Sommige extensies worden verstrekt door Microsoft en andere extensies worden verstrekt door [andere bedrijven](ui-extensions-other.md). Alle extensies worden getest voordat ze voor u beschikbaar worden gemaakt, maar het is raadzaam dat u toegang hebt tot de koppelingen die met elke extensie worden verschaft als u meer wilt weten over de extensie voordat u ervoor kiest deze te installeren.

Microsoft biedt de volgende extensies:

* [Extensie AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)
* [Ceridian Payroll](ui-extensions-ceridian-payroll.md)
* [Bedrijfshub](ui-extensions-company-hub.md)  
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
* [Btw-groep](ui-extensions-vat-group.md)
* [WorldPay Payments Standard](ui-extensions-worldpay-payments-standard.md)
* [DK - C5 Gegevensmigratie](ui-extensions-c5-data-migration.md)
* [DK - Betalingen en afstemmingen](ui-extensions-payments-reconciliation-formats-dk.md)
* [DK - Btw-bestandsindelingen](ui-extensions-tax-file-formats-dk.md)
* [De extensie GetAddress.io UK Postcodes](LocalFunctionality/UnitedKingdom/ui-extensions-getaddressio.md)  
* [VS/CA/VK/AU/NZ/ZA - Overschrijvingsadvies verzenden](ui-extensions-send-remittance-advice.md)

## <a name="uninstalling-an-extension"></a>Een extensie verwijderen

U kunt een extensie verwijderen op de pagina **Extensiebeheer**. Als u een extensie verwijdert en u vervolgens van gedachten verandert, kunt u de extensie opnieuw installeren. Wanneer u een extensie verwijdert die u hebt gebruikt, worden de gegevens standaard bewaard zodat deze gegevens nog steeds beschikbaar zijn als u de extensie opnieuw installeert. U kunt er in plaats daarvan ook voor kiezen om de gegevens samen met de extensie te verwijderen. Dit kunt u opgeven door het selectievakje **Extensiegegevens verwijderen** in of uit te schakelen. Dit selectievakje is standaard *uitgeschakeld*.

> [!IMPORTANT]  
> Als u het selectievakje **Extensiegegevens verwijderen** inschakelt, wordt er een bevestigingsvenster weergegeven en moet u **OK** kiezen. Als het selectievakje **Extensiegegevens verwijderen** is ingeschakeld, kunt u nu de extensie verwijderen en wordt u vervolgens gevraagd opnieuw te bevestigen dat u de extensie wilt verwijderen en dat u de gegevens wilt verwijderen. De actie kan niet ongedaan worden gemaakt.
Sommige extensies zijn vereist. U kunt deze niet verwijderen vanaf de pagina **Extensiebeheer**. Als u het probeert, verschijnt er een foutmelding.  

## <a name="see-also"></a>Zie ook

[Business Central aanpassen](ui-customizing-overview.md)  
[Business Central-extensies van andere providers](ui-extensions-other.md)  
[De Envestnet Yodlee Bank Feeds-service instellen](bank-how-setup-bank-statement-service.md)  
[Klantbetalingen inschakelen via PayPal](sales-how-enable-payment-service-extensions.md)  
[Bedrijfsgegevens migreren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[De extensie GetAddress.io UK Postcode instellen](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] Extensies door andere providers](ui-extensions-other.md)  
[Aan de slag](product-get-started.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]