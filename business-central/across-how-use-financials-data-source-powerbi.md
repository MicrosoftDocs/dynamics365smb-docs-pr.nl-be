---
title: Rapporten maken in Power BI Desktop om Business Central-gegevens weer te geven | Microsoft Docs
description: Maak uw gegevens als gegevensbron in Power BI beschikbaar en maak krachtige rapporten met de status van uw bedrijf.
author: jswymer
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'business intelligence, KPI, Odata, Power App, SOAP, analysis'
ms.date: 09/07/2022
ms.author: jswymer
---

# Power BI-rapporten maken om [!INCLUDE [prod_long](includes/prod_long.md)]-gegevens weer te geven

U kunt uw [!INCLUDE[prod_long](includes/prod_long.md)]-gegevens als gegevensbron beschikbaar maken in Power BI Desktop en krachtige rapporten maken met de status van uw bedrijf.

In dit artikel wordt beschreven hoe u aan de slag kunt met Power BI Desktop om rapporten te maken waarin [!INCLUDE[prod_long](includes/prod_long.md)]-gegevens worden weergegeven.  Nadat u rapporten hebt gemaakt, kunt u deze publiceren via uw Power BI-service of delen met alle gebruikers in uw organisatie. Zodra deze rapporten zich in de Power BI-service bevinden, kunnen gebruikers die ervoor zijn ingesteld, vervolgens de rapporten bekijken in [!INCLUDE[prod_long](includes/prod_long.md)].

## Bereid u voor

