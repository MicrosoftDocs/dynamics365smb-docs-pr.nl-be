---
title: Werken met dimensies| Microsoft Docs
description: U gebruikt dimensies om posten te categoriseren, bijvoorbeeld per afdeling of project, zodat u gemakkelijk gegevens kunt traceren en analyseren.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 06/14/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 844668124df1897493737b28383a68a2a0a66d10
ms.contentlocale: nl-be
ms.lasthandoff: 09/22/2017

---
# <a name="working-with-dimensions"></a>Werken met dimensies
Als u analyse in documenten zoals verkooporders eenvoudiger wilt maken, kunt u dimensies gebruiken. Dimensies zijn kenmerken en waarden waarmee posten worden gecategoriseerd, zodat u ze kunt bijhouden en analyseren. Dimensies kunnen bijvoorbeeld aangeven tot welk project of welke afdeling een post behoort.  

U kunt dimensies bijvoorbeeld gebruiken in plaats van aparte grootboekrekeningen voor elke afdeling en elk project in te stellen. Hiermee krijgt u uitgebreide mogelijkheden voor analyse zonder een ingewikkeld rekeningschema te maken. Zie voor meer informatie [Bedrijfsinformatie](bi.md).

Een ander voorbeeld is een dimensie in te stellen met de naam *Afdeling* en deze dimensie te gebruiken wanneer u verkoopdocumenten boekt. Zo kunt u met BI-programma´s bekijken welke afdeling welke artikelen heeft verkocht.
Hoe meer dimensies u gebruikt, hoe gedetailleerder de rapporten waarop u uw bedrijfsbeslissingen kunt baseren. Eén verkooppost kan bijvoorbeeld meerdere dimensiegegevens bevatten, zoals:  

* De rekening waarnaar de artikelverkoop is geboekt  
* Waar het artikel is verkocht
* Wie het heeft verkocht
* Het soort klant die het artikel heeft gekocht  

> [!NOTE]  
>   Deze functionaliteit vereist dat uw ervaring is ingesteld op **Suite**. Zie voor meer informatie [Uw [!INCLUDE[d365fin](includes/d365fin_md.md)]-ervaring aanpassen](ui-experiences.md).

## <a name="analyzing-by-dimensions"></a>Analyseren per dimensies
De dimensiefunctionaliteit speelt een belangrijke rol in bedrijfsinformatie, zoals bij het definiëren van analyseweergaven. Zie voor meer informatie [Procedure: gegevens analyseren per dimensies](bi-how-analyze-data-dimension.md).

> [!TIP]
> Als snelle manier om transactiegegevens te analyseren per dimensie kunt u totalen in het rekeningschema en posten in de vensters **Posten** filteren op dimensie. Zoek de actie **Dimensiefilter instellen**.

## <a name="dimension-sets"></a>Dimensiesets
Een dimensieset is een unieke combinatie dimensiewaarden. Een dimensieset wordt als dimensiesetposten in de database opgeslagen. Elke dimensiesetpost vertegenwoordigt één dimensiewaarde. De dimensiesetpost wordt geïdentificeerd door een gemeenschappelijke dimensieset-id die is toegewezen aan elke dimensiesetpost die tot de dimensieset behoort.  

Wanneer u een dagboekregel, documentkop of documentregel maakt, kunt u een combinatie van dimensiewaarden opgeven. In plaats van elke dimensiewaarde expliciet in de database op te slaan, wordt een dimensieset-id toegewezen aan de dagboekregel, documentkop of documentregel om zo de dimensieset op te geven.  

## <a name="setting-up-dimensions"></a>Dimensies instellen
U kunt de dimensies en dimensiewaarden definiëren om dagboeken en documenten te categoriseren, zoals verkooporders en inkooporders. U stelt dimensies in het venster **Dimensies** in. In dit venster maakt u één regel voor elke dimensie, zoals *Project*, *Afdeling*, *District* en *Verkoper*.

