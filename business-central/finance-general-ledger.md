---
title: Het grootboek en rekeningschema begrijpen
description: 'Beschrijft het grootboek, het rekeningschema en rekeningcategorieën. Gebruik de pagina Grootboekinstellingen om op te geven hoe boekhoudkwesties in uw bedrijf worden afgehandeld.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'analysis, history, track'
ms.search.form: '18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158'
ms.date: 08/24/2022
ms.author: bholtorf
---
# Het grootboek en het rekeningschema begrijpen

In het grootboek (GB) worden uw financiële gegevens opgeslagen en het rekeningschema (COA) bevat de rekeningen waarnaar alle grootboekposten worden geboekt. [!INCLUDE[prod_short](includes/prod_short.md)] bevat een standaardrekeningschema dat gereed is voor ondersteuning van uw bedrijf.

## Grootboekinstellingen en algemene boekingsinstellingen

De instelling van het grootboek bevindt zich in de kern van financiële processen omdat hiermee wordt bepaald hoe u gegevens boekt. Twee pagina's spelen in het bijzonder een belangrijke rol bij het configureren van uw financiële processen:  

* De pagina **Boekhoudinstellingen**

  Op de pagina **Grootboekinstellingen** geeft u op hoe bepaalde boekhoudkwesties in uw bedrijf worden afgehandeld, zoals:  

  * Factuurafrondingsdetails  
  * Adresindelingen  
  * Financiële rapportage

  > [!TIP]
  > De pagina **Grootboekinstellingen** bevat algemene velden en velden die specifiek zijn voor uw land/regio. Als u niet zeker bent van de betekenis van een veld, raden we u aan om samen met uw accountant te bepalen of dit relevant is voor uw organisatie. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

  Open de pagina [hier](https://businesscentral.dynamics.com/?page=118).
  
* De pagina **Boekingsgroepinstellingen**

  Op de pagina **Boekingsgroepinstelling** geeft u op dezelfde manier op hoe u combinaties van algemene bedrijfsgroepen en algemene productboekingsgroepen wilt instellen. Met boekingsgroepen worden entiteiten zoals klanten, leveranciers, artikelen, resources en verkoop- en inkoopdocumenten aan grootboekrekeningen gekoppeld. U vult een regel in voor elke combinatie van bedrijfs- en productboekingsgroep. Maar u kunt ook elke regel openen in een eigen instellingskaart voor boekingen. Zie voor meer informatie [Instellingen voor boekingsgroepen](finance-posting-groups.md).  

  > [!TIP]
  > Als u de velden die u zoekt niet ziet op de pagina **Boekingsgroepinstellingen**, gebruikt u de horizontale schuifbalk onder aan de pagina om naar rechts te schuiven.  

  Open de pagina [hier](https://businesscentral.dynamics.com/?page=314).

## Het rekeningschema

In het rekeningschema worden alle grootboekrekeningen weergegeven. In het rekeningschema kunt u onder andere het volgende doen:  

* Rapporten weergeven waarin grootboekposten en saldi worden weergegeven.  
* Sluit uw resultatenrekening.  
* Open de grootboekrekeningkaart om instellingen toe te voegen of te wijzigen.  
* Bekijk een lijst met boekingsgroepen voor die rekening.
* Afzonderlijke debet- en creditsaldo's voor één rekening bekijken.

U kunt grootboekrekeningen toevoegen, wijzigen of verwijderen. Om verschillen te voorkomen, kunt u echter geen grootboekrekening verwijderen als deze gegevens worden gebruikt in het rekeningschema. Vanaf releasewave 2 van 2022 kunt u ook het per ongeluk verwijderen van accounts in gevoelige perioden blokkeren. Lees meer in de sectie [Rekeningen verwijderen](finance-setup-chart-accounts.md#delete-accounts).  

## Rekeningcategorieën

U kunt de structuur van uw financiële overzichten personaliseren door grootboekrekeningen toe te wijzen aan rekeningcategorieën.  

De pagina **GB-rekeningcategorieën** toont uw categorieën en subcategorieën en de grootboekrekeningen die eraan zijn toegewezen. U kunt nieuwe subcategorieën maken en die categorieën toewijzen aan bestaande rekeningen.  

U kunt een categoriegroep maken door andere subcategorieën onder een regel te laten inspringen op de pagina **GB-rekeningcategorieën**. Categoriegroepen maken het gemakkelijk voor u om een overzicht te krijgen, omdat elke groepering een totaalsaldo weergeeft. U kunt bijvoorbeeld subcategorieën maken voor verschillende soorten activa en vervolgens categoriegroepen maken voor vaste activa versus huidige activa.  

U kunt definiëren of specifieke soorten lijsten de rekeningen in elke subcategorie moeten bevatten. De rekeningcategorieën helpen de indeling te definiëren van uw financiële overzichten.  

### Voorbeeld

Het standaardsaldo-overzicht heeft bijvoorbeeld één subcategorie voor *Kas* onder *Huidige activa*. Als u wilt dat het saldo-overzicht rekening houdt met kleine kas en betaalrekening, moet u de volgende stappen zetten:

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **GB-rekeningcategorieën** in en kies vervolgens de gerelateerde koppeling.
   1. Een andere optie is om [de pagina hier te openen](https://businesscentral.dynamics.com/?page=790).
2. Kies de actie **Lijst bewerken**.
3. Voeg twee nieuwe subcategorieën toe: een voor kleine kas en een voor uw betaalrekening:
   1. Selecteer de categorie **Vlottende activa**.
   2. Kies de actie **Nieuw**.
   3. Type de naam van de subcategorie in het veld **Omschrijving**.
   4. Selecteer in het veld **GB-rekeningen in categorie** de juiste grootboekrekening.
   5. Selecteer in het veld **Aanvullende lijstdefinitie** de optie **Kasrekeningen**.
4. Laat ze inspringen onder de subcategorie **Kas**.
   1. Selecteer de subcategorie die in stap 3 is gemaakt.
   2. Kies de actie **Inspringen**.
   3. Kies de actie **Omlaag**.
   4. Kies de **Inspringen** actie om in te springen onder de subcategorie **Contant geld**.

Wanneer u kiest voor de actie **Financiële rapporten genereren** - of de volgende keer dat het rapport wordt gegenereerd - toont uw saldo-overzicht de volgende regels:

* Totaal saldo voor contant geld.
* Regels met saldi voor kleingeld en de betaalrekening.  

> [!NOTE]
> Als u een grootboekrekening maakt zonder een rekeningcategorie toe te wijzen en u de rekening toewijst aan een boekingsgroep, wijst [!INCLUDE[prod_short](includes/prod_short.md)] automatisch de rekeningcategorie toe van de grootboekrekening direct boven de rekening in uw rekeningschema. Om de nieuwe rekening in uw financiële rapporten op te nemen, moet u echter de actie **Financiële rapporten genereren** kiezen op de pagina **GB-rekeningcategorieën**. U kunt ook de pagina grootboekrekeningkaart openen, de rekeningcategorie specificeren en vervolgens uw financiële rapport opnieuw genereren.

## Een snel overzicht krijgen

Op de pagina **Rekeningschema** worden rekeningen weergegeven in een hiërarchische lijst die snelle toegang biedt tot de belangrijkste informatie voor elke rekening. De lijst is echter statisch en als u veel rekeningen hebt, moet u misschien een beetje scrollen om informatie voor verschillende rekeningen te bekijken. Als u gewoon een snel overzicht wilt van de basisprincipes, zoals nettowijzigingen en saldi, is de pagina **Overzicht van rekeningschema** een handig alternatief. De kolomindeling op de pagina is nu hetzelfde als op de pagina **Rekeningschema** (maar met minder kolommen), zodat u zich niet hoeft te heroriënteren. U kunt de hiërarchische niveaus uitvouwen of samenvouwen om de weergave compacter te maken. Om het schakelen tussen de pagina's gemakkelijk te maken is de pagina **Overzicht van rekeningschema** beschikbaar op de pagina **Rekeningschema**.

## Toegang om accounts en accountcategorieën te maken en te bewerken

In een kleine organisatie, zoals het CRONUS-voorbeeldbedrijf, kunnen de meeste gebruikers het rekeningschema bewerken, behalve gebruikers met een TEAMLID-licentie. In grotere organisaties worden meestal rollen en machtigingen gebruikt om toegang tot het bewerken van de rekeningschema's te beperken. Als u een beheerder bent of de rol *Bedrijfsmanager* of *Accountant* hebt, kunt u de machtigingen bepalen om er zeker van te zijn dat de juiste mensen toegang hebben tot de relevante tabellen. Zie voor meer informatie de sectie [Een overzicht krijgen van de machtigingen van een gebruiker](ui-define-granular-permissions.md#to-get-an-overview-of-a-users-permissions).  

## Zie ook

[De rekeningschema's instellen of wijzigen](finance-setup-chart-accounts.md)  
[Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md)  
[Bedrijfsinformatie](bi.md)  
[Financiën](finance.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
