---
title: Extensies installeren om Business Central aan te passen
description: Meer informatie over het toevoegen van functionaliteit en het aanpassen van Business Central door extensies te installeren vindt u hier.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: app, add-in, manifest, customize
ms.date: 06/23/2021
ms.author: edupont
ms.openlocfilehash: 073b89f7c80035da12f329f752b64dc8142f309d
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/30/2021
ms.locfileid: "6325596"
---
# <a name="customizing-business-central-online-using-extensions"></a>Business Central Online aanpassen met extensies

U kunt [!INCLUDE[prod_short](includes/prod_short.md)] online wijzigen door extensies te installeren die bijvoorbeeld functionaliteit toevoegen, gedrag wijzigen of u toegang verlenen tot nieuwe online services.

> [!NOTE]
> Als u extensies wilt installeren vanuit AppSource extensies per tenant wilt toevoegen, moet u de juiste machtigingen hebben. U moet lid zijn van de gebruikersgroep D365 EXTENSIEBEHEER of u moet beschikken over de machtigingenset D365 EXTENSIEBEHEER. Als u een beheerder bent, kunt u gebruikersgroepen en machtigingen toewijzen aan andere gebruikers in uw bedrijf.

Als u de functionaliteit van een extensie wilt gebruiken, zoals pagina's openen, rapporten uitvoeren, acties selecteren, enzovoort, moeten aan u de machtigingensets zijn toegewezen die als onderdeel van de extensie zijn geïnstalleerd.

> [!IMPORTANT]  
> Het uploaden van extensies per huurder en de installatie van AppSource-extensies wordt niet ondersteund via de pagina **Extensiebeheer** voor lokale installaties. U kunt AppSource-extensies niet on-premises installeren, inclusief in op Docker gebaseerde implementaties.

Wanneer u [!INCLUDE[prod_short](includes/prod_short.md)] voor het eerst start, zijn bepaalde extensies al voor u geïnstalleerd. In de loop van de tijd zullen meer extensies beschikbaar voor u worden gemaakt en u kunt dan zelf bepalen of u de extensie wilt gebruiken of niet.

Zo verschaft Microsoft een extensie die integratie met PayPal Payments Standard biedt. Deze extensie is standaard geïnstalleerd.
Maar als er een andere extensie beschikbaar komt die integratie met een andere betalingsservice biedt, kunt u de nieuwe extensie installeren en vervolgens bepalen welke van de services moeten worden gebruikt.  

U beheert de extensies op de pagina **Extensiebeheer**. U kunt tot deze pagina toegang krijgen via de startpagina. Of kies het pictogram **Zoeken naar pagina of rapport** ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen") in de rechterbovenhoek, voer **Extensie** in en kies vervolgens de gerelateerde koppeling. Zie [Extensies installeren en verwijderen](ui-extensions-install-uninstall.md) voor meer informatie.

> [!NOTE]  
> Als u denkt u dat toegang tot een extensie zou moeten hebben maar de functionaliteit ervan niet vindt, kijk dan op de pagina **Extensiebeheer**. Als de extensie daar niet wordt vermeld, kunt u de extensie installeren zoals beschreven in het volgende gedeelte.  

> [!NOTE]  
> Meld u aan bij [AppSourceAppSource.microsoft.com](https://appsource.microsoft.com/) met het e-mailaccount dat u gebruikt voor [!INCLUDE[prod_short](includes/prod_short.md)] online. Gebruik voor het gemak dezelfde e-mailaccount voor andere producten en services.  

U kunt ook naar de marktplaats gaan vanuit [!INCLUDE[prod_short](includes/prod_short.md)]. Op de pagina **Extensiebeheer** kunt u de extensies bekijken die momenteel zijn geïnstalleerd en kunt u de pagina **Extensiemarktplaats** openen waarop de extensies van [!INCLUDE[prod_short](includes/prod_short.md)] worden weergegeven die momenteel beschikbaar zijn in AppSource. Als u de koppeling *Meer apps* kiest, komt u terecht op [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).  

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

> [!NOTE]  
> U kunt op de hoogte blijven van nieuwe extensies van Microsoft en andere leveranciers op [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).


## <a name="extensions-and-data-transfer"></a>Extensies en gegevensoverdracht

Aangezien de volgende extensies communiceren met andere services, kunnen ze gegevens uit de geografie van de [!INCLUDE[prod_short](includes/prod_short.md)]-omgeving overdragen:

* AMC Banking 365 Fundamentals-extensie
* Afbeeldingsanalyse
* Voorspelling van te late betaling
* PayPal Payments Standard
* Verkoop- en voorraadprognose
* WorldPay Payments Standard

Dit geldt ook voor bepaalde functionaliteit in de basistoepassing, zoals de volgende mogelijkheden:

* Cashflowprognose
* Documentuitwisselingsservice
* Dataverse-verbindingen
* OCR-service
* Online Map
* EU btw-nummers Service

## <a name="see-also"></a>Zie ook

[Business Central aanpassen](ui-customizing-overview.md)  
[Business Central-extensies van andere providers](ui-extensions-other.md)  
[De Envestnet Yodlee Bank Feeds-service instellen](bank-how-setup-bank-statement-service.md)  
[Klantbetalingen inschakelen via PayPal](sales-how-enable-payment-service-extensions.md)  
[Bedrijfsgegevens migreren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[De extensie GetAddress.io UK Postcode instellen](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] Extensies door andere providers](ui-extensions-other.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  


[!INCLUDE[footer-include](includes/footer-banner.md)]
