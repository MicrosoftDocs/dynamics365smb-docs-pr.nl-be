---
title: Dimensies instellen | Microsoft Docs
description: "U kunt de dimensies en dimensiewaarden definiëren die u wilt gebruiken om dagboeken en documenten te categoriseren, zoals verkooporders en inkooporders."
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 03/28/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: 0da77c5be3b49f715384752ad61fc072aea8525c
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---
# <a name="setting-up-dimensions"></a>Dimensies instellen
U kunt de dimensies en dimensiewaarden definiëren om dagboeken en documenten te categoriseren, zoals verkooporders en inkooporders. U stelt dimensies in het venster **Dimensies** in. In dit venster maakt u één regel voor elke dimensie, zoals *Project*, *Afdeling*, *District* en *Verkoper*.

U stelt ook waarden voor dimensies in. Waarden kunnen bijvoorbeeld afdelingen in uw bedrijf zijn. Dimensiewaarden kunnen worden ingesteld in een hiërarchische structuur, vergelijkbaar met het rekeningschema, zodat gegevens kunnen worden onderverdeeld in verschillende niveaus en zodat subsets van dimensiewaarden kunnen worden opgeteld. U kunt zoveel dimensies en dimensiewaarden definiëren als u nodig hebt en iedereen in uw bedrijf kan deze gebruiken.

U kunt ook een aantal globale dimensies en shortcutdimensies instellen:  

* **Globale dimensies** worden als filters gebruikt, bijvoorbeeld in rapporten en batchverwerkingen. U kunt slechts twee globale dimensies gebruiken. Kies dus dimensies die u vaak gebruikt.
* **Shortcutdimensies** zijn beschikbaar als velden in dagboek- en documentregels. U kunt maximaal zes shortcutdimensies maken.  

**Opmerking**: voor deze functionaliteit is vereist dat uw ervaring is ingesteld op **Pakket**. Zie [Uw ervaring in [!INCLUDE[d365fin](includes/d365fin_md.md)] aanpassen](ui-experiences.md) voor meer informatie.

## <a name="set-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Standaarddimensies voor klanten, leveranciers en andere rekeningen instellen
U kunt een standaarddimensie toewijzen voor een specifieke rekening. De dimensie wordt naar het dagboek of document gekopieerd wanneer u het rekeningnummer op een regel invoert, maar u kunt de code op de regel desgewenst verwijderen of wijzigen. U kunt ook een dimensie maken die is vereist om een post te boeken met een specifiek rekeningsoort.  

## <a name="translate-the-names-of-dimensions"></a>De namen van dimensies vertalen
Wanneer u een dimensie maakt, en met name een shortcutdimensie, maakt u eigenlijk een aangepast veld of een kolomkop. Als uw bedrijf internationaal is, kunt u vertalingen voor de naam van de dimensie opgeven. In documenten die de dimensie bevatten, wordt indien van toepassing de vertaalde naam gebruikt.   

## <a name="example"></a>Opmerking
Stel dat uw bedrijf transacties wil traceren op basis van organisatorische structuur en geografische locaties. Hiervoor kunt u twee dimensies instellen in het venster **Dimensies**:

* **DISTRICT**  
* **AFDELING**  

| Code | Name | Codebijschrift | Filterbijschrift |
| --- | --- | --- | --- |
| DISTRICT |District |Districtcode |Districtfilter |
| KSTNPLAATS |Kostenplaats |Afdelingscode |Kostenplaatsfilter |

Voor **DISTRICT** voegt u de volgende dimensiewaarden toe:

| Code | Name | Dimensiewaardesoort |
| --- | --- | --- |
| 10 |Noord- en Zuid-Amerika |Begintotaal |
| 2.0 |Noord-Amerika |Standaard |
| 30 |Stille Oceaan |Standaard |
| 40 |Zuid-Amerika |Standaard |
| 50 |Noord- en Zuid-Amerika, totaal |Eindtotaal |
| 60 |Europa |Begintotaal |
| 70 |EU |Standaard |
| 80 |Niet-EU |Standaard |
| 90 |Europa, totaal |Eindtotaal |

Voor de twee belangrijke geografische gebieden, Noord- en Zuid-Amerika en Europa, voegt u subcategorieën toe voor regio's door de dimensiewaarden te laten inspringen. Zo kunt u rapporteren over verkoop of kosten in regio's en totalen ophalen voor de grotere geografische gebieden. U kunt er ook voor kiezen landen of regio's te gebruiken als uw dimensiewaarden, of provincies of plaatsen. Dit hangt af van uw bedrijf.  
**Opmerking**: als u een hiërarchie wilt instellen, moeten de codes in alfabetische volgorde zijn. Dit omvat de codes van de dimensiewaarden die worden verschaft in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Voor **AFDELING** voegt u de volgende dimensiewaarden toe:

| Code | Name | Dimensiewaardesoort |
| --- | --- | --- |
| ADMIN |Beheer |Standaard |
| PROD |Productie |Standaard |
| VERKOOP |Verkoop |Standaard |

Met deze instellingen kunt u vervolgens uw twee dimensies toevoegen als twee globale dimensies in het venster **Boekhoudinstellingen**. Dit betekent dat u DISTRICT en AFDELING kunt gebruiken als filters voor grootboekposten, evenals in alle rapporten en rapportageschema's. Beide globale dimensies kunnen ook automatisch worden gebruikt als shortcutdimensies in postregels en documentkoppen.  

Met deze instelling kunt u beginnen met het toevoegen van dimensies aan documenten en dagboeken. Zie [Dimensies](finance-dimensions.md) voor meer informatie.  

## <a name="see-also"></a>Zie ook
[Dimensies](finance-dimensions.md)  
[Financiën instellen](finance-setup-finance.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

