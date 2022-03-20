---
title: KPI-webservices instellen en publiceren voor rekeningschema's
description: In dit onderwerp wordt beschreven hoe u de KPI-gegevens uit het rapportageschema weergeeft op basis van specifieke rapportageschema's.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.search.form: 103, 104, 197, 196, 195, 198, 490, 764, 765, 766
ms.date: 06/15/2021
ms.author: bholtorf
ms.openlocfilehash: b02b8fe9aeee685f65cf82ad66c9492d241c6711
ms.sourcegitcommit: 5a02f8527faecdffcc54f9c5c70cefe8c4b3b3f4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/04/2022
ms.locfileid: "8381310"
---
# <a name="set-up-and-publish-kpi-web-services-based-on-account-schedules"></a>KPI-webservices instellen en publiceren op basis van rekeningschema's
Op de pagina **Instellingen rapportageschema KPI-webservice** stelt u in hoe de KPI-gegevens van het rapportageschema worden weergegeven en op welke specifieke rapportageschema's de KPI's zijn gebaseerd. Wanneer u de knop **Webservice publiceren** kiest, worden de opgegeven gegevens van de rapportageschema-KPI toegevoegd aan de lijst met gepubliceerde webservices op de pagina **Webservices**.  

> [!NOTE]
> Wanneer u deze webservice gebruikt, worden sluitingsdatums niet opgenomen in uw dataset. Hiermee kunt u filters gebruiken in Power BI om verschillende tijdsperioden te analyseren.

## <a name="to-set-up-and-publish-a-kpi-web-service-that-is-based-on-account-schedules"></a>Een KPI-webservice instellen en publiceren die is gebaseerd op rekeningschema's  
1.  Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Instellingen rapportageschema KPI-webservice** in en kies vervolgens de gerelateerde koppeling.  
2.  Vul in het sneltabblad **Algemeen** de velden in, zoals in de volgende tabel is beschreven.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Start prognose waarden**|Geef op op welk tijdstip voorspelde waarden in de KPI-illustratie van het rapportageschema worden weergegeven.<br /><br /> De voorspelde waarden worden opgehaald uit het budget dat u hebt geselecteerd in het veld **Budget**. **Opmerking:** als u KPI's wilt verkrijgen die voorspelde cijfers na een bepaalde datum en werkelijke cijfers voor die datum tonen, kunt u het veld **Boeken toegest. vanaf** wijzigen op de pagina **Grootboekinstellingen**. Zie Boeken toegest. vanaf voor meer informatie.|  
    |**Budgetnaam**|Geef de naam op van het grootboekbudget dat voorspelde waarden aan de KPI-webservice van het rapportageschema levert.|  
    |**Periode**|Geef de periode op waarop de KPI-webservice van het rapportageschema is gebaseerd.|  
    |**Weergeven per**|Geef op in welk tijdsinterval de rapportageschema-KPI wordt weergegeven.|  
    |**Webservicenaam**|Geef de naam op van de KPI-webservice van het rapportageschema.<br /><br /> Deze naam wordt weergegeven in het veld **Servicenaam** op de pagina **Webservices**.|  

    Geef een of meer rapportageschema's op die u wilt publiceren als KPI-webservice volgens de instellingen die u in de vorige tabel hebt gemaakt.  

3.  Vul in het sneltabblad **Rapportageschema's** de velden in, zoals in de volgende tabel is beschreven.  

    |Veld|Omschrijving|  
    |---------------------------------|---------------------------------------|  
    |**Rapportageschema**|Geef het rekeningschema op waarop de KPI-webservice is gebaseerd.|  
    |**Omschrijving rapportageschema**|Geef de omschrijving op van het rekeningschema waarop de KPI-webservice is gebaseerd.|  

4.  Herhaal stap 3 voor alle rapportageschema's waarop u de webservice rapportageschema-KPI wilt baseren.  
5.  Als u het geselecteerde rapportageschema wilt weergeven of bewerken, kiest u op het sneltabblad **Rapportageschema** de actie **Rapportageschema bewerken**.  
6.  Om de gegevens van de rapportageschema KPI weer te geven die u hebt ingesteld, kiest u de actie **Rapportageschema KPI-webservice**.  
7.  Als u de KPI-webservice van het rapportageschema wilt publiceren, kiest u de actie **Webservice publiceren**. De webservice wordt toegevoegd aan de lijst met gepubliceerde webservices op de pagina **Webservices**.  

> [!NOTE]  
>  U kunt de KPI-webservice ook publiceren door te wijzen naar het paginaobject **Instellingen rapportageschema KPI-webservice** vanuit de pagina **Webservices**. Zie voor meer informatie [Een webservice publiceren](across-how-publish-web-service.md).  

## <a name="see-also"></a>Zie ook  
[Bedrijfsinformatie](bi.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Het grootboek en het rekeningschema](finance-general-ledger.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]