---
title: Extensies installeren en verwijderen
description: Hier krijgt u meer informatie over het installeren en verwijderen van extensies in Business Central.
author: SusanneWindfeldPedersen
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: app, add-in, manifest, customize, install, uninstall
ms.search.form: 2500
ms.date: 05/24/2022
ms.author: solsen
ms.openlocfilehash: a70ea442ffb9d6e5f131e4d720da57f033474e16
ms.sourcegitcommit: 6eeac924d8e211080316ce5068e3d4fb5a2d5ed9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 05/25/2022
ms.locfileid: "8804668"
---
# <a name="install-and-uninstall-extensions-in-business-central"></a>Extensies installeren en verwijderen in Business Central

U kunt [!INCLUDE[prod_short](includes/prod_short.md)] wijzigen door extensies te installeren die bijvoorbeeld functionaliteit toevoegen, gedrag wijzigen of u toegang verlenen tot nieuwe online services. Zie [Business Central aanpassen met extensies](ui-extensions.md) voor meer informatie.

> [!NOTE]
> Als u extensies wilt installeren of verwijderen vanuit AppSource of extensies per tenant wilt toevoegen, moet u de juiste machtigingen hebben. U moet ofwel lid zijn van de gebruikersgroep UITGEBREID BEHEER - - BEHEERDER of u moet de machtigingenset UITGEBR. BEHEER - - BEHEERDER hebben. Als u een beheerder bent, kunt u gebruikersgroepen en machtigingen toewijzen aan andere gebruikers in uw bedrijf.
>
> Als u de functionaliteit van een extensie wilt gebruiken, zoals pagina's openen, rapporten uitvoeren, acties selecteren, enzovoort, moeten aan u de machtigingensets zijn toegewezen die als onderdeel van de extensie zijn geïnstalleerd.

> [!NOTE]  
> De machtigingenset **UITGEBREID BEHEER - BEHEERDER** is geïntroduceerd in Business Central 2021 releasewave 1, als vervanging voor de machtigingenset **D365 EXTENSIEBEHEER** in eerdere versies.

## <a name="install-an-extension"></a><a name="install"></a>Een extensie installeren

U beheert de extensies op de pagina **Extensiebeheer**. U kunt tot deze pagina toegang krijgen via de startpagina. Of kies het pictogram **Pagina of rapport zoeken** ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") in de rechterbovenhoek, voer **Extensie** in en kies vervolgens de gerelateerde koppeling.  

U kunt nieuwe extensies verkrijgen via de marktplaats op [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). Hier kunt u alle beschikbare extensies voor [!INCLUDE[prod_short](includes/prod_short.md)] bekijken en kunt u apps, extensies en inhoudpakketten voor andere Microsoft-producten verkrijgen. Stel de gewenste filters in, bekijk de gegevens voor elke extensie en haal een extensie voor uw [!INCLUDE[prod_short](includes/prod_short.md)] op.  

