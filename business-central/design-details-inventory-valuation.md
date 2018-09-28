---
title: 'Ontwerpdetails: Voorraadwaardering | Microsoft Docs'
description: Voorraadwaardering XE "Voorraadwaardering" is de bepaling van de kosten die worden toegewezen aan een voorraadartikel, zoals uitgedrukt met de volgende vergelijking.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 10/01/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 1e2f307a4309389b09e5ce291cb5eca3abee6b88
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-inventory-valuation"></a>Ontwerpdetails: Voorraadwaardering
Voorraadwaardering XE "Voorraadwaardering" is de bepaling van de kosten die worden toegewezen aan een voorraadartikel, zoals uitgedrukt met de volgende vergelijking.  

Eindvoorraad = beginvoorraad + netto inkopen - kosten van verkochte goederen  

De berekening van voorraadwaardering gebruikt het veld **Tot. werk. kosten** van de waardeposten voor het artikel. De posten zijn ingedeeld volgens het boekingssoort XE "Entry Type" dat overeenkomt met de kostenonderdelen, directe kosten, indirecte kosten, verschillen, herwaarderingen en afrondingen. Zie [Ontwerpdetails: kostenonderdelen](design-details-cost-components.md) voor meer informatie.  

Posten worden met elkaar vereffend door vaste vereffening XE "Vereffening; Vast" of op basis van de aanname van de algemene kostenstroom die wordt gedefinieerd door de waarderingsmethode XE "Methode; Waardering" XE "Waarderingsmethode". Eén negatieve voorraadmutatiepost kan worden vereffend met meer dan één positieve post met verschillende boekingsdatums en mogelijk verschillende aanschafkosten XE "Acquisition Cost". Zie [Ontwerpdetails: artikelvereffening](design-details-item-application.md) voor meer informatie. Berekening van de voorraadwaarde XE "Inventory Value" voor een bepaalde datum is daarom gebaseerd op het totaliseren van positieve en negatieve waardeposten.  

## <a name="inventory-valuation-report"></a>Rapport Voorraadwaardering  
Voor het berekenen van de voorraadwaarde in de lijst **Voorraadwaardering** wordt eerst de waarde van de voorraad van het artikel berekend op een bepaalde begindatum. Vervolgens wordt de waarde van positieve voorraadmutaties opgeteld en wordt de waarde van negatieve voorraadmutaties afgetrokken tot een bepaalde einddatum. Het eindresultaat is de voorraadwaarde op de einddatum. De lijst berekent deze waarden door de waarden in het veld **Tot. werk. kosten** in de waardeposten op te tellen, met de boekingsdatums als filters.  

De afgedrukte lijst geeft altijd de werkelijke bedragen weer, dat wil zeggen, de kosten van posten die als gefactureerd zijn geboekt. De verwachte kosten van posten die als ontvangen of verzonden zijn geboekt, worden ook in de lijst afgedrukt als u het selectievakje Inclusief verwachte kosten op het sneltabblad Opties inschakelt.  

> [!IMPORTANT]  
>  Waarden in de lijst **Voorraadwaardering** worden gereconcilieerd met de voorraadrekening in het grootboek, wat betekent dat de waardeposten in kwestie naar het grootboek zijn geboekt.  

> [!IMPORTANT]  
>  Bedragen in de **Waarde**-kolommen van het rapport zijn gebaseerd op de boekingsdatum van transacties voor een artikel.  

## <a name="inventory-valuation---wip-report"></a>Rapport Voorraadwaardering - OHW  
Een productiebedrijf moet de waarde van drie soorten voorraad bepalen:  

* Voorraad grondstoffen  
* OHW-voorraad  
* Voorraad eindproducten  

De waarde van OHW-vooraad wordt bepaald door de volgende vergelijking:  

* Eind-OHW-voorraad = begin-OHW-voorraad + productiekosten - kosten van vervaardigde goederen  

Voor ingekochte voorraad vormen de waardeposten de basis van de voorraadwaardering. De berekening wordt uitgevoerd met de waarden in het veld **Tot. werk. kosten** van het artikel en capaciteitswaardeposten die aan een productieorder zijn gekoppeld.  

Het doel van OHW-voorraadwaardering is de waarde te bepalen van de artikelen waarvoor productie nog niet is voltooid op een bepaalde datum. De OHW-voorraadwaarde wordt daarom gebaseerd op de waardeposten die gekoppeld zijn aan de verbruiks- en capaciteitsposten. Verbruikposten moeten volledig worden gefactureerd op de datum van de waardering. De lijst **Voorraadwaardering - OHW** geeft daarom de kosten voor de OHW-voorraadwaarde in twee categorieën weer: verbruik en capaciteit.  

## <a name="see-also"></a>Zie ook  
[Ontwerpdetails: Reconciliatie met het grootboek](design-details-reconciliation-with-the-general-ledger.md)   
[Ontwerpdetails: Herwaardering](design-details-revaluation.md)   
[Ontwerpdetails: Productieorderboeking](design-details-production-order-posting.md)
[Voorraadkosten beheren](finance-manage-inventory-costs.md)  
[Financiën](finance.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

