---
title: Statussen instellen voor serviceorders en reparaties | Microsoft Docs
description: U moet negen herstelstatusopties instellen waarmee u de voortgang van herstel en onderhoud van serviceartikelen in serviceorders kunt aangeven.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="set-up-statuses-for-service-orders-and-repairs"></a>Statussen instellen voor serviceorders en reparaties

U moet herstelstatusopties instellen waarmee u de voortgang van herstel en onderhoud van serviceartikelen in serviceorders kunt aangeven. U moet minimaal negen herstelstatusopties instellen om situaties of ondernomen acties met betrekking tot de service voor serviceartikelen aan te duiden.  

U kunt het prioriteitsniveau voor serviceorderstatusopties instellen. De vier prioriteiten zijn **Hoog**, **Relatief hoog**, **Relatief laag** en **Laag**.  

Wanneer u de herstelstatus van een serviceartikel in een serviceorder wijzigt, wordt de serviceorderstatus bijgewerkt. De herstelstatus van elk serviceartikel is gekoppeld aan de serviceorderstatus. Als de serviceartikelen zijn gekoppeld aan twee of meer opties voor serviceorderstatus, wordt de serviceorderstatus met de hoogste prioriteit geselecteerd.  

Voordat u een reparatiestatus kunt instellen, moet u servicestatusprioriteiten instellen.

## <a name="to-set-up-service-status-priorities"></a>Servicestatusprioriteiten instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Serviceorderstatus** in en kies vervolgens de gerelateerde koppeling  
2. Selecteer de serviceorderstatus waarvoor u een prioriteit wilt instellen.  
3. Kies de gewenste prioriteit voor deze serviceorderstatus in het veld **Prioriteit**.  

Herhaal stap 2 en 3 totdat u de prioriteit voor elk van de vier statusopties hebt ingesteld: **In behandeling**, **In verwerking**, **Gereedgemeld** en **Afwachten**.  

## <a name="to-set-up-a-repair-status"></a>Herstelstatus instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Herstelstatus** in en kies vervolgens de gerelateerde koppeling.
2. Maak een nieuwe herstelstatus.  
3. Vul de velden **Code** en **Omschrijving** in.  
4. In het veld **Serviceorderstatus** kiest u de orderstatus waaraan u de herstelstatus wilt koppelen. In het veld **Prioriteit** wordt de prioriteit weergegeven van de serviceorderstatus die u hebt gekozen.  
5. Kies een herstelstatus. U kunt er slechts één kiezen. Een reparatiestatus kan niet worden gekoppeld aan meer dan één reparatiestatusoptie.  
6. Kies het veld **Boeken toegestaan** als u serviceorders wilt boeken met serviceartikelen met deze herstelstatus.  
7. Schakel het selectievakje **Status Wachtend toegestaan** in als u de optie voor serviceorderstatus handmatig wilt wijzigen in **In behandeling** op serviceorders met serviceartikelen met deze herstelstatus.  
8. Schakel de selectievakjes **Status In verwerking toegestaan**, **Status Gereedgemeld toegestaan** en **Status Afwachten toegestaan** op dezelfde manier in.

Herhaal deze stappen voor elke herstelstatusoptie die u wilt maken.

## <a name="see-also"></a>Zie ook

[Serviceorderstatus en herstelstatus](service-service-order-status-and-repair-status.md)  
[CRM - Service instellen](service-setup-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
