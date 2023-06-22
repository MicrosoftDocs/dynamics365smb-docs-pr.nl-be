---
title: Business Central Online aanpassen met apps
description: Meer informatie over het toevoegen van functionaliteit en het aanpassen van Business Central door apps te installeren.
author: edupont04
ms.topic: conceptual
ms.search.keywords: 'app, add-in, manifest, customize'
ms.search.form: '2500, 2502, 20350, 20353'
ms.date: 09/27/2022
ms.author: edupont
---
# <a name="customizing-business-central-online-with-apps" />Business Central Online aanpassen met apps

U kunt [!INCLUDE[prod_short](includes/prod_short.md)] online wijzigen door apps te installeren die bijvoorbeeld functionaliteit toevoegen, gedrag wijzigen of u toegang verlenen tot nieuwe online services. Deze apps worden ook wel *extensies* omdat ze [!INCLUDE [prod_short](includes/prod_short.md)] *uitbreiden*.

## <a name="manage-apps" />App beheren

[!INCLUDE [2023rw1-sec-group-short](includes/2023rw1-sec-group-short.md)]

Wanneer u [!INCLUDE[prod_short](includes/prod_short.md)] voor het eerst start, zijn bepaalde apps al voor u geïnstalleerd. In de loop van de tijd zullen meer apps beschikbaar voor u worden gemaakt en u kunt dan zelf bepalen of u de app wilt gebruiken of niet.

Zo verschaft Microsoft een app die integratie met PayPal Payments Standard biedt. Deze extensie is standaard geïnstalleerd. Maar als er een andere extensie beschikbaar komt die integratie met een andere betalingsservice biedt, kunt u de nieuwe extensie installeren en vervolgens bepalen welke van de services moeten worden gebruikt.  

Als u de functionaliteit van een app wilt gebruiken, zoals pagina's openen, rapporten uitvoeren, acties selecteren, enzovoort, moeten aan u de machtigingensets zijn toegewezen die als onderdeel van de app zijn geïnstalleerd.

Als u extensies wilt installeren of verwijderen vanuit AppSource of extensies per tenant wilt toevoegen, moet u de juiste machtigingen hebben. U moet lid zijn van de gebruikersgroep **D365 extensiebeheer** of u moet expliciet beschikken over de machtigingenset **UITGEBREID BEHEER - BEHEERDER**. Als u een beheerder bent, kunt u gebruikersgroepen en machtigingen toewijzen aan andere gebruikers in uw bedrijf. Zie [Gebruikers maken volgens licenties](ui-how-users-permissions.md) voor meer informatie.  

> [!IMPORTANT]  
> Voor [!INCLUDE [prod_short](includes/prod_short.md)] on-premises u kunt geen extensies per tenant uploaden of AppSource-apps installeren via de pagina **Extensiebeheer**. U kunt AppSource-apps niet on-premises installeren, inclusief in op Docker gebaseerde implementaties.

U beheert de apps op de pagina **Extensiebeheer**. U kunt tot deze pagina toegang krijgen via de startpagina. Of kies het pictogram **Zoeken naar pagina of rapport** ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen") in de rechterbovenhoek, voer **Extensie** in en kies vervolgens de gerelateerde koppeling. Zie [Apps installeren en verwijderen](ui-extensions-install-uninstall.md) voor meer informatie.

> [!NOTE]  
> Als u denkt u dat toegang tot een app zou moeten hebben maar de functionaliteit ervan niet vindt, kijk dan op de pagina **Extensiebeheer**. Als de app daar niet wordt vermeld, kunt u deze installeren zoals beschreven in het volgende gedeelte.  

