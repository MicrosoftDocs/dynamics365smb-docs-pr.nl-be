---
title: Het rekeningschema begrijpen
description: 'Beschrijft het rekeningschema, hoe u het instelt en hoe u het gebruikt.'
author: kennienp
ms.topic: conceptual
ms.search.keywords: 'analysis, history, track'
ms.search.form: '18, 20, 37, 65, 99, 312, 314, 313, 395, 552, 569, 570, 634, 790, 791, 1158'
ms.date: 04/17/2024
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics-365-business-central
---

# <a name="understanding-the-chart-of-accounts"></a>Het rekeningschema begrijpen

Een rekeningschema dient als een uitgebreid register van financiële rekeningen en de bijbehorende referentienummers. Een rekeningschema heeft doorgaans twee hoofdcategorieën rekeningen:

- Balansrekeningen: deze rekeningen volgen de activa, schulden en nettowaarde van uw bedrijf.
- Resultatenrekeningen: deze rekeningen registreren inkomsten uit verschillende bronnen en houden ook uitgaven bij.

Balansrekeningen worden verder onderverdeeld in drie groepen:

1. Activarekeningen: deze rekeningen volgen alle waardevolle bronnen die eigendom zijn van uw bedrijf.
1. Aansprakelijkheidsrekeningen: ze registreren de schulden van uw bedrijf.
1. Vermogensrekeningen: vertegenwoordigen de restwaarde in het bedrijf na aftrek van de verplichtingen van activa.

Inkomstenrekeningen zijn onderverdeeld in twee groepen:

1. Inkomstenrekeningen: deze rekeningen registreren de inkomsten van uw bedrijf uit verschillende bronnen.
1. Onkostenrekeningen: deze rekeningen omvatten alle uitgaven van uw bedrijf.

Gebruik het rekeningschema om transacties vast te leggen in het grootboek van uw organisatie. Elke rekening heeft doorgaans een id (rekeningnummer) en een beschrijvend bijschrift of koptekst, en ze worden systematisch gecodeerd op basis van hun rekeningtype.

[!INCLUDE[prod_short](includes/prod_short.md)] bevat een standaardrekeningschema dat gereed is voor ondersteuning van uw bedrijf.

De samenstelling van het rekeningschema van uw bedrijf is een strategische beslissing die door uw management wordt genomen (of door landspecifieke regelgeving). Het varieert afhankelijk van de sector, het bedrijfsmodel en de financiële structuur van uw bedrijf. Afhankelijk van uw branche heeft u bijvoorbeeld mogelijk specifieke activarekeningen die zijn afgestemd op de unieke activiteiten en behoeften van uw bedrijf:

* Een detailhandelsbedrijf kan de nadruk leggen op voorraad en debiteuren.
* Een technologiebedrijf kan zich richten op immateriële activa zoals patenten en software.
* Een fabriek zou vaste activa en voorraden volgen.

## <a name="the-chart-of-accounts-page"></a>De pagina Rekeningschema

In het rekeningschema worden alle grootboekrekeningen weergegeven. In het rekeningschema kunt u onder andere het volgende doen:  

* Rapporten weergeven waarin grootboekposten en saldi worden weergegeven.  
* Sluit uw resultatenrekening.  
* De grootboekrekeningkaart openen, waar u instellingen kunt toevoegen of wijzigen.  
* Bekijk een lijst met boekingsgroepen voor die rekening.
* Afzonderlijke debet- en creditsaldo's voor één rekening bekijken.

