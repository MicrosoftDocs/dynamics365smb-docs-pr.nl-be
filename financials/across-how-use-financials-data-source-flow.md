---
title: Dynamics 365 for Financials gebruiken in Microsoft Flow | Microsoft Docs
description: U kunt uw Financials-gegevens als gegevensbron beschikbaar maken in PowerApps.
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: workflow, Odata, Power App, SOAP
ms.date: 03/15/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 76d24ed80adb08083c6167040be8cc6a4bcc3167
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="using-dynamics-365-for-financials-in-microsoft-flow"></a>Dynamics 365 for Financials gebruiken in Microsoft Flow
U kunt uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-gegevens als onderdeel van een werkstroom in Microsoft Flow gebruiken.  

**Opmerking**: u moet een geldige account bij [!INCLUDE[d365fin](includes/d365fin_md.md)] en Flow hebben.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-flow"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)] als gegevensbron in Flow toevoegen
1. Navigeer in uw browser naar [flow.microsoft.com](https://flow.microsoft.com/en-us/) en meld u aan.
2. Kies **Mijn Flows** vanuit het lint boven aan de pagina.
3. Kies in het venster **Mijn Flows** de optie **Geheel nieuw maken**.
4. Selecteer in de lijst met beschikbare triggers een van de twee beschikbare [!INCLUDE[d365fin](includes/d365fin_md.md)]-triggers: *Wanneer een record wordt gemaakt* of *Wanneer een record wordt gewijzigd*.
5. Met Flow wordt een verbindingspagina weergegeven waarin u wordt gevraagd om de gegevens die zijn vereist om verbinding te maken met uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-gegevens. Als u verbinding wilt maken, moet u een naam voor de verbinding, een URL, gebruikersnaam, wachtwoord en bedrijfsnaam voor OData opgeven.

   Voor de *OData-URL* kunt u de URL van OData V4 kopiëren van een van de webservices die worden weergegeven op de pagina **Webservices** in [!INCLUDE[d365fin](includes/d365fin_md.md)], zoals `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   Voor *Bedrijfsnaam* gebruikt u de naam van het veld **Naam** in het venster **Bedrijfsgegevens** in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Als [!INCLUDE[d365fin](includes/d365fin_md.md)] meerdere bedrijven bevat, kies u de relevante bedrijfsnaam in de lijst van het venster **Bedrijven**. In beide gevallen moet u ervoor zorgen dat de naam die u in de PowerApps-wizard opgeeft, exact overeenkomt met de tekst die in [!INCLUDE[d365fin](includes/d365fin_md.md)] wordt weergegeven, zoals `My Company`.

   Voor de gebruikersnaam en het wachtwoord gebruikt u de naam en de toegangssleutel van de webservice die voor uw account worden weergegeven in het venster **Gebruikers** in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Uw gebruikersnaam is bijvoorbeeld *ADMIN* en de webservicetoegangssleutel die dient als uw wachtwoord, is *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*. Zie [Procedure: Gebruikers en machtigingen beheren](ui-how-users-permissions.md) voor meer informatie.
6. Kies de knop **Maken** onder aan de pagina als u wilt doorgaan.

   Met Flow wordt een lijst met tabellen weergegeven die beschikbaar zijn in [!INCLUDE[d365fin](includes/d365fin_md.md)]. Met deze tabellen, of eindpunten, worden alle webservices vertegenwoordigd die u hebt gepubliceerd vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)].

   U kunt ook een nieuwe webservice-URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] maken met behulp van de actie **Gegevensset maken** op de pagina **Webservices** met de begeleide instelling **Rapportage instellen** of door de actie **Bewerken in Excel** in de lijsten te kiezen.
7. Kies de gegevens die u in Flow wilt gebruiken.

Nu hebt u met succes een verbinding gemaakt met uw Dynamics 365-gegevens en kunt u uw Flow gaan maken. Zie de [Flow-documentatie](https://flow.microsoft.com/documentation/getting-started/) voor meer informatie.

## <a name="see-also"></a>Zie ook
[Welkom bij [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)](index.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](upload-data.md)  
[Procedure: Gebruikers en machtigingen beheren](ui-how-users-permissions.md)    
[[!INCLUDE[d365fin](includes/d365fin_md.md)] instellen](setup.md)  
[Financiën](finance.md)  

