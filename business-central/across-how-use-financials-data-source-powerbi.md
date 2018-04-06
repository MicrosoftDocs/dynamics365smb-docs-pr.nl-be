---
title: Rapportage voor Business Central instellen in Power BI | Microsoft Docs
description: U kunt uw Financials-gegevens als gegevensbron in Power BI beschikbaar maken en krachtige rapporten maken van de status van uw bedrijf.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 12/21/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 42939e97d121bd3a2abff91671d9f9571faffbfd
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="using-included365finincludesd365finmdmd-as-power-bi-data-source-for-building-reports"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)] gebruiken als Power BI-gegevensbron voor het maken van rapporten
U kunt uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-gegevens als gegevensbron in Power BI beschikbaar maken en krachtige rapporten maken van de status van uw bedrijf.  

> [!NOTE]  
> U moet een geldig account bij [!INCLUDE[d365fin](includes/d365fin_md.md)] en Power BI hebben. Ook moet u [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) downloaden.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-power-bi-desktop"></a>[!INCLUDE[d365fin](includes/d365fin_md.md)] als gegevensbron in Power BI Desktop toevoegen
1. Kies in Power BI Desktop in het linkernavigatievenster **Gegevens ophalen**.
2. Kies in het venster **Gegevens ophalen** achtereenvolgens **Online Services**, **Dynamics 365 Business Central** en de knop **Verbinden**.
3. Power BI geeft een wizard weer die u door het [verbindingsproces](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md) begeleidt. De eerste stap is u aan te melden voor de service. Selecteer **Aanmelden** en kies het account waaronder u zich wilt aanmelden. Dit moet hetzelfde account zijn als waarmee u zich aanmeldt bij [!INCLUDE[d365fin](includes/d365fin_md.md)].
4. Kies de knop **Verbinding maken** om door te gaan. De Power BI-wizard bevat een lijst met [!INCLUDE[d365fin](includes/d365fin_md.md)]-bedrijven en -gegevensbronnen. Met deze gegevensbron worden alle webservices vertegenwoordigd die u hebt gepubliceerd vanuit elk bedrijf in [!INCLUDE[d365fin](includes/d365fin_md.md)].
5. U kunt ook een nieuwe webservice-URL in [!INCLUDE[d365fin](includes/d365fin_md.md)] maken met behulp van de actie **Gegevensset maken** op de pagina **Webservices** met de begeleide instelling **Rapportage instellen** of door de actie **Bewerken in Excel** in de lijsten te kiezen.
6. Geef de gegevens op die u aan uw gegevensmodel wilt toevoegen en kies vervolgens de knop **Laden**.
7. Herhaal de vorige stappen om aanvullende [!INCLUDE[d365fin](includes/d365fin_md.md)]-gegevens aan uw Power BI-gegevensmodel toe te voegen.

> [!NOTE]  
> Zodra u met succes verbinding hebt gemaakt met [!INCLUDE[d365fin](includes/d365fin_md.md)], wordt u niet opnieuw gevraagd zich aan te melden.

Zodra de gegevens zijn geladen, worden deze in de rechternavigatie op de pagina weergegeven. Nu hebt u met succes een verbinding gemaakt met uw Business Central-gegevens en kunt u uw Power BI-rapport gaan maken. Zie de [Power BI-documentatie](https://powerbi.microsoft.com/documentation/powerbi-landing-page/) voor meer informatie.

## <a name="see-also"></a>Zie ook
[Bedrijfsinformatie](bi.md)  
[Welkom bij [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](upload-data.md)  
[Instellen [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)   
[Financiën](finance.md)  
[Power BI verbinden met [!INCLUDE[d365fin](includes/d365fin_md.md)]](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md)  

