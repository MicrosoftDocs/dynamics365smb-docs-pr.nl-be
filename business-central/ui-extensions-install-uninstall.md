---
title: Apps installeren en verwijderen
description: Leer hoe u apps installeert en verwijdert in Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.date: 09/07/2023
ms.custom: bap-template
ms.search.keywords: 'app, add-in, manifest, customize, install, uninstall'
ms.search.form: '2500, 2514, 20350'
---

# Extensies (apps) installeren en verwijderen in Business Central

U kunt [!INCLUDE[prod_short](includes/prod_short.md)] wijzigen door apps te installeren die bijvoorbeeld functionaliteit toevoegen, gedrag wijzigen of u toegang verlenen tot nieuwe online services. Zie [Business Central aanpassen met extensies](ui-extensions.md) voor meer informatie.

> [!NOTE]
> Als u apps wilt installeren of verwijderen vanuit AppSource of apps per tenant wilt toevoegen, moet u de juiste machtigingen hebben. U moet lid zijn van de gebruikersgroep D365 Extensiebeheer of u moet de machtigingenset UITGEBREID BEHEER - - BEHEERDER hebben. Als u een beheerder bent, kunt u gebruikersgroepen en machtigingen toewijzen aan andere gebruikers in uw bedrijf. Ga voor meer informatie over gebruikersgroepen en machtigingen naar [Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md).
>
> Als u de functionaliteit van een extensie wilt gebruiken, zoals pagina's openen, rapporten uitvoeren, acties selecteren, enzovoort, moeten aan u de machtigingensets zijn toegewezen die als onderdeel van de extensie zijn geïnstalleerd.

Als u een extensie wilt gebruiken, moet u de bijbehorende machtigingensets toegewezen krijgen.

## <a name="install"></a>Een extensie installeren

U beheert apps en extensies op de pagina **Extensiebeheer**. U kunt tot deze pagina toegang krijgen via de startpagina. Of kies het pictogram **Pagina of rapport zoeken** ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer in de rechterbovenhoek **Extensie** in en kies vervolgens de gerelateerde koppeling.  

U kunt nieuwe apps verkrijgen via de marktplaats op [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646). De marktplaats biedt alle beschikbare apps voor [!INCLUDE[prod_short](includes/prod_short.md)], plus apps en inhoudspakketten voor andere Microsoft-producten. Stel de gewenste filters in, bekijk de gegevens voor elke extensie en haal een extensie voor uw [!INCLUDE[prod_short](includes/prod_short.md)] op.  

