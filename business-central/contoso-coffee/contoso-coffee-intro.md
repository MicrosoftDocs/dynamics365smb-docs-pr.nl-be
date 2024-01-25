---
title: Inleiding tot de demogegevens voor Contoso Coffee
description: Overzicht van scenario's voor hoe Contoso Coffee-demogegevens u kunnen helpen bij het leren gebruiken van de mogelijkheden in Business Central.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.date: 09/20/2023
ms.topic: article
ms.service: dynamics-365-business-central
ms.search.form: '5194,'
ms.custom: bap-template
---

# <a name="introduction-to-contoso-coffee-demo-data"></a>Inleiding tot de demogegevens voor Contoso Coffee

Contoso Coffee is een fictief bedrijf dat koffiezetapparaten voor consumenten en bedrijven maakt. De **Contoso Coffee**-apps voor [!INCLUDE [prod_short](../includes/prod_short.md)] voegen demogegevens toe die u kunt gebruiken om te leren hoe u de mogelijkheden in [!INCLUDE [prod_short](../includes/prod_short.md)] kunt benutten.  

## <a name="set-up-contoso-coffee-data"></a>Gegevens voor Contoso Coffee instellen

[!INCLUDE [contoso-coffee-app-install](../includes/contoso-coffee-app-install.md)]

Wanneer de apps zijn geïnstalleerd, gebruikt u op de pagina **Demohulpmiddel van Contoso** de actie **Configureren** om de volgende modules voor te bereiden. U kunt ervoor kiezen om alle beschikbare gegevens, inclusief installatie- en productiegegevens, of alleen installatiegegevens te installeren.

 - De **Gemeenschappelijke module** om algemene instellingen voor te bereiden die [!INCLUDE [prod_short](../includes/prod_short.md)] vereist. Bijvoorbeeld zaken als nummerreeksen. 

De volgende tabel beschrijft de instellingen:  

|Veld  |Omschrijving  |
|---------|---------|
|**Beginjaar** |Hiermee wordt het eerste jaar opgegeven dat u wilt gebruiken voor de demonstratiegegevens van Contoso Coffee. Afhankelijk van de bedrijfsconfiguratie is het jaar een kalenderjaar of een boekjaar.|
|**Land-/regiocode**|Hiermee wordt een land/regio voor binnenlandse klanten en leveranciers opgegeven.|
|**Bedrijfstype**    |Hiermee wordt aangegeven of het huidige bedrijf btw of omzetbelasting moet aangeven. |
|**Prijsfactor**     |Hiermee wordt een factor opgegeven om een prijs om te rekenen van USD/EUR naar de lokale valuta. *1* betekent dat de prijs hetzelfde bedrag is in elke valuta. Er wordt een hoger getal gebruikt om de prijs in de lokale valuta weer te geven. |
|**Afrondingsprecisie**  |Hiermee wordt de afrondingsprecisie opgegeven waarmee u de demogegevens wilt maken.|

 - De [Productiemodule](manufacturing/contoso-coffee-manufacturing-intro.md) ter voorbereiding op [productiescenario's](manufacturing/contoso-coffee-manufacturing-intro.md#scenarios).
 - De [Magazijnmodule](warehousing/contoso-coffee-warehousing-intro.md) ter voorbereiding op [magazijnscenario's](warehousing/contoso-coffee-warehousing-intro.md#scenarios)
 - De [Servicemodule](service/contoso-coffee-service-intro.md) ter voorbereiding op [servicescenario's](service/contoso-coffee-service-intro.md#scenarios).

Nadat u de modules heeft geconfigureerd die u wilt uitproberen, kiest u de actie **Genereren** om er demonstratiegegevens voor te maken.

## <a name="see-also"></a>Zie ook

[Productie](../production-manage-manufacturing.md)  
[Magazijnen](../warehouse-manage-warehouse.md)  
[Onderhoud](../service-service.md)
<!-- [Projects and Jobs](../projects-manage-projects.md) -->

