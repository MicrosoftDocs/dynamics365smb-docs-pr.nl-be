---
title: Resourcetoewijzing instellen | Microsoft Docs
description: Leer hoe u er met het systeem voor kunt zorgen dat u iemand toewijst die over de vereiste vaardigheden beschikt om een service te bieden.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: resource, skill, service, zones
ms.date: 10/01/2019
ms.author: bholtorf
ms.openlocfilehash: ee97797c9dabab188f1e6a2bbf2cb1f9846e7321
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2316176"
---
# <a name="set-up-resource-allocation"></a>Resourcetoewijzing instellen
Om ervoor te zorgen dat een servicetaak goed wordt uitgevoerd, is het belangrijk een resource te vinden die gekwalificeerd is om het werk uit te voeren. U kunt [!INCLUDE[d365fin](includes/d365fin_md.md)] zo instellen dat het eenvoudig is om iemand toe te wijzen die over de juiste bekwaamheden voor het project beschikt. In [!INCLUDE[d365fin](includes/d365fin_md.md)] noemen we dit _resourcetoewijzing_. U kunt resources toewijzen op basis van hun vaardigheden, beschikbaarheid en locatie (of ze zich in dezelfde serviceregio als de klant bevinden). 

U moet het volgende instellen om resourcetoewijzing te gebruiken:  
  
* De benodigde bekwaamheden om serviceartikelen te repareren en te onderhouden. U wijst deze toe aan serviceartikelen en resources.  
* Geografische gebieden, regio's, die u voor de markt definieert. Dit kunnen bijvoorbeeld Oost, West, Centraal, enzovoort zijn. U wijst deze toe aan klanten en resources.  
* Of er resourcebekwaamheden en -regio's moeten worden weergegeven en of er een waarschuwing moet worden weergegeven als iemand een ongeschikte resource kiest of een resource die zich niet in de klantregio bevindt.  

## <a name="to-set-up-skills"></a>Bekwaamheden instellen
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Bekwaamheden** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-skills-to-service-items-and-resources"></a>Bekwaamheden toewijzen aan serviceartikelen en resources
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Serviceartikelen** of **Resources** in en kies vervolgens de gerelateerde koppeling.  
2. Open de kaart voor het serviceartikel of de resource en kies een van de volgende opties:  
  
    * Voor serviceartikelen kiest u **Resourcebekwaamheden**.  
    * Voor resources kiest u **Bekwaamheden**.  

## <a name="to-set-up-zones"></a>Regio's instellen
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Zones** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de benodigde velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-zones-to-customers-and-resources"></a>Regio's toewijzen aan klanten en resources 
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klanten** of **Resources** in en kies vervolgens de gerelateerde koppeling.  
2. Open de kaart voor het serviceartikel of de resource en kies een van de volgende opties:  
  
    * Voor klanten kiest u een regio in het veld **Serviceregiocode**.  
    * Voor resources kiest u de actie **Serviceregio's**.  

## <a name="to-specify-what-to-show-when-a-resource-is-chosen"></a>Opgeven wat er moet worden weergegeven wanneer een resource is gekozen
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Service-instellingen** in en kies vervolgens de gerelateerde koppeling. 
2. Kies in het veld **Optie resourcebekwaamheden** een van de opties die in de volgende tabel worden beschreven.  
  
    |**Optie**|**Beschrijving**|  
    |------------|-------------|  
    |Code getoond | Alleen de code wordt weergegeven.|  
    |Waarschuwing getoond | De informatie wordt weergegeven en er wordt een waarschuwing weergegeven als u een resource kiest die niet geschikt is.|  
    |Niet gebruikt. | Geef deze gegevens niet weer.|  

## <a name="to-update-resource-capacity"></a>Resourcecapaciteit bijwerken  
U kunt de resourcecapaciteit desgewenst wijzigen.  
  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Resourcecapaciteit** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de resource en kies vervolgens de actie **Capaciteit instellen**.  
3. Breng de wijzigingen aan en kies **Capaciteit bijwerken**.  

## <a name="to-update-skills-for-items-service-items-or-service-item-groups"></a>Bekwaamheden voor artikelen, serviceartikelen of serviceartikelgroepen bijwerken
Wilt u de bekwaamheidscodes wijzigen die aan artikelen zijn toegewezen, bijvoorbeeld van **PC** in **STUKS**, dan kunt u dit voor een artikel, serviceartikel of alle items in een serviceartikelgroep doen.  
  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Artikelen**, **Serviceartikel** of **Serviceartikelgroep** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de entiteit die u wilt bijwerken en kies vervolgens de actie **Resourcebekwaamheden**.  
3. Op de regel met de code die u wilt wijzigen, selecteert u de betreffende bekwaamheidscode in het veld **Bekwaamheidscode**.  
4.  Als er serviceartikelen aan het artikel zijn gekoppeld, wordt er een dialoogvenster geopend met de volgende twee opties:  
  
    * De bekwaamheidscodes wijzigen in de geselecteerde waarde: selecteer deze optie als u de oude bekwaamheidscode voor alle gerelateerde serviceartikelen wilt vervangen door de nieuwe code.  
    * De bekwaamheidscodes verwijderen of hun relatie bijwerken: selecteer deze optie als u alleen voor dit artikel de bekwaamheidscode wilt wijzigen. De bekwaamheidscode voor de gerelateerde serviceartikelen wordt opnieuw toegewezen, dat wil zeggen dat het veld **Toegewezen vanuit** wordt bijgewerkt.  
  
## <a name="see-also"></a>Zie ook
[Resources toewijzen](service-how-to-allocate-resources.md)  
[Service- en werkuren instellen](service-how-setup-work-service-hours.md)  
[Foutrapportage instellen](service-how-setup-fault-reporting.md)  
[Codes voor standaardservices instellen](service-how-setup-service-coding.md)  
 

