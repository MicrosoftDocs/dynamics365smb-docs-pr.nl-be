---
title: Werken met Business Central Data in Power BI| Microsoft Docs
description: 'Met Power BI kunt u eenvoudig inzicht verwerven, bedrijfsinformatie genereren en KPI''s vaststellen op basis van uw Business Central-gegevens.'
author: jswymer
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'account schedule, analysis, reporting, financial report, business intelligence, KPI'
ms.date: 09/07/2022
ms.author: jswymer
---
# Werken met [!INCLUDE [prod_short](includes/prod_short.md)] -gegevens in Power BI

In dit artikel leert u enkele basisbeginselen kennen van het werken met rapporten en dashboards in Power BI, dat gebruikmaakt van [!INCLUDE [prod_short](includes/prod_short.md)] als gegevensbron. In het artikel worden enkele aspecten besproken die u op weg helpen als [!INCLUDE[prod_short](includes/prod_short.md)]-gebruiker. Raadpleeg voor algemene richtlijnen en instructies voor het gebruik van Power BI de [Power BI-documentatie voor consumenten](/power-bi/consumer).

## Bereid u voor

Meld u aan voor de Power BI-service. Als u zich nog niet hebt aangemeld, gaat u naar [https://powerbi.microsoft.com](https://powerbi.microsoft.com). Gebruik wanneer u zich aanmeldt een zakelijk e-mailadres en wachtwoord.

## Aan de slag

Als u eenmaal een Power BI-account hebt, kunt u zich aanmelden via [https://powerbi.microsoft.com/](https://powerbi.microsoft.com/).

De Power BI-service host alle rapporten die voor u beschikbaar zijn. Als u een rapport wilt bekijken, selecteert u **Mijn werkruimte** > **Rapporten**. Selecteer vervolgens het rapport dat u wilt bekijken.

Met [!INCLUDE[prod_short](includes/prod_short.md)] online hebt u automatisch de beschikking over een set standaardrapporten in uw werkruimte. Als u uw eigen rapporten wilt maken, kunt u gebruikmaken van Power BI Desktop om rapporten te maken en deze vervolgens te publiceren naar uw werkruimte. Zie [Aan de slag met het maken van rapporten in Power BI Desktop om [!INCLUDE [prod_long](includes/prod_long.md)]-gegevens weer te geven](across-how-use-financials-data-source-powerbi.md) voor meer informatie.

[!INCLUDE[note-multicompany-reports](includes/note-multicompany-reports.md)]

Als u [!INCLUDE[prod_short](includes/prod_short.md)] on-premises gebruikt, moet u alle rapporten zelf maken met Power BI Desktop. Power BI-rapporten kunnen desgewenst worden gedistribueerd als bestanden die kunnen worden geüpload.

## De meest recente gegevens ophalen

Elk Power BI-rapport is gebaseerd op een gegevensset die gegevens ophaalt uit de [!INCLUDE[prod_short](includes/prod_short.md)]-bronnen. U wilt er uiteraard zeker van zijn dat de gegevens in uw Power BI-rapporten altijd up-to-date zijn, dus overeenkomen met de gegevens in [!INCLUDE[prod_short](includes/prod_short.md)]. Dit concept wordt *vernieuwen* genoemd.  Of de gegevens automatisch worden vernieuwd, hangt af van de manier waarop uw organisatie Power BI heeft geconfigureerd. Er zijn twee manieren om gegevens te vernieuwen: handmatig of via een geplande automatische vernieuwingsactie. Handmatig vernieuwen kan op aanvraag, wanneer dat nodig is. Met gepland vernieuwen kunt u de gegevens steeds automatisch laten vernieuwen na een bepaald tijdsinterval.

### Handmatig vernieuwen

Selecteer in het navigatievenster onder **Gegevenssets** de opdracht **Meer opties (...)** naast de gegevensset en selecteer vervolgens **Nu vernieuwen**.

### Het vernieuwen van gegevens plannen

Selecteer in het navigatievenster onder Gegevenssets de opdracht Meer opties (...) naast de gegevensset en selecteer vervolgens **Vernieuwen plannen**. Vul de gegevens in in het gedeelte **Vernieuwen plannen** en selecteer **Toepassen**.

Zie [Geplande vernieuwing configureren](/power-bi/connect-data/refresh-scheduled-refresh) voor meer informatie.

## <a name="upload"></a>Rapporten uploaden vanuit bestanden

Power BI-rapporten kunnen onder gebruikers worden verspreid als PBIX-bestanden. Als u een PBIX-bestand heeft, kunt u het bestand uploaden naar een werkruimte. Voer de volgende stappen uit om een rapport te uploaden:

1. Selecteer in uw nieuwe werkruimte de optie **Gegevens ophalen**.

2. Selecteer in het vak Bestanden de optie **Ophalen**.

3. Selecteer **Lokaal bestand**, navigeer naar de plaats waar u het bestand hebt opgeslagen en selecteer **Openen**.

Zie [Het rapport uploaden naar de service](/power-bi/paginated-reports/paginated-reports-quickstart-aw#upload-the-report-to-the-service) voor meer informatie.

> [!NOTE]
> Als u een rapport wilt uploaden, moet u beschikken over een werkruimte in een [Premium-capaciteit](/power-bi/service-premium-what-is). Raadpleeg [Premium-capaciteiten beheren](/power-bi/admin/service-premium-capacity-manage) voor meer informatie. 

> [!TIP]
> Als u [!INCLUDE[prod_short](includes/prod_short.md)] online gebruikt, kunt u ook een rapport uploaden vanuit [!INCLUDE[prod_short](includes/prod_short.md)]. Zie [Werken met Power BI-rapporten in [!INCLUDE [prod_short](includes/prod_short.md)] - Rapporten uploaden](across-working-with-powerbi.md#upload) voor meer informatie.

## <a name="share"></a>Rapporten met anderen delen

Zodra een rapport zich in uw werkruimte bevindt, kunt u het delen met anderen in uw organisatie.

Als u een rapport wilt delen, selecteert u in een lijst met rapporten of in een geopend rapport de optie **Delen**. Voer in het deelvenster **Rapport delen** het volledige e-mailadres in van individuen of distributiegroepen waarmee u het rapport wilt delen. Volg de instructies op het scherm om het delen te voltooien. Zie [Een dashboard of rapport delen](/power-bi/collaborate-share/service-share-dashboards#share-a-dashboard-or-report) voor meer informatie.

> [!NOTE]
> U moet een [Power BI Pro-licentie](/power-bi/service-features-license-type) hebben en dat geldt ook voor de mensen met wie u het rapport deelt. De inhoud moet zich in een werkruimte in een [Premium-capaciteit](/power-bi/service-premium-what-is) bevinden. Zie [Manieren om uw werk te delen in Power BI](/power-bi/service-how-to-collaborate-distribute-dashboards-reports) voor meer informatie.

## Zie gerelateerde [Microsoft-training](/training/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## Zie ook

[Business Central en Power BI](admin-powerbi.md)  
[Power BI-rapporten maken om [!INCLUDE [prod_long](includes/prod_long.md)]-gegevens weer te geven](across-how-use-financials-data-source-powerbi.md)  
[Power BI-integratieonderdeel en architectuuroverzicht voor [!INCLUDE[prod_short](includes/prod_short.md)]](admin-powerbi-overview.md)  
[Werken met Power BI-rapporten in [!INCLUDE [prod_short](includes/prod_short.md)]](across-working-with-powerbi.md)  
[Power BI voor consumenten](/power-bi/consumer/end-user-consumer)  
[De 'nieuwe look' van de Power BI-service](/power-bi/service-new-look)  
[Snelle start: verbinding maken met uw gegevens in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
[Power BI-documentatie](/power-bi/)  
[Bedrijfsinformatie](bi.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Instellen van [!INCLUDE[prod_short](includes/prod_short.md)]](setup.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken als Power BI-gegevensbron](across-how-use-financials-data-source-powerbi.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken als Power Apps-gegevensbron](across-how-use-financials-data-source-powerapps.md)  
[[!INCLUDE[prod_short](includes/prod_short.md)] gebruiken in Power Automate](across-how-use-financials-data-source-flow.md)  




[!INCLUDE[footer-include](includes/footer-banner.md)]
