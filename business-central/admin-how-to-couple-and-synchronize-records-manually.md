---
title: Koppelen en synchroniseren | Microsoft Docs
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
ms.openlocfilehash: fa4d6cfe13662613a73c14d68542f8319798ea80
ms.sourcegitcommit: 2e7307fbe1eb3b34d0ad9356226a19409054a402
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/17/2020
ms.locfileid: "4752687"
---
# <a name="coupling-and-synchronizing"></a>Koppelen en synchroniseren
In dit onderwerp wordt beschreven hoe u een of meer records in [!INCLUDE[prod_short](includes/prod_short.md)] koppelt aan records in Dataverse of [!INCLUDE[crm_md](includes/crm_md.md)]. Door records te koppelen kunt u Dataverse-informatie vanuit [!INCLUDE[prod_short](includes/prod_short.md)]bekijken en andersom. Door de koppeling kunt u ook gegevens synchroniseren tussen de records. U kunt bestaande records koppelen of nieuwe records maken en koppelen.

> [!Note]
> Gegevens koppelen en synchroniseren is alleen beschikbaar als de systeembeheerder een verbinding tussen [!INCLUDE[prod_short](includes/prod_short.md)] en Dataverse of [!INCLUDE[crm_md](includes/crm_md.md)] heeft gemaakt. Een snelle manier om dat te controleren is de **Klant**-kaart te openen en de actie **Koppeling instellen** te zoeken. Als de actie beschikbaar is, zijn de apps verbonden.   

## <a name="video-example"></a>Videovoorbeeld

> [!VIDEO https://go.microsoft.com/fwlink/?linkid=2098376]

## <a name="to-couple-a-record"></a>Een record koppelen  
1.  In [!INCLUDE[prod_short](includes/prod_short.md)] opent u de kaart voor de record die moeten worden gekoppeld. Bijvoorbeeld de klant- of contactkaart.  

    U kunt ook slechts de lijstpagina openen en de record selecteren die u wilt koppelen.  

2.  Kies de actie **Koppeling instellen**.  
3.  Vul de velden in en kies de knop **OK**.  

## <a name="to-synchronize-a-single-record"></a>Eén record synchroniseren  
1.  In [!INCLUDE[prod_short](includes/prod_short.md)] opent u de kaart voor de record die moeten worden gekoppeld. Bijvoorbeeld de klant- of contactkaart.  
2.  Kies de actie **Nu synchroniseren**.  
3.  Als een record in één richting kan worden gesynchroniseerd, selecteert u de optie die de richting van de gegevensupdate opgeeft, en kiest u vervolgens **OK**.  

## <a name="to-synchronize-a-single-record-from-crm_md"></a>Eén record synchroniseren vanuit [!INCLUDE[crm_md](includes/crm_md.md)]  
1.  In [!INCLUDE[crm_md](includes/crm_md.md)] opent u het formulier voor de record die u wilt koppelen. Bijvoorbeeld het formulier Accountkaart of Contactkaart.  
2.  Kies de actie **[!INCLUDE[prod_short](includes/prod_short.md)]** op het lint om een record automatisch te openen en te koppelen.

> [!Note]
> U kunt één record alleen automatisch synchroniseren vanuit [!INCLUDE[crm_md](includes/crm_md.md)] wanneer **Alleen gekoppelde records synchr.** is uitgeschakeld en de synchronisatierichting is ingesteld op Bidirectioneel of Van integratietabel op de pagina **Toewijzing van integratietabel** voor de record. Zie voor meer informatie [De tabellen en velden toewijzen voor synchronisatie](admin-how-to-modify-table-mappings-for-synchronization.md#creating-new-records).     

## <a name="to-synchronize-multiple-records"></a>Meerdere records synchroniseren  
1.  Open in [!INCLUDE[prod_short](includes/prod_short.md)] de lijstpagina voor de record, zoals lijstpagina Klanten of Contact.  
2.  Selecteer de records die u wilt synchroniseren en kies vervolgens de actie **Nu synchroniseren**.  
3.  Als records in één richting kunnen worden gesynchroniseerd, selecteert u de optie die de richting opgeeft, en kiest u vervolgens **OK**.  

## <a name="uncoupling-records"></a>Records ontkoppelen
U kunt een of meer records loskoppelen van lijstpagina's of de pagina **Fouten met gekoppelde gegevenssynchronisatie** door een of meer regels te kiezen en **Koppeling verwijderen** te kiezen. U kunt ook alle koppelingen verwijderen voor een of meer tabeltoewijzingen op de pagina **Integratietabeltoewijzingen**.

## <a name="see-also"></a>Zie ook  
[Microsoft Dynamics 365 Sales gebruiken vanuit Business Central](marketing-integrate-dynamicscrm.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]