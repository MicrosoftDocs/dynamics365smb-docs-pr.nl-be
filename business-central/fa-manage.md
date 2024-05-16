---
title: Vaste activa beheren (bevat video)
description: Leren over de vaste-activafunctionaliteit en een overzicht krijgen van hoe u met vaste activa werkt en deze beheert.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: 'machinery, buildings'
ms.search.form: '5604, 5606, 5664, 5601, 5602, 5658, 5603, 5671, 5641, 5629, 5633, 5634, 5649, 5622, 5650'
ms.date: 05/06/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---

# <a name="manage-fixed-assets"></a>Vaste activa beheren

De functionaliteit voor vaste activa in [!INCLUDE[prod_short](includes/prod_short.md)] biedt een overzicht van uw vaste activa en helpt zorgen dat de afschrijving ervan klopt. U kunt hiermee ook uw onderhoudskosten bijhouden, verzekeringspolissen beheren, transacties voor vaste activa boeken en verschillende rapporten en statistieken genereren.

## <a name="video-overview"></a>Video-overzicht

De volgende video behandelt de basisprincipes van vaste activa:

> [!Video https://www.microsoft.com/en-us/videoplayer/embed/RE4AegS?rel=0]

## <a name="initial-setup-of-fixed-assets"></a>Initiële instelling van vaste activa

Voordat u vaste activa kunt beheren, moet u de volgende instellingen voltooien:

- Standaardwaarden
- Boekhouding van vaste activa
- Groepen en typen boeken
- Verdeelsleutels
- VA-dagboeken

Ga voor informatie naar [Vaste activa instellen](fa-setup.md).

## <a name="fixed-assets-analytics"></a>Analyses van vaste activa

In dit gedeelte worden de analytische hulpmiddelen beschreven die u kunt gebruiken om inzicht te krijgen in gegevens over uw vaste activa.

| Actie | Zie |
| --- | --- |
| Leer meer over de mogelijkheden voor het analyseren van gegevens over vaste activa. | [Overzicht van analyses van vaste activa](fa-analytics-overview.md) |
| Voer ad-hocanalyses uit van gegevens over vaste activa rechtstreeks op lijstpagina's en query's. | [Adhoc-analyse van vaste-activagegevens](ad-hoc-analysis-fa.md) |
| Ingebouwde rapporten voor vaste activa verkennen. | [Ingebouwde vaste-activarapporten](fa-reports.md) |
| Onderhoudskosten controleren. | [Onderhoudskosten controleren](fa-how-maintain.md#to-monitor-maintenance-costs)|
| Verzekeringsdekking controleren. | [Verzekeringsdekking controleren](fa-how-insure.md#to-monitor-insurance-coverage) |
| Buitengebruikstellingsposten bekijken. | [Buitengebruikstellingsposten weergeven](fa-how-dispose-retire.md#to-view-disposal-ledger-entries) |
| Geschatte buitengebruikstellingswaarden bekijken. | [Voorspelde buitengebruikstellingswaarden weergeven](fa-how-manage-budgets.md#to-view-projected-disposal-values) |

## <a name="register-fixed-assets"></a>Vaste activa registreren

Voor elk vast activum moet u een kaart maken met informatie erover. Gebouwen of productiemateriaal kunnen bijvoorbeeld als hoofdactivum worden ingesteld, met een onderdelenlijst. U kunt activa op verschillende manieren groeperen, bijvoorbeeld per klasse, afdeling of vestiging. Vervolgens kunt u beginnen met het aanschaffen, onderhouden en verkopen van de vaste activa. U kunt ook gebudgetteerde activa instellen. Met budgettering kunt u verwachte aan- en verkopen opnemen in rapporten.

| Tot  | Zie |
| --- | --- |
| Budgetten voor vaste activa beheren, aanschafkosten budgetteren, buitengebruikstellingen van vaste activa budgetteren en afschrijving budgetteren. |[Budgetten voor vaste activa beheren](fa-how-manage-budgets.md) |
| Vaste activa maken, afschrijvingsmethoden toewijzen, aankopen boeken, restwaarden boeken en VA-lijsten afdrukken. |[Vaste activa aanschaffen](fa-how-acquire.md) |

## <a name="set-up-depreciations-for-your-fixed-assets"></a>Afschrijvingen instellen voor uw vaste activa

Om afschrijvingen van vaste activa en andere financiële transacties voor vaste activa bij te houden, kunt u een of meer afschrijvingsboeken voor elk vast activum instellen. Er zijn een aantal stappen voor het afschrijven van activa:

1. Een rapport uitvoeren om periodieke afschrijving te berekenen.
1. Een dagboek invullen met de resulterende posten.
1. Boek het dagboek.

[!INCLUDE[prod_short](includes/prod_short.md)] ondersteunt verschillende afschrijvingsmethoden. Ga voor meer informatie naar [Afschrijvingsmethoden](fa-depreciation-methods.md). U kunt meerdere afschrijvingsboeken voor elk vast activum instellen voor verschillende doeleinden, bijvoorbeeld één boek voor belastingrapportage en een ander boek voor interne rapportage.

| Tot  | Zie |
| --- | --- |
| Meer informatie over andere afschrijvingsmethoden voor vaste activa. |[Afschrijvingsmethoden](fa-depreciation-methods.md) |
| Afschrijving berekenen, afschrijving boeken en afschrijving analyseren in rapporten voor vaste activa. |[Vaste activa afschrijven of aflossen](fa-how-depreciate-amortize.md) |
| Gewijzigde afschrijvingsboekwaarden bekijken. | [Gewijzigde afschrijvingsboekwaarden weergeven](fa-how-trans-split-combine.md#to-view-changed-depreciation-book-values-due-to-fixed-asset-reclassification) |
| Registreer vaste activa handmatig op de pagina **Financieel dagboek voor vaste activa** of op de pagina **VA-dagboek**, afhankelijk van de vraag of de transacties zijn bedoeld voor financiële rapportage of intern beheer. | [Afschrijving van vaste activa instellen](fa-how-setup-depreciation.md) |

## <a name="fixed-assets-maintenance-and-insurance"></a>Onderhoud en verzekering van vaste activa

Voor elk activum kunt u de onderhoudskosten en de volgende onderhoudsbeurt vastleggen. Het bijhouden van onderhoudskosten is belangrijk voor budgetdoeleinden en bij het maken van een beslissing over het al dan niet vervangen van een vast activum. U kunt elk vast activum koppelen aan een of meer verzekeringspolissen en controleren of de polispremies overeenkomen met de waarde van de activa.

| Tot  | Zie |
| --- | --- |
| Onderhoudsbeurten registreren, onderhoudskosten boeken en onderhoudskosten controleren. |[Vaste activa onderhouden](fa-how-maintain.md) |
| Onderhoudskosten controleren. | [Onderhoudskosten controleren](fa-how-maintain.md#to-monitor-maintenance-costs)|
| Verzekeringsinformatie bijwerken, aanschafkosten boeken naar verzekeringspolissen, verzekeringsdekking wijzigen, verzekeringsstatistieken bekijken en een lijst met verzekeringspolissen weergeven. |[Vaste activa verzekeren](fa-how-insure.md) |
| Verzekeringsdekking controleren. | [Verzekeringsdekking controleren](fa-how-insure.md#to-monitor-insurance-coverage) |

## <a name="reclassify-transfer-split-upcombine-adjust-value-write-down-and-dispose-fixed-assets"></a>Vaste activa herclassificeren, overdragen, opsplitsen/combineren, van waarde aanpassen, afschrijven en afstoten

| Tot  | Zie |
| --- | --- |
| Vaste activa herindelen, vaste activa naar andere locaties verplaatsen, activa opsplitsen of combineren. |[Vaste activa overboeken, splitsen of combineren](fa-how-trans-split-combine.md) |
| Waarden van vaste activa aanpassen, waardevermeerderings- en waardeverminderingstransacties boeken. |[Vaste activa herwaarderen](fa-how-revalue.md) |
| Buitengebruikstellingstransacties boeken, buitengebruikstellingsposten bekijken en gedeeltelijke buitengebruikstellingen boeken. |[Vaste activa buiten gebruik stellen of wegdoen](fa-how-dispose-retire.md) |
| Buitengebruikstellingsposten bekijken. | [Buitengebruikstellingsposten weergeven](fa-how-dispose-retire.md#to-view-disposal-ledger-entries) |
| Geschatte buitengebruikstellingswaarden bekijken. | [Voorspelde buitengebruikstellingswaarden weergeven](fa-how-manage-budgets.md#to-view-projected-disposal-values) |

## <a name="see-also"></a>Zie ook

[Vaste activa instellen](fa-setup.md)  
[Overzicht van VA-analyse](fa-analytics-overview.md)  
[Overzicht van financiën](finance.md)  
[Voorbereid zijn om zaken te doen](ui-get-ready-business.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Wijzigen welke functies worden weergegeven](ui-experiences.md)  

## [!INCLUDE[prod_short](includes/free_trial_md.md)]  

[!INCLUDE[footer-include](includes/footer-banner.md)]
