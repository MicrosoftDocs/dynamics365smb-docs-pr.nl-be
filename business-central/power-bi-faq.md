---
title: Veelgestelde vragen over Power BI
description: Krijg antwoorden op enkele veelvoorkomende vragen over het werken met Power BI en Business Central.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Power BI, reports, faq, errors
ms.date: 04/22/2021
ms.author: jswymer
ms.openlocfilehash: 939b280e631113d3196f6fbbc90d9bf19b9fc408
ms.sourcegitcommit: a76475f124e79440a5bba20577b335c4d50a2d83
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025845"
---
# <a name="power-bi--faq"></a>Veelgestelde vragen over Power BI

In dit artikel worden enkele van de vragen beantwoord die u mogelijk hebt over het werken met Power BI en [!INCLUDE [prod_short](includes/prod_short.md)].

## <a name="general"></a>[Alge&meen](#tab/general)
<!-- 26 -->
### <a name="ive-selected-a-report-for-my-role-center-in-business-central-if-i-later-make-changes-to-the-reports-visuals-online-will-the-role-center-automatically-update-to-my-changes"></a>Ik heb een rapport geselecteerd voor mijn rolcentrum in Business Central. Wordt het rolcentrum automatisch bijgewerkt met mijn wijzigingen als ik later online wijzigingen aanbreng in de visuals van het rapport?

Ja, de rapporten zijn ingesloten vanuit Power BI.

<!-- 3 -->
### <a name="are-the-business-central-apps-for-power-bi-available-in-languages-other-than-english"></a>Zijn de Business Central-apps voor Power BI beschikbaar in andere talen dan het Engels?

Nee. Deze apps zijn momenteel alleen beschikbaar in het Engels.

<!-- 24 -->
### <a name="once-a-report-is-published-on-mypowerbicomworkspace-can-i-download-its-pbix"></a>Kan ik de pbix downloaden zodra een rapport is gepubliceerd op mijn powerbi.com-werkruimte? 

Ja. Zie voor meer informatie [Een rapport van de Power BI-service naar Power BI Desktop downloaden](/power-bi/create-reports/service-export-to-pbix).  

<!-- 27 -->
### <a name="can-i-download-the-apps-as-pbix-files"></a>Kan ik de apps downloaden als pbix-bestanden? 

Nee. Momenteel bieden we geen downloadbare pbix-bestanden voor de officiële Power BI-apps omdat ze worden gepubliceerd op AppSource.

## <a name="license"></a>[Licentie](#tab/license)

<!-- 14 -->
### <a name="do-i-need-a-power-bi-pro-license-to-publish-reports"></a>Heb ik een Power BI Pro-licentie nodig om rapporten te publiceren? 