> [!NOTE]  
> Meld u bij [AppSourceAppSource.microsoft.com](https://appsource.microsoft.com/) aan met het e-mailaccount dat u gebruikt voor [!INCLUDE[prod_short](includes/prod_short.md)]. Gebruik voor het gemak dezelfde e-mailaccount voor andere producten en services.  

U kunt ook naar AppSource gaan vanuit [!INCLUDE[prod_short](includes/prod_short.md)]. Op de pagina **Extensiebeheer** kunt u de apps bekijken die momenteel zijn geïnstalleerd en kunt u de pagina **Extensiemarktplaats** openen waarop de apps van [!INCLUDE[prod_short](includes/prod_short.md)] worden weergegeven die momenteel beschikbaar zijn in AppSource. Als u de koppeling *Meer apps* kiest, komt u terecht op [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).  

Kies een app om te leren over wat deze doet en u kunt Help opvragen voor de app voor meer informatie. Wanneer u een app wilt verkrijgen, moet u akkoord gaan met de gebruiksvoorwaarden ervan. Als u de app van de AppSource-website ophaalt, wordt u aangemeld bij [!INCLUDE[prod_short](includes/prod_short.md)] om de installatie te voltooien.  

Nadat u een app hebt geïnstalleerd, moet u deze mogelijk instellen. Sommige apps vereisen dat u wat informatie verstrekt voordat u ze kunt gebruiken. Nadat u bijvoorbeeld de app **PayPal Payments Standard** hebt geïnstalleerd, moet u het e-mailadres of de verkopersaccount-id voor uw PayPal-account opgeven. Om een app in te stellen of om te zien welke informatie u nodig hebt, gaat u naar de pagina **Geïnstalleerde extensies** en kiest u de actie **Instellen**.  

Met andere apps worden gewoonweg velden aan een bestaande pagina toegevoegd of wordt bijvoorbeeld een nieuwe pagina toegevoegd.

Als u een app verwijdert en vervolgens van gedachten verandert, kunt u deze opnieuw installeren. Wanneer u een app verwijdert die u hebt gebruikt, worden uw gegevens niet verwijderd. De gegevens zijn beschikbaar als u de app opnieuw installeert.

Sommige apps worden verstrekt door Microsoft en andere apps worden verstrekt door [andere bedrijven](ui-extensions-other.md). We raden u aan om meer te weten te komen over de app voordat u ervoor kiest om deze te installeren.

Microsoft biedt de volgende apps:

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
* [VS/CA/VK/AU/NZ/ZA - Afdrachtsadvies verzenden](ui-extensions-send-remittance-advice.md)

## Een app instellen

Nadat u een app hebt geïnstalleerd, moet u deze mogelijk instellen. Bijvoorbeeld voor de app **PayPal Payments Standard voor [!INCLUDE[prod_short](includes/prod_short.md)]** moet u de PayPal-rekening opgeven die u wilt gebruiken. Als dat het geval is, vraagt [!INCLUDE[prod_short](includes/prod_short.md)] wanneer de installatie is voltooid of u de app meteen wilt instellen. Er kunnen instellingen vereist zijn om de app te laten werken, of optioneel.

Als u ervoor kiest om uw app meteen in te stellen en deze een vereiste configuratie heeft, opent [!INCLUDE[prod_short](includes/prod_short.md)] de vereiste instellingen. De instelling kan een pagina zijn waar u informatie invoert, of een begeleide instelling die u door de stappen helpt. Als u de instelling niet in één keer voltooit, kunt u de pagina **Instellingen voor _naam van app_** gebruiken, die alle instellingen voor de app weergeeft. Vereiste instellingen aangegeven door **vetgedrukte letters**.

## Een per-tenant extensie (PTE) uploaden

U uploadt een PTE met behulp van de pagina **Extensiebeheer**. Ga op de pagina **Extensiebeheer** naar **Beheren** en kies **Extensie uploaden**. Geef op de pagina **Extensie uploaden en implementeren** het .app-bestand op dat u wilt uploaden. Kies om verder te gaan de knop **Accepteren** en dan de knop **Implementeren**. Hierdoor wordt hiermee het proces van het implementeren van de PTE gestart.

Als de PTE onderbrekende schemawijzigingen bevat, is het mogelijk om een upload ervan *af te dwingen*. Om dat te doen kiest u bij **Schemasynchronisatiemodus** de optie **Afdwingen**. U krijgt een bevestigingsdialoogvenster om te accepteren voordat u verder gaat.  

## Een app verwijderen

U kunt een app verwijderen op de pagina **Extensiebeheer**. Om een app te verwijderen selecteert u deze op de pagina en selecteert u vervolgens de actie **Verwijderen**. Als u een app verwijdert en u vervolgens van gedachten verandert, kunt u de app opnieuw installeren.

Wanneer u een app verwijdert die u hebt gebruikt, worden uw gegevens standaard niet verwijderd. Als u zeker weet dat u de app niet opnieuw zult installeren, kunt u de gegevens verwijderen wanneer u de app verwijdert. Als u gegevens wilt verwijderen wanneer u een app verwijdert, schakelt u de schakelaar **Extensiegegevens verwijderen** in. U krijgt een bevestigingsvenster en je moet **Ja** kiezen om het in te schakelen. Nadat de schakelaar **Extensiegegevens verwijderen** is ingeschakeld, kunt u de app verwijderen en wordt u vervolgens gevraagd opnieuw te bevestigen dat u de app en de gegevens wilt verwijderen.

> [!IMPORTANT]  
> * Er kunnen andere apps zijn die afhankelijk zijn van de app die u wilt verwijderen om te kunnen werken. Deze andere apps worden aangeduid als *afhankelijk*. U kunt een app niet verwijderen, tenzij u ook de afhankelijke apps verwijdert. Wanneer u een app met afhankelijke apps verwijdert, wordt een dialoogvenster weergegeven met de afhankelijke apps. Om door te gaan, moet u **Ja** selecteren om de app en de afhankelijke apps te verwijderen.
> * Als u de schakelaar **Extensiegegevens verwijderen** aanzet, verwijdert u met de app alle gegevens voor de app en *ook* gegevens voor alle afhankelijke apps. De actie kan niet ongedaan worden gemaakt.
> * Sommige apps zijn vereist en u kunt ze niet verwijderen op de pagina **Extensiebeheer**.  

Als u de gegevens van een verwijderde app wilt behouden, kunt u de gegevens later verwijderen. Op de pagina **Extensiegegevens verwijderen waarnaar niet wordt verwezen** wordt een lijst weergegeven van de apps waarvoor u nog gegevens heeft. Als u de gegevens wilt verwijderen, kiest u de app en kiest u vervolgens **Gegevens verwijderen**. 

## Zie ook

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