- Meld u aan voor de Power BI-service.

  Als u zich nog niet hebt aangemeld, gaat u naar [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Gebruik wanneer u zich aanmeldt uw zakelijke e-mailadres en wachtwoord.

- Download [Power BI Desktop](https://powerbi.microsoft.com/desktop/).

  Power BI Desktop is een gratis toepassing die u op uw lokale computer installeert. Zie voor meer informatie [Snelle start: verbinden met gegevens in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).

- Zorg dat de gegevens die u in het rapport wilt, beschikbaar zijn als een API-pagina of zijn gepubliceerd als een webservice.

  Voor meer informatie zie [Gegevens beschikbaar stellen via API-pagina's of OData-webservices](admin-powerbi-setup.md#exposedata).

- Zorg dat u voor [!INCLUDE[prod_short](includes/prod_short.md)] on-premises over de volgende informatie beschikt:

  - De OData-URL voor [!INCLUDE[prod_short](includes/prod_short.md)].
  
    Deze URL heeft doorgaans de indeling `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, bijvoorbeeld `https://localhost:7048/BC190/ODataV4`. Als u een implementatie met meerdere tenants hebt, neemt u de tenant op in de URL, bijvoorbeeld `https://localhost:7048/BC190/ODataV4?tenant=tenant1`.
  - Een gebruikersnaam en een webservicetoegangssleutel van een [!INCLUDE[prod_short](includes/prod_short.md)]-account.

    Power BI maakt gebruik van basisverificatie om gegevens op te halen uit [!INCLUDE[prod_short](includes/prod_short.md)]. U hebt dus een gebruikersnaam en een webservicetoegangssleutel nodig om verbinding te maken. Het account kan uw eigen gebruikersaccount zijn. Het kan ook zijn dat uw organisatie een specifiek account heeft voor dit doel.

- Download het [!INCLUDE [prod_short](includes/prod_short.md)]-rapportthema (optioneel).

  Zie [Het [!INCLUDE [prod_short](includes/prod_short.md)]-rapportthema gebruiken](#theme) in dit artikel voor meer informatie.

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

## <a name="getdata"></a>[!INCLUDE[prod_short](includes/prod_short.md)] als gegevensbron toevoegen in Power BI Desktop

De eerste taak bij het maken van rapporten is het toevoegen van [!INCLUDE[prod_short](includes/prod_short.md)] als een gegevensbron in Power BI Desktop. Als de verbinding tot stand is gebracht, kunt u beginnen met het maken van het rapport.

1. Start Power BI Desktop.
2. Selecteer **Gegevens ophalen**.

    Als u de optie **Gegevens ophalen** niet ziet, selecteert u het menu **Bestand** en vervolgens de optie **Gegevens ophalen**.
3. Selecteer op de pagina **Gegevens ophalen** de optie **Onlineservices**.
4. Voer in het deelvenster **Onlineservices** een van de volgende stappen uit:

    - Om verbinding te maken met [!INCLUDE [prod_short](includes/prod_short.md)] online selecteert u **Dynamics 365 Business Central** en dan **Verbinden**.
    - Om verbinding te maken met [!INCLUDE [prod_short](includes/prod_short.md)] on-premises selecteert u **Dynamics 365 Business Central (on-premises)** en dan **Verbinden**.

5. Meld u aan bij [!INCLUDE [prod_short](includes/prod_short.md)] (eenmalig).

    Als u zich niet eerder hebt aangemeld bij [!INCLUDE [prod_short](includes/prod_short.md)] vanuit Power BI desktop, wordt u gevraagd zich aan te melden.

    - Voor [!INCLUDE [prod_short](includes/prod_short.md)] online selecteert u **Aanmelden** en kiest u het relevante account. Gebruik hetzelfde account dat u gebruikt om u aan te melden bij [!INCLUDE [prod_short](includes/prod_short.md)]. Wanneer u klaar bent, selecteert u **Verbinden**.

    - Voor [!INCLUDE [prod_short](includes/prod_short.md)] on-premises voert u eerst de OData-URL in voor [!INCLUDE[prod_short](includes/prod_short.md)] en selecteert u vervolgens **OK**. Voer wanneer daarom wordt gevraagd de gebruikersnaam en het wachtwoord in van het account dat u wilt gebruiken voor het maken van verbinding met [!INCLUDE[prod_short](includes/prod_short.md)]. Voer in het vak **Wachtwoord** de toegangssleutel voor de webservice in. Wanneer u klaar bent, selecteert u **Verbinden**.

    > [!NOTE]  
    > Zodra u met succes verbinding hebt gemaakt met [!INCLUDE[prod_short](includes/prod_short.md)], wordt u niet opnieuw gevraagd zich aan te melden. [Hoe wijzig of wis ik het account dat ik momenteel gebruik om verbinding te maken met Business Central vanuit Power BI Desktop?](/dynamics365/business-central/power-bi-faq?tabs=designer#perms)

6. Eenmaal verbonden neemt Power BI contract op met de Business Central-service. Het **navigatie**venster verschijnt en toont beschikbare gegevensbronnen voor het maken van rapporten. Selecteer een map om deze uit te vouwen en de beschikbare gegevensbronnen te bekijken. 

   Deze gegevensbronnen vertegenwoordigen alle webservices en API-pagina's die zijn gepubliceerd vanuit [!INCLUDE [prod_short](includes/prod_short.md)]. De gegevensbronnen zijn gegroepeerd op de Business Central-omgevingen en -bedrijven. Met Business Central online heeft **Navigator** de volgende opbouw:

    - **Omgevingsnaam**
      - **Bedrijfsnaam**
        - **Geavanceerde API's**

          Deze map bevat geavanceerde API-pagina's die door Microsoft zijn gepubliceerd, zoals de [API's voor Business Central-automatisering](/dynamics365/business-central/dev-itpro/administration/itpro-introduction-to-automation-apis) en [aangepaste API-pagina's voor Business Central](/dynamics365/business-central/dev-itpro/developer/devenv-develop-custom-api). Aangepaste API-pagina's zijn verder gegroepeerd in mappen op de eigenschappen [APIPublisher](/dynamics365/business-central/dev-itpro/developer/properties/devenv-apipublisher-property)/[APIGroup](/dynamics365/business-central/dev-itpro/developer/properties/devenv-apigroup-property) van de broncode van de API-pagina.

        - **Standaard API's v2.0**

          Deze map bevat de API-pagina's die worden weergegeven door de [Business Central API V2.0](/dynamics365/business-central/dev-itpro/api-reference/v2.0/).

        - **Webservices \(legacy)**

          Deze map bevat pagina's, codeunits en query's die zijn gepubliceerd als webservices in Business Central.

    > [!NOTE]
    > De structuur voor Business Central on-premises is anders omdat het geen API-pagina's ondersteunt.

7. Selecteer de gegevensbron of -bronnen die u aan uw gegevensmodel wilt toevoegen en selecteer vervolgens de knop **Laden**.
8. Als u later meer Business Central-gegevens wilt toevoegen, kunt u de vorige stappen herhalen.

Zodra de gegevens zijn geladen, ziet u deze in de rechternavigatie op de pagina. U hebt nu met succes verbinding gemaakt met uw [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens en u kunt uw Power BI-rapport gaan maken.  

> [!TIP]
> Zie [Aan de slag met Power BI Desktop](/power-bi/fundamentals/desktop-getting-started) voor meer informatie over het gebruik van Power BI Desktop.

## Toegankelijke rapporten maken

Het is belangrijk om uw rapporten bruikbaar te maken voor zoveel mogelijk mensen. Probeer rapporten zo te ontwerpen dat ze geen speciale aanpassingen nodig hebben om aan specifieke behoeften van verschillende gebruikers te voldoen. Zorg ervoor dat gebruikers dankzij het ontwerp kunnen profiteren van standaard ondersteunende technologieën, zoals schermlezers. Power BI bevat verschillende toegankelijkheidsfuncties, tools en richtlijnen om dit doel te bereiken. Zie voor meer informatie [Power BI-rapporten voor toegankelijkheid](/power-bi/create-reports/desktop-accessibility-creating-reports) in de Power BI-documentatie.

## Rapporten maken om gegevens weer te geven die aan een lijst zijn gekoppeld

U kunt rapporten maken die worden weergegeven in een feitenblok van een [!INCLUDE [prod_short](includes/prod_short.md)]-lijstpagina. De rapporten kunnen gegevens bevatten over de record die in de lijst is geselecteerd. U kunt deze rapporten op ongeveer dezelfde manier maken als andere rapporten, maar u moet wel een paar dingen doen om ervoor te zorgen dat de rapporten worden weergegeven zoals verwacht. Zie [Power BI-rapporten maken voor het weergeven van lijstgegevens in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md) voor meer informatie.

## <a name="theme"></a>Het [!INCLUDE [prod_short](includes/prod_short.md)]-rapportthema gebruiken (optioneel)

U wordt aangeraden om voordat u uw rapport maakt het [!INCLUDE [prod_short](includes/prod_short.md)]-themabestand te downloaden en importeren. Het themabestand maakt een kleurenpalet, zodat u rapporten kunt maken met dezelfde kleurstijl als de [!INCLUDE [prod_short](includes/prod_short.md)]-apps zonder dat u aangepaste kleuren hoeft te definiëren voor elk visueel element.

> [!NOTE]
> Deze taak is optioneel. U kunt altijd uw rapporten maken en later alsnog de stijlsjabloon downloaden en toepassen.

### Het thema downloaden

Het themabestand is beschikbaar als JSON-bestand in de themagalerij van de Microsoft Power BI-community. Voer de volgende stappen uit om het themabestand te downloaden:

1. Ga naar de themagalerij van de [Microsoft Power BI-community voor Microsoft Dynamics 365 Business Central](https://community.powerbi.com/t5/Themes-Gallery/Microsoft-Dynamics-365-Business-Central/m-p/385875).
2. Selecteer de downloadbijlage **Microsoft Dynamics Business Central.json**.

### Het thema in een rapport importeren

Nadat u het [!INCLUDE [prod_short](includes/prod_short.md)]-rapportthema hebt gedownload, kunt u het in uw rapporten importeren. Als u het thema wilt importeren, selecteert u **Weergave** > **Thema's** > **Thema's zoeken**. Zie [Power BI Desktop - aangepaste rapportthema's importeren](/power-bi/create-reports/desktop-report-themes#import-custom-report-theme-files) voor meer informatie.

## Rapporten publiceren

Nadat u een rapport hebt gemaakt of gewijzigd, kunt u het rapport publiceren naar uw Power BI-service en delen met anderen in uw organisatie. Als het rapport eenmaal is gepubliceerd, kunt u het bekijken in Power BI. Het rapport kan ook worden geselecteerd in [!INCLUDE[prod_short](includes/prod_short.md)].

Als u een rapport wilt publiceren, selecteert u **Publiceren** op het tabblad **Start** of in het menu **Bestand**. Als u bent aangemeld bij de Power BI-service, wordt het rapport naar deze service gepubliceerd. Als dat niet het geval is, wordt u gevraagd u aan te melden. 

## Een rapport distribueren of delen

Er zijn een aantal manieren om rapporten beschikbaar te maken voor uw collega's en anderen:

- U kunt rapporten distribueren als PBIX-bestanden.

    Rapporten worden op uw computer opgeslagen als PBIX-bestanden. U kunt het PBIX-rapportbestand net als elk ander bestand onder gebruikers distribueren. Vervolgens kunnen gebruikers het bestand uploaden naar hun Power BI-service. Zie [Rapporten uploaden vanuit bestanden](across-working-with-business-central-in-powerbi.md#upload).

    > [!NOTE]
    > Als u een rapport op deze manier distribueert, houdt dat in dat iedere gebruiker afzonderlijk de gegevens van dat rapport moet vernieuwen. Deze situatie kan van invloed zijn op de prestaties van [!INCLUDE[prod_short](includes/prod_short.md)].

- Het rapport delen vanuit uw Power BI-service

    Als u een Power BI Pro-licentie hebt, kunt u het rapport rechtstreeks vanuit uw Power BI-service delen met anderen. Zie [Power BI - een dashboard of rapport delen](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report) voor meer informatie.

## Problemen oplossen

### "Kan geen record invoegen. De huidige verbindingsintentie is alleen-lezen." fout bij het verbinden met aangepaste API-pagina

> **VAN TOEPASSING OP:** Business Central online

Vanaf februari 2022 maken nieuwe rapporten die gebruikmaken van Business Central-gegevens, standaard verbinding met een alleen-lezen replica van de Business Central-database. In zeldzame gevallen, afhankelijk van het pagina-ontwerp, krijgt u een foutmelding wanneer u verbinding probeert te maken en gegevens van de pagina probeert op te halen.

1. Start Power BI Desktop.
2. Selecteer op het lint **Gegevens ophalen** > **Onlineservices**.
3. Selecteer in het deelvenster **Onlineservices** **Dynamics 365 Business Central** en dan **Verbinden**.
4. Selecteer in het venster **Navigator** het API-eindpunt waaruit u gegevens wilt laden.
5. In het voorbeeldvenster aan de rechterkant ziet u de volgende fout:

   *Dynamics365BusinessCentral: Aanvraag mislukt: de externe server heeft een fout geretourneerd: (400) Ongeldige aanvraag. (Kan geen record invoegen. Huidige verbindingsintentie is Alleen-lezen. CorrelationId: [...])".*

6. Selecteer **Gegevens transformeren** in plaats van **Laden** zoals u normaal zou doen.
7. Selecteer in de **Power Query-editor** **Geavanceerde editor** vanaf het lint.
8. Vervang op de regel die begint met **Source =**, de volgende tekst:

   ```
   Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, null)
   ```

   door:

   ```
   Dynamics365BusinessCentral.ApiContentsWithOptions(null, null, null, [UseReadOnlyReplica = false])
   ```

9. Selecteer **Gereed**.
10. Selecteer **Sluiten en toepassen** op het lint om de wijzigingen op te slaan en de Power Query-editor te sluiten.

## Zie ook

[Uw bedrijfsgegevens inschakelen voor Power BI](admin-powerbi.md)  
[Bedrijfsinformatie](bi.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Instellen van [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Financiën](finance.md)  
[Snelle start: Uw gegevens verbinden in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
