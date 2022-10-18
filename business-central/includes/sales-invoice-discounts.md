---
author: brentholtorf
ms.topic: include
ms.date: 10/05/2022
ms.author: bholtorf
ms.openlocfilehash: 8849f1c5d33cd1f826e7f53be317cb01e513fcd1
ms.sourcegitcommit: a9c778b65925435a4099fad45b3611f310e0b203
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/12/2022
ms.locfileid: "9652150"
---
Nadat u alle artikelen op regels hebt toegevoegd, kunt u de factuurkorting voor het hele verkoopdocument berekenen door de actie **Factuurkorting berekenen** te kiezen.

De korting wordt berekend op basis van alle regels op het verkoopdocument waar het selectievakje **Factuurkorting toestaan** is gekozen. Factuurkortingen zijn standaard toegestaan. Regels met artikeltoeslagen worden bijvoorbeeld echter niet meegenomen in de berekening van de factuurkorting. Om een korting op dergelijke regels toe te passen voert u een waarde in het veld **Totale regelkorting** op de regels in.  

> [!NOTE]
> Standaard zijn de velden **Factuurkorting toestaan.** en **Totale regelkorting** verborgen op regels. Als de velden niet beschikbaar zijn, kunt u ze toevoegen door de pagina te personaliseren. Zie [Uw werkruimte personaliseren](../ui-personalization-user.md#to-start-personalizing-a-page-through-the-personalizing-banner) voor meer informatie.

> [!TIP]
> Als het veld **Factuurkorting berekenen** is geselecteerd op de pagina **Verkoopinstellingen**, wordt de factuurkorting automatisch berekend. Wanneer de berekening plaatsvindt, verschilt afhankelijk van het type verkoopdocument dat u gebruikt.
>
> Als u een verkooporder gebruikt, wordt de korting berekend wanneer u een regel toevoegt. Voor alle andere verkoopdocumenten, zoals verkoopfacturen, wordt de korting berekend wanneer u een van de volgende acties uitvoert:
>
> * Statistieken weergeven
> * Een testrapport weergeven
> * Afdrukken
> * Post

U definieert factuurkortingvoorwaarden voor een klant op de pagina **Verkoopfactuurkortingen**. De valutacode op het verkoopdocument wordt gebruikt om de factuurkortingscondities in de bijbehorende valuta te zoeken.

Als u geen factuurkortingen voor vreemde valuta hebt gedefinieerd, worden de kortingsvoorwaarden op de pagina **Verkoopfactuurkortingen** gebruikt om de korting te berekenen. De berekening gebruikt uw lokale valuta en de wisselkoers die geldig was op de boekingsdatum van het document.
