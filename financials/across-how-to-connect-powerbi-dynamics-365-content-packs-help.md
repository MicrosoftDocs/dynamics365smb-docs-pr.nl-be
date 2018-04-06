---
title: Power BI verbinden met Finance and Operations, Business edition | Microsoft Docs
description: Inzicht, bedrijfsinformatie en KPI's krijgen uit uw gegevens van Finance and Operations, Business edition is gemakkelijk met Power BI en de inhoudspakketten van Finance and Operations, Business edition.
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: account schedule, analysis, reporting, financial report, business intelligence, KPI
ms.date: 02/05/2018
ms.author: solsen
ms.translationtype: HT
ms.sourcegitcommit: b4e2e7bc1c2622d329c73ae5bf47b4accff10aa8
ms.openlocfilehash: aff8d95b13f795fa12d3146e5613712fb3baf9b4
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="connecting-power-bi-to-finance-and-operations-business-edition-content-packs"></a>Power BI verbinden met inhoudspakketten van Finance and Operations, Business edition
Inzicht krijgen in uw Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-gegevens is gemakkelijk met Power BI en de inhoudspakketten van Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. Power BI haalt uw gegevens op en maakt vervolgens een kant-en-klaar dashboard en rapporteert op basis van die gegevens.

> [!NOTE]  
>  U moet een geldig account bij Dynamics 365 en Power BI hebben. Ook moet u [Power BI Desktop](https://powerbi.microsoft.com/en-us/desktop/) downloaden.  
>  Voor Power BI-inhoudspakketten zijn machtigingen vereist voor de tabellen waaruit de gegevens worden opgehaald. Meer details over de vereisten worden verderop beschreven.  

## <a name="how-to-connect"></a>Verbinding maken
1. Selecteer **Gegevens ophalen** onder in het linkernavigatiedeelvenster.  
![Navigeren om gegevens op te halen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-get-data.png)
2. Selecteer **Ophalen** in het vak **Diensten**. Hierdoor wordt een venster geopend met de **AppSource** en **Apps voor Power BI-apps**.  
![Inhoudspakketten kiezen uit online services](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-online-services-get.png)
3. Selecteer **Apps** op het tabblad **Apps voor Power BI-apps** en kies het inhoudspakket van **Microsoft Dynamics 365 for Finance and Operations** dat u wilt gebruiken, Selecteer vervolgens **Nu ophalen**.  
![Selecteer Dynamics 365 for Finance and Operations, Business edition en selecteer Nu ophalen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-dynamics365-for-financials-get-it-now.png)
4. Voer wanneer daarom wordt gevraagd de naam van *uw bedrijf* in [!INCLUDE[d365fin_md](includes/d365fin_long_md.md)]. Dit is niet de weergavenaam.  
![Selecteer Dynamics 365 for Finance and Operations, Business edition en selecteer Nu ophalen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-connect-to-d365-finance-and-operations-crm.png)
5. Nadat verbinding is gemaakt, worden automatisch een dashboard, rapport en gegevensset geladen in uw Power BI-werkruimte. Wanneer dit is voltooid, worden de tegels bijgewerkt met gegevens uit uw account.
![Selecteer Dynamics 365 for Finance and Operations, Business edition en selecteer Nu ophalen](./media/across-how-to-connect-powerbi-d365-content-packs/powerbi-workspace-dashboard-report-dataset.png)

## <a name="what-now"></a>Wat nu?

- Probeer [een vraag te stellen in het vraag- en antwoordvak](https://docs.microsoft.com/en-us/power-bi/service-q-and-a) boven aan het dashboard.  
- [Wijzig de tegels](https://docs.microsoft.com/en-us/power-bi/service-dashboard-edit-tile) in het dashboard.  
- [Selecteer een tegel](https://docs.microsoft.com/en-us/power-bi/service-dashboard-tiles) om het onderliggende rapport te openen.  
- Terwijl uw gegevensset wordt gepland om dagelijks te worden vernieuwd, kunt u het vernieuwingsschema wijzigen of op verzoek proberen te vernieuwen met **Nu vernieuwen**.

## <a name="system-requirements"></a>Systeemvereisten
Als u de gegevens [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] in Power BI wilt importeren, moet u machtigingen hebben voor de webservices die worden gebruikt om gegevens op te halen. De webservices die voor elk inhoudspakket vereist zijn omvatten:

**Microsoft Dynamics 365 for Finance and Operations, Business edition – CRM**
- SalesOpportunities
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 for Finance and Operations, Business edition – Verkoop**
- ItemSalesbyCustomer
- SalesDashboard
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 for Finance and Operations, Business edition – Financiën**
- PowerBIFinance
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 for Finance and Operations, Business edition – Projecten**
- Projectoverzicht
- Projectplanningsregels
- Projecttaakregels

**Microsoft Dynamics 365 for Finance and Operations, Business edition - Klantenlijst**
- ItemSalesbyCustomer
- Power_BI_Item_Purchase_List
- Power_BI_Item_Sales_List
- SalesDashboard
- Power_BI_Customer_List
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 for Finance and Operations, Business edition - Artikellijst**
- ItemSalesbyCustomer
- Power_BI_Item_Purchase_List
- Power_BI_Item_Sales_List
- Artikelen
- SalesDashboard
- ExcelTemplateViewCompany

**Microsoft Dynamics 365 for Finance and Operations, Business edition - Leverancierslijst**
- ItemSalesbyCustomer
- Power_BI_Item_Purchase_List
- Power_BI_Item_Sales_List
- Artikelen
- SalesDashboard
- Power_BI_Customer_List
- ItemSalesbyCustomer
- Power_BI_Vendor_List
- ExcelTemplateViewCompany

## <a name="web-services"></a>Webservices
Een eenvoudige manier om de webservices te vinden is te zoeken naar webservices in [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]. In de lijst moet u ervoor zorgen het vakje Publiceren is gemarkeerd voor de hierboven genoemde webservices.

## <a name="troubleshooting"></a>Problemen oplossen
Het dashboard van Power BI gebruikt de gepubliceerde webservices die hierboven worden genoemd en bevat gegevens van het demobedrijf of uw eigen bedrijf als u gegevens importeert uit uw huidige financiële oplossing. Als er echter iets verkeerd gaat, biedt deze sectie een oplossing voor de meest voorkomende problemen.

### <a name="incorrect-company-name"></a>Onjuiste bedrijfsnaam  
Een veel voorkomende fout is de weergavenaam van het bedrijf in te voeren in plaats van de bedrijfsnaam. Als u de bedrijfsnaam wilt vinden, zoekt u naar **Bedrijven**. Gebruik vervolgens het veld **Naam** wanneer u uw bedrijfsnaam invoert.

### <a name="incorrect-user-name-and-password"></a>Onjuiste gebruikersnaam en wachtwoord  
De gebruikersnaam en het wachtwoord die worden gebruikt om verbinding te maken, zijn hetzelfde als wat wordt gebruikt om verbinding te maken met uw Microsoft Office 365-account.  

De inhoudspakketten vereisen ook dat u een Microsoft-[!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)] hebt. Zodra u uw aanmeldingsgegevens invoert, worden eventuele Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-tenants waartoe u toegang hebt, automatisch gevonden. Als u geen gelicentieerd of proef Microsoft [!INCLUDE[d365fin_long_md](includes/d365fin_long_md.md)]-account hebt, wordt een foutbericht weergegeven.

### <a name="the-key-didnt-match-any-rows-in-the-table"></a>De sleutel kwam met geen rijen uit de tabel overeen
Als u niet een geldige bedrijfsnaam invoert tijdens het verbindingsproces, kunt u de foutmelding "De sleutel kwam met geen rijen uit de tabel overeen" krijgen. Geef de juiste bedrijfsnaam op en probeer opnieuw verbinding te maken.

## <a name="see-also"></a>Zie ook
[Aan de slag met Power BI](https://docs.microsoft.com/en-us/power-bi/service-get-started)  
[Power BI - Basisconcepten](https://docs.microsoft.com/en-us/power-bi/service-basic-concepts)
[Bedrijfsinformatie](bi.md)  
[Welkom bij [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Bedrijfsgegevens importeren uit andere financiële systemen](upload-data.md)  
[Instellen van [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Financiën](finance.md)  
[Rapportage instellen voor [!INCLUDE[d365fin](includes/d365fin_md.md)] in Power BI](across-how-use-financials-data-source-powerbi.md)  

