---
title: Handmatig btw-correcties doorvoeren
description: U kunt geboekte btw-posten corrigeren zonder de correctie in de btw- of grootboekposten te boeken. Dit is handig als u de btw-bedragen voor de totale verkoop of inkoop moet wijzigen zonder de btw-basis te wijzigen. U kunt btw bijvoorbeeld handmatig corrigeren als u een factuur ontvangt van een leverancier die de btw verkeerd heeft berekend.
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 6d0f874acd85464181e18c094cd9e3d94cce6786
ms.contentlocale: nl-be
ms.lasthandoff: 03/22/2018

---
# <a name="make-manual-corrections-to-vat"></a>Handmatig btw-correcties doorvoeren
U kunt geboekte btw-posten corrigeren zonder de correctie in de btw- of grootboekposten te boeken. Dit is handig als u de btw-bedragen voor de totale verkoop of inkoop moet wijzigen zonder de btw-basis te wijzigen. U kunt btw bijvoorbeeld handmatig corrigeren als u een factuur ontvangt van een leverancier die de btw verkeerd heeft berekend.  

## <a name="to-make-manual-corrections-to-vat"></a>Handmatig btw-correcties doorvoeren  

1.  Klik op het pictogram ![Zoeken naar pagina of rapport](../../media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport"), voer **Btw-aangiftevoorbeeld** in en klik vervolgens op de gerelateerde koppeling.  
2.  Selecteer de regel die moet worden gecorrigeerd. U kunt de btw-correctie voor de rijen **Vak-/Rubrieksamentelling** en **Btw-postentotaal** doorvoeren bij **Soort**.  
3.  Kies het veld **Correctiebedrag** om de correctie door te voeren. Het venster **Lijst met handmatige btw-correcties** wordt geopend.  
4.  Kies de actie **Lijst bewerken**. Vul in het nieuwe venster **Lijst met handmatige btw-correcties** de velden in zoals wordt beschreven in de volgende tabel.  

    |Veld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Boekingsdatum**|Voer de boekingsdatum van de btw-correctie in.|  
    |**Bedrag**|Voer het bedrag van de btw-correctie in. U moet het correctiebedrag invoeren, niet het nieuwe bedrag. Als het bedrag 1000,00 is en dit 1200,00 moet zijn, voert u bijvoorbeeld 200,00 in.|  
    |**Bedrag (Rapp.-val.)**|Dit veld bevat het bedrag van de btw-correctie in de rapportagevaluta.<br /><br /> Het veld wordt automatisch berekend, op basis van de inhoud van het veld **Bedrag** en de actuele wisselkoers voor het omrekenen.|  

5.  Kies de knop **OK**.  
6.  Vernieuw het venster **Btw-aangiftevoorbeeld** om uw correcties te bekijken.  
7.  Als u een rapport met betrekking tot het voorbeeld van de btw-informatie wilt bekijken, kiest u een van de volgende acties:  

    |Actie|Description|  
    |------------|---------------------------------------|  
    |**Gedetailleerd rapport**|Hiermee opent u het rapport **Btw-aangifte**. Zie Btw-aangifte voor meer informatie.|  
    |**Formulier/Intervat-aangifte**|Hiermee opent u het rapport **Btw - Formulier**. Zie Btw - Formulier voor meer informatie.<br /><br /> Het rapport **Formulier/Intervat-aangifte** is gebaseerd op de btw-aangiftesjabloon die is gedefinieerd in de boekhoudinstellingen. Daarom kunnen er gegevens worden geëxporteerd die niet overeenkomen met wat in het venster **Btw-aangiftevoorbeeld** wordt weergegeven.|  
    |**Aangifteoverzichtsrapport**|Hiermee opent u het rapport **Btw-aangifteoverzicht**. Zie Btw-aangifteoverzicht voor meer informatie.|  

## <a name="see-also"></a>Zie ook  
 [Belgische btw](belgian-vat.md)   
 [Periodieke btw-rapporten afdrukken](how-to-print-periodic-vat-reports.md)   
 [Niet-aftrekbare btw instellen](how-to-set-up-non-deductible-vat.md)

