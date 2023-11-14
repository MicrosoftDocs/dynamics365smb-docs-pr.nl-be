---
title: 'Ontwerpdetails: Integratie met voorraad'
description: De module Warehouse Management en het toepassingsgebied Voorraad kunnen met elkaar communiceren in inventarisatie en in voorraad- of magazijnherwaardering.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: bholtorf
---
# Ontwerpdetails: Integratie met voorraad

Magazijnbeheer- en inventarisfuncties werken met elkaar samen in fysieke inventarisatie en in voorraad- of magazijnaanpassing.  

## Fysieke inventaris  

De pagina **Mag.-inventarisatiedagboek** wordt gebruikt met de pagina **Inventarisatiedagboek** voor alle geavanceerd magazijnvestigingen. De voorraad op het niveau van opslaglocaties wordt berekend en er wordt een afgedrukte lijst geleverd voor de magazijnmedewerker. Het overzicht toont welke artikelen in welke opslaglocaties moeten worden geteld.  
  
De magazijnmedewerker voert het getelde aantal op de pagina **Mag.-inventarisatiedagboek** in en boekt vervolgens het dagboek.  
  
Als het getelde aantal groter is dan het aantal op de dagboekregel, wordt een verplaatsing voor dit verschil geboekt van de standaard herwaarderingsopslaglocatie naar de getelde opslaglocatie. Hiermee wordt het aantal in de getelde opslaglocatie verhoogd en het aantal in de standaardherwaarderingsopslaglocatie verlaagd.  
  
Als het getelde aantal kleiner is dan het aantal op de dagboekregel, wordt een verplaatsing voor dit verschil geboekt van de getelde opslaglocatie naar de standaard herwaarderingsopslaglocatie. Hiermee wordt het aantal in de getelde opslaglocatie verlaagd en het aantal in de standaardherwaarderingsopslaglocatie verhoogd.  
  
In geavanceerde magazijnconfiguraties wordt de waarde in het veld **Aantal (berekend)** opgehaald uit artikelposten en wordt de waarde in het veld **Aantal (Inventarisatie)** opgehaald uit magazijnposten, met uitzondering van de inhoud van de herwaarderingsopslaglocatie. Het veld **Aantal** geeft het verschil aan tussen de eerste twee velden, en moet gelijk zijn aan de inhoud van de correctieopslaglocatie.  
  
Wanneer u het inventarisatiedagboek boekt, wordt de voorraad en de standaardherwaarderingsopslaglocatie bijgewerkt.  

[!INCLUDE [preview-posting-inventory](includes/preview-posting-inventory.md)]
  
## Magazijncorrecties in de artikelpost  

U gebruikt de pagina **Artikeldagboek** en de functie **Magazijnherwaardering berekenen** om voorraad op de artikelpost aan te passen in overeenstemming met een aanpassing die is gemaakt in het artikelaantal in een magazijnopslaglocatie. Als u een koppeling tussen de voorraad en het magazijn wilt maken, moet u een standaardherwaarderingsopslaglocatie per vestiging definiëren.  
  
De standaardcorrectieopslaglocatie registreert artikelen in het magazijn wanneer u een toename voor de voorraad boekt. Als u echter een afname boekt, wordt het aantal op de standaardopslaglocatie ook verlaagd. In beide gevallen worden artikelposten en magazijnposten gemaakt.  
  
> [!NOTE]  
> Voorraadberekeningen houden geen rekening met de correctieopslaglocatie.  
  
Om de inhoud van de opslaglocatie aan te passen, gebruikt u een magazijnartikeldagboek gebruiken, waar u het artikelnummer, de zonecode, de opslaglocatiecode en het aantal kunt invoeren die u wilt aanpassen.  
  
Als u een positief aantal invoert en de regel boekt, wordt de voorraad die in de opslaglocatie is opgeslagen vergroot en wordt het aantal dat in de standaardherwaarderingsopslaglocatie is opgeslagen, even veel verkleind.  
  
## Zie ook  

[Overzicht van magazijnbeheer](design-details-warehouse-management.md)  
[Ontwerpdetails: Beschikbaarheid in het magazijn](design-details-availability-in-the-warehouse.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]