---
title: Het grootboek en het rekeningschema begrijpen
description: 'Beschrijft het grootboek, het rekeningschema en rekeningcategorieën. Gebruik de pagina Grootboekinstellingen om op te geven hoe boekhoudkwesties in uw bedrijf worden afgehandeld.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'analysis, history, track'
ms.search.form: '18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158'
ms.date: 04/19/2024
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# <a name="understanding-the-general-ledger-and-chart-of-accounts"></a>Het grootboek en het rekeningschema begrijpen

In het grootboek (GB) worden uw financiële gegevens opgeslagen en het rekeningschema bevat de rekeningen waarnaar u grootboekposten boekt. [!INCLUDE[prod_short](includes/prod_short.md)] bevat een standaardrekeningschema dat gereed is voor ondersteuning van uw bedrijf.

## <a name="general-ledger-setup-and-general-posting-setup"></a>Grootboekinstellingen en algemene boekingsinstellingen

De instelling van het grootboek bevindt zich in de kern van financiële processen omdat hiermee wordt bepaald hoe u gegevens boekt. Twee pagina's spelen in het bijzonder een belangrijke rol bij het configureren van uw financiële processen:  

* **Boekhoudinstellingen**
* **Boekingsgroepinstellingen**

### <a name="the-general-ledger-setup-page"></a>De pagina **Boekhoudinstellingen**

Gebruik de pagina **Grootboekinstellingen** om op te geven hoe bepaalde boekhoudkwesties in uw bedrijf worden afgehandeld, zoals:  

* Factuurafrondingsdetails  
* Adresindelingen  
* Financiële rapportage

> [!TIP]
> De pagina **Grootboekinstellingen** bevat algemene velden en velden die specifiek zijn voor uw land/regio. Als u niet zeker bent van de betekenis van een veld, raden we u aan om samen met uw accountant te bepalen of dit relevant is voor uw organisatie. [!INCLUDE [tooltip-inline-tip_md](includes/tooltip-inline-tip_md.md)]  

