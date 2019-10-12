---
title: Artikeltypen | Microsoft Docs
description: U kunt de voorraadwaarde van een artikel herwaarderen met de waarderingsmethoden FIFO of Gemiddeld, bijvoorbeeld als de kosten van een artikel veranderen om andere redenen dan transacties.
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 10/01/2019
ms.author: sgroespe
ms.openlocfilehash: 91a0a1d00972f33d3d934e12274a8567b8157cea
ms.sourcegitcommit: 02e704bc3e01d62072144919774f1244c42827e4
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2019
ms.locfileid: "2308560"
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

> [!NOTE]
> Artikelen die u aan uw klanten aanbiedt, maar die u niet in uw systeem wilt beheren tot u ze begint te verkopen, kunnen worden ingesteld als catalogusartikelen. Catalogusartikelen moeten niet worden verward met normale artikelen van het type Niet-voorraad. Zie voor meer informatie [Werken met catalogusartikelen](inventory-how-work-nonstock-items.md).

> [!NOTE]
> Artikelen van klanten waaraan u onderhoud verricht, zoals een printer, worden serviceartikelen genoemd. Serviceartikelen hebben niets van doen met normale of catalogusartikelen. Serviceonderdelen kunnen echter gewone artikelen zijn. Zie voor meer informatie [Serviceartikelen en serviceartikelonderdelen instellen](service-how-setup-service-items.md).

## <a name="see-also"></a>Zie ook
[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Voorraad instellen](inventory-setup-inventory.md)  
[Voorraadkosten beheren](finance-manage-inventory-costs.md)  
[Voorraad](inventory-manage-inventory.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
