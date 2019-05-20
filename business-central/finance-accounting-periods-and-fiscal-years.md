---
title: Werken met boekingsperioden en boekjaren | Microsoft Docs
description: Leren werken met boekhoudperioden om te definiëren wanneer uw bedrijf financiële prestaties rapporteert.
services: project-madeira
documentationcenter: ''
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2019
ms.author: bholtorf
ms.openlocfilehash: 50df903e664f98f038a82c646dd3bd9c2f5ef479
ms.sourcegitcommit: 60b87e5eb32bb408dd65b9855c29159b1dfbfca8
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 04/29/2019
ms.locfileid: "1239096"
---
# <a name="working-with-accounting-periods-and-fiscal-years"></a>Werken met boekingsperioden en boekjaren
Boekhoudperioden, ook wel rapportageperioden genoemd, zijn perioden waarvoor een bedrijf of organisatie financiële prestaties rapporteert, bijvoorbeeld door de balans of resultatenrekening te genereren. Meestal verwijzen boekhoudperioden naar het boekjaar van het bedrijf, dat verschillende boekingsperioden zoals maanden of kwartalen kan bevatten.

Voor veel bedrijven valt het boekjaar niet samen met het kalenderjaar. Het boekjaar eindigt bijvoorbeeld op 30 juni in plaats van 31 december. Voor nieuw gemaakte bedrijven kan het fiscale jaar langer zijn dan 12 maanden. 

[!INCLUDE[d365fin](includes/d365fin_md.md)] vereist alleen boekingsperioden als u een resultatenrekening wilt afsluiten of gegevenscompressietaken wilt uitvoeren. 

U kunt boekingsperioden gebruiken in rapportage. Bijvoorbeeld als u geboekte posten op de pagina **Saldo/Budget** controleert waar het rapportage-interval kan worden opgegeven. Een van de opties die u kunt opgeven om te rapporteren per boekhoudperiode. U kunt ook een rapportageschema maken dat resultaten voor verschillende boekingsperioden vergelijkt.

## <a name="creating-a-new-fiscal-year"></a>Een nieuw boekjaar maken
U kunt boekingsperioden in bulk maken door de batchverwerking **Boekjaar maken** te gebruiken of handmatig.

### <a name="how-to-create-accounting-periods-in-bulk"></a>Boekhoudperioden in bulk maken
Gebruik de batchverwerking **Boekjaar maken** om een boekjaar in perioden van gelijke lengte op te delen.  

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Boekingsperioden** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies de actie **Jaar maken**.  <!--What about the Scheduling option? Should we mention that? There's also the Report Output Type field...-->
3. Voer in het veld **Begindatum** de datum in waarop het boekjaar begint.  
4. Voer in het veld **Aantal perioden** het aantal boekhoudperioden in waarin u het boekjaar wilt verdelen. Er kunnen maximaal 365 perioden in een jaar vallen.  
5. Voer in het veld **Periodelengte** de duur voor elke periode in. Bijvoorbeeld 1M voor één maand, 1K voor één kwartaal en 1J voor één jaar.  
6. Klik op **OK**.  

### <a name="how-to-create-accounting-periods-manually"></a>Boekhoudperioden handmatig maken
Als de boekhoudperioden in uw boekjaar verschillende duren hebben, zoals de 4-4-5 agenda die in detailhandel wordt gebruikt, kunt u het handmatig instellen.  
  
1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Boekingsperioden** in en klik vervolgens op de gerelateerde koppeling.  
2. Voer in het veld **Begindatum** de datum in waarop het boekjaar begint. Het veld **Naam** bevat de naam van de maand.  
3. Kies het selectievakje **Nieuw boekjaar** om aan te geven dat dit de eerste periode in het jaar is. [!INCLUDE[d365fin](includes/d365fin_md.md)] gebruikt deze periode om te bepalen welke perioden aan het einde van het jaar moeten worden afgesloten.
4. Herhaal stap 2 en 3 voor elke resterende periode.  

## <a name="closing-a-fiscal-year"></a>Een fiscaal jaar afsluiten
Het afsluiten van het boekjaar is een van de taken voor het afsluiten van de boeken. Nadat u het boekjaar hebt afgesloten, zijn de selectievakjes **Afgesloten** en **Geblokkeerd** ingeschakeld voor alle perioden van het jaar. U kunt een boekjaar niet opnieuw openen of de selectievakjes uitschakelen.

> [!NOTE]  
>  U moet altijd minimaal één open boekjaar hebben. Wanneer u een jaar afsluit, moet u ervoor zorgen dat een nieuw jaar is gemaakt. Houd er ook rekening mee dat als u een jaar afsluit, u de begindatum van het volgende jaar niet kunt wijzigen.

1. Klik op het pictogram ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "pictogram Zoeken naar pagina of rapport"), voer **Boekingsperioden** in en klik vervolgens op de gerelateerde koppeling.  
2. Kies de actie **Jaar afsluiten**.  

## <a name="posting-entries-to-a-closed-fiscal-year"></a>Posten boeken naar een afgesloten boekjaar
Zelfs als een boekjaar is afgesloten, kunt u er nog steeds grootboekposten naar boeken. Als u dit doet, worden de posten gemarkeerd als zijnde geboekt naar een afgesloten boekjaar en wordt het veld **Naboeking** geselecteerd. Standaard wordt het selectievakje niet weergegeven op de pagina, maar u kunt het toevoegen. De volgende stappen zijn de resultatenrekeningen te sluiten en de resultaten van het jaar over te brengen naar een rekening op de balans. Herhaal deze stappen elke keer dat u posten boekt naar een afgesloten boekjaar.

## <a name="see-also"></a>Zie ook
[De boeken sluiten](year-close-books.md)  
[Afsluitingsjaren en -perioden](year-close-years-periods.md)  
[Werken met rapportageschema's](bi-how-work-account-schedule.md)  
  





