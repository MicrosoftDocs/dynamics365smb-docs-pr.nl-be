---
title: Veelgestelde vragen over Power BI
description: Krijg antwoorden op enkele veelvoorkomende vragen over het werken met Power BI en Business Central.
author: jswymer
ms.topic: get-started
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'Power BI, reports, faq, errors'
ms.date: 04/22/2021
ms.author: jswymer
---
# Veelgestelde vragen over Power BI

In dit artikel worden enkele van de vragen beantwoord die u mogelijk hebt over het werken met Power BI en [!INCLUDE [prod_short](includes/prod_short.md)].

## [Algemeen](#tab/general)
<!-- 26 -->
### Ik heb een rapport geselecteerd voor mijn rolcentrum in Business Central. Wordt het rolcentrum automatisch bijgewerkt met mijn wijzigingen als ik later online wijzigingen aanbreng in de visuals van het rapport?

Ja, de rapporten zijn ingesloten vanuit Power BI.

<!-- 3 -->
### Zijn de Business Central-apps voor Power BI beschikbaar in andere talen dan het Engels?

Nee. Deze apps zijn momenteel alleen beschikbaar in het Engels.

<!-- 24 -->
### Kan ik de pbix downloaden zodra een rapport is gepubliceerd op mijn powerbi.com-werkruimte? 

Ja. Zie voor meer informatie [Een rapport van de Power BI-service naar Power BI Desktop downloaden](/power-bi/create-reports/service-export-to-pbix).  

<!-- 27 -->
### Kan ik de apps downloaden als pbix-bestanden? 

Nee. Momenteel bieden we geen downloadbare pbix-bestanden voor de officiële Power BI-apps omdat ze worden gepubliceerd op AppSource.

## [Licentie](#tab/license)

<!-- 14 -->
### Heb ik een Power BI Pro-licentie nodig om rapporten te publiceren? 