<!-- todo What does " or for every user that consults the published report" mean? fixed -->
Nee. Een Pro-licentie is niet nodig om rapporten te publiceren. De (gratis) standaardlicentie voor Power BI volstaat. Zie [Power BI-licenties](admin-powerbi-setup.md#license) voor meer informatie.

<!-- 15 -->
### <a name="is-there-anything-i-cant-do-with-the-free-license"></a>Is er iets dat ik niet kan doen met de gratis licentie?

U kunt geen rapporten delen of de Business Central-apps voor Power BI installeren. Verder kunt u met de gratis licentie bijna alle variaties van grafieken en rapporten maken.

<!-- 16 -->
### <a name="if-someone-shares-a-report-with-another-person-then-that-person-needs-a-pro-license-to-see-the-report-are-there-plans-to-make-this-capability-possible-with-the-free-license"></a>Als iemand een rapport met een andere persoon deelt, heeft die persoon een Pro-licentie nodig om het rapport te zien. Zijn er plannen om deze mogelijkheid mogelijk te maken met de gratis licentie?

We hebben geen controle over deze vereiste. Deze vereiste wordt gesteld door Power BI. Zie voor meer informatie [Power BI-dashboards en -rapporten met collega's en anderen delen](/power-bi/collaborate-share/service-share-dashboards).  

## <a name="designer"></a>[Ontwerper](#tab/designer)

<!-- 7 -->
### <a name="does-the-connector-work-with-api-pages"></a>Werkt de connector met API-pagina's?

Nog niet. Maar vanaf juni 2021 ondersteunt de nieuwe Power BI-connector zowel Business Central-webservices als API-pagina's. Zie voor meer informatie [Power BI-connector inschakelen om te werken met Business Central-API's in plaats van alleen met webservices](/dynamics365-release-plan/2021wave1/smb/dynamics365-business-central/enable-power-bi-connector-work-business-central-apis-instead-web-services-only).

<!-- 11 --> 
### <a name="is-it-possible-to-choose-which-business-central-environment-to-get-data-from-for-power-bi-for-example-like-a-sandbox-or-production-environment"></a>Is het mogelijk om te kiezen uit welke Business Central-omgeving de gegevens moeten worden opgehaald voor Power BI, bijvoorbeeld een sandbox- of productieomgeving? 

Ja. Dit kan gemakkelijk. Wanneer u via de connector verbinding maakt met Business Central, moet u de omgeving en de bedrijfsnaam kiezen.

<!-- 6 --> 
### <a name="can-i-merge-data-from-several-production-environments-of-the-same-tenant"></a>Kan ik gegevens uit verschillende productieomgevingen van dezelfde tenant samenvoegen?

Ja. Voer in Power BI de bewerking Gegevens ophalen opnieuw uit en kies de gewenste omgeving.

<!-- 25 -->
### <a name="which-pages-in-business-central-have-the-power-bi-report-part"></a>Welke pagina's in Business Central bieden het Power BI-rapportonderdeel?  

Momenteel zijn er enkele geselecteerde pagina's met een feitenblok met een onderdeel **Power BI-rapporten** voor het weergeven van een rapport. 

Op lijstpagina's wordt het onderdeel **Power BI-rapporten** gefilterd om rapporten weer te geven die betrekking hebben op gegevens in de lijst. Dit zijn de lijsttypepagina's die het onderdeel **Power BI-rapporten** bevatten:

|Pagina-id|Name|
|-------|----|
|22|Klantenoverzicht|
|27|Leveranciersoverzicht|
|31|Artikeloverzicht|
|9305|Verkooporderoverzicht|
|9308|Inkoopfacturen|

Hier zijn andere pagina's die het grotere, niet-gefilterde onderdeel **Power BI-rapporten** bevatten:

|Pagina-id|Name|
|-------|----|
|1156|Bedrijfsdetails|
|4013|Intelligente cloud-inzichten |
|9006|Orderverwerker Rolcentrum|
|9008|Magazijninventarisatie Basisrolcentrum|
|9010|Rolcentrum productieplanner|
|9015|RC opdrachtprojectmanager|
|9016|Rolcentrum servicedispatcher|
|9022|Rolcentrum bedrijfsmanager|
|9024|Rolcentrum beveiligingsbeheerder|
|9026|Verkoop- en relatiemanager RC|
|9027|Rolcentrum Accountant|

> [!TIP]
> We hebben momenteel geen plannen om het aan alle lijstpagina's toe te voegen. U kunt echter een eenvoudige pagina-extensie maken die het onderdeel **Power BI-rapporten** toevoegt in een feitenblok. Zie voor meer informatie [De onderdelen van Power BI-rapporten toevoegen aan pagina's](/dynamics365/business-central/dev-itpro/developer/devenv-power-bi-report-parts) in de Help voor ontwikkelaars en IT-professionals.

<!-- 5 -->
### <a name="is-there-any-way-to-filter-a-dataset-from-business-central-before-i-pull-it-into-power-bi-instead-of-applying-filters-afterwards"></a>Is er een manier om een gegevensset uit Business Central te filteren *voordat* ik deze in Power BI opneem in plaats van achteraf filters toe te passen?

Om grotere datasets te filteren, is de eenvoudigste manier om een filter voor uw Power BI-rapport in te stellen door de Power Query-formule rechtstreeks te bewerken. De meeste filters die u op deze manier instelt, worden doorgegeven aan Business Central via het opvouwen van query's. Zie [Incrementele vernieuwing voor datasets](/power-bi/admin/service-premium-incremental-refresh).

Er is momenteel geen manier om een filter in te stellen voor de webservicegegevens vanuit Business Central. Als uw toepassing een filter moet instellen vanuit Business Central, moet u voor dit doel een aangepaste Business Central-app maken.

<!-- 8 and 9 -->

### <a name="for-embedding-reports-in-business-central-pages-right-now-its-only-possible-to-get-reports-from-my-workspace-in-power-bi-are-there-plans-to-make-it-possible-to-get-them-from-custom-workspaces"></a>Als u rapporten in Business Central-pagina's wilt insluiten, is het momenteel alleen mogelijk om rapporten uit *Mijn werkruimte* in Power BI op te nemen. Zijn er plannen om het mogelijk te maken om ze uit aangepaste werkruimten te halen?

