---
title: Artikeltypen begrijpen
description: 'U kunt de voorraadwaarde van een artikel herwaarderen met de waarderingsmethoden FIFO of Gemiddeld, als de kosten van een artikel veranderen om andere redenen dan transacties.'
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '9297, 5845, 30,'
ms.date: 06/16/2021
ms.author: edupont
---
# <a name="about-item-types" />Over artikeltypen
In het veld **Soort** op de pagina **Artikelkaart** kunt u selecteren waarvoor het artikel in uw bedrijf wordt gebruikt. Dit heeft invloed op de mate waarin u het artikel kunt beheren in de voorraad. In de volgende tabel worden de drie soorten artikelen vermeld en beschreven die beschikbaar zijn.

|Optie|Gebruikelijk doel|
|------|-----------|
|Voorraad|Fysieke zaken, zoals fietsen, telefoons en bureaus, waarvoor u alle voorraadprocessen wilt kunnen gebruiken. Dit kunnen ook niet-fysieke items zijn, zoals softwarelicenties en abonnementen, als de items identificatienummers hebben, zoals serienummers. U kunt artikelwaarden en beschikbaarheid in de voorraad volledig volgen.|
|Niet-voorraad|Doorgaans zijn niet-voorraadartikelen fysieke dingen, zoals bouten of pennen, die een bedrijf gebruikt, maar niet volledig in de voorraad wil bijhouden. Een reden hiervoor kan zijn dat het goedkope artikelen zijn die alleen intern worden gebruikt.|
|Service|Een arbeidstijdseenheid, zoals een adviesuur, voor beperkte bedrijfsondersteuning.|

> [!NOTE]
> De typen **Service** en **Niet-voorraad** bieden geen ondersteuning voor het volgen van voorraadaantallen en -waarden. Alleen geselecteerde artikeltransactietypen en -functies worden ondersteund.

In de volgende tabel worden functies beschreven die de drie artikeltypen ondersteunen.

|Artikelsoort|Verkoop|Inkopen|Projectverbruik|Serviceverbruik|Assemblageverbruik|Productieverbruik|Assemblage-uitvoer|Productieoutput|Locatietransfer|Fysieke telling|Voorraadherwaardering|Voorraadwaardering|Artikeltracering|Reservering|Magazijn|Planning|Orderplanning|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Voorraad|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|
|Niet-voorraad|Ja|Ja|Ja|Ja|Ja|Ja|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Ja|
|Onderhoud|Ja|Ja|Ja|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Ja|

## <a name="costing-methods-for-types-of-items" />Waarderingsmethoden voor soorten artikelen
Als u voorraadtransacties boekt, worden de gewijzigde voorraadaantallen en -waarden vastgelegd in respectievelijk de artikel- en waardeposten. 

Voor voorraadartikelen worden de kosten geregistreerd in het veld **Tot. werk. kosten** op de pagina **Waardeposten** en wanneer deze zijn gereconcilieerd met het grootboek, worden de kosten weergegeven in het veld **Kosten geboekt naar grootboek**. Zie voor meer informatie [Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md).

Voor niet-voorraad- en serviceartikelen worden de kosten geregistreerd in het veld **Kostenbedrag (Niet-inv.)** op de pagina **Waardeposten**. Voor niet-voorraad- en serviceartikelen worden de kosten gespecificeerd op de verkoop-, assembly- en productiedocumenten en -dagboeken. De standaardkosten kunnen worden gespecificeerd in het veld **Kostprijs** op de pagina's **Artikelkaart** en **SKU**. Kosten voor dit soort artikelen worden niet gereconcilieerd met het grootboek. 

## <a name="catalog-and-service-items" />Catalogus- en serviceartikelen
Artikelen die u aan uw klanten aanbiedt, maar die u niet in uw systeem wilt beheren tot u ze begint te verkopen, kunnen worden ingesteld als catalogusartikelen. Catalogusartikelen moeten niet worden verward met normale artikelen van het type Niet-voorraad. Zie voor meer informatie [Werken met catalogusartikelen](inventory-how-work-nonstock-items.md).

Artikelen van klanten waaraan u onderhoud verricht, zoals een printer, worden serviceartikelen genoemd. Serviceartikelen hebben niets van doen met normale of catalogusartikelen. Serviceonderdelen kunnen echter gewone artikelen zijn. Zie voor meer informatie [Serviceartikelen en serviceartikelonderdelen instellen](service-how-setup-service-items.md).

## <a name="see-also" />Zie ook
[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Voorraad instellen](inventory-setup-inventory.md)  
[Voorraadkosten beheren](finance-manage-inventory-costs.md)  
[Voorraad](inventory-manage-inventory.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
