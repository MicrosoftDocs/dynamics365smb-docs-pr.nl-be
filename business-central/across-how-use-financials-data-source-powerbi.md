---
title: Rapporten maken in Power BI Desktop om Business Central-gegevens weer te geven | Microsoft Docs
description: Maak uw gegevens als gegevensbron in Power BI beschikbaar en maak krachtige rapporten met de status van uw bedrijf.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 04/01/2021
ms.author: jswymer
ms.openlocfilehash: ee7e6a132f463f35206dd9ac4fe75ce1a41fd40d
ms.sourcegitcommit: 766e2840fd16efb901d211d7fa64d96766ac99d9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5780094"
---
# <a name="building-power-bi-reports-to-display-prod_long-data"></a>Power BI-rapporten maken om [!INCLUDE [prod_long](includes/prod_long.md)]-gegevens weer te geven

U kunt uw [!INCLUDE[prod_long](includes/prod_long.md)]-gegevens als gegevensbron beschikbaar maken in Power BI Desktop en krachtige rapporten maken met de status van uw bedrijf.

In dit artikel wordt beschreven hoe u aan de slag kunt met Power BI Desktop om rapporten te maken waarin [!INCLUDE[prod_long](includes/prod_long.md)]-gegevens worden weergegeven.  Nadat u rapporten hebt gemaakt, kunt u deze publiceren via uw Power BI-service of delen met alle gebruikers in uw organisatie. Zodra deze rapporten zich in de Power BI-service bevinden, kunnen gebruikers die ervoor zijn ingesteld, vervolgens de rapporten bekijken in [!INCLUDE[prod_long](includes/prod_long.md)].

## <a name="get-ready"></a>Bereid u voor