Ja. We zijn van plan om ondersteuning voor gedeelde werkplekken toe te voegen, maar we kunnen nu nog geen tijdlijn geven.  

<!-- 10 -->
### <a name="from-power-bi-besides-using-a-query-is-there-another-way-to-get-data-from-business-central-tables-that-dont-have-an-associated-page-for-example-like-the-item-attributes-value-mapping-table"></a>Is het mogelijk om in Power BI, behalve met een query, ook nog op een andere manier gegevens uit Business Central-tabellen worden opgehaald die geen gekoppelde pagina hebben? Bijvoorbeeld zoals de tabel *Toewijzing van artikelkenmerkwaarde*.

Nee. Op dit moment niet.

<!-- 12 --> 
### <a name="are-published-queries-faster-to-use-than-published-pages"></a>Zijn gepubliceerde zoekopdrachten sneller in het gebruik dan gepubliceerde pagina's?

Als het om webservices gaat, zijn gepubliceerde zoekopdrachten meestal sneller dan gelijkwaardige gepubliceerde pagina's. De reden is dat query's zijn geoptimaliseerd voor het lezen van gegevens en geen dure triggers, zoals OnAfterGetRecord, bevatten.

Wanneer de nieuwe connector in juni 2021 beschikbaar is, wordt u aangemoedigd om API-pagina's te gebruiken in plaats van query's die als webservices zijn gepubliceerd.

<!-- 13 --> 
### <a name="is-there-a-way-for-an-end-user-to-create-a-web-service-with-a-column-thats-in-a-business-central-table-but-not-a-page-or-will-developer-have-to-create-a-custom-query"></a>Is er een manier voor een eindgebruiker om een webservice te maken met een kolom die in een Business Central-tabel staat, maar geen pagina? Of moet de ontwikkelaar een aangepaste query maken? 

Nog niet. Maar wanneer de nieuwe connector in juni 2021 beschikbaar is, kan een ontwikkelaar een nieuwe API-pagina maken om aan deze vereiste te voldoen. 

<!-- 28 --> 
### <a name="can-i-connect-power-bi-to-a-read-only-database-server-of-business-central-online"></a>Kan ik Power BI verbinden met een alleen-lezen databaseserver van Business Central Online? 

Nee. We hebben deze functie echter wel op onze langetermijnplanning staan. 

## <a name="performance"></a>[Prestaties](#tab/performance)

<!-- 17 -->

### <a name="is-it-faster-to-get-data-using-api-pages-than-using-web-services"></a>Gaat het ophalen van gegevens sneller met API-pagina's dan met webservices?

Ja. Uit onze tests blijkt dat API-pagina's tot 25% beter presteren dan webservices.

<!-- 18 -->
### <a name="are-there-plans-to-have-a-mirror-on-the-azure-sql-database-instance-which-i-can-connect-to-directly"></a>Zijn er plannen voor een mirror voor het Azure SQL Database-exemplaar, waarmee ik rechtstreeks verbinding kan maken?

Nee. Op dit moment niet. U kunt alleen communiceren met Business Central via API's.

<!-- 19 -->
### <a name="loading-data-from-business-central-web-services-seems-slow-is-there-any-way-to-get-data-directly-from-the-sql-database-table"></a>Het laden van gegevens van Business Central-webservices lijkt traag te verlopen. Is er een manier om gegevens rechtstreeks uit de SQL-databasetabel op te halen?

Nee. Directe toegang tot de database is niet mogelijk, maar overschakelen naar API-pagina's (wanneer de nieuwe connector beschikbaar is) helpt enorm.

## <a name="advanced"></a>[Geavanceerd](#tab/advanced)
<!-- 1 -->

### <a name="are-there-plans-for-the-power-bi-connector-to-support-the-incremental-refresh-features-in-the-power-bi-service"></a>Is het de bedoeling dat de Power BI-connector de incrementele vernieuwingsfuncties in de Power BI-service in de toekomst ondersteunt?

Ja. Dat is de bedoeling.

<!-- 2 -->
### <a name="if-a-business-central-on-premises-solution-doesnt-have-internet-access-can-i-still-use-power-bi"></a>Kan ik Power BI nog steeds gebruiken als een on-premises oplossing van Business Central geen internettoegang heeft?
<!-- todo: please explain this one-->

