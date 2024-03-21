---
title: Ongerealiseerde btw instellen
description: 'Als u op kas gebaseerde boekhouding gebruikt, kunt u opgeven hoe ongerealiseerde btw voor verkopen en inkopen moet worden verwerkt.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'cash, VAT, unrealized, cash-based'
ms.search.form: '118, 472, 473'
ms.date: 04/01/2021
ms.author: bholtorf
ms.service: dynamics-365-business-central
---

# Ongerealiseerde btw voor op kas gebaseerde boekhouding instellen

Als u op kas gebaseerde boekhoudingsmethoden gebruikt, kunt u [!INCLUDE[prod_short](includes/prod_short.md)] instellen om ongerealiseerde btw te verwerken.

## Grootboekrekeningen gebruiken voor ongerealiseerde btw

U kunt ervoor kiezen btw-bedragen te laten berekenen en boeken naar een tijdelijke grootboekrekening wanneer een factuur wordt geboekt. Vervolgens wordt de factuur geboekt naar de juiste grootboekrekening en opgenomen in btw-aangiften wanneer de werkelijke betaling van de factuur is geboekt. Hiervoor moet u eerst de [btw-boekingsinstellingen](finance-setup-vat.md) voltooien.

Ga als volgt te werk om rekeningen voor ongerealiseerde btw te gebruiken:

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") en voer **Grootboek instellen** in.
2. Selecteer op de pagina **Boekhoudinstellingen** het selectievakje **Ongereal. btw**.
3. Kies het pictogram **Zoeken naar pagina of rapport** ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") en voer **Btw-boekingsinstellingen** in.
4. Op de pagina **Btw-boekingsinstellingen** kiest u de btw-boekingsgroep en vervolgens de actie **Bewerken**.
5. In het veld **Ongerealiseerde btw-soort** kiest u een optie om op te geven hoe u betalingen toewijst aan het factuurbedrag (zonder btw) en het btw-bedrag zelf, en hoe btw-bedragen van de ongerealiseerde btw-rekening moeten worden overgeboekt naar de gerealiseerde rekening. De volgende tabel beschrijft de opties.

| Optie | Omschrijving |
| --- | --- |
| Leeg | Kies deze optie als u de functie voor ongerealiseerde btw niet wilt gebruiken. |
| Percentage | Zowel het btw- als het factuurbedrag worden verrekend met de betalingen in verhouding tot het betalingspercentage van het resterende factuurbedrag. Het betaalde btw-bedrag wordt van de ongerealiseerde btw-rekening overgeboekt naar de gerealiseerde btw-rekening. |
| Eerste | Eerst wordt het btw-bedrag verrekend met de betalingen en dan het factuurbedrag. Het bedrag dat van de ongerealiseerde btw-rekening wordt overgemaakt naar de btw-rekening, is dan gelijk aan het betalingsbedrag totdat de volledige btw is betaald. |
| Laatste | Eerst wordt het factuurbedrag verrekend met de betalingen en dan het btw-bedrag. In dit geval wordt er alleen een bedrag van de ongerealiseerde btw-rekening overgeboekt naar de btw-rekening als het volledige factuurbedrag, exclusief de btw, is betaald. |
| Eerste (Voll. bet.) | Eerst wordt de btw verrekend met betalingen (zoals bij de optie _Eerste_), maar er wordt pas een bedrag naar de btw-rekening overgeboekt als het volledige btw-bedrag is betaald. |
| Laatste (Voll. bet.) | Eerst wordt het factuurbedrag verrekend met betalingen (zoals bij de optie _Laatste_), maar er wordt pas een bedrag naar de btw-rekening overgeboekt als het volledige btw-bedrag is betaald. |

6. Kies in het veld **Ongerealiseerde verkoop-btw-rekening** de rekening voor ongerealiseerde verkoop-btw.

    > [!NOTE]  
    > Het btw-bedrag wordt naar deze rekening geboekt en blijft daar tot de betaling van de klant is geboekt. Daarna wordt het bedrag overgeboekt naar de rekening voor verkoop-btw.
7. Voer in het veld **Ongereal. ink.-btw-rekening** de grootboekrekening voor ongerealiseerde inkoop-btw in.

> [!NOTE]  
> Het btw-bedrag wordt naar deze rekening geboekt en blijft daar tot de betaling van de klant is geboekt. Daarna wordt het bedrag overgeboekt naar de rekening voor inkoop-btw.

## Zie ook
[Berekeningen en boekingsmethoden voor btw instellen](finance-setup-vat.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
