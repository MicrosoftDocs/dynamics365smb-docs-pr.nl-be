---
title: Een Power BI-gegevensbron maken met uw Financials | Microsoft Docs
description: U kunt uw Financials-gegevens als gegevensbron in Power BI beschikbaar maken en krachtige rapporten maken van de status van uw bedrijf.
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 06/06/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 3f98a08415a896c37868bf0ed5efd9314d5ab07a
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="using-included365finincludesd365finmdmd-as-a-power-bi-data-source"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken als een Power BI-gegevensbron
U kunt uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-gegevens als gegevensbron in Power BI beschikbaar maken en krachtige rapporten maken van de status van uw bedrijf.  

> [!NOTE]  
>   U moet een geldig account bij [!INCLUDE[d365fin](includes/d365fin_md.md)] en Power BI hebben. Ook moet u [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) downloaden.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-power-bi-desktop"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)] als gegevensbron in Power BI Desktop toevoegen
1. Kies in Power BI Desktop in het linkernavigatievenster **Gegevens ophalen**.
2. Kies in het venster **Gegevens ophalen** achtereenvolgens **Online Services**, **Dynamics 365 for Financials** en de knop **Verbinden**.

   Power BI geeft een wizard weer die u in het verbindingsproces begeleidt. De eerste stap bestaat eruit een OData-URL in te voeren en de bedrijfsnaam die aan uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-account is gekoppeld.  

   Voor de *OData-URL* kunt u de URL van OData V4 kopiëren van een van de webservices die worden weergegeven op de pagina **Webservices** in [!INCLUDE[d365fin](includes/d365fin_md.md)], zoals `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   Voor *Bedrijfsnaam* gebruikt u de naam van het veld **Naam** in het venster **Bedrijfsgegevens** in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Als [!INCLUDE[d365fin](includes/d365fin_md.md)] meerdere bedrijven bevat, kies u de relevante bedrijfsnaam in de lijst van het venster **Bedrijven**. In beide gevallen moet u ervoor zorgen dat de naam die u in de Power BI-wizard opgeeft, exact overeenkomt met de tekst die in [!INCLUDE[d365fin](includes/d365fin_md.md)] wordt weergegeven, zoals `My Company`.
3. Klik op OK nadat u de gegevens hebt ingevoerd. De volgende stap in de wizard bestaat eruit uw gebruikersnaam en wachtwoord in te voeren.

   > [!NOTE]  
>    Als er andere verificatieopties beschikbaar zijn in de linkernavigatie, kiest u *Basis*.
4. Voer uw gebruikersnaam en wachtwoord in. U vindt deze informatie in het venster **Gebruikers** in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Gebruik **Webtoegangssleutel** als uw wachtwoord.

   Uw gebruikersnaam is bijvoorbeeld *ADMIN* en de webservicetoegangssleutel die dient als uw wachtwoord, is *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*.
5. Kies de knop **Verbinding** om door te gaan. De Power BI-wizard bevat een lijst met [!INCLUDE[d365fin](includes/d365fin_md.md)]-gegevensbronnen. Met deze gegevensbron worden alle webservices vertegenwoordigd die u hebt gepubliceerd vanuit uw [!INCLUDE[d365fin](includes/d365fin_md.md)].

   U kunt ook een nieuwe webservice-URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] maken met behulp van de actie **Gegevensset maken** op de pagina **Webservices** met de begeleide instelling **Rapportage instellen** of door de actie **Bewerken in Excel** in de lijsten te kiezen.

6. Geef de gegevens op die u aan uw gegevensmodel wilt toevoegen en kies vervolgens de knop **Laden**.
7. Herhaal de vorige stappen om aanvullende [!INCLUDE[d365fin](includes/d365fin_md.md)]-gegevens aan uw Power BI-gegevensmodel toe te voegen.

   > [!NOTE]  
>    Zodra u verbinding hebt gemaakt met [!INCLUDE[d365fin](includes/d365fin_md.md)], wordt u niet weer gevraagd om de URL, gebruikersnaam of het wachtwoord van OData.

Zodra de gegevens zijn geladen, worden deze in de rechternavigatie op de pagina weergegeven. Nu hebt u met succes een koppeling gemaakt naar uw Dynamics 365-gegevens en kunt u uw Power BI-rapport gaan maken. Zie de [Power BI-documentatie](https://powerbi.microsoft.com/documentation/powerbi-landing-page/) voor meer informatie.

## <a name="see-also"></a>Zie ook
[Bedrijfsinformatie](bi.md)  
[Welkom bij [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](upload-data.md)  
[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Financiën](finance.md)  

