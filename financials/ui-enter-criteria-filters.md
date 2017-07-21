---
title: "Zoekcriteria in filters definiëren | Microsoft Docs"
description: Beschrijft hoe u met filters werkt, zoals het Snelfilter, om de resultaten te verfijnen die u krijgt wanneer u gegevens zoekt.
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: delimit, FlowFilter
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 86ca45493081d9dbd229548f7c560e1df4e1c7c3
ms.contentlocale: nl-be
ms.lasthandoff: 07/07/2017


---
# <a name="entering-criteria-in-filters"></a>Criteria in filters invoeren
Wanneer u naar gegevens, zoals klantnamen, adressen of productgroepen wilt zoeken, voert u criteria in. In zoekcriteria kunt u alle cijfers en letters gebruiken die u normaal in het specifieke veld gebruikt. Daarnaast kunt u speciale symbolen gebruiken om de resultaten verder te filteren.

## <a name="searching-using-the-quick-filter"></a>Zoeken met het Snelfilter
U kunt filters toevoegen aan alle pagina's met het Snelfilter. Het Snelfilter wordt ingeschakeld door het vergrootglaspictogram in de rechterbovenhoek van een pagina te kiezen. Dit type filter wordt gebruikt voor een snelle invoer van criteria.

> [!IMPORTANT]  
>   Het snelfilter biedt een eenvoudig toegang tot filtergegevens door onbewerkte tekst in te voeren, maar biedt ook veel opties voor zoekcriteria. Afhankelijk van of u normale tekst of tekst met symbolen invoert, werkt het snelfilter anders.  

* Als u gewone tekst in de zoekcriteria opgeeft, worden de zoekcriteria geïnterpreteerd als een hoofdletterongevoelige zoekactie die bepaalde tekst bevat.  
* Als u tekst inclusief symbolen in de zoekcriteria opgeeft, worden de zoekcriteria precies zo geïnterpreteerd als u ze hebt ingevoerd en wordt onderscheid gemaakt tussen hoofdletters en kleine letters.

### <a name="quick-filter-criteria"></a>Snelfiltercriteria
<!-- html syntax because symbols conflict with MarkDown syntax -->
<TABLE>
  <TR>
    <TH>Zoekcriteria</TH>
    <TH>Geïnterpreteerd als...</TH>
    <TH>Retourneert...</TH>
  </TR>
  <TR>
    <TD>man</TD>
    <TD>@&#42;man&#42;</TD>
    <TD>Alle records met de tekst <b>man</b> en ongevoelig voor hoofdletters en kleine letters.</TD>
  </TR>
  <TR>
    <TD>se</TD>
    <TD>@&#42;zo&#42;</TD>
    <TD>Alle records met de tekst <b>se</b> en ongevoelig voor hoofdletters en kleine letters.</TD>
  </TR>
  <TR>
    <TD>Man&#42;</TD>
    <TD>Begint met <b>Man</b> en is hoofdlettergevoelig.</TD>
    <TD>Alle records die beginnen met de tekst <b>Man</b>.</TD>
  </TR>
  <TR>
    <TD>'man'</TD>
    <TD>Een exacte tekst en gevoelig voor hoofdletters en kleine letters.</TD>
    <TD>Alle records die precies overeenkomen met <b>man</b>.</TD>
  </TR>
  <TR>
    <TD>@man* </TD>
    <TD>Begint met en is niet hoofdlettergevoelig.</TD>
    <TD>Alle records die beginnen met <b>man</b>.</TD>
  </TR>
    <TR>
    <TD>@&#42;man</TD>
    <TD>Eindigt met en is niet hoofdlettergevoelig.</TD>
    <TD>Alle records die eindigen met <b>man</b>.</TD>
  </TR>
</TABLE>

> [!NOTE]  
>   U kunt geen jokerteken gebruiken bij het filteren op opsommingsvelden, zoals het veld **Status** op verkooporders. Om een filter voor deze veldsoort in te voeren, kunt u de numerieke waarde als een filterparameter invoeren. Bijvoorbeeld: gebruik in het veld **Status** op een verkooporder met de waarden **Open**, **Vrijgegeven**, **Wacht op goedkeuring** en **Wacht op vooruitbetaling** de waarden **0**, **1**, **2** en **3** om voor deze opties te filteren.  

## <a name="see-also"></a>Zie ook
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

