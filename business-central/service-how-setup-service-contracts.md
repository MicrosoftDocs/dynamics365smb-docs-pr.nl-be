---
title: Servicecontracten opstellen | Microsoft Docs
description: Leer hoe u servicecontracten opstelt.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: service, cost, service order
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 33b900f1ac9e295921e7f3d6ea72cc93939d8a1b
ms.openlocfilehash: a965721aef3769aa1e794c0edb9ffa48faf99541
ms.contentlocale: nl-be
ms.lasthandoff: 11/26/2018

---

# <a name="set-up-service-contracts"></a>Servicecontracten instellen
Voordat u met contracten kunt werken, moet u het volgende instellen: 

* **Servicecontractgroepen**, waarmee gerelateerde servicecontracten worden verzameld.
* **Servicecontractboekingsgroepen**, die worden gebruikt om de servicecontractboekingen te groeperen voor servicefacturen die worden gemaakt voor servicecontracten. U wijst deze groepen toe aan servicecontracten.  
* **Contractsjablonen** waarmee contractindelingen worden gedefinieerd van contracten waarin de meestvoorkomende servicecontractdetails zijn opgenomen. U kunt servicecontractoffertes maken met sjablonen. Wanneer u een contractofferte maakt, bevatten de velden automatisch de inhoud van de sjabloonvelden.
* **Klantensjablonen** waarmee u offertes voor contacten of potentiële klanten kunt maken die niet als klant zijn geregistreerd in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

## <a name="to-set-up-a-service-contract-group"></a>Servicecontractgroepen instellen  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Servicecontractgroepen** in en kies vervolgens de gerelateerde koppeling.  
2. Vul de velden in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Schakel het selectievakje **Alleen kort. op contr.-orders** in als u wilt dat contract- of servicekortingen alleen geldig zijn voor contractserviceorders, zoals onderhoud.  

## <a name="to-set-up-a-service-contract-account-group"></a>Servicecontractboekingsgroepen instellen  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Servicecontractboekingsgroepen** in en kies vervolgens de gerelateerde koppeling.  
2. Maak een nieuwe servicecontractboekingsgroep.   
3. Vul de velden **Code** en **Omschrijving** in. Met deze velden wordt de servicecontractboekingsgroep omschreven.  
4. Vul het veld **Niet-vooruitbetaalde contractenrekening** in. Kies het nummer van de niet-vooruitbetaalde grootboekrekening.  
5. Kies in het veld **Vooruitbetaalde contractenrekening** het nummer van de vooruitbetaalde grootboekrekening.  

## <a name="to-set-up-a-contract-template"></a>Contractsjablonen instellen  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Servicecontractsjablonen** in en kies vervolgens de gerelateerde koppeling.  
2. Maak een nieuwe servicecontractsjabloon.  
3. Selecteer in het veld **Nr.** een nummer voor de contractsjabloon.  
  
     Als u op de pagina **Servicebeheerinstellingen** nummerreeksen voor contractsjablonen hebt ingesteld, kunt u ook op Enter drukken om het eerstvolgende beschikbare contractsjabloonnummer in te voeren. Vul eventueel de andere velden in.  
  
4. Vul op het sneltabblad **Factuur** het veld **Serv.-contractboekingsgroep**, de **Factuurperiode**, enzovoort in. Vul eventueel de andere velden in.  
5. Kies de actie **Servicekortingen** om contractkortingen toe te voegen.  

## <a name="to-set-up-a-customer-template"></a>Klantsjablonen instellen  
1. Kies het pictogram ![lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Klantensjablonen** in en kies vervolgens de gerelateerde koppeling.  
2. Maak een nieuwe klantensjabloonkaart.  
3. Typ op het sneltabblad **Algemeen** een code en omschrijving voor de klantensjabloonkaart in de velden **Code** en **Omschrijving**. 
4. Als u zoekcriteria wilt opgeven, vult u de andere velden in, zoals **Land-/regiocode**, **Regio** en **Taal**.  
5. Vul de velden **Bedrijfsboekingsgroep** en **Klantboekingsgroep** in.  

## <a name="see-also"></a>Zie ook
[CRM - Service instellen](service-setup-service.md)
