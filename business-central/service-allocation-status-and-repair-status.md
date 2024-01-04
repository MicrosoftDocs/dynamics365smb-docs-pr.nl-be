---
title: Toewijzingsstatus en herstelstatus | Microsoft Docs
description: Kom meer te weten over de relatie tussen de herstelstatus van serviceartikelen en de toewijzingsstatus van de toewijzingsposten hiervoor.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'resources, allocation, status, repairs'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="allocation-status-and-repair-status-of-service-items"></a>Toewijzingsstatus en herstelstatus van serviceartikelen
Tussen de herstelstatus van serviceartikelen en de toewijzingsstatus van de toewijzingsposten voor de serviceartikelen bestaat een bepaalde relatie in de module Servicebeheer. De toewijzingsstatus verandert wanneer u de herstelstatus van het serviceartikel wijzigt in **Gereedgemeld** of **Deels service verleend** en een serviceofferte omzet in een serviceorder. De herstelstatus van het serviceartikel verandert wanneer u de toewijzing van het serviceartikel wijzigt of het serviceartikel toewijst aan een andere resource. U kunt de herstelstatus van serviceartikelen bekijken op de pagina **Servicetaken** en bijwerken in het veld **Herstelstatuscode** op de pagina **Serviceartikelwerkbon**. U kunt de toewijzingsstatus bekijken in het veld **Status** op de pagina **Resourcetoewijzingen**.  
  
## <a name="changing-repair-status"></a>Herstelstatus wijzigen
Wanneer u de herstelstatus van een serviceartikel op een serviceartikelregel wijzigt, wordt voor dit serviceartikel automatisch naar een bijbehorende toewijzingspost met de status **Actief** gezocht. Als een dergelijke toewijzingspost wordt gevonden, wordt de status op een van de volgende manieren bijgewerkt:  
  
* Als u de herstelstatus wijzigt in **Gereedgemeld**, wordt de toewijzingsstatus van **Actief** gewijzigd in **Gereedgemeld**.  
* Wijzigt u de herstelstatus in **Deels service verleend** (dat wil zeggen: een deel van de service is voltooid) of **Toegewezen** (dat wil zeggen: er is geen service uitgevoerd), dan wordt de toewijzingsstatus van **Actief** gewijzigd in **Hertoewijzing vereist**.  
* Wanneer een toewijzingspost wordt gemaakt voor een serviceorder met de aanduiding dat er geen resource is toegewezen, wordt het veld **Status** op de pagina **Resourcetoewijzingen** ingesteld op **Niet-actief**.  
* De status van de toewijzingspost wordt ingesteld op **Geannuleerd** wanneer u het toegewezen serviceartikel in de toewijzingspost van de serviceorder opnieuw toewijst. Hiermee wordt aangegeven dat de toegewezen resource of resourcegroep nog niet is begonnen met de servicetaak.  
  
Met de toewijzingsstatus wordt aangegeven wanneer het serviceproces is voltooid of wanneer een andere resource nodig is om de service voor het serviceartikel te voltooien.  
  
## <a name="converting-service-quotes-to-service-orders"></a>Serviceoffertes omzetten in serviceorders
Wanneer u een serviceofferte omzet in een serviceorder, worden de serviceorder, de serviceartikelen in de order en de toewijzingsposten als volgt bijgewerkt:  
  
* De herstelstatus van de serviceartikelen wordt gewijzigd in **Eerste**.  
* De serviceorderstatus wordt gewijzigd in **In behandeling**.  
* Voor de serviceartikelen met de status **Actief** in de serviceorder wordt gezocht naar toewijzingsposten. Als dergelijke toewijzingsposten worden gevonden, wordt de toewijzingsstatus van **Actief** gewijzigd in **Hertoewijzing vereist**.  
  
## <a name="canceling-allocations"></a>Toewijzingen annuleren
Wanneer u een toewijzing voor een serviceartikel annuleert, wordt de toewijzingsstatus van de bijbehorende toewijzingspost in [!INCLUDE[prod_short](includes/prod_short.md)] bijgewerkt van **Actief** in **Hertoewijzing vereist**:

De herstelstatus van het serviceartikel in de toewijzingspost wordt als volgt bijgewerkt:  
  
* Als de herstelstatus de waarde **Eerste** heeft, wordt de herstelstatus gewijzigd in **Toegewezen** (er is nog geen service begonnen).  
* Heeft de herstelstatus de waarde **In verwerking**, dan wordt de herstelstatus gewijzigd in **Deels service verleend** (een deel van de service is voltooid).  
  
## <a name="reallocating-an-active-allocation-entry"></a>Een actieve toewijzingspost opnieuw toewijzen
Wanneer u een serviceartikel in een toewijzingspost met de status **Actief** opnieuw toewijst, wordt de toewijzingspost als volgt bijgewerkt:  
  
* Als de service is begonnen terwijl de toewijzing de waarde **Actief** had (dat wil zeggen, als de herstelstatus van het serviceartikel in de post is gewijzigd in **In verwerking**), wordt de toewijzingsstatus gewijzigd van **Actief** in **Gereedgemeld**.  
* Als de service niet is gestart terwijl de toewijzing de waarde **Actief** heeft, wordt de toewijzingsstatus gewijzigd van **Actief** in **Geannuleerd**.  
  
De herstelstatus van het serviceartikel in de toewijzingspost wordt bijgewerkt alsof u de toewijzing hebt geannuleerd:  
  
* Als de herstelstatus de waarde **Eerste** heeft, wordt de herstelstatus gewijzigd in **Toegewezen** (er is nog geen service begonnen).  
* Heeft de herstelstatus de waarde **In verwerking**, dan wordt de herstelstatus gewijzigd in **Deels service verleend** (een deel van de service is voltooid).  
  
Er wordt een nieuwe toewijzingspost gemaakt met de nieuwe resource en de status **Actief**.  
  
## <a name="reallocating-a-service-item"></a>Een serviceartikel opnieuw toewijzen
Wanneer u een serviceartikel in een toewijzingspost met de status **Hertoewijzing vereist** opnieuw toewijst, wordt de toewijzingspost als volgt bijgewerkt:  
  
* Als de service is begonnen terwijl de toewijzing de waarde **Actief** had (dat wil zeggen, als de herstelstatus van het serviceartikel in de post is gewijzigd in **In verwerking**), wordt de toewijzingsstatus gewijzigd van **Hertoewijzing vereist** in **Gereedgemeld**.  
* Als de service niet is gestart terwijl de toewijzing de waarde **Actief** heeft, wordt de toewijzingsstatus gewijzigd van **Hertoewijzing vereist** in **Geannuleerd**.  
  
Er wordt een nieuwe toewijzingspost gemaakt met de nieuwe resource en de status **Actief**.  
  
## <a name="see-also"></a>Zie ook
[Resourcetoewijzingen instellen](service-how-setup-resource-allocation.md)  
[Resources toewijzen](service-how-to-allocate-resources.md)  



[!INCLUDE[footer-include](includes/footer-banner.md)]
