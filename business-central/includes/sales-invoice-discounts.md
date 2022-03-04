---
author: edupont04
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: ed62e60d3b5b1af2158d8adc6c411884ea4c12aa
ms.sourcegitcommit: ef80c461713fff1a75998766e7a4ed3a7c6121d0
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 02/15/2022
ms.locfileid: "8133588"
---
Wanneer alle artikelen als regels zijn ingevoerd, kunt u de factuurkorting voor het hele verkoopdocument berekenen door de actie **Factuurkorting berekenen** te kiezen.

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
