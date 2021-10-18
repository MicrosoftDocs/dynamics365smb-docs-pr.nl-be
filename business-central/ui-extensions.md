---
title: Extensies installeren om Business Central aan te passen
description: Meer informatie over het toevoegen van functionaliteit en het aanpassen van Business Central door extensies te installeren vindt u hier.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: app, add-in, manifest, customize
ms.date: 08/25/2021
ms.author: edupont
ms.openlocfilehash: b9a4d6b37bce0772540a307edc9c64cba1780dc5
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2021
ms.locfileid: "7587796"
---
# <a name="customizing-business-central-online-using-extensions"></a>Business Central Online aanpassen met extensies

U kunt [!INCLUDE[prod_short](includes/prod_short.md)] online wijzigen door extensies te installeren die bijvoorbeeld functionaliteit toevoegen, gedrag wijzigen of u toegang verlenen tot nieuwe online services.

> [!NOTE]
> Als u extensies wilt installeren of verwijderen vanuit AppSource of extensies per tenant wilt toevoegen, moet u de juiste machtigingen hebben. U moet ofwel lid zijn van de gebruikersgroep UITGEBREID BEHEER - - BEHEERDER of u moet de machtigingenset UITGEBR. BEHEER - - BEHEERDER hebben. Als u een beheerder bent, kunt u gebruikersgroepen en machtigingen toewijzen aan andere gebruikers in uw bedrijf.
>
> Als u de functionaliteit van een extensie wilt gebruiken, zoals pagina's openen, rapporten uitvoeren, acties selecteren, enzovoort, moeten aan u de machtigingensets zijn toegewezen die als onderdeel van de extensie zijn geïnstalleerd.

> [!NOTE]  
> De machtigingenset **UITGEBREID BEHEER - BEHEERDER** is geïntroduceerd in Business Central 2021 releasewave 1, als vervanging voor de machtigingenset **D365 EXTENSIEBEHEER** in eerdere versies.

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

## <a name="recommended-apps"></a>Aanbevolen apps
Microsoft-partners en -resellers kunnen extensies maken die ze kunnen gebruiken om lijsten met apps samen te stellen die ze vaak aan hun klanten aanbevelen. Als ze dat doen en de extensie in uw tenant hebben geïmplementeerd, zijn de apps beschikbaar op de pagina **Aanbevolen apps**. Daar kunt u over elke app lezen en beslissen of u deze wilt installeren.

> [!NOTE]
> Als u een Microsoft-partner of -wederverkoper bent en u een lijst met aanbevolen apps wilt geven, gaat u naar [Apps aanbevelen uit AppSource](/dynamics365/business-central/dev-itpro/administration/recommend-apps).

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
