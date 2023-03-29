---
title: KPI-webservices instellen en publiceren op basis van financiële rapporten
description: In dit artikel wordt beschreven hoe u de KPI-gegevens uit het financieel rapport weergeeft op basis van specifieke financiële rapporten.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.service: dynamics365-business-central
ms.topic: how-to
ms.date: 12/16/2022
ms.custom: bap-template
ms.search.form: '103, 104, 108, 195, 196, 197, 198, 489, 490, 764, 765, 766'
---
# KPI-webservices instellen en publiceren op basis van financiële rapporten

Op de pagina **Instellingen KPI-webservice financiële rapporten** stelt u in hoe de KPI-gegevens (Key Performance Indicator) van het financiële rapport worden weergegeven en op welke specifieke financiële rapporten de KPI's zijn gebaseerd. Wanneer u **Webservice publiceren** kiest, worden de opgegeven KPI-gegevens voor financiële rapporten toegevoegd aan de lijst met gepubliceerde webservices op de pagina **Webservices**.

> [!NOTE]
> Wanneer u deze webservice gebruikt, worden sluitingsdatums niet opgenomen in uw dataset. U kunt filters gebruiken in Power BI om verschillende tijdsperioden te analyseren.

## KPI-webservices instellen en publiceren op basis van financiële rapporten
  
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Instellingen financieel rapport KPI-webservice** in en kies vervolgens de gerelateerde koppeling.
2. Vul de velden op het sneltabblad **Algemeen** in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Vul de velden van het sneltabblad **Rijdefinities** in.
4. Herhaal stap 3 voor alle financiële rapporten waarop u de KPI-webservice voor financiële rapporten wilt baseren.  
5. Als u het geselecteerde financiële rapport wilt weergeven of bewerken, kiest u op het sneltabblad **Rijdefinities** de actie **Rijdefinitie bewerken**.
6. Om de gegevens van de financieel rapport KPI weer te geven die u hebt ingesteld, kiest u de actie **Financieel rapport KPI-webservice**.
7. Als u de KPI-webservice van het financieel rapport wilt publiceren, kiest u de actie **Webservice publiceren**.

U kunt nu financiële rapporten maken in Power BI op basis van de webservice of services die u heeft gemaakt.

> [!NOTE]  
> U kunt de KPI-webservice ook publiceren door te wijzen naar het paginaobject **Instellingen financieel rapport KPI-webservice** vanuit de pagina **Webservices**. Voor meer informatie: [Een webservice publiceren](across-how-publish-web-service.md).

## Zie ook

[Financiële bedrijfsinformatie](bi.md)  
[Financiën](finance.md)  
[Financiën instellen](finance-setup-finance.md)  
[Het grootboek en het rekeningschema](finance-general-ledger.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