U kunt grootboekrekeningen toevoegen, wijzigen of verwijderen. Om verschillen te voorkomen, kunt u echter geen grootboekrekening verwijderen als deze gegevens worden gebruikt in het rekeningschema. U kunt ook de abusievelijke verwijdering van rekeningen in gevoelige periodes voorkomen. Ga voor meer informatie over het beschermen van rekeningen tegen verwijdering naar [Rekeningen verwijderen](finance-setup-chart-accounts.md#delete-accounts).  

## <a name="the-code-hierarchy-in-gl-accounts"></a>De codehiërarchie in grootboekrekeningen

Bedrijven creëren doorgaans een hiërarchische structuur in grootboekrekeningcodes om weer te geven waar ze thuishoren in het rekeningschema. In sommige implementaties geven grootboekrekeningcodes die beginnen met **1**, bijvoorbeeld activarekeningen aan, terwijl grootboekrekeningcodes die met 3 beginnen, vermogensrekeningen aanduiden. In sommige regio's gelden lokale voorschriften voor het gebruik van een standaardrekeningschema. Om gebruikers te helpen deze hiërarchie te begrijpen zonder dat ze de interne codestructuur hoeven te kennen, kunt u in uw rekeningschema kopteksten en subtotalen definiëren die deze interne structuren samenvatten.

## <a name="designing-your-chart-of-accounts"></a>Uw rekeningschema ontwerpen

Elke regel in het rekeningschema is een grootboekrekening van een van de volgende typen:

* Boeking (dagboeken kunnen regels naar deze rekeningen boeken)
* Kop (definieert een algemene kop in het rekeningschema)
* Totaal (definieert een formule voor een subtotaal in het rekeningschema)
* Begintotaal (definieert een beginkop voor een subtotaal in het rekeningschema. Alle volgende regels tot een eindtotaalregel zijn ingesprongen
* Eindtotaal (definieert een eindkop voor een subtotaal en de formule daarvoor in het rekeningschema. Alle volgende regels na deze eindtotaalregel zijn uitgesprongen)

Een minimalistisch rekeningschema kan alleen uit regels met boekingsrekeningen bestaan. De andere vier typen gebruikt u om te definiëren hoe het rekeningschema ook een financieel overzicht met kopteksten en subtotalen weergeeft. Totaalrekeningen worden vaak gebruikt in financiële rapportage.

> [!TIP]
> Als u in uw rekeningschema andere rekeningtypen gebruikt dan **Boeking**, kunt u verschillende weergaven definiëren om de 'onbewerkte' boekingsrekeningen weer te geven zonder de rapportagetyperekeningtypen voor de totaaltelling en koppen. Bijvoorbeeld Alleen boekingsrekeningen weergeven en Geblokkeerde rekeningen verbergen.

## <a name="use-dimensions-to-simplify-your-chart-of-accounts"></a>Dimensies gebruiken om uw rekeningschema te vereenvoudigen

Dimensies zijn waarden waarmee posten worden gecategoriseerd, zodat u ze kunt bijhouden en analyseren in documenten, zoals verkooporders. Dimensies kunnen bijvoorbeeld aangeven tot welk project of welke afdeling een post behoort. Dus in plaats van voor elke afdeling en project aparte grootboekrekeningen in te stellen, kunt u bijvoorbeeld dimensies gebruiken als basis voor analyse en hoeft u geen ingewikkeld rekeningschema te maken.

Ga voor meer informatie over dimensies naar [Werken met dimensies](finance-dimensions.md).

## <a name="get-a-quick-overview-of-your-finances"></a>Snel een overzicht krijgen van uw financiën

Op de pagina **Rekeningschema** worden rekeningen weergegeven in een hiërarchische lijst die snelle toegang biedt tot de belangrijkste informatie voor elke rekening. De lijst is echter statisch en als u veel rekeningen hebt, moet u misschien een beetje scrollen om informatie voor verschillende rekeningen te bekijken. Als u gewoon een snel overzicht wilt van de basisprincipes, zoals nettowijzigingen en saldi, is de pagina **Overzicht van rekeningschema** een handig alternatief. De kolomindeling op de pagina is hetzelfde als op de pagina **Rekeningschema** (hoewel met minder kolommen), dus het is gemakkelijk te begrijpen. U kunt de hiërarchische niveaus uitvouwen of samenvouwen. Om het schakelen tussen de pagina's gemakkelijk te maken is de pagina **Overzicht van rekeningschema** beschikbaar op de pagina **Rekeningschema**.

## <a name="access-to-create-and-edit-the-chart-of-accounts"></a>Toegang om het rekeningschema te maken en te bewerken

In een kleine organisatie, zoals het CRONUS-voorbeeldbedrijf, kunnen de meeste gebruikers het rekeningschema bewerken, behalve gebruikers met een TEAMLID-licentie. In grotere organisaties worden meestal rollen en machtigingen gebruikt om toegang tot het bewerken van de rekeningschema's te beperken. Als u een beheerder bent of de rol Bedrijfsmanager of Accountant hebt, kunt u de machtigingen bepalen om er zeker van te zijn dat de juiste mensen toegang hebben tot de relevante tabellen. Ga voor meer informatie naar [Een overzicht krijgen van de machtigingen van een gebruiker](ui-define-granular-permissions.md#get-an-overview-of-a-users-permissions).  


<!-- ## Standard chart of accounts in different regions
Uncomment when we have more examples added to our localization documentation

Some regions have defined standards for the chart of accounts structure you should use in your company. 

Here are some examples of such standards that have been implemented in localized versions of [!INCLUDE[prod_short](includes/prod_short.md)]:

* [Standard chart of accounts in Denmark](localfunctionality/denmark/how-to-set-up-standard-coa.md)
-->

## <a name="chart-of-accounts-best-practices"></a>Best practices voor rekeningschema's

Hier volgen enkele best practices waarmee u rekening kunt houden bij het ontwikkelen en onderhouden van uw rekeningschema's:

* Stel het rekeningschema van uw bedrijf samen om de financiële rapportagebehoeften van uw management te ondersteunen bij het nemen van strategische beslissingen.
* Overweeg eenvoudig te beginnen met minder grootboekrekeningen. Indien nodig kunt u altijd meer gedetailleerde rekeningen toevoegen.
* Definieer kopteksten en subtotalen in uw rekeningschema die de interne structuren in grootboekrekeningen samenvatten.
* Gebruik dimensies om uw rekeningschema te vereenvoudigen. Heb geen specifieke grootboekrekeningen voor elk product of elke afdeling.
* Voeg nieuwe grootboekrekeningen toe zodra ze binnenkomen, maar verwijder rekeningen alleen uit uw rekeningschema aan het einde van uw financiële periode.

## <a name="see-also"></a>Zie ook

[De rekeningschema's instellen of wijzigen](finance-setup-chart-accounts.md)  
[Het grootboek begrijpen](finance-general-ledger.md)
[Financiële analyse](bi.md)  
[Overzicht van financiën](finance.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
