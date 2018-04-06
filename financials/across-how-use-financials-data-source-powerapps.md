---
title: Gebruik uw gegevens om een app te maken| Microsoft Docs
description: U kunt uw Financials-gegevens als gegevensbron beschikbaar maken en een OData-URL van uw webservices opgeven om een bedrijfsapp te maken met PowerApps.
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 40f8d00c8ee064fdee4b676e4863279ec9e50d6d
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="connecting-to-your-financials-data-to-build-a-business-app-using-powerapps"></a>Verbinding met uw Financials-gegevens maken om een bedrijfsapp te maken met PowerApps
U kunt uw gegevens [!INCLUDE[d365fin](includes/d365fin_md.md)] als gegevensbron beschikbaar maken in PowerApps.  

> [!NOTE]  
>   U moet een geldig account bij [!INCLUDE[d365fin](includes/d365fin_md.md)] en PowerApps hebben.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-powerapps"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)] als gegevensbron in PowerApps toevoegen
1. Navigeer in de browser naar [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/) en meld u aan.
2. Kies in het linkernavigatievenster de optie **Nieuwe app**.
3. Kies uw editor, PowerApps Studio for Windows of PowerApps Studio for Web.

   PowerApps Studio for Windows is een bureaubladtoepassing die wordt gebruikt om PowerApps te maken en te publiceren. PowerApps Studio for Web is de online oplossing die wordt gebruikt om PowerApps te maken en te publiceren.
4. De volgende stap om een PowerApp te maken bestaat eruit uw gegevens te selecteren. Kies het pijlpictogram en kies vervolgens de optie **Nieuwe verbinding** linksboven in de pagina.
5. Kies in de lijst met beschikbare verbindingen **Dynamics 365 for Finance and Operations, Business edition**.
6. Met PowerApps wordt een verbindingspagina weergegeven waarin u wordt gevraagd om de gegevens die zijn vereist om verbinding te maken met uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-gegevens. Als u verbinding wilt maken, moet u een URL, gebruikersnaam, wachtwoord en bedrijfsnaam voor OData opgeven.

   Voor de *OData-URL* kunt u de URL van OData V4 kopiëren van een van de webservices die worden weergegeven op de pagina **Webservices** in [!INCLUDE[d365fin](includes/d365fin_md.md)], zoals `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   Voor *Bedrijfsnaam* gebruikt u de naam van het veld **Naam** in het venster **Bedrijfsgegevens** in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Als [!INCLUDE[d365fin](includes/d365fin_md.md)] meerdere bedrijven bevat, kies u de relevante bedrijfsnaam in de lijst van het venster **Bedrijven**. In beide gevallen moet u ervoor zorgen dat de naam die u in de PowerApps-wizard opgeeft, exact overeenkomt met de tekst die in [!INCLUDE[d365fin](includes/d365fin_md.md)] wordt weergegeven, zoals `My Company`.

   Voor de gebruikersnaam en het wachtwoord gebruikt u de naam en de toegangssleutel van de webservice die voor uw account worden weergegeven in het venster **Gebruikers** in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Uw gebruikersnaam is bijvoorbeeld *ADMIN* en de webservicetoegangssleutel die dient als uw wachtwoord, is *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*.
7. Kies de knop **Verbinding** om door te gaan. Met PowerApps wordt een standaardgegevensset weergegeven voor [!INCLUDE[d365fin](includes/d365fin_md.md)]. Kies de gegevensset **Standaard**.

   Met PowerApps wordt een lijst met tabellen weergegeven die beschikbaar zijn in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Met deze tabellen, of eindpunten, worden alle webservices vertegenwoordigd die u hebt gepubliceerd vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)].

   U kunt ook een nieuwe webservice-URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] maken met behulp van de actie **Gegevensset maken** op de pagina **Webservices** met de begeleide instelling **Rapportage instellen** of door de actie **Bewerken in Excel** in de lijsten te kiezen.
8. Kies de tabel die u voor uw PowerApp wilt gebruiken en kies de knop **Verbinding maken**.
9. Herhaal de vorige stappen om aanvullende [!INCLUDE[d365fin](includes/d365fin_md.md)]-gegevens aan uw Power BI-gegevensmodel toe te voegen.

   > [!NOTE]  
>    Zodra u verbinding hebt gemaakt met [!INCLUDE[d365fin](includes/d365fin_md.md)], wordt u niet weer gevraagd om de URL, gebruikersnaam of het wachtwoord van OData.

Nu hebt u met succes een verbinding gemaakt met uw Finance and Operations, Business edition-gegevens en kunt u uw PowerApp gaan maken. Zie de [PowerApps-documentatie](https://powerapps.microsoft.com/tutorials/getting-started/) voor meer informatie.

## <a name="see-also"></a>Zie ook
[Welkom bij [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](upload-data.md)  
[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Financiën](finance.md)  

