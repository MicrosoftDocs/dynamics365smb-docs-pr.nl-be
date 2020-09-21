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
ms.date: 08/12/2020
ms.author: edupont
ms.openlocfilehash: 2011728e8e036442418c6a2d8b51477b45b02d1e
ms.sourcegitcommit: 43284728c34b72ad1984a516273dc80e4cdc99ab
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 09/04/2020
ms.locfileid: "3765933"
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

U beheert de extensies op de pagina **Extensiebeheer**. U kunt tot deze pagina toegang krijgen via de startpagina. Of kies het pictogram **Zoeken naar pagina of rapport** ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen") in de rechterbovenhoek, voer **Extensie** in en kies vervolgens de gerelateerde koppeling. Zie [Extensies installeren en verwijderen](ui-extensions-install-uninstall.md) voor meer informatie.

> [!NOTE]  
> Als u denkt u dat toegang tot een extensie zou moeten hebben maar de functionaliteit ervan niet vindt, kijk dan op de pagina **Extensiebeheer**. Als de extensie daar niet wordt vermeld, kunt u de extensie installeren zoals beschreven in het volgende gedeelte.  

> [!NOTE]  
> Nieuwe extensies zijn niet direct in AppSource beschikbaar nadat we een update aankondigen. U kunt de extensies in de gaten houden op [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

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
