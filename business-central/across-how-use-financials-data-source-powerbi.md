---
title: Business Central gebruiken in Power BI-rapporten | Microsoft Docs
description: Maak uw gegevens als gegevensbron in Power BI beschikbaar en maak krachtige rapporten met de status van uw bedrijf.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2019
ms.author: edupont
ms.openlocfilehash: c843f0fb6c8017817ada9dc5bf2af0ef68a5cc5a
ms.sourcegitcommit: cfc92eefa8b06fb426482f54e393f0e6e222f712
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/03/2019
ms.locfileid: "2878760"
---
# <a name="using-include-prodlongincludesprodlongmd-as-power-bi-data-source-for-building-reports"></a>[!INCLUDE [prodlong](includes/prodlong.md)] gebruiken als Power BI-gegevensbron voor het maken van rapporten

U kunt uw [!INCLUDE[prodlong](includes/prodlong.md)]-gegevens als gegevensbron beschikbaar maken in Power BI en krachtige rapporten maken met de status van uw bedrijf.  

U moet een geldig account bij [!INCLUDE[prodshort](includes/prodshort.md)] en Power BI hebben. U moet ook [Power BI Desktop](https://powerbi.microsoft.com/desktop/) downloaden. Zie voor meer informatie [Snelle start: verbinden met gegevens in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).  

## <a name="to-add-includeprodshortincludesprodshortmd-as-a-data-source-in-power-bi-desktop"></a>[!INCLUDE[prodshort](includes/prodshort.md)] als gegevensbron toevoegen in Power BI Desktop

1. Kies in Power BI Desktop in het linkernavigatievenster **Gegevens ophalen**.
2. Kies op de pagina **Gegevens ophalen** **Online Services**, kies **Microsoft Dynamics 365 Business Central** en kies vervolgens de knop **Verbinden**.
3. Power BI geeft een wizard weer die u door het verbindingsproces begeleidt. U wordt gevraagd u aan te melden bij [!INCLUDE [prodshort](includes/prodshort.md)]. Selecteer **Aanmelden** en kies het account waaronder u zich wilt aanmelden. Dit moet hetzelfde account zijn als waarmee u zich aanmeldt bij [!INCLUDE [prodshort](includes/prodshort.md)].
4. Kies de knop **Verbinding maken** om door te gaan. De Power BI-wizard bevat een lijst met Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]-omgevingen, -bedrijven en -gegevensbronnen. Met deze gegevensbron worden alle webservices vertegenwoordigd die u hebt gepubliceerd vanuit elke tenant/elk bedrijf in [!INCLUDE [prodshort](includes/prodshort.md)].
5. U kunt ook een nieuwe webservice-URL in [!INCLUDE [prodshort](includes/prodshort.md)] maken met behulp van de actie **Gegevensset maken** op de pagina **Webservices** met de begeleide instelling **Rapportage instellen** of door de actie **Bewerken in Excel** in de lijsten te kiezen.
6. Geef de gegevens op die u aan uw gegevensmodel wilt toevoegen en kies vervolgens de knop **Laden**.
7. Herhaal de vorige stappen om aanvullende [!INCLUDE [prodshort](includes/prodshort.md)]- of andere gegevens aan uw Power BI-gegevensmodel toe te voegen.

> [!NOTE]  
> Zodra u met succes verbinding hebt gemaakt met [!INCLUDE [prodshort](includes/prodshort.md)], wordt u niet opnieuw gevraagd zich aan te melden.

Zodra de gegevens zijn geladen, worden deze in de rechternavigatie op de pagina weergegeven. Nu hebt u met succes een koppeling gemaakt naar uw [!INCLUDE [prodshort](includes/prodshort.md)]-gegevens en kunt u uw Power BI-rapport gaan maken.  

Voordat u uw rapport maakt, is het raadzaam dat u het [!INCLUDE [prodshort](includes/prodshort.md)]-themabestand importeert.  Het themabestand maakt een kleurenpalet, zodat u rapporten kunt maken met dezelfde kleurstijl als de [!INCLUDE [prodshort](includes/prodshort.md)]-apps zonder aangepaste kleuren te hoeven definiëren voor elk visueel element.

Zie voor meer informatie de [documentatie van Power BI](/power-bi/consumer/power-bi-consumer-landing/).

## <a name="see-also"></a>Zie ook

[Uw bedrijfsgegevens inschakelen voor Power BI](admin-powerbi.md)  
[Bedrijfsinformatie](bi.md)  
[Aan de slag](product-get-started.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Financiën](finance.md)  
[Snelle start: Uw gegevens verbinden in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
