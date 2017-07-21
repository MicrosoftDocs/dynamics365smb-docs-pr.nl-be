---
title: Aangepaste lay-outs voor een rapport of document maken | Microsoft Docs
description: Leren hoe u uw eigen, aangepaste lay-outs maakt om de weergave aan te passen van een rapport wanneer het wordt bekeken, afgedrukt of opgeslagen.
services: project-madeira
documentationcenter: 
author: SusanneWindfeldPedersen
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: customized report, document layout, logo, personalize
ms.date: 03/29/2017
ms.author: solsen
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: 551e838c2896470f9ee620f4ca09a6af3377b458
ms.contentlocale: nl-be
ms.lasthandoff: 07/07/2017


---
# <a name="how-to-create-a-custom-report-or-document-layout"></a>Procedure: Een aangepaste lay-out voor een rapport of document maken
Standaard heeft een rapport een ingebouwde rapportlay-out die een RDLC-rapportlay-out, een Word-rapportlay-out of beide kan zijn. U kunt geen ingebouwde lay-outs wijzigen. U kunt echter uw eigen aangepaste lay-outs maken waarmee u de weergave van een rapport kunt wijzigen wanneer het wordt weergegeven, afgedrukt of opgeslagen. U kunt meerdere aangepaste lay-outs voor hetzelfde rapport maken en vervolgens indien nodig de lay-out wijzigen die door het rapport wordt gebruikt.

> [!NOTE]  
>   In [!INCLUDE[d365fin](includes/d365fin_md.md)] omvat de term 'rapport' ook documenten die extern worden verspreid, zoals verkoopfacturen en orderbevestigingen die u aan klanten als pdf-bestanden verzendt.

Als u een aangepaste lay-out wilt maken, kunt u een kopie van een bestaande lay-out maken of een nieuwe aangepaste lay-out toevoegen, die in de meeste gevallen is gebaseerd op een ingebouwde lay-out. Wanneer u een nieuwe aangepaste lay-out toevoegt, kunt u een RDLC-rapportlay-out, een Word-rapportlay-out of beide kiezen. De nieuwe aangepaste lay-out wordt automatisch gebaseerd op de ingebouwde lay-out voor het rapport, als er een is. Als er geen ingebouwde lay-out is voor het soort, wordt een nieuwe, lege lay-out gemaakt die u nog helemaal moet wijzigen en ontwerpen. Zie [Rapportlay-outs beheren](ui-manage-report-layouts.md) voor meer informatie over RDLC- en Word-rapportlay-outs, ingebouwde en aangepaste lay-outs.  

## <a name="to-create-a-custom-layout"></a>Een aangepaste lay-out maken
1. Kies het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Search for Page or Report icon"), voer **Selectie van rapportlay-out** in en kies vervolgens de gerelateerde koppeling.  
   Het venster** Selectie rapportlay-out** bevat een overzicht van alle rapporten die beschikbaar zijn in het bedrijf dat in het veld Bedrijf boven aan het venster wordt opgegeven.
2. Stel het veld **Bedrijf** in op het bedrijf waarin u de rapportlay-out wilt maken.
3. Selecteer de rij voor het rapport waarvoor u de lay-out wilt maken, en kies vervolgens **Aangepaste lay-outs**.  
   In het venster **Aangepaste rapportlay-outs** worden alle aangepaste lay-outs weergegeven die beschikbaar zijn voor het geselecteerde rapport.
4. Als u een kopie van een bestaande aangepaste lay-out wilt maken, selecteert u de bestaande aangepaste lay-out in de lijst en kiest u vervolgens **Kopiëren**.  
   De kopie van de aangepaste lay-out wordt in het venster **Aangepaste rapportlay-outs** weergegeven en bevat de woorden Kopie van in het veld.
5. Als u een nieuwe aangepaste lay-out wilt toevoegen die op een ingebouwde lay-out is gebaseerd, doet u het volgende:  
   1. Kies **Nieuwe**. Het venster **Ingebouwde lay-out voor een rapport invoegen** verschijnt. De velden **Id** en **Naam** worden automatisch ingevuld.
   2. Als u een aangepaste Word-rapportlay-out wilt toevoegen, schakelt u het selectievakje **Word-lay-out invoegen** in.
   3. Als u een aangepaste RDLC-rapportlay-out wilt toevoegen, schakelt u het selectievakje **RDLC-lay-out invoegen** in.
   4. Kies de knop **Ok**.  
      De nieuwe aangepaste lay-outs worden weergegeven in het venster **Aangepaste rapportlay-outs**. Als een nieuwe lay-out wordt gebaseerd op een ingebouwde lay-out, bevat deze de woorden **Kopie van een ingebouwde lay-out** in het veld **Beschrijving**. Als er geen ingebouwde lay-out voor het rapport was, bevat de nieuwe lay-out de woorden **Nieuwe lay-out** in het veld **Beschrijving**, wat aangeeft dat de aangepaste lay-out leeg is.
6. Standaard is het veld **Bedrijfsnaam** leeg, wat betekent dat de aangepaste lay-out beschikbaar voor het rapport is in alle bedrijven. Als u de aangepaste lay-out alleen beschikbaar wilt maken voor een specifiek bedrijf, kiest u **Bewerken** en stelt u het veld **Bedrijfsnaam** in op het gewenste bedrijf.

## <a name="see-also"></a>Zie ook
[Rapportlay-outs beheren](ui-manage-report-layouts.md)  
[Procedure: Wijzigen welke lay-out momenteel in een rapport wordt gebruikt](ui-how-change-layout-currently-used-report.md)  
[Werken met [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)