Ja. In dit geval gebruikt u Power BI Desktop lokaal en maakt u on-premises verbinding met Business Central. Eenmaal verbonden, kunt u rapporten maken en bekijken, maar u kunt ze niet publiceren naar de Power BI-service. 
<!-- 20 -->
### <a name="are-there-any-plans-to-make-it-possible-to-replicate-business-central-online-databases-so-theyre-accessible-for-read-only-sql-queries-this-capability-would-support-incremental-refresh-and-be-a-lot-faster-than-apis-or-web-services"></a>Zijn er plannen om het mogelijk te maken om online databases in Business Central te repliceren, zodat ze toegankelijk zijn voor alleen-lezen SQL-query's? Deze mogelijkheid zou incrementele vernieuwing ondersteunen en veel sneller zijn dan API's of webservices.

<!-- todo: what does "BC-Saas-DB-replicated DB accessible" mean? fixe-->
Ja. We hebben deze functie wel op onze langetermijnplanning staan. 

<!-- 21 -->
### <a name="if-i-use-azure-data-factory-to-get-data-from-business-central-and-consume-it-on-power-bi-will-that-help-in-increase-in-performance"></a>Kan ik betere prestaties verwachten als ik Azure Data Factory gebruik om gegevens uit Business Central op te halen en deze te gebruiken in Power BI? 

Ja. Met geavanceerde scenario blijft Business Central goed presteren omdat de gegevenstoegang plaatsvindt via Azure Data Factory.

<!-- 22 -->
### <a name="are-there-any-plans-to-support-power-bi-deployment-pipelines-or-a-way-to-build-deployment-pipelines-for-pbi-reports-similar-to-extensions-or-maybe-even-a-simple-api-in-the-business-admin-center"></a>Zijn er plannen om ondersteuning te bieden voor implementatiepijplijnen voor Power BI of een manier om implementatiepijplijnen te bouwen voor PBI-rapporten, vergelijkbaar met extensies? Of misschien zelfs een simpele API in het Business Central-beheercentrum? 

We onderzoeken deze functie. Power BI biedt uitgebreide API's om de implementatie van rapporten te beheren. Zie voor meer informatie [Inleiding op implementatiepijplijnen](/power-bi/create-reports/deployment-pipelines-overview).

### <a name="ive-tried-the-preview-of-the-new-connector-which-will-be-live-in-june-2021-i-see-some-values-like-_x0020_-when-connecting-to-api-v20-what-are-these-values"></a>Ik heb de preview van de nieuwe connector geprobeerd, die in juni 2021 in gebruik wordt genomen. Ik zie waarden zoals _x0020_  wanneer ik verbinding maak met API v2.0. Wat zijn dit voor waarden?

Met de aanstaande versie van de Power BI-connector kunt u verbinding maken met de Business Central API-pagina's, inclusief API v2.0. Deze pagina's bevatten een aantal velden die zijn gebaseerd op [AL Enum-objecten](/dynamics365/business-central/dev-itpro/developer/devenv-extensible-enums). Velden die zijn gebaseerd op AL Enum-objecten moeten namen hebben die consistent en altijd hetzelfde zijn, zodat rapportfilters altijd werken, ongeacht de taal die of het besturingssysteem dat u gebruikt. Om deze reden worden de velden die zijn gebaseerd op AL Enum niet vertaald en worden ze gecodeerd om speciale tekens, inclusief de spatie, te vermijden. Met name wanneer er een lege optie in het AL Enum-object is, wordt deze gecodeerd naar _x0020_. U kunt altijd een transformatie op uw gegevens toepassen in Power BI als u een andere waarde voor deze velden wilt weergeven, bijvoorbeeld Leeg.


---

## <a name="see-also"></a>Zie ook

[Power BI-licenties](admin-powerbi-setup.md#license)
[Inleiding op Business Central en Power BI](admin-powerbi.md)  
[Overzicht van Power BI-integratie](admin-powerbi-overview.md)  
[Power BI inschakelen in Business Central](admin-powerbi-setup.md)  
[Werken met Power BI-rapporten in Business Central](across-working-with-powerbi.md)  
[Werken met Business Central-gegevens in Power BI](across-working-with-business-central-in-powerbi.md)  
[Power BI-rapporten maken om Business Central-gegevens weer te geven](across-how-use-financials-data-source-powerbi.md)  
[Power BI-documentatie](/power-bi/)  


[!INCLUDE[footer-include](includes/footer-banner.md)]