<!-- todo What does " or for every user that consults the published report" mean? fixed -->
Nee. Een Pro-licentie is niet nodig om rapporten te publiceren. De (gratis) standaardlicentie voor Power BI volstaat. Zie [Power BI-licenties](admin-powerbi-setup.md#license) voor meer informatie.

<!-- 15 -->
### Is er iets dat ik niet kan doen met de gratis licentie?

U kunt geen rapporten delen of de Business Central-apps voor Power BI installeren. Verder kunt u met de gratis licentie bijna alle variaties van grafieken en rapporten maken.

<!-- 16 -->
### Als iemand een rapport met een andere persoon deelt, heeft die persoon een Pro-licentie nodig om het rapport te zien. Zijn er plannen om deze mogelijkheid mogelijk te maken met de gratis licentie?

We hebben geen controle over deze vereiste. Deze vereiste wordt gesteld door Power BI. Zie voor meer informatie [Power BI-dashboards en -rapporten met collega's en anderen delen](/power-bi/collaborate-share/service-share-dashboards).  

## [Ontwerper](#tab/designer)

<!-- 7 -->
### Werkt de connector met API-pagina's?

Ja. Vanaf juni 2021 ondersteunt de nieuwe Power BI-connector zowel Business Central-webservices als API-pagina's. Zie voor meer informatie [Power BI-connector inschakelen om te werken met Business Central-API's in plaats van alleen met webservices](/dynamics365-release-plan/2021wave1/smb/dynamics365-business-central/enable-power-bi-connector-work-business-central-apis-instead-web-services-only).

### Kan ik een Power BI-rapport maken met de Verkoopfactuurregels- of Journaalregels-API's?

De meest gebruikte regelrecords zijn beschikbaar in de [Business Central-API's v2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/)). U kunt ze dus gebruiken om rapporten in Power BI te maken door ze te selecteren in de **Dynamics 365 Business Central**-connector. Echter, de **Regels**-API's zijn ontworpen om alleen te worden gebruikt met enkele zeer specifieke filters en werken mogelijk niet in uw scenario. U krijgt mogelijk een foutmelding die lijkt op "U moet een id of een document-id opgeven om de regels te krijgen". Om dit probleem op te lossen voert u de volgende stappen uit bij het ophalen van gegevens van Business Central voor het rapport in Power BI Desktop:

1. Voeg de bovenliggende gegevensbron toe in plaats van de gegevensbron voor de regelentiteit op te nemen. Voeg bijvoorbeeld **Verkoopfactuur** toe in plaats van **Verkoopfactuurregels**.
2. Selecteer **Gegevens transformeren** in de Power BI Desktop-actiebalk.
3. Selecteer de query die u zojuist heeft toegevoegd, bijvoorbeeld **Verkoopfacturen**.
4. Pas eventueel benodigde filtering op de records toe om het aantal records dat in uw rapport wordt geladen te verminderen.
5. Schuif naar rechts totdat u een kolom vindt met de naam regels, bijvoorbeeld **Verkoopfactuurregels**.
6. Selecteer de uitvouwknop in de kop van de kolom, naast de kolomnaam.

   :::image type="content" source="media/saleinvoicelines.png" alt-text="Toont de kolom Verkoopfactuurregels in Power BI Desktop.":::
<!-- 11 --> 
### Is het mogelijk om te kiezen uit welke Business Central-omgeving de gegevens moeten worden opgehaald voor Power BI, bijvoorbeeld een sandbox- of productieomgeving? 

Ja. Dit kan gemakkelijk. Wanneer u via de connector verbinding maakt met Business Central, moet u de omgeving en de bedrijfsnaam kiezen.

<!-- 6 --> 
### Kan ik gegevens uit verschillende productieomgevingen van dezelfde tenant samenvoegen?

Ja. Voer in Power BI de bewerking Gegevens ophalen opnieuw uit en kies de gewenste omgeving.

<!-- 25 -->
### Welke pagina's in Business Central bieden het Power BI-rapportonderdeel?  

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
### Is er een manier om een gegevensset uit Business Central te filteren *voordat* ik deze in Power BI opneem in plaats van achteraf filters toe te passen?

Om grotere datasets te filteren is de eenvoudigste manier een filter voor uw Power BI-rapport in te stellen door de Power Query-formule rechtstreeks te bewerken. De meeste filters die u op deze manier instelt, worden doorgegeven aan Business Central via het opvouwen van query's. Zie [Incrementele vernieuwing voor datasets](/power-bi/admin/service-premium-incremental-refresh).

Er is momenteel geen manier om een filter in te stellen voor de webservicegegevens vanuit Business Central. Als uw toepassing een filter moet instellen vanuit Business Central, moet u voor dit doel een aangepaste Business Central-app maken.

<!-- 10 -->
### Is het mogelijk om in Power BI, behalve met een query, ook nog op een andere manier gegevens uit Business Central-tabellen worden opgehaald die geen gekoppelde pagina hebben? Bijvoorbeeld zoals de tabel *Toewijzing van artikelkenmerkwaarde*.

Nee. Op dit moment niet.

<!-- 12 --> 
### Zijn gepubliceerde zoekopdrachten sneller in het gebruik dan gepubliceerde pagina's?

Als het om webservices gaat, zijn gepubliceerde zoekopdrachten meestal sneller dan gelijkwaardige gepubliceerde pagina's. De reden is dat query's zijn geoptimaliseerd voor het lezen van gegevens en geen dure triggers, zoals OnAfterGetRecord, bevatten.

Webservices zijn gebaseerd op pagina's of zoekopdrachten die zijn gebouwd voor toegang vanaf internet en meestal niet zijn geoptimaliseerd voor toegang vanaf externe services. Hoewel de Business Central-connector nog steeds ondersteuning biedt voor het ophalen van gegevens van webservices, raden we u aan om waar mogelijk API-pagina's te gebruiken in plaats van webservices.

<!-- 13 --> 
### Is er een manier voor een eindgebruiker om een webservice te maken met een kolom die in een Business Central-tabel staat, maar geen pagina? Of moet de ontwikkelaar een aangepaste query maken? 

Er is momenteel geen manier om een nieuw veld toe te voegen aan een webservice. API-pagina's bieden volledige flexibiliteit in de paginastructuur, zodat een ontwikkelaar een nieuwe API-pagina kan maken om aan deze vereiste te voldoen. 

<!-- 28 --> 
### Kan ik Power BI verbinden met een alleen-lezen databaseserver van Business Central Online? 

Deze functionaliteit zal binnenkort beschikbaar zijn. Vanaf februari 2022 proberen nieuwe rapporten die u maakt op basis van Business Central online-gegevens automatisch verbinding te maken met een alleen-lezen databasereplica. Hierdoor worden uw rapporten sneller vernieuwd en heeft dit minder invloed op de prestaties als u Business Central gebruikt terwijl een rapport wordt vernieuwd. We raden u toch aan om, indien mogelijk, uw rapporten zo te plannen dat ze buiten de normale werkuren worden vernieuwd.

Als u oude rapporten hebt die zijn gebaseerd op Business Central-gegevens, maken ze geen verbinding met de alleen-lezen databasereplica.

### <a name="databasemods"></a>Ik heb de preview van de nieuwe connector voor de update van februari 2022 geprobeerd. Wanneer ik verbinding maak met mijn aangepaste Business Central API-pagina, krijg ik de foutmelding "Kan geen record invoegen. De huidige verbindingsintentie is alleen-lezen." Hoe kan ik dit herstellen?

Met de nieuwe connector maken nieuwe rapporten die gebruikmaken van Business Central-gegevens standaard verbinding met een alleen-lezen replica van de Business Central-database. Deze wijziging zorgt voor een prestatieverbetering. In zeldzame gevallen kan dit echter de fout veroorzaken. Deze fout treedt meestal op omdat uw aangepaste API wijzigingen aanbrengt in Business Central-records terwijl Power BI probeert de gegevens op te halen. Het gebeurt met name als onderdeel van de AL-triggers: OnInit, OnOpenPage, OnFindRecord, OnNextRecord, OnAfterGetRecord en OnAfterGetCurrRecord.

Als u dit probleem wilt oplossen door de Business Central-connector te dwingen dit gedrag toe te staan, raadpleegt u [Power BI-rapporten maken om Business Central-gegevens weer te geven - Problemen oplossen](across-how-use-financials-data-source-powerbi.md#fixing-problems).

<!--
In general, we recommend avoiding any database modifications in API pages when they're opening or loading records, because they cause performance issues and might cause your report refresh to fail. In some cases, you might still need to make a database modification when your custom API page opens or loads records. You can force the Business Central connector to allow this behavior. Do the following steps when getting data from Business Central for the report in Power BI Desktop:

1. Start Power BI Desktop.
2. In the ribbon, select **Get Data** > **Online Services**.
3. In the **Online Services** pane, select **Dynamics 365 Business Central**, then **Connect**.
4. In the **Navigator** window, select the API endpoint that you want to load data from.
5. In the preview pane on the right, you'll see the following error:

   *Dynamics365BusinessCentral: Request failed: The remote server returned an error: (400) Bad Request. (Cannot insert a record. Current connection intent is Read-Only. CorrelationId: [...])".*

6.  Select **Transform Data** instead of **Load** as you might normally do.
7. In **Power Query Editor**, select **Advanced Editor** from the ribbon.
8.  Replace the following line:

   ```
   Source = Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, null),
   ```

   with the line:

   ```
   Source = Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, [UseReadOnlyReplica = false]),
   ```

9.  Select **Done**.
10. Select **Close & Apply** from the ribbon to save the changes and close Power Query Editor.

-->
### <a name="perms"></a>Hoe wijzig of wis ik het gebruikersaccount dat ik momenteel gebruik om verbinding te maken met Business Central vanuit Power BI Desktop?

Ga in Power BI Desktop op een van de volgende manieren te werk:

1. Selecteer in het menu Bestand **Opties en instellingen** > **Instellingen van gegevensbron**.
2. Selecteer **Dynamics Business Central** uit de lijst en selecteer vervolgens **Machtigingen wissen** > **Verwijderen**.

De volgende keer dat u verbinding maakt met Business Central om gegevens op te halen, wordt u gevraagd u aan te melden.

## [Prestaties](#tab/performance)

<!-- 17 -->

### Gaat het ophalen van gegevens sneller met API-pagina's dan met webservices?

Ja. Uit onze tests blijkt dat API-pagina's tot 25% beter presteren dan webservices.

<!-- 18 -->
### Zijn er plannen voor een mirror voor het Azure SQL Database-exemplaar, waarmee ik rechtstreeks verbinding kan maken?

Nee. Op dit moment niet. U kunt alleen communiceren met Business Central via API's.

<!-- 19 -->
### Het laden van gegevens van Business Central-webservices lijkt traag te verlopen. Is er een manier om gegevens rechtstreeks uit de SQL-databasetabel op te halen?

Nee. Directe toegang tot de database is niet mogelijk, maar overschakelen naar API-pagina's (wanneer de nieuwe connector beschikbaar is) helpt enorm.

## [Geavanceerd](#tab/advanced)
<!-- 1 -->

### Is het de bedoeling dat de Power BI-connector de incrementele vernieuwingsfuncties in de Power BI-service in de toekomst ondersteunt?

Ja. Dat is de bedoeling.

<!-- 2 -->
### Kan ik Power BI nog steeds gebruiken als een on-premises oplossing van Business Central geen internettoegang heeft?
<!-- todo: please explain this one-->

Ja. In dit geval gebruikt u Power BI Desktop lokaal en maakt u on-premises verbinding met Business Central. Eenmaal verbonden, kunt u rapporten maken en bekijken, maar u kunt ze niet publiceren naar de Power BI-service. 
<!-- 20 -->
### Zijn er plannen om het mogelijk te maken om online databases in Business Central te repliceren, zodat ze toegankelijk zijn voor alleen-lezen SQL-query's? Deze mogelijkheid zou incrementele vernieuwing ondersteunen en veel sneller zijn dan API's of webservices.

<!-- todo: what does "BC-Saas-DB-replicated DB accessible" mean? fixe-->
Ja. We hebben deze functie wel op onze langetermijnplanning staan. 

<!-- 21 -->
### Kan ik betere prestaties verwachten als ik Azure Data Factory gebruik om gegevens uit Business Central op te halen en deze te gebruiken in Power BI? 

Ja. Met geavanceerde scenario blijft Business Central goed presteren omdat de gegevenstoegang plaatsvindt via Azure Data Factory.

<!-- 22 -->
### Zijn er plannen om ondersteuning te bieden voor implementatiepijplijnen voor Power BI of een manier om implementatiepijplijnen te bouwen voor PBI-rapporten, vergelijkbaar met extensies? Of misschien zelfs een simpele API in het Business Central-beheercentrum? 

We onderzoeken deze functie. Power BI biedt uitgebreide API's om de implementatie van rapporten te beheren. Zie voor meer informatie [Inleiding op implementatiepijplijnen](/power-bi/create-reports/deployment-pipelines-overview).

### Wanneer ik gegevens van Business Central ontvang om te gebruiken in mijn Power BI-rapporten, zie ik enkele waarden zoals "_x0020_". Wat zijn dit voor waarden?

Sommige API-pagina's, waaronder de meeste API v2.0-pagina's, hebben velden die zijn gebaseerd op [AL Enum-objecten](/dynamics365/business-central/dev-itpro/developer/devenv-extensible-enums). Velden die zijn gebaseerd op AL enum-objecten moeten namen hebben die consistent en altijd hetzelfde zijn, zodat rapportfilters altijd werken&mdash;ongeacht de taal die of het besturingssysteem dat u gebruikt. Om deze reden worden de velden die zijn gebaseerd op AL enums niet vertaald en worden ze gecodeerd om speciale tekens, inclusief de spatie, te vermijden. Met name wanneer er een lege optie in het AL Enum-object is, wordt deze gecodeerd naar _x0020_. U kunt altijd een transformatie op uw gegevens toepassen in Power BI als u een andere waarde voor deze velden wilt weergeven, bijvoorbeeld Leeg.

## Zie ook

[Power BI-licenties](admin-powerbi-setup.md#license)  
[Inleiding in Business Central en Power BI](admin-powerbi.md)  
[Overzicht van Power BI-integratie](admin-powerbi-overview.md)  
[Power BI inschakelen in Business Central](admin-powerbi-setup.md)  
[Werken met Power BI-rapporten in Business Central](across-working-with-powerbi.md)  
[Werken met Business Central-gegevens in Power BI](across-working-with-business-central-in-powerbi.md)  
[Power BI-rapporten maken om Business Central-gegevens weer te geven](across-how-use-financials-data-source-powerbi.md)  
[Power BI-documentatie](/power-bi/)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
