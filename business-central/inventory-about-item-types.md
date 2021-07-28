---
title: Artikeltypen begrijpen
description: U kunt de voorraadwaarde van een artikel herwaarderen met de waarderingsmethoden FIFO of Gemiddeld, als de kosten van een artikel veranderen om andere redenen dan transacties.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 2541f509d02a584620c83903c3b92983aba1c2a8
ms.sourcegitcommit: e562b45fda20ff88230e086caa6587913eddae26
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 06/30/2021
ms.locfileid: "6322806"
---
# <a name="about-item-types"></a>Over artikeltypen
In het veld **Soort** op de pagina **Artikel** kunt u selecteren waarvoor het artikel in uw bedrijf wordt gebruikt en dus hoe het wordt beheerd in het systeem. Er zijn drie opties:

|Optie|Gebruikelijk doel|
|------|-----------|
|Voorraad|Een fysieke eenheid, bijvoorbeeld een fiets, voor volledige bedrijfsondersteuning.|
|Niet-voorraad|Een fysieke eenheid, zoals een bout, voor beperkte bedrijfsondersteuning, bijvoorbeeld omdat het artikel alleen intern wordt gebruikt en lage kosten heeft.|
|Service|Een arbeidstijdseenheid, zoals een adviesuur, voor beperkte bedrijfsondersteuning.|

Het soort **Voorraad** betreft volledige tracering van voorraadaantal en -waarde. Daarom worden alle artikeltransactiesoorten ondersteund en kunnen artikelen van het type voorraad worden gebruikt met alle functies voor artikelverwerking.

De typen **Service** en **Niet-voorraad** betreffen geen tracering van voorraadaantal en -waarde. Daarom worden alleen geselecteerde artikeltransactietypen en -functies ondersteund.

De drie artikeltypen ondersteunen respectievelijk de volgende functies.

|Artikelsoort|Verkoop|Inkopen|Projectverbruik|Serviceverbruik|Assemblageverbruik|Productieverbruik|Assemblage-uitvoer|Productieoutput|Locatietransfer|Fysieke telling|Voorraadherwaardering|Voorraadwaardering|Artikeltracering|Reservering|Magazijn|Planning|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Voorraad|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|
|Niet-voorraad|Ja|Ja|Ja|Ja|Ja|Ja|Nee|Nee|Nee|Nee|Nee|Nee|Nee|Nee|Nee|Nee|
|Service|Ja|Ja|Ja|Nee|Nee|Nee|Nee|Nee|Nee|Nee|Nee|Nee|Nee|Nee|Nee|Nee|

## <a name="costing-methods-for-types-of-items"></a>Waarderingsmethoden voor soorten artikelen
Als u voorraadtransacties boekt, worden de gewijzigde voorraadaantallen en -waarden vastgelegd in respectievelijk de artikel- en waardeposten. 

Voor voorraadartikelen worden de kosten geregistreerd in het veld **Tot. werk. kosten** op de pagina **Waardeposten** en wanneer deze zijn gereconcilieerd met het grootboek, worden de kosten weergegeven in het veld **Kosten geboekt naar grootboek**. Zie voor meer informatie [Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md).

Voor niet-voorraad- en serviceartikelen worden de kosten geregistreerd in het veld **Kostenbedrag (Niet-inv.)** op de pagina **Waardeposten**. Voor niet-voorraad- en serviceartikelen worden de kosten gespecificeerd op de verkoop-, assembly- en productiedocumenten en -dagboeken. De standaardkosten kunnen worden gespecificeerd in het veld **Kostprijs** op de pagina's **Artikelkaart** en **SKU**. Kosten voor dit soort artikelen worden niet gereconcilieerd met het grootboek. 

## <a name="catalog-and-service-items"></a>Catalogus- en serviceartikelen
Artikelen die u aan uw klanten aanbiedt, maar die u niet in uw systeem wilt beheren tot u ze begint te verkopen, kunnen worden ingesteld als catalogusartikelen. Catalogusartikelen moeten niet worden verward met normale artikelen van het type Niet-voorraad. Zie voor meer informatie [Werken met catalogusartikelen](inventory-how-work-nonstock-items.md).

Artikelen van klanten waaraan u onderhoud verricht, zoals een printer, worden serviceartikelen genoemd. Serviceartikelen hebben niets van doen met normale of catalogusartikelen. Serviceonderdelen kunnen echter gewone artikelen zijn. Zie voor meer informatie [Serviceartikelen en serviceartikelonderdelen instellen](service-how-setup-service-items.md).

## <a name="see-also"></a>Zie ook
[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Voorraad instellen](inventory-setup-inventory.md)  
[Voorraadkosten beheren](finance-manage-inventory-costs.md)  
[Voorraad](inventory-manage-inventory.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]