- Meld u aan voor de Power BI-service.

    Als u zich nog niet hebt aangemeld, gaat u naar [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Gebruik wanneer u zich aanmeldt uw zakelijke e-mailadres en wachtwoord.

- Download [Power BI Desktop](https://powerbi.microsoft.com/desktop/).

   Power BI Desktop is een gratis toepassing die u op uw lokale computer installeert. Zie voor meer informatie [Snelle start: verbinden met gegevens in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).

- Zorg ervoor dat de gegevens die u in het rapport wilt opnemen, als webservice worden gepubliceerd.
    
    Er worden standaard veel webservices gepubliceerd. Een eenvoudige manier om de webservices te vinden, is te zoeken naar *webservices* in [!INCLUDE[prod_short](includes/prod_short.md)]. Zorg ervoor dat op de pagina **Webservices** het veld **Publiceren** is geselecteerd. Deze taak is gewoonlijk een beheertaak.
    
    Zie [Een webservice publiceren](across-how-publish-web-service.md) voor meer informatie over het publiceren van webservices.

- Zorg dat u voor [!INCLUDE[prod_short](includes/prod_short.md)] on-premises over de volgende informatie beschikt:

    - De OData-URL voor [!INCLUDE[prod_short](includes/prod_short.md)]. Deze URL heeft doorgaans de indeling `http[s]://[computer]:[port]/[serverinstance]/ODataV4`, bijvoorbeeld `https://localhost:7048/BC160/ODataV4`. Als u een implementatie met meerdere tenants hebt, neemt u de tenant op in de URL, bijvoorbeeld `https://localhost:7048/BC160/ODataV4?tenant=tenant1`.
    - Een gebruikersnaam en een webservicetoegangssleutel van een [!INCLUDE[prod_short](includes/prod_short.md)]-account.

      Power BI maakt gebruik van basisverificatie om gegevens op te halen uit [!INCLUDE[prod_short](includes/prod_short.md)]. U hebt dus een gebruikersnaam en een webservicetoegangssleutel nodig om verbinding te maken. Het account kan uw eigen gebruikersaccount zijn. Het kan ook zijn dat uw organisatie een specifiek account heeft voor dit doel.

- Download het [!INCLUDE [prod_short](includes/prod_short.md)]-rapportthema (optioneel).

    Zie [Het [!INCLUDE [prod_short](includes/prod_short.md)]-rapportthema gebruiken](#theme) in dit artikel voor meer informatie.

## <a name="add-prod_short-as-a-data-source-in-power-bi-desktop"></a><a name="getdata"></a>[!INCLUDE[prod_short](includes/prod_short.md)] als gegevensbron toevoegen in Power BI Desktop

De eerste taak bij het maken van rapporten is het toevoegen van [!INCLUDE[prod_short](includes/prod_short.md)] als een gegevensbron in Power BI Desktop. Als de verbinding tot stand is gebracht, kunt u beginnen met het maken van het rapport.

1. Start Power BI Desktop.
2. Selecteer **Gegevens ophalen**.

    Als u de optie **Gegevens ophalen** niet ziet, selecteert u het menu **Bestand** en vervolgens de optie **Gegevens ophalen**.
2. Selecteer op de pagina **Gegevens ophalen** de optie **Onlineservices**.
3. Voer in het deelvenster **Onlineservices** een van de volgende stappen uit:

    1. Als u online verbinding wilt maken met [!INCLUDE [prod_short](includes/prod_short.md)], kiest u **Dynamics 365 Business Central** en vervolgens **Verbinden**.
    2. Als u on-premises verbinding wilt maken met [!INCLUDE [prod_short](includes/prod_short.md)], kiest u **Dynamics 365 Business Central (on-premises)** en vervolgens **Verbinden**.

4. Power BI geeft een wizard weer die u door het verbindingsproces begeleidt, inclusief aanmelden bij [!INCLUDE [prod_short](includes/prod_short.md)].

    Maakt u online verbinding, kies dan **Aanmelden** en kies vervolgens het relevante account. Gebruik hetzelfde account dat u gebruikt om u aan te melden bij [!INCLUDE [prod_short](includes/prod_short.md)].
    
    Maakt u on-premises verbinding, voer dan de OData-URL in voor [!INCLUDE[prod_short](includes/prod_short.md)] en desgewenst de bedrijfsnaam. Voer vervolgens, wanneer daarom wordt gevraagd, de gebruikersnaam en het wachtwoord in van het account dat u wilt gebruiken voor het maken van een verbinding met [!INCLUDE[prod_short](includes/prod_short.md)]. Voer in het vak **Wachtwoord** de toegangssleutel voor de webservice in.

    > [!NOTE]  
    > Zodra u met succes verbinding hebt gemaakt met [!INCLUDE[prod_short](includes/prod_short.md)], wordt u niet opnieuw gevraagd zich aan te melden.
    
5. Kies **Verbinden** om door te gaan.

    De wizard Power BI bevat een lijst met Microsoft [!INCLUDE[prod_short](includes/prod_short.md)]-omgevingen, -bedrijven en -gegevensbronnen. Deze gegevensbronnen vertegenwoordigen alle webservices die u hebt gepubliceerd vanuit [!INCLUDE [prod_short](includes/prod_short.md)].
6. Geef de gegevens op die u aan uw gegevensmodel wilt toevoegen en kies vervolgens de knop **Laden**.
7. Herhaal de vorige stappen om aanvullende [!INCLUDE [prod_short](includes/prod_short.md)]- of andere gegevens aan uw Power BI-gegevensmodel toe te voegen.

Zodra de gegevens zijn geladen, ziet u deze in de rechternavigatie op de pagina. U hebt nu met succes verbinding gemaakt met uw [!INCLUDE[prod_short](includes/prod_short.md)]-gegevens en u kunt uw Power BI-rapport gaan maken.  

> [!TIP]
> Zie [Aan de slag met Power BI Desktop](/power-bi/fundamentals/desktop-getting-started) voor meer informatie over het gebruik van Power BI Desktop.

## <a name="creating-reports-to-display-data-associated-with-a-list"></a>Rapporten maken om gegevens weer te geven die aan een lijst zijn gekoppeld

U kunt rapporten maken die worden weergegeven in een feitenblok van een [!INCLUDE [prod_short](includes/prod_short.md)]-lijstpagina. De rapporten kunnen gegevens bevatten over de record die in de lijst is geselecteerd. U kunt deze rapporten op ongeveer dezelfde manier maken als andere rapporten, maar u moet wel een paar dingen doen om ervoor te zorgen dat de rapporten worden weergegeven zoals verwacht. Zie [Power BI-rapporten maken voor het weergeven van lijstgegevens in [!INCLUDE[prod_short](includes/prod_short.md)]](across-how-use-powerbi-reports-factbox.md) voor meer informatie.

## <a name="using-the-prod_short-report-theme-optional"></a><a name="theme"></a>Het [!INCLUDE [prod_short](includes/prod_short.md)]-rapportthema gebruiken (optioneel)

U wordt aangeraden om voordat u uw rapport maakt het [!INCLUDE [prod_short](includes/prod_short.md)]-themabestand te downloaden en importeren. Het themabestand maakt een kleurenpalet, zodat u rapporten kunt maken met dezelfde kleurstijl als de [!INCLUDE [prod_short](includes/prod_short.md)]-apps zonder dat u aangepaste kleuren hoeft te definiëren voor elk visueel element.

> [!NOTE]
> Deze taak is optioneel. U kunt altijd uw rapporten maken en later alsnog de stijlsjabloon downloaden en toepassen.

### <a name="download-the-theme"></a>Het thema downloaden

Het themabestand is beschikbaar als JSON-bestand in de themagalerij van de Microsoft Power BI-community. Voer de volgende stappen uit om het themabestand te downloaden:

1. Ga naar de themagalerij van de [Microsoft Power BI-community voor Microsoft Dynamics 365 Business Central](https://community.powerbi.com/t5/Themes-Gallery/Microsoft-Dynamics-365-Business-Central/m-p/385875).
2. Selecteer de downloadbijlage **Microsoft Dynamics Business Central.json**.

### <a name="import-the-theme-on-a-report"></a>Het thema in een rapport importeren

Nadat u het [!INCLUDE [prod_short](includes/prod_short.md)]-rapportthema hebt gedownload, kunt u het in uw rapporten importeren. Als u het thema wilt importeren, selecteert u **Weergave** > **Thema's** > **Thema's zoeken**. Zie [Power BI Desktop - aangepaste rapportthema's importeren](/power-bi/create-reports/desktop-report-themes#import-custom-report-theme-files) voor meer informatie.

## <a name="publish-reports"></a>Rapporten publiceren

Nadat u een rapport hebt gemaakt of gewijzigd, kunt u het rapport publiceren naar uw Power BI-service en delen met anderen in uw organisatie. Als het rapport eenmaal is gepubliceerd, kunt u het bekijken in Power BI. Het rapport kan ook worden geselecteerd in [!INCLUDE[prod_short](includes/prod_short.md)].

Als u een rapport wilt publiceren, selecteert u **Publiceren** op het tabblad **Start** of in het menu **Bestand**. Als u bent aangemeld bij de Power BI-service, wordt het rapport naar deze service gepubliceerd. Als dat niet het geval is, wordt u gevraagd u aan te melden. 

## <a name="distribute-or-share-a-report"></a>Een rapport distribueren of delen

Er zijn een aantal manieren om rapporten beschikbaar te maken voor uw collega's en anderen:

- U kunt rapporten distribueren als PBIX-bestanden.

    Rapporten worden op uw computer opgeslagen als PBIX-bestanden. U kunt het PBIX-rapportbestand net als elk ander bestand onder gebruikers distribueren. Vervolgens kunnen gebruikers het bestand uploaden naar hun Power BI-service. Zie [Rapporten uploaden vanuit bestanden](across-working-with-business-central-in-powerbi.md#upload).

    > [!NOTE]
    > Als u een rapport op deze manier distribueert, houdt dat in dat iedere gebruiker afzonderlijk de gegevens van dat rapport moet vernieuwen. Deze situatie kan van invloed zijn op de prestaties van [!INCLUDE[prod_short](includes/prod_short.md)].

- Het rapport delen vanuit uw Power BI-service

    Als u een Power BI Pro-licentie hebt, kunt u het rapport rechtstreeks vanuit uw Power BI-service delen met anderen. Zie [Power BI - een dashboard of rapport delen](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report) voor meer informatie.

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Uw bedrijfsgegevens inschakelen voor Power BI](admin-powerbi.md)  
[Bedrijfsinformatie](bi.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Instellen van [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[Financiën](finance.md)  
[Snelle start: Uw gegevens verbinden in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  


[!INCLUDE[footer-include](includes/footer-banner.md)]