Om de pagina nu te openen, gebruikt u de volgende link [Grootboekinstellingen](https://businesscentral.dynamics.com/?page=118).

### <a name="the-general-posting-setup-page"></a>De pagina **Boekingsgroepinstellingen**

Gebruik de pagina **Boekingsgroepinstellingen** om combinaties van algemene bedrijfs- en productboekingsgroepen in te stellen. Met boekingsgroepen worden entiteiten zoals klanten, leveranciers, artikelen, resources en verkoop- en inkoopdocumenten aan grootboekrekeningen gekoppeld. U vult een regel in voor elke combinatie van bedrijfs- en productboekingsgroep. Maar u kunt ook elke regel openen in een eigen instellingskaart voor boekingen. Zie voor meer informatie [Instellingen voor boekingsgroepen](finance-posting-groups.md).  

> [!TIP]
> Als u de velden die u zoekt niet ziet op de pagina **Boekingsgroepinstellingen**, gebruikt u de horizontale schuifbalk onder aan de pagina om naar rechts te schuiven.  

Om de pagina nu te openen, gebruikt u de volgende link [Boekingsgroepinstellingen](https://businesscentral.dynamics.com/?page=314).

## <a name="the-chart-of-accounts"></a>Het rekeningschema

Op de pagina **Rekeningschema** worden alle grootboekrekeningen weergegeven. In het rekeningschema kunt u onder andere het volgende doen:  

* Rapporten weergeven waarin grootboekposten en saldi worden weergegeven.  
* Sluit uw resultatenrekening.  
* Open de grootboekrekeningkaart om instellingen toe te voegen of te wijzigen.  
* Bekijk een lijst met boekingsgroepen voor die rekening.
* Afzonderlijke debet- en creditsaldo's voor één rekening bekijken.

Ga voor meer informatie naar [Het rekeningschema begrijpen](finance-chart-of-accounts.md).

## <a name="account-categories"></a>Rekeningcategorieën

U kunt de structuur van uw financiële overzichten personaliseren door grootboekrekeningen toe te wijzen aan rekeningcategorieën.  

De pagina **GB-rekeningcategorieën** toont uw categorieën en subcategorieën en de grootboekrekeningen die eraan zijn toegewezen. U kunt nieuwe subcategorieën maken en die categorieën toewijzen aan bestaande rekeningen.  

U kunt een categoriegroep maken door andere subcategorieën onder een regel te laten inspringen op de pagina **GB-rekeningcategorieën**. Categoriegroepen maken het gemakkelijk voor u om een overzicht te krijgen, omdat elke groepering een totaalsaldo weergeeft. U kunt bijvoorbeeld subcategorieën maken voor verschillende soorten activa en vervolgens categoriegroepen maken voor vaste activa versus huidige activa.  

U kunt definiëren of specifieke soorten lijsten de rekeningen in elke subcategorie moeten bevatten. De rekeningcategorieën helpen de indeling te definiëren van uw financiële overzichten.  

### <a name="example"></a>Voorbeeld

Het standaardsaldo-overzicht heeft bijvoorbeeld één subcategorie voor *Kas* onder *Huidige activa*. Als u wilt dat het saldo-overzicht rekening houdt met kleingeld en cheques, voert u de volgende stappen uit:

1. Kies het pictogram ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **GB-rekeningcategorieën** in en kies vervolgens de gerelateerde koppeling.
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

Wanneer u kiest voor de actie **Financiële rapporten genereren**, of de volgende keer dat het rapport wordt gegenereerd, toont uw saldo-overzicht de volgende regels:

* Totaal saldo voor contant geld.
* Regels met saldi voor kleingeld en de betaalrekening.  

> [!NOTE]
> Als u een grootboekrekening maakt zonder een rekeningcategorie toe te wijzen en u de rekening toewijst aan een boekingsgroep, wijst [!INCLUDE[prod_short](includes/prod_short.md)] automatisch de rekeningcategorie toe van de grootboekrekening direct boven de rekening in uw rekeningschema. Om de nieuwe rekening in uw financiële rapporten op te nemen, moet u echter de actie **Financiële rapporten genereren** kiezen op de pagina **GB-rekeningcategorieën**. U kunt ook de pagina Grootboekrekening openen, de rekeningcategorie specificeren en vervolgens uw financiële rapport opnieuw genereren.

## <a name="access-to-create-and-edit-gl-accounts-and-account-categories"></a>Toegang om GB-rekeningen en rekeningcategorieën te maken en te bewerken

In een kleine organisatie, zoals het CRONUS-demonstratiebedrijf, kunnen de meeste gebruikers financiële entiteiten bewerken, zoals grootboekrekeningen, rekeningcategorieën en het rekeningschema, behalve gebruikers met een TEAM MEMBER-licentie. In grotere organisaties worden meestal rollen en machtigingen gebruikt om toegang tot het bewerken van deze entiteiten te beperken. Als u een beheerder bent of de rol *Bedrijfsmanager* of *Accountant* hebt, kunt u de machtigingen bepalen om er zeker van te zijn dat de juiste mensen toegang hebben tot de relevante tabellen. Ga voor meer informatie naar [Een overzicht krijgen van de machtigingen van een gebruiker](ui-define-granular-permissions.md#get-an-overview-of-a-users-permissions).  

## <a name="use-dimensions-to-simplify-your-chart-of-accounts"></a>Dimensies gebruiken om uw rekeningschema te vereenvoudigen

Dimensies zijn waarden waarmee posten worden gecategoriseerd, zodat u ze kunt bijhouden en analyseren in documenten, zoals verkooporders. Dimensies kunnen bijvoorbeeld aangeven tot welk project of welke afdeling een post behoort. Dus in plaats van voor elke afdeling en project aparte grootboekrekeningen in te stellen, kunt u bijvoorbeeld dimensies gebruiken als basis voor analyse en hoeft u geen ingewikkeld rekeningschema te maken.

Ga voor meer informatie over dimensies naar [Standaarddimensies voor klanten, leveranciers en andere accounts instellen](finance-dimensions.md#to-set-up-default-dimensions-for-customers-vendors-and-other-accounts).

## <a name="see-also"></a>Zie ook

[Het rekeningschema begrijpen](finance-chart-of-accounts.md)  
[Werken met dimensies](finance-dimensions.md)  
[Machtigingen toewijzen aan gebruikers en groepen](ui-define-granular-permissions.md)  
[Bedrijfsinformatie](bi.md)  
[Financiën](finance.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
