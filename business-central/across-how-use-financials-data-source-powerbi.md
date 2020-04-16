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
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: 4f140303f037ea4a914cba1ded44fd453bcdfabb
ms.sourcegitcommit: 88e4b30eaf6fa32af0c1452ce2f85ff1111c75e2
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3187904"
---
# <a name="using-prodlong-as-power-bi-data-source-for-building-reports"></a>[!INCLUDE [prodlong](includes/prodlong.md)] gebruiken als Power BI-gegevensbron voor het maken van rapporten

U kunt uw [!INCLUDE[prodlong](includes/prodlong.md)]-gegevens als gegevensbron beschikbaar maken in Power BI en krachtige rapporten maken met de status van uw bedrijf.  

U moet een geldig account bij [!INCLUDE[prodshort](includes/prodshort.md)] en Power BI hebben. U moet ook [Power BI Desktop](https://powerbi.microsoft.com/desktop/) downloaden. Zie voor meer informatie [Snelle start: verbinden met gegevens in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data).  

## <a name="to-add-prodshort-as-a-data-source-in-power-bi-desktop"></a>[!INCLUDE[prodshort](includes/prodshort.md)] als gegevensbron toevoegen in Power BI Desktop

1. Kies in Power BI Desktop in het linkernavigatievenster **Gegevens ophalen**.
2. Kies op de pagina **Gegevens ophalen** **Online Services**, kies **Microsoft Dynamics 365 Business Central** en kies vervolgens de knop **Verbinden**.
3. Power BI geeft een wizard weer die u door het verbindingsproces begeleidt, inclusief aanmelden bij [!INCLUDE [prodshort](includes/prodshort.md)]. Kies **Aanmelden** en kies vervolgens het relevante account. Gebruik hetzelfde account als waarmee u zich aanmeldt bij [!INCLUDE [prodshort](includes/prodshort.md)].
4. Kies de knop **Verbinding maken** om door te gaan. De wizard Power BI bevat een lijst met Microsoft [!INCLUDE[d365fin](includes/d365fin_md.md)]-omgevingen, -bedrijven en -gegevensbronnen. Met deze gegevensbronnen worden alle webservices vertegenwoordigd die u hebt gepubliceerd vanuit [!INCLUDE [prodshort](includes/prodshort.md)].

    U kunt ook een nieuwe webservice-URL maken in [!INCLUDE [prodshort](includes/prodshort.md)]. Kies een van de volgende methoden:

      - De actie **Gegevensset maken** op de pagina **Webservices** gebruiken
      - De begeleide instelling **Rapportage instellen** gebruiken
      - De actie **Bewerken in Excel** kiezen in een lijst

5. Geef de gegevens op die u aan uw gegevensmodel wilt toevoegen en kies vervolgens de knop **Laden**.
6. Herhaal de vorige stappen om aanvullende [!INCLUDE [prodshort](includes/prodshort.md)]- of andere gegevens aan uw Power BI-gegevensmodel toe te voegen.

> [!NOTE]  
> Zodra u met succes verbinding hebt gemaakt met [!INCLUDE [prodshort](includes/prodshort.md)], wordt u niet opnieuw gevraagd zich aan te melden.

Zodra de gegevens zijn geladen, ziet u deze in de rechternavigatie op de pagina. U hebt met succes een koppeling gemaakt naar uw [!INCLUDE [prodshort](includes/prodshort.md)]-gegevens en kunt u uw Power BI-rapport gaan maken.  

Voordat u uw rapport maakt, is het raadzaam dat u het [!INCLUDE [prodshort](includes/prodshort.md)]-themabestand importeert.  Het themabestand maakt een kleurenpalet, zodat u rapporten kunt maken met dezelfde kleurstijl als de [!INCLUDE [prodshort](includes/prodshort.md)]-apps zonder aangepaste kleuren te hoeven definiëren voor elk visueel element.

Zie voor meer informatie de [documentatie van Power BI](/power-bi/consumer/).

## <a name="see-related-training-at-microsoft-learn"></a>Zie Gerelateerde training op [Microsoft Learn](/learn/modules/configure-powerbi-excel-dynamics-365-business-central/index)

## <a name="see-also"></a>Zie ook

[Uw bedrijfsgegevens inschakelen voor Power BI](admin-powerbi.md)  
[Bedrijfsinformatie](bi.md)  
[Aan de slag](product-get-started.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](across-import-data-configuration-packages.md)  
[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Financiën](finance.md)  
[Snelle start: Uw gegevens verbinden in Power BI Desktop](/power-bi/desktop-quickstart-connect-to-data)  
