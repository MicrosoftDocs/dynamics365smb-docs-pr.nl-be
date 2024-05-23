---
title: Voorraad- en magazijnrapporten en analyses
description: 'Bekijk welke voorraad- en magazijnrapporten en analyses beschikbaar zijn in de standaardversie van Business Central, zodat u uw bedrijf kunt volgen.'
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: reporting
ms.search.form: 'Report_707, Report_716, Report_813, Report_1001, Report_5807, Report_5808, Report_5809, Report_7313, Report_7319, Report_7320'
ms.date: 03/21/2024
ms.custom: bap-template
ms.service: dynamics-365-business-central
---
# <a name="inventory-and-warehouse-reports-and-analytics"></a>Voorraad- en magazijnrapporten en analyses

Voorraad- en magazijnrapportage in [!INCLUDE [prod_short](includes/prod_short.md)] stelt voorraad- en zakelijke professionals in staat om inzichten en statistieken te krijgen over huidige en vroegere voorraad- en magazijnactiviteiten.  

## <a name="reports"></a>Rapporten

[!INCLUDE [inventory_WMS_reports](includes/inventory-WMS-reports-include.md)]

## <a name="tasks"></a>Taken

In de volgende artikelen worden enkele van de belangrijkste taken beschreven voor het analyseren van de toestand van uw bedrijf:

* [Analyserapporten maken](bi-how-create-analysis-views-reports.md)  
* [De beschikbaarheid van artikelen weergeven](inventory-how-availability-overview.md)

## <a name="print-and-scan-barcodes"></a>Barcodes afdrukken en scannen

Het gebruik van barcodes kan u helpen uw inkomende, uitgaande en interne magazijnprocessen te stroomlijnen. 

[!INCLUDE [barcode-mobile-app](includes/barcode-mobile-app.md)]

Nadat u de app heeft geïnstalleerd, kunt u de actie **Label afdrukken** gebruiken om 1D- en 2D-barcodes af te drukken vanaf de pagina's in de volgende tabel.

|Pagina  |Veldwaarden die barcodes kunnen bevatten  |
|---------|---------|
|Artikelen, Artikelkaart     |Artikelnr., Omschrijving en GTIN         |
|Artikelreferentielijst, Artikelreferentie     |Artikelnr., Beschrijving, Maateenheid en Referentienr.         |
|Gegevensoverzicht lotnr., Lotnr.-label     |Artikelnr., Beschrijving en Lotnummer       |
|SN-label     |Nr., Beschrijving en Serienummer         |

> [!NOTE]
> Sommige printers en barcode/QR-code-indelingen vereisen een specifieke implementatie. Mogelijk moet u een andere Word-sjabloon uploaden of het rapport klonen om uw eigen aangepaste versie te maken.


## <a name="explore-inventory-reports-with-report-explorer"></a>Voorraadrapporten verkennen met Rapportverkenner

Om een overzicht te krijgen van de beschikbare rapporten voor voorraad kiest u **Alle rapporten** op uw startpagina. Met deze actie gaat u naar de Rolverkenner, die wordt gefilterd op de functies in de optie **Rapport en analyse**. Kies onder het kopje **Verkoop en marketing** **Verkennen**.

:::image type="content" source="media/report-explorer-sales.png" alt-text="Voorbeeld van rapporten over het financiële rolcentrum." lightbox="media/report-explorer-sales.png":::

Ga voor meer informatie naar [Rapporten zoeken met de Rolverkenner](ui-role-explorer.md).


## <a name="see-also"></a>Zie ook

[Adhoc-analyse van voorraadgegevens](ad-hoc-analysis-inventory.md)  
[Overzicht van voorraadanalyse](inventory-analytics-overview.md)   
[Voorraad instellen](inventory-setup-inventory.md)  
[Voorraad](inventory-manage-inventory.md)  
[Magazijnbeheer instellen](warehouse-setup-warehouse.md)  
[Overzicht van magazijnbeheer](design-details-warehouse-management.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