U stelt ook waarden voor dimensies in. Waarden kunnen bijvoorbeeld afdelingen in uw bedrijf zijn. Dimensiewaarden kunnen worden ingesteld in een hiërarchische structuur, vergelijkbaar met het rekeningschema, zodat gegevens kunnen worden onderverdeeld in verschillende niveaus en zodat subsets van dimensiewaarden kunnen worden opgeteld. U kunt zoveel dimensies en dimensiewaarden definiëren als u nodig hebt en iedereen in uw bedrijf kan deze gebruiken.

U kunt ook een aantal globale dimensies en shortcutdimensies instellen:  

* **Globale dimensies** worden als filters gebruikt, bijvoorbeeld in rapporten en batchverwerkingen. U kunt slechts twee globale dimensies gebruiken. Kies dus dimensies die u vaak gebruikt.
* **Shortcutdimensies** zijn beschikbaar als velden in dagboek- en documentregels. U kunt maximaal zes shortcutdimensies maken.  

### <a name="setting-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Standaarddimensies instellen voor klanten, leveranciers en andere rekeningen
U kunt een standaarddimensie toewijzen voor een specifieke rekening. De dimensie wordt naar het dagboek of document gekopieerd wanneer u het rekeningnummer op een regel invoert, maar u kunt de code op de regel desgewenst verwijderen of wijzigen. U kunt ook een dimensie maken die is vereist om een post te boeken met een specifiek rekeningsoort.  

### <a name="translating-the-names-of-dimensions"></a>De namen van dimensies vertalen
Wanneer u een dimensie maakt, en met name een shortcutdimensie, maakt u eigenlijk een aangepast veld of een kolomkop. Als uw bedrijf internationaal is, kunt u vertalingen voor de naam van de dimensie opgeven. In documenten die de dimensie bevatten, wordt indien van toepassing de vertaalde naam gebruikt.   

### <a name="example-of-dimension-setup"></a>Voorbeeld van dimensie-instelling
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
> [!NOTE]  
>   Als u een hiërarchie wilt instellen, moeten de codes op alfabetische volgorde staan Dit omvat de codes van de dimensiewaarden die worden verschaft in [!INCLUDE[d365fin](includes/d365fin_md.md)].  

Voor **AFDELING** voegt u de volgende dimensiewaarden toe:

| Code | Name | Dimensiewaardesoort |
| --- | --- | --- |
| ADMIN |Beheer |Standaard |
| PROD |Productie |Standaard |
| VERKOOP |Verkoop |Standaard |

Met deze instellingen kunt u vervolgens uw twee dimensies toevoegen als twee globale dimensies in het venster **Boekhoudinstellingen**. Dit betekent dat u DISTRICT en AFDELING kunt gebruiken als filters voor grootboekposten, evenals in alle rapporten en rapportageschema's. Beide globale dimensies kunnen ook automatisch worden gebruikt als shortcutdimensies in postregels en documentkoppen.  

## <a name="using-dimensions"></a>Dimensies gebruiken
In een document zoals een verkooporder kunt u dimensiegegevens toevoegen voor een afzonderlijke documentregel en voor het document zelf. In het venster **Verkooporder** kunt u bijvoorbeeld dimensiewaarden invoeren voor de eerste twee shortcutdimensies op de afzonderlijke verkoopregels, en u kunt meer dimensiegegevens toevoegen als u de knop **Dimensies** kiest.  

Als u in plaats daarvan in een dagboek werkt, kunt u ook op dezelfde manier dimensiegegevens toevoegen aan een post als u shortcutdimensies direct als velden hebt ingesteld op dagboekregels.  

U kunt standaarddimensies instellen voor rekeningen of rekeningsoorten, zodat dimensies en dimensiewaarden automatisch worden ingevuld.

## <a name="see-also"></a>Zie ook
[Bedrijfsinformatie](bi.md)  
[Financiën](finance.md)  
[Procedure: Gegevens analyseren per dimensie](bi-how-analyze-data-dimension.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  

