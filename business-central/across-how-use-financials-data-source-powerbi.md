---
title: Rapportage voor Business Central instellen in Power BI | Microsoft Docs
description: Maak uw gegevens als gegevensbron in Power BI beschikbaar en maak krachtige rapporten met de status van uw bedrijf.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: business intelligence, KPI, Odata, Power App, SOAP, analysis
ms.date: 10/01/2018
ms.author: edupont
ms.openlocfilehash: ca4c27eaa1fe66e9bee678d6ec197fee7b928bdd
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/08/2019
ms.locfileid: "816794"
---
# <a name="using-included365finlongmdincludesd365finlongmdmd-as-power-bi-data-source-for-building-reports"></a>[!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] gebruiken als Power BI-gegevensbron voor het maken van rapporten
U kunt uw [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-gegevens als gegevensbron beschikbaar maken in Power BI en krachtige rapporten maken met de status van uw bedrijf.  

U moet een geldig account bij [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] en Power BI hebben. U moet ook [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) downloaden.  

## <a name="to-add-included365finlongmdincludesd365finlongmdmd-as-a-data-source-in-power-bi-desktop"></a>[!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] als gegevensbron toevoegen in Power BI Desktop
1. Kies in Power BI Desktop in het linkernavigatievenster **Gegevens ophalen**.
2. Kies op de pagina **Gegevens ophalen** **Online Services**, kies **Microsoft Dynamics 365 Business Central** en kies vervolgens de knop **Verbinden**.
3. Power BI geeft een wizard weer die u door het [verbindingsproces](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md) begeleidt. U wordt gevraagd u aan te melden voor de service. Selecteer **Aanmelden** en kies het account waaronder u zich wilt aanmelden. Dit moet hetzelfde account zijn als waarmee u zich aanmeldt bij [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].
4. Kies de knop **Verbinding maken** om door te gaan. De Power BI-wizard bevat een lijst met Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]-bedrijven en -gegevensbronnen. Met deze gegevensbron worden alle webservices vertegenwoordigd die u hebt gepubliceerd vanuit elk bedrijf in Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)].
5. U kunt ook een nieuwe webservice-URL in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] maken met behulp van de actie **Gegevensset maken** op de pagina **Webservices** met de begeleide instelling **Rapportage instellen** of door de actie **Bewerken in Excel** in de lijsten te kiezen.
6. Geef de gegevens op die u aan uw gegevensmodel wilt toevoegen en kies vervolgens de knop **Laden**.
7. Herhaal de vorige stappen om aanvullende Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-gegevens of andere gegevens aan uw Power BI-gegevensmodel toe te voegen.

> [!NOTE]  
> Zodra u met succes verbinding hebt gemaakt met Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)], wordt u niet opnieuw gevraagd zich aan te melden.

Zodra de gegevens zijn geladen, worden deze in de rechternavigatie op de pagina weergegeven. Nu hebt u met succes een koppeling gemaakt naar uw Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-gegevens en kunt u uw Power BI-rapport gaan maken. 

Voordat u uw rapport maakt, is het raadzaam dat u het Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-themabestand importeert.  Het themabestand maakt een kleurenpalet, zodat u rapporten kunt maken met dezelfde kleurstijl als de Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-inhoudspakketten zonder aangepaste kleuren te hoeven definiëren voor elk visueel element.

Zie voor meer informatie de [documentatie van Power BI](https://powerbi.microsoft.com/documentation/powerbi-landing-page/).

## <a name="see-also"></a>Zie ook
[Bedrijfsinformatie](bi.md)  
[Aan de slag](product-get-started.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Instellen [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)   
[Financiën](finance.md)  
[Power BI verbinden met [!INCLUDE[d365fin](includes/d365fin_md.md)]](across-how-to-connect-powerbi-dynamics-365-content-packs-help.md)  
