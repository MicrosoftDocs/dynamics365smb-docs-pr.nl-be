---
title: KPI-webservices instellen en publiceren op basis van rekeningschema's | Microsoft Docs
description: In het venster **Instellingen rapportageschema KPI-webservice** stelt u in hoe de KPI-gegevens van het rapportageschema worden weergegeven en op welke specifieke rapportageschema's de KPI's zijn gebaseerd.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 57f36592105faf0801864e034c3b930ae196ee62
ms.contentlocale: nl-be
ms.lasthandoff: 01/30/2018

---
# <a name="set-up-and-publish-kpi-web-services-based-on-account-schedules"></a>KPI-webservices instellen en publiceren op basis van rekeningschema's
In het venster **Instellingen rapportageschema KPI-webservice** stelt u in hoe de KPI-gegevens van het rapportageschema worden weergegeven en op welke specifieke rapportageschema's de KPI's zijn gebaseerd. Wanneer u de knop **Webservice publiceren** kiest, worden de opgegeven gegevens van de rapportageschema-KPI toegevoegd aan de lijst met gepubliceerde webservices in het venster **Webservices**.  

## <a name="to-set-up-and-publish-a-kpi-web-service-that-is-based-on-account-schedules"></a>Een KPI-webservice instellen en publiceren die is gebaseerd op rekeningschema's  

1.  Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Instellingen rapportageschema KPI-webservice** in en kies vervolgens de gerelateerde koppeling.  
2.  Vul in het sneltabblad **Algemeen** de velden in, zoals in de volgende tabel is beschreven.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Start prognose waarden**|Geef op op welk tijdstip voorspelde waarden in de KPI-illustratie van het rapportageschema worden weergegeven.<br /><br /> De voorspelde waarden worden opgehaald uit het budget dat u hebt geselecteerd in het veld **Budget**. **Opmerking:** als u KPI's wilt verkrijgen die voorspelde cijfers na een bepaalde datum en werkelijke cijfers voor die datum tonen, kunt u het veld **Boeken toegest. vanaf** wijzigen in het venster **Grootboekinstellingen**. Zie Boeken toegest. vanaf voor meer informatie.|  
    |**Budgetnaam**|Geef de naam op van het grootboekbudget dat voorspelde waarden aan de KPI-webservice van het rapportageschema levert.|  
    |**Periode**|Geef de periode op waarop de KPI-webservice van het rapportageschema is gebaseerd.|  
    |**Weergeven per**|Geef op in welk tijdsinterval de rapportageschema-KPI wordt weergegeven.|  
    |**Webservicenaam**|Geef de naam op van de KPI-webservice van het rapportageschema.<br /><br /> Deze naam wordt weergegeven in het veld **Servicenaam** in het venster **Webservices**.|  

    U kunt nu doorgaan om een of meer rapportageschema's op te geven die u wilt publiceren als KPI-webservice volgens de instellingen die u in de vorige tabel hebt gemaakt.  

3.  Vul in het sneltabblad **Rapportageschema's** de velden in, zoals in de volgende tabel is beschreven.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Rapportageschema**|Geef het rekeningschema op waarop de KPI-webservice is gebaseerd.|  
    |**Omschrijving rapportageschema**|Geef de omschrijving op van het rekeningschema waarop de KPI-webservice is gebaseerd.|  

4.  Herhaal stap 3 voor alle rapportageschema's waarop u de webservice rapportageschema-KPI wilt baseren.  
5.  Als u het geselecteerde rapportageschema wilt weergeven of bewerken, kiest u op het sneltabblad **Rapportageschema** de actie **Rapportageschema bewerken**.  
6.  Om de gegevens van de rapportageschema KPI weer te geven die u hebt ingesteld, kiest u de actie **Rapportageschema KPI-webservice**.  
7.  Als u de KPI-webservice van het rapportageschema wilt publiceren, kiest u de actie **Webservice publiceren**. De webservice wordt toegevoegd aan de lijst met gepubliceerde webservices in het venster **Webservices**.  

> [!NOTE]  
>  U kunt de KPI-webservice ook publiceren door te wijzen naar het paginaobject **Instellingen rapportageschema KPI-webservice** vanuit het venster **Webservices**. Zie voor meer informatie [Een webservice publiceren](across-how-publish-web-service.md).  

## <a name="see-also"></a>Zie ook  
[Bedrijfsinformatie](bi.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Het grootboek en het rekeningschema](finance-general-ledger.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

