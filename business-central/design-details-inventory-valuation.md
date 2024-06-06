---
title: 'Ontwerpdetails: Voorraadwaardering | Microsoft Docs'
description: Voorraadwaardering is de bepaling van de kostprijs van een voorraadartikel.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: null
ms.date: 12/13/2023
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Ontwerpdetails: Voorraadwaardering
Voorraadwaardering is de bepaling van de kosten die worden toegewezen aan een voorraadartikel, zoals uitgedrukt met de volgende vergelijking.  

Eindvoorraad = beginvoorraad + netto inkopen - kosten van verkochte goederen  

De berekening van voorraadwaardering gebruikt het veld **Tot. werk. kosten** van de waardeposten voor het artikel. De posten zijn ingedeeld volgens het boekingssoort dat overeenkomt met de kostenonderdelen, directe kosten, indirecte kosten, verschil, herwaardering en afronding. Zie [Ontwerpdetails: kostenonderdelen](design-details-cost-components.md) voor meer informatie.  

Posten worden met elkaar vereffend door vaste vereffening of op basis van de aanname van de algemene kostenstroom die wordt gedefinieerd door de waarderingsmethode. Eén negatieve voorraadmutatiepost kan worden vereffend met meer dan één positieve post met verschillende boekingsdatums en mogelijk verschillende aanschafkosten. Zie [Ontwerpdetails: artikelvereffening](design-details-item-application.md) voor meer informatie. Berekening van de voorraadwaarde voor een bepaalde datum is daarom gebaseerd op het totaliseren van positieve en negatieve waardeposten.  

## Rapport Voorraadwaardering  
Voor het berekenen van de voorraadwaarde in de lijst **Voorraadwaardering** wordt eerst de waarde van de voorraad van het artikel berekend op een bepaalde begindatum. Vervolgens wordt de waarde van positieve voorraadmutaties opgeteld en wordt de waarde van negatieve voorraadmutaties afgetrokken tot een bepaalde einddatum. Het eindresultaat is de voorraadwaarde op de einddatum. De lijst berekent deze waarden door de waarden in het veld **Tot. werk. kosten** in de waardeposten op te tellen, met de boekingsdatums als filters.  

De afgedrukte lijst geeft altijd de werkelijke bedragen weer, dat wil zeggen, de kosten van posten die als gefactureerd zijn geboekt. De verwachte kosten van posten die als ontvangen of verzonden zijn geboekt, worden ook in de lijst afgedrukt als u het selectievakje Inclusief verwachte kosten op het sneltabblad Opties inschakelt.  

> [!IMPORTANT]  
>  Waarden in de lijst **Voorraadwaardering** worden gereconcilieerd met de voorraadrekening in het grootboek, wat betekent dat de waardeposten in kwestie naar het grootboek zijn geboekt.  

> [!IMPORTANT]  
>  Bedragen in de **Waarde**-kolommen van het rapport zijn gebaseerd op de boekingsdatum van transacties voor een artikel.  

## Rapport Voorraadwaardering - OHW  
Een productiebedrijf moet de waarde van drie soorten voorraad bepalen:  

* Voorraad grondstoffen  
* OHW-voorraad  
* Voorraad eindproducten  

De waarde van OHW-vooraad wordt bepaald door de volgende vergelijking:  

* Eind-OHW-voorraad = begin-OHW-voorraad + productiekosten - kosten van vervaardigde goederen  

Voor ingekochte voorraad vormen de waardeposten de basis van de voorraadwaardering. De berekening wordt uitgevoerd met de waarden in het veld **Tot. werk. kosten** van het artikel en capaciteitswaardeposten die aan een productieorder zijn gekoppeld.  

Het doel van OHW-voorraadwaardering is de waarde te bepalen van de artikelen waarvoor productie nog niet is voltooid op een bepaalde datum. De OHW-voorraadwaarde wordt daarom gebaseerd op de waardeposten die gekoppeld zijn aan de verbruiks- en capaciteitsposten. Verbruikposten moeten worden gefactureerd op de datum van de waardering. De lijst **Voorraadwaardering - OHW** geeft daarom de kosten voor de OHW-voorraadwaarde in twee categorieën weer: verbruik en capaciteit.  

## Zie ook  
[Ontwerpdetails: Reconciliatie met het grootboek](design-details-reconciliation-with-the-general-ledger.md)   
[Ontwerpdetails: Herwaardering](design-details-revaluation.md)   
[Ontwerpdetails: Productieorderboeking](design-details-production-order-posting.md)  
[Voorraadkosten beheren](finance-manage-inventory-costs.md)    
[Financiën](finance.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]