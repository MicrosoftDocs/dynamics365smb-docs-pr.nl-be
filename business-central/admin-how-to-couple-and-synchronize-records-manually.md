---
title: Records handmatig koppelen en synchroniseren | Microsoft Docs
description: Als een integratietabeltoewijzing wordt gesynchroniseerd, kunnen gegevens in alle records in een tabel in Business Central en Dynamics 365 Sales worden gesynchroniseerd die zijn gekoppeld.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 10/01/2020
ms.author: bholtorf
ms.openlocfilehash: d8140f71709208a271eff5c8de415b0e95736072
ms.sourcegitcommit: ddbb5cede750df1baba4b3eab8fbed6744b5b9d6
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2020
ms.locfileid: "3911417"
---
# <a name="couple-and-synchronize-records-manually"></a>Records handmatig koppelen en synchroniseren
In dit onderwerp wordt beschreven hoe u een of meer records in [!INCLUDE[d365fin](includes/d365fin_md.md)] koppelt aan records in Common Data Service of [!INCLUDE[crm_md](includes/crm_md.md)]. Door records te koppelen kunt u Common Data Service-informatie vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)]bekijken en andersom. Door de koppeling kunt u ook gegevens synchroniseren tussen de records. U kunt bestaande records koppelen of nieuwe records maken en koppelen.

> [!Note]
> Gegevens koppelen en synchroniseren is alleen beschikbaar als de systeembeheerder een verbinding tussen [!INCLUDE[d365fin](includes/d365fin_md.md)] en Common Data Service of [!INCLUDE[crm_md](includes/crm_md.md)] heeft gemaakt. Een snelle manier om dat te controleren is de **Klant** -kaart te openen en de actie **Koppeling instellen** te zoeken. Als de actie beschikbaar is, zijn de apps verbonden.   

## <a name="video-example"></a>Videovoorbeeld

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a>Een record koppelen  
1.  In [!INCLUDE[d365fin](includes/d365fin_md.md)] opent u de kaart voor de record die moeten worden gekoppeld. Bijvoorbeeld de klant- of contactkaart.  

    U kunt ook slechts de lijstpagina openen en de record selecteren die u wilt koppelen.  

2.  Kies de actie **Koppeling instellen** .  
3.  Vul de velden in en kies de knop **OK** .  

## <a name="to-synchronize-a-single-record"></a>Eén record synchroniseren  
1.  In [!INCLUDE[d365fin](includes/d365fin_md.md)] opent u de kaart voor de record die moeten worden gekoppeld. Bijvoorbeeld de klant- of contactkaart.  
2.  Kies de actie **Nu synchroniseren** .  
3.  Als een record in één richting kan worden gesynchroniseerd, selecteert u de optie die de richting van de gegevensupdate opgeeft, en kiest u vervolgens **OK** .  

## <a name="to-synchronize-a-single-record-from-crm_md"></a>Eén record synchroniseren vanuit [!INCLUDE[crm_md](includes/crm_md.md)]  
1.  In [!INCLUDE[crm_md](includes/crm_md.md)] opent u het formulier voor de record die u wilt koppelen. Bijvoorbeeld het formulier Accountkaart of Contactkaart.  
2.  Kies de actie **[!INCLUDE[d365fin](includes/d365fin_md.md)]** op het lint om een record automatisch te openen en te koppelen.

> [!Note]
> U kunt één record alleen automatisch synchroniseren vanuit [!INCLUDE[crm_md](includes/crm_md.md)] wanneer **Alleen gekoppelde records synchr.** is uitgeschakeld en de synchronisatierichting is ingesteld op Bidirectioneel of Van integratietabel op de pagina **Toewijzing van integratietabel** voor de record. Zie voor meer informatie [De tabellen en velden toewijzen voor synchronisatie](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).     

## <a name="to-synchronize-multiple-records"></a>Meerdere records synchroniseren  
1.  Open in [!INCLUDE[d365fin](includes/d365fin_md.md)] de lijstpagina voor de record, zoals lijstpagina Klanten of Contact.  
2.  Selecteer de records die u wilt synchroniseren en kies vervolgens de actie **Nu synchroniseren** .  
3.  Als records in één richting kunnen worden gesynchroniseerd, selecteert u de optie die de richting opgeeft, en kiest u vervolgens **OK** .  

## <a name="see-also"></a>Zie ook  
[Microsoft Dynamics 365 Sales gebruiken vanuit Business Central](marketing-integrate-dynamicscrm.md)