> [!NOTE]  
> Meld u aan bij [AppSourceAppSource.microsoft.com](https://appsource.microsoft.com/) met het e-mailaccount dat u gebruikt voor [!INCLUDE[prod_short](includes/prod_short.md)] online. Gebruik voor het gemak dezelfde e-mailaccount voor andere producten en services.  

U kunt ook naar de marktplaats gaan vanuit [!INCLUDE[prod_short](includes/prod_short.md)]. Op de pagina **Extensiebeheer** kunt u de apps bekijken die momenteel zijn geïnstalleerd en kunt u de pagina **Extensiemarktplaats** openen waarop de apps van [!INCLUDE[prod_short](includes/prod_short.md)] worden weergegeven die momenteel beschikbaar zijn in AppSource. Als u de koppeling *Meer apps* kiest, komt u terecht op [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).  

Als u een app kiest, kunt u lezen over wat de app doet en kunt u Help opvragen voor de app voor meer informatie. Wanneer u een app wilt verkrijgen, moet u akkoord gaan met de gebruiksvoorwaarden. Als u de app van de AppSource-website ophaalt, wordt u aangemeld bij [!INCLUDE[prod_short](includes/prod_short.md)] om de installatie uit te voeren.  

Wanneer u een app installeert, moet u deze mogelijk instellen. Zo moet u wellicht een rekening opgeven met de **extensie PayPal Payments Standard voor [!INCLUDE[prod_short](includes/prod_short.md)]**.
Met andere apps worden gewoonweg velden aan een bestaande pagina toegevoegd of wordt bijvoorbeeld een nieuwe pagina toegevoegd.   

Als u een app verwijdert en vervolgens van gedachten verandert, kunt u deze opnieuw installeren. Wanneer u een app verwijdert die u gebruikt, worden de gegevens bewaard zodat deze gegevens nog steeds beschikbaar zijn als u de app opnieuw installeert. Er zijn enkele apps vereist. U kunt deze niet verwijderen vanaf de pagina **Extensiebeheer**. Als u het probeert, verschijnt er een foutmelding.  

Sommige apps worden verstrekt door Microsoft en andere apps worden verstrekt door [andere bedrijven](ui-extensions-other.md). Alle apps worden getest voordat ze voor u beschikbaar worden gemaakt, maar het is raadzaam dat u toegang hebt tot de koppelingen die met elke extensie worden verschaft als u meer wilt weten over de app voordat u ervoor kiest deze te installeren.  

> [!NOTE]  
> U kunt op de hoogte blijven van nieuwe apps van Microsoft en andere leveranciers op [AppSource.microsoft.com](https://appsource.microsoft.com/marketplace/apps?product=dynamics-365%3Bdynamics-365-business-central&page=1).

## <a name="apps-and-data-transfer" />Apps en gegevensoverdracht

Aangezien de volgende apps communiceren met andere services, kunnen ze gegevens uit de geografie van de [!INCLUDE[prod_short](includes/prod_short.md)]-omgeving overdragen:

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
* EU btw-nummers Onderhoud

## <a name="connect-your-business" />Uw bedrijf verbinden

Vanaf 2022 release wave 2 kunnen [!INCLUDE [prod_short](includes/prod_short.md)] online-omgevingen een of meer apps vermelden op de pagina's **Connectiviteits-apps** en **Bank-apps**. Deze apps kunnen uw bedrijf met externe services verbinden om de productiviteit te verhogen door processen te automatiseren. U kunt bijvoorbeeld verbinding maken met uw banken en automatisch banktransacties importeren. De apps zijn eenvoudig te installeren en direct vanaf deze pagina in te stellen. Kies een app voor meer informatie over mogelijkheden en prijzen.  

Bekijk de lijst met voorgestelde apps door de actie **Connectiviteits-apps** te kiezen op de pagina **Extensiebeheer**.  

> [!NOTE]
> De eerste persoon die de pagina **Connectiviteits-apps** opent, moet toestaan dat de extensie verbinding maakt met een externe service. Sta de verbinding eenmalig of altijd toe. Als u ervoor kiest om de verbinding te blokkeren, moet u de relevante apps vinden op AppSource.

Deze externe service genereert een lijst met relevante apps op basis van uw land of regio

## <a name="recommended-apps" />Aanbevolen apps

Microsoft-partners en -resellers kunnen apps maken die ze kunnen gebruiken om lijsten met apps samen te stellen die ze vaak aan hun klanten aanbevelen. Als ze dat doen en de app in uw tenant hebben geïmplementeerd, zijn de apps beschikbaar op de pagina **Aanbevolen apps**. Daar kunt u over elke app lezen en beslissen of u deze wilt installeren.

> [!NOTE]
> Als u een Microsoft-partner of -wederverkoper bent en u een lijst met aanbevolen apps wilt geven, gaat u naar [Apps aanbevelen uit AppSource](/dynamics365/business-central/dev-itpro/administration/recommend-apps) in de beheerinhoud.

## <a name="see-related-microsoft-trainingtrainingmodulescustomize-dynamics--business-central" />Zie gerelateerde [Microsoft-training](/training/modules/customize-dynamics-365-business-central/)

## <a name="see-also" />Zie ook

[Apps installeren en verwijderen](ui-extensions-install-uninstall.md)  
[Business Central aanpassen](ui-customizing-overview.md)  
[Business Central-apps van andere providers](ui-extensions-other.md)  
[De Envestnet Yodlee Bank Feeds-service instellen](bank-how-setup-bank-statement-service.md)  
[Klantbetalingen via betalingsservices inschakelen](sales-how-enable-payment-service-extensions.md)  
[Bedrijfsgegevens migreren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[De extensie GetAddress.io UK Postcode instellen](LocalFunctionality/UnitedKingdom/uk-setup-postal-code-service.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)]-apps door andere providers](ui-extensions-other.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  

## <a name="includeprodshortincludesfreetrialmdmd" />[!INCLUDE[prod_short](includes/free_trial_md.md)]


[!INCLUDE[footer-include](includes/footer-banner.md)]
