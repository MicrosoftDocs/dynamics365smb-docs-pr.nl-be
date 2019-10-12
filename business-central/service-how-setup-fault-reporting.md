---
title: Probleemrapportage instellen in CRM - Service | Microsoft Docs
description: Leer hoe u processen voor probleemrapportage instelt.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 8c3d770f1ee6e0c50439f5d0a4591c463b91631a
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2316200"
---
# <a name="set-up-fault-reporting"></a>Foutrapportage instellen
Met probleemrapportage kunt u standaarden voor het vastleggen van probleemgegevens voor service-items bepalen. U kunt bijvoorbeeld opgeven wat het probleem is, welke symptomen u ziet, wat de oorzaak van het probleem is en hoe het probleem moet worden verholpen.  

Met probleemcodes worden de veelvoorkomende serviceartikelproblemen of ondernomen acties met betrekking tot serviceartikelen beschreven. Afhankelijk van het niveau van probleemrapportage in het bedrijf, moet u wellicht probleemgebiedcodes en symptoomcodes instellen voordat u probleemcodes instelt. Met probleemgebieden worden gebieden van serviceartikelproblemen beschreven. Met probleemoorzaakcodes kan de oorzaak voor serviceartikelproblemen worden omschreven en kan zo nodig worden aangegeven of garantie- en contractkortingen moeten worden uitgesloten. U kunt bijvoorbeeld garantie- en contractkortingen uitsluiten wanneer de klant op enige manier verantwoordelijk is voor het serviceartikelprobleem. U wijst probleemoorzaakcodes toe aan serviceorders. Zie voor meer informatie [Werken aan servicetaken](service-how-to-work-on-service-tasks.md).  

## <a name="to-specify-the-overall-level-of-fault-reporting-to-use"></a>Het algemene probleemrapportageniveau voor gebruik opgeven
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Service-instellingen** in en kies vervolgens de gerelateerde koppeling.
2. Kies in het veld **Probleemrapportageniveau** een van de opties die in de volgende tabel worden beschreven.  

    |**Probleemniveau**|**Beschrijving**|  
    |------------|-------------|  
    |Geen | Er worden geen rapportagecodes gebruikt.|  
    |Probleem | De codes worden weergegeven in de tabel **Probleemcodes**. Deze codes duiden op problemen met serviceartikelen of acties die moeten worden ondernomen voor de serviceartikelen. U kunt gerelateerde codes groeperen in groepen van het type **Probleemgebiedcode**.|  
    |Probleem + symptoom. | U geeft een combinatie van codes op in de tabellen **Probleemcodes** en **Symptoomcodes**. Veelvoorkomende symptoomcodes kunnen bijvoorbeeld bestaan uit indicaties die een klant kan gebruiken om een probleem te beschrijven, zoals een geluid of kwaliteit.|  
    |Probleem + symptoom + gebied | U gebruikt probleem-, symptoom- en probleemgebiedcodes als een implementatie van IRIS, het internationale systeem voor reparatiecodes.|  

Ten slotte kunt u bij het instellen van probleemrapportage ook opgeven welke reparaties of oplossingen aan een probleem of defect zijn gekoppeld. U stelt dit in op de pagina **Relaties probleem-/oplossingscodes**, waar u combinaties van codes instelt voor de serviceartikelgroep van het serviceartikel van waaruit u het venster hebt geopend. Tevens wordt aangegeven hoe vaak elke combinatie voorkomt.

## <a name="to-create-fault-and-resolution-code-relationships"></a>Relaties tussen probleem- en oplossingscodes maken
<!--this needs to go in a working with topic-->
 Als u de veelgebruikte herstelmethoden voor bepaalde artikelproblemen wilt bekijken wanneer u service voor de artikelen uitvoert, moet u gegevens over relaties tussen probleem- en oplossingscodes instellen. Met de batchtaak **Rel. probleem-/oplossingscodes invoegen** kunt u alle combinaties van probleem- en oplossingscodes in geboekte serviceorders zoeken en deze vastleggen op de pagina **Rel. probleem-/oplossingscodes**.

1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rel. probleem-/oplossingscodes invoegen** in en kies vervolgens de gerelateerde koppeling.  
2. Voer datums in om de periode op te geven die u in de batchverwerking wilt opnemen.  
3. Schakel het selectievakje **Relatie op basis van serviceartikelgroep** in als u de relaties wilt rangschikken op serviceartikelgroep.  
4. Schakel het selectievakje **Handmatig ingevoegde records behouden** in als u de records wilt bewaren die u handmatig op de pagina **Rel. probleem-/oplossingscodes** hebt ingevoegd.  

## <a name="see-also"></a>Zie ook
[CRM - Service instellen](service-setup-service.md)  
[CRM - Service](service-service.md)  
