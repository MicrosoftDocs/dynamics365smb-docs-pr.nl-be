---
title: 'Ontwerpdetails: Beschikbaarheid in het magazijn'
description: Meer informatie over de verschillende factoren die de artikelbeschikbaarheid in uw magazijn beïnvloeden.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
---
# Ontwerpdetails: Beschikbaarheid in het magazijn

Blijf op de hoogte van de artikelbeschikbaarheid om ervoor te zorgen dat uitgaande orders efficiënt stromen en dat uw levertijden optimaal zijn.  

Beschikbaarheid kan variëren, afhankelijk van verschillende factoren. Bijvoorbeeld:

* Toewijzingen op magazijnniveau wanneer magazijnactiviteiten zoals picks en verplaatsingen plaatsvinden.
* Wanneer het voorraadreserveringssysteem beperkingen oplegt waaraan moet worden voldaan.

[!INCLUDE [prod_short](includes/prod_short.md)] verifieert of aan alle voorwaarden is voldaan voordat aantallen worden toegewezen aan picks voor uitgaande stromen.

Wanneer niet aan de voorwaarden wordt voldaan, worden foutmeldingen weergegeven. Een typische boodschap is de generieke "Niets te verwerken". bericht. Het bericht kan om allerlei redenen worden weergegeven, zowel in uitgaande als inkomende stromen, waar een direct of indirect betrokken documentregel het veld **Te verwerken aantal** bevat.

## Inhoud van opslaglocatie en reserveringen  

Artikelhoeveelheden bestaan als magazijnposten en als artikelposten in voorraad. Deze twee boekingssoorten bevatten verschillende informatie over waar artikelen zijn en of ze beschikbaar zijn. Met magazijnposten wordt de beschikbaarheid van een artikel per (soort) opslaglocatie gedefinieerd, wat opslaglocatie-inhoud wordt genoemd. Artikelposten definiëren de beschikbaarheid van een artikel op basis van de reservering hiervan voor uitgaande documenten.  

[!INCLUDE [prod_short](includes/prod_short.md)] berekent de hoeveelheid die beschikbaar is om te picken wanneer opslaglocatie-inhoud is gekoppeld aan reserveringen.  

## Beschikbaar aantal voor picken  

[!INCLUDE [prod_short](includes/prod_short.md)] reserveert artikelen voor wachtende verkooporderverzendingen zodat ze niet worden gepickt voor andere verkooporders die eerder worden verzonden. [!INCLUDE [prod_short](includes/prod_short.md)] trekt als volgt hoeveelheden af van artikelen die al worden verwerkt:

* Hoeveelheden gereserveerd voor andere uitgaande documenten.
* Hoeveelheden op bestaande pickdocumenten.
* Hoeveelheden die zijn gepickt maar nog niet zijn verzonden of verbruikt.  

Het resultaat wordt dynamisch berekend en weergegeven in het veld **Beschikb. te picken aantal** op de pagina **Pickvoorstel**. De waarde wordt ook berekend wanneer gebruikers magazijnpicks direct voor uitgaande documenten maken. Het volgende zijn voorbeelden van uitgaande documenten:

* Verkooporders
* Productieverbruik
* Uitgaande transfers

Het resultaat is in deze documenten beschikbaar in de hoeveelheidsvelden, zoals het veld **Te verwerken aantal**.  

> [!NOTE]  
> Voor wat betreft de prioriteit van reserveringen wordt het te reserveren aantal afgetrokken van het aantal dat beschikbaar is voor picken. Als het beschikbare aantal in pickopslaglocaties bijvoorbeeld 5 eenheden is, maar 100 eenheden zich in opslaglocaties bevinden en u probeert meer dan 5 eenheden voor een andere order te reserveren, wordt een foutbericht weergegeven omdat het extra aantal in pickopslaglocaties beschikbaar moet zijn.  

### Het aantal berekenen dat beschikbaar is voor picken  

[!INCLUDE [prod_short](includes/prod_short.md)] berekent het aantal dat beschikbaar is voor picken, als volgt:  

beschikbaar aantal om te picken = aantal in pickopslaglocaties - aantal in picks en verplaatsingen – (gereserveerd aantal in pickopslaglocaties + gereserveerd aantal in picks en verplaatsingen)  

Het volgende diagram bevat de verschillende elementen van de berekening.  

![Beschikbaar om te picken met reserveringoverlap.](media/design_details_warehouse_management_availability_2.png "Beschikbaar om te picken met reserveringoverlap")  

## Beschikbaar aantal voor reserveren

Omdat de concepten opslaglocatie en reservering naast elkaar bestaan, moet het aantal artikelen dat beschikbaar is om te reserveren, afgestemd zijn met toewijzingen aan uitgaande magazijndocumenten.  

U kunt alle voorraadartikelen reserveren, behalve artikelen waarvan de uitgaande verwerking is gestart. De hoeveelheid die beschikbaar is om te reserveren, wordt gedefinieerd als de hoeveelheid in alle documenten en opslaglocatietypes. De volgende uitgaande hoeveelheden zijn uitzonderingen:  

* Aantal in niet-geregistreerde pickdocumenten  
* Aantal in verzendopslaglocaties  
* Aantal in naar-productieopslaglocaties  
* Aantal in grijpvoorraadlocaties  
* Aantal in naar-assemblageopslaglocaties  
* Aantal in correctieopslaglocaties  

Het resultaat wordt weergegeven in het veld **Totaal beschikbaar aantal** op de pagina **Reservering**.  

Op een reserveringsregel wordt het aantal dat niet kan worden gereserveerd omdat het in het magazijn is toegewezen, weergegeven in het veld **Aant. toegewezen in magazijn** op de pagina **Reservering**.  

### Het aantal berekenen dat beschikbaar is voor reservering

[!INCLUDE [prod_short](includes/prod_short.md)] berekent het aantal dat beschikbaar is voor reserveringen, als volgt:  

beschikbaar aantal om te reserveren = totaal aantal in voorraad - aantal in picks en verplaatsingen voor brondocumenten - gereserveerd aantal - aantal in uitgaande opslaglocaties  

Het volgende diagram bevat de verschillende elementen van de berekening.  

![Beschikbaar om te reserveren per magazijntoewijzing.](media/design_details_warehouse_management_availability_3.png "Beschikbaar om te reserveren per magazijntoewijzing")  

## Zie ook  

[Overzicht van magazijnbeheer](design-details-warehouse-management.md)
[Beschikbaarheid van artikelen weergeven](inventory-how-availability-overview.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]