---
author: edupont04
ms.service: dynamics365-business-central
ms.topic: include
ms.date: 01/20/2021
ms.author: edupont
ms.openlocfilehash: 718845561c1a18701d20b93ebdc8339308ce7ac8
ms.sourcegitcommit: adf1a87a677b8197c68bb28c44b7a58250d6fc51
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035809"
---
Wanneer alle artikelen op de verkooporderregels zijn ingevoerd, kunt u de factuurkorting voor het hele verkoopdocument berekenen door de actie **Factuurkorting berekenen**.

Als het veld **Factuurkorting berekenen** is ingeschakeld in het venster **Verkoopinstellingen**, wordt de factuurkorting automatisch berekend als een van de volgende doet in een verkoopdocument:

* Statistieken weergeven
* Een testrapport weergeven
* Afdrukken
* Post

De korting wordt evenredig verdeeld over alle regels op het verkoopdocument voor artikelen waarvan het veld **Factuurkorting berekenen** op de verkooporderregel is ingesteld op **Ja**. Dit is de standaardinstelling voor artikelen.

De factuurkortingscondities worden gedefinieerd op de pagina **Factuurkortingen berekenen** om de factuurkorting te berekenen. De valutacode op het verkoopdocument wordt gebruikt om de factuurkortingscondities in de bijbehorende valuta te zoeken.

Als u geen factuurkortingen hebt gedefinieerd voor vreemde valuta's, worden de factuurkortingscondities die op de pagina **Factuurkortingen berekenen** zijn gedefinieerd, met bedragen in uw lokale valuta en de wisselkoers op de boekingsdatum in het verkoopdocument gebruikt om de factuurkorting in de vreemde valuta te berekenen.