> [!NOTE]  
> Meld u bij [AppSourceAppSource.microsoft.com](https://appsource.microsoft.com/) aan met het e-mailaccount dat u gebruikt voor [!INCLUDE[prod_short](includes/prod_short.md)]. Gebruik voor het gemak dezelfde e-mailaccount voor andere producten en services.  

U kunt ook naar de marktplaats gaan vanuit [!INCLUDE[prod_short](includes/prod_short.md)]. Op de pagina **Extensiebeheer** kunt u de extensies bekijken die momenteel zijn geïnstalleerd en kunt u de pagina **Extensiemarktplaats** openen waarop de extensies van [!INCLUDE[prod_short](includes/prod_short.md)] worden weergegeven die momenteel beschikbaar zijn in AppSource. Als u de koppeling *Meer apps* kiest, komt u terecht op [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).  

Als u een extensie kiest, kunt u lezen over wat de extensie doet en kunt u Help opvragen voor de extensie voor meer informatie. Wanneer u een extensie wilt verkrijgen, moet u akkoord gaan met de gebruiksvoorwaarden. Als u de extensie van de AppSource-website ophaalt, wordt u aangemeld bij [!INCLUDE[prod_short](includes/prod_short.md)] om de installatie te voltooien.  

Wanneer u een extensie installeert, moet u deze mogelijk instellen. Zo moet u wellicht een rekening opgeven met de **extensie PayPal Payments Standard voor [!INCLUDE[prod_short](includes/prod_short.md)]**.
Met andere extensies worden gewoonweg velden aan een bestaande pagina toegevoegd of wordt bijvoorbeeld een nieuwe pagina toegevoegd.

Als u een extensie verwijdert en vervolgens van gedachten verandert, kunt u deze opnieuw installeren. Wanneer u een extensie verwijdert die u gebruikt, worden de gegevens bewaard zodat deze gegevens nog steeds beschikbaar zijn als u de extensie opnieuw installeert. Er zijn enkele extensies vereist. U kunt deze extensies niet verwijderen vanaf de pagina **Extensiebeheer**. Als u het probeert, verschijnt er een foutmelding.

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

## <a name="upload-a-per-tenant-extension-pte"></a>Een per-tenant extensie (PTE) uploaden

U uploadt een PTE met behulp van de pagina **Extensiebeheer**. Ga op de pagina **Extensiebeheer** naar **Beheren** en kies **Extensie uploaden**. Geef op de pagina **Extensie uploaden en implementeren** het .app-bestand op dat u wilt uploaden. Kies om verder te gaan de knop **Accepteren** en dan de knop **Implementeren**. Hierdoor wordt hiermee het proces van het implementeren van de PTE gestart.

Als de PTE onderbrekende schemawijzigingen bevat, is het mogelijk om een upload ervan *af te dwingen*. Om dat te doen kiest u in de **Schemasynchronisatiemodus** de optie **Afdwingen**. U krijgt een bevestigingsdialoogvenster om te accepteren voordat u verder gaat.  

## <a name="uninstall-an-extension"></a>Een extensie verwijderen

U kunt een extensie verwijderen op de pagina **Extensiebeheer**. Om een extensie te verwijderen selecteert u deze op de pagina en selecteert u vervolgens de actie **Verwijderen**. Als u een extensie verwijdert en u vervolgens van gedachten verandert, kunt u de extensie opnieuw installeren.

Wanneer u een extensie verwijdert die u hebt gebruikt, worden de gegevens standaard bewaard voor het geval dat u de extensie weer installeert. U kunt er in plaats daarvan ook voor kiezen om de gegevens samen met de extensie te verwijderen. Deze bewerking wordt beheerd door de schakelaar **Extensiegegevens verwijderen**. Standaard staat deze schakelaar **uit**. Wanneer u de schakelaar **Extensiegegevens verwijderen** probeert in te schakelen voor de extensie, krijgt u een bevestigingsvenster en moet u **Ja** kiezen om deze aan te zetten. Nadat de schakelaar **Extensiegegevens verwijderen** is ingeschakeld, kunt u de extensie verwijderen en wordt u vervolgens gevraagd opnieuw te bevestigen dat u de extensie en de gegevens wilt verwijderen.

> [!IMPORTANT]  
> - Er kunnen andere extensies zijn die afhankelijk zijn van de extensie die u wilt verwijderen om te kunnen werken. Deze andere extensies worden aangeduid als *afhankelijk*. U kunt een extensie niet verwijderen, tenzij de afhankelijke extensies ook zijn verwijderd.
> - Wanneer u ervoor kiest om een extensie te verwijderen die een of meer afhankelijke extensies heeft, krijgt u een bevestigingsvenster waarin de afhankelijke extensies worden vermeld en wordt gevraagd of u de extensie en alle afhankelijkheden wilt verwijderen. U moet **Ja** selecteren om door te gaan.
> - Als u de schakelaar **Extensiegegevens verwijderen** aan zet, verwijdert u met het verwijderen van de extensie **ook** alle gegevens voor alle afhankelijke extensies. De actie kan niet ongedaan worden gemaakt.
> - Sommige extensies zijn vereist. U kunt deze niet verwijderen vanaf de pagina **Extensiebeheer**. Als u het probeert, verschijnt er een foutmelding.  

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