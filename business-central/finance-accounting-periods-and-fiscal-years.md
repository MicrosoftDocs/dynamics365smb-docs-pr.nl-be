---
title: Werken met boekingsperioden en boekjaren
description: Leren werken met boekhoudperioden om te definiëren wanneer uw bedrijf financiële prestaties rapporteert.
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.form: 100
ms.date: 08/25/2022
ms.author: bholtorf
ms.service: dynamics-365-business-central
---
# Werken met boekingsperioden en boekjaren

Boekhoudperioden, ook wel rapportageperioden genoemd, zijn perioden waarvoor een bedrijf of organisatie financiële prestaties rapporteert door, bijvoorbeeld, de balans of resultatenrekening te genereren. Meestal verwijzen boekhoudperioden naar het boekjaar van het bedrijf, dat verschillende boekingsperioden zoals maanden of kwartalen kan bevatten.

Voor veel bedrijven loopt het boekjaar niet gelijk met het kalenderjaar, bijvoorbeeld wanneer het boekjaar eindigt op 30 juni in plaats van op 31 december. Voor onlangs opgerichte bedrijven kan het boekjaar zelfs langer zijn dan 12 maanden.  

[!INCLUDE[prod_short](includes/prod_short.md)] vereist alleen boekhoudperioden als u een resultatenrekening wilt afsluiten of gegevenscompressietaken wilt uitvoeren.

U kunt behoudperioden gebruiken in rapportages, bijvoorbeeld als u geboekte posten op de pagina **Saldo/Budget** controleert waar het rapportage-interval wordt opgegeven. Een van de opties die u kunt opgeven, is om te rapporteren per boekhoudperiode. U kunt ook een financieel rapport maken dat resultaten voor verschillende boekhoudperioden vergelijkt.

## Een nieuw boekjaar maken

U kunt boekhoudperioden in bulk maken door de batchverwerking **Boekjaar maken** te gebruiken of dit handmatig doen.

### Boekhoudperioden in bulk maken

Gebruik de batchverwerking **Boekjaar maken** om een boekjaar in perioden van gelijke lengte op te delen.  

1. Kies het pictogram ![Pagina of rapport zoeken.](media/ui-search/search_small.png "Pictogram Pagina of rapport zoeken"), voer **Boekhoudperioden** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Jaar maken**.
3. Voer in het veld **Begindatum** de datum in waarop het boekjaar begint.  
4. Voer in het veld **Aantal perioden** het aantal boekhoudperioden in waarin u het boekjaar wilt verdelen. Er kunnen maximaal 365 perioden in een jaar vallen.  
5. Voer in het veld **Periodelengte** de duur voor elke periode in. Identifiers voor duur zijn onder andere 1M voor één maand, 1K voor één kwartaal en 1J voor één jaar.  
6. Klik op **OK**.  

### Boekhoudperioden handmatig maken

Als de boekhoudperioden in uw boekjaar verschillende duren hebben, zoals het 4-4-5 schema dat in detailhandel wordt gebruikt, kunt u het handmatig instellen.  
  
1. Kies het pictogram ![Pagina of rapport zoeken.](media/ui-search/search_small.png "Pictogram Pagina of rapport zoeken"), voer **Boekhoudperioden** in en kies vervolgens de gerelateerde koppeling.  
2. Voer in het veld **Begindatum** de datum in waarop het boekjaar begint. Het veld **Naam** bevat de naam van de maand.  
3. Kies het selectievakje **Nieuw boekjaar** om aan te geven dat dit de eerste periode in het jaar is. [!INCLUDE[prod_short](includes/prod_short.md)] gebruikt deze periode om te bepalen welke perioden aan het einde van het jaar moeten worden afgesloten.
4. Herhaal stap 2 en 3 voor elke resterende periode.  

## Een boekjaar afsluiten

Het afsluiten van het boekjaar is een van de taken voor het afsluiten van de boeken. Nadat u het boekjaar hebt afgesloten, zijn de selectievakjes **Afgesloten** en **Geblokkeerd** ingeschakeld voor alle perioden van het jaar. U kunt een boekjaar niet opnieuw openen of de selectievakjes uitschakelen.

> [!NOTE]  
> U moet altijd minimaal één open boekjaar hebben. Wanneer u een jaar afsluit, moet u ervoor zorgen dat een nieuw jaar is gemaakt. Houd er ook rekening mee dat als u een jaar afsluit, u de begindatum van het volgende jaar niet kunt wijzigen.

1. Kies het pictogram ![Pagina of rapport zoeken.](media/ui-search/search_small.png "Pictogram Pagina of rapport zoeken"), voer **Boekhoudperioden afsluiten** in en kies vervolgens de gerelateerde koppeling.  
2. Kies de actie **Jaar afsluiten**.  

## Posten boeken naar een afgesloten boekjaar

Zelfs als een boekjaar is afgesloten, kunt u er nog steeds grootboekposten naar boeken. Als u dit doet, worden de posten gemarkeerd als zijnde geboekt naar een afgesloten boekjaar en wordt het veld **Naboeking** geselecteerd. Standaard wordt het selectievakje niet weergegeven op de pagina, maar u kunt het toevoegen. De volgende stappen zijn de resultatenrekeningen te sluiten en de resultaten van het jaar over te brengen naar een rekening op de balans. Herhaal deze stappen elke keer dat u posten boekt naar een afgesloten boekjaar.

## Zie ook

[De boeken sluiten](year-close-books.md)  
[Afsluitingsjaren en -perioden](year-close-years-periods.md)  
[Werken met financiële rapporten](bi-how-work-account-schedule.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
