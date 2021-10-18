---
title: Artikelverwijzingen gebruiken
description: Stel verwijzingen in tussen de beschrijvingen die u en uw leverancier voor een artikel gebruiken om de artikelbeschrijving van de leverancier op inkoopdocumenten in te voegen.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: item reference, cross reference, inventory
ms.date: 06/16/2021
ms.author: edupont
ms.openlocfilehash: 4eed6fce594b0b6835020fcdddb7275489b4d160
ms.sourcegitcommit: 6ad0a834fc225cc27dfdbee4a83cf06bbbcbc1c9
ms.translationtype: HT
ms.contentlocale: nl-BE
ms.lasthandoff: 10/01/2021
ms.locfileid: "7588613"
---
# <a name="use-item-references"></a>Artikelverwijzingen gebruiken
Als u een verwijzing instelt tussen de artikelbeschrijving die u voor een artikel gebruikt, en de beschrijving die de leverancier van dat artikel gebruikt, wordt de artikelbeschrijving van de leverancier automatisch in inkoopdocumenten voor de leverancier ingevuld wanneer u het veld **Verwijzingsnr.** invult. Dezelfde functionaliteit geldt voor klantartikelnummers in verkoopdocumenten.

In de volgende procedures wordt beschreven hoe u artikelverwijzingen aan de inkoopkant gebruikt. De stappen zijn vergelijkbaar voor de verkoopkant.

> [!NOTE]
> Niet alle bedrijven gebruiken artikelreferenties, dus om de rommel op pagina's te minimaliseren hebben we de gerelateerde velden en acties verborgen. Als u besluit ze te gebruiken, kunt u de schakelaar **Artikelverwijzingen gebruiken** aanzetten op de pagina **Voorraadinstellingen**. Nadat u artikelreferenties hebt ingeschakeld, zijn de velden en acties beschikbaar op de pagina's Artikelkaart, Leverancierskaart en Klantenkaart en in verkoop- en inkoopdocumenten.

## <a name="to-start-using-item-references"></a>Artikelreferenties gaan gebruiken
1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Voorraadinstellingen** in en kies vervolgens de gerelateerde koppeling.
2. Zet de schakelaar **Artikelverwijzingen gebruiken** aan.

## <a name="to-set-up-an-item-reference-to-a-vendors-item-description"></a>Een artikelverwijzing naar de artikelbeschrijving van een leverancier instellen

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen") voer **Artikelen** in en kies vervolgens de gerelateerde koppeling.
2. Open de kaart voor een artikel waarvoor u een verwijzing wilt maken naar de artikelomschrijving die de leverancier gebruikt voor het artikel.
3. Kies de actie **Artikelverwijzingen**.

     Als u de actie **Artikelverwijzingen** niet kunt vinden, kiest u ervoor om meer opties weer te geven en zoekt u de actie vervolgens onder **Gerelateerd** > **Artikel**.
  
4. Vul op een nieuwe regel op de pagina **Artikelverwijzingsposten** de velden naar wens in. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].

## <a name="to-enter-a-vendors-item-description-on-a-purchase-order"></a>De artikelomschrijving van een leverancier invoeren in een inkooporder

1. Kies het ![Lampje dat de functie Vertel me opent.](media/ui-search/search_small.png "Vertel me wat u wilt doen"), voer **Inkooporders** in en kies vervolgens de gerelateerde koppeling
2. Maak een inkooporder voor de leverancier voor wie u een artikelverwijzing hebt ingesteld in de vorige procedure.
3. Maak een inkoopregel voor het artikel waarvoor u een artikelverwijzing hebt ingesteld in de vorige procedure.
4. Selecteer in het veld **Nr. van artikelreferentie** de artikelverwijzing die u hebt gemaakt, en kies vervolgens de knop **OK**.

Het veld **Omschrijving** op de regel wordt overschreven met de artikelomschrijving van de leverancier, zoals ingesteld in de artikelverwijzingspost.

## <a name="see-also"></a>Zie ook
[Nieuwe artikelen registreren](inventory-how-register-new-items.md)  
[Voorraad](inventory-manage-inventory.md)  
[Werken met [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]