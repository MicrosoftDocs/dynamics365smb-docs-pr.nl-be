---
title: Records handmatig koppelen en synchroniseren | Microsoft Docs
description: Als een integratietabeltoewijzing wordt gesynchroniseerd, kunnen gegevens in alle records in een tabel in Business Central en Dynamics 365 for Sales worden gesynchroniseerd die zijn gekoppeld.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: crm, sales, couple, decouple, synchronize
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 36f1a0fe8c50744d9ce13d1e6c3c899f4ceaf5e4
ms.sourcegitcommit: bd78a5d990c9e83174da1409076c22df8b35eafd
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 03/31/2019
ms.locfileid: "940569"
---
# <a name="couple-and-synchronize-records-manually"></a>Records handmatig koppelen en synchroniseren
In dit onderwerp wordt beschreven hoe u een of meer records in [!INCLUDE[d365fin](includes/d365fin_md.md)] koppelt aan records in [!INCLUDE[crm_md](includes/crm_md.md)]. Door records te koppelen kunt u [!INCLUDE[crm_md](includes/crm_md.md)]-informatie vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)]bekijken en andersom. Door de koppeling kunt u ook gegevens synchroniseren tussen de records. U kunt bestaande records koppelen of nieuwe records maken en koppelen.

> [!Note]
> Gegevens koppelen en synchroniseren met [!INCLUDE[crm_md](includes/crm_md.md)] is alleen beschikbaar als de systeembeheerder een verbinding tussen [!INCLUDE[d365fin](includes/d365fin_md.md)] en [!INCLUDE[crm_md](includes/crm_md.md)] heeft gemaakt. Een snelle manier om dat te controleren is de **Klant**-kaart te openen en de actie **Koppeling instellen** te zoeken. Als de actie beschikbaar is, zijn de apps verbonden.   

## <a name="to-couple-a-record"></a>Een record koppelen  
1.  In [!INCLUDE[d365fin](includes/d365fin_md.md)] opent u de kaart voor de record die moeten worden gekoppeld. Bijvoorbeeld de klant- of contactkaart.  

    U kunt ook slechts de lijstpagina openen en de record selecteren die u wilt koppelen.  

2.  Kies de actie **Koppeling instellen**.  
3.  Vul de velden in en kies de knop **OK**.  

## <a name="to-synchronize-a-single-record"></a>Eén record synchroniseren  
1.  In [!INCLUDE[d365fin](includes/d365fin_md.md)] opent u de kaart voor de record die moeten worden gekoppeld. Bijvoorbeeld de klant- of contactkaart.  
2.  Kies de actie **Nu synchroniseren**.  
3.  Als een record kan worden gesynchroniseerd vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)] of vanuit [!INCLUDE[crm_md](includes/crm_md.md)] naar [!INCLUDE[d365fin](includes/d365fin_md.md)], selecteert u de optie die de richting van gegevensupdate opgeeft, en kiest u vervolgens **OK**.  

## <a name="to-synchronize-multiple-records"></a>Meerdere records synchroniseren  
1.  Open in [!INCLUDE[d365fin](includes/d365fin_md.md)] de lijstpagina voor de record, zoals lijstpagina Klanten of Contact.  
2.  Selecteer de records die u wilt synchroniseren en kies vervolgens de actie **Nu synchroniseren**.  
3.  Als records kunnen worden gesynchroniseerd vanuit [!INCLUDE[d365fin](includes/d365fin_md.md)] naar [!INCLUDE[crm_md](includes/crm_md.md)] of vanuit [!INCLUDE[crm_md](includes/crm_md.md)] naar [!INCLUDE[d365fin](includes/d365fin_md.md)], selecteert u de optie die de richting van gegevensupdate opgeeft, en kiest u vervolgens **OK**.  

## <a name="see-also"></a>Zie ook  
[Dynamics 365 for Sales gebruiken vanuit Business Central](marketing-integrate-dynamicscrm.md)
