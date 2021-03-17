---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/25/2021
ms.author: edupont
ms.openlocfilehash: 539ee2eb2c9e4a71eacfb78d95320870128fb1d9
ms.sourcegitcommit: cb06aa973f5c767df774b0e1e199c6fbe0e85b88
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470299"
---
Wanneer alle artikelen op de orderregels zijn ingevoerd, kunt u de factuurkorting voor het hele document berekenen door de actie **Factuurkorting berekenen** te kiezen.

De korting wordt berekend op basis van alle regels in het verkoopdocument voor artikelen waarvan het veld **Factuurkorting toestaan** op de verkooporderregel **Ja** bevat. Dit is de standaardinstelling voor artikelen. Regels met artikeltoeslagen worden bijvoorbeeld niet meegenomen in de berekening van de factuurkorting. Als u op dergelijke regels een korting wilt toepassen, moet u het veld **Regelkorting %** instellen op de relevante regels.  

> [!TIP]
> Als het veld **Factuurkorting berekenen** is ingeschakeld op de pagina **Verkoopinstellingen**, wordt de factuurkorting automatisch berekend als u een van de volgende doet in een verkoopdocument:
>
> * Statistieken weergeven
> * Een testrapport weergeven
> * Afdrukken
> * Post

De factuurkortingscondities voor een klant worden gedefinieerd op de pagina **Verkoopfactuurkorting** voor de klant. De valutacode op het verkoopdocument wordt gebruikt om de factuurkortingscondities in de bijbehorende valuta te zoeken.

Als u geen factuurkortingen hebt gedefinieerd voor vreemde valuta's, worden de factuurkortingscondities die op de pagina **Factuurkortingen berekenen** zijn gedefinieerd, met bedragen in uw lokale valuta en de wisselkoers op de boekingsdatum in het verkoopdocument gebruikt om de factuurkorting in de vreemde valuta te berekenen.
