---
title: Taken op de achtergrond uitvoeren
description: Synchronisatie van gegevens configureren tussen Business Central en Shopify op de achtergrond.
ms.date: 05/11/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: edupont04
ms.author: andreipa
ms.openlocfilehash: f353edb4c505fd7b3eb498392abca3ce481b6009
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768172"
---
# <a name="run-tasks-in-the-background"></a>Taken op de achtergrond uitvoeren

Het is efficiënt om sommige taken gelijktijdig en geautomatiseerd uit te voeren. U kunt dergelijke taken op de achtergrond uitvoeren en u kunt ook een schema instellen wanneer u wilt dat deze taken automatisch worden uitgevoerd. Om taken op de achtergrond uit te voeren, worden twee modi ondersteund:

- Handmatig geactiveerde taken worden direct ingepland via **Taakwachtrijposten**
- Terugkerende taken worden gepland in **Taakwachtrijposten**

## <a name="run-tasks-in-the-background-for-a-specific-shop"></a>Voer taken op de achtergrond uit voor een specifieke winkel

1. Ga naar het pictogram zoeken ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen") voer de naam in van **Shopify-winkel** en kies de winkelnaam uit de lijst.
2. Selecteer de winkel waarvoor u artikelen wilt synchroniseren om de pagina **Shopify-winkelkaart** te openen.
3. Schakel de schakelaar **Synchronisatie op achtergrond toestaan** in.

Wanneer de synchronisatieactie nu wordt geactiveerd, wordt u gevraagd te wachten in plaats van dat er een taak op de voorgrond wordt uitgevoerd. Wanneer het is voltooid, kunt u doorgaan naar de volgende actie. De taak wordt gemaakt als **Taakwachtrij-item** en start onmiddellijk op een niet-blokkerende manier.

## <a name="to-schedule-recurring-tasks"></a>Terugkerende taken plannen

U kunt de volgende terugkerende activiteiten plannen om geautomatiseerd te worden uitgevoerd. Zie voor meer informatie over het plannen van taken [Taakwachtrij](../admin-job-queues-schedule-tasks.md).

|Taak|Object|
|------|------------|
|**Orders synchroniseren vanuit Shopify**|Rapport 30104 Orders synchroniseren vanuit Shopify|
|**Shopify-orders verwerken**|Rapport 30103 Shopify-verkooporders maken|
|**Verzendingen synchroniseren met Shopify**|Rapport 30109 Verzending synchroniseren met Shopify|
|**Producten en/of prijzen synchroniseren**|Rapport 30108 Shopify-producten synchroniseren|
|**Voorraad synchroniseren**|Rapport 30102 Voorraad synchroniseren met Shopify|
|**Afbeeldingen synchroniseren**|Rapport 30107 Shopify-afbeeldingen synchroniseren|
|**Klanten synchroniseren**|Rapport 30100 Shopify-klanten synchroniseren|
|**Betalingen synchroniseren**|Rapport 30105 Shopify-betalingen synchroniseren|

## <a name="see-also"></a>Zie ook

[Aan de slag met de connector voor Shopify](get-started.md)  
