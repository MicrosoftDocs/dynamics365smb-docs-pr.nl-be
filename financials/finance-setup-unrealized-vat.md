---
title: Ongerealiseerde btw instellen | Microsoft Docs
description: Als u op kas gebaseerde boekhouding gebruikt, kunt u opgeven hoe ongerealiseerde btw voor verkopen en inkopen moet worden verwerkt.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: cash, VAT, unrealized, cash-based
ms.date: 04/20/2017
ms.author: bholtorf
ms.translationtype: Human Translation
ms.sourcegitcommit: a31be0f9d07e2abb591e26f6bae34c6f6e4dcda6
ms.openlocfilehash: f87da12abcd2fd513a1579dd9362159687baaab8
ms.contentlocale: nl-be
ms.lasthandoff: 05/04/2017


---

# <a name="set-up-unrealized-vat-for-cash-based-accounting"></a>Ongerealiseerde btw voor op kas gebaseerde boekhouding instellen
Als u op kas gebaseerde boekhoudingsmethoden gebruikt, kunt u [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)] instellen om ongerealiseerde btw te verwerken.

## <a name="use-general-ledger-accounts-for-unrealized-vat"></a>Grootboekrekeningen gebruiken voor ongerealiseerde btw
U kunt ervoor kiezen btw-bedragen te laten berekenen en boeken naar een tijdelijke grootboekrekening wanneer een factuur wordt geboekt. Vervolgens wordt de factuur geboekt naar de juiste grootboekrekening en opgenomen in btw-aangiften wanneer de werkelijke betaling van de factuur is geboekt. Hiervoor moet u eerst de btw-boekingsinstellingen voltooien.

Ga als volgt te werk om rekeningen voor ongerealiseerde btw te gebruiken:
1. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport") en voer **Grootboekinstellingen** in. 
2. Kies op de pagina **Boekhoudinstellingen** op het sneltabblad **Algemeen** **Meer weergeven** en kies vervolgens het selectievakje **Ongerealiseerde btw**.
3. Sluit de pagina.
4. Kies in de rechterbovenhoek het pictogram **Zoeken naar pagina of rapport** ![Zoeken naar pagina of rapport](media/ui-search/search_small.png "Pictogram Zoeken naar pagina of rapport") en voer **Btw-boekingsinstellingen** in. 
5. Op de pagina **Btw-boekingsinstellingen** kiest u de btw-boekingsgroep en vervolgens **Bewerken**. 
6. In het veld **Ongerealiseerde btw-soort** kiest u een optie om op te geven hoe u betalingen toewijst aan het factuurbedrag (zonder btw) en het btw-bedrag zelf, en hoe btw-bedragen van de ongerealiseerde btw-rekening moeten worden overgeboekt naar de gerealiseerde rekening. De volgende tabel beschrijft de opties.

| Optie | Omschrijving |
| --- | --- |
| Leeg | Kies deze optie als u de functie voor ongerealiseerde btw niet wilt gebruiken. |
| Percentage | Zowel het btw- als het factuurbedrag worden verrekend met de betalingen in verhouding tot het betalingspercentage van het resterende factuurbedrag. Het betaalde btw-bedrag wordt van de ongerealiseerde btw-rekening overgeboekt naar de gerealiseerde btw-rekening. |
| Eerste | Eerst wordt het btw-bedrag verrekend met de betalingen en dan het factuurbedrag. Het bedrag dat van de ongerealiseerde btw-rekening wordt overgemaakt naar de btw-rekening, is dan gelijk aan het betalingsbedrag totdat de volledige btw is betaald. |
| Laatste | Eerst wordt het factuurbedrag verrekend met de betalingen en dan het btw-bedrag. In dit geval wordt er alleen een bedrag van de ongerealiseerde btw-rekening overgeboekt naar de btw-rekening als het volledige factuurbedrag, exclusief de btw, is betaald. |
| Eerste (Voll. bet.) | Eerst wordt de btw verrekend met betalingen (zoals bij de optie _Eerste_), maar er wordt pas een bedrag naar de btw-rekening overgeboekt als het volledige btw-bedrag is betaald. |
| Laatste (Voll. bet.) | Eerst wordt het factuurbedrag verrekend met betalingen (zoals bij de optie _Laatste_), maar er wordt pas een bedrag naar de btw-rekening overgeboekt als het volledige btw-bedrag is betaald. |

6. Kies in het veld **Ongerealiseerde verkoop-btw-rekening** de rekening voor ongerealiseerde verkoop-btw.

    **Opmerking**: het btw-bedrag wordt naar deze rekening geboekt en blijft daar tot de betaling van de klant is geboekt. Daarna wordt het bedrag overgeboekt naar de rekening voor verkoop-btw.
7. Voer in het veld **Ongerealiseerde inkoop-btw-rekening** de grootboekrekening voor ongerealiseerde inkoop-btw in.

    **Opmerking**: het btw-bedrag wordt naar deze rekening geboekt en blijft daar tot de betaling van de klant is geboekt. Daarna wordt het bedrag overgeboekt naar de rekening voor verkoop-btw.

## <a name="see-also"></a>Zie ook
[Btw instellen](finance-setup-vat.md)
