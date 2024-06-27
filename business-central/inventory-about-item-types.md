---
title: Artikeltypen begrijpen
description: Meer informatie over de typen artikelen die u in de voorraad kunt beheren en hoe deze typen van invloed zijn. U kunt de voorraadwaardering van een artikel aanpassen met behulp van de FIFO- of Gemiddelde-waarderingsmethode wanneer de artikelkosten om andere redenen dan transacties veranderen.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: bholtorf
ms.topic: conceptual
ms.search.keywords: null
ms.search.form: '9297, 5845, 30,'
ms.date: 05/24/2024
ms.service: dynamics-365-business-central
ms.custom: bap-template
---
# <a name="about-item-types"></a>Over artikeltypen

In het veld **Soort** op de pagina **Artikelkaart** kunt u selecteren waarvoor het artikel in uw bedrijf wordt gebruikt. Dit heeft invloed op de mate waarin u het artikel kunt beheren in de voorraad. In de volgende tabel worden de drie soorten artikelen vermeld en beschreven die beschikbaar zijn.

|Optie|Gebruikelijk doel|
|------|-----------|
|Voorraad|Fysieke zaken, zoals fietsen, telefoons en bureaus, waarvoor u alle voorraadprocessen wilt kunnen gebruiken. Voorraadartikelen kunnen ook niet-fysieke items omvatten, zoals softwarelicenties en abonnementen, als de artikelen identificatienummers hebben, zoals serienummers. U kunt artikelwaarden en beschikbaarheid in de voorraad volledig volgen.|
|Niet-voorraad|Doorgaans zijn niet-voorraadartikelen fysieke dingen, zoals bouten of pennen, die uw bedrijf gebruikt, maar niet volledig in de voorraad wil bijhouden. Een reden hiervoor kan zijn dat het goedkope artikelen zijn die alleen intern worden gebruikt.|
|Onderhoud|Een arbeidstijdseenheid, zoals een adviesuur, voor beperkte bedrijfsondersteuning.|

> [!NOTE]
> Met de typen **Service** en **Niet-voorraad** kunt u geen voorraadaantallen en -waarden bijhouden. Alleen geselecteerde artikeltransactietypen en -functies worden ondersteund. In de volgende tabel worden functies beschreven die de drie artikeltypen ondersteunen.

|Artikelsoort|Verkoop|Inkopen|Projectverbruik|Serviceverbruik|Assemblageverbruik|Productieverbruik|Assemblage-uitvoer|Productieoutput|Locatietransfer|Fysieke telling|Voorraadherwaardering|Voorraadwaardering|Artikeltracering|Reservering|Magazijn|Planning|Orderplanning|
|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Voorraad|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|Ja|
|Niet-voorraad|Ja|Ja|Ja|Ja|Ja|Ja|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Ja|
|Onderhoud|Ja|Ja|Ja|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Nr.|Ja|

## <a name="costing-methods-for-types-of-items"></a>Waarderingsmethoden voor soorten artikelen

Als u voorraadtransacties boekt, worden de gewijzigde voorraadaantallen en -waarden vastgelegd in respectievelijk de artikel- en waardeposten.

U legt de kosten van voorraadartikelen vast in het veld **Kostenbedrag (werkelijk)** op de pagina **Waardeposten**. Wanneer u de post in het grootboek reconcilieert, worden de kosten weergegeven in het veld **Kosten geboekt naar grootboek**. Ga voor meer informatie over voorraadkosten naar [Ontwerpdetails: Voorraadwaardering](design-details-inventory-costing.md).

Voor niet-voorraad- en serviceartikelen worden de kosten geregistreerd in het veld **Kostenbedrag (Niet-inv.)** op de pagina **Waardeposten**. Voor niet-voorraad- en serviceartikelen worden de kosten gespecificeerd op de verkoop-, assembly- en productiedocumenten en -dagboeken. Geef de standaardkosten op in het veld **Kostprijs** op de pagina's **Artikelkaart** en **SKU**. Kosten voor dit soort artikelen worden niet gereconcilieerd met het grootboek.

## <a name="catalog-and-service-items"></a>Catalogus- en serviceartikelen

U kunt artikelen instellen die u aan uw klanten aanbiedt, maar die u niet in uw systeem beheert tot u ze verkoopt als catalogusartikelen. Hoewel catalogusartikelen vergelijkbaar zijn met reguliere artikelen van het type **Niet-voorraad**, moet u de twee niet verwarren, want er zijn verschillen. Ga voor meer informatie naar [Werken met catalogusartikelen](inventory-how-work-nonstock-items.md).

Artikelen van klanten waaraan u onderhoud verricht, zoals een printer, worden serviceartikelen genoemd. Serviceartikelen hebben niets van doen met normale of catalogusartikelen. Serviceonderdelen kunnen echter gewone artikelen zijn. Ga voor meer informatie naar [Serviceartikelen en serviceartikelonderdelen instellen](service-how-setup-service-items.md).

## <a name="see-also"></a>Zie ook

[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Voorraad instellen](inventory-setup-inventory.md)  
[Voorraadkosten beheren](finance-manage-inventory-costs.md)  
[Voorraad](inventory-manage-inventory.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
