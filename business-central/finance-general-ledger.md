---
title: Het grootboek en rekeningschema begrijpen
description: Beschrijft het grootboek, het rekeningschema en rekeningcategorieën. Gebruik de pagina Grootboekinstellingen om op te geven hoe boekhoudkwesties in uw bedrijf worden afgehandeld.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.search.form: 18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158
ms.date: 01/21/2022
ms.author: edupont
ms.openlocfilehash: 1834cfe7bbbc933a1aebddbc94ea6dfe09523605
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8510884"
---
# <a name="understanding-the-general-ledger-and-the-chart-of-accounts"></a>Het grootboek en het rekeningschema

In het grootboek worden uw financiële gegevens opgeslagen en het rekeningschema bevat de rekeningen waarnaar alle grootboekposten worden geboekt. [!INCLUDE[prod_short](includes/prod_short.md)] bevat een standaardrekeningschema dat gereed is voor ondersteuning van uw bedrijf.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Grootboekinstellingen en algemene boekingsinstellingen

De instelling van het grootboek bevindt zich in de kern van financiële processen omdat hiermee wordt bepaald hoe u gegevens boekt. Twee pagina's spelen een belangrijke rol bij het configureren van uw financiële processen:  

* De pagina **Boekhoudinstellingen**

    Op de pagina **Grootboekinstellingen** geeft u op hoe bepaalde boekhoudkwesties in uw bedrijf worden afgehandeld, zoals:  

    * Factuurafrondingsdetails  
    * Adresindelingen  
    * Financiële rapportage  

    > [!TIP]
    > De pagina **Grootboekinstellingen** bevat algemene velden en velden die specifiek zijn voor uw land of regio. Als u niet zeker bent van de betekenis van een veld, raden we u aan om samen met uw accountant te bepalen of dit relevant is voor uw organisatie. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

    Open de pagina [hier](https://businesscentral.dynamics.com/?page=118)
* De pagina **Boekingsgroepinstellingen**

    Op de pagina **Boekingsgroepinstelling** geeft u op dezelfde manier op hoe u combinaties van algemene bedrijfsgroepen en algemene productboekingsgroepen wilt instellen. Met boekingsgroepen worden entiteiten zoals klanten, leveranciers, artikelen, resources en verkoop- en inkoopdocumenten aan grootboekrekeningen gekoppeld. U vult een regel in voor elke combinatie van bedrijfs- en productboekingsgroep. Maar u kunt ook elke regel openen in een eigen instellingskaart voor boekingen. Zie [Boekingsgroepinstellingen](finance-posting-groups.md) voor meer informatie.  

    > [!TIP]
    > Als u de velden die u zoekt, niet ziet op de pagina **Boekingsgroepinstellingen**, gebruikt u de horizontale schuifbalk onder aan de pagina om naar rechts te schuiven.  

    Open de pagina [hier](https://businesscentral.dynamics.com/?page=314)

## <a name="the-chart-of-accounts"></a>Het rekeningschema

In het rekeningschema worden alle grootboekrekeningen weergegeven. In het rekeningschema kunt u onder andere het volgende doen:  

* Rapporten weergeven waarin grootboekposten en saldi worden weergegeven.  
* Sluit uw resultatenrekening.  
* Open de grootboekrekeningkaart om instellingen toe te voegen of te wijzigen.  
* Bekijk een lijst met boekingsgroepen waarmee naar die rekening wordt geboekt.
* Afzonderlijke debet- en creditsaldo's voor één rekening bekijken  

U kunt grootboekrekeningen toevoegen, wijzigen of verwijderen. Om verschillen te voorkomen, kunt u echter geen grootboekrekening verwijderen als deze gegevens worden gebruikt in het rekeningschema. Vanaf releasewave 2 van 2022 kunt u ook het per ongeluk verwijderen van accounts in gevoelige perioden blokkeren. Zie [Rekeningen verwijderen](finance-setup-chart-accounts.md#delete-accounts) voor meer informatie.  

## <a name="account-categories"></a>Rekeningcategorieën

U kunt de structuur van uw financiële overzichten personaliseren door grootboekrekeningen toe te wijzen aan rekeningcategorieën.  

De pagina **GB-rekeningcategorieën** toont uw categorieën en subcategorieën en de grootboekrekeningen die eraan zijn toegewezen. U kunt nieuwe subcategorieën maken en die categorieën toewijzen aan bestaande rekeningen.  

U maakt een categoriegroep door andere subcategorieën onder een regel te laten inspringen op de pagina **GB-rekeningcategorieën**. Zo wordt het gemakkelijk voor u om een overzicht te krijgen, omdat elke groepering een totaalsaldo weergeeft. U kunt bijvoorbeeld subcategorieën maken voor verschillende soorten activa en vervolgens categoriegroepen maken voor vaste activa versus huidige activa.  

U kunt opgeven of de rekeningen in elke subcategorie moeten worden opgenomen in bepaalde soorten rapporten. De rekeningcategorieën helpen de indeling te definiëren van uw financiële overzichten.  

### <a name="example"></a>Voorbeeld

Het standaardsaldo-overzicht heeft bijvoorbeeld één subcategorie voor *Kas* onder *Huidige activa*. U wilt dat het saldo-overzicht rekening houdt met kleingeld en cheques, dus onderneemt u de volgende stappen:  

1. Voeg twee nieuwe subcategorieën toe:

    * Een voor kleingeld  
    * Een voor uw betaalrekening  
2. Geef de andere rapportdefinitie **Kasrekeningen** voor deze subcategorieën op.  
3. Laat ze inspringen onder de subcategorie **Kas**.  

De volgende keer dat u rapportageschema's genereert, bevat uw saldo-overzicht een totaalsaldo voor kas en twee regels met saldi voor kleine kas en de betaalrekening.  

## <a name="get-a-quick-overview"></a>Een snel overzicht krijgen

Op de pagina **Rekeningschema** worden rekeningen weergegeven in een hiërarchische lijst die snelle toegang biedt tot de belangrijkste informatie voor elke rekening. De lijst is echter statisch en als u veel accounts hebt, moet u misschien een beetje bladeren om informatie voor verschillende accounts te bekijken. Als u gewoon een snel overzicht wilt van de basisprincipes, zoals nettowijzigingen en saldi, is de pagina **Overzicht van rekeningschema** een handig alternatief. De kolomindeling op de pagina is nu hetzelfde als op de pagina **Rekeningschema** (er zijn er alleen minder), dus u hoeft zich niet te heroriënteren en u kunt de hiërarchische niveaus uitvouwen of samenvouwen om de weergave te condenseren. Om het schakelen tussen de pagina's gemakkelijk te maken is de pagina **Overzicht van rekeningschema** beschikbaar op de pagina **Rekeningschema**.

## <a name="access-to-create-and-edit-accounts-and-account-categories"></a>Toegang om accounts en accountcategorieën te maken en te bewerken

In een kleine organisatie, zoals het CRONUS-demonstratiebedrijf, kunnen de meeste gebruikers het rekeningschema bewerken, behalve gebruikers met een TEAMLID-licentie. In grotere organisaties wordt de toegang om het rekeningschema te bewerken echter beperkt door rollen en machtigingen. Als u een beheerder bent of de rol *Bedrijfsmanager* of *Accountant* hebt, kunt u de machtigingen voor alle gebruikers controleren om er zeker van te zijn dat de juiste mensen toegang hebben tot de relevante tabellen. Zie voor meer informatie [Een overzicht krijgen van de machtigingen van een gebruiker](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).  

## <a name="see-also"></a>Zie ook

[Financiën](finance.md)  
[De rekeningschema's instellen of wijzigen](finance-setup-chart-accounts.md)  
[Bedrijfsinformatie](bi.md)  
[Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
