---
title: Taken uitvoeren op de achtergrond en periodiek
description: Synchronisatie van gegevens configureren tussen Business Central en Shopify op de achtergrond.
ms.date: 03/26/2024
ms.topic: article
ms.service: dynamics-365-business-central
ms.reviewer: solsen
author: brentholtorf
ms.author: bholtorf
---

# <a name="run-tasks-in-the-background"></a>Taken op de achtergrond uitvoeren

Het is efficiënt om sommige taken gelijktijdig en geautomatiseerd uit te voeren. U kunt dergelijke taken op de achtergrond uitvoeren en u kunt ook een schema instellen wanneer u wilt dat deze taken automatisch worden uitgevoerd. Om taken op de achtergrond uit te voeren, worden twee modi ondersteund:

- Handmatig geactiveerde taken worden direct ingepland via **Taakwachtrijposten**
- Periodieke taken worden gepland in **Taakwachtrijposten**.

## <a name="run-tasks-in-the-background-for-a-specific-shop"></a>Voer taken op de achtergrond uit voor een specifieke winkel

1. Kies het ![Lampje dat de functie Vertel me opent.](../media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Shopify-winkel** in en kies vervolgens de gerelateerde koppeling.
2. Selecteer de winkel waarvoor u synchronisatie op de achtergrond wilt uitvoeren om de **Shopify-winkelkaart** te openen.
3. Zet de schakelaar **Synchronisatie op achtergrond toestaan** in.

Wanneer de synchronisatieactie nu wordt gestart, wordt u gevraagd te wachten in plaats van dat er een taak op de voorgrond wordt uitgevoerd. Wanneer de actie is voltooid, kunt u doorgaan naar de volgende actie. De taak wordt gemaakt als een **Taakwachtrij-item** en start onmiddellijk.

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
|**Bedrijven synchroniseren**|Rapport 30114 Shopify-bedrijven (B2B) synchroniseren|
|**Betalingen synchroniseren**|Rapport 30105 Shopify-betalingen synchroniseren|
|**Catalogi synchroniseren**|Rapport 30115 Shopify-catalogi (B2B) synchroniseren|
|**Catalogusprijzen synchroniseren**|Rapport 30116 Shopify-catalogusprijzen synchroniseren (B2B)|

> [!NOTE]
> Sommige elementen kunnen door verschillende taken worden bijgewerkt. Wanneer u orders importeert, kan het systeem, afhankelijk van de instelling op de **Shopify-winkelkaart**, bijvoorbeeld ook klant- en productgegevens importeren en bijwerken. Vergeet niet om dezelfde taakwachtrijcategorie te gebruiken om conflicten te voorkomen.

Andere taken die nuttig kunnen zijn om de verdere verwerking van verkoopdocumenten te automatiseren:

- Rapport 297 Batchboeken verkoopfacturen
- Rapport 296 Batchboeken verkooporders

U kunt het veld **Shopify-ordernr.** gebruiken om verkoopdocumenten te identificeren die zijn geïmporteerd uit Shopify.

Ga voor meer informatie over het boeken van verkooporders in een batch naar [Een taakwachtrijitem maken voor het batchgewijs boeken van verkooporders](../ui-batch-posting.md#to-create-a-job-queue-entry-for-batch-posting-of-sales-orders).

## <a name="to-check-the-status-of-synchronization"></a>De status van synchronisatie controleren

In **Rolcentrum bedrijfsmanager** biedt het gedeelte **Shopify-activiteiten** verschillende aanwijzingen waarmee u snel kunt vaststellen of er problemen zijn met Shopify-connector.

- **Niet-toegewezen klanten**: Shopify-klant wordt geïmporteerd, maar wordt niet gekoppeld aan een corresponderende klantpost in [!INCLUDE [prod_short](../includes/prod_short.md)].
- **Niet-toegewezen producten** - Shopify-product wordt geïmporteerd, maar wordt niet gekoppeld aan een corresponderende artikelinvoer in [!INCLUDE [prod_short](../includes/prod_short.md)].
- **Niet-verwerkte orders**: Shopify-orders worden geïmporteerd, maar verkoopdocumenten in [!INCLUDE [prod_short](../includes/prod_short.md)] zijn niet gemaakt, vaak vanwege niet-toegewezen producten of klanten.
- **Niet-verwerkte verzendingen**: geboekte verkoopverzendingen die afkomstig zijn van Shopify-orders worden niet gesynchroniseerd met Shopify.
- **Verzendingsfouten**: Shopify-connector kan geboekte verkoopverzendingen niet synchroniseren met Shopify.
- **Synchronisatiefouten**: er zijn mislukte taakwachtrij-items gerelateerd aan synchronisatie met Shopify.

## <a name="see-also"></a>Zie ook

[Aan de slag met de Shopify-connector](get-started.md)  
