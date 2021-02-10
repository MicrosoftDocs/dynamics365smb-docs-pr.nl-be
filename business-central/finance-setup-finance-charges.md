---
title: Rentefactuurcondities instellen
description: Leer hoe u Business Central zo instelt dat u klanten op de hoogte kunt stellen van extra kosten door rentefacturen te verzenden.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment due, debt, overdue, fee, charge
ms.date: 12/03/2020
ms.author: edupont
ms.openlocfilehash: aba5ca8eb9425c11c7f8a55a08a153ee18821632
ms.sourcegitcommit: 06bfb3aa59de50d983175e68e681b9d206423242
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672024"
---
# <a name="set-up-finance-charge-terms"></a>Rentefactuurcondities instellen

Wanneer een klant niet op de vervaldatum betaalt, kunt u automatisch aanmaningskosten laten berekenen en die optellen bij de openstaande bedragen op de rekening van de klant. U kunt klanten op de hoogte stellen van de toeslagen door rentefacturen te versturen. Maar u moet eerst een code instellen die elke renteberekening vertegenwoordigt. Vervolgens kunt u deze code opgeven in het veld Rentefactuurconditie op de klantenkaarten.  

## <a name="finance-charge-terms"></a>Rentefactuurcondities

U moet rentefactuurcondities instellen voor elke berekening van financieringskosten en vervolgens de voorwaarden toewijzen aan de klant in het veld **Rentefactuurconditie** op de pagina **Klant**.

U berekent rentefacturen via de rentedagenmethode of de methode voor openstaande saldi.

* Rentedagen  
  
  Er wordt rekening gehouden met het aantal dagen dat de betalingstermijn is verstreken:  
  *Methode Rentedagen* - *Rente* = *Openstaand bedrag* x *(Dagen overschreden/Renteperiode)* x *(Rentepercentage/100)*

* Openstaand bedrag  
  
  De rentefactuur is een percentage van het openstaande bedrag:  
  *Methode Openstaand bedrag* - *Rente* = *Openstaand bedrag* x *(rentepercentage/100)*

Elke conditie in de tabel Rentefactuurcondities is bovendien gekoppeld aan de subtabel Rentefactuurtekst. Voor elke set rentefactuurcondities kunt u een begin- en/of eindtekst definiëren die in de rentefactuur wordt opgenomen.

### <a name="to-set-up-finance-charge-terms"></a>Rentefactuurcondities instellen

1. Kies het pictogram ![Lampje dat de functie Vertel me opent](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Rentefactuurcondities** in en kies de gerelateerde koppeling.  
2. Vul indien nodig de velden in.
3. Als u meer dan één combinatie van rentefactuurcondities wilt gebruiken, stelt u een code in voor elke.

    Voor elke rentefactuurconditie kunt u afzonderlijke voorwaarden specificeren, die extra kosten in zowel de lokale valuta als in vreemde valuta kunnen bevatten. U kunt aanvullende toeslagen in vreemde valuta's definiëren voor elke conditie op de pagina **Rentefactuurcondities**.
4. Kies de actie **Valuta's**.
5. Op de pagina **Valuta's voor rentefactuurcondities** definieert u voor elke conditie een valutacode en een toeslag.

    > [!NOTE]  
    > Wanneer u aanmaningskosten in een vreemde valuta maakt, worden de vreemdevalutacondities die u instelt, gebruikt om rentefacturen te maken. Als u geen condities voor rentefactuurcondities in vreemde valuta's hebt ingesteld, worden de condities in de lokale valuta die op de pagina **Rentefactuurcondities** zijn opgegeven, gebruikt en omgerekend naar de betreffende valuta.

    Voor elke rentefactuurconditie kunt u tekst opgeven die wordt afgedrukt vóór (**Begintekst**) of na (**Eindtekst**) in de posten op de rentefactuur.  
6. Kies respectievelijk de acties **Begintekst** of **Eindtekst** en vul de pagina **Rentefactuurtekst** in.
7. Als u automatisch gerelateerde waarden in de resulterende rentefactuurtekst wilt invoegen, voert u de volgende tijdelijke aanduidingen in het veld **Tekst** in.

|Tijdelijke aanduiding|Waarde|  
|-----------------|-----------|  
|%1|Inhoud van het veld **Documentdatum** in de rentefactuurkoptekst|  
|%2|Inhoud van het veld **Vervaldatum** in de rentefactuurkoptekst|  
|%3|Inhoud van het veld **Rente** in de gerelateerde rentefactuurcondities|  
|%4|Inhoud van het veld **Restbedrag** in de rentefactuurkoptekst|  
|%5|Inhoud van het veld **Rentebedrag** in de rentefactuurkoptekst|  
|%6|Inhoud van het veld **Toeslag** in de rentefactuurkoptekst|  
|%7|Het totaalbedrag van de aanmaning|  
|%8|Inhoud van het veld **Valutacode** in de rentefactuurkoptekst|  
|%9|Inhoud van het veld **Boekingsdatum** in de rentefactuurkoptekst|  

## <a name="see-also"></a>Zie ook

[Openstaande saldi innen](receivables-collect-outstanding-balances.md)  
[De termijnen en niveaus van aanmaningen instellen](finance-setup-reminders.md)  
[Financiën instellen](finance-setup-finance.md)  
