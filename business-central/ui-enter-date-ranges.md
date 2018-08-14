---
title: Datumbereiken instellen in Business Central | Microsoft Docs
description: Leren hoe u een rapport kunt verkrijgen om gegevens te tonen uit specifieke tijdperioden met behulp van datumbereiken in Business Central.
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: dates, reporting, filter
ms.date: 07/05/2018
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7664360941313da6ea0b797ef00df2e9810ad62
ms.openlocfilehash: ff63ae71a78f956dddb7b5247ee66f9416cf7cf1
ms.contentlocale: nl-be
ms.lasthandoff: 07/09/2018

---
# <a name="entering-date-ranges"></a>Datumbereiken invoeren
U kunt filters met een begin- en einddatum instellen om alleen de gegevens in dat datumbereik of tijdsinterval in te stellen. Voor het instellen van een datumbereik gelden speciale regels. Neem als voorbeeld de **Klanten top 10**:

![Een datumbereik instellen op de aanvraagpagina voor de lijst Klanten top 10](./media/ui-enter-date-ranges/customer-top10-list.png)

Hier kunt u de lijst tot een datumbereik beperken, zoals de afgelopen 2 weken of een totaal van 6 weken, of wat voor bereik u ook nodig hebt. Als u datumbereiken wilt invoeren, voert u datums in en gebruikt u **..** of **|** om het bereik in te stellen. Als u in ons voorbeeld de top 10 klanten voor de eerste twee weken van mei wilt invoeren, stelt u het datumfilter in op *05 01 17..05 14 17*.
Hier volgen enkele andere voorbeelden:

| Betekenis | Opmerking | Opgenomen posten |
|---|---|---|
|Gelijk aan| 12 15 16 |Alleen posten die zijn geboekt op 15 december 2016.|
|Interval| 12 15 16..01 15 17<br /><br />..12 15 16|Posten die zijn geboekt in de periode tussen en tot en met 15 december 2016 en 15 januari 2017.<br /><br />Posten die zijn geboekt op 15 december 2016 of eerder.|
|Of/of|12 15 16&#124;12 16 16|Posten die zijn geboekt op 15 december of 16 december 2016. Als deze posten zijn geboekt op beide dagen, worden ze allebei weergegeven.|

U kunt de verschillende notatiesoorten ook combineren.

| Opmerking | Opgenomen posten |
|---|---|
|12 15 16&#124;12 01 16..05 31 17 | Posten die zijn geboekt op 15 december 2016 of op datums tussen en tot en met 1 december 2016 en 31 mei 2017. |
|..12 14 16&#124;12 30 16.. | Posten die zijn geboekt op 14 december of eerder, of posten die zijn geboekt op 30 december of later. Dit wil zeggen, alle posten behalve die zijn geboekt tussen 15 december en 29 december tot en met. |

U ziet dat we hier de Amerikaanse datumnotatie MMDDYY hebben gebruikt. Zodra [!INCLUDE[d365fin](includes/d365fin_md.md)] beschikbaar wordt in andere markten, zult u de indelingen kunnen gebruiken die u gewend bent.

## <a name="using-date-formulas"></a>Datumformules gebruiken
Een datumformule is een korte, afgekorte combinatie van letters en cijfers op basis waarvan datums worden berekend. U kunt datumformules invoeren in verschillende datumberekeningsvelden en in de frequentievelden van periodieke dagboeken.

> [!NOTE]
>  In alle datumformulevelden wordt automatisch één dag opgenomen om ervoor te zorgen dat de huidige dag wordt gebruikt als begindatum van de periode. Als u dus bijvoorbeeld **1W** invoert, zal de periode in feite acht dagen bestrijken omdat vandaag ook is opgenomen. Als u een periode van zeven dagen (exact één week) wilt opgeven, inclusief de begindatum van de periode, moet u **6D** of **1W\-1D**. opgeven.

Hier volgen enkele voorbeelden van het gebruik van datumformules:

-   De datumformule in de frequentievelden van periodieke dagboeken geeft aan hoe vaak de dagboekregel moet worden geboekt.

-   De datumformule in het veld **Respijtperiode** van een bepaald aanmaningsniveau bepaalt hoelang de vervaldatum (of de vervaldatum van de vorige aanmaning) moet zijn verstreken voordat een aanmaning wordt gemaakt.

-   De datumformule in het veld **Vervaldatumformule** bepaalt hoe de vervaldatum voor de aanmaning wordt berekend.

In de berekeningsformule voor de datum kunt u maximaal 20 tekens gebruiken (cijfers en/of letters). U kunt de volgende letters gebruiken als afkorting voor tijdsaanduidingen.

|  Letter  |  Tijdspecificatie  |
|----------|----------------------|
|U|Actueel|
|D|Dag\(en\)|
|W|We(e)k\(en\)|
|M|Maand\(en\)|
|K|Kwarta(a)l\(en\)|
|J|Ja(a)r\(en\)|

Er zijn drie soorten datumformules.

In het volgende voorbeeld wordt weergegeven hoe **C** kan worden gebruikt voor huidig en een tijdseenheid.

|  Expressie  |  Betekenis  |
|--------------|-----------|
|LW|Lopende week|
|LM|Lopende maand|

In het volgende voorbeeld wordt weergegeven hoe een getal en een tijdseenheid moet worden gebruikt. Nummers mogen niet groter zijn dan 9999.

|  Expressie  |  Betekenis  |
|--------------|-----------|
|10D|10 dagen vanaf vandaag|
|2W|2 weken vanaf vandaag|

In het volgende voorbeeld wordt weergegeven hoe een tijdseenheid en een getal moet worden gebruikt.

|  Expressie  |  Betekenis  |
|--------------|-----------|
|D10|De volgende tiende dag van een maand|
|WD4|De volgende vierde dag van een week \(donderdag\)|

Het volgende voorbeeld geeft weer hoe u deze drie soorten naar wens kunt combineren.

|  Expressie  |  Betekenis  |
|--------------|-----------|
|CM\+10D|Lopende maand \+ 10 dagen|

In het volgende voorbeeld ziet u hoe u een minteken gebruikt om een datum in het verleden aan te duiden.

|  Expressie  |  Betekenis  |
|--------------|-----------|
|-1J|1 jaar geleden vanaf vandaag|

> [!IMPORTANT]
>  Als de vestiging een basisagenda gebruikt, wordt de datumformule die u invoert in dit veld, bijvoorbeeld het veld **Verzendtijd** beschouwd als agendawerkdag. Bijvoorbeeld: **1W** betekent zeven werkdagen.

## <a name="see-also"></a>Zie ook
[Werken met [!INCLUDE[d365fin](includes/d365fin_long_md.md)]](ui-work-product.md)  
[Datumberekening voor inkoop](purchasing-date-calculation-for-purchases.md)  
[Criteria in filters invoeren](ui-enter-criteria-filters.md